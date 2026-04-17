---
name: emri-resonances
description: EMRI orbital resonances - transient, sustained, tidal resonances, jump sizes, detection impact
type: knowledge
---

# EMRI: Orbital Resonances

## Resonance Condition

k*Omega_r + n*Omega_theta = 0 (k,n integers)

Low-order: (k,n) = (1,1), (1,2), (2,3), ...

## Transient Resonance

Inspiral crossing causes jumps in orbital constants:
Delta_E ~ O(eps^1/2), Delta_Lz ~ O(eps^1/2), Delta_Q ~ O(eps^1/2)

Effective Hamiltonian near resonance:
H_eff = p_psi^2/2 - V0*cos(psi), V0 ~ eps^1/2

## Detection Impact (Berry et al. 2016/2017)

- Large fraction of EMRIs encounter low-order resonances in late inspiral
- Ignoring transient resonances: ~4% detectable signal loss
- Higher eccentricity: larger impact

## Handling (Lynch et al. 2024)

NIT + switching scheme: use slow "resonance phase" variable near resonance.
Phase error improved from O(eps^{-1/2}) to O(eps^{4/7}).

## Key References

- Gair, Yunes & Bender 2011 (1111.3605) - asymptotic analysis
- van de Meent 2013 (1311.4457) - sustained resonance conditions
- Berry et al. 2016 (1608.08951) - population statistics impact
- Bonga, Yang & Hughes 2019 (1905.00030) - tidal resonances
- Lynch et al. 2024 (2405.21072) - NIT switching scheme
