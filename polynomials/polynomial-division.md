# Polynomial Division

Source: algebrica.org — CC BY-NC 4.0

## The division algorithm

Let \\(P(x)\\) and \\(D(x)\\) be [polynomials](../polynomials/) in \\(\mathbb{R}[x]\\) with \\(D(x) \neq 0\\). The division algorithm asserts the existence of unique polynomials \\(Q(x)\\) and \\(R(x)\\) in \\(\mathbb{R}[x]\\) such that:

\\[
P(x) = Q(x) \cdot D(x) + R(x)
\\]

\\[
\deg R(x) < \deg D(x) \quad \text{or} \quad R(x) = 0
\\]

- The polynomial \\(P(x)\\) is referred to as the dividend.
- \\(D(x)\\) as the divisor.
- \\(Q(x)\\) as the quotient.
- \\(R(x)\\) as the remainder.

If \\(R(x) = 0\\), the division is exact and \\(D(x)\\) divides \\(P(x)\\) in \\(\mathbb{R}[x]\\). This result is directly analogous to the Euclidean division of [integers](../integers/) and holds in any polynomial [ring](../rings/) \\(F[x]\\), where \\(F\\) is a [field](../fields/). The existence of such a representation can be established by induction on \\(\deg P\\), while uniqueness follows from a degree argument. Suppose that two representations exist:

\\[
\begin{align}
P(x) &= Q_1(x) \cdot D(x) + R_1(x) \\\\[6pt]
     &= Q_2(x) \cdot D(x) + R_2(x)
\end{align}
\\]

Subtracting yields \\((Q_1(x) - Q_2(x)) \cdot D(x) = R_2(x) - R_1(x)\\). If \\(Q_1 \neq Q_2\\), the left-hand side has degree at least \\(\deg D\\), whereas the right-hand side satisfies \\(\deg(R_2 - R_1) < \deg D\\), a contradiction. Therefore \\(Q_1 = Q_2\\), and consequently \\(R_1 = R_2\\).

> A ring is an algebraic structure with two operations, addition and multiplication, that satisfy associativity, distributivity, and the existence of additive inverses. A field is a ring in which every nonzero element possesses a multiplicative inverse. Common examples of fields are \\(\mathbb{Q}\\), \\(\mathbb{R}\\), and \\(\mathbb{C}.\\)

- - -

Let \\(P(x)\\) and \\(D(x)\\) be nonzero polynomials such that \\(\deg P \geq \deg D\\). The degrees of the quotient and remainder are as follows:

\\[
\deg Q(x) = \deg P(x) - \deg D(x)
\\]

\\[
\deg R(x) < \deg D(x)
\\]

If \\(\deg P < \deg D\\), then the quotient is the zero polynomial and the remainder is \\(P(x)\\).

- - -
## Properties of polynomial division

The division algorithm gives rise to several properties that follow directly from the uniqueness of the quotient and the remainder, or from the behaviour of the degree under polynomial operations.

The quotient and the remainder are uniquely determined by the dividend and the divisor. Given \\(P(x)\\) and \\(D(x)\\) with \\(D(x) \neq 0\\) there exists one pair \\((Q(x), R(x))\\) satisfying the division identity \\(P(x) = Q(x) D(x) + R(x)\\) with \\(\deg R < \deg D\\) or \\(R = 0\\). The degree of the quotient is determined by the degrees of the dividend and the divisor:

\\[\deg Q(x) = \deg P(x) - \deg D(x)\\]
\\[\deg P \geq \deg D\\]

When \\(\deg P < \deg D\\), the algorithm produces \\(Q(x) = 0\\) and \\(R(x) = P(x)\\). The degree of the remainder is always strictly less than the degree of the divisor, regardless of the dividend.

Polynomial division is linear in the dividend. Given two polynomials \\(P_1(x)\\) and \\(P_2(x)\\), and constants \\(\alpha, \beta \in \mathbb{R}\\), the division of \\(\alpha P_1(x) + \beta P_2(x)\\) by \\(D(x)\\) yields:

\\[
\alpha P_1(x) + \beta P_2(x) = \big(\alpha Q_1(x) + \beta Q_2(x)\big) D(x) + \big(\alpha R_1(x) + \beta R_2(x)\big)
\\]

where \\(Q_i\\) and \\(R_i\\) are the quotient and the remainder of dividing \\(P_i\\) by \\(D\\). The linearity reduces the division of a sum of polynomials to the division of each term separately.

The division is invariant under multiplication of the divisor by a nonzero constant. Given \\(\lambda \in \mathbb{R}\\) with \\(\lambda \neq 0\\), dividing \\(P(x)\\) by \\(\lambda D(x)\\) produces the quotient \\(Q(x)/\lambda\\) and the same remainder \\(R(x)\\). The relation \\(P(x) = Q(x) D(x) + R(x)\\) is therefore unaffected by rescaling the divisor, up to a corresponding rescaling of the quotient.

> The polynomial [ring](../rings/) \\(\mathbb{R}[x]\\), equipped with the division algorithm, is an example of a Euclidean ring. The degree function plays the role of the Euclidean valuation, and the existence of a division with remainder satisfying \\(\deg R < \deg D\\) is precisely what characterises Euclidean structure in the polynomial setting.

- - -
## Polynomial long division

The long division algorithm involves repeatedly dividing the leading term of the current remainder by the leading term of \\(D(x)\\), subtracting the resulting product, and continuing this process until the degree of the remainder is less than that of \\(D(x)\\). The procedure can be summarized in the following steps:

- Divide the leading term of the current dividend by the leading term of \\(D(x)\\) to determine the next term of \\(Q(x)\\).
- Multiply this term by \\(D(x)\\) and subtract the result from the current dividend.
- Repeat these steps until the degree of the remaining expression is strictly less than \\(\deg D(x)\\).

> When the divisor is a linear polynomial of the form \\(x - c\\), the procedure can be carried out more efficiently using the [synthetic division method](../synthetic-division/), which reduces the computation to operations on coefficients alone.

- - -
## Example 1

Consider the polynomials \\(P(x) = x^3 + 2x^2 - x - 2\\) and \\(D(x) = x - 1\\). The method outlined above is applied to compute the quotient and the remainder of \\(P(x)\\) divided by \\(D(x)\\):

\\[
P(x) = x^3 + 2x^2 - x - 2
\\]

\\[
D(x) = x - 1
\\]

The division table is constructed with terms arranged in descending order of degree:

\\[
\begin{array}{rrrr|rr}
+x^3 & +2x^2 & -x & -2 & +x & -1 \\\\
\\\\
\end{array}
\\]

Dividing the leading term \\(x^3\\) by \\(x\\) yields \\(x^2\\). Multiplying \\(x^2\\) by \\(D(x) = x - 1\\) and subtracting the result gives:

\\[
\begin{array}{rrrr|rr}
+x^3 & +2x^2 & -x & -2 & +x & -1 \\\\
-x^3 & +x^2 &     &    & x^2 &    \\\\
\text{//} & +3x^2 & -x & -2 & &
\end{array}
\\]

Dividing \\(3x^2\\) by \\(x\\) yields \\(3x\\). Multiplying and subtracting as before produces:

\\[
\begin{array}{rrrr|rr}
+x^3 & +2x^2 & -x & -2 & +x & -1 \\\\
-x^3 & +x^2 &     &    & x^2 & +3x \\\\
\text{//} & +3x^2 & -x & -2 & & \\\\
     & -3x^2 & +3x &    & & \\\\
\text{//} & \text{//} & +2x & -2 & &
\end{array}
\\]

Dividing \\(2x\\) by \\(x\\) yields \\(2\\). Multiplying and subtracting completes the process:

\\[
\begin{array}{rrrr|rr}
+x^3 & +2x^2 & -x & -2 & +x & -1 \\\\
-x^3 & +x^2 &     &    & x^2 & +3x+2 \\\\
\text{//} & +3x^2 & -x & -2 & & \\\\
     & -3x^2 & +3x &    & & \\\\
\text{//} & \text{//} & +2x & -2 & & \\\\
     &      & -2x & +2 & & \\\\
     &      & \text{//} & 0 & &
\end{array}
\\]

The remainder is zero, so the division is exact. The quotient and the remainder are:

\\[
Q(x) = x^2 + 3x + 2 \qquad R(x) = 0
\\]

The factorization of \\(P(x)\\) is therefore:

\\[
x^3 + 2x^2 - x - 2 = (x^2 + 3x + 2)(x - 1)
\\]

- - -

## Example 2

The following example illustrates a case where the division is not exact: the remainder \\(R(x)\\) is a nonzero polynomial whose degree is strictly less than \\(\deg D(x)\\). Consider the polynomials:

\\[
P(x) = x^3 + x^2 + x + 2
\\]

\\[
D(x) = x^2 + 1
\\]

The division table is constructed with terms arranged in descending order of degree:

\\[
\begin{array}{rrrr|rr}
+x^3 & +x^2 & +x & +2 & +x^2 & +1 \\\\
\\\\
\end{array}
\\]

Dividing \\(x^3\\) by \\(x^2\\) yields \\(x\\). Multiplying \\(x\\) by \\(D(x)\\) and subtracting the result produces:

\\[
\begin{array}{rrrr|rr}
\+x^3 & +x^2 & +x & +2 & +x^2 & +1 \\\\
\-x^3 &      & -x &    & +x   &    \\\\
\text{//} & +x^2 & \text{//} & +2 & &
\end{array}
\\]

Dividing \\(x^2\\) by \\(x^2\\) yields \\(1\\). Multiplying and subtracting gives:

\\[
\begin{array}{rrrr|rr}
\+x^3 & +x^2 & +x & +2 & +x^2 & +1 \\\\
\-x^3 &      & -x &    & +x   & +1 \\\\
\text{//} & +x^2 & \text{//} & +2 & & \\\\
     & -x^2 &           & -1 & & \\\\
     & \text{//} &      & +1 & &
\end{array}
\\]

The degree of the remainder \\(1\\) is \\(0\\), which is strictly less than \\(\deg D(x) = 2\\), so the algorithm terminates. The quotient and the remainder are:

\\[
Q(x) = x + 1 \qquad R(x) = 1
\\]

The division can therefore be written as:

\\[
x^3 + x^2 + x + 2 = (x + 1)(x^2 + 1) + 1
\\]

- - -

## The remainder theorem and the factor theorem

The division algorithm leads to a result that connects polynomial division with the evaluation of a polynomial at a specific point. The remainder theorem expresses \\(P\(c\)\\) as the remainder of dividing \\(P(x)\\) by the linear polynomial \\(x - c\\). Let \\(P(x) \in \mathbb{R}[x]\\) and \\(c \in \mathbb{R}\\). When \\(P(x)\\) is divided by \\(x - c\\), the remainder equals \\(P\(c\)\\).

Applying the division algorithm with divisor \\(D(x) = x - c\\), and observing that \\(\deg D = 1\\), the remainder \\(R(x)\\) must satisfy \\(\deg R < 1\\), so that \\(R(x)\\) is a constant, denoted \\(r\\). The division algorithm yields:

\\[
P(x) = Q(x)(x - c) + r
\\]

Substituting \\(x = c\\) into both sides gives:

\\[
P\(c\) = Q\(c\)(c - c) + r = 0 + r = r
\\]

The identity \\(r = P\(c\)\\) establishes the result.

> The remainder theorem offers a direct method for evaluating a polynomial at a specific point without performing the complete division. The value \\(P\(c\)\\) is given by the remainder when dividing by \\(x - c\\).

- - -

The factor theorem is a direct consequence of the remainder theorem. Let \\(P(x) \in \mathbb{R}[x]\\) and \\(c \in \mathbb{R}\\). The polynomial \\(x - c\\) divides \\(P(x)\\) in \\(\mathbb{R}[x]\\) if and only if \\(P\(c\) = 0\\).

The proof follows directly from the remainder theorem. Dividing \\(P(x)\\) by \\(x - c\\) gives \\(P(x) = Q(x)(x - c) + r\\), where \\(r = P\(c\)\\). The polynomial \\(x - c\\) divides \\(P(x)\\) if and only if \\(r = 0\\), which is equivalent to \\(P\(c\) = 0.\\)

The factor theorem establishes a correspondence between the [roots](../roots-of-a-polynomial/) of a polynomial and its linear factors: \\(c\\) is a root of \\(P(x)\\) if and only if \\(x - c\\) is a factor of \\(P(x)\\) in \\(\mathbb{R}[x]\\).

> This principle underlies the factorization of polynomials over a field and will be explored further in the section on [polynomial factorization](../polynomials/).

- - -

## Example 3

As an application of the remainder theorem, consider the polynomial:

\\[
P(x) = 2x^3 - 3x^2 + x - 5
\\]

and the value \\(c = 2\\). According to the theorem, dividing \\(P(x)\\) by \\(x - 2\\) yields a remainder equal to \\(P(2)\\). Computing \\(P(2)\\) directly by substitution gives:

\\[
P(2) = 2(2)^3 - 3(2)^2 + (2) - 5 = 16 - 12 + 2 - 5 = 1
\\]

The remainder theorem predicts that the remainder of dividing \\(P(x)\\) by \\(x - 2\\) is \\(1\\). The result can be verified using the long division method:

\\[
\begin{array}{rrrr|rr}
\+2x^3 & -3x^2 & +x & -5 & +x & -2 \\\\
\\\\
\end{array}
\\]

Dividing the leading term \\(2x^3\\) by \\(x\\) yields \\(2x^2\\), which serves as the initial term of the quotient. Multiplying \\(2x^2\\) by \\(D(x) = x - 2\\) and subtracting the result from the dividend produces:

\\[
\begin{array}{rrrr|rr}
\+2x^3 & -3x^2 & +x & -5 & +x & -2 \\\\
\-2x^3 & +4x^2 &    &    & 2x^2 &    \\\\
\text{//} & +x^2 & +x & -5 & &
\end{array}
\\]

Dividing \\(x^2\\) by \\(x\\) yields \\(x\\). Multiplying and subtracting gives:

\\[
\begin{array}{rrrr|rr}
\+2x^3 & -3x^2 & +x & -5 & +x & -2 \\\\
\-2x^3 & +4x^2 &    &    & 2x^2 & +x \\\\
\text{//} & +x^2 & +x & -5 & & \\\\
      & -x^2 & +2x &    & & \\\\
\text{//} & \text{//} & +3x & -5 & &
\end{array}
\\]

Dividing \\(3x\\) by \\(x\\) yields \\(3\\). Multiplying and subtracting:

\\[
\begin{array}{rrrr|rr}
+2x^3 & -3x^2 & +x & -5 & +x & -2 \\\\
-2x^3 & +4x^2 &    &    & 2x^2 & +x+3 \\\\
\text{//} & +x^2 & +x & -5 & & \\\\
      & -x^2 & +2x &    & & \\\\
\text{//} & \text{//} & +3x & -5 & & \\\\
      &      & -3x & +6 & & \\\\
      &      & \text{//} & +1 & &
\end{array}
\\]

The remainder is \\(1\\), confirming that \\(R = P(2) = 1\\) in accordance with the remainder theorem. The quotient and the remainder are:

\\[
Q(x) = 2x^2 + x + 3 \qquad R = 1
\\]

The division can therefore be written as:

\\[
2x^3 - 3x^2 + x - 5 = (2x^2 + x + 3)(x - 2) + 1
\\]

- - -

## Rational functions and polynomial division

When the division of two polynomials is performed without separating the remainder, the result is represented as a [rational function](../rational-functions/) where \\(D(x) \neq 0\\):

\\[
F(x) = \frac{P(x)}{D(x)}
\\]

In this context, polynomial division provides a systematic method to decompose \\(F(x)\\) into a polynomial component and a proper rational component. A proper rational function is one in which the numerator has a strictly lower degree than the denominator:

\\[
\frac{P(x)}{D(x)} = Q(x) + \frac{R(x)}{D(x)}
\\]

The decomposition is unique: the polynomial part \\(Q(x)\\) and the proper rational part \\(R(x)/D(x)\\) are uniquely determined by \\(P(x)\\) and \\(D(x)\\), as a direct consequence of the uniqueness of the division algorithm.

The decomposition serves as the foundation for [partial fraction decomposition](../partial-fraction-decomposition/), a technique that expresses the proper rational component as a sum of simpler fractions. The method is widely used in integration.

- - -
## Polynomial division and the GCD

Polynomial division is the basic operation underlying the computation of the greatest common divisor of two polynomials. Given \\(P(x)\\) and \\(D(x)\\) in \\(\mathbb{R}[x]\\) with \\(D(x) \neq 0\\), the greatest common divisor \\(\gcd(P, D)\\) is defined as the polynomial of highest degree that divides both \\(P(x)\\) and \\(D(x)\\). The Euclidean algorithm for polynomials computes \\(\gcd(P, D)\\) through successive divisions, in direct analogy with the Euclidean algorithm for integers. The procedure rests on the following observation. Dividing \\(P(x)\\) by \\(D(x)\\) gives:

\\[
P(x) = Q(x) D(x) + R(x)
\\]

The common divisors of \\(P(x)\\) and \\(D(x)\\) coincide with the common divisors of \\(D(x)\\) and \\(R(x)\\). The identity \\(\gcd(P, D) = \gcd(D, R)\\) reduces the original problem to the computation of the GCD of two polynomials of strictly smaller degree. Iterating the construction produces a sequence of remainders of decreasing degree:

\\[
\begin{align}
P(x)     &= Q_1(x) D(x) + R_1(x) \\\\[6pt]
D(x)     &= Q_2(x) R_1(x) + R_2(x) \\\\[6pt]
R_1(x)   &= Q_3(x) R_2(x) + R_3(x) \\\\[6pt]
         &\\;\\;\vdots
\end{align}
\\]

The sequence terminates when a remainder \\(R_n(x) = 0\\) is reached. The last nonzero remainder \\(R_{n-1}(x)\\) is the greatest common divisor of \\(P(x)\\) and \\(D(x)\\), determined up to multiplication by a nonzero constant.

The Euclidean algorithm for polynomials provides a constructive method for testing whether two polynomials share a common factor, for simplifying rational expressions, and for verifying coprimality. Two polynomials \\(P(x)\\) and \\(D(x)\\) are coprime in \\(\mathbb{R}[x]\\) when \\(\gcd(P, D)\\) is a nonzero constant.

> The Euclidean algorithm extends to a stronger result known as Bézout's identity: given \\(P(x)\\) and \\(D(x)\\) in \\(\mathbb{R}[x]\\), there exist polynomials \\(A(x)\\) and \\(B(x)\\) such that \\(A(x) P(x) + B(x) D(x) = \gcd(P, D)\\). The polynomials \\(A(x)\\) and \\(B(x)\\) can be reconstructed by tracking the coefficients through the successive divisions of the algorithm.