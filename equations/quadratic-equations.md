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

+ The coefficients $a$, $b$, and $c$ are constants, while $x$ represents the variable.
+ When $a = 0$ the equation reduces to the [linear equation](../linear-equations/) $bx + c = 0$.
+ If both $a = 0$ and $b = 0$, the equation becomes constant and has either no solution or infinitely many, depending on whether $c \neq 0$ or $c = 0$.

Replacing the equality sign with one of the relations $<$, $>$, $\leq$, or $\geq$ turns the equation into a [quadratic inequality](../quadratic-inequalities/), which is solved by studying the sign of the same quadratic expression.

The quadratic equation is the simplest case of a [trinomial equation](../trinomial-equations/), which has the general form:

$$ax^{2n} + bx^{n} + c = 0$$

Setting $n = 1$ recovers the standard quadratic form $ax^2 + bx + c = 0$. For $n \geq 2$ the equation can be reduced to a quadratic in the auxiliary variable $y = x^n$ and solved with the same techniques.

## Geometrical interpretation

The equation $y = ax^2 + bx + c$, with $a \neq 0$, represents a [parabola](../parabola/) in the plane defined by the variables $x$ and $y$. A fuller account of this correspondence is given in the entry on the [geometrical meaning of quadratic equations](../geometrical-meaning-quadratic-equations/).

![Img. 1](svg/quadratic-equations.svg)

When the coefficient $a > 0$ the parabola opens upward and the vertex is a minimum of the function. When $a < 0$ it opens downward and the vertex is a maximum.

The real solutions of the equation $ax^2 + bx + c = 0$ correspond to the points at which the parabola intersects the $x$-axis. The sign of the [discriminant](../quadratic-formula/) $\Delta = b^2 - 4ac$ controls this configuration:

+ For $\Delta > 0$ the parabola crosses the axis at two distinct points.
+ For $\Delta = 0$ it is tangent to the axis.
+ For $\Delta < 0$ it does not intersect the axis and the equation has no real solutions.

> The condition $a \neq 0$ ensures that the equation describes a parabolic curve rather than a [linear equation](../linear-equations/).

## Resolution methods

A quadratic equation is [incomplete](../incomplete-quadratic-equations/) when either the coefficient $b$ or the coefficient $c$ is equal to zero. In this case the equation takes a simpler form and can be solved directly, without applying the general formula. The first step in solving any quadratic equation is to rewrite it in standard form:

$$ax^2 + bx + c = 0$$

This form allows the coefficients to be identified and the [discriminant](../quadratic-formula/) $\Delta = b^2 - 4ac$ to be computed. The discriminant determines the nature of the solutions:

+ Two distinct real roots when $\Delta > 0$.
+ One real root of multiplicity two when $\Delta = 0$.
+ A pair of complex conjugate roots when $\Delta < 0$.

The most general method of resolution is the [quadratic formula](../quadratic-formula/). In some cases, however, [factoring](../factoring-quadratic-equations/) or [completing the square](../completing-the-square/) can offer a more direct route to the solution.

The [fundamental theorem of algebra](../roots-of-a-polynomial/) guarantees that a quadratic equation has exactly two roots in $\mathbb{C}$, counted with multiplicity. The roots are both real when $\Delta \geq 0$, and form a pair of [complex conjugates](../quadratic-equations-with-complex-solutions/) when $\Delta < 0$.

## Quadratic formula

Given a quadratic equation in the standard form $ax^2 + bx + c = 0$, the [quadratic formula](../quadratic-formula/) expresses its roots as:

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

+ $a$, $b$, $c$ are real coefficients and $a \neq 0$.
+ The $\pm$ symbol reflects the existence of two solutions, corresponding to the two signs.
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

The following decision tree summarises the resolution strategy, moving from the simplest configurations of the coefficients to the general method.

+ Rewrite the equation in standard form $ax^2 + bx + c = 0$.
+ Calculate the discriminant $\Delta = b^2 - 4ac$.
+ Apply the quadratic formula:

$$x = \frac{-b \pm \sqrt{\Delta}}{2a}$$

+ Simplify the result.
+ If $\Delta \geq 0$ the solutions are real, while if $\Delta < 0$ the solutions are complex conjugates.

> The quadratic formula is the universal method, but not always the most efficient. When the equation is incomplete or admits an obvious factorization, the roots can often be obtained more quickly by direct inspection.

## Quadratic equations with parameters

A natural extension of the study of quadratic equations is the case in which the coefficients are not fixed numbers but depend on an external parameter. In this setting we speak of [quadratic equations with a parameter](../quadratic-equations-with-parameters/), also called literal quadratic equations, which take the form:

$$a(k)x^2 + b(k)x + c(k) = 0, \quad a(k) \neq 0$$

Varying the parameter $k$ alters the equation and, consequently, the nature of its solutions. The analysis relies on the discriminant:

$$\Delta(k) = b(k)^2 - 4a(k)c(k)$$

which, exactly as in the classical case, determines whether the equation admits two distinct real solutions, a repeated solution, or a pair of complex conjugate solutions.