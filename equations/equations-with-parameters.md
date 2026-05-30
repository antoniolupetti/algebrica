---
title: Equations with Parameters
source: https://algebrica.org/equations-with-parameters/
license: CC BY-NC 4.0
tags:
  - equations
  - parameters
  - parametric-equations
---

## Introduction

A parametric equation is a family of [equations](../equations/) indexed by a real quantity that is allowed to vary freely. This quantity, known as a parameter, appears among the coefficients of the equation and is treated as a constant while solving for the unknown, even though its value is not specified in advance.

A parameter differs from an ordinary unknown in that its value is fixed temporarily while the equation is solved for the remaining variable. The behaviour of the solutions is then analysed as the parameter varies. This distinction matters from the outset. For example, in the following equation both the structure and the solution are completely determined:

$$2x + 3 = 7$$

The situation changes when the equation is written as follows:

$$kx + 3 = 7$$

More generally we have:

$$kx + m = 0$$

In this context $k$ and $m$ are real parameters, and the equation defines not a single algebraic problem but an entire family of problems, one for each admissible pair $(k, m)$.

Solving an equation with parameters means determining, for each parameter configuration, the values of the unknown that satisfy the equation, and analysing how these values depend on the parameter.

- - -

A parameter is a real number that remains fixed within a single instance of an equation, whereas the unknown is the variable being solved for. The same symbol may play different roles depending on how the problem is framed.

For example, in the equation $ax + b = 0$, if the objective is to find the value of $x$ that satisfies the equation, then $a$ and $b$ are parameters and $x$ is the unknown. Conversely, if the question concerns which pairs $(a, b)$ yield a solution equal to $1$, then $a$ and $b$ become the unknowns.

The term parametric equations also appears in calculus and analytic geometry to describe curves whose coordinates are expressed as functions of a common variable, such as $x(t)$ and $y(t)$. In the present context, however, the term refers to equations whose coefficients depend on one or more real parameters, with solutions analysed as those parameters vary.

## Linear equations with parameters

The most basic context in which parameters arise is the [first-degree equation](../linear-equations-with-parameters/). A general linear equation with one unknown $x$ and a real parameter $k$ can be written as:

$$a(k) \cdot x + b(k) = 0$$

Here $a(k)$ and $b(k)$ are expressions involving $k$. The analysis divides into two cases, determined by whether the coefficient of $x$ is zero. When $a(k) \neq 0$, the equation has a unique solution:

$$x = -\frac{b(k)}{a(k)}$$

This solution defines a [function](../functions/) of the parameter.

+ If $a(k) = 0$, the equation is no longer linear.
+ If $b(k)$ also equals zero, every real number is a solution and the equation is satisfied identically.
+ If $b(k) \neq 0$, no solution exists and the equation is inconsistent.

## Example 1

Consider the following linear equation involving the parameter $k$:

$$(k - 1)x = k^2 - 1$$

The coefficient of $x$ is $a(k) = k - 1$, and the right-hand side is $b(k) = k^2 - 1$. Since the right-hand side factors as $(k-1)(k+1)$, the case $k = 1$ requires separate consideration.

For $k \neq 1$, both sides can be divided by $k - 1$ without ambiguity, since the divisor is nonzero. This yields:

$$x = \frac{(k-1)(k+1)}{k-1} = k + 1$$

The equation therefore has the unique solution $x = k + 1$ for every real value of $k$ except $1$. When $k = 1$, both sides become zero and the equation reduces to $0 \cdot x = 0$. This identity is satisfied by every real $x$, so the solution set is $\mathbb{R}$. In summary:

$$
\begin{align}
k = 1 &\Rightarrow x \in \mathbb{R} \\[6pt]
k \neq 1 &\Rightarrow x = k + 1
\end{align}
$$

## Quadratic equations with parameters

Introducing a parameter into the coefficients of a [quadratic equation](../quadratic-equations-with-parameters/) increases the complexity of the analysis. The structure of the solution set depends both on the possible vanishing of a coefficient and on the sign of the discriminant, which itself varies with the parameter. A general parametric quadratic equation can be written as:

$$a(k)x^2 + b(k)x + c(k) = 0 \qquad a(k) \neq 0$$

The condition $a(k) \neq 0$ must be verified for each value of the parameter, or the equation reduces to a linear form. The [discriminant](../quadratic-formula/) becomes a real-valued function of $k$:

$$\Delta(k) = b(k)^2 - 4a(k)c(k)$$

Analysing the sign of the discriminant classifies the solutions:

+ Two distinct real roots occur when $\Delta(k) > 0$.
+ A repeated real root arises when $\Delta(k) = 0$.
+ Two [complex conjugate roots](../quadratic-equations-with-complex-solutions/) exist when $\Delta(k) < 0$.

The parameter values at which the discriminant changes sign are critical thresholds, marking transitions between qualitatively different solution structures.

## Higher-degree and transcendental equations with parameters

This reasoning extends beyond quadratic equations. Consider a general [polynomial equation](../polynomial-equations/) of degree $n$:

$$a_n(k)x^n + a_{n-1}(k)x^{n-1} + \cdots + a_1(k)x + a_0(k) = 0$$

The number and nature of the solutions depend on the parameter in ways that are often harder to characterise. For $n \geq 3$, closed-form solution formulas become highly intricate or are unavailable in the classical sense.

Parameters may also appear in non-polynomial equations, including [exponential equations](../exponential-equations/) of the form $a^x = f(k)$, [logarithmic equations](../logarithmic-equations/) involving $\log_a(x + k)$, and trigonometric equations such as $\sin x = k$.

For example, the equation $\sin x = k$ has solutions only when $|k| \leq 1$, and within this interval there are infinitely many solutions distributed periodically along the real line. When $k$ lies outside $[-1, 1]$, the equation has no solution. The parameter therefore determines not only the form of the solutions but also their existence.

## Example 2

The next example illustrates a case where the existence of solutions cannot be determined by algebraic manipulation alone, but requires an analytic argument based on the behaviour of a derived function. Consider the equation:

$$\sin x = kx \qquad k \in \mathbb{R}$$

The solution $x = 0$ exists for every value of $k$, since $\sin 0 = 0$. The question of interest is whether non-trivial solutions exist. Defining $f(x) = \sin x - kx$, the solutions correspond to the zeros of $f$. Since $f$ is an odd function, it suffices to study the case $x > 0$.

For $x > 0$, the condition $\sin x = kx$ can be rewritten as:

$$k = \frac{\sin x}{x}$$

The function $g(x) = \dfrac{\sin x}{x}$ is [continuous](../continuous-functions/) for $x > 0$, tends to $1$ as $x \to 0^+$, and oscillates with decreasing amplitude toward $0$. Its [local maxima](../maximum-minimum-and-inflection-points/) form a strictly decreasing [sequence](../sequences/), all below $1$.

+ For $k \geq 1$, the line $y = kx$ is too steep to intersect the sinusoid outside the origin, and no non-trivial solution exists.
+ For $0 < k < 1$, the line intersects the curve $y = \sin x$ on each arc where $\left|\frac{\sin x}{x}\right| > k$, producing infinitely many non-trivial solutions, distributed symmetrically about the origin.

As $k \to 0^+$, the number of intersections grows without bound. For $k \leq 0$, the right-hand side $kx$ is non-positive for $x > 0$, while $\sin x$ changes sign, so solutions still exist but their distribution depends on the specific value of $k$. In summary, the solution set is:

+ If $k \geq 1$: $x = 0$ is the only solution.
+ If $0 < k < 1$: $x = 0$ and infinitely many symmetric non-trivial solutions.
+ If $k \leq 0$: $x = 0$ and additional solutions depending on $k$.

## Systems of equations with parameters

Parameters appear naturally in systems as well. A [linear system](../systems-of-linear-equations/) of two equations in two unknowns takes the general form:

$$
\begin{align}
a_{11}(k)x + a_{12}(k)y &= b_1(k) \\[6pt]
a_{21}(k)x + a_{22}(k)y &= b_2(k)
\end{align}
$$

The system has a unique solution when the coefficient [matrix](../matrices/) is invertible, that is when its determinant $D(k)$ is nonzero:

$$D(k) = a_{11}(k)a_{22}(k) - a_{12}(k)a_{21}(k)$$

When $D(k) = 0$ for some value of the parameter, the system either becomes inconsistent or admits infinitely many solutions, depending on whether the right-hand side [vector](../vectors/) is compatible with the structure of the coefficient matrix at that value.

## Example 3

Consider the following system:

$$
\begin{align}
kx + y &= 1 \\[6pt]
x + ky &= 1
\end{align}
$$

The determinant of the coefficient matrix is:

$$D(k) = k \cdot k - 1 \cdot 1 = k^2 - 1 = (k-1)(k+1)$$

When $k \neq \pm 1$, the determinant is nonzero and [Cramer's rule](../cramers-rule/) applies directly, yielding a unique solution:

$$x = \frac{k - 1}{k^2 - 1} = \frac{1}{k+1}$$

$$y = \frac{k - 1}{k^2 - 1} = \frac{1}{k+1}$$

We obtain:

$$x = y = \frac{1}{k+1}, \quad k \neq \pm 1$$

At $k = 1$, both equations become $x + y = 1$, so the system reduces to a single equation. The two lines are coincident, and every point on the line $x + y = 1$ is a solution. The solution set is infinite and can be parametrised as $x = t$, $y = 1 - t$ for $t \in \mathbb{R}$.

At $k = -1$, the first equation gives $-x + y = 1$ and the second gives $x - y = 1$. These relations are inconsistent: adding them yields $0 = 2$, a contradiction. The lines are parallel and distinct, and the system has no solution.

The two values $k = \pm 1$ are therefore not merely special but structurally opposite: one leads to underdetermination and the other to incompatibility. In summary:

+ If $k = 1$: infinitely many solutions, $x = t$, $y = 1 - t$ for $t \in \mathbb{R}$.
+ If $k = -1$: no solution.
+ If $k \neq \pm 1$: unique solution $x = y = \dfrac{1}{k+1}$.
