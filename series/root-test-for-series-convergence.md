---
title: Root Test for Series Convergence
source: https://algebrica.org/root-test-for-series-convergence/
license: CC BY-NC 4.0
tags:
  - absolute-convergence
  - convergence
  - root-test
  - series
---
## What is the root test

The root test is a method used to determine whether an infinite [series](../series/) converges or diverges. It is particularly useful when each term of the series involves an expression raised to the $n$-th [power](../powers/), such as [exponentials](../exponential-function/) or [roots](../radicals/). Suppose we have a series with positive terms of the form:

$$
\sum_{n=1}^{+\infty} a_n
$$

Assume that the [limit](../limits/) exists and is finite:

$$
\limsup_{n \to \infty} \sqrt[n]{|a_n|} = L
$$

We use $\limsup$ because it is always defined for real sequences that are bounded from below. This makes the root test reliable even when the usual limit $\lim_{n \to \infty} \sqrt[n]{|a_n|}$ does not exist. By taking the [limit superior](../superior-and-inferior-limits-of-a-sequence/), the test can still detect the long-term behavior of the sequence and determine whether the series converges or diverges.

If the limit $L$ exists, three cases can occur:

+ If $L < 1$, the series converges absolutely.
+ If $L > 1$ or $L = \infty$, the series diverges.
+ If $L = 1$, the test is inconclusive.

> We use the [absolute value](../absolute-value/) $|a_n|$ to apply the root test to the absolute convergence of the series. This ensures the test works even if the terms $a_n$ are negative or alternate in sign, allowing us to focus only on their magnitude.

## How to recognize when to apply the root test

The root test is especially useful when the general term of a series is expressed in the form $a_n = (b_n)^n$, that is, when the entire term is raised to the power of $n$. In such cases, taking the $n$-th root of $a_n$ simplifies the expression significantly and often leads directly to a manageable limit.

By contrast, other tests may become more complicated in this context, especially when the ratio $\frac{a_{n+1}}{a_n}$ does not simplify easily or when factorials or [exponential](../exponential-function/) terms are involved in a way that makes limits more difficult to compute.

The root test is particularly effective in the following situations:

+ When $a_n = (f(n))^n$, with $f(n) > 0$
+ When the terms involve exponential-like growth or decay
+ When the limit $\sqrt[n]{|a_n|}$ is easier to compute than $\frac{a_{n+1}}{a_n}$

In all other cases, if the general term is not raised to the $n$-th power other tests may be more suitable.

## Proof

Consider the case of absolute convergence, with $L < 1$. There exists a [real number](../types-of-numbers/) $r$ such that:

$$
L < r < 1
$$

By the definition of $\limsup$, there exists an [integer](../integers/) $N$ such that for all $n \geq N$:

$$
\sqrt[n]{|a_n|} < r
\quad \rightarrow \quad |a_n| < r^n
$$

So the tail of the series satisfies:

$$
\sum_{n=N}^{\infty} |a_n| < \sum_{n=N}^{\infty} r^n
$$

Since $0 < r < 1$, the [geometric series](../geometric-series/) $\sum r^n$ converges. Therefore, by the [comparison test](../series-with-positive-terms/), the tail $\sum_{n=N}^{\infty} |a_n|$ converges, and so does the entire series $\sum |a_n|$.

- - -

Consider the case in which the series diverges, with $L > 1$. By definition of $\limsup$, for infinitely many indices $n$, we have:

$$
\sqrt[n]{|a_n|} > r
\quad \text{for some } r > 1
$$

Thus, $|a_n| > r^n$ infinitely often. But since $r^n \to \infty$, we know that $|a_n| \nrightarrow 0$.

The necessary condition for convergence of $\sum a_n$ fails, so the series diverges.

- - -

In the final case nothing can be concluded, namely when $L = 1$. For every $\varepsilon > 0$ we can find infinitely many $n$ such that:

$$
\sqrt[n]{|a_n|} > 1 - \varepsilon
\quad \text{and} \quad
\sqrt[n]{|a_n|} < 1 + \varepsilon
$$

This range includes both convergent and divergent behaviors. For example, the [harmonic series](../harmonic-series/) $a_n = \frac{1}{n}$ has $\sqrt[n]{|a_n|} \to 1$ and diverges. The [p-series](../harmonic-series/) $a_n = \frac{1}{n^2}$ also has $\sqrt[n]{|a_n|} \to 1$, but it converges. So, the test is inconclusive when $L = 1$.

## Example

Consider the series:

$$
\sum_{n=1}^{\infty} \left( \frac{3n}{5n + 2} \right)^n
$$

We determine whether this series converges or diverges. Each term has the form $a_n = (\text{expression})^n$, so the root test applies and is simpler than other methods.

- - -

We define the [sequence](../sequences/):

$$
a_n = \left( \frac{3n}{5n + 2} \right)^n
$$

To apply the root test, we evaluate the limit superior of the $n$-th root of $a_n$:

$$
\limsup_{n \to \infty} \sqrt[n]{a_n} = \lim_{n \to \infty} \left( \frac{3n}{5n + 2} \right)
$$

Since the terms are positive, we omit the absolute value and simplify:

$$
\frac{3n}{5n + 2} = \frac{3}{5 + \frac{2}{n}} \longrightarrow \frac{3}{5} \quad \text{as } n \to \infty
$$

Therefore, we find:

$$
\limsup_{n \to \infty} \sqrt[n]{a_n} = \frac{3}{5} < 1
$$

Since the limit is less than $1$, the root test tells us that the series converges absolutely.

- - -

A trigonometric factor raised to the $n$-th power leads to the same kind of computation. We study the series:

$$
\sum_{n=1}^{\infty} \left( \frac{n}{3} \tan \frac{1}{n} \right)^n
$$

The terms are positive for every $n \geq 1$, and the whole expression is raised to the power $n$, so the root test is the natural choice. Taking the $n$-th root removes the outer exponent:

$$
\sqrt[n]{a_n} = \frac{n}{3} \tan \frac{1}{n}
$$

As $n \to \infty$ the argument $\frac{1}{n}$ tends to zero, where $\tan \frac{1}{n} \sim \frac{1}{n}$ is a [remarkable limit](../remarkable-limits/). The limit of the root is therefore:

$$
\lim_{n \to \infty} \frac{n}{3} \tan \frac{1}{n} = \lim_{n \to \infty} \frac{n}{3} \cdot \frac{1}{n} = \frac{1}{3}
$$

Since the limit equals $\frac{1}{3} < 1$, the series converges.