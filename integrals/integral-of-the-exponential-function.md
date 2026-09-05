---
title: Integral of the Exponential Function
source: https://algebrica.org/integral-of-the-exponential-function/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - chain-rule
  - error-function
  - exponential-function
  - indefinite-integral
  - integration
  - integration-by-parts
  - integration-by-substitution
  - linearity
  - logarithms
---

## A reminder about the exponential function

An [exponential function](../exponential-function/) is a function of the form $e^x$ or $\alpha^x,$ with $\alpha > 0$ and $\alpha \neq 1.$ The number $e$ has a central role in analysis because it is the only base for which the [derivative](../derivatives/) of the exponential function is the function itself. For a general exponential function $\alpha^x$ with $\alpha > 0,$ differentiation introduces an additional factor:

$$\frac{d}{dx}\alpha^x = \alpha^x \ln \alpha$$

The [logarithmic](../logarithms/) term expresses how the choice of base affects the growth of the function. This factor disappears in just one case, when $\ln \alpha = 1$ and the derivative equals the function itself:

$$\frac{d}{dx}\alpha^x = \alpha^x$$

The only number satisfying this condition is $e,$ so $e^x$ is the only exponential function that remains unchanged under differentiation, and the same property extends to integration. This explains the role of $e$ in differential and integral calculus.

- - -

To evaluate the [integral](../indefinite-integrals/) of an exponential function, we distinguish two cases, according to whether the base is $e$ or a general positive number $\alpha \neq 1.$ The integral of $e^x$ is straightforward and is given by:

$$\int e^x \ dx = e^x + c \tag{1}$$

Differentiating the right-hand side gives:

$$\frac{d}{dx}\left[e^x + c\right] = \frac{d}{dx}e^x + \frac{d}{dx}c = e^x + 0 = e^x$$

We have thus verified that $e^x + c$ is an antiderivative of $e^x.$ The integral of $\alpha^x$ is instead given by:

$$\int \alpha^x \ dx = \frac{1}{\ln \alpha} \cdot \alpha^x + c \tag{2}$$

We can also verify this formula directly as follows:

$$\frac{d}{dx}\left[ \frac{1}{\ln \alpha} \cdot \alpha^x + c \right] = \frac{1}{\ln \alpha} \cdot (\ln \alpha \cdot \alpha^x) = \alpha^x$$

The factor $1/\ln \alpha$ compensates for the logarithmic term introduced by differentiation, so we recover the original integrand.

## Canonical forms of exponential integrals

The following table lists the antiderivatives of the most common exponential forms, with the integral on the left and the corresponding antiderivative on the right. The constants $a$ and $b$ are real, with $a \neq 0,$ while $\alpha > 0$ and $\alpha \neq 1.$ In the last row, $f(x)$ is any differentiable function. These forms cover the cases we encounter most often in integration exercises.

[class="table-1"]

|    |                                            |                                                                |
| -- | ------------------------------------------ | -------------------------------------------------------------- |
| 1. | $$\int e^x \ dx$$                          | $$e^x + c$$                                                    |
| 2. | $$\int \alpha^x \ dx$$                     | $$\dfrac{1}{\ln \alpha} \alpha^x + c$$                         |
| 3. | $$\int e^{ax + b} \ dx$$                   | $$\dfrac{1}{a} e^{ax + b} + c$$                                |
| 4. | $$\int \alpha^{ax + b} \ dx$$              | $$\dfrac{1}{a \ln \alpha} \alpha^{ax + b} + c$$                |
| 5. | $$\int e^{f(x)} f'(x) \ dx$$               | $$e^{f(x)} + c$$                                               |

[/class]

> Observe that integration preserves the exponential form in each of these formulas. Apart from the constant of integration, the exponential term in the antiderivative differs from the original exponential term only by a constant factor, which depends on the coefficients in the exponent or on the base of the power.

## Example 1

As a first example, we evaluate the following integral:

$$\int (e^x + 3^x) \ dx$$

By the [linearity](../integration-strategies/) of the [indefinite integral](../indefinite-integrals/), the integral of a sum equals the sum of the integrals, so we can rewrite it as:

$$\int (e^x + 3^x) \ dx = \int e^x \ dx + \int 3^x \ dx$$

The first integral follows directly from formula $(1)$ and equals $e^x + c.$ For the second integral, we use formula $(2)$ with $\alpha = 3$ to obtain:

$$\int 3^x \ dx = \frac{1}{\ln 3} \cdot 3^x + c$$

Adding the two contributions gives:

$$e^x + \frac{1}{\ln 3} \cdot 3^x + c$$

## Exponential with a linear argument

In applications, we often encounter exponentials whose argument is a linear function $ax + b,$ with $a \neq 0.$ In such cases, the corresponding integration formula is:

$$\int e^{ax + b} \ dx = \frac{1}{a} e^{ax + b} + c \tag{3}$$

The factor $1/a$ compensates for the coefficient introduced by the [chain rule](../chain-rule/). To verify this, we differentiate the right-hand side and obtain:

$$\frac{d}{dx}\left[ \frac{1}{a} e^{ax + b} + c \right] = \frac{1}{a} \cdot a \cdot e^{ax + b} = e^{ax + b}$$

As expected, the result equals the original integrand. When the exponent is a differentiable function $f(x),$ we can generalise formula $(3)$ through [integration by substitution](../integration-by-substitution/):

$$\int e^{f(x)} \cdot f'(x) \ dx = e^{f(x)} + c$$

The integrand must contain the exponential $e^{f(x)}$ multiplied by the derivative of its exponent. In this situation, integration is immediate and the antiderivative is $e^{f(x)} + c.$ If the factor $f'(x)$ is absent from the integrand, we must first use an algebraic manipulation or a suitable substitution to obtain this form before applying the rule.

The same reasoning extends to exponential functions with a general base $\alpha.$ When the exponent is $ax + b$ rather than $x,$ differentiation produces two factors, the coefficient $a$ from the exponent and $\ln \alpha$ from the base. We therefore obtain the following formula:

$$\int \alpha^{ax + b} \ dx = \frac{1}{a \ln \alpha} \alpha^{ax + b} + c$$

Expressions of this type often appear in intermediate steps when we break down more complicated integrals in an attempt to reduce them to elementary ones.

## Example 2

We evaluate the following integral, which contains the product of two exponential terms with different bases:

$$\int 8^x \cdot 2^{-3x + 4} \ dx$$

We can simplify the integrand using the [properties of powers](../powers/). In the second factor, we separate the terms in the exponent of $2$ and write:

$$2^{-3x + 4} = 2^{-3x} \cdot 2^4 = 16 \cdot 2^{-3x}$$

Substituting this identity into the integral and taking the constant outside gives:

$$\int 8^x \cdot 2^{-3x + 4} \ dx = 16 \int 8^x \cdot 2^{-3x} \ dx$$

We can rewrite the base $8$ as a power of $2,$ so that the integrand reduces to a single power of $2:$

$$
\begin{align}
16 \int 8^x \cdot 2^{-3x} \ dx &= 16 \int (2^3)^x \cdot 2^{-3x} \ dx \\[6pt]
                               &= 16 \int 2^{3x} \cdot 2^{-3x} \ dx \\[6pt]
                               &= 16 \int 2^{3x - 3x} \ dx \\[6pt]
                               &= 16 \int 1 \ dx\\[6pt]
                               &= 16x + c
\end{align}
$$

> As we have seen, once both exponential factors are written with the same base, the integrand simplifies and all that remains is to integrate a constant.

## Example 3

We next consider the following integral, in which both factors are exponentials with linear arguments and bases that can be reduced to a common base:

$$\int 9^{x - 1} \cdot 3^{-x + 2} \ dx$$

Using the properties of powers, we can separate the terms in each exponent and write:

$$9^{x - 1} \cdot 3^{-x + 2} = 9^x \cdot 9^{-1} \cdot 3^{-x} \cdot 3^2$$

A straightforward calculation reduces the integrand to:

$$9^x \cdot 3^{-x}$$

Rewriting $9^x$ as $3^{2x},$ we can combine the two exponential factors with base $3$ into a single power:

$$9^x \cdot 3^{-x} = 3^{2x} \cdot 3^{-x} = 3^{2x - x} = 3^x$$

The integral therefore reduces to the canonical form $\int \alpha^x \ dx$ with $\alpha = 3:$

$$\int 9^{x - 1} \cdot 3^{-x + 2} \ dx = \int 3^x \ dx$$

Applying formula $(2)$ gives the result:

$$\frac{1}{\ln 3} \cdot 3^x + c$$

> When evaluating integrals of this kind, the main step is to reduce the factors to a common base. Once both factors are expressed as powers of the same base, the integrand becomes a single exponential and integration is immediate.

## Example 4

As a further example, we evaluate the following integral, in which the exponent is a linear function of $x:$

$$\int e^{3x - 2} \ dx$$

As we know, we can apply the rule for exponentials of the form $e^{ax + b}$ directly. The derivative of $3x - 2$ is $3,$ so we must include the factor $1/3$ in the antiderivative:

$$\int e^{3x - 2} \ dx = \frac{1}{3} e^{3x - 2} + c$$

We verify the result by differentiating the right-hand side:

$$\frac{d}{dx}\left[ \frac{1}{3} e^{3x - 2} + c \right] = \frac{1}{3} \cdot 3 \cdot e^{3x - 2} = e^{3x - 2}$$

Differentiation recovers the original integrand, so the antiderivative agrees with the integration rule.


## Example 5

We now consider the following integral, in which the exponent is a [quadratic function](../polynomial-function/) of $x$ rather than a linear one.

$$\int x e^{x^2} \ dx$$

In this case, we cannot directly apply the rule for exponentials of the form $e^{ax + b}.$ The form of the integrand, however, suggests how to proceed. The derivative of $x^2$ is $2x,$ and the integrand already contains a factor $x.$ Multiplying and dividing by $2$ introduces the missing constant without changing the value of the integral:

$$\int x e^{x^2} \ dx = \frac{1}{2} \int 2x e^{x^2} \ dx$$

The integrand now has the canonical form $e^{f(x)} f'(x)$ with $f(x) = x^2,$ so we can apply the formula in row $(5)$ of the table and integrate directly:

$$\int x e^{x^2} \ dx = \frac{1}{2} e^{x^2} + c$$

We verify the result by differentiating the right-hand side:

$$\frac{d}{dx}\left[ \frac{1}{2} e^{x^2} + c \right] = \frac{1}{2} \cdot 2x \cdot e^{x^2} = x e^{x^2}$$

Differentiation recovers the original integrand and therefore confirms the antiderivative obtained.

## When the derivative factor is missing

For completeness, we briefly turn to a more advanced topic. To understand the role of the factor $x$ in the previous example, we examine what happens if we remove it. The integral would become:

$$\int e^{x^2} \ dx$$

This integral has no antiderivative expressible in terms of elementary functions. Its antiderivatives are conventionally written in terms of the so-called imaginary error function $\mathrm{erfi}(x),$ defined by:

$$\mathrm{erfi}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{t^2} \ dt$$

This is not an elementary function, meaning that it cannot be obtained from polynomials, exponentials, logarithms, and trigonometric functions through a finite combination of algebraic operations. The [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/), however, allows us to find its derivative directly from the integral that defines it. Repeated differentiation also shows that it is [infinitely differentiable](../higher-order-derivatives/).

The comparison with Example $5$ clarifies the role of the factor $x.$ To recap, in the integral $\int x e^{x^2} \ dx,$ the factor $x$ supplies, up to the constant $1/2,$ the derivative of the exponent $x^2.$ The integrand has the canonical form $e^{f(x)} f'(x),$ and the antiderivative is elementary. When the factor $x$ is absent, this correspondence is lost, and the integral can no longer be evaluated by elementary techniques, placing it beyond our present scope.

> When no elementary closed form is available, we can still approximate the corresponding [definite integral](../definite-integrals/) using [numerical integration](../numerical-integration/), as in the case of $\int e^{x^2} \ dx$ over a [finite interval](../intervals/).

## Integration by parts with exponential factors

Several integrals involving the exponential function cannot be reduced to a canonical form by algebraic manipulation alone. When the integrand is the product of an exponential and a polynomial, or of an exponential and another [transcendental function](../functions/), [integration by parts](../integration-by-parts/) gives us a systematic method. The method is based on the formula:

$$\int u(x) v'(x) \ dx = u(x) v(x) - \int u'(x) v(x) \ dx$$

When an exponential factor is present, it is generally convenient to choose $v'(x) = e^{ax + b},$ since, as we know, integration leaves the exponential unchanged up to a constant factor, while the other factor is differentiated and progressively simplified.

- - -

The simplest case occurs when the integrand is the product of a first-degree polynomial and an exponential. For example, we evaluate the following integral:

$$\int x e^x \ dx$$

We set $u(x) = x$ and $v'(x) = e^x,$ which gives $u'(x) = 1$ and $v(x) = e^x.$ Substituting these expressions into the integration by parts formula gives:

$$\int x e^x \ dx = x e^x - \int e^x \ dx = x e^x - e^x + c$$

Factoring out the exponential gives:

$$\int x e^x \ dx = (x - 1) e^x + c$$

Differentiating the result directly recovers the original integrand and verifies the antiderivative:

$$\frac{d}{dx}\left[ (x - 1) e^x + c \right] = e^x + (x - 1) e^x = x e^x$$

- - -

When the [polynomial](../polynomials/) factor has degree greater than $1,$ one application of the formula is not enough, and we must repeat the procedure several times. Consider, for example, the following integral:

$$\int x^2 e^x \ dx$$

We set $u(x) = x^2$ and $v'(x) = e^x.$ The first application of the formula gives:

$$\int x^2 e^x \ dx = x^2 e^x - \int 2x e^x \ dx$$

The remaining integral has the same form as the one in the previous example, which we have already evaluated. Substituting that result gives:

$$\int x^2 e^x \ dx = x^2 e^x - 2(x - 1) e^x + c = (x^2 - 2x + 2) e^x + c$$

The same reasoning extends to any polynomial $P(x)$ of degree $n.$ After $n$ successive applications of integration by parts, the polynomial factor reduces to a constant and the calculation is complete. The [general recurrence relation](../reduction-formulas/) is:

$$\int x^n e^x \ dx = x^n e^x - n \int x^{n - 1} e^x \ dx$$

This equality expresses the integral of $x^n e^x$ in terms of that of $x^{n - 1} e^x$ and allows us to obtain an antiderivative in closed form in a finite number of steps.

- - -

A further variation occurs when the exponent is a linear function of $x.$ We can use the same method as above, remembering to include the factor $1/a$ in the antiderivative of $e^{ax + b}.$ We therefore evaluate the integral:

$$\int x e^{2x} \ dx$$

We set $u(x) = x$ and $v'(x) = e^{2x}.$ An antiderivative of $v'(x)$ is $v(x) = 1/2 \cdot e^{2x},$ and applying the integration by parts formula gives:

$$\int x e^{2x} \ dx = \frac{x}{2} e^{2x} - \int \frac{1}{2} e^{2x} \ dx = \frac{x}{2} e^{2x} - \frac{1}{4} e^{2x} + c$$

Factoring out the exponential term gives the result:

$$\frac{1}{4} e^{2x} (2x - 1) + c$$

The coefficient $a = 2$ in the exponent does not change the procedure. It simply introduces a factor $1/2$ at each integration step, whose effect appears in the final expression.
