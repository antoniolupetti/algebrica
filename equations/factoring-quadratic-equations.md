---
title: Factoring Quadratic Equations
source: https://algebrica.org/factoring-quadratic-equations/
license: CC BY-NC 4.0
tags:
  - ac-method
  - discriminant
  - factoring
  - quadratic-equation
  - vieta-formulas
---
## Derivation

A [quadratic equation](../quadratic-equations/) in standard form is written as:

$$ax^{2} + bx + c = 0, \qquad a \neq 0$$

Factoring the equation means rewriting the left-hand side as a product of linear factors with the same roots. When the [discriminant](../quadratic-formula/) $\Delta = b^2 - 4ac$ is non-negative, the equation admits two [real roots](../roots-of-a-polynomial/) $x_1$ and $x_2$, and the following identity holds:

$$ax^{2} + bx + c = a(x - x_1)(x - x_2) \tag{1}$$

The roots coincide when $\Delta = 0$, in which case the factorization reduces to $a(x - x_0)^2$. When $\Delta < 0$ the polynomial is irreducible over $\mathbb{R}$ and admits a factorization only over $\mathbb{C}$, where the two roots are [complex conjugates](../quadratic-equations-with-complex-solutions/).

- - -

Consider the quadratic [polynomial](../polynomials/) associated with the equation:

$$P(x) = ax^2 + bx + c$$

Since $a \neq 0$, the leading coefficient can be factored out:

$$P(x) = a\left(x^2 + \frac{b}{a}x + \frac{c}{a}\right)$$

The coefficients of the monic polynomial inside the parentheses are linked to the roots through [Vieta's formulas](../quadratic-formula/):

$$x_1 + x_2 = -\frac{b}{a}, \qquad x_1x_2 = \frac{c}{a}$$

Substituting these expressions into the polynomial gives:

$$
\begin{align}
P(x) &= a\left[x^2 - (x_1 + x_2)x + x_1x_2\right] \\[6pt]
&= a\left(x^2 - x_1x - x_2x + x_1x_2\right) \\[6pt]
&= a\left[x(x - x_1) - x_2(x - x_1)\right] \\[6pt]
&= a(x - x_1)(x - x_2)
\end{align}
$$

This establishes identity $(1)$. The roots of the equation are recovered by setting each linear factor equal to zero:

$$x - x_1 = 0 \implies x = x_1$$
$$x - x_2 = 0 \implies x = x_2$$

> The factorization above is exact and follows directly from the values of the roots. When the roots are not known in advance, they are obtained from the [quadratic formula](../quadratic-formula/) and substituted into $(1)$. An alternative approach, useful when the coefficients are integers and the roots are rational, is the [AC method](../factoring-polynomials-ac-method/), which factors the polynomial without computing the discriminant explicitly.

## Example 1

Consider a polynomial with integer roots:

$$x^{2} - 4x + 3$$

Here $a = 1$, so identity $(1)$ reduces to $(x - x_1)(x - x_2)$. The roots can be found by inspection, looking for two numbers whose sum is $4$ and whose product is $3$. The pair $(1, 3)$ satisfies both conditions, and the factorization is:

$$x^{2} - 4x + 3 = (x - 1)(x - 3)$$

The associated equation has solutions $x_1 = 1$ and $x_2 = 3$.

## Example 2

Consider a polynomial whose leading coefficient is different from one:

$$2x^{2} - 7x + 3$$

The discriminant is $\Delta = 49 - 24 = 25$, so the roots are real and distinct. Applying the quadratic formula gives:

$$x = \frac{7 \pm 5}{4}$$

which yields $x_1 = 3$ and $x_2 = \frac{1}{2}$. Substituting these values into identity $(1)$ with $a = 2$:

$$2x^{2} - 7x + 3 = 2(x - 3)\left(x - \tfrac{1}{2}\right) = (x - 3)(2x - 1)$$

> The factor $2$ has been absorbed into the second linear term to produce a factorization with integer coefficients.

## Example 3

Consider a polynomial whose discriminant vanishes, so that the two roots coincide:

$$x^{2} - 6x + 9$$

The [discriminant](../quadratic-formula/) is $\Delta = 36 - 36 = 0$, and the unique root is $x_0 = 3$. The factorization is:

$$x^{2} - 6x + 9 = (x - 3)^{2}$$

This is consistent with identity $(1)$, where $x_1 = x_2 = x_0$.

## Example 4

Consider a polynomial whose discriminant is negative, so that the polynomial is irreducible over $\mathbb{R}$:

$$x^{2} + 2x + 5$$

The discriminant is $\Delta = 4 - 20 = -16$, and the roots are the complex conjugate pair $x_{1,2} = -1 \pm 2i$. The factorization holds only over $\mathbb{C}$:

$$x^{2} + 2x + 5 = (x + 1 - 2i)(x + 1 + 2i)$$

A complete discussion of this case is given in the entry on [quadratic equations with complex solutions](../quadratic-equations-with-complex-solutions/).