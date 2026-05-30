---
title: Quadratic Equations with Parameters
source: https://algebrica.org/quadratic-equations-with-parameters/
license: CC BY-NC 4.0
tags:
  - discriminant
  - parameters
  - quadratic-equation
  - sign-analysis
---

## Definition

[Quadratic equations](../quadratic-equations/) are usually introduced in their classical form, where all coefficients are fixed real numbers. The standard expression serves as the basic model for every second-degree equation:

$$ax^{2} + bx + c = 0$$

The key ideas behind quadratic equations are closely linked to the geometry of the [parabola](../parabola/) and to the behaviour of the [discriminant](../quadratic-formula/). These elements determine how the graph bends, where its vertex lies, and whether the equation has two real solutions, a repeated solution, or a pair of [complex roots](../quadratic-equations-with-complex-solutions/).

![Img. 1](svg/quadratic-equations.svg)

In many situations, however, the coefficients are not constant but depend on an external quantity treated as a parameter. The numbers $a$, $b$, and $c$ then become functions of a real parameter $k$, and the equation takes the more general form:

$$a(k)x^{2} + b(k)x + c(k) = 0, \qquad a(k) \neq 0$$

The condition $a(k) \neq 0$ prevents the equation from collapsing into a [linear equation with parameters](../linear-equations-with-parameters/) as the parameter varies, ensuring that it retains the structure of a quadratic for all admissible values of $k$.

> This page focuses on the quadratic case. For a broader discussion of parametric equations across different degrees, see [equations with parameters](../equations-with-parameters/).

## The role of the discriminant

The discriminant describes how the solutions of a quadratic equation behave. When the coefficients depend on a parameter, this idea is unchanged, but the discriminant becomes a function of that parameter. Starting from the coefficients $a(k)$, $b(k)$, and $c(k)$, we obtain:

$$\Delta(k) = b(k)^{2} - 4a(k)c(k)$$

In this form the discriminant gives a picture of what happens to the roots for each value of $k$. Its sign determines the nature of the solutions:

+ When $\Delta(k) > 0$, the equation has two distinct real solutions.
+ When $\Delta(k) = 0$, the equation has one real solution that appears as a double root.
+ When $\Delta(k) < 0$, the equation has two [complex conjugate solutions](../quadratic-equations-with-complex-solutions/).

## Example 1

Consider the quadratic equation:

$$x^{2} + kx + 1 = 0$$

This example is useful because each coefficient depends on the parameter $k$ in a simple way:

$$a(k) = 1 \qquad b(k) = k \qquad c(k) = 1$$

In the standard case the discriminant is $\Delta = b^{2} - 4ac$, and its sign determines the nature of the solutions. Substituting $a(k)$, $b(k)$, and $c(k)$ into the same formula gives:

$$\Delta(k) = b(k)^{2} - 4a(k)c(k)$$

which simplifies to:

$$\Delta(k) = k^{2} - 4$$

To determine when real solutions exist, we study the [quadratic inequality](../quadratic-inequalities/):

$$k^{2} - 4 \ge 0$$

Solving it yields two separate intervals:

$$k \le -2 \quad\text{or}\quad k \ge 2$$

For these values the discriminant is positive and the quadratic has two distinct real roots. At the boundary points $k = \pm 2$ the discriminant becomes zero and the equation has a single repeated solution. When:

$$-2 < k < 2$$

the discriminant is negative and the equation has no real roots, producing instead a pair of complex conjugate solutions. The following table summarises the [sign analysis](../sign-analysis-in-inequalities/) of $k - 2$, $k + 2$, and their product across the three intervals determined by the critical points $k = -2$ and $k = 2$:

[class="table-sign"]

|                       |        | $-2$ | $2$ |
|:---------------------:|:------:|:----:|:---:|
| $k - 2 > 0$           | $-$    | $-$  | $+$ |
| $k + 2 > 0$           | $-$    | $+$  | $+$ |
| $(k - 2)(k + 2) > 0$  | $+$    | $-$  | $+$ |

[/class]

- - -

When the roots are real, an explicit expression for them is useful. Applying the quadratic formula to this family gives the two real solutions in closed form:

$$x = \frac{-k \pm \sqrt{k^{2} - 4}}{2}$$

This expression shows how each root depends on the parameter $k$ and makes it possible to study how the solutions move along the real line as $k$ varies. From the analysis above, the outcomes are:

+ If $k < -2$ or $k > 2$, the equation has two distinct real solutions.
+ If $k = \pm 2$, there is one real double solution.
+ If $-2 < k < 2$, the equation has two complex conjugate solutions.

## Geometric interpretation of parameter changes

Continuing with the equation of Example 1, it is helpful to look at how the graph of the corresponding parabola changes as the parameter $k$ varies. To each value of $k$ we associate the [parabola](../parabola/):

$$y = x^{2} + kx + 1$$

so analysing the roots is equivalent to studying where this curve meets the $x$-axis. As the parameter moves, the entire family of parabolas shifts smoothly. The behaviour can be described in three regimes.

- - -

When $|k|$ is very large ($k \to +\infty$ or $k \to -\infty$), the linear term $kx$ dominates and the two roots separate widely. A simple [asymptotic](../asymptotes/) argument shows that one root tends to $0$ while the other behaves approximately like $-k$. Geometrically, the intersection points move far apart: one stays close to the origin, while the other drifts along the negative axis, and the parabola appears increasingly tilted.

- - -

At the critical values $k = \pm 2$, the discriminant becomes zero. This is the moment when the parabola touches the $x$-axis at exactly one point: the graph has a single point of tangency, the equation has one repeated root, and the vertex lies on the axis.

- - -

Within the interval $-2 < k < 2$, the discriminant is negative, so the equation has no real solutions. Geometrically, the parabola does not meet the $x$-axis at all. Since the leading coefficient is positive, the parabola opens upward, and in this region the vertex lies strictly above the $x$-axis. The entire curve stays on one side of the axis, reflecting that the solutions move into the complex plane.

## Example 2

Consider a more elaborate parameter-dependent quadratic equation:

$$(a + 2)x^{2} + (3a - 1)x + (a - 4) = 0, \qquad a \neq -2$$

where the condition $a \neq -2$ ensures that the coefficient of $x^{2}$ does not vanish, so the expression remains a genuine quadratic for every admissible value of the parameter. The goal is to determine for which values of $a$ the equation has two distinct real solutions. As usual, this depends on the sign of the [discriminant](../quadratic-formula/). To avoid confusion with the parameter $a$, we denote the coefficients of the present quadratic by $A$, $B$, $C$, so the general formula reads:

$$\Delta = B^{2} - 4AC$$

Substituting the coefficients of the present equation gives:

$$\Delta(a) = (3a - 1)^{2} - 4(a + 2)(a - 4)$$

- - -

Expanding the two parts, we first compute the square:

$$(3a - 1)^{2} = 9a^{2} - 6a + 1$$

and then the product of the quadratic and constant coefficients:

$$(a + 2)(a - 4) = a^{2} - 2a - 8$$

Inserting these expressions into the discriminant and collecting like terms gives the simplified form:

$$\Delta(a) = 5a^{2} + 2a + 33$$

- - -

This is a quadratic function of $a$ with positive leading coefficient. To determine whether it can ever be zero or negative, we examine its discriminant:

$$2^{2} - 4 \cdot 5 \cdot 33 = 4 - 660 < 0$$

Since this value is negative, the parabola associated with $5a^{2} + 2a + 33$ never meets the horizontal axis: it remains strictly positive for all real values of $a$. Therefore:

$$\Delta(a) > 0 \quad \forall\, a \in \mathbb{R}$$

The equation has two distinct real solutions for every real value of the parameter $a$, except $a = -2$, which must be excluded because it would make the coefficient of $x^{2}$ vanish and reduce the expression to a first-degree equation.

## Example 3

Consider the parameter-dependent quadratic equation:

$$x^{2} - (a - 4)x + (a^{2} - a) = 0$$

where $a$ is a real parameter. We want the values of $a$ for which the product of the two solutions is strictly less than $2$. For a general monic quadratic equation:

$$x^{2} + bx + c = 0$$

the product of the solutions satisfies $x_{1}x_{2} = c$.

> This identity follows from the [factorised form](../factoring-quadratic-equations/) of a monic quadratic, where $x^{2} + bx + c = (x - x_{1})(x - x_{2})$. Expanding the product, the constant term appears as $x_{1}x_{2}$, which is why the product of the solutions equals $c$.

- - -

Here the constant term is $c = a^{2} - a$, and requiring the product of the two solutions to be less than $2$ gives the inequality:

$$a^{2} - a < 2$$

Bringing all terms to the left gives:

$$a^{2} - a - 2 < 0$$

The quadratic [polynomial](../polynomials/) on the left factors as:

$$a^{2} - a - 2 = (a - 2)(a + 1)$$

The critical points are therefore $a = -1$ and $a = 2$. To determine where the expression is negative, we analyse the signs of the two factors:

[class="table-sign"]

|                      |     | $-1$ | $2$ |
|:--------------------:|:---:|:----:|:---:|
| $a - 2 > 0$          | $-$ | $-$  | $+$ |
| $a + 1 > 0$          | $-$ | $+$  | $+$ |
| $(a - 2)(a + 1) < 0$ | $+$ | $-$  | $+$ |

[/class]

- - -

The sign chart shows that $(a - 2)(a + 1) < 0$ when the parameter lies between the two roots:

$$-1 < a < 2$$

The product of the solutions satisfies $x_{1}x_{2} < 2$ if and only if $-1 < a < 2$.
