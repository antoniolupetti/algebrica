---
title: Polynomial Inequalities
source: https://algebrica.org/polynomial-inequalities/
license: CC BY-NC 4.0
tags:
  - factoring
  - polynomial-inequalities
  - roots
  - sign-chart
---

## Definition

A polynomial inequality is an inequality in which one side consists of a [polynomial](../polynomials/) expression and the other is zero. The general form is one of the following:

$$
\begin{align}
P(x) > 0 \qquad & P(x) \geq 0 \\[6pt]
P(x) < 0 \qquad & P(x) \leq 0
\end{align}
$$

In each case $P(x)$ is a polynomial of the form:

$$P(x) = a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0$$

The integer $n$ is the degree of the inequality, the coefficients $a_0, a_1, \ldots, a_n$ are real numbers, and the leading coefficient $a_n$ is assumed to be nonzero. Polynomial inequalities of degree one and two are treated separately in the entries on [linear inequalities](../linear-inequalities/) and [quadratic inequalities](../quadratic-inequalities/). The present discussion concerns the general case, with particular attention to degrees greater than two.

## Reduction to canonical form

Polynomial inequalities are not always presented with zero on the right-hand side. Any inequality between two polynomials can be brought to this form by moving every term to one side. The inequality:

$$2x^3 + x > x^2 + 6$$

is rewritten as $2x^3 - x^2 + x - 6 > 0$ before the resolution begins. This step is essential, because the standard method relies on studying the sign of a single polynomial, not on comparing two separate expressions.

## Resolution by factorisation

The key observation is that a polynomial $P(x)$ with real coefficients can change sign only at its real [roots](../roots-of-a-polynomial/). Between two consecutive real roots the polynomial keeps a constant sign, since it is a [continuous function](../continuous-functions/) that does not vanish on the open interval between them. The resolution of a polynomial inequality therefore proceeds in three steps.

+ The first step is to determine the real roots of $P(x)$ by solving the associated [polynomial equation](../polynomial-equations/) $P(x) = 0$, possibly by [factorisation](../factoring-polynomials-ac-method/), by the [rational root theorem](../polynomial-equations/), or by [polynomial division](../polynomial-division/).
+ The second step is to factor $P(x)$ as a product of linear and irreducible quadratic factors, exhibiting each real root as the zero of a linear factor and grouping every pair of complex conjugate roots into a single quadratic factor that keeps a constant sign throughout $\mathbb{R}$.
+ The third step is to construct a [sign chart](../sign-analysis-in-inequalities/) recording the sign of each factor on every interval determined by the real roots, and to combine the signs by the standard rule that the product of factors with the same sign is positive and the product of factors with opposite signs is negative.

The intervals where the sign of the product matches the direction of the inequality, together with the roots themselves when the inequality is non-strict, form the solution set.

> A useful check on the completed chart comes from the behaviour of the polynomial for large values of $|x|$. On the rightmost interval the sign of $P(x)$ coincides with the sign of the leading coefficient $a_n$. On the leftmost interval it coincides with the sign of $a_n$ when the degree is even, and with the opposite sign when the degree is odd.

## Multiplicity and sign changes

The [multiplicity](../roots-of-a-polynomial/) of each real root determines whether the polynomial changes sign at that root. A root of odd multiplicity is a point where the polynomial changes sign, since the corresponding linear factor appears an odd number of times and contributes an odd power that changes sign in a neighbourhood of the root. A root of even multiplicity is a point where the polynomial does not change sign, since the corresponding factor appears an even number of times and contributes an even power that keeps the same sign on both sides of the root.

This distinction must be taken into account when constructing the sign chart. Treating every real root as a sign-change point produces incorrect solution [sets](../sets/) when repeated factors are present.

> A typical situation arises when the polynomial contains a factor of the form $(x - x_0)^2$. The polynomial vanishes at $x = x_0$, but the sign on the two sides of $x_0$ is the same. The point $x_0$ may belong to the solution set only when the inequality is non-strict, in which case it appears as an isolated point of the solution.

## Irreducible quadratic factors

When the polynomial $P(x)$ has degree greater than two, it may contain irreducible quadratic factors corresponding to pairs of [complex conjugate roots](../quadratic-equations-with-complex-solutions/). An irreducible quadratic factor $ax^2 + bx + c$ with discriminant $\Delta = b^2 - 4ac < 0$ keeps the sign of its leading coefficient $a$ throughout $\mathbb{R}$, since the corresponding parabola does not meet the horizontal axis.

This observation simplifies the sign chart, since an irreducible quadratic factor contributes a constant sign on every interval, equal to the sign of $a$, and therefore plays the role of a constant factor in the overall product. The intervals of the sign chart are determined only by the real roots of $P(x)$, not by the roots of the irreducible factors.

In the extreme case where $P(x)$ has no real roots, the factorisation contains only irreducible quadratic factors and the polynomial keeps a constant sign on the whole real line. The solution set is then either $\mathbb{R}$ or the empty set, depending on whether that constant sign agrees with the direction of the inequality. The inequality $x^4 + 1 > 0$, for instance, is satisfied by every real number, while $x^4 + 1 < 0$ has no solution.

> This situation can occur only when the degree of $P(x)$ is even, because every polynomial of odd degree with real coefficients has at least one real root.

## Example 1

Determine the values of $x$ that satisfy the following inequality.

$$x^3 - 4x^2 + x + 6 \geq 0$$

The associated polynomial equation $x^3 - 4x^2 + x + 6 = 0$ has integer coefficients and leading coefficient equal to $1$, so the [rational root theorem](../polynomial-equations/) restricts the candidate rational roots to the integer divisors of the constant term $6$, that is $\pm 1, \pm 2, \pm 3, \pm 6$. Substituting $x = -1$ gives:

$$(-1)^3 - 4(-1)^2 + (-1) + 6 = -1 - 4 - 1 + 6 = 0$$

so $x = -1$ is a root and the factor $(x + 1)$ divides the polynomial. Performing the [polynomial division](../polynomial-division/) yields the following factorisation.

$$x^3 - 4x^2 + x + 6 = (x + 1)(x^2 - 5x + 6)$$

The residual quadratic factors as $(x - 2)(x - 3)$, giving the complete factorisation.

$$x^3 - 4x^2 + x + 6 = (x + 1)(x - 2)(x - 3)$$

The three real roots are $x = -1$, $x = 2$, and $x = 3$, all of multiplicity one. They partition the real line into four intervals. The sign chart records the sign of each factor on every interval and the sign of the product.

[class="table-sign"]

|                     |                  |      $$-1$$      |      $$2$$       |      $$3$$       |
| :------------------ | :--------------: | :--------------: | :--------------: | :--------------: |
| $$x + 1$$           | $\boldsymbol{-}$ | $\boldsymbol{+}$ | $\boldsymbol{+}$ | $\boldsymbol{+}$ |
| $$x - 2$$           | $\boldsymbol{-}$ | $\boldsymbol{-}$ | $\boldsymbol{+}$ | $\boldsymbol{+}$ |
| $$x - 3$$           | $\boldsymbol{-}$ | $\boldsymbol{-}$ | $\boldsymbol{-}$ | $\boldsymbol{+}$ |
| $$(x+1)(x-2)(x-3)$$ | $\boldsymbol{-}$ | $\boldsymbol{+}$ | $\boldsymbol{-}$ | $\boldsymbol{+}$ |
[/class]

The polynomial is non-negative on the intervals $[-1, 2]$ and $[3, +\infty)$. Since the inequality is non-strict, the roots are included in the solution set. The complete solution is the following.

$$[-1, 2] \cup [3, +\infty)$$

## Example 2

Determine the values of $x$ that satisfy the following inequality.

$$(x - 1)^2 (x + 2) < 0$$

The polynomial is already in factored form. The real roots are $x = 1$, with multiplicity two, and $x = -2$, with multiplicity one. The factor $(x - 1)^2$ is non-negative for every real $x$ and vanishes only at $x = 1$, so it does not change sign as $x$ crosses $x = 1$. The sign of the product is therefore determined solely by the sign of $(x + 2)$, except at the point $x = 1$ where the product vanishes.

The expression $(x + 2)$ is negative when $x < -2$ and positive when $x > -2$. The product is therefore negative on $(-\infty, -2)$ and positive on $(-2, 1) \cup (1, +\infty)$, with zeros at $x = -2$ and $x = 1$. Since the inequality is strict, neither zero belongs to the solution set. The solution is the following.

$$(-\infty, -2)$$

> The root $x = 1$ does not contribute an isolated point to the solution set, because the inequality is strict and the polynomial vanishes there. The even multiplicity prevents the polynomial from becoming negative in a neighbourhood of $x = 1$, so this region is excluded.

## Example 3

Determine the values of $x$ that satisfy the following inequality.

$$x^4 + x^2 - 6 \geq 0$$

This is a [trinomial inequality](../trinomial-inequalities/) of degree four, since the polynomial contains only terms of degree $4$, $2$, and $0$. Setting $y = x^2$ transforms the associated equation into a quadratic in $y$.

$$y^2 + y - 6 = 0 \quad \rightarrow \quad (y - 2)(y + 3) = 0$$

The two values are $y_1 = 2$ and $y_2 = -3$. Reversing the substitution $y = x^2$ produces two equations of the form $x^2 = y_i$. For $y_1 = 2$ we obtain $x = \pm\sqrt{2}$, while for $y_2 = -3$ no real solution exists, since $x^2 \geq 0$ for every real $x$. The polynomial therefore factors as follows.

$$x^4 + x^2 - 6 = (x^2 - 2)(x^2 + 3)$$

The second factor is an irreducible quadratic with positive leading coefficient and is strictly positive for every real $x$. The sign of the polynomial is governed entirely by the first factor $x^2 - 2$, which is non-negative when $x \leq -\sqrt{2}$ or $x \geq \sqrt{2}$. The solution is the following.

$$(-\infty, -\sqrt{2}] \cup [\sqrt{2}, +\infty)$$
