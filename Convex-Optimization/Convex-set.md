---
layout: math
---

#### affine set

 A set  $C \subseteq \mathbf{R}^{n}$ is **affine** if the line through any two distinct points in $C$ lies in $ C$.

Every affine set can be expressed as the solution set of a system of linear equations.

![Screen Shot 2022-07-13 at 11.06.48 AM](https://live.staticflickr.com/65535/52212234482_fb037e04b7_o.png)

#### Aﬃne combination of $x_1, \ldots x_k$

 $\theta_{1} x_{1}+\cdots+\theta_{k} x_{k}$ where $\theta_{1}+\cdots+\theta_{k}=1$

an aﬃne set contains every aﬃne combination of its points.

#### Affine hull

 The set of all aﬃne combinations of points in some set $C \subseteq \mathbf{R}^{n}$ 

$$\text { aff } C=\left\{\theta_{1} x_{1}+\cdots+\theta_{k} x_{k} \mid x_{1}, \ldots, x_{k} \in C, \theta_{1}+\cdots+\theta_{k}=1\right\}$$

#### Affine dimension

We deﬁne the affine dimension of a set C as the dimension of its aﬃne hull.

#### Relative interior of set $C$

#### $\text { relint } C=\{x \in C \mid B(x, r) \cap \text { aff } C \subseteq C \text { for some } r>0\}$ Where $B(x, r)=\{y \mid\|y-x\| \leq r\}$ 

#### Convex sets

A set $C$ is convex if the line segment between any two points in $C$ lies in $C$.

A convex set every locally optimal solution is global.

#### Convex combination of $x_1, \ldots x_k$

$\theta_{1} x_{1}+\cdots+\theta_{k} x_{k}$ where $\theta_{1}+\cdots+\theta_{k}=1$, and $\theta_{i} \geq 0, i=1, \ldots, k$. A convex combination of points can be thought of as a mixture or weighted average of the points.

#### Convex hull

is the smallest convex set that contains $C$

$$\operatorname{conv} C=\left\{\theta_{1} x_{1}+\cdots+\theta_{k} x_{k} \mid x_{i} \in C, \theta_{i} \geq 0, i=1, \ldots, k, \theta_{1}+\cdots+\theta_{k}=1\right\}$$

![image-20220720230059916](https://s2.loli.net/2022/07/21/CnHvu2MqBWDT9hb.png)

#### cone

A set $C$ is called a **cone**, or **nonnegative homogeneous,** if for every $x \in C$ and $\theta \geq 0$ we have $\theta x \in C$.

#### convex cone

A set $C$ is a **convex cone** if it is convex and a cone, which means that for any $x_{1}, x_{2} \in C$ and $\theta_{1}, \theta_{2} \geq 0$, we have $\theta_{1} x_{1}+\theta_{2} x_{2} \in C$.

#### conic combination

A point of the form $\theta_{1} x_{1}+\cdots+\theta_{k} x_{k}$ with $\theta_{1}, \ldots, \theta_{k} \geq 0$ is called a **conic combination** (or a **nonnegative linear combination**) of $x_{1}, \ldots, x_{k}$.

#### conic hull

The **conic hull** of a set $C$ is the set of all conic combinations of points in $C, i . e .$

$$\left\{\theta_{1} x_{1}+\cdots+\theta_{k} x_{k} \mid x_{i} \in C, \theta_{i} \geq 0, i=1, \ldots, k\right\}$$

![image-20220720230129635](https://s2.loli.net/2022/07/21/v31At7FGOTU4RzN.png)

Affine > cone > convex

#### hyperplane

![image-20220722163155786](https://s2.loli.net/2022/07/22/Ydh2nXMrkDjLuvS.png)

![image-20220722162902484](https://s2.loli.net/2022/07/22/8hpXyIa1v745WTJ.png)

Analytically it is the solution set of a nontrivial linear equation among the components of x (and hence an affine set).



![image-20220722165851620](https://s2.loli.net/2022/07/22/5y9x6NkRUfHzWGK.png)

#### half spaces

![image-20220722181328554](https://s2.loli.net/2022/07/23/Gp5JqTnAgd6EkcN.png)

![image-20220722172842182](https://s2.loli.net/2022/07/22/9q4mciNLgvZxdOW.png)

![image-20220722181241168](https://s2.loli.net/2022/07/23/faeQwkmHzEKWAd1.png)

#### Euclidian Norm

![image-20220722184556317](https://s2.loli.net/2022/07/23/n4SQJ1Wf7m2ibyM.png)

#### Euclidean balls

![image-20220722183949404](https://s2.loli.net/2022/07/23/hcZMC5a36DWOJw1.png)#

![image-20220722184858800](https://s2.loli.net/2022/07/23/YzWkFgQin83ROIf.png)

#### ellipsoids

![image-20220722191559915](https://s2.loli.net/2022/07/23/AS8kJ1Wxyqf6lHs.png)

![image-20220722191543139](https://s2.loli.net/2022/07/23/le2ThV4dsZWngiX.png)

#### Norm ball

![image-20220722194829785](https://s2.loli.net/2022/07/23/jyufSWVli7R4IZB.png)

#### Nrom corn

![image-20220722194937021](https://s2.loli.net/2022/07/23/8eH7KlCo4tuORQS.png)

#### Second order corn

![image-20220722195926374](https://s2.loli.net/2022/07/23/TFiKftBJNa5rPDk.png)

![image-20220722195000463](https://s2.loli.net/2022/07/23/Tj9hkfE23OYBzPs.png)

#### Polyhedra

A polyhedron is defined as the solution set of a finite number of linear equalities and inequalities.

the intersection of a finite number of halfspaces and hyperplanes.

![image-20220722200416897](https://s2.loli.net/2022/07/23/Sg1szaQ5vjB8MVt.png)

![image-20220722202235236](https://s2.loli.net/2022/07/23/nATwbe4iOBq63um.png)

![image-20220722202331832](https://s2.loli.net/2022/07/23/vKigXVm5CPa6syI.png)

![image-20220722202528304](https://s2.loli.net/2022/07/23/DNhcrEnZ1uqJIQT.png)

#### polytope

A bounded polyhedron

#### Simplex

affinely independent $v_0,\ldots ,v_k$:

![image-20220722204838335](https://s2.loli.net/2022/07/23/DcoqXLnENy25iKM.png)

#### Unit simplex - n dimension

![image-20220722224635017](https://s2.loli.net/2022/07/23/nAFIRUxpsKft1iJ.png)

![image-20220722224940380](https://s2.loli.net/2022/07/23/TJYot6RGrcI9Mbf.png)

#### Probability simplex - n-1 dimension

![image-20220722225029525](https://s2.loli.net/2022/07/23/oYiL6f4uVCrF1Dv.png)

![image-20220722225050705](https://s2.loli.net/2022/07/23/SFOxVqdUk4e87mD.png)