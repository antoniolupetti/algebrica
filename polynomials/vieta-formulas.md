---
title: Vieta's Formulas
source: https://algebrica.org/vieta-formulas/
license: CC BY-NC 4.0
tags:
  - elementary-symmetric-polynomials
  - polynomial
  - polynomial-roots
  - symmetric-polynomials
  - vieta-formulas
---

## Introduction and formulas

Recall that a [polynomial equation](../polynomial-equations/) in one variable has the form $P(x) = 0,$ where $P(x)$ is a [polynomial](../polynomials/). Its standard form is:

$$\tag{1}
a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0 = 0
$$

The coefficients $a_0, a_1, \ldots, a_n$ may be real or [complex numbers](../complex-numbers/), and $n$ is the degree of the equation. The condition $a_n \neq 0$ is required for $(1)$ to have degree $n.$ For example, a [quadratic equation](../quadratic-equations/) is a polynomial equation of degree $n=2,$ with $a \neq 0$ and standard form:

$$ax^2 + bx + c = 0 \tag{2}$$

For equations of the form $(1)$ or $(2),$ the identities that explicitly relate the [roots](../roots-of-a-polynomial/) to the coefficients of the polynomial are known as Vieta's formulas. These formulas can be viewed in two equivalent ways. They express the sum and product of the roots in terms of the coefficients to help solve an equation, and they describe how to determine the coefficients of a polynomial once its roots are known.

- - -

Consider a general quadratic equation in the standard form $(2).$ Denoting its two roots by $x_1$ and $x_2,$ we can factor the polynomial as follows:

$$a(x - x_1)(x - x_2) \tag{3}$$

[Expanding the product](../multiplying-polynomials/) gives:

$$
ax^2 - a(x_1 + x_2)x + ax_1 x_2
$$

Comparing coefficients with $(2),$ we obtain $-a(x_1 + x_2) = b$ and $ax_1x_2 = c.$ Since $a \neq 0,$ we can divide by $a$ to obtain Vieta's formulas for quadratic equations:

$$\tag{4}
\begin{align}
x_1 + x_2 &= -\frac{b}{a} \\[6pt]
x_1 x_2 &= \frac{c}{a}
\end{align}
$$

These identities express the relationships between the roots and the coefficients. They hold for every value of the discriminant, including the case of [complex conjugate roots](../quadratic-equations-with-complex-solutions/).

- - -

An alternative derivation of $(4)$ uses the [quadratic formula](../quadratic-formula/), which gives the two roots as follows:

$$
x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

Recalling that $\Delta = b^2 - 4ac,$ we add $x_1$ and $x_2$ to obtain the first identity in $(4)$:

$$
\begin{align}
x_1 + x_2 &= \frac{-b + \sqrt{\Delta} - b - \sqrt{\Delta}}{2a} \\[6pt]
&= \frac{-2b}{2a} \\[6pt]
&= -\frac{b}{a}
\end{align}
$$

To compute the product, we apply the [difference-of-squares identity](../notable-products/) $(u + v)(u - v) = u^2 - v^2$ to the numerator and substitute the expression for the discriminant. This gives the second identity in $(4)$:

$$
\begin{align}
x_1 x_2 &= \frac{(-b + \sqrt{\Delta})(-b - \sqrt{\Delta})}{4a^2} \\[6pt]
&= \frac{b^2 - \Delta}{4a^2} \\[6pt]
&= \frac{b^2 - (b^2 - 4ac)}{4a^2} \\[6pt]
&= \frac{c}{a}
\end{align}
$$

## General form

The formulas in $(4)$ extend to any polynomial $P(x)$ of degree $n$ written in the form:

$$ \tag{5}
P(x) = a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0
$$

By the [fundamental theorem of algebra](../roots-of-a-polynomial/), the polynomial in $(5)$ has $n$ roots in $\mathbb{C},$ counted with multiplicity. Denoting them by $x_1, x_2, \ldots, x_n,$ we can factor it as in the quadratic case in $(3)$:

$$
P(x) = a_n (x - x_1)(x - x_2) \cdots (x - x_n)
$$

To expand the product, recall that a term in $x^{n-k}$ is obtained by choosing $-x_i$ from $k$ factors and $x$ from the remaining $n-k$ factors. The coefficient of $x^{n-k}$ is therefore the sum of all products of $k$ roots with distinct indices, multiplied by $a_n(-1)^k.$ We can write this sum as follows:

$$ \tag{6}
e_k(x_1, \ldots, x_n) = \sum_{1 \le i_1 < i_2 < \cdots < i_k \le n} x_{i_1} x_{i_2} \cdots x_{i_k}
$$

The expression $e_k$ is called an elementary symmetric polynomial. Comparing the coefficient of $x^{n-k}$ in the expansion with that in $(5),$ we obtain $a_{n-k} = a_n(-1)^k e_k.$ Since $a_n \neq 0,$ we can divide by $a_n$ to obtain Vieta's formulas in their general form:

$$
\frac{a_{n-k}}{a_n} = (-1)^k e_k(x_1, \ldots, x_n), \qquad k = 1, 2, \ldots, n
$$

For $k = 1,$ each product in $(6)$ contains just one root, so $e_1 = x_1 + \cdots + x_n.$ This gives Vieta's formula for the sum of the roots of a polynomial of degree $n,$ generalising the first identity in $(4)$:

$$ \tag{7}
x_1 + x_2 + \cdots + x_n = -\frac{a_{n-1}}{a_n}
$$

The second identity in $(4)$ is generalised by setting $k = n$:

$$ \tag{8}
x_1 x_2 \cdots x_n = (-1)^n\frac{a_0}{a_n}
$$

In the quadratic case, $n = 2$ and the coefficients are $a_2 = a,$ $a_1 = b$ and $a_0 = c.$ Since $e_1 = x_1 + x_2$ and $e_2 = x_1 x_2,$ applying the general formula with $k = 1$ and $k = 2$ recovers exactly the identities in $(4)$:

$$
\begin{align}
x_1 + x_2 &= -\frac{a_1}{a_2} = -\frac{b}{a} \\[6pt]
x_1 x_2 &= (-1)^2 \frac{a_0}{a_2} = \frac{c}{a}
\end{align}
$$
- - -

As a particular case, we apply the general formula to degree three. Consider a cubic equation in standard form:

$$
ax^3 + bx^2 + cx + d = 0
$$

As in the quadratic case, we denote the roots by $x_1,$ $x_2$ and $x_3.$ Vieta's formulas then give the following identities:

$$
\begin{align}
x_1 + x_2 + x_3 &= -\frac{b}{a} \\[6pt]
x_1 x_2 + x_1 x_3 + x_2 x_3 &= \frac{c}{a} \\[6pt]
x_1 x_2 x_3 &= -\frac{d}{a}
\end{align}
$$

## Examples

To apply the formulas introduced so far, consider the quadratic equation:

$$
x^2 - 5x + 6 = 0
$$

The coefficients are $a = 1,$ $b = -5$ and $c = 6,$ so the roots must have sum $5$ and product $6.$ To find them, we follow the method described in the discussion of [factoring quadratic equations](../factoring-quadratic-equations/) and seek a factorisation of the form $(x + r)(x + s).$ In this notation, $r = -x_1$ and $s = -x_2,$ since each root makes the corresponding factor zero. Expanding the product gives $x^2 + (r + s)x + rs.$ Comparing coefficients therefore yields the conditions:

$$
\begin{align}
rs &= \frac{c}{a} = 6 \\[6pt]
r + s &= \frac{b}{a} = -5
\end{align}
$$

The table lists all pairs of integers whose product is $6,$ omitting pairs that differ only in order. In the last column, we calculate the sum to see which pair also satisfies the second condition:

$$
\begin{array}{c|c|c|c}
r & s & rs & r+s \\[6pt]
\hline
1 & 6 & 6 & 7 \\[6pt]
2 & 3 & 6 & 5 \\[6pt]
-1 & -6 & 6 & -7 \\[6pt]
-2 & -3 & 6 & -5
\end{array}
$$

Only the last row satisfies both conditions. Setting $r = -2$ and $s = -3,$ we obtain the factorisation:

$$
x^2 - 5x + 6 = (x - 2)(x - 3)
$$

By the zero-product property, the equation holds when $x - 2 = 0$ or $x - 3 = 0.$ The roots are therefore $x_1 = -r = 2$ and $x_2 = -s = 3.$

- - -

Next, consider the cubic equation:

$$
x^3 - 6x^2 + 11x - 6 = 0 \tag{9}
$$

Suppose we have identified $1,$ $2$ and $3$ as possible roots. We evaluate the polynomials $e_i$ at these values:

$$
\begin{align}
e_1 &= 1 + 2 + 3 = 6 \\[6pt]
e_2 &= 1 \cdot 2 + 1 \cdot 3 + 2 \cdot 3 = 11 \\[6pt]
e_3 &= 1 \cdot 2 \cdot 3 = 6
\end{align}
$$

Vieta's formulas become $-b = e_1,$ $c = e_2$ and $-d = e_3.$ Substituting the coefficients of the equation gives $-(-6) = 6,$ $11 = 11$ and $-(-6) = 6,$ so all three equalities hold. We can therefore factor the polynomial in $(9)$ as follows:

$$
x^3 - 6x^2 + 11x - 6 = (x - 1)(x - 2)(x - 3)
$$

Again, the zero-product property shows that the roots of the equation are $1,$ $2$ and $3.$

- - -

For a final example, we consider a leading coefficient other than $1.$ Take the quadratic equation:

$$
2x^2 - 8x + 6 = 0
$$

Applying the formulas in $(4)$ gives:

$$
\begin{align}
x_1 + x_2 &= -\frac{-8}{2} = 4 \\[6pt]
x_1 x_2 &= \frac{6}{2} = 3
\end{align}
$$

We therefore seek two numbers with product $3$ and sum $4.$ We can use a table like the one in the first example, this time listing the possible roots directly in the columns $x_1$ and $x_2$:

$$
\begin{array}{c|c|c|c}
x_1 & x_2 & x_1x_2 & x_1+x_2 \\[6pt]
\hline
1 & 3 & 3 & 4 \\[6pt]
-1 & -3 & 3 & -4
\end{array}
$$

Only the first row also has sum $4,$ so the required numbers are $1$ and $3.$ Since we must retain the leading coefficient $a = 2$ in the factorisation, we write:

$$
2x^2 - 8x + 6 = 2(x - 1)(x - 3)
$$

The zero-product property again gives the roots of the equation as $x_1 = 1$ and $x_2 = 3.$

## Constructing a polynomial

As noted in the introduction, Vieta's formulas can also be used in the opposite direction to construct a polynomial $P(x)$ from its roots. If the roots are $\alpha_1, \alpha_2, \ldots, \alpha_n,$ the monic polynomial, that is, the one with leading coefficient $1,$ is given by:

$$\tag{10}
P(x) = x^n - e_1 x^{n-1} + e_2 x^{n-2} - \cdots + (-1)^n e_n
$$

For example, we seek the monic cubic polynomial whose roots are $2,$ $-1$ and $3.$ Setting $n = 3,$ the formula becomes:

$$
P(x) = x^3 - e_1 x^2 + e_2 x - e_3
$$

To determine its coefficients, we need to calculate $e_1,$ the sum of the roots, $e_2,$ the sum of their pairwise products, and $e_3,$ the product of all three roots. This gives the following equalities:

$$
\begin{align}
e_1 &= 2 + (-1) + 3 = 4 \\[6pt]
e_2 &= 2 \cdot (-1) + 2 \cdot 3 + (-1) \cdot 3 = 1 \\[6pt]
e_3 &= 2 \cdot (-1) \cdot 3 = -6
\end{align}
$$

Applying $(10),$ the required polynomial is therefore:

$$
P(x) = x^3 - 4x^2 + x + 6
$$
