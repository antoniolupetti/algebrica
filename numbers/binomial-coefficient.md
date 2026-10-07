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

The binomial coefficient is used to solve combinatorial counting problems and gives the number of ways to choose $k$ elements from a set of $n$ elements, regardless of the order in which they are chosen. It is given by the following formula involving factorials. As discussed in the article on [factorials](../factorial/), $n!$ counts the permutations of $n$ distinct objects:

$$\tag{1}
\binom{n}{k} = \begin{cases} \displaystyle\frac{n!}{k!(n-k)!} & \text{if } 0 \leq k \leq n \\[6pt] 0 & \text{if } k > n \end{cases}
$$

For example, we want to calculate the following binomial coefficient:

$$\binom{4}{2}$$

We therefore want to determine how many [subsets](../sets/) of $2$ elements can be chosen from a set of $4$ elements, denoted by $P = \{p, q, r, s\}.$ The six possible pairs are:

$$\tag{2}
\{p,q\} \quad \{p,r\} \quad \{p,s\} \quad \{q,r\} \quad \{q,s\} \quad \{r,s\}
$$

Here, the pair $\{p,q\}$ is the same as the pair $\{q,p\},$ so it is counted only once, as is every other pair listed in $(2).$ This differs from permutations, where order matters. Applying formula $(1)$ with $n = 4$ and $k = 2,$ we obtain the same value, consistent with the pairs listed in $(2):$

$$
\binom{4}{2} = \frac{4!}{2!(4-2)!} = \frac{4!}{2!2!} = \frac{24}{2 \cdot 2} = 6
$$

The second case of $(1)$ also merits a comment. It has a fairly intuitive explanation, since, when $k > n,$ it is impossible to choose $k$ distinct elements from a set containing only $n,$ so the number of possible choices is zero. For example, returning to the set $P$ with four elements, we cannot choose $5$ distinct elements because only $4$ are available. We therefore have:

$$\binom{4}{5} = 0$$

- - -

Formula $(1)$ can be generalized by replacing $n$ with any [real number](../real-numbers/) $\alpha,$ while $k$ remains a non-negative integer.

$$\tag{3}
\binom{\alpha}{k} = \frac{\alpha(\alpha - 1)(\alpha - 2) \cdots (\alpha - k + 1)}{k!}
$$

Consider a few typical cases:

+ For $k = 0,$ the product in the numerator is empty and equals $1,$ so $(3)$ also equals $1.$
+ If $\alpha$ is a non-negative integer and $k \leq \alpha,$ the expression reduces to $(1).$
+ If $\alpha$ is a non-negative integer and $k > \alpha,$ the binomial coefficient equals $0.$ In this case, we subtract from $\alpha$ every integer from $0$ to $k-1.$ Since $k > \alpha,$ these integers include $\alpha$ itself. The product in the numerator therefore contains the factor $\alpha-\alpha=0,$ so $(3)$ equals zero.

For other real values of $\alpha,$ the product in the numerator remains defined and the denominator $k!$ is positive, so the formula gives a value that is not necessarily an integer.

- - -

Formula $(3)$ extends the expansion of powers of a [binomial](../binomials/) to any real exponent $\alpha.$ For $|x| < 1,$ Newton's binomial formula holds:

$$\tag{4}
(1 + x)^{\alpha} = \sum_{k=0}^{\infty} \binom{\alpha}{k} x^k
$$

If $\alpha = n$ is a non-negative integer, the series reduces to the finite sum in the [binomial theorem](../binomial-theorem/), whereas for other real values of $\alpha,$ the expansion contains infinitely many terms. We now consider two special cases of $(4).$ In the first, we set $\alpha = -1,$ obtaining a [geometric series](../geometric-series/):

$$
\frac{1}{1+x} = \sum_{k=0}^{\infty} (-1)^k x^k
$$

In the second, we set $\alpha = 1/2,$ obtaining the expansion of $\sqrt{1+x},$ which is used in physics (for example, to estimate the change in the period of a simple pendulum) when $x$ is very small in [absolute value](../absolute-value/):

$$
\sqrt{1+x} = 1 + \frac{1}{2}x - \frac{1}{8}x^2 + \frac{1}{16}x^3 - \cdots
$$

- - -

The binomial coefficient also appears in the [binomial distribution](../binomial-distribution/). For $n$ independent trials, each with two possible outcomes and constant probabilities $p$ of success and $q = 1-p$ of failure, the probability of obtaining exactly $x$ successes is given by:

$$
b(x; n, p) = \binom{n}{x} p^{x} q^{n - x}
$$

The expression combines the binomial coefficient, which counts the ways to arrange $x$ successes among $n$ trials, and the factor $p^x q^{n-x},$ which gives the probability of each such arrangement.

## Pascal's triangle

Pascal's triangle is a graphical arrangement of the binomial coefficients that appear in the expansion of a binomial $(a+b)$ raised to a non-negative integer power. The first row contains only $1,$ and for $n \geq 2$ and $1 \leq k \leq n-1,$ the following relation holds:

$$\tag{5}
\binom{n}{k} = \binom{n - 1}{k - 1} + \binom{n - 1}{k}
$$

In practice, $(5)$ is a recurrence relation stating that each interior entry of the triangle is the sum of the two entries in the preceding row immediately above it. For example, constructing the first six rows gives:

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

Numbering the rows and columns from $0,$ the entry in row $n$ and column $k$ corresponds to the binomial coefficient given by $(1).$ For example, the number at $n = 4,$ $k = 2$ is:

$$
\binom{4}{2} = \frac{4!}{2!(4 - 2)!} = \frac{4!}{2!2!} = \frac{24}{4} = 6
$$

Indeed, in the fifth row, with index $4,$ and the third column, with index $2,$ we find the number $6.$

## Fundamental properties

The following fundamental properties are useful when solving problems involving binomial coefficients. The first states that the entries at both ends of each row are always equal to $1.$ We have:

$$
\binom{n}{0} = \binom{n}{n} = 1
$$

The symmetry property concerns the choice of a subset of $k$ elements from a set of $n$ elements. The number of ways to make this choice equals the number of ways to choose the remaining $n-k$ elements:

$$
\binom{n}{k} = \binom{n}{n-k}
$$

This property is visible in each row of Pascal's triangle, where the numbers at equal distances to the left and right of the central axis are equal.

The next property is the additive property, which relates two consecutive binomial coefficients through the following identity:

$$
\binom{n}{k} + \binom{n}{k+1} = \binom{n+1}{k+1}
$$

In practice, this property allows us to calculate a binomial coefficient from two coefficients in the preceding row.

- - -

We now examine another property in more detail, namely the recursive structure of the binomial coefficient. In practice, to count the ways to choose $k$ elements from a set of $n,$ we need the answers to two smaller versions of the problem, choosing $k-1$ and $k$ elements, respectively, from a set of $n-1$ elements, as expressed by the following formula:

$$\tag{6}
\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}
$$

For example, we calculate the following binomial coefficient by rewriting it using $(6):$

$$
\binom{3}{2} = \binom{2}{1} + \binom{2}{2} = 2 + 1 = 3
$$

## Notable identities

We now list several fundamental identities for binomial coefficients that are useful in solving problems. The first states that the sum of all the binomial coefficients in row $n$ of Pascal's triangle equals $2^n:$

$$\tag{7}
\sum_{k=0}^{n} \binom{n}{k} = 2^n
$$

For example, consider the sum of the binomial coefficients in the fifth row of Pascal's triangle, with index $4.$ A set of $4$ elements has one empty subset, four subsets of one element, six of two elements, four of three elements, and one of four elements. Applying $(7),$ we therefore obtain $16:$

$$
\binom{4}{0} + \binom{4}{1} + \binom{4}{2} + \binom{4}{3} + \binom{4}{4} = 1 + 4 + 6 + 4 + 1 = 16 = 2^4
$$

- - -

The next identity concerns the alternating sum. It is analogous to $(7),$ but with alternating signs. For $n \geq 1,$ the following relation holds:

$$
\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0
$$

This identity follows from the binomial theorem by setting $a = 1$ and $b = -1,$ and the result expresses a symmetry between subsets of even [cardinality](../cardinality-and-countable-sets/) and those of odd cardinality.

- - -

The following identity describes a property of diagonal sums in Pascal's triangle. Suppose we start from an entry equal to $1$ at the far left of a row $n$ and sum all the entries along the diagonal down to row $n+r.$ This sum equals the number immediately below and to the left of the last entry included. The identity can be written as:

$$
\sum_{i=0}^{r} \binom{n+i}{i} = \binom{n+r+1}{r}
$$

To illustrate the formula, take $n = 1$ and $r = 2.$ We therefore start at row $1$ and sum the entries encountered along the diagonal down to row $3,$ obtaining:

$$
\binom{1}{0} + \binom{2}{1} + \binom{3}{2} = 1 + 2 + 3 = 6
$$

Indeed, the value $6$ lies immediately below and to the left of the last entry, $3.$

$$
\begin{array}{c}
1 \\[6pt]
1 \quad 1 \\[6pt]
1 \quad 2 \quad 1 \\[6pt]
1 \quad 3 \quad 3 \quad 1 \\[6pt]
1 \quad 4 \quad \enclose{circle}{6} \quad 4 \quad 1 \\[6pt]
1 \quad 5 \quad 10 \quad 10 \quad 5 \quad 1
\end{array}
$$

- - -

Finally, Vandermonde's identity counts the ways to choose $r$ elements from the union of two disjoint sets containing $m$ and $n$ elements:

$$\tag{8}
\binom{m+n}{r} = \sum_{k=0}^{r} \binom{m}{k} \binom{n}{r-k}
$$

For a concrete example, we return to the opening example and count the subsets of two elements of $P = \{p,q,r,s\}$ again, this time using $(8).$ We first divide $P$ into two disjoint subsets $A = \{p,q\}$ and $B = \{r,s\},$ and set $m = n = 2$ and $r = 2$ in the formula. The index $k$ tells us how many of the two selected elements belong to $A,$ while $2-k$ tells us how many belong to $B.$ We have three cases:

+ If $k = 0,$ we choose both elements from $B,$ so the only pair is $\{r,s\}.$
+ If $k = 1,$ we choose one element from $A$ and one from $B,$ giving four pairs in total, namely $\{p,r\},$ $\{p,s\},$ $\{q,r\},$ and $\{q,s\}.$
+ If $k = 2,$ we have the last possible case, in which both elements belong to $A$ and the only pair is $\{p,q\}.$

The calculation can be written as follows:

$$
\begin{align}
\binom{4}{2} &= \binom{2}{0}\binom{2}{2} + \binom{2}{1}\binom{2}{1} + \binom{2}{2}\binom{2}{0} \\[6pt]
&= 1 \cdot 1 + 2 \cdot 2 + 1 \cdot 1 = 6
\end{align}
$$

We have therefore found the same pairs listed in $(2),$ giving $6$ pairs in total.

## Examples

We now consider two examples that apply the binomial coefficient to practical problems. In the first, a group consists of $7$ scientists and $8$ engineers, and we want to count how many groups of $3$ scientists and $4$ engineers can be formed. To form a group, we must choose $3$ scientists from the $7$ available and $4$ engineers from the $8$ available, so we use the product of two binomial coefficients:

$$
\binom{7}{3} \times \binom{8}{4}
$$

Evaluating the factors gives:

$$
\binom{7}{3} = \frac{7 \times 6 \times 5}{3 \times 2 \times 1} = 35
$$

$$
\binom{8}{4} = \frac{8 \times 7 \times 6 \times 5}{4 \times 3 \times 2 \times 1} = 70
$$

The number of possible groups is therefore $35 \times 70 = 2{,}450.$

- - -

We now consider the same situation as in the previous example, with an additional condition. If two engineers cannot be assigned to the same group for some reason, how many combinations are possible? We must clearly exclude the groups containing both engineers who cannot work together. We proceed as follows:

+ We include the two engineers who cannot work together.
+ In each group, they occupy 2 of the 4 places for engineers.
+ We therefore need to choose only 2 engineers from the remaining $8-2=6,$ giving the following number of choices:

$$
\binom{6}{2}
$$

Since there are no further restrictions, the number of ways to choose the scientists is the same as in the previous example:

$$
\binom{7}{3}
$$

The number of inadmissible groups, $N_{\text{NA}},$ containing both engineers who cannot work together is therefore:

$$
N_{\text{NA}} = \binom{7}{3} \times \binom{6}{2}
$$

Evaluating the coefficients and substituting their values gives:

$$
\binom{7}{3} = 35 \qquad \binom{6}{2} = 15
$$

$$
N_{\text{NA}} = 35 \times 15 = 525
$$

At this point, the calculation is straightforward. We subtract the inadmissible groups just counted from the total in the previous example:

$$
2{,}450 - 525 = 1{,}925
$$
