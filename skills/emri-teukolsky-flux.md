---
name: emri-teukolsky-flux
description: Teukolsky 方程结构、边界条件、辐射通量计算、绝热演化方程的核心知识模块
type: knowledge
---

# EMRI 知识模块：Teukolsky 方程与辐射通量

## 1. Newman-Penrose 标量 $\Psi_4$

$\Psi_4 = C_{\mu\nu\rho\sigma}n^\mu\bar{m}^\nu n^\rho\bar{m}^\sigma$（出射引力辐射，$s=-2$）

## 2. 频域分离

$$\Psi_4 = \sum_{lm}\int d\omega\, e^{-i\omega t+im\phi}\, {}_{-2}S_{lm}^{a\omega}(\theta)\, R_{lm\omega}(r)$$

## 3. 边界条件

- **视界** ($r\to r_+$)：纯入射波 $R^{\rm in} \sim e^{-ikr_*}$，$k=\omega-m\Omega_H$
- **无穷远** ($r\to\infty$)：纯出射波 $R^{\rm up} \sim r^{-1}e^{i\omega r_*}$

## 4. 辐射振幅与通量

$$\dot{E}_{\rm GW}^{\infty} = \sum_{lmkn} \frac{|Z_{lmkn}^\infty|^2}{4\pi\omega_{mkn}^2}$$

## 5. 绝热演化

$$\dot{E} = -\dot{E}_{\rm GW}^{\infty} - \dot{E}_{\rm GW}^{H}$$

## 6. 关键参考文献

- Teukolsky 1973 — 原始方程
- Sasaki & Tagoshi 2003 (gr-qc/0306120) — BHP 综述
- Drasco & Hughes 2006 (gr-qc/0509101) — 一般轨道波形
- Katz et al. 2021 (2104.04582) — FEW 框架
