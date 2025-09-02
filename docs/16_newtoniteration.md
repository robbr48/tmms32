---
title: 16. Newton Iteration
layout: default
nav_order: 16
---

## Newton Iteration
Consider the following differential equation:

$\dot{x}(t) = 20x(t)+x(t)^3$

Integrate the equation using backwards Euler method with a step length of $h=0.01$ and a starting value of $x(0)=2$. Iterate three steps using Newton iteration.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
x_{n+1} = 2.76393

{::nomarkdown}</details>{:/nomarkdown}



{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}

Euler integration:

$x_{n+1} = x_n + h \dot{x}_{n+1} \Rightarrow$

$x_{n+1} = x_n + h (20x+x_{n+1}^3)$

So we need to solve the equation:

$x_{n+1} - x_n - h (20x_{n+1} + x_{n+1}^3) = 0$

For readability we rename $x_{n+1}$ to $x$ and $x_n$ to $x_0$:

$x - x_0 - h (20x + x^3) = 0$ 

Newton iteration:

$x^{k+1} = x^k-\dfrac{g(x^k)}{g'(x^k)}$

where

$g(x) = x - x_0 - 20 h x - h x^3$

and

$g'(x) = 1 - 20 h - 3 h x^2$

First iteration:

$x^1 = x^0-\dfrac{x^0 - x_0 - 20 h x^0 - h (x^0)^3}{1 - 20 h - 3 h (x^0)^2} = 2-\dfrac{2 - 2 - 20\cdot 0.01\cdot 2 - 0.01\cdot 2^3}{1 - 20\cdot 0.01 - 3\cdot 0.01\cdot 2^2} = 2.70588$

Second iteration:

$x^2 = x^1-\dfrac{x^1 - x_0 - 20 h x^1 - h (x^1)^3}{1 - 20 h - 3 h (x^1)^2} = 2.70588-\dfrac{2.70588 - 2 - 20\cdot 0.01\cdot 2.70588 - 0.01\cdot 2.70588^3}{1 - 20\cdot 0.01 - 3\cdot 0.01\cdot 2.70588^2} = 2.76346$

Third iteration:

$x^3 = x^2-\dfrac{x^2 - x_0 - 20 h x^2 - h (x^2)^3}{1 - 20 h - 3 h (x^2)^2} = 2.76346-\dfrac{2.76346 - 2 - 20\cdot 0.01\cdot 2.76346 - 0.01\cdot 2.76346^3}{1 - 20\cdot 0.01 - 3\cdot 0.01\cdot 2.76346^2} = 2.76393$

{::nomarkdown}</details>{:/nomarkdown}
