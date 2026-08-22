---
title: Techniques for Computing Limits of Sequences
source: https://algebrica.org/techniques-for-computing-limits-of-sequences/
license: CC BY-NC 4.0
tags:
  - asymptotic-equivalence
  - growth-rates
  - indeterminate-forms
  - limit-of-a-sequence
  - logarithms
  - rationalization
  - remarkable-limits
  - sequence
---

## Limits requiring further analysis

One of the main difficulties in computing limits is the wide variety of cases that may arise. For [sequences](../sequences/), determining the limit is not always straightforward. For example, when a sequence leads to an [indeterminate form](../indeterminate-forms/) such as $0/0,$ $+\infty/+\infty,$ $0\cdot\infty,$ or $+\infty-\infty,$ the [limit laws](../algebra-of-limits/) alone no longer suffice to determine convergence. In such cases, we must use other tools and examine, for example, the structure and behavior of the relevant components.

The limit of a sequence depends only on its tail. The idea is intuitive: if, beyond some index, its terms approach a given value, the sequence [converges](../convergent-and-divergent-sequences/) to that value; otherwise, it diverges. More precisely, suppose that two sequences $(a_n)$ and $(b_n)$ satisfy $a_n=b_n$ for every $n\geq n_0.$ From the index $n_0$ onward, the two sequences have the same behavior and therefore the same limit. This observation allows us to ignore finitely many initial terms and work with conditions that hold from some index $n_i$ onward, which substantially simplifies the computation.

The following sections present several methods for evaluating limits that are not immediately determined, chosen according to the structure of the terms in the sequence.

## Dominant terms

One of the simplest methods is to identify the dominant terms. For a sequence whose general term is a ratio of [polynomials](../polynomials/), divide the numerator and denominator by the highest power of $n$ appearing in the two polynomials. Consider the following limit:

$$\lim_{n\to+\infty}\frac{4n^3-5n+1}{2n^3+n^2-7}$$

Direct substitution as $n$ tends to infinity produces the indeterminate form $\infty/\infty,$ which gives no information about the behavior of the sequence. Dividing instead by the highest power of $n$ gives:

$$\lim_{n\to+\infty}\frac{4-5/n^2+1/n^3}{2+1/n-7/n^3}=2$$

More generally, if $P$ and $Q$ have degrees $p$ and $q$ and leading coefficients $a$ and $b,$ then:

$$
\frac{P(n)}{Q(n)}
=n^{p-q}\frac{a+o(1)}{b+o(1)}
$$

The [little-o notation](../little-o-notation/) $o(1)$ collects all terms that tend to zero. The ratio then has three possible behaviors:

+ it tends to $0$ when $p<q;$
+ it tends to $a/b$ when $p=q;$
+ when $p>q,$ its [absolute value](../absolute-value/) tends to infinity and it eventually has the sign of $a/b.$

- - -

The same procedure, factoring out the power of $n$ with the larger exponent, applies to sums of powers. For example, consider the difference $n^\alpha-3n^\beta$ with $\alpha<\beta.$ Factoring out the power with the larger exponent gives:

$$
n^\alpha-3n^\beta
=n^\beta\left(n^{\alpha-\beta}-3\right)
$$

Since $n^{\alpha-\beta}$ tends to zero, the factor in parentheses tends to $-3,$ and the dominant term is $-3n^\beta.$

- - -

Another case arises when a square factor must be extracted from a square root. Since the radicand must be nonnegative, for every value of $n$ we have:

$$\sqrt{n^2}=|n|$$

The absolute value is therefore necessary. As $n\to+\infty,$ the indices are positive, so $|n|=n,$ and we may write, for example, $\sqrt{n^2+3}=n\sqrt{1+3/n^2}.$

## Hierarchy of growth rates

As $n\to+\infty,$ for every choice of constants $p,q>0$ and $a>1,$ the following growth hierarchy holds:

$$
(\ln n)^p\ll n^q\ll a^n\ll n!\ll n^n
$$

The notation $u_n\ll v_n$ means that $u_n/v_n\to0,$ so the sequence to the left of $\ll$ grows more slowly than the one to its right. For example, $(\ln n)^p/n^q$ tends to $0,$ and the same statement holds for every adjacent pair in the chain.

To make the comparisons explicit, consider the first relation, $(\ln n)^p\ll n^q.$ Setting $t=\ln n,$ the ratio becomes:

$$
\frac{(\ln n)^p}{n^q}
=\frac{t^p}{e^{qt}}
\longrightarrow0
$$

For the two comparisons $n^q\ll a^n$ and $a^n\ll n!,$ define $d_n=n^q/a^n$ and $c_n=a^n/n!.$ Their successive-term ratios satisfy:

$$
\begin{align}
\frac{d_{n+1}}{d_n}&=\frac{(1+1/n)^q}{a}\longrightarrow\frac{1}{a}<1 \\[6pt]
\frac{c_{n+1}}{c_n}&=\frac{a}{n+1}\longrightarrow0
\end{align}
$$

Both sequences therefore tend to zero.

Finally, consider the comparison involving the [factorial](../factorial/). We first write:

$$n!/n^n=\prod_{k=1}^n(k/n)$$

At least $\lfloor n/2\rfloor$ factors are less than or equal to $1/2,$ while the remaining factors are less than or equal to $1.$ Therefore:

$$
0\leq\frac{n!}{n^n}
\leq\left(\frac{1}{2}\right)^{\lfloor n/2\rfloor}
\longrightarrow0
$$

When comparing sequences of the same type, the order depends on their parameters. If $0<r<s,$ then $n^r\ll n^s;$ if $1<a<b,$ then $a^n\ll b^n.$

The hierarchy also has a direct practical use, since it helps evaluate limits that cannot be handled immediately by the limit laws. For example, consider:

$$
a_n=\frac{2^n+n^5}{3^n+\ln n}
$$

This sequence tends to zero. In the denominator, $3^n$ dominates $\ln n,$ so we divide the numerator and denominator by $3^n:$

$$
a_n=\frac{(2/3)^n+n^5/3^n}{1+(\ln n)/3^n}
$$

The hierarchy gives $n^5/3^n\to0$ and $(\ln n)/3^n\to0.$ Moreover, the [geometric sequence](../geometric-sequence/) $(2/3)^n\to0$ because $0<2/3<1.$ Thus the numerator tends to $0,$ while the denominator tends to $1,$ and hence $a_n\to0.$

## Asymptotic behavior and standard limits

One way to compare two sequences is through their asymptotic behavior. A sequence $(a_n)$ is asymptotically equivalent to $(b_n)$ if:

$$
\lim_{n\to+\infty}\frac{a_n}{b_n}=1 \tag{1}
$$

Asymptotic equivalence is also written as $a_n\sim b_n$ and requires $b_n\neq0.$ Equation $(1)$ allows us to express [standard limits](../remarkable-limits/) as equivalences between sequences. For example, let $(x_n)$ be a sequence such that $x_n\to0$ and $x_n\neq0.$ Consider the standard limit:

$$\lim_{x\to0}\frac{\sin x}{x}=1$$

By equation $(1),$ we must have $\sin x_n\sim x_n.$ Applying the same reasoning to the standard limits listed below gives the following equivalences:

[class="table-1"]

|              |           |
| ------------ | --------- |
| $\sin x_n$   | $x_n$     |
| $\ln(1+x_n)$ | $x_n$     |
| $e^{x_n}-1$  | $x_n$     |
| $1-\cos x_n$ | $x_n^2/2$ |

[/class]

These equivalences are useful because they may be substituted into products and quotients to simplify the analysis of a sequence, provided that the denominators are eventually nonzero. Consider the following expression. Substituting the corresponding equivalents gives:

$$
\frac{(e^{2/n}-1)\ln(1+3/n)}{1-\cos(1/n)}
\sim
\frac{(2/n)(3/n)}{1/(2n^2)}=12
$$

As noted above, these substitutions are valid in products and quotients, but not term by term in a difference, because cancellation may remove the leading term that determines the behavior of the sequence and thereby change the limit.

Asymptotic equivalences can also be used to evaluate indeterminate products. For example, consider:

$$
a_n=n^\alpha\ln\left(1+\frac{1}{n}\right),\qquad \alpha>0
$$

The factor $n^\alpha$ tends to $+\infty,$ while $\ln(1+1/n)$ tends to $0,$ so direct substitution would produce the indeterminate form $\infty\cdot0.$ To apply the equivalence $\ln(1+x)\sim x,$ we compare the logarithm with $1/n:$

$$
a_n
=n^{\alpha-1}\frac{\ln(1+1/n)}{1/n}
\sim n^{\alpha-1}
$$

The quotient containing the logarithm tends to $1,$ so $a_n$ has the same behavior as $n^{\alpha-1}.$ Three cases follow: $a_n\to0$ when $0<\alpha<1,$ $a_n\to1$ when $\alpha=1,$ and $a_n\to+\infty$ when $\alpha>1.$

## Rationalization

Consider a difference of two terms that both tend to $+\infty,$ so that direct substitution produces the indeterminate form $+\infty-\infty.$ A fairly common case involves square roots. We then multiply and divide by their sum, called the conjugate. Let $A_n,B_n\geq0$ with $A_n+B_n>0.$ Then:

$$
\sqrt{A_n}-\sqrt{B_n}
=\frac{A_n-B_n}{\sqrt{A_n}+\sqrt{B_n}} \tag{2}
$$

Equation $(2)$ replaces the difference between the roots with the difference between the radicands. Consider the following example:

$$
\begin{align}
n\left(\sqrt{n^2+3}-n\right)
&=n\frac{(n^2+3)-n^2}{\sqrt{n^2+3}+n} \\[6pt]
&=\frac{3}{\sqrt{1+3/n^2}+1}
\longrightarrow\frac{3}{2}
\end{align}
$$

This identity is specific to square roots. To [rationalize](../radicals/) roots of higher order, we use the factorization of a difference of powers.

## Variable powers

Consider a sequence whose base and exponent both vary with $n.$ Its terms have the form $a_n=b_n^{c_n},$ where $b_n$ is the base and $c_n$ is the exponent. Direct substitution may produce indeterminate forms such as $1^\infty,$ $0^0,$ and $(+\infty)^0,$ which alone give no information about the behavior of the sequence. When $b_n>0$ eventually, we may rewrite the [power](../powers/) in terms of the product $c_n\ln b_n$ through the identity:

$$
a_n=e^{c_n\ln b_n} \tag{3}
$$

The limit therefore depends only on $c_n\ln b_n.$ If this product tends to some $\ell\in\mathbb{R},$ then $a_n\to e^\ell.$ If instead it tends to $-\infty$ or $+\infty,$ the power tends to $0$ or $+\infty,$ respectively. If $u_n\to0,$ $u_n\neq0$ eventually, and $c_nu_n\to\ell,$ then the asymptotic equivalence $\ln(1+u_n)\sim u_n$ gives:

$$
(1+u_n)^{c_n}\to e^\ell
$$

For a concrete example, consider the sequence:

$$
a_n=\left(\frac{n+2}{n-1}\right)^n
=\left(1+\frac{3}{n-1}\right)^n
$$

Its [logarithm](../logarithms/) can be written as:

$$
\ln a_n
=\frac{3n}{n-1}
\frac{\ln(1+3/(n-1))}{3/(n-1)}
\longrightarrow3
$$

It follows that $a_n\to e^3.$

## Oscillating sequences

Consider sequences that oscillate while remaining bounded in absolute value. Terms of this kind are called bounded perturbations. Examples are $\sin n$ and $\cos n,$ both of which have absolute value at most $1.$ When multiplied by a sequence tending to zero, their product tends to zero. Formally, if $(u_n)$ is bounded and $v_n\to0,$ then $u_nv_n\to0.$ For example:

$$
\left|\frac{\sin(n^2)}{\sqrt n}\right|
\leq\frac{1}{\sqrt n}\to0
$$

More generally, if $b_n\to\ell,$ $r_n\to0,$ and $|a_n-b_n|\leq r_n$ eventually, the [squeeze theorem](../squeeze-theorem/) gives $a_n\to\ell.$ For example, consider:

$$
a_n=\frac{2n+\sin n}{n+\cos n}
$$

For $n\geq2,$ we have:

$$
|a_n-2|
=\left|\frac{\sin n-2\cos n}{n+\cos n}\right|
\leq\frac{3}{n-1}\to0
$$

Therefore $a_n\to2,$ even though the trigonometric perturbations do not converge.
