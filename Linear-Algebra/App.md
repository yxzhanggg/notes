---
layout: math
title: Linear Algebra
---

#### Incidence matrix

![image-20220716120827293](https://s2.loli.net/2022/07/16/XSIg4cJajCvMDLx.png)

#### complete

every pair of nodes is connected by an edge

maximum edges $\frac{1}{2}n(n-1)$

#### Tree

no closed loops

minimum edges $n-1$

- Elimination reduces every graph to a tree.

#### Kirchhoff's Voltage Law:

he components of $Ax = b$ add to zero around every loop.

#### Kirchhoff's Current Law:

$$A^\mathbf{T} y = 0$$
Flow in equals flow out at each node.

the matrix in this balance equation is the transpose of the incidence matrix A.

![image-20220716214219336](https://s2.loli.net/2022/07/17/DxbjlTFzBkLRoa4.png)

#### Euler's formula

$$\text{(number of nodes) - (number of edges) + (number of small loops)} = 1$$

$$( n) - ( m) + ( m - n + 1) = 1$$

#### Laplacian matrix

![image-20220716222115406](https://s2.loli.net/2022/07/17/Hqg9YTCZkU2XtoF.png)

![image-20220716222124750](https://s2.loli.net/2022/07/17/Sq5NvRioJHwca6C.png)

#### stiffness matrix

![image-20220717092045628](https://s2.loli.net/2022/07/17/rHRtLsv6d1bEgpB.png)

#### Markov Matrix

1. Every entry of $A$ is positive: $a_{ij} > 0$.
2. Every column of $A$ adds to 1.

![image-20220717095104838](https://s2.loli.net/2022/07/17/lWeE2zbipSy1q7Z.png)

#### Perron-Frobenius Theorem

![image-20220717095211722](https://s2.loli.net/2022/07/17/sjFb2c36A5tl7rI.png)

#### Linear Programming

Linear programming is linear algebra plus two new ideas: inequalities and minimization.

he cost is $c_1 x_1 + · · · + c_nx_n$. The winning vector $x^*$ is the nonnegative solution of $Ax = b$ that has smallest cost.

![image-20220717105845230](https://s2.loli.net/2022/07/17/t8sfSVCNjU1PbDz.png)

Solution is the **corners**!

#### Duality

$$\text{max=min}$$

The number of independent rows equals the number of independent columns.

![image-20220717114705270](https://s2.loli.net/2022/07/17/CemvlTHRNMgbnEd.png)

#### Simplex method (moves along the edges of the feasible set)

The simplex method goes from one corner to a neighboring corner of lower cost. (move along edge)

A **corner** is a vector $x\geq0$ that satisfies the $m$ equations $Ax = b$ with at most $m$ positive components. The other $n - m$ components are zero.

The simplex method must decide which component "enters" by becoming positive, and which component "leaves" by becoming zero. The **entering variable** is the one that gives the **most negative reduced cost** $r$.

Solve the $Ax=b$ by iterately knock off the free column from $A$, then solve the $Bx=b$. (a column enters and an old column leaves)

#### Interior Point Methods (move inside the feasible set)

![image-20220717144203291](https://s2.loli.net/2022/07/17/1LCRc5raz7tAGhw.png)

![image-20220717145121620](https://s2.loli.net/2022/07/17/OH1D7WZuRyKvGNC.png)

![image-20220717145143397](https://s2.loli.net/2022/07/17/hNW5AjuPvdcQnmb.png)

![image-20220717145218909](https://s2.loli.net/2022/07/17/ad2sT4x3mPUtEcl.png)

#### Hilbert spaces

![image-20220717145635275](https://s2.loli.net/2022/07/17/OsM3k9QYZNp5CBl.png)

![image-20220717153147736](https://s2.loli.net/2022/07/17/UpkvHmdhK8tNFT6.png)

#### Homogeneous coordinate

![image-20220717174342178](https://s2.loli.net/2022/07/17/JyVmWl5sP2voT6S.png)

#### Field $F$

a set of scalars that can be added and multiplied and inverted (except 0 can't be inverted).
