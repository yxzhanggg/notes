---
layout: base
title: Complex
parent: Linear Algebra
nav_order: 7
---

![image-20220714164858697](https://s2.loli.net/2022/07/14/OjZPiWpFTqAQwd8.png)

![image-20220714194842442](https://s2.loli.net/2022/07/15/Rv5C8w9IgxdGYeM.png)

#### trigonometry (double angle rule)

$$(\cos\theta+i\sin\theta) x (\cos\theta+i\sin\theta) =\cos2 \theta+i^2 \sin2 \theta+2i\sin\theta\cos\theta= \cos 2\theta+i\sin 2\theta$$

#### Euler's Formula

$$\cos \theta = 1 - \frac{1}{2}\theta^2+\ldots$$

$$\sin \theta = \theta - \frac{1}{6}\theta^3$$

$$e^{i\theta}=\cos \theta+ i \sin \theta=1+i\theta+\frac{1}{2}i^2\theta^2+\frac{1}{6}i^3\theta^3+\ldots$$

#### nth roots of 1: $\omega=e^{2\pi i /n}$

$$e^{2\pi i /n}=1\rightarrow z^n=1\rightarrow \omega^n=1$$



![image-20220715112152573](https://s2.loli.net/2022/07/15/1FKrXZ7HmJNbYD2.png)

#### Conjugate transpose $z^\mathbf{H}$ and $A^\mathbf{H}$ ("adjoint" of A)

![image-20220715115920278](https://s2.loli.net/2022/07/15/AXO7Z5ID4EqasRi.png)

$$(Au)^\mathbf{H}v=u^\mathbf{H}(A^\mathbf{H}v)$$

$$(AB)^\mathbf{H}=B^\mathbf{H}A^\mathbf{H}$$

![image-20220715114442762](https://s2.loli.net/2022/07/15/g6hRs1l4WVBAYXr.png)

#### Length

![image-20220715115503354](https://s2.loli.net/2022/07/15/H74PSdCZF3qaw5n.png)

![image-20220715115644249](https://s2.loli.net/2022/07/15/Vn8AOWJvm23aYXS.png)

#### Inner product

![image-20220715120023298](https://s2.loli.net/2022/07/15/JzBTdVb1RW9AjGX.png)

$v^\mathbf{H}u$ is the complex conjungate of $u^\mathbf{H}v$

#### Hermitian Matrices

$$S=S^\mathbf{H}$$

##### Properties

1. energy : f $S = S^\mathbf{H}$ and $z$ is any real or complex column vector, the number $z^\mathbf{H}Sz$ is **real**.

2. Every eigenvalue of a Hermitian matrix is **real**.

3. The eigenvectors of a Hermitian matrix are **orthogonal**  (when they correspond to different eigenvalues). 

   If $Sz = \lambda z$ and $Sy=\beta y$ then $y^\mathbf{H}z = 0$

#### Unitary Matrices

A unitary matrix $Q$ is a (complex) square matrix that has orthonormal columns.

$$|\lambda|=1$$

#### Fast Fourier Transform (a matrix multiplying a vector)

Polynomial:

![image-20220715214628734](https://s2.loli.net/2022/07/16/m9ozkLDjT2RQSKr.png)

Discrete Fourier Transform Matrix:

![image-20220715191654249](https://s2.loli.net/2022/07/16/wTSx4mCb3Z6Dt7K.png)

$$F_n\overline{F}_n=nI$$

$$F_n^{-1}=\overline{F}_n/n$$

![image-20220715222918563](https://s2.loli.net/2022/07/16/DdqEt9FH2ayjRih.png)

![image-20220716114229023](https://s2.loli.net/2022/07/16/Az2CskHWRqva7D5.png)

algebra form to calculate even and odd part:

![image-20220715223235579](https://s2.loli.net/2022/07/16/NoX7gY5ljdFMLbT.png)

![image-20220715223447063](https://s2.loli.net/2022/07/16/QdmWDjti5SrNuZf.png)

$$\omega^2_n=\omega_m$$

$$\omega^{2jk}_n=\omega^{jk}_m$$

![image-20220715223459219](https://s2.loli.net/2022/07/16/DQGop3YPVaEeIFW.png)



![image-20220716113825350](https://s2.loli.net/2022/07/16/uPyB2lY4ITZ7bEg.png)

FFT use the convinience of **even/odd function (symmetry)** and the **symmetry of complex number** based on **polynomial representation** to reduce the complexity of the DFT.

#### Interpolation

![image-20220715193926199](https://s2.loli.net/2022/07/16/op9ZPEvgXV56rbK.png)

If function $f(x)$ has period $2\pi$, change $x$ to $e^{i\theta}$, then find the polynomial $p(z) = c_0 + c_1 z + · · · +C_{n -1}Z^{n -1}$ that match the value $f_0,\ldots,f_{n-1}$.

The Fourier matrix is the Vandermonde matrix for interpolation at those $n$ special points.
