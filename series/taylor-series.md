---
title: Taylor Series
source: https://algebrica.org/taylor-series/
license: CC BY-NC 4.0
tags:
  - analytic-functions
  - maclaurin-series
  - power-series
  - taylor-series
---
## Introduction

The idea behind a Taylor series is to replace a function with an infinite [polynomial](../polynomials/) whose coefficients are entirely determined by the local behaviour of the function at a single point. This perspective reduces the study of a wide class of [functions](../functions/) to the algebraic manipulation of [power series](../power-series/) and at the same time it provides a constructive way to approximate values that would otherwise be inaccessible by elementary means.

Throughout this page we shall assume familiarity with the notion of [derivative](../derivatives/) of arbitrary order and with the basic theory of power series, in particular with the notion of radius of convergence.

Let $f$ be a real function defined on an open interval containing the point $a$. The question we want to address is whether it is possible to represent $f$ on a neighbourhood of $a$ by means of an expression of the form:

$$
f(x) = \sum_{n=0}^{\infty} c_n (x-a)^n
$$

The coefficients $c_n$ are [real numbers](../real-numbers/) and the series converges in some [interval](../intervals/) centred at $a$. When such a representation exists with positive radius of convergence, the function is said to be analytic at $a$.

The class of analytic functions includes nearly every elementary function on its [domain](../determining-the-domain-of-a-function/): polynomials, [exponentials](../exponential-function/), [logarithms](../logarithmic-function/) on the positive half-line, trigonometric and hyperbolic functions, [rational functions](../rational-functions/) away from their poles, and roots away from branch points. The functions that fail to be analytic at a given point are those that exhibit a singular behaviour there, such as a vertical tangent, an infinite value, or some form of irregular oscillation.

## Determination of the coefficients

The main observation is that, if a representation of the form written above exists, then the coefficients $c_n$ are determined by $f$ and its derivatives at $a$. To see this, recall that within the radius of convergence a power series can be differentiated term by term, and the resulting series has the same radius of convergence as the original one. Setting $x = a$ in the original series leaves only the term with $n = 0$, so we obtain:

$$
c_0 = f(a)
$$

Differentiating once and then evaluating at $a$ eliminates all terms except the one corresponding to $n = 1$, yielding:

$$
c_1 = f'(a)
$$

Differentiating twice produces a factor $2 \cdot 1$ in front of $c_2$, so that:

$$
c_2 = \frac{f''(a)}{2!}
$$

Iterating this procedure, the $N$-th derivative of the series evaluated at $a$ yields a single non-vanishing term, which carries the [factorial](../factorial/) $N!$ and the coefficient $c_N$. The general formula is therefore:

$$
c_n = \frac{f^{(n)}(a)}{n!}
$$

This computation, which is algebraic once term-by-term differentiation has been justified, is the content of the following statement.

## The Taylor series theorem

Let $f$ be analytic at $a$, so that there exist coefficients $c_n$ and a positive radius $R$ for which the following holds when $|x-a| < R$:

$$f(x) = \sum_{n=0}^{\infty} c_n (x-a)^n $$

Then the coefficients are given by:

$$
c_n = \frac{f^{(n)}(a)}{n!} \qquad n = 0, 1, 2, \dots
$$

The representation takes the explicit form:

$$
f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!} (x-a)^n
$$

This expression is called the Taylor series of $f$ centred at $a$. When the centre is chosen at the origin (when $a = 0$), the series is referred to as the Maclaurin series of $f$.

> A common source of confusion concerns the meaning of the symbols $f^{(n)}(a)$. These are real numbers, obtained by computing the $n$-th derivative as a function of $x$ and then evaluating at the centre $a$. They are not functions of $x$ and the variable $x$ appears only through the factors $(x-a)^n$.


## Taylor polynomials and the formula with remainder

In practice the infinite series cannot be summed exactly and one truncates it after a finite number of terms. The following polynomial is called the Taylor polynomial of $f$ of order $N$ centred at $a$:

$$
T_N(x) = \sum_{n=0}^{N} \frac{f^{(n)}(a)}{n!} (x-a)^n
$$

The first non-trivial case, corresponding to $N = 1$, recovers the linear approximation:

$$
T_1(x) = f(a) + f'(a)(x-a)
$$

The graph of $T_1$ is the tangent line to $f$ at $a$. Higher-order Taylor polynomials provide successively better local approximations, in the sense that they share with $f$ an increasing number of [derivatives](../derivatives/) at the centre. The discrepancy between the function and its $N$-th Taylor polynomial is called the remainder of order $N$ and is denoted as:

$$
R_N(x) = f(x) - T_N(x)
$$

If $f$ is of class $C^{N+1}$ on an interval containing both $a$ and $x$, then there exists a point $\xi$ strictly between $a$ and $x$ such that:

$$
R_N(x) = \frac{f^{(N+1)}(\xi)}{(N+1)!} (x-a)^{N+1}
$$

Saying that the Taylor series of $f$ converges to $f$ on an interval is therefore equivalent to saying that $R_N(x) \to 0$ as $N \to \infty$ for every $x$ in that interval.

> The mere existence of all derivatives of $f$ at $a$ is sufficient to write down the Taylor series formally, but it does not guarantee that the series converges to $f$. The convergence must be checked separately, and this is precisely the role of the remainder.

## A criterion for analyticity

The remainder formula yields a workable sufficient condition for the convergence of the Taylor series to its function. Suppose $f$ is infinitely differentiable on the closed interval $I = [a-r, a+r]$ and denote by $M_k$ the largest value attained by the absolute value of the $k$-th derivative on this interval:

$$
M_k = \max_{|x-a| \leq r} |f^{(k)}(x)|
$$

If these bounds decay fast enough to satisfy:

$$
\lim_{k \to \infty} \frac{M_k}{k!} r^k = 0
$$

then $f$ is analytic at $a$ and coincides with its Taylor series on the whole interval $I$. The proof is immediate from the Lagrange remainder, since for $|x-a| \leq r$ we have $|R_N(x)| \leq \frac{M_{N+1}}{(N+1)!} r^{N+1}$, and the right-hand side tends to zero by hypothesis.

> This criterion turns the analytic question into an estimate on the derivatives. When the derivatives of $f$ admit a uniform bound on $I$, or grow slowly enough to be dominated by the factorial, the series represents the function throughout $I$.

## Maclaurin series of the exponential function

Consider the function $f(x) = e^x$, which satisfies the elementary differential identity $f'(x) = f(x)$. Every derivative of $f$ coincides with $f$ itself and evaluating at the origin, for every $n \geq 0$, yields:

$$
f^{(n)}(0) = e^0 = 1
$$

The Maclaurin coefficients are therefore $c_n = 1/n!$, and the resulting series is:

$$
e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots
$$

To establish convergence for every real $x$ it suffices to apply the [ratio test](../ratio-test-for-series-convergence/) to the absolute values of the terms:

$$
\lim_{n \to \infty} \left| \frac{x^{n+1}/(n+1)!}{x^n/n!} \right| = \lim_{n \to \infty} \frac{|x|}{n+1} = 0
$$

Since the limit is zero regardless of $x$, the series converges absolutely on the whole real line. On any interval $[-r, r]$ every derivative of $e^x$ is bounded by $M_k = e^r$, so the criterion for analyticity applies and the sum of the series is precisely $e^x$.

## Irrationality of e

Evaluating the exponential series at $x = 1$ expresses Euler's number as a sum of reciprocal factorials:

$$
e = \sum_{k=0}^{\infty} \frac{1}{k!}
$$

This representation leads to a short proof that $e$ is [irrational](../irrational-numbers/), and the argument rests on a sharp estimate of the tail of the series. For every integer $q \geq 1$ the terms beyond the $q$-th can be bounded by a geometric series:

$$
\sum_{k=q+1}^{\infty} \frac{1}{k!} = \frac{1}{(q+1)!}\left(1 + \frac{1}{q+2} + \frac{1}{(q+2)(q+3)} + \cdots\right) < \frac{1}{(q+1)!} \sum_{k=0}^{\infty} \frac{1}{(q+2)^k}
$$

The geometric sum on the right equals $\frac{q+2}{q+1}$, and simplifying the resulting product yields the bound:

$$
\sum_{k=q+1}^{\infty} \frac{1}{k!} < \frac{1}{q \cdot q!}
$$

Suppose now, for contradiction, that $e$ is rational, so that $e = p/q$ with $p$ and $q$ coprime positive integers. Subtracting the partial sum up to $k = q$ and using the tail estimate gives:

$$
0 < \frac{p}{q} - \sum_{k=0}^{q} \frac{1}{k!} = \sum_{k=q+1}^{\infty} \frac{1}{k!} < \frac{1}{q \cdot q!}
$$

Multiplying through by $q!$ produces:

$$
0 < p (q-1)! - \sum_{k=0}^{q} \frac{q!}{k!} < \frac{1}{q} \leq 1
$$

The central expression is an integer, because each term $q!/k!$ with $k \leq q$ is a whole number and $p(q-1)!$ is one as well. No integer lies strictly between $0$ and $1$, so the assumption is untenable and $e$ is irrational.

## Maclaurin series of sine and cosine

The functions [sine](../sine-function/) and [cosine](../cosine-function/) are perhaps the most instructive example because their derivatives cycle through a period of length four. For $f(x) = \sin x$ we have:

$$
\begin{align}
f(x) &= \sin x \\[6pt]
f'(x) &= \cos x \\[6pt]
f''(x) &= -\sin x \\[6pt]
f'''(x) &= -\cos x
\end{align}
$$

From the fourth derivative onwards the pattern repeats. Evaluating at the origin we obtain the following sequence:

$$0, 1, 0, -1, 0, 1, 0, -1, \dots$$

So that all even-indexed coefficients vanish and the odd-indexed ones alternate in sign. Substituting into the general formula gives:

$$
\sin x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots
$$

An analogous computation, starting from $f(x) = \cos x$, yields:

$$
\cos x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots
$$

The ratio test, applied as in the case of the exponential, shows that both series converge for every real $x$. Since all derivatives of sine and cosine are bounded by $M_k = 1$ on every interval, the criterion for analyticity guarantees that the sums are $\sin x$ and $\cos x$. Note that the same series interpreted with [complex arguments](../complex-numbers-introduction/) are the foundation of Euler's identity $e^{ix} = \cos x + i \sin x$, but this connection lies beyond the scope of the present discussion.

> The fact that the Maclaurin series of $\sin x$ contains only odd powers, and that of $\cos x$ only even powers, is a manifestation of the [parity](../even-and-odd-functions/) of these functions: $\sin$ is odd and $\cos$ is even.


## Maclaurin series of the logarithm

The [logarithmic function](../logarithmic-function/) presents an additional subtlety, because $\ln x$ is not defined at the origin. To obtain a Maclaurin series we therefore consider the shifted function $f(x) = \ln(1+x)$, which is well defined and infinitely differentiable on the interval $(-1, +\infty)$. Computing successive derivatives we find:

$$
f^{(n)}(x) = (-1)^{n-1} \frac{(n-1)!}{(1+x)^n} \qquad \text{for } n \geq 1
$$

Evaluating at the origin yields $f^{(n)}(0) = (-1)^{n-1} (n-1)!$. The corresponding coefficients are $c_n = (-1)^{n-1}/n$, and the Maclaurin series reads:

$$
\ln(1+x) = \sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots
$$

The ratio test shows that the radius of convergence is exactly equal to $1$, and a more delicate analysis at the boundary establishes convergence at $x = 1$, with the celebrated identity:

$$
\ln 2 = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots
$$

## The binomial series

A further fundamental example is provided by the function $f(x) = (1+x)^{\alpha}$, where $\alpha$ is an arbitrary real exponent. When $\alpha$ is a non-negative [integer](../integers/) the function is a polynomial and the Maclaurin series reduces to the [binomial expansion](../binomial-theorem/) of Newton. For a general real exponent the situation is more interesting, since the series is infinite and its convergence depends on the magnitude of $x$. Successive differentiation gives:

$$
f^{(n)}(x) = \alpha (\alpha - 1) \cdots (\alpha - n + 1) (1+x)^{\alpha - n}
$$

Evaluation at the origin yields the generalised [binomial coefficients](../binomial-coefficient/):

$$
\binom{\alpha}{n} = \frac{\alpha (\alpha - 1) \cdots (\alpha - n + 1)}{n!}
$$

The Maclaurin series therefore takes the form:

$$
(1+x)^{\alpha} = \sum_{n=0}^{\infty} \binom{\alpha}{n} x^n
$$

The radius of convergence follows from the ratio of consecutive coefficients:

$$
\left| \frac{\binom{\alpha}{n+1}}{\binom{\alpha}{n}} \right| = \left| \frac{\alpha - n}{n+1} \right| \longrightarrow 1 \qquad (n \to \infty)
$$

so the series converges for $|x| < 1$. To identify its sum, denote by $f$ the function it defines on the interval $(-1, 1)$ and differentiate it term by term:

$$
f'(x) = \sum_{n=1}^{\infty} \binom{\alpha}{n} n x^{n-1}
$$

The generalised binomial coefficients satisfy the identity:

$$
\binom{\alpha}{n+1}(n+1) + \binom{\alpha}{n} n = \alpha \binom{\alpha}{n}
$$

Multiplying $f'(x)$ by $(1+x)$ and collecting equal powers of $x$ through this identity gives the differential equation:

$$
(1+x) f'(x) = \alpha f(x)
$$

Consider now the auxiliary function $F(x) = f(x)(1+x)^{-\alpha}$. Its derivative is:

$$
F'(x) = \frac{(1+x) f'(x) - \alpha f(x)}{(1+x)^{\alpha+1}} = 0 \qquad |x| < 1
$$

so $F$ is constant on $(-1, 1)$. Since $F(0) = 1$, we have $F(x) = 1$ throughout the interval, which is to say $f(x) = (1+x)^{\alpha}$. The Maclaurin series therefore represents the function on $|x| < 1$.

## Example

To appreciate the practical strength of the method we compute an approximation of $\sin(10^{\circ})$. Trigonometric arguments must first be expressed in radians, so we write

$$
10^{\circ} = \frac{\pi}{180} \cdot 10 = \frac{\pi}{18}
$$

The value $\pi/18$ is approximately $0.1745$, which is small enough to expect rapid convergence of the Maclaurin series. Truncating after the cubic term we obtain:

$$
\sin\!\left(\tfrac{\pi}{18}\right) \approx \frac{\pi}{18} - \frac{1}{3!} \left(\frac{\pi}{18}\right)^3
$$

Substituting a sufficiently accurate value of $\pi$ and performing the arithmetic, the Taylor polynomial of order three already yields $\sin(10^{\circ}) \approx 0.173648$, in agreement with the true value to five decimal places.

## Choice of the centre

An essential aspect of the method concerns the choice of the centre $a$ of the expansion. The choice is constrained by three requirements that must be balanced against one another: 

+ the function must be analytic at $a$.
+ the value $f(a)$ and the derivatives $f^{(n)}(a)$ must be computable in closed form.
+ the distance $|x - a|$ must be small enough to fall within the radius of convergence and to ensure rapid decay of the terms.

To illustrate this point, suppose we wish to compute $\sqrt{2}$ by means of the Taylor series of $f(x) = \sqrt{x}$. The candidate $a = 0$ is excluded, because $\sqrt{x}$ is not analytic at the origin: a series in non-negative powers of $x$ would force the function to be defined for negative arguments, which is impossible. 

The choice $a = 1$ gives convergent derivatives, but the distance $|2 - 1| = 1$ coincides with the radius of convergence and the series converges very slowly. The choice $a = 2$ is circular, since computing $f(2)$ is exactly the problem we wish to solve. A compromise is $a = 9/4$, because $\sqrt{9/4} = 3/2$ is rational, the distance $|2 - 9/4| = 1/4$ is small, and the derivatives can be evaluated explicitly. With this choice the partial sums of the Taylor series converge to $\sqrt{2}$ at a satisfactory rate, and a few terms suffice to obtain five-digit accuracy.

The result of this construction is that $\sqrt{2} \approx 1.41421$, already attained by the Taylor polynomial of order four centred at $9/4$.

## Smooth functions that are not analytic

One may wonder whether infinite differentiability alone guarantees that a function coincides with the sum of its Taylor series. The answer is negative, and the standard counterexample is the function:

$$
f(x) = \begin{cases} e^{-1/x^2} & \text{if } x \neq 0 \\[6pt] 0 & \text{if } x = 0\end{cases}
$$

A direct computation, which uses the fact that exponentials decay faster than any polynomial, shows that all derivatives of $f$ at the origin are equal to zero. Consequently the Maclaurin series of $f$ is identically zero,

$$
\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!} x^n = 0
$$

Yet the function itself takes strictly positive values for every $x \neq 0$. The Taylor series exists, converges everywhere, but does not represent the function except at the single point $x = 0$. This phenomenon clarifies once more that analyticity is a stronger property than $C^{\infty}$ regularity, and that the Lagrange remainder cannot be ignored.

## Applications

Three classes of problems deserve to be mentioned at least briefly. The first concerns the computation of [limits of indeterminate form](../indeterminate-forms/). Replacing each factor of an expression by a Taylor polynomial of suitable order often reveals the dominant behaviour and resolves indeterminacies of type $0/0$ without recourse to repeated applications of de [l'Hôpital's rule](../hopital-rule/). For instance, the well-known limit $\lim_{x \to 0} (\sin x)/x = 1$ follows immediately from the Maclaurin series of the sine, since $(\sin x)/x = 1 - x^2/6 + O(x^4)$ tends to $1$ as $x \to 0$.

The second class concerns the integration of functions whose antiderivatives cannot be expressed in elementary terms. The following [integrals](../integrals/) have no representation in closed form:

$$
\int e^{-x^2}\ dx \qquad \text{and} \qquad \int \frac{\sin x}{x}\ dx
$$

Their integrands admit Maclaurin series that can be integrated term by term, producing series representations of the antiderivatives that are perfectly suited for numerical evaluation.

The third class concerns the resolution of [differential equations](../differential-equations/) by series methods. Seeking a solution in the form of a power series and substituting into the equation produces a recurrence relation for the coefficients, which in many cases can be solved explicitly.

The Taylor series construction shows that the entire global behaviour of an analytic function is encoded in the sequence of its derivatives at a single point. This rigidity is one of the defining features of the analytic category and has no counterpart among smooth functions, where local data and global behaviour are to a large extent independent. 

The same rigidity reappears, in an even more striking form, in the theory of holomorphic functions of a complex variable, where it leads to the principle of analytic continuation and to the celebrated identity theorem. The real-variable Taylor series presented here is the elementary face of a phenomenon that pervades large portions of modern analysis.