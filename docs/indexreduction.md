---
title: Index Reduction
layout: default
nav_order: 2
---

## 12. Index Reduction

Consider the following DAE system:

$\ddot{x}(t)+y(t) = \cos(t)$

$x(t)=\sin(t)$

Perform an index reduction to convert the system into an equivalent *index-1 DAE system*, which is needed for numerical simulation.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
$\ddot{x}(t)+y(t) = \cos(t)$

$ y(t)=\sin(t)+\cos(t)$

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
*Analytical solution*

Semi-explicit DAE systems of index-1 has the form

$\dot{x}=f(x,y,u)$

$0 = g(x,y,u)$

In this case, the algebraic variable $y$ does not appear in the second equation. Hence, the DAE system must have a higher index than 1.

To combine the two equations, we need $\ddot{x}$ also in the second equation. Hence, we differentiate it twice:

$\ddot{x}(t)+y(t) = \cos(t)$

$\ddot{x}(t)=-\sin(t)$

This enables us to rearrange the equations:

$\ddot{x}(t)+y(t) = \cos(t)$

$ y(t)=\sin(t)+\cos(t)$

Differentiating the both equations once would yield an ODE system. Hence, the system is now of index 1. Total number of differentiations for any of the equations to get an index-0 system is three, which means the original system was of index 3.

*Matlab solution*

```
syms x(t) y(t)
eqs = [diff(x(t),2) + y(t) == cos(t),...
       x(t) == sin(t)]
vars = [x(t), y(t)];
[eqs, vars]= reduceDifferentialOrder(eqs, vars);`
```

This yields

```
Dxtt(t) - cos(t) + y(t)
          x(t) - sin(t)
      Dxt(t) - Dxt21(t)
      Dxt21(t) - cos(t)
     Dxt21t(t) + sin(t)
    Dxtt(t) - Dxt21t(t)
```
    
 Which is an over-determined system, that can be simplified into the same answer as from the analytical solution above!

{::nomarkdown}</details>{:/nomarkdown}

