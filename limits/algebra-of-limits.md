---
title: Algebra of Limits
source: https://algebrica.org/algebra-of-limits/
license: CC BY-NC 4.0
tags:
  - algebra-of-limits
  - continuous-functions
  - indeterminate-forms
  - limits
  - remarkable-limits
---
## Limit of a sum

As we saw in its definition, a [limit](../limits/) describes the behavior of a function 𝑓(𝑥) as 𝑥 approaches a point $x_0.$ Beyond evaluating limits by substitution or using techniques for resolving [indeterminate forms](../indeterminate-forms/), most problems require operations that allow us to rewrite the original expressions in simpler forms through the algebra of limits. To approach the problem, let $L$ and $M$ be two [real numbers](../real-numbers/) for which the following identities hold:

$$
\begin{align}
\lim_{x \to x_0} f(x) &= L \notag \\[6pt]
\lim_{x \to x_0} g(x) &= M \tag{1}
\end{align}
$$

Using $(1),$ we begin by examining the limit of the sum of two functions that approach finite values near a given point. In simple terms, if $f$ tends to $L$ and $g$ to $M,$ the limit of the sum equals the sum of the limits, and we have:

$$\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M \tag{2}$$

To prove $(2),$ fix $\varepsilon \gt 0;$ by $(1),$ when $x$ is sufficiently close to $x_0$ and $x \neq x_0,$ both deviations $|f(x)-L|$ and $|g(x)-M|$ are less than $\varepsilon/2.$ The [triangle inequality](../complex-number-fundamental-inequalities/) gives:

$$|f(x)+g(x)-(L+M)| \leq |f(x)-L|+|g(x)-M| \lt \varepsilon \tag{3}$$

Equation $(3)$ therefore shows that the sum tends to $L+M.$ As an example of rule $(2),$ consider the following functions

$$
\begin{align}
f(x) &= \frac{\sin x}{x} \notag \\[6pt]
g(x) &= \frac{1 - \cos x}{x^2} \tag{4}
\end{align}
$$

We now evaluate the following limits, obtaining two finite values:

$$
\begin{align}
&\lim_{x \to 0} \frac{\sin x}{x} = 1 \notag \\[6pt]
&\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2} \tag{5}
\end{align}
$$

Thus, using the values found in $(5)$ and applying rule $(2),$ we obtain precisely that the limit of the sum equals the sum of the limits:

$$\lim_{x \to 0} \left(\frac{\sin x}{x}+\frac{1-\cos x}{x^2}\right) = 1 + \frac{1}{2} = \frac{3}{2} \tag{6}$$

The sum rule $(2)$ also extends to the limit of a difference. Under the assumptions in $(1),$ we have:

$$\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M \tag{7}$$

Indeed, if $g(x)$ tends to $M,$ then $-g(x)$ tends to $-M,$ and applying $(2)$ gives $(7).$ As an example, consider the following functions:

$$
\begin{align}
f(x) &= \frac{x^2-1}{x-1} \notag \\[6pt]
g(x) &= \frac{x^3-1}{x-1} \tag{8}
\end{align}
$$

The functions in $(8)$ are undefined at $x=1,$ but to evaluate their limits we only need to consider values with $x\neq1,$ for which the factor $x-1$ can be canceled. The numerators are a [difference of two squares](../notable-products/) and a [difference of two cubes](../notable-products/), respectively, which we can therefore factor as follows:

$$
\begin{align}
\lim_{x \to 1} \frac{x^2-1}{x-1} &= \lim_{x \to 1}\frac{(x-1)(x+1)}{x-1} \notag \\[6pt]
\lim_{x \to 1} \frac{x^3-1}{x-1} &= \lim_{x \to 1}\frac{(x-1)(x^2+x+1)}{x-1} \tag{9}
\end{align}
$$

From $(9),$ we obtain the following limits:

$$
\begin{align}
&\lim_{x \to 1}(x+1) = 2 \notag \\[6pt]
&\lim_{x \to 1}(x^2+x+1) = 3 \tag{10}
\end{align}
$$

Applying $(7)$ with the limits found in $(10),$ we obtain:

$$\lim_{x \to 1} \left(\frac{x^2-1}{x-1}-\frac{x^3-1}{x-1}\right) = 2-3 = -1 \tag{11}$$

We have therefore shown that the limit of the difference is precisely the difference of the two limits.

## Limit of a product

In addition to the sum and difference rules, if $f(x)$ tends to a finite value $L,$ as in $(1),$ the following relation holds for every real constant $c:$

$$\lim_{x \to x_0} c f(x) = c L \tag{12}$$

For $c=0,$ the proof is trivial because the product is zero. When $c \neq 0,$ the following linear relation holds:

$$|cf(x)-cL|=|c||f(x)-L|$$ 
Thus, taking a limit is also a linear operation. As an example, we evaluate the following limit:

$$\lim_{x \to 0} 3\frac{\ln(1+x)}{x} \tag{13}$$

Direct substitution leaves the quotient undefined at $x=0,$ but $(13)$ involves the following [standard limit](../remarkable-limits/):

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1 \tag{13}$$

Applying $(12)$ with $c=3$ and using the limit obtained in $(13),$ we get:

$$\lim_{x \to 0} 3\frac{\ln(1 + x)}{x} = 3\lim_{x \to 0}\frac{\ln(1 + x)}{x} = 3 \cdot 1 = 3 \tag{14}$$

We now consider the case in which both factors are functions with finite limits, as assumed in $(1),$ and evaluate the limit of their product, which equals the product of their respective limits:

$$\lim_{x \to x_0} \big(f(x)g(x)\big) = LM \tag{15}$$

To prove $(15),$ we rewrite the deviation from $LM$ and apply the triangle inequality to obtain:

$$|f(x)g(x)-LM| \leq |f(x)||g(x)-M|+|M||f(x)-L| \tag{16}$$

Since $f(x)$ tends to a finite value, it is [bounded](../theorems-on-limits/) near $x_0,$ and by $(1)$ both deviations in $(16)$ tend to zero, so the product tends to $LM.$ For example, consider the following functions:

$$
\begin{align}
&f(x) = \frac{e^x-1}{x} \notag \\[6pt]
&g(x) = \frac{\ln(1+x)}{x} \tag{17}
\end{align}
$$

The functions in $(17)$ are undefined at $x=0,$ but their limits are standard limits (the second was given in $(13)$):

$$
\begin{align}
&\lim_{x \to 0} \frac{e^x-1}{x} = 1 \notag \\[6pt]
&\lim_{x \to 0} \frac{\ln(1+x)}{x} = 1 \tag{18}
\end{align}
$$

Applying $(15)$ with the values in $(18),$ we obtain the general rule in $(15):$

$$\lim_{x \to 0} \frac{(e^x-1)\ln(1+x)}{x^2} = 1 \cdot 1 = 1 \tag{19}$$

## Limit of a quotient

We now consider the limit of a quotient, for which the following relation holds under the assumptions in $(1):$

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}\tag{20}$$

In $(20),$ M and $g(x)$ must be nonzero. In particular, the first condition ensures that, for $x$ sufficiently close to $x_0$ and distinct from $x_0,$ the following bound holds:

$$|g(x)| \gt |M|/2$$

The denominator is therefore nonzero, and the deviation of its reciprocal satisfies the following chain of relations:

$$\left|\frac{1}{g(x)}-\frac{1}{M}\right| = \frac{|g(x)-M|}{|g(x)||M|} \leq \frac{2}{|M|^2}|g(x)-M| \tag{21}$$

By $(1),$ the last expression in $(21)$ tends to zero, so $1/g(x)$ tends to $1/M.$ Applying the product rule $(15)$ then gives $(20).$ When $M=0,$ however, the rule does not apply and the quotient requires a separate analysis, as in the case of the indeterminate form $0/0.$ We therefore consider the following functions and evaluate the limit of their quotient:

$$
\begin{align}
f(x) = \frac{e^x-1}{x} &\notag \\[6pt]
g(x) = \frac{x^2+1}{x+1} &\tag{22}
\end{align}
$$

For $f,$ we use the standard limit already given in $(18).$ The function $g,$ on the other hand, is continuous at $x=0,$ so its limit can be evaluated by substitution. This gives:

$$
\begin{align}
&\lim_{x \to 0}\frac{e^x-1}{x} = 1 \notag \\[6pt]
&\lim_{x \to 0}\frac{x^2+1}{x+1} = \frac{0+1}{0+1} = 1 \tag{23}
\end{align}
$$

Applying $(20),$ we therefore obtain:

$$\lim_{x \to 0}\frac{\dfrac{e^x-1}{x}}{\dfrac{x^2+1}{x+1}} = \frac{1}{1} = 1 \tag{24}$$


## Limits of powers and polynomials

The product rule in $(15)$ also allows us to evaluate the limit of a power. Under the same assumptions in $(1),$ for every positive integer $n$ we have:

$$\lim_{x \to x_0}\big(f(x)\big)^n = L^n \tag{25}$$

To prove $(25),$ the case $n=1$ is precisely the assumption on the limit of $f;$ each step from $n$ to $n+1$ follows by applying the product rule $(15)$ to $f(x)^n$ and $f(x).$ Combining $(25)$ with the sum rule $(2)$ and the constant multiple rule $(12)$ then gives the limit of a [polynomial](../polynomials/) $P(x):$

$$\lim_{x \to x_0}P(x) = a_0+a_1x_0+\cdots+a_nx_0^n = P(x_0) \tag{26}$$

As an example of the power rule, we evaluate the following limit:

$$\lim_{x \to 0}\left(\frac{\ln(1+2x)}{x}\right)^4 \tag{27}$$

We proceed step by step, first evaluating the limit of the base by multiplying the numerator and denominator by $2$ and setting $t=2x,$ so that $t \to 0$ as $x \to 0.$ Using $(12)$ and the standard limit already given in $(18),$ we obtain:

$$
\begin{align}
\lim_{x \to 0}\frac{\ln(1+2x)}{x}
&= \lim_{x \to 0}\frac{2\ln(1+2x)}{2x} \notag \\[6pt]
&= 2\lim_{x \to 0}\frac{\ln(1+2x)}{2x} \notag \\[6pt]
&= 2\lim_{t \to 0}\frac{\ln(1+t)}{t} \notag \\[6pt]
&= 2 \cdot 1 = 2 \tag{28}
\end{align}
$$

The base therefore tends to $2,$ and applying $(25)$ with $n=4$ gives:

$$\lim_{x \to 0}\left(\frac{\ln(1+2x)}{x}\right)^4 = \left(\lim_{x \to 0}\frac{\ln(1+2x)}{x}\right)^4 = 2^4 = 16 \tag{29}$$

## Limit of a composition

We now examine the limit of a [composition of functions](../composite-functions/) of the form $\varphi(f(x)).$ In this case, if $f(x)$ tends to the finite value $L,$ as in $(1),$ and $\varphi$ is continuous at $L,$ the following relation holds:

$$\lim_{x \to x_0}\varphi(f(x)) = \varphi\left(\lim_{x \to x_0}f(x)\right) = \varphi(L) \tag{30}$$

To prove $(30),$ we assume that the composition is defined for $x$ sufficiently close to $x_0$ with $x \neq x_0.$ [Continuity](../continuous-functions/) at $L$ ensures that, as $f(x)$ tends to $L,$ the value $\varphi(f(x))$ tends to $\varphi(L).$ To illustrate $(30)$ in practice, we evaluate the following limit:

$$\lim_{x \to 0}e^{\frac{\sqrt{1+x}-1}{x}} \tag{31}$$

First, we identify the two functions separately:

$$
\begin{align}
f(x) &= \frac{\sqrt{1+x}-1}{x} \notag \\[6pt]
\varphi(t) &= e^t \tag{32}
\end{align}
$$

We first evaluate the limit of $f(x),$ obtaining:

$$
\begin{align}
\lim_{x \to 0}\frac{\sqrt{1+x}-1}{x}
&= \lim_{x \to 0}\frac{(\sqrt{1+x}-1)(\sqrt{1+x}+1)}{x(\sqrt{1+x}+1)} \notag \\[6pt]
&= \lim_{x \to 0}\frac{x}{x(\sqrt{1+x}+1)} \notag \\[6pt]
&= \lim_{x \to 0}\frac{1}{\sqrt{1+x}+1} = \frac{1}{2} \tag{33}
\end{align}
$$

The [exponential function](../exponential-function/) is continuous at $t=1/2,$ so:

$$\lim_{t \to 1/2}e^t = e^{1/2} \tag{34}$$

Since the inner function in $(33)$ tends to $1/2,$ applying the composition rule $(30)$ gives:

$$\lim_{x \to 0}e^{\frac{\sqrt{1+x}-1}{x}} = e^{1/2} = \sqrt{e} \tag{35}$$

## Summary

The table summarizes the rules proved under the assumptions in $(1).$ For the quotient, we require $M \neq 0,$ as in $(20).$ For the power, $n$ is a positive integer, as in $(25),$ while for the composition, $\varphi$ must be continuous at $L$ and defined at the values taken by $f$ near $x_0,$ as in $(30).$

[class="table-1"]

|                       |                                                            |
| --------------------- | ---------------------------------------------------------- |
| Sum                 | $\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M$         |
| Difference            | $\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M$         |
| Constant multiple | $\lim_{x \to x_0} c f(x) = c L$                            |
| Product of functions  | $\lim_{x \to x_0} \big( f(x) \cdot g(x) \big) = L \cdot M$ |
| Quotient             | $\lim_{x \to x_0} \dfrac{f(x)}{g(x)} = \dfrac{L}{M}$       |
| Power               | $\lim_{x \to x_0} \big( f(x) \big)^n = L^n$                |
| Composition          | $\lim_{x \to x_0} \varphi(f(x)) = \varphi(L)$              |
[/class]

If one of the limits is infinite or the denominator of a quotient tends to zero, a separate analysis is needed because the assumptions of the stated rules no longer hold, and in some cases we may obtain indeterminate forms, which are discussed in a separate entry.
