# Riemann Integrability Criteria

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/riemann-integrability-criteria/

## Introduction

The Riemann integral is built to measure the net area under a bounded [function](../functions/) on a [closed interval](../intervals/) by approximating it with rectangles. The subtle point is not computing the integral once it exists, but deciding when the [limiting](../limits) process is well-defined. This page collects the most useful criteria for Riemann integrability, in a form that is easy to apply when you meet a function that is not obviously [continuous](../continuous-functions/). 

> If you want the definition and basic properties of the definite integral first, see: [Definite Integrals](../definite-integrals/).

- - -
## Partitions, upper sums, lower sums

Let \\( f:[a,b]\to\mathbb{R} \\) be bounded. A partition \\( P \\) of \\( [a,b] \\) is a finite collection of points

\\[P=\{x_0,x_1,\dots,x_n\}\\]
\\[a=x_0<x_1<\cdots<x_n=b\\]

On each subinterval \\( [x_{i-1},x_i] \\) we record how high and how low the function can reach. Since \\( f \\) is bounded, both quantities are well defined:

\\[M_i=\sup_{x\in[x_{i-1},x_i]} f(x)\\]
\\[m_i=\inf_{x\in[x_{i-1},x_i]} f(x)\\]

+ \\( M_i \\) is the least upper bound of \\( f \\) on that subinterval (the smallest value that is still at least as large as every value \\( f \\) takes there). 
+ \\( m_i \\) is the greatest lower bound (the largest value that is still no greater than any value \\( f \\) takes there). 

![Img. 1](svg/riemann-integrability-criteria-1.svg)

The diagram above shows the lower sum: each rectangle is built using the infimum of \\( f \\) on its subinterval, so every rectangle fits entirely below the curve. No part of any rectangle sticks out above it. The diagram below shows the upper sum: here each rectangle uses the supremum, so the rectangles overshoot the curve and cover more area than is actually there. The true area under the curve lies somewhere between the two.

![Img. 2](svg/riemann-integrability-criteria-2.svg)

As the partition gets finer and the subintervals shrink, the rectangles in both sums become thinner and more numerous, and the two approximations are forced closer and closer together.

- - -

When \\( f \\) is continuous, these coincide with the actual maximum and minimum on the subinterval. For a general bounded function, sup and inf are used because a maximum or minimum may not be attained. Using \\( M_i \\) and \\( m_i \\), we define the Darboux upper and lower sums:

\\[U(f,P)=\sum_{i=1}^n M_i(x_i-x_{i-1})\\]
\\[L(f,P)=\sum_{i=1}^n m_i(x_i-x_{i-1})\\]

Two facts keep the whole construction coherent. First, making a partition finer, adding points to it, can only push upper sums down and lower sums up. Second, no matter which partition you choose, the lower sum never exceeds the upper sum:

\\[
L(f,P) \leq U(f,P)
\\]

Together, these mean that as partitions get finer, the upper and lower sums are squeezed toward each other. When they meet at a common limit, the function is integrable and that limit is the integral.

- - -
## The Darboux criterion

Before stating the criterion, it helps to fix two numbers that summarize all possible upper and lower sums at once. Define the upper and lower integrals as:

\\[U(f)=\inf_{P} U(f,P)\\]
\\[L(f)=\sup_{P} L(f,P)\\]

where the infimum and supremum range over all partitions \\( P \\) of \\( [a,b] \\). In plain terms: 

+ \\( U(f) \\) is the smallest value the upper sums can be pushed down to, by choosing finer and finer partitions. 
+ \\( L(f) \\) is the largest value the lower sums can be pushed up to. 

One can show that \\( L(f) \leq U(f) \\) always holds, regardless of the function.

- - -

A bounded function \\( f \\) is Riemann integrable on \\( [a,b] \\) if and only if these two numbers coincide:

\\[
U(f) = L(f)
\\]

In that case, their common value is the integral:

\\[
\int_a^b f(x)\\,dx = U(f) = L(f)
\\]

This is clean as a definition, but in practice it is hard to compute \\( U(f) \\) and \\( L(f) \\) directly. The following equivalent formulation is far more useful when you actually want to prove integrability: a bounded function \\( f \\) is Riemann integrable on \\( [a,b] \\) if and only if for every \\( \varepsilon > 0 \\) there exists a partition \\( P \\) such that

\\[
U(f,P) - L(f,P) < \varepsilon
\\]

![Img. 3](svg/riemann-integrability-criteria-3.svg)

The difference becomes clear looking at the two diagrams. With a coarse partition, each rectangle is wide enough to leave a noticeable gap between the upper and lower bounds. Narrowing the subintervals forces both sums to track the curve more closely, and the space between them shrinks accordingly.

![Img. 4](svg/riemann-integrability-criteria-4.svg)

In other words, you can always find a partition that forces the upper and lower sums as close together as you like. This is the criterion to reach for when you want to prove integrability by squeezing the two sums toward each other.

- - -

On each subinterval \\( [x_{i-1},x_i] \\), the difference \\( M_i - m_i \\) represents the range of values taken by \\( f \\) on that portion of the interval, that is, its oscillation over that segment. A straightforward computation then shows that:

\\[
U(f,P) - L(f,P) = \sum_{i=1}^n (M_i - m_i)(x_i - x_{i-1})
\\]

This is the central idea. A function is integrable if we can divide the interval into sufficiently small pieces so that the variation of the function on each piece contributes only a negligible error to the total sum. If, on the contrary, the function keeps oscillating in an uncontrollable way on every subinterval, no matter how fine the partition, then this condition cannot be met, and the function fails to be integrable in the Riemann sense.

> Once a function is known to be Riemann integrable, the [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/) provides the main tool for evaluating it.

- - -
## Common sufficient conditions

The Darboux criterion is the foundation, but in practice most functions you encounter fall into one of three categories that guarantee integrability without any direct computation of sums. A function \\( f \\) on \\( [a,b] \\) is Riemann integrable if it satisfies any one of the following conditions.

+ If \\( f \\) is [continuous](../continuous-functions/) on \\( [a,b] \\), integrability follows from uniform continuity: on a closed bounded interval, continuity forces the oscillation \\( M_i - m_i \\) to be uniformly small on every sufficiently short subinterval, which is exactly what the Darboux criterion requires.

+ If \\( f \\) is monotone on \\( [a,b] \\), the oscillation on each subinterval reduces to a difference of endpoint values. These differences telescope when summed across the partition, and the total \\( U(f,P) - L(f,P) \\) can be made small simply by taking the mesh fine enough.

+ If \\( f \\) is bounded and has only finitely many discontinuities, each can be enclosed in a subinterval of arbitrarily small length, while the function remains continuous and well-behaved everywhere else.

> These three conditions are independent: a function can be monotone without being continuous, and can have finitely many discontinuities without being monotone. What they share is that none of them allows discontinuities to accumulate densely, and that is the key.

- - -

## The discontinuity-set criterion

A bounded function \\( f:[a,b]\to\mathbb{R} \\) is Riemann integrable if and only if its set of discontinuities has Lebesgue measure zero. A set \\( D \subset [a,b] \\) has measure zero if for every \\( \varepsilon > 0 \\) you can cover \\( D \\) with a countable collection of intervals whose total length is less than \\( \varepsilon \\). The discontinuities can be hidden inside intervals that, taken together, occupy as little of the real line as you want. Two examples show what this means in practice.

> Lebesgue measure is the standard way of assigning length to subsets of the real line. For an interval \\( [c,d] \\) it equals \\( d - c \\). A set has measure zero if it can be covered by intervals of arbitrarily small total length — it occupies no space on the line in any meaningful sense. Finite and countable sets, such as the rationals, all have measure zero.

- - -

[Dirichlet's function](../dirichlet-function/) is defined as:

\\[
f(x) =
\begin{cases}
1 & x \in \mathbb{Q} \\\\[6pt]
0 & x \notin \mathbb{Q}
\end{cases}
\\]

It is [discontinuous](../discontinuities-of-real-functions/) at every point of \\( [a,b] \\), so its discontinuity set is the entire interval, which does not have measure zero. It is not Riemann integrable. Every subinterval contains both rationals and irrationals, so every \\( M_i = 1 \\) and every \\( m_i = 0 \\), which gives \\( U(f,P) - L(f,P) = b - a \\) for every partition \\( P \\), regardless of how fine it is.

- - -

Thomae's function is defined as

\\[
t(x) =
\begin{cases}
0 & x \notin \mathbb{Q} \\\\
\dfrac{1}{q} & x = \dfrac{p}{q} \text{ in lowest terms}
\end{cases}
\\]

It is discontinuous exactly at the rationals and continuous at every irrational. The rationals in \\( [a,b] \\) form a countable set, and every countable set has measure zero. So Thomae's function is Riemann integrable and its integral over any interval is zero, despite being discontinuous at infinitely many points.

- - -
## Recognising Riemann integrability

When you encounter a bounded function \\( f \\) on \\( [a,b] \\) and need to decide whether it is Riemann integrable, the following sequence of checks usually settles the question quickly.

+ If \\( f \\) is continuous on \\( [a,b] \\), then it is integrable.
+ If \\( f \\) is monotone on \\( [a,b] \\), then it is integrable.
+ If \\( f \\) has only finitely many discontinuities, then it is integrable.
+ If the discontinuities of \\( f \\) form a set of measure zero, then it is integrable.
+ If \\( f \\) is discontinuous on a set that cannot be made small, show that \\( U(f,P) - L(f,P) \\) stays bounded away from zero for every partition \\( P \\). Then \\( f \\) is not Riemann integrable.