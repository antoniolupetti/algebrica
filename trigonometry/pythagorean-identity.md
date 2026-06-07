---
title: Pythagorean Identity
source: https://algebrica.org/pythagorean-identity/
license: CC BY-NC 4.0
tags:
  - pythagorean-identity
  - trigonometric-identities
  - trigonometry
  - unit-circle
---

## Definition

The Pythagorean identity is an equation that connects trigonometry and geometry, and it derives directly from the [Pythagorean theorem](../pythagorean-theorem/), which relates the sides of a right triangle. Consider a right triangle whose hypotenuse has length $1$. Placing the triangle on the [unit circle](../unit-circle/) and letting $\theta$ denote an [angle](../angles-and-angular-measure/) at the origin, the two legs have lengths equal to $\sin(\theta)$ and $\cos(\theta)$, respectively.

![IMG. 1](svg/unit-circle-2.svg)

The identity takes the form

$$
\sin^2\theta + \cos^2\theta = 1
$$

where $\sin^2\theta$ stands for $(\sin\theta)^2$ and $\cos^2\theta$ stands for $(\cos\theta)^2$. To see why this holds, recall that the Pythagorean theorem states that, in any right triangle, the square of the hypotenuse equals the sum of the squares of the two legs.

![IMG. 2](svg/pythagorean-theorem-1.svg)

Denoting the hypotenuse by $c$ and the legs by $a$ and $b$, the theorem reads

$$
a^2 + b^2 = c^2
$$

By placing the triangle inside the unit circle, the hypotenuse $c$ coincides with the radius of the circle, which by definition equals one. Substituting $c = 1$, $a = \sin\theta$, and $b = \cos\theta$ into the equation above yields the Pythagorean identity directly.

The Pythagorean identity makes it possible to express each of the two functions in terms of the other. Solving for sine gives

$$
\sin\theta = \pm \sqrt{1 - \cos^2\theta}
$$

and solving for cosine gives:

$$
\cos\theta = \pm \sqrt{1 - \sin^2\theta}
$$

In each case, the sign depends on the [quadrant](../identities-using-reference-angles/) in which $\theta$ lies. In the first quadrant both functions are positive, so the positive square root applies; in the remaining quadrants the sign must be chosen in accordance with the known sign of the relevant function in that region.

The same identity also gives rise to two further relationships, one involving [tangent](../tangent-and-cotangent/) and [secant](../secant-and-cosecant/), the other involving [cotangent](../tangent-and-cotangent/) and [cosecant](../secant-and-cosecant/).

To obtain the first, divide both sides of $\sin^2\theta + \cos^2\theta = 1$ by $\cos^2\theta$:

$$
\frac{\sin^2\theta}{\cos^2\theta} + \frac{\cos^2\theta}{\cos^2\theta} = \frac{1}{\cos^2\theta}
$$

Recognising that $\sin\theta / \cos\theta = \tan\theta$ and $1/\cos\theta = \sec\theta$, the equation reduces to:

$$
\tan^2\theta + 1 = \sec^2\theta
$$

To obtain the second, divide both sides instead by $\sin^2\theta$:

$$
\frac{\sin^2\theta}{\sin^2\theta} + \frac{\cos^2\theta}{\sin^2\theta} = \frac{1}{\sin^2\theta}
$$

Since $\cos\theta / \sin\theta = \cot\theta$ and $1/\sin\theta = \csc\theta$, this simplifies to:

$$
1 + \cot^2\theta = \csc^2\theta
$$

The three identities obtained, together with the original Pythagorean identity, form the backbone of most algebraic manipulations encountered in trigonometry.

## Domain restrictions

The following identities hold only where the respective divisions are defined.

$$
\begin{align}
\tan^2\theta + 1 &= \sec^2\theta \\[6pt]
1 + \cot^2\theta &= \csc^2\theta
\end{align}
$$ 

Dividing by $\cos^2\theta$ is valid for all $\theta$ that are not odd multiples of $\pi/2$, since those are precisely the values at which $\cos\theta = 0$ and $\tan\theta$ and $\sec\theta$ are undefined.

Similarly, dividing by $\sin^2\theta$ requires $\sin\theta \neq 0$, which excludes all integer multiples of $\pi$, where $\cot\theta$ and $\csc\theta$ are undefined. The original identity $\sin^2\theta + \cos^2\theta = 1$, by contrast, holds for every real value of $\theta$ without exception.

This coincidence between the [domain](../determining-the-domain-of-a-function/) restrictions and the natural domains of $\tan$, $\sec$, $\cot$, and $\csc$ is not accidental. These four functions are defined precisely as ratios involving sine and cosine, so the values excluded from their domains are exactly those at which the relevant denominator vanishes. The restrictions that appear when deriving the identities by division are therefore the same restrictions that define the functions themselves, and could not be otherwise.

## Validity for arbitrary angles

The geometric argument given above establishes the identity for acute angles, since it relies on interpreting sine and cosine as the lengths of the legs of a right triangle. This interpretation ceases to be meaningful when $\theta$ is obtuse, negative, or greater than $2\pi$, and a more general foundation is therefore needed.

The standard approach is to define sine and cosine analytically via the unit circle. For any real number $\theta$, one defines $\cos\theta$ and $\sin\theta$ as the coordinates of the point obtained by moving a distance $\theta$ along the unit circle starting from $(1, 0)$, with the convention that positive values correspond to counterclockwise motion.

Under this definition, the point $(\cos\theta, \sin\theta)$ lies on the unit circle by construction, and the equation of the unit circle is $x^2 + y^2 = 1$. Substituting $x = \cos\theta$ and $y = \sin\theta$ yields:

$$
\cos^2\theta + \sin^2\theta = 1
$$

for every real value of $\theta$, without any restriction on the quadrant or the magnitude of the angle. The identity is therefore not a consequence of triangle geometry, but a direct expression of the definition of the trigonometric functions on the real line.

## Example 1

The Pythagorean identity is often useful in simplifying expressions that do not appear, at first glance, to involve it. The following expression illustrates how recognising an algebraic structure in the numerator can reduce an apparently non-trivial fraction to a constant. Consider the expression:

$$
\frac{\sin^4\theta - \cos^4\theta}{\sin^2\theta - \cos^2\theta}
$$

The numerator is a difference of two squares, and factors accordingly as:

$$
\sin^4\theta - \cos^4\theta = (\sin^2\theta + \cos^2\theta)(\sin^2\theta - \cos^2\theta)
$$

Since $\sin^2\theta + \cos^2\theta = 1$ by the Pythagorean identity, the numerator reduces to $\sin^2\theta - \cos^2\theta$. The expression therefore simplifies to:

$$
\frac{\sin^2\theta - \cos^2\theta}{\sin^2\theta - \cos^2\theta} = 1
$$

provided that $\sin^2\theta \neq \cos^2\theta$, that is, for all $\theta$ that are not odd multiples of $\pi/4$.

## Rewriting expressions in a single function

A common requirement in calculus and mathematical analysis is to rewrite a trigonometric expression so that it involves only one function. The three Pythagorean identities provide a systematic way to do this, and the technique appears repeatedly across a wide range of problems, from the simplification of trigonometric expressions to the computation of integrals and the solution of differential equations.

From the fundamental identity:

$$\sin^2\theta + \cos^2\theta = 1$$

we obtain the two substitution rules:

$$
\begin{align}
\sin^2\theta &= 1 - \cos^2\theta \\[6pt]
\cos^2\theta &= 1 - \sin^2\theta
\end{align}
$$


These allow any [polynomial](../polynomials/) expression in both sine and cosine to be reduced to a polynomial in one of them alone. For example, an expression of the form:

$$\sin^2\theta + 2\sin\theta\cos\theta + \cos^2\theta$$

can be simplified by observing that: $\sin^2\theta + \cos^2\theta = 1$, leaving $1 + 2\sin\theta\cos\theta$, which is recognisable as $1 + \sin 2\theta$.

The derived identities serve the same purpose for expressions involving the reciprocal and ratio functions. From $\tan^2\theta + 1 = \sec^2\theta$ one obtains $\tan^2\theta = \sec^2\theta - 1$, which is useful whenever an expression mixes $\tan\theta$ and $\sec\theta$ and a reduction to a single function is needed.

Similarly, from $1 + \cot^2\theta = \csc^2\theta$ one obtains $\cot^2\theta = \csc^2\theta - 1$, allowing expressions in $\cot\theta$ and $\csc\theta$ to be written in terms of $\csc\theta$ alone.

Many standard [integrals](../definite-integrals/) require the integrand to be expressed in a form that matches a known pattern before a substitution can be applied. The integral of $\tan^2\theta$, for instance, is not immediately reducible by elementary rules. Substituting $\tan^2\theta = \sec^2\theta - 1$ rewrites the integrand as a difference of two terms, each of which is straightforward to integrate:

$$
\begin{align}
\int \tan^2\theta \ d\theta &= \int (\sec^2\theta - 1) \ d\theta \\[6pt]
&= \int \sec^2\theta \ d\theta - \int d\theta \\[6pt]
&= \tan\theta - \theta + c
\end{align}
$$

The same principle underlies trigonometric substitution, where expressions involving radicals such as $\sqrt{1 - x^2}$ or $\sqrt{1 + x^2}$ are handled by introducing a trigonometric variable and then applying the appropriate Pythagorean identity to eliminate the radical entirely. In the case of $\sqrt{1 - x^2}$, the substitution $x = \sin\theta$ transforms the radical as follows:

$$
\sqrt{1 - x^2} = \sqrt{1 - \sin^2\theta} = \sqrt{\cos^2\theta} = |\cos\theta|
$$

which reduces to $\cos\theta$ whenever $\theta \in \left[-\dfrac{\pi}{2}, \dfrac{\pi}{2}\right]$, the standard range chosen for this substitution. The radical has been eliminated entirely, and the resulting integral involves only trigonometric functions, to which standard techniques apply directly.

## Example 2

The substitution $x = \sin\theta$ is a standard technique for integrals containing the radical $\sqrt{1 - x^2}$. The Pythagorean identity is what makes the substitution effective: it guarantees that the radical collapses to a single trigonometric function, eliminating the square root entirely. Consider the following integral:

$$
\int \sqrt{1 - x^2} \ dx
$$

Setting $x = \sin\theta$, with $\theta \in \left[-\dfrac{\pi}{2}, \dfrac{\pi}{2}\right]$, gives $dx = \cos\theta \ d\theta$. The [radical](../radicals/) transforms as follows:

$$
\sqrt{1 - x^2} = \sqrt{1 - \sin^2\theta} = \sqrt{\cos^2\theta} = \cos\theta
$$

where the last step uses the fact that $\cos\theta \geq 0$ on the chosen interval. Substituting into the integral gives:

$$
\int \sqrt{1 - x^2} \ dx = \int \cos\theta \cdot \cos\theta \ d\theta = \int \cos^2\theta \ d\theta
$$

The integrand $\cos^2\theta$ is handled via the identity $\cos^2\theta = \dfrac{1 + \cos 2\theta}{2}$, which yields:

$$
\begin{align}
\int \cos^2\theta \ d\theta &= \int \frac{1 + \cos 2\theta}{2} \ d\theta \\[6pt]
&= \frac{\theta}{2} + \frac{\sin 2\theta}{4} + c
\end{align}
$$

It remains to return to the original variable. Since $x = \sin\theta$, one has $\theta = \arcsin x$. For the term $\sin 2\theta$, the double angle formula gives $\sin 2\theta = 2\sin\theta\cos\theta = 2x\sqrt{1-x^2}$.

The solution is therefore:

$$
\int \sqrt{1 - x^2} \ dx = \frac{\arcsin x}{2} + \frac{x\sqrt{1 - x^2}}{2} + c
$$

> This is the area formula for a semicircle of unit radius, as expected from the geometric interpretation of the integrand.

## Derivation from the equation $y'' + y = 0$

The Pythagorean identity admits a purely analytical proof that does not rely on the geometry of the unit circle. The starting point is the fact that both $\sin x$ and $\cos x$ are solutions of the linear second-order differential equation:

$$
y'' + y = 0
$$

This follows directly from the [derivatives](../derivatives/) $\sin'(x) = \cos(x)$ and $\cos'(x) = -\sin(x)$, which together give $\sin''(x) = -\sin(x)$ and $\cos''(x) = -\cos(x)$.

For any twice differentiable function $f$ that satisfies $f'' + f = 0$, the auxiliary quantity:

$$
E(x) := \bigl(f'(x)\bigr)^{2} + \bigl(f(x)\bigr)^{2}
$$

is constant on the entire real line. To verify this, we compute its derivative:

$$
\begin{align}
E'(x)
&= 2 f'(x) f''(x) + 2 f(x) f'(x) \\[6pt]
&= 2 f'(x) \bigl(f''(x) + f(x)\bigr)
\end{align}
$$

The factor in parentheses vanishes by hypothesis, so $E'(x) = 0$ for every $x$. A function with identically zero derivative on $\mathbb{R}$ is constant, and the constant is recovered by evaluating $E$ at any chosen point. Choosing the origin yields:

$$
E(x) = E(0) = \bigl(f'(0)\bigr)^{2} + \bigl(f(0)\bigr)^{2}
$$

Applying this conservation law to $f = \sin$, whose initial values are $\sin(0) = 0$ and $\sin'(0) = \cos(0) = 1$, we obtain:

$$
\bigl(\sin'(x)\bigr)^{2} + \bigl(\sin(x)\bigr)^{2} = 1^{2} + 0^{2} = 1
$$

Since $\sin'(x) = \cos(x)$, the left-hand side coincides with $\cos^{2}(x) + \sin^{2}(x)$, and the Pythagorean identity follows for every real $x$.

> Read in this way, the identity is the conservation law associated with the equation $y'' + y = 0$. The quantity $(f')^{2} + f^{2}$ plays the role of total energy of a harmonic oscillator and remains constant along every solution, with the value of $\sin^{2} x + \cos^{2} x$ fixed once and for all by the initial data of the sine function.

## Connection with Euler's formula

The Pythagorean identity admits an especially transparent proof once the trigonometric functions are extended to the complex plane. [Euler's formula](../eulers-formula/) states that for any real $\theta$, the [complex exponential](../complex-numbers-exponential-form/) satisfies:

$$e^{i\theta} = \cos\theta + i\sin\theta$$

Since $e^{i\theta}$ lies on the unit circle in the complex plane, its [modulus](../complex-numbers-introduction/) is equal to one. Computing the squared modulus directly gives:

$$
|e^{i\theta}|^2 = \cos^2\theta + \sin^2\theta = 1
$$

which recovers the Pythagorean identity as an immediate consequence of the definition of the exponential function on the imaginary axis.