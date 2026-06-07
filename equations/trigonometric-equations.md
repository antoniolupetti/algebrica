---
title: Trigonometric Equations
source: https://algebrica.org/trigonometric-equations/
license: CC BY-NC 4.0
tags:
  - arccosine
  - arcsine
  - arctangent
  - cosine
  - sine
  - tangent
  - trigonometric-equation
  - unit-circle
---
## Definition

A trigonometric equation is an [equation](../equations/) in which the unknown appears as the argument of one or more trigonometric functions. The simplest cases involve a single function set equal to a constant, in the form:

$$\sin(x) = m, \quad \cos(x) = m, \quad \tan(x) = m$$

A second family of equations places a function of the unknown inside the trigonometric function, in the form:

$$\sin[f(x)] = m, \quad \cos[f(x)] = m, \quad \tan[f(x)] = m$$

The two families are treated below. Because the trigonometric functions are periodic, each solvable equation of this kind admits infinitely many solutions, and the central task is to describe them all through a compact general formula. Replacing the equality with an inequality sign leads to a [trigonometric inequality](../trigonometric-inequalities/), where the same periodicity produces an infinite union of intervals rather than a discrete family of solutions.

## Equations of the form sine of x equals m

Consider the equation

$$\sin(x) = m \tag{1}$$

Solving it means determining every [angle](../angles-and-angular-measure/) $x$ whose [sine](../sine-and-cosine/) equals $m$. The sine function takes values in the interval $[-1, 1]$, so a real solution exists only when $-1 \leq m \leq 1$. If $|m| > 1$, equation $(1)$ has no real solution and is called impossible.

On the [unit circle](../unit-circle/), the equation corresponds to the horizontal line $y = m$. When $-1 < m < 1$, this line meets the circle at two distinct points, symmetric with respect to the vertical axis, which produce two angles in $[0, 2\pi)$:

$$x = \alpha \quad \text{and} \quad x = \pi - \alpha$$

Here $\alpha$ is the [arcsine](../arcsine-and-arccosine/) of $m$, that is the unique angle in $[-\pi/2, \pi/2]$ satisfying $\sin(\alpha) = m$. Since the sine function is periodic with period $2\pi$, the complete set of solutions is:

$$
\begin{align}
x &= \alpha + 2k\pi \\[6pt]
x &= \pi - \alpha + 2k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

The integer $k$ ranges over all of $\mathbb{Z}$, where $\mathbb{Z}$ denotes the set of [integers](../integers/), and accounts for the periodic nature of the function.

> The two families coincide at the boundary values of $m$. When $m = 1$ the line is tangent to the circle at the top, giving the single family $x = \pi/2 + 2k\pi$; when $m = -1$ it gives $x = -\pi/2 + 2k\pi$. When $m = 0$ the solutions merge into $x = k\pi$.

As an example, consider the equation

$$\sin(x) = \frac{1}{2}$$

The reference angle is $\alpha = \pi/6$, since $\sin(\pi/6) = 1/2$. The two families of solutions are therefore:

$$
\begin{align}
x &= \frac{\pi}{6} + 2k\pi \\[6pt]
x &= \pi - \frac{\pi}{6} + 2k\pi = \frac{5\pi}{6} + 2k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

Within the interval $[0, 2\pi)$ these reduce to the two values $x = \pi/6$ and $x = 5\pi/6$.

## Equations of the form cosine of x equals m

The equation

$$\cos(x) = m \tag{2}$$

is governed by the same range condition, since the [cosine](../sine-and-cosine/) also takes values in $[-1, 1]$. For $-1 < m < 1$ the line $x = m$ meets the unit circle at two points symmetric with respect to the horizontal axis, which produce two opposite angles. Writing $\alpha = \arccos(m)$ for the [arccosine](../arcsine-and-arccosine/) of $m$, the unique value in $[0, \pi]$ with $\cos(\alpha) = m$, the general solution is:

$$x = \pm\alpha + 2k\pi, \quad k \in \mathbb{Z}$$

The two signs encode the symmetry of the cosine about the horizontal axis, so the solutions in $[0, 2\pi)$ are $\alpha$ and $2\pi - \alpha$.

As an example, consider the equation

$$\cos(x) = \frac{1}{2}$$

From the known value $\cos(\pi/3) = 1/2$ we take $\alpha = \pi/3$, and the general solution is:

$$x = \pm\frac{\pi}{3} + 2k\pi, \quad k \in \mathbb{Z}$$

Within the interval $[0, 2\pi)$ this gives the two values:

$$x_1 = \frac{\pi}{3}, \quad x_2 = \frac{5\pi}{3}$$

> The boundary values again collapse the two families into one: $m = 1$ gives $x = 2k\pi$, $m = -1$ gives $x = \pi + 2k\pi$, and $m = 0$ gives $x = \pi/2 + k\pi$.

## Equations of the form tangent of x equals m

The equation

$$\tan(x) = m \tag{3}$$

behaves differently, because the [tangent](../tangent-and-cotangent/) is not bounded. Its range is the whole real line, so equation $(3)$ has a solution for every real value of $m$, and no range condition is required. The tangent is periodic with period $\pi$, so once a single solution is known the rest follow by adding integer multiples of $\pi$. Writing $\alpha = \arctan(m)$ for the [arctangent](../arctangent-and-arccotangent/) of $m$, the value in $(-\pi/2, \pi/2)$ with $\tan(\alpha) = m$, the general solution is:

$$x = \arctan(m) + k\pi, \quad k \in \mathbb{Z}$$

As an example, consider the equation

$$\tan(x) = 2$$

The value $2$ is not one of the angles with a familiar tangent, so the principal angle is expressed directly through the arctangent. The general solution is:

$$x = \arctan(2) + k\pi, \quad k \in \mathbb{Z}$$

When the value of the function is not a standard one, the corresponding inverse function provides the principal angle. The same approach applies to the arcsine and the arccosine, which return the principal angle for any admissible value of the sine or cosine.

## Equations solved by substitution

A second family of equations places a function of the unknown inside the trigonometric function, the simplest case being:

$$\sin[f(x)] = m \tag{4}$$

The strategy is to treat $f(x)$ as a new unknown. Setting $u = f(x)$ reduces the problem to a simple equation $\sin(u) = m$ of the kind treated above. Once the general solution for $u$ is written, the substitution is reversed and the resulting equations are solved for $x$. As with every sine equation, a real solution exists only when $-1 \leq m \leq 1$.

Consider the equation

$$\sin(2x) = \frac{1}{2}$$

The value $1/2$ lies in the admissible range, so with $u = 2x$ the equation $\sin(u) = 1/2$ has the two families:

$$
\begin{align}
u &= \frac{\pi}{6} + 2k\pi \\[6pt]
u &= \frac{5\pi}{6} + 2k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

Reversing the substitution $u = 2x$ gives:

$$
\begin{align}
2x &= \frac{\pi}{6} + 2k\pi \\[6pt]
2x &= \frac{5\pi}{6} + 2k\pi
\end{align}
$$

Dividing both equations by $2$, the solutions for $x$ are:

$$
\begin{align}
x &= \frac{\pi}{12} + k\pi \\[6pt]
x &= \frac{5\pi}{12} + k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

> Dividing the periodic term by the coefficient of $x$ is what shrinks the period: the angle $u = 2x$ has period $2\pi$, so $x$ has period $\pi$. Forgetting to divide the term $2k\pi$ along with the rest is the most common error in these equations, and it discards half of the solutions.

## A complete worked example

Solve the equation

$$\cos(3x + 2) = \frac{1}{\sqrt{2}}$$

The argument $3x + 2$ plays the role of the substituted variable $u = 3x + 2$, and the equation becomes $\cos(u) = 1/\sqrt{2}$. Since $\cos(\pi/4) = 1/\sqrt{2}$, the cosine equation has the general solution:

$$u = \pm\frac{\pi}{4} + 2k\pi, \quad k \in \mathbb{Z}$$

Reversing the substitution, the variable $x$ satisfies the two equations:

$$
\begin{align}
3x + 2 &= \frac{\pi}{4} + 2k\pi \\[6pt]
3x + 2 &= -\frac{\pi}{4} + 2k\pi
\end{align}
$$

Subtracting $2$ from both sides isolates the term in $x$:

$$
\begin{align}
3x &= \frac{\pi}{4} - 2 + 2k\pi \\[6pt]
3x &= -\frac{\pi}{4} - 2 + 2k\pi
\end{align}
$$

Dividing each equation by $3$ gives the solutions:

$$
\begin{align}
x &= \frac{\pi}{12} - \frac{2}{3} + \frac{2k\pi}{3} \\[6pt]
x &= -\frac{\pi}{12} - \frac{2}{3} + \frac{2k\pi}{3}, \quad k \in \mathbb{Z}
\end{align}
$$

Collecting the constant terms over a common denominator, the general solution can be written in the compact form:

$$
\begin{align}
x &= \frac{\pi - 8}{12} + \frac{2k\pi}{3} \\[6pt]
x &= \frac{-\pi - 8}{12} + \frac{2k\pi}{3}, \quad k \in \mathbb{Z}
\end{align}
$$

These two families describe every value of $x$ that satisfies the original equation.

## Equations reducible to an algebraic equation

A broad class of trigonometric equations contains a single trigonometric function, possibly raised to a power, rather than the bare function set equal to a constant. Such equations can be reduced to an ordinary algebraic equation by introducing a new variable equal to the trigonometric function. Once the algebraic equation is solved, each admissible value produces an elementary trigonometric equation of the kind treated above.

Consider the equation:

$$2\sin^2(x) - 3\sin(x) + 1 = 0$$

The sine is the only function present, so the substitution $t = \sin(x)$ turns the equation into a [quadratic equation](../quadratic-equations/):

$$2t^2 - 3t + 1 = 0$$

Applying the [quadratic formula](../quadratic-formula/) gives:

$$t = \frac{3 \pm \sqrt{9 - 8}}{4} = \frac{3 \pm 1}{4}$$

so $t_1 = 1$ and $t_2 = \frac{1}{2}$. Both values lie in the interval $[-1, 1]$, so both are admissible.

- - -

Reversing the substitution $t = \sin(x)$ produces two elementary equations. The first is:

$$\sin(x) = 1$$

which gives the single family of solutions:

$$x = \frac{\pi}{2} + 2k\pi, \quad k \in \mathbb{Z}$$

The second is:

$$\sin(x) = \frac{1}{2}$$

which gives the two families:

$$
\begin{align}
x &= \frac{\pi}{6} + 2k\pi \\[6pt]
x &= \frac{5\pi}{6} + 2k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

> A value of the auxiliary variable outside the interval $[-1, 1]$ must be discarded when the function is a sine or cosine, since neither can exceed that range. No such restriction applies when the function is a tangent, whose range is the whole real line.

## Equations with mixed functions

When an equation contains different trigonometric functions, a preliminary step is needed to express every term through a single function before the substitution can be applied. The [trigonometric identities](../trigonometric-identities/) provide the necessary tools: the Pythagorean identity $\sin^2(x) + \cos^2(x) = 1$ converts a square of one function into the other, while the double angle formulas rewrite $\sin(2x)$ and $\cos(2x)$ in terms of $\sin(x)$ and $\cos(x)$.

Consider the equation:

$$2\cos^2(x) + \sin(x) - 1 = 0$$

The cosine and the sine appear together, so the equation is not yet reducible to a single function. Applying the Pythagorean identity in the form $\cos^2(x) = 1 - \sin^2(x)$ rewrites every term through the sine:

$$2\bigl(1 - \sin^2(x)\bigr) + \sin(x) - 1 = 0$$

Expanding and collecting like terms gives:

$$-2\sin^2(x) + \sin(x) + 1 = 0$$

Multiplying both sides by $-1$ produces the standard form:

$$2\sin^2(x) - \sin(x) - 1 = 0$$

- - -

Setting $t = \sin(x)$, the equation becomes the [quadratic equation](../quadratic-equations/):

$$2t^2 - t - 1 = 0$$

Applying the [quadratic formula](../quadratic-formula/) gives:

$$t = \frac{1 \pm \sqrt{1 + 8}}{4} = \frac{1 \pm 3}{4}$$

so $t_1 = 1$ and $t_2 = -\frac{1}{2}$. Both values lie in $[-1, 1]$ and are therefore admissible.

- - -

Reversing the substitution $t = \sin(x)$ produces two elementary equations. The first is:

$$\sin(x) = 1$$

which gives the solution:

$$x = \frac{\pi}{2} + 2k\pi, \quad k \in \mathbb{Z}$$

The second is:

$$\sin(x) = -\frac{1}{2}$$

which gives the two families:

$$
\begin{align}
x &= -\frac{\pi}{6} + 2k\pi \\[6pt]
x &= \frac{7\pi}{6} + 2k\pi, \quad k \in \mathbb{Z}
\end{align}
$$

> The Pythagorean identity preserves equivalence, so no extraneous solutions are introduced. Care is needed instead when an equation is divided by a trigonometric function, since the values that make that function vanish may themselves be solutions and would otherwise be lost.

- - -

Equations in which several trigonometric functions appear together with the same degree in every term form a separate class, treated in the discussion of [homogeneous trigonometric equations](../homogeneous-trigonometric-equations/). The [reduction formulas](../reduction-formulas-and-reference-angles/) are often useful for rewriting an argument before solving.
