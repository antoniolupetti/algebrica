---
title: Mean or Expected Value of a Random Variable
source: https://algebrica.org/mean-or-expected-value-of-a-random-variable/
license: CC BY-NC 4.0
tags:
  - expected-value
  - mean
  - probability
  - random-variables
  - statistics
---

## The expected value of a random variable

The [mean](../introduction-to-the-mean/) is a statistical measure of the central tendency of a dataset, as is the [median](../median-and-quantiles/). It reduces an entire distribution to a single quantity, the point around which the values balance.

Among the main types of means are the [arithmetic mean](../arithmetic-mean/), the [geometric mean](../geometric-mean/), and the [harmonic mean](../harmonic-mean/), all used to summarize a finite set of numerical values. These measures describe the central tendency of observed data, and the same concept extends to [discrete random variables](../discrete-random-variables/) and [continuous random variables](../continuous-random-variables/).

Given a random variable $X$ on a probability space $(\Omega, \mathcal{F}, P),$ its mean, also called the expected value or mathematical expectation, is defined when $\int_{\Omega}|X(\omega)| \ dP(\omega) < +\infty.$ Its general expression is:

$$\mu = E(X) = \int_{\Omega} X(\omega) \ dP(\omega)$$

The expected value is the balance point of the distribution, but it need not be a possible value of $X$ or a point near which the outcomes concentrate. Its interpretation as a long-term average follows from the law of large numbers. If $X_1, X_2, \ldots$ are independent repetitions with the same distribution as $X,$ then:

$$\frac{X_1 + X_2 + \cdots + X_n}{n} \longrightarrow E(X) \quad \text{almost surely}$$

When $E[(X - E(X))^2]$ is finite, the dispersion of the outcomes around the expected value is measured by the [variance](../variance/).

- - -

For [discrete random variables](../discrete-random-variables/), the mean is defined as:

$$\mu = E(X) = \sum_x x f(x)$$

In this expression $x$ ranges over the possible values of $X,$ and $f(x)$ is the probability mass function, which assigns to each value its probability.

- - -

For continuous random variables, the mean is defined as:

$$\mu = E(X) = \int_{-\infty}^{+\infty} x f(x) \ dx$$

Here $f(x)$ is the probability density function of $X,$ and the [improper integral](../improper-integrals/) sums the contributions of all possible values of $x$ across the entire [real line](../real-numbers/).

> In both cases the mean is determined by the probability distribution itself. Instead of being calculated from a limited set of data points, it reflects the balance of all possible outcomes of $X,$ each contributing in proportion to its probability or density. The mean is finite precisely when $E(|X|) < +\infty.$ In the discrete case this condition is $\sum_x |x|f(x) < +\infty,$ while in the continuous case it is $\int_{-\infty}^{+\infty} |x|f(x) \ dx < +\infty.$ If the condition fails, $X$ has no finite mean.

## Properties of the expected value of a random variable

The expected value has several properties that follow from its definition. Suppose throughout this section that $X$ and $Y$ are integrable random variables. The monotonicity property states that if $X \ge Y$ almost surely, which means that the inequality fails only on an event of probability zero, then the same relation holds for their expected values:

$$E(X) \ge E(Y)$$

Expectation preserves order, and the mean of a larger quantity cannot be smaller than the mean of a smaller one.

- - -

Homogeneity with respect to constants describes the effect of a constant multiplier. When a random variable $X$ is multiplied by a real constant $c,$ the expected value scales by the same factor:

$$E(cX) = cE(X)$$

Multiplying all possible values of $X$ by the same constant rescales its distribution and, when $c < 0,$ reverses the order of its values. A constant $c,$ viewed as a random variable that takes a single value, has expected value $E(c) = c.$

- - -

The additivity property states that the expected value of the sum of two random variables equals the sum of their individual expectations:

$$E(X + Y) = E(X) + E(Y)$$

The identity holds whether or not $X$ and $Y$ are independent. Combined with homogeneity and $E(c) = c,$ it gives $E(aX + b) = aE(X) + b$ for all real constants $a$ and $b.$

## Expectation for jointly distributed variables

The definition of the mean extends to a measurable function $g(X, Y)$ of two jointly distributed random variables $X$ and $Y.$ The formulas below give a finite expected value when $E(|g(X, Y)|) < +\infty.$

If the pair $(X, Y)$ is discrete, the expected value is:

$$\mu_{g(X,Y)} = E[g(X,Y)] = \sum_x \sum_y g(x, y) f_{X,Y}(x, y)$$

If the pair $(X, Y)$ has a joint probability density, the expression becomes:

$$\mu_{g(X,Y)} = E[g(X,Y)] = \int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} g(x, y) f_{X,Y}(x, y) \ dy \ dx$$

In the discrete formula $f_{X,Y}$ is the joint probability mass function, while in the continuous formula it is the joint probability density function. In both forms the mean is the weighted average of $g(X, Y)$ with respect to the joint distribution of $X$ and $Y.$

## Example 1

Consider two products selected independently from a production process in which each product has probability $0.1$ of being defective. The discrete random variable $X$ counts the defective products among the two selected items.

The possible values of $X$ are $0,$ $1,$ and $2,$ corresponding to the number of defective items in the sample. The resulting probability distribution is:

| $x$ | $0$ | $1$ | $2$ |
|:--:|:--:|:--:|:--:|
| $f(x)$ | $0.9^2$ | $2 \cdot 0.1 \cdot 0.9$ | $0.1^2$ |
| $f(x)$ | $0.81$ | $0.18$ | $0.01$ |

The mean follows from the formula for discrete random variables:

$$\mu = E(X) = \sum_x x f(x)$$

Substituting the values of the distribution, we obtain:

$$
\begin{align}
\mu = E(X) &= 0 \cdot 0.81 + 1 \cdot 0.18 + 2 \cdot 0.01 \\[6pt]
    &= 0 + 0.18 + 0.02 \\[6pt]
    &= 0.20
\end{align}
$$

The expected number of defective items in the two-product sample is therefore $0.2.$ Across many independent samples, the total number of defective items approaches $0.2$ times the number of samples, which is one defective item per five samples on average.

## Example 2

The second example involves the continuous case, in which the random variable takes infinitely many values within an [interval](../intervals/). We study the lifetime, measured in hours, of a light bulb, assuming that longer lifetimes are more likely than shorter ones. The random variable $X$ is the lifetime of the bulb, and its [probability density function](../continuous-random-variables/) is:

$$
f(x) =
\begin{cases}
\dfrac{2x}{25^2} & 0 \le x \le 25 \\[6pt]
0 & \text{otherwise}
\end{cases}
$$

This function is non-negative and its integral over the real line equals $1,$ since:

$$\int_0^{25} \frac{2x}{25^2} \ dx = \left[\frac{x^2}{25^2}\right]_0^{25} = 1$$

The expected value is the theoretical average lifetime of the bulb. For a continuous random variable, it is defined as:

$$\mu = E(X) = \int_{-\infty}^{+\infty} x f(x) \ dx$$

Since the density is zero outside the interval $[0, 25],$ the integral reduces to:

$$\mu = \int_0^{25} x \cdot \frac{2x}{25^2} \ dx$$

This expression is the weighted average of all possible lifetimes, each value $x$ weighted by its density $f(x).$

- - -

Factoring the constant out of the integral, we obtain:

$$\mu = \frac{2}{25^2} \int_0^{25} x^2 \ dx$$

The remaining integral can be computed with the [fundamental theorem of calculus](../fundamental-theorem-of-calculus/):

$$\int_0^{25} x^2 \ dx = \frac{25^3}{3} = \frac{15625}{3}$$

In fact, integrating $x^2$ gives the [antiderivative](../indefinite-integrals/) $\tfrac{1}{3}x^3,$ and evaluating it between $0$ and $25$ yields the value of the [definite integral](../definite-integrals/):

$$\frac{1}{3} \cdot 25^3 - \frac{1}{3} \cdot 0^3 = \frac{25^3}{3}$$

- - -

Substituting this result, we obtain:

$$\mu = \frac{2}{625} \cdot \frac{15625}{3} = \frac{50}{3}$$

The mean lifetime of the light bulb is therefore $\mu = \frac{50}{3} \approx 16.67$ hours.
