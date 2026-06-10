---
title: Systems of Inequalities
source: https://algebrica.org/systems-of-inequalities/
license: CC BY-NC 4.0
tags:
  - inconsistent-systems
  - intersection-of-solution-sets
  - linear-inequalities
  - systems-of-inequalities
---
## Definition

A system of inequalities is a collection of two or more [inequalities](../inequalities/) involving one or several variables that must hold simultaneously. The solution of the system is the set of all values of the variables that satisfy all inequalities simultaneously, that is, the intersection of the solution sets associated with the individual inequalities.

In this section we focus on systems in a single real variable $x$. Such systems can be written in the general form:

$$
\begin{cases}
f_1(x) \geq 0 \\[6pt]
f_2(x) \geq 0 \\[6pt]
\quad \quad \vdots \\[6pt]
f_k(x) \geq 0
\end{cases}
$$

In this expression each $f_i(x)$ is a function or an expression in the variable $x$, and the relation in each row can be any of the inequality signs $<$, $\leq$, $>$, $\geq$.

> The brace on the left expresses a logical conjunction, since every inequality in the system must be satisfied at once. This is the reason why the solution sets of the individual inequalities are combined by intersection and not by union.

A system admitting no solutions is called an inconsistent system. If even a single inequality in the system has an empty solution set, the entire system is inconsistent. The converse does not hold, because a system can be inconsistent even when each inequality, taken on its own, admits solutions, provided the individual solution sets have no point in common.

In the section on [linear inequalities](../linear-inequalities/) we have seen that solving [inequalities involving the absolute value](../inequalities-with-absolute-value/) leads to systems of inequalities. The following example shows how a system of linear inequalities is solved in practice.

## Example 1

Consider the following system of linear inequalities:

$$
\begin{cases}
3x + 6 > 0 \\[6pt]
x - 3 \geq 0 \\[6pt]
9 - x > 0
\end{cases}
$$

We need to determine the values of $x$ that satisfy all three inequalities simultaneously, so we begin by solving each inequality separately.

In the first inequality, subtracting $6$ from both sides gives $3x > -6$. Dividing both sides by $3$, which is positive and therefore preserves the direction of the inequality, yields $x > -2$.

The second inequality requires only adding $3$ to both sides, which yields $x \geq 3$.

In the third inequality, subtracting $9$ from both sides gives $-x > -9$. Multiplying both sides by $-1$ reverses the direction of the inequality and yields $x < 9$.

The three solution sets are therefore $x > -2$, $x \geq 3$, and $x < 9$. The solution of the system consists of the values common to all three. Representing the three intervals on the real line makes the intersection immediately visible.

[shortcode="intervals"]
|     | $-2$                 | $3$           | $9$                |     |
|:----|----------------------|---------------|--------------------|-----|
|     | sign+l-o             |               |                    |     |
|     |                      | sign+l-c      |                    |     |
|     |                      |               | sign+r-o           |     |
|     |                      | sign+l-in-c-h | sign+r-in-o-h      |     |
[/shortcode]

The solution of the system is the half-open interval:

$$x \in [3, 9)$$

This interval includes $3$, because the second inequality is not strict, and excludes $9$, because the third inequality is strict.

> For a detailed discussion of the structure and interpretation of intervals on the real line, refer to the [dedicated entry](../determining-the-domain-of-a-function/).

## General strategy for solving systems of inequalities

The system in the previous example is a very simple one, consisting of three linear inequalities in the variable $x$. Systems of inequalities can be considerably more complex and may involve rational expressions, [roots](../radicals/), [powers](../powers/), [logarithms](../logarithms/), exponentials, and [trigonometric functions](../sine-and-cosine/).

Although the resolution of each inequality depends on the specific form and properties of the functions involved, the governing principle remains the same, the admissible values are those satisfying all inequalities in the system simultaneously, that is, the intersection of their individual solution sets.

The resolution of a system of inequalities follows a well-defined sequence of steps:

+ Solve each inequality individually and determine its solution set.
+ When appropriate, represent the solution sets on the real line in order to visualize the resulting intervals.
+ Identify the intersection of all the solution sets, since only the values shared by every inequality satisfy the system.
+ Express the final solution in interval notation, ensuring that inclusions and exclusions at the endpoints are correctly indicated.

> This procedure provides a dependable framework that adapts to a wide variety of problems. As the complexity of the functions involved increases, the same principles continue to guide the analysis, and each step remains logically grounded.

## Example 2

Consider the following system, in which the first inequality involves logarithms:

$$
\begin{cases}
\log_2(2x+4) > \log_2(x) \\[6pt]
x - 2 > 0
\end{cases}
$$

Before solving the first inequality, we need to determine the [domain](../determining-the-domain-of-a-function/) of the logarithmic expressions, since a logarithm is defined only when its argument is greater than zero. This requirement produces two conditions.

$$
\begin{align}
2x + 4 > 0 \ &\rightarrow \ x > -2 \\[6pt]
x > 0 \ &\rightarrow \ x > 0
\end{align}
$$

The intersection of the two conditions yields $x > 0$, which is the set on which the first inequality is meaningful.

At this stage we can solve the first inequality. The two logarithms share the same base $2$, and since the base is greater than $1$, the logarithmic function is strictly increasing. The inequality between the logarithms is therefore equivalent, within the domain, to the same inequality between the arguments.

$$2x + 4 > x \ \rightarrow \ x > -4$$

Intersecting this condition with the domain $x > 0$, we conclude that the first inequality is satisfied for $x > 0$. The second inequality reduces to $x > 2$ by adding $2$ to both sides. We now determine where the two solution sets overlap.

[shortcode="intervals"]
|     | $0$                    | $2$             |   |
|:----|----------------------|---------------|---|
|     | sign+l-o             |               |   |
|     |                      | sign+l-o      |   |
|     |                      | sign+l-o-h    |   |
[/shortcode]

The solution of the system is the unbounded interval:

$$x > 2$$

Since $(2, +\infty)$ is contained in $(0, +\infty)$, the condition imposed by the domain of the logarithms is automatically satisfied by every solution of the system.

## An inconsistent system

A system can fail to have solutions even when each of its inequalities admits solutions on its own. Consider the system:

$$
\begin{cases}
x - 5 > 0 \\[6pt]
2 - x \geq 0
\end{cases}
$$

The first inequality yields $x > 5$ and the second yields $x \leq 2$. Each solution set is a non-empty interval, but no real number can be greater than $5$ and at the same time less than or equal to $2$. The intersection of the two intervals is empty, so the system is inconsistent and its solution set is the empty set $\varnothing$.

## Multivariable systems of inequalities

More complex systems consist of $k$ inequalities involving $m$ variables and have the general form:

$$
\begin{cases}
f_1(x_1, x_2, \ldots, x_m) \geq 0 \\[6pt]
f_2(x_1, x_2, \ldots, x_m) \geq 0 \\[6pt]
\quad \quad \vdots \\[6pt]
f_k(x_1, x_2, \ldots, x_m) \geq 0
\end{cases}
$$

In this setting the solution set is a region of $\mathbb{R}^m$ rather than a union of intervals, and its determination requires more advanced methods, such as graphical techniques, sign analysis, linear programming, and various numerical procedures. The two-variable case is treated in the entries on [linear inequalities in two variables](../linear-inequalities-in-two-variables/) and [systems of linear inequalities in two variables](../systems-of-linear-inequalities-in-two-variables/).
