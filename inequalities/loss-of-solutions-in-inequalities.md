---
title: Loss and Introduction of Solutions
source: https://algebrica.org/loss-of-solutions-in-inequalities/
license: CC BY-NC 4.0
tags:
  - admissible-operations
  - extraneous-solutions
  - irrational-inequalities
  - loss-of-solutions
  - rational-inequalities
  - squaring
---
## Why solutions disappear or multiply

The resolution of an [inequality](../inequalities/) proceeds by applying a sequence of transformations that turn the original inequality into a simpler form whose solution set is apparent. The procedure rests on the assumption that each transformation is equivalence-preserving, that is, that the transformed inequality has exactly the same solution set as the original. When a step fails to preserve equivalence, the solution set of the transformed inequality differs from the original, and the discrepancy can go in either direction.

+ Loss of solutions occurs when the transformation eliminates values that satisfy the original inequality, producing a solution set strictly smaller than the correct one.
+ Introduction of extraneous solutions occurs when the transformation adds values that satisfy the transformed inequality but not the original, producing a solution set strictly larger than the correct one.

The two phenomena have the same origin. The transformation is valid only on a portion of the domain, and the difference between the original and the transformed inequality is concentrated on the portion where the transformation does not apply. 

The standard methods are to keep track of the domain at every step, to perform case analyses based on the sign of any expression by which both sides are multiplied or divided, and to verify candidate solutions against the original inequality whenever a non-equivalence transformation has been used.

> The analogous phenomenon for equations is treated in the entry on [loss of roots](../loss-of-roots/). The difference between equations and inequalities is that an inequality has a continuum of solutions rather than a discrete set, so the loss or introduction of solutions affects entire [intervals](../intervals/) rather than isolated points.

## Multiplying by an expression of variable sign

The most frequent source of loss or introduction of solutions in inequalities is the multiplication or division of both sides by an expression that depends on the unknown. 

+ When the multiplier is a fixed positive constant, the direction of the inequality is preserved and no error is possible. 
+ When the multiplier is a fixed negative constant, the direction must be reversed, and the procedure remains equivalence-preserving as long as the reversal is performed. 
+ When the multiplier depends on the unknown, its sign depends on the value of the unknown, and the direction of the inequality may need to be preserved on some intervals and reversed on others.

Consider the inequality:

$$\frac{1}{x - 2} > 1$$

A common mistake is to clear the denominator by multiplying both sides by $x - 2$, obtaining the linear inequality $1 > x - 2$, that is $x < 3$. This procedure is incorrect because the sign of $x - 2$ is not constant, since the expression is positive for $x > 2$ and negative for $x < 2$. Multiplying both sides by $x - 2$ preserves the inequality on the region $x > 2$ but reverses it on the region $x < 2$.

The result $x < 3$ obtained without distinguishing the two cases is correct only on $x > 2$, where it gives $2 < x < 3$, and is wrong on $x < 2$, where it should give the opposite condition $1 < x - 2$, that is $x > 3$, which has no intersection with $x < 2$ and contributes no solution.

[shortcode="intervals"]
|                      | $2$               | $3$                   |     |
|----------------------|-----------------|---------------------|-----|
|                     |   sign+l-o      |                     |     |
|                     |                 | sign+r-o            |     |
|                 |   sign+l-in-o-h   | sign+r-in-o-h     |     |
[/shortcode]


The correct solution set is therefore $(2, 3)$, and the naive procedure produces the incorrect set $(-\infty, 3)$, introducing every value $x \leq 2$ as an extraneous solution. The point $x = 2$ is extraneous for a further reason, as it lies outside the domain of the original inequality.

The correct approach is to bring the inequality to canonical form by moving every term to one side and combining over a common denominator, as illustrated in the entry on [rational inequalities](../rational-inequalities/). Subtracting $1$ from both sides and combining gives the following.

$$\frac{1 - (x - 2)}{x - 2} > 0 \quad \rightarrow \quad \frac{3 - x}{x - 2} > 0$$

The sign of the ratio is determined by a [sign chart](../sign-analysis-in-inequalities/) on the numerator and the denominator, with critical points at $x = 2$ and $x = 3$. The ratio is positive precisely on the inner interval $(2, 3)$, which is the correct solution set.

> The reduction to canonical form preserves the inequality on the entire domain, so no value is added or lost. The naive multiplication, by contrast, fails because it implicitly assumes a sign for the multiplier and discards the alternative case.

## Cancelling a common factor

A related error consists in cancelling a common factor from both sides of an inequality. The cancellation amounts to a division by that factor, and the same caution applies as for any multiplication or division by an expression depending on the unknown. Consider the inequality:

$$x(x - 3) > 2(x - 3)$$

Cancelling the common factor $(x - 3)$ from both sides gives the linear inequality $x > 2$. This procedure is incorrect because the sign of $x - 3$ is not constant. The factor is positive for $x > 3$ and negative for $x < 3$, so the cancellation preserves the inequality on $x > 3$ and reverses it on $x < 3$. Moreover, the cancellation discards the value $x = 3$, at which both sides of the original inequality vanish and which deserves separate consideration.

The correct approach is to bring the inequality to the form $f(x) > 0$ by moving every term to one side and factoring the resulting expression.

$$x(x - 3) - 2(x - 3) > 0 \quad \rightarrow \quad (x - 3)(x - 2) > 0$$

The product is positive on the two outer intervals determined by the roots $x = 2$ and $x = 3$, so the correct solution set is the following.

$$(-\infty, 2) \cup (3, +\infty)$$

The naive cancellation produces only the right half-line $x > 2$, introducing the values $2 < x \leq 3$ as extraneous solutions and losing the entire interval $x < 2$. The value $x = 3$ is extraneous because at that point both sides of the original inequality are equal, so the strict inequality fails.

## Squaring both sides

Squaring both sides of an inequality is a standard technique in the resolution of [irrational inequalities](../irrational-inequalities/) and of [inequalities with absolute value](../inequalities-with-absolute-value/), but it is not an equivalence-preserving transformation in general. The function $t \mapsto t^2$ is not monotonic on $\mathbb{R}$, being increasing on $[0, +\infty)$ and decreasing on $(-\infty, 0]$, so squaring preserves the order between two numbers only when both are non-negative.

The rule for squaring an inequality is therefore the following.

+ If both sides are known to be non-negative, the inequality $A > B$ is equivalent to $A^2 > B^2$.
+ If both sides are known to be non-positive, the inequality $A > B$ is equivalent to $A^2 < B^2$, with the direction reversed.
+ If the two sides may have opposite signs or the sign cannot be determined, squaring is not equivalence-preserving and a case analysis is required.

A common source of error is to apply squaring without verifying the sign condition. Consider the inequality:

$$\sqrt{x + 1} < x - 1$$

The left-hand side is non-negative on its domain $x \geq -1$, but the right-hand side has variable sign, non-negative only for $x \geq 1$ and negative for $x < 1$. Squaring both sides without case analysis would give the inequality $x + 1 < (x - 1)^2$, that is $x^2 - 3x > 0$, with solutions $x < 0$ or $x > 3$. 

The portion $-1 \leq x < 0$ is entirely spurious, because on this region the right-hand side $x - 1$ is negative while the left-hand side $\sqrt{x + 1}$ is non-negative, so the original inequality is automatically false.

The correct procedure is to separate the cases based on the sign of the right-hand side, and to combine the squaring step with the domain condition on the radicand and with the sign condition on the right-hand side. The resolution gives the solution set $(3, +\infty)$, while the naive squaring restricted to the domain would suggest the larger set $[-1, 0) \cup (3, +\infty)$, with $[-1, 0)$ introduced as extraneous.

Squaring can also lose solutions when the case of a negative side is silently discarded. Consider the reversed inequality:

$$\sqrt{x + 1} > x - 1$$

For $-1 \leq x < 1$ the right-hand side is negative while the left-hand side is non-negative, so the inequality holds at every point of this interval and no squaring is needed. For $x \geq 1$ both sides are non-negative and squaring is admissible, giving $x + 1 > (x - 1)^2$, that is $x^2 - 3x < 0$, which combined with $x \geq 1$ yields $1 \leq x < 3$. The complete solution set is the union of the two cases, namely $[-1, 3)$. Squaring directly without case analysis produces only the interval $(0, 3)$ and drops the interval $[-1, 0]$, every point of which satisfies the original inequality.

> The general principle is that squaring is admissible without case analysis only when both sides are known to be non-negative. In every other situation the resolution must distinguish cases according to the sign of each side, and the candidate solutions must be checked against the original inequality.

## Raising to an even power

The remarks on squaring extend to every transformation that raises both sides to an even power. The function $t \mapsto t^{2k}$ is even and is monotonic only on $[0, +\infty)$ and on $(-\infty, 0]$ separately, so the order between two numbers is preserved by such a transformation only when both have the same sign.

The same does not apply to odd powers. The function $t \mapsto t^{2k+1}$ is strictly [increasing](../increasing-and-decreasing-functions/) on $\mathbb{R}$ and is therefore an equivalence-preserving transformation when applied to both sides of an inequality. The inequality $A > B$ is equivalent to $A^{2k+1} > B^{2k+1}$ without any sign restriction, for every positive integer $k$.

This distinction explains the asymmetry between even and odd radicals in the resolution of [irrational inequalities](../irrational-inequalities/). An inequality of the form $\sqrt[2k+1]{f(x)} > g(x)$ can be solved directly by raising both sides to the $(2k+1)$-th power and reducing to a polynomial inequality, with no sign condition to verify. 

An inequality of the form $\sqrt[2k]{f(x)} > g(x)$ requires a case analysis on the sign of $g(x)$ and a domain condition on the radicand $f(x) \geq 0$.

## Applying monotonic functions

The rules on [powers](../powers/) are special cases of a general principle. Applying a strictly increasing function to both sides of an inequality preserves its direction and its solution set, while applying a strictly decreasing function reverses the direction. A transformation of this kind fails to preserve equivalence only when the function is not monotonic on the entire interval of interest, as happens with even powers, or when its domain is smaller than the domain of the original inequality, in which case a domain condition must accompany the transformed inequality.

The principle governs in particular the resolution of [exponential inequalities](../exponential-inequalities/) and [logarithmic inequalities](../logarithmic-inequalities/). The inequality $a^{f(x)} > a^{g(x)}$ is equivalent to $f(x) > g(x)$ when $a > 1$ and to $f(x) < g(x)$ when $0 < a < 1$, because the exponential function with base smaller than one is strictly decreasing. The same dichotomy on the base applies to logarithms, with the additional requirement that the arguments be positive. Omitting the reversal of direction for a base between $0$ and $1$, or omitting the positivity condition on the arguments of a logarithm, produces exactly the loss and introduction phenomena described above.

## Combining inequalities

A related source of error arises when two inequalities are added or subtracted member by member without attention to the direction of the inequality signs.

+ Adding two inequalities of the same direction is admissible. From $A > B$ and $C > D$ one can deduce $A + C > B + D$, since the sum of the two positive differences $A - B$ and $C - D$ is positive.
+ Subtracting is not admissible in the same way, because from $A > B$ and $C > D$ one cannot in general deduce $A - C > B - D$, the direction of the resulting inequality depending on the magnitudes involved.
+ Multiplying two inequalities member by member is admissible when all four quantities are non-negative. From $0 \leq A \leq B$ and $0 \leq C \leq D$ one deduces $AC \leq BD$. When some of the quantities are negative, multiplication can reverse the direction in unexpected ways, and a case analysis is required.

> These restrictions reflect the fact that the order relation on the [real numbers](../real-numbers/) interacts with the four arithmetic operations in different ways. Addition and subtraction respect the order relation in a one-sided manner: addition of two inequalities of the same direction is always admissible, but subtraction is not. Multiplication and division respect the order relation only on the non-negative semi-axis, and they reverse it on the negative semi-axis. Every transformation must be examined against these basic rules before being applied.

## General principles

Several principles help prevent the unintentional loss or introduction of solutions when solving inequalities.

The most reliable strategy is to move all terms to one side and reduce the inequality to the canonical form $f(x) > 0$, then to study the sign of the single function $f(x)$ through a [sign chart](../sign-analysis-in-inequalities/). The reduction to canonical form preserves the inequality on the entire domain and avoids the difficulties associated with multiplication or division by sign-variable expressions.

Multiplication or division of both sides by an expression involving the unknown should be avoided unless that expression is known to have a constant sign throughout the domain. When such a multiplication appears necessary, a case analysis must be performed based on the sign of the multiplier, with the direction of the inequality preserved on the intervals where the multiplier is positive and reversed on the intervals where it is negative.

When an inequality involves even-index radicals or absolute values, the resolution must distinguish cases based on the sign of the expressions involved. Squaring both sides is admissible only when both sides are known to be non-negative, and the alternative case in which one side is negative must be examined separately.

Substituting each candidate value back into the original inequality is a useful verification, especially after a step that is not strictly equivalence-preserving. The verification detects both the extraneous solutions introduced by a non-equivalent manipulation and any valid solutions that may have been dropped along the way. 

Unlike the case of equations, where the verification involves a finite list of candidates, the verification in the case of inequalities involves testing a representative point of each interval of the candidate solution set, since the solution is generally a continuum rather than a discrete collection of points.
