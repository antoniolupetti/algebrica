---
title: Limits
source: https://algebrica.org/limits/
license: CC BY-NC 4.0
tags:
  - asymptotes
  - continuous-functions
  - epsilon-delta-definition
  - indeterminate-forms
  - limits
  - neighbourhood
---
## Introduction and definition

Limits are fundamental to mathematical analysis because they allow us to study a function's behaviour as its values approach a given value arbitrarily closely. Before giving the definition, consider a [function](../functions/) $f(x)$ and an [interval](../intervals/) consisting of all points sufficiently close to $x,$ called a [neighbourhood](../topology-of-the-real-line/) of $x.$ More specifically, given a point $x$ and two points $x - \delta$ and $x + \delta$ on the [real line](../real-numbers/), we define a symmetric neighbourhood of $x$ as the open interval $(x - \delta, x + \delta)$ with $\delta > 0.$


![IMG. 1](svg/limits-1.svg)

Neighbourhoods allow us to define limits by describing the local behaviour of $f(x)$ near a given point. As the figure shows, the smaller the neighbourhood, the narrower the interval $(x - \delta, x + \delta),$ and the closer its points are to $x.$

To give a formal definition of a limit, consider again a function $f(x)$ whose behaviour we wish to study as $x$ approaches the point $x_0.$ We say that, as $x$ tends to $x_0,$ the function $f(x)$ has limit $\ell,$ and we write:

$$\lim_{x \to x_0} f(x) = \ell \tag{1}$$

Equation (1) states that we can make the values of $f(x)$ arbitrarily close to $\ell,$ provided we choose $x$ sufficiently close to $x_0$ and different from $x_0.$ To do this, we fix a tolerance $\varepsilon > 0,$ which specifies how close to $\ell$ we want the values of $f(x)$ to be. Equation (1) requires that, for every choice of $\varepsilon > 0,$ there exist a number $\delta > 0$ that guarantees this closeness for all points $x$ in the [domain](../determining-the-domain-of-a-function/) satisfying the following condition:

$$0 < |x - x_0| < \delta\tag{3}$$

The inequality $|x - x_0| < \delta$ in (3) requires $x$ to be at a distance less than $\delta$ from $x_0,$ while $0 < |x - x_0|$ excludes the point $x = x_0.$ The choice of $\delta$ must ensure that the distance between $f(x)$ and $\ell$ is less than the tolerance, so the following inequality must hold:

$$|f(x) - \ell| < \varepsilon\tag{4}$$

The following example illustrates how to choose $\delta$ in terms of $\varepsilon.$ Take the function $f(x) = 2x$ and compute its limit as $x$ tends to $3,$ which is $6.$ We can write:

$$|f(x) - 6| = |2x - 6| = 2|x - 3| \tag{5}$$

If we want $f(x)$ to be within $0.01$ of $6,$ it is enough to require $x$ to be within $0.005$ of $3,$ since $(5)$ shows that the distance $|f(x) - 6|$ is twice the distance $|x - 3|.$ Indeed, if $|x - 3| < 0.005,$ we obtain:

$$|f(x) - 6| = 2|x - 3| < 2 \cdot 0.005 = 0.01$$

We have therefore chosen $\varepsilon = 0.01$ and found $\delta = 0.005.$ In this example, requiring $f(x)$ to be within $0.01$ of $6$ is equivalent to requiring its value to lie in the neighbourhood $(5.99, 6.01)$ of $6.$ Such neighbourhoods can be made arbitrarily small by reducing the tolerance. We have seen that the condition holds for all $x$ in the interval $(2.995, 3.005),$ a neighbourhood of $3,$ excluding $x = 3,$ as required by $(3).$ For every $\varepsilon > 0,$ the choice $\delta = \varepsilon/2$ guarantees (4), confirming that the limit is $6.$

- - -

We have seen that $(1)$ applies as $x$ tends to $x_0,$ but the same definition can be applied when $x$ approaches $x_0$ from the right or from the left. These are called the right-hand limit and the left-hand limit, respectively, and are denoted as follows:

$$ \tag{6}
\begin{align}
&\lim_{x \to x_0^+} f(x) \\[6pt]
&\lim_{x \to x_0^-} f(x)
\end{align}
$$

In the first case, $x$ approaches $x_0$ through values close to and greater than $x_0,$ while in the second case it approaches through smaller values. When these limits exist and are finite, but have different values $\ell_1 \neq \ell_2,$ we have:

$$ \tag{7}
\begin{cases}
\lim\limits_{x \to x_0^-} f(x) = \ell_1 \in \mathbb{R} \\[6pt]
\lim\limits_{x \to x_0^+} f(x) = \ell_2 \in \mathbb{R}
\end{cases} \implies \nexists \lim\limits_{x \to x_0} f(x)
$$

In this situation, two distinct one-sided limits exist, but the limit as $x$ tends to $x_0$ without restriction on the direction of approach does not exist.

## Uniqueness theorem for limits

Statement (7) follows from the [uniqueness theorem for limits](../theorems-on-limits/), which states that the limit of a function, if it exists, is unique. For example, if the limit as $x \to x_0$ is $\ell,$ the right-hand and left-hand limits must also equal $\ell.$ We prove the theorem by contradiction, starting from the following assumptions:

+ $x_0$ is an [accumulation point](../topology-of-the-real-line/) of the domain, so every neighbourhood of $x_0$ contains at least one point of the domain different from $x_0.$
+ Two limits $\ell_1$ and $\ell_2$ exist, with $\ell_1 \lt \ell_2.$

We choose the following tolerance:

$$\varepsilon = \frac{\ell_2 - \ell_1}{2} > 0$$

Since the function is assumed to tend to both $\ell_1$ and $\ell_2,$ condition $(3)$ gives a number $\delta_1 > 0$ such that, for all $x$ in the domain with $0 < |x - x_0| < \delta_1,$ we have $|f(x) - \ell_1| < \varepsilon,$ as in $(4).$ This requires $f(x)$ to be less than $\ell_1 + \varepsilon,$ the midpoint between the two values.

The same argument applies to the limit $\ell_2.$ In this case, we have a distance $\delta_2 > 0$ such that $0 < |x - x_0| < \delta_2$ implies $|f(x) - \ell_2| < \varepsilon.$ This requires $f(x)$ to be greater than $\ell_2 - \varepsilon,$ which is the same midpoint.

We now choose a point $x$ in the domain whose distance from $x_0$ is positive and satisfies the following condition:

$$0 < |x - x_0| < \min\{\delta_1, \delta_2\}$$

By $(4),$ both of the following inequalities must hold for this $x$:

$$
\begin{align}
f(x) &< \ell_1 + \varepsilon = \frac{\ell_1 + \ell_2}{2} \\[6pt]
f(x) &> \ell_2 - \varepsilon = \frac{\ell_1 + \ell_2}{2}
\end{align}
$$

This leads to a contradiction. For example, if $\ell_1 = 2$ and $\ell_2 = 4,$ the chosen tolerance is $\varepsilon = (4 - 2)/2 = 1.$ The two conditions become:

$$
\begin{align}
f(x) &< 2 + 1 = 3 \\[6pt]
f(x) &> 4 - 1 = 3
\end{align}
$$

The same value $f(x)$ would then have to be both less than $3$ and greater than $3,$ which is impossible. Thus the assumption that the two limits $\ell_1$ and $\ell_2$ are distinct is impossible, proving the theorem in the finite case.

Next, suppose that a finite limit $\ell$ and an infinite limit both exist. If $f(x)$ tends to $\ell,$ choosing $\varepsilon = 1$ gives the following inequality for every $x$ in the domain sufficiently close to $x_0$ and different from $x_0$:

$$\ell - 1 < f(x) < \ell + 1 \tag{8}$$

If the function also tended to $\pm\infty,$ we would have $f(x) > \ell + 1$ or $f(x) < \ell - 1$ sufficiently close to $x_0,$ contradicting $(8).$

Finally, suppose that the two limits are $+\infty$ and $-\infty.$ A limit of $+ \infty$ would require $f(x) > 1$ for $x$ sufficiently close to $x_0$ and different from $x_0,$ whereas a limit of $- \infty$ would require $f(x) < -1.$ This again leads to a contradiction.

The preceding cases therefore show that, if the limit of a function as $x \to x_0$ exists, whether finite or infinite, its value is unique, as the theorem asserts.

## Asymptotes

In general, the variable $x$ in a limit may approach a real number $x_0$ or $\pm \infty,$ while the value of the limit may be finite or infinite. As $x$ approaches a finite point, the possible cases are:

$$
\begin{align}
\lim_{x \to x_0} f(x) &= \ell \\[6pt]
\lim_{x \to x_0} f(x) &= \pm \infty
\end{align}
$$

As $x$ tends to $\pm \infty,$ the possible cases are:

$$
\begin{align}
\lim_{x \to \pm \infty} f(x) &= \ell \\[6pt]
\lim_{x \to \pm \infty} f(x) &= \pm \infty
\end{align}
$$


When $f(x)$ tends to $\pm \infty$ as $x$ approaches $x_0,$ the function's behaviour near that point determines a vertical asymptote with equation $x = x_0.$ An asymptote is a line that the graph of a function approaches as either $x$ or $f(x)$ increases or decreases without bound. The distance between the curve and the asymptote tends to zero as the graph extends to infinity in the [coordinate plane](../the-cartesian-coordinate-plane/).


![IMG. 2](svg/limits-2.svg)


Sometimes, as in the example shown in the figure, the right-hand and left-hand limits diverge with opposite signs:

$$
\begin{align}
\lim_{x \to x_0^+} f(x) &= -\infty \\[6pt]
\lim_{x \to x_0^-} f(x) &= +\infty
\end{align}
$$


When $f(x)$ tends to a finite value $L$ as $x$ tends to $+\infty$ or $-\infty,$ the line $y = L$ is a horizontal asymptote of the function in the corresponding direction.


![IMG. 3](svg/limits-3.svg)


The same line is a horizontal asymptote in both directions when the two limits at infinity are equal to $L$:

$$
\begin{align}
\lim_{x \to +\infty} f(x) &= L \\[6pt]
\lim_{x \to -\infty} f(x) &= L
\end{align}
$$

Oblique asymptotes are also possible. These are lines with equation $y = mx + q,$ where $m \neq 0,$ such that the distance between the graph and the line tends to zero as $x \to +\infty$ or $x \to -\infty.$ A systematic treatment of [horizontal, vertical, and oblique asymptotes](../asymptotes/) is given in the dedicated article.

## Properties

Limits satisfy a number of [algebraic properties](../algebra-of-limits/), which are discussed in detail, with worked examples, in the dedicated article. Here we summarise the properties of the basic operations that simplify calculations when solving problems.

The limit of the product of a constant and a function equals the product of the constant and the limit of the function:

$$\lim_{x \to x_0} c f(x)  = c \lim_{x \to x_0} f(x) = c \cdot \ell \tag{9}$$

The limit of the sum of two functions equals the sum of their limits:

$$\lim_{x \to x_0} \big( f(x) + g(x) \big) = \lim_{x \to x_0} f(x) + \lim_{x \to x_0} g(x) = \ell_1 + \ell_2\tag{10}$$

Property $(10)$ is particularly useful when working with [polynomials](../polynomials/), trigonometric functions such as [sine and cosine](../sine-and-cosine/), and other common elementary expressions whose limits can be reduced to a sum of two limits.

Another property concerns the limit of the product of two functions, which equals the product of their limits:

$$\lim\limits_{x \to x_0} \big( f(x) g(x) \big) = \lim\limits_{x \to x_0} f(x) \cdot \lim\limits_{x \to x_0} g(x) = \ell_1 \cdot \ell_2 \tag{11}$$

Finally, the limit of the quotient of two functions equals the quotient of their limits:

$$\lim\limits_{x \to x_0} \left( \frac{f(x)}{g(x)} \right) = \frac{\lim\limits_{x \to x_0} f(x)}{\lim\limits_{x \to x_0} g(x)} = \frac{\ell_1}{\ell_2} \tag{12}$$

All the properties stated above hold when the limits involved exist and are finite and, in the case of a quotient, the limit of the denominator is nonzero. In practice, however, substituting the limits for the functions can lead to expressions that do not determine the value of the limit, as in the following cases:

$$\frac{0}{0} \qquad \frac{\infty}{\infty} \qquad \infty - \infty$$

These expressions are known as [indeterminate forms](../indeterminate-forms/). Resolving them requires specific techniques, such as factorisation, asymptotic comparison, [L'Hôpital's rule](../hopital-rule/), [Taylor expansions](../taylor-series/), and [little-o notation](../little-o-notation/). One of the best-known examples is the following limit:

$$\lim_{x \to 0} \frac{\sin x}{x} \tag{13}$$

Substituting $x = 0$ directly into the expression in $(13)$ gives the indeterminate form $0/0,$ which is undefined, and the quotient rule for limits cannot be applied because the limit of the denominator is zero. The limit in $(13)$ is a [standard limit](../remarkable-limits/) with value $1.$ Indeterminate forms and standard limits are treated in two separate articles.

## Limits of elementary functions

In the section of the site on functions, each type of function has a section devoted to its elementary and standard limits. The most familiar limits are summarised below:

For a constant function $f(x) = k$ with $k \in \mathbb{R},$ we have:

$$
\begin{align}
\lim_{x \to -\infty} k &= k \\[6pt]
\lim_{x \to +\infty} k &= k
\end{align}
$$

For the identity function $f(x) = x,$ we have:

$$
\begin{align}
\lim_{x \to -\infty} x &= -\infty \\[6pt]
\lim_{x \to +\infty} x &= +\infty
\end{align}
$$

For the [exponential function](../exponential-function/) with base $a > 1,$ we have:

$$
\begin{align}
\lim_{x \to -\infty} a^x &= 0 \\[6pt]
\lim_{x \to +\infty} a^x &= +\infty
\end{align}
$$

For the exponential function with base $0 < a < 1,$ we have:

$$
\begin{align}
\lim_{x \to -\infty} a^x &= +\infty \\[6pt]
\lim_{x \to +\infty} a^x &= 0
\end{align}
$$

For the [power function](../power-function/) $f(x) = x^n,$ we distinguish two cases. The first is a positive even exponent $n \in \mathbb{N},$ for which we have:

$$
\begin{align}
\lim_{x \to -\infty} x^n &= +\infty \\[6pt]
\lim_{x \to +\infty} x^n &= +\infty
\end{align}
$$

When the exponent is odd, we have:

$$
\begin{align}
\lim_{x \to -\infty} x^n &= -\infty \\[6pt]
\lim_{x \to +\infty} x^n &= +\infty
\end{align}
$$

For the [root function](../radicals/) $f(x) = \sqrt[n]{x},$ we also distinguish two cases. The first is an even index, for which we have:

$$\lim_{x \to +\infty} \sqrt[n]{x} = +\infty$$

For an odd index, we have:

$$
\begin{align}
\lim_{x \to -\infty} \sqrt[n]{x} &= -\infty \\[6pt]
\lim_{x \to +\infty} \sqrt[n]{x} &= +\infty
\end{align}
$$

For the [logarithmic function](../logarithmic-function/) with base $a > 1,$ we have:

$$
\begin{align}
\lim_{x \to 0^+} \log_a x &= -\infty \\[6pt]
\lim_{x \to +\infty} \log_a x &= +\infty
\end{align}
$$

When the base satisfies $0 < a < 1,$ we have:

$$
\begin{align}
\lim_{x \to 0^+} \log_a x &= +\infty \\[6pt]
\lim_{x \to +\infty} \log_a x &= -\infty
\end{align}
$$

For the [absolute value function](../absolute-value-function/) $f(x) = |x|,$ we have:

$$
\begin{align}
\lim_{x \to -\infty} |x| &= +\infty \\[6pt]
\lim_{x \to +\infty} |x| &= +\infty
\end{align}
$$

Finally, for the [sign function](../sign-function/) $\mathrm{sgn}(x),$ we have:

$$
\begin{align}
\lim_{x \to -\infty} \mathrm{sgn}(x) &= -1 \\[6pt]
\lim_{x \to +\infty} \mathrm{sgn}(x) &= 1
\end{align}
$$
