---
title: First-Order Differential Equations
source: https://algebrica.org/first-order-differential-equations/
license: CC BY-NC 4.0
tags:
  - autonomous-differential-equations
  - bernoulli-differential-equation
  - differential-equations
  - exact-differential-equations
  - first-order-differential-equations
  - homogeneous-differential-equations
  - initial-value-problem
  - integrating-factor
  - linear-differential-equations
  - ordinary-differential-equations
  - separable-differential-equations
---
## First-order equations

A scalar [ordinary differential equation](../differential-equations/) has order one when the first [derivative](../derivatives/) $y'$ is present and all [higher-order derivatives](../higher-order-derivatives/) are absent. Its implicit form is:

$$F(x,y,y')=0$$

The variable $x$ is independent, and $y=y(x)$ is the unknown function. If the equation can be solved for $y',$ it has the normal form:

$$y'=f(x,y)$$

In normal form, $f(x,y)$ is the slope at the point $(x,y).$ A solution is a differentiable function whose graph has this slope at every point. An implicit equation need not have a single normal form. One example is:

$$(y')^2+y^2=1$$

Wherever $|y|<1,$ its two normal forms are:

$$y'=\pm\sqrt{1-y^2}$$

The two possible slopes are $\sqrt{1-y^2}$ and $-\sqrt{1-y^2}.$ At $|y|=1,$ the only possible derivative is zero, while no real slope satisfies the equation when $|y|>1.$

## Solutions and maximal intervals

A solution of $y'=f(x,y)$ on an [interval](../intervals/) $I$ is a differentiable function $y:I\to\mathbb{R}$ such that:

$$y'(x)=f(x,y(x)) \qquad \forall x\in I$$

The [domain](../determining-the-domain-of-a-function/) is part of the solution. A formula may satisfy the equation wherever it is defined and still fail to extend across a point where the formula or the equation is undefined.

The equation below has solutions whose maximal intervals end at a finite point:

$$y'=y^2$$

On an interval where $y\neq0,$ the equation is [separable](../separable-differential-equations/). Separation of variables places the factors depending on $y$ on one side and those depending on $x$ on the other. Here we divide by $y^2$ and have:

$$\frac{1}{y^2} \ dy=1 \ dx$$

After we [integrate](../indefinite-integrals/) both sides, we have:

$$
\begin{align}
\int y^{-2} \ dy&=\int 1 \ dx \\[6pt]
-\frac{1}{y}&=x+C_0 \\[6pt]
y&=\frac{1}{C-x}
\end{align}
$$

For each $C\in\mathbb{R},$ the two maximal solution intervals are $(-\infty,C)$ and $(C,+\infty).$ The solution cannot be extended through $x=C$ because its values are unbounded there. Division by $y^2$ excluded the constant solution $y=0,$ whose maximal interval is $\mathbb{R}.$

> The zeros of an expression containing the unknown function must be checked before division. Division may remove valid solutions. Conversely, an operation such as squaring may add candidates, so every candidate must be substituted into the original equation.

A nonconstant particular solution has a fixed value of $C$ and one of the two maximal intervals above. A formula without its interval is therefore incomplete.

## Initial-value problems

An [initial-value problem](../initial-value-problems/) has a differential equation and the value of the unknown function at one point:

$$y'=f(x,y) \qquad y(x_0)=y_0$$

Geometrically, the solution graph passes through $(x_0,y_0)$ and has the slope prescribed by $f$ at every point. Often, exactly one value of the arbitrary constant is compatible with the initial condition, but this depends on the equation. Some initial-value problems have no solution, some have one, and some have several.

The initial-value problem below is separable:

$$y'=\frac{x}{y} \qquad y(0)=2$$

The equation is defined only where $y\neq0,$ so we may multiply by $y$ without changing its solutions. The separated equation is:

$$y \ dy=x \ dx$$

After we integrate, we have:

$$
\begin{align}
\int y \ dy&=\int x \ dx \\[6pt]
\frac{y^2}{2}&=\frac{x^2}{2}+C \\[6pt]
y^2&=x^2+C_1
\end{align}
$$

The condition $y(0)=2$ implies $C_1=4.$ The equation $y^2=x^2+4$ has two branches:

$$y=\pm\sqrt{x^2+4}$$

Only the positive branch has value $2$ at $x=0,$ so the solution is:

$$y(x)=\sqrt{x^2+4}$$

The expression under the [square root](../radicals/) is positive for every real $x,$ and the solution has domain $\mathbb{R}.$ Its derivative is:

$$y'(x)=\frac{x}{\sqrt{x^2+4}}$$

Since $x/y(x)=x/\sqrt{x^2+4},$ the function satisfies both the differential equation and the initial condition.

## Main classes

Several common forms have standard substitution or integration methods.

+ A [separable equation](../separable-differential-equations/) has the form $y'=g(x)h(y).$ On an interval where $h(y)\neq0,$ we may divide by $h(y)$ and write $\frac{1}{h(y)} \ dy=g(x) \ dx.$ The zeros of $h$ must be checked separately because division may remove constant solutions.

+ A [linear equation](../first-order-linear-differential-equations/) has the form $y'+p(x)y=q(x).$ When we multiply by an integrating factor that depends only on $x,$ the left-hand side is the derivative of a product. A linear equation is homogeneous when $q=0.$

+ An [exact equation](../exact-differential-equations/) has the form $A(x,y) \ dx+B(x,y) \ dy=0.$ Its left-hand side is the differential of a potential function $\Phi(x,y),$ and the solutions satisfy $\Phi(x,y)=C.$ The first step is to calculate this potential function from $A$ and $B.$

+ In a different use of the term, a [homogeneous equation](../homogeneous-differential-equations/) has a right-hand side that depends on $x$ and $y$ only through their quotient. Its normal form is $y'=R(y/x)$ on an interval where $x\neq0,$ and with $v=y/x$ the equation is separable in $v.$

+ An [autonomous equation](../autonomous-differential-equations/) has the form $y'=f(y),$ with no explicit occurrence of $x.$ For every zero $y_*$ of $f,$ the function $y=y_*$ is a constant equilibrium solution. Away from these zeros, the equation is separable.

+ A [Bernoulli equation](../bernoulli-differential-equation/) has the form $y'+a(x)y=b(x)y^m.$ When $m\neq0,1,$ the equation in $z=y^{1-m}$ is linear on an interval where the power is defined and $y\neq0.$

These classes are not disjoint. The equation below is both separable and linear:

$$y'=x(1+y)$$

It is separable because its right-hand side is a product of a function of $x$ and a function of $y.$ It is linear because it can also be written as:

$$y'-xy=x$$

The solution family is the same with either method, provided that the constant solution $y=-1$ excluded by separation is included.

## Linear equations of order one

The linear case has the standard form:

$$y'+p(x)y=q(x)$$

Suppose that $p$ and $q$ are [continuous](../continuous-functions/) on an interval $I.$ Choose a fixed antiderivative $P$ of $p,$ and let $\mu=e^P.$ By the [chain rule](../chain-rule/), we have $\mu'=p\mu.$ After we multiply the standard form by $\mu,$ the [product rule](../differentiation-rules/) shows that the transformed equation is:

$$\left(\mu y\right)'=\mu q$$

If $Q$ is a fixed antiderivative of $\mu q,$ then since $\mu=e^P>0,$ the general solution is:

$$y=e^{-P}(Q+C)$$

For $x_0\in I,$ the condition $y(x_0)=y_0$ determines exactly one value of $C.$

Suppose that a body has temperature $T(t)$ and its surroundings have the constant temperature $T_a.$ Newton's law of cooling assumes that $T'$ is $-k$ times the difference $T-T_a.$ Its linear form is:

$$T'+kT=kT_a \qquad k>0$$

Both $p(t)=k$ and $q(t)=kT_a$ are constant, so the integrating factor is $\mu(t)=e^{kt}.$ After we multiply by this factor, the transformed equation is:

$$\left(e^{kt}T\right)'=kT_ae^{kt}$$

The function $T_ae^{kt}$ is an antiderivative of $kT_ae^{kt},$ so $e^{kt}T=T_ae^{kt}+C.$ Since $e^{kt}>0,$ the temperature is:

$$T(t)=T_a+Ce^{-kt}$$

The constant $C$ is the initial difference $T(0)-T_a,$ and the temperature tends to $T_a$ as $t\to+\infty.$

A complete account of the general method, the structure of the solution set, initial-value problems, singular leading coefficients, and further applications is in [first-order linear differential equations](../first-order-linear-differential-equations/).

## Exact, homogeneous, autonomous, and Bernoulli equations

An [exact differential equation](../exact-differential-equations/) has the form:

$$A(x,y) \ dx+B(x,y) \ dy=0$$

It is exact when a function $\Phi(x,y)$ has [partial derivatives](../partial-derivatives/) $\Phi_x=A$ and $\Phi_y=B.$ The equation is then $d\Phi=0,$ so its solutions have the implicit form:

$$\Phi(x,y)=C$$

Suppose that $A$ and $B$ have continuous first partial derivatives on an open, simply connected region. The equation is exact there precisely when:

$$\frac{\partial A}{\partial y}=\frac{\partial B}{\partial x}$$

Simple connectivity ensures the converse. Without it, a region with a hole can have a differential form that satisfies this equality but has no single-valued potential on the whole region. To calculate $\Phi,$ integrate one coefficient and compare the result with the other.

An equation that fails the test may be exact after we multiply it by a nonzero factor. A function $\mu(x,y)$ for which $\mu A \ dx+\mu B \ dy=0$ is exact is an [integrating factor](../integrating-factors/) of the equation. Write $A_y$ and $B_x$ for the two partial derivatives above. If the integrating factor depends only on $x,$ exactness requires $\mu A_y=\mu'B+\mu B_x.$ On a region where $B\neq0,$ we divide by $\mu B$ and have:

$$\frac{\mu'}{\mu}=\frac{A_y-B_x}{B}$$

Such a factor exists when the right-hand side depends on $x$ alone. Similarly, on a region where $A\neq0,$ a factor that depends only on $y$ must satisfy $\frac{1}{\mu}\frac{d\mu}{dy}=(B_x-A_y)/A.$ It exists when the right-hand side depends on $y$ alone. Consider the equation:

$$\left(3xy+y^2\right) \ dx+\left(x^2+xy\right) \ dy=0$$

The two partial derivatives are $A_y=3x+2y$ and $B_x=2x+y.$ Where $B=x(x+y)\neq0,$ the expression in the integrating-factor criterion is:

$$\frac{A_y-B_x}{B}=\frac{x+y}{x(x+y)}=\frac{1}{x}$$

This calculation suggests $\mu(x)=x.$ On each half-plane $x>0$ or $x<0,$ the factor is nonzero, and direct differentiation verifies exactness even at points where $x+y=0.$ After we multiply by $x,$ the equation is exact and has the potential $\Phi(x,y)=x^3y+\frac{1}{2}x^2y^2.$ Its solutions satisfy $\Phi(x,y)=C.$

On an interval where $x\neq0,$ a [homogeneous equation](../homogeneous-differential-equations/) in the quotient sense has the normal form:

$$y'=R\left(\frac{y}{x}\right)$$

The right-hand side depends on the two variables only through their quotient. If $A$ and $B$ in $A \ dx+B \ dy=0$ are homogeneous functions of the same degree $k,$ then on each region where $x\neq0$ and $B\neq0$ the normal form depends only on $y/x.$ Homogeneity means that $A(\lambda x,\lambda y)=\lambda^kA(x,y)$ and $B(\lambda x,\lambda y)=\lambda^kB(x,y)$ for every $\lambda>0.$ The common factor $\lambda^k$ cancels in the quotient $-A/B.$ With $v=y/x,$ we have $y=vx$ and $y'=v+xv',$ so the transformed equation is:

$$xv'=R(v)-v$$

This equation is separable. For each root $c$ of $R(v)=v,$ the line $y=cx$ is a solution on every interval where $x\neq0.$ These solutions must be recorded before we divide by $R(v)-v.$ Consider the equation:

$$y'=\frac{y}{x}+\frac{y^2}{x^2}$$

With $v=y/x,$ the equation is $xv'=v^2.$ For $v\neq0,$ we separate the variables and integrate. We then have $-1/v=\ln|x|+C.$ Since $v=y/x,$ the nonzero solutions are:

$$y(x)=-\frac{x}{\ln|x|+C}$$

The formula defines a solution on any interval where $x\neq0$ and $\ln|x|+C\neq0.$ The root $v=0,$ excluded by division, corresponds to the solution $y=0.$ Its two maximal intervals are $(-\infty,0)$ and $(0,+\infty).$

An [autonomous equation](../autonomous-differential-equations/) is:

$$y'=f(y)$$

For every zero $y_*$ of $f,$ the function $y=y_*$ is a constant equilibrium solution. These equilibrium solutions must be recorded before we divide by $f(y).$ On an interval where $f(y)\neq0,$ the nonconstant solutions satisfy:

$$\frac{1}{f(y)} \ dy=1 \ dx$$

The sign of $f(y)$ is enough to decide monotonicity. A solution is increasing where $f(y)>0$ and decreasing where $f(y)<0.$

A [Bernoulli equation](../bernoulli-differential-equation/) is:

$$y'+a(x)y=b(x)y^m$$

Assume that $m\neq0,1$ and work on an interval where the power is defined and $y\neq0.$ For the substitution $z=y^{1-m},$ the derivative is:

$$z'=(1-m)y^{-m}y'$$

After we divide the Bernoulli equation by $y^m$ and multiply it by $1-m,$ the equation is linear in $z:$

$$z'+(1-m)a(x)z=(1-m)b(x)$$

Any solution excluded by the condition $y\neq0$ must be checked in the original equation.

## Existence and uniqueness

Consider the initial-value problem:

$$y'=f(x,y) \qquad y(x_0)=y_0$$

The equation and initial value do not by themselves guarantee a solution. If $f$ is continuous on a rectangle about $(x_0,y_0),$ then by Peano's theorem at least one solution exists on an interval about $x_0.$ If, in addition, $f$ is locally Lipschitz with respect to $y,$ exactly one local solution exists. These are the hypotheses of the Picard-Lindelöf theorem.

The local Lipschitz condition means that, on a smaller rectangle, some constant $L>0$ satisfies the following inequality whenever $(x,y_1)$ and $(x,y_2)$ belong to the rectangle:

$$\left|f(x,y_1)-f(x,y_2)\right|\leq L\left|y_1-y_2\right|$$

A continuous partial derivative $\partial f/\partial y$ near the initial point is sufficient for this condition.

A proof of the Picard-Lindelöf theorem begins with the integral form of the problem. After we integrate from $x_0$ to $x$ and use the initial value, the equation is:

$$y(x)=y_0+\int_{x_0}^{x}f\left(t,y(t)\right) \ dt$$

Define the integral operator $T$ by:

$$(T\phi)(x):=y_0+\int_{x_0}^{x}f\left(t,\phi(t)\right) \ dt$$

A continuous function solves the initial-value problem exactly when it is a fixed point of $T.$ Choose a sufficiently short closed interval $J$ about $x_0,$ and let $C(J)$ be the space of continuous real functions on $J,$ with the uniform norm $\|u\|_\infty=\max_{x\in J}|u(x)|.$ Restrict $T$ to the closed subset of functions whose graphs remain in a closed rectangle where $f$ is continuous and has Lipschitz constant $L.$ Continuity on this rectangle makes $f$ bounded, so for a sufficiently short $J$ the operator maps this subset into itself.

If $h=\max_{x\in J}|x-x_0|,$ then for any two functions $\phi$ and $\psi$ in this subset:

$$\|T\phi-T\psi\|_\infty\leq Lh\|\phi-\psi\|_\infty$$

Choose $J$ so that $Lh<1.$ The space $C(J)$ is complete, and the restricted subset is closed, so it is also complete. The Banach fixed-point theorem now implies that $T$ has a unique fixed point. Starting with the constant function $\phi_0(x)=y_0,$ the Picard iterates $\phi_{k+1}=T\phi_k$ converge uniformly to this fixed point, which is the solution of the initial-value problem.

Continuity alone does not imply uniqueness. Consider the problem:

$$y'=3|y|^{2/3} \qquad y(0)=0$$

Two solutions through $(0,0)$ are:

$$y_1(x)=0 \qquad y_2(x)=x^3$$

For $y_2=x^3,$ the derivative is $3x^2,$ and $3|x^3|^{2/3}=3x^2.$ The function $f(y)=3|y|^{2/3}$ is continuous at $y=0,$ but it is not locally Lipschitz there. The two solutions do not contradict the uniqueness theorem because its Lipschitz hypothesis fails.

Local existence and uniqueness do not imply that a solution is defined for every real $x.$ For the equation $y'=y^2$ considered above, the condition $y(0)=1$ implies $C=1.$ The unique local solution is $y=1/(1-x),$ its maximal interval is $(-\infty,1),$ and it becomes unbounded as $x\to1^-.$

By contrast, suppose that $p$ and $q$ in a [first-order linear equation](../first-order-linear-differential-equations/) are continuous on an interval $I,$ with $x_0\in I.$ For every initial value at $x_0,$ the linear problem has a unique solution on all of $I.$

## Reduction of higher-order equations

Some equations of higher order reduce directly to equations of order one. If the unknown function itself does not occur in a second-order equation, its form is:

$$F(x,y',y'')=0$$

With $p=y',$ the first-order equation is $F(x,p,p')=0.$ Once $p$ is known, we integrate $y'=p$ to find $y.$

If the independent variable does not occur, the equation has the form:

$$F(y,y',y'')=0$$

On an interval where $y$ can be used as the independent variable, set $p(y)=y'.$ By the [chain rule](../chain-rule/), we have $y''=p\frac{dp}{dy},$ so the equation is first-order in $p(y).$ For $yy''=(y')^2,$ the transformed equation is:

$$yp\frac{dp}{dy}=p^2$$

On an interval where $p\neq0$ and $y\neq0,$ we divide by $p$ and $y.$ We then have $\frac{dp}{p}=\frac{dy}{y}.$ After integration, $\ln|p|=\ln|y|+C,$ and hence $p=C_1y.$ The remaining equation $y'=C_1y$ has the solutions:

$$y(x)=C_2e^{C_1x}$$

When $p=0,$ the solutions are constant, and the formula contains them when $C_1=0.$

Any equation of order $n$ in normal form can instead be written as a system of $n$ equations of order one. A second-order equation in normal form is:

$$y''=G(x,y,y')$$

Set $y_1=y$ and $y_2=y'.$ The equation is equivalent to the [system of differential equations](../systems-of-differential-equations/):

$$
\begin{align}
y_1'&=y_2 \\[6pt]
y_2'&=G(x,y_1,y_2)
\end{align}
$$

For an equation of order $n,$ set $y_1=y,$ $y_2=y',$ $\ldots,$ and $y_n=y^{(n-1)}.$ The resulting first-order system has $n$ unknown functions. Existence and uniqueness results for first-order systems are therefore also results for higher-order equations.
