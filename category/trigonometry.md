---
title: Trigonometry
source: https://algebrica.org/category/trigonometry/
license: CC BY-NC 4.0
tags:
  - angles
  - hyperbolic-functions
  - radians
  - trigonometric-functions
  - trigonometric-identities
  - unit-circle
---
## Introduction to the chapter

Trigonometry studies the relations between the angles and side lengths of a triangle and the functions that describe those relations. An oriented [angle](../../angles-and-angular-measure/) $\theta$ with vertex at the centre of a circle of radius $r$ sweeps out an arc whose signed length is $s,$ and its radian measure is:

$$\theta = \frac{s}{r}$$

For a fixed angle, doubling the radius doubles the signed arc length, so the ratio depends only on the angle, not on the circle. A full turn measures $2\pi$ radians, a straight angle $\pi,$ and a right angle $\pi/2.$

An angle is in standard position when its vertex is the origin and its initial side lies on the positive $x$-axis. The terminal side meets the [unit circle](../../unit-circle/) at a single point $P,$ and the [cosine and sine](../../sine-and-cosine/) of $\theta$ are the coordinates of that point:

$$P = (\cos\theta, \sin\theta)$$

Angles differing by an integer multiple of $2\pi$ determine the same point, so both functions are periodic with period $2\pi.$ Since $P$ lies on the circle of equation $x^2+y^2=1,$ its coordinates satisfy the [Pythagorean identity](../../pythagorean-identity/):

$$\sin^2\theta+\cos^2\theta = 1$$

The four remaining trigonometric functions are the [tangent and cotangent](../../tangent-and-cotangent/) and the [secant and cosecant](../../secant-and-cosecant/). They are defined in terms of sine and cosine wherever their denominators are nonzero:

$$
\begin{align}
\tan\theta &= \frac{\sin\theta}{\cos\theta} \qquad \cot\theta = \frac{\cos\theta}{\sin\theta} \\[6pt]
\sec\theta &= \frac{1}{\cos\theta} \qquad \csc\theta = \frac{1}{\sin\theta}
\end{align}
$$

In [right triangle trigonometry](../../right-triangle-trigonometry/), the same functions are ratios of side lengths. Two right triangles with the same acute angle $\theta$ have the same interior angles and are therefore similar, so each corresponding side ratio has the same value in both triangles. For an acute angle $\theta$ with opposite leg $y,$ adjacent leg $x,$ and hypotenuse $h,$ the three principal ratios are:

$$\sin\theta = \frac{y}{h} \qquad \cos\theta = \frac{x}{h} \qquad \tan\theta = \frac{y}{x}$$

When a triangle has no right angle, the [law of sines](../../law-of-sines/) and the [law of cosines](../../law-of-cosines/) relate its side lengths and angles and determine the possible values of missing sides or angles when enough data are known. The [trigonometric identities](../../trigonometric-identities/) include formulas for sums, double angles, and half angles.

None of the six functions is injective on its whole domain, so each must be restricted before it has an [inverse function](../../inverse-function/). The sine restricted to $[-\pi/2, \pi/2]$ is invertible, and its inverse is the [arcsine](../../arcsine-and-arccosine/). Analogous restrictions define the arccosine and the [arctangent and arccotangent](../../arctangent-and-arccotangent/).

The [hyperbolic sine and cosine](../../hyperbolic-sine-and-cosine/) are the coordinate functions on the right branch of the equilateral [hyperbola](../../hyperbola/) of equation $X^2-Y^2=1,$ parametrized by twice the signed area of the corresponding sector. They satisfy $\cosh^2 x-\sinh^2 x = 1$ and have the following expressions in terms of the [exponential function](../../exponential-function/):

$$\sinh x = \frac{e^x-e^{-x}}{2} \qquad \cosh x = \frac{e^x+e^{-x}}{2}$$

The chapter begins with [angles and angular measure](../../angles-and-angular-measure/), which defines degrees, radians, and the orientation conventions used in the remaining entries.
