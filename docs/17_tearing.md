---
title: 17. Tearing
layout: default
nav_order: 17
---

## Tearing
Two hydraulic orifices are connected in series, according to the figure. Assume laminar flow ($q=K\cdot \Delta p$). The supply pressure is $p_s=20\ \mathrm{MPa}$. The two orifices have laminar flow coefficients of $K_1=1\cdot 10^{-11}$ and $K_2=3\cdot 10^{-11}$, respectively.

<img src="../assets/images/orifices.png" width="300">

$q=K_1(p_s-p)$\
$q=K_2 p$

Calculate the pressure and flow by *tearing* the equations, using the flow $q$ as tearing variable. Use $q=1.6\cdot 10^{-4}\ \mathrm{ m^3}/\mathrm{s}$ as an initial guess. Iterate five times.
 $x(0)=2$. Iterate three steps using Newton iteration.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
$p = 5\cdot 10^6\ \mathrm{Pa}$\
$q = 1.5\cdot 10^{-4}\ \mathrm{m^3}/\mathrm{s}$

{::nomarkdown}</details>{:/nomarkdown}



{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}

Residual function: 
$\hat{q} = K_1(p_s-p)$

First iteration:

$p^{(1)} = \dfrac{\hat{q}}{K_2} = \dfrac{1.6\cdot 10^{-4}}{3\cdot 10^{-11}} = 5.33\cdot 10^6\ \mathrm{Pa}$\
$\hat{q} = K_1(p_s-p^{(1)}) = 1\cdot 10^{-11}(20\cdot 10^6-5.33\cdot 10^6)=1.467\cdot 10^{-4}\ \mathrm{m^3}/\mathrm{s}$

Second iteration:

$p^{(2)} = \dfrac{\hat{q}}{K_2} = \dfrac{1.467\cdot 10^{-4}}{3\cdot 10^{-11}} = 4.89\cdot 10^6\ \mathrm{Pa}$\
$\hat{q} = K_1(p_s-p^{(2)}) = 1\cdot 10^{-11}(20\cdot 10^6-4.89\cdot 10^6)=1.511\cdot 10^{-4}\ \mathrm{m^3}/\mathrm{s}$

Third iteration:

$p^{(3)} = 5.04\cdot 10^6\ \mathrm{Pa}$\
$\hat{q} = 1.496\cdot 10^{-4}\ \mathrm{m^3}/\mathrm{s}$

Forth iteration:

$p^{(4)} = 4.99\cdot 10^6\ \mathrm{Pa}$\
$\hat{q} = 1.501\cdot 10^{-4}\ \mathrm{m^3}/\mathrm{s}$

Fifth iteration:

$p^{(5)} = 5.00\cdot 10^6\ \mathrm{Pa}$\
$\hat{q} = 1.500\cdot 10^{-4}\ \mathrm{m^3}/\mathrm{s}$

{::nomarkdown}</details>{:/nomarkdown}
