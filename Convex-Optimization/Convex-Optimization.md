---
layout: default
title: Convex Optimization
nav_order: 6
has_children: true
permalink: /docs/Convex-Optimization
---

Reference: Boyd, Stephen, Stephen P. Boyd, and Lieven Vandenberghe. *Convex optimization*. Cambridge university press, 2004.

![Screen Shot 2022-07-13 at 11.43.47 AM](https://live.staticflickr.com/65535/52213287116_9a61f2835f_o.png)

---

#### Mathematical optimization problem

$\begin{array}{ll}
\operatorname{minimize} & f_{0}(x) \\
\text {subject to } & f_{i}(x) \leq b_{i}, \quad i=1, \ldots, m
\end{array}$

**Optimization variable** $x=(x_1, \ldots, x_n)$

**Objective function** $f_{0}: \mathbf{R}^{n} \rightarrow \mathbf{R}$

**Constraint functions**  $f_{i}: \mathbf{R}^{n} \rightarrow \mathbf{R}, \quad i=1, \ldots, m$

**Limits/bounds for the constraints**  $b_1, \ldots, b_m$

**Optimal vector / solution** $x^\star$

#### Linear program

If  objective and constraint functions $f_0, \ldots, f_m$ are linear.

$$f_{i}(\alpha x+\beta y)=\alpha f_{i}(x)+\beta f_{i}(y) \ \text{for all} \ x, y\in\mathbb{R}^n\ \text{and all} \ \alpha, \beta\in\mathbb{R}$$

$$\begin{array}{ll}
\operatorname{minimize} & c^{T} x \\
\text { subject to } & a_{i}^{T} x \leq b_{i}, \quad i=1, \ldots, m
\end{array}$$

Here the vector $c, a_{1}, \ldots, a_{m} \in \mathbf{R}^{n}$ and the scalar $b_{1}, \ldots, b_{m} \in \mathbf{R}$ are problem parameters that specify the objective and constraint functions.a

#### Nonlinear program

If not above but not convex.

#### Convex optimization problems

$$f_{i}(\alpha x+\beta y) \leq \alpha f_{i}(x)+\beta f_{i}(y)$ for all $x, y\in\mathbb{R}^n$ And all $\alpha, \beta\in\mathbb{R}$ with $\alpha+\beta=1, \alpha \geq 0, \beta \geq 0$$

We can consider convex optimization to be a generalization of linear programming.

##### Application

The optimization problem is an abstraction of the problem of making the best possible choice of a vector in $R^n$ from a set of candidate choices.

#### Least-squares problems

A least-squares problem is an optimization problem with **no constraints** and an objective which is a sum of squares of terms of the form $a_{i}^{T} x-b_{i}$:

$$\operatorname{minimize} \quad f_{0}(x)=\|A x-b\|_{2}^{2}=\sum_{i=1}^{k}\left(a_{i}^{T} x-b_{i}\right)^{2} .$$

Here $A \in \mathbf{R}^{k \times n} \text { (with } k \geq n \text { ) }$, $a_i^T$ are the rows of $A$, vector $x\in R$ is the optimization variable.

$$\left(A^{T} A\right) x=A^{T} b$$

$$x=\left(A^{T} A\right)^{-1} A^{T} b$$

**Rocognizing least-squares problem** the objective is a quadratic function; the associated quadratic form is positive semideﬁnite.

**Weighted least-squares** $\sum_{i=1}^{k} w_{i}\left(a_{i}^{T} x-b_{i}\right)^{2}$, where $w_{1}, \ldots, w_{k}$ are positive, is minimized.

**Regularization** $\sum_{i=1}^{k}\left(a_{i}^{T} x-b_{i}\right)^{2}+\rho \sum_{i=1}^{n} x_{i}^{2}$ Where $\rho>0$. Regularization comes up in statistical estimation when the vector x to be estimated is given a prior distribution.
