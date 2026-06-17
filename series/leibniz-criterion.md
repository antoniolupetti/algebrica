---
title: Leibniz Criterion
source: https://algebrica.org/leibniz-criterion/
license: CC BY-NC 4.0
tags:
  - alternating-series
  - convergence
  - leibniz-criterion
  - series
---
## What is Leibniz’s criterion used for

Leibniz’s criterion studies the convergence of alternating [series](../series/), composed of infinitely many terms that alternate in sign. Consider the alternating series:

$$
\sum_{n=1}^{+\infty} (-1)^n a_n
$$

In this expression $a_n \geq 0$ for every $n \in \mathbb{N}$. Leibniz’s criterion states that the series converges if the following conditions are satisfied:

+ the [sequence](../sequences/) $\{a_n\}$ is infinitesimal, so its [limit](../limits/) is zero, $\lim_{n \to +\infty} a_n = 0$
+ the sequence $\{a_n\}$ is eventually [non-increasing](../monotone-sequences/), so there exists an index $n_0$ such that $a_{n+1} \leq a_n$ for every $n \geq n_0$

In practice, the criterion allows one to establish the convergence of a series based solely on the verification of the above conditions. However, the test is not generalizable and applies only to alternating series. If the series

$$
\sum_{k=1}^{+\infty} (-1)^k a_k
$$

is convergent and $S$ is its sum, then for every $n \in \mathbb{N}$, the error made by truncating the series at the $n$-th term is at most equal to the next term $a_{n+1}$:

$$
\left| S - \sum_{k=1}^{n} (-1)^k a_k \right| \leq a_{n+1}
$$

This means that if you are summing the alternating [harmonic series](../harmonic-series/):

$$
\sum_{n=1}^{+\infty} \frac{(-1)^n}{n}
$$

and you stop at the term $n = 10$, then the maximum error you are making is:

$$
\left| S - \sum_{k=1}^{10} \frac{(-1)^k}{k} \right| \leq \frac{1}{11}
$$

The convergence guaranteed by the criterion is in general conditional and not absolute. The alternating [harmonic series](../harmonic-series/) makes this clear, since it converges while the corresponding series of [absolute values](../absolute-value/), the harmonic series, diverges. Leibniz’s criterion therefore establishes convergence in cases where every test based on absolute values fails.

> Leibniz’s criterion only tells us whether an alternating series converges, it provides no information about the actual sum of the series. To compute the sum, one must use other tools such as [Taylor](../taylor-series/) or Maclaurin series expansions, when available.

## Proof

Let $\{a_n\}$ be a sequence of [positive real numbers](../series-with-positive-terms/) such that $a_{n+1} \leq a_n$ for every $n$, and $\lim_{n \to \infty} a_n = 0$. We consider the alternating series:

$$
\sum_{n=1}^{\infty} (-1)^{n+1} a_n
$$

and aim to prove that it converges.

> The leading term is taken positive here for convenience. The same argument applies when the series begins with a negative term, since multiplying every partial sum by $-1$ leaves convergence unaffected.

- - -

To do this, we examine the sequence of partial sums:

$$
S_n = \sum_{k=1}^{n} (-1)^{k+1} a_k
$$

We analyze this sequence by distinguishing between the even and odd partial sums. When $n$ is even, say $n = 2m$, the sum becomes:

$$
S_{2m} = a_1 - a_2 + a_3 - a_4 + \cdots + a_{2m-1} - a_{2m}.
$$

Grouping the terms in pairs gives:

$$
S_{2m} = (a_1 - a_2) + (a_3 - a_4) + \cdots + (a_{2m-1} - a_{2m}).
$$

Since the sequence $\{a_n\}$ is decreasing, each difference $a_k - a_{k+1}$ is non-negative. Each pair in the grouped sum is therefore non-negative, and the subsequence $\{S_{2m}\}$ is increasing. The same sum can be regrouped as

$$
S_{2m} = a_1 - (a_2 - a_3) - (a_4 - a_5) - \cdots - a_{2m},
$$

where every parenthesis is non-negative, so $S_{2m} \leq a_1$. The subsequence $\{S_{2m}\}$ is increasing and bounded above, hence it converges. Next, we observe that the odd partial sums can be written as

$$
S_{2m+1} = S_{2m} + a_{2m+1}.
$$

A symmetric grouping shows that $\{S_{2m+1}\}$ is decreasing, and the identity above gives $S_{2m+1} \geq S_{2m}$, so every odd partial sum lies above every even one. The even sums increase, the odd sums decrease, and they enclose one another, which means the two subsequences define a nested family of intervals whose lengths $a_{2m+1}$ shrink to zero.

Since $\lim_{n \to \infty} a_n = 0$, the difference between $S_{2m+1}$ and $S_{2m}$ tends to zero as $m \to \infty$, so both subsequences $\{S_{2m}\}$ and $\{S_{2m+1}\}$ converge to the same limit. The full sequence $\{S_n\}$ of partial sums therefore converges, and the alternating series is convergent.

## Example

Consider the following alternating series:

$$
\sum_{n=1}^{+\infty} \frac{(-1)^n}{n!}
$$

We define $a_n = \frac{1}{n!}$ and study the [absolute values](../absolute-value/) of the terms, which is what Leibniz’s criterion requires. To apply Leibniz’s criterion, we need to verify three conditions. First, the terms $a_n$ are all positive for every $n \in \mathbb{N}.$ Second, the sequence $\{a_n\}$ is decreasing. Since the [factorial](../factorial/) function grows rapidly, we have:

$$
a_{n+1} = \frac{1}{(n+1)!} < \frac{1}{n!} = a_n
$$

This confirms that the sequence is strictly decreasing. Third, the limit of the general term is zero:

$$
\lim_{n \to +\infty} \frac{1}{n!} = 0
$$

Since all three conditions are satisfied, Leibniz’s criterion ensures that the following series converges.

$$
\sum_{n=1}^{+\infty} \frac{(-1)^n}{n!}
$$


## Why monotonicity cannot be dropped

The hypothesis that $\{a_n\}$ is eventually non-increasing is essential and cannot be relaxed to mere convergence of $a_n$ to zero. Suppose we only require that $a_n$ is positive and infinitesimal. Decompose the general term as:

$$
a_n = b_n + c_n
$$

where $b_n$ is positive, decreasing, and infinitesimal, while $c_n$ is infinitesimal but not monotone. The series $\sum (-1)^n b_n$ converges by Leibniz’s criterion, so the convergence of $\sum (-1)^n a_n$ depends on $\sum (-1)^n c_n$. The latter can diverge, and in that case the full series diverges as well, even though $a_n \to 0.$

An example is the sequence:

$$
a_n = \frac{1}{\sqrt{n}} + \frac{(-1)^n}{n}
$$

which is positive and tends to zero, but is not eventually monotone. The associated alternating series

$$
\sum_{n=2}^{+\infty} (-1)^n a_n = \sum_{n=2}^{+\infty} \frac{(-1)^n}{\sqrt{n}} + \sum_{n=2}^{+\infty} \frac{1}{n}
$$

splits into a convergent part and the harmonic tail, which diverges. The whole series therefore diverges, which shows that the limit condition alone does not guarantee convergence.

## Relation to Dirichlet’s criterion

Leibniz’s criterion is a special case of Dirichlet’s criterion for series. Dirichlet’s criterion states that $\sum a_n b_n$ converges whenever $\{a_n\}$ is monotone and infinitesimal and the partial sums of $\{b_n\}$ are bounded. 

Taking $b_n = (-1)^n$, the partial sums $\sum_{k=1}^{n} (-1)^k$ alternate between $-1$ and $0$, so they are bounded by $1$. With $\{a_n\}$ monotone and infinitesimal, the hypotheses of Dirichlet’s criterion are met, and convergence of the alternating series follows at once. Leibniz’s criterion is thus the instance of Dirichlet’s criterion obtained for the bounded oscillating factor $(-1)^n$.