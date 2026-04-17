---
name: emri-post-adiabatic
description: EMRI post-adiabatic framework - 2GSF, 1PA waveforms, EOB, transition-to-plunge
type: knowledge
---

# EMRI: Post-Adiabatic Framework and 2GSF

## Expansion Hierarchy

| Order | Phase error | Requires | Status |
|-------|-------------|----------|--------|
| 0PA (adiabatic) | O(1/q) rad | dissipative 1GSF | Done (FEW) |
| 1PA | O(1) rad | conservative 1GSF + oscillatory dissipative | Partial |
| 2PA | O(q) rad | 2GSF | Frontier |

## 2GSF Waveform (Wardell et al. 2023, PRL 130, 241402)

First complete 1PA waveform:
- Quasi-circular non-spinning Schwarzschild, two-timescale expansion
- Tens of ms generation (10^4-10^6x speedup)
- Phase difference < 0.1 rad vs NR at q >= 10

## EOB + GSF (Albertini et al. 2023)

Full EOB EMRI model with spin and eccentricity, embedding 1GSF conservative info into EOB potential.

## Transition-to-Plunge (Kuchler et al. 2024, 2405.00170)

Multi-timescale derivation of transition-to-plunge, asymptotically matched to late inspiral.

## Key References

- Wardell et al. 2021 (2112.12265) - first 2GSF waveform
- Burke et al. 2023 (2310.08927) - 1PA accuracy requirements
- Lynch et al. 2024 (2405.21072) - NIT + resonance handling
- Kuchler et al. 2024 (2405.00170) - transition-to-plunge
