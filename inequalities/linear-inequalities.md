---
title: Linear Inequalities
source: https://algebrica.org/linear-inequalities/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - intervals
  - linear-inequality
  - parameters
---
## Introduction

An inequality is a mathematical statement involving algebraic expressions for which we seek the values of the variables that make the inequality true. In general, an inequality between two algebraic expressions $A(x)$ and $B(x)$ is defined as the relation:  

$$A(x) > B(x)$$

Solving an inequality involves determining the solution set, that is, all the values of $x$ that satisfy the previous inequality. For a linear inequality in one real variable, the solution set is always a subset of $\mathbb{R}$ in the form of an interval, possibly unbounded, or, in degenerate cases, the whole real line or the empty set. 

Higher-degree inequalities, or those involving several variables, yield more complex solution sets, which are treated in the dedicated entries.

Given two real numbers $a$ and $b$ with $a < b$, a bounded [interval](../intervals/) is defined as the [set](../sets/) of [real numbers](../real-numbers/) between $a$ and $b$, where $a$ and $b$ are the lower and upper bounds, respectively. An unbounded interval is the set of numbers that either precede $a$ or follow $a$. If the endpoints of a bounded interval are included, the interval is called closed, otherwise, it is called open.

[shortcode="intervals"]
|                      | $-3$              | $6$                   |     |
|----------------------|-----------------|---------------------|-----|
|                      |   sign+l-c      |                     |     |
|                      |   sign+l-in-c   | sign+r-in-o         |     |
[/shortcode]


> In the first interval, the number $3$ is included among the elements of the interval. It is represented as $[3,\infty)$, which is closed at $3$ and open toward infinity. In the second interval, the number $3$ is included in the interval, while the number $6$ is excluded. It is represented as $[3,6)$, which is closed at $3$ and open at $6$.

- - -

The inequality sign determines whether the solution interval is open or closed at its boundary. A strict inequality, expressed with $>$ or $<$, excludes the boundary value, yielding an open interval. A non-strict inequality, expressed with $\geq$ or $\leq$, includes it, yielding a closed or half-open interval.

| Inequality | Interval |
|---|---|
| $x > a$ | $(a, +\infty)$ |
| $x \geq a$ | $[a, +\infty)$ |
| $x < a$ | $(-\infty, a)$ |
| $x \leq a$ | $(-\infty, a]$ |
| $a < x < b$ | $(a, b)$ |
| $a \leq x \leq b$ | $[a, b]$ |

> The previous table summarizes the correspondence between the inequality sign and the resulting interval notation for a single-variable linear inequality.

- - -

The degree of an inequality corresponds to the degree of the [polynomial](../polynomials/) $P(x)$ obtained by rewriting the inequality in the form $P(x) > 0$. A linear or first-degree inequality in one variable, in its more general form, is a comparison between two first-degree expressions:

$$ax + b > cx + d$$

When $c = d = 0$ this reduces to $ax + b > 0$, a linear polynomial compared to zero. By moving all terms involving $x$ to one side and the constant terms to the other, every linear inequality can be rewritten in the equivalent reduced form:

$$Ax > B$$

where $A = a - c$ and $B = d - b$. The reduced form is the one we use throughout the rest of the discussion.

Every first-degree inequality with $A \neq 0$ has an interval of values as its solution. The condition $A \neq 0$ is essential. When $A = 0$, the variable disappears entirely from the inequality, and the problem reduces to comparing two constants. Substituting $A = 0$ into the reduced form gives the following.

$$0 \cdot x > B$$

This simplifies to $0 > B$. If $B < 0$, the inequality holds regardless of the value of $x$, and the solution set is all of $\mathbb{R}$. If $B \geq 0$, the inequality is never satisfied, and the solution set is empty. In either case, there is no interval determined by a boundary point: the outcome is a global truth or a contradiction, not a proper first-degree inequality.

- - -

Given an inequality, an equivalent inequality can be obtained by adding the same number or expression to both sides, provided that the expression is well-defined within the same [domain](../determining-the-domain-of-a-function/). The inequality $5x - 2 > x + 3$ is equivalent to the inequality $4x - 2 > 3$, by subtracting $x$ from both sides.

An equivalent inequality can also be obtained by dividing or multiplying both sides by the same non-zero value. These manipulations are the same ones used to solve a [linear equation](../linear-equations/), with one crucial difference: if the value is negative, the inequality sign must be reversed. It is always useful to rewrite a first-degree inequality like $-x + 5 < -3$ in the form $x - 5 > 3$. Changing the signs requires reversing the direction of the inequality.

## Geometric interpretation

The solution set of a linear inequality always corresponds to a half-line on the real number line, that is, an unbounded interval extending indefinitely in one direction from a boundary point. 

+ When the inequality is strict, the boundary point is excluded and the half-line is open at that end. 

+ When the inequality is non-strict, the boundary point belongs to the solution set and the half-line is closed.

Consider, for instance, the simple inequality $x \geq 1$. Its solution set is the closed half-line $[1, +\infty)$, represented below.

[shortcode="intervals"]
|   | $1$        |   |
|---|----------|---|
|   | sign+l-c |   |
[/shortcode]

This geometric reading clarifies why the solution of a first-degree inequality is never an isolated point or a bounded interval: the linear structure of the expression $Ax - B$ ensures that its sign changes exactly once, at $x = B/A$, dividing the real line into precisely two regions, one of which constitutes the solution.

## Example 1

Consider the following inequality:

$$-\frac{x}{2} + 5 > 2x - 5$$

The goal is to reduce it to the standard form $Ax > B$. Since the left-hand side contains a fraction with denominator $2$, multiplying both sides by $2$ clears the denominator without altering the direction of the inequality, as the multiplier is positive.

$$-x + 10 > 4x - 10$$

Collecting all terms involving $x$ on the left and moving the constant terms to the right yields the following.

$$-5x > -20$$

Dividing both sides by $-5$ isolates the variable. Since the divisor is negative, the direction of the inequality must be reversed.

$$x < 4$$

[shortcode="intervals"]
|   | $4$        |   |
|---|----------|---|
|   | sign+r-o |   |
[/shortcode]

The solution set is the open interval $(-\infty, 4)$.

## How to solve literal first-degree inequalities

In the case of literal first-degree inequalities, the coefficient of the variable is not a fixed constant but depends on one or more parameters. Consider the following inequality.

$$z(x - 1) < 2x + 1$$

The first step is to expand and collect terms so as to rewrite the expression in one of the standard forms $Ax > B$, $Ax < B$, $Ax \geq B$, or $Ax \leq B$. Expanding the left-hand side and moving all terms involving $x$ to the left yields the following.

$$\begin{align}
&zx - z < 2x + 1 \\[6pt]
&zx - 2x < z + 1 \\[6pt]
&(z - 2)x < z + 1
\end{align}$$

The inequality is now in the form $Ax < B$ with $A = z - 2$ and $B = z + 1$. Since dividing both sides by $A$ requires knowing its sign, and the sign of $z - 2$ depends on the value of the parameter $z$, it is necessary to distinguish three separate cases.

- - -

When $z > 2$, the coefficient $z - 2$ is positive. Dividing both sides by a positive quantity preserves the direction of the inequality, giving the following:

$$x < \frac{z + 1}{z - 2}$$


When $z = 2$, the coefficient $z - 2$ vanishes. Substituting this value reduces the inequality to $0 \cdot x < 3$, which holds for every $x \in \mathbb{R}$. The solution set is all of $\mathbb{R}$.

When $z < 2$, the coefficient $z - 2$ is negative. Dividing both sides by a negative quantity reverses the direction of the inequality, giving the following:

$$x > \frac{z + 1}{z - 2}$$

## Absolute value inequalities

Absolute value inequalities are inequalities that follow the properties of [absolute value](../absolute-value/) and are of the form:

$$|x| < z$$

In general, inequalities involving absolute values do not belong to the class of linear inequalities, since the absolute value function is defined piecewise and the algebraic expression of the inequality changes form at the points where the argument vanishes. 

However, through an appropriate decomposition process, they can be transformed into one or more equivalent systems of linear inequalities, allowing them to be analyzed using the same methods applied to first-degree inequalities. 

A more systematic and complete discussion is provided in the dedicated entry on [inequalities with absolute value](../inequalities-with-absolute-value/), while the use of systems to combine the resulting conditions is treated in the entry on [systems of inequalities](../systems-of-inequalities/).

- - -

To solve them, we need to consider the sign of the absolute value by dividing it into two cases:

+ $|x| < z$ if and only if $-z < x < z$.
+ $|x| > z$ if and only if $x < -z \quad \text{or} \quad x > z$.

We must therefore solve a system of inequalities resulting from the possible cases considered in the analysis. The process is slightly more complicated than simple linear equations, and careful attention must be paid to the signs and the direction of the inequality during calculations.

## Example 2

Let’s try to solve the following absolute value inequality:

$$|x - 1| < 2x + 4$$

First, we study the sign of $|x - 1|$. We have:

$$|x - 1| =
\begin{cases}
x - 1 & \quad x \ge 1 \\[6pt]
-x + 1 & \quad x < 1
\end{cases}$$

Substituting the first branch into the inequality and solving yields the following system.

$$\begin{cases}
x \geq 1 \\[6pt]
x - 1 < 2x + 4
\end{cases}$$

The second inequality reduces to $x > -5$. The solution of the system is the intersection of $x \geq 1$ and $x > -5$, which is $x \geq 1$.

[shortcode="intervals"]
| | $-5$            | $1$                  |     |
|-|---------------|--------------------|-----|
| |               | sign+l-c           |     |
| | sign+l-o      |                    |     |
| |               | sign+l-c-h         |     |
[/shortcode]

Substituting the second branch into the inequality and solving yields the following system:

$$\begin{cases}
x < 1 \\[6pt]
-x + 1 < 2x + 4
\end{cases}$$

The second inequality reduces to $x > -1$. The solution of the system is the intersection of $x < 1$ and $x > -1$, which is the open interval $(-1, 1)$.

[shortcode="intervals"]
|                      | $-1$              | $1$                   |     |
|----------------------|-----------------|---------------------|-----|
|                      |   sign+l-in-o   | sign+r-in-o         |     |
|                      |   sign+l-in-o-h | sign+r-in-o-h       |     |
[/shortcode]


The complete solution is obtained by taking the union of the two partial solution sets. Since $x \geq 1$ and $(-1, 1)$ are adjacent intervals that together cover all values greater than $-1$, the solution to the inequality is the following.

$$x > -1$$
