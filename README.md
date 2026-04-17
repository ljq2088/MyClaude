# MyClaude

A living record of my Claude Code configuration: skills, MCP servers, subagents, and scripts.

Last updated: 2026-04-17

## Structure

```
agents/          # Subagent definitions
skills/          # Skill files (single .md or directory with SKILL.md)
mcp/             # MCP server config and notes
```

## MCP Servers

| Name | Command | Purpose |
|------|---------|--------|
| arxiv | arxiv-mcp-server.exe | arXiv search + paper download |
| arxiv-mcp | node autoresearch-lab | Alternative arXiv MCP |
| wsl-exec | npx mcp-wsl-exec | Execute commands in WSL Ubuntu-22.04-D |
| zotero | zotero-mcp.exe | Zotero library access (local mode) |
| drawio | npx @drawio/mcp | Open draw.io diagrams in browser |

## Agents

| Name | Purpose |
|------|--------|
| paper-engineer | Draft/revise academic papers, manage LaTeX projects, code-to-paper grounding |
| toolchain-installer | Install/configure MCP servers, skills, integrations |
| wsl-worker | Git and file ops for WSL repo via bridge script |

## Skills

See `skills/` directory. Key skills:
- `nn-diagram` — TikZ/draw.io diagrams for DL papers
- `prd-grqc` — PRD-style writing for GR/GW papers
- `crossref` — Academic literature search + sci-hub download
- `wsl-ops` — Canonical WSL operations from Windows Claude
- `mcp-install-debug` — MCP installation debugging
- `zotero-scholar` — Zotero-integrated literature discussion
- EMRI physics skills: `emri-waveform-models`, `emri-computational-efficiency`, `emri-ml-deeplearning`, etc.
