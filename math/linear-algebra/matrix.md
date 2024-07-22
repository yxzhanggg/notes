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

where $\boldsymbol{A}_{i j}$ is the matrix obtained by removing the $i$th row and $j$th column from $\boldsymbol{A}$.

For square matrix $\boldsymbol{A}_{n\times n}$,  
if $\operatorname{det}(\boldsymbol{A}) \neq 0$, then $\boldsymbol{A}$ is invertible/nonsingular.

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

The quadratic form of an $n × n$ Hermitian matrix $\boldsymbol{A}$ is
$$
Q_A(x)=\boldsymbol{x}^{\mathrm{H}} \boldsymbol{A} \boldsymbol{x}=\sum_{i=1}^n \sum_{j=1}^n x_i^* a_{i j} x_j
$$

| Notation                | Name                  | Inequality                                                           |
| ----------------------- | --------------------- | -------------------------------------------------------------------- |
| $\boldsymbol{A} > 0$    | Positive definite     | $Q_A(\boldsymbol{x}) > 0, \forall \boldsymbol{x} \neq \mathbf{0}$    |
| $\boldsymbol{A} \geq 0$ | Positive semidefinite | $Q_A(\boldsymbol{x}) \geq 0, \forall \boldsymbol{x} \neq \mathbf{0}$ |
| $\boldsymbol{A} < 0$    | Negative definite     | $Q_A(\boldsymbol{x}) < 0, \forall \boldsymbol{x} \neq \mathbf{0}$    |
| $\mathbf{A} \leq 0$     | Negative semidefinite | $Q_A(\boldsymbol{x}) \leq 0, \forall \boldsymbol{x} \neq \mathbf{0}$ |

For any $n \times n$ matrix $\boldsymbol{A}$ and any $n \times m(m \leq n)$ matrix $\boldsymbol{B}$ with full rank $m$, the definiteness of $\boldsymbol{A}$ and $\boldsymbol{B}^{\mathrm{H}} \boldsymbol{A} \boldsymbol{B}$ are the same.

# Eigenvalues and eigenvectors

For an $n \times n$ matrix $\boldsymbol{A}$ there are $n$ eigenvalues $\lambda_i$ and $n$ eigenvectors $\boldsymbol{v}_i$ satisfying

$$
\boldsymbol{A} \boldsymbol{v}_i=\lambda_i \boldsymbol{v}_i
$$

The eigenvalues are the roots of the characteristic polynomial

$$
p(\lambda)=\operatorname{det}(\boldsymbol{A}-\lambda \boldsymbol{I})
$$

- The eigenvectors have a scaling ambiguity and are often normalized, $\left\|\boldsymbol{v}_i\right\|=1$.
- The eigenvectors corresponding to distinct eigenvalues are linearly independent.
- If $\boldsymbol{A}$ has $\rho(\boldsymbol{A})$, then $\boldsymbol{A}$ has $\rho(\boldsymbol{A})$ nonzero eigenvalues and $n-\rho(\boldsymbol{A})$ zero eigenvalues.
- For a Hermitian matrix,
	- the eigenvalues are real;
	- the eigenvectors are orthonormal;
	- matrix positive (negative) definite $\Leftrightarrow$ all eigenvalues positive (negative).

# Eigenvalue decomposition

For an $n \times n$ matrix $\boldsymbol{A}$ with a set of $n$ linearly independent eigenvectors we can perform an eigenvalue decomposition of $\boldsymbol{A}$

$$
A=v \Lambda v^{-1}
$$

where $\boldsymbol{v}$ contains the eigenvectors and $\boldsymbol{\Lambda}$ is a diagonal matrix holding the eigenvalues.

Since for a Hermitian matrix there always exists a set of $n$ orthonormal eigenvectors, the eigenvalue decomposition can be written as

$$
\boldsymbol{A}=\boldsymbol{v} \boldsymbol{\Lambda} \boldsymbol{v}^{\mathrm{H}}=\lambda_1 \boldsymbol{v}_1 \boldsymbol{v}_1^{\mathrm{H}}+\lambda_2 \boldsymbol{v}_2 \boldsymbol{v}_2^{\mathrm{H}}+\cdots+\lambda_n \boldsymbol{v}_n \boldsymbol{v}_n^{\mathrm{H}}
$$

where $\lambda_i$ are the eigenvalues and $\boldsymbol{v}_i$ is a set of orthonormal eigenvectors.

