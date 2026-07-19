---
title: Poisson Distribution
source: https://algebrica.org/poisson-distribution/
license: CC BY-NC 4.0
tags:
  - binomial-distribution
  - cumulative-distribution-function
  - discrete-random-variables
  - expected-value
  - poisson-distribution
  - poisson-process
  - probability
  - probability-mass-function
  - statistics
  - variance
---
## Definition

The Poisson distribution is the [discrete probability distribution](../discrete-random-variables/) of a count observed in a fixed region of time or space. It is used when counts in disjoint subregions are independent, the average rate is constant, and two or more occurrences in a sufficiently small subregion are unlikely. Examples include the number of calls received in ten minutes, radioactive particles detected in one second, or defects found along one meter of wire.

A discrete random variable $X$ has a Poisson distribution with parameter $\lambda>0,$ written $X\sim\mathrm{Poisson}(\lambda),$ if its probability mass function is:

$$
P(X=x)=p(x;\lambda)=\frac{e^{-\lambda}\lambda^x}{x!},\qquad x=0,1,2,\ldots
$$

In this expression $x$ is the observed number of occurrences, $\lambda$ is the expected number of occurrences in the fixed interval, $e$ is [Euler's number](../euler-number-limit-sequence/), and $x!$ is the [factorial](../factorial/) of $x.$ Thus $\lambda$ is the mean count in the chosen interval. When a process has a rate of $\rho$ occurrences per unit of time, the count in an interval of length $t$ has parameter $\lambda=\rho t.$

The probability mass function has non-negative values. Its values also sum to $1,$ as required for every discrete probability distribution. The [Taylor series](../taylor-series/) of the exponential function gives:

$$
\sum_{x=0}^{\infty}P(X=x)=e^{-\lambda}\sum_{x=0}^{\infty}\frac{\lambda^x}{x!}=e^{-\lambda}e^{\lambda}=1
$$

## The Poisson process

A homogeneous Poisson process describes the times at which occurrences accumulate. Let $\rho>0$ be its intensity, measured in occurrences per unit of time, and let $R_1,R_2,\ldots$ be independent waiting times with the same exponential distribution:

$$
P(R_i>s)=e^{-\rho s},\qquad s\geq 0
$$

The time of the $n$th occurrence is the sum of the first $n$ waiting times:

$$
T_0=0,\qquad T_n=R_1+R_2+\cdots+R_n
$$

For $t\geq0,$ the counting random variable is:

$$
N(t)=\max\{\ n\geq0\mid T_n\leq t\ \}
$$

Thus $N(t)$ is the number of occurrences up to time $t.$ Its distribution is Poisson with parameter $\rho t:$

$$
N(t)\sim\mathrm{Poisson}(\rho t),\qquad P(N(t)=x)=\frac{e^{-\rho t}(\rho t)^x}{x!}
$$

Counts in disjoint time intervals are independent. More precisely, for $0\leq s<t,$ the increment $N(t)-N(s)$ counts the occurrences in $(s,t]$ and satisfies:

$$
N(t)-N(s)\sim\mathrm{Poisson}(\rho(t-s))
$$

The distribution of an increment therefore depends only on the length $t-s,$ not on the position of the interval. The process has stationary and independent increments. For a short interval of length $h,$ the Poisson increment formula gives:

$$
\begin{align}
P(N(t+h)-N(t)=1)&=\rho h+o(h) \\[6pt]
P(N(t+h)-N(t)\geq2)&=o(h)
\end{align}
$$

Here $o(h)$ denotes a quantity whose ratio to $h$ tends to zero as $h\to0,$ in the sense of [little-o notation](../little-o-notation/). These relations state precisely that the rate is $\rho$ and that two or more occurrences in a very short interval have negligible probability compared with the interval length.

For example, suppose that $N(t)$ has intensity $\rho=4.$ To find the probability of three occurrences by time $2$ and four by time $5,$ write the event in terms of counts on disjoint intervals:

$$
\{\ N(2)=3,N(5)=4\ \}=\{\ N(2)=3,N(5)-N(2)=1\ \}
$$

The first count has parameter $4\cdot2=8,$ while the second has parameter $4\cdot(5-2)=12.$ Independence gives:

$$
\begin{align}
P(N(2)=3,N(5)=4)
&=P(N(2)=3)P(N(5)-N(2)=1) \\[6pt]
&=\frac{e^{-8}8^3}{3!}\frac{e^{-12}12}{1!} \\[6pt]
&\approx0.0000021
\end{align}
$$

## Main properties

For $X\sim\mathrm{Poisson}(\lambda),$ the probability mass function, [expected value](../mean-or-expected-value-of-a-random-variable/), [variance](../variance-and-covariance-of-a-random-variable/), and [standard deviation](../variance/) are given below.

[class="table-1"]

|                                                                 |
| :-------------------------------------------------------------- |
| $P(X=x)=\dfrac{\lambda^xe^{-\lambda}}{x!},\quad x=0,1,2,\ldots$ |
| $\mu=E(X)=\lambda$                                              |
| $\sigma^2=\mathrm{Var}(X)=\lambda$                              |
| $\sigma=\sqrt{\lambda}$                                         |

[/class]

The equality $E(X)=\mathrm{Var}(X)$ is a necessary condition for an exact Poisson model. A persistent difference between the sample mean and sample variance can indicate that the Poisson assumptions do not fit the occurrence mechanism.

## Mean of the Poisson distribution

The expected value of $X$ is defined by:

$$
E(X)=\sum_{x=0}^{\infty}xP(X=x)
$$

Substitution of the probability mass function gives:

$$
E(X)=\sum_{x=0}^{\infty}x\frac{e^{-\lambda}\lambda^x}{x!}
$$

The term with $x=0$ is zero. For every $x\geq1,$ the identity $x/x!=1/(x-1)!$ gives:

$$
E(X)=e^{-\lambda}\lambda\sum_{x=1}^{\infty}\frac{\lambda^{x-1}}{(x-1)!}
$$

With $k=x-1,$ the exponential series yields:

$$
E(X)=e^{-\lambda}\lambda\sum_{k=0}^{\infty}\frac{\lambda^k}{k!}=e^{-\lambda}\lambda e^{\lambda}=\lambda
$$

Thus the expected count in the fixed interval is the parameter $\lambda.$

## Variance of the Poisson distribution

The variance can be computed from the second moment by using:

$$
\mathrm{Var}(X)=E(X^2)-[E(X)]^2
$$

The identity $x^2=x(x-1)+x$ separates the second moment into two sums:

$$
E(X^2)=\sum_{x=0}^{\infty}x(x-1)\frac{e^{-\lambda}\lambda^x}{x!}+\sum_{x=0}^{\infty}x\frac{e^{-\lambda}\lambda^x}{x!}
$$

The second sum is $E(X)=\lambda.$ In the first sum the terms with $x=0$ and $x=1$ are zero. Cancelling $x(x-1)$ against $x!$ and setting $k=x-2$ gives:

$$
\sum_{x=2}^{\infty}\frac{e^{-\lambda}\lambda^x}{(x-2)!}=\lambda^2e^{-\lambda}\sum_{k=0}^{\infty}\frac{\lambda^k}{k!}=\lambda^2
$$

Hence $E(X^2)=\lambda^2+\lambda,$ and therefore:

$$
\mathrm{Var}(X)=\lambda^2+\lambda-\lambda^2=\lambda
$$

The standard deviation is the positive square root $\sqrt{\lambda}.$

## Cumulative Poisson distribution

For a non-negative integer $r,$ the [cumulative distribution function](../discrete-random-variables/) gives the probability of at most $r$ occurrences:

$$
F(r;\lambda)=P(X\leq r)=e^{-\lambda}\sum_{x=0}^{r}\frac{\lambda^x}{x!}
$$

The same function gives upper-tail and interval probabilities. For integers $1\leq a\leq b,$ we have:

$$
\begin{align}
&P(X\geq a)=1-F(a-1;\lambda) \\[6pt]
&P(a\leq X\leq b)=F(b;\lambda)-F(a-1;\lambda)
\end{align}
$$

Cumulative Poisson tables list precomputed values of $F(r;\lambda)$ for selected values of $r$ and $\lambda.$ A small portion of such a table is shown below.

| $\lambda$ | $r=0$ | $1$ | $2$ | $3$ | $4$ | ... |
| :-------- | :---- | :-- | :-- | :-- | :-- | :-- |
| 0.02 | 0.980 | 1.000 | | | | ... |
| 0.04 | 0.961 | 0.999 | 1.000 | | | ... |
| 0.06 | 0.942 | 0.998 | 1.000 | | | ... |
| 0.08 | 0.923 | 0.997 | 1.000 | | | ... |
| 0.10 | 0.905 | 0.995 | 1.000 | | | ... |
| 0.15 | 0.861 | 0.990 | 0.999 | 1.000 | | ... |
| ... | ... | ... | ... | ... | ... | ... |

The entry in row $\lambda$ and column $r$ is $P(X\leq r).$ Blank cells in this shortened table correspond to values that round to $1.000$ at three decimal places.

## Computing a Poisson probability

Suppose a call center receives an average of five calls every ten minutes. We find the probability that exactly eight calls arrive during a ten-minute interval, assuming independent arrivals at a constant rate.

Let $X$ count the calls received in ten minutes. Then $X\sim\mathrm{Poisson}(5),$ and direct substitution gives:

$$
P(X=8)=\frac{e^{-5}5^8}{8!}=\frac{e^{-5}390625}{40320}\approx0.0653
$$

The probability is approximately $0.0653,$ or $6.53\%.$

The same probability can be recovered from a cumulative table. For $\lambda=5,$ suppose the table gives:

$$
\begin{align}
P(X\leq8)&=0.9319 \\[6pt]
P(X\leq7)&=0.8666
\end{align}
$$

The probability of exactly eight calls is the difference between these cumulative probabilities:

$$
P(X=8)=P(X\leq8)-P(X\leq7)=0.9319-0.8666=0.0653
$$

## From the binomial to the Poisson distribution

The Poisson distribution is the limit of the [binomial distribution](../binomial-distribution/) when the number of trials tends to infinity and the probability of success tends to zero while the expected number of successes remains fixed. Divide a fixed interval into $n$ subintervals and assume that:

+ Each subinterval contains at most one occurrence.
+ The probability of one occurrence in a subinterval is $p=\lambda/n.$
+ Counts in distinct subintervals are independent.

Under these assumptions the total count $X$ has a binomial distribution with parameters $n$ and $p.$ For a fixed non-negative integer $x,$ its probability is:

$$
P(X=x)=\binom{n}{x}p^x(1-p)^{n-x}
$$

After substituting $p=\lambda/n$ and expanding the [binomial coefficient](../binomial-coefficient/), the probability becomes:

$$
\begin{align}
P(X=x)
&=\binom{n}{x}\left(\frac{\lambda}{n}\right)^x\left(1-\frac{\lambda}{n}\right)^{n-x} \\[6pt]
&=\frac{n!}{x!(n-x)!}\frac{\lambda^x}{n^x}\left(1-\frac{\lambda}{n}\right)^n\left(1-\frac{\lambda}{n}\right)^{-x}
\end{align}
$$

As $n\to\infty,$ with $x$ and $\lambda$ fixed, the factors that depend on $n$ have the [limits](../limits/):

$$
\frac{n!}{n^x(n-x)!}\to1,\qquad \left(1-\frac{\lambda}{n}\right)^n\to e^{-\lambda},\qquad \left(1-\frac{\lambda}{n}\right)^{-x}\to1
$$

It follows that:

$$
\lim_{n\to\infty}P(X=x)=\frac{e^{-\lambda}\lambda^x}{x!}
$$

For finite $n,$ this limit supports the Poisson approximation to a binomial count when $n$ is large, $p$ is small, and $np=\lambda.$
