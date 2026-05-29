---
title: Absolute Value
source: https://algebrica.org/absolute-value/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - distance
  - even-function
  - inequalities
  - norm
  - real-line
  - reverse-triangle-inequality
  - sign-function
  - triangle-inequality
---

## Definition

The absolute value of a number represents its distance from zero on the number line, without considering its sign. It tells us how far a number is from zero, whether positive or negative, and is always non-negative. The absolute value is written using vertical bars, $|x|$, and is defined as follows:

$$
|x| =
\begin{cases}
+x & \text{if } x \geq 0 \\[6pt]
-x & \text{if } x < 0
\end{cases}
\quad
\forall \ x \in \mathbb{R}
$$

For example, $|5| = 5$ and $|-6| = -(-6) = 6$. The expression $f(x) := |x|$, with $x \in \mathbb{R}$, defines a function $f: \mathbb{R} \rightarrow \mathbb{R}$ whose image is $f(\mathbb{R}) = [0, +\infty)$.

- - -

The absolute value function assigns to each [real number](../real-numbers/) its distance from zero on the real line. Negative numbers are mapped to their positive counterparts, while positive numbers remain unchanged, since distance is always non-negative.

![IMG. 1](svg/real-numbers-1.svg)

More generally, the absolute value expression $|x - a|$ can be interpreted as the distance between the point $x$ and the point $a$ on the number line. We have:

$$
|x-a| = |a-x|
$$

For instance, the distance between $x = 3$ and $a = 7$ is $|3 - 7| = |-4| = 4$, which equals $|7 - 3| = |4| = 4$, confirming that distance is symmetric.

- - -

The absolute value of a number $|x|$ can also be represented using the sign function $\mathrm{sgn}(x)$, as:

$$
|x| = x \cdot \mathrm{sgn}(x)
$$

The [sign function](../sign-functions/) is defined as:

$$
\mathrm{sgn}(x) =
\begin{cases}
-1 & \text{if } x < 0 \\[6pt]
0 & \text{if } x = 0 \\[6pt]
1 & \text{if } x > 0
\end{cases}
$$

Multiplying $x$ by $\mathrm{sgn}(x)$ ensures that the result is always non-negative, as required by the definition of the absolute value. Specifically:

+ If $x > 0$, then $\mathrm{sgn}(x) = 1$ and $x \cdot \mathrm{sgn}(x) = x$.
+ If $x < 0$, then $\mathrm{sgn}(x) = -1$ and $x \cdot \mathrm{sgn}(x) = -x$.
+ If $x = 0$, then $\mathrm{sgn}(x) = 0$ and $x \cdot \mathrm{sgn}(x) = 0$.

## Properties

The absolute value of a number equals the absolute value of its opposite. This follows directly from the definition: whether one starts from a positive or a negative value, the distance from the origin is the same. For instance, $|3| = |-3| = 3$.

$$
|x| = |-x| \quad \forall \ x \in \mathbb{R}
$$

- - -

The absolute value of a product equals the product of the absolute values. The property extends naturally to any finite number of factors: $|x_1 \cdot x_2 \cdots x_n| = |x_1| \cdot |x_2| \cdots |x_n|$. As a special case, taking $x = y$ gives $|x^2| = |x|^2$, which is consistent with the fact that squares are always non-negative.

$$
|x \cdot y| = |x| \cdot |y| \quad \forall \ x, y \in \mathbb{R}
$$

- - -

Two real numbers have equal absolute values if and only if they are either equal or opposite. Geometrically, $|x| = |y|$ means that $x$ and $y$ lie at the same distance from the origin on the real line, which is precisely the case when $x = y$ or $x = -y$.

$$
|x| = |y| \iff x = \pm y \quad \forall \ x, y \in \mathbb{R}
$$

- - -

The comparison of absolute values is equivalent to the comparison of squares. This holds because both $|x|$ and $|y|$ are non-negative, and for non-negative numbers the squaring function is strictly increasing: $a \leq b \iff a^2 \leq b^2$ whenever $a, b \geq 0$. The equivalence $|x|^2 = x^2$ then completes the argument.

$$
|x| \leq |y| \iff x^2 \leq y^2 \quad \forall \ x, y \in \mathbb{R}
$$

- - -

The absolute value of a quotient equals the quotient of the absolute values, provided the denominator is non-zero. This is a direct consequence of the multiplicative property: writing $x/y = x \cdot y^{-1}$ and applying $|x \cdot y^{-1}| = |x| \cdot |y^{-1}| = |x|/|y|$.

$$
\left| \frac{x}{y} \right| = \frac{|x|}{|y|} \quad \forall \ x, y \in \mathbb{R},\ y \ne 0
$$

- - -

The principal square root of $x^2$ is the absolute value of $x$, not $x$ itself. Since the square root symbol denotes the non-negative root, one has $\sqrt{x^2} = x$ only when $x \geq 0$, and $\sqrt{x^2} = -x$ when $x < 0$. Writing $\sqrt{x^2} = x$ without qualification is a common error, valid solely for non-negative values.

$$
\sqrt{x^2} = |x| \quad \forall \ x \in \mathbb{R}
$$

> The properties listed here are the foundation for the study of equations and inequalities that involve the absolute value, and they connect directly to the geometric interpretation discussed in the next section.

## Triangle inequality

The triangle inequality is a fundamental property of the absolute value on the real line. For any numbers $a, b \in \mathbb{R}$, the following inequality holds:

$$
|a + b| \le |a| + |b|
$$

The inequality states that the distance of the sum $a + b$ from zero cannot exceed the sum of the individual distances of $a$ and $b$. Equality holds when both numbers have the same sign or when at least one of them is zero. When their signs differ and both are nonzero, partial cancellation occurs, resulting in a strict inequality.

- - -

To prove the inequality, we consider all possible sign configurations of $a$ and $b$:

$$
\begin{align}
(1)\quad & a \ge 0, \quad b \ge 0 \\[6pt]
(2)\quad & a \le 0, \quad b \le 0 \\[6pt]
(3)\quad & a \ge 0, \quad b \le 0 \\[6pt]
(4)\quad & a \le 0, \quad b \ge 0
\end{align}
$$

In case $(1)$, we have $a + b \geq 0$:

$$
|a + b| = a + b = |a| + |b|
$$

In case $(2)$, we have $a + b \leq 0$:

$$
|a + b| = -(a + b) = (-a) + (-b) = |a| + |b|
$$

In case $(3)$, since $a \ge 0$ and $b \le 0$, we have $|a| = a$ and $|b| = -b$, and therefore $|a| + |b| = a - b$. We must show that $|a + b| \le a - b$:

+ When $a + b \ge 0$, we have $|a + b| = a + b \le a - b$, since $b \le 0$.
+ When $a + b \le 0$, we obtain $|a + b| = -(a + b) = -a - b \le a - b$, which is equivalent to $-a \le a$, a condition that holds because $a \ge 0$.

In case $(4)$, where $a \le 0$ and $b \ge 0$, the argument is symmetric to case $(3)$ and leads to the same conclusion.

- - -

A consequence of the triangle inequality is the reverse triangle inequality. For any $a, b \in \mathbb{R}$:

$$
\bigl||a| - |b|\bigr| \le |a - b|
$$

The reverse triangle inequality says that the difference between the distances of $a$ and $b$ from zero cannot exceed the distance between $a$ and $b$ themselves. To see why, apply the triangle inequality to the identity $a = (a - b) + b$:

$$
|a| = |(a - b) + b| \le |a - b| + |b|
$$

This gives $|a| - |b| \le |a - b|$. By symmetry, swapping $a$ and $b$ yields $|b| - |a| \le |a - b|$. Since both $|a| - |b|$ and its negative are bounded by $|a - b|$, we conclude:

$$
\bigl||a| - |b|\bigr| \le |a - b|
$$

## The graph of $y = |x|$

The graph of the absolute value function $|x|$ is symmetric with respect to the $y$-axis. This symmetry implies that the function is even, meaning it satisfies the identity:

$$
|{-x}| = |x| \quad \text{for all } x \in \mathbb{R}
$$

![IMG. 1](svg/absolute-value-1.svg)
## Interpreting absolute value inequalities

An inequality that involves an absolute value expresses a condition about distance on the number line. The notation $|A|$ represents the distance of the quantity $A$ from zero, which is always non-negative. Consider first the inequality:

$$
|A| < k
$$

The inequality tells us that the distance between $A$ and zero is smaller than $k$. Geometrically, all numbers that satisfy this inequality are located within an open [interval](../intervals/) centred at the origin, extending $k$ units to the left and $k$ units to the right. Algebraically, this condition can be rewritten as:

$$
-k < A < k
$$

- - -

If instead the inequality is:

$$
|A| > k
$$

the meaning changes completely. The distance of $A$ from zero now exceeds $k$, so the admissible values of $A$ are those lying outside the interval $(-k, k)$. In algebraic terms, the inequality becomes:

$$
A < -k \quad \text{or} \quad A > k
$$

> Transformations of this kind are particularly useful when solving inequalities that contain absolute values. By rewriting the condition without the absolute value symbol, the problem is converted into one or more standard inequalities that can be solved using familiar algebraic techniques.

## Absolute value as a norm

The absolute value is more than a convenient notation for removing signs. It is a norm on $\mathbb{R}$, a function that assigns to each real number a non-negative length, in the same way that a norm on a vector space measures the size of a vector. A norm on a real [vector space](../vector-spaces/) $V$ is a function $\|\cdot\| : V \to [0, +\infty)$ satisfying three conditions for all $x, y \in V$ and all $\lambda \in \mathbb{R}$:

$$
\|x\| = 0 \iff x = 0
$$

$$
\|\lambda x\| = |\lambda| \cdot \|x\|
$$

$$
\|x + y\| \le \|x\| + \|y\|
$$

The absolute value $|\cdot|$ satisfies all three conditions. The first holds by definition, since $|x| = 0$ if and only if $x = 0$. The second follows directly from the multiplicative property $|x \cdot y| = |x| \cdot |y|$, applied with $y = \lambda$. The third is precisely the triangle inequality proved above.

> This observation places the absolute value within a broader mathematical structure and clarifies why its properties, in particular the triangle inequality, are not isolated facts but specific instances of general principles that reappear throughout analysis and linear algebra. The triangle inequality is the standard tool for controlling distances in the $\varepsilon$-definition of convergence used for [sequences](../convergent-and-divergent-sequences/) and [Cauchy sequences](../cauchy-sequence/).
