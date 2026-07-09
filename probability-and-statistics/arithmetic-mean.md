---
title: Arithmetic Mean
source: https://algebrica.org/arithmetic-mean/
license: CC BY-NC 4.0
tags:
  - arithmetic-mean
  - expected-value
  - geometric-mean
  - harmonic-mean
  - mean
  - statistics
  - weighted-mean
---
## Definition

The arithmetic mean is the most common average, and it belongs to the family of power means. For a data set it is the total sum of the observations divided by their [number](../types-of-numbers/). It is based on additive aggregation, so it fits quantities that combine linearly, such as raw measurements or values that do not grow proportionally or [exponentially](../exponential-function/). The arithmetic mean is the equilibrium point of the distribution, the value around which the data balance.

For the values $x_1, x_2, \dots, x_n$, the arithmetic mean is:

$$M_a = \frac{1}{n}\sum_{i=1}^{n} x_i$$

Here $n$ is the number of elements.

+ The arithmetic mean applies to any set of [real numbers](../types-of-numbers/), including negative values and zero.
+ It is sensitive to extreme values, so outliers can distort it, and other means such as the median or [geometric mean](../geometric-mean/) are more suitable in some cases.

## Example 1

The following data set has five values.

| $x_i$ | Value |
|---|---|
| $x_1$ | 7.2 |
| $x_2$ | 4.8 |
| $x_3$ | 9.1 |
| $x_4$ | 5.5 |
| $x_5$ | 6.4 |

With $n=5$, substituting the values gives:

$$M_a = \frac{7.2 + 4.8 + 9.1 + 5.5 + 6.4}{5} = \frac{33.0}{5} = 6.6$$

The arithmetic mean of the data set is $M_a=6.6$.

## Algebraic properties

Shifts, scalings, and the merging of data sets change the arithmetic mean in ways that follow directly from the definition.

The deviations of the values from their mean sum to zero. Since $\sum_{i=1}^{n} x_i = nM_a$,

$$\sum_{i=1}^{n} (x_i - M_a) = \sum_{i=1}^{n} x_i - nM_a = nM_a - nM_a = 0$$

The positive and negative deviations cancel, so $M_a$ is the value that balances the data. Adding a constant $c$ to every value shifts the mean by the same constant, since the constant factors out of the sum:

$$\frac{1}{n}\sum_{i=1}^{n} (x_i + c) = \frac{1}{n}\sum_{i=1}^{n} x_i + c = M_a + c$$

Multiplying every value by a constant $c$ multiplies the mean by $c$, since the factor comes out of the sum:

$$\frac{1}{n}\sum_{i=1}^{n} cx_i = c\cdot\frac{1}{n}\sum_{i=1}^{n} x_i = cM_a$$

The two rules combine into a single linear rule. For the transformed values $y_i = ax_i + b$ the mean is $aM_a + b$, so a change of unit or origin transforms the mean the same way it transforms each observation. The mean of a merged data set is the weighted mean of the partial means. For a first group of $n_1$ values with mean $M_1$ and a second group of $n_2$ values with mean $M_2$, the combined mean has all $n_1 + n_2$ values in its numerator:

$$M_c = \frac{n_1M_1 + n_2M_2}{n_1 + n_2}$$

The group sizes are the weights, which connects the pooling of data sets to the weighted arithmetic mean developed in the next section.

## Weighted arithmetic mean

When the data points do not contribute equally, each observation $x_i$ has a weight $w_i$ set by its importance or frequency. The weighted arithmetic mean is:

$$M_{aw} = \frac{\sum_{i=1}^{n} w_i x_i}{\sum_{i=1}^{n} w_i}$$

Here $x_i$ are the observed values and $w_i>0$ are their weights.

+ The weighted arithmetic mean generalizes the simple arithmetic mean through the weights $w_i$.
+ Observations with larger weights have a stronger influence on the result.
+ When all weights are equal, the weighted arithmetic mean reduces to the simple arithmetic mean.

## Example 2

A company computes the weighted arithmetic mean of its monthly sales. Each month has a different number of working days, and these counts are the weights.

| Month | $x_i$ = daily sales in dollars | $w_i$ = working days |
|:---:|:---:|:---:|
| January | 420 | 20 |
| February | 380 | 22 |
| March | 460 | 18 |
| April | 400 | 21 |
| May | 440 | 19 |

Substituting into the formula gives:

$$
\begin{align}
M_{aw} &= \frac{(420 \times 20) + (380 \times 22) + (460 \times 18) + (400 \times 21) + (440 \times 19)}{20 + 22 + 18 + 21 + 19} \\[6pt]
&= \frac{8400 + 8360 + 8280 + 8400 + 8360}{100} \\[6pt]
&= \frac{41800}{100} \\[12pt]
&= 418
\end{align}
$$

The weighted arithmetic mean of the company's sales is $M_{aw}=418$ dollars per day.

## The Pythagorean means and the mean inequality

The arithmetic mean is one of the three Pythagorean means, together with the [geometric mean](../geometric-mean/) and the [harmonic mean](../harmonic-mean/). For positive values $x_1, \dots, x_n$ the geometric mean is the $n$-th root of the product, and the harmonic mean is the reciprocal of the average of the reciprocals:

$$G = \left( \prod_{i=1}^{n} x_i \right)^{\frac{1}{n}} \qquad H = \frac{n}{\sum_{i=1}^{n} \frac{1}{x_i}}$$

Each of the three is the [power mean](../introduction-to-the-mean/) of the same values for a different exponent, with the arithmetic mean at exponent $1$, the geometric mean in the limit at exponent $0$, and the harmonic mean at exponent $-1$. For positive values the three means satisfy the chain

$$H \le G \le M_a$$

with equality throughout only when all the values coincide. Both inequalities already hold for a pair of positive numbers $a$ and $b$, and the general case follows from the same argument applied to the power mean. The inequality $M_a \ge G$ rests on the square of a difference of square roots. Since a square is nonnegative,

$$(\sqrt{a} - \sqrt{b})^2 \ge 0$$

Expanding the square gives $a - 2\sqrt{ab} + b \ge 0$, and rearranging the terms yields:

$$\frac{a + b}{2} \ge \sqrt{ab}$$

The left side is the arithmetic mean of $a$ and $b$ and the right side is their geometric mean, so $M_a \ge G$, with equality when $a = b$. The inequality $G \ge H$ follows from the same idea applied to the reciprocals. Since a square is nonnegative,

$$\left( \frac{1}{\sqrt{a}} - \frac{1}{\sqrt{b}} \right)^2 \ge 0$$

Expanding and rearranging gives $\frac{1}{a} + \frac{1}{b} \ge \frac{2}{\sqrt{ab}}$, and taking reciprocals of both sides yields:

$$\sqrt{ab} \ge \frac{2}{\frac{1}{a} + \frac{1}{b}}$$

The left side is the geometric mean of $a$ and $b$ and the right side is their harmonic mean, so $G \ge H$, again with equality when $a = b$. The two results combine into the full chain $H \le G \le M_a$.

## The sample mean and the population mean

When the data are a sample drawn from a larger population, the arithmetic mean of the sample estimates the mean of the whole population. The population mean is the [expected value](../mean-or-expected-value-of-a-random-variable/) of the underlying distribution. For a [discrete random variable](../discrete-random-variables/) it is the sum of the possible values weighted by their probabilities:

$$\mu = E(X) = \sum_x xf(x)$$

For a [continuous random variable](../continuous-random-variables/) the sum becomes an integral of the values weighted by the probability density over the whole range:

$$\mu = E(X) = \int_{-\infty}^{+\infty} xf(x) \ dx$$

The arithmetic mean computed from the sample is the [sample mean](../sampling-distributions/), and it is the natural estimator of $\mu$.

Suppose the sample has $n$ independent observations $X_1, \dots, X_n$, each drawn from a distribution with mean $\mu$ and variance $\sigma^2$. The sample mean is the random variable

$$\overline{X} = \frac{1}{n} \sum_{i=1}^{n} X_i$$

Its expected value equals the population mean, because expectation is linear:

$$E(\overline{X}) = \frac{1}{n} \sum_{i=1}^{n} E(X_i) = \frac{1}{n}\cdot n\mu = \mu$$

An estimator whose expected value equals the quantity it estimates is unbiased, so the sample mean is an unbiased estimator of the population mean.

The spread of the sample mean around $\mu$ shrinks as the sample grows. Because the observations are independent, the variance of their sum is the sum of the variances, and the factor $\frac{1}{n}$ comes out squared:

$$\mathrm{var}(\overline{X}) = \frac{1}{n^2} \sum_{i=1}^{n} \mathrm{var}(X_i) = \frac{1}{n^2}\cdot n\sigma^2 = \frac{\sigma^2}{n}$$

The variance of the sample mean is the population variance divided by the sample size, so it does not depend on the shape of the distribution, and a larger sample concentrates the estimate more tightly around $\mu$.

> The identity $\mathrm{var}(\overline{X}) = \sigma^2/n$ assumes independent observations with a common variance. Correlation between the observations changes the variance of the mean.

- - -

For a large sample the distribution of $\overline{X}$ is close to normal, while for a small sample from a normal population the standardized sample mean follows Student's $t$-distribution. An estimator with smaller variance is more efficient, and for a normal population the sample mean is more efficient than the sample median, because the variance of the median is larger than that of the mean by a factor of about $\pi/2$. The mean is therefore the more precise summary of the center when the data are close to normal.

For a moderately skewed distribution the mean, the median, and the mode satisfy an approximate relation:

$$\text{mean} - \text{mode} \approx 3(\text{mean} - \text{median})$$

The mean lies farthest from the peak in the direction of the longer tail, so a gap between the mean and the median measures the skewness of the data.
