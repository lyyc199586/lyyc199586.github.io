---
layout: post
title: "FEniCS notes: Poisson equation"
categories: note
author: Yangyuanchen Liu
tag: [FEniCS, code]
excerpt_separator: <!--more-->
---

It is a "Hello, World!" program in FEniCS that solves following boundary-value problem.
<!--more-->

## Reference

> [Sovling PDEs in Python - The FEniCS Tutorial Volume I](https://fenicsproject.org/pub/tutorial/html/._ftut1004.html)

## Mathematical problem formulation

$$
- \nabla^2 u(\boldsymbol{x}) = f(\boldsymbol{x}), \boldsymbol{x} \text{ in } \Omega,
\\
u(\boldsymbol{x}) = u_D(\boldsymbol{x}), \boldsymbol{x} \text{ on } \partial\Omega.
$$

Where $u=u(\boldsymbol{x})$ is the unknown function, $f=f(\boldsymbol{x})$ is a prescribed function,  in 2D with coordinates $x$ and $y$, the Poisson equation can be written as

$$
-{\partial^2 u \over \partial x^2} - {\partial^2 u \over \partial y^2} = f(x,y).
$$

## Steps in FEniCS

1. Identify the compiutational domain $\Omega$, the PDE, its boundary conditions, and source term $f$.
2. Reformulate the PDE as a finite element variational problem.
3. Write a Python program which defines the computational domain, the variational problem, the boundary conditions, and source terms, using the corresponding FEniCS abstractions.
4. Call FEniCS to solve the boundary-value problem and , optionally, extend the program to compare derived quantities such as fluxes and averages, and visualize the results.

## Finite element variational formulation

* Poisson equation
  
$$
-\int_\Omega(\nabla^2 u) v \mathrm d x = \int_\Omega fv \mathrm d x.
$$

* After intergration by parts
  
$$
-\int_\Omega \nabla u \cdot \nabla v \mathrm d x = \int_\Omega f v \mathrm d x.
$$

* The statement of our variational problem: find $u\in V$ such that
  
$$
-\int_\Omega \nabla u \cdot \nabla v \mathrm d x = \int_\Omega f v \mathrm d x \quad\forall v \in \hat{V}.
$$

* The tiral and test space $V$ and $\hat{V}$ are in the present problem defined as
  
$$
V = \{v\in H^1(\Omega): v = u_D \text{ on } \partial \Omega\},
\\
\hat{V} = \{v\in H^1(\Omega): v = 0 \text{ on } \partial \Omega\}.
$$

* The discrete variational problem reads: find $u_h\in V_h \subset V$ such that
  
$$
-\int_\Omega \nabla u_h \cdot \nabla v \mathrm d x = \int_\Omega f v \mathrm d x \quad \forall v\in \hat{V}_h\subset \hat{V}.
$$

## Abstract finite element variational formulation

using canonical notation: find $u\in V$ such that

$$
a(u, v) = L(v)\quad \forall v\in \hat{V}.
$$

For the Poisson equation, we have:

$$
a(u, v) = \int_\Omega \nabla u \cdot \nabla v \mathrm d x,\\
L(v) = \int_\Omega fv \mathrm d x.
$$

To solve a **linear PDE** in FEniCS:

* Choose the finite element spaces $V$ and $\hat{V}$ by specifying the domain (the mesh) and the type of function space (polynomial degree and type).
* Express the PDE as a (discrete) variational problem: find $u\in V$ such that $a(u,v)=L(v)$ for all $v\in\hat{V}$.

## A test problem

* the exact solution
  
$$
u_e(x,y) = 1+ x^2 + 2y^2.
$$

* It is the solution of
  
$$
f(x,y)=-6, u_D(x,y)=u_e(x,y) = 1+ x^2 + 2y^2,
$$

* Domain $\Omega$
  
$$
\Omega=[0,1]\times[0,1].
$$

---

## Codes

Note: I am using [Colab](https://colab.research.google.com) to run FEniCS codes, colab is an online coding platform supported by Google. It is the most convenient way to play with FEniCS and share your notebook with other users.

> How to use FEniCS in Google Colab: see [colab-fenics-install](https://github.com/cmaurini/damage-course/blob/master/colab-fenics-install.ipynb) by [cmaurini](https://github.com/cmaurini).

### settings

```python
# environment setting
from dolfin import *
from mshr import *
import numpy as np
from fenics import *

import matplotlib.pyplot as plt
```

### mesh, space and boundary condition

```python
# Create mesh and define function space
mesh = UnitSquareMesh(8, 8)
V = FunctionSpace(mesh, 'P', 1)

# Define boundary condition
u_D = Expression('1 + x[0]*x[0] + 2*x[1]*x[1]', degree = 2)

def boundary(x, on_boundary):
    return on_boundary

bc = DirichletBC(V, u_D, boundary)
plot(mesh)
```

![mesh](/pic/20190807/mesh.png)

### Define problem and compute solution
  
```python
# Define variational problem
u = TrialFunction(V)
v = TestFunction(V)
f = Constant(-6.0)
a = dot(grad(u), grad(v))*dx
L = f*v*dx

# Compute solution
u = Function(V)
solve(a == L, u, bc)

# Plot solution and mesh
plot(u)
plot(mesh)
```

![solution](/pic/20190807/u.png)

### errors

```python
# Compute error in L2 norm
error_L2 = errornorm(u_D, u, 'L2')

# Compute maximum error at vertices
vertex_values_u_D = u_D.compute_vertex_values(mesh)
vertex_values_u = u.compute_vertex_values(mesh)
error_max = np.max(np.abs(vertex_values_u_D - vertex_values_u))

# Print errors
print('error_L2 = ', error_L2)
print('error_max = ', error_max)
```

```python
error_L2 =  0.008235098073354827
error_max =  1.3322676295501878e-15
```
