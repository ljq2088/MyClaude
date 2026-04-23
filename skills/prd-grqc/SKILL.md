---
name: prd-grqc
description: Use when drafting, revising, reviewing, or restructuring Physical Review D style manuscripts in general relativity and quantum cosmology adjacent areas, especially gravitational waves, black hole perturbation theory, ringdown, QNMs, numerical relativity, cosmology, field theory in curved spacetime, EMRIs, and related theory/numerics papers.
user-invocable: true
disable-model-invocation: false
allowed-tools:
  - Read
  - Write
  - Edit
  - MultiEdit
  - Glob
  - Grep
  - Bash(ls *)
  - Bash(dir *)
  - Bash(git status *)
  - Bash(git diff *)
  - Bash(python *)
  - Bash(latexmk *)
  - Bash(pdflatex *)
  - Bash(xelatex *)
  - Bash(lualatex *)
  - Bash(bibtex *)
  - Bash(biber *)
---

# PRD GRQC Style

## Goal

Write and revise manuscripts in a PRD-compatible style for gravity / gr-qc adjacent research.

This skill specializes the more general `prd-style` skill for areas such as:
- black hole perturbation theory
- gravitational waves
- ringdown and QNMs
- nonlinear gravitational-wave phenomena
- EMRIs
- Teukolsky / Regge-Wheeler / Zerilli / Kerr perturbations
- numerical relativity adjacent theory/data-analysis work
- cosmology and field theory in curved spacetime where PRD style is appropriate

It should collaborate with:
- `paper-workbench` for local project structure and build workflow
- `prd-style` for general PRD rhetoric and section logic
- `zotero-scholar` and any available Zotero MCP for citation grounding
- `polish-expand-package` only after the scientific logic is already correct

## Domain-specific writing principles

Write as a technically controlled PRD gravity paper, not as a broad popular-science narrative.

Prefer:
- explicit statement of background geometry, regime, and approximations
- clear separation between analytic setup, numerical implementation, and phenomenology
- precise language for asymptotics, boundary conditions, gauge choices, and mode content
- careful distinction between exact results, approximations, fits, heuristics, and conjectures
- explicit notation definitions before heavy reuse
- honest statements of scope, limitations, and parameter-domain validity

Avoid:
- dramatic novelty claims
- vague phrases such as "reveals deep physics" unless justified concretely
- mixing physical interpretation with implementation detail without warning
- overstating detectability, significance, or generality
- presenting code intent as if it were verified behavior

## Title and abstract behavior

For this domain, titles should usually identify:
- the physical system
- the equation/formalism or method
- the target phenomenon, observable, or numerical task

Abstracts should usually contain:
1. the concrete physics problem
2. the framework or method
3. the main result
4. the scientific use or implication
5. if relevant, the regime or assumptions under which the statement holds

Do not let the abstract become a hype paragraph.
Do not overload it with undefined abbreviations.
Do not state detectability or robustness unless the manuscript actually supports it.

## Introduction logic for gravity / gr-qc papers

A strong introduction in this domain usually follows this order:

1. Broad scientific context
2. More specific technical context
3. Literature map
4. Gap statement
5. This paper's contribution
6. Optional roadmap paragraph

## Methods / formalism logic

For formal derivations or model setup:
- define the geometry, coordinates, conventions, and units early
- state equation definitions before discussing numerical strategy
- separate: physical ansatz / mathematical reformulation / numerical discretization or training procedure
- move long algebra or engineering details to appendices if that improves readability
- preserve technical symbols and notation consistency across the paper

When the paper includes code or numerics:
- inspect the real code and config before writing the corresponding prose
- distinguish: verified implementation details / inferred implementation intent / proposed future implementation
- if uncertainty remains, leave a TODO instead of inventing text

## Results logic

Results sections should be organized by scientific question. Each results unit should contain:
1. what is being tested or shown
2. what data/figure/output supports it
3. what interpretation is justified
4. what caveat or regime restriction applies

## Domain-specific citation behavior

When citing in gravity / gr-qc:
- separate seminal references from recent refinements
- prefer primary sources where feasible
- avoid citation dumping around famous topics
- do not cite a paper for a claim it does not actually support
- distinguish: BHPT / waveform/data-analysis / detector / mathematical method / numerical implementation references

## Code-to-paper grounding

If the manuscript describes a solver, PINN, waveform reconstruction, filtering, numerical evolution, fitting pipeline, or data-analysis procedure:
1. inspect the relevant code, config, scripts, and logs
2. identify what is actually implemented
3. identify what outputs or plots already exist
4. identify what parts of the intended story are not yet supported
5. revise the manuscript so that it matches the implementation and available evidence

## Preferred rhetorical style

Use: "we consider", "we find", "we show", "within this regime", "under these assumptions", "this indicates", "this suggests", "we leave ... to future work"

Use more cautiously: "demonstrates", "establishes", "proves", "robust", "generic", "universal"

## Final checks

Before finalizing text:
1. check claim strength against evidence
2. check notation consistency
3. check citation support
4. check separation of physics, numerics, and interpretation
5. check that the prose sounds like a controlled PRD gravity paper
6. flag unresolved evidence gaps explicitly
