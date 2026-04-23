# MyClaude

A living record of my Claude Code configuration: skills, MCP servers, subagents, and scripts.

Last updated: 2026-04-23

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
- `scigym` — Automated research machine framework (Benchmark + CLI/Gym + Interface + AutoRun)
- `nn-diagram` — TikZ/draw.io diagrams for DL papers
- `prd-grqc` — PRD-style writing for GR/GW papers
- `crossref` — Academic literature search + sci-hub download
- `wsl-ops` — Canonical WSL operations from Windows Claude
- `mcp-install-debug` — MCP installation debugging
- `zotero-scholar` — Zotero-integrated literature discussion
- `emri-paper-digest` — Structured EMRI paper reading framework
- `mma-python-call` — 从Python调用MMA kernel，含安全关闭和超时保护
- `arxiv-emri-zotero` — Daily arXiv EMRI search + Zotero import
- `gwosc` — GWOSC gravitational wave data access
- `lira-reviewer` — LiRA double reviewer agent
- `literature-reviewer` — Structured literature review
- `math-physics-derivation` — Math/physics derivation protocol
- `researcher` — Literature search subagent
- `wsl-access` — WSL filesystem access via UNC paths

### EMRI Physics Knowledge Modules
- `emri-waveform-models` — AK/NK/AAK/FEW/GSF model hierarchy
- `emri-teukolsky-flux` — Teukolsky equation, BCs, radiation flux, adiabatic evolution
- `emri-teukolsky-solvers` — Leaver/MST/direct integration applicability and misconceptions
- `emri-gsf-selfforce` — MiSaTaQuWa equation, regularization, post-adiabatic framework
- `emri-post-adiabatic` — 2GSF, 1PA waveforms, EOB, transition-to-plunge
- `emri-kerr-geodesics` — Kerr geodesics, three frequencies, action-angle variables
- `emri-resonances` — Transient/sustained/tidal resonances, detection impact
- `emri-gr-tests` — No-hair theorem, scalar fields, Kerr symmetry breaking, ECO
- `emri-astrophysics` — Formation rates, population statistics, environmental effects
- `emri-lisa-data-analysis` — TDI, source confusion, global fit, parameter estimation
- `emri-ml-deeplearning` — ML/DL for EMRI waveforms, PE, population inference
- `emri-computational-efficiency` — Speed benchmarks, acceleration techniques, LISA requirements
