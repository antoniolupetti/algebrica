---
title: Fundamental Inequalities for Complex Numbers
source: https://algebrica.org/complex-number-fundamental-inequalities/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - cauchy-schwarz-inequality
  - complex-modulus
  - complex-numbers
  - reverse-triangle-inequality
  - triangle-inequality
---
## Introduction

A defining feature of the [field](../fields/) $\mathbb{C}$ is the absence of a total order compatible with its arithmetic operations. As established in the discussion of [complex numbers](../complex-numbers-introduction/), no relation $\leq$ can be defined on $\mathbb{C}$ so that it behaves consistently with [addition and multiplication](../complex-number-operations/). Statements such as $z_1 < z_2$ are therefore meaningless for arbitrary complex numbers, and the comparison techniques available in $\mathbb{R}$ do not transfer to the complex setting.

What survives, and what makes a quantitative theory possible, is the [modulus](../complex-numbers-introduction/) $|z|$. It assigns to every complex number a non-negative real value, and through it one can compare sizes, estimate distances, and bound sums and products. The inequalities collected here form the basic toolkit for these comparisons. They appear repeatedly in the analysis of complex sequences, in the convergence of series of complex terms, and in the geometric description of regions of the plane defined by analytic conditions.

> The presentation that follows proceeds from the simplest estimates, those concerning the real and imaginary components, towards the triangle inequality and its consequences, and concludes with the Cauchy-Schwarz inequality, which provides a unifying perspective on the others.

## Inequalities involving real and imaginary parts

Let $z = a + bi$ be a [complex number](../complex-numbers-introduction/), with $a = \mathrm{Re}(z)$ and $b = \mathrm{Im}(z)$. The modulus is defined by $|z| = \sqrt{a^2 + b^2}$, and from this definition follow three elementary inequalities that compare the modulus with the [absolute values](../absolute-value/) of the components.

The first asserts that the absolute value of either part cannot exceed the modulus:

$$|\mathrm{Re}(z)| \leq |z|, \qquad |\mathrm{Im}(z)| \leq |z|$$

The proof is immediate. Since $a^2 \leq a^2 + b^2$, taking square roots yields $|a| \leq \sqrt{a^2 + b^2} = |z|$, and the corresponding argument applies to $b$. Equality for the real part holds precisely when $b = 0$, that is, when $z$ is real. Analogously, equality for the imaginary part holds exactly when $a = 0$, so when $z$ is purely imaginary.

Geometrically, this is the statement that the projection of a [vector](../vectors/) onto either coordinate axis cannot be longer than the vector itself. The projections become equal to the original length only in the degenerate case where the vector is already aligned with the axis.

- - -

The second inequality reverses the comparison and provides an upper bound for the modulus in terms of its components:

$$|z| \leq |\mathrm{Re}(z)| + |\mathrm{Im}(z)|$$

This bound follows from the algebraic identity $(|a| + |b|)^2 = a^2 + 2|a||b| + b^2$, in which the cross term is non-negative. Hence one has $a^2 + b^2 \leq (|a| + |b|)^2$, and taking square roots gives the assertion. Equality occurs when $|a||b| = 0$, so when at least one of the components vanishes.

These three inequalities allow one to convert bounds on $|z|$ into bounds on the components, and conversely.

## Triangle inequality

The most important inequality in the arithmetic of complex numbers is the triangle inequality, which asserts that the modulus of a sum is bounded by the sum of the moduli. For any $z_1, z_2 \in \mathbb{C}$ the following relation holds.

$$|z_1 + z_2| \leq |z_1| + |z_2|$$

The proof relies on the identity $|z|^2 = z\overline{z}$, established in the discussion of [operations with complex numbers](../complex-number-operations/), which converts modulus computations into algebraic manipulations of [conjugates](../complex-numbers-introduction/). Expanding the square of the modulus of the sum gives the following.

$$
\begin{align}
|z_1 + z_2|^2 &= (z_1 + z_2)\overline{(z_1 + z_2)} \\[6pt]
              &= (z_1 + z_2)(\overline{z_1} + \overline{z_2}) \\[6pt]
              &= |z_1|^2 + z_1 \overline{z_2} + \overline{z_1} z_2 + |z_2|^2
\end{align}
$$

The two middle terms are complex conjugates of one another, so their sum is a real number equal to twice the real part of either:

$$z_1 \overline{z_2} + \overline{z_1} z_2 = 2\mathrm{Re}(z_1 \overline{z_2})$$

By the inequality on real parts established in the previous section, one has $\mathrm{Re}(z_1 \overline{z_2}) \leq |z_1 \overline{z_2}| = |z_1||z_2|$. Substituting this bound yields the following estimate.

$$|z_1 + z_2|^2 \leq |z_1|^2 + 2|z_1||z_2| + |z_2|^2 = (|z_1| + |z_2|)^2$$

Taking square roots, both sides being non-negative, completes the argument.

- - -

Equality in the triangle inequality holds precisely when $\mathrm{Re}(z_1 \overline{z_2}) = |z_1 \overline{z_2}|$, which occurs if and only if $z_1 \overline{z_2}$ is a non-negative real number. Geometrically, this condition means that $z_1$ and $z_2$ lie on the same ray from the origin, or that one of the two vanishes. In all other configurations the inequality is strict.

The geometric content is transparent. Interpreting $z_1$ and $z_2$ as [vectors](../vectors/) in the plane, the sum $z_1 + z_2$ is the diagonal of the parallelogram whose sides are the two vectors. The diagonal cannot exceed the sum of the lengths of the sides, and the two coincide only when the parallelogram degenerates into a segment, that is, when the vectors are parallel and point in the same direction.

- - -

A useful corollary applies to differences. Replacing $z_2$ with $-z_2$, and noting that $|-z_2| = |z_2|$, one obtains the following.

$$|z_1 - z_2| \leq |z_1| + |z_2|$$

This estimate has a direct interpretation as a bound on the distance between two points of the complex plane: the distance from $z_1$ to $z_2$ cannot exceed the sum of the distances of the two points from the origin.

## Reverse triangle inequality

The triangle inequality has a companion result, often called the reverse triangle inequality, which provides a lower bound for the modulus of a difference. For any $z_1, z_2 \in \mathbb{C}$ one has the following.

$$\bigl||z_1| - |z_2|\bigr| \leq |z_1 - z_2|$$

The derivation rests on a simple rewriting. Starting from the identity $z_1 = (z_1 - z_2) + z_2$ and applying the triangle inequality to the right-hand side, one obtains:

$$|z_1| \leq |z_1 - z_2| + |z_2|$$

Rearranging gives $|z_1| - |z_2| \leq |z_1 - z_2|$. Exchanging the roles of $z_1$ and $z_2$, and using $|z_2 - z_1| = |z_1 - z_2|$, produces the symmetric estimate $|z_2| - |z_1| \leq |z_1 - z_2|$. Combining the two inequalities yields the desired bound on the absolute value of the difference of the moduli.

Equality holds, as in the direct triangle inequality, when $z_1$ and $z_2$ lie on the same ray from the origin.

- - -

The reverse triangle inequality has an important analytic consequence. Viewed as a map $|\cdot| : \mathbb{C} \to \mathbb{R}$, the modulus is a Lipschitz function with constant $1$. The inequality says exactly that the change in modulus is no larger than the distance between the two points. As a consequence, the modulus is uniformly continuous on $\mathbb{C}$, a property routinely invoked in the analysis of sequences, series, and limits of complex-valued expressions.

> Lipschitz continuity with constant $1$ is a strong form of uniform continuity. It guarantees that arbitrarily small variations of $z$ produce variations of $|z|$ that are no larger in magnitude than the variation of $z$ itself.

## Generalized triangle inequality

The triangle inequality extends to finite sums of arbitrary length. For any $n \geq 1$ and any complex numbers $z_1, z_2, \ldots, z_n$, one has the following.

$$\left|\sum_{k=1}^{n} z_k\right| \leq \sum_{k=1}^{n} |z_k|$$

The proof proceeds by [induction](../principle-of-mathematical-induction/) on $n$. The case $n = 1$ is trivial, since both sides reduce to $|z_1|$, and the case $n = 2$ is precisely the original triangle inequality. Suppose the bound holds for some $n \geq 2$. Writing the sum of $n + 1$ terms as the sum of two complex numbers, one consisting of the first $n$ summands and one consisting of the last, the triangle inequality gives:

$$\left|\sum_{k=1}^{n+1} z_k\right| = \left|\sum_{k=1}^{n} z_k + z_{n+1}\right| \leq \left|\sum_{k=1}^{n} z_k\right| + |z_{n+1}|$$

Applying the inductive hypothesis to the first term on the right yields:

$$\left|\sum_{k=1}^{n+1} z_k\right| \leq \sum_{k=1}^{n} |z_k| + |z_{n+1}| = \sum_{k=1}^{n+1} |z_k|$$

The estimate therefore holds at step $n + 1$, which completes the induction.

- - -

Equality requires more attention than in the two-term case. It holds if and only if all the non-zero summands lie on a single ray from the origin, that is, there exists a fixed unit vector $e^{i\alpha}$ and non-negative real numbers $r_1, r_2, \ldots, r_n$ such that $z_k = r_k e^{i\alpha}$ for every $k$. The exponential factor $e^{i\alpha}$ is the unit complex number associated with the common direction, as discussed in the entry on [Euler's formula](../eulers-formula/). Under this condition the sum is itself a non-negative multiple of $e^{i\alpha}$, and its modulus equals the sum of the individual moduli.

The generalized triangle inequality is the foundation on which the theory of [series](../geometric-series/) of complex terms is built. The notion of absolute convergence, in particular, depends on this estimate, since it allows one to control the modulus of partial sums by partial sums of moduli, which are real and non-negative.

## Cauchy-Schwarz inequality

The Cauchy-Schwarz inequality is a quantitative refinement that relates sums of products of complex numbers to sums of their squared moduli. In its finite form, for any complex numbers $a_1, \ldots, a_n$ and $b_1, \ldots, b_n$ one has the following.

$$\left|\sum_{k=1}^{n} a_k \overline{b_k}\right|^2 \leq \left(\sum_{k=1}^{n} |a_k|^2\right) \left(\sum_{k=1}^{n} |b_k|^2\right)$$

A standard derivation considers, for an arbitrary complex parameter $t$, the non-negative quantity:

$$P(t) = \sum_{k=1}^{n} |a_k - t b_k|^2$$

Setting $\sigma = \sum_{k=1}^{n} a_k \overline{b_k}$ and expanding the squared moduli gives the following.

$$
\begin{align}
P(t) &= \sum_{k=1}^{n} (a_k - t b_k)\bigl(\overline{a_k} - \overline{t}\,\overline{b_k}\bigr) \\[6pt]
     &= \sum_{k=1}^{n} |a_k|^2 - t\overline{\sigma} - \overline{t}\sigma + |t|^2 \sum_{k=1}^{n} |b_k|^2
\end{align}
$$

If $\sum_{k=1}^{n} |b_k|^2 = 0$, then every $b_k$ vanishes and the inequality holds trivially. In all other cases the choice $t = \sigma / \sum_{k=1}^{n} |b_k|^2$ minimises $P(t)$, and substituting this value yields the following estimate.

$$0 \leq P(t) = \sum_{k=1}^{n} |a_k|^2 - \frac{|\sigma|^2}{\sum_{k=1}^{n} |b_k|^2}$$

Rearranging the last inequality produces the bound:

$$|\sigma|^2 \leq \left(\sum_{k=1}^{n} |a_k|^2\right) \left(\sum_{k=1}^{n} |b_k|^2\right)$$

which is exactly the Cauchy-Schwarz inequality.

Equality holds when $P(t) = 0$ for some value of $t$, which means that $a_k = t b_k$ for every index $k$. In other words, equality occurs precisely when the tuples $(a_1, \ldots, a_n)$ and $(b_1, \ldots, b_n)$ are proportional in $\mathbb{C}^n$.

> The role of Cauchy-Schwarz extends well beyond the present setting. In the theory of inner product spaces, of which $\mathbb{C}^n$ is the prototypical finite-dimensional example, the inequality becomes the foundational estimate from which the geometric notion of angle, the parallelogram identity, and the entire structure of orthogonality follow.

## Examples and applications

A first illustration concerns the use of the elementary component inequalities. Suppose $z = a + bi$ satisfies $|z| \leq 5$. The estimate $|a| \leq |z|$ gives $-5 \leq a \leq 5$, and the corresponding bound for $b$ shows that the point $z$ is contained in the square of side $10$ centred at the origin. Conversely, if $|a| \leq 3$ and $|b| \leq 4$, the inequality $|z| \leq |a| + |b|$ gives the loose bound $|z| \leq 7$. The sharper estimate $|z| \leq \sqrt{9 + 16} = 5$ requires the full [Pythagorean computation](../pythagorean-theorem/) but produces a tighter result.

- - -

A second application concerns the localisation of roots of [polynomials](../polynomials/). Consider a monic polynomial of degree $n$:

$$p(z) = z^n + a_{n-1} z^{n-1} + \cdots + a_1 z + a_0$$

Suppose $z_0 \in \mathbb{C}$ is a [root](../roots-of-a-polynomial/) of $p$, so that $z_0^n = -a_{n-1} z_0^{n-1} - \cdots - a_0$. Applying the generalized triangle inequality to the right-hand side yields the following bound.

$$|z_0|^n \leq \sum_{k=0}^{n-1} |a_k| \cdot |z_0|^k$$

Setting $M = \max_{0 \leq k \leq n-1} |a_k|$ and assuming $|z_0| > 1$, the right-hand side admits the upper bound $M \cdot \frac{|z_0|^n - 1}{|z_0| - 1} \leq M \cdot \frac{|z_0|^n}{|z_0| - 1}$, from which one derives the inequality $|z_0| - 1 \leq M$. Consequently every root of $p$ satisfies the following estimate.

$$|z_0| \leq 1 + M$$

This is a classical bound, due to Cauchy, asserting that all the complex roots of a monic polynomial lie in a closed disc whose radius is determined by the largest coefficient. The argument is short, but it combines the triangle inequality with the [geometric series](../geometric-series/) and illustrates how the basic estimates yield substantive structural information about polynomial equations.

- - -

A third application uses the Cauchy-Schwarz inequality directly. Given complex numbers $z_1, \ldots, z_n$, choosing $a_k = z_k$ and $b_k = 1$ in the inequality gives the following.

$$\left|\sum_{k=1}^{n} z_k\right|^2 \leq n \sum_{k=1}^{n} |z_k|^2$$

This estimate compares the squared modulus of a sum of $n$ terms with the sum of the squared moduli, weighted by the number of summands. Unlike the generalized triangle inequality, which involves the linear sum of moduli, the bound on the right depends on the quadratic average of the $|z_k|$, and grows only as $\sqrt{n}$ when the moduli remain uniformly bounded. This sharper behaviour is one of the reasons why Cauchy-Schwarz plays a central role in the analysis of orthogonal sums and in the convergence of Fourier expansions.
