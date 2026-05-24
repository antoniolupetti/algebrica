---
title: Monotone Sequences
source: https://algebrica.org/monotone-sequences/
license: CC BY-NC 4.0
tags:
  - bounded-sequence
  - harmonic-series
  - monotone-convergence-theorem
  - monotone-sequence
  - sequence
  - supremum-and-infimum
---

## Definition

A [sequence](../sequences/) of real numbers may exhibit a particularly regular pattern of
growth or decay: each term may be consistently larger than the previous one, or
consistently smaller. Sequences with this property are called monotone. Let
$\{a_n\}_{n \in \mathbb{N}}$ be a sequence of real numbers. The sequence is said to
be monotonically increasing if the following condition holds for every index:

$$ a_n \leq a_{n+1} \quad  \forall  n \in \mathbb{N} $$

If the inequality is strict, the sequence is called strictly increasing. Similarly, the
sequence is monotonically decreasing if the reverse holds for every index:

$$ a_n \geq a_{n+1} \quad \forall  n \in \mathbb{N} $$

and strictly decreasing if $a_n > a_{n+1}$ for all $n$. A sequence is called monotone if it is either monotonically increasing or monotonically decreasing.

A constant sequence, in which every term equals the same value, satisfies both
$a_n \leq a_{n+1}$ and $a_n \geq a_{n+1}$ for all $n$, and is therefore
both increasing and decreasing under the non-strict definition. It is, however, neither
strictly increasing nor strictly decreasing, since the condition $a_n = a_{n+1}$
holds throughout.

## The monotone convergence theorem

The importance of monotone sequences lies in the following result, which gives a complete characterization of their convergence. A monotone sequence of [real numbers](../properties-of-real-numbers/) converges if and only if it is bounded. Moreover, if $\{a_n\}$ is monotonically increasing and bounded above, then its [limit](../limits/) equals the supremum of its range.

$$
\lim_{n \to \infty} a_n = \sup\\{a_n : n \in \mathbb{N}\\}
$$

Analogously, if $\{a_n\}$ is monotonically decreasing and bounded below, then its
limit equals the infimum of its range.

$$
\lim_{n \to \infty} a_n = \inf\\{a_n : n \in \mathbb{N}\\}
$$

The proof of the increasing case runs as follows. Let $L = \sup\{a_n : n \in \mathbb{N}\}$, which exists as a finite real number because the sequence is bounded above. Let $\varepsilon > 0$. 

Since $L$ is the least upper bound, the value $L - \varepsilon$ is not an upper bound for the sequence, and there exists therefore an index $N$ such that $a_N > L - \varepsilon$. 

Because the sequence is increasing, every subsequent term satisfies $a_n \geq a_N > L - \varepsilon$ for all $n \geq N$. Since $L$ is an upper bound, we also have $a_n \leq L < L + \varepsilon$ for all $n$. 

Combining these two inequalities gives $|a_n - L| < \varepsilon  \forall  n \geq N$, which is exactly the definition of convergence to $L$.

> The theorem connects convergence directly to the [supremum and infimum](../supremum-and-infimum/) of the sequence, showing that monotone sequences always converge to a boundary value of their range when they are bounded, and diverge to infinity when they are not.

## Example

Consider the sequence defined by the following expression:

$$
a_n = 1 - \frac{1}{n}
$$

Each term satisfies $a_n < a_{n+1}$, since subtracting a smaller quantity from $1$
yields a larger result as $n$ increases. The sequence is therefore strictly increasing. It is also bounded above by $1$, since $a_n < 1$ for every finite $n$. By the monotone convergence theorem, the sequence converges, and its limit equals the supremum of its range.

$$
\lim_{n \to \infty} \left(1 - \frac{1}{n}\right) = 1
$$

- - -
As a second example, consider the sequence defined recursively as follows:

$$
a_1 = 2, \qquad a_{n+1} = \frac{a_n}{2} + \frac{1}{a_n}
$$

To show that the sequence is decreasing, we examine the sign of $a_{n+1} - a_n$.

$$
a_{n+1} - a_n = \frac{a_n}{2} + \frac{1}{a_n} - a_n = \frac{1}{a_n} - \frac{a_n}{2} = \frac{2 - a_n^2}{2a_n}
$$

This expression is negative whenever $a_n > \sqrt{2}$, which we now show holds for all $n \geq 1$. By the AM-GM inequality applied to $\frac{a_n}{2}$ and $\frac{1}{a_n}$, we have the following:

$$
a_{n+1} = \frac{a_n}{2} + \frac{1}{a_n} \geq 2\sqrt{\frac{a_n}{2} \cdot \frac{1}{a_n}} = 2 \cdot \frac{1}{\sqrt{2}} = \sqrt{2}
$$

Since $a_1 = 2 > \sqrt{2}$, and each term satisfies $a_{n+1} \geq \sqrt{2}$, the
sequence is bounded below by $\sqrt{2}$ and strictly decreasing. The monotone convergence theorem therefore guarantees that it converges to some limit $L \geq \sqrt{2}$.

To identify $L$, we pass to the limit in the recursive relation. Since $a_{n+1} \to L$ and $a_n \to L$, we obtain the equation:

$$L = \frac{L}{2} + \frac{1}{L}$$

which simplifies to $L^2 = 2$. Given that $L \geq \sqrt{2} > 0$, we conclude that $L = \sqrt{2}$. This example illustrates how the monotone convergence theorem can be used to establish convergence and locate the limit of a recursively defined sequence, even when no closed-form expression for the general term is available.

## Unbounded monotone sequences

If a monotone sequence is not bounded, the monotone convergence theorem implies that it
cannot converge to any finite limit. This is not merely a failure of the theorem: it is
a precise statement about the behavior of the sequence. An increasing sequence that is
unbounded above has terms that eventually exceed any fixed real number, no matter how
large, and the sequence therefore diverges to $+\infty$. Symmetrically, a decreasing
sequence that is unbounded below diverges to $-\infty$.

The sequence $a_n = n$ is the simplest example of the former case. It is strictly
increasing and has no upper bound, so it diverges to $+\infty$. A less immediate
example is the sequence of partial sums of the harmonic series, defined by the following
expression:

$$
s_n = \sum_{k=1}^{n} \frac{1}{k} = 1 + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n}
$$

This sequence is strictly increasing, since each new term adds a positive quantity. Whether it is bounded above is a non-trivial question, and the answer is negative: the harmonic series diverges, so $s_n \to +\infty$. 

The divergence is slow enough that the  unboundedness is not immediately apparent from numerical inspection (for instance, $s_{100} \approx 5.187$ and $s_{10000} \approx 9.787$) yet the sequence grows without bound. 

> This example shows that an increasing sequence can be unbounded even when its terms grow very slowly, and that the monotone convergence theorem provides no shortcut: boundedness must be verified, not assumed.

## Eventual monotonicity

In practice, the condition of monotonicity need not hold from the very first term of a sequence. A sequence is called eventually increasing if there exists an index $N$ such that $a_n \leq a_{n+1}$ for all $n \geq N$, and eventually decreasing if $a_n \geq a_{n+1}$ for all $n \geq N$. The initial segment of the sequence, consisting of the finitely many terms before index $N$, is irrelevant to the question of convergence.

This is a consequence of a general principle in the theory of sequences: convergence is a property of the tail of a sequence, meaning it depends only on what happens for sufficiently large indices. Modifying or removing any finite number of terms at the beginning of a sequence leaves its convergence and its limit entirely unchanged. The monotone convergence theorem therefore applies without modification to eventually monotone sequences: 

+ If a sequence is eventually increasing and bounded above, it converges.
+ If it is eventually decreasing and bounded below, it converges as well.

As an illustration, consider the sequence whose general term is the following:

$$
a_n = \frac{n^2 - 5n}{n + 1}
$$

The first few terms are negative and the sequence initially decreases, but from a certain index onward the terms become positive and the sequence increases without bound. The sequence is eventually increasing but unbounded above, so it diverges. Boundedness cannot be dropped from the hypothesis of the theorem.
