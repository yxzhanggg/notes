---
layout: math
---
# Discrete-time signal

A discrete-time signal is an indexed sequence of complex numbers $x(n)$.
- The notation $x(n)$ is not only used to represent the value at index $n$, but also to represent the whole sequence of values at all indices.
- lollipop plot.

Special functions

| Name                | Expression                                                                                        |
| ------------------- | ------------------------------------------------------------------------------------------------- |
| unit sample         | $\delta(n)=\left\{\begin{array}{ll}1 & ; & n=0 \\0 & ; & \text { otherwise }\end{array}\right.$   |
| unit step           | $u(n)=\left\{\begin{array}{lll}1 & ; & n \geq 0 \\0 & ;  & \text { otherwise }\end{array}\right.$ |
| complex exponential | $e^{j n \omega_0}=\cos \left(n \omega_0\right)+j \sin\left(n \omega_0\right)$                     |

# Discrete-time System

A linear shift-invariant (LSI) system is uniquely characterized by its unit sample response $h(n)$; the input $x(n)$ and output $y(n)$ are related by the convolution sum:

$$
y(n)=\sum_{k=-\infty}^{\infty} x(k) h(n-k)=x(n) * h(n)
$$

Properties of an LSI system:

| Name          | Expression                                                          |
| ------------- | ------------------------------------------------------------------- |
| causality     | $h(n)=0$ for $n<0$                                                  |
| stability     | $\sum_{n=-\infty}^{\infty}\|h(n)\|<\infty$                          |
| invertibility | given $x_1(n) \neq x_2(n)$ it is required that $y_1(n) \neq y_2(n)$ |

Special class of LSI given by linear constant coefficient difference equation:

$$
y(n)=\sum_{k=0}^q b(k) x(n-k)-\sum_{k=1}^p a(k) y(n-k)
$$

$p=0$: finite impulse response (FIR) system  
$p \neq 0$: infinite impulse response (IIR) system

# Discrete-time Fourier transform (DTFT)

$$
X\left(e^{j \omega}\right)=\sum_{n=-\infty}^{\infty} x(n) e^{-j n \omega}=\left|X\left(e^{j \omega}\right)\right| e^{j \phi_x(\omega)}
$$

- Existence requires $x(n)$ abs. summable, unless the (dirac) impulse $u_0(\omega)$ is introduced.
- If $x(n)$ is real, then $X\left(e^{j \omega}\right)=X^*\left(e^{-j \omega}\right)$ or $\left|X\left(e^{j \omega}\right)\right|=\left|X\left(e^{-j \omega}\right)\right|, \phi_x(\omega)=-\phi_x(-\omega)$.

# z-transform


# filters




