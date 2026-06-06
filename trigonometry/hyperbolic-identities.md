---
title: Hyperbolic Identities
source: https://algebrica.org/hyperbolic-identities/
license: CC BY-NC 4.0
tags:
  - hyperbolic-functions
  - hyperbolic-identities
  - trigonometry
---

## Introduction

A hyperbolic identity is an equation involving hyperbolic functions that holds for every admissible value of the variables. Unlike a hyperbolic equation, which is solved for a specific set of arguments, an identity is an equality that holds throughout the common domain of the functions involved.

The study of these identities organises the algebraic relationships that tie [hyperbolic sine and cosine](../hyperbolic-sine-and-cosine/), [hyperbolic tangent and cotangent](../hyperbolic-tangent-and-cotangent/) together, and provides the tools needed to manipulate hyperbolic expressions into equivalent forms that are easier to evaluate, [differentiate](../derivatives/), [integrate](../indefinite-integrals/), or interpret geometrically.

The identities presented below are grouped into families according to the type of transformation they perform. Some express a [function](../functions/) of a modified argument in terms of the original argument, others convert products into sums or sums into products, and others still reduce a general argument to a parametric variable.

Each group plays a distinct role in the resolution of hyperbolic equations, in the simplification of expressions, and in the broader apparatus of calculus.

## Fundamental identities

Before examining the transformations relating hyperbolic functions with different arguments, it is useful to recall the elementary identities that connect the six hyperbolic functions at a single argument. These identities descend directly from the definitions of the equilateral [hyperbola](../hyperbola/) and from the exponential representations of $\sinh(x)$ and $\cosh(x)$, and they form the algebraic foundation on which every subsequent identity is built. The fundamental hyperbolic identity expresses the constraint that the coordinates of any point on the right branch of the unit equilateral hyperbola satisfy the equation of the curve itself:

$$
\cosh^2(x) - \sinh^2(x) = 1
$$

Dividing both sides of this identity by $\cosh^2(x)$, which never vanishes, yields the corresponding identity involving the hyperbolic tangent and the hyperbolic secant:

$$
1 - \tanh^2(x) = \operatorname{sech}^2(x)
$$

An analogous division by $\sinh^2(x)$, under the assumption $\sinh(x) \neq 0$, produces the identity involving the hyperbolic cotangent and the hyperbolic cosecant:

$$
\coth^2(x) - 1 = \operatorname{csch}^2(x)
$$

The quotient identities relate hyperbolic tangent and cotangent to the ratio of hyperbolic sine and cosine. They follow directly from the definitions of the four functions:

$$
\begin{align}
&\tanh(x) = \frac{\sinh(x)}{\cosh(x)} \\[6pt]
&\coth(x) = \frac{\cosh(x)}{\sinh(x)}
\end{align}
$$

> The first identity is valid for every real $x$, since $\cosh(x) \geq 1$; the second requires $\sinh(x) \neq 0$, that is $x \neq 0$. Together, the fundamental and quotient identities are sufficient to re-express any hyperbolic expression in terms of hyperbolic sine and cosine alone, a reduction that is often the first step in the simplification of more elaborate formulas.

## Parity and symmetry

Whereas the trigonometric functions admit a rich family of [reduction formulas](../reduction-formulas-and-reference-angles/) based on the quadrants of the unit circle, the hyperbolic functions, defined on the single right branch of the equilateral hyperbola, possess a simpler symmetry structure governed entirely by the parity of their arguments. The hyperbolic sine is an odd function, while the hyperbolic cosine is even:

$$
\begin{align}
&\sinh(-x) = -\sinh(x) \\[6pt]
&\cosh(-x) = \cosh(x)
\end{align}
$$

The parity of $\sinh$ and $\cosh$ is inherited by the remaining hyperbolic functions. The hyperbolic tangent and cotangent, being quotients of an odd and an even function, are themselves odd:

$$
\begin{align}
&\tanh(-x) = -\tanh(x) \\[6pt]
&\coth(-x) = -\coth(x)
\end{align}
$$

while the hyperbolic secant inherits the parity of the cosine and the hyperbolic cosecant the parity of the sine:

$$
\begin{align}
&\operatorname{sech}(-x) = \operatorname{sech}(x) \\[6pt]
&\operatorname{csch}(-x) = -\operatorname{csch}(x)
\end{align}
$$

These identities follow immediately from the exponential definitions $\sinh(x) = (e^{x} - e^{-x})/2$ and $\cosh(x) = (e^{x} + e^{-x})/2$, since the substitution $x \mapsto -x$ exchanges the two exponentials and leaves the cosine unchanged while reversing the sign of the sine. The absence of further reduction formulas reflects the topological difference between the circle, which is closed, and the hyperbola, whose branch extends to infinity in both directions.

## Sum and difference

The sum and difference formulas express a hyperbolic function of the sum or difference of two arguments as a combination of the hyperbolic functions of the individual arguments. For sine and cosine the following identities hold:

$$
\begin{align}
&\sinh(a + b) = \sinh(a)\cosh(b) + \cosh(a)\sinh(b) \\[6pt]
&\sinh(a - b) = \sinh(a)\cosh(b) - \cosh(a)\sinh(b) \\[6pt]
&\cosh(a + b) = \cosh(a)\cosh(b) + \sinh(a)\sinh(b) \\[6pt]
&\cosh(a - b) = \cosh(a)\cosh(b) - \sinh(a)\sinh(b)
\end{align}
$$

The analogous identities for hyperbolic tangent and cotangent follow by taking the ratio of the corresponding sine and cosine formulas, provided the denominators do not vanish:

$$
\begin{align}
&\tanh(a + b) = \frac{\tanh(a) + \tanh(b)}{1 + \tanh(a)\tanh(b)} \\[6pt]
&\tanh(a - b) = \frac{\tanh(a) - \tanh(b)}{1 - \tanh(a)\tanh(b)} \\[6pt]
&\coth(a + b) = \frac{\coth(a)\coth(b) + 1}{\coth(a) + \coth(b)} \\[6pt]
&\coth(a - b) = \frac{\coth(a)\coth(b) - 1}{\coth(b) - \coth(a)}
\end{align}
$$

> These identities form the backbone of the entire body of hyperbolic identities. The double-argument, half-argument, and prosthaphaeresis-type formulas are all derived from them through appropriate substitutions or algebraic manipulations. Compared with their circular counterparts, the cosine sum formula carries a plus sign rather than a minus, a difference that originates in the change of sign in the fundamental identity.

## Double-argument

The double-argument formulas express the hyperbolic functions of an argument $2x$ in terms of the hyperbolic functions of $x$. For sine and cosine the following identities hold:

$$
\begin{align}
&\sinh(2x) = 2\sinh(x)\cosh(x) \\[6pt]
&\cosh(2x) = \cosh^2(x) + \sinh^2(x)
\end{align}
$$

The hyperbolic cosine double-argument formula admits two equivalent forms obtained by applying the fundamental identity $\cosh^2(x) - \sinh^2(x) = 1$:

$$
\begin{align}
&\cosh(2x) = 1 + 2\sinh^2(x) \\[6pt]
&\cosh(2x) = 2\cosh^2(x) - 1
\end{align}
$$

The corresponding identities for hyperbolic tangent and cotangent are:

$$
\begin{align}
&\tanh(2x) = \frac{2\tanh(x)}{1 + \tanh^2(x)} \\[6pt]
&\coth(2x) = \frac{\coth^2(x) + 1}{2\coth(x)}
\end{align}
$$

The derivation of the hyperbolic sine double-argument formula proceeds from the sum identity for the sine:

$$
\sinh(a + b) = \sinh(a)\cosh(b) + \cosh(a)\sinh(b)
$$

Setting $a = b = x$, the left-hand side becomes $\sinh(2x)$ and the right-hand side reduces to two identical terms:

$$
\sinh(2x) = \sinh(x)\cosh(x) + \cosh(x)\sinh(x)
$$

Combining the two identical terms on the right gives the final result:

$$
\sinh(2x) = 2\sinh(x)\cosh(x)
$$

The same reasoning applied to the sum identity for the cosine, with $a = b = x$, yields the double-argument formula for the hyperbolic cosine.

## Example

Consider the [integral](../indefinite-integrals/):

$$
\int \frac{\cosh(2x) - 1}{2}\ dx
$$

The integrand contains a hyperbolic cosine of a doubled argument, which makes a direct computation awkward. The double-argument identity $\cosh(2x) = 1 + 2\sinh^2(x)$ allows the numerator to be rewritten as:

$$
\cosh(2x) - 1 = \left(1 + 2\sinh^2(x)\right) - 1 = 2\sinh^2(x)
$$

Substituting this result in the original expression transforms the integrand into a single [power](../powers/) of the hyperbolic sine:

$$
\int \frac{2\sinh^2(x)}{2}\ dx = \int \sinh^2(x)\ dx
$$

The identity has reduced the problem to the integration of $\sinh^2(x)$, which is a standard form. The same double-argument identity can now be applied in the opposite direction to linearise the square, writing:

$$\sinh^2(x) = \frac{\cosh(2x) - 1}{2}$$

The integral becomes elementary:

$$\int \sinh^2(x)\ dx = \frac{\sinh(2x)}{4} - \frac{x}{2} + c$$

> The integral, which at first sight required a non-trivial technique, has been reduced to a sum of elementary antiderivatives through a single hyperbolic identity.

## Triple-argument formulas

The triple-argument formulas extend the construction of the double-argument identities to the case in which the argument is tripled. They express the hyperbolic functions of the argument $3x$ as [polynomial](../polynomials/) expressions in the corresponding functions of $x$. For sine and cosine the identities are:

$$
\begin{align}
&\sinh(3x) = 3\sinh(x) + 4\sinh^3(x) \\[6pt]
&\cosh(3x) = 4\cosh^3(x) - 3\cosh(x)
\end{align}
$$

The corresponding identity for the hyperbolic tangent takes the rational form:

$$
\tanh(3x) = \frac{3\tanh(x) + \tanh^3(x)}{1 + 3\tanh^2(x)}
$$

The derivation rests on the decomposition $3x = 2x + x$ together with the repeated application of the sum identity. The hyperbolic sine of the sum gives:

$$
\sinh(3x) = \sinh(2x)\cosh(x) + \cosh(2x)\sinh(x)
$$

Substituting the double-argument expressions $\sinh(2x) = 2\sinh(x)\cosh(x)$ and $\cosh(2x) = 1 + 2\sinh^2(x)$ produces:

$$
\sinh(3x) = 2\sinh(x)\cosh^2(x) + \sinh(x) + 2\sinh^3(x)
$$

The fundamental identity allows the replacement of $\cosh^2(x)$ with $1 + \sinh^2(x)$, and a collection of the resulting terms leads to the final polynomial form $3\sinh(x) + 4\sinh^3(x)$. The identical procedure applied to $\cosh(3x) = \cosh(2x + x)$ yields the cosine identity, and the tangent identity follows on dividing the sine expansion by the cosine expansion and rewriting the quotient as a rational function of $\tanh(x)$.

> The triple-argument formulas are the simplest non-trivial instance of a more general pattern: every hyperbolic function of $nx$ can be expressed as a polynomial in $\sinh(x)$ and $\cosh(x)$. For $n = 3$ the polynomial form is particularly compact, and it provides, among other things, the hyperbolic resolution of certain irreducible cubic equations through Cardano's formula.

## Half-argument formulas

The half-argument formulas express the hyperbolic functions of $\frac{x}{2}$ in terms of the hyperbolic functions of $x$. For sine and cosine the following identities hold:

$$
\begin{align}
&\sinh\left(\frac{x}{2}\right) = \pm\sqrt{\frac{\cosh(x) - 1}{2}} \\[6pt]
&\cosh\left(\frac{x}{2}\right) = \sqrt{\frac{\cosh(x) + 1}{2}}
\end{align}
$$

The sign on the right-hand side of the hyperbolic sine identity is determined by the sign of $x$, since $\sinh$ is an odd function; the hyperbolic cosine, being everywhere positive, requires no sign ambiguity.

The half-argument formulas for hyperbolic tangent and cotangent can be written either in radical form or in rational form. The rational form is generally preferred because it avoids the ambiguity of the sign:

$$
\begin{align}
&\tanh\left(\frac{x}{2}\right) = \frac{\sinh(x)}{\cosh(x) + 1} = \frac{\cosh(x) - 1}{\sinh(x)} \\[6pt]
&\coth\left(\frac{x}{2}\right) = \frac{\cosh(x) + 1}{\sinh(x)} = \frac{\sinh(x)}{\cosh(x) - 1}
\end{align}
$$

> The derivation of the half-argument formulas follows from the two alternative forms of the cosine double-argument identity. Writing $\cosh(x) = 1 + 2\sinh^2(x/2)$ and solving for $\sinh(x/2)$ yields the half-argument formula for the hyperbolic sine; the analogous manipulation on $\cosh(x) = 2\cosh^2(x/2) - 1$ produces the half-argument formula for the hyperbolic cosine.

## Parametric formulas

The parametric formulas express the hyperbolic functions of an argument $x$ in terms of the single auxiliary variable:

$$
t = \tanh\left(\frac{x}{2}\right)
$$

Using this substitution, hyperbolic sine and cosine take the rational form:

$$
\begin{align}
&\sinh(x) = \frac{2t}{1 - t^2} \\[6pt]
&\cosh(x) = \frac{1 + t^2}{1 - t^2}
\end{align}
$$

The corresponding expressions for hyperbolic tangent and cotangent are:

$$
\begin{align}
&\tanh(x) = \frac{2t}{1 + t^2} \\[6pt]
&\coth(x) = \frac{1 + t^2}{2t}
\end{align}
$$

The substitution is valid for every real $x$, since $|t| = |\tanh(x/2)| < 1$ and the denominator $1 - t^2$ never vanishes within the range of the substitution. The practical importance of the parametric formulas lies in their ability to reduce a hyperbolic expression to a rational function of a single algebraic variable, a property widely exploited in the integration of rational functions of hyperbolic sine and cosine, in direct analogy with the Weierstrass substitution for trigonometric integrals.

## Werner-type formulas

The Werner-type formulas transform the product of two hyperbolic functions into a sum or difference of hyperbolic functions. The three identities are:

$$
\begin{align}
&\sinh(\alpha)\sinh(\beta) = \frac{1}{2}[\cosh(\alpha + \beta) - \cosh(\alpha - \beta)] \\[6pt]
&\cosh(\alpha)\cosh(\beta) = \frac{1}{2}[\cosh(\alpha + \beta) + \cosh(\alpha - \beta)] \\[6pt]
&\sinh(\alpha)\cosh(\beta) = \frac{1}{2}[\sinh(\alpha + \beta) + \sinh(\alpha - \beta)]
\end{align}
$$

Each identity follows by adding or subtracting the appropriate pair of sum and difference formulas. For example, adding the expansions of $\cosh(\alpha + \beta)$ and $\cosh(\alpha - \beta)$ cancels the hyperbolic sine terms and leaves twice the product $\cosh(\alpha)\cosh(\beta)$, from which the second identity is immediate. These formulas are particularly useful in the integration of products of hyperbolic functions and in the analysis of damped oscillations and exponential growth, where the product of two hyperbolic signals is naturally decomposed into components at the sum and difference arguments.

## Prosthaphaeresis-type formulas

The prosthaphaeresis-type formulas perform the transformation opposite to Werner's: they rewrite a sum or difference of hyperbolic sines or cosines as a product of hyperbolic functions. The four identities are:

$$
\begin{align}
&\sinh(p) + \sinh(q) = 2\sinh\left(\frac{p+q}{2}\right)\cosh\left(\frac{p-q}{2}\right) \\[6pt]
&\sinh(p) - \sinh(q) = 2\cosh\left(\frac{p+q}{2}\right)\sinh\left(\frac{p-q}{2}\right) \\[6pt]
&\cosh(p) + \cosh(q) = 2\cosh\left(\frac{p+q}{2}\right)\cosh\left(\frac{p-q}{2}\right) \\[6pt]
&\cosh(p) - \cosh(q) = 2\sinh\left(\frac{p+q}{2}\right)\sinh\left(\frac{p-q}{2}\right)
\end{align}
$$

These identities are derived from the Werner-type formulas by the substitution:

$$
\alpha = \frac{p+q}{2},\quad \beta = \frac{p-q}{2}
$$

so that $p = \alpha + \beta$ and $q = \alpha - \beta$. Replacing these values in the Werner-type identities and multiplying both sides by two yields the prosthaphaeresis-type formulas. Their structure mirrors that of their circular counterparts, with the only difference appearing in the cosine subtraction formula, where the absence of a leading minus sign reflects the inversion of sign in the fundamental hyperbolic identity.

## Linear combination of hyperbolic sine and cosine

A [linear combination](../linear-combinations/) of hyperbolic sine and cosine sharing the same argument can be rewritten as a single hyperbolic function with shifted argument and adjusted amplitude, provided the coefficients satisfy a suitable condition. Given two real coefficients $a$ and $b$ with $|a| > |b|$, the following identity holds for every $x$:

$$
a\sinh(x) + b\cosh(x) = R\sinh(x + \varphi)
$$

The amplitude $R$ and the shift $\varphi$ are determined by the relations:

$$
R = \sqrt{a^2 - b^2} \qquad \cosh(\varphi) = \frac{a}{R} \qquad \sinh(\varphi) = \frac{b}{R}
$$

The derivation proceeds from the sum formula for the hyperbolic sine. Expanding the right-hand side yields:

$$
R\sinh(x + \varphi) = R\cosh(\varphi)\sinh(x) + R\sinh(\varphi)\cosh(x)
$$

Matching the coefficients of $\sinh(x)$ and $\cosh(x)$ with those of the original combination produces the system $R\cosh(\varphi) = a$ and $R\sinh(\varphi) = b$. Squaring the two equations and subtracting them isolates the amplitude $R = \sqrt{a^2 - b^2}$, while the ratio of the second to the first determines the shift $\varphi$ uniquely, since the hyperbolic tangent is a bijection from the real line onto $(-1, 1)$.

When the coefficients satisfy $|b| > |a|$, the analogous representation uses a single hyperbolic cosine:

$$
a\sinh(x) + b\cosh(x) = R\cosh(x + \psi)
$$

In this form $R = \sqrt{b^2 - a^2}$ and the shift satisfies $\cosh(\psi) = b/R$ and $\sinh(\psi) = a/R$. The two representations carry the same information and apply in complementary regimes determined by the relative magnitudes of the coefficients.

The practical importance of this identity is twofold. Because the hyperbolic sine is a strictly increasing bijection from the real line onto itself, the expression $a\sinh(x) + b\cosh(x)$ attains every real value exactly once when $|a| > |b|$, and a hyperbolic equation of the form $a\sinh(x) + b\cosh(x) = c$ reduces, through this identity, to the elementary equation:

$$
\sinh(x + \varphi) = \frac{c}{R}
$$

This auxiliary equation admits a unique solution for every real $c$ when $|a| > |b|$, while in the complementary case $|b| > |a|$ the cosine form yields solutions whenever $|c| \geq R$. The construction also underlies the representation of an exponentially varying quantity as the resultant of two hyperbolic components, a description that appears throughout the analysis of catenary curves, relativistic rapidities, and the propagation of waves in dispersive media.

> The construction extends without modification to any linear combination of hyperbolic sines and cosines that share a common argument. When the hyperbolic arguments are distinct, the identity no longer applies, and the appropriate transformation belongs instead to the family of Werner-type or prosthaphaeresis-type formulas.
