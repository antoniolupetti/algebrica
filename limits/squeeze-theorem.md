---
title: Squeeze Theorem
source: https://algebrica.org/squeeze-theorem/
license: CC BY-NC 4.0
tags:
  - bounded-functions
  - limits
  - oscillating-functions
  - squeeze-theorem
---
## What is the squeeze theorem

The squeeze theorem, also called the sandwich theorem, provides a method for determining the [limit](../limits/) of a [function](../functions/) when direct evaluation is challenging or when the function exhibits complex oscillatory behaviour near a specific point. The theorem is frequently applied to functions involving [sine and cosine](../sine-and-cosine/), particularly when these trigonometric terms oscillate in such a way that direct limit evaluation is impossible, as in:

$$\sin\left( \frac{1}{x} \right) \quad \text{or} \quad \cos\left( \frac{1}{x} \right)$$

In these situations, the function is constrained between two other functions with known and equal limits, which makes the evaluation of the target limit accessible.

## Statement

**Theorem.** Let $x_0 \in \mathbb{R} \cup \{ \pm\infty \}$ be a limit point, that is, a point such that every neighbourhood of $x_0$ contains at least one point of the [domain](../functions/) different from $x_0$. Let $f$, $g$, and $h$ be real-valued functions defined on a neighbourhood $I$ of $x_0$, and assume that for every $x \in I$ the inequality:

$$g(x) \leq f(x) \leq h(x)$$

holds. Suppose, in addition, that the limits of $g(x)$ and $h(x)$ as $x \to x_0$ both exist and coincide with the same value $\ell$:

$$\lim_{x \to x_0} g(x) = \lim_{x \to x_0} h(x) = \ell$$

Under these hypotheses, the function $f(x)$ also admits a limit as $x \to x_0$, and that limit is:

$$\lim_{x \to x_0} f(x) = \ell$$

- - -

Graphically, the curve representing $f(x)$ lies entirely between the lower bound $g(x)$ and the upper bound $h(x)$. As both bounding functions tend to $\ell$, the function $f(x)$ is forced to approach the same limit.

![IMG. 1](svg/squeeze-theorem-1.svg)

This expresses the geometric intuition behind the theorem: if a function is bounded above and below by two functions that both converge to the same value, then it must converge to that value.

## Proof of the squeeze theorem

Let $\varepsilon > 0$ be arbitrary. The goal is to prove that the function $f(x)$, which lies between $g(x)$ and $h(x)$, tends to the same limit $\ell$ as $x \to x_0$.

By assumption, $\lim_{x \to x_0} g(x) = \ell$. This means that there exists a positive number $\delta_1$ such that, for every $x$ sufficiently close to $x_0$, specifically for all $x$ satisfying $0 < |x - x_0| < \delta_1$:

$$|g(x) - \ell| < \varepsilon \quad \implies \quad \ell - \varepsilon < g(x) < \ell + \varepsilon$$

Similarly, since $\lim_{x \to x_0} h(x) = \ell$, there exists another positive number $\delta_2$ such that:

$$|h(x) - \ell| < \varepsilon \quad \implies \quad \ell - \varepsilon < h(x) < \ell + \varepsilon$$

Set $\delta = \min(\delta_1, \delta_2)$. For every $x$ such that $0 < |x - x_0| < \delta$, both inequalities above are satisfied. Since $f(x)$ is squeezed between $g(x)$ and $h(x)$:

$$g(x) \leq f(x) \leq h(x)$$

Combining this with the bounds on $g(x)$ and $h(x)$:

$$\ell - \varepsilon < f(x) < \ell + \varepsilon \quad \implies \quad |f(x) - \ell| < \varepsilon$$

Since this inequality holds for every $\varepsilon > 0$, we conclude:

$$\lim_{x \to x_0} f(x) = \ell$$

## Example 1

The following example illustrates how the theorem is applied to compute the limit:

$$\lim_{x \to 0} x \cdot \sin\left( \frac{1}{x} \right)$$

- - -

The term $\sin\left( \frac{1}{x} \right)$ does not admit a limit as $x \to 0$, since it oscillates indefinitely between $-1$ and $1$. For every [real number](../real-numbers/) $x \neq 0$, however, the inequality:

$$-1 \leq \sin\left( \frac{1}{x} \right) \leq 1$$

holds. Multiplying through by $x$ and using the [absolute value](../absolute-value/) to symmetrise the inequality, we obtain:

$$-|x| \leq x \cdot \sin\left( \frac{1}{x} \right) \leq |x|$$

- - -

For $x > 0$, the inequality is preserved; for $x < 0$, the direction reverses, but the absolute value ensures that the comparison remains symmetric with respect to zero. Both bounding functions $-|x|$ and $|x|$ tend to zero as $x \to 0$:

$$\lim_{x \to 0} -|x| = 0 \qquad \lim_{x \to 0} |x| = 0$$

Since $x \sin(1/x)$ is squeezed between two functions that both approach zero, the squeeze theorem applies and gives:

$$\lim_{x \to 0} x \cdot \sin\left( \frac{1}{x} \right) = 0$$

In many problems, when an oscillating function is multiplied by a power of $x$ that approaches zero, the overall limit is zero. The reason is that the oscillation remains bounded, as is the case for sine and cosine, which are confined to the interval $[-1, 1]$. The factor $x^n$ approaches zero rapidly enough to dominate the oscillation, so the entire product converges to zero.

## Example 2

Evaluate the limit:

$$\lim_{x \to +\infty} \frac{\ln(3 + \sin x)}{x^3}$$

- - -

The sine function is bounded between $-1$ and $1$ for every real $x$:

$$-1 \leq \sin x \leq 1$$

Adding $3$ to each term gives:

$$2 \leq 3 + \sin x \leq 4 \quad \text{for all } x \in \mathbb{R}$$

- - -

Since the [logarithmic function](../logarithms/) is strictly increasing, the same chain of inequalities is preserved under $\ln$:

$$\ln 2 \leq \ln(3 + \sin x) \leq \ln 4$$

Dividing all three terms by $x^3$ (which is positive for $x > 0$):

$$\frac{\ln 2}{x^3} \leq \frac{\ln(3 + \sin x)}{x^3} \leq \frac{\ln 4}{x^3} \quad \forall x > 0$$

Both bounding functions tend to zero as $x \to +\infty$. Applying the squeeze theorem:

$$\lim_{x \to +\infty} \frac{\ln(3 + \sin x)}{x^3} = 0$$

## Example 3

Evaluate the limit:

$$\lim_{x \to 0} \left( x^4 \cdot \cos\left( \frac{2}{x} \right) + 2 \right)$$

We analyse the behaviour of the function $x^4 \cdot \cos\left( \frac{2}{x} \right)$ separately. The cosine function is bounded between $-1$ and $1$ for all real values:

$$-1 \leq \cos\left( \frac{2}{x} \right) \leq 1$$

Multiplying all three terms by $x^4$, which is non-negative, gives:

$$-x^4 \leq x^4 \cdot \cos\left( \frac{2}{x} \right) \leq x^4$$

- - -

Taking the limit of the left and right bounds as $x \to 0$:

$$\lim_{x \to 0} (-x^4) = 0 \qquad \lim_{x \to 0} x^4 = 0$$

By the squeeze theorem:

$$\lim_{x \to 0} x^4 \cdot \cos\left( \frac{2}{x} \right) = 0$$

The original expression can now be evaluated by applying the sum rule from the [algebra of limits](../algebra-of-limits/):

$$\lim_{x \to 0} \left( x^4 \cdot \cos\left( \frac{2}{x} \right) + 2 \right) = 0 + 2 = 2$$

The squeeze theorem complements the techniques developed for [indeterminate forms](../indeterminate-forms/) and is often the simplest route whenever a function can be controlled between two functions with a common limit.
