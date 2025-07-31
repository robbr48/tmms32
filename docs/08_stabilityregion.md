---
title: 8. Stability Region
layout: default
nav_order: 2
---

## 8. Stability Region

*Derive* expressions for the stability regions of the forward and backwards Euler methods.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

Forward Euler: $\|1+h\lambda\| < 1$

Backwards Euler: $\|1-h\lambda\| > 1$

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
We will use the stability criterion

$\|\dfrac{x\_{n+1}}{x\_n}\|<1 \quad (1)$

together with Dahlquist test equation

$\dot{x} = \lambda\cdot x \quad (2)$,

where $\lambda$ is a complex number

**Forward Euler:**

$\dot{x}\_n = \dfrac{x\_{n+1}- x\_n}{h} (3)$

(3) in (2) gives:

$\dfrac{x\_{n+1}}{x\_n}=1+h\lambda \quad (4)$

(4) in (1) gives:

$\|1+h\lambda\| < 1$

<img src="assets/images/forwardeulerstability.png" width="300">

**Backwards Euler:**

$\dot{x}\_{n+1} = \dfrac{x\_{n+1}- x\_n}{h} (5)$

(5) in (2):

$\dfrac{x\_{n+1}}{x\_n}=\dfrac{1}{1-h\lambda} \quad (4)$

(6) in (1) gives:

$\|1-h\lambda\| > 1$

<img src="assets/images/backwardseulerstability.png" width="300">
{::nomarkdown}</details>{:/nomarkdown}
