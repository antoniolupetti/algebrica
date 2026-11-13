---
title: Topology of the Real Line
source: https://algebrica.org/topology-of-the-real-line/
license: CC BY-NC 4.0
tags:
  - accumulation-point
  - boundary-point
  - closed-set
  - closure
  - compactness
  - connectedness
  - heine-borel-theorem
  - interior-point
  - isolated-point
  - neighborhood
  - open-cover
  - open-set
  - real-line
---

## Neighborhoods and open sets

The distance between two [real numbers](../real-numbers/) $x$ and $y$ is $|x-y|.$ The open neighborhood centered at $x$ with radius $\varepsilon\gt 0$ is the [open interval](../intervals/) of points whose distance from $x$ is less than $\varepsilon,$ and it can be written as:

$$
I_\varepsilon(x)=(x-\varepsilon,x+\varepsilon)
=\{y\in\mathbb{R}\mid |y-x|\lt\varepsilon\} \tag{1}
$$

Removing $x$ from the interval in $(1)$ gives the punctured neighborhood centered at $x$ with radius $\varepsilon:$

$$
I_\varepsilon^*(x)=I_\varepsilon(x)\setminus\{x\}
=\{y\in\mathbb{R}\mid 0\lt |y-x|\lt\varepsilon\} \tag{2}
$$

A set $U\subseteq\mathbb{R}$ is open if for every $x\in U$ there is a radius $\varepsilon\gt 0$ such that the open neighborhood $I_\varepsilon(x)$ in $(1)$ is entirely contained in $U.$ For example, if $x\in(a,b),$ taking the smaller of the distances $x-a$ and $b-x$ as the radius gives a neighborhood contained in $(a,b),$ so the interval is open.

We now consider two properties that define the topology of $\mathbb{R}.$ The empty set and $\mathbb{R}$ are open, and so is the union of any family of open sets, because each point of the union belongs to at least one set in the family and therefore has a neighborhood contained in that set. For a point in the intersection of finitely many open sets, choose, for each set, a neighborhood of the point contained in that set. The smallest of the chosen radii is still positive, and the neighborhood with that radius is contained in every set, so the intersection is open.

For infinitely many open sets, the neighborhood radii can become arbitrarily small. For example, all the neighborhoods $I_{1/n}(0)$ contain $0,$ but any $x\neq 0$ lies outside at least one of them, since the [Archimedean property](../supremum-and-infimum/) allows us to choose $n$ with $1/n\lt |x|,$ which gives:

$$
\bigcap_{n=1}^{\infty} I_{1/n}(0)=\{0\} \tag{3}
$$

In $(3),$ the common point is $0,$ but none of its open neighborhoods is contained in the intersection, so the intersection is not open. The criterion for openness can also be applied to individual points of a set $E\subseteq\mathbb{R}.$ A point is interior to $E$ if it has a neighborhood contained in $E$ and exterior to $E$ if it has a neighborhood contained in the complement $\mathbb{R}\setminus E.$ The points whose neighborhoods all meet both sets form the boundary $\partial E.$ The interior $E^\circ$ is the union of all open sets contained in $E,$ so it is the largest of them. By the preceding criterion, $E$ is open if and only if $E=E^\circ.$ For example, if $E=(0,1],$ the interior is $(0,1),$ the exterior is $(-\infty,0)\cup(1,+\infty)$ and the boundary is $\{0,1\}.$

## Accumulation points and closed sets

A point $x$ is an accumulation point of $E$ if every open neighborhood of $x$ contains at least one point of $E$ other than $x,$ or equivalently, if every punctured neighborhood in $(2)$ contains at least one point of $E.$ The set of accumulation points is denoted by $E'.$ A point $x\in E$ is isolated if it has a neighborhood that meets $E$ only at $x.$

A point $x$ belongs to $E'$ if and only if there is a [sequence](../sequences/) $(x_n)$ of points of $E\setminus\{x\}$ that converges to $x.$ Indeed, if $x\in E',$ then for each positive integer $n$ one can choose a point $x_n$ of $E$ in the punctured neighborhood of radius $1/n,$ obtaining a sequence that converges to $x.$ Conversely, a sequence of points of $E$ distinct from $x$ that converges to $x$ has terms in every punctured neighborhood of $x.$

By the [Bolzano-Weierstrass theorem](../convergent-and-divergent-sequences/), every infinite bounded subset of $\mathbb{R}$ has at least one accumulation point. The notion also enters the definition of the [limit of a function](../limits/), where the point that the variable approaches must be an accumulation point of the domain.

A set $F$ is closed if its complement is open, meaning that every point outside $F$ has a neighborhood disjoint from $F.$ This is equivalent to requiring that $F'\subseteq F,$ because for $x\notin F$ any point of $F$ in a neighborhood of $x$ also lies in the corresponding punctured neighborhood. By the sequential criterion, the condition is equivalent to requiring that the limit of every convergent sequence of points of $F$ belong to $F.$ Indeed, a limit outside $F$ would be an accumulation point outside $F,$ and such a point would give rise to a sequence of this kind.

The interval $[a,b]$ is closed because its complement is the union of two open intervals. The interval $(0,1]$ is not open because $1$ is not an interior point, and it is not closed because $0$ is an accumulation point that does not belong to the interval. By [De Morgan's laws](../de-morgan-laws/), arbitrary intersections and finite unions of closed sets are closed.
## Closure and density

We now define the closure $\overline{E}$ as the smallest closed set containing $E,$ obtained by intersecting all the closed sets that contain it. A point lies outside $\overline{E}$ if and only if it has a neighborhood disjoint from $E.$ Indeed, the complement of $\overline{E}$ is open and disjoint from $E,$ while the complement of a neighborhood disjoint from $E$ is a closed set containing $E$ and hence also $\overline{E}.$ This gives the following identities:

$$
\begin{align}
x\in\overline{E}
&\iff I_\varepsilon(x)\cap E\neq\emptyset
\quad\text{for every }\varepsilon\gt 0 \tag{4} \\[6pt]
\overline{E} &= E\cup E' \tag{5} \\[6pt]
\partial E &= \overline{E}\cap\overline{\mathbb{R}\setminus E}
 = \overline{E}\setminus E^\circ \tag{6}
\end{align}
$$

If $x\in E,$ every neighborhood of $x$ meets $E$ at least at $x$ itself. If $x\notin E,$ the condition in $(4)$ is equivalent to requiring that every punctured neighborhood of $x$ meet $E,$ which gives $(5).$ Moreover, a point lies outside the closure of the complement of $E$ exactly when it has a neighborhood contained in $E,$ so the set of points outside that closure is $E^\circ.$

A set $E$ is dense in $\mathbb{R}$ if $\overline{E}=\mathbb{R},$ meaning that it meets every nonempty open set. Every nonempty open interval contains both rational and [irrational numbers](../irrational-numbers/), so both sets are dense and $(6)$ gives $\partial\mathbb{Q}=\mathbb{R}.$ Since $\mathbb{Q}$ is countable, the real line is separable, meaning that it has a countable dense subset.

## Connectedness and intervals

A set $S\subseteq\mathbb{R}$ is connected if it cannot be written as the union of two disjoint nonempty subsets that are open in $S.$ A subset of $S$ is open in $S$ if it is the intersection of $S$ with an open set of the real line. If a set contains two points but omits a point $c$ between them, its intersections with $(-\infty,c)$ and $(c,+\infty)$ separate it into two nonempty subsets open in $S.$ Thus every nonempty connected set is an interval.

Suppose now that an interval $I$ is the union of two disjoint nonempty subsets $U$ and $V$ that are open in $I.$ Having chosen $u\in U$ and $v\in V,$ we may assume that $u\lt v.$ Since $I$ is an interval, it contains $[u,v].$ Let $c$ be the supremum of $U\cap[u,v].$ Since $V$ contains a relative neighborhood of $v,$ we have $c\lt v.$ If $c\in U,$ the fact that $U$ is open in $I$ gives points of $U\cap[u,v]$ greater than $c,$ while if $c\in V,$ there is a neighborhood of $c$ disjoint from $U\cap[u,v].$ Both cases contradict the definition of $c,$ so every interval is connected and the only subsets of the real line that are both open and closed are $\emptyset$ and $\mathbb{R}.$

Every nonempty open set in $\mathbb{R}$ can be written as a union of pairwise disjoint open intervals. For each point of the open set, take all the open intervals that contain the point and are contained in the set. Their union is again an open interval because the intervals share a point. Any two maximal intervals obtained in this way that intersect must coincide, since their union would otherwise be a larger open interval. Each interval contains [a rational number](../rational-numbers/), and disjoint intervals contain distinct rational numbers, so the decomposition has at most countably many intervals.

## Compactness and the Heine-Borel theorem

An open cover of $K\subseteq\mathbb{R}$ is a family of open sets whose union contains $K.$ The set $K$ is compact if every open cover of $K$ has a finite subfamily that still covers $K.$ For example, the intervals $(1/n,1)$ for $n\geq 2$ cover $(0,1),$ but the union of any finite selection of them is $(1/N,1),$ where $N$ is the largest index chosen, and leaves points near $0$ uncovered.

The Heine-Borel theorem states that a subset of $\mathbb{R}$ is compact if and only if it is closed and bounded. To prove the first implication, let $K$ be compact and nonempty. The intervals $(-n,n)$ for $n\geq 1$ cover $K,$ and the union of a finite subcover is the interval with the largest index, so $K$ is bounded. To show that $K$ is closed, fix $y\notin K$ and consider the following open sets:

$$
A_n=\left(-\infty,y-\frac{1}{n}\right)\cup
\left(y+\frac{1}{n},+\infty\right)
\qquad n=1,2,\ldots \tag{7}
$$

The sets $A_n$ form an increasing family and cover $K$ because each point of $K$ is at a positive distance from $y.$ A finite subcover places all of $K$ in a single set $A_N,$ so $I_{1/N}(y)$ is disjoint from $K.$ Thus every point of the complement has a neighborhood contained in the complement. The empty set is also compact, closed and bounded.

For the converse, suppose that an open cover of $J_1=[a,b]$ has no finite subcover. Bisecting $J_1$ gives two closed intervals, at least one of which has the same property, since otherwise the union of the two finite subcovers would cover $J_1.$ Repeating the bisection produces nested closed intervals $J_n$ of length $(b-a)/2^{n-1},$ each with no finite subcover. By [completeness](../real-numbers/), the set of left endpoints has a supremum $c.$ Since the intervals are nested, each right endpoint is an [upper bound](../supremum-and-infimum/) for all the left endpoints, so $c$ belongs to every $J_n.$ An open set $A$ in the cover contains $c$ and therefore contains a neighborhood $I_\varepsilon(c).$ For sufficiently large $n,$ the length of $J_n$ is less than $\varepsilon,$ and since $c\in J_n,$ we have:

$$
J_n\subseteq I_\varepsilon(c)\subseteq A \tag{8}
$$

The set $A$ alone covers $J_n,$ contradicting the assumption under which $J_n$ was chosen. Thus every closed bounded interval is compact. If $K$ is closed and bounded, place it in an interval $[a,b]$ and add the open set $\mathbb{R}\setminus K$ to any open cover of $K.$ The resulting family covers $[a,b]$ and has a finite subcover, from which the complement of $K$ can be removed if it was selected.

## Compactness and sequences

A set $K\subseteq\mathbb{R}$ is compact if and only if every sequence of points of $K$ has a subsequence that converges to a point of $K.$

To prove the equivalence, suppose that $K$ is compact. By the Heine-Borel theorem, $K$ is closed and bounded, so every sequence of points of $K$ is bounded. Furthermore, by the Bolzano-Weierstrass theorem, every such sequence has a convergent subsequence. Since $K$ is closed, the limit belongs to $K.$

Conversely, suppose that every sequence of points of $K$ has a subsequence that converges to a point of $K.$ If $K$ were unbounded, we could choose a sequence $(x_n)$ of points of $K$ with $|x_n|\gt n,$ all of whose subsequences would be unbounded and hence divergent. If $K$ were not closed, the sequential criterion for closedness would give a sequence of points of $K$ converging to a point outside $K,$ and every subsequence would have the same limit. The assumption therefore implies that $K$ is closed and bounded, so it is compact by the Heine-Borel theorem.

The image of a compact set under a [continuous function](../continuous-functions/) is compact. This property yields the [extreme value theorem](../weierstrass-theorem/), which states that a continuous real-valued function on a nonempty closed bounded interval attains its maximum and minimum.
