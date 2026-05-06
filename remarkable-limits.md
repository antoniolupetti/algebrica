# Remarkable Limits

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/remarkable-limits/

# Introduction 

Notable [limits](../limits/) play a central role in mathematical analysis. They are used in calculations and help describe both the local behaviour of [functions](../functions) and their behaviour at infinity. The most important cases are collected below. They include trigonometric, exponential, and logarithmic expressions, as well as standard comparisons between quantities that grow without bound and those that tend to zero.

- - -
## The trigonometric fundamental limit

The most fundamental and structurally significant trigonometric limit is given by:

\\[
\lim_{x \to 0} \frac{\sin x}{x} = 1
\\]

This result characterizes the local linearity of the [sine function](../sine-function/) at the origin and is equivalent to the following statement:

\\[
\left.\frac{d}{dx}\sin x\right|_{x=0} = 1
\\]

From this limit, it follows directly that for any real constant a we have:

\\[\lim_{x \to 0} \frac{\sin(ax)}{ax} = 1\\]
\\[\lim_{x \to 0} \frac{\sin(ax)}{x} = a\\]

- - -
## The tangent limit

To evaluate the [tangent](../tangent-function/) limit, consider the following identity:

\\[
\frac{\tan x}{x} = \frac{\sin x}{x} \cdot \frac{1}{\cos x}
\\]

Applying the continuity of the cosine function at the origin yields:

\\[
\lim_{x \to 0} \frac{\tan x}{x} = 1
\\]

More generally, for any real constant \\(a\\) we have:

\\[
\lim_{x \to 0} \frac{\tan(ax)}{x} = a
\\]

- - -
## The cosine limit

Quadratic, or second-order, behaviour emerges in the evaluation of this limit:

\\[
\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}
\\]

In this case, the numerator vanishes quadratically with respect to \\(x\\), rather than linearly. The [cosine function](../cosine-function/) is tangent to the horizontal line \\(y = 1\\) at the origin: its first derivative at \\(x = 0\\) is zero, and the first non-vanishing term in its Taylor expansion is of order \\(x^2\\). Indeed:
\\[
\cos x = 1 - \frac{x^2}{2} + o(x^2)
\\]

> Here \\( o(x^2) \\) denotes the [little-o notation](../little-o-notation/), meaning a term that becomes negligible compared to \\( x^2 \\) as \\( x \to 0 \\).

Dividing by \\(x^2\\) isolates the leading quadratic term and yields the limit. More generally we have:

\\[
\lim_{x \to 0} \frac{1 - \cos(ax)}{x^2} = \frac{a^2}{2}
\\]

- - -
## The exponential fundamental limit

The [exponential function](../exponential-function/) exhibits first-order behaviour near the origin: the deviation from the constant 1 is linear in \\(x\\):
\\[
\lim_{x \to 0} \frac{e^x - 1}{x} = 1
\\]
This limit reflects the fact that the derivative of \\(e^x\\) at the origin equals one:
\\[
\left.\frac{d}{dx}e^x\right|\_{x=0} = 1
\\]
This result follows directly from the Taylor expansion of \\(e^x\\) near the origin:
\\[
e^x = 1 + x + \frac{x^2}{2!} + o(x^2)
\\]
from which dividing by \\(x\\) and taking the limit immediately yields 1, as all higher-order terms vanish. More generally, for any real constant \\(a\\) we have:
\\[
\lim_{x \to 0} \frac{e^{ax} - 1}{x} = a
\\]
which follows by substituting \\(u = ax\\) and reducing to the standard form.

> Here \\(n!\\) denotes the [factorial](../factorial/) of \\(n\\), defined as the product of all positive integers up to \\(n\\); in particular, \\(2! = 2\\).

- - -
## The logarithmic fundamental limit

For the natural [logarithm](../logarithmic-function/), the following limit holds:
\\[
\lim_{x \to 0} \frac{\ln(1+x)}{x} = 1
\\]
This result corresponds to the derivative of \\(\ln x\\) evaluated at \\(x = 1\\):
\\[
\left.\frac{d}{dx}\ln x\right|\_{x=1} = 1
\\]
More generally, for any real constant \\(a\\) we have:
\\[
\lim_{x \to 0} \frac{\ln(1+ax)}{x} = a
\\]

- - -
## Limits defining exponential functions

A standard limit that defines Euler's number is given by:
\\[
\lim_{x \to 0} (1 + x)^{\frac{1}{x}} = e
\\]
or equivalently, in its discrete form:
\\[
\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e
\\]

> The discrete form is obtained by restricting \\(x\\) to values of the form \\(\frac{1}{n}\\), where \\(n\\) is a positive integer, so that \\(x \to 0\\) corresponds to \\(n \to \infty\\). Substituting yields the sequence \\(\left(1 + \frac{1}{n}\right)^n\\), whose limit as \\(n \to \infty\\) coincides with that of the continuous form.

More generally, for any real constant \\(a\\) we have:
\\[
\lim_{x \to 0} (1 + ax)^{\frac{1}{x}} = e^{a}
\\]

- - -
## Limits involving power functions

For any real exponent \\(\alpha\\) we have:
\\[
\lim_{x \to 0} \frac{(1+x)^\alpha - 1}{x} = \alpha
\\]

This result may be derived using the binomial expansion when \\(\alpha\\) is rational, or by applying logarithmic differentiation in the general case.

- - -
## Asymptotic equivalence

The following notable limits illustrate local [asymptotic](../asymptotes/) relationships:
\\[
\sin x \sim x \qquad \tan x \sim x \qquad 1 - \cos x \sim \frac{x^2}{2}
\\]
\\[
e^x - 1 \sim x \qquad \ln(1+x) \sim x
\\]
More precisely, the notation \\(f(x) \sim g(x)\\) as \\(x \to 0\\) indicates that the two functions are asymptotically equivalent near the origin, meaning that:
\\[
\lim_{x \to 0} \frac{f(x)}{g(x)} = 1
\\]
Each of these relationships corresponds to the first nonzero term in the local Taylor expansion of a smooth function near a regular point. Consequently, these equivalences can be used to replace more complex expressions with simpler ones when evaluating limits.

- - -
## Structural interpretation

From an advanced perspective, remarkable limits serve as expressions of differentiability and local linearization. Every limit of the form:

\\[ \lim_{x \to 0} \frac{f(x) - f(0)}{x} \\] 

corresponds to the definition of the [derivative](../derivatives/) of \\(f\\) at the origin. Classical remarkable limits represent particular cases where this derivative can be calculated explicitly and then utilised as a foundational method for addressing more complex [indeterminate forms](../indeterminate-forms/).

- - -
## Summary of the main remarkable limits

|  |  |
|------------------|-------------------|
| \\[\lim_{x \to 0} \frac{\sin x}{x}\\] | \\[1\\] |
| \\[\lim_{x \to 0} \frac{\sin(ax)}{ax}\\] | \\[1\\] |
| \\[\lim_{x \to 0} \frac{\sin(ax)}{x}\\] | \\[a\\] |
| \\[\lim_{x \to 0} \frac{\tan x}{x}\\] | \\[1\\] |
| \\[\lim_{x \to 0} \frac{\tan(ax)}{x}\\] | \\[a\\] |
| \\[\lim_{x \to 0} \frac{1-\cos x}{x^2}\\] | \\[\frac{1}{2}\\] |
| \\[\lim_{x \to 0} \frac{1-\cos(ax)}{x^2}\\] | \\[\frac{a^2}{2}\\] |
| \\[\lim_{x \to 0} \frac{e^x - 1}{x}\\] | \\[1\\] |
| \\[\lim_{x \to 0} \frac{e^{ax} - 1}{x}\\] | \\[a\\] |
| \\[\lim_{x \to 0} \frac{\ln(1+x)}{x}\\] | \\[1\\] |
| \\[\lim_{x \to 0} \frac{\ln(1+ax)}{x}\\] | \\[a\\] |
| \\[\lim_{x \to 0}(1 + x)^{1/x}\\] | \\[e\\] |
| \\[\lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n\\] | \\[e\\] |
| \\[\lim_{x\to 0}(1+ax)^{1/x}\\] | \\[e^a\\] |
| \\[\lim_{x \to 0} \frac{(1+x)^\alpha - 1}{x}\\] | \\[\alpha\\] |