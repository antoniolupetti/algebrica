---
title: L'Hopital's Rule
source: https://algebrica.org/hopital-rule/
license: CC BY-NC 4.0
tags:
  - derivatives
  - differential-calculus-theorems
  - hopital-rule
  - indeterminate-forms
  - limits
---

## Evaluating limits involving indeterminate forms

L'Hôpital's rule is a very useful method that allows us to evaluate certain [limits](../limits/) involving [indeterminate forms](../indeterminate-forms/) of the type $0/0$ or $\infty/\infty$ with ease. Informally, under certain conditions, the theorem underlying the formula states that the limit of the quotient of two functions equals the limit of the quotient of their respective [derivatives](../derivatives/). In some cases, this step eliminates the indeterminate form and allows us to evaluate the limit by direct substitution or with a few algebraic manipulations. Keep in mind that this transformation does not always simplify the calculation, because the quotient of the derivatives may itself yield an indeterminate form. In that situation, if the hypotheses of the theorem still hold, we can apply the rule again or use another method.

To illustrate the theorem, consider two [functions](../functions/) $f$ and $g$ defined on an [open neighbourhood](../topology-of-the-real-line/) $I$ containing $x_0,$ except possibly at $x_0$ itself, and consider the limit of their quotient:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} \tag{1}$$

Substituting $x_0$ into the quotient in $(1)$ gives one of the following indeterminate forms, which tells us nothing about the value or existence of the limit:

$$\frac{0}{0} \quad \frac{\infty}{\infty}$$

Suppose that the following conditions hold for $(1):$

+ $f$ and $g$ are differentiable at every point of $I$ other than $x_0.$
+ The derivative $g'(x)$ is nonzero for every $x \in I$ with $x \neq x_0.$
+ In the $0/0$ case, we have $\displaystyle \lim_{x \to x_0} f(x) = \lim_{x \to x_0} g(x) = 0;$ in the $\infty/\infty$ case, each function tends to $+\infty$ or $-\infty$ as $x \to x_0.$
+ The following limit of the quotient of the derivatives of $f$ and $g$ exists, either finite or infinite:

$$\lim_{x \to x_0} \frac{f'(x)}{g'(x)} \tag{2}$$

Under these hypotheses, the limit of the quotient of the functions also exists, and the following equality holds:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)} \tag{3}$$

Note that in $(3)$ the numerator and denominator are differentiated separately, so the [quotient rule for derivatives](../differentiation-rules/) must not be applied.

- - -

An important consideration is the existence of the limit of the quotient of the derivatives. If this limit does not exist, the theorem gives no conclusion about the original limit in $(1).$ Consider, for example, the functions $f(x) = x + \sin x$ and $g(x) = x.$ As $x$ tends to $\infty,$ their quotient tends to one, since:

$$\lim_{x \to +\infty} \frac{f(x)}{g(x)} = \lim_{x \to +\infty} \left(1 + \frac{\sin x}{x}\right) = 1$$

If we instead differentiate the numerator and denominator, we find that the quotient of their derivatives is $1 + \cos x,$ an oscillating expression with no limit at infinity. We can therefore conclude that, under the other hypotheses of the theorem, the existence of the limit of the quotient of the derivatives is sufficient, but not necessary, for the existence of the limit of the quotient of the functions.

## Proof of the $0/0$ case

We now prove rule $(3)$ when the limit in $(1)$ yields the indeterminate form $0/0.$ Since both $f(x)$ and $g(x)$ tend to zero, we can extend them continuously to $x_0$ by assigning each function the value of its limit:

$$f(x_0) = g(x_0) = 0\tag{4}$$

Fix $x \in I$ with $x > x_0.$ In this case, the denominator is nonzero. Indeed, if it were zero, $g$ would have the same value at both endpoints of $[x_0, x].$ Since it is [continuous](../continuous-functions/) on the closed interval and differentiable in its interior, [Rolle's theorem](../rolle-theorem/) would imply that its derivative vanishes at some interior point. This contradicts the hypothesis that $g'$ is nonzero at every point of $I$ other than $x_0.$ We can therefore conclude that $g(x) \neq 0$ and apply [Cauchy's theorem](../cauchy-theorem/) on $[x_0, x]$ to obtain a point $c \in (x_0, x)$ for which the following equality holds:

$$\frac{f(x) - f(x_0)}{g(x) - g(x_0)} = \frac{f'(c)}{g'(c)} \tag{5}$$

Since $(4)$ holds, $(5)$ becomes:

$$\frac{f(x)}{g(x)} = \frac{f'(c)}{g'(c)}$$

For every $x > x_0,$ Cauchy's theorem guarantees a point, denoted by $c(x),$ that satisfies:

$$x_0 < c(x) < x \tag{6}$$

Subtracting $x_0$ from all three terms in $(6)$ gives:

$$0 < c(x) - x_0 < x - x_0$$

For the right-hand limit, the distance $x - x_0$ tends to zero, so the distance $c(x) - x_0$ must also tend to zero. By the [squeeze theorem](../squeeze-theorem/), it follows that:

$$\lim_{x \to x_0^+} c(x) = x_0$$

For the left-hand limit, we apply Cauchy's theorem on $[x, x_0],$ where the point $c(x)$ satisfies:

$$x < c(x) < x_0$$

Subtracting each term from $x_0$ and reordering the inequalities gives:

$$0 < x_0 - c(x) < x_0 - x$$

As $x$ approaches $x_0$ from the left, the distance $x_0 - x$ tends to zero, so the distance $x_0 - c(x)$ also tends to zero. The squeeze theorem gives:

$$\lim_{x \to x_0^-} c(x) = x_0$$

We have therefore shown that $c(x)$ tends to $x_0$ as $x$ approaches from either side; we can now use the hypothesis that the limit in $(2)$ exists, denoting its value, finite or infinite, by $L:$

$$\lim_{x \to x_0} \frac{f'(x)}{g'(x)} = L$$

Since $c(x) \to x_0$ and $c(x) \neq x_0,$ we can write:

$$\lim_{x \to x_0} \frac{f'(c(x))}{g'(c(x))} = L$$

Return to equality $(5),$ obtained from Cauchy's theorem. By $(4),$ the values of the functions at $x_0$ are zero, so, denoting the intermediate point by $c(x),$ we have:

$$\frac{f(x)}{g(x)} = \frac{f'(c(x))}{g'(c(x))}$$

We have just shown that the quotient on the right tends to $L.$ Since the two quotients are equal, the one on the left also tends to $L,$ so:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = L$$

Replacing $L$ with the limit in $(2),$ we obtain precisely formula $(3),$ which we wanted to prove for the $0/0$ case:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)}$$

## Proof of the $\infty/\infty$ case

We now prove the theorem when $(1)$ yields the indeterminate form $\infty/\infty.$ In this case, we proceed as follows. Suppose that the limit in $(2)$ is a real number $L.$ Given $\varepsilon > 0,$ the definition of a limit allows us to choose $\delta > 0$ such that:

$$
\left| \frac{f'(t)}{g'(t)} - L \right| < \frac{\varepsilon}{2} \quad \forall \ t \in (x_0, x_0 + \delta)
$$

Fix a point $y \in (x_0, x_0 + \delta)$ and consider $x$ such that $x_0 < x < y.$ By [Cauchy's theorem](../cauchy-theorem/), a point $c \in (x, y)$ exists for which the following equality holds:

$$
\frac{f(x) - f(y)}{g(x) - g(y)} = \frac{f'(c)}{g'(c)} \tag{7}
$$

For $x$ sufficiently close to $x_0,$ both $f(x)$ and $g(x)$ are nonzero, and we can rewrite $(7)$ as follows:

$$
\frac{f(x)}{g(x)} \cdot \frac{1 - f(y)/f(x)}{1 - g(y)/g(x)} = \frac{f'(c)}{g'(c)}
$$

Now set:

$$
\begin{align}
A(x) &= \frac{1 - f(y)/f(x)}{1 - g(y)/g(x)} \\[6pt]
R(x) &= \frac{f'(c)}{g'(c)}
\end{align}
$$

Equation $(7)$ then becomes:

$$\frac{f(x)}{g(x)} = \frac{R(x)}{A(x)} \tag{8}$$

Since $c$ lies in the chosen neighbourhood, the initial estimate for the quotient of the derivatives also applies to $R(x).$ In addition, the [triangle inequality](../absolute-value/) gives an upper bound, so we can write:

$$
\begin{align}
|R(x) - L| &< \frac{\varepsilon}{2} \\[6pt]
|R(x)| &\leq |L| + |R(x) - L| < |L| + \frac{\varepsilon}{2}
\end{align}
$$

Since $|R(x)|$ is bounded and $1/A(x) - 1$ tends to zero, for $x$ sufficiently close to $x_0$ from the right we have:

$$|R(x)|\left|\frac{1}{A(x)} - 1\right| < \frac{\varepsilon}{2}$$

Using $(8),$ we obtain:

$$
\begin{align}
\left|\frac{f(x)}{g(x)} - L\right|
&= \left|R(x)\left(\frac{1}{A(x)} - 1\right) + R(x) - L\right| \\[6pt]
&\leq |R(x)|\left|\frac{1}{A(x)} - 1\right| + |R(x) - L| \\[6pt]
&< \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon
\end{align}
$$

This estimate shows that the quotient of the functions is as close to $L$ as we wish, provided that $x$ is sufficiently close to $x_0$ from the right. Since $L$ is the limit of the quotient of the derivatives, we have proved that:

$$\lim_{x \to x_0^+} \frac{f(x)}{g(x)} = \lim_{x \to x_0^+} \frac{f'(x)}{g'(x)} = L$$

This completes the proof of the rule for the $\infty/\infty$ form in the case of a right-hand limit with finite $L.$

> We have thus proved the result when $L$ is a finite real number. The same procedure can be adapted to $L = +\infty$ by showing that the quotient of the functions exceeds any prescribed positive number for $x$ sufficiently close to $x_0.$ The case $L = -\infty$ follows by changing the sign of $f,$ and analogous adjustments handle the left-hand limit and limits at infinity.

## Examples

The following examples show how L'Hôpital's rule can be used to evaluate limits involving indeterminate forms. As a first example, consider the [standard trigonometric limit](../remarkable-limits/):

$$\lim_{x \to 0} \frac{\sin x}{x}$$

Direct substitution shows that both the numerator and denominator tend to zero, giving the indeterminate form $0/0.$ First, we check whether L'Hôpital's rule applies. The functions in the numerator and denominator are differentiable in a neighbourhood of zero, and the derivative of the denominator equals $1$ (so it does not vanish). The quotient of the derivatives is $\cos x,$ which tends to $1.$ We have thus verified all the hypotheses and can apply the rule to obtain:

$$
\begin{align}
\lim_{x \to 0} \frac{\sin x}{x}
&= \lim_{x \to 0} \frac{(\sin x)'}{(x)'} \\[6pt]
&= \lim_{x \to 0} \frac{\cos x}{1} \\[6pt]
&= 1
\end{align}
$$

- - -

Now consider a difference of functions that yields the indeterminate form $\infty - \infty.$ The difference can be rewritten as a single quotient to reduce it to one of the forms to which the rule applies. We illustrate this with the following limit:

$$\lim_{x \to 0} \left(\frac{1}{\sin x} - \frac{2}{x}\right)$$

We can rewrite the expression whose limit we seek as:

$$\frac{1}{\sin x} - \frac{2}{x} = \frac{x - 2\sin x}{x \sin x}$$

The new quotient yields the form $0/0.$ The numerator and denominator are differentiable near zero, and the quotient of their derivatives is:

$$\frac{1 - 2\cos x}{\sin x + x\cos x}$$

For $0 < |x| < \pi/2,$ the terms $\sin x$ and $x\cos x$ have the same sign, so their sum does not vanish and the hypothesis on the derivative of the denominator is satisfied. The numerator tends to $-1,$ while the denominator tends to zero, and therefore:

$$
\lim_{x \to 0^+} \frac{1 - 2\cos x}{\sin x + x\cos x} = -\infty
$$

$$
\lim_{x \to 0^-} \frac{1 - 2\cos x}{\sin x + x\cos x} = +\infty
$$

We can therefore apply L'Hôpital's rule to each one-sided limit to obtain:

$$
\lim_{x \to 0^+} \left(\frac{1}{\sin x} - \frac{2}{x}\right) = -\infty
$$

$$
\lim_{x \to 0^-} \left(\frac{1}{\sin x} - \frac{2}{x}\right) = +\infty
$$

The one-sided limits are different, so the two-sided limit does not exist.

- - -

We now consider a case in which we compare algebraic manipulation with the transformation used in L'Hôpital's rule. Consider the following limit:

$$\lim_{x \to 1} \frac{\sqrt{x} - 1}{x^2 - 1} \tag{9}$$

Direct substitution gives the form $0/0.$ We first try to resolve it algebraically by [factoring the denominator](../notable-products/). We can rewrite $(9)$ as:

$$
\begin{align}
\lim_{x \to 1} \frac{\sqrt{x} - 1}{x^2 - 1}
&= \lim_{x \to 1} \frac{\sqrt{x} - 1}{(x + 1)(x - 1)} \\[6pt]
&= \lim_{x \to 1} \frac{\sqrt{x} - 1}{(x + 1)(\sqrt{x} - 1)(\sqrt{x} + 1)} \\[6pt]
&= \lim_{x \to 1} \frac{1}{(x + 1)(\sqrt{x} + 1)} \\[6pt]
&= \frac{1}{(1 + 1)(1 + 1)} = \frac{1}{4}
\end{align}
$$

In this case, the calculation using L'Hôpital's rule is shorter. To check that the hypotheses of the theorem hold, observe that:

+ the functions $f(x) = \sqrt{x} - 1$ and $g(x) = x^2 - 1$ are differentiable for $x > 0$
+ $g'(x) = 2x$ does not vanish in a neighbourhood of $1.$ 
+ The quotient of the derivatives is $1/(4x\sqrt{x}),$ which is continuous at $1$ and has limit $1/4.$ 

The hypotheses are therefore satisfied, so we apply $(3)$ to evaluate the limit in a single step:

$$
\begin{align}
\lim_{x \to 1} \frac{\sqrt{x} - 1}{x^2 - 1}
&= \lim_{x \to 1} \frac{\dfrac{1}{2\sqrt{x}}}{2x} \\[6pt]
&= \lim_{x \to 1} \frac{1}{4x\sqrt{x}} = \frac{1}{4}
\end{align}
$$

- - -

Now consider the following limit:

$$\lim_{x \to 0^+} x \ln x$$

The product yields the indeterminate form $0 \cdot (-\infty),$ which we can reduce to the form $\infty/\infty$ to apply L'Hôpital's rule:

$$\lim_{x \to 0^+} x \ln x = \lim_{x \to 0^+} \frac{\ln x}{\dfrac{1}{x}}$$

In this form, direct substitution gives a numerator tending to $-\infty$ and a denominator tending to $+\infty.$ Checking the hypotheses of the theorem, we find that both functions are differentiable for $x > 0,$ and the derivative of the denominator is $-1/x^2,$ which is nonzero. The quotient of the derivatives is $-x$ and tends to zero, so we apply the rule to evaluate the limit:

$$
\begin{align}
\lim_{x \to 0^+} \frac{\ln x}{\dfrac{1}{x}}
&= \lim_{x \to 0^+} \frac{(\ln x)'}{\left(\dfrac{1}{x}\right)'} \\[6pt]
&= \lim_{x \to 0^+} \frac{\dfrac{1}{x}}{-\dfrac{1}{x^2}} \\[6pt]
&= \lim_{x \to 0^+} (-x) = 0
\end{align}
$$

## Exponential indeterminate forms

L'Hôpital's rule can also be used to handle the following exponential indeterminate forms:

$$0^0 \qquad \infty^0 \qquad 1^\infty$$

The aim is to proceed as in the last example, reducing these expressions to a form of the type $0/0$ or $\infty/\infty.$ Consider, for example, the typical situation described by the following exponential expression:

$$y = f(x)^{g(x)} \tag{10}$$

Assuming that $f(x) > 0$ in the neighbourhood under consideration, we can take [logarithms](../logarithms/) and rewrite $(10)$ as follows:

$$\ln y = g(x)\ln f(x) \tag{11}$$

If, in addition, $g(x) \neq 0$ in the same neighbourhood, we can rewrite $(11)$ as a quotient to which we can apply L'Hôpital's rule:

$$\ln y = g(x)\ln f(x) = \frac{\ln f(x)}{\dfrac{1}{g(x)}} \tag{12}$$

At this point, if the hypotheses hold, we apply L'Hôpital's rule to $(12)$ to evaluate $L = \lim \ln y.$ If $L$ is finite, the continuity of the [exponential function](../exponential-function/) gives:

$$\lim f(x)^{g(x)} = e^L \tag{13}$$

Consider, for example:

$$\lim_{x \to 0^+} x^x$$

Both the base and the exponent tend to zero, so we obtain the indeterminate form $0^0.$ Setting $y = x^x,$ we have $\ln y = x\ln x.$ In the preceding section, we proved that:

$$\lim_{x \to 0^+} x\ln x = 0$$

Applying the exponential function, we obtain the limit from $(13):$

$$\lim_{x \to 0^+} x^x = e^0 = 1$$
