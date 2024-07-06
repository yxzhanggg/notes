---
layout: default
title: Logic
parent: Fundamentals
nav_order: 1
---

Reference:

- [mathematics for computer science - MIT opencourseware](https://ocw.mit.edu/courses/6-042j-mathematics-for-computer-science-fall-2010/)
- ![Screen Shot 2022-07-13 at 11.41.40 AM](https://live.staticflickr.com/65535/52212278217_481e447149_o.png)

---

# Proofs

## Logics

#### Propositions

A proposition is a statement that is either true or false.

#### Boolean variables

 $\mathbf{T}$ (true) and $\mathbf{F}$ (false)

#### Truth tables

**Compound propositions**

|              English              |     Symbolic Notation     |
| :-------------------------------: | :-----------------------: |
|      $\operatorname{NOT}(P)$      |    $\neg P / \bar{P}$     |
|        $P \text { AND } Q$        |       $P \wedge Q$        |
|        $P \text { OR } Q$         |        $ P \vee Q$        |
|      $P \text { IMPLIES } Q$      |   $P \longrightarrow Q$   |
| $\text { if } P \text { then } Q$ |   $P \longrightarrow Q$   |
|        $P \text { IFF } Q$        | $P \longleftrightarrow Q$ |

**NOT**


| $P$  | $\operatorname{NOT}(P)$ |
| :--: | :---------------------: |
|  T   |            F            |
|  F   |            T            |

**AND**

| $P$  | $Q$  | $P\operatorname{AND}Q$ |
| :--: | :--: | :--------------------: |
|  T   |  T   |           T            |
|  T   |  F   |           F            |
|  F   |  T   |           F            |
|  F   |  F   |           F            |

**OR**

| $P$  | $Q$  | $P\operatorname{OR}Q$ |
| :--: | :--: | :-------------------: |
|  T   |  T   |           T           |
|  T   |  F   |           T           |
|  F   |  T   |           T           |
|  F   |  F   |           F           |

**EXCLUSIVE-OR**

| $P$  | $Q$  | $P\operatorname{XOR}Q$ |
| :--: | :--: | :--------------------: |
|  T   |  T   |           F            |
|  T   |  F   |           T            |
|  F   |  T   |           T            |
|  F   |  F   |           F            |

**IMPLIES** An implication is true exactly when the if-part is false or the then-part is true.

| $P$  | $Q$  | $P\operatorname{IMPLIES}Q$ |
| :--: | :--: | :------------------------: |
|  T   |  T   |             T              |
|  T   |  F   |             F              |
|  F   |  T   |             T              |
|  F   |  F   |             T              |

**IF AND ONLY IF**

| $P$  | $Q$  | $P\operatorname{IFF}Q$ |
| :--: | :--: | :--------------------: |
|  T   |  T   |           T            |
|  T   |  F   |           F            |
|  F   |  T   |           F            |
|  F   |  F   |           T            |

**Contrapositive** Logically equivalent implications

**Converse**

| $P$  | $Q$  | $P\operatorname{IMPLIES}Q$ | $Q\operatorname{IMPLIES}P$ |
| :--: | :--: | :------------------------: | :------------------------: |
|  T   |  T   |             T              |             T              |
|  T   |  F   |             F              |             T              |
|  F   |  T   |             T              |             F              |
|  F   |  F   |             T              |             T              |

#### Predicates

A predicate is a proposition whose truth depends on the value of one or more variables.

#### Quantiﬁers

- **Universally quantiﬁed statement** $\forall x \in D . P(x)$ An assertion that a predicate is always true

- **Existentially quantiﬁed statement** $\exists x \in D . P(x)$ An assertion that a predicate is sometimes true

#### Order of quantiﬁers

Swapping the order of different kinds of quantiﬁers (existential or universal) usually changes the meaning of a proposition.

#### Domain of discourse / plain domain of the formula

The unnamed nonempty set that $x$ and $y$ range over: When all the variables in a formula are understood to take values from the same nonempty set, $D$, $\forall x \in D \exists y \in D . Q(x, y)$, we'd write $\forall x \exists y . Q(x, y)$.

#### Negating quantiﬁers

$$\operatorname{NOT}(\exists x . P(x))\operatorname{IFF}\forall x . \operatorname{NOT}(P(x))$$

Moving a “not” across a quantiﬁer changes the kind of quantiﬁer.

#### Validity

 A propositional formula is called valid when it evaluates to $\mathbf{T}$ no matter what truth values are assigned to the individual propositional variables.

#### Satisﬁability

 A proposition is satisﬁable if some setting of the variables makes the proposition true.

#### SAT

 The general problem of deciding whether a proposition is satisﬁable is called SAT.

#### “P vs. NP” problem

## Patterns of Proof

#### Axioms

Propositions that are simply accepted as true.

#### Proof

A proof is a sequence of logical deductions from axioms and previously-proved statements that concludes with the proposition in question.

#### Theorems

Important propositions.

#### Lemma

A lemma is a preliminary proposition useful for proving later propositions.

#### Corollary

A corollary is a proposition that follows in just a few logical steps from a lemma or a theorem.

#### Axiomatic method

Euclid’s axiom-and-proof approach

#### Zermelo-Frankel Set Theory with Choice (ZFC)

- **Extensionality** Two sets are equal if they have the same members.

- **Pairing** For any two sets $x$ and $y$, there is a set, $\{x, y\}$, with $x$ and $y$ as its only elements.

- **Union** The union, $u$, of a collection, $z$, of sets is also a set.

- **Inﬁnity** There is an inﬁnite set.

- **Subset** Given any set, $x$, and any proposition $P(y)$, there is a set containing precisely those elements $y\in x$ for which $P(y)$ holds.
- **Power Set** All the subsets of a set form another set: $\forall x . \exists p . \forall u . u \subseteq x \text { IFF } u \in p$.

- **Replacement** Suppose a formula, $\phi$, of set theory deﬁnes the graph of a function, that is, $\forall x, y, z \cdot[\phi(x, y) \text { AND } \phi(x, z)] \text { IMPLIES } y=z$ . Then the image of any set, $s$, under that function is also a set, $t$. Namely, $\forall s \exists t \forall y \cdot[\exists x . \phi(x, y) \text { IFF } y \in t]$.

- **Foundation** Every nonempty set has a “member-minimal” element. $\operatorname{member}-\operatorname{minimal}(m, x)::=[m \in x \operatorname{AND} \forall y \in x, y \notin m]$ $\forall x . x \neq \emptyset \text { IMPLIES } \exists m . \text { member-minimal }(m, x) .$
- **Choice** Given a set, $s$, whose members are nonempty sets no two of which have any element in common, then there is a set, $c$, consisting of exactly one element from each set in $s$.

#### Logical deductions / inference rules

 Logical deductions or inference rules are used to prove new propositions using previously proved ones.

#### modus ponens

This rule says that a proof of $P$ together with a proof that $P\operatorname{IMPLIES}Q$ is a proof of $Q$.

$$\frac{P, \quad P \text { IMPLIES } Q}{Q}$$

$$\frac{antecedents}{conclusion/consequent}$$

#### Set builder notation

 To deﬁne a set using a predicate.

## Induction

#### The Well Ordering Principle

Every nonempty set of nonnegative integers has a smallest element.

#### Ordinary Induction

$$\frac{P(0), \, \forall n \in \mathbb{N} . P(n) \text { IMPLIES } P(n+1)}{\forall m \in \mathbb{N} . P(m)}$$

#### Invariants

A property that is preserved through a series of operations or steps is known as an invariant.

#### Strong Induction

$$\frac{P(0), \, \forall n \in \mathbb{N} .(P(0) \text { AND } P(1) \text { AND ... AND } P(m)) \text { IMPLIES } P(n+1)]}{\forall m \in \mathbb{N} . P(m)}$$

#### Recursive data types

They are speciﬁed by recursive deﬁnitions that say how to build something from its parts.

#### Recursive definitions

- Base case(s) that don't depend on anything else.

- Constructor case(s) that depend on previous cases.

#### Structural Induction

Structural induction is a method for proving that some property, $P$, holds for all the elements of a recursively-deﬁned data type.

- Prove $P$ for the base cases of the deﬁnition.
- Prove $P$ for the constructor cases of the deﬁnition, assuming that it is true for the component data item

#### Functions

A function assigns an element of one set, called the domain, to elements of another set, called the codomain.

#### Ambiguity

When a recursive deﬁnition of a data type allows the same element to be constructed in more than one way, the deﬁnition is said to be ambiguous.

## Number Theory

Number theory is the study of the integers.

#### Divisibility

If $a \| b$, then we also say that b is a multiple of a.

#### Greatest common divisor

The largest number that is a divisor of both $a$ and $b$.

#### Euclid’s Algorithm

$$\mathrm{gcd}(a,b)=\mathrm{gcd}(b,\mathrm{rem}(a,b,))$$

#### Fundamental Theorem of Arithmetic

Every positive integer n can be written in a unique way as a product of primes.

#### The Prime Number Theorem

Let $\pi(x)$ denote the number of primes less than or equal to $x$.

 $$\lim _{x \rightarrow \infty} \frac{\pi(x)}{x / \ln x}=1$$

As a rule of thumb, about 1 integer out of every ln x in the vicinity of x is a prime.

#### Fermat’s Little Theorem

Suppose $p$ is a prime and $k$ is not a multiple of $p$. Then: $k^{p-1}\equiv 1 \ (\mod{p})$

#### Riemann Hypothesis

Every nontrivial zero of the zeta function $\xi(s)$ lies on the line $s=1/2+ci$ in the complex plane.

# Structure

## Graph Theory

## Relations and Partial Orders

#### Relation

A **relation** is a mathematical tool for describing associations between elements of sets.

#### Image

The image of a set $Y$ under a relation $R:A\rightarrow B$, written $R(Y)$, is the set of elements that are related to some element in $Y$.

#### Surjective

If every element of B is assigned to at least one element of A.

#### Total

when every element of A is assigned to some element of B.

#### Injective

If every element of B is mapped at most once

#### Bijective

If R is total, surjective, injective, and a function

