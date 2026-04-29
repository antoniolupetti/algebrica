# Complex Numbers in Trigonometric Form

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/complex-numbers-trigonometric-form/

## Definition

The [algebraic form](../complex-numbers-introduction) \\( z = a + bi \\) represents a complex number through its real and imaginary components directly. Every nonzero complex number can also be described by two geometric quantities, its distance from the origin and its angular position in the complex plane. This leads to the trigonometric form of a complex number:

\\[z = r (\cos\theta + i\sin\theta)\\]

- \\( r = |z| = \sqrt{a^2 + b^2} \\) is the modulus, representing the distance of \\( z \\) from the origin in the complex plane.
- \\( \theta = \arg(z) \\) is the argument, the angle in radians between the positive real axis and the [vector](../vectors/) representing \\( z \\).

Since the point \\( z = (a, b) \\) lies in the complex plane at distance \\( r \\) from the origin, and \\( \theta \\) is the angle it forms with the positive real axis, the real and imaginary components can be expressed through the definitions of [sine](../sine-and-cosine) and [cosine](../sine-and-cosine) in a right triangle. The projections onto the two axes are the following.

\\[\overline{OA} = \overline{OP} \cdot \cos(\theta) = r \cos(\theta)\\]
\\[\overline{OB} = \overline{OP} \cdot \sin(\theta) = r \sin(\theta)\\]

That is, \\( a = r\cos(\theta) \\) and \\( b = r\sin(\theta) \\). Substituting these into the algebraic form of a complex number yields its trigonometric representation.

\\[
\begin{align}
z = (a, b) &= a + ib \\\\[6pt]
           &= r \cos(\theta) + i r \sin(\theta) \\\\[6pt]
           &= r [\cos(\theta) + i \sin(\theta)] \\\\[6pt]
\end{align}
\\]

---

The complex conjugate \\( \bar{z} \\) of a complex number \\( z \\) in trigonometric form is obtained by replacing \\( \theta \\) with \\( -\theta \\), which corresponds geometrically to reflecting \\( z \\) across the real axis. Since cosine is an even function and sine is odd, the result takes the following form.

\\[\bar{z} = r (\cos\theta - i\sin\theta)\\]

> See also how to express a complex number in its [exponential form](../complex-numbers-exponential-form).

- - -
## Operations

Given two complex numbers in trigonometric form:

\\[z_1 = r_1 [\cos(\theta_1) + i \sin(\theta_1)]\\]
\\[z_2 = r_2 [\cos(\theta_2) + i \sin(\theta_2)]\\]

their product is another complex number whose modulus is the product of the moduli and whose argument is the sum of the arguments. The multiplication formula is the following.

\\[z_1 z_2 = r_1 r_2 [\cos(\theta_1 + \theta_2) + i \sin(\theta_1 + \theta_2)]\\]

Geometrically, [multiplying two complex numbers](../complex-number-operations/) corresponds to scaling their distances from the origin by the product of their moduli and rotating the result by the sum of their arguments, combining a dilation and a rotation in a single operation. 

> This interpretation extends naturally to integer powers through [De Moivre's theorem](../de-moivre-theorem/).

---

The quotient of two complex numbers in trigonometric form, defined for \\( z_2 \neq 0 \\), follows a symmetric rule: the modulus of the result is the ratio of the moduli, and the argument is the difference of the arguments.

\\[\frac{z_1}{z_2} = \frac{r_1}{r_2} \left[ \cos(\theta_1 - \theta_2) + i\sin(\theta_1 - \theta_2) \right]\\]

---

Addition does not admit a comparably compact formula. The most direct approach is to convert both numbers to algebraic form, add their real and imaginary parts separately, and then convert the result back to trigonometric form if needed. The real and imaginary parts of the sum are the following.

\\[x = r_1\cos\theta_1 + r_2\cos\theta_2\\]
\\[y = r_1\sin\theta_1 + r_2\sin\theta_2\\]

The sum \\( z_1 + z_2 \\) is then expressed in algebraic form as \\( x + iy \\). To recover the trigonometric form, one computes the modulus and the argument of the result. The modulus is given by the following.

\\[r = \sqrt{x^2 + y^2}\\]

The argument requires attention to the quadrant of the point \\( (x, y) \\) in the complex plane. When \\( x > 0 \\), one has the following.

\\[\theta = \arctan\\!\left(\frac{y}{x}\right)\\]

When \\( x < 0 \\), a correction of \\( \pm\pi \\) must be applied depending on the sign of \\( y \\), and when \\( x = 0 \\) the argument is \\( \pm\pi/2 \\) according to the sign of \\( y \\).

- - -
## Modulus and argument

The modulus \\( r \\) of a complex number represents its distance from the origin in the complex plane. It is computed via the [Pythagorean theorem](../pythagorean-theorem/) applied to the real and imaginary components, and its value is always non-negative.

\\[r = |z| = \sqrt{a^2 + b^2} \geq 0\\]

Since the modulus measures a geometric length, it cannot be negative. When \\( r = 0 \\), the only complex number satisfying this condition is \\( z = 0 \\), which corresponds to the origin of the complex plane. In that case, there is no directional component and the argument \\( \theta \\) is undefined. For every nonzero complex number, the modulus is strictly positive, that is, \\( r > 0 \\).

---

The argument \\( \theta \\) of a complex number describes its angular position in the complex plane, measured in radians from the positive real axis. Unlike the modulus, which is uniquely determined, the argument is not unique: two angles that differ by an [integer](../integers/) multiple of \\( 2\pi \\) describe the same direction, and therefore the same complex number. More precisely, for any \\( k \in \mathbb{Z} \\), the angles \\( \theta \\) and \\( \theta + 2k\pi \\) correspond to the same point in the complex plane. This is often written in the following compact form:

\\[\arg(z) = \theta + 2k\pi, \quad k \in \mathbb{Z}\\]

To obtain a unique representative, one typically selects the principal argument, denoted \\( \text{Arg}(z), \\) which is the value of \\( \theta \\) lying in the interval below.

\\[-\pi < \theta \leq \pi\\]

In this convention, angles are measured counterclockwise from the positive real axis, with negative values corresponding to directions below it. An alternative convention, common in engineering and applied mathematics, restricts the argument to the interval below.

\\[0 \leq \theta < 2\pi\\]

In this case all arguments are taken as non-negative. Both conventions are equally valid; the choice depends on the context. Regardless of the convention adopted, the argument of \\( z = 0 \\) remains undefined, since the origin carries no directional information.

- - -
## How to express a complex number in trigonometric form

- Given a complex number \\( z = a + bi \\), compute its modulus using the following formula.
  \\[r = \sqrt{a^2 + b^2}\\]
- Determine the argument \\( \theta \\) by identifying the quadrant of the point \\( (a, b) \\) in the complex plane. When \\( a > 0 \\), the argument is given by the following.
  \\[\theta = \arctan\\!\left(\frac{b}{a}\right)\\]
  When \\( a < 0 \\), a correction of \\( \pm\pi \\) must be added depending on the sign of \\( b \\). When \\( a = 0 \\) the argument is \\( \pi/2 \\) if \\( b > 0 \\) and \\( -\pi/2 \\) if \\( b < 0 \\).
- Substitute \\( r \\) and \\( \theta \\) into the trigonometric form.
  \\[z = r (\cos \theta + i \sin \theta)\\]

- - -
## Example

Consider the complex number \\( z = 1 + i \\) and its conversion to trigonometric form. The modulus is computed by applying the definition directly. Since \\( a = 1 \\) and \\( b = 1 \\), one obtains the following:

\\[r = \sqrt{a^2 + b^2} = \sqrt{1^2 + 1^2} = \sqrt{2}\\]

To determine the argument, observe that the point \\( (1, 1) \\) lies in the first quadrant of the complex plane, where both components are positive. Since \\( a > 0 \\), the argument is given by the arctangent of the ratio \\( b/a \\). Substituting the values yields the following:

\\[\theta = \arctan\\!\left(\frac{b}{a}\right) = \arctan\\!\left(\frac{1}{1}\right) = \arctan(1) = \frac{\pi}{4}\\]

This result is consistent with the geometry of the situation: the complex number \\( 1 + i \\) lies along the bisector of the first quadrant, which forms an angle of \\( \pi/4 \\) radians with the positive real axis.

Substituting \\( r = \sqrt{2} \\) and \\( \theta = \dfrac{\pi}{4} \\) into the trigonometric form gives the final result.

The complex number \\( 1 + i \\) in its trigonometric form is:

\\[z = \sqrt{2} \left(\cos\frac{\pi}{4} + i\sin\frac{\pi}{4} \right)\\]