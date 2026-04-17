---
name: emri-teukolsky-solvers
description: Teukolsky equation solvers (Leaver/MST/direct integration) - applicability, failure modes, common misconceptions
type: knowledge
---

# Teukolsky Equation Solvers: Applicability and Common Misconceptions

## Applicability Comparison

| Region | Leaver | MST | Recommended |
|--------|--------|-----|-------------|
| General real freq, |aw|<5, k!=0 | OK | OK | Either |
| **High freq** |aw|>>1 | **OK** | slow convergence | **Leaver** |
| **Superradiant** k->0 | **fails** | **OK** | **MST** |
| QNM complex freq | original use | needs regularization | **Leaver** |
| PN analytic expansion | unsuitable | optimal | **MST** |

**Key insight**: Leaver is more robust at high frequency. The common belief "Leaver=low freq, MST=high freq" is wrong.

## Common Misconceptions

- "Low freq use Leaver, high freq use MST" -> Wrong: MST converges slowly at high freq
- "Leaver only for QNM" -> Wrong: works for real-freq R_in too (truncated continued fraction)
- "MST and Leaver are independent" -> Wrong: both use continued fractions to fix parameters

## Near-Extremal Kerr (a~0.99)

Both methods degrade. Use near-horizon matched asymptotic expansions.

## Key References

- Leaver (1985): Proc. R. Soc. London A 402, 285
- Mano, Suzuki, Takasugi (1996): PTP 95, 1079
- Sasaki & Tagoshi (2003): gr-qc/0306120
- Nasipak (2024): 2412.06503 - MST nu via monodromy
