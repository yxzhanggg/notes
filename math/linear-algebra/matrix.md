---
layout: math
---
A matrix is
$$
\boldsymbol{A}=\left[a_{i j}\right]=\left[\begin{array}{cccc}
a_{11} & a_{12} & \cdots & a_{1 m} \\
a_{21} & a_{22} & \cdots & a_{2 m} \\
\vdots & \vdots & & \vdots \\
a_{n 1} & a_{n 2} & \cdots & a_{n m}
\end{array}\right]
$$

# Transpose

$$
\text{row}\leftrightarrow\text{column} \quad \left(\boldsymbol{A}^{\mathbf{T}}\right)_{i j}=\boldsymbol{A}_{j i}
$$

Complex conjugate (Hermitian) transpose:

$$
\boldsymbol{A}^{\mathrm{H}}=\left(\boldsymbol{A}^{\mathbf{T}}\right)^*=\left(\boldsymbol{A}^*\right)^\mathbf{T}
$$

Hermitian matrix:

$$
\boldsymbol{A}=\boldsymbol{A}^{\mathrm{H}}
$$

Symmetric matrix:

$$
\boldsymbol{A}=\boldsymbol{A}^{\mathrm{T}}
$$

# Inverse  
Rank: $$\rho(\boldsymbol{A})$$

$$
\rho(\boldsymbol{A})=\rho\left(\boldsymbol{A}^{\mathrm{H}}\right)=\rho\left(\boldsymbol{A A}^{\mathrm{H}}\right)=\rho\left(\boldsymbol{A}^{\mathrm{H}} \boldsymbol{A}\right)
$$

If $\boldsymbol{A}$ is square and full rank, then there is a unique $\boldsymbol{A}^{-1}$:

$$
\boldsymbol{A A}^{-1}=\boldsymbol{A}^{-1} \boldsymbol{A}=\boldsymbol{I}=\left[\begin{array}{cccc}
1 & 0 & \cdots & 0 \\
0 & 1 & \cdots & 0 \\
\vdots & \vdots & & \vdots \\
0 & 0 & \cdots & 1
\end{array}\right]
$$

For square matrix $\boldsymbol{A}_{n\times n}$,  
if $\rho(\boldsymbol{A})=n$, then $\boldsymbol{A}$ is invertible/nonsingular;  
if $\rho(\boldsymbol{A})<n$, then $\boldsymbol{A}$ is noninvertible/singular.

Properties:

$$
(\boldsymbol{A} \boldsymbol{B})^{-1}=\boldsymbol{B}^{-1} \boldsymbol{A}^{-1} \\
$$

$$
\left(\boldsymbol{A}^{\mathrm{H}}\right)^{-1}=\left(\boldsymbol{A}^{-1}\right)^{\mathrm{H}}
$$

Matrix Inverse Lemma:

$$
(\boldsymbol{A+B C D})^{-1}=\boldsymbol{A}^{-1}-\boldsymbol{A}^{-1} \boldsymbol{B}\left(\boldsymbol{C}^{-1}+\boldsymbol{D A}^{-1} \boldsymbol{B}\right)^{-1} \boldsymbol{D A}^{-1}
$$

Woodbury’s Identity (special case of Matrix Inversion Lemma):

$$
\left(\boldsymbol{A}+\boldsymbol{u} \boldsymbol{v}^{\mathrm{H}}\right)^{-1}=\boldsymbol{A}^{-1}-\frac{\boldsymbol{A}^{-1} \boldsymbol{u} \boldsymbol{v}^{\mathrm{H}} \boldsymbol{A}^{-1}}{1+\boldsymbol{v}^{\mathrm{H}} \boldsymbol{A}^{-1} \boldsymbol{u}}
$$

# Determinant

$$
\operatorname{det}(\boldsymbol{A})=\sum_{i=1}^n(-1)^{i+j} a_{i j} \operatorname{det}\left(\boldsymbol{A}_{i j}\right)
$$

where $$\boldsymbol{A}_{i j}$$ is the matrix obtained by removing the $i$th row and $j$th column from $$\boldsymbol{A}$$.

For square matrix $$\boldsymbol{A}_{n\times n}$$,  
if $$\operatorname{det}(\boldsymbol{A}) \neq 0$$, then $$\boldsymbol{A}$$ is invertible/nonsingular.

Properties:

$$
\operatorname{det}(\boldsymbol{A} \boldsymbol{B})=\operatorname{det}(\boldsymbol{A}) \operatorname{det}(\boldsymbol{B})
$$

$$
\operatorname{det}(\alpha \boldsymbol{A})=\alpha^n \operatorname{det}(\boldsymbol{A})
$$

$$
\operatorname{det}\left(\boldsymbol{A}^{-1}\right)=\frac{1}{\operatorname{det}(\boldsymbol{A})}
$$

# Trace

$$
\operatorname{tr}(\boldsymbol{A})=\sum_{i=1}^n a_{i i}
$$

# Special matrix

Diagonal and block diagonal matrix:

$$
\boldsymbol{A}=\left[\begin{array}{cccc}
a_{11} & 0 & \cdots & 0 \\
0 & a_{22} & \cdots & 0 \\
\vdots & \vdots & & \vdots \\
0 & 0 & \cdots & a_{n n}
\end{array}\right], \quad \boldsymbol{A}=\left[\begin{array}{cccc}
\boldsymbol{A}_{11} & 0 & \cdots & 0 \\
0 & \boldsymbol{A}_{22} & \cdots & 0 \\
\vdots & \vdots & & \vdots \\
0 & 0 & \cdots & \boldsymbol{A}_{k k}
\end{array}\right]
$$

Toeplitz and Hankel matrix (constant along (anti-)diagonal):

$$
\boldsymbol{A}=\left[\begin{array}{llll}
1 & 3 & 5 & 7 \\
2 & 1 & 3 & 5 \\
4 & 2 & 1 & 3 \\
6 & 4 & 2 & 1
\end{array}\right], \quad \boldsymbol{A}=\left[\begin{array}{llll}
1 & 3 & 5 & 7 \\
3 & 5 & 7 & 4 \\
5 & 7 & 4 & 2 \\
7 & 4 & 2 & 1
\end{array}\right]
$$

Unitary matrix: A square matrix $\boldsymbol{A}$ is called **unitary** if $\boldsymbol{A A ^ { H }}=I$ and $\boldsymbol{A}^{\mathrm{H}} \boldsymbol{A}=\boldsymbol{I}$, or in other words, the columns and rows of $\boldsymbol{A}$ are orthonormal.

$$
\boldsymbol{A}=\left[\begin{array}{cc}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
\frac{1}{\sqrt{2}} i & -\frac{1}{\sqrt{2}} i
\end{array}\right]
$$

# Hermitian forms


