---
layout: base
title: Fundamentals
parent: Signals and Systems
nav_order: 1
---

# Transfromations of Independent Variable

#### Time Shift

$$x[n]\longrightarrow x[n-\color{red}{n_0}]$$

$$x(t)\longrightarrow x(t-\color{red}{t_0})$$

The origin moves form 0 to $\color{red}{n_0}$ or $\color{red}{t_0}$.

delayed: $\color{red}{n_0}/\color{red}{t_0}>0$.

advanced: $\color{red}{n_0}/\color{red}{t_0}<0$.

#### Time Reversal

$$x[n]\longrightarrow x[\color{red}{-}n]$$

$$x(t)\longrightarrow x(\color{red}{-}t)$$

#### Time Scaling

$$x[\alpha n]\longrightarrow \mathrm{harizontally \ scaled \ by \ a \ factor \ of} \ \frac{1}{\alpha}$$

$$x(\alpha t)\longrightarrow \mathrm{harizontally \ scaled \ by \ a \ factor \ of} \ \frac{1}{\alpha}$$

#### Properties of Functions

##### Parity

$$even \ \ x[n]=-x[n] \ \ \ \ \ \ \ \ \ \ x(t)=-x(t)$$

$$odd \ x[-n]=-x[n] \ \ \ \ \ \ \ \ x(-t)=-x(t)$$

Any signal can be broken into a sum of two signals:

$$x(t)=\mathcal{Ev}\{x(t)\}+\mathcal{Od}\{x(t)\}$$

$$\mathcal{Ev}\{x(t)\}=\frac{1}{2}[x(t)+x(-t)]$$

$$\mathcal{Od}\{x(t)\}=\frac{1}{2}[x(t)-x(-t)]$$

##### Periodicity

$$x(t)=x(t+T)$$

#### Exponential signals and Sinusoidal signals

##### Real exponential signals

$$x(t)=C\mathrm{e}^{at}$$

##### Sinusoidal signals

$$x(t)=A\cos(\omega_0t+\phi)$$

###### amplitude: $A [-]$

###### fundamental period: $T_0=\frac{2\pi}{\omega_0}=\frac{1}{f}$

###### ordinary frequency: $f \ [\mathrm{s}^{-1}]$ (rate of oscillation / cycles per second)

###### fundamental/angular frequency: $[\mathrm{rad \ s}^{-1}] \ \omega_0=\frac{2\pi}{T_0}=2\pi f$

###### phase: $\phi \ [\mathrm{rad}]$ (${\pi} \ \mathrm{rad}=180^\mathrm{o}$)

##### Forms of signals expression

Using Euler's Formula, we can express or transform signals between exponential form and sinusoidal form. 

$$A\cos(\omega_0t+\phi)=\frac{A}{2}\mathrm{e}^{j(\omega_0t+\phi)}+\frac{A}{2}\mathrm{e}^{-j(\omega_0t+\phi)}=\frac{A}{2}\mathrm{e}^{j\phi}\mathrm{e}^{j\omega_0t}+\frac{A}{2}\mathrm{e}^{-j\phi}\mathrm{e}^{-j\omega_0t}$$

Complex exponential form

$$\color{red}{C\mathrm{e}^{j(\omega_0t+\phi)}}=|C|\cos(\omega_0t+\phi)+|C|j\sin(\omega_0t+\phi)$$

Sinusoidal form

$$\color{red}{A\cos(\omega_0t+\phi)}=A\mathcal{Re}\{\mathrm{e}^{j(\omega_0t+\phi)}\}$$

$$\color{red}{A\sin(\omega_0t+\phi)}=A\mathcal{Im}\{\mathrm{e}^{j(\omega_0t+\phi)}\}$$

We showed the properties using Continuous-time $x(t)$, the properties are also satisfied for discrete-time $x[n]$ but periodicity and phase change causing time shift. It is easy to understand because of discreate signals are not always uniformly distributed relative to its scale.

# Properties of Basic Signals and Systems

## Signals

#### Unit Impulse

$$\delta[n]=

\begin{cases}

0& \text{n$\neq$0}\\

1& \text{n=0}

\end{cases}

\quad

\delta(t)=\frac{\mathrm{d}u(t)}{\mathrm{d}t}  \, (\mathrm{Area=1})$$

Unit impulse at $n=k$: $\delta[n-k]$

#### Unit step

$$
u[n]=

\begin{cases}

0& \text{n<0}\\

1& \text{n$\geq$0}

\end{cases}

\quad

u(t)=

\begin{cases}

0& \text{t<0}\\

1& \text{t>0}

\end{cases}
$$

#### Relations

- First backward difference: $\delta[n]=u[n]-u[n-1]$

- Running sum $u[n]=\sum^n_{m=-\infty}\delta[m]$

​          Running integral $u(t)=\int_{-\infty}^t\delta(\tau)\mathrm{d}\tau$

- Sequence superposition expression $u[n]=\sum^\infty_{k=0}\delta[n-k]$

## Systems

#### Memoryless

$$y(t)=x(t)$$

Its output for each value of the independent variable at a given time is dependent on the input at only that same time.

#### Invertibility

$$y(t)\leftrightarrow x(t)$$

If distinct inputs lead to distinct outputs.

#### Causality

$$y(t)=x(t)+x(t-1)+...$$

If the output at any time depends on values of the input at only the present and past times.

- "nonanticipative": the system output does not anticipate future values of the input.

- All memoryless systems are causal, since the output responds only to the current value of the input.

- Initial rest: if the input to a causal system is 0 up to some point in time, then the output must also be 0 up to that time.

#### Stability

Do not diverge.

#### Time Invariance

$$y(t+k)=x(t+k)$$

If a time shift in the input signal results in an identical time shift in the output signal.\\

Not sensitive to the time origin.

#### Linearity

$$y_1(t)+y_2(t)=x_1(t)+x_2(t)$$

$$ay_1(t)=ax_1(t)$$

The response to $x_1(t)+x_2(t)$ is $y_1(t)+y_2(t)$.\\

The response to $ax_1(t)$ is $ay_1(t)$, where a is any complex constant.

# Convolution - Scaled Superposition

- System: linear (superposition) \& time-invariant (LTI Systems) (for many physical processes)

- Signal: delayed impulses

- time scale: $k/\tau$ time in impulse response; $n/t$ time in system

We find the signal can be constructed by scaled units: Signal is superposition of scaled and shifted unit impulse.

Then the output signal can be represented by the superposition of response signal corresponding to the desired time point scaled by input signal:

$$\mathrm{Output signal \ is \ the \ superposition \ of \ response signals \ scaled \ by \ input signals.}$$

That is the convolution.

#### Sifting property

$$\mathrm{arbitrary \ sequence=linear\ conbination \ of \ shifted \ unit \ impulses} \ \delta[n-k]$$

Discrete-time signal can be constructed by a  a sequence of individual impulses.

$$\mathrm{expresion\ of \ signal} \ [\color{red}{n}] = \ <\color{blue}{\mathrm{sifting \ from -\infty \ to +\infty}}> \ ( \ \mathrm{individual \ impulse \ at} \ [\color{blue}{k}]\ )$$

The impulses can be constructed by linear conbination of unit impulses at that time.

$$( \ \mathrm{individual \ impulse \ at} \ [\color{blue}{k}]\ )= ( \ \mathrm{magnitude \ of \ signal \ at} \ [\color{blue}{k}]\times \mathrm{unit \ impulse \ at} \ [\color{blue}{k}] \ )$$

So Discrete-time signal can be constructed by additional shifted, scaled impulses.

$$\mathrm{expresion\ of \ signal} \ [\color{red}{n}]=\color{blue}{\mathrm{sifting \ from -\infty \ to +\infty}} \ ( \ \mathrm{magnitude \ of \ signal \ at} \ [\color{blue}{k}]\times \mathrm{unit \ impulse \ at} \ [\color{blue}{k}] \ )$$

In summary:

By that we get the \emph{*sifting property*} of discrete-time unit impulse:

$$x[\color{red}{n}]=\color{blue}{\sum_{k=-\infty}^{+\infty}}x[\color{blue}{k}]\delta[\color{red}{n}-\color{blue}{k}]$$

$$x(t)=\int_{-\infty}^{+\infty}x(\tau)\delta(t-\tau)\mathrm{d}\tau$$

## Convolution Sum / Superpositional Sum

$$y[n]=\sum_{+\infty}^{-\infty}x[k]h[n-k]$$  

$$y[n]=x[n]*h[n]$$

Intuitively, $y[n]$ is a superposition of the response scaled by each corresponding impulse; mathematically, $y[n]$ is the sifting and sum of product between response and impluse at point n.  

This two interpretation is equivalent is because of the property of LTI System. It makes each response shifted without any change of profile, and signals is simply  Addable.

## Convolution Integral / Superpositional Integral

Similarly, we firstly develop the \emph{*sifting property*} of the continuous-time impulse:

$$y(t)=\int_{-\infty}^{+\infty}x(\tau)h(t-\tau)\mathrm{d}\tau$$

$$y(t)=x(t)*h(t)$$

## Properties of Linear Time-invariance (LTI) System

#### Commutative property

$$x[n]*h[n]=h[n]*x[n]$$

$$x(t)*h(t)=h(t)*x(t)$$

#### Distributive property

$$x[n]*(h_1[n]+h_2[n])=x[n]*h_1[n]+x[n]*h_2[n]$$

$$x(t)*(h_1(t)+h_2(t))=x(t)*h_1(t)+x(t)*h_2(t)$$

#### Associative property

$$x[n]*(h_1[n]*h_2[n])=(x[n]*h_1[n])*h_2[n]$$

$$x(t)*[h_1(t)*h_2[t)]=[x(t)*h_1(t)]*h_2[t)$$

#### Is it memoryless?

A LTI system is only memoryless if the impulse response:

$$h[n\neq 0]=0$$

$$h(t\neq 0)=0$$

Then the impulse response has the form:

$$h[n]=K\delta [n]$$

$$h(t)=K\delta (t)$$

then the LTI system has the form:

$$y[n]=Kx[n]$$

$$y(t)=Kx(t)$$

#### Invertibility (Analogy: $AA^{-1}=E$)

$$h[n]*h_i[n]=\delta[n]$$

$$h(t)*h_i(t)=\delta(t)$$

Convolving a signal with a shifted impulse is the same as shifting the signal.

$$x(t-t_0)=x(t)*\delta(t-t_0)$$

$$h(t)*h_i(t)=\delta(t-t_0)*\delta(t+t_0)=\delta(t)$$

#### Is it causal (initial rest) ?

A LTI system is only causal if and only if:

$$h[n<0]=0$$

$$h(t<0)=0$$

#### Stability

For bounded input the system has bounded output only if the impulse response is

##### Aabsolutely summable

$$\sum_{k=-\infty}^{+\infty}|h[k]|<\infty$$

##### Absolutely integrable

$$\int_{-\infty}^{+\infty}|h(\tau)|\mathrm{d}\tau<\infty$$

#### Unit Step Response

The response of unit step.

$$s[n]=u[n]*h[n]$$

$$s[n]=\sum_{k=-\infty}^nh[k]$$

$$h[n]=s[n]-s[n-1]$$

$$s(t)=\int_{-\infty}^th(\tau)\mathrm{d}\tau$$

$$h(t)=\frac{\mathrm{d}s(t)}{\mathrm{d}t}=s'(t)$$

## Causal LTI system

### Linear Constant-Coefficient Differential and Difference Equations (Process)

A constraint between the input and the output of a system.

$$\mathrm{solution = particular \ solution + homogeneous \ solution}$$

particular: of, relating to, or concerned with details; denoting an individual member or subclass in logic.

- Homogeneous solution / natural response: with source turned off, initial condition zero. (input is zero)

- Particular solution / forced response: with source turned on, initial condition zero. (have a source as input)

## Nth-order Linear Cnstant-Coefficient Differential Equations

$$\sum_{k=0}^Na_k\frac{\mathrm{d}^ky(t)}{\mathrm{d}t^k}=\sum_{k=0}^Nb_k\frac{\mathrm{d}^kx(t)}{\mathrm{d}t^k}\quad\mathrm{solution}\quad y_p(t)+y_h(t)$$

#### Homogeneous

$$\sum_{k=0}^Na_k\frac{\mathrm{d}^ky(t)}{\mathrm{d}t^k}=0\quad\mathrm{solution}\quad y_h(t)$$

#### Guess solution

$$y_h(t)=A\mathrm{e}^{st}$$

$$\sum_{k=0}^Na_kAs_k\mathrm{e}^{st}=0$$

$$\sum_{k=0}^Na_ks_k=0\quad N \ \mathrm{roots} \ s_i(i=1,2,...,N)$$

$$y_h(t)=A_1\mathrm{e}^{s_1t}+A_2\mathrm{e}^{s_2t}+...+A_N\mathrm{e}^{s_Nt}$$

#### Auxiliary Conditions

$$y(t_0),\frac{\mathrm{d}y(t_0)}{\mathrm{d}t},...,\frac{\mathrm{d}^{N-1}y(t_0)}{\mathrm{d}t^{N-1}}$$

#### Initial Rest Condition

$$y(t_0)=\frac{\mathrm{d}y(t_0)}{\mathrm{d}t}=...=\frac{\mathrm{d}^{N-1}y(t_0)}{\mathrm{d}t^{N-1}}=0$$

## Nth-order Linear Constant-coefficient Difference Equations

$$\sum_{k=0}^Na_ky[n-k]=\sum_{k=0}^Nb_kx[n-k]\quad\mathrm{solution}\quad y_p[t]+y_h[t]$$

#### Homogeneous

$$\sum_{k=0}^Na_ky[n-k]=\=0\quad\mathrm{solution}\quad y_h[n]$$

#### Guess solution

$$y_h[n]=Az^{n}$$

$$\sum_{k=0}^Na_kAz^nz^{-k}=0$$

$$\sum_{k=0}^Na_kz^{-k}=0\quad N \ \mathrm{roots} \ z_i(i=1,2,...,N)$$

$$y_h[n]=A_1z_1^n+A_2z_2^n+...+A_Nz_N^n$$

#### Auxiliary Conditions

$$y[n_0],y[n_0-1],...y[n_0-N+1]$$

#### Recursive Equation - Infinite Impulse Response (IIR) Systems

$$y[n]=\frac{1}{a_0}\left\{\sum_{k-0}^Mb_kx[n-k]-\sum_{k=1}^Na_ky[n-k]\right\}$$

It specifies a recursive procedure for determining the output in terms of the input and previous outputs.

- Recursion: the determination of a succession of elements (such as numbers or functions) by operation on one or more preceding elements according to a rule or formula involving a finite number of steps.

#### Nonrecursive Equation - Finite Impulse Response (FIR) Systems

$$y[n]=\sum_{k=0}^M\left(\frac{b_k}{a_0}\right)x[n-k]$$

#### Block Diagram Representations

## Singularity Functions

This part relate the convolution and differentiation/integration together. And the tool is the singularity function.

### Operational definition of singularity function - differentiator \& integrator

Singular functions can be defined operationally in terms of its behavior under convolution.  

Belows are the examples of operational definitions of singularity functions.

#### Unit impulse $\delta(t)$

$$x(t)=x(t)*\delta(t)$$

#### Unit doublet $u_1(t)$

$$y_1(t)=\frac{\mathrm{d}x(t)}{\mathrm{d}t}=x(t)*u_1(t)$$

Similarly, we can define a $u_2(t)$:

$$y_2(t)=\frac{\mathrm{d}^2x(t)}{\mathrm{d}t^2}=x(t)*u_2(t)$$

It is easy to find that:

$$y_2(t)=\frac{\mathrm{d}^2x(t)}{\mathrm{d}t^2}=\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\mathrm{d}x(t)}{\mathrm{d}t}\right)=(x(t)*u_1(t))*u_1(t)$$

Then

$$u_2(t)=u_1(t)*u_1(t)$$

### Cascades of differentiators $u_{k}(t)$ of order $k$

$u_k(t)$ (k>0) is the kth derivative of $\delta(t)$ and thus is the impulse response of a system that takes the kth derivative of the input.

$$u_k(t)=u_1(t)*...(k \ \mathrm{times})...*u_1(t)$$

### Cascades of integrators $u_{-k}(t)$ of order $k$

An integrator:

$$y(t)=\int_{-\infty}^{t}x(\tau)\mathrm{d}\tau$$

Then we can use the character of integrator to represent a unit step impulse response:

$$u(t)=\int_{-\infty}^{t}\delta(\tau)\mathrm{d}\tau$$

Then the following operation definition of $u(t)$ (operate on an input $x(t)$:

$$x(t)*u(t)=\int_{-\infty}^{t}x(\tau)\mathrm{d}\tau$$

Similarly, define a system of a cascade of two integrators:

$$u_{-2}(t)=u(t)*u(t)=\int_{-\infty}^{t}u(\tau)\mathrm{d}\tau$$

By the way, since $u(t)$ is a unit step impulse response, here is the \emph{*unit ramp function*}:

$$u_{-2}(t)=tu(t)$$

And we get the cascades of integrators:

$$u_{-k}(t)=u(t)*...(k \ \mathrm{times})...*u(t)=\int_{-\infty}^tu_{-(k-1)}(\tau)\mathrm{d}\tau$$

$$\delta(t)=u_0(t)$$

$$u(t)=u_{-1}(t)$$

$$u_k(t)*u_r(t)=u_{k+r}(t)$$

#### Invertibility $u(t)*u_1(t)=u_{-1}(t)*u_1(t)=\delta(t)$

# Fourier Series Representation of Periodic Signals

#### Tigonometric sum Sums of harmonically related sines and cosines or periodic

complex exponentials.

## Response of LTI Systems to Complex Exponentials

The response of an LTI system to a complex exponential input is the same complex

exponential with only a change in amplitude.

$$\mathrm{contunuous \ time} \quad e^{st}\longrightarrow H(s)e^{st}$$

$$\mathrm{discrete \ time} \quad z^n \longrightarrow H(z)z^n$$

$$y(t)=\int_{-\infty}^{+\infty}h(\tau)x(t-\tau)\mathrm{d}\tau=\int_{-\infty}^{+\infty}h(\tau)\mathrm{e}^{s(t-\tau)}\mathrm{d}\tau$$

$$y(t)=e^{st}\int_{-\infty}^{+\infty}h(\tau)\mathrm{e}^{-s\tau}\mathrm{d}\tau$$

Assuming that the integral on the RHS converges,

$$y(t)=H(s)e^{st}$$

Hence, we have shown that complex exponentials are eigenfunctions of LTI systems.The constant $H(s)$ for a specific value of $s$ bis then the eigenvalue associated with the eigenfunction $e^{st}$.

\paragraph{Eigenfunction $e^{st}$} A signal for which the system output is a (possibly complex) constant times the input.

#### Eigenvalue $H(s)$ Amplitude (constant).

#### System Functions

$$H(s)=\int_{-\infty}^{+\infty}h(\tau)\mathrm{e}^{-s\tau}\mathrm{d}\tau$$

$$H(z)=\sum_{-\infty}^{+\infty}h[k]z^{-k}$$

#### Frequency Response Response in frequency domain? $\mathcal{Re}{(s)}=0\rightarrow s=j\omega$

$$H(j\omega)=\int_{-\infty}^{+\infty}h(t)\mathrm{e}^{-j\omega t}\mathrm{d}t$$

$$H(\mathrm{e}^{j\omega})=\sum_{-\infty}^{+\infty}h[n]\mathrm{e}^{j\omega n}$$

## Fourier Series

$$\mathrm{synthesis \ equation}\quad x(t)=\sum_{k=-\infty}^{+\infty}a_ke^{jk\omega_0t}=\sum_{k=-\infty}^{+\infty}a_ke^{jk(2\pi/T)t}$$

#### Fourier Series Coefficients / Spectral Coefficients of $x(t)$

$$\mathrm{analysis \ equation}\quad a_k=\frac{1}{T}\int_Tx(t)e^{-jk\omega_0t}\mathrm{d}T=\frac{1}{t}\int_Tx(t)e^{-jk(2\pi/T)t}\mathrm{d}t$$

#### Fundamental Harmonic Component/First Harmonic Components $x(t)$ when $k=\pm 1$

#### Nth Harmonic Components $x(t)$ when $k=\pm N$

$$a_0=\frac{1}{T}\int_Tx(t)\mathrm{d}t$$

#### Real Periodic Signals $a_k=A_k$

$$x(t)=a_0+2\sum_{k=1}^\infty A_k\cos (k\omega_0t+\theta_k)$$

#### Complex Periodic Signals $a_k=B_k+jC_k$

$$x(t)=a_0+2\sum_{k=1}^\infty[B_k\cos k\omega_0t-C_k\sin k\omega_0t]$$

#### Periodic Square Wave

$$a_0=\frac{2T_1}{T}\quad k=0$$

$$a_k=\frac{\sin (k\omega_0T_1)}{k\pi}\quad k\neq 0$$

## Convergence Conditions of the Fourier Series

#### Finite Energy over a Single Period

$$\int_T|x(t)|^2\mathrm{d}t<\infty$$

#### Dirichlet Conditions

- Condition 1: Over any period, $x(t)$ must be absolutely integrable; this guarantees that each coefficient ak will be finite.

$$\int_T|x(t)|\mathrm{d}t<\infty$$

- Condition 2: In any finite interval of time, $x(t)$ is of bounded variation; that is, there are no more than a finite number of maxima and minima during any single period of the signal.

- Condition 3: In any finite interval of time, there are only a finite number of discontinuities. Furthermore, each of these discontinuities is finite.

#### Gibbs Phenomenon

## Properties of Continuous-time Fourier Series

Same period $T$

$$x(t)\stackrel{\mathcal{FS}}\longleftrightarrow a_k$$

$$y(t)\stackrel{\mathcal{FS}}\longleftrightarrow b_k$$

#### Linearity

$$Ax(t)+By(t)\stackrel{\mathcal{FS}}\longleftrightarrow Aa_k+Bb_k$$

#### Time Shifting

$$x(t-t_0)\stackrel{\mathcal{FS}}\longleftrightarrow a_k\mathrm{e}^{-jk\omega_0t_0}=a_ke^{-jk(2\pi/T)t_0}$$

#### Frequency Shifting

$$e^{jM\omega_0t}x(t)=e^{jM(2\pi/T)t}x(t)\stackrel{\mathcal{FS}}\longleftrightarrow a_{k-M}$$

#### Conjugation

$$x^*(t)\stackrel{\mathcal{FS}}\longleftrightarrow a^*_{-k}$$

#### Time Reversal

$$x(-t)\stackrel{\mathcal{FS}}\longleftrightarrow a_{-k}$$

#### Time Scaling $\alpha>0$, $x(\alpha t)\longleftrightarrow T/\alpha\quad\alpha\omega_0$

$$x(\alpha t)=\sum_{k=-\infty}^{+\infty}a_k\mathrm{e}^{jk\alpha\omega_0t}\stackrel{\mathcal{FS}}\longleftrightarrow a_{k}$$

#### Periodic Convolution

$$\int_Tx(\tau)y(t-\tau)\mathrm{d}\tau\stackrel{\mathcal{FS}}\longleftrightarrow Ta_kb_k$$

#### Multiplication

 Discrete-time convolution of the sequence representing the Fourier coefficients of $x(t)$ and the sequence representing the Fourier coefficients of $y(t)$.

$$x(t)y(t)\stackrel{\mathcal{FS}}\longleftrightarrow \sum_{l=-\infty}^{+\infty} a_lb_{k-l}$$

#### Differentiation

$$\frac{\mathrm{d}x(t)}{\mathrm{d}t}\stackrel{\mathcal{FS}}\longleftrightarrow jk\omega_0a_k=jk\frac{2\pi}{T}a_k$$

#### Integration Finite valued and periodic only if $a_0=0$.

$$\int_{-\infty}^tx(t)\mathrm{d}t\stackrel{\mathcal{FS}}\longleftrightarrow \left(\frac{1}{jk\omega_0}\right)a_k=\left(\frac{1}{jk(2\pi/T)}\right)a_k$$

#### Conjugate symmetry for Real Signals

 $x(t)$ real $x(t)=x^*(t)$.

$$a_k=a_{-k}^*$$

$$\mathcal{Re}\{a_k\}=\mathcal{Re}\{a_{-k}\}$$

$$\mathcal{Im}\{a_k\}=-\mathcal{Im}\{a_{-k}\}$$

$$|a_k|=|a_{-k}|$$

$$\arg a_k=-\arg a_{-k}$$

#### Real and Even Signals

 $x(t)$ real and even, $a_k$ real and even.

#### Real and Odd Signals

 $x(t)$ real and odd, $a_k$ purely imaginary and odd.

#### Even-Odd Decomposition of Real Signals

$$
\begin{cases}

x_e(t)=\mathcal{Ev}\{x(t)\} \ [x(t) \ \mathrm{real}]& \mathcal{Re}\{a_k\}\\

x_o(t)=\mathcal{Od}\{x(t)\} \ [x(t) \ \mathrm{real}]& j\mathcal{Im}\{a_k\}

\end{cases}
$$

#### Parseval's Relation for Continuous-Time Periodic Signals

 $\|a_k\|^2$ is the average power in the $k$th harmonic component of $x(t)$. Thus, what Parseval's relation states is that the total average power in a periodic signal equals the sum of the average powers in all of its harmonic components.

$$\frac{1}{T}\int_T|x(t)|^2\mathrm{d}t=\frac{1}{T}\int_T|a_ke^{jk\omega_0t}|^2\mathrm{d}t=\sum_{k=-\infty}^{+\infty}|a_k|^2$$

#### Impulse Train

$$x(t)=\sum_{k=-\infty}^{+\infty}\delta(t-kT)$$

#### Discrete-time Fourier Series

$$\phi_k[n]=\mathrm{e}^{jk\omega_0n}=\mathrm{e}^{jk(2\pi/T)n},k=0,\pm 1,\pm 2,...$$

$$\phi_k[n]=\phi_{k+rN}[n]$$

$$\mathrm{synthesis \ equation}\quad x[n]=\sum_{k=\langle N\rangle}a_k\phi(n)=\sum_{k=\langle N\rangle}a_k\mathrm{e}^{jk\omega_0n}=\sum_{k=\langle N\rangle}a_k\mathrm{e}^{jk(2\pi/T)n}$$

$$\mathrm{analysis \ equation}\quad a_k=\frac{1}{N}\sum_{n=\langle N\rangle}x[n]\mathrm{e}^{-jk\omega_0n}=\frac{1}{N}\sum_{n=\langle N\rangle}x[n]\mathrm{e}^{-jk(2\pi/N)n}$$

#### First Difference

$$x[n]-x[n-1]\stackrel{\mathcal{FS}}\longleftrightarrow(1-\mathrm{e}^{-jk(2\pi/N)})a_k$$

#### Parseval's Relation

 Parseval's relation states that the average power in a periodic signal equals the sum of the average powers in all of its harmonic components.

$$\frac{1}{N}\sum_{n=\langle N\rangle}|x[n]|^2=\sum_{k=\langle N\rangle}|a_k|^2$$

## Filtering

#### Filtering

 Fhange the relative amplitudes of the frequency components in a signal or perhaps eliminate some frequency components entirely.

- Frequency-shaping Filters: Linear time-invariant systems that change the shape of the spectrum.

- Frequency-selective Filters: Systems that are designed to pass some frequencies essentially undistorted and significantly attenuate or eliminate others.

$$x(t)=\sum_ka_ke^{s_kt}\longrightarrow y(t)=\sum_ka_kH(s_k)e^{s_kt}$$

$$x[n]=\sum_ka_kz_k^n\longrightarrow y[n]=\sum_ka_kH(z_k)z_k^n$$
