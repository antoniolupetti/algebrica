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

## Sequence limits that are not straightforward

One of the main difficulties in computing limits lies in the wide variety of cases that may arise in their study. For [sequences](../sequences/), determining the limit is not always easy or immediate. For example, when we encounter sequences that reduce to an [indeterminate form](../indeterminate-forms/) such as $0/0,$ $+\infty/+\infty,$ $0\cdot\infty,$ or $+\infty-\infty,$ the [limit laws](../algebra-of-limits/) alone are no longer sufficient to determine whether the sequence converges. In cases of this kind, we must use different tools and examine, for example, the structure and behavior of the components involved.

In general, it is important to remember that the limit of a sequence depends exclusively on its tail. This is fairly intuitive in itself: the more consistently a sequence behaves in a certain way from some point onward, the more closely it approaches a given value and, in that case, it [converges](../convergent-and-divergent-sequences/). Otherwise, it diverges. In practical terms, suppose that two sequences $(a_n)$ and $(b_n)$ satisfy $a_n=b_n$ for every $n\geq n_0.$ It is fairly intuitive that, from index $n_0$ onward, the two sequences have the same behavior and therefore the same limit. This reasoning allows us to disregard conditions that affect only the initial terms and impose different conditions from some index $n_i$ onward, substantially simplifying the calculation.

Several approaches are available for evaluating less straightforward limits, depending on the properties of the terms that make up a given sequence. The following sections discuss them in detail.

## Dominant terms

One of the simplest methods uses what are known as dominant terms. When the limit of a sequence involves a ratio of [polynomials](../polynomials/), we divide both the numerator and the denominator by the highest power of $n$ occurring in either polynomial. Consider the simple case of the limit of the following sequence:

$$\lim_{n\to+\infty}\frac{4n^3-5n+1}{2n^3+n^2-7}$$

Evaluating the sequence directly as $n$ tends to infinity produces the indeterminate form $\infty/\infty,$ which gives no information about its behavior. Dividing the numerator and denominator instead by the highest power of $n$ gives:

$$\lim_{n\to+\infty}\frac{4-5/n^2+1/n^3}{2+1/n-7/n^3}=2$$

More generally, if $P$ and $Q$ have degrees $p$ and $q$ and leading coefficients $a$ and $b,$ the following identity holds:

$$
\frac{P(n)}{Q(n)}
=n^{p-q}\frac{a+o(1)}{b+o(1)}
$$

The [little-o notation](../little-o-notation/) $o(1)$ concisely collects all the terms that tend to zero. In this way, three cases arise when evaluating the ratio:

+ in the first case, the ratio tends to $0$ when $p<q;$
+ in the second case, it tends instead to $a/b$ when $p=q;$
+ in the final case, when $p>q,$ its [absolute value](../absolute-value/) tends to infinity and the ratio eventually has the sign of $a/b.$

- - -

The same procedure, which consists of factoring out the power of $n$ with the larger exponent, is also used for sums of powers. For example, consider the difference $n^\alpha-3n^\beta$ with $\alpha<\beta.$ Factoring out the power with the larger exponent gives:

$$
n^\alpha-3n^\beta
=n^\beta\left(n^{\alpha-\beta}-3\right)
$$

Since $n^{\alpha-\beta}$ tends to zero, the factor in parentheses tends to $-3,$ and the dominant term is $-3n^\beta.$

- - -

Another case arises when a square factor must be extracted from a square root. Since the radicand must always be greater than or equal to zero, for every value of $n$ we have:

$$\sqrt{n^2}=|n|$$

The use of the absolute value is therefore required. If we consider the limit $n\to+\infty,$ then $n$ is eventually positive, so $|n|=n,$ and we may write, for example, $\sqrt{n^2+3}=n\sqrt{1+3/n^2}.$

## Growth hierarchies

When $n\to+\infty,$ for every choice of constants $p,q>0$ and $a>1,$ the following growth hierarchy holds:

$$
(\ln n)^p\ll n^q\ll a^n\ll n!\ll n^n
$$

The general notation $u_n\ll v_n$ means that the ratio $u_n/v_n\to0.$ This is equivalent to saying that the sequence to the left of $\ll$ grows more slowly than the sequence immediately to its right. For example, the ratio $(\ln n)^p/n^q$ tends to $0,$ and the same holds for each of the other adjacent pairs, with the entry in position $i$ in the numerator and the entry in position $i+1$ in the denominator.

To make the comparisons explicit, consider the first relation, $(\ln n)^p\ll n^q.$ Setting $t=\ln n,$ the ratio becomes:

$$
\frac{(\ln n)^p}{n^q}
=\frac{t^p}{e^{qt}}
\longrightarrow0
$$

For the two comparisons $n^q\ll a^n$ and $a^n\ll n!,$ we instead define $d_n=n^q/a^n$ and $c_n=a^n/n!.$ The ratios of consecutive terms satisfy the following identities:

$$
\begin{align}
\frac{d_{n+1}}{d_n}&=\frac{(1+1/n)^q}{a}\longrightarrow\frac{1}{a}<1 \\[6pt]
\frac{c_{n+1}}{c_n}&=\frac{a}{n+1}\longrightarrow0
\end{align}
$$

Both sequences therefore tend to zero.

Finally, consider the last case, involving the [factorial](../factorial/). We may first write the following identity:

$$n!/n^n=\prod_{k=1}^n(k/n)$$

At least $\lfloor n/2\rfloor$ factors are less than or equal to $1/2,$ while the remaining factors are less than or equal to $1.$ The relation can therefore be written as the following estimate:

$$
0\leq\frac{n!}{n^n}
\leq\left(\frac{1}{2}\right)^{\lfloor n/2\rfloor}
\longrightarrow0
$$

When comparing sequences of the same form, the order depends instead on their parameters. If $0<r<s,$ then $n^r\ll n^s,$ whereas if $1<a<b,$ then $a^n\ll b^n.$

The growth hierarchy is therefore a theoretical tool with an important practical application. It allows us to evaluate limits of sequences that cannot be handled immediately by the limit laws and that appear complicated at first sight. For example, consider the following sequence:

$$
a_n=\frac{2^n+n^5}{3^n+\ln n}
$$

This sequence tends to zero. Indeed, in the denominator $3^n$ dominates $\ln n,$ so we divide the numerator and denominator by $3^n:$

$$
a_n=\frac{(2/3)^n+n^5/3^n}{1+(\ln n)/3^n}
$$

The hierarchy gives $n^5/3^n\to0$ and $(\ln n)/3^n\to0.$ Moreover, [$(2/3)^n$](../geometric-sequence/) tends to $0$ because $0<2/3<1.$ The numerator therefore tends to $0,$ while the denominator tends to $1,$ and hence $a_n\to0.$

## Asymptotic behavior and standard limits

One way to compare two sequences is to use their asymptotic behavior. A sequence $(a_n)$ is said to be asymptotically equivalent to $(b_n)$ if the following equality holds:

$$
\lim_{n\to+\infty}\frac{a_n}{b_n}=1 \tag{1}
$$

Asymptotic equivalence is also written as $a_n\sim b_n$ and requires $b_n\neq0.$ From equation $(1),$ we can express [standard limits](../remarkable-limits/) as equivalences between sequences. For example, let $(x_n)$ be a sequence such that $x_n\to0$ and $x_n\neq0.$ Consider the following standard limit:

$$\lim_{x\to0}\frac{\sin x}{x}=1$$

Again by equation $(1),$ we must have $\sin x_n\sim x_n.$ If we apply the same reasoning to the fundamental limits, we obtain the following equivalences:

[class="table-1"]

| Expression | Asymptotic equivalent |
| ---------- | --------------------- |
| $\sin x_n$ | $x_n$                |
| $\ln(1+x_n)$ | $x_n$              |
| $e^{x_n}-1$ | $x_n$                |
| $1-\cos x_n$ | $x_n^2/2$          |

[/class]

These equivalences are very useful because asymptotically equivalent factors can replace one another in products and quotients, simplifying the analysis of a sequence's behavior, provided that the denominators are eventually nonzero. For example, consider the following sequence. Applying the appropriate substitutions yields the following asymptotic relation:

$$
\frac{(e^{2/n}-1)\ln(1+3/n)}{1-\cos(1/n)}
\sim
\frac{(2/n)(3/n)}{1/(2n^2)}=12
$$

As mentioned earlier, asymptotically equivalent factors can replace one another in products and quotients, but not term by term in a difference, because their leading terms may cancel, and replacing the terms individually could therefore alter the value obtained for the limit.

The use of these equivalent forms also makes it possible to evaluate limits involving indeterminate products. For example, consider the following sequence:

$$
a_n=n^\alpha\ln\left(1+\frac{1}{n}\right),\qquad \alpha>0
$$

The factor $n^\alpha$ tends to $+\infty,$ while $\ln(1+1/n)$ tends to $0,$ so direct substitution would produce the indeterminate form $\infty\cdot0.$ To apply the equivalence $\ln(1+x)\sim x,$ we must compare the logarithm with $1/n:$

$$
a_n
=n^{\alpha-1}\frac{\ln(1+1/n)}{1/n}
\sim n^{\alpha-1}
$$

The quotient containing the logarithm tends to $1,$ so the behavior of $a_n$ is the same as that of $n^{\alpha-1}.$ Three cases follow: $a_n\to0$ when $0<\alpha<1,$ $a_n\to1$ when $\alpha=1,$ and $a_n\to+\infty$ when $\alpha>1.$

## Rationalization

We now consider two terms in a difference that both tend to $+\infty$ and therefore produce the indeterminate form $+\infty-\infty$ under direct substitution. One situation that is not uncommon involves a difference of square roots. In this case, it is useful to multiply and divide by their sum, also called the conjugate expression. For example, let $A_n,B_n\geq0$ with $A_n+B_n>0.$ Then:

$$
\sqrt{A_n}-\sqrt{B_n}
=\frac{A_n-B_n}{\sqrt{A_n}+\sqrt{B_n}} \tag{2}
$$

Equation $(2)$ eliminates the difference between the roots and replaces it with the difference between the radicands. Consider the following example:

$$
\begin{align}
n\left(\sqrt{n^2+3}-n\right)
&=n\frac{(n^2+3)-n^2}{\sqrt{n^2+3}+n} \\[6pt]
&=\frac{3}{\sqrt{1+3/n^2}+1}
\longrightarrow\frac{3}{2}
\end{align}
$$

Identity $(2)$ applies only to square roots. When roots of higher order occur, we first [rationalize](../radicals/) the expression using the factorization of a difference of powers.

## Variable powers

We now consider a sequence involving a variable [power](../powers/), namely, a sequence whose terms have the form $a_n=b_n^{c_n},$ where both the base $b_n$ and the exponent $c_n$ may depend on $n.$ In this case as well, direct substitution when computing the limit may produce indeterminate forms of the type $1^\infty,$ $0^0,$ and $(+\infty)^0,$ which give no information about the behavior of the sequence. When $b_n>0$ eventually, we can use $\ln b_n$ to reduce the analysis of the power to that of the product $c_n\ln b_n$ through the identity:

$$
a_n=e^{c_n\ln b_n} \tag{3}
$$

The limit therefore depends only on $c_n\ln b_n.$ If this product tends to a value $\ell\in\mathbb{R},$ then $a_n\to e^\ell.$ If instead it tends to $-\infty$ or $+\infty,$ the power tends to $0$ or $+\infty,$ respectively. Recalling the standard limits and their asymptotic behavior, suppose that $u_n\to0,$ $u_n\neq0$ eventually, and $c_nu_n\to\ell.$ The standard logarithmic limit, written asymptotically as $\ln(1+u_n)\sim u_n,$ then gives:

$$
(1+u_n)^{c_n}\to e^\ell
$$

To clarify the method with an example, consider the following sequence:

$$
a_n=\left(\frac{n+2}{n-1}\right)^n
=\left(1+\frac{3}{n-1}\right)^n
$$

Its [logarithm](../logarithms/) satisfies the following relation:

$$
\ln a_n
=\frac{3n}{n-1}
\frac{\ln(1+3/(n-1))}{3/(n-1)}
\longrightarrow3
$$

It follows from this that $a_n\to e^3.$

## On oscillating sequences

We now consider oscillating sequences whose absolute values remain bounded by a fixed constant and which are referred to here as perturbations. Examples are $\sin n$ and $\cos n,$ which oscillate while their absolute values never exceed $1.$ When such a sequence is multiplied by a sequence tending to zero, its contribution tends to zero. In formal terms, if $(u_n)$ is bounded and $v_n\to0,$ then $u_nv_n\to0.$ For example:

$$
\left|\frac{\sin(n^2)}{\sqrt n}\right|
\leq\frac{1}{\sqrt n}\to0
$$

More generally, if $b_n\to\ell,$ $r_n\to0,$ and $|a_n-b_n|\leq r_n$ eventually, the [squeeze theorem](../squeeze-theorem/) gives $a_n\to\ell.$ For example, consider the following sequence:

$$
a_n=\frac{2n+\sin n}{n+\cos n}
$$

For $n\geq2,$ the following estimate holds:

$$
|a_n-2|
=\left|\frac{\sin n-2\cos n}{n+\cos n}\right|
\leq\frac{3}{n-1}\to0
$$

Therefore $a_n\to2,$ even though the trigonometric perturbations do not converge.
