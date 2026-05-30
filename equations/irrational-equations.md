---
title: Irrational Equations
source: https://algebrica.org/irrational-equations/
license: CC BY-NC 4.0
tags:
  - irrational-equations
  - radicals
  - systems-of-inequalities
---

## Definition of irrational equations

Irrational equations, also called radical equations, are [equations](../equations/) in which the unknown $x$ appears within a [radical](../radicals/) or is raised to a fractional [exponent](../powers/). They form a distinct class of problems that cannot be addressed through standard algebraic manipulations alone. The presence of roots and non-integer exponents imposes additional constraints on the admissible values of $x$, making [domain analysis](../determining-the-domain-of-a-function/) an essential preliminary step.

An irrational equation is an equation of the form $F(x) = 0$ in which at least one term contains a fractional power of a function, that is a power whose exponent has a denominator greater than one. Equivalently, these equations contain radical expressions. The defining term takes the form:

$$f(x)^{\frac{p}{q}} \quad \text{with } q > 1$$

In radical notation it is written as:

$$\sqrt[q]{f(x)}$$

Typical forms place a [polynomial](../polynomials/) under an $n$-th root or raise it to a reciprocal power:

$$\sqrt[n]{f(x)} = g(x)$$

$$f(x)^{\frac{1}{n}} = g(x)$$

In these expressions $f(x)$ and $g(x)$ are [polynomials](../polynomials/) of arbitrary degree with [real coefficients](../types-of-numbers/).

> Solving such equations typically involves eliminating the radical by raising both sides to a suitable power. This process may introduce extraneous solutions, so each candidate must be verified against the domain constraints determined by the original radical expression.

## General forms of irrational equations

Three structural patterns occur most often. The following table compares the radical form of each equation with its equivalent exponential form, in which the radical is expressed as a fractional exponent.

[class="table-1"]

| | |
|--------|--------|
| $$\sqrt[n]{f(x)} = g(x)$$ | $$f(x)^{1/n} = g(x)$$ |
| $$\sqrt[n]{f(x)} = k$$ | $$f(x)^{1/n} = k$$ |
| $$\sqrt[n]{x^m}$$ | $$x^{m/n}$$ |

[/class]

> Roots set clear [limits](../limits/) on the [domain](../determining-the-domain-of-a-function/), and after removing radicals the candidate solutions must be checked. Algebraic steps may produce possible answers, but each one must be verified carefully.

## How to solve irrational equations

The strategy depends on the structure of the radical and on the position of the unknown within the expression. Despite these variations, the overall approach follows a few essential steps:

+ Determine the [domain](../determining-the-domain-of-a-function/) by considering whether the index of the root is even or odd, and impose the relevant conditions.
+ Eliminate the roots by raising both sides of the equation to the appropriate power.
+ Solve the resulting equation and check the admissibility of each solution by verifying that it belongs to the original domain and satisfies the initial equation.

## A closer look at the general forms

Irrational equations appear in several structural patterns, and recognising them is essential. The position of the variable inside a radical and the value of the index determine both the domain of definition and the algebraic manipulations that can be applied.

- - -

A first and very common case is that of an even index $n$. These equations have the general form:

$$\sqrt[n]{f(x)} = g(x), \quad n \in 2\mathbb{Z}$$

where $2\mathbb{Z}$ denotes the set of even [integers](../integers/). Since an even root is defined only for non-negative radicands, specific conditions of existence must be imposed before solving:

+ Impose the domain: $f(x) \ge 0$ and $g(x) \ge 0$.
+ Remove the radical by raising both sides to the power $n$.
+ Solve the resulting algebraic equation.
+ Check each solution in the original equation.
+ Keep only the values that satisfy all domain conditions.

> The condition $g(x) \ge 0$ must also be verified, since an even-index root produces only non-negative real values and cannot equal a negative quantity.

- - -

When the equation has the form:

$$\sqrt[n]{f(x)} = k$$

and $k$ is a non-negative real number, the domain of existence is given by the values of the variable satisfying:

$$f(x) \ge 0$$

Only for those values is the radicand well defined. To solve the equation:

+ Impose the domain condition $f(x) \ge 0$.
+ Remove the radical by raising both sides to the power $n$.
+ Solve the resulting algebraic equation.
+ Check each candidate solution in the original equation.
+ Keep only the values that satisfy the domain and the original equality.

- - -

If instead the equation has the form:

$$\sqrt[n]{f(x)} = k$$

with $k$ a negative real number, then the equation has no solution. An even-index radical cannot yield a negative value, so the equality cannot hold for any real value of the variable.

- - -

A more general situation arises when:

$$\sqrt[n]{f(x)} = g(x)$$

and $g(x)$ is a rational function. Determining the domain then requires analysing both sides. The admissible values of $x$ are those satisfying the following [system of inequalities](../systems-of-inequalities/):

$$
\begin{cases}
f(x) \ge 0 \\[6pt]
g(x) \ge 0
\end{cases}
$$

Once the domain is established, the equation can be transformed by raising both sides to the power $n$, giving the equivalent algebraic equation:

$$f(x) = \bigl(g(x)\bigr)^n$$

Under these conditions the radical is well defined, the equality is meaningful, and the resulting equation remains consistent with the original.

- - -

If the equation is written as:

$$f(x)^{1/n} = g(x), \quad n \in 2\mathbb{Z}$$

and $g(x)$ takes negative values for some real $x$, then the equation has no solution at those points. When $n$ is even, the expression $f(x)^{1/n}$ is an even-index root, which produces only non-negative real numbers. The equality cannot hold whenever $g(x) < 0$. Possible solutions exist only where $g(x) \ge 0$, and these must also satisfy $f(x) \ge 0$ so that the radicand is defined.

## Distinction between irrational and rational equations

The difference between irrational and [rational equations](../rational-equations/) lies in the way the variable $x$ appears within the expression. Rational equations are built from ratios of polynomials, so the unknown occurs only in the numerator or denominator of a fraction whose components are polynomial expressions. An example is:

$$\frac{2x}{2x - 1}$$

which remains entirely within the framework of rational expressions.

Irrational equations are instead characterised by the variable appearing inside a root or raised to a fractional exponent. They involve [radical](../radicals/) notation, often with an explicit index, and their structure introduces domain restrictions that must be considered before solving. A typical example is:

$$\frac{2x}{\sqrt{2x - 1}}$$

where the square root makes the equation irrational. Recognising whether an equation is rational or irrational is an essential first step, as each class requires different solving techniques and carries its own algebraic constraints.

## Roots with odd indexes

When the index $n$ of a radical is odd, the behaviour of the equation is particularly manageable. Unlike even roots, which restrict the radicand, an odd root can be evaluated for any real input. The expression therefore remains meaningful over the entire real line, without conditions limiting the domain. The possibility of extracting the root of a negative number greatly simplifies the structure of the equation.

If $n = 2k + 1$ is odd, the function:

$$x \longmapsto \sqrt[n]{x}$$

is defined for every $x \in \mathbb{R}$. This stems from the fact that raising a real number to an odd power always gives a real value, whether the number is positive, negative, or zero. Taking an odd root, the inverse operation, is therefore always possible and never introduces sign-related inconsistencies. A general irrational equation with an odd root can be written as:

$$\sqrt[n]{f(x)} = g(x), \quad n \in 2\mathbb{Z} + 1$$

and is transformed into an equivalent algebraic equation simply by raising both sides to the power $n$:

$$f(x) = \bigl(g(x)\bigr)^{n}$$

Here the radical imposes no additional inequalities such as $f(x) \ge 0$ or $g(x) \ge 0$; any restrictions arise only from expressions outside the radical, for instance denominators or further roots. A numerical example illustrates this:

$$\sqrt[3]{-8} = -2$$

because:

$$(-2)^3 = -8$$

More generally, for any real number $a$ and any odd index $n = 2k + 1$:

$$\sqrt[n]{a} = a^{1/n}$$

and the result remains real. This correspondence between odd-index radicals and fractional powers explains why irrational equations of this type can often be handled by direct algebraic manipulation, without the preliminary domain checks required in the even-index case.

## Keeping roots on opposite sides

When solving equations with roots, it is useful to keep the radicals on opposite sides of the equals sign. This prevents the introduction of extraneous solutions during exponentiation. Consider the irrational equation:

$$\sqrt{2x} - \sqrt{x + 1} = 0$$

- - -

Squaring the left-hand side directly introduces a mixed term that complicates the calculation:

$$
\begin{align}
&(\sqrt{2x} - \sqrt{x + 1})^2 = 0 \\[6pt]
&2x - (x + 1) + 2\sqrt{2x}\cdot\sqrt{x+1} = 0
\end{align}
$$

- - -

It is preferable to isolate the radicals on opposite sides before squaring:

$$
\begin{align}
&\sqrt{2x} = \sqrt{x + 1} \\[6pt]
&(\sqrt{2x})^2 = (\sqrt{x + 1})^2 \\[6pt]
&2x = x + 1 \\[6pt]
&2x - x = 1 \\[6pt]
&x = 1
\end{align}
$$

## Example 1

Solve the irrational equation:

$$\sqrt{x^2 - 2} = \sqrt{4x}$$

The equation has the form $\sqrt[n]{f(x)} = g(x)$ with even index $n$. The admissible set of solutions is determined by solving the [system of inequalities](../systems-of-inequalities/):

$$
\begin{cases}
f(x) \geq 0 \\[6pt]
g(x) \geq 0
\end{cases}
$$

Substituting the polynomials under the roots gives:

$$
\begin{cases}
x^2 - 2 \geq 0 \\[6pt]
4x \geq 0
\end{cases}
$$

Solving the [second-degree](../quadratic-equations/) inequality $x^2 - 2 \geq 0$ gives the solutions $x_{1,2} = \pm\sqrt{2}$, so the domain of the first [inequality](../inequalities/) consists of the intervals:

$$(-\infty, -\sqrt{2}] \ \cup \ [\sqrt{2}, +\infty)$$

The second inequality gives $x \geq 0$. The intersection of the two conditions gives the admissible set, which can be visualised with the graphical method:

[shortcode="intervals"]
|     | $-\sqrt{2}$ | $0$      | $+\sqrt{2}$ |     |
|:----|:-----------:|:--------:|:-----------:|:----|
|     | sign+r-o    |          | sign+l-o    |     |
|     |             | sign+l-o |             |     |
|     |             |          | sign+l-o-h  |     |
[/shortcode]

The system admits solutions in the interval $[\sqrt{2}, +\infty)$.

- - -

To solve the original equation, the radicals are isolated on opposite sides and both sides are squared:

$$
\begin{align}
&\sqrt{x^2 - 2} = \sqrt{4x} \\[6pt]
&x^2 - 2 = 4x \\[6pt]
&x^2 - 4x - 2 = 0
\end{align}
$$

This is a [quadratic equation](../quadratic-equations/), solved with the [quadratic formula](../quadratic-formula/):

$$
\begin{align}
x_{1,2} &= \frac{-(-4) \pm \sqrt{(-4)^2 - 4 \cdot 1 \cdot (-2)}}{2 \cdot 1} \\[6pt]
&= \frac{4 \pm \sqrt{16 + 8}}{2} \\[6pt]
&= \frac{4 \pm \sqrt{24}}{2} \\[6pt]
&= \frac{4 \pm 2\sqrt{6}}{2} \\[6pt]
&= 2 \pm \sqrt{6}
\end{align}
$$

- - -

Before verifying the solutions, we check whether they belong to the admissible set $[\sqrt{2}, +\infty)$:

+ $x_2 = 2 + \sqrt{6} \approx 4.449 \in [\sqrt{2}, +\infty)$
+ $x_1 = 2 - \sqrt{6} \approx -0.449 \notin [\sqrt{2}, +\infty)$

The value $x_1 = 2 - \sqrt{6}$ is an extraneous solution introduced during squaring and is discarded. It remains to verify that $x_2 = 2 + \sqrt{6}$ satisfies the original equation:

$$
\begin{align}
&\sqrt{(2 + \sqrt{6})^2 - 2} = \sqrt{4(2 + \sqrt{6})} \\[6pt]
&\sqrt{4 + 4\sqrt{6} + 6 - 2} = \sqrt{8 + 4\sqrt{6}} \\[6pt]
&\sqrt{8 + 4\sqrt{6}} = \sqrt{8 + 4\sqrt{6}}
\end{align}
$$

The equality holds. The solution of the equation is therefore:

$$x = 2 + \sqrt{6}$$
