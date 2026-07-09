---
title: Introduction to the Mean
source: https://algebrica.org/introduction-to-the-mean/
license: CC BY-NC 4.0
tags:
  - arithmetic-mean
  - expected-value
  - geometric-mean
  - harmonic-mean
  - mean
  - statistics
---
## The central behavior of a data distribution

The mean condenses a collection of observations into a single value that reflects the typical level around which the data are distributed. It marks the balance point of the data, and it supports many methods of descriptive and inferential analysis.

A general formulation of the mean was proposed by Oscar Chisini in 1929. By his definition, the mean of a set of numerical values is the number $M$ that, when substituted for each observation in a symmetric [function](../functions/) $F$, leaves the overall result unchanged:

$$F(x_1, x_2, \dots, x_n) = F(M, M, \dots, M)$$

> A function is symmetric when the order of the data does not matter, since it depends only on the values themselves, not on their arrangement.

- - -

This definition unifies the different types of means, such as the [arithmetic](../arithmetic-mean/), [geometric](../geometric-mean/), and [harmonic mean](../harmonic-mean/) within a single framework. Each specific mean is obtained by choosing a particular function $F$ that describes the relationship among the data values. When $F$ is the sum of all data values, that is:

$$F(x_1, x_2, \dots, x_n) = x_1 + x_2 + \dots + x_n$$

the general expression becomes:

$$x_1 + x_2 + \dots + x_n = nM$$

From this relation, we obtain the formula of the [arithmetic mean](../arithmetic-mean/):

$$M = \frac{x_1 + x_2 + \dots + x_n}{n} = \frac{1}{n} \sum_{i=1}^{n} x_i$$

## The mean as the minimum substitution error

A second definition of the mean is due to Abraham Wald, who connected the mean with the substitution error. The mean is the value that minimizes the total error produced when all data points are replaced by a single representative number, the point that yields the smallest discrepancy between the observed values and their common substitute. This is written as:

$$M = \arg\min_{\mu} \sum_{i=1}^{n} (x_i - \mu)^2$$

The value $\mu$ that minimizes this expression is the arithmetic mean, which balances the squared deviations of the data.

## Hölder mean

The Hölder mean, also known as the power mean or generalized mean, defines a family of means that includes the arithmetic, geometric, and harmonic mean as special cases. It is defined for positive values $x_1, x_2, \dots, x_n$ as:

$$M_s = \left( \frac{1}{n} \sum_{i=1}^{n} x_i^s \right)^{\frac{1}{s}}$$

For different values of $s$, the Hölder mean reproduces the main classical means.

+ For $s = 1$ it corresponds to the arithmetic mean.
+ For $s = 0$ it becomes the geometric mean.
+ For $s = -1$ it yields the harmonic mean.
+ For $s = 2$ it represents the quadratic mean.

## List of the main means

The table below collects the classical means in both their simple and weighted forms, each obtained from the Hölder mean for a particular value of $s$.

[class="table-1 -right"]

| | |
|---|---|
| $$M_1 = \frac{1}{n} \sum_{i=1}^{n} x_i$$ | [more](../arithmetic-mean/) |
| $$M_1 = \frac{\sum_{i=1}^{n} w_i x_i}{\sum_{i=1}^{n} w_i}$$ | [more](../arithmetic-mean/) |
| $$M_0 = \left( \prod_{i=1}^{n} x_i \right)^{\frac{1}{n}}$$ | [more](../geometric-mean/) |
| $$M_0 = \left( \prod_{i=1}^{n} x_i^{w_i} \right)^{\frac{1}{\sum_{i=1}^{n} w_i}}$$ | [more](../geometric-mean/) |
| $$M_{-1} = \frac{n}{\sum_{i=1}^{n} \frac{1}{x_i}}$$ | [more](../harmonic-mean/) |
| $$M_2 = \left( \frac{1}{n} \sum_{i=1}^{n} x_i^2 \right)^{\frac{1}{2}}$$ | [more](../root-mean-square/) |
[/class]

Each formula summarizes a collection of values in a specific way, depending on how the individual values contribute to the final result. All means describe central tendency, and their interpretation varies with the mathematical operation that defines them.

+ [Arithmetic mean](../arithmetic-mean/) ($M_1$): used when values combine additively, such as totals of quantities like income, length, or temperature. It expresses the point of balance of the data, where each observation contributes equally to the result.

+ [Weighted arithmetic mean](../arithmetic-mean/) ($M_1$ weighted): applied when some data points have more relevance or occur more frequently than others. Each observation is multiplied by a weight that reflects its importance before computing the average.

+ [Geometric mean](../geometric-mean/) ($M_0$): suitable for quantities that combine multiplicatively, such as growth factors, returns, or indices. It describes the representative rate of change over time, showing how values scale proportionally.

+ [Weighted geometric mean](../geometric-mean/) ($M_0$ weighted): used when multiplicative data have different levels of importance, as in finance or performance analysis, where certain elements influence the result more than others.

+ [Harmonic mean](../harmonic-mean/) ($M_{-1}$): appropriate for averaging rates, speeds, or ratios where smaller values should weigh more. It reflects the true mean rate when the total distance, quantity, or workload remains constant.

+ [Quadratic mean](../root-mean-square/) ($M_2$): chosen when values combine quadratically, as with voltages, accelerations, or power. It gives greater influence to larger variations, so it reports the effective magnitude of the data.

## Mean or expected value of a random variable

For [discrete random variables](../discrete-random-variables/), the mean or [expected value](../mean-or-expected-value-of-a-random-variable/) is the sum of all possible values of $X$ weighted by their probabilities:

$$\mu = E(X) = \sum_x xf(x)$$

For [continuous random variables](../continuous-random-variables/), the mean is obtained by integrating each possible value of $X$ weighted by its probability density over the entire range:

$$\mu = E(X) = \int_{-\infty}^{+\infty} xf(x) \ dx$$

> Both forms express the same idea, the mean reflects where the values of a random variable tend to cluster. In the discrete case it is found by summing over all possible outcomes, while in the continuous case the same principle extends through integration.

## Mean of a sampling distribution

The [sample mean](../sampling-distributions/) is the average value of the observations in a sample drawn from a population, and it estimates the population mean. It is defined as:

$$\overline{X} = \frac{1}{n} \sum_{i=1}^{n} X_i$$

where $\overline{X}$ is the sample mean, $n$ is the sample size, and $X_i$ is the value of the $i$-th observation in the sample.
