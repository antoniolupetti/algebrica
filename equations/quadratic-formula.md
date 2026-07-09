---
title: Quadratic Formula
source: https://algebrica.org/quadratic-formula/
license: CC BY-NC 4.0
tags:
  - completing-the-square
  - discriminant
  - quadratic-equation
  - quadratic-formula
  - vieta-formulas
---

## Definition

Given a [quadratic equation](../quadratic-equations/) in standard form $ax^2 + bx + c = 0$, the quadratic formula provides an explicit expression for its roots in terms of the coefficients $a$, $b$, and $c$:

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

The formula is derived by applying the method of [completing the square](../completing-the-square/) to the general standard form, and it constitutes one of the central results of elementary algebra. It applies to any quadratic equation with real or complex coefficients, provided that $a \neq 0$.

+ $a$, $b$, $c$ are the coefficients of the equation, with $a \neq 0$.
+ The plus-minus symbol reflects the fact that the formula yields two values, corresponding to the two roots of the polynomial.
+ By the [fundamental theorem of algebra](../roots-of-a-polynomial/), a polynomial of degree two has exactly two roots in $\mathbb{C}$, counted with multiplicity. These may be two distinct real numbers, a repeated real root, or a pair of complex conjugates, depending on the sign of the discriminant.

The quadratic formula is valid whenever square roots can be computed. When the coefficients are [real](../properties-of-real-numbers/), the formula always yields solutions in $\mathbb{C}$, since every complex number has a square root in $\mathbb{C}$. This guarantees that no quadratic equation is ever without solutions, provided one works in the right setting.

> The quadratic formula also provides a natural framework for studying how the roots vary when the coefficients depend on a parameter. In that setting the discriminant becomes a function of the parameter itself, and its sign determines how the nature of the roots changes as the parameter varies. This analysis is developed in the dedicated entry on [quadratic equations with parameters](../quadratic-equations-with-parameters/).

## Derivation by completing the square

The quadratic formula is obtained from the general equation by the method of [completing the square](../completing-the-square/). The starting point is the standard form, with the condition $a \neq 0$ that guarantees the equation is genuinely quadratic:

$$ax^2 + bx + c = 0$$

The first step moves the constant term to the right-hand side, isolating the terms that contain the unknown:

$$ax^2 + bx = -c$$

Since completing the square applies to a monic expression, both sides are divided by the leading coefficient $a$, which is nonzero by assumption:

$$x^2 + \frac{b}{a}x = -\frac{c}{a}$$

- - -

The left-hand side is now turned into a perfect square. The coefficient of the linear term is $\frac{b}{a}$, and completing the square requires adding the square of its half, that is $\left(\frac{b}{2a}\right)^2$, to both sides so that the equality is preserved:

$$x^2 + \frac{b}{a}x + \left(\frac{b}{2a}\right)^2 = -\frac{c}{a} + \left(\frac{b}{2a}\right)^2$$

By construction the left-hand side is the square of a binomial, while the right-hand side is combined over the common denominator $4a^2$:

$$\left(x + \frac{b}{2a}\right)^2 = \frac{b^2 - 4ac}{4a^2}$$

- - -

Taking the square root of both sides introduces the double sign, since both the positive and the negative root satisfy the equality. The denominator $4a^2$ is a perfect square whose root is $2|a|$, and the double sign already accounts for the sign of $a$:

$$x + \frac{b}{2a} = \pm\frac{\sqrt{b^2 - 4ac}}{2a}$$

Moving the term $\frac{b}{2a}$ to the right-hand side isolates the unknown:

$$x = -\frac{b}{2a} \pm \frac{\sqrt{b^2 - 4ac}}{2a}$$

The two fractions share the denominator $2a$ and combine into the single expression that constitutes the quadratic formula:

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

This derivation shows that the formula holds for every quadratic equation with $a \neq 0$, and that the quantity $b^2 - 4ac$ appearing under the root, the discriminant, arises naturally from the algebraic manipulation.

## Discriminant

The term under the square root, $\Delta = b^2 - 4ac$, is known as the discriminant, and it determines the number and nature of the solutions of a quadratic equation.

When $\Delta > 0$, the equation has two distinct real solutions:

$$S = \{\ x_1, x_2 \ \} \qquad x_1, x_2 \in \mathbb{R} \qquad x_1 \neq x_2$$

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

When $\Delta = 0$, the equation has two coincident real solutions, that is, a single root of multiplicity two:

$$S = \{\ x \ \} \qquad x \in \mathbb{R} \qquad x = x_1 = x_2$$
$$x = -\frac{b}{2a}$$

When $\Delta < 0$, the equation has no real solutions. It instead gives rise to a pair of complex conjugate solutions with nonzero imaginary part:

$$\nexists\ x \in \mathbb{R}$$
$$x_{1,2} = \frac{-b \pm i\sqrt{4ac - b^2}}{2a}$$

A detailed treatment of this last case is presented in the entry on [quadratic equations with complex solutions](../quadratic-equations-with-complex-solutions/).

- - -

The discriminant $\Delta = b^2 - 4ac$ also determines how the graph of the quadratic function $f(x) = ax^2 + bx + c$ behaves with respect to the $x$-axis. Geometrically, a quadratic equation is associated with a [parabola](../parabola/), and the sign of the discriminant fixes its position relative to the axis:

![IMG. 1](../polynomials/svg/polynomials-2.svg)

+ If $\Delta > 0$, the parabola intersects the $x$-axis at two distinct points.
+ If $\Delta = 0$, the parabola is tangent to the $x$-axis at a single point, the vertex.
+ If $\Delta < 0$, the parabola does not intersect the $x$-axis.

The relationship between the discriminant and the shape of the curve is examined further in the entry on the [geometrical meaning of quadratic equations](../geometrical-meaning-quadratic-equations/).

## Vieta's formulas

For a quadratic equation $ax^2 + bx + c = 0$ with roots $x_1$ and $x_2$, the sum and the product of the roots are given by:

$$x_1 + x_2 = -\frac{b}{a} \qquad x_1x_2 = \frac{c}{a}$$

These relations hold in $\mathbb{C}$ for any value of the discriminant, and they follow directly from expanding the [factored form](../factoring-quadratic-equations/) $a(x - x_1)(x - x_2)$ and comparing coefficients. The general statement for polynomials of any degree, together with its derivation and applications, is developed in the entry on [Vieta's formulas](../vieta-formulas/), while the role these relations play in factoring higher-degree polynomials is discussed in the entry on [trinomial equations](../trinomial-equations/).

## Example 1

Solve the equation $x^2 - 4x + 2 = 0$ using the quadratic formula. The equation is already in standard form, with $a = 1$, $b = -4$, and $c = 2$. Substituting into the formula gives:

$$
\begin{align*}
x_{1,2} &= \frac{-(-4) \pm \sqrt{(-4)^2 - 4(1)(2)}}{2(1)} \\[6pt]
&= \frac{4 \pm \sqrt{16 - 8}}{2} \\[6pt]
&= \frac{4 \pm \sqrt{8}}{2}
\end{align*}
$$

Since $\Delta = 8 > 0$, the equation has two distinct real solutions. Simplifying $\sqrt{8} = 2\sqrt{2}$ we obtain:

$$x_{1,2} = \frac{4 \pm 2\sqrt{2}}{2} = 2 \pm \sqrt{2}$$

The two solutions are therefore $x_1 = 2 - \sqrt{2}$ and $x_2 = 2 + \sqrt{2}$.

## Example 2

Solve the equation $x^2 - 6x + 9 = 0$. Here $a = 1$, $b = -6$, and $c = 9$, so the discriminant is:

$$\Delta = (-6)^2 - 4(1)(9) = 36 - 36 = 0$$

Since $\Delta = 0$, the two roots coincide. Substituting into the formula gives:

$$x = -\frac{b}{2a} = -\frac{-6}{2(1)} = 3$$

The equation has the single real root $x = 3$, counted with multiplicity two. The associated parabola is tangent to the $x$-axis at the point $(3, 0)$.

## Example 3

Solve the equation $x^2 + 2x + 5 = 0$. The coefficients are $a = 1$, $b = 2$, and $c = 5$, and the discriminant is:

$$\Delta = 2^2 - 4(1)(5) = 4 - 20 = -16$$

Since $\Delta < 0$, the equation has no real solutions. Writing the square root in terms of the imaginary unit, $\sqrt{-16} = 4i$, the formula gives:

$$x_{1,2} = \frac{-2 \pm 4i}{2} = -1 \pm 2i$$

The solutions form the complex conjugate pair $x_1 = -1 - 2i$ and $x_2 = -1 + 2i$.