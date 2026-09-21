---
title: Arc Length of a Curve
source: https://algebrica.org/arc-length-of-a-curve/
license: CC BY-NC 4.0
tags:
  - arc-length
  - cartesian-coordinates
  - definite-integral
  - derivatives
  - integration
  - mean-value-theorem
  - parametric-curves
  - rectifiable-curves
  - riemann-integral
---
## From line segments to curved arcs

To determine the length of a line segment joining two distinct points in the plane, $A$ and $B,$ we use the Euclidean distance formula:

$$
d(A,B)=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2} \tag{1}
$$

This simple and fairly intuitive formula uses the differences between the points' $x$- and $y$-coordinates, measured along the coordinate axes, and applies directly to a line segment, which is simply a straight portion of a line. The situation becomes more complicated when, instead of a segment, we need to measure the length of a curve, which typically does not follow a straight path and may have a more varied shape.

In such cases, we use a construction based on the same procedure used to define the [definite integral](../definite-integrals/), approximating the curve by segments whose lengths are easy to measure and then taking a [limit](../limits/). Consider, for example, a function $f(x)$ that is [continuous](../continuous-functions/) and differentiable with a continuous derivative on a closed interval $[a, b].$ Our aim is to measure the arc between the points with $x$-coordinates $a$ and $b$ by assigning it a real number that measures its length. First, we inscribe a polygonal line in the curve, then calculate its length and progressively improve the approximation by adding points whose spacing along the $x$-axis tends to zero.

Formally, let $P = \{\ x_0, x_1, \dots, x_n \ \}$ be a [partition](../riemann-integrability-criteria/) of the interval $[a, b]$ such that:

$$a = x_0 < x_1 < \cdots < x_n = b$$

We construct the polygonal line by associating each point of the partition with the point $(x_k, f(x_k))$ on the graph of the function. Joining the resulting points by line segments gives a polygonal line inscribed in the curve, whose total length is the sum of the Euclidean distances between consecutive points. The length of the individual segment with index $k$ can therefore be obtained from the following Euclidean distance formula, which is an instance of $(1)$:

$$\ell_k = \sqrt{(x_k - x_{k-1})^2 + (f(x_k) - f(x_{k-1}))^2} \tag{2}$$

![Fig. 1](svg/arc-length-of-a-curve-1.svg)


Since $f$ is differentiable on $[x_{k-1}, x_k],$ the [mean value theorem](../lagrange-theorem/) guarantees a point $\xi_k$ in the open interval $(x_{k-1}, x_k)$ such that:

$$f(x_k) - f(x_{k-1}) = f'(\xi_k)(x_k - x_{k-1})$$

Substituting this identity into $(2)$ and factoring out $(x_k - x_{k-1})^2$ gives:

$$\ell_k = \sqrt{1 + [f'(\xi_k)]^2}(x_k - x_{k-1})$$

The total length of the polygonal line inscribed in the curve is therefore a Riemann sum of the function $\sqrt{1 + [f'(x)]^2}$ for the partition $P,$ and as the mesh of the partition tends to zero, this sum converges to a definite integral.

## Arc length in Cartesian form

The construction just described leads to the definition of length for curves expressed as graphs of functions in the [Cartesian plane](../the-cartesian-coordinate-plane/). Consider a function $f$ with a continuous [derivative](../derivatives/) on the closed [interval](../intervals/) $[a, b].$ The arc length of the graph of $f$ from $x = a$ to $x = b$ is defined by the following definite integral:

$$L = \int_a^b \sqrt{1 + [f'(x)]^2} \ dx \tag{3}$$

The continuity of $f'$ on $[a, b]$ guarantees the continuity of the integrand and hence its Riemann integrability. A function whose derivative is bounded but not continuous may still have a graph with a well-defined length. In this case, the elementary proof just presented does not apply directly, and the discussion requires the more general framework of rectifiable curves.

The expression $\sqrt{1 + [f'(x)]^2} \ dx$ is called the arc length element and is denoted by $ds.$ It expresses the infinitesimal length of the curve associated with an infinitesimal increment $dx$ of the independent variable and satisfies the following identity:
$$ds^2 = dx^2 + dy^2 \tag{4}$$
A closer look at $(4)$ reveals the [Pythagorean theorem](../pythagorean-theorem/) applied to a right triangle with legs $dx$ and $dy = f'(x) \ dx.$

- - -

As a practical example, we calculate the length of the [parabolic arc](../parabola/) described by the function $f(x) = x^2$ on the interval $[0, 1].$ To do this, we apply $(3),$ first calculating the derivative of $f$ to obtain:

$$f'(x) = 2x$$

Substituting into formula $(3),$ we can express the arc length as:

$$L = \int_0^1 \sqrt{1 + 4x^2} \ dx$$

This is an integral of an algebraic function involving a square root of the form $\sqrt{1 + (2x)^2},$ which is typically evaluated by the [substitution](../integration-by-substitution/) $2x = \sinh t.$ The corresponding [differential relation](../differential-of-a-function/) is $2 \ dx = \cosh t \ dt,$ giving:

$$dx = \frac{1}{2}\cosh t \ dt$$

The [hyperbolic identity](../hyperbolic-identities/) $1 + \sinh^2 t = \cosh^2 t$ allows us to simplify the radical to $\cosh t,$ obtaining:

$$L = \int_0^{\mathrm{arsinh} 2} \cosh t \cdot \frac{1}{2}\cosh t \ dt = \frac{1}{2}\int_0^{\mathrm{arsinh} 2} \cosh^2 t \ dt$$

Applying the identity $\cosh^2 t = \tfrac{1}{2}(1 + \cosh 2t),$ we obtain the [antiderivative](../indefinite-integrals/):

$$\int \cosh^2 t \ dt = \frac{1}{2}t + \frac{1}{4}\sinh 2t + c$$

Evaluating the integral at the limits and using $\sinh 2t = 2\sinh t \cosh t,$ together with the relations $\sinh(\mathrm{arsinh} 2) = 2$ and $\cosh(\mathrm{arsinh} 2) = \sqrt{5},$ we obtain the length of the parabolic arc between the origin and the point $(1, 1)$:

$$L = \frac{1}{4}\mathrm{arsinh} 2 + \frac{\sqrt{5}}{2}$$

## Arc length in parametric form

We next consider a common situation involving curves such as circles, [ellipses](../ellipse/), and spirals, which cannot be described as graphs of a single function because more than one value of $y$ may correspond to a given value of $x.$ For these curves, an auxiliary variable is typically introduced, and the two coordinates of the moving point are expressed as functions of this parameter. This is the parametric description of a curve, which, as we shall see below, coincides with the Cartesian description when the parameter is the $x$-coordinate. Consider, for example, a plane curve described by a parameter $t$ in a closed interval:

$$\begin{cases} x = x(t) \\[6pt] y = y(t) \end{cases} \quad t \in [\alpha, \beta]$$

Suppose that the functions $x(t)$ and $y(t)$ are continuously differentiable on the interval $[\alpha, \beta].$ We apply the polygonal construction described above to a partition of the parameter interval. This gives a chord joining the points associated with two consecutive values $t_{k-1}$ and $t_k,$ whose length, by $(1),$ is given by:

$$\ell_k = \sqrt{[x(t_k) - x(t_{k-1})]^2 + [y(t_k) - y(t_{k-1})]^2}$$

We apply the mean value theorem to $x$ and $y$ and take the limit as the mesh of the partition tends to zero. This gives the arc length formula in parametric form:

$$L = \int_\alpha^\beta \sqrt{[x'(t)]^2 + [y'(t)]^2} \ dt \tag{5}$$

> Recall that a curve generally admits many distinct parametrizations, but its arc length depends only on the geometric image of the portion traversed, provided that the parametrization is regular and [injective](../injective-surjective-and-bijective-functions/).

- - -

We stated that the Cartesian formula is a special case of the parametric formula when we choose the parameter $t = x.$ In this case, the parametrization reduces to:

$$\begin{cases} x(t) = t \\[6pt] y(t) = f(t) \end{cases}$$

We therefore have $x'(t) = 1$ and $y'(t) = f'(t).$ Substituting these expressions into formula $(5)$ gives formula $(3).$ The parametric representation is thus more general and is useful in situations where the Cartesian formulation is not directly applicable.

- - -

As another example, we calculate the length of a [circle](../circumference/) of radius $r$ centered at the origin, this time using the parametric representation:

$$\begin{cases} x(t) = r\cos t \\[6pt] y(t) = r\sin t \end{cases} \quad t \in [0, 2\pi]$$

We begin by calculating the derivatives of the parametric functions:

$$x'(t) = -r\sin t \qquad y'(t) = r\cos t$$

Substituting into the parametric arc length formula and using the [fundamental trigonometric identity](../pythagorean-identity/) $\sin^2 t + \cos^2 t = 1,$ the integrand becomes:

$$\sqrt{[x'(t)]^2 + [y'(t)]^2} = \sqrt{r^2\sin^2 t + r^2\cos^2 t} = r$$

Over the interval $[0, 2\pi],$ we therefore obtain the following integral:

$$L = \int_0^{2\pi} r \ dt = 2\pi r$$

We have thus shown that the circle has length $2\pi r.$

- - -

Next, consider a cycloid generated by a point on a circle of radius $r$ rolling without slipping along a straight line. The standard parametrization of one arch of the cycloid is:

$$\begin{cases} x(t) = r(t - \sin t) \\[6pt] y(t) = r(1 - \cos t) \end{cases} \quad t \in [0, 2\pi]$$

We calculate the derivatives of the parametric components:

$$x'(t) = r(1 - \cos t) \qquad y'(t) = r\sin t$$

Adding the squares of these two components and using the [identities](../trigonometric-identities/) $1 - \cos t = 2\sin^2(t/2)$ and $\sin t = 2\sin(t/2)\cos(t/2),$ we obtain:

$$
\begin{align}
[x'(t)]^2 + [y'(t)]^2 &= r^2(1 - \cos t)^2 + r^2\sin^2 t \\[6pt]
                      &= 2r^2(1 - \cos t)
\end{align}
$$

Applying the half-angle identities, the expression becomes $4r^2\sin^2(t/2),$ whose square root is $2r |\sin(t/2)|.$ Since $t/2 \in [0, \pi]$ over the interval of integration, the sine is nonnegative and we can remove the [absolute value](../absolute-value/). The arc length integral therefore reduces to:

$$L = \int_0^{2\pi} 2r\sin(t/2) \ dt$$

An antiderivative of $\sin(t/2)$ is $-2\cos(t/2),$ and evaluating at the limits gives the length of one arch of the cycloid, which is $8r$:

$$
\begin{align}
L &= 2r\bigl[-2\cos(t/2)\bigr]_0^{2\pi} \\[6pt]
  &= 2r(-2\cos\pi + 2\cos 0) \\[6pt]
  &= 2r(2 + 2) \\[6pt]
  &= 8r
\end{align}
$$

## A brief summary and limits of applicability

We have described how to calculate the length of an arc using the Cartesian and parametric formulations. The formulas to remember are:

[class="table-1"]

|                                             |                                                             |
| ------------------------------------------- | ----------------------------------------------------------- |
| $y = f(x),$ with $x \in [a, b]$              | $$L = \int_a^b \sqrt{1 + [f'(x)]^2} \ dx$$                  |
| $(x(t), y(t)),$ with $t \in [\alpha, \beta]$ | $$L = \int_\alpha^\beta \sqrt{[x'(t)]^2 + [y'(t)]^2} \ dt$$ |

[/class]

The formulas presented so far assume that the derivatives involved exist and are continuous throughout the interval of integration. When this regularity fails at isolated points, the integral can often be interpreted as an [improper integral](../improper-integrals/), and the arc length may still be finite. However, continuous curves of infinite length exist for which the elementary formulas are not applicable, and we turn to the general theory of rectifiable curves (which is beyond the scope of this discussion), where length is defined directly as the [supremum](../supremum-and-infimum/) of the lengths of all inscribed polygonal lines.

To give a brief indication, a curve is said to be rectifiable when this supremum is finite. In general, continuously differentiable curves on a closed bounded interval are rectifiable, and in these cases the supremum coincides with the value calculated using the integral formulas.

The class of rectifiable curves is broader than that of curves of class $C^1,$ that is, curves with a continuous first derivative, and provides the basis for the general formulation of the notion of length.

Finally, recall that when the arc length integral cannot be evaluated in closed form, its value can still be approximated using [numerical integration](../numerical-integration/).
