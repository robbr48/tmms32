## 5. Damping

Which of the following ODE systems are over-damped, under-damped or critically damped?

1. $\begin{bmatrix}\dot{x}\_1 \\\ \dot{x}\_2\end{bmatrix} = \begin{bmatrix}-2 & 1 \\\ -3 & -4\end{bmatrix}\begin{bmatrix}x_1 \\\ x_2\end{bmatrix}$

2. $\begin{bmatrix}\dot{x}\_1 \\\ \dot{x}\_2\end{bmatrix} = \begin{bmatrix} -2 & 1 \\\ 0 & -2\end{bmatrix}\begin{bmatrix}x_1 \\\ x_2\end{bmatrix}$

3. $\begin{bmatrix}\dot{x}\_1 \\\ \dot{x}\_2\end{bmatrix} = \begin{bmatrix} -2 & 1 \\\ 1 & -2\end{bmatrix}\begin{bmatrix}x_1 \\\ x_2\end{bmatrix}$

<details>
<summary>
Answer
</summary>

1. Over-damped
2. Under-damped
3. Critically damped

</details>

<details>
<summary>Solution
</summary>
A system is over-damped if it has two real but distinct eigenvalues, under-damped if it has complex eigenvalues, and critically damped if it has only one eigenvalue.

First system eigenvalues:

$\mathbf{A}-\lambda\mathbf{I} = 0 \Rightarrow (-2-\lambda)(-4-\lambda)+3=0 \Rightarrow \lambda^2+6\lambda+5=0\Rightarrow \lambda=-3\pm\sqrt(2)$

Under-damped, because eigenvalues are complex.

Second system eigenvalues:

$(-2-\lambda)(-2-\lambda)=0 \Rightarrow \lambda=-2$

Critically damped, because only one eigenvalue.

Third system eigenvalues:

$(-2-\lambda)(-2-\lambda)-1=0 \Rightarrow (-2-\lambda)^2 = \lambda=-1, -3$

Over-damped, because two distinct and real eigenvalues.

</details>
