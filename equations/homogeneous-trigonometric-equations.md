---
title: Homogeneous Trigonometric Equations
source: https://algebrica.org/homogeneous-trigonometric-equations/
license: CC BY-NC 4.0
tags:
  - tangent
  - trigonometric-equation
  - trigonometric-identities
---

## What are homogeneous trigonometric equations

Homogeneous trigonometric equations are [trigonometric equations](../trigonometric-equations/) in which every term involves trigonometric functions, such as [sine and cosine](../sine-and-cosine/), raised to the same degree. A first-degree homogeneous equation has the general form:

$$a\sin x + b\cos x = 0$$

Each term has degree $1$, and $a$ and $b$ are [real coefficients](../types-of-numbers/). The general first-degree trigonometric equation is:

$$a\sin x + b\cos x + c = 0$$

This equation is homogeneous when the constant term satisfies $c = 0$. The same idea extends to the second degree, where only second-degree terms appear:

$$a\sin^2 x + b\sin x\cos x + c\cos^2 x = 0$$

> The definition generalises to the third, fourth, and higher degrees. In every case all terms must involve trigonometric [functions](../functions/) raised to the same degree, so that the equation remains homogeneous.

A homogeneous equation of degree $n$ can be solved by dividing each term by $\cos^n x$, which transforms it into a polynomial equation in $\tan x$.

## Dividing by cosine and the case where cosine vanishes

Dividing every term by $\cos^n x$ is legitimate only when $\cos x \neq 0$. The values $x = \frac{\pi}{2} + k\pi$, where the cosine vanishes, are excluded by the division and must be examined separately, otherwise some solutions may be lost.

The verification is immediate. When $\cos x = 0$ the sine equals $\pm 1$, so substituting these values into a homogeneous equation of degree $n$ leaves only the term in which $\sin x$ appears with the full degree $n$. For the second-degree equation $a\sin^2 x + b\sin x\cos x + c\cos^2 x = 0$ this term is $a\sin^2 x$, which reduces to $a$. The values $x = \frac{\pi}{2} + k\pi$ are therefore solutions precisely when $a = 0$, that is, when the term of highest degree in $\sin x$ is absent.

> In practice it is enough to check whether $x = \frac{\pi}{2} + k\pi$ satisfies the original equation. If it does, these values are added to the solutions obtained from the equation in $\tan x$. If it does not, the division by $\cos^n x$ loses nothing and the method applies without restriction.

## Example 1

Consider the first-degree homogeneous trigonometric equation:

$$\sin x - \sqrt{3}\cos x = 0$$

- - -

Before dividing, observe that $x = \frac{\pi}{2} + k\pi$ gives $\sin x = \pm 1$ and $\cos x = 0$, so the left-hand side equals $\pm 1$, which is never zero. The values where the cosine vanishes are not solutions, and dividing by $\cos x$ is safe. This division gives:

$$\frac{\sin x}{\cos x} - \sqrt{3} = 0$$

Since the ratio of sine to cosine is the [tangent](../tangent-and-cotangent/), the equation can be rewritten in terms of $\tan x$:

$$\tan x = \sqrt{3}$$

The value that satisfies this equation is:

$$x = \arctan(\sqrt{3}) = \frac{\pi}{3}$$

Since the tangent is periodic with period $\pi$, the general solution is:

$$x = \frac{\pi}{3} + k\pi, \quad k \in \mathbb{Z}$$

Whenever [trigonometric identities](../trigonometric-identities/) allow an equation to be rewritten in homogeneous form, doing so is generally preferable, since it simplifies the calculations.

## Example 2

Consider the second-degree trigonometric equation:

$$\sin^2 x + \sin 2x - \cos^2 x = 0$$

This is not homogeneous as written, because the terms do not all share the same degree. In particular $\sin 2x$ is a first-degree term, while $\sin^2 x$ and $\cos^2 x$ are second-degree terms. Dividing every term by $\cos^2 x$ is therefore not yet possible, since the first-degree term would not transform into a useful expression. The method applies only when all terms have the same degree.

- - -

Using the double angle formula from the [trigonometric identities](../trigonometric-identities/), $\sin 2x$ can be rewritten as $2\sin x\cos x$. The equation becomes:

$$\sin^2 x + 2\sin x\cos x - \cos^2 x = 0$$

This is now a second-degree homogeneous equation. The values $x = \frac{\pi}{2} + k\pi$ give a left-hand side equal to $1$, so they are not solutions, and dividing every term by $\cos^2 x$ is admissible:

$$\frac{\sin^2 x}{\cos^2 x} + \frac{2\sin x\cos x}{\cos^2 x} - \frac{\cos^2 x}{\cos^2 x} = 0$$

- - -

Simplifying each term gives a [quadratic equation](../quadratic-equations/) in $\tan x$:

$$\tan^2 x + 2\tan x - 1 = 0$$

Substituting $t = \tan x$, the equation becomes:

$$t^2 + 2t - 1 = 0$$

Applying the [quadratic formula](../quadratic-formula/):

$$t = \frac{-2 \pm \sqrt{4 + 4}}{2} = \frac{-2 \pm 2\sqrt{2}}{2} = -1 \pm \sqrt{2}$$

The two solutions are:

$$t_1 = -1 + \sqrt{2}, \quad t_2 = -1 - \sqrt{2}$$

- - -

Substituting back $t = \tan x$ gives:

$$\tan x = -1 + \sqrt{2} \quad \text{and} \quad \tan x = -1 - \sqrt{2}$$

The general solutions are therefore:

$$
\begin{align}
x_1 &= \arctan(-1 + \sqrt{2}) + k\pi, \quad k \in \mathbb{Z} \\[6pt]
x_2 &= \arctan(-1 - \sqrt{2}) + k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

## Example 3

A trigonometric equation with a nonzero constant term can often be reduced to a homogeneous one. Consider the second-degree equation:

$$2\sin^2 x - 3\sin x\cos x + 3\cos^2 x = 1$$

The constant on the right-hand side prevents the terms from sharing the same degree, since $1$ has degree zero. The [Pythagorean identity](../pythagorean-identity/) provides the tool to restore homogeneity, because it allows the constant to be written as a second-degree expression:

$$1 = \sin^2 x + \cos^2 x$$

- - -

Replacing $1$ with this identity and moving every term to the left-hand side gives:

$$2\sin^2 x - 3\sin x\cos x + 3\cos^2 x - \sin^2 x - \cos^2 x = 0$$

Collecting the like terms produces a second-degree homogeneous equation:

$$\sin^2 x - 3\sin x\cos x + 2\cos^2 x = 0$$

The values $x = \frac{\pi}{2} + k\pi$ make the left-hand side equal to $1$, so they are not solutions and the division by $\cos^2 x$ is admissible. Dividing each term gives a quadratic equation in $\tan x$:

$$\tan^2 x - 3\tan x + 2 = 0$$

- - -

Substituting $t = \tan x$ and factoring the [quadratic equation](../quadratic-equations/):

$$t^2 - 3t + 2 = (t - 1)(t - 2) = 0$$

The two roots are $t = 1$ and $t = 2$, which correspond to:

$$\tan x = 1 \quad \text{and} \quad \tan x = 2$$

The general solutions are therefore:

$$
\begin{align}
x_1 &= \frac{\pi}{4} + k\pi, \quad k \in \mathbb{Z} \\[6pt]
x_2 &= \arctan(2) + k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

## Example 4

The following equation shows a case in which the values where the cosine vanishes are genuine solutions, so the preliminary check is essential. Consider the second-degree homogeneous equation:

$$\sin x\cos x - \sqrt{3}\cos^2 x = 0$$

The term in $\sin^2 x$ is absent, which means the coefficient $a$ of the highest power of $\sin x$ is zero. According to the criterion established above, the values $x = \frac{\pi}{2} + k\pi$ should then be solutions. Substituting them confirms it: $\sin x = \pm 1$ and $\cos x = 0$ give $\pm 1 \cdot 0 - \sqrt{3} \cdot 0 = 0$. These values satisfy the equation and form the first family of solutions:

$$x = \frac{\pi}{2} + k\pi, \quad k \in \mathbb{Z}$$

- - -

For the remaining solutions, where $\cos x \neq 0$, dividing every term by $\cos^2 x$ gives an equation in $\tan x$:

$$\frac{\sin x\cos x}{\cos^2 x} - \sqrt{3}\frac{\cos^2 x}{\cos^2 x} = 0$$

Simplifying each term reduces the equation to:

$$\tan x - \sqrt{3} = 0$$

This gives $\tan x = \sqrt{3}$, whose general solution is:

$$x = \frac{\pi}{3} + k\pi, \quad k \in \mathbb{Z}$$

- - -

The complete solution set combines the two families obtained:

$$
\begin{align}
x_1 &= \frac{\pi}{2} + k\pi, \quad k \in \mathbb{Z} \\[6pt]
x_2 &= \frac{\pi}{3} + k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

The same conclusion can be reached by factoring the original equation as $\cos x(\sin x - \sqrt{3}\cos x) = 0$, which separates the two branches directly. The first factor reproduces the solutions where the cosine vanishes, the second reproduces those obtained from the equation in $\tan x$. This confirms that the branch $\cos x = 0$ is a true solution and would have been lost by dividing without the preliminary check.
