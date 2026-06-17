---
title: Harmonic Series
source: https://algebrica.org/harmonic-series/
license: CC BY-NC 4.0
tags:
  - divergence
  - harmonic-series
  - p-series
  - series
---
## Definition

The harmonic series is defined as the infinite sum:

$$
\sum_{k=1}^{\infty} \frac{1}{k}
$$

where each term is the reciprocal of a [natural number](../natural-numbers/). Despite the terms approaching zero, the [series](../series/) diverges, meaning the sum grows without bound. Because it is a series with [positive terms](../series-with-positive-terms/), the limit of the sequence of its partial sums exists, and the series diverges to positive infinity:

$$
S = \lim_{n \to +\infty} s_n = \lim_{n \to +\infty} \sum_{k=1}^{n} \frac{1}{k}
$$

One might think that, as $n \to \infty$, the terms tend to zero and so the series converges. This is a logical error, the terms $\frac{1}{n}$ do approach zero but not fast enough for the series to converge.

![IMG. 1](svg/harmonic-series-1.svg)

> Here is the graph of the partial sums of the harmonic series up to $n = 100.$ As can be seen, the curve rises slowly yet unceasingly, confirming that the series is divergent.

- - -

Several methods prove that the harmonic series diverges. One groups the terms of the [partial sums](../series/):

$$
\sum_{k=1}^{\infty} \frac{1}{k} = 1 + \frac{1}{2} + \left( \frac{1}{3} + \frac{1}{4} \right) + \left( \frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8} \right) + \cdots
$$

Each group contains twice as many terms as the previous one. By observing that each group adds at least $1/2$ to the sum, we conclude that the overall series grows without bound:

$$
\sum_{k=1}^{\infty} \frac{1}{k} = \infty
$$

Hence, the harmonic series diverges. Knowing how the harmonic series and its variants behave is useful, since the [comparison test](../series-with-positive-terms/) and the [asymptotic comparison test](../asymptotic-comparison-test/) often let us relate a complex series to a harmonic one to check whether it converges.

## Generalized harmonic series (p-series)

Raising the denominator to a [power](../powers/) $a$ produces the series:

$$
\sum_{k=1}^{\infty} \frac{1}{k^a}
$$

Unlike the standard harmonic series, its convergence depends on the exponent $a$:

+ If $a > 1$ the series converges.
+ If $a \leq 1$ the series diverges.

- - -

A necessary condition for the convergence of a series $\sum a_k$ is that the general term tends to zero:

$$
\lim_{k \to \infty} a_k = 0.
$$

If this condition is not satisfied, that is, if $\lim_{k \to \infty} a_k \neq 0$, then the series diverges. For the generalized harmonic series with exponent $a \leq 1$, this condition fails. For example, when $a = 0$, the terms become constant $a_k = 1$, and:

$$
\lim_{k \to \infty} \frac{1}{k^0} = \lim_{k \to \infty} 1 = 1 \neq 0.
$$

Hence, the series diverges because its general term does not tend to zero.

- - -

When $a > 1$, we apply the [integral test](../integral-test-for-series-convergence/) to determine whether the series converges. We consider the corresponding [improper integral](../improper-integrals/):

$$
\int_1^{\infty} \frac{1}{x^a} \ dx
$$

Since $a > 1$, we have:

$$
\int_1^{\infty} \frac{1}{x^a} \ dx
= \lim_{t \to \infty} \int_1^t x^{-a} \ dx 
$$

By evaluating the integral at the endpoints, we obtain:

$$
\lim_{t \to \infty} \left[ \frac{x^{1-a}}{1 - a} \right]_1^t
= \lim_{t \to \infty} \left( \frac{t^{1 - a}}{1 - a} - \frac{1}{1 - a} \right)
$$

Because $a > 1$, the exponent $1 - a < 0$, so $t^{1 - a} \to 0$. Therefore:

$$
\int_1^{\infty} \frac{1}{x^a} \ dx = \frac{1}{a - 1}
$$

which is finite. Hence the series converges for all $a > 1$.

## Abel series

Weighting the generalized harmonic series with a [logarithmic](../logarithms/) factor produces the Abel series, which depends on two exponents $p$ and $q$:

$$
\sum_{n=2}^{\infty} \frac{1}{n^p (\log n)^q}
$$

The summation starts at $n = 2$ to avoid the index $n = 1$, where $\log 1 = 0$ causes division by zero. The power $n^p$ sets the dominant rate of decay, while the logarithmic factor refines the behavior only at the boundary. Its nature follows four cases:

+ If $p > 1$, the series converges for every $q$.
+ If $p = 1$ and $q > 1$, the series converges.
+ If $p = 1$ and $q \leq 1$, the series diverges.
+ If $p < 1$, the series diverges for every $q$.

- - -

When $p \neq 1$ the power $n^p$ dominates the logarithm, so the series follows the generalized harmonic series. For $p > 1$, choose an exponent $s$ with $1 < s < p$. Since $(\log n)^q$ grows slower than any positive power of $n$, eventually:

$$
\frac{1}{n^p (\log n)^q} < \frac{1}{n^s}
$$

The series $\sum \frac{1}{n^s}$ converges because $s > 1$, so the [comparison test](../series-with-positive-terms/) gives convergence. For $p < 1$, choose $s$ with $p < s < 1$. Eventually the inequality reverses:

$$
\frac{1}{n^p (\log n)^q} > \frac{1}{n^s}
$$

The series $\sum \frac{1}{n^s}$ diverges because $s < 1$, so the original series diverges as well.

- - -

The case $p = 1$ is the boundary, where the logarithm alone decides. We apply the [integral test](../integral-test-for-series-convergence/) to the function:

$$
f(x) = \frac{1}{x (\log x)^q}
$$

which is positive, [continuous](../continuous-functions/), and [decreasing](../increasing-and-decreasing-functions/) for $x \geq 2$. Using the [substitution](../integration-by-substitution/) $u = \log x$, the improper integral becomes:

$$
\int_2^{\infty} \frac{1}{x (\log x)^q} \ dx = \int_{\log 2}^{\infty} \frac{1}{u^q} \ du
$$

The last integral converges if and only if $q > 1$. By the integral test the series with $p = 1$ converges if and only if $q > 1$. As an application, we study the nature of the series:

$$
\sum_{n=2}^{\infty} \frac{1}{n \sqrt{\log n}}
$$

This is an Abel series with $p = 1$ and $q = \frac{1}{2}$. Since $p = 1$ and $q = \frac{1}{2} \leq 1$, the series diverges.