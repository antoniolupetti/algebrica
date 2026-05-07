# Vieta's Formulas

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/vieta-formulas/

## Introduction

Given a [polynomial equation](../polynomial-equations/) with assigned roots, the coefficients are not free parameters and are determined, up to a multiplicative constant, by the roots themselves. The identities that explicitly relate the roots to the coefficients are known as Vieta’s formulas. They provide one of the simplest examples of how symmetric relationships between the roots are reflected in the coefficients of a [polynomial](../polynomials/).

The formulas can be stated in two equivalent ways. 

+ From the perspective of solving an equation, they give the sum, the product, and a hierarchy of intermediate symmetric expressions of the roots, all in terms of the coefficients. 
+ From the perspective of constructing a polynomial, they describe how to assemble the coefficients once the roots are fixed.

- - -
## Quadratic case

Consider the [quadratic equation](../quadratic-equations/) in standard form:

\\[
ax^2 + bx + c = 0, \qquad a \neq 0
\\]

If \\(x_1\\) and \\(x_2\\) denote its two roots in \\(\mathbb{C}\\), counted with multiplicity, the polynomial admits the factorisation \\(a(x - x_1)(x - x_2)\\). Expanding the product gives:

\\[
a(x - x_1)(x - x_2) = ax^2 - a(x_1 + x_2)\\,x + a\\,x_1 x_2
\\]

Equating the coefficients of \\(x^2\\), \\(x\\), and the constant term with those of \\(ax^2 + bx + c\\) yields Vieta's formulas in the quadratic case:

\\[
x_1 + x_2 = -\frac{b}{a}, \qquad x_1 x_2 = \frac{c}{a}
\\]

These two identities encode all the information about the roots that can be read directly from the coefficients without solving the equation. They hold for every value of the [discriminant](../quadratic-formula/), including the case in which the roots form a pair of complex conjugates.

> The same identities can be derived from the [quadratic formula](../quadratic-formula/) by computing the sum and the product of the two expressions \\(\frac{-b + \sqrt{\Delta}}{2a}\\) and \\(\frac{-b - \sqrt{\Delta}}{2a}\\). The argument by factorisation is shorter and generalises to higher degrees with no modification.

- - -
## General form

The same reasoning applies, with no essential change, to a polynomial of arbitrary degree. Let \\(p(x)\\) be a polynomial of degree \\(n\\) with leading coefficient \\(a_n \neq 0\\):

\\[
p(x) = a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0
\\]

By the [fundamental theorem of algebra](../roots-of-a-polynomial/), \\(p(x)\\) admits exactly \\(n\\) roots in \\(\mathbb{C}\\), counted with multiplicity. Denoting them \\(x_1, x_2, \ldots, x_n\\), the polynomial factors as:

\\[
p(x) = a_n (x - x_1)(x - x_2) \cdots (x - x_n)
\\]

Expanding the product and collecting like terms produces a polynomial whose coefficients are themselves polynomial expressions in the roots. These expressions share two structural features: they are symmetric, in the sense that any permutation of the roots leaves them unchanged, and elementary, in the sense that each consists of a sum of products of distinct roots. They are the elementary symmetric polynomials.

For \\(k = 1, 2, \ldots, n\\), the \\(k\\)-th elementary symmetric polynomial in the roots is defined as follows.

\\[
e_k(x_1, \ldots, x_n) = \sum_{1 \le i_1 < i_2 < \cdots < i_k \le n} x_{i_1} x_{i_2} \cdots x_{i_k}
\\]

In other words, \\(e_k\\) is the sum of all distinct products of \\(k\\) roots. The first and last instances are the most familiar:

\\[
e_1 = x_1 + x_2 + \cdots + x_n, \qquad e_n = x_1 x_2 \cdots x_n
\\]

With this notation, Vieta's formulas in their general form take the compact statement:

\\[
\frac{a_{n-k}}{a_n} = (-1)^k\\, e_k(x_1, \ldots, x_n), \qquad k = 1, 2, \ldots, n
\\]

Two cases deserve to be singled out. The coefficient adjacent to the leading one corresponds to the negative of the sum of the roots:

\\[
\frac{a_{n-1}}{a_n} = -(x_1 + x_2 + \cdots + x_n)
\\]

The constant term encodes the product of the roots, with a sign that depends on the parity of the degree:

\\[
\frac{a_0}{a_n} = (-1)^n\\, x_1 x_2 \cdots x_n
\\]

> When the polynomial is monic, that is, when \\(a_n = 1\\), the formulas simplify accordingly. The factor at the denominator disappears, and each coefficient \\(a_{n-k}\\) coincides, up to the sign \\((-1)^k\\), with the corresponding elementary symmetric polynomial in the roots.

- - -
## The cubic case

Specialising the general statement to degree three produces a useful intermediate case between the quadratic identities and the formal expression in arbitrary degree. Consider the cubic equation in standard form:

\\[
ax^3 + bx^2 + cx + d = 0, \qquad a \neq 0
\\]

Calling the roots \\(x_1\\), \\(x_2\\), \\(x_3\\), Vieta's formulas read:

\\[
\begin{align}
x_1 + x_2 + x_3 &= -\frac{b}{a} \\\\[6pt]
x_1 x_2 + x_1 x_3 + x_2 x_3 &= \frac{c}{a} \\\\[6pt]
x_1 x_2 x_3 &= -\frac{d}{a}
\end{align}
\\]

The three identities correspond to the elementary symmetric polynomials \\(e_1\\), \\(e_2\\), and \\(e_3\\). The middle one, often the least familiar, is the sum of all distinct pairwise products of the roots. The pattern of alternating signs, already visible in the quadratic case, is dictated by the formula \\((-1)^k e_k = a_{n-k}/a_n\\).

- - -
## Example 1

Consider the quadratic equation:

\\[
x^2 - 5x + 6 = 0
\\]

Vieta's formulas demand that the two roots have sum equal to \\(5\\) and product equal to \\(6\\). Among the integer pairs whose product is \\(6\\), namely \\((1, 6)\\), \\((-1, -6)\\), \\((2, 3)\\), and \\((-2, -3)\\), only the pair \\((2, 3)\\) also has the required sum. The polynomial therefore admits the factorisation:

\\[
x^2 - 5x + 6 = (x - 2)(x - 3)
\\]

The roots are \\(x_1 = 2\\) and \\(x_2 = 3\\). The procedure works whenever the roots are rational and small enough to be located by inspection. When this fails, the [quadratic formula](../quadratic-formula/) remains the general-purpose method.

- - -
## Example 2

Consider the cubic equation:

\\[
x^3 - 6x^2 + 11x - 6 = 0
\\]

Suppose, by inspection or by trial, that its roots are \\(1\\), \\(2\\), and \\(3\\). To confirm, we evaluate the elementary symmetric polynomials in these three values:

\\[
\begin{align}
e_1 &= 1 + 2 + 3 = 6 \\\\[6pt]
e_2 &= 1 \cdot 2 + 1 \cdot 3 + 2 \cdot 3 = 11 \\\\[6pt]
e_3 &= 1 \cdot 2 \cdot 3 = 6
\end{align}
\\]

The leading coefficient is \\(a = 1\\), so Vieta's formulas read \\(-b = e_1\\), \\(c = e_2\\), and \\(-d = e_3\\). Substituting the values from the equation gives \\(-(-6) = 6\\), \\(11 = 11\\), and \\(-(-6) = 6\\), all in agreement. The factorisation is therefore:

\\[
x^3 - 6x^2 + 11x - 6 = (x - 1)(x - 2)(x - 3)
\\]

- - -
## Constructing a polynomial from its roots

Vieta's formulas can be read in the opposite direction: given a list of numbers, the monic polynomial having precisely those numbers as roots is determined by their elementary symmetric polynomials. If \\(\alpha_1, \alpha_2, \ldots, \alpha_n\\) are the assigned roots, the polynomial is:

\\[
p(x) = x^n - e_1\\, x^{n-1} + e_2\\, x^{n-2} - \cdots + (-1)^n e_n
\\]

As an illustration, suppose we want the monic polynomial whose roots are \\(2\\), \\(-1\\), and \\(3\\). Computing the three elementary symmetric polynomials in these values:

\\[
\begin{align}
e_1 &= 2 + (-1) + 3 = 4 \\\\[6pt]
e_2 &= 2 \cdot (-1) + 2 \cdot 3 + (-1) \cdot 3 = 1 \\\\[6pt]
e_3 &= 2 \cdot (-1) \cdot 3 = -6
\end{align}
\\]

Substituting into the general formula yields:

\\[
p(x) = x^3 - 4x^2 + x + 6
\\]

The polynomial has the prescribed roots, as can be verified by direct substitution of \\(x = 2\\), \\(x = -1\\), and \\(x = 3\\), each of which makes \\(p(x)\\) vanish.

- - -
## Applications

Vieta's formulas underpin a number of techniques that recur throughout elementary algebra and beyond. Three uses are worth recording.

The first is the verification of a candidate factorisation. Given a proposed pair of roots \\(x_1\\) and \\(x_2\\) for a quadratic with coefficients \\(a\\), \\(b\\), \\(c\\), the conditions \\(x_1 + x_2 = -b/a\\) and \\(x_1 x_2 = c/a\\) provide a fast consistency check that requires no recomputation of the discriminant.

The second is the [AC method](../factoring-polynomials-ac-method/) for factoring quadratic trinomials. The conditions \\(mn = ac\\) and \\(m + n = b\\) imposed by that procedure are precisely Vieta's formulas applied to the rescaled polynomial \\(u^2 + bu + ac\\), with \\(u = ax\\). The dedicated entry develops the correspondence in detail.

The third arises in the study of the [roots of unity](../roots-of-unity/), where the polynomial \\(z^n - 1\\) has all its non-leading coefficients equal to zero except for the constant term. Vieta's formulas then state that the sum of the \\(n\\)-th roots of unity vanishes whenever \\(n \geq 2\\), and that their product equals \\((-1)^{n+1}\\). Both results follow by inspection of the coefficients of \\(z^n - 1\\).

- - -
## Structural interpretation

Behind Vieta's formulas lies a more general phenomenon. The elementary symmetric polynomials \\(e_1, e_2, \ldots, e_n\\) form a system of generators for the ring of symmetric polynomials in the variables \\(x_1, \ldots, x_n\\): every polynomial expression in the roots that is invariant under permutation can be written, in a unique way, as a polynomial in the \\(e_k\\). This statement is the fundamental theorem of symmetric polynomials.

Vieta's formulas record one half of this picture, expressing the coefficients of the polynomial in terms of the elementary symmetric polynomials. The other half consists of expressing other symmetric quantities of the roots, such as the power sums \\(x_1^p + x_2^p + \cdots + x_n^p\\), in terms of the same \\(e_k\\). These conversions are organised by Newton's identities. Together, the two results form the foundation on which more advanced developments rest, including the systematic study of how the roots of a polynomial transform under permutations, which eventually leads to the framework of Galois theory.

> When the roots are not all distinct, Vieta's formulas remain valid provided that each root is listed in the elementary symmetric polynomials according to its multiplicity. A double root \\(x_0\\), for instance, appears as \\(x_1 = x_2 = x_0\\) in the list, and contributes accordingly to each \\(e_k\\).
