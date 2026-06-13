---
title: Partial Derivatives
source: https://algebrica.org/partial-derivatives/
license: CC BY-NC 4.0
tags:
  - gradient
  - hessian-matrix
  - jacobian-matrix
  - multivariable-calculus
  - partial-derivatives
  - schwarz-theorem
---
## Definition

Partial derivatives generalise the concept of the [derivative](../derivatives/) to functions of several real variables. For a [function](../functions/) of a single variable, the derivative quantifies the rate of change of the function value along the sole available direction. In the context of multiple variables, it is necessary to specify the variable with respect to which the rate of change is computed, while holding all other variables constant. Formally:

+ Let $f : A \subseteq \mathbb{R}^n \to \mathbb{R}$ denote a function defined on an open set $A$.
+ Let $x_0 = (x_1^0, \ldots, x_n^0) \in A$ be a fixed point.

The partial derivative of $f$ with respect to the variable $x_i$ at $x_0$ is defined as the following limit:

$$\frac{\partial f}{\partial x_i}(x_0) = \lim_{h \to 0} \frac{f(x_1^0, \ldots, x_i^0 + h, \ldots, x_n^0) - f(x_0)}{h}$$

This definition applies whenever the [limit](../limits/) exists and is finite. In such cases, $f$ is said to be partially differentiable with respect to $x_i$ at $x_0$.

The notation is analogous to that of the ordinary derivative:

$$f'(c) = \lim_{h \to 0} \frac{f(c+h) - f(c)}{h}$$

For the partial derivative the symbol $\partial$ indicates that only one coordinate is varied. Common alternative notations include $\partial_{x_i} f(x_0)$ and $f_{x_i}(x_0)$. From a computational perspective, evaluating $\partial f/\partial x_i$ involves differentiating $f$ with respect to $x_i$ using standard calculus rules, while treating all other variables as constants.

- - -

Consider the setting $f : A \subseteq \mathbb{R}^2 \to \mathbb{R}$, where $A$ is open and $(x_0, y_0) \in A$. The two partial derivatives are defined as:

$$\frac{\partial f}{\partial x}(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0 + h, y_0) - f(x_0, y_0)}{h}$$

$$\frac{\partial f}{\partial y}(x_0, y_0) = \lim_{h \to 0} \frac{f(x_0, y_0 + h) - f(x_0, y_0)}{h}$$

Geometrically, $\frac{\partial f}{\partial x}(x_0, y_0)$ represents the slope of the curve formed by intersecting the graph of $f$ with the plane $y = y_0$, while $\frac{\partial f}{\partial y}(x_0, y_0)$ corresponds to the slope of the intersection with the plane $x = x_0$. Along each of these curves, $f$ becomes a function of a single real variable.

For example, consider the function of two variables:

$$f(x, y) = x^3 y^2 - \sin(xy)$$

Treating $y$ and $x$ as constants in turn yields:

$$
\begin{align}
\frac{\partial f}{\partial x} &= 3x^2 y^2 - y\cos(xy) \\[6pt]
\frac{\partial f}{\partial y} &= 2x^3 y - x\cos(xy)
\end{align}
$$

> The first expression results from differentiating $f$ with respect to $x$ while keeping $y$ constant. The second expression is obtained by differentiating with respect to $y$ while keeping $x$ constant. In both cases, the standard [differentiation rules](../differentiation-rules/), such as the power rule and the [chain rule](../chain-rule/), apply as they do in the single-variable context.

## Example 1

To illustrate the process of partial differentiation, consider a function of three variables instead of two. The inclusion of an additional variable does not introduce conceptual complexity and the procedure remains unchanged. This example clarifies how each variable is treated independently, with the remaining variables regarded as constants. For example, let us compute the partial derivatives of the following function:

$$f(x, y, z) = e^{x^2 z} \ln(1 + y^2 z)$$

Differentiation with respect to $x$ is straightforward. Here, $y$ and $z$ are treated as constants, so $\ln(1 + y^2 z)$ factors out, and the chain rule is applied to $e^{x^2 z}$ with the inner function $x^2 z$:

$$\frac{\partial f}{\partial x} = 2xze^{x^2 z} \ln(1 + y^2 z)$$

The derivative with respect to $y$ follows a similar structure but operates on the other factor. In this case, $e^{x^2 z}$ serves as the constant multiplier, and the chain rule is applied to $\ln(1 + y^2 z)$ with the inner function $1 + y^2 z$:

$$\frac{\partial f}{\partial y} = \frac{2yze^{x^2 z}}{1 + y^2 z}$$

The derivative with respect to $z$ is the most complex of the three cases. Since neither factor is constant in $z$, the product rule must be applied. The exponential term $e^{x^2 z}$ yields $x^2 e^{x^2 z}$ as its derivative, while $\ln(1 + y^2 z)$ yields $\frac{y^2}{1 + y^2 z}$:

$$\frac{\partial f}{\partial z} = x^2 e^{x^2 z} \ln(1 + y^2 z) + \frac{y^2 e^{x^2 z}}{1 + y^2 z}$$

## Higher-order partial derivatives

If the partial derivatives are differentiable functions on $A$, they can be further differentiated with respect to any variable $x_j$, resulting in second-order partial derivatives, in analogy with the [higher-order derivatives](../higher-order-derivatives/) of functions of a single variable. For a function of two variables $f(x, y)$, there are four possible second-order partial derivatives:

$$\frac{\partial^2 f}{\partial x^2} \qquad \frac{\partial^2 f}{\partial y^2} \qquad \frac{\partial^2 f}{\partial y \ \partial x} \qquad \frac{\partial^2 f}{\partial x \ \partial y}$$

The last two are called mixed partial derivatives. They differ in the sequence of differentiation:

+ In $\dfrac{\partial^2 f}{\partial y \ \partial x}$, differentiation is first performed with respect to $x$, followed by differentiation with respect to $y$.
+ In $\dfrac{\partial^2 f}{\partial x \ \partial y}$, the order of differentiation is reversed, with differentiation first performed with respect to $y$, then with respect to $x$.

- - -

Consider the function $f(x, y) = x^3 \sin(xy)$ in order to compute all four second-order partial derivatives. Begin by determining the first-order partial derivatives:

$$
\begin{align}
\frac{\partial f}{\partial x} &= 3x^2 \sin(xy) + x^3 y \cos(xy) \\[6pt]
\frac{\partial f}{\partial y} &= x^4 \cos(xy)
\end{align}
$$

The four second-order derivatives are obtained by differentiating each first-order derivative with respect to the relevant variable. Differentiating $\frac{\partial f}{\partial x}$ with respect to $x$ requires application of the product rule twice:

$$
\begin{align}
\frac{\partial^2 f}{\partial x^2} &= 6x \sin(xy) + 3x^2 y \cos(xy) + 3x^2 y \cos(xy) - x^3 y^2 \sin(xy) \\[6pt]
&= 6x \sin(xy) + 6x^2 y \cos(xy) - x^3 y^2 \sin(xy)
\end{align}
$$

Differentiating $\frac{\partial f}{\partial y}$ with respect to $y$ is more straightforward due to the simpler structure:

$$\frac{\partial^2 f}{\partial y^2} = -x^5 \sin(xy)$$

For the mixed derivatives, differentiating $\frac{\partial f}{\partial x}$ with respect to $y$ yields:

$$
\begin{align}
\frac{\partial^2 f}{\partial y \ \partial x} &= 3x^2 \cdot x\cos(xy) + x^3 \cos(xy) - x^3 y \cdot x \sin(xy) \\[6pt]
&= 4x^3 \cos(xy) - x^4 y \sin(xy)
\end{align}
$$

Similarly, differentiating $\frac{\partial f}{\partial y}$ with respect to $x$ yields:

$$\frac{\partial^2 f}{\partial x \ \partial y} = 4x^3 \cos(xy) - x^4 y \sin(xy)$$

## Schwarz's theorem

Schwarz's theorem addresses whether the order of differentiation affects the computation of mixed partial derivatives. A fundamental result in analysis establishes that, under appropriate regularity conditions, the order does not matter. Specifically, the Schwarz theorem states the following.

Let $f : A \subseteq \mathbb{R}^2 \to \mathbb{R}$ be a function for which the mixed partial derivatives exist on $A$ and are [continuous](../continuous-functions/) at a point $(x_0, y_0) \in A$. Then these mixed derivatives are equal at that point:

$$\frac{\partial^2 f}{\partial y \ \partial x}(x_0, y_0) = \frac{\partial^2 f}{\partial x \ \partial y}(x_0, y_0)$$

- - -

Continuity of the mixed partial derivatives is the essential hypothesis in Schwarz's theorem. There are functions for which both mixed derivatives exist but are [discontinuous](../discontinuities-of-real-functions/), resulting in different values at certain points. A classical counterexample is provided below.

$$f(x,y) = \begin{cases} xy\dfrac{x^2 - y^2}{x^2 + y^2} & (x,y) \neq (0,0) \\[8pt] 0 & (x,y) = (0,0) \end{cases}$$

Both mixed partial derivatives exist at the origin and can be computed directly from their definitions. To compute $\frac{\partial^2 f}{\partial y \ \partial x}(0,0)$, first evaluate:

$$
\begin{align}
\frac{\partial f}{\partial x}(0,y) &= \lim_{h \to 0} \frac{f(h,y) - f(0,y)}{h} \\[6pt]
&= \lim_{h \to 0} \frac{hy\dfrac{h^2 - y^2}{h^2 + y^2}}{h} \\[6pt]
&= \lim_{h \to 0} y\frac{h^2 - y^2}{h^2 + y^2} \\[6pt]
&= -y
\end{align}
$$

Next, differentiating with respect to $y$ at the origin:

$$\frac{\partial^2 f}{\partial y \ \partial x}(0,0) = \frac{\partial}{\partial y}(-y)\bigg|_{y=0} = -1$$

A similar calculation in the reverse order yields:

$$\frac{\partial f}{\partial y}(x,0) = x \qquad \frac{\partial^2 f}{\partial x \ \partial y}(0,0) = \frac{\partial}{\partial x}(x)\bigg|_{x=0} = +1$$

Therefore, the two mixed derivatives take opposite values at the origin, confirming that the conclusion of Schwarz's theorem does not hold when the continuity hypothesis is not satisfied:

$$\frac{\partial^2 f}{\partial y \ \partial x}(0,0) = -1 \neq +1 = \frac{\partial^2 f}{\partial x \ \partial y}(0,0)$$

## Gradient

If $f : A \subseteq \mathbb{R}^n \to \mathbb{R}$ is partially differentiable with respect to each variable at a point $x_0 \in A$, the collection of all partial derivatives forms a [vector](../vectors/) known as the gradient of $f$ at $x_0$. This gradient is denoted by $\nabla f(x_0)$ or $\mathrm{grad}\ f(x_0)$:

$$\nabla f(x_0) = \left( \frac{\partial f}{\partial x_1}(x_0), \frac{\partial f}{\partial x_2}(x_0), \ldots, \frac{\partial f}{\partial x_n}(x_0) \right) \in \mathbb{R}^n$$

The gradient is fundamental in multivariable analysis, providing the optimal linear approximation to the variation of $f$ near $x_0$, and its direction indicates the direction of steepest ascent. The precise meaning of this linear approximation is clarified in the definition of differentiability below.

> This geometric property is also the foundation of gradient descent, the iterative optimization algorithm widely used in machine learning to minimize loss functions by moving in the direction opposite to the gradient.

## Existence of partial derivatives and continuity

The existence of all partial derivatives at a point is a weaker condition than it may appear, since it does not even guarantee that the function is [continuous](../continuous-functions/) at that point. Each partial derivative records the behaviour of $f$ along a single coordinate direction, so a function can be regular along every axis while behaving irregularly along other directions. A standard example is the following.

$$f(x,y) = \begin{cases} \dfrac{xy}{x^2 + y^2} & (x,y) \neq (0,0) \\[8pt] 0 & (x,y) = (0,0) \end{cases}$$

Both partial derivatives exist at the origin, because $f$ vanishes identically along the two coordinate axes. Evaluating the limits directly gives:

$$\frac{\partial f}{\partial x}(0,0) = \lim_{h \to 0} \frac{f(h,0) - f(0,0)}{h} = 0, \qquad \frac{\partial f}{\partial y}(0,0) = 0$$

The function is nevertheless not continuous at the origin. Approaching along the line $y = mx$ yields:

$$f(x, mx) = \frac{x\cdot mx}{x^2 + m^2 x^2} = \frac{m}{1 + m^2}$$

The value obtained depends on the slope $m$, so $f$ admits no [limit](../limits/) at the origin and cannot be continuous there. This shows that partial differentiability does not imply continuity, which motivates the stronger notion introduced below.

## Differentiability and the total differential

The existence of partial derivatives at a point does not, in general, ensure differentiability. Differentiability is a stronger condition that requires the function to admit a linear approximation at the given point. A function $f : A \subseteq \mathbb{R}^n \to \mathbb{R}$ is differentiable at $x_0 \in A$ if there exists a linear map $L : \mathbb{R}^n \to \mathbb{R}$ such that:

$$\lim_{h \to 0} \frac{f(x_0 + h) - f(x_0) - L(h)}{|h|} = 0$$

The linear map $L$ is uniquely determined and takes the form:

$$L(h) = \nabla f(x_0) \cdot h$$

Differentiability implies that in a neighbourhood of $x_0$, the function admits the following expansion:

$$f(x_0 + h) = f(x_0) + \nabla f(x_0) \cdot h + o(|h|)$$

In this formula $o(|h|)$ denotes a term that vanishes faster than $|h|$ as $h \to 0$. The linear map $h \mapsto \nabla f(x_0) \cdot h$ is called the total differential of $f$ at $x_0$, in analogy with the [differential of a function](../differential-of-a-function/) of a single variable.

Differentiability is therefore stronger than both continuity and the existence of partial derivatives. A function differentiable at $x_0$ is automatically continuous at $x_0$ and admits all partial derivatives there, while neither of these two weaker properties implies differentiability in return.

## Jacobian matrix

Consider a function that takes vector values, specifically $f : A \subseteq \mathbb{R}^n \to \mathbb{R}^m$ with $f = (f_1, \ldots, f_m)$. The partial derivative of each component $f_k$ with respect to each variable $x_j$ can be computed. The Jacobian matrix of $f$ at $x_0$ organises this information and is defined as the $m \times n$ [matrix](../matrices/):

$$J_{f}(x_0) = \begin{pmatrix} \dfrac{\partial f_1}{\partial x_1}(x_0) & \cdots & \dfrac{\partial f_1}{\partial x_n}(x_0) \\[10pt] \vdots & \ddots & \vdots \\[4pt] \dfrac{\partial f_m}{\partial x_1}(x_0) & \cdots & \dfrac{\partial f_m}{\partial x_n}(x_0) \end{pmatrix}$$

The $k$-th row of $J_{f}(x_0)$ corresponds to the gradient $\nabla f_k(x_0)$. When $m = 1$, the Jacobian matrix reduces to a row vector, which is equivalent to the gradient of $f$.

## Directional derivatives

The partial derivative with respect to $x_i$ represents a specific instance of the broader concept of the directional derivative, taken in the direction of the $i$-th canonical basis vector $e_i$. For any unit vector $v \in \mathbb{R}^n$ with $|v| = 1$, the directional derivative of $f$ at $x_0$ in the direction of $v$ is defined as follows:

$$D_{v} f(x_0) = \lim_{t \to 0} \frac{f(x_0 + tv) - f(x_0)}{t}$$

When $f$ is differentiable at $x_0$, the following formula holds:

$$D_{v} f(x_0) = \nabla f(x_0) \cdot v = \sum_{i=1}^n \frac{\partial f}{\partial x_i}(x_0)v_i$$

The dot represents the Euclidean inner product on $\mathbb{R}^n$. Selecting $v = e_i$ yields $\frac{\partial f}{\partial x_i}(x_0)$, which aligns with the original definition of the partial derivative. This formula is valid only when $f$ is differentiable at $x_0$, rather than when only the partial derivatives exist.

## The chain rule in multivariable calculus

The [chain rule](../chain-rule/) for composite functions is fundamental in multivariable analysis. Suppose $g : U \subseteq \mathbb{R}^k \to \mathbb{R}^n$ is differentiable at $t_0 \in U$, and $f : A \subseteq \mathbb{R}^n \to \mathbb{R}$ is differentiable at $x_0 = g(t_0) \in A$. The composite function $h = f \circ g$ is then differentiable at $t_0$, and its partial derivative with respect to $t_j$ is given by:

$$\frac{\partial h}{\partial t_j}(t_0) = \sum_{i=1}^n \frac{\partial f}{\partial x_i}(x_0)\frac{\partial g_i}{\partial t_j}(t_0)$$

In matrix notation, this relationship can be expressed as:

$$J_h(t_0) = J_f(x_0)J_g(t_0)$$

This formula represents the product of the Jacobian matrices in the correct order. In the particular case where $k = 1$ and $g(t)$ defines a curve, the formula reduces to the standard derivative of $h(t) = f(g(t))$:

$$\frac{d}{dt} f(g(t))\bigg|_{t=t_0} = \nabla f(g(t_0)) \cdot g'(t_0)$$

## Classes of regularity

A function $f$ is said to be of class $C^1$ on an open set $A$, denoted $f \in C^1(A)$, if all first-order partial derivatives exist and are continuous on $A$. More generally, $f \in C^k(A)$ if all partial derivatives up to order $k$ exist and are continuous on $A$. The notation $f \in C^\infty(A)$ indicates that $f \in C^k(A)$ for every $k \geq 1$.

+ Functions of class $C^1$ possess a significant property, namely that continuity of the partial derivatives ensures differentiability. Specifically, if $f \in C^1(A)$, then $f$ is differentiable at every point of $A$. However, this condition is sufficient but not necessary, as there exist differentiable functions whose partial derivatives are not continuous.
+ For functions of class $C^2$, Schwarz's theorem applies automatically because the required continuity is assumed. Consequently, the equality of mixed partial derivatives holds throughout $A$.

## The Hessian matrix

Given a function $f : A \subseteq \mathbb{R}^n \to \mathbb{R}$ of class $C^2$ defined on an open set $A$, the second-order partial derivatives may be arranged into a single square matrix. The Hessian matrix of $f$ at a point $x_0 \in A$ is the $n \times n$ symmetric matrix defined as follows:

$$H_f(x_0) = \begin{pmatrix} \dfrac{\partial^2 f}{\partial x_1^2}(x_0) & \cdots & \dfrac{\partial^2 f}{\partial x_1 \ \partial x_n}(x_0) \\[10pt] \vdots & \ddots & \vdots \\[4pt] \dfrac{\partial^2 f}{\partial x_n \ \partial x_1}(x_0) & \cdots & \dfrac{\partial^2 f}{\partial x_n^2}(x_0) \end{pmatrix}$$

The entry in position $(j, k)$ is given by:

$$\frac{\partial^2 f}{\partial x_j \ \partial x_k}(x_0)$$

Because $f \in C^2(A)$, Schwarz's theorem ensures that all mixed partial derivatives are equal, so the Hessian is symmetric:

$$H_f(x_0) = H_f(x_0)^T$$

The Hessian is fundamental in the second-order analysis of $f$. At a critical point $x_0$ where $\nabla f(x_0) = 0$, the definiteness of $H_f(x_0)$ determines the character of the point: if $H_f(x_0)$ is positive definite, then $x_0$ is a local minimum; if negative definite, a local maximum; if indefinite, a saddle point. This result generalises the second derivative test to functions of several variables, as discussed in the entry on [maximum, minimum, and inflection points](../maximum-minimum-and-inflection-points/).
