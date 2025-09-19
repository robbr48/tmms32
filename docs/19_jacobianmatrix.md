---
title: 3d. Jacobian Matrix
parent: 3. Equation-based Modelling
layout: default
nav_order: 4
---

## 3d. Jacobian Matrix

Consider the same system of equations as in the previous task:

$\mathrm{eq1: } u_R(t) - R i(t)$\
$\mathrm{eq1: } u_L(t) - L \dfrac{d}{dt}i(t) = 0$\
$\mathrm{eq1: } u_C(t) - \dfrac{1}{C}\int i(t) dt = 0$\
$\mathrm{eq1: } u_S(t) - u_R(t) - u_L(t) - u_C(t) = 0$

Construct the *Jacobian matrix* for the system.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

|         | $i$   | $u_R$ | $u_L$ | $u_C$ |
|--------:|:-----:|:-----:|:-----:|:-----:|
| **eq1** | $-R$  | $1$   | $0$   | $0$   |
| **eq2** | $0$   | $0$   | $1    | $0$   |
| **eq3** | $0$   | $0$   | $0    | $1$   |
| **eq4** | $0$   | $-1$  | $-1$  | $-1$  |

{::nomarkdown}</details>{:/nomarkdown}



{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}

The Jacobian matrix is the matrix of the partial derivative of each equation with respect to each variable. This is used e.g. for iterating using Newton's method.

Note that we only differentiate with respect to the actual variables - **not** their derivatives or integrals. 

Note that derivatives and integrals also counts. Delayed variables, in the case of *difference equations*, however does not (but this is not relevant for this task).

We use the same variable order as in the previous task: $\left[i, u_R, u_L, u_C\right]$.

Equation 1 differentiated with respect to variable $i$ is calculated as:

$\dfrac{\partial}{\partial i}\left(u_R-R i\right) = -R$

We populate now populate the Jacobian matrix by repeating this for each combination of equation and variable:

|         | $i$   | $u_R$ | $u_L$ | $u_C$ |
|--------:|:-----:|:-----:|:-----:|:-----:|
| **eq1** | -R    | 1     | 0     | 0     |
| **eq2** | 0     | 0     | 1     | 0     |
| **eq3** | 0     | 0     | 0     | 1     |
| **eq4** | 0     | -1    | -1    | -1    |

{::nomarkdown}</details>{:/nomarkdown}
