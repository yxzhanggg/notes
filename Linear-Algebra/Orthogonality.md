---
layout: base
title: Orthogonality
parent: Linear Algebra
nav_order: 3
---
#### Orthogonal vectors

$$\boldsymbol{v}^{\mathrm{T}} \boldsymbol{w}=0 \quad \text { and } \quad\|\boldsymbol{v}\|^{2}+\|\boldsymbol{w}\|^{2}=\|\boldsymbol{v}+\boldsymbol{w}\|^{2}$$

#### Orthogonal

Definition: Two subspaces $\boldsymbol{V}$ and $\boldsymbol{W}$ of a vector space are **orthogonal** if every vector $\boldsymbol{v}$ in $V$ is perpendicular to every vector $w$ in $W$.

The unit vectors $q_{1}, \ldots, q_{n}$ are **orthonormal** if

$$\boldsymbol{q}_{i}^{\mathrm{T}} \boldsymbol{q}_{j}=\left\{\begin{array}{lll}
0 & \text { when } i \neq j & \text { (orthogonal vectors) } \\
1 & \text { when } i=j & \left(\text { unit vectors: }\left\|\boldsymbol{q}_{i}\right\|=1\right)
\end{array}\right.$$

A matrix with **unit** orthonormal columns is assigned the special letter $Q$.

$$\boldsymbol{Q}^{\mathrm{T}} \boldsymbol{Q}=\left[\begin{array}{c}-\boldsymbol{q}_{1}^{\mathrm{T}}- \\ -\boldsymbol{q}_{2}^{\mathrm{T}}- \\ -\boldsymbol{q}_{n}^{\mathrm{T}}-\end{array}\right]\left[\begin{array}{ccc}1 & \mid & 1 \\ \boldsymbol{q}_{1} & \boldsymbol{q}_{2} & \boldsymbol{q}_{n} \\ 1 & \mid & 1\end{array}\right]=\left[\begin{array}{cccc}1 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & 1\end{array}\right]=\boldsymbol{I}$$

$$\boldsymbol{v}^{\mathrm{T}} \boldsymbol{w}=0 \text { for all } v \text { in } \boldsymbol{V} \text { and all } \boldsymbol{w} \text { in } W$$

![Screen Shot 2022-07-04 at 4.54.11 PM](https://live.staticflickr.com/65535/52192216197_e291ca7e32_o.png)

![Screen Shot 2022-07-04 at 6.07.08 PM](https://live.staticflickr.com/65535/52192387322_eaa6507e54_o.png)

![Screen Shot 2022-07-04 at 6.18.39 PM](https://live.staticflickr.com/65535/52193422546_ff2f26b778_o.png)

#### Orthogonal Complements

Definition:The orthogonal complement of a subspace $V$ contains every vector that is perpendicular to $V$. This orthogonal subspace is denoted by $V^{\perp}$ (pronounced " $V$ perp").

#### Orthogonal matrix

When $Q$ is square, $Q^{\mathrm{T}} Q=I$ means that $Q^{\mathrm{T}}=Q^{-1}$ : transpose $=$ inverse, the square matrix is called **orthogonal matrix**.

Does multiplication by any orthogonal matrix $Q$ - **lengths** and **angles** don't change.

##### Rotation

$Q$ rotates every vector in the plane by the angle $\theta$ :

$Q=\left[\begin{array}{rr}\cos \theta & -\sin \theta \\ \sin \theta & \cos \theta\end{array}\right] \quad$ and $\quad Q^{\mathrm{T}}=Q^{-1}=\left[\begin{array}{rr}\cos \theta & \sin \theta \\ -\sin \theta & \cos \theta\end{array}\right]$

##### ![Screen Shot 2022-07-08 at 11.59.46 AM](https://live.staticflickr.com/65535/52202440925_0f72d0ca30_o.png)Permutation

Every permutation matrix is an orthogonal matrix.

##### Reflection

If $\boldsymbol{u}$ is any unit vector, set $Q=I-2 u u^{\mathrm{T}}$

$Q^{\mathrm{T}}=I-2 \boldsymbol{u} \boldsymbol{u}^{\mathrm{T}}=Q \quad$ and $\quad Q^{\mathrm{T}} Q=I-4 \boldsymbol{u} \boldsymbol{u}^{\mathrm{T}}+4 \boldsymbol{u} \boldsymbol{u}^{\mathrm{T}} \boldsymbol{u} \boldsymbol{u}^{\mathrm{T}}=I$

![Screen Shot 2022-07-08 at 12.07.19 PM](https://live.staticflickr.com/65535/52202450280_9a9863135b_o.png)

---

# Fundamental Theorem of Linear Algebra. Pt.2

$\boldsymbol{N}(\boldsymbol{A})$ is the orthogonal complement of the row space $\boldsymbol{C}\left(A^{\mathrm{T}}\right)$ (in $\mathbf{R}^{n}$ ).

$\boldsymbol{N}\left(A^{\mathrm{T}}\right)$ is the orthogonal complement of the column space $C(A)\left(\right.$ in $\left.\mathbf{R}^{m}\right) .$

![Screen Shot 2022-07-04 at 9.16.06 PM](https://live.staticflickr.com/65535/52194314620_5b60203db5_o.png)

**After the transformation, the information of nullspace is annihilated. For example after the transformation of first differentiation, the information of position has dissappeared, then second differentiation crash the information of velocity, third accelaration...**

And if we do integration, we need to add the constant C, that integration process is the back-transformation of differentiation, which bring back to the general null space - C position, C velocity, C acceleration...

Remember the particular solution of integration, it is the information brought back by the transformation feature of the system from the "b"; the general solution is the information of nullspace brought back by the annihilation feature of the system from 0!

---

# Projection

#### Projection Matrix $P$

$$\boldsymbol{p}_{1}=P_{1} \boldsymbol{b}=\left[\begin{array}{lll}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 1
\end{array}\right]\left[\begin{array}{l}
x \\
y \\
z
\end{array}\right]=\left[\begin{array}{l}
\mathbf{0} \\
\mathbf{0} \\
\boldsymbol{z}
\end{array}\right] \quad \boldsymbol{p}_{2}=P_{2} \boldsymbol{b}=\left[\begin{array}{lll}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{array}\right]\left[\begin{array}{l}
x \\
y \\
z
\end{array}\right]=\left[\begin{array}{l}
\boldsymbol{x} \\
\boldsymbol{y} \\
\mathbf{0}
\end{array}\right]$$

![Screen Shot 2022-07-06 at 10.51.51 AM](https://live.staticflickr.com/65535/52197523148_22dcc3fa63_o.png)

The vectors give $\boldsymbol{p}_{1}+\boldsymbol{p}_{2}=\boldsymbol{b}$.

The matrices give $P_{1}+P_{2}=I$.

The vector $b$ is being split into the projection $p$ and the error $e = b- p$.

$$P \boldsymbol{b}=\boldsymbol{p}$$

Projection again is still the projection:

$$P^{2}=P$$

$$P^{\mathrm{T}}=P$$

#### Error $e$

The distance from $b$ to the the subspace $C(A)$ is $\|\|e\|\|$

$$e=b-\widehat{x} a$$

#### best/closest choice $\widehat{x}$

$$\begin{gathered}
\boldsymbol{a}_{1}^{\mathrm{T}}(\boldsymbol{b}-A \widehat{\boldsymbol{x}})=0 \\
\vdots \\
\boldsymbol{a}_{n}^{\mathrm{T}}(\boldsymbol{b}-A \widehat{\boldsymbol{x}})=0
\end{gathered} \quad \text { or } \quad\left[\begin{array}{c}
-\boldsymbol{a}_{1}^{\mathrm{T}}- \\
\vdots \\
-\boldsymbol{a}_{n}^{\mathrm{T}}-
\end{array}\right][\boldsymbol{b}-A \widehat{\boldsymbol{x}}]=\left[\begin{array}{l}
0
\end{array}\right]$$

Rewrite above (orthogonality):

$$A^{\mathrm{T}}(\boldsymbol{b}-A \widehat{\boldsymbol{x}})=\mathbf{0}$$

$$A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b}$$



![Screen Shot 2022-07-06 at 11.21.18 AM](https://live.staticflickr.com/65535/52197560778_a0c086264e_o.png)

When $P$ projects onto one subspace, $I - P$ projects onto the perpendicular subspace.

#### 3 steps to find $P$

1. Find the vector $\widehat{x}$

2. Find the projection $p=A \widehat{x}$
3. Find the projection matrix $P$

![Screen Shot 2022-07-06 at 9.16.26 PM](https://live.staticflickr.com/65535/52198611826_429549c22f_o.png)

![Screen Shot 2022-07-06 at 9.19.41 PM](https://live.staticflickr.com/65535/52198893479_c7fa4329f6_o.png)

# Least Squares Approximations

When the length of $\boldsymbol{e}$ is as small as possible, $\widehat{\boldsymbol{x}}$ is $a$ least squares solution.

#### Minimizing the error

1. By geometry

   The smallest possible error is $e = b - p$, perpendicular to the columns space of $A$.

2. By algebra

   $$A \boldsymbol{x}=\boldsymbol{b}=\boldsymbol{p}+\boldsymbol{e} \text { is impossible } \quad A \widehat{\boldsymbol{x}}=\boldsymbol{p} \text { is solvable } \quad \widehat{\boldsymbol{x}} \text { is }\left(A^{\mathrm{T}} A\right)^{-1} A^{\mathrm{T}} \boldsymbol{b} \text {. }$$

   Squared length for any $x$
   
   $$\|A \boldsymbol{x}-\boldsymbol{b}\|^2=\|A \boldsymbol{x}-\boldsymbol{p}\|^2+\|\boldsymbol{e}\|^2$$
   
   $$\text { The least squares solution } \widehat{x} \text { makes } E=\|A x-b\|^{2} \text { as small as possible. }$$
   
   $$\|A \boldsymbol{x}-\boldsymbol{b}\|^{2}=\boldsymbol{x}^{\mathrm{T}} A^{\mathrm{T}} A \boldsymbol{x}-2 \boldsymbol{x}^{\mathrm{T}} A^{\mathrm{T}} \boldsymbol{b}+\boldsymbol{b}^{\mathrm{T}} \boldsymbol{b}$$

3. By calculus

   $$\text { The partial derivatives of }\|A x-b\|^{2} \text { are zeno when } A^{\mathrm{T}} A \hat{x}=A^{\mathrm{T}} b \text {. }
   \\$$

![Screen Shot 2022-07-07 at 10.23.43 PM](https://live.staticflickr.com/65535/52199933392_5ae30a21fd_o.png)

## Fitting a Straight Line

$$\begin{equation}
A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b}
\end{equation}$$

$$\begin{equation}
\text { Dot-product matrix } \boldsymbol{A}^{\mathbf{T}} \boldsymbol{A}=\left[\begin{array}{ccc}
1 & \cdots & 1 \\
t_{1} & \cdots & t_{m}
\end{array}\right]\left[\begin{array}{cc}
1 & t_{1} \\
\vdots & \vdots \\
1 & t_{m}
\end{array}\right]=\left[\begin{array}{cc}
m & \sum t_{i} \\
\sum t_{i} & \sum t_{i}^{2}
\end{array}\right] \text {. }
\end{equation}$$

$$\begin{equation}
A^{\mathrm{T}} \boldsymbol{b}=\left[\begin{array}{ccc}
1 & \cdots & 1 \\
t_{1} & \cdots & t_{m}
\end{array}\right]\left[\begin{array}{c}
b_{1} \\
\vdots \\
b_{m}
\end{array}\right]=\left[\begin{array}{c}
\sum b_{i} \\
\sum t_{i} b_{i}
\end{array}\right]
\end{equation}$$

$$\begin{equation}
A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b} \quad\left[\begin{array}{cc}
m & \sum t_{i} \\
\sum t_{i} & \sum t_{i}^{2}
\end{array}\right]\left[\begin{array}{l}
C \\
D
\end{array}\right]=\left[\begin{array}{c}
\sum b_{i} \\
\sum t_{i} b_{i}
\end{array}\right]
\end{equation}$$

## Fitting by a Parabola

$$\begin{equation}
A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b}
\end{equation}$$

$$\begin{array}{cl}C+D t_{1}+E t_{1}^{2}=b_{1} & \text { is } A \boldsymbol{x}=\boldsymbol{b} \text { with } \\ \vdots & \text { the } m \text { by } 3 \text { matrix } \\ C+D t_{m}+E t_{m}^{2}=b_{m} & \end{array} A=\left[\begin{array}{ccc}1 & t_{1} & t_{1}^{2} \\ \vdots & \vdots & \vdots \\ 1 & t_{m} & t_{m}^{2}\end{array}\right]$$

Least squares: The closest parabola $C+D t+E t^{2}$ chooses $\widehat{\boldsymbol{x}}=(C, D, E)$ to satisfy the three normal equations $A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b}$.

## Q replace A

$$\begin{equation}
A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b}
\end{equation}$$

$$A^{\mathrm{T}} A=Q^{\mathrm{T}} Q=I$$

$$\widehat{\boldsymbol{x}}=Q^{\mathrm{T}} \boldsymbol{b}$$

$$P=A\left(A^{\mathrm{T}} A\right)^{-1} A^{\mathrm{T}}=Q Q^{\mathrm{T}}$$

When $Q$ is square and $m=n$. In this case $\boldsymbol{p}=\boldsymbol{b}$ and $P=Q Q^{\mathrm{T}}=I$.

$$\boldsymbol{p}=Q \widehat{\boldsymbol{x}}=Q Q^{\mathrm{T}} \boldsymbol{b}$$

Every $\boldsymbol{b}=Q Q^{\mathrm{T}} \boldsymbol{b}$ is the sum of its components along the q's:

$$\boldsymbol{b}=\boldsymbol{q}_{1}\left(\boldsymbol{q}_{1}^{\mathrm{T}} \boldsymbol{b}\right)+\boldsymbol{q}_{2}\left(\boldsymbol{q}_{2}^{\mathrm{T}} \boldsymbol{b}\right)+\cdots+\boldsymbol{q}_{n}\left(\boldsymbol{q}_{n}^{\mathrm{T}} \boldsymbol{b}\right)$$

Then $b$ is decomposited into the composition of different orthogonal basis.

Transforms: $Q Q^{\mathrm{T}}=I$ is the foundation of Fourier series and all the great "transforms" of applied mathematics. They break vectors $\boldsymbol{b}$ or functions $f(x)$ into perpendicular pieces. Then by adding the pieces, the inverse transform puts $b$ and $f(x)$ back together.

## Use QR decomposition

$$\begin{equation}
A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b}
\end{equation}$$

$$\boldsymbol{A}^{\mathrm{T}} \boldsymbol{A}=(\boldsymbol{Q} \boldsymbol{R})^{\mathrm{T}} \boldsymbol{Q} R=\boldsymbol{R}^{\mathrm{T}} \boldsymbol{Q}^{\mathrm{T}} \boldsymbol{Q} \boldsymbol{R}=\boldsymbol{R}^{\mathrm{T}} \boldsymbol{R}$$

$$R^{\mathrm{T}} R \widehat{\boldsymbol{x}}=R^{\mathrm{T}} Q^{\mathrm{T}} \boldsymbol{b} \text { or } R \widehat{\boldsymbol{x}}=Q^{\mathrm{T}} \boldsymbol{b} \text { or } \widehat{\boldsymbol{x}}=R^{-1} Q^{\mathrm{T}} \boldsymbol{b}$$

We can solve it by backward substitution. The cost is the $mn^2$ multiplications in the Gram-Schmidt process, which are needed to construct the orthogonal $Q$ and the triangular $R$ with $A = QR$.

# The Gram-Schmidt Process

One and only one idea: Subtract from every new vector its projections in the directions already set.

Producing unit orthogonal vectors from existing vectors.

1. choosing $A=a$

2. Start with $b$ and subtract its projection along $A$

$\boldsymbol{B}=\boldsymbol{b}-\frac{\boldsymbol{A}^{\mathrm{T}} \boldsymbol{b}}{\boldsymbol{A}^{\mathrm{T}} \boldsymbol{A}} \boldsymbol{A}$

3. same process with $c, d, e,\ldots$

$$\boldsymbol{C}=\boldsymbol{c}-\frac{\boldsymbol{A}^{\mathrm{T}} \boldsymbol{c}}{\boldsymbol{A}^{\mathrm{T}} \boldsymbol{A}} \boldsymbol{A}-\frac{\boldsymbol{B}^{\mathrm{T}} \boldsymbol{c}}{\boldsymbol{B}^{\mathrm{T}} \boldsymbol{B}} \boldsymbol{B}$$

Final step. divide the orthogonal vectors by their lengths.

#### $A=QR$

Gram-Schmidt in a nutshell

$$A=Q R=(\text { orthogonal } Q)(\text { triangular } R)$$

$$\left[\begin{array}{lll}a & b & c\end{array}\right]=\left[\begin{array}{lll} & & \\ \boldsymbol{q}_{1} & \boldsymbol{q}_{2} & \boldsymbol{q}_{3}\\  & & \end{array}\right]\left[\begin{array}{lll}\boldsymbol{q}_{1}^{\mathrm{T}} \boldsymbol{a} & \boldsymbol{q}_{1}^{\mathrm{T}} \boldsymbol{b} & \boldsymbol{q}_{1}^{\mathrm{T}} \boldsymbol{c} \\ & \boldsymbol{q}_{2}^{\mathrm{T}} \boldsymbol{b} & \boldsymbol{q}_{2}^{\mathrm{T}} \boldsymbol{c} \\ & & \boldsymbol{q}_{3}^{\mathrm{T}} \boldsymbol{c}\end{array}\right] \quad \text{or} \quad \boldsymbol{A}=\boldsymbol{Q} \boldsymbol{R}$$

Any $m$ by $n$ matrix $A$ with independent columns can be factored into $A = QR$.

## Gram-Schmidt



From independent vectors $a_{1}, \ldots, a_{n}$, Gram-Schmidt constructs orthonormal vectors $q_{1}, \ldots, q_{n}$. 

The matrices with these columns satisfy $A=Q R$. Then $R=Q^{\mathrm{T}} A$ is upper triangular because later $\boldsymbol{q}$ 's are orthogonal to earlier $\boldsymbol{a}$ 's.
