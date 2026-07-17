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

In normal form, $f(x,y)$ is the slope at the point $(x,y).$ A solution is a differentiable function whose graph has this slope at every point. Not every implicit equation has a single normal form. For example, the equation:

$$(y')^2+y^2=1$$

has two normal forms wherever $|y|<1:$

$$y'=\sqrt{1-y^2}$$

and:

$$y'=-\sqrt{1-y^2}$$

The two signs are the two possible slopes through the same point. At $|y|=1,$ the derivative is zero, while no real slope satisfies the equation when $|y|>1.$

## Solutions and maximal intervals

A solution of $y'=f(x,y)$ on an [interval](../intervals/) $I$ is a differentiable function $y:I\to\mathbb{R}$ such that:

$$y'(x)=f(x,y(x)) \qquad \forall x\in I$$

The [domain](../determining-the-domain-of-a-function/) is part of the solution. A formula may satisfy the equation wherever it is defined and still fail to extend across a point where the formula or the equation is undefined.

Consider the equation:

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

For each $C\in\mathbb{R},$ this formula has two maximal intervals, $(-\infty,C)$ and $(C,+\infty).$ It cannot be extended through $x=C$ because its values are unbounded there. The equation also has the constant solution $y=0,$ which was excluded when we divided by $y^2.$

> The zeros of an expression containing the unknown function must be checked before division. Division may remove valid solutions. Conversely, an operation such as squaring may add candidates, so every candidate must be substituted into the original equation.

Each value of $C$ gives a member of the solution family. A particular solution has a fixed value of $C$ and a specified interval. A formula without its interval is therefore incomplete.

## Initial-value problems

An [initial-value problem](../initial-value-problems/) has a differential equation and the value of the unknown function at one point:

$$y'=f(x,y) \qquad y(x_0)=y_0$$

Geometrically, the solution graph passes through $(x_0,y_0)$ and has the slope prescribed by $f$ at every point. The initial value often fixes the arbitrary constant in a solution family, but this conclusion depends on the equation. Some initial-value problems have no solution, some have one, and some have several.

Consider the separable initial-value problem:

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

The form of a first-order equation tells which method applies. Several classes have their own substitution or integration method.

+ A [separable equation](../separable-differential-equations/) has the form $y'=g(x)h(y).$ On an interval where $h(y)\neq0,$ it becomes $\frac{1}{h(y)} \ dy=g(x) \ dx,$ and both sides can be integrated. The zeros of $h$ must be checked separately because division may remove constant solutions.

+ A [linear equation](../first-order-linear-differential-equations/) has the form $y'+p(x)y=q(x).$ An integrating factor depending only on $x$ makes the left-hand side the derivative of a product.

+ An [exact equation](../exact-differential-equations/) has the form $A(x,y) \ dx+B(x,y) \ dy=0.$ Its left-hand side is the differential of a potential function $\Phi(x,y),$ and the solutions satisfy $\Phi(x,y)=C.$ The first step is to calculate this potential function from $A$ and $B.$

+ An [autonomous equation](../autonomous-differential-equations/) has the form $y'=f(y),$ with no explicit occurrence of $x.$ The zeros of $f$ give the constant equilibrium solutions. Away from these zeros, the equation is separable.

+ A [Bernoulli equation](../bernoulli-differential-equation/) has the form $y'+a(x)y=b(x)y^m.$ When $m\neq0,1,$ the substitution $z=y^{1-m}$ changes it into a linear equation for $z.$
	
These classes are not disjoint. The equation:

$$y'=x(1+y)$$

is separable because its right-hand side is a product of a function of $x$ and a function of $y.$ It is also linear because it can be written as:

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

Hence:

$$y=\frac{1}{\mu(x)}\left(\int \mu(x)q(x) \ dx+C\right)$$

This formula has one arbitrary constant, as expected for a first-order equation. Its derivation and worked examples are in the entry on [first-order linear differential equations](../first-order-linear-differential-equations/).

## Exact, autonomous, and Bernoulli equations

An [exact differential equation](../exact-differential-equations/) has the form:

$$A(x,y) \ dx+B(x,y) \ dy=0$$

It is exact when a function $\Phi(x,y)$ has partial derivatives $\Phi_x=A$ and $\Phi_y=B.$ The equation is then $d\Phi=0,$ so its solutions have the implicit form:

$$\Phi(x,y)=C$$

Suppose that $A$ and $B$ have continuous first partial derivatives on a simply connected region. The equation is exact there precisely when:

$$\frac{\partial A}{\partial y}=\frac{\partial B}{\partial x}$$

This equality is a test for exactness. To calculate $\Phi,$ integrate one coefficient and compare the result with the other.

An [autonomous equation](../autonomous-differential-equations/) is:

$$y'=f(y)$$

Every zero $y_*$ of $f$ gives a constant solution $y=y_*.$ These equilibrium solutions must be recorded before division by $f(y).$ On an interval where $f(y)\neq0,$ the nonconstant solutions satisfy:

$$\frac{1}{f(y)} \ dy=dx$$

The sign of $f(y)$ is enough to decide monotonicity. A solution is increasing where $f(y)>0$ and decreasing where $f(y)<0.$

A [Bernoulli equation](../bernoulli-differential-equation/) is:

$$y'+a(x)y=b(x)y^m$$

When $m\neq0,1$ and $y\neq0,$ the substitution $z=y^{1-m}$ gives:

$$z'=(1-m)y^{-m}y'$$

After division by $y^m,$ the Bernoulli equation becomes linear in $z:$

$$z'+(1-m)a(x)z=(1-m)b(x)$$

Any solution excluded by the condition $y\neq0$ must be checked in the original equation.

## Local existence and uniqueness

For the initial-value problem:

$$y'=f(x,y) \qquad y(x_0)=y_0$$

the equation and initial value do not by themselves guarantee a solution. If $f$ is continuous on a rectangle containing $(x_0,y_0),$ at least one solution exists on some interval about $x_0.$ If $f$ is locally Lipschitz with respect to $y,$ at most one solution passes through $(x_0,y_0).$ Together, the two hypotheses give a unique local solution. A continuous [partial derivative](../partial-derivatives/) $\partial f/\partial y$ near the initial point is sufficient for the local Lipschitz condition.

Continuity alone does not give uniqueness. The problem:

$$y'=3|y|^{2/3} \qquad y(0)=0$$

has the constant solution:

$$y(x)=0$$

It also has the solution:

$$y(x)=x^3$$

For $y=x^3,$ the derivative is $3x^2,$ and $3|x^3|^{2/3}=3x^2.$ The function $f(y)=3|y|^{2/3}$ is continuous at $y=0,$ but it is not locally Lipschitz there. The two solutions through $(0,0)$ do not contradict the uniqueness theorem because its hypothesis fails.

Existence and uniqueness are local statements. For example, the solution $y=1/(1-x)$ of $y'=y^2$ with $y(0)=1$ is unique near $x=0,$ but its maximal interval is $(-\infty,1).$ The solution becomes unbounded as $x\to1^-.$

## Higher-order equations as first-order systems

First-order equations are also the basic form for equations of higher order. Consider a second-order equation in normal form:

$$y''=G(x,y,y')$$

Set $u=y$ and $v=y'.$ The equation is equivalent to the [system of differential equations](../systems-of-differential-equations/):

$$
\begin{align}
u'&=v \\[6pt]
v'&=G(x,u,v)
\end{align}
$$

An equation of order $n$ has an analogous system, with one new unknown for each derivative from $y$ through $y^{(n-1)}.$ Existence and uniqueness results for first-order systems are therefore also results for higher-order equations.
