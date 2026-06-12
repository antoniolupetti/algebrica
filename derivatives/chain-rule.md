---
title: The Chain Rule
source: https://algebrica.org/chain-rule/
license: CC BY-NC 4.0
tags:
  - chain-rule
  - composite-functions
  - derivatives
  - differentiation-rules
---
## Introduction

Let $g$ be differentiable at $x$, and let $f$ be differentiable at $z = g(x)$. Then the composite function $y = f(g(x))$ is differentiable at $x$, and its [derivative](../derivatives/) is the product of the derivative of $f$ evaluated at $g(x)$ and the derivative of $g$ at $x$:

$$D[f(g(x))] = f'(g(x)) \cdot g'(x)$$

This result is known as the chain rule. It states that to differentiate a composite function, one multiplies the derivative of the outer function, evaluated at the inner function, by the derivative of the inner function.

In Leibniz notation, if $y = f(u)$ and $u = g(x)$, the chain rule takes the form:

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

## Proof

To prove that $D[f(g(x))] = f'(g(x)) \cdot g'(x)$ we calculate the following [limit](../limits/):

$$D[f(g(x))] = \lim_{h \to 0} \frac{f(g(x + h))-f(g(x))}{h}$$

Let $z = g(x)$, and set $\Delta z = g(x+h)-g(x)$. This implies that $g(x+h) = g(x) + \Delta z$. The limit becomes:

$$D[f(g(x))] = \lim_{h \to 0} \frac{f(z+\Delta z)-f(z)}{h}$$

Multiplying both the numerator and the denominator by $\Delta z$, we get:

$$
\begin{align}
D[f(g(x))] &= \lim_{h \to 0} \frac{f(z + \Delta z)-f(z)}{\Delta z} \cdot \frac{\Delta z}{h} \\[6pt]
&= \lim_{h \to 0} \frac{f(z + \Delta z)-f(z)}{\Delta z} \cdot \frac{g(x + h)-g(x)}{h} \\[6pt]
&= f'(z) \cdot g'(x) \\[6pt]
&= f'(g(x)) \cdot g'(x)
\end{align}
$$

Since $g$ is differentiable at $x$, it is also continuous there, so $\Delta z \to 0$ as $h \to 0$, and the first factor tends to $f'(z)$.

> This argument assumes $\Delta z \neq 0$ for $h$ sufficiently small. A complete proof handles the case $\Delta z = 0$ separately via an auxiliary function, and the conclusion is the same.

## A first example

Let us compute the derivative of the following composite function:

$$y = f(g(x)) = \sin(3x^2 + 2x)$$

In this case, we have:

+ The inner function $g(x) = 3x^2 + 2x$
+ The outer function $f(t) = \sin(t)$, where $t = g(x) = 3x^2 + 2x$

The derivative of the outer function $f(t) = \sin(t)$ is:

$$f'(t) = \cos(t)$$

Substituting $t = g(x)$, we obtain:

$$f'(g(x)) = \cos(3x^2 + 2x)$$

The derivative of the inner function $g(x) = 3x^2 + 2x$ is:

$$g'(x) = 6x + 2$$

Applying the chain rule, we multiply the two derivatives:

$$D[f(g(x))] = f'(g(x)) \cdot g'(x) = (6x + 2)\cos(3x^2 + 2x)$$

We conclude that the derivative of $y = \sin(3x^2 + 2x)$ is $(6x + 2)\cos(3x^2 + 2x)$.

## The chain rule in Leibniz notation

In Leibniz notation the computation proceeds by an explicit change of variable. Consider the function:

$$y = \ln(x^2 + 1)$$

Setting $u = x^2 + 1$, the function decomposes as $y = \ln(u)$ with $u = x^2 + 1$. The two derivatives are:

$$\frac{dy}{du} = \frac{1}{u}, \qquad \frac{du}{dx} = 2x$$

By the chain rule, the derivative of $y$ with respect to $x$ is the product of the two:

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = \frac{1}{u} \cdot 2x$$

Since the result must be expressed in terms of the original variable, we substitute $u = x^2 + 1$ back into the expression:

$$\frac{dy}{dx} = \frac{2x}{x^2 + 1}$$

> The substitution of $u = g(x)$ at the end of the computation corresponds, in the prime notation, to evaluating $f'$ at $g(x)$ rather than at $x$. Omitting this step is among the most frequent errors in applying the rule.

## Special cases

When the outer function is a power, an exponential, or a logarithm, the chain rule produces formulas that recur constantly in computations. For a differentiable function $f$:

$$
\begin{align}
D[f(x)^a] &= a[f(x)]^{a-1}f'(x) \\[14pt]
D\left[e^{f(x)}\right] &= e^{f(x)}f'(x) \\[6pt]
D[\ln f(x)] &= \frac{f'(x)}{f(x)}
\end{align}
$$

The first formula holds for any real exponent $a$, and the third requires $f(x) > 0$. Each follows from the chain rule with outer function $t^a$, $e^t$ and $\ln(t)$ respectively.

For example, in order to differentiate $y = (x^3 + 2)^{50}$, there is no need to expand the power. Applying the first formula with $f(x) = x^3 + 2$ and $a = 50$, we obtain:

$$D[(x^3 + 2)^{50}] = 50(x^3 + 2)^{49} \cdot 3x^2 = 150x^2(x^3 + 2)^{49}$$

The power formula also covers roots, since $\sqrt{f(x)} = f(x)^{1/2}$. To differentiate $y = \sqrt{x^2 + 1}$, we apply the formula with $f(x) = x^2 + 1$ and $a = \frac{1}{2}$:

$$D\left[\sqrt{x^2 + 1}\right] = \frac{1}{2}(x^2 + 1)^{-1/2} \cdot 2x = \frac{x}{\sqrt{x^2 + 1}}$$

We conclude that the derivative of $y = \sqrt{x^2 + 1}$ is $\dfrac{x}{\sqrt{x^2 + 1}}$.

> The power formula applies only when the exponent is constant. A related technique handles [composite power functions](../derivative-of-composite-power-functions/), that is, functions of the type $f(x)^{g(x)}$, where both the base and the exponent depend on $x$.

## Combining with the product rule

In most computations the chain rule operates together with the product or quotient rule rather than alone. Consider the function:

$$y = x^2 e^{\sin(x)}$$

The function is a product of $x^2$ and $e^{\sin(x)}$, so the differentiation begins with the product rule:

$$D\left[x^2 e^{\sin(x)}\right] = 2xe^{\sin(x)} + x^2 D\left[e^{\sin(x)}\right]$$

The remaining factor $e^{\sin(x)}$ is a composite function with outer function $e^t$ and inner function $\sin(x)$, so the chain rule gives:

$$D\left[e^{\sin(x)}\right] = e^{\sin(x)}\cos(x)$$

Substituting this result into the previous expression and collecting the common factor $xe^{\sin(x)}$, we obtain:

$$D\left[x^2 e^{\sin(x)}\right] = 2xe^{\sin(x)} + x^2 e^{\sin(x)}\cos(x) = xe^{\sin(x)}(2 + x\cos(x))$$

We conclude that the derivative of $y = x^2 e^{\sin(x)}$ is $xe^{\sin(x)}(2 + x\cos(x))$.

## Extension to multiple compositions

The chain rule can be extended to compositions involving three or more functions. For example, given $y = f(g(h(x)))$, the derivative is:

$$D[f(g(h(x)))] = f'(g(h(x))) \cdot g'(h(x)) \cdot h'(x)$$

Each factor represents the derivative of a function in the composition, evaluated at the composition of all subsequent functions. This pattern generalises to any finite number of nested functions. For $y = f_1(f_2(\cdots f_n(x)\cdots))$, the derivative is given by the product:

$$f_1'(f_2(\cdots f_n(x)\cdots)) \cdot f_2'(f_3(\cdots f_n(x)\cdots)) \cdots f_{n-1}'(f_n(x)) \cdot f_n'(x)$$

In practical applications, differentiation proceeds from the outermost function inward, with each derivative computed in sequence and the results multiplied together.

- - -

As an example, consider $y = \sin(e^{3x})$. The composition involves three functions:

$$
\begin{align}
h(x) &= 3x \\[6pt]
g(t) &= e^t \\[6pt]
f(s) &= \sin(s)
\end{align}
$$

Applying the chain rule from the outside inward we obtain:

$$
\begin{align}
D[\sin(e^{3x})] &= \cos(e^{3x}) \cdot e^{3x} \cdot 3 \\[6pt]
&= 3e^{3x}\cos(e^{3x})
\end{align}
$$

We conclude that the derivative of $y = \sin(e^{3x})$ is $3e^{3x}\cos(e^{3x})$.
