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
## Introduction

Integrals involving trigonometric functions, such as [sine](../sine-function/), [cosine](../cosine-function/), [tangent](../tangent-function/), and [cotangent](../cotangent-function/), can often be quite challenging to evaluate. In general (and this applies to all integrals), they require familiarity with a few [basic techniques](../integration-strategies/) for manipulating the integrand to obtain an integral that is easier to evaluate. This page presents the most common methods for handling the cases that arise most often, which are enough to evaluate a large proportion of integrals of this kind.

First, you need to memorize the [antiderivatives](../indefinite-integrals/) of the elementary trigonometric functions, since they underpin the basic steps. The table below provides a useful, concise reference.

[class="table-1"]

|     |                                                                              |
| --- | ---------------------------------------------------------------------------- |
| 1.  | $$\int \sin x \ dx = -\cos x + c$$                                           |
| 2.  | $$\int \cos x \ dx = \sin x + c$$                                            |
| 3.  | $$\int \tan x \ dx = -\ln \mid \cos x \mid + c$$                             |
| 4.  | $$\int \cot x \ dx = \ln \mid \sin x \mid + c$$                              |
| 5.  | $$\int \sec x \ dx = \ln \mid \sec x + \tan x \mid + c$$                     |
| 6.  | $$\int \csc x \ dx = \ln \mid \csc x - \cot x  \mid + c$$                    |
| 7.  | $$\int \sinh x \ dx = \cosh x + c$$                                          |
| 8.  | $$\int \cosh x \ dx = \sinh x + c$$                                          |
| 9.  | $$\int \tanh x \ dx = \ln \mid \cosh x \mid + c$$                            |
| 10. | $$\int \coth x \ dx = \ln \mid \sinh x \mid + c$$                            |
| 11. | $$\int \mathrm{sech} x \ dx = 2 \arctan\!\left(\tanh\frac{x}{2}\right) + c$$ |
| 12. | $$\int \operatorname{csch} x \ dx = \ln\left\lvert\tanh\frac{x}{2}\right\rvert + c$$ |

[/class]

There are relatively few cases to memorize, but this takes some effort; with practice, recalling them will become automatic. Before proceeding, I therefore encourage you to make sure you know the expressions above well, as some will be useful in the theory and examples that follow.

## Integrals of trigonometric powers with even $n$

We begin with a simple and fairly common case in which the integrand contains sine or cosine raised to an integer power, such as $\sin^4x,$ so its antiderivative is not immediately apparent. Integrals of this kind have the following general form:

$$\int \sin^{n} x \ dx \qquad \int \cos^{n} x \ dx \tag{1}$$

We first consider the case where the exponent $n$ is even. Here, we simplify the integral by rewriting the squared trigonometric terms using the power reduction formulas for sine and cosine:

$$\sin^{2} x = \frac{1 - \cos 2x}{2} \tag{2}$$

$$\cos^{2} x = \frac{1 + \cos 2x}{2} \tag{3}$$

In each identity, the right-hand side expresses the square of sine or cosine in terms of a lower power than the one on the left, allowing us to evaluate the integral. The first expression follows from the [Pythagorean identity](../pythagorean-identity/):

$$\sin^{2}x + \cos^{2}x = 1$$

The second follows from the [double-angle formula](../trigonometric-identities/) for cosine:

$$\cos 2x = \cos^{2}x - \sin^{2}x$$

By combining these identities, we can express $\cos 2x$ in terms of either $\cos^{2}x$ or $\sin^{2}x.$ Replacing $\sin^{2}x$ with $1 - \cos^{2}x$ gives:

$$\cos 2x = \cos^{2}x - (1 - \cos^{2}x) = 2\cos^{2}x - 1$$

Solving for $\cos^{2}x$ gives precisely identity $(3)$:

$$\cos^{2}x = \frac{1 + \cos 2x}{2}$$

The same reasoning applies to $\sin^{2}x.$ Substituting $\cos^{2}x = 1 - \sin^{2}x$ into the double-angle formula gives:

$$\cos 2x = (1 - \sin^{2}x) - \sin^{2}x = 1 - 2\sin^{2}x$$

Solving for $\sin^{2}x,$ we obtain identity $(2)$:

$$\sin^{2}x = \frac{1 - \cos 2x}{2}$$
- - -

To illustrate the method in practice, consider the following integral:

$$\int 2\cos^{4}x \ dx$$

Here we have the fourth power of cosine, for which identity $(3)$ is a convenient choice. We therefore rewrite the fourth power as follows:

$$
\begin{align}
\cos^{4}x &= \left(\frac{1 + \cos 2x}{2}\right)^{2} \\[6pt]
          &= \frac{1}{4}\left(1 + 2\cos 2x + \cos^{2} 2x\right) \tag{4}
\end{align}
$$

This has reduced the power of cosine, but a squared term remains. We use the same identity to reduce it, obtaining:

$$\cos^{2} 2x = \frac{1 + \cos 4x}{2}$$

Substituting this expression into $(4)$ and simplifying gives:

$$
\begin{align}
\cos^{4}x &= \frac{1}{4}\left(1 + 2\cos 2x + \frac{1 + \cos 4x}{2}\right) \\[6pt]
          &= \frac{1}{4}\left(\frac{3}{2} + 2\cos 2x + \frac{1}{2}\cos 4x\right) \\[6pt]
          &= \frac{3}{8} + \frac{1}{2}\cos 2x + \frac{1}{8}\cos 4x
\end{align}
$$

Multiplying by $2,$ as required by the original integral, gives:

$$\int 2\cos^{4}x \ dx = \int \left(\frac{3}{4} + \cos 2x + \frac{1}{4}\cos 4x\right) \ dx$$

We have now rewritten the original integral as a sum of terms that can be integrated separately, giving:

$$\frac{3}{4}x + \frac{1}{2}\sin 2x + \frac{1}{16}\sin 4x + c$$

> Keep in mind that the aim here is to reduce powers greater than $(1)$ to a sum of elementary terms, each of which can be integrated separately and directly.

## Integrals of trigonometric powers with odd $n$

When the exponent $n$ is odd, the method consists of setting aside one factor of the function raised to the odd power and rewriting the remaining even power using the Pythagorean identity. Consider a general odd power of the form $n = 2k + 1.$ For sine, we have:

$$
\begin{align}
\int \sin^{n} x \ dx &= \int \sin x (\sin^{2}x)^{k} \ dx \\[6pt]
                     &= \int \sin x (1 - \cos^{2}x)^{k} \ dx
\end{align}
$$

We then use [integration by substitution](../integration-by-substitution/), setting $u = \cos x$ and $du = -\sin x \ dx.$ This gives the integral of a [polynomial](../polynomials/) in $u,$ which we can evaluate directly.

The procedure for an odd power of cosine is entirely analogous. Again, we set aside one factor of $\cos x$ and rewrite the remaining even power using the identity:

$$\cos^{2}x = 1 - \sin^{2}x$$

We then make the substitution $u = \sin x,$ again obtaining the integral of a polynomial.

- - -

As a practical example, consider the following integral involving an odd power:

$$\int \cos^{5}x \ dx$$

The exponent is odd, so we set aside one cosine factor and rewrite the remaining even [power](../powers/) using the Pythagorean identity. We begin by rewriting the integral:

$$\int \cos^{5}x \ dx = \int \cos^{4}x \cdot \cos x \ dx$$

The factor $\cos^{4}x$ is an even power, so the procedure described earlier allows us to express it in terms of $\sin^{2}x$ using the identity:

$$\cos^{4}x = (\cos^{2}x)^{2} = (1 - \sin^{2}x)^{2}$$

The integral then becomes:

$$\int (1 - \sin^{2}x)^{2} \cdot \cos x \ dx$$

With a little practice, we immediately recognize that the factor $\cos x \ dx$ contains the [derivative](../derivatives/) of $\sin x,$ so we substitute $u = \sin x$ and $du = \cos x \ dx$ to obtain the integral of a polynomial in $u$:

$$\int (1 - u^{2})^{2} \ du$$

[Expanding the square](../notable-products/) gives:

$$\int (1 - 2u^{2} + u^{4}) \ du$$

Integrating each term, we obtain:

$$u - \frac{2}{3}u^{3} + \frac{1}{5}u^{5} + c$$

Substituting back $u = \sin x,$ we obtain the following result:

$$\sin x - \frac{2}{3}\sin^{3}x + \frac{1}{5}\sin^{5}x + c$$

## Products of powers of sine and cosine

A more general situation arises when sine and cosine appear together in integrals of the form:

$$\int \sin^{m} x \cos^{n} x \ dx \tag{5}$$

Here, the choice of method depends on the exponents and combines the two procedures described earlier. Suppose that $n$ is odd. Whenever at least one exponent is odd, we use the method for odd powers. In this case, we set aside one factor of $\cos x,$ express the remaining even power of cosine in terms of sine using $\cos^{2}x = 1 - \sin^{2}x,$ and substitute $u = \sin x.$ If instead $m$ is odd, we set aside one factor of $\sin x$ and let $u = \cos x.$ When both exponents are odd, either choice is valid.

When both $m$ and $n$ are even, the first step is to apply the power reduction formulas, $(2)$ and $(3),$ to each squared term. Another identity that is often useful is:

$$\sin x \cos x = \frac{1}{2}\sin 2x$$

This allows us to reduce the overall power in a single step. Repeatedly applying these identities reduces the integrand to a sum of terms of the form $\cos kx,$ each of which can be integrated directly, as in the previous examples.

- - -

As a practical example, consider the following integral of the form $(5)$:

$$\int \sin^{2} x \cos^{3} x \ dx$$

We see at once that the exponent of cosine is odd, so we set aside one factor of $\cos x$ and rewrite the even power of cosine in terms of sine:

$$\int \sin^{2} x \cos^{3} x \ dx = \int \sin^{2} x \cdot \cos^{2} x \cdot \cos x \ dx$$

Using the identity $\cos^{2}x = 1 - \sin^{2}x,$ the integral becomes:

$$\int \sin^{2} x (1 - \sin^{2}x) \cdot \cos x \ dx$$

The factor $\cos x \ dx$ is the [differential](../differential-of-a-function/) of $\sin x,$ so we set $u = \sin x$ and $du = \cos x \ dx,$ obtaining the integral of a polynomial in $u$:

$$\int u^{2}(1 - u^{2}) \ du = \int (u^{2} - u^{4}) \ du$$

Integrating each term gives:

$$\frac{1}{3}u^{3} - \frac{1}{5}u^{5} + c$$

Finally, substituting back $u = \sin x,$ we find that the integral is:

$$\frac{1}{3}\sin^{3}x - \frac{1}{5}\sin^{5}x + c$$

## Reciprocals of sine and cosine

Other common cases involve integrals of the reciprocals of sine and cosine. Although these expressions may seem less straightforward, their integrals can be evaluated using the same algebraic procedure. Consider, for example, the reciprocal of cosine:

$$\int \frac{1}{\cos x} \ dx$$

We know that the integrand is the [secant function](../secant-function/). We now multiply the secant by a fraction equal to $1$:

$$\begin{align}
\int \sec x \ dx &= \int \sec x \cdot \frac{\sec x + \tan x}{\sec x + \tan x} \ dx \\[12pt]
                 &= \int \frac{\sec^{2}x + \sec x\tan x}{\sec x + \tan x} \ dx
\end{align}
$$

This trick makes the numerator the derivative of the denominator, since the following identity holds:

$$\frac{d}{dx}(\sec x + \tan x) = \sec x\tan x + \sec^{2}x$$

The integral therefore has the form:

$$\int \frac{f'(x)}{f(x)} \ dx$$

An antiderivative is $\ln|f(x)|.$ We therefore obtain:

$$\int \frac{1}{\cos x} \ dx = \int \sec x \ dx = \ln|\sec x + \tan x| + c$$

The same approach applies to the integral of the reciprocal of sine:

$$\int \frac{1}{\sin x} \ dx$$

Here the integrand is the [cosecant function](../cosecant-function/). Multiplying it by a fraction equal to $1,$ as above, gives the counterpart of the expression for the reciprocal of cosine:

$$
\begin{align}
\int \csc x \ dx &= \int \csc x \cdot \frac{\csc x - \cot x}{\csc x - \cot x} \ dx \\[12pt]
                 &= \int \frac{\csc^{2}x - \csc x\cot x}{\csc x - \cot x} \ dx
\end{align}
$$

Again, the numerator is the derivative of the denominator, since the following identity holds:

$$\frac{d}{dx}(\csc x - \cot x) = -\csc x\cot x + \csc^{2}x$$

The integral of $\csc x$ is therefore:

$$\int \frac{1}{\sin x} \ dx = \int \csc x \ dx = \ln|\csc x - \cot x| + c$$

## A procedure for choosing the method

We can now outline a procedure that summarizes how to apply the cases discussed above to a general trigonometric integral.

+ First, when the integrand is a single trigonometric or hyperbolic function, integrate directly using the table of basic antiderivatives.
+ When the integrand is a power $\sin^{n} x$ or $\cos^{n} x$ with even $n,$ apply the power reduction formulas to each squared term and repeat until no even powers remain. This reduces the integrand to a sum of expressions of the form $\cos kx,$ which can be integrated directly.
+ When the integrand is a power $\sin^{n} x$ or $\cos^{n} x$ with odd $n,$ set aside one factor of the function, rewrite the remaining even power using the Pythagorean identity, and substitute $u = \cos x$ or $u = \sin x,$ so that the differential matches the factor set aside. This gives the integral of a polynomial in $u,$ which is straightforward to evaluate.
+ When the integrand has the form $\sin^{m} x \cos^{n} x$ with at least one odd exponent, set aside one factor of the function with the odd exponent and rewrite the remaining even power using the Pythagorean identity. Then choose the other function as the new variable, setting $u = \sin x$ when cosine has an odd exponent or $u = \cos x$ when its exponent is even.
+ When both $m$ and $n$ are even, apply the power reduction formulas to each squared term and integrate term by term.
+ For $\sec x$ and $\csc x,$ multiply the integrand by a fraction equal to $1,$ chosen so that the numerator becomes the derivative of the denominator. This gives the corresponding [logarithmic form](../logarithms/).
+ Finally, when the integrand is a rational function of $\sin x$ and $\cos x$ that does not fit any of the preceding cases, use the [Weierstrass substitution](../the-weierstrass-substitution/), which transforms the integrand into a [rational function](../rational-functions/) of a new variable. For [radicals](../radicals/) of quadratic expressions, use [trigonometric substitution](../trigonometric-substitution-for-integrals/).

> These techniques are very useful, but trigonometric integrals cannot always be reduced to the cases presented on this page. For example, when a product of two functions does not fit any of the cases discussed, [integration by parts](../integration-by-parts/) is a common alternative. In more complicated cases, when no closed-form antiderivative exists, the value of a [definite integral](../definite-integrals/) can still be approximated using [numerical integration](../numerical-integration/).
