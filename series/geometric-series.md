---
title: Geometric Series
source: https://algebrica.org/geometric-series/
license: CC BY-NC 4.0
tags:
  - common-ratio
  - convergence
  - geometric-series
  - series
---
## Definition

A geometric series is based on a [geometric sequence](../geometric-sequence/), where each term is obtained by multiplying the previous term by a constant ratio. It is defined as the following sum:

$$
\sum_{n=0}^{\infty} r^n
$$

The value $r$ is the constant factor used to multiply each term to produce the next. If $r = 0$, the series converges to $1$, because all subsequent terms are zero:
$$
\sum_{n=0}^{\infty} 0^n = 1 + 0 + 0 + \dots = 1
$$

If $r = 1$, the series diverges, because the sequence of partial sums grows without bound:

$$
s_n = 1 + 1 + \dots + 1 = n + 1 \quad \rightarrow \quad \lim_{n \to \infty} s_n = \infty
$$

The geometric series serves as a reference model for analyzing more complex series, because its behavior is well understood and defined. For [series with positive terms](../series-with-positive-terms/), it is used in comparison tests to determine convergence or divergence. If a given series can be bounded above or below by a geometric series, we can often deduce the nature of the series by analogy.

- - -

The $n$-th partial sum of a geometric [series](../series/) with $r \ne 0$ and $r \ne 1$ is given by:

$$
S_n = \sum_{k=0}^{n} r^k = \frac{1 - r^{n+1}}{1 - r}
$$

This result is obtained starting from:

$$
s_n = 1 + r + r^2 + r^3 + \dots + r^n
$$

Multiplying both sides by $r$, we get:

$$
\begin{align}
r \cdot s_n &= r(1 + r + r^2 + \dots + r^n) \\[6pt]
&= r + r^2 + r^3 + \dots + r^n + r^{n+1} \\[6pt]
&= 1+ r + r^2 + r^3 + \dots + r^n + r^{n+1} -1 \\[6pt]
\end{align}
$$

In the last term of the equation, we added and subtracted $+1$. This way, the expression from $1 + \dots + r^n$ becomes $s_n$. By substituting the values, we obtain:

$$
\begin{align}
r \cdot s_n &= s_n + r^{n+1} - 1 \\[6pt]
s_n (1 - r) &= 1 - r^{n+1}
\end{align}
$$

and finally:

$$
s_n = \frac{1 - r^{n+1}}{1 - r} \quad \text{for } r \ne 1
$$

> The condition $r \ne 1$ is essential; otherwise, the denominator becomes zero and the formula is undefined.

- - -

When $|r| < 1$ the geometric series converges, because the terms decrease in absolute value. The infinite sum is computed using the formula:

$$
\sum_{n=0}^{\infty} r^n = \frac{1}{1 - r}
$$

This result holds because $\lim_{n \to \infty} r^{n+1} = 0$ when $|r| < 1$, which simplifies the formula for the partial sum:

$$
s_n = \frac{1 - r^{n+1}}{1 - r} \quad \rightarrow \quad \lim_{n \to \infty} s_n = \frac{1}{1 - r}
$$

A geometric series may have a first term different from $1$. Multiplying every term by a constant $a$ gives the general form:

$$
\sum_{n=0}^{\infty} ar^n = a + ar + ar^2 + \dots
$$

The constant $a$ factors out of the sum, so the partial sum follows from the case with first term $1$:

$$
S_n = a\frac{1 - r^{n+1}}{1 - r}
$$

When $|r| < 1$ the series converges, and its sum is:

$$
\sum_{n=0}^{\infty} ar^n = \frac{a}{1 - r}
$$

A nonzero constant $a$ scales every term by the same factor, so it changes the value of the limit but not whether the series converges. In general, when the index starts at a value $n > 0$, for example $\alpha$, the formula for the sum of the geometric series becomes:

$$
\sum_{n=\alpha}^{\infty} r^n = \frac{r^{\alpha}}{1 - r}
$$

- - -

When $r > 1$ the geometric series diverges, because the terms $r^n$ grow without bound as $n \to \infty$, and so does the sequence of partial sums:

$$
\lim_{n \to \infty} s_n = \lim_{n \to \infty} \sum_{k=0}^{n} r^k = \infty
$$

Since the terms do not tend to zero and their sum grows without bound, the series does not have a finite limit and therefore diverges.

- - -

When $r \leq -1$ the limit of $s_n$ does not exist, and the series is indeterminate. The terms $r^n$ alternate in sign and grow in magnitude, so the partial sums $s_n$ oscillate without approaching any finite value, and the series neither converges nor diverges to infinity. For example, if $r = -2$, the terms become:

$$
1 - 2 + 4 - 8 + 16 - \dots
$$

and the partial sums fluctuate without stabilizing.

A different behavior appears at the boundary $r = -1$, where the terms keep a constant magnitude instead of growing:

$$
1 - 1 + 1 - 1 + \dots
$$

The partial sums alternate between $1$ and $0$, so they stay bounded yet still fail to approach a single value. The series is indeterminate, like every case with $r \leq -1$.

- - -

Therefore, we can conclude that the series:

+ converges if $|r| < 1$ and its sum is $\dfrac{1}{1 - r}$ when the index starts at a value $n = 0$, or $\dfrac{r^\alpha}{1 - r}$ when the index starts at a value $n > 0$;
+ diverges to $+\infty$ if $r \geq 1$;
+ is indeterminate if $r \leq -1$.

## Relation to power series

Replacing the common ratio with a variable $x$ turns the geometric series into a [power series](../power-series/):

$$
\sum_{n=0}^{\infty} x^n = \frac{1}{1 - x} \quad \text{for } |x| < 1
$$

This is the simplest power series, the one whose coefficients are all equal to $1$, and the condition $|x| < 1$ gives it a radius of convergence equal to $1$. The same identity supports the ratio test and the [root test](../root-test-for-series-convergence/), which establish the convergence of a general series by comparing it to a geometric one.

## Example

We study the following geometric series and compute its sum.

$$\sum_{n=0}^{\infty} \frac{3^n + 4^n}{5^n}$$

By the linearity of summation, we can rewrite the series as the sum of two geometric series:

$$\sum_{n=0}^{\infty} \left( \frac{3}{5} \right)^n +  \sum_{n=0}^{\infty} \left( \frac{4}{5} \right)^n$$

The common ratio of both series is $< 1$, so by the properties of geometric series both converge. The sum of a geometric series is given by:

$$
\sum_{n=0}^{\infty} r^n = \frac{1}{1 - r}
$$

We have:

$$\sum_{n=0}^{\infty} \left( \frac{3}{5} \right)^n = \frac{1}{1 - \frac{3}{5}} = \frac{1}{\frac{2}{5}} = \frac{5}{2}$$

$$\sum_{n=0}^{\infty} \left( \frac{4}{5} \right)^n = \frac{1}{1 - \frac{4}{5}} = \frac{1}{\frac{1}{5}} = 5$$

By adding the two values, we obtain:

$$\frac{5}{2} + 5 = \frac{15}{2}$$

Therefore, the series converges and its sum is:
$$ \frac{15}{2} $$

## Repeating decimals

A decimal with an infinitely repeating pattern can be written as a geometric series, which turns it into a ratio of two integers. Consider the number $0.\overline{12} = 0.121212\dots$, where the block $12$ repeats without end. It can be expressed as:

$$
0.\overline{12} = \sum_{n=1}^{\infty} \frac{12}{100^n}
$$

This is a geometric series with first term $a=\frac{12}{100}$ and common ratio $r=\frac{1}{100}$. Since $|r| < 1$, the series converges, and applying the formula for the sum gives:

$$
0.\overline{12} = \frac{\frac{12}{100}}{1 - \frac{1}{100}} = \frac{\frac{12}{100}}{\frac{99}{100}} = \frac{12}{99} = \frac{4}{33}
$$

The same procedure rewrites any repeating decimal as a fraction, which shows that every such number is rational.