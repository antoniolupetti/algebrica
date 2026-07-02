---
title: L'Hopital's Rule
source: https://algebrica.org/hopital-rule/
license: CC BY-NC 4.0
tags:
  - derivatives
  - differential-calculus-theorems
  - hopital-rule
  - indeterminate-forms
  - limits
---

## Statement

L'Hôpital's rule is a method for evaluating certain [limits](../limits/) that yield in [indeterminate forms](../indeterminate-forms/). The theorem provides a criterion for resolving the indeterminate behaviour of the limit of a quotient of two functions by using their [derivatives](../derivatives/). By indeterminate forms, we mean expressions of the type:

$$\frac{0}{0} \qquad \frac{\infty}{\infty}$$

These expressions prevent the direct evaluation of a limit, as they describe situations in which the basic limit theorems are insufficient to determine the result, and additional analytical techniques are required.

Let $f(x)$ and $g(x)$ be two [functions](../functions/) defined on a punctured neighbourhood $I$ of a point $x_0$. Assume that the following conditions are satisfied:

+ $f(x)$ and $g(x)$ are differentiable on $I$, except possibly at $x_0$.
+ $g'(x) \neq 0$ for every $x \in I$ with $x \neq x_0$.
+ $\displaystyle \lim_{x \to x_0} f(x) = \lim_{x \to x_0} g(x) = 0$.
+ The following limit exists, finite or infinite:

$$\lim_{x \to x_0} \frac{f'(x)}{g'(x)}$$

Under these assumptions the original limit also exists and is equal to the limit of the ratio of the derivatives:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)}$$

> In simpler terms, when the quotient of two functions presents itself as an indeterminate form $0/0$, its limit can be determined by evaluating the limit of the ratio of their derivatives, provided that this latter limit exists.

- - -
The rule applies in an analogous way to the indeterminate form $\infty/\infty$. Suppose that $f(x) \to \pm\infty$ and $g(x) \to \pm\infty$ as $x \to x_0$, and that the remaining conditions on differentiability and on $g'(x)$ are satisfied. If the limit of the ratio of the derivatives exists, then the original limit is equal to this value:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)}$$

The rule remains valid when $x_0$ is replaced by $+\infty$ or $-\infty$, with no change in the form of the statement. In this case, the hypotheses on differentiability and on $g'$ are imposed on a half-line of the form $(M, +\infty)$ or $(-\infty, M)$, and the limits are computed accordingly.

> The conclusion of the rule fails when the limit of the ratio of the derivatives does not exist. A classical counterexample is given by $f(x) = x + \sin x$ and $g(x) = x$ as $x \to +\infty$: the original quotient tends to $1$, but the quotient of the derivatives $1 + \cos x$ has no limit. It is therefore essential to verify that the limit of the ratio of the derivatives actually exists before applying the theorem.

## Proof

We prove the rule for the form $0/0$. The case $\infty/\infty$ can be handled in an analogous way, with adaptations that are standard in advanced calculus. We treat the right limit $x \to x_0^+$, the case $x \to x_0^-$ being symmetric, and the bilateral limit being obtained by combining the two.

Since $\displaystyle \lim_{x \to x_0} f(x) = \lim_{x \to x_0} g(x) = 0$, we extend the two functions continuously to $x_0$ by setting $f(x_0) = g(x_0) = 0$. With this extension $f$ and $g$ are continuous on $I$ and differentiable on $I \setminus \{x_0\}$, with $g'(x) \neq 0$.

Fix an arbitrary $x \in I$ with $x > x_0$. By applying [Cauchy's theorem](../cauchy-theorem/) to $f$ and $g$ on the closed interval $[x_0, x]$, there exists a point $c \in (x_0, x)$ such that:

$$\frac{f(x) - f(x_0)}{g(x) - g(x_0)} = \frac{f'(c)}{g'(c)}$$

Using $f(x_0) = g(x_0) = 0$, the equation simplifies to:

$$\frac{f(x)}{g(x)} = \frac{f'(c)}{g'(c)}$$

At this stage the point $c$ is not fixed: it depends on $x$. More precisely, for each $x \neq x_0$, Cauchy's theorem guarantees the existence of a point $c = c(x)$ such that:

$$x_0 < c(x) < x \quad \text{if } x > x_0$$

$$x < c(x) < x_0 \quad \text{if } x < x_0$$

Consider for instance the right limit and let $x \to x_0^+$. Then $0 < c(x) - x_0 < x - x_0$, and since $x - x_0 \to 0$, by the [squeeze theorem](../squeeze-theorem/) it follows that $c(x) - x_0 \to 0$, hence $c(x) \to x_0$. An analogous argument applies to the left limit.

By hypothesis, the following limit exists, finite or infinite:

$$L = \lim_{t \to x_0} \frac{f'(t)}{g'(t)}$$

Since $c(x) \to x_0$ as $x \to x_0$ and $c(x) \neq x_0$ for every $x \in I$ with $x \neq x_0$, by composition of limits we obtain:

$$\lim_{x \to x_0} \frac{f'(c(x))}{g'(c(x))} = L$$

Combining this with the equality $f(x)/g(x) = f'(c(x))/g'(c(x))$ established above, we obtain:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = L = \lim_{x \to x_0} \frac{f'(x)}{g'(x)}$$

This value is what we wanted to prove. Note that the argument does not require the continuity of the derivatives at $x_0$. The existence of the limit of $f'/g'$ at $x_0$, assumed in the statement, is by itself sufficient to guarantee the conclusion via the composition of limits.

## Proof of the case $\infty/\infty$

The argument for the form $\infty/\infty$ requires a slightly different construction because the trick of setting $f(x_0) = g(x_0) = 0$ is not available. We treat the right limit $x \to x_0^+$, with $f(x), g(x) \to +\infty$; the other cases are obtained by symmetry or by changing signs.

Assume that the limit of $f'/g'$ exists and is finite, equal to $L$. Fix $\varepsilon > 0$. By definition of limit, there exists a neighbourhood $(x_0, x_0 + \delta)$ on which:

$$
\left| \frac{f'(t)}{g'(t)} - L \right| < \frac{\varepsilon}{2} \quad \forall t \in (x_0, x_0 + \delta)
$$

Fix a point $y \in (x_0, x_0 + \delta)$ and consider the auxiliary interval $[x, y]$ with $x_0 < x < y$. By [Cauchy's theorem](../cauchy-theorem/) applied to $f$ and $g$ on $[x, y]$, there exists $c \in (x, y)$ such that:

$$
\frac{f(x) - f(y)}{g(x) - g(y)} = \frac{f'(c)}{g'(c)}
$$

The point $c$ lies in $(x_0, x_0 + \delta)$, so the right-hand side stays within distance $\varepsilon/2$ from $L$. Rewriting the left-hand side as a quotient that involves $f(x)/g(x)$:

$$
\frac{f(x)}{g(x)} \cdot \frac{1 - f(y)/f(x)}{1 - g(y)/g(x)} = \frac{f'(c)}{g'(c)}
$$

Since $f(x), g(x) \to +\infty$ as $x \to x_0^+$, the ratios $f(y)/f(x)$ and $g(y)/g(x)$ tend to zero, so the correction factor on the left-hand side tends to $1$. For $x$ sufficiently close to $x_0$ the absolute difference between $f(x)/g(x)$ and $f'(c)/g'(c)$ becomes smaller than $\varepsilon/2$. Combining the two bounds:

$$
\left| \frac{f(x)}{g(x)} - L \right| < \varepsilon
$$

for every $x$ in a suitably restricted right neighbourhood of $x_0$. The arbitrariness of $\varepsilon$ proves that $f(x)/g(x) \to L$.

- - -
The case $L = +\infty$ is treated analogously, with the inequality $f'(t)/g'(t) > N$ replacing the two-sided bound, and the case $L = -\infty$ by symmetry. The same argument adapts to the limits at infinity, $x \to +\infty$ and $x \to -\infty$, with the role of the neighbourhood $(x_0, x_0 + \delta)$ played by a half-line of the form $(M, +\infty)$.

> The technical core of the $\infty/\infty$ case is the algebraic manipulation that isolates $f(x)/g(x)$ and treats the residual factor as a perturbation tending to $1$. The hypotheses $g'(x) \neq 0$ and the existence of the limit $\lim f'/g'$ are the same as in the $0/0$ case and are used at the same points of the argument.

## Example 1

Let us compute the following limit involving the [sine function](../sine-function/):

$$\lim_{x \to 0} \frac{\sin x}{x}$$

At first glance, this expression leads to an indeterminate form. Indeed, substituting $x = 0$ we obtain:

$$\frac{\sin 0}{0} = \frac{0}{0}$$

The functions $\sin x$ and $x$ satisfy the hypotheses of L'Hôpital's rule, so the limit of the quotient can be replaced by the limit of the ratio of the derivatives:

$$\lim_{x \to 0} \frac{\sin x}{x} = \lim_{x \to 0} \frac{(\sin x)'}{(x)'} = \lim_{x \to 0} \frac{\cos x}{1}$$

> The hypotheses of the theorem are satisfied: $\sin x$ and $x$ are [continuous functions](../continuous-functions/) at $x_0 = 0$, with $\sin(0) = 0$ and $x\big|_{x=0} = 0$. Both functions are differentiable on every open interval containing $0$, and the derivative of the denominator, $g'(x) = 1$, never vanishes.

- - -
The remaining expression is no longer indeterminate. By evaluating the cosine at $0$ we obtain:

$$\lim_{x \to 0} \frac{\cos x}{1} = \frac{\cos(0)}{1} = 1$$

We can therefore conclude that:

$$\lim_{x \to 0} \frac{\sin x}{x} = \lim_{x \to 0} \frac{\cos x}{1} = 1$$

## Example 2

Let us now consider a more involved situation in which the expression results in an indeterminate form of the type $-\infty + \infty$. In such cases the recommended approach is to rewrite the difference between the two functions as a product or a quotient, so that the expression is brought back to one of the standard forms to which L'Hôpital's rule applies, namely:

$$\frac{0}{0} \quad \text{or} \quad \frac{\infty}{\infty}$$

- - -
Consider the following limit:

$$\lim_{x \to 0} \left(\frac{1}{\sin x} - \frac{2}{x}\right)$$

The limit leads to an indeterminate form of type $-\infty + \infty$. To apply L'Hôpital's rule we first rewrite it as a single fraction, thus obtaining an indeterminate form of type $0/0$:

$$\lim_{x \to 0} \left(\frac{1}{\sin x} - \frac{2}{x}\right) = \lim_{x \to 0} \frac{x - 2\sin x}{x \sin x}$$

> Before applying the rule, it is always necessary to verify that the conditions of the theorem are satisfied for the rewritten expression.

- - -
Computing the derivatives of the numerator and the denominator, the limit becomes:

$$\lim_{x \to 0} \frac{1 - 2\cos x}{\sin x + x \cos x}$$

Substituting $x = 0$ in the resulting expression gives $-1/0$, which shows that the limit diverges. The result is therefore:

$$\lim_{x \to 0} \frac{1 - 2\cos x}{\sin x + x \cos x} = -\infty$$

> If the application of L'Hôpital's rule yields a quotient that still presents an [indeterminate form](../indeterminate-forms/), the rule may be applied repeatedly, provided that the conditions of the theorem are met at each step. At each iteration it is essential to verify that both the new numerator and the new denominator approach either $0$ or $\pm\infty$.

## Indeterminate products

The same principle illustrated in the previous example also applies to indeterminate forms of the type $0 \cdot \infty$, which arise from the product of two functions $f(x) \cdot g(x)$. To rewrite the expression in a form suitable for L'Hôpital's rule, it is enough to express the product as a quotient:

$$f(x) \cdot g(x) = \frac{f(x)}{\dfrac{1}{g(x)}} \quad \text{or} \quad f(x) \cdot g(x) = \frac{g(x)}{\dfrac{1}{f(x)}}$$

- - -
For example, consider the following limit:

$$\lim_{x \to 0^+} x \ln x$$

This expression is an indeterminate form of type $0 \cdot (-\infty)$. The product can be rewritten as a quotient:

$$\lim_{x \to 0^+} x \ln x = \lim_{x \to 0^+} \frac{\ln x}{\dfrac{1}{x}}$$

The resulting expression is now an indeterminate form of type $\infty/\infty$, suitable for the application of L'Hôpital's rule:

$$\lim_{x \to 0^+} \frac{\ln x}{\dfrac{1}{x}} = \lim_{x \to 0^+} \frac{(\ln x)'}{\left(\dfrac{1}{x}\right)'} = \lim_{x \to 0^+} \frac{\dfrac{1}{x}}{-\dfrac{1}{x^2}} = \lim_{x \to 0^+} (-x) = 0$$

## Exponential indeterminate forms

A further class of indeterminate forms that can be addressed through L'Hôpital's rule consists of the exponential forms:

$$0^0 \qquad \infty^0 \qquad 1^\infty$$

These arise from the limit of expressions of the form $f(x)^{g(x)}$ whenever the base and the exponent tend to specific values that prevent the direct evaluation of the power. The standard technique consists in taking the natural logarithm of the expression, in order to convert the power into a product, which is then handled with the methods discussed above.

Set $y = f(x)^{g(x)}$. Taking the [logarithm](../logarithms/) yields:

$$\ln y = g(x) \ln f(x)$$

The limit of $\ln y$ is computed by transforming the product $g(x) \ln f(x)$ into a quotient and applying L'Hôpital's rule. Once the value $L = \lim \ln y$ has been obtained, the limit of the original expression follows by exponentiation:

$$\lim f(x)^{g(x)} = e^{L}$$

As an illustration, consider the limit:

$$\lim_{x \to 0^+} x^x$$

The expression represents an indeterminate form of type $0^0$. Setting $y = x^x$ and taking the logarithm we obtain $\ln y = x \ln x$, and the corresponding limit was already computed in the previous section:

$$\lim_{x \to 0^+} x \ln x = 0$$

The limit of the original expression is therefore:

$$\lim_{x \to 0^+} x^x = e^{0} = 1$$

> Beyond the evaluation of plain limits, L'Hôpital's rule is the standard tool for analysing the asymptotic behaviour of an integrand at infinity or near a singular point, and it is therefore the natural entry point for the convergence analysis of [improper integrals](../improper-integrals/).

> L'Hopital's rule rests on [Cauchy's theorem](../cauchy-theorem/), itself a refinement of [Lagrange's theorem](../lagrange-theorem/) and, ultimately, of [Rolle's theorem](../rolle-theorem/). The existence theorems that ground the chain are [Fermat's theorem](../fermat-theorem/) for the location of stationary points and [Weierstrass' theorem](../weierstrass-theorem/) for the attainment of extrema on closed intervals.
