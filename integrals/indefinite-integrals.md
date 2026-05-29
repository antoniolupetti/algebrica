---
title: Indefinite Integrals
source: https://algebrica.org/indefinite-integrals/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - definite-integral
  - fundamental-theorem-of-calculus
  - indefinite-integral
  - integration
  - integration-rules
  - linearity
  - power-rule
  - primitive
---
## Primitives

Differentiation assigns to each function a unique [derivative](../derivatives/) by definition. The inverse problem asks whether, given a function $f(x)$, there exists a function $F(x)$ whose derivative is exactly $f(x)$. Such a function is called a primitive (or antiderivative) of $f$. 

**Definition 1.** $F(x)$ is a primitive of $f(x)$ on the [interval](../intervals/) $[a, b]$ when $F$ is differentiable throughout $[a, b]$ and the following identity holds:

$$F'(x) = f(x) \qquad \forall x \in [a, b]$$

Not every function admits a primitive on a given interval. A sufficient condition is [continuity](../continuous-functions/): every continuous function on a closed interval $[a, b]$ admits a primitive there. The converse does not hold in general. As an example, when $f(x) = 3x^2$, a primitive is $F(x) = x^3$, since:

$$\frac{d}{dx} x^3 = 3x^2$$

- - -

Unlike derivatives, primitives are not unique. Since the derivative of any constant is zero, the functions $x^3$, $x^3 + 5$, and $x^3 - \frac{1}{2}$ are all primitives of $3x^2$. More generally, if $F(x)$ is a primitive of $f(x)$, then so is $F(x) + c$ for any $c \in \mathbb{R}$, since:

$$\frac{d}{dx}[F(x) + c] = F'(x) = f(x)$$

Conversely, any two primitives of the same function differ by a constant. If $F_1(x)$ and $F_2(x)$ are both primitives of $f(x)$, then their difference has zero derivative:

$$\frac{d}{dx}[F_1(x) - F_2(x)] = F_1'(x) - F_2'(x) = f(x) - f(x) = 0$$

This forces $F_1(x) - F_2(x) = c$ for some constant $c \in \mathbb{R}$.

## What is the indefinite integral

**Definition 2.** The indefinite integral of a function $f(x)$ is the set of all its primitives. Since any two primitives differ by a constant, the entire family is written as $F(x) + c$ for $c \in \mathbb{R}$, and is denoted by the symbol:

$$\int f(x) \ dx = F(x) + c \qquad c \in \mathbb{R}$$

From this definition the following identity follows directly:

$$\frac{d}{dx}\left[\int f(x) \ dx\right] = f(x)$$

Differentiating an indefinite integral returns the original function. The precise formal connection between differentiation and integration, including its definite-integral counterpart, is the content of the [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/).

- - -

Find the primitive of $f(x) = 3x$ whose graph passes through the point $(2, 1)$. The general primitive is obtained by integrating:

$$F(x) = \int 3x \ dx = \frac{3}{2}x^2 + c$$

To determine the constant, the condition $F(2) = 1$ is imposed:

$$
\begin{align}
\frac{3}{2}(2)^2 + c &= 1 \\[6pt]
6 + c &= 1 \\[6pt]
c &= -5
\end{align}
$$

The unique primitive satisfying the given condition is:

$$F(x) = \frac{3}{2}x^2 - 5$$

## Linearity properties

The indefinite integral is a linear operator. The integral of a sum of integrable functions equals the sum of their integrals:

$$\int [f(x) + g(x)] \ dx = \int f(x) \ dx + \int g(x) \ dx \tag{1}$$

A constant factor can be moved outside the integral sign:

$$\int k f(x) \ dx = k \int f(x) \ dx \qquad \forall k \in \mathbb{R} \tag{2}$$

These two properties make the indefinite integral a linear map on the space of integrable functions, and they reduce the computation of integrals of linear combinations to the computation of integrals of the individual terms.

- - -

Compute the integral of $f(x) = 3x^2 + 2x$. Applying property $(1)$, the integral splits into two terms, each of which falls under the power rule:

$$\int (3x^2 + 2x) \ dx = \int 3x^2 \ dx + \int 2x \ dx$$

The two integration constants arising from each term combine into a single arbitrary constant, and the result is:

$$\int (3x^2 + 2x) \ dx = x^3 + x^2 + c \qquad c \in \mathbb{R}$$

- - -

Compute the integral of $f(x) = 5\sin(x)$. Applying property $(2)$, the constant factor is moved outside the integral:

$$\int 5\sin(x) \ dx = 5 \int \sin(x) \ dx$$

The integral of $\sin(x)$ is $-\cos(x)$, and therefore:

$$\int 5\sin(x) \ dx = -5\cos(x) + c \qquad c \in \mathbb{R}$$

## Integral of a power function

For every real exponent $a \neq -1$, the integral of the [power function](../powers/) $x^a$ is given by:

$$\int x^a \ dx = \frac{x^{a+1}}{a+1} + c$$

The case $a = -1$ produces a zero denominator and requires a separate treatment, discussed in the section on the logarithmic integral.

- - -

Compute the following integral:

$$\int (3x^4 + 5x^2) \ dx$$

Applying linearity, the constant factors are moved outside and the power rule is applied to each term:

$$\int (3x^4 + 5x^2) \ dx = 3 \int x^4 \ dx + 5 \int x^2 \ dx = 3 \cdot \frac{x^5}{5} + 5 \cdot \frac{x^3}{3} + c$$

The result is:

$$\int (3x^4 + 5x^2) \ dx = \frac{3}{5}x^5 + \frac{5}{3}x^3 + c \qquad c \in \mathbb{R}$$
- - -

Compute the following integral:

$$\int \left(4x^3 - \frac{3}{\sqrt{x}} + 2\cos x\right) dx$$

Applying linearity, the integral splits into three terms:

$$\int 4x^3 \ dx - \int 3x^{-1/2} \ dx + \int 2\cos x \ dx$$

The first term follows directly from the power rule: $\int 4x^3 \ dx = x^4$. For the second, rewriting $1/\sqrt{x}$ as $x^{-1/2}$ and applying the power rule with $a = -1/2$ gives $\int 3x^{-1/2} \ dx = 6\sqrt{x}$. The third term follows from the standard integral of the cosine: $\int 2\cos x \ dx = 2\sin x$. Assembling the three contributions:

$$\int \left(4x^3 - \frac{3}{\sqrt{x}} + 2\cos x\right) dx = x^4 - 6\sqrt{x} + 2\sin x + c$$

> The result can be verified by differentiating $x^4 - 6\sqrt{x} + 2\sin x + c$ term by term, which returns the original integrand.

## The logarithmic integral

When $a = -1$, the power rule formula produces a zero denominator and does not apply. The integral in this case is given by the [natural logarithm](../logarithms/) of the [absolute value](../absolute-value/):

$$\int \frac{1}{x} \ dx = \ln |x| + c$$

This identity follows from the fact that $\frac{d}{dx} \ln |x| = \frac{1}{x}$, which holds for every $x \neq 0$. The absolute value is necessary because $\ln$ is defined only for positive arguments, while $1/x$ is defined on both $(-\infty, 0)$ and $(0, +\infty)$.

> The identity $\int \frac{1}{x} \ dx = \ln|x| + c$ holds separately on $(-\infty, 0)$ and on $(0, +\infty)$. On each interval the arbitrary constant may take a different value, so the most general antiderivative of $1/x$ on its full domain is not a single expression $\ln|x| + c$ with one constant, but a piecewise family with independent constants on the two components.

## Fundamental integration rules

The four rules collected here are the foundation of every elementary integration procedure. Linearity reduces an integral of a linear combination to a sum of simpler integrals, the power rule covers all real exponents different from $-1$, and the logarithmic case fills the gap left by the exception.

[class="table-1"]

|                  |                                                               |
| ---------------- | ------------------------------------------------------------- |
| Linearity        | $$\int (f(x) + g(x)) \ dx = \int f(x) \ dx + \int g(x) \ dx$$ |
| Linearity        | $$\int k f(x) \ dx = k \int f(x) \ dx$$                       |
| Power rule       | $$\int x^a \ dx = \dfrac{x^{a+1}}{a+1} + c \quad a \neq -1$$  |
| Logarithmic case | $$\int \dfrac{1}{x} \ dx = \ln \lvert x \rvert + c$$          |
[/class]

## Common integrals

The following identities collect the basic indefinite integrals used most frequently in calculus. Each result can be verified by differentiating the right-hand side and recovering the integrand.

[class="table-1 -right"]

|                                                     |                                                             |
| --------------------------------------------------- | ----------------------------------------------------------- |
| $$\int \frac{1}{x} \ dx = \ln \lvert x \lvert + c$$ | [more](../integral-of-rational-functions/)       |
| $$\int a^x \ dx = \frac{1}{\ln a} \cdot a^x + c$$   | [more](../integral-of-the-exponential-function/) |
| $$\int \sin x \ dx = -\cos x + c$$                  | [more](../integral-of-trigonometric-functions/)  |
| $$\int \cos x \ dx = \sin x + c$$                   | [more](../integral-of-trigonometric-functions/)  |
| $$\int \frac{1}{\sin^2 x} \ dx = -\cot x + c$$      | [more](../integral-of-trigonometric-functions/)  |
| $$\int \frac{1}{\cos^2 x} \ dx = \tan x + c$$       | [more](../integral-of-trigonometric-functions/)  |
| $$\int \sec^2 x \ dx = \tan x + c$$                 | [more](../integral-of-trigonometric-functions/)  |
| $$\int \sec x \tan x \ dx = \sec x + c$$            | [more](../integral-of-trigonometric-functions/)  |
| $$\int \csc^2 x \ dx = -\cot x + c$$                | [more](../integral-of-trigonometric-functions/)  |
| $$\int \csc x \cot x \ dx = -\csc x + c$$           | [more](../integral-of-trigonometric-functions/)  |
| $$\int \frac{dx}{1 + x^2} = \arctan x + c$$         | —                                                           |
| $$\int \frac{dx}{\sqrt{1 - x^2}} = \arcsin x + c$$  | —                                                           |

[/class]

> The identities above hold on any interval where the integrand is defined and continuous. When the integrand does not admit an elementary antiderivative or does not fall directly under one of these rules, the standard recourse is to a change of variable through [integration by substitution](../integration-by-substitution/) or to [integration by parts](../integration-by-parts/). The evaluation of an indefinite integral between two endpoints produces a [definite integral](../definite-integrals/) and computes the corresponding signed area.
