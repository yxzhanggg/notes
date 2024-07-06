---
layout: default
title: Spaces
parent: Linear Algebra
nav_order: 2
---
# Transfroming things between subspaces!

---

# The Reduced Row Echelon Form $R=\mathrm{rref}(A)$

#### The triangular echelon matrix $U$

$U$ tells **which** columns are combinations of earlier columns (pivots are missing).

---

Then $R$ tells us **what** those **combinations** are.

The pivot columns of $R$ contain $I$.

Easy to find **special solutions**.

Every ''free column" is a combination of earlier pivot columns.

R reveals a "basis" for three fundamental subspaces:

- The column space of $A$ - choose the pivot columns of $A$ as a basis.
- The row space of $A$ - choose the nonzero rows of $R$ as a basis.
- The nullspace of $A$ - choose the special solutions to $Rx = 0$ (and $Ax = 0$).

![Screen Shot 2022-07-02 at 10.39.28 PM](https://live.staticflickr.com/65535/52189330349_9f5554da7d_o.png)

Suppose $Ax = 0$ has more unknowns than equations ($n > m$, more columns than rows). There must be at least one free column. Then $Ax = 0$ has nonzero solutions.

"Dimension" of nullspace is the number of free variables.

#### $A=CR$

![Screen Shot 2022-07-04 at 1.27.14 PM](https://live.staticflickr.com/65535/52193066549_fa03f2aa52_o.png)

$$EA=R\rightarrow A=E^{-1}R\rightarrow A=CR$$

$$\left[\begin{array}{ccc}
\operatorname{col basis} 1 & \text { col basis } 2 & \text { col basis 3} \\
\cdot & \cdot & \cdot \\
\cdot & \cdot & \cdot
\end{array}\right]\left[\begin{array}{ccc}
\text { row basis } 1 & \cdots \cdot \\
\text { row basis } 2 & \cdots \cdot \\
\text { row basis } 3 & \cdots \cdot
\end{array}\right]\\=(\operatorname{col basis} 1)(\text { row basis 1) }+(\operatorname{col basis} 2)(\text { row basis 2) }+(\operatorname{col basis} 3)(\text { row basis 3) }$$

#### Space

Definition: The space $\mathbf{R}^{n}$ consists of all column vectors $v$ with $n$ components. (for complex numbers  $\mathbf{C}^{n}$)

The eight conditions are required:

|        Axiom         |                           Meaning                            |
| :------------------: | :----------------------------------------------------------: |
|   Commutative Low    | $\boldsymbol{v}+\boldsymbol{w}=\boldsymbol{w}+\boldsymbol{v}$ |
|   Distributive Law   | $c(\boldsymbol{v}+\boldsymbol{w})=c \boldsymbol{v}+c \boldsymbol{w}$ |
| Unique "zero vector" |              $0+\boldsymbol{v}=\boldsymbol{v}$               |
|         ...          |                             ...                              |

$\mathbf{M}$ The vector space of all real 2 by 2 matrices.

$\mathbf{F}$ The vector space of all real functions $f(x)$.

$\mathbf{Z}$ The vector space that consists only of a zero vector.

#### Subspace

Definition: A **subspace** of a vector space is a set of vectors (including 0) that satisfies two requirements: If v and ware vectors in the subspace and c is any scalar, then

1. $\boldsymbol{v}+\boldsymbol{w}$ is in the subspace
2. $c \boldsymbol{v}$ is in the subspace.

- All linear combinations stay in the subspace.
- Every subspace contains the zero vector.
- Lines through the origin are also subspaces.

##### Column space of $A$ - the 'b's 

Definition: The column space consists of all linear combinations of the columns. ($\mathbf{R}^{m}$)

The combinations are all possible vectors $A \boldsymbol{x}$. They fill the column space $\boldsymbol{C}(A)$.

- The system $A x=b$ is solvable if and only if $b$ is in the column space of $A$.

![Screen Shot 2022-07-02 at 4.07.30 PM](https://live.staticflickr.com/65535/52188376726_43a5a69386_o.png)

Any set of column vectors: $\mathbf{S}=$ set of vectors in $\mathbf{V}$ (probably not a subspace)

Subspace: $\mathbf{S S}=$ all combinations of vectors in $\mathbf{S}$ (definitely a subspace)

$$\mathbf{S S}=\text { all } c_{1} \boldsymbol{v}_{1}+\cdots+c_{N} \boldsymbol{v}_{N}=\text { the subspace of } \mathbf{V} \text { "spanned" by } \mathbf{S}$$

$\mathbf{S S}$ is the smallest subspace containing $\mathbf{S}$.

##### Nullspace of $A$ - the 'x's 

The nullspace $N(A)$ consists of all solutions to $A x=0$. These vectors $x$ are in $\mathbf{R}^{n}$.

The nullspace of $A$ consists of all combinations of the special solutions to $A x=0$.

The **free components** correspond to columns with no pivots. The special choice (one or zero) is only for the free variables in the special solutions.

##### Row space

$$\boldsymbol{v}^{\mathrm{T}} \boldsymbol{x}=\mathbf{0}$$

All vectors $\boldsymbol{x}$ in the nullspace must be orthogonal to $\boldsymbol{v}$ in the row space.

##### Left nullspace

$$R^{\mathrm{T}} \boldsymbol{y}=\mathbf{0}$$

$$\boldsymbol{y}^{\mathrm{T}} R=\mathbf{0}^{\mathrm{T}}$$

The $y$'s in the left nullspace combine the rows to give the zero row.

##### Matrix spaces

![Screen Shot 2022-07-03 at 10.49.41 PM](https://live.staticflickr.com/65535/52191460306_828573005f_o.png)

##### Function spaces

#### Rank

The true size of linear space $A$ is given by its rank.

Definition: 

- (computational) The rank of $A$ is the number of pivots. This number is $r$.

- $A$ and $U$ and $R$ also have $r$ independent columns (the pivot columns) and independent rows.
- The rank $r$ is the "dimension" of the column space. It is also the dimension of the row space. ($n - r$ is the dimension of the nullspace.)

##### Rank 1

Every rank one matrix is one column times one row：

$$\boldsymbol{A}=\text { column times row }=u v^{\mathrm{T}}$$

##### Rank 2 = rank 1 + rank 1 (A=CR)

$$\begin{array}{lll}
\text { Matrix } \boldsymbol{A} \\
\text { Rank two }
\end{array} \quad A=\left[\begin{array}{lll}
\boldsymbol{u}_{1} & \boldsymbol{u}_{2} & \boldsymbol{u}_{3}
\end{array}\right]\left[\begin{array}{c}
\boldsymbol{v}_{1}^{\mathrm{T}} \\
\boldsymbol{v}_{2}^{\mathrm{T}} \\
\text { zero row }
\end{array}\right]=\boldsymbol{u}_{1} \boldsymbol{v}_{1}^{\mathrm{T}}+\boldsymbol{u}_{2} \boldsymbol{v}_{2}^{\mathrm{T}}=(\operatorname{rank} 1)+(\operatorname{rank} 1)$$

##### Every rank $r$ matrix is a sum of $r$ rank one matrices

Pivot columns of  $A$ times nonzero rows of $R$. The row $\left[\begin{array}{lll}
0 & 0 & 0
\end{array}\right]$ simply disappeared.

$$\boldsymbol{u}_{1}, \ldots, \boldsymbol{u}_{n}$$

are bases for the column space, 

$$\boldsymbol{v}_{1}^{\mathrm{T}}, \ldots, \boldsymbol{v}_{n}^{\mathrm{T}}$$

are bases for the row space.

##### Rank Theorem

The number of independent columns =the number of independent rows.

#### Particular solution $Ax_p=b$

Set free variables to be zero.

$$R x_{p}=\left[\begin{array}{cccc}
\mathbf{1} & 3 & \mathbf{0} & 2 \\
\mathbf{0} & 0 & \mathbf{1} & 4 \\
0 & 0 & 0 & 0
\end{array}\right]\left[\begin{array}{l}
\mathbf{1} \\
0 \\
\mathbf{6} \\
0
\end{array}\right]=\left[\begin{array}{l}
\mathbf{1} \\
\mathbf{6} \\
0
\end{array}\right] \quad \begin{aligned}
&\text { Pivot variables } \mathbf{1 , 6} \\
&\text { Solution } \boldsymbol{x}_{\boldsymbol{p}}=(\mathbf{1}, \mathbf{0}, \mathbf{6}, \mathbf{0}) .
\end{aligned}$$

$$\left[\begin{array}{ll}
A & \boldsymbol{b}
\end{array}\right]\rightarrow \left[\begin{array}{ll}
R & \boldsymbol{d}
\end{array}\right]$$

For invertible matrix $A$,

$$\left[\begin{array}{ll}
A & \boldsymbol{b}
\end{array}\right] \rightarrow \left[\begin{array}{ll}
I & A^{-1} \boldsymbol{b}
\end{array}\right]$$

![Screen Shot 2022-07-03 at 1.36.11 PM](https://live.staticflickr.com/65535/52190331351_d2052559aa_o.png)

![Screen Shot 2022-07-03 at 5.32.51 PM](https://live.staticflickr.com/65535/52189761217_ba324cd2db_o.png)

#### Full column rank ($m>=n$) - overdetermined - one solution / no solution

Independent columns

$$\text { Full column rank } R=\left[\begin{array}{l}
I \\
0
\end{array}\right]=\left[\begin{array}{l}
n \text { by } n \text { identity matrix } \\
m-n \text { rows of zeros }
\end{array}\right]$$

Every matrix A with full column rank ($r=n$) has all these properties:

1. All columns of $A$ are pivot columns.

2. There are no free variables or special solutions.

3. The nullspace $N(A)$ contains only the zero vector $x=0$.

4. If $Ax=b$ has a solution (it might not) then it has only one solution.

#### Full row rank ($m<=n$) - underdetermined - one solution / infinitely many solutions

independent rows

Every matrix $A$ with full row rank ($r=m$) has all these properties:

1. All rows have pivots, and $R$ has no zero rows.
2. $Ax = b$ has a solution for every right side $b$.
3. The column space is the whole space $\mathbf{R}^{m}$ .
4. There are $n - r=n - m$ special solutions in the nullspace of $A$.

---

The number of solutions depends on if the linear system has free variables.

![Screen Shot 2022-07-03 at 5.57.07 PM](https://live.staticflickr.com/65535/52190838683_cce5258203_o.png)

![Screen Shot 2022-07-03 at 5.56.29 PM](https://live.staticflickr.com/65535/52191076679_00fbd3cdc9_o.png)

---

#### Dimension

The dimension is measured by counting independent columns - **rank** $r$.

$$\mathrm{Dimension \ of \ subspace = Rank \ of \ matrix}$$

The dimension of a space is the number of vectors in every basis.

#### Basis

Independent vectors that "span the space".

Every vector in the space is a unique combination of the basis yectors.

The columns of every invertible $n$ by $n$ matrix give a basis for $\mathbf{R}^{n}$.

The pivot columns of invertible $n$ by $n$ matrix $A$ are a basis for its column space.

1. The $r$ pivot rows of $R$ are a basis for the row spaces of $R$ and $A$ (same space).
2. The $r$ pivot columns of $A(!)$ are a basis for its column space $\boldsymbol{C}(A)$.
3. The $n-r$ special solutions are a basis for the nullspaces of $A$ and $R$ (same space).
4. If $E A=R$, the last $m-r$ rows of $E$ are a basis for the left nullspace of $A$.

#### Spanning a space

A set of vectors spans a space if their linear combinations fill the space.

#### Linear Independence

Definition: 

1. The columns of $A$ are linearly independent when the only solution to $Ax = 0$ is $x = 0$. No other combination $Ax$ of the columns gives the zero vector.

2. The sequence of vectors $v_1 , \ldots , v_n$ is linearly independent if the only combination that gives the zero vector is $0v_1 + 0v_2 + \ldots + 0v_n$ .

   $$x_{1} \boldsymbol{v}_{1}+x_{2} \boldsymbol{v}_{2}+\cdots+x_{n} \boldsymbol{v}_{n}=\mathbf{0} \quad \text { only happens when all } x \text { 's are zero. }$$

Full column rank: The columns of $A$ are independent exactly when the rank is $r = n$. There are $n$ pivots and no free variables. Only $x = 0$ is in the nullspace.

---

# Fundamental Theorem of Linear Algebra. Pt.1

The column space and row space both have dimension $r$. 

The nullspaces have dimensions $n-r$ and $m-r$.

Four Fundamental Subspaces
1. The row space is $C(A^{\mathrm{T}})$, a subspace of $\mathbf{R}^{n}$.
2. The column space is $C(A)$, a subspace of $\mathbf{R}^{m}$.
3. The nullspace is $N(A)$, a subspace of $\mathbf{R}^{n}$.
4. The left nullspace is $N(A^{\mathrm{T}})$, a subspace of $\mathbf{R}^{m}$.

![Screen Shot 2022-07-03 at 10.26.38 PM](https://live.staticflickr.com/65535/52190401527_5eaf6b94eb_o.png)

---

#### Incidence matrix

![Screen Shot 2022-07-04 at 10.24.13 AM](https://live.staticflickr.com/65535/52192798324_0b5b79525e_o.png)

##### Kirchhoff's Voltage Law

$$A \boldsymbol{x}=\boldsymbol{b}$$

##### Kirchhoff's Current Law

$$A^{\mathrm{T}} \boldsymbol{y}=\mathbf{0}$$
