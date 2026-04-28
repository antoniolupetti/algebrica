# Partial Fraction Decomposition

Source: algebrica.org — CC BY-NC 4.0

## Introduction 

Partial fraction decomposition is a method that allows rewriting a [rational function](../rational-functions/) as a sum of fractions, based on the idea that when the denominator can be factored into its irreducible components, the original [function](../functions/) can be expressed as a combination of basic terms. Consider, for example, a rational function of the form:

\\[\frac{P(x)}{Q(x)}\\]

We have the following constraints:

+ \\(P(x)\\) and \\(Q(x)\\) are polynomials.
+ the degree of \\(P(x)\\) is strictly less than the degree of \\(Q(x)\\).

The procedure consists in factoring \\(Q(x)\\) and rewriting \\(P(x)/Q(x)\\) as a sum of fractions whose denominators are those factors. The result is a sum of elementary fractions, one term for each linear or irreducible quadratic factor of \\(Q(x)\\).

> The method is useful, for instance, when [integrating rational functions](../integral-of-rational-functions/): each partial fraction has a standard antiderivative.

- - -

## Example 1

To illustrate how the method works, consider the following rational function:
\\[
\frac{5x + 4}{(x - 2)(2x + 3)}
\\]
Both the numerator and the denominator are [polynomials](../polynomials/), and the degree of the numerator is strictly less than the degree of the denominator. Hence the expression is a proper rational function, and the conditions required for applying the partial fraction method are satisfied.

As a first step, we rewrite the function as a sum of two simpler terms, each having one of the linear factors of the denominator as its denominator. In other words, we seek constants \\(A\\) and \\(B\\) such that the expression can be written as
\\[
\frac{5x + 4}{(x - 2)(2x + 3)} = \frac{A}{x - 2} + \frac{B}{2x + 3} \tag{1}
\\]
At this point, our objective is to determine the constants \\(A\\) and \\(B\\) so that the identity above holds for all real values of \\(x\\). Multiplying both sides of equation \\((1)\\) by \\((x - 2)(2x + 3)\\) clears the denominators and yields the polynomial identity:
\\[
5x + 4 = A(2x + 3) + B(x - 2) \tag{2}
\\]
This relation must hold for every value of \\(x\\). The advantage of this transformation is that it converts the original rational expression into an equation involving only polynomials, allowing us to determine the unknown coefficients through direct algebraic comparison. To find \\(A\\) and \\(B\\), we apply a simple procedure known as the cover-up rule. The idea is to assign strategic values to \\(x\\) so as to eliminate one coefficient at a time: by choosing values that make one of the linear factors vanish, we remove the corresponding term from the equation and can solve directly for the remaining coefficient.

For example, by choosing \\(x = 2\\) we eliminate the term involving \\(B\\), since the factor \\((x - 2)\\) becomes zero. Substituting \\(x = 2\\) into identity \\((2)\\) we obtain:
\\[
5(2) + 4 = A(2 \cdot 2 + 3) + B(0)
\\]
This simplifies to:
\\[
14 = 7A
\\]
and therefore:
\\[
A = 2
\\]
To determine \\(B\\), we choose the value of \\(x\\) that makes the factor \\(2x + 3\\) vanish. Setting \\(x = -\dfrac{3}{2}\\) eliminates the term involving \\(A\\). Substituting this value into identity \\((2)\\) we obtain:
\\[
5\left(-\frac{3}{2}\right) + 4 = A(0) + B\left(-\frac{3}{2} - 2\right)
\\]
Simplifying each term gives:
\\[
-\frac{7}{2} = -\frac{7}{2}\\, B
\\]
and therefore:
\\[
B = 1
\\]

Substituting the values of \\(A\\) and \\(B\\) into equation \\((1)\\), the original rational function admits the partial fraction representation:

\\[
\frac{5x + 4}{(x - 2)(2x + 3)} = \frac{2}{x - 2} + \frac{1}{2x + 3}
\\]

- - -

## Application to the computation of integrals

As mentioned at the beginning, partial fraction decomposition is useful in practical settings, especially when [integrating rational functions](../integral-of-rational-functions/). Returning to the function from Example 1, consider the integral:

\\[
\int \frac{5x + 4}{(x - 2)(2x + 3)} \\, dx
\\]

In this form the expression is not straightforward to evaluate, but once the integrand is rewritten as a sum of simpler terms, however, we obtain:

\\[
\int \frac{5x + 4}{(x - 2)(2x + 3)} \\, dx = \int \left( \frac{2}{x - 2} + \frac{1}{2x + 3} \right) \\, dx
\\]

By the [linearity property](../indefinite-integrals/), the integral of a sum equals the sum of the integrals. Hence:

\\[
\int \frac{5x + 4}{(x - 2)(2x + 3)} \\, dx = 2 \int \frac{1}{x - 2} \\, dx + \int \frac{1}{2x + 3} \\, dx
\\]

Each term on the right-hand side can now be evaluated using standard [logarithmic](../logarithms/) formulas:

\\[
\int \frac{1}{x - 2} \\, dx = \ln|x - 2| + c_{1}
\\]

\\[
\int \frac{1}{2x + 3} \\, dx = \frac{1}{2} \ln|2x + 3| + c_{2}
\\]

Combining the results yields the antiderivative of the original rational function:

\\[
\int \frac{5x + 4}{(x - 2)(2x + 3)} \\, dx = 2 \ln|x - 2| + \frac{1}{2} \ln|2x + 3| + c
\\]

- - -

## General structure of partial fraction decomposition

The decomposition of a rational function into partial fractions is governed by a systematic rule that depends exclusively on the factorization of the denominator. Once the denominator is expressed as a product of linear and irreducible quadratic factors, possibly with multiplicity greater than one, the rational function admits a representation as a sum of elementary terms, each determined by one such factor.

To every linear factor of the form \\(x + a\\) corresponds a term:

\\[
\frac{A}{x + a}
\\]

If the factor occurs with multiplicity \\(k\\), the decomposition includes \\(k\\) terms, one for each power up to \\(k\\):

\\[
\frac{A_{1}}{x + a}
\+ \frac{A_{2}}{(x + a)^{2}}
\+ \cdots
\+ \frac{A_{k}}{(x + a)^{k}}
\\]

To every irreducible quadratic factor \\(x^{2} + ax + b\\) corresponds a term:

\\[
\frac{Bx + C}{x^{2} + ax + b}
\\]

The numerator is a linear polynomial because the denominator has degree two, and a proper fraction with such a denominator admits a numerator of degree at most one. If the quadratic factor is repeated \\(k\\) times, the decomposition contains the full sequence:

\\[
\frac{B_{1}x + C_{1}}{x^{2} + ax + b}
\+ \frac{B_{2}x + C_{2}}{(x^{2} + ax + b)^{2}}
\+ \cdots
\+ \frac{B_{k}x + C_{k}}{(x^{2} + ax + b)^{k}}
\\]

> Every rational function whose denominator factors over the real numbers admits a unique partial fraction representation, determined up to the values of the coefficients.

- - -

## Example 2

Let us now consider a more complicated example. We want to find the partial fraction decomposition of the rational function:

\\[
\frac{1}{x^{3} - 6x^{2} + 11x - 6}
\\]

Although the numerator is already as simple as possible, the denominator is a cubic polynomial, and its factorization will guide the entire decomposition process. Our first step is to factor the denominator into its irreducible components. Testing possible rational [roots](../roots-of-a-polynomial/), we find that \\(x = 1\\) satisfies:

\\[
1 - 6 + 11 - 6 = 0
\\]

so \\((x - 1)\\) is a factor. Dividing the polynomial by \\((x - 1)\\) using [synthetic division](../synthetic-division/) we have:

\\[
\begin{array}{r|rrrr}
1 & 1 & -6 & 11 & -6 \\\\[6pt]
  &   & 1 & -5 & 6 \\\\[6pt]
\hline
  & 1 & -5 & 6 & 0
\end{array}
\\]

In this way we obtain the quotient \\(x^{2} - 5x + 6\\), which further factorizes as:

\\[
x^{2} - 5x + 6 = (x - 2)(x - 3)
\\]

The complete factorization of the denominator is therefore:

\\[
x^{3} - 6x^{2} + 11x - 6 = (x - 1)(x - 2)(x - 3)
\\]

Since all factors are linear and distinct, the rational function admits the decomposition:

\\[
\frac{1}{(x - 1)(x - 2)(x - 3)} = \frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{x - 3}
\\]

To determine the constants \\(A\\), \\(B\\) and \\(C\\), we multiply both sides by the common denominator \\((x - 1)(x - 2)(x - 3)\\), obtaining the polynomial identity:

\\[
1 = A(x - 2)(x - 3) + B(x - 1)(x - 3) + C(x - 1)(x - 2)
\\]

This relation must hold for every real \\(x\\). By substituting values that annul each linear factor in turn, we eliminate two of the three terms at a time and solve directly for the remaining coefficient. Setting \\(x = 1\\) eliminates the contributions of \\(B\\) and \\(C\\), leaving:

\\[
1 = A(1 - 2)(1 - 3) = 2A
\\]

so that \\(A = \tfrac{1}{2}\\). Setting \\(x = 2\\) gives:

\\[
1 = B(2 - 1)(2 - 3) = -B
\\]

from which \\(B = -1\\). Finally, setting \\(x = 3\\) gives:

\\[
1 = C(3 - 1)(3 - 2) = 2C
\\]

and therefore \\(C = \tfrac{1}{2}\\).

Substituting the three values into the decomposition, the original rational function can be written as:

\\[
\frac{1}{x^{3} - 6x^{2} + 11x - 6} = \frac{1}{2(x - 1)} - \frac{1}{x - 2} + \frac{1}{2(x - 3)}
\\]

> This expresses the original rational function as a sum of elementary fractions, each associated with one of the linear factors of the denominator, and shows how the partial fraction method extends naturally to denominators of higher degree once they have been properly factorized.

- - -

## Example 3

Let us now consider a case in which one of the linear factors of the denominator appears with multiplicity greater than one. We want to find the partial fraction decomposition of the rational function:

\\[
\frac{2x + 3}{(x - 1)^{2}(x + 2)}
\\]

The denominator is already factored, but the factor \\((x - 1)\\) appears squared. According to the general rule, the decomposition must therefore include two distinct terms associated with this repeated factor, one for each power up to the multiplicity. We may write:

\\[
\frac{2x + 3}{(x - 1)^{2}(x + 2)} = \frac{A}{x - 1} + \frac{B}{(x - 1)^{2}} + \frac{C}{x + 2}
\\]

Multiplying both sides by the common denominator \\((x - 1)^{2}(x + 2)\\) yields the polynomial identity:

\\[
2x + 3 = A(x - 1)(x + 2) + B(x + 2) + C(x - 1)^{2} \tag{3}
\\]

This relation must hold for every real \\(x\\). To determine the three constants we now combine two complementary techniques. The cover-up rule allows us to compute \\(B\\) and \\(C\\) directly. Setting \\(x = 1\\) annuls both \\((x - 1)\\) and \\((x - 1)^{2}\\), eliminating the contributions of \\(A\\) and \\(C\\):

\\[
2(1) + 3 = B(1 + 2)
\\]

which gives \\(B = \tfrac{5}{3}\\). Setting \\(x = -2\\) annuls \\((x + 2)\\) and eliminates the contributions of \\(A\\) and \\(B\\):

\\[
2(-2) + 3 = C(-2 - 1)^{2}
\\]

which gives \\(C = -\tfrac{1}{9}\\). The constant \\(A\\), however, cannot be obtained in the same way: no real value of \\(x\\) annuls only the factors associated with \\(B\\) and \\(C\\) while leaving \\(A\\) isolated. To determine it we apply the method of comparison of coefficients, which consists in expanding the right-hand side of identity \\((3)\\) and matching the coefficients of equal powers of \\(x\\) with those of the left-hand side. Expanding the right-hand side gives:

\\[
\begin{align}
A(x - 1)(x + 2) &= A x^{2} + A x - 2A \\\\[6pt]
B(x + 2) &= B x + 2B \\\\[6pt]
C(x - 1)^{2} &= C x^{2} - 2C x + C
\end{align}
\\]

Collecting terms by degree, the right-hand side of identity \\((3)\\) becomes:

\\[
(A + C)\, x^{2} + (A + B - 2C)\, x + (-2A + 2B + C)
\\]

Since the left-hand side is \\(2x + 3\\), the coefficient of \\(x^{2}\\) on the right-hand side must vanish, and we obtain the relation:

\\[
A + C = 0
\\]

Substituting the value \\(C = -\tfrac{1}{9}\\) found above gives \\(A = \tfrac{1}{9}\\).

Substituting the three constants into the decomposition, the original rational function admits the partial fraction representation:

\\[
\frac{2x + 3}{(x - 1)^{2}(x + 2)} = \frac{1}{9(x - 1)} + \frac{5}{3(x - 1)^{2}} - \frac{1}{9(x + 2)}
\\]

> This example shows that, when the denominator contains a repeated linear factor, the cover-up rule still determines the coefficients associated with the highest power of each factor, while the remaining coefficients are recovered by comparing the coefficients of the polynomial identity.

- - -

## Example 4

We now consider a case in which the denominator contains an irreducible quadratic factor. We want to find the partial fraction decomposition of the rational function:

\\[
\frac{3x + 1}{(x - 1)(x^{2} + 1)}
\\]

The factor \\(x^{2} + 1\\) has discriminant \\(\Delta = -4 < 0\\), so it has no real roots and cannot be factored further over the real numbers. According to the general rule, the term of the decomposition associated with this factor must therefore have a numerator of degree at most one. We may write:

\\[
\frac{3x + 1}{(x - 1)(x^{2} + 1)} = \frac{A}{x - 1} + \frac{Bx + C}{x^{2} + 1}
\\]

Multiplying both sides by the common denominator \\((x - 1)(x^{2} + 1)\\) yields the polynomial identity:

\\[
3x + 1 = A(x^{2} + 1) + (Bx + C)(x - 1) \tag{4}
\\]

This relation must hold for every real \\(x\\). The cover-up rule still allows us to determine the constant \\(A\\), since \\(x = 1\\) annuls the factor \\((x - 1)\\) and eliminates the contribution of \\(Bx + C\\). Substituting into identity \\((4)\\) gives:

\\[
3(1) + 1 = A(1^{2} + 1)
\\]

which simplifies to \\(4 = 2A\\), and therefore \\(A = 2\\).

To determine \\(B\\) and \\(C\\) we apply the method of comparison of coefficients, since no real value of \\(x\\) annuls the factor \\(x^{2} + 1\\). Expanding the right-hand side of identity \\((4)\\) gives:

\\[
\begin{align}
A(x^{2} + 1) &= A x^{2} + A \\\\[6pt]
(Bx + C)(x - 1) &= B x^{2} - B x + C x - C
\end{align}
\\]

Collecting terms by degree, the right-hand side becomes:

\\[
(A + B)\, x^{2} + (-B + C)\, x + (A - C)
\\]

Since the left-hand side of identity \\((4)\\) is \\(3x + 1\\), the coefficients of equal powers of \\(x\\) on both sides must match. This produces the system:

\\[
\begin{align}
A + B &= 0 \\\\[6pt]
-B + C &= 3 \\\\[6pt]
A - C &= 1
\end{align}
\\]

Substituting \\(A = 2\\) into the first equation gives \\(B = -2\\). Substituting \\(A = 2\\) into the third equation gives \\(C = 1\\). The second equation \\(-(-2) + 1 = 3\\) is automatically satisfied, confirming the consistency of the values found.

Substituting the three constants into the decomposition, the original rational function admits the partial fraction representation:

\\[
\frac{3x + 1}{(x - 1)(x^{2} + 1)} = \frac{2}{x - 1} + \frac{-2x + 1}{x^{2} + 1}
\\]

> This example shows how the partial fraction method handles an irreducible quadratic factor: the corresponding numerator is taken as a generic polynomial of degree one, and its coefficients are recovered by comparing the

- - -

## The case of improper rational functions

In the form presented above, the partial fraction method requires the rational function to be proper, that is, \\(\deg P(x) < \deg Q(x)\\). When this condition fails, the function is improper, and a preliminary step precedes the decomposition. The numerator is divided by the denominator via [polynomial division](../polynomial-division/), yielding a quotient \\(S(x)\\) and a remainder \\(R(x)\\). The rational function then rewrites as:

\\[
\frac{P(x)}{Q(x)} = S(x) + \frac{R(x)}{Q(x)}
\\]

with \\(\deg R(x) < \deg Q(x)\\). The first term is a polynomial and requires no further treatment; the second is a proper rational function, to which the partial fraction rules apply directly. Consider, for example:

\\[
\frac{x^{3} + 2x}{x^{2} - 1}
\\]

The numerator has degree three and the denominator degree two, so the function is improper. Polynomial division of \\(x^{3} + 2x\\) by \\(x^{2} - 1\\) yields quotient \\(x\\) and remainder \\(3x\\), giving:

\\[
\frac{x^{3} + 2x}{x^{2} - 1} = x + \frac{3x}{x^{2} - 1}
\\]

The polynomial part is now separated from the proper rational part, and the partial fraction method applies to the latter after factoring \\(x^{2} - 1 = (x - 1)(x + 1)\\).

> When the degree condition fails, the preliminary division is performed first; the partial fraction decomposition is then applied to the proper remainder, never to the original improper expression.