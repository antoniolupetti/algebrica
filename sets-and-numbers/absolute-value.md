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

Consider the real line, the line containing all [real numbers](../real-numbers/) from negative to positive infinity, and fix a unit of length to measure the distance between any two points $a$ and $b.$ This distance is given by the [Euclidean distance formula](../the-cartesian-coordinate-plane/):

$$
d(a,b)=\sqrt{(a-b)^2} \tag{1}
$$

As we know, a distance is always non-negative and is zero only when the two points coincide. This gives us the absolute value of a real number, which is the distance of a point $x$ from zero. Setting $a=x$ and $b=0$ in $(1),$ we obtain:

$$
|x|=d(x,0)=\sqrt{x^2} \tag{2}
$$

As we know, the [square root](../radicals/) always gives a non-negative value, so we can rewrite $(2)$ in the following form:

$$ \tag{3}
|x| =
\begin{cases}
+x & \text{if } x \geq 0 \\[6pt]
-x & \text{if } x < 0
\end{cases}
\quad
\forall \ x \in \mathbb{R}
$$

For example, $|5|=5$ and $|-6|=-(-6)=6.$ If we replace the origin with an arbitrary point of coordinate $a,$ we can rewrite $(2)$ as follows:

$$
d(x,a)=\sqrt{(x-a)^2}=|x-a|  \tag{4}
$$

Thus, in this case, the absolute value of the difference between the coordinates $x$ and $a$ gives precisely the distance between the two points.


![IMG. 1](svg/real-numbers-1.svg)


More generally, the distance in $(4)$ satisfies the following symmetry relation, since exchanging the two points leaves their distance unchanged.

$$
|x-a| = |a-x|
$$

For example, the distance from $3$ to $7$ is $|3-7|=4,$ which equals the distance from $7$ to $3,$ namely $|7-3|=4.$

- - -

So far, we have discussed absolute value as a number, but if we let $x$ vary over $\mathbb{R},$ we obtain a [function](../functions/) that assigns to each real number its absolute value. This function is defined by:

$$
y = |x| =
\begin{cases}
+x & \text{if } x \geq 0 \\[6pt]
-x & \text{if } x < 0
\end{cases}
$$


![IMG. 1](svg/absolute-value-1.svg)

As the figure shows, its graph consists of two rays meeting at the origin and is symmetric about the $y$-axis, so it is an [even function](../even-and-odd-functions/) satisfying the following relation:

$$|{-x}| = |x| \quad \text{for all } x \in \mathbb{R}$$

For a detailed description of the [absolute value function](../absolute-value-function/), see the corresponding entry.

- - -

In $(3),$ we saw that the sign of $x$ determines how its absolute value is calculated. We can express this dependence through the [sign function](../sign-function/), which allows us to write the absolute value as follows:

$$
|x| = x \cdot \mathrm{sgn}(x)\tag{5}
$$

The sign function is defined on the following [intervals](../intervals/) by:

$$
\mathrm{sgn}(x) =
\begin{cases}
-1 & \text{if } x < 0 \\[6pt]
0 & \text{if } x = 0 \\[6pt]
1 & \text{if } x > 0
\end{cases}
$$

On each interval, the product of $x$ and $\mathrm{sgn}(x)$ is always non-negative, so we obtain the following results, which agree with the definition of absolute value in $(3):$

+ If $x > 0,$ then $\mathrm{sgn}(x) = 1$ and $x \cdot \mathrm{sgn}(x) = x.$
+ If $x < 0,$ then $\mathrm{sgn}(x) = -1$ and $x \cdot \mathrm{sgn}(x) = -x.$
+ If $x = 0,$ then $\mathrm{sgn}(x) = 0$ and $x \cdot \mathrm{sgn}(x) = 0.$

## Properties

Having defined the absolute value of a real number, we list some fundamental properties below. We begin with the one that follows most directly from the definition. As we have said, a real number and its opposite are at the same distance from the origin and therefore have the same absolute value. For example, $|3|=|-3|=3.$ In general, the following identity holds:

$$
|x| = |-x| \quad \forall \ x \in \mathbb{R}
$$

- - -

Since $x$ and $-x$ are at the same distance from the origin, the smaller of the two is non-positive and equals $-|x|,$ while the larger equals $|x|.$ Since $x$ is one of these two values, it lies between $-|x|$ and $|x|,$ so the following relation holds.

$$
-|x| \leq x \leq |x| \quad \forall \ x \in \mathbb{R}
$$

Following this reasoning, we can also conclude that the absolute value is the maximum of $x$ and $-x,$ so we have:

$$
|x| = \max\{x,-x\} \quad \forall \ x \in \mathbb{R}
$$

- - -

From an algebraic perspective, it is important to know that the absolute value of a product equals the product of the absolute values. Indeed, repeated application of this property gives the following identity for every finite product:

$$|x_1 \cdot x_2 \cdots x_n|=|x_1| \cdot |x_2| \cdots |x_n|$$

The property can be stated concisely as:

$$
|x \cdot y| = |x| \cdot |y| \quad \forall \ x, y \in \mathbb{R} \tag{6}
$$

- - -

Now consider two real numbers $x$ and $y.$ These numbers have the same absolute value if and only if they are equal or opposite. From the definition of absolute value, we know that $|x|=|y|$ means that $x$ and $y$ are at the same distance from the origin, which happens exactly when $x=y$ or $x=-y.$ Formally, this property is written as:

$$
|x| = |y| \iff x = \pm y \quad \forall \ x, y \in \mathbb{R}
$$

- - -

For two non-negative numbers, the first is less than or equal to the second if and only if its square is less than or equal to the square of the second. We apply this property to $|x|$ and $|y|,$ which are non-negative for any pair of real numbers $x$ and $y.$ Since $|x|^2=x^2$ and $|y|^2=y^2,$ we can write:

$$
|x| \leq |y| \iff x^2 \leq y^2 \quad \forall \ x, y \in \mathbb{R}
$$

- - -

Another useful property in calculations is that the absolute value of a quotient equals the quotient of the absolute values. Consider two numbers $x$ and $y$ with $y \ne 0$ to ensure that the denominator is non-zero, and apply the product property $(6)$ to the identity $yy^{-1}=1.$ We obtain $|y^{-1}|=|y|^{-1},$ which gives:

$$
\left| \frac{x}{y} \right| = \frac{|x|}{|y|} \quad \forall \ x, y \in \mathbb{R},\ y \ne 0
$$

- - -

Finally, consider the square root of $x^2,$ which, as we know, is always non-negative and therefore equals $x$ if $x\geq 0$ and $-x$ if $x<0.$ We can therefore write this last identity, which is particularly important because it often arises in equations, especially [equations involving radicals](../irrational-equations/):

$$
\sqrt{x^2} = |x| \quad \forall \ x \in \mathbb{R}
$$

## Triangle inequality

To introduce the triangle inequality, we begin with an intuitive argument. If we want to go from a point $a$ to a point $b,$ we know that the shortest path is the line segment joining them. Passing through a third point may make the path longer, but it cannot make it shorter. Applying the same reasoning to a triangle, we find that the length of one side is always less than or equal to the sum of the lengths of the other two. If we now consider the path from $0$ to $a+b$ through $a,$ the first part has length $|a|$ and the second has length $|b|.$ The distance between the starting point and the endpoint, however, is $|a+b|.$ This gives us precisely the triangle inequality, expressed by the following relation:

$$
|a + b| \le |a| + |b| \tag{7}
$$

To make this clearer, suppose, for example, that we start at $0$ and move to the right until we reach $5.$ We then turn back and reach $2,$ travelling a further 3 units. We have travelled a total of $8$ units, but the distance between the starting point $0$ and the endpoint $2$ is only $2,$ in agreement with $(7).$

- - -

To prove $(7)$ formally, we consider all possible cases for the signs of $a$ and $b:$

$$
\begin{align}
(1)\quad & a \ge 0, \quad b \ge 0 \\[6pt]
(2)\quad & a \le 0, \quad b \le 0 \\[6pt]
(3)\quad & a \ge 0, \quad b \le 0 \\[6pt]
(4)\quad & a \le 0, \quad b \ge 0
\end{align}
$$

In case $(1),$ the sum satisfies $a + b \geq 0,$ so we have:

$$
|a + b| = a + b = |a| + |b|
$$

In case $(2),$ the sum instead satisfies $a + b \leq 0,$ so the following relation holds:

$$
|a + b| = -(a + b) = (-a) + (-b) = |a| + |b|
$$

In case $(3),$ since $a \ge 0$ and $b \le 0,$ we have $|a| = a$ and $|b| = -b,$ so $|a| + |b| = a - b.$ To prove that $|a + b| \le a - b,$ we must distinguish the following cases:

+ When $a + b \ge 0,$ we have $|a + b| = a + b \le a - b,$ since $b \le 0.$
+ When $a + b \le 0,$ we instead obtain $|a + b| = -(a + b) = -a - b \le a - b.$

The last inequality is equivalent to $-a \le a,$ and this condition holds because $a \ge 0.$ Finally, case $(4)$ reduces to case $(3)$ by exchanging $a$ and $b.$

- - -

The reverse triangle inequality also follows from $(7);$ that is, for all $a,b \in \mathbb{R},$ we have:

$$
\bigl||a| - |b|\bigr| \le |a - b| \tag{8}
$$

In this relation, the absolute value of the difference between the distances of $a$ and $b$ from zero is less than or equal to the distance between $a$ and $b.$ To prove it, we apply the triangle inequality to the identity $a=(a-b)+b,$ obtaining:

$$
|a| = |(a - b) + b| \le |a - b| + |b|
$$

This gives $|a| - |b| \le |a - b|.$ Exchanging $a$ and $b,$ we obtain $|b| - |a| \le |a - b|,$ and since both $|a| - |b|$ and $|b|-|a|$ are less than or equal to $|a - b|,$ we conclude that $(8)$ holds.

## Further considerations

Absolute value applies to real numbers and, as we have noted several times in this entry, measures their distance from zero. A norm $\|\cdot\|$ extends this idea to [vectors](../vectors/) by assigning each vector a non-negative length. In general, a norm on a real [vector space](../vector-spaces/) $V$ is a function $\|\cdot\|:V \to [0,+\infty)$ satisfying the following three properties for all $x,y \in V$ and all $\lambda \in \mathbb{R}:$

$$
\begin{align}
\quad & \|x\| = 0 \iff x = 0 \\[6pt]
\quad & \|\lambda x\| = |\lambda| \cdot \|x\| \\[6pt]
\quad & \|x + y\| \le \|x\| + \|y\|
\end{align}
$$

Absolute value satisfies all three properties: the first follows from the definition in $(3),$ the second is the product property $(6)$ applied to $\lambda x,$ and the third is the triangle inequality given in $(7).$

- - -

Finally, it is worth mentioning [inequalities involving absolute value](../inequalities-with-absolute-value/), which express a condition on distance along the real line. The first case is the inequality $|A| < k,$ which can be written equivalently as:

$$
-k < A < k
$$
The second case has the form $|A| > k,$ which can be rewritten as:

$$
A < -k \quad \text{or} \quad A > k
$$

For a detailed explanation, see the corresponding entry.
