# Quadratic Formula

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/quadratic-formula/

## Definition

Given a [quadratic equation](../quadratic-equations/) in standard form \\(ax^2 + bx + c = 0\\), the quadratic formula provides an explicit expression for its roots in terms of the coefficients \\(a\\), \\(b\\), and \\(c\\):

\\[
x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
\\]

The formula is derived by applying the method of [completing the square](../completing-the-square/) to the general standard form, and constitutes one of the central results of algebra. It is universally applicable to any quadratic equation with real or complex coefficients, provided that \\(a \neq 0\\).

+ \\(a, b, c\\) are the coefficients of the equation, with \\(a \neq 0\\).
+ The plus-minus symbol reflects the fact that the formula yields two values, corresponding to the two roots of the polynomial.
+ By the [Fundamental Theorem of Algebra](/roots-of-a-polynomial/), a polynomial of degree 2 has exactly two roots in \\(\mathbb{C}\\), counted with multiplicity. These may be two distinct real numbers, a repeated real root, or a pair of complex conjugates depending on the sign of the discriminant.

The quadratic formula is valid only when square roots can be computed. When the coefficients are [real](../properties-of-real-numbers/), the formula always yields solutions in \\(\mathbb{C}\\), since every complex number has a square root in \\(\mathbb{C}\\). This guarantees that no quadratic equation is ever without solutions, provided one works in the right setting.

> The quadratic formula also provides a natural framework for studying how the roots vary when the coefficients depend on a parameter. In that setting, the discriminant becomes a function of the parameter itself, and its sign determines how the nature of the roots changes as the parameter varies. This analysis is developed in detail in the dedicated entry on [quadratic equations with parameters](../quadratic-equations-with-parameters/).

- - -
## Discriminant

The term within the square root, \\(\Delta = b^2 - 4ac\\), is known as the discriminant, and it is crucial in determining the nature and number of solutions of a quadratic equation.

If \\( \Delta > 0\\), the quadratic equation has two distinct real solutions. \\[S = \\{x_1, x_2\\} \quad x_1, x_2 \in \mathbb{R} \quad x_1 \neq x_2 \\] \\[ x_{1,2} = \frac{-b \pm \sqrt{b^2-4ac}}{2a}\\]

- - -

If \\( \Delta = 0\\), the quadratic equation has two coincident real solutions. \\[S = \\{x\\} \quad x \in \mathbb{R} \quad x = x_1 = x_2 \\] \\[x= -\frac{b}{2a}\\]

- - -

If \\( \Delta < 0\\), the quadratic equation has no real solutions. Instead, it gives rise to a pair of complex conjugate solutions with nonzero imaginary part. \\[\nexists \hspace{10px} x \in \mathbb{R}\\] \\[x_{1,2} = \frac{-b \pm i\sqrt{4ac - b^2}}{2a}\\]
A detailed treatment of this case is presented in the entry on [quadratic equations with complex solutions](../quadratic-equations-with-complex-solutions/).

- - -

The discriminant \\(\Delta = b^2 - 4ac\\) also determines how the graph of the quadratic function \\(f(x) = ax^2 + bx + c\\) behaves with respect to the x-axis. Geometrically, a quadratic equation represents a [parabola](../parabola). Consider for example the following equation \\( y = x^2 + 4x + 4 \\).

In general we have:

+ If \\(\Delta \gt 0\\), the graph of the parabola intersects the x-axis at two distinct points.  

+ if \\(\Delta = 0\\), the graph of the parabola is tangent to the x-axis at a single point (the vertex).  

+ if \\(\Delta \lt 0\\), the graph of the parabola does not intersect the \\(x\\)-axis at all.
- - -
## Vieta's formulas

For a quadratic equation \\( ax^2 + bx + c = 0 \\) with roots \\( x_1 \\) and \\( x_2 \\), the sum and product of the roots are given by:

\\[x_1 + x_2 = -\frac{b}{a} \qquad x_1 \cdot x_2 = \frac{c}{a}\\]

These relations hold in \\( \mathbb{C} \\) for any value of the discriminant, and follow directly from expanding the factored form \\( a(x - x_1)(x - x_2) \\) and comparing coefficients. Their derivation and applications, including the role they play in factoring higher-degree polynomials, are discussed in detail in the entry on [trinomial equations](../trinomial-equations/).

- - -
## Example 1

Solve the equation \\( x^2 - 4x + 2 = 0 \\) using the quadratic formula. The equation is already in standard form, with \\( a = 1 \\), \\( b = -4 \\), and \\( c = 2 \\). Substituting into the formula:

\\[
\begin{align*}
x_{1,2} &= \frac{-(-4) \pm \sqrt{(-4)^2 - 4(1)(2)}}{2(1)} \\\\[0.8em]
&= \frac{4 \pm \sqrt{16 - 8}}{2} \\\\[0.8em]
&= \frac{4 \pm \sqrt{8}}{2}
\end{align*}
\\]

Since \\( \Delta = 8 > 0 \\), the equation has two distinct real solutions. Simplifying \\( \sqrt{8} = 2\sqrt{2} \\) we obtain:

\\[x_{1,2} = \frac{4 \pm 2\sqrt{2}}{2} = 2 \pm \sqrt{2}\\]

The solutions are therefore:
\\[ x_1 = 2 - \sqrt{2}\\]
\\[ x_2 = 2 + \sqrt{2} \\]