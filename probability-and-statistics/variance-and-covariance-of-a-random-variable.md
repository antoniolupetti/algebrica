---
title: Variance and Covariance of Random Variables
source: https://algebrica.org/variance-and-covariance-of-a-random-variable/
license: CC BY-NC 4.0
tags:
  - correlation-coefficient
  - covariance
  - probability
  - random-variables
  - standard-deviation
  - statistics
  - variance
---

## Variance of a random variable

For a finite dataset, the [variance](../variance/) is the mean of the squared deviations from the [arithmetic mean](../arithmetic-mean/). If the observations are $x_1, \ldots, x_n$ and their mean is $M,$ then:

$$
\sigma^2 = \frac{1}{n}\sum_{i=1}^{n}(x_i - M)^2
$$

After [expanding the square](../notable-products/), the same variance is:

$$
\sigma^2 = \frac{1}{n}\sum_{i=1}^{n}x_i^2 - M^2
$$

Thus the variance is the mean of the squares minus the square of the mean.

- - -

Suppose $X$ has a finite second moment, so $E[X^2] < +\infty,$ and write $\mu = E[X]$ for its [expected value](../mean-or-expected-value-of-a-random-variable/). The variance of $X$ is the expected squared deviation from $\mu:$

$$
\mathrm{Var}(X) = E[(X - \mu)^2]
$$

By the linearity of expectation, the expanded form is:

$$
\mathrm{Var}(X) = E[X^2] - [E[X]]^2
$$

The variance is non-negative. It is $0$ exactly when $X = \mu$ with probability $1.$ For a [discrete random variable](../discrete-random-variables/) with probability mass function $f,$ the variance is:

$$
\sigma^2 = E[(X - \mu)^2] = \sum_x (x - \mu)^2 f(x)
$$

In this expression $x$ ranges over the possible values of $X.$ For a [continuous random variable](../continuous-random-variables/) with probability density function $f,$ the variance is the [improper integral](../improper-integrals/):

$$
\sigma^2 = E[(X - \mu)^2] = \int_{-\infty}^{+\infty} (x - \mu)^2 f(x) \ dx
$$

These are the discrete and continuous forms of the same expectation $E[(X - \mu)^2].$

## Deviation and standard deviation

The difference $x - \mu$ is the deviation of a possible value $x$ from the expected value. It is positive when $x > \mu,$ negative when $x < \mu,$ and zero when $x = \mu.$ Its [absolute value](../absolute-value/) is the distance from $\mu.$ The non-negative [square root](../radicals/) of the variance is the standard deviation:

$$
\sigma = \sqrt{\mathrm{Var}(X)}
$$

The standard deviation has the same units as $X,$ whereas the variance has squared units.

## Example 1

Let $X$ be the number of defective components in a batch of four from a manufacturing line. Its probability mass function is:

| $x$ | $0$ | $1$ | $2$ | $3$ | $4$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| $f(x)$ | $0.1$ | $0.3$ | $0.4$ | $0.1$ | $0.1$ |

The expected value is:

$$
E[X] = \sum_x x f(x)
$$

The numerical calculation is:

$$
\begin{align}
E[X] &= (0)(0.1) + (1)(0.3) + (2)(0.4) + (3)(0.1) + (4)(0.1) \\[6pt]
     &= 0 + 0.3 + 0.8 + 0.3 + 0.4 = 1.8
\end{align}
$$

The expected number of defective components per batch is $\mu = 1.8.$ The variance is:

$$
\mathrm{Var}(X) = \sum_x (x - \mu)^2 f(x)
$$

With $\mu = 1.8,$ the numerical calculation is:

$$
\begin{align}
\mathrm{Var}(X) &= (0 - 1.8)^2(0.1) + (1 - 1.8)^2(0.3) + (2 - 1.8)^2(0.4) + (3 - 1.8)^2(0.1) + (4 - 1.8)^2(0.1) \\[6pt]
&= (3.24)(0.1) + (0.64)(0.3) + (0.04)(0.4) + (1.44)(0.1) + (4.84)(0.1) \\[6pt]
&= 0.324 + 0.192 + 0.016 + 0.144 + 0.484 = 1.16
\end{align}
$$

The standard deviation is the non-negative square root of the variance:

$$
\sigma = \sqrt{\mathrm{Var}(X)} = \sqrt{1.16} \approx 1.08
$$

Therefore the variance is $1.16$ components squared, and the standard deviation is approximately $1.08$ components.

## Covariance of two random variables

Suppose $X$ and $Y$ are jointly distributed and have finite second moments. Their means are $\mu_X = E[X]$ and $\mu_Y = E[Y],$ and their covariance is the expected product of their deviations from these means:

$$
\mathrm{Cov}(X, Y) = E[(X - \mu_X)(Y - \mu_Y)]
$$

Positive covariance means that the deviations tend to have the same sign, while negative covariance means that they tend to have opposite signs. After expanding the product, the covariance is:

$$
\mathrm{Cov}(X, Y) = E[XY] - E[X]E[Y]
$$

For discrete random variables with joint probability mass function $f,$ the covariance is:

$$
\mathrm{Cov}(X, Y) = \sum_x \sum_y (x - \mu_X)(y - \mu_Y) f(x, y)
$$

For each pair $(x, y),$ the value $f(x, y)$ is its probability in the [joint probability distribution](../discrete-random-variables/). If the pair $(X, Y)$ has a [joint probability density function](../continuous-random-variables/) $f,$ the covariance is:

$$
\mathrm{Cov}(X, Y) = \int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} (x - \mu_X)(y - \mu_Y) f(x, y) \ dy \ dx
$$

Covariance is symmetric, and the covariance of a variable with itself is its variance:

$$
\mathrm{Cov}(X, Y) = \mathrm{Cov}(Y, X), \qquad \mathrm{Cov}(X, X) = \mathrm{Var}(X)
$$

Independent random variables with finite second moments have zero covariance. The converse is false. Dependent random variables can have zero covariance.

## Correlation coefficient

The units of covariance are the product of the units of $X$ and $Y,$ so its magnitude depends on the choice of units. If both variables have positive variance, their correlation coefficient is the covariance divided by the product of their standard deviations:

$$
\rho_{XY} = \frac{\sigma_{XY}}{\sigma_X \sigma_Y} = \frac{\mathrm{Cov}(X, Y)}{\sqrt{\mathrm{Var}(X)} \sqrt{\mathrm{Var}(Y)}}
$$

In this expression $\sigma_{XY} = \mathrm{Cov}(X, Y),$ while $\sigma_X$ and $\sigma_Y$ are the standard deviations of the two variables. The value of $\rho_{XY}$ is unchanged when either variable is shifted or multiplied by a positive constant.

The Cauchy-Schwarz inequality implies $-1 \le \rho_{XY} \le 1.$ The coefficient is $1$ exactly when one centered variable is a positive scalar multiple of the other with probability $1,$ and it is $-1$ exactly when that multiple is negative. A coefficient close to either endpoint means that the linear association is strong. A coefficient close to $0$ means that the linear association is weak, but nonlinear dependence may still be present. For example, if $X$ is uniformly distributed on $[-1, 1]$ and $Y = X^2,$ then $\mathrm{Cov}(X, Y) = 0$ even though $Y$ is determined by $X.$

## Example 2

Let $X$ be the number of hours spent studying during a week, and let $Y$ be the score on a six-point assessment. The following four pairs have positive probability:

| $X$ | $Y$ | $f(x, y)$ |
|:---:|:---:|:---------:|
| $1$ | $2$ | $0.2$ |
| $2$ | $3$ | $0.3$ |
| $3$ | $5$ | $0.3$ |
| $4$ | $6$ | $0.2$ |

All other pairs have probability $0.$ Larger values of $X$ occur with larger values of $Y,$ but the four pairs do not lie on a straight line. We compute the correlation coefficient of $X$ and $Y.$

The expected values of the two variables are:

$$
\begin{align}
E[X] &= (1)(0.2) + (2)(0.3) + (3)(0.3) + (4)(0.2) = 2.5 \\[6pt]
E[Y] &= (2)(0.2) + (3)(0.3) + (5)(0.3) + (6)(0.2) = 4.0
\end{align}
$$

The expected value of the product $XY$ is:

$$
\begin{align}
E[XY] &= (1 \cdot 2)(0.2) + (2 \cdot 3)(0.3) + (3 \cdot 5)(0.3) + (4 \cdot 6)(0.2) \\[6pt]
      &= 0.4 + 1.8 + 4.5 + 4.8 = 11.5
\end{align}
$$

Using $\mathrm{Cov}(X, Y) = E[XY] - E[X]E[Y],$ the covariance is:

$$
\mathrm{Cov}(X, Y) = 11.5 - (2.5)(4.0) = 11.5 - 10 = 1.5
$$

The expected values of the squares are:

$$
\begin{align}
E[X^2] &= (1)^2(0.2) + (2)^2(0.3) + (3)^2(0.3) + (4)^2(0.2) = 7.3 \\[6pt]
E[Y^2] &= (2)^2(0.2) + (3)^2(0.3) + (5)^2(0.3) + (6)^2(0.2) = 18.2
\end{align}
$$

The variances of $X$ and $Y$ are:

$$
\begin{align}
\mathrm{Var}(X) &= E[X^2] - [E[X]]^2 = 7.3 - (2.5)^2 = 7.3 - 6.25 = 1.05 \\[6pt]
\mathrm{Var}(Y) &= E[Y^2] - [E[Y]]^2 = 18.2 - (4.0)^2 = 18.2 - 16 = 2.2
\end{align}
$$

The correlation coefficient is:

$$
\begin{align}
\rho_{XY} &= \frac{\mathrm{Cov}(X, Y)}{\sqrt{\mathrm{Var}(X)} \sqrt{\mathrm{Var}(Y)}} \\[6pt]
          &= \frac{1.5}{\sqrt{1.05}\sqrt{2.2}} = \frac{1.5}{\sqrt{2.31}} \approx 0.987
\end{align}
$$

The correlation between $X$ and $Y$ is approximately $0.987.$ The four possible pairs therefore lie close to an increasing straight line, but not exactly on one.
