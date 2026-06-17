---
title: Asymptotic Comparison Test
source: https://algebrica.org/asymptotic-comparison-test/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - comparison-test
  - convergence
  - series
---
## What is the asymptotic comparison test

The asymptotic comparison test compares two series with positive terms through the limit of their ratio rather than through a term-by-term inequality. It removes the main difficulty of the [direct comparison test](../series-with-positive-terms/), where one must guess the right inequality and prove it. Let $\sum a_n$ and $\sum b_n$ be two series with positive terms, and suppose the terms are asymptotically equivalent:

$$
a_n \sim b_n \quad \text{as } n \to +\infty
$$

The two series then share the same behavior, they either both converge or both diverge. The relation $a_n \sim b_n$ means that the ratio of the terms tends to $1$:

$$
\lim_{n \to +\infty} \frac{a_n}{b_n} = 1
$$

The conclusion holds more generally whenever this limit is finite and strictly positive, since a ratio that stabilizes at a positive constant keeps the two general terms of the same order of magnitude.

> Asymptotic equivalence concerns only the eventual size of the terms, so the test reads the nature of a series from a simpler model series with the same dominant behavior.

## Why it works

Suppose $\frac{a_n}{b_n} \to L$ with $0 < L < +\infty$. From the definition of limit, for every small $\varepsilon > 0$ an [integer](../integers/) $N$ exists such that for all $n \geq N$:

$$
(L - \varepsilon) b_n < a_n < (L + \varepsilon) b_n
$$

Both inequalities involve only positive multiples of $b_n$. If $\sum b_n$ converges, the right inequality bounds $a_n$ above by a convergent series, so $\sum a_n$ converges by the [direct comparison test](../series-with-positive-terms/). If $\sum b_n$ diverges, the left inequality bounds $a_n$ below by a divergent series, so $\sum a_n$ diverges. The two series therefore have the same nature.

A natural reference for this comparison is the [generalized harmonic series](../harmonic-series/), whose convergence is fully known in terms of its exponent. Another frequent model is the [Mengoli series](../telescoping-series/) $\sum \frac{1}{n(n+1)}$, which converges to $1$ and is asymptotically equivalent to $\sum \frac{1}{n^2}$, since $\frac{1}{n^2} \sim \frac{1}{n(n+1)}$.

## Example

Using the asymptotic comparison test, we study the nature of the series:

$$
\sum_{n=1}^{\infty} \frac{e^{\sin^3\left(\frac{1}{\sqrt[3]{n}}\right)} - 1}{\sqrt[3]{n}}
$$

The terms are positive for every $n \geq 1$, so a comparison with a positive-term model is legitimate. As $n \to +\infty$ the argument $\frac{1}{\sqrt[3]{n}}$ tends to zero, which lets us replace each factor by its leading-order behavior. Using the [remarkable limits](../remarkable-limits/) $\sin x \sim x$ and $e^x - 1 \sim x$ for $x \to 0$, the numerator satisfies:

$$
e^{\sin^3\left(\frac{1}{\sqrt[3]{n}}\right)} - 1 \sim \sin^3\left(\frac{1}{\sqrt[3]{n}}\right) \sim \left(\frac{1}{\sqrt[3]{n}}\right)^3 = \frac{1}{n}
$$

Dividing by $\sqrt[3]{n}$ gives the model term:

$$
a_n \sim \frac{1}{n \sqrt[3]{n}} = \frac{1}{n^{1 + \frac{1}{3}}} = \frac{1}{n^{\frac{4}{3}}} = b_n
$$

The series $\sum b_n$ is a generalized harmonic series with exponent $\frac{4}{3} > 1$, so it converges. By the asymptotic comparison test the original series converges as well.
