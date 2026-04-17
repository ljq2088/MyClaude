---
name: nn-diagram
description: Use when creating neural network architecture diagrams or training workflow diagrams for papers. TikZ preferred for publication figures.
user-invocable: true
---

# NN Diagram

**For paper figures: prefer TikZ.** draw.io MCP cannot save locally.

## Tool preference
1. **TikZ** (default) — pdflatex, `\input{}`, publication quality
2. **draw.io MCP** — interactive only, cannot auto-save
3. **matplotlib** — last resort

## TikZ workflow
1. Read source code/config
2. Write `\documentclass[tikz,border=4pt]{standalone}`
3. `\usetikzlibrary{arrows.meta,positioning,fit,calc,backgrounds}`
4. Compile: `pdflatex <file>.tex`
5. Insert: `\input{figures/<file>}` in `figure*`

## Style (DL paper)
- `\sffamily\footnotesize` labels
- `rounded corners=3pt`
- Blue (`#DAEEFF`/`#4A86C8`): inputs
- Purple (`#EAE0F5`/`#8B5FBF`): encoders
- Green (`#D6EDD4`/`#5A9E52`): backbone
- Orange (`#FFF0DC`/`#D07A00`): fusion/loss
- Red (`#FCDEDE`/`#B84040`): output/physics
- Arrows: `{Stealth[length=4pt,width=3pt]}` color `#444444`
- Two panels: `\begin{scope}[xshift=Xcm]`
