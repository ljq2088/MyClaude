---
name: polish-expand-package
description: Use when polishing, expanding, packaging, sharpening, or presenting existing research writing without changing the underlying scientific meaning. Useful for turning rough notes, fragmented draft paragraphs, bullet points, code-grounded findings, or Chinese draft text into publication-ready academic prose.
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
---

# Polish Expand Package

## Goal

Improve existing writing so that it becomes clearer, more complete, more coherent, better packaged rhetorically, and more publication-ready — without changing the scientific meaning unless the user explicitly asks for conceptual revision.

This skill should often work together with:
- `paper-workbench` for project-aware file editing
- `prd-style` or `prd-grqc` for venue-appropriate tone
- `zotero-scholar` when new citation support is actually needed

## Core rule

Do not fake substance. Polishing and packaging must not:
- invent references
- create nonexistent results
- exaggerate novelty
- silently strengthen claims
- convert tentative statements into definitive ones without evidence
- pretend that an implementation has been verified if it has not

## Three operating modes

### 1. Polish
Use when the text is basically complete but awkward. Focus on sentence smoothness, paragraph flow, terminology consistency, reducing redundancy, and improving readability while preserving content exactly.

### 2. Expand
Use when the material is too compressed. Focus on unpacking hidden logical steps, restoring omitted transitions, making assumptions explicit, turning bullets or terse notes into proper prose, and supplying structure around already-available substance.

Expansion must remain evidence-preserving. Do not add scientific content that is not already supported by the source material, code, notes, or cited literature.

### 3. Package
Use when the text has content but lacks professional presentation. Focus on stronger section opening and closing sentences, clearer contribution framing, better sequencing of points, and more convincing but still honest positioning.

## Input types this skill handles well

- rough LaTeX paragraphs
- mixed Chinese and English notes
- bullet-point outlines
- fragmented methods descriptions
- raw figure captions
- response-letter drafts
- code-grounded findings that need to be written up
- heavily literal translations that need academic English packaging

## Citation rules

This skill does not add citations casually. If citations are needed:
1. first determine whether the claim truly requires external support
2. then use `zotero-scholar` or available Zotero MCP
3. verify metadata before adding or editing BibTeX entries
4. avoid citation padding merely to make the text look more academic

## Code-aware packaging

If the writing is based on code, experiments, scripts, or logs:
- inspect the materials before packaging the prose
- align terminology with the actual implementation
- do not package intended behavior as completed behavior
- if evidence is partial, package the text around that limitation honestly

## Reporting rule

After revising, briefly report:
- what was preserved
- what was expanded
- what was only packaged rhetorically
- any claims that still need evidence or citations
