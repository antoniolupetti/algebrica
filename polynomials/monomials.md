---
title: Monomials
source: https://algebrica.org/monomials/
license: CC BY-NC 4.0
tags:
  - degree-of-a-monomial
  - gcd
  - lcm
  - monomial
  - polynomial
---

## Definition

A monomial is an algebraic expression consisting of a single term. It is written as the product of a numerical coefficient and one or more variables, each raised to a non-negative [integer](../integers/) exponent. The general form of a monomial is:

$$
a \cdot x_1^{n_1} \cdot x_2^{n_2} \cdot \dots \cdot x_k^{n_k}
$$

+ $a \in \mathbb{R}$ is the numerical coefficient.
+ $x_1, x_2, \dots, x_k$ are the variables.
+ $n_1, n_2, \dots, n_k \in \mathbb{N}_0$ are the exponents.

The zero monomial is the special case where $a = 0$. It is considered a monomial but its degree is left undefined.

- - -
Examples of monomials include:

+ $4$: a non-zero real constant (coefficient only, no variables).
+ $-2x$: coefficient $-2$ and variable $x$ with exponent $1$.
+ $3x^2y$: coefficient $3$, variable $x$ with exponent $2$, variable $y$ with exponent $1$.
+ $0$: the zero monomial.

A monomial in $k$ variables can be viewed as an element of the polynomial ring $\mathbb{R}[x_1, \dots, x_k]$, where it corresponds to a single term of the form $a \cdot x_1^{n_1} \cdots x_k^{n_k}$.

> A [ring](../rings/) is an algebraic structure with two operations, addition and multiplication, that satisfy associativity, distributivity, and the existence of an additive identity and additive inverses.

- - -
A [polynomial](../polynomials/) is called homogeneous if all its terms have the same total degree. Since a monomial consists of a single term, every monomial is homogeneous by definition. The monomials of degree $d$ in $k$ variables form a basis for the $\mathbb{R}$ [vector](../vectors/) space of homogeneous polynomials of degree $d$. For example, $x^2, xy, y^2$ form a basis for the space of homogeneous polynomials of degree $2$ in two variables. Polynomials with two or three such terms receive specific names: [binomials](../binomials/) for two terms, [trinomials](../trinomials/) for three.


## Why exponents in a monomial must be non-negative integers

The constraint that exponents be non-negative integers follows directly from the definition of a [polynomial](../polynomials/): each variable must appear with an exponent in $\mathbb{N}_0$. This ensures that a monomial represents a finite product of variables, with no divisions or radicals involved. The following expressions are not monomials:

$$
3x^{-1} \qquad 5x^{1/2} \qquad \frac{4}{x}
$$

In the first case, $x^{-1} = 1/x$, a negative exponent introduces a division.
In the second, $x^{1/2} = \sqrt{x}$, a fractional exponent introduces a radical.
The third case, $4/x = 4x^{-1}$, is simply a negative exponent in disguise.


## Degree of a monomial

The degree of a monomial is the sum of the exponents of all its variables. For the monomial $ab^2c^3$, the exponents are $1$, $2$, and $3$, so its degree is:

$$1 + 2 + 3 = 6$$

The degree of a non-zero constant is $0$, since no variables are present. The zero monomial has no defined degree.

- - -
The partial degree of a monomial with respect to a given variable is the exponent of that variable. For the monomial $3x^2y^3$, the partial degree in $x$ is $2$ and the partial degree in $y$ is $3$. The total degree is the sum of all partial degrees:

$$2 + 3 = 5$$

- - -
The total number of monomials of degree $d$ in $k$ variables can be determined using the following [binomial coefficient](../binomial-coefficient/):

$$\binom{d+k-1}{k-1}$$

For instance, the monomials of degree $2$ in $2$ variables are $x^2$, $xy$, and $y^2$. This corresponds to:

$$\binom{2+2-1}{2-1} = \binom{3}{1} = 3$$


## Similar, opposite and equal monomials

Two monomials are defined as similar if they possess identical variable parts, meaning the same variables raised to the same exponents. For example, $3x^2y$ and $-5x^2y$ are similar monomials.

Two monomials are considered opposite if they are similar and their coefficients sum to zero. For instance, $4xy$ and $-4xy$ are opposite monomials.

Two monomials are defined as equal if they have both the same variable part and the same coefficient. Formally, two monomials are equal if and only if they are similar and their coefficients are equal.


## Addition and subtraction of monomials

In polynomial algebra, the addition or subtraction of monomials is governed by specific rules. Monomials may be combined only if their variables and corresponding exponents are identical. In these cases, the coefficients are added or subtracted, while the variables and exponents remain unchanged. For example:

$$3x + 2x = 5x$$

For the expression $3x^2 + 2x$, the monomials cannot be combined because they have different variable parts.


## Product of monomials

Monomials can be multiplied by multiplying their coefficients and adding the [exponents](../powers/) of the like variables. For instance, the product of $(3x^2)(2x^3)$ can be computed as follows:

+ First, we multiply the coefficients: $3 \times 2 = 6$
+ Next, we add the exponents of the like variables: $2+3 = 5$

Thus, we get:

$$(3x^2)(2x^3) = 6x^{2+3} = 6x^5 $$

The same rule applies to monomials with multiple variables: multiply the coefficients and add the exponents of each variable independently. For example:

$$(3x^2y)(2xy^3) = 6x^{2+1}y^{1+3} = 6x^3y^4 $$

- - -
The product of monomials is both commutative and associative, since multiplication in $\mathbb{R}[x_1, \dots, x_k]$ inherits these properties from $\mathbb{R}$. This means the order and grouping of factors does not affect the result:

$$(3x^2y)(2xy^3) = (2xy^3)(3x^2y) = 6x^3y^4$$

- - -
The set of all monomials in $k$ variables with coefficients in $\mathbb{R}$ is closed under multiplication, as the product of any two monomials yields another monomial. Consequently, the monomials constitute a multiplicative semigroup within the polynomial ring $\mathbb{R}[x_1, \dots, x_k].$ This product extends, via the distributive property, to the more general operation of [multiplying polynomials](../multiplying-polynomials/) of arbitrary length.


## Division of monomials

To divide monomials, divide their coefficients and subtract the exponents of like variables. For example:

$$ \frac{6x^5}{2x^2} = 3x^{5-2} = 3x^3 $$

This rule also applies to monomials with multiple variables: divide the coefficients and subtract the exponents of each variable independently. For example:

$$ \frac{6x^3y^2}{2xy} = 3x^{3-1}y^{2-1} = 3x^2y $$

If the exponent in the divisor is greater than that in the dividend, the result will have a negative exponent, which can be rewritten as a fraction. For example:

$$ \frac{x^2}{3x^3} = \frac{1}{3} x^{2-3} = \frac{1}{3} x^{-1} = \frac{1}{3x} $$

Dividing monomials is straightforward when the bases are the same. In contrast, dividing polynomials is more complex and requires structured methods such as [polynomial long division](../polynomial-division/) or [Ruffini's rule](../synthetic-division/).


## Powers

When a monomial is raised to a [power](../powers/), the exponent applies to each factor: the coefficient is raised to that power, and the exponents of the variables are multiplied by it. For a monomial raised to a positive integer power $n$:

$$(a \cdot x_1^{n_1} \cdots x_k^{n_k})^n = a^n \cdot x_1^{n_1 \cdot n} \cdots x_k^{n_k \cdot n}$$

For example:

$$(3x^3)^2 = 3^2 \cdot x^{3 \cdot 2} = 9x^6$$

The same rule extends to monomials in multiple variables:

$$(2x^2y^3)^3 = 2^3 \cdot x^{2 \cdot 3} \cdot y^{3 \cdot 3} = 8x^6y^9$$

When $n = 0$, any non-zero monomial raised to the zeroth power equals $1$, since $a^0 = 1$ and $x_i^{0} = 1$ for all $i$.


## GCD and LCM of monomials

The greatest common divisor (GCD) of two or more monomials is defined as the monomial with the largest coefficient that divides all given coefficients and the smallest exponent for each variable present in all monomials. In contrast, the least common multiple (LCM) is the monomial with the smallest coefficient divisible by all given coefficients and the largest exponent for each variable present in any of the monomials.

For example, consider the monomials $12x^3y^2$ and $8x^2y^4$. The GCD of the coefficients is $\gcd(12, 8) = 4$. For each variable, the minimum exponent is selected: $\min(3,2) = 2$ for $x$ and $\min(2,4) = 2$ for $y$. Therefore, the GCD is:

$$\gcd(12x^3y^2, 8x^2y^4) = 4x^2y^2$$

For the LCM, the least common multiple of the coefficients is $\text{lcm}(12, 8) = 24$. For each variable, the maximum exponent is selected: $\max(3,2) = 3$ for $x$ and $\max(2,4) = 4$ for $y$. Therefore, the LCM is:

$$\text{lcm}(12x^3y^2, 8x^2y^4) = 24x^3y^4$$

A variable that appears in only one of the monomials is included in the LCM with its full exponent, but is excluded from the GCD.
