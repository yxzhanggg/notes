---
layout: math
---
A set of m linear equations in n unknowns (stacked in the vector x), can be written as

$$
\boldsymbol{A x=b}
$$

Solution:

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
