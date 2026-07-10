---
title: Harmonic Mean
source: https://algebrica.org/harmonic-mean/
license: CC BY-NC 4.0
tags:
  - harmonic-mean
  - means
  - power-means
  - statistics
---

## Definition

The harmonic mean is one of the [power means](../introduction-to-the-mean/). Unlike the [arithmetic mean](../arithmetic-mean/), it applies when the data combine reciprocally rather than additively. It takes the reciprocal of each value, averages them, and then takes the reciprocal of that average.

The harmonic mean is the appropriate average for rates and ratios, such as speed, cost per unit, or productivity, where each value applies to the same fixed quantity. The arithmetic mean gives more weight to the larger values, whereas the harmonic mean gives more weight to the smaller ones. In its general form, the harmonic mean is:

$$M_h = \frac{n}{\displaystyle\sum_{i=1}^{n} \frac{1}{x_i}}$$

In this expression $x_1, x_2, \ldots, x_n$ are positive values and $n$ is the number of elements. The reciprocal of the harmonic mean equals the arithmetic mean of the reciprocals:

$$\frac{1}{M_h} = \frac{1}{n}\sum_{i=1}^{n}\frac{1}{x_i}$$

Read from right to left, the identity recovers $M_h$ from the reciprocals, so the harmonic mean and the arithmetic mean of the reciprocals determine each other.

+ The harmonic mean is defined only for positive values, since a zero value has no reciprocal and mixed signs can make the denominator vanish.
+ The smaller values have more weight in the result than the larger ones.
+ It is always less than or equal to the [geometric mean](../geometric-mean/), which in turn is less than or equal to the arithmetic mean.
+ For equal amounts of work or distance covered at varying speeds, the harmonic mean is the true average rate.

> The harmonic mean is often written $M_{-1}$ because it is the power mean of exponent $s=-1$ in the Hölder family.

## Example 1

A car travels a road divided into two equal segments. On the first half it moves at $60$ km/h, and on the second half at $90$ km/h. The distance is the same on each half, but the time is not. The half covered at the lower speed takes more time, so the lower speed has a greater influence on the average. The arithmetic mean of the two speeds, $75$ km/h, is therefore not the average speed of the trip.

Call the two speeds $v_1$ and $v_2$ and let $d$ be the length of each half. The car takes time $t_1 = d/v_1$ on the first half and $t_2 = d/v_2$ on the second, so the average speed $\bar{v}$ is the total distance divided by the total time:

$$\bar{v} = \frac{2d}{t_1 + t_2} = \frac{2d}{\frac{d}{v_1} + \frac{d}{v_2}} = \frac{2}{\frac{1}{v_1} + \frac{1}{v_2}}$$

The distance $d$ cancels, and the average speed is the harmonic mean of the two speeds. Substituting $v_1 = 60$ and $v_2 = 90$ gives:

$$M_h = \frac{2}{\frac{1}{60} + \frac{1}{90}} = \frac{2}{\frac{5}{180}} = \frac{360}{5} = 72$$

The harmonic mean accounts for the extra time spent at the lower speed, so the average speed for the trip is $72$ km/h.

## Example 2

A machine completes five production runs of equal size and works at a different rate on each run. The table lists the rate of each run in units per minute.

| Run | Rate (units/minute) |
|:------:|:-------------------:|
| 1 | 10 |
| 2 | 12 |
| 3 | 8 |
| 4 | 15 |
| 5 | 9 |

Each run produces the same number of units, so the overall average rate is the harmonic mean, not the arithmetic one. A slower run takes more time for the same output, so it counts more in the average.

Substituting the observed values gives:

$$
\begin{align}
M_h &= \frac{5}{\frac{1}{10} + \frac{1}{12} + \frac{1}{8} + \frac{1}{15} + \frac{1}{9}} \\[6pt]
&= \frac{5}{0.1 + 0.0833 + 0.125 + 0.0667 + 0.1111} \\[6pt]
&= \frac{5}{0.4861} \approx 10.29
\end{align}
$$

The average rate of production is therefore about $10.3$ units per minute.

## The harmonic mean of two numbers

For two positive values $a$ and $b,$ the sum of the reciprocals is $\frac{a+b}{ab},$ so the harmonic mean reduces to:

$$M_h = \frac{2}{\frac{1}{a}+\frac{1}{b}} = \frac{2ab}{a+b}$$

Write $A=\frac{a+b}{2}$ for the arithmetic mean of the pair and $G=\sqrt{ab}$ for the geometric mean. Multiplying $M_h$ by $A$ cancels the factor $a+b$ and leaves $ab,$ so:

$$M_h A = ab = G^2$$

The geometric mean is thus the geometric mean of the arithmetic and harmonic means, $G=\sqrt{A M_h}.$ Since $G \le A,$ the identity $M_h A = G^2$ gives $M_h = G^2/A \le G,$ so $M_h \le G \le A,$ with equality only when $a=b.$

> The identity $M_h A = G^2$ holds only for two values. For the values $1, 1, 4$ the harmonic mean is $\frac{4}{3},$ the arithmetic mean is $2,$ and $M_h A = \frac{8}{3}$ differs from $G^2 = 2\sqrt[3]{2}.$

In the harmonic sequence $1, \frac{1}{2}, \frac{1}{3}, \ldots$ every term after the first is the harmonic mean of its two neighbors, since the reciprocals of $\frac{1}{n-1}$ and $\frac{1}{n+1}$ have arithmetic mean $n.$ The name of the mean comes from this sequence, which the Pythagoreans connected to the lengths of vibrating strings and to musical harmony.

## Bounds and behavior

The harmonic mean does not decrease when a single value grows, because a larger $x_i$ lowers its reciprocal $\frac{1}{x_i}$ and shrinks the denominator. The harmonic mean of positive data therefore lies between the smallest and the largest value:

$$\min_i x_i \le M_h \le \max_i x_i$$

with equality only when all the values coincide. A large value adds a small reciprocal to the denominator and shifts the harmonic mean very little, while a small value adds a large reciprocal and dominates the sum. Sending some of the values toward infinity, with at least one held fixed, leaves the harmonic mean finite, so a single large observation cannot raise it without bound as it would the arithmetic mean.

The inequality between the three means holds for any number of values, not only for two. The geometric mean of positive values is $G = \left(\prod_{i=1}^{n} x_i\right)^{1/n},$ and the geometric mean of the reciprocals is $\frac{1}{G},$ since inverting every factor inverts the product. Applying the arithmetic-geometric mean inequality to the reciprocals gives:

$$\frac{1}{M_h} = \frac{1}{n}\sum_{i=1}^{n}\frac{1}{x_i} \ge \left(\prod_{i=1}^{n}\frac{1}{x_i}\right)^{1/n} = \frac{1}{G}$$

Taking reciprocals reverses the inequality between positive numbers, hence $M_h \le G.$ The same inequality applied to the values themselves gives $G \le A,$ so $M_h \le G \le A$ holds for every $n,$ with equality only when the $x_i$ are all equal.

## Applications

The $F_1$ score of a binary classifier is the harmonic mean of its precision $P,$ the fraction of predicted positives that are correct, and its recall $R,$ the fraction of actual positives that are identified:

$$F_1 = \frac{2}{\frac{1}{P} + \frac{1}{R}} = \frac{2PR}{P+R}$$

The harmonic mean stays close to the smaller of the two quantities, so high precision cannot compensate for poor recall, and a recall near zero forces $F_1$ near zero regardless of the precision.

In physics, resistances in parallel combine through their reciprocals, because the voltage is common to all branches and the currents add. Two resistances $R_1$ and $R_2$ in parallel have equivalent resistance:

$$R_{\mathrm{eq}} = \frac{1}{\frac{1}{R_1} + \frac{1}{R_2}} = \frac{R_1 R_2}{R_1 + R_2}$$

This value is half the harmonic mean of the pair, and $n$ resistances in parallel have equivalent resistance $\frac{M_h}{n}.$ The same rule applies to capacitors in series, and the focal length of a thin lens is half the harmonic mean of the object and image distances.

## Weighted harmonic mean

When the observations are not equally important, each value $x_i$ has a weight $w_i>0$ set by its frequency or relevance. The weighted harmonic mean is:

$$M_{hw} = \frac{\sum_{i=1}^{n} w_i}{\displaystyle\sum_{i=1}^{n} \frac{w_i}{x_i}}$$

In this expression $x_i>0$ are the observed values and $w_i$ their weights.

+ The weighted harmonic mean generalizes the simple harmonic mean through the weights $w_i.$
+ Observations with larger weights have a stronger influence on the result.
+ When all weights are equal, the weighted harmonic mean reduces to the simple harmonic mean.

The weighted form is the correct average for ratios such as the price-to-earnings ratio. A portfolio holds $30000$ dollars of a stock at a P/E of $10$ and $10000$ dollars of a stock at a P/E of $40.$ Weighting each ratio by the amount invested gives:

$$M_{hw} = \frac{30000 + 10000}{\frac{30000}{10} + \frac{10000}{40}} = \frac{40000}{3250} \approx 12.3$$

The weighted arithmetic mean of the two ratios is $17.5,$ above the true figure, because it overweights the stock with the higher ratio. The weighted harmonic mean is the portfolio's actual price-to-earnings ratio, the total price divided by the total earnings.
