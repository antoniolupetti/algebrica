---
title: Hyperbolic Secant and Cosecant
source: https://algebrica.org/hyperbolic-secant-and-cosecant/
license: CC BY-NC 4.0
tags:
  - hyperbolic-cosecant
  - hyperbolic-functions
  - hyperbolic-secant
  - trigonometry
---

## Hyperbolic secant

The hyperbolic secant arises from the [hyperbolic cosine](../hyperbolic-sine-and-cosine/) in exactly the same way that the circular [secant](../secant-and-cosecant/) arises from the circular cosine. Given the right branch of the equilateral [hyperbola](../hyperbola/):

$$
X^{2} - Y^{2} = 1
$$

and the point $P(\cosh(x), \sinh(x))$ associated with a signed hyperbolic sector of area $x/2$, the hyperbolic secant of $x$ is defined as the reciprocal of the horizontal coordinate of $P$:

$$
\mathrm{sech}(x) := \frac{1}{\cosh(x)}
$$

Since $\cosh(x) \geq 1$ for every real $x$, the denominator never vanishes, and the hyperbolic secant is defined on the entire real line. The values of $\mathrm{sech}(x)$ are therefore confined to the interval $(0, 1]$, attaining the maximum at $x = 0$ where $\cosh(0) = 1$.

![IMG. 1](svg/hyperbolic-sine-and-cosine-1.svg)

From a geometric point of view, the reciprocal $1/\cosh(x)$ measures the proportion between the unit radius of the hyperbola and the horizontal coordinate of $P$. As the hyperbolic parameter $x$ grows in absolute value, the point $P$ moves away from the $Y$-axis and $\cosh(x)$ increases exponentially, so the hyperbolic secant approaches zero from above without ever reaching it.

> This section examines the hyperbolic secant from a geometric point of view. For the analytical properties of the function, including domain, symmetry, limits, derivatives, and integrals, see the dedicated entry on the [hyperbolic secant function](../hyperbolic-secant-function/).

## Common values of the hyperbolic secant

Below are some commonly known values of $\mathrm{sech}(x)$ for selected arguments, useful in various applications involving hyperbolic functions:

$$
\begin{align}
x &= 0      && \mathrm{sech}(x) = 1 \\[6pt]
x &= \ln 2  && \mathrm{sech}(x) = \tfrac{4}{5} \\[6pt]
x &= \ln 3  && \mathrm{sech}(x) = \tfrac{3}{5} \\[6pt]
x &= 1      && \mathrm{sech}(x) = \tfrac{2}{e + e^{-1}} \\[6pt]
x &\to \pm\infty && \mathrm{sech}(x) \to 0
\end{align}
$$

## Hyperbolic identities for the secant

The identities governing the hyperbolic secant follow from its definition as the reciprocal of the hyperbolic cosine. Dividing the fundamental hyperbolic identity $\cosh^{2}(x) - \sinh^{2}(x) = 1$ by $\cosh^{2}(x)$ produces the relation that connects the hyperbolic secant to the hyperbolic tangent, while the even symmetry of the cosine transfers directly to the secant. The relations collected below summarise these connections together with the algebraic forms most often encountered in computations.

$$
\begin{align}
&\mathrm{sech}(x) = \frac{1}{\cosh(x)} \\[6pt]
&1 - \tanh^{2}(x) = \mathrm{sech}^{2}(x) \\[10pt]
&\mathrm{sech}(-x) = \mathrm{sech}(x) \\[6pt]
&\mathrm{sech}(x)\tanh(x) = \frac{\sinh(x)}{\cosh^{2}(x)} \\[6pt]
&\mathrm{sech}^{2}(x) + \tanh^{2}(x) = 1
\end{align}
$$

> These formulas collect the most useful identities involving the hyperbolic secant, including the reciprocal definition, the identity inherited from the fundamental hyperbolic relation, the symmetry property, and common algebraic transformations. For a broader overview, refer to the full collection of [hyperbolic identities](../hyperbolic-identities/).

## Hyperbolic cosecant

In parallel with the construction above, the hyperbolic cosecant is defined as the reciprocal of the hyperbolic sine. Starting again from the point $P(\cosh(x), \sinh(x))$ on the right branch of the equilateral hyperbola, the hyperbolic cosecant of $x$ is the reciprocal of the vertical coordinate of $P$:

$$
\mathrm{csch}(x) := \frac{1}{\sinh(x)}
$$

Since $\sinh(x)$ vanishes at $x = 0$, the hyperbolic cosecant is defined on the entire real line with the exception of the origin. On its domain the function takes every nonzero real value, since $\sinh(x)$ is a bijection from $\mathbb{R} \setminus \{0\}$ onto $\mathbb{R} \setminus \{0\}$.

Geometrically, the reciprocal $1/\sinh(x)$ compares the unit radius of the hyperbola with the vertical coordinate of $P$. As $|x|$ becomes large, the point $P$ moves away from the $X$-axis and $|\sinh(x)|$ increases exponentially, so the hyperbolic cosecant approaches zero. Near $x = 0$, the vertical coordinate vanishes and the hyperbolic cosecant is unbounded.

> This section examines the hyperbolic cosecant from a geometric point of view. For the analytical properties of the function, including domain, symmetry, limits, derivatives, and integrals, see the dedicated entry on the [hyperbolic cosecant function](../hyperbolic-cosecant-function/).

## Geometric interpretation

Both definitions rest on the same geometric object: the point $P(\cosh(x), \sinh(x))$ on the right branch of the equilateral hyperbola, whose horizontal and vertical coordinates encode the [hyperbolic cosine and sine](../hyperbolic-sine-and-cosine/). The hyperbolic secant and cosecant are read from these coordinates by taking their reciprocals, in close parallel with the circular case, where the circular [secant and cosecant](../secant-and-cosecant/) are reciprocals of the cosine and sine.

This common origin also makes transparent the asymmetric behaviour of the two functions. As $|x|$ grows, both $\cosh(x)$ and $\sinh(x)$ grow exponentially, so $\mathrm{sech}(x)$ and $\mathrm{csch}(x)$ both tend to zero. Near the origin, however, the two functions differ sharply: $\cosh(0) = 1$ keeps $\mathrm{sech}(x)$ bounded above by $1$, while $\sinh(0) = 0$ forces $\mathrm{csch}(x)$ to diverge.

## Common values of the hyperbolic cosecant

Below are some commonly known values of $\mathrm{csch}(x)$ for selected arguments, useful in various applications involving hyperbolic functions:

$$
\begin{align}
x &= 0      && \mathrm{csch}(x) \text{ is undefined} \\[6pt]
x &= \ln 2  && \mathrm{csch}(x) = \tfrac{4}{3} \\[6pt]
x &= \ln 3  && \mathrm{csch}(x) = \tfrac{3}{4} \\[6pt]
x &= 1      && \mathrm{csch}(x) = \tfrac{2}{e - e^{-1}} \\[6pt]
x &\to \pm\infty && \mathrm{csch}(x) \to 0
\end{align}
$$

## Hyperbolic identities for the cosecant

The identities involving the hyperbolic cosecant arise in the same way from its definition as the reciprocal of the hyperbolic sine. Dividing the fundamental hyperbolic identity $\cosh^{2}(x) - \sinh^{2}(x) = 1$ by $\sinh^{2}(x)$, for $x \neq 0$, yields the relation that links the hyperbolic cosecant to the hyperbolic cotangent, and the odd symmetry of the sine carries over to the cosecant through a change of sign. The relations listed below gather these properties alongside the algebraic forms that recur in practice.

$$
\begin{align}
&\mathrm{csch}(x) = \frac{1}{\sinh(x)} \\[6pt]
&\coth^{2}(x) - 1 = \mathrm{csch}^{2}(x) \\[8pt]
&\mathrm{csch}(-x) = -\mathrm{csch}(x) \\[6pt]
&\mathrm{csch}(x)\coth(x) = \frac{\cosh(x)}{\sinh^{2}(x)} \\[6pt]
&\coth^{2}(x) - \mathrm{csch}^{2}(x) = 1
\end{align}
$$

> These formulas collect the most useful identities involving the hyperbolic cosecant, including the reciprocal definition, the identity descending from the fundamental hyperbolic relation, the symmetry property, and common algebraic transformations. For a broader overview, refer to the full collection of [hyperbolic identities](../hyperbolic-identities/).

## Analytical expression of the hyperbolic secant

Using the analytical expression of the [hyperbolic cosine](../hyperbolic-sine-and-cosine/) in terms of the [exponential function](../exponential-function/), the hyperbolic secant admits a closed form in terms of $e^{x}$ and $e^{-x}$. Substituting:

$$
\cosh(x) = \frac{e^{x} + e^{-x}}{2}
$$

into the definition $\mathrm{sech}(x) = 1/\cosh(x)$ and inverting the resulting fraction, we obtain:

$$
\mathrm{sech}(x) = \frac{2}{e^{x} + e^{-x}}
$$

Multiplying numerator and denominator by $e^{x}$ provides an equivalent form that makes the behaviour at $\pm\infty$ more transparent:

$$
\mathrm{sech}(x) = \frac{2e^{x}}{e^{2x} + 1}
$$

From this expression one reads off at once that $\mathrm{sech}(x) \to 0$ as $x \to \pm\infty$, while the value $\mathrm{sech}(0) = 1$ is recovered by direct substitution.

## Analytical expression of the hyperbolic cosecant

The derivation of the analytical expression for the hyperbolic cosecant follows the same pattern. Substituting:

$$
\sinh(x) = \frac{e^{x} - e^{-x}}{2}
$$

into the definition $\mathrm{csch}(x) = 1/\sinh(x)$, we obtain:

$$
\mathrm{csch}(x) = \frac{2}{e^{x} - e^{-x}}
$$

Multiplying numerator and denominator by $e^{x}$ gives the equivalent compact form:

$$
\mathrm{csch}(x) = \frac{2e^{x}}{e^{2x} - 1}
$$

This expression shows that the function approaches zero as $x \to \pm\infty$ and diverges at $x = 0$, where the denominator vanishes. The sign of $\mathrm{csch}(x)$ coincides with the sign of $x$, in agreement with the odd parity inherited from the hyperbolic sine.

## Hyperbolic secant and cosecant functions

The [hyperbolic secant function](../hyperbolic-secant-function/) $f(x) = \mathrm{sech}(x)$ assigns to each real number $x$ the value $1/\cosh(x)$. Its graph is a bell-shaped curve, everywhere positive, with maximum value $1$ at the origin and horizontal [asymptote](../asymptotes/) $y = 0$ in both directions. The [domain](../determining-the-domain-of-a-function/) of $\mathrm{sech}(x)$ is the entire real line, while its range is the interval $(0, 1]$.

+ Domain: $x \in \mathbb{R}$
+ Range: $y \in (0, 1]$
+ Periodicity: not periodic
+ Parity: [even](../even-and-odd-functions/), $\mathrm{sech}(-x) = \mathrm{sech}(x)$
+ Horizontal asymptote: $y = 0$ as $x \to \pm\infty$

The [hyperbolic cosecant function](../hyperbolic-cosecant-function/) $f(x) = \mathrm{csch}(x)$ assigns to each nonzero real number $x$ the value $1/\sinh(x)$. Its graph consists of two branches separated by a vertical asymptote at the origin: one for $x > 0$, where the function decreases from $+\infty$ toward $0$, and one for $x < 0$, where it increases from $0$ toward $-\infty$. The domain of $\mathrm{csch}(x)$ is the set of all nonzero real numbers, while its range is $\mathbb{R} \setminus \{0\}$.

+ Domain: $x \in \mathbb{R},\; x \neq 0$
+ Range: $y \in \mathbb{R},\; y \neq 0$
+ Periodicity: not periodic
+ Parity: [odd](../even-and-odd-functions/), $\mathrm{csch}(-x) = -\mathrm{csch}(x)$
+ Vertical asymptote: $x = 0$
+ Horizontal asymptote: $y = 0$ as $x \to \pm\infty$

## Relation to the circular secant and cosecant

The circular [secant and cosecant](../secant-and-cosecant/) are defined as reciprocals of the circular cosine and sine, which in turn arise from the geometry of the [unit circle](../unit-circle/). By exact analogy, the hyperbolic secant and cosecant are reciprocals of the hyperbolic cosine and sine, which arise from the geometry of the equilateral hyperbola. 

In both settings, the constraint that the coordinates of the underlying point satisfy the defining equation of the curve propagates to a corresponding identity for the reciprocal functions.

There is, however, a fundamental difference between the two cases: while the circular secant and cosecant are periodic with period $2\pi$ and satisfy $|\sec(\theta)| \geq 1$ and $|\csc(\theta)| \geq 1$ wherever defined, the hyperbolic secant is bounded by $1$ and tends to zero at infinity, while the hyperbolic cosecant is unbounded near the origin and tends to zero at infinity. 

The unit-circle bound, which forces the circular reciprocals away from zero, has no counterpart in the hyperbolic setting, where the right branch of the hyperbola extends without limit.

> Both the circular and the hyperbolic reciprocal functions encode the same geometric idea: each measures the reciprocal of a coordinate of a point on a curve, one on the unit circle and the other on the equilateral hyperbola. The contrast between bounded periodic behaviour and unbounded monotone decay is one of the recurrent themes that distinguish the circular and hyperbolic families.
