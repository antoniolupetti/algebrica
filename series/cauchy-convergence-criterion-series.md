---
title: Cauchy Convergence Criterion for Series
source: https://algebrica.org/cauchy-convergence-criterion-series/
license: CC BY-NC 4.0
tags:
  - cauchy-criterion
  - convergence
  - partial-sums
  - series
---
## Definition

Cauchy’s criterion proves that a [series](../series/) converges without requiring its sum. Rather than computing the value of the series, the criterion checks whether the partial sums eventually become arbitrarily close to one another. When this condition holds, the series converges even if its [limit](../limits/) remains unknown.

This criterion relies on the [Cauchy convergence criterion](../cauchy-sequence/) for [sequences](../sequences/), which states that a sequence $a_n$ is convergent if and only if:

$$
\forall \ \varepsilon > 0 \ \exists \ \nu \in \mathbb{N} \ : \ |a_n - a_m| < \varepsilon \quad \forall\ n, m > \nu
$$


Let $\sum_{k=1}^{\infty} a_k$ be a series. According to Cauchy’s criterion, the series is convergent if and only if the following condition holds:

$$
\forall \ \varepsilon > 0 \ \exists \ \nu \in \mathbb{N}\ : \ 
\left| \sum_{k=\nu+1}^{\nu+p} a_k \right| < \varepsilon \quad \forall \ p \in \mathbb{N}
$$

The sum of any tail of the series, starting from a sufficiently large index, must be arbitrarily small, which ensures that the partial sums converge. To prove this, we apply the Cauchy convergence criterion for sequences to the series.

+ Recall that a series $\sum a_k$ converges if and only if the sequence of its partial sums $s_n = \sum_{k=1}^{n} a_k$ converges. 
+ Therefore, the series converges if and only if the sequence $(s_n)$ is a Cauchy sequence.

In the case of a series, the difference between two partial sums can be written as:

$$
s_{n+p} - s_n = \sum_{k=n+1}^{n+p} a_k
$$

Taking the absolute value, we get:

$$
|s_{n+p} - s_n| = \left| \sum_{k=n+1}^{n+p} a_k \right|
$$

The Cauchy criterion for sequences requires that $|s_{n+p} - s_n| < \varepsilon$ for all $p \in \mathbb{N}$, provided that $n$ is large enough. In our case, the expression:

$$
\left| \sum_{k=n+1}^{n+p} a_k \right|
$$

represents a tail of the series. If this tail becomes small for large $n$, it plays the role of $\varepsilon$ in the Cauchy condition for sequences, which proves the criterion.

## Example 1

We use Cauchy’s criterion to prove that the [geometric series](../geometric-series/) converges when $|x| < 1$:

$$
\sum_{k=0}^{\infty} x^k
$$

We consider the tail of the series starting from index $n+1$:

$$
\left| \sum_{k=n+1}^{n+p} x^k \right| = \left| x^{n+1} + x^{n+2} + \dots + x^{n+p} \right|
$$

This is a finite geometric sum, which we can compute explicitly:

$$
\left| \sum_{k=n+1}^{n+p} x^k \right| = \left| x^{n+1} \cdot \frac{1 - x^p}{1 - x} \right| = \frac{|x|^{n+1} \cdot |1 - x^p|}{|1 - x|}
$$

Since $|x| < 1$, we have $|x|^{n+1} \to 0$ as $n \to \infty$, and the other factors remain bounded. Therefore, for any $\varepsilon > 0$, we can find $n$ large enough so that the entire expression is less than $\varepsilon$.This shows that the tail becomes arbitrarily small, which satisfies Cauchy’s criterion.

## Example 2

We now prove that the geometric series converges at a specific value, $x = 0.5$:

$$
\sum_{k=0}^{\infty} x^k
$$

Since $|x| < 1$, we expect the series to converge. To apply Cauchy’s convergence criterion, we examine the size of the tail:

$$
\left| \sum_{k=n+1}^{n+p} x^k \right|
$$

We can evaluate the sum using the formula:

$$
\sum_{k=n+1}^{n+p} x^k = x^{n+1} \cdot \frac{1 - x^p}{1 - x}
$$

Taking the absolute value gives:

$$
\left| \sum_{k=n+1}^{n+p} x^k \right| = \frac{(0.5)^{n+1} \cdot |1 - (0.5)^p|}{|1 - 0.5|} = 2 \cdot (0.5)^{n+1} \cdot |1 - (0.5)^p|
$$

Two facts bound this expression: $(0.5)^{n+1} \to 0$ as $n \to \infty$ and $|1 - (0.5)^p| \leq 1$ for all $p \in \mathbb{N}$. Therefore:

$$
\left| \sum_{k=n+1}^{n+p} x^k \right| \leq 2 \cdot (0.5)^{n+1}
$$

Since the right-hand side tends to zero as $n \to \infty$, for any $\varepsilon > 0$, we can find $n$ large enough so that:

$$
\left| \sum_{k=n+1}^{n+p} x^k \right| < \varepsilon \quad \text{for all } p \in \mathbb{N}
$$

This satisfies Cauchy’s convergence criterion. So the series converges for $x = 0.5$.