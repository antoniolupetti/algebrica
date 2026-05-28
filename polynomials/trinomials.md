---
title: Trinomials
source: https://algebrica.org/trinomials/
license: CC BY-NC 4.0
tags:
  - completing-the-square
  - discriminant
  - factoring
  - perfect-square-trinomial
  - quadratic-trinomial
  - trinomial
  - vieta-formulas
---

## Definition

A trinomial is defined as a [polynomial](../polynomials/) consisting of exactly three non-zero, pairwise distinct terms. More generally, within a commutative ring with unity, a trinomial in the indeterminate $x$ is any expression of the form:

$$ a_n x^n + a_m x^m + a_k x^k$$
$$n > m > k \geq 0$$

The coefficients $a_n, a_m, a_k$ are non-zero elements of the ring. When the underlying ring is $\mathbb{R}$, the coefficients are real numbers and the degree of the trinomial is $n$.

> A [ring](../rings/) is a set equipped with addition and multiplication satisfying the standard algebraic axioms: associativity, distributivity, and the existence of an additive identity and inverses. A commutative ring with unity additionally requires commutativity of multiplication and a multiplicative identity. Typical examples are $\mathbb{Z}$, $\mathbb{R}$, and $\mathbb{C}.$

- - -
The [quadratic trinomial](../quadratic-equations/) in one variable, which has degree two, is the most frequently studied case and takes the following canonical form where $a, b, c \in \mathbb{R}$ and $a \neq 0$:

$$ ax^2 + bx + c \tag{1}$$

The requirement $a \neq 0$ is essential because, if omitted, the leading term vanishes and the expression ceases to be quadratic. The coefficient $a$ is referred to as the leading coefficient, $b$ as the linear coefficient, and $c$ as the constant term.

Not every polynomial with three terms is of the form (1). For example, expressions such as $x^3 + 2x + 1$, $x^4 - x^2 + 3$, and $x^2 y + xy^2 - 1$ are all trinomials, each representing a distinct class. The subsequent discussion primarily addresses the quadratic case, with a dedicated section for higher-degree trinomials that can be reduced to this form through substitution.

- - -
The quadratic trinomial (1) defines the quadratic function $f(x) = ax^2 + bx + c$, whose graph is a [parabola](../parabola/). The vertex form indicates that the vertex of the parabola is located at

$$ \left( -\frac{b}{2a},  -\frac{\Delta}{4a} \right) $$

The parabola opens upward if $a > 0$ and downward if $a < 0$.

![IMG. 1](svg/trinomials-1.svg)

The number of intersections with the $x$-axis corresponds to the number of distinct real roots. The sign of $\Delta$ provides a geometric interpretation: $\Delta > 0$ indicates two $x$-intercepts, $\Delta = 0$ indicates tangency to the $x$-axis, and $\Delta < 0$ indicates no real intersection.


## Classification of trinomials

Trinomials are classified according to two primary criteria: degree and number of variables. With respect to degree, the simplest non-trivial trinomials in one variable are quadratic trinomials (degree 2). Cubic trinomials, such as $x^3 + px + q$, are significant in the theory of cubic equations, while degree-four trinomials arise in the study of biquadratic equations.

In the case of two variables, trinomials of the form $ax^2 + bxy + cy^2$ represent homogeneous quadratic forms. Homogeneous trinomials deserve a brief mention: a trinomial $ax^n + bx^{n-1}y + cy^{n-2}$ is not homogeneous unless all three terms share the same total degree. The trinomial $x^2 + xy + y^2$, for instance, is homogeneous of degree 2, while $x^2 + xy + y$ is not.


## The discriminant

The algebraic properties of the quadratic trinomial $ax^2 + bx + c$ are determined by a single quantity known as the discriminant, defined as follows:

$$ \Delta = b^2 - 4ac \tag{2} $$

The discriminant determines the nature of the [roots](../roots-of-a-polynomial/) of the quadratic equation $ax^2 + bx + c = 0$ and, consequently, the factorisation structure of the trinomial over the real numbers $\mathbb{R}$ and the complex numbers $\mathbb{C}$. Three distinct cases arise based on the value of the discriminant.

If $\Delta > 0$, the trinomial possesses two distinct real roots, $x_1$ and $x_2$, which are given by the [quadratic formula](../quadratic-formula/):

$$ x_{1,2} = \frac{-b \pm \sqrt{\Delta}}{2a} \tag{3} $$

If $\Delta = 0$, the two roots coincide, resulting in a single value $x_0 = -b/(2a)$, referred to as a repeated root or a root of multiplicity two.

If $\Delta < 0$, the trinomial has no real roots and is irreducible over $\mathbb{R}$, as it cannot be expressed as a product of two linear factors with real coefficients. However, over the [complex numbers](../complex-numbers-introduction/) $\mathbb{C}$, formula (3) remains valid, with $\sqrt{\Delta}$ interpreted as $i\sqrt{|\Delta|}$, resulting in a conjugate pair of [complex roots](../quadratic-equations-with-complex-solutions/).

- - -
If $\Delta \geq 0$, the trinomial in equation (1) can be completely factorised over the real numbers:

$$ ax^2 + bx + c = a(x - x_1)(x - x_2) \tag{4} $$

$x_1$ and $x_2$ denote the roots specified in equation (3). In the case of a repeated root, this factorisation simplifies to

$$ ax^2 + bx + c = a(x - x_0)^2 $$

The factorisation in equation (4) represents the product form of the trinomial. This form is fundamental for simplifying rational expressions, solving inequalities, and evaluating [limits](../limits/) and [integrals](../definite-integrals/) that involve quadratic denominators.


## Vieta's formulas

An immediate consequence of equation (4) is that the roots satisfy the following relations, known as [Vieta's formulas](../vieta-formulas/):

$$
\begin{align}
x_1 + x_2 &= -\frac{b}{a} \\[6pt]
x_1 x_2 &= \frac{c}{a}
\end{align}
\tag{5}
$$

These identities are derived by expanding $a(x-x_1)(x-x_2)$ and equating coefficients with $ax^2 + bx + c$. Vieta's formulas are particularly useful because they enable verification of a factorisation without explicitly computing the roots and underpin several factorisation techniques, including the [AC method](../factoring-ac-method/) for trinomials with integer coefficients. For example, to factor $x^2 - 5x + 6$, it is necessary to identify two numbers whose sum is 5 and whose product is 6. We can use this simple scheme to find the numbers that satisfy our constraints.

$$
\begin{array}{rrrr}
m & n & P & S \\ \hline
1 & 6 & 6 & 7 \\
-1 & -6 & 6 & -7 \\
2 & 3 & 6 & 5 \\
-2 & -3 & 6 & -5 \\
\end{array}
$$

The pair $(2, 3)$ in row 3 satisfies both conditions, thus:

$$ x^2 - 5x + 6 = (x - 2)(x - 3) $$

> This mental arithmetic approach is effective whenever the roots are rational.


## Example 1

Factor the trinomial $3x^2 - 7x + 2$. The first step is to compute the discriminant: $\Delta = (-7)^2 - 4 \cdot 3 \cdot 2 = 49 - 24 = 25 > 0$. Since $\Delta > 0$, the trinomial has two distinct real roots, which can be determined using the quadratic formula:

$$ x_{1,2} = \frac{7 \pm \sqrt{25}}{6} = \frac{7 \pm 5}{6} $$

This calculation yields $x_1 = 12/6 = 2$ and $x_2 = 2/6 = 1/3$. The factorisation over $\mathbb{R}$ is therefore

$$
\begin{align}
3x^2 - 7x + 2 &= 3\left(x - 2\right)\left(x - \tfrac{1}{3}\right) \\[6pt]
               &= (x-2)(3x-1)
\end{align}
$$

As a consistency check, Vieta's formulas (5) require that $x_1 + x_2 = -b/a$ and $x_1 x_2 = c/a$. Indeed, $x_1 + x_2 = 2 + 1/3 = 7/3$ and $x_1 x_2 = 2 \cdot 1/3 = 2/3$, both in agreement with $-b/a = 7/3$ and $c/a = 2/3$.

The factorisation therefore yields:
$$(x-2)(3x-1)$$


## Perfect square trinomials

A trinomial is defined as a perfect square if it can be expressed as the square of a binomial. The two fundamental identities, treated more broadly among the [notable products](../notable-products/), are as follows:

$$(a + b)^2 = a^2 + 2ab + b^2$$

$$(a - b)^2 = a^2 - 2ab + b^2$$

To identify a perfect square trinomial, three conditions must be verified simultaneously: the first and last terms must be perfect squares (such as $a^2$ and $b^2$), and the middle term must be exactly $\pm 2ab$. If any of these conditions is not satisfied, the trinomial is not a perfect square.

For instance, $9x^2 - 12x + 4$ satisfies all conditions: $9x^2 = (3x)^2$, $4 = 2^2$, and $12x = 2 \cdot 3x \cdot 2$. Therefore

$$ 9x^2 - 12x + 4 = (3x - 2)^2 $$

A frequent mistake is to assume that $x^2 + 4x + 8$ is a perfect square solely because the first term is a perfect square. This is incorrect, as $8 \neq (2)^2 = 4$. Calculating the discriminant confirms this: $\Delta = 16 - 32 = -16 < 0$ indicating that the trinomial is irreducible over $\mathbb{R}$.

A perfect square trinomial always has a discriminant $\Delta = 0$, as its two roots are identical. Conversely, any quadratic trinomial with $\Delta = 0$ is a perfect square.

- - -
For example, determine whether $4x^2 - 12x + 9$ is a perfect square and factor it. To verify, note that $4x^2 = (2x)^2$, $9 = 3^2$, and $12x = 2 \cdot 2x \cdot 3$. Since all three conditions are satisfied we have:

$$ 4x^2 - 12x + 9 = (2x - 3)^2 $$

The discriminant $\Delta = 144 - 144 = 0$ confirms the presence of a repeated root at $x_0 = 3/2$.


## Example 2

Determine whether the polynomial $x^2 + x + 1$ is reducible over $\mathbb{R}$, and identify its complex roots. The discriminant is $\Delta = 1 - 4 = -3 < 0$. Because $\Delta < 0$, the polynomial has no real roots and is irreducible over $\mathbb{R}$. It cannot be expressed as a product of two linear factors with real coefficients.

Over $\mathbb{C}$, the quadratic formula applies with $\sqrt{\Delta} = i\sqrt{3}$, resulting in a pair of complex conjugate roots:

$$ x_{1,2} = \frac{-1 \pm i\sqrt{3}}{2} $$

These roots are primitive sixth roots of unity, as they satisfy $x^6 = 1$ but $x^k \neq 1$ for $k = 1, 2, 3, 4, 5$. The factorisation over $\mathbb{C}[x]$ is therefore given by

$$ x^2 + x + 1 = \left(x - \frac{-1 + i\sqrt{3}}{2}\right)\left(x - \frac{-1 - i\sqrt{3}}{2}\right) $$

Thus, the trinomial is irreducible over $\mathbb{R}$, and its two complex roots are:
$$x_1 = \dfrac{-1 + i\sqrt{3}}{2} \quad x_2 = \dfrac{-1 - i\sqrt{3}}{2}$$


## The method of completing the square

[Completing the square](https://algebrica.org/completing-the-square/) is a technique used to rewrite any quadratic trinomial of the form $ax^2 + bx + c$ as an equivalent expression:

 $$a(x - h)^2 + k$$

$h$ and $k$ are constants determined by the original coefficients. This form allows for direct identification of the vertex of the corresponding [parabola](../parabola/) and serves as a fundamental step in deriving the quadratic formula. For a comprehensive discussion, refer to the dedicated page on completing the square.


## Trinomials reducible to quadratic form

Certain higher-degree trinomials may be reduced to quadratic form through an appropriate change of variable. Specifically, a trinomial of the form:

$$ ax^{2n} + bx^n + c $$

$n \geq 2$ is a positive [integer](../integers/), becomes quadratic when the substitution $t = x^n$ is applied:

$$ at^2 + bt + c $$

The roots $t_1, t_2$ of the resulting quadratic equation correspond to the roots of the original trinomial, which are obtained by solving $x^n = t_i$ for each $i$. The number and type of solutions depend on the value of $n$ and the sign of each $t_i$. When $n = 2$, the trinomial is referred to as a biquadratic trinomial. For example, consider

$$ x^4 - 5x^2 + 4 $$

Applying the substitution $t = x^2$ results in:

$$t^2 - 5t + 4 = (t-1)(t-4)$$

So $t = 1$ or $t = 4.$

Reverting to the original variable, $x^2 = 1$ yields $x = \pm 1$, and $x^2 = 4$ yields $x = \pm 2$. Thus, the complete factorisation over $\mathbb{R}$ is:

$$ x^4 - 5x^2 + 4 = (x-1)(x+1)(x-2)(x+2) $$

If any value $t_i$ is negative and $n$ is even, the equation $x^n = t_i$ admits no real solutions. In this case, the corresponding factor is irreducible over $\mathbb{R}$ but splits over $\mathbb{C}$.

The trinomial $x^4 + x^2 + 1$ serves as a less straightforward example. Substituting $t = x^2$ yields $t^2 + t + 1$, which has discriminant $\Delta = 1 - 4 = -3 < 0$ and is therefore irreducible over $\mathbb{R}$. However, the original trinomial can be factored over $\mathbb{R}$ by alternative methods, as shown below:

$$
\begin{align}
x^4 + x^2 + 1 &= (x^4 + 2x^2 + 1) - x^2 \\[6pt]
               &= (x^2+1)^2 - x^2 \\[6pt]
               &= (x^2 + x + 1)(x^2 - x + 1)
\end{align}
$$

Each factor is a quadratic trinomial with a negative discriminant, so the factorisation cannot be further refined over $\mathbb{R}$.


## Irreducibility and complex roots

A quadratic trinomial $ax^2 + bx + c$ with $\Delta < 0$ cannot be decomposed into linear factors over $\mathbb{R}$. Over $\mathbb{C}$, every quadratic polynomial can be factored completely. The roots form a conjugate pair:

$$ x_{1,2} = \frac{-b \pm i\sqrt{|\Delta|}}{2a} $$

The corresponding factorisation is $a(x - x_1)(x - x_2)$, which holds in $\mathbb{C}[x]$. This result follows from the [Fundamental Theorem of Algebra](../roots-of-a-polynomial/), which states that every non-constant polynomial over $\mathbb{C}$ can be factored completely into linear factors.

> This irreducibility constitutes a property with significant implications in real analysis and integration theory. Specifically, integrals involving an irreducible quadratic in the denominator necessitate completing the square and substitution, rather than employing partial fractions with real linear factors.
