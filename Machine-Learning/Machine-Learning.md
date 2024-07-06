---
layout: base
title: Machine Learning
nav_order: 7
has_children: true
permalink: /docs/Machine-Learning
---

Machine learning is still nothing greater that Hash table. Most of the concepts are renamed from the classical concepts, which likes the result of commercial bidding, for example, the activation function is actually the system function, and hypothesis is the system response. And the name neural network is just connected function compositions, to say more rigorously, transformation network. So it is just a fancy technique which distorted some concepts in the classical mathematics. If you want establish your great building of mathematics, then do not touch machine learning first!

# Best article to understand machine learning 

http://staff.ustc.edu.cn/~lgliu/Resources/DL/What_is_DeepLearning.html

"Machine learning is the generalization of approximation theory"

"Neural network is a nonlinear-to-linear projector"

fitting-eigen-fitter-eigen-fitting-eigen-...

the layers are multiple transformations and projections between different spaces.

parameterization the transformations.

---

Reference: 

- [Book: Goodfellow, Bengio, Courville (2016). Deep Learning. MIT Press.](https://www.deeplearningbook.org)
- [Bishop (2006). Pattern Recognition and Machine Learning. Springer, Cambridge, UK.](https://www.microsoft.com/en-us/research/uploads/prod/2006/01/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf)

![image-20220801085921335](https://s2.loli.net/2022/08/01/CuqP2Ec3mWz7F1h.png)

---

**Arthur Samuel (1959).** Machine Learning: Field of study that gives computers the ability to learn without being explicitly programmed.

**Tom Mitchell (1998).** Well-posed Learning Problem: A computer program is said to learn from experience $E$ with respect to some task $T$ and some performance measure $P$, if its performance on $T$, as measured by $\mathrm{P}$, improves with experience $E$.

---

- Supervised learning - regression

- Unsupervised learning

---

# Basics

#### Bias

 A preference or inclination for or against something

#### Prejudice

An assumption made without adequate knowledge

#### Discrimination

The actions taken based on a prejudice

#### Fairness

The absence of bias or discrimination on specific realms

#### Linear classiﬁers

 Linear hyperplanes in feature space that partition the space in (two) classes

#### Task $T$

How machine process examples with features. i.e. vector  (example) $\mathbf{x}\in\mathbb{R}^n$ with entry (feature) $\mathbf{x}_i$.

##### Classification

$$f:\mathbb{R}^n\rightarrow\{1,...,k\}$$

##### Classification with Missing Inputs

##### Regression

$$f:\mathbb{R}^n\rightarrow\mathbb{R}$$

##### Transcription

Transcribe unstructured information into discrete textual form. i.e. optical character recognition.

##### Machine Translation

Convert a sequence of symbols of some language into another language. i.e. English to French.

##### Structured Output

Output several values that are all tightly interrelated. i.e. vector, tree.

##### Anomaly Detaction

Sifting and find.

##### Synthesis and Sampling

Generate new similar data.

##### Imputation of Missing Values

Example $\mathbf{x}\in\mathbb{R}^n$ with some entries $\mathbf{x}_i$ of $\mathbf{x}$ missing.

##### Denoising

Corrupted example $\tilde{\mathbf{x}}\in\mathbb{R}^n$ from a clean example $\mathbf{x}\in\mathbb{R}^n$, predict $\mathbf{x}$ from $\tilde{\mathbf{x}}$ or conditional probability distribution $P(\mathbf{x}\|\tilde{\mathbf{x}})$.

##### Density Estimation / Probability Mass Function Estimation

Probability density/mass($x$ continuous/discrete) function $p_{model}:\mathbb{R}^n\rightarrow\mathbb{R}$.

#### Performance Measure $P$

Specific to the task $T$ being carried out by the system.

##### Accuracy 

The proportion of examples for which the model produces the correct output.

##### Error rate

The proportion of of examples for which the model produces the incorrect output. For task as Classification, Classification with missing input, and Transcription.

##### 0-1 loss

##### Average Log-probability

##### Test set

Being separated from data to measure the performance on data that ML algorithm has not seen before.

#### Experience $E$

Machine learning algorithm can be categorized as **unsupervised / supervised** by what kind of experience they are allowed to have during the learning process.

##### Dataset

Collections of data points (examples).

##### Designed matrix

row - example; column - feature.

##### Unsupervised(uninstructed) Learning Algorithm - Finding Properties

Experience a dataset containing many features, then learn useful property of the structure of the dataset. i.e. clustering.

##### Supervised(instructed) Learning Algorithm - Associating  $p(\mathbf{y}\|\textbf{x})$ for Predicting $\mathbf{y}$:

Experience a dataset containing structured features label/target).

##### Simi-supervised learning algorithm

Some examples include a supervision target but others do not.

##### Multi-instance Learning

##### Reinforcement Learning Algorithm

Interact with an environment but not a fixed dataset - feedback loop.
