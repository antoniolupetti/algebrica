---
title: Big-O Notation
source: https://algebrica.org/big-o-notation/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - big-o-notation
  - landau-symbols
  - limits
  - little-o-notation
  - taylor-series
---
## Big-O of a variable

In the article on [little-o notation](../little-o-notation/), we introduced the Landau symbols, which describe the asymptotic behaviour of two [functions](../functions/) by examining the [limit](../limits/) of their ratio. We introduce big-O notation as follows. Let $f, g : A \to \mathbb{R}$ be two functions, with $A \subseteq \mathbb{R},$ and let $x_0$ be an [accumulation point](../topology-of-the-real-line/) of $A,$ meaning that every neighbourhood of $x_0$ contains at least one point of $A$ other than $x_0.$ Suppose also that $g(x)$ is nonzero at points of $A$ near $x_0$ other than $x_0$ itself. We say that $f(x)$ is "big-O" of $g(x)$ as $x$ tends to $x_0$ if there is a constant $M > 0$ such that the following inequality holds at all these points:

$$\left|\frac{f(x)}{g(x)}\right| \leq M \tag{1}$$

Condition $(1)$ is expressed by the notation $f(x) = O(g(x))$ as $x \to x_0.$ The class of all functions $f$ satisfying this condition can also be written as:

$$O_{x_0}(g) = \{\ f : A \to \mathbb{R} \mid \limsup_{\substack{x \to x_0 \\ x \in A}} \left|\frac{f(x)}{g(x)}\right| < +\infty \ \}$$


To make the phrase "near $x_0$" precise, we fix a threshold $\delta > 0$ below which the distance between $x$ and $x_0,$ given by $|x - x_0|,$ must remain. Condition $(1)$ therefore requires that we can choose a constant $M > 0$ and a number $\delta > 0$ so that the bound in $(1)$ holds at every point of $A$ in this neighbourhood except $x_0.$ These points satisfy:

$$0 < |x - x_0| < \delta \tag{2}$$

For all points satisfying $(2),$ we can rewrite $(1)$ using the rule for the [absolute value](../absolute-value/) of a quotient:

$$\frac{|f(x)|}{|g(x)|} \leq M \tag{3}$$

Since $|g(x)| > 0,$ multiplying both sides of $(3)$ by $|g(x)|$ gives:

$$|f(x)| \leq M|g(x)| \tag{4}$$

To illustrate the definition, consider the functions $f(x) = x^2$ and $g(x) = x$ as $x \to 0.$ For $x \neq 0,$ the absolute value of their ratio is:

$$\left|\frac{x^2}{x}\right| = |x|$$

If $0 < |x| < 1,$ this ratio is less than $1.$ Condition $(1)$ is therefore satisfied with $M = 1$ and $\delta = 1,$ so as $x$ tends to zero we have:

$$x^2 = O(x)$$

For a numerical comparison, we take positive values of $x$ progressively closer to zero and calculate $x^2$ and the ratio $x^2/x.$ This gives:

$$
\begin{array}{c|c|c}
x & x^2 & x^2/x \\[6pt]
\hline
0.1 & 0.01 & 0.1 \\[6pt]
0.01 & 0.0001 & 0.01 \\[6pt]
0.001 & 0.000001 & 0.001
\end{array}
$$

The ratio remains bounded and tends to zero. By the definition of little-o, both $x^2 = O(x)$ and $x^2 = o(x)$ therefore hold as $x \to 0.$

- - -

Now consider the limit as $x \to +\infty.$ In this case, condition $(2)$ is replaced by $x > N,$ where $N > 0$ is a threshold beyond which the bound in $(3)$ must hold. For the functions $f(x) = x$ and $g(x) = x^2,$ when $x > 1$ we obtain:

$$\left|\frac{x}{x^2}\right| = \frac{1}{x} \leq 1$$

Condition $(1)$ holds with $M = 1$ and $N = 1,$ so $x = O(x^2)$ as $x \to \infty.$

- - -

Another example is the comparison between $\log x$ and $x,$ for which we have:

$$\lim_{x \to \infty} \frac{\log x}{x} = 0$$

Since a function that tends to zero remains bounded for sufficiently large $x,$ condition $(1)$ gives $\log x = O(x)$ as $x \to \infty.$ As in the example comparing $x^2$ and $x$ as $x \to 0,$ the ratio tends to zero and therefore also satisfies the definition of little-o. We can thus write $\log x = o(x)$ as $x \to \infty.$ This relation provides more information than the big-O statement, since it says that $\log x$ is negligible compared with $x,$ whereas big-O only requires the ratio to remain bounded.

- - -

For a case in which the ratio does not tend to zero, consider the following [polynomial](../polynomials/), which we wish to compare with $x^2$ as $x \to \infty.$

$$f(x) = 3x^2 + 2x + 1$$

Dividing each term by $x^2,$ we obtain:

$$\frac{3x^2 + 2x + 1}{x^2} = 3 + \frac{2}{x} + \frac{1}{x^2} \tag{5}$$

As $x$ tends to $+\infty,$ the ratio in $(5)$ tends to $3$ and therefore remains bounded. To verify the definition of big-O, we apply $(3)$ and seek a constant $M > 0$ such that the ratio does not exceed $M$ for all sufficiently large $x.$ Since we are considering the limit as $x \to \infty,$ we may restrict attention to $x \geq 1.$ For $x \geq 1,$ we also have $x^2 \geq 1.$ The denominators are therefore at least $1,$ which gives $2/x \leq 2$ and $1/x^2 \leq 1.$ Adding these bounds to estimate the ratio in $(3),$ we obtain:

$$\frac{3x^2 + 2x + 1}{x^2} \leq 3 + 2 + 1 = 6$$

The definition is therefore satisfied with $M = 6,$ so we conclude that as $x$ tends to $+\infty$ we have:

$$3x^2 + 2x + 1 = O(x^2)$$

Multiplying the preceding inequality by $x^2 > 0,$ we obtain $f(x) \leq 6x^2$ for $x \geq 1.$ The following graph illustrates this bound by comparing the polynomial with the function $6x^2,$ obtained by multiplying $g(x) = x^2$ by the constant $M = 6.$

![IMG. 1](svg/big-o-notation-1.svg)

The bound can also be checked at particular values, for example:

$$
\begin{array}{c|c|c}
x & f(x) & 6x^2 \\[6pt]
\hline
10 & 321 & 600 \\[6pt]
100 & 30201 & 60000 \\[6pt]
1000 & 3002001 & 6000000
\end{array}
$$

- - -

The distinction from little-o notation is that big-O requires the absolute value of the ratio of two functions to remain bounded, whereas little-o requires the ratio to tend to zero. Condition $(1)$ is thus replaced by the more restrictive condition:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = 0$$

If this limit is zero, the ratio remains bounded near $x_0,$ so every relation $f(x) = o(g(x))$ implies $f(x) = O(g(x)).$ In set-theoretic terms, the class of functions satisfying $f = o(g)$ is a [proper subset](../sets/) of the class satisfying $f = O(g),$ and the converse implication does not hold.


## The meaning of $O(1)$

The symbol $O(1),$ read as "big-O of 1", denotes functions that remain bounded as $x \to x_0.$ Applying $(1)$ with the constant function $g(x) = 1,$ we say that $f(x) = O(1)$ if there exist $M > 0$ and $\delta > 0$ such that, for every point $x \in A$ satisfying $(2),$ the following inequality holds:

$$\left|\frac{f(x)}{1}\right| = |f(x)| \leq M \tag{6}$$

In other words, let $A \subseteq \mathbb{R}$ and let $x_0$ be an accumulation point of $A.$ The class of functions defined on $A$ that are big-O of $1$ as $x \to x_0$ can be written as:

$$O_{x_0}(1) = \{\ f : A \to \mathbb{R} \mid \limsup_{\substack{x \to x_0 \\ x \in A}} |f(x)| < +\infty \ \}$$

Consider, for example, the following function, defined for $x \neq 0:$

$$f(x) = \sin\left(\frac{1}{x}\right)$$

The [sine function](../sine-function/) takes values between $-1$ and $1,$ so its absolute value cannot exceed $1$ when its argument is $1/x.$ Thus, for every $x \neq 0,$ we have:

$$\left|\sin\left(\frac{1}{x}\right)\right| \leq 1 \tag{7}$$

Inequality $(7)$ is precisely condition $(6)$ with $M = 1.$ In particular, it holds at all points with $0 < |x| < 1,$ so we may choose $\delta = 1.$ The definition is satisfied, and we conclude that as $x$ tends to zero we have:

$$\sin\left(\frac{1}{x}\right) = O(1)$$

## Properties

The following properties are useful for algebraic manipulations involving big-O notation. The first follows from definition $(1).$ If $f(x) = O(g(x))$ as $x \to x_0$ and $g(x)$ is nonzero in a punctured neighbourhood of $x_0$ relative to $A,$ the ratio remains bounded in absolute value. This condition can be written as:

$$\limsup_{x \to x_0} \left|\frac{f(x)}{g(x)}\right| < \infty$$

Requiring the limit superior to be finite expresses the boundedness of the ratio, even when the limit does not exist, as in the preceding example with $\sin(1/x).$ Another property concerns multiplication of a function $g$ by a constant $c \in \mathbb{R}$ with $c \neq 0.$ As $x \to x_0,$ the following relations hold:

$$
\begin{align}
O(cg(x)) &= O(g(x)) \\[6pt]
cO(g(x)) &= O(g(x))
\end{align}
$$

An analogous property holds for addition:

$$O(f(x)) + O(f(x)) = O(f(x))$$

If two functions are bounded in absolute value by $M_1|f(x)|$ and $M_2|f(x)|,$ respectively, the triangle inequality shows that their sum is bounded in absolute value by $(M_1 + M_2)|f(x)|.$ Now consider the product of an $O(g(x))$ term and $f(x).$ We obtain the following relation:

$$f(x)O(g(x)) = O(f(x)g(x))$$

Indeed, if $|r(x)| \leq M|g(x)|,$ then $|f(x)r(x)| \leq M|f(x)g(x)|.$ For example, choosing $g(x) = x$ and multiplying an $O(x)$ term by $f(x) = x^2$ gives:

$$x^2O(x) = O(x^3)$$

An analogous property holds for [powers](../powers/) and follows by raising both sides of $(4)$ to the power $a.$ If $f(x) = O(g(x))$ as $x \to x_0,$ with $f$ and $g$ nonnegative, then for every exponent $a > 0$ we have:

$$[f(x)]^a = O([g(x)]^a) \tag{8}$$


In addition to these rules, the big-O relation is transitive. If $f(x) = O(g(x))$ and $g(x) = O(h(x))$ as $x \to x_0,$ then:

$$f(x) = O(h(x))$$

By assumption, there are two positive constants $M_1$ and $M_2$ such that $|f(x)| \leq M_1|g(x)|$ and $|g(x)| \leq M_2|h(x)|$ in suitable punctured neighbourhoods of $x_0.$ Taking the intersection of these neighbourhoods and combining the two inequalities gives $|f(x)| \leq M_1M_2|h(x)|.$

Transitivity also allows two nested big-O symbols to be reduced to one. In this sense, we can write:

$$O(O(f(x))) = O(f(x))$$

## Big-O notation in Taylor expansions

In [asymptotic expansions](../asymptotic-expansion/), big-O notation describes the truncation error by means of an upper bound. In other words, if a function $f$ is $n+1$ times [differentiable](../derivatives/) in a neighbourhood of $x_0,$ its [Taylor expansion](../taylor-series/) of order $n$ has the form:

$$f(x) = f(x_0) + f'(x_0)(x - x_0) + \frac{f''(x_0)}{2!}(x - x_0)^2 + \cdots + \frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + O\big((x - x_0)^{n+1}\big)$$

The symbol $O((x - x_0)^{n+1})$ indicates that the absolute value of the remainder is bounded by a constant multiple of $|x - x_0|^{n+1}$ as $x \to x_0,$ so the remainder is controlled by the first omitted power. The following table lists several expansions near $x = 0$ with their remainders expressed in big-O notation. In the last row, $\alpha$ is a fixed real exponent.

[class="table-1"]

|                  |                                                                       |
| ---------------- | --------------------------------------------------------------------- |
| $e^x$            | $1 + x + \dfrac{x^2}{2!} + \dfrac{x^3}{3!} + O(x^4)$                  |
| $\sin x$         | $x - \dfrac{x^3}{6} + O(x^5)$                                         |
| $\cos x$         | $1 - \dfrac{x^2}{2} + \dfrac{x^4}{24} + O(x^6)$                       |
| $\ln(1+x)$       | $x - \dfrac{x^2}{2} + \dfrac{x^3}{3} + O(x^4)$                        |
| $(1+x)^\alpha$   | $1 + \alpha x + \dfrac{\alpha(\alpha-1)}{2} x^2 + O(x^3)$              |

[/class]

These expansions are useful for evaluating limits involving [indeterminate forms](../indeterminate-forms/). Consider, for example, the following limit, which cannot be evaluated by direct substitution:

$$\lim_{x \to 0} \frac{e^x - 1 - x}{x^2}$$

Substituting the expansion of $e^x$ through the quadratic term, we can rewrite it as:

$$\lim_{x \to 0} \frac{\dfrac{x^2}{2} + O(x^3)}{x^2} = \frac{1}{2}$$

After division by the denominator, the remainder $O(x^3)$ becomes an $O(x)$ term, whose absolute value is bounded by $M|x|$ and therefore tends to zero. The limit is thus determined by the coefficient of the quadratic term.
