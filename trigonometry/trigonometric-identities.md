---
title: Trigonometric Identities
source: https://algebrica.org/trigonometric-identities/
license: CC BY-NC 4.0
tags:
  - trigonometric-identities
  - trigonometry
---

## Introduction

A trigonometric identity is an equation involving trigonometric functions that holds for every admissible value of the variables. Unlike a trigonometric equation, which is solved for a specific set of [angles](../angles-and-angular-measure/), an identity is an equality that holds throughout the common domain of the functions involved. 

The study of these identities organises the algebraic relationships that tie [sine and cosine](../sine-and-cosine/), [tangent and cotangent](../tangent-and-cotangent/) together, and provides the tools needed to manipulate trigonometric expressions into equivalent forms that are easier to evaluate, [differentiate](../derivatives/), [integrate](../indefinite-integrals/), or interpret geometrically.

The identities presented below are grouped into families according to the type of transformation they perform. Some express a [function](../functions/) of a modified angle in terms of the original angle, others convert products into sums or sums into products, and others still reduce a general angle to a parametric variable. 

Each group plays a distinct role in the resolution of [trigonometric equations](../trigonometric-equations/), in the simplification of expressions, and in the broader apparatus of calculus.

## Fundamental identities

Before examining the transformations that relate trigonometric functions of different angles, it is useful to recall the elementary identities that connect the six trigonometric functions at a single angle. These identities descend directly from the definitions on the [unit circle](../unit-circle/) and from the [Pythagorean theorem](../pythagorean-theorem/), and they form the algebraic foundation on which every subsequent identity is built. The [Pythagorean identity](../pythagorean-identity/) expresses the constraint that the coordinates of any point on the unit circle satisfy the equation of the circle itself:

$$
\sin^2(\theta) + \cos^2(\theta) = 1
$$

Dividing both sides of this identity by $\cos^2(\theta)$, provided $\cos(\theta) \neq 0$, yields the corresponding identity involving the tangent and the [secant](../secant-and-cosecant/):

$$
1 + \tan^2(\theta) = \sec^2(\theta)
$$

An analogous division by $\sin^2(\theta)$, under the assumption $\sin(\theta) \neq 0$, produces the identity involving the cotangent and the cosecant:

$$
1 + \cot^2(\theta) = \csc^2(\theta)
$$

The quotient identities relate tangent and cotangent to the ratio of sine and cosine. They follow directly from the definitions of the four functions on the unit circle:

$$
\begin{align}
&\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)} \\[6pt]
&\cot(\theta) = \frac{\cos(\theta)}{\sin(\theta)}
\end{align}
$$

> The first identity is valid for $\cos(\theta) \neq 0$, the second for $\sin(\theta) \neq 0$. Together, the Pythagorean and quotient identities are sufficient to re-express any trigonometric expression in terms of sine and cosine alone, a reduction that is often the first step in the simplification of more elaborate formulas.

## Reference angles and reflections

The method of [reference angles](../identities-using-reference-angles/), sometimes called the method of reflections, is a family of identities that allow one to express a trigonometric function of a non-acute angle in terms of the corresponding acute angle in the first quadrant of the Cartesian plane. Any trigonometric function, whether [sine](../sine-and-cosine/), [cosine](../sine-and-cosine/), [tangent](../tangent-and-cotangent/), or [cotangent](../tangent-and-cotangent/), with an argument of the form:

$$
\frac{\pi}{2} \pm \alpha, \quad \pi \pm \alpha, \quad \frac{3\pi}{2} \pm \alpha, \quad 2\pi - \alpha
$$

can be rewritten as a function of the acute angle $\alpha$, with an appropriate adjustment of the sign determined by the quadrant in which the angle lies. Consider the angle:

$$
\frac{\pi}{2} + \alpha
$$

In Cartesian coordinates, this angle lies in the second quadrant. 

![IMG. 1](svg/trigonometric-identities-1.svg)

A direct geometric analysis of the corresponding point on the [unit circle](../unit-circle/) yields the following two identities:

$$
\begin{align}
&\sin\left(\frac{\pi}{2} + \alpha\right) = \cos\alpha \\[6pt]
&\cos\left(\frac{\pi}{2} + \alpha\right) = -\sin\alpha
\end{align}
$$

The vertical segment associated with the sine of $\alpha$ in the first quadrant has the same length as the horizontal segment associated with the cosine of $\frac{\pi}{2} + \alpha$ in the second quadrant, while the sign of the cosine becomes negative because the second quadrant lies to the left of the vertical axis. The same procedure applied to every angle of the form listed above produces a full catalogue of reduction formulas, discussed in detail in the page on [reduction formulas and reference angles](../reduction-formulas-and-reference-angles/).

## Sum and difference

The sum and difference formulas express a trigonometric function of the sum or difference of two angles as a combination of the trigonometric functions of the individual angles. For sine and cosine the following identities hold:

$$
\begin{align}
&\sin(a + b) = \sin(a)\cos(b) + \cos(a)\sin(b) \\[6pt]
&\sin(a - b) = \sin(a)\cos(b) - \cos(a)\sin(b) \\[6pt]
&\cos(a + b) = \cos(a)\cos(b) - \sin(a)\sin(b) \\[6pt]
&\cos(a - b) = \cos(a)\cos(b) + \sin(a)\sin(b)
\end{align}
$$

The analogous identities for tangent and cotangent follow by taking the ratio of the corresponding sine and cosine formulas, provided the denominators do not vanish:

$$
\begin{align}
&\tan(a + b) = \frac{\tan(a) + \tan(b)}{1 - \tan(a)\tan(b)} \\[6pt]
&\tan(a - b) = \frac{\tan(a) - \tan(b)}{1 + \tan(a)\tan(b)} \\[6pt]
&\cot(a + b) = \frac{\cot(a)\cot(b) - 1}{\cot(a) + \cot(b)} \\[6pt]
&\cot(a - b) = \frac{\cot(a)\cot(b) + 1}{\cot(b) - \cot(a)}
\end{align}
$$

> These identities form the backbone of the entire body of trigonometric identities. The double-angle, half-angle, and prosthaphaeresis formulas are all derived from them through appropriate substitutions or algebraic manipulations.

## Double-angle

The double-angle formulas express the trigonometric functions of an angle $2\theta$ in terms of the trigonometric functions of $\theta$. For sine and cosine the following identities hold:

$$
\begin{align}
&\sin(2\theta) = 2\sin(\theta)\cos(\theta) \\[6pt]
&\cos(2\theta) = \cos^2(\theta) - \sin^2(\theta)
\end{align}
$$

The cosine double-angle formula admits two equivalent forms obtained by applying the [Pythagorean identity](../pythagorean-identity/) $\sin^2\theta + \cos^2\theta = 1$:

$$
\begin{align}
&\cos(2\theta) = 1 - 2\sin^2(\theta) \\[6pt]
&\cos(2\theta) = 2\cos^2(\theta) - 1
\end{align}
$$

The corresponding identities for tangent and cotangent are:

$$
\begin{align}
&\tan(2\theta) = \frac{2\tan(\theta)}{1 - \tan^2(\theta)} \\[6pt]
&\cot(2\theta) = \frac{\cot^2(\theta) - 1}{2\cot(\theta)}
\end{align}
$$

The derivation of the sine double-angle formula proceeds from the sum identity for the sine:

$$
\sin(a + b) = \sin(a)\cos(b) + \cos(a)\sin(b)
$$

Setting $a = b = \theta$, the left-hand side becomes $\sin(2\theta)$ and the right-hand side reduces to two identical terms:

$$
\sin(2\theta) = \sin(\theta)\cos(\theta) + \cos(\theta)\sin(\theta)
$$

Combining the two identical terms on the right gives the final result:

$$
\sin(2\theta) = 2\sin(\theta)\cos(\theta)
$$

The same reasoning applied to the sum identity for the cosine, with $a = b = \theta$, yields the double-angle formula for the cosine.

## Example

Consider the [integral](../indefinite-integrals/):

$$
\int \frac{1 - \cos(2\theta)}{2}\ d\theta
$$

The integrand contains a cosine of a doubled angle, which makes a direct computation awkward. The double-angle identity $\cos(2\theta) = 1 - 2\sin^2(\theta)$ allows the numerator to be rewritten as:

$$
1 - \cos(2\theta) = 1 - \left(1 - 2\sin^2(\theta)\right) = 2\sin^2(\theta)
$$

Substituting this result in the original expression transforms the integrand into a single [power](../powers/) of the sine:

$$
\int \frac{2\sin^2(\theta)}{2}\ d\theta = \int \sin^2(\theta)\ d\theta
$$

The identity has reduced the problem to the integration of $\sin^2(\theta)$, which is a standard form. The same double-angle identity can now be applied in the opposite direction to linearise the square, writing:

$$\sin^2(\theta) = \frac{1 - \cos(2\theta)}{2}$$

The integral becomes elementary:

$$\int \sin^2(\theta)\ d\theta = \frac{\theta}{2} - \frac{\sin(2\theta)}{4} + c$$

> The integral, which at first sight required a non-trivial technique, has been reduced to a sum of elementary antiderivatives through a single trigonometric identity.

## Triple-angle formulas

The triple-angle formulas extend the construction of the double-angle identities to the case in which the argument is tripled. They express the trigonometric functions of the angle $3\theta$ as [polynomial](../polynomials/) expressions in the corresponding functions of $\theta$. For sine and cosine the identities are:

$$
\begin{align}
&\sin(3\theta) = 3\sin(\theta) - 4\sin^3(\theta) \\[6pt]
&\cos(3\theta) = 4\cos^3(\theta) - 3\cos(\theta)
\end{align}
$$

The corresponding identity for the tangent takes the rational form:

$$
\tan(3\theta) = \frac{3\tan(\theta) - \tan^3(\theta)}{1 - 3\tan^2(\theta)}
$$

The derivation rests on the decomposition $3\theta = 2\theta + \theta$ together with the repeated application of the sum identity. The sine of the sum gives:

$$
\sin(3\theta) = \sin(2\theta)\cos(\theta) + \cos(2\theta)\sin(\theta)
$$

Substituting the double-angle expressions $\sin(2\theta) = 2\sin(\theta)\cos(\theta)$ and $\cos(2\theta) = 1 - 2\sin^2(\theta)$ produces:

$$
\sin(3\theta) = 2\sin(\theta)\cos^2(\theta) + \sin(\theta) - 2\sin^3(\theta)
$$

The Pythagorean identity allows the replacement of $\cos^2(\theta)$ with $1 - \sin^2(\theta)$, and a collection of the resulting terms leads to the final polynomial form $3\sin(\theta) - 4\sin^3(\theta)$. The identical procedure applied to $\cos(3\theta) = \cos(2\theta + \theta)$ yields the cosine identity, and the tangent identity follows on dividing the sine expansion by the cosine expansion and rewriting the quotient as a rational function of $\tan(\theta)$.

> The triple-angle formulas are the simplest non-trivial instance of a more general pattern: every trigonometric function of $n\theta$ can be expressed as a polynomial in $\sin(\theta)$ and $\cos(\theta)$. For $n = 3$ the polynomial form is particularly compact, and it provides, among other things, the trigonometric resolution of certain irreducible cubic equations and the exact values of trigonometric functions at angles such as $\frac{\pi}{5}$ and $\frac{\pi}{9}$.

## Half-angle formulas

The half-angle formulas express the trigonometric functions of $\frac{\theta}{2}$ in terms of the trigonometric functions of $\theta$. For sine and cosine the following identities hold:

$$
\begin{align}
&\sin\left(\frac{\theta}{2}\right) = \pm\sqrt{\frac{1 - \cos(\theta)}{2}} \\[6pt]
&\cos\left(\frac{\theta}{2}\right) = \pm\sqrt{\frac{1 + \cos(\theta)}{2}}
\end{align}
$$

The sign on the right-hand side is determined by the quadrant in which the half-angle $\frac{\theta}{2}$ lies, and must be selected according to the geometric position of the angle on the [unit circle](../unit-circle/).

The half-angle formulas for tangent and cotangent can be written either in radical form or in rational form. The rational form is generally preferred because it avoids the ambiguity of the sign:

$$
\begin{align}
&\tan\left(\frac{\theta}{2}\right) = \frac{\sin(\theta)}{1 + \cos(\theta)} = \frac{1 - \cos(\theta)}{\sin(\theta)} \\[6pt]
&\cot\left(\frac{\theta}{2}\right) = \frac{1 + \cos(\theta)}{\sin(\theta)} = \frac{\sin(\theta)}{1 - \cos(\theta)}
\end{align}
$$

> The derivation of the half-angle formulas follows from the two alternative forms of the cosine double-angle identity. Writing $\cos(\theta) = 1 - 2\sin^2(\theta/2)$ and solving for $\sin(\theta/2)$ yields the half-angle formula for the sine; the analogous manipulation on $\cos(\theta) = 2\cos^2(\theta/2) - 1$ produces the half-angle formula for the cosine.

## Parametric formulas

The parametric formulas express the trigonometric functions of an angle $\theta$ in terms of the single auxiliary variable:

$$
t = \tan\left(\frac{\theta}{2}\right)
$$

Using this substitution, sine and cosine take the rational form:

$$
\begin{align}
&\sin(\theta) = \frac{2t}{1 + t^2} \\[6pt]
&\cos(\theta) = \frac{1 - t^2}{1 + t^2}
\end{align}
$$

The corresponding expressions for tangent and cotangent are:

$$
\begin{align}
&\tan(\theta) = \frac{2t}{1 - t^2} \\[6pt]
&\cot(\theta) = \frac{1 - t^2}{2t}
\end{align}
$$

The substitution is valid whenever $\theta \neq \pi + 2k\pi$ with $k \in \mathbb{Z}$, since at those values the tangent of the half-angle is undefined. The practical importance of the parametric formulas lies in their ability to reduce a trigonometric expression to a rational function of a single algebraic variable, a property widely exploited in the integration of rational functions of sine and cosine through the Weierstrass substitution.

## Werner's formulas

Werner's formulas transform the product of two trigonometric functions into a sum or difference of trigonometric functions. The three identities are:

$$
\begin{align}
&\sin(\alpha)\sin(\beta) = \frac{1}{2}[\cos(\alpha - \beta) - \cos(\alpha + \beta)] \\[6pt]
&\cos(\alpha)\cos(\beta) = \frac{1}{2}[\cos(\alpha + \beta) + \cos(\alpha - \beta)] \\[6pt]
&\sin(\alpha)\cos(\beta) = \frac{1}{2}[\sin(\alpha + \beta) + \sin(\alpha - \beta)]
\end{align}
$$

Each identity follows by adding or subtracting the appropriate pair of sum and difference formulas. For example, adding the expansions of $\cos(\alpha - \beta)$ and $\cos(\alpha + \beta)$ cancels the sine terms and leaves twice the product $\cos(\alpha)\cos(\beta)$, from which the second identity is immediate. These formulas are particularly useful in the integration of products of trigonometric functions and in the analysis of the interference of waves in physics, where the product of two sinusoidal signals is naturally decomposed into components at the sum and difference frequencies.

## Prosthaphaeresis formulas

The prosthaphaeresis formulas perform the transformation opposite to Werner's: they rewrite a sum or difference of sines or cosines as a product of trigonometric functions. The four identities are:

$$
\begin{align}
&\sin(p) + \sin(q) = 2\sin\left(\frac{p+q}{2}\right)\cos\left(\frac{p-q}{2}\right) \\[6pt]
&\sin(p) - \sin(q) = 2\cos\left(\frac{p+q}{2}\right)\sin\left(\frac{p-q}{2}\right) \\[6pt]
&\cos(p) + \cos(q) = 2\cos\left(\frac{p+q}{2}\right)\cos\left(\frac{p-q}{2}\right) \\[6pt]
&\cos(p) - \cos(q) = -2\sin\left(\frac{p+q}{2}\right)\sin\left(\frac{p-q}{2}\right)
\end{align}
$$

These identities are derived from Werner's formulas by the substitution:

$$
\alpha = \frac{p+q}{2},\quad \beta = \frac{p-q}{2}
$$

so that $p = \alpha + \beta$ and $q = \alpha - \beta$. Replacing these values in Werner's identities and multiplying both sides by two yields the prosthaphaeresis formulas. Their name derives from the Greek words for addition and subtraction, and reflects the historical role they played in pre-logarithmic astronomy, where they were used to convert multiplications into additions and thus simplify numerical computation.

## Linear combination of sine and cosine

A [linear combination](../linear-combinations/) of sine and cosine sharing the same argument can be rewritten as a single sinusoid with shifted phase and adjusted amplitude. Given two real coefficients $a$ and $b$, not both zero, the following identity holds for every $\theta$:

$$
a\sin(\theta) + b\cos(\theta) = R\sin(\theta + \varphi)
$$

The amplitude $R$ and the phase $\varphi$ are determined by the relations:

$$
R = \sqrt{a^2 + b^2}, \quad \cos(\varphi) = \frac{a}{R}, \quad \sin(\varphi) = \frac{b}{R}
$$

The derivation proceeds from the sum formula for the sine. Expanding the right-hand side yields:

$$
R\sin(\theta + \varphi) = R\cos(\varphi)\sin(\theta) + R\sin(\varphi)\cos(\theta)
$$

Matching the coefficients of $\sin(\theta)$ and $\cos(\theta)$ with those of the original combination produces the system $R\cos(\varphi) = a$ and $R\sin(\varphi) = b$. Squaring the two equations and adding them isolates the amplitude $R = \sqrt{a^2 + b^2}$, while the ratio of the second to the first determines the phase $\varphi$ up to the appropriate quadrant, which is fixed by the individual signs of $a$ and $b$.

An equivalent representation in terms of a single cosine is sometimes more convenient:

$$
a\sin(\theta) + b\cos(\theta) = R\cos(\theta - \psi)
$$

In this form the phase satisfies $\cos(\psi) = b/R$ and $\sin(\psi) = a/R$. The two representations carry the same information and differ only in the choice of reference function and in the position of the resulting phase.

The practical importance of this identity is twofold. Because the sine function is bounded between $-1$ and $1$, the expression $a\sin(\theta) + b\cos(\theta)$ attains its maximum value $\sqrt{a^2 + b^2}$ at the angles for which $\sin(\theta + \varphi) = 1$, and its minimum value $-\sqrt{a^2 + b^2}$ at those for which $\sin(\theta + \varphi) = -1$. A trigonometric equation of the form $a\sin(\theta) + b\cos(\theta) = c$ reduces, through this identity, to the elementary equation:

$$
\sin(\theta + \varphi) = \frac{c}{R}
$$

This auxiliary equation admits solutions whenever $|c| \leq R$, and the original equation inherits the same solvability condition. The construction also underlies the representation of a harmonic oscillation as the resultant of two perpendicular components, a description that appears throughout the analysis of vibrating systems and alternating signals.

> The construction extends without modification to any linear combination of sines and cosines that share a common argument. When the trigonometric arguments are distinct, the identity no longer applies, and the appropriate transformation belongs instead to the family of Werner's or prosthaphaeresis formulas.
