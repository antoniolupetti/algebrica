---
title: Asymptotic Expansion
source: https://algebrica.org/asymptotic-expansion/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - indeterminate-forms
  - landau-symbols
  - order-of-an-infinitesimal
  - principal-part
  - taylor-polynomial
---
## Order of an infinitesimal

A function $f$ is infinitesimal at $x_0$ when its [limit](../limits/) is zero, that is, when $f(x) \to 0$ as $x \to x_0.$ In an [indeterminate form](../indeterminate-forms/) of type $0/0$ the numerator and denominator both tend to zero, and the limit depends on their relative rates of convergence. We compare these rates with a family of reference functions. Near a finite point, the reference functions used in elementary analysis are the [powers](../powers/) $(x-x_0)^{\alpha}$ with $\alpha > 0.$

Let $f$ be infinitesimal at $x_0.$ We say that $f$ has order $\alpha > 0$ at $x_0$ if the quotient of $f$ by the corresponding power has a finite limit different from zero:

$$\lim_{x \to x_0} \frac{f(x)}{(x-x_0)^{\alpha}} = c \neq 0$$

The product $c(x-x_0)^{\alpha}$ is the principal part of $f$ at $x_0.$

> For an arbitrary real exponent, the expression $(x-x_0)^{\alpha}$ need not be real when $x<x_0.$ We may take a right-hand limit, where the power is defined. For a two-sided comparison, we may use the [absolute value](../absolute-value/) $|x-x_0|^{\alpha},$ in which case the principal part is $c|x-x_0|^{\alpha}.$

- - -

The order, when it exists, is unique, and it determines the constant $c.$ Suppose $f$ had two orders $\alpha < \beta$ with constants $c$ and $d.$ We would then have:

$$\frac{f(x)}{(x-x_0)^{\beta}} = \frac{f(x)}{(x-x_0)^{\alpha}} \cdot \frac{1}{(x-x_0)^{\beta - \alpha}}$$

The first factor tends to $c \neq 0,$ while the second is unbounded. The left side cannot tend to the finite number $d.$ Hence at most one exponent satisfies the definition, and the corresponding quotient has the unique limit $c.$

Three infinitesimals at the origin illustrate the definition. From the [remarkable limits](../remarkable-limits/), the function $1-\cos x$ has order $2$ and principal part $x^2/2.$ The difference $\sin x-x$ has order $3$ and principal part $-x^3/6,$ because the first nonzero term after subtracting $x$ from the [expansion of the sine](../taylor-formula-with-remainder/) is cubic. As $x \to 0^+,$ the function $\sqrt{x}\sin x$ has order $3/2,$ since its quotient by $x^{3/2}$ is $\sin(x)/x$ and tends to $1.$ Its principal part is $x^{3/2}.$

- - -

Not every infinitesimal has an order in this scale. Define $f(0)=0$ and $f(x)=e^{-1/x^2}$ for $x \neq 0.$ For every $\alpha > 0,$ the quotient $f(x)/|x|^{\alpha}$ tends to zero because the exponential decreases faster than every power. Thus $f(x)=o(|x|^{\alpha})$ for every $\alpha > 0,$ and no exponent gives a finite nonzero limit.

The function $x\ln x$ as $x \to 0^+$ has no order for the opposite reason. Its quotient by $x^{\alpha}$ is $x^{1-\alpha}\ln x,$ which tends to $0$ when $\alpha < 1$ and is unbounded when $\alpha \geq 1.$ Equivalently, $|x\ln x|=o(x^{\alpha})$ for every $\alpha<1,$ while $x=o(|x\ln x|).$ No power is asymptotically equivalent to $x\ln x$ up to a nonzero constant.

> The powers form an incomplete scale. A wider scale also has logarithmic and exponential factors, although elementary limits seldom require them.

## Principal parts and the substitution principle

The principal part of $f$ is the monomial in the reference scale that is asymptotically equivalent to $f.$ If $g$ is nonzero in a punctured neighbourhood of $x_0,$ we write $f(x) \sim g(x)$ when $f(x)/g(x) \to 1.$ Thus a function of order $\alpha$ with constant $c$ satisfies:

$$f(x) \sim c(x-x_0)^{\alpha} \qquad x \to x_0$$

Asymptotic equivalence permits the replacement of an infinitesimal by its principal part in products and quotients. Suppose $f \sim f_1$ and $g \sim g_1$ as $x \to x_0,$ and suppose the quotient $f_1/g_1$ has a limit. We have:

$$\frac{f(x)}{g(x)} = \frac{f(x)}{f_1(x)} \cdot \frac{f_1(x)}{g_1(x)} \cdot \frac{g_1(x)}{g(x)}$$

The outer factors tend to $1$ by hypothesis, so the whole quotient has the same limit as the middle factor by the [algebra of limits](../algebra-of-limits/). In this quotient, both functions may be replaced by their principal parts. For two infinitesimals of orders $\alpha$ and $\beta$ with constants $c$ and $d,$ we obtain:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{c}{d}(x-x_0)^{\alpha - \beta}$$

If $\alpha=\beta,$ the limit is $c/d.$ If $\alpha>\beta,$ the quotient tends to $0.$ If $\alpha<\beta,$ its absolute value tends to $+\infty;$ its sign and the existence of a one-sided or two-sided infinite limit depend on the constants, the exponent, and the direction of approach. Products have the corresponding property because the product of two asymptotic equivalences is an asymptotic equivalence.

## Where substitution fails

Asymptotic equivalence alone does not justify substitution in a sum. If $f \sim f_1$ and $g \sim g_1,$ the sum $f_1+g_1$ need not be equivalent to $f+g.$ Failure occurs when the principal parts cancel. Consider:

$$\lim_{x \to 0} \frac{\tan x - \sin x}{x^3}$$

Both the [tangent function](../tangent-function/) and the [sine function](../sine-function/) are equivalent to $x$ at the origin. Replacing each function by $x$ turns the numerator into zero and suggests the value $0.$ The computation requires one term beyond the principal part of each function:

$$
\begin{align}
\tan x &= x + \frac{x^3}{3} + o(x^3) \\[6pt]
\sin x &= x - \frac{x^3}{6} + o(x^3)
\end{align}
$$

Subtracting, the linear terms cancel and the cubic terms survive:

$$\tan x - \sin x = \left(\frac{1}{3} + \frac{1}{6}\right)x^3 + o(x^3) = \frac{x^3}{2} + o(x^3)$$

The limit is $1/2.$ Replacing the two functions by their principal parts discards the cubic terms that remain after cancellation.

- - -

Composition can also destroy equivalence. As $x \to +\infty$ we have $x+1 \sim x,$ while their exponentials satisfy:

$$\frac{e^{x+1}}{e^{x}} = e \neq 1$$

Products and quotients preserve asymptotic equivalence whenever they are defined. Sums, differences, and [compositions](../composite-functions/) require separate hypotheses because cancellation or amplification can destroy the relation.

## Finite-order expansions

The remedy for cancellation is to retain more than one term. Let $f$ be defined near $x_0$ and let $n$ be a non-negative integer. An expansion of $f$ of order $n$ at $x_0$ is a representation:

$$f(x) = c_0 + c_1(x-x_0) + \cdots + c_n(x-x_0)^n + o\big((x-x_0)^n\big) \qquad x \to x_0$$

The [polynomial](../polynomials/) contains the terms through the scale $(x-x_0)^n,$ and the [little-o](../little-o-notation/) remainder is smaller than that scale. When $f$ has derivatives through order $n$ in a neighbourhood of $x_0,$ the polynomial is the Taylor polynomial and $c_k=f^{(k)}(x_0)/k!,$ as established in [Taylor's formula with the Peano remainder](../taylor-formula-with-remainder/).

The coefficients of an expansion of order $n$ are unique, so two expansions of the same function may be equated term by term. They may be found from known expansions by substitution or by the algebraic rules below, provided that the required orders are available and every denominator has a nonzero constant term.

When $f$ is infinitesimal at $x_0,$ its first nonzero coefficient determines both the order and the principal part. If $c_0=\cdots=c_{k-1}=0$ and $c_k \neq 0,$ then $f$ has order $k$ and principal part $c_k(x-x_0)^k.$ The later terms are corrections at smaller scales.

## Operations on expansions

Let $P$ and $Q$ be polynomials of degree at most $n$ in $x-x_0,$ and suppose that as $x \to x_0:$

$$f(x) = P(x) + o\big((x-x_0)^n\big) \qquad g(x) = Q(x) + o\big((x-x_0)^n\big)$$

Sums and scalar multiples follow from the algebra of little-o terms. The sum of two remainders $o((x-x_0)^n)$ is again $o((x-x_0)^n),$ so $f+g$ has polynomial part $P+Q$ and a remainder of that form.

For the product, write $[R]_n$ for the polynomial obtained from $R$ by discarding the monomials of degree above $n.$ Then:

$$f(x)g(x) = [PQ]_n(x) + o\big((x-x_0)^n\big)$$

The monomials of $PQ$ with degree above $n$ are $o((x-x_0)^n).$ In each mixed product, the polynomial factor is bounded near $x_0,$ so the product is still $o((x-x_0)^n).$ The product of the two remainders has the same property. Thus we multiply the two polynomials and retain only the terms through degree $n.$

Division reduces to multiplication after normalising the denominator. If $g(x_0) \neq 0,$ write $g(x)=g(x_0)(1+u(x)),$ where $u(x) \to 0,$ and use the expansion of the reciprocal obtained from the [geometric series](../geometric-series/):

$$\frac{1}{1+u} = 1 - u + u^2 - \cdots + (-1)^n u^n + o(u^n) \qquad u \to 0$$

For composition, suppose that $g$ is infinitesimal at $x_0$ of positive integer order $p$ and that $f$ has at the origin the expansion $a_0+a_1u+\cdots+a_nu^n+o(u^n).$ Substitution gives:

$$f(g(x))=a_0+a_1g(x)+\cdots+a_ng(x)^n+o\big((x-x_0)^{np}\big)$$

The order of $g$ determines the remainder after substitution. To obtain a polynomial in $x-x_0$ through degree $np,$ we also need an expansion of $g$ through the required degree.

## Division and composition in practice

The reciprocal of the cosine near the origin illustrates the rule for division. Starting from $\cos x = 1 - x^2/2 + x^4/24 + o(x^4),$ define:

$$u = \frac{x^2}{2} - \frac{x^4}{24} + o(x^4)$$

We then have $\cos x=1-u,$ and $u$ has order $2.$ Only $u$ and $u^2$ have terms through degree four, because $u^3$ has order six:

$$u^2 = \frac{x^4}{4} + o(x^4)$$

Substitution into the geometric expansion gives:

$$\frac{1}{\cos x} = 1 + \frac{x^2}{2} - \frac{x^4}{24} + \frac{x^4}{4} + o(x^4) = 1 + \frac{x^2}{2} + \frac{5x^4}{24} + o(x^4)$$

- - -

Consider the expansion of $\ln(1+\sin x)$ through order three. The inner function has order one, so we need the expansion of $\ln(1+u)$ through order three:

$$\ln(1+u) = u - \frac{u^2}{2} + \frac{u^3}{3} + o(u^3)$$

With $u=\sin x=x-x^3/6+o(x^3),$ the required powers are $u^2=x^2+o(x^3)$ and $u^3=x^3+o(x^3).$ Substitution gives:

$$\ln(1+\sin x) = x - \frac{x^3}{6} - \frac{x^2}{2} + \frac{x^3}{3} + o(x^3) = x - \frac{x^2}{2} + \frac{x^3}{6} + o(x^3)$$

The coefficients are the same if the composite function is differentiated three times at the origin.

## Choosing the order of the expansion

Consider a quotient whose denominator has positive integer order $p$ and a nonzero principal coefficient. It is sufficient to expand every term in the numerator with remainder $o((x-x_0)^p).$ If the lowest surviving degree in the numerator is $q<p,$ the quotient is unbounded in absolute value. If it is $q=p,$ the quotient has a finite limit determined by the two principal coefficients. If every coefficient through degree $p$ cancels, the numerator is $o((x-x_0)^p)$ and the limit is zero.

An expansion below order $p$ may leave the limit undetermined. In the earlier example, stopping the tangent and the sine at the linear term gives:

$$\frac{\tan x - \sin x}{x^3} = \frac{\big(x + o(x)\big) - \big(x + o(x)\big)}{x^3} = \frac{o(x)}{x^3}$$

The numerator is known only to be smaller than $x,$ and such a quantity divided by $x^3$ can tend to any finite value, be unbounded, or have no limit. The relation is correct but does not determine the limit. This occurs when the polynomial part of the numerator vanishes and the remainder is not $o(x^3).$ We must expand through the order of the denominator and repeat the calculation.

> For a quotient with denominator of order $p,$ an expansion of the numerator through order $p$ is sufficient. Terms of higher degree cannot affect the limit, while an expansion of lower order may be insufficient.

## Example 1

We evaluate a limit in which the coefficients of degrees zero, one, and two in the numerator cancel:

$$\lim_{x \to 0} \frac{\sqrt{1+2x}-e^{x}+x^2}{x^3}$$

The denominator has order three, so both functions in the numerator require expansions through order three. In the binomial expansion of $(1+u)^{1/2},$ the coefficients through degree three are $1/2,$ $-1/8,$ and $1/16.$ Substituting $u=2x$ gives:

$$\sqrt{1+2x} = 1 + x - \frac{x^2}{2} + \frac{x^3}{2} + o(x^3)$$

The exponential has the expansion:

$$e^{x} = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + o(x^3)$$

Subtracting, the constant and the linear terms cancel, and the quadratic terms combine into $-x^2:$

$$\sqrt{1+2x}-e^{x} = -x^2 + \left(\frac{1}{2} - \frac{1}{6}\right)x^3 + o(x^3) = -x^2 + \frac{x^3}{3} + o(x^3)$$

The term $x^2$ added in the numerator removes the quadratic contribution, and the cubic term is the first to survive:

$$\lim_{x \to 0} \frac{\dfrac{x^3}{3} + o(x^3)}{x^3} = \frac{1}{3}$$

After three applications of [de l'Hôpital's rule](../hopital-rule/), the value is again $1/3.$

## Example 2

For an exponential form, the [logarithm](../logarithmic-function/) converts the exponent into a factor. Consider:

$$\lim_{x \to 0} \left(\frac{\sin x}{x}\right)^{1/x^2}$$

The base is positive near the origin and tends to $1,$ while the exponent tends to $+\infty.$ We first compute the limit of the logarithm:

$$A:=\lim_{x \to 0}\frac{1}{x^2}\ln\frac{\sin x}{x}$$

After division of the sine expansion by $x,$ the base has the form $1+u,$ where $u$ has order two:

$$\frac{\sin x}{x} = 1 - \frac{x^2}{6} + o(x^2)$$

Since $u$ has order two and the logarithm is divided by $x^2,$ the relation $\ln(1+u)=u+o(u)$ is sufficient, with $o(u)=o(x^2):$

$$\ln \frac{\sin x}{x} = -\frac{x^2}{6} + o(x^2)$$

Thus $A=-1/6.$ Since the [exponential function](../exponential-function/) is [continuous](../continuous-functions/), the original limit is:

$$\lim_{x \to 0}\left(\frac{\sin x}{x}\right)^{1/x^2}=e^{-1/6}$$

## Expansions at infinity and for sequences

At infinity, the powers of $x-x_0$ no longer form a scale centred at a finite point. The powers $x^{-\alpha}$ are a reference scale for infinitesimals. The substitution $t=1/x$ converts behaviour at infinity into behaviour at the origin. A limit as $x \to +\infty$ becomes a limit as $t \to 0^+,$ and expansions at the origin apply to $t.$

The same substitution applies to [sequences](../sequences/). An expansion in $1/n$ follows from an expansion at the origin by substituting $1/n,$ or another [sequence that tends to zero](../convergent-and-divergent-sequences/), for the variable. Each substitution requires the inner sequence to tend to the centre of the known expansion.

## Example 3

The following limit combines a divergent factor with a logarithm:

$$\lim_{x \to +\infty}\left(x-x^2\ln\left(1+\frac{1}{x}\right)\right)$$

Both terms diverge, so the form is $\infty - \infty.$ Setting $t = 1/x,$ the limit becomes:

$$\lim_{t \to 0^+}\left(\frac{1}{t}-\frac{\ln(1+t)}{t^2}\right)$$

The second term has a factor $t^{-2},$ so the logarithm requires an expansion through order two:

$$\ln(1+t) = t - \frac{t^2}{2} + o(t^2)$$

Dividing by $t^2$ produces a divergent term that matches the first one:

$$\frac{\ln(1+t)}{t^2} = \frac{1}{t} - \frac{1}{2} + o(1)$$

The two divergent contributions cancel and the constant remains:

$$\lim_{t \to 0^+}\left(\frac{1}{t}-\frac{1}{t}+\frac{1}{2}+o(1)\right) = \frac{1}{2}$$

## Example 4

For a sequence, consider:

$$\lim_{n \to \infty}n^{3/2}\left(\sqrt{n+1}+\sqrt{n-1}-2\sqrt{n}\right)$$

Factoring $\sqrt{n}$ from each square root introduces the infinitesimal $1/n:$

$$\sqrt{n \pm 1} = \sqrt{n}\left(1 \pm \frac{1}{n}\right)^{1/2}$$

After this factorisation, the product of the two external factors is $n^2.$ Hence the sum of the binomial terms minus $2$ must be known through order two in $1/n.$ The binomial expansion with exponent $1/2$ is:

$$\left(1 \pm \frac{1}{n}\right)^{1/2} = 1 \pm \frac{1}{2n} - \frac{1}{8n^2} + o\left(\frac{1}{n^2}\right)$$

Adding the two expansions cancels the terms of first order and doubles the constants, and subtracting $2\sqrt{n}$ removes the constants as well:

$$\sqrt{n+1}+\sqrt{n-1}-2\sqrt{n} = \sqrt{n}\left(-\frac{1}{4n^2}+o\left(\frac{1}{n^2}\right)\right)$$

Multiplying by $n^{3/2}$ leaves a finite value:

$$\lim_{n \to \infty}n^{3/2}\left(\sqrt{n+1}+\sqrt{n-1}-2\sqrt{n}\right) = -\frac{1}{4}$$

> The expression in parentheses is infinitesimal of order $3/2$ in the scale $1/n.$ With a factor $n^{3/2},$ the limit is finite and nonzero. With a larger power of $n,$ it is $-\infty,$ while with a smaller power it is $0.$

## What an expansion does not provide

An expansion is a statement about a limit and cannot in general be differentiated term by term. Define $f(0)=0$ and $f(x)=x^2\sin(1/x)$ for $x \neq 0,$ as in the entry on [points of non-differentiability](../points-of-non-differentiability/). Since $|f(x)| \leq x^2,$ we have $f(x)=o(x)$ as $x \to 0.$ This is an expansion of order one with zero coefficients. If we treated it as an identity and differentiated both sides, we would obtain $f'(x)=o(1),$ which would imply $f'(x) \to 0.$ For $x \neq 0,$ however, the derivative is:

$$f'(x) = 2x\sin\frac{1}{x} - \cos\frac{1}{x} \qquad x \neq 0$$

For $x_n=1/(2\pi n)$ and $y_n=1/((2n+1)\pi),$ the derivative tends respectively to $-1$ and $1.$ Hence $f'$ has no limit at the origin, although the expansion of $f$ is correct. If $f$ is locally integrable, its expansion may be [integrated from the centre](../definite-integrals/) term by term, and a remainder $o((x-x_0)^n)$ has an integral of order $o((x-x_0)^{n+1}).$ Termwise differentiation requires separate hypotheses on the derivative.

A second limitation concerns the meaning of the remainder. An expansion of order $n$ describes the behaviour of $f$ as $x \to x_0$ with $n$ fixed, and says nothing about the limit as $n \to \infty$ with $x$ fixed. Convergence of the [Taylor series](../taylor-series/) requires a remainder estimate, such as the Lagrange remainder, that tends to zero as $n \to \infty.$ For the extension of $e^{-1/x^2}$ defined above, every derivative at the origin is zero. Every term of its Taylor series is therefore zero, and the series does not equal the function at any nonzero point. The zero polynomial is nevertheless an asymptotic expansion of every finite order at the origin.

> The relations $\sin x=x+o(x^2)$ and $\sin x=x+O(x^3)$ contain different bounds on the remainder. The first states that the error divided by $x^2$ tends to zero. The second states that the error is bounded in absolute value by a constant multiple of $|x|^3$ near the origin, and is the sharper estimate.
