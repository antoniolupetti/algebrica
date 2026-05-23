---
title: Integration by Substitution
source: https://algebrica.org/integration-by-substitution/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - chain-rule
  - change-of-variable
  - composite-functions
  - definite-integral
  - indefinite-integral
  - integration
  - integration-by-substitution
  - trigonometric-substitution
---
## How substitution simplifies integration

Integration by substitution is a technique that simplifies an [integral](../indefinite-integrals/) by introducing a change of variable. When the integral is not straightforward, this method allows the integral of a function $f(x)$ to be rewritten in terms of a new variable $u$, often producing a much simpler computation:

$$\int f(g(x)) g'(x) \ dx = \int f(u) \ du$$

The procedure involves the following steps:

+ Introduce a change of variable by defining $u = g(x)$, where $g(x)$ is an appropriately chosen function.
+ Compute the differential transformation, given by $du = g'(x) \ dx$.
+ Rewrite the integral in terms of $u$, replacing $x$ and $dx$ accordingly, so that the resulting expression is easier to handle.
+ Once the integral in $u$ has been evaluated, revert to the original variable $x$ to express the final result in its initial form.

> Substitution reverses the [chain rule](../the-derivative-of-a-composite-function/): recognising this connection makes it easier to identify when and how the technique can be applied.

- - -

The method of substitution is a direct consequence of the chain rule for [derivatives](../derivatives/). If $F(x) = H(g(x))$, then by the chain rule:

$$F'(x) = H'(g(x)) g'(x)$$

Whenever an integrand has the form $H'(g(x)) g'(x)$, it is therefore the derivative of the composite function $H(g(x))$. Integration by substitution simply reverses this process by introducing $u = g(x)$, reducing the integral to:

$$\int H'(u) \ du = H(u) + c$$

## Recognising when to use substitution

Before turning to concrete examples, it helps to understand when a substitution is likely to be effective. The technique is most natural when the integrand contains a [composite function](../composite-functions/). In many cases, the integral has the general form:

$$f(g(x)) g'(x)$$

or differs from it only by a constant factor. When this pattern appears, choosing $u = g(x)$ simplifies the expression by reducing the composite structure to a single variable. A common signal is the presence of expressions such as $(ax + b)^n$, $\sqrt{ax + b}$, $\ln(ax + b)$, or $e^{ax + b}$. In these cases, the inner linear function $ax + b$ is a natural candidate for substitution. Similarly, in rational expressions of the form:

$$\frac{g'(x)}{g(x)}$$

the derivative of the denominator suggests the substitution $u = g(x)$.

> The key idea in practice is to look for an inner expression whose derivative also appears, exactly or up to a multiplicative constant, elsewhere in the integrand. When such a relationship is present, substitution typically transforms the integral into a simpler form.

## Substitution patterns

These integrals exhibit recurring structural patterns in which an appropriate substitution reduces the integrand to a simpler expression that can be integrated more directly:

[class="table-1"]

|                                  |              |
| -------------------------------- | ------------ |
| $$\int f(g(x)) g'(x) \ dx$$      | $$u = g(x)$$ |
| $$\int (ax + b)^n \ dx$$         | $$u = ax + b$$ |
| $$\int e^{ax + b} \ dx$$         | $$u = ax + b$$ |
| $$\int \ln(ax + b) \ dx$$        | $$u = ax + b$$ |
| $$\int \dfrac{g'(x)}{g(x)} \ dx$$ | $$u = g(x)$$ |

[/class]

## Example 1

Consider the following integral:

$$\int (2x + 1)^3 \ dx$$

Set $u = 2x + 1$, which simplifies the exponentiation. Differentiating both sides with respect to $x$:

$$du = 2 \ dx$$

Solving for $dx$:

$$dx = \frac{du}{2}$$

- - -

Expressing the integral entirely in terms of $u$:

$$\int u^3 \cdot \frac{du}{2} = \frac{1}{2} \int u^3 \ du$$

The integral in $u$ falls under the power rule. Computing:

$$\frac{1}{2} \cdot \frac{u^4}{4} + c = \frac{1}{8} u^4 + c$$

Substituting back $u = 2x + 1$:

$$\int (2x + 1)^3 \ dx = \frac{1}{8} (2x + 1)^4 + c$$

## Example 2

Evaluate the following integral:

$$\int \frac{1}{3x - 5} \ dx$$

Set $u = 3x - 5$, which simplifies the denominator. Differentiating both sides with respect to $x$:

$$du = 3 \ dx$$

Solving for $dx$:

$$dx = \frac{du}{3}$$

- - -

Expressing the integral entirely in terms of $u$:

$$\int \frac{1}{u} \cdot \frac{du}{3} = \frac{1}{3} \int \frac{du}{u}$$

The integral in $u$ is the logarithmic case. Computing:

$$\frac{1}{3} \ln |u| + c$$

Substituting back $u = 3x - 5$:

$$\int \frac{1}{3x - 5} \ dx = \frac{1}{3} \ln |3x - 5| + c$$

> Integration by substitution is an effective technique, but selecting the right substitution requires practice and the ability to recognise the structure of the integrand.

## Example 3

Evaluate the following integral:

$$\int x \sin(x^2) \ dx$$

The substitution is less immediate here, since the integrand does not match the standard pattern as directly as in the previous examples. Set $u = x^2$, which simplifies the argument of the sine function. Differentiating both sides with respect to $x$:

$$du = 2x \ dx$$

Solving for $dx$:

$$dx = \frac{du}{2x}$$

- - -

Rewriting everything in terms of $u$, the factor $x$ in the original integrand cancels with the $x$ in the denominator of $dx$:

$$\int x \sin(u) \cdot \frac{du}{2x} = \frac{1}{2} \int \sin(u) \ du$$

The integral in $u$ is standard:

$$\int \sin u \ du = -\cos u$$

Therefore:

$$\frac{1}{2} (-\cos u) + c = -\frac{1}{2} \cos u + c$$

Substituting back $u = x^2$:

$$\int x \sin(x^2) \ dx = -\frac{1}{2} \cos(x^2) + c$$

## Example 4

Evaluate the following integral:

$$\int \cos x \sqrt{\sin x} \ dx$$

Set $u = \sin x$, which simplifies the square root. Differentiating both sides with respect to $x$:

$$du = \cos x \ dx$$

The factor $\cos x \ dx$ appears in the integrand and can be replaced directly by $du$.

- - -

Substituting $u = \sin x$ and $du = \cos x \ dx$:

$$\int \sqrt{u} \ du = \int u^{1/2} \ du$$

Applying the power rule:

$$\int u^{1/2} \ du = \frac{u^{3/2}}{3/2} = \frac{2}{3} u^{3/2} + c$$

Substituting back $u = \sin x$:

$$\int \cos x \sqrt{\sin x} \ dx = \frac{2}{3} (\sin x)^{3/2} + c$$

## Trigonometric substitutions

Trigonometric substitution applies when an integral involves [polynomial](../polynomials/), [rational](../rational-functions/), or algebraic expressions that can be simplified using the [fundamental trigonometric identity](../pythagorean-identity/):

$$\sin^2 x + \cos^2 x = 1$$

which can be rewritten in the following forms:

$$
\begin{align}
\cos^2 x &= 1 - \sin^2 x \\[6pt]
\sec^2 x &= 1 + \tan^2 x \\[6pt]
\tan^2 x &= \sec^2 x - 1
\end{align}
$$

The choice of substitution depends on the form of the expression under the radical:

+ When the integrand contains $1 - x^2$, use $x = \sin u$.
+ When the integrand contains $1 + x^2$, use $x = \tan u$.
+ When the integrand contains $x^2 - 1$, use $x = \sec u$.

> A complete discussion of trigonometric substitution, including the geometric rationale and fully worked examples, is presented on the dedicated page on [trigonometric substitution for integrals](../trigonometric-substitution-for-integrals/).

## Example 5

Evaluate the following integral:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx$$

For expressions of the form $a^2 - x^2$, a natural substitution is:

$$x = 3\sin u$$

Differentiating both sides:

$$dx = 3\cos u \ du$$

- - -

Substituting $x = 3\sin u$ in the denominator:

$$\sqrt{9 - x^2} = \sqrt{9 - 9\sin^2 u} = \sqrt{9(1 - \sin^2 u)}$$

Since $\sin^2 u + \cos^2 u = 1$:

$$\sqrt{9(1 - \sin^2 u)} = \sqrt{9\cos^2 u} = 3\cos u$$

The integral transforms into:

$$\int \frac{3\cos u \ du}{3\cos u} = \int du = u + c$$

> This step assumes $\cos u \geq 0$, which holds since the substitution $x = 3\sin u$ implies $u \in [-\pi/2, \pi/2]$.

- - -

From the substitution $x = 3\sin u$, solving for $u$ through the [arcsine](../arcsine-and-arccosine/) function gives:

$$u = \arcsin\left(\frac{x}{3}\right)$$

The final result is therefore:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx = \arcsin\left(\frac{x}{3}\right) + c$$

## Substitution rule for definite integrals

When substitution is applied to evaluate [definite integrals](../definite-integrals/), the limits of integration must be adjusted to reflect the new variable. If the limits are not changed, the result will be incorrect. Given the substitution $u = g(x)$:

$$\int_{a}^{b} f(g(x)) g'(x) \ dx = \int_{g(a)}^{g(b)} f(u) \ du$$

- - -

Evaluate the following definite integral:

$$\int_{0}^{1} x\cos(x^2) \ dx$$

Using the substitution $u = x^2$:

$$du = 2x \ dx \qquad dx = \frac{du}{2x}$$

The limits of integration must be updated. When $x = 0$, then $u = 0$; when $x = 1$, then $u = 1$. The transformed limits coincide with the original ones in this case, but in general this need not happen. The integral becomes:

$$\int_{0}^{1} x\cos(x^2) \ dx = \int_{0}^{1} \cos u \cdot \frac{du}{2} = \frac{1}{2}\int_{0}^{1} \cos u \ du$$

Evaluating:

$$\frac{1}{2}\Bigl[\sin u\Bigr]_{0}^{1} = \frac{1}{2}(\sin 1 - \sin 0) = \frac{\sin 1}{2}$$

## Decision procedure

The following stepwise procedure summarises the application of integration by substitution to a generic integral.

+ Identify the structure of the integrand. When it matches a standard form (power, exponential, logarithmic, trigonometric), integrate directly through the corresponding formula collected on the page on [indefinite integrals](../indefinite-integrals/).
+ When the integrand contains a radical expression of the form $a^2 - x^2$, $a^2 + x^2$, or $x^2 - a^2$, apply the appropriate trigonometric substitution: $x = a\sin u$, $x = a\tan u$, or $x = a\sec u$ respectively. A detailed treatment is given on the page on [trigonometric substitution for integrals](../trigonometric-substitution-for-integrals/).
+ When the integrand has the form $f(g(x)) g'(x)$, set $u = g(x)$, compute $du = g'(x) \ dx$, rewrite the integral entirely in $u$, and integrate by the appropriate standard formula.
+ For definite integrals, update the limits of integration to $g(a)$ and $g(b)$ before evaluating, so that no back-substitution is needed.
+ For indefinite integrals, substitute back $u = g(x)$ to express the antiderivative in the original variable.
+ When the integrand is the product of two functions that do not fit a substitution pattern, [integration by parts](../integration-by-parts/) is generally the appropriate alternative. For integrands that are rational functions of $\sin x$ and $\cos x$, the [Weierstrass substitution](../weierstrass-substitution/) provides a systematic route.
