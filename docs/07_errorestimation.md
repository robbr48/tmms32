---
title: 7. Error Estimation
layout: default
nav_order: 2
---

## 7. Error Estimation

Consider the following ODE:

$\begin{cases}\dot{x}(t)=-3x(t) \\\ x(0)=x\_0=1\end{cases}$


The model is simulated using forward Euler method with a step size of $h=0.2 \text{ s}$.

*Estimate* the local truncation error of the first step.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
$\hat{\tau}\_1 = 0.18$
{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
Euler integration becomes:

$x\_{n+1} = x\_n + h\cdot(-3x\_n) + ch^2$

Integration error from each step is $\tau_n=ch^2$. We first integrate one single step. This yields:

$y^*\_{n+1} = 0.4 + ch^2\quad(1)$,

where c is a constant.

Then we integrate two half steps:

$y^*\_{n+1} = 0.49 + c\left(\dfrac{h}{2}\right)^2 + c\left(\dfrac{h}{2}\right)^2 = 0.49 + \dfrac{ch^2}{2}\quad(2)$,

Combining equation (1) and (2) yields:

$0.49-0.4 = \dfrac{ch^2}{2}\Rightarrow \tau_1 = ch^2 = 2(0.49-0.4) = 0.18$
{::nomarkdown}</details>{:/nomarkdown}
