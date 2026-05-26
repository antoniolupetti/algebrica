---
title: Sequences
source: https://algebrica.org/sequences/
license: CC BY-NC 4.0
tags:
  - fibonacci-sequence
  - monotone-sequence
  - recursive-sequence
  - sequence
  - term
---

## What is a sequence 

A sequence is an ordered collection of elements, each assigned to a specific position indexed by a [natural number](../natural-numbers/). Let us consider the set of real numbers $\mathbb{R}$. A sequence with values in $\mathbb{R}$ is a function of the form $\mathbb{N} \rightarrow \mathbb{R}$, that assigns to each $n \in \mathbb{N}$ a unique real number $a(n) \in \mathbb{R}$.
 
+ A sequence $a : \mathbb{N} \rightarrow \mathbb{R}$ is denoted by $\lbrace a_n \rbrace_{n \in \mathbb{N}}.$
+ Each element produced by the sequence is known as a term.
+ The expression for $a_n$ defines the rule that determines every term of the sequence.

It is often useful to consider sequences defined only on a subset of natural numbers, such as those starting from a specific [integer](../integers/) value. These are sequences of the form:

$$
a : \{n \in \mathbb{N} : n \geq n_0\} \to \mathbb{R}.
$$

This means the sequence is defined for all natural numbers greater than or equal to some initial index $n_0$.

- - -
Consider, for example, the [function](../functions/) $a: \mathbb{N}^+ \to \mathbb{R}$ defined by $a(n) := \dfrac{1}{n}$. This is a real-valued sequence defined for every $n \in \mathbb{N}^+$, and its terms are:

$$
a_1 = 1, \quad a_2 = \frac{1}{2}, \quad \dots, \quad a_n = \frac{1}{n} \quad \forall n \in \mathbb{N}^+.
$$

- - -
Another example of a sequence is $a_n = n!$, the [factorial](../factorial/) of $n$, which is defined as the product of all positive integers from 1 to $n$. The first few terms of the sequence are:

$$
a_1 = 1, \quad a_2 = 2, \quad a_3 = 6, \quad a_4 = 24, \quad a_5 = 120, \quad \dots
$$

## Example 

Consider, for example, the formula:

$$
a_n := \frac{1}{n - 2}
$$
  
defines a real-valued sequence $a : \{3, 4, 5, \dots\} \to \mathbb{R}$, where the values $3, 4, 5, \dots$ represent the indices of the sequence. Indeed, since the denominator becomes zero for $n = 2$, the term $a_2$ is undefined. To avoid this singularity, we restrict the [domain](../determining-the-domain-of-a-function/) to $n \geq 3$. In this case, we write the sequence as:

$$
(a_n)_{n \geq 3} = \left( \frac{1}{n - 2} \right)_{n \geq 3}
$$

The first few terms of the sequence are:

$$
a_3 = 1, \quad a_4 = \frac{1}{2}, \quad a_5 = \frac{1}{3}, \quad a_6 = \frac{1}{4}, \quad a_7 = \frac{1}{5}, \ \dots
$$

As we can see, this sequence decreases and converges to zero as $n \to \infty$ (we will see later what this means).

## Recursively defined sequences

A recursive sequence is a sequence where each term is defined in terms of one or more of the preceding terms. To define such a sequence, two components are needed:

+ An initial value.
+ A recurrence relation, which determines how to compute each new term.

One of the most famous recursive sequences is the Fibonacci sequence, defined as:

$$
\begin{cases}
a_0 = 0, \\[0.5em]
a_1 = 1, \\[0.5em]
a_n = a_{n-1} + a_{n-2} \quad \text{for all } n \geq 2
\end{cases}
$$

This means that every term is the sum of the two preceding ones. The first few terms of the sequence are:

$$
\begin{aligned}
a_0 &= 0 \\[0.5em]
a_1 &= 1 \\[0.5em]
a_2 &= 1 \\[0.5em]
a_3 &= 2 \\[0.5em]
a_4 &= 3 \\[0.5em]
a_5 &= 5 \\[0.5em]
a_6 &= 8 \\[0.5em]
&\vdots
\end{aligned}
$$


> Recursion is a common strategy in programming that allows complex tasks to be solved by repeatedly applying the same rule until a base case is reached. It's especially effective for generating sequences and solving problems with a self-repeating structure.

## Monotonic sequences

A sequence can be classified based on how its terms evolve. In general, a sequence that satisfies any of these conditions is called a [monotonic sequence](../monotone-sequences/):

+ Constant: if every term is equal to the previous one: $a_n = a_{n+1} \quad \forall n \in \mathbb{N}$.

+ Increasing: if each term is greater than the previous one: $a_n < a_{n+1} \quad \forall n \in \mathbb{N}$.

 + Decreasing: if each term is less than the previous one: $a_n > a_{n+1} \quad \forall n \in \mathbb{N}$.

+ Non-decreasing: $a_n \leq a_{n+1} \quad \forall n \in \mathbb{N}$.

+ Non-increasing: $a_n \geq a_{n+1} \quad \forall n \in \mathbb{N}$.

**Theorem 1.** If a sequence $(a_n)_{n \in \mathbb{N}}$ is monotonic and bounded, then it admits a finite [limit](../convergent-and-divergent-sequences/). 

**Theorem 2.** If the sequence is monotonic but unbounded, then it diverges to $+\infty$ or to $-\infty$ depending on the direction of monotonicity. In the bounded case the limit is determined by the [supremum or infimum](../supremum-and-infimum/) of the range of the sequence:

$$
\lim_{n \to +\infty} a_n =
\begin{cases}
\sup \{ a_n : n \in \mathbb{N} \} & \text{if } (a_n)_{n \in \mathbb{N}} \text{ is increasing} \\[0.5em]
\inf \{ a_n : n \in \mathbb{N} \} & \text{if } (a_n)_{n \in \mathbb{N}} \text{ is decreasing}
\end{cases}
$$

This result guarantees that bounded monotonic sequences always converge, and their limit corresponds to the supremum or infimum depending on the direction of monotonicity. The dedicated page on [monotone sequences](../monotone-sequences/) develops the proof of the theorem and treats the unbounded case in detail.

## Cauchy sequences

A different way of describing the behaviour of a sequence focuses on the mutual distance between its terms rather than on the existence of a fixed limit. A sequence whose terms get arbitrarily close to one another from a certain index onward is called a [Cauchy sequence](../cauchy-sequence/). 

In $\mathbb{R}$ every Cauchy sequence converges, and conversely every convergent sequence is a Cauchy sequence: this equivalence is the structural completeness of the real line, and it distinguishes $\mathbb{R}$ from the field of rational numbers.

## Special sequences and further developments

Among the most important classes of sequences are the [arithmetic sequences](../arithmetic-sequence/), whose terms differ by a constant amount, and the [geometric sequences](../geometric-sequence/), whose terms are linked by a constant ratio. Their behaviour and the closed-form expression for the sum of the first $n$ terms are treated in the dedicated pages.

When the rule that generates each term yields a [function](../functions/) rather than a number, the resulting object is a [sequence of functions](../sequence-of-functions/), whose convergence is studied in pointwise and uniform form. 

The limit $e := \lim_{n \to \infty}(1 + 1/n)^n$ provides a celebrated example of a monotone bounded sequence and is discussed on the page about [Euler's number](../euler-number-limit-sequence/). Many properties of sequences are most efficiently established by the [principle of mathematical induction](../principle-of-mathematical-induction/), which applies whenever a statement is parametrised by a natural number.

For sequences that do not converge but remain bounded, such as oscillating sequences, the ordinary limit does not exist. The [superior and inferior limits](../superior-and-inferior-limits-of-a-sequence/) extend the analysis to this case, identifying the largest and smallest cluster values around which the terms accumulate for arbitrarily large indices.

