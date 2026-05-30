---
title: Trinomial Equations
source: https://algebrica.org/trinomial-equations/
license: CC BY-NC 4.0
tags:
  - equations
  - quadratic-formula
  - trinomial-equations
---

## Definition

Trinomial equations are a particular class of [polynomial equations](../polynomial-equations/) consisting of three terms that involve constants and [powers](../powers/) of a variable. Their general form is the following:

$$ax^{2n} + bx^{n} + c = 0$$

This form is convenient because it admits a substitution strategy: setting $x^n = y$ transforms the equation into a standard quadratic.

In this expression $a$, $b$, and $c$ are numerical coefficients, while $x$ is the unknown. When $n = 1$, the equation becomes an ordinary [quadratic equation](../quadratic-equations/):

$$ax^2 + bx + c = 0$$

When $n = 2$, the equation takes the form $ax^4 + bx^2 + c = 0$ and is called a biquadratic equation. This is the most frequently encountered trinomial equation, and the substitution $x^2 = y$ reduces it to a quadratic in $y$.

## How to solve trinomial equations

A trinomial equation of the form $ax^{2n} + bx^n + c = 0$ is solved through a substitution that reduces it to a quadratic. Setting:

$$x^n = y$$

the equation becomes:

$$ay^2 + by + c = 0$$

This quadratic in $y$ can be solved by [factoring](../factoring-quadratic-equations/), [completing the square](../completing-the-square/), or the [quadratic formula](../quadratic-formula/). Once the values of $y$ are found, they are substituted back through $y = x^n$ to recover the corresponding values of $x$. The procedure can be summarised as follows:

+ Set $y = x^n$, so the equation becomes $ay^2 + by + c = 0$.
+ Solve the quadratic equation in $y$.
+ For each solution $y_i$, solve $x^n = y_i$ to find the corresponding values of $x$.
+ Check every solution in the original equation.

The substitution can introduce extraneous solutions, that is values which satisfy the transformed equation but not the original one. Substituting each candidate back into the original equation confirms that it is valid and respects any implicit conditions.

## Number of real solutions

The quadratic in $y$ produces at most two values $y_1$ and $y_2$, but the number of real values of $x$ recovered from each $y_i$ depends on the parity of $n$ and on the sign of $y_i$. The final step $x^n = y_i$ behaves like a [binomial equation](../binomial-equations/), and its real solutions follow the same rules.

When $n$ is even, the equation $x^n = y_i$ contributes:

+ two real solutions $x = \pm\sqrt[n]{y_i}$ when $y_i > 0$
+ one real solution $x = 0$ when $y_i = 0$
+ no real solution when $y_i < 0$

When $n$ is odd, the equation $x^n = y_i$ always contributes exactly one real solution $x = \sqrt[n]{y_i}$, since an odd root is defined for every real number, whether positive or negative.

> A biquadratic equation can therefore have four, three, two, one, or no real solutions, according to the number and the sign of the roots $y_i$ of the associated quadratic.

## Example 1

Consider the biquadratic equation $3x^4 - 7x^2 + 2 = 0$. Substituting $y = x^2$ transforms it into a quadratic equation:

$$3y^2 - 7y + 2 = 0$$

Applying the [quadratic formula](../quadratic-formula/) gives the values of $y$:

$$
\begin{align}
y &= \frac{-(-7) \pm \sqrt{(-7)^2 - 4 \cdot 3 \cdot 2}}{2 \cdot 3} \\[6pt]
  &= \frac{7 \pm \sqrt{49 - 24}}{6} \\[6pt]
  &= \frac{7 \pm \sqrt{25}}{6} \\[6pt]
  &= \frac{7 \pm 5}{6}
\end{align}
$$

The two values are:

$$y_1 = \frac{12}{6} = 2, \qquad y_2 = \frac{2}{6} = \frac{1}{3}$$

- - -

Each value of $y$ is substituted back through $x^2 = y$ to find the corresponding values of $x$. For $y = 2$:

$$x^2 = 2 \quad \rightarrow \quad x = \pm\sqrt{2}$$

For $y = \frac{1}{3}$:

$$x^2 = \frac{1}{3} \quad \rightarrow \quad x = \pm\sqrt{\frac{1}{3}}$$

- - -

The candidate solutions are verified by substituting them into the original equation $3x^4 - 7x^2 + 2 = 0$. For $x = \pm\sqrt{2}$:

$$3(\sqrt{2})^4 - 7(\sqrt{2})^2 + 2 = 3 \cdot 4 - 7 \cdot 2 + 2 = 12 - 14 + 2 = 0$$

For $x = \pm\sqrt{\frac{1}{3}}$:

$$3\left(\sqrt{\frac{1}{3}}\right)^4 - 7\left(\sqrt{\frac{1}{3}}\right)^2 + 2 = 3 \cdot \frac{1}{9} - 7 \cdot \frac{1}{3} + 2 = \frac{1}{3} - \frac{7}{3} + 2 = 0$$

All four values satisfy the original equation. The solution is therefore:

$$x = \pm\sqrt{2} \quad \text{and} \quad x = \pm\sqrt{\frac{1}{3}}$$

## Example 2

Consider the biquadratic equation $x^4 - 3x^2 - 4 = 0$. Substituting $y = x^2$ transforms it into a quadratic equation, which factors as:

$$y^2 - 3y - 4 = 0 \quad \rightarrow \quad (y - 4)(y + 1) = 0$$

The two values are:

$$y_1 = 4, \qquad y_2 = -1$$

- - -

Each value of $y$ is substituted back through $x^2 = y$. Since the index of the root is even, only a non-negative value of $y$ can produce real solutions. For $y = 4$:

$$x^2 = 4 \quad \rightarrow \quad x = \pm 2$$

The value $y = -1$ is discarded, because the equation $x^2 = -1$ has no solution in the [real numbers](../types-of-numbers/). The original equation therefore has two real solutions:

$$x = -2 \quad x = 2$$

## Example 3

Consider the equation $x^6 + 7x^3 - 8 = 0$, where the exponent of the leading term is $6$ and the substitution involves an odd power. Setting $y = x^3$ transforms it into a quadratic equation, which factors as:

$$y^2 + 7y - 8 = 0 \quad \rightarrow \quad (y - 1)(y + 8) = 0$$

The two values are:

$$y_1 = 1, \qquad y_2 = -8$$

- - -

Each value of $y$ is substituted back through $x^3 = y$. Since the index of the root is odd, every real value of $y$ yields exactly one real solution, including the negative one. For $y = 1$:

$$x^3 = 1 \quad \rightarrow \quad x = 1$$

For $y = -8$:

$$x^3 = -8 \quad \rightarrow \quad x = -2$$

Both values are real, so the equation has two solutions:

$$x = -2 \quad x = 1$$

> Equations of higher even degree, such as the one above, illustrate that the substitution method extends to any exponent of the form $2n$, with the parity of $n$ governing how each root $y_i$ is converted back into values of $x$.
