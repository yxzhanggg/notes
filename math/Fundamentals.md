---
layout: base
title: What is matrix (Ax = b)
parent: Linear Algebra
nav_order: 1
---
# Basics

#### vector

A vector in $n$ dimension space has $n$ components $v_1, v_2,\ldots,v_n$.

$$\boldsymbol{v}+\boldsymbol{w}=\left(v_{1}+w_{1}, v_{2}+w_{2}\right)$$

$$c \boldsymbol{v}=\left(c v_{1}, c v_{2}\right)$$

#### Length of a vector

$$\text { length }=\|\boldsymbol{v}\|=\sqrt{\boldsymbol{v} \cdot \boldsymbol{v}}=\left(v_{1}^{2}+v_{2}^{2}+\cdots+v_{n}^{2}\right)^{1 / 2}$$

#### Linear combination

$$c \boldsymbol{u}+d \boldsymbol{v}+e \boldsymbol{w}$$

#### Cosine formula

$$\cos \theta=\frac{\boldsymbol{v} \cdot \boldsymbol{w}}{\|\boldsymbol{v}\|\|\boldsymbol{w}\|}$$

#### Schwarz inequality

$$\|\boldsymbol{v} \cdot \boldsymbol{w}\| \leq{\|\boldsymbol{v}\|\|\boldsymbol{w}\|}$$

#### Triangle Inequality

$$\|\boldsymbol{v}+\boldsymbol{w}\| \leq\|\boldsymbol{v}\|+\|\boldsymbol{w}\|$$

# Different viewpoints

#### Row picture

$$\begin{aligned}
x-2 y &=1 \\
3 x+2 y &=11
\end{aligned}$$

The **row picture** shows two lines meeting at a single point (the solution).

![Screen Shot 2022-06-13 at 22.00.48](https://live.staticflickr.com/65535/52144395134_e9909f4531_o.png)

#### Column picture

$$\left[\begin{array}{rr}
1 & -2 \\
3 & 2
\end{array}\right]\left[\begin{array}{l}
3 \\
1
\end{array}\right]=\left[\begin{array}{r}
1 \\
11
\end{array}\right]$$

The **column picture** combines the column vectors on the left side to produce the vector b on the right side.

![Screen Shot 2022-06-13 at 22.03.47](https://live.staticflickr.com/65535/52144183903_039eee5beb_o.png)

#### Hyperplane

the plane $n>3$

# Matrix multiplication

#### Direct method

The entry in row $i$ and column $j$ of $A B$ is $($ row $i$ of $A) \cdot($ column $j$ of $B)$.

![Screen Shot 2022-06-14 at 18.27.10](https://live.staticflickr.com/65535/52146378173_1a6be3cdab_o.png)

#### Column picture

Matrix $A$ times every column of $B$

$$A\left[\boldsymbol{b}_{1} \cdots \boldsymbol{b}_{p}\right]=\left[A \boldsymbol{b}_{1} \cdots A \boldsymbol{b}_{p}\right]$$

#### Row picture

Every row of $A$ times matrix $B$

$$[\text { row } i \text { of } A]B=[\text { row } i \text { of } A B]$$

$AB= (m \times n)(n \times p) = (m \times p)$, $mp$ dot products with $n$ steps each.

#### Columns by rows

Multiply columns $1$ to $n$ of $A$ times rows $1$ to $n$ of $B$. Add those matrices.

$$\left[\begin{array}{ccc}
\operatorname{col} 1 & \text { col } 2 & \text { col 3} \\
\cdot & \cdot & \cdot \\
\cdot & \cdot & \cdot
\end{array}\right]\left[\begin{array}{ccc}
\text { row 1 } & \cdots \cdot \\
\text { row 2 } & \cdots \cdot \\
\text { row } 3 & \cdots \cdot
\end{array}\right]=(\operatorname{col} 1)(\text { row 1) }+(\operatorname{col} 2)(\text { row 2) }+(\operatorname{col} 3)(\text { row 3) }$$

#### Schur complement

$$S=D-C A^{-1} B$$

$$\left[\begin{array}{c|c}
I & \mathbf{0} \\
\hline-C A^{-1} & I
\end{array}\right]\left[\begin{array}{c|c}
A & B \\
\hline C & D
\end{array}\right]=\left[\begin{array}{c|c}
A & B \\
\hline \mathbf{0} & \boldsymbol{D}-\boldsymbol{C A}^{-\mathbf{1}} \boldsymbol{B}
\end{array}\right]$$

# Inversion

#### Inverse matrix

The matrix $A$ is invertible if there exists a matrix $A^{-1}$ that "inverts" $A$:

$$A^{-1} A=I \quad \text { and } \quad A A^{-1}=I$$

- Two-sided inversion: square matrix
- One-sided inversion: rectangular matrix

#### Inversibility

The inverse exists if and only if **elimination** produces $n$ pivots.

##### Properties

1. $(A B C)^{-1}=C^{-1} B^{-1} A^{-1}$

2. $K$ is symmetric across its main diagonal. Then $K^{-1}$ is also symmetric.

3. $K$ is tridiagonal (only three nonzero diagonals = band). But $K^{-1}$ is a dense matrix with no zeros. 

4. An invertible matrix cannot have a zero determinant.

5. If $A$ is invertible and upper triangular, so is $A^{-1}$. Start with $A A^{-1}=I$.

6. Diagonally dominant matrices are invertible: 

    $$\left|\boldsymbol{a}_{i i}\right|>\sum_{j \neq i}\left|\boldsymbol{a}_{i j}\right|$$

For **elimination matrix** $E$

![Screen Shot 2022-06-25 at 22.59.14](https://live.staticflickr.com/65535/52171580522_a0f5588f13_o.png)

#### Gauss-Jordan method

The Gauss-Jordan method computes $A^{-1}$ by solving all $n$ equations together.

$$A A^{-1}=A\left[\begin{array}{lll}
x_{1} & x_{2} & x_{3}
\end{array}\right]=\left[\begin{array}{lll}
e_{1} & e_{2} & e_{3}
\end{array}\right]=I$$

$$A^{-1}\left[\begin{array}{ll}
A & I
\end{array}\right]=E\left[\begin{array}{ll}
A & I
\end{array}\right]=\left[\begin{array}{ll}
I & A^{-1}
\end{array}\right]$$

The matrix $E$ keeps a record.

#### From Cofactor matrix

$$\left(A^{-1}\right)_{i j}=\frac{C_{j i}}{\operatorname{det} A} \quad \text { and } \quad A^{-1}=\frac{C^{\mathrm{T}}}{\operatorname{det} A}$$

# Transpose and Permutation

#### Transpose

$$\text{row}\leftrightarrow\text{column} \quad \left(A^{\mathbf{T}}\right)_{i j}=A_{j i}$$

	Mathematical definition: $A^{\mathrm{T}}$ is the matrix that makes these two inner products equal for every $x$ and $y$:

$$(A x)^{\mathrm{T}} y=x^{\mathrm{T}}\left(A^{\mathrm{T}} y\right) \quad \text { Inner product of } A x \text { with } y=\text { Inner product of } x \text { with } A^{\mathrm{T}} y$$

##### Properties

1. SUM: The transpose of $A+B$ is $A^{\mathrm{T}}+B^{\mathrm{T}}$.

2. PRODUCT: $(A B C)^{T}=C^{T}B^{T}A^{T}$.

    $A \boldsymbol{x}$ combines the columns of $A$ while $\boldsymbol{x}^{\mathrm{T}} A^{\mathrm{T}}$ combines the rows of $A^{\mathrm{T}}$ .

3. INVERSE: The transpose of $A^{-1}$ is $\left(A^{-1}\right)^{\mathrm{T}}=\left(A^{\mathrm{T}}\right)^{-1}$.

4. $A^{\mathrm{T}}$ is invertible exactly when $A$ is invertible.

5. $A^\mathrm{T} A$ is invertible if and only if $A$ has linearly independent columns.

6. $A^{\mathrm{T}} A$ is symmetric.

7. Transformation perspective: transpose matrix is an n-dimensional scissors.

#### Inner products / Dot product ($^\mathbf{T}$ is inside)

$$x^{\mathrm{T}} y \quad(1 \times n)(n \times 1)$$

#### Outer products / Rank one product ($^\mathbf{T}$ is inside)

$$x y^{\mathrm{T}} \quad(n \times 1)(1 \times n)$$

#### Symmetric Matrix

Definition: A symmetric matrix has $S^{\mathrm{T}}=S .$ This means that $s_{j i}=s_{i j}$.

##### Properties

The inverse of a symmetric matrix is also symmetric.  $\left(S^{-1}\right)^{\mathrm{T}}=\left(S^{\mathrm{T}}\right)^{-1}=S^{-1}$

#### $S=A^{\mathrm{T}} A$

The transpose of $A^{\mathrm{T}} A$ is $A^{\mathrm{T}}\left(A^{\mathrm{T}}\right)^{\mathrm{T}}$ which is $A^{\mathrm{T}} A$ again.

#### Permutation Matrix

Definition: A permutation matrix $P$ has the rows of the identity $I$ in any order.

$$P P^{\mathrm{T}}=I \leftrightarrow P^{\mathrm{T}}=P^{-1}$$

#### $PA=LU \quad / \quad A=LPU$

When there is a row exchange, the sign of determinant is reversed.

# Determinant

$$\begin{aligned}
&\text {The determinant of an } n \text { by } n \text { matrix can be found in three ways: }\\
&\begin{array}{ll}
1 \text { Multiply the } n \text { pivots (times } 1 \text { or }-1) & \text { This is the pivot formula. } \\
2 \text { Add up } n \text { ! terms (times } 1 \text { or }-1) & \text { This is the "big' formula. } \\
\mathbf{3} \text { Combine } n \text { smaller determinants (times } 1 \text { or }-1 \text { ) } & \text { This is the cofactor formula. }
\end{array}
\end{aligned}$$

## Properties

$$\operatorname{det} A \text { and }|A|$$

1. The determinant of the $n$ by $n$ identity matrix is $1 .$

2. The determinant changes sign when two rows are exchanged (sign reversal):

3. The determinant is a linear function of each row separately (all other rows stay fixed).

   ![Screen Shot 2022-07-08 at 3.19.48 PM](https://live.staticflickr.com/65535/52201208012_3ee0721520_o.png)

4. 4 If two rows of $A$ are equal, then $\operatorname{det} A=0$.
5. Subtracting a multiple of one row from another row leaves $\operatorname{det} A$ unchanged.
6. A matrix with a row of zeros has $\operatorname{det} A=0$.
7. If $A$ is triangular then $\operatorname{det} A=a_{11} a_{22} \cdots a_{n n}= \text{product of diagonal entries}$. 
8. If $A$ is singular then $\operatorname{det} A=0$. If $A$ is invertible then $\operatorname{det} A \neq 0$.
9. The determinant of $A B$ is $\operatorname{det} A$ times $\operatorname{det} B:\|A B\|=\|A\|\|B\|$.
10. $$A^{\mathrm{T}}=\operatorname{det} A$$

## Calculate the determinant

#### The Pivot Formula

$$\operatorname{det} A=(\operatorname{det} L)(\operatorname{det} U)=(1)\left(d_{1} d_{2} \cdots d_{n}\right)$$

Pivots from determinants:

The $k$ th pivot is $\boldsymbol{d}_{\boldsymbol{k}}=\frac{d_{1} d_{2} \cdots d_{k}}{d_{1} d_{2} \cdots d_{k-1}}=\frac{\operatorname{det} A_{k}}{\operatorname{det} A_{k-1}}$.

#### The Big Formula for Determinants

$\operatorname{det} A=$ sum over all $\mathbf{n} !$ column permutations $P=(\alpha, \beta, \ldots, \omega)$
$$
=\sum(\operatorname{det} P) a_{1 \alpha} a_{2 \beta} \cdots a_{n \omega}=\text { BIG FORMULA. }
$$

#### Determinant by Cofactors

The determinant is the dot product of any row $i$ of $A$ with its cofactors using other rows: COFACTOR FORMULA
$$
\operatorname{det} A=a_{i 1} C_{i 1}+a_{i 2} C_{i 2}+\cdots+a_{i n} C_{i n} \text {. }
$$
Each cofactor $C_{i j}$ (order $n-1$, without row $i$ and column $j$ ) includes its correct sign:
Cofactor $C_{i j}=(-1)^{i+j} \operatorname{det} M_{i j}$

# Solving

#### Elimination

To **eliminate** $x$: Subtract a multiple of equation $1$ from equation $2$.

**Pivot** = first nonzero in the row that does the elimination

**Multiplier** = (entry to eliminate) divided by (pivot) = $\ell_{i j}=\frac{\text { entry to eliminate in row } i}{\text { pivot in row } j}$

![Screen Shot 2022-06-13 at 22.19.20](https://live.staticflickr.com/65535/52144200581_0e7dc90af3_o.png)

##### Possible result

1. Permanent failure with no solution.![Screen Shot 2022-06-13 at 22.21.18](https://live.staticflickr.com/65535/52144226868_1a0fc2ddbd_o.png)

2. Failure with infinitely many solutions.

![Screen Shot 2022-07-05 at 3.38.19 PM](https://live.staticflickr.com/65535/52196122935_d6b8d13a41_o.png)

#### $A = LU$

This is elimination without row exchanges. The multipliers $l_{ij}$ are below the diagonal of $L$.

##### Elimination: factorization

$$A=L U=\text { (lower triangular) (upper triangular) }=(E_1^{-1}E_2^{-1}\ldots E_n^{-1})U$$

Elimination on $A$ requires about $\frac{1}{3} n^{3}$ multiplications and $\frac{1}{3} n^{3}$ subtractions.

##### Substitution: solve

$$\text { Forward and backward: Solve } \quad L c=b \quad \text { and then solve } \quad U x=c$$

Each right side $b/c$ needs $n^{2}$ multiplications and $n^{2}$ subtractions.

- Band matrix $B$ (with $w$ nonzero diagonals)

$A$ to $U$: $\frac{1}{3} n^{3}$ reduces to $n w^{2}$

Solve: $n^{2}$ reduces to $2 n w$

#### $A = LDU$

$$\text { Split } U \text { into }\left[\begin{array}{llll}
d_{1} & & & \\
& d_{2} & & \\
& & \ddots & \\
& & & d_{n}
\end{array}\right]\left[\begin{array}{cccc}
1 & u_{12} / d_{1} & u_{13} / d_{1} & \cdot \\
& 1 & u_{23} / d_{2} & \cdot \\
& & \ddots & \vdots \\
& & & 1
\end{array}\right]$$

#### $S=LDL^{\mathrm{T}}$

If $S=S^{\mathrm{T}}$ is factored into $L D U$ with no row exchanges, then $U$ is exactly $L^{\mathrm{T}}$.

#### $A = LPU$

permutation

#### Inversion

$$\text { Multiply } A x=b \text { by } A^{-1} \text {. Then } x=A^{-1} A x=A^{-1} b \text {. }$$

#### Cramer's Rule

explicit formula but huge complexity $(n+1) !$

If $\operatorname{det} A$ is not zero, $A \boldsymbol{x}=\boldsymbol{b}$ is solved by determinants:
$$
x_{1}=\frac{\operatorname{det} B_{1}}{\operatorname{det} A} \quad x_{2}=\frac{\operatorname{det} B_{2}}{\operatorname{det} A} \quad \ldots \quad x_{n}=\frac{\operatorname{det} B_{n}}{\operatorname{det} A}
$$
The matrix $B_{j}$ has the jth column of A replaced by the vector $b$.

Set $B=I$ we can find inverse matrix.

$$[A]\left[\begin{array}{lll}
\boldsymbol{x}_{1} & 0 & 0 \\
\boldsymbol{x}_{2} & 1 & 0 \\
\boldsymbol{x}_{3} & 0 & 1
\end{array}\right]=\left[\begin{array}{lll}
\boldsymbol{b}_{\mathbf{1}} & a_{12} & a_{13} \\
\boldsymbol{b}_{\mathbf{2}} & a_{22} & a_{23} \\
\boldsymbol{b}_{\mathbf{3}} & a_{32} & a_{33}
\end{array}\right]=B_{1}$$

$$(\operatorname{det} A)\left(x_{1}\right)=\operatorname{det} B_{1} \quad \text { or } \quad x_{1}=\frac{\operatorname{det} B_{1}}{\operatorname{det} A} .$$

Take determinants of the three matrices to find $x_1$:

Product rule
$$
(\operatorname{det} A)\left(x_{1}\right)=\operatorname{det} B_{1} \quad \text { or } \quad x_{1}=\frac{\operatorname{det} B_{1}}{\operatorname{det} A}
$$

# Derivative $A$

#### Inner product of functions

1. $$x^{\mathbf{T}} y=(x, y)=\int_{-\infty}^{\infty} x(t) y(t) d t$$

2. $$(A \boldsymbol{x})^{\mathrm{T}} \boldsymbol{y}=\boldsymbol{x}^{\mathrm{T}}\left(A^{\mathrm{T}} \boldsymbol{y}\right)$$
3. $$(A x, y)=\int_{-\infty}^{\infty} \frac{d x}{d t} y(t) d t=\int_{-\infty}^{\infty} x(t)\left(-\frac{d y}{d t}\right) d t=\left(x, A^{\mathrm{T}} y\right)$$

the transpose of the derivative is minus the derivative

$$A=d / d t \quad A^{\mathrm{T}}=-d / d t$$

#### Forward difference matrix to backward difference matrix

$$A=\left[\begin{array}{rrrr}
0 & 1 & 0 & 0 \\
-1 & 0 & 1 & 0 \\
0 & -1 & 0 & 1 \\
0 & 0 & -1 & 0
\end{array}\right] \quad \text { transposes to } \quad A^{\mathrm{T}}=\left[\begin{array}{rrrr}
0 & -1 & 0 & 0 \\
1 & 0 & -1 & 0 \\
0 & 1 & 0 & -1 \\
0 & 0 & 1 & 0
\end{array}\right]=-A$$

- 1st derivative is antisymmetric
- 2st derivative as symmetric

# Cross Product

![Screen Shot 2022-07-08 at 8.28.32 PM](https://live.staticflickr.com/65535/52203010674_da70e69066_o.png)

$$\|\boldsymbol{u} \times \boldsymbol{v}\|=\|\boldsymbol{u}\|\|\boldsymbol{v}\||\sin \theta| \quad \text { and } \quad|\boldsymbol{u} \cdot \boldsymbol{v}|=\|\boldsymbol{u}\|\|\boldsymbol{v}\||\cos \theta|$$

![Screen Shot 2022-07-08 at 8.32.14 PM](https://live.staticflickr.com/65535/52202748236_4471781510_o.png)

![Screen Shot 2022-07-08 at 8.33.19 PM](https://live.staticflickr.com/65535/52202750006_a2f5cbf4bf_o.png)

#### turning force or torque

$$u \times F$$

position of a mass: $\left(u_{1}, u_{2}, u_{3}\right)$

force acting on it: $\left(F_{x}, F_{y}, F_{z}\right)$

#### moment

$\|\boldsymbol{u}\|\|\boldsymbol{F}\| \sin \theta$
