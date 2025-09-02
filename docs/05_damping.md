---
title: 2a. Damping
parent: 1. General Concepts
layout: default
nav_order: 2
---

## 2a. Damping

Which of the following ODE systems are over-damped, under-damped or critically damped?

1. $\begin{bmatrix}\dot{x}\_1 \\\ \dot{x}\_2\end{bmatrix} = \begin{bmatrix}-2 & 1 \\\ -3 & -4\end{bmatrix}\begin{bmatrix}x_1 \\\ x_2\end{bmatrix}$

2. $\begin{bmatrix}\dot{x}\_1 \\\ \dot{x}\_2\end{bmatrix} = \begin{bmatrix} -2 & 1 \\\ 0 & -2\end{bmatrix}\begin{bmatrix}x_1 \\\ x_2\end{bmatrix}$

3. $\begin{bmatrix}\dot{x}\_1 \\\ \dot{x}\_2\end{bmatrix} = \begin{bmatrix} -2 & 1 \\\ 1 & -2\end{bmatrix}\begin{bmatrix}x_1 \\\ x_2\end{bmatrix}$

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

1. Over-damped
2. Under-damped
3. Critically damped

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
A system is over-damped if it has two real but distinct eigenvalues, under-damped if it has complex eigenvalues, and critically damped if it has only one eigenvalue.

First system eigenvalues:

$\mathbf{A}-\lambda\mathbf{I} = 0 \Rightarrow (-2-\lambda)(-4-\lambda)+3=0 \Rightarrow \lambda^2+6\lambda+11=0\Rightarrow \lambda=-3\pm i\sqrt{2}$

Under-damped, because eigenvalues are complex.

Second system eigenvalues:

$(-2-\lambda)(-2-\lambda)=0 \Rightarrow \lambda=-2$

Critically damped, because only one eigenvalue.

Third system eigenvalues:

$(-2-\lambda)(-2-\lambda)-1=0 \Rightarrow (-2-\lambda)^2 = \lambda=-1, -3$

Over-damped, because two distinct and real eigenvalues.

{::nomarkdown}</details>{:/nomarkdown}
