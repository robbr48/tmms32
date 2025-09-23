---
title: 3e. Matching
parent: 3. Equation-based Modelling
layout: default
nav_order: 5
---

## 3e. Matching

Consider the following equation system:

$\mathrm{eq1\colon }\enspace u(t) = R i(t)$

$\mathrm{eq2\colon }\enspace  u(t) = \dfrac{dQ(t)}{dt}$

$\mathrm{eq3\colon }\enspace  Q(t)=C u(t)$

with the state variables:

$u(t)$ (voltage)

$i(t)$ (current)

$Q(t)$ (charge)


*Match each variables with one unique equation. Is the system structurally solvable?*

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
$u(t) \rightarrow \mathrm{eq3}$\
$i(t) \rightarrow \mathrm{eq1}$\
$Q(t) \rightarrow \mathrm{eq2}$

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
For each combination of equation and variable we can determine the *cost*:

- **Low cost**: linear combinations or integration
- **High cost**: solving by numerical differentiation or risk for division-by-zero
- **Infinite cost**: variable does not appear in equation or equation cannot be inverted

Variable $u(t)$ appears in all three equations, but equation 2 would require differentiation $\left(u(t) = \dot{Q}(t)\right)$, which gives a high cost.

Variable $i(t)$ only appears in equation 1, with a low cost.

Variable $Q(t)$ appears in equations 2 and 3. Both are low cost (integration in equation 2: $Q(t) = \int u(t) dt$, and a linear combination in equation 3).

This gives us the following cost table:

|          | $u(t)$ | $i(t)$   | $Q(t)$   |
|---------:|:------:|:--------:|:--------:|
| **eq1:** | low    | low      | $\infty$ |
| **eq2:** | high   | $\infty$ | low      |
| **eq3:** | low    | $\infty$ | low      |

The only combination that gives low cost for all three variables is thus:

$u(t) \rightarrow \mathrm{eq3}$\
$i(t) \rightarrow \mathrm{eq1}$\
$Q(t) \rightarrow \mathrm{eq2}$

{::nomarkdown}</details>{:/nomarkdown}

