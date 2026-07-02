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

Fix the point $x$ and write $z = g(x)$. Differentiating the composition directly from the [limit](../limits/) is delicate, because the natural manipulation of the difference quotient divides by $g(x+h) - g(x)$, a quantity that can vanish for values of $h$ arbitrarily close to $0$. To sidestep this, we record the derivative of $f$ at $z$ in an auxiliary function that involves no division. Define $\varphi$ on the domain of $f$ by:

$$
\varphi(w) =
\begin{cases}
\dfrac{f(w) - f(z)}{w - z} & w \neq z \\[8pt]
f'(z) & w = z
\end{cases}
$$

Since $f$ is differentiable at $z$, the difference quotient tends to $f'(z)$ as $w \to z$, which is the value assigned to $\varphi$ at $z$. The auxiliary function is therefore [continuous](../continuous-functions/) at $z$:

$$\lim_{w \to z} \varphi(w) = f'(z) = \varphi(z)$$

Directly from its definition, $\varphi$ satisfies the identity:

$$f(w) - f(z) = \varphi(w)(w - z)$$

For $w \neq z$ this is the definition of $\varphi$ multiplied by $w - z$, and for $w = z$ both sides vanish, so the identity holds for every $w$ without exception.

Evaluating the identity at $w = g(x+h)$, for which $w - z = g(x+h) - g(x)$, and dividing by $h \neq 0$, the difference quotient of the composite function splits into a product:

$$\frac{f(g(x+h)) - f(g(x))}{h} = \varphi(g(x+h)) \cdot \frac{g(x+h) - g(x)}{h}$$

Now let $h \to 0$. The inner function $g$ is differentiable at $x$, hence continuous there, so $g(x+h) \to g(x) = z$. Since $\varphi$ is continuous at $z$, the composition gives $\varphi(g(x+h)) \to \varphi(z) = f'(z)$. The second factor is the difference quotient of $g$ at $x$, which tends to $g'(x)$. Therefore:

$$
\begin{align}
D[f(g(x))] &= \lim_{h \to 0} \left( \varphi(g(x+h)) \cdot \frac{g(x+h) - g(x)}{h} \right) \\[6pt]
&= f'(z) \cdot g'(x) \\[6pt]
&= f'(g(x)) \cdot g'(x)
\end{align}
$$

> The identity $f(w) - f(z) = \varphi(w)(w - z)$ is the step the naive computation cannot supply. It multiplies by $w - z$ instead of dividing, so it stays valid at the values of $h$ where $g(x+h) = g(x)$, which is exactly where dividing by $g(x+h) - g(x)$ would break down.

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

In most computations the chain rule operates together with the product or quotient rule rather than alone. The basic [differentiation rules](../differentiation-rules/) handle the algebraic structure of an expression, while the chain rule handles the nesting of one function inside another. Consider the function:

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

Each factor is the derivative of a function in the composition, evaluated at the composition of all subsequent functions. This pattern generalises to any finite number of nested functions. For $y = f_1(f_2(\cdots f_n(x)\cdots))$, the derivative is given by the product:

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
