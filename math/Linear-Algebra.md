---
layout: base
title: Linear Algebra
nav_order: 3
has_children: true
permalink: /docs/Linear-Algebra
---

Reference: Strang, Gilbert, et al. *Introduction to linear algebra*. Vol. 3. Wellesley, MA: Wellesley-Cambridge Press, 1993.

![linearalgebra5_Front](https://live.staticflickr.com/65535/52213295678_dfd4ecdd08_o.jpg)

---

# The matrix alphabet

$$\begin{array}{llcl}
\boldsymbol{A} & \text { Any Matrix } & \boldsymbol{P} & \text { Permutation Matrix } \\
\boldsymbol{B} & \text { Basis Matrix } & \boldsymbol{P} & \text { Projection Matrix } \\
\boldsymbol{C} & \text { Cofactor Matrix } & \boldsymbol{Q} & \text { Orthogonal Matrix } \\
\boldsymbol{D} & \text { Diagonal Matrix } & \boldsymbol{R} & \text { Upper Triangular Matrix } \\
\boldsymbol{E} & \text { Elimination Matrix } & \boldsymbol{R} & \text { Reduced Echelon Matrix } \\
\boldsymbol{F} & \text { Fourier Matrix } & \boldsymbol{S} & \text { Symmetric Matrix } \\
\boldsymbol{H} & \text { Hadamard Matrix } & \boldsymbol{T} & \text { Linear Transformation } \\
\boldsymbol{I} & \text { Identity Matrix } & \boldsymbol{U} & \text { Upper Triangular Matrix } \\
\boldsymbol{J} & \text { Jordan Matrix } & \boldsymbol{U} & \text { Left Singular Vectors } \\
\boldsymbol{K} & \text { Stiffness Matrix } & \boldsymbol{V} & \text { Right Singular Vectors } \\
\boldsymbol{L} & \text { Lower Triangular Matrix } & \boldsymbol{X} & \text { Eigenvector Matrix } \\
\boldsymbol{M} & \text { Markov Matrix } & \boldsymbol{\Lambda} & \text { Eigenvalue Matrix } \\
\boldsymbol{N} & \text { Nullspace Matrix } & \boldsymbol{\Sigma} & \text { Singular Value Matrix }
\end{array}$$


#### Minor $\mathbf{M}_{ij}$
Operational Definition:

$$\mathbf{M}_{2,3}=\operatorname{det}\left[\begin{array}{ccc}
    1 & 4 & \square \\
    \square & \square & \square \\
    -1 & 9 & \square
    \end{array}\right]=\operatorname{det}\left[\begin{array}{cc}
    1 & 4 \\
    -1 & 9
    \end{array}\right]=9-(-4)=13$$

#### Adjugate Matrix $\operatorname{adj}(\mathbf{A})$ or $\mathbf{A}^*$

$$\mathbf{C}_{ij}=(-1)^{ij}\mathbf{M}_{ij}$$

$$\operatorname{adj}(\mathbf{A})=\mathbf{C^T}$$

#### Determinant $\operatorname{det}(\mathbf{A})$ or$|\mathbf{A}|$
#### Inverse Matrix $\mathbf{A}^{-1}$

$$\mathbf{A}^{-1}=\frac{\operatorname{adj}(\mathbf{A})}{\operatorname{det}(\mathbf{A})}$$

##### $2\times2$ Matrix

$$\left[\begin{array}{cc}
    a & b \\ 
    c & d
    \end{array}\right]^{-1}=
\left[\begin{array}{cc}
    d & -b \\ 
    -c & a
    \end{array}\right]$$

## Calculation Rules

#### Product

##### Hadamard Product / Schur Product / Element-wise Product / Entrywise Product

$$(A\circ B)_{ij}=(A\odot B)_{ij}=(A)_{ij}(B)_{ij}$$

##### Dot Product / Scalar Product

$$A\cdot B$$

##### Matrix Multiplication

$$AB$$

##### Cross Product

$$A\times B$$

# Vector Calculus

#### Scalar Fields

#### Vector Fields

#### Vectors and Pseudovectors

#### Vector Addition: 2 vectors $\longrightarrow$ 1 vector

$$\textbf{v}_1+\textbf{v}_2$$

#### Scalar Multiplication: 1 scalar $+$ 1 vector $\longrightarrow$ 1 vector

$$\alpha\textbf{v}_2$$

#### Dot Product: 2 vector $\longrightarrow$ 1 scalar

$$\textbf{v}_1\cdot\textbf{v}_2$$

#### Cross Product: 2 vectors in $\mathbb{R}^3\longrightarrow$ 1 (pseudo)vector

$$\textbf{v}_1\times\textbf{v}_2$$

## Operators

#### Gradient: scalar fields $\longrightarrow$ vector fields

$$\mathrm{grad}(f)=\nabla f$$

#### Divergence: vector fields $\longrightarrow$ scalar fields

$$\mathrm{div}(\textbf{F})=\nabla\cdot\textbf{F}$$

#### Curl: vector fields $\longrightarrow$ vector fields

$$\mathrm{curl}(\textbf{F})=\nabla\times\textbf{F}$$

#### Laplacian: vector fields $\longrightarrow$ vector fields

$$\Delta f=\nabla^2f=\nabla\cdot\nabla f$$

#### Vector Laplacian: vector fields $\longrightarrow$ vector fields

$$\Delta \textbf{F}=\nabla^2\textbf{F}=\nabla(\nabla\cdot\textbf{F})-\nabla\times(\nabla\times\textbf{F})$$

## Integral Theorems

#### Gradient Theorem

$$\int_{L\subset\mathbb{R}^n}\nabla\phi\cdot\mathrm{d}r=\phi(q)-\phi(p) \ for \ L=L[p\rightarrow q]$$

#### Divergence Theorem

$$\int...\int_{V\subset\mathbb{R}^n}(\nabla\cdot\textbf{F})\mathrm{d}V=\oint...\oint_{\partial V}F\cdot\mathrm{d}S$$

#### Curl (Kelvin-Stokes) Theorem

$$\iint_{\Sigma\subset\mathbb{R}^3}(\nabla\times\textbf{F})\mathrm{d}\Sigma=\oint_{\partial\Sigma}\textbf{F}\mathrm{d}r$$

#### Green's Theorem (Divergence/Curl Theorem in 2D)

$$\iint_{A\subset\mathbb{R}^2}-\left(\frac{\partial L}{\partial y}\right)\mathrm{d}A=\oint_{\partial A}(L\mathrm{d}x+M\mathrm{d}y)$$

#### Jacobian Matrix and Determinant

$$\textbf{f}:\mathbb{R}^n\rightarrow\mathbb{R}^m$$

$$\textbf{J}_{ij}=\frac{\partial f_i}{\partial x_j}$$

$$\textbf{J}=\nabla ^\mathrm{T}\textbf{f}$$

$$\mathbf{J}=\left[\begin{array}{ccc}
\frac{\partial \mathbf{f}}{\partial x_{1}} & \cdots & \frac{\partial \mathbf{f}}{\partial x_{n}}
\end{array}\right]=\left[\begin{array}{c}
\nabla^{\mathrm{T}} f_{1} \\
\vdots \\
\nabla^{\mathrm{T}} f_{m}
\end{array}\right]=\left[\begin{array}{ccc}
\frac{\partial f_{1}}{\partial x_{1}} & \cdots & \frac{\partial f_{1}}{\partial x_{n}} \\
\vdots & \ddots & \vdots \\
\frac{\partial f_{m}}{\partial x_{1}} & \cdots & \frac{\partial f_{m}}{\partial x_{n}}
\end{array}\right]_{m \times n}$$

If $m=n$, Jacobian matrix has its determinant $\|\textbf{J}\|$.

Its value represents the transformation ratio of $\textbf{f}$.

#### Hessian Matrix

$$f:\mathbb{R}^n\rightarrow\mathbb{R}$$

$$(\textbf{H}_{f})_{ij}=\frac{\partial^2 f}{\partial x_i\partial x_j}$$

$$\mathbf{H}_{f}=\left[\begin{array}{cccc}
\frac{\partial^{2} f}{\partial x_{1}^{2}} & \frac{\partial^{2} f}{\partial x_{1} \partial x_{2}} & \cdots & \frac{\partial^{2} f}{\partial x_{1} \partial x_{n}} \\
\frac{\partial^{2} f}{\partial x_{2} \partial x_{1}} & \frac{\partial^{2} f}{\partial x_{2}^{2}} & \cdots & \frac{\partial^{2} f}{\partial x_{2} \partial x_{n}} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial^{2} f}{\partial x_{n} \partial x_{1}} & \frac{\partial^{2} f}{\partial x_{n} \partial x_{2}} & \cdots & \frac{\partial^{2} f}{\partial x_{n}^{2}}
\end{array}\right]_{n \times n}$$

$$\textbf{H}(f(\textbf{x}))=\textbf{J}(\nabla f(\textbf{x}))=\nabla ^\mathrm{T}(\nabla f(\textbf{x}))$$
