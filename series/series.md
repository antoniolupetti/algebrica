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

Let $\{a_n\}_{n \geq 1}$ be an infinite [sequence](../sequences/) of [real numbers](../real-numbers/). The partial sum of order $n$ is the sum of the first $n$ terms:

$$
s_n = \sum_{k=1}^{n} a_k = a_1 + a_2 + \cdots + a_n
$$

The partial sums form the sequence $\{s_n\}.$ We denote the associated series by $\sum_{n=1}^{\infty} a_n.$ The [limit](../limits/) of $\{s_n\}$ determines whether the series converges and gives its sum when it does.

The terms considered here are real numbers, but a series can also have [complex numbers](../complex-numbers/), [functions](../function-series/), [vectors](../vectors/), or [matrices](../matrices/) as terms. In each case, the ambient space must have an addition operation and a specified notion of convergence for the partial sums.

## Nature of a series

The [convergence or divergence of the sequence](../convergent-and-divergent-sequences/) of partial sums determines the behavior of the series:

$$
\lim_{n \to \infty} s_n = \lim_{n \to \infty} \sum_{k=1}^{n} a_k
$$

+ If the limit exists and is finite, the series $\sum a_n$ converges. The value of the limit is the sum of the series.
+ If the partial sums tend to $+\infty$ or $-\infty,$ the series $\sum a_n$ diverges to $+\infty$ or $-\infty,$ respectively.
+ If the partial sums have no limit, for example because they oscillate, the series $\sum a_n$ also diverges.

> The phrase "sum of a series" is conventional. It denotes the limit of the sequence of partial sums rather than an ordinary finite sum.

A series $\sum a_k$ converges absolutely if the series of [absolute values](../absolute-value/) $\sum |a_k|$ converges. Every absolutely convergent series converges, but the converse can fail. A convergent series that is not absolutely convergent is conditionally convergent. Every rearrangement of an absolutely convergent series has the same sum. By contrast, rearranging a conditionally convergent series can change its sum or make it diverge.

Changing finitely many terms does not affect convergence. Two series that differ only in finitely many terms therefore either both converge or both diverge. When they converge, their sums need not be equal.

## Necessary condition for convergence

If the series $\sum_{n=1}^{\infty} a_n$ converges, its general term must tend to zero:

$$
\lim_{n \to \infty} a_n = 0
$$

This condition is necessary but not sufficient, since $a_n \to 0$ does not guarantee that the series converges. The harmonic series below provides a counterexample to sufficiency. To prove the necessary condition, let $S$ be the sum of the series, so the sequence of partial sums $\{s_n\}$ tends to $S.$ The shifted sequence $\{s_{n-1}\}$ tends to the same limit:

$$
S = \lim_{n \to \infty} s_n = \lim_{n \to \infty} s_{n-1}
$$

The identity $a_n = s_n - s_{n-1}$ and the [algebra of limits](../algebra-of-limits/) give:

$$
\lim_{n \to \infty} (s_n - s_{n-1}) = \lim_{n \to \infty} a_n = S - S = 0
$$

## Partial remainder

For a convergent series with sum $S,$ the partial remainder of order $n,$ written $R_n,$ is the sum of the terms that follow the index $n:$

$$
R_n = \sum_{k=n+1}^{\infty} a_k
$$

The remainder is also the difference between the sum of the series and the partial sum of order $n:$

$$
R_n = S - s_n
$$

The difference $R_n = S - s_n$ measures the error in approximating $S$ by $s_n,$ while $|R_n|$ is the absolute error. Since $s_n \to S,$ this identity gives:

$$
\lim_{n \to \infty} R_n = 0
$$

The [Cauchy convergence criterion for series](../cauchy-convergence-criterion-series/) characterizes convergence through finite tails without requiring the sum $S$ to be known.

## Linear properties of series

For every $\lambda \in \mathbb{R}$ and every convergent series $\sum_{k=1}^{\infty} a_k,$ the series $\sum_{k=1}^{\infty} \lambda a_k$ also converges, and its sum is:

$$
\sum_{k=1}^{\infty} \lambda a_k = \lambda \sum_{k=1}^{\infty} a_k
$$

If both series $\sum_{k=1}^{\infty} a_k$ and $\sum_{k=1}^{\infty} b_k$ converge, their term-by-term sum also converges and satisfies:

$$
\sum_{k=1}^{\infty} (a_k + b_k) = \sum_{k=1}^{\infty} a_k + \sum_{k=1}^{\infty} b_k
$$

Both properties follow by applying the linearity of finite sums and the limit laws to the partial sums.

## Cauchy product of two series

For finite sums, multiplication produces one term for every pair of indices. For infinite series, we group the products $a_k b_{n-k}$ that have the same index sum $n.$ The Cauchy product of $\sum_{n=0}^{\infty} a_n$ and $\sum_{n=0}^{\infty} b_n$ is the series $\sum_{n=0}^{\infty} c_n$ with general term:

$$
c_n = \sum_{k=0}^{n} a_k b_{n-k}
$$

This grouping reproduces the ordinary product for finite sums. For [power series](../power-series/), $c_n$ is the coefficient of the term of degree $n$ in the product.

Convergence of both factors does not imply convergence of their Cauchy product. Mertens' theorem gives a sufficient condition. If $\sum_{n=0}^{\infty} a_n$ converges absolutely to $A$ and $\sum_{n=0}^{\infty} b_n$ converges to $B,$ then the Cauchy product converges to the product of the sums:

$$
\sum_{n=0}^{\infty} c_n = A \cdot B
$$

When both series converge conditionally, the Cauchy product may diverge. For example, set $a_n = b_n = \frac{(-1)^n}{\sqrt{n+1}}.$ Both series converge by the [Leibniz criterion](../leibniz-criterion/) because $(n+1)^{-1/2}$ decreases to zero. Their absolute-value series is the $p$-series with $p = \frac{1}{2},$ which diverges by the classification below. Their Cauchy coefficients are:

$$
c_n = (-1)^n \sum_{k=0}^{n} \frac{1}{\sqrt{(k+1)(n-k+1)}}
$$

For $0 \leq k \leq n,$ the [arithmetic-geometric mean inequality](../arithmetic-mean/) gives $\sqrt{(k+1)(n-k+1)} \leq \frac{n+2}{2}.$ Taking reciprocals gives a lower bound of $\frac{2}{n+2}$ for each of the $n+1$ summands. Summing these bounds gives:

$$
|c_n| \geq \frac{2(n+1)}{n+2}
$$

The right-hand side tends to $2,$ so $c_n$ does not tend to zero and the Cauchy product diverges.

## Fundamental series

The arithmetic, harmonic, geometric, and telescoping series recur as examples and as comparison series in convergence tests.

The [direct comparison test](../series-with-positive-terms/) and the [asymptotic comparison test](../asymptotic-comparison-test/) use known series as models. Other criteria include the [ratio test](../ratio-test-for-series-convergence/), the [root test](../root-test-for-series-convergence/), and the [integral test](../integral-test-for-series-convergence/).

An [arithmetic series](../arithmetic-series/) has the terms of an [arithmetic sequence](../arithmetic-sequence/). Consecutive terms differ by a fixed number $d$ called the common difference:

$$
\sum_{n=1}^{\infty} a_n, \qquad a_n = a_1 + (n-1)d
$$

Pairing the terms symmetrically around their average gives a closed form for the partial sum of the first $n$ terms:

$$
s_n = \frac{n(a_1 + a_n)}{2} = \frac{n}{2}[2a_1 + (n-1)d]
$$

The zero series is the only convergent arithmetic series. If $d = 0$ and $a_1 \neq 0,$ the general term is a nonzero constant. If $d \neq 0,$ its absolute value grows without bound. In both cases, $a_n$ does not tend to zero, so the arithmetic series diverges.

- - -

The [harmonic series](../harmonic-series/) is the sum of the reciprocals of the [natural numbers](../natural-numbers/):

$$
\sum_{n=1}^{\infty} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n} + \cdots
$$

The term $1/n$ tends to zero. For $m \geq 1,$ the terms with indices from $2^{m-1}+1$ through $2^m$ form a block of $2^{m-1}$ terms, each at least $1/2^m.$ Each block therefore has sum at least $1/2,$ so the partial sums are unbounded and the series diverges. Thus the condition $a_n \to 0$ is not sufficient for convergence. Allowing a real exponent $p$ gives the generalized harmonic series:

$$
\sum_{n=1}^{\infty} \frac{1}{n^p} = 1 + \frac{1}{2^p} + \frac{1}{3^p} + \cdots + \frac{1}{n^p} + \cdots, \quad p \in \mathbb{R}
$$

Its convergence depends on $p:$

+ If $p > 1,$ the series converges.
+ If $p \leq 1,$ the series diverges.

The ordinary harmonic series is the boundary case $p = 1.$

- - -

The terms of the [geometric series](../geometric-series/) form a [geometric sequence](../geometric-sequence/) with common ratio $q:$

$$
\sum_{n=0}^{\infty} q^n = 1 + q + q^2 + q^3 + \cdots + q^n + \cdots
$$

Each term after the first is $q$ times the preceding term. For $q \neq 1,$ the sum of the first $n$ terms is:

$$
s_n = \sum_{k=0}^{n-1} q^k = \frac{1-q^n}{1-q}
$$

+ If $|q| < 1,$ then $q^n \to 0,$ so the series converges to $\frac{1}{1-q}.$
+ If $|q| \geq 1,$ then $q^n$ does not tend to zero, so the series diverges.

For $q = -1,$ the partial sums oscillate between $1$ and $0;$ when $q < -1,$ their absolute values grow without bound.

- - -

A [telescoping series](../telescoping-series/) has terms that decompose so that consecutive contributions cancel. The following series is telescoping:

$$
\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = \frac{1}{2} + \frac{1}{6} + \cdots + \frac{1}{n(n+1)} + \cdots
$$

Each term has the [partial-fraction decomposition](../partial-fraction-decomposition/) $\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1},$ so every intermediate contribution cancels and the two uncancelled terms give:

$$
s_n = 1 - \frac{1}{n+1}
$$

Since $\frac{1}{n+1}$ tends to zero, $s_n$ tends to $1,$ and the series has sum $1.$
