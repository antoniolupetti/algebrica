---
title: Quadratic Equations
source: https://algebrica.org/quadratic-equations/
license: CC BY-NC 4.0
tags:
  - discriminant
  - parabola
  - quadratic-equation
  - quadratic-formula
  - vieta-formulas
---
## Introduction

A quadratic equation is a second-degree [polynomial equation](../polynomial-equations/) in one variable. Its standard form is the following:

$$ax^2 + bx + c = 0$$

In this expression $a$, $b$, and $c$ are real coefficients, $x$ is the unknown, and $a \neq 0$. The coefficient $a$ multiplies the quadratic term $x^2$, the coefficient $b$ multiplies the linear term $x$, and $c$ is the constant term.

+ The coefficients $a$, $b$, and $c$ are constants, while $x$ is the variable.
+ When $a = 0$ the equation reduces to the [linear equation](../linear-equations/) $bx + c = 0$.
+ If both $a = 0$ and $b = 0$, the equation becomes constant and has either no solution or infinitely many, depending on whether $c \neq 0$ or $c = 0$.

Replacing the equality sign with one of the relations $<$, $>$, $\leq$, or $\geq$ turns the equation into a [quadratic inequality](../quadratic-inequalities/), which is solved by studying the sign of the same quadratic expression.

The quadratic equation is the simplest case of a [trinomial equation](../trinomial-equations/), which has the general form:

$$ax^{2n} + bx^{n} + c = 0$$

Setting $n = 1$ recovers the standard quadratic form $ax^2 + bx + c = 0$. For $n \geq 2$ the equation can be reduced to a quadratic in the auxiliary variable $y = x^n$ and solved with the same techniques.

## Geometrical interpretation

The graph of $y = ax^2 + bx + c$, with $a \neq 0$, is a [parabola](../parabola/) in the plane defined by the variables $x$ and $y$. A fuller account of this correspondence is given in the entry on the [geometrical meaning of quadratic equations](../geometrical-meaning-quadratic-equations/).

![Img. 1](svg/quadratic-equations.svg)

When the coefficient $a > 0$ the parabola opens upward and the vertex is a minimum of the function. When $a < 0$ it opens downward and the vertex is a maximum.

The real solutions of the equation $ax^2 + bx + c = 0$ correspond to the points at which the parabola intersects the $x$-axis. The sign of the [discriminant](../quadratic-formula/) $\Delta = b^2 - 4ac$ controls this configuration:

+ For $\Delta > 0$ the parabola crosses the axis at two distinct points.
+ For $\Delta = 0$ it is tangent to the axis.
+ For $\Delta < 0$ it does not intersect the axis and the equation has no real solutions.

> The condition $a \neq 0$ ensures that the equation describes a parabolic curve rather than a [linear equation](../linear-equations/).

## Solution methods

A quadratic equation is [incomplete](../incomplete-quadratic-equations/) when either the coefficient $b$ or the coefficient $c$ is equal to zero. In this case the equation takes a simpler form and can be solved directly, without applying the general formula. The first step in solving any quadratic equation is to rewrite it in standard form:

$$ax^2 + bx + c = 0$$

This form allows the coefficients to be identified and the [discriminant](../quadratic-formula/) $\Delta = b^2 - 4ac$ to be computed. The discriminant determines the nature of the solutions:

+ Two distinct real roots when $\Delta > 0$.
+ One real root of multiplicity two when $\Delta = 0$.
+ A pair of complex conjugate roots when $\Delta < 0$.

The most general method is the [quadratic formula](../quadratic-formula/). In some cases, however, [factoring](../factoring-quadratic-equations/) or [completing the square](../completing-the-square/) can give a more direct route to the solution.

The [fundamental theorem of algebra](../roots-of-a-polynomial/) guarantees that a quadratic equation has exactly two roots in $\mathbb{C}$, counted with multiplicity. The roots are both real when $\Delta \geq 0$, and form a pair of [complex conjugates](../quadratic-equations-with-complex-solutions/) when $\Delta < 0$.

## Quadratic formula

Given a quadratic equation in the standard form $ax^2 + bx + c = 0$, the [quadratic formula](../quadratic-formula/) expresses its roots as:

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

+ $a$, $b$, $c$ are real coefficients and $a \neq 0$.
+ The $\pm$ symbol gives the two solutions, one for each sign.
+ A quadratic equation has exactly two roots in $\mathbb{C}$, counted with multiplicity.
+ By [Vieta's formulas](../quadratic-formula/), the roots satisfy $x_1 + x_2 = -b/a$ and $x_1x_2 = c/a$.

A further property of the discriminant is the following:

$$\Delta = a^2(x_1 - x_2)^2$$

This identity shows directly that $\Delta \geq 0$ when the roots are real, and that $\Delta = 0$ if and only if the two roots coincide.

> When the discriminant is negative, the solutions are complex. The dedicated entry on [quadratic equations with complex solutions](../quadratic-equations-with-complex-solutions/) covers this case in full.

## Factoring

A quadratic equation can be [factored](../factoring-quadratic-equations/) into the following form:

$$ax^2 + bx + c = 0 \quad \Longleftrightarrow \quad a(x - x_1)(x - x_2) = 0$$

In this identity $x_1$ and $x_2$ are the roots of the equation. By [Vieta's formulas](../quadratic-formula/), the roots satisfy the following relations:

$$x_1 + x_2 = -\frac{b}{a}$$
$$x_1x_2 = \frac{c}{a}$$

This method is effective when the roots can be identified by inspection or by simple trial, but it becomes impractical for equations with irrational or complex roots, where the [quadratic formula](../quadratic-formula/) is preferable.

## How to solve a quadratic equation

The following decision tree summarises the solution strategy, moving from the simplest configurations of the coefficients to the general method.

+ Rewrite the equation in standard form $ax^2 + bx + c = 0$.
+ Calculate the discriminant $\Delta = b^2 - 4ac$.
+ Apply the quadratic formula:

$$x = \frac{-b \pm \sqrt{\Delta}}{2a}$$

+ Simplify the result.
+ If $\Delta \geq 0$ the solutions are real, while if $\Delta < 0$ the solutions are complex conjugates.

> The quadratic formula is the universal method, but not always the most efficient. When the equation is incomplete or has an obvious factorization, the roots can often be obtained more quickly by direct inspection.

## Quadratic equations with parameters

A natural extension of the study of quadratic equations is the case in which the coefficients are not fixed numbers but depend on an external parameter. These are called [quadratic equations with a parameter](../quadratic-equations-with-parameters/), or literal quadratic equations, and take the form:

$$a(k)x^2 + b(k)x + c(k) = 0, \quad a(k) \neq 0$$

Varying the parameter $k$ alters the equation and, consequently, the nature of its solutions. The analysis relies on the discriminant:

$$\Delta(k) = b(k)^2 - 4a(k)c(k)$$

which, exactly as in the classical case, determines whether the equation has two distinct real solutions, a repeated solution, or a pair of complex conjugate solutions.

## Examples

The following equations illustrate how the form of the coefficients determines the most convenient resolution method. We use [factoring](../factoring-quadratic-equations/) when the linear factors can be identified directly and the [quadratic formula](../quadratic-formula/) when no simple factorisation is apparent.

[class="table-1"]

|                                     |
| :---------------------------------- |
| $9x^2 + 7x - 2 = 0$                 |
| $p^2x^2 + (p^2 - q^2)x - q^2 = 0$   |
| $x^2 + x + 2 = 0$                   |
| $\sqrt{7}x^2 - 6x - 13\sqrt{7} = 0$ |
| $z^2 - 32z - 105 = 0$               |
| $\sqrt{2}x^2 - 3x - 2\sqrt{2} = 0$  |
| $n^2 + 7n + 15 = 5$                 |
[/class]

We begin by solving the first equation. The product of the constant terms must be $-2$, and the factors $(9x - 2)$ and $(x + 1)$ produce the required linear coefficient:

$$9x^2 + 7x - 2 = (9x - 2)(x + 1)$$

The equation is therefore equivalent to:

$$(9x - 2)(x + 1) = 0$$

The zero-product property gives:

$$9x - 2 = 0 \quad \text{or} \quad x + 1 = 0$$

Hence $x = 2/9$ or $x = -1$. The associated [parabola](../parabola/) $y = 9x^2 + 7x - 2$ intersects the $x$-axis at $(-1, 0)$ and $(2/9, 0)$, and it intersects the $y$-axis at $(0, -2)$. Its vertex is:

$$V\left(-\frac{7}{18}, -\frac{121}{36}\right)$$

The equation has two distinct real solutions, $x_1 = -1$ and $x_2 = 2/9$.

- - -

For the second equation to be quadratic, we assume $p \neq 0$. Its left-hand side has the direct factorization:

$$p^2x^2 + (p^2 - q^2)x - q^2 = (x + 1)(p^2x - q^2)$$

The equation becomes:

$$(x + 1)(p^2x - q^2) = 0$$

Setting each factor equal to zero gives:

$$x + 1 = 0 \quad \text{or} \quad p^2x - q^2 = 0$$

The equation has two distinct real solutions, $x_1 = -1$ and $x_2 = q^2/p^2$, for every $p, q \in \mathbb{R}$ with $p \neq 0$.

- - -

The third polynomial has no simple factorization over $\mathbb{R}$, so we calculate its [discriminant](../quadratic-formula/):

$$\Delta = 1^2 - 4(1)(2) = -7$$

Since the discriminant is negative, the quadratic formula gives two [complex conjugate](../quadratic-equations-with-complex-solutions/) values:

$$
\begin{align}
x_{1,2} &= \frac{-1 \pm \sqrt{-7}}{2} \\[6pt]
&= \frac{-1 \pm i\sqrt{7}}{2}
\end{align}
$$

The parabola $y = x^2 + x + 2$ does not intersect the $x$-axis, while it intersects the $y$-axis at $(0, 2)$. Its vertex is $V(-1/2, 7/4)$, which lies above the $x$-axis. The equation has no real solutions, only the two complex conjugates $x_1 = (-1 + i\sqrt{7})/2$ and $x_2 = (-1 - i\sqrt{7})/2$.

- - -

In the fourth equation the irrational coefficients make direct factorization less obvious. We therefore identify $a = \sqrt{7}$, $b = -6$, and $c = -13\sqrt{7}$ and calculate the discriminant:

$$
\begin{align}
\Delta &= (-6)^2 - 4(\sqrt{7})(-13\sqrt{7}) \\[6pt]
&= 36 + 364 \\[6pt]
&= 400
\end{align}
$$

The quadratic formula gives:

$$x_{1,2} = \frac{6 \pm 20}{2\sqrt{7}}$$

Simplifying the two values separately yields:

$$x_1 = \frac{26}{2\sqrt{7}} = \frac{13\sqrt{7}}{7}, \qquad x_2 = \frac{-14}{2\sqrt{7}} = -\sqrt{7}$$

The equation has two distinct real solutions, $x_1 = 13\sqrt{7}/7$ and $x_2 = -\sqrt{7}$.

- - -

For the fifth equation we seek two integers whose product is $-105$ and whose sum is $-32$. The integers $-35$ and $3$ satisfy both conditions, so the polynomial factors as:

$$z^2 - 32z - 105 = (z - 35)(z + 3)$$

The equation is equivalent to:

$$(z - 35)(z + 3) = 0$$

The zero-product property gives $z - 35 = 0$ or $z + 3 = 0$. The equation has two distinct real solutions, $z_1 = 35$ and $z_2 = -3$.

- - -

For the sixth equation we apply the quadratic formula, with $a = \sqrt{2}$, $b = -3$, and $c = -2\sqrt{2}$. The discriminant is:

$$
\begin{align}
\Delta &= (-3)^2 - 4(\sqrt{2})(-2\sqrt{2}) \\[6pt]
&= 9 + 16 \\[6pt]
&= 25
\end{align}
$$

Substituting into the formula gives:

$$x_{1,2} = \frac{3 \pm 5}{2\sqrt{2}}$$

The two values simplify as follows:

$$x_1 = \frac{8}{2\sqrt{2}} = 2\sqrt{2}, \qquad x_2 = \frac{-2}{2\sqrt{2}} = -\frac{\sqrt{2}}{2}$$

The equation has two distinct real solutions, $x_1 = 2\sqrt{2}$ and $x_2 = -\sqrt{2}/2$.

- - -

The seventh equation must first be written in standard form. Subtracting $5$ from both sides gives:

$$n^2 + 7n + 10 = 0$$

The integers $5$ and $2$ have product $10$ and sum $7$, so the left-hand side factors as:

$$n^2 + 7n + 10 = (n + 5)(n + 2)$$

The equation is therefore equivalent to:

$$(n + 5)(n + 2) = 0$$

The equation has two distinct real solutions, $n_1 = -5$ and $n_2 = -2$.
