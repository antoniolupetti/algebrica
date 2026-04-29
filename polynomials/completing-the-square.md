## Completing the square

Source: algebrica.org — CC BY-NC 4.0

## Introduction

Completing the square is a technique used to rewrite a quadratic [polynomial](../polynomials/) in a form that reveals its structural properties. Consider a polynomial of the form:

\\[
p(x) = ax^2 + bx + c, \quad a \neq 0
\\]

The objective is to determine real constants \\( h \\) and \\( k \\), which depend on \\( a \\), \\( b \\), and \\( c \\), so that \\( p(x) \\) assumes the vertex form

\\[
p(x) = a(x + h)^2 + k
\\]

The pair \\( (-h,\\, k) \\) specifies the vertex of the corresponding [parabola](../parabola/). The value \\( k \\) represents the minimum of \\( p \\) when \\( a > 0 \\) and the maximum when \\( a < 0 \\). Setting \\( p(x) \\) equal to zero yields the equation \\( a(x+h)^2 = -k \\), from which the [roots](../roots-of-a-polynomial/) can be obtained by taking square roots of both sides.

- - -

To derive explicit expressions for \\( h \\) and \\( k \\), the process begins by factoring \\( a \\) from the quadratic and linear terms:

\\[
p(x) = a\\left(x^2 + \\frac{b}{a}x\\right) + c
\\]

The crucial step is to add and subtract \\( \\left(\\dfrac{b}{2a}\\right)^{\\!2} \\) inside the parentheses, a quantity chosen so that the three terms involving \\( x \\) form a perfect square [trinomial](../trinomials/):

\\[
p(x) = a\\left(x^2 + \\frac{b}{a}x + \\left(\\frac{b}{2a}\\right)^{\\!2} - \\left(\\frac{b}{2a}\\right)^{\\!2}\\right) + c
\\]

Recognising the perfect square trinomial allows it to be rewritten in compact form:

\\[
p(x) = a\\left[\\left(x + \\frac{b}{2a}\\right)^{\\!2} - \\frac{b^2}{4a^2}\\right] + c
\\]

Distributing \\( a \\) and combining the constant terms yields:

\\[
p(x) = a\\left(x + \\frac{b}{2a}\\right)^{\\!2} - \\frac{b^2}{4a} + c
\\]

which is the vertex form with:

\\[
h = \\frac{b}{2a} \qquad k = c - \\frac{b^2}{4a}
\\]

- - -
## Geometric interpretation

The algebraic identity underlying the method of completing the square allows for a direct geometric interpretation. Consider the following expression:

\\[
x^2 + 6x + 9
\\]

Each term represents the area of a specific geometric region: \\( x^2 \\) corresponds to a square with side length \\( x \\); \\( 6x \\) represents the combined area of two rectangles, each measuring \\( x \\times 3 \\); and \\( 9 \\) denotes the area of a square with side length \\( 3 \\). When these three regions are arranged around a common vertex, they tile a larger square with side length \\( x + 3 \\), thereby confirming the identity:

\\[
x^2 + 6x + 9 = (x + 3)^2
\\]

This geometric reasoning applies precisely when the constant term equals the square of half the linear coefficient, as in a polynomial with a repeated root. Setting the expression equal to zero yields the equation \\( (x+3)^2 = 0 \\), whose unique solution is \\( x = -3 \\). In the general case, completing the square provides the necessary correction algebraically, even when the resulting configuration does not correspond to a concrete geometric realisation over the positive real numbers.

> When the coefficients are small integers and the polynomial factors readily, this geometric approach is often more straightforward than using the [quadratic formula](../quadratic-formula). Its effectiveness decreases when the leading coefficient or the linear term contains fractions or irrational numbers, as the arithmetic becomes more complex and the quadratic formula is generally preferable.

- - -
## Example 1

An application of the method can be demonstrated using the following quadratic equation:

\\[
3x^2 - 4x - 1 = 0
\\]

The constant term is moved to the right-hand side, and both sides are divided by \\( 3 \\):

\\[
x^2 - \\frac{4}{3}x = \\frac{1}{3}
\\]

The value added to both sides is the square of half the coefficient of \\( x \\), specifically:

\\[
\\left(\\frac{1}{2} \\cdot \\frac{4}{3}\\right)^{\\!2} = \\left(\\frac{2}{3}\\right)^{\\!2} = \\frac{4}{9}
\\]

\\[
x^2 - \\frac{4}{3}x + \\frac{4}{9} = \\frac{1}{3} + \\frac{4}{9}
\\]

At this stage, the left-hand side forms a perfect square trinomial:

\\[
\\left(x - \\frac{2}{3}\\right)^{\\!2} = \\frac{3}{9} + \\frac{4}{9} = \\frac{7}{9}
\\]

Taking the square root of both sides yields

\\[
x - \\frac{2}{3} = \\pm\\,\\frac{\\sqrt{7}}{3}
\\]

The equation has two real roots:

\\[
x = \\frac{2 \\pm \\sqrt{7}}{3}
\\]

> When the coefficients are not small integers, completing the square is typically more laborious than directly applying the [quadratic formula](../quadratic-formula). The latter method is generally preferable in such cases.

- - -

## Derivation of the quadratic formula

A principal application of completing the square is that it produces the [quadratic formula](../quadratic-formula/) as a direct consequence, rather than as an independent result. The derivation begins with the general quadratic equation:

\\[
ax^2 + bx + c = 0 \quad a \neq 0.
\\]

Dividing both sides by \\( a \\) and transposing the constant term to the right-hand side:

\\[
x^2 + \\frac{b}{a}x = -\\frac{c}{a}
\\]

Adding \\( \\left(\\dfrac{b}{2a}\\right)^{\\!2} \\) to both sides completes the square on the left:

\\[
x^2 + \\frac{b}{a}x + \\left(\\frac{b}{2a}\\right)^{\\!2} = \\left(\\frac{b}{2a}\\right)^{\\!2} - \\frac{c}{a}
\\]

This yields:

\\[
\\left(x + \\frac{b}{2a}\\right)^{\\!2} = \\frac{b^2 - 4ac}{4a^2}
\\]

Taking the square root of both sides and solving for \\( x \\) we obtain:

\\[
x = \\frac{-b \\pm \\sqrt{b^2 - 4ac}}{2a}
\\]

> This derivation shows that the quadratic formula is a direct consequence of completing the square applied to the general [quadratic equation](../quadratic-equations/).

- - -

The expression \\( b^2 - 4ac \\), which appears under the square root in the quadratic formula, is called the discriminant of the equation. Its sign determines the nature of the roots: 

+ When \\( b^2 - 4ac > 0 \\) the equation has two distinct real roots.
+ When \\( b^2 - 4ac = 0 \\) it has a single repeated real root.
+ When \\( b^2 - 4ac < 0 \\) there are no real roots, since the square root of a negative number is not defined in \\( \\mathbb{R} \\).