---
title: Arctangent and Arccotangent
source: https://algebrica.org/arctangent-and-arccotangent/
license: CC BY-NC 4.0
tags:
  - arccotangent
  - arctangent
  - inverse-trigonometric-functions
  - trigonometry
---

## Arctangent definition

In the [unit circle](../unit-circle/), the [tangent](../tangent-and-cotangent/) of an angle $\theta$ can be visualised as the length of the segment tangent to the circle at the point where the terminal side meets it, measured along the vertical tangent line at $(1, 0)$. The arctangent performs the reverse process: given a [real number](../properties-of-real-numbers/) $x$, it returns the unique angle $\theta$ in the interval $\left(-\pi/2, \pi/2\right)$ whose tangent equals $x$. This geometric relationship illustrates how the tangent and arctangent are interconnected as a function and its inverse, each reversing the role of angle and ratio.

![IMG. 1](svg/arctangent-and-arccotangent-1.svg)

By relating the arctangent to the concept of a [function](../functions/), we can formally express the relationship between tangent and arctangent as follows:

$$
\begin{align}
\arctan(x) &= \theta \quad \iff \quad \tan(\theta) = x \\[6pt]
\theta &\in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)
\end{align}
$$

The arctangent establishes a correspondence between a real number $x$ and the unique angle $\theta$ in the interval $\left(-\pi/2, \pi/2\right)$ whose tangent equals $x$. The restriction to this interval is necessary because the tangent function is periodic and therefore not injective over its full domain. By confining it to $\left(-\pi/2, \pi/2\right)$, one obtains a strictly increasing bijection, which admits a well-defined [inverse](../inverse-function/). This reciprocal relationship is summarized by the identity:

$$
\tan(\arctan(x)) = x \quad \forall x \in \mathbb{R}
$$

+ When the tangent value $x$ is positive, the corresponding angle $\theta$ lies in the first quadrant.

+ When $x$ is negative, the angle lies in the fourth quadrant; and when $x = 0$, the angle is zero.

As $x$ grows without bound, the corresponding angle $\theta$ approaches the [asymptotic](../asymptotes/) values:

$$
\begin{align}
\lim_{x \to +\infty} \arctan(x) &= \frac{\pi}{2} \\[6pt]
\lim_{x \to -\infty} \arctan(x) &= -\frac{\pi}{2}
\end{align}
$$

These values are never attained, since no finite value of $x$ has tangent equal to $\pm \pi/2$. They correspond to the directions in which the terminal side of the angle becomes parallel to the $y$-axis.

## Reference values of arctangent

Below are some commonly known values of $\arctan(x)$ for selected inputs, useful in various applications of trigonometry:

$$
\begin{align}
x &\to -\infty  &\quad& \arctan(x) \to -\pi/2 \\[6pt]
x &= -\sqrt{3} &\quad& \arctan(-\sqrt{3}) = -\pi/3 \\[6pt]
x &= -1 &\quad& \arctan(-1) = -\pi/4 \\[6pt]
x &= -1/\sqrt{3} &\quad& \arctan(-1/\sqrt{3}) = -\pi/6 \\[6pt]
x &= 0 &\quad& \arctan(0) = 0 \\[6pt]
x &= 1/\sqrt{3} &\quad& \arctan(1/\sqrt{3}) = \pi/6 \\[6pt]
x &= 1 &\quad& \arctan(1) = \pi/4 \\[6pt]
x &= \sqrt{3} &\quad& \arctan(\sqrt{3}) = \pi/3 \\[6pt]
x &\to +\infty &\quad& \arctan(x) \to \pi/2
\end{align}
$$

## Arctangent function

The arctangent function $f(x) = \arctan(x)$ assigns to each real number $x \in \mathbb{R}$ the unique angle $\theta \in \left(-\pi/2, \pi/2\right)$ whose tangent equals $x$. Its graph is a continuous, strictly increasing curve that admits two horizontal asymptotes, namely $y = -\pi/2$ and $y = \pi/2$. The function is the [inverse](../inverse-function/) of the tangent restricted to its principal domain $\left(-\pi/2, \pi/2\right)$, over which the tangent is strictly increasing and bijective.

+ Domain: $x \in \mathbb{R}$
+ Range: $y \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$
+ The arctangent is an [odd function](../even-and-odd-functions/), meaning that:

  $$
  \arctan(-x) = -\arctan(x) \quad \forall x \in \mathbb{R}
  $$

  This follows directly from the fact that the tangent is itself an odd function, and reflects the symmetry of the graph of $\arctan$ with respect to the origin.

> A [bijective function](../functions/) is both injective and surjective, that is, if for every $y \in B$ there exists a unique $x \in A$ such that $f(x) = y$.

## Analytical expression of the arctangent

The arctangent can also be written using the [sine and cosine](../sine-and-cosine/) functions, which highlights its geometric foundation on the unit circle and its connection with the other inverse trigonometric functions. Starting from the identity:

$$
\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)}
$$

one can consider a [right triangle](../right-triangle-trigonometry/) in which the angle $\theta$ satisfies $\tan(\theta) = x$, that is, the ratio of the opposite side to the adjacent side equals $x$. Taking the adjacent side equal to $1$ and the opposite side equal to $x$, the hypotenuse is $\sqrt{1 + x^2}$ by the [Pythagorean theorem](../pythagorean-theorem/), so that:

$$
\begin{align}
\sin(\theta) &= \frac{x}{\sqrt{1 + x^2}} \\[6pt]
\cos(\theta) &= \frac{1}{\sqrt{1 + x^2}}
\end{align}
$$

Reversing these relationships yields two equivalent expressions for the arctangent:

$$
\begin{align}
\arctan(x) &= \arcsin\!\left(\frac{x}{\sqrt{1 + x^2}}\right) \\[6pt]
\arctan(x) &= \arccos\!\left(\frac{1}{\sqrt{1 + x^2}}\right)
\end{align}
$$

> This equivalence is often useful in calculus and in analytical derivations, because it allows expressions involving the arctangent to be rewritten in terms of the [arcsine or arccosine](../arcsine-and-arccosine/), depending on which form simplifies the computation.

## Addition formula for the arctangent

The arctangent satisfies a notable identity that expresses the arctangent of a sum in terms of the individual arctangents. For any two real numbers $x$ and $y$ satisfying $xy < 1$, the following identity holds:

$$
\arctan(x) + \arctan(y) = \arctan\!\left(\frac{x + y}{1 - xy}\right)
$$

This formula follows directly from the addition formula for the tangent function. If $\alpha = \arctan(x)$ and $\beta = \arctan(y)$, then $\tan(\alpha) = x$ and $\tan(\beta) = y$, and the tangent addition formula gives:

$$
\tan(\alpha + \beta) = \frac{\tan(\alpha) + \tan(\beta)}{1 - \tan(\alpha)\tan(\beta)} = \frac{x + y}{1 - xy}
$$

Applying the arctangent to both sides then yields the identity. The condition $xy < 1$ ensures that $\alpha + \beta \in \left(-\pi/2, \pi/2\right)$, which is the principal interval of the arctangent; when $xy > 1$, a correction term of $\pm\pi$ must be added depending on the sign of $x$.

A particularly useful special case arises by setting $y = 1/x$ with $x > 0$, so that $xy = 1$. In this situation the general formula does not apply directly, but one can verify the result by observing that $\arctan(x)$ and $\arctan\!\left(1/x\right)$ are complementary angles. The identity takes the form:

$$
\arctan(x) + \arctan\!\left(\frac{1}{x}\right) = \frac{\pi}{2} \qquad (x > 0)
$$

This follows from the fact that for $x > 0$ one has $\mathrm{arccot}(x) = \arctan\!\left(1/x\right)$, and the complementarity relation $\arctan(x) + \mathrm{arccot}(x) = \pi/2$ holds for all positive $x$.

## Arccotangent definition

In the [unit circle](../unit-circle/), the [cotangent](../tangent-and-cotangent/) of an angle $\theta$ can be visualized as the length of the segment tangent to the circle at the point where the terminal side meets it, measured along the horizontal tangent line at $(0, 1)$. The arccotangent performs the reverse process: given a real number $x$, it returns the unique angle $\theta$ in the interval $(0, \pi)$ whose cotangent equals $x$. This geometric relationship illustrates how the cotangent and arccotangent are interconnected as a function and its inverse, each reversing the role of angle and ratio.

![IMG. 2](svg/arctangent-and-arccotangent-2.svg)

By relating the arccotangent to the concept of a [function](../functions/), we can formally express the relationship between cotangent and arccotangent as follows:

$$
\begin{align}
\mathrm{arccot}(x) &= \theta \quad \iff \quad \cot(\theta) = x \\[6pt]
\theta &\in (0, \pi)
\end{align}
$$

The arccotangent establishes a correspondence between a real number $x$ and the unique angle $\theta$ in the interval $(0, \pi)$ whose cotangent equals $x$. The restriction to this interval is necessary because the cotangent function is periodic and therefore not injective over its full domain; by confining it to $(0, \pi)$, one obtains a strictly decreasing bijection, which admits a well-defined [inverse](../inverse-function/). This reciprocal relationship is summarized by the identity:

$$
\cot(\mathrm{arccot}(x)) = x \quad \text{for all } x \in \mathbb{R}
$$

+ When the cotangent value $x$ is positive, the corresponding angle $\theta$ lies in the first quadrant.
+ When $x$ is negative, the angle lies in the second quadrant; and when $x = 0$, the angle equals $\frac{\pi}{2}$.

As $x$ grows without bound, the corresponding angle $\theta$ approaches the asymptotic values:

$$
\begin{align}
\lim_{x \to +\infty} \mathrm{arccot}(x) &= 0 \\[6pt]
\lim_{x \to -\infty} \mathrm{arccot}(x) &= \pi
\end{align}
$$

  These values are never attained, since no finite value of $x$ has cotangent equal to $0$ or $\pi$; they correspond to the directions in which the terminal side of the angle becomes parallel to the $x$-axis.

## Reference values of arccotangent

Below are some commonly known values of $\mathrm{arccot}(x)$ for selected inputs, useful in various applications of trigonometry:

$$
\begin{align}
x &\to -\infty  &\quad& \mathrm{arccot}(x) \to \pi \\[6pt]
x &= -\sqrt{3} &\quad& \mathrm{arccot}(-\sqrt{3}) = 2\pi/3 \\[6pt]
x &= -1 &\quad& \mathrm{arccot}(-1) = 3\pi/4 \\[6pt]
x &= -1/\sqrt{3} &\quad& \mathrm{arccot}(-1/\sqrt{3}) = 5\pi/6 \\[6pt]
x &= 0 &\quad& \mathrm{arccot}(0) = \pi/2 \\[6pt]
x &= 1/\sqrt{3} &\quad& \mathrm{arccot}(1/\sqrt{3}) = \pi/3 \\[6pt]
x &= 1 &\quad& \mathrm{arccot}(1) = \pi/4 \\[6pt]
x &= \sqrt{3} &\quad& \mathrm{arccot}(\sqrt{3}) = \pi/6 \\[6pt]
x &\to +\infty &\quad& \mathrm{arccot}(x) \to 0
\end{align}
$$

## Arccotangent function

The arccotangent function $f(x) = \mathrm{arccot}(x)$ assigns to each real number $x \in \mathbb{R}$ the unique angle $\theta \in (0, \pi)$ whose cotangent equals $x$. Its graph is a continuous, strictly decreasing curve that admits two horizontal asymptotes, namely $y = 0$ and $y = \pi$. The function is the [inverse](../inverse-function/) of the cotangent restricted to its principal domain $(0, \pi)$, over which the cotangent is strictly decreasing and bijective.

+ Domain: $x \in \mathbb{R}$
+ Range: $y \in (0, \pi)$
+ The arccotangent satisfies the identity:
  $$
  \mathrm{arccot}(-x) = \pi - \mathrm{arccot}(x) \quad \forall x \in \mathbb{R}
  $$

  This follows from the fact that the cotangent is an odd function, and reflects the symmetry of the graph of $\mathrm{arccot}$ with respect to the point $\left(0, \pi/2\right)$.

## Analytical expression of the arccotangent

The arccotangent can also be expressed in relation to the arctangent, sine, and cosine functions, emphasizing its complementary nature within the family of inverse trigonometric functions. Starting from the identity:

$$
\cot(\theta) = \frac{\cos(\theta)}{\sin(\theta)}
$$

one can consider a right triangle in which $\cot(\theta) = x$, that is, the ratio of the adjacent side to the opposite side equals $x$. Taking the opposite side equal to $1$ and the adjacent side equal to $x,$ the hypotenuse is $\sqrt{1 + x^2}$ by the Pythagorean theorem, so that:

$$\sin(\theta) = \frac{1}{\sqrt{1 + x^2}}$$
$$ \cos(\theta) = \frac{x}{\sqrt{1 + x^2}}$$

Reversing these relationships yields two equivalent expressions for the arccotangent:
$$
\begin{align}
\mathrm{arccot}(x) &= \arcsin\!\left(\frac{1}{\sqrt{1 + x^2}}\right) \\[6pt]
\mathrm{arccot}(x) &= \arccos\!\left(\frac{x}{\sqrt{1 + x^2}}\right)
\end{align}
$$

Two further identities connect the arccotangent directly to the arctangent. For positive values of $x$, one has:

$$
\mathrm{arccot}(x) = \arctan\!\left(\frac{1}{x}\right)
$$

since the cotangent and tangent of the same angle are reciprocals of each other. A more general identity, valid for all $x \in \mathbb{R}$, is:

$$
\mathrm{arccot}(x) = \frac{\pi}{2} - \arctan(x)
$$

which follows from the complementary relationship between tangent and cotangent: for any angle $\theta$, one has $\cot(\theta) = \tan\!\left(\frac{\pi}{2} - \theta\right)$, so inverting both sides yields the identity directly.
