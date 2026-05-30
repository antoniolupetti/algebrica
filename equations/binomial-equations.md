---
title: Binomial Equations
source: https://algebrica.org/binomial-equations/
license: CC BY-NC 4.0
tags:
  - binomial-equations
  - equations
  - radicals
---
## What are binomial equations

Binomial equations are a particular class of algebraic [equations](../equations/) that involve only two terms. Their general form is the following:

$$ax^n + b = 0$$

In this expression $a$ and $b$ are constants, while $x$ is the unknown raised to the power $n$, where $n$ is a positive [integer](../integers/).

The strategy used to solve a binomial equation depends on the value of $n$. When $n$ is odd, the equation has a unique real solution. When $n$ is even, the existence of real solutions depends on the sign of the radicand: the equation has no real solution when solving it requires an even root of a negative number. In more advanced settings the solutions may also be complex, a case treated in the study of the [roots of complex numbers](../complex-numbers-roots/).

## Equations of degree one or two

When $n = 1$, the equation reduces to a [linear equation](../linear-equations/) of the form $ax + b = 0$, solved by isolating the variable:

$$ax + b = 0 \quad \rightarrow \quad x = -\frac{b}{a}$$

When $n = 2$, the equation reduces to a [quadratic equation](../quadratic-equations/) of the form $ax^2 + b = 0$. This can be solved with the [quadratic formula](../quadratic-formula/) or, more directly, by extracting the square root of $-\frac{b}{a}$:

$$x = \pm\sqrt{-\frac{b}{a}}$$

> This expression yields real solutions only when $-\frac{b}{a} \geq 0$. Otherwise the equation has [complex solutions](../quadratic-equations-with-complex-solutions/).

## Equations with degree greater than two

When $n$ is greater than $2$, the equation can be solved by extracting the $n$-th root of $-\frac{b}{a}$, distinguishing two cases according to whether $n$ is even or odd.

When $n$ is even and $-\frac{b}{a}$ is positive, the equation has two distinct solutions, which reduce to a single solution when $-\frac{b}{a}$ equals $0$:

$$x = \pm\sqrt[n]{-\frac{b}{a}}$$

When $n$ is even and $-\frac{b}{a}$ is negative, the equation has no solution in the field of [real numbers](../types-of-numbers/).

- - -

When $n$ is odd, the equation always has a single real solution:

$$x = \sqrt[n]{-\frac{b}{a}}$$

The $n$-th [root](../radicals/) of a negative number exists in the reals only when the index is odd. The extraction follows the same method used for positive numbers, and the result of an odd root of a negative number is itself negative. When the index is even, no real result exists.

## Example 1

Consider the binomial equation $x^3 - 27 = 0$. Isolating the power and extracting the cube root gives:

$$
\begin{align}
x^3 &= 27 \\[6pt]
x &= \sqrt[3]{27} \\[6pt]
  &= 3
\end{align}
$$

Here $n$ is odd and the number under the root is positive, so the equation admits a single real solution:

$$x = 3$$

## Example 2

Consider the binomial equation $x^3 + 8 = 0$. Isolating the power and extracting the cube root gives:

$$
\begin{align}
x^3 &= -8 \\[6pt]
x &= \sqrt[3]{-8} \\[6pt]
  &= -2
\end{align}
$$

Here $n$ is odd and the number under the root is negative, so the equation admits a single real solution:

$$x = -2$$

## Example 3

Consider the binomial equation $x^4 - 16 = 0$. Isolating the power and extracting the fourth root gives:

$$
\begin{align}
x^4 &= 16 \\[6pt]
x &= \pm\sqrt[4]{16} \\[6pt]
  &= \pm 2
\end{align}
$$

Here $n$ is even and the number under the root is positive, so the equation admits two distinct real solutions, symmetric with respect to the origin:

$$x = -2 \quad x = 2$$

## Example 4

Consider the binomial equation $x^4 + 5 = 0$. Isolating the power gives:

$$
\begin{align}
x^4 &= -5 \\[6pt]
x &= \sqrt[4]{-5}
\end{align}
$$

Here $n$ is even and the number under the root is negative, so the equation admits no real solution. The set of real solutions is therefore empty:

$$S = \varnothing$$

These examples illustrate the most direct cases. In practice, more complex [polynomial equations](../polynomial-equations/) can sometimes be reduced to binomial equations, which are then resolved by the straightforward methods shown here.
