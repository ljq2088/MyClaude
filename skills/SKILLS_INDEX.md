# Skills 目录

## EMRI 物理知识模块

| 文件 | 内容 |
|------|------|
| [emri-kerr-geodesics.md](emri-kerr-geodesics.md) | Kerr 测地线、三基本频率、动作角变量、共振动力学 |
| [emri-teukolsky-flux.md](emri-teukolsky-flux.md) | Teukolsky 方程、边界条件、辐射通量、绝热演化 |
| [emri-teukolsky-solvers.md](emri-teukolsky-solvers.md) | Leaver/MST/直接积分适用域、失效条件、常见误区 |
| [emri-gsf-selfforce.md](emri-gsf-selfforce.md) | MiSaTaQuWa 方程、正则化、后绝热框架 |
| [emri-post-adiabatic.md](emri-post-adiabatic.md) | 2GSF、1PA 波形、EOB、transition-to-plunge |
| [emri-waveform-models.md](emri-waveform-models.md) | AK/NK/AAK/FEW/GSF 模型层级、精度要求、频域扩展 |
| [emri-resonances.md](emri-resonances.md) | 瞬态/持续/潮汐共振、跳变大小、探测影响 |
| [emri-gr-tests.md](emri-gr-tests.md) | no-hair 定理、标量场、Kerr 对称性破缺、ECO |
| [emri-astrophysics.md](emri-astrophysics.md) | 形成机制、事件率、LISA 探测、环境效应 |
| [emri-lisa-data-analysis.md](emri-lisa-data-analysis.md) | LISA 噪声、数据分析流程、参数估计 |

## 文献与工具

| 文件 | 内容 |
|------|------|
| [emri-paper-digest.md](emri-paper-digest.md) | 文献高效消化策略、三层阅读协议 |
| [arxiv-emri-zotero.md](arxiv-emri-zotero.md) | arXiv 搜索与 Zotero 数据库使用 |
| [gwosc.md](gwosc.md) | GWOSC 引力波数据访问 |
| [literature-reviewer.md](literature-reviewer.md) | 深度文献评审 agent，生成结构化评审报告 |
| [researcher.md](researcher.md) | 文献检索与初步筛选子代理，返回结构化结果 |

## 学习方法

| 文件 | 内容 |
|------|------|
| [emri-paper-digest.md](emri-paper-digest.md) | 文献消化、归档结构、skill 提取标准 |

## SciGym 框架

| 文件 | 内容 |
|------|------|
| [scigym.md](scigym.md) | SciGym 主入口，结构化实验循环 |
| [scigym-benchmark.md](scigym-benchmark.md) | Phase 1: 独立验证基准 |
| [scigym-gym.md](scigym-gym.md) | Phase 2: CLI/Gym 环境包装 |
| [scigym-interface.md](scigym-interface.md) | Phase 3: 硬件/集群接口 |
| [scigym-autorun.md](scigym-autorun.md) | Phase 4: AutoRun 24/7 自主实验 |
| [scigym-submit.md](scigym-submit.md) | 提交流程 |

---

## EMRI 主线优先级

1. **波形计算**：Teukolsky → FEW → GSF（最高优先级）
2. **参数估计**：Fisher 矩阵、MCMC、ML 方法
3. **GR 检验**：no-hair、标量场、ECO
4. **天文学背景**：形成机制、事件率
