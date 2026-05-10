
# Finding Areas by Integration

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/finding-areas-by-integration/

## Area between two curves using definite integrals

Building on the concept of [definite integrals](../definite-integrals), which measure the area between a curve and the x-axis, we can extend the same idea to find the area enclosed between two curves. Let \\( f(x) \\) and \\( g(x) \\) be two [continuous](../continuous-functions/) functions defined on the same [interval](../intervals/) \\([a, b]\\), such that \\( f(x) \geq g(x) \\) for every \\( x \in [a, b] \\), and suppose their graphs enclose a region. The area of this region is given by:

\\[
A = \int_a^b [f(x) - g(x)] \\, dx \tag{1}
\\]

> Since both \\( f \\) and \\( g \\) are continuous on \\([a,b]\\), their difference \\( f(x) - g(x) \\) is also continuous on the same interval. A continuous function on a closed and bounded interval is [Riemann-integrable](../riemann-integrability-criteria/). Therefore, the function \\( f(x) - g(x) \\) is integrable on \\([a,b]\\), and the area between the two curves is well defined through a definite integral.

- - -

We want to calculate the area of the gray-shaded region between the curves \\( f(x) \\) and \\( g(x) \\):

![Img. 1](finding-areas-by-integration-1.svg)
Intuitively, we can see that the area \\( A \\) is given by the difference between the area under the curve \\( f(x) \\) and the area under the curve \\( g(x) \\). In other words, formally:

\\[
A = \int_a^b f(x) \\, dx  \\,\\,- \int_a^b g(x) \\, dx
\\]

By the [linearity of the integral](../indefinite-integrals), this becomes equation \\(1\\).

- - -
## Areas between intersecting curves

So far we assumed that \\( f(x) \geq g(x) \\) throughout the entire interval \\( [a, b] \\). In many cases, however, the interval itself is not given: the two curves determine it, and the first step is to find where they meet. To locate the intersection points, set \\( f(x) = g(x) \\) and solve for \\( x \\). The solutions are the limits of integration.

Once the interval is known, the two curves can cross inside it, meaning that \\( f(x) \\) and \\( g(x) \\) swap their relative position at some interior point \\( c \\). When this happens, the integrand \\( f(x) - g(x) \\) changes sign, and a single integral over \\( [a, b] \\) would cause areas above and below the x-axis to cancel out, producing an incorrect result. 

- - -

The correct approach is to split the interval at each crossing point and integrate separately over each subinterval, always subtracting the lower curve from the upper one:

\\[
A = \int_{a}^{c} [f(x) - g(x)] \\, dx + \int_{c}^{b} [g(x) - f(x)] \\, dx
\\]

A compact way to write this without tracking which curve is on top is:

\\[
A = \int_{a}^{b} |f(x) - g(x)| \\, dx
\\]

![Img. 2](finding-areas-by-integration-2.svg)

The [absolute value](../absolute-value/) guarantees that each piece of area is counted as positive, regardless of which [function](../functions/) is larger on that subinterval.

> The formula \\( A = \int_a^b |f(x)-g(x)|\\,dx \\) is valid provided that all intersection points of the two curves are included among the limits of integration. The absolute value ensures that the difference between the two functions is always taken as positive, so that no portion of the enclosed region cancels out when the curves swap their relative position.

- - -
## Example 1

Suppose we want to find the area enclosed between the curves \\(y_1 = e^x\\) and \\(y_2 = x^2 - 1\\) over the interval \\( x \in [-1, 1] \\). Graphically, we have the following situation:

![Img. 3](finding-areas-by-integration-3.svg)

To calculate the area, we use equation \\((1)\\) and set up the following definite integral:

\\[
A = \int_{-1}^{1} \left[ e^x - (x^2 - 1) \right] \\, dx
\\]

- - -

Solving the integral, we obtain:

\\[
\begin{aligned}
A &= \int_{-1}^{1} \left[ e^x - x^2 + 1 \right] \\, dx \\\\
&= \left[ e^x - \frac{x^3}{3} + x \right]\_{-1}^{1} \\\\
&= \left( e - \frac{1}{3} + 1 \right) - \left( e^{-1} + \frac{1}{3} - 1 \right) \\\\
&= e - \frac{1}{e} + \frac{4}{3}
\end{aligned}
\\]

Therefore, the area between the two curves is:

\\[
A = e - \frac{1}{e} + \frac{4}{3}
\\]

- - -
## Example 2

Find the area of the region enclosed between the curves \\(f(x) = x^3 - 3x\\) and \\(g(x) = x
\\). The interval is not given. We start by finding where the two curves intersect, setting \\( f(x) = g(x) \\):

\\[
\begin{aligned}
x^3 - 3x &= x \\\\[6pt]
x^3 - 4x &= 0 \\\\[6pt]
x(x^2 - 4) &= 0
\end{aligned}
\\]

The solutions are \\( x = -2 \\), \\( x = 0 \\), and \\( x = 2 \\). These are the limits of integration.

- - -

Since the curves cross at \\( x = 0 \\), we check which function is on top in each subinterval. Evaluating at \\( x = -1 \\) we obtain:

\\[
\begin{aligned}
f(-1) &= (-1)^3 - 3(-1) = 2 \\\\
g(-1) &= -1
\end{aligned}
\\]

So \\( f(x) \geq g(x) \\) on \\( [-2, 0] \\). By symmetry, \\( g(x) \geq f(x) \\) on \\( [0, 2] \\).

- - -

We now split the integral accordingly:

\\[
A = \int_{-2}^{0} [f(x) - g(x)] \\, dx + \int_{0}^{2} [g(x) - f(x)] \\, dx
\\]

\\[
A = \int_{-2}^{0} (x^3 - 4x) \\, dx + \int_{0}^{2} (4x - x^3) \\, dx
\\]

- - -

Computing the first integral, we have:

\\[
\begin{aligned}
\int_{-2}^{0} (x^3 - 4x) \\, dx &= \left[ \frac{x^4}{4} - 2x^2 \right]_{-2}^{0} \\\\
&= \left(0\right) - \left(\frac{16}{4} - 2 \cdot 4\right) \\\\
&= 0 - (4 - 8) \\\\
&= 4
\end{aligned}
\\]

Computing the second integral, we obtain:

\\[
\begin{aligned}
\int_{0}^{2} (4x - x^3) \\, dx &= \left[ 2x^2 - \frac{x^4}{4} \right]\_{0}^{2} \\\\
&= \left(2 \cdot 4 - \frac{16}{4}\right) - 0 \\\\
&= 8 - 4 \\\\
&= 4
\end{aligned}
\\]

The total area is:

\\[
A = 4 + 4 = 8
\\]

The symmetry of the result is not a coincidence: \\( f(x) = x^3 - 3x \\) is an [odd function](../even-and-odd-functions/), and the two regions are mirror images of each other across the origin.

- - -
## Flowchart

- `Area to compute`
  - **IF** the interval \\([a, b]\\) is given and \\( f(x) \geq g(x) \\) throughout
    - _apply the standard formula directly_
      \\[A = \int_a^b [f(x) - g(x)] \, dx\\]
    - _evaluate and stop_
  - `ELSE IF` the interval is not given
    - _find the intersection points_
      set \\( f(x) = g(x) \\) and solve for \\( x \\); the solutions are the limits of integration
    - _check which curve is on top_
      evaluate \\( f(x) - g(x) \\) at a test point in each subinterval
    - **IF** the curves do not cross inside the interval
      - _integrate directly_
        \\[A = \int_a^b [f(x) - g(x)] \, dx\\]
      - _evaluate and stop_
    - `ELSE`
      - _split at each crossing point \\( c \\)_
        \\[A = \int_a^c [f(x) - g(x)] \, dx + \int_c^b [g(x) - f(x)] \, dx\\]
      - _evaluate each piece and sum_
  - `ELSE IF` the interval is given but the curves cross inside it
    - _locate all interior crossing points_
      solve \\( f(x) = g(x) \\) restricted to \\((a, b)\\)
    - _split and integrate over each subinterval_
      always subtract the lower curve from the upper one on each piece
    - _sum the results_