---
title: 3. Solvability
layout: default
nav_order: 3
---

## 3. Solvability

Consider the following DAE:

$\begin{bmatrix}1 & 0\\\0 & 0\end{bmatrix}\dot{x}+\begin{bmatrix}0 & -1\\\a & a\end{bmatrix}x=\begin{bmatrix}1\\\0\end{bmatrix}u$

For which values of $a$ is the system solvable?

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

$a\ne 0$

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
A first-order system on the form $\mathbf{A}x=\mathbf{B}$ is solvable if $\det(\mathbf{A})\ne 0$.

We can rewrite our DAE to the same form by converting to Laplace:

$\left(\begin{bmatrix}1 & 0\\\0 & 0\end{bmatrix}s +\begin{bmatrix}0 & -1\\\a & a\end{bmatrix}\right)x=\begin{bmatrix}1\\\0\end{bmatrix}u \Rightarrow$

$\begin{bmatrix}s & -1\\\a & a\end{bmatrix}x=\begin{bmatrix}1\\\0\end{bmatrix}u $

$\det(\mathbf{A}) = \det\begin{bmatrix}s & -1\\\a & a\end{bmatrix} = a(s+1)$

As can be seen, the system is solvable assuming $a\ne 0$.
{::nomarkdown}</details>{:/nomarkdown}


