---
title: Integration by Substitution
source: https://algebrica.org/integration-by-substitution/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - chain-rule
  - change-of-variable
  - composite-functions
  - definite-integral
  - indefinite-integral
  - integration
  - integration-by-substitution
  - trigonometric-substitution
---
## How substitution simplifies integration

Integration by substitution simplifies an [integral](../indefinite-integrals/) by changing the variable of integration. If $F' = f,$ the substitution $u = g(x)$ gives:

$$\int f(g(x))g'(x) \ dx = F(g(x)) + c$$

The procedure has four steps:

+ Set $u = g(x),$ where the structure of the integrand suggests $g(x).$
+ Differentiate to obtain $du = g'(x) \ dx.$
+ Rewrite every factor and differential in terms of $u.$
+ Integrate with respect to $u.$ For an indefinite integral, replace $u$ by $g(x).$ For a definite integral, use limits expressed in $u.$

> Substitution is the reverse of the [chain rule](../the-derivative-of-a-composite-function/). The inner function and its derivative determine the change of variable.

- - -

The substitution rule follows from the chain rule for [derivatives](../derivatives/). If $F(x) = H(g(x)),$ the chain rule gives:

$$F'(x) = H'(g(x)) g'(x)$$

An integrand of the form $H'(g(x))g'(x)$ is therefore the derivative of the composite function $H(g(x)).$ With $u = g(x),$ its antiderivative is:

$$\int H'(u) \ du = H(u) + c$$

## Recognising when to use substitution

A substitution is useful when the integrand contains a [composite function](../composite-functions/) together with a factor proportional to the derivative of its inner function. The basic pattern is:

$$f(g(x)) g'(x)$$

The integrand may differ from this pattern by a constant factor. The substitution $u = g(x)$ replaces $g(x)$ by $u$ and $g'(x) \ dx$ by $du.$ Expressions such as $(ax + b)^n,$ $\sqrt{ax + b},$ $\ln(ax + b),$ and $e^{ax + b}$ suggest the inner linear function $ax + b$ as the new variable. A rational expression may have the form:

$$\frac{g'(x)}{g(x)}$$

If the numerator is $g'(x)$ up to a constant factor, set $u = g(x).$

> Choose an inner expression whose derivative occurs elsewhere in the integrand, exactly or up to a nonzero constant factor. A complete substitution leaves no occurrence of the original variable in the transformed integral.

## Substitution patterns

The table lists common integrand patterns and a suitable substitution for each one:

[class="table-1"]

|                                  |              |
| -------------------------------- | ------------ |
| $$\int f(g(x)) g'(x) \ dx$$      | $$u = g(x)$$ |
| $$\int (ax + b)^n \ dx$$         | $$u = ax + b$$ |
| $$\int e^{ax + b} \ dx$$         | $$u = ax + b$$ |
| $$\int \ln(ax + b) \ dx$$        | $$u = ax + b$$ |
| $$\int \dfrac{g'(x)}{g(x)} \ dx$$ | $$u = g(x)$$ |

[/class]

## Example 1

Consider the following integral:

$$\int (2x + 1)^3 \ dx$$

Set $u = 2x + 1$ to replace the cubic expression by $u^3.$ Differentiation gives:

$$du = 2 \ dx$$

This relation is equivalent to:

$$dx = \frac{du}{2}$$

The substituted integral is:

$$\int \frac{u^3}{2} \ du = \frac{1}{2}\int u^3 \ du$$

The power rule gives:

$$\frac{1}{2}\left(\frac{u^4}{4}\right) + c = \frac{u^4}{8} + c$$

Replacing $u$ by $2x + 1$ gives:

$$\int (2x + 1)^3 \ dx = \frac{1}{8}(2x + 1)^4 + c$$

## Example 2

Evaluate the following integral:

$$\int \frac{1}{3x - 5} \ dx$$

Set $u = 3x - 5$ to replace the denominator by $u.$ Differentiation gives:

$$du = 3 \ dx$$

This relation is equivalent to:

$$dx = \frac{du}{3}$$

The substituted integral is:

$$\int \frac{1}{3u} \ du = \frac{1}{3}\int \frac{du}{u}$$

The logarithmic formula gives:

$$\frac{1}{3}\ln|u| + c$$

Replacing $u$ by $3x - 5$ gives:

$$\int \frac{1}{3x - 5} \ dx = \frac{1}{3}\ln|3x - 5| + c$$

## Example 3

Evaluate the following integral:

$$\int x \sin(x^2) \ dx$$

The inner expression $x^2$ has derivative $2x,$ so the integrand contains one half of its differential. Set $u = x^2.$ This substitution gives:

$$du = 2x \ dx \qquad x \ dx = \frac{1}{2} \ du$$

The substitution gives:

$$\int x\sin(x^2) \ dx = \frac{1}{2}\int \sin u \ du$$

The transformed antiderivative is:

$$\frac{1}{2}\int \sin u \ du = -\frac{1}{2}\cos u + c$$

Replacing $u$ by $x^2$ gives:

$$\int x\sin(x^2) \ dx = -\frac{1}{2}\cos(x^2) + c$$

## Example 4

On an open interval where $\sin x > 0,$ evaluate the following integral:

$$\int \cos x \sqrt{\sin x} \ dx$$

The substitution $u = \sin x$ replaces the radical by $\sqrt{u}.$ Its differential is:

$$du = \cos x \ dx$$

The substituted integral is:

$$\int \sqrt{u} \ du = \int u^{1/2} \ du$$

The power rule gives:

$$\int u^{1/2} \ du = \frac{u^{3/2}}{3/2} = \frac{2}{3} u^{3/2} + c$$

Replacing $u$ by $\sin x$ gives:

$$\int \cos x\sqrt{\sin x} \ dx = \frac{2}{3}(\sin x)^{3/2} + c$$

## Trigonometric substitutions

Trigonometric substitution is useful for radicals containing the quadratic expressions $a^2 - x^2,$ $a^2 + x^2,$ and $x^2 - a^2,$ where $a > 0.$ The relevant formulas follow from the [fundamental trigonometric identity](../pythagorean-identity/):

$$\sin^2 x + \cos^2 x = 1$$

This identity has the following equivalent forms:

$$
\begin{align}
\cos^2 x &= 1 - \sin^2 x \\[6pt]
\sec^2 x &= 1 + \tan^2 x \\[6pt]
\tan^2 x &= \sec^2 x - 1
\end{align}
$$

For $a > 0,$ the standard substitution depends on the expression under the radical:

+ For $a^2 - x^2,$ set $x = a\sin u.$
+ For $a^2 + x^2,$ set $x = a\tan u.$
+ For $x^2 - a^2,$ set $x = a\sec u.$

> The page on [trigonometric substitution for integrals](../trigonometric-substitution-for-integrals/) develops the geometric basis and gives complete worked examples.

## Example 5

Evaluate the following integral:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx$$

For $|x| < 3,$ choose $u \in (-\pi/2, \pi/2)$ and set:

$$x = 3\sin u$$

The differential is:

$$dx = 3\cos u \ du$$

The denominator after substitution is:

$$\sqrt{9 - x^2} = \sqrt{9 - 9\sin^2 u} = \sqrt{9(1 - \sin^2 u)}$$

On the chosen interval $\cos u > 0.$ The identity $\sin^2 u + \cos^2 u = 1$ gives:

$$\sqrt{9(1 - \sin^2 u)} = \sqrt{9\cos^2 u} = 3\lvert\cos u\rvert = 3\cos u$$

The integral is:

$$\int \frac{3\cos u \ du}{3\cos u} = \int \ du = u + c$$

Since $u$ is in the principal range of the [arcsine](../arcsine-function/) function, the equation $x = 3\sin u$ implies:

$$u = \arcsin\left(\frac{x}{3}\right)$$

The antiderivative in the original variable is:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx = \arcsin\left(\frac{x}{3}\right) + c$$

## Substitution rule for definite integrals

If we evaluate a transformed [definite integral](../definite-integrals/) in $u,$ its limits are values of $u.$ Alternatively, we may find an antiderivative in $u,$ replace $u$ by $g(x),$ and then use the original limits in $x.$ Assume that $g$ is continuously differentiable on $[a,b]$ and $f$ is continuous on an interval containing $g([a,b]).$ Under these hypotheses, the substitution rule is:

$$\int_a^b f(g(x))g'(x) \ dx = \int_{g(a)}^{g(b)} f(u) \ du$$

- - -

Evaluate the following definite integral:

$$\int_{0}^{1} x\cos(x^2) \ dx$$

Set $u = x^2.$ This substitution gives:

$$du = 2x \ dx \qquad x \ dx = \frac{1}{2} \ du$$

The transformed endpoints are $u(0) = 0$ and $u(1) = 1.$ Here they coincide numerically with the original bounds. The integral is:

$$\int_0^1 x\cos(x^2) \ dx = \frac{1}{2}\int_0^1 \cos u \ du$$

The [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/) gives:

$$\frac{1}{2}\Bigl[\sin u\Bigr]_{0}^{1} = \frac{1}{2}(\sin 1 - \sin 0) = \frac{\sin 1}{2}$$

## Decision procedure

The following steps show when substitution applies and how to carry it out.

+ Identify the structure of the integrand. When it matches a standard form (power, exponential, logarithmic, or trigonometric), use the corresponding formula in [indefinite integrals](../indefinite-integrals/).
+ After checking for a direct substitution, consider a trigonometric substitution when a radical contains $a^2 - x^2,$ $a^2 + x^2,$ or $x^2 - a^2,$ where $a > 0.$ The standard choices are $x = a\sin u,$ $x = a\tan u,$ and $x = a\sec u,$ respectively. The entry on [trigonometric substitution for integrals](../trigonometric-substitution-for-integrals/) gives the full procedure.
+ When the integrand has the form $f(g(x))g'(x),$ set $u = g(x),$ compute $du = g'(x) \ dx,$ rewrite the integral entirely in $u,$ and use the corresponding standard formula.
+ For a definite integral evaluated in $u,$ replace the original limits by $g(a)$ and $g(b).$ If the antiderivative is first expressed in $x,$ retain the original limits.
+ For an indefinite integral, replace $u$ by $g(x)$ to express the antiderivative in $x.$
+ For a product of two functions, [integration by parts](../integration-by-parts/) is useful when differentiation simplifies one factor and the other has an antiderivative that is easy to compute. The [Weierstrass substitution](../weierstrass-substitution/) converts every rational function of $\sin x$ and $\cos x$ into a rational function of the new variable.

## Further worked examples

The table lists integrals in increasing order of difficulty. A sentence before each solution identifies the feature of the integrand that suggests the substitution. In the later examples, the solution also transforms the limits, rewrites an algebraic factor, or uses a trigonometric substitution.

[class="table-1"]

|                                             |
| :------------------------------------------ |
| $\int \dfrac{dt}{(1 - 6t)^4}$               |
| $\int x^3(2 + x^4)^5 \ dx$                  |
| $\int \cos^3\theta\sin\theta \ d\theta$     |
| $\int \dfrac{2^{\ln x}}{x} \ dx$            |
| $\int_0^{\ln 4} \dfrac{e^t}{1 + 2e^t} \ dt$ |
| $\int_{\pi/4}^{\pi/3} \csc^2(5x) \ dx$      |
| $\int \dfrac{9x^3}{\sqrt{1 + x^2}} \ dx$    |
| $\int_0^1 \sqrt{4 - x^2} \ dx$              |
[/class]

The denominator is a power of the linear expression $1 - 6t,$ whose derivative is constant.

$$u = 1 - 6t \qquad du = -6 \ dt$$

$$
\begin{align}
\int \frac{dt}{(1 - 6t)^4} &= -\frac{1}{6} \int u^{-4} \ du \\[6pt]
&= \frac{1}{18}u^{-3} + c \\[6pt]
&= \frac{1}{18(1 - 6t)^3} + c
\end{align}
$$

- - -

The factor $x^3$ is proportional to the derivative of the inner expression $2 + x^4.$

$$u = 2 + x^4 \qquad du = 4x^3 \ dx$$

$$
\begin{align}
\int x^3(2 + x^4)^5 \ dx &= \frac{1}{4} \int u^5 \ du \\[6pt]
&= \frac{u^6}{24} + c \\[6pt]
&= \frac{(2 + x^4)^6}{24} + c
\end{align}
$$

- - -

The factor $\sin\theta$ is the negative derivative of $\cos\theta.$

$$u = \cos\theta \qquad du = -\sin\theta \ d\theta$$

$$
\begin{align}
\int \cos^3\theta\sin\theta \ d\theta &= -\int u^3 \ du \\[6pt]
&= -\frac{u^4}{4} + c \\[6pt]
&= -\frac{\cos^4\theta}{4} + c
\end{align}
$$

- - -

For $x > 0,$ the exponent $\ln x$ has derivative $1/x,$ which is the other factor in the integrand.

$$u = \ln x \qquad du = \frac{1}{x} \ dx$$

$$
\begin{align}
\int \frac{2^{\ln x}}{x} \ dx &= \int 2^u \ du \\[6pt]
&= \frac{2^u}{\ln 2} + c \\[6pt]
&= \frac{2^{\ln x}}{\ln 2} + c
\end{align}
$$

- - -

The denominator $1 + 2e^t$ has derivative $2e^t,$ which is twice the numerator. We transform the limits together with the variable.

$$u = 1 + 2e^t \qquad du = 2e^t \ dt$$

$$t = 0 \Longrightarrow u = 3 \qquad t = \ln 4 \Longrightarrow u = 9$$

$$
\begin{align}
\int_0^{\ln 4} \frac{e^t}{1 + 2e^t} \ dt &= \frac{1}{2} \int_3^9 \frac{1}{u} \ du \\[6pt]
&= \frac{1}{2}\Bigl[\ln u\Bigr]_3^9 \\[6pt]
&= \frac{1}{2}\ln 3
\end{align}
$$

- - -

The linear argument $5x$ has constant derivative. We transform the limits before integrating $\csc^2u.$

$$u = 5x \qquad du = 5 \ dx$$

$$x = \frac{\pi}{4} \Longrightarrow u = \frac{5\pi}{4} \qquad x = \frac{\pi}{3} \Longrightarrow u = \frac{5\pi}{3}$$

$$
\begin{align}
\int_{\pi/4}^{\pi/3} \csc^2(5x) \ dx &= \frac{1}{5} \int_{5\pi/4}^{5\pi/3} \csc^2u \ du \\[6pt]
&= -\frac{1}{5}\Bigl[\cot u\Bigr]_{5\pi/4}^{5\pi/3} \\[6pt]
&= \frac{1}{5}\left[\cot\left(\frac{5\pi}{4}\right) - \cot\left(\frac{5\pi}{3}\right)\right] \\[6pt]
&= \frac{1}{5}\left(1 + \frac{\sqrt{3}}{3}\right)
\end{align}
$$

- - -

The expression $1 + x^2$ has derivative $2x.$ After the substitution $u = 1 + x^2,$ the remaining factor is $x^2 = u - 1.$

$$u = 1 + x^2 \qquad du = 2x \ dx \qquad x^2 = u - 1$$

$$
\begin{align}
\int \frac{9x^3}{\sqrt{1 + x^2}} \ dx &= \frac{9}{2} \int \frac{u - 1}{\sqrt{u}} \ du \\[6pt]
&= \frac{9}{2} \int \left(u^{1/2} - u^{-1/2}\right) \ du \\[6pt]
&= 3u^{3/2} - 9u^{1/2} + c \\[6pt]
&= 3(x^2 - 2)\sqrt{1 + x^2} + c
\end{align}
$$

- - -

The radical has the form $\sqrt{a^2 - x^2},$ so we set $x = 2\sin\theta.$ The transformed interval is $[0, \pi/6],$ on which $\cos\theta \geq 0.$

$$x = 2\sin\theta \qquad dx = 2\cos\theta \ d\theta$$

$$x = 0 \Longrightarrow \theta = 0 \qquad x = 1 \Longrightarrow \theta = \frac{\pi}{6}$$

$$\sqrt{4 - x^2} = \sqrt{4 - 4\sin^2\theta} = \sqrt{4\cos^2\theta} = 2\cos\theta$$

$$
\begin{align}
\int_0^1 \sqrt{4 - x^2} \ dx &= 4 \int_0^{\pi/6} \cos^2\theta \ d\theta \\[6pt]
&= 2 \int_0^{\pi/6} \left(1 + \cos(2\theta)\right) \ d\theta \\[6pt]
&= \Bigl[2\theta + \sin(2\theta)\Bigr]_0^{\pi/6} \\[6pt]
&= \frac{\pi}{3} + \frac{\sqrt{3}}{2}
\end{align}
$$
