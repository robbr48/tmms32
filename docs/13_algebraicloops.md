---
title: 13. Algebraic Loops
layout: default
nav_order: 2
---

## 13. Algebraic Loops

A spring-loaded hydraulic valve is defined by the following equations:

$m\ddot{x} + c\dot{x} + k x + F\_0 + F\_s - F\_m = 0$

$F\_s = 2 C\_q wx(p\_1-p\_2\cos{\delta}$

$q = C\_q wx\sqrt{\dfrac{2}{\rho}(p\_1-p\_2)}$

where

* $x$ = spool position [m]
* $m$ = spool mass [kg]
* $c$ = viscous friction [Ns/m]
* $k$ = spring constant [N/m]
* $F\_0$ = spring preload [N]
* $F\_s$ = flow forces [N]
* $F\_m$ = force from electromagnet [N]
* $C\_q$ = flow coefficient [-]
* $w$ = area gradient [m]
* $\rho$ = fluid density [kg/m^3^]
* $\delta$ = jet angle [rad]
* $p\_1$ = upstream pressure [Pa]
* $p\_2$ = downstream pressure [Pa]
* $q$ = volumetric flow rate [m^3^/s]

Identify any algebraic loops in the model. Can it be solved sequentially?

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
There is an algebraic loop between first and second equation, which both contain the variable $x$.

In this case the two equationsa are both linear, so it is possible to eliminate the algebraic loop by eliminating variable $F\_s$ and merge the two equations.
{::nomarkdown}</details>{:/nomarkdown}
