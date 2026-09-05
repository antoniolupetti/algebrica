---
title: Integral of Rational Functions
source: https://algebrica.org/integral-of-rational-functions/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - arctangent
  - completing-the-square
  - indefinite-integral
  - integration
  - integration-by-substitution
  - linearity
  - logarithms
  - partial-fractions
  - polynomial-division
  - rational-functions
---

## How to approach integrals of rational functions

Recall that a [rational function](../rational-functions/) is a quotient of two [polynomials](../polynomials/), with $N(x)$ in the numerator and $D(x)$ in the denominator. Its [indefinite integral](../indefinite-integrals/) has the general form:

$$\int \frac{N(x)}{D(x)} \ dx \tag{1}$$

When integrating a rational function, we must first identify the [zeros](../roots-of-a-polynomial/) of $D(x)$ to determine where the integrand is defined.

Below, we examine several common cases of integrals of the form $(1)$ and show the most suitable method for each. These integrals are generally not especially difficult to evaluate, but recognising the right method at once takes considerable practice and allows us to avoid unnecessary steps and complete the calculation efficiently.

To choose a method, we begin by comparing the degrees of the two polynomials, aiming to reduce the quotient to a proper fraction, that is, one whose numerator has degree strictly less than that of the denominator.

If the original integrand is already a proper fraction, we can apply the methods described below directly.

If, however, the degree of the numerator is greater than or equal to that of the denominator, the fraction is improper. We can then use [polynomial division](../polynomial-division/) to obtain a quotient $Q(x)$ and a remainder $R(x)$ satisfying the identity:

$$N(x) = Q(x)D(x) + R(x)$$

The remainder is either zero or has degree strictly less than that of $D(x).$ At points where the denominator is nonzero, we can divide the identity by $D(x)$ and write:

$$\frac{N(x)}{D(x)} = Q(x) + \frac{R(x)}{D(x)}$$

Using $(1)$ and the [linearity of integration](../integration-strategies/), we can write:

$$\int \frac{N(x)}{D(x)} \ dx = \int Q(x) \ dx + \int \frac{R(x)}{D(x)} \ dx \tag{2}$$

If the remainder $R(x)$ is zero, we only need to integrate $Q(x),$ a straightforward term-by-term application of the power rule. If the remainder is nonzero, we must also integrate the fraction $R(x)/D(x).$ Polynomial division has made the numerator's degree smaller than the denominator's, giving us the proper fraction we were seeking.

To evaluate the second integral in $(2),$ recall that over the real numbers every nonconstant polynomial factors into [linear and irreducible quadratic factors](../unique-factorization-of-polynomials/), possibly repeated. This factorisation allows us to express the fraction as a sum of partial fractions, to which we can apply the integration formulas introduced in the following sections.

> Before starting polynomial division or factorisation, we should always check whether the numerator and denominator have common factors that can be cancelled, remembering to exclude the zeros of the original denominator, which lie outside the [integrand's domain](../determining-the-domain-of-a-function/).

- - -

We can illustrate the procedure with an example. We evaluate the following integral, whose integrand is an improper fraction:

$$\int \frac{x^3 + x + 1}{x^2 + 1} \ dx$$

The numerator has degree $3$ and the denominator has degree $2,$ so we use polynomial division to bring the integral into the form $(2).$ The quotient of the leading terms is $x^3/x^2 = x.$ Multiplying the denominator by $x$ gives $x^3 + x,$ and we can write:

$$x^3 + x + 1 = x(x^2 + 1) + 1$$

The quotient is $Q(x) = x$ and the remainder is $R(x) = 1.$ Dividing by $x^2 + 1$ gives:

$$\frac{x^3 + x + 1}{x^2 + 1} = x + \frac{1}{x^2 + 1}$$

We can therefore rewrite the original integral as:

$$
\begin{align}
\int \frac{x^3 + x + 1}{x^2 + 1} \ dx &= \int x \ dx + \int \frac{1}{x^2 + 1} \ dx \\[6pt]
  &= \frac{x^2}{2} + \arctan x + k
\end{align}
$$

The first term is straightforward to integrate by the power rule, while the second integrand is the [derivative of the arctangent](../arctangent-function/). We have thus found the antiderivatives on all of $\mathbb{R},$ since the denominator $x^2 + 1$ is always positive.

## When the denominator is linear

If a proper fraction has a denominator of degree one, its numerator must be constant. Denoting this constant by $c,$ we need to evaluate an integral of the form:

$$\int \frac{c}{ax + b} \ dx \tag{3}$$

The coefficients $a,$ $b$ and $c$ are real, with $a \neq 0.$ We can use [integration by substitution](../integration-by-substitution/) in this case. Setting $t = ax + b$ and $dt = a \ dx,$ we rewrite integral $(3)$ as:

$$
\begin{align}
\int \frac{c}{ax + b} \ dx &= \frac{c}{a} \int \frac{1}{t} \ dt \\[8pt]
  &= \frac{c}{a} \ln|t| + k \\[10pt]
  &= \frac{c}{a} \ln|ax + b| + k
\end{align}
$$

- - -

We apply the method just described to the following integral:

$$\int \frac{2}{6x + 1} \ dx$$

Set $t = 6x + 1.$ The derivative of $t$ with respect to $x$ is $6,$ so $dt = 6 \ dx$ and $dx = dt/6.$ Substitution gives:

$$
\begin{align}
\int \frac{2}{6x + 1} \ dx &= \frac{2}{6} \int \frac{1}{t} \ dt \\[8pt]
  &= \frac{1}{3} \ln|t| + k \\[10pt]
  &= \frac{1}{3} \ln|6x + 1| + k
\end{align}
$$

The calculation is quite simple because it always leads to a logarithmic antiderivative. Once we identify the right substitution, the rest follows directly.


## Partial fraction decomposition

We now consider denominators with several factors and use [partial fraction decomposition](../partial-fraction-decomposition/) to separate their contributions. Consider, for example, the integral:



$$\int \frac{7x + 5}{(x - 1)(3x + 2)} \ dx$$

When the factors are linear and distinct, each contributes a fraction with a constant numerator.

$$\frac{A}{x - 1} + \frac{B}{3x + 2}$$

We determine the coefficients $A$ and $B$ by requiring the sum to equal the original function:

$$\frac{7x + 5}{(x - 1)(3x + 2)} = \frac{A}{x - 1} + \frac{B}{3x + 2} \tag{4}$$

Carrying out the algebra gives:

$$7x + 5 = A(3x + 2) + B(x - 1)$$

Setting $x=1$ eliminates the term with coefficient $B$ and gives $A = 12/5.$ Setting $x = -2/3$ instead eliminates the term with coefficient $A$ and gives $B = -1/5.$ Substituting these values into $(4)$ gives:

$$\frac{7x + 5}{(x - 1)(3x + 2)} = \frac{12}{5(x - 1)} - \frac{1}{5(3x + 2)}$$

We can therefore rewrite the integral as:

$$
\begin{align}
\int \frac{7x + 5}{(x - 1)(3x + 2)} \ dx &= \frac{12}{5} \int \frac{1}{x - 1} \ dx - \frac{1}{5} \int \frac{1}{3x + 2} \ dx \\[6pt]
  &= \frac{12}{5} \ln|x - 1| - \frac{1}{15} \ln|3x + 2| + k
\end{align}
$$

The antiderivatives are therefore given by this difference of logarithmic terms on the [intervals](../intervals/) $(-\infty,-2/3),$ $(-2/3,1)$ and $(1,+\infty).$

## Repeated linear factors

We next consider a denominator containing a factor $(x - r)^k$ of multiplicity $k \geq 2.$ The decomposition must include a term for each power of the factor, from the first to the $k$th, giving the form:

$$\frac{A_1}{x - r} + \frac{A_2}{(x - r)^2} + \dots + \frac{A_k}{(x - r)^k}$$

The numerators are constants to be determined by the partial fraction method used above. With luck, some will be zero, simplifying the calculation. The first term, with denominator $x - r,$ has antiderivative $A_1\ln|x - r|.$ For the higher powers, we use the [power rule for integration](../power-function/), since the exponent in the integrand is $-j \neq -1.$ For each $j \geq 2,$ we have:

$$\int \frac{A_j}{(x - r)^j} \ dx = \frac{A_j}{1 - j}(x - r)^{1 - j} + k$$

We illustrate this with a worked example, evaluating the following integral:

$$\int \frac{3x + 1}{(x - 1)^2(x + 2)} \ dx \tag{5}$$

The factor $x - 1$ has multiplicity $2,$ while $x + 2$ occurs only once. We therefore write the decomposition:

$$\frac{3x + 1}{(x - 1)^2(x + 2)} = \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{x + 2}$$

Multiplying by the common denominator gives:

$$3x + 1 = A(x - 1)(x + 2) + B(x + 2) + C(x - 1)^2$$

At $x = 1,$ the first and third terms on the right vanish, so $4 = 3B$ and $B = 4/3.$ At $x = -2,$ only the term containing $C$ remains, so $-5 = 9C$ and $C = -5/9.$ To find $A,$ we can compare the coefficients of $x^2.$ The coefficient on the left is zero, while that on the right is $A + C.$ Hence $A + C = 0$ and $A = 5/9.$ The decomposition is therefore:

$$\frac{3x + 1}{(x - 1)^2(x + 2)} = \frac{5}{9(x - 1)} + \frac{4}{3(x - 1)^2} - \frac{5}{9(x + 2)}$$

We thus obtain:

$$
\begin{align}
\int \frac{3x + 1}{(x - 1)^2(x + 2)} \ dx &= \frac{5}{9} \int \frac{1}{x - 1} \ dx + \frac{4}{3} \int \frac{1}{(x - 1)^2} \ dx - \frac{5}{9} \int \frac{1}{x + 2} \ dx \\[6pt]
  &= \frac{5}{9} \ln|x - 1| - \frac{4}{3(x - 1)} - \frac{5}{9} \ln|x + 2| + k
\end{align}
$$

We have therefore obtained the antiderivatives on each of the intervals $(-\infty,-2),$ $(-2,1)$ and $(1,+\infty).$ These intervals exclude $x = -2$ and $x = 1,$ where the denominator in $(5)$ vanishes and the original integrand is undefined.

## Irreducible quadratic factors

The next case is slightly more involved than the previous ones. Recall that a quadratic polynomial with a negative [discriminant](../quadratic-formula/) has no real roots and cannot be written as a product of real linear factors. The quadratic factor therefore remains intact in the denominator. To simplify the calculation, we divide the numerator and denominator by the coefficient of $x^2,$ so that the factor takes the form:

$$q(x) = x^2 + bx + c \qquad b^2 - 4c < 0$$

If this factor occurs only once, we associate with it a term of the form:

$$\frac{Ax + B}{q(x)}$$

The numerator has degree at most $1,$ so it may also be constant or zero. To integrate this fraction, we compare the numerator with the derivative $q'(x) = 2x + b.$ We then write the numerator as a multiple of this derivative plus a constant:

$$Ax + B = \frac{A}{2}(2x + b) + \left(B - \frac{Ab}{2}\right)$$

The integral therefore splits into two parts:

$$\int \frac{Ax + B}{q(x)} \ dx = \frac{A}{2} \int \frac{q'(x)}{q(x)} \ dx + \left(B - \frac{Ab}{2}\right) \int \frac{1}{q(x)} \ dx$$

The first part gives a [logarithm](../logarithmic-function/) through the substitution $v = q(x).$ For the second, we [complete the square](../completing-the-square/):

$$q(x) = \left(x + \frac{b}{2}\right)^2 + c - \frac{b^2}{4}$$

The negative discriminant implies $c - b^2/4 > 0.$ We therefore set $\rho = \sqrt{c - b^2/4} > 0$ and $u = x + b/2.$ Since $du = dx,$ the second integral becomes:

$$\int \frac{1}{q(x)} \ dx = \int \frac{1}{u^2 + \rho^2} \ du$$

With the further substitution $t = u/\rho,$ we have $du = \rho \ dt$ and recognise the derivative of the [arctangent](../arctangent-and-arccotangent/):

$$
\begin{align}
\int \frac{1}{u^2 + \rho^2} \ du &= \frac{1}{\rho} \int \frac{1}{1 + t^2} \ dt \\[6pt]
  &= \frac{1}{\rho} \arctan t + k \\[6pt]
  &= \frac{1}{\rho} \arctan\left(\frac{u}{\rho}\right) + k
\end{align}
$$

Combining the two contributions gives the formula:

$$\int \frac{Ax + B}{q(x)} \ dx = \frac{A}{2}\ln q(x) + \frac{B - Ab/2}{\rho}\arctan\left(\frac{x + b/2}{\rho}\right) + k$$

The formula therefore allows us to evaluate the integral by expressing the antiderivative in terms of a logarithm and an arctangent. To apply it, we identify the coefficients $A,$ $B,$ $b$ and $c,$ calculate $\rho = \sqrt{c - b^2/4}$ and substitute these values into the expression obtained.

- - -

A worked example will help clarify the steps and the substitutions involved. We evaluate the following integral:

$$\int \frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} \ dx$$

The denominator contains the linear factor $x + 1$ and the quadratic factor $x^2 + 2x + 3.$ The discriminant of the latter is $2^2 - 4 \cdot 3 = -8,$ so the factor is irreducible over the reals. We set up the decomposition:

$$\frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} = \frac{A}{x + 1} + \frac{Bx + C}{x^2 + 2x + 3}$$

Multiplying by the common denominator gives the identity:

$$5x^2 + 3x - 2 = A(x^2 + 2x + 3) + (Bx + C)(x + 1)$$

At $x = -1,$ the left-hand side is $5 - 3 - 2 = 0$ and the right-hand side reduces to $2A.$ Hence $A = 0.$ Expanding the remaining product gives:

$$5x^2 + 3x - 2 = Bx^2 + (B + C)x + C$$

Comparing the coefficients of $x^2$ and the constant terms gives $B = 5$ and $C = -2.$ The coefficients of $x$ also agree, since $B + C = 3.$ For $x \neq -1,$ the fraction therefore reduces to:

$$\frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} = \frac{5x - 2}{x^2 + 2x + 3}$$

The derivative of the new denominator is $2x + 2.$ To obtain this term in the numerator, we write:

$$5x - 2 = \frac{5}{2}(2x + 2) - 7$$

Separating the contributions, we can rewrite the original integral as:

$$\int \frac{5x - 2}{x^2 + 2x + 3} \ dx = \frac{5}{2} \int \frac{2x + 2}{x^2 + 2x + 3} \ dx - 7 \int \frac{1}{x^2 + 2x + 3} \ dx$$

In the first integral, the numerator is the derivative of the denominator, giving $(5/2)\ln(x^2 + 2x + 3).$ The denominator is positive because $x^2 + 2x + 3 = (x + 1)^2 + 2.$ This same identity allows us to evaluate the second integral by setting $u = x + 1$ and using the arctangent formula with $\rho = \sqrt{2}:$

$$-7 \int \frac{1}{(x + 1)^2 + 2} \ dx = -\frac{7}{\sqrt{2}}\arctan\left(\frac{x + 1}{\sqrt{2}}\right) + k$$

Combining the results gives:

$$\int \frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} \ dx = \frac{5}{2}\ln(x^2 + 2x + 3) - \frac{7}{\sqrt{2}}\arctan\left(\frac{x + 1}{\sqrt{2}}\right) + k$$

The procedure is a little more involved than in the previous cases, but do not be discouraged. By keeping the desired final form in mind and systematically making the appropriate substitutions, you will find these integrals fairly straightforward to evaluate with practice.

## Repeated irreducible quadratic factors

Our final case is more involved still and concerns integrals whose denominator contains a power $q(x)^k$ of an irreducible quadratic factor. Here we must include every power from $1$ to $k,$ just as we did for repeated linear factors. With $q(x) = x^2 + bx + c$ and $b^2 - 4c < 0,$ the corresponding part of the decomposition is:

$$\frac{A_1x + B_1}{q(x)} + \frac{A_2x + B_2}{q(x)^2} + \dots + \frac{A_kx + B_k}{q(x)^k}$$

Each numerator has degree at most $1.$ To integrate the term with index $j,$ we split the numerator as in the previous case:

$$A_jx + B_j = \frac{A_j}{2}q'(x) + \left(B_j - \frac{A_jb}{2}\right)$$

The part containing $q'(x)$ is integrated by the substitution $v = q(x).$ For $j = 1,$ we again obtain a logarithm. For $j \geq 2,$ we instead obtain:

$$\int \frac{q'(x)}{q(x)^j} \ dx = \int v^{-j} \ dv = \frac{q(x)^{1-j}}{1-j} + K$$

It remains to integrate the term with a constant numerator. Setting $u = x + b/2$ and $\rho = \sqrt{c - b^2/4} > 0$ as before, we reduce it to the family of integrals:

$$I_j = \int \frac{1}{(u^2 + \rho^2)^j} \ du$$

We have just considered the case $j = 1.$ For $j \geq 2,$ we can lower the exponent using a [reduction formula](../reduction-formulas/). To derive it, we start with the derivative:

$$
\begin{align}
\frac{d}{du}\left[\frac{u}{(u^2 + \rho^2)^{j-1}}\right] &= \frac{1}{(u^2 + \rho^2)^{j-1}} - \frac{2(j-1)u^2}{(u^2 + \rho^2)^j} \\[6pt]
  &= \frac{2(j-1)\rho^2}{(u^2 + \rho^2)^j} - \frac{2j-3}{(u^2 + \rho^2)^{j-1}}
\end{align}
$$

In the last step, we substituted $u^2 = (u^2 + \rho^2) - \rho^2$ and collected the terms with the same denominator. Integrating the identity and solving for $I_j$ gives:

$$I_j = \frac{u}{2(j-1)\rho^2(u^2 + \rho^2)^{j-1}} + \frac{2j-3}{2(j-1)\rho^2}I_{j-1} \qquad (j \geq 2)$$

Each application lowers the index by one, so after $j - 1$ steps we reach the form:

$$I_1 = \frac{1}{\rho}\arctan\left(\frac{u}{\rho}\right) + K$$

For example, when $j = 2,$ a single application of the formula gives:

$$I_2 = \frac{u}{2\rho^2(u^2 + \rho^2)} + \frac{1}{2\rho^3}\arctan\left(\frac{u}{\rho}\right) + k$$

This expression gives the antiderivatives of $1/(u^2 + \rho^2)^2$ on all of $\mathbb{R},$ since $\rho > 0$ and the denominator never vanishes.

These cases can be fairly laborious, especially when the quadratic factor has high multiplicity, since more coefficients must be determined and the reduction formula must be applied several times. We therefore restrict ourselves to the case $j = 2,$ which shows how to use the formula. A further example would repeat the decomposition and substitutions already illustrated, mainly adding algebraic steps without introducing any new integration techniques.