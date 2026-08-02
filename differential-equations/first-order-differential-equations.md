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

The signs give the two possible slopes through the same point. At $|y|=1,$ the only possible derivative is zero, while no real slope satisfies the equation when $|y|>1.$

## Solutions and maximal intervals

A solution of $y'=f(x,y)$ on an [interval](../intervals/) $I$ is a differentiable function $y:I\to\mathbb{R}$ such that:

$$y'(x)=f(x,y(x)) \qquad \forall x\in I$$

The [domain](../determining-the-domain-of-a-function/) is part of the solution. A formula may satisfy the equation wherever it is defined and still fail to extend across a point where the formula or the equation is undefined.

The equation below has solutions whose maximal intervals end at a finite point:

$$y'=y^2$$

On an interval where $y\neq0,$ separation gives:

$$\frac{1}{y^2}\frac{dy}{dx}=1$$

[Indefinite integration](../indefinite-integrals/) gives:

$$
\begin{align}
\int y^{-2} \ dy&=\int 1 \ dx \\[6pt]
-\frac{1}{y}&=x+C_0 \\[6pt]
y&=\frac{1}{C-x}
\end{align}
$$

For each $C\in\mathbb{R},$ this formula has two maximal intervals, $(-\infty,C)$ and $(C,+\infty).$ It cannot be extended through $x=C$ because its values are unbounded there. Division by $y^2$ excluded the constant solution $y=0,$ so it must be added to the solution family.

> The zeros of an expression containing the unknown function must be checked before division. Division may remove valid solutions. Conversely, an operation such as squaring may add candidates, so every candidate must be substituted into the original equation.

Each choice of $C$ and one of the two maximal intervals gives a member of the solution family. A particular solution has a fixed value of $C$ and a specified interval. A formula without its interval is therefore incomplete.

## Initial-value problems

An [initial-value problem](../initial-value-problems/) has a differential equation and the value of the unknown function at one point:

$$y'=f(x,y) \qquad y(x_0)=y_0$$

Geometrically, the solution graph passes through $(x_0,y_0)$ and has the slope prescribed by $f$ at every point. The initial value often fixes the arbitrary constant in a solution family, but this conclusion depends on the equation. Some initial-value problems have no solution, some have one, and some have several.

The initial-value problem below is separable:

$$y'=\frac{x}{y} \qquad y(0)=2$$

The equation is defined only where $y\neq0.$ Multiplying by $y$ separates the variables:

$$y\frac{dy}{dx}=x$$

Integration gives:

$$
\begin{align}
\int y \ dy&=\int x \ dx \\[6pt]
\frac{y^2}{2}&=\frac{x^2}{2}+C \\[6pt]
y^2&=x^2+C_1
\end{align}
$$

The condition $y(0)=2$ gives $C_1=4.$ Solving for $y$ gives two branches:

$$y=\pm\sqrt{x^2+4}$$

Only the positive branch has value $2$ at $x=0,$ so the solution is:

$$y(x)=\sqrt{x^2+4}$$

The expression under the [square root](../radicals/) is positive for every real $x,$ and the solution has domain $\mathbb{R}.$ Its derivative is:

$$y'(x)=\frac{x}{\sqrt{x^2+4}}$$

Since $x/y(x)=x/\sqrt{x^2+4},$ the function satisfies both the differential equation and the initial condition.

## Main classes

The form of a first-order equation often indicates a substitution or integration method.

+ A [separable equation](../separable-differential-equations/) has the form $y'=g(x)h(y).$ On an interval where $h(y)\neq0,$ it becomes $\frac{1}{h(y)} \ dy=g(x) \ dx,$ and both sides can be integrated. The zeros of $h$ must be checked separately because division may remove constant solutions.

+ A [linear equation](../first-order-linear-differential-equations/) has the form $y'+p(x)y=q(x).$ An integrating factor depending only on $x$ makes the left-hand side the derivative of a product.

+ An [exact equation](../exact-differential-equations/) has the form $A(x,y) \ dx+B(x,y) \ dy=0.$ Its left-hand side is the differential of a potential function $\Phi(x,y),$ and the solutions satisfy $\Phi(x,y)=C.$ The first step is to calculate this potential function from $A$ and $B.$

+ A [homogeneous equation](../homogeneous-differential-equations/) has a right-hand side that depends on $x$ and $y$ only through their quotient, so its normal form is $y'=R(y/x)$ on an interval where $x\neq0.$ The substitution $v=y/x$ gives a separable equation for $v.$

+ An [autonomous equation](../autonomous-differential-equations/) has the form $y'=f(y),$ with no explicit occurrence of $x.$ The zeros of $f$ give the constant equilibrium solutions. Away from these zeros, the equation is separable.

+ A [Bernoulli equation](../bernoulli-differential-equation/) has the form $y'+a(x)y=b(x)y^m.$ When $m\neq0,1,$ the substitution $z=y^{1-m}$ gives a linear equation for $z$ on an interval where the power is defined and $y\neq0.$

These classes are not disjoint. The equation below is both separable and linear:

$$y'=x(1+y)$$

It is separable because its right-hand side is a product of a function of $x$ and a function of $y.$ It is linear because it can also be written as:

$$y'-xy=x$$

Either classification can be used to find the same solution family.

## Linear equations of order one

The linear case has the standard form:

$$y'+p(x)y=q(x)$$

On an interval where $p$ and $q$ are [continuous](../continuous-functions/), an [integrating factor](../integrating-factors/) is:

$$\mu(x)=e^{\int p(x) \ dx}$$

The [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/) and the [chain rule](../chain-rule/) give $\mu'(x)=p(x)\mu(x).$ Multiplication by $\mu(x)$ gives:

$$\mu(x)y'+\mu(x)p(x)y=\mu(x)q(x)$$

The left-hand side is the derivative of $\mu(x)y$ by the [product rule](../differentiation-rules/):

$$\left(\mu(x)y\right)'=\mu(x)q(x)$$

One integration then gives:

$$\mu(x)y=\int \mu(x)q(x) \ dx+C$$

Solving for $y$ gives:

$$y=\frac{1}{\mu(x)}\left(\int \mu(x)q(x) \ dx+C\right)$$

The arbitrary constant $C$ is determined when one initial value is prescribed.

Suppose that a body has temperature $T(t)$ and its surroundings have the constant temperature $T_a.$ Newton's law of cooling assumes that $T'$ is $-k$ times the difference $T-T_a.$ Its linear form is:

$$T'+kT=kT_a \qquad k>0$$

Both $p(t)=k$ and $q(t)=kT_a$ are constant, so the integrating factor is $\mu(t)=e^{kt}$ and the equation becomes:

$$\left(e^{kt}T\right)'=kT_ae^{kt}$$

One integration gives $e^{kt}T=T_ae^{kt}+C.$ Solving for $T$ gives:

$$T(t)=T_a+Ce^{-kt}$$

The constant $C$ is the initial difference $T(0)-T_a,$ and the temperature tends to $T_a$ as $t\to+\infty.$

Further examples are in the entry on [first-order linear differential equations](../first-order-linear-differential-equations/).

## Exact, homogeneous, autonomous, and Bernoulli equations

An [exact differential equation](../exact-differential-equations/) has the form:

$$A(x,y) \ dx+B(x,y) \ dy=0$$

It is exact when a function $\Phi(x,y)$ has partial derivatives $\Phi_x=A$ and $\Phi_y=B.$ The equation is then $d\Phi=0,$ so its solutions have the implicit form:

$$\Phi(x,y)=C$$

Suppose that $A$ and $B$ have continuous first partial derivatives on a simply connected region. The equation is exact there precisely when:

$$\frac{\partial A}{\partial y}=\frac{\partial B}{\partial x}$$

This equality is a test for exactness. To calculate $\Phi,$ integrate one coefficient and compare the result with the other.

An equation that fails the test may become exact after multiplication by a nonzero factor. A function $\mu(x,y)$ for which $\mu A \ dx+\mu B \ dy=0$ is exact is an [integrating factor](../integrating-factors/) of the equation. Write $A_y$ and $B_x$ for the two partial derivatives above. If the integrating factor depends only on $x,$ exactness requires $\mu A_y=\mu'B+\mu B_x.$ On a region where $B\neq0,$ division by $\mu B$ gives:

$$\frac{\mu'}{\mu}=\frac{A_y-B_x}{B}$$

Such a factor exists when the right-hand side depends on $x$ alone. Similarly, on a region where $A\neq0,$ a factor that depends only on $y$ must satisfy $\frac{1}{\mu}\frac{d\mu}{dy}=(B_x-A_y)/A.$ It exists when the right-hand side depends on $y$ alone. Consider the equation:

$$\left(3xy+y^2\right) \ dx+\left(x^2+xy\right) \ dy=0$$

The two partial derivatives are $A_y=3x+2y$ and $B_x=2x+y,$ so $(A_y-B_x)/B=1/x.$ On a region where $x\neq0,$ the function $\mu(x)=x$ is nonzero and is an integrating factor. Multiplication by $x$ gives an exact equation with potential $\Phi(x,y)=x^3y+\frac{1}{2}x^2y^2,$ and its solutions satisfy $\Phi(x,y)=C.$

A [homogeneous equation](../homogeneous-differential-equations/) has the normal form on an interval where $x\neq0$:

$$y'=R\left(\frac{y}{x}\right)$$

The right-hand side depends on the two variables only through their quotient. If $A$ and $B$ in $A \ dx+B \ dy=0$ are homogeneous functions of the same degree $k,$ the equation also has this normal form. Homogeneity means that $A(\lambda x,\lambda y)=\lambda^kA(x,y)$ and $B(\lambda x,\lambda y)=\lambda^kB(x,y)$ for every $\lambda>0.$ The common factor $\lambda^k$ cancels in the quotient $-A/B.$ Setting $v=y/x$ gives $y=vx$ and $y'=v+xv',$ so the equation becomes:

$$xv'=R(v)-v$$

This equation is separable. Each root $c$ of $R(v)=v$ gives the line $y=cx$ as a solution on an interval where $x\neq0,$ and these solutions must be recorded before division by $R(v)-v.$ Consider the equation:

$$y'=\frac{y}{x}+\frac{y^2}{x^2}$$

The substitution gives $xv'=v^2.$ For $v\neq0,$ separation and integration give $-1/v=\ln|x|+C,$ so:

$$y(x)=-\frac{x}{\ln|x|+C}$$

The formula defines a solution on any interval where $x\neq0$ and $\ln|x|+C\neq0.$ The root $v=0,$ excluded by division, gives the solution $y=0$ on any interval that does not contain $0.$

> The word homogeneous has a second, unrelated meaning for linear equations, where the right-hand side is zero. The context distinguishes the two uses.

An [autonomous equation](../autonomous-differential-equations/) is:

$$y'=f(y)$$

Every zero $y_*$ of $f$ gives a constant solution $y=y_*.$ These equilibrium solutions must be recorded before division by $f(y).$ On an interval where $f(y)\neq0,$ the nonconstant solutions satisfy:

$$\frac{1}{f(y)} \ dy=dx$$

The sign of $f(y)$ is enough to decide monotonicity. A solution is increasing where $f(y)>0$ and decreasing where $f(y)<0.$

A [Bernoulli equation](../bernoulli-differential-equation/) is:

$$y'+a(x)y=b(x)y^m$$

Assume that $m\neq0,1$ and work on an interval where the power is defined and $y\neq0.$ The substitution $z=y^{1-m}$ gives:

$$z'=(1-m)y^{-m}y'$$

After division by $y^m,$ the Bernoulli equation becomes linear in $z:$

$$z'+(1-m)a(x)z=(1-m)b(x)$$

Any solution excluded by the condition $y\neq0$ must be checked in the original equation.

## Existence and uniqueness

Consider the initial-value problem:

$$y'=f(x,y) \qquad y(x_0)=y_0$$

The equation and initial value do not by themselves guarantee a solution. If $f$ is continuous on a rectangle about $(x_0,y_0),$ Peano's theorem gives at least one solution on an interval about $x_0.$ If $f$ is locally Lipschitz with respect to $y,$ at most one solution passes through $(x_0,y_0).$ Together, the two hypotheses give the unique local solution asserted by the Picard-Lindelöf theorem. A continuous [partial derivative](../partial-derivatives/) $\partial f/\partial y$ near the initial point is sufficient for the local Lipschitz condition.

A proof of the Picard-Lindelöf theorem begins by writing the problem in integral form. Integrating from $x_0$ to $x$ and using the initial value gives:

$$y(x)=y_0+\int_{x_0}^{x}f\left(t,y(t)\right) \ dt$$

A continuous function satisfies this relation on an interval about $x_0$ exactly when it solves the initial-value problem there. Starting with the constant function $y_0(x)=y_0,$ define the Picard iterates by:

$$y_{k+1}(x)=y_0+\int_{x_0}^{x}f\left(t,y_k(t)\right) \ dt$$

On a sufficiently short interval, the Lipschitz condition makes the integral operator in this recurrence a contraction in the uniform norm. The iterates converge uniformly to its unique fixed point, which is the solution of the initial-value problem.

Continuity alone does not give uniqueness. Consider the problem:

$$y'=3|y|^{2/3} \qquad y(0)=0$$

Two solutions through $(0,0)$ are:

$$y_1(x)=0 \qquad y_2(x)=x^3$$

For $y_2=x^3,$ the derivative is $3x^2,$ and $3|x^3|^{2/3}=3x^2.$ The function $f(y)=3|y|^{2/3}$ is continuous at $y=0,$ but it is not locally Lipschitz there. The two solutions do not contradict the uniqueness theorem because its Lipschitz hypothesis fails.

Existence and uniqueness are local statements. The equation $y'=y^2$ considered above also illustrates this point. The initial value $y(0)=1$ selects $C=1,$ so the unique local solution is $y=1/(1-x).$ Its maximal interval is $(-\infty,1),$ and the solution becomes unbounded as $x\to1^-.$

If $p$ and $q$ in the linear equation $y'+p(x)y=q(x)$ are continuous on an interval $I$ and $x_0\in I,$ the integrating factor is nonzero throughout $I.$ Its formula gives one solution for each initial value on the whole of $I.$

## Reduction of higher-order equations

Some equations of higher order reduce directly to equations of order one. If the unknown function itself does not occur in a second-order equation, its form is:

$$F(x,y',y'')=0$$

The substitution $p=y'$ gives the first-order equation $F(x,p,p')=0.$ Solving it for $p$ and integrating once recovers $y.$

If the independent variable does not occur, the equation has the form:

$$F(y,y',y'')=0$$

On an interval where $y$ can be used as the independent variable, set $p(y)=y'.$ The [chain rule](../chain-rule/) gives $y''=p\frac{dp}{dy},$ and the equation is first-order in $p(y).$ For $yy''=(y')^2,$ this substitution gives:

$$yp\frac{dp}{dy}=p^2$$

On an interval where $p\neq0$ and $y\neq0,$ division gives $y\frac{dp}{dy}=p,$ hence $\frac{dp}{p}=\frac{dy}{y}$ and $p=C_1y.$ The remaining equation $y'=C_1y$ has the solutions:

$$y(x)=C_2e^{C_1x}$$

The excluded case $p=0$ gives the constant solutions, and the formula contains them when $C_1=0.$

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
