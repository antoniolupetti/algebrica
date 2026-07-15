---
title: Variance
source: https://algebrica.org/variance/
license: CC BY-NC 4.0
tags:
  - dispersion
  - mean-deviations
  - quadratic-mean
  - random-variables
  - sample-variance
  - standard-deviation
  - statistics
  - variance
---

## Mean deviations

The [mean](../introduction-to-the-mean/) alone cannot describe a set of observations completely. A full description requires knowing how the observations spread around it, that is, how far each value lies from the center. The mean deviations measure this spread, and their general form is:

$$
{}^sS_M =
\left[
\frac{\sum_{i=1}^{n} \left| x_i - M \right|^s}{n}
\right]^{1/s}
$$

In this expression $M$ is the reference mean around which the deviations are measured, and the exponent $s$ is the order of the corresponding [power mean](../introduction-to-the-mean/).

For $s = 1$ the formula gives the mean absolute deviation, the arithmetic mean of the [absolute values](../absolute-value/) $|x_i - M|$ of the deviations. Among all reference values, the [median](../median-and-quantiles/) makes this deviation smallest.

For $s = 2$ the formula gives the quadratic mean deviation, the [root mean square](../root-mean-square/) of the deviations. It is the [square root](../radicals/) of the ratio between the sum of the squared deviations, known as the deviance, and the number of observations:

$$
{}^2S =
\sqrt{
\frac{\sum_{i=1}^{n}(x_i - M)^2}{n}
}
$$

Here $x_i$ is the $i$-th observation and $M$ is the reference mean, typically the [arithmetic mean](../arithmetic-mean/).

## Example 1

We compute the quadratic mean deviation of five observed values:

| $X_i$ | Observation |
|:--------:|:------------:|
| $x_1$ | 3 |
| $x_2$ | 5 |
| $x_3$ | 7 |
| $x_4$ | 10 |
| $x_5$ | 15 |

The [arithmetic mean](../arithmetic-mean/) of the observations is:

$$
M = \frac{3 + 5 + 7 + 10 + 15}{5} = \frac{40}{5} = 8
$$

We square the deviation of each observation from the mean, so that positive and negative deviations cannot cancel and the larger ones carry more weight:

| $x_i$ | $x_i - M$ | $(x_i - M)^2$ |
|:--------:|:----------------:|:--------------------:|
| 3 | -5 | 25 |
| 5 | -3 | 9 |
| 7 | -1 | 1 |
| 10 | 2 | 4 |
| 15 | 7 | 49 |

The sum of the squared deviations is:

$$
\sum (x_i - M)^2 = 25 + 9 + 1 + 4 + 49 = 88
$$

Dividing this sum by the number of observations and taking the square root gives:

$$
{}^2S = \sqrt{ \frac{ \sum (x_i - M)^2 }{n} } =
\sqrt{ \frac{88}{5} } = \sqrt{17.6} \approx 4.195
$$

The quadratic mean deviation is therefore ${}^2S \approx 4.20,$ and the observations differ from the mean by about $4.2$ units on average.

## Variance

The square of the quadratic mean deviation is called the variance. It is the mean of the squared differences between each observation and a reference value $M,$ and it measures how widely the data are dispersed around that point. The quadratic mean deviation has the same unit as the data, while the variance has squared units. Its expression is:

$$
\sigma^2 = \frac{\sum_{i=1}^{n}(x_i - M)^2}{n}
$$

The square root $\sigma$ of the variance is called the standard deviation. It restores the unit of the data and coincides with the quadratic mean deviation ${}^2S$ when $M$ is the arithmetic mean.

When the data form a frequency distribution, each distinct value $x_i$ appears with frequency $n_i$ and the variance has the weighted form:

$$
\sigma^2 = \frac{\sum_{i=1}^{k}(x_i - M)^2 n_i}{N}
$$

Here $k$ is the number of distinct values and $N = n_1 + n_2 + \ldots + n_k$ is the total number of observations.

+ When $\sigma^2 = 0,$ every observation coincides with $M$ and the data show no dispersion.
+ When $\sigma^2 = 1,$ the squared deviations from $M$ have mean one and the standard deviation equals one unit.
+ Adding the same constant to every observation leaves the variance unchanged.
+ Multiplying every observation by a constant $a$ multiplies the variance by $a^2.$
+ The larger the variance, the wider the spread of the data around $M.$

- - -

A more compact expression for the variance follows from [expanding the square](../notable-products/) in its definition:

$$
(x_i - M)^2 = x_i^2 - 2Mx_i + M^2
$$

Substituting this expansion into the definition, we obtain:

$$
\sigma^2 = \frac{\sum_{i=1}^{n}x_i^2 - 2M\sum_{i=1}^{n}x_i + nM^2}{n}
$$

Since the mean is $M = \frac{\sum_{i=1}^{n}x_i}{n},$ substituting it into the middle term gives:

$$
\sigma^2 = \frac{\sum_{i=1}^{n}x_i^2}{n} - 2M^2 + M^2
$$

The two terms in $M^2$ combine and the expression reduces to:

$$
\sigma^2 = \frac{\sum_{i=1}^{n}x_i^2}{n} - M^2
$$

The first term is the mean of the squared observations, written $M(x^2),$ so the variance has the compact form:

$$
\sigma^2 = M(x^2) - M^2
$$

The variance is the mean of the squares minus the square of the mean.

## Example 2

We now compute the variance of five observations, obtained from those of Example 1 by adding $2$ to each value:

| $X_i$ | Observation |
|:--------:|:------------:|
| $x_1$ | 5 |
| $x_2$ | 7 |
| $x_3$ | 9 |
| $x_4$ | 12 |
| $x_5$ | 17 |

Summing the values and dividing by their number gives the mean, which increases by the same constant:

$$
M = \frac{5 + 7 + 9 + 12 + 17}{5} = \frac{50}{5} = 10
$$

Since every observation and the mean shift by the same amount, the deviations $x_i - M$ coincide with those of Example 1:

| $x_i$ | $x_i - M$ | $(x_i - M)^2$ |
|:--------:|:------------:|:----------------:|
| 5 | -5 | 25 |
| 7 | -3 | 9 |
| 9 | -1 | 1 |
| 12 | 2 | 4 |
| 17 | 7 | 49 |

Adding the squared deviations gives:

$$
\sum (x_i - M)^2 = 25 + 9 + 1 + 4 + 49 = 88
$$

Dividing this total by the number of observations, we obtain the variance:

$$
\sigma^2 = \frac{88}{5} = 17.6
$$

The variance equals the square of the quadratic mean deviation found in Example 1, and the shift by $2$ has left it unchanged, in agreement with the property stated above.

## Example 3

The compact formula $\sigma^2 = M(x^2) - M^2$ shortens the computation when the sum of the values and the sum of their squares are already available. Consider the following observations:

| $X_i$ | Observation |
|:--------:|:------------:|
| $x_1$ | 3 |
| $x_2$ | 9 |
| $x_3$ | 11 |
| $x_4$ | 14 |

The mean of the observations is:

$$
M = \frac{3 + 9 + 11 + 14}{4} = \frac{37}{4} = 9.25
$$

The mean of the squared observations is:

$$
\begin{align}
M(x^2) &= \frac{3^2 + 9^2 + 11^2 + 14^2}{4} \\[6pt]
       &= \frac{9 + 81 + 121 + 196}{4} \\[6pt]
       &= \frac{407}{4} = 101.75
\end{align}
$$

Substituting both values into the compact formula gives:

$$
\sigma^2 = M(x^2) - M^2 = 101.75 - (9.25)^2 = 101.75 - 85.5625 = 16.1875
$$

The variance of the observations is therefore $\sigma^2 \approx 16.19.$

## Variance of discrete and continuous random variables

For [discrete random variables](../discrete-random-variables/), the [variance](../variance-and-covariance-of-a-random-variable/) is defined through the [expected value](../mean-or-expected-value-of-a-random-variable/):

$$
\sigma^2 = E[(X - \mu)^2] = \sum_x (x - \mu)^2 f(x)
$$

Here $x$ denotes each value that the random variable $X$ can assume, $\mu = E[X]$ is the expected value, or theoretical mean, of the variable, and $f(x)$ is the probability mass function, which assigns a probability to each possible outcome of $X.$

- - -

For [continuous random variables](../continuous-random-variables/), the sum is replaced by an [improper integral](../improper-integrals/) over the whole real line:

$$
\sigma^2 = E[(X - \mu)^2] = \int_{-\infty}^{+\infty} (x - \mu)^2 f(x) \ dx
$$

Here $f(x)$ is the probability density function, which describes how the probability is distributed over the values of $X.$

In both cases, expanding the square and applying the linearity of the expected value yields the compact form:

$$
\sigma^2 = E[X^2] - \mu^2
$$

This identity is the analogue for random variables of the relation $\sigma^2 = M(x^2) - M^2$ obtained for observed data, and it shortens the computation in the same way.

## Variance of a sampling distribution

The [sample variance](../sampling-distributions/) measures how the data in a sample spread around the sample mean. Given random variables $X_1, X_2, \ldots, X_n,$ it is defined as:

$$
S^2 = \frac{1}{n - 1} \sum_{i=1}^{n} (X_i - \overline{X})^2
$$

where $\overline{X}$ is the sample mean and $n$ is the sample size.

> The divisor is $n - 1$ rather than $n$ because the deviations are measured from $\overline{X}$ instead of the population mean; this correction makes $S^2$ an unbiased estimator of the [population variance](../variance-and-covariance-of-a-random-variable/).
