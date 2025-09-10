---
title: 2a. Stability
parent: 2. Numerical Integration
layout: default
nav_order: 1
---

## 2a. Stability

The ODE system

$\dot{x} = \begin{bmatrix}-4 & 3 \\\ -1 & 0\end{bmatrix}x$

is simulated using the forward Euler method. 

*For which values of the time step $h$ will the integration be stable?*

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
$0<h<\dfrac{2}{3}$
{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
Forward Euler is stable if $|1-h\lambda|<1$, where $\lambda$ is the worst-case eigenvalue of the system.

Compute the Eigenvalues:

$\det(\mathbf{A}-\mathbf{I}\lambda) = 0 \Rightarrow$

$(-4-\lambda)(0-\lambda) - 3\cdot (-1) = 0 \Rightarrow $

$\lambda^2 +4\lambda +3 = 0\Rightarrow \begin{cases}\lambda_1=-1\\\ \lambda_2=-3\end{cases}$

Worst case is $\lambda=-3$, which yields $0<h<\dfrac{2}{3}$.
{::nomarkdown}</details>{:/nomarkdown}

