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

A differential equation is an [equation](../equations/) that has a [function](../functions/) as its unknown and contains one or more of its [derivatives](../derivatives/). In an algebraic equation the unknowns are numbers. In a differential equation the unknowns are functions subject to conditions on their rates of change. For a function $y = y(x)$ of one variable, a differential equation of order $n$ has the general implicit form:

$$F\left(x, y, y', y'', \ldots, y^{(n)}\right) = 0$$

A solution on an [interval](../intervals/) $I$ is a function $y:I \to \mathbb{R},$ with all the derivatives required by the equation, for which the equation is true at every point of $I.$ The [domain](../determining-the-domain-of-a-function/) is part of the solution because the same formula may be defined on one interval and undefined on another. A simple example is:

$$y' + y = 0$$

For each [real number](../real-numbers/) $C,$ the function $y(x) = Ce^{-x}$ has derivative $y'(x) = -Ce^{-x}.$ Substitution gives:

$$y'(x) + y(x) = -Ce^{-x} + Ce^{-x} = 0$$

Thus $y(x) = Ce^{-x}$ is a family of solutions on $\mathbb{R}.$ A differential equation usually has a family of solutions, and additional conditions may fix one of them. A differential equation is often a model for a quantity that changes and its derivatives describe how that quantity changes in time or space.

## Ordinary and partial differential equations

An [ordinary differential equation](../ordinary-differential-equations/) has one independent variable, and all its derivatives are taken with respect to that variable. If $y$ depends on $x,$ the equation:

$$y'' + x^2y' - y = \sin(x)$$

is an ordinary differential equation because $x$ is its only independent variable.

A [partial differential equation](../partial-differential-equations/) has an unknown function of two or more independent variables and contains at least one [partial derivative](../partial-derivatives/). If $u = u(x,t)$ is the temperature at position $x$ and time $t,$ the one-dimensional heat equation is:

$$\frac{\partial u}{\partial t} = k\frac{\partial^2u}{\partial x^2} \qquad k > 0$$

The derivative with respect to $t$ is the rate of change in time, while the second derivative with respect to $x$ measures spatial curvature. Ordinary and partial differential equations have different solution theories, even when they model related phenomena.

## Classification by order

Inspect the derivatives that occur in the equation. If $y^{(n)}$ is present and every derivative of greater order is absent, the equation has order $n.$ Linearity is a separate classification.

+ $y' = x-y$ is a first-order equation.
+ $y'' + 4y = 0$ is a second-order equation.
+ $y''' + yy' = e^x$ is a third-order equation.

The order is also the usual number of initial values for a scalar equation. Under the hypotheses of an existence and uniqueness theorem, an initial-value problem for a first-order equation has one prescribed value, while one for a second-order equation has two.

For instance, the second-order equation $y'' + 4y = 0$ has a solution family made from [sine and cosine](../sine-and-cosine/):

$$y(x) = A\cos(2x) + B\sin(2x)$$

The values of $y(x_0)$ and $y'(x_0)$ fix the two constants.

## First-order differential equations

In a [first-order differential equation](../first-order-differential-equations/), $y'$ occurs but [higher-order derivatives](../higher-order-derivatives/) do not. Its implicit form is:

$$F(x,y,y') = 0$$

If the equation can be solved for $y',$ its normal form is:

$$y' = f(x,y)$$

Among first-order equations, separability means $y' = g(x)h(y),$ while linearity means $y' + p(x)y = q(x).$ Some first-order equations are both separable and linear. The following equation is separable:

$$y' = 2xy$$

Assume that $y \neq 0$ on an interval. Dividing by $y$ separates the two variables:

$$\frac{1}{y}\frac{dy}{dx} = 2x$$

Using [indefinite integration](../indefinite-integrals/) on both sides gives:

$$\ln|y| = x^2 + C_1$$

The [absolute value](../absolute-value/) inside the [logarithm](../logarithms/) is needed because $1/y$ has antiderivatives on both $y > 0$ and $y < 0.$ Exponentiation gives the solution family:

$$y(x) = Ce^{x^2}$$

The case $C = 0$ is the zero solution, which was lost temporarily when we divided by $y.$ The [chain rule](../chain-rule/) verifies the formula:

$$y'(x) = 2xCe^{x^2} = 2xy(x)$$

This equation is also linear because it can be written as $y' - 2xy = 0.$ The factor $-2x$ is an allowed coefficient because it depends on the independent variable alone. Order and linearity are independent. Equations of order one include linear and nonlinear cases, while linear equations occur at every order.

## Linear and nonlinear differential equations

In a [linear differential equation](../linear-differential-equations/), the unknown function and its derivatives form a linear combination. For an equation of order $n,$ this combination is:

$$a_n(x)y^{(n)} + a_{n-1}(x)y^{(n-1)} + \cdots + a_1(x)y' + a_0(x)y = g(x)$$

The leading coefficient $a_n(x)$ is nonzero throughout the interval. Each coefficient is a function of the independent variable $x$ alone. The unknown function and its derivatives have exponent one, and no two of them are multiplied together. The equation is homogeneous when $g(x) = 0$ throughout the interval and nonhomogeneous otherwise.

When $n = 1,$ division by the leading coefficient gives:

$$y' + p(x)y = q(x)$$

A first-order example is:

$$y' + 2y = e^x$$

The integrating factor is $e^{2x}.$ By the [product rule](../differentiation-rules/), the left-hand side after multiplication is the derivative of a product:

$$e^{2x}y' + 2e^{2x}y = e^{3x}$$

Therefore:

$$\left(e^{2x}y\right)' = e^{3x}$$

Integration and division by $e^{2x}$ give:

$$
\begin{align}
e^{2x}y &= \frac{1}{3}e^{3x} + C \\[6pt]
y &= \frac{1}{3}e^x + Ce^{-2x}
\end{align}
$$

Both terms in the solution are constant multiples of [exponential functions](../exponential-function/).

The general method is given in the entry on [first-order linear differential equations](../first-order-linear-differential-equations/).

In a [nonlinear differential equation](../nonlinear-differential-equations/), the unknown function or at least one of its derivatives appears in a nonlinear term. The following equations are nonlinear for different reasons:

+ In $yy' = x,$ the unknown function is multiplied by its derivative.
+ In $(y')^2 + y = 0,$ the derivative is squared.
+ In $y'' + \sin(y) = 0,$ the sine is applied to the unknown function.

For example, $y' = y^2$ has order one and is nonlinear, whereas $y'' + 4y = 0$ has order two and is linear.

## Autonomous equations and systems

In an autonomous ordinary differential equation, the independent variable does not occur explicitly. A first-order autonomous equation is of the form $y' = f(y).$ The logistic equation for a population $P(t)$ is an example:

$$P' = rP\left(1-\frac{P}{K}\right) \qquad r,K > 0$$

The rate is a function of the current population alone, and time does not occur explicitly. The equation is first-order, autonomous, separable, and nonlinear.

If $0 < P(0) < K,$ each nonconstant solution has the shape of a [sigmoid function](../sigmoid-function/).

A [system of differential equations](../systems-of-differential-equations/) is a collection of equations for several unknown functions and their derivatives. A model for two interacting populations is:

$$
\begin{align}
x' &= ax-bxy \\[6pt]
y' &= -cy+dxy
\end{align}
$$

Here $x$ and $y$ are unknown functions of time, and $a,b,c,d$ are positive constants. The products $xy$ make the system nonlinear. A higher-order equation in normal form is equivalent to a first-order system after new variables are introduced for its successive derivatives.

## Initial and boundary conditions

Besides the equation, a differential problem has conditions on its solutions. An [initial-value problem](../initial-value-problems/) has all its prescribed values at the same point of the independent variable. Consider:

$$y' = 2y \qquad y(0) = 3$$

The differential equation has the family $y(x) = Ce^{2x}.$ The condition $y(0) = 3$ gives $C = 3,$ so the solution is:

$$y(x) = 3e^{2x}$$

For a scalar equation of order $n,$ the usual initial data are the values of $y,y',\ldots,y^{(n-1)}$ at one point.

A [boundary-value problem](../boundary-value-problems/) has conditions at different points, often at the endpoints of an interval. Consider:

$$y'' + y = 0 \qquad y(0) = 0 \qquad y\left(\frac{\pi}{2}\right) = 1$$

The general solution of the differential equation is $y(x) = A\cos(x) + B\sin(x).$ The first boundary condition gives $A = 0,$ and the second then gives $B = 1.$ The solution is therefore:

$$y(x) = \sin(x)$$

Conditions alone do not ensure a unique solution. Depending on the equation and the data, an initial-value problem or a boundary-value problem may have no solution, one solution, or several solutions. An existence theorem gives hypotheses for at least one solution, while a uniqueness theorem gives hypotheses that rule out a second. [Continuity](../continuous-functions/) is part of many existence hypotheses, although continuity alone does not guarantee uniqueness.

## Explicit, implicit, and numerical descriptions

An explicit solution has the dependent variable isolated, as in $y(x) = Ce^{-x}.$ An implicit solution is a relation between the variables. For example:

$$y^2-x^2 = C$$

is an implicit solution of $yy' = x.$ Differentiation with respect to $x$ gives $2yy'-2x = 0,$ which is equivalent to the differential equation. Solving for $y$ gives separate explicit branches, each defined only on intervals where the chosen [square root](../radicals/) is defined.

For many differential equations, the solutions cannot be expressed in elementary functions. The main questions then concern existence, uniqueness, qualitative behavior, stability, and numerical approximation. Methods such as [Euler's method](../euler-method/) give approximate values from an initial condition. Qualitative analysis gives information about the solutions without a closed formula. For a linear equation with analytic coefficients, a [power series](../power-series/) may give a local representation of a solution.
