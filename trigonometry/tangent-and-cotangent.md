# Tangent and Cotangent

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/tangent-and-cotangent

## Introduction

Tangent and cotangent are two trigonometric ratios derived from [sine and cosine](../sine-and-cosine). Given an oriented angle \\(\theta\\), the tangent is defined as the ratio of the sine of \\(\theta\\) to its cosine, and the cotangent as the reciprocal ratio:

\\[
\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)} \qquad \cot(\theta) = \frac{\cos(\theta)}{\sin(\theta)}
\\]

Both admit a precise geometric interpretation on the [unit circle](../unit-circle), where they appear as signed lengths of segments associated with the terminal side of the angle. Unlike sine and cosine, which are defined for every real number, tangent and cotangent are not defined everywhere: the tangent is undefined where the cosine vanishes, and the cotangent where the sine vanishes.

- - -
## Tangent

Consider the unit circle centered at the origin \\(\text{O} = (0,0)\\) with radius 1. Let \\(\theta\\) be an angle in standard position, and denote by \\(\text{P}\\) the point on the circle where the terminal side of \\(\theta\\) intersects it.

* The point \\(\text{S} = (1, 0)\\) is where the circle meets the vertical line \\(x = 1\\). The line through \\(\text{S}\\) perpendicular to the \\(x\\)-axis is tangent to the [unit circle](../unit-circle) at \\(\text{S}\\).
* Extend the ray from \\(\text{O}\\) through \\(\text{P}\\) until it meets this vertical tangent line at a point \\(\text{T}\\).
* The signed length of the segment \\(\overline{ST}\\) defines the tangent of \\(\theta\\):

\\[
\tan(\theta) = \overline{ST}
\\]

From the definition, it follows that the trigonometric tangent is a numerical value representing a ratio, whereas the geometric tangent is a line. The two should not be confused: the trigonometric tangent quantifies the relationship between the [sine and cosine](../sine-and-cosine) of an angle, while the geometric tangent is the line touching a circle at exactly one point.

Triangles \\(\text{OST}\\) and \\(\text{ORP}\\) are similar by construction. Their proportionality gives:

\\[
\frac{\overline{ST}}{\overline{OS}} = \frac{\overline{RP}}{\overline{OR}}
\\]

By the definition of [sine and cosine](../sine-and-cosine), one has \\(\overline{RP} = \sin(\theta)\\) and \\(\overline{OR} = \cos(\theta)\\), so that:

\\[
\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)}
\\]

Since the cosine vanishes at \\(\theta = \dfrac{\pi}{2} + k\pi\\) for every \\(k \in \mathbb{Z}\\), the tangent is undefined at those values:

\\[
\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)} \qquad \theta \neq \frac{\pi}{2} + k\pi \quad k \in \mathbb{Z}
\\]

- - -
## Common values of the tangent

The following table collects the values of \\( \tan(x) \\) at the most frequently encountered angles, expressed in radians.

\\[
\begin{align}
x &= -\pi/3  &\quad& \tan(-\pi/3) = -\sqrt{3} \\\\[6pt]
x &= -\pi/4  &\quad& \tan(-\pi/4) = -1 \\\\[6pt]
x &= -\pi/6  &\quad& \tan(-\pi/6) = -1/\sqrt{3} \\\\[6pt]
x &= 0       &\quad& \tan(0) = 0 \\\\[6pt]
x &= \pi/6   &\quad& \tan(\pi/6) = 1/\sqrt{3} \\\\[6pt]
x &= \pi/4   &\quad& \tan(\pi/4) = 1 \\\\[6pt]
x &= \pi/3   &\quad& \tan(\pi/3) = \sqrt{3}
\end{align}
\\]

- - -
## Trigonometric identities for the tangent

+ \\[  \text{1.} \quad \tan(x+y) = \frac{\tan(x) + \tan(y)}{1 - \tan(x)\tan(y)} \\]

+ \\[ \text{2.} \quad  \tan(x-y) = \frac{\tan(x) - \tan(y)}{1 + \tan(x)\tan(y)} \\]

+ \\[\text{3.} \quad  \tan(2x) = \frac{2\\,\tan(x)}{1 - \tan^{2}(x)} \\]

+ \\[ \text{4.} \quad  \tan\left(\frac{x}{2}\right) = \frac{\sin x}{1 + \cos x} = \frac{1 - \cos x}{\sin x} \\]

+ \\[\text{5.} \quad  1 + \tan^{2}(x) = \sec^{2}(x)\\]
+ \\[\text{6.} \quad  \tan(x)\\,\cot(x) = 1\\]

> These identities describe how tangent behaves under angle addition, subtraction, doubling, halving, and reciprocal relationships. They complement the identities for sine and cosine and are especially useful when simplifying expressions or transforming trigonometric equations. For a broader overview, refer to the full collection of [trigonometric identities](../trigonometric-identities/).

- - -
## Cotangent

The reciprocal of the tangent is called the cotangent and is denoted by \\(\cot(\theta).\\) Geometrically, it corresponds to the signed length of a segment \\(\overline{ZV}\\) constructed on the horizontal tangent line at the top of the unit circle, in a manner analogous to the construction for the tangent. It can be expressed as:

\\[
\cot(\theta) = \frac{1}{\tan(\theta)} = \frac{\cos(\theta)}{\sin(\theta)} = \overline{ZV}
\\]

Since the sine vanishes at \\(\theta = k\pi\\) for every \\(k \in \mathbb{Z}\\), the cotangent is undefined at those values:

\\[
\cot(\theta) = \frac{\cos(\theta)}{\sin(\theta)} \qquad \theta \neq k\pi \quad k \in \mathbb{Z}
\\]

- - -
## Trigonometric identities for the cotangent

+ \\[\text{1.} \quad  \cot(x+y) = \frac{\cot(x)\cot(y) - 1}{\cot(x) + \cot(y)}\\]

+ \\[\text{2.} \quad  \cot(x-y) = \frac{\cot(x)\cot(y) + 1}{\cot(y) - \cot(x)}\\]

+ \\[\text{3.} \quad  \cot(2x) = \frac{\cot^{2}(x) - 1}{2\\,\cot(x)}  \\]

+ \\[\text{4.} \quad \cot\left(\frac{x}{2}\right) = \frac{1 + \cos x}{\sin x}\\]
+ \\[\text{5.} \quad 1 + \cot^{2}(x) = \csc^{2}(x)\\]

> These identities describe how cotangent behaves under angle addition, subtraction, doubling, halving, and reciprocal relationships.

- - -
## Tangent and cotangent functions

The [tangent function](../tangent-function/) \\(f(x) = \tan(x)\\) assigns to each angle \\(x\\), expressed in radians, its corresponding tangent value. Its graph is a periodic curve with period \\(\pi\\), crossing the horizontal axis at every integer multiple of \\(\pi\\) and displaying vertical [asymptotes](../asymptotes/) at \\(x = \pi/2 + k\pi\\) for \\(k \in \mathbb{Z}\\), where the cosine vanishes. The [domain](../determining-the-domain-of-a-function/) of \\(\tan(x)\\) consists of all [real numbers](../types-of-numbers) except these values, and its range is the entire real line.

* Domain: \\( \left\\{ x \in \mathbb{R} : x \neq \frac{\pi}{2} + k\pi \text{ for all } k \in \mathbb{Z} \right\\} \\)
* Range: \\( y \in \mathbb{R} \\)
* Periodicity: periodic in \\( x \\) with period \\( \pi \\)
* Parity: [odd](../even-and-odd-functions/), \\( \tan(-x) = -\tan(x) \\)

---

The [cotangent function](../cotangent-function) \\( f(x) = \cot(x) \\) assigns to each angle \\( x \\), expressed in radians, its corresponding cotangent value. Its graph is a periodic curve with period \\( \pi \\), featuring vertical asymptotes at \\( x = k\pi \\) for \\( k \in \mathbb{Z} \\), where the sine vanishes. The domain excludes these points, and the range is the entire real line.

* Domain: \\( \left\\{ x \in \mathbb{R} : x \neq k\pi \text{ for all } k \in \mathbb{Z} \right\\} \\)
* Range: \\( y \in \mathbb{R} \\)
* Periodicity: periodic in \\( x \\) with period \\( \pi \\)
* Parity: [odd](../even-and-odd-functions/), \\( \cot(-x) = -\cot(x) \\)
## Tangent and cotangent in the complex setting

In the theory of [complex numbers](../complex-numbers-introduction), the tangent and cotangent arise from the [trigonometric form](../complex-numbers-trigonometric-form) of a complex number. Any complex number \\(z = a + bi\\) can be written as:

\\[
z = r(\cos\theta + i\sin\theta)
\\]

where \\(r = \sqrt{a^2+b^2}\\) is the modulus and \\(\theta\\) is the argument. In this representation, the tangent of the argument satisfies:

\\[
\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)} = \frac{b/r}{a/r} = \frac{b}{a}
\\]

so that the tangent of the argument of a complex number coincides with the ratio of its imaginary part to its real part. This is the basis of the formula \\(\theta = \arctan(b/a)\\), used to recover the argument from the Cartesian components of \\(z\\).

A deeper connection emerges through the [exponential form](../complex-numbers-exponential-form). By Euler's formula:

\\[
e^{i\theta} = \cos\theta + i\sin\theta
\\]

one can express the tangent entirely in terms of complex exponentials:

\\[
\tan(\theta) = \frac{\sin\theta}{\cos\theta} = \frac{e^{i\theta} - e^{-i\theta}}{i(e^{i\theta} + e^{-i\theta})}
\\]

This expression mirrors the structure of the [hyperbolic tangent](../hyperbolic-tangent-and-cotangent), which is defined as \\(\tanh(x) = (e^x - e^{-x})/(e^x + e^{-x})\\), and reveals that the two are related by the substitution \\(x \to i\theta\\):

\\[
\tan(\theta) = -i\tanh(i\theta)
\\]

This identity reflects the deeper unity between circular and hyperbolic trigonometry, both of which emerge from the same exponential framework over the complex numbers.

- - -
## The Weierstrass substitution

The half-angle formula for the tangent is the starting point of one of the most useful techniques in [integral](../definite-integrals/) calculus, the Weierstrass substitution. The substitution is defined by:

\\[
t = \tan\\!\left(\frac{x}{2}\right)
\\]

From this assignment one derives the rational expressions of sine and cosine in terms of \\(t\\):

\\[
\begin{align}
\sin x &= \frac{2t}{1+t^{2}} \\\\[6pt]
\cos x &= \frac{1-t^{2}}{1+t^{2}}
\end{align}
\\]

The differential transforms accordingly:

\\[
dx = \frac{2\\,dt}{1+t^{2}}
\\]

Any integral whose integrand is a rational function of \\(\sin x\\) and \\(\cos x\\) becomes an integral of a rational function in the single variable \\(t\\), which can be evaluated by [partial fraction decomposition](https://algebrica.org/partial-fraction-decomposition/). The half-angle identity thus connects trigonometric integration with the integration of rational functions.