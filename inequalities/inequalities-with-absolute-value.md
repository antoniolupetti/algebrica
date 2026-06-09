---
title: Inequalities With Absolute Value
source: https://algebrica.org/inequalities-with-absolute-value/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - distance
  - triangle-inequality
---
## Introduction

The [absolute value](../absolute-value/) of a real number $x$ is defined as follows:

$$|x| = \begin{cases} +x & \text{if } x \geq 0 \\[6pt]
-x & \text{if } x < 0 \end{cases}
 \qquad \forall x \in \mathbb{R}$$

Geometrically, $|x|$ represents the distance of $x$ from the origin on the real line, and more generally $|x - a|$ represents the distance between $x$ and the point $a$. This geometric interpretation is often the most natural way to understand inequalities involving absolute value, and it will guide the intuition behind the solution methods discussed below.

- - -

The properties that underlie the resolution of such inequalities are the following. For every [real number](../properties-of-real-numbers/) $k > 0$ and every real expression $f(x)$, the following equivalences hold:

+ $|f(x)| \leq k$ if and only if $-k \leq f(x) \leq k$.
+ $|f(x)| \geq k$ if and only if $f(x) \leq -k$ or $f(x) \geq k$.

The same equivalences extend to the strict inequality cases, replacing $\leq$ with $<$ and $\geq$ with $>$. The remaining values of $k$ are settled directly by the non-negativity of the absolute value. When $k = 0$, the inequality $|f(x)| \leq 0$ is satisfied only when $f(x) = 0$, while $|f(x)| < 0$ has no solution. For $k < 0$, the inequality $|f(x)| \leq k$ has no solution for any $x$. Symmetrically, $|f(x)| \geq k$ is satisfied by every $x$ in the domain of $f$ whenever $k \leq 0$, and $|f(x)| > 0$ holds for every $x$ except the zeros of $f$.

An alternative method, applicable whenever the expression inside the absolute value is [linear](../linear-inequalities/), consists in analysing the sign of the argument by means of its piecewise definition. One identifies the point at which the argument vanishes, divides the real line into the two corresponding half-lines, and rewrites the inequality separately on each of them, removing the absolute value. The partial solutions are then collected by union.

> Solving an inequality involving absolute value follows the same principle as solving an [equation with absolute value](../absolute-value-equations/): one applies the defining properties of the absolute value function to remove it algebraically, reducing the problem to a set of ordinary inequalities to be solved and combined.

## The triangle inequality

A fundamental result closely related to inequalities with absolute value is the triangle inequality. For any two real numbers $a$ and $b$, the following relation holds:

$$|a + b| \leq |a| + |b|$$

This inequality states that the absolute value of a sum never exceeds the sum of the absolute values. A useful companion is the reverse triangle inequality, which bounds the difference of the absolute values from above:

$$\bigl| |a| - |b| \bigr| \leq |a - b|$$

The proofs of both results and a detailed discussion of their consequences are presented in the entry on the [absolute value](../absolute-value/).

> The result is worth keeping in mind when working with expressions involving sums of absolute values, as it provides an immediate upper bound that can simplify estimates without requiring a full case-by-case analysis.

## Example 1

Consider the following simple inequality:

$$|x - 3| \leq 5$$

Applying the fundamental property for the case $\leq$, one obtains a [compound inequality](../compound-inequalities/), equivalent to a [system](../systems-of-inequalities/) of two simultaneous conditions:

$$-5 \leq x - 3 \leq 5$$

To isolate $x$, one adds $3$ to all three members of the compound inequality. This operation is admissible because adding the same quantity to both sides of an inequality does not alter its direction.

$$-5 + 3 \leq x \leq 5 + 3$$

$$-2 \leq x \leq 8$$

Representing the values obtained on the real line gives the following scheme:

[shortcode="intervals"]
| | $-2$     | $8$   |     |
|----------------------|---------------|--------------------|-----|
| |              |      sign+r-c       |     |
| | sign+l-c      |                    |     |
| |    sign+l-in-c-h           |     sign+r-in-c-h   |     |
[/shortcode]

The highlighted row represents the intersection of the two conditions, that is, the set of values of $x$ for which both inequalities are simultaneously satisfied. The solution is therefore the closed interval $[-2, 8]$.

> The same conclusion follows from the geometric interpretation. The inequality $|x - 3| \leq 5$ asks for the points whose distance from $3$ does not exceed $5$, and these form precisely the interval $[3 - 5, 3 + 5] = [-2, 8]$.

## Example 2

Consider the following inequality:

$$|2x + 1| > 3$$

Applying the fundamental property for the case $>$, the inequality splits into two alternative conditions, at least one of which must be satisfied.

$$2x + 1 < -3$$
$$2x + 1 > 3$$

Resolving the first condition, subtracting $1$ from both sides gives $2x < -4$, and dividing by $2$ yields $x < -2$. Since the divisor is positive, the direction of the inequality is preserved.

Resolving the second condition in the same way and subtracting $1$ gives $2x > 2$, and dividing by $2$ yields $x > 1$.

Representing the values obtained on the real line gives the following picture:

[shortcode="intervals"]
| | $-2$      | $1$  |     |
|----------------------|---------------|--------------------|-----|
| | sign+r-o      |                    |     |
| |               |      sign+l-o      |     |
| | sign+r-o-h    |         sign+l-o-h           |  |
[/shortcode]

In contrast with the previous case, the highlighted row represents the union of the two conditions, that is, the set of values of $x$ for which at least one of the two inequalities is satisfied.

The solution is therefore the union of open intervals $(-\infty, -2) \cup (1, +\infty)$.

> Geometrically, dividing both sides by $2$ rewrites the inequality as $\left|x + \frac{1}{2}\right| > \frac{3}{2}$, which asks for the points whose distance from $-\frac{1}{2}$ exceeds $\frac{3}{2}$. These are exactly the points lying to the left of $-2$ or to the right of $1$.

## Example 3

The fundamental equivalences do not depend on the algebraic form of the expression inside the absolute value, and apply unchanged when the argument is not linear. Consider the following inequality:

$$|x^2 - 9| < 7$$

Applying the fundamental property for the case $<$, the inequality is equivalent to a compound condition:

$$-7 < x^2 - 9 < 7$$

Adding $9$ to each member isolates $x^2$ and yields the following:

$$2 < x^2 < 16$$

The two members must hold simultaneously. The left inequality $x^2 > 2$ is satisfied for $x < -\sqrt{2}$ or $x > \sqrt{2}$, while the right inequality $x^2 < 16$ is satisfied for $-4 < x < 4$. The intersection consists of the points lying in $(-4, 4)$ and at the same time outside the closed interval $[-\sqrt{2}, \sqrt{2}]$.

The solution is therefore the union of two open intervals:

$$\left(-4, -\sqrt{2}\right) \cup \left(\sqrt{2}, 4\right)$$

## Example 4

When the right-hand side is not a constant but depends on $x$, the piecewise definition of the absolute value provides a systematic route to the solution. Consider the following inequality:

$$|x - 4| > -2x + 1$$

The expression $x - 4$ vanishes at $x = 4$, and the real line splits into the two half-lines $x \geq 4$ and $x < 4$. On each of them the absolute value can be removed and the inequality rewritten in elementary form.

- - -

Case $x \geq 4$. In this region $x - 4 \geq 0$ and the absolute value leaves the argument unchanged. The inequality becomes the following:

$$x - 4 > -2x + 1$$

Adding $2x$ to both sides and then $4$ gives $3x > 5$, hence $x > \frac{5}{3}$. The intersection with the region $x \geq 4$ produces $x \geq 4$, since $\frac{5}{3} < 4$.

- - -

Case $x < 4$. In this region $x - 4 < 0$ and the absolute value reverses the sign. The inequality becomes the following:

$$-(x - 4) > -2x + 1$$

$$-x + 4 > -2x + 1$$

Adding $2x$ to both sides yields $x + 4 > 1$, hence $x > -3$. The intersection with the region $x < 4$ produces $-3 < x < 4$.

- - -

Collecting the two partial contributions by union, the points $x \geq 4$ obtained from the first case and the points $-3 < x < 4$ obtained from the second case together cover every value greater than $-3$.

The solution is therefore the open half-line $\left(-3, +\infty\right)$.

> An alternative treatment of inequalities of this type, based on the sign of the right-hand side rather than on the sign of the argument, is discussed in the section on inequalities with a non-constant right-hand side below.

## Example 5

Consider the following inequality, in which two distinct absolute values appear:

$$|x + 1| + |x - 2| > 4$$

When an inequality contains more than one absolute value, the most systematic approach is to partition the real line according to the zeros of the arguments. The expressions $x + 1$ and $x - 2$ vanish at $x = -1$ and $x = 2$ respectively, giving three regions to be analysed separately.

- - -

Case $x < -1$. In this region $x + 1 < 0$ and $x - 2 < 0$, so both arguments are negative and the absolute value reverses their sign. The inequality becomes the following:

$$-(x + 1) + (-(x - 2)) > 4$$

$$-x - 1 - x + 2 > 4$$

$$-2x + 1 > 4$$

Subtracting $1$ from both sides gives $-2x > 3$. Dividing by $-2$ and reversing the direction of the inequality, since the divisor is negative, one obtains the following:

$$x < -\frac{3}{2}$$

This condition must hold within the region $x < -1$. Since $-\frac{3}{2} < -1$, the condition $x < -\frac{3}{2}$ is the more restrictive of the two, and the intersection with $x < -1$ reduces to $x < -\frac{3}{2}$. The contribution of this case is therefore $\left(-\infty, -\frac{3}{2}\right)$.

- - -

Case $-1 \leq x < 2$. In this region $x + 1 \geq 0$ and $x - 2 < 0$. The inequality becomes the following:

$$(x + 1) + (-(x - 2)) > 4$$

$$x + 1 - x + 2 > 4$$

$$3 > 4$$

This is a contradiction, which holds for no value of $x$. The middle case therefore yields no solution.

- - -

Case $x \geq 2$. In this region $x + 1 > 0$ and $x - 2 \geq 0$, so both arguments are non-negative and the absolute value leaves them unchanged. The inequality becomes the following:

$$(x + 1) + (x - 2) > 4$$

$$2x - 1 > 4$$

Adding $1$ to both sides gives $2x > 5$, and dividing by $2$ yields the following:

$$x > \frac{5}{2}$$

Intersecting with $x \geq 2$: since $\frac{5}{2} > 2$, the effective condition is $x > \frac{5}{2}$. The contribution of this case is therefore $\left(\frac{5}{2}, +\infty\right)$.

- - -

Collecting the contributions from all three cases, the partial solutions obtained on each region of the real line are plotted below.

[shortcode="intervals"]
| | $-\frac{3}{2}$      | $\frac{5}{2}$   |     |
|----------------------|---------------|--------------------|-----|
| | sign+r-o      |                    |     |
| |               |      sign+l-o      |     |
| | sign+r-o-h    |         sign+l-o-h           |  |
[/shortcode]

The union of the two open half-lines gives the complete solution set.

The solution of the inequality is therefore:

$$\left(-\infty, -\frac{3}{2}\right) \cup \left(\frac{5}{2}, +\infty\right)$$

> The geometric interpretation explains why the middle case is empty. The quantity $|x + 1| + |x - 2|$ is the sum of the distances of $x$ from the points $-1$ and $2$. For every $x$ lying between them this sum equals the fixed distance $3$ between the two points, which is smaller than $4$, so no solution can arise in that region.

## Example 6

We now consider a more involved case, in which the right-hand side of the inequality is not a fixed number but a [real parameter](../equations-with-parameters/) $k$. The structure of the solution set depends on the value of $k$, and a complete discussion requires treating several cases separately. Consider the following inequality:

$$|x - 1| > k$$

The behaviour of the solution changes substantially depending on whether $k$ is negative, zero, or positive, and this is what we set out to determine.

- - -

Case $k < 0$. Since the absolute value is always non-negative, the left-hand side satisfies $|x - 1| \geq 0 > k$ for every real $x$. The inequality is therefore satisfied by all real numbers, and the solution is $\mathbb{R}$.

- - -

Case $k = 0$. The inequality reduces to $|x - 1| > 0$, which holds for every $x$ except the point where the absolute value vanishes. Since $|x - 1| = 0$ if and only if $x = 1$, the solution is $\mathbb{R} \setminus \{1\}$.

- - -

Case $k > 0$. Applying the fundamental property for the case $>$, the inequality splits into two alternative conditions:

$$x - 1 < -k$$
$$x - 1 > k$$

Adding $1$ to both sides of each condition yields the following:

$$x < 1 - k \qquad \text{or} \qquad x > 1 + k$$

- - -

Representing the solution on the real line gives the following picture:

[shortcode="intervals"]
| | $1-k$      | $1+k$   |     |
|----------------------|---------------|--------------------|-----|
| | sign+r-o      |                    |     |
| |               |      sign+l-o      |     |
| | sign+r-o-h    |         sign+l-o-h           |  |
[/shortcode]

As $k \to 0^+$ the two boundary points $1 - k$ and $1 + k$ approach $1$ from opposite sides, and the solution set approaches $\mathbb{R} \setminus \{1\}$, consistently with the case $k = 0$.

The solution is therefore the union of two open intervals:

$$\left(-\infty, 1-k\right) \cup \left(1+k, +\infty\right)$$

## Inequalities with a non-constant right-hand side

The equivalences stated above were formulated for a positive constant $k$, but they remain valid when the right-hand side is itself a function of $x$, say $g(x)$. Consider the following inequality.

$$|f(x)| \leq g(x)$$

Applying the same reasoning as before, this is equivalent to the following compound inequality.

$$-g(x) \leq f(x) \leq g(x)$$

The equivalence requires no restriction on the sign of $g(x)$. At any point where $g(x) < 0$ the original inequality fails, since the left-hand side is non-negative, and the compound inequality fails as well, because $-g(x) \leq g(x)$ forces $g(x) \geq 0$. The two formulations therefore agree everywhere.

> Since the left-hand side is non-negative, every solution must satisfy $g(x) \geq 0$. Although this condition is already encoded in the compound inequality, making it explicit at the outset often simplifies the computation, as it restricts the analysis to a smaller region from the start.

As a concrete instance, consider the following.

$$|x - 1| \leq 2x - 3$$

The right-hand side $g(x) = 2x - 3$ is non-negative only when $x \geq \frac{3}{2}$, so every solution must lie in this half-line. At the boundary point $x = \frac{3}{2}$ the inequality would require $|x - 1| \leq 0$, that is $x = 1$, which is impossible, so the analysis can be confined to the region $x > \frac{3}{2}$. There the inequality is equivalent to the following system.

$$-(2x - 3) \leq x - 1 \leq 2x - 3$$

The left inequality $-(2x - 3) \leq x - 1$ simplifies to $-2x + 3 \leq x - 1$, that is $4 \leq 3x$, yielding $x \geq \frac{4}{3}$. The right inequality $x - 1 \leq 2x - 3$ simplifies to $2 \leq x$, yielding $x \geq 2$. Since $\frac{4}{3} < \frac{3}{2} < 2$, the condition $x \geq \frac{4}{3}$ is already implied by the requirement $x > \frac{3}{2}$, and the binding constraint among all three is $x \geq 2$. Representing the solution on the real line gives the following picture.

[shortcode="intervals"]
|   | $\frac{4}{3}$ | $\frac{3}{2}$ | $2$ |   |
|---|------------------|------------------|--------|---|
|   |     sign+l-c              |         |        |   |
|   |                  |      sign+l-c             | |   |
|   |                  |                  | sign+l-c |   |
|   |                  |                  | sign+l-c-h |   |
[/shortcode]

The three critical values appearing in the graph reflect the three conditions derived during the solution: the threshold $\frac{4}{3}$ from the left inequality, the threshold $\frac{3}{2}$ from the sign requirement on $g(x)$, and the threshold $2$ from the right inequality. Since each condition is more restrictive than the previous one, the effective solution is determined entirely by the rightmost bound.

The solution is therefore the interval $[2, +\infty)$.

The companion case $|f(x)| \geq g(x)$ with a non-constant right-hand side admits an analogous unconditional reduction, being equivalent to the pair of alternatives $f(x) \leq -g(x)$ or $f(x) \geq g(x)$. 

In practice it is often convenient to split the analysis according to the sign of the right-hand side. Wherever $g(x) \leq 0$ the inequality holds automatically, since the left-hand side is non-negative, while wherever $g(x) > 0$ the two alternatives are solved as ordinary inequalities. The full solution is the union of the contributions from the two regions, and this is precisely the structure observed in Example 4 above.

## Absolute values on both sides

A particularly situation occurs when both sides of the inequality carry an absolute value, as in $|f(x)| \lessgtr |g(x)|$. Since both members are non-negative and the squaring map $t \mapsto t^2$ is increasing on $[0, +\infty)$, squaring is an equivalence rather than a one-way implication, and no auxiliary sign condition is required. The inequality is therefore equivalent to the corresponding inequality between the squares.

$$|f(x)| < |g(x)| \iff f(x)^2 < g(x)^2$$

The same equivalence holds with $\leq$, $>$ or $\geq$ in place of $<$. Moving every term to one side and factoring the difference of squares reduces the problem to a [sign analysis](../sign-analysis-in-inequalities/) of a product.

$$f(x)^2 - g(x)^2 = \bigl(f(x) - g(x)\bigr)\bigl(f(x) + g(x)\bigr)$$

As a concrete instance, consider the following inequality.

$$|x - 1| < |2x + 3|$$

Squaring both sides and moving the terms to the left gives $(x-1)^2 - (2x+3)^2 < 0$. Factoring the difference of squares yields the following.

$$\bigl((x-1) - (2x+3)\bigr)\bigl((x-1) + (2x+3)\bigr) < 0$$

The two factors simplify to $-x - 4$ and $3x + 2$, so the inequality becomes $(-x - 4)(3x + 2) < 0$. Multiplying by $-1$ and reversing the direction gives $(x + 4)(3x + 2) > 0$, a product that is positive outside the interval determined by its roots $x = -4$ and $x = -2/3$.

The solution is therefore the union of two open intervals.

$$\left(-\infty, -4\right) \cup \left(-\frac{2}{3}, +\infty\right)$$
