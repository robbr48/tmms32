---
title: 2b. Truncation Error
parent: 2. Numerical Integration
layout: default
nav_order: 2
---


## 2b. Truncation Error

Consider the following ODE:

$\begin{cases}\dot{x}(t)=-3x(t) \\\ x(0)=x\_0=1\end{cases}$

With the exact solution:

$x(t) = x\_0e^{-3t}$

The model is simulated from 0 to 1 seconds using forward Euler method with a step size of $h=0.2 \text{ s}$.

Compute the *local truncation error* of the first step and the *global truncation error* at $t=1$.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

Local truncation error of first step: $\tau\_1 = 0.1488$

Global truncation error: $e\_5 = 0.03955$

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
Euler integration becomes:

$x\_{n+1} = x\_n + h\cdot(-3x\_n)$

This gives:

$x(0.2)=0.4$
$x(0.4) = 0.16$
$x(0.6) = 0.064$
$x(0.8) = 0.0256$
$x(1.0) = 0.01024$

Truncation error at $t=0$ is the difference between the exact and the calculated value at $t=0.2$:

$\tau\_1 = \|\hat{x}(0.2)-x(0.2)\| = 0.4 - 1\cdot e^{-3\cdot 0.2} = 0.1488$

Global truncation error is the difference between the exact and the calculated value at $t=1$:

$e\_5 = \|\hat{x}(0.2)-x(0.2)\| = 0.01024 - 1\cdot e^{-3\cdot 1} = 0.03955$

{::nomarkdown}</details>{:/nomarkdown}
