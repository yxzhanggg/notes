---
layout: base
title: SVD
parent: Linear Algebra
nav_order: 5
---

The singular value theorem for $A$ is the eigenvalue theorem for $A^{\mathrm{T}} A$ and $A A^{\mathrm{T}}$.

$$\text { Use the eigenvectors } u \text { of } A A^{\mathrm{T}} \text { and the eigenvectors } v \text { of } A^{\mathrm{T}} A$$

#### left singular vectors $u$'s

the principal components

$$\text { unit eigenvectors of } A A^{\mathrm{T}}$$

#### Right singular vectors $v$'s

the combination if principal components

$$\text { unit eigenvectors of } A^{\mathrm{T}} A$$

$$A A^{\mathrm{T}} \boldsymbol{u}_{i}=\sigma_{i}^{2} \boldsymbol{u}_{i} \quad A^{\mathrm{T}} A \boldsymbol{v}_{i}=\sigma_{i}^{2} \boldsymbol{v}_{i} \quad A \boldsymbol{v}_{i}=\sigma_{i} \boldsymbol{u}_{i}$$

$\sigma_{i}$is the length of $A \boldsymbol{v}_{i}$

A is diagonalized:

$$A =\sum_i\boldsymbol{u}_{i}\sigma_{i} \boldsymbol{v}_{i}^\mathrm{T}$$

![image-20220714171111844](https://s2.loli.net/2022/07/14/GOsTvMWzKrgeExQ.png)

![Screen Shot 2022-07-12 at 10.35.14 AM](https://live.staticflickr.com/65535/52211227194_4448d8f338_o.png)

$$\sigma_{1} \geq \sigma_{2} \geq \ldots \sigma_{r}>0$$

include all the $v$'s and $u$'s:

![Screen Shot 2022-07-12 at 11.05.47 AM](https://live.staticflickr.com/65535/52211481700_1576e7f06e_o.png)

---

$$A=U \boldsymbol{\Sigma} V^{\mathbf{T}}=u_{1} \sigma_{1} v_{1}^{\mathbf{T}}+\cdots+u_{r} \sigma_{r} v_{r}^{\mathbf{T}}$$

---

If $A$ is positive semidefinite (or definite) symmetric matrix,

$$A=X \Lambda X^{-1}=Q \Lambda Q^{\mathrm{T}}=U \Sigma V^{\mathrm{T}}$$

$$\begin{array}{ll}
\text { Symmetric } \boldsymbol{S} & S=Q \Lambda Q^{\mathrm{T}}=\lambda_{1} \boldsymbol{q}_{1} \boldsymbol{q}_{1}^{\mathrm{T}}+\lambda_{2} \boldsymbol{q}_{2} \boldsymbol{q}_{2}^{\mathrm{T}}+\cdots+\lambda_{r} \boldsymbol{q}_{r} \boldsymbol{q}_{r}^{\mathrm{T}} \\
\text { Any matrix } \boldsymbol{A} & A=U \Sigma V^{\mathrm{T}}=\sigma_{1} \boldsymbol{u}_{1} \boldsymbol{v}_{1}^{\mathrm{T}}+\sigma_{2} \boldsymbol{u}_{2} \boldsymbol{v}_{2}^{\mathrm{T}}+\cdots+\sigma_{r} \boldsymbol{u}_{r} \boldsymbol{v}_{r}^{\mathrm{T}}
\end{array}$$

#### normal matrix

$$A^{\mathrm{T}} A=A A^{\mathrm{T}}$$

the eigenvectors of $A$ are orthogonal and the eigenvalues of $A$ are totally stable.

but the singular values of any matrix are stable.

#### Rayleigh quotient

$$r(\boldsymbol{x})=\boldsymbol{x}^{\mathrm{T}} S \boldsymbol{x} / \boldsymbol{x}^{\mathrm{T}} \boldsymbol{x}$$

The derivatives of $r(x)=\frac{x^{\mathrm{T}} S x}{x^{\mathrm{T}} x}$ are zero when $S \boldsymbol{x}=r(\boldsymbol{x}) \boldsymbol{x}$

# Principal Component Analysis (singular value = variance)

#### sample covariance matrix 

The covariance matrix predicts the spread of future measurements around their mean.

Find the average (the mean) $\mu_{1}, \mu_{2}, \ldots, \mu_{m}$ of each row. Subtract each mean $\mu_{i}$ from row $i$ to center the data.

$$S=\frac{A A^{\mathrm{T}}}{n-1}$$

$A$ shows the distance $a_{i j}-\mu_{i}$ from each measurement to the row average $\mu_{i}$. 

$$\left(A A^{\mathrm{T}}\right)_{11}, \left(A A^{\mathrm{T}}\right)_{22}$$

show the sum of squared distances (sample variances $s_1^2, s_2^2$ ). 

$\left(A A^{\mathrm{T}}\right)_{12}$ shows the sample covariance:

$$s_{12}=(\operatorname{row} 1 \text { of } A) \cdot(\operatorname{row} 2 \text { of } A)$$

one degree of freedom was used by the mean so $n-1$

Since the rows of $A$ have $n$ entries, the numbers in $A A^{\mathrm{T}}$ have size growing like $n$ and the division by $n-1$ keeps them steady.

- The total variance in the data is the sum of all eigenvalues and of sample variances $s^{2}$ : Total variance $T=\sigma_1^2+\cdots+\sigma_m^2=s_1^2+\cdots+s_m^2=$ trace (diagonal sum).
- The first eigenvector $\boldsymbol{u}_1$ of $S$ points in the most significant direction of the data. That direction accounts for (or explains) a fraction $\sigma_1^2 / T$ of the total variance.
- The next eigenvector $\boldsymbol{u}_2$ (orthogonal to $\boldsymbol{u}_1$ ) accounts for a smaller fraction $\sigma_2^2 / T$.
- Stop when those fractions are small. You have the $R$ directions that explain most of the data. The $n$ data points are very near an $R$-dimensional subspace with basis $\boldsymbol{u}_1$ to $\boldsymbol{u}_R$. These $\boldsymbol{u}$ 's are the principal components in $m$-dimensional space.
- $R$ is the "effective rank" of $A$. The true rank $r$ is probably $m$ or $n$ : full rank matrix.

#### Perpendicular Least Squares / orthogonal regression

$$\text { Right triangles } \sum_{j=1}^{n}\left\|\boldsymbol{a}_{j}\right\|^{2}=\sum_{j=1}^{n}\left|\boldsymbol{a}_{j}^{\mathrm{T}} \boldsymbol{u}_{1}\right|^{2}+\sum_{j=1}^{n}\left|\boldsymbol{a}_{j}^{\mathrm{T}} \boldsymbol{u}_{2}\right|^{2}$$

RHS is fixed, choosing maximum $u_1$ term will result in minimum $u_2$ term.

#### Sample Correlation Matrix (nomalized)

A diagonal matrix $D$ rescales $A$. Each row of $D A$ has length $\sqrt{n-1}$.
The sample correlation matrix $C=D A A^{\mathrm{T}} D /(n-1)$ has $1$ 's on its diagonal.

# Model Order Reduction

A reduced model tries to identify important states of the system.

#### Dynamic

"Dynamic" means that the solution $u ( t )$ evolves as time goes forward.

#### snapshot

A snapshot is a column vector that describes the state of the system

It can be an approximation to a typical true state $\boldsymbol{u}\left(t^{*}\right)$

From $n$ snapshots, build a matrix $A$ whose columns span a useful range of states

#### Proper Orthogonal Decomposition

The first $R$ left singular vectors $\boldsymbol{u}_1$ to $\boldsymbol{u}_R$ of snapshot $A$ are a basis for POD.

Variance $\approx$ Energy

$\sigma_{1}^{2}+\cdots+\sigma_{R}^{2}$ is $99 \%$ or $99.9 \%$ of $\sigma_{1}^{2}+\cdots+\sigma_{n}^{2}$

# The Geometry of the SVD

$$(\text { orthogonal }) \times(\text { diagonal }) \times(\text { orthogonal })$$

$$(\text { rotation }) \times(\text { stretching }) \times(\text { rotation })$$

$$A \boldsymbol{x}=U \Sigma V^{\mathrm{T}} \boldsymbol{x}$$

![Screen Shot 2022-07-12 at 4.05.46 PM](https://live.staticflickr.com/65535/52210447702_746752d194_o.png)

#### The Norm of a Matrix

largest singular value $\sigma_{1}$

$$\text { The norm }\|A\| \text { is the largest ratio } \frac{\|A x\|}{\|x\|} \quad\|A\|=\max _{x \neq 0} \frac{\|A x\|}{\|x\|}=\sigma_{1}$$

#### Eckart-Young-Mirsky Theorem

$$\text { The closest rank } \boldsymbol{k} \text { matrix to } \boldsymbol{A} \text { is } \boldsymbol{A}_{\boldsymbol{k}}=\sigma_{1} \boldsymbol{u}_{1} \boldsymbol{v}_{1}^{\mathrm{T}}+\cdots+\sigma_{k} \boldsymbol{u}_{k} \boldsymbol{v}_{k}^{\mathrm{T}}$$

$$\|A-B\| \geq\left\|A-A_{k}\right\|=\sigma_{k+1} \text { for all matrices } B \text { of rank } k \text {. }$$

#### Polar Decomposition $A=QS$

Every real square matrix can be factored into $A=Q S$, where $Q$ is orthogonal and $S$ is symmetric positive semidefinite. If $A$ is invertible, $S$ is positive definite.

$$A=U \Sigma V^{\mathrm{T}}=\left(U V^{\mathrm{T}}\right)\left(V \Sigma V^{\mathrm{T}}\right)=(Q)(S)$$

$$A=U \Sigma V^{\mathrm{T}}=\left(U \Sigma U^{\mathrm{T}}\right)\left(U V^{\mathrm{T}}\right)=(K)(Q)$$

The product of orthogonal matrices is orthogonal.

In mechanics, the polar decomposition separates the rotation (in $Q$ ) from the stretching (in $S$ ). The eigenvalues of $S$ give the stretching factors. The eigenvectors of $S$ give the stretching directions (the principal axes of the ellipse). The orthogonal matrix $Q$ includes both rotations $U$ and $V^{\mathrm{T}}$.

Here is a fact about rotations. $Q=U V^{\mathrm{T}}$ is the nearest orthogonal matrix to $A$. This $Q$ makes the norm $\|Q-A\|$ as small as possible. That corresponds to the fact that $e^{i \theta}$ is the nearest number on the unit circle to $r e^{i \theta}$.

$$\text { The nearest singular matrix } A_{0} \text { to } A \text { comes by changing the smallest } \sigma_{\min } \text { to zero. }$$

So $\sigma_{\min }$ is measuring the distance from $A$ to singularity.

#### Pseudoinverse $A^{+}$

![Screen Shot 2022-07-12 at 9.24.24 PM](https://live.staticflickr.com/65535/52212104513_44d3acbfd5_o.png)

$$A^{+} \boldsymbol{u}_{i}=\frac{1}{\sigma_{i}} \boldsymbol{v}_{i} \quad \text { for } i \leq r \quad \text { and } \quad A^{+} \boldsymbol{u}_{i}=\mathbf{0} \text { for } i>r$$

![Screen Shot 2022-07-12 at 10.00.08 PM](https://live.staticflickr.com/65535/52211148447_4e54e2b572_o.png)

![Screen Shot 2022-07-12 at 10.02.04 PM](https://live.staticflickr.com/65535/52212431914_ed5e2d33bf_o.png)

$$\boldsymbol{x}^{+}=\boldsymbol{A}^{+} \boldsymbol{b} \text { is the shortest solution to } A^{\mathrm{T}} A \widehat{\boldsymbol{x}}=A^{\mathrm{T}} \boldsymbol{b} \text { and } A \widehat{\boldsymbol{x}}=\boldsymbol{p}$$

The least square approximation decomposite the vectors, psudoinverse faked a matrix that can operate like a real inverse matrix.

Principally, the inverse will bring the left null space to a certain space, but the psudoinverse brings it to zero.
