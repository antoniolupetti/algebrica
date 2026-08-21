---
title: Convergence Tests for Improper Integrals
source: https://algebrica.org/convergence-tests-for-improper-integrals/
license: CC BY-NC 4.0
tags:
  - abel-test
  - absolute-convergence
  - cauchy-criterion
  - cauchy-principal-value
  - conditional-convergence
  - dirichlet-test
  - fresnel-integrals
  - improper-integrals
  - oscillating-integrands
  - second-mean-value-theorem
---
## Introduction

In this entry we examine convergence tests for [improper integrals](../improper-integrals/), a class of integrals in which one or both limits of integration are $\pm \infty$ or the integrand is unbounded near a finite endpoint. Recall that these integrals cannot be evaluated simply by subtracting the values of their [antiderivatives](../indefinite-integrals/) at the endpoints, because this would involve an infinite quantity. For this reason, we study the corresponding [limit](../limits/), typically in the following form:

$$\int_a^{+\infty} f(x) \ dx := \lim_{t \to +\infty} \int_a^t f(x) \ dx \tag{1}$$

The entry on improper integrals presented the direct and limit comparison tests, which establish convergence without finding an antiderivative. In the form stated there, however, these tests require an integrand of constant sign and cannot detect conditional convergence when the integrand oscillates, because convergence then depends on cancellation between positive and negative contributions. The tests collected in this entry address this case.

## The Cauchy criterion

The first is the Cauchy criterion, which, as we shall see, does not require the function to have a fixed sign and, more importantly, does not give the value of the integral, but only determines whether it converges. Let $f$ be [Riemann integrable](../riemann-integrability-criteria/) on every interval $[a,t]$ with $t\gt a,$ and let $F$ be its [accumulation function](../fundamental-theorem-of-calculus/):

$$F(t):=\int_a^t f(x) \ dx$$

By the definition of convergence, the improper integral can converge only if $F$ has a finite limit as $t\to+\infty.$ Consider the integral in $(1)$:

$$\int_a^{+\infty}f(x) \ dx$$ 

This integral converges if and only if for every $\varepsilon\gt0$ there exists $c\geq a$ such that:

$$\left|\int_u^v f(x) \ dx\right|\lt\varepsilon \qquad v\gt u\gt c \tag{2}$$

The endpoints $u$ and $v$ are arbitrary, provided that both exceed the threshold $c,$ which depends on $\varepsilon.$


- - -

An analogue of $(2)$ also holds at a single finite endpoint. Suppose that $f$ is Riemann integrable on every interval $[t,b]$ with $a\lt t\lt b$ and unbounded in every right-hand neighbourhood of $a.$ Consider the integral:

$$\int_a^b f(x) \ dx$$

This integral converges if and only if for every $\varepsilon\gt0$ there exists $\delta\gt0$ such that:

$$\left|\int_u^v f(x) \ dx\right|\lt\varepsilon \qquad a\lt u\lt v\lt a+\delta \tag{3}$$

An immediate consequence of $(3)$ is that absolute convergence, meaning convergence of the integral of the [absolute value](../absolute-value/) of the integrand, implies convergence. The relevant inequality is:

$$\left|\int_u^v f(x) \ dx\right|\leq\int_u^v|f(x)| \ dx$$

It follows that if $|f|$ satisfies the Cauchy condition, then so does $f.$

## Dirichlet's test

A second test for the convergence of an improper integral with an oscillatory integrand is Dirichlet's test, which considers two functions $f$ and $g$ defined on an interval $[a,+\infty),$ with $f$ Riemann integrable on every interval $[a,t]$ and $g$ [monotone](../increasing-and-decreasing-functions/). Consider the accumulation function:

$$F(t)=\int_a^t f(x) \ dx \tag{4}$$ 
The test requires two hypotheses:

+ The first is that $F$ is bounded, which means that $|F(t)|\leq K$ for every $t\geq a.$
+ The second is that $g(x)\to0$ as $x\to+\infty$

Now consider the integral:

$$\int_a^{+\infty}f(x)g(x) \ dx \tag{5}$$

If these assumptions are satisfied, the integral converges.

- - - 

To prove this, suppose $K\gt0$ and fix $v\gt u\geq a.$ The [second mean value theorem for integrals](../mean-value-theorem-for-integrals/) provides a point $\xi\in[u,v]$ for which the following identity holds:

$$\int_u^v f(x)g(x) \ dx=g(u)\int_u^{\xi}f(x) \ dx+g(v)\int_{\xi}^v f(x) \ dx \tag{6}$$

We can express the two integrals on the right-hand side in terms of $F$ as follows:

$$\left|\int_u^{\xi}f(x) \ dx\right|=|F(\xi)-F(u)|\leq2K$$

$$\left|\int_{\xi}^v f(x) \ dx\right|=|F(v)-F(\xi)|\leq2K$$

Substituting the preceding relations into $(6)$ gives:

$$\left|\int_u^v f(x)g(x) \ dx\right|\leq2K\big(|g(u)|+|g(v)|\big)$$

Fix $\varepsilon\gt0.$ By the second assumption, $g$ tends to zero, so there exists $c\geq a$ such that $|g(x)|\lt\varepsilon/(4K)$ for every $x\geq c.$ If $v\gt u\geq c,$ both $|g(u)|$ and $|g(v)|$ satisfy this inequality, and the preceding bound becomes:

$$\left|\int_u^v f(x)g(x) \ dx\right|\leq2K\left(|g(u)|+|g(v)|\right)\lt2K\left(\frac{\varepsilon}{4K}+\frac{\varepsilon}{4K}\right)=\varepsilon$$

The Cauchy criterion therefore proves the convergence of the integral $(5)$.

## Abel's test

Abel's test modifies Dirichlet's test by dropping the assumption that the function $g$ tends to zero. Let $f$ and $g$ be defined on $[a,+\infty),$ with $f$ Riemann integrable on every interval $[a,t]$ and $g$ monotone and bounded. Suppose further that the following integral converges:

$$\int_a^{+\infty}f(x) \ dx \tag{7}$$

These assumptions imply that the following integral converges:

$$\int_a^{+\infty}f(x)g(x) \ dx$$

The proof is not particularly difficult and reduces the statement to Dirichlet's test. A bounded monotone function has a finite limit $L$ as $x\to+\infty,$ so the function $h=g-L$ is monotone and tends to zero. The accumulation function $F$ is [continuous](../continuous-functions/) and has a finite limit as $t\to+\infty,$ and is therefore bounded on $[a,+\infty).$ Dirichlet's test applied to the pair $f$ and $h$ guarantees the convergence of:

$$\int_a^{+\infty}f(x)h(x) \ dx$$ 
The decomposition gives:

$$f(x)g(x)=f(x)h(x)+Lf(x)$$

The convergence of $(7)$ therefore proves the claim.

## Integrals involving the sine function

A familiar family of integrals involving the [sine function](../sine-function/) is given by:

$$\int_1^{+\infty}\frac{\sin x}{x^p} \ dx \tag{8}$$

In this case, for every $p\gt0$ the pair $f(x)=\sin x$ and $g(x)=x^{-p}$ satisfies the hypotheses of Dirichlet's test. Moreover, the accumulation function of $f$ is bounded, as shown by:

$$\left|\int_1^t\sin x \ dx\right|=|\cos1-\cos t|\leq2$$

The function $x^{-p}$ is decreasing and tends to zero. It follows that the integral $(8)$ converges for every $p\gt0.$

- - -

Absolute convergence of $(8)$ requires a stricter condition. For $p\gt1$ we consider the following bound:

$$|\sin x|/x^p\leq1/x^p$$

This bound and the $p$-integral test establish absolute convergence. For $0\lt p\leq1$ the integral of the absolute value diverges. The inequality $\sin^2x\leq|\sin x|$ and the identity $\sin^2x=(1-\cos2x)/2$ give:

$$\int_1^T\frac{|\sin x|}{x^p} \ dx\geq\frac{1}{2}\int_1^T\frac{dx}{x^p}-\frac{1}{2}\int_1^T\frac{\cos2x}{x^p} \ dx$$

The first integral on the right tends to $+\infty$ because $p\leq1,$ while the second converges by Dirichlet's test, since $\int_1^t\cos2x \ dx$ is bounded and $x^{-p}$ tends to zero. The right-hand side therefore tends to $+\infty,$ and for $0\lt p\leq1$ the integral $(8)$ converges conditionally.

For $p\leq0$ the Cauchy criterion fails. Let $k$ be a positive integer and define the following interval:

$$I_k=[2k\pi+\pi/6,\ 2k\pi+5\pi/6]$$ 

On this interval $\sin x\geq1/2,$ and $p\leq0$ implies $x^{-p}\geq1$ for $x\geq1,$ so:

$$\int_{I_k}\frac{\sin x}{x^p} \ dx\geq\frac{1}{2}\cdot\frac{2\pi}{3}=\frac{\pi}{3}$$

The endpoints of $I_k$ tend to $+\infty$ while the integral over $I_k$ stays bounded away from zero, so the integral $(8)$ does not converge. We can therefore summarize the cases in the table:

[class="table-1"]

|              |                          |
| ------------ | ------------------------ |
| $p\gt1$        | converges absolutely     |
| $0\lt p\leq1$   | converges conditionally  |
| $p\leq0$     | does not converge        |

[/class]

## The Fresnel integrals

Dirichlet's test also applies to the Fresnel integrals, whose integrands do not tend to zero. These integrals are of the form:

$$\int_0^{+\infty}\sin(x^2) \ dx=\int_0^{+\infty}\cos(x^2) \ dx=\frac{1}{2}\sqrt{\frac{\pi}{2}}$$

Consider the sine case:

$$\int_0^{+\infty}\sin(x^2) \ dx \tag{9}$$

On the interval $[0,1]$ the integrand is continuous and the integral is proper. On the interval $[1,T]$ we make the [substitution](../integration-by-substitution/) $t=x^2,$ with $x=\sqrt t$ and $dx=dt/(2\sqrt t),$ obtaining:

$$\int_1^T\sin(x^2) \ dx=\frac{1}{2}\int_1^{T^2}\frac{\sin t}{\sqrt t} \ dt$$

The right-hand side has a finite limit as $T\to+\infty$ because it corresponds to the case $p=1/2$ of the family $(8).$ Adding the proper integral over $[0,1]$ shows that $(9)$ converges. Since $p=1/2\lt1,$ the integral of the absolute value diverges and the convergence is conditional. The same substitution can be applied to $\cos(x^2)$ and leads to the same conclusions.

The two integrals are known as the Fresnel integrals and have the same value:

$$\int_0^{+\infty}\sin(x^2) \ dx=\int_0^{+\infty}\cos(x^2) \ dx=\frac{1}{2}\sqrt{\frac{\pi}{2}}$$

This value can be computed using methods from complex analysis.

> Recall that convergence of a [series](../cauchy-convergence-criterion-series/) $\sum a_n$ requires $a_n\to0,$ whereas no analogous condition holds for improper integrals, and $\sin(x^2)$ is a counterexample: it oscillates between $-1$ and $1$ without having a limit, yet its integral converges. The local wavelength is asymptotic to $\pi/x,$ so the integrals over consecutive lobes alternate in sign and decrease in absolute value to zero, and their contributions behave like the terms of an [alternating series](../leibniz-criterion/).

## The Cauchy principal value

To conclude, we introduce the Cauchy principal value, which is the limit of integrals over intervals symmetric about the origin and is defined by:

$$\mathrm{p.v.}\int_{-\infty}^{+\infty}f(x) \ dx:=\lim_{R\to+\infty}\int_{-R}^{R}f(x) \ dx$$

Consider the following [odd function](../even-and-odd-functions/):

$$f(x)=\frac{2x}{1+x^2}$$

Now consider the improper integral over $\mathbb{R}$:

$$\int_{-\infty}^{+\infty}\frac{2x}{1+x^2} \ dx$$

This integral does not converge, because for every $R$ we have

$$\int_0^R f(x) \ dx=\ln(1+R^2) \to +\infty$$

$$\int_{-R}^R f(x) \ dx=0$$

Thus the principal value is zero.

If an ordinary improper integral over $\mathbb{R}$ converges, its principal value exists and agrees with the improper integral, because taking symmetric bounds is a special case of letting the two bounds tend to infinity independently. The converse, however, is false, as the preceding example shows.
