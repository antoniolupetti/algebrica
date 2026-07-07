---
title: Binomial Coefficient
source: https://algebrica.org/binomial-coefficient/
license: CC BY-NC 4.0
tags:
  - binomial-coefficient
  - binomial-distribution
  - binomial-theorem
  - combinatorics
  - factorial
  - generalized-binomial-coefficient
  - pascals-triangle
  - recursion
  - vandermonde-identity
---

## Introduction

Given two non-negative natural numbers $n$ and $k,$ the binomial coefficient is the number of ways to choose $k$ elements from a set of $n$ elements, disregarding the selection order. It is denoted by $n$ choose $k,$ and its formula is:

$$
\binom{n}{k} = \begin{cases} \displaystyle\frac{n!}{k! \ (n-k)!} & \text{if } 0 \leq k \leq n \\[6pt] 0 & \text{if } k > n \end{cases}
$$

The components of the expression are the following:

+ $n$ is the number of elements in the set.
+ $k$ is the number of elements to be selected.
+ $n!$ and $(n-k)!$ are two [factorials](../factorial/).

For example, to determine the value of the binomial coefficient $\binom{4}{2},$ we count the number of pairs that can be formed from a set of four elements. Starting from a generic set $P = \\{p, q, r, s\\},$ the number of subsets of two elements is six:

$$
(p,q) \quad (p,r) \quad (p,s) \quad (q,r) \quad (q,s) \quad (r,s)
$$

Unlike permutations, where order matters, the pairs $(p,q)$ and $(q,p)$ describe the same selection and are counted once. The expression $\frac{n!}{(n-k)!}$ counts the ordered selections of $k$ elements from a set of $n.$ Since order does not matter, each unordered subset is counted $k!$ times, once per arrangement of its elements. Dividing by $k!$ removes the double counting and yields:

$$
\binom{n}{k} = \frac{n!}{(n-k)!} \cdot \frac{1}{k!} = \frac{n!}{k! \ (n-k)!}
$$

> The binomial coefficient appears in the [binomial theorem](../binomial-theorem/), where it gives the coefficients of each term in the expansion of $(a+b)^n.$

## Pascal's triangle

Pascal's triangle is a triangular arrangement of the binomial coefficients that appear in the expansion of $(a+b)$ raised to a non-negative integer power $n.$ The first row contains only $1,$ and each number in the subsequent rows is the sum of the two numbers directly above it. The outermost elements of every row are always $1.$ The first six rows are:

$$
\begin{array}{c}
1 \\[6pt]
1 \quad 1 \\[6pt]
1 \quad 2 \quad 1 \\[6pt]
1 \quad 3 \quad 3 \quad 1 \\[6pt]
1 \quad 4 \quad 6 \quad 4 \quad 1 \\[6pt]
1 \quad 5 \quad 10 \quad 10 \quad 5 \quad 1
\end{array}
$$

- - -

Each element in row $n$ and column $k$ corresponds to the binomial coefficient $\binom{n}{k}.$ For example, the number at $n = 4,$ $k = 2$ is:

$$
\binom{4}{2} = \frac{4!}{2!(4 - 2)!} = \frac{4!}{2! \ 2!} = \frac{24}{4} = 6
$$

In the fourth row, the third number is indeed $6.$

- - -

Pascal's triangle satisfies the recurrence relation that follows directly from its construction:

$$
\binom{n}{k} = \binom{n - 1}{k - 1} + \binom{n - 1}{k}
$$


## Fundamental properties of the binomial coefficient

The edge property concerns the coefficients at the two ends of each row, which are always equal to one:

$$
\binom{n}{0} = \binom{n}{n} = 1
$$

For any natural number $n,$ there is exactly one possible way to choose none of the available elements, and likewise only one way to choose all of them.

- - -

The symmetry property concerns the selection of a subset of $k$ elements from a set of $n$ elements. The number of ways to do this is always equal to the number of ways to select the remaining $n-k$ elements, as expressed by the following equivalence:

$$
\binom{n}{k} = \binom{n}{n-k}
$$

Choosing which $k$ elements to include is the same as leaving out the other $n-k,$ so the two counts match.

- - -

The additive property relates consecutive binomial coefficients. For $\binom{n}{k}$ and $\binom{n}{k+1}$ we have:

$$
\binom{n}{k} + \binom{n}{k+1} = \binom{n+1}{k+1}
$$

The property gives a quick way to compute the next binomial coefficient from the previous ones. It follows from the definition and the recurrence, which express each coefficient in terms of the preceding ones.

- - -

The [recursive property](#recursion) describes how each binomial coefficient can be derived from those in the previous row of Pascal's triangle. Every coefficient is obtained as the sum of the two elements positioned directly above it:

$$
\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}
$$

This rule provides a recursive definition for the binomial coefficient and explains the additive structure underlying Pascal's triangle.

## Notable identities of the binomial coefficient

Beyond the core properties, the binomial coefficient satisfies several further identities that recur across combinatorics, probability, and analysis.

The row sum identity states that the sum of all binomial coefficients in row $n$ of Pascal's triangle equals $2^n:$

$$
\sum_{k=0}^{n} \binom{n}{k} = 2^n
$$

To see why the identity is true, consider a set of $n$ elements. Each element can either be included in a subset or not, giving two independent choices per element. The total number of subsets is therefore $2^n,$ and since $\binom{n}{k}$ counts the subsets of exactly $k$ elements, summing over all possible values of $k$ from $0$ to $n$ recovers the same count.

- - -

The alternating sum identity is a close relative of the row sum, but with alternating signs:

$$
\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0
$$

This identity follows directly from evaluating the binomial theorem at $a = 1$ and $b = -1.$ The result reflects a symmetry between subsets of even and odd size. For any $n \geq 1,$ there are exactly as many even-sized subsets of an $n$-element set as there are odd-sized ones.

- - -

The Vandermonde identity describes what happens when two independent selections are combined into a single one. Given two disjoint groups of $m$ and $n$ elements respectively, the number of ways to choose $r$ elements from the combined group equals:

$$
\binom{m+n}{r} = \sum_{k=0}^{r} \binom{m}{k} \binom{n}{r-k}
$$

The reasoning is direct. Any selection of $r$ elements from the combined group must draw exactly $k$ elements from the first group and $r - k$ from the second, for some $k$ between $0$ and $r.$ Each such split contributes $\binom{m}{k} \cdot \binom{n}{r-k}$ combinations, and summing over all valid values of $k$ gives the total. A useful special case arises when $m = n$ and $r = n:$

$$
\binom{2n}{n} = \sum_{k=0}^{n} \binom{n}{k}^2
$$

The central binomial coefficient, the middle entry of row $2n$ in Pascal's triangle, counts the number of ways to select $n$ elements from a group of $2n,$ which can always be decomposed as choosing $k$ from one half and $n - k$ from the other.

- - -

The upper summation identity relates a binomial coefficient to a sum of coefficients from earlier rows:

$$
\sum_{i=0}^{r} \binom{n+i}{i} = \binom{n+r+1}{r}
$$

The name comes from the shape this identity traces in Pascal's triangle: a diagonal run of entries whose sum equals a single entry one step to the right and one step down. The identity is useful when computing cumulative counts that build row by row.

## Generalized binomial coefficient

The definition introduced at the start of this page requires $n$ and $k$ to be natural numbers. The constraint, however, is not as rigid as it appears. The factorial in the numerator can be replaced by a product that makes sense for any real number $\alpha,$ leading to the generalized binomial coefficient:

$$
\binom{\alpha}{k} = \frac{\alpha(\alpha - 1)(\alpha - 2) \cdots (\alpha - k + 1)}{k!}
$$

Here $\alpha \in \mathbb{R}$ and $k$ remains a non-negative integer. When $\alpha$ is a natural number and $k \leq \alpha,$ the expression reduces to the standard binomial coefficient. When $\alpha$ is not a natural number, or when $k > \alpha,$ it produces values that are no longer integers but remain well-defined. This generalization extends the [binomial theorem](../binomial-theorem/) beyond integer exponents. For $|x| < 1,$ Newton showed that:

$$
(1 + x)^{\alpha} = \sum_{k=0}^{\infty} \binom{\alpha}{k} x^k
$$

Unlike the standard binomial theorem, this sum does not terminate and is an infinite series. Two special cases follow. Taking $\alpha = -1$ recovers the geometric series:

$$
\frac{1}{1+x} = \sum_{k=0}^{\infty} (-1)^k x^k
$$

Taking $\alpha = \tfrac{1}{2}$ produces the expansion of $\sqrt{1+x}:$

$$
\sqrt{1+x} = 1 + \frac{1}{2}x - \frac{1}{8}x^2 + \frac{1}{16}x^3 - \cdots
$$

This expansion is used routinely in physics and engineering when $x$ is small. In both cases, the coefficients are computed directly from the generalized binomial coefficient, the same formula with $\alpha$ no longer restricted to a whole number.

## Example 1

A research team has $7$ scientists and $8$ engineers. We want to count how many ways we can form a working group of $3$ scientists and $4$ engineers. To form the group, we must independently select $3$ scientists from $7$ and $4$ engineers from $8.$ Since the two selections are independent, the total number of possible combinations is given by:

$$
N = \binom{7}{3} \times \binom{8}{4}
$$

We compute each factor:

$$
\binom{7}{3} = \frac{7 \times 6 \times 5}{3 \times 2 \times 1} = 35
$$

$$
\binom{8}{4} = \frac{8 \times 7 \times 6 \times 5}{4 \times 3 \times 2 \times 1} = 70
$$

- - -

Combining the possible selections of scientists and engineers, we obtain:

$$
N = 35 \times 70 = 2450
$$

> Based on the available group of scientists and engineers, we can form $2{,}450$ distinct working teams of $3$ scientists and $4$ engineers.

## Example 2

We now consider the same situation described in Example 1, with an additional condition. If two engineers disagree and cannot be assigned to the same group, how many valid combinations can be formed? The total number of possible groups, without restrictions, is $2{,}450.$

We must now exclude the groups that include both of the two engineers who cannot work together. If both conflicting engineers are included in the same group, we have already chosen $2$ specific engineers, so we only need to select the remaining $2$ engineers from the other $6:$

$$
\binom{6}{2}
$$

At the same time, we still need to select $3$ scientists from the $7$ available:

$$
\binom{7}{3}
$$

The number of invalid groups that contain both conflicting engineers is therefore:

$$
N_{\text{invalid}} = \binom{7}{3} \times \binom{6}{2}
$$

Substituting the values, we have:

$$
\binom{7}{3} = 35 \qquad \binom{6}{2} = 15
$$

$$
N_{\text{invalid}} = 35 \times 15 = 525
$$

Subtracting the invalid cases from the total gives the number of valid combinations:

$$
N_{\text{valid}} = N_{\text{total}} - N_{\text{invalid}} = 2450 - 525 = 1925
$$

When the two conflicting engineers cannot be assigned to the same group, $1{,}925$ valid combinations remain.

## Recursion

The binomial coefficient has a natural recursive structure. To count the ways to choose $k$ elements from $n,$ it is enough to know the answers to two smaller versions of the same problem:

$$
\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}
$$

The reasoning is combinatorial. Fix one element from the set, call it $x.$ Every subset of size $k$ either contains $x$ or it does not. If it does, the remaining $k-1$ elements must be chosen from the other $n-1,$ giving $\binom{n-1}{k-1}.$ If it does not, all $k$ elements come from the remaining $n-1,$ giving $\binom{n-1}{k}.$ The two cases are mutually exclusive and together cover all possibilities. For example:

$$
\binom{3}{2} = \binom{2}{1} + \binom{2}{2} = 2 + 1 = 3
$$

This identity is useful in computing because the recursion is already present in the mathematics rather than imposed from outside. A recursive function follows that structure, reducing each call to two smaller ones until it reaches the base cases:

$$
\binom{n}{0} = \binom{n}{n} = 1
$$

> Recursion recalculates the same values multiple times. The computational cost grows quickly with $n,$ a problem that memoization solves by storing intermediate results as they are computed. The trade-off between simplicity and efficiency is explored in the analysis of [Big O notation](../big-o-notation/).

## Foundation of the binomial distribution

The binomial coefficient appears in the binomial distribution, which describes the probability of obtaining a specific number of successes in a fixed number of independent trials. If each trial has only two possible outcomes, success with probability $p$ and failure with probability $q = 1 - p,$ the probability of observing exactly $x$ successes in $n$ trials is given by:

$$
b(x; n, p) = \binom{n}{x} p^{x} q^{n - x}
$$

The expression combines the binomial coefficient, which counts the number of ways $x$ successes can be arranged across $n$ trials, and the factor $p^x q^{n-x},$ which measures the probability of any one such arrangement. Fixing $n$ and $p,$ and letting $x$ vary from $0$ to $n,$ gives the full distribution, with each outcome weighted by the number of ways it can occur.
