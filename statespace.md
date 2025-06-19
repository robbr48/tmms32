## 11. State-space Representation

Consider a mass-spring-damper system modelled by a second-order differential equation:

$m\ddot{x}(t)+c\dot{x}(t)+kx(t)=F(t)$

where

* $x(t)$ = mass displacement [m]
* $\dot{x}(t)$ = mass velocity [m/s]
* $F(t)$ = external force [N]
* $m$ = mass [kg]
* $c$ = damping coefficient [Ns/m]
* $k$ = spring constant [N/m]

Rewrite the system in *state-space form*. Does the system have *direct feed-through*?

<details>
<summary>
#### Answer
</summary>

$\begin{bmatrix}\dot{z}\_1 \\\ \dot{z}\_2\end{bmatrix} = \begin{bmatrix}0 & 1 \\\ -\dfrac{k}{m} & -\dfrac{c}{m}\end{bmatrix}\begin{bmatrix}z\_1 \\\ z\_2\end{bmatrix}+ \begin{bmatrix}0 \\\ \dfrac{1}{m}\end{bmatrix}u(t)$\

$y = \begin{bmatrix}1 & 0\end{bmatrix}\begin{bmatrix}z\_1 &&& z\_2\end{bmatrix} + 0\cdot u(t)$

where

* $z_1 = x(t)$
* $z_2 = \dot{x}(t)$

The system has no direct feed-through.
</details>

<details>
<summary>{::nomarkdown}Solution{:/nomarkdown}
</summary>

The equation has only one state variable, $x$. However, it contains a second-order derivative with respect to time. State variables must have first-order derivatives. To solve this, we introduce as second state variable that is the derivative of the first one:

* $z_1 = x(t)$
* $z_2 = \dot(t)$

The system then becomes:

$m\dot{z}\_2(t)+cz\_2(t)+k z\_1(t)=F(t)$\

$z\_2 = \dot(t)$

Let us also introduce the *input* variable(s) $u(t) = F(t)$ and the *output* variable(s) $y(t) = x(t)$.

Then re-write the equations in the standard state-space form:

$\mathbf{\dot{z}} = A\mathbf{z} + B\mathbf{u}$\

$\mathbf{y} = C\mathbf{z} + D\mathbf{u}$

This gives us the system on state-space form:


$\begin{bmatrix}\dot{z}\_1 \\\ \dot{z}\_2\end{bmatrix} = \begin{bmatrix}0 & 1 \\\ -\dfrac{k}{m} & -\dfrac{c}{m}\end{bmatrix}\begin{bmatrix}z\_1 \\\ z\_2\end{bmatrix}+ \begin{bmatrix}0 \\\ \dfrac{1}{m}\end{bmatrix}u(t)$\
$y = \begin{bmatrix}1 & 0\end{bmatrix}\begin{bmatrix}z\_1 \\\ z\_2\end{bmatrix} + 0\cdot u(t)$

The output variable $y$ does not depend directly on input variable $u$, so there is *no direct feed-through*.
</details>
