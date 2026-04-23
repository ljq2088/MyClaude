---
name: prd-style
description: Use when drafting, revising, reviewing, or restructuring a manuscript in the style of Physical Review D, especially for gravity, cosmology, field theory, astrophysics, numerical relativity, black hole physics, and related theory/data-analysis papers.
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
  - Bash(bibtex *)
  - Bash(biber *)
---

# PRD Style

## Goal

Write and revise manuscripts in a style appropriate for Physical Review D. Collaborate with `paper-workbench` for project structure and `zotero-scholar`/Zotero MCP for citation grounding.

## Core PRD writing character

PRD prose should be: precise, technically controlled, compact but not cryptic, formal without rhetorical inflation, evidence-driven, moderate in claims, explicit about assumptions and scope.

Avoid: exaggerated novelty claims, promotional language ("very interesting", "remarkable", "obviously"), sweeping unsupported statements, conversational transitions.

Prefer: direct statements of setup/method/result/limitation/implication, careful distinction between exact/approximate/numerical/conjectural statements.

## Section-by-section guide

**Title**: identify physical system + method/phenomenon + scope. No ornament or excessive generality.

**Abstract**: state (1) problem, (2) method, (3) main result, (4) significance without overselling. Self-contained, no citations unless necessary, no undefined abbreviations.

**Introduction**: establish context -> identify problem -> explain relevance -> survey literature -> state gap -> state contribution. Not a mini-review.

**Methods/Formalism**: define conventions early, separate physical assumptions from numerical choices, explain why formulation is chosen. When code exists: verify before describing, distinguish analytic from implementation details.

**Results**: organized by scientific question. Interpret figures/tables (don't just point to them). State comparison baselines, uncertainties, regime limitations.

**Discussion/Conclusion**: summarize what is established, distinguish implications from speculation, state limitations honestly, controlled next-steps. No verbatim abstract repeat.

## Citation behavior

Use citations as part of scientific argument. Use `zotero-scholar`/Zotero MCP to identify sources, verify metadata before adding BibTeX. Cite primary sources, avoid citation dumping, never cite a source for a claim it doesn't support.

## Figure and table narration

Don't write "Figure 1 shows the result." Instead: state what physical/numerical behavior the figure demonstrates, explain axes/trends/comparisons/takeaways, mention limitations when relevant.

## Reviewer response style

Polite, direct, specific. Acknowledge valid points. Distinguish agreement from disagreement with scientific reasoning. Point to exact manuscript changes. No defensive tone.

Structure: thank referee -> restate issue precisely -> explain resolution -> quote/summarize manuscript change.

## Formula and notation

Define symbols before heavy reuse. Keep notation stable. Place secondary derivations in appendices when helpful. When revising equations, preserve scientific meaning and propagate changes consistently.

## Final checks before output

- claim strength matches evidence
- citations present where needed
- notation consistent
- paragraph transitions technically meaningful
- prose reads like PRD, not a general essay
- flag unresolved citation/evidence gaps explicitly
