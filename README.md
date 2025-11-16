<!-- # BEM_Solver (2D): a solver based on Boundary Element Method
In this repository, we aim to build a simple two-dimensional Boundary Element Method (BEM) solver to compute the velocity field of a wave system using given surface information: surface velocity potential $\phi^S(x)$ and surface elevation $\eta(x)$.

For details of the theory, please refer to the **theory** folder in this repository.

The governing equation for the 2D wave field (irrotational and incompressible) is the Laplace equation:

$$
\nabla^2 \phi = 0
$$

The top and bottom boundary condition: 
top: $\phi = \phi^S, \; y = \eta$
bottom: $\frac{\partial \phi}{\partial n} = 0, \; y = -d$

Periodic boundary condition are applied at left ($x=0$) and right ($x=L_x$) boudaries:
$$
\frac{\partial \phi}{\partial n}_{x=0} = -\frac{\partial \phi}{\partial n}_{x=L_x} \\
\phi_{x=0} = \phi_{x=L_x}
$$ -->
# BEM_Solver (2D): a solver based on the Boundary Element Method

In this repository, we aim to build a simple two-dimensional Boundary Element Method (BEM) solver to compute the velocity field of a wave system using given surface information: the surface velocity potential $\phi^S(x)$ and the surface elevation $\eta(x)$.

For details of the theory, please refer to the **theory** folder in this repository.

---

## Governing Equation

The governing equation for a 2D irrotational and incompressible wave field is the Laplace equation:

$$
\nabla^2 \phi = 0.
$$

---

## Boundary Conditions

### Free surface (top boundary)

At the free surface $y = \eta(x)$:

$$
\phi = \phi^S(x)
$$

### Seabed (bottom boundary)

At the bottom $y = -d$, a no-flux (Neumann) condition is applied:

$$
\frac{\partial \phi}{\partial n} = 0
$$

---

## Periodic Boundary Conditions (lateral boundaries)

At the left boundary $x = 0$ and right boundary $x = L_x$, periodicity is enforced:

$$
\phi(x = 0, y) = \phi(x = L_x, y)
$$

And the normal derivative satisfies:

$$ 
\frac{\partial \phi}{\partial n}\Big|_{x=0} = -\,\frac{\partial \phi}{\partial n}\Big|_{x=L_x}
$$
