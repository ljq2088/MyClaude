---
name: projects
description: 当用户提及"项目某某"时，映射到 WSL 中对应的本地代码项目。本地 WSL 版本优先于 GitHub 版本。
user-invocable: false
---

# Projects Skill

## 项目映射表

| 用户提及 | WSL 路径 | 说明 |
|---------|---------|------|
| SolvingTeukolsky / PINN | `/home/ljq/code/PINN/SolvingTeukolsky` | Teukolsky 方程 PINN 求解器，test2 分支为最新 |
| EMRI_Package | `/home/ljq/code/EMRI_Package` | EMRI 波形管道骨架，含 orbit/angular/radial 接口 |
| FEW / FastEMRIWaveforms | `/home/ljq/code/FEW2025` 或 `/home/ljq/code/FastEMRIWaveforms` | Fast EMRI Waveforms 框架 |
| GremlinEq / SWSH | `/home/ljq/code/GremlinEq` 或 `/home/ljq/code/Teukolsky_based/GremLinEqRe` | 角向方程求解 |
| Teukolsky_based | `/home/ljq/code/Teukolsky_based` | Teukolsky 相关工具集 |

## 使用规则

- 用户说"项目 X"时，查表找到对应 WSL 路径
- 若名字不完全匹配，以 WSL 本地实际目录名为准
- 访问方式：UNC 路径 `//wsl.localhost/Ubuntu-22.04-D<wsl-path>` 或 `powershell.exe -Command "wsl -d Ubuntu-22.04-D -- ..."`
- git 操作通过 wsl-worker agent 或 bridge 脚本执行
