---
title: Integration Strategies
source: https://algebrica.org/integration-strategies/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - indefinite-integral
  - integration
  - integration-by-parts
  - integration-by-substitution
  - integration-rules
  - linearity
  - power-rule
  - standard-integrals
---
## Recognising the form of an integrand

At first, integration often seems more difficult than differentiation. The notation is unfamiliar, the definition uses a [limit](../limits/) of sums over partitions, and an exercise usually requires a choice before the calculation begins. Most integrals in a calculus course, however, use a small table of antiderivatives, a few general methods and the ability to recognise the form of the integrand.

Differentiation has a fixed procedure at this level. For an elementary [function](../functions/) built from differentiable components, the rules for sums, products, quotients and [compositions](../composite-functions/) produce its derivative in finitely many steps. Integration has no corresponding procedure. In particular, the antiderivative of a product or quotient cannot be obtained directly from antiderivatives of its factors. The form of the integrand determines which rewriting or method is appropriate.

The same integrand may be evaluated by substitution, integration by parts or algebraic rewriting, and the resulting calculations can have very different lengths. A good choice makes the next integral simpler. A poor choice may make it longer or start a repetition that does not terminate. For example, integration by parts applied to $\int xe^x \ dx,$ with the exponential differentiated and the power integrated, gives:

$$\int xe^x \ dx = \frac{x^2}{2}e^x - \int \frac{x^2}{2}e^x \ dx$$

Repeating this choice raises the degree of the algebraic factor at every step. With $u=x$ and $dv=e^x \ dx,$ differentiation lowers the degree of the polynomial factor, and one application gives the antiderivative. A substitution passes the same test only when the new integrand is simpler than the original one.

Within the families treated in a standard calculus course, the calculation is largely mechanical once the form of the integrand has been recognised. Even a complicated integrand usually reduces to a finite sequence of algebraic rewritings and standard techniques. Experience is needed chiefly to choose a short sequence and to abandon a substitution or integration by parts when it makes the expression more complicated.

Memorisation is part of this process. The basic antiderivatives and a small set of algebraic and trigonometric identities must be memorised. When these formulas are recalled immediately, a complicated integrand can be separated into familiar parts. If each formula has to be derived or consulted, the underlying pattern is harder to see.

Differentiation checks every proposed antiderivative. If the derivative is the original integrand, the calculation is correct, regardless of how the antiderivative was found.

Throughout this page, every formula is understood on a connected [interval](../intervals/) where all the expressions involved are defined.

## Basic antiderivatives

A short table of basic antiderivatives is the starting point for longer calculations. The simplest case is the integral of the zero function:

$$\int 0 \ dx = c$$

By [Lagrange's theorem](../lagrange-theorem/), a function with zero derivative on an interval is constant. Thus the antiderivatives of the zero function are exactly the constant functions. For the constant function equal to $1,$ the integrand is often left implicit:

$$\int 1 \ dx = \int dx = x + c$$

The identity holds because $\frac{d}{dx}x=1.$

- - -

The power rule holds for every real exponent except $-1,$ on each interval where the power is defined:

$$\int x^n \ dx = \frac{x^{n+1}}{n+1} + c \qquad n \neq -1$$

Differentiating the right-hand side confirms it:

$$\frac{d}{dx}\left(\frac{x^{n+1}}{n+1}\right) = \frac{(n+1)x^{n}}{n+1} = x^{n}$$

The exponent $n=-1$ is excluded because it makes the denominator vanish. Its antiderivative is logarithmic:

$$\int \frac{1}{x} \ dx = \ln|x| + c$$

The [absolute value](../absolute-value/) is present because $1/x$ is defined on both $(-\infty,0)$ and $(0,+\infty),$ while the [logarithmic function](../logarithmic-function/) accepts only positive arguments.

- - -

The table below contains the formulas used most often. Each one is an entry in the table of [derivatives](../derivatives/) read in reverse.

[class="table-1"]

|                     |                                                                        |
| ------------------- | ---------------------------------------------------------------------- |
| Zero function       | $$\int 0 \ dx = c$$                                                    |
| Constant            | $$\int dx = x + c$$                                                    |
| Power rule          | $$\int x^n \ dx = \dfrac{x^{n+1}}{n+1} + c \quad n \neq -1$$           |
| Logarithmic case    | $$\int \dfrac{1}{x} \ dx = \ln \lvert x \rvert + c$$                   |
| Natural exponential | $$\int e^x \ dx = e^x + c$$                                            |
| General exponential | $$\int a^x \ dx = \dfrac{a^x}{\ln a} + c \quad a > 0, \ a \neq 1$$     |
| Sine                | $$\int \sin x \ dx = -\cos x + c$$                                     |
| Cosine              | $$\int \cos x \ dx = \sin x + c$$                                      |
| Squared secant      | $$\int \dfrac{1}{\cos^2 x} \ dx = \tan x + c$$                         |
| Squared cosecant    | $$\int \dfrac{1}{\sin^2 x} \ dx = -\cot x + c$$                        |
| Arctangent          | $$\int \dfrac{1}{1 + x^2} \ dx = \arctan x + c$$                       |
| Arcsine             | $$\int \dfrac{1}{\sqrt{1 - x^2}} \ dx = \arcsin x + c$$                |
| [Hyperbolic sine](../hyperbolic-sine-function/) | $$\int \sinh x \ dx = \cosh x + c$$                                    |
| Hyperbolic cosine   | $$\int \cosh x \ dx = \sinh x + c$$                                    |

[/class]

> The page on [indefinite integrals](../indefinite-integrals/) contains the complete list and a derivation of each entry. The remaining circular and hyperbolic functions are treated in [integral of trigonometric functions](../integral-of-trigonometric-functions/), and the exponential cases in [integral of the exponential function](../integral-of-the-exponential-function/).

## Linearity of the integral

If $F'=f$ and $G'=g,$ integration is linear up to the arbitrary additive constant:

$$\int [\alpha f(x) + \beta g(x)] \ dx = \alpha F(x) + \beta G(x) + c \qquad \alpha, \beta \in \mathbb{R}$$

This formula is the linearity of differentiation read in reverse. It separates a sum into terms that can be matched individually with the table of basic antiderivatives.

For the integrand below, linearity separates three standard terms:

$$\int \left(6x^5 - 4\sqrt[3]{x} + \frac{7}{x}\right) \ dx$$

$$
\begin{align}
\int \left(6x^5 - 4\sqrt[3]{x} + \frac{7}{x}\right) \ dx &= 6\int x^5 \ dx - 4\int x^{1/3} \ dx + 7\int \frac{dx}{x} \\[6pt]
&= 6 \cdot \frac{x^6}{6} - 4 \cdot \frac{x^{4/3}}{4/3} + 7\ln|x| + c \\[6pt]
&= x^6 - 3x^{4/3} + 7\ln|x| + c
\end{align}
$$

The antiderivative is therefore $x^6-3x^{4/3}+7\ln|x|+c.$

- - -

Linearity applies to sums, but it has no counterpart for products or quotients. To see the failure for products, take $f(x)=g(x)=x.$ The integral of their product is:

$$\int x^2 \ dx = \frac{x^3}{3} + c$$

The product of one antiderivative of $f$ and one antiderivative of $g$ is:

$$\frac{x^2}{2} \cdot \frac{x^2}{2} = \frac{x^4}{4}$$

The derivative of the second expression is $x^3,$ not $x^2.$ Thus the integral of a product is not the product of the integrals. The same failure occurs for quotients. A product may require [integration by parts](../integration-by-parts/) or substitution, while a quotient may require algebraic rewriting or [partial fraction decomposition](../partial-fraction-decomposition/).

- - -

Algebraic simplification often turns the integrand into a sum of standard terms. Here, it is enough to expand the square:

$$\int \frac{(x+1)^2}{x} \ dx$$

$$
\begin{align}
\int \frac{(x+1)^2}{x} \ dx &= \int \frac{x^2 + 2x + 1}{x} \ dx \\[6pt]
&= \int \left(x + 2 + \frac{1}{x}\right) \ dx \\[6pt]
&= \frac{x^2}{2} + 2x + \ln|x| + c
\end{align}
$$

The antiderivative is $\frac{x^2}{2}+2x+\ln|x|+c.$

The next integral only requires division term by term:

$$\int \frac{2x^4 - 3}{x^2} \ dx$$

$$
\begin{align}
\int \frac{2x^4 - 3}{x^2} \ dx &= \int \left(2x^2 - 3x^{-2}\right) \ dx \\[6pt]
&= \frac{2x^3}{3} + 3x^{-1} + c \\[6pt]
&= \frac{2x^3}{3} + \frac{3}{x} + c
\end{align}
$$

The antiderivative is $\frac{2x^3}{3}+\frac{3}{x}+c.$

> This rewriting is ordinary algebra and should come before the choice of an integration method whenever it reduces the integrand to standard terms.

## The composite power rule

The power rule extends to a power of a differentiable function multiplied by its derivative:

$$\int [f(x)]^n f'(x) \ dx = \frac{[f(x)]^{n+1}}{n+1} + c \qquad n \neq -1$$

The [chain rule](../chain-rule/) shows that the derivative of the right-hand side is the integrand. The formula applies when a power of $f(x)$ occurs together with $f'(x),$ possibly up to a nonzero constant factor.

With $f(x)=x^2+1,$ the factor $x$ is half of $f'(x):$

$$\int x(x^2+1)^5 \ dx$$

$$
\begin{align}
\int x(x^2+1)^5 \ dx &= \frac{1}{2}\int (x^2+1)^5 \cdot 2x \ dx \\[6pt]
&= \frac{1}{2} \cdot \frac{(x^2+1)^6}{6} + c \\[6pt]
&= \frac{(x^2+1)^6}{12} + c
\end{align}
$$

The factor $1/2$ compensates for the derivative of $x^2+1,$ so the antiderivative is $\frac{(x^2+1)^6}{12}+c.$

- - -

Negative and fractional exponents require no new rule. With $f(x)=x^3+8$ and $n=-1/2,$ we have:

$$\int \frac{x^2}{\sqrt{x^3+8}} \ dx$$

$$
\begin{align}
\int \frac{x^2}{\sqrt{x^3+8}} \ dx &= \frac{1}{3}\int (x^3+8)^{-1/2} \cdot 3x^2 \ dx \\[6pt]
&= \frac{1}{3} \cdot \frac{(x^3+8)^{1/2}}{1/2} + c \\[6pt]
&= \frac{2}{3}\sqrt{x^3+8} + c
\end{align}
$$

The antiderivative is $\frac{2}{3}\sqrt{x^3+8}+c.$

- - -

The inner function may also be trigonometric. Since $(\sin x)'=\cos x,$ we have:

$$\int \sin^3 x \cos x \ dx$$

$$
\begin{align}
\int \sin^3 x \cos x \ dx &= \int (\sin x)^3 (\sin x)' \ dx \\[6pt]
&= \frac{\sin^4 x}{4} + c
\end{align}
$$

The antiderivative is $\frac{\sin^4 x}{4}+c.$

## The logarithmic derivative

For the excluded exponent $n=-1,$ the composite formula is logarithmic. Its numerator is the derivative of its denominator:

$$\int \frac{f'(x)}{f(x)} \ dx = \ln|f(x)| + c$$

This is the chain rule applied to $\ln|f(x)|.$ A constant multiple of $f'(x)$ can be adjusted by linearity.

> To apply this formula directly, the numerator must be $f'(x),$ up to a nonzero constant factor. In general, the integral of $1/f(x)$ is not $\ln|f(x)|.$ A linear denominator has a constant derivative, so $\int \frac{dx}{ax+b}$ has a logarithmic antiderivative. By contrast, $\int \frac{dx}{x^2+1}$ has an arctangent as its antiderivative.

- - -

For a linear denominator, the formula is:

$$\int \frac{dx}{ax+b} = \frac{1}{a}\ln|ax+b| + c \qquad a \neq 0$$

The factor $1/a$ compensates for the derivative $a$ of the denominator. With the denominator $2x+7,$ the coefficient is $1/2:$

$$\int \frac{dx}{2x+7}$$

$$
\begin{align}
\int \frac{dx}{2x+7} &= \frac{1}{2}\int \frac{2 \ dx}{2x+7} \\[6pt]
&= \frac{1}{2}\ln|2x+7| + c
\end{align}
$$

Thus the antiderivative is $\frac{1}{2}\ln|2x+7|+c.$

- - -

Trigonometric quotients often have the logarithmic form because the derivative of the denominator is already present in the numerator. Since $(\cos x)'=-\sin x,$ the [tangent function](../tangent-function/) requires a minus sign:

$$\int \tan x \ dx$$

$$
\begin{align}
\int \tan x \ dx &= \int \frac{\sin x}{\cos x} \ dx \\[6pt]
&= -\int \frac{-\sin x}{\cos x} \ dx \\[6pt]
&= -\ln|\cos x| + c
\end{align}
$$

The logarithmic form gives $\int \tan x \ dx=-\ln|\cos x|+c.$

- - -

For $f(x)=1+\sin x,$ the numerator is exactly $f'(x):$

$$\int \frac{\cos x}{1 + \sin x} \ dx$$

$$
\begin{align}
\int \frac{\cos x}{1 + \sin x} \ dx &= \int \frac{(1 + \sin x)'}{1 + \sin x} \ dx \\[6pt]
&= \ln|1 + \sin x| + c
\end{align}
$$

The antiderivative is $\ln|1+\sin x|+c.$

- - -

An algebraic or trigonometric rewriting may reveal the logarithmic form. Dividing numerator and denominator by $\cos^2 x$ produces the derivative of $\tan x$ in the numerator:

$$\int \frac{dx}{\sin x \cos x}$$

$$
\begin{align}
\int \frac{dx}{\sin x \cos x} &= \int \frac{1/\cos^2 x}{\sin x \cos x / \cos^2 x} \ dx \\[6pt]
&= \int \frac{1/\cos^2 x}{\tan x} \ dx \\[6pt]
&= \int \frac{(\tan x)'}{\tan x} \ dx \\[12pt]
&= \ln|\tan x| + c
\end{align}
$$

Therefore the antiderivative is $\ln|\tan x|+c$ on each interval where the integrand is defined.

## Antiderivatives of composite functions

The composite power rule and the logarithmic derivative both follow from the [chain rule](../chain-rule/). More generally, if $F'=g,$ then:

$$\int g(f(x))f'(x) \ dx=F(f(x))+c$$

Each basic antiderivative has a composite form in which the derivative of the inner function is also present. When this form is visible, no temporary variable is needed.

[class="table-1"]

|             |                                                                                       |
| ----------- | ------------------------------------------------------------------------------------- |
| Power       | $$\int [f(x)]^n f'(x) \ dx = \dfrac{[f(x)]^{n+1}}{n+1} + c \quad n \neq -1$$           |
| Logarithm   | $$\int \dfrac{f'(x)}{f(x)} \ dx = \ln \lvert f(x) \rvert + c$$                         |
| Exponential | $$\int e^{f(x)} f'(x) \ dx = e^{f(x)} + c$$                                            |
| Sine        | $$\int \sin(f(x))f'(x) \ dx = -\cos(f(x)) + c$$                                          |
| Cosine      | $$\int \cos(f(x))f'(x) \ dx = \sin(f(x)) + c$$                                           |
| Arctangent  | $$\int \dfrac{f'(x)}{1 + [f(x)]^2} \ dx = \arctan f(x) + c$$                           |
| Arcsine     | $$\int \dfrac{f'(x)}{\sqrt{1 - [f(x)]^2}} \ dx = \arcsin f(x) + c$$                    |

[/class]

For the inner function $\arctan x,$ the derivative $1/(1+x^2)$ is already present:

$$\int \frac{e^{\arctan x}}{1+x^2} \ dx$$

$$
\begin{align}
\int \frac{e^{\arctan x}}{1+x^2} \ dx &= \int e^{\arctan x}(\arctan x)' \ dx \\[6pt]
&= e^{\arctan x} + c
\end{align}
$$

Since $(\arctan x)'=1/(1+x^2),$ the antiderivative is $e^{\arctan x}+c.$

## Substitution

[Integration by substitution](../integration-by-substitution/) replaces an inner function by a new variable and rewrites the integral in terms of that variable:

$$\int f(g(x)) g'(x) \ dx = \int f(u) \ du \qquad u = g(x), \quad du = g'(x) \ dx$$

The method has four steps. Choose $u=g(x),$ compute $du=g'(x) \ dx,$ rewrite every part of the integral in terms of $u,$ and substitute $g(x)$ back into the antiderivative. The composite power rule and the logarithmic derivative are the special cases in which the new integrand is a power or a reciprocal.

If the inner function is linear and $F$ is an antiderivative of $f,$ then:

$$\int f(ax+b) \ dx = \frac{1}{a}F(ax+b) + c \qquad a \neq 0$$

Every entry in the table therefore has a version with a linear argument, and its coefficient is $1/a.$

> A substitution should make the integrand simpler. If the new expression is longer, or if both variables remain without a simple relation between them, choose a different substitution or method.

- - -

A substitution need not remove every occurrence of $x$ by cancellation. If $u=g(x)$ can be solved for $x,$ the remaining occurrences of $x$ can be expressed in terms of $u.$ With $u=x+4,$ we also have $x=u-4:$

$$\int \frac{x}{\sqrt{x+4}} \ dx$$

$$u = x + 4 \qquad x = u - 4 \qquad dx = du$$

$$
\begin{align}
\int \frac{x}{\sqrt{x+4}} \ dx &= \int \frac{u-4}{\sqrt{u}} \ du \\[6pt]
&= \int \left(u^{1/2} - 4u^{-1/2}\right) \ du \\[6pt]
&= \frac{2}{3}u^{3/2} - 8u^{1/2} + c \\[6pt]
&= \frac{2}{3}(x+4)^{3/2} - 8\sqrt{x+4} + c
\end{align}
$$

Substitution back into the final expression gives $\frac{2}{3}(x+4)^{3/2}-8\sqrt{x+4}+c.$

- - -

The choice $u=e^x$ turns the [exponential function](../exponential-function/) in the integrand below into a [rational function](../rational-functions/):

$$\int \frac{dx}{e^x + 1}$$

$$u = e^x \qquad du = e^x \ dx \qquad dx = \frac{du}{u}$$

$$
\begin{align}
\int \frac{dx}{e^x + 1} &= \int \frac{du}{u(u+1)} \\[6pt]
&= \int \left(\frac{1}{u} - \frac{1}{u+1}\right) \ du \\[6pt]
&= \ln|u| - \ln|u+1| + c \\[6pt]
&= x - \ln(e^x + 1) + c
\end{align}
$$

The resulting antiderivative is $x-\ln(e^x+1)+c.$

> The decomposition of $\frac{1}{u(u+1)}$ into two simpler fractions is [partial fraction decomposition](../partial-fraction-decomposition/), the general method for [integrals of rational functions](../integral-of-rational-functions/). Since $e^x>0$ and $e^x+1>0,$ the last line has no absolute values.

- - -

For an integrand containing $\sqrt{x},$ the choice $u=\sqrt{x}$ removes the radical:

$$\int \frac{dx}{\sqrt{x}(1+x)}$$

$$u = \sqrt{x} \qquad x = u^2 \qquad dx = 2u \ du$$

$$
\begin{align}
\int \frac{dx}{\sqrt{x}(1+x)} &= \int \frac{2u \ du}{u(1+u^2)} \\[6pt]
&= 2\int \frac{du}{1+u^2} \\[6pt]
&= 2\arctan u + c \\[6pt]
&= 2\arctan \sqrt{x} + c
\end{align}
$$

The substitution gives the antiderivative $2\arctan\sqrt{x}+c.$

- - -

For each family in the following table, the indicated substitution turns the integrand into a rational function. Division and [partial fraction decomposition](../partial-fraction-decomposition/) then give an elementary antiderivative. Here $R$ denotes a rational expression in its arguments. The radical indices are positive integers. In the second row, $\alpha\delta-\beta\gamma\neq0,$ and in the exponential row, $a\neq0.$

[class="table-1"]

|                                                       |                                                              |
| ----------------------------------------------------- | ------------------------------------------------------------ |
| $$\int R\left(x, \sqrt[n_1]{x}, \ldots, \sqrt[n_r]{x}\right) \ dx$$ | $$x = t^{\mu}, \quad \mu = \mathrm{lcm}(n_1, \ldots, n_r)$$ |
| $$\int R\left(x, \sqrt[n]{\frac{\alpha x + \beta}{\gamma x + \delta}}\right) \ dx$$ | $$\frac{\alpha x + \beta}{\gamma x + \delta} = t^n$$ |
| $$\int R\left(e^{ax}\right) \ dx$$                  | $$t = e^{ax}$$                                               |
| $$\int R(\cos x)\sin x \ dx$$                         | $$t = \cos x$$                                               |
| $$\int R(\sin x)\cos x \ dx$$                         | $$t = \sin x$$                                               |
| $$\int R\left(\sin^2 x, \cos^2 x, \tan x\right) \ dx$$ | $$t = \tan x$$                                              |
| $$\int R(\sin x, \cos x) \ dx$$                       | $$t = \tan\frac{x}{2}$$                                      |

[/class]

The last two rows have different ranges of application. The [Weierstrass substitution](../the-weierstrass-substitution/) $t=\tan\frac{x}{2}$ rationalises every rational expression in $\sin x$ and $\cos x,$ but it may produce denominators of high degree. When sine and cosine occur only through even powers or through the tangent, $t=\tan x$ gives a rational function of lower degree. The required identities are:

$$\sin^2 x = \frac{t^2}{1+t^2} \qquad \cos^2 x = \frac{1}{1+t^2} \qquad dx = \frac{dt}{1+t^2}$$

They reduce the following integral to a rational one:

$$\int \frac{dx}{1+\sin^2 x}$$

$$
\begin{align}
\int \frac{dx}{1+\sin^2 x} &= \int \frac{1}{1 + \frac{t^2}{1+t^2}} \cdot \frac{dt}{1+t^2} \\[6pt]
&= \int \frac{dt}{1+2t^2} \\[6pt]
&= \frac{1}{\sqrt{2}}\arctan\left(\sqrt{2}t\right) + c \\[6pt]
&= \frac{1}{\sqrt{2}}\arctan\left(\sqrt{2}\tan x\right) + c
\end{align}
$$

On each interval where $\tan x$ is continuous, the antiderivative is:

$$\frac{1}{\sqrt{2}}\arctan(\sqrt{2}\tan x)+c.$$

> The last formula is local because $\tan x$ is undefined at $x=\frac{\pi}{2}+k\pi,$ where $k\in\mathbb{Z}.$ The original integrand is defined at these points, so constants on adjacent intervals must be chosen so that the local antiderivatives join across them. For an integrand containing $\sqrt{ax^2+bx+c},$ Euler substitutions give rational forms, while [trigonometric substitution](../trigonometric-substitution-for-integrals/) is often simpler.

## Integration by parts

[Integration by parts](../integration-by-parts/) is often suitable when a product has no evident composite derivative. Its formula transfers a derivative from one factor to the other:

$$\int f(x)g'(x) \ dx = f(x)g(x) - \int f'(x)g(x) \ dx + c$$

In compact notation, with $u=f(x)$ and $dv=g'(x) \ dx:$

$$\int u \ dv = uv - \int v \ du + c$$

The formula is a rearrangement of the [product rule](../differentiation-rules/). The factor chosen as $u$ should become simpler when differentiated, and the factor chosen as $dv$ should have a known antiderivative. The LIATE order, discussed on the dedicated page, is a heuristic for choosing $u.$ It gives priority to logarithmic, inverse trigonometric, algebraic, trigonometric and exponential factors, in that order.

- - -

An integrand with a single factor is also a product with the constant $1.$ For $\arctan x,$ take $u=\arctan x$ and $dv=dx:$

$$\int \arctan x \ dx$$

$$u = \arctan x \qquad du = \frac{dx}{1+x^2} \qquad dv = dx \qquad v = x$$

$$
\begin{align}
\int \arctan x \ dx &= x\arctan x - \int \frac{x}{1+x^2} \ dx \\[6pt]
&= x\arctan x - \frac{1}{2}\int \frac{2x}{1+x^2} \ dx \\[6pt]
&= x\arctan x - \frac{1}{2}\ln(1+x^2) + c
\end{align}
$$

The antiderivative is $x\arctan x-\frac{1}{2}\ln(1+x^2)+c.$

> The choice $dv=dx$ also applies to $\ln x$ and the other inverse trigonometric functions. The last logarithm has no absolute value because $1+x^2>0$ for every real $x.$

- - -

Some integrals need substitution followed by integration by parts. Here substitution removes the square root from the argument, and integration by parts treats the resulting product:

$$\int \sin\sqrt{x} \ dx$$

$$t = \sqrt{x} \qquad x = t^2 \qquad dx = 2t \ dt$$

$$
\begin{align}
\int \sin\sqrt{x} \ dx &= 2\int t\sin t \ dt \\[6pt]
&= 2\left(-t\cos t + \int \cos t \ dt\right) \\[6pt]
&= 2\left(-t\cos t + \sin t\right) + c \\[12pt]
&= 2\sin\sqrt{x} - 2\sqrt{x}\cos\sqrt{x} + c
\end{align}
$$

After replacing $t$ by $\sqrt{x},$ the antiderivative is $2\sin\sqrt{x}-2\sqrt{x}\cos\sqrt{x}+c.$

> In the second line, $u=t$ and $dv=\sin t \ dt,$ so $du=dt$ and $v=-\cos t.$ The remaining integral is a basic antiderivative.

- - -

For a product of a polynomial with an exponential, sine, or cosine, repeated integration by parts can be recorded in a table. Differentiate the polynomial until it becomes zero, integrate the other factor repeatedly, and combine the products with alternating signs. For $\int x^3e^x \ dx,$ the table is:

| Sign | Derivative of $x^3$ | Antiderivative of $e^x$ |
| ---- | ------------------- | ----------------------- |
| $+$  | $x^3$               | $e^x$                   |
| $-$  | $3x^2$              | $e^x$                   |
| $+$  | $6x$                | $e^x$                   |
| $-$  | $6$                 | $e^x$                   |

The next derivative is $0,$ so the tabular process stops after the row containing $6.$ Combining the four rows gives:

$$\int x^3e^x \ dx=e^x(x^3-3x^2+6x-6)+c$$

The table is a shorthand for four applications of integration by parts. For $J_n=\int x^ne^{ax} \ dx,$ where $n\geq1$ is an integer, the same calculation has the [reduction formula](../reduction-formulas/):

$$J_n=\frac{x^ne^{ax}}{a}-\frac{n}{a}J_{n-1}+c \qquad a\neq0$$

Each application lowers the degree of the polynomial by one, so the process ends at $J_0.$

- - -

Repeated integration by parts returns the original integral when the derivatives repeat. Temporarily omitting the arbitrary constants, set $I$ equal to the integral:

$$I=\int e^x\cos x \ dx$$

Two applications return the original integral:

$$
\begin{align}
I &= e^x\sin x-\int e^x\sin x \ dx \\[6pt]
  &= e^x\sin x+e^x\cos x-I
\end{align}
$$

Collecting the two occurrences of $I$ and restoring the arbitrary constant gives:

$$I=\frac{e^x(\sin x+\cos x)}{2}+c$$

This cyclic calculation works whenever repeated differentiation returns the original factors. After collecting the occurrences of the integral on one side, their total coefficient must be nonzero. If they cancel, the calculation gives an identity rather than an antiderivative.

## Quadratic denominators

After [polynomial division](../polynomial-division/), a rational function with a quadratic denominator has a numerator of degree at most one. Write this numerator as a multiple of the derivative of the denominator plus a constant. The first part gives a logarithmic term. For the constant part, write the denominator as $ax^2+bx+c,$ where $a\neq0.$ Its discriminant $\Delta=b^2-4ac$ determines the antiderivative. Since multiplying the numerator and denominator by $-1$ does not change the fraction, we may assume $a>0.$ Distinct [real roots](../roots-of-a-polynomial/) give logarithms, a repeated root gives a reciprocal power, and a quadratic with no real roots gives an arctangent.

When $\Delta>0,$ the denominator has two distinct linear factors, and [partial fraction decomposition](../partial-fraction-decomposition/) gives two logarithmic terms. For the denominator $x^2-x-6=(x-3)(x+2),$ we have:

$$\int \frac{x+5}{x^2-x-6} \ dx$$

$$\frac{x+5}{(x-3)(x+2)} = \frac{A}{x-3} + \frac{B}{x+2} \qquad A = \frac{8}{5}, \quad B = -\frac{3}{5}$$

$$
\begin{align}
\int \frac{x+5}{x^2-x-6} \ dx &= \frac{8}{5}\int \frac{dx}{x-3} - \frac{3}{5}\int \frac{dx}{x+2} \\[6pt]
&= \frac{8}{5}\ln|x-3| - \frac{3}{5}\ln|x+2| + c
\end{align}
$$

The antiderivative is $\frac{8}{5}\ln|x-3|-\frac{3}{5}\ln|x+2|+c.$

- - -

When $\Delta=0,$ the denominator has the form $a(x-x_0)^2.$ The substitution $u=x-x_0$ separates the fraction into a term $\alpha/u$ and a term $\beta/u^2.$ For the denominator $(x+3)^2,$ set $u=x+3:$

$$\int \frac{2x+5}{x^2+6x+9} \ dx$$

$$u = x+3 \qquad x = u-3 \qquad dx = du$$

$$
\begin{align}
\int \frac{2x+5}{x^2+6x+9} \ dx &= \int \frac{2u-1}{u^2} \ du \\[6pt]
&= 2\int \frac{du}{u} - \int u^{-2} \ du \\[6pt]
&= 2\ln|u| + \frac{1}{u} + c \\[6pt]
&= 2\ln|x+3| + \frac{1}{x+3} + c
\end{align}
$$

The two terms give $2\ln|x+3|+\frac{1}{x+3}+c.$

- - -

When $\Delta<0,$ the denominator has no real linear factors. [Completing the square](../completing-the-square/) gives a positive multiple of a square plus a positive constant, whose reciprocal has an [arctangent](../arctangent-and-arccotangent/) as an antiderivative. For $x^2+4x+13,$ the completed square is $(x+2)^2+9:$

$$\int \frac{dx}{x^2+4x+13}$$

$$
\begin{align}
\int \frac{dx}{x^2+4x+13} &= \int \frac{dx}{(x+2)^2 + 9} \\[6pt]
&= \frac{1}{9}\int \frac{dx}{\left(\frac{x+2}{3}\right)^2 + 1} \\[6pt]
&= \frac{1}{9} \cdot 3\int \frac{du}{u^2+1} \qquad u = \frac{x+2}{3} \\[6pt]
&= \frac{1}{3}\arctan\frac{x+2}{3} + c
\end{align}
$$

The antiderivative is $\frac{1}{3}\arctan\frac{x+2}{3}+c.$

- - -

For a first-degree numerator, decompose it into a multiple of the derivative of the denominator and a constant. For the denominator $x^2+2x+5,$ write $x=\frac{1}{2}(2x+2)-1:$

$$\int \frac{x}{x^2+2x+5} \ dx$$

$$(x^2+2x+5)' = 2x+2 \qquad x = \frac{1}{2}(2x+2) - 1$$

$$
\begin{align}
\int \frac{x}{x^2+2x+5} \ dx &= \frac{1}{2}\int \frac{2x+2}{x^2+2x+5} \ dx - \int \frac{dx}{(x+1)^2+4} \\[6pt]
&= \frac{1}{2}\ln(x^2+2x+5) - \frac{1}{2}\arctan\frac{x+1}{2} + c
\end{align}
$$

The antiderivative is $\frac{1}{2}\ln(x^2+2x+5)-\frac{1}{2}\arctan\frac{x+1}{2}+c.$

> The logarithm has no absolute value because a quadratic with $\Delta<0$ and positive leading coefficient is positive for every real $x.$ The same decomposition applies to any first-degree numerator. Matching the leading term determines the coefficient of the logarithm, and the remaining numerator is constant.

- - -

After completing the square, a quadratic under a square root reduces to one of the following forms:

$$
\begin{align}
\int \frac{dx}{\sqrt{a^2-x^2}} &= \arcsin\frac{x}{a} + c \qquad a>0 \\[6pt]
\int \frac{dx}{\sqrt{x^2+k}} &= \ln\left|x + \sqrt{x^2+k}\right| + c \qquad k\neq 0
\end{align}
$$

The formulas hold on each interval where their integrands are defined.

For $5-4x-x^2=9-(x+2)^2,$ the first formula applies:

$$\int \frac{dx}{\sqrt{5-4x-x^2}}$$

$$
\begin{align}
\int \frac{dx}{\sqrt{5-4x-x^2}} &= \int \frac{dx}{\sqrt{9-(x+2)^2}} \\[6pt]
&= \arcsin\frac{x+2}{3} + c
\end{align}
$$

The antiderivative is $\arcsin\frac{x+2}{3}+c.$

> A first-degree numerator over such a radical has the same decomposition. A multiple of the derivative of the radicand $g(x)$ gives a term $\int [g(x)]^{-1/2}g'(x) \ dx,$ while the remaining numerator is constant. If this decomposition is insufficient, [trigonometric substitution](../trigonometric-substitution-for-integrals/) is a systematic method.

## Algebraic and trigonometric reductions

The remaining examples require an algebraic or trigonometric rewriting before a standard antiderivative appears.

If the numerator of a rational integrand has degree at least that of the denominator, [polynomial division](../polynomial-division/) gives a polynomial and a proper fraction. Here, adding and subtracting $1$ performs the division directly:

$$\int \frac{x^2}{x^2+1} \ dx$$

$$
\begin{align}
\int \frac{x^2}{x^2+1} \ dx &= \int \frac{x^2 + 1 - 1}{x^2+1} \ dx \\[6pt]
&= \int \left(1 - \frac{1}{x^2+1}\right) \ dx \\[6pt]
&= x - \arctan x + c
\end{align}
$$

The decomposition gives the antiderivative $x-\arctan x+c.$

- - -

Multiplying the numerator and denominator by a conjugate produces an expression that the [Pythagorean identity](../pythagorean-identity/) may simplify. For the denominator $1+\sin x,$ use the conjugate $1-\sin x:$

$$\int \frac{dx}{1+\sin x}$$

$$
\begin{align}
\int \frac{dx}{1+\sin x} &= \int \frac{1-\sin x}{(1+\sin x)(1-\sin x)} \ dx \\[6pt]
&= \int \frac{1-\sin x}{1-\sin^2 x} \ dx \\[6pt]
&= \int \frac{1-\sin x}{\cos^2 x} \ dx \\[6pt]
&= \int \frac{dx}{\cos^2 x} - \int \frac{\sin x}{\cos^2 x} \ dx \\[6pt]
&= \tan x - \frac{1}{\cos x} + c \\[6pt]
&= -\frac{\cos x}{1+\sin x} + c
\end{align}
$$

The antiderivative is $-\frac{\cos x}{1+\sin x}+c$ on each interval where the integrand is defined. The intermediate rewriting assumes $\cos x\neq 0,$ but the final expression extends across the points where $\sin x=1.$

> The first integral in the fourth line is $\tan x.$ The second uses the composite power rule with $f(x)=\cos x$ and $n=-2,$ since $\int (\cos x)^{-2}\sin x \ dx=-\int (\cos x)^{-2}(\cos x)' \ dx=(\cos x)^{-1}.$ For $\sec x,$ multiply the numerator and denominator by $\sec x+\tan x$ to obtain $\int \sec x \ dx=\ln|\sec x+\tan x|+c.$

- - -

A conjugate also removes a sum or difference of radicals from a denominator. The product of the following denominator and its conjugate is equal to $1:$

$$\left(\sqrt{x+1}+\sqrt{x}\right)\left(\sqrt{x+1}-\sqrt{x}\right)=1$$

Therefore multiplication by the conjugate removes the denominator:

$$
\begin{align}
\int\frac{dx}{\sqrt{x+1}+\sqrt{x}} &= \int\left(\sqrt{x+1}-\sqrt{x}\right) \ dx \\[6pt]
&= \frac{2}{3}(x+1)^{3/2}-\frac{2}{3}x^{3/2}+c
\end{align}
$$

The formula holds for $x\geq0,$ which is the real domain of the integrand.

- - -

For an odd power of sine or cosine, separate one factor and rewrite the remaining even power with $\sin^2 x+\cos^2 x=1.$ For $\sin^3 x,$ this gives:

$$\int \sin^3 x \ dx$$

$$
\begin{align}
\int \sin^3 x \ dx &= \int (1-\cos^2 x)\sin x \ dx \\[6pt]
&= \int \sin x \ dx - \int \cos^2 x \sin x \ dx \\[6pt]
&= -\cos x + \frac{\cos^3 x}{3} + c
\end{align}
$$

The antiderivative is $-\cos x+\frac{\cos^3 x}{3}+c.$

The [product-to-sum identities](../trigonometric-identities/) convert products of sines and cosines with different angles into sums. Applying $\sin(\alpha)\cos(\beta)=\frac{1}{2}[\sin(\alpha+\beta)+\sin(\alpha-\beta)]$ to $\sin 3x\cos x$ gives:

$$\int \sin 3x \cos x \ dx$$

$$
\begin{align}
\int \sin 3x \cos x \ dx &= \frac{1}{2}\int \left(\sin 4x + \sin 2x\right) \ dx \\[6pt]
&= -\frac{\cos 4x}{8} - \frac{\cos 2x}{4} + c
\end{align}
$$

The two resulting sine integrals give $-\frac{\cos 4x}{8}-\frac{\cos 2x}{4}+c.$

- - -

For even powers of a single sine or cosine, the Pythagorean identity does not lower the exponent. The power-reduction formula $\cos^2 x=\frac{1+\cos 2x}{2}$ gives:

$$
\begin{align}
\int \cos^2 x \ dx &= \frac{1}{2}\int (1 + \cos 2x) \ dx \\[6pt]
&= \frac{x}{2} + \frac{\sin 2x}{4} + c
\end{align}
$$

Thus $\int \cos^2 x \ dx=\frac{x}{2}+\frac{\sin 2x}{4}+c.$

The power-reduction identity above treats the square directly. For an arbitrary integer exponent $n\geq2,$ integration by parts gives the reduction formulas:

$$
\begin{align}
\int\sin^n x \ dx &= -\frac{\sin^{n-1}x\cos x}{n}+\frac{n-1}{n}\int\sin^{n-2}x \ dx+c \\[6pt]
\int\cos^n x \ dx &= \frac{\sin x\cos^{n-1}x}{n}+\frac{n-1}{n}\int\cos^{n-2}x \ dx+c
\end{align}
$$

Each recurrence lowers the exponent by two. It ends with the integral of $1$ when $n$ is even and with the integral of $\sin x$ or $\cos x$ when $n$ is odd.

- - -

For products $\tan^m x\sec^n x,$ where $m$ and $n$ are nonnegative integers, the parity of the exponents determines the substitution. If $n$ is even and positive, reserve one factor $\sec^2 x \ dx,$ rewrite the remaining secant powers through $\sec^2x=1+\tan^2x,$ and set $u=\tan x.$ If $m$ is odd and $n$ is positive, reserve $\sec x\tan x \ dx,$ rewrite the remaining tangent powers through $\tan^2x=\sec^2x-1,$ and set $u=\sec x.$ For example:

$$
\begin{align}
\int\tan^3x\sec x \ dx &= \int\tan^2x(\tan x\sec x) \ dx \\[6pt]
&= \int(u^2-1) \ du \qquad u=\sec x \\[6pt]
&= \frac{\sec^3x}{3}-\sec x+c
\end{align}
$$

The corresponding rules for powers of cotangent and cosecant follow from $\csc^2x=1+\cot^2x,$ $(\cot x)'=-\csc^2x,$ and $(\csc x)'=-\csc x\cot x.$

- - -

Since $(e^xf(x))'=e^x[f(x)+f'(x)],$ the product rule gives:

$$\int e^x[f(x) + f'(x)] \ dx = e^x f(x) + c$$

With $f(x)=\ln x,$ the identity becomes:

$$\int e^x\left(\ln x + \frac{1}{x}\right) \ dx$$

$$
\begin{align}
\int e^x\left(\ln x + \frac{1}{x}\right) \ dx &= \int \left[e^x\ln x + e^x(\ln x)'\right] \ dx \\[6pt]
&= \int \left(e^x\ln x\right)' \ dx \\[6pt]
&= e^x\ln x + c
\end{align}
$$

The antiderivative is $e^x\ln x+c.$

When the integrand is $e^{ax}P(x),$ with $a\neq0$ and $P$ a nonzero polynomial, its antiderivative has the form $e^{ax}Q(x),$ where $Q$ has the same degree as $P.$ The derivative of this expression is:

$$\left(e^{ax}Q(x)\right)'=e^{ax}\left[Q'(x)+aQ(x)\right]$$

The coefficients of $Q$ are therefore determined by the polynomial equation $Q'+aQ=P.$ Consider the integral:

$$\int e^x(x^2+1) \ dx$$

Set $Q(x)=Ax^2+Bx+C.$ Its derivative gives:

$$Q+Q'=Ax^2+(B+2A)x+(C+B)$$

Comparison with $x^2+1$ gives $A=1,$ $B=-2$ and $C=3.$ The antiderivative is:

$$\int e^x(x^2+1) \ dx=e^x(x^2-2x+3)+c$$

This coefficient method gives the same result as repeated integration by parts without writing the intermediate integrals.

The quotient rule gives the analogous identity:

$$\int \frac{f'(x)g(x)-f(x)g'(x)}{[g(x)]^2} \ dx=\frac{f(x)}{g(x)}+c$$

- - -

For an integrand containing an [absolute value](../absolute-value/), its zeros divide the interval into parts on which the sign is fixed. The [piecewise definition](../piecewise-functions/) then allows the absolute value to be removed separately on each part. For example, $|x-1|=1-x$ when $x\leq1$ and $|x-1|=x-1$ when $x\geq1,$ so:

$$
\begin{align}
\int_{-1}^{2}|x-1| \ dx &= \int_{-1}^{1}(1-x) \ dx+\int_{1}^{2}(x-1) \ dx \\[6pt]
&= 2+\frac{1}{2} \\[6pt]
&= \frac{5}{2}
\end{align}
$$

The splitting points are the zeros of the expressions inside the absolute values; with several factors, all such zeros must be ordered before the integral is divided.

- - -

For [definite integrals](../definite-integrals/), symmetry may determine the value without an antiderivative. An [odd function](../even-and-odd-functions/) has integral zero over an interval symmetric about the origin. For example:

$$\int_{-1}^{1} \frac{x^3\cos x}{1+x^2} \ dx = 0$$

The numerator is odd and the denominator is even, so the integrand is odd. For an even integrand, the integral over $[-1,1]$ is twice the integral over $[0,1].$

- - -

For an integrable function $f$ on $[a,b],$ the substitution $x=a+b-t$ reverses the endpoints and gives, after renaming the integration variable:

$$
\begin{align}
\int_a^b f(x) \ dx &= \int_a^b f(a+b-x) \ dx \\[6pt]
&= \frac{1}{2}\int_a^b\left[f(x)+f(a+b-x)\right] \ dx
\end{align}
$$

The average in the second line is useful when the two terms simplify after they are added. For example, define the integral:

$$I=\int_0^1\frac{x}{x^2+(1-x)^2} \ dx$$

Reflection about $x=1/2$ replaces the numerator $x$ by $1-x$ and leaves the denominator unchanged. Adding the two forms gives:

$$
\begin{align}
2I &= \int_0^1\frac{dx}{x^2+(1-x)^2} \\[6pt]
   &= \left[\arctan(2x-1)\right]_0^1 \\[6pt]
   &= \frac{\pi}{2}
\end{align}
$$

Therefore $I=\pi/4.$

- - -

For an [improper integral](../improper-integrals/) on $(0,+\infty),$ the reciprocal substitution $x=1/t$ has $dx=-dt/t^2$ and reverses the endpoints. Restoring their order gives, whenever the integrals converge:

$$\int_0^{+\infty}f(x) \ dx=\int_0^{+\infty}\frac{f(1/x)}{x^2} \ dx$$

The identity is useful when $f(1/x)/x^2$ is equal to $f(x)$ or $-f(x),$ or when the sum of the two expressions is simpler. Consider the absolutely convergent integral:

$$I=\int_0^{+\infty}\frac{\ln x}{1+x^2} \ dx$$

The reciprocal substitution gives:

$$
\begin{align}
I &= \int_0^{+\infty}\frac{\ln(1/x)}{1+1/x^2}\frac{dx}{x^2} \\[6pt]
  &= -\int_0^{+\infty}\frac{\ln x}{1+x^2} \ dx \\[12pt]
  &= -I
\end{align}
$$

The integral is absolutely convergent, so $I=-I$ implies $I=0.$

- - -

Symmetry can also compare a pair of definite integrals. If the integrals are equal and their sum is elementary, each one is half of the sum. The substitution $x=t+\frac{\pi}{2}$ and periodicity give:

$$\int_{0}^{2\pi} \sin^2 x \ dx = \int_{0}^{2\pi} \cos^2 x \ dx$$

Their sum is determined by the Pythagorean identity:

$$\int_{0}^{2\pi} \left(\sin^2 x + \cos^2 x\right) \ dx = \int_{0}^{2\pi} dx = 2\pi$$

The two equal integrals have sum $2\pi,$ so each is equal to $\pi.$ On an interval where the two integrals are not equal, the power-reduction formula gives their values separately.

## Choosing an integration method

For an unfamiliar integrand, work through these checks in order. If the integrand already matches one of the later cases, start with that case.

+ Simplify the integrand. Expand products and squares when this exposes standard terms, divide polynomials, split fractions, apply [trigonometric identities](../trigonometric-identities/), write radicals as powers, and use a conjugate when it removes a radical or simplifies a denominator. For an absolute value, split the interval at every point where its argument changes sign.
+ Check the table. If the integrand is a table entry, possibly with a linear argument $\alpha x+\beta$ and $\alpha\neq0,$ write the answer directly and divide by $\alpha.$
+ Look for an inner function together with its derivative. The composite forms include a power of $f$ times $f',$ a quotient $f'/f,$ and the exponential and trigonometric analogues. Linearity supplies a missing constant factor.
+ Try a substitution. Common choices are the argument of a composition, the expression under a radical and the denominator of a fraction. The resulting integral should be entirely in the new variable and simpler than the original one.
+ For a rational integrand, divide if the numerator has degree at least that of the denominator. With a quadratic denominator, compute $\Delta$ and follow the corresponding case; with a denominator of higher degree, factor it and apply [partial fraction decomposition](../partial-fraction-decomposition/).
+ For powers of sine and cosine, use parity first and a reduction formula when the exponent remains high. For products of tangent and secant, reserve $\sec^2x \ dx$ when the secant exponent is even or $\sec x\tan x \ dx$ when the tangent exponent is odd and a secant factor is present.
+ For a product of factors from different families, apply [integration by parts](../integration-by-parts/) with $u$ chosen by the LIATE heuristic. Use the tabular form when a polynomial is differentiated repeatedly. If the original integral returns, collect its occurrences and solve the resulting linear equation.
+ For a single factor such as $\ln x$ or an inverse trigonometric function, use integration by parts with $dv=dx.$
+ For an integrand $e^{ax}P(x)$ with $a\neq0$ and $P$ a nonzero polynomial, seek an antiderivative $e^{ax}Q(x)$ of the same polynomial degree and determine the coefficients from $Q'+aQ=P.$
+ For radicals of the form $\sqrt{a^2-x^2},$ $\sqrt{a^2+x^2}$ or $\sqrt{x^2-a^2},$ use [trigonometric substitution](../trigonometric-substitution-for-integrals/). For the other families in the table of rationalising substitutions, use the corresponding substitution and integrate the resulting rational function.
+ For a definite integral, test parity, reflection about the midpoint and periodicity before finding an antiderivative. On $(0,+\infty),$ also test the reciprocal substitution $x=1/t.$
+ Differentiate the result. This check detects sign errors, incorrect coefficients and misapplied rules.

## Non-elementary antiderivatives

An elementary function need not have an elementary antiderivative. In such a case, no finite expression formed from algebraic functions, exponentials, logarithms, trigonometric functions, inverse trigonometric functions and their compositions has the required derivative. Three standard examples are:

$$\int e^{-x^2} \ dx \qquad \int \frac{\sin x}{x} \ dx \qquad \int \frac{dx}{\ln x}$$

Each integrand is [continuous](../continuous-functions/) on a suitable interval, so the [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/) defines an antiderivative as an integral function. The obstruction concerns an elementary closed form. Liouville's theorem on integration in finite terms characterises the possible form of such an antiderivative.

> Chebyshev's theorem gives a complete criterion for one family. The binomial differential $\int x^q(a+bx^r)^s \ dx,$ where $q,$ $r$ and $s$ are rational and $a,b,r\neq 0,$ has an elementary antiderivative if and only if at least one of $s,$ $\frac{q+1}{r}$ and $s+\frac{q+1}{r}$ is an integer. When one of these numbers is an integer, a substitution reduces the integral to a rational function. Otherwise, the antiderivative is not elementary.

- - -

Even without an elementary antiderivative, a definite integral may exist and have a computable value. [Numerical integration](../numerical-integration/) gives an approximation, a [power series](../power-series/) may be integrated term by term, and an auxiliary parameter sometimes gives an exact value.

For the sine integral, multiply the integrand by $e^{-bx}$ and define the family:

$$I(b) = \int_{0}^{+\infty} \frac{\sin x}{x}e^{-bx} \ dx \qquad b > 0$$

The [partial derivative](../partial-derivatives/) in $b$ removes the factor $1/x,$ and the remaining integral is elementary:

$$
\begin{align}
I'(b) &= \int_{0}^{+\infty} \frac{\partial}{\partial b}\left(\frac{\sin x}{x}e^{-bx}\right) \ dx \\[6pt]
&= -\int_{0}^{+\infty} e^{-bx}\sin x \ dx \\[6pt]
&= -\frac{1}{b^2+1}
\end{align}
$$

Integration in $b$ gives $I(b)=-\arctan b+k.$ Since $|\sin x|\leq x$ on $(0,+\infty),$ the estimate $|I(b)|\leq\int_{0}^{+\infty}e^{-bx} \ dx=1/b$ holds. Hence $I(b)\to 0$ as $b\to+\infty,$ and $k=\frac{\pi}{2}.$ The limit as $b\to 0^+$ then gives:

$$\int_{0}^{+\infty} \frac{\sin x}{x} \ dx = \lim_{b \to 0^+} \left(\frac{\pi}{2} - \arctan b\right) = \frac{\pi}{2}$$

Both operations require justification. On every half-line $b\geq b_0>0,$ the derivative in $b$ is dominated by the integrable function $e^{-b_0x}.$ For the limit $b\to 0^+,$ dominated convergence applies on every finite interval. On the remaining tail, [Dirichlet's estimate](../convergence-tests-for-improper-integrals/) is uniform for $b\geq 0,$ which gives continuity at $b=0.$ The integral at $b=0$ is only conditionally convergent.

The factor $e^{-bx}$ works because differentiation in $b$ removes $1/x,$ while exponential decay controls the improper integral for $b>0.$ A parameter method requires a family whose derivative is simpler than the original integrand, so it is less systematic than the preceding strategies.
