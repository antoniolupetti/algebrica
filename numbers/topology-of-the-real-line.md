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
  - heine-borel-theorem
  - interior-point
  - isolated-point
  - neighborhood
  - open-cover
  - open-set
  - real-line
---

## Introduction

The topology of the real line is the family of open [subsets](../sets/) of $\mathbb{R}.$ On the [real line](../real-numbers/) these sets are defined through the distance $|x-y|$ between two points. A set is open when each of its points is the center of an open interval contained in the set. The family of all such sets is the standard topology of $\mathbb{R},$ and membership in its open sets describes proximity without reference to distance.

The notions are neighborhoods, interior and boundary points, accumulation and isolated points, open and closed sets, closure and interior. The Heine-Borel theorem states that a subset of $\mathbb{R}$ is compact if and only if it is closed and bounded.

## Neighborhoods, interior and boundary points

Given a point $x\in\mathbb{R}$ and a radius $\varepsilon>0,$ the $\varepsilon$-neighborhood of $x$ is the open [interval](../intervals/):

$$
I_\varepsilon(x)=(x-\varepsilon,x+\varepsilon)=\{y\in\mathbb{R} \mid |y-x|<\varepsilon\}
$$

Its points are those whose distance from $x,$ measured by the [absolute value](../absolute-value/), is smaller than $\varepsilon.$ If $0<\delta<\varepsilon,$ then $I_\delta(x)\subseteq I_\varepsilon(x).$

The punctured $\varepsilon$-neighborhood of $x$ has all the points of $I_\varepsilon(x)$ except its center:

$$
I_\varepsilon^*(x)=I_\varepsilon(x)\setminus\{x\}=\{y\in\mathbb{R} \mid 0<|y-x|<\varepsilon\}
$$

The punctured neighborhood contains the points near $x$ but not $x.$ It is used in the definitions of accumulation points and limits, which concern behavior arbitrarily close to a point and do not require a value at the point.

Let $E\subseteq\mathbb{R}$ and let $x$ be a point of the line. Exactly one of three situations occurs.

+ $x$ is an interior point of $E$ when some neighborhood of $x$ is contained in $E.$
+ $x$ is an exterior point of $E$ when some neighborhood of $x$ is contained in the complement $\mathbb{R}\setminus E.$
+ $x$ is a boundary point of $E$ when every neighborhood of $x$ contains at least one point of $E$ and at least one point of $\mathbb{R}\setminus E.$

The three classes are pairwise disjoint and cover $\mathbb{R}.$ The set of interior points is the interior of $E,$ written $E^{\circ},$ and the set of boundary points is the boundary of $E,$ written $\partial E.$ An interior point belongs to $E,$ an exterior point does not, and a boundary point may lie in $E$ or in its complement.

For $E=(0,1]$ the interior is $(0,1),$ the exterior is $(-\infty,0)\cup(1,+\infty)$ and the boundary is $\{0,1\},$ where $1\in E$ and $0\notin E.$ For $E=\mathbb{Q},$ every neighborhood of a real number contains both rational and irrational numbers, so no point is interior or exterior to $\mathbb{Q},$ and $\partial\mathbb{Q}=\mathbb{R}.$

## Open sets

A set $A\subseteq\mathbb{R}$ is open when every point of $A$ is an interior point of $A,$ that is, when $A=A^{\circ}.$ For each $x\in A$ there is a radius $\varepsilon>0,$ depending on $x,$ such that $I_\varepsilon(x)\subseteq A.$

The bounded interval $(a,b)$ is open. Let $x\in(a,b)$ and put $\varepsilon=\min\{x-a,b-x\},$ a positive number because $a<x<b.$ If $|y-x|<\varepsilon,$ then $y>x-\varepsilon\geq a$ and $y<x+\varepsilon\leq b,$ so $I_\varepsilon(x)\subseteq(a,b).$ The unbounded intervals $(a,+\infty)$ and $(-\infty,b)$ are open, with $\varepsilon=x-a$ and $\varepsilon=b-x$ respectively. The empty set is open because it contains no point to be tested, and $\mathbb{R}$ is open because it contains every neighborhood. The closed interval $[a,b]$ is not open, since for every $\varepsilon>0$ the point $a-\varepsilon/2$ lies in $I_\varepsilon(a)$ and outside $[a,b],$ so $a$ fails to be an interior point.

Two operations preserve openness. An arbitrary union of open sets is open, and an intersection of finitely many open sets is open.

Let $\{A_i\}_{i\in I}$ be open sets and let $x$ belong to their union. Then $x\in A_{i_0}$ for some index $i_0,$ and since $A_{i_0}$ is open there is an $\varepsilon>0$ with $I_\varepsilon(x)\subseteq A_{i_0},$ hence $I_\varepsilon(x)$ is contained in the union. For finitely many open sets $A_1,\dots,A_n$ and a point $x$ in their intersection, for each $j$ there is a radius $\varepsilon_j>0$ such that $I_{\varepsilon_j}(x)\subseteq A_j.$ The number $\varepsilon=\min\{\varepsilon_1,\dots,\varepsilon_n\}$ is positive because it is the smallest of finitely many positive numbers. Since $I_\varepsilon(x)\subseteq A_j$ for every $j,$ the neighborhood lies in the intersection.

Finiteness is necessary for intersections. The intersection of all the neighborhoods $(-1/n,1/n)$ with $n\in\mathbb{N}$ is a single point:

$$
\bigcap_{n=1}^{\infty}\left(-\frac{1}{n},\frac{1}{n}\right)=\{0\}
$$

A real number $x$ with $x\neq0$ satisfies $|x|>1/n$ for $n$ large, by the [Archimedean property](../real-numbers/), so it lies outside one of the sets. The singleton $\{0\}$ is not open, because every neighborhood of $0$ contains points other than $0.$ For an infinite family the minimum used in the previous argument becomes an infimum, and an infimum of positive numbers can be zero.

> The two stability properties, together with the openness of $\emptyset$ and $\mathbb{R},$ are taken as axioms in general topology. A topology on a set $X$ is a family of subsets of $X,$ called open sets, that contains $\emptyset$ and $X$ and is stable under arbitrary unions and finite intersections. The open subsets of $\mathbb{R}$ form the standard topology, or Euclidean topology, of the real line.

Every non-empty open subset $A$ of $\mathbb{R}$ is the union of a countable family of pairwise disjoint open intervals. For $x\in A$ the union of all open intervals that contain $x$ and are contained in $A$ is an open interval, and two intervals obtained in this way are either equal or disjoint. Each of them contains a [rational number](../rational-numbers/) by density, and disjoint intervals contain distinct rational numbers, so the family is countable.

## Accumulation points and isolated points

A point $x\in\mathbb{R}$ is an accumulation point of $E\subseteq\mathbb{R}$ when $I_\varepsilon^*(x)\cap E\neq\emptyset$ for every $\varepsilon>0.$ Equivalently, every neighborhood of $x$ contains at least one point of $E$ different from $x.$ The set of accumulation points of $E$ is the derived set $E'.$

The definition compares $x$ with the points of $E$ near it and does not require $x\in E.$ Thus, an accumulation point of $E$ need not belong to $E,$ and a point of $E$ need not be an accumulation point. A point $x\in E$ that is not an accumulation point of $E$ is an isolated point of $E,$ and it has a neighborhood meeting $E$ only at $x.$ Every point of $E$ is therefore either isolated or an accumulation point of $E.$

Every neighborhood of an accumulation point contains infinitely many points of $E.$ Suppose that a neighborhood $I_\varepsilon(x)$ contained only the points $y_1,\dots,y_n$ of $E$ distinct from $x.$ This list is not empty, because $x\in E',$ and the number $\delta=\min\{|y_1-x|,\dots,|y_n-x|\}$ is positive, since none of the $y_j$ equals $x.$ Every point of $E$ lying in $I_\delta(x)$ and differing from $x$ would be one of the $y_j,$ which is impossible because $|y_j-x|\geq\delta.$ So $I_\delta(x)$ contains no point of $E$ other than possibly $x,$ contradicting $x\in E'.$

Accumulation points have a characterization through [sequences](../sequences/). A point $x$ belongs to $E'$ if and only if some sequence $(x_n)$ of points of $E,$ all different from $x,$ converges to $x.$ If $x\in E',$ choose for each $n\in\mathbb{N}$ a point $x_n\in I_{1/n}(x)\cap E$ with $x_n\neq x.$ Then $|x_n-x|<1/n,$ so $x_n\to x.$ Conversely, such a sequence has a term different from $x$ in every neighborhood of $x.$

The definition of [limit](../limits/) uses this notion. Writing $\lim_{x\to x_0}f(x)=\ell$ requires $x_0$ to be an accumulation point of the domain of $f,$ so that the values of $f$ can be examined at points arbitrarily close to $x_0.$ The point $x_0$ may be missing from the domain, which is why the definition excludes it from the comparison.

+ For $E=(0,1]$ one has $E'=[0,1],$ and $E$ has no isolated point.
+ For $E=\{1/n \mid n\in\mathbb{N}\}$ every point is isolated, and $E'=\{0\},$ so the only accumulation point of $E$ is not an element of $E.$
+ For $E=\mathbb{Q}$ one has $E'=\mathbb{R}$ because the rational numbers are dense.
+ Finite sets and $\mathbb{Z}$ have no accumulation points, and all their points are isolated.

A subset of $\mathbb{R}$ without accumulation points must be finite or unbounded. Every bounded infinite subset of $\mathbb{R}$ has at least one accumulation point. This is the set-theoretic form of the [Bolzano-Weierstrass theorem](../convergent-and-divergent-sequences/) and is a consequence of the [completeness](../real-numbers/) of the real numbers. The statement fails in $\mathbb{Q},$ where the set of the decimal truncations of $\sqrt{2}$ is bounded and infinite and has no accumulation point in $\mathbb{Q}.$

## Closed sets

A set $F\subseteq\mathbb{R}$ is closed when its complement $\mathbb{R}\setminus F$ is open. Equivalently, $F$ is closed if and only if each of its accumulation points belongs to it, that is, when $F'\subseteq F.$

Let $F$ be closed and let $x\in F'.$ If $x$ did not belong to $F,$ it would belong to the open set $\mathbb{R}\setminus F,$ so one of its neighborhoods would be contained in $\mathbb{R}\setminus F$ and would contain no point of $F,$ which contradicts $x\in F'.$ Conversely, assume $F'\subseteq F$ and take $x\in\mathbb{R}\setminus F.$ From $x\notin F'$ it follows that some neighborhood $I_\varepsilon(x)$ contains no point of $F$ other than $x,$ and $x\notin F,$ so $I_\varepsilon(x)\subseteq\mathbb{R}\setminus F.$ The complement of $F$ is open and $F$ is closed.

A sequential criterion follows from the characterization of accumulation points. A set $F$ is closed if and only if the limit of every [convergent sequence](../convergent-and-divergent-sequences/) of points of $F$ belongs to $F.$ If $F$ is closed and $x_n\to x$ with $x_n\in F,$ either $x=x_n$ for some index, and then $x\in F,$ or $x_n\neq x$ for infinitely many indices, and then $x\in F'\subseteq F.$

+ The interval $[a,b]$ is closed, since its complement $(-\infty,a)\cup(b,+\infty)$ is a union of two open sets.
+ Finite sets and $\mathbb{Z}$ have no accumulation points, so they are closed.
+ The set $\{1/n \mid n\in\mathbb{N}\}$ is not closed, because $0$ is an accumulation point that does not belong to it. The set $\{0\}\cup\{1/n \mid n\in\mathbb{N}\}$ is closed.
+ The interval $[0,1)$ is neither open nor closed, since $0$ is not an interior point and $1$ is an accumulation point outside the set.
+ The sets $\emptyset$ and $\mathbb{R}$ are both open and closed, and they are the only subsets of $\mathbb{R}$ with this property. This is equivalent to the [connectedness](../intervals/) of the real line.

By the [De Morgan laws](../sets/), an arbitrary intersection of closed sets is closed, and a union of finitely many closed sets is closed. Finiteness is required for unions. The sets $[1/n,1]$ are closed for every $n\in\mathbb{N},$ but their union over all $n$ is $(0,1],$ which is not closed.

## Closure, interior and boundary

The interior of $E$ was defined pointwise. It is the union of all open sets contained in $E,$ hence it is the largest open subset of $E.$ The closure of $E,$ written $\overline{E},$ is the intersection of all closed sets containing $E.$ An intersection of closed sets is closed, so $\overline{E}$ is the smallest closed set containing $E.$

The closure of $E$ consists of the points of $E$ and its accumulation points:

$$
\overline{E}=E\cup E'
$$

Equivalently, a point belongs to the closure of $E$ when each of its neighborhoods meets $E$:

$$
x\in\overline{E}\iff I_\varepsilon(x)\cap E\neq\emptyset \quad \text{for every }\varepsilon>0
$$

If $x\in E,$ the intersection contains $x.$ If $x\notin E$ and every neighborhood of $x$ meets $E,$ each intersection contains a point of $E$ different from $x,$ so $x\in E'.$ The converse follows from the definition of an accumulation point.

The set $E\cup E'$ contains $E$ and is closed. To see this, let $x$ be an accumulation point of $E\cup E'$ and let $\varepsilon>0.$ The neighborhood $I_\varepsilon(x)$ contains a point $y\neq x$ of $E\cup E'.$ If $y\in E,$ the neighborhood meets $E$ away from $x.$ If $y\in E',$ choose a neighborhood of $y$ contained in $I_\varepsilon(x)$ that avoids $x.$ This neighborhood contains a point of $E$ different from $y.$ In both cases $I_\varepsilon(x)$ meets $E$ at a point other than $x,$ so $x\in E'.$ Any closed set $F$ containing $E$ satisfies $E'\subseteq F'\subseteq F,$ hence $E\cup E'\subseteq F,$ and the smallest closed set containing $E$ is $E\cup E'.$ Thus, $E$ is closed if and only if $E=\overline{E},$ and $E$ is open if and only if $E=E^{\circ}.$ The boundary is the difference between the closure and the interior:

$$
\partial E=\overline{E}\setminus E^{\circ}
$$

A boundary point has every neighborhood meeting both $E$ and its complement. Therefore, the boundary is the intersection of the two closures:

$$
\partial E=\overline{E}\cap\overline{\mathbb{R}\setminus E}
$$

A set $A\subseteq\mathbb{R}$ is dense in $\mathbb{R}$ when $\overline{A}=\mathbb{R},$ or equivalently when every non-empty open set contains a point of $A.$ Both the [rational numbers](../rational-numbers/) and the [irrational numbers](../irrational-numbers/) are dense. Thus, for $E=\mathbb{Q}$ one has $\overline{E}=\mathbb{R},$ $E^{\circ}=\emptyset,$ and $\partial\mathbb{Q}=\mathbb{R}.$ Since $\mathbb{Q}$ is countable, the real line contains a countable dense subset, a property known as separability.

## Compactness

An open cover of a set $K\subseteq\mathbb{R}$ is a family $\{A_i\}_{i\in I}$ of open sets whose union contains $K.$ A subcover is a subfamily whose union contains $K,$ and it is finite when the subfamily has finitely many members. The set $K$ is compact when every open cover of $K$ has a finite subcover.

The definition concerns every open cover. A finite subcover for one cover does not prove compactness.

Finite sets are compact. Given an open cover, choose one member that contains each point of the finite set. The chosen members form a finite subcover. The interval $(0,1)$ is not compact. The intervals $A_n=(1/n,1)$ with $n\geq2$ are open and cover $(0,1),$ because every $x\in(0,1)$ satisfies $x>1/n$ for $n$ large. A finite subfamily has union $(1/N,1)$ for the largest index $N$ appearing in it, and this misses the points of $(0,1)$ below $1/N.$ The line is not compact because the cover $\{(-n,n)\}_{n\in\mathbb{N}}$ has no finite subcover.

Every compact subset of $\mathbb{R}$ is bounded and closed.

A compact set $K$ is [bounded](../supremum-and-infimum/). The intervals $(-n,n)$ with $n\in\mathbb{N}$ form an open cover of $K,$ and a finite subcover has union $(-N,N)$ for some $N,$ so $|x|<N$ for every $x\in K.$

A compact set $K$ is closed. Fix $y\notin K$ and consider the sets:

$$
A_n=\left(-\infty,y-\frac{1}{n}\right)\cup\left(y+\frac{1}{n},+\infty\right)
$$

Each $A_n$ is open because it is a union of two open intervals, and $A_n\subseteq A_{n+1}.$ Every $x\in K$ satisfies $|x-y|>0,$ hence $|x-y|>1/n$ for $n$ large, so the family $\{A_n\}_{n\in\mathbb{N}}$ covers $K.$ A finite subcover has union $A_N$ for the largest index $N$ it contains, and $K\subseteq A_N$ means $I_{1/N}(y)\cap K=\emptyset.$ The point $y$ is exterior to $K,$ so $\mathbb{R}\setminus K$ is open.

## The Heine-Borel theorem

A set $K\subseteq\mathbb{R}$ is compact if and only if it is closed and bounded.

One implication has been proved. For the converse, we first prove that every closed bounded interval is compact and then consider an arbitrary closed bounded set.

A closed interval $J_1=[a,b]$ is compact. Suppose that an open cover $\mathcal{O}$ of $J_1$ has no finite subcover, and split $J_1$ at its midpoint into two closed halves. If both halves had a finite subcover from $\mathcal{O},$ the union of the two finite subfamilies would cover $J_1,$ so at least one half has none. Call it $J_2$ and repeat the bisection. The result is a nested sequence of closed intervals:

$$
J_1\supseteq J_2\supseteq J_3\supseteq\cdots
$$

The interval $J_n$ has length $(b-a)/2^{n-1},$ and no $J_n$ has a finite subcover from $\mathcal{O}.$ By the [nested interval theorem](../real-numbers/), there is a point $c$ in every $J_n.$ Since $\mathcal{O}$ covers $J_1,$ some $A\in\mathcal{O}$ contains $c,$ and since $A$ is open there is an $\varepsilon>0$ with $I_\varepsilon(c)\subseteq A.$ Choose $n$ with $(b-a)/2^{n-1}<\varepsilon.$ Every point of $J_n$ is then at distance less than $\varepsilon$ from $c,$ because $c\in J_n,$ so:

$$
J_n\subseteq I_\varepsilon(c)\subseteq A
$$

The set $A$ is a finite subcover of $J_n.$ This contradicts the choice of $J_n,$ so $\mathcal{O}$ has a finite subcover of $[a,b].$

Now let $K$ be closed and bounded, and let $\mathcal{O}$ be an open cover of $K.$ Since $K$ is bounded, some interval $[a,b]$ contains it. The set $\mathbb{R}\setminus K$ is open because $K$ is closed. Therefore $\mathcal{O}\cup\{\mathbb{R}\setminus K\}$ is an open cover of $[a,b]$ and has a finite subcover by the previous step. If this finite subcover contains $\mathbb{R}\setminus K,$ remove it. The remaining members belong to $\mathcal{O}$ and cover $K,$ since no point of $K$ lies in $\mathbb{R}\setminus K.$ Therefore $K$ is compact.

> The theorem is a property of $\mathbb{R}$ and not a general fact about sets equipped with a distance. Take $X=(0,1)$ with the distance inherited from the line, and let $F=\{1/n \mid n\geq2\}.$ Inside $X$ the set $F$ is bounded and closed, since its only accumulation point in $\mathbb{R}$ is $0,$ which does not belong to $X.$ The interval of radius $1/(n+1)^2$ around $1/n$ meets $F$ only at $1/n,$ so these intervals form an open cover of $F$ in which no finite subfamily covers $F,$ and $F$ is not compact. The difference is that $\mathbb{R}$ is complete and $X$ is not.

## Compactness and sequences

A sequential condition is equivalent to compactness in $\mathbb{R}.$ A set $K\subseteq\mathbb{R}$ is compact if and only if every sequence of points of $K$ has a subsequence converging to a point of $K.$ This property is called sequential compactness.

Let $K$ be compact, hence closed and bounded, and let $(x_n)$ be a sequence in $K.$ The sequence is bounded, so it has a convergent subsequence by the [Bolzano-Weierstrass theorem](../convergent-and-divergent-sequences/), and its limit lies in $K$ because $K$ is closed. Conversely, suppose $K$ is not compact. If $K$ is unbounded, choose $x_n\in K$ with $|x_n|>n$ for every $n.$ No subsequence of $(x_n)$ is bounded, so none of them converges. If $K$ is not closed, take an accumulation point $x\in K'$ with $x\notin K$ and choose $x_n\in K$ with $|x_n-x|<1/n.$ Then $x_n\to x,$ every subsequence converges to $x$ as well, and the limit is outside $K.$

If a [continuous function](../continuous-functions/) has a compact domain, its image is compact. [Weierstrass' theorem](../weierstrass-theorem/) states that a continuous function on a closed bounded interval has a maximum and a minimum. A continuous function on a compact set is [uniformly continuous](../uniform-continuity/), whereas continuity alone does not imply uniform continuity on intervals such as $(0,1)$ and $[0,+\infty).$
