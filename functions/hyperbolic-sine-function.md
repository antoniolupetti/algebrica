---
title: Hyperbolic Sine Function
source: https://algebrica.org/hyperbolic-sine-function/
license: CC BY-NC 4.0
tags:
  - derivatives
  - exponential-function
  - hyperbolic-functions
  - hyperbolic-sine
---

## Introduction

The geometric construction of the hyperbolic sine from the area of a sector of the equilateral [hyperbola](../hyperbola/) is given in [hyperbolic sine and cosine](../hyperbolic-sine-and-cosine/). Here the hyperbolic sine is a real [function](../functions/) of a real variable and has the [exponential](../exponential-function/) definition:

$$\sinh(x) = \frac{e^x - e^{-x}}{2}$$

The function $f(x) = \sinh(x)$ is half the difference between $e^x$ and $e^{-x}.$ It is defined for every real number and has range $\mathbb{R}.$ Its graph passes through the origin with slope $1.$ The function tends to $+\infty$ as $x \to +\infty$ and to $-\infty$ as $x \to -\infty,$ while the [circular sine](../sine-function/) oscillates. For large positive $x,$ the term $e^{-x}$ becomes negligible and $\sinh(x)$ is close to $e^x/2,$ while for large negative $x,$ it is close to $-e^{-x}/2.$

![IMG. 1](svg/hyperbolic-sine-function-1.svg)

The hyperbolic sine measures the arc length of the catenary, the curve $y = \cosh(x)$ along which a uniform chain hangs under its own weight. For $a \geq 0,$ the [length](../arc-length-of-a-curve/) of the arc from the vertex to the point of abscissa $a$ is $\sinh(a),$ because the fundamental hyperbolic identity gives $\sqrt{1 + \sinh^2(x)} = \cosh(x)$ and $\int_0^a \cosh(x) \ dx = \sinh(a).$

## Properties

The exponential definition gives the following properties.

+ [Domain](../determining-the-domain-of-a-function/): $x \in \mathbb{R}$
+ Range: $y \in \mathbb{R}$
+ Periodicity: the hyperbolic sine is not periodic on the real line.
+ Parity: [odd](../even-and-odd-functions/), with $\sinh(-x) = -\sinh(x)$
+ Monotonicity: strictly [increasing](../increasing-and-decreasing-functions/) on the whole domain
+ Sign: negative for $x < 0$ and positive for $x > 0$
+ Root: $x = 0,$ the only point at which the function vanishes
+ [Maximum and minimum points](../maximum-minimum-and-inflection-points/): none, since the function is strictly increasing on the whole domain

The hyperbolic sine is continuous and strictly increasing, and its range is the whole real line, so it is a [bijection](../injective-surjective-and-bijective-functions/) of $\mathbb{R}$ onto $\mathbb{R}.$ The hyperbolic sine and the [hyperbolic cosine](../hyperbolic-sine-and-cosine/) satisfy the fundamental hyperbolic identity:

$$\cosh^2(x) - \sinh^2(x) = 1$$

For the circular functions, the [Pythagorean identity](../pythagorean-identity/) has a plus sign, $\cos^2(x) + \sin^2(x) = 1.$ Since $\cosh(x) \geq 1$ for every real $x,$ the hyperbolic identity gives $\cosh(x) = \sqrt{1 + \sinh^2(x)}.$ The addition and duplication formulas for $\sinh$ are collected in [hyperbolic identities](../hyperbolic-identities/).

## Limits, derivatives, and integrals of the hyperbolic sine function

The behaviour near the origin follows from the [remarkable limit](../remarkable-limits/) of the exponential function. The quotient can be written as

$$\frac{\sinh(x)}{x} = \frac{1}{2}\left(\frac{e^x - 1}{x} + \frac{e^{-x} - 1}{-x}\right)$$

As $x$ tends to zero, both quotients in parentheses tend to $1.$ It follows that

$$\lim_{x \to 0} \frac{\sinh(x)}{x} = 1$$

Near the origin $\sinh(x)$ is therefore close to $x,$ as for the circular sine. The limits at infinity and the comparison with $e^x/2$ at $+\infty$ are

$$
\begin{align}
\lim_{x \to +\infty} \sinh(x) &= +\infty \\[6pt]
\lim_{x \to -\infty} \sinh(x) &= -\infty \\[6pt]
\lim_{x \to +\infty} \left(\sinh(x) - \frac{e^x}{2}\right) &= 0
\end{align}
$$

The last limit holds because the difference equals $-e^{-x}/2.$ The curve approaches $e^x/2$ from below. At $-\infty,$ the equality $\sinh(x) + e^{-x}/2 = e^x/2 \to 0$ shows that the curve approaches $-e^{-x}/2$ from above. Continuity on $\mathbb{R}$ excludes vertical [asymptotes](../asymptotes/), while $\dfrac{\sinh(x)}{x} \to +\infty$ as $x \to \pm\infty$ excludes horizontal and oblique asymptotes.

The function $\sinh(x)$ is [continuous](../continuous-functions/) and differentiable on $\mathbb{R}.$ Differentiating the exponential expression term by term gives the [derivative](../derivatives/):

$$\frac{d}{dx}\sinh(x) = \frac{e^x + e^{-x}}{2} = \cosh(x)$$

Differentiating again gives the original function, so the derivatives alternate with period two:

$$\frac{d^2}{dx^2}\sinh(x) = \sinh(x)$$

The [$n$-th derivative](../higher-order-derivatives/) is therefore determined by the parity of $n:$

$$
\frac{d^n}{dx^n}\sinh(x) =
\begin{cases}
\sinh(x) & \text{if } n \text{ is even} \\[6pt]
\cosh(x) & \text{if } n \text{ is odd}
\end{cases}
$$

> The hyperbolic sine is the unique solution of the [differential equation](../differential-equations/) $y'' = y$ with $y(0) = 0$ and $y'(0) = 1.$ The circular sine solves $y'' = -y$ with the same initial conditions.

- - -

Since the derivative of $\cosh(x)$ is $\sinh(x),$ the [indefinite integral](../indefinite-integrals/) of the hyperbolic sine is:

$$\int \sinh(x) \ dx = \cosh(x) + c$$

The [definite integral](../definite-integrals/) over an interval symmetric about the origin vanishes, because the function is odd:

$$\int_{-a}^{a} \sinh(x) \ dx = 0$$

For integrals containing $\sqrt{1 + x^2},$ the [substitution](../integration-by-substitution/) $x = \sinh(t)$ gives $\sqrt{1 + x^2} = \cosh(t)$ and $dx = \cosh(t) \ dt.$ The transformed integrand therefore has no radical of this form. For $\sqrt{1 - x^2},$ the corresponding [trigonometric substitution](../trigonometric-substitution-for-integrals/) is $x = \sin(t)$ with $-\pi/2 \leq t \leq \pi/2.$

## Monotonicity and convexity

The derivative $\cosh(x)$ is at least $1$ at every point, so the hyperbolic sine is strictly increasing on $\mathbb{R}$ and has no stationary points. The smallest slope is attained at the origin, where the tangent is the line $y = x.$

The second derivative $\sinh(x)$ determines [convexity and concavity](../convexity-and-concavity-of-functions/). It is negative for $x < 0$ and positive for $x > 0,$ so the graph is concave on $(-\infty, 0)$ and convex on $(0, +\infty).$ The origin is an [inflection point](../maximum-minimum-and-inflection-points/), where the second derivative vanishes and changes sign.

On the half line $x \geq 0$ the graph is convex, so it lies above the tangent at the origin. This gives the inequality:

$$\sinh(x) \geq x$$

Equality holds only at $x = 0.$ By oddness the reversed inequality $\sinh(x) \leq x$ holds for $x \leq 0.$

## Inverse function

Since the hyperbolic sine is a bijection from $\mathbb{R}$ to itself, its [inverse function](../inverse-function/) is defined on $\mathbb{R}$ and is denoted by $\mathrm{arsinh}.$

To obtain a closed form, solve $x = \sinh(y)$ for $y.$ Setting $t = e^y$ and multiplying the equation $2x = t - t^{-1}$ by $t$ gives the [quadratic equation](../quadratic-equations/):

$$t^2 - 2xt - 1 = 0$$

Its roots are $t = x \pm \sqrt{x^2 + 1}.$ Since $\sqrt{x^2 + 1} > |x|,$ only the root with the plus sign is positive, as required by $t = e^y.$ Since $y$ is the [natural logarithm](../logarithms/) of $t,$ substituting $t = x + \sqrt{x^2 + 1}$ gives

$$\mathrm{arsinh}(x) = \ln\left(x + \sqrt{x^2 + 1}\right)$$

The [derivative of the inverse function](../derivative-of-the-inverse-function/) is the reciprocal of $\cosh$ evaluated at $\mathrm{arsinh}(x).$ Since $\cosh$ is positive, the fundamental hyperbolic identity gives $\cosh(\mathrm{arsinh}(x)) = \sqrt{1 + x^2}.$ The derivative is therefore

$$\frac{d}{dx}\mathrm{arsinh}(x) = \frac{1}{\sqrt{1 + x^2}}$$

The antiderivatives of $\dfrac{1}{\sqrt{1 + x^2}}$ are therefore given by

$$\int \frac{1}{\sqrt{1 + x^2}} \ dx = \ln\left(x + \sqrt{x^2 + 1}\right) + c$$

## Maclaurin series

The Maclaurin series of the hyperbolic sine follows from the series of the exponential function. Subtracting the expansion of $e^{-x}$ from that of $e^x$ cancels the even powers and doubles the odd ones, and dividing by $2$ gives a [power series](../power-series/) that converges for every [real number](../real-numbers/):

$$\sinh(x) = \sum_{n=0}^{\infty} \frac{x^{2n+1}}{(2n+1)!} = x + \frac{x^3}{3!} + \frac{x^5}{5!} + \frac{x^7}{7!} + \cdots$$

Only odd powers appear because the hyperbolic sine is odd. All coefficients are positive, whereas the [Taylor series](../taylor-series/) of the circular sine has the same terms with alternating signs. For $x > 0$ every partial sum is strictly less than the value of the function, so the first partial sum gives $\sinh(x) > x.$ Keeping the first term gives the approximation $\sinh(x) \approx x$ for small $x.$ Dividing the series by $x$ proves that $\dfrac{\sinh(x)}{x} \to 1$ as $x \to 0.$

## Relation to the circular sine

The [exponential definitions](../eulers-formula/) of $\sinh(x)$ and $\sin(x)$ extend to [complex](../complex-numbers/) values of $x:$

$$
\begin{align}
\sinh(x) &= \frac{e^x - e^{-x}}{2} \\[6pt]
\sin(x) &= \frac{e^{ix} - e^{-ix}}{2i}
\end{align}
$$

Direct substitution of $ix$ for $x$ in both formulas gives

$$\sinh(ix) = i\sin(x) \qquad \sin(ix) = i\sinh(x)$$

The map $z \mapsto iz$ is a rotation through an angle $\pi/2$ about the origin. In the Maclaurin series of $\sinh,$ the same substitution multiplies the term of degree $2n+1$ by $i^{2n+1} = i(-1)^n.$ Factoring out $i$ leaves the alternating series of the circular sine.
