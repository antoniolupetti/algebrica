---
title: Hierarchy of Growth Rates
source: https://algebrica.org/hierarchy-of-growth-rates/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - exponential-functions
  - growth-rates
  - limits
  - logarithms
  - powers
---
## Hierarchy of growth rates

The hierarchy of growth rates is a method for calculating [limits](../limits/) involving [logarithms](../logarithms/), [powers](../powers/), and [exponentials](../exponential-function/) by identifying which terms in an expression become negligible relative to the others, and is useful, for example, in resolving certain [indeterminate forms](../indeterminate-forms/). When considering a limit at $\infty,$ some functions grow more slowly than others, which allows us to make observations that help determine their behavior. Consider the following parameters: 

$$ \tag{1}
\begin{align}
p &> 0 \\[6pt]
0 &< \alpha < \beta \\[6pt]
1 &< a < b
\end{align}
$$

We can then write the following chain of inequalities, which shows the growth rates of the individual functions in increasing order from left to right:

$$
(\ln x)^p \ll x^\alpha \ll x^\beta \ll a^x \ll b^x \ll e^{x^2}
\qquad

\tag{2}
$$

In $(2),$ the symbol $\ll$ indicates that the ratio of the function on the left to the function on the right tends to zero. In the specific case of $(2),$ as $x$ tends to $+\infty$ all the functions tend to $+\infty,$ but at different rates. In general, saying that $f$ grows more slowly than $g$ means that, for every positive constant $M,$ the inequality $g>Mf$ holds for all sufficiently large $x.$ This comparison requires more than a simple inequality $f(x)<g(x):$ for example, $x$ is always less than $2x$ for $x>0,$ but their ratio does not tend to zero:

$$
\lim_{x\to+\infty}\frac{x}{2x}=\frac12\ne0
\tag{3}
$$

Thus, $(3)$ shows that $x$ is not negligible relative to $2x,$ whereas in the hierarchy in $(2),$ each function becomes negligible relative to the next. To calculate these limits, we therefore need to compare the ratios after simplifying any cancellations between terms.

## Comparison using ratios

We begin by comparing two positive functions through the limit of their ratio. For sufficiently large $x,$ if this limit is zero, the numerator is negligible relative to the denominator, whereas if the limit is a positive constant, the two functions have the same order of magnitude. In the first case, we introduce [little-o notation](../little-o-notation/), with reference to the limit under consideration, and write:

$$
\lim_{x\to+\infty}\frac{f(x)}{g(x)}=0
\quad\Longleftrightarrow\quad f(x)=o(g(x))
\tag{4}
$$

In the second case, we have:

$$
\lim_{x\to+\infty}\frac{f(x)}{g(x)}=L,
\qquad 0\lt L \lt+\infty
\tag{5}
$$

In $(5),$ we say that $f(x)$ is asymptotically equivalent to $Lg(x)$ and, when $L=1,$ the functions are asymptotically equivalent, which we write as:

$$f(x)\sim g(x)\tag{6}$$ 
For example, we compare $3x^2$ with $x^2,$ then $x^2+x$ with $x^2,$ by calculating the ratio of the first function to the second in each pair:

$$
\begin{align}
\lim_{x\to+\infty}\frac{3x^2}{x^2}&=3 \\[6pt]
\lim_{x\to+\infty}\frac{x^2+x}{x^2}
&=\lim_{x\to+\infty}\left(1+\frac1x\right)=1
\end{align}
\tag{7}
$$

The first limit in $(7)$ shows that $3x^2$ and $x^2$ have the same order because their ratio tends to a finite positive constant, whereas in the second limit the ratio tends to $1,$ so the numerator and denominator are asymptotically equivalent by $(6).$ Now consider the case in which the limit of the ratio gives:
$$\frac{f(x)}{g(x)}\to+\infty \tag{8}$$

The result in $(8)$ means that $g$ is negligible relative to $f.$ Bear in mind that not every pair of functions admits this type of comparison, since in some cases the ratio may have no limit, as in the following example:

$$
\frac{(2+\sin x)x}{x}=2+\sin x \tag{9}
$$

As $x\to+\infty,$ the ratio in $(9)$ has no limit because it oscillates between $3$ when $x=\pi/2+2k\pi$ and $1$ when $x=3\pi/2+2k\pi$. Thus, the hierarchy of growth rates can only be applied when the ratio has a definite limiting behavior.

## Comparisons within the same family

Before comparing different families of functions, it is useful to check how growth rates change with the exponents and bases. To clarify this, consider the ratio of two powers of $x,$ which, by the laws of exponents, can be written as follows when $x\to+\infty$ and $\alpha<\beta$: 

$$
\frac{x^\alpha}{x^\beta}=x^{\alpha-\beta}
\longrightarrow0
\tag{10}
$$

Since the exponent $\alpha-\beta$ in $(10)$ is negative, the ratio tends to zero, which means that the power with the smaller exponent is negligible relative to the other. Another common case is the ratio of exponentials with exponent $x,$ which, for $x \to \infty$ and $1<a<b,$ can be rewritten as:

$$
\frac{a^x}{b^x}=\left(\frac{a}{b}\right)^x \longrightarrow0
\tag{11}
$$

In $(11),$ the base $a/b$ lies in the interval $(0,1),$ so the ratio tends to zero, and therefore the exponential with the smaller base is always negligible relative to the one with the larger base. Now consider positive powers of the logarithm, for which the same comparison of exponents as in $(10)$ applies, because $\ln x\to+\infty.$ Indeed, when $x\to+\infty$ and $0<p<q,$ the ratio can be rewritten as:

$$
\frac{(\ln x)^p}{(\ln x)^q}=(\ln x)^{p-q}\longrightarrow0
\tag{12}
$$

In $(12),$ the exponent $p-q$ is negative, so the power of the logarithm with the smaller exponent is negligible relative to the one with the larger exponent.

In $(12),$ we compared powers of the same logarithm, changing only the exponent, but the situation changes if we keep the exponent equal to $1$ and change the base of the logarithm instead. Take $a,b>1$ and apply the change-of-base formula to the following ratio:

$$
\frac{\log_a x}{\log_b x}=\frac{\ln b}{\ln a}
\tag{13}
$$

The logarithms in $(13)$ therefore differ only by a constant factor and consequently have the same order.

## Logarithms, powers, and exponentials

Having compared functions within the same family, we now consider comparisons between different families. The first concerns powers of the logarithm and powers of $x.$ We know that however large $p>0$ is and however small $\alpha>0$ is, the function $(\ln x)^p$ grows more slowly than $x^\alpha,$ so their ratio tends to zero:

$$
\lim_{x\to+\infty}\frac{(\ln x)^p}{x^\alpha}=0
\tag{14}
$$

The second comparison concerns powers of $x$ and exponentials $a^x$ with base $a>1,$ which grow more rapidly than any power $x^\alpha$ with constant exponent $\alpha>0.$ For example, $x^{100}$ is negligible relative to $2^x,$ and in general we have:

$$
\lim_{x\to+\infty}\frac{x^\alpha}{a^x}=0
\tag{15}
$$

Both comparisons can be proved by starting with $(15).$ We use the [Taylor series expansion](../taylor-series/) of the exponential, given by:

$$
e^u=\sum_{n=0}^{\infty}\frac{u^n}{n!}
=1+u+\frac{u^2}{2!}+\frac{u^3}{3!}+\cdots
$$

We then choose an integer $k>\alpha$ and set $u=x\ln a,$ obtaining:

$$a^x=e^{x\ln a}\ge \frac{(x\ln a)^k}{k!} \tag{16}$$ 
Using $(16),$ we obtain an upper bound for the ratio and can write the following relation:

$$
0\le\frac{x^\alpha}{a^x}
\le\frac{k!x^\alpha}{(x\ln a)^k}
=\frac{k!}{(\ln a)^k}\frac{1}{x^{k-\alpha}}
\longrightarrow0
\tag{17}
$$

Since $k-\alpha>0,$ the final expression tends to zero, and the [squeeze theorem](../squeeze-theorem/) gives precisely $(15).$ To derive $(14),$ we set $t=\ln x,$ so that $x=e^t$ and $t\to+\infty,$ and can therefore write: 

$$
\frac{(\ln x)^p}{x^\alpha}
=\frac{t^p}{e^{\alpha t}}
=\frac{t^p}{(e^\alpha)^t}
\longrightarrow0
\tag{18}
$$

In $(18),$ the denominator is an exponential with base $e^\alpha>1,$ so $(15)$ applies to the variable $t$ and gives the required limit. It remains to prove the last step in the hierarchy in $(2),$ where $e^{x^2}$ grows more rapidly than $b^x.$ Writing $b^x=e^{x\ln b},$ we obtain:

$$\tag{19}
\frac{b^x}{e^{x^2}}=e^{x\ln b-x^2}
$$

The term $x^2$ in the exponent in $(19)$ grows more rapidly than $x\ln b,$ which grows linearly because $\ln b$ is a constant, so $x\ln b-x^2$ tends to $-\infty$ and the exponential tends to zero. We can therefore conclude that $b^x$ is negligible relative to $e^{x^2}.$

## Products of powers and logarithms

Limits often involve products of factors from different families, and in these cases the first step is to simplify the ratio using, for example, the laws of powers and logarithms. For example, consider the following ratio and its rewritten form:

$$
\frac{x^\alpha(\ln x)^p}{x^\beta(\ln x)^q}=x^{\alpha-\beta}(\ln x)^{p-q}
\tag{20}
$$

When $\alpha<\beta,$ the expression in $(20)$ tends to zero regardless of the value of $p-q,$ and when this difference is positive, we use $(14).$ When the difference is zero or negative, the logarithmic factor is bounded for sufficiently large $x$ and the factor $x^{\alpha-\beta}$ tends to zero. When $\alpha>\beta,$ the ratio tends to $+\infty.$ When $\alpha=\beta,$ the powers of $x$ cancel, and the comparison depends only on the exponents of the logarithm. The same reasoning extends to products of the following form, with fixed parameters and $a>1$: 

$$a^xx^\alpha(\ln x)^p\tag{21}$$ 
If the bases of the exponentials in $(21)$ are different, the product with the larger base grows more rapidly, whereas if the bases are equal, the exponential factors cancel and we compare the exponents of $x.$ Finally, if those exponents are also equal, we compare the exponents of the logarithm, as in $(12).$ To see why the larger base determines the comparison in $(21),$ we compare two products with $1<a<b$ by writing their ratio as follows: 

$$
\frac{a^xx^\alpha(\ln x)^p}{b^xx^\beta(\ln x)^q}
=\frac{x^{\alpha-\beta}(\ln x)^{p-q}}{(b/a)^x}
\tag{22}
$$

In $(22),$ the base $b/a$ is greater than $1,$ the logarithm in the numerator grows more slowly than a power of $x,$ as shown by $(14),$ and by $(15)$ every power of $x$ grows more slowly than the exponential in the denominator. The ratio therefore tends to zero.

## Limits of sums and ratios of sums

These comparisons also allow us to calculate limits of sums and ratios of sums by following a simple principle based on the growth of one of the terms. When one term grows more rapidly than the others, it is said to dominate them, while the others remain negligible relative to it, so it determines the behavior of the sum. Suppose we have the following sum, where $c\ne0$ is a constant and $r(x)$ collects all the terms that are negligible relative to $g(x):$

$$F(x)=cg(x)+r(x) \tag{23}$$  
To verify that the sum in $(23)$ behaves like the term $cg(x)$ alone, we rewrite $(23)$ as follows:

$$
\frac{F(x)}{cg(x)}
=1+\frac{r(x)}{cg(x)}
\longrightarrow1
\tag{24}
$$

The ratio in $(24)$ tends to $1,$ so $F(x)\sim cg(x).$ For example, as $x\to+\infty,$ the dominant terms in the following ratio are $2^x$ and $3x^3,$ so the limit is infinite:

$$
\frac{2^x+x^{10}+\ln x}{3x^3+(\ln x)^2}
\sim\frac{2^x}{3x^3}
\longrightarrow+\infty
\tag{25}
$$

When the dominant terms have the same order, the limit can instead be finite and nonzero, as in the following example.

$$
\frac{5x^2\ln x+x^2}{2x^2\ln x+e^{-x}}
\sim\frac{5x^2\ln x}{2x^2\ln x}
=\frac52
\tag{26}
$$

In the ratios in $(25)$ and $(26),$ we replaced the numerator and denominator with their respective dominant terms, but differences require greater care because the same procedure can give an incorrect result when the leading terms cancel. Consider the following example:

$$
\lim_{x\to+\infty}\left(\sqrt{x^2+x}-x\right) \tag{27}
$$

In $(27),$ as $x\to+\infty$ we have $\sqrt{x^2+x}\sim x,$ but replacing the square root with $x$ would give zero. To calculate the limit, we must therefore retain the full expression and rewrite it by multiplying the numerator and denominator by its conjugate:

$$
\begin{align}
\sqrt{x^2+x}-x
&=\frac{(\sqrt{x^2+x}-x)(\sqrt{x^2+x}+x)}{\sqrt{x^2+x}+x} \\[6pt]
&=\frac{x}{\sqrt{x^2+x}+x} \\[6pt]
&=\frac{1}{\sqrt{1+1/x}+1}\longrightarrow\frac12
\end{align}
\tag{28}
$$

## Infinitesimals and limits at zero

Now consider functions that tend to zero and are therefore infinitesimals. We begin with a simple example, considering $a^x,$ which grows more rapidly than $x^\alpha,$ and its reciprocal $a^{-x},$ which tends to zero more rapidly than $x^{-\alpha}.$ Indeed, the ratio $a^{-x}/x^{-\alpha}=x^\alpha/a^x$ tends to zero by $(15).$ Applying the same reasoning to the comparison between powers and logarithms in $(14),$ for $p,\alpha>0$ and $a>1$ we obtain:

$$
a^{-x}\ll x^{-\alpha}\ll\frac{1}{(\ln x)^p}
\qquad (x\to+\infty)
\tag{29}
$$

For example, $x^\alpha e^{-x}\to0,$ since the product can be rewritten as $x^\alpha/e^x.$ This method is useful for resolving indeterminate forms of the type $0\cdot\infty$ by reducing them to a known comparison. The same hierarchy allows us to calculate limits as $x\to0^+,$ as in the following example:

$$
\lim_{x\to0^+}x\ln\frac1x \tag{30}
$$

In $(30),$ attempting to evaluate the limit by direct substitution gives an indeterminate form of the type $0\cdot\infty.$ To resolve it, we make the substitution $t=1/x,$ so that $x=1/t,$ and obtain:

$$
\lim_{x\to0^+}x\ln\frac1x
=\lim_{t\to+\infty}\frac{\ln t}{t}
=0
\tag{31}
$$

Now consider a second example, with $\alpha>0:$

$$ \tag{32}
\lim_{x\to0^+}\frac{e^{-1/x}}{x^\alpha}
$$

The numerator and denominator in $(32)$ both tend to zero, and applying the same substitution as before, $t=1/x,$ transforms the numerator into $e^{-t}$ and the denominator into $t^{-\alpha},$ so we obtain:

$$
\lim_{x\to0^+}\frac{e^{-1/x}}{x^\alpha}
=\lim_{t\to+\infty}\frac{t^\alpha}{e^t}
=0
\tag{33}
$$

Equation $(15)$ gives the limit in $(33),$ which shows that $e^{-1/x}$ tends to zero more rapidly than every positive power of $x.$