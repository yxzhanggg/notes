---
layout: default
title: Mechanics
parent: Fundamentals
nav_order: 4
---

---

Landau

---

# The Equation of Motion

#### The Equation of Motion

The relations between the accelerations, velocities and co-ordinates are called the \emph{*equations of motion*}.

## Generalised Co-ordinates

#### Particle

A body whose dimensions may be neglected in describing its motion.

#### Cartesian Co-ordinates $x,y,z$ 

#### Radius Vector

$\mathbf{r}=(x,y,z)$ (Cartesian co-ordinates)

#### Velocity $\mathbf{v}=\mathrm{d}\mathbf{r}/\mathrm{d}t=\dot{\mathbf{r}}$

#### Acceleration $\mathbf{a}=\mathrm{d}^2\mathbf{r}/\mathrm{d}t^2=\ddot{\mathbf{r}}$

#### The Number of Degree of Freedom

The number of independent quantities which must be specified in order to define uniquely the position of any system.

#### Quantities $q_i$

- Generalised co-ordinates: Any $s$ quantities $q_1,q_2,...,q_s$ which completely define the position of a system with $s$ degrees of freedom.

- Generalised velocities $\dot{q_i}$

## Principle of Least Action / Hamilton's Principle

#### Lagrangian

 A definite function which characterizes a mechanical system.

$$L(q_1,q_2,...,q_s,\dot{q}_1,\dot{q_2},...,\dot{q_s},t)\quad \mathrm{or}\quad L(q,\dot{q},t)$$

#### Action

$$S=\int_{t_1}^{t_2}L(q,\dot{q},t)\mathrm{d}t$$

#### Principle of Least Action

The defineing condition of the system is that action $S$ takes the least possible value.

#### Variation of funtion $q(t)$ $\delta q(t)$ is a function which is small everywhere in the interval of time from $t_1$ to $t_2$.

 $$\mathbf{Principle \ of \ Least \ Action\longrightarrow Lagrange's \ Equations}$$

$$\delta S=0$$

Replace $q(t)$ by $q(t)+\delta q(t)$ to get:

$$\delta q(t_1)=\delta q(t_2)=0$$

$$
\begin{aligned}
\delta S=\delta \int_{t_{1}}^{t_{2}} L(q, \dot{q}, t) \mathrm{d} t &=\int_{t_{1}}^{t_{2}}\left(\frac{\partial L}{\partial q} \delta q+\frac{\partial L}{\partial \dot{q}} \delta \dot{q}\right) \mathrm{d} t \\
& \stackrel{\delta \dot{q}=\mathrm{d}(\delta q) / \mathrm{d} t}{=} \int_{t_{1}}^{t_{2}}\left(\frac{\partial L}{\partial q} \delta q+\frac{\partial L}{\partial \dot{q}} \frac{\mathrm{d} \delta q}{\mathrm{~d} t}\right) \mathrm{d} t \\
& \stackrel{\text { integrating by part of 2nd term }}{=}\left[\frac{\partial L}{\partial \dot{q}} \delta q\right]_{t_{1}}^{t_{2}}+\int_{t_{1}}^{t_{2}}\left[\frac{\partial L}{\partial q}-\frac{\mathrm{d}}{\mathrm{d} t}\left(\frac{\partial L}{\partial \dot{q}}\right)\right] \delta q \mathrm{~d} t=0
\end{aligned}
$$

$$\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial L}{\partial\dot{q}}\right)-\frac{\partial L}{\partial q}=0$$

For $s$ different functions $q_i(t)$:

#### Lagrange's Equations

Give the relations between accelerations. velocities and coordinates.

$$\color{red}{\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial L}{\partial\dot{q}_i}\right)-\frac{\partial L}{\partial q_i}=0}\quad(i=1,2,...,s)$$

#### Properties of Lagrangians

##### Additivity

$$\lim L=L_A+L_B$$

##### The Lagrangian is defined only to within $\frac{\mathrm{d}}{\mathrm{d}t}f(q,t)$}

$$L'(q,\dot{q},t)=L(q,\dot{q},t)+\frac{\mathrm{d}}{\mathrm{d}t}f(q,t)$$

$$S'=\int_{t_1}^{t_2}L'(q,\dot{q},t)\mathrm{d}t=\int_{t_1}^{t_2}L(q,\dot{q},t)\mathrm{d}t+\int_{t_1}^{t_2}\frac{\mathrm{d}f}{\mathrm{d}t}\mathrm{d}t=S+f(q^{(2)},t_2)-f(q^{(1)},t_1)$$

$$\delta S'=0\longleftrightarrow\delta S=0$$

Then the equation of motion unchanged.

## Galileo's Relativity Principle

An infinity of inertial frames moving, relative to one another, uniformly in a straight line. In all these frames the properties of space and time are the same, and the laws of mechanics are the same.

#### A Frame of Reference 

Finding a frame of reference in which the laws of mechanics take their simplest form.

#### Inhomogeneous and Anisotropic

Even if a body interacted with no other bodies, different \emph{*time*}, its various \emph{*positions*} in space and its different \emph{*orientations*} would not be mechanically equivalent.

#### Inertial Frame of Reference

A frame of reference which space is homogeneous and isotropic and time is homogeneous.

$$\mathbf{Lagrange's \ Equations\longrightarrow Law \ of \ Inertia}$$

##### Lagrangian

Independent of the radius vector $\mathbf{r}$ $(\frac{\partial L}{\partial \mathbf{r}}=0)$ and time $t$.

$$L=L(v^2)$$

##### Lagrange's Equation

$$\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial L}{\partial\mathbf{v}}\right)=0$$

Hence $\partial L/\partial\mathbf{v}=\mathrm{constant}$. Since $\partial L/\partial\mathbf{v}$ is a function of the velocity $\mathbf{v}$ only, it folows that $\mathbf{v}=\mathrm{constant}$.

#### Law of Inertia

In an inertial frarne, any free motion takes place with a velocity which is constant in both magnitude and direction.

#### Properties of Inertial Frame of Reference

No "absolute" frame preferred.

#### Galilean Transformation

$$\mathrm{Frame \ of \ reference \ K}: \mathrm{Coordinate \ r},\mathrm{Relative \ velocity \ \mathbf{0}}$$

$$\mathrm{Frame \ of \ reference \ K'}: \mathrm{Coordinate \ r'},\mathrm{Relative \ velocity \ \mathbf{V}}$$

$$\mathbf{r}=\mathbf{r}'+\mathbf{V}t$$

$$t=t'$$

## The Lagrangian for a Free Particle

$$v'=v+\epsilon$$

$$L(v^2)$$

$$L'=L(v'^2)=L(v^2+2\mathbf{v}\cdot\mathbf{\epsilon}+\epsilon^2)$$

Expanding this expression in powers of $\epsilon$ and neglecting terms above the first order:

$$L(v'^2)=L(v^2)+\frac{\partial L}{\partial v^2}2\mathbf{v\cdot\epsilon}$$

The second term on the right of this equation is a total time derivative only if it is a linear function of the velocity $\mathbf{v}$. Hence $\frac{\partial L}{\partial v^2}$ is independent of the velocity.

#### Mass $m$

$$L=\frac{1}{2}mv^2$$

$$L'=\frac{1}{2}mv'^2=\frac{1}{2}mv^2+m\mathbf{v\cdot V}+\frac{1}{2}mV^2=L+\mathrm{d}(m\mathbf{r\cdot V}+\frac{1}{2}mV^2t)/\mathrm{d}t$$

The second term is a total time derivative and may be omitted.

#### Additive Property

$$L=\sum\frac{1}{2}m_av_a^2$$

#### Co-ordinates

$$v^2=(\mathrm{d}l/\mathrm{d}t)^2=(\mathrm{d}l)^2/(\mathrm{d}t)^2$$

##### Cartesian co-ordinates

$$\mathrm{d}l^2=\mathrm{d}x^2+\mathrm{d}y^2+\mathrm{d}z^2$$

$$L=\frac{1}{2}m(\dot{x}^2+\dot{y}^2+\dot{z}^2)$$

#### Cylindrical co-ordinates

$$\mathrm{d}l^2=\mathrm{d}r^2+r^2\mathrm{d}\phi^2+\mathrm{d}z^2$$

$$L=\frac{1}{2}m(\dot{r}^2+r^2\dot{\phi}^2+\dot{z}^2)$$

##### Spherical co-ordinates

$$\mathrm{d}l^2=\mathrm{d}r^2+r^2\mathrm{d}\theta^2+r^2\sin^2\theta\mathrm{d}\phi^2$$

$$L=\frac{1}{2}m(\dot{r}^2+r^2\dot{\theta}^2+r^2\dot{\phi}^2\sin^2\theta)$$

## The Lagrangian for a System of Particles

#### Closed System

A system of particles which interact with one another but with no other bodies.

$$L=\sum\frac{1}{2}m_av_a^2-U(\mathbf{r}_1,\mathbf{r}_2,...)$$

##### Kinetic energy $T=\sum\frac{1}{2}m_av_a^2$

##### Potential energy $U(\mathbf{r}_1,\mathbf{r}_2,...)$

##### Lagrange's equations

$$\frac{\mathrm{d}}{\mathrm{d}t}\frac{\partial L}{\partial\mathbf{v}_a}=\frac{\partial L}{\partial \mathbf{r}_a}$$

#### Newton's Equations

$$m_a\frac{\mathrm{d}\mathbf{v}_a}{\mathrm{d}t}=-\frac{\partial U}{\partial\mathbf{r}_a}$$

#### The Force on the ath Particle

$$\mathbf{F}=-\frac{\partial U}{\partial\mathbf{r}_a}$$

#### Generalised co-ordinates $q_i$

$$x_a=f_a(q_1,q_2,...,q_s)$$

$$\dot{x}_a=\sum_k\frac{\partial f_a}{\partial q_k}\dot{q}_k$$

$$L=\frac{1}{2}\sum_k m_a(\dot{x}_a^2+\dot{y}_a^2+\dot{z}_a^2)-U$$

$$L=\frac{1}{2}\sum_{i,k}a_{ik}\dot{q}_i\dot{q}_k-U(q)$$

##### $a_{ik}$: functions of the co-ordinates only

#### Single Particle Moves in an External Field

$$\mathrm{General \ Form \ of \ the \ Lagrangian}\quad L=\frac{1}{2}mv^2-U(\mathbf{r},t)$$

$$\mathrm{Equation \ of \ Motion}\quad\dot{\mathbf{v}}=-\frac{\partial U}{\partial\mathbf{r}}$$

$$\mathrm{Potential \ Energy}\quad U=-\mathbf{F\cdot r}\quad(\mathrm{uniform \ field})$$

##### $A$ in field $B$

$$L_A=T_A(q_A,\dot{q}_A)-U[q_A,q_B(t)]$$

# Conservation Laws (Closed System)

## Energy - Homogeneous of Time

#### Integrals of Motion

Functions of quantities in $q_i$ and $\dot{q}_i$ whose values remain constant during the motion, and depend only on the initial conditions.

- energy $E\equiv\sum_a\frac{1}{2}m_av_a^2+U(\mathbf{r}_1,\mathbf{r}_2,...)$

- three components of momentum $P\equiv\sum_a m_a\mathbf{v}_a$

- three components of angular momentum $\mathbf{M}\equiv\sum_a\mathbf{r}_a\times\mathbf{p}_a$

#### Lagrangian of Closed System

$$\frac{\mathrm{d} L}{\mathrm{d}t}=\sum_i\frac{\partial L}{\partial q_i}\dot{q}_i+\sum_i\frac{\partial L}{\partial \dot{q}_i}\ddot{q}_i$$

Replace by Lagrange's Equations,

$$\frac{\mathrm{d} L}{\mathrm{d}t}=\sum_i\dot{q}_i\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial L}{\partial\dot{q}_i}\right)+\sum_i\frac{\partial L}{\partial \dot{q}_i}\ddot{q}_i=\sum_i\frac{\mathrm{d}}{\mathrm{d}t}\left(\dot{q}_i\frac{\partial L}{\partial\dot{q}_i}\right)$$

$$\frac{\mathrm{d}}{\mathrm{d}t}\left(\sum_i\dot{q}_i\frac{\partial L}{\partial\dot{q}_i}-L\right)=0$$

$$E \equiv \sum_{i} \dot{q}_{i} \frac{\partial L}{\partial \dot{q}_{i}}-L \stackrel{\text { Euler'sTheorem }}{=} T(q, \dot{q})+U(q)=\sum_{a} \frac{1}{2} m_{a} v_{a}^{2}+U\left(\mathbf{r}_{1}, \mathbf{r}_{2}, \ldots\right)$$

## Momentum - Homogeneous of Space

$$\delta L = \sum_a\frac{\partial L}{\partial\mathbf{r}_a}\cdot\delta\mathbf{r}_a=\epsilon\cdot\sum_a\frac{\partial L}{\partial\mathbf{r}_a}=0$$

$$\sum_a\frac{\partial L}{\partial\mathbf{r}_a}=0$$

From Lagrange's Equations,

$$P\equiv\frac{\partial L}{\partial \mathbf{v}_a}=\sum_a m_a\mathbf{v}_a$$

#### Newton's Third Law

$$\frac{\partial L}{\partial\mathbf{r}_a}=-\frac{\partial U}{\partial\mathbf{r}_a}=\mathbf{F}_a=0$$

#### Generalized Momenta

$$p_i=\frac{\partial L_i}{\partial \dot{q}}$$

#### Generalized Forces

$$F_i=\frac{\partial L_i}{\partial q}$$

#### Lagrange's Equations

$$\dot{p}_i=F_i$$

## Centre of Mass

#### Two Frames of Reference $K$ and $K'$

$$\mathbf{P}=\mathbf{P}'+\mathbf{V}\sum_am_a$$

#### At Rest

 $\mathbf{P}'=0$ The total momentum of a mechanical system in a given frame of reference is zero.

$$\mathbf{V}=\mathbf{P}/\sum_am_a=\sum_am_a\mathbf{v}_a/\sum_am_a$$

#### Additivity of Mass

$$\mu=\sum_am_a$$

#### Cetre of Mass of the System

Velocity of the system as a whole is the rate of motion in space of \emph{*the point*} whose radius vector is

$$\mathbf{R}\equiv\sum_am_a\mathbf{r}_a/\sum_am_a$$

#### Internal Energy $E_i$

The energy of a mechanical system which is at rest as a whole. This includes the kinetic energy of the relative motion of the particles in the system and the potential energy of their interaction.

#### Two Frames of Reference $K$ and $K'$

$$E=E'+\mathbf{V\cdot P'}+\frac{1}{2}\mu\mathbf{V}^2$$

If the centre of mass is at rest in $K'$, then $P'=0$, $E'=E_i$, we have

$$\mathrm{total \ energy}\quad E=\frac{1}{2}\mu\mathbf{V}^2+E_i\quad\mathrm{System \ moves \ with \ velocity \ of \ \mathbf{V}}$$

## Angular Momentum

$$|\delta \mathbf{r}|=r\sin\theta\delta\phi$$

$$\delta \mathbf{r}=\delta\mathbf{\Phi}\times\mathbf{r}$$

$$\delta \mathbf{v}=\delta\mathbf{\Phi}\times\mathbf{v}$$

$$\delta L=\sum_a\left(\frac{\partial L}{\partial\mathbf{r}_a}\cdot\delta\mathbf{r}_a+\frac{\partial L}{\partial\mathbf{v}_a}\cdot\delta\mathbf{v}_a\right)=\delta\mathbf{\Phi}\cdot\frac{\mathrm{d}}{\mathrm{d}t}\sum_a\mathbf{r}_a\times\mathbf{p}_a=0$$

#### Angular Momentum / Moment of Momentum

$$\mathbf{M}\equiv\sum_a\mathbf{r}_a\times\mathbf{p}_a$$

#### Two Frames of Reference $K$ and $K'$

$$\mathbf{r}_a=\mathbf{r}_a'+\mathbf{a}$, $\mathbf{v}_a=\mathbf{v}_a'+\mathbf{V}$$

$$\mathbf{M}=\mathbf{M}'+\mathbf{a}\times\mathbf{P}$$

$$\mathbf{M}=\mathbf{M}'+\mu\mathbf{R}\times\mathbf{V}$$

## Mechanical Similarity

#### Homogeneous Function

$\alpha$ is any constant and $k$ the degree of homogeneity of the function.

$$U(\alpha\mathbf{r}_1,\alpha\mathbf{r}_2,...\alpha\mathbf{r}_n)=\alpha^kU(\alpha\mathbf{r}_1,\alpha\mathbf{r}_2,...\alpha\mathbf{r}_n)$$

#### Transformation

$$\mathbf{r}_a\rightarrow\alpha\mathbf{r}_a$$

$$t\rightarrow\beta t$$

$$L=\sum\frac{1}{2}m_av_a^2-U(\mathbf{r}_1,\mathbf{r}_2,...)$$

$$\frac{\alpha^2}{\beta^2}=\alpha^k$$

$$\beta=\alpha^{1-\frac{1}{2}k}$$

$$\frac{t'}{t}=\left(\frac{l'}{l}\right)^{1-\frac{1}{2}k}$$

$$\frac{v'}{v}=\left(\frac{l'}{l}\right)^{\frac{1}{2}k}$$

$$\frac{E'}{E}=\left(\frac{l'}{l}\right)^k$$

$$\frac{M'}{M}=\left(\frac{l'}{l}\right)^{1+\frac{1}{2}k}$$

#### Homogeneous Function

$$f(sx_1,...,sx_n)=s^kf(x_1,...,x_n)$$

#### Euler's Homogeneous Function Theorem

If $f$ is a (partial) function of n real variables that is positively homogeneous of degree $k$, and continuously differentiable in some open subset of $\mathbb{R}^{n}$ then it satisfies in this open set the partial differential equation

$$kf(x_1,...,x_n)=\sum_{i=1}^nx_i\frac{\partial f}{\partial x_i}(x_1,...,x_n)$$

#### Virial Theorem

$$2\overline{T}=k\overline{U}$$

# Integration of the Equations of Motion

## Motion in One Dimension



---

V. I. Arnold

---

# Newtonian Mechanics

Newtonian mechanics studies the motion of a system of point masses in three-dimensional euclidean space.

A newtonian potential mechanical system is specified by the masses of the points and by the potential energy. The motions of space which leave the potential energy invariant correspond to laws of conservation.

#### Affine N-dimensional Space $A^n$
