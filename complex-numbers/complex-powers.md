---
title: Complex Powers
source: https://algebrica.org/complex-powers/
license: CC BY-NC 4.0
tags:
  - complex-exponential
  - complex-logarithm
  - complex-numbers
  - complex-powers
---
## Definition

The complex power with base $z\neq 0$ and exponent $a\in\mathbb{C}$ is the [set](../sets/) of values obtained by multiplying each [complex logarithm](../complex-logarithm/) of $z$ by $a$ and applying the exponential:

$$z^a:=\{\ e^{aw}\mid w\in\log z\ \} \tag{1}$$

Let $r=|z|$ be the [modulus](../complex-numbers/) and fix an argument $\theta$ of $z.$ Each integer $k$ determines a logarithm of $z$ with real part $\ln r$ and imaginary part $\theta+2k\pi.$ Substituting this logarithm for $w$ in $(1)$ gives the following value:

$$v_k(a)=e^{a(\ln r+i(\theta+2k\pi))} \tag{2}$$

As $k$ ranges over the integers, $(2)$ uses every logarithm of $z,$ so it gives the same set of values for $z^a$ regardless of which argument $\theta$ we start with. The principal value of the power $z^a$ is obtained using the principal logarithm $\mathrm{Log}(z),$ which takes the argument of $z$ in $(-\pi,\pi].$ In $(2)$ this choice corresponds to $k=0$ when $\theta=\mathrm{Arg}(z):$

$$z_{\mathrm{pr}}^a:=e^{a\mathrm{Log}(z)} \tag{3}$$

When $z=x>0,$ the principal logarithm is $\ln x,$ so for real $a$ the value in $(3)$ agrees with the corresponding [real power](../powers/). To calculate $i^i$ using $(2),$ we set $\ln r=0,$ $\theta=\pi/2$ and $a=i.$ The product of $i$ and $i(\pi/2+2k\pi)$ is real and equals $-\pi/2-2k\pi,$ so we obtain:

$$i^i=\{\ e^{-\pi/2-2k\pi}\mid k\in\mathbb{Z}\ \} \tag{4}$$

All the values in $(4)$ are positive real numbers, and setting $k=0$ gives the principal value $e^{-\pi/2}.$

## Properties

The first property concerns the number of distinct values of the complex power $z^a,$ which depends only on the exponent $a.$ To see why, we determine when two indices $k$ and $j$ give the same value of the power. We first subtract the exponents in the ratio $v_k(a)/v_j(a)$ of the values given by $(2).$ The terms involving the modulus $r$ and the argument $\theta$ cancel, leaving the ratio:

$$\frac{v_k(a)}{v_j(a)}=e^{2\pi i(k-j)a}$$

The values $v_k(a)$ and $v_j(a)$ coincide if and only if this ratio equals $1.$ The [complex exponential](../euler-formula/) equals $1$ precisely at integer multiples of $2\pi i,$ so:

$$
\begin{aligned}
v_k(a)=v_j(a) &\quad\Longleftrightarrow\quad e^{2\pi i(k-j)a}=1 \\[6pt]
              &\quad\Longleftrightarrow\quad (k-j)a\in\mathbb{Z}
\end{aligned} \tag{5}
$$

If the exponent is [rational](../rational-numbers/), we write $a=p/q$ in lowest terms, with $q>0,$ and apply $(5),$ which states that $v_k(a)$ and $v_j(a)$ coincide if and only if $(k-j)p/q$ is an integer. Since $p$ and $q$ are [coprime](../greatest-common-divisor/), this happens when $k-j$ is a multiple of $q,$ so the values repeat every $q$ indices, and the indices from $0$ to $q-1$ give all $q$ distinct values of the power because no two distinct indices in this range differ by a multiple of $q.$

For an integer exponent $a=n,$ the denominator is $q=1,$ so there is a single value and it agrees with the usual [integer power](../de-moivre-theorem/) because $e^{nw}=(e^w)^n=z^n$ for every logarithm $w$ of $z.$ For $a=1/q,$ on the other hand, we obtain all the $q$th [roots](../complex-numbers-exponential-form/) of $z.$ Indeed, for every logarithm $w$ of $z,$ raising $e^{w/q}$ to the power $q$ gives $e^w=z.$

Finally, when $a$ is an [irrational real number](../irrational-numbers/) or has a nonzero imaginary part, no nonzero integer multiple of $a$ is an integer, so by $(5)$ distinct indices give distinct values and the power has infinitely many values.

- - -

The exponent addition rule gives the following identity for every pair of exponents $a,b\in\mathbb{C}$:

$$e^{aw}e^{bw}=e^{(a+b)w} \tag{6}$$

Varying $w$ in $(6)$ gives all the values of $z^{a+b},$ while choosing $w=\mathrm{Log}(z)$ for both factors gives the same identity for the principal values. If the logarithm is chosen separately for each factor, the product can take additional values, as when we multiply the [two square roots](../roots-of-unity/) of $1,$ namely $1$ and $-1,$ to obtain $-1,$ whereas the only value of $1^1$ is $1.$ For a power of a [product](../complex-number-operations/), if $w_1$ and $w_2$ are logarithms of $z_1$ and $z_2,$ then $w_1+w_2$ is a logarithm of $z_1z_2,$ and this choice gives the following identity:

$$e^{a(w_1+w_2)}=e^{aw_1}e^{aw_2} \tag{7}$$

Even when $w_1$ and $w_2$ are the principal logarithms, their sum may have an imaginary part outside $(-\pi,\pi],$ in which case the left-hand side of $(7)$ is evaluated using a logarithm other than the principal one. This happens when $z_1=z_2=-1$ and $a=1/2,$ because the principal value of the power of the product is $1,$ whereas the product of the principal values is $i\cdot i=-1.$

The choice of logarithm also matters when raising a power to another power, because if $u=e^{aw}$ is a value of $z^a,$ using $aw$ as a logarithm of $u$ gives $e^{baw}$ as a value of $u^b.$ The principal logarithm of $u$ can give a different result, as it does for $z=-1,$ $a=2$ and $b=1/2,$ when squaring and then taking the principal value of the square root gives $1,$ whereas the power with exponent $ab=1$ equals $-1.$
