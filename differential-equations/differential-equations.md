---
title: Differential Equations
source: https://algebrica.org/differential-equations/
license: CC BY-NC 4.0
tags:
  - boundary-value-problem
  - differential-equations
  - first-order-differential-equations
  - initial-value-problem
  - linear-differential-equations
  - nonlinear-differential-equations
  - ordinary-differential-equations
  - partial-differential-equations
---
## Introduction

A differential equation is an [equation](../equations/) in which the unknown is a [function](../functions/) and one or more of its [derivatives](../derivatives/) are present. In contrast, an algebraic equation has numbers as its unknowns. For a function $y = y(x)$ of one variable, a differential equation of order $n$ has the implicit form:

$$F\left(x, y, y', y'', \ldots, y^{(n)}\right) = 0$$

The dependence of $F$ on $y^{(n)}$ means that the derivative of order $n$ is present. A solution on an [interval](../intervals/) $I$ is a function $y:I \to \mathbb{R}$ that has all the derivatives required by the equation and satisfies it at every point of $I.$ The [domain](../determining-the-domain-of-a-function/) is part of the solution because the equation and the required derivatives must be defined throughout $I.$ For example, $\ln|x| + C$ solves $y' = 1/x$ on an interval that does not contain $0,$ but it is not a solution on an interval that contains $0.$

A first-order example is:

$$y' + y = 0$$

For each [real number](../real-numbers/) $C,$ the function $y(x) = Ce^{-x}$ has derivative $y'(x) = -Ce^{-x}.$ Substitution gives:

$$y'(x) + y(x) = -Ce^{-x} + Ce^{-x} = 0$$

Conversely, if $y$ is any solution, the product rule gives $\left(e^xy\right)' = e^x(y' + y) = 0.$ Hence $e^xy = C,$ and $y = Ce^{-x}.$ The functions $y(x) = Ce^{-x},$ with $C \in \mathbb{R},$ therefore form the general solution on $\mathbb{R}.$ A single member of the family is a particular solution. An initial condition may select one member.

In the equivalent form $y' = -y,$ the equation states that a quantity decreases at a rate proportional to the amount present. The condition $y(0) = y_0 > 0$ gives the particular solution $y(x) = y_0e^{-x},$ whose value is halved over each interval of length $\ln(2).$ Models of radioactive decay and capacitor discharge have the form $y' = -ky,$ where $k > 0$ sets the time scale and the half-life is $\ln(2)/k.$

## Ordinary and partial differential equations

An [ordinary differential equation](../ordinary-differential-equations/) has one independent variable, and all its derivatives are taken with respect to that variable. If $y$ depends on $x,$ the equation below is ordinary because $x$ is its only independent variable:

$$y'' + x^2y' - y = \sin(x)$$

A [partial differential equation](../partial-differential-equations/) has an unknown function of two or more independent variables and at least one [partial derivative](../partial-derivatives/). If $u = u(x,t)$ is the temperature at position $x$ and time $t,$ the one-dimensional heat equation is:

$$\frac{\partial u}{\partial t} = k\frac{\partial^2u}{\partial x^2} \qquad k > 0$$

The derivative with respect to $t$ is the rate of change in time, while the second derivative with respect to $x$ measures spatial curvature.

## Classification by order

The order of an equation is the order of its highest derivative. Thus, if $y^{(n)}$ is present and every derivative of greater order is absent, the equation has order $n.$ Linearity is a separate classification.

+ $y' = x-y$ is a first-order equation.
+ $y'' + 4y = 0$ is a second-order equation.
+ $y''' + yy' = e^x$ is a third-order equation.

For a scalar equation in normal form, the order is also the number of values in its standard initial data. Under the hypotheses of an existence and uniqueness theorem, an initial-value problem for a first-order equation has one prescribed value, while one for a second-order equation has two.

The second-order equation $y'' + 4y = 0$ has the general solution in terms of [sine and cosine](../sine-and-cosine/):

$$y(x) = A\cos(2x) + B\sin(2x)$$

The values of $y(x_0)$ and $y'(x_0)$ fix the two constants.

## First-order differential equations

In a [first-order differential equation](../first-order-differential-equations/), $y'$ occurs but [higher-order derivatives](../higher-order-derivatives/) do not. Its implicit form is:

$$F(x,y,y') = 0$$

If the equation can be solved for $y',$ its normal form is:

$$y' = f(x,y)$$

Among first-order equations, an equation is [separable](../separable-differential-equations/) if it can be written as $y' = g(x)h(y),$ and it is linear if it has the form $y' + p(x)y = q(x).$ Some first-order equations are both separable and linear. One separable equation is:

$$y' = 2xy$$

Assume that $y \neq 0$ on an interval. Dividing by $y$ separates the two variables:

$$\frac{1}{y}\frac{dy}{dx} = 2x$$

Integrating both sides gives:

$$\ln|y| = x^2 + C_1$$

The [absolute value](../absolute-value/) inside the [logarithm](../logarithms/) is needed because $1/y$ has antiderivatives on both $y > 0$ and $y < 0.$ Exponentiation gives the solution family:

$$y(x) = Ce^{x^2}$$

Division by $y$ excluded the zero solution, so we include $C = 0$ in the family. The [chain rule](../chain-rule/) verifies the formula:

$$y'(x) = 2xCe^{x^2} = 2xy(x)$$

This equation is also linear because it can be written as $y' - 2xy = 0,$ whose coefficient $-2x$ depends only on the independent variable. Order and linearity are independent. Equations of order one include linear and nonlinear cases, while linear equations occur at every order.

## Linear and nonlinear differential equations

In a [linear differential equation](../linear-differential-equations/), the unknown function and its derivatives form a linear combination. For an equation of order $n,$ this combination is:

$$a_n(x)y^{(n)} + a_{n-1}(x)y^{(n-1)} + \cdots + a_1(x)y' + a_0(x)y = g(x)$$

The leading coefficient $a_n(x)$ is nonzero throughout the interval, and each coefficient is a function of the independent variable $x$ alone. The unknown function and its derivatives occur only to the first power, no two of them are multiplied together, and none is the argument of a nonlinear function. The equation is homogeneous when $g(x) = 0$ throughout the interval and nonhomogeneous otherwise.

Write the left-hand side as $L[y].$ If $y_1$ and $y_2$ are solutions of the homogeneous equation and $c_1,c_2$ are constants, linearity gives:

$$L[c_1y_1 + c_2y_2] = c_1L[y_1] + c_2L[y_2] = 0$$

The homogeneous solutions therefore form a [vector space](../vector-spaces/). When the coefficients are continuous and $a_n$ has no zero on the interval, this vector space has dimension $n.$ Hence $n$ linearly independent solutions give every solution as a [linear combination](../linear-combinations/). The family $A\cos(2x) + B\sin(2x)$ above is the general solution of $y'' + 4y = 0.$

The difference of two solutions of a nonhomogeneous equation is a solution of the associated homogeneous equation because subtracting their equations cancels the right-hand side $g(x).$ Every solution therefore has the form $y = y_p + y_h,$ where $y_p$ is one fixed solution of the nonhomogeneous equation and $y_h$ is any homogeneous solution. These properties follow from linearity and do not hold in general for nonlinear equations.

When $n = 1,$ division by the leading coefficient gives:

$$y' + p(x)y = q(x)$$

The equation below is linear and first-order:

$$y' + 2y = e^x$$

An integrating factor $\mu(x)$ must satisfy $\mu' = 2\mu,$ so we take $\mu(x) = e^{2x}.$ After multiplication by $e^{2x},$ the left-hand side is the derivative of a product by the [product rule](../differentiation-rules/):

$$e^{2x}y' + 2e^{2x}y = e^{3x}$$

The equation is therefore equivalent to:

$$\left(e^{2x}y\right)' = e^{3x}$$

Integration and division by $e^{2x}$ give:

$$
\begin{align}
e^{2x}y &= \frac{1}{3}e^{3x} + C \\[6pt]
y &= \frac{1}{3}e^x + Ce^{-2x}
\end{align}
$$

The term $\frac{1}{3}e^x$ is a particular solution, and $Ce^{-2x}$ is the general solution of the associated homogeneous equation.

The entry on [first-order linear differential equations](../first-order-linear-differential-equations/) gives the general method.

In a [nonlinear differential equation](../nonlinear-differential-equations/), the unknown function or at least one of its derivatives appears in a nonlinear term. The source of nonlinearity differs in these examples:

+ In $yy' = x,$ the unknown function is multiplied by its derivative.
+ In $(y')^2 + y = 0,$ the derivative is squared.
+ In $y'' + \sin(y) = 0,$ the sine is applied to the unknown function.

For example, $y' = y^2$ has order one and is nonlinear, whereas $y'' + 4y = 0$ has order two and is linear.

## Autonomous equations and systems

In an autonomous ordinary differential equation, the independent variable does not occur explicitly. A first-order autonomous equation is of the form $y' = f(y).$ The logistic equation for a population $P(t)$ is autonomous:

$$P' = rP\left(1-\frac{P}{K}\right) \qquad r,K > 0$$

The rate is a function of the current population alone, and time does not occur explicitly. The equation is first-order, autonomous, separable, and nonlinear. The constant functions $P(t) = 0$ and $P(t) = K$ are its equilibrium solutions.

If $0 < P(0) < K,$ the solution is increasing and has the shape of a [sigmoid function](../sigmoid-function/).

A [system of differential equations](../systems-of-differential-equations/) is a collection of equations for several unknown functions and their derivatives. A model for two interacting populations is:

$$
\begin{align}
x' &= ax-bxy \\[6pt]
y' &= -cy+dxy
\end{align}
$$

Here $x$ and $y$ are unknown functions of time, and $a,b,c,d$ are positive constants. The products $xy$ make the system nonlinear. Setting $z_1 = y,$ $z_2 = y',$ $\ldots,$ and $z_n = y^{(n-1)}$ converts an equation of order $n$ in normal form into a first-order system for $z_1,\ldots,z_n.$

## Initial and boundary conditions

A differential problem has an equation and conditions on its solutions. An [initial-value problem](../initial-value-problems/) has all its prescribed values at the same point of the independent variable. The problem below has one condition at $x = 0$:

$$y' = 2y \qquad y(0) = 3$$

The differential equation has the family $y(x) = Ce^{2x}.$ The condition $y(0) = 3$ gives $C = 3,$ so the solution is:

$$y(x) = 3e^{2x}$$

For a scalar equation in normal form of order $n,$ the initial data are the values of $y,y',\ldots,y^{(n-1)}$ at one point.

A [boundary-value problem](../boundary-value-problems/) has conditions at different points, often at the endpoints of an interval. The problem below has conditions at two points:

$$y'' + y = 0 \qquad y(0) = 0 \qquad y\left(\frac{\pi}{2}\right) = 1$$

The general solution of the differential equation is $y(x) = A\cos(x) + B\sin(x).$ The first boundary condition gives $A = 0,$ and the second then gives $B = 1.$ The solution is therefore:

$$y(x) = \sin(x)$$

Conditions alone do not ensure a unique solution. The equation $y'' + y = 0$ on $[0,\pi]$ has no solution with $y(0) = 0$ and $y(\pi) = 1,$ since every function $B\sin(x)$ vanishes at both endpoints. With the conditions $y(0) = y(\pi) = 0,$ every function $B\sin(x)$ is a solution. Thus a boundary-value problem may have no solution, one solution, or several solutions.

An existence theorem states sufficient conditions for at least one solution, while a uniqueness theorem states sufficient conditions under which two solutions with the same data are equal. [Continuity](../continuous-functions/) alone does not guarantee uniqueness. For example, the problem $y' = 3\sqrt[3]{y^2},$ $y(0) = 0,$ has both $y(x) = 0$ and $y(x) = x^3$ as solutions. For $y(x) = x^3,$ both sides of the equation are $3x^2,$ while both sides vanish for $y(x) = 0.$

For a linear equation, suppose that its coefficients and right-hand side are continuous on an interval $I$ and that its leading coefficient has no zero there. An initial-value problem posed at a point of $I$ then has exactly one solution on the whole interval $I.$ For a nonlinear equation $y' = f(x,y),$ continuity of $f$ and local Lipschitz continuity with respect to $y$ near the initial point give a unique local solution. The equation $y' = y^2,$ with $y(0) = 1,$ has the solution $y(x) = 1/(1-x),$ which is unbounded as $x$ approaches $1.$ Thus a local solution need not extend to the whole domain of $f.$

## Explicit, implicit, and numerical descriptions

An explicit solution has the dependent variable isolated, as in $y(x) = Ce^{-x}.$ An implicit solution is a relation between the variables. The relation below defines an implicit family of solutions of $yy' = x$:

$$y^2-x^2 = C$$

Differentiation with respect to $x$ gives $2yy'-2x = 0,$ which is equivalent to the differential equation. Away from points where $y = 0,$ solving for $y$ gives the explicit branches $y = \pm\sqrt{x^2+C}.$ Each sign gives a solution on an interval where $x^2+C > 0.$

The solution of an initial-value problem may not be expressible in elementary functions. For example, $y' = e^{-x^2},$ $y(0) = 0,$ has the solution $y(x) = \int_0^x e^{-t^2} \ dt,$ which is not an elementary function. When no elementary formula is available, one studies existence and uniqueness, properties of the solution, or numerical approximations. For the initial-value problem $y' = f(x,y),$ $y(x_0) = y_0,$ [Euler's method](../euler-method/) with step size $h$ uses the recurrence:

$$x_{n+1} = x_n + h, \qquad y_{n+1} = y_n + hf(x_n,y_n)$$

The values $y_n$ approximate the solution at the points $x_n.$ Qualitative analysis can determine properties such as monotonicity and stability without a closed formula. At a point where the leading coefficient is nonzero, a linear equation with analytic coefficients has local solutions that can be represented by [power series](../power-series/).
