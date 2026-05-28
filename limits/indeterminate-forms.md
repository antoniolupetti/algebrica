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

When working with limits, expressions of the following type occur repeatedly:

$$\frac{0}{0} \qquad \frac{\infty}{\infty} \qquad 0 \cdot \infty \qquad \infty - \infty$$

$$1^{\infty} \qquad 0^{0} \qquad \infty^{0}$$

These are called indeterminate forms, because the value of the limit cannot be determined from the symbol alone. Different [functions](../functions/) can produce the same symbolic form yet lead to completely different values. The following sections review what these forms mean, why they are called indeterminate, and how to handle them in practice.

In simple terms, an indeterminate form does not stand for a specific number. It signals that direct substitution is insufficient to find the limit. Suppose, for example, that two functions $f(x)$ and $g(x)$ both tend to zero as $x$ approaches some value $a$:

$$\lim_{x \to a} f(x) = 0 \qquad \lim_{x \to a} g(x) = 0$$

If we try to find the limit of their ratio, direct substitution gives:

$$\lim_{x \to a} \frac{f(x)}{g(x)} \to \frac{0}{0}$$

This notation alone does not tell us how the ratio will behave. Depending on how $f(x)$ and $g(x)$ approach zero, the limit could be any finite number, zero, infinity, or it might not exist at all. The indeterminate form does not resolve the problem; it signals that further analysis is required.

Three considerations should be kept in mind before analysing each form:

+ An indeterminate form does not represent a specific number.
+ It does not stand for an equality.
+ It serves as a label describing the limiting behaviour of the expressions involved.

## The form $\frac{0}{0}$

This is the indeterminate form encountered most frequently. It typically appears when both numerator and denominator vanish at the same point. Often the expression can be simplified by algebraic manipulation before taking the limit. As an example, consider:

$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$$

Direct substitution gives $\dfrac{0}{0}$. Factoring the numerator:

$$x^2 - 4 = (x - 2)(x + 2)$$

so that, for $x \neq 2$:

$$\frac{x^2 - 4}{x - 2} = x + 2$$

We therefore obtain:

$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = 4$$

> Once the simplification is carried out, the underlying structure of the expression becomes visible and the indeterminate form disappears. In more advanced problems, [L'Hôpital's rule](../hopital-rule/) provides a systematic way to resolve this type of limit, provided that its hypotheses are satisfied. A complementary approach uses [Taylor expansions](../taylor-series/) with [little-o notation](../little-o-notation/) to isolate the leading term of numerator and denominator.

## The form $\dfrac{\infty}{\infty}$

This form arises when both numerator and denominator diverge. Consider, for example:

$$\lim_{x \to \infty} \frac{3 x^2 + 1}{2 x^2 - 5}$$

Direct substitution gives $\dfrac{\infty}{\infty}$. To resolve the indeterminacy, we factor out the highest power of $x$ in both numerator and denominator:

$$
\begin{align}
\frac{3 x^2 + 1}{2 x^2 - 5}
&= \frac{x^2 (3 + 1/x^2)}{x^2 (2 - 5/x^2)} \\[6pt]
&= \frac{3 + 1/x^2}{2 - 5/x^2}
\end{align}
$$

As $x \to \infty$, the terms $1/x^2$ and $5/x^2$ vanish, so the limit becomes:

$$\lim_{x \to \infty} \frac{3 x^2 + 1}{2 x^2 - 5} = \frac{3}{2}$$

> Symbolic appearance alone is not enough. The way the dominant terms behave for large $x$ determines the answer, and the procedure of factoring out the leading power formalises this idea. The same conclusion can be reached by applying [L'Hôpital's rule](../hopital-rule/) twice, since the form $\dfrac{\infty}{\infty}$ is also covered by the theorem.

## The form $0 \cdot \infty$

This form arises when one factor approaches zero while the other increases without bound. For example:

$$\lim_{x \to 0^+} x \ln x$$

As $x$ approaches zero from the right, $\ln x$ becomes increasingly negative, so the product takes the form $0 \cdot (-\infty)$. To resolve the indeterminacy, we rewrite the expression as a ratio:

$$x \ln x = \frac{\ln x}{1/x}$$

Now, as $x \to 0^+$, we have:

$$\ln x \to -\infty \qquad \frac{1}{x} \to +\infty$$

The expression takes the form $\dfrac{-\infty}{+\infty}$, which can be resolved by asymptotic comparison between the [logarithm](../logarithms/) and a power, or by [L'Hôpital's rule](../hopital-rule/). The result is:

$$\lim_{x \to 0^+} x \ln x = 0$$

> The key step is to transform the product into a quotient, which reduces the problem to one of the more familiar forms $0/0$ or $\infty/\infty$.

## The form $\infty - \infty$

This form can conceal the fact that two divergent quantities partially cancel each other out. Consider, for instance:

$$\lim_{x \to \infty} \left( \sqrt{x^2 + x} - x \right)$$

Both terms grow without bound, which gives the form $\infty - \infty$. To resolve the indeterminacy, we rationalise the expression by multiplying and dividing by the conjugate:

$$
\begin{align}
\sqrt{x^2 + x} - x
&= \frac{\left( \sqrt{x^2 + x} - x \right) \left( \sqrt{x^2 + x} + x \right)}{\sqrt{x^2 + x} + x} \\[6pt]
&= \frac{x^2 + x - x^2}{\sqrt{x^2 + x} + x} \\[6pt]
&= \frac{x}{\sqrt{x^2 + x} + x}
\end{align}
$$

Next, we factor $x$ from the denominator:

$$
\begin{align}
\frac{x}{\sqrt{x^2 + x} + x}
&= \frac{x}{x \left( \sqrt{1 + 1/x} + 1 \right)} \\[6pt]
&= \frac{1}{\sqrt{1 + 1/x} + 1}
\end{align}
$$

Taking the limit as $x \to \infty$:

$$\lim_{x \to \infty} \frac{1}{\sqrt{1 + 1/x} + 1} = \frac{1}{\sqrt{1} + 1} = \frac{1}{2}$$

> After the simplification, the apparent divergence disappears and the limit is finite.

## Rationale for using the conjugate

The technique applied to the form $\infty - \infty$ relies on the conjugate, that is, an expression identical to the original except for the sign between the two terms. The rationale behind this choice is examined below. Consider the limit:

$$\lim_{x \to \infty} \left( \sqrt{x^2 + 2 x + 3} - x \right)$$

Both terms increase without bound, so direct substitution yields the indeterminate form $\infty - \infty$. The fundamental issue is not divergence itself, but the fact that the two quantities grow at the same leading order. Their subtraction conceals a cancellation of dominant terms, and the expression in its present form does not reveal what remains after this cancellation takes place. Multiplying and dividing by the conjugate makes the cancellation explicit:

$$
\begin{align}
\frac{\left( \sqrt{x^2 + 2 x + 3} - x \right) \left( \sqrt{x^2 + 2 x + 3} + x \right)}{\sqrt{x^2 + 2 x + 3} + x}
&= \frac{x^2 + 2 x + 3 - x^2}{\sqrt{x^2 + 2 x + 3} + x} \\[6pt]
&= \frac{2 x + 3}{\sqrt{x^2 + 2 x + 3} + x}
\end{align}
$$

The original difference is now expressed as a quotient. The leading $x^2$ term is removed, and the remaining expression can be analysed further by factoring $x$ from both numerator and denominator:

$$
\begin{align}
\frac{2 x + 3}{\sqrt{x^2 + 2 x + 3} + x}
&= \frac{x \left( 2 + 3/x \right)}{x \left( \sqrt{1 + 2/x + 3/x^2} + 1 \right)} \\[6pt]
&= \frac{2 + 3/x}{\sqrt{1 + 2/x + 3/x^2} + 1}
\end{align}
$$

As $x \to \infty$, the terms $3/x$, $2/x$, and $3/x^2$ all approach zero, and the limit simplifies to:

$$\lim_{x \to \infty} \left( \sqrt{x^2 + 2 x + 3} - x \right) = \frac{2}{1 + 1} = 1$$

> The use of the conjugate makes the cancellation of dominant terms explicit and reveals the true order of growth. The leading $x^2$ terms cancel, and the behaviour is governed by lower-order terms. This perspective connects naturally with [Big O](../big-o-notation/) and [little-o notation](../little-o-notation/), where limits are understood by comparing relative growth rates.

## Exponential indeterminate forms

When working with limits that involve exponential expressions, three further indeterminate forms can appear:

$$1^{\infty} \qquad 0^{0} \qquad \infty^{0}$$

These arise in expressions of the form:

$$\lim_{x \to a} F(x)^{G(x)}$$

in which base and exponent behave in conflicting ways. As with the other indeterminate forms, the symbolic appearance alone is not enough to determine the outcome.

The standard procedure is the logarithmic transformation. Taking the [logarithm](../logarithms/) converts the exponential structure into a product, which can then be rewritten as a ratio and resolved by L'Hôpital's rule or by Taylor expansion. The general scheme is the following. Suppose we want to compute:

$$L = \lim_{x \to a} F(x)^{G(x)}$$

Taking the natural logarithm of both sides:

$$\ln L = \lim_{x \to a} G(x) \ln F(x)$$

This reduces the problem to a limit of the form $0 \cdot \infty$ or $\dfrac{0}{0}$, both of which can be handled by the techniques already discussed. Once $\ln L$ is determined, the original limit is recovered as $L = e^{\ln L}$.

As a concrete example, consider:

$$\lim_{x \to 0} (1 + x)^{1/x}$$

This has the form $1^{\infty}$. Setting $L$ equal to the limit and taking the logarithm:

$$\ln L = \lim_{x \to 0} \frac{\ln(1 + x)}{x}$$

This is now a $\dfrac{0}{0}$ form. Applying [L'Hôpital's rule](../hopital-rule/), we differentiate numerator and denominator separately:

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = \lim_{x \to 0} \frac{1/(1+x)}{1} = 1$$

Hence:

$$L = e^{1} = e$$

This value coincides with the [remarkable limit](../remarkable-limits/) that defines the [number $e$](../euler-number-limit-sequence/).

> The exponential form conceals a hidden quotient structure. Applying a logarithmic transformation exposes this structure and reduces the problem to a familiar one.

All seven indeterminate forms share a common feature: the symbolic expression alone does not determine the value of the limit. The decisive factor is always the relative rate at which the quantities involved grow or vanish. Recognising the indeterminate form is only the first step; computing the limit requires a closer analysis of the functions involved.

## A strategy for computing limits

Each indeterminate form admits more than one resolution technique, and the choice between them affects how quickly the calculation reaches a determinate expression. A working strategy starts from the recognition of the form, proceeds with the application of a primary technique chosen for its directness on that specific case, and turns to an alternative whenever the first attempt becomes algebraically heavy or fails to produce a conclusion.

For a quotient that reduces to $\dfrac{0}{0}$, the first attempt is algebraic simplification through factoring of numerator and denominator and cancellation of the common vanishing factor. When the simplification is not transparent, [remarkable limits](../remarkable-limits/) provide a direct shortcut, especially in the presence of trigonometric, exponential, or logarithmic expressions near the origin. If neither route is available, [Taylor expansions](../taylor-series/) with [little-o notation](../little-o-notation/) isolate the leading behaviour of numerator and denominator. [L'Hôpital's rule](../hopital-rule/) is reserved for situations in which the preceding methods are inconvenient, since it can hide structural information about the limit.

For a quotient that reduces to $\dfrac{\infty}{\infty}$, the standard move is to factor the dominant term from numerator and denominator and to read the limit from the surviving ratio. When the dominant term is not immediately identifiable, the comparison between growth rates of logarithms, powers, exponentials, and factorials provides the answer. L'Hôpital's rule remains available, but the dominant-term approach is usually faster.

For a product of the form $0 \cdot \infty$, the resolution proceeds by rewriting the product as a quotient. The transformed expression takes either the form $\dfrac{0}{0}$ or the form $\dfrac{\infty}{\infty}$, and the techniques listed above apply.

For a difference of the form $\infty - \infty$, the appropriate step depends on the algebraic structure of the two divergent quantities. When they share a common dominant term, the conjugate produces a cancellation that exposes lower-order behaviour. When the two terms admit a common denominator, the difference reduces to a quotient. In both cases the indeterminacy is converted into a $\dfrac{0}{0}$ or $\dfrac{\infty}{\infty}$ form.

For an exponential form $1^{\infty}$, $0^{0}$, or $\infty^{0}$, the logarithmic transformation reduces the calculation to a product $0 \cdot \infty$, which is then handled by the techniques already listed.

## Resolution techniques

A compact list of the recurring techniques, together with the form on which each is typically deployed, keeps the strategy organised.

+ Factoring and cancellation, effective for $\dfrac{0}{0}$ when numerator and denominator share a vanishing factor.
+ Rationalisation by the conjugate, used in $\infty - \infty$ and in $\dfrac{0}{0}$ expressions containing square roots, where the conjugate makes the dominant-term cancellation explicit.
+ Division by the dominant term, the primary tool for $\dfrac{\infty}{\infty}$ involving polynomials, rational functions, or sums of monomials of mixed degree.
+ Substitution, in which a change of variable such as $t = 1/x$ or $t = x - a$ transports the limit into a form where another technique applies more naturally.
+ Remarkable limits, applied through algebraic manipulation of the expression to match a known pattern from the standard catalogue.
+ Taylor expansions with little-o notation, indispensable when numerator and denominator must be compared at higher orders, or when several remarkable limits would otherwise have to be combined.
+ L'Hôpital's rule, a last-resort method for $\dfrac{0}{0}$ and $\dfrac{\infty}{\infty}$, subject to verification of its hypotheses.

The following table associates each indeterminate form with a primary technique and a typical alternative.

[class="table-1"]

|                          |                                                                                                                  |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| $\dfrac{0}{0}$           | Factor and simplify, apply [L'Hôpital's rule](../hopital-rule/), or expand by [Taylor series](../taylor-series/) |
| $\dfrac{\infty}{\infty}$ | Factor out the dominant term, or apply L'Hôpital's rule                                                          |
| $0 \cdot \infty$         | Rewrite as $\dfrac{0}{1/\infty}$ or $\dfrac{\infty}{1/0}$ to obtain $\dfrac{0}{0}$ or $\dfrac{\infty}{\infty}$   |
| $\infty - \infty$        | Multiply by the conjugate, or find a common denominator                                                          |
| $1^{\infty}$             | Take the logarithm and reduce to $0 \cdot \infty$                                                                |
| $0^{0}$                  | Take the logarithm and reduce to $0 \cdot \infty$                                                                |
| $\infty^{0}$             | Take the logarithm and reduce to $0 \cdot \infty$                                                                |
[/class]

The techniques summarised here build on the [algebra of limits](../algebra-of-limits/) and connect with the [squeeze theorem](../squeeze-theorem/) whenever the function under study can be bounded between two functions with a common limit.


## Cautions on L'Hôpital and Taylor

L'Hôpital's rule requires that the limit reduce to $\dfrac{0}{0}$ or $\dfrac{\infty}{\infty}$, that numerator and denominator be differentiable in a neighbourhood of the point, that the derivative of the denominator be non-zero there, and that the limit of the ratio of the derivatives exist. Applying the rule when the hypotheses fail produces results that are formally derived but logically unjustified. A frequent error is the application of L'Hôpital to a quotient that has already become determinate after a previous algebraic step, with the consequence of reintroducing a spurious indeterminate form into a calculation that no longer required one.

Taylor expansions resolve a limit when the expansions of numerator and denominator are pushed to sufficient order to make the leading non-zero terms visible. Truncating too early produces an apparent cancellation that does not reflect the true behaviour of the function. The order of expansion must therefore be chosen by inspecting the order of vanishing of the dominant term, and not by reflex.

> The choice between L'Hôpital and Taylor often reduces to a matter of perspective. L'Hôpital is procedural and almost mechanical, but it blurs the structure of the functions involved. Taylor exposes that structure and reveals at which order the limit is determined, at the cost of slightly heavier algebra.