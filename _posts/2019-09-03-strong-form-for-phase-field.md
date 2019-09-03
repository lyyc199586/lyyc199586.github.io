---
layout: post
title: "Strong form for Phase Field"
categories: note
author: Yangyuanchen Liu
tag: [mechanices, phasefield]
---

> see [Implementation Details for the Phase Field Approach to Fracture](https://doi.org/10.1007/s12204-018-1922-0)

## Elastostatics

$\varOmega\subset \mathbb{R}^n, n=2,3$ is a bounded domain with a Lipschitz continuous boundary. Linear elastostatics on $\Omega$ can be formulated as minimizing the potential energy

$$
\varPi[\mathbf{u}]:=\int_\Omega \psi_0
$$