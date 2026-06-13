---
title: Higher-Order Derivatives
source: https://algebrica.org/higher-order-derivatives/
license: CC BY-NC 4.0
tags:
  - concavity
  - derivatives
  - higher-order-derivatives
  - second-derivative
  - second-derivative-test
---
## Definition

Let $y = f(x)$ be a [function](../functions/) differentiable on an interval. Its [derivative](../derivatives/) $f'(x)$ is itself a function defined on the same interval, and it may in turn be differentiable. If it is, its derivative is called the second derivative of $f$ and is denoted by $f''(x)$:

$$f''(x) = \lim_{h \to 0} \frac{f'(x+h) - f'(x)}{h}$$

The process can be iterated. The derivative of the second derivative is the third derivative $f'''(x)$, and in general the derivative of order $n$, or $n$-th derivative, is obtained by differentiating the function $n$ times. It is denoted by $f^{(n)}(x)$, and it is defined recursively by:

$$f^{(n)}(x) = D\left[f^{(n-1)}(x)\right]$$

For the $n$-th derivative to exist at a point, each of the derivatives of order $1, \ldots, n-1$ must exist and be differentiable in a neighborhood of that point.

- - -

Several notations for higher-order derivatives coexist in the literature. For low orders, primes are used, as in $f'(x)$, $f''(x)$, $f'''(x)$. From the fourth derivative onward, the parenthesized exponent is preferred, as in $f^{(4)}(x)$ and, in general, $f^{(n)}(x)$. In Leibniz notation, the first and second derivatives are written as:

$$f'(x) = \frac{df}{dx} \qquad f''(x) = \frac{d^2f}{dx^2}$$

The $n$-th derivative is correspondingly denoted by:

$$f^{(n)}(x) = \frac{d^nf}{dx^n}$$

> The parentheses in $f^{(n)}(x)$ distinguish the $n$-th derivative from the $n$-th power, so that $f^{(2)}(x) = f''(x)$ while $f^2(x) = [f(x)]^2$. By convention, $f^{(0)}(x)$ denotes the function itself.

## Example 1

Consider the polynomial function:

$$f(x) = 2x^4 - 5x^3 + 3x - 7$$

Applying the power rule term by term, each differentiation lowers the degree of the polynomial by one:

$$
\begin{align}
f'(x) &= 8x^3 - 15x^2 + 3 \\[6pt]
f''(x) &= 24x^2 - 30x \\[6pt]
f'''(x) &= 48x - 30 \\[6pt]
f^{(4)}(x) &= 48 \\[6pt]
f^{(5)}(x) &= 0
\end{align}
$$

Since the fourth derivative is constant, every derivative of order greater than four is identically zero. This behavior is general, as for a [polynomial](../polynomials/) of degree $n$ the derivative of order $n$ is a constant, and all derivatives of order greater than $n$ vanish.

## Example 2

The derivatives of a function need not terminate. Consider the function defined for $x \neq 0$:

$$f(x) = \frac{1}{x^2} = x^{-2}$$

Applying the power rule repeatedly, we obtain:

$$
\begin{align}
f'(x) &= -2x^{-3} \\[6pt]
f''(x) &= 6x^{-4} \\[6pt]
f'''(x) &= -24x^{-5}
\end{align}
$$

A pattern emerges. Each differentiation multiplies the coefficient by the current exponent and lowers the exponent by one, so the signs alternate and the coefficients grow factorially. The general formula for the $n$-th derivative is:

$$f^{(n)}(x) = (-1)^n \frac{(n+1)!}{x^{n+2}}$$

The formula can be verified by induction. For $n = 1$ it gives $-\frac{2!}{x^3} = -2x^{-3}$, in agreement with the direct computation, and differentiating the general term reproduces the same expression with $n$ replaced by $n+1$. In this case the function admits derivatives of every order at each point of its domain.

## Geometric and physical meaning

The first derivative measures the rate of change of the function, and the second derivative measures the rate of change of the slope. When $f''(x) > 0$ on an interval, the slope of the tangent line increases as $x$ increases, and the graph is concave upward. When $f''(x) < 0$, the slope decreases and the graph is concave downward. The points where the concavity changes are the inflection points, studied in detail in the entry on [maximum, minimum, and inflection points](../maximum-minimum-and-inflection-points/).

In physics, if $s(t)$ denotes the position of a particle at time $t$, the first derivative $s'(t)$ is the velocity and the second derivative $s''(t)$ is the acceleration. Newton's second law relates force to the second derivative of position, which explains why second derivatives appear throughout the differential equations of mechanics.

> The third derivative of position with respect to time also has a physical name, the jerk, which measures how abruptly the acceleration itself changes.

## The second derivative test

The second derivative provides a practical criterion for classifying the [stationary points](../maximum-minimum-and-inflection-points/) of a function, that is, the points where $f'(x_0) = 0$. Suppose $f$ is twice differentiable in a neighborhood of $x_0$ and $f'(x_0) = 0$. Then:

+ If $f''(x_0) > 0$, the point $x_0$ is a local minimum.
+ If $f''(x_0) < 0$, the point $x_0$ is a local maximum.
+ If $f''(x_0) = 0$, the test is inconclusive.

The intuition behind the criterion is that at a stationary point with positive second derivative the graph is concave upward, so the function lies above its horizontal tangent line near the stationary point, which is therefore a local minimum. The symmetric argument applies to local maxima.

When the test is inconclusive, the point may be of any nature. The functions $f(x) = x^4$, $f(x) = -x^4$, and $f(x) = x^3$ all satisfy $f'(0) = 0$ and $f''(0) = 0$, yet the origin is respectively a local minimum, a local maximum, and a horizontal inflection point. In these cases, the study of the sign of $f'(x)$ around the point remains the appropriate tool.

## Example 3

The stationary points of the following function are to be classified:

$$f(x) = x^3 - 6x^2 + 9x + 1$$

The first derivative is:

$$f'(x) = 3x^2 - 12x + 9 = 3(x^2 - 4x + 3) = 3(x-1)(x-3)$$

The stationary points are therefore $x = 1$ and $x = 3$. The second derivative is:

$$f''(x) = 6x - 12$$

Evaluating the second derivative at the two stationary points, we obtain:

$$f''(1) = 6 - 12 = -6 < 0 \qquad f''(3) = 18 - 12 = 6 > 0$$

By the second derivative test, the point $x = 1$ is a local maximum, with $f(1) = 1 - 6 + 9 + 1 = 5$, and the point $x = 3$ is a local minimum, with $f(3) = 27 - 54 + 27 + 1 = 1$. Moreover, since $f''(x)$ changes sign at $x = 2$, where $f(2) = 8 - 24 + 18 + 1 = 3$, the point $(2, 3)$ is an inflection point of the function.

## Smoothness classes

Higher-order derivatives provide a natural way to measure the regularity of a function. Given an interval $I$, a function $f$ is said to be of class $C^k(I)$ if all its derivatives up to order $k$ exist and are [continuous](../continuous-functions/) on $I$. In particular, $C^0(I)$ denotes the class of continuous functions, and $C^\infty(I)$ denotes the class of functions admitting derivatives of every order, often called smooth functions.

The inclusions between these classes are strict. For example, the function $f(x) = x|x|$ is of class $C^1(\mathbb{R})$ but not of class $C^2(\mathbb{R})$. Indeed, the function coincides with $x^2$ for $x \geq 0$ and with $-x^2$ for $x < 0$, so its derivative is $f'(x) = 2|x|$, which is continuous on all of $\mathbb{R}$. The derivative, however, has a corner at the origin, so $f''(0)$ does not exist.

> Polynomials, the exponential function, the sine and the cosine are all of class $C^\infty(\mathbb{R})$, since each differentiation produces another function of the same family.

## Higher-order derivatives in several variables

The iteration of derivatives extends to functions of several variables, where differentiating the first-order [partial derivatives](../partial-derivatives/) produces second-order partial derivatives, including the mixed ones. In that setting, the equality of mixed derivatives is governed by Schwarz's theorem, and the second-order information is organized in the Hessian matrix, which generalizes the second derivative test to functions of several variables.
