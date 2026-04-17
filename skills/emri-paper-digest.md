---
name: emri-paper-digest
description: Use when reading or summarizing EMRI/GW physics papers. Structured framework to extract maximum value efficiently.
---

# EMRI Paper Digest Framework

## Step 1: 5-min Quick Assessment

Read title + abstract + conclusion first paragraph. Answer:
1. Core contribution? (one sentence)
2. Which tier? (methodology / physics result / review)
3. Relevance to main thread? (1-5)
   - 5: directly used in waveform calculation
   - 3: background knowledge
   - 1: peripheral

**Relevance < 3 -> record abstract only, skip deep read.**

## Step 2: Structured Deep Read (relevance >= 3)

### A. Physical Setup
- Spacetime background (Kerr / non-Kerr / perturbed)
- Orbit type (circular / eccentric / inclined / generic)
- Approximation level (geodesic / adiabatic / post-adiabatic / GSF)

### B. Core Equations/Methods
- Key equation numbers (note, don't copy)
- Relation to Teukolsky equation
- Numerical or analytic method

### C. Main Results
- Quantitative results (accuracy, speed, overlap)
- Comparison with existing models (AK/NK/AAK/FEW)
- Scope and limitations

### D. Implications for Main Thread
- Directly usable in FEW / GSF framework?
- Changes understanding of any physical effect?

## Step 3: Output Format

```markdown
## [Author Year] Title
- arXiv: xxxx.xxxxx
- Relevance: X/5
- Core contribution: (one sentence)
- Physical setup:
- Key method:
- Main results:
- Implications:
- Zotero: archived / pending
```

## Pitfalls to Avoid

- Don't deep-read every paper
- Don't record only conclusions without methods
- Don't skip the "limitations" section
- Don't spend >10 min on background references
