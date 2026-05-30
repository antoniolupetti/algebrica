---
title: Rational Equations
source: https://algebrica.org/rational-equations/
license: CC BY-NC 4.0
tags:
  - equations
  - polynomials
  - rational-equations
---

## What are rational equations

Rational equations contain at least one fraction whose numerator and denominator are [polynomials](../polynomials/). They are called rational because they can be expressed as the ratio of two polynomials. A rational equation can present fractions on both sides, but by transferring every term to one side and combining the result over a common denominator it always reduces to the canonical form:

$$\frac{P(x)}{Q(x)} = 0$$

In this expression $P(x)$ and $Q(x)$ are polynomials with $Q(x) \neq 0$. A polynomial is a combination of [monomials](../monomials/) added or subtracted together, and its general form is the following:

$$a_nx^n + a_{n-1}x^{n-1} + \dotsb + a_2x^2 + a_1x + a_0$$

In this expression the symbols have the following meaning:

+ $a_nx^n$ is a monomial
+ $a$ is a real number, the coefficient of the term
+ $n$ is a non-negative [integer](../integers/), the exponent of the variable

## Distinction between irrational and rational equations

The distinction between rational and [irrational equations](../irrational-equations/) lies in their structure. Rational equations consist of fractions whose numerator and denominator are polynomials, and can always be written as a ratio of two polynomials. Irrational equations contain roots of various orders, expressed through [radical](../radicals/) notation with an index indicating their order, and their solutions cannot in general be described as rational numbers.

- - -

This difference is clarified by two examples:

+ $\dfrac{2x}{2x-1}$ is a rational expression, since it contains only ratios of polynomial terms
+ $\dfrac{1}{\sqrt{2x-1}}$ is an [irrational](../irrational-equations/) expression, since the variable appears inside a root

## How to solve rational equations

The solution of a rational equation proceeds in three stages:

+ Determine the values that make the denominators vanish. These values must be excluded, since they leave the expression undefined. The set of admissible values, those for which every denominator is nonzero, constitutes the conditions of existence of the equation.
+ Determine the least common multiple of the [polynomials](../polynomials/) appearing in the denominators, clear the denominators, and solve the resulting polynomial equation in the numerator.
+ Compare each solution with the conditions of existence, discarding any value that nullifies a denominator, and verify that the remaining solutions satisfy the original equation.

> Comparing the solutions with the conditions of existence is essential. Clearing denominators can produce values that solve the transformed equation while violating the original one. Such values are extraneous solutions and must be discarded, a phenomenon related to the [loss of roots](../loss-of-roots/).

## Example with a single admissible solution

Solve the rational equation:

$$\frac{1}{x+1} + \frac{1}{x+2} = 0$$

The first step is to determine the values that make the denominators vanish, since these lead to an undefined expression:

$$
\begin{align}
x + 1 = 0 \quad &\rightarrow \quad x = -1 \\[6pt]
x + 2 = 0 \quad &\rightarrow \quad x = -2
\end{align}
$$

The values $x = -1$ and $x = -2$ must be excluded from the solution set, since they would make a denominator zero.

Reducing the two fractions to a common denominator and combining them gives:

$$
\begin{align}
&\frac{x+2}{(x+1)(x+2)} + \frac{x+1}{(x+1)(x+2)} = 0 \\[6pt]
&\frac{x+2+x+1}{(x+1)(x+2)} = 0 \\[6pt]
&\frac{2x+3}{(x+1)(x+2)} = 0
\end{align}
$$

A fraction equals zero when its numerator equals zero. Setting $2x + 3 = 0$ gives a first-degree [linear equation](../linear-equations/) with the unique solution $x = -\frac{3}{2}$. This value is not among those that nullify the denominators, so it is admissible. Substituting it into the original equation confirms the result:

$$
\begin{align}
\frac{1}{-\frac{3}{2}+1} + \frac{1}{-\frac{3}{2}+2} &= 0 \\[6pt]
\frac{1}{-\frac{1}{2}} + \frac{1}{\frac{1}{2}} &= 0 \\[6pt]
-2 + 2 &= 0
\end{align}
$$

The equality holds. The solution of the equation is therefore:

$$x = -\frac{3}{2}$$

## Example with an extraneous solution

The next example shows why the comparison with the conditions of existence cannot be omitted. Consider the equation:

$$\frac{x}{x-2} + \frac{2}{x+1} = \frac{6}{(x-2)(x+1)}$$

The denominators vanish at the values that annul the factors $x-2$ and $x+1$:

$$
\begin{align}
x - 2 = 0 \quad &\rightarrow \quad x = 2 \\[6pt]
x + 1 = 0 \quad &\rightarrow \quad x = -1
\end{align}
$$

The conditions of existence therefore require $x \neq 2$ and $x \neq -1$. The least common multiple of the denominators is $(x-2)(x+1)$, since the third denominator already coincides with this product. Multiplying every term by this common factor clears the fractions and leaves a polynomial equation:

$$
\begin{align}
x(x+1) + 2(x-2) &= 6 \\[6pt]
x^2 + x + 2x - 4 &= 6 \\[6pt]
x^2 + 3x - 10 &= 0
\end{align}
$$

The result is a [quadratic equation](../quadratic-equations/). Factoring the trinomial gives:

$$(x+5)(x-2) = 0$$

The product vanishes when one of its factors is zero, which yields the two candidate solutions $x = -5$ and $x = 2$. The second candidate coincides with one of the excluded values, so it violates the conditions of existence and must be discarded as an extraneous solution. Only $x = -5$ remains, and substituting it into the original equation confirms its validity:

$$
\begin{align}
\frac{-5}{-5-2} + \frac{2}{-5+1} &= \frac{6}{(-5-2)(-5+1)} \\[6pt]
\frac{-5}{-7} + \frac{2}{-4} &= \frac{6}{(-7)(-4)} \\[6pt]
\frac{5}{7} - \frac{1}{2} &= \frac{6}{28} \\[6pt]
\frac{3}{14} &= \frac{3}{14}
\end{align}
$$

The equality holds, while the candidate $x = 2$ would have produced a division by zero. The unique solution of the equation is therefore:

$$x = -5$$
