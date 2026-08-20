---
title: Integrals of Irrational Functions
source: https://algebrica.org/integrals-of-irrational-functions/
license: CC BY-NC 4.0
tags:
  - binomial-differentials
  - completing-the-square
  - euler-substitution
  - indefinite-integral
  - integration-by-substitution
  - integration-techniques
  - irrational-functions
  - rationalizing-substitution
---
## Introduction

Integrals of [irrational functions](../irrational-functions/), where the variable appears under a radical sign, can be rather laborious if one does not know the techniques needed to evaluate them comfortably. As a rule, our aim is to reduce the initial integral to a form free of radicals and to turn the problem into an [integral of a rational function](../integral-of-rational-functions/), whose evaluation is far simpler.

Let $R(u,v)$ denote a rational function in the two indeterminates $u$ and $v.$ Consider a [substitution](../integration-by-substitution/) $x=\chi(t)$ and set $\psi(t)=\sqrt[n]{\varphi\big(\chi(t)\big)}.$ If $\chi(t)$ and $\psi(t)$ are rational functions of $t,$ the substitution rationalises the integral and we have:

$$\int R\big(x,\sqrt[n]{\varphi(x)}\big) \ dx=\int R\big(\chi(t),\psi(t)\big)\chi'(t) \ dt$$

In what follows, every substitution is understood on an interval of the real domain where a branch of the [radicals](../radicals/) is fixed and the denominators do not vanish. This convention lets us read the identities between radicals and powers without introducing sign changes.

This is the formula of the general procedure, but it should be kept in mind that not every irrational function admits an elementary antiderivative. Integrals such as the one below belong to the class of elliptic integrals and cannot be expressed in terms of elementary functions:

$$\int\frac{dx}{\sqrt{1-x^4}}$$

All the substitutions discussed in this entry therefore concern only the cases where rationalisation is possible, and elliptic integrals are left to a separate treatment. Before going on, make sure you have acquired the main [integration techniques](../integration-strategies/), since otherwise what follows may be hard to understand.

## Radicals of linear fractional expressions

We begin with a relatively simple case, an integrand that is rational in $x$ and in the $n$-th root of a ratio of two first-degree binomials:

$$\int R\left(x,\sqrt[n]{\frac{ax+b}{cx+d}}\right) \tag{1}dx$$

Before going on we must impose the condition $ad-bc\neq0,$ which rules out the case where numerator and denominator are proportional. If they were, the radical would reduce to a number and no substitution would be needed. The point becomes clearer with the following example. Set $a=2,$ $b=4,$ $c=1$ and $d=2,$ which gives:

$$\sqrt{\frac{2x+4}{x+2}}=\sqrt2 \qquad x\neq-2$$

The radical is a constant and the integrand is already rational in $x$ alone, so no substitution is required. Since luck favours few, one more often meets integrals that do require a substitution, which for $(1)$ consists in replacing the radical with $t$:

$$t=\sqrt[n]{\frac{ax+b}{cx+d}}$$

The previous expression implies that:

$$t^n=\frac{ax+b}{cx+d}$$

At this point we solve the second equality for $x,$ and a few elementary algebraic steps give:

$$x=\frac{b-dt^n}{ct^n-a}$$

This is a rational function of $t,$ and so is its derivative. Expanding the derivative of the quotient, the numerator collapses to the constant $ad-bc$ multiplied by $nt^{n-1}$:

$$dx=\frac{n(ad-bc)t^{n-1}}{(ct^n-a)^2} \ dt$$

In this way the rationalisation is complete.

- - -

A frequent case occurs for $c=0$ and $d=1,$ when a simple first-degree binomial appears under the radical:

$$\int R\big(x,\sqrt[n]{ax+b}\big) \ dx \qquad t=\sqrt[n]{ax+b}$$

Here the inverse substitution is $x=(t^n-b)/a$ and the differential is $dx=(n/a)t^{n-1} \ dt.$

When the same binomial appears under radicals of different indices, a single substitution rationalises all of them, provided the chosen exponent is divisible by each index. The general form with several radicals is the following:

$$\int R\big(x,\sqrt[n_1]{ax+b},\dots,\sqrt[n_j]{ax+b}\big) \ dx$$

Here we set $t^m=ax+b$ with $m$ equal to the least common multiple of $n_1,\dots,n_j.$ If $m$ is even, we choose $t\geq0.$ Every root then becomes an integer power of $t,$ because $\sqrt[n_i]{ax+b}=t^{m/n_i}$ and the exponent $m/n_i$ is an integer by the way $m$ was chosen.

To make the criterion more concrete, let us apply it to the following integral:

$$\int\frac{dx}{\sqrt x+\sqrt[3]x}$$

In this example the indices of the radicals are $2$ and $3$ respectively, and their least common multiple is $6.$ Setting $x=t^6$ with $t>0$, we get $dx=6t^5 \ dt,$ $\sqrt x=t^3$ and $\sqrt[3]x=t^2.$ A short calculation gives:

$$\int\frac{6t^5}{t^3+t^2} \ dt=6\int\frac{t^3}{t+1} \ dt$$

The numerator now has higher degree than the denominator, so we can apply [polynomial division](../polynomial-division/), which gives:

$$\frac{t^3}{t+1}=t^2-t+1-\frac{1}{t+1}$$

The integral is elementary and we can proceed term by term:

$$6\left(\frac{t^3}{3}-\frac{t^2}{2}+t-\ln|t+1|\right)=2t^3-3t^2+6t-6\ln(t+1)$$

Since $t > 0$ we can drop the absolute value inside the logarithm. Returning now to the original variable, $t=\sqrt[6]x,$ hence $t^3=\sqrt x$ and $t^2=\sqrt[3]x$. The integral we started from is therefore:

$$\int\frac{dx}{\sqrt x+\sqrt[3]x}=2\sqrt x-3\sqrt[3]x+6\sqrt[6]x-6\ln\big(\sqrt[6]x+1\big)+k$$

- - -

Let us take a second example and evaluate the following integral:

$$\int\sqrt{\frac{x}{1-x}} \ dx \qquad 0\leq x<1$$

The coefficients are $a=1,$ $b=0,$ $c=-1,$ $d=1,$ so $ad-bc=1$ and the substitution must be applied. We set $t=\sqrt{x/(1-x)},$ from which $t^2(1-x)=x,$ and we obtain:

$$x=\frac{t^2}{1+t^2} \qquad dx=\frac{2t}{(1+t^2)^2} \ dt$$

At this point the integrand becomes a rational function:

$$\int t\cdot\frac{2t}{(1+t^2)^2} \ dt=2\int\frac{t^2}{(1+t^2)^2} \ dt$$

A short digression: bear in mind that, in a great many contexts, adding and subtracting the same quantity within an expression you seem to be stuck on can turn the situation around. A classic trick, which students either do not know or struggle to handle because standard mathematics courses treat it as an almost superfluous embellishment, is to add and subtract $1.$ In our example, writing $t^2=(1+t^2)-1$ splits the quotient into the difference between $1/(1+t^2)$ and $1/(1+t^2)^2.$ The second term reduces to the case $n=2$ of the [reduction formula](../reduction-formulas/) for powers of a quadratic denominator, and we obtain:

$$\int\frac{dt}{(1+t^2)^2}=\frac{t}{2(1+t^2)}+\frac{1}{2}\arctan t$$

To return now to the original variable, observe that $1+t^2=1/(1-x),$ hence $t/(1+t^2)=t(1-x)=\sqrt{x(1-x)}.$ The result is:

$$\int\sqrt{\frac{x}{1-x}} \ dx=\arctan\sqrt{\frac{x}{1-x}}-\sqrt{x(1-x)}+k$$

## The square root of a quadratic trinomial

We now turn to the most frequent family of integrals, the one in which a second-degree polynomial appears under the radical:

$$\int R\big(x,\sqrt{ax^2+bx+c}\big) \ dx$$

We must impose the conditions $a\neq0$ and $b^2-4ac\neq0$ to exclude a degenerate case. The first tool to use here is [completing the square](../completing-the-square/), which brings the trinomial back to one of the three canonical forms treated on the page about [trigonometric substitution](../trigonometric-substitution-for-integrals/). It is better, though, to record first the two elementary antiderivatives that occur in almost every computation of this family. Write $Q(x)=ax^2+bx+c$ and $D=b^2-4ac,$ and observe that multiplying $Q$ by $4a$ and completing the square gives the identity:

$$4aQ(x)=(2ax+b)^2-D$$

This relation suggests a linear substitution $w=2ax+b,$ with $dw=2a \ dx$. For $a>0$ the identity gives $\sqrt{Q(x)}=\sqrt{w^2-D}/(2\sqrt a),$ and the integral reduces to the antiderivative of $1/\sqrt{w^2-D}:$

$$\int\frac{dx}{\sqrt{ax^2+bx+c}}=\frac{1}{\sqrt a}\ln\left|2ax+b+2\sqrt a\sqrt{ax^2+bx+c}\right|+k$$

For $a<0$ the radicand is positive only on a bounded interval, and this forces the [discriminant](../trinomials/) to be positive. The identity now gives $\sqrt{Q(x)}=\sqrt{D-w^2}/(2\sqrt{-a}),$ and the integral reduces to the [arcsine](../arcsine-function/) antiderivative:

$$\int\frac{dx}{\sqrt{ax^2+bx+c}}=-\frac{1}{\sqrt{-a}}\arcsin\frac{2ax+b}{\sqrt{b^2-4ac}}+k$$

Since $Q'(x)=2ax+b,$ every binomial $mx+n$ decomposes as a linear combination of the derivative of the trinomial and the constant $1$:

$$mx+n=\frac{m}{2a}(2ax+b)+\left(n-\frac{mb}{2a}\right)$$

The first summand produces an immediate integral, because its numerator is exactly the derivative of the radicand and the antiderivative of $Q'/\sqrt Q$ is $2\sqrt Q.$ The second one leads back to the two formulas just written, so:

$$\int\frac{mx+n}{\sqrt{ax^2+bx+c}} \ dx=\frac{m}{a}\sqrt{ax^2+bx+c}+\left(n-\frac{mb}{2a}\right)\int\frac{dx}{\sqrt{ax^2+bx+c}}$$

## The Euler substitutions

Things do not always run smoothly, however. Completing the square settles only the cases where the radical appears on its own in the numerator or in the denominator. When $R$ instead combines $x$ and the radical into an arbitrary fraction, the trigonometric route leads to the integral of a rational function of sine and cosine, which in turn calls for the [Weierstrass substitution](../the-weierstrass-substitution/).

In these cases the Euler substitutions come into play, and they rationalise the integrand directly, without going through trigonometric functions.

The first substitution requires $a>0$ and sets:

$$\sqrt{ax^2+bx+c}=t-x\sqrt a$$

Squaring both sides cancels the term $ax^2$ and leaves $bx+c=t^2-2\sqrt atx.$ From here $x$ is obtained as a rational function of $t$:

$$x=\frac{t^2-c}{2\sqrt at+b}$$

Differentiating the quotient gives the differential, and carrying the expression of $x$ back into the substitution gives the radical:

$$dx=\frac{2\big(\sqrt at^2+bt+\sqrt ac\big)}{(2\sqrt at+b)^2} 
\ dt$$

$$\sqrt{ax^2+bx+c}=\frac{\sqrt at^2+bt+\sqrt ac}{2\sqrt at+b}$$

- - -

The second substitution requires $c>0$ and sets:

$$\sqrt{ax^2+bx+c}=xt+\sqrt c$$

Squaring cancels the constant term and leaves $ax^2+bx=x^2t^2+2\sqrt cxt.$ Factoring out $x$ yields the solution $x=0,$ which does not determine the change of variables. On an interval where $x\neq0,$ we divide by $x$ and obtain a first-degree equation, hence:

$$x=\frac{2\sqrt ct-b}{a-t^2}$$

- - -

The third substitution requires the trinomial to have two distinct real [roots](../roots-of-a-polynomial/) $\alpha$ and $\beta,$ that is $b^2-4ac>0.$ In that case the factorisation holds:

$$ax^2+bx+c=a(x-\alpha)(x-\beta)$$

We then set:

$$\sqrt{ax^2+bx+c}=t(x-\alpha)$$

Squaring everything and dividing by the common factor $x-\alpha$ we obtain:

$$x=\frac{a\beta-\alpha t^2}{a-t^2}$$

It is useful to know that the three substitutions overlap in the cases they cover. When $a>0$ the first one applies. When $a<0$ the radicand is positive only on a bounded interval and the discriminant is therefore positive, which makes the third one applicable. The first and the third are enough to cover every trinomial whose radicand is not negative everywhere, while the second is a shortcut worth taking when $c>0,$ because it shortens the computations appreciably.

- - -

To clarify with a worked example what we have described so far, let us evaluate the following integral by this method:

$$\int\frac{dx}{x\sqrt{x^2+x+1}}$$

The trinomial has $a=1$ and $c=1,$ so we can use either the first or the second substitution (since the discriminant equals $-3,$ we can rule out the third). We choose the second and set:

$$\sqrt{x^2+x+1}=xt+1$$

Squaring and cancelling the constant term leaves $x^2+x=x^2t^2+2xt.$ Dividing by $x$ we get $x+1=xt^2+2t,$ and therefore:

$$x=\frac{2t-1}{1-t^2}$$

From this expression we obtain the differential and the radical as rational functions of $t$:

$$dx=\frac{2\big(t^2-t+1\big)}{(1-t^2)^2} \ dt$$

$$\sqrt{x^2+x+1}=xt+1=\frac{t^2-t+1}{1-t^2}$$

Substituting the three factors into the integrand and carrying out the computation we obtain:

$$
\begin{align}
\int\frac{dx}{x\sqrt{x^2+x+1}} &= \int\frac{1-t^2}{2t-1}\cdot\frac{1-t^2}{t^2-t+1}\cdot\frac{2\big(t^2-t+1\big)}{(1-t^2)^2} \ dt \\[6pt]
&= \int\frac{2}{2t-1} \ dt
\end{align}
$$

The final integral equals $\ln|2t-1|.$ From the substitution we then get $t=\big(\sqrt{x^2+x+1}-1\big)/x,$ hence $2t-1=\big(2\sqrt{x^2+x+1}-x-2\big)/x,$ and the antiderivative is:

$$\int\frac{dx}{x\sqrt{x^2+x+1}}=\ln\left|\frac{2\sqrt{x^2+x+1}-x-2}{x}\right|+k$$

> Take it on trust that this procedure is far more efficient than trigonometric substitution, which in some cases can complicate the original integral considerably, making the computations much longer or even barely practicable. The advice is therefore to learn to handle these methods with some confidence, because the practical cases they apply to are rather frequent, so they can prove very useful, if not decisive, for solving integrals that look quite laborious at first sight.

## Polynomial numerator and undetermined coefficients

Let us examine at this point a further case, the one where the radical appears only in the denominator and the numerator is a polynomial. The good news is that a method exists which avoids substitutions altogether. Let $P_n$ denote a polynomial of degree $n$ and, as above, let $Q(x)=ax^2+bx+c$ be the trinomial under the radical. We look for an antiderivative of the following form:

$$\int\frac{P_n(x)}{\sqrt{Q(x)}} \ dx=S_{n-1}(x)\sqrt{Q(x)}+\lambda\int\frac{dx}{\sqrt{Q(x)}}$$

$S_{n-1}$ is a polynomial of degree $n-1$ with unknown coefficients and $\lambda$ is a constant. The integral on the right is one of the two antiderivatives obtained above by completing the square, so it is already known. To determine the coefficients we differentiate the equality with respect to $x$ and multiply both sides by $\sqrt Q,$ an operation that removes every radical and leaves an identity between polynomials:

$$P_n(x)=S_{n-1}'(x)Q(x)+\frac{1}{2}S_{n-1}(x)Q'(x)+\lambda$$

The two sides have the same degree $n,$ because $S_{n-1}'$ has degree $n-2$ and $Q$ has degree $2,$ while $S_{n-1}$ has degree $n-1$ and $Q'$ has degree $1.$ Comparing the coefficients produces $n+1$ [linear equations](../systems-of-linear-equations/) in the $n$ unknowns of $S_{n-1}$ and in $\lambda,$ that is in $n+1$ unknowns, and the system is solved in succession starting from the highest degree. Let us see a worked case, which I hope will make the whole thing less murky. We evaluate the following integral:

$$\int\frac{x^2}{\sqrt{x^2+1}} \ dx$$

Here $n=2,$ so $S_1(x)=Ax+B$ and the identity between polynomials becomes:

$$x^2=A\big(x^2+1\big)+\frac{1}{2}(Ax+B)(2x)+\lambda=2Ax^2+Bx+(A+\lambda)$$

Comparing the coefficients gives $A=1/2$ from the quadratic term, $B=0$ from the linear term and $\lambda=-1/2$ from the constant term. The remaining integral is the case $a=1,$ $b=0,$ $c=1$ of the formula for $a>0,$ which reduces to $\ln\big(x+\sqrt{x^2+1}\big)$. The antiderivative is therefore:

$$\int\frac{x^2}{\sqrt{x^2+1}} \ dx=\frac{x}{2}\sqrt{x^2+1}-\frac{1}{2}\ln\big(x+\sqrt{x^2+1}\big)+k$$

## Binomial differentials

The last family of integrals we shall see has a structure different from those seen so far, because the radical applies to a [binomial](../binomials/) in which the variable appears with an arbitrary exponent. A binomial differential is defined as an expression of the form:

$$x^m\big(a+bx^n\big)^p \ dx \qquad a,b\neq0, \quad m,n,p\in\mathbb{Q}, \quad n\neq0$$

The assumption $n\neq0$ excludes the degenerate case $n=0,$ in which the factor $(a+bx^n)^p$ is constant and the integral, when defined, reduces to the integral of a monomial.

Setting $z=x^n,$ from which $dz=nx^{n-1} \ dx,$ the integral is rewritten in a form that brings out the exponents $(m+1)/n-1$ and $p,$ on which the classification below depends:

$$\int x^m\big(a+bx^n\big)^p \ dx=\frac{1}{n}\int z^{\frac{m+1}{n}-1}(a+bz)^p \ dz$$

In the general case the antiderivative is not elementary at all. The result that establishes exactly when it is, due to Chebyshev (but outside our treatment), concerns the following three numbers:

$$p \qquad \frac{m+1}{n} \qquad \frac{m+1}{n}+p$$

Just note that, in these cases, the integral is expressible through elementary functions if and only if at least one of these three numbers is an integer.

+ If $p$ is an integer, the integrand is rational in the powers of $x^{1/s},$ where $s$ is the least common multiple of the denominators of $m$ and $n,$ so we set $x=t^s.$
+ If $(m+1)/n$ is an integer, we set $a+bx^n=t^s,$ where $s$ is the denominator of $p.$
+ If $(m+1)/n+p$ is an integer, we set $ax^{-n}+b=t^s,$ with the same $s.$

- - -

The second case is easy to recognise. Consider for instance:

$$\int\frac{\sqrt[3]{1+\sqrt[4]x}}{\sqrt x} \ dx \qquad x>0$$

Rewritten as a binomial differential it has $m=-1/2,$ $n=1/4$ and $p=1/3.$ The denominator of $p$ equals $3,$ and the substitution is $1+x^{1/4}=t^3,$ from which:

$$x=\big(t^3-1\big)^4$$

$$dx=12t^2\big(t^3-1\big)^3 \ dt$$

$$\sqrt x=\big(t^3-1\big)^2$$

We can rewrite everything as

$$
\begin{align}
\int\frac{t\cdot12t^2\big(t^3-1\big)^3}{\big(t^3-1\big)^2} \ dt &= 12\int\big(t^6-t^3\big) \ dt \\[6pt]
&= \frac{12t^7}{7}-3t^4
\end{align}
$$

Returning to the original variable with $t=\sqrt[3]{1+\sqrt[4]x}$ we obtain:

$$\int\frac{\sqrt[3]{1+\sqrt[4]x}}{\sqrt x} \ dx=\frac{12}{7}\big(1+\sqrt[4]x\big)^{7/3}-3\big(1+\sqrt[4]x\big)^{4/3}+k$$

A little laborious, as you have seen, but feasible.

- - -

The third case is the least immediate to recognise, because the condition involves a sum and not a single exponent. Take for instance:

$$\int\frac{dx}{x^4\sqrt{1+x^2}} \qquad x>0$$

The exponents are $m=-4,$ $n=2$ and $p=-1/2.$ Neither $p$ nor $(m+1)/n=-3/2$ is an integer, while the sum $(m+1)/n+p=-2$ is, so we set $x^{-2}+1=t^2$ with $t>1.$ From this relation $x^2=1/(t^2-1),$ and differentiating we obtain:

$$dx=-t\big(t^2-1\big)^{-3/2} \ dt$$

$$\sqrt{1+x^2}=\frac{t}{\sqrt{t^2-1}}$$

Simplifying the powers of $t^2-1,$ the integrand reduces once again to a polynomial, and therefore:

$$
\begin{align}
\int\frac{dx}{x^4\sqrt{1+x^2}} &= \int\big(t^2-1\big)^2\cdot\frac{\sqrt{t^2-1}}{t}\cdot\Big({-t}\big(t^2-1\big)^{-3/2}\Big) \ dt \\[6pt]
&= -\int\big(t^2-1\big) \ dt \\[6pt]
&= t-\frac{t^3}{3}
\end{align}
$$

Returning to the original substitution, with $t=\sqrt{1+x^2}/x$ and collecting the radical as a common factor, we obtain:

$$\int\frac{dx}{x^4\sqrt{1+x^2}}=\frac{\big(2x^2-1\big)\sqrt{1+x^2}}{3x^3}+k$$

## Remarks on the choice of the substitution

We can summarise the choice of the criterion to use in the following points.

+ For roots of a first-degree binomial, including roots of different indices, set $t^m=ax+b$ with $m$ the least common multiple of the indices.
+ For the root of a ratio of two first-degree binomials, set $t$ equal to the radical, after checking that $ad-bc\neq0.$
+ For the square root of a quadratic trinomial appearing on its own, complete the square and apply the trigonometric substitution, or use the two direct formulas obtained above.
+ For the root of a trinomial inside an arbitrary rational expression, choose among the three Euler substitutions according to the sign of $a,$ the sign of $c$ and the discriminant.
+ For a polynomial divided by the square root of a trinomial, apply the method of undetermined coefficients.
+ For a power of $x$ multiplied by a power of a binomial in $x^n,$ check Chebyshev's criterion and choose among the three corresponding substitutions.

An integral can fall under more than one entry of the list, and in that case the decision is best made on the length of the computations that each route involves. This is of course not immediate beforehand, but with a little experience it becomes reasonably easy to see which substitution is preferable.

> Outside these families an elementary antiderivative does not exist in general. If $P$ is a polynomial of degree $3$ or $4$ with no multiple roots, the integral $\int \frac{dx}{\sqrt{P(x)}}$ is an elliptic integral. The mere presence of $\sqrt{P(x)}$ in the integrand is not enough to rule out an elementary antiderivative, because multiple roots or particular numerators can reduce the integral to elementary forms. Elliptic integrals appear, for example, in computing the [length](../arc-length-of-a-curve/) of an arc of an ellipse, and they are studied as special functions.
