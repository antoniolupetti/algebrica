---
title: Exponential Inequalities
source: https://algebrica.org/exponential-inequalities/
license: CC BY-NC 4.0
tags:
  - exponential-function
  - inequalities
  - logarithms
  - monotonicity
---
## Introduction

Exponential inequalities are [inequalities](../inequalities/) in which the unknown appears in the exponent of a [power](../powers/). They take the general form:

$$a^{f(x)} > a^{g(x)}$$

or, in the simpler cases, the form:

$$a^x > b$$

The same definitions apply with the symbols $<$, $\geq$ and $\leq$ in place of $>$. We assume that the base $a$ is a positive real number with $a \neq 1$. The value $a = 1$ is excluded for the same reason given for [exponential equations](../exponential-equations/), since $1^x$ equals $1$ for every real $x$ and the comparison degenerates into a numerical statement that no longer involves the unknown.

The resolution of these inequalities rests on the monotonicity of the [exponential function](../exponential-function/). When $a > 1$ the function $a^x$ is strictly increasing, so larger exponents produce larger powers. When $0 < a < 1$ the function is strictly decreasing, so larger exponents produce smaller powers. Every method described below is an application of this single principle.

## Reduction to a common base

When both sides of the inequality can be expressed as powers of the same base, the comparison between the powers translates into a comparison between the exponents. The direction of the resulting inequality depends on the base.

+ If $a > 1$, the inequality $a^{f(x)} > a^{g(x)}$ is equivalent to $f(x) > g(x)$.
+ If $0 < a < 1$, the inequality $a^{f(x)} > a^{g(x)}$ is equivalent to $f(x) < g(x)$.

The same equivalences hold for non-strict inequalities. The method therefore consists of two steps, rewriting both sides as powers of a common base and then comparing the exponents according to whether the base is greater than one or strictly between zero and one.

## Example 1

Solve the exponential inequality:

$$2^{x^2 - x} < 64$$

The right-hand side is a power of $2$, since $64 = 2^6$, so the inequality can be written with a common base on both sides:

$$2^{x^2 - x} < 2^6$$

The base is $2 > 1$, so the exponential function is strictly increasing and the inequality between the exponents keeps the same direction:

$$
\begin{align}
&x^2 - x < 6 \\[6pt]
&x^2 - x - 6 < 0
\end{align}
$$

The result is a [quadratic inequality](../quadratic-inequalities/). The associated equation factors as $(x + 2)(x - 3) = 0$, with roots $x_1 = -2$ and $x_2 = 3$. The leading coefficient is positive, so the corresponding parabola opens upward and the trinomial is negative between the roots. The inequality is satisfied on the open interval:

$$(-2, 3)$$

## Example 2

Solve an inequality whose base lies between zero and one:

$$\left(\frac{1}{2}\right)^{3x - 4} \geq 8$$

The right-hand side can be expressed as a power of $\frac{1}{2}$, since $8 = 2^3 = \left(\frac{1}{2}\right)^{-3}$:

$$\left(\frac{1}{2}\right)^{3x - 4} \geq \left(\frac{1}{2}\right)^{-3}$$

The base lies strictly between zero and one, so the exponential function is strictly decreasing and the inequality between the exponents reverses direction:

$$
\begin{align}
&3x - 4 \leq -3 \\[6pt]
&3x \leq 1 \\[6pt]
&x \leq \frac{1}{3}
\end{align}
$$

The solution set is the half-line $\left(-\infty, 1/3\right]$. A quick check confirms the direction of the solution, since $x = 0$ gives $\left(\frac{1}{2}\right)^{-4} = 16$, which is indeed greater than $8$, while $x = 2$ gives $\left(\frac{1}{2}\right)^{2} = \frac{1}{4}$, which is not.

> The reversal of the inequality is the single most common source of error in this topic. Whenever the base of the powers being compared is strictly between zero and one, the comparison between the exponents must change direction.

## Choosing the base of comparison

An inequality whose base lies strictly between zero and one can always be rewritten in terms of the reciprocal base, which is greater than one. Both routes lead to the same solution, and the second removes the step in which the direction of the inequality has to be reversed. Consider the inequality:

$$\left(\frac{1}{3}\right)^{2x - 5} > 81$$

Working directly with the base $\frac{1}{3}$, the right-hand side is expressed as $81 = 3^4 = \left(\frac{1}{3}\right)^{-4}$. The base lies between zero and one, so the comparison between the exponents reverses direction:

$$
\begin{align}
&2x - 5 < -4 \\[6pt]
&x < \frac{1}{2}
\end{align}
$$

Alternatively, the identity $\frac{1}{3} = 3^{-1}$ allows the left-hand side to be written as a power of $3$:

$$\left(\frac{1}{3}\right)^{2x - 5} = 3^{-(2x - 5)} = 3^{5 - 2x}$$

The inequality becomes $3^{5 - 2x} > 3^4$, and the base is now greater than one, so the comparison passes to the exponents without a change of direction. The condition $5 - 2x > 4$ gives again $x < \frac{1}{2}$, in agreement with the first computation.

> Either base is acceptable, and the choice is a matter of convenience. Rewriting every power in a base greater than one is often the safer habit, because it eliminates the step where the inequality must be reversed.

## Inequalities with radicals

When the exponential expressions appear under root signs, the radicals are first converted into powers with fractional exponents, and the inequality is then reduced to a common base as in the previous cases. Consider the inequality:

$$7\sqrt{3^{x + 4}} < 21\sqrt[3]{9^{x - 1}}$$

Dividing both sides by $7$, which is positive, and writing each root as a fractional power gives:

$$3^{\frac{x + 4}{2}} < 3 \cdot \left(9^{x - 1}\right)^{\frac{1}{3}}$$

Since $9 = 3^2$, the right-hand side collects into a single power of $3$:

$$3 \cdot 3^{\frac{2(x - 1)}{3}} = 3^{1 + \frac{2x - 2}{3}} = 3^{\frac{2x + 1}{3}}$$

The two sides now share the base $3 > 1$, so the inequality passes to the exponents with the same direction:

$$\frac{x + 4}{2} < \frac{2x + 1}{3}$$

Multiplying both sides by $6$, which is positive, clears the denominators:

$$
\begin{align}
&3(x + 4) < 2(2x + 1) \\[6pt]
&3x + 12 < 4x + 2 \\[6pt]
&x > 10
\end{align}
$$

The solution set is the half-line $(10, +\infty)$. A quick check confirms the direction, since $x = 14$ gives the exponents $\frac{18}{2} = 9$ on the left and $\frac{29}{3}$ on the right, and indeed $9 < \frac{29}{3}$.

## When bases differ: solving with logarithms

When the right-hand side cannot be written as a power of the base appearing on the left, the standard technique is to apply a [logarithm](../logarithms/) to both sides. Consider the inequality:

$$2^{3x - 1} > 5$$

Since $5$ is not a rational power of $2$, we take the base-$2$ logarithm of both sides. The function $\log_2$ is strictly increasing, because its base is greater than one, so the direction of the inequality is preserved:

$$
\begin{align}
&3x - 1 > \log_2 5 \\[6pt]
&x > \frac{1 + \log_2 5}{3}
\end{align}
$$

The solution set is the half-line of all real numbers greater than $\frac{1 + \log_2 5}{3}$.

> If the logarithm were taken in a base strictly between zero and one, the direction of the inequality would reverse. Choosing a base greater than one, typically the base of the exponential itself or the natural base $e$, avoids this complication and is the standard convention.

- - -

A different situation arises when the two sides carry the same exponent but different bases. Consider the inequality:

$$7^x > 4^x$$

Dividing both sides by $4^x$, which is positive for every real $x$, preserves the direction of the inequality and isolates a single power:

$$\left(\frac{7}{4}\right)^x > 1$$

Writing $1 = \left(\frac{7}{4}\right)^0$ and observing that the base $\frac{7}{4}$ is greater than one, the comparison between the exponents gives $x > 0$. The solution set is the half-line $(0, +\infty)$, in agreement with the graphs of the two exponentials, which intersect only at the point $(0, 1)$.

## Inequalities reducible to a polynomial by substitution

A frequent class of exponential inequalities contains the same exponential expression more than once, often with one term squared. These inequalities are solved by introducing a new variable equal to the exponential, which transforms the problem into an algebraic inequality. Consider the inequality:

$$9^x - 10 \cdot 3^x + 9 \leq 0$$

The two exponential terms can be expressed through the single base $3$, since $9^x = (3^2)^x = (3^x)^2$. Setting $t = 3^x$, with $t > 0$, the inequality becomes a [quadratic inequality](../quadratic-inequalities/) in the auxiliary variable:

$$t^2 - 10t + 9 \leq 0$$

The associated equation factors as $(t - 1)(t - 9) = 0$, with roots $t_1 = 1$ and $t_2 = 9$. The parabola opens upward, so the trinomial is non-positive between the roots:

$$1 \leq t \leq 9$$

This interval lies entirely in the region $t > 0$, so no part of it has to be discarded. Reversing the substitution $t = 3^x$ and writing the bounds as powers of $3$ produces a double exponential inequality:

$$3^0 \leq 3^x \leq 3^2$$

The base is $3 > 1$, so both comparisons keep their direction when read on the exponents, and the unknown satisfies $0 \leq x \leq 2$. The solution set is the closed interval:

$$[0, 2]$$

> The constraint $t > 0$ must always be intersected with the solution of the auxiliary inequality. Any portion of that solution lying in $t \leq 0$ corresponds to no value of $x$, since an exponential expression takes only positive values.

## Inequalities with terms of opposite sign in the exponent

A related case arises when the unknown appears with exponents of opposite sign, so that an exponential and its reciprocal occur together. Consider the inequality:

$$2^x - 2^{1 - x} < 1$$

Since $2^{1 - x} = \frac{2}{2^x}$, the substitution $t = 2^x$, with $t > 0$, rewrites the inequality as:

$$t - \frac{2}{t} < 1$$

Multiplying both sides by $t$ preserves the direction of the inequality, because $t$ is strictly positive by construction:

$$
\begin{align}
&t^2 - 2 < t \\[6pt]
&t^2 - t - 2 < 0
\end{align}
$$

The trinomial factors as $(t + 1)(t - 2) < 0$, so the inequality holds for $-1 < t < 2$. Intersecting with the constraint $t > 0$ leaves the interval $0 < t < 2$. Reversing the substitution gives:

$$0 < 2^x < 2$$

The left condition is satisfied by every real $x$, since the exponential is always positive. The right condition, written as $2^x < 2^1$ with base greater than one, gives $x < 1$. The solution set is the half-line:

$$(-\infty, 1)$$

> Multiplying an inequality by an expression whose sign is unknown would require a case distinction, as discussed in the entry on [loss of solutions](../loss-of-solutions/). The substitution avoids this difficulty here, because $t = 2^x$ is positive for every real $x$.

## Existence and structure of the solution set

The elementary inequality $a^x > b$ behaves differently according to the sign of $b$. 

+ When $b \leq 0$ it is satisfied by every real number, because the exponential takes only positive values. 
+ When $b > 0$ and $a > 1$ the solution is the half-line $x > \log_a b$, while for $0 < a < 1$ it is the half-line $x < \log_a b$. The opposite inequality $a^x < b$ has no solution when $b \leq 0$, and a single half-line as solution when $b > 0$.

In the more elaborate cases the solution set is a finite union of [intervals](../intervals/) of the real line, possibly empty or equal to all of $\mathbb{R}$. When the inequality is reduced to a polynomial inequality through a substitution, each interval of admissible positive values of the auxiliary variable is carried back to an interval of values of the unknown by a logarithm, and the monotonicity of the logarithm guarantees that the interval structure is preserved. 

A symmetric treatment, in which the unknown appears inside a logarithm rather than in an exponent, is given in the entry on [logarithmic inequalities](../logarithmic-inequalities/).
