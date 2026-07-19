---
title: Multiplying Polynomials
source: https://algebrica.org/multiplying-polynomials/
license: CC BY-NC 4.0
tags:
  - distributive-property
  - foil-method
  - multiplication-of-polynomials
  - notable-products
  - polynomial
  - polynomial-degree
  - polynomial-ring
---

## Definition and basic properties

**Definition 1.** Let $R$ be a commutative [ring](../rings/) and $R[x]$ the ring of [polynomials](../polynomials/) in one indeterminate over $R$. Consider two polynomials of degree $n$ and $m$ respectively:

$$
P(x) = \sum_{i=0}^{n} a_i x^i \qquad Q(x) = \sum_{j=0}^{m} b_j x^j
$$

The product $P(x) \cdot Q(x)$ is the polynomial whose coefficient of $x^k$ is obtained by summing the products $a_i b_j$ over all pairs $(i, j)$ such that $i + j = k$:

$$
(P \cdot Q)(x) = \sum_{k=0}^{n+m} \left( \sum_{i=0}^{k} a_i b_{k-i} \right) x^k
$$

This formula is the Cauchy convolution of the coefficient sequences. It defines the product independently of how zero coefficients beyond the degrees of $P$ and $Q$ are written.

The coefficient indexed by $k$ collects every contribution to the term of degree $k$ that arises from pairing a term of degree $i$ in $P$ with a term of degree $k - i$ in $Q$. 

The convention $a_i = 0$ for $i > n$ and $b_j = 0$ for $j > m$ extends the sums beyond the actual degree of each polynomial without altering the result.

> With [addition](../adding-and-subtracting-polynomials/) and this product, $R[x]$ is a ring. If $R$ is commutative with unity, so is $R[x]$. If $R$ is an integral domain, then $R[x]$ is also an integral domain.

- - -
The degree of the product satisfies the identity:

$$
\deg(P \cdot Q) = \deg P + \deg Q
$$

provided that neither factor is the zero polynomial. The identity holds in any integral domain because the leading coefficient of $P \cdot Q$ is the product $a_n b_m$, which is non-zero whenever $a_n$ and $b_m$ are. The convention $\deg 0 = -\infty$ extends the relation to the case in which one of the two factors vanishes, since $-\infty + k = -\infty$ for every finite $k$.

## Multiplication term by term

Computing the product in practice does not require the explicit double summation: the same result is obtained by repeated application of the distributive property, multiplying every term of one polynomial by every term of the other and collecting like terms.

Given $P(x) = a_n x^n + a_{n-1} x^{n-1} + \cdots + a_0$ and $Q(x) = b_m x^m + b_{m-1} x^{m-1} + \cdots + b_0$, the product expands as a finite sum of pairwise products of the form $a_i x^i \cdot b_j x^j = a_i b_j x^{i+j}$. The number of monomials produced in this raw form is $(n+1)(m+1)$; collecting terms of equal degree reduces them to at most $n + m + 1$ entries, one for each integer degree from $0$ to $n + m$.

The columnar layout that is convenient for the [sum and difference of polynomials](../adding-and-subtracting-polynomials/) extends to multiplication once the partial products are arranged by degree. Each term of $P$ generates a row of partial products with $Q$; the rows are then aligned by degree and summed column by column, exactly as for addition.

## Properties of polynomial multiplication

Polynomial multiplication inherits its structural properties from the multiplication of the underlying ring $R$. Since the product is defined coefficient by coefficient via convolution, every property that holds for the product in $R$ transfers to the product in $R[x]$. Four properties characterise the multiplicative behaviour of $(R[x], \cdot)$.

The first is associativity. For every triple of polynomials $P(x)$, $Q(x)$, $S(x)$:

$$
\bigl(P(x) \cdot Q(x)\bigr) \cdot S(x) = P(x) \cdot \bigl(Q(x) \cdot S(x)\bigr)
$$

The second is the existence of a multiplicative identity. The constant polynomial $1 \in R[x]$ satisfies:

$$
P(x) \cdot 1 = 1 \cdot P(x) = P(x)
$$

for every polynomial $P(x)$.

- - -
The third property is left and right distributivity over addition:

$$
\begin{align}
P(x) \cdot \bigl(Q(x) + S(x)\bigr) &= P(x) \cdot Q(x) + P(x) \cdot S(x) \\[6pt]
\bigl(P(x) + Q(x)\bigr) \cdot S(x) &= P(x) \cdot S(x) + Q(x) \cdot S(x)
\end{align}
$$

The fourth is commutativity, which holds whenever the underlying ring $R$ is commutative. For every pair of polynomials:

$$
P(x) \cdot Q(x) = Q(x) \cdot P(x)
$$

Together with the abelian group structure of $(R[x], +)$ discussed in the section on the [sum and difference of polynomials](../adding-and-subtracting-polynomials/), these four properties make $(R[x], +, \cdot)$ a commutative ring with unity.

> Unlike addition, polynomial multiplication is not defined by combining coefficients of equal degree. The contribution to the coefficient of $x^k$ comes instead from every pair of degrees $(i, j)$ with $i + j = k$, and this is precisely what distinguishes a product from a coefficient-wise operation.

## Example 1

Consider the following polynomials of degree $2$:

$$
P(x) = 2x^2 + 3x - 1
$$

$$
Q(x) = x^2 - 2x + 4
$$

The product is computed by distributing every term of $P(x)$ over $Q(x)$:

$$
\begin{align}
P(x) \cdot Q(x) &= 2x^2 (x^2 - 2x + 4) \\[6pt]
                &\quad + 3x (x^2 - 2x + 4) \\[6pt]
                &\quad + (-1)(x^2 - 2x + 4)
\end{align}
$$

Expanding each row gives:

$$
\begin{align}
2x^2 (x^2 - 2x + 4) &= 2x^4 - 4x^3 + 8x^2 \\[6pt]
3x (x^2 - 2x + 4)   &= 3x^3 - 6x^2 + 12x \\[6pt]
(-1)(x^2 - 2x + 4)  &= -x^2 + 2x - 4
\end{align}
$$

Aligning the partial products by degree and adding the coefficients column by column produces:

$$
\begin{align}
P(x) \cdot Q(x) &= 2x^4 + (-4 + 3)x^3 + (8 - 6 - 1)x^2 + (12 + 2)x + (-4) \\[6pt]
                &= 2x^4 - x^3 + x^2 + 14x - 4
\end{align}
$$

The degrees of $P(x)$ and $Q(x)$ are both equal to $2$, so the degree of the product is $4$, in agreement with the identity $\deg(P \cdot Q) = \deg P + \deg Q$.

## Example 2

When one of the factors is a [monomial](../monomials/), the multiplication reduces to a single application of the distributive property: each term of the other polynomial is multiplied by the monomial, and no collection of like terms is required, because the partial products have pairwise distinct degrees. Consider:

$$
P(x) = 3x^2
$$

$$
Q(x) = x^3 - 5x^2 + 2x - 7
$$

Multiplying each term of $Q(x)$ by $3x^2$ gives:

$$
\begin{align}
P(x) \cdot Q(x) &= 3x^2 \cdot x^3 + 3x^2 \cdot (-5x^2) + 3x^2 \cdot 2x + 3x^2 \cdot (-7) \\[6pt]
                &= 3x^5 - 15x^4 + 6x^3 - 21x^2
\end{align}
$$

The degree of the result is $5 = 2 + 3$, consistent with the general rule.

## Example 3

When the leading coefficients are opposites of one another, the term of highest degree cancels in some products and survives in others, depending on the sign of the constant by which each polynomial is multiplied. Consider the following polynomials:

$$
P(x) = x^2 + x + 1
$$

$$
Q(x) = x^2 - x + 1
$$

Distributing every term of $P(x)$ over $Q(x)$ produces:

$$
\begin{align}
P(x) \cdot Q(x) &= x^2(x^2 - x + 1) + x(x^2 - x + 1) + 1 \cdot (x^2 - x + 1) \\[6pt]
                &= (x^4 - x^3 + x^2) + (x^3 - x^2 + x) + (x^2 - x + 1) \\[6pt]
                &= x^4 + x^2 + 1
\end{align}
$$

The terms of intermediate degree cancel in pairs, leaving only $x^4$, $x^2$, and $1$. The resulting identity:

$$
(x^2 + x + 1)(x^2 - x + 1) = x^4 + x^2 + 1
$$

is one of the [notable products](../notable-products/) discussed on the dedicated page, where the factorisation of $x^4 + x^2 + 1$ is derived from the difference of two squares.

## Multiplying two binomials and the FOIL method

For two [binomials](../binomials/), the FOIL method is a compact form of the distributive law. Its name abbreviates First, Outer, Inner, Last. For a product of the form $(a+b)(c+d)$:

$$
(a + b)(c + d) = ac + ad + bc + bd
$$

the four monomials in the expansion correspond, in order, to the products of the first terms, the outer terms, the inner terms, and the last terms of the two binomials. The method is a mnemonic device for the systematic application of the distributive property to a product of two binomials. 

It does not extend to factors with more than two terms, where the general procedure of multiplying every term of one polynomial by every term of the other must be used instead. A dedicated treatment with worked examples appears in the entry on [binomials](../binomials/).

## Notable products

Several recurring polynomial identities are [notable products](../notable-products/), including the square and the cube of a binomial:

$$
(a + b)^2 = a^2 + 2ab + b^2
$$

$$
(a + b)^3 = a^3 + 3a^2 b + 3ab^2 + b^3
$$

and the difference of two squares:

$$
a^2 - b^2 = (a + b)(a - b)
$$

The [binomial theorem](../binomial-theorem/) is the general expansion of $(a+b)^n$ for a non-negative integer $n$. Its coefficients are the [binomial coefficients](../binomial-coefficient/). The dedicated page derives the formula from the distributive property and lists its standard special cases.

## Multiplying polynomials in several indeterminates

The definition of the product extends with no essential modification to polynomials in more than one indeterminate. 

**Definition 2.** Let $R[x_1, \dots, x_n]$ be the ring of polynomials in $n$ indeterminates over a commutative ring $R$. A polynomial in this ring is a finite sum of monomials of the form $a_{\alpha} x_1^{\alpha_1} \cdots x_n^{\alpha_n}$, indexed by multi-indices $\alpha = (\alpha_1, \dots, \alpha_n)$ of non-negative integers.

Given two such polynomials $P = \sum_{\alpha} a_{\alpha} x^{\alpha}$ and $Q = \sum_{\beta} b_{\beta} x^{\beta}$, the product is defined by:

$$
P \cdot Q = \sum_{\gamma} \left( \sum_{\alpha + \beta = \gamma} a_{\alpha} b_{\beta} \right) x^{\gamma}
$$

The sum over $\alpha + \beta = \gamma$ runs over all pairs of multi-indices that combine component by component to give $\gamma$. The construction reduces to the univariate case when $n = 1$ and shares with it the algebraic properties: associativity, commutativity (when $R$ is commutative), distributivity, and existence of the multiplicative identity. The total degree of the product equals the sum of the total degrees of the factors, with the same convention for the zero polynomial.

- - -
Consider, as a concrete example, the following polynomials in two indeterminates:

$$
P(x, y) = x + 2y
$$

$$
Q(x, y) = x^2 - xy + y^2
$$

Distributing each term of $P$ over $Q$ produces:

$$
\begin{align}
P(x, y) \cdot Q(x, y) &= x(x^2 - xy + y^2) + 2y(x^2 - xy + y^2) \\[6pt]
                      &= x^3 - x^2 y + x y^2 + 2x^2 y - 2x y^2 + 2 y^3 \\[6pt]
                      &= x^3 + x^2 y - x y^2 + 2 y^3
\end{align}
$$

The total degree of $P$ is $1$ and that of $Q$ is $2$, so the total degree of the product is $3$, as expected.

## Multiplication and factorisation

The inverse problem for polynomial multiplication is [factorisation](../unique-factorization-of-polynomials/). Given a polynomial $P(x)$, the goal is to identify polynomials $P_1(x), \dots, P_k(x)$ of lower degree whose product equals $P(x)$. Multiplication and factorisation are linked by the [polynomial division algorithm](../polynomial-division/), which determines, for any pair of polynomials $P(x)$ and $D(x)$ with $D(x) \neq 0$, a unique quotient $Q(x)$ and remainder $R(x)$ such that:

$$
P(x) = Q(x) \cdot D(x) + R(x) \qquad \deg R < \deg D
$$

When the remainder vanishes, the factorisation $P=QD$ is exact, and $D$ is a factor of $P$. Concrete factorisation methods combine multiplication, division, and information about the [roots](../roots-of-a-polynomial/) of $P$. The related pages treat the [AC method](../factoring-polynomials-ac-method/), [completing the square](../completing-the-square/), and [synthetic division](../synthetic-division/).
