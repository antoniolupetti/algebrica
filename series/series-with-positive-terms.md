---
title: Series With Positive Terms
source: https://algebrica.org/series-with-positive-terms/
license: CC BY-NC 4.0
tags:
  - comparison-test
  - convergence
  - positive-term-series
  - series
---
## Definition

A series with positive terms is one in which every term $a_k$ satisfies $a_k > 0$ for all $k \in \mathbb{N}$. As a result, the sequence of partial sums:

$$
S_n = \sum_{k=1}^{n} a_k
$$

is strictly increasing, since each new term contributes a positive quantity. This guarantees that the [series](../series/) cannot oscillate or decrease. Such a series has only two possible behaviors, it either converges to a finite value if the partial sums are bounded above, or it diverges to infinity if they are not. It is never indeterminate or conditionally convergent. More formally, for a series of the form:

$$
\sum_{k=1}^{\infty} a_k \quad \text{with } a_k > 0
$$

the series converges if and only if the sequence of partial sums $(S_n)$ is bounded. This property makes positive-term series suitable for convergence tests such as the comparison test, the [integral test](../integral-test-for-series-convergence/), and the [ratio test](../ratio-test-for-series-convergence/), all of which require non-negative terms.

- - -

The [harmonic series](../harmonic-series/) is an example of a positive-term series that diverges:

$$
\sum_{k=1}^{\infty} \frac{1}{k}
$$

Although the terms $\frac{1}{k}$ tend to zero, the sequence of partial sums increases without limit.

In general, we refer to a constant-sign series when the terms of the sequence $\{a_n\}$ all have the same sign for every $n \in \mathbb{N}$; that is, they are either all positive or all negative.

## Comparison test

To determine whether a series converges or diverges, we compare it with another series whose behavior is already known. This method is useful for series with positive terms, where direct evaluation of convergence is difficult.

Let $\sum a_k$ and $\sum b_k$ be two series with positive terms. Suppose there exists an [integer](../integers/) $N \in \mathbb{N}$ such that:

$$
0 \leq a_k \leq b_k \quad \text{for all } k \geq N
$$

Each term $a_k$ is non-negative and less than or equal to the corresponding term $b_k$ (this condition is essential for applying the comparison test correctly). Then:

+ If $\sum b_k$ converges, then $\sum a_k$ also converges.
+ If $\sum a_k$ diverges, then $\sum b_k$ also diverges.

- - -

Consider the partial sums of each series:

$$
S_n = \sum_{k=1}^{n} a_k, \quad T_n = \sum_{k=1}^{n} b_k
$$

Since both sequences $a_k$ and $b_k$ are made of non-negative terms, both $S_n$ and $T_n$ are non-decreasing. Because $a_k \leq b_k$ for all $k \geq N$, we have:

$$
S_n \leq T_n \quad \text{for all } n \geq N
$$

If the series $\sum b_k$ converges, then $T_n$ has a finite limit and is bounded above. Since $S_n \leq T_n$, the sequence of partial sums $S_n$ is also bounded above. A non-decreasing and bounded sequence converges, so $\sum a_k$ also converges.

If $\sum a_k$ diverges, then $S_n \to \infty$. But since $S_n \leq T_n$, the only way this inequality can hold is if $T_n$ also grows without bound. Therefore, $\sum b_k$ also diverges.


## Example

Using the comparison test, we determine the nature of the following series:

$$
\sum_{n=1}^{\infty} \frac{1}{n^2 + 2n + 1}
$$

The denominator is a polynomial and all terms are positive, so this is a positive-term series and the comparison test applies.

> This point must be verified, since the comparison test is valid only for series in which all terms are positive.

- - -


First, we check whether the necessary condition for convergence is satisfied:

$$
\lim_{n \to +\infty} \frac{1}{n^2 + 2n + 1} = 0
$$

The [limit](../limits/) has the form $\frac{1}{\infty}$, so it equals zero, and the necessary condition for convergence is satisfied. By the comparison test:

$$ \frac{1}{n^2 + 2n + 1} < \frac{1}{n^2} $$

since the denominator in the first expression is greater than the denominator in the second. With:

$$ a_n = \frac{1}{n^2 + 2n + 1} \quad \text{and} \quad b_n = \frac{1}{n^2} $$

we have:

$$ a_n < b_n $$

The following series is a [generalized harmonic series](../harmonic-series/), which is known to converge when the exponent in the denominator satisfies the condition $p > 1$: 

$$ \sum_{n=1}^{\infty} b_n = \sum_{n=1}^{\infty} \frac{1}{n^2} $$ 
Hence, by the comparison test, since the series $\sum b_n$ converges, the series $\sum a_n$ also converges.

> Determining the nature of a positive-term series with the comparison test is straightforward, and choosing the right comparison and justifying the inequality requires practice.

## Extension to series of definite sign

The convergence tests built for positive-term series, the comparison test above together with the [asymptotic comparison test](../asymptotic-comparison-test/), the [ratio test](../ratio-test-for-series-convergence/), and the [root test](../root-test-for-series-convergence/), need only that the terms be non-negative from some index onward. Since altering finitely many terms does not change the nature of a series, these tests apply unchanged to a series whose terms are definitively non-negative, that is $a_n \geq 0$ for all $n \geq N$.

A series with non-positive terms reduces to this case by factoring out a minus sign:

$$
\sum_{n=0}^{\infty} a_n = -\sum_{n=0}^{\infty} (-a_n)
$$

The series $\sum (-a_n)$ has non-negative terms, so the tests decide its nature, and the overall factor $-1$ leaves convergence and divergence unchanged. The same reduction handles a series that is only definitively non-positive.