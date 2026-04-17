---
name: emri-lisa-data-analysis
description: LISA data analysis - TDI, source confusion, global fit, parameter estimation methods
type: knowledge
---

# EMRI: LISA Data Analysis

## TDI

LISA unequal arms require time-delay interferometry to cancel laser noise (~10^6x above GW signal).
Standard variables: X,Y,Z (Michelson) or A,E,T (orthogonal).

## Source Confusion

LISA band (10^{-4}-10^{-1} Hz): galactic binaries (~10^7), MBHB (tens), EMRI (tens to hundreds/yr).
All overlap in frequency -> global fit required.

## Global Fit (3 stages)

1. Galactic binaries: iterative subtraction of ~10^4 resolvable sources
2. MBHB: matched filtering (high SNR)
3. EMRI: semi-coherent search + Bayesian PE

Circular dependency: noise estimation depends on signal subtraction.

## EMRI Parameter Estimation

14-dim space: M, mu, a, p0, e0, iota0, phi0, sky position, ...

Fisher matrix precision: Delta_M/M ~ 10^{-4}-10^{-6}, Delta_a ~ 10^{-4}-10^{-7}

Main challenge: ~10^4-10^6 local maxima, MCMC needs 10^3-10^5 CPU hours.

2025 ML acceleration:
- SBI/TMNRE (Cole 2025): 10^6-10^7x parameter space compression
- FM-MCMC (Liang 2025): CNF initial points + PTMCMC
- NN population (Singh 2025): >10^6x detectability integral

## Key References

- Liang et al. 2025 (2508.00348) - FM-MCMC
- Cole et al. 2025 (2505.16795) - SBI/TMNRE
- Singh et al. 2026 (2601.15198) - hierarchical Bayesian
