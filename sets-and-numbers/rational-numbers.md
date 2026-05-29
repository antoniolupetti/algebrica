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

The [set](../sets/) of rational numbers, denoted by $\mathbb{Q}$, collects all the quantities that can be expressed as a ratio of two [integers](../integers/) with a nonzero denominator. The standard description is given by:

$$
\mathbb{Q} = \left\{ \frac{p}{q} : p,q \in \mathbb{Z},\ q \neq 0 \right\}
$$

In the fraction $p/q$ the integer $p$ is called the numerator and the integer $q$ is called the denominator. The requirement $q \neq 0$ excludes division by zero, which has no meaning within $\mathbb{Z}$ or $\mathbb{Q}$.

Every integer is a rational number, since any $n \in \mathbb{Z}$ can be written as $n/1$. The inclusion $\mathbb{Z} \subset \mathbb{Q}$ is therefore immediate, and the same reasoning extends the chain of inclusions described in [types of numbers](../types-of-numbers/):

$$
\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q}
$$

The passage from $\mathbb{Z}$ to $\mathbb{Q}$ resolves a structural limitation of the integers. Division by a nonzero integer is not in general well-defined within $\mathbb{Z}$, since the quotient $1/2$ does not exist there. Inside $\mathbb{Q}$ every nonzero element admits a multiplicative inverse, and division by any nonzero rational becomes an operation that never leaves the set.

## Construction as equivalence classes

A rigorous construction of $\mathbb{Q}$ presents each rational number as an equivalence class of ordered pairs of integers, in close analogy with the construction of $\mathbb{Z}$ from ordered pairs of [natural numbers](../natural-numbers/). Consider the set:

$$
P = \\{\ (p, q) \in \mathbb{Z} \times \mathbb{Z} : q \neq 0 \ \\}
$$

Two pairs $(p, q)$ and $(r, s)$ in $P$ are declared equivalent when they encode the same ratio. The condition is expressed by cross-multiplication, which avoids any reference to division:

$$
(p, q) \sim (r, s) \quad \longleftrightarrow \quad ps = qr
$$

The relation $\sim$ is reflexive, symmetric, and transitive, so it is an equivalence relation on $P$. The set of rational numbers is then defined as the quotient:

$$
\mathbb{Q} := P / {\sim}
$$

The fraction $p/q$ is interpreted as the equivalence class of the pair $(p, q)$. For example, the pairs $(2, 3)$, $(4, 6)$, and $(-6, -9)$ all belong to the same class, and they represent the same rational number $2/3$. The check is direct:

$$
2 \cdot 6 = 12 = 3 \cdot 4, \qquad 2 \cdot (-9) = -18 = 3 \cdot (-6)
$$

The construction explains why two fractions that look different on the page may denote the same rational number. The identity of a rational depends on the equivalence class, not on the particular representative chosen to describe it.

## Lowest terms

Each rational number admits a distinguished representative, called the reduced form or lowest terms. A fraction $p/q$ is in lowest terms when $\gcd(p, q) = 1$ and $q > 0$. The condition selects a unique pair $(p, q)$ in each equivalence class and provides a canonical way to write a rational number.

The reduction is performed by dividing numerator and denominator by their greatest common divisor. Consider the fraction $18/24$. The greatest common divisor of $18$ and $24$ is $6$, and dividing through gives:

$$
\frac{18}{24} = \frac{18 / 6}{24 / 6} = \frac{3}{4}
$$

The pair $(3, 4)$ satisfies $\gcd(3, 4) = 1$ and is the lowest-terms representative of the class. The same procedure applies to fractions with negative entries, with the convention that the sign is carried by the numerator. The reduced form of $-15/35$ is $-3/7$.

> Two fractions in lowest terms denote the same rational number if and only if they coincide. The canonical representative therefore acts as a label that identifies each element of $\mathbb{Q}$ unambiguously, in contrast with the redundancy of the general fractional notation.

## Arithmetic operations

The operations of addition and multiplication on $\mathbb{Q}$ are defined directly on representatives, and the definitions are independent of the choice of representative within each class. Given $p/q$ and $r/s$ in $\mathbb{Q}$, the operations are:

$$
\frac{p}{q} + \frac{r}{s} = \frac{ps + qr}{qs}
$$

$$
\frac{p}{q} \cdot \frac{r}{s} = \frac{pr}{qs}
$$

The denominator $qs$ is nonzero whenever $q$ and $s$ are nonzero, so both results remain inside $\mathbb{Q}$. Subtraction and division are derived from the two primary operations. Subtraction follows from addition by introducing the additive inverse $-p/q = (-p)/q$, and division by a nonzero rational $r/s$ is the multiplication by the reciprocal $s/r$:

$$
\frac{p}{q} - \frac{r}{s} = \frac{ps - qr}{qs}
$$

$$
\frac{p}{q} \div \frac{r}{s} = \frac{p}{q} \cdot \frac{s}{r} = \frac{ps}{qr}, \qquad r \neq 0
$$

The four operations are closed in $\mathbb{Q}$, with the single exception that division by zero remains undefined. A short example illustrates the rules:

$$
\frac{2}{3} + \frac{1}{4} = \frac{2 \cdot 4 + 3 \cdot 1}{3 \cdot 4} = \frac{11}{12}
$$

$$
\frac{2}{3} \cdot \frac{1}{4} = \frac{2}{12} = \frac{1}{6}
$$

The result of the second computation has been reduced to lowest terms, in agreement with the convention introduced above.

## Field structure

The algebraic properties of the four operations make $\mathbb{Q}$ a [field](../fields/), the smallest field containing $\mathbb{Z}$. The field axioms describe the joint behaviour of addition and multiplication. For all $a, b, c \in \mathbb{Q}$:

+ Addition is associative and commutative, with $0 = 0/1$ as additive identity.
+ Every rational $a$ has an additive inverse $-a$, so that $a + (-a) = 0$.
+ Multiplication is associative and commutative, with $1 = 1/1$ as multiplicative identity.
+ Every nonzero rational $a$ has a multiplicative inverse $a^{-1}$, so that $a \cdot a^{-1} = 1$.
+ Multiplication distributes over addition: $a(b + c) = ab + ac$.

The presence of multiplicative inverses for every nonzero element is the structural feature that separates $\mathbb{Q}$ from $\mathbb{Z}$. Within the integers only $1$ and $-1$ admit inverses, while inside $\mathbb{Q}$ the reciprocal of every nonzero rational exists and remains rational.

$\mathbb{Q}$ also carries a total order, inherited from $\mathbb{Z}$ and compatible with the field operations. A rational number $p/q$ with $q > 0$ is positive when $p > 0$ and negative when $p < 0$, and the comparison between two rationals reduces to an integer comparison after cross-multiplication. The combination of field axioms and an order compatible with the operations makes $\mathbb{Q}$ an [ordered field](../real-numbers/).

## Decimal representation

Every rational number admits a decimal expansion that is either terminating or eventually periodic. The expansion is obtained by performing long division of the numerator by the denominator, and its behaviour is dictated by the prime factorisation of the denominator in lowest terms.

A fraction $p/q$ in lowest terms has a terminating decimal expansion if and only if the prime factorisation of $q$ involves only the primes $2$ and $5$. In every other case the expansion is non-terminating but periodic, with a period whose length divides $\varphi(q)$, where $\varphi$ denotes Euler's totient function.

The two regimes are illustrated by the following examples:

$$
\frac{1}{4} = 0.25, \qquad \frac{3}{8} = 0.375
$$

$$
\frac{1}{3} = 0.\overline{3}, \qquad \frac{1}{7} = 0.\overline{142857}, \qquad \frac{5}{6} = 0.8\overline{3}
$$

The overline indicates the block of digits that repeats indefinitely. In $1/7$ the period has length $6$, the maximal value compatible with $\varphi(7) = 6$. In $5/6$ the expansion has a non-repeating prefix followed by a periodic tail, a behaviour that arises whenever the denominator contains both primes from $\\{2, 5\\}$ and other primes.

> The dichotomy between terminating and eventually periodic expansions provides a working criterion to recognise rational numbers from their decimal form. A real number with a non-terminating and non-periodic expansion is irrational, as discussed in [irrational numbers](../irrational-numbers/).

## Converting a periodic decimal to a fraction

The recovery of a rational number from its periodic decimal expansion is a direct application of elementary algebra. The procedure exploits the fact that multiplying a decimal by a suitable power of $10$ shifts the period by one full cycle, and the difference between the shifted and the original number cancels the periodic tail.

Consider the decimal $x = 0.\overline{27}$, in which the block $27$ repeats indefinitely. Multiplying by $100$ shifts the expansion by two digits, the length of the period:

$$
100 x = 27.\overline{27}
$$

Subtracting the original equation $x = 0.\overline{27}$ removes the periodic tail and produces a linear equation in $x$:

$$
100 x - x = 27 \quad\Longrightarrow\quad 99 x = 27 \quad\Longrightarrow\quad x = \frac{27}{99} = \frac{3}{11}
$$

The last step reduces the fraction to lowest terms by dividing numerator and denominator by $\gcd(27, 99) = 9$. The same method handles expansions with a non-repeating prefix, by first shifting past the prefix and then applying the cancellation argument to the periodic part.

## Density in the real line

The rational numbers are dense in $\mathbb{R}$: between any two distinct real numbers there exists a rational number. For every $x, y \in \mathbb{R}$ with $x < y$, there exists $q \in \mathbb{Q}$ such that $x < q < y$. The argument relies on the Archimedean property of $\mathbb{R}$, discussed in [real numbers](../real-numbers/).

Given $x < y$, the Archimedean property supplies a positive integer $n$ such that $n(y - x) > 1$. The interval $(nx, ny)$ has length greater than $1$, so it contains at least one integer $m$. Dividing through by $n$ gives:

$$
x < \frac{m}{n} < y
$$

The rational number $m/n$ lies strictly between $x$ and $y$. The construction shows that every open interval of $\mathbb{R}$, however small, contains infinitely many rational numbers. The same conclusion holds inside $\mathbb{Q}$ itself: between any two distinct rationals there are infinitely many other rationals.

Density makes the rational line a fine net that approximates every real number arbitrarily well. Despite this, the net is full of holes: the irrational numbers occupy positions that no rational ever reaches, and the completion to $\mathbb{R}$ fills these gaps.

## Cardinality

The rational numbers form a countable set, which means their elements can be placed in a one-to-one correspondence with $\mathbb{N}$. The result is due to Cantor and is established by an explicit enumeration that lists every rational exactly once.

The positive rationals are arranged in an infinite table whose entry in row $p$ and column $q$ is the fraction $p/q$:

$$
\begin{array}{cccccc}
1/1 & 1/2 & 1/3 & 1/4 & 1/5 & \cdots \\[6pt]
2/1 & 2/2 & 2/3 & 2/4 & 2/5 & \cdots \\[6pt]
3/1 & 3/2 & 3/3 & 3/4 & 3/5 & \cdots \\[6pt]
4/1 & 4/2 & 4/3 & 4/4 & 4/5 & \cdots \\[6pt]
\vdots & \vdots & \vdots & \vdots & \vdots & \ddots
\end{array}
$$

Traversing the table along its diagonals and skipping the fractions that have already appeared in lowest terms produces a sequence that enumerates the positive rationals. The negative rationals and zero are inserted with a simple interleaving, and the resulting sequence enumerates $\mathbb{Q}$ in its entirety.

The countability of $\mathbb{Q}$ stands in sharp contrast with the uncountability of $\mathbb{R}$. The two sets have radically different cardinalities, although $\mathbb{Q}$ is dense in $\mathbb{R}$. In the precise sense of cardinality, the rationals form a vanishingly small portion of the real line.

> The contrast between density and cardinality is one of the structural tensions of the real number system. The rationals are everywhere on the line, yet they leave room for an overwhelmingly larger set of irrationals, as discussed in [irrational numbers](../irrational-numbers/).

## Position within the real line

Geometrically, the rational numbers correspond to the points of the real line that admit a fractional label of the form $p/q$ with $p, q \in \mathbb{Z}$ and $q \neq 0$. They are arranged densely along the line, and any sufficiently magnified portion of $\mathbb{R}$ contains infinitely many of them. The remaining points of the line, those that no fraction can name, are the irrational numbers.

The transition from $\mathbb{Q}$ to $\mathbb{R}$ is not algebraic in nature: it does not introduce new operations, nor does it remove any structural limitation of the field axioms. The transition is analytic, and it responds to the failure of $\mathbb{Q}$ to satisfy the [completeness axiom](../real-numbers/). The set:

$$
S = \\{\ q \in \mathbb{Q} : q^2 < 2 \ \\}
$$

is non-empty and bounded above within $\mathbb{Q}$, yet has no least upper bound in $\mathbb{Q}$, because the candidate value $\sqrt{2}$ lies outside the rational field. The construction of $\mathbb{R}$ supplies the missing supremum and, simultaneously, every other irrational quantity that geometric and analytic considerations require.
