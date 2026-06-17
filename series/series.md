---
title: Series
source: https://algebrica.org/series/
license: CC BY-NC 4.0
tags:
  - convergence
  - divergence
  - partial-sums
  - series
---
## Introduction

The concept of a series is closely tied to infinite [sequences](../sequences/) of [real numbers](../types-of-numbers/), with the main goal of studying the behavior of their infinite sum. This involves determining whether the sum approaches a finite [limit](../limits/) (convergence) or grows without bound (divergence). From a formal point of view, let $\{a_n\}_{n \in \mathbb{N}}$ be a sequence of real numbers. The partial sum of order $n$ collects the first $n$ terms of the sequence:

$$
s_n = \sum_{k=1}^{n} a_k = a_1 + a_2 + \cdots + a_n
$$

The partial sums form a new sequence $\{s_n\}$, and the series associated with $\{a_n\}$ is the infinite sum obtained as $n$ grows without bound, written $\sum_{n=1}^{\infty} a_n$.

The terms summed here are real numbers, but the notion of a series is more general. The objects added can be [complex numbers](../complex-numbers/), [functions](../function-series/), [vectors](../vectors/), or [matrices](../matrices/), provided the space they belong to gives meaning to the limit of the partial sums. Real terms are the foundation for these extensions, since each of them reduces to a numerical series once a coordinate or a norm is fixed.

## Nature of a series

Whether a series converges is decided by the limit of its sequence of partial sums:

$$
\lim_{n \to \infty} s_n = \lim_{n \to \infty} \sum_{k=1}^{n} a_k
$$

+ If the limit exists and is finite, the series $\sum a_n$ is said to converge. In this case, the value of the limit is called the sum of the series.
+ If the limit is $+\infty$ or $-\infty$, the series $\sum a_n$ is said to diverge.
+ In all other cases, such as when the limit does not exist or oscillates, the series $\sum a_n$ is considered indeterminate.

A series $\sum a_k$ converges absolutely if the series of [absolute values](../absolute-value/) $\sum |a_k|$ converges. Absolute convergence is stronger than ordinary convergence, because every absolutely convergent series converges, while the converse can fail. It also makes the sum stable under reordering. A finite sum always obeys the commutative law, whereas an infinite series may not, and rearranging the terms of a series that converges without converging absolutely can change its sum or even destroy convergence.

> The expression sum of a series is a conventional term, since infinitely many terms are involved, it is not a finite sum in the traditional sense, but the limit of the sequence of partial sums.

Altering a finite number of terms in the series does not affect its convergence or divergence. That is, two series that differ only by finitely many terms share the same convergence nature. However, they do not necessarily have the same sum.

## Necessary condition for convergence

If the series $\sum_{n=1}^{\infty} a_n$ converges, its general term must tend to zero:

$$
\lim_{n \to \infty} a_n = 0
$$

This condition is necessary but not sufficient, since $a_n \to 0$ does not guarantee that the series converges. To prove it, let $S$ be the sum of the series, so that the sequence of partial sums $\{s_n\}$ tends to $S$. The shifted sequence $\{s_{n-1}\}$ tends to the same limit:

$$
S = \lim_{n \to \infty} s_n = \lim_{n \to \infty} s_{n-1}
$$

Since consecutive partial sums differ by a single term, $s_n - s_{n-1} = a_n$, the difference must tend to zero:

$$
\lim_{n \to \infty} (s_n - s_{n-1}) = \lim_{n \to \infty} a_n = S - S = 0
$$

## Partial remainder

The partial remainder of order $n$, written $R_n$, collects the terms of a series that follow the index $n$:

$$
R_n = \sum_{k=n+1}^{\infty} a_k
$$

When the series converges with sum $S$, the remainder is the difference between the total sum and the partial sum of order $n$:

$$
R_n = S - s_n
$$

This identity makes $R_n$ the error committed when the partial sum $s_n$ is used to approximate the sum of the series. If the series $\sum a_n$ converges, then the remainder tends to zero:

$$
\lim_{n \to \infty} R_n = 0
$$

The partial sums $s_n$ tend to $S$ by definition of convergence, so the difference $S - s_n$ tends to $S - S = 0$. The vanishing of the remainder expresses the same fact as convergence, the contribution of the discarded tail becomes negligible as more terms are retained.

## Linear properties of series

Let $\sum_{k=1}^{\infty} a_k$ be a convergent series, and let $\lambda \in \mathbb{R}$, $\lambda \ne 0$. Then the series $\sum_{k=1}^{\infty} \lambda a_k$ also converges, and its sum is:

$$
\sum_{k=1}^{\infty} \lambda a_k = \lambda \sum_{k=1}^{\infty} a_k
$$

If both series $\sum_{k=1}^{\infty} a_k$ and $\sum_{k=1}^{\infty} b_k$ converge, then their term-by-term sum also defines a convergent series:

$$
\sum_{k=1}^{\infty} (a_k + b_k)
$$

Moreover, the sum of the resulting series is equal to the sum of the individual series:

$$
\sum_{k=1}^{\infty} (a_k + b_k) = \sum_{k=1}^{\infty} a_k + \sum_{k=1}^{\infty} b_k
$$

## Cauchy product of two series

Multiplying two series is less immediate than adding them, since the product of two infinite sums generates all the pairwise products $a_i b_j$. Collecting the terms for which the indices sum to a fixed value $n$ gives the Cauchy product of $\sum_{n=0}^{\infty} a_n$ and $\sum_{n=0}^{\infty} b_n$, defined as the series $\sum_{n=0}^{\infty} c_n$ with general term:

$$
c_n = \sum_{k=0}^{n} a_k b_{n-k}
$$

This grouping is the one that reproduces the ordinary product when both series are finite, and it is the natural choice for power series, where $c_n$ is the coefficient of the term of degree $n$ in the product.

The Cauchy product does not always converge to the product of the two sums, and convergence of both factors alone is not enough to control it. A sufficient condition is absolute convergence, stated by Mertens' theorem. If $\sum_{n=0}^{\infty} a_n$ converges absolutely to $A$ and $\sum_{n=0}^{\infty} b_n$ converges to $B$, then the Cauchy product converges to the product of the sums:

$$
\sum_{n=0}^{\infty} c_n = A \cdot B
$$

When both series converge only conditionally, the product series may fail to converge. Taking $a_n = b_n = \frac{(-1)^n}{\sqrt{n+1}}$ gives a general term $c_n$ that does not tend to zero, so the Cauchy product diverges even though each factor converges.

## Fundamental series

A few series recur so frequently that they serve as reference cases, both as standard examples and as terms of comparison for the convergence tests applied to other series. The arithmetic series, the harmonic series, the geometric series, and the telescoping series are the most representative.

The [arithmetic series](../arithmetic-series/) sums the terms of an arithmetic progression, in which each term differs from the previous one by a fixed amount $d$ called the common difference:

$$
\sum_{n=1}^{\infty} a_n, \qquad a_n = a_1 + (n-1)d
$$

The partial sum of the first $n$ terms has a closed form, obtained by pairing the terms symmetrically around their average:

$$
s_n = \frac{n(a_1 + a_n)}{2} = \frac{n}{2}[2a_1 + (n-1)d]
$$

Unless every term is zero, the general term does not tend to zero, either because it stays at a constant nonzero value when $d = 0$, or because it grows without bound when $d \neq 0$. The necessary condition for convergence fails, so the arithmetic series diverges.

- - -

The harmonic series is the sum of the reciprocals of the [natural numbers](../natural-numbers/):

$$
\sum_{n=1}^{\infty} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n} + \cdots
$$

Its general term tends to zero, yet the series diverges, so the necessary condition for convergence is met without convergence taking place. The partial sums grow without bound, only at an increasingly slow rate. Replacing the exponent of the denominator with a real parameter $p$ produces the [generalized harmonic series](../harmonic-series/):

$$
\sum_{n=1}^{\infty} \frac{1}{n^p} = 1 + \frac{1}{2^p} + \frac{1}{3^p} + \cdots + \frac{1}{n^p} + \cdots, \quad p \in \mathbb{R}
$$

Its behavior depends on the value of $p$:

+ If $p > 1$ the series converges.
+ If $p \leq 1$ the series diverges.

The ordinary harmonic series is the case $p = 1$, which lies on the boundary between the two regimes.

- - -

The [geometric series](../geometric-series/) collects the successive powers of a fixed ratio $q$:

$$
\sum_{n=0}^{\infty} q^n = 1 + q + q^2 + q^3 + \cdots + q^n + \cdots
$$

Each term is obtained from the previous one by multiplying by $q$, so the size of $q$ governs whether the terms shrink or grow. Its behavior depends on the value of $q$:

+ If $-1 < q < 1$, the terms tend to zero and the series converges.
+ If $q \geq 1$, the terms do not vanish and the series diverges.
+ If $q \leq -1$, the series is irregular, since its partial sums either diverge or oscillate without approaching a limit.

When the series converges, its sum has the closed form $\frac{1}{1-q}$.

- - -

The [telescoping series](../telescoping-series/) is built from terms that split so that consecutive contributions cancel:

$$
\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = \frac{1}{2} + \frac{1}{6} + \cdots + \frac{1}{n(n+1)} + \cdots
$$

Each term decomposes as $\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}$, so in the partial sum every fraction cancels with the following one, leaving only the first and the last:

$$
s_n = 1 - \frac{1}{n+1}
$$

As $n$ grows without bound the last term vanishes, so the series converges to $1.$