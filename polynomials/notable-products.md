---
title: Notable Products
source: https://algebrica.org/notable-products/
license: CC BY-NC 4.0
tags:
  - binomial-theorem
  - difference-of-squares
  - factoring
  - notable-products
  - sum-and-difference-of-cubes
---

## List of notable products

Notable products are identities that describe the expansion or [factorisation](../unique-factorization-of-polynomials/) of [polynomials](../polynomials/) and are very useful because they allow expressions such as [binomials](../binomials/) or [trinomials](../trinomials/) to be written in expanded or simpler form, depending on the calculations required in each problem. In general, many of the identities presented below are special cases of the [binomial theorem](../binomial-theorem/), which, for any non-negative integer $n$ and two [real numbers](../real-numbers/) $a$ and $b,$ gives the expansion of the following binomial:

$$(a+b)^n$$

We begin with one of the most recognisable notable products, the square of a binomial, which is obtained by multiplying the binomial by itself. We can distinguish two cases, one for the sum and the other for the difference of the terms:

$$ \tag{1}
\begin{align}
(a+b)^2 &= a^2 + 2ab + b^2 \\[6pt]
(a-b)^2 &= a^2 - 2ab + b^2
\end{align}
$$

To prove this, we expand the first product in $(1)$ to obtain:

$$
\begin{align}
(a+b)^2 &= (a+b)(a+b) \\[6pt]
&= a^2 + ab + ab + b^2 \\[6pt]
&= a^2 + 2ab + b^2
\end{align}
$$

The second identity in $(1)$ is proved in the same way as the first:

$$
\begin{align}
(a-b)^2 &= (a-b)(a-b) \\[6pt]
&= a^2 - ab - ab + b^2 \\[6pt]
&= a^2 - 2ab + b^2
\end{align}
$$
- - -

For a difference of two squares, we can instead rewrite the expression as follows:

$$
a^2 - b^2 = (a+b)(a-b) \tag{2}
$$

To prove this, we rewrite the product on the right-hand side using simple algebraic manipulations to obtain the result in $(2)$:

$$
\begin{align}
(a+b)(a-b) &= a(a-b) + b(a-b) \\[6pt]
&= a^2 - ab + ab - b^2 \\[6pt]
&= a^2 - b^2
\end{align}
$$

- - -

It is worth mentioning that, to factorise a sum of two squares into linear factors, we need to work with [complex numbers](../complex-numbers/), using the imaginary unit $i.$ Suppose, for example, that $a$ and $b$ are real numbers and that we rewrite $b^2=-(ib)^2.$ For the sum of squares, we obtain:

$$ \tag{3}
\begin{align}
a^2+b^2 &= a^2-i^2b^2 \\[6pt]
&= a^2-(ib)^2 \\[6pt]
&= (a+ib)(a-ib)
\end{align}
$$

For example, setting $a=x$ and $b=1$ gives the factorisation:

$$x^2+1=(x+i)(x-i)$$

Formula $(3)$ is also useful for eliminating the imaginary part from the denominator of a fraction, for example when we want to write the [quotient of two complex numbers](../complex-number-operations/) in the form $x+iy$ to determine its real and imaginary parts. If $a$ and $b$ are not both zero, then $a^2+b^2>0.$ Multiplying the numerator and denominator by the conjugate $a-ib,$ we obtain:

$$
\begin{align}
\frac{1}{a+ib} &= \frac{a-ib}{(a+ib)(a-ib)} \\[6pt]
&= \frac{a-ib}{a^2+b^2} \\[6pt]
&= \frac{a}{a^2+b^2}-i\frac{b}{a^2+b^2}
\end{align}
$$

- - -

The following identities hold for the cube of a binomial, depending on whether the two terms are added or subtracted:

$$ \tag{4}
\begin{align}
(a+b)^3 &= a^3 + 3a^2b + 3ab^2 + b^3 \\[6pt]
(a-b)^3 &= a^3 - 3a^2b + 3ab^2 - b^3
\end{align}
$$

To prove the first identity in $(4),$ we expand the left-hand side:

$$
\begin{align}
(a+b)^3 &= (a+b)^2(a+b) \\[6pt]
&= (a^2+2ab+b^2)(a+b) \\[6pt]
&= a(a^2+2ab+b^2)+b(a^2+2ab+b^2) \\[6pt]
&= a^3+2a^2b+ab^2+a^2b+2ab^2+b^3 \\[6pt]
&= a^3+3a^2b+3ab^2+b^3
\end{align}
$$

Similarly, we prove the second identity in $(4)$ to obtain:

$$
\begin{align}
(a-b)^3 &= (a-b)^2(a-b) \\[6pt]
&= (a^2-2ab+b^2)(a-b) \\[6pt]
&= a(a^2-2ab+b^2)-b(a^2-2ab+b^2) \\[6pt]
&= a^3-2a^2b+ab^2-a^2b+2ab^2-b^3 \\[6pt]
&= a^3-3a^2b+3ab^2-b^3
\end{align}
$$

- - -

We now consider the sum and difference of two cubes, for which we have the following identities:

$$ \tag{5}
\begin{align}
a^3 + b^3 &= (a+b)(a^2 - ab + b^2) \\[6pt]
a^3 - b^3 &= (a-b)(a^2 + ab + b^2)
\end{align}
$$

We prove the first identity in $(5)$ by expanding the right-hand side to obtain:

$$
\begin{align}
(a+b)(a^2-ab+b^2) &= a^3 - a^2b + ab^2 + a^2b - ab^2 + b^3 \\[6pt]
&= a^3 + b^3
\end{align}
$$

The same procedure applies to the difference $a^3 - b^3$ and gives:

$$
\begin{align}
(a-b)(a^2+ab+b^2) &= a^3 + a^2b + ab^2 - a^2b - ab^2 - b^3 \\[6pt]
&= a^3 - b^3
\end{align}
$$

You will no doubt have noticed that, while a sum of two cubes can be factorised over the reals, factorising a sum of two squares into linear factors requires the imaginary unit, as shown in $(3).$ This is because the cubes of a real number and its negative are also negatives of each other, so $a^3+b^3$ is zero when $a=-b$ and has $a+b$ as a factor. The squares of real numbers, on the other hand, are always non-negative, and their sum can be zero only when both terms are zero.

- - - 

We therefore summarise the preceding formulas below:

[class="table-1"]

|                                         |                                                                         |
| --------------------------------------- | ----------------------------------------------------------------------- |
| $$(a + b)^2$$                           | $$a^2 + 2ab + b^2$$                                                     |
| $$(a - b)^2$$                           | $$a^2 - 2ab + b^2$$                                                     |
| $$a^2 - b^2$$                           | $$(a + b)(a - b)$$                                                      |
| $$(a + b)^3$$                           | $$a^3 + 3a^2b + 3ab^2 + b^3$$                                           |
| $$(a - b)^3$$                           | $$a^3 - 3a^2b + 3ab^2 - b^3$$                                           |
| $$a^3 + b^3$$                           | $$(a + b)(a^2 - ab + b^2)$$                                             |
| $$a^3 - b^3$$                           | $$(a - b)(a^2 + ab + b^2)$$                                             |

[/class]


## Relationship with the binomial theorem

As stated at the beginning, expressions such as the square and cube of a binomial follow from a general formula given by the binomial theorem, which expands a general binomial through the following identity:

$$ \tag{6}
(a+b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^{k}
$$

Recall that in $(6)$ the [binomial coefficients](../binomial-coefficient/) are defined by formula $(7),$ which uses [factorials](../factorial/):

$$ \tag{7}
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

As an example, we derive the cube of a binomial, that is, the first identity in $(4),$ by setting $n=3$ and calculating the coefficients in the sum. We obtain:

$$
\begin{align}
\binom{3}{0}=\binom{3}{3} &= \frac{3!}{0!3!}=1 \\[6pt]
\binom{3}{1}=\binom{3}{2} &= \frac{3!}{1!2!}=3
\end{align}
$$

Substituting these values into $(6)$ gives precisely the identity we were seeking:

$$
(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3
$$

## Using notable products to solve equations

Notable products allow us to solve some [polynomial equations](../polynomial-equations/) by factorisation, which reduces the problem to equations of lower degree. Consider the following equation:

$$x^3-8=7(x-2) \tag{8}$$

The left-hand side of $(8)$ can be rewritten as $x^3-2^3,$ giving a difference of two cubes. Applying the second identity in $(5),$ we obtain:

$$
\begin{align}
(x-2)(x^2+2x+4)=7(x-2) \\[6pt]
(x-2)(x^2+2x+4)-7(x-2) &= 0 \\[6pt]
(x-2)(x^2+2x+4-7) &= 0 \\[6pt]
(x-2)(x^2+2x-3) &= 0
\end{align}
$$

By the [zero-product property](../factoring-quadratic-equations/), we know that the equation holds when at least one of the two factors is zero, which means solving the two equations:

$$
\begin{align}
&1) \ x-2 = 0 \\[6pt]
&2) \ x^2+2x-3 = 0
\end{align}
$$

The first equation is linear and gives $x=2.$ For the second, we use the [quadratic formula](../quadratic-formula/) to obtain:

$$
\begin{align}
x &= \frac{-2\pm\sqrt{2^2-4(1)(-3)}}{2} \\[6pt]
&= \frac{-2\pm\sqrt{16}}{2} \\[6pt]
&= \frac{-2\pm4}{2}
\end{align}
$$

The solutions of the second equation are $x=1$ and $x=-3.$ The original equation therefore has the three solutions $-3,$ $1$ and $2.$ Factorisation using notable products has thus reduced the cubic equation to a [linear equation](../linear-equations/) and a [quadratic equation](../quadratic-equations/). We have therefore found the solutions of a cubic equation without using [synthetic division](../synthetic-division/).

## Sum and difference of nth powers

The factorisations we have seen for squares and cubes are special cases of more general formulas. For every positive integer $n,$ the difference $a^n-b^n$ always has $a-b$ as a factor. The sum $a^n+b^n,$ on the other hand, has $a+b$ as a factor only when $n$ is odd. When $n \geq 2,$ the difference can be factorised using the formula:

$$ \tag{9}
a^n-b^n = (a-b)(a^{n-1}+a^{n-2}b+a^{n-3}b^2+\cdots+ab^{n-2}+b^{n-1})
$$

When $n \geq 3$ is odd, the sum has a factorisation analogous to $(9),$ with alternating signs in the second factor:

$$ \tag{10}
a^n+b^n = (a+b)(a^{n-1}-a^{n-2}b+a^{n-3}b^2-\cdots-ab^{n-2}+b^{n-1})
$$

In both $(9)$ and $(10),$ when $n=1$ the second factor is $1.$ When $n$ is even, the sum $a^n+b^n$ is not divisible by $a+b,$ but it may admit other factorisations over the reals. The polynomial $a^2+b^2,$ for example, is irreducible over $\mathbb{R},$ whereas $a^4+b^4$ can be factorised into two quadratic factors with real coefficients. In the latter case, since $n = 4$ is even, we cannot apply the formula for the sum of nth powers, which holds for odd exponents. The polynomial nevertheless admits the following factorisation over the reals:

$$a^4 + b^4 = (a^2 + \sqrt{2}ab + b^2)(a^2 - \sqrt{2}ab + b^2)$$

To verify the factorisation, we group $a^2$ and $b^2$ in each factor and rewrite the first factor as $(a^2+b^2)+\sqrt{2}ab$ and the second as $(a^2+b^2)-\sqrt{2}ab.$ The product therefore has the form $(A+B)(A-B),$ with $A=a^2+b^2$ and $B=\sqrt{2}ab.$ Applying identity $(2),$ we obtain:

$$
\begin{align}
(a^2 + \sqrt{2}ab + b^2)(a^2 - \sqrt{2}ab + b^2) &= (a^2 + b^2)^2 - (\sqrt{2}ab)^2 \\[6pt]
&= a^4 + 2a^2b^2 + b^4 - 2a^2b^2 \\[6pt]
&= a^4 + b^4
\end{align}
$$

- - -

Another useful factorisation is Germain's identity, which shows that some [integers](../integers/) of the form $n^4+4m^4$ can be written as a product of two integers greater than $1:$

$$ \tag{11}
a^4+4b^4 = (a^2+2b^2+2ab)(a^2+2b^2-2ab)
$$

The coefficient $4$ in $(11)$ allows us to [complete the square](../completing-the-square/) and rewrite the right-hand side as a difference of two squares:

$$
a^4+4b^4 = (a^2+2b^2)^2-(2ab)^2
$$

Some products involving nth powers are briefly summarised below:

[class="table-1"]

|                                         |                                                                         |
| --------------------------------------- | ----------------------------------------------------------------------- |
| $$a^n + b^n \quad (n \text{ odd})$$ | $$(a + b)(a^{n-1} - a^{n-2}b + \cdots + b^{n-1})$$                      |
| $$a^n - b^n$$                           | $$(a - b)(a^{n-1} + a^{n-2}b + \cdots + b^{n-1})$$                      |
| $$a^{2n} - b^{2n}$$                     | $$(a^n - b^n)(a^n + b^n)$$                                              |
| $$a^4 - b^4$$                           | $$(a - b)(a + b)(a^2 + b^2)$$                                           |
| $$a^4 + b^4$$                           | $$(a^2 + \sqrt{2}ab + b^2)(a^2 - \sqrt{2}ab + b^2)$$                    |
| $$(a + b + c)^2$$                       | $$a^2 + b^2 + c^2 + 2(ab + ac + bc)$$                                   |
| $$(a + b + c)^3$$                       | $$a^3 + b^3 + c^3 + 3(a^2b + a^2c + b^2a + b^2c + c^2a + c^2b) + 6abc$$ |
[/class]

