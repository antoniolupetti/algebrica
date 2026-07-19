---
title: Hypergeometric Distribution
source: https://algebrica.org/hypergeometric-distribution/
license: CC BY-NC 4.0
tags:
  - binomial-distribution
  - discrete-random-variables
  - expected-value
  - hypergeometric-distribution
  - probability
  - probability-mass-function
  - sampling-without-replacement
  - statistics
  - variance
---
## Definition

The hypergeometric distribution is a discrete probability distribution that describes the number of successes in a simple random sample drawn without replacement from a finite population. In the [binomial distribution](../binomial-distribution/) the trials are independent and the probability of success stays constant. In the hypergeometric setting each draw changes the composition of the population, so the probability of selecting a success varies from one draw to the next.

Consider a finite population divided into successes and failures, from which a sample of fixed size is drawn without replacement. The experiment has the following properties:

+ The population has fixed size $N \ge 2,$ with $K \in \{0,\ldots,N\}$ successes and $N-K$ failures.
+ The sample size satisfies $1 \le n \le N,$ and every subset of $n$ items has the same probability of being selected.
+ Each item drawn is either a success or a failure.
+ The [discrete random variable](../discrete-random-variables/) $X$ is the number of successes observed in the sample.

Drawing the items successively, with every remaining item equally likely at each step, produces this sampling scheme. A given subset can be drawn in $n!$ different orders, and each order has probability $1/[N(N-1)\cdots(N-n+1)].$ Hence the probability of selecting any particular subset is:

$$\frac{n!}{N(N-1)\cdots(N-n+1)} = \frac{1}{\binom{N}{n}}$$

The probability of observing exactly $x$ successes in the sample is:

$$P(X = x) = \frac{\binom{K}{x}\binom{N-K}{n-x}}{\binom{N}{n}}$$

In this expression the [binomial coefficient](../binomial-coefficient/) $\binom{K}{x}$ counts the ways to choose $x$ successes from the $K$ available, $\binom{N-K}{n-x}$ counts the ways to choose the remaining $n-x$ items from the $N-K$ failures, and $\binom{N}{n}$ is the number of distinct samples of size $n$ that can be drawn from a population of size $N.$

> The binomial coefficient $\binom{a}{b}$ is zero when $b > a$ or $b < 0,$ so $P(X = x)$ is nonzero only for $\max(0, n-N+K) \le x \le \min(n, K).$

- - -

The probabilities sum to $1,$ as required of any probability distribution, by [Vandermonde's identity](../binomial-coefficient/):

$$\sum_{x=0}^{n} \binom{K}{x}\binom{N-K}{n-x} = \binom{N}{n}$$

The same model applies whenever a simple random sample is drawn without replacement from a finite population and each item either has a specified characteristic or does not. In quality control, $X$ can count the defective items in a sample from a batch with known numbers of defective and non-defective units. In an opinion poll, $X$ can count the sampled individuals who would answer "yes" when $K$ members of the population would give that answer.

- - -

For $X \sim \mathrm{Hyp}(N, K, n),$ the probability mass function, mean, variance, and [standard deviation](../variance-and-covariance-of-a-random-variable/) are given below.

[class="table-1"]

|                                                                                         |
| --------------------------------------------------------------------------------------- |
| $P(X = x) = \frac{\binom{K}{x}\binom{N-K}{n-x}}{\binom{N}{n}} \quad x = 0, 1, \dots, n$  |
| $\mu = E(X) = n\frac{K}{N}$                                                              |
| $\sigma^{2} = \mathrm{Var}(X) = n\frac{K}{N}\left(1 - \frac{K}{N}\right)\frac{N-n}{N-1}$ |
| $\sigma = \sqrt{n\frac{K}{N}\left(1 - \frac{K}{N}\right)\frac{N-n}{N-1}}$                |

[/class]

## Mean of the hypergeometric distribution

The [mean](../introduction-to-the-mean/), or [expected value](../mean-or-expected-value-of-a-random-variable/), of a hypergeometric distribution is the expected number of successes in a sample of size $n.$ By definition:

$$\mu = E(X) = \sum_{x=0}^{n} xP(X = x)$$

Substitution of the probability mass function gives:

$$E(X) = \sum_{x=0}^{n} x\frac{\binom{K}{x}\binom{N-K}{n-x}}{\binom{N}{n}}$$

We use the identity:

$$x\binom{K}{x} = K\binom{K-1}{x-1}$$

If $K=0,$ then $X=0$ and the mean formula follows directly. For $K \ge 1,$ the term with $x = 0$ vanishes because of the factor $x.$ The identity rewrites each remaining summand so that the constant factor $K$ can be collected:

$$E(X) = \frac{K}{\binom{N}{n}} \sum_{x=1}^{n} \binom{K-1}{x-1}\binom{N-K}{n-x}$$

Since $N-K = (N-1)-(K-1),$ Vandermonde's identity applies again, this time with population size $N-1,$ $K-1$ successes, and sample size $n-1$:

$$\sum_{x=1}^{n} \binom{K-1}{x-1}\binom{N-K}{n-x} = \binom{N-1}{n-1}$$

Substituting this value into the expression for $E(X)$ gives:

$$E(X) = \frac{K}{\binom{N}{n}} \binom{N-1}{n-1}$$

From $\binom{N}{n} = \frac{N}{n}\binom{N-1}{n-1}$ we get $\binom{N-1}{n-1}/\binom{N}{n} = n/N,$ and the mean is:

$$\mu = E(X) = n\frac{K}{N}$$

The factor $K/N$ is the proportion of successes in the population. The expected count agrees with sampling with replacement, although the draws here are dependent.

## Variance of the hypergeometric distribution

The [variance](../variance-and-covariance-of-a-random-variable/) of a hypergeometric distribution measures the dispersion of the number of observed successes around the mean $\mu = nK/N.$ Its relation to the second moment is:

$$\sigma^{2} = \mathrm{Var}(X) = E(X^{2}) - [E(X)]^{2}$$

We write $X$ as the sum of $n$ indicator variables, one for each draw:

$$X = X_{1} + X_{2} + \cdots + X_{n}$$

The indicator $X_{i}$ is equal to $1$ if the $i$-th draw is a success and to $0$ otherwise. By symmetry, each position of the sample is equally likely to be occupied by any of the $N$ items of the population, so every indicator has expectation:

$$E(X_{i}) = P(X_{i} = 1) = \frac{K}{N}$$

Since $X_{i}$ is a [Bernoulli variable](../bernoulli-distribution/) with parameter $K/N,$ its variance is:

$$\mathrm{Var}(X_{i}) = \frac{K}{N}\left(1 - \frac{K}{N}\right)$$

Because the sampling is done without replacement, the indicators are not independent, and the variance of their sum has an additional covariance term for every pair of distinct draws:

$$\mathrm{Var}(X) = \sum_{i=1}^{n} \mathrm{Var}(X_{i}) + \sum_{i \neq j} \mathrm{Cov}(X_{i}, X_{j})$$

For $i \neq j,$ the product $X_{i}X_{j}$ is equal to $1$ exactly when draws $i$ and $j$ are both successes. Among the $N(N-1)$ ordered pairs of distinct population items, $K(K-1)$ consist of two successes. Hence:

$$E(X_{i}X_{j}) = P(X_{i} = 1, X_{j} = 1) = \frac{K}{N} \cdot \frac{K-1}{N-1}$$

The covariance of two distinct indicators is therefore:

$$
\begin{align}
\mathrm{Cov}(X_{i}, X_{j}) &= E(X_{i}X_{j}) - E(X_{i})E(X_{j}) \\[6pt]
&= \frac{K}{N} \cdot \frac{K-1}{N-1} - \frac{K^{2}}{N^{2}} \\[6pt]
&= -\frac{K}{N}\left(1 - \frac{K}{N}\right)\frac{1}{N-1}
\end{align}
$$

The covariance is negative because a success drawn in one position leaves fewer successes available for the others. Summing the $n$ variances and the $n(n-1)$ covariances we obtain:

$$
\begin{align}
\mathrm{Var}(X) &= n\frac{K}{N}\left(1 - \frac{K}{N}\right) - n(n-1)\frac{K}{N}\left(1 - \frac{K}{N}\right)\frac{1}{N-1} \\[6pt]
&= n\frac{K}{N}\left(1 - \frac{K}{N}\right)\left(1 - \frac{n-1}{N-1}\right) \\[6pt]
&= n\frac{K}{N}\left(1 - \frac{K}{N}\right)\frac{N-n}{N-1}
\end{align}
$$

> The factor $(N-n)/(N-1)$ is called the finite population correction. For $n > 1$ it is smaller than $1,$ so the variance is smaller than the [binomial variance](../binomial-distribution/) $np(1-p)$ with $p = K/N,$ and it vanishes when $n = N,$ because then the sample is the whole population and the number of successes is certain.

## Example 1

A batch contains $800$ items, of which 12% are defective. An inspector selects a simple random sample of $25$ items for quality control. The random variable $X$ is the number of defective items in the sample.

A selected item is not placed back into the batch, so its composition changes after every draw and the probability of selecting a defective item is not constant. The draws are therefore dependent. Since every sample of $25$ items is equally likely, the number of possible samples is:

$$\binom{800}{25}$$

The batch has $0.12 \times 800 = 96$ defective items and $800 - 96 = 704$ non-defective ones. The probability that the sample contains exactly $x$ defective items is:

$$P(X = x) = \frac{\binom{96}{x}\binom{704}{25-x}}{\binom{800}{25}}$$

Thus $X$ has a hypergeometric distribution with parameters $N = 800,$ $K = 96,$ and $n = 25.$ Its mean is $E(X) = 25 \times 96/800 = 3,$ so the inspector finds on average $3$ defective items in the sample.

## Comparison with the binomial distribution

The hypergeometric and [binomial distributions](../binomial-distribution/) both describe the number of successes observed in a fixed number of draws, but they use different sampling assumptions.

+ The binomial distribution assumes independent trials with a constant probability of success, as if each draw were taken from an infinite population or the sampled item were replaced before the next draw.
+ The hypergeometric distribution applies to sampling without replacement from a finite population, where each draw changes the composition of the remaining items, the probability of success varies across draws, and the outcomes are not independent.

If each item is replaced before the next draw, the draws are independent and the probability of success is always $K/N.$ The number of successes then has the exact distribution:

$$X \sim \mathrm{Bin}\left(n, \frac{K}{N}\right)$$

When the population size $N$ is large compared with the sample size $n,$ removing a few items barely changes the composition of the population. The hypergeometric distribution is then well approximated by a binomial distribution with parameter $p = K/N$:

$$\mathrm{Hyp}(N, K, n) \approx \mathrm{Bin}\left(n, \frac{K}{N}\right)$$

As a rule of thumb, the binomial approximation is used when the sampling fraction satisfies $n/N \le 0.05.$
