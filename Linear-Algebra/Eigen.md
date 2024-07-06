---
layout: base
title: Eigens
parent: Linear Algebra
nav_order: 4
---

#### Eigenvectors

Certain exceptional vectors $x$ are in the same direction as $Ax$.

$$A \boldsymbol{x}=\lambda \boldsymbol{x}$$

![Screen Shot 2022-07-09 at 1.26.33 PM](https://live.staticflickr.com/65535/52204094088_0c3a8d4706_o.png)

#### Eigenvalues

1. **Markov matrix**: Each column of $P$ adds to 1 , so $\lambda=1$ is an eigenvalue.
2. The matrix is singular, so $\lambda=0$ is an eigenvalue.

##### Projection

$$\lambda=1 \text { and } 0$$

##### Permutation

$$|\lambda|=1$$

##### Reflection

$$\lambda=1 \text { and } -1$$

$$\text { reflection }=2(\text { projection })-I$$

$$\text { When a matrix is shifted by } I \text {, each } \lambda \text { is shifted by } 1 \text {. No change in eigenvectors. }$$

![Screen Shot 2022-07-09 at 4.04.42 PM](https://live.staticflickr.com/65535/52204295846_16bda204c3_o.png)

#### Calculation to get eigenvalues and eigenvectors

1. Compute the determinant of $A-\lambda I$. With $\lambda$ subtracted along the diagonal, this determinant starts with $\lambda^{n}$ or $-\lambda^{n}$. It is a polynomial in $\lambda$ of degree $n$.
2. Find the roots of this polynomial, by solving $\operatorname{det}(A-\lambda I)=0$. The $n$ roots are the $n$ eigenvalues of $A$. They make $A-\lambda I$ singular.
3. For each eigenvalue $\lambda$, solve $(A-\lambda I) \boldsymbol{x}=\mathbf{0}$ to find an eigenvector $\boldsymbol{x}$.

$$\lambda_{1}\lambda_{2}\cdots\lambda_{n}=\operatorname{determinant}$$

#### trace

$$\lambda_{1}+\lambda_{2}+\cdots+\lambda_{n}=\operatorname{trace}=a_{11}+a_{22}+\cdots+a_{n n}$$

#### symmetric matrix

real number

$$S^{\mathrm{T}}=S$$

#### skew-symmetric matrix

imaginary number

$$A^{\mathrm{T}}=-A$$

#### orthogonal matrix

$$\text{complex number with}|\lambda|=1$$

$$Q^{\mathrm{T}} Q=I$$

$$A \text { and } B \text { share the same } \boldsymbol{n} \text { independent eigenvectors if and only if } \boldsymbol{A B}=\boldsymbol{B A} \text {. }$$

# Diagonalization (factorization)

#### Eigenvector matrix $X$ 

#### Eigenvalue matrix $\Lambda$

$$
X^{-1} A X=\Lambda=\left[\begin{array}{lll}
\lambda_{1} & & \\
& \ddots & \\
& & \lambda_{n}
\end{array}\right]
$$

$$A X=X \Lambda \quad \text { is } \quad \boldsymbol{X}^{-1} \boldsymbol{A} \boldsymbol{X}=\boldsymbol{\Lambda} \quad \text { or } \quad \boldsymbol{A}=\boldsymbol{X} \boldsymbol{\Lambda} \boldsymbol{X}^{-1}$$

Each eigenvalue has at least one eigenvector.

- **Invertibility** is concerned with the eigenvalues $(\lambda=0$ or $\lambda \neq 0) .$
- **Diagonalizability** is concerned with the eigenvectors (too few or enough for $X$ ).

#### Independent $\boldsymbol{x}$ from different $\lambda$

Eigenvectors $x_{1}, \ldots, \boldsymbol{x}_{j}$ that correspond to distinct (all different) eigenvalues are linearly independent. An $n$ by $n$ matrix that has $n$ different eigenvalues (no repeated $\lambda$ 's) must be diagonalizable.

#### Similar Matrices

- Same Eigenvalues

$$A=X \Lambda X^{-1}$$

- all invertible matrices $B$

$$A=B C B^{-1}$$

#### Follow the eigenvectors

Decomposite the vecotors into combination of eigenvecotors, and every transformation make the eigenvectors grow by eigenvalues.

$$\boldsymbol{u}_{0}=c_{1} \boldsymbol{x}_{1}+\cdots+c_{n} \boldsymbol{x}_{n}$$

$$\boldsymbol{u}_{k}=c_{1}\left(\lambda_{1}\right)^{k} \boldsymbol{x}_{1}+\cdots+c_{n}\left(\lambda_{n}\right)^{k} \boldsymbol{x}_{n}$$

$$A^{k} u_{0}=X \Lambda^{k} X^{-1} u_{0}=X \Lambda^{k} c=\left[\begin{array}{lll}
x_{1} & \ldots & x_{n} 
\end{array}\right]\left[\begin{array}{ccc}
\left(\lambda_{1}\right)^{k} & & \\
& \ddots & \\
& & \left(\lambda_{n}\right)^{k}
\end{array}\right]\left[\begin{array}{c}
c_{1} \\
\vdots \\
c_{n}
\end{array}\right]$$

#### Geometric Multiplicity GM

Number of independent eigenvectors for specific $\lambda$.

Then GM is the dimension of the nullspace of $A-\lambda I$.

#### Algebraic Multiplicity = AM

number of repetitions of specific $\lambda$,

$n$ roots of $\operatorname{det}(A-\lambda I)=0$.

#### Diagonalizability

$A$ is diagonalizable if every eigenvalue has enough eigenvectors (GM= AM)

# Systems of Differential Equations

Choose $\boldsymbol{u}=e^{\lambda t} \boldsymbol{x}$ when $\boldsymbol{A x}=\boldsymbol{\lambda} \boldsymbol{x}$

$$\frac{d u}{d t}=A \boldsymbol{u}=A e^{\lambda t} \boldsymbol{x}=\lambda e^{\lambda t} \boldsymbol{x}$$

1. Write $\boldsymbol{u}(0)$ as a combination $c_1 \boldsymbol{x}_1+\cdots+c_n \boldsymbol{x}_n$ of the eigenvectors of $\boldsymbol{A}$.
2. Multiply each eigenvector $x_{i}$ by its **growth factor** $e^{\lambda_{i} t}$.
3. The solution is the same combination of those pure solutions $e^{\lambda t} \boldsymbol{x}$ :

$$
\frac{d u}{d t}=A u \quad u(t)=c_{1} e^{\lambda_{1} t} x_{1}+\cdots+c_{n} e^{\lambda_{n} t} x_{n}
$$

## Second order

$$m \frac{d^{2} y}{d t^{2}}+b \frac{d y}{d t}+k y=0 \quad \text { becomes } \quad\left(m \lambda^{2}+b \lambda+k\right) e^{\lambda t}=0$$

$$m=1$$

$$\begin{aligned}
&\boldsymbol{d} \boldsymbol{y} / \boldsymbol{d} t=\boldsymbol{y}^{\prime} \\
&\boldsymbol{d} \boldsymbol{y}^{\prime} / \boldsymbol{d} t=-\boldsymbol{k} y-\boldsymbol{b} \boldsymbol{y}^{\prime}
\end{aligned} \quad \text { converts to } \quad \frac{d}{d t}\left[\begin{array}{c}
y \\
y^{\prime}
\end{array}\right]=\left[\begin{array}{rr}
\mathbf{0} & \mathbf{1} \\
-\boldsymbol{k} & -\boldsymbol{b}
\end{array}\right]\left[\begin{array}{c}
y \\
y^{\prime}
\end{array}\right]=A \boldsymbol{u} .$$

$$A-\lambda I=\left[\begin{array}{cc}
-\lambda & 1 \\
-k & -b-\lambda
\end{array}\right] \quad \text { has determinant } \quad \lambda^{2}+b \lambda+k=0$$

$$\boldsymbol{x}_{1}=\left[\begin{array}{c}
1 \\
\lambda_{1}
\end{array}\right] \quad \boldsymbol{x}_{2}=\left[\begin{array}{c}
1 \\
\lambda_{2}
\end{array}\right] \quad \boldsymbol{u}(t)=c_{1} e^{\lambda_{1} t}\left[\begin{array}{c}
1 \\
\lambda_{1}
\end{array}\right]+c_{2} e^{\lambda_{2} t}\left[\begin{array}{c}
1 \\
\lambda_{2}
\end{array}\right]$$

## Defference equations

![Screen Shot 2022-07-10 at 10.05.10 PM](https://live.staticflickr.com/65535/52207815305_4f5d16f24f_o.png)

![Screen Shot 2022-07-10 at 10.19.41 PM](https://live.staticflickr.com/65535/52207620489_67eea11c42_o.png)

![Screen Shot 2022-07-10 at 10.23.41 PM](https://live.staticflickr.com/65535/52207359131_b11e7ca0f7_o.png)

real below, imaginary above the parabola

# Matrix exponential

$$e^{x}=1+x+\frac{1}{2} x^{2}+\frac{1}{6} x^{3}+\cdots$$

$$e^{A t}=I+A t+\frac{1}{2}(A t)^{2}+\frac{1}{6}(A t)^{3}+\cdots$$

take derivative w.r.t. $t$: 

$$A+A^{2} t+\frac{1}{2} A^{3} t^{2}+ \cdots=A e^{A t}$$

Its **eigenvalues** are $e^{\boldsymbol{\lambda} t}$

$$e^{A t}x=e^{\lambda t}x$$

$$\left(I+A t+\frac{1}{2}(A t)^{2}+\cdots\right) \boldsymbol{x}=\left(1+\lambda t+\frac{1}{2}(\lambda t)^{2}+\cdots\right) \boldsymbol{x}$$

1. $e^{A t}$ always has the inverse $e^{-A t}$.
2. The eigenvalues of $e^{A t}$ are always $e^{\lambda t}$.
3. When $A$ is antisymmetric, $e^{A t}$ is orthogonal. Inverse $=$ transpose $=e^{-A t}$.

## find $\boldsymbol{u}(t)=e^{A t} \boldsymbol{u}(0)$

$$e^{A t}=X e^{\Lambda t} X^{-1}$$

1. $\boldsymbol{u}(0)=c_1 \boldsymbol{x}_1+\cdots+c_n \boldsymbol{x}_n=X \boldsymbol{c}$. Here we need $n$ independent eigenvectors.

2. Multiply each $\boldsymbol{x}_i$ by its growth factor $e^{\lambda_{i} t}$ to follow it forward in time.

3. The best form of $e^{A t} \boldsymbol{u}(0)$ is 

   $$\boldsymbol{u}(t)=\boldsymbol{c}_\boldsymbol{1} e^{\lambda_\boldsymbol{1} t} \boldsymbol{x}_\boldsymbol{1}+\cdots+\boldsymbol{c}_\boldsymbol{n} e^{\lambda_n t} \boldsymbol{x}_\boldsymbol{n}$$

 It is a short form solution compatible with the original one ($u(t)=c_{1} e^{\lambda_{1} t} x_{1}+\cdots+c_{n} e^{\lambda_{n} t} x_{n}$),

$$e^{A t} u(0)=X e^{\Lambda t} X^{-1} u(0)=\left[\begin{array}{lll}
\boldsymbol{x}_{1} & \cdots & \boldsymbol{x}_{n} 
\end{array}\right]\left[\begin{array}{ccc}
e^{\lambda_{1} t} & & \\
& \ddots & \\
& & e^{\lambda_{n} t}
\end{array}\right]\left[\begin{array}{c}
c_{1} \\
\vdots \\
c_{n}
\end{array}\right]$$

we can use it to find the solution when the eigenvectors are not enough to produce the solution in original form:

(where the $t e^{t}$ comes from)

### if diagonalization is not possible

there are repeated eigenvalues and less eigenvectors. we cannot express solution as:

$$u(t)=c_{1} e^{\lambda_{1} t} x_{1}+\cdots+c_{n} e^{\lambda_{n} t} x_{n}$$

use series to express the solution:

$$e^{A t}=e^{I t} e^{(A-I) t}=e^{t}[I+(A-I) t]$$

$$\left[\begin{array}{l}
y \\
y^{\prime}
\end{array}\right]=e^{t}\left[I+\left[\begin{array}{ll}
-1 & 1 \\
-1 & 1
\end{array}\right] t\right]\left[\begin{array}{r}
y(0) \\
y^{\prime}(0)
\end{array}\right] \quad y(t)=e^{t} y(0)-t e^{t} y(0)+t e^{t} y^{\prime}(0)$$

# Symmetric Matrices

1. A symmetric matrix has only real eigenvalues.

2. The eigenvectors can be chosen orthonormal.

#### $S=Q \Lambda Q^{\mathrm{T}}$

#### Spectral Theorem / Principal axis theorem

$$\text{symmetric matrix=(orthonormal eigenvectors)(eigenvalue)(orthonormal eigenvectors)}^\mathrm{T}$$

Every symmetric matrix has the factoriztion $S=Q \Lambda Q^{\mathrm{T}}$ with real eigenvalues in $\Lambda$ and orthonormal eigenvectors in the columns of $Q$:

Symmetric diagonalization $S=Q \Lambda Q^{-1}=Q \Lambda Q^{\mathrm{T}} \quad$ with $\quad Q^{-1}=Q^{\mathrm{T}}$

#### Orthogonal Eigenvectors

Eigenvectors of a real symmetric matrix (when they correspond to different $\lambda$ 's) are always perpendicular.

---

Every 2 by 2 symmetric matrix is **(rotation)(stretch)(rotate back)**

$$S=Q \Lambda Q^{\mathrm{T}}=\left[\begin{array}{ll}
\boldsymbol{q}_{1} & \boldsymbol{q}_{2}
\end{array}\right]\left[\begin{array}{ll}
\lambda_{1} & \\
& \lambda_{2}
\end{array}\right]\left[\begin{array}{l}
\boldsymbol{q}_{1}^{\mathrm{T}} \\
\boldsymbol{q}_{2}^{\mathrm{T}}
\end{array}\right]$$

$$S=Q \Lambda Q^{\mathrm{T}}=\lambda_{1} q_{1} \boldsymbol{q}_{1}^{\mathrm{T}}+\cdots+\lambda_{n} \boldsymbol{q}_{n} \boldsymbol{q}_{n}^{\mathrm{T}}$$

#### Complex Eigenvalues of Real Matrices

![Screen Shot 2022-07-11 at 11.02.04 AM](https://live.staticflickr.com/65535/52208559943_fc2734ff1c_o.png)

#### Eigenvalues versus Pivots

$$\text { product of pivots }=\text { determinant }=\text { product of eigenvalues. }$$

For symmetric matrices, **(same signs)** the number of positive **eigenvalues** of $S=S^{\mathrm{T}}$ equals the number of positive **pivots**.

All Symmetric Matrices are Diagonalizable.

#### Schur's Theorem (triangularization)

Every square $A$ factors into $Q T Q^{-1}$ where $T$ is upper triangular and $\bar{Q}^{\mathrm{T}}=Q^{-1}$. If $A$ has real eigenvalues then $Q$ and $T$ can be chosen real: $Q^{\mathrm{T}} Q=I$.

If $A=S$ then $T=\Lambda$.

# Positive Definite Matrices

the **symmetric** matrices that have **positive eigenvalues**

The eigenvalues of $S$ are positive if and only if the pivots are positive

#### Energy-based Definition

$$\text{energy}=\boldsymbol{x}^{\mathrm{T}} S \boldsymbol{x}=\lambda \boldsymbol{x}^{\mathrm{T}} \boldsymbol{x}=\lambda \|\boldsymbol{x}\|^{2}>0$$

for all nonzero vectors $x$

If $S$ and $T$ are symmetric positive definite, so is $S + T$.

If the columns of $A$ are independent, then $S=A^{\mathrm{T}} A$ is positive definite.

##### Properties

When a symmetric matrix $S$ has one of these five properties, it has them all:
1. All $n$ pivots of $S$ are positive.
2. All n upper left determinants are positive.
3. All n eigenvalues of $S$ are positive.
4. $\boldsymbol{x}^{\mathrm{T}} S \boldsymbol{x}$ is positive except at $\boldsymbol{x}=\mathbf{0}$. This is the energy-based definition.
5. $S$ equals $A^{\mathrm{T}} A$ for a matrix $A$ with independent columns.

#### split up $\boldsymbol{x}^{\mathrm{T}} S \boldsymbol{x}$

![Screen Shot 2022-07-11 at 12.52.10 PM](https://live.staticflickr.com/65535/52207679547_04975b2992_o.png)

#### Positive Semidefinite Matrices

dependent columns

#### The Ellipse $\boldsymbol{x}^{\mathrm{T}} S \boldsymbol{x}=a x^{2}+2 b x y+c y^{2}=1$

![Screen Shot 2022-07-11 at 1.02.19 PM](https://live.staticflickr.com/65535/52208725083_985dae2191_o.png)

1. The tilted ellipse is associated with $S$. Its equation is $\boldsymbol{x}^{\mathrm{T}} S \boldsymbol{x}=1$.
2. The lined-up ellipse is associated with $\Lambda$. Its equation is $\boldsymbol{X}^{\mathrm{T}} \Lambda \boldsymbol{X}=1$.
3. The rotation matrix that lines up the ellipse is the eigenvector matrix $Q$.

$\boldsymbol{S}=Q \Lambda Q^{\mathrm{T}}$ is positive definite when all $\lambda_{i}>0$. The graph of $\boldsymbol{x}^{\mathrm{T}} S \boldsymbol{x}=1$ is an ellipse: 

#### Ellipse

$$\left[\begin{array}{ll}x & y\end{array}\right] Q \Lambda Q^{\mathrm{T}}\left[\begin{array}{l}x \\ y\end{array}\right]=\left[\begin{array}{ll}X & Y\end{array}\right] \Lambda\left[\begin{array}{l}X \\ Y\end{array}\right]=\boldsymbol{\lambda}_{1} \boldsymbol{X}^{2}+\boldsymbol{\lambda}_{2} Y^{2}=\mathbf{1}$$

The axes point along eigenvectors of $S$. The half-lengths are $1 / \sqrt{\lambda_{1}}$ and $1 / \sqrt{\lambda_{2}}$.

#### Hyperbola

one eigen value is negative

#### Ellipsoid

$S$ is $n$ by $n$.

#### Minimum

![Screen Shot 2022-07-11 at 1.20.51 PM](https://live.staticflickr.com/65535/52208999609_c100c7fffc_o.png)
