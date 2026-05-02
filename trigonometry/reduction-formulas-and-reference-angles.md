# Reduction Formulas and Reference Angles

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/reduction-formulas-and-reference-angles/

## Using reference angles to rewrite angles

Given an angle \\( \theta \\) in standard position on the [unit circle](../unit-circle/), the acute angle formed between its terminal side and the horizontal axis is called the reference angle of \\( \theta \\), and is usually denoted by \\( \alpha \\). The reference angle provides a direct link between the trigonometric functions of a generic angle and those of an acute angle in the first quadrant, where all values are positive and computable from elementary geometric considerations.

The identities that realize this link are known as reduction formulas. Each of them expresses a trigonometric function of \\( \theta \\) in terms of the same function, or its cofunction, evaluated at \\( \alpha \\), with a sign fixed by the quadrant in which \\( \theta \\) lies. The angle forms that appear most frequently are the following:

\\[
\frac{\pi}{2}\pm\alpha,\quad \pi\pm\alpha,\quad \frac{3\pi}{2}\pm\alpha,\quad 2\pi-\alpha
\\]

Every other case reduces to one of these by adding or subtracting an integer multiple of \\( 2\pi \\).

- - -

For each of these forms, two pieces of information completely determine the corresponding reduction formula: the quadrant of the angle, which fixes the signs of the four trigonometric functions, and the axis used as reference, which determines whether the reduction preserves each function or swaps it with its cofunction. 

Angles written as deviations from \\( \pi/2\\) or \\(3\pi/2\\) are measured from a vertical axis, and their reduction involves the exchange of [sine with cosine](../sine-and-cosine/) and of [tangent with cotangent](../tangent-and-cotangent/). Angles written as deviations from \\( \pi \\) or \\( 2\pi \\) are measured from a horizontal axis, and their reduction keeps each function unchanged. The table below gathers this information for all the forms considered on this page, listing the quadrant, the sign of each trigonometric function, and whether a cofunction swap occurs.


| Form | Quadrant | \\( \sin \\) | \\( \cos \\) | \\( \tan \\) | \\( \cot \\) | Cofunction swap |
| --- | --- | --- | --- | --- | --- | --- |
| \\( \pi/2-\alpha \\) | 1° | \\( + \\) | \\( + \\) | \\( + \\) | \\( + \\) | yes |
| \\( \pi/2+\alpha \\) | 2° | \\( + \\) | \\( - \\) | \\( - \\) | \\( - \\) | yes |
| \\( \pi-\alpha \\) | 2° | \\( + \\) | \\( - \\) | \\( - \\) | \\( - \\) | no |
| \\( \pi+\alpha \\) | 3° | \\( - \\) | \\( - \\) | \\( + \\) | \\( + \\) | no |
| \\( 3\pi/2-\alpha \\) | 3° | \\( - \\) | \\( - \\) | \\( + \\) | \\( + \\) | yes |
| \\( 3\pi/2+\alpha \\) | 4° | \\( - \\) | \\( + \\) | \\( - \\) | \\( - \\) | yes |
| \\( 2\pi-\alpha \\) | 4° | \\( - \\) | \\( + \\) | \\( - \\) | \\( - \\) | no |

> The sections that follow derive each identity geometrically, starting from the position of the terminal side on the unit circle and reading the sign of the coordinates directly from the figure.

- - -
## Reduction formulas for \\( \pi/2 + \alpha \\)

Consider an angle of the form \\(\pi/2+\alpha\\) where \\( \alpha \\) denotes an acute angle measured from the positive \\( x \\)-axis. Starting from \\( \frac{\pi}{2} \\), which corresponds to the vertical direction, the addition of \\( \alpha \\) rotates the terminal side slightly to the left of the vertical axis, as shown in the figure below. The resulting angle lies strictly between \\( \frac{\pi}{2} \\) and \\( \pi \\), and therefore its terminal side falls in the second quadrant of the Cartesian plane.

A direct geometric analysis of the right triangle determined by the terminal side yields the following identities for sine and cosine:
\\[
\begin{align}
\sin\left(\frac{\pi}{2}+\alpha\right) &= \cos\alpha \\\\[6pt]
\cos\left(\frac{\pi}{2}+\alpha\right) &= -\sin\alpha
\end{align}
\\]
The geometric meaning of these identities is transparent. The [sine](../sine-and-cosine) of \\( \alpha \\), which measures the vertical segment associated with the acute angle in the first quadrant, coincides in length with the [cosine](../sine-and-cosine) of \\( \frac{\pi}{2}+\alpha \\), which measures the horizontal segment associated with the corresponding angle in the second quadrant. The only difference is the sign, since the latter segment extends to the left of the vertical axis and therefore carries a negative value. The identities for tangent and cotangent follow at once from the definitions:

\\[
\begin{align}
\tan\alpha &= \frac{\sin\alpha}{\cos\alpha} \\\\[6pt]
\cot\alpha &= \frac{\cos\alpha}{\sin\alpha}
\end{align}
\\]

Substituting the expressions obtained above into these definitions gives:

\\[
\begin{align}
\tan\left(\frac{\pi}{2}+\alpha\right) &= \frac{\cos\alpha}{-\sin\alpha} = -\cot\alpha \\\\[6pt]
\cot\left(\frac{\pi}{2}+\alpha\right) &= \frac{-\sin\alpha}{\cos\alpha} = -\tan\alpha
\end{align}
\\]

The tangent and cotangent of \\( \pi/2+\alpha \\) therefore differ from the cotangent and tangent of \\( \alpha \\) only by a change of sign, consistently with the fact that both functions are negative in the second quadrant.

- - -
## Reduction formulas for \\( \pi/2 - \alpha \\)

Consider now an angle of the form \\(\frac{\pi}{2}-\alpha\\) where \\( \alpha \\) denotes an acute angle in the first quadrant. This angle is obtained by rotating counterclockwise from the positive \\( x \\)-axis up to \\( \frac{\pi}{2} \\), and then turning back by \\( \alpha \\). The backward rotation brings the terminal side to the right of the vertical axis, keeping it between \\( 0 \\) and \\( \frac{\pi}{2} \\). The resulting angle therefore lies in the first quadrant of the Cartesian plane.

A geometric analysis of the right triangle associated with the terminal side yields the following identities for sine and cosine:
\\[
\begin{align}
\sin\left(\frac{\pi}{2}-\alpha\right) &= \cos\alpha \\\\[6pt]
\cos\left(\frac{\pi}{2}-\alpha\right) &= \sin\alpha
\end{align}
\\]
In this case both functions retain a positive sign, consistently with the fact that the angle lies in the first quadrant, and the cofunction swap exchanges sine with cosine in a perfectly symmetric way. The identities for tangent and cotangent follow directly from their definitions as ratios:
\\[
\begin{align}
\tan\left(\frac{\pi}{2}-\alpha\right) &= \frac{\cos\alpha}{\sin\alpha} = \cot\alpha \\\\[6pt]
\cot\left(\frac{\pi}{2}-\alpha\right) &= \frac{\sin\alpha}{\cos\alpha} = \tan\alpha
\end{align}
\\]
The tangent of \\( \pi/2-\alpha \\) therefore coincides with the cotangent of \\( \alpha \\), and viceversa, in agreement with the general rule that angles measured from a vertical axis produce a cofunction swap.

- - -
## Reduction formulas for \\( \pi + \alpha \\)

Consider now an angle of the form \\(\pi+\alpha)\\), where \\( \alpha \\) denotes an acute angle. Starting from \\( \pi \\), which corresponds to the negative direction of the \\( x \\)-axis, the addition of \\( \alpha \\) rotates the terminal side slightly downward, bringing it into the lower-left region of the Cartesian plane. The resulting angle lies strictly between \\( \pi \\) and \\( 3\pi/2 \\), and therefore its terminal side falls in the third quadrant.

A direct reading of the coordinates of the terminal side on the unit circle gives the following identities for sine and cosine:
\\[
\begin{align}
\sin(\pi+\alpha) &= -\sin\alpha \\\\[6pt]
\cos(\pi+\alpha) &= -\cos\alpha
\end{align}
\\]
Both values carry a negative sign, as expected in the third quadrant, where the terminal side lies below the horizontal axis and to the left of the vertical one. In magnitude, however, each function coincides with the corresponding value at \\( \alpha \\), since \\( \pi+\alpha \\) is obtained from \\( \alpha \\) by a rotation of exactly \\( \pi \\), which reflects the point on the unit circle through the origin. The identities for tangent and cotangent follow at once from the definitions of these functions as ratios:
\\[
\begin{align}
\tan(\pi+\alpha) &= \frac{-\sin\alpha}{-\cos\alpha} = \tan\alpha \\\\[6pt]
\cot(\pi+\alpha) &= \frac{-\cos\alpha}{-\sin\alpha} = \cot\alpha
\end{align}
\\]
The two negative signs cancel in each quotient, and the tangent and cotangent of \\( \pi+\alpha \\) therefore coincide with those of \\( \alpha \\). This is the analytic counterpart of the fact that tangent and cotangent have period \\( \pi \\), whereas sine and cosine have period \\( 2\pi.\\)

- - -
## Reduction formulas for \\( \pi - \alpha \\)

Consider now an angle of the form \\(\pi-\alpha\\) where \\( \alpha \\) denotes an acute angle. Since \\( \pi \\) corresponds to the negative direction of the \\( x \\)-axis, the subtraction of \\( \alpha \\) rotates the terminal side slightly upward, bringing it into the upper-left region of the Cartesian plane. The resulting angle lies strictly between \\( \pi/2 \\) and \\( \pi \\), and therefore its terminal side falls in the second quadrant.

A direct reading of the coordinates of the terminal side on the unit circle gives the following identities for sine and cosine:
\\[
\begin{align}
\sin(\pi-\alpha) &= \sin\alpha \\\\[6pt]
\cos(\pi-\alpha) &= -\cos\alpha
\end{align}
\\]
The sine retains a positive value, consistently with the fact that the terminal side lies above the horizontal axis, while the cosine changes sign because the terminal side is reflected to the left of the vertical axis. In magnitude, both functions coincide with the corresponding values at \\( \alpha \\), since \\( \pi-\alpha \\) and \\( \alpha \\) are symmetric with respect to the vertical axis. The identities for tangent and cotangent follow at once from the definitions of these functions as ratios:
\\[
\begin{align}
\tan(\pi-\alpha) &= \frac{\sin\alpha}{-\cos\alpha} = -\tan\alpha \\\\[6pt]
\cot(\pi-\alpha) &= \frac{-\cos\alpha}{\sin\alpha} = -\cot\alpha
\end{align}
\\]
Both quotients carry a single minus sign, and the tangent and cotangent of \\( \pi-\alpha \\) therefore differ from those of \\( \alpha \\) only by a change of sign. This is consistent with the fact that in the second quadrant both functions take negative values.

- - -
## Reduction formulas for \\( 3\pi/2 + \alpha \\)

Consider now an angle of the form \\(\frac{3\pi}{2}+\alpha\\) where \\( \alpha \\) denotes an acute angle. Starting from \\( 3\pi/2 \\), which corresponds to the negative direction of the \\( y \\)-axis, the addition of \\( \alpha \\) rotates the terminal side slightly to the right of the vertical axis. The resulting angle lies strictly between \\( 3\pi/2 \\) and \\( 2\pi \\), and therefore its terminal side falls in the fourth quadrant of the Cartesian plane.

A direct reading of the coordinates of the terminal side on the unit circle gives the following identities for sine and cosine:
\\[
\begin{align}
\sin\left(\frac{3\pi}{2}+\alpha\right) &= -\cos\alpha \\\\[6pt]
\cos\left(\frac{3\pi}{2}+\alpha\right) &= \sin\alpha
\end{align}
\\]
The sine takes a negative value because the terminal side lies below the horizontal axis, while the cosine remains positive since the terminal side falls to the right of the vertical axis. The cofunction swap is again present, in accordance with the general rule that angles measured from a vertical axis exchange sine with cosine and tangent with cotangent. The identities for tangent and cotangent follow at once from the definitions of these functions as ratios:
\\[
\begin{align}
\tan\left(\frac{3\pi}{2}+\alpha\right) &= \frac{-\cos\alpha}{\sin\alpha} = -\cot\alpha \\\\[6pt]
\cot\left(\frac{3\pi}{2}+\alpha\right) &= \frac{\sin\alpha}{-\cos\alpha} = -\tan\alpha
\end{align}
\\]
Both quotients carry a single minus sign, and the tangent and cotangent of \\( 3\pi/2+\alpha \\) therefore differ from the cotangent and tangent of \\( \alpha \\) only by a change of sign. This is consistent with the fact that in the fourth quadrant both functions take negative values.

- - -
## Reduction formulas for \\( 3\pi/2 - \alpha \\)

Consider now an angle of the form \\(\frac{3\pi}{2}-\alpha\\) where \\( \alpha \\) denotes an acute angle. Since \\( 3\pi/2 \\) corresponds to the negative direction of the \\( y \\)-axis, the subtraction of \\( \alpha \\) rotates the terminal side backward toward \\( \pi \\), bringing it into the lower-left region of the Cartesian plane. The resulting angle lies strictly between \\( \pi \\) and \\( 3\pi/2 \\), and therefore its terminal side falls in the third quadrant.

A direct reading of the coordinates of the terminal side on the unit circle gives the following identities for sine and cosine:
\\[
\begin{align}
\sin\left(\frac{3\pi}{2}-\alpha\right) &= -\cos\alpha \\\\[6pt]
\cos\left(\frac{3\pi}{2}-\alpha\right) &= -\sin\alpha
\end{align}
\\]
Both values carry a negative sign, consistently with the fact that in the third quadrant the terminal side lies below the horizontal axis and to the left of the vertical one. The cofunction swap is again present, as expected for angles measured as deviations from a vertical axis. The identities for tangent and cotangent follow at once from the definitions of these functions as ratios:
\\[
\begin{align}
\tan\left(\frac{3\pi}{2}-\alpha\right) &= \frac{-\cos\alpha}{-\sin\alpha} = \cot\alpha \\\\[6pt]
\cot\left(\frac{3\pi}{2}-\alpha\right) &= \frac{-\sin\alpha}{-\cos\alpha} = \tan\alpha
\end{align}
\\]
The two negative signs cancel in each quotient, and the tangent of \\( 3\pi/2-\alpha \\) therefore coincides with the cotangent of \\( \alpha \\), while the cotangent of \\( 3\pi/2-\alpha \\) coincides with the tangent of \\( \alpha \\). This is in agreement with the fact that both functions take positive values in the third quadrant.

- - -
## Reduction formulas for \\( 2\pi - \alpha = -\alpha \\)

Consider finally an angle of the form \\(2\pi-\alpha\\) where \\( \alpha \\) denotes an acute angle. Since \\( 2\pi \\) corresponds to a full revolution and therefore identifies the same terminal side as \\( 0 \\), the subtraction of \\( \alpha \\) rotates the terminal side slightly below the positive \\( x \\)-axis. The resulting angle lies strictly between \\( 3\pi/2 \\) and \\( 2\pi \\), and therefore its terminal side falls in the fourth quadrant.

The angle \\( 2\pi-\alpha \\) is coterminal with \\( -\alpha \\), that is, the two angles differ by an integer multiple of \\( 2\pi \\) and therefore identify the same point on the unit circle. Since the trigonometric functions have period \\( 2\pi \\), they take the same values at \\( 2\pi-\alpha \\) and at \\( -\alpha \\), and this equivalence will be used implicitly in the identity.

A direct reading of the coordinates of the terminal side on the unit circle gives the following identities for sine and cosine:
\\[
\begin{align}
\sin(2\pi-\alpha) &= -\sin\alpha \\\\[6pt]
\cos(2\pi-\alpha) &= \cos\alpha
\end{align}
\\]
The sine takes a negative value because the terminal side lies below the horizontal axis, while the cosine remains positive since the terminal side falls to the right of the vertical axis. These identities also express the fact that sine is an odd function and cosine an even function of the angle, since \\( 2\pi-\alpha \\) is coterminal with \\( -\alpha \\). The identities for tangent and cotangent follow at once from the definitions of these functions as ratios:
\\[
\begin{align}
\tan(2\pi-\alpha) &= \frac{-\sin\alpha}{\cos\alpha} = -\tan\alpha \\\\[6pt]
\cot(2\pi-\alpha) &= \frac{\cos\alpha}{-\sin\alpha} = -\cot\alpha
\end{align}
\\]
Both quotients carry a single minus sign, and the tangent and cotangent of \\( 2\pi-\alpha \\) therefore differ from those of \\( \alpha \\) only by a change of sign. This is consistent with the fact that in the fourth quadrant both functions take negative values, and with the odd symmetry of tangent and cotangent with respect to the origin.

- - -
## Structural remarks

Beyond their immediate computational use, the reduction formulas reveal a structural feature of the trigonometric functions that is worth stating explicitly. Every identity derived on this page is a consequence of two elementary symmetries of the unit circle: the invariance of the coordinates under a rotation by \\( 2\pi \\), which encodes the periodicity of sine and cosine, and their behaviour under reflections with respect to the coordinate axes, which produces the sign changes and the cofunction swaps. In this sense, reduction formulas are the algebraic translation of how a point moves on the unit circle under a finite group of rigid transformations.

This perspective has concrete consequences in several directions. In the solution of [trigonometric equations](../trigonometric-equations/), reduction formulas are what allows one to reduce any equation involving \\( \sin\theta \\), \\( \cos\theta \\), \\( \tan\theta \\) or \\( \cot\theta \\) to a problem on an acute reference angle, and then to recover the full set of solutions by exploiting periodicity. In [integral calculus](../indefinite-integrals/), they are routinely used to simplify integrands of the form \\( \sin(k\pi\pm x) \\) or \\( \cos(k\pi\pm x) \\) before applying standard integration techniques. In the study of [Fourier series](../fourier-series/), the same sign rules underlie the classification of a function as even, odd, or neither, and determine which coefficients of the series vanish. From a more advanced standpoint, the reduction formulas anticipate the general addition formulas:

\\[
\begin{align}
\sin(\alpha+\beta) &= \sin\alpha\cos\beta+\cos\alpha\sin\beta \\\\[6pt]
\cos(\alpha+\beta) &= \cos\alpha\cos\beta-\sin\alpha\sin\beta
\end{align}
\\]

from which each identity on this page can be recovered by choosing \\( \beta \\) equal to \\( \pi/2 \\), \\( \pi \\), \\( 3\pi/2 \\) or \\( 2\pi \\). What appears here as a catalogue of individual cases is therefore a finite specialization of a single continuous structure, and this is the viewpoint that analytic trigonometry adopts systematically.