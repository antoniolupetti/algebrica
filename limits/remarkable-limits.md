---
title: Remarkable Limits
source: https://algebrica.org/remarkable-limits/
license: CC BY-NC 4.0
tags:
  - derivatives
  - eulers-number
  - geometric-proof
  - growth-rates
  - indeterminate-forms
  - limits
  - remarkable-limits
  - taylor-series
---
## Introduction

A small collection of [limits](../limits/) plays a central role throughout mathematical analysis. They appear in routine calculations and capture both the local behaviour of [functions](../functions/) near a regular point and their behaviour at infinity. The most important cases are collected below. 

They include trigonometric, exponential, and logarithmic expressions, as well as standard comparisons between quantities that grow without bound and those that tend to zero.

## The trigonometric fundamental limit

The most structurally significant trigonometric limit is:

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

This result characterises the local linearity of the [sine function](../sine-and-cosine/) at the origin and is equivalent to the statement that the [derivative](../derivatives/) of $\sin x$ at zero equals one:

$$\left. \frac{d}{dx} \sin x \right|_{x = 0} = 1$$

From this limit, it follows directly that for any real constant $a$:

$$\lim_{x \to 0} \frac{\sin(a x)}{a x} = 1$$

$$\lim_{x \to 0} \frac{\sin(a x)}{x} = a$$

## Geometric proof of the trigonometric fundamental limit

The classical justification of this limit relies on a comparison of areas on the unit circle. Fix an angle $x \in (0, \pi/2)$ and consider three regions sharing the vertex at the origin $O$: the triangle $OPA$, where $A = (1, 0)$ and $P = (\cos x, \sin x)$; the circular sector $OPA$; and the triangle $OQA$, where $Q$ is the intersection of the line through $O$ and $P$ with the vertical tangent to the circle at $A$, so that $Q = (1, \tan x)$.

The three regions are nested, with the triangle $OPA$ contained in the sector and the sector contained in the larger triangle $OQA$. Computing the corresponding areas one obtains the inequality:

$$\frac{1}{2}\sin x < \frac{1}{2} x < \frac{1}{2}\tan x$$

Multiplying through by $2$ gives the fundamental geometric inequality:

$$\sin x < x < \tan x \qquad \text{for } x \in (0, \pi/2)$$

Since $\sin x > 0$ on this interval, dividing each term by $\sin x$ preserves the inequalities and yields:

$$1 < \frac{x}{\sin x} < \frac{1}{\cos x}$$

Taking reciprocals reverses the inequalities and produces a two-sided bound for $\sin(x)/x$:

$$\cos x < \frac{\sin x}{x} < 1$$

As $x \to 0^+$, the lower bound $\cos x$ tends to $1$ by continuity of the cosine function at the origin, while the upper bound is the constant $1$. Applying the [squeeze theorem](../squeeze-theorem/) gives:

$$\lim_{x \to 0^+} \frac{\sin x}{x} = 1$$

The function $\sin(x)/x$ is even, so the same value is obtained as $x \to 0^-$. The two one-sided limits coincide, hence the two-sided limit exists and equals $1$.

## The tangent limit

To evaluate the [tangent](../tangent-and-cotangent/) limit, consider the identity:

$$\frac{\tan x}{x} = \frac{\sin x}{x} \cdot \frac{1}{\cos x}$$

Applying the continuity of the cosine function at the origin yields:

$$\lim_{x \to 0} \frac{\tan x}{x} = 1$$

More generally, for any real constant $a$:

$$\lim_{x \to 0} \frac{\tan(a x)}{x} = a$$

## The cosine limit

Quadratic, or second-order, behaviour emerges in the evaluation of this limit:

$$\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$$

In this case the numerator vanishes quadratically in $x$, rather than linearly. The [cosine function](../sine-and-cosine/) is tangent to the horizontal line $y = 1$ at the origin: its first derivative at $x = 0$ is zero, and the first non-vanishing term in its [Taylor expansion](../taylor-series/) is of order $x^2$. Indeed:

$$\cos x = 1 - \frac{x^2}{2} + o(x^2)$$

> Here $o(x^2)$ denotes a [little-o term](../little-o-notation/), that is, a quantity that becomes negligible compared to $x^2$ as $x \to 0$.

Dividing by $x^2$ isolates the leading quadratic term and yields the limit. More generally:

$$\lim_{x \to 0} \frac{1 - \cos(a x)}{x^2} = \frac{a^2}{2}$$

## Proof of the cosine limit

The result can be derived from the trigonometric fundamental limit through the half-angle identity:

$$1 - \cos x = 2 \sin^2\!\left(\frac{x}{2}\right)$$

Substituting this expression into the original quotient and rewriting the denominator in a form that matches the half-angle gives:

$$\frac{1 - \cos x}{x^2} = \frac{2 \sin^2(x/2)}{x^2} = \frac{1}{2}\left(\frac{\sin(x/2)}{x/2}\right)^{\!2}$$

As $x \to 0$, the argument $x/2$ also tends to $0$, so the factor inside the parentheses tends to $1$ by the trigonometric fundamental limit. Taking the square preserves the limit, and the prefactor $1/2$ remains. The result follows:

$$\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$$

## The exponential fundamental limit

The [exponential function](../exponential-function/) exhibits first-order behaviour near the origin: the deviation from the constant $1$ is linear in $x$:

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

This limit reflects the fact that the derivative of $e^x$ at the origin equals one:

$$\left. \frac{d}{dx} e^x \right|_{x = 0} = 1$$

The result follows directly from the [Taylor expansion](../taylor-series/) of $e^x$ near the origin:

$$e^x = 1 + x + \frac{x^2}{2!} + o(x^2)$$

Dividing by $x$ and taking the limit immediately yields $1$, since all higher-order terms vanish. More generally, for any real constant $a$:

$$\lim_{x \to 0} \frac{e^{a x} - 1}{x} = a$$

which follows by the substitution $u = a x$ and reduction to the standard form.

> Here $n!$ denotes the [factorial](../factorial/) of $n$, defined as the product of all positive integers up to $n$; in particular, $2! = 2$.

## Proof of the exponential fundamental limit

A self-contained proof can be obtained directly from the Taylor expansion of the exponential function at the origin:

$$e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$

Subtracting $1$ and dividing by $x$ produces:

$$\frac{e^x - 1}{x} = 1 + \frac{x}{2!} + \frac{x^2}{3!} + \frac{x^3}{4!} + \cdots$$

Every term except the first is a polynomial in $x$ vanishing at the origin. Taking the limit as $x \to 0$ leaves only the constant term:

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

> The interchange of limit and series in this argument is justified by the fact that the Taylor series of $e^x$ converges uniformly on every bounded interval, so each term may be evaluated separately at $x = 0$.

## The logarithmic fundamental limit

For the natural [logarithm](../logarithms/), the following limit holds:

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

This result corresponds to the [derivative](../derivatives/) of $\ln x$ evaluated at $x = 1$:

$$\left. \frac{d}{dx} \ln x \right|_{x = 1} = 1$$

More generally, for any real constant $a$:

$$\lim_{x \to 0} \frac{\ln(1 + a x)}{x} = a$$

## Proof of the logarithmic fundamental limit

The logarithmic limit reduces to the exponential one through a change of variable. Set:

$$y = \ln(1 + x) \quad \Longleftrightarrow \quad x = e^{y} - 1$$

The natural logarithm is continuous at $1$ with $\ln 1 = 0$, so $y \to 0$ as $x \to 0$, and the map $x \mapsto y$ is a bijection between two neighbourhoods of the origin. Rewriting the quotient in terms of $y$ gives:

$$\frac{\ln(1 + x)}{x} = \frac{y}{e^{y} - 1} = \left(\frac{e^{y} - 1}{y}\right)^{\!-1}$$

The denominator inside the parentheses tends to $1$ by the exponential fundamental limit, so the reciprocal also tends to $1$:

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

## Limits defining the exponential function

A standard limit defines Euler's number $e$:

$$\lim_{x \to 0} (1 + x)^{\frac{1}{x}} = e$$

or, equivalently, in its discrete form:

$$\lim_{n \to \infty} \left( 1 + \frac{1}{n} \right)^n = e$$

> The discrete form is obtained by restricting $x$ to values of the form $\frac{1}{n}$, where $n$ is a positive integer, so that $x \to 0$ corresponds to $n \to \infty$. Substituting yields the [sequence](../sequences/) $\left( 1 + \frac{1}{n} \right)^n$, whose limit as $n \to \infty$ coincides with that of the continuous form. A self-contained treatment of this sequence is developed in the page on the [Euler number as a limit](../euler-number-limit-sequence/).

More generally, for any real constant $a$:

$$\lim_{x \to 0} (1 + a x)^{\frac{1}{x}} = e^{a}$$
## Limits involving power functions

For any real exponent $\alpha$:

$$\lim_{x \to 0} \frac{(1 + x)^\alpha - 1}{x} = \alpha$$

This result may be derived from the [binomial expansion](../binomial-theorem/) when $\alpha$ is rational, or by logarithmic differentiation in the general case.

## Comparison of growth rates

When evaluating quotients of functions that diverge to infinity, the indeterminate form $\infty/\infty$ is resolved by knowing which factor grows faster. The principal classes of elementary functions arrange themselves into a strict hierarchy of growth at infinity. For positive constants $\alpha > 0$ and $a > 1$, the chain is:

$$\ln x \ \ll \ x^{\alpha} \ \ll \ a^{x} \ \ll \ x! \ \ll \ x^{x} \qquad \text{as } x \to +\infty$$

The symbol $f \ll g$, equivalent to the [little-o relation](../little-o-notation/) $f = o(g)$, means that the quotient $f/g$ tends to zero in the limit:

$$f \ll g \quad \Longleftrightarrow \quad \lim_{x \to +\infty} \frac{f(x)}{g(x)} = 0$$

Each link in the chain corresponds to a standard limit that is verified directly or by repeated application of [L'Hôpital's rule](../hopital-rule/). The most frequently used cases are collected here.

Logarithms grow more slowly than every positive power:

$$\lim_{x \to +\infty} \frac{\ln x}{x^{\alpha}} = 0 \qquad \alpha > 0$$

Polynomials grow more slowly than every exponential with base greater than one:

$$\lim_{x \to +\infty} \frac{x^{n}}{a^{x}} = 0 \qquad n \in \mathbb{N}, \ a > 1$$

In the discrete setting, exponentials grow more slowly than the factorial:

$$\lim_{n \to +\infty} \frac{a^{n}}{n!} = 0 \qquad a > 0$$

Finally, the factorial itself is dominated by the self-power $n^{n}$:

$$\lim_{n \to +\infty} \frac{n!}{n^{n}} = 0$$

These comparisons govern the asymptotic behaviour of expressions encountered throughout calculus. They are decisive in the study of the convergence of [series](../series/), where the term being summed must decrease quickly enough, and they play an equally central role in the analysis of algorithms, where the running time of a procedure is classified according to the same hierarchy.

> The notation $f \ll g$ used here is the strict-domination version of [little-o notation](../little-o-notation/) as $x \to +\infty$. The reciprocal hierarchy $g \gg f$ describes the same situation from the perspective of the dominant function.

## Asymptotic equivalence

The remarkable limits collected above can be reformulated as local asymptotic equivalences near the origin:

$$\sin x \sim x \qquad \tan x \sim x \qquad 1 - \cos x \sim \frac{x^2}{2}$$

$$e^x - 1 \sim x \qquad \ln(1 + x) \sim x$$

The notation $f(x) \sim g(x)$ as $x \to 0$ means that the two functions are asymptotically equivalent near the origin:

$$\lim_{x \to 0} \frac{f(x)}{g(x)} = 1$$

Each of these relationships corresponds to the first nonzero term in the local [Taylor expansion](../taylor-series/) of a smooth function near a regular point. As a consequence, these equivalences can be used to replace more complex expressions with simpler ones when evaluating limits and to resolve [indeterminate forms](../indeterminate-forms/).

## Structural interpretation

From a more advanced viewpoint, remarkable limits are expressions of differentiability and local linearisation. Every limit of the form:

$$\lim_{x \to 0} \frac{f(x) - f(0)}{x}$$

coincides with the definition of the [derivative](../derivatives/) of $f$ at the origin. The classical remarkable limits are exactly those particular cases in which this derivative can be computed explicitly. They then serve as a starting point for resolving more complex [indeterminate forms](../indeterminate-forms/), often in combination with [L'Hôpital's rule](../hopital-rule/) or with [little-o notation](../little-o-notation/) inside Taylor expansions.

## Summary

The following table summarizes the most common remarkable limits. These results play a fundamental role in differential and integral calculus and frequently serve as the starting point for evaluating more complicated limits through algebraic manipulations, substitutions, asymptotic equivalence, or [L’Hôpital’s rule](../hopital-rule/).

[class="table-1"]

|                                                         |                  |
| ------------------------------------------------------- | ---------------- |
| $\lim_{x \to 0} \dfrac{\sin x}{x}$                      | $1$              |
| $\lim_{x \to 0} \dfrac{\sin(a x)}{a x}$                 | $1$              |
| $\lim_{x \to 0} \dfrac{\sin(a x)}{x}$                   | $a$              |
| $\lim_{x \to 0} \dfrac{\tan x}{x}$                      | $1$              |
| $\lim_{x \to 0} \dfrac{\tan(a x)}{x}$                   | $a$              |
| $\lim_{x \to 0} \dfrac{1 - \cos x}{x^2}$                | $\dfrac{1}{2}$   |
| $\lim_{x \to 0} \dfrac{1 - \cos(a x)}{x^2}$             | $\dfrac{a^2}{2}$ |
| $\lim_{x \to 0} \dfrac{e^x - 1}{x}$                     | $1$              |
| $\lim_{x \to 0} \dfrac{e^{a x} - 1}{x}$                 | $a$              |
| $\lim_{x \to 0} \dfrac{\ln(1 + x)}{x}$                  | $1$              |
| $\lim_{x \to 0} \dfrac{\ln(1 + a x)}{x}$                | $a$              |
| $\lim_{x \to 0} (1 + x)^{1/x}$                          | $e$              |
| $\lim_{n \to \infty} \left( 1 + \dfrac{1}{n} \right)^n$ | $e$              |
| $\lim_{x \to 0} (1 + a x)^{1/x}$                        | $e^a$            |
| $\lim_{x \to 0} \dfrac{(1 + x)^\alpha - 1}{x}$          | $\alpha$         |

[/class]