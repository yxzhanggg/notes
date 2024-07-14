---
layout: default
title: Information and Probability
nav_order: 4
has_children: true
permalink: /docs/Info-Prob
---

# Information theory

![image-20220719104113266](https://s2.loli.net/2022/07/19/eOy1dLohzQ6HmCM.png)

#### conveying information

1. "setup": agree on what they will communicate about, , and exactly what each sequence of bits means - **code**.
2. “outcome”: sequences of information are sent - data.

#### uncertainty

#### Boolean functions

![image-20220719114825806](https://s2.loli.net/2022/07/19/ifOKhXY6lCwD8ye.png)

![image-20220719115040461](https://s2.loli.net/2022/07/19/Aj9qg7tTNb2DSnZ.png)

![image-20220719115105061](https://s2.loli.net/2022/07/19/fUPt8dc1qxDvzJY.png)

#### Properties of Boolean Algebra

![image-20220719115238219](https://s2.loli.net/2022/07/19/nJo9rdTZ53Nq2kx.png)

#### Logic gates

![image-20220719115517595](https://s2.loli.net/2022/07/19/aDPz1rIW9uJbvfS.png)

![image-20220719115538278](https://s2.loli.net/2022/07/19/oNbau1j78YxRhQl.png)

#### quantum bit / qubit

a model of an object that can store a single bit but is so small that it is subject to the limitations quantum mechanics places on measurements

1. Reversibility: transformation between each state.
1. Superposition
1. Entanglement

#### classical bit

an abstraction in which the bit can be measured without perturbing it.

$$0V-0.2V=0,0.8V-1V=1$$

#### encode and decode

![image-20220719163748627](https://s2.loli.net/2022/07/19/rFRhSsYxWaHQzEK.png)

#### symbol space size

the number of symbols that need to be encoded

#### Integer codes

![image-20220719195624004](https://s2.loli.net/2022/07/20/B2E1pTWCVh5nYzO.png)

#### Morse code

![image-20220719203232092](https://s2.loli.net/2022/07/20/WmV4yNnq7gQx8Fw.png)

#### Compression

![image-20220719205911075](https://s2.loli.net/2022/07/20/GwyNs2iBRVWJudj.png)

- Variable-Length Encoding

- Run Length Encoding

- Static Dictionary

- Semi-adaptive Dictionary

- Dynamic Dictionary - LZW compression technique

  ![image-20220720184633043](https://s2.loli.net/2022/07/21/O9hArFWmPCnEINU.png)

- Discrete Cosine Transformation

  ![image-20220720184657241](https://s2.loli.net/2022/07/21/yNXUongwKarvhCm.png)

![image-20220720184703353](https://s2.loli.net/2022/07/21/7svi48ydKrcSG1M.png)

#### Hamming Distance

the diﬀerence between two bit patterns is the number of bits that are diﬀerent between the two.

#### code rate

the number of bits before channel coding divided by the number after the encoder.

#### Parity

"check bit"added bit would be 1 if the number of bits equal to 1 is odd, and 0 otherwise.

#### Rectangular Codes

![image-20220720184958471](https://s2.loli.net/2022/07/21/XPkx9elMAFGtDOu.png)

---

# Probability theory

#### Marginal Probability

$$p(X=x_i)=\sum_{j=1}^Lp(X=x_i,Y=y_j)$$

#### Conditional Probability of $Y=y_j$ given $X=x_i$

$$p(Y=y_i|X=x_i)=\frac{n_ij}{ci}$$

For single point probability

$$p(X=x_i,Y=y_j)=\frac{n_{ij}}{c_i}\cdot\frac{c_i}{N}=p(Y=y_j|X=x_i)P(X=x_i)$$

#### Sum Rule

$$p(X)=\sum_Yp(X,Y)$$

#### Product Rule

$$p(X,Y)=p(Y|X)p(X)$$

#### Bayes' Theorem

$$p(Y|X)=\frac{p(X|Y)p(Y)}{p(X)}$$

$$p(X)=\sum_Yp(X|Y)p(Y)$$

Continuous form:

$$p(x)=\int p(x,y)\mathrm{d}y$$

$$p(x,y)=p(y|x)p(x)$$

#### Probability Density over $x$: $p(x)$

$$p(x\in(a,b))=\int_a^bp(x)\mathrm{d}x$$

$$p(x)\geq0$$

$$\int_{-\infty}^{\infty}p(x)=1$$

#### Cumulative Distribution Function $P(z)$

$$P(z)=\int_{-\infty}^zp(x)\mathrm{d}x$$

$$P'(x)=p(x)$$

#### Joint Probability Density in $\mathbf{x}$ Space

$$p(\mathbf{x})=p(x_1,...,x_D)$$

$$p(\mathbf{x})\geq0$$

$$\int_{-\infty}^{\infty}p(\mathbf{x})=1$$

If $\mathbf{x}$ is discrete, $p(\mathbf{x})$ is called \emph{*probability mass function*}.

#### Expectation of $f(x)$: $\mathbb{E}(f)$

$$\mathbb{E}[f]=\sum_xp(x)f(x)$$

$$\mathbb{E}[f]=\int p(x)f(x)\mathrm{d}x$$

Approximation:

$$\mathbb{E}[f]\simeq\frac{1}{N}\sum_{n=1}^N f(x_n)$$

Multi-variable:

$$\mathbb{E}_x[f(x,y)]$$

$$\mathbb{E}_x[f|y]=\sum_xp(x|y)f(x)$$

#### Variance

$$\mathrm{var}[f]=\mathbb{E}[(f(x)-\mathbb{E}[f(x)])^2]$$

$$\mathrm{var}[f]=\mathbb{E}[f(x)^2]-\mathbb{E}[f(x)]^2$$

In particular,

$$\mathrm{var}[x]=\mathbb{E}[x^2]-\mathbb{E}[x]^2$$

Covariance of two random variables:

$$\mathrm{cov}[x,y]=\mathbb{E}_{x,y}[\{x-\mathbb{E}[x]\}\{y-\mathbb{E}[y]\}]=\mathbb{E}_{x,y}[xy]-\mathbb{E}[x]\mathbb{E}[y]$$

For two vectors:

$$\mathrm{cov}[\mathbf{x},\mathbf{y}]=\mathbb{E}_{\mathbf{x},\mathbf{y}}[\{\mathbf{x}-\mathbb{E}[\mathbf{x}]\}\{\mathbf{y}^\mathrm{T}-\mathbb{E}[\mathbf{y}^\mathrm{T}]\}]=\mathbb{E}_{\mathbf{x},\mathbf{y}}[\mathbf{x}\mathbf{y}^\mathrm{T}]-\mathbb{E}[\mathbf{x}]\mathbb{E}[\mathbf{y}^\mathrm{T}]$$

$$\mathrm{cov}[\mathbf{x}]\equiv\mathrm{cov}[\mathbf{x,x}]$$

#### Bayesian Probabilities

Quantify the uncertainty that surrounds the appropriate choice for the model parameters $\mathbf{w}$.

$$\mathrm{posterior\propto likelihood\times prior}$$

$$p(\mathbf{w}|\mathcal{D})=\frac{p(\mathcal{D}|\mathbf{w})p(\mathbf{w})}{p(\mathcal{D})}$$

$$p(\mathcal{D})=\int p(\mathcal{D}|\mathbf{w})p(\mathbf{w})\mathrm{d}\mathbf{w}$$

#### Data $\mathcal{D}$  

#### Parameter $\mathbf{w}$  

#### Likelihood Function

 $$p(\mathcal{D}|\mathbf{w})=f(\mathbf{w})$$

 It expresses how probable the observed data set is for different settings of the parameter vector $\mathbf{w}$.

#### Estimator: Maximum Likelihood

Set $\mathbf{w}$ to make $p(\mathcal{D}\|\mathbf{w})$ maximum.

#### Error Function

 $$-\log(p(\mathcal{D}|\mathbf{w}))$$

#### Decision Theory

Minimizing the misclassification rate.

##### Class $\mathcal{C}_k$  

##### Decision Region $\mathcal{R}_k$  

##### Decision Boundaries / Decision Surfaces

## Permutation and Combination

$$0!=1$$

$$A_n^m=\frac{n!}{(n-m)!}$$

$$C_n^m=\frac{n!}{m!(n-m)!}$$
