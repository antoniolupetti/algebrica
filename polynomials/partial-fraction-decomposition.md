---
title: Partial Fraction Decomposition
source: https://algebrica.org/partial-fraction-decomposition/
license: CC BY-NC 4.0
tags:
  - cover-up-rule
  - improper-rational-function
  - partial-fractions
  - polynomial-division
  - rational-function
---

## The decomposition method

Partial fraction decomposition is a method for rewriting a [proper rational function](../rational-functions/) as a sum of fractions, based on the fact that once the denominator has been factored into [irreducible factors](../unique-factorization-of-polynomials/), the original function can be expressed as a sum of elementary terms. This simplifies many calculations, including integration, since it reduces the problem to integrating partial fractions whose antiderivatives are generally known. Consider, for example, a general proper rational function in which $P(x)$ and $Q(x)$ are [polynomials](../polynomials/) and the degree of $P$ is less than that of $Q$:

$$\frac{P(x)}{Q(x)} \tag{1}$$

To decompose the fraction in $(1)$ into partial fractions, we write $Q(x)$ as a product of linear and quadratic factors that are irreducible over the reals. If $Q(x)=(x-a)(x-b)$ with $a\ne b,$ the two partial fractions have constant numerators $A$ and $B$:

$$
\frac{P(x)}{(x-a)(x-b)} = \frac{A}{x-a} + \frac{B}{x-b} \tag{2}
$$

As an example, we apply $(2)$ to the following rational function:

$$
\frac{5x + 4}{2x^2 - x - 6} \tag{3}
$$

The fraction in $(3)$ is proper, and its denominator factors as $(x-2)(2x+3).$ Since the two factors have [distinct roots](../roots-of-a-polynomial/), $(2)$ gives the following decomposition:

$$
\frac{5x + 4}{(x - 2)(2x + 3)} = \frac{A}{x - 2} + \frac{B}{2x + 3} \tag{4}
$$

To determine $A$ and $B,$ we multiply both sides of $(4)$ by the common denominator $(x-2)(2x+3)$ to obtain:

$$
5x + 4 = A(2x + 3) + B(x - 2) \tag{5}
$$

To isolate one coefficient at a time, we use Heaviside's method and substitute the two roots of the denominator into $(5).$ For example, substituting $x = 2$ into $(5)$ gives:

$$
5(2) + 4 = A(2 \cdot 2 + 3) + B(0)
$$

Simplifying gives the value of $A$:

$$
\begin{align}
14 &= 7A \\[6pt]
A &= 2
\end{align}
$$

We next find $B.$ Setting $x=-3/2$ in $(5)$ gives:

$$
\begin{align}
5\left(-\frac{3}{2}\right)+4 &= B\left(-\frac{3}{2}-2\right) \\[6pt]
-\frac{7}{2} &= -\frac{7}{2}B \\[6pt]
B &= 1
\end{align}
$$

Substituting $A=2$ and $B=1$ into $(4),$ we obtain the decomposition of $(3)$ into two partial fractions:

$$
\frac{5x + 4}{(x - 2)(2x + 3)} = \frac{2}{x - 2} + \frac{1}{2x + 3}
$$

- - -

In general, if an irreducible factor of $Q(x)$ has multiplicity $k,$ we write one partial fraction for each power of the factor, from the first through the $k$th. For example, for a linear factor $x+a$ the numerators are constants, so this factor contributes the following terms to the decomposition:

$$
\frac{A_1}{x+a}+\frac{A_2}{(x+a)^2}+\cdots+\frac{A_k}{(x+a)^k} \tag{6}
$$

For an irreducible quadratic factor $q(x)=x^2+ax+b,$ the numerators have degree at most one. Writing each numerator in the form $B_jx+C_j,$ we obtain:

$$
\frac{B_1x+C_1}{q(x)}+\frac{B_2x+C_2}{q(x)^2}+\cdots+\frac{B_kx+C_k}{q(x)^k} \tag{7}
$$

> Every proper rational function with real coefficients has a partial fraction decomposition, and once the factors of the denominator are fixed, the coefficients in $(6)$ and $(7)$ are uniquely determined.

## Example 1

As a further example, we apply $(6)$ to a fraction with a cubic denominator:

$$
\frac{1}{x^3-6x^2+11x-6} \tag{8}
$$

The denominator vanishes at $x=1,$ since $1-6+11-6=0.$ Dividing by $x-1$ using [synthetic division](../synthetic-division/) gives:

$$
\begin{array}{r|rrrr}
1 & 1 & -6 & 11 & -6 \\[6pt]
  &   & 1 & -5 & 6 \\[6pt]
\hline
  & 1 & -5 & 6 & 0
\end{array} \tag{9}
$$

The quotient $x^2-5x+6$ from $(9)$ factors as $(x-2)(x-3).$ The denominator therefore has three distinct linear factors, each with a constant numerator in the decomposition, so we can write:

$$
\frac{1}{(x-1)(x-2)(x-3)}
= \frac{A}{x-1}+\frac{B}{x-2}+\frac{C}{x-3} \tag{10}
$$

Multiplying both sides of $(10)$ by the common denominator gives the following identity:

$$
\begin{align}
1 &= A(x-2)(x-3)+B(x-1)(x-3) \\[6pt]
  &\quad + C(x-1)(x-2) \tag{11}
\end{align}
$$

Substituting each root of the denominator of $(8)$ into $(11)$ eliminates two terms and determines the coefficient of the third, giving:

$$
\begin{align}
x=1 &\implies 1=2A  &&\implies A=1/2 \\[6pt]
x=2 &\implies 1=-B  &&\implies B=-1 \\[6pt]
x=3 &\implies 1=2C  &&\implies C=1/2 \tag{12}
\end{align}
$$

Substituting the coefficients from $(12)$ into $(10)$ gives the decomposition of $(8)$:

$$
\frac{1}{x^3-6x^2+11x-6}
= \frac{1}{2(x-1)}-\frac{1}{x-2}+\frac{1}{2(x-3)}
$$

## Example 2

We now apply $(6)$ to a repeated linear factor:

$$
\frac{2x+3}{(x-1)^2(x+2)}
= \frac{A}{x-1}+\frac{B}{(x-1)^2}+\frac{C}{x+2}
$$

Multiplying by the common denominator, as in the previous example, gives the following identity:

$$
2x+3=A(x-1)(x+2)+B(x+2)+C(x-1)^2 \tag{13}
$$

Substituting the roots of the denominator into $(13)$ isolates first $B$ and then $C$:

$$
\begin{align}
x=1 &\implies 5=3B &&\implies B=5/3 \\[6pt]
x=-2 &\implies -1=9C &&\implies C=-1/9
\end{align}
$$

Comparing the coefficients of $x^2$ in $(13)$ gives $A+C=0,$ so $A=-C=1/9.$ The resulting decomposition is:

$$
\frac{2x+3}{(x-1)^2(x+2)}
= \frac{1}{9(x-1)}+\frac{5}{3(x-1)^2}-\frac{1}{9(x+2)}
$$

- - -

Next, consider a denominator with one linear factor and one quadratic factor, $x^2+1,$ which has [no real roots](../quadratic-equations/). By $(7)$ the numerator of the corresponding partial fraction has the form $Bx+C.$

$$
\frac{3x+1}{(x-1)(x^2+1)}
= \frac{A}{x-1}+\frac{Bx+C}{x^2+1}
$$

Multiplying by the common denominator gives the identity:

$$
3x+1=A(x^2+1)+(Bx+C)(x-1) \tag{14}
$$

Setting $x=1$ in $(14)$ gives $4=2A,$ so $A=2.$ We now compare the coefficients of $x^2$ and the constant terms on the two sides:

$$
\begin{align}
A+B &= 0 &&\implies B=-2 \\[6pt]
A-C &= 1 &&\implies C=1
\end{align}
$$

The decomposition is therefore:

$$
\frac{3x+1}{(x-1)(x^2+1)}
= \frac{2}{x-1}+\frac{-2x+1}{x^2+1}
$$

## Improper rational functions

The preceding examples all involved proper fractions. We now consider what happens when the degree of $P(x)$ is greater than or equal to that of $Q(x).$ Dividing $P$ by $Q$ gives a [quotient](../polynomial-division/) $S$ and a remainder $R,$ so we can write the ratio of the two polynomials as follows:

$$
\frac{P(x)}{Q(x)}=S(x)+\frac{R(x)}{Q(x)} \tag{15}
$$

If the remainder is zero, the division is exact. Otherwise, $\deg R\lt\deg Q,$ so $R(x)/Q(x)$ is a proper fraction.

Consider, for example, the following improper fraction:

$$
\frac{x^3+2x}{x^2-1} \tag{16}
$$

Dividing the numerator $x^3+2x$ by the denominator $x^2-1$ gives the quotient $S(x)=x$ and the remainder $R(x)=3x,$ so by $(15)$ we can rewrite $(16)$ as:

$$
\begin{align}
\frac{x^3+2x}{x^2-1}
&=x+\frac{3x}{x^2-1} \\[6pt]
&=x+\frac{3}{2(x-1)}+\frac{3}{2(x+1)}
\end{align}
$$

## Application to integration

As noted at the outset, partial fraction decomposition is useful in calculations involving rational functions, particularly in [integration](../integral-of-rational-functions/). Consider, for example, the following integral:

$$
I=\int \frac{5x+4}{(x-2)(2x+3)} \ dx \tag{17}
$$

The integrand is the function in $(3),$ for which we have already found the coefficients $A=2$ and $B=1.$ Using the decomposition in $(4),$ we can therefore write:

$$
\frac{5x+4}{(x-2)(2x+3)}=\frac{2}{x-2}+\frac{1}{2x+3}
$$

By [linearity of integration](../indefinite-integrals/), $(17)$ reduces to the sum of two integrals:

$$
I=2\int\frac{1}{x-2} \ dx+\int\frac{1}{2x+3} \ dx
$$

Both integrands have [logarithmic](../logarithms/) antiderivatives because each has a linear denominator and a constant numerator, so we obtain:

$$
I=2\ln|x-2|+\frac{1}{2}\ln|2x+3|+c
$$