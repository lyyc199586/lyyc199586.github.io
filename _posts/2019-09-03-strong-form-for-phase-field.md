---
layout: post
title: "Strong form for Phase Field"
categories: note
author: Yangyuanchen Liu
tag: [mechanices, phasefield]
---

> see [Implementation Details for the Phase Field Approach to Fracture](https://doi.org/10.1007/s12204-018-1922-0)

## Elastostatics

### Energy functional

$\varOmega\subset \mathbb{R}^n, n=2,3$ is a bounded domain with a Lipschitz continuous boundary. Linear elastostatics on $\Omega$ can be formulated as minimizing the potential energy

$$
\varPi[\bm{u}]:=\int_\Omega \psi_0[\bm{\varepsilon(\bm{u})}]\mathrm{d}\varOmega - \int_{\Gamma_N} \bm{t}_N \cdot \bm{u} \mathrm{d} \Gamma - \int_\varGamma \bm{b}\cdot \bm{u} \mathrm{d}\varOmega,
$$

where

- displacement field: $u\in H^1(\varOmega;\mathbb{R}^n)$
- body force: $\bm{b}:\varOmega\rightarrow\mathbb{R}^n$
- displacement boundary condition: $\bm{u}_D:\Gamma_D\rightarrow\mathbb{R}^n$
- traction boundary condition: $\bm{t}_N:\Gamma_N\rightarrow \mathbb{R}^n$
- strain: $\bm{\varepsilon(\bm{u})} := {1\over 2} (\nabla{\bm{u}} + \nabla{\bm{u}}^T)$
- strain energy density: $\psi_0(\bm{\varepsilon}):={\lambda\over 2} (\mathrm{tr }\bm{\varepsilon})^2 + \mu\bm{\varepsilon}:\bm{\varepsilon}$

### Weak Form

Taking the first variation of (1) yields

$$
\delta\varPi[\bm{u};\bm{\bar{u}}] = \int_\varOmega \bm{\sigma}[\bm{\varepsilon(\bm{u})}]:\bm{\varepsilon(\bm{\bar{u}})}\mathrm{d}\varOmega - \int_{\varGamma_N} \bm{t}_N\cdot \bm{\bar{u}} \mathrm{d} \varGamma - \int_\varGamma \bm{b}\cdot \bm{\bar{u}} \mathrm{d} \Omega.
$$

The weak form is thus: finding $\bm{u}\in H^1(\varOmega;\mathrm{R}^n)$ with $\bm{u}=\bm{u}_D$ on $\varGamma_D$, such that for all $\bm{\bar{u}}\in H^1(\varOmega;\mathrm{R}^n)$ with $\bm{\bar{u}}=\bm{0}$ on $\varGamma_D$, $\delta\varPi[\bm{u};\bm{\bar{u}}]=0$, or,

$$
\int_\varOmega \bm{\sigma}[\bm{\varepsilon(\bm{u})}]:\bm{\varepsilon(\bm{\bar{u}})}\mathrm{d}\varOmega 
= \int_{\varGamma_N} \bm{t}_N\cdot \bm{\bar{u}} \mathrm{d} \varGamma + \int_\varGamma \bm{b}\cdot \bm{\bar{u}} \mathrm{d} \Omega.
$$

### Strong Form

Look at the LHS of (3), write it in the index form and use intergration by parts and the divergence thorem,

$$
\int_\varOmega \sigma_{ij}\bar{u}_{i,j}\mathrm{d}\varOmega
= \int_\varOmega (\sigma_{ij} \bar{u}_{i})_{,j} \mathrm{d} \varOmega
- \int_\varOmega \sigma_{ij,j} \bar{u}_{i} \mathrm{d} \varOmega\\
= \int_{\varGamma_N} \sigma_{ij} \bar{u}_{i}n_j \mathrm{d} \varGamma
- \int_\varOmega \sigma_{ij,j} \bar{u}_{i} \mathrm{d} \varOmega
$$

Combine (3) and (4) we have the strong form (the Euler-Lagrange equations) for stress:

$$
\sigma_{ij,j} + b_i = 0, \quad \text{in } \varOmega,\\
\sigma_{ij}n_j-t_i = 0,\quad \text{on } \varGamma_N,
$$

or in tensor form:

$$
\mathrm{div}\bm{\sigma[\varepsilon(u)]} + \bm{b} = \bm{0}, \quad \text{in } \varOmega,\\
\mathrm{div}\bm{\sigma[\varepsilon(u)]} \cdot \bm{n}-\bm{t}_N = \bm{0},\quad \text{on } \varGamma_N.
$$

which are the equilibrium equation and the traction boundary condition, respectively.

## Quasistatic Phase Field Formulation

