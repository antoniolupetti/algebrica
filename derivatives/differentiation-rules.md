---
title: Differentiation Rules
source: https://algebrica.org/differentiation-rules/
license: CC BY-NC 4.0
tags:
  - derivatives
  - differentiation-rules
  - linearity
  - product-rule
  - quotient-rule
  - sum-rule
---
## Introduction

Computing a [derivative](../derivatives/) directly from the limit of the [difference quotient](../difference-quotient/) is possible in principle, but it becomes impractical for all but the simplest functions. The differentiation rules describe how the derivative behaves under the basic operations on [functions](../functions/), that is, multiplication by a constant, addition, multiplication, and division. Together with the derivatives of the elementary functions, collected in the table of [fundamental derivatives](../derivatives/), these rules allow the derivative of most functions met in practice to be computed without returning to the definition.

Throughout this entry, $f$ and $g$ denote functions that are differentiable at the point $x$ under consideration. Every rule stated below holds at any point where this assumption is satisfied.

## Linearity of the derivative

The first two rules express the linearity of differentiation. The derivative of a constant multiple of a function is the constant times the derivative of the function:

$$D[c \cdot f(x)] = c \cdot f'(x)$$

The derivative of a sum of two functions is the sum of the two derivatives:

$$D[f(x) + g(x)] = f'(x) + g'(x)$$

The rule for the difference follows by combining these two statements with $c = -1$, which gives:

$$D[f(x) - g(x)] = f'(x) - g'(x)$$

Taken together, these properties mean that the derivative of a linear combination of differentiable functions is the same linear combination of their derivatives. This is what allows a polynomial to be differentiated term by term.

## Proof of linearity

The constant multiple rule follows from the definition of the derivative and from the fact that a constant factor can be taken outside a [limit](../limits/):

$$
\begin{align}
D[c \cdot f(x)] &= \lim_{h \to 0} \frac{c f(x+h) - c f(x)}{h} \\[6pt]
&= c \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} \\[6pt]
&= c \cdot f'(x)
\end{align}
$$

For the sum, we write the difference quotient of $f + g$ and separate it into two fractions, one for each function:

$$
\begin{align}
D[f(x) + g(x)] &= \lim_{h \to 0} \frac{[f(x+h) + g(x+h)] - [f(x) + g(x)]}{h} \\[6pt]
&= \lim_{h \to 0} \left( \frac{f(x+h) - f(x)}{h} + \frac{g(x+h) - g(x)}{h} \right) \\[6pt]
&= f'(x) + g'(x)
\end{align}
$$

The last equality uses the rule that the limit of a sum is the sum of the limits, which applies since both limits exist by hypothesis.

## The product rule

The derivative of a product is not the product of the derivatives. The correct expression is given by the product rule, also known as the Leibniz rule:

$$D[f(x) \cdot g(x)] = f'(x) \cdot g(x) + f(x) \cdot g'(x)$$

In words, the derivative of a product is obtained by differentiating one factor at a time and adding the two contributions. The structure of the formula extends to products of more than two factors, where each term differentiates a single factor and leaves the others unchanged.

## Proof of the product rule

We start from the difference quotient of the product $f \cdot g$:

$$D[f(x) \cdot g(x)] = \lim_{h \to 0} \frac{f(x+h) g(x+h) - f(x) g(x)}{h}$$

The numerator cannot be factored directly. We therefore add and subtract the term $f(x+h) g(x)$, an operation that does not change its value:

$$f(x+h) g(x+h) - f(x+h) g(x) + f(x+h) g(x) - f(x) g(x)$$

Grouping the four terms in pairs, the first pair has $f(x+h)$ as a common factor and the second pair has $g(x)$ as a common factor:

$$f(x+h) [g(x+h) - g(x)] + g(x) [f(x+h) - f(x)]$$

Dividing by $h$ and passing to the limit, the difference quotient splits into two parts:

$$
\begin{align}
D[f(x) \cdot g(x)] &= \lim_{h \to 0} \left( f(x+h) \frac{g(x+h) - g(x)}{h} + g(x) \frac{f(x+h) - f(x)}{h} \right) \\[6pt]
&= f(x) \cdot g'(x) + g(x) \cdot f'(x)
\end{align}
$$

The factor $f(x+h)$ tends to $f(x)$ as $h \to 0$, since a function differentiable at $x$ is [continuous](../continuous-functions/) at that point. The two remaining quotients tend to $g'(x)$ and $f'(x)$ respectively, which gives the stated formula.

## The quotient rule

The derivative of a quotient of two functions, valid wherever the denominator does not vanish, is given by the quotient rule:

$$D\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x) \cdot g(x) - f(x) \cdot g'(x)}{g^2(x)}$$

The order of the two terms in the numerator matters, since the subtraction is not symmetric. The denominator is the square of the original denominator, and the whole expression is defined only where $g(x) \neq 0$.

## Proof of the quotient rule

A direct way to obtain the quotient rule is to first establish the reciprocal rule, which gives the derivative of $1/g$, and then combine it with the product rule. Starting from the definition, the difference quotient of $1/g$ is:

$$D\left[\frac{1}{g(x)}\right] = \lim_{h \to 0} \frac{1}{h} \left( \frac{1}{g(x+h)} - \frac{1}{g(x)} \right)$$

Bringing the two fractions inside the parentheses to a common denominator, we obtain:

$$
\begin{align}
D\left[\frac{1}{g(x)}\right] &= \lim_{h \to 0} \frac{1}{h} \cdot \frac{g(x) - g(x+h)}{g(x+h) g(x)} \\[6pt]
&= \lim_{h \to 0} \left( -\frac{g(x+h) - g(x)}{h} \cdot \frac{1}{g(x+h) g(x)} \right) \\[6pt]
&= -\frac{g'(x)}{g^2(x)}
\end{align}
$$

In the last step the first factor tends to $g'(x)$ by definition, while $g(x+h)$ tends to $g(x)$ by continuity, so the second factor tends to $1/g^2(x)$. This establishes the reciprocal rule:

$$D\left[\frac{1}{g(x)}\right] = -\frac{g'(x)}{g^2(x)}$$

The quotient $f/g$ can now be written as the product of $f$ and $1/g$. Applying the product rule and then the reciprocal rule yields:

$$
\begin{align}
D\left[\frac{f(x)}{g(x)}\right] &= D\left[ f(x) \cdot \frac{1}{g(x)} \right] \\[6pt]
&= f'(x) \cdot \frac{1}{g(x)} + f(x) \cdot \left( -\frac{g'(x)}{g^2(x)} \right) \\[6pt]
&= \frac{f'(x)}{g(x)} - \frac{f(x) g'(x)}{g^2(x)} \\[6pt]
&= \frac{f'(x) \cdot g(x) - f(x) \cdot g'(x)}{g^2(x)}
\end{align}
$$

The reduction to a common denominator in the final line produces the standard form of the quotient rule.

## Example 1

Consider the function obtained as a product of a [power](../powers/) and a [logarithm](../logarithms/):

$$f(x) = x^3 \ln(x)$$

The two factors are $x^3$, with derivative $3x^2$, and $\ln(x)$, with derivative $1/x$, both taken from the table of [fundamental derivatives](../derivatives/). Applying the product rule, we differentiate one factor at a time:

$$
\begin{align}
f'(x) &= 3x^2 \cdot \ln(x) + x^3 \cdot \frac{1}{x} \\[6pt]
&= 3x^2 \ln(x) + x^2
\end{align}
$$

Collecting the common factor $x^2$, the derivative takes the compact form:

$$f'(x) = x^2 \left( 3\ln(x) + 1 \right)$$

## Example 2

Consider the quotient of the exponential function and a quadratic polynomial:

$$f(x) = \frac{e^x}{x^2 + 1}$$

The numerator has derivative $e^x$, and the denominator has derivative $2x$. Applying the quotient rule, we obtain:

$$
\begin{align}
f'(x) &= \frac{e^x (x^2 + 1) - e^x \cdot 2x}{(x^2 + 1)^2} \\[6pt]
&= \frac{e^x (x^2 - 2x + 1)}{(x^2 + 1)^2}
\end{align}
$$

The numerator contains the perfect square $x^2 - 2x + 1 = (x-1)^2$, so the derivative can be written as:

$$f'(x) = \frac{e^x (x - 1)^2}{(x^2 + 1)^2}$$

Since the numerator is never negative, this shows that $f$ is increasing on the whole real line, with a horizontal tangent at $x = 1$.

## Composite functions and the chain rule

The rules presented here account for products, quotients, and linear combinations, but they do not cover the composition of functions. When a function is built by substituting one expression into another, as in $y = f(g(x))$, its derivative is governed by a separate result, the [chain rule](../chain-rule/). In practice the differentiation rules and the chain rule are applied together, the former to handle the algebraic structure of an expression and the latter to handle the nesting of one function inside another.
