---
title: Triangle Inequality
source: https://algebrica.org/complex-number-fundamental-inequalities/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - complex-modulus
  - complex-numbers
  - reverse-triangle-inequality
  - triangle-inequality
---
## Definition

The triangle inequality states that the modulus of the sum of two [complex numbers](../complex-numbers/) $z_1$ and $z_2$ is at most the sum of their moduli.

$$|z_1 + z_2| \leq |z_1| + |z_2| \tag{1}$$

To prove $(1),$ we use the identity $|z|^2 = z\overline{z}$ and the following property of the [conjugate of a sum](../complex-number-operations/).

$$\overline{z_1 + z_2} = \overline{z_1} + \overline{z_2} \tag{2}$$

We then expand $|z_1 + z_2|^2$ as follows.

$$
\begin{aligned}
|z_1 + z_2|^2 &= (z_1 + z_2)\overline{(z_1 + z_2)} \\[6pt]
              &= (z_1 + z_2)(\overline{z_1} + \overline{z_2}) \\[6pt]
              &= |z_1|^2 + z_1\overline{z_2} + \overline{z_1}z_2 + |z_2|^2
\end{aligned}
\tag{3}
$$

In the last equality of $(3),$ the terms $z_1\overline{z_2}$ and $\overline{z_1}z_2$ are complex conjugates. Their sum is therefore twice the real part of either term.

$$z_1\overline{z_2} + \overline{z_1}z_2 = 2\mathrm{Re}(z_1\overline{z_2}) \tag{4}$$

By $(4),$ to bound the cross terms it suffices to bound $\mathrm{Re}(z_1\overline{z_2}).$ For any complex number $w = a + bi,$ we have $\mathrm{Re}(w) \leq |w|,$ since $\mathrm{Re}(w) = a \leq |a|$ and $|a| = \sqrt{a^2} \leq \sqrt{a^2 + b^2} = |w|.$ Setting $w = z_1\overline{z_2}$ gives $\mathrm{Re}(z_1\overline{z_2}) \leq |z_1\overline{z_2}| = |z_1||z_2|,$ since the modulus is multiplicative and $|\overline{z_2}| = |z_2|.$ Applying this bound to the expansion of $|z_1 + z_2|^2$ in $(3)$ gives the following estimate.

$$
\begin{aligned}
|z_1 + z_2|^2 &= |z_1|^2 + 2\mathrm{Re}(z_1\overline{z_2}) + |z_2|^2 \\[6pt]
              &\leq |z_1|^2 + 2|z_1||z_2| + |z_2|^2 \\[6pt]
              &= (|z_1| + |z_2|)^2
\end{aligned}
\tag{5}
$$

Taking the [square root](../radicals/) of both sides of $(5)$ gives the following inequality.

$$|z_1 + z_2| = \sqrt{|z_1 + z_2|^2} \leq \sqrt{(|z_1| + |z_2|)^2} = |z_1| + |z_2|$$

This proves $(1).$

- - -

Equality in $(1)$ is equivalent to equality in $(5)$ because the square root is strictly increasing on the [nonnegative real numbers](../real-numbers/).

When the vectors $z_1$ and $z_2$ are not collinear, the segments joining them to the origin form [adjacent sides of a parallelogram](../vectors/). The sum vector $z_1 + z_2$ is the diagonal, and by $(1)$ its length is at most that of the path between the same vertices along two consecutive sides.

![IMG. 1](svg/triangle-inequality-1.svg)

Applying $(1)$ to $z_1$ and $-z_2$ and using $|-z_2| = |z_2|,$ we obtain an upper bound for the modulus of the difference.

$$|z_1 - z_2| \leq |z_1| + |z_2| \tag{6}$$

![IMG. 2](svg/triangle-inequality-2.svg)

The left-hand side is the length of the segment joining $z_1$ and $z_2.$ The right-hand side is the length of the path from $z_1$ to $z_2$ through the origin.

- - -

The triangle inequality can be generalized to finite sums of arbitrary length. More generally, the following inequality holds for every $n \geq 1$ and every choice of complex numbers $z_1, z_2, \ldots, z_n.$

$$\left|\sum_{k=1}^{n} z_k\right| \leq \sum_{k=1}^{n} |z_k| \tag{12}$$

The proof of $(12)$ proceeds by [induction](../principle-of-mathematical-induction/) on $n.$ When $n = 1,$ both sides equal $|z_1|.$ Now suppose $(12)$ holds for some integer $n \geq 1.$ For the step to $n + 1$ terms, we apply $(1)$ to the sum of the first $n$ terms and the final term to obtain the following estimate.

$$\left|\sum_{k=1}^{n+1} z_k\right| = \left|\sum_{k=1}^{n} z_k + z_{n+1}\right| \leq \left|\sum_{k=1}^{n} z_k\right| + |z_{n+1}| \tag{13}$$

The induction hypothesis gives the following bound for the first term on the right-hand side.

$$\left|\sum_{k=1}^{n+1} z_k\right| \leq \sum_{k=1}^{n} |z_k| + |z_{n+1}| = \sum_{k=1}^{n+1} |z_k| \tag{14}$$

Since the estimate also holds for $n + 1,$ this completes the induction and proves $(12).$

- - -

Equality holds in $(12)$ if and only if all nonzero summands lie on the same ray from the origin. If two nonzero summands $z_j$ and $z_k$ have different directions, $(1)$ gives the following strict inequality.

$$|z_j + z_k| < |z_j| + |z_k|$$

Grouping these two summands and applying $(12)$ to the resulting sum yields a strict inequality. Conversely, if all nonzero summands have the same direction, we can write $z_k = r_k e^{i\alpha}$ with $r_k = |z_k|$ and the same $\alpha$ for every index. Factoring out $e^{i\alpha},$ which has modulus $1,$ gives equality in $(12).$

Inequality $(12)$ is useful because it allows us to prove that every absolutely convergent series of complex terms converges. For example, define the [partial sum](../series/) $S_n$ as follows.

$$S_n = \sum_{k=1}^{n} z_k$$

By the [Cauchy criterion](../cauchy-convergence-criterion-series/), it suffices to show that $|S_n - S_m|$ becomes arbitrarily small for $n > m$ once $m$ is sufficiently large. Subtracting $S_m$ from $S_n$ cancels the first $m$ terms. Applying $(12)$ to the remaining terms gives the following estimate.

$$|S_n - S_m| = \left|\sum_{k=m+1}^{n} z_k\right| \leq \sum_{k=m+1}^{n} |z_k| \tag{15}$$

Let $T_n$ and $T_m$ be the partial sums of the series of moduli $\sum_{k=1}^{\infty} |z_k|.$

$$
\begin{align}
T_n &= \sum_{k=1}^{n} |z_k| \\[6pt]
T_m &= \sum_{k=1}^{m} |z_k|
\end{align}
$$

The right-hand side of $(15)$ is the following finite sum.

$$\sum_{k=m+1}^{n} |z_k| = T_n - T_m$$

By hypothesis, the series $\sum_{k=1}^{\infty} |z_k|$ converges, so $T_n - T_m$ tends to zero as $m \to \infty$ with $n > m.$ It follows from $(15)$ that $|S_n - S_m|$ also tends to zero, so by the Cauchy criterion the series $\sum_{k=1}^{\infty} z_k$ converges.


## Reverse triangle inequality

The reverse triangle inequality gives a lower bound on the distance between two complex numbers $z_1$ and $z_2$ in terms of their moduli alone.

$$\bigl||z_1| - |z_2|\bigr| \leq |z_1 - z_2| \tag{7}$$

To prove $(7),$ we write $z_1 = (z_1 - z_2) + z_2$ and apply $(1)$ to the two summands to obtain the following inequality.

$$|z_1| \leq |z_1 - z_2| + |z_2| \tag{8}$$

Subtracting $|z_2|$ from both sides of $(8)$ gives the first bound.

$$|z_1| - |z_2| \leq |z_1 - z_2| \tag{9}$$

Interchanging $z_1$ and $z_2$ in $(9)$ and using $|z_2 - z_1| = |z_1 - z_2|$ gives the second bound.

$$|z_2| - |z_1| \leq |z_1 - z_2| \tag{10}$$

Inequalities $(9)$ and $(10)$ show that both $|z_1| - |z_2|$ and $|z_2| - |z_1|$ are at most $|z_1 - z_2|.$ The same bound holds for their maximum, which is $\bigl||z_1| - |z_2|\bigr|.$ This proves $(7).$

- - -

To determine when equality holds in $(7),$ we compare the squares of its two sides, both of which are nonnegative. Replacing $z_2$ with $-z_2$ in the first line of $(5)$ and subtracting the square of the difference of the moduli gives the following identity.

$$|z_1 - z_2|^2 - (|z_1| - |z_2|)^2 = 2\bigl(|z_1||z_2| - \mathrm{Re}(z_1\overline{z_2})\bigr) \tag{11}$$

By $(11),$ the squares are equal if and only if $\mathrm{Re}(z_1\overline{z_2}) = |z_1\overline{z_2}|.$ This is the same condition for equality as in $(1).$ In the complex plane, this condition holds when at least one of the numbers is zero or when both lie on the same ray from the origin.

> It follows from $(7)$ that the modulus is [uniformly continuous](../uniform-continuity/) on $\mathbb{C}.$ Inequality $(7)$ states that the absolute change in modulus does not exceed the distance between the two points. In this sense, the modulus is Lipschitz with constant $1.$ To keep the change in modulus below a tolerance $\varepsilon > 0,$ it suffices to choose $\delta = \varepsilon.$ Indeed, for every pair $z_1, z_2 \in \mathbb{C}$ with $|z_1 - z_2| < \delta,$ we have $\bigl||z_1| - |z_2|\bigr| < \varepsilon.$ The same threshold $\delta$ applies to all points in the complex plane.
