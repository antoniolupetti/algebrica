# Right Triangle Trigonometry

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/right-triangle-trigonometry/

## Understanding the sides of a right triangle

Trigonometry studies the relationships between angles and sides of triangles, and the right triangle is where the basic trigonometric functions are usually introduced: [sine](../sine-and-cosine/), [cosine](../sine-and-cosine/), and [tangent](../tangent-and-cotangent/). A right triangle has one interior angle of exactly \\(90^\circ.\\) The two sides meeting at the right angle are the legs, and the third side, opposite the right angle, is the hypotenuse, which is always the longest of the three. Fix an acute angle \\(\theta\\) inside the triangle. The hypotenuse does not depend on the choice of \\(\theta\\), but the two legs do: one lies opposite to \\(\theta\\), the other borders it. The trigonometric functions arise precisely from this asymmetry, as ratios between pairs of sides.

- Hypotenuse \\(h\\): the longest side, opposite the right angle.
- Opposite leg \\(y\\): the leg opposite to \\(\theta\\).
- Adjacent leg \\(x\\): the leg that bounds \\(\theta\\) together with the hypotenuse.

A key observation is that these ratios depend only on \\(\theta\\), not on the size of the triangle. If we scale a right triangle by any factor, all three sides grow by the same amount, so the ratio between any two of them stays the same. Two right triangles sharing the acute angle \\(\theta\\) are therefore similar, and their corresponding ratios coincide. The trigonometric functions are for this reason well defined as functions of the angle alone.

- - -
## SOH-CAH-TOA method

Place a right triangle inside a [unit circle](../unit-circle/), with the acute angle \\(\theta\\) at the origin of the Cartesian coordinate system and the hypotenuse running from the origin to a point on the circle. In this configuration the hypotenuse has length \\(h = 1\\), and the two legs coincide with the horizontal and vertical coordinates of that point. The ratios that define the trigonometric functions take an especially transparen form here, because dividing by \\(h = 1\\) leaves the coordinates themselves as the values of sine and cosine.

The name SOH-CAH-TOA is a mnemonic that encodes the three primary trigonometric functions as ratios of sides: [sine](../sine-and-cosine/) is Opposite over Hypotenuse, [cosine](../sine-and-cosine/) is Adjacent over Hypotenuse, and [tangent](../tangent-and-cotangent/) is Opposite over Adjacent. Reading each triple from left to right gives the function on the left and the two sides forming the ratio on the right. The three reciprocal functions, [cosecant](../secant-and-cosecant/), [secant](../secant-and-cosecant/), and [cotangent](../tangent-and-cotangent/), follow by inverting each ratio.

The SOH group gives the sine of the angle and its reciprocal, the cosecant:

\\[
\begin{align}
\sin(\theta) &= \frac{y}{h} \\\\[6pt]
\csc(\theta) &= \frac{h}{y}
\end{align}
\\]

> Rearranging the SOH relation gives \\(y = h \sin(\theta)\\), which returns the length of the opposite leg whenever the angle and the hypotenuse are known. The CAH and TOA relations can be rearranged in the same way to recover any missing side from the other two pieces of information.

- - -

The CAH group gives the cosine and its reciprocal, the secant:

\\[
\begin{align}
\cos(\theta) &= \frac{x}{h} \\\\[6pt]
\sec(\theta) &= \frac{h}{x}
\end{align}
\\]

The TOA group gives the tangent and its reciprocal, the cotangent:

\\[
\begin{align}
\tan(\theta) &= \frac{y}{x} \\\\[6pt]
\cot(\theta) &= \frac{x}{y}
\end{align}
\\]

The tangent can also be written directly in terms of sine and cosine, since \\(y/x = (y/h)/(x/h)\\). This gives the identity \\(\tan(\theta) = \sin(\theta)/\cos(\theta)\\), and by reciprocation \\(\cot(\theta) = \cos(\theta)/\sin(\theta)\\). The six trigonometric functions are therefore not independent of each other: sine and cosine alone determine all of them.

- - -
## The Pythagorean identity

The sine and cosine of the same angle are not independent quantities: they satisfy the [Pythagorean identity](../pythagorean-identity/), which in any right triangle with acute angle \\(\theta\\) takes the form:

\\[
\sin^2(\theta) + \cos^2(\theta) = 1
\\]

The identity is a direct consequence of the [Pythagorean theorem](../pythagorean-theorem/). Starting from \\(x^2 + y^2 = h^2\\) and dividing both sides by \\(h^2\\), the equation becomes:

\\[
\left(\frac{y}{h}\right)^2 + \left(\frac{x}{h}\right)^2 = 1
\\]

The two ratios on the left coincide with \\(\sin(\theta)\\) and \\(\cos(\theta)\\) by the SOH and CAH relations, which gives the identity in its standard form. The same conclusion follows geometrically from the [unit circle](../unit-circle/). A point on the circle has coordinates \\((\cos(\theta), \sin(\theta))\\), and the equation of the circle, \\(x^2 + y^2 =1\\), is exactly the [Pythagorean identity](../pythagorean-identity/) rewritten in those coordinates.

- - -
## Solving a right triangle

A right triangle is fully determined by any two of its elements beyond the right angle itself, provided that at least one of the two is a side. The right angle fixes the shape up to similarity, and knowing one side sets the overall scale, so the remaining elements follow from SOH-CAH-TOA together with the Pythagorean identity. Three configurations cover all practical cases.

- Two sides are known. The third side follows from the Pythagorean theorem, and the two acute angles follow from any of the SOH-CAH-TOA ratios.
- One side and one acute angle are known. The other two sides follow from SOH-CAH-TOA, and the second acute angle is the complement \\(90^\circ - \theta\\).
- Two angles are known. The triangle is determined only up to similarity, and an additional piece of information, typically the length of one side, is needed to fix its size.

The configuration with one side and one acute angle is the most common in applications, since in problems involving heights, distances, and slopes the angle is usually measured directly and one length is known from the setting. The example below illustrates this case.

- - -
## Example

Consider a right triangle in which the leg opposite to the acute angle \\(\theta = 30^\circ\\) measures \\(y = 5\\), and suppose we want to determine the length of the adjacent leg \\(x\\).

The two legs and the angle \\(\theta\\) are linked by the TOA relation, which expresses the tangent of the angle as the ratio between the opposite and the adjacent leg:

\\[
\tan(\theta) = \frac{y}{x}
\\]

Substituting the known values, the equation becomes:

\\[
\tan(30^\circ) = \frac{5}{x}
\\]

Since the unknown \\(x\\) appears in the denominator, we multiply both sides by \\(x\\) to bring it to the numerator, and then divide by \\(\tan(30^\circ)\\) to isolate it on the left:

\\[
x = \frac{5}{\tan(30^\circ)}
\\]

The tangent of \\(30^\circ\\) is equal to \\(1/\sqrt{3}\\), so the expression simplifies to \\(x = 5\sqrt{3}\\), which is approximately \\(8.66\\). The adjacent leg therefore measures about \\(8.66\\) units.

