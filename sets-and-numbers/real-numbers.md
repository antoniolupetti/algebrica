---
title: Real Numbers
source: https://algebrica.org/real-numbers/
license: CC BY-NC 4.0
tags:
  - archimedean-property
  - bolzano-weierstrass
  - cauchy-sequence
  - completeness
  - dedekind-cut
  - density
  - nested-intervals
  - nth-root
  - ordered-field
  - real-line
  - real-numbers
  - uncountability
---

## Field and order structure

The real numbers are introduced as a structure characterised by a combination of algebraic and order properties. These properties determine their behaviour and distinguish it from all other numerical fields. The real numbers form a [field](../fields/) under addition and multiplication. Both operations are associative and commutative, multiplication distributes over addition, and every nonzero real number admits a multiplicative inverse. The additive identity is $0$ and the multiplicative identity is $1$. The algebraic axioms underlying this structure are discussed in detail in [properties of real numbers](../properties-of-real-numbers/). Beyond its algebraic structure, $\mathbb{R}$ carries a total order relation, denoted $<$. For any two elements $x, y \in \mathbb{R}$, exactly one of the following three relations holds:

$$
x < y \qquad x = y \qquad y < x
$$

The order is compatible with the field operations:

+ If $x < y$, then $x + z < y + z$ for every $z \in \mathbb{R}$.
+ If $x < y$ and $z > 0$, then $xz < yz$.

A field equipped with a total order satisfying these compatibility conditions is an ordered field. Both $\mathbb{Q}$ and $\mathbb{R}$ are ordered fields. What separates the two is the completeness property introduced below.

## The real line

The real numbers admit a geometric interpretation that makes their order and completeness clear. Fix an arbitrary point on a straight line and label it $0$. Fix a second point to its right and label it $1$. Every real number $x$ then corresponds to a unique point on the line: positive numbers lie to the right of $0$, negative numbers to the left, at a distance from the origin equal to the [absolute value](../absolute-value/) $|x|$. 

![IMG. 1](svg/real-numbers-1.svg)


This correspondence is a bijection between $\mathbb{R}$ and the points of the line, and it preserves the order. The relation $x < y$ holds if and only if the point corresponding to $x$ lies to the left of the point corresponding to $y$.


## The completeness axiom

The property that distinguishes $\mathbb{R}$ from $\mathbb{Q}$ is completeness. It expresses the absence of gaps. Every position on the number line that could be approached by a [sequence](../sequences/) of [rational numbers](../rational-numbers/) is actually occupied by a real number. The rational numbers, by contrast, leave the line with infinitely many holes, one for each [irrational](../irrational-numbers/) value.

The formulation relies on the notion of an upper bound. A subset $S \subseteq \mathbb{R}$ is bounded above if there exists a real number $M$ such that $x \leq M$ for every $x \in S$. Such a number $M$ is called an upper bound of $S$. When a smallest upper bound exists, it is called the supremum of $S$, or least upper bound, and is denoted $\sup S$.

The completeness axiom of the real numbers can be stated as follows: every non-empty subset of $\mathbb{R}$ that is bounded above has a [supremum](../supremum-and-infimum/) in $\mathbb{R}$. The statement is known as the least upper bound property. The rational numbers fail to satisfy it. To see why, consider the following [set](../sets/):

$$
S = \\{ q \in \mathbb{Q} : q^2 < 2 \\}
$$

This set is non-empty and bounded above within $\mathbb{Q}$, yet it has no least upper bound in $\mathbb{Q}$. The value $\sqrt{2}$, which plays the role of $\sup S$, is irrational and therefore absent from $\mathbb{Q}$. In $\mathbb{R}$, the number $\sqrt{2}$ exists and one has $\sup S = \sqrt{2}$.

Completeness produces the number $\sqrt{2}$ itself. Formed inside $\mathbb{R},$ the set $\\{ x \in \mathbb{R} : x^2 < 2 \\}$ is non-empty and bounded above, so it has a supremum $r.$ The two alternatives $r^2 < 2$ and $r^2 > 2$ each lead to a contradiction, since a number slightly above or slightly below $r$ would still lie in the set or still bound it, so $r^2 = 2.$ The same argument applied to $\\{ x \in \mathbb{R} : x^n < c \\}$ for $c > 0$ gives a supremum whose $n$-th power equals $c,$ so every positive real has a unique positive $n$-th root for each [natural number](../natural-numbers/) $n.$ Radicals are defined in $\mathbb{R}$ through this construction, and the same suprema do not exist in $\mathbb{Q}.$

A symmetric notion applies to sets bounded below. A subset $S \subseteq \mathbb{R}$ is bounded below if there exists $m \in \mathbb{R}$ such that $x \geq m$ for all $x \in S$. The greatest lower bound, or [infimum](../supremum-and-infimum/), is denoted $\inf S$. The completeness axiom implies that every non-empty subset of $\mathbb{R}$ bounded below has an infimum in $\mathbb{R}$.

## The Archimedean property

A consequence of completeness is the Archimedean property of $\mathbb{R}$. For every real number $x$, there exists a [natural number](../natural-numbers/) $n$ such that $n > x$. Equivalently, the set of natural numbers $\mathbb{N}$ is not bounded above in $\mathbb{R}$. The argument runs as follows:

+ Suppose, for contradiction, that $\mathbb{N}$ were bounded above in $\mathbb{R}$.
+ By the completeness axiom, $\mathbb{N}$ would then have a supremum that we call $s = \sup \mathbb{N}$.
+ Since $s - 1 < s$, the number $s - 1$ is not an upper bound of $\mathbb{N}$, so there exists $n \in \mathbb{N}$ with $n > s - 1$.
+ It follows that $n + 1 > s$. Since $n + 1 \in \mathbb{N}$, this contradicts $s$ being an upper bound of $\mathbb{N}$.

To illustrate the property concretely, consider the real number $x = 7.4$. The Archimedean property guarantees the existence of a natural number greater than $x$: since $8 > 7.4$, the smallest such natural number is $n = 8$. The result, elementary as it appears, depends on the completeness of $\mathbb{R}$ and fails in ordered fields that do not satisfy it.

## Dedekind cuts

A Dedekind cut is a subset $A \subseteq \mathbb{Q}$ satisfying three conditions: $A$ is non-empty and $A \neq \mathbb{Q}$; if $q \in A$ and $p < q$ then $p \in A$; and $A$ has no greatest element. The set $\mathbb{R}$ is then defined as the collection of all Dedekind cuts of $\mathbb{Q}$.

To illustrate, the rational number $r \in \mathbb{Q}$ corresponds to the cut $A_r = \\{ q \in \mathbb{Q} : q < r \\}$. An irrational number such as $\sqrt{2}$ corresponds instead to the cut:

$$
A = \\{ q \in \mathbb{Q} : q < 0 \\} \cup \\{ q \in \mathbb{Q} : q > 0 \text{ and } q^2 < 2 \\}
$$

This set satisfies all three conditions, yet has no rational supremum in $\mathbb{Q}$. The cut carves out a position on the rational line where no rational number sits, and it is precisely this gap that the construction fills by declaring $A$ itself to be a real number.

The algebraic structure of $\mathbb{R}$ is then built directly from set-theoretic operations on cuts. Addition is defined by setting:

$$
A + B = \\{ p + q : p \in A, \ q \in B \\}
$$

The order is given by inclusion: $A \leq B$ if and only if $A \subseteq B$. These definitions make $\mathbb{R}$ into a totally ordered field. The completeness of $\mathbb{R}$ in this construction has the following proof: given a non-empty collection $S$ of cuts that is bounded above, the supremum is the union $\bigcup_{A \in S} A$, which is itself a cut and is the least upper bound of $S$ by construction.

> The Dedekind construction builds the real numbers from the order structure of $\mathbb{Q}$ alone. Its main contribution is to show that the completeness of $\mathbb{R}$ is a consequence of filling in all the gaps that the rational order leaves open.

## Cauchy sequence construction

A second construction of $\mathbb{R}$ starts from a limitation of $\mathbb{Q}$. Not every [Cauchy sequence](../cauchy-sequence/) of rational numbers converges to a rational number. A sequence $(x_n)_{n \in \mathbb{N}}$ in $\mathbb{Q}$ is a Cauchy sequence if for every $\varepsilon \in \mathbb{Q}^+$ there exists $N \in \mathbb{N}$ such that:

$$
m, n \geq N \implies |x_m - x_n| < \varepsilon
$$

The terms of the sequence cluster together without the sequence needing to refer to a [limit](../limits/), which may not yet exist in $\mathbb{Q}$. The sequence of rational approximations to $\sqrt{2}$ is a standard example:

$$
\left(1, \ \frac{3}{2}, \ \frac{7}{5}, \ \frac{17}{12}, \ \ldots\right)
$$

The sequence is Cauchy in $\mathbb{Q}$, yet its limit lies outside $\mathbb{Q}$. Two Cauchy sequences $(x_n)$ and $(y_n)$ in $\mathbb{Q}$ are declared equivalent if their difference tends to zero:

$$
(x_n) \sim (y_n) \iff \lim_{n \to \infty} |x_n - y_n| = 0
$$

One verifies that $\sim$ is an equivalence relation. The real numbers are then defined as the set of equivalence classes:

$$
\mathbb{R} := C/{\sim}
$$

Here $C$ denotes the collection of all Cauchy sequences in $\mathbb{Q}$. Addition and multiplication are defined termwise:

$$
[(x_n)] + [(y_n)] = [(x_n + y_n)]
$$

$$
[(x_n)] \cdot [(y_n)] = [(x_n y_n)]
$$

These operations are well-defined, that is, independent of the choice of representative. The order is given by $[(x_n)] \leq [(y_n)]$ when either $(x_n) \sim (y_n)$ or there exists $N \in \mathbb{N}$ such that $x_n < y_n$ for all $n \geq N$. The rational numbers embed into $\mathbb{R}$ via $q \mapsto [(q, q, q, \ldots)]$, preserving both operations and order.

The real number $\sqrt{2}$, for instance, is the equivalence class of any Cauchy sequence of rationals converging to it, such as $(1, 1.4, 1.41, 1.414, \ldots)$. Two such sequences satisfy $(x_n) \sim (y_n)$ and therefore define the same real number. Completeness in this construction means that every Cauchy sequence of real numbers converges to a real number. The Dedekind and Cauchy constructions are isomorphic as complete ordered fields, and they describe exactly the same mathematical object.

## Consequences of completeness

The rational numbers are dense in $\mathbb{R}$: between any two distinct real numbers there exists a rational number. For every $x, y \in \mathbb{R}$ with $x < y$, there exists $q \in \mathbb{Q}$ such that $x < q < y$. This follows from the Archimedean property. Given $x < y$, one finds a natural number $n$ satisfying $n(y - x) > 1$, and among the integers $m$ with $m > nx$ one can identify one for which $x < m/n < y$ holds.

The same density is the basis for the standard method of proving non-strict inequalities in $\mathbb{R}.$ If a real number $x$ satisfies $x \leq \varepsilon$ for every $\varepsilon > 0,$ then $x \leq 0,$ since a positive $x$ would exceed the admissible choice $\varepsilon = x/2.$ In the version with absolute value, $|x| \leq \varepsilon$ for all $\varepsilon > 0$ forces $x = 0.$ An analyst proves an equality by bounding a difference below every positive threshold, and the same technique returns in the study of [limits](../limits/).

Despite the density of $\mathbb{Q}$ in $\mathbb{R}$, the two sets differ in cardinality. The rational numbers are countable, that is, their elements can be placed in a one-to-one correspondence with the natural numbers. The real numbers are uncountable, since no such correspondence exists. This result implies that the [irrational numbers](../irrational-numbers/), which form the set $\mathbb{R} \setminus \mathbb{Q}$, are far more numerous than the rationals.

The nested interval theorem supplies the argument behind this uncountability. A sequence of closed intervals $I_n = [a_n, b_n]$ is nested when $I_1 \supseteq I_2 \supseteq I_3 \supseteq \cdots$. Completeness guarantees that their intersection contains at least one point:

$$
\bigcap_{n=1}^{\infty} I_n \neq \emptyset
$$

The left endpoints form a non-decreasing sequence bounded above by every $b_m$, so they admit a supremum $x = \sup_n a_n$ satisfying $a_n \leq x \leq b_n$ for all $n$. The point $x$ then lies in every interval. When the lengths $b_n - a_n$ tend to zero, the intersection reduces to this single point. The rational numbers fail the property: a sequence of nested intervals with rational endpoints shrinking around $\sqrt{2}$ has empty intersection in $\mathbb{Q}$.

The uncountability of $\mathbb{R}$ follows by contradiction. Suppose the real numbers in $[0, 1]$ could be arranged in a list $x_1, x_2, x_3, \ldots$. Choose a closed interval $I_1 \subseteq [0, 1]$ that excludes $x_1$, then a closed interval $I_2 \subseteq I_1$ that excludes $x_2$, and continue so that $x_n \notin I_n$ at every step. The nested interval theorem provides a point $x \in \bigcap_n I_n$. This $x$ differs from each $x_n$ and therefore escapes the list, contradicting the assumption that the list was complete.

A second proof of the same result, Cantor's diagonal argument, works directly with decimal expansions. Write each number of the supposed list as $x_k = 0.d_{k1} d_{k2} d_{k3} \ldots,$ and build a new number $y = 0.e_1 e_2 e_3 \ldots$ whose $k$-th digit $e_k$ is chosen to differ from $d_{kk},$ for example $e_k = 1$ when $d_{kk} \neq 1$ and $e_k = 2$ when $d_{kk} = 1.$ By construction $y$ disagrees with $x_k$ in the $k$-th place for every $k,$ so it is absent from the list, and $[0, 1]$ cannot be enumerated. Selecting the digits from $\\{ 1, 2 \\}$ avoids the two-valued expansions such as $0.4999\ldots = 0.5000\ldots,$ which are the only source of ambiguity in decimal notation.

The Bolzano-Weierstrass theorem is a further consequence of completeness. Every bounded sequence of real numbers has a convergent subsequence. The result guarantees that bounded infinite sets cannot spread indefinitely without accumulating somewhere, and it underpins the theory of [limits](../limits/), continuous functions, and compactness in $\mathbb{R}$.

## Uniqueness of $\mathbb{R}$

The real number system is the unique complete ordered field. Any two complete ordered fields are isomorphic as ordered fields, and the isomorphism between them is unique. Up to a structure-preserving bijection, $\mathbb{R}$ is the unique completion of $\mathbb{Q}$.

> Beyond its self-contained algebraic structure, $\mathbb{R}$ is the prototypical scalar field for linear algebra. The Euclidean spaces $\mathbb{R}^n$ are the basic examples of [vector spaces](../vector-spaces/) over $\mathbb{R}$, and any other field can play the same structural role, although the analytic properties that depend on completeness and order are specific to $\mathbb{R}$.

## Intervals

Among the subsets of $\mathbb{R}$, [intervals](../intervals/) occupy a central role. An interval is a subset $I \subseteq \mathbb{R}$ with the property that, whenever two points belong to it, every point lying between them also belongs to it. Intervals may be bounded, such as the open interval $(a, b)$ or the closed interval $[a, b]$, or unbounded, such as $[a, +\infty)$ or $(-\infty, b)$. The entire real line is itself an interval, denoted $(-\infty, +\infty)$.

Intervals vary widely in length yet share a single cardinality. The linear map $x \mapsto 2x$ sends $[0, 1]$ onto $[0, 2]$ bijectively, and the tangent function carries the bounded interval $(-\pi/2, \pi/2)$ onto the whole line, so even a bounded interval matches $\mathbb{R}$ point for point. The intervals $[0, 1]$ and $(0, 1)$ have the same cardinality too, although writing down an explicit bijection between them takes more effort. Length still separates these intervals, but it measures size on a finer scale than cardinality does.
