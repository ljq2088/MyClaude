---
name: mma-python-call
description: 从Python脚本调用Mathematica (MMA) kernel的标准方法，含安全关闭和超时保护
---

# 从 Python 调用 MMA Kernel

## 核心类：MathematicaRinSampler

位置：`/home/ljq/code/PINN/SolvingTeukolsky/mma/rin_sampler.py`

```python
from mma.rin_sampler import MathematicaRinSampler

sampler = MathematicaRinSampler(
    kernel_path="/mnt/f/mma/WolframKernel.exe",
    wl_path_win="F:/EMRI/Radial_flow/Radial_Function.wl",
    timeout_sec=8.0,
)
# 用完必须关闭
try:
    result = sampler.evaluate_rin_at_points_direct(
        s=-2, l=2, m=2, a=0.1, omega=0.1,
        r_query=np.array([3.0, 5.0, 10.0]),
        function_name="SampleRinAtPoints",  # 或 "SampleRinAtPointsMST"
    )
finally:
    sampler.close()
```

## 安全规则

### 超时保护（SIGALRM）
```python
import signal

def run_with_hard_timeout(timeout_sec, fn):
    def _handle(signum, frame):
        raise TimeoutError(f"timeout after {timeout_sec}s")
    old = signal.getsignal(signal.SIGALRM)
    try:
        signal.signal(signal.SIGALRM, _handle)
        signal.setitimer(signal.ITIMER_REAL, timeout_sec)
        return fn()
    finally:
        signal.setitimer(signal.ITIMER_REAL, 0.0)
        signal.signal(signal.SIGALRM, old)
```

### Kernel 崩溃检测
```python
def should_reset_mma_session(exc):
    text = f"{type(exc).__name__}: {exc}".lower()
    markers = ("socket exception", "failed to start", "wstp",
               "linkobject", "transport", "connection", "broken pipe")
    return any(m in text for m in markers)

# 在 classify 函数中：
try:
    result = run_with_hard_timeout(timeout, lambda: sampler.evaluate_rin_at_points_direct(...))
except Exception as exc:
    if should_reset_mma_session(exc):
        sampler.close()  # 关闭崩溃的 session
    return False, f"mma:{type(exc).__name__}"
```

### 关键原则
- **单一持久 session**：整个扫描只开一个 kernel，不要循环开关
- **finally 块保证关闭**：`try: ... finally: sampler.close()`
- **最多重启一次**：kernel 崩溃后可重建 sampler，但只允许一次
- **TimeConstrained**：在 wl 表达式层面也加超时：`wl.TimeConstrained(expr, 20)`
- **不要在循环内开关 kernel**：每次 open/close 都有几秒开销，且容易卡死

## pybhpt 调用（subprocess 隔离）

pybhpt 只在 conda env `gw_ml_env` 中可用，用 multiprocessing.spawn 隔离：

```python
import multiprocessing as mp

def _pybhpt_worker(queue, s, l, m, a, omega, r_refs):
    try:
        from pybhpt.radial import RadialTeukolsky
        rad = RadialTeukolsky(s=s, j=l, m=m, a=a, omega=omega, r=r_refs)
        rad.solve()
        vals = np.asarray(rad.radialsolutions("In"), dtype=np.complex128)
        queue.put({"ok": True, "vals": vals.tolist()})
    except Exception as exc:
        queue.put({"ok": False, "err": str(exc)})

def solve_pybhpt_timeout(s, l, m, a, omega, r_refs, timeout_sec=20.0):
    ctx = mp.get_context("spawn")
    q = ctx.Queue()
    p = ctx.Process(target=_pybhpt_worker, args=(q, s, l, m, a, omega, r_refs), daemon=True)
    p.start()
    p.join(timeout_sec)
    if p.is_alive():
        p.terminate(); p.join(1.0)
        raise TimeoutError("pybhpt timeout")
    result = q.get()
    if not result["ok"]:
        raise RuntimeError(result["err"])
    return np.array(result["vals"])
```

## 参考脚本
完整域扫描示例：`/home/ljq/code/PINN/SolvingTeukolsky/pybhpt/plot_safe_domain_scan_pybhpt.py`
