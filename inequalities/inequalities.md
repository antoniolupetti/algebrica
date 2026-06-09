---
title: Inequalities
source: https://algebrica.org/inequalities/
license: CC BY-NC 4.0
tags:
  - algebraic-inequalities
  - inequalities
  - transcendental-inequalities
---

## Definition

An inequality is a mathematical statement asserting that two expressions stand in an order relation, typically written in the form $F(x) > G(x)$, $F(x) < G(x)$, $F(x) \geq G(x)$, or $F(x) \leq G(x)$, where one or more variables act as unknowns ranging over a specified [set](../types-of-numbers/), such as $\mathbb{R}$. Solving an inequality means determining every value of the variable, within the appropriate [domain](../determining-the-domain-of-a-function/), for which the order relation holds. Many inequalities can be reorganised into the form:

$$F(x) > 0$$

This representation simplifies their study, highlights their structure, and provides a unified framework for the different solution methods. The same form, with the symbol $>$ replaced by $<$, $\geq$, or $\leq$, governs every case.

The solution to an inequality is the set of all values of the variable that make the order relation true. Unlike the [solution of an equation](../equations/), which is typically a discrete collection of points, the solution of an inequality is generally a union of [intervals](../intervals/) of the real line, possibly supplemented by isolated points. Depending on the inequality and its structure, the solution set may consist of:

+ a single interval, bounded or unbounded
+ a union of several disjoint intervals
+ the empty set, when no value satisfies the inequality
+ all of $\mathbb{R}$, when the inequality holds identically

> The endpoints of each interval depend on whether the inequality is strict or non-strict. A strict inequality, written with $>$ or $<$, excludes the boundary points, producing open intervals; a non-strict inequality, written with $\geq$ or $\leq$ includes them, producing closed or half-open intervals.

For trigonometric inequalities the solution set is often infinite and periodic, reflecting the periodicity of the functions involved. For algebraic inequalities, the structure of the solution set is governed by the zeros of the polynomial obtained after moving every term to one side.

## Equivalent inequalities and admissible operations

Two inequalities are equivalent when they have identical solution sets. The objective in solving an inequality is to apply a sequence of transformations that preserve this equivalence, reducing the inequality to a simpler form in which the solution set is apparent. The algebraic rules that govern these transformations descend from the [order properties of the real numbers](../properties-of-real-numbers/), which characterise $\mathbb{R}$ as an ordered field and from which every admissible manipulation can be derived.

Certain operations are guaranteed to yield an equivalent inequality. Adding or subtracting the same expression on both sides leaves both the order relation and the solution set unchanged, exactly as for [equations](../equations/). The behaviour under multiplication and division is more delicate, because the sign of the multiplier affects the direction of the inequality.

+ Multiplying or dividing both sides by a positive constant preserves the direction of the inequality.
+ Multiplying or dividing both sides by a negative constant reverses the direction of the inequality.

This distinction has no parallel in the theory of equations and is the most frequent source of error in elementary work with inequalities. As an illustration, the inequality $-2x > 4$ becomes $x < -2$ after dividing both sides by $-2$, with the inequality sign reversed.

Other operations can disrupt equivalence in less obvious ways. Multiplying both sides by an expression involving the variable requires a [sign analysis](../sign-analysis-in-inequalities/) of that expression, because the direction of the inequality must be reversed precisely on the intervals where the expression is negative. Similarly, squaring both sides is admissible only when both sides are known to be non-negative, a condition that arises naturally in [irrational inequalities](../irrational-inequalities/).

A systematic discussion of the manipulations that can add extraneous values to the solution set or remove valid ones, together with the corresponding countermeasures, is given in the entry on [loss and introduction of solutions](../loss-of-solutions/).

## Algebraic inequalities

Algebraic inequalities are inequalities in which both sides consist entirely of [polynomials](../polynomials/). After moving every term to one side, the problem reduces to studying the sign of a single polynomial $P(x)$. Algebraic inequalities are classified according to the degree of this polynomial.

[Linear inequalities](../linear-inequalities/) have degree $1$. The variable appears to no power higher than the first, and the solution set is always a half-line whenever the leading coefficient is nonzero.

[Quadratic inequalities](../quadratic-inequalities/) have degree $2$ and take the standard form $ax^2 + bx + c > 0$, with $a \neq 0$. The structure of their solution set is governed by the [discriminant](../quadratic-formula/) $\Delta = b^2 - 4ac$ of the associated equation and by the sign of the leading coefficient $a$.

+ If $\Delta > 0$ the solution set is the union of the two outer intervals or the single inner interval between the roots, according to the inequality sign.
+ If $\Delta = 0$ the solution set is either all of $\mathbb{R}$ or the empty set, possibly with the double root included or excluded.
+ If $\Delta < 0$ the quadratic keeps the sign of $a$ throughout, so the solution set is either all of $\mathbb{R}$ or the empty set.

A detailed account of these cases is given in the entry on [quadratic inequalities](../quadratic-inequalities/), and their geometric content is treated in [geometric interpretation of quadratic inequalities](../geometric-interpretation-quadratic-inequalities/).

[Polynomial inequalities](../polynomial-inequalities/) of degree higher than two follow the same principle. The polynomial is factored into linear and irreducible quadratic factors, and the sign of the product is studied through a [sign chart](../sign-analysis-in-inequalities/) that records the contribution of each factor on each interval determined by the real roots.

Among higher-degree inequalities, [binomial](../binomial-inequalities/) and [trinomial inequalities](../trinomial-inequalities/) deserve particular attention. These contain only two or three distinct terms and can often be solved by substitution or by extracting a root, reducing the problem to a lower-degree inequality.

## Rational inequalities

[Rational inequalities](../rational-inequalities/) contain at least one fractional expression whose numerator and denominator are polynomials. After moving every term to one side and combining over a common denominator, the problem reduces to one of the canonical forms:

$$\frac{P(x)}{Q(x)} > 0 \qquad \frac{P(x)}{Q(x)} \geq 0$$

The natural domain excludes every value for which $Q(x) = 0$, and these excluded values can never belong to the solution set. The sign of the ratio is determined by the signs of $P(x)$ and $Q(x)$ separately, with the rule that the ratio is positive when both share the same sign and negative when they have opposite signs.

> Clearing the denominator by multiplying both sides by $Q(x)$ is generally not admissible, because the sign of $Q(x)$ depends on $x$ and would require a case analysis. The standard procedure works with the ratio in its canonical form and analyses the sign of numerator and denominator through a sign chart.

## Irrational inequalities

[Irrational inequalities](../irrational-inequalities/) have the variable inside a radical. A typical inequality contains one radical, for example:

$$\sqrt[n]{f(x)} > g(x)$$

The technique depends on the parity of the index and on the sign of the two sides. When the index is even, the radicand must be non-negative for the radical to be defined in the reals, and squaring both sides is admissible only when both sides have the same sign. 

The resolution therefore splits into cases, each governed by a system of polynomial inequalities. When the index is odd, the radical is defined for every real value of the radicand and the squaring step is replaced by raising both sides to the $n$-th power without restrictions on the sign.

Each case requires careful verification, since raising both sides to an even power can introduce extraneous solutions that do not satisfy the original inequality.

## Absolute value inequalities

[Inequalities with absolute value](../inequalities-with-absolute-value/) are inequalities in which the unknown appears inside an [absolute value](../absolute-value/) expression. The simplest cases take the form $|x| < a$ or $|x| > a$, where $a$ is a real constant, and the solution set is described by a pair of linear inequalities.

+ The inequality $|x| < a$ with $a > 0$ is equivalent to $-a < x < a$, producing the open interval $(-a, a)$.
+ The inequality $|x| > a$ with $a > 0$ is equivalent to $x < -a$ or $x > a$, producing the union of two unbounded intervals.
+ When $a \leq 0$, the structure degenerates: $|x| < a$ has no solution, while $|x| > a$ is satisfied by every real $x$ if $a < 0$ and by every $x \neq 0$ if $a = 0$.

Absolute value inequalities that contain polynomial or rational expressions require case analysis based on the sign of the inner expression. Each case produces a system of inequalities, and the final solution set is obtained by collecting the solutions of all cases.

## Transcendental inequalities

Transcendental inequalities are inequalities in which one or more variables appear within transcendental functions, such as [exponential](../exponential-function/), [logarithmic](../logarithmic-function/), or [trigonometric functions](../sine-function/). These inequalities go beyond polynomial or rational forms, and their solution often relies on the monotonicity properties of the functions involved.

[Logarithmic inequalities](../logarithmic-inequalities/) involve the variable inside a logarithmic expression. They are solved by using the properties of logarithms to isolate the unknown, while accounting for the condition that the argument of every logarithm must be strictly positive.

[Exponential inequalities](../exponential-inequalities/) have the variable in the exponent. The solution exploits the monotonicity of the exponential function: the inequality between exponents has the same direction as the original when the base is greater than one, and the opposite direction when the base lies strictly between zero and one.

[Trigonometric inequalities](../trigonometric-inequalities/) involve periodic functions such as $\sin(x)$, $\cos(x)$, or $\tan(x)$. The periodicity produces solution sets that are themselves periodic, typically expressed as the union of infinitely many intervals separated by the period of the function.

## Inequalities in two variables

An inequality is said to be in two variables when its solution set is a subset of the Cartesian plane $\mathbb{R}^2$ rather than of the real line. A [linear inequality in two variables](../linear-inequalities-in-two-variables/) takes the form $ax + by + c > 0$, with the symbol $>$ possibly replaced by $<$, $\geq$, or $\leq$, and its solution set is always a half-plane bounded by the line $ax + by + c = 0$. The boundary line is included or excluded according to whether the inequality is non-strict or strict, and the half-plane to be selected is identified by the test point method.

The same construction extends to several inequalities considered simultaneously. A [system of linear inequalities in two variables](../systems-of-linear-inequalities-in-two-variables/) defines a region of the plane obtained as the intersection of the corresponding half-planes. This region is always convex, possibly empty, possibly unbounded, and it is the feasible region of the system. When the region is a bounded convex polygon, the vertices play a distinguished role in the optimisation of a linear objective function over the region, which is the geometric starting point of linear programming.

When the function defining the inequality is not a linear combination of the two unknowns, the inequality belongs to the class of [nonlinear inequalities in two variables](../nonlinear-inequalities-in-two-variables/). The boundary is no longer a line but a curve, typically a [conic section](../conic-sections/) such as a parabola, a circle, an ellipse, or a hyperbola, and the solution set is one of the regions of the plane determined by this curve. The test point method identifies the correct region exactly as in the linear case, and systems of nonlinear inequalities produce feasible regions that can be non-convex and bounded by arcs of different curves.

## Systems of inequalities

A [system of inequalities](../systems-of-inequalities/) arises when several inequalities must be satisfied simultaneously by the same variable. The solution set of the system is the intersection of the solution sets of the individual inequalities, since a value of the variable belongs to the solution of the system if and only if it satisfies every inequality at once.

The intersection of intervals is computed graphically on a number line, where each inequality is represented by its solution set and the system solution is the region in which all the corresponding marks coincide. This procedure is used systematically in the case analysis required by absolute value, irrational, and parametric inequalities. The two-variable analogue, in which the intersection takes place in the Cartesian plane rather than on the real line, is treated in the entry on [systems of linear inequalities in two variables](../systems-of-linear-inequalities-in-two-variables/).

A related notational variant of the system is the [compound inequality](../compound-inequalities/), in which two inequalities sharing a common middle expression are combined into a single chained statement of the form $a < f(x) < b$. The compound notation is solved by operating on all three parts at once when the unknown is confined to the middle expression, and it reduces to a system of two component inequalities when the unknown appears in more than one part.

## Inequalities with parameters

When some of the coefficients of an inequality depend on a real quantity treated as a constant, the inequality belongs to the broader class of [inequalities with parameters](../inequalities-with-parameters/). The solution set is no longer a fixed subset of $\mathbb{R}$, but a family of subsets indexed by the parameter, and the analysis proceeds by partitioning the parameter range into regions where the solution behaves uniformly.

The two basic cases are treated separately in the entries on [linear inequalities with parameters](../linear-inequalities-with-parameters/) and [quadratic inequalities with parameters](../quadratic-inequalities-with-parameters/). The general principle is the same in both cases: every parameter value that changes the sign of a coefficient or the sign of the discriminant marks a transition between qualitatively different solution structures and must be examined separately.
