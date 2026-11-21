---
title: Indeterminate Forms
source: https://algebrica.org/indeterminate-forms/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - hopital-rule
  - indeterminate-forms
  - limits
  - taylor-series
---

## What are indeterminate forms

When calculating [limits](../limits/), we often encounter expressions whose limit cannot be determined directly, known as indeterminate forms; the complete list of these forms is given below:

$$
\begin{align}
&\frac{0}{0} \qquad \frac{\infty}{\infty} \qquad 0 \cdot \infty \qquad \infty - \infty \notag \\[6pt]
&1^{\infty} \qquad 0^{0} \qquad \infty^{0} \tag{1}
\end{align}
$$

In very simple terms, a form such as those in $(1)$ does not denote a specific number but indicates that direct substitution is not useful for calculating the limit in question. Suppose, for example, that we have two [functions](../functions/) $f(x)$ and $g(x)$ that both tend to zero as $x$ approaches $a$:

$$
\begin{align}
\lim_{x \to a} f(x) &= 0 \notag \\[6pt]
\lim_{x \to a} g(x) &= 0 \tag{2}
\end{align}
$$

If we tried to calculate the limit of their ratio by direct substitution, we would obtain an indeterminate result that tells us nothing about the behaviour of the limit:

$$\lim_{x \to a} \frac{f(x)}{g(x)} \to \frac{0}{0} \tag{3}$$

In $(3),$ the limit could be any finite number, zero, infinity, or might not exist at all, so when we encounter these forms we need to take a different approach, using the techniques listed below. Before analysing each form, remember that an indeterminate form such as those in $(1)$ neither represents a number nor expresses an equality, but is simply an indication that the behaviour of the limit needs to be investigated in another way.

## The form $\frac{0}{0}$

This is the indeterminate form most frequently encountered in exercises and typically appears when the numerator and denominator vanish at the same point. Sometimes it can be resolved by simplifying the expression through a few algebraic steps before calculating the limit. Consider, for example, the following limit:

$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} \tag{4}$$

In $(4),$ direct substitution of $x=2$ gives precisely $0/0,$ so we cannot draw any conclusion about the behaviour of the limit. We can, however, overcome this problem by factoring the numerator as a difference of two squares:

$$x^2 - 4 = (x - 2)(x + 2) \tag{5}$$

Substituting $(5)$ into $(4)$ and requiring $x \neq 2,$ we obtain:

$$
\begin{align}
&\lim_{x \to 2} \frac{(x - 2)(x + 2)}{x - 2} \notag \\[6pt]
& \lim_{x \to 2} (x + 2) = 2 + 2 = 4 \tag{6}
\end{align}
$$

In more advanced problems, [L'Hôpital's rule](../hopital-rule/) provides a systematic method for evaluating this type of limit, while other cases require [Taylor expansions](../limits-using-taylor-expansions/) or [little-o notation](../little-o-notation/) to isolate the leading term of the numerator and denominator. These techniques are developed in detail in their respective entries.

## The form $\dfrac{\infty}{\infty}$

We now examine how to handle this form, which arises when the numerator and denominator of a ratio diverge. Consider, for example, the following limit:

$$\lim_{x \to \infty} \frac{3 x^2 + 1}{2 x^2 - 5} \tag{7}$$

Here too, direct substitution leads to the indeterminate form $\infty/\infty,$ and, as in the previous example, we cannot say anything about the value of the limit. We can, however, try to evaluate $(7)$ through algebraic transformations, for example by factoring out the highest power of $x$ from the numerator and denominator, obtaining:

$$
\begin{align}
\frac{3 x^2 + 1}{2 x^2 - 5}
&= \frac{x^2 (3 + 1/x^2)}{x^2 (2 - 5/x^2)} \notag \\[6pt]
&= \frac{3 + 1/x^2}{2 - 5/x^2} \tag{8}
\end{align}
$$

As $x \to \infty,$ the terms $1/x^2$ and $5/x^2$ tend to zero, so the limit becomes:

$$\lim_{x \to \infty} \frac{3 x^2 + 1}{2 x^2 - 5} = \frac{3}{2}$$

In some circumstances, the same result can be obtained more quickly by applying L'Hôpital's rule repeatedly, but remember that once the method has been mastered, the procedure for evaluating the limit becomes fairly mechanical and reduces to a few straightforward steps.

## The form $0 \cdot \infty$

This form arises when the limit involves a product of two factors, one of which tends to zero while the other grows without bound. For example, consider the following limit:

$$\lim_{x \to +\infty} x\left(\sqrt{x^2 + 1} - x\right) \tag{9}$$

In $(9),$ the factor $x$ tends to $+\infty,$ while $\sqrt{x^2 + 1} - x$ tends to zero, because rationalising this difference gives $1/(\sqrt{x^2 + 1} + x).$ The product therefore has the form $0 \cdot \infty.$ Here too, we can use a simple algebraic trick, writing $x = 1/(1/x)$ and expressing $(9)$ as a quotient:

$$x\left(\sqrt{x^2 + 1} - x\right) = \frac{\sqrt{x^2 + 1} - x}{1/x} \tag{10}$$

In $(10),$ the numerator and denominator both tend to zero, so we obtain the form $0/0$ encountered earlier. In this case, we can rationalise the numerator and factor out $x$ from the denominator, bearing in mind that $x \gt 0,$ to obtain:

$$
\begin{align}
\frac{\sqrt{x^2 + 1} - x}{1/x}
&= \frac{(x^2 + 1) - x^2}{(1/x)\left(\sqrt{x^2 + 1} + x\right)} \notag \\[6pt]
&= \frac{1}{(1/x)x\left(\sqrt{1 + 1/x^2} + 1\right)} \notag \\[6pt]
&= \frac{1}{\sqrt{1 + 1/x^2} + 1} \tag{11}
\end{align}
$$

In $(11),$ the term $1/x^2$ tends to zero and the denominator tends to $2,$ allowing us finally to calculate the limit as follows:

$$\lim_{x \to +\infty} \frac{1}{\sqrt{1 + 1/x^2} + 1} = \frac{1}{2} \tag{12}$$

Cases such as this are resolved simply by transforming the product into a quotient and, with luck, calculating the limit after just one step. If, as in $(10),$ the manipulation produces another indeterminate form, we can continue rewriting the expression using the methods appropriate to the resulting case in order to resolve the indeterminacy.

## The form $\infty - \infty$

This form arises when the limit can be expressed as the difference of two divergent quantities. For example, let us try to evaluate the following limit:

$$\lim_{x \to \infty} \left( \sqrt{x^2 + x} - x \right) \tag{13}$$

Direct substitution gives the form $\infty - \infty,$ which can be resolved by rationalising the numerator, that is, multiplying and dividing by the conjugate of the expression inside the limit (obtained by changing the sign between the terms). This eliminates the square root from the numerator and gives:

$$
\begin{align}
\sqrt{x^2 + x} - x
&= \frac{\left( \sqrt{x^2 + x} - x \right) \left( \sqrt{x^2 + x} + x \right)}{\sqrt{x^2 + x} + x} \notag \\[6pt]
&= \frac{x^2 + x - x^2}{\sqrt{x^2 + x} + x} \notag \\[6pt]
&= \frac{x}{\sqrt{x^2 + x} + x} \tag{14}
\end{align}
$$

We can now factor out $x$ from the denominator and, with a few algebraic steps, obtain the following expression:

$$
\begin{align}
\frac{x}{\sqrt{x^2 + x} + x}
&= \frac{x}{x \left( \sqrt{1 + 1/x} + 1 \right)} \\[6pt]
&= \frac{1}{\sqrt{1 + 1/x} + 1}
\end{align}
$$

We have now obtained a form whose limit can be evaluated, and indeed, taking the limit as $x \to \infty,$ we obtain:

$$\lim_{x \to \infty} \frac{1}{\sqrt{1 + 1/x} + 1} = \frac{1}{\sqrt{1} + 1} = \frac{1}{2}$$

We have seen that the technique applied in $(14)$ uses the conjugate of the original expression, and to understand why, we consider another example:

$$\lim_{x \to \infty} \left( \sqrt{x^2 + 2 x + 3} - x \right) \tag{15}$$

Direct substitution in $(15)$ gives the indeterminate form $\infty - \infty$ because the two quantities have the same leading term $x,$ so we need to determine what remains of their difference. Multiplying and dividing by the conjugate gives the difference of the squares of the two quantities in the numerator, where the $x^2$ terms cancel:

$$
\begin{align}
\frac{\left( \sqrt{x^2 + 2 x + 3} - x \right) \left( \sqrt{x^2 + 2 x + 3} + x \right)}{\sqrt{x^2 + 2 x + 3} + x}
&= \frac{x^2 + 2 x + 3 - x^2}{\sqrt{x^2 + 2 x + 3} + x} \\[6pt]
&= \frac{2 x + 3}{\sqrt{x^2 + 2 x + 3} + x}
\end{align}
$$

We have thus rewritten the original difference as a quotient and eliminated the leading term $x^2.$ We now obtain:

$$
\begin{align}
\frac{2 x + 3}{\sqrt{x^2 + 2 x + 3} + x}
&= \frac{x \left( 2 + 3/x \right)}{x \left( \sqrt{1 + 2/x + 3/x^2} + 1 \right)} \\[6pt]
&= \frac{2 + 3/x}{\sqrt{1 + 2/x + 3/x^2} + 1}
\end{align}
$$

As $x \to \infty,$ the terms with $x$ in the denominator tend to zero, so we obtain:

$$\lim_{x \to \infty} \frac{2 + 3/x}{\sqrt{1 + 2/x + 3/x^2} + 1} = \frac{2}{1 + 1} = 1$$

The same limit can also be calculated using [asymptotic expansions](../asymptotic-expansion/), with [big-O](../big-o-notation/) and little-o notation to control the remainder terms after the leading terms cancel.

## Exponential forms

We now turn to the cases in $(1)$ involving exponential indeterminate forms of the following types:

$$1^{\infty} \qquad 0^{0} \qquad \infty^{0} \tag{16}$$

These expressions typically arise when the limit is reduced to an expression of the following form:

$$\lim_{x \to a} F(x)^{G(x)} \tag{17}$$

Suppose that $F(x) \gt 0$ for $x$ sufficiently close to $a$ within the domain under consideration, possibly excluding $a$ itself. The standard procedure for handling expressions such as $(17)$ is to take the [logarithm of the power](../logarithms/), giving $\ln(F(x)^{G(x)}) = G(x)\ln F(x).$ The product can then be rewritten as a ratio and studied using L'Hôpital's rule or a Taylor expansion. Let $L$ denote the limit to be calculated, if it exists:

$$L = \lim_{x \to a} F(x)^{G(x)} \tag{18}$$

We first calculate the limit of the logarithm of the expression in $(18)$:

$$\ell = \lim_{x \to a} G(x) \ln F(x) \tag{19}$$

This reduces the problem to a limit of the form $0 \cdot \infty,$ which may be rewritten as $0/0$ and studied using the techniques already discussed. If the limit $\ell$ exists and is finite, continuity of the [exponential function](../exponential-function/) ensures that the original limit also exists and satisfies:

$$L = e^{\ell} \tag{20}$$

If instead $\ell = -\infty,$ the original limit is $0;$ if $\ell = +\infty,$ it is $+\infty.$

Consider, for example, the following limit, for which direct substitution gives the indeterminate form $1^{\infty}:$

$$\lim_{x \to 0} (1 + x)^{1/x} \tag{21}$$

Applying the transformation in $(19)$ to $(21),$ we obtain:

$$\ell = \lim_{x \to 0} \frac{\ln(1 + x)}{x}$$

We have now obtained the form $0/0,$ which in this case can be resolved using L'Hôpital's rule, differentiating the numerator and denominator separately. The rule is discussed in its own entry, but for our purposes it is enough to know that the limit becomes:

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = \lim_{x \to 0} \frac{1/(1+x)}{1} = 1$$

Applying $(20),$ we therefore obtain:

$$L = e^{1} = e$$

## A strategy for calculation

In general, beyond the methods illustrated here, each indeterminate form may admit several techniques for resolving it, and the choice between them affects how quickly the calculation reaches a determinate expression that can be evaluated. In practice, the best strategy for tackling these problems is to recognise the indeterminate form and apply a technique that yields the result as quickly and with as little calculation as possible. If, for example, an attempt becomes too algebraically involved or repeatedly leads to further indeterminate forms, the chosen method is probably not the best one for that limit.

My suggestion for the form $0/0$ is that the first attempt should often be algebraic simplification by factoring the numerator and denominator and cancelling the factor that tends to zero. In some cases, [standard limits](../remarkable-limits/) can be used, particularly when trigonometric, exponential, or logarithmic expressions are involved. If neither approach is feasible, asymptotic expansions with little-o notation can be used to isolate the leading behaviour of the numerator and denominator. In other cases, L'Hôpital's rule can be used, especially when the preceding methods become laborious.

For the form $\infty/\infty,$ the standard procedure is to factor out the leading term from the numerator and denominator and determine the limit from the remaining ratio. When the leading term is not immediately identifiable, [logarithms, powers, and exponentials can be compared](../hierarchy-of-growth-rates/). In some cases, L'Hôpital's rule may apply, but the leading-term method is typically quicker and simpler.

The techniques listed above apply to the form $0 \cdot \infty,$ while for the form $\infty - \infty,$ the appropriate step depends on the algebraic structure of the two divergent quantities. Finally, for exponential forms and the product $0 \cdot \infty,$ the techniques illustrated above are used. The following table summarises the main techniques to apply to each form:

[class="table-1"]

|                          |                                                                                                                  |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| $\dfrac{0}{0}$           | Factor and simplify, apply L'Hôpital's rule, or use a [Taylor series expansion](../taylor-series/) |
| $\dfrac{\infty}{\infty}$ | Factor out the leading term or apply L'Hôpital's rule |
| $0 \cdot \infty$         | Rewrite as $\dfrac{0}{1/\infty}$ or $\dfrac{\infty}{1/0}$ to obtain $\dfrac{0}{0}$ or $\dfrac{\infty}{\infty}$ |
| $\infty - \infty$        | Multiply and divide by the conjugate or use a common denominator |
| $1^{\infty}$             | Take the logarithm and reduce to $0 \cdot \infty$ |
| $0^{0}$                  | Take the logarithm and reduce to $0 \cdot \infty$ |
| $\infty^{0}$             | Take the logarithm and reduce to $0 \cdot \infty$ |
[/class]
