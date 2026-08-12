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
+ Periodicity: the set of nonzero [periods](../functions/) is $\mathbb{Q} \setminus \{0\},$ and no fundamental period exists.

If $r \in \mathbb{Q},$ then $x + r$ is rational exactly when $x$ is, and $D(x + r) = D(x).$ Conversely, suppose that $D(x + r) = D(x)$ for every $x \in \mathbb{R}.$ Setting $x = 0$ gives $D(r) = D(0) = 1,$ so $r \in \mathbb{Q}.$ The positive rational periods have no least element, so $D$ has no fundamental period.

$\mathbb{Q}$ and $\mathbb{R} \setminus \mathbb{Q}$ are [dense](../topology-of-the-real-line/) in the [real line](../real-numbers/). Fix $x_0 \in \mathbb{R}$ and take $\varepsilon = 1/2.$ If $x_0$ is rational, every $\delta$-neighborhood of $x_0$ contains an irrational number $x$ satisfying $0 < |x - x_0| < \delta.$ The function values satisfy:

$$|D(x) - D(x_0)| = 1 > \varepsilon$$

If $x_0$ is irrational, the argument uses a rational number $x$ in the $\delta$-neighborhood. Thus the $\varepsilon$-$\delta$ condition for [continuity](../continuous-functions/) fails at every $x_0,$ and $D$ is discontinuous everywhere.

- - -

The function $D$ is an iterated pointwise limit of continuous functions:

$$D(x) = \lim_{k \to \infty} \lim_{j \to \infty} \cos^{2j}(k!\pi x)$$

If $x = p/q$ is rational, with $p \in \mathbb{Z}$ and $q \in \mathbb{N}_{>0},$ then the [factorial](../factorial/) $k!$ is divisible by $q$ for every $k \geq q.$ For these values of $k,$ the number $k!x$ is an integer, $\cos(k!\pi x) = \pm 1,$ and the inner limit is $1.$ If $x$ is irrational, then $|\cos(k!\pi x)| < 1$ for every [positive integer](../natural-numbers/) $k,$ and the inner limit is $0.$ The outer limit agrees with $D(x).$

For fixed $k,$ denote the inner limit by $g_k.$ Each $g_k$ is of Baire class one because it is a [pointwise limit](../sequence-of-functions/) of continuous functions. The identity $D = \lim_{k \to \infty} g_k$ shows that $D$ is of Baire class at most two. A function of Baire class one is continuous on a dense set, whereas $D$ is discontinuous everywhere. This excludes class one, so the Baire class of $D$ is two.

Differentiability at a point implies continuity at that point. Because $D$ is discontinuous everywhere, it is nowhere [differentiable](../derivatives/).

## Riemann and Lebesgue integrability

Let $[a, b]$ be a [compact interval](../intervals/) with $a < b.$ Every subinterval of a partition $P$ contains rational and irrational points. The [supremum](../supremum-and-infimum/) of $D$ on that subinterval is $1,$ and the infimum is $0.$ For each partition, the [upper and lower Darboux sums](../definite-integrals/) are given by:

$$
\begin{align}
U(D, P) &= b - a \\[6pt]
L(D, P) &= 0
\end{align}
$$

For $a < b,$ these sums are unequal, which violates the [Darboux criterion](../riemann-integrability-criteria/). The function $D$ is not Riemann integrable on any non-degenerate compact interval.

- - -

The [countable](../cardinality-and-countable-sets/) set $\mathbb{Q}$ is Borel and has [Lebesgue measure zero](../riemann-integrability-criteria/). Its indicator function $D$ is measurable and equals zero almost everywhere. For every Lebesgue-measurable set $E \subseteq \mathbb{R},$ the integral of $D$ over $E$ is equal to:

$$\int_E D(x) \ d\lambda = \lambda(E \cap \mathbb{Q}) = 0$$

In particular, taking $E = \mathbb{R}$ shows that $D$ is Lebesgue integrable on $\mathbb{R},$ with integral zero.
