---
title: Logarithmic Equations
source: https://algebrica.org/logarithmic-equations/
license: CC BY-NC 4.0
tags:
  - equations
  - logarithmic-function
  - logarithms
---
## Introduction

Logarithmic equations are [equations](../equations/) in which the unknown appears inside a [logarithm](../logarithms/). Solving them rests on the properties of logarithms and on the way these properties allow the unknown to be isolated. A logarithmic equation has the general form:

$$\log_a f(x) = g(x)$$

+ $a$ is the base of the logarithm and must satisfy $a > 0$ and $a \neq 1$.
+ $f(x)$, the argument of the logarithm, must be greater than zero, because the [logarithmic function](../logarithmic-function/) is defined only for positive [numbers](../types-of-numbers/).

> Solving logarithmic equations relies on a firm grasp of the logarithmic properties, in particular the product, quotient, and power rules, which allow complex expressions to be simplified and the unknown to be isolated.

## How to solve logarithmic equations

The resolution of a logarithmic equation can be organized into four steps.

+ Determine the [domain](../determining-the-domain-of-a-function/) of the equation by requiring that the argument of every logarithm be positive and that each base be greater than zero and different from one. 
+ For a single logarithm $\log_a f(x)$ these conditions read: 

$$\begin{cases} a > 0 \\[6pt] a \neq 1 \\[6pt] f(x) > 0 \end{cases}$$

+ Apply the [logarithmic properties](../logarithms/), such as the product, quotient, and power rules, to combine and simplify the logarithmic terms. The aim is to reduce the equation to a simpler form in which the unknown can be isolated.

+ Once the equation is simplified, solve for the unknown by removing the logarithms. This step usually amounts to passing to the exponential form on both sides.

+ Substitute the solutions back into the original equation and confirm that each one lies within the domain identified in the first step.

> The domain restrictions found in the first step often introduce additional conditions on the unknown. A systematic treatment of these conditions appears in the dedicated entry on [logarithmic inequalities](../logarithmic-inequalities/), which complements the solution of logarithmic equations.

## Simplified forms of logarithmic equations

Once a logarithmic equation has been simplified, it usually reduces to one of a few standard forms. The first is the equality between two logarithms with the same base:

$$\log_a f(x) = \log_a g(x)$$

Since the logarithmic function is injective, two logarithms with the same base are equal precisely when their arguments are equal. It is therefore enough to equate the arguments and solve the resulting equation:

$$f(x) = g(x)$$

> This equivalence holds only where both logarithmic expressions are defined. Always verify that $f(x) > 0$, that $g(x) > 0$, and that the base satisfies $a > 0$ and $a \neq 1$ before equating the arguments.

- - -

The second standard form is the equality between a logarithm and a constant:

$$\log_a f(x) = b$$

Here no further simplification is possible, so the solution uses the definition of the logarithm and passes to the exponential form, giving:

$$f(x) = a^b$$

- - -

The third standard form arises when the same logarithm appears raised to different powers, with one base and one argument:

$$\log_a^2(x + c) + \log_a(x + c) + k = 0$$

In this case the substitution $z = \log_a(x + c)$ transforms the equation into:

$$z^2 + z + k = 0$$

The problem becomes a [quadratic equation](../quadratic-equations/), or more generally an equation of degree $n$, which can be solved with the [quadratic formula](../quadratic-formula/) or with [synthetic division](../synthetic-division/) for [polynomials](../polynomials/) of degree $n > 2$.

## Example 1

We solve the logarithmic equation:

$$\log_3(2x + 1) = \log_3(x^2)$$

- - -

The first step is to determine the domain, requiring that the argument of each logarithm be positive. This produces two conditions:

$$2x + 1 > 0 \rightarrow x > -\frac{1}{2}$$


$$x^2 > 0 \rightarrow x \neq 0$$

[shortcode="intervals"]
|     | $-\frac{1}{2}$  | $0$      |     |
|:----|------------|---------------|-----|
|     | sign+l-o-h |     |     |
|     |   | sign+r-o-h sign+l-o-h    |     |
[/shortcode]

Combining the two conditions, the domain $D$ is given by the union of intervals:

$$\left( -\frac{1}{2}, 0 \right) \cup (0, +\infty)$$

- - -

The logarithms have the same base and the equation has the form $\log_a f(x) = \log_a g(x)$, so we may equate the arguments. Moving every term to one side produces a standard [quadratic equation](../quadratic-equations/):

$$x^2 - 2x - 1 = 0$$

We solve it with the [quadratic formula](../quadratic-formula/):

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

where $a = 1$, $b = -2$, and $c = -1$. Substituting these values gives:

$$
\begin{align}
x &= \frac{-(-2) \pm \sqrt{(-2)^2 - 4 \cdot 1 \cdot (-1)}}{2 \cdot 1} \\[6pt]
  &= \frac{2 \pm \sqrt{4 + 4}}{2} \\[6pt]
  &= \frac{2 \pm \sqrt{8}}{2} \\[6pt]
  &= \frac{2 \pm 2\sqrt{2}}{2} \\[6pt]
  &= 1 \pm \sqrt{2}
\end{align}
$$

- - -

It remains to check that both solutions lie in the domain:

+ $x = 1 + \sqrt{2} \approx 2.414$ satisfies $x > -\frac{1}{2}$ and $x \neq 0$.
+ $x = 1 - \sqrt{2} \approx -0.414$ satisfies $x > -\frac{1}{2}$ and $x \neq 0$.

Both values belong to $D$, so the equation has two solutions:

$$x = 1 \pm \sqrt{2}$$

## Example 2

We solve a logarithmic equation that combines two logarithms through the product rule and reduces to the constant form:

$$\log_2(x - 1) + \log_2(x + 1) = 3$$

- - -

The first step is to determine the domain. Both arguments must be positive, which produces two conditions:

$$x - 1 > 0 \rightarrow x > 1$$


$$x + 1 > 0 \rightarrow x > -1$$

The two conditions hold simultaneously only when $x > 1$, so the domain is the interval:

$$D = (1, +\infty)$$

- - -

The two logarithms have the same base and are added, so the [product rule](../logarithms/) combines them into a single logarithm:

$$\log_2\bigl[(x - 1)(x + 1)\bigr] = 3$$

Expanding the product gives a single logarithm of a quadratic expression:

$$\log_2(x^2 - 1) = 3$$

The equation now has the constant form $\log_a f(x) = b$, so passing to the exponential form removes the logarithm:

$$x^2 - 1 = 2^3$$

- - -

The resulting [quadratic equation](../quadratic-equations/) is solved directly:

$$
\begin{align}
&x^2 - 1 = 8 \\[6pt]
&x^2 = 9 \\[6pt]
&x = \pm 3
\end{align}
$$

It remains to compare the candidate solutions with the domain $D = (1, +\infty)$:

+ $x = 3$ satisfies $x > 1$ and is admissible.
+ $x = -3$ does not satisfy $x > 1$ and must be discarded.

The value $x = -3$ is an extraneous solution introduced when the two logarithms were combined, since it makes the original arguments negative. The equation therefore has the single solution:

$$x = 3$$

## Example 3

We solve a logarithmic equation in which the same logarithm appears raised to the second power, illustrating the substitution form:

$$\log_2^2 x - 3\log_2 x + 2 = 0$$

- - -

The argument of the logarithm must be positive, so the domain is:

$$D = (0, +\infty)$$

The same logarithmic expression $\log_2 x$ appears with exponent two and one, so the substitution $z = \log_2 x$ transforms the equation into a [quadratic equation](../quadratic-equations/):

$$z^2 - 3z + 2 = 0$$

Factoring the trinomial gives:

$$(z - 1)(z - 2) = 0$$

so the two values are $z_1 = 1$ and $z_2 = 2$.

- - -

Reversing the substitution $z = \log_2 x$ produces two elementary logarithmic equations. The first is:

$$\log_2 x = 1$$

which gives $x = 2^1 = 2$. The second is:

$$\log_2 x = 2$$

which gives $x = 2^2 = 4$. Both values are positive and therefore belong to the domain $D$. The equation has the two solutions:

$$x_1 = 2 \qquad x_2 = 4$$

## Existence and number of solutions

The number of solutions of a logarithmic equation reflects the behaviour of the [logarithmic function](../logarithmic-function/). For a base $a > 1$ the function $\log_a x$ is strictly increasing, while for $0 < a < 1$ it is strictly decreasing; in both cases it is injective, so an elementary equation $\log_a x = b$ has exactly one solution for every real value of $b$. This is the property that justifies equating the arguments of two logarithms with the same base.

The domain conditions are what limit the number of admissible solutions. Algebraic manipulations such as the product and quotient rules can enlarge the domain of the transformed equation, introducing values that satisfy it but not the original equation. 

Each candidate must therefore be checked against the domain determined at the outset, as in Example 2, where one of the two algebraic roots had to be discarded. 

Verifying the domain is the step that distinguishes correct solutions from extraneous ones, and it parallels the analogous requirement for [exponential equations](../exponential-equations/), where the inverse relationship between the two functions governs the same reasoning.
