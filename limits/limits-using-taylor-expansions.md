---
title: Limits Using Taylor Expansions
source: https://algebrica.org/limits-using-taylor-expansions/
license: CC BY-NC 4.0
tags:
  - indeterminate-forms
  - limits
  - little-o-notation
  - peano-remainder
  - taylor-polynomial
---

## Taylor expansions

As we know, a [Taylor series expansion](../taylor-series/) expresses a function about a point as the sum of a [polynomial](../polynomials/) and a remainder. This representation is useful when direct substitution in a [limit](../limits/) produces an [indeterminate form](../indeterminate-forms/), because it allows us to simplify the original expression and identify the remaining terms so that we can assess the contribution of the error. Suppose, then, that a function $f$ is defined on a [neighbourhood](../topology-of-the-real-line/) of $x_0$ and is $n$ times differentiable at $x_0,$ with $n\geq1.$ This method is preferable to [de l'Hôpital's rule](../hopital-rule/) or algebraic manipulation when these require lengthy calculations, because it allows us to determine the limit more directly. As $x\to x_0,$ [Taylor's formula with the Peano remainder](../taylor-formula-with-remainder/) gives the following equality:

$$
f(x)=\sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k+o\big((x-x_0)^n\big) \tag{1}
$$

The polynomial in $(1)$ has the same [derivatives](../higher-order-derivatives/) as $f$ through order $n$ at $x_0,$ while the remainder is the difference between the function and the polynomial, and the [little-o notation](../little-o-notation/) means that:

$$
\lim_{x\to x_0}\frac{f(x)-\displaystyle\sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k}{(x-x_0)^n}=0 \tag{2}
$$

Equation $(2)$ justifies the use of the expansion in limits, because the remainder, once divided by $(x-x_0)^n,$ tends to zero and therefore does not contribute to the value of the limit. When $x_0=0$ in $(2),$ the expansion is also called a Maclaurin expansion. For [expansions of elementary functions](../taylor-formula-with-remainder/) used in solving problems, see the corresponding entry.

## Choosing the order of the expansion

To apply this method to limits, we first need to choose the order to which the functions should be expanded, because some terms may cancel and the remainder must be small enough to tend to zero after division by the denominator. Consider, for example, the following limit:

$$
\lim_{x\to0}\frac{\cos x-1+\dfrac{x^2}{2}}{x^4} \tag{3}
$$

If we stop at the expansion of order $2$ in $(3)$ we obtain:

$$\cos x=1-x^2/2+o(x^2)$$

This expansion is insufficient, however, because the quotient $o(x^2)/x^4$ does not necessarily tend to zero, and the remainder may contain a term of degree four that contributes to the limit. Continuing the expansion through degree $4$ gives:

$$
\begin{align}
\cos x-1+\frac{x^2}{2}&=1-\frac{x^2}{2}+\frac{x^4}{24}+o(x^4)-1+\frac{x^2}{2} \notag \\[6pt]
&=\frac{x^4}{24}+o(x^4) \tag{4}
\end{align}
$$

Dividing $(4)$ by $x^4,$ the remainder becomes $o(1)$ and the limit in $(3)$ is $1/24.$ More generally, suppose that the denominator has the following form, with $b\neq0$ and $m$ a positive integer:

$$bx^m+o(x^m)$$

The general rule is to expand the numerator as a whole through order $m,$ so that the remainder tends to zero after division by the denominator. If the terms of lower degree cancel and we are left with $ax^m+o(x^m),$ we have:

$$
\lim_{x\to0}\frac{ax^m+o(x^m)}{bx^m+o(x^m)}
=\lim_{x\to0}\frac{a+o(1)}{b+o(1)}=\frac ab \tag{5}
$$

If the coefficient $a$ is also zero, the numerator is $o(x^m)$ and the limit is zero. If, instead, a nonzero term of degree less than $m$ remains in the numerator, the quotient cannot have a finite limit and there is no need to continue the expansion, because terms of higher degree cannot cancel the term already identified. We then examine the sign of the quotient to determine whether the limit is infinite or the two one-sided limits are infinite with opposite signs.

## Operations and control of the remainder

Taylor series expansions can be combined using the usual algebraic operations while keeping track of the remainders. As $x\to0$ the following relations hold:

$$
\begin{align}
o(x^m)+o(x^m)&=o(x^m) \notag \\[6pt]
x^r o(x^m)&=o(x^{m+r}) \notag \\[6pt]
\frac{o(x^m)}{x^r}&=o(x^{m-r}) \tag{6}
\end{align}
$$

We illustrate the rules in $(6)$ by calculating the following limit, for which direct substitution gives the indeterminate form $0/0:$

$$
\lim_{x\to0}\frac{e^x-1-x}{\sin^2 x} \tag{7}
$$

In the numerator, we use the expansion $e^x=1+x+x^2/2+o(x^2),$ obtaining $x^2/2+o(x^2).$ In the denominator, the expansion $\sin x=x+o(x)$ is sufficient, because we then square it to obtain:

$$
\sin^2 x=(x+o(x))^2=x^2+o(x^2) \tag{8}
$$

Applying $(5)$ and $(8)$ gives:

$$
\lim_{x\to0}\frac{e^x-1-x}{\sin^2 x}
=\lim_{x\to0}\frac{\dfrac{x^2}{2}+o(x^2)}{x^2+o(x^2)}=\frac12 \tag{9}
$$

## Expansions of composite functions

Limits may involve [composite functions](../composite-functions/) such as $e^{x^2},$ in which the argument of the exponential is $x^2$ rather than $x.$ To expand them, we can start with the expansion of the outer function at the origin and substitute the inner expression for its variable, provided that this expression tends to zero. The substitution must also be made in the remainder, whose order must be expressed in terms of the variable of the limit. Consider, for example, the following limit:

$$
\lim_{x\to0}\frac{e^{x^2}-\cos x-\dfrac32x^2}{x^4} \tag{10}
$$

For the exponential, we set $t=x^2$ and, since $t\to0,$ we can use the expansion of $e^t$ through order two, so that $t^2$ becomes $x^4$ and the remainder $o(t^2)$ becomes $o(x^4),$ giving:

$$
\begin{align}
e^{x^2}&=1+x^2+\frac{x^4}{2}+o(x^4) \notag \\[6pt]
\cos x&=1-\frac{x^2}{2}+\frac{x^4}{24}+o(x^4) \tag{11}
\end{align}
$$

Substituting $(11)$ and cancelling terms leaves:

$$
e^{x^2}-\cos x-\frac32x^2=\frac{11}{24}x^4+o(x^4) \tag{12}
$$

In $(12),$ after division by $x^4,$ the remainder tends to zero and the limit in $(10)$ is $11/24.$

## Exponential forms

Taylor expansions also allow us to handle forms such as $1^\infty,$ by taking [logarithms](../logarithms/) and evaluating the resulting limit. For example, consider the following limit, which cannot be evaluated by direct substitution:

$$
\lim_{x\to0}\left(\frac{\sin x}{x}\right)^{1/x^2} \tag{13}
$$

Set $y(x)=(\sin x/x)^{1/x^2}.$ Since $\sin x/x$ tends to $1,$ the base is positive for $x$ sufficiently close to zero, with $x\neq0,$ and we can take logarithms to obtain:

$$
\ln y(x)=\frac{1}{x^2}\ln\left(\frac{\sin x}{x}\right) \tag{14}
$$

We now use the expansion $\sin x=x-x^3/6+o(x^3)$ and, after dividing by $x,$ we can write the base as $1+u(x)$ and identify the term $u(x):$

$$
\begin{align}
\frac{\sin x}{x}&=1+u(x) \notag \\[6pt]
u(x)&=-\frac{x^2}{6}+o(x^2) \tag{15}
\end{align}
$$

We then use the expansion $\ln(1+u)=u+o(u)$ and, by $(15),$ we have $u(x)/x^2\to-1/6,$ so the remainder $o(u(x))$ is also $o(x^2).$ Thus $(14)$ becomes:

$$
\ln y(x)=\frac{-\dfrac{x^2}{6}+o(x^2)}{x^2}\longrightarrow-\frac16 \tag{16}
$$

By [continuity](../continuous-functions/) of the [exponential function](../exponential-function/), $y(x)=e^{\ln y(x)}$ implies that the limit in $(13)$ is $e^{-1/6}.$

## Nonzero points and limits at infinity

Taylor expansions at the origin can also be used when the variable tends to another point. Indeed, for a limit as $x\to a$ we can set $h=x-a,$ so that $h\to0.$ For example, we rewrite the following limit:

$$
\lim_{x\to1}\frac{\ln x-(x-1)}{(x-1)^2}
=\lim_{h\to0}\frac{\ln(1+h)-h}{h^2} \tag{17}
$$

The expansion $\ln(1+h)=h-h^2/2+o(h^2)$ shows that the numerator in $(17)$ is $-h^2/2+o(h^2).$ Dividing by $h^2,$ we therefore obtain the limit $-1/2.$ For a limit at infinity, we can instead introduce the variable $t=1/x$ to obtain our result. Consider, for example, the following limit, for which direct substitution gives the indeterminate form $\infty-\infty:$

$$
\lim_{x\to+\infty}\left(\sqrt{x^2+x}-x\right) \tag{18}
$$

Since $x\gt0,$ we factor $x$ out of the square root and set $t=1/x.$ As $x\to+\infty,$ we have $t\to0^+$ and the expression becomes:

$$
\sqrt{x^2+x}-x=x\left(\sqrt{1+\frac1x}-1\right)=\frac{\sqrt{1+t}-1}{t} \tag{19}
$$

We now choose $\alpha=1/2$ in the power expansion and retain terms through first order:

$$
\sqrt{1+t}=1+\frac t2+o(t) \tag{20}
$$

Substituting $(20)$ into $(19),$ the constant terms cancel and we obtain:

$$
\lim_{t\to0^+}\frac{\dfrac t2+o(t)}{t}=\frac12 \tag{21}
$$

