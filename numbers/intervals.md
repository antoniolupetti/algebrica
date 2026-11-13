---
title: Intervals
source: https://algebrica.org/intervals/
license: CC BY-NC 4.0
tags:
  - bounded-interval
  - closed-interval
  - connectedness
  - convexity
  - half-open-interval
  - interval
  - length
  - neighborhood
  - open-interval
  - real-line
  - unbounded-interval
---

## Definition

A subset $I \subseteq \mathbb{R}$ is an interval if and only if the following implication holds for every pair of real numbers $a,b$:

$$
\begin{align}
a,b \in I,\quad a \lt b &\implies \{x \in \mathbb{R} : a \leq x \leq b\} \subseteq I \tag{1}
\end{align}
$$

Equation $(1)$ states that if $a$ and $b$ belong to $I,$ then every point between $a$ and $b$ also belongs to $I.$ This property is called convexity. For example, the set $\{0,2\}$ is not an interval because it contains $0$ and $2$ but omits $1,$ which lies between them. An interval $I$ is bounded if there are real numbers $m \leq M$ such that every point of $I$ is at least $m$ and at most $M.$ Given two real numbers $a \lt b,$ we define the open interval with endpoints $a$ and $b$ as follows:

$$
\begin{align}
(a,b) &= \{x \in \mathbb{R} : a \lt x \lt b\} \tag{2}
\end{align}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-o | sign+r-in-o |     |
[/shortcode]

Given two real numbers $a \leq b,$ the following equality defines the closed interval with endpoints $a$ and $b$:

$$
\begin{align}
[a,b] &= \{x \in \mathbb{R} : a \leq x \leq b\} \tag{3}
\end{align}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-c | sign+r-in-c |     |
[/shortcode]

Given two real numbers $a \lt b,$ both half-open intervals with endpoints $a$ and $b$ contain every point strictly between $a$ and $b$ and exactly one endpoint. We define the first as follows:

$$
\begin{align}
[a,b) &= \{x \in \mathbb{R} : a \leq x \lt b\} \tag{4}
\end{align}
$$


[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-c | sign+r-in-o |     |
[/shortcode]

We define the second half-open interval as follows:

$$
\begin{align}
(a,b] &= \{x \in \mathbb{R} : a \lt x \leq b\} \tag{5}
\end{align}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-o | sign+r-in-c |     |
[/shortcode]

The degenerate interval $[a,a]=\{a\}$ consists of a single point and satisfies the definition of an interval because it contains no pair of distinct points that would require it to contain the points between them. We now turn to unbounded intervals, which extend indefinitely in at least one direction. The following equalities define these intervals:

$$
[a, +\infty) = \{x \in \mathbb{R} : x \geq a\} \tag{6}
$$

[shortcode="intervals"]
|     | $a$ |     |
|:----|-----|-----|
|     | sign+l-c |     |
[/shortcode]

$$
(a, +\infty) = \{x \in \mathbb{R} : x > a\} \tag{7}
$$

[shortcode="intervals"]
|     | $a$ |     |
|:----|-----|-----|
|     | sign+l-o |     |
[/shortcode]

$$
(-\infty, b] = \{x \in \mathbb{R} : x \leq b\} \tag{8}
$$

[shortcode="intervals"]
|     | $b$ |     |
|:----|-----|-----|
|     | sign+r-c |     |
[/shortcode]

$$
(-\infty, b) = \{x \in \mathbb{R} : x < b\} \tag{9}
$$

[shortcode="intervals"]
|     | $b$ |     |
|:----|-----|-----|
|     | sign+r-o |     |
[/shortcode]

The real line itself is also an interval, written $(-\infty,+\infty)=\mathbb{R},$ and contains every real number.

## Operations on intervals

We now define some operations on intervals, starting with the [intersection](../sets/) $I \cap J,$ the set of points that belong to both $I$ and $J.$ If two points belong to both intervals, then by $(1)$ every point between them belongs to both as well. The intersection therefore satisfies the same condition and is an interval that may be empty or degenerate. For example, a point in $(1,5)$ also belongs to $(3,7)$ if it is greater than $3,$ so we can write their intersection as follows:

$$
\begin{align}
(1,5) \cap (3,7) &= (3,5) \tag{10}
\end{align}
$$

[shortcode="intervals"]
|     | $1$ | $3$ | $5$ | $7$ |     |
|:----|-----|-----|-----|-----|-----|
|     | sign+l-in-o |             | sign+r-in-o |             |     |
|     |             | sign+l-in-o |             | sign+r-in-o |     |
|     |             | sign+l-in-o-h | sign+r-in-o-h |           |     |
[/shortcode]

The third row of the diagram shows the interval obtained in $(10).$

- - -

The union $I \cup J$ is the set of points that belong to at least one of the two intervals. Thus, the union of two nonempty intervals is an interval if they overlap or meet at an endpoint that belongs to at least one of them. In the previous example, the union is the interval $(1,7).$

[shortcode="intervals"]
|     | $1$ | $3$ | $5$ | $7$ |     |
|:----|-----|-----|-----|-----|-----|
|     | sign+l-in-o |             | sign+r-in-o |             |     |
|     |             | sign+l-in-o |             | sign+r-in-o |     |
|     | sign+l-in-o-h | sign+s-h |             | sign+r-in-o-h |     |
[/shortcode]

The third row shows the union $(1,7).$ The union $(1,3)\cup(5,7)$ fails to be an interval because the points between $3$ and $5$ belong to neither set.

## Neighborhoods

The definition of an interval gives us a way to define neighborhoods, in particular the $\varepsilon$-neighborhood of a point $x_0 \in \mathbb{R},$ which is the open interval centered at $x_0$ with radius $\varepsilon \gt 0.$ This neighborhood contains every point whose distance from $x_0$ is strictly less than $\varepsilon,$ where the distance from $x$ to $x_0$ is the [absolute value](../absolute-value/) of $x-x_0.$ We can write the neighborhood as follows:

$$
\begin{align}
(x_0 - \varepsilon, \ x_0 + \varepsilon) &= \{x \in \mathbb{R} : |x-x_0| \lt \varepsilon\} \tag{11}
\end{align}
$$

[shortcode="intervals"]
|     | $x_0 - \varepsilon$ | $x_0$ | $x_0 + \varepsilon$ |     |
|:----|---------------------|-------|---------------------|-----|
|     | sign+l-in-o-h | sign+s-h | sign+r-in-o-h |     |
[/shortcode]

Neighborhoods are useful in defining [limits](../limits/) and continuity. For example, a function $f\colon D\to\mathbb{R},$ with $D\subseteq\mathbb{R},$ is continuous at $x_0\in D$ if for every neighborhood radius $\varepsilon\gt 0$ there is a $\delta\gt 0$ such that the following implication holds for every $x\in D$:

$$
\begin{align}
|x-x_0| \lt \delta &\implies |f(x)-f(x_0)| \lt \varepsilon \tag{12}
\end{align}
$$

In $(12)$ we choose the radius $\delta$ so that the images of domain points near $x_0$ lie in the neighborhood of $f(x_0).$ To determine whether $x_0$ is an interior point of a set $S\subseteq\mathbb{R},$ we look for a radius $\varepsilon\gt 0$ for which every point in the neighborhood of $x_0$ in $(11)$ belongs to $S.$

Every point of $(a,b)$ is an interior point because we can choose a radius smaller than its distance to either endpoint. Every neighborhood of $a$ contains points less than $a,$ and every neighborhood of $b$ contains points greater than $b.$ Consequently, neither endpoint of $[a,b]$ is an interior point. The article on the [topology of the real line](../topology-of-the-real-line/) develops the relationship between neighborhoods, interior points, and open and closed sets.

## Length of an interval

The length of a nonempty bounded interval $I$ is the distance between its infimum $a$ and its supremum $b,$ which we can write as follows:

$$
\begin{align}
\ell(I) &= b-a \tag{13}
\end{align}
$$

Since $(13)$ depends only on the values of the endpoints, the intervals $(a,b),$ $[a,b),$ $(a,b]$ and $[a,b]$ all have the same length when $a\lt b.$ If the two endpoints coincide, $(13)$ gives $\ell([a,a])=0,$ the length of the degenerate interval introduced above. An unbounded interval has infinite length because for every $M\gt 0$ it contains two points more than $M$ apart and thus contains a closed interval of length greater than $M.$

Intervals of different lengths can have the same cardinality. Indeed, every interval containing at least two points has the same cardinality as $\mathbb{R},$ whether its length is finite or infinite. Lebesgue measure extends the length of intervals to a broader class of subsets of the real line and assigns to each nonempty bounded interval the length given by $(13).$ In general, every finite set has [measure zero](../riemann-integrability-criteria/), so adding or removing finitely many points leaves the measure unchanged even if the resulting set is no longer an interval (this measure is the basis for the Lebesgue integral).
