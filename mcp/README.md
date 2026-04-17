# MCP Servers

Config lives at `~/.mcp.json` (NOT `~/.claude/mcp.json`).

## arxiv
- Package: `arxiv-mcp-server` (pip)
- Tools: search, get_abstract, download_paper, read_paper, semantic_search
- Env: `ARXIV_PAPER_DIR` = local paper cache directory

## arxiv-mcp (autoresearch-lab)
- Source: https://github.com/OpenResearchInstitute/autoresearch-lab
- Build: `npm run build` in `packages/arxiv-mcp/`
- Entry: `dist/index.js`

## wsl-exec
- Package: `mcp-wsl-exec` (npm)
- Purpose: run commands in WSL distro from Windows Claude
- Note: frequently times out on long commands; use bridge script instead

## zotero
- Package: `zotero-mcp` (pip)
- Requires: Zotero desktop running with local API enabled (port 23119)
- Mode: local (no API key needed)

## drawio
- Package: `@drawio/mcp` (npm, auto-installed via npx)
- Limitation: opens browser only, cannot save files locally
- Workaround: use TikZ for paper figures instead
