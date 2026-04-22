---
name: wsl-access
description: 从 Windows Claude Code 访问 WSL 文件系统的方法
---

# WSL 文件系统访问

## 直接路径访问（推荐）

Windows 可通过 UNC 路径直接读写 WSL 文件：

```
//wsl.localhost/<distro>/<path>
```

示例：
```bash
ls "//wsl.localhost/Ubuntu-22.04-D/home/ljq/code/"
cat "//wsl.localhost/Ubuntu-22.04-D/home/ljq/code/EMRI_Package/README.md"
```

用 Read/Write/Edit 工具时同样有效：
```
file_path: //wsl.localhost/Ubuntu-22.04-D/home/ljq/code/PINN/SolvingTeukolsky/trainer/losses.py
```

## 注意事项

- `mcp-wsl-exec` 经常 HCS_E_CONNECTION_TIMEOUT，优先用 UNC 路径
- git 命令在 UNC 路径下报 "dubious ownership"，无法直接用
- 发行版名称：`Ubuntu-22.04-D`，用户：`ljq`

## 常用路径

| 项目 | 路径 |
|------|------|
| SolvingTeukolsky | `//wsl.localhost/Ubuntu-22.04-D/home/ljq/code/PINN/SolvingTeukolsky` |
| EMRI_Package | `//wsl.localhost/Ubuntu-22.04-D/home/ljq/code/EMRI_Package` |
| FEW2025 | `//wsl.localhost/Ubuntu-22.04-D/home/ljq/code/FEW2025` |
