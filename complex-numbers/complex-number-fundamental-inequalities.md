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
## Fundamental inequalities

As we saw in the introduction, the set of [complex numbers](../complex-numbers/) $\mathbb{C}$ is a [field](../fields/) that admits no total order compatible with its arithmetic operations. An expression of the following form requires choosing an order on the complex numbers.

$$z_1 < z_2 \tag{1}$$

However, the modulus $|z|$ makes a quantitative treatment possible by assigning each complex number a nonnegative real value that can be used to compare magnitudes, estimate distances, and bound [sums and products](../complex-number-operations/). Recall that the modulus of a complex number $z = a + bi$ is defined by the following formula and gives the length of the [vector](../vectors/) from the origin to the point $(a,b).$

$$|z| = \sqrt{a^2 + b^2} \tag{2}$$

Several inequalities allow us to make these comparisons and are also used in the study of complex [sequences](../sequences/) and [series](../series/). We begin with inequalities for the real and imaginary parts. Given a complex number in algebraic form $z = a + bi,$ we set $a = \mathrm{Re}(z)$ and $b = \mathrm{Im}(z).$ It follows from $(2)$ that the [absolute value](../absolute-value/) of each component is at most the modulus of $z.$

$$
\begin{align}
|\mathrm{Re}(z)| &\leq |z| \tag{3} \\[6pt]
|\mathrm{Im}(z)| &\leq |z| \tag{4}
\end{align}
$$

To prove $(3),$ it suffices to observe that $a^2 \leq a^2 + b^2.$ Since the [square root](../radicals/) is increasing on the nonnegative real numbers, we obtain the following bound.

$$|a| \leq \sqrt{a^2 + b^2} = |z|$$

Inequality $(4)$ likewise follows from $b^2 \leq a^2 + b^2.$ Equality holds in $(3)$ if and only if $b = 0,$ and in $(4)$ if and only if $a = 0.$ The sum of the absolute values of the components, in turn, gives the following upper bound on the modulus.

$$|z| \leq |\mathrm{Re}(z)| + |\mathrm{Im}(z)| \tag{5}$$

To prove $(5),$ we expand the square of the sum as follows.

$$(|a| + |b|)^2 = a^2 + b^2 + 2|a||b|$$

Since the term $2|a||b|$ is nonnegative, we have the following inequality.

$$a^2 + b^2 \leq (|a| + |b|)^2 \tag{6}$$

Taking square roots in $(6)$ gives $(5).$ Equality holds if and only if $|a||b| = 0,$ that is, if at least one of the two components is zero. Two other useful inequalities are the triangle inequality and the Cauchy-Schwarz inequality, which are shown below and discussed in their respective entries.

[class="table-1 -right"]

| $$\lvert z_1 + z_2\rvert \leq \lvert z_1\rvert + \lvert z_2\rvert$$                                                                                             | [Explore](../triangle-inequality/)       |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| $$\left\lvert\sum_{k=1}^{n} a_k\overline{b_k}\right\rvert^2 \leq \left(\sum_{k=1}^{n} \lvert a_k\rvert^2\right)\left(\sum_{k=1}^{n} \lvert b_k\rvert^2\right)$$ | [Explore](../cauchy-schwarz-inequality/) |

[/class]