---
title: Little-o Notation
source: https://algebrica.org/little-o-notation/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - big-o-notation
  - landau-symbols
  - limits
  - little-o-notation
  - taylor-series
---
## Little-o of a variable

When studying a limit, it can be useful to compare two [functions](../functions/) to understand, for example, how quickly they grow or tend to zero, and thus determine which terms dominate and which are negligible. These comparisons are expressed using Landau symbols, namely the so-called "little-o" and "big-O" notation for real or complex variables.

Suppose we have two functions $f(x), \ g(x) : A \to \mathbb{R}$ (if you have followed the topics covered so far on Algebrica, you should by now be familiar with $A$ as the [domain](../determining-the-domain-of-a-function/) and $\mathbb{R}$ as the codomain), and suppose that $x_0$ is a [limit point](../topology-of-the-real-line/) of $A,$ meaning that every neighbourhood of $x_0$ contains at least one point of $A$ other than $x_0.$ We say that $f(x)$ is "little-o" of $g(x)$ as $x$ tends to $x_0$ if the following relation holds:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = 0 \tag{1}$$

Condition $(1)$ requires $g(x)$ to be nonzero and can also be expressed using the notation $f(x) = o(g(x))$ as $x \to x_0,$ indicating that $f(x)$ is negligible compared to $g(x)$ as $x$ tends to $x_0.$ In general, we can describe the class of all functions $f$ satisfying $(1)$ as follows:

$$o_{x_0}(g) = \{\ f : A \to \mathbb{R} \mid \lim_{x \to x_0} \frac{f(x)}{g(x)} = 0 \ \}$$

But what does "negligible" mean formally? To make this precise, we recall the [definition of a limit](../limits/), discussed in the corresponding article. The difference between the ratio in $(1)$ and zero must become smaller than any given positive number when $x$ is sufficiently close to $x_0.$ Choosing an arbitrarily small $\varepsilon,$ we express this distance through the following inequality:

$$\left|\frac{f(x)}{g(x)} - 0\right| < \varepsilon \tag{2}$$

Thus, for every $\varepsilon > 0,$ there exists $\delta > 0$ such that $(2)$ holds for all points $x \in A$ satisfying the condition:

$$0 < |x - x_0| < \delta \tag{3}$$

For all points satisfying $(3),$ condition $(2)$ therefore holds and can be rewritten as:

$$\frac{|f(x)|}{|g(x)|} < \varepsilon \tag{4}$$


This gives:

$$|f(x)| < \varepsilon \cdot |g(x)| \tag{5}$$

The connection with little-o is that we can make $|f(x)|$ smaller than an arbitrarily small fraction of $|g(x)|,$ which explains what "negligible" compared to $g(x)$ means. To clarify the concept, we consider two functions, $f(x) = x^2$ and $g(x) = x,$ and calculate the limit of their ratio:

$$\lim_{x \to 0} \frac{x^2}{x} = 0$$

Since this limit is zero, definition $(1)$ tells us that $f(x)$ is "little-o" of $g(x)$ and that, as $x$ tends to zero, we have:

$$x^2 = o(x)$$

The following graph makes the reasoning easier to follow. As $x \to 0,$ both functions tend to zero, but at different rates. Near the origin, $x^2$ is much smaller than $x$ in [absolute value](../absolute-value/), as the corresponding curve shows:


![IMG. 1](svg/little-o-1.svg)


To see this comparison numerically, we take several values of $x$ increasingly close to zero and, for each, calculate $x^2$ and the ratio $x^2/x:$

$$
\begin{array}{c|c|c}
x & x^2 & x^2/x \\[6pt]
\hline
0.1 & 0.01 & 0.1 \\[6pt]
0.01 & 0.0001 & 0.01 \\[6pt]
0.001 & 0.000001 & 0.001
\end{array}
$$

As we continue, the square becomes an ever smaller fraction of $x,$ showing that $x^2$ is negligible compared to $x,$ or equivalently, that $x^2 = o(x)$ as $x \to 0.$

- - -

We now consider a similar case, but with the variable $x$ tending to infinity. We calculate the following limit:

$$\lim_{x \to \infty} \frac{x}{x^2} = \lim_{x \to \infty} \frac{1}{x} = 0$$

Here too, the ratio of the two functions $x$ and $x^2$ tends to zero, so $(1)$ gives, as $x \to \infty,$ the relation:

$$x = o(x^2)$$

- - -

For a final example, we evaluate the following limit:

$$\lim_{x \to \infty} \frac{\log x}{x} = 0$$

Since this ratio has limit zero, $(1)$ implies that, as $x \to \infty,$ $\log x = o(x).$ This result is useful in practice, particularly in algorithm design, because [logarithmic growth](../logarithmic-function/) is negligible compared to linear growth.

## The meaning of $o(1)$

We now introduce the symbol $o(1),$ read as "little-o of 1", which denotes functions that tend to zero as $x \to x_0.$ A function $f(x)$ belongs to $o(1)$ when it is infinitesimal compared to the constant $1$ in that limit, meaning that the following equality holds:

$$\lim_{x \to x_0} \frac{f(x)}{1} = \lim_{x \to x_0} f(x) = 0 \tag{6}$$

In other words, let $A \subseteq \mathbb{R}$ and let $x_0$ be a limit point of $A.$ The class of functions defined on $A$ that are little-o of $1$ as $x \to x_0$ can be written as:

$$o_{x_0}(1) = \{\ f : A \to \mathbb{R} \mid \lim_{x \to x_0} f(x) = 0 \ \}$$

As an immediate example, we consider the following [standard limit](../remarkable-limits/):

$$\lim_{x \to 0} \frac{\sin x}{x}$$

To evaluate the limit, we use the [Taylor expansion](../taylor-series/), which allows us to write $\sin x$ as $x$ plus an error that is negligible compared to $x.$ As $x \to 0,$ we obtain:

$$\sin x = x - \frac{x^3}{6} + o(x^3) \quad \text{as} \quad x \to 0 \tag{7}$$

Dividing both sides by $x,$ we can rewrite $(7)$ as:

$$\frac{\sin x}{x} = 1 - \frac{x^2}{6} + o(x^2) \tag{8}$$

Both $-x^2/6$ and $o(x^2)$ tend to zero as $x$ tends to zero. Since $o(1)$ denotes a quantity that tends to zero, we can rewrite $(8)$ as follows:

$$\frac{\sin x}{x} = 1 + o(1)$$


## Properties

We now list several standard properties of little-o notation that are useful for solving the kinds of problems encountered in this setting. The first follows directly from definition $(1),$ namely that if $g(x) = o(f(x))$ as $x \to x_0,$ the ratio of the two functions tends to zero:

$$\lim_{x \to x_0} \frac{o(f(x))}{f(x)} = 0$$

Another property concerns multiplication. Multiplying a function by a nonzero constant does not change its asymptotic behaviour in little-o notation. Thus, for every constant $c \in \mathbb{R}$ with $c \neq 0$ and every function $g(x),$ the following relations hold as $x \to x_0:$

$$
\begin{align}
o(c \cdot g(x)) &= o(g(x)) \\[6pt]
c \cdot o(g(x)) &= o(g(x))
\end{align}
$$

An analogous property holds for addition. The sum of two little-o terms of the same function is still a little-o term of that function, so we have:

$$o(f(x)) + o(f(x)) = o(f(x))$$

Recall from the [algebra of limits](../algebra-of-limits/) that the limit of a sum is the sum of the limits, so the sum of two ratios that tend to zero also tends to zero. We now consider a further property concerning the product of a little-o term and a function. Multiplying a little-o term of $g(x)$ by $f(x),$ with $f(x) \neq 0$ at points of $A$ sufficiently close to $x_0$ and distinct from it, gives a little-o term of the product $f(x)g(x).$ That is:

$$f(x) \cdot o(g(x)) = o(f(x) g(x))$$

For example, if $g(x) = x$ and $o(g(x)) = o(x),$ multiplying by $f(x) = x^2$ gives:

$$x^2 \cdot o(x) = o(x^3)$$

An analogous property holds for powers. If $f(x) = o(g(x))$ as $x \to x_0,$ with $f$ and $g$ nonnegative, then for every exponent $a > 0$ the following holds in the same limit:

$$[f(x)]^a = o([g(x)]^a)$$

In addition to these calculation rules, the little-o relation is transitive. Thus, if $f(x) = o(g(x))$ and $g(x) = o(h(x))$ as $x \to x_0,$ then:

$$f(x) = o(h(x))$$

This relation also follows directly from definition $(1),$ because both ratios tend to zero and hence so does their product. Finally, transitivity allows two nested little-o symbols to be reduced to a single symbol. If $h(x) = o(g(x))$ and $g(x) = o(f(x))$ as $x \to x_0,$ then every function that is little-o of $g$ is also little-o of $f,$ giving the following relation:

$$o(o(f(x))) = o(f(x))$$

## Comparison with big-O notation

The distinction between little-o and [big-O notation](../big-o-notation/) deserves a brief mention here; big-O notation is discussed in detail in a separate article. In brief, as $x$ approaches $x_0,$ big-O requires the absolute value of the ratio of the two functions to remain below some constant bound, whereas little-o requires the ratio to tend to zero.

Compared to $(1),$ we therefore replace the requirement of a zero limit with an inequality. Assuming $g(x) \neq 0$ at the points under consideration, we write $f(x) = O(g(x))$ as $x \to x_0$ if there exist constants $M > 0$ and $\delta > 0$ such that, for every $x \in A$ with $0 < |x - x_0| < \delta,$ we have:

$$\left|\frac{f(x)}{g(x)}\right| \leq M$$

In terms of [set inclusion](../sets/), the class of functions satisfying $f = o(g)$ is strictly contained in the class of functions satisfying $f = O(g).$ Every little-o relation is also a big-O relation, but the converse does not hold.

## Little-o notation in Taylor expansions

A more advanced application concerns the use of little-o notation in [asymptotic expansions](../asymptotic-expansion/). It merits a brief mention because it extends the use already seen in the example with $\sin x.$ In general, in an asymptotic expansion, little-o notation describes the error introduced by truncating at a given degree. For a function $f(x)$ that is [$n$ times differentiable](../higher-order-derivatives/) at $x_0,$ its [Taylor expansion of order $n$](../taylor-formula-with-remainder/) has the form:

$$f(x) = f(x_0) + f'(x_0)(x - x_0) + \frac{f''(x_0)}{2!}(x - x_0)^2 + \cdots + \frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + o\big( (x - x_0)^n \big)$$

The symbol $o((x - x_0)^n)$ denotes the remainder and provides asymptotic information about the function. It states that the error tends to zero more rapidly than $(x - x_0)^n$ as $x \to x_0$ and is therefore negligible compared to this power. When $f^{(n)}(x_0) \neq 0,$ the error is also negligible compared to the last explicit term of the expansion. Several Taylor expansions near $x = 0$ have a remainder expressed in little-o notation, including the following:

[class="table-1"]

|                  |                                                                       |
| ---------------- | --------------------------------------------------------------------- |
| $e^x$            | $1 + x + \dfrac{x^2}{2!} + \dfrac{x^3}{3!} + o(x^3)$                  |
| $\sin x$         | $x - \dfrac{x^3}{6} + o(x^3)$                                         |
| $\cos x$         | $1 - \dfrac{x^2}{2} + \dfrac{x^4}{24} + o(x^4)$                       |
| $\ln(1+x)$       | $x - \dfrac{x^2}{2} + \dfrac{x^3}{3} + o(x^3)$                        |
| $(1+x)^\alpha$   | $1 + \alpha x + \dfrac{\alpha(\alpha-1)}{2} x^2 + o(x^2)$              |

[/class]

These expansions are useful for evaluating limits involving [indeterminate forms](../indeterminate-forms/), since substituting a function's Taylor expansion gives an expression in which the contribution of the remainder tends to zero. For example:

$$\lim_{x \to 0} \frac{e^x - 1 - x}{x^2} = \lim_{x \to 0} \frac{\dfrac{x^2}{2} + o(x^2)}{x^2} = \frac{1}{2}$$

As $x \to 0,$ the ratio $o(x^2)/x^2$ tends to zero, so the limit is determined by the coefficient of the quadratic term.
