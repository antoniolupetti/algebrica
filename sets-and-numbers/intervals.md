
# Intervals

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/intervals/

## Definition

An interval is a subset of the real line with the property that, whenever two points belong to it, every point lying between them also belongs to it. More precisely, a subset \\( I \subseteq \mathbb{R} \\) is an interval if and only if, for every pair of points \\( a, b \in I \\) with \\( a < b \\), the entire set \\( \{x \in \mathbb{R} : a \leq x \leq b\} \\) is contained in \\( I \\). This property, known as convexity on the [real line](../real-numbers/), distinguishes intervals from arbitrary subsets of \\( \mathbb{R} \\) such as finite sets or unions of disconnected pieces.

Intervals are among the most fundamental objects in mathematical analysis. They appear as [domains of functions](../determining-the-domain-of-a-function/), as regions of integration](../definite-integrals/), as sets on which [continuity](../continuous-functions/) and [differentiability](../derivatives/) are studied and as the building blocks for describing more complex subsets of the real line.

Intervals are classified according to whether their endpoints are included or excluded, and  according to whether they are bounded or extend indefinitely in one or both directions.

- - -
## Bounded intervals

A bounded interval is one that is contained within a finite portion of the real line, that is, one for which there exist real numbers \\( a \\) and \\( b \\) with \\( a \leq b \\) such that the interval is a subset of \\( [a, b] \\). The open interval with endpoints \\( a \\) and \\( b \\) is the set of all real numbers strictly between \\( a \\) and \\( b \\), excluding both endpoints. It is defined as follows:
\\[
(a, b) = \{x \in \mathbb{R} : a < x < b\}
\\]

[field_math]
|     | \\[ a\\] | \\[ b\\] |     |
|:----|----------|----------|-----|
|     | sign+l-in-o-h     | sign+r-in-o-h     |     |
[/field_math]

The closed interval with endpoints \\( a \\) and \\( b \\) is the set of all real numbers between \\( a \\) and \\( b \\), including both endpoints. It is defined as follows:
\\[
[a, b] = \{x \in \mathbb{R} : a \leq x \leq b\}
\\]

[field_math]
|     | \\[ a\\] | \\[ b\\] |     |
|:----|----------|----------|-----|
|     | sign+l-in-c-h    | sign+r-in-c-h     |     |
[/field_math]

The two half-open intervals with endpoints \\( a \\) and \\( b \\) include one endpoint and 
exclude the other. They are defined as follows:
\\[
[a, b) = \{x \in \mathbb{R} : a \leq x < b\}
\\]

[field_math]
|     | \\[ a\\] | \\[ b\\] |     |
|:----|----------|----------|-----|
|     | sign+l-in-c-h    | sign+r-in-o-h     |     |
[/field_math]

\\[
(a, b] = \{x \in \mathbb{R} : a < x \leq b\}
\\]

[field_math]
|     | \\[ a\\] | \\[ b\\] |     |
|:----|----------|----------|-----|
|     | sign+l-in-o-h    | sign+r-in-c-h     |     |
[/field_math]

A degenerate interval is the special case \\( [a, a] = \\{a\\} \\), which contains exactly one point. It satisfies the definition of an interval vacuously, since there are no two distinct points between which additional points could be required.

- - -
## Unbounded intervals

An unbounded interval extends indefinitely in at least one direction. Since infinity is not 
a real number, the symbols \\( +\infty \\) and \\( -\infty \\) are used purely as notational 
conventions to indicate that the interval has no finite bound in the corresponding direction. 
Consequently, the endpoints \\( +\infty \\) and \\( -\infty \\) are always excluded, and 
the corresponding bracket is always a parenthesis. The four unbounded intervals are defined as follows.
\\[
[a, +\infty) = \{x \in \mathbb{R} : x \geq a\}
\\]

[field_math]
|     | \\[ a\\] |     |
|:----|----------|-----|
|     | sign+l-c-h    |     |
[/field_math]

\\[
(a, +\infty) = \{x \in \mathbb{R} : x > a\}
\\]

[field_math]
|     | \\[ a\\] |     |
|:----|----------|-----|
|     | sign+l-o-h    |     |
[/field_math]

\\[
(-\infty, b] = \{x \in \mathbb{R} : x \leq b\}
\\]

[field_math]
|     | \\[ b\\] |     |
|:----|----------|-----|
|     | sign+r-c-h    |     |
[/field_math]

\\[
(-\infty, b) = \{x \in \mathbb{R} : x < b\}
\\]

[field_math]
|     | \\[ b\\] |     |
|:----|----------|-----|
|     | sign+r-o-h    |     |
[/field_math]

Finally, the entire real line is itself an interval, denoted \\( (-\infty, +\infty) = \mathbb{R} \\), which contains every real number and has no restriction of any kind.

- - -
## Operations on intervals

Given two intervals, one may form new sets by combining them through the standard 
set-theoretic operations of intersection and union. The intersection \\( I \cap J \\) is the set of all points belonging to both intervals simultaneously. The intersection of two intervals is always an interval, possibly empty or degenerate. Consider for example \\( I = (1, 5) \\) and \\( J = (3, 7) \\). The values belonging to both are precisely those in \\( (3, 5) \\).

[field_math]
|     | \\[ 1\\] | \\[ 3\\] | \\[ 5\\] | \\[ 7\\] |     |
|:----|----------|----------|----------|----------|-----|
|     | sign+l-in-o |   | sign+r-in-o |  |     |
|     |  | sign+l-in-o |  | sign+r-in-o |     |
|     |  | sign+l-in-o-h | sign+r-in-o-h |  |     |
[/field_math]

The third row shows the intersection \\( (3, 5) \\), which is the portion shared by both 
intervals.

- - -

The union \\( I \cup J \\) is the set of all points belonging to at least one of the two 
intervals. Unlike intersection, the union of two intervals is not always an interval: it is 
an interval if and only if the two intervals overlap or share an endpoint. Consider the same 
example, \\( I = (1, 5) \\) and \\( J = (3, 7) \\). Since the two intervals overlap, their 
union is the interval \\( (1, 7) \\).

[field_math]
|     | \\[ 1\\] | \\[ 3\\] | \\[ 5\\] | \\[ 7\\] |     |
|:----|----------|----------|----------|----------|-----|
|     | sign+l-in-o |  | sign+r-in-o |  |     |
|     |  | sign+l-in-o |  | sign+r-in-o |     |
|     | sign+l-in-o-h | sign+s-h |  | sign+r-in-o-h |     |
[/field_math]

The third row shows the union \\( (1, 7) \\). By contrast, the union \\( (1, 3) \cup (5, 7) \\) 
is not an interval, because the points between \\( 3 \\) and \\( 5 \\) belong to neither set.
- - -
## Intervals and neighborhoods

A concept closely related to intervals and central to mathematical analysis is that of a 
neighborhood of a point. Given a point \\( x_0 \in \mathbb{R} \\) and a real number 
\\( \varepsilon > 0 \\), the open interval:

\\[
(x_0 - \varepsilon,\\, x_0 + \varepsilon)
\\]

is called the \\( \varepsilon \\)-neighborhood of \\( x_0 \\), or simply a neighborhood of 
\\( x_0 \\). It consists of all points whose distance from \\( x_0 \\) is strictly less than 
\\( \varepsilon \\), that is, all \\( x \\) satisfying \\( |x-x_0| < \varepsilon \\), 
where \\( |\cdot| \\) denotes the [absolute value](../absolute-value/).

[field_math]
|     | \\[ x_0 - \varepsilon\\] | \\[ x_0\\] | \\[ x_0 + \varepsilon\\] |     |
|:----|--------------------------|------------|--------------------------|-----|
|     | sign+l-in-o-h | sign+s-h | sign+r-in-o-h |     |
[/field_math]

Neighborhoods provide the language in which the definitions of [limit](../limits/), continuity, and differentiability are naturally expressed. A function \\( f \\) is continuous at \\( x_0 \\) if for every neighborhood of \\( f(x_0) \\) there exists a neighborhood of \\( x_0 \\) whose image under \\( f \\) is contained in the former. This formulation is equivalent to the classical \\( \varepsilon \\)-\\( \delta \\) definition and makes the role of intervals explicit.

A point \\( x_0 \\) is said to be interior to a set \\( S \subseteq \mathbb{R} \\) if some neighborhood of \\( x_0 \\) is entirely contained in \\( S \\). Every point of an open interval is interior to it, which is one reason open intervals play a privileged role in analysis. By contrast, the endpoints of a closed interval are not interior points: every 
neighborhood of an endpoint contains points outside the interval.

- - -
## Length of an interval

The length of a bounded interval with endpoints \\( a \\) and \\( b \\) is defined as \\( b - a \\), regardless of whether the endpoints are included or excluded. That is, the four intervals \\( (a, b) \\), \\( [a, b) \\), \\( (a, b] \\), and \\( [a, b] \\) all have the same length, given by the following expression.

\\[
\ell(I) = b-a
\\]

This reflects the fact that a single point has no extent: adding or removing a finite number of points from an interval does not alter its length. A degenerate interval \\( [a, a] \\) has length \\( \ell([a,a]) = 0 \\), consistently with this observation. Unbounded intervals have infinite length, in the sense that for every \\( M > 0 \\) there exist points in the 
interval whose distance exceeds \\( M \\), so no finite value can be assigned as their length.

This notion of length is the starting point for the theory of measure on the real [line](../lines/), which assigns a generalized notion of size to arbitrary subsets of \\( \mathbb{R} \\). The measure of an interval \\( [a, b] \\) coincides with its length \\( b - a \\), and the extension of this assignment to more complex sets, through the notion of outer measure and measurability, forms the foundation of the [Lebesgue integral](../riemann-integrability-criteria/).

- - -
## Characterization of intervals

A subset of the real line is said to be connected if it cannot be written as the union of 
two disjoint non-empty open sets. The following theorem provides a complete characterization 
of intervals in terms of this property. A subset \\( S \subseteq \mathbb{R} \\) is an interval if and only if it is connected.

This result makes precise the intuitive idea that an interval is a portion of the real line 
with no gaps. The condition of connectedness rules out sets such as \\( (1, 2) \cup (3, 4) \\), 
which fail to be intervals precisely because they can be separated into two disjoint open pieces.

[field_math]
|     | \\[ 1\\] | \\[ 2\\] | \\[ 3\\] | \\[ 4\\] |     |
|:----|----------|----------|----------|----------|-----|
|     | sign+l-in-o-h | sign+r-in-o-h |  |  |     |
|     |  |  | sign+l-in-o-h | sign+r-in-o-h |     |
[/field_math]

> The two intervals occupy separate, non-overlapping portions of the real line and cannot be joined into a single connected piece, which confirms that their union is not an interval.