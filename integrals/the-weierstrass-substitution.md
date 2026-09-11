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
## When to use the substitution

The Weierstrass substitution is a method for evaluating integrals that cannot be computed directly, whose integrands are [rational functions](../rational-functions/) involving sine and cosine, by making a suitable change of variable. In general, integrals of this type have forms similar to those listed below, where the numerator and denominator are polynomials in $\sin x$ and $\cos x:$

$$\frac{1}{1 + \sin x} \qquad \frac{1}{5 - 3\cos x} \qquad \frac{1}{\sin x + \cos x} \tag{1}$$

We have already covered some techniques for [integrating trigonometric functions](../integral-of-trigonometric-functions/), based on power-reduction formulas or separating out factors. However, in cases such as those in $(1)$ these techniques do not provide a useful way to obtain a result readily. In the cases we will consider shortly, we need to make a change of variable that reduces the problem to integrating a simple rational function, which is generally handled using [polynomial division](../polynomial-division/) and [partial fraction decomposition](../partial-fraction-decomposition/).

The Weierstrass substitution is based on introducing the following variable:

$$t = \tan\left(\frac{x}{2}\right) \tag{2}$$

This substitution allows us to write $\sin x,$ $\cos x$ and the [differential](../differential-of-a-function/) $dx$ as rational expressions in $t.$ To derive these expressions, as we will see shortly, we use the double-angle formulas and the [Pythagorean identity](../pythagorean-identity/). Once we have calculated the antiderivative in $t,$ we return to the original variable $x$ by substituting $t = \tan(x/2).$

First, we examine how to derive the expressions for sine, cosine and the differential. I should mention at the outset that recalling the various trigonometric identities we will use in the calculations will require a little effort, so I encourage you to consult the relevant page before proceeding. For sine, we start with the [double-angle formula](../trigonometric-identities/), which gives:

$$\sin x = 2\sin\left(\frac{x}{2}\right)\cos\left(\frac{x}{2}\right) \tag{3}$$

Multiplying by $\cos(x/2) / \cos(x/2)$ allows us to rewrite the right-hand side as:

$$2\tan\left(\frac{x}{2}\right)\cos^2\left(\frac{x}{2}\right) \tag{4}$$

The following trigonometric identity holds for cosine:

$$\cos^2\left(\frac{x}{2}\right) = \frac{1}{1 + \tan^2(x/2)}$$

Substituting this into $(4)$ allows us to rewrite the expression for sine in $(3)$ as:

$$\sin x = \frac{2t}{1 + t^2} \tag{5}$$

- - -

A similar procedure applies to deriving the expression for cosine, using the corresponding double-angle formula:

$$\cos x = \cos^2\left(\frac{x}{2}\right) - \sin^2\left(\frac{x}{2}\right)$$

We divide the right-hand side by $\cos^2(x/2) + \sin^2(x/2)$ and then divide the numerator and denominator by $\cos^2(x/2),$ obtaining:

$$\cos x = \frac{1 - t^2}{1 + t^2} \tag{6}$$

- - -

Finally, we calculate the differential by differentiating relation $(2)$ with respect to $x.$ This gives:

$$\frac{dt}{dx} = \frac{1}{2}\sec^2\left(\frac{x}{2}\right) = \frac{1}{2}\left(1 + \tan^2\left(\frac{x}{2}\right)\right) = \frac{1 + t^2}{2}$$

Solving for $dx$ gives the third identity on which the substitution is based, namely:

$$dx = \frac{2}{1 + t^2} \ dt \tag{7}$$

The formulas $(5),$ $(6)$ and $(7)$ just derived therefore allow us to apply the Weierstrass method by substituting them into the integral of any rational expression in $\sin x$ and $\cos x$ to express it in the simpler variable $t$. To recap, the substitutions to apply are as follows:

[class="table-1"]

|          |                         |
| -------- | ----------------------- |
| $\sin x$ | $\dfrac{2t}{1+t^2}$     |
| $\cos x$ | $\dfrac{1-t^2}{1+t^2}$  |
| $dx$     | $\dfrac{2}{1+t^2} \ dt$ |

[/class]

## Practical applications

We work through a few examples to illustrate how the Weierstrass method is applied in practice. Consider the following integral, whose integrand is a rational function of sine:

$$\int \frac{dx}{1 + \sin x}$$

Using identity $(5),$ we can rewrite the denominator as follows:

$$
\begin{align}
1 + \sin x &= 1 + \frac{2t}{1+t^2} \\[6pt]
           &= \frac{1 + t^2 + 2t}{1+t^2} \\[6pt]
           &= \frac{(1+t)^2}{1+t^2}
\end{align}
$$

We now rewrite the differential using $(7),$ obtaining:

$$
\begin{align}
\frac{1}{1+\sin x} \ dx &= \frac{1+t^2}{(1+t)^2} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                       &= \frac{2}{(1+t)^2} \ dt
\end{align}
$$

This gives an integrand whose [antiderivative](../indefinite-integrals/) can be calculated directly:

$$\int \frac{2}{(1+t)^2} \ dt = -\frac{2}{1+t} + c$$

At this point, returning to the original variable through the identity $t = \tan(x/2),$ we obtain the result:

$$\int \frac{dx}{1 + \sin x} = -\frac{2}{1 + \tan(x/2)} + c$$

- - -

Now consider the following integral, whose integrand is a rational function of cosine:

$$\int \frac{dx}{5 - 3\cos x}$$

Using identity $(6),$ we can rewrite the denominator as:

$$
\begin{align}
5 - 3\cos x &= 5 - 3 \cdot \frac{1 - t^2}{1+t^2} \\[6pt]
            &= \frac{5(1+t^2) - 3(1-t^2)}{1+t^2} \\[6pt]
            &= \frac{2 + 8t^2}{1+t^2} \\[8pt]
            &= \frac{2(1 + 4t^2)}{1+t^2}
\end{align}
$$

Now substituting the expression for the differential using $(7),$ we obtain:

$$
\begin{align}
\frac{1}{5-3\cos x} \ dx &= \frac{1+t^2}{2(1+4t^2)} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                        &= \frac{dt}{1 + 4t^2}
\end{align}
$$

Here too, the remaining integral reduces to an elementary form, and since $1 + 4t^2 = 1 + (2t)^2,$ we set $u = 2t$ and $du = 2 \ dt,$ so the integral becomes:

$$
\begin{align}
\int \frac{dt}{1 + 4t^2} &= \frac{1}{2}\int \frac{du}{1 + u^2} \\[6pt]
                        &= \frac{1}{2}\arctan u + c \\[6pt]
                        &= \frac{1}{2}\arctan(2t) + c
\end{align}
$$

Returning to the variable $x,$ we obtain the antiderivative:

$$\int \frac{dx}{5 - 3\cos x} = \frac{1}{2}\arctan(2\tan(x/2)) + c$$

- - -

We present one final case by evaluating the following integral:

$$\int \frac{dx}{2 + \sin x}$$

Applying the identities already derived, we can rewrite the denominator as follows:

$$
\begin{align}
2 + \sin x &= 2 + \frac{2t}{1+t^2} \\[6pt]
           &= \frac{2(1+t^2) + 2t}{1+t^2} \\[6pt]
           &= \frac{2(t^2 + t + 1)}{1+t^2}
\end{align}
$$

The expression to be integrated therefore becomes:

$$
\begin{align}
\frac{1}{2+\sin x} \ dx &= \frac{1+t^2}{2(t^2+t+1)} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                       &= \frac{dt}{t^2+t+1}
\end{align}
$$

[Completing the square](../completing-the-square/) in the denominator, we obtain:

$$t^2 + t + 1 = \left(t + \frac{1}{2}\right)^2 + \frac{3}{4}$$

The integral therefore becomes:

$$\int \frac{dt}{\left(t+\frac{1}{2}\right)^2 + \frac{3}{4}}$$

With a little practice, we can recognize that this expression matches the elementary form:

$$\int \frac{du}{u^2 + a^2}$$

In this case, we have $u = t + 1/2$ and $a = \sqrt{3}/2.$ Using the corresponding integration formula, we obtain:

$$\int \frac{dt}{t^2+t+1} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2t+1}{\sqrt{3}}\right) + c$$

Once again substituting $t = \tan(x/2),$ we obtain the final expression:

$$\int \frac{dx}{2+\sin x} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2\tan(x/2)+1}{\sqrt{3}}\right) + c$$

> Here too, we have seen that after the substitution, the integrand becomes a rational function of $t,$ simpler than the original one, and its antiderivative may contain [arctangents](../arctangent-function/) and [logarithms](../logarithms/), which typically appear when [integrating rational functions](../integral-of-rational-functions/).

## Domain conditions

We need to consider the domains of the functions involved in the substitutions. The substitution $t = \tan(x/2)$ is defined for every $x$ such that $x/2 \neq \pi/2 + k\pi,$ that is, for every $x \notin \pi + 2\pi\mathbb{Z}.$ When evaluating an [indefinite integral](../indefinite-integrals/), the resulting formulas hold on intervals where both the original integrand and the substitution are defined.

Greater care is needed when applying the substitution to a [definite integral](../definite-integrals/) whose limits of integration may lie in different intervals. In this case, we apply the substitution separately to each part of the [domain](../determining-the-domain-of-a-function/) of integration on which it is defined, has a continuous nonzero derivative and is [invertible](../inverse-function/) on the interval in question, then add the resulting contributions. Mechanically applying the substitutions above across a point of the form $x = (2k+1)\pi$ could lead to incorrect results, since the substitution might not be defined at that point. Consider, for example, the definite integral:

$$\int_0^{2\pi} \frac{dx}{5 - 3\cos x}$$

The integrand is [continuous](../continuous-functions/) throughout the interval $[0,2\pi]$ but the substitution $t = \tan(x/2),$ by contrast, is not defined at $x = \pi.$ For this reason, we must split the integral at this point and rewrite the two contributions using the following [limits](../limits/):

$$
\lim_{a \to \pi^-}\int_0^a \frac{dx}{5 - 3\cos x}
+ \lim_{b \to \pi^+}\int_b^{2\pi} \frac{dx}{5 - 3\cos x}
$$

As we have already shown in the preceding examples, the Weierstrass substitution transforms the expression to be integrated into:

$$\frac{dx}{5 - 3\cos x} = \frac{dt}{1 + 4t^2}$$

On the first interval, $x = 0$ corresponds to $t = 0,$ while $t \to +\infty$ as $x \to \pi^-.$ On the second interval, $t \to -\infty$ as $x \to \pi^+,$ while $x = 2\pi$ corresponds to $t = 0.$ We therefore obtain two [improper integrals](../improper-integrals/), which we write as follows:

$$\int_0^{+\infty} \frac{dt}{1 + 4t^2} + \int_{-\infty}^0 \frac{dt}{1 + 4t^2}$$

We calculate the two contributions separately and obtain the following values for the respective integrals:

$$
\begin{align}
\int_0^{+\infty} \frac{dt}{1 + 4t^2}
&= \lim_{A \to +\infty}\left[\frac{1}{2}\arctan(2t)\right]_0^A
= \frac{\pi}{4} \\[6pt]
\int_{-\infty}^0 \frac{dt}{1 + 4t^2}
&= \lim_{B \to -\infty}\left[\frac{1}{2}\arctan(2t)\right]_B^0
= \frac{\pi}{4}
\end{align}
$$

Adding the two contributions, we finally obtain the value of the original integral:

$$\frac{\pi}{4} + \frac{\pi}{4} = \frac{\pi}{2}$$

> The given integral therefore equals $\pi/2.$ Transforming only the original limits of integration $0$ and $2\pi$ would have produced two limits both equal to zero, failing to account for the passage through the point where the substitution is undefined.

## Final remarks

The Weierstrass substitution is not always the most efficient method. When the integrand contains only even powers of $\sin x$ and $\cos x$ it is preferable to use the basic methods for integrating trigonometric functions. The same also applies when the integrand can be rewritten using the following identities:

$$\sin^2 x = (1 - \cos 2x)/2$$
$$\cos^2 x = (1 + \cos 2x)/2$$ 

When the integrand has the form $R(\sin x)\cos x$ or $R(\cos x)\sin x,$ the direct [substitutions](../integration-by-substitution/) $u = \sin x$ or $u = \cos x$ are quicker. As a practical guideline, it is advisable to use the Weierstrass substitution only when the integrand is a rational function of $\sin x$ and $\cos x$ with no obvious simplifications available through [trigonometric identities](../trigonometric-identities/) or direct substitutions. In other cases, simpler techniques lead to shorter calculations.