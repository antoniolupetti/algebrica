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

The definition of a [limit](../limits/) provides a framework for describing how a function $f(x)$ approaches a specific value near a given point $x_0$. By itself, this definition is not enough for practical calculations. In most cases, we deal with limits when [functions](../functions/) are added, multiplied, divided, composed, or raised to a power.

The algebra of limits collects the operational rules derived directly from the formal definition. These rules describe the structural compatibility between the limit operator and the standard algebraic operations. Throughout this page, $L$ and $M$ denote [real numbers](../real-numbers/) such that:

$$\lim_{x \to x_0} f(x) = L \qquad \lim_{x \to x_0} g(x) = M$$

## Limit of a sum

When two functions approach finite values near a point, the sum of the functions approaches the sum of those values. If $f(x)$ remains close to $L$ and $g(x)$ remains close to $M$, then their combined variation remains close to $L + M$. Formally:

$$\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M$$

This property follows directly from the definition of a limit. For any tolerance around $L + M$, the deviations of $f(x)$ and $g(x)$ can be controlled independently to ensure that their combined deviation remains within the prescribed bound. Consider, for instance, two expressions involving the [sine and cosine](../sine-and-cosine/) functions:

$$
\begin{align}
f(x) &= \frac{\sin x}{x} \\[6pt]
g(x) &= \frac{1 - \cos x}{x^2}
\end{align}
$$

and suppose we wish to compute the sum:

$$\lim_{x \to 0} \big( f(x) + g(x) \big)$$

Neither function is defined at $x = 0$, which prevents evaluating the limit by direct substitution. Two [remarkable limits](../remarkable-limits/), however, are available:

$$
\begin{align}
\lim_{x \to 0} \frac{\sin x}{x} &= 1 \\[6pt]
\lim_{x \to 0} \frac{1 - \cos x}{x^2} &= \frac{1}{2}
\end{align}
$$

By the sum rule, we conclude:

$$\lim_{x \to 0} \big( f(x) + g(x) \big) = 1 + \frac{1}{2} = \frac{3}{2}$$

> Rather than analysing the combined expression directly, which would require substantial algebraic manipulation, the sum rule decomposes the problem into two independent limits, each of which can be evaluated separately.

## Limit of a difference

A similar argument applies to subtraction. If two functions approach $L$ and $M$, then their difference approaches $L - M$. The algebraic structure of the real numbers ensures that subtraction is consistent with the limit operation:

$$\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M$$

The proof parallels that of the sum, since subtraction can be interpreted as addition of the additive inverse. As an example, consider the functions:

$$
\begin{align}
f(x) &= \frac{1 - \cos x}{x^2} \\[6pt]
g(x) &= \frac{\sin^2 x}{2x^2}
\end{align}
$$

and suppose we wish to compute the difference:

$$\lim_{x \to 0} \big( f(x) - g(x) \big)$$

Neither function is defined at $x = 0$, so direct substitution is not available. Two known results give:

$$
\begin{align}
\lim_{x \to 0} \frac{1 - \cos x}{x^2} &= \frac{1}{2} \\[6pt]
\lim_{x \to 0} \frac{\sin^2 x}{2x^2} &= \frac{1}{2}
\end{align}
$$

The second result follows from the [remarkable limit](../remarkable-limits/) $\lim_{x \to 0} \frac{\sin x}{x} = 1$. Using the difference rule:

$$\lim_{x \to 0} \big( f(x) - g(x) \big) = \frac{1}{2} - \frac{1}{2} = 0$$

At first sight, this result is not obvious from the combined expression:

$$\frac{1 - \cos x}{x^2} - \frac{\sin^2 x}{2 x^2}$$

because each term approaches $\frac{1}{2}$, and recovering their difference requires some careful algebraic work. The difference rule, like the sum rule, reduces the problem to two simpler limits.

## Limit of a constant multiple

If a function approaches a value $L$, multiplying it by a constant multiplies the limit by that same constant. This expresses the linearity of the limit operator: for any real constant $c$, we have:

$$\lim_{x \to x_0} c f(x) = c L$$

The constant does not interact with the limiting process, but only rescales the final value. To illustrate, consider:

$$\lim_{x \to 0} 3 \frac{\ln(1 + x)}{x}$$

The [logarithmic function](../logarithms/) is not defined at $x = 0$, so direct substitution is not available. From the table of [remarkable limits](../remarkable-limits/), we know:

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

Applying the constant multiple rule:

$$\lim_{x \to 0} 3 \cdot \frac{\ln(1 + x)}{x} = 3 \cdot 1 = 3$$

## Limit of a product

If two functions approach finite values near a point, their product approaches the product of those values. With $f(x)$ close to $L$ and $g(x)$ close to $M$, the product stays close to $L \cdot M$:

$$\lim_{x \to x_0} \big( f(x) \cdot g(x) \big) = L \cdot M$$

The key idea behind this rule is that both factors can be controlled independently near $x_0$, and their combined effect remains bounded. Consider the functions:

$$
\begin{align}
f(x) &= \frac{e^x - 1}{x} \\[6pt]
g(x) &= \frac{\ln(1 + x)}{x}
\end{align}
$$

Neither is defined at $x = 0$, so direct substitution is not available. Both are [remarkable limits](../remarkable-limits/) with known values:

$$
\begin{align}
\lim_{x \to 0} \frac{e^x - 1}{x} &= 1 \\[6pt]
\lim_{x \to 0} \frac{\ln(1 + x)}{x} &= 1
\end{align}
$$

By the product rule:

$$\lim_{x \to 0} \frac{(e^x - 1) \ln(1 + x)}{x^2} = 1 \cdot 1 = 1$$

## Limit of a quotient

When dividing two limits, an essential restriction applies to the denominator. If $g(x)$ approaches a nonzero value $M \neq 0$, the quotient behaves regularly near $x_0$. If the denominator tends to zero, the resulting expression may be an [indeterminate form](../indeterminate-forms/) of type $0/0$ or $\ell/0$, which requires separate analysis. Assuming $M \neq 0$:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}$$

The key observation is that, because $g(x)$ stays close to a nonzero number near $x_0$, it does not approach zero in any neighbourhood of $x_0$. This excludes division-by-zero issues, and the limit behaves as expected. Consider the functions:

$$
\begin{align}
f(x) &= \frac{e^x - 1}{x} \\[6pt]
g(x) &= \frac{x^2 + 1}{x + 1}
\end{align}
$$

Suppose we want to find the quotient:

$$\lim_{x \to 0} \frac{f(x)}{g(x)}$$

The function $f(x)$ is not defined at $x = 0$, so direct substitution is not available for the numerator. From the table of [remarkable limits](../remarkable-limits/), we know:

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

For the denominator, direct substitution can be used because $g(x)$ is defined and [continuous](../continuous-functions/) at $x = 0$:

$$\lim_{x \to 0} \frac{x^2 + 1}{x + 1} = \frac{0 + 1}{0 + 1} = 1$$

Since the denominator's limit is $M = 1 \neq 0$, the quotient rule applies and gives:

$$\lim_{x \to 0} \frac{f(x)}{g(x)} = \frac{1}{1} = 1$$

> This example shows the importance of verifying that the denominator's limit is nonzero before applying the quotient rule. Here $g(x)$ stays close to $1$ near $x = 0$, so there is no risk of dividing by zero.

## Limits of powers and polynomials

Repeated multiplication leads to limits of powers. If $f(x)$ approaches $L$, then for any positive integer $n$:

$$\lim_{x \to x_0} \big( f(x) \big)^n = L^n$$

A direct consequence is that the limit of a [polynomial](../polynomials/) can be obtained by substituting the limiting value. Since polynomials are built from sums and products, they inherit the corresponding rules for limits. Consider the function:

$$\lim_{x \to 0} \left( \frac{e^x - 1}{x} \right)^4$$

The function is not defined at $x = 0$, so direct substitution is not available. The base, however, is a [remarkable limit](../remarkable-limits/):

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

Applying the power rule with $n = 4$:

$$\lim_{x \to 0} \left( \frac{e^x - 1}{x} \right)^4 = 1^4 = 1$$

The power rule avoids the explicit expansion of the expression, which would make the calculation significantly more involved. Once the limit of the base is known, the result is obtained by raising it to the required power.

## Limit of a composition

We now consider the case of function composition. Given two functions $\varphi$ and $f$, the composition $\varphi(f(x))$ consists in applying $f$ first and then $\varphi$ to the result. Suppose that:

$$\lim_{x \to x_0} f(x) = L$$

If $\varphi$ is [continuous](../continuous-functions/) at $L$, the limit can be carried through the outer function:

$$\lim_{x \to x_0} \varphi \big( f(x) \big) = \varphi(L)$$

This property connects the algebra of limits with continuity. The continuity of $\varphi$ ensures that small variations of the input near $L$ produce small variations of the output. Without continuity, the rule cannot be guaranteed.

For instance, consider:

$$f(x) = \frac{\ln(1 + x)}{x} \qquad \varphi(t) = \sqrt{t}$$

Suppose we want to compute:

$$\lim_{x \to 0} \sqrt{\frac{\ln(1 + x)}{x}}$$

The function $f(x)$ is not defined at $x = 0$, so direct substitution is not available. From the table of [remarkable limits](../remarkable-limits/):

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

Since $\varphi(t) = \sqrt{t}$ is continuous at $t = 1$, the limit can be carried through the square root:

$$\lim_{x \to 0} \sqrt{\frac{\ln(1 + x)}{x}} = \sqrt{1} = 1$$

> The composition rule reduces the problem to two separate steps: first identifying the limit of the inner function, and then evaluating the outer function at that value. This procedure is justified only if $\varphi$ is continuous at $L = 1$.

## Summary

The following table summarizes the main algebraic properties of limits. These rules allow more complex limits to be evaluated by combining simpler ones, provided that the individual limits exist and the required conditions are satisfied. They form the foundation of most limit computations in elementary calculus.

[class="table-1"]

|                   |                                                                                |
| ----------------- | ------------------------------------------------------------------------------ |
| Sum               | $\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M$                             |
| Difference        | $\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M$                             |
| Constant multiple | $\lim_{x \to x_0} c f(x) = c L$                                                |
| Product           | $\lim_{x \to x_0} \big( f(x) \cdot g(x) \big) = L \cdot M$                     |
| Quotient          | $\lim_{x \to x_0} \dfrac{f(x)}{g(x)} = \dfrac{L}{M}, \quad M \neq 0$           |
| Power             | $\lim_{x \to x_0} \big( f(x) \big)^n = L^n$                                    |
| Composition       | $\lim_{x \to x_0} \varphi(f(x)) = \varphi(L), \quad \varphi$ continuous ad $L$ |
[/class]

When one or more of the underlying limits is infinite, or when the denominator of a quotient tends to zero, these rules do not apply directly. 

The resulting expressions become [indeterminate forms](../indeterminate-forms/) and require dedicated techniques such as factorisation, asymptotic comparison, [L'Hôpital's rule](../hopital-rule/), or [Taylor expansions](../taylor-series/) combined with [little-o notation](../little-o-notation/).
