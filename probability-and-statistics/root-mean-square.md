---
title: Root Mean Square
source: https://algebrica.org/root-mean-square/
license: CC BY-NC 4.0
tags:
  - means
  - power-means
  - quadratic-mean
  - root-mean-square
  - statistics
---

## Definition

The quadratic mean, also called the root mean square, is one of the [power means](../introduction-to-the-mean/). It is the square root of the [arithmetic mean](../arithmetic-mean/) of the squared values, and it is the appropriate average when the sign of the data is irrelevant and only the magnitude of each value matters. In its general form, the quadratic mean is:

$$M_2 = \sqrt{\frac{1}{n} \sum_{i=1}^{n} x_i^2}$$

In this expression $x_1, x_2, \ldots, x_n$ are the observed values and $n$ is the number of elements. Squaring removes the sign of each value, so opposite values cannot cancel, and the larger magnitudes have a stronger influence on the result than the smaller ones.

+ The quadratic mean is defined for any set of real numbers, positive or negative, and its value is never negative.
+ It lies between the smallest and the largest of the absolute values of the data.
+ Every dataset satisfies $M_2 \ge |M_1|,$ with equality only when all the values are equal, and for [positive values](../types-of-numbers/) the chain $M_{-1} \le M_0 \le M_1 \le M_2$ orders the [harmonic](../harmonic-mean/), [geometric](../geometric-mean/), arithmetic, and quadratic means.
+ Quantities that combine through their squares, such as voltages, molecular speeds, or measurement errors, have the quadratic mean as their correct average.

> The quadratic mean is often written $M_2$ because it is the power mean of exponent $s=2$ in the Hölder family. In physics the same quantity appears as $\sqrt{\langle x^2 \rangle},$ where the angle brackets denote the mean of the squared values.

## Example 1

The table records the temperature variation in a small mountain town on five consecutive autumn days. The variations fall above and below zero, and the quadratic mean measures their overall magnitude regardless of sign.

| Day | Variation (°C) |
|:---:|:--------------:|
| Monday | -3.5 |
| Tuesday | 0.0 |
| Wednesday | 2.8 |
| Thursday | -1.6 |
| Friday | 3.2 |

Substituting the observed values into the quadratic mean formula gives:

$$
\begin{align}
M_2 &= \sqrt{\frac{(-3.5)^2 + 0.0^2 + 2.8^2 + (-1.6)^2 + 3.2^2}{5}} \\[6pt]
&= \sqrt{\frac{12.25 + 0.00 + 7.84 + 2.56 + 10.24}{5}} \\[6pt]
&= \sqrt{\frac{32.89}{5}} = \sqrt{6.578} \approx 2.56
\end{align}
$$

The arithmetic mean of the same values is $0.18$ °C, far below the quadratic mean, because the sum keeps the sign of each variation and the negative days offset the positive ones. The quadratic mean treats a drop of $3.5$ degrees and a rise of $3.5$ degrees as equally large, so the average magnitude of the daily variation over the period is about $2.56$ °C.

## Relation to the standard deviation

The variance $\sigma^2$ is the mean of the squared deviations from the arithmetic mean $M_1.$ Expanding the square of each deviation gives:

$$\sigma^2 = \frac{1}{n}\sum_{i=1}^{n}(x_i - M_1)^2 = \frac{1}{n}\sum_{i=1}^{n} x_i^2 - M_1^2 = M_2^2 - M_1^2$$

The mean of the squares thus splits into the square of the mean plus the variance, $M_2^2 = M_1^2 + \sigma^2.$ The standard deviation is the quadratic mean of the deviations $x_i - M_1,$ and the quadratic mean of a dataset coincides with its standard deviation exactly when the arithmetic mean is zero. For the variations of Example 1, $M_1 = 0.18$ and $M_2^2 = 6.578,$ so the variance is $6.578 - 0.0324 = 6.5456$ and the standard deviation is $\sigma \approx 2.558,$ slightly below $M_2 \approx 2.565.$ In the physical sciences the term root mean square often denotes this standard deviation, the square root of the mean squared deviation of a signal from a baseline or from a fitted curve.

The identity also explains how the quadratic mean responds to a shift of the data. Adding the same positive constant $c$ to every value raises the arithmetic mean by exactly $c$ but raises the quadratic mean by less, a result of Hoehn and Niven (1985). For positive values that are not all equal:

$$M_2(x_1 + c, \ldots, x_n + c) < c + M_2(x_1, \ldots, x_n)$$

Both sides are positive, so comparing their squares decides the inequality. The shift replaces $M_1$ with $M_1 + c$ and leaves the variance unchanged, hence the left side squared is $(M_1 + c)^2 + \sigma^2.$ The right side squared exceeds it by $2c(M_2 - M_1),$ which is positive because the values are not all equal.

For a [continuous random variable](../continuous-random-variables/) $X$ with density $f,$ the quadratic mean has the same structure, with the density weighting each squared value:

$$\sqrt{E(X^2)} = \sqrt{\int_{-\infty}^{+\infty} x^2 f(x) \ dx}$$

The decomposition $E(X^2) = \mu^2 + \sigma^2$ holds again, with $\mu = E(X)$ the [expected value](../mean-or-expected-value-of-a-random-variable/) of $X$ and $\sigma^2$ its variance.

## The quadratic mean of a function

For a function $f$ defined on an interval $[T_1, T_2],$ the sum over discrete values becomes a [definite integral](../definite-integrals/), and the quadratic mean of $f$ is:

$$f_{\mathrm{RMS}} = \sqrt{\frac{1}{T_2 - T_1} \int_{T_1}^{T_2} [f(t)]^2 \ dt}$$

When $f$ is periodic, the interval of integration is one full period, since every period repeats the same values. For the sinusoid $f(t) = A\sin t$ with amplitude $A > 0,$ the identity:

$$\sin^2 t = \frac{1 - \cos 2t}{2}$$ 
reduces the integrand to a constant plus a cosine term whose integral over a period is zero, so $\int_0^{2\pi} \sin^2 t \ dt = \pi$ and:

$$
\begin{align}
f_{\mathrm{RMS}} &= \sqrt{\frac{1}{2\pi} \int_{0}^{2\pi} A^2 \sin^2 t \ dt} \\[6pt]
&= \sqrt{\frac{A^2}{2\pi} \cdot \pi} = \frac{A}{\sqrt{2}} \approx 0.707 A
\end{align}
$$

The quadratic mean of a [sine](../sine-and-cosine/) wave is its amplitude divided by $\sqrt{2},$ whatever the frequency.