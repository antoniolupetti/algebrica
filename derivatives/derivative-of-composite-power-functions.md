---
title: Derivative of Composite Power Functions
source: https://algebrica.org/derivative-of-composite-power-functions/
license: CC BY-NC 4.0
tags:
  - composite-functions
  - derivatives
  - logarithmic-differentiation
  - power-functions
---
## Composite power functions

We have previously introduced how to calculate the [derivative](../derivatives/) of a function at a point using the definition of the [difference quotient](../difference-quotient/), and how to differentiate composite functions through the [chain rule](../chain-rule/). A separate technique is required for power functions in which both the base and the exponent depend on the variable, that is, functions of the form:

$$y = f(x)^{g(x)}$$

The expression is defined for $f(x) > 0$. Since the variable appears both in the base and in the exponent, neither the power rule nor the rule for exponential functions applies directly. The standard technique, known as logarithmic differentiation, combines the properties of [logarithms](../logarithms/) with the chain rule. The general formula for the derivative of $f(x)^{g(x)}$, with $f$ and $g$ differentiable, is the following:

$$D\left[f(x)^{g(x)}\right] = f(x)^{g(x)} \left[ g'(x) \ln f(x) + g(x) \frac{f'(x)}{f(x)} \right]$$

In this formula:

+ $f(x)^{g(x)}$ is the original function
+ $f'(x)$ is the derivative of $f(x)$
+ $\ln f(x)$ is the natural logarithm of $f(x)$
+ $g'(x)$ is the derivative of $g(x)$

> The formula can also be obtained by rewriting the function in exponential form as $f(x)^{g(x)} = e^{g(x)\ln f(x)}$ and applying the chain rule together with the product rule to the exponent.

## Example 1

The function $y = x^{2x}$ is defined for $x > 0$, and its derivative is calculated as follows.

First, we rewrite the function by applying the natural logarithm to both sides:

$$\ln y = \ln(x^{2x})$$

By the property of logarithms $\log_a(b^c) = c \cdot \log_a(b)$, the equality can be rewritten as:

$$\ln y = 2x\ln(x)$$

Since $\ln y$ is a composite function of $x$, differentiating the left-hand side with respect to $x$ yields, by the chain rule:

$$D[\ln y] = \frac{1}{y} \cdot y'$$

The right-hand side $2x\ln(x)$ is a product, so we apply the product rule:

$$D[2x\ln(x)] = 2\ln(x) + 2x \cdot \frac{1}{x} = 2\ln(x) + 2$$

Equating the two derivatives, we obtain:

$$\frac{1}{y} \cdot y' = 2\ln(x) + 2$$

Multiplying both sides by $y$, and recalling that $y = x^{2x}$, we have:

$$y' = x^{2x}(2\ln(x) + 2)$$

We conclude that the derivative of $y = x^{2x}$ is $x^{2x}(2\ln(x) + 2)$.

## Example 2

The function $y = x^{\ln(x)}$ is defined for $x > 0$, and its derivative is computed as follows.

Applying the natural logarithm to both sides and using the property of logarithms, we obtain:

$$\ln y = \ln(x)\ln(x) = \ln^2(x)$$

Differentiating the left-hand side gives $\frac{1}{y}y'$ as before. For the right-hand side, $\ln^2(x)$ is a composite function, with outer function $t^2$ and inner function $\ln(x)$, so by the chain rule:

$$D[\ln^2(x)] = 2\ln(x) \cdot \frac{1}{x}$$

Equating the two derivatives and multiplying both sides by $y = x^{\ln(x)}$, we obtain:

$$y' = x^{\ln(x)} \cdot \frac{2\ln(x)}{x}$$

We conclude that the derivative of $y = x^{\ln(x)}$ is $\dfrac{2\ln(x)}{x}x^{\ln(x)}$.

## Example 3

A further case involves a function whose exponent is trigonometric:

$$y = x^{2\cos(x)}$$

The function is defined for $x > 0$. Applying the natural logarithm to both sides, we have:

$$\ln y = 2\cos(x)\ln(x)$$

The left-hand side differentiates to $\frac{1}{y}y'$. The right-hand side is a product of $2\cos(x)$ and $\ln(x)$, so the product rule gives:

$$D[2\cos(x)\ln(x)] = -2\sin(x)\ln(x) + \frac{2\cos(x)}{x}$$

Equating the two derivatives and multiplying both sides by $y = x^{2\cos(x)}$, we obtain:

$$y' = x^{2\cos(x)} \left( \frac{2\cos(x)}{x} - 2\sin(x)\ln(x) \right)$$

We conclude that the derivative of $y = x^{2\cos(x)}$ is $x^{2\cos(x)} \left( \frac{2\cos(x)}{x} - 2\sin(x)\ln(x) \right)$.

> In each example, the same result can be verified by writing the function as $e^{g(x)\ln f(x)}$ and differentiating the exponential form, or by substituting directly into the general formula stated at the beginning of the entry.
