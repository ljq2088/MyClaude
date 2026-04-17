---
name: emri-kerr-geodesics
description: Kerr geodesics, three fundamental frequencies, action-angle variables, resonance dynamics
type: knowledge
---

# EMRI: Kerr Geodesics and Three-Frequency Structure

## Four Constants of Motion

- mu^2 (particle mass), E=-p_t (energy), Lz=p_phi (axial angular momentum)
- Q = p_theta^2 + cos^2(theta)[a^2(mu^2-E^2) + Lz^2/sin^2(theta)] (Carter constant)

## Mino Time and Three Frequencies

Mino time lambda (dlambda = dtau/Sigma) decouples r and theta motion.

Boyer-Lindquist frequencies (Gamma = <dt/dlambda>):
$$\Omega_r = \pi/(\Lambda_r \Gamma), \quad \Omega_\theta = \pi/(\Lambda_\theta \Gamma), \quad \Omega_\phi = \Upsilon_\phi/\Gamma$$

## GW Frequency Structure

$$f_{knm} = k\Omega_r + n\Omega_\theta + m\Omega_\phi \quad \text{(discrete spectral lines)}$$

## Orbital Resonances

Resonance condition: k*Omega_r + n*Omega_theta = 0

Resonance island width: Delta ~ sqrt(epsilon), timescale: t_res ~ 1/(sqrt(epsilon)*Omega)

## Key References

- Fujita & Hikida 2009 (0906.1420) - first complete analytic three-frequency solution
- Drasco & Hughes 2006 (gr-qc/0509101) - three-frequency structure and Teukolsky waveforms
- Lynch et al. 2024 (2405.21072) - resonance handling and NIT
- Park & Nasipak 2024 (2406.01413) - KerrGeoPy Python implementation
