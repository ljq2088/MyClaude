---
name: emri-waveform-models
description: EMRI 波形模型层级（AK/NK/AAK/FEW/GSF）的对比、适用场景和精度要求
type: knowledge
---

# EMRI 知识模块：波形模型层级

## 模型对比表

| 模型 | 轨道动力学 | 辐射生成 | 速度 | 适用场景 |
|------|-----------|---------|------|---------|
| AK | PN（Peters+进动） | 四极矩（平直时空） | ~ms | 大规模扫描 |
| NK | 数值 Kerr 测地线 | 四极矩/八极矩 | ~s | AAK fiducial |
| AAK | 数值 Kerr 频率+AK框架 | 四极矩 | ~10ms | 搜索标准模板 |
| FEW | 绝热（Teukolsky通量） | 完整 Teukolsky 振幅 | ~100ms(GPU) | 参数估计中间层 |
| 1GSF | 一阶自力 | 完整 GSF | ~hours | 精测参考 |

## 精度层级

AK < NK ≈ AAK < FEW < 1GSF < 2GSF

## FEW 架构

离线：预计算 $Z_{lmkn}(p,e)$，稀疏网格存储
在线：插值 + GPU 并行模式求和，$\sim 10^5$ 倍加速

## 关键文献

- Barack & Cutler 2004 (gr-qc/0310125) — AK
- Katz et al. 2021 (2104.04582) — FEW
- Speri et al. 2023 (2307.12585) — FEW 频域
- Chapman-Bird et al. 2025 (2506.09470) — FEW for Kerr
