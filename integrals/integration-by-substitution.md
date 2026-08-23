---
title: Integration by Substitution
source: https://algebrica.org/integration-by-substitution/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - chain-rule
  - change-of-variable
  - composite-functions
  - definite-integral
  - indefinite-integral
  - integration
  - integration-by-substitution
  - trigonometric-substitution
---
## Simplifying integration

In practical problems, we regularly encounter integrals that cannot be evaluated immediately or by inspection. To rewrite them in a more manageable form, we must perform a series of manipulations. At first, finding the right sequence involves some trial and error, but with experience we acquire enough fluency to recognize at a glance a strategy that simplifies the computation even for integrals that initially appear very complicated. As I have pointed out several times in the entries on this topic, integrals, at least those encountered in the early years of university study, can be evaluated by fairly mechanical procedures and do not require any exceptional capacity for abstraction. What they require above all is considerable practice and a thorough knowledge of the standard antiderivatives, their algebraic properties, and the main methods of integration.

The method of integration by substitution, which we shall examine in detail shortly, is fairly simple because it reverses the chain rule. In brief, the method seeks to simplify the original integral by making a suitable change of variable, and it generally applies to integrals of the following form:

$$\int f(g(x))g'(x) \ dx \tag{1}$$

Suppose that $F$ is an antiderivative of $f,$ that is, $F' = f.$ Using the substitution $u = g(x),$ the integral becomes:

$$\int f(g(x))g'(x) \ dx = \int f(u) \ du = F(u) + c = F(g(x)) + c$$

The procedure can be organized into four basic steps:

+ First, set $u = g(x),$ choosing $g(x)$ according to the structure of the original integral.
+ Next, differentiate the chosen function to obtain $du = g'(x) \ dx.$
+ At this point, rewrite all the factors and the differential in terms of $u.$
+ Finally, integrate with respect to $u$ and, for an indefinite integral, substitute $g(x)$ back for $u.$

> For a definite integral, remember to use the original limits of integration reexpressed in terms of $u,$ as explained later in the section devoted to this case.

- - -

As noted above, the substitution method follows from the chain rule for derivatives. Applying the chain rule to the composite function $F(g(x))$ gives:

$$\frac{d}{dx}F(g(x)) = F'(g(x))g'(x) = f(g(x))g'(x)$$

The integrand $f(g(x))g'(x)$ is therefore the derivative of $F(g(x)).$ Setting $u = g(x)$ gives:

$$\int f(u) \ du = F(u) + c$$

Substituting $g(x)$ back for $u$ gives $F(g(x)) + c,$ as in the original formula.

- - -

How can we tell whether a substitution is genuinely useful? To apply this method, we must recognize the pattern in $(1),$ namely, the presence in the integrand of a [composite function](../composite-functions/) together with a factor proportional to the derivative of its inner function.

After identifying a possible inner function $g(x),$ we calculate $g'(x)$ and compare this derivative with the remaining factors in the integrand. The factor $g'(x)$ need not appear exactly as such; it is enough for one of those factors to be a nonzero constant multiple of it. The constant is factored out of the integral, while the substitution $u = g(x)$ transforms $g'(x) \ dx$ into $du.$

For example, consider expressions of the following kinds:

$$(ax + b)^n \quad \quad \sqrt{ax + b}$$
$$\ln(ax + b) \quad \quad e^{ax + b}$$

In all these cases, the inner function is:

$$g(x) = ax + b$$

Its derivative is simply $g'(x) = a.$ Since this derivative is constant, the substitution $u = ax + b$ can also be applied when the factor $a$ does not appear explicitly in the integrand. Indeed, for $a \neq 0,$ the relation $du = a \ dx$ gives $dx = \frac{1}{a} \ du.$

The same criterion applies to a rational expression of the following form, with the inner function in the denominator and its derivative in the numerator:

$$\frac{g'(x)}{g(x)}$$

If the numerator agrees with $g'(x)$ up to a nonzero constant factor, we set $u = g(x).$

- - -

The following table summarizes the recurring patterns discussed so far together with the appropriate substitutions:

[class="table-1"]

|                                  |              |
| -------------------------------- | ------------ |
| $$\int f(g(x))g'(x) \ dx$$       | $$u = g(x)$$ |
| $$\int (ax + b)^n \ dx$$         | $$u = ax + b$$ |
| $$\int e^{ax + b} \ dx$$         | $$u = ax + b$$ |
| $$\int \ln(ax + b) \ dx$$        | $$u = ax + b$$ |
| $$\int \dfrac{g'(x)}{g(x)} \ dx$$ | $$u = g(x)$$ |

[/class]

As the table shows, only a few cases occur, so a little practice makes them immediately recognizable.

## Examples

Below we present several concrete examples to illustrate how the method works in practice. First, consider the following integral:

$$\int (2x + 1)^3 \ dx$$

This integral has the form $(ax+b)^n,$ so it is enough to set $u = 2x + 1$ and replace the cubic expression by $u^3.$ Differentiating the substitution gives $du = 2 \ dx,$ and hence:

$$dx = \frac{du}{2}$$
The transformed integral is therefore:

$$\int \frac{u^3}{2} \ du = \frac{1}{2}\int u^3 \ du$$

As we can see, the integral has been reduced to an elementary form, and the power rule for integration gives:

$$\frac{1}{2}\left(\frac{u^4}{4}\right) + c = \frac{u^4}{8} + c$$

Always remember, however, to return to the original variable by substituting back for $u.$ In this case, we obtain:

$$\int (2x + 1)^3 \ dx = \frac{1}{8}(2x + 1)^4 + c$$

- - -

We now consider an example with a rational integrand:

$$\int \frac{1}{3x - 5} \ dx$$

As discussed above, in this case it is enough to set $u = 3x - 5,$ and differentiation gives $du = 3 \ dx.$ We can therefore write:

$$dx = \frac{du}{3}$$

The transformed integral becomes:

$$\int \frac{1}{3u} \ du = \frac{1}{3}\int \frac{du}{u}$$

This is the standard logarithmic integral and gives:

$$\frac{1}{3}\ln|u| + c$$

Substituting $3x - 5$ back for $u$ gives:

$$\int \frac{1}{3x - 5} \ dx = \frac{1}{3}\ln|3x - 5| + c$$

- - -

We now compute the following integral:

$$\int x \sin(x^2) \ dx$$

The inner expression $x^2$ has derivative $2x.$ We set $u = x^2$ and obtain $du = 2x \ dx,$ hence:

$$\qquad x \ dx = \frac{1}{2} \ du$$

The substitution gives:

$$\int x\sin(x^2) \ dx = \frac{1}{2}\int \sin u \ du$$

The antiderivative in the new variable is:

$$\frac{1}{2}\int \sin u \ du = -\frac{1}{2}\cos u + c$$

Replacing $u$ with $x^2$ gives:

$$\int x\sin(x^2) \ dx = -\frac{1}{2}\cos(x^2) + c$$

- - -

Finally, consider the following integral:

$$\int \cos x \sqrt{\sin x} \ dx$$

In this case, we set $u = \sin x$ so that the radical becomes $\sqrt{u}.$ The differential of the new variable is therefore $du = \cos x \ dx,$ and the integral becomes:

$$\int \sqrt{u} \ du = \int u^{1/2} \ du$$

This is also an elementary integral that, again by the power rule, gives:

$$\int u^{1/2} \ du = \frac{u^{3/2}}{3/2} = \frac{2}{3} u^{3/2} + c$$

Replacing $u$ with $\sin x$ gives:

$$\int \cos x\sqrt{\sin x} \ dx = \frac{2}{3}(\sin x)^{3/2} + c$$

## Trigonometric substitutions

Besides the substitutions considered above, it is sometimes necessary to use trigonometric substitutions. They are especially useful when an integral contains radicals involving quadratic expressions of the forms $a^2 - x^2,$ $a^2 + x^2$ and $x^2 - a^2.$

Trigonometric substitution makes these expressions manageable by rewriting the radicands by means of the [Pythagorean identity](../pythagorean-identity/):

$$\sin^2 x + \cos^2 x = 1$$

This identity can be rewritten in the following equivalent forms:

$$
\begin{align}
\cos^2 x &= 1 - \sin^2 x \\[6pt]
\sec^2 x &= 1 + \tan^2 x \\[6pt]
\tan^2 x &= \sec^2 x - 1
\end{align}
$$

When $a > 0,$ the substitution depends on the expression under the radical. Each substitution must be applied on an interval where the chosen trigonometric function is invertible and each resulting factor has a fixed sign. In the case of $\sqrt{x^2 - a^2},$ the branches $x \geq a$ and $x \leq -a$ must be treated separately. The choice of intervals and the treatment of absolute values are explained in the entry devoted to [trigonometric substitutions for integrals](../trigonometric-substitution-for-integrals/). The standard substitutions are summarized below:

[class="table-1"]

|                         |                  |
| ----------------------- | ---------------- |
| $$\sqrt{a^2 - x^2}$$   | $$x = a\sin u$$ |
| $$\sqrt{a^2 + x^2}$$   | $$x = a\tan u$$ |
| $$\sqrt{x^2 - a^2}$$   | $$x = a\sec u$$ |

[/class]

- - -

As an example, we compute the following indefinite integral:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx$$

For $|x| < 3,$ we choose $u \in (-\pi/2, \pi/2)$ and set $x = 3\sin u.$ The differential becomes:

$$dx = 3\cos u \ du$$

After the substitution, the denominator becomes:

$$\sqrt{9 - x^2} = \sqrt{9 - 9\sin^2 u} = \sqrt{9(1 - \sin^2 u)}$$

On the chosen interval, $\cos u > 0.$ The identity $\sin^2 u + \cos^2 u = 1$ gives:

$$\sqrt{9(1 - \sin^2 u)} = \sqrt{9\cos^2 u} = 3\lvert\cos u\rvert = 3\cos u$$

The integral therefore becomes:

$$\int \frac{3\cos u \ du}{3\cos u} = \int \ du = u + c$$

Since $u$ lies in the principal range of the [arcsine function](../arcsine-function/), the equation $x = 3\sin u$ implies:

$$u = \arcsin\left(\frac{x}{3}\right)$$

The antiderivative expressed in the original variable is therefore:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx = \arcsin\left(\frac{x}{3}\right) + c$$

## Substitution rule for definite integrals

So far, we have considered only indefinite integrals. When evaluating definite integrals, we must also transform the bounds according to the substitution we use. Alternatively, we can find an antiderivative with respect to $u,$ replace $u$ with $g(x)$ and use the original bounds in $x.$ Suppose that $g$ is continuously differentiable on $[a,b]$ and that $f$ is continuous on an interval containing $g([a,b]).$ Under these hypotheses, the substitution rule is analogous to $(1),$ with the bounds of integration made explicit:

$$\int_a^b f(g(x))g'(x) \ dx = \int_{g(a)}^{g(b)} f(u) \ du$$

As a concrete example, we compute the following definite integral:

$$\int_{2}^{3} x\cos(x^2) \ dx$$

We set $u = x^2.$ The relation between the differentials is:

$$du = 2x \ dx \qquad x \ dx = \frac{1}{2} \ du$$

We transform the bounds using the same substitution:

$$x = 2 \Longrightarrow u = 4 \qquad x = 3 \Longrightarrow u = 9$$

The integral in the new variable is therefore:

$$\int_2^3 x\cos(x^2) \ dx = \frac{1}{2}\int_4^9 \cos u \ du$$

By the [fundamental theorem of calculus](../fundamental-theorem-of-calculus/) we obtain:

$$\frac{1}{2}\Bigl[\sin u\Bigr]_{4}^{9} = \frac{1}{2}(\sin 9 - \sin 4)$$

Thus, the value of the integral is $\frac{1}{2}(\sin 9 - \sin 4).$

- - -

When the integrand is a rational function of $\sin x$ and $\cos x$ that cannot be simplified using trigonometric identities or direct substitutions, we can use the [Weierstrass substitution](../the-weierstrass-substitution/).

## Further worked examples

The table lists the integrals in increasing order of difficulty. A sentence before each solution identifies the feature of the integrand that suggests the substitution. In the later examples, the solution also transforms the limits of integration, rewrites an algebraic factor, or uses a trigonometric substitution.

[class="table-1"]

|                                                        |
| :----------------------------------------------------- |
| $$1 \quad \int \dfrac{dt}{(1 - 6t)^4}$$                |
| $$2. \quad \int x^3(2 + x^4)^5 \ dx$$                  |
| $$3. \quad \int \cos^3\theta\sin\theta \ d\theta$$     |
| $$4. \int \dfrac{2^{\ln x}}{x} \ dx$$                  |
| $$5. \quad \int_0^{\ln 4} \dfrac{e^t}{1 + 2e^t} \ dt$$ |
| $$6. \quad \int_{\pi/4}^{\pi/3} \csc^2(5x) \ dx$$      |
| $$7. \quad \int \dfrac{9x^3}{\sqrt{1 + x^2}} \ dx$$    |
| $$8. \quad \int_0^1 \sqrt{4 - x^2} \ dx$$              |
[/class]

We begin with the first integral. The denominator is a power of the linear expression $1 - 6t,$ whose derivative is constant. Set $u = 1 - 6t,$ so that $du = -6 \ dt.$ We can therefore rewrite the integral as:

$$
\begin{align}
\int \frac{dt}{(1 - 6t)^4} &= -\frac{1}{6} \int u^{-4} \ du \\[6pt]
&= \frac{1}{18}u^{-3} + c \\[6pt]
&= \frac{1}{18(1 - 6t)^3} + c
\end{align}
$$

- - -

In the second integral, the factor $x^3$ is proportional to the derivative of the inner expression $2 + x^4.$ Substitute $u = 2 + x^4$ and obtain $du = 4x^3 \ dx.$ The integral can therefore be rewritten as:

$$
\begin{align}
\int x^3(2 + x^4)^5 \ dx &= \frac{1}{4} \int u^5 \ du \\[6pt]
&= \frac{u^6}{24} + c \\[6pt]
&= \frac{(2 + x^4)^6}{24} + c
\end{align}
$$

- - -

For the third integral, observe that the factor $\sin\theta$ is the negative of the derivative of $\cos\theta.$ Substitute $u = \cos\theta,$ so that $du = -\sin\theta \ d\theta.$ The transformed integral becomes:

$$
\begin{align}
\int \cos^3\theta\sin\theta \ d\theta &= -\int u^3 \ du \\[6pt]
&= -\frac{u^4}{4} + c \\[6pt]
&= -\frac{\cos^4\theta}{4} + c
\end{align}
$$

- - -

In the fourth integral, the exponent $\ln x$ has derivative $1/x,$ which is the other factor in the integrand. We therefore substitute $u = \ln x,$ so that $du = 1/x \ dx.$ The integral can be rewritten as:

$$
\begin{align}
\int \frac{2^{\ln x}}{x} \ dx &= \int 2^u \ du \\[6pt]
&= \frac{2^u}{\ln 2} + c \\[6pt]
&= \frac{2^{\ln x}}{\ln 2} + c
\end{align}
$$

- - -

We now consider the fifth integral. The denominator $1 + 2e^t$ has derivative $2e^t,$ which is twice the numerator. Since this is a definite integral, we must also transform the limits of integration along with the variable. We use the following substitution:

$$u = 1 + 2e^t \qquad du = 2e^t \ dt$$

$$t = 0 \Longrightarrow u = 3 \qquad t = \ln 4 \Longrightarrow u = 9$$

The integral can therefore be rewritten as:

$$
\begin{align}
\int_0^{\ln 4} \frac{e^t}{1 + 2e^t} \ dt &= \frac{1}{2} \int_3^9 \frac{1}{u} \ du \\[6pt]
&= \frac{1}{2}\Bigl[\ln u\Bigr]_3^9 \\[6pt]
&= \frac{1}{2}\ln 3
\end{align}
$$

- - -

For the sixth integral, observe that the argument $5x$ of the cosecant has a constant derivative. We therefore make the following substitutions:

$$u = 5x \qquad du = 5 \ dx$$

$$x = \frac{\pi}{4} \Longrightarrow u = \frac{5\pi}{4} \qquad x = \frac{\pi}{3} \Longrightarrow u = \frac{5\pi}{3}$$

We can now rewrite the integral and evaluate it using the transformed limits:

$$
\begin{align}
\int_{\pi/4}^{\pi/3} \csc^2(5x) \ dx &= \frac{1}{5} \int_{5\pi/4}^{5\pi/3} \csc^2u \ du \\[6pt]
&= -\frac{1}{5}\Bigl[\cot u\Bigr]_{5\pi/4}^{5\pi/3} \\[6pt]
&= \frac{1}{5}\left[\cot\left(\frac{5\pi}{4}\right) - \cot\left(\frac{5\pi}{3}\right)\right] \\[6pt]
&= \frac{1}{5}\left(1 + \frac{\sqrt{3}}{3}\right)
\end{align}
$$

- - -

In example $7,$ the expression $1 + x^2$ under the radical has derivative $2x.$ After the substitution $u = 1 + x^2,$ the remaining factor is $x^2 = u - 1.$

$$u = 1 + x^2 \qquad du = 2x \ dx \qquad x^2 = u - 1$$

The integral therefore becomes:

$$
\begin{align}
\int \frac{9x^3}{\sqrt{1 + x^2}} \ dx &= \frac{9}{2} \int \frac{u - 1}{\sqrt{u}} \ du \\[6pt]
&= \frac{9}{2} \int \left(u^{1/2} - u^{-1/2}\right) \ du \\[6pt]
&= 3u^{3/2} - 9u^{1/2} + c \\[6pt]
&= 3(x^2 - 2)\sqrt{1 + x^2} + c
\end{align}
$$

- - -

Finally, in the last case, the radical has the form $\sqrt{a^2 - x^2},$ so we set $x = 2\sin\theta$ and transform the limits of integration as well. The substitution gives:

$$x = 2\sin\theta \qquad dx = 2\cos\theta \ d\theta$$

$$x = 0 \Longrightarrow \theta = 0 \qquad x = 1 \Longrightarrow \theta = \frac{\pi}{6}$$

$$\sqrt{4 - x^2} = \sqrt{4 - 4\sin^2\theta} = \sqrt{4\cos^2\theta} = 2\cos\theta$$

The integral therefore becomes:

$$
\begin{align}
\int_0^1 \sqrt{4 - x^2} \ dx &= 4 \int_0^{\pi/6} \cos^2\theta \ d\theta \\[6pt]
&= 2 \int_0^{\pi/6} \left(1 + \cos(2\theta)\right) \ d\theta \\[6pt]
&= \Bigl[2\theta + \sin(2\theta)\Bigr]_0^{\pi/6} \\[6pt]
&= \frac{\pi}{3} + \frac{\sqrt{3}}{2}
\end{align}
$$
