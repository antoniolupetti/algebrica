---
title: Cauchy’s Theorem
source: https://algebrica.org/cauchy-theorem/
license: CC BY-NC 4.0
tags:
  - cauchy-theorem
  - differential-calculus-theorems
  - polynomials
  - theorems
  - derivatives
---
## Statement

Cauchy's theorem establishes a relationship between the variations of two differentiable functions over a closed interval, expressed through the ratio of their derivatives at a suitable interior point. It generalises [Lagrange's theorem](../lagrange-theorem/) to a pair of functions and provides the analytical basis for the proof of [L'Hôpital's rule](../hopital-rule/).

**Theorem 1.** Let $f(x)$ and $g(x)$ be two real-valued functions defined on $[a, b]$. Assume that:

+ $f(x)$ and $g(x)$ are [continuous](../continuous-functions/) on the closed interval $[a, b]$.
+ $f(x)$ and $g(x)$ are differentiable on the open interval $(a, b)$.
+ $g'(x) \neq 0$ for every $x \in (a, b)$.

Then there exists at least one point $c \in (a, b)$ such that:

$$\frac{f'(c)}{g'(c)} = \frac{f(b) - f(a)}{g(b) - g(a)}$$

In other words, the ratio of the increments of the two functions over the interval $[a, b]$ coincides with the ratio of their [derivatives](../derivatives) at some interior point.

> The hypothesis $g'(x) \neq 0$ on $(a, b)$ ensures, via [Rolle's theorem](../rolles-theorem/) applied to $g$, that $g(b) \neq g(a)$, so that the denominator on the right-hand side does not vanish. A detailed discussion of this point is given in the last section.

- - -

The choice $g(x) = x$ reduces Cauchy's theorem to [Lagrange's theorem](../lagrange-theorem/). In that case $g'(x) = 1$ and $g(b) - g(a) = b - a$, and the conclusion takes the familiar form:

$$f'(c) = \frac{f(b) - f(a)}{b - a}$$

Lagrange's theorem is therefore the special case of Cauchy's, obtained when one of the two functions is the identity.

## Geometric interpretation

Cauchy's theorem admits a clear geometric meaning when the pair $(g(t), f(t))$ is regarded as a parametric curve in the plane, with $t$ varying in $[a, b]$. The chord joining the endpoints $(g(a), f(a))$ and $(g(b), f(b))$ of the curve has slope:

$$\frac{f(b) - f(a)}{g(b) - g(a)}$$

The tangent to the curve at the parameter $t = c$ has slope $f'(c)/g'(c)$. Cauchy's theorem asserts therefore the existence of at least one interior parameter $c$ at which the tangent to the curve is parallel to the chord connecting its endpoints. When $g(t) = t$ the curve coincides with the graph of $f$, and the statement reduces to the geometric content of Lagrange's theorem.

## Proof

To prove the theorem we introduce an auxiliary function depending on a real parameter $\lambda$:

$$\varphi(x) = f(x) - \lambda g(x)$$

The parameter $\lambda$ is chosen so that the values of $\varphi$ at the endpoints of the interval coincide. The condition $\varphi(a) = \varphi(b)$ leads to:

$$\lambda = \frac{f(b) - f(a)}{g(b) - g(a)}$$

The denominator is non-zero because the hypothesis $g'(x) \neq 0$ on $(a, b)$ excludes the case $g(b) = g(a)$, as discussed in the last section.

- - -

The function $\varphi(x)$ is continuous on $[a, b]$ and differentiable on $(a, b)$, since it is a linear combination of $f$ and $g$, which satisfy these regularity properties by hypothesis. Moreover $\varphi(a) = \varphi(b)$ by the very choice of $\lambda$. The hypotheses of [Rolle's theorem](../rolles-theorem/) are therefore satisfied, and there exists at least one point $c \in (a, b)$ such that $\varphi'(c) = 0$. Computing the derivative of $\varphi$ and evaluating it at $c$ gives:

$$\varphi'(x) = f'(x) - \lambda g'(x)$$

$$f'(c) = \lambda g'(c)$$

- - -

Substituting the value of $\lambda$ into the previous equality we obtain:

$$f'(c) = \frac{f(b) - f(a)}{g(b) - g(a)} \, g'(c)$$

Since $g'(c) \neq 0$ by hypothesis, dividing both sides by $g'(c)$ yields:

$$\frac{f'(c)}{g'(c)} = \frac{f(b) - f(a)}{g(b) - g(a)}$$

This is the conclusion of the theorem.

## Example 1

Let us verify that the hypotheses of Cauchy's theorem are satisfied by the functions:

$$f(x) = 2x^2 - 4x + 2 \qquad g(x) = x^2$$

on the interval $[1, 3]$, and let us determine the corresponding value of $c$ predicted by the statement.

The two functions are [polynomials](../polynomials), hence continuous and differentiable for every $x \in \mathbb{R}$. The derivative of the denominator is $g'(x) = 2x$, which is non-zero on $[1, 3]$. The hypotheses of the theorem are therefore satisfied.

- - -

The theorem guarantees the existence of a point $c \in (1, 3)$ such that:

$$\frac{f'(c)}{g'(c)} = \frac{f(3) - f(1)}{g(3) - g(1)}$$

We begin by evaluating $f$ and $g$ at the endpoints:

$$f(1) = 2 - 4 + 2 = 0 \qquad f(3) = 18 - 12 + 2 = 8$$

$$g(1) = 1 \qquad g(3) = 9$$

The ratio of the increments is therefore:

$$\frac{f(3) - f(1)}{g(3) - g(1)} = \frac{8 - 0}{9 - 1} = 1$$

- - -

Computing the derivatives we obtain $f'(x) = 4x - 4$ and $g'(x) = 2x$, hence:

$$\frac{f'(c)}{g'(c)} = \frac{4c - 4}{2c}$$

Imposing the equality between the two ratios, the equation determining $c$ takes the form:

$$
\begin{aligned}
\frac{4c - 4}{2c} &= 1 \\[6pt]
4c - 4 &= 2c \\[6pt]
2c &= 4 \\[6pt]
c &= 2
\end{aligned}
$$

Since $c = 2 \in (1, 3)$, the theorem is verified and the point predicted by the statement is explicitly identified.

## A note on the hypothesis $g'(x) \neq 0$

The hypothesis $g'(x) \neq 0$ on $(a, b)$ has a precise role both in the statement and in the proof. Consider the situation in which $g(b) = g(a)$. In this case the denominator of the ratio:

$$\frac{f(b) - f(a)}{g(b) - g(a)}$$

vanishes, and the expression is undefined. For the same reason the constant:

$$\lambda = \frac{f(b) - f(a)}{g(b) - g(a)}$$

cannot be introduced, and the auxiliary function used in the proof:

$$\varphi(x) = f(x) - \lambda g(x)$$

is no longer well defined.

Under the hypotheses of Cauchy's theorem, however, this situation does not arise. Suppose by contradiction that $g(a) = g(b)$. Since $g$ is continuous on $[a, b]$ and differentiable on $(a, b)$, Rolle's theorem applied to $g$ would produce a point $\xi \in (a, b)$ with $g'(\xi) = 0$, contradicting the assumption $g'(x) \neq 0$ on the open interval. Therefore $g(b) \neq g(a)$, the ratio defining $\lambda$ is well posed, and the proof goes through without difficulty.
