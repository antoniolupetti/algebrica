---
title: Geometric Distribution
source: https://algebrica.org/geometric-distribution/
license: CC BY-NC 4.0
tags:
  - bernoulli-distribution
  - binomial-distribution
  - discrete-random-variables
  - expected-value
  - exponential-distribution
  - geometric-distribution
  - memorylessness
  - probability
  - probability-mass-function
  - statistics
  - variance
---
## Definition

The geometric distribution is the discrete probability distribution of the number of independent trials needed to obtain the first success in a repeated experiment. Each trial is a [Bernoulli trial](../bernoulli-distribution/) with the same probability of success. A geometric random variable is therefore a waiting time, whereas a [binomial random variable](../binomial-distribution/) is the number of successes in a fixed number of trials. In the [hypergeometric distribution](../hypergeometric-distribution/) the probability of success is not constant because sampling is without replacement; in the geometric distribution it is constant.

Consider a sequence of trials with the following properties:

+ Each trial has exactly two possible outcomes, success and failure.
+ The probability of success $p \in (0,1]$ is the same in every trial.
+ The trials are mutually independent.
+ The [discrete random variable](../discrete-random-variables/) $X$ is the index of the trial on which the first success occurs.

We write $X \sim \mathrm{Geom}(p).$ Its probability mass function is:

$$P(X = k) = (1-p)^{k-1}p$$

In this expression $k = 1, 2, 3, \dots$ is the trial on which the first success occurs, $p$ is the probability of success in a single trial, and $1-p$ is the probability of failure. The factor $(1-p)^{k-1}$ is the probability of the $k-1$ consecutive failures that precede the success.

Some authors instead define a geometric variable $F$ as the number of failures before the first success. The two conventions are related by $F = X-1,$ and the zero-based probability mass function is:

$$P(F = k) = (1-p)^{k}p \qquad k = 0, 1, 2, \dots$$

Under this convention the geometric distribution is the case $r = 1$ of the negative binomial distribution, which counts the failures before the $r$-th success. All formulas below use the positive-integer convention for $X.$ For this variable, $P(X > n) = (1-p)^{n}$ tends to $0$ as $n$ tends to infinity, so the first success occurs after finitely many trials with probability $1.$

The waiting time has a geometric distribution when the trials are independent and have a constant probability of success. In a communication system, $X$ is the number of transmission attempts needed to deliver a message over an unreliable channel; in quality control, it is the number of items inspected until the first defective one is found.

- - -

For $X \sim \mathrm{Geom}(p),$ its probability mass function, mean, variance, and [standard deviation](../variance/) are:

[class="table-1"]

|                                                    |
| -------------------------------------------------- |
| $P(X = k) = (1-p)^{k-1}p \quad k = 1, 2, 3, \dots$ |
| $\mu = E(X) = \frac{1}{p}$                         |
| $\sigma^{2} = \mathrm{Var}(X) = \frac{1-p}{p^{2}}$ |
| $\sigma = \sqrt{\frac{1-p}{p^{2}}}$                |

[/class]

## Deriving the geometric distribution

Consider independent Bernoulli trials $Y_1, Y_2, \dots,$ each with success probability $p,$ and let $X$ be the index of the first successful trial. The first few cases are:

+ If $X = 1,$ the first trial is a success, so the probability is $p.$
+ If $X = 2,$ the first trial is a failure and the second is a success, so the probability is $(1-p)p.$
+ If $X = 3,$ the first two trials are failures and the third is a success, so the probability is $(1-p)^{2}p.$

In general, the event $X = k$ occurs when the first $k-1$ trials are failures and the $k$-th is a success. Since the trials are independent, the probabilities of these outcomes multiply:

$$P(X = k) = (1-p)^{k-1}p$$

The probabilities sum to $1,$ as required of any probability distribution, by the formula for a [geometric series](../geometric-series/):

$$\sum_{k=1}^{\infty} (1-p)^{k-1}p = p \cdot \frac{1}{1-(1-p)} = 1$$

By the recurrence $P(X = k+1) = (1-p)P(X = k),$ the probabilities are a [geometric sequence](../geometric-sequence/) with first term $p$ and common ratio $1-p.$ For $0 < p < 1,$ they decrease as $k$ increases. When $p$ is smaller, the common ratio is closer to $1$ and the decrease is slower; for $p = 1,$ all the probability is concentrated at $X = 1.$

## Mean of the geometric distribution

The [mean](../introduction-to-the-mean/), or [expected value](../mean-or-expected-value-of-a-random-variable/), of a geometric distribution is the long-run average number of trials needed to observe the first success. For a discrete random variable, its definition is:

$$\mu = E(X) = \sum_{k=1}^{\infty} kP(X = k)$$

Substituting the probability mass function, we have:

$$E(X) = \sum_{k=1}^{\infty} k(1-p)^{k-1}p$$

To evaluate the sum, we use the identity:

$$\sum_{k=1}^{\infty} kr^{k-1} = \frac{1}{(1-r)^{2}} \qquad |r| < 1$$

For $|r| < 1,$ this identity is the termwise derivative of $\sum_{k=0}^{\infty} r^{k} = 1/(1-r).$

With $r = 1-p,$ we have:

$$\sum_{k=1}^{\infty} k(1-p)^{k-1} = \frac{1}{p^{2}}$$

Multiplying by $p,$ we have:

$$E(X) = p \cdot \frac{1}{p^{2}} = \frac{1}{p}$$

For example, when $p = 0.1,$ the expected waiting time is $1/p = 10$ trials.

## Variance of the geometric distribution

The [variance](../variance-and-covariance-of-a-random-variable/) of a geometric distribution is the expected squared deviation from the mean $\mu = 1/p.$ Its relation to the second moment is:

$$\sigma^{2} = \mathrm{Var}(X) = E(X^{2}) - [E(X)]^{2}$$

For the second moment, we use the identity:

$$\sum_{k=1}^{\infty} k^{2}r^{k-1} = \frac{1+r}{(1-r)^{3}} \qquad |r| < 1$$

With $r = 1-p$ and $1-r = p,$ we have:

$$E(X^{2}) = p\sum_{k=1}^{\infty} k^{2}(1-p)^{k-1} = p \cdot \frac{1+(1-p)}{p^{3}} = \frac{2-p}{p^{2}}$$

Substituting this result and $E(X) = 1/p$ into the definition, we have:

$$\mathrm{Var}(X) = \frac{2-p}{p^{2}} - \left(\frac{1}{p}\right)^{2} = \frac{2-p-1}{p^{2}} = \frac{1-p}{p^{2}}$$

As $p$ approaches $0,$ the variance grows like $1/p^{2}.$ As $p$ approaches $1,$ it tends to $0$ because the first trial is then almost certain to succeed.

## Example 1

A technician tests a digital sensor that occasionally fails to detect a signal. Detection attempts are independent, and the probability that the sensor registers the signal on a single attempt is $p = 0.2.$ Let $X$ be the number of attempts needed until the first successful detection.

Since $X$ is the number of independent trials until the first success, it has a geometric distribution with parameter $p = 0.2$ and probability mass function:

$$P(X = k) = (1-p)^{k-1}p = (0.8)^{k-1}(0.2) \qquad k = 1, 2, 3, \dots$$

Its expected value is:

$$E(X) = \frac{1}{p} = \frac{1}{0.2} = 5$$

Its variance is:

$$\mathrm{Var}(X) = \frac{1-p}{p^{2}} = \frac{0.8}{(0.2)^{2}} = \frac{0.8}{0.04} = 20$$

The corresponding standard deviation is:

$$\sigma = \sqrt{20} \approx 4.472$$

The expected number of attempts is therefore $5,$ and the standard deviation is approximately $4.472$ attempts.

## Connection with the exponential distribution

The geometric and exponential distributions are waiting-time distributions on different time scales. The geometric variable $X$ is the number of discrete Bernoulli trials up to the first success. In continuous time, the [continuous random variable](../continuous-random-variables/) $T$ has an exponential distribution when events occur at a constant rate $\lambda.$ Its density is:

$$
f(t;\lambda) =
\begin{cases}
\lambda e^{-\lambda t} & t > 0 \\[6pt]
0 & t \le 0
\end{cases}
$$

Although one distribution is discrete and the other continuous, both are memoryless. For $0 < p < 1$ and all nonnegative integers $m$ and $n,$ the geometric distribution satisfies:

$$P(X > m+n \mid X > m) = P(X > n)$$

This identity follows from $P(X > n) = (1-p)^{n},$ the probability of $n$ initial failures, together with $(1-p)^{m+n} = (1-p)^{m}(1-p)^{n}.$ For the exponential distribution, the corresponding identity for all $s, t > 0$ is:

$$P(T > s+t \mid T > s) = P(T > t)$$

Memorylessness means that the probability of waiting an additional amount of time does not depend on how long one has already waited. The geometric distributions are the only nondegenerate distributions on the positive integers with this property. The exponential distributions are the only continuous distributions on $[0,\infty)$ with the same property.
