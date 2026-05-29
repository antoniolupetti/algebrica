---
title: Irrational Numbers
source: https://algebrica.org/irrational-numbers/
license: CC BY-NC 4.0
tags:
  - algebraic-numbers
  - cardinality
  - decimal-expansion
  - density
  - golden-ratio
  - irrational-numbers
  - real-numbers
  - square-root-of-two
  - transcendental-numbers
---

## Definition

A real number is irrational when it cannot be written as a ratio of two integers. The set of irrational numbers is the complement, inside $\mathbb{R}$, of the [rational numbers](../rational-numbers/) $\mathbb{Q}$, and is denoted by $\mathbb{I}$. The formal description is given by:

$$
\mathbb{I} = \\{\ x \in \mathbb{R} : x \notin \mathbb{Q} \ \\}
$$

Equivalently, $\mathbb{I} = \mathbb{R} \setminus \mathbb{Q}$. The two sets $\mathbb{Q}$ and $\mathbb{I}$ partition the [real line](../real-numbers/): every real number is either rational or irrational, and the two possibilities are mutually exclusive. The decomposition is summarised by the identities:

$$
\mathbb{R} = \mathbb{Q} \cup \mathbb{I}, \qquad \mathbb{Q} \cap \mathbb{I} = \emptyset
$$

Irrational numbers do not arise as an algebraic enlargement of $\mathbb{Q}$ in the sense in which $\mathbb{Z}$ extends $\mathbb{N}$ or $\mathbb{Q}$ extends $\mathbb{Z}$. They appear only when the completion of the rational line forces the existence of points that the rationals fail to occupy, as discussed in [real numbers](../real-numbers/). The presence of $\mathbb{I}$ inside $\mathbb{R}$ is therefore a consequence of the [completeness axiom](../real-numbers/) rather than an independent algebraic construction.

## Decimal representation

The most concrete characterisation of irrational numbers is based on their decimal expansions. A [rational number](../rational-numbers/) always admits a decimal representation that is either terminating, such as $1/4 = 0.25$, or eventually periodic, such as $1/7 = 0.\overline{142857}$. 

An irrational number behaves differently: its decimal expansion is non-terminating and non-periodic, which means that no finite block of digits repeats indefinitely from some point onward.

This dichotomy provides a working criterion for irrationality. A [real number](../real-numbers/) $x$ is rational if and only if its decimal expansion is eventually periodic. The contrapositive states that any decimal expansion lacking eventual periodicity defines an irrational number. The following construction illustrates the point:

$$
x = 0.101001000100001000001\ldots
$$

The digits are arranged so that each $1$ is separated from the next by an increasing number of zeros. No block of digits repeats forever, and the resulting number is irrational by direct construction. The example shows that irrational numbers can be exhibited explicitly, without any reference to algebraic equations or to geometric magnitudes.

## Irrationality of $\sqrt{2}$

The oldest known irrational number is $\sqrt{2}$, the length of the diagonal of a unit square. The classical proof of its irrationality proceeds by contradiction and relies only on elementary properties of the integers.

Suppose, for contradiction, that $\sqrt{2}$ is rational. Then there exist integers $p$ and $q$ with $q \neq 0$ such that:

$$
\sqrt{2} = \frac{p}{q}
$$

The fraction $p/q$ can be assumed to be in lowest terms, that is, with $p$ and $q$ sharing no common factor greater than $1$. Squaring both sides yields:

$$
2 = \frac{p^2}{q^2} \quad\Longrightarrow\quad p^2 = 2q^2
$$

The equation $p^2 = 2q^2$ shows that $p^2$ is an even integer, and since the square of an odd number is odd, this forces $p$ itself to be even. Write $p = 2k$ for some integer $k$. Substituting gives:

$$
(2k)^2 = 2q^2 \quad\Longrightarrow\quad 4k^2 = 2q^2 \quad\Longrightarrow\quad q^2 = 2k^2
$$

The same argument applied to $q^2$ implies that $q$ is also even. Hence both $p$ and $q$ are divisible by $2$, in contradiction with the assumption that the fraction $p/q$ was in lowest terms. The original hypothesis therefore fails, and $\sqrt{2}$ cannot be expressed as a ratio of two integers.

> The same argument extends without modification to every square root $\sqrt{n}$ with $n$ a positive integer that is not a perfect square. More generally, the root $\sqrt[k]{n}$ is irrational whenever $n$ is a positive integer that is not the $k$-th power of an integer.

## Algebraic and transcendental irrationals

The irrational numbers further split into two disjoint classes according to a finer algebraic criterion. A real number is algebraic if it is a root of some nonzero polynomial with integer coefficients, and transcendental otherwise. The classification interacts with the rational and irrational dichotomy as follows:

+ Every rational number is algebraic, since $p/q$ is the unique root of the polynomial $qx - p$.
+ Many irrational numbers are algebraic. The number $\sqrt{2}$ is a root of $x^2 - 2$, and the [golden ratio](../golden-ratio/) is a root of $x^2 - x - 1$.
+ Transcendental numbers are necessarily irrational, since rationality would make them algebraic.

The transcendental irrationals form the most elusive class, and proving that a specific number is transcendental is often a delicate matter. The Lindemann-Weierstrass theorem establishes the transcendence of $e$ and $\pi$, and a discussion of these results, together with the partition $\mathbb{R} = \mathbb{A} \cup (\mathbb{R} \setminus \mathbb{A})$, is given in [types of numbers](../types-of-numbers/).

## Classical examples

Several irrational numbers occur repeatedly across mathematics and admit short descriptions. They illustrate how irrationality arises from different sources, ranging from algebraic equations to analytic limits.

+ The square root $\sqrt{n}$ is irrational for every positive integer $n$ that is not a perfect square. The smallest cases are $\sqrt{2}$, $\sqrt{3}$, $\sqrt{5}$, $\sqrt{6}$, $\sqrt{7}$, $\sqrt{8}$, and $\sqrt{10}$.
+ The cube root $\sqrt[3]{n}$ is irrational for every positive integer $n$ that is not a perfect cube. The same principle generalises to higher roots.
+ The golden ratio, defined by $\varphi = (1 + \sqrt{5})/2$, is the positive root of $x^2 - x - 1 = 0$ and inherits its irrationality from $\sqrt{5}$.
+ The number $\pi$ is the ratio of the circumference of a circle to its diameter and is transcendental.
+ The number $e$ is the base of the natural logarithm and is transcendental as well. It can be introduced as the [limit of a sequence](../euler-number-limit-sequence/) of rationals that does not converge to a rational value.

A further example is provided by the natural logarithm $\ln 2$, which is transcendental and therefore irrational. The decimal expansions of these constants begin as follows:

$$
\sqrt{2} = 1.41421356\ldots, \qquad \varphi = 1.61803398\ldots
$$

$$
\pi = 3.14159265\ldots, \qquad e = 2.71828182\ldots
$$

The digits continue indefinitely without falling into any repeating pattern, in agreement with the decimal characterisation of irrationality.

## Density on the real line

Irrational numbers are not isolated points on the real line. Between any two distinct real numbers there exists an irrational number, a property known as the density of $\mathbb{I}$ in $\mathbb{R}$. Given $x, y \in \mathbb{R}$ with $x < y$, one can produce an irrational $\xi$ with $x < \xi < y$ as follows.

By the density of the rationals in $\mathbb{R}$, there exists $q \in \mathbb{Q}$ such that the inequality below holds:

$$
x - \sqrt{2} < q < y - \sqrt{2}
$$

Adding $\sqrt{2}$ to each term gives $x < q + \sqrt{2} < y$. The number $\xi = q + \sqrt{2}$ is irrational, because the sum of a rational and an irrational number is always irrational. To see this last fact, suppose $q + \sqrt{2}$ were rational. Then $\sqrt{2} = (q + \sqrt{2}) - q$ would be a difference of rationals and hence rational, contradicting the irrationality of $\sqrt{2}$.

The argument shows that every open interval of $\mathbb{R}$, however small, contains infinitely many irrational numbers. Combined with the analogous density statement for $\mathbb{Q}$, this means that rationals and irrationals are interleaved at every scale on the real line.

## Cardinality

Although rationals and irrationals are both dense, they differ profoundly at the level of cardinality. The set $\mathbb{Q}$ is countable, while the set $\mathbb{R}$ is uncountable. The argument is short and rests on the identity $\mathbb{R} = \mathbb{Q} \cup \mathbb{I}$. If $\mathbb{I}$ were countable, then $\mathbb{R}$ would be the union of two countable sets, and hence countable as well. Since this conclusion is false, $\mathbb{I}$ must be uncountable.

The result has a striking interpretation. In the sense of cardinality, almost every real number is irrational: the rationals form a vanishingly small subset of $\mathbb{R}$, even though they are dense in it. The picture sharpens further when one separates algebraic and transcendental irrationals. The algebraic numbers $\mathbb{A}$ are countable, since each polynomial with integer coefficients has finitely many roots and the family of such polynomials is countable. The transcendental numbers, which form the complement $\mathbb{R} \setminus \mathbb{A}$ inside $\mathbb{R}$, are therefore uncountable.

> The contrast between density and cardinality is one of the foundational tensions in the analysis of $\mathbb{R}$. The rationals fill the line densely, yet leave room for an overwhelmingly larger set of irrationals, and within the irrationals the transcendentals dominate the algebraic ones in cardinality, despite being far harder to exhibit explicitly.

## Algebraic behaviour

The set $\mathbb{I}$ is not closed under the standard arithmetic operations, in sharp contrast with $\mathbb{Q}$ and $\mathbb{R}$. The failure of closure is evident from elementary examples.

The sum of two irrational numbers may be rational, as the following identity shows:

$$
\sqrt{2} + (-\sqrt{2}) = 0
$$

The product of two irrational numbers may be rational as well:

$$
\sqrt{2} \cdot \sqrt{2} = 2, \qquad \sqrt{2} \cdot \sqrt{8} = 4
$$

A mixed operation between a rational and an irrational number behaves more predictably. If $q \in \mathbb{Q}$ and $\xi \in \mathbb{I}$, then $q + \xi \in \mathbb{I}$, and if $q \neq 0$ then $q \cdot \xi \in \mathbb{I}$. The argument is the same in both cases: a rational result would force $\xi$ to be rational, contradicting the assumption.

The structural conclusion is that $(\mathbb{I}, +)$ is not a [group](../groups/), since it is not closed under addition, and $\mathbb{I}$ is not a [ring](../rings/) in any natural way. The algebraic richness of the real number system resides in $\mathbb{R}$ itself, not in either of the two complementary pieces $\mathbb{Q}$ and $\mathbb{I}$ taken separately.

## Geometric origin

The discovery of irrational numbers is traditionally attributed to the Pythagorean school and is linked to the diagonal of the unit square. By the Pythagorean theorem, the length $d$ of the diagonal of a square of side $1$ satisfies:

$$
d^2 = 1^2 + 1^2 = 2
$$

The diagonal therefore measures $d = \sqrt{2}$, a quantity that the proof above shows to be irrational. The same construction applied to a regular pentagon yields the golden ratio $\varphi$, while the rectification of the circle produces $\pi$. 

The historical sequence in which these numbers appeared reflects the gradual recognition that the rational numbers, despite their density, do not suffice to measure the lengths arising from elementary geometric figures. The completion to $\mathbb{R}$ resolves this insufficiency by adjoining all the irrational magnitudes that geometry inevitably produces.
