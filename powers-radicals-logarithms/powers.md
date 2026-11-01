---
title: Powers
source: https://algebrica.org/powers/
license: CC BY-NC 4.0
tags:
  - exponential
  - exponents
  - logarithms
  - power-rules
  - powers
---
## Introduction

The power $a^n$ of a [real number](../real-numbers/) $a$ (called the base) with a [positive integer](../integers/) $n$ (called the exponent) is the product of $n$ factors equal to $a:$

$$a^n = \underbrace{a \cdot a \cdots a}_{n \text{ times}}\tag{1}$$

Integer powers extend definition $(1)$ to zero and negative exponents. For $a \neq 0$ and any positive integer $n,$ a power with a negative exponent is defined as the reciprocal:

$$a^{-n} = \frac{1}{a^{n}} \tag{2}$$

For $a > 0$ and any positive integer $m,$ a power with an exponent of the form $1/m$ is defined using a [radical](../radicals/):

$$a^{\frac{1}{m}} = \sqrt[m]{a} \tag{3}$$

Combining $(2)$ and $(3)$ gives the following identity:

$$a^{-\frac{1}{m}} = \frac{1}{\sqrt[m]{a}} \tag{4}$$

The following table lists some values of $a^n.$ Each row corresponds to a fixed base $a$ and each column to a fixed exponent $n.$

|      | $a^{-2}$ | $a^{-1}$ | $a^{0}$ | $a^{1}$ | $a^{2}$ | ... |
| :--: | :------: | :------: | :-----: | :-----: | :-----: | :-: |
| $-2$ |  $1/4$   |  $-1/2$  |   $1$   |  $-2$   |   $4$   | ... |
| $-1$ |   $1$    |   $-1$   |   $1$   |  $-1$   |   $1$   | ... |
| $0$  | undefined | undefined | undefined |   $0$   |   $0$   | ... |
| $1$  |   $1$    |   $1$    |   $1$   |   $1$   |   $1$   | ... |
| $2$  |  $1/4$   |  $1/2$   |   $1$   |   $2$   |   $4$   | ... |
| ...  |   ...    |   ...    |   ...   |   ...   |   ...   | ... |

Consider the specific case of a negative base. In this case, the exponent determines both whether the power has a real value and its sign. Indeed, when $a \lt 0$ and $n$ is an integer, the sign of $a^n$ depends on the parity of $n.$ For example, $(-1)^n$ equals $1$ when $n$ is even and $-1$ when $n$ is odd. When $a < 0$ and the exponent is a fraction $p/q$ in lowest terms with $q > 0,$ the power $a^{p/q}$ has a real value if and only if $q$ is odd. Thus $(-8)^{1/3} = -2,$ whereas $(-1)^{1/2}$ has no value in $\mathbb{R}.$

- - -

Definition $(1)$ defines $a^n$ only when $n$ is a positive integer, whereas powers with real exponents require the [exponential function](../exponential-function/) and the [natural logarithm](../logarithmic-function/), as follows. For a base $a > 0$ and $x \in \mathbb{R},$ we have:

$$a^x = e^{x \ln a} \tag{5}$$

This definition agrees with $(1)$ for positive integer exponents and with radicals for rational exponents. Indeed, if $p \in \mathbb{Z}$ and $q$ is a positive integer, we have:

$$a^{p/q} = e^{\frac{p}{q}\ln a} = \sqrt[q]{a^p} \tag{6}$$

The same definition allows us to calculate powers with irrational exponents, such as:

$$2^{\sqrt{2}} = e^{\sqrt{2}\ln 2} \approx 2.665$$

In this case, the base must be positive because the real logarithm is defined only when its argument is greater than zero.

## Properties of powers

The basic properties of powers allow us to rewrite expressions in equivalent forms and simplify calculations. We begin with a nonzero base raised to the power zero. For any base $a \gt 0,$ the following relation holds:

$$a^0 = 1 \tag{7}$$
As the table above also shows, powers of zero with negative exponents are undefined because they would require division by zero. The expression $0^0$ is also undefined because no value can be assigned to it that makes the power function continuous at the origin $(0,0).$ Recall that, when calculating [limits](../limits/), $0^0$ is an [indeterminate form](../indeterminate-forms/) that cannot be resolved by direct substitution but requires appropriate techniques described on the page devoted to this topic. In combinatorics and algebra, the following convention preserves the validity of formulas such as the [binomial theorem](../binomial-theorem/), allowing terms with exponent zero to be evaluated even when one of the bases is zero:

$$0^0=1 \tag{8}$$

For a positive integer $n,$ the power $0^n$ is a product of $n$ zeros, and more generally, for positive real exponents, the expression $0^x$ is defined as:

$$0^x = 0 \tag{9}$$
- - -

We now consider a further property concerning the product of two powers with the same base $a.$ In this case, the following identity holds:

$$a^n \cdot a^m = a^{n+m} \tag{10}$$

Identity $(10)$ follows directly from definition $(1).$ For positive integer exponents, $a^n$ is the product of $n$ factors equal to $a$ and $a^m$ is the product of $m$ factors also equal to $a.$ We therefore obtain $n+m$ factors equal to the base $a,$ which we can write as:

$$ \tag{11}
a^n \cdot a^m = \underbrace{a \cdot a \cdots a}_{n \text{ times}} \cdot \underbrace{a \cdot a \cdots a}_{m \text{ times}} = \underbrace{a \cdot a \cdots a}_{n+m \text{ times}} = a^{n+m}
$$

For arbitrary real exponents and $a > 0,$ identity $(5)$ gives:

$$a^n \cdot a^m = e^{n \ln a} \cdot e^{m \ln a} = e^{(n+m) \ln a} = a^{n+m}\tag{12}$$

When multiplying powers with different bases and the same exponent, the following identity holds for $a,b > 0$ and $n \in \mathbb{R}:$

$$a^{n} \cdot b^n = (ab)^n\tag{13}$$

- - -

For the quotient of two powers with the same base $a,$ the following relation holds.

$$\frac{a^n}{a^m} = a^{n-m} \tag{14}$$

This property follows directly from $(10).$ Indeed, dividing by $a^m$ is equivalent to multiplying by $a^{-m},$ so we can rewrite $(14)$ as:

$$\frac{a^n}{a^m} = a^n \cdot a^{-m} = a^{n+(-m)} = a^{n-m}$$

Relation $(14)$ requires $a \neq 0$ so that the denominator $a^m$ and its reciprocal are defined. When the quotient involves different bases with the same exponent $n,$ for $a,b > 0$ and $n \in \mathbb{R}$ we obtain the counterpart of $(13):$

$$\frac{a^n}{b^n} = \left(\frac{a}{b}\right)^n \tag{15}$$

- - -

For a power raised to another power, with $a > 0$ and $m,n \in \mathbb{R},$ the following relation holds, in which the exponents are multiplied:

$$(a^m)^n = a^{m \cdot n}\tag{16}$$

When the exponent is rational, the power can be expressed using a radical, as we saw in $(3).$ For $a \gt 0,$ $m \in \mathbb{Z}$ and $n \in \mathbb{N}$ with $n\gt 0,$ we obtain:

$$a^{\frac{m}{n}} = \sqrt[n]{a^m} \tag{17}$$

- - -

Using property $(14),$ we can show why $a^0=1.$ We start with the following identity:

$$\frac{a^n}{a^n} = 1$$

Rewriting it using the difference of the exponents gives:

$$\frac{a^n}{a^n} = a^{n-n} = a^0 = 1$$

Finally, we mention [Bernoulli's inequality](../bernoulli-inequality/), which gives a lower bound for the power $(1+x)^n$ by stating that $(1+x)^n \ge 1+nx$ for $x \ge -1$ and every positive integer $n,$ and which is discussed on a separate page.

## Powers with complex exponents

So far, we have considered powers with real exponents, but we can also define powers whose exponents belong to the field of [complex numbers](../complex-numbers/). For a base $a > 0$ and $z \in \mathbb{C},$ we define a power with a complex exponent as:

$$a^z = e^{z \ln a} \tag{18}$$

To derive $(18),$ we use the [Taylor series](../taylor-series/) of the real exponential function, which converges for every $w \in \mathbb{C}:$

$$e^w = \sum_{n=0}^{\infty} \frac{w^n}{n!}$$

When $w = i\theta,$ with $\theta \in \mathbb{R},$ the terms with even powers of $i$ form the cosine series, while those with odd powers form $i$ times the sine series, giving [Euler's formula](../eulers-formula/):

$$e^{i\theta} = \cos\theta + i\sin\theta \tag{19}$$

Using $(19),$ we can calculate the power defined in $(18).$ Indeed, writing $z = u+iv,$ with $u,v \in \mathbb{R},$ we obtain:

$$a^{u+iv} = e^{u\ln a}e^{iv\ln a} = a^u\bigl(\cos(v\ln a) + i\sin(v\ln a)\bigr)$$

The real part of the power is $a^u\cos(v\ln a),$ while $a^u\sin(v\ln a)$ is the imaginary part. In the particular case $\theta = \pi,$ Euler's formula gives $e^{i\pi} = -1,$ from which Euler's identity follows:

$$e^{i\pi} + 1 = 0 \tag{20}$$

Euler's formula also allows us to write every nonzero complex number in the form $re^{i\theta},$ where $r > 0$ is its modulus and $\theta$ is an argument, defined modulo $2\pi.$ This representation and the methods for calculating powers and roots of complex numbers are discussed on the page on [complex numbers in exponential form](../complex-numbers-exponential-form/).
