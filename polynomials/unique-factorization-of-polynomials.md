---
title: Unique Factorization of Polynomials
source: https://algebrica.org/unique-factorization-of-polynomials/
license: CC BY-NC 4.0
tags:
  - euclids-lemma
  - irreducible-polynomial
  - polynomial
  - polynomial-factorization
  - polynomial-ring
  - unique-factorization
---

## Divisibility, units and associates

Let $\mathbb{F}$ be a [field](../fields/). For [polynomials](../polynomials/) $A(x),B(x)\in\mathbb{F}[x]$, the polynomial $B(x)$ divides $A(x)$ if some $Q(x)\in\mathbb{F}[x]$ satisfies the identity $A(x)=B(x)Q(x)$. In this case $B(x)$ is a divisor of $A(x)$, and $A(x)$ is a multiple of $B(x)$.

A unit is a polynomial that has a multiplicative inverse in $\mathbb{F}[x]$. The units are exactly the nonzero constant polynomials. If $U(x)V(x)=1$, the [degree formula for a product](../multiplying-polynomials/) is:

$$
\deg U+\deg V=0
$$

Both degrees must be zero. Conversely, each nonzero constant $c\in\mathbb{F}$ has the constant inverse $c^{-1}$ because $\mathbb{F}$ is a field.

Two polynomials are associates when one is a unit multiple of the other. Thus $A(x)$ and $cA(x)$ are associates for every nonzero scalar $c$. Associates have the same divisibility properties, so a factor is determined only up to multiplication by a nonzero constant unless a normalization is imposed.

The usual normalization takes each nonconstant factor to be monic. Every nonzero polynomial $A(x)$ has a unique monic associate, obtained by dividing $A(x)$ by its leading coefficient. For example, the same polynomial has these two decompositions:

$$
12(x-1)(x+1)=3(2x-2)(2x+2)
$$

The factors differ only by the placement of constant units in $\mathbb{Q}[x]$. Keeping the leading coefficient outside the product and choosing monic factors removes this ambiguity.

## Irreducible and prime polynomials

A polynomial $P(x)\in\mathbb{F}[x]$ is irreducible over $\mathbb{F}$ if it has positive degree and every factorization $P(x)=A(x)B(x)$ contains a unit among $A(x)$ and $B(x)$. The phrase "over $\mathbb{F}$" is part of the assertion because changing the coefficient field can introduce new factors.

A nonzero nonunit $P(x)$ is prime in $\mathbb{F}[x]$ when the following implication holds for all $A(x),B(x)\in\mathbb{F}[x]$:

$$
P(x)\mid A(x)B(x)\quad\Longrightarrow\quad P(x)\mid A(x)\text{ or }P(x)\mid B(x)
$$

Prime and irreducible elements need not coincide in every [integral domain](../rings/). They do coincide in $\mathbb{F}[x]$, as follows from the Euclidean algorithm.

Every polynomial of degree one is irreducible. A polynomial of degree two or three is irreducible over $\mathbb{F}$ precisely when it has no [root](../roots-of-a-polynomial/) in $\mathbb{F}$. If such a polynomial were reducible, one of its nonconstant factors would have degree one, so the polynomial would have a root. The converse follows from the [factor theorem](../polynomial-division/).

For degree four and above, the absence of roots does not prove irreducibility. Consider the polynomial given by:

$$
(x^2+1)(x^2+2)
$$

It has no real root, but its displayed expression is already a nontrivial factorization in $\mathbb{R}[x]$.

## Euclid's lemma in polynomial rings

In the [Euclidean algorithm for polynomials](../polynomial-division/), the monic associate of the last nonzero remainder is the greatest common divisor. Back-substitution proves Bézout's identity. If $A(x)$ and $B(x)$ are not both zero, polynomials $S(x),T(x)\in\mathbb{F}[x]$ satisfy:

$$
S(x)A(x)+T(x)B(x)=\gcd(A,B)
$$

Suppose that an irreducible polynomial $P(x)$ divides $A(x)B(x)$ but does not divide $A(x)$. Every common divisor of $P(x)$ and $A(x)$ must then be a unit. After monic normalization their greatest common divisor is $1$, so polynomials $S(x)$ and $T(x)$ satisfy:

$$
S(x)P(x)+T(x)A(x)=1
$$

After multiplication by $B(x)$, the identity is:

$$
S(x)P(x)B(x)+T(x)A(x)B(x)=B(x)
$$

The polynomial $P(x)$ divides both terms on the left. It therefore divides $B(x)$. This proves Euclid's lemma in $\mathbb{F}[x]$ and shows that every irreducible polynomial is prime.

Conversely, every prime polynomial is irreducible. If a prime $P(x)$ were written as $P(x)=A(x)B(x)$, primality would force $P(x)$ to divide one factor. Cancellation then shows that the other factor is a unit. Hence prime and irreducible polynomials are the same elements of $\mathbb{F}[x]$, up to associates.

## The unique factorization theorem

Every nonzero polynomial $A(x)\in\mathbb{F}[x]$ of positive degree has a factorization of the form:

$$
A(x)=aP_1(x)^{e_1}\cdots P_r(x)^{e_r}
$$

In this expression $a\in\mathbb{F}$ is the nonzero leading coefficient of $A(x)$, the polynomials $P_1(x),\ldots,P_r(x)$ are distinct monic irreducible polynomials, and the exponents $e_1,\ldots,e_r$ are positive integers. The scalar $a$, the irreducible factors, and their exponents are unique apart from the order of the factors.

Existence follows by induction on $\deg A$. A polynomial of degree one is irreducible. For the inductive step, either $A(x)$ is irreducible or it has a factorization $A(x)=B(x)C(x)$ in which both factors have smaller positive degree. By induction, both factors are products of irreducibles, so their combined product is a factorization of $A(x)$. Rescaling each irreducible factor to make it monic moves all constant factors into $a$, and equal monic factors can be collected into powers. Since the degree decreases in every nontrivial factorization, the process cannot continue indefinitely.

For uniqueness, suppose that two products of irreducibles are equal. An irreducible factor from the first product divides the entire second product. Repeated application of Euclid's lemma shows that it divides one irreducible factor in the second product. Those two factors are associates, and they are equal if both are monic. Cancelling the common factor reduces the comparison to products of smaller degree. Iteration matches every factor and its multiplicity. The leading coefficients on the two sides then determine the same scalar $a$.

> Constant nonzero polynomials correspond to the case $r=0$, with the product of irreducible factors interpreted as an empty product. The zero polynomial has no factorization of this form because every polynomial divides zero.

The proof depends on a fixed sequence of results. Division with remainder makes the Euclidean algorithm possible. Back-substitution proves Bézout's identity, which proves Euclid's lemma. Euclid's lemma supplies uniqueness.

## Dependence on the coefficient field

Irreducibility can change when the coefficient field is enlarged. The polynomial $x^2-2$ has no rational root and is irreducible in $\mathbb{Q}[x]$, while in $\mathbb{R}[x]$ it has the following factorization:

$$
x^2-2=(x-\sqrt{2})(x+\sqrt{2})
$$

The polynomial $x^2+1$ is irreducible in $\mathbb{R}[x]$ but splits in $\mathbb{C}[x]$ as follows:

$$
x^2+1=(x-i)(x+i)
$$

The [Fundamental Theorem of Algebra](../roots-of-a-polynomial/) implies that every irreducible polynomial in $\mathbb{C}[x]$ has degree one. Over $\mathbb{R}$, the irreducible polynomials are the linear polynomials and the quadratic polynomials with negative discriminant. If $\alpha+i\beta$ is a nonreal root of a real polynomial, then $\beta\neq 0$ and $\alpha-i\beta$ is also a root. The product of the corresponding linear factors is:

$$
(x-\alpha-i\beta)(x-\alpha+i\beta)=x^2-2\alpha x+\alpha^2+\beta^2
$$

This quadratic has discriminant $-4\beta^2$, so it has no real root.

For a concrete comparison, consider the polynomial defined by:

$$
A(x)=6x^4-30x^2+36
$$

Its factorization into monic irreducibles over $\mathbb{Q}$ is:

$$
A(x)=6(x^2-2)(x^2-3)
$$

Neither quadratic has a rational root. Over $\mathbb{R}$ both factors split, and the factorization becomes:

$$
A(x)=6(x-\sqrt{2})(x+\sqrt{2})(x-\sqrt{3})(x+\sqrt{3})
$$

Uniqueness holds in each polynomial ring, but the irreducible factors depend on the chosen field.

## Integer coefficients and Gauss's lemma

The coefficient ring $\mathbb{Z}$ is not a field, so division by a leading coefficient may leave $\mathbb{Z}[x]$. Factorization over the [integers](../integers/) is connected to factorization over $\mathbb{Q}$ through the content of a polynomial. For a nonzero polynomial $A(x)\in\mathbb{Z}[x]$, its content $c(A)$ is the positive greatest common divisor of its coefficients. The polynomial is primitive when $c(A)=1$.

Gauss's lemma states that the product of two primitive polynomials is primitive. Suppose that a prime integer $p$ divides every coefficient of $A(x)B(x)$. Since $A(x)$ and $B(x)$ are primitive, both reductions modulo $p$ are nonzero, while the reduction of their product is zero. This is impossible because the polynomial ring $\mathbb{F}_p[x]$ has no zero divisors.

Every nonzero integer polynomial has the following decomposition:

$$
A(x)=c(A)A_0(x)
$$

The polynomial $A_0(x)$ is primitive. Gauss's lemma has two useful consequences.

+ A primitive polynomial of positive degree is irreducible in $\mathbb{Z}[x]$ if and only if it is irreducible in $\mathbb{Q}[x]$.
+ The factorization of an integer polynomial separates into the prime factorization of its content and the factorization of its primitive part.

For example, $6x^2-12=6(x^2-2)$. Here $6$ is the content, while $x^2-2$ is primitive and irreducible over $\mathbb{Q}$. The [rational root theorem](../roots-of-a-polynomial/) and other irreducibility criteria apply to the primitive part.
