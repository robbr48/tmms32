---
title: 9. BLT Transform
layout: default
nav_order: 2
---

## 9. BLT Transform

Consider the following equation system:

$\begin{cases}x=y+z & (1) \\\ y=2 & (2) \\\ z=2-y & (3)\end{cases}$

Perform a *BLT tranasform* to make the equations sequentially solvable.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

$\begin{cases}y=2 & (2) \\\ z=2-y & (3) \\\ x=y+z & (1)\end{cases}$

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}
**Dependency matrix:**

|         | **x** | **y** | **z** |
|---------|-------|-------|-------|
| **(1)** | 1     | 1     | 1     |
| **(2)** |       | 1     |       |
| **(3)** | 1     |       | 1     |

**Dependency analysis**

Equation (1) depends on equations (2) and (3).
Equation (3) depends on equation (2).

Dependency graph:

<img src="assets/images/dependencygraph.png" width="150">

Sort the equations topologically based on the graph. We start with equation (2), that does not depend on any other equation. 

With (2) removed from the graph, (3) no longer depends on anything, so this is our second equation.

Finally, only (1) remains. The final order of the equations now becomes:

$\begin{cases}y=2 & (2) \\\ z=2-y & (3) \\\ x=y+z & (1)\end{cases}$

With dependency graph:

|         | **x** | **y** | **z** |
|---------|-------|-------|-------|
| **(1)** | 1     |       |       |
| **(2)** |       | 1     |       |
| **(3)** | 1     | 1     | 1     |

No elements above diagonal, so the system is sequentially solvable!

{::nomarkdown}</details>{:/nomarkdown}
