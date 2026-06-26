## Introduction

The [absolute value](../absolute-value) of a number, is defined as follows:

\\[
|x| =
\begin{cases}
+x & \text{if } x \geq 0 \\\\[0.5em]
-x & \text{if } x < 0
\end{cases}
\quad \forall \\, x \in \mathbb{R} 
\\]

The absolute value function assigns to each real number its distance from zero on the number line. This means that negative numbers are mapped to their positive counterparts, while positive numbers remain unchanged, since distance is always non-negative. 

More generally, the absolute value expression \\(|x - a|\\) can be interpreted as the distance between the point \\(x\\) and the point \\(a\\) on the number line. We have:

\\[|x-a| = |a-x| \\]

In fact, we can observe that \\( a - x \\) is simply the opposite of \\( x - a \\); in other words \\(a - x = -(x - a)\\). It follows that \\(|a - x| = |- (x - a)| = |x - a|\\). This shows that the two expressions have the same absolute value, even though the terms inside the parentheses appear in reverse order.

## Graph and symmetry of the absolute value function

The absolute value function is:

\\[
y = |x| =
\begin{cases}
+x & \text{if } x \geq 0 \\\\[0.5em]
-x & \text{if } x < 0 
\end{cases}
\\]

The graph of \\(y= |x|\\) is:

- - -

The graph of the absolute value function \\( |x| \\) is symmetric with respect to the y-axis. This symmetry implies that the function is [even](../even-and-odd-functions/), meaning it satisfies the identity:

\\[|{-x}| = |x| \quad \text{for all } x \in \mathbb{R}\\]

## Properties

- [Domain](../determining-the-domain-of-a-function/): \\( \mathbb{R} \\).
- Range: \\( \mathbb{R}^+_0 \\).
- The function is [decreasing](../increasing-and-decreasing-functions/) on \\( (-\infty, 0] \\)and increasing on \\( [0, +\infty) \\).  
- The function is [even](../even-and-odd-functions/), since \\( |{-x}| = |x| \\).  
- The function is [continuous](../continuous-functions/) over the entire real line \\( \mathbb{R} \\).
- The function is differentiable everywhere except at \\( x = 0 \\) where it has a [corner point](../points-of-non-differentiability/).  
- The function has an [absolute minimum](../maximum-minimum-and-inflection-points/) at \\( x = 0 \\), where \\( |x| = 0 \\) and it has no maximum. 
- Limits as \\( x \\) approaches the extremes of the domain:
\\[
\begin{align}
\lim_{x \to -\infty} |x| &= +\infty \\\\[0.5em]
\lim_{x \to +\infty} |x| &= +\infty
\end{align}
\\]

## How to graph the absolute value of a function: flip the negative part

Let us consider the [parabola](../parabola) defined by the equation

\\[
y = x^2 - 1
\\]

This graph includes a portion of the curve that lies below the x-axis, specifically in the interval where the function takes negative values. 

To find this interval, we solve:

\\[
x^2 - 1 < 0 \rightarrow -1 < x < 1.
\\]

So, the function \\( y = x^2 - 1 \\) is negative on the open interval \\( (-1, 1) \\), and the graph dips below the x-axis in that region.

- - -

To graph the function \\( f(x) = |x^2 - 1| \\), we start from the graph of \\( y = x^2 - 1 \\). We leave unchanged the portions of the graph that lie on or above the x-axis, and we reflect across the x-axis all portions that were originally below it. We obtain:

This transformation ensures that all function values become non-negative, as required by the absolute value.

## Limits, derivatives, and integrals of the absolute value function

The fundamental [limit](../limits) associated with the absolute value function is:
\\[
\lim_{x \to 0} \frac{|x|}{x}
\\]
This limit does not exist, because the left-hand and right-hand limits are different:
\\[
\lim_{x \to 0^-} \frac{|x|}{x} = -1 \quad \text{and} \quad \lim_{x \to 0^+} \frac{|x|}{x} = 1
\\]
This behavior highlights the non-differentiability of \\( |x| \\) at \\( x = 0 \\).

- - -

The [derivative](../derivatives) of the absolute value function is defined piecewise as:
\\[
\frac{d}{dx} |x| =
\begin{cases}
1 & \text{if } x > 0 \\\\[0.5em]
-1 & \text{if } x < 0
\end{cases}
\\]
The derivative does not exist at \\( x = 0 \\), because the function has a [sharp corner](../points-of-non-differentiability/) at that point.

- - -

The [indefinite integral](../indefinite-integrals) of the absolute value function is:
\\[
\int |x| \\, dx = \frac{x^2 \cdot \operatorname{sgn}(x)}{2} + c
\\]
where \\( \operatorname{sgn}(x) \\) is the [sign function](../sign-function/), defined as:
\\[
\operatorname{sgn}(x) =
\begin{cases}
-1 & \text{if } x < 0 \\\\[0.5em]
0 & \text{if } x = 0 \\\\[0.5em]
1 & \text{if } x > 0
\end{cases}
\\]