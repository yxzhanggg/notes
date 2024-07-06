---
layout: base
title: Probability & Statistics
parent: Linear Algebra
nav_order: 10
---

#### mean

the average value or expected value

![image-20220718161202937](https://s2.loli.net/2022/07/18/FjPegLlU3Gw5cMz.png)

#### expected value

![image-20220718161231843](https://s2.loli.net/2022/07/18/vnoXGHb1htImWyV.png)

#### variance $\sigma^2$

measures the average squared distance from the mean $m$

measures expected distance (squared) from the expected mean $E[x]$.

![image-20220718164800455](https://s2.loli.net/2022/07/18/MkHAFQyi4KoGn7h.png)

#### sample variance $S^2$

measures actual distance (squared) from the sample mean.

![image-20220718163639529](https://s2.loli.net/2022/07/18/vBPaRDLCMxE7ef1.png)

![image-20220718164848937](https://s2.loli.net/2022/07/18/V4dlGD3w2hEcTji.png)

#### standard deviation $\sigma$ or $S$

#### probabilities of $n$ different outcomes

positive numbers $p_1, ... , P_n$ adding to 1.

#### sample values, expected values

#### Law of Large Numbers 

With probability 1, the sample mean will converge to its expected value $E[x]$ as the sample size $N$ increases.

# Continuous

![image-20220718185436799](https://s2.loli.net/2022/07/19/MHibgUXS8ZYupdJ.png)

![image-20220718185451724](https://s2.loli.net/2022/07/19/kt4iPCvhqjZ2Npl.png)

#### Uniform distribution

![image-20220718191045340](https://s2.loli.net/2022/07/19/FA1xZsCvtHSmzXd.png)

#### Normal distribution

![image-20220718193120705](https://s2.loli.net/2022/07/19/HYfPLGi9q4a7U3X.png)

![image-20220718193206143](https://s2.loli.net/2022/07/19/OsWw6LNgvpm2Una.png)

![image-20220718194447755](https://s2.loli.net/2022/07/19/ePgEBpdNcjDSoy4.png)

![image-20220718195011328](https://s2.loli.net/2022/07/19/Rw8QixcN9WHyzlI.png)

![image-20220718195635439](https://s2.loli.net/2022/07/19/2nZajTqUYK6hMct.png)

![image-20220718195814858](https://s2.loli.net/2022/07/19/F2dcm4EQRVSJ7bM.png)

![image-20220718201456754](https://s2.loli.net/2022/07/19/olQKmYNfF3jbOgJ.png)

![image-20220718202207497](https://s2.loli.net/2022/07/19/odu2E1gR8QBmb5j.png)

#### Monte Carlo Estimation Methods

accepting uncertainty in the inputs and estimating the variance in the outputs.

try different inputs $b$ and compute the outputs $x$ and take an average.

Monte Carlo approximates an expected value $E[x]$ by a sample average $(x_1 + · · · +x_N )/ N$.

![image-20220718213030484](https://s2.loli.net/2022/07/19/YcNnMeGKk31ZlHF.png)

#### Covariance

![image-20220718223449475](https://s2.loli.net/2022/07/19/WVA2YB1UCzsGcjQ.png)

![image-20220718223505780](https://s2.loli.net/2022/07/19/dAWzNnH6bfes7Ra.png)

![image-20220718223658835](https://s2.loli.net/2022/07/19/t6kgyAaQVXWUuRE.png)

![image-20220718224705394](https://s2.loli.net/2022/07/19/Y69xuFqEgDXwayB.png)

![image-20220719083623710](https://s2.loli.net/2022/07/19/1BlK5RV38uidT6c.png)

Diagonalizing the covariance matrix means finding $M$ independent experiments as combinations of the original $M$ experiments.

#### "whitening" the noise:

![image-20220719084106817](https://s2.loli.net/2022/07/19/RVEOKvk9c4XhJ8p.png)

#### Kalman Filter

dynamic: new measurements $b_k$ keep coming. 

matrix $A$ is also changing.

recursive least squares: adding new data $b_k$ and updating both $\hat{x}$ and $W$.

![image-20220719084809771](https://s2.loli.net/2022/07/19/xviK2uljR6EVySn.png)

![image-20220719084817405](https://s2.loli.net/2022/07/19/H6MRAsmwFaQ12xh.png)

![image-20220719084827527](https://s2.loli.net/2022/07/19/t4JmUFZo5wNCO9r.png)

![image-20220719084841455](https://s2.loli.net/2022/07/19/QcYi4VaDXfRZ1dK.png)
