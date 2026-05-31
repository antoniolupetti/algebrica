---
title: Absolute Value Equations
source: https://algebrica.org/absolute-value-equations/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - equations
---

## Introduction

Absolute value equations are a particular class of [equations](../equations/) in which the unknown $x$ appears inside an [absolute value](../absolute-value/) expression. The absolute value measures how far a [number](../types-of-numbers/) lies from zero on the number line, regardless of its sign, and therefore transforms any real number into its non-negative counterpart according to the following rule:

$$
|x| =
\begin{cases}
x & \text{if } x \geq 0 \\[6pt]
-x & \text{if } x < 0
\end{cases}
$$

When an equation involves an absolute value, both cases must be considered, since the sign of the expression inside the bars determines which branch of the definition applies. This distinction typically splits the original problem into two separate equations, each valid on its own interval, which are then examined individually.

## Properties

The [absolute value function](../absolute-value-function/) $|x|$ obeys several algebraic properties that describe how it interacts with the basic arithmetic operations and with comparisons. These rules are the foundation for simplifying expressions and solving equations that contain absolute values. The most useful identities are the following:

[class="table-1"]

|                            |                                                                                                                                 |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Symmetry                   | $$\lvert x \rvert = \lvert -x \rvert \quad \forall x \in \mathbb{R}$$                                                           |
| Product                    | $$\lvert xy \rvert = \lvert x \rvert \cdot \lvert y \rvert \quad \forall x, y \in \mathbb{R}$$                                  |
| Equal absolute values      | $$\lvert x \rvert = \lvert y \rvert \iff x = \pm y \quad \forall x, y \in \mathbb{R}$$                                          |
| Comparison through squares | $$\lvert x \rvert \leq \lvert y \rvert \iff x^2 \leq y^2 \quad \forall x, y \in \mathbb{R}$$                                    |
| Quotient                   | $$\left\lvert \frac{x}{y} \right\rvert = \frac{\lvert x \rvert}{\lvert y \rvert} \quad \forall x, y \in \mathbb{R},\ y \neq 0$$ |
| Square root relation       | $$\sqrt{x^2} = \lvert x \rvert \quad \forall x \in \mathbb{R}$$                                                                 |
[/class]

> These properties allow absolute value expressions to be rewritten in equivalent forms, which often simplifies the calculations required to solve the associated equations.

## Solving absolute value equations

Solving an equation that contains an absolute value requires analyzing the expression inside the bars and the signs it can take. The strategy depends on the structure of the equation, that is, on whether the absolute value equals a constant, another expression, or a second absolute value. In each situation the equation is separated into distinct cases that reflect the definition of the absolute value.

Consider first the basic case in which the absolute value equals a constant:

$$|A(x)| = a$$

When $a \geq 0$, this equation is equivalent to $A(x) = a$ or $A(x) = -a$. When $a < 0$, the equation has no solution, since an absolute value can never be negative. For instance, the equation $|3 + 2x| = -2$ admits no solution because the left-hand side is non-negative for every real $x$.

- - -

Consider now the case in which the absolute value equals another expression:

$$|A(x)| = B(x)$$

Here the solution requires taking into account the sign of $A(x)$, because the definition of the absolute value must be applied separately on each interval where that sign is constant.

- - -

A further case arises when both sides of the equation are absolute values:

$$|A(x)| = |B(x)|$$

By the property $|A| = |B| \iff A = \pm B$, this equation is equivalent to the two equations $A(x) = B(x)$ and $A(x) = -B(x)$, which can be solved directly without any preliminary sign analysis. The solutions of both equations are then collected together. The examples below illustrate these situations in increasing order of complexity.

## Example 1

We solve the equation in which an absolute value equals a positive constant:

$$|3x - 1| = 5$$

Since the right-hand side is positive, the definition of the absolute value gives two possibilities for the expression inside the bars, according to its sign. The equation is therefore equivalent to:

$$3x - 1 = 5 \quad \text{or} \quad 3x - 1 = -5$$

Solving the first equation isolates the unknown:

$$3x = 6 \rightarrow x = 2$$

Solving the second equation in the same way gives:

$$3x = -4 \rightarrow x = -\frac{4}{3}$$

Both values are admissible, since the constant on the right-hand side is positive and no further constraint applies. The equation has two solutions:

$$x = -\frac{4}{3} \quad x = 2$$

## Example 2

We solve the equation:

$$|2x - 4| = x + 1$$

We begin by analyzing the sign of the expression inside the bars. The condition $2x - 4 \geq 0$ holds when $x \geq 2$, so the absolute value can be written as a piecewise expression:

$$
|2x - 4| =
\begin{cases}
2x - 4 & \text{if } x \geq 2 \\[6pt]
-2x + 4 & \text{if } x < 2
\end{cases}
$$

- - -

On the interval $x \geq 2$ the absolute value equals $2x - 4$, which leads to the system:

$$
\begin{cases}
x \geq 2 \\[6pt]
2x - 4 = x + 1
\end{cases}
$$

Solving the second equation isolates the unknown:

$$
\begin{cases}
x \geq 2 \\[6pt]
2x - x = 1 + 4 \rightarrow x = 5
\end{cases}
$$

The value $x = 5$ is acceptable because it satisfies the condition $x \geq 2$.

> The pair formed by the constraint and the equation is a [system of inequalities](../systems-of-inequalities/) in one variable. The dedicated entry discusses the solving process and how to handle more involved cases.

- - -

On the interval $x < 2$ the absolute value equals $-2x + 4$, which leads to the second system:

$$
\begin{cases}
x < 2 \\[6pt]
-2x + 4 = x + 1
\end{cases}
$$

Solving the second equation gives:

$$
\begin{cases}
x < 2 \\[6pt]
-2x - x = 1 - 4 \rightarrow -3x = -3 \rightarrow x = 1
\end{cases}
$$

The value $x = 1$ is acceptable because it satisfies the condition $x < 2$. Collecting the results from both intervals, the equation has two solutions:

$$x = 1 \quad x = 5$$

## Example 3

We solve the equation:

$$\frac{|3x|}{|x + 1|} = |x|$$

This is a [rational equation](../rational-equations/), so we first determine the conditions of existence, given by the values of $x$ that do not annihilate the denominator. The denominator vanishes when $x = -1$, and this value must therefore be excluded from the set of solutions.

- - -

Using the properties of the absolute value, the left-hand side can be rewritten as a single absolute value:

$$\left| \frac{3x}{x + 1} \right| = |x|$$

By the property $|A| = |B| \iff A = \pm B$, the equation splits into two cases according to the sign relating the two arguments. We start with the first case:

$$\frac{3x}{x + 1} = x \rightarrow 3x = x^2 + x \rightarrow x^2 - 2x = 0 \rightarrow x(x - 2) = 0$$

This is a [quadratic equation](../quadratic-equations/) whose solutions are:

$$x = 0 \quad x = 2$$

Both values are acceptable because they differ from $-1$.

> The quadratic equation was solved without the [quadratic formula](../quadratic-formula/), by [factoring](../factoring-quadratic-equations/) the corresponding [polynomial](../polynomials/) and finding the values of $x$ that make each linear factor vanish.

- - -

We now consider the second case:

$$\frac{3x}{x + 1} = -x \rightarrow 3x = -x^2 - x \rightarrow x^2 + 4x = 0 \rightarrow x(x + 4) = 0$$

Proceeding as above, the quadratic equation has the solutions:

$$x = 0 \quad x = -4$$

Both values are acceptable because they differ from $-1$. Collecting the solutions of the two cases, the equation has three distinct solutions:

$$x = -4 \quad x = 0 \quad x = 2$$

## Example 4

We solve an equation containing two distinct absolute values:

$$|x - 1| + |x + 2| = 5$$

When several absolute values appear together, the sign of each expression inside the bars must be examined separately. The two expressions change sign at $x = 1$ and at $x = -2$, and these critical points divide the real line into three intervals on which every absolute value has a constant sign. The equation is then solved on each interval, replacing each absolute value with the appropriate branch of its definition.

- - -

On the interval $x < -2$ both expressions are negative, so the equation becomes:

$$
\begin{cases}
x < -2 \\[6pt]
-(x - 1) - (x + 2) = 5
\end{cases}
$$

Expanding and collecting the unknown gives:

$$
\begin{cases}
x < -2 \\[6pt]
-2x - 1 = 5 \rightarrow x = -3
\end{cases}
$$

The value $x = -3$ is acceptable because it satisfies the condition $x < -2$.

- - -

On the interval $-2 \leq x < 1$ the first expression is negative while the second is non-negative, so the equation becomes:

$$
\begin{cases}
-2 \leq x < 1 \\[6pt]
-(x - 1) + (x + 2) = 5
\end{cases}
$$

The terms in $x$ cancel and the equation reduces to a contradiction:

$$-(x - 1) + (x + 2) = 3 \neq 5$$

This interval therefore contributes no solution.

- - -

On the interval $x \geq 1$ both expressions are non-negative, so the equation becomes:

$$
\begin{cases}
x \geq 1 \\[6pt]
(x - 1) + (x + 2) = 5
\end{cases}
$$

Collecting the unknown gives:

$$
\begin{cases}
x \geq 1 \\[6pt]
2x + 1 = 5 \rightarrow x = 2
\end{cases}
$$

The value $x = 2$ is acceptable because it satisfies the condition $x \geq 1$. Collecting the contributions of the three intervals, the equation has two solutions:

$$x = -3 \quad x = 2$$

> Equations of this kind are closely related to [inequalities with absolute value](../inequalities-with-absolute-value/), where the same case analysis is applied to comparisons rather than equalities.
