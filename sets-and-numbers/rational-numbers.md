---
title: Rational Numbers
source: https://algebrica.org/rational-numbers/
license: CC BY-NC 4.0
tags:
  - cardinality
  - countability
  - decimal-expansion
  - density
  - equivalence-class
  - field
  - lowest-terms
  - ordered-field
  - periodic-expansion
  - rational-numbers
---

## Definition

The [set](../sets/) of rational numbers is denoted by $\mathbb{Q}$. Its elements are the ratios of two [integers](../integers/) with a nonzero denominator:

$$
\mathbb{Q} := \left\{\ \frac{p}{q} \mid p,q \in \mathbb{Z},\ q \neq 0\ \right\}
$$

In the fraction $p/q$ the integer $p$ is the numerator and the integer $q$ is the denominator. The condition $q \neq 0$ is necessary because division by zero is undefined in $\mathbb{Z}$ and $\mathbb{Q}$.

Every integer is a rational number, since any $n \in \mathbb{Z}$ can be written as $n/1$. Thus $\mathbb{Z} \subset \mathbb{Q}$. Together with $\mathbb{N} \subset \mathbb{Z}$, this gives the chain of inclusions described in [types of numbers](../types-of-numbers/):

$$
\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q}
$$

The integers are not closed under division by nonzero integers, since $1/2$ is not an integer. Every nonzero rational number has a multiplicative inverse in $\mathbb{Q}$, so the quotient of two rational numbers is rational whenever the divisor is nonzero.

## Construction as equivalence classes

In a rigorous construction of $\mathbb{Q}$, each rational number is an equivalence class of ordered pairs of integers. This construction is analogous to the construction of $\mathbb{Z}$ from ordered pairs of [natural numbers](../natural-numbers/). Consider the set:

$$
P = \{\ (p, q) \in \mathbb{Z} \times \mathbb{Z} \mid q \neq 0\ \}
$$

Two pairs $(p, q)$ and $(r, s)$ in $P$ are equivalent when their cross-products are equal. This condition does not use division:

$$
(p, q) \sim (r, s) \quad \longleftrightarrow \quad ps = qr
$$

The relation $\sim$ is reflexive, symmetric, and transitive. It is therefore an equivalence relation on $P$, and the set of rational numbers is the quotient set:

$$
\mathbb{Q} := P / {\sim}
$$

The fraction $p/q$ is the equivalence class of the pair $(p, q)$. For example, the pairs $(2, 3)$, $(4, 6)$, and $(-6, -9)$ are in the same class and represent the rational number $2/3$. The cross-products confirm both equivalences:

$$
2 \cdot 6 = 12 = 3 \cdot 4, \qquad 2 \cdot (-9) = -18 = 3 \cdot (-6)
$$

Fractions with different numerators and denominators may denote the same rational number. A rational number is the equivalence class, not one particular representative of that class.

## Lowest terms

Each rational number has a unique representative in reduced form, also called lowest terms. A fraction $p/q$ is in lowest terms when $\gcd(p, q) = 1$ and $q > 0$. These conditions identify one pair $(p, q)$ in each equivalence class.

To reduce a fraction, we divide its numerator and denominator by their greatest common divisor. For $18/24$ the greatest common divisor is $6$, so:

$$
\frac{18}{24} = \frac{18 / 6}{24 / 6} = \frac{3}{4}
$$

The pair $(3, 4)$ satisfies $\gcd(3, 4) = 1$ and is the lowest-terms representative of the class. For a negative rational number, the numerator has the negative sign and the denominator remains positive. Thus the reduced form of $-15/35$ is $-3/7$.

> Suppose that $p/q$ and $r/s$ are in lowest terms and represent the same rational number. The equality $ps = qr$, the coprimality of both pairs, and the conditions $q, s > 0$ imply $p = r$ and $q = s$. Hence two reduced fractions represent the same rational number if and only if they are identical.

## Arithmetic operations

Addition and multiplication on $\mathbb{Q}$ are defined on representatives. For $p/q$ and $r/s$ in $\mathbb{Q}$, the definitions are:

$$
\frac{p}{q} + \frac{r}{s} = \frac{ps + qr}{qs}
$$

$$
\frac{p}{q} \cdot \frac{r}{s} = \frac{pr}{qs}
$$

The denominator $qs$ is nonzero whenever $q$ and $s$ are nonzero. Cross-multiplication shows that equivalent representatives give equivalent sums and products, so both operations are well-defined on equivalence classes. Subtraction uses the additive inverse $-p/q = (-p)/q$, while division by a nonzero rational $r/s$ is multiplication by its reciprocal $s/r$:

$$
\frac{p}{q} - \frac{r}{s} = \frac{ps - qr}{qs}
$$

$$
\frac{p}{q} \div \frac{r}{s} = \frac{p}{q} \cdot \frac{s}{r} = \frac{ps}{qr}, \qquad r \neq 0
$$

The rational numbers are closed under addition, subtraction, and multiplication. They are also closed under division when the divisor is nonzero. For example:

$$
\frac{2}{3} + \frac{1}{4} = \frac{2 \cdot 4 + 3 \cdot 1}{3 \cdot 4} = \frac{11}{12}
$$

$$
\frac{2}{3} \cdot \frac{1}{4} = \frac{2}{12} = \frac{1}{6}
$$

Since $\gcd(2, 12) = 2$, the second result reduces to $1/6$.

## Field structure

With these operations, $\mathbb{Q}$ is a [field](../fields/). It is the field of fractions of $\mathbb{Z}$ and, up to the usual [embedding](../homomorphisms-and-isomorphisms/) $n \mapsto n/1$, the smallest field containing the integers. For all $a, b, c \in \mathbb{Q}$, the field axioms are:

+ Addition is associative and commutative, with $0 = 0/1$ as additive identity.
+ Every rational $a$ has an additive inverse $-a$, so that $a + (-a) = 0$.
+ Multiplication is associative and commutative, with $1 = 1/1$ as multiplicative identity.
+ Every nonzero rational $a$ has a multiplicative inverse $a^{-1}$, so that $a \cdot a^{-1} = 1$.
+ Multiplication distributes over addition: $a(b + c) = ab + ac$.

The difference from $\mathbb{Z}$ is that every nonzero element of $\mathbb{Q}$ has a multiplicative inverse. The only integers whose inverses are integers are $1$ and $-1$.

$\mathbb{Q}$ also has a total order inherited from $\mathbb{Z}$. A rational number $p/q$ with $q > 0$ is positive when $p > 0$ and negative when $p < 0$. If $q, s > 0$, then $p/q < r/s$ if and only if $ps < rq$. This order is compatible with addition and multiplication by positive elements, so $\mathbb{Q}$ is an [ordered field](../properties-of-real-numbers/).

## Decimal representation

Every rational number has a decimal expansion that terminates or is eventually periodic. The expansion is the result of long division, and its form depends on the prime factorisation of the denominator in lowest terms.

Write the positive denominator as $q = 2^a5^bm$, where $a, b \geq 0$ and $\gcd(m, 10) = 1$. The decimal expansion terminates if and only if $m = 1$. If $m > 1$, the periodic part has length equal to the [multiplicative order](../groups/) of $10$ modulo $m$, which divides $\varphi(m)$, where $\varphi$ is [Euler's totient function](../modulo-operator/).

The two cases are:

$$
\frac{1}{4} = 0.25, \qquad \frac{3}{8} = 0.375
$$

$$
\frac{1}{3} = 0.\overline{3}, \qquad \frac{1}{7} = 0.\overline{142857}, \qquad \frac{5}{6} = 0.8\overline{3}
$$

The overline marks the block of digits that repeats indefinitely. For $1/7$ the period has length $6$, which equals $\varphi(7)$. Since $6 = 2 \cdot 3$, the factor $2$ in the denominator of $5/6$ gives the non-repeating prefix and the factor $3$ gives the periodic part. A terminating decimal also has a second representation with a repeating $9$, for example $0.25 = 0.24\overline{9}$.

> A real number is rational if and only if its decimal expansion terminates or is eventually periodic. A non-terminating, non-periodic expansion therefore represents an [irrational number](../irrational-numbers/).

## Converting a periodic decimal to a fraction

Every eventually periodic decimal is rational. To recover its fractional form, we multiply it by a power of $10$ that aligns two copies of the repeating block, then subtract the original decimal. The repeating tails cancel.

For $x = 0.\overline{27}$, the repeating block has two digits. Multiplication by $100$ moves the decimal point through one complete period:

$$
100 x = 27.\overline{27}
$$

Subtracting the original equation $x = 0.\overline{27}$ removes the periodic tail and leaves a linear equation:

$$
100 x - x = 27 \quad\Longrightarrow\quad 99 x = 27 \quad\Longrightarrow\quad x = \frac{27}{99} = \frac{3}{11}
$$

Since $\gcd(27, 99) = 9$, the fraction in the last step reduces to $3/11$. For an expansion with a non-repeating prefix, we first multiply by a power of $10$ that moves the decimal point past the prefix, then apply the same cancellation to the periodic part.

## Density in the real line

The rational numbers are dense in $\mathbb{R}$. Thus, for every $x, y \in \mathbb{R}$ with $x < y$, a rational number $q$ satisfies $x < q < y$. The proof uses the Archimedean property of $\mathbb{R}$, discussed in [real numbers](../real-numbers/).

Given $x < y$, the Archimedean property guarantees a positive integer $n$ such that $n(y - x) > 1$. The [open interval](../intervals/) $(nx, ny)$ then has length greater than $1$, so some integer $m$ satisfies $nx < m < ny$. Since $n > 0$, division by $n$ gives:

$$
x < \frac{m}{n} < y
$$

The rational number $m/n$ lies strictly between $x$ and $y$. Applying the same argument recursively to $(x, m/n)$ gives infinitely many distinct rational numbers in $(x, y)$. In particular, between any two distinct rational numbers there are infinitely many other rational numbers.

Equivalently, in terms of [absolute value](../absolute-value/), for every $x \in \mathbb{R}$ and every $\varepsilon > 0$, some $q \in \mathbb{Q}$ satisfies $|x - q| < \varepsilon$. This approximation property does not imply that $\mathbb{Q}$ is complete. For example, a [Cauchy sequence](../cauchy-sequence/) of rational numbers can converge in $\mathbb{R}$ to $\sqrt{2}$, although $\sqrt{2} \notin \mathbb{Q}$.

## Cardinality

The rational numbers are countably infinite, that is, $\mathbb{Q}$ and $\mathbb{N}$ are in [bijection](../functions/). An explicit enumeration proves this statement. The general criteria for countability and a second proof based on a surjection from $\mathbb{Z}\times(\mathbb{N}\setminus\{0\})$ are given in [cardinality and countable sets](../cardinality-and-countable-sets/).

The following infinite table has the fraction $p/q$ in row $p$ and column $q$:

$$
\begin{array}{cccccc}
1/1 & 1/2 & 1/3 & 1/4 & 1/5 & \cdots \\[6pt]
2/1 & 2/2 & 2/3 & 2/4 & 2/5 & \cdots \\[6pt]
3/1 & 3/2 & 3/3 & 3/4 & 3/5 & \cdots \\[6pt]
4/1 & 4/2 & 4/3 & 4/4 & 4/5 & \cdots \\[6pt]
\vdots & \vdots & \vdots & \vdots & \vdots & \ddots
\end{array}
$$

If we traverse the table along diagonals and retain $p/q$ exactly when $\gcd(p, q) = 1$, every positive rational occurs once. Interleaving each positive rational with its negative and placing $0$ at the beginning gives an enumeration of $\mathbb{Q}$.

Thus $|\mathbb{Q}| = |\mathbb{N}|$, whereas $\mathbb{R}$ is uncountable. Density and cardinality answer different questions. Every nonempty real interval contains rational numbers, but no enumeration of $\mathbb{Q}$ can exhaust $\mathbb{R}$. In fact, the set of [irrational numbers](../irrational-numbers/) is uncountable.

## Position within the real line

On the real line, the rational points are exactly those whose coordinates have the form $p/q$, where $p, q \in \mathbb{Z}$ and $q \neq 0$. Every nonempty interval contains infinitely many such points. All other points have irrational coordinates.

Both $\mathbb{Q}$ and $\mathbb{R}$ are ordered fields, but $\mathbb{Q}$ does not satisfy the [completeness axiom](../supremum-and-infimum/). Consider the set:

$$
S = \{\ q \in \mathbb{Q} \mid q^2 < 2\ \}
$$

The set $S$ is non-empty because $1 \in S$, and it is bounded above by $2$. Suppose that $u \in \mathbb{Q}$ were its least upper bound. Then $1 \leq u \leq 2$. For this $u$, the following number is rational:

$$
v = \frac{2(u + 1)}{u + 2}
$$

We have:

$$
v - u = \frac{2 - u^2}{u + 2}, \qquad v^2 - 2 = \frac{2(u^2 - 2)}{(u + 2)^2}
$$

If $u^2 < 2$, then $v > u$ and $v \in S$, contrary to the fact that $u$ is an upper bound. If $u^2 > 2$, then $0 < v < u$ and $v^2 > 2$. Every negative element of $S$ is less than $v$, and every nonnegative $q \in S$ satisfies $q^2 < 2 < v^2$, hence $q < v$. Thus $v$ is an upper bound smaller than $u$, contrary to the leastness of $u$. The remaining equality $u^2 = 2$ would imply $u = \sqrt{2}$, which is [irrational](../irrational-numbers/). Hence $S$ has no least upper bound in $\mathbb{Q}$, while its least upper bound in $\mathbb{R}$ is $\sqrt{2}$.
