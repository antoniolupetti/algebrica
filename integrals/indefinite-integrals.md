---
title: Indefinite Integrals
source: https://algebrica.org/indefinite-integrals/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - definite-integral
  - fundamental-theorem-of-calculus
  - indefinite-integral
  - integration
  - integration-rules
  - linearity
  - power-rule
  - primitive
---
## Primitives

Every differentiable function has a unique [derivative](../derivatives/). The inverse problem is to determine whether a given function $f$ is the derivative of some function $F$. Any such function $F$ is a primitive (or antiderivative) of $f$. Let $I$ be an open [interval](../intervals/). A differentiable function $F\colon I \to \mathbb{R}$ is a primitive of $f\colon I \to \mathbb{R}$ when the following identity holds:

$$F'(x) = f(x) \qquad \forall x \in I$$

Not every function has a primitive on a given interval. [Continuity](../continuous-functions/) is sufficient. Every continuous function on an open interval $I$ has a primitive on $I$. For example, $F(x) = x^3$ is a primitive of $f(x) = 3x^2$. Its derivative is:

$$\frac{d}{dx} x^3 = 3x^2$$

A function need not be continuous to have a primitive. The following function is differentiable on $\mathbb{R}:$

$$
F(x) :=
\begin{cases}
x^2\sin(1/x) & \text{if } x \neq 0 \\[6pt]
0 & \text{if } x = 0
\end{cases}
$$

For $x \neq 0,$ its derivative is $F'(x) = 2x\sin(1/x) - \cos(1/x).$ At the origin, the derivative is:

$$F'(0) = \lim_{h \to 0}\frac{h^2\sin(1/h)}{h} = \lim_{h \to 0}h\sin(1/h) = 0$$

Thus $f := F'$ has $F$ as a primitive on $\mathbb{R},$ but $f$ is not continuous at $0$ because $\cos(1/x)$ has no limit as $x \to 0.$

By [Darboux's theorem](../darboux-theorem/), every derivative has the intermediate value property. Hence a function with a jump discontinuity has no primitive on any open interval containing the point of discontinuity.

- - -

Unlike derivatives, primitives are not unique. Since the derivative of any constant is zero, the functions $x^3$, $x^3 + 5$, and $x^3 - \frac{1}{2}$ are all primitives of $3x^2$. More generally, if $F(x)$ is a primitive of $f(x)$ on an interval $I$, then so is $F(x) + c$ for any $c \in \mathbb{R}$. The derivative of $F(x) + c$ is:

$$\frac{d}{dx}[F(x) + c] = F'(x) = f(x)$$

Conversely, any two primitives of the same function on an interval differ by a constant. If $F_1(x)$ and $F_2(x)$ are both primitives of $f(x)$ on $I$, then their difference has zero derivative:

$$\frac{d}{dx}[F_1(x) - F_2(x)] = F_1'(x) - F_2'(x) = f(x) - f(x) = 0$$

By [Lagrange's theorem](../lagrange-theorem/), a function with zero derivative on an interval is constant. Hence $F_1(x) - F_2(x) = c$ for some $c \in \mathbb{R}$.

## The indefinite integral

Suppose that $f$ has a primitive $F$ on an open interval $I$. The indefinite integral of $f$ on $I$ is the family of all its primitives. This family has the form $F(x) + c$, where $c \in \mathbb{R}$. We write this family as:

$$\int f(x) \ dx = F(x) + c \qquad c \in \mathbb{R}$$

Every member of this family has derivative $f$:

$$\frac{d}{dx}[F(x) + c] = f(x)$$

Equivalently, the integral of $F'$ is the family of functions $F + c.$

$$\int F'(x) \ dx = F(x) + c \qquad c \in \mathbb{R}$$

The [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/) relates primitives to definite integrals.

- - -

Find the primitive of $f(x) = 3x$ whose graph passes through the point $(2, 1)$. Every primitive has the form:

$$F(x) = \int 3x \ dx = \frac{3}{2}x^2 + c$$

Since the graph passes through $(2, 1)$, the constant must satisfy $F(2) = 1$:

$$
\begin{align}
\frac{3}{2}(2)^2 + c &= 1 \\[6pt]
6 + c &= 1 \\[6pt]
c &= -5
\end{align}
$$

The unique primitive satisfying the given condition is:

$$F(x) = \frac{3}{2}x^2 - 5$$

More generally, let $F_0$ be a primitive of $f$ on an open interval $I,$ and choose $x_0 \in I$ and $y_0 \in \mathbb{R}.$ Every primitive has the form $F_0 + c.$ The condition $F(x_0) = y_0$ is equivalent to $c = y_0 - F_0(x_0),$ so exactly one primitive has the prescribed value:

$$F(x) = F_0(x) + y_0 - F_0(x_0)$$

The graphs of the functions $F_0 + c$ are vertical translations of the graph of $F_0.$ Exactly one of these graphs passes through a prescribed point $(x_0, y_0).$

## Linearity properties

Suppose that $f$ and $g$ have primitives $F$ and $G$ on the same interval. Since $(F + G)' = f + g$, every primitive of $f + g$ has the form $F + G + c$:

$$\int [f(x) + g(x)] \ dx = F(x) + G(x) + c \qquad c \in \mathbb{R} \tag{1}$$

For every $k \in \mathbb{R}$, the identity $(kF)' = kf$ shows that every primitive of $kf$ has the form $kF + c$:

$$\int kf(x) \ dx = kF(x) + c \qquad k, c \in \mathbb{R} \tag{2}$$

These formulas are the linearity rules for indefinite integrals. They reduce the integral of a linear combination to primitives of its individual terms.

- - -

Compute the integral of $f(x) = 3x^2 + 2x$. By linearity, the integral is the sum of two terms, and the power rule applies to each:

$$\int (3x^2 + 2x) \ dx = \int 3x^2 \ dx + \int 2x \ dx$$

The two terms have constants $c_1$ and $c_2$, whose sum is another arbitrary constant $c$. Hence the integral is:

$$\int (3x^2 + 2x) \ dx = x^3 + x^2 + c \qquad c \in \mathbb{R}$$

- - -

Compute the integral of $f(x) = 5\sin(x)$. Since $5$ is constant, property $(2)$ gives:

$$\int 5\sin(x) \ dx = 5 \int \sin(x) \ dx$$

A primitive of $\sin(x)$ is $-\cos(x)$. Therefore, the integral is:

$$\int 5\sin(x) \ dx = -5\cos(x) + c \qquad c \in \mathbb{R}$$

## Integral of a power function

For every real exponent $a \neq -1$, the [power function](../powers/) $x^a$ has the following indefinite integral on $(0, +\infty)$:

$$\int x^a \ dx = \frac{x^{a+1}}{a+1} + c$$

When $a = -1$, the denominator is zero, so the formula is undefined. For this exponent, the primitive is logarithmic and has a separate formula. Compute the following integral:

$$\int (3x^4 + 5x^2) \ dx$$

Linearity and the power rule give:

$$\int (3x^4 + 5x^2) \ dx = 3 \int x^4 \ dx + 5 \int x^2 \ dx = 3 \cdot \frac{x^5}{5} + 5 \cdot \frac{x^3}{3} + c$$

Thus, the integral is:

$$\int (3x^4 + 5x^2) \ dx = \frac{3}{5}x^5 + \frac{5}{3}x^3 + c \qquad c \in \mathbb{R}$$

- - -

For $x > 0$, compute the following integral:

$$\int \left(4x^3 - \frac{3}{\sqrt{x}} + 2\cos x\right) \ dx$$

Linearity gives three terms:

$$\int 4x^3 \ dx - \int 3x^{-1/2} \ dx + \int 2\cos x \ dx$$

By the power rule, $x^4$ is a primitive of $4x^3$. Since $1/\sqrt{x} = x^{-1/2}$ for $x > 0$, $6\sqrt{x}$ is a primitive of $3x^{-1/2}$. Finally, $2\sin x$ is a primitive of $2\cos x$. Their signed sum is:

$$\int \left(4x^3 - \frac{3}{\sqrt{x}} + 2\cos x\right) \ dx = x^4 - 6\sqrt{x} + 2\sin x + c$$

> Differentiating $x^4 - 6\sqrt{x} + 2\sin x + c$ term by term gives the original integrand.

## The logarithmic integral

For $a = -1$, the denominator in the power-rule formula is zero. On each open interval contained in $\mathbb{R} \setminus \{0\}$, the corresponding integral is the [natural logarithm](../logarithms/) of the [absolute value](../absolute-value/):

$$\int \frac{1}{x} \ dx = \ln |x| + c$$

The function $\ln|x|$ has derivative $1/x$ for every $x \neq 0$. The absolute value is needed because $\ln x$ is defined only for $x > 0$, whereas $1/x$ is also defined for $x < 0$.

> The identity $\int \frac{1}{x} \ dx = \ln|x| + c$ holds separately on $(-\infty, 0)$ and on $(0, +\infty)$. On each interval the arbitrary constant may take a different value, so the most general antiderivative of $1/x$ on its full domain is not a single expression $\ln|x| + c$ with one constant, but a piecewise family with independent constants on the two components.

## Fundamental integration rules

The table lists the two linearity identities, the power rule for $a \neq -1$, and the logarithmic case $a = -1$.

[class="table-1"]

|                  |                                                                                                   |
| ---------------- | ------------------------------------------------------------------------------------------------- |
| Linearity        | $$\int (f(x) + g(x)) \ dx = F(x) + G(x) + c \qquad F'=f,\quad G'=g,\quad c \in \mathbb{R}$$    |
| Linearity        | $$\int kf(x) \ dx = kF(x) + c \qquad F'=f,\quad k,c \in \mathbb{R}$$                         |
| Power rule       | $$\int x^a \ dx = \dfrac{x^{a+1}}{a+1} + c \qquad a \in \mathbb{R}\setminus\{-1\},\quad x > 0$$ |
| Logarithmic case | $$\int \dfrac{1}{x} \ dx = \ln \lvert x \rvert + c$$                                          |
[/class]

## Common integrals

The table lists basic indefinite integrals. The derivative of each right-hand side is the corresponding integrand.

[class="table-1 -right"]

|                                                                       |                                                  |
| --------------------------------------------------------------------- | ------------------------------------------------ |
| $$\int \frac{1}{x} \ dx = \ln \lvert x \rvert + c$$                   | [more](../integral-of-rational-functions/)       |
| $$\int a^x \ dx = \frac{a^x}{\ln a} + c \qquad a > 0,\quad a \neq 1$$ | [more](../integral-of-the-exponential-function/) |
| $$\int \sin x \ dx = -\cos x + c$$                                    | [more](../integral-of-trigonometric-functions/)  |
| $$\int \cos x \ dx = \sin x + c$$                                     | [more](../integral-of-trigonometric-functions/)  |
| $$\int \frac{1}{\sin^2 x} \ dx = -\cot x + c$$                        | [more](../integral-of-trigonometric-functions/)  |
| $$\int \frac{1}{\cos^2 x} \ dx = \tan x + c$$                         | [more](../integral-of-trigonometric-functions/)  |
| $$\int \sec^2 x \ dx = \tan x + c$$                                   | [more](../integral-of-trigonometric-functions/)  |
| $$\int \sec x \tan x \ dx = \sec x + c$$                              | [more](../integral-of-trigonometric-functions/)  |
| $$\int \csc^2 x \ dx = -\cot x + c$$                                  | [more](../integral-of-trigonometric-functions/)  |
| $$\int \csc x \cot x \ dx = -\csc x + c$$                             | [more](../integral-of-trigonometric-functions/)  |
| $$\int \frac{1}{1 + x^2} \ dx = \arctan x + c$$                       |                                                  |
| $$\int \frac{1}{\sqrt{1 - x^2}} \ dx = \arcsin x + c$$                |                                                  |

[/class]

The page on [integration strategies](../integration-strategies/) examines the structure of common integrands and explains how to choose among direct integration, substitution, integration by parts, and algebraic or trigonometric reduction.

> The identities above hold on any interval where the integrand is defined and continuous. [Integration by substitution](../integration-by-substitution/) and [integration by parts](../integration-by-parts/) apply to some integrals outside this table, but neither method guarantees an elementary primitive. If $f$ is continuous on $[a, b]$ and $F$ is continuous on $[a, b]$ with $F'(x) = f(x)$ for every $x \in (a, b)$, the Fundamental Theorem of Calculus gives $\int_a^b f(x) \ dx = F(b) - F(a).$ This [definite integral](../definite-integrals/) is the net signed area between the graph of $f$ and the $x$-axis over $[a, b]$.
