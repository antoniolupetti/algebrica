---
title: Fourier Series
source: https://algebrica.org/fourier-series/
license: CC BY-NC 4.0
tags:
  - fourier-coefficients
  - fourier-series
  - orthogonality
  - periodic-functions
  - trigonometric-series
---
## Definition

A Fourier series represents a periodic function as an infinite [series](../series/) of [sine](../sine-function/) and [cosine functions](../cosine-function/). More precisely, it shows that periodic behavior can be decomposed into elementary harmonic oscillations. This result expresses a structural property of periodic [functions](../functions/), since oscillatory components form a coordinate system for describing repetition.

Let $f : \mathbb{R} \to \mathbb{R}$ be a function that is periodic with period $2\pi$, meaning:

$$
f(x + 2\pi) = f(x) \ \forall x \in \mathbb{R}
$$

Assume that $f$ is [integrable](../definite-integrals/) on the [interval](../intervals/) $[-\pi,\pi]$. The Fourier series of $f$ is the formal trigonometric expansion:

$$
f(x) \sim \frac{a_0}{2}
+
\sum_{n=1}^{\infty}
a_n \cos(nx) + b_n \sin(nx)
$$

+ The symbol $\sim$ emphasizes that we are not yet asserting equality (we are defining a trigonometric series associated with $f$).
+ The question of whether the series converges to $f$ will be addressed later.
+ Each term $\cos(nx)$ and $\sin(nx)$ represents an oscillation of frequency $n$.
+ The expansion therefore decomposes $f$ into its harmonic components.

## Fourier coefficients

The coefficients $a_n$ and $b_n$ are defined by the following integrals:

$$
\begin{align}
a_0 &= \frac{1}{\pi}
\int_{-\pi}^{\pi} f(x)\ dx \\[6pt]
a_n &= \frac{1}{\pi}
\int_{-\pi}^{\pi} f(x)\cos(nx)\ dx \\[6pt]
b_n &= \frac{1}{\pi}
\int_{-\pi}^{\pi} f(x)\sin(nx)\ dx
\quad n \ge 1
\end{align}
$$

These formulas follow from a structural property of [sines and cosines](../sine-and-cosine/), namely their orthogonality over a full period. On the interval $[-\pi,\pi]$, trigonometric waves of different frequencies remain independent under integration:

$$
\begin{align}
\int_{-\pi}^{\pi} \cos(nx)\cos(mx)\ dx &=
\begin{cases}
\pi & n=m\neq 0 \\[6pt]
0 & n\ne m
\end{cases} \\[6pt]
\int_{-\pi}^{\pi} \sin(nx)\sin(mx)\ dx &=
\begin{cases}
\pi & n=m\neq 0 \\[6pt]
0 & n\ne m
\end{cases} \\[6pt]
\int_{-\pi}^{\pi} \sin(nx)\cos(mx)\ dx &= 0
\end{align}
$$

These relations let us recover each coefficient from the function itself. Suppose for a moment that the series converges to $f$ and that we may integrate it term by term. Multiplying the expansion by $\cos(mx)$ and integrating over $[-\pi,\pi]$, every product with $n\neq m$ vanishes, and so does each mixed term $\sin(nx)\cos(mx)$. Only the term with $n=m$ survives:

$$
\int_{-\pi}^{\pi} f(x)\cos(mx)\ dx
=
a_m \int_{-\pi}^{\pi} \cos^2(mx)\ dx
=
\pi a_m
$$

Solving for $a_m$ and renaming the index gives the formula for $a_n$. Repeating the argument with $\sin(mx)$ produces $b_n$, and integrating the bare expansion produces $a_0$. The orthogonality relations also turn the trigonometric system into an orthogonal family under the inner product:

$$
\langle f, g \rangle =
\int_{-\pi}^{\pi} f(x)g(x)\ dx
$$

Each coefficient measures how much of a specific harmonic direction is present in the function. In this sense, the Fourier expansion is a projection process in an infinite-dimensional space.

## Example: the sawtooth wave

This example shows how even a simple linear function acquires a rich harmonic structure when periodically extended. Consider the function $f(x) = x$, defined on $(-\pi,\pi)$ and extended periodically with period $2\pi$. This function is odd. Therefore:

$$
a_0 = 0
\quad
a_n = 0
$$

We compute the [sine](../sine-and-cosine/) coefficients:

$$
b_n =
\frac{1}{\pi}
\int_{-\pi}^{\pi}
x\sin(nx)\ dx
$$

Using [integration by parts](../integration-by-parts/), we obtain:

$$
b_n = \frac{2(-1)^{n+1}}{n}
$$

Hence the Fourier series is:

$$
x \sim
2
\sum_{n=1}^{\infty}
\frac{(-1)^{n+1}}{n}
\sin(nx)
$$

The point $x = \frac{\pi}{2}$ lies inside a period, away from the jumps of the extension at odd multiples of $\pi$, so the series converges there to the value $\frac{\pi}{2}$. Since $\sin(nx)$ vanishes for even $n$ and alternates between $1$ and $-1$ for odd $n$, the expansion collapses to:

$$
\frac{\pi}{2}
=
2\left(
1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots
\right)
$$

Dividing by $2$ recovers Leibniz's series for $\pi$:

$$
\frac{\pi}{4}
=
\sum_{k=0}^{\infty}
\frac{(-1)^k}{2k+1}
$$

> The coefficients decay like $\frac{1}{n}$. The slow decay reflects the fact that $f$ is continuous inside the period but its periodic extension has jump discontinuities at multiples of $\pi$, which influences convergence behavior.

## Example: the triangular wave

Consider now the even function $f(x) = |x|$ on $[-\pi,\pi]$, extended periodically with period $2\pi$. Because $f$ is even, every sine coefficient vanishes and the expansion contains only cosine terms. The constant term is the average value of $f$ over a period:

$$
a_0 =
\frac{1}{\pi}
\int_{-\pi}^{\pi} |x|\ dx
=
\frac{2}{\pi}
\int_{0}^{\pi} x\ dx
=
\pi
$$

For the remaining coefficients we use the evenness of the integrand and [integration by parts](../integration-by-parts/):

$$
a_n =
\frac{2}{\pi}
\int_{0}^{\pi} x\cos(nx)\ dx
=
\frac{2}{\pi}\cdot
\frac{(-1)^n - 1}{n^2}
$$

This expression vanishes when $n$ is even and equals $-\frac{4}{\pi n^2}$ when $n$ is odd. Writing the surviving terms with the index $2k+1$, the Fourier series is:

$$
|x| \sim
\frac{\pi}{2}
-
\frac{4}{\pi}
\sum_{k=0}^{\infty}
\frac{\cos\big((2k+1)x\big)}{(2k+1)^2}
$$

The function is continuous everywhere, including the corners at multiples of $\pi$, so the series converges to $f$ at every point. Evaluating at $x = 0$, where $|x| = 0$, isolates a numerical series:

$$
\sum_{k=0}^{\infty}
\frac{1}{(2k+1)^2}
=
\frac{\pi^2}{8}
$$

Splitting the sum over all positive integers into odd and even indices relates this value to the Basel series:

$$
\sum_{n=1}^{\infty}
\frac{1}{n^2}
=
\frac{\pi^2}{6}
$$

> Here the coefficients decay like $\frac{1}{n^2}$, faster than the $\frac{1}{n}$ rate of the sawtooth. The corner of $|x|$ is a milder singularity than a jump, and smoother periodic behavior produces faster decay of the harmonic amplitudes.

## Functions of arbitrary period

The construction extends to any period through a change of scale. Let $f$ be periodic with period $2L$ and integrable on $[-L,L]$. The [substitution](../integration-by-substitution/) $x = \frac{Lt}{\pi}$ maps $[-L,L]$ onto $[-\pi,\pi]$ and turns $f$ into a function of $t$ with period $2\pi$, to which the previous formulas apply. Translating the result back to $x$ gives the Fourier series:

$$
f(x) \sim
\frac{a_0}{2}
+
\sum_{n=1}^{\infty}
a_n \cos\frac{n\pi x}{L}
+
b_n \sin\frac{n\pi x}{L}
$$

The coefficients carry the same structure, with the period entering through the frequency $\frac{n\pi}{L}$:

$$
\begin{align}
a_0 &= \frac{1}{L}
\int_{-L}^{L} f(x)\ dx \\[6pt]
a_n &= \frac{1}{L}
\int_{-L}^{L} f(x)\cos\frac{n\pi x}{L}\ dx \\[6pt]
b_n &= \frac{1}{L}
\int_{-L}^{L} f(x)\sin\frac{n\pi x}{L}\ dx
\quad n \ge 1
\end{align}
$$

When $L = \pi$ these reduce to the formulas on $[-\pi,\pi]$. The discrete frequencies $\frac{n\pi}{L}$ replace the integers $n$, so a longer period packs the harmonics more densely along the frequency axis.

## Convergence of Fourier series

The definition of the Fourier series does not by itself guarantee convergence to the original function. A sufficient condition requires that $f$ be periodic and that $f$ together with its derivative $f'$ be piecewise continuous on a period. Concretely, on $[-\pi,\pi]$ the function should satisfy:

+ $f$ is bounded with finitely many maxima and minima
+ $f$ has finitely many discontinuities, all of jump type

Under these hypotheses the series converges at every point $x$. As with any [function series](../function-series/), its behaviour is read from the partial sums. Consider the $N$-th partial sum:

$$
S_N(x) =
\frac{a_0}{2}
+
\sum_{n=1}^{N}
a_n\cos(nx)+b_n\sin(nx)
$$

The limit of these partial sums equals the average of the one-sided limits of $f$ at the point:

$$
\lim_{N\to\infty}
S_N(x)
=
\frac{f(x^+)+f(x^-)}{2}
$$

Where $f$ is continuous the two one-sided limits coincide and the series returns $f(x)$. At a jump it settles on the midpoint between the left and right [limits](../limits/), so Fourier approximation reproduces the average local behavior rather than either one-sided value.

Near a jump the partial sums show a characteristic feature. As $N$ grows they overshoot the jump by a fixed proportion of its height, close to nine percent, and this overshoot does not shrink. Only the width of the region where it occurs contracts toward the discontinuity. This persistent overshoot is the Gibbs phenomenon.

The rate at which the coefficients decay mirrors the regularity of $f$:

+ If $f$ is continuously differentiable, the coefficients decay faster.
+ If $f$ has discontinuities, the decay is slower.
+ The smoother the function, the more rapidly the harmonic amplitudes decrease.

## Harmonics and applications

Each pair of terms of a fixed frequency combines into a single oscillation, the $n$-th harmonic of $f$:

$$
a_n \cos\frac{n\pi x}{L}
+
b_n \sin\frac{n\pi x}{L}
$$

Its amplitude records how strongly that frequency is present in the function:

$$
A_n = \sqrt{a_n^2 + b_n^2}
$$

The sequence of squared amplitudes $A_n^2$ describes how the function distributes its weight across frequencies, a description that physicists call the energy spectrum. Two periodic signals built from the same set of frequencies differ precisely in the relative sizes of these amplitudes.

Fourier introduced these series while studying heat conduction, and Daniel Bernoulli and Euler had already met them in the analysis of vibrating strings. The motivation is that many phenomena are periodic by nature, including tides, sound, and mechanical oscillations, so expressing them through periodic building blocks is natural. In music the same note played by two instruments produces different harmonic amplitudes, and this difference is what the ear perceives as timbre. The same expansions also solve the wave equation and the heat equation, where writing the solution as a sum of harmonics separates the spatial and temporal behavior.
