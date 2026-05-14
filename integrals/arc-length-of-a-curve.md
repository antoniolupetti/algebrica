
# Arc Length of a Curve

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/arc-length-of-a-curve/

## From straight segments to curved arcs

The notion of length is immediate for a straight segment, since two points in the plane determine a single line and the Euclidean distance provides an unambiguous measurement. When the path between two points is not straight but follows the graph of a function, the same intuitive idea of measuring a physical thread laid along the curve must be turned into a precise analytical definition. The construction that achieves this goal is the same that underlies the [definite integral](../definite-integrals/): one approximates the curve by simpler objects whose length is already known, and then refines the approximation by a limiting procedure.

Consider a function \\( f(x) \\) defined and [continuously differentiable](../continuous-functions/) on a closed interval \\([a,b]\\). The arc of the graph between the points of abscissa \\( a \\) and \\( b \\) is a curve in the plane, and the question is how to attach to it a real number that quantifies its length. The procedure we will follow consists in inscribing a polygonal line in the curve, computing the length of this polygonal line, and then refining the construction by adding vertices whose spacing tends to zero.

- - -

## Polygonal approximation and the differential element

Let \\( P = \\{x_0, x_1, \dots, x_n\\} \\) be a [partition](../riemann-integrability-criteria/) of the interval \\([a,b]\\) with

\\[
a = x_0 < x_1 < \cdots < x_n = b
\\]

To each subdivision point we associate the point \\( (x_k, f(x_k)) \\) on the graph of the function. Joining consecutive points by straight segments produces a polygonal line inscribed in the curve, and its total length is the sum of the Euclidean distances between consecutive vertices. The length of the \\( k \\)-th segment is given by:

\\[
\ell_k = \sqrt{(x_k - x_{k-1})^2 + (f(x_k) - f(x_{k-1}))^2}
\\]

Since \\( f \\) is differentiable on \\([x_{k-1}, x_k]\\), the [mean value theorem](../definite-integrals/) guarantees the existence of a point \\( \xi_k \\) in the open interval \\( (x_{k-1}, x_k) \\) such that:

\\[
f(x_k) - f(x_{k-1}) = f'(\xi_k)\\,(x_k - x_{k-1})
\\]

Substituting this identity into the expression for \\( \ell_k \\) and factoring \\( (x_k - x_{k-1})^2 \\) under the radical, we obtain:

\\[
\ell_k = \sqrt{1 + [f'(\xi_k)]^2}\\,(x_k - x_{k-1})
\\]

The total length of the inscribed polygonal line therefore equals a [Riemann sum](../definite-integrals/) of the function \\( \sqrt{1 + [f'(x)]^2} \\) on the partition \\( P \\). When the mesh of the partition tends to zero, this Riemann sum converges to a definite integral, provided that the integrand is itself Riemann-integrable.

- - -
## Arc length in Cartesian form

The construction above leads to the fundamental definition for curves expressed as graphs of functions in the Cartesian plane. Let \\( f \\) be a function with continuous [derivative](../derivatives/) on the closed [interval](../intervals/) \\([a,b]\\). The arc length of the graph of \\( f \\) from \\( x = a \\) to \\( x = b \\) is defined by:

\\[
L = \int_a^b \sqrt{1 + [f'(x)]^2}\\, dx \tag{1}
\\]

The hypothesis that \\( f' \\) be continuous on \\([a,b]\\) is essential, because it ensures the continuity of the integrand and therefore its [Riemann integrability](../riemann-integrability-criteria/). A function whose derivative is merely bounded but not continuous may still admit a well-defined arc length, but the elementary proof presented above no longer applies, and the discussion requires the more general framework of rectifiable curves.

> The expression \\( \sqrt{1 + [f'(x)]^2}\\, dx \\) is called the arc length element, and it is usually denoted by \\( ds \\). It represents the infinitesimal length of the curve associated with an infinitesimal increment \\( dx \\) of the independent variable, and it satisfies the identity \\( ds^2 = dx^2 + dy^2 \\), which is nothing more than the Pythagorean theorem applied to the infinitesimal triangle of legs \\( dx \\) and \\( dy = f'(x)\\, dx \\).


- - -
## Example 1

We compute the length of the parabolic arc described by the function \\( f(x) = x^2 \\) on the interval \\([0, 1]\\). The derivative of the function is given by:

\\[
f'(x) = 2x
\\]

Substituting into formula \\((1)\\), the arc length is expressed as:

\\[
L = \int_0^1 \sqrt{1 + 4x^2}\\, dx
\\]

The integrand has the structure \\( \sqrt{1 + (2x)^2} \\) and this form invites the hyperbolic substitution \\( 2x = \sinh t \\). The differential is transformed as follows:

\\[
2\\, dx = \cosh t\\, dt
\\]

so that \\( dx = \tfrac{1}{2}\cosh t\\, dt \\). Moreover, using the hyperbolic identity \\( 1 + \sinh^2 t = \cosh^2 t \\), the radical simplifies to \\( \cosh t \\). The integral therefore becomes:

\\[
L = \int_0^{\operatorname{arsinh} 2} \cosh t \cdot \frac{1}{2}\cosh t\\, dt = \frac{1}{2}\int_0^{\operatorname{arsinh} 2} \cosh^2 t\\, dt
\\]

Applying the standard identity \\( \cosh^2 t = \frac{1}{2}(1 + \cosh 2t) \\), the antiderivative is obtained as:

\\[
\int \cosh^2 t\\, dt = \frac{1}{2}t + \frac{1}{4}\sinh 2t + c
\\]

Evaluating at the limits and using \\( \sinh 2t = 2\sinh t \cosh t \\) together with \\( \sinh(\operatorname{arsinh} 2) = 2 \\) and \\( \cosh(\operatorname{arsinh} 2) = \sqrt{5} \\), we arrive at the closed-form result:

\\[
L = \frac{1}{4}\operatorname{arsinh} 2 + \frac{\sqrt{5}}{2}
\\]

The length of the parabolic arc between the origin and the point \\( (1,1) \\) is therefore equal to \\( \tfrac{\sqrt{5}}{2} + \tfrac{1}{4}\ln(2 + \sqrt{5}) \\), since the inverse hyperbolic sine admits the logarithmic representation \\( \operatorname{arsinh} u = \ln(u + \sqrt{1+u^2}) \\).

- - -

## Arc length in parametric form

Several curves that occur in geometry and in physics, among which circles, ellipses, cycloids, and spirals, cannot be written as graphs of a single-valued function. For curves of this kind one introduces an auxiliary variable, called the parameter, and describes the two coordinates of the moving point as functions of it. The point then traces out the curve as the parameter varies over a real interval, and the Cartesian description is recovered as the particular case in which the parameter coincides with the abscissa. Consider a planar curve parametrised by:

\\[
\begin{cases} x = x(t) \\\\[6pt] y = y(t) \end{cases} \quad t \in [\alpha, \beta]
\\]

where \\( x(t) \\) and \\( y(t) \\) are continuously differentiable functions on the interval \\([\alpha, \beta]\\). Repeating the polygonal approximation construction with respect to a partition of the parameter interval, the chord joining the points associated with consecutive parameter values \\( t_{k-1} \\) and \\( t_k \\) has length:

\\[
\ell_k = \sqrt{[x(t_k) - x(t_{k-1})]^2 + [y(t_k) - y(t_{k-1})]^2}
\\]

Applying the mean value theorem separately to \\( x \\) and \\( y \\), and passing to the limit as the mesh of the partition tends to zero, one obtains the parametric arc length formula:

\\[
L = \int_\alpha^\beta \sqrt{[x'(t)]^2 + [y'(t)]^2}\\, dt \tag{2}
\\]

Under the square root one recognises the squared modulus of the velocity vector associated with the parametrisation, and this observation suggests a kinematic reading of the formula. If the parameter \\( t \\) is interpreted as time, the quantity \\( \sqrt{[x'(t)]^2 + [y'(t)]^2} \\) is the instantaneous speed of a point moving along the curve, and integrating it over the time interval yields the distance covered.

> A curve admits in general many distinct parametrisations, but the arc length depends only on the geometric image of the curve and on the interval over which it is traversed, provided that the parametrisation is regular and injective. This invariance under reparametrisation is a fundamental property and reflects the intrinsic geometric nature of length.

- - -
## Relation between the two formulations

The Cartesian formula is a special case of the parametric one. Choosing the parameter \\( t = x \\), the parametrisation reduces to:

\\[
\begin{cases} x(t) = t \\\\[6pt] y(t) = f(t) \end{cases}
\\]

so that \\( x'(t) = 1 \\) and \\( y'(t) = f'(t) \\). Substituting these expressions into formula \\((2)\\) immediately yields formula \\((1)\\). The parametric representation is therefore strictly more general, and it remains applicable when the curve possesses vertical tangents or self-intersections, situations in which the Cartesian formulation breaks down.

- - -
## Example 2

We compute the circumference of a circle of radius \\( r \\) centred at the origin, using the parametric representation:

\\[
\begin{cases} x(t) = r\cos t \\\\[6pt] y(t) = r\sin t \end{cases} \quad t \in [0, 2\pi]
\\]

The derivatives of the parametric functions are given by:

\\[x'(t) = -r\sin t\\] 
\\[ y'(t) = r\cos t\\]

Substituting into the parametric arc length formula and using the fundamental trigonometric identity \\( \sin^2 t + \cos^2 t = 1 \\), the integrand simplifies considerably:

\\[
\sqrt{[x'(t)]^2 + [y'(t)]^2} = \sqrt{r^2\sin^2 t + r^2\cos^2 t} = r
\\]

The integral therefore reduces to the computation of a constant function over the interval \\([0, 2\pi]\\), and the result is obtained immediately:

\\[
L = \int_0^{2\pi} r\\, dt = 2\pi r
\\]

> The parametric formula reproduces the expression for the circumference of a circle, and this agreement is a useful coherence check for the construction we have built.

- - -
## Example 3

Consider the cycloid generated by a point on the rim of a circle of radius \\( r \\) rolling without slipping along a straight line. The standard parametrisation of one full arch of the cycloid is given by:

\\[
\begin{cases} x(t) = r(t - \sin t) \\\\[6pt] y(t) = r(1 - \cos t) \end{cases} \quad t \in [0, 2\pi]
\\]

The derivatives of the parametric components are:

\\[x'(t) = r(1 - \cos t)\\] 
\\[ y'(t) = r\sin t\\]

Adding the squares of these two components and using the identities \\( 1 - \cos t = 2\sin^2(t/2) \\) and \\( \sin t = 2\sin(t/2)\cos(t/2) \\), the integrand can be reduced to a much simpler expression. A direct computation gives:

\\[
\begin{align}
[x'(t)]^2 + [y'(t)]^2
&= r^2(1 - \cos t)^2 + r^2\sin^2 t \\\\[6pt]
&= 2r^2(1 - \cos t)
\end{align}
\\]

Applying the half-angle identity once more, the expression becomes \\( 4r^2\sin^2(t/2) \\), and the square root yields \\( 2r\\,|\sin(t/2)| \\). Since \\( t/2 \\in [0, \pi] \\) over the interval of integration, the sine is non-negative and the absolute value can be removed. The arc length integral therefore reduces to:

\\[
L = \int_0^{2\pi} 2r\sin(t/2)\\, dt
\\]

The antiderivative of \\( \sin(t/2) \\) is \\( -2\cos(t/2) \\), and evaluating at the limits gives:

\\[
\begin{align}
L
&= 2r\bigl[-2\cos(t/2)\bigr]_0^{2\pi} \\\\[6pt]
&= 2r\bigl(-2\cos\pi + 2\cos 0\bigr) \\\\[6pt]
&= 2r(2 + 2) \\\\[6pt]
&= 8r
\end{align}
\\]

The length of a full arch of the cycloid is therefore equal to eight times the radius of the rolling circle. The result was established by Christopher Wren in 1658 and deserves attention for two reasons: the length is an integer multiple of the radius, and a transcendental curve produces here a perfectly algebraic value.

- - -
## Conditions and limitations

The formulas obtained above rest on the assumption that the relevant derivatives exist and are continuous throughout the interval of integration. If this regularity fails at isolated points, the integral can often be interpreted as an [improper integral](../improper-integrals/), and the arc length still turns out to be finite. There exist, on the other hand, continuous curves whose length is infinite; the classical examples come from fractal geometry, the Koch snowflake being the most familiar. For curves of this kind the elementary formulas lose their meaning, and one falls back on the general theory of rectifiable curves, where the length is defined directly as the supremum of the lengths of all inscribed polygonal lines.

> A curve is said to be rectifiable when this supremum is finite. Continuously differentiable curves on a closed bounded interval are rectifiable, and for them the supremum reduces to the value computed by the integral formulas. The class of rectifiable curves is strictly larger than that of curves of class \\( C^1 \\), and provides the proper setting for the most general formulation of the notion of length.

