---
title: Algebra of Limits
source: https://algebrica.org/algebra-of-limits/
license: CC BY-NC 4.0
tags:
  - algebra-of-limits
  - continuous-functions
  - indeterminate-forms
  - limits
  - remarkable-limits
---
## Introduction

The definition of a [limit](../limits/) describes how a function $f(x)$ approaches a value near a point $x_0$, but on its own it is not a practical computational tool. In most problems we meet limits of [functions](../functions/) that are added, multiplied, divided, composed, or raised to a power. The algebra of limits collects the rules that let a limit pass through each of these operations, every one of them derived from the definition. Throughout this page $L$ and $M$ denote [real numbers](../real-numbers/) with:

$$\lim_{x \to x_0} f(x) = L \qquad \lim_{x \to x_0} g(x) = M$$

## Limit of a sum

When two functions approach finite values near a point, their sum approaches the sum of those values. If $f(x)$ stays close to $L$ and $g(x)$ stays close to $M$, their sum stays close to $L + M$:

$$\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M$$

The proof comes from the definition: given any tolerance around $L + M$, the deviations of $f(x)$ and $g(x)$ can be kept small enough, and separately, that their sum lands within the bound. The rule turns an awkward sum into two limits that are already known. Take

$$
\begin{align}
f(x) &= \frac{\sin x}{x} \\[6pt]
g(x) &= \frac{1 - \cos x}{x^2}
\end{align}
$$

neither of which is defined at the origin, together with the sum

$$\lim_{x \to 0} \big( f(x) + g(x) \big)$$

which substitution cannot reach. Each term is a standard [remarkable limit](../remarkable-limits/):

$$
\begin{align}
\lim_{x \to 0} \frac{\sin x}{x} &= 1 \\[6pt]
\lim_{x \to 0} \frac{1 - \cos x}{x^2} &= \frac{1}{2}
\end{align}
$$

The sum rule then gives:

$$\lim_{x \to 0} \big( f(x) + g(x) \big) = 1 + \frac{1}{2} = \frac{3}{2}$$

## Limit of a difference

The same argument applies to subtraction: if the two functions approach $L$ and $M$, their difference approaches $L - M$:

$$\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M$$

The proof repeats that of the sum, since $f - g$ is the sum of $f$ and $-g$. A more delicate case uses two quotients that both tend to $\frac{1}{2},$ so their difference is not settled by the two values on their own:

$$
\begin{align}
f(x) &= \frac{1 - \cos x}{x^2} \\[6pt]
g(x) &= \frac{\sin^2 x}{2x^2}
\end{align}
$$

Term by term the difference

$$\lim_{x \to 0} \big( f(x) - g(x) \big)$$

is undefined at $x = 0$, but both limits are known:

$$
\begin{align}
\lim_{x \to 0} \frac{1 - \cos x}{x^2} &= \frac{1}{2} \\[6pt]
\lim_{x \to 0} \frac{\sin^2 x}{2x^2} &= \frac{1}{2}
\end{align}
$$

The second follows from the [remarkable limit](../remarkable-limits/) $\lim_{x \to 0}\frac{\sin x}{x}=1.$ The difference rule gives:

$$\lim_{x \to 0} \big( f(x) - g(x) \big) = \frac{1}{2} - \frac{1}{2} = 0$$

Written as a single fraction

$$\frac{1 - \cos x}{x^2} - \frac{\sin^2 x}{2 x^2}$$

the value $0$ is far from obvious, since both terms tend to $\frac{1}{2}$ and only their cancellation produces it. Splitting the difference into two known limits sidesteps that cancellation.

## Limit of a constant multiple

If a function approaches $L$, scaling it by a constant scales the limit by the same constant. This is the linearity of the limit in its simplest form: for any real constant $c$,

$$\lim_{x \to x_0} c f(x) = c L$$

The constant plays no part in the limiting process and only rescales the final value. A direct case is

$$\lim_{x \to 0} 3 \frac{\ln(1 + x)}{x}$$

The [logarithmic](../logarithms/) quotient is undefined at $x = 0$, but the [remarkable limit](../remarkable-limits/)

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

supplies the limit of the unscaled quotient. Multiplying by the constant,

$$\lim_{x \to 0} 3 \cdot \frac{\ln(1 + x)}{x} = 3 \cdot 1 = 3$$

## Limit of a product

If two functions approach finite values near a point, their product approaches the product of those values. With $f(x)$ close to $L$ and $g(x)$ close to $M$, the product stays close to $L \cdot M$:

$$\lim_{x \to x_0} \big( f(x) \cdot g(x) \big) = L \cdot M$$

Both factors stay bounded and can be controlled independently near $x_0$, so their product stays close to $L \cdot M$. Set

$$
\begin{align}
f(x) &= \frac{e^x - 1}{x} \\[6pt]
g(x) &= \frac{\ln(1 + x)}{x}
\end{align}
$$

Both are undefined at the origin, and both are [remarkable limits](../remarkable-limits/):

$$
\begin{align}
\lim_{x \to 0} \frac{e^x - 1}{x} &= 1 \\[6pt]
\lim_{x \to 0} \frac{\ln(1 + x)}{x} &= 1
\end{align}
$$

By the product rule:

$$\lim_{x \to 0} \frac{(e^x - 1) \ln(1 + x)}{x^2} = 1 \cdot 1 = 1$$

## Limit of a quotient

When dividing two limits, a restriction on the denominator is unavoidable. If $g(x)$ approaches a nonzero value $M \neq 0$, the quotient behaves regularly near $x_0$. If the denominator tends to zero, the expression may be an [indeterminate form](../indeterminate-forms/) of type $0/0$ or $\ell/0$ and needs separate analysis. Assuming $M \neq 0$:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$$

Because $g(x)$ stays close to the nonzero number $M$, it is bounded away from zero on some neighbourhood of $x_0$, which excludes division by zero and lets the quotient behave as expected. Take

$$
\begin{align}
f(x) &= \frac{e^x - 1}{x} \\[6pt]
g(x) &= \frac{x^2 + 1}{x + 1}
\end{align}
$$

and their quotient as $x \to 0$:

$$\lim_{x \to 0} \frac{f(x)}{g(x)}$$

The numerator is undefined at $x = 0$ and comes from the [remarkable limit](../remarkable-limits/):

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

The denominator, [continuous](../continuous-functions/) at $x = 0$, is handled by substitution:

$$\lim_{x \to 0} \frac{x^2 + 1}{x + 1} = \frac{0 + 1}{0 + 1} = 1$$

Since the denominator's limit is $M = 1 \neq 0$, the quotient rule applies and gives:

$$\lim_{x \to 0} \frac{f(x)}{g(x)} = \frac{1}{1} = 1$$

## Limits of powers and polynomials

Taking $f = g$ in the product rule and iterating gives the limit of a power. If $f(x)$ approaches $L$, then for any positive integer $n$:

$$\lim_{x \to x_0} \big( f(x) \big)^n = L^n$$

A [polynomial](../polynomials/), built from sums and products, inherits these rules, so its limit is found by substituting the limiting value. For a power of a familiar quotient,

$$\lim_{x \to 0} \left( \frac{e^x - 1}{x} \right)^4$$

the base is undefined at the origin but is again a [remarkable limit](../remarkable-limits/):

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

The power rule with $n = 4$ then gives:

$$\lim_{x \to 0} \left( \frac{e^x - 1}{x} \right)^4 = 1^4 = 1$$

without expanding the fourth power, which would multiply the work for no gain.

## Limit of a composition

The last rule concerns composition. For two functions $\varphi$ and $f$, the composition $\varphi(f(x))$ applies $f$ first and then $\varphi$ to the result. Suppose that:

$$\lim_{x \to x_0} f(x) = L$$

If $\varphi$ is [continuous](../continuous-functions/) at $L$, the limit passes through the outer function:

$$\lim_{x \to x_0} \varphi \big( f(x) \big) = \varphi(L)$$

Continuity of $\varphi$ is what makes this work, since it forces small variations of the input near $L$ to produce small variations of the output. Without it the rule fails.

The square root of a remarkable limit is a simple instance. Set

$$f(x) = \frac{\ln(1 + x)}{x} \qquad \varphi(t) = \sqrt{t}$$

and compute:

$$\lim_{x \to 0} \sqrt{\frac{\ln(1 + x)}{x}}$$

The inner function is undefined at $x = 0$, with the [remarkable limit](../remarkable-limits/):

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

Since $\varphi(t) = \sqrt{t}$ is continuous at $t = 1$, the limit passes through the square root:

$$\lim_{x \to 0} \sqrt{\frac{\ln(1 + x)}{x}} = \sqrt{1} = 1$$

## Summary

The table below records the rules established above. Each holds when the individual limits $L$ and $M$ exist and the stated side conditions are met, in particular $M \neq 0$ for the quotient and continuity of $\varphi$ at $L$ for the composition.

[class="table-1"]

|                   |                                                                                |
| ----------------- | ------------------------------------------------------------------------------ |
| Sum               | $\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M$                             |
| Difference        | $\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M$                             |
| Constant multiple | $\lim_{x \to x_0} c f(x) = c L$                                                |
| Product           | $\lim_{x \to x_0} \big( f(x) \cdot g(x) \big) = L \cdot M$                     |
| Quotient          | $\lim_{x \to x_0} \dfrac{f(x)}{g(x)} = \dfrac{L}{M}, \quad M \neq 0$           |
| Power             | $\lim_{x \to x_0} \big( f(x) \big)^n = L^n$                                    |
| Composition       | $\lim_{x \to x_0} \varphi(f(x)) = \varphi(L), \quad \varphi$ continuous at $L$ |
[/class]

When one or more of the underlying limits is infinite, or when the denominator of a quotient tends to zero, these rules do not apply directly.

The resulting expressions become [indeterminate forms](../indeterminate-forms/) and require dedicated techniques such as factorisation, asymptotic comparison, [L'Hôpital's rule](../hopital-rule/), or [Taylor expansions](../taylor-series/) combined with [little-o notation](../little-o-notation/).
