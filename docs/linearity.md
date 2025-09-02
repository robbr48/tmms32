---
title: 4a. Linearity
parent: 4. Model Simplification
layout: default
nav_order: 1
---

## 4a. Linearity

Which of he following ODE equations are linear?

1. $2\dot{x}+10\sin{(x)} = 0$
2. $2\ddot{x}-10x = 0$
3. $2\dot{x}-5x^2 = 0$

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

1. Non-linear
2. Linear
3. Non-linear

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
An ODE is linear if it satisfies $f(x_1+x_2) = f(x_1)+f(x_2)$.

**Equation 1:**

$f(x_1 +x_2) = 2\dot{x}_1 + 2\dot{x}_2 + 10\sin{(x_1 +x_2)}$

$f(x_1) + f(x_2) = 2\dot{x}_1+10\sin{(x_1)} + 2\dot{x}_2+10\sin{(x_2)}$

Not linear, because $f(x_1+x_2) \ne f(x_1) + f(x_2)$.

**Equation 2:**

$f(x_1 +x_2) = 2\ddot{x}_1 + 2\ddot{x}_2 - 10x_1 - 10x_2$

$f(x_1) + f(x_2) = 2\ddot{x}_1-10x_1 + 2\ddot{x}_2-10x_2$

Linear, because $f(x_1+x_2) = f(x_1) + f(x_2)$.

**Equation 3:**

$f(x_1 +x_2) = 2\dot{x}_1 + 2\dot{x}_2 - 5(x_1 +x_2)^2 = 2\dot{x}_1 + 2\dot{x}_2 - 5x_1^2-10x_1x_2-5x_2 ^2$

$f(x_1) + f(x_2) = 2\dot{x}_1-5x_1^2 + 2\dot{x}_2-5x_2^2 $

Not linear, because $f(x_1+x_2) \ne f(x_1) + f(x_2)$.

{::nomarkdown}</details>{:/nomarkdown}
