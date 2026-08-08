---
title: Powers, Radicals and Logarithms
source: https://algebrica.org/category/powers-radicals-logarithms/
license: CC BY-NC 4.0
tags:
  - exponential-function
  - logarithms
  - nth-root
  - powers
  - radicals
  - rational-exponent
---
## Introduction to the chapter

For a real number $a$ and a positive integer $n,$ the power $a^n$ is the product of $n$ factors equal to $a:$

$$a^n = \underbrace{a \cdot a \cdot a \cdots a}_{n \text{ times}}$$

The number $a$ is the base, and $n$ is the exponent. The relation $a^n = b$ leads to three questions, each corresponding to a topic of this chapter. [Powers](../../powers/) determine $b$ from the base and the exponent. [Radicals](../../radicals/) determine the possible values of the base from the exponent and the result. [Logarithms](../../logarithms/) determine the exponent from the base and the result.

Repeated multiplication defines $a^n$ only for positive integer exponents. For $a \neq 0,$ the zero power is $a^0 = 1.$ For $a \neq 0$ and every positive integer $n,$ a negative exponent is the reciprocal of the corresponding positive power:

$$a^{-n} = \frac{1}{a^n}$$

The equation $x^n = a,$ with $n \in \mathbb{N}$ and $n \ge 2,$ asks for a base whose $n$-th power equals $a.$ When $a \ge 0,$ the principal $n$-th root $\sqrt[n]{a}$ is the unique non-negative real number with this property. The parity of the index determines which radicands are admissible. For even $n,$ the equation has no real solutions when $a < 0,$ has the single solution $x = 0$ when $a = 0,$ and has the two solutions $\sqrt[n]{a}$ and $-\sqrt[n]{a}$ when $a > 0.$ For odd $n,$ every real number $a$ has exactly one real $n$-th root.

For $a > 0,$ $m \in \mathbb{Z},$ and a positive integer $n,$ a power with rational exponent $m/n$ can be written in radical notation as follows:

$$a^{\frac{m}{n}} = \sqrt[n]{a^m}$$

The preceding radical identity does not cover $2^{\sqrt{2}},$ since $\sqrt{2}$ cannot be written as $m/n$ with $m \in \mathbb{Z}$ and $n$ a positive integer. For $a > 0$ and $x \in \mathbb{R},$ the definition of a real power in terms of the [exponential function](../../exponential-function/) and the natural logarithm is:

$$a^x = e^{x \ln a}$$

The condition $a > 0$ is required because $\ln a$ has no real value when $a \le 0.$ For rational exponents, this definition agrees with the radical one.

In the third question, the base and the result are known, while the exponent is unknown. For $a, b > 0$ with $a \neq 1,$ the logarithm of $b$ to the base $a$ is the exponent to which $a$ must be raised to obtain $b:$

$$\log_a b = c \iff a^c = b$$

The base must differ from $1$ because $1^x = 1$ for every real $x,$ so the corresponding exponential function is constant and has no [inverse function](../../inverse-function/).

The exponent rules give the corresponding logarithmic identities. For $a > 0$ with $a \neq 1,$ $x, y > 0,$ and $n \in \mathbb{R},$ these identities are:

$$
\begin{align}
\log_a(xy) &= \log_a x+\log_a y \\[6pt]
\log_a\frac{x}{y} &= \log_a x-\log_a y \\[6pt]
\log_a(x^n) &= n\log_a x
\end{align}
$$

In group-theoretic language, the first identity states that $\log_a$ is a homomorphism from the multiplicative group $(0,+\infty)$ to the additive group $\mathbb{R}.$ Since $\log_a$ is bijective, it is an isomorphism between these groups.

The chapter begins with [powers](../../powers/), where the exponent rules are established for integer exponents and then extended to real ones. The properties of radicals and logarithms are derived from these rules.
