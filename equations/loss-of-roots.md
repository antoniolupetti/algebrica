---
title: Loss of Roots
source: https://algebrica.org/loss-of-roots/
license: CC BY-NC 4.0
tags:
  - extraneous-solutions
  - irrational-equations
  - loss-of-roots
  - quadratic-equations
  - rational-equations
  - zero-product-property
---
## Why solutions disappear

Loss of roots occurs when an algebraic manipulation eliminates one or more [roots](../../polynomials/roots-of-a-polynomial/) of an [equation](../equations/), yielding a result that is only a partial solution set. The most frequent cause is dividing both sides of the equation by an expression containing the unknown, an operation that is valid only when that expression is guaranteed to be nonzero. Consider, for example, the equation:

$$x(2x-5) = x$$

A common mistake is to cancel the factor $x$ appearing on both sides. This reduces the equation to a linear equation in $x$:

$$2x - 5 = 1$$

$$x = \frac{6}{2} = 3$$

The cancellation is equivalent to dividing both sides by $x$, an operation that presupposes $x \neq 0$. The case $x = 0$ is silently discarded, and one solution is lost.

More generally, any factor containing the unknown may be cancelled from both sides only after verifying that it cannot equal zero. When that condition cannot be established, the equation must be factored rather than simplified by division.

## Correct method

The correct approach consists in bringing the equation to standard form before any further manipulation. Rather than attempting to simplify factors, all terms are moved to one side so that the equation takes the form $ax^2 + bx + c = 0$. Starting from the equation:

$$x(2x-5) = x$$

Expanding the left-hand side and subtracting $x$ from both members yields the following:

$$
\begin{align}
2x^2 - 5x - x &= 0 \\[6pt]
2x^2 - 6x &= 0 \\[6pt]
2x(x - 3) &= 0
\end{align}
$$

The result is an [incomplete quadratic equation](../incomplete-quadratic-equations/) in which the constant term $c$ is zero. Applying the zero-product property, the product $2x(x-3)$ vanishes if and only if at least one of the two factors is zero.

Setting each factor equal to zero separately gives the two solutions of the equation:

$$x_1 = 0 \qquad x_2 = 3$$

> The solution $x_1 = 0$, discarded by the incorrect cancellation, is recovered as a direct consequence of the factored form. The equation admits two distinct real solutions, and the value obtained by the flawed procedure accounts for only one of them.

## Why division removes a solution

The reason the two procedures disagree can be made precise by comparing the logical content of each step. Dividing both sides of $x(2x-5) = x$ by $x$ replaces the original equation with the equation $2x - 5 = 1$, but the two are equivalent only under the additional hypothesis $x \neq 0$. The division therefore does not transform the equation into an equivalent one; it transforms it into the equation that holds on the restricted domain $x \neq 0$, and the value $x = 0$ is excluded before it can be tested.

Factoring, by contrast, preserves the full equation. Writing $x(2x-5) - x = 0$ and collecting the common factor produces $2x(x-3) = 0$, an identity valid for every real $x$. No value is removed from the domain at any stage, so no solution can be lost. This is the structural advantage of reduction to a product equal to zero: the set of solutions of the factored form coincides exactly with the set of solutions of the original equation.

## Loss of roots by squaring

A second common source of root loss arises when solving [irrational equations](../irrational-equations/). Squaring both sides of an equation is a standard technique for eliminating radicals, but it is not an equivalence transformation. The squared equation may admit solutions that the original does not, and an incorrect application of the method can suppress valid ones. Consider the equation:

$$\sqrt{2x + 1} = x - 1$$

Squaring both sides yields the following:

$$
\begin{align}
2x + 1 &= (x-1)^2 \\[6pt]
2x + 1 &= x^2 - 2x + 1 \\[6pt]
x^2 - 4x &= 0 \\[6pt]
x(x - 4) &= 0
\end{align}
$$

The two candidates are $x_1 = 0$ and $x_2 = 4$. Substituting back into the original equation, $x_1 = 0$ gives $\sqrt{1} = -1$, which is false, so $x_1 = 0$ is an extraneous solution introduced by squaring. The candidate $x_2 = 4$ gives $\sqrt{9} = 3$, which is true, so it is the only valid solution.

> In this case no root is lost, but the example illustrates why verification is indispensable. Squaring can both introduce spurious solutions and, when applied selectively or incorrectly, discard valid ones.

The loss of a genuine root by squaring typically occurs when only one of two admissible sign choices is retained. An equation of the form $|f(x)| = g(x)$ is equivalent to the pair $f(x) = g(x)$ and $f(x) = -g(x)$, and squaring encodes both branches simultaneously. If the same problem is approached by removing the absolute value with a single sign, the branch that is dropped may contain a valid solution. For this reason, when an equation involves even-index radicals or absolute values, both sign possibilities must be carried as candidates and tested against the original equation.

## Loss of roots in rational equations

A common mistake when solving [rational equations](../rational-equations/) is to multiply both sides by the denominator in order to eliminate fractions. When the denominator contains the unknown, this step is legitimate only where the denominator does not vanish. Excluding the values that make the denominator zero does not cause any solution to be lost, since those values do not belong to the domain in the first place. The risk lies in the opposite direction: if a candidate is not checked against the domain, one may retain a value that does not actually satisfy the original equation, an extraneous solution.

A genuine loss of roots occurs instead when the equation is simplified by cancelling a factor of the denominator before solving. Cancellation silently removes from consideration every value that makes the cancelled factor zero. Whether this is harmless depends on whether that value was already excluded from the domain. Consider the equation:

$$\frac{x^2 - 4}{x - 2} = 0$$

Cancelling the factor $(x-2)$ from numerator and denominator yields $x + 2 = 0$, so $x = -2$. The value $x = 2$ is excluded from the domain because it makes the denominator zero. The equation therefore has exactly one solution, $x = -2$, and no root is lost: the cancellation is harmless precisely because $x = 2$ was never an admissible value.

The situation differs when the cancelled factor does not correspond to a domain restriction. Consider the equation:

$$x(x - 3) = 2(x - 3)$$

Cancelling $(x - 3)$ from both sides gives $x = 2$. The value $x = 3$, however, also satisfies the original equation, since both sides equal zero when $x = 3$, and this solution is removed by the cancellation. Reducing the equation to standard form preserves it:

$$
\begin{align}
x(x - 3) - 2(x - 3) &= 0 \\[6pt]
(x - 3)(x - 2) &= 0
\end{align}
$$

The zero-product property then gives both solutions, $x_1 = 2$ and $x_2 = 3$, whereas the incorrect simplification retains only one.

## General principles

Several principles help prevent the unintentional loss of solutions when solving equations.

The most reliable strategy is to move all terms to one side, reduce the equation to zero, and factor the resulting expression. Once the equation is written as a product of factors equal to zero, the zero-product property guarantees that every solution corresponds to the vanishing of at least one factor, and none can be overlooked.

Division of both sides by an expression involving the unknown should be avoided unless that expression is known to be nonzero throughout the domain. When such a division appears necessary, the case in which the divisor equals zero must be analysed separately, since it may itself yield a valid solution.

When an equation involves even-index radicals or absolute values, every admissible sign must be retained as a candidate. Restricting attention to the principal root, or to a single sign, without examining the alternative is a common source of incomplete solution sets.

Substituting each candidate solution back into the original equation remains an essential step, in particular after squaring both sides or performing any transformation that is not strictly reversible. This verification detects both the extraneous solutions introduced by a non-equivalent manipulation and any valid solutions that may have been dropped along the way.
