---
layout: math
---
A set of m linear equations in n unknowns (stacked in the vector x), can be written as

$$
\boldsymbol{A x=b}
$$

# Solution

- If $m=n$ (square) and $\rho(\boldsymbol{A})=n$ (invertible/nonsingular), then $x=\boldsymbol{A}^{-1} \boldsymbol{b}$;
- If $m=n$ (square) and $\rho(\boldsymbol{A})<n$ (noninvertible/singular), then there is either no solution or many solutions.
- If $m<n$, then there are many solutions (underdetermined problem). We often take the solution with the minimal norm:
$$
\min _x\|\boldsymbol{x}\| \text { such that } \boldsymbol{A} \boldsymbol{x}=\boldsymbol{b}
$$
The solution is given by $x_0=\boldsymbol{A}^{\mathrm{H}}\left(\boldsymbol{A A ^ { \mathrm { H } }}\right)^{-1} \boldsymbol{b}$, where $\boldsymbol{A}^{+}=\boldsymbol{A}^{\mathrm{H}}\left(\boldsymbol{A A ^ { \mathrm { H } }}\right)^{-1}$ is the pseudo-inverse of $\boldsymbol{A}$ for the underdetermined problem ($\rho(\boldsymbol{A})=m$).
- If $m>n$, then there is no solutions (overdetermined problem). We often take the least squares solution:
$$
\min _{\boldsymbol{x}}\|\boldsymbol{b}-\boldsymbol{A} \boldsymbol{x}\|
$$
The solution is given by $\boldsymbol{x}_0=\left(\boldsymbol{A}^{\mathrm{H}} \boldsymbol{A}\right)^{-1} \boldsymbol{A}^{\mathrm{H}} \boldsymbol{b}$, where $\boldsymbol{A}^{+}=\left(\boldsymbol{A}^{\mathrm{H}} \boldsymbol{A}\right)^{-1} \boldsymbol{A}^{\mathrm{H}}$ is the pseudo-inverse of $\boldsymbol{A}$ for the overdetermined problem ($\rho(\boldsymbol{A})=n$).

# Optimization theory

The local and global minima of an objective function $f(x)$, with $x$ real, satisfy

$$
\frac{d f(x)}{d x}=0 \quad \frac{d^2 f(x)}{d x}>0
$$

If $f(x)$ is convex, there is only one minimum, which is the global one.

For an objective function $f(z)$, with $z$ complex,
1. we rewrite $f(z)$ as $f\left(z, z^*\right)$ and treat $z$ and $z^*$ as two independent variables,
2. minimize $f\left(z, z^*\right)$ w.r.t. $z$ and $z^*$,
3. the stationary points of $f\left(z, z^*\right)$ are found by setting the derivative of $f\left(z, z^*\right)$ w.r.t. to $z$ or $z^*$ to zero,
4. but, the direction of the maximum rate of change is the gradient w.r.t. $z^*$.

For an objective function in two or more real variables, $f\left(x_1, x_2, \ldots, x_n\right)=f(\boldsymbol{x})$, the first-order derivative (gradient) and second-order derivative (Hessian) are required

$$
\left\{\nabla_x f(\boldsymbol{x})\right\}_i=\frac{\partial f(\boldsymbol{x})}{\partial x_i} \quad\left\{\boldsymbol{H}_x\right\}_{i j}=\frac{\partial^2 f(\boldsymbol{x})}{\partial x_i \partial x_j}
$$

The local and global minima of an objective function $f(\boldsymbol{x})$, with $\boldsymbol{x}$ real, satisfy

$$
\nabla_x f(x)=\mathbf{0} \quad \boldsymbol{H}_x>0
$$


