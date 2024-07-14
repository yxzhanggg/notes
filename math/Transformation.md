---
layout: base
title: Transformation
parent: Linear Algebra
nav_order: 6
---

#### linear transformation

$$T(c \boldsymbol{v}+d \boldsymbol{w}) \quad \text { must equal } \quad c T(\boldsymbol{v})+d T(\boldsymbol{w})$$

Shift is not linear:

$$\boldsymbol{v}+\boldsymbol{w}+\boldsymbol{u}_{0} \quad \text { is not } T(\boldsymbol{v})+T(\boldsymbol{w})=\left(\boldsymbol{v}+\boldsymbol{u}_{0}\right)+\left(\boldsymbol{w}+\boldsymbol{u}_{0}\right)$$

Equally spaced points go to equally spaced points.

#### affine

linear-plus-shift transformation $T(v)=A v+u_{0}$.

Straight lines stay straight although $T$ is not linear.

affine provides the ability to move things.

#### Linearity

$$\boldsymbol{u} =c_{1} \boldsymbol{v}_{1}+c_{2} \boldsymbol{v}_{2}+\cdots+c_{n} \boldsymbol{v}_{n}$$

must transform to:

$$T(\boldsymbol{u}) =c_{1} T\left(\boldsymbol{v}_{1}\right)+c_{2} T\left(\boldsymbol{v}_{2}\right)+\cdots+c_{n} T\left(\boldsymbol{v}_{n}\right)$$

Suppose you know $T(v)$ for all vectors $v_{1}, \ldots, v_{n}$ in a basis Then you know $T(u)$ for every vector $u$ in the space.

#### Calculus

$$T=\text { derivative}$$

$$T^{+}=\text {integral}$$

#### Fundamental Theorem of Calculus

Integration is the (pseudo)inverse of differentiation.

The derivative of a constant function is zero. That zero is on the diagonal of $A^{+} A$. Calculus wouldn't be calculus without that 1 -dimensional nullspace of $T=d / d x$.

#### range

column space

Set of all outputs $T(v)$.

#### kernel

nullspace

Set of all inputs for which $T(\boldsymbol{v})=0$.

#### Trigonometry (the double angle rule)

$$A^2=\left[\begin{array}{rr}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{array}\right]\left[\begin{array}{rr}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{array}\right]=\left[\begin{array}{cc}
\cos ^{2} \theta-\sin ^{2} \theta & -2 \sin \theta \cos \theta \\
2 \sin \theta \cos \theta & \cos ^{2} \theta-\sin ^{2} \theta
\end{array}\right]=\left[\begin{array}{rr}
\cos 2 \theta & -\sin 2 \theta \\
\sin 2 \theta & \cos 2 \theta
\end{array}\right]$$

#### Rotate back

$$A B=\left[\begin{array}{rr}
\cos \theta & \sin \theta \\
-\sin \theta & \cos \theta
\end{array}\right]\left[\begin{array}{rr}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{array}\right]=\left[\begin{array}{cc}
\cos ^{2} \theta+\sin ^{2} \theta & 0 \\
0 & \cos ^{2} \theta+\sin ^{2} \theta
\end{array}\right]=I$$

#### isometric

$C=Q_{1}^{-1} A Q_{2}$ is isometric to $A$ if $Q_{1}$ and $Q_{2}$ are orthogonal.

---

$A_{\text {new }}=B^{-1} A B$ in the new basis of $b$ 's is **similar** to $A$ in the standard basis:

![Screen Shot 2022-07-13 at 4.34.38 PM](https://live.staticflickr.com/65535/52214232370_7625ed365c_o.png)

The best input-output bases are eigenvectors and/or singular vectors of $A$.

$$B^{-1} A B=\Lambda= \text{eigenvalues} $$

$$B_{\text {out }}^{-1} A B_{\text {in }}=\Sigma=$ \text{singular values}$$

---

# Good Basis

#### $$X^{-1} A X=\text { eigenvalues in } \Lambda$$

#### $$U^{-1} A V=\text { diagonal } \Sigma$$

#### Jordan form

independent eigenvectors $s$, constructed $n -s$ additional " generalized" eigenvectors

$$B^{-1} A B=\text { Jordan form } J (B_{\text {in }}=B_{\text {out }}=\text { generalized eigenvectors of } A)$$

![Screen Shot 2022-07-13 at 5.11.11 PM](https://live.staticflickr.com/65535/52213838558_433a634d80_o.png)

the generalized eigenvector is tied to the previous eigenvector.

![image-20220714121459482](https://s2.loli.net/2022/07/14/SMqkZ7dbYnomAPJ.png)

Like Laplace transform is a generalization of Fourier transform, Jordan form is a generalization of finding eigenbases.

The rank of $J$ (and $A$) will be the total number of 1's. The maximum rank is $n/2$.

#### $$B_{\text {in }}=B_{\text {out }}=\text { Forier matrix } F$$

Discrete Fourier Transform $Fx$

![image-20220714150905250](https://s2.loli.net/2022/07/14/Jr2moDCKOH1wVg9.png)

![image-20220714143703521](https://s2.loli.net/2022/07/14/RlaxTEJA5BNu6Zd.png)

![image-20220714150851321](https://s2.loli.net/2022/07/14/JOK2sfSbhIt8qw9.png)

![image-20220714155939186](https://s2.loli.net/2022/07/14/tDRo2Mljnk9bdiQ.png)

#### basis for function space

![image-20220714162229250](https://s2.loli.net/2022/07/14/Lm7EuC1vFSAJef2.png)

![image-20220714164605894](https://s2.loli.net/2022/07/14/GBbWvNnzPOX6mAR.png)

#### Orthogonality between even and odd functions

![image-20220714162423956](https://s2.loli.net/2022/07/14/gy3xcB1wYmARnrI.png)

#### Fourier basis

$$1, \sin x, \cos x, \sin 2x, \cos 2x, ...$$

linear algebra in function space, projecting vector $b$ onto the line through $a$.

$$a_i=\boldsymbol{b}^\mathrm{T}\boldsymbol{a}/\boldsymbol{a}^\mathrm{T}\boldsymbol{a}$$

#### Legendre basis

$$1,x, x^2-\frac{1}{3}, x^3-\frac{3}{5}x,\ldots $$

is the result of Grant-Schmidt: orthogonalize the power $1, x, x^2$

#### Chebyshev basis

$$1,x,2x^2-1,4x^3-3x,\ldots$$

set $x=\cos \theta$

![image-20220714163933245](https://s2.loli.net/2022/07/14/yO5uqnQtxlhpfDZ.png)

$$n^\text{th} \, \text{degree Chebyshev polynomial}\quad\mathbf{T}_n(x)\stackrel{\mathcal{F}}\longrightarrow \mathbf{T}_n(\cos \theta) =\cos n\theta$$
