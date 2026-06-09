---
title: Rational Inequalities
source: https://algebrica.org/rational-inequalities/
license: CC BY-NC 4.0
tags:
  - multiplicity
  - rational-inequality
  - sign-chart
  - zeros
---
## Introduction

A rational inequality is an inequality that involves at least one rational expression, that is, a ratio in which both the numerator and the denominator are [polynomials](../polynomials/). The natural domain of such an expression is the set of all real numbers for which the denominator does not vanish; any value of $x$ that makes the denominator equal to zero is excluded from the domain and cannot belong to the solution set. Every rational inequality can be reduced to one of the following canonical forms.

$$\frac{P(x)}{Q(x)} > 0 \qquad \frac{P(x)}{Q(x)} \geq 0$$

$$\frac{P(x)}{Q(x)} < 0 \qquad \frac{P(x)}{Q(x)} \leq 0$$

In each case, $P(x)$ and $Q(x)$ are polynomials with real coefficients, and the expression on the left-hand side is defined only where $Q(x) \neq 0$. These inequalities take their name from the notion of a rational function, in the same way that [rational equations](../rational-equations/) do. All four forms are handled by the same method, as illustrated in the examples below.

- - -

Solving a rational inequality means finding all values of $x$ in the natural domain of the expression for which the inequality holds. The standard approach proceeds through the following steps.

+ The first step is to rewrite the inequality so that all terms appear on the left-hand side and the right-hand side is zero, thereby reducing the problem to one of the canonical forms above. This allows one to study the sign of a single rational expression rather than comparing two separate expressions.
+ The second step is to determine the natural [domain](../determining-the-domain-of-a-function/) of the rational expression by identifying all values of $x$ for which the denominator vanishes. These values must be excluded from the solution set regardless of the inequality symbol.
+ The third step is to find the zeros of the numerator and the zeros of the denominator separately. These critical points, taken together, partition the real line into open intervals on which the rational expression maintains a constant sign, since the sign of a ratio can change only where the numerator or the denominator equals zero.
+ The fourth step is to construct a [sign chart](../sign-analysis-in-inequalities/), recording the sign of the numerator and the sign of the denominator in each interval, and then determining the sign of the ratio by the standard rule: the ratio is positive when numerator and denominator share the same sign, and negative when they have opposite signs.
+ The fifth step is to collect the intervals where the sign of the expression is consistent with the original inequality, taking care to include the zeros of the numerator if and only if the inequality is non-strict, and to exclude in every case the zeros of the denominator.

> The key observation underlying this method is that a rational expression $P(x)/Q(x)$ can change sign only at a zero of $P(x)$ or at a zero of $Q(x)$. Between any two consecutive critical points, the expression is either strictly positive or strictly negative throughout, which makes it sufficient to test a single representative value in each interval.

## Multiplicity and sign changes

The multiplicity of each zero is crucial in determining how the sign of a rational expression changes across its critical points. A zero of odd multiplicity, whether located in the numerator or denominator, causes the expression to change sign as $x$ crosses that point. The expression is positive on one side and negative on the other.

In contrast, a zero of even multiplicity does not produce a sign change. The expression maintains the same sign on both sides of that point because the corresponding factor contributes an even power, which does not change sign in a neighbourhood of the zero.

This behaviour must be explicitly considered when constructing the sign chart. Treating all critical points as sign-change points, regardless of multiplicity, is a common error that yields incorrect solution sets when repeated factors appear in the numerator or denominator.

- - -

Consider the following inequality, which demonstrates the effect of even multiplicity on the sign chart.

$$\frac{(x-1)^2}{x-3} \geq 0$$

The denominator vanishes at $x = 3$, which must therefore be excluded from the solution set regardless of the inequality symbol, since the expression is undefined at that point. The natural domain is thus the set of all real numbers with $x \neq 3$. The numerator vanishes at $x = 1$, which is a zero of multiplicity two. The critical points are $x = 1$ and $x = 3$, and they partition the real line into three intervals.

[class="table-sign"]

|                                  |                      |       $$1$$        |       $$3$$        |
| :------------------------------- | :------------------: | :------------------: | :------------------: |
| $$(x-1)^2 \geq 0$$             | $\boldsymbol{+}$ | $\boldsymbol{+}$ | $\boldsymbol{+}$ |
| $$x - 3 \geq 0$$               | $\boldsymbol{-}$ | $\boldsymbol{-}$ | $\boldsymbol{+}$ |
| $$\frac{(x-1)^2}{x-3} \geq 0$$ | $\boldsymbol{-}$ | $\boldsymbol{-}$ | $\boldsymbol{+}$ |
[/class]

Since $(x-1)^2$ is non-negative for all real $x$ and equals zero only at $x = 1$, it does not change sign as $x$ crosses $x = 1$. The sign of the entire expression is therefore determined solely by the sign of the denominator $x - 3$.

The expression is positive when $x > 3$, and it equals zero at $x = 1$. The point $x = 3$ is excluded from the solution set because it does not belong to the natural domain of the expression. The solution set is as follows.

$$\{1\} \cup (3, +\infty)$$

The point $x = 1$ appears as an isolated point in the solution set, a consequence of the even multiplicity of the corresponding zero.

- - -

The same reasoning applies when the zero of even multiplicity is located in the denominator, with one difference, the point must be removed from the solution set instead of being added as an isolated point. Consider the following inequality.

$$\frac{x + 1}{(x - 2)^2} > 0$$

The factor $(x-2)^2$ is positive for every $x \neq 2$, so the sign of the expression coincides with the sign of the numerator $x + 1$ throughout the natural domain. The expression is therefore positive for $x > -1$, except at the point $x = 2$, where it is undefined. The solution set is the following.

$$(-1, 2) \cup (2, +\infty)$$

The zero of the denominator does not produce a sign change, yet it must be excluded from the solution set, which leaves a punctured interval.

## Structure of the solution set

The solution set of a rational inequality is always a union of intervals of the real line, possibly supplemented by isolated points. Each interval in the solution set is bounded by critical points, and its endpoints are either zeros of the numerator, which may be included if the inequality is non-strict, or zeros of the denominator, which are always excluded. When a zero of even multiplicity appears in the numerator, it contributes an isolated point to the solution set rather than an interval, as discussed in the preceding section on multiplicity and sign changes.

To make this concrete, consider a rational expression with critical points at $x = 1$, $x = 2$, and $x = 4$, where $x = 2$ is a zero of the denominator. If the sign chart shows that the expression is non-negative on $[1, 2)$ and on $(2, 4]$, the solution set is the following.

$$[1, 2) \cup (2, 4]$$

The point $x = 2$ is absent from both intervals because it does not belong to the natural domain of the expression, even though the adjacent intervals extend up to it from both sides.

## Example 1

Determine the values of $x$ that satisfy the following inequality.

$$\frac{x - 1}{2 - x} < 0$$

The inequality is already in canonical form. The denominator $2 - x$ vanishes at $x = 2$, so this value must be excluded from the solution set. The natural domain of the expression is the following.

$$D = \{\ x \in \mathbb{R} : x \neq 2 \ \}$$

To determine the intervals where the inequality is satisfied, we use the fact that a rational expression is negative exactly when the numerator and the denominator have opposite signs. The numerator $x - 1$ is negative when $x < 1$, while the denominator $2 - x$ is negative when $x > 2$. By constructing the [sign chart](../sign-analysis-in-inequalities/), we obtain:

[class="table-sign"]

|                           |              |      $$1$$             |     $$2$$              |   
|:-------------------------|:------------------------:|:------------------------:|:-------------------------:|
| $$x - 1 \lt 0$$       | $\boldsymbol{-}$   | $\boldsymbol{+}$   | $\boldsymbol{+}$    |
| $$2 - x \lt 0$$       | $\boldsymbol{+}$   | $\boldsymbol{+}$   | $\boldsymbol{-}$    |
| $$\frac{x-1}{2-x} \lt 0$$ | $\boldsymbol{-}$ | $\boldsymbol{+}$   | $\boldsymbol{-}$    |
[/class]

From the sign chart, the expression is negative on the intervals $x < 1$ and $x > 2$. Since the inequality is strict, the endpoints are excluded, and the solution set is the following:

$$(-\infty, 1) \cup (2, +\infty)$$

## Example 2

Determine the values of $x$ that satisfy the following inequality.

$$\frac{x - 1}{x^2 - 5x + 6} \geq 0$$

The denominator is a quadratic polynomial whose zeros are found by solving the associated [quadratic equation](../quadratic-equations/), in the same spirit as a [quadratic inequality](../quadratic-inequalities/). The polynomial [factors](../factoring-quadratic-equations/) as follows.

$$(x-2)(x-3) = 0$$

This gives $x = 2$ and $x = 3$, which are the values that make the denominator zero and must therefore be excluded from the solution set. The natural domain is the following.

$$D = \{\ x \in \mathbb{R} : x \neq 2, x \neq 3 \ \}$$

The numerator vanishes at $x = 1$, which together with $x = 2$ and $x = 3$ gives three critical points partitioning the real line into four open intervals. We now represent their signs on a [sign chart](../sign-analysis-in-inequalities/):

[class="table-sign"]

|             |      | $$1$$   | $$2$$     |    $$3$$      |
|:-----------|:------------------:|:------------:|:----------------:|:----------------:|
| $$x-1 \geq 0$$ | $\boldsymbol{-}$ | $\boldsymbol{+}$  |  $\boldsymbol{+}$  |  $\boldsymbol{+}$ |
| $$x^2 - 5x + 6 \geq 0$$ |  $\boldsymbol{+}$ |$\boldsymbol{+}$  | $\boldsymbol{-}$  | $\boldsymbol{+}$  |
| $$\frac{x - 1}{x^2 - 5x + 6} \geq 0$$ | $\boldsymbol{-}$  | $\boldsymbol{+}$ |  $\boldsymbol{-}$  | $\boldsymbol{+}$ | 
[/class]

From the sign chart, the expression is non-negative on the interval $1 \leq x < 2$ and on the interval $x > 3$. The endpoints $x = 2$ and $x = 3$ are excluded because they do not belong to the natural domain, while $x = 1$ is included because the inequality is non-strict and the numerator vanishes there. The solution set is the following:

$$[1, 2) \cup (3, +\infty)$$

## Reduction to canonical form

The method described above assumes that the inequality is already in canonical form, with a single rational expression on the left-hand side and zero on the right. In practice, inequalities do not always appear in this form. A common case is one in which a rational expression appears on both sides, such as the following.

$$\frac{2x + 1}{x - 3} \geq \frac{1}{x + 1}$$

The correct approach is to move all terms to the left-hand side and combine them into a single rational expression. Subtracting the right-hand side from both sides gives the following.

$$\frac{2x + 1}{x - 3} - \frac{1}{x + 1} \geq 0$$

The two fractions are then combined over a common denominator.

$$\frac{(2x + 1)(x + 1) - (x - 3)}{(x - 3)(x + 1)} \geq 0$$

Expanding the numerator yields the following.

$$\frac{2x^2 + 3x + 1 - x + 3}{(x - 3)(x + 1)} \geq 0$$

which simplifies to the following.

$$\frac{2x^2 + 2x + 4}{(x - 3)(x + 1)} \geq 0$$

The numerator $2x^2 + 2x + 4$ can be written as $2(x^2 + x + 2)$. The discriminant of $x^2 + x + 2$ is $\Delta = 1 - 8 = -7 < 0$, so the quadratic has [no real roots](../quadratic-equations-with-complex-solutions/) and is strictly positive for all real $x$. The sign of the entire expression is therefore determined solely by the sign of the denominator $(x-3)(x+1)$, which is positive when $x < -1$ or $x > 3$. Since the numerator is never zero, neither endpoint can be included, and the solution set is the following.

$$(-\infty, -1) \cup (3, +\infty)$$

The same reduction applies when the right-hand side is a nonzero constant, as in $\frac{x+2}{x-1} \leq 2$. Subtracting the constant and combining over the common denominator $x - 1$ again produces a single rational expression compared with zero, after which the sign chart proceeds as usual.

A common error in this type of problem is to multiply both sides of the original inequality by $x - 3$ or $x + 1$ without accounting for the sign of those factors. Since the sign of a linear expression depends on $x$, such a multiplication would require a case analysis and is more error-prone than the reduction to canonical form illustrated above.

A further caution concerns common factors between numerator and denominator. The natural domain must be determined before any cancellation, because a cancelled factor still excludes its zero from the domain. Consider the following inequality.

$$\frac{(x - 1)(x + 2)}{x - 1} > 0$$

For $x \neq 1$ the expression equals $x + 2$, so the simplified inequality $x + 2 > 0$ holds on $x > -2$. The point $x = 1$ does not belong to the natural domain and must be removed even after the cancellation, so the solution set is the following.

$$(-2, 1) \cup (1, +\infty)$$

Cancelling first and forgetting the excluded value would produce the incorrect answer $(-2, +\infty)$, which contains the point $x = 1$ where the original expression is undefined.

## The reciprocal rule

A particular class of rational inequalities involves the reciprocal of a function of the unknown, in the form $1/f(x) > k$ or in the comparison $1/f(x) > 1/g(x)$. These inequalities deserve a separate discussion because the temptation to take reciprocals of both sides directly is a frequent source of error.

The interaction between the reciprocal and the [order relation](../properties-of-real-numbers/) is governed by the following rule. For any real numbers $a$ and $b$ with the same sign and $a < b$:

$$0 < a < b \quad \Longrightarrow \quad \frac{1}{b} < \frac{1}{a}$$

$$a < b < 0 \quad \Longrightarrow \quad \frac{1}{b} < \frac{1}{a}$$

In both cases the direction of the inequality is reversed when the reciprocal is taken. The same conclusion does not hold when $a$ and $b$ have opposite signs, since the reciprocals then differ in sign and the direction of the original relation cannot be transferred to the reciprocals.

Consider the inequality:

$$\frac{1}{x} > 4$$

A naive application of the reciprocal rule would suggest $x < \frac{1}{4}$, but this conclusion is incorrect because the rule applies only when both sides are known to have the same sign. The condition $\frac{1}{x} > 4$ requires $\frac{1}{x}$ to be positive, which in turn requires $x > 0$, so a case analysis based on the sign of $x$ is built into the reasoning. The correct procedure follows the canonical method: move every term to one side and combine over a common denominator.

$$\frac{1}{x} - 4 > 0$$

Combining the two terms over the common denominator $x$ gives the following.

$$\frac{1 - 4x}{x} > 0$$

The critical points are $x = 0$ and $x = \frac{1}{4}$. The sign chart on the numerator and the denominator gives the following.

[class="table-sign"]

|                          |          | $$0$$            | $$\frac{1}{4}$$  |
| :----------------------- | :------: | :--------------: | :--------------: |
| $$1 - 4x > 0$$           | $\boldsymbol{+}$ | $\boldsymbol{+}$ | $\boldsymbol{-}$ |
| $$x > 0$$                | $\boldsymbol{-}$ | $\boldsymbol{+}$ | $\boldsymbol{+}$ |
| $$\frac{1 - 4x}{x} > 0$$ | $\boldsymbol{-}$ | $\boldsymbol{+}$ | $\boldsymbol{-}$ |
[/class]

The ratio is positive on the open interval $\left(0, 1/4\right)$, which is the correct solution set. The naive reciprocal procedure would have produced the larger set $\left(-\infty, 1/4\right)$, introducing every $x < 0$ as an extraneous solution, since the inequality $1/x > 4$ is automatically false on $x < 0$ where the left-hand side is negative.

> The reciprocal rule and its operational use are particular cases of the more general phenomenon analysed in the entry on [loss and introduction of solutions](../loss-of-solutions/). The reduction to canonical form is the systematic countermeasure and replaces the case analysis on the sign of the variable expression with a single sign chart on the numerator and the denominator.
