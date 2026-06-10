---
title: Logarithmic Inequalities
source: https://algebrica.org/logarithmic-inequalities/
license: CC BY-NC 4.0
tags:
  - inequalities
  - logarithmic-function
  - logarithms
  - monotonicity
---

## Introduction

Logarithmic inequalities are [inequalities](../inequalities/) in which the unknown appears inside a [logarithm](../logarithms/), either in the argument or, in some cases, in the base. They take the general form:

$$\log_a f(x) > \log_a g(x)$$

or, in the simpler cases, the form:

$$\log_a f(x) > b$$

The same definitions apply with the symbols $<$, $\geq$ and $\leq$ in place of $>$. The base $a$ must satisfy $a > 0$ and $a \neq 1$, the same admissibility conditions required for [logarithmic equations](../logarithmic-equations/). In addition, the argument of every logarithm must be strictly positive, because the [logarithmic function](../logarithmic-function/) is defined only on the positive real numbers. This requirement gives logarithmic inequalities a feature that exponential ones do not have, since the solution process must always begin by determining a domain.

The resolution rests on the monotonicity of the logarithmic function. When $a > 1$ the function $\log_a x$ is strictly increasing, so larger arguments produce larger logarithms. 

When $0 < a < 1$ the function is strictly [decreasing](../increasing-and-decreasing-functions/), so larger arguments produce smaller logarithms. The comparison between two logarithms with the same base therefore translates into a comparison between the arguments, with the same direction in the first case and the opposite direction in the second.

## How to solve logarithmic inequalities

The solution of an inequality of the form $\log_a f(x) > \log_a g(x)$ can be organized into four steps.

+ Determine the [domain](../determining-the-domain-of-a-function/) by requiring that the argument of every logarithm be strictly positive, which gives the system $f(x) > 0$ and $g(x) > 0$.
+ If the inequality involves logarithms with different bases, rewrite all logarithmic terms in a common base through the change-of-base formula and combine them using the properties of logarithms.
+ Remove the logarithms by monotonicity. If $a > 1$ the inequality between the arguments keeps the direction of the original one, while if $0 < a < 1$ the direction reverses.
+ Solve the resulting algebraic inequality and intersect its solution set with the domain found in the first step.

Since the logarithmic function is strictly monotonic, removing the logarithms produces an inequality that is equivalent to the original one within the domain. No solutions are gained or lost, provided that the final intersection with the domain is carried out.

The intersection in the last step is not a formality. The algebraic inequality obtained after removing the logarithms is generally satisfied by values for which the original logarithms are not even defined, and these values must be discarded.

## Comparing a logarithm with a constant

A frequent special case is the comparison between a single logarithm and a constant. The constant can always be written as a logarithm in the same base, since $b = \log_a a^b$, after which the monotonicity rule applies. Consider the inequality:

$$\log_3(2x + 5) \leq 2$$

The domain requires $2x + 5 > 0$, that is $x > -\frac{5}{2}$. Writing $2 = \log_3 9$ brings the inequality to a comparison between two logarithms with base $3 > 1$, so the direction is preserved when the logarithms are removed:

$$
\begin{align}
&2x + 5 \leq 9 \\[6pt]
&x \leq 2
\end{align}
$$

Intersecting with the domain gives the solution set $\left(-\frac{5}{2}, 2\right]$.

- - -

The same procedure with a base between zero and one requires the reversal of the inequality. Consider:

$$\log_{\frac{1}{2}}(x + 1) \geq -2$$

The domain requires $x > -1$. Writing $-2 = \log_{\frac{1}{2}} 4$, since $\left(\frac{1}{2}\right)^{-2} = 4$, and using the fact that the base lies strictly between zero and one, the comparison between the arguments reverses direction, giving $x + 1 \leq 4$, that is $x \leq 3$. Intersecting with the domain gives the solution set $(-1, 3]$.

> The lower endpoint of the solution comes from the domain and the upper endpoint from the inequality itself. Forgetting the domain would incorrectly admit values such as $x = -1$, for which the logarithm is not defined.

## Example 1

We solve a logarithmic inequality with the same base on both sides, greater than one:

$$\log_2(x^2 - 3) > \log_2(2x)$$

The domain requires both arguments to be strictly positive:

$$\begin{cases}
x^2 - 3 > 0 \\[6pt]
2x > 0
\end{cases}$$

The first condition gives $x < -\sqrt{3}$ or $x > \sqrt{3}$, the second gives $x > 0$. Their intersection is $x > \sqrt{3}$, which is the domain of the inequality.

The base is $2 > 1$, so the logarithmic function is strictly increasing and removing the logarithms preserves the direction:

$$
\begin{align}
&x^2 - 3 > 2x \\[6pt]
&x^2 - 2x - 3 > 0
\end{align}
$$

The resulting [quadratic inequality](../quadratic-inequalities/) has associated equation $(x + 1)(x - 3) = 0$, with roots $x_1 = -1$ and $x_2 = 3$. The parabola opens upward, so the trinomial is positive on the two outer intervals, $x < -1$ or $x > 3$. Intersecting with the domain $x > \sqrt{3}$ eliminates the entire branch $x < -1$ and trims the other, leaving the solution set:

$$(3, +\infty)$$

[shortcode="intervals"]
| | $-1$            | $\sqrt{3}$       |     $3$      |     |
|-|---------------|----------|-----------|-----|
| |  sign+r-o     |          | sign+l-o   |     |
| |               | sign+l-o |            |     |
| |               |          | sign+l-o-h |     |
[/shortcode]

> The branch $x < -1$ satisfies the algebraic inequality but contains no admissible value, since $2x$ is negative there. This is the typical way in which the domain reshapes the solution of a logarithmic inequality.

## Example 2

We solve an inequality whose base lies between zero and one:

$$\log_{\frac{1}{3}}(x - 2) > \log_{\frac{1}{3}}(8 - x)$$

The domain requires both arguments to be strictly positive:

$$\begin{cases}
x - 2 > 0 \\[6pt]
8 - x > 0
\end{cases}$$

The first condition gives $x > 2$ and the second gives $x < 8$, so the domain is the interval $(2, 8)$.

The base is $1/3$, which lies strictly between zero and one, so the logarithmic function is strictly decreasing and the comparison between the arguments reverses direction:

$$
\begin{align}
&x - 2 < 8 - x \\[6pt]
&2x < 10 \\[6pt]
&x < 5
\end{align}
$$

Intersecting with the domain $(2, 8)$ gives the solution set:

$$(2, 5)$$

[shortcode="intervals"]
| | $2$             | $5$       |     $8$      |     |
|-|---------------|----------|-----------|-----|
| |  sign+l-o     |          | sign+r-o   |     |
| |               | sign+r-o |            |     |
| | sign+l-in-o-h | sign+r-in-o-h  |      |     |
[/shortcode]

A quick check confirms the result. For $x = 3$ the inequality compares $\log_{\frac{1}{3}} 1 = 0$ with $\log_{\frac{1}{3}} 5$, which is negative, and the comparison holds. For $x = 6$ it compares $\log_{\frac{1}{3}} 4$ with $\log_{\frac{1}{3}} 2$, and the first is the smaller of the two, so the inequality fails.

## Reduction to a common base

When the logarithms appearing in the inequality have different bases, the [change-of-base formula](../logarithms/) brings every term to a single base, after which the usual procedure applies. Consider the inequality:

$$\log_4 x + \log_2 x \geq 3$$

The domain requires $x > 0$. The first term can be rewritten in base $2$, since:

$$\log_4 x = \frac{\log_2 x}{\log_2 4} = \frac{1}{2}\log_2 x$$

Substituting into the inequality and collecting the logarithmic terms gives:

$$
\begin{align}
&\frac{1}{2}\log_2 x + \log_2 x \geq 3 \\[6pt]
&\frac{3}{2}\log_2 x \geq 3 \\[6pt]
&\log_2 x \geq 2
\end{align}
$$

The base is $2 > 1$, so passing to the arguments preserves the direction and gives $x \geq 2^2 = 4$. The bound lies inside the domain, so the solution set is the half-line:

$$[4, +\infty)$$

> The multiplication by $\frac{2}{3}$ in the last step preserves the direction of the inequality because the factor is positive. Multiplying an inequality by a negative constant, as can happen when the change of base produces a negative coefficient, reverses the direction instead.

## Inequalities reducible to a polynomial by substitution

A frequent class of logarithmic inequalities contains the same logarithm more than once, often with one term squared. These inequalities are solved by introducing a new variable equal to the logarithm, which transforms the problem into an algebraic inequality. Consider the inequality:

$$\ln^2 x - \ln x - 6 \leq 0$$

The domain requires $x > 0$. Setting $t = \ln x$, the inequality becomes a [quadratic inequality](../quadratic-inequalities/) in the auxiliary variable:

$$t^2 - t - 6 \leq 0$$

The associated equation factors as $(t + 2)(t - 3) = 0$, with roots $t_1 = -2$ and $t_2 = 3$. The parabola opens upward, so the trinomial is non-positive between the roots:

$$-2 \leq t \leq 3$$

Reversing the substitution $t = \ln x$ gives the double inequality $-2 \leq \ln x \leq 3$. Since the natural logarithm is strictly increasing, passing to the arguments preserves both comparisons, and the unknown satisfies:

$$e^{-2} \leq x \leq e^{3}$$

Both endpoints are positive, so the entire interval lies inside the domain and the solution set is the closed interval $[e^{-2}, e^{3}]$.

> Unlike the substitution $t = a^x$ used for [exponential inequalities](../exponential-inequalities/), the substitution $t = \log_a x$ imposes no sign restriction on $t$, since the logarithm takes every real value. Here the negative value $t = -2$ is fully admissible and produces the endpoint $x = e^{-2}$. The constraint on the original variable comes entirely from the domain $x > 0$.

## Inequalities with the unknown in the base

When the unknown appears in the base of the logarithm, the admissibility conditions $h(x) > 0$ and $h(x) \neq 1$ restrict the domain, and the direction of the inequality after the logarithms are removed is no longer fixed in advance. The monotonicity of $\log_{h(x)}$ depends on whether the base is greater than or smaller than one, so the problem splits into two cases. Consider the inequality:

$$\log_x 9 < 2$$

The base conditions require $x > 0$ and $x \neq 1$. Writing $2 = \log_x x^2$ brings the inequality to a comparison between two logarithms in the same base, and the analysis proceeds by cases.

When $x > 1$ the logarithm is strictly increasing, so the direction is preserved and the inequality reduces to $9 < x^2$. For positive values this means $x > 3$, and combined with $x > 1$ the first case gives $x > 3$.

When $0 < x < 1$ the logarithm is strictly decreasing, so the direction reverses and the inequality becomes $9 > x^2$, that is $x < 3$ for positive values. Every number in $(0, 1)$ satisfies this condition, so the second case contributes the whole interval $(0, 1)$.

Collecting the two cases, the solution set is the union:

$$(0, 1) \cup (3, +\infty)$$

> The interval $(0, 1)$ may look surprising at first sight, but for a base between zero and one the logarithm of $9$ is negative, and a negative number is certainly smaller than $2$. The case analysis captures this behavior automatically.

## Structure of the solution set and the role of the domain

The solution set of a logarithmic inequality is a finite union of intervals contained in the domain, possibly empty. The elementary inequality $\log_a x > b$ with $a > 1$ has the solution $x > a^b$, a half-line whose endpoint is always positive, while with $0 < a < 1$ it has the solution $0 < x < a^b$, a bounded interval anchored at zero by the domain. In both cases the boundary $x = a^b$ is the unique point where the logarithm equals $b$, a consequence of the injectivity of the logarithmic function.

The domain plays a more active role here than in [exponential inequalities](../exponential-inequalities/), where the unknown can take any real value. Algebraic manipulations such as the product and quotient rules can enlarge the set of values satisfying the transformed inequality, exactly as they introduce extraneous solutions in [logarithmic equations](../logarithmic-equations/). The intersection with the domain determined at the outset is therefore an integral part of the method, not a final verification that can be omitted.
