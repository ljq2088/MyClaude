---
name: emri-gsf-selfforce
description: Gravitational self-force (GSF) theory - MiSaTaQuWa equation, regularization, post-adiabatic framework
type: knowledge
---

# EMRI: Gravitational Self-Force (GSF)

## MiSaTaQuWa Equation

$$\mu\frac{Du^\mu}{d\tau} = F^\mu_{\rm self} = F^\mu_{\rm cons} + F^\mu_{\rm diss}$$

- Dissipative: drives orbital constant evolution (E-dot, Lz-dot, Q-dot)
- Conservative: shifts orbital frequencies, no long-term average change

## Regularization (Detweiler-Whiting)

$$h_{\mu\nu}^{\rm ret} = h_{\mu\nu}^S + h_{\mu\nu}^R$$

Mode-sum regularization:
$$F^\mu_{\rm self} = \sum_l \left[F^\mu_{(l)} - A^\mu(l+\tfrac{1}{2}) - B^\mu - \frac{C^\mu}{l+\tfrac{1}{2}}\right]$$

## Expansion Hierarchy

| Order | Phase error | Requires | Status |
|-------|-------------|----------|--------|
| 0PA (adiabatic) | O(1/q) rad | dissipative 1GSF | Done (FEW) |
| 1PA (post-adiabatic) | O(1) rad | conservative 1GSF | Partial |
| 2PA | O(q) rad | 2GSF | Frontier |

## Key References

- Barack 2001 (gr-qc/0105040) - mode-sum regularization
- Pound & Wardell 2021 (2101.04592) - BHP+GSF review
- Burke et al. 2023 (2310.08927) - 1PA accuracy requirements
