---
title: Superior and Inferior Limits of a Sequence
source: https://algebrica.org/superior-and-inferior-limits-of-a-sequence/
license: CC BY-NC 4.0
tags:
  - accumulation-point
  - bounded-sequence
  - convergent-sequence
  - limit-inferior
  - limit-of-a-sequence
  - limit-superior
  - sequence
---

## Introduction

The [supremum and infimum](../supremum-and-infimum/) of the range of a [sequence](../sequences/) describe how its terms are positioned globally, but they say nothing about the long-term behavior. The sequence $a_n = (-1)^n$ has supremum $1$ and infimum $-1$, and these values are attained again and again as $n$ grows, yet the sequence does not [converge](../convergent-and-divergent-sequences/). 

At the other extreme, the sequence $a_n = 1/n$ has supremum $1$, which is attained only once, while every subsequent term lies arbitrarily close to $0$. The supremum of the range is therefore misleading as a description of the eventual behavior.

A more refined construction is required, one that records the values around which the terms cluster for arbitrarily larg

e indices, and discards the contribution of any finite initial segment. The limit superior and limit inferior provide such a construction. They are defined for every sequence of [real numbers](../real-numbers/), they always exist in the extended real line $[-\infty, +\infty]$, and they coincide exactly when the sequence converges. For sequences that fail to converge but remain bounded, they capture the two extremal cluster values between which the terms oscillate.

## Definition via nested suprema and infima

**Definition 1.** Let $(a_n)_{n \in \mathbb{N}}$ be a sequence of real numbers. For each index $n$, consider the tail of the sequence starting from position $n$, and form its supremum and its infimum.

$$
M_n = \sup_{k \geq n} a_k, \qquad m_n = \inf_{k \geq n} a_k
$$

Each $M_n$ is a real number when the sequence is bounded above, and equals $+\infty$ otherwise; similarly for $m_n$. As the index $n$ increases, the tail shrinks: the set $\\{a_k : k \geq n+1\\}$ is contained in $\\{a_k : k \geq n\\}$. Taking the supremum over a smaller set cannot produce a larger value, so the sequence $(M_n)$ is non-increasing. By the same reasoning, $(m_n)$ is non-decreasing.

A monotone sequence in the extended real line always admits a limit, possibly equal to $\pm\infty$. The [monotone convergence theorem](../monotone-sequences/) identifies these limits explicitly, and we set:

$$
\limsup_{n \to \infty} a_n = \lim_{n \to \infty} M_n = \inf_{n \in \mathbb{N}} M_n
$$

$$
\liminf_{n \to \infty} a_n = \lim_{n \to \infty} m_n = \sup_{n \in \mathbb{N}} m_n
$$

The limit superior is the infimum of the non-increasing sequence of tail-suprema, and the limit inferior is the supremum of the non-decreasing sequence of tail-infima. Both quantities are defined for every sequence of real numbers, with values in $[-\infty, +\infty]$.

> The interpretation is the following. The tail-supremum $M_n$ measures how high the sequence can still go after position $n$. As $n$ grows, the early outliers are discarded, and $M_n$ approaches the largest value around which the terms continue to accumulate. The tail-infimum $m_n$ plays the symmetric role from below.

## Worked examples

Consider first the oscillating sequence $a_n = (-1)^n$, whose terms alternate between $+1$ and $-1$. For every index $n$, the tail $\\{a_k : k \geq n\\}$ contains both $+1$ and $-1$, so the supremum of the tail is always $+1$ and the infimum is always $-1$.

$$
M_n = 1, \qquad m_n = -1 \qquad \forall n \in \mathbb{N}
$$

Both sequences are constant, and their limits are immediate.

$$
\limsup_{n \to \infty} (-1)^n = 1, \qquad \liminf_{n \to \infty} (-1)^n = -1
$$

The two quantities differ, in agreement with the fact that the sequence does not converge.

- - -

Consider next the sequence defined by the following expression:

$$
a_n = (-1)^n + \frac{1}{n}
$$

The terms alternate in sign while drifting toward $\pm 1$. The even-indexed terms form the subsequence $1 + 1/(2k)$, which decreases toward $1$ from above. The odd-indexed terms form the subsequence $-1 + 1/(2k+1)$, which increases toward $-1$ from above. For every index $n$, the tail contains even-indexed terms greater than $1$, so $M_n > 1$, and the tail-supremum is attained by the smallest even index $k \geq n$.

$$
M_n = 1 + \frac{1}{k_n^{\text{even}}}, \qquad k_n^{\text{even}} = \min\\{k \geq n : k \text{ even}\\}
$$

As $n \to \infty$, the index $k_n^{\text{even}}$ also tends to infinity, and $M_n \to 1$. A symmetric argument applies to the tail-infimum: the most negative term in the tail is the odd-indexed term with the smallest index, and $m_n \to -1$.

$$
\limsup_{n \to \infty} \left( (-1)^n + \frac{1}{n} \right) = 1, \qquad \liminf_{n \to \infty} \left( (-1)^n + \frac{1}{n} \right) = -1
$$

The example shows how the perturbation $1/n$ leaves the limit superior and limit inferior unchanged compared with the bare oscillation $(-1)^n$. Adding an [infinitesimal](../convergent-and-divergent-sequences/) sequence to a bounded sequence shifts its cluster values by zero.

- - -

A third example brings out a different feature. Consider the sequence:

$$
a_n = \sin\left( \frac{n\pi}{2} \right)
$$

The values cycle through $0, 1, 0, -1$ as $n$ runs through $0, 1, 2, 3$, and then repeat with period four. Every tail contains all four values, so:

$$
M_n = 1, \qquad m_n = -1 \qquad \forall n \in \mathbb{N}
$$

and consequently $\limsup a_n = 1$, $\liminf a_n = -1$. The value $0$, which appears infinitely often in the sequence, lies strictly between the limit inferior and the limit superior. This is consistent with the characterization developed below: $0$ is an accumulation point of the sequence, but neither the largest nor the smallest.

## Characterization via accumulation points

**Definition 2.** A real number $\ell$ is called an accumulation point of the sequence $(a_n)$ if there exists a subsequence $(a_{n_k})$ such that $a_{n_k} \to \ell$. 

The set of accumulation points of a sequence may contain a single point (when the sequence converges), finitely many points (as in the example $a_n = \sin(n\pi/2)$, whose accumulation points are exactly $-1, 0, 1$), or even an uncountable family. The values $\pm\infty$ are admitted as accumulation points when the sequence has subsequences diverging to $\pm\infty$.

**Theorem 1.** Let $(a_n)$ be a sequence of real numbers. The limit superior is the largest accumulation point of $(a_n)$ in $[-\infty, +\infty]$, and the limit inferior is the smallest.

The proof requires two steps for each quantity: the limit superior is itself an accumulation point, and no accumulation point exceeds it. We argue the first step assuming $L = \limsup a_n$ is finite. The cases $L = \pm\infty$ are analogous and slightly simpler.

By definition, $M_n \to L$, so for every $\varepsilon > 0$ there exists $N$ such that $L - \varepsilon < M_n < L + \varepsilon$ for all $n \geq N$. The inequality $M_n > L - \varepsilon$ means that the tail starting at $n$ contains a term strictly greater than $L - \varepsilon$, and the inequality $M_n < L + \varepsilon$ means that every term of that tail is at most $L + \varepsilon$ (more precisely, strictly less than $L + \varepsilon$ except possibly equal to $M_n$ when the supremum is attained). 

One can therefore extract a subsequence of indices $n_1 < n_2 < \cdots$ such that $|a_{n_k} - L| < 1/k$, by choosing at each step a sufficiently advanced tail and a term in that tail close to its supremum. The constructed subsequence converges to $L$, so $L$ is an accumulation point.

For the second step, suppose $\ell$ is an accumulation point with $\ell > L$. Choose $\varepsilon = (\ell - L)/2 > 0$. Convergence of $M_n$ to $L$ gives an index $N$ such that $M_n < L + \varepsilon = \ell - \varepsilon$ for every $n \geq N$. In particular, every term $a_k$ with $k \geq N$ satisfies $a_k \leq M_N < \ell - \varepsilon$, contradicting the existence of a subsequence converging to $\ell$. No accumulation point can exceed $L$.

The argument for $\liminf$ is symmetric. Limits inferior and superior therefore bracket all accumulation points of the sequence, and they themselves belong to that set.

> The theorem provides an alternative definition of $\limsup$ and $\liminf$ in terms of subsequential limits. Both formulations are equivalent and each illuminates a different aspect: the tail-supremum construction is constructive and easy to compute in concrete cases, while the accumulation-point characterization is conceptually closer to the meaning of these quantities.

## The convergence criterion

The relationship between $\limsup$, $\liminf$, and the ordinary limit is captured by the following statement, which is one of the most useful applications of the construction.

**Theorem 2.** Let $(a_n)$ be a sequence of real numbers and let $\ell \in \mathbb{R}$. Then $a_n \to \ell$ if and only if:

$$
\limsup_{n \to \infty} a_n = \liminf_{n \to \infty} a_n = \ell
$$

We prove both implications. Suppose first that $a_n \to \ell$. Every subsequence of a convergent sequence also converges, to the same limit, so the only accumulation point of $(a_n)$ is $\ell$. By Theorem 1, $\limsup a_n = \liminf a_n = \ell$.

Conversely, suppose $\limsup a_n = \liminf a_n = \ell$, with $\ell$ a finite real number. From the definitions:

$$
M_n \to \ell, \qquad m_n \to \ell
$$

Fix $\varepsilon > 0$. There exists $N$ such that for every $n \geq N$ we have $\ell - \varepsilon < m_n$ and $M_n < \ell + \varepsilon$. By construction, $m_n \leq a_n \leq M_n$ for every $n$, so the chain of inequalities:

$$
\ell - \varepsilon < m_n \leq a_n \leq M_n < \ell + \varepsilon
$$

holds for every $n \geq N$. This says exactly that $|a_n - \ell| < \varepsilon$ for every $n \geq N$, which is the definition of convergence to $\ell$.

The same statement extends to the case $\ell = \pm\infty$ with the natural interpretation: $a_n \to +\infty$ if and only if $\liminf a_n = +\infty$, and $a_n \to -\infty$ if and only if $\limsup a_n = -\infty$. In both cases the two extended-real quantities collapse to the same value, which becomes the limit of the sequence.

> The criterion is particularly valuable when working with sequences for which a direct $\varepsilon$-argument is difficult, but the tail-suprema and tail-infima are accessible. Computing $\limsup$ and $\liminf$ separately and comparing them turns the question of convergence into a question of equality between two well-defined quantities.

## Basic inequalities

Several order properties follow directly from the definitions and are used throughout the analysis of sequences.

The first concerns the relative position of the two quantities. For every sequence $(a_n)$:

$$
\liminf_{n \to \infty} a_n \leq \limsup_{n \to \infty} a_n
$$

To see this, note that $m_n \leq a_n \leq M_n$ for every $n$, hence $m_n \leq M_n$ for every $n$. Passing to the limit on both sides preserves the inequality, since both sequences are monotone and admit limits in the extended real line.

The second concerns comparison between two sequences. If $a_n \leq b_n$ holds for every $n$ sufficiently large, then:

$$
\limsup_{n \to \infty} a_n \leq \limsup_{n \to \infty} b_n, \qquad \liminf_{n \to \infty} a_n \leq \liminf_{n \to \infty} b_n
$$

The argument is the same for both. Suppose $a_n \leq b_n$ for every $n \geq N$. For every $k \geq N$:

$$
\sup_{j \geq k} a_j \leq \sup_{j \geq k} b_j
$$

since the supremum is taken over the same range of indices and the inequality holds termwise. Passing to the limit as $k \to \infty$ preserves the inequality and yields $\limsup a_n \leq \limsup b_n$. The argument for the limit inferior is identical, with $\inf$ replacing $\sup$.

A useful consequence is the squeeze for $\limsup$ and $\liminf$: if $a_n \leq b_n \leq c_n$ for every $n$ sufficiently large, then:

$$
\liminf a_n \leq \liminf b_n \leq \limsup b_n \leq \limsup c_n
$$

When the outer bounds satisfy $\liminf a_n = \limsup c_n = \ell$, the chain forces $\liminf b_n = \limsup b_n = \ell$, and by Theorem 2 the sequence $(b_n)$ converges to $\ell$. This recovers the [squeeze theorem](../convergent-and-divergent-sequences/) in a slightly more flexible form, since the outer sequences need not be convergent themselves.

## Connection to the root test

The limit superior plays a central role in the convergence of [series](../series/) with non-negative terms, through the root test. Given a series $\sum_{n=0}^{\infty} a_n$ with $a_n \geq 0$, set:

$$
\rho = \limsup_{n \to \infty} \sqrt[n]{a_n}
$$

The series converges if $\rho < 1$ and diverges if $\rho > 1$; the case $\rho = 1$ is inconclusive. The use of $\limsup$ rather than $\lim$ is essential: it makes the root test applicable to every series, not only to those for which the ordinary limit $\lim \sqrt[n]{a_n}$ exists.