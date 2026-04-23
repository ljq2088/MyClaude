---
name: paper-workbench
description: Use when drafting, revising, reviewing, translating, or restructuring academic papers; building local LaTeX paper projects; checking citations and bibliography consistency; or reading code to write accurate methods, experiments, and results sections.
user-invocable: true
allowed-tools:
  - Read
  - Write
  - Edit
  - Glob
  - Grep
  - Bash(ls *)
  - Bash(git status *)
  - Bash(git diff *)
  - Bash(python *)
  - Bash(latexmk *)
  - Bash(pdflatex *)
  - Bash(xelatex *)
  - Bash(bibtex *)
  - Bash(biber *)
---

# Paper Workbench

## Default local project convention

Each paper lives in: `C:\Users\12511\papers\<project-name>\`

Preferred structure:
- `main.tex`, `references.bib`, `CLAUDE.md`, `README.md`
- `sections/`, `figures/`, `tables/`, `notes/`, `scripts/`, `code/`, `output/`

## What to do first

1. Read `CLAUDE.md` at the project root
2. Identify: target journal, LaTeX engine, bibliography tool, main file, current TODOs
3. If new project, initialize structure before drafting

## Writing rules

* Preserve scientific meaning unless user requests content changes
* Never fabricate references or implementation details
* Separate verified facts from proposed wording
* Leave explicit TODO/placeholder if evidence is missing

## Citation workflow

1. Use `zotero-scholar` + Zotero MCP to find sources
2. Verify metadata before writing BibTeX entry
3. Add/update entries in `references.bib`
4. Ensure every citation key in `.tex` exists in `references.bib`

## Code-to-paper workflow

1. Locate relevant code, config, scripts, logs
2. Read implementation before drafting
3. Distinguish: verified / likely / needs rerunning
4. Write text that matches implementation and available evidence

## Output expectations

* revised `.tex` / `.bib` content
* change summary
* list of unresolved citation or evidence gaps
* code-backed explanation of methods/results if relevant
