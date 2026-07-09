---
title: Geometric Mean
source: https://algebrica.org/geometric-mean/
license: CC BY-NC 4.0
tags:
  - geometric-mean
  - means
  - power-means
  - statistics
---

## Definition

The geometric mean is one of the [power means](../introduction-to-the-mean/). Unlike the [arithmetic mean](../arithmetic-mean/), it is based on the product of the elements rather than their sum, so it is suitable for average growth rates, returns over time, and quantities that vary multiplicatively. When data changes through proportional or percentage steps, the geometric mean describes its central tendency more accurately than the arithmetic mean.

In its general form, the geometric mean is:

$$M_g = \left( \prod_{i=1}^{n} x_i \right)^{\frac{1}{n}}$$

In this expression $x_1, x_2, \dots, x_n$ are positive values and $n$ is the number of elements.

+ The geometric mean is defined only for sets of positive values, because it multiplies the elements and extracts a [root](../radicals/).
+ Because it has a multiplicative structure, the geometric mean is tied to [exponential growth](../exponential-function/).
+ The geometric mean is always less than or equal to the arithmetic mean.

> For two positive numbers $a$ and $b,$ the formula reduces to $\sqrt{ab},$ the side length of a square with the same area as a rectangle with sides $a$ and $b.$ The name comes from this construction.

## Logarithmic form

Taking [logarithms](../logarithms/) gives a second expression for the geometric mean of positive values $x_1, x_2, \ldots, x_n$:

$$M_g = \exp\left(\frac{1}{n} \sum_{i=1}^{n} \ln x_i \right)$$

+ Logarithms turn products into sums and exponents into multipliers, which simplifies the computation.
+ The formula shows that the geometric mean is the exponential of the [arithmetic mean](../arithmetic-mean/) of the logarithms of the data.
+ The logarithmic form is convenient for numbers that span several orders of magnitude, or when the product is too large or too small for floating-point arithmetic.

## Example 1

Consider the following set of five positive values:

| $x_i$ | Value |
|:-------:|:-------:|
| $x_1$ | 2.0 |
| $x_2$ | 3.5 |
| $x_3$ | 4.0 |
| $x_4$ | 5.5 |
| $x_5$ | 6.0 |

Here $n = 5$. Substituting the values, we get:

$$M_g = (2.0 \times 3.5 \times 4.0 \times 5.5 \times 6.0)^{\frac{1}{5}}$$

$$M_g = (924)^{\frac{1}{5}} \approx 3.92$$

The geometric mean of this set is therefore approximately $3.92$.

> The arithmetic mean of these numbers is $(2.0 + 3.5 + 4.0 + 5.5 + 6.0)/5 = 4.2$. The geometric mean is lower ($3.92$) because it gives less weight to the larger values.


## Example 2

The average return of a stock over a period is a standard application of the geometric mean. In finance, returns combine multiplicatively, and each month's performance compounds with the previous ones. The geometric mean accounts for this compounding, so it measures average growth more accurately than the arithmetic mean.

We calculate the geometric mean of Tesla's monthly returns for the first five months of 2025 to estimate its average monthly performance across the period.

| Month (2025) | Return |
|:--------------|:-------:|
| January | +12.4% |
| February | -3.8% |
| March | +7.6% |
| April | +2.1% |
| May | +4.5% |

With percentage returns, each return $x_i$ is first converted into a growth factor by adding $1$, giving $1 + x_i$. These factors are multiplied, the $n$-th root is taken, and $1$ is subtracted to return to percentage form.

$$M_g = \left[ \prod_{i=1}^{n} (1 + x_i) \right]^{\frac{1}{n}} - 1$$

For the five months, we obtain:

$$
\begin{align}
M_g &= \left[(1.124) \times (0.962) \times (1.076) \times (1.021) \times (1.045)\right]^{\tfrac{1}{5}} - 1 \\[6pt]
&= 1.0442 - 1 \\[6pt]
&= 0.0442 \\[6pt]
&= 4.42\%
\end{align}
$$

The average monthly return of Tesla's stock over these five months was therefore approximately $4.4\%$.

## Weighted geometric mean

When data points do not contribute equally, each observation $x_i$ has a weight $w_i$ chosen according to its importance or frequency. The weighted geometric mean is defined as:

$$M_{gw} = \left( \prod_{i=1}^{n} x_i^{w_i} \right)^{\frac{1}{\sum_{i=1}^{n} w_i}}$$

In this expression $x_i > 0$ are the observed values and $w_i > 0$ are their weights.

+ The weighted geometric mean generalizes the simple geometric mean through the weights $w_i$.
+ Larger or more relevant observations have a stronger influence on the result.
+ When all weights are equal, the weighted geometric mean reduces to the simple geometric mean.

## Example 3

Consider the same Tesla data, now with weights chosen as described in the note.

| Month | Return | Weight |
|:--------|:-----------:|:----------------|
| January | +12.4% | 3 |
| February | -3.8% | 1 |
| March | +7.6% | 2 |
| April | +2.1% | 1 |
| May | +4.5% | 3 |

> January is a strong growth month and has a high weight. February is negative and has a low weight. March is a partial recovery and has a medium weight. April is stable and has a low weight. May is positive and has a high weight.

Using the growth factors $(1 + x_i)$ and the weights $w_i$, we obtain:

$$
\begin{align}
M_{gw} &= \left[(1.124)^3 \times (0.962)^1 \times (1.076)^2 \times (1.021)^1 \times (1.045)^3\right]^{\tfrac{1}{10}} - 1 \\[6pt]
&= (1.8428)^{0.1} - 1 \\[6pt]
&= 1.0630 - 1 \\[6pt]
&= 0.0630 \\[6pt]
&= 6.30\%
\end{align}
$$

> The exponent $\tfrac{1}{10}$ is the reciprocal of the sum of the weights. Since $w_i = \{\ 3, 1, 2, 1, 3\ \}$, their total is $\sum w_i = 10$.

With these weights, Tesla's weighted average monthly return over the five months is approximately $6.3\%$, above the unweighted value because the months with positive performance have more weight.

## Geometric mean of a continuous function

The logarithmic form extends from a finite set to a positive [continuous function](../continuous-functions/) $f$ on an [interval](../intervals/) $[a, b]$, with the sum replaced by a [definite integral](../definite-integrals/):

$$M_g = \exp\left( \frac{1}{b-a} \int_a^b \ln f(x) \ dx \right)$$

The factor $\frac{1}{b-a}$ replaces $\frac{1}{n}$ and averages $\ln f$ over the interval rather than over a finite set of points. The exponential then returns the average to the original scale of $f$.

As an example, take $f(x) = x$ on $[1, e]$. The integral of the logarithm, found by [integration by parts](../integration-by-parts/), is:

$$\int_1^e \ln x \ dx = \left[ x\ln x - x \right]_1^e = 1$$

Dividing by the length $e - 1$ and applying the exponential gives:

$$M_g = \exp\left( \frac{1}{e-1} \right) \approx 1.79$$

The geometric mean of $f(x) = x$ over $[1, e]$ is therefore approximately $1.79$.
