---
title: Dirichlet Function
source: https://algebrica.org/dirichlet-function/
license: CC BY-NC 4.0
tags:
  - differentiability
  - discontinuity
  - lebesgue-integration
  - riemann-integrability
---
## Definition

The Dirichlet function $D : \mathbb{R} \to \{0, 1\}$ is the indicator function $\mathbf{1}_{\mathbb{Q}}$ of the [rational numbers](../rational-numbers/). It assigns the value $1$ to rational numbers and $0$ to [irrational numbers](../irrational-numbers/):

$$
D(x) = \mathbf{1}_{\mathbb{Q}}(x) =
\begin{cases}
1 & \text{if } x \in \mathbb{Q} \\[6pt]
0 & \text{if } x \in \mathbb{R} \setminus \mathbb{Q}
\end{cases}
$$

## Properties

+ [Domain](../determining-the-domain-of-a-function/): $\mathbb{R}$
+ Range: $\{0, 1\}$
+ Boundedness: $0 \leq D(x) \leq 1$ for every $x \in \mathbb{R}$
+ Parity: [even](../even-and-odd-functions/), with $D(-x) = D(x)$
+ Periodicity: the set of nonzero periods is $\mathbb{Q} \setminus \{0\},$ and no fundamental period exists.

If $r \in \mathbb{Q},$ then $x + r$ is rational exactly when $x$ is, and $D(x + r) = D(x).$ Conversely, suppose that $D(x + r) = D(x)$ for every $x \in \mathbb{R}.$ Setting $x = 0$ gives $D(r) = D(0) = 1,$ hence $r \in \mathbb{Q}.$ Thus the nonzero periods are the nonzero rational numbers. Since the positive rationals have no least element, $D$ has no fundamental period.

$\mathbb{Q}$ and $\mathbb{R} \setminus \mathbb{Q}$ are dense in the [real line](../real-numbers/). Fix $x_0 \in \mathbb{R}$ and take $\varepsilon = 1/2.$ If $x_0$ is rational, every $\delta$-neighborhood of $x_0$ contains an irrational number $x$ satisfying $0 < |x - x_0| < \delta.$ The function values satisfy:

$$|D(x) - D(x_0)| = 1 > \varepsilon$$

If $x_0$ is irrational, the argument uses a rational number $x$ in the $\delta$-neighborhood. Thus the $\varepsilon$-$\delta$ condition for [continuity](../continuous-functions/) fails at every $x_0,$ and $D$ is nowhere continuous.

- - -

For each positive integer $k,$ define the function $g_k$ by:

$$g_k(x) := \lim_{j \to \infty} \cos^{2j}(k!\pi x)$$

Each $g_k$ is of Baire class one because it is a pointwise limit of continuous functions. If $x = p/q$ is rational, with $p \in \mathbb{Z}$ and $q \in \mathbb{N}_{>0},$ then $k!x$ is an integer for every $k \geq q,$ and $g_k(x) = 1.$ If $x$ is irrational, then $|\cos(k!\pi x)| < 1$ for every $k,$ and $g_k(x) = 0.$ The two cases give the identity:

$$D(x) = \lim_{k \to \infty} g_k(x)$$

Since $D$ is a pointwise limit of functions of Baire class one, it is of Baire class at most two. If it were of class one, it would be continuous on a dense set, but $D$ is nowhere continuous. Hence its Baire class is two.

Differentiability at a point implies continuity at that point. Since $D$ is nowhere continuous, it is nowhere [differentiable](../derivatives/).

## Riemann and Lebesgue integrability

Let $[a, b]$ be a compact interval with $a < b.$ Every subinterval of a partition $\mathcal{P}$ contains rational and irrational points, so the [supremum](../supremum-and-infimum/) of $D$ on that subinterval is $1$ and the infimum is $0.$ For every partition, the upper and lower Darboux sums are:

$$
\begin{align}
U(D, \mathcal{P}) &= b - a \\[6pt]
L(D, \mathcal{P}) &= 0
\end{align}
$$

Since $a < b,$ these sums are unequal. The [Darboux criterion](../riemann-integrability-criteria/) fails, so $D$ is not Riemann integrable on any non-degenerate compact interval.

- - -

The set $\mathbb{Q}$ is countable, hence Borel, and has Lebesgue measure zero. Its indicator function $D$ is measurable and equals zero almost everywhere. For every Lebesgue-measurable set $E \subseteq \mathbb{R},$ the integral of $D$ over $E$ is:

$$\int_E D(x) \ d\lambda = \lambda(E \cap \mathbb{Q}) = 0$$

Taking $E = \mathbb{R}$ shows that $D$ is Lebesgue integrable on $\mathbb{R},$ with integral zero.
