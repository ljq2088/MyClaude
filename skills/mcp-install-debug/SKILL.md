---
name: mcp-install-debug
description: Install, configure, debug MCP servers in Claude Code.
---

# MCP 安装与调试

## 核心原则
MCP 配置在 `~/.mcp.json`（**不是** `~/.claude/settings.json`）。

```json
{
  "mcpServers": {
    "server-name": {
      "command": "C:\\full\\path\\to\\exe.exe",
      "args": ["serve"],
      "env": {"KEY": "value"}
    }
  }
}
```

## 常见错误
| 错误 | 原因 | 修复 |
|------|------|------|
| 工具不出现 | 配置在 settings.json | 移到 `~/.mcp.json` |
| Server 加载失败 | args 子命令错误 | `<cmd> --help` 确认 |
| 重启后仍不出现 | 只重启了 session | 完全关闭应用再重开 |

## Windows 注意事项
- Python 脚本用 `powershell.exe -Command "python ..."` 不是 `python3`
- bash 下 `python3` exit code 49 无输出
- subprocess GBK 编码：`capture_output=True` + `.decode('utf-8', errors='replace')`
- wsl.exe 被 Git for Windows 遮蔽：改用 `powershell.exe -Command "wsl ..."`

## drawio MCP
- `npx -y @drawio/mcp`，只能打开浏览器，**不能本地保存**
- 论文图用 TikZ 代替

## 验证
```
ListMcpResourcesTool(server="server-name")
# "No resources found" = 加载成功
# "Server not found" = 未加载
```
