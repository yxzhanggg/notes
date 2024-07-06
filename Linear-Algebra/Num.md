---
layout: base
title: Numerical
parent: Linear Algebra
nav_order: 9
---

#### partial pivoting

Small pivot brings large round off error

Choose the largest number in row $k$ or below. Exchange its row with row $k$.

partial pivoting exchange rows, complete pivoting exchange both rows and columns.

#### Elimination

1. Elimination requires $\frac{1}{2}n^3$ multiply-subtracts, compared to $n^3$ for $A^{-1}$•
2. If $A$ is banded so are $L$ and $U$: by comparison $A^{- 1}$ is full of nonzeros.

#### Band Matrices

![image-20220718095810967](https://s2.loli.net/2022/07/18/hOSbycfuv9R8iPa.png)

A band matrix has $a_{ij} = 0$ when $\|i - j \|> w$.

Elimination

![image-20220718101042191](https://s2.loli.net/2022/07/18/KsfXLBn7SeQPpwo.png)

#### Matrix norm

![image-20220718104927245](https://s2.loli.net/2022/07/18/xsLMAj1WR2u8vOP.png)

#### condition number

$$c=\frac{\|A\|}{|]A^{-1}\|}$$

![image-20220718110318999](https://s2.loli.net/2022/07/18/LP2Eikgt954NMj3.png)

#### iterative problem

$$A=S-T$$

![image-20220718110948796](https://s2.loli.net/2022/07/18/AoDGSdczriCVqpt.png)

![image-20220718111007344](https://s2.loli.net/2022/07/18/GCTFLWle712wSYr.png)

##### residual

$$r_k = b - Ax_k$$

#### preconditioner $S$

diagonal or trianular part of $A$, many zeros.

![image-20220718120006552](https://s2.loli.net/2022/07/18/zKRGyE859oMQ7Da.png)

##### error

$$e_k=x-x_k$$

![image-20220718115425104](https://s2.loli.net/2022/07/18/H5Vmy1SufwrctIe.png)

##### spectral radius

$$B=S^{-1}T$$

![image-20220718121100579](https://s2.loli.net/2022/07/18/EhLVO1xkQe2rYW8.png)

---

![image-20220718124135376](https://s2.loli.net/2022/07/18/TStPc3LBNHn8Quh.png)

#### Jacobi's method

![image-20220718124105813](https://s2.loli.net/2022/07/18/toQYkgBeU4S8ZCc.png)

Keep the diagonal of $A$ on the left side (this is $S$). Move the off-diagonal part of $A$ to the right side (this is $T$).

Jacobi's method works well when the main diagonal of $A$ is large compared to the off-diagonal part. (diagonal dominate)

#### Gauss-Seidel method

![image-20220718124118545](https://s2.loli.net/2022/07/18/tbNBwkjZfqUMVHO.png)

Keeps the whole lower triangular part of $A$ as $S$.

no $u_k$, save storage of data.

Twice faster than Jacobi.

$$\rho_\text{GS}=(\rho_\text{J})^2 \ \text{when A is positive definite tridiagonal}$$

#### successive overrelaxation method (SOR)

Gauss-Seidel, with an adjustable number $\omega$

$$\omega Ax=\omega b$$

$$T=S-\omega A$$

![image-20220718124640205](https://s2.loli.net/2022/07/18/r54hlEFNfmbp2zv.png)
