# Adding and Subtracting Polynomials

Source: algebrica.org — CC BY-NC 4.0

## Definition and basic properties

Let \\( R \\) be a commutative [ring](../rings) and \\( R[x] \\) the ring of polynomials in one indeterminate over \\( R \\). Consider two [polynomials](../polynomials/) \\( P(x) \\) and \\( Q(x) \\), where any missing coefficients are understood to be zero:

\\[
P(x) = \sum_{k=0}^{n} a_k x^k
\\]

\\[
Q(x) = \sum_{k=0}^{m} b_k x^k
\\]

Addition is performed by summing the coefficients of terms of equal degree:

\\[
P(x) + Q(x) = \sum_{k=0}^{\max(n,m)} (a_k + b_k)\\, x^k
\\]

This operation is the Cauchy sum of the coefficient sequences of \\( P \\) and \\( Q \\), which ensures that polynomial addition is well-defined and independent of the representation chosen for each polynomial. The result is again a polynomial, and \\( R[x] \\) forms an abelian group under addition.

> An abelian group is a set equipped with a binary operation that is commutative, associative, admits a neutral element, and assigns an inverse to every element. The pair \\( (R[x], +) \\) satisfies all four conditions, with the zero polynomial as neutral element and \\( -P(x) \\) as the inverse of \\( P(x) \\).

Subtraction is defined analogously, with each coefficient \\( b_k \\) replaced by \\( -b_k \\):

\\[
P(x) - Q(x) = \sum_{k=0}^{\max(n,m)} (a_k - b_k)\\, x^k
\\]

The degree of the result depends on whether the leading terms cancel. Denoting \\( \deg P = n \\) and \\( \deg Q = m \\), the general bound is:

\\[
\deg\bigl(P(x) \pm Q(x)\bigr) \leq \max\\{n,\\, m\\}
\\]

If \\( n \neq m \\), the leading term of the polynomial of higher degree has no counterpart to cancel against, and the degree of the result is exactly \\( \max\\{n,\\, m\\} \\). When \\( n = m \\), the degree may decrease: under addition, the leading term cancels whenever \\( a_n + b_n = 0 \\); under subtraction, whenever \\( a_n = b_n \\). If every term cancels, the result is the zero polynomial, to which the deg

- - -

## Addition and subtraction term by term

The summation form introduced above admits a concrete computational counterpart, in which the two polynomials are written in standard form and the coefficients of terms of equal degree are combined directly. This is the procedure used in practice whenever a sum or difference must be evaluated by hand.

Given two polynomials \\( P(x) \\) and \\( Q(x) \\), the sum is obtained in three steps: arrange both polynomials in decreasing order of degree, align the terms of equal degree, and add the corresponding coefficients. Missing terms are treated as having coefficient zero, so that every degree from \\( 0 \\) up to \\( \max\\{\deg P,\\, \deg Q\\} \\) is represented. Consider the following polynomials:

\\[ P(x) = 4x^3 + 2x - 7 \\]

\\[ Q(x) = x^3 - 5x^2 + 3 \\]

The polynomial \\( P(x) \\) contains no degree-2 term and \\( Q(x) \\) contains no degree-1 term. The aligned form makes the missing coefficients explicit:

\\[
\begin{align}
P(x) &= 4x^3 + 0\\,x^2 + 2x - 7 \\\\[6pt]
Q(x) &= x^3 - 5x^2 + 0\\,x + 3
\end{align}
\\]

The sum is then computed by adding the coefficients column by column:

\\[
\begin{align}
P(x) + Q(x)
  &= (4+1)\\,x^3 + (0-5)\\,x^2 + (2+0)\\,x + (-7+3) \\\\[6pt]
  &= 5x^3 - 5x^2 + 2x - 4
\end{align}
\\]

Subtraction follows the same procedure, with the coefficients of \\( Q(x) \\) replaced by their opposites before the column-wise combination. Equivalently, one may write \\( P(x) - Q(x) = P(x) + (-Q(x)) \\) and apply the addition rule. The difference of the two polynomials above is:

\\[
\begin{align}
P(x) - Q(x)
  &= (4-1)\\,x^3 + (0+5)\\,x^2 + (2-0)\\,x + (-7-3) \\\\[6pt]
  &= 3x^3 + 5x^2 + 2x - 10
\end{align}
\\]

> The columnar layout is not a separate definition but a notational convenience. It corresponds exactly to the summation form \\( \sum (a_k \pm b_k)\\, x^k \\), with the convention that any coefficient absent from the standard form of a polynomial is taken to be zero.

- - -

## Properties of polynomial addition and subtraction

Polynomial addition inherits its structural properties directly from the addition of the underlying ring \\( R \\). Since the sum is defined coefficient by coefficient, every property that holds for \\( + \\) in \\( R \\) transfers to \\( + \\) in \\( R[x] \\). The four properties below characterize \\( (R[x], +) \\) as an abelian [group](../groups/). The first property is commutativity. For every pair of polynomials \\( P(x) \\) and \\( Q(x):\\)

\\[
P(x) + Q(x) = Q(x) + P(x)
\\]

The second property is associativity. For every triple \\( P(x) \\), \\( Q(x) \\), \\( R(x) \\):

\\[
\bigl(P(x) + Q(x)\bigr) + R(x) = P(x) + \bigl(Q(x) + R(x)\bigr)
\\]

The third property is the existence of a neutral element. The zero polynomial, denoted \\( 0 \\), satisfies:

\\[
P(x) + 0 = P(x)
\\]

The fourth property is the existence of an additive inverse. For every polynomial \\( P(x) = \sum_{k=0}^{n} a_k x^k \\), the polynomial obtained by negating each coefficient,

\\[
-P(x) = \sum_{k=0}^{n} (-a_k)\\, x^k
\\]

satisfies \\( P(x) + \bigl(-P(x)\bigr) = 0 \\). Subtraction is then defined as addition of the additive inverse:

\\[
P(x) - Q(x) = P(x) + \bigl(-Q(x)\bigr)
\\]

This definition makes subtraction a derived operation rather than a primitive one. As a consequence, subtraction is neither commutative nor associative: in general \\( P(x) - Q(x) \neq Q(x) - P(x) \\), and \\( \bigl(P(x) - Q(x)\bigr) - R(x) \neq P(x) - \bigl(Q(x) - R(x)\bigr) \\).

A further property concerns the interaction with multiplication. Polynomial multiplication distributes over addition, both on the left and on the right:

\\[
\begin{align}
P(x) \cdot \bigl(Q(x) + R(x)\bigr) &= P(x)\,Q(x) + P(x)\,R(x) \\\\[6pt]
\bigl(P(x) + Q(x)\bigr) \cdot R(x) &= P(x)\,R(x) + Q(x)\,R(x)
\end{align}
\\]

Together with the abelian group structure of \\( (R[x], +) \\), distributivity is what makes \\( R[x] \\) a ring. When \\( R \\) is commutative, \\( R[x] \\) is also commutative, and the two distributive laws coincide.

- - -

## Polynomials in several indeterminates

The construction extends naturally to polynomials in more than one indeterminate. Let \\( R \\) be a commutative ring and \\( R[x_1, \dots, x_n] \\) the ring of polynomials in \\( n \\) indeterminates over \\( R \\). A polynomial in this ring is a finite sum of monomials of the form:

\\[
a_{\alpha}\\, x_1^{\alpha_1} x_2^{\alpha_2} \cdots x_n^{\alpha_n}
\\]

The exponent vector \\( \alpha = (\alpha_1, \dots, \alpha_n) \\) is a multi-index of non-negative integers, and \\( a_{\alpha} \in R \\) is the coefficient associated with that multi-index. Using multi-index notation, a polynomial \\( P(x_1, \dots, x_n) \\) is written compactly as:

\\[
P(x_1, \dots, x_n) = \sum_{\alpha} a_{\alpha}\\, x^{\alpha}
\\]

The sum runs over a finite set of multi-indices, and \\( x^{\alpha} \\) denotes the monomial \\( x_1^{\alpha_1} \cdots x_n^{\alpha_n} \\).

Addition is defined by combining the coefficients of monomials with the same multi-index. Given two polynomials,

\\[
P(x_1, \dots, x_n) = \sum_{\alpha} a_{\alpha}\\, x^{\alpha}
\\]

\\[
Q(x_1, \dots, x_n) = \sum_{\alpha} b_{\alpha}\\, x^{\alpha},
\\]

their sum is:

\\[
P + Q = \sum_{\alpha} (a_{\alpha} + b_{\alpha})\\, x^{\alpha}
\\]

Subtraction is defined analogously, with each coefficient \\( b_{\alpha} \\) replaced by \\( -b_{\alpha} \\). The procedure is identical to the univariate case: only the indexing changes, with multi-indices replacing single integer exponents.

> Two monomials are combined only when they have identical exponents in every indeterminate. The monomials \\( x_1^2 x_2 \\) and \\( x_1 x_2^2 \\) correspond to distinct multi-indices, \\( (2,1) \\) and \\( (1,2) \\), and are therefore not combined.

Consider the following polynomials in two indeterminates:

\\[ P(x, y) = 3x^2 y + 2xy - y^2 + 4 \\]

\\[ Q(x, y) = x^2 y - xy + 5y^2 - 1 \\]

Their sum is computed by combining the coefficients of monomials of equal multi-index:

\\[
\begin{align}
P(x, y) + Q(x, y)
  &= (3+1)\\, x^2 y + (2-1)\\, xy + (-1+5)\\, y^2 + (4-1) \\\\[6pt]
  &= 4x^2 y + xy + 4y^2 + 3
\end{align}
\\]

The structural properties carry over without modification: \\( (R[x_1, \dots, x_n], +) \\) is an abelian group, with the zero polynomial as neutral element and \\( -P \\) as the additive inverse of \\( P \\). The multivariate setting introduces no new algebraic phenomena for addition and subtraction; the only conceptual shift is the indexing of coefficients by multi-indices rather than by a single integer.

- - -

## Example 1

Consider the following polynomials of degree 2:

\\[ P(x) = x^2 + 3x - 1 \\]

\\[ Q(x) = 2x^2 - x + 5 \\]

Their sum is computed by adding the coefficients of terms of equal degree:

\\[
\begin{align}
P(x) + Q(x)
  &= (x^2 + 3x - 1) + (2x^2 - x + 5) \\\\[6pt]
  &= (1+2)\\,x^2 + (3-1)\\,x + (-1+5) \\\\[6pt]
  &= 3x^2 + 2x + 4
\end{align}
\\]

The leading coefficients satisfy \\( 1 + 2 = 3 \neq 0 \\), so the degree-2 term is preserved. The sum is the polynomial \\( 3x^2 + 2x + 4 \\), of degree 2.

- - -

## Example 2

Consider the following polynomials of degree 2:

\\[ P(x) = 2x^2 + 3x - 1 \\]

\\[ Q(x) = 2x^2 - x + 5 \\]

Their difference is computed by subtracting the coefficients of terms of equal degree:

\\[
\begin{align}
P(x) - Q(x)
  &= (2x^2 + 3x - 1) - (2x^2 - x + 5) \\\\[6pt]
  &= (2-2)\\,x^2 + (3+1)\\,x + (-1-5) \\\\[6pt]
  &= 4x - 6
\end{align}
\\]

The two polynomials share the same leading coefficient, so the degree-2 term cancels and the result has degree 1. This illustrates the strict case of the bound:

\\[ \deg(P - Q) < \max\\{\deg P,\\, \deg Q\\} \\]

The difference is the polynomial \\( 4x - 6 \\), of degree 1.

- - -

## Example 3

Consider the following polynomials of different degrees:

\\[ P(x) = x^2 + 3x - 1 \\]

\\[ Q(x) = 2x^4 - x + 5 \\]

Their sum is computed by aligning the coefficients of terms of equal degree:

\\[
\begin{align}
P(x) + Q(x)
  &= (x^2 + 3x - 1) + (2x^4 - x + 5) \\\\[6pt]
  &= 2x^4 + x^2 + (3-1)\\,x + (-1+5) \\\\[6pt]
  &= 2x^4 + x^2 + 2x + 4
\end{align}
\\]

Since the two polynomials have different degrees, the leading term of \\( Q(x) \\) has no counterpart in \\( P(x) \\) and is preserved in the result. The degree of the sum is therefore \\( \max\\{2,\\, 4\\} = 4 \\), and the result is the polynomial \\( 2x^4 + x^2 + 2x + 4 \\).

- - -

## Example 4

Consider the following polynomials of degree 3:

\\[ P(x) = 2x^3 - 4x^2 + x - 7 \\]

\\[ Q(x) = 2x^3 - 4x^2 + x - 7 \\]

The two polynomials are identical, so their difference is computed by subtracting each coefficient from itself:

\\[
\begin{align}
P(x) - Q(x)
  &= (2x^3 - 4x^2 + x - 7) - (2x^3 - 4x^2 + x - 7) \\\\[6pt]
  &= (2-2)\\, x^3 + (-4+4)\\, x^2 + (1-1)\\, x + (-7+7) \\\\[6pt]
  &= 0
\end{align}
\\]

Every coefficient cancels and the result is the zero polynomial. By the convention introduced earlier, the degree of the zero polynomial is \\( -\infty \\), so:

\\[ \deg\bigl(P(x) - Q(x)\bigr) = -\infty \\]

This is the extreme case of the bound \\( \deg(P - Q) \leq \max\\{\deg P,\\, \deg Q\\} \\), in which the difference loses every term and the inequality becomes vacuous on the right-hand side. The convention \\( \deg 0 = -\infty \\) ensures that the multiplicative identity \\( \deg(PQ) = \deg P + \deg Q \\) continues to hold without exception, since adding \\( -\infty \\) to any finite degree yields \\( -\infty \\).