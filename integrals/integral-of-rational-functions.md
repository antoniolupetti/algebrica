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
## Integration of rational functions with polynomial division

A [rational function](../rational-functions/) is the quotient of two polynomials, and the corresponding [indefinite integral](../indefinite-integrals/) takes the general form:

$$\int \frac{N(x)}{D(x)} \ dx$$

where $N(x)$ and $D(x)$ are [polynomials](../polynomials/) with real coefficients, and $D(x)$ is not identically zero. The strategy for computing an integral of this kind depends on the relation between the degrees of the numerator and the denominator. The discussion starts with the case in which the degree of $N(x)$ is greater than or equal to the degree of $D(x)$.

- - -

From the general properties of polynomials, it is always possible to perform the [division](../polynomial-division/) of a polynomial $N(x)$ by a non-zero polynomial $D(x)$. The result of this operation consists of two polynomials:

+ A quotient polynomial $Q(x)$.
+ A remainder polynomial $R(x)$, whose degree is strictly less than the degree of $D(x)$.

This process produces an identity of the form:

$$N(x) = Q(x) D(x) + R(x)$$

Dividing both sides by $D(x)$:

$$\frac{N(x)}{D(x)} = Q(x) + \frac{R(x)}{D(x)}$$

Integrating both sides:

$$\int \frac{N(x)}{D(x)} \ dx = \int Q(x) \ dx + \int \frac{R(x)}{D(x)} \ dx$$

- - -

What guides the choice of method is the comparison between the degrees of the numerator and the denominator. When $\deg N(x) \geq \deg D(x)$, the rational function is improper and must first be reduced by polynomial long division. Only after this preliminary step does the integral take a manageable form.

When $\deg N(x) < \deg D(x)$, the rational function is already proper, and attention shifts to the factorisation of the denominator. Its algebraic structure dictates the technique:

+ When the denominator is a single linear factor, a simple substitution typically settles the integral immediately.
+ When it splits into distinct linear factors, decomposing into partial fractions converts the expression into a sum of elementary terms.
+ When a linear factor is repeated, each power of that factor generates its own term in the decomposition, forming a small hierarchy of fractions.
+ When an irreducible quadratic factor is present, the path runs through completing the square and naturally leads to an inverse tangent term.

> Once the rational function has been reduced to the proper case, the denominator governs the entire strategy. Its factorisation over the real numbers determines the structure of the partial fraction decomposition. Integration then becomes a systematic reduction to logarithmic and inverse trigonometric primitives.

## Example 1

Compute the integral of the rational function:

$$\int \frac{x^3 + x + 1}{x^2 + 1} \ dx$$

The first step is the [polynomial division](../polynomial-division/) of the numerator by the denominator, which gives:

$$Q(x) = x \qquad R(x) = 1$$

so that:

$$\frac{x^3 + x + 1}{x^2 + 1} = x + \frac{1}{x^2 + 1}$$

> The method of dividing two polynomials is treated in detail on the page on [polynomials](../polynomials/).

- - -

The integral splits into two terms:

$$\int \frac{x^3 + x + 1}{x^2 + 1} \ dx = \int x \ dx + \int \frac{1}{x^2 + 1} \ dx$$

Evaluating each term and combining the constants of integration:

$$\int \frac{x^3 + x + 1}{x^2 + 1} \ dx = \frac{x^2}{2} + \arctan(x) + c$$

## Integrals with linear denominators

The simplest case of a proper rational function occurs when the denominator is a polynomial of degree one. The integral takes the form:

$$\int \frac{c}{ax + b} \ dx$$

where $a$, $b$, and $c$ are real constants with $a \neq 0$. The numerator is a constant, and the degree condition $\deg N(x) < \deg D(x)$ is automatically satisfied.

An integral of this type is solved by [integration by substitution](../integration-by-substitution/). Setting $t = ax + b$ gives $dt = a \ dx$, and the integral becomes:

$$\int \frac{c}{ax + b} \ dx = \frac{c}{a} \int \frac{1}{t} \ dt = \frac{c}{a} \ln|t| + k$$

Returning to the original variable:

$$\int \frac{c}{ax + b} \ dx = \frac{c}{a} \ln|ax + b| + k$$

The absolute value is essential, since the linear expression $ax + b$ changes sign at $x = -b/a$ and the natural logarithm is defined only for positive arguments. The formula holds on any interval that does not contain this point, where the integrand is otherwise continuous. This case also serves as a building block for the more general situation. Once a proper rational function has been decomposed into partial fractions, every term whose denominator is a simple linear factor reduces to an integral of the form considered here. The logarithmic primitive obtained above therefore appears repeatedly in the rest of the discussion.

## Example 2

Compute the integral of the rational function:

$$\int \frac{2}{6x + 1} \ dx$$

Apply the substitution $t = 6x + 1$. Differentiating both sides with respect to $x$:

$$\frac{dt}{dx} = 6 \quad \Rightarrow \quad dx = \frac{dt}{6}$$

Replacing into the integral:

$$\int \frac{2}{6x + 1} \ dx = \int \frac{2}{t} \cdot \frac{dt}{6} = \frac{1}{3} \int \frac{1}{t} \ dt$$

The remaining integral is one of the elementary forms recalled in the page on [indefinite integrals](../indefinite-integrals/), and its primitive is the natural logarithm of the absolute value of $t$:

$$\frac{1}{3} \int \frac{1}{t} \ dt = \frac{1}{3} \ln|t| + c$$

Returning to the original variable by substituting $t = 6x + 1$, the final result is:

$$\int \frac{2}{6x + 1} \ dx = \frac{1}{3} \ln|6x + 1| + c$$

## Partial fraction decomposition

In many situations, the integral of a rational function cannot be computed directly by inspection. Even when the expression appears relatively simple, algebraic manipulations may not reveal an immediate antiderivative. In such cases, the method of [partial fraction decomposition](../partial-fraction-decomposition/) provides a systematic way to rewrite the function as a sum of elementary terms whose integrals are well known. By decomposing the rational function into simpler components, a representation far more suitable for integration is obtained. To illustrate the idea in a setting different from the earlier examples, consider the integral:

$$\int \frac{7x + 5}{(x - 1)(3x + 2)} \ dx$$

At first glance, the structure of this expression does not suggest an obvious primitive. Once the integrand is decomposed into partial fractions, the computation becomes straightforward. The starting point is:

$$\frac{7x + 5}{(x - 1)(3x + 2)} = \frac{A}{x - 1} + \frac{B}{3x + 2} \tag{1}$$

Multiplying both sides by $(x - 1)(3x + 2)$ yields the identity:

$$7x + 5 = A(3x + 2) + B(x - 1)$$

The coefficients $A$ and $B$ are determined by evaluating at the convenient values $x = 1$ and $x = -2/3$:

$$A = 4 \qquad B = -5$$

Substituting these values into identity $(1)$:

$$\frac{7x + 5}{(x - 1)(3x + 2)} = \frac{4}{x - 1} - \frac{5}{3x + 2}$$

The integral becomes:

$$\int \left( \frac{4}{x - 1} - \frac{5}{3x + 2} \right) dx$$

By the linearity of the [indefinite integral](../indefinite-integrals/), each term can be treated separately:

$$4 \int \frac{1}{x - 1} \ dx \qquad 5 \int \frac{1}{3x + 2} \ dx$$

Both integrals reduce to elementary [logarithmic](../logarithms/) forms:

$$4 \ln|x - 1| + c_1 \qquad \frac{5}{3} \ln|3x + 2| + c_2$$

Combining the constants and simplifying:

$$\int \frac{7x + 5}{(x - 1)(3x + 2)} \ dx = 4 \ln|x - 1| - \frac{5}{3} \ln|3x + 2| + c$$

> This example shows how a rational function that initially presents no clear path to integration becomes entirely tractable once rewritten in partial fractions. The method transforms the integral into a collection of standard forms, making the computation both systematic and transparent.

## Repeated linear factors

When the denominator of a rational function contains a linear factor raised to a power greater than one, the decomposition into partial fractions requires a structural adjustment. A single term of the form $A/(x - r)$ is no longer sufficient to capture the behaviour of the function near the repeated root. Each power of the factor must contribute its own term to the decomposition.

When the denominator contains the factor $(x - r)^k$, the corresponding contribution to the partial fraction decomposition is:

$$\frac{A_1}{x - r} + \frac{A_2}{(x - r)^2} + \dots + \frac{A_k}{(x - r)^k}$$

Each numerator is a constant, and the denominators range over all powers of $(x - r)$ from the first up to the multiplicity $k$. Omitting any of these terms would, in general, make the system of equations for the coefficients inconsistent.

Once the decomposition has been written, the integration proceeds term by term. The first contribution produces a logarithm, while every term of the form $A_j/(x - r)^j$ with $j \geq 2$ integrates to a power of $(x - r)$ with negative exponent:

$$\int \frac{1}{(x - r)^j} \ dx = \frac{(x - r)^{1 - j}}{1 - j} + c \qquad (j \geq 2)$$

The logarithmic term therefore appears only once, associated with the simple power, whereas the higher powers contribute rational expressions without logarithms.

## Example 3

Consider the integral:

$$\int \frac{3x + 1}{(x - 1)^2 (x + 2)} \ dx$$

The denominator contains the factor $x - 1$ with multiplicity two and the simple factor $x + 2$. According to the general rule for repeated linear factors, the partial fraction decomposition takes the form:

$$\frac{3x + 1}{(x - 1)^2 (x + 2)} = \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{x + 2}$$

Multiplying both sides by the common denominator $(x - 1)^2 (x + 2)$, the polynomial identity reads:

$$3x + 1 = A(x - 1)(x + 2) + B(x + 2) + C(x - 1)^2$$

The coefficients are determined by evaluating the identity at convenient values of $x$. Substituting $x = 1$ eliminates every term containing the factor $x - 1$, and the identity reduces to $4 = 3B$, from which:

$$B = \frac{4}{3}$$

Substituting $x = -2$ eliminates every term containing the factor $x + 2$, and the identity reduces to $-5 = 9C$, from which:

$$C = -\frac{5}{9}$$

The remaining coefficient $A$ cannot be obtained by direct substitution, since no value of $x$ simultaneously cancels all the terms that depend on $A$. The standard approach is to compare the coefficients of the highest power of $x$ on both sides of the identity. The left-hand side contains no term in $x^2$, so its coefficient is zero. On the right-hand side, expanding the products shows that the coefficient of $x^2$ is $A + C$. Setting the two expressions equal gives $A + C = 0$, from which:

$$A = \frac{5}{9}$$

Substituting the values just obtained into the decomposition:

$$\frac{3x + 1}{(x - 1)^2 (x + 2)} = \frac{5/9}{x - 1} + \frac{4/3}{(x - 1)^2} - \frac{5/9}{x + 2}$$

The integral splits into three terms, each of which admits a known primitive:

$$\frac{5}{9} \int \frac{1}{x - 1} \ dx + \frac{4}{3} \int \frac{1}{(x - 1)^2} \ dx - \frac{5}{9} \int \frac{1}{x + 2} \ dx$$

The first and the third integrals produce logarithmic primitives, while the second integral produces a rational expression with negative exponent. Combining the contributions, an antiderivative of the original rational function is:

$$\frac{5}{9} \ln|x - 1| - \frac{4}{3} \cdot \frac{1}{x - 1} - \frac{5}{9} \ln|x + 2| + c$$

The final expression shows how the two distinct powers of the factor $x - 1$ generate primitives of different nature: a logarithm from the simple power and a rational term from the squared power.

> The repeated factor $(x - 1)^2$ contributes two distinct terms to the antiderivative. Only the simple power produces a logarithm, whereas the higher power yields a rational expression with negative exponent. The same pattern applies to every linear factor of multiplicity greater than one.

## Irreducible quadratic factors in the denominator

Not every polynomial splits into linear factors over the real numbers. A quadratic expression $ax^2 + bx + c$ whose [discriminant](../quadratic-formula/) satisfies $b^2 - 4ac < 0$ has no real roots. It cannot be written as $(x - r_1)(x - r_2)$ with $r_1, r_2 \in \mathbb{R}$.

Over the real field, such a quadratic is said to be irreducible. When a factor of this type appears in the denominator of a rational function, the strategy for partial fraction decomposition changes slightly. In the linear case, each factor $(x - r)$ gives rise to a term of the form:

$$\frac{A}{x - r}$$

Here there are no real roots to attach such terms to. The quadratic must therefore remain intact in the denominator. An irreducible quadratic factor $ax^2 + bx + c$ contributes a term of the form:

$$\frac{Ax + B}{ax^2 + bx + c}$$

The numerator must have degree strictly smaller than the denominator, and in the quadratic case that means degree one. Using only a constant would not provide enough flexibility to match the original rational function. Once the decomposition is complete, integration typically proceeds by rewriting the quadratic denominator through [completing the square](../completing-the-square/). After an appropriate change of variable, the integral reduces to:

$$\int \frac{1}{u^2 + a^2} \ du$$

whose antiderivative is:

$$\frac{1}{a}\arctan\!\left(\frac{u}{a}\right) + c$$

The appearance of the [arctangent](../arctangent-and-arccotangent/) reflects the geometric structure encoded in the expression $u^2 + a^2$, which cannot vanish over the real numbers and corresponds, analytically, to the derivative of the inverse [tangent function](../tangent-function/).

## Example 4

Consider the following integral:

$$\int \frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} \ dx$$

The denominator is already written as a product. One factor, $x + 1$, is linear. The other, $x^2 + 2x + 3$, deserves a closer look. Its discriminant is:

$$\Delta = 2^2 - 4 \cdot 1 \cdot 3 = 4 - 12 = -8 < 0$$

so it has no real zeros and is irreducible over $\mathbb{R}$. This determines the shape of the partial fraction decomposition:

$$\frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} = \frac{A}{x + 1} + \frac{Bx + C}{x^2 + 2x + 3}$$

Clearing denominators by multiplying both sides by $(x + 1)(x^2 + 2x + 3)$ produces the identity:

$$5x^2 + 3x - 2 = A(x^2 + 2x + 3) + (Bx + C)(x + 1)$$

A convenient first step is to evaluate at $x = -1$. The second term vanishes at that value, and:

$$5(-1)^2 + 3(-1) - 2 = A\bigl((-1)^2 + 2(-1) + 3\bigr)$$

The left-hand side simplifies to $5 - 3 - 2 = 0$, while the right-hand side becomes $A(1 - 2 + 3) = 2A$. Hence $0 = 2A$, so:

$$A = 0$$

With $A = 0$, the identity reduces to:

$$5x^2 + 3x - 2 = (Bx + C)(x + 1)$$

Expanding the right-hand side:

$$(Bx + C)(x + 1) = Bx^2 + (B + C)x + C$$

Matching coefficients term by term:

$$B = 5 \qquad B + C = 3$$

From the second relation, $C = -2$. The decomposition therefore collapses to:

$$\frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} = \frac{5x - 2}{x^2 + 2x + 3}$$

The integral simplifies considerably:

$$\int \frac{5x - 2}{x^2 + 2x + 3} \ dx$$

The standard strategy at this point is to relate the numerator to the derivative of the denominator. Since:

$$\frac{d}{dx}(x^2 + 2x + 3) = 2x + 2$$

the numerator is rewritten as a combination of this derivative and a constant:

$$5x - 2 = \frac{5}{2}(2x + 2) - 7$$

The integral splits accordingly:

$$\frac{5}{2} \int \frac{2x + 2}{x^2 + 2x + 3} \ dx - 7 \int \frac{1}{x^2 + 2x + 3} \ dx$$

- - -

For the first piece, the numerator is exactly the derivative of the denominator, which produces a logarithm:

$$\frac{5}{2} \ln|x^2 + 2x + 3|$$

Since the quadratic has negative discriminant it is always positive, so the [absolute value](../absolute-value/) is not strictly necessary, though keeping it causes no harm.

- - -

For the second piece, completing the square gives $x^2 + 2x + 3 = (x + 1)^2 + 2$, so the integral becomes:

$$-7 \int \frac{1}{(x + 1)^2 + 2} \ dx$$

With the substitution $u = x + 1$ and $a^2 = 2$:

$$-\frac{7}{\sqrt{2}} \arctan\!\left(\frac{x + 1}{\sqrt{2}}\right)$$

Putting everything together, an antiderivative is:

$$\frac{5}{2} \ln(x^2 + 2x + 3) - \frac{7}{\sqrt{2}} \arctan\!\left(\frac{x + 1}{\sqrt{2}}\right) + c$$

> The factor $x + 1$ initially appears to require its own term in the decomposition. Once the coefficients are computed, that contribution disappears entirely. The full decomposition must always be written down: what seems essential at first may ultimately cancel.

## Decision procedure

The following stepwise procedure summarises the integration of a generic rational function.

+ When $\deg N(x) \geq \deg D(x)$, perform polynomial long division to write $N(x) = Q(x) D(x) + R(x)$ with $\deg R(x) < \deg D(x)$, split the integral as $\int Q(x) \ dx + \int R(x)/D(x) \ dx$, and restart with the proper part.
+ When $D(x)$ is a single linear factor $ax + b$, apply the substitution $t = ax + b$. The result is the logarithm $\tfrac{c}{a}\ln|ax + b| + k$.
+ When $D(x)$ factors into distinct linear factors, write the partial fraction decomposition with one term $A_i/(x - r_i)$ per factor, determine the coefficients by evaluation at the roots or by matching coefficients, and integrate term by term: each contribution is a logarithm.
+ When $D(x)$ contains a repeated linear factor $(x - r)^k$, expand the decomposition into one term per power, from $A_1/(x - r)$ up to $A_k/(x - r)^k$, and integrate term by term: the simple power produces a logarithm, the higher powers produce rational terms.
+ When $D(x)$ contains an irreducible quadratic factor $ax^2 + bx + c$ with $b^2 - 4ac < 0$, add the term $(Ax + B)/(ax^2 + bx + c)$ to the decomposition. Split the numerator into a multiple of the derivative of the denominator plus a constant, and integrate the two pieces: the derivative part produces a logarithm, while the constant part is reduced by completing the square and yields an arctangent.
+ When a product of polynomial and exponential or polynomial and trigonometric function appears alongside the rational structure, the standard alternative is [integration by parts](../integration-by-parts/). For rational integrands in $\sin x$ and $\cos x$, the [Weierstrass substitution](../weierstrass-substitution/) is the natural tool.
