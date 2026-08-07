---
title: Fundamental Theorem of Calculus
source: https://algebrica.org/fundamental-theorem-of-calculus/
license: CC BY-NC 4.0
tags:
  - accumulation-function
  - antiderivative
  - average-value
  - change-of-variable
  - continuous-functions
  - definite-integral
  - derivatives
  - differentiation
  - extreme-value-theorem
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

## Bounds for a continuous integrand

The proof of the first statement uses an estimate that holds whenever the integrand is continuous on a closed and bounded interval. Let $f$ be continuous on $[a, b]$ with $a < b.$ By the [Weierstrass theorem](../weierstrass-theorem/), $f$ has a minimum and a maximum, attained at points $t_m, t_M \in [a, b],$ respectively. Denote these extreme values by:

$$m = f(t_m) \qquad M = f(t_M)$$

Every value of $f$ on the interval lies between these two numbers, so $m \leq f(t) \leq M$ for every $t \in [a, b].$ Applying the comparison property of [definite integrals](../definite-integrals/) to the constant functions $m$ and $M$ gives:

$$m(b - a) \leq \int_a^b f(t) \ dt \leq M(b - a)$$

When $f$ is nonnegative, the two outer quantities are the areas of rectangles with base $[a, b].$ The rectangle of height $m$ is contained in the region between the graph and the horizontal axis, and that region is contained in the rectangle of height $M.$ The figure illustrates this case.

![Img. 1](svg/fundamental-theorem-of-calculus-1.svg)

> The heights of the two rectangles are values of $f,$ attained at points of $[a, b].$ In the figure the minimum and the maximum both occur inside the interval, but either may be attained at an endpoint.

A bounded [Riemann-integrable](../riemann-integrability-criteria/) function satisfies the same inequality with $m$ and $M$ replaced by the [infimum and supremum](../supremum-and-infimum/) of $f$ on the interval. If $f$ is continuous on a closed and bounded interval, it attains both extrema. This fact has two consequences.

The first concerns the sign of the integral. If $f(t) > 0$ for every $t \in [a, b],$ then $m$ is a value of $f$ and is therefore positive, so:

$$0 < m(b - a) \leq \int_a^b f(t) \ dt$$

The infimum of a positive function need not be positive. Define $g$ on $[0, 1]$ by $g(0) = 1$ and $g(t) = t$ for $t > 0.$ This function is positive and Riemann-integrable, but its infimum is $0,$ so the lower bound only shows that its integral is nonnegative. A continuous positive function on $[a, b]$ has a positive minimum, which makes the inequality above strict. Symmetrically, if $f(t) < 0$ throughout $[a, b],$ then $M < 0$ and the integral is negative. A continuous integrand that is everywhere positive or everywhere negative has an integral with the same sign.

The second consequence concerns the average value of $f.$ Dividing the estimate by $b - a > 0$ gives:

$$m \leq \frac{1}{b - a} \int_a^b f(t) \ dt \leq M$$

The middle quantity is the average value of $f$ on $[a, b].$ Since this average lies between $m$ and $M,$ the [intermediate value theorem](../intermediate-value-theorem/) applied to $f$ on the interval with endpoints $t_m$ and $t_M$ gives a point $c$ for which $f(c)$ equals the average:

$$\int_a^b f(t) \ dt = f(c)(b - a)$$

This identity is the mean value theorem for integrals. Both $t_m$ and $t_M$ belong to $[a, b],$ and so does $c.$

> The point can always be chosen in the open interval $(a, b).$ Suppose the average value equals $M.$ The function $M - f$ is continuous, nonnegative, and has zero integral on $[a, b].$ If it were positive at some point, it would be positive throughout a subinterval, and the strict bound above would imply that its integral is positive. Hence $f$ is constant on $[a, b]$ and every interior point satisfies the identity. The case of the minimum is symmetric.

## The first fundamental theorem of calculus

Let $f$ be [continuous](../continuous-functions/) on a [closed interval](../intervals/) $[a, b].$ For $x \in [a, b],$ define:

$$F(x) = \int_a^x f(t) \ dt$$

The function $F$ is continuous on $[a, b],$ differentiable on $(a, b),$ and satisfies:

$$F'(x) = f(x)$$

At $a$ and $b,$ the same identity holds for the right and left derivatives, respectively. To prove continuity, set $K = \max\{|m|, |M|\},$ where $m$ and $M$ are the extreme values from the previous section, so that $|f(t)| \leq K$ on $[a, b].$ For any $x, y \in [a, b],$ the standard estimate for definite integrals gives:

$$|F(y) - F(x)| = \left|\int_x^y f(t) \ dt\right| \leq K|y - x|$$

Thus $F$ is [Lipschitz continuous](../uniform-continuity/) on $[a, b].$ To prove the derivative identity, fix $x \in (a, b)$ and consider the [difference quotient](../difference-quotient/) for $h \neq 0$ such that $x + h \in [a, b]:$

$$\frac{F(x + h) - F(x)}{h} = \frac{1}{h} \left( \int_a^{x + h} f(t) \ dt - \int_a^x f(t) \ dt \right)$$

[Definite integrals](../definite-integrals/) satisfy the additivity property over adjacent intervals:

$$\int_a^b f(t) \ dt + \int_b^c f(t) \ dt = \int_a^c f(t) \ dt$$

The difference quotient is therefore:

$$\frac{F(x + h) - F(x)}{h} = \frac{1}{h} \int_x^{x + h} f(t) \ dt$$

The mean value theorem for integrals proved above gives a point $c_h$ between $x$ and $x + h$ such that:

$$\int_x^{x + h} f(t) \ dt = f(c_h) h$$

Hence the difference quotient is:

$$\frac{F(x + h) - F(x)}{h} = f(c_h)$$

Since $c_h$ lies between $x$ and $x + h,$ it approaches $x$ as $h \to 0.$ By continuity of $f,$ we have:

$$\lim_{h \to 0} \frac{F(x + h) - F(x)}{h} = f(x)$$

Thus $F'(x) = f(x).$ Any fixed point $d \in [a, b]$ can be used as the base point. Define:

$$F_d(x) = \int_d^x f(t) \ dt$$

Since $F_d$ differs from $F$ by the constant $-F(d),$ it has the same derivative. For $d = a,$ this is the original accumulation function $F.$

The value $F(x)$ is the [signed area](../finding-areas-by-integration/) accumulated from $a$ to $x.$ Its derivative is the rate at which this area changes. When $f(x) > 0,$ the area increases, and when $f(x) < 0,$ it decreases.

![Img. 2](svg/fundamental-theorem-of-calculus-2.svg)

> The shaded signed area is $F(x).$ It increases where $f$ is positive and decreases where $f$ is negative.

## Extension to variable limits of integration

In the theorem above, the lower limit is constant and the upper limit is the variable $x.$ Suppose instead that $a$ and $b$ are differentiable functions, and that $f$ is continuous on an [interval](../intervals/) containing their ranges. Define:

$$\Phi(x) = \int_{a(x)}^{b(x)} f(t) \ dt$$

The derivative of $\Phi$ is:

$$\Phi'(x) = f(b(x)) b'(x) - f(a(x)) a'(x)$$

This identity is the simplest form of the Leibniz rule for differentiation under the integral sign. If $a(x) = a$ is constant and $b(x) = x,$ the formula becomes $\Phi'(x) = f(x)$ because $a'(x) = 0$ and $b'(x) = 1.$ This is the First Fundamental Theorem. To prove the formula, fix a constant $c$ in the domain of $f$ and use additivity over adjacent intervals:

$$\int_{a(x)}^{b(x)} f(t) \ dt = \int_c^{b(x)} f(t) \ dt - \int_c^{a(x)} f(t) \ dt$$

Define the auxiliary function:

$$F(u) = \int_c^u f(t) \ dt$$

By the First Fundamental Theorem, $F'(u) = f(u).$ The definition of $F$ gives:

$$\Phi(x) = F(b(x)) - F(a(x))$$

The [chain rule](../chain-rule/) gives:

$$\Phi'(x) = F'(b(x)) b'(x) - F'(a(x)) a'(x) = f(b(x)) b'(x) - f(a(x)) a'(x)$$

This proves the formula. For example, consider:

$$\Phi(x) = \int_{x}^{x^2} \sin(t^2) \ dt$$

The integrand is the [sine function](../sine-function/) composed with $t^2,$ so it is continuous on $\mathbb{R}.$ Both limits are differentiable. The lower limit $a(x) = x$ has derivative $a'(x) = 1,$ and the upper limit $b(x) = x^2$ has derivative $b'(x) = 2x.$ The Leibniz rule gives:

$$\Phi'(x) = \sin\!\left((x^2)^2\right) \cdot 2x - \sin(x^2) \cdot 1 = 2x \sin(x^4) - \sin(x^2)$$

The integrand $\sin(t^2)$ has no [elementary antiderivative](../integration-strategies/), but the Leibniz rule gives the derivative of the integral in closed form.

> The first term is the contribution from the moving upper limit, and the second is the contribution from the moving lower limit. Their signs follow from the orientation of the integral.

## The second fundamental theorem of calculus

Let $f$ be continuous on $[a, b],$ and suppose $F$ is continuous on $[a, b],$ differentiable on $(a, b),$ and satisfies $F'(x) = f(x)$ for every $x \in (a, b).$ Then the endpoint formula is:

$$\int_a^b f(x) \ dx = F(b) - F(a)$$

The second statement says that the definite integral is the change in any antiderivative over the interval. Define:

$$G(x) = \int_a^x f(t) \ dt$$

From the First Fundamental Theorem, $G'(x) = f(x).$ Since both $F$ and $G$ have the same derivative, [Lagrange's theorem](../lagrange-theorem/) implies that their difference is constant:

$$F(x) = G(x) + c$$

Evaluating at $x = a$ gives:

$$F(a) = G(a) + c$$

Because $G(a) = 0,$ the constant is $c = F(a),$ and therefore:

$$G(x) = F(x) - F(a)$$

At $x = b,$ this identity becomes:

$$\int_a^b f(x) \ dx = G(b) = F(b) - F(a)$$

For a continuous function $f,$ the definite integral is also the [net signed area](../finding-areas-by-integration/) between its graph and the horizontal axis. By the theorem, this area is the change $F(b) - F(a)$ in any antiderivative $F.$

The [change-of-variable formula](../integration-by-substitution/) is a direct consequence. Let $g$ be continuously differentiable on $[\alpha, \beta],$ and let $f$ be continuous on an interval containing $g([\alpha, \beta]).$ The two forms of the Fundamental Theorem and the chain rule give:

$$\int_{\alpha}^{\beta} f(g(x))g'(x) \ dx = \int_{g(\alpha)}^{g(\beta)} f(u) \ du$$

No [monotonicity](../increasing-and-decreasing-functions/) assumption on $g$ is needed. If $H(y) = \int_{g(\alpha)}^y f(u) \ du,$ then the [composite function](../composite-functions/) satisfies $(H \circ g)'(x) = f(g(x))g'(x).$ The Second Fundamental Theorem applied to $H \circ g$ proves the formula.

Applying the endpoint formula to the product rule gives [integration by parts](../integration-by-parts/).

## Beyond continuity

Continuity of $f$ is sufficient for both statements above. When $f$ is only Riemann-integrable, the accumulation function has some, but not all, of these properties.

Let $f$ be [Riemann-integrable](../riemann-integrability-criteria/) on $[a, b],$ and define the accumulation function:

$$F(x) = \int_a^x f(t) \ dt$$

The function $F$ is defined for every $x \in [a, b].$ A Riemann-integrable function is bounded, so $|f|$ has an upper bound $K$ on $[a, b].$ Here $f$ need not have a minimum or a maximum. For $u, v \in [a, b]$ with $u < v,$ the standard estimate for definite integrals gives:

$$|F(v) - F(u)| = \left| \int_{u}^{v} f(t) \ dt \right| \leq K (v - u)$$

By symmetry, the same estimate holds with $|v - u|.$ Thus $F$ is Lipschitz continuous on $[a, b]$ with Lipschitz constant $K,$ and in particular it is continuous.

Differentiability depends on the local behavior of $f.$ Fix a point $x_0 \in (a, b)$ where $f$ is continuous, and let $\varepsilon > 0.$ Since $f$ is continuous at $x_0,$ choose $\delta > 0$ so that whenever $|t - x_0| < \delta,$ the following inequality holds:

$$|f(t) - f(x_0)| < \varepsilon$$

If $0 < |h| < \delta$ and $x_0 + h \in [a, b],$ then:

$$
\begin{align}
\left|\frac{F(x_0 + h) - F(x_0)}{h} - f(x_0)\right|
&= \left|\frac{1}{h}\int_{x_0}^{x_0 + h} (f(t) - f(x_0)) \ dt\right| \\[6pt]
&\leq \frac{1}{|h|}\int_{\min\{x_0,x_0+h\}}^{\max\{x_0,x_0+h\}} |f(t) - f(x_0)| \ dt \\[6pt]
&< \varepsilon
\end{align}
$$

Therefore $F'(x_0) = f(x_0).$ This proof requires continuity only at $x_0,$ whereas the mean value theorem for integrals used above requires continuity on the whole interval of integration. The same argument gives the appropriate one-sided derivative when $x_0$ is an endpoint. At a point of [discontinuity](../discontinuities-of-real-functions/) of $f,$ the difference quotient of $F$ need not converge, and differentiability may fail.

Consider the [sign function](../sign-function/) on $[-1, 1]:$

$$
f(t) = \begin{cases} -1 & \text{if } t < 0 \\[6pt] 0 & \text{if } t = 0 \\[6pt] 1 & \text{if } t > 0 \end{cases}
$$

The function $f$ is Riemann-integrable on $[-1, 1]$ because it is bounded and has only one discontinuity. With $-1$ as the base point, the integrand is $-1$ on the whole interval of integration when $x \in [-1, 0),$ so:

$$F(x) = \int_{-1}^{x} (-1) \ dt = -x - 1$$

For $x \in [0, 1],$ the interval of integration crosses $0,$ so additivity gives:

$$F(x) = \int_{-1}^{0} (-1) \ dt + \int_{0}^{x} 1 \ dt = -1 + x$$

Both expressions give $F(0) = -1,$ so $F(x) = |x| - 1$ on $[-1, 1].$ This is the [absolute value function](../absolute-value-function/) shifted downward by $1.$ The function $F$ is continuous on this interval. For $x \neq 0,$ its derivative exists and equals $f(x).$ At the origin, the left derivative is $-1$ and the right derivative is $1,$ so $F$ has a [point of non-differentiability](../points-of-non-differentiability/) at the only discontinuity of $f.$

A discontinuity of the integrand need not make the accumulation function nondifferentiable. Consider the function:

$$
g(t) = \begin{cases} 1 & \text{if } t = 0 \\[6pt] 0 & \text{if } t \neq 0 \end{cases}
$$

The function $g$ is Riemann-integrable on $[-1, 1],$ and its value at one point does not affect the integral. Hence $G(x) = \int_{-1}^x g(t) \ dt$ is identically zero. The derivative $G'(0)$ exists and equals $0,$ although $g$ is discontinuous at $0$ and $G'(0) \neq g(0).$ Continuity at a point is sufficient for the derivative identity, but it is not necessary for differentiability of the accumulation function.

For the endpoint formula, continuity of $f$ can be replaced by Riemann integrability when an antiderivative is already known. Suppose $f$ is Riemann-integrable on $[a, b].$ Assume that $F$ is continuous on $[a, b],$ differentiable on $(a, b),$ and satisfies $F'(x) = f(x)$ for every $x \in (a, b).$ Then the endpoint identity is:

$$\int_a^b f(x) \ dx = F(b) - F(a)$$

To prove the formula, take a partition $P = \{x_0, x_1, \ldots, x_n\}$ of $[a, b].$ On each subinterval $[x_{i-1}, x_i],$ the mean value theorem gives a point $c_i \in (x_{i-1}, x_i)$ such that:

$$F(x_i) - F(x_{i-1}) = F'(c_i)(x_i - x_{i-1}) = f(c_i)(x_i - x_{i-1})$$

Let $m_i$ and $M_i$ be the [infimum and supremum](../supremum-and-infimum/) of $f$ on $[x_{i-1}, x_i].$ Since $m_i \leq f(c_i) \leq M_i$ and $\Delta x_i = x_i - x_{i-1} > 0,$ we have:

$$m_i\Delta x_i \leq F(x_i) - F(x_{i-1}) \leq M_i\Delta x_i$$

When these inequalities are summed over the partition, the middle terms telescope:

$$\sum_{i=1}^n m_i\Delta x_i \leq F(b) - F(a) \leq \sum_{i=1}^n M_i\Delta x_i$$

The expressions on the left and right are the [lower and upper sums](../riemann-integrability-criteria/) of $f.$ Because $f$ is Riemann-integrable, the supremum of its lower sums and the infimum of its upper sums are both $\int_a^b f(x) \ dx.$ The middle term must have the same value.

The conclusion also holds when $F$ fails to be differentiable at finitely many points, provided $F$ is continuous and $f = F'$ at every other point. The interval $[a, b]$ can be split at the exceptional points, and the formula applies to each resulting subinterval. When the resulting identities are added, the values at the internal endpoints cancel. The values assigned to $f$ at the exceptional points do not change its Riemann integral.

> If $f$ is of class $C^k,$ [repeated differentiation](../higher-order-derivatives/) of $F' = f$ shows that the accumulation function $F$ is of class $C^{k + 1}.$

## Example 1

For $f(x) = 3x^2,$ evaluate:

$$\int_0^1 3x^2 \ dx$$

An antiderivative of $3x^2$ is $F(x) = x^3.$ By the Second Fundamental Theorem:

$$\int_0^1 3x^2 \ dx = F(1) - F(0) = 1^3 - 0^3 = 1$$

Thus the area under the curve $3x^2$ over $[0, 1]$ is $1.$

For the [logarithmic function](../logarithmic-function/), consider the accumulation function:

$$H(x) = \int_1^x \ln t \ dt$$

The value $H(1)$ is $0$ because an integral over a degenerate interval is zero. Since $\ln t$ is continuous for $t > 0,$ the function $H$ is defined for $x > 0.$ The First Fundamental Theorem gives:

$$H'(x) = \ln x$$

Thus $H$ is an antiderivative of $\ln x$ on $(0, +\infty)$ with $H(1) = 0.$

## Example 2

Compute the derivative:

$$\frac{d}{dx} \int_1^x e^{-t^2} \ dt$$

The integrand $f(t) = e^{-t^2}$ is the [exponential function](../exponential-function/) composed with $-t^2,$ so it is continuous on $\mathbb{R}.$ The lower limit is constant, and the upper limit is $x.$ The First Fundamental Theorem gives:

$$\frac{d}{dx} \int_1^x e^{-t^2} \ dt = e^{-x^2}$$

> An elementary antiderivative is not needed here. The function $e^{-t^2}$ has no elementary antiderivative, but the derivative above is explicit. A fixed definite integral of this function may instead be evaluated by [numerical integration](../numerical-integration/) or expressed in terms of a special function.

## The infinitesimal formulation

The preceding arguments use [epsilon-delta limits](../limits/). Nonstandard analysis formulates the same material in the hyperreal field, an ordered field that contains $\mathbb{R}$ as a [proper subfield](../fields/). An infinitesimal $\varepsilon$ satisfies $|\varepsilon| < r$ for every positive real number $r,$ and every nonzero infinitesimal has an infinite reciprocal. Three notions are needed. Two hyperreals are infinitely close when their difference is infinitesimal. Every finite hyperreal $z$ is infinitely close to a unique real number, called its standard part $\mathrm{st}(z).$ The transfer principle states that a [first-order statement](../first-order-logic/) about the real numbers is true exactly when its transferred counterpart is true in the hyperreal field.

In this formulation, let $x$ be a real interior point and let $\Delta x$ be a nonzero infinitesimal. We use the same symbol for a real function and its natural hyperreal extension. If the difference quotient is finite and its standard part is independent of $\Delta x,$ that standard part is the derivative:

$$F'(x) = \mathrm{st}\!\left(\frac{F(x + \Delta x) - F(x)}{\Delta x}\right)$$

By the transfer principle, the bound for a continuous integrand also holds on the interval with endpoints $x$ and $x + \Delta x.$ For $\Delta x > 0,$ let $m$ and $M$ be the extreme values of $f$ on that interval. The resulting inequality is:

$$m\Delta x \leq F(x + \Delta x) - F(x) \leq M\Delta x$$

After division by $\Delta x,$ the difference quotient lies between $m$ and $M.$ Since $f$ is continuous at $x,$ both extreme values are infinitely close to $f(x).$ The quotient is therefore infinitely close to $f(x),$ and its standard part is $f(x).$ The case $\Delta x < 0$ is the same after reversing the endpoints. This is the estimate used in the second section, with the standard-part map in place of the limit $h \to 0.$

The two formulations differ in language, but their conclusions about real functions are the same. The infinitesimal formulation replaces epsilon-delta estimates with infinitesimal closeness and the standard-part map.

> Abraham Robinson developed nonstandard analysis and presented it in Non-Standard Analysis, North-Holland, 1966. A first-year textbook based on this formulation is H. Jerome Keisler's [Elementary Calculus: An Infinitesimal Approach](https://people.math.wisc.edu/~hkeisler/calc.html), whose second edition of 1986 treats the Fundamental Theorem in section 4.2.
