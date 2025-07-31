---
title: 10. State Variables
layout: default
nav_order: 10
---

## 10. State Variables

Consider the simplified model of a DC motor driving a mechanical load. The electrical and mechanical dynamics of the system can be described by the following equations

$V(t) = L\dfrac{di(t)}{dt}+Ri(t)+K\_e\omega(t)$\
$J\dfrac{d\omega(t)}{dt}+B\omega(t) = K\_t i(t)$

with the following variables:

* $V(t)$: input voltage [V]
* $i(t)$: motor current [A]
* $\omega(t)$: angular velocity of motor shaft [rad/s]
* $L$: motor inductance [H]
* $R$: motor resistance [$\Omega$]
* $K_e$: back-emf constant [Vs/rad]
* $K_t$: motor torque constant
* $J$: moment of inertia [kg m^2]
* $B$: viscous friction [Nms/rad]

Identify the *state variables* of the system.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

$i(t)$ and $\omega(t)$

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}

We need two state variables since we have two equations. Both $i(t)$ and $\omega(t)$ appear with first-order derivatives. Knowing $i(t)$ and $\omega(t)$ allows us to predict future system behavior for a given input.

{::nomarkdown}</details>{:/nomarkdown}
