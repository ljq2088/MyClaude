---
name: wsl-ops
description: Canonical WSL operations from Windows Claude Code for /home/ljq/code/PINN/SolvingTeukolsky.
user-invocable: true
---

# WSL Ops

**IMPORTANT**: Do NOT use `wsl.exe` directly — shadowed by Git for Windows. Always use `powershell.exe -Command "wsl ..."`.

## Commands

```bash
# Status
powershell.exe -Command "wsl -d Ubuntu-22.04-D -- bash -lc '/home/ljq/bin/cc-wsl-bridge git-status'"

# Diff
powershell.exe -Command "wsl -d Ubuntu-22.04-D -- bash -lc '/home/ljq/bin/cc-wsl-bridge git-diff'"

# Create file
powershell.exe -Command "wsl -d Ubuntu-22.04-D -- bash -lc '/home/ljq/bin/cc-wsl-bridge write-file path/to/file content'"

# Stage exact file
powershell.exe -Command "wsl -d Ubuntu-22.04-D -- bash -lc '/home/ljq/bin/cc-wsl-bridge git-add-safe path/to/file'"

# Ask WSL Claude to analyze
powershell.exe -Command "wsl -d Ubuntu-22.04-D -- bash -lc '/home/ljq/bin/cc-wsl-bridge claude-print \"prompt\"'"
```

## Rules
- Never `git add .` unless explicitly asked
- Never use Windows-side git against `\\wsl.localhost` paths
- Prefer exact file paths
