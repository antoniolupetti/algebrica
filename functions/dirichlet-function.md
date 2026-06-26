---
title: Dirichlet Function
source: https://algebrica.org/dirichlet-function/
license: CC BY-NC 4.0
tags:
  - differentiability
  - discontinuity
  - lebesgue-integration
  - riemann-integrability
  - thomae-function
---
## Definition

The Dirichlet function is defined on $\mathbb{R}$ by the following rule:

$$
D(x) =
\begin{cases}
1 & \text{if } x \in \mathbb{Q} \\[6pt]
0 & \text{if } x \in \mathbb{R} \setminus \mathbb{Q}
\end{cases}
$$

At first glance this appears to be an almost trivial definition, a simple distinction between [rationals](../rational-numbers/) and [irrationals](../irrational-numbers/). The function is [even](../even-and-odd-functions/), and every nonzero rational is a period of $D,$ since $x + r$ is rational exactly when $x$ is, so $D$ is periodic without a fundamental period. Yet this simplicity conceals an extremely irregular analytic behaviour, which has made this function a standard reference object in [integration](../definite-integrals/) theory and real analysis.

- - -

A notable property of $D$ is its [discontinuity](../discontinuities-of-real-functions/) at every point of $\mathbb{R}.$ This result follows from the mutual density of $\mathbb{Q}$ and $\mathbb{R} \setminus \mathbb{Q}$ in the [real line](../real-numbers/).

For any fixed point $x_0 \in \mathbb{R}$ and any $\varepsilon > 0,$ the [interval](../intervals/) $(x_0 - \varepsilon, x_0 + \varepsilon)$ contains both rational and irrational numbers. Therefore, there is no neighborhood of $x_0$ on which $D$ is constant, and any [sequence](../convergent-and-divergent-sequences/) converging to $x_0$ can be constructed so that the values of $D$ alternate indefinitely between $0$ and $1.$ As a result, the following [limit](../limits/):

$$\lim_{x \to x_0} D(x)$$

does not exist for any $x_0,$ establishing discontinuity at every point. Since a function that is discontinuous everywhere cannot be [Riemann integrable](../riemann-integrability-criteria/) on any non-degenerate interval, this can be confirmed by noting that the upper and lower Darboux sums remain fixed at $1$ and $0,$ respectively, for every partition of the interval.

> Darboux sums are sums obtained by multiplying the maximum or minimum value of a function on each subinterval of a partition by the width of that subinterval. These sums are used to approximate the integral from above and below.

Dirichlet's original construction expresses $D$ as a double limit of continuous functions:

$$D(x) = \lim_{k \to \infty} \lim_{j \to \infty} \cos^{2j}(k!\pi x)$$

For a rational $x,$ once $k$ is large enough the number $k!x$ is an integer, so $\cos(k!\pi x) = \pm 1$ and the inner limit equals $1.$ For an irrational $x,$ the number $k!x$ is never an integer, hence $|\cos(k!\pi x)| < 1$ and the inner limit equals $0.$ This places $D$ in Baire class two. It cannot belong to class one, because a Baire-one function is continuous on a dense set of points, while $D$ is continuous nowhere.

## Non-integrability in the Riemann sense

Consider an interval $[a, b]$ with $a < b$ and any partition $\mathcal{P}$ such that:

$$\mathcal{P} = \{\ a = x_0 < x_1 < \cdots < x_n = b \ \}$$

On each subinterval $[x_{i-1}, x_i],$ the [supremum](../supremum-and-infimum/) of $D$ is $1$ due to the density of the rationals, while the infimum is $0$ due to the density of the irrationals. Therefore:

$$U(D, \mathcal{P}) = \sum_{i=1}^{n} 1 \cdot (x_i - x_{i-1}) = b - a$$

$$L(D, \mathcal{P}) = \sum_{i=1}^{n} 0 \cdot (x_i - x_{i-1}) = 0$$

Because $U(D, \mathcal{P}) - L(D, \mathcal{P}) = b - a > 0$ for every partition $\mathcal{P},$ the Riemann criterion is not satisfied. Consequently, the function is not integrable in the classical sense on any non-trivial interval.

- - -

Lebesgue's integration theory introduces a significant shift in perspective. The set $\mathbb{Q}$ is countable and therefore has Lebesgue measure zero: $\lambda(\mathbb{Q}) = 0.$ It follows that $D(x) = 0$ almost everywhere with respect to the Lebesgue measure, and since a function that equals zero almost everywhere has integral zero, one obtains

$$\int_{a}^{b} D(x) \ d\lambda = 0$$

for every interval $[a, b].$ This is one of the more immediate illustrations of the greater reach of Lebesgue's theory relative to Riemann's, since by construction it assigns no weight to sets of measure zero, even when those sets are dense in the real line.

## Differentiability

The question of whether $D$ possesses a [derivative](../derivatives/) at any point has a definitive answer, $D$ is nowhere differentiable. The derivative of $D$ at a point $x_0$ is defined as the limit:

$$D'(x_0) = \lim_{h \to 0} \frac{D(x_0 + h) - D(x_0)}{h}$$

provided this limit exists. Since differentiability implies [continuity](../continuous-functions/) and $D$ is discontinuous at every point of $\mathbb{R},$ it follows immediately that $D$ cannot be differentiable anywhere.

This conclusion can also be seen directly through [difference quotients](../difference-quotient/). Fix any $x_0$ and consider two sequences $(r_n)$ and $(s_n)$ converging to $x_0,$ with $r_n \in \mathbb{Q}$ and $s_n \in \mathbb{R} \setminus \mathbb{Q}$ for all $n.$ If $x_0 \in \mathbb{Q},$ then:

$$\frac{D(r_n) - D(x_0)}{r_n - x_0} = \frac{1 - 1}{r_n - x_0} = 0$$

$$\frac{D(s_n) - D(x_0)}{s_n - x_0} = \frac{0 - 1}{s_n - x_0} = \frac{-1}{s_n - x_0}$$

The second expression is unbounded as $s_n \to x_0.$ If instead $x_0 \in \mathbb{R} \setminus \mathbb{Q},$ then:

$$\frac{D(r_n) - D(x_0)}{r_n - x_0} = \frac{1 - 0}{r_n - x_0} = \frac{1}{r_n - x_0}$$

$$\frac{D(s_n) - D(x_0)}{s_n - x_0} = \frac{0 - 0}{s_n - x_0} = 0$$

It is now the first expression that grows without bound as $r_n \to x_0.$ In either case, the difference quotient admits no finite limit, confirming that $D'(x_0)$ does not exist.

## The Thomae function

A function closely related to the Dirichlet function, known as the Thomae function or the popcorn function, is defined as follows:

$$
T(x) =
\begin{cases}
\dfrac{1}{q} & \text{if } x = \dfrac{p}{q} \\[6pt]
0 & \text{if } x \in \mathbb{R} \setminus \mathbb{Q}
\end{cases}
$$

We have $p \in \mathbb{Z},$ $q \in \mathbb{N}_{>0},$ and $\gcd(|p|, q) = 1,$ that is, the fraction $p/q$ is in lowest terms.

In contrast to the Dirichlet function, the Thomae function is continuous at every irrational point and discontinuous at every rational point. This behaviour exemplifies the boundary case allowed by the Lebesgue criterion for Riemann integrability, where a Riemann-integrable function may be discontinuous on a set of measure zero, and the rationals, though dense, constitute precisely such a set.

Consequently, the Thomae function is Riemann integrable, with integral equal to zero on every interval, and is a well-behaved counterpart to the Dirichlet function.
