---
title: Determining the Domain of a Function
source: https://algebrica.org/determining-the-domain-of-a-function/
license: CC BY-NC 4.0
tags:
  - domain
  - domain-restrictions
  - elementary-functions
  - intervals
---
## A systematic method for determining the domain of a function

In the introduction to [functions](../functions/), we discussed the domain of a function, that is, the set of input values for which an expression is mathematically meaningful. We also examined how to determine the domain of basic families of functions such as [polynomials](../polynomials/), [radicals](../radicals/), [logarithms](../logarithms/), and [trigonometric](../sine-and-cosine/) expressions.

In practice we often encounter more elaborate expressions that combine several types of functions in a single formula. In these situations identifying the domain is not immediate, because each internal component may introduce its own restrictions. The most effective strategy can be summarized in the following steps:

+ Examine the inner components of the expression and determine the domain required by each of them.
+ Move outward, layer by layer, propagating the restrictions imposed by every new operation or function involved.
+ Combine all the resulting conditions by intersection, since the overall domain consists only of the values that satisfy every constraint simultaneously.

To see how the procedure works in practice, it is helpful to move directly to concrete examples and apply each step to real expressions.

## Types of intervals

When studying the domain of a function, it is useful to recall how real [intervals](../intervals/) are defined, since the domain is always expressed as a union of such sets. Intervals describe continuous portions of the real line and provide a compact way to specify which values of $x$ are allowed. The first type is the open interval, which contains all points strictly between two endpoints while excluding the endpoints themselves. In descriptive form it is written:

$$
\{\,x : a < x < b\,\}
$$

and in interval notation it appears as:

$$
(a, b)
$$

This notation is convenient when $a$ and $b$ correspond to points where the function is not defined or where a [discontinuity](../discontinuities-of-real-functions/) occurs. Graphically, the endpoints $a$ and $b$ are shown as open circles to indicate that they are not included, while the segment connecting them represents all values strictly between $a$ and $b$. This makes an open interval immediately recognizable, emphasizing that its endpoints are excluded.

[shortcode="intervals"]
|     | $a$  | $b$      |     |
|:----|------------|---------------|-----|
|     | sign+l-in-o-h  |   sign+r-in-o-h  |     |
[/shortcode]

The second type is the closed interval, which includes both endpoints. In descriptive form it is written:

$$
\{\,x : a \le x \le b\,\}
$$

and the corresponding interval notation is:

$$
[a, b]
$$

This representation is typical when the function is defined and continuous even at the boundary points $a$ and $b$. The closed interval is represented graphically by filling the endpoints. The solid dots indicate that both boundary values are included, while the segment between them depicts every point from $a$ to $b$. This makes the structure of a closed interval clear, emphasizing that its endpoints belong to the set.

[shortcode="intervals"]
|     | $a$  | $b$      |     |
|:----|------------|---------------|-----|
|     | sign+l-in-c-h  |   sign+r-in-c-h  |     |
[/shortcode]

Other combinations of open and closed endpoints are also possible. For instance, one may have a half-closed interval such as $[a, +\infty)$, or more generally intervals that mix inclusion and exclusion at their boundaries such as $(a, b]$. These forms are commonly used when describing domains that extend indefinitely or start from a specific boundary value.

[shortcode="intervals"]
|     | $a$  | $b$      |     |
|:----|------------|---------------|-----|
|     | sign+l-c-h  |    |     |
|     | sign+l-in-o-h  |   sign+r-in-c-h  |     |
[/shortcode]

## Domain of elementary functions

It is useful to summarize the domain restrictions induced by the most common expressions:

+ Polynomials: always defined on $\mathbb{R}$
+ Rational functions: denominator $\neq 0$
+ Even roots: radicand $\ge 0$
+ Odd roots: always defined on $\mathbb{R}$
+ Logarithms: argument $> 0$, base $> 0$, base $\neq 1$
+ Absolute values: always defined on $\mathbb{R}$
+ Trigonometric functions $\sin x$ and $\cos x$: always defined on $\mathbb{R}$
+ Inverse trigonometric functions: argument within specific bounds

> The even-root condition is the radicand being non-negative, $\ge 0$, not strictly positive: $\sqrt{0} = 0$ is defined.

## Example 1

To show how the graphical method is used, let us consider the function:

$$
f(x) = \log(x - 1) + \sqrt{x + 4}
$$

To determine its domain, each component must be examined separately, because the function is defined only for those values of $x$ that satisfy all underlying conditions at the same time.

- - -

The logarithmic term $\log(x - 1)$ requires its argument to be strictly positive, which leads to the condition:

$$
x - 1 > 0
$$

Only values greater than $1$ are admissible; any value less than or equal to $1$ violates the definition of the logarithm. Graphically, we represent the condition as follows:

[shortcode="intervals"]
|     | $1$  |       |    
|:----|------------|---------------|
|     | sign+l-o  |    |
[/shortcode]

The square root term $\sqrt{x + 4}$ requires its argument to be non-negative:

$$
x + 4 \ge 0
$$

so the values $x \ge -4$ are allowed. Compared with the logarithmic constraint, this requirement is less restrictive, since every value greater than $1$ is automatically greater than $-4$. Adding this result to the previous diagram, we obtain:

[shortcode="intervals"]
|     | $-4$  | $1$      |     |
|:----|------------|---------------|-----|
|     |   |   sign+l-o   |     |
|     | sign+l-c |     |     |
|     |   |   sign+l-o-h   |     |
[/shortcode]

Putting everything together, the domain is obtained by intersecting the two conditions $x > 1$ and $x \ge -4$. Because $x > 1$ already implies $x \ge -4$, the intersection reduces to the inequality $x > 1$. The domain corresponds to the highlighted segment, that is, the interval:

$$
(1, +\infty)
$$

## Example 2

Let us consider an example that combines a square root, a logarithm, and a trigonometric function:

$$
f(x) = \sqrt{\frac{\log(2 + \sin x)}{\sinh(x)}}
$$

Determining the domain is not immediate. One initial observation is that the presence of a trigonometric term suggests that the conditions we obtain are likely to repeat periodically. We apply the method outlined above, examining the restrictions introduced by each component, starting from the innermost element.

- - -

The first element we encounter is the [logarithm](../logarithms/):

$$\log(2 + \sin x)$$

Since the logarithm is defined only for strictly positive arguments, we require:

$$2 + \sin x > 0$$

Because $\sin x$ ranges between $-1$ and $1$, the smallest value this expression can take is $2 - 1 = 1$, which is already positive. The logarithm therefore introduces no restriction, as its argument is positive for every real $x$.

- - -

Moving one step outward, the logarithm appears in the numerator of a fraction whose denominator is the [hyperbolic sine](../hyperbolic-sine-and-cosine/) $\sinh(x)$. A denominator cannot be zero, since division by zero is not defined in the [real numbers](../real-numbers/), so we exclude the values of $x$ for which $\sinh(x) = 0$. The hyperbolic sine vanishes only at $x = 0$, so this point must be removed from the domain.

- - -

Finally, the entire fraction appears under a square root, whose argument must be non-negative.

+ The numerator $\log(2 + \sin x)$ is always non-negative and equals zero precisely when $\sin x = -1$, that is, at the points $x = -\frac{\pi}{2} + 2k\pi$. At those points the fraction is zero, hence acceptable, provided the denominator is non-zero, which holds except at $x = 0$, already excluded.
+ For all other values, $\log(2 + \sin x)$ is strictly positive, so the sign of the fraction depends only on the sign of $\sinh(x)$. The hyperbolic sine is positive for $x > 0$ and negative for $x < 0$. Since the radicand must be non-negative, the fraction is admissible exactly when $x > 0$, or when the numerator is zero.

Putting these observations together, the domain consists of all $x$ greater than zero, together with the isolated points where $\sin x = -1$. The domain is therefore:

$$
(0, +\infty) \;\cup\; \left\{ -\frac{\pi}{2} + 2k\pi \,\middle|\, k \in \mathbb{Z} \right\}
$$

## Example 3

Let us determine the domain of the function:

$$
f(x) = \sqrt{\cos^{2}(3x - 1) - \log\!\bigl(5 - |2x|\bigr)}
$$

We examine the expression from the inside out, identifying the restrictions introduced by each component and combining them at the end. The first element that imposes a constraint is the logarithm. Since the logarithm accepts only strictly positive arguments, we require:

$$
5 - |2x| > 0
$$

Solving this [inequality](../inequalities-with-absolute-value/), which involves an [absolute value](../absolute-value/), gives:

$$
|2x| < 5 \quad \rightarrow \quad -\frac{5}{2} < x < \frac{5}{2}
$$


The trigonometric part $\cos^{2}(3x - 1)$ introduces no additional restriction, because the [cosine function](../cosine-function/) and its square are defined for all real $x$.


We now move one level outward and consider the whole expression inside the square root. A square root is defined only when its argument is non-negative, so we impose:

$$
\cos^{2}(3x - 1) - \log(5 - |2x|) \ge 0
$$

This inequality links two terms with very different behaviour. The squared cosine oscillates between $0$ and $1$, while the logarithm varies over $\left(-\infty, \log 5\right]$ on the admissible interval and tends to $-\infty$ as $|2x|$ approaches $5$ from below. The inequality holds only where the logarithmic term does not exceed the squared cosine:

$$
\log(5 - |2x|) \le \cos^{2}(3x - 1)
$$


The solutions are contained in $\left(-\frac{5}{2}, \frac{5}{2}\right)$, since outside this interval the logarithm is undefined. Combining the two requirements by intersection, the domain is the set of points of that interval which also satisfy the radicand condition:

$$
\mathrm{dom}(f) = \left\{\, x \in \left(-\tfrac{5}{2}, \tfrac{5}{2}\right) \ \middle|\ \cos^{2}(3x - 1) \ge \log(5 - |2x|) \,\right\}
$$

This last inequality has no elementary closed-form solution and must be examined numerically or graphically. It is a proper restriction, not the whole interval: near $x = 0$, for instance, we have $\log 5 \approx 1.61$, which exceeds $\cos^{2}(1) \approx 0.29$, so a neighbourhood of the origin is excluded. The domain is therefore a proper subset of $\left(-\frac{5}{2}, \frac{5}{2}\right)$.
