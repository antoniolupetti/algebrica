---
title: Equations
source: https://algebrica.org/equations/
license: CC BY-NC 4.0
tags:
  - algebraic-equations
  - equations
  - transcendental-equations
---

## Definition

An equation is a mathematical statement asserting that two expressions take the same value, typically written in the form $F(x) = G(x)$, where one or more variables act as unknowns ranging over a specified [set](../types-of-numbers/), such as $\mathbb{R}$ or $\mathbb{C}$. To solve an equation is to determine every value of the variable, within the appropriate [domain](../determining-the-domain-of-a-function/), for which the equality holds. Many equations can be reorganized into the form:

$$F(x) = 0$$

This representation simplifies their study, highlights their structure, and provides a unified framework for the different solution methods.

The solution to an equation is any value of the variables that makes the equality true. Depending on the equation and its structure, the solution set may contain:

+ a unique solution
+ multiple solutions
+ infinitely many solutions
+ no solution at all

> In some cases, such as trigonometric equations, the set of solutions can be infinite, because the functions involved are periodic.

In other contexts, especially polynomial, exponential, or transcendental equations, the solutions may not lie within the real numbers. When no real value satisfies the equation, the natural setting becomes the [complex plane](../complex-numbers-introduction/), where solutions can still exist and be meaningfully interpreted.

An example is the quadratic equation with negative discriminant, which admits no real roots but always has two complex conjugate solutions, as discussed on the page on [quadratic equations with complex solutions](../quadratic-equations-with-complex-solutions/).

## Equivalent equations and admissible operations

Two equations are equivalent when they have identical solution sets. The objective in solving an equation is to apply a sequence of transformations that preserve this equivalence, reducing the equation to a simpler form in which the solutions are apparent.

Certain operations are guaranteed to yield an equivalent equation. Adding or subtracting the same expression on both sides, or multiplying both sides by a nonzero constant, does not alter the solution set. These manipulations form the basis of most elementary solution techniques. As an illustration, the equation $2x + 4 = 0$ is equivalent to $x + 2 = 0$, obtained by dividing both sides by $2$, and both equations share the unique solution $x = -2$.

Other operations can disrupt equivalence in less obvious ways. Multiplying both sides by an expression involving the variable may introduce extraneous solutions when that expression equals zero for some value of $x$. Similarly, squaring both sides, a common technique for [irrational equations](../irrational-equations/), can produce solutions that satisfy the transformed equation but not the original. Conversely, dividing both sides by a variable expression may eliminate solutions at the points where that expression is zero, a phenomenon addressed on the page on [loss of roots](../loss-of-roots/).

## Algebraic equations

Algebraic equations are equations in which both sides consist entirely of [polynomials](../polynomials/). A polynomial in one variable is a formal expression of the form:

$$P(x) = a_{n}x^{n} + a_{n-1}x^{n-1} + \cdots + a_{1}x + a_{0}$$

In this expression $n$ is a non-negative integer, the coefficients $a_0, a_1, \ldots, a_n$ belong to a fixed field (typically $\mathbb{R}$ or $\mathbb{C}$), and $a_n \neq 0$ when $n \geq 1$. The [integer](../integers/) $n$ is the degree of the polynomial. An algebraic equation takes the form $P(x) = Q(x)$, or equivalently $P(x) - Q(x) = 0$, which reduces the problem to finding the roots of a single polynomial. Algebraic equations are classified according to the degree of the polynomial involved.

[Linear equations](../linear-equations/) have degree $1$. The variable appears to no power higher than the first, and the solution is unique whenever the leading coefficient is nonzero.

[Quadratic equations](../quadratic-equations/) have degree $2$ and take the standard form $ax^2 + bx + c = 0$, with $a \neq 0$. The nature of their solutions is governed by the [discriminant](../quadratic-formula/) $\Delta = b^2 - 4ac$.

+ If $\Delta > 0$ there are two distinct real solutions.
+ If $\Delta = 0$ there is one repeated real solution.
+ If $\Delta < 0$ the solutions are a pair of complex conjugates.

Cubic equations have degree $3$ and take the general form $ax^3 + bx^2 + cx + d = 0$. By the [Fundamental Theorem of Algebra](../roots-of-a-polynomial/), every polynomial of degree $n$ with coefficients in $\mathbb{C}$ has exactly $n$ roots in $\mathbb{C}$, counted with multiplicity. A cubic equation therefore has exactly three roots in $\mathbb{C}$, which may be all real, or one real and two complex conjugates.

Equations of degree higher than three follow the same principle: a [polynomial equation](../polynomial-equations/) of degree $n$ has exactly $n$ roots in $\mathbb{C}$, counted with multiplicity, though explicit formulas for the roots in terms of radicals exist only up to degree four, a fact made precise by Galois theory.

Among higher-degree equations, [binomial](../binomial-equations/) and [trinomial equations](../trinomial-equations/) deserve particular attention. These are equations of degree greater than two that contain only two or three distinct terms, and can often be solved by substitution or by factoring into lower-degree polynomials.

## Rational equations

[Rational equations](../rational-equations/) contain at least one fractional expression whose numerator and denominator are polynomials. In their general form they involve a ratio of polynomials on both sides, and can always be reduced to the form:

$$\frac{P(x)}{Q(x)} = 0$$

This is obtained by transferring all terms to one side and combining them over a common denominator, with the restriction that $Q(x) \neq 0$. A standard approach is to clear denominators by multiplying both sides by the least common multiple of all denominators, transforming the problem into a polynomial equation.

> This step requires care: any value that makes a denominator vanish must be excluded from the solution set from the outset, and candidate solutions obtained after clearing must be checked against these excluded values.

## Irrational equations

[Irrational equations](../irrational-equations/) have the variable inside a radical. A typical equation contains one radical, for example:

$$\sqrt[n]{f(x)} = g(x)$$

In this expression $f(x)$ and $g(x)$ are polynomials with real coefficients. The standard technique consists of isolating the radical and raising both sides to the $n$-th power to eliminate it. When the equation contains more than one radical, the process is applied iteratively: after each step a new radical is isolated and the procedure is repeated until none remain. Each time both sides are raised to a power, the transformation is not equivalence-preserving and may introduce extraneous solutions.

It is therefore necessary to verify every candidate solution in the original equation, and this requirement becomes more important as the number of radicals grows.

## Absolute value equations

[Absolute value equations](../absolute-value-equations/) are equations in which the unknown appears inside an [absolute value](../absolute-value/) expression. The simplest case takes the form $|x| = a$, where $a$ is a real constant, and the solution set depends entirely on the sign of $a$.

+ If $a > 0$, the equation has exactly two solutions, $x = a$ and $x = -a$, since both values have the same distance from the origin on the real line.
+ If $a = 0$, the only solution is $x = 0$, since the absolute value of a real number vanishes if and only if the number itself is zero.
+ If $a < 0$, the equation has no solution in $\mathbb{R}$, since the absolute value is non-negative and cannot equal a negative constant.

> Absolute value equations that contain polynomial or rational expressions often require case analysis based on the sign of the inner expression. Each candidate solution must be verified against the original equation, since the case-splitting procedure may introduce extraneous solutions.

## Transcendental equations

Transcendental equations are equations in which one or more variables appear within transcendental functions, such as [exponential](../exponential-function/), [logarithmic](../logarithmic-function/), or [trigonometric functions](../sine-function/), that cannot be expressed as finite combinations of algebraic operations. These equations go beyond polynomial or rational forms and frequently resist closed-form solution: in many cases no explicit formula for the roots exists, and one must resort to numerical methods to approximate them.

[Logarithmic equations](../logarithmic-equations/) involve a variable inside a logarithmic expression, such as $2\log_2{(2 - x)^2} = 0$. They are typically solved by applying logarithmic properties, such as the power rule, the product and quotient rules, or the change of base formula, to simplify the expression and isolate the variable.

[Exponential equations](../exponential-equations/) have the variable in the exponent of an exponential expression. They typically involve forms such as $a^x = b$, where $a$ and $b$ are constants and $x$ is the unknown.

[Trigonometric equations](../trigonometric-equations/) involve periodic trigonometric functions such as $\sin(x)$, $\cos(x)$, or $\tan(x)$ containing a variable. Because these functions are periodic, trigonometric equations often have infinitely many solutions.

## Systems of equations

A system of equations arises when several equations must be satisfied simultaneously by the same set of unknowns. Such a system consists of two or more equations involving the same variables, and a solution is any assignment of values that satisfies all equations concurrently. 

Systems may be classified as [linear](../systems-of-linear-equations/) or nonlinear according to the form of their equations. Analysing them often requires techniques beyond those used for single equations, including substitution, elimination, and matrix methods for linear systems.
