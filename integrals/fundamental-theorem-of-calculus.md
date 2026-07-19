---
title: Fundamental Theorem of Calculus
source: https://algebrica.org/fundamental-theorem-of-calculus/
license: CC BY-NC 4.0
tags:
  - accumulation-function
  - antiderivative
  - change-of-variable
  - continuous-functions
  - definite-integral
  - derivatives
  - differentiation
  - fundamental-theorem-of-calculus
  - indefinite-integral
  - integration
  - leibniz-rule
  - mean-value-theorem
---
## Introduction

The Fundamental Theorem of Calculus relates [differentiation](../derivatives/) and [integration](../indefinite-integrals/). Differentiation describes instantaneous variation, whereas integration measures accumulated quantity. Under suitable regularity assumptions, each operation reverses the other. The theorem has two statements:

+ The First Fundamental Theorem of Calculus
+ The Second Fundamental Theorem of Calculus

> The First Fundamental Theorem states that every continuous function on a closed interval has an antiderivative defined by an integral. The Second states that the [definite integral](../definite-integrals/) is the difference between the endpoint values of any antiderivative.

## The first fundamental theorem of calculus

Let $f$ be [continuous](../continuous-functions/) on a [closed interval](../intervals/) $[a, b]$. For $x \in [a, b]$, define:

$$F(x) = \int_a^x f(t) \ dt$$

The function $F$ is continuous on $[a, b]$, differentiable on $(a, b)$, and satisfies:

$$F'(x) = f(x)$$

At $a$ and $b$, the same identity holds for the right and left derivatives, respectively. To prove continuity, the [Weierstrass theorem](../weierstrass-theorem/) gives a constant $M > 0$ such that $|f(t)| \leq M$ on $[a, b]$. For any $x, y \in [a, b]$, the standard estimate for definite integrals gives:

$$|F(y) - F(x)| = \left|\int_x^y f(t) \ dt\right| \leq M|y - x|$$

Thus $F$ is [Lipschitz continuous](../uniform-continuity/) on $[a, b]$. To prove the derivative identity, fix $x \in (a, b)$ and consider the [difference quotient](../difference-quotient/) for $h \neq 0$ such that $x + h \in [a, b]$:

$$\frac{F(x + h) - F(x)}{h} = \frac{1}{h} \left( \int_a^{x + h} f(t) \ dt - \int_a^x f(t) \ dt \right)$$

[Definite integrals](../definite-integrals/) satisfy the additivity property over adjacent intervals:

$$\int_a^b f(t) \ dt + \int_b^c f(t) \ dt = \int_a^c f(t) \ dt$$

The difference quotient is therefore:

$$\frac{F(x + h) - F(x)}{h} = \frac{1}{h} \int_x^{x + h} f(t) \ dt$$

Since $f$ is continuous on the interval with endpoints $x$ and $x + h$, the mean value theorem for integrals, discussed on the page on [definite integrals](../definite-integrals/), gives a point $c$ between $x$ and $x + h$ such that:

$$\int_x^{x + h} f(t) \ dt = f(c) h$$

Hence:

$$\frac{F(x + h) - F(x)}{h} = f(c)$$

As $h \to 0$, the point $c \to x$. Continuity of $f$ gives:

$$\lim_{h \to 0} \frac{F(x + h) - F(x)}{h} = f(x)$$

Thus $F'(x) = f(x)$. Any fixed point $d \in [a, b]$ can be used as the base point. Define:

$$F_d(x) = \int_d^x f(t) \ dt$$

Since $F_d$ differs from $F$ by the constant $-F(d)$, it has the same derivative. For the base point $a$, the formula is:

$$F(x) = \int_a^x f(t) \ dt$$

The value $F(x)$ is the [signed area](../finding-areas-by-integration/) accumulated from $a$ to $x$. Its derivative is the rate at which this area changes. When $f(x) > 0$, the area increases, and when $f(x) < 0$, it decreases.

![Img. 1](svg/fundamental-theorem-of-calculus-1.svg)

> The shaded signed area is $F(x)$. It increases where $f$ is positive and decreases where $f$ is negative.

## Extension to variable limits of integration

The theorem above treats a constant lower limit and the variable upper limit $x$. Suppose instead that $a$ and $b$ are differentiable functions, and that $f$ is continuous on an [interval](../intervals/) containing their ranges. Define:

$$\Phi(x) = \int_{a(x)}^{b(x)} f(t) \ dt$$

The derivative of $\Phi$ is:

$$\Phi'(x) = f(b(x)) b'(x) - f(a(x)) a'(x)$$

This identity is the simplest form of the Leibniz rule for differentiation under the integral sign. If $a(x) = a$ is constant and $b(x) = x$, the formula becomes $\Phi'(x) = f(x)$ because $a'(x) = 0$ and $b'(x) = 1$. This is the First Fundamental Theorem. To prove the formula, fix a constant $c$ in the domain of $f$ and use additivity over adjacent intervals:

$$\int_{a(x)}^{b(x)} f(t) \ dt = \int_c^{b(x)} f(t) \ dt - \int_c^{a(x)} f(t) \ dt$$

Define the auxiliary function:

$$F(u) = \int_c^u f(t) \ dt$$

By the First Fundamental Theorem, $F'(u) = f(u)$. The definition of $F$ gives:

$$\Phi(x) = F(b(x)) - F(a(x))$$

The [chain rule](../chain-rule/) gives:

$$\Phi'(x) = F'(b(x)) b'(x) - F'(a(x)) a'(x) = f(b(x)) b'(x) - f(a(x)) a'(x)$$

This proves the formula. For example, consider:

$$\Phi(x) = \int_{x}^{x^2} \sin(t^2) \ dt$$

The integrand is the [sine function](../sine-function/) composed with $t^2$, so it is continuous on $\mathbb{R}$. Both limits are differentiable. The lower limit $a(x) = x$ has derivative $a'(x) = 1$, and the upper limit $b(x) = x^2$ has derivative $b'(x) = 2x$. The Leibniz rule gives:

$$\Phi'(x) = \sin\!\left((x^2)^2\right) \cdot 2x - \sin(x^2) \cdot 1 = 2x \sin(x^4) - \sin(x^2)$$

The integrand $\sin(t^2)$ has no elementary antiderivative, but the Leibniz rule gives the derivative of the integral in closed form.

> The first term is the contribution from the moving upper limit, and the second is the contribution from the moving lower limit. Their signs follow from the orientation of the integral.

## The second fundamental theorem of calculus

Let $f$ be continuous on $[a, b]$, and suppose $F$ is continuous on $[a, b]$, differentiable on $(a, b)$, and satisfies $F'(x) = f(x)$ for every $x \in (a, b)$. Then:

$$\int_a^b f(x) \ dx = F(b) - F(a)$$

The second statement says that the definite integral is the change in any antiderivative over the interval. Define:

$$G(x) = \int_a^x f(t) \ dt$$

From the First Fundamental Theorem, $G'(x) = f(x)$. Since both $F$ and $G$ have the same derivative, [Lagrange's theorem](../lagrange-theorem/) implies that their difference is constant:

$$F(x) = G(x) + c$$

Evaluating at $x = a$ gives:

$$F(a) = G(a) + c$$

Because $G(a) = 0$, the constant is $c = F(a)$, and therefore:

$$G(x) = F(x) - F(a)$$

At $x = b$, this identity becomes:

$$\int_a^b f(x) \ dx = G(b) = F(b) - F(a)$$

For a continuous function $f$, the definite integral is also the [net signed area](../finding-areas-by-integration/) between its graph and the horizontal axis. By the theorem, this area is the change $F(b) - F(a)$ in any antiderivative $F$.

The [change-of-variable formula](../integration-by-substitution/) is a direct consequence. Let $g$ be continuously differentiable on $[\alpha, \beta]$, and let $f$ be continuous on an interval containing $g([\alpha, \beta])$. The two forms of the Fundamental Theorem and the chain rule give:

$$\int_{\alpha}^{\beta} f(g(x))g'(x) \ dx = \int_{g(\alpha)}^{g(\beta)} f(u) \ du$$

No monotonicity assumption on $g$ is needed. If $H(y) = \int_{g(\alpha)}^y f(u) \ du$, then the [composite function](../composite-functions/) satisfies $(H \circ g)'(x) = f(g(x))g'(x)$. The Second Fundamental Theorem applied to $H \circ g$ proves the formula.

## Beyond continuity

Continuity of $f$ is sufficient for both statements above. When $f$ is only Riemann-integrable, the accumulation function retains some, but not all, of these properties.

Let $f$ be [Riemann-integrable](../riemann-integrability-criteria/) on $[a, b]$, and define the accumulation function:

$$F(x) = \int_a^x f(t) \ dt$$

The function $F$ is defined for every $x \in [a, b]$. A Riemann-integrable function is bounded, so $|f|$ has an upper bound $M$ on $[a, b]$. For $x_1, x_2 \in [a, b]$ with $x_1 < x_2$, the standard estimate for definite integrals gives:

$$|F(x_2) - F(x_1)| = \left| \int_{x_1}^{x_2} f(t) \ dt \right| \leq M (x_2 - x_1)$$

By symmetry, the same estimate holds with $|x_2 - x_1|$. Thus $F$ is Lipschitz continuous on $[a, b]$ with Lipschitz constant $M$, and in particular it is continuous.

Differentiability depends on the local behavior of $f$. Fix a point $x_0 \in (a, b)$ where $f$ is continuous, and let $\varepsilon > 0$. Continuity at $x_0$ gives $\delta > 0$ such that:

$$|f(t) - f(x_0)| < \varepsilon$$

whenever $|t - x_0| < \delta$. If $0 < |h| < \delta$ and $x_0 + h \in [a, b]$, then:

$$
\begin{align}
\left|\frac{F(x_0 + h) - F(x_0)}{h} - f(x_0)\right|
&= \left|\frac{1}{h}\int_{x_0}^{x_0 + h} (f(t) - f(x_0)) \ dt\right| \\[6pt]
&\leq \frac{1}{|h|}\int_{\min\{x_0,x_0+h\}}^{\max\{x_0,x_0+h\}} |f(t) - f(x_0)| \ dt \\[6pt]
&< \varepsilon
\end{align}
$$

Therefore $F'(x_0) = f(x_0)$. This proof requires continuity only at $x_0$, whereas the mean value theorem for integrals used above requires continuity on the whole interval of integration. The same argument gives the appropriate one-sided derivative when $x_0$ is an endpoint. At a point of [discontinuity](../discontinuities-of-real-functions/) of $f$, the difference quotient of $F$ need not converge, and differentiability may fail.

Consider the [sign function](../sign-function/) on $[-1, 1]$:

$$
f(t) = \begin{cases} -1 & \text{if } t < 0 \\[6pt] 0 & \text{if } t = 0 \\[6pt] 1 & \text{if } t > 0 \end{cases}
$$

The function $f$ is Riemann-integrable on $[-1, 1]$ because one discontinuity does not affect integrability. With $-1$ as the base point, the integrand is $-1$ on the whole interval of integration when $x \in [-1, 0)$, so:

$$F(x) = \int_{-1}^{x} (-1) \ dt = -x - 1$$

For $x \in [0, 1]$, the interval of integration crosses $0$, so additivity gives:

$$F(x) = \int_{-1}^{0} (-1) \ dt + \int_{0}^{x} 1 \ dt = -1 + x$$

Both expressions give $F(0) = -1$, so $F(x) = |x| - 1$ on $[-1, 1]$. This is the [absolute value function](../absolute-value-function/) shifted downward by $1$. The function $F$ is continuous on this interval. For $x \neq 0$, its derivative exists and equals $f(x)$. At the origin, the left derivative is $-1$ and the right derivative is $1$, so $F$ has a [point of non-differentiability](../points-of-non-differentiability/) at the only discontinuity of $f$.

A discontinuity of the integrand does not always make the accumulation function nondifferentiable. Consider the function:

$$
g(t) = \begin{cases} 1 & \text{if } t = 0 \\[6pt] 0 & \text{if } t \neq 0 \end{cases}
$$

The function $g$ is Riemann-integrable on $[-1, 1]$, and its value at one point does not affect the integral. Hence $G(x) = \int_{-1}^x g(t) \ dt$ is identically zero. The derivative $G'(0)$ exists and equals $0$, although $g$ is discontinuous at $0$ and $G'(0) \neq g(0)$. Continuity at a point is sufficient for the derivative identity, but it is not necessary for differentiability of the accumulation function.

For the endpoint formula, continuity of $f$ can be replaced by Riemann integrability when an antiderivative is already known. Suppose $f$ is Riemann-integrable on $[a, b]$. Assume that $F$ is continuous on $[a, b]$, differentiable on $(a, b)$, and satisfies $F'(x) = f(x)$ for every $x \in (a, b)$. Then:

$$\int_a^b f(x) \ dx = F(b) - F(a)$$

To prove the formula, take a partition $P = \{x_0, x_1, \ldots, x_n\}$ of $[a, b]$. On each subinterval $[x_{i-1}, x_i]$, the mean value theorem gives a point $c_i \in (x_{i-1}, x_i)$ such that:

$$F(x_i) - F(x_{i-1}) = F'(c_i)(x_i - x_{i-1}) = f(c_i)(x_i - x_{i-1})$$

Let $m_i$ and $M_i$ be the [infimum and supremum](../supremum-and-infimum/) of $f$ on $[x_{i-1}, x_i]$. Since $m_i \leq f(c_i) \leq M_i$ and $\Delta x_i = x_i - x_{i-1} > 0$, we have:

$$m_i\Delta x_i \leq F(x_i) - F(x_{i-1}) \leq M_i\Delta x_i$$

Summing these inequalities over the partition, the middle terms telescope:

$$\sum_{i=1}^n m_i\Delta x_i \leq F(b) - F(a) \leq \sum_{i=1}^n M_i\Delta x_i$$

The expressions on the left and right are the [lower and upper sums](../riemann-integrability-criteria/) of $f$. Because $f$ is Riemann-integrable, the supremum of its lower sums and the infimum of its upper sums are both $\int_a^b f(x) \ dx$. The middle term must have the same value.

The conclusion also holds when $F$ fails to be differentiable at finitely many points, provided $F$ is continuous and $f = F'$ at every other point. The proof splits $[a, b]$ at the exceptional points and applies the formula to each subinterval. When the resulting identities are added, the values at the internal endpoints cancel. The values assigned to $f$ at the exceptional points do not change its Riemann integral.

> If $f$ is of class $C^k$, repeated differentiation of $F' = f$ shows that the accumulation function $F$ is of class $C^{k + 1}$.

## Example 1

For $f(x) = 3x^2$, evaluate:

$$\int_0^1 3x^2 \ dx$$

An antiderivative of $3x^2$ is $F(x) = x^3$. By the Second Fundamental Theorem:

$$\int_0^1 3x^2 \ dx = F(1) - F(0) = 1^3 - 0^3 = 1$$

Thus the area under the curve $3x^2$ over $[0, 1]$ is $1$.

For the [logarithmic function](../logarithmic-function/), consider the accumulation function:

$$H(x) = \int_1^x \ln t \ dt$$

The value $H(1)$ is $0$ because an integral over a degenerate interval is zero. Since $\ln t$ is continuous for $t > 0$, the function $H$ is defined for $x > 0$. The First Fundamental Theorem gives:

$$H'(x) = \ln x$$

Thus $H$ is an antiderivative of $\ln x$ on $(0, +\infty)$ with $H(1) = 0$.

## Example 2

Compute the derivative:

$$\frac{d}{dx} \int_1^x e^{-t^2} \ dt$$

The integrand $f(t) = e^{-t^2}$ is the [exponential function](../exponential-function/) composed with $-t^2$, so it is continuous on $\mathbb{R}$. The lower limit is constant, and the upper limit is $x$. The First Fundamental Theorem gives:

$$\frac{d}{dx} \int_1^x e^{-t^2} \ dt = e^{-x^2}$$

> An elementary antiderivative is not needed here. The function $e^{-t^2}$ has no elementary antiderivative, but the derivative above is explicit. A fixed definite integral of this function may instead require [numerical integration](../numerical-integration/) or a special function.
