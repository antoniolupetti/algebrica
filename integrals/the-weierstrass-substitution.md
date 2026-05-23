---
title: The Weierstrass Substitution
source: https://algebrica.org/the-weierstrass-substitution/
license: CC BY-NC 4.0
tags:
  - arctangent
  - half-angle-substitution
  - indefinite-integral
  - integration-by-substitution
  - partial-fractions
  - rational-functions
  - trigonometric-identities
  - trigonometric-integrals
  - weierstrass-substitution
---
## The class of integrals to be handled

Many integrals encountered in elementary calculus involve a [rational function](../rational-functions/) whose variable is itself a combination of sine and cosine. Expressions such as:

$$\frac{1}{1 + \sin x} \qquad \frac{1}{5 - 3\cos x} \qquad \frac{1}{\sin x + \cos x}$$

share a common structure: the numerator and the denominator are [polynomials](../polynomials/) in $\sin x$ and $\cos x$. The techniques developed for [trigonometric integrals](../integral-of-trigonometric-functions/), which rely on power-reduction identities or on separating one factor from the rest, do not provide a uniform procedure for integrands of this kind. What is required is a single change of variable that converts every rational expression in $\sin x$ and $\cos x$ into an ordinary rational function of a new variable, so that the problem reduces to the [integral of a rational function](../integral-of-rational-functions/), treated by polynomial division and [partial fraction decomposition](../partial-fraction-decomposition/).

The substitution that achieves this is built on the half-angle $x/2$, and it exploits in a single step the algebraic identities relating [tangent](../tangent-and-cotangent/), [sine and cosine](../sine-and-cosine/).

## The substitution $t = \tan(x/2)$

The new variable is introduced through the equation:

$$t = \tan\left(\frac{x}{2}\right) \tag{1}$$

The angle $x$ is restricted, for the moment, to the open [interval](../intervals/) $(-\pi, \pi)$, so that $\tan(x/2)$ is well defined and the map $x \mapsto t$ is a bijection onto the real line. The original variable is recovered through the inverse relation $x = 2\arctan t$, which uses the [arctangent](../arctangent-and-arccotangent/) function and will appear whenever the result must be expressed back in terms of $x$.

The strength of the substitution lies in the fact that $\sin x$, $\cos x$, and the differential $dx$ all admit a closed-form rational expression in $t$. The derivation of these expressions uses the double-angle identities and the [Pythagorean identity](../pythagorean-identity/) $\sin^2\theta + \cos^2\theta = 1$.

## Translating sine, cosine, and the differential

The starting point is the [double-angle identity](../trigonometric-identities/) for the sine:

$$\sin x = 2\sin\left(\frac{x}{2}\right)\cos\left(\frac{x}{2}\right)$$

Writing the right-hand side as $2\tan(x/2)\cos^2(x/2)$ and using the identity $\cos^2(x/2) = 1/(1 + \tan^2(x/2))$, the sine takes the form:

$$\sin x = \frac{2t}{1 + t^2} \tag{2}$$

The double-angle identity for the cosine reads $\cos x = \cos^2(x/2) - \sin^2(x/2)$. Dividing both the numerator and the denominator (which equals $1$ by the Pythagorean identity) by $\cos^2(x/2)$, one arrives at:

$$\cos x = \frac{1 - t^2}{1 + t^2} \tag{3}$$

The differential is computed by differentiating the relation $t = \tan(x/2)$ with respect to $x$:

$$\frac{dt}{dx} = \frac{1}{2}\sec^2\left(\frac{x}{2}\right) = \frac{1}{2}\left(1 + \tan^2\left(\frac{x}{2}\right)\right) = \frac{1 + t^2}{2}$$

Solving for $dx$ yields the third fundamental identity:

$$dx = \frac{2}{1 + t^2} \ dt \tag{4}$$

Formulas $(2)$, $(3)$, and $(4)$ are the three keys of the method. Substituting them into any rational expression in $\sin x$ and $\cos x$ produces a rational expression in $t$, which can be integrated by the techniques developed for rational functions: polynomial division, decomposition into partial fractions, and integration of elementary blocks.

> The factor $2/(1+t^2)$ introduced by the differential is the same one that appears in the derivative of $\arctan$. The coincidence reflects the inverse relation $x = 2\arctan t$ between the two variables. The presence of $1 + t^2$ in every formula is a direct consequence of this connection.

## Example 1

Consider the integral:

$$\int \frac{dx}{1 + \sin x}$$

Applying the substitution and using identity $(2)$, the denominator becomes:

$$
\begin{align}
1 + \sin x &= 1 + \frac{2t}{1+t^2} \\[6pt]
           &= \frac{1 + t^2 + 2t}{1+t^2} \\[6pt]
           &= \frac{(1+t)^2}{1+t^2}
\end{align}
$$

Combining this expression with the differential $(4)$, the integrand reduces to:

$$
\begin{align}
\frac{1}{1+\sin x} \ dx &= \frac{1+t^2}{(1+t)^2} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                       &= \frac{2}{(1+t)^2} \ dt
\end{align}
$$

The factor $1 + t^2$ cancels exactly, and what remains is an integral of $t$ alone. The [antiderivative](../indefinite-integrals/) is immediate:

$$\int \frac{2}{(1+t)^2} \ dt = -\frac{2}{1+t} + c$$

Reverting to the original variable through the identity $t = \tan(x/2)$, the final answer is:

$$\int \frac{dx}{1 + \sin x} = -\frac{2}{1 + \tan(x/2)} + c$$

> The result can be checked by direct differentiation, which restores the original integrand after a short computation.

## Example 2

Consider the integral:

$$\int \frac{dx}{5 - 3\cos x}$$

Using identity $(3)$, the denominator takes the form:

$$
\begin{align}
5 - 3\cos x &= 5 - 3 \cdot \frac{1 - t^2}{1+t^2} \\[6pt]
            &= \frac{5(1+t^2) - 3(1-t^2)}{1+t^2} \\[6pt]
            &= \frac{2 + 8t^2}{1+t^2} \\[6pt]
            &= \frac{2(1 + 4t^2)}{1+t^2}
\end{align}
$$

Combining this with the differential $(4)$, the integrand simplifies considerably:

$$
\begin{align}
\frac{1}{5-3\cos x} \ dx &= \frac{1+t^2}{2(1+4t^2)} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                        &= \frac{dt}{1 + 4t^2}
\end{align}
$$

The cancellation of $1 + t^2$ is again the decisive step. The remaining integral has standard arctangent form, since $1 + 4t^2 = 1 + (2t)^2$. Setting $u = 2t$, so that $du = 2 \ dt$, the integral becomes:

$$
\begin{align}
\int \frac{dt}{1 + 4t^2} &= \frac{1}{2}\int \frac{du}{1 + u^2} \\[6pt]
                        &= \frac{1}{2}\arctan u + c \\[6pt]
                        &= \frac{1}{2}\arctan(2t) + c
\end{align}
$$

Returning to the variable $x$, the antiderivative reads:

$$\int \frac{dx}{5 - 3\cos x} = \frac{1}{2}\arctan(2\tan(x/2)) + c$$

> The pattern that emerges is typical of the method: after substitution the integrand becomes a rational function in $t$, and the result is a combination of arctangents and logarithms, the elementary building blocks for the integration of rational functions.

## Example 3

Consider the integral:

$$\int \frac{dx}{2 + \sin x}$$

Applying the substitution to the denominator gives:

$$
\begin{align}
2 + \sin x &= 2 + \frac{2t}{1+t^2} \\[6pt]
           &= \frac{2(1+t^2) + 2t}{1+t^2} \\[6pt]
           &= \frac{2(t^2 + t + 1)}{1+t^2}
\end{align}
$$

The integrand therefore becomes:

$$
\begin{align}
\frac{1}{2+\sin x} \ dx &= \frac{1+t^2}{2(t^2+t+1)} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                       &= \frac{dt}{t^2+t+1}
\end{align}
$$

Completing the square in the denominator:

$$t^2 + t + 1 = \left(t + \frac{1}{2}\right)^2 + \frac{3}{4}$$

The integral is now in the form:

$$\int \frac{dt}{\left(t+\frac{1}{2}\right)^2 + \frac{3}{4}}$$

This matches the standard pattern $\int du/(u^2 + a^2)$ with $u = t + 1/2$ and $a = \sqrt{3}/2$. Using the standard antiderivative for this form, the result is:

$$\int \frac{dt}{t^2+t+1} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2t+1}{\sqrt{3}}\right) + c$$

Substituting back $t = \tan(x/2)$ produces the final expression:

$$\int \frac{dx}{2+\sin x} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2\tan(x/2)+1}{\sqrt{3}}\right) + c$$

> The three examples illustrate the typical behaviour of the method. After the substitution the integral becomes a rational function in $t$, and the antiderivative is invariably a combination of rational functions, arctangents, and logarithms in the new variable, transposed back at the end through the identity $t = \tan(x/2)$.

## Conditions on the domain

The substitution $t = \tan(x/2)$ is defined for every $x$ such that $x/2 \neq \pi/2 + k\pi$, that is, for every $x \notin \pi + 2\pi\mathbb{Z}$. The map $x \mapsto t$ is a smooth bijection from each open interval $((2k-1)\pi, (2k+1)\pi)$ onto the whole real line. When the goal is an [indefinite integral](../indefinite-integrals/), the formulas obtained above are valid on each such interval, and the constant of integration may take different values on different intervals.

The situation is more delicate for a [definite integral](../definite-integrals/) whose endpoints belong to different fundamental intervals. The substitution must then be applied separately on each piece of the integration [domain](../determining-the-domain-of-a-function/) where it is regular, and the contributions must be assembled at the end. A direct mechanical application of the substitution across a point of the form $x = (2k+1)\pi$ leads to incorrect results, since the substitution is undefined there.

> A second source of caution is the orientation. The inverse map $x = 2\arctan t$ sends the real line to the open interval $(-\pi, \pi)$, so any antiderivative expressed through $\arctan(\cdots\tan(x/2)\cdots)$ is continuous on each open interval but exhibits jumps of $2\pi$ at the points $x = (2k+1)\pi$. The constant of integration must be redefined on each interval whenever a globally continuous primitive is required.

## When to prefer other techniques

The Weierstrass substitution always works on rational integrands in sine and cosine, but it is not always the most efficient route. When the integrand contains only even powers of $\sin x$ and $\cos x$, or admits a reorganisation through the identities $\sin^2 x = (1 - \cos 2x)/2$ and $\cos^2 x = (1 + \cos 2x)/2$, the half-angle substitution introduces unnecessary algebraic complications. Similarly, when the integrand has the form $R(\sin x)\cos x$ or $R(\cos x)\sin x$, the direct [substitutions](../integration-by-substitution/) $u = \sin x$ or $u = \cos x$ are far quicker, since they bypass the rationalisation altogether.

A practical guideline is therefore the following. When the integrand is a true rational function of $\sin x$ and $\cos x$, with no obvious simplification through [trigonometric identities](../trigonometric-identities/) or direct substitutions, the Weierstrass substitution is the appropriate tool. In the other cases the simpler techniques produce shorter and cleaner computations.
