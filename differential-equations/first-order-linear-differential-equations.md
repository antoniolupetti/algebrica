---
title: First-Order Linear Differential Equations
source: https://algebrica.org/first-order-linear-differential-equations/
license: CC BY-NC 4.0
tags:
  - differential-equations
  - first-order-differential-equations
  - initial-value-problem
  - integrating-factor
  - linear-differential-equations
  - ordinary-differential-equations
  - separable-differential-equations
---
## Standard form

A [first-order differential equation](../first-order-differential-equations/) is linear when the unknown function and its derivative occur only to the first power, are not multiplied together, and are not arguments of a nonlinear function. It is a [linear differential equation](../linear-differential-equations/) of order one. Its standard form is:

$$y'+p(x)y=q(x)$$

The coefficient $p$ and the right-hand side $q$ depend on the independent variable alone. The equation is homogeneous when $q$ vanishes throughout the interval and nonhomogeneous otherwise.

+ $y'+3y=e^x$ is linear, with $p(x)=3$ and $q(x)=e^x.$
+ $y'+\frac{y}{x}=\ln(x)$ is linear on every interval contained in $(0,\infty).$
+ $y'+y^2=x$ is not linear, because the unknown function is squared.
+ $yy'=x$ is not linear, because the unknown function multiplies its derivative.
+ $y'+\sin(y)=0$ is not linear, because $y$ is the argument of the sine.

On an interval where $a_1(x)\neq0,$ we may divide an equation written as $a_1(x)y'+a_0(x)y=g(x)$ by $a_1(x)$ and write it in standard form. The method therefore applies on an interval where the leading coefficient does not vanish.

Linearity is a condition on how the unknown function enters the equation. The functions $p$ and $q$ may be nonlinear functions of $x.$ The equation $y'+e^{x^2}y=\tan(x)$ is linear, while $y'=y^2$ is not.

## The integrating factor

After we multiply the standard form by a function $\mu(x),$ the equation is:

$$\mu(x)y'+\mu(x)p(x)y=\mu(x)q(x)$$

The [product rule](../differentiation-rules/) gives $(\mu y)'=\mu y'+\mu'y.$ The left-hand side above is therefore the derivative of the product $\mu y$ exactly when:

$$\mu'(x)=p(x)\mu(x)$$

A single such function is sufficient. Suppose that $p$ is [continuous](../continuous-functions/) on an [interval](../intervals/) $I.$ An antiderivative $P$ of $p$ exists on $I$ by the [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/). The [chain rule](../chain-rule/) gives:

$$\left(e^{P(x)}\right)'=P'(x)e^{P(x)}=p(x)e^{P(x)}$$

Thus $\mu(x)=e^{P(x)}$ is an [integrating factor](../integrating-factors/) of the equation. The usual notation is:

$$\mu(x)=e^{\int p(x) \ dx}$$

Here and below, an indefinite integral without an added constant denotes one fixed antiderivative. Two antiderivatives of $p$ on $I$ differ by a constant $k,$ so the corresponding factors differ by the nonzero constant $e^k.$ The solution set is the same for either factor. Since the exponential is positive on $I,$ we may divide by $\mu(x)$ throughout the interval.

## The general solution

With $\mu(x)=e^{P(x)},$ the equation is:

$$\left(\mu(x)y\right)'=\mu(x)q(x)$$

If $q$ is continuous on $I,$ the right-hand side is continuous. After [integrating](../indefinite-integrals/) both sides, we have:

$$\mu(x)y=\int\mu(x)q(x) \ dx+C$$

Since $\mu(x)>0$ on $I,$ the general solution is:

$$y(x)=e^{-P(x)}\left(\int e^{P(x)}q(x) \ dx+C\right)$$

Every transformation is reversible, so this family is exactly the set of solutions on $I.$ No solution is lost, because the only division is by the positive function $\mu.$ By contrast, [separation of variables](../separable-differential-equations/) can lose constant solutions when it requires division by a factor depending on $y.$

The calculation has four steps.

+ Choose an interval on which the leading coefficient does not vanish and the functions $p$ and $q$ obtained after division are continuous, then write the equation in the form $y'+p(x)y=q(x).$
+ Choose an antiderivative $P$ of $p$ and set $\mu(x)=e^{P(x)}.$
+ Multiply the equation by $\mu$ to obtain $(\mu y)'=\mu q.$
+ Integrate and divide by the positive function $\mu.$

Consider the equation below on the interval $\left(-\frac{\pi}{2},\frac{\pi}{2}\right).$

$$y'+\tan(x)y=\cos(x)$$

The [tangent](../tangent-function/) is continuous there. Since the cosine is positive on the interval, the function $P(x)=-\ln\left(\cos(x)\right)$ is an antiderivative of the tangent. The integrating factor is:

$$\mu(x)=e^{-\ln(\cos(x))}=\frac{1}{\cos(x)}$$

When we multiply by $1/\cos(x),$ the right-hand side is $1$ and the equation is:

$$\left(\frac{y}{\cos(x)}\right)'=1$$

We integrate and then multiply by $\cos(x).$ The two equations are:

$$
\begin{align}
\frac{y}{\cos(x)}&=x+C \\[6pt]
y(x)&=(x+C)\cos(x)
\end{align}
$$

The derivative is $y'(x)=\cos(x)-(x+C)\sin(x),$ and the terms containing $x+C$ cancel, so $y'+\tan(x)y=\cos(x).$ For each value of $C,$ the function is a solution on the whole interval. The coefficient $\tan(x)$ is undefined at $x=\pm\pi/2,$ so the equation is not defined at either endpoint.

## Structure of the solution set

The homogeneous equation associated with $y'+p(x)y=q(x)$ is:

$$y'+p(x)y=0$$

After we multiply by $\mu=e^P,$ the homogeneous equation is $\left(e^{P(x)}y\right)'=0.$ Hence $e^{P(x)}y$ is constant on $I,$ so the homogeneous solutions are:

$$y(x)=Ce^{-P(x)}$$

The homogeneous solutions on $I$ are the multiples of the single function $e^{-P},$ which never vanishes. They form a [vector space](../vector-spaces/) of dimension one.

Suppose now that $y_1$ and $y_2$ both solve the nonhomogeneous equation. The difference between the two equations is:

$$(y_1-y_2)'+p(x)(y_1-y_2)=0$$

Their difference solves the homogeneous equation. Conversely, the sum of a nonhomogeneous solution and a homogeneous solution is another solution of the nonhomogeneous equation. If $y_p$ is one fixed solution, the solution set on $I$ is therefore:

$$\{\ y_p+Ce^{-P(x)} \mid C\in\mathbb{R} \ \}$$

The solution set is a translate of the one-dimensional homogeneous solution space and is therefore an affine line in the space of differentiable functions on $I.$ If $Q$ is a fixed antiderivative of $e^Pq,$ then $e^{-P}Q$ is one particular solution and $Ce^{-P}$ is the general homogeneous solution.

Consider the equation:

$$y'+y=x$$

The integrating factor is $\mu(x)=e^x,$ so $\left(e^xy\right)'=xe^x.$ By [integration by parts](../integration-by-parts/), the function $(x-1)e^x$ is an antiderivative of $xe^x.$ Hence the general solution is:

$$y(x)=x-1+Ce^{-x}$$

The function $y_p(x)=x-1$ solves the equation, and $Ce^{-x}$ is the general solution of $y'+y=0.$ The solution set is unchanged if $y_p$ is replaced by another particular solution, such as $x-1+e^{-x},$ because $x-1+e^{-x}+Ce^{-x}=x-1+(C+1)e^{-x}.$

- - -

Linearity also relates solutions with different right-hand sides. Suppose that $y_1$ solves $y'+p(x)y=q_1(x)$ and $y_2$ solves $y'+p(x)y=q_2(x).$ For any constants $c_1$ and $c_2,$ the following identity holds:

$$(c_1y_1+c_2y_2)'+p(x)(c_1y_1+c_2y_2)=c_1q_1(x)+c_2q_2(x)$$

If the right-hand side is a sum, we may add one solution for each term. For example, the constant function $y_1=1$ solves $y'+y=1,$ while $y_2=x-1$ solves $y'+y=x.$ Their sum $y_1+y_2=x$ solves $y'+y=x+1.$

## Initial-value problems

Suppose that $p$ and $q$ are continuous on an interval $I,$ and let $x_0\in I.$ The [initial-value problem](../initial-value-problems/) is:

$$y'+p(x)y=q(x) \qquad y(x_0)=y_0$$

Choose the antiderivative that vanishes at the initial point:

$$P(x)=\int_{x_0}^{x}p(t) \ dt$$

Since $P(x_0)=0,$ we integrate $\left(e^Py\right)'=e^Pq$ from $x_0$ to $x.$ The resulting equality is:

$$e^{P(x)}y(x)-y_0=\int_{x_0}^{x}e^{P(t)}q(t) \ dt$$

After we divide by $e^{P(x)},$ the [definite-integral](../definite-integrals/) formula is:

$$y(x)=e^{-P(x)}\left(y_0+\int_{x_0}^{x}e^{P(t)}q(t) \ dt\right)$$

The integrand $e^{P(t)}q(t)$ is continuous on $I,$ so the formula defines a differentiable function on the whole interval. This function satisfies both the equation and the initial condition, and the derivation shows that every solution must have this form. The problem therefore has a unique solution on $I.$

This result guarantees existence and uniqueness on the largest interval containing $x_0$ on which $p$ and $q$ are continuous. If either function is not continuous at an endpoint, the theorem does not determine whether a solution continues through that point. The original equation must then be examined directly.

A [nonlinear first-order equation](../first-order-differential-equations/) can have finite-time blow-up even when its right-hand side is smooth on the whole plane. The problem $y'=y^2,$ $y(0)=1,$ has the solution $y=1/(1-x),$ which becomes unbounded as $x\to1^-.$

The definite-integral formula is also valid when the integrand has no elementary antiderivative. Consider the problem:

$$y'+2xy=1 \qquad y(0)=0$$

Here $P(x)=\int_0^x2t \ dt=x^2,$ so the solution is:

$$y(x)=e^{-x^2}\int_{0}^{x}e^{t^2} \ dt$$

The product rule and the Fundamental Theorem of Calculus give $y'(x)=-2xy(x)+1,$ and the integral vanishes at $x=0.$ The function $e^{t^2}$ has no elementary antiderivative, but the integral above is an exact representation of the solution for every real $x.$

- - -

The functions $p$ and $q$ in standard form must satisfy the continuity hypotheses. When the leading coefficient of the original equation vanishes, the equation cannot be put in standard form at that point and must be examined directly. Consider:

$$xy'-2y=x^4$$

On an interval that does not contain $0,$ the standard form is $y'-\frac{2}{x}y=x^3,$ and its integrating factor is $x^{-2}.$ Since $\left(x^{-2}y\right)'=x,$ the solutions on that interval are:

$$y(x)=\frac{x^4}{2}+Cx^2$$

At $x=0$ the original equation is $-2y(0)=0,$ so no solution defined near the origin can have $y(0)\neq0.$ In particular, the initial-value problem with $y(0)=1$ has no solution.

The initial-value problem with $y(0)=0$ has solutions, but they are not unique. Choose two constants $C_+$ and $C_-,$ and define:

$$
y(x)=
\begin{cases}
\dfrac{x^4}{2}+C_+x^2 & x\geq0 \\[6pt]
\dfrac{x^4}{2}+C_-x^2 & x<0
\end{cases}
$$

Both formulas have value and derivative equal to $0$ at the origin, so the two pieces form a differentiable function on $\mathbb{R}.$ They satisfy the equation away from the origin, and both sides of the equation are $0$ at the origin. For every pair $(C_+,C_-),$ the piecewise function is therefore a solution, so the initial-value problem has infinitely many solutions. The standard theorem applies where the leading coefficient does not vanish and the functions $p$ and $q$ in standard form are continuous. At a zero of the leading coefficient, existence and uniqueness must be studied separately.

## A circuit with an alternating source

A series circuit has a resistor with resistance $R>0,$ an inductor with inductance $L>0,$ and a voltage source $E(t).$ If $i(t)$ is the current, Kirchhoff's voltage law states that the source voltage is the sum of the voltage drops $Ri$ and $Li'.$ The circuit equation is:

$$Li'+Ri=E(t)$$

When we divide by $L,$ the equation is in standard form with the constant coefficient $R/L,$ and its integrating factor is $e^{Rt/L}.$ Suppose that the source is $E(t)=E_0\sin(\omega t),$ where $E_0>0$ is the voltage amplitude and $\omega>0$ is the angular frequency. When we multiply by the integrating factor, the equation is:

$$\left(e^{Rt/L}i\right)'=\frac{E_0}{L}e^{Rt/L}\sin(\omega t)$$

Set $a=R/L,$ and let $I$ and $J$ be antiderivatives of $e^{at}\sin(\omega t)$ and $e^{at}\cos(\omega t),$ respectively. For the first [integration by parts](../integration-by-parts/), the choices are $u=\sin(\omega t)$ and $dv=e^{at} \ dt.$ For the second, the choices are $u=\cos(\omega t)$ and the same $dv.$ The two identities are:

$$
\begin{align}
I&=\frac{e^{at}\sin(\omega t)}{a}-\frac{\omega}{a}J+C_1 \\[6pt]
J&=\frac{e^{at}\cos(\omega t)}{a}+\frac{\omega}{a}I+C_2
\end{align}
$$

Substitute the second identity into the first and collect the terms containing $I.$ Since $C_1$ and $C_2$ are arbitrary, their resulting linear combination is another arbitrary constant $C.$ Hence the antiderivative $I$ is:

$$I=\frac{e^{at}\left(a\sin(\omega t)-\omega\cos(\omega t)\right)}{a^2+\omega^2}+C$$

After we replace $a$ by $R/L,$ substitute the antiderivative into the differential equation, divide by $e^{Rt/L},$ and rename the arbitrary constant, the general solution is:

$$i(t)=\frac{E_0\left(R\sin(\omega t)-\omega L\cos(\omega t)\right)}{R^2+\omega^2L^2}+Ce^{-Rt/L}$$

The first term is a periodic particular solution, and $Ce^{-Rt/L}$ is the general solution of the homogeneous equation $Li'+Ri=0.$ The initial current affects only the constant $C.$ Since $R/L>0,$ the homogeneous term tends to $0$ as $t\to+\infty.$ For example, if $i(0)=0,$ then the constant is:

$$C=\frac{E_0\omega L}{R^2+\omega^2L^2}$$

The phase angle $\varphi$ is defined by:

$$\varphi=\arctan\left(\frac{\omega L}{R}\right)$$

Since $R,$ $L,$ and $\omega$ are positive, the angle is in $(0,\pi/2).$ It satisfies $\cos(\varphi)=R/\sqrt{R^2+\omega^2L^2}$ and $\sin(\varphi)=\omega L/\sqrt{R^2+\omega^2L^2}.$ Therefore the periodic term is:

$$\frac{E_0}{\sqrt{R^2+\omega^2L^2}}\sin(\omega t-\varphi)$$

The complex impedance is $Z=R+j\omega L,$ where $j^2=-1.$ Its modulus is $\lvert Z\rvert=\sqrt{R^2+\omega^2L^2}.$ Thus the periodic current has amplitude $E_0/\lvert Z\rvert$ and lags the voltage by the angle $\varphi.$ The ratio $\tau=L/R$ is the decay time constant, since the homogeneous factor is $e^{-t/\tau}$ and has the value $e^{-1}$ after one time constant.

## Equations linear in the other variable

An equation that is not linear in $y$ may be linear after the roles of the two variables are exchanged. The method is local because passing from $y(x)$ to $x(y),$ and then back, requires the relevant derivative to be nonzero. Consider:

$$y'=\frac{1}{x+y^2}$$

The unknown function is squared, so the equation is not linear in $y.$ On every solution interval, the denominator is nonzero and continuous. Hence $y'$ is continuous and never vanishes, so it has a constant sign. The solution is strictly [monotone](../increasing-and-decreasing-functions/) and has a differentiable [inverse function](../inverse-function/). The derivative of the inverse is:

$$\frac{dx}{dy}=\frac{1}{y'}=x+y^2$$

As an equation for $x$ as a function of $y,$ this equation is linear, with coefficient $-1$ and right-hand side $y^2.$ Its integrating factor is $\mu(y)=e^{-y},$ so the transformed equation is:

$$\frac{d}{dy}\left(e^{-y}x\right)=y^2e^{-y}$$

We apply [integration by parts](../integration-by-parts/) twice. The function $-\left(y^2+2y+2\right)e^{-y}$ is an antiderivative of $y^2e^{-y},$ so the solution for $x$ is:

$$x(y)=-\left(y^2+2y+2\right)+Ce^y$$

For a fixed $C,$ let $J$ be an interval of $y$-values on which:

$$\frac{dx}{dy}=Ce^y-2y-2\neq0$$

On $J,$ the function $x(y)$ has a differentiable inverse $y(x),$ and that inverse is a solution of the original equation. Zeros of $Ce^y-2y-2$ separate distinct branches, because the original right-hand side is undefined there.

For $C=0,$ the relation is $x=-(y+1)^2-1,$ and it has the two elementary inverse branches:

$$y(x)=-1\pm\sqrt{-x-1} \qquad x<-1$$

The plus sign corresponds to $y>-1,$ and the minus sign corresponds to $y<-1.$ The point $x=-1$ is excluded because the denominator of the original equation is $0$ there.

For a general value of $C,$ the inverse need not be an elementary function. In that case, the relation $x=x(y)$ is an exact representation of each solution branch.

> A [Bernoulli equation](../bernoulli-differential-equation/) reduces to a first-order linear equation after a power substitution on an interval where that substitution is defined. Any solution excluded by the substitution must be checked in the original equation.
