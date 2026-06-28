---
title: Cosecant Function
source: https://algebrica.org/cosecant-function/
license: CC BY-NC 4.0
tags:
  - cosecant
  - derivatives
  - trigonometric-functions
  - trigonometry
---

## Introduction

> The geometric construction of the cosecant from the [unit circle](../unit-circle/) is developed in [secant and cosecant](../secant-and-cosecant/). Here, the cosecant is treated as a real [function](../functions/) of a real variable.

The cosecant function $f(x) = \csc(x)$ assigns to each angle $x,$ measured in [radians](../angles-and-angular-measure/), the reciprocal of its [sine](../sine-function/) value, defined wherever $\sin(x) \neq 0.$ Its graph is a periodic curve with period $2\pi$ and has vertical [asymptotes](../asymptotes/) where the sine of $x$ vanishes, at $x = k\pi$ with $k \in \mathbb{Z}.$ The [domain](../determining-the-domain-of-a-function/) is the set of all real numbers except these points, and the range is $(-\infty, -1] \cup [1, +\infty).$

![IMG. 1](../trigonometry/svg/secant-and-cosecant-4.svg)


The cosecant is the reciprocal of the sine, so it stays bounded where the sine is near $\pm 1$ and grows without bound as the sine approaches zero:

$$\csc(x) = \frac{1}{\sin(x)}$$

Because the sine never exceeds $1$ in absolute value, its reciprocal never falls between $-1$ and $1,$ and each branch reaches a single extremum of $1$ or $-1$ where the sine equals $\pm 1$ before diverging toward the neighbouring asymptotes.

## Properties

The following properties of the cosecant function follow from its definition as the reciprocal of the sine.

+ [Domain](../determining-the-domain-of-a-function/): $\{\ x \in \mathbb{R} \mid x \neq k\pi \ \text{ for all } k \in \mathbb{Z} \ \}$
+ Range: $y \in (-\infty, -1] \cup [1, +\infty)$
+ Periodicity: periodic in $x$ with period $2\pi$
+ Parity: [odd](../even-and-odd-functions/), with $\csc(-x) = -\csc(x)$
+ The graph has vertical [asymptotes](../asymptotes/) at $x = k\pi$ with $k \in \mathbb{Z}$

## Relation with the cotangent

The cosecant and the [cotangent](../tangent-function/) are tied by a [Pythagorean identity](../pythagorean-identity/). Dividing $\sin^2(x) + \cos^2(x) = 1$ by $\sin^2(x)$ and using the reciprocal definitions gives:

$$\csc^2(x) = 1 + \cot^2(x)$$

The two functions share the same vertical asymptotes, and the cosecant grows together with the cotangent.

## Limits, derivatives, and integrals of the cosecant function

Near $x = \pi/2$ the sine reaches its maximum, so the cosecant takes its least positive value:

$$\lim_{x \to \frac{\pi}{2}} \csc(x) = 1$$

The behaviour near the vertical asymptote at the origin is described by one-sided limits. As $x$ approaches $0$ from the right the sine is positive and tends to zero, so the function grows without bound,

$$\lim_{x \to 0^+} \csc(x) = +\infty$$

while from the left the sine is negative and the values diverge to negative infinity,

$$\lim_{x \to 0^-} \csc(x) = -\infty$$

The function is [continuous](../continuous-functions/) and differentiable on its domain. Its [derivative](../derivatives/) is:

$$\frac{d}{dx}\csc(x) = -\csc(x)\cot(x)$$

The [indefinite integral](../indefinite-integrals/) is:

$$\int \csc(x) \ dx = -\ln\left|\csc(x) + \cot(x)\right| + c$$

> A broader treatment of trigonometric integrals, with the transformation and substitution techniques for the more complex cases, is given in [trigonometric function integrals](../integral-of-trigonometric-functions/).

The cosecant function can also be written using [imaginary](../complex-numbers/) numbers. With $e^{ix}$ the [exponential function](../exponential-function/) of base $e$ and $i$ the imaginary unit, [Euler's formula](../eulers-formula/) gives:

$$\csc(x) = \frac{2i}{e^{ix} - e^{-ix}}$$
