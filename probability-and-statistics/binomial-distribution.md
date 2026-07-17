---
title: Binomial Distribution
source: https://algebrica.org/binomial-distribution/
license: CC BY-NC 4.0
tags:
  - bernoulli-distribution
  - binomial-distribution
  - discrete-random-variables
  - expected-value
  - normal-approximation
  - probability
  - probability-mass-function
  - statistics
  - variance
---
## Definition

The binomial distribution is a discrete probability distribution that models the number of successes in a fixed sequence of independent [Bernoulli trials](../bernoulli-distribution/) with the same probability of success. Its parameters are an integer $n \ge 1,$ the number of trials, and a probability $p \in [0,1].$ For every $x \in \{0,1,\ldots,n\},$ the model gives the probability of observing exactly $x$ successes. An experiment of this type has the following properties:

+ Each trial has exactly two mutually exclusive outcomes: success, with probability $p,$ and failure, with probability $1-p.$
+ The trials are independent.
+ The probability of success $p$ is constant across all trials.
+ The number of trials $n$ is fixed in advance.
+ The random variable $X$ is the number of successes in the $n$ trials.

The probability of obtaining exactly $x$ successes in $n$ trials is:

$$P(X = x) = b(x; n, p) = \binom{n}{x} p^{x} q^{n-x}$$

In this expression $q = 1-p$ is the probability of failure. Each fixed arrangement of $x$ successes and $n-x$ failures has probability $p^{x}q^{n-x},$ while the [binomial coefficient](../binomial-coefficient/) $\binom{n}{x}$ counts these arrangements. For every $x \notin \{0,1,\ldots,n\},$ the probability $P(X = x)$ is zero. When $p=0$ or $p=1,$ the distribution is degenerate because the number of successes is certain.

Since $p + q = 1,$ the binomial model satisfies the condition required of any probability distribution:

$$\sum_{x=0}^{n} b(x; n, p) = (p+q)^{n} = 1$$

> The binomial distribution is related to the [binomial theorem](../binomial-theorem/), because the expansion of $(p+q)^{n}$ contains one term for each possible number of successes $x,$ and that term is exactly $b(x; n, p).$

- - -

For $X \sim \mathrm{Bin}(n, p),$ the probability mass function, mean, variance, and standard deviation are given below.

[class="table-1"]

|                                                                               |
| ----------------------------------------------------------------------------- |
| $P(X = x) = b(x; n, p) = \binom{n}{x} p^{x} q^{n-x} \quad x = 0, 1, \dots, n$  |
| $\mu = E(X) = np$                                                              |
| $\sigma^{2} = \mathrm{Var}(X) = np(1-p)$                                       |
| $\sigma = \sqrt{np(1-p)}$                                                      |

[/class]

## Mean of the binomial distribution

The [mean](../introduction-to-the-mean/), or [expected value](../mean-or-expected-value-of-a-random-variable/), of a binomial distribution is the average number of successes expected over a large number of repetitions of the experiment. We start from the definition of the expected value:

$$\mu = E(X) = \sum_{x=0}^{n} xP(X = x)$$

Substituting the probability mass function of the binomial distribution we have:

$$E(X) = \sum_{x=0}^{n} x\binom{n}{x} p^{x} (1-p)^{n-x}$$

We use the identity:

$$x\binom{n}{x} = n\binom{n-1}{x-1}$$

This identity relates two binomial coefficients by lowering both $n$ and $x$ by one. Applying it to each term of the sum and collecting the factor $np$ we obtain:

$$E(X) = np \sum_{x=1}^{n} \binom{n-1}{x-1} p^{x-1} (1-p)^{(n-1)-(x-1)}$$

The summation is equal to $1,$ because it is the total probability of a binomial distribution with parameters $n-1$ and $p.$ Therefore:

$$\mu = E(X) = np$$

For fixed $p,$ the mean is proportional to the number of trials, and for fixed $n$ it is proportional to the probability of success. The expected number of successes among the $n$ trials is $np.$

- - -

The same result follows by writing the binomial variable $X$ as the sum of $n$ independent Bernoulli variables $X_1, X_2, \ldots, X_n,$ each equal to $1$ (success) with probability $p$ and to $0$ (failure) with probability $1-p$:

$$X = X_1 + X_2 + \cdots + X_n$$

Each term has expected value $E(X_i) = p,$ so by the [linearity of expectation](../mean-or-expected-value-of-a-random-variable/):

$$E(X) = E(X_1) + E(X_2) + \cdots + E(X_n) = np$$

## Variance of the binomial distribution

The [variance](../variance-and-covariance-of-a-random-variable/) of a binomial distribution is the expected squared deviation of the number of successes from the mean $\mu = np.$ It can be computed from the second moment:

$$\sigma^{2} = \mathrm{Var}(X) = E(X^{2}) - [E(X)]^{2}$$

To compute it, we write $X$ again as the sum of $n$ independent Bernoulli variables $X_1, X_2, \ldots, X_n,$ each with probability of success $p$:

$$X = X_1 + X_2 + \cdots + X_n$$

A Bernoulli variable has variance $\mathrm{Var}(X_i) = p(1-p),$ and the trials are independent, so the variance of the sum is the sum of the variances:

$$\mathrm{Var}(X) = \mathrm{Var}(X_1) + \mathrm{Var}(X_2) + \cdots + \mathrm{Var}(X_n)$$

Each of the $n$ terms is equal to $p(1-p) = pq,$ and the variance of the binomial distribution is:

$$\sigma^{2} = npq = np(1-p)$$

> For fixed $p,$ the variance grows linearly with the number of trials $n.$ For fixed $n$ it has its maximum at $p = 1/2$ and vanishes when $p = 0$ or $p = 1,$ because in those cases the outcome of every trial is certain.

## Example 1

A factory produces electronic sensors, and each sensor is tested to verify whether it operates correctly under specific temperature conditions. Suppose that $6$ sensors are selected at random from a production batch. Assume that their test outcomes are independent and that each sensor passes the test with probability $p = 0.7.$ We want the probability that exactly $4$ of the $6$ sensors function properly during the test.

Since the tests are independent, the number of sensors that pass the test follows a binomial distribution with $n = 6$ and $p = 0.7,$ and the required probability is:

$$
\begin{align}
b(4; 6, 0.7) &= \binom{6}{4} (0.7)^{4} (0.3)^{2} \\[6pt]
&= \frac{6!}{4!2!} (0.7)^{4} (0.3)^{2} \\[6pt]
&= 15 \times 0.2401 \times 0.09 = 0.324135
\end{align}
$$

> For an integer $m \ge 1,$ the [factorial](../factorial/) $m!$ is the product of the positive integers from $1$ to $m.$ By convention, $0! = 1.$

Therefore, the probability that exactly four sensors out of six pass the test is approximately $0.324,$ or 32.4%.

## Cumulative binomial distribution

In some problems the goal is not the probability of exactly $x$ successes, but the probability of at most $r$ successes in $n$ Bernoulli trials. For an integer $r \in \{0,1,\ldots,n\},$ this probability is obtained by summing the terms of the binomial distribution from $x = 0$ to $x = r$:

$$B(r; n, p) = \sum_{x=0}^{r} b(x; n, p)$$

In this expression $b(x; n, p)$ is the probability mass function of the binomial distribution. Writing out the probability mass function, the cumulative probability is:

$$P(X \le r) = B(r; n, p) = \sum_{x=0}^{r} \binom{n}{x} p^{x} (1-p)^{n-x}$$

The same cumulative function gives upper-tail and interval probabilities by complementation. For integers $0 \le a \le b \le n,$ we have:

$$P(X \ge a) = 1-B(a-1; n, p) \quad \text{and} \quad P(a \le X \le b) = B(b; n, p)-B(a-1; n, p)$$

Here $B(-1; n, p) = 0$ by convention.

Cumulative binomial tables list pre-computed values of $P(X \le r)$ for selected combinations of $n$ and $p,$ in the same way that the [standard normal Z table](../standard-normal-z-table/) lists cumulative probabilities of the [normal distribution](../normal-distribution/). A simplified portion of such a table is shown below.

| $n$ | $r$ | $p = 0.05$ | $p = 0.10$ | $p = 0.20$ | $p = 0.30$ | $p = 0.40$ | $p = 0.50$ | ... |
| --- | --- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | --- |
| $1$ | $0$ | 0.950      | 0.900      | 0.800      | 0.700      | 0.600      | 0.500      | ... |
| $1$ | $1$ | 1.000      | 1.000      | 1.000      | 1.000      | 1.000      | 1.000      | ... |
| $2$ | $0$ | 0.903      | 0.810      | 0.640      | 0.490      | 0.360      | 0.250      | ... |
| $2$ | $1$ | 0.998      | 0.990      | 0.960      | 0.910      | 0.840      | 0.750      | ... |
| $2$ | $2$ | 1.000      | 1.000      | 1.000      | 1.000      | 1.000      | 1.000      | ... |
| ... | ... | ...        | ...        | ...        | ...        | ...        | ...        | ... |

The intersection of a row and a column gives the cumulative probability $P(X \le r),$ that is, the probability of obtaining at most $r$ successes for the corresponding values of $n$ and $p.$ The table replaces the term-by-term computation of the sum.

## Normal approximation of the binomial distribution

The binomial distribution is discrete, but it can be approximated by a continuous [normal distribution](../normal-distribution/) when the expected numbers of successes and failures are both sufficiently large. The inequalities $np \ge 5$ and $n(1-p) \ge 5$ are a common preliminary criterion, although the required accuracy depends on the problem. Under these conditions, if $X \sim \mathrm{Bin}(n,p),$ we approximate its distribution by that of a normal random variable $Y$ with the same mean and variance:

$$Y \sim \mathcal{N}(np,npq)$$

The approximation simplifies the calculations, because binomial probabilities can then be estimated with the [Z tables](../standard-normal-z-table/) of the normal distribution.

- - -

Fix $p \in (0,1)$ and, for each $n,$ let $X_n \sim \mathrm{Bin}(n,p).$ The de Moivre-Laplace theorem states that the standardized variables converge in distribution to the [standard normal distribution](../normal-distribution/):

$$Z_n = \frac{X_n-np}{\sqrt{np(1-p)}} \xrightarrow{d} \mathcal{N}(0,1) \quad \text{as } n \to \infty$$

> The symbol $\xrightarrow{d}$ denotes convergence in distribution, which means that the distributions of the standardized variables approach the standard normal distribution as $n$ increases.

## Example 2

To illustrate the normal approximation, consider a company that produces small electronic components. During quality control each item is tested to check whether it meets the required electrical specifications. Suppose that $100$ components are tested, their outcomes are independent, and each component passes with probability $p = 0.9.$ We want the probability that between $85$ and $92$ components pass the inspection.

Let $X$ be the number of components that pass the test. The required probability is:

$$P(85 \le X \le 92) = \sum_{x=85}^{92} b(x; 100, 0.9)$$

Here $np = 90$ and $n(1-p) = 10,$ so both expected counts satisfy the preliminary criterion for the normal approximation. The approximating distribution has:

$$
\begin{align}
\mu &= np = 100 \times 0.9 = 90 \\[6pt]
\sigma &= \sqrt{npq} = \sqrt{100 \times 0.9 \times 0.1} = 3
\end{align}
$$

The binomial variable $X$ is discrete, because it takes only [integer](../integers/) values, while the normal distribution is continuous. The probability that $X$ lies between $85$ and $92$ is therefore better approximated by the area under the normal curve from half a unit below $85$ to half a unit above $92,$ and we replace the discrete bounds with:

$$x_1 = 84.5 \quad \text{and} \quad x_2 = 92.5$$

We standardize the bounds with the [transformation](../normal-distribution/) $z = (x-\mu)/\sigma$:

$$z_1 = \frac{84.5 - 90}{3} \approx -1.83 \quad \text{and} \quad z_2 = \frac{92.5 - 90}{3} \approx 0.83$$

In terms of the standardized variable $Z$ the probability becomes:

$$P(85 \le X \le 92) = \sum_{x=85}^{92} b(x; 100, 0.9) \approx P(-1.83 \le Z \le 0.83)$$

The probability of the interval is the difference of two cumulative probabilities:

$$P(-1.83 \le Z \le 0.83) = P(Z \le 0.83) - P(Z \le -1.83)$$

The [standard normal Z table](../standard-normal-z-table/) gives:

$$P(Z \le 0.83) \approx 0.7967 \quad \text{and} \quad P(Z \le -1.83) \approx 0.0336$$

Subtracting the two values we obtain:

$$P(-1.83 \le Z \le 0.83) \approx 0.7967 - 0.0336 = 0.7631$$

Therefore, the continuity-corrected normal approximation gives $0.763,$ or 76.3%, for the probability that between $85$ and $92$ components pass the quality test.

For comparison, direct evaluation of the binomial sum gives approximately $0.7541.$ The reported normal approximation therefore exceeds the exact binomial probability by about $0.0090.$

## Comparison between the binomial and hypergeometric distributions

The binomial distribution applies when each trial has the same probability of success and no trial influences the next. This setting is exact for sampling with replacement. For sampling without replacement from a finite population, the binomial distribution can be an approximation when the sample size is small relative to the population size. Otherwise the composition of the population changes appreciably after each draw, and the [hypergeometric distribution](../hypergeometric-distribution/) is the exact model.

When the sampling fraction $n/N$ is not negligible, the probability of success changes across trials, and the finite-population model is:

$$X \sim \mathrm{Hyp}(N, K, n)$$

In this notation $K$ is the number of successes in the population. The binomial model has independent trials with a fixed probability of success, while the hypergeometric model describes sampling without replacement.

## Connection between the binomial and the Poisson distribution

Fix $\lambda > 0$ and an integer $x \ge 0.$ For each $n,$ set $p_n = \lambda/n$ and let $X_n \sim \mathrm{Bin}(n,p_n).$ As $n$ tends to infinity, the binomial probability converges to the corresponding probability of the [Poisson distribution](../poisson-distribution/):

$$\lim_{n \to \infty}P(X_n = x) = \lim_{n \to \infty}\binom{n}{x}\left(\frac{\lambda}{n}\right)^{x}\left(1-\frac{\lambda}{n}\right)^{n-x} = \frac{e^{-\lambda}\lambda^{x}}{x!}$$

> The Poisson limit models rare events, that is, events with a small probability of occurring in each of a large number of independent trials.
