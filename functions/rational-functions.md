---
title: Rational Functions
source: https://algebrica.org/rational-functions/
license: CC BY-NC 4.0
tags:
  - functions
  - limits
  - polynomials
  - rational-functions
---

## Definition

Rational functions are [functions](../functions/) whose numerator and denominator are both [polynomials](../polynomials/), of degrees $n$ and $m.$ They are written as a ratio of two polynomials.

$$y = \frac{P(x)}{Q(x)}$$

Here $P(x)$ and $Q(x)$ are polynomials with $Q(x) \neq 0.$ Written out in full, a rational function has the form below.

$$y = \frac{a_n x^n + a_{n-1} x^{n-1} + \dots + a_1 x + a_0}{b_m x^m + b_{m-1} x^{m-1} + \dots + b_1 x + b_0}$$

Consider the function:

$$R(x) = \frac{2x + 3}{x - 1}$$

Here the numerator and the denominator are first-degree polynomials. The expression is defined for every real number except the value that makes the denominator vanish. This happens at $x = 1,$ which must be excluded. The [domain](../determining-the-domain-of-a-function/) of the function is:

$$\{\ x \in \mathbb{R} : x \neq 1 \ \}$$

This elementary case already shows the features of a rational function: an algebraic form given by a ratio of polynomials, a domain determined by the zeros of the denominator, and a behavior described through limits, asymptotes, and algebraic simplification.

## Properties

The [domain](../determining-the-domain-of-a-function/) consists of all real numbers except the zeros of the denominator $Q(x):$

$$D = \mathbb{R} \setminus \{\ x \in \mathbb{R} \mid Q(x) = 0 \ \}$$

The range is the set of [real values](../types-of-numbers/) the function attains. It depends on the form of the function and cannot be stated in general.

The [evenness or oddness](../even-and-odd-functions/) of the function, together with its boundedness, [monotonicity](../increasing-and-decreasing-functions/), concavity, and convexity, cannot be determined in advance. These properties depend on the specific form of the rational function.

## Special cases and algebraic structure

Every polynomial is a rational function, the ratio of itself and the constant polynomial $1.$ Constants fall under the same description, since a number is a polynomial of degree zero. So [polynomials](../polynomials/) and constant functions are particular rational functions, those whose denominator carries no variable. A function is rational only when it can be written as a ratio of two polynomials, which excludes expressions such as $\sqrt{x},$ $\sin x,$ and $e^x,$ none of which is a quotient of polynomials.

The rational functions are closed under the four arithmetic operations. The sum, difference, and product of two rational functions is again a ratio of polynomials, and so is the quotient whenever the divisor is not the zero function. With these operations the rational functions form a field, in the same way the fractions of integers form the [rational numbers](../rational-numbers/).

## Proper and improper rational functions

A rational function is proper when the degree of the numerator is smaller than the degree of the denominator, $n < m,$ and improper when $n \geq m.$ The distinction matters because an improper rational function reduces to a polynomial plus a proper part. Dividing $P(x)$ by $Q(x)$ gives a quotient $E(x)$ and a remainder $S(x)$ with $\deg S < \deg Q,$ so that

$$\frac{P(x)}{Q(x)} = E(x) + \frac{S(x)}{Q(x)}$$

The polynomial $E(x)$ governs the function for large $|x|,$ since the proper part $S(x)/Q(x)$ tends to zero. The graph of $R(x)$ approaches the curve $y = E(x),$

$$\frac{P(x)}{Q(x)} - E(x) \to 0 \qquad (|x| \to \infty)$$

This decomposition underlies the [integral of a rational function](../integral-of-rational-functions/), and it explains the oblique asymptote, since when $n = m + 1$ the quotient $E(x)$ has degree one and the line $E(x) = ax + b$ is the asymptote.

As an example, divide the numerator of $R(x) = \frac{x^2 + 1}{x - 1}$ by its denominator. The quotient is $x + 1$ and the remainder is $2,$ so

$$R(x) = x + 1 + \frac{2}{x - 1}$$

The polynomial part $x + 1$ is the oblique asymptote, and the term $2/(x - 1)$ vanishes as $x \to \pm\infty.$

## Reduced form and removable discontinuities

A rational function is in reduced form, or lowest terms, when its numerator and denominator share no common polynomial factor. When they do share a factor, canceling it produces a simpler expression that agrees with the original wherever the original is defined. The canceled factor leaves a removable discontinuity, a point absent from the domain at which the function would otherwise extend continuously.

Consider $\frac{x^2 - 1}{x - 1}.$ The numerator factors as $(x - 1)(x + 1),$ and canceling the common factor $x - 1$ gives

$$\frac{x^2 - 1}{x - 1} = x + 1 \qquad x \neq 1$$

The reduced expression $x + 1$ is a polynomial defined everywhere, but the original function is undefined at $x = 1.$ Its graph is the line $y = x + 1$ with a single missing point at $x = 1,$ a removable discontinuity rather than a vertical asymptote. Distinguishing a true asymptote from a removable point therefore requires reducing the function to lowest terms before reading off its behavior.

## Continuity of rational functions

Rational functions are quotients of polynomials, and polynomials are continuous on all of $\mathbb{R}.$ A rational function is therefore continuous at every point $x_0$ where $Q(x_0) \neq 0.$ Discontinuities occur only at the solutions of $Q(x) = 0$ where the expression is not defined. The type of discontinuity depends on the numerator. If both polynomials vanish at $x_0,$ that is $P(x_0) = 0$ and $Q(x_0) = 0,$ the factor $x - x_0$ divides both, so a common factor always cancels. Whether the discontinuity is removable depends on the multiplicities. It is removable only when the multiplicity of the zero in the numerator is at least its multiplicity in the denominator, otherwise a vertical asymptote remains once the common factors are canceled. If only the denominator vanishes, with $P(x_0) \neq 0$ and $Q(x_0) = 0,$ the function diverges and a vertical asymptote appears.

## Limits at infinity for rational functions

To understand how a rational function behaves for large values of $x,$ we compare the growth of the numerator and the denominator. Far from the origin the lower-degree terms become negligible, and the function is governed by the degrees and leading coefficients of the two polynomials. Consider a rational function $R(x) = P(x)/Q(x),$ where $P(x)$ and $Q(x)$ have degrees $n$ and $m.$ The comparison between $n$ and $m$ determines the behavior as $x \to \pm\infty.$

If $n < m,$ the denominator dominates and the limit is zero:

$$\lim_{x \to \pm\infty} R(x) = 0$$

If $n = m,$ the highest-degree terms balance and the limit is the ratio of the leading coefficients:

$$\lim_{x \to \pm\infty} R(x) = \frac{a_n}{b_m}$$

If $n = m + 1,$ the function behaves like a line for large $|x|,$ which gives an oblique asymptote. The limit is not finite, but for a suitable line $ax + b$ the difference $R(x) - (ax + b)$ tends to zero.

If $n > m + 1,$ the numerator grows faster and the function diverges in magnitude:

$$\lim_{x \to \pm\infty} R(x) = \pm\infty$$

The sign of each one-sided limit depends on the sign of $a_n/b_m$ and on the parity of $n - m.$

## Limits at points where the denominator becomes zero

The delicate cases occur at the values of $x$ where the denominator vanishes. Two situations must be distinguished. In the first, the denominator is zero at a point $x_0$ while the numerator is nonzero:

$$Q(x_0) = 0 \qquad P(x_0) \neq 0$$

Near $x_0$ the expression has the form $P(x_0)/0,$ so the function grows without bound as $x$ approaches that value. The line $x = x_0$ is a vertical asymptote, and the limit is infinite.

$$\lim_{x \to x_0^\pm} R(x) = \pm\infty$$

Its sign is fixed by how the denominator changes on either side of $x_0.$

- - -

A different situation occurs when numerator and denominator vanish at the same point, which produces the [indeterminate form](../indeterminate-forms/):

$$\frac{0}{0}$$

Here the limit cannot be read directly from the polynomials evaluated at $x_0.$ The function may simplify to a finite limit, or it may diverge. To determine the result, we factor the numerator and the denominator to cancel common factors, or apply [L'Hôpital's rule](../hopital-rule/) when its conditions hold.

## Asymptotes

A rational function does not always have an [asymptote](../asymptotes/). A polynomial has none, and a fraction with $n > m + 1$ and a denominator that never vanishes diverges without one. When asymptotes do occur, their nature depends on the degrees of the two polynomials and on the zeros of the denominator. The following cases can be identified:

+ If $Q(x_0) = 0$ and $P(x_0) \neq 0,$ the line $x = x_0,$ the point where the denominator vanishes, is a vertical asymptote.
+ If $n = m,$ the function has a horizontal asymptote at the ratio of the leading coefficients $a_n/b_m.$ If $n < m,$ the horizontal asymptote is the line $y = 0.$
+ An oblique asymptote occurs when the degree of $P(x)$ exceeds the degree of $Q(x)$ by one, that is $n = m + 1.$

## Partial fraction decomposition

A proper rational function splits into a sum of simpler fractions, one for each factor of the denominator. After factoring $Q(x)$ into linear and irreducible quadratic factors, the function is written as a sum of terms whose denominators are those factors, with constant or linear numerators left to determine. This [partial fraction decomposition](../partial-fraction-decomposition/) turns a single complicated ratio into pieces that are simple to differentiate, integrate, and expand. Take:

$$\frac{3x + 5}{(x - 1)(x + 2)}$$

and look for constants $A$ and $B$ with

$$\frac{3x + 5}{(x - 1)(x + 2)} = \frac{A}{x - 1} + \frac{B}{x + 2}$$

Multiplying both sides by $(x - 1)(x + 2)$ gives $3x + 5 = A(x + 2) + B(x - 1).$ Setting $x = 1$ yields $8 = 3A,$ so $A = 8/3.$ Setting $x = -2$ yields $-1 = -3B,$ so $B = 1/3.$ The decomposition is

$$\frac{3x + 5}{(x - 1)(x + 2)} = \frac{8/3}{x - 1} + \frac{1/3}{x + 2}$$

When the numerator has degree at least that of the denominator, we first divide to extract the polynomial part, then decompose the proper remainder. The factors that fix the partial fractions are the zeros of the denominator, so this decomposition also organizes the analysis of vertical asymptotes and the computation of the [integral of a rational function](../integral-of-rational-functions/).

## Derivatives and integrals

Rational functions are [continuous](../continuous-functions/) and differentiable on their whole domain. The [derivative](../derivatives/) has no single closed form, but it is computed with the quotient rule,

$$\frac{d}{dx} \left[ \frac{P(x)}{Q(x)} \right] = \frac{P'(x)Q(x) - P(x)Q'(x)}{[Q(x)]^2}$$

- - -

Integration has no single standard method either, and depends on the form of the function. The general approach combines the two decompositions already seen. Polynomial division first separates the polynomial part from a proper remainder,

$$\int \frac{P(x)}{Q(x)} \ dx = \int E(x) \ dx + \int \frac{S(x)}{Q(x)} \ dx$$

The polynomial part $E(x)$ integrates directly, while the proper part $S(x)/Q(x)$ is split by partial fractions into terms that integrate to logarithms and arctangents. The full procedure is developed in the [integral of a rational function](../integral-of-rational-functions/).
