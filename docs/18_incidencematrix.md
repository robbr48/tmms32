---
title: 3c. Incidence Matrix
parent: 3. Equation-based Modelling
layout: default
nav_order: 3
---

## 3c. Incidence Matrix

Consider the following system of equations, describing an electric RLC circuit:

$\mathrm{eq1: } u_R(t) - R i(t)$\
$\mathrm{eq1: } u_L(t) - L \dfrac{d}{dt}i(t) = 0$\
$\mathrm{eq1: } u_C(t) - \dfrac{1}{C}\int i(t) dt = 0$\
$\mathrm{eq1: } u_S(t) - u_R(t) - u_L(t) - u_C(t) = 0$

where 

$i(t)$ = electric current

$u_R(t)$ = voltage across resistor

$u_L(t)$ = voltage across inductor

$u_C(t)$ = voltage across capacitor

$u_S(t)$ = voltage source (input)

$R,L,C$ = constants

Construct the *incidence matrix* for the system.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}
\begin{tabular}{r | c c c c}
& $i$ & $u_R $ u_L $ u_C \\
\hline
& eq1 & 1 & 1 & 0 & 0 \\
& eq2 & 1 & 0 & 1 & 0 \\
& eq3 & 1 & 0 & 0 & 1 \\
& eq4 & 0 & 1 & 1 & 1 \\
\end{tabular}

{::nomarkdown}</details>{:/nomarkdown}



{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}

The incidence matrix indicates which variables that appears in which equation. Each row corresponds to one equation, and each column to one variable. If the variable appears in the equation the element is 1, otherwise 0.

Note that derivatives and integrals also counts. Delayed variables, in the case of *difference equations*, however does not (but this is not relevant for this task).

We do not know the order of variables, so we choose an arbitrary order: $\left[i, u_R, u_L, u_C\right]$.

Equation 1 contains variables $i$ and $u_R$, but not $u_L$ and $u_C$. Hence, the first row becomes $[1 1 0 0]$.

Repeating for each equation finally yields:

$\begin{tabular}{r | c c c c}
& $i$ & $u_R $ u_L $ u_C \\
\hline
& eq1 & 1 & 1 & 0 & 0 \\
& eq2 & 1 & 0 & 1 & 0 \\
& eq3 & 1 & 0 & 0 & 1 \\
& eq4 & 0 & 1 & 1 & 1 \\
\end{tabular}$

|         | $i$   | $u_R$ | $u_L$ | $u_C$ |
|---------|-------|-------|-------|-------|
| **eq1** | $1$   | $1$   | $0$   | $0$   |
| **eq2** | $1$   | $0$   | $1$   | $0$   |
| **eq3** | $1$   | $0$   | $0$   | $1$   |
| **eq4** | $0$   | $1$   | $1$   | $1$   |

{::nomarkdown}</details>{:/nomarkdown}
