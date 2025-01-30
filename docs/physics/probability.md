---
layout: math
---
# Probability

"Probability" of a particular outcome of an observation we mean our estimate for the most likely fraction of a number of repeated observations that will yield that particular outcome.

1. A probability of something happening only if the occurrence is a possible outcome of some repeatable observation.
2. $N_A$ is our best estimate of what would occur in $N$ imagined observations.

$$
P(A) = N_A/N
$$


杨辉三角 / Pascal's Triangle -- binominal coefficient:

$$
(^n_k)= \frac{n!}{k!(n-k)!}
$$

$$
n!=(n)(n-1)(n-2)...(3)(2)(1)
$$

$$
P(k,n) = \frac{(^n_k)}{2^n}
$$

Bernoulli / binomial probability:

$$
P(k,n) = (^n_k)p^kq^{n-k}
$$


## Random walk

Expected value / mean square distance

$$
\langle D^2_N \rangle = N
$$

Root-mean-square distance

$$
D_\text{rms} = \sqrt{\langle D^2_N \rangle} = \sqrt{N}
$$

Root-mean-square deviation (of steps in one direction)

$$
(N_\text{H}-\frac{N}{2})_\text{rms} = \frac{D_\text{rms}}{2} = \frac{1}{2}\sqrt{N}
$$

Probability with fluctuation

$$
P(H) = \frac{N_\text{H} \pm \frac{1}{2}\sqrt{N}}{N}
= \frac{N_\text{H}}{N} \pm \frac{1}{2\sqrt{N}}
$$

depend on
1. disrriburion of individual steps
2. N, the number of steps taken

## A probability distribution

Probability distribution

$$
P(x,\Delta x) = p(x)\Delta x
$$

$$
P(x_1<D<x_2) = \sum p(x)\Delta x = \int^{x_2}_{x_1} p(x)dx
$$

$$
\int^{+\infty}_{-\infty}p(x)dx=1
$$

Normal/gaussian probability density
$$
p(x) = \frac{1}{\sigma \sqrt{2\pi}}e^{-x^2/2\sigma^2}
$$

standard deviation
$$
\sigma = \sqrt{N}S_\text{rms}
$$

## Heisenberg uncertainty

$$
[\Delta x][\Delta v] \ge h/m
$$