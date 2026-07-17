---
title: Bernoulli Distribution
source: https://algebrica.org/bernoulli-distribution/
license: CC BY-NC 4.0
tags:
  - bernoulli-distribution
  - binomial-distribution
  - discrete-random-variables
  - expected-value
  - probability
  - probability-mass-function
  - statistics
  - variance
---
## Definition

The Bernoulli distribution models a single experiment with exactly two mutually exclusive outcomes, called success and failure. Such an experiment is a Bernoulli trial. A [discrete random variable](../discrete-random-variables/) follows a Bernoulli distribution when it takes the value $1$ if the trial results in success and the value $0$ if it results in failure. The distribution has a single parameter $p \in [0,1],$ the probability of success, while failure has probability $1-p.$ We write $X \sim \mathrm{Bernoulli}(p).$

The Bernoulli distribution is defined by $P(X = 1) = p$ and $P(X = 0) = 1-p.$ For $x \in \{0,1\},$ these two cases combine into the probability mass function:

$$P(X = x) = b(x;p) = p^{x}(1-p)^{1-x}$$

In this expression $x \in \{0,1\}$ is the observed outcome of the trial. For every $x \notin \{0,1\},$ the probability $P(X = x)$ is zero. When $p=0$ or $p=1,$ the distribution is degenerate because one outcome occurs with probability $1.$

Equivalently, if $A$ is an event with $P(A) = p,$ its indicator, which equals $1$ on $A$ and $0$ on its complement, follows a Bernoulli distribution with parameter $p.$

> The binomial distribution extends this model to a fixed number of independent Bernoulli trials.

- - -

For $X \sim \mathrm{Bernoulli}(p),$ the probability mass function, mean, variance, and standard deviation are given below.

[class="table-1"]

|                                         |
| --------------------------------------- |
| $P(X = x) = b(x;p) = p^{x}(1-p)^{1-x}$  |
| $\mu = E(X) = p$                        |
| $\sigma^{2} = \mathrm{Var}(X) = p(1-p)$ |
| $\sigma = \sqrt{p(1-p)}$                |

[/class]

## Mean of the Bernoulli distribution

The [mean](../introduction-to-the-mean/), or [expected value](../mean-or-expected-value-of-a-random-variable/), of a Bernoulli distribution is obtained by weighting the values $0$ and $1$ by their probabilities. We start from the definition of the expected value of a discrete random variable:

$$\mu = E(X) = \sum_{x \in \{0,1\}} xb(x;p)$$

For a Bernoulli distribution the probability mass function is:

$$b(x;p) = p^{x}(1-p)^{1-x}$$

The sum has only two terms, one for each value of $x$:

$$E(X) = 0 \cdot (1-p) + 1 \cdot p$$

The first term vanishes and the mean reduces to the parameter itself:

$$\mu = E(X) = p$$

> For independent repetitions of the trial, the [sample mean](../arithmetic-mean/) is the observed proportion of successes. By the law of large numbers, it converges to $p$ as the number of trials increases.

## Variance of the Bernoulli distribution

The [variance](../variance-and-covariance-of-a-random-variable/) of a Bernoulli distribution is the expected squared deviation of the outcome from the mean $\mu=p.$ It can be computed from the second moment:

$$\sigma^{2} = \mathrm{Var}(X) = E(X^{2}) - [E(X)]^{2}$$

A Bernoulli random variable takes only the values $0$ and $1.$ Squaring changes neither of them, so $X^{2} = X$ and the second moment coincides with the mean of $X$ itself:

$$E(X^{2}) = 0^{2}(1-p) + 1^{2}p = p$$

Substituting $E(X^{2}) = p$ and $E(X) = p$ into the definition yields the variance:

$$\sigma^{2} = \mathrm{Var}(X) = p - p^{2} = p(1-p)$$

> The identity $p(1-p) = 1/4 - (p-1/2)^{2},$ obtained by [completing the square](../completing-the-square/), shows that the variance has its maximum value $1/4$ at $p = 1/2.$ It decreases as $p$ approaches $0$ or $1,$ because one outcome becomes more likely than the other.

## Example 1

Consider a quality-control test on a single electronic component. During the inspection the component is powered on and must reach a specific voltage level to be considered functional. Let $X$ be the random variable for the outcome of the test:

+ $X = 1$ if the component meets the required standard (success).
+ $X = 0$ if it fails the test (failure).

Suppose that historical data give a success rate of $0.85,$ which we use as the parameter $p = 0.85.$ The random variable $X$ then follows a Bernoulli distribution with parameter $p,$ and its probability mass function is:

$$P(X = x) = p^{x}(1-p)^{1-x}$$

To compute the probability of success we evaluate the probability mass function at $x = 1$:

$$P(X = 1) = p^{1}(1-p)^{0} = 0.85$$

The same computation at $x = 0$ gives the probability of failure:

$$P(X = 0) = p^{0}(1-p)^{1} = 0.15$$

Therefore, the probability that the component passes the test is $0.85,$ or 85%.

> The historical rate estimates $p$ only when the sampled components and test conditions are representative of the component under inspection.

## The Bernoulli distribution in the binomial model

Let $X_{1},\ldots,X_{n}$ be independent Bernoulli random variables with the same parameter $p.$ Their sum

$$Y = X_{1} + \cdots + X_{n}$$

counts the number of successes in the $n$ trials and follows a binomial distribution. For $k \in \{0,\ldots,n\},$ its probability mass function is:

$$P(Y = k) = \binom{n}{k}p^{k}(1-p)^{n-k}$$

The [binomial coefficient](../binomial-coefficient/) counts the arrangements of $k$ successes among $n$ trials, and the factor $p^{k}(1-p)^{n-k}$ is the probability of each arrangement. [Linearity of expectation](../mean-or-expected-value-of-a-random-variable/) gives the mean $np$ of the binomial distribution, while independence gives its variance $np(1-p).$

The following table compares the two distributions. The Bernoulli distribution describes a single success-failure experiment, while the binomial distribution counts successes in a fixed number of independent trials with the same probability $p.$

| Feature          | Bernoulli  | Binomial          |
| ---------------- | ---------- | ----------------- |
| Number of trials | $1$        | $n$               |
| Parameters       | $p$        | $n, p$            |
| Support          | $\{0,1\}$  | $\{0, \dots, n\}$ |
| Mean             | $p$        | $np$              |
| Variance         | $p(1-p)$   | $np(1-p)$         |
