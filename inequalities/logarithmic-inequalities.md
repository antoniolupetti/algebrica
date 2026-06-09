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

Logarithmic inequalities are [inequalities](../inequalities/) that involve one or more [logarithmic](../logarithms/) expressions, in which the unknown $x$ appears either in the argument of the logarithm or, in some cases, in the base itself. 

Before tackling logarithmic inequalities, it is essential to have a solid understanding of logarithms, their fundamental properties, and the standard methods used to solve [logarithmic equations](../logarithmic-equations/), as these tools are crucial for approaching and resolving such inequalities correctly.

- - -

Logarithmic inequalities may have the general form:

$$\log_a f(x) \lesseqgtr \log_a g(x)$$

+ $a$ is the base of the logarithm, with $a > 0$ and $a \neq 1.$
+ $f(x)$ and $g(x)$ are algebraic expressions depending on the variable $x.$
+ The symbol $\lesseqgtr$ denotes one of the relations $<$, $\le$, $>$, or $\ge.$

Moreover, for the inequality to be well defined, the arguments of both logarithms must be strictly positive:

$$\begin{cases}
f(x) > 0 \\[6pt]
g(x) > 0
\end{cases}$$

- - -

An inequality that contains a logarithmic expression in which the unknown variable does not appear in either the argument or the base of the logarithm is not a logarithmic inequality. Consider for instance the inequality:

$$\log_3(9) - 3x > 0$$

This is an ordinary [linear inequality](../linear-inequalities/), since the logarithmic term is a constant. By contrast, the inequality:

$$\log_3(9x) - 3x > 0$$

is a logarithmic inequality, because the variable $x$ appears inside the argument of the logarithm and directly affects its domain and behavior.

## How to solve logarithmic inequalities

The solution process is general, but for explanatory convenience let us consider an inequality of the form:

$$\log_a f(x) \ge \log_a g(x)$$

The procedure can be structured into four fundamental steps.

1. Determine the [domain](../determining-the-domain-of-a-function/) of the inequality by imposing the admissibility conditions. The argument of every logarithm must be strictly positive, which for the form above gives the system:

$$\begin{cases}
f(x) > 0 \\[6pt]
g(x) > 0
\end{cases}$$

2. If the inequality involves logarithms with different bases, rewrite all logarithmic terms in a common base using the change-of-base formula, and combine them by means of the [properties of logarithms](../logarithms/), so that the inequality takes the form of a comparison between two logarithms with the same base.

3. Use the monotonicity of the [logarithmic function](../logarithmic-function/) to remove the logarithms and reduce the problem to an equivalent algebraic inequality involving $f(x)$ and $g(x)$. If $a > 1$, the logarithmic function is [increasing](../increasing-and-decreasing-functions/) and the inequality preserves its direction when the logarithms are removed. If $0 < a < 1$, the logarithmic function is decreasing and the direction of the inequality must be reversed.

4. Solve the resulting algebraic inequality and intersect its solution set with the domain previously determined, discarding any values that do not satisfy the original logarithmic conditions.

- - -

The role played by the base of the logarithm follows from the behavior of the logarithmic function. When $a > 1$ the function $\log_a x$ is strictly increasing over its entire domain, so larger arguments produce larger logarithms and the comparison between logarithms translates directly into the same comparison between arguments. 

When $0 < a < 1$ the function is strictly decreasing, so larger arguments produce smaller logarithms and the comparison between arguments is reversed. In both cases the function is defined only for $x > 0$, has a vertical asymptote along the $y$-axis, and takes the value $0$ at $x = 1$, so the two graphs intersect at the point $(1, 0)$.

> Since the logarithmic function is strictly monotonic, hence injective, removing the logarithms produces an inequality that is equivalent to the original one within the domain. No solutions are gained or lost, provided the intersection with the domain is carried out.

## Comparing a logarithm with a constant

A frequent special case is the comparison between a single logarithm and a constant:

$$\log_a f(x) \lesseqgtr b$$

The constant can always be written as a logarithm in the same base, since $b = \log_a a^b$. The inequality then takes the standard form of a comparison between two logarithms, and the monotonicity rule applies. For $a > 1$ the inequality $\log_a f(x) > b$ is equivalent, within the domain, to $f(x) > a^b$, while for $0 < a < 1$ it is equivalent to $f(x) < a^b$.

As an illustration, consider the inequality:

$$\log_2(x - 1) < 3$$

The domain requires $x - 1 > 0$, that is $x > 1$. Writing $3 = \log_2 8$, the inequality becomes $\log_2(x - 1) < \log_2 8$. Since the base satisfies $2 > 1$, the function is increasing and the direction is preserved, which gives $x - 1 < 8$, that is $x < 9$. Intersecting with the domain, the solution set is the interval $(1, 9)$.

> The intersection with the domain is essential in this type of inequality. The condition $x - 1 < 8$ alone would admit values such as $x = 0$, for which the original logarithm is not defined.

## Example 1

Consider the logarithmic inequality, in which the base is greater than one:

$$\log_3(2x - 1) > \log_3(x + 1)$$

We begin by determining the domain. The argument of each logarithm must be strictly positive, which gives the following system.

$$\begin{cases}
2x - 1 > 0 \\[6pt]
x + 1 > 0
\end{cases}$$

The first condition gives $x > 1/2$ and the second gives $x > -1$. Their intersection, which is the domain of the inequality, is $x > 1/2$.

Next, we examine the base. Since $3 > 1$, the logarithmic function is strictly increasing, so removing the logarithms preserves the direction of the inequality. The original inequality is therefore equivalent to the following.

$$2x - 1 > x + 1$$

Solving this [linear inequality](../linear-inequalities/) gives $x > 2$. Intersecting with the domain $x > 1/2$ leaves the condition unchanged, since every value with $x > 2$ already satisfies $x > 1/2$.

Hence the solution set of the logarithmic inequality is the following.

$$x > 2$$

## Example 2

Consider the logarithmic inequality:

$$\log_{\frac{1}{2}}(x + 3) \ge \log_{\frac{1}{2}}(2x - 1)$$

We begin by determining the domain of the inequality. The arguments of the logarithms must be strictly positive:

$$\begin{cases}
x + 3 > 0 \\[6pt]
2x - 1 > 0
\end{cases}$$

The first condition gives $x > -3$ and the second gives $x > 1/2$. Using a graphical representation and considering the solution intervals of the [linear inequalities](../linear-inequalities/) in the previous system, we find that their intersection is precisely given by $x > 1/2$.

[shortcode="intervals"]
| | $-3$      | $1/2$   |     |
|----------------------|---------------|--------------------|-----|
| |               | sign+l-o           |     |
| | sign+l-o      |                    |     |
| |               | sign+l-o-h           |     |
[/shortcode]

Therefore, the domain $D$ of the original inequality is given by the following interval:

$$\left(\frac{1}{2}, +\infty\right)$$

- - -

Next, we analyze the base of the logarithm. Since the base satisfies:

$$0 < \frac{1}{2} < 1$$

the logarithmic function is strictly decreasing. As a consequence, when the logarithms are removed, the direction of the inequality must be reversed. Therefore, the given inequality:

$$\log_{\frac{1}{2}}(x + 3) \ge \log_{\frac{1}{2}}(2x - 1)$$

is equivalent to:

$$x + 3 \le 2x - 1$$

- - -

We now solve the resulting algebraic inequality. Subtracting $x$ from both sides and adding $1$ to both sides gives $4 \le x$, that is:

$$x \ge 4$$

Finally, we intersect this result with the domain previously determined. Since every value with $x \ge 4$ also satisfies $x > 1/2$, the intersection leaves the condition unchanged.

Hence, the solution set of the logarithmic inequality is:

$$x \ge 4$$

## Example 3

Consider the logarithmic inequality, in which the two logarithms have different bases:

$$\log_{\frac{1}{2}}(x+1) > \log_2(2-x)$$

We begin by determining the [domain](../determining-the-domain-of-a-function/). The arguments of the logarithms must be strictly positive, hence:

$$\begin{cases}
x+1 > 0 \\[6pt]
2-x > 0
\end{cases}$$

Using a graphical representation and considering the solution intervals of the linear inequalities in the previous system, we find that their intersection is given by $-1 < x < 2$.

[shortcode="intervals"]
| | $-1$     | $2$  |     |
|----------------------|---------------|--------------------|-----|
| |      sign+l-o      |           |     |
| |      |         sign+r-o            |     |
| |         sign+l-in-o-h  |   sign+r-in-o-h  |           |     |
[/shortcode]

Therefore, the domain $D$ of the original inequality is given by the following interval:

$$(-1, 2)$$

- - -

Next, we rewrite the logarithm with base $1/2$ in terms of base $2$. By the change-of-base formula, and since $\log_2 \frac{1}{2} = -1$, we have:

$$\log_{\frac{1}{2}}(x+1)
= \frac{\log_2(x+1)}{\log_2 \frac{1}{2}}
= -\log_2(x+1)$$

Substituting into the original inequality and multiplying both sides by $-1$, which reverses the direction, we obtain:

$$\log_2(x+1) < -\log_2(2-x)$$

Bringing all logarithmic terms to the same side, we get:

$$\log_2(x+1) + \log_2(2-x) < 0$$

By the sum property, stating that the [sum of two logarithms](../logarithms/) equals the logarithm of their product, the inequality can be rewritten as follows:

$$\log_2 \bigl((x+1)(2-x)\bigr) < 0$$

Writing $0 = \log_2 1$ and using the fact that the logarithmic function with base $2 > 1$ is strictly increasing, this inequality is equivalent, within the domain, to:

$$(x+1)(2-x) < 1$$

> Within the domain $(-1, 2)$ both factors are positive, so the condition $(x+1)(2-x) > 0$, required for the logarithm of the product to be defined, is automatically satisfied.

Expanding the product and bringing all terms to the same side, we obtain a [quadratic inequality](../quadratic-inequalities/):

$$x^2 - x - 1 > 0$$

The associated [quadratic equation](../quadratic-equations/) has roots:

$$x = \frac{1 \pm \sqrt{5}}{2}$$

Since the parabola opens upward, the inequality is satisfied outside the interval determined by these roots. Both roots lie inside the domain $(-1, 2)$, so intersecting with the domain we finally obtain the solution set:

$$-1 < x < \frac{1-\sqrt{5}}{2} \lor \frac{1+\sqrt{5}}{2} < x < 2$$

## Inequalities reducible to a polynomial by substitution

A frequent class of logarithmic inequalities contains the same logarithm more than once, often with one term squared. These inequalities are solved by introducing a new variable equal to the logarithm, which transforms the problem into an algebraic inequality. Consider the inequality:

$$\log_2^2 x - 3\log_2 x + 2 > 0$$

The domain requires $x > 0$. Setting $t = \log_2 x$, the inequality becomes a [quadratic inequality](../quadratic-inequalities/) in $t$:

$$t^2 - 3t + 2 > 0$$

The associated quadratic equation factors as $(t - 1)(t - 2) = 0$, so the roots are $t_1 = 1$ and $t_2 = 2$. The parabola opens upward, so the expression is positive on the two outer intervals:

$$t < 1 \lor t > 2$$

Reversing the substitution $t = \log_2 x$ yields two elementary logarithmic inequalities, namely $\log_2 x < 1$ and $\log_2 x > 2$. Since the base satisfies $2 > 1$, the first gives $x < 2$ and the second gives $x > 4$. Intersecting with the domain $x > 0$, the complete solution is the union of the two intervals:

$$(0, 2) \cup (4, +\infty)$$

> Unlike the substitution $t = a^x$ used for [exponential inequalities](../exponential-inequalities/), the substitution $t = \log_a x$ imposes no sign restriction on $t$, since the logarithm takes every real value. The constraint on the original variable comes entirely from the domain $x > 0$.

## Inequalities with the unknown in the base

In the cases treated so far the base of the logarithm is a fixed constant. When the unknown appears in the base, as in an inequality of the following form, two further considerations arise:

$$\log_{h(x)} f(x) > c$$

The base must satisfy the admissibility conditions $h(x) > 0$ and $h(x) \neq 1$, which restrict the domain. In addition, the direction of the inequality after the logarithm is removed is no longer fixed in advance, since the monotonicity of $\log_{h(x)}$ depends on whether the base is greater than or smaller than one. The problem therefore splits into two cases according to the position of $h(x)$ relative to $1$.

As an illustration, consider the following inequality.

$$\log_x 4 \ge 1$$

The base conditions require $x > 0$ and $x \neq 1$. Writing $1 = \log_x x$, the inequality takes the form $\log_x 4 \ge \log_x x$, and the analysis proceeds by cases on the base.

When $x > 1$ the logarithm is increasing, so the direction is preserved and the inequality reduces to $4 \ge x$. Combined with $x > 1$, this case gives $1 < x \le 4$.

When $0 < x < 1$ the logarithm is decreasing, so the direction is reversed and the inequality becomes $4 \le x$. This is incompatible with $0 < x < 1$, so this case contributes no solution.

Collecting the two cases, the solution set is the interval $(1, 4]$.