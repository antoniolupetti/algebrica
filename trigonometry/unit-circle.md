# Unit Circle

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/unit-circle/

## Definition

The unit circle (or the trigonometric circle) is a circle of radius one centered at the origin of the Cartesian plane. It serves as the geometric reference for representing angles and their positions, providing a precise way to describe rotation, orientation, and the relationship between points on the circle as an angle varies. In formal terms, consider a circle of unit radius centered at the origin \\( O \\), and let \\( P \\) be a point on the circle. The segment \\( \overline{OP} \\), which has length one, forms an angle \\( \theta \\) with the positive \\( x \\)-axis, and \\( R \\) denotes the foot of the perpendicular dropped from \\( P \\) to the \\( x \\)-axis.

By convention, the counterclockwise direction is assigned a positive sign and the clockwise direction a negative sign. The angle \\( \theta \\) is therefore positive when \\( P \\) is reached by moving counterclockwise from the positive \\( x \\)-axis, and negative otherwise. 

Let \\( S \\) be the point \\( (1, 0) \\) where the unit circle meets the positive \\( x \\)-axis, and let \\( T \\) be the point where the line through \\( O \\) and \\( P \\) intersects the vertical tangent to the circle at \\( S \\).

- The length of the vertical segment \\( \overline{PR} \\) equals the [sine](../sine-and-cosine) of the angle \\( \theta \\).
- The length of the horizontal segment \\( \overline{OR} \\) equals the [cosine](../sine-and-cosine) of the angle \\( \theta \\).
- The length of the vertical segment \\( \overline{ST} \\) equals the [tangent](../tangent-and-cotangent) of the angle \\( \theta \\).

- - -
## Fundamental trigonometric identity

Once the notions of [sine and cosine](../sine-and-cosine/) are introduced through the geometry of the unit circle, their relationship becomes obvious. If a point \\( P \\) lies on the unit circle and the segment \\( \overline{OP} \\) forms an angle \\( \theta \\) with the positive \\( x \\)-axis, the right triangle with vertices at \\( O \\), \\( R \\), and \\( P \\) has hypotenuse of length \\( 1 \\), horizontal leg of length \\( \cos\theta \\), and vertical leg of length \\( \sin\theta \\). Applying the [Pythagorean theorem](../pythagorean-theorem/) to this triangle gives the following identity:

\\[
\sin^2\theta + \cos^2\theta = 1
\\]

This relation holds for every angle \\( \theta \\), regardless of the position of \\( P \\) on the circle. In analytic terms, it expresses the fact that the point \\( (\cos\theta, \sin\theta) \\) always lies on the unit circle, whose equation is the following:

\\[
x^{2} + y^{2} = 1
\\]

Reversing the perspective, every point on the unit circle can be written in the form \\( (\cos\theta, \sin\theta) \\) for some angle \\( \theta \\), which is the parametric representation of the circle.

-  - -
## Angles on the unit circle

Consider a point \\( P \\) on the unit circle. Its position is uniquely identified by the angle \\( \theta \\) formed between the positive \\( x \\)-axis and the segment \\( \overline{OP} \\), where \\( O \\) denotes the origin. The angle is measured counterclockwise from the positive \\( x \\)-axis, following the standard convention.

Angles are typically expressed in degrees according to the sexagesimal system, in which a complete revolution corresponds to \\( 360^\circ \\). Since the circle is a closed curve, rotating by \\( 360^\circ \\) returns the point \\( P \\) to its original position, so angles are naturally defined modulo \\( 360^\circ \\). As a result, values exceeding \\( 360^\circ \\) represent rotations involving one or more full turns, while negative values indicate clockwise rotation. For instance:

- \\( 450^\circ \\) represents one full turn (\\( 360^\circ \\)) plus an additional \\( 90^\circ \\).
- \\( -90^\circ \\) corresponds to a quarter-turn in the clockwise direction.

- - -
## Arc length and radians

Let \\( A \\) be the point where the positive \\( x \\)-axis intersects the unit circle, and let \\( P \\) be any point on the unit circle. The point \\( P \\) can be uniquely identified by the length of the arc from \\( A \\) to \\( P \\), measured counterclockwise along the unit circle.

The maximum length of such an arc, corresponding to a full turn, is \\( 2\pi \\). As in the case of degrees, arc lengths greater than \\( 2\pi \\) represent multiple full rotations, while negative values correspond to clockwise movement.

This arc length is called the radian measure of the angle \\( \angle AOP \\), and, because rotations are periodic, it is defined modulo \\( 2\pi \\). To convert an angle from degrees to radians, one multiplies its degree measure by the factor \\( \pi/180 \\). For example, the angle \\( \theta = 30^\circ \\) corresponds to the following radian measure.
\\[
\theta = 30 \times \frac{\pi}{180} = \frac{\pi}{6}
\\]

- - -
## Cartesian coordinates and parametric representation

The unit circle admits a natural parametric representation in the Cartesian coordinate system. Any point \\( P \\) on the circle is uniquely determined by the angle \\( \theta \\) formed between the positive \\( x \\)-axis and the segment \\( \overline{OP} \\). As \\( \theta \\) ranges over \\( [0, 2\pi) \\), the point \\( P \\) traces the circle exactly once, and the correspondence is expressed by the following parametric equations.
\\[
\begin{align}
x &= \cos\theta \\\\[6pt]
y &= \sin\theta \\\\[6pt]
\end{align}
\\]
When \\( \theta \\) is allowed to range over all of \\( \mathbb{R} \\), the same point may be reached multiple times, reflecting the periodicity of the trigonometric functions. Substituting the parametric expressions into the equation \\( x^2 + y^2 = 1 \\) recovers the [fundamental trigonometric identity](../pythagorean-identity/) \\( \sin^2\theta + \cos^2\theta = 1 \\), confirming that every point of this form lies on the unit circle.

As an example, consider the angle \\( \theta = \pi/3 \\). The [parametric equations](../equations-with-parameters/) give the following values.

\\[\cos\frac{\pi}{3} = \frac{1}{2}\\] 
\\[\sin\frac{\pi}{3} = \frac{\sqrt{3}}{2}\\]

The corresponding point on the unit circle is therefore:
\\[ P\\!\left(\frac{1}{2},\\, \frac{\sqrt{3}}{2}\right) \\]

One may verify directly that:

\\[ \left(\frac{1}{2}\right)^2 + \left(\frac{\sqrt{3}}{2}\right)^2 = \frac{1}{4} + \frac{3}{4} = 1 \\]

- - -
## Periodic nature of the parametrization

The parametric representation of the unit circle reflects a fundamental property of the 
trigonometric functions: since the circle is a closed curve, completing a full rotation of 
\\( 2\pi \\) radians returns the point \\( P \\) to its original position. As a consequence, 
adding any integer multiple of \\( 2\pi \\) to the angle \\( \theta \\) leaves the 
corresponding point on the circle unchanged. This is expressed by the following identity:

\\[
(\cos(\theta + 2k\pi),\\, \sin(\theta + 2k\pi)) = (\cos\theta,\\, \sin\theta)
\\]

for every integer \\( k \in \mathbb{Z} \\). In particular, this means that the parametrization by \\( \theta \in \mathbb{R} \\) is not injective: infinitely many values of \\( \theta \\)  correspond to the same point on the circle, and a bijective correspondence is recovered only by restricting \\( \theta \\) to an interval of length \\( 2\pi \\), such as \\( [0, 2\pi) \\).
 
This periodic behaviour is a defining property of the [sine and cosine](../sine-and-cosine/), which inherit it directly from the geometry of the unit circle.

- - -
## Notable angles and their coordinates

Some angles appear frequently in trigonometry. At these values of \\(\theta\\), sine and cosine can be calculated through elementary geometric arguments, with no need for numerical approximation. The table below lists the corresponding coordinates \\((\cos\theta, \sin\theta)\\) for the most common angles.

\\[
\begin{align}
\theta &= 0 &\quad& \cos 0 = 1 &\quad& \sin 0 = 0 \\\\[6pt]
\theta &= \frac{\pi}{6} &\quad& \cos\frac{\pi}{6} = \frac{\sqrt{3}}{2} &\quad& \sin\frac{\pi}{6} = \frac{1}{2} \\\\[6pt]
\theta &= \frac{\pi}{4} &\quad& \cos\frac{\pi}{4} = \frac{\sqrt{2}}{2} &\quad& \sin\frac{\pi}{4} = \frac{\sqrt{2}}{2} \\\\[6pt]
\theta &= \frac{\pi}{3} &\quad& \cos\frac{\pi}{3} = \frac{1}{2} &\quad& \sin\frac{\pi}{3} = \frac{\sqrt{3}}{2} \\\\[6pt]
\theta &= \frac{\pi}{2} &\quad& \cos\frac{\pi}{2} = 0 &\quad& \sin\frac{\pi}{2} = 1 \\\\[6pt]
\theta &= \pi &\quad& \cos\pi = -1 &\quad& \sin\pi = 0 \\\\[6pt]
\theta &= \frac{3\pi}{2} &\quad& \cos\frac{3\pi}{2} = 0 &\quad& \sin\frac{3\pi}{2} = -1
\end{align}
\\]

The values at \\(\theta = \pi/4\\) follow from a single observation: an isosceles right triangle inscribed in the unit circle has equal legs, so that \\( \cos(\pi/4) = \sin(\pi/4) = \sqrt{2}/2 .\\] The values at \\(\theta = \pi/6\\) and \\(\theta = \pi/3\\) come instead from the geometry of the equilateral triangle, whose interior angles all equal \\(\pi/3\\).

- - -
## The unit circle and complex numbers

The unit circle admits a natural interpretation in the context of complex numbers. Recall that a [complex number](../complex-numbers/) \\( z = x + iy \\) can be represented as a point \\( (x, y) \\) in the Cartesian plane. The modulus of \\( z \\) is defined as \\( |z| = \sqrt{x^2 + y^2} \\), so the condition \\( |z| = 1 \\) describes precisely the set of complex numbers lying on the unit circle. By the parametric representation established above, every such number can be written in the form:

 \\[ z = \cos\theta + i\sin\theta \\]

for some angle \\( \theta \\). This expression coincides with the [exponential form of a complex number](../complex-numbers-exponential-form/), given by Euler's formula:

\\[
e^{i\theta} = \cos\theta + i\sin\theta
\\]

The unit circle is therefore the set of all complex numbers of the form \\( e^{i\theta} \\) 
as \\( \theta \\) ranges over \\( \mathbb{R} \\), or equivalently the set 
\\( \{z \in \mathbb{C} : |z| = 1\} \\). Multiplication of two such numbers corresponds 
geometrically to a rotation: if \\( z_1 = e^{i\alpha} \\) and \\( z_2 = e^{i\beta} \\), 
then \\( z_1 z_2 = e^{i(\alpha+\beta)} \\), which is the point obtained by rotating 
\\( z_1 \\) by the angle \\( \beta \\). This geometric interpretation underlies both 
[De Moivre's theorem](../de-moivre-theorem/) and the study of the [roots of unity](../roots-of-unity/).