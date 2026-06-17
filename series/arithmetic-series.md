---
title: Arithmetic Series
source: https://algebrica.org/arithmetic-series/
license: CC BY-NC 4.0
tags:
  - arithmetic-series
  - common-difference
  - gauss-trick
  - partial-sums
  - series
---
## Definition

An arithmetic series is the sum of the terms of an [arithmetic sequence](../arithmetic-sequence/), a [sequence](../sequences/) in which every term differs from the one before it by a fixed amount. This amount is the common difference $d$. Starting from a first term $a$, the terms are:

$$
a, \quad a + d, \quad a + 2d, \quad a + 3d, \quad \dots
$$

The term of index $k$ is $a + (k-1)d$, and the [series](../series/) obtained by adding the first $n$ terms is:

$$
S_n = \sum_{k=1}^{n} \left[ a + (k-1)d \right] = a + (a+d) + (a+2d) + \dots + \left[ a + (n-1)d \right]
$$

For example, the sequence $1, 3, 5, 7, 9, \dots$ is arithmetic with first term $a = 1$ and common difference $d = 2$, so the sum of its first $n$ terms is an arithmetic series.

The constant difference gives a local description of the sequence. A sequence is arithmetic exactly when each interior term equals the arithmetic mean of its two neighbors:

$$
a_k = \frac{a_{k-1} + a_{k+1}}{2}
$$

The two neighbors sit at equal distance $d$ below and above $a_k$, so their average returns $a_k$. The condition is equivalent to a constant difference, because it forces $a_{k+1} - a_k = a_k - a_{k-1}$ at every interior index. This mean property is the source of the name.

## Sum of a finite arithmetic series

The partial sum with first term $a$ and common difference $d$ has a closed form:

$$
S_n = \frac{1}{2}n \left[ 2a + (n-1)d \right]
$$

The result follows from a symmetry of the sum, a device usually credited to Gauss. We write the sum once in its natural order and once in reverse, then add the two expressions term by term:

$$
\begin{align}
S_n &= a + (a+d) + \dots + \left[ a + (n-1)d \right] \\[6pt]
S_n &= \left[ a + (n-1)d \right] + \left[ a + (n-2)d \right] + \dots + a \\[6pt]
2S_n &= \left[ 2a + (n-1)d \right] + \left[ 2a + (n-1)d \right] + \dots + \left[ 2a + (n-1)d \right]
\end{align}
$$

Each column of the last line sums to the same value $2a + (n-1)d$, because the increase of one term across a column is matched by the decrease of the other. Since the line contains $n$ such columns, we obtain:

$$
2S_n = n \left[ 2a + (n-1)d \right]
$$

Dividing by $2$ gives the closed form for $S_n$.

> The argument works because the first and last terms add to the same total as the second and second-to-last, and so on inward. Pairing the terms from the outside replaces $n$ different summands with $n$ copies of a single value.

---

When the last term is known, the formula takes a more compact shape. Writing $z = a + (n-1)d$ for the final term, the bracket $2a + (n-1)d$ equals $a + z$, so:

$$
S_n = \frac{n(a+z)}{2}
$$

This form reads as the number of terms times the average of the first and last term. The two expressions are interchangeable, and the choice between them depends on whether the common difference or the final term is the known quantity.

The most familiar instance is the sum of the first $n$ positive integers, obtained by setting $a = 1$ and $d = 1$, so that the final term is $z = n$. The compact form gives:

$$
1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2}
$$

These totals are the triangular numbers, the running sums of the [natural numbers](../natural-numbers/), and they appear as soon as a quantity accumulates in equal unit steps.

## Behavior of the infinite series

Unlike a [geometric series](../geometric-series/), whose terms can shrink fast enough to give a finite sum, an arithmetic series with $d \neq 0$ never converges. The general term $a + (k-1)d$ grows without bound in absolute value as $k$ increases, so it does not tend to zero, and a series whose terms fail to vanish cannot converge. The partial sums themselves confirm this, since $S_n$ is a quadratic expression in $n$:

$$
S_n = \frac{d}{2}n^2 + \left( a - \frac{d}{2} \right) n
$$

When $d > 0$ the partial sums diverge to $+\infty$, and when $d < 0$ they diverge to $-\infty$. The remaining case $d = 0$ reduces the sequence to the constant $a$, whose partial sums $S_n = na$ still diverge unless $a = 0$.

## Example with a known number of terms

A display of cans is stacked so that the top row holds one can and each lower row holds two cans more than the row above. We find how many rows are needed for the display to contain $100$ cans.

The number of cans in the rows forms an arithmetic sequence with first term $a = 1$ and common difference $d = 2$. The total contained in $n$ rows is the corresponding arithmetic series:

$$
S_n = \frac{1}{2}n \left[ 2 \cdot 1 + (n-1) \cdot 2 \right] = \frac{1}{2}n \left[ 2n \right] = n^2
$$

Setting this total equal to $100$ gives $n^2 = 100$, and since the number of rows is positive we take $n = 10$. The display therefore contains ten rows.

## Example with shifted indices

An arithmetic sequence $\{a_n\}$ has prescribed sums on its first hundred and second hundred terms:

$$
a_1 + a_2 + \dots + a_{100} = 100, \qquad a_{101} + a_{102} + \dots + a_{200} = 200
$$

We determine the common difference $d = a_2 - a_1$.

Each term of the second block is obtained from the matching term of the first block by advancing one hundred places, so $a_{101} = a_1 + 100d$, then $a_{102} = a_2 + 100d$, and in general $a_{100+k} = a_k + 100d$. Summing these hundred identities turns the second condition into a statement about the first block:

$$
\begin{align}
(a_1 + 100d) + (a_2 + 100d) + \dots + (a_{100} + 100d) &= 200 \\[6pt]
(a_1 + a_2 + \dots + a_{100}) + 100 \cdot 100d &= 200 \\[6pt]
100 + 10000d &= 200
\end{align}
$$

Solving the last equation gives $10000d = 100$, so the common difference is $d = \frac{1}{100}$.
