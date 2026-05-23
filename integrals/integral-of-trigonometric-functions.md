---
title: Integral of Trigonometric Functions
source: https://algebrica.org/integral-of-trigonometric-functions/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - hyperbolic-functions
  - indefinite-integral
  - integration
  - integration-by-substitution
  - power-reduction
  - pythagorean-identity
  - trigonometric-functions
  - trigonometric-identities
---
## Standard antiderivatives

The individual [function](../functions/) pages, such as those for [sine](../sine-function/), [cosine](../cosine-function/), [tangent](../tangent-function/), and [cotangent](../cotangent-function/), state the corresponding antiderivatives alongside the other defining properties. These integrals are straightforward to compute since they appear constantly in problem solving. The list below collects the antiderivatives of all the main trigonometric functions, providing an immediate overall view of the essential results. 

The final six entries record the corresponding [hyperbolic](../hyperbolic-functions/) integrals, included for completeness because they arise from the same techniques and are often needed alongside their circular counterparts.

[class="table-1"]

|     |                                                                                    |     |
| --- | ---------------------------------------------------------------------------------- | --- |
| 1.  | $$\int \sin x \ dx = -\cos x + c$$                                                 |     |
| 2.  | $$\int \cos x \ dx = \sin x + c$$                                                  |     |
| 3.  | $$\int \tan x \ dx = -\ln \mid \cos x \mid + c$$                                   |     |
| 4.  | $$\int \cot x \ dx = \ln \mid \sin x \mid + c$$                                    |     |
| 5.  | $$\int \sec x \ dx = \ln \mid \sec x + \tan x \mid + c$$                           |     |
| 6.  | $$\int \csc x \ dx = \ln \mid \csc x - \cot x  \mid + c$$                          |     |
| 7.  | $$\int \sinh x \ dx = \cosh x + c$$                                                |     |
| 8.  | $$\int \cosh x \ dx = \sinh x + c$$                                                |     |
| 9.  | $$\int \tanh x \ dx = \ln \mid \cosh x \mid + c$$                                  |     |
| 10. | $$\int \coth x \ dx = \ln \mid \sinh x \mid + c$$                                  |     |
| 11. | $$\int \operatorname{sech} x \ dx = 2 \arctan\!\left(\tanh\frac{x}{2}\right) + c$$ |     |
| 12. | $$\int \operatorname{csch} x \ dx = \ln\left\|\tanh\frac{x}{2}\right\| + c$$       |     |

[/class]

> The symbol $c$ denotes the constant of integration, included to represent the entire family of antiderivatives associated with an [indefinite integral](../indefinite-integrals/). Each value of $c$ corresponds to a different primitive, and all of them share the same derivative.

## Integrals of trigonometric powers with $n$ even

A frequent case in which the antiderivative is not immediately accessible occurs when sine or cosine appears raised to an integer power:

$$\int \sin^{n} x \ dx \qquad \int \cos^{n} x \ dx$$

When the exponent $n$ is even, the integral is simplified by rewriting the squared trigonometric terms through the power-reduction identities:

$$\sin^{2} x = \frac{1 - \cos 2x}{2} \qquad \cos^{2} x = \frac{1 + \cos 2x}{2}$$

These identities lower the power of the function and make the integral accessible. They follow directly from two standard relationships. Starting from the [Pythagorean identity](../pythagorean-identity/):

$$\sin^{2}x + \cos^{2}x = 1$$

and combining it with the [double-angle formula](../trigonometric-identities/):

$$\cos 2x = \cos^{2}x - \sin^{2}x$$

the expression $\cos 2x$ can be written entirely in terms of either $\cos^{2}x$ or $\sin^{2}x$. Replacing $\sin^{2}x$ with $1 - \cos^{2}x$ gives:

$$\cos 2x = \cos^{2}x - (1 - \cos^{2}x) = 2\cos^{2}x - 1$$

Solving this expression for $\cos^{2}x$ yields:

$$\cos^{2}x = \frac{1 + \cos 2x}{2}$$

A similar argument holds for $\sin^{2}x$. Substituting $\cos^{2}x = 1 - \sin^{2}x$ into the double-angle formula gives:

$$\cos 2x = (1 - \sin^{2}x) - \sin^{2}x = 1 - 2\sin^{2}x$$

Solving for $\sin^{2}x$:

$$\sin^{2}x = \frac{1 - \cos 2x}{2}$$

## Example 1

As an illustration of the method, consider the following integral:

$$\int 2\cos^{4}x \ dx$$

To handle the fourth power of the cosine, the starting point is the power-reduction identity:

$$\cos^{2}x = \frac{1 + \cos 2x}{2}$$

Applying this identity rewrites the integrand in a more manageable form:

$$
\begin{align}
\cos^{4}x &= \left(\frac{1 + \cos 2x}{2}\right)^{2} \\[6pt]
          &= \frac{1}{4}\left(1 + 2\cos 2x + \cos^{2} 2x\right)
\end{align}
$$

A residual power of cosine still remains, and is reduced through the same identity:

$$\cos^{2} 2x = \frac{1 + \cos 4x}{2}$$

Substituting this expression into the previous result:

$$
\begin{align}
\cos^{4}x &= \frac{1}{4}\left(1 + 2\cos 2x + \frac{1 + \cos 4x}{2}\right) \\[6pt]
          &= \frac{1}{4}\left(\frac{3}{2} + 2\cos 2x + \frac{1}{2}\cos 4x\right) \\[6pt]
          &= \frac{3}{8} + \frac{1}{2}\cos 2x + \frac{1}{8}\cos 4x
\end{align}
$$

Multiplying by $2$, as required by the original integral, gives:

$$2\cos^{4}x = \frac{3}{4} + \cos 2x + \frac{1}{4}\cos 4x$$

Integrating each term separately:

$$\int 2\cos^{4}x \ dx = \frac{3}{4}x + \frac{1}{2}\sin 2x + \frac{1}{16}\sin 4x + c$$

> The fourth power has therefore been reduced to a sum of elementary terms, each integrable on sight, which is the central advantage of the power-reduction approach when the exponent is even.

## Integrals of trigonometric powers with $n$ odd

When the exponent $n$ is odd, the method becomes more direct. One factor of the function whose power is odd is separated, and the remaining even power is rewritten through the Pythagorean identity. Writing $n = 2k + 1$, for sine this gives:

$$
\begin{align}
\int \sin^{n} x \ dx &= \int \sin x (\sin^{2}x)^{k} \ dx \\[6pt]
                     &= \int \sin x (1 - \cos^{2}x)^{k} \ dx
\end{align}
$$

The [substitution](../integration-by-substitution/):

$$u = \cos x \qquad du = -\sin x \ dx$$

transforms the integral into a [polynomial](../polynomials/) in $u$, which can then be integrated without difficulty. The procedure for an odd power of cosine is entirely analogous: one extracts a single factor $\cos x$ and rewrites the remaining even power using:

$$\cos^{2}x = 1 - \sin^{2}x$$

leading to the substitution $u = \sin x$. In both cases, isolating one factor reduces the integral to a polynomial form.

## Example 2

Consider the following integral:

$$\int \cos^{5}x \ dx$$

The exponent is odd, so the strategy is to isolate one factor of cosine and rewrite the remaining even [power](../powers/) using the Pythagorean identity:

$$\int \cos^{5}x \ dx = \int \cos^{4}x \cdot \cos x \ dx$$

The factor $\cos^{4}x$ is an even power, so it can be expressed in terms of $\sin^{2}x$:

$$\cos^{4}x = (\cos^{2}x)^{2} = (1 - \sin^{2}x)^{2}$$

The integral becomes:

$$\int (1 - \sin^{2}x)^{2} \cdot \cos x \ dx$$

The factor $\cos x \ dx$ is exactly the differential of $\sin x$, so set:

$$u = \sin x \qquad du = \cos x \ dx$$

The integral transforms into a polynomial in $u$:

$$\int (1 - u^{2})^{2} \ du$$

Expanding the square:

$$\int (1 - 2u^{2} + u^{4}) \ du$$

Each term integrates immediately:

$$u - \frac{2}{3}u^{3} + \frac{1}{5}u^{5} + c$$

Substituting back $u = \sin x$:

$$\int \cos^{5}x \ dx = \sin x - \frac{2}{3}\sin^{3}x + \frac{1}{5}\sin^{5}x + c$$

> The substitution resolved the integral cleanly because the isolated factor $\cos x$ was precisely the derivative of $u = \sin x$. Recognising this pattern is what reduces the odd-exponent case to a routine polynomial integration.

## Mixed powers of sine and cosine

A more general situation arises when sine and cosine appear together, in integrals of the form:

$$\int \sin^{m} x \cos^{n} x \ dx$$

The strategy depends on the parity of the exponents, and it combines the two methods already developed. When at least one of the exponents is odd, the odd-power technique applies directly. Suppose $n$ is odd: one isolates a factor of $\cos x$, converts the remaining even power of cosine into sine through $\cos^{2}x = 1 - \sin^{2}x$, and uses the substitution $u = \sin x$. If instead $m$ is odd, the symmetric procedure isolates a factor of $\sin x$ and substitutes $u = \cos x$. When both exponents are odd, either choice works.

When both $m$ and $n$ are even, no factor can be split off to serve as a differential. In this case the power-reduction identities are applied to every squared term:

$$\sin^{2} x = \frac{1 - \cos 2x}{2} \qquad \cos^{2} x = \frac{1 + \cos 2x}{2}$$

The identity $\sin x \cos x = \tfrac{1}{2}\sin 2x$ is frequently useful as well, since it lowers the combined degree in a single step. Repeated application reduces the integrand to a sum of terms of the form $\cos kx$, each of which integrates immediately, exactly as in Example 1.

## Example 3

Consider the following integral:

$$\int \sin^{2} x \cos^{3} x \ dx$$

The exponent of cosine is odd, so a factor of $\cos x$ is isolated and the remaining even power is rewritten in terms of sine:

$$\int \sin^{2} x \cos^{3} x \ dx = \int \sin^{2} x \cdot \cos^{2} x \cdot \cos x \ dx$$

Using $\cos^{2}x = 1 - \sin^{2}x$:

$$\int \sin^{2} x (1 - \sin^{2}x) \cdot \cos x \ dx$$

The factor $\cos x \ dx$ is the differential of $\sin x$, so set:

$$u = \sin x \qquad du = \cos x \ dx$$

The integral transforms into a polynomial in $u$:

$$\int u^{2}(1 - u^{2}) \ du = \int (u^{2} - u^{4}) \ du$$

Each term integrates immediately:

$$\frac{1}{3}u^{3} - \frac{1}{5}u^{5} + c$$

Substituting back $u = \sin x$:

$$\int \sin^{2} x \cos^{3} x \ dx = \frac{1}{3}\sin^{3}x - \frac{1}{5}\sin^{5}x + c$$

The presence of a second function raised to a power did not change the method: as long as one factor with an odd exponent can be detached, the integral reduces to a polynomial in the complementary function.

## Reciprocals of sine and cosine

Other frequently encountered cases involve the integrals of the reciprocals of sine and cosine. Although these expressions appear less straightforward at first, both follow from the same algebraic device. For the secant, the integrand is multiplied by a fraction equal to $1$:

$$
\begin{align}
\int \sec x \ dx &= \int \sec x \cdot \frac{\sec x + \tan x}{\sec x + \tan x} \ dx \\[6pt]
                 &= \int \frac{\sec^{2}x + \sec x\tan x}{\sec x + \tan x} \ dx
\end{align}
$$

The numerator is now exactly the derivative of the denominator, since:

$$\frac{d}{dx}(\sec x + \tan x) = \sec x\tan x + \sec^{2}x$$

The integral therefore has the form $\int f'(x)/f(x) \ dx$, which integrates directly to $\ln|f(x)|$:

$$\int \frac{1}{\cos x} \ dx = \int \sec x \ dx = \ln|\sec x + \tan x| + c$$

The same structure applies to the cosecant. Multiplying the integrand by $(\csc x - \cot x)/(\csc x - \cot x)$ gives:

$$
\begin{align}
\int \csc x \ dx &= \int \csc x \cdot \frac{\csc x - \cot x}{\csc x - \cot x} \ dx \\[6pt]
                 &= \int \frac{\csc^{2}x - \csc x\cot x}{\csc x - \cot x} \ dx
\end{align}
$$

The numerator is again the derivative of the denominator, since:

$$\frac{d}{dx}(\csc x - \cot x) = -\csc x\cot x + \csc^{2}x$$

so the integral of $\csc x$ produces:

$$\int \frac{1}{\sin x} \ dx = \int \csc x \ dx = \ln|\csc x - \cot x| + c$$

In both cases the result is [logarithmic](../logarithms/), and the sign inside the [absolute value](../absolute-value/) is easily confused. The two forms are best memorised together: $\sec x + \tan x$ for the cosine reciprocal, $\csc x - \cot x$ for the sine reciprocal.

## Decision procedure

The following stepwise procedure summarises the application of the techniques above to a generic trigonometric integral.

+ When the integrand is a single trigonometric or hyperbolic function, integrate directly through the corresponding entry in the table of standard antiderivatives.
+ When the integrand is a single power $\sin^{n} x$ or $\cos^{n} x$ with $n$ even, apply the power-reduction identities to every squared term and repeat until no even power remains. The integrand then reduces to a sum of expressions of the form $\cos kx$ that integrate immediately.
+ When the integrand is a single power $\sin^{n} x$ or $\cos^{n} x$ with $n$ odd, detach one factor of the function, convert the remaining even power through the Pythagorean identity, and apply the substitution $u = \cos x$ or $u = \sin x$, so that the differential matches the detached factor. The integral becomes a polynomial in $u$, evaluated by the power rule and followed by back-substitution.
+ When the integrand has the form $\sin^{m} x \cos^{n} x$ with at least one odd exponent, detach one factor of the odd-power function, convert the remaining even power through the Pythagorean identity, and substitute with the complementary function: $u = \sin x$ when cosine carries the odd exponent, $u = \cos x$ otherwise.
+ When both $m$ and $n$ are even, apply the power-reduction identities to every squared term, possibly together with $\sin x \cos x = \tfrac{1}{2}\sin 2x$, and integrate term by term.
+ For $\sec x$ and $\csc x$, multiply the integrand by a fraction equal to $1$ chosen so that the numerator becomes the derivative of the denominator, and recognise the resulting logarithmic form.
+ When the integrand is a rational function of $\sin x$ and $\cos x$ that does not fit the cases above, apply the [Weierstrass substitution](../weierstrass-substitution/), which converts the integrand into a [rational function](../rational-functions/) of a new variable. For radicals of quadratic expressions, the natural tool is instead [trigonometric substitution](../trigonometric-substitution-for-integrals/).

> When a product of two functions does not match any of the patterns above, the standard alternative is [integration by parts](../integration-by-parts/). When no closed-form antiderivative exists, the value of a definite integral can still be approximated through [numerical integration](../numerical-integration/).
