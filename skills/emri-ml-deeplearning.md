---
name: emri-ml-deeplearning
description: ML/deep learning for EMRI waveform modeling, parameter estimation, population inference - main research direction
type: knowledge
---

# EMRI x ML/Deep Learning

## Key Bottleneck

14-dim parameter space, ~10^4-10^6 local maxima, single FEW waveform ~100ms -> standard MCMC needs 10^3-10^5 CPU hours.

ML role: **accelerate inference, not replace physics models**.

## Simulation-Based Inference (Cole et al. 2025, 2505.16795)

- Method: Truncated Marginal Neural Ratio Estimation (TMNRE)
- Result: 11-dim parameter space volume compressed 10^6-10^7x
- No explicit likelihood needed

## Flow-Matching MCMC (Liang et al. 2025, 2508.00348)

- CNF generates high-likelihood initial points + PTMCMC refinement
- Solves local-maxima trapping problem
- ~10x convergence speedup

## Neural Population Simulator (Singh et al. 2025, 2508.16399)

- NN replaces detectability integral
- 10^5 EMRIs evaluated in seconds (>10^6x speedup)
- Enables hierarchical Bayesian EMRI population inference

## PINN for Teukolsky (ljq2088, 2026)

- Repo: github.com/ljq2088/SolvingTeukolskyEq
- DeepONet variant + Chebyshev expansion
- Branch MLP: (a,omega,l,m) -> Chebyshev coefficients
- Physical ansatz: R(r) = U(r)*f(y), U hardcodes asymptotics
- Open question: can it reach FEW accuracy (mismatch < 10^-3)?

## Key References

| Paper | Method | Speedup |
|-------|--------|---------|
| Cole et al. 2025 (2505.16795) | SBI/TMNRE | 10^6-10^7x param space |
| Liang et al. 2025 (2508.00348) | FM-MCMC | ~10x convergence |
| Singh et al. 2025 (2508.16399) | NN population | >10^6x detectability |
| Katz et al. 2021 (2104.04582) | FEW (NN amplitudes) | 10^4x vs direct |
