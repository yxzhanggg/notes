---
layout: math
---
A vector is
$$
\boldsymbol{x}=\left[\begin{array}{c}
x_1 \\
x_2 \\
\vdots \\
x_N
\end{array}\right]
$$
# Transpose
$$
\boldsymbol{x}^{\mathbf{T}}=\left[\begin{array}{lll}
x_1 & x_2 & \ldots & x_N
\end{array}\right]
$$
 Complex conjugate (Hermitian) transpose:
$$
\boldsymbol{x}^{\mathbf{H}}=\left(\boldsymbol{x}^{\mathbf{T}}\right)^*=\left(\boldsymbol{x}^*\right)^{\mathbf{T}}=\left[\begin{array}{lll}
x_1^* & x_2^* & \ldots & x_N^*
\end{array}\right]
$$
# Norm
1-norm:
$$
\|\boldsymbol{x}\|_1=\sum_{i=1}^N\left|x_i\right|
$$
2-norm (Euclidean norm):
Also the "length" $\|\boldsymbol{x}\|$ of the vector.
$$
\|\boldsymbol{x}\|_2=\left(\sum_{i=1}^N\left|x_i\right|^2\right)^{1 / 2}=\left(\sum_{i=1}^N x_i^* x_i\right)^{1 / 2}=\left(\boldsymbol{x}^H \boldsymbol{x}\right)^{1 / 2}
$$
$\infty$-norm:
$$
\|\boldsymbol{x}\|_{\infty}=\max _i\left|x_i\right|
$$
# Inner Product
$$
\langle\boldsymbol{a}, \boldsymbol{b}\rangle=\boldsymbol{a}^{\mathrm{H}} \boldsymbol{b}=\sum_{i=1}^N a_i^* b_i
$$
Orthogonal if $\langle\boldsymbol{a}, \boldsymbol{b}\rangle=0$.
Orthonormal if $\|\boldsymbol{a}\|=\|\boldsymbol{b}\|=1$.
Cauchy-Schwarz:
$$
|\langle\boldsymbol{a}, \boldsymbol{b}\rangle| \leq\|\mathbf{a}\|\|\boldsymbol{b}\|
$$
Miscellaneous:
$$
2|\langle\boldsymbol{a}, \boldsymbol{b}\rangle| \leq\|\boldsymbol{a}\|^2+\|\boldsymbol{b}\|^2
$$
## Miscellaneous
Triangle:
$$
\|\boldsymbol{a}+\boldsymbol{b}\| \leq\|\boldsymbol{a}\|+\|\boldsymbol{b}\|
$$