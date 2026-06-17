---
title: Telescoping Series
source: https://algebrica.org/telescoping-series/
license: CC BY-NC 4.0
tags:
  - partial-fractions
  - partial-sums
  - series
  - telescoping-series
---
## Definition

A telescoping series is a [series](../series/) whose general term can be written as the difference of two consecutive values of an auxiliary [sequence](../sequences/). When the terms are added, each negative part cancels the positive part of the following term, and the partial sum collapses to a few surviving terms. The name comes from a hand telescope, which folds down to a fraction of its extended length when the inner tubes slide into one another.

Suppose the general term of a series has the form:

$$
a_k = b_k - b_{k+1}
$$

for some sequence $\{b_k\}$. The partial sum of the first $n$ terms then reduces to two terms:

$$
\begin{align}
S_n = \sum_{k=1}^{n} a_k &= (b_1 - b_2) + (b_2 - b_3) + (b_3 - b_4) + \dots + (b_n - b_{n+1}) \\[6pt]
&= b_1 - b_{n+1}
\end{align}
$$

Every interior term appears once with a plus sign and once with a minus sign, so only the first and the last value remain. The difficulty of a telescoping problem lies in recognizing the sequence $\{b_k\}$, since once the term is rewritten as a difference the sum is immediate.

## Convergence of the infinite series

The behavior of the infinite series depends only on the limit of the auxiliary sequence. From the partial sum $S_n = b_1 - b_{n+1}$, the infinite series converges exactly when $\{b_{n+1}\}$ has a finite limit:

$$
\sum_{k=1}^{\infty} (b_k - b_{k+1}) = b_1 - \lim_{n \to \infty} b_{n+1}
$$

If $b_n \to L$ as $n \to \infty$, the sum equals $b_1 - L$. If the sequence has no finite limit, the series diverges. A telescoping series therefore turns a question about an infinite sum into a question about a single limit, the limit of the sequence that generates the differences.

## Example

We evaluate the finite sum of reciprocals of consecutive products:

$$
\frac{1}{1 \cdot 2} + \frac{1}{2 \cdot 3} + \frac{1}{3 \cdot 4} + \dots + \frac{1}{99 \cdot 100}
$$

The general term is $\frac{1}{k(k+1)}$. Decomposing it into [partial fractions](../partial-fraction-decomposition/) expresses it as a difference:

$$
\frac{1}{k(k+1)} = \frac{1}{k} - \frac{1}{k+1}
$$

This matches the telescoping form with $b_k = \frac{1}{k}$. Substituting the decomposition into the sum and letting the interior terms cancel gives:

$$
\begin{align}
\sum_{k=1}^{99} \frac{1}{k(k+1)} &= \left( 1 - \frac{1}{2} \right) + \left( \frac{1}{2} - \frac{1}{3} \right) + \dots + \left( \frac{1}{99} - \frac{1}{100} \right) \\[6pt]
&= 1 - \frac{1}{100} = \frac{99}{100}
\end{align}
$$

The same decomposition handles the infinite series. Here $b_{n+1} = \frac{1}{n+1} \to 0$, so the sum converges:

$$
\sum_{k=1}^{\infty} \frac{1}{k(k+1)} = 1 - \lim_{n \to \infty} \frac{1}{n+1} = 1
$$

This convergent value, the Mengoli sum, makes $\sum \frac{1}{n(n+1)}$ a standard model for the [comparison test](../series-with-positive-terms/) and the [asymptotic comparison test](../asymptotic-comparison-test/), where a more involved positive-term series is matched against it.

## A fixed gap between the cancelling terms

In the basic form each term cancels against its immediate successor, and a single value survives. The same mechanism works when the two parts of the difference are separated by a fixed number of positions. Suppose the general term has the form:

$$
a_k = b_k - b_{k+p}
$$

for a fixed integer $p \geq 1$. The positive parts of the partial sum run through $b_1, b_2, \dots, b_n$, while the negative parts run through $b_{1+p}, b_{2+p}, \dots, b_{n+p}$. The two ranges overlap on the indices from $1+p$ to $n$, where the cancellation takes place, and a block of $p$ terms survives at each end:

$$
S_n = \sum_{k=1}^{n} (b_k - b_{k+p}) = (b_1 + b_2 + \dots + b_p) - (b_{n+1} + b_{n+2} + \dots + b_{n+p})
$$

The leading block $b_1 + \dots + b_p$ is fixed, so convergence depends only on the trailing block. If $b_n \to L$, each of the $p$ final terms tends to $L$, and the series sums to:

$$
\sum_{k=1}^{\infty} (b_k - b_{k+p}) = (b_1 + b_2 + \dots + b_p) - pL
$$

When $L = 0$ the sum is the leading block $b_1 + \dots + b_p$. The consecutive case of the previous sections corresponds to $p = 1$, where the block reduces to the single term $b_1$.

A partial fraction decomposition often produces this pattern, with the gap fixed by the distance between the factors of the denominator. We evaluate the infinite sum:

$$
\sum_{k=1}^{\infty} \frac{1}{k(k+2)}
$$

The factors $k$ and $k+2$ stand two positions apart, so the decomposition splits the term into a difference with gap $p = 2$:

$$
\frac{1}{k(k+2)} = \frac{1}{2} \left( \frac{1}{k} - \frac{1}{k+2} \right)
$$

This matches the gap form with $b_k = \frac{1}{k}$ and an overall factor $\frac{1}{2}$. Since $b_k \to 0$, only the leading block of two terms survives, and the sum is:

$$
\sum_{k=1}^{\infty} \frac{1}{k(k+2)} = \frac{1}{2} (b_1 + b_2) = \frac{1}{2} \left( 1 + \frac{1}{2} \right) = \frac{3}{4}
$$

The factor $\frac{1}{2}$ from the decomposition multiplies the whole result, a step that disappears in the Mengoli case where the two factors are adjacent and the constant equals $1$.

## A telescoping series with factorials

Telescoping is not restricted to fractions. Consider the sequence $a_k = (k^2 + 1) \, k!$ and the partial sums $b_k = a_1 + a_2 + \dots + a_k$. We find a closed form for $b_k$.

The key step rewrites the general term as a difference of consecutive multiples of [factorials](../factorial/). Starting from $a_k$ and using $k \cdot k! = (k+1)! - k!$, we get:

$$
\begin{align}
(k^2 + 1) \, k! &= k(k \cdot k!) + k! \\[6pt]
&= k \left[ (k+1)! - k! \right] + k! \\[6pt]
&= k(k+1)! - k \cdot k! + k! \\[6pt]
&= k(k+1)! - (k-1) \, k!
\end{align}
$$

The right side is the difference $c_{k+1} - c_k$ with $c_k = (k-1) \, k!$, since $c_{k+1} = k(k+1)!$. Summing from $1$ to $k$ collapses the partial sum to its final term, because $c_1 = 0 \cdot 1! = 0$:

$$
b_k = \sum_{j=1}^{k} (c_{j+1} - c_j) = c_{k+1} - c_1 = k(k+1)!
$$

This closed form simplifies ratios involving the partial sums. For instance, the quotient of a term and the running total is:

$$
\frac{a_k}{b_k} = \frac{(k^2 + 1) \, k!}{k(k+1)!} = \frac{k^2 + 1}{k(k+1)} = \frac{k^2 + 1}{k^2 + k}
$$

At $k = 100$ this gives $\frac{a_{100}}{b_{100}} = \frac{10001}{10100}$, a ratio already in lowest terms.

## Telescoping products

The cancellation that simplifies a telescoping sum has a multiplicative counterpart, where consecutive factors cancel instead of consecutive terms. We evaluate the product:

$$
\prod_{k=2}^{N} \frac{k^2}{k^2 - 1}
$$

Factoring the denominator as $k^2 - 1 = (k-1)(k+1)$ splits each factor into two ratios:

$$
\frac{k^2}{(k-1)(k+1)} = \frac{k}{k-1} \cdot \frac{k}{k+1}
$$

The product separates into two telescoping products, one rising and one falling:

$$
\prod_{k=2}^{N} \frac{k}{k-1} = \frac{N}{1}, \qquad \prod_{k=2}^{N} \frac{k}{k+1} = \frac{2}{N+1}
$$

In the first product each numerator cancels the denominator of the next factor, leaving $N$ over the initial denominator $1$. In the second the cancellation runs the other way, leaving the initial numerator $2$ over the final denominator $N+1$. Multiplying the two surviving fractions gives the value of the product:

$$
\prod_{k=2}^{N} \frac{k^2}{k^2 - 1} = \frac{N}{1} \cdot \frac{2}{N+1} = \frac{2N}{N+1}
$$

As $N \to \infty$ this approaches $2$, so the infinite product converges to $2$.
