---
title: Irrational Numbers
source: https://algebrica.org/irrational-numbers/
license: CC BY-NC 4.0
tags:
  - algebraic-numbers
  - cardinality
  - cauchy-sequence
  - decimal-expansion
  - density
  - golden-ratio
  - irrational-numbers
  - real-numbers
  - square-root-of-two
  - transcendental-numbers
---

## Definition

A real number is irrational when it cannot be written as a ratio of two integers. The set of irrational numbers is the complement, inside $\mathbb{R},$ of the [rational numbers](../rational-numbers/) $\mathbb{Q},$ and is denoted by $\mathbb{I}.$ The formal description is given by:

$$
\mathbb{I} = \{x \in \mathbb{R} \mid x \notin \mathbb{Q}\}
$$

Equivalently, $\mathbb{I} = \mathbb{R} \setminus \mathbb{Q}.$ The two sets $\mathbb{Q}$ and $\mathbb{I}$ form a [partition](../sets/) of the [real line](../real-numbers/). Every real number is either rational or irrational, and the two possibilities are mutually exclusive. The decomposition is summarised by the identities:

$$
\mathbb{R} = \mathbb{Q} \cup \mathbb{I}, \qquad \mathbb{Q} \cap \mathbb{I} = \emptyset
$$

Irrational numbers do not arise as an algebraic enlargement of $\mathbb{Q}$ in the sense in which $\mathbb{Z}$ extends $\mathbb{N}$ or $\mathbb{Q}$ extends $\mathbb{Z}.$ They appear only when the completion of the rational line forces the existence of points that the rationals fail to occupy. The presence of $\mathbb{I}$ inside $\mathbb{R}$ is therefore a consequence of the [completeness axiom](../real-numbers/) rather than an independent algebraic construction.

## Decimal representation

Decimal expansions give a direct characterisation of irrational numbers. A [rational number](../rational-numbers/) always has a decimal representation that is either terminating, such as $1/4 = 0.25,$ or eventually periodic, such as $1/7 = 0.\overline{142857}.$

An irrational number has a non-terminating and non-periodic decimal expansion. No finite block of digits repeats indefinitely from some point onward.

This dichotomy is a working criterion for irrationality. A real number $x$ is rational if and only if its decimal expansion is eventually periodic. The contrapositive states that any decimal expansion lacking eventual periodicity defines an irrational number. The following construction illustrates the point:

$$
x = 0.101001000100001000001\ldots
$$

The digits are arranged so that each $1$ is separated from the next by an increasing number of zeros. No block of digits repeats forever, and the resulting number is irrational by direct construction. The example shows that irrational numbers can be exhibited explicitly, without any reference to algebraic equations or to geometric magnitudes.

## Irrationality of $\sqrt{2}$

The number $\sqrt{2},$ the length of the diagonal of a unit square, is a classical example of an irrational number. Its proof by contradiction uses only elementary properties of the integers.

Suppose, for contradiction, that $\sqrt{2}$ is rational. Then there exist integers $p$ and $q$ with $q \neq 0$ such that:

$$
\sqrt{2} = \frac{p}{q}
$$

The fraction $p/q$ can be assumed to be in lowest terms, that is, with $p$ and $q$ sharing no common factor greater than $1.$ Squaring both sides yields:

$$
2 = \frac{p^2}{q^2} \quad\Longrightarrow\quad p^2 = 2q^2
$$

The equation $p^2 = 2q^2$ shows that $p^2$ is an even integer, and since the square of an odd number is odd, this forces $p$ itself to be even. Write $p = 2k$ for some integer $k.$ Substituting gives:

$$
(2k)^2 = 2q^2 \quad\Longrightarrow\quad 4k^2 = 2q^2 \quad\Longrightarrow\quad q^2 = 2k^2
$$

The same argument applied to $q^2$ implies that $q$ is also even. Hence both $p$ and $q$ are divisible by $2,$ in contradiction with the assumption that the fraction $p/q$ was in lowest terms. The original hypothesis therefore fails, and $\sqrt{2}$ cannot be expressed as a ratio of two integers.

The contradiction can also be formulated as an infinite descent. Starting from positive integers $p,q$ satisfying $p^2=2q^2,$ write $p=2k.$ The equation then becomes $q^2=2k^2,$ so $(q,k)$ is another positive integer solution of the same equation. Moreover, $q<p$ because $p^2=2q^2.$ Repeating the construction would produce an infinite strictly decreasing sequence of positive integers, which is impossible by the well-ordering of $\mathbb{N}.$

The rational gap at $\sqrt{2}$ can be bracketed with arbitrary precision. For every rational $\varepsilon>0,$ there exists a non-negative rational $x$ such that:

$$
x^2<2<(x+\varepsilon)^2
$$

Suppose no such $x$ existed. Since no rational square equals $2,$ the implication $x^2<2 \Rightarrow (x+\varepsilon)^2<2$ would hold for every non-negative rational $x.$ Starting with $0^2<2,$ induction would give $(n\varepsilon)^2<2$ for every $n\in\mathbb{N}.$ By the Archimedean property, there is an integer $n>2/\varepsilon,$ for which $n\varepsilon>2$ and hence $(n\varepsilon)^2>4,$ a contradiction. For $\varepsilon=0.001,$ one may take $x=1.414,$ since $1.414^2=1.999396$ and $1.415^2=2.002225.$

Thus rational numbers can approach the missing value from both sides even though none equals it. Successively choosing smaller values of $\varepsilon$ produces rational approximations such as $1.4,1.41,1.414,\ldots.$ These approximations form a [Cauchy sequence](../cauchy-sequence/) whose limit is absent from $\mathbb{Q}$ and is present in its completion $\mathbb{R}.$

> Let $k\geq2$ and let $n$ be a positive integer that is not a perfect $k$-th power. Some prime occurs in the factorisation of $n$ with an exponent not divisible by $k.$ If $\sqrt[k]{n}=p/q$ for relatively prime positive integers $p,q,$ then $p^k=nq^k.$ The exponent of that prime would be both divisible by $k$ and nonzero modulo $k,$ a contradiction. Hence $\sqrt[k]{n}$ is irrational.

## Algebraic and transcendental irrationals

The irrational numbers further split into two disjoint classes according to a finer algebraic criterion. A real number is algebraic if it is a root of some nonzero [polynomial](../polynomials/) with integer coefficients, and transcendental otherwise. The classification interacts with the rational and irrational dichotomy as follows:

+ Every rational number is algebraic, since $p/q$ is the unique root of the polynomial $qx - p.$
+ Many irrational numbers are algebraic. The number $\sqrt{2}$ is a root of $x^2 - 2,$ and the golden ratio is a root of $x^2 - x - 1.$
+ Transcendental numbers are necessarily irrational, since rationality would make them algebraic.

Proving that a specific number is transcendental usually requires results beyond elementary algebra. The Lindemann-Weierstrass theorem establishes the transcendence of $e$ and $\pi.$ The partition $\mathbb{R} = \mathbb{A} \cup (\mathbb{R} \setminus \mathbb{A})$ is discussed in [types of numbers](../types-of-numbers/).

## Classical examples

Several irrational numbers have short algebraic, geometric, or analytic definitions.

+ The [square root](../radicals/) $\sqrt{n}$ is irrational for every positive integer $n$ that is not a perfect square. The smallest cases are $\sqrt{2},$ $\sqrt{3},$ $\sqrt{5},$ $\sqrt{6},$ $\sqrt{7},$ $\sqrt{8},$ and $\sqrt{10}.$
+ The cube root $\sqrt[3]{n}$ is irrational for every positive integer $n$ that is not a perfect cube. The same principle generalises to higher roots.
+ The golden ratio, defined by $\varphi = (1 + \sqrt{5})/2,$ is the positive root of $x^2 - x - 1 = 0$ and inherits its irrationality from $\sqrt{5}.$
+ The number $\pi$ is the ratio of the [circumference](../circumference/) of a circle to its diameter and is transcendental.
+ The number $e$ is the base of the [natural logarithm](../logarithms/) and is transcendental as well. It can be introduced as the [limit of a sequence](../euler-number-limit-sequence/) of rationals that does not converge to a rational value.

The natural logarithm $\ln 2$ is another transcendental, and therefore irrational, number. The decimal expansions of these constants begin as follows:

$$
\sqrt{2} = 1.41421356\ldots, \qquad \varphi = 1.61803398\ldots
$$

$$
\pi = 3.14159265\ldots, \qquad e = 2.71828182\ldots
$$

The digits continue indefinitely without falling into any repeating pattern, in agreement with the decimal characterisation of irrationality.

## Density on the real line

Irrational numbers are not isolated points on the real line. Between any two distinct real numbers there exists an irrational number, a property known as the density of $\mathbb{I}$ in $\mathbb{R}.$ Given $x, y \in \mathbb{R}$ with $x < y,$ one can produce an irrational $\xi$ with $x < \xi < y$ as follows.

By the density of the rationals in $\mathbb{R},$ there exists $q \in \mathbb{Q}$ such that the inequality below holds:

$$
x - \sqrt{2} < q < y - \sqrt{2}
$$

Adding $\sqrt{2}$ to each term gives $x < q + \sqrt{2} < y.$ The number $\xi = q + \sqrt{2}$ is irrational, because the sum of a rational and an irrational number is always irrational. To see this last fact, suppose $q + \sqrt{2}$ were rational. Then $\sqrt{2} = (q + \sqrt{2}) - q$ would be a difference of rationals and hence rational, contradicting the irrationality of $\sqrt{2}.$

The argument shows that every open interval of $\mathbb{R},$ however small, contains infinitely many irrational numbers. Combined with the analogous density statement for $\mathbb{Q},$ this means that rationals and irrationals are interleaved at every scale on the real line.

## Cardinality

Rationals and irrationals are both dense but have different cardinalities. The set $\mathbb{Q}$ is countable, while $\mathbb{R}$ is uncountable. If $\mathbb{I}$ were countable, then the identity $\mathbb{R}=\mathbb{Q}\cup\mathbb{I}$ would express $\mathbb{R}$ as a union of two countable sets. Therefore $\mathbb{I}$ is uncountable.

Thus the irrationals are uncountable even though the rationals are dense in $\mathbb{R}.$ The algebraic numbers $\mathbb{A}$ are countable, since each polynomial with integer coefficients has finitely many roots and the family of such polynomials is countable. Their complement $\mathbb{R} \setminus \mathbb{A},$ the set of transcendental numbers, is therefore uncountable.

> Density and cardinality measure different properties. Every open interval contains rational and irrational numbers, but the rationals and the algebraic numbers are countable, whereas the irrationals and the transcendental numbers are uncountable.

## Algebraic behaviour

The set $\mathbb{I}$ is not closed under the usual arithmetic operations, unlike $\mathbb{Q}$ and $\mathbb{R}.$ Elementary examples show the failure of closure.

The sum of two irrational numbers may be rational, as the following identity shows:

$$
\sqrt{2} + (-\sqrt{2}) = 0
$$

The product of two irrational numbers may be rational as well:

$$
\sqrt{2} \cdot \sqrt{2} = 2, \qquad \sqrt{2} \cdot \sqrt{8} = 4
$$

A mixed operation between a rational and an irrational number has a fixed outcome. If $q \in \mathbb{Q}$ and $\xi \in \mathbb{I},$ then $q + \xi \in \mathbb{I},$ and if $q \neq 0$ then $q \cdot \xi \in \mathbb{I}.$ In either case, a rational result would force $\xi$ to be rational, contradicting the assumption.

Consequently, $(\mathbb{I}, +)$ is not a [group](../groups/) because it is not closed under addition, and $\mathbb{I}$ is not a [ring](../rings/) under the operations inherited from $\mathbb{R}.$ The field structure belongs to $\mathbb{R},$ not to either complementary subset $\mathbb{Q}$ or $\mathbb{I}$ separately.

## Geometric origin

The discovery of irrational numbers is traditionally attributed to the Pythagorean school and is linked to the diagonal of the unit square. By the [Pythagorean theorem](../pythagorean-theorem/), the length $d$ of the diagonal of a square of side $1$ satisfies:

$$
d^2 = 1^2 + 1^2 = 2
$$

The diagonal therefore measures $d = \sqrt{2},$ a quantity that the proof above shows to be irrational. The same construction applied to a regular pentagon yields the golden ratio $\varphi,$ while the rectification of the circle produces $\pi.$

These examples show that rational numbers, despite their density, do not measure every length arising from elementary geometric figures. The completion $\mathbb{R}$ contains the missing irrational lengths.
