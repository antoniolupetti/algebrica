---
title: Cauchy-Schwarz Inequality
source: https://algebrica.org/complex-number-fundamental-inequalities/
license: CC BY-NC 4.0
tags:
  - cauchy-schwarz-inequality
  - complex-modulus
  - complex-numbers
---
## Definition

Given two lists of [complex numbers](../complex-numbers/), $a_1, \ldots, a_n$ and $b_1, \ldots, b_n,$ the [Cauchy-Schwarz inequality](../inner-product-spaces/) bounds the modulus of the sum of the products $a_k\overline{b_k}$ in terms of the moduli of those numbers. The formal statement is as follows.

$$\left|\sum_{k=1}^{n} a_k \overline{b_k}\right|^2 \leq \left(\sum_{k=1}^{n} |a_k|^2\right) \left(\sum_{k=1}^{n} |b_k|^2\right) \tag{1}$$

To prove $(1),$ we define the sum $P(t)$ for each $t \in \mathbb{C}$ as follows.

$$P(t) = \sum_{k=1}^{n} |a_k - t b_k|^2 \tag{2}$$

Let $\sigma$ denote the sum on the left-hand side of $(1).$

$$\sigma = \sum_{k=1}^{n} a_k \overline{b_k} \tag{3}$$

With the notation in $(3),$ the left-hand side of $(1)$ is $|\sigma|^2.$ We expand the sum in $(2)$ by applying the [identity](../complex-number-operations/) $|z|^2 = z\overline{z}$ with $z = a_k - tb_k.$

$$
\begin{aligned}
P(t) &= \sum_{k=1}^{n} |a_k - tb_k|^2 \\[6pt]
     &= \sum_{k=1}^{n} (a_k - tb_k)\bigl(\overline{a_k} - \overline{t}\overline{b_k}\bigr) \\[6pt]
     &= \sum_{k=1}^{n} \bigl(|a_k|^2 - tb_k\overline{a_k} - \overline{t}a_k\overline{b_k} + |t|^2|b_k|^2\bigr) \\[6pt]
     &= \sum_{k=1}^{n} |a_k|^2 - t\sum_{k=1}^{n} b_k\overline{a_k} - \overline{t}\sum_{k=1}^{n} a_k\overline{b_k} + |t|^2\sum_{k=1}^{n} |b_k|^2 \\[6pt]
     &= \sum_{k=1}^{n} |a_k|^2 - t\overline{\sigma} - \overline{t}\sigma + |t|^2 \sum_{k=1}^{n} |b_k|^2
\end{aligned}
\tag{4}
$$

If the sum $\sum_{k=1}^{n} |b_k|^2$ is zero, then every $b_k$ is zero and equality holds in $(1).$ Indeed, both sides are zero in this case, as shown below.

$$\left|\sum_{k=1}^{n} a_k\overline{b_k}\right|^2 = 0 = \left(\sum_{k=1}^{n} |a_k|^2\right)\left(\sum_{k=1}^{n} |b_k|^2\right) \tag{5}$$

Now suppose that $\sum_{k=1}^{n} |b_k|^2 > 0$ and define $t_0$ as follows.

$$t_0 = \sigma / \sum_{k=1}^{n} |b_k|^2$$

Since $t_0\sum_{k=1}^{n} |b_k|^2 = \sigma,$ the last term in $(4)$ becomes $\overline{t_0}\sigma$ and cancels the preceding term. By the definition in $(2),$ $P(t_0)$ is nonnegative, so we obtain the following relation.

$$0 \leq P(t_0) = \sum_{k=1}^{n} |a_k|^2 - t_0\overline{\sigma} = \sum_{k=1}^{n} |a_k|^2 - \frac{|\sigma|^2}{\sum_{k=1}^{n} |b_k|^2} \tag{6}$$

From $(6)$ we obtain the following bound.

$$\frac{|\sigma|^2}{\sum_{k=1}^{n} |b_k|^2} \leq \sum_{k=1}^{n} |a_k|^2 \tag{7}$$

Since $\sum_{k=1}^{n} |b_k|^2$ is positive, multiplying both sides of $(7)$ by this sum preserves the [direction of the inequality](../inequalities/) and gives the following bound.

$$|\sigma|^2 \leq \left(\sum_{k=1}^{n} |a_k|^2\right) \left(\sum_{k=1}^{n} |b_k|^2\right) \tag{8}$$

Substituting the expression for $\sigma$ from $(3)$ into $(8)$ gives $(1).$ From $(5)$ we know that equality holds if every $b_k$ is zero. If at least one $b_k$ is nonzero, then $(6)$ shows that equality holds in $(8)$ precisely when $P(t_0) = 0.$ By $(2),$ this sum can be zero only if all its terms are zero, that is, if $a_k = t_0b_k$ for every $k.$

Conversely, if the second tuple is nonzero and $a_k = cb_k$ for every $k,$ then $(3)$ gives $\sigma = c\sum_{k=1}^{n} |b_k|^2.$ It follows that $t_0 = c$ and $P(t_0) = 0.$

This proves $(1)$ and establishes that equality holds if and only if the tuples $(a_1, \ldots, a_n)$ and $(b_1, \ldots, b_n)$ are [linearly dependent](../vector-spaces/) in $\mathbb{C}^n.$

- - -

To see how to apply the inequality, we seek the maximum of $|z + (1+i)w|$ over pairs of complex numbers $(z,w)$ satisfying the following constraint.

$$|z|^2 + |w|^2 = 1 \tag{9}$$

To apply $(1),$ we take $(a_1,a_2) = (z,w)$ and $(b_1,b_2) = (1,1-i),$ so that the conjugate of $b_2$ is the coefficient of $w.$ In the product on the right-hand side of $(1),$ the first factor is $1$ by $(9),$ and the second is $1 + |1-i|^2 = 1 + 1^2 + (-1)^2 = 3.$

$$|z + (1+i)w|^2 \leq (|z|^2 + |w|^2)(1 + |1-i|^2) = 3$$

Both sides are nonnegative, so taking [square roots](../radicals/) gives the bound on the modulus.

$$|z + (1+i)w| \leq \sqrt{3}$$

Equality holds in $(1)$ if and only if the two tuples are linearly dependent. Here the second tuple is $(1,1-i)$ and is nonzero, so we choose $(z,w)$ to be a multiple of it. Since $1 + |1-i|^2 = 3,$ we divide both components of $(1,1-i)$ by $\sqrt{3}$ to satisfy the constraint in $(9).$

$$z = \frac{1}{\sqrt{3}}, \qquad w = \frac{1-i}{\sqrt{3}} \tag{10}$$

Substituting the values from $(10)$ gives $|z + (1+i)w| = |(1+2)/\sqrt{3}| = \sqrt{3}.$ Since the upper bound is attained, the maximum is $\sqrt{3}.$
