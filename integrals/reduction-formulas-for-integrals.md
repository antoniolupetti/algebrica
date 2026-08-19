---
title: Reduction Formulas for Integrals
source: https://algebrica.org/reduction-formulas/
license: CC BY-NC 4.0
tags:
  - definite-integral
  - indefinite-integral
  - integration-by-parts
  - integration-techniques
  - recurrence-relations
  - reduction-formulas
---
## Introduction

The reduction formulas introduced below can make integrals that initially appear difficult much easier to evaluate. They are useful for evaluating certain integrals involving exponential or trigonometric functions.

In general, before introducing the formulas, we organise related integrals into indexed families whose members we denote by $I_n.$ This notation simplifies the computations by allowing us to work with a general exponent. In what follows, $n$ always denotes a non-negative integer, unless a particular family requires a stronger restriction. Consider, for example, the following two integrals:

$$\int \sin^3 x dx \quad \text{or} \quad \int \sin^5 x dx$$

We can regard both as members of the following family:

$$I_n=\int\sin^nx \ dx$$

This generalisation allows us to perform the calculation once for a general exponent $n,$ rather than repeat it separately for $n=3$ and $n=5.$ This approach is useful because it significantly reduces the amount of computation in problems involving integrals of this type.

The reduction formulas considered in this post have the form:

$$I_n=g_n(x)+\lambda_nI_{n-k} \tag{1}$$

+ The term $g_n(x)$ is the explicit term produced by the reduction
+ The coefficient $\lambda_n$ depends on the index but not on the variable
+ The integer $k\geq1$ is the step by which the index is reduced.

In what follows, every equality between [indefinite integrals](../indefinite-integrals/) is understood modulo an additive constant. Equivalently, for each family we choose antiderivatives compatible with the recurrence and add the arbitrary constant only to the final result.

The method will become clear in the sections below. As often happens in mathematics, however, it is not always as convenient as this introduction may suggest. A reduction formula is generally useful when the exponent is high enough that [integration by parts](../integration-by-parts/) or another direct manipulation would be lengthy; for low exponents, it is not always the best choice.

## Products of powers of $x$ with $e^{ax}$, $\sin x$, and $\cos x$

We begin with integrals formed by multiplying $x^n$ by an [exponential](../integral-of-the-exponential-function/), and define $J_n$ by:

$$J_n=\int x^ne^{ax} \ dx \qquad a\neq0, \quad n\geq0$$

The factor $e^{ax}$ is easy to integrate, while differentiating $x^n$ lowers its degree. We therefore apply integration by parts with $u=x^n$ and $dv=e^{ax} \ dx.$ This gives $du=nx^{n-1} \ dx$ and $v=e^{ax}/a,$ so the integration-by-parts formula yields:

$$J_n=\frac{x^ne^{ax}}{a}-\frac{n}{a}J_{n-1} \qquad n\geq1 \tag{2}$$

For $n=0,$ the base case is $J_0=e^{ax}/a.$ As an example, we compute the following integral:

$$\int x^3e^x \ dx$$

Applying relation $(2)$ iteratively, we obtain:

$$
\begin{align}
J_3 &= x^3e^x-3J_2 \\[6pt]
J_2 &= x^2e^x-2J_1 \\[6pt]
J_1 &= xe^x-J_0 \\[6pt]
J_0 &= e^x
\end{align}
$$

Starting from the last line, we find $J_1=xe^x-e^x$ and then $J_2=x^2e^x-2xe^x+2e^x.$ Substituting $J_2$ into the first line and factoring out $e^x,$ we obtain:

$$\int x^3e^x \ dx=e^x(x^3-3x^2+6x-6)+c$$

For general $n,$ the closed form has coefficients given by the factorial ratios arising from successive differentiation of $x^n$:

$$\int x^ne^{ax} \ dx=e^{ax}\sum_{k=0}^{n}(-1)^k\frac{n!}{(n-k)!}\frac{x^{n-k}}{a^{k+1}}+c \tag{3}$$

- - -

Replacing the exponential by sine or cosine changes the situation slightly. Setting $u=x^n$ and $dv=\sin x \ dx$ introduces cosine, and a second integration by parts returns to an integral involving sine:

$$\int x^n\sin x \ dx=-x^n\cos x+nx^{n-1}\sin x-n(n-1)\int x^{n-2}\sin x \ dx \qquad n\geq2$$

There are now two base cases: for even $n$ the recurrence terminates at $\int\sin x \ dx,$ and for odd $n$ at $\int x\sin x \ dx.$

## Powers of sine and cosine

We next consider integer powers of sine. Define $S_n$ by:

$$S_n=\int\sin^nx \ dx \qquad n\geq0$$

We write the integrand as $\sin^{n-1}x\cdot\sin x$ and set $u=\sin^{n-1}x$ and $dv=\sin x \ dx,$ from which $du=(n-1)\sin^{n-2}x\cos x \ dx$ and $v=-\cos x.$ Integration by parts allows us to rewrite the integral as:

$$S_n=-\sin^{n-1}x\cos x+(n-1)\int\sin^{n-2}x\cos^2x \ dx$$

The integral on the right does not belong to the family because it contains $\cos^2x.$ Substituting the [fundamental trigonometric identity](../pythagorean-identity/) $\cos^2x=1-\sin^2x$ splits the integral into two members of the family, with indices $n-2$ and $n,$ respectively:

$$S_n=-\sin^{n-1}x\cos x+(n-1)S_{n-2}-(n-1)S_n$$

Moving the term $(n-1)S_n$ to the left and dividing by $n$ gives:

$$S_n=-\frac{\sin^{n-1}x\cos x}{n}+\frac{n-1}{n}S_{n-2} \qquad n\geq2 \tag{4}$$

The cosine case is analogous. Taking $u=\cos^{n-1}x$ and $dv=\cos x \ dx$ gives the counterpart of $(4)$:

$$C_n=\int\cos^nx \ dx=\frac{\cos^{n-1}x\sin x}{n}+\frac{n-1}{n}C_{n-2} \qquad n\geq2 \tag{5}$$

We now determine the two base cases for each family. For the sine family, we have $S_0=x$ and $S_1=-\cos x,$ while for the cosine family we have $C_0=x$ and $C_1=\sin x.$ We apply $(4)$ to $\int\sin^4x \ dx,$ where the first step reduces the index to two and the second to zero:

$$
\begin{align}
S_4 &= -\frac{\sin^3x\cos x}{4}+\frac{3}{4}S_2 \\[6pt]
S_2 &= -\frac{\sin x\cos x}{2}+\frac{1}{2}S_0 \\[6pt]
S_0 &= x
\end{align}
$$

Substituting $S_2$ into the first line and rearranging the terms gives the antiderivative:

$$\int\sin^4x \ dx=-\frac{\sin^3x\cos x}{4}-\frac{3\sin x\cos x}{8}+\frac{3x}{8}+c$$

For odd exponents, $(4)$ remains valid, but it is preferable to factor out $\sin x$ and use the fundamental trigonometric identity to express the remaining factor in terms of cosine. A single [substitution](../integration-by-substitution/) then evaluates the integral, as shown in the discussion of [integrals of trigonometric functions](../integral-of-trigonometric-functions/). The reduction formula is most useful for even exponents, for which the fundamental identity does not lower the exponent.

## Powers of $\tan x$ and $\ln x$

We next consider powers of tangent, for which an algebraic identity suffices. Integration by parts is not needed. Consider the following family:

$$T_n=\int\tan^nx \ dx \qquad n\geq0$$

Using $\tan^2x=\sec^2x-1,$ obtained by dividing the fundamental trigonometric identity by $\cos^2x,$ gives:

$$
\begin{align}
T_n &= \int\tan^{n-2}x(\sec^2x-1) \ dx \\[6pt]
    &= \int\tan^{n-2}x\sec^2x \ dx-T_{n-2}
\end{align}
$$

The first integral is evaluated directly by the substitution $u=\tan x,$ since $du=\sec^2x \ dx.$ Thus:

$$T_n=\frac{\tan^{n-1}x}{n-1}-T_{n-2} \qquad n\geq2 \tag{6}$$

The base cases are $T_0=x$ and $T_1=-\ln|\cos x|.$ The coefficient in $(6)$ equals $-1$ and does not depend on the index, so the recurrence produces an alternating sum of powers of tangent. It terminates at $T_0=x$ for even $n$ and at $T_1=-\ln|\cos x|$ for odd $n.$ For $n=4,$ the recurrence gives $T_4=\tan^3x/3-T_2$ and then $T_2=\tan x-T_0,$ hence:

$$\int\tan^4x \ dx=\frac{\tan^3x}{3}-\tan x+x+c$$

- - -

For powers of the [logarithmic function](../logarithmic-function/), we return to integration by parts. Define $L_n$ by:

$$L_n=\int\ln^nx \ dx \qquad n\geq0$$

We regard the integrand as $\ln^nx\cdot1$ and apply integration by parts with $u=\ln^nx$ and $dv=dx.$ Since $v=x$ and $du=n\ln^{n-1}x/x \ dx,$ the factor $x$ from $v$ cancels the denominator in $du,$ giving:

$$L_n=x\ln^nx-nL_{n-1} \qquad n\geq1 \tag{7}$$

The base case is $L_0=x.$ The recurrence has the same structure as $(2).$ For $n=3,$ repeated application gives $L_3=x\ln^3x-3L_2,$ $L_2=x\ln^2x-2L_1,$ and $L_1=x\ln x-x,$ hence:

$$\int\ln^3x \ dx=x\ln^3x-3x\ln^2x+6x\ln x-6x+c$$

The coefficients $1,3,6,6$ are the same as those in the exponential example, and the coincidence is not accidental. The substitution $x=e^t$ transforms $dx$ into $e^t \ dt$ and $\ln^nx$ into $t^n,$ so the integral defining $L_n$ becomes the case $a=1$ of $J_n,$ with $t$ as the integration variable. Relations $(2)$ and $(7)$ correspond under this substitution.

## Powers of a quadratic denominator

The final family arises in the [integration of rational functions](../integral-of-rational-functions/) and has a different structure from the preceding families. The procedure is more involved, but it is worth presenting because integrals of this type are fairly common:

$$I_n=\int\frac{dx}{(x^2+a^2)^n} \qquad a\neq0, \quad n\geq1$$

The base case is the standard [arctangent](../arctangent-function/) integral:

$$I_1=\frac{1}{a}\arctan\frac{x}{a}$$

We set $u=(x^2+a^2)^{-n}$ and $dv=dx,$ hence $v=x$ and $du=-2nx(x^2+a^2)^{-n-1} \ dx.$ Integration by parts produces:

$$I_n=\frac{x}{(x^2+a^2)^n}+2n\int\frac{x^2}{(x^2+a^2)^{n+1}} \ dx$$

We express the integral on the right in terms of the family by writing $x^2=(x^2+a^2)-a^2$ and splitting the fraction into two terms. The first term reduces to $I_n,$ while the second is $-a^2I_{n+1},$ giving:

$$\int\frac{x^2}{(x^2+a^2)^{n+1}} \ dx=I_n-a^2I_{n+1}$$

Substituting and collecting the $I_n$ terms gives:

$$I_n=x(x^2+a^2)^{-n}+2nI_n-2na^2I_{n+1}$$

Solving for $I_{n+1}$ gives the reduction formula:

$$I_{n+1}=\frac{1}{2na^2}\left[\frac{x}{(x^2+a^2)^n}+(2n-1)I_n\right] \tag{8}$$

This is the only recurrence above that is first written with the higher-index integral on the left. Differentiating the negative power $(x^2+a^2)^{-n}$ changes the exponent to $-n-1,$ increasing its magnitude. Shifting the index gives the descending form, valid for $n\geq2$:

$$I_n=\frac{1}{2(n-1)a^2}\left[\frac{x}{(x^2+a^2)^{n-1}}+(2n-3)I_{n-1}\right]$$

In either form, the recurrence is anchored at the base case $I_1,$ the arctangent integral. The first step gives the frequently used formula for $I_2$:

$$I_2=\frac{x}{2a^2(x^2+a^2)}+\frac{1}{2a^3}\arctan\frac{x}{a}+c$$

Formula $(8)$ evaluates the constant-numerator terms arising after the [partial-fraction decomposition](../partial-fraction-decomposition/) of a rational function with a repeated irreducible quadratic factor. When the denominator contains $(x^2+bx+c)^k$ with negative discriminant, the decomposition contains one term for each power of the factor, from one to $k,$ each with a linear numerator:

$$\frac{A_1x+B_1}{x^2+bx+c}+\frac{A_2x+B_2}{(x^2+bx+c)^2}+\dots+\frac{A_kx+B_k}{(x^2+bx+c)^k}$$

Every numerator can be written as a multiple of the derivative of the denominator plus a constant. The part proportional to the derivative is integrated by substitution and gives a power of the denominator, or a logarithm when the exponent is one. After [completing the square](../completing-the-square/), the constant part reduces to an integral of the form $I_j,$ since the substitution $u=x+b/2$ puts the denominator in the form $u^2+a^2$ with $a^2=c-b^2/4,$ positive because the discriminant is negative.

An example makes the idea clear. For $j=2,$ the numerator is already the sum of the derivative of the denominator and a constant, so the integral separates immediately into two terms:

$$\int\frac{2x+3}{(x^2+4)^2} \ dx=\int\frac{2x}{(x^2+4)^2} \ dx+3\int\frac{dx}{(x^2+4)^2}$$

For the first integral, set $u=x^2+4,$ so that $du=2x \ dx$ and the integral becomes $\int u^{-2} \ du=-1/u.$ The second is $3I_2$ with $a=2,$ so the formula just derived gives:

$$I_2=x/\big(8(x^2+4)\big)+\frac{1}{16}\arctan(x/2).$$

Adding the two contributions and combining the rational terms over a common denominator gives:

$$\int\frac{2x+3}{(x^2+4)^2} \ dx=\frac{3x-8}{8(x^2+4)}+\frac{3}{16}\arctan\frac{x}{2}+c$$

## Recurrences for definite integrals

For [definite integrals](../definite-integrals/), integration by parts gives:

$$\int_a^b u \ dv=\Big[uv\Big]_a^b-\int_a^b v \ du$$

For definite integrals, every reduction formula becomes a recurrence among numerical values. The term $g_n$ in $(1)$ contributes $g_n(b)-g_n(a).$ When this difference vanishes, the recurrence has purely numerical coefficients and the whole family is determined by the base cases alone.

The standard example is the integral of $\sin^nx$ over $[0,\pi/2].$ The explicit term in $(4)$ is $-\sin^{n-1}x\cos x/n.$ It vanishes at $0$ because of the sine factor and at $\pi/2$ because of the cosine factor, so the recurrence reduces to:

$$\int_0^{\pi/2}\sin^nx \ dx=\frac{n-1}{n}\int_0^{\pi/2}\sin^{n-2}x \ dx \qquad n\geq2 \tag{9}$$

The two base cases are $\int_0^{\pi/2}dx=\pi/2$ and $\int_0^{\pi/2}\sin x \ dx=1.$ The recurrence preserves the parity of the index, so the value for even $n$ retains the factor $\pi/2,$ while for odd $n$ it is a rational number. For $n=4$ and $n=5,$ for example, we obtain:

$$\int_0^{\pi/2}\sin^4x \ dx=\frac{3}{4}\cdot\frac{1}{2}\cdot\frac{\pi}{2}=\frac{3\pi}{16}$$

$$\int_0^{\pi/2}\sin^5x \ dx=\frac{4}{5}\cdot\frac{2}{3}=\frac{8}{15}$$

The change of variable $u=\pi/2-x$ interchanges sine and cosine and maps the interval to itself, so the two definite integrals coincide for every $n.$ Applying $(5)$ over the same interval yields the same sequence of values.

> The integrals in $(9)$ are called Wallis integrals. Their monotonicity, asymptotic behaviour, and the associated infinite product are properties of the sequence rather than of the integration technique, so they are treated separately.
