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
## Definition

An [exponential function](../exponential-function/) is a function of the form $e^x$ or $\alpha^x$, with $\alpha > 0$ and $\alpha \neq 1$. The number $e$ occupies a central position in analysis because it is the only base for which the exponential function reproduces itself under differentiation. For a general exponential function $\alpha^x$ with $\alpha > 0$, differentiation introduces an additional factor:

$$\frac{d}{dx}\alpha^x = \alpha^x \ln \alpha$$

The [logarithmic](../logarithms/) term reflects how the chosen base scales the growth of the function. There is exactly one case in which this extra factor disappears. When $\ln \alpha = 1$, the derivative reduces to the function itself:

$$\frac{d}{dx}\alpha^x = \alpha^x$$

The unique number satisfying this condition is $e \approx 2.718$. The function $e^x$ is therefore the only exponential function that remains unchanged by differentiation, and the same property extends to integration. This structural feature explains why $e$ plays such a fundamental role in calculus. The computation of the [integral](../indefinite-integrals/) of an exponential function reduces to two distinct cases, according to whether the base is $e$ or a generic positive number $\alpha \neq 1$. The integral of $e^x$ is given by:

$$\int e^x \ dx = e^x + c \tag{1}$$

The result follows from the fact that the [derivative](../derivatives/) of $e^x$ is itself $e^x$. Differentiating the right-hand side gives:

$$\frac{d}{dx}\left[e^x + c\right] = \frac{d}{dx}e^x + \frac{d}{dx}c = e^x + 0 = e^x$$

which confirms that $e^x + c$ is indeed an antiderivative of $e^x$. The integral of $\alpha^x$ is given by:

$$\int \alpha^x \ dx = \frac{1}{\ln \alpha} \cdot \alpha^x + c \tag{2}$$

A direct verification confirms the formula:

$$\frac{d}{dx}\left[ \frac{1}{\ln \alpha} \cdot \alpha^x + c \right] = \frac{1}{\ln \alpha} \cdot (\ln \alpha \cdot \alpha^x) = \alpha^x$$

The factor $1/\ln \alpha$ compensates exactly for the logarithmic term produced by differentiation, and the result reduces to the original integrand.

## Canonical forms of exponential integrals

The following table collects the antiderivatives of the standard exponential integrands, with the integrand on the left and the corresponding antiderivative on the right. The constants $a$ and $b$ are real, with $a \neq 0$, and $\alpha > 0$ with $\alpha \neq 1$. In the last row, $f(x)$ is any differentiable function. These forms cover the cases most commonly encountered in integration problems.

[class="table-1"]

|    |                                            |                                                                |
| -- | ------------------------------------------ | -------------------------------------------------------------- |
| 1. | $$\int e^x \ dx$$                          | $$e^x + c$$                                                    |
| 2. | $$\int \alpha^x \ dx$$                     | $$\dfrac{1}{\ln \alpha} \alpha^x + c$$                         |
| 3. | $$\int e^{ax + b} \ dx$$                   | $$\dfrac{1}{a} e^{ax + b} + c$$                                |
| 4. | $$\int \alpha^{ax + b} \ dx$$              | $$\dfrac{1}{a \ln \alpha} \alpha^{ax + b} + c$$                |
| 5. | $$\int e^{f(x)} f'(x) \ dx$$               | $$e^{f(x)} + c$$                                               |

[/class]

> Each formula shows that integration preserves the exponential structure of the integrand. The antiderivative differs from the original function only by a multiplicative constant that depends on the coefficients appearing in the exponent or on the base of the power.

## Example 1

Consider the following integral:

$$\int (e^x + 3^x) \ dx$$

By the linearity property of the [indefinite integral](../indefinite-integrals/), the integral of a sum equals the sum of the integrals:

$$\int (f(x) + g(x)) \ dx = \int f(x) \ dx + \int g(x) \ dx$$

Applying this property, the integral decomposes as:

$$\int (e^x + 3^x) \ dx = \int e^x \ dx + \int 3^x \ dx$$

The first integral follows directly from formula $(1)$:

$$\int e^x \ dx = e^x + c$$

The second integral follows from formula $(2)$ with $\alpha = 3$:

$$\int 3^x \ dx = \frac{1}{\ln 3} \cdot 3^x + c$$

Combining the two contributions:

$$\int (e^x + 3^x) \ dx = e^x + \frac{1}{\ln 3} \cdot 3^x + c$$

> The antiderivative is the sum of two exponential terms, each governed by its own base.

## Exponential with a linear argument

A frequent situation in applications is an exponential whose argument is a linear function $ax + b$, with $a \neq 0$. The corresponding integration formula is:

$$\int e^{ax + b} \ dx = \frac{1}{a} e^{ax + b} + c$$

The factor $1/a$ compensates for the coefficient that the [chain rule](../the-derivative-of-a-composite-function/) introduces upon differentiation. A direct verification yields:

$$\frac{d}{dx}\left[ \frac{1}{a} e^{ax + b} + c \right] = \frac{1}{a} \cdot a \cdot e^{ax + b} = e^{ax + b}$$

which coincides with the original integrand.

When the exponent is a differentiable function $f(x)$, the formula generalises through [integration by substitution](../integration-by-substitution/):

$$\int e^{f(x)} \cdot f'(x) \ dx = e^{f(x)} + c$$

The integrand must contain the exponential $e^{f(x)}$ multiplied by the derivative of its exponent. Under this condition the integration is immediate and the antiderivative is $e^{f(x)} + c$. When the factor $f'(x)$ is not present in the integrand, an algebraic manipulation or a suitable substitution is required before the rule can be applied.

The same reasoning extends to exponential functions with an arbitrary base $\alpha$. When the exponent is $ax + b$ rather than $x$, differentiation produces two factors: the coefficient $a$ from the exponent and $\ln \alpha$ from the base. The corresponding formula is:

$$\int \alpha^{ax + b} \ dx = \frac{1}{a \ln \alpha} \alpha^{ax + b} + c$$

A direct differentiation of the right-hand side confirms the result. Expressions of this type frequently appear in intermediate steps when more complicated integrals are reduced to their elementary components.

## Example 2

Consider the following integral, which involves a product of two exponential terms with different bases:

$$\int 8^x \cdot 2^{-3x + 4} \ dx$$

The integrand can be simplified by applying the [properties of powers](../powers/). The exponent of $2$ in the second factor splits as:

$$2^{-3x + 4} = 2^{-3x} \cdot 2^4 = 16 \cdot 2^{-3x}$$

Substituting this identity into the integral and extracting the constant $16$ by linearity:

$$\int 8^x \cdot 2^{-3x + 4} \ dx = 16 \int 8^x \cdot 2^{-3x} \ dx$$

The base $8$ can be rewritten as a power of $2$, since $8 = 2^3$. The integrand then reduces to a single power of $2$:

$$
\begin{align}
16 \int 8^x \cdot 2^{-3x} \ dx &= 16 \int (2^3)^x \cdot 2^{-3x} \ dx \\[6pt]
                               &= 16 \int 2^{3x} \cdot 2^{-3x} \ dx \\[6pt]
                               &= 16 \int 2^{3x - 3x} \ dx \\[6pt]
                               &= 16 \int 1 \ dx
\end{align}
$$

The integral of the constant function $1$ is $x + c$, so the final result is:

$$\int 8^x \cdot 2^{-3x + 4} \ dx = 16x + c$$

> The apparent complexity of the original integrand disappears once the two exponential factors are reduced to the same base, and the integral collapses to that of a constant.

## Example 3

Consider the following integral, in which both factors are exponentials with linear arguments and related bases:

$$\int 9^{x - 1} \cdot 3^{-x + 2} \ dx$$

The two exponents can be separated by means of the properties of powers:

$$9^{x - 1} \cdot 3^{-x + 2} = 9^x \cdot 9^{-1} \cdot 3^{-x} \cdot 3^2$$

Since $3^2 = 9$, the factor $9^{-1} \cdot 9$ reduces to $1$ and the integrand simplifies to:

$$9^x \cdot 3^{-x}$$

Rewriting $9^x$ as $3^{2x}$, the product of the two exponential factors with base $3$ collapses into a single power:

$$9^x \cdot 3^{-x} = 3^{2x} \cdot 3^{-x} = 3^{2x - x} = 3^x$$

The integral therefore reduces to the canonical form $\int \alpha^x \ dx$ with $\alpha = 3$:

$$\int 9^{x - 1} \cdot 3^{-x + 2} \ dx = \int 3^x \ dx$$

Applying formula $(2)$, the final result is:

$$\int 9^{x - 1} \cdot 3^{-x + 2} \ dx = \frac{1}{\ln 3} \cdot 3^x + c$$

> The reduction to a common base is the key step: once both factors are expressed as powers of $3$, the integrand becomes a single exponential and the integration is immediate.

## Example 4

Consider the following integral:

$$\int e^{3x - 2} \ dx$$

The exponent is a linear function of $x$, so the standard rule for exponentials of the form $e^{ax + b}$ applies directly. The derivative of $3x - 2$ is $3$, and the compensating factor in the antiderivative is therefore $1/3$:

$$\int e^{3x - 2} \ dx = \frac{1}{3} e^{3x - 2} + c$$

A direct differentiation of the right-hand side confirms the result:

$$\frac{d}{dx}\left[ \frac{1}{3} e^{3x - 2} + c \right] = \frac{1}{3} \cdot 3 \cdot e^{3x - 2} = e^{3x - 2}$$

The differentiation recovers the original integrand, so the antiderivative is consistent with the integration rule.

## A common oversight

A frequent source of error in the integration of exponential functions arises when the exponent carries a coefficient different from $1$. A common incorrect formulation is:

$$\int e^{3x - 2} \ dx = e^{3x - 2} + c$$

in which the factor $1/3$ has been omitted. The mistake is identified by differentiating the proposed antiderivative:

$$\frac{d}{dx} e^{3x - 2} = 3 e^{3x - 2}$$

The result is three times the original integrand, which shows that $e^{3x - 2}$ alone is not an antiderivative of itself. Whenever the exponent has the form $ax + b$ with $a \neq 1$, the compensating factor $1/a$ must appear in the antiderivative, since the chain rule introduces the multiplicative constant $a$ upon differentiation.

## Example 5

Consider the following integral, in which the exponent is no longer a linear function of $x$:

$$\int x \ e^{x^2} \ dx$$

The exponent $x^2$ is a quadratic function, so the rule for exponentials of the form $e^{ax + b}$ cannot be applied directly. The structure of the integrand, however, suggests the appropriate strategy. The derivative of $x^2$ is $2x$, and a factor $x$ is already present in the integrand. Multiplying and dividing by $2$ introduces the missing constant without altering the value of the integral:

$$\int x \ e^{x^2} \ dx = \frac{1}{2} \int 2x \ e^{x^2} \ dx$$

The integrand now matches the canonical form $e^{f(x)} f'(x)$ with $f(x) = x^2$, so formula $(5)$ of the canonical table applies and the integration is immediate:

$$\int x \ e^{x^2} \ dx = \frac{1}{2} e^{x^2} + c$$

A direct differentiation of the right-hand side confirms the result:

$$\frac{d}{dx}\left[ \frac{1}{2} e^{x^2} + c \right] = \frac{1}{2} \cdot 2x \cdot e^{x^2} = x e^{x^2}$$

> The differentiation recovers the original integrand, which validates the antiderivative obtained.

## When the matching factor is missing

The role of the factor $x$ in the previous example becomes evident when it is removed. The integral:

$$\int e^{x^2} \ dx$$

does not admit an antiderivative expressible in terms of elementary functions. Its value is conventionally written in terms of the error function $\operatorname{erf}(x)$, defined by:

$$\operatorname{erf}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{-t^2} \ dt$$

The function $\operatorname{erf}(x)$ is not elementary, in the sense that it cannot be obtained from polynomials, exponentials, logarithms, and trigonometric functions through a finite combination of algebraic operations, compositions, and inversions. It was introduced precisely because the integrand $e^{-t^2}$ has no elementary antiderivative, even though the function itself is perfectly regular and infinitely differentiable.

The comparison with the previous example clarifies the role of the factor $x$. In $\int x \ e^{x^2} \ dx$ the factor $x$ provides, up to the constant $1/2$, the derivative of the exponent $x^2$. The integrand matches the canonical form $e^{f(x)} f'(x)$, and the antiderivative is elementary. When the factor $x$ is absent, the matching is lost and the integral falls outside the class of integrals solvable through elementary techniques.

> When a closed-form expression is not available, the value of the corresponding [definite integral](../definite-integrals/) can still be approximated through [numerical integration](../numerical-integration/), which is the standard route for $\int e^{-x^2} \ dx$ over a finite interval.

## Integration by parts with exponential factors

Several integrals involving the exponential function cannot be reduced to a canonical form through algebraic manipulation alone. When the integrand is the product of an exponential and a polynomial, or of an exponential and another transcendental function, the technique of [integration by parts](../integration-by-parts/) provides a systematic approach. The method is based on the formula:

$$\int u(x) v'(x) \ dx = u(x) v(x) - \int u'(x) v(x) \ dx$$

The choice of $u(x)$ and $v'(x)$ is the decisive step. When an exponential factor is present, it is generally convenient to take $v'(x) = e^{ax + b}$, since the exponential is invariant under integration up to a multiplicative constant, while the remaining factor is differentiated and progressively simplified.

- - -

The simplest case arises when the integrand is the product of a first-degree polynomial and an exponential. Consider the integral:

$$\int x \ e^x \ dx$$

Setting $u(x) = x$ and $v'(x) = e^x$, the derivatives and antiderivatives are $u'(x) = 1$ and $v(x) = e^x$. Substituting into the integration by parts formula:

$$\int x \ e^x \ dx = x \ e^x - \int e^x \ dx = x \ e^x - e^x + c$$

The final expression can be factored as:

$$\int x \ e^x \ dx = (x - 1) e^x + c$$

A direct differentiation confirms the result and recovers the original integrand:

$$\frac{d}{dx}\left[ (x - 1) e^x + c \right] = e^x + (x - 1) e^x = x \ e^x$$

- - -

When the [polynomial](../polynomials/) factor has degree greater than $1$, a single application of the formula is not sufficient and the procedure must be iterated. Consider the integral:

$$\int x^2 \ e^x \ dx$$

Setting $u(x) = x^2$ and $v'(x) = e^x$, the first application of the formula yields:

$$\int x^2 \ e^x \ dx = x^2 \ e^x - \int 2x \ e^x \ dx$$

The remaining integral has the same structure as the previous example and has already been computed. Substituting the result:

$$\int x^2 \ e^x \ dx = x^2 \ e^x - 2(x - 1) e^x + c = (x^2 - 2x + 2) e^x + c$$

The same reasoning extends to any polynomial $P(x)$ of degree $n$. After $n$ successive applications of integration by parts, the polynomial factor is reduced to a constant and the integration terminates. The general recurrence relation is:

$$\int x^n \ e^x \ dx = x^n \ e^x - n \int x^{n - 1} \ e^x \ dx$$

which expresses the integral of $x^n e^x$ in terms of the integral of $x^{n - 1} e^x$, and produces a closed-form antiderivative in a finite number of steps.

- - -

A further variation occurs when the exponent of the exponential is itself a linear function of $x$. The same technique applies, with the only adjustment being the compensating factor $1/a$ in the antiderivative of $e^{ax + b}$. Consider the integral:

$$\int x \ e^{2x} \ dx$$

Setting $u(x) = x$ and $v'(x) = e^{2x}$, the antiderivative of $v'(x)$ is $v(x) = \tfrac{1}{2} e^{2x}$. The integration by parts formula gives:

$$\int x \ e^{2x} \ dx = \frac{x}{2} e^{2x} - \int \frac{1}{2} e^{2x} \ dx = \frac{x}{2} e^{2x} - \frac{1}{4} e^{2x} + c$$

Factoring the common exponential term, the final result is:

$$\int x \ e^{2x} \ dx = \frac{1}{4} e^{2x} (2x - 1) + c$$

The presence of the coefficient $a = 2$ in the exponent does not change the structure of the procedure: it only introduces the factor $1/2$ at each integration step, which propagates into the final expression.

## Decision procedure

The following stepwise procedure summarises the choice of method for a generic exponential integral.

+ When the integrand is $e^x$ or $\alpha^x$ with constant base, apply the corresponding formula directly: $\int e^x \ dx = e^x + c$ or $\int \alpha^x \ dx = \tfrac{1}{\ln \alpha} \alpha^x + c$.
+ When the exponent is a linear function $ax + b$, use the compensating factor: $\int e^{ax + b} \ dx = \tfrac{1}{a} e^{ax + b} + c$ for the natural base, or $\int \alpha^{ax + b} \ dx = \tfrac{1}{a \ln \alpha} \alpha^{ax + b} + c$ for a generic base.
+ When the exponent is a differentiable function $f(x)$ and the integrand contains $f'(x)$, possibly up to a multiplicative constant, adjust the constant if necessary and apply $\int e^{f(x)} f'(x) \ dx = e^{f(x)} + c$.
+ When the integrand is a product of an exponential and a polynomial $P(x)$, apply integration by parts with $u(x) = P(x)$ and $v'(x) = e^{ax + b}$. When the polynomial has degree $n > 1$, the procedure is iterated and each application reduces the degree by one until a constant remains.
+ When the integrand is a product of two exponentials with related bases, apply the properties of powers to reduce both factors to a common base, simplify, and return to one of the previous cases.
+ When none of the above applies, the integral may not admit a closed form in terms of elementary functions. Integrals such as $\int e^{x^2} \ dx$ or $\int e^x/x \ dx$ are written in terms of special functions like the error function $\operatorname{erf}(x)$ or the exponential integral $\operatorname{Ei}(x)$, and their definite versions are best approached through [numerical integration](../numerical-integration/).
