---
title: Integration by Parts
source: https://algebrica.org/integration-by-parts/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - definite-integral
  - indefinite-integral
  - integration
  - integration-by-parts
  - liate-rule
  - product-rule
  - trigonometric-integrals
---
## The method of integration by parts

Integration by parts is a technique that rewrites the integral of the product of two [functions](../functions/) in a more tractable form by transferring a derivative from one factor to the other. For [indefinite integrals](../indefinite-integrals/), the formula reads:

$$\int f(x)g'(x) \ dx = f(x)g(x) - \int f'(x)g(x) \ dx + c$$

For [definite integrals](../definite-integrals/), the formula extends as:

$$\int_a^b f(x)g'(x) \ dx = [f(x)g(x)]_a^b - \int_a^b f'(x)g(x) \ dx$$

The bracket $[f(x)g(x)]_a^b = f(b)g(b) - f(a)g(a)$ is the boundary term and must be evaluated explicitly. In both cases, $f$ and $g$ are assumed to be differentiable on the [interval](../intervals/) of integration. The method is conceptually simple, but it requires practice to identify which factor should be differentiated and which should be integrated in order to simplify the expression.

> Integration by parts is sometimes applied more than once before the integral resolves. Repeated applications must be carried out with care, since each step increases the length of the computation and the likelihood of sign errors.

## Derivation of the formula

The integration by parts formula follows from the product rule for [derivatives](../derivatives/). The starting point is the identity:

$$\frac{d}{dx}(f(x)g(x)) = f'(x)g(x) + f(x)g'(x)$$

Integrating both sides with respect to $x$ gives:

$$\int \frac{d}{dx}(f(x)g(x)) \ dx = \int f'(x)g(x) \ dx + \int f(x)g'(x) \ dx$$

The left-hand side is the integral of a derivative, which returns the original function up to a constant:

$$f(x)g(x) = \int f'(x)g(x) \ dx + \int f(x)g'(x) \ dx$$

Isolating the second integral on the left produces the integration by parts formula:

$$\int f(x)g'(x) \ dx = f(x)g(x) - \int f'(x)g(x) \ dx + c$$

In the compact notation $u = f(x)$, $dv = g'(x) \ dx$, the formula takes its familiar form:

$$\int u \ dv = uv - \int v \ du$$

> The method is most effective when differentiating one factor makes it simpler, while the other can still be integrated without difficulty. Many problems can be reduced step by step until the residual integral matches a standard form.

## How to choose $u$ and $dv$

The method is effective only when the new integral $\int v \ du$ is simpler than the original. The outcome depends entirely on the assignment of $u$ and $dv$, so the choice is not arbitrary. A practical strategy is the following:

+ Choose $u$ as the factor that becomes simpler when differentiated.
+ Choose $dv$ as the remaining factor, so that $v = \int dv$ is easy to compute.

- - -

A useful order for the selection of $u$ is the hierarchy known by the acronym LIATE:

+ Logarithmic functions
+ Inverse trigonometric functions
+ Algebraic expressions
+ Trigonometric functions
+ Exponential functions

The ordering reflects how these functions behave under differentiation. [Logarithmic](../logarithmic-function/) and inverse trigonometric functions simplify considerably when differentiated, which makes them natural candidates for $u$. [Exponential functions](../exponential-function/), by contrast, remain essentially unchanged after differentiation and are generally better assigned to $dv$.

> Choosing $u$ according to this hierarchy frequently reduces the complexity of the remaining integral after a single application of the formula.

## Most common mistakes

A few recurring errors are worth keeping in mind when applying integration by parts.

The first error is the careless choice of $dv$. Assigning to $dv$ a factor whose antiderivative $v$ is harder to compute than the original integrand often makes the problem worse rather than better. When the resulting $\int v \ du$ is more complex than the starting integral, the assignment should be reconsidered before proceeding.

In the [definite integral](../definite-integrals/) version of the formula, the boundary term $[uv]_a^b$ must be evaluated explicitly. Omitting it is among the most common sources of incorrect results, particularly when the computation spans several lines and attention drifts toward the integral that follows.

Sign errors during differentiation are especially insidious in cyclic cases, where $\sin(x)$ and $\cos(x)$ alternate and a misplaced minus sign propagates through the entire calculation. Tracking signs at each step, rather than reconstructing them at the end, saves considerable time and prevents errors that are difficult to spot in hindsight.

In the indefinite case, the constant of integration $c$ must appear in the final result. After repeated applications of the formula the constant is easy to lose, particularly when intermediate integrals are written without it. A reliable habit is to carry $c$ explicitly only in the last step and to confirm its presence before writing the answer.

## Example 1

Consider the following integral:

$$\int x^2 \ln(x) \ dx$$

The integrand is a product of a logarithmic function and a [power](../powers/) of $x$. Following the LIATE hierarchy, $\ln(x)$ takes priority and is assigned to $f$, while $x^2$ is assigned to $g'$:

$$f(x) = \ln(x) \quad \rightarrow \quad f'(x) = \frac{1}{x}$$

$$g'(x) = x^2 \quad \rightarrow \quad g(x) = \frac{x^3}{3}$$

Applying the formula gives:

$$
\begin{align}
\int x^2 \ln(x) \ dx &= \ln(x) \cdot \frac{x^3}{3} - \int \frac{1}{x} \cdot \frac{x^3}{3} \ dx + c \\[6pt]
                    &= \ln(x) \cdot \frac{x^3}{3} - \int \frac{x^2}{3} \ dx + c
\end{align}
$$

The remaining integral falls under the power rule and is considerably simpler than the original. Completing the calculation yields:

$$\ln(x) \cdot \frac{x^3}{3} - \frac{x^3}{9} + c$$

Factoring $x^3/3$ produces the final result in compact form:

$$\int x^2 \ln(x) \ dx = \frac{x^3}{3}\left(\ln(x) - \frac{1}{3}\right) + c$$

## Example 2

Some integrals do not resolve after a single application of integration by parts. A repeated application can return the original integral, and what looks at first like a failure becomes the starting point for an algebraic resolution. Consider the integral:

$$\int e^x \sin(x) \ dx$$

Denote the integral by $I$:

$$I = \int e^x \sin(x) \ dx$$

Following the LIATE hierarchy, the trigonometric function $\sin(x)$ takes priority over the exponential, so $u = \sin(x)$ and $dv = e^x \ dx$ are the natural assignments, from which:

$$du = \cos(x) \ dx \qquad v = e^x$$

Applying the formula gives:

$$I = e^x \sin(x) - \int e^x \cos(x) \ dx$$

The new integral is no simpler in structure than the original, since it still involves the product of $e^x$ and a trigonometric function. A second application of integration by parts is needed. Denoting:

$$J = \int e^x \cos(x) \ dx$$

and keeping consistent with the previous choice, $u = \cos(x)$ and $dv = e^x \ dx$, from which:

$$du = -\sin(x) \ dx \qquad v = e^x$$

This yields:

$$J = e^x \cos(x) + \int e^x \sin(x) \ dx = e^x \cos(x) + I$$

The original integral $I$ has reappeared. Substituting back into the expression for $I$:

$$I = e^x \sin(x) - (e^x \cos(x) + I)$$

Both occurrences of $I$ now appear in the same equation. Collecting them on the left-hand side gives:

$$2I = e^x \sin(x) - e^x \cos(x)$$

Dividing through by $2$ and adding the constant of integration produces the result:

$$I = \frac{e^x}{2}(\sin(x) - \cos(x)) + c$$

> The cyclic structure converts an apparently endless recursion into a [linear equation](../linear-equations/) in $I$, which can be solved directly. The same technique applies whenever repeated integration by parts returns the original integral with a nonzero coefficient.

## Example 3

This example illustrates the definite integral version of the formula. Compute:

$$\int_0^1 x \ln(x) \ dx$$

The integrand is a product of a logarithmic function and a power of $x$. Following the LIATE hierarchy, $\ln(x)$ takes priority and is assigned to $f$, while $x$ is assigned to $g'$:

$$f(x) = \ln(x) \quad \rightarrow \quad f'(x) = \frac{1}{x}$$

$$g'(x) = x \quad \rightarrow \quad g(x) = \frac{x^2}{2}$$

Applying the definite integral form of the formula gives:

$$
\begin{align}
\int_0^1 x \ln(x) \ dx &= \left[\frac{x^2}{2}\ln(x)\right]_0^1 - \int_0^1 \frac{x^2}{2} \cdot \frac{1}{x} \ dx \\[6pt]
                      &= \left[\frac{x^2}{2}\ln(x)\right]_0^1 - \frac{1}{2}\int_0^1 x \ dx
\end{align}
$$

The boundary term requires care at $x = 0$. Since $\ln(1) = 0$ and $x^2\ln(x) \to 0$ as $x \to 0^+$, both endpoints vanish:

$$\left[\frac{x^2}{2}\ln(x)\right]_0^1 = 0$$

The remaining integral falls under the power rule:

$$\frac{1}{2}\int_0^1 x \ dx = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}$$

The final result is therefore:

$$\int_0^1 x \ln(x) \ dx = -\frac{1}{4}$$

> The [limit](../limits/) $\lim_{x \to 0^+} x^2 \ln(x) = 0$ holds because [polynomial](../polynomials/) growth dominates [logarithmic](../logarithms/) decay near zero. The same boundary analysis is required whenever the integrand is not defined at one of the endpoints.

## Decision procedure

The following stepwise procedure summarises the application of integration by parts to a generic integral involving a product of two factors.

+ Identify the integrand as a product $f(x) \cdot g'(x)$ of two functions. If the integrand is not in this form, simplify it first by expansion, factoring, application of [trigonometric identities](../trigonometric-identities/), or [partial fractions](../partial-fraction-decomposition/), and restart from the simplified expression.
+ Choose $u$ and $dv$ according to the LIATE hierarchy. The factor $u$ is assigned to the function that appears first among logarithmic, inverse trigonometric, algebraic, trigonometric, and exponential functions. The remaining factor is assigned to $dv$.
+ Compute the derivative $f'(x)$ of $u$ and the antiderivative $g(x)$ of $dv$.
+ Apply the formula in its appropriate form:

$$\int f(x)g'(x) \ dx = f(x)g(x) - \int f'(x)g(x) \ dx + c$$

+ Examine the new integral $\int f'(x)g(x) \ dx$. Three outcomes are possible:

The first outcome is that the new integral is more complex than the original. In this case, swap the roles of $u$ and $dv$ and reapply the formula. The aim of the method is always to produce a simpler remaining integral.

The second outcome is that the original integral reappears, possibly after a second application of the formula. The integral $I$ then satisfies a [linear equation](../linear-equations/) with a nonzero coefficient on $I$, which can be solved directly by isolating $I$ and dividing by the coefficient.

The third outcome is that the new integral can be evaluated by a standard formula or by a further application of integration by parts. In the definite case, the boundary term $[f(x)g(x)]_a^b = f(b)g(b) - f(a)g(a)$ must be evaluated explicitly, and the final result is a numerical value. In the indefinite case, the antiderivative is written as $f(x)g(x) - \int f'(x)g(x) \ dx + c$, with the constant of integration added explicitly at the last step to avoid omissions.

> When the integrand contains a rational expression in $\sin x$ and $\cos x$ rather than a clear product, integration by parts is often not the right tool. The [Weierstrass substitution](../weierstrass-substitution/) and direct trigonometric substitutions $u = \sin x$ or $u = \cos x$ are typically more efficient in those cases.
