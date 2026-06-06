---
title: Hyperbolic Tangent and Cotangent
source: https://algebrica.org/hyperbolic-tangent-and-cotangent/
license: CC BY-NC 4.0
tags:
  - hyperbolic-cotangent
  - hyperbolic-functions
  - hyperbolic-tangent
  - trigonometry
---
## Introduction

The hyperbolic tangent and cotangent arise from the hyperbolic sine and cosine in exactly the same way that the circular [tangent and cotangent](../tangent-and-cotangent/) arise from the circular [sine and cosine](../sine-and-cosine/). Given the [hyperbolic sine and cosine](../hyperbolic-sine-and-cosine/), both introduced in relation to the right branch of the equilateral [hyperbola](../hyperbola/):

$$
X^{2} - Y^{2} = 1
$$

The hyperbolic tangent is defined as their ratio, provided that $\cosh(x)$ is not zero. Since $\cosh(x) \geq 1$ for all real $x$, the denominator is never zero, and the hyperbolic tangent is therefore defined on the entire real line. The hyperbolic cotangent involves the reciprocal ratio and requires $\sinh(x) \neq 0$, which excludes only $x = 0$.

Once the point $P(\cosh(x), \sinh(x))$ on the hyperbola has been identified as the one corresponding to a signed hyperbolic sector of area $x/2$, the hyperbolic tangent and cotangent can be read from its coordinates. The hyperbolic tangent is the ratio of the vertical coordinate to the horizontal coordinate:

$$
\tanh(x) := \frac{\sinh(x)}{\cosh(x)}
$$

![IMG. 1](svg/hyperbolic-tangent-and-cotangent-1.svg)


> To make the construction more intuitive, consider the unit hyperbola $x^2 - y^2 = 1$ and the point $P = (\cosh x, \sinh x)$, associated with a hyperbolic angle $x$. Draw the [line](../lines/) passing through the origin $O$ and $P$, and consider the vertical line $x = 1$. Their intersection defines the point $T$, which has coordinates $T = (1, \tanh x)$, since the slope of the line $OP$ is $\sinh x/ \cosh x = \tanh x$. The vertical segment joining $(1,0)$ to $T$ therefore represents geometrically the length of the hyperbolic tangent.

The hyperbolic cotangent is the reciprocal ratio, that is, the horizontal coordinate divided by the vertical one:

$$
\coth(x) := \frac{\cosh(x)}{\sinh(x)}
$$

![IMG. 2](svg/hyperbolic-tangent-and-cotangent-2.svg)


> As in the case illustrated above for the hyperbolic tangent, to make the construction more intuitive, consider the unit hyperbola $x^2 - y^2 = 1$ and the point $P = (\cosh x, \sinh x)$, associated with a hyperbolic angle $x$. Draw the [line](../lines/) passing through the origin $O$ and $P$, and consider the horizontal line $y = 1$. Their intersection defines the point $S$, which has coordinates $S = (\coth x, 1)$, since the slope of the line $OP$ is $\sinh x / \cosh x = \tanh x$, and thus its reciprocal gives $\coth x = \cosh x / \sinh x$. The horizontal segment joining $(0,1)$ to $S$ therefore represents geometrically the length of the hyperbolic cotangent.

In this geometric picture, the hyperbolic tangent and cotangent measure a kind of slope of the point on the hyperbola relative to its two coordinates, in analogy with the way the circular tangent expresses the slope of the point on the [unit circle](../unit-circle/).

## Fundamental hyperbolic identity for tangent and cotangent

The hyperbolic tangent and cotangent satisfy an identity that follows directly from the [fundamental hyperbolic identity](../hyperbolic-sine-and-cosine/). Starting from:

$$
\cosh^{2}(x) - \sinh^{2}(x) = 1
$$

and dividing both sides by $\cosh^{2}(x)$, which is always positive, we obtain the identity for the hyperbolic tangent:

$$
1 - \tanh^{2}(x) = \frac{1}{\cosh^{2}(x)}
$$

Analogously, dividing the fundamental identity by $\sinh^{2}(x)$ for $x \neq 0$ gives the identity for the hyperbolic cotangent:

$$
\coth^{2}(x) - 1 = \frac{1}{\sinh^{2}(x)}
$$

Both identities record a direct consequence of the hyperbola equation: the coordinates of the point $P$ are constrained to satisfy $X^{2} - Y^{2} = 1$, and dividing by either coordinate squared translates this constraint into a relation involving the ratio functions.

## Hyperbolic identities

The addition, subtraction, double-argument, and reciprocal relations for the two functions are collected below:

$$
\begin{align}
&\tanh(x+y) = \frac{\tanh(x) + \tanh(y)}{1 + \tanh(x)\tanh(y)} \\[8pt]
&\tanh(x-y) = \frac{\tanh(x) - \tanh(y)}{1 - \tanh(x)\tanh(y)} \\[8pt]
&\tanh(2x)  = \frac{2\tanh(x)}{1 + \tanh^{2}(x)} \\[6pt]
&\coth(x+y) = \frac{1 + \coth(x)\coth(y)}{\coth(x) + \coth(y)} \\[8pt]
&\coth(x-y) = \frac{-1 + \coth(x)\coth(y)}{\coth(x) - \coth(y)} \\[15pt]
&\tanh(x)\coth(x) = 1
\end{align}
$$

> The addition and subtraction formulas for the hyperbolic tangent and cotangent closely mirror their circular counterparts, but are governed by the algebra of the equilateral hyperbola. The last identity simply states that $\tanh$ and $\coth$ are reciprocal functions wherever both are defined.

## Analytical expression of the hyperbolic tangent

Using the analytical expressions of the hyperbolic sine and cosine in terms of the [exponential function](../exponential-function/), we can write the hyperbolic tangent directly. Substituting:

$$
\begin{align}
\sinh(x) &= \frac{e^{x} - e^{-x}}{2} \\[6pt]
\cosh(x) &= \frac{e^{x} + e^{-x}}{2}
\end{align}
$$

into the definition $\tanh(x) = \sinh(x)/\cosh(x)$ and simplifying the factor $1/2$ that appears in both numerator and denominator, we obtain:

$$
\tanh(x) = \frac{e^{x} - e^{-x}}{e^{x} + e^{-x}}
$$

An equivalent and often more compact form is obtained by multiplying numerator and denominator by $e^{-x}$:

$$
\tanh(x) = \frac{1 - e^{-2x}}{1 + e^{-2x}}
$$

or, equivalently, by multiplying by $e^{x}$:

$$
\tanh(x) = \frac{e^{2x} - 1}{e^{2x} + 1}
$$

A further equivalent form follows from a purely algebraic rearrangement of the last expression. Writing the numerator as $e^{2x} - 1 = (e^{2x} + 1) - 2$ and splitting the fraction, we obtain:

$$
\tanh(x) = 1 - \frac{2}{e^{2x} + 1}
$$

All four expressions are equivalent and each makes apparent a different aspect of the function: in the first form, the numerator and denominator are the analytically defined [hyperbolic sine and cosine](../hyperbolic-sine-and-cosine/) themselves. In the second and third, the exponential growth as $x \to +\infty$ or $x \to -\infty$ becomes immediately visible, and from them one can read off at once that the function tends to $1$ and $-1$ respectively. The fourth form displays $\tanh(x)$ as the translate of $1$ by a strictly positive quantity that decreases monotonically with $x$, so that the bound $\tanh(x) < 1$ appears as an algebraic identity rather than as an asymptotic property.

## Analytical expression of the hyperbolic cotangent

The derivation of the analytical expression for the hyperbolic cotangent follows the same pattern. Substituting the expressions of $\sinh(x)$ and $\cosh(x)$ into the definition $\coth(x) = \cosh(x)/\sinh(x)$, and again cancelling the common factor $1/2$, we get:

$$
\coth(x) = \frac{e^{x} + e^{-x}}{e^{x} - e^{-x}}
$$

As before, multiplying numerator and denominator by $e^{-x}$ or by $e^{x}$ gives the equivalent forms:

$$
\coth(x) = \frac{1 + e^{-2x}}{1 - e^{-2x}} = \frac{e^{2x} + 1}{e^{2x} - 1}
$$

The latter expressions show that for large positive $x$ the function approaches $1$ from above, while for large negative $x$ it approaches $-1$ from below, with a vertical asymptote at $x = 0$ in both cases.

## Hyperbolic tangent and cotangent functions

The hyperbolic tangent function $f(x) = \tanh(x)$ is defined for all real numbers. Unlike the circular tangent, it does not have vertical [asymptotes](../asymptotes/): its graph is a smooth, monotonically increasing curve that passes through the origin with slope $1$ and remains bounded for all $x$. As $x \to +\infty$ the function approaches $1$ asymptotically, while as $x \to -\infty$ it approaches $-1$, so the range is the open interval $(-1, 1)$.


![IMG. 3](svg/hyperbolic-tangent-and-cotangent-3.svg)

+ Domain: $x \in \mathbb{R}$
+ Range: $y \in (-1, 1)$
+ Periodicity: not periodic
+ Parity: [odd](../even-and-odd-functions/), $\tanh(-x) = -\tanh(x)$
+ Horizontal asymptotes: $y = 1$ as $x \to +\infty$; $y = -1$ as $x \to -\infty$

The hyperbolic cotangent function $f(x) = \coth(x)$ is defined for all real $x \neq 0$. Its graph consists of two branches: one for $x > 0$, where the function decreases from $+\infty$ toward $1$, and one for $x < 0$, where it increases from $-\infty$ toward $-1$. The origin is a vertical asymptote, and the lines $y = 1$ and $y = -1$ are horizontal asymptotes.


![IMG. 4](svg/hyperbolic-tangent-and-cotangent-4.svg)

+ Domain: $x \in \mathbb{R},\; x \neq 0$
+ Range: $y \in (-\infty, -1) \cup (1, +\infty)$
+ Periodicity: not periodic
+ Parity: [odd](../even-and-odd-functions/), $\coth(-x) = -\coth(x)$
+ Vertical asymptote: $x = 0$
+ Horizontal asymptotes: $y = 1$ as $x \to +\infty$; $y = -1$ as $x \to -\infty$

## Relation to the circular tangent and cotangent

The circular [tangent and cotangent](../tangent-and-cotangent/) are defined as ratios of the circular sine and cosine, which in turn arise from the geometry of the unit circle. By exact analogy, the hyperbolic tangent and cotangent are ratios of the hyperbolic sine and cosine, which arise from the geometry of the equilateral hyperbola. In both settings, the underlying identity constraining the coordinates of a point on the curve propagates to a corresponding identity for the ratio functions.

There is, however, a fundamental difference between the two cases: while the circular tangent is periodic with period $\pi$ and is unbounded, the hyperbolic tangent is monotone and bounded between $-1$ and $1$. Similarly, the circular cotangent has vertical asymptotes at every integer multiple of $\pi$, whereas the hyperbolic cotangent has only one, at the origin.

> Both the circular and the hyperbolic tangent measure a kind of ratio of coordinates of a point on a curve, one on the unit circle and the other on the equilateral hyperbola. The structural parallelism between the two families of functions is one of the most elegant features of classical analysis.
