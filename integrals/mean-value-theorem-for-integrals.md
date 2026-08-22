---
title: Mean Value Theorem for Integrals
source: https://algebrica.org/mean-value-theorem-for-integrals/
license: CC BY-NC 4.0
tags:
  - average-value
  - continuous-functions
  - darboux-theorem
  - definite-integral
  - fundamental-theorem-of-calculus
  - integration
  - intermediate-value-theorem
  - mean-value-theorem
  - weierstrass-theorem
---
## Statement

The mean value theorem for integrals is fairly simple and can be understood intuitively without even examining its formal statement and proof. Consider the [graph of a function](../analyzing-the-graphs-of-functions/) defined and continuous on a given interval. The function's average value lies between its minimum and maximum and, by continuity, the function attains it at least once. If we regard the horizontal line at this value as a threshold, the area between the graph and the line where the graph lies above it cancels the corresponding area where the graph lies below it. When the function is nonnegative, its integral over the interval is therefore the area of a rectangle whose base is the chosen interval and whose height is the average value. Keep in mind from the outset that the main application of this theorem is in the proof of the [first fundamental theorem of calculus](../fundamental-theorem-of-calculus/), where it converts the difference quotient of the accumulation function into a value of the integrand.

We now give the formal statement. Let $f$ be a [continuous function](../continuous-functions/) on a closed and bounded [interval](../intervals/) $[a, b]$ with $a < b.$ Then there exists a point $c \in [a, b]$ such that:

$$\int_a^b f(x) \ dx = f(c)(b - a) \tag{1}$$

In practice, the [definite integral](../definite-integrals/) of $f$ over the interval equals the integral of the constant function $f(c)$ over the same interval, whose length is represented in the formula by the difference $(b-a)$. When $f$ is nonnegative, identity $(1)$ shows that the [region between the graph and the horizontal axis](../finding-areas-by-integration/) has the same area as a rectangle with base $b - a$ and height $f(c).$ The identity can also be written as:

$$\int_a^b (f(x) - f(c)) \ dx = 0 \tag{2}$$

This second identity describes the relationship between the shaded areas in the following figure. On the interval $[a, b],$ the area between the graph of $f$ and the line $y = f(c)$ where the graph lies above the line equals the corresponding area where the graph lies below it. In the figure, $M = f(x_M)$ is the maximum value of $f$ on the interval, and $m = f(x_m)$ is its minimum value. As we shall see in the next section, these values are used in the proof of the theorem.

![A continuous graph with equal total areas above and below the horizontal line at its average value](svg/mean-value-theorem-for-integrals-1.svg)

> Keep in mind that continuity is the theorem's only hypothesis concerning $f.$ [Differentiability](../derivatives/) is not required, and the conclusion remains valid when $f$ is nowhere differentiable in $(a, b).$

## Proof

The proof of the theorem is also fairly simple. We know that a continuous function on a closed and bounded interval is Riemann integrable. By the [Weierstrass theorem](../weierstrass-theorem/), $f$ also attains a [minimum and a maximum](../maximum-minimum-and-inflection-points/) on $[a, b],$ at the points $x_m$ and $x_M,$ respectively:

$$m = f(x_m) \qquad M = f(x_M)$$

Every value of $f$ lies between these two numbers, so $m \leq f(x) \leq M$ for every $x \in [a, b].$ The comparison property for definite integrals, applied to the constant functions $m$ and $M,$ gives:

$$m(b - a) \leq \int_a^b f(x) \ dx \leq M(b - a)$$

Dividing by $b - a$ gives:

$$m \leq \frac{1}{b - a} \int_a^b f(x) \ dx \leq M \tag{3} $$

Let $\mu$ denote the middle term. Then:

$$f(x_m) \le \mu \le f(x_M)$$

By the [intermediate value theorem](../intermediate-value-theorem/), there exists a point $c$ in the closed interval with endpoints $x_m$ and $x_M$ such that $f(c) = \mu.$ Since $x_m$ and $x_M$ both belong to $[a, b],$ the same is true of $c.$ Multiplying $f(c) = \mu$ by $b - a$ then gives identity $(1)$.

> In addition to Riemann integrability, the proof uses two consequences of continuity. The extrema $m$ and $M$ are values of the function, and the function attains every value between them.

- - -

The point $c$ can also be chosen in the open interval $(a, b).$ Suppose that $m < \mu < M.$ Then $f(x_m) \neq \mu$ and $f(x_M) \neq \mu,$ so the point $c$ provided by the intermediate value theorem lies strictly between $x_m$ and $x_M.$ Both points belong to $[a, b],$ hence $c \in (a, b).$

Suppose instead that $\mu = M.$ The function $M - f$ is continuous and nonnegative on $[a, b],$ and its integral is zero because:

$$\int_a^b (M - f(x)) \ dx = M(b - a) - \mu(b - a) = 0 \tag{4}$$

If $M - f$ were positive at some point $x_0,$ continuity would provide a subinterval $J \subseteq [a, b]$ of positive length $\ell$ on which:

$$M - f(x) \geq \frac{1}{2}(M - f(x_0))$$

It would follow that:

$$\int_a^b (M - f(x)) \ dx \geq \int_J (M - f(x)) \ dx \geq \frac{M - f(x_0)}{2} \ell > 0$$

This contradicts the fact that the integral in $(4)$ is zero. Thus $f$ is constant and equal to $M,$ and every interior point satisfies $f(c) = \mu$ (the case $\mu = m$ is symmetric).

## The average value of a function

For a function $f$ that is [Riemann integrable](../riemann-integrability-criteria/) on $[a, b],$ the middle term in $(3)$ is the average value of $f$ on the interval, also called the integral mean:

$$\mu = \frac{1}{b - a} \int_a^b f(x) \ dx$$

The definition extends the concept of the [arithmetic mean](../arithmetic-mean/) in statistics to functions of a continuous variable through a limit of [Riemann sums](../definite-integrals/). Suppose that we divide the interval $[a, b]$ into $n$ subintervals of equal length $\Delta x = (b - a)/n,$ and sample $f$ at the right endpoint $x_k = a + k \Delta x$ of each subinterval. Since $\Delta x/(b - a) = 1/n,$ the arithmetic mean of the $n$ sampled values can be rewritten as:

$$\frac{1}{n} \sum_{k=1}^{n} f(x_k) = \frac{1}{b - a} \sum_{k=1}^{n} f(x_k) \Delta x$$

The expression on the right is a Riemann sum of $f$ on $[a, b],$ divided by the length of the interval; as $n \to \infty,$ this expression converges to $\mu.$ The average value is therefore the limit of the arithmetic means of samples taken from increasingly fine partitions.

For a concrete example, if $v(t)$ is the [velocity](../velocity/) of a point moving along a line and $t_1 < t_2$ are two distinct times, the integral of $v$ on $[t_1, t_2]$ is the displacement over that time interval. The average velocity over the interval is:

$$\mu = \frac{1}{t_2 - t_1} \int_{t_1}^{t_2} v(t) \ dt$$

This value is the constant velocity that would produce the same displacement in the same time. When the velocity is continuous, there exists a time $c \in [t_1, t_2]$ at which $v(c) = \mu.$

## A terminological clarification

To avoid confusion, recall that the mean value theorem for integrals is quite different from the other mean value theorem, also known as [Lagrange's theorem](../lagrange-theorem/). If $f$ is continuous on $[a, b]$ and differentiable on $(a, b),$ the latter gives a point $c \in (a, b)$ at which the derivative equals the [difference quotient](../difference-quotient/) determined by the endpoints of the interval:

$$f'(c) = \frac{f(b) - f(a)}{b - a} \tag{5}$$

By contrast, as we saw just above, the mean value theorem for integrals states that an integrand equals its average value at some point of the interval under consideration:

$$f(c) = \frac{1}{b - a} \int_a^b f(x) \ dx$$

Although the two theorems have different hypotheses and conclusions, the [fundamental theorem of calculus](../fundamental-theorem-of-calculus/) establishes a connection between them. In particular, the second fundamental theorem of calculus states that if $f$ is continuous on $[a, b]$ and $F$ is any [antiderivative](../indefinite-integrals/) of $f,$ then the definite integral over $[a, b]$ is:

$$\int_a^b f(x) \ dx = F(b) - F(a)$$

Identity $(5)$ then becomes:

$$F(b) - F(a) = F'(c)(b - a)$$

This is Lagrange's theorem applied to $F.$ Conversely, Lagrange's theorem applied to an antiderivative of a continuous function $f$ yields the mean value theorem for integrals. It is important to remember that, for a function $F$ with a continuous derivative, the two theorems are equivalent.

## What happens without continuity

Many theorems about functions assume continuity, and their conclusions depend on that hypothesis. For a bounded [Riemann-integrable](../riemann-integrability-criteria/) function, the same inequalities hold, but with the [infimum and supremum](../supremum-and-infimum/) in place of the [minimum and maximum](../maximum-minimum-and-inflection-points/). Relation $(3)$ can therefore be rewritten as:

$$\inf_{[a, b]} f \leq \frac{1}{b - a} \int_a^b f(x) \ dx \leq \sup_{[a, b]} f$$

In this case too, the average value remains defined and lies between these bounds but, unlike what we have seen so far, the function need not attain it. Consider the following [step function](../heaviside-function/) on the interval $[0, 2]:$

$$
f(x) = \begin{cases} 0 & \text{if } 0 \leq x < 1 \\[6pt] 1 & \text{if } 1 \leq x \leq 2 \end{cases}
$$

The function $f$ is bounded and has only one [discontinuity](../discontinuities-of-real-functions/), so it is Riemann integrable, and its integral on $[0, 2]$ is equal to $1$ (a very simple calculation suffices to verify this). The average value is therefore $1/2,$ but, as you can see, the function never takes this value because its [range](../functions/) is $\{\ 0, 1 \ \}.$ Thus boundedness and Riemann integrability do not suffice for the conclusion.


> The proof of the theorem applies to every Riemann-integrable function that attains its extrema and has the intermediate value property. [Darboux's theorem](../darboux-theorem/) shows that the latter property can hold without continuity, since every derivative has the intermediate value property, even when the derivative is discontinuous.

## The weighted form

The mean value theorem for integrals also has a form in which the values of $f$ are averaged against a weight. Let $f$ be continuous on $[a, b]$ and let $g$ be Riemann integrable and nonnegative on the same interval. Under these conditions, there exists $c \in [a, b]$ such that:

$$\int_a^b f(x) g(x) \ dx = f(c) \int_a^b g(x) \ dx \tag{6}$$

If $g(x) = 1,$ we obtain identity $(1),$ and the proof follows the same two steps. Multiplying the inequalities $m \leq f(x) \leq M$ by $g(x)$ gives:

$$m g(x) \leq f(x) g(x) \leq M g(x)$$

The product $fg$ is Riemann integrable, and integrating the three terms gives:

$$m \int_a^b g(x) \ dx \leq \int_a^b f(x) g(x) \ dx \leq M \int_a^b g(x) \ dx \tag{7}$$

Set $G = \int_a^b g(x) \ dx$ and consider the following cases:

+ if $G = 0,$ it follows from $(7)$ that the integral of the product $fg$ is zero, and hence identity $(6)$ holds for every choice of $c;$
+ if $G > 0,$ dividing $(7)$ by $G$ shows that $\frac{1}{G} \int_a^b f(x) g(x) \ dx$ lies between $m$ and $M,$ and the intermediate value theorem provides a point $c$ such that:

$$f(c) = \frac{1}{G} \int_a^b f(x) g(x) \ dx$$

The theorem has been proved for a nonnegative weight, but the same conclusion holds when $g$ is nonpositive throughout the interval. In this case the function $-g$ is nonnegative, so it satisfies the hypotheses of the case already proved.

- - -

Identity $(6)$ is the statement of the first mean value theorem for integrals. In a second form, $g$ is assumed to be [monotone](../increasing-and-decreasing-functions/) rather than of constant sign, and $f$ need only be Riemann integrable. Under these hypotheses, there exists $\xi \in [a, b]$ such that:

$$\int_a^b f(x) g(x) \ dx = g(a) \int_a^{\xi} f(x) \ dx + g(b) \int_{\xi}^b f(x) \ dx$$

This form is used in proofs of the [Dirichlet and Abel tests](../convergence-tests-for-improper-integrals/) for the convergence of [improper integrals](../improper-integrals/) with oscillatory integrands.

## Some examples

Consider a practical example in which we calculate the average value of the [square root function](../irrational-functions/) and find a point where that value is attained. We have:

$$\int_0^9 \sqrt{x} \ dx = \left[ \frac{2}{3} x^{3/2} \right]_0^9 = \frac{2}{3} \cdot 27 = 18$$

The interval has length $9,$ so the average value is:

$$\mu = \frac{1}{9} \int_0^9 \sqrt{x} \ dx = \frac{18}{9} = 2$$

To locate the point, we solve $f(c) = \mu,$ that is, $\sqrt{c} = 2,$ obtaining $c = 4,$ which lies in the interior of the interval $(0, 9).$

The point $c = 4$ lies to the left of $4.5,$ the midpoint of the interval. Since $\sqrt{x} > 2$ for $x \in (4, 9],$ the function lies above its average value on an interval of length $5,$ which is more than half the length of $[0, 9].$

- - -

As we saw in the theoretical discussion, the theorem guarantees the existence of the point $c$ but not its uniqueness. Consider, for example, the following integral:

$$\int_0^{\pi} \sin x \ dx = \left[ -\cos x \right]_0^{\pi} = -\cos \pi + \cos 0 = 1 + 1 = 2$$

The interval has length $\pi,$ so the average value is:

$$\mu = \frac{2}{\pi} \approx 0.6366$$

The admissible points are the solutions of $\sin c = 2/\pi$ on $[0, \pi].$ On this interval, since the [sine function](../sine-function/) is periodic, it takes every value in $(0, 1)$ exactly twice, at two points symmetric about $\pi/2,$ so the two solutions can be written in terms of the [arcsine function](../arcsine-function/):

$$c_1 = \arcsin \frac{2}{\pi} \approx 0.690$$

$$c_2 = \pi - \arcsin \frac{2}{\pi} \approx 2.451$$


It is therefore important to remember that the set of admissible points $c$ may consist of a single point, a finite set, or an entire interval when $f$ is constant.

- - -

Finally, consider one last example in which the weighted form changes both the average and the point where it is attained. Take the [power function](../power-function/) $f(x) = x^2$ with the weight $g(x) = x$ on $[0, 2].$ The function $f$ is continuous and $g$ is nonnegative on the interval, so the hypotheses of the theorem are satisfied. The two integrals are:

$$\int_0^2 x^2 \cdot x \ dx = \left[ \frac{x^4}{4} \right]_0^2 = 4$$

$$\int_0^2 x \ dx = \left[ \frac{x^2}{2} \right]_0^2 = 2$$

The weighted average of $f$ is the quotient of the first integral by the second, namely $4/2 = 2.$ Setting $f(c) = 2$ gives $c^2 = 2,$ whose solutions are $\pm \sqrt{2}.$ Only the positive solution belongs to the interval, so:

$$c = \sqrt{2} \approx 1.414$$

For comparison, the unweighted average of the same function on the same interval is:

$$\frac{1}{2} \int_0^2 x^2 \ dx = \frac{1}{2} \cdot \frac{8}{3} = \frac{4}{3}$$

This value is attained where $c^2 = 4/3,$ that is, at $c = 2/\sqrt{3} \approx 1.155.$ With the weight $x,$ the right-hand part of the interval is weighted more heavily than the left-hand part, and $f$ is larger there, so the weighted average exceeds the unweighted average and the point where it is attained shifts to the right.
