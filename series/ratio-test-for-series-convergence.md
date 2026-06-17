---
title: Ratio Test for Series Convergence
source: https://algebrica.org/ratio-test-for-series-convergence/
license: CC BY-NC 4.0
tags:
  - convergence
  - divergence
  - ratio-test
  - series
---
## What is the ratio test

The ratio test decides whether an infinite [series](../series/) with positive terms converges or diverges by examining the limit of the quotient between consecutive terms. It is the natural choice when the general term contains factorials or exponentials, where the ratio $\frac{a_{n+1}}{a_n}$ simplifies more than the $n$-th root used by the [root test](../root-test-for-series-convergence/). Suppose we have a series with positive terms:

$$
\sum_{n=0}^{\infty} a_n, \qquad a_n > 0
$$

Assume that the [limit](../limits/) of the ratio between a term and the one before it exists:

$$
\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = l
$$

Three cases can occur:

+ If $l < 1$, the series converges.
+ If $l > 1$, the series diverges.
+ If $l = 1$, the test is inconclusive.

> The same statement holds for a series whose terms are negative or, more generally, of constant sign, since the ratio of consecutive terms then coincides with the ratio of their absolute values.

## Proof

Consider first the case $l < 1$. Choose a [real number](../types-of-numbers/) $r$ with $l < r < 1$. By the definition of limit, there exists an [integer](../integers/) $N$ such that for all $n \geq N$:

$$
\frac{a_{n+1}}{a_n} < r
$$

Applying this inequality repeatedly from the index $N$ onward gives:

$$
a_{N+k} < r^k a_N \qquad \text{for every } k \geq 0
$$

The tail of the series is therefore bounded above by a [geometric series](../geometric-series/) of ratio $r$:

$$
\sum_{k=0}^{\infty} a_{N+k} < a_N \sum_{k=0}^{\infty} r^k
$$

Since $0 < r < 1$, the geometric series on the right converges. By the [comparison test](../series-with-positive-terms/) the tail converges, and so does the whole series.

- - -

Consider now the case $l > 1$. Choose a real number $r$ with $1 < r < l$. By the definition of limit there exists an integer $N$ such that for all $n \geq N$:

$$
\frac{a_{n+1}}{a_n} > r
$$

The terms are then increasing from the index $N$ onward, so $a_n > r^{n-N} a_N$. The right-hand side grows without bound, hence $a_n \nrightarrow 0$. The necessary condition for convergence fails and the series diverges.

> When $l > 1$ the general term does not tend to zero, it grows without bound. Divergence is caused by a term that fails to vanish, not by a slow accumulation of vanishing terms.

The boundary value $l = 1$ carries no information. The [harmonic series](../harmonic-series/) $a_n = \frac{1}{n}$ gives ratio $\frac{n}{n+1} \to 1$ and diverges, while the [p-series](../harmonic-series/) $a_n = \frac{1}{n^2}$ gives ratio $\left(\frac{n}{n+1}\right)^2 \to 1$ and converges.

## Example

Using the ratio test, we determine the nature of the series:

$$
\sum_{n=1}^{\infty} \frac{n!2^n}{n^n}
$$

The terms are positive for every $n \geq 1$, and the presence of a factorial together with the powers $2^n$ and $n^n$ makes the ratio of consecutive terms the convenient quantity to study. We form the ratio:

$$
\begin{align}
\frac{a_{n+1}}{a_n} &= \frac{(n+1)!2^{n+1}}{(n+1)^{n+1}} \cdot \frac{n^n}{n!2^n} \\[6pt]
&= \frac{(n+1)2n^n}{(n+1)^{n+1}} \\[6pt]
&= 2\left(\frac{n}{n+1}\right)^n
\end{align}
$$

The remaining limit is a standard exponential limit, which we rewrite through the exponential function:

$$
\lim_{n \to \infty} \left(\frac{n}{n+1}\right)^n = \lim_{n \to \infty} e^{n\log\left(\frac{n}{n+1}\right)}
$$

The exponent tends to a finite value, since:

$$
\lim_{n \to \infty} n\log\left(1 - \frac{1}{n+1}\right) = \lim_{n \to \infty} n\left(-\frac{1}{n+1}\right) = -1
$$

Substituting back, the ratio between consecutive terms has limit:

$$
\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = 2e^{-1} = \frac{2}{e} < 1
$$

Since the limit is smaller than $1$, the series converges by the ratio test.
