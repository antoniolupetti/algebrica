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
## Introduction to powers

For a real [number](../types-of-numbers/) $a$ and a positive integer $n,$ the power $a^n$ is the product of $n$ factors equal to $a:$

$$a^n = \underbrace{a \cdot a \cdot a \cdots a}_{n \text{ times}}$$

The number $a$ is the base, and $n$ is the exponent.

> For a positive number $a,$ the expression $a^2$ is the area of a square with side length $a,$ while $a^3$ is the volume of a cube with edge length $a.$

- - -

Integer powers extend this definition to zero and negative exponents. For $a \neq 0$ and every positive integer $n,$ a negative exponent is defined by:

$$a^{-n} = \frac{1}{a^{n}}$$

The negative power is therefore the reciprocal of the corresponding positive power. For $a > 0$ and every positive integer $m,$ an exponent of the form $1/m$ is defined through a [radical](../radicals/):

$$a^{\frac{1}{m}} = \sqrt[m]{a}$$

This expression is the positive $m$-th root of $a.$ Combining the two definitions gives:

$$a^{-\frac{1}{m}} = \frac{1}{\sqrt[m]{a}}$$

Fractional and negative exponents defined in this way satisfy the same exponent rules as positive integer powers.

The table below shows selected values of $a^n$ where each row corresponds to a fixed base $a$ and each column to a fixed exponent $n.$

|      | $a^{-2}$ | $a^{-1}$ | $a^{0}$ | $a^{1}$ | $a^{2}$ | ... |
| :--: | :------: | :------: | :-----: | :-----: | :-----: | :-: |
| $-2$ |  $1/4$   |  $-1/2$  |   $1$   |  $-2$   |   $4$   | ... |
| $-1$ |   $1$    |   $-1$   |   $1$   |  $-1$   |   $1$   | ... |
| $0$  | undefined | undefined | undefined |   $0$   |   $0$   | ... |
| $1$  |   $1$    |   $1$    |   $1$   |   $1$   |   $1$   | ... |
| $2$  |  $1/4$   |  $1/2$   |   $1$   |   $2$   |   $4$   | ... |
| ...  |   ...    |   ...    |   ...   |   ...   |   ...   | ... |

> Negative powers of zero require division by zero. The expression $0^0$ is left undefined here, while the symbol $0^0$ denotes an [indeterminate form](../indeterminate-forms/) in limit problems.

If the base $a$ is negative and $n$ is an integer, the sign of $a^n$ depends on the parity of $n.$ For instance, $(-1)^n = 1$ when $n$ is even, and $(-1)^n = -1$ when $n$ is odd. If $a < 0$ and $p/q$ is in lowest terms with $q > 0,$ then $a^{p/q}$ has a real value exactly when $q$ is odd. Thus $(-8)^{1/3} = -2,$ while $(-1)^{1/2}$ has no value in $\mathbb{R}.$

## Powers with real exponents

Repeated multiplication defines $a^n$ only when $n$ is a positive [integer](../integers/). To define powers with [real](../properties-of-real-numbers/) exponents, we use the [exponential function](../exponential-function/) and the [natural logarithm](../logarithms/). For $a > 0$ and $x \in \mathbb{R},$ define:

$$a^x = e^{x \ln a}$$

For positive integer exponents, this definition agrees with repeated multiplication. The radical definition of a rational power assigns $\sqrt[q]{a^p}$ to the exponent $p/q,$ where $p \in \mathbb{Z}$ and $q$ is a positive integer. Set $y = e^{(p/q)\ln a}.$ Then $y > 0$ and:

$$y^q = e^{p \ln a} = a^p$$

Since $y$ is positive, it is the positive $q$-th root of $a^p.$ The exponential and radical definitions therefore give the same value:

$$e^{\frac{p}{q} \ln a} = \sqrt[q]{a^p}$$

The expression $2^{\sqrt{2}}$ requires the real-exponent definition because $\sqrt{2}$ is irrational and has no representation as a ratio of integers. It gives:

$$2^{\sqrt{2}} = e^{\sqrt{2} \ln 2} \approx e^{0.9803} \approx 2.665$$

The condition $a > 0$ is required because $\ln a$ has no real value when $a \leq 0.$ The rational powers of a negative base described above do not define $a^x$ for every real exponent $x.$ For every $a > 0,$ the function $f(x) = a^x$ is [continuous](../continuous-functions/) and [differentiable](../derivatives/) on $\mathbb{R}.$

## Fundamental rules of powers

For the algebraic rules involving arbitrary real exponents, every base is positive. With integer exponents, bases may be real whenever all powers and quotients involved are defined. Positive powers of zero are stated separately.

Raising any nonzero base to the exponent zero gives $1.$ The restriction on $a$ is necessary because $0^0$ is left undefined under the convention used here.

$$a^0 = 1 \quad \text{if} \quad a \neq 0$$

- - -

For a positive integer $n,$ the power $0^n$ is a product of $n$ zeros. More generally, $0^x$ is defined as $0$ for every positive real exponent $x:$

$$0^x = 0 \quad \text{for } x > 0$$

Under the convention used here, $0^0$ is undefined. Two limiting paths toward the pair $(0,0)$ give different values:

$$
\begin{align}
\lim_{x \to 0^+} 0^x &= 0 \\[6pt]
\lim_{x \to 0} x^0 &= 1
\end{align}
$$

Thus no continuous definition at $(0,0)$ can agree with both expressions. In [limits](../limits/), the symbols $0^0,$ $1^{\infty},$ and $\infty^0$ denote indeterminate forms whose values depend on the functions involved.

> In combinatorics and algebra, $0^0$ is often defined as $1$ because this convention preserves formulas such as the [binomial theorem](../binomial-theorem/).

- - -

The product of two powers with the same base $a$ is a power with base $a$ whose exponent is the sum of the original exponents:

$$a^n \cdot a^m = a^{n+m}$$

For positive integer exponents, $a^n$ is the product of $n$ factors equal to $a,$ and $a^m$ is the product of $m$ such factors. Joining the products gives $n+m$ factors:

$$
a^n \cdot a^m = \underbrace{a \cdot a \cdots a}_{n \text{ times}} \cdot \underbrace{a \cdot a \cdots a}_{m \text{ times}} = \underbrace{a \cdot a \cdots a}_{n+m \text{ times}} = a^{n+m}
$$

For arbitrary real exponents and $a > 0,$ the same rule follows from $a^x = e^{x \ln a}$ and $e^u \cdot e^v = e^{u+v}:$

$$a^n \cdot a^m = e^{n \ln a} \cdot e^{m \ln a} = e^{(n+m) \ln a} = a^{n+m}$$

- - -

The product of powers with different bases $a$ and $b$ but the same exponent $n$ is a power whose base is the product of the original bases.

$$a^{n} \cdot b^n = (ab)^n$$

> For example, $2^3 \cdot 5^3 = (2 \cdot 5)^3 = 10^3$ because both factors have exponent $3.$

- - -

The quotient of two powers with the same base $a$ is a power with the same base and exponent equal to the difference between the exponents.

$$\frac{a^n}{a^m} = a^{n-m}$$

This follows directly from the product rule established above. Dividing by $a^m$ is equivalent to multiplying by $a^{-m},$ so the quotient can be rewritten as follows:

$$\frac{a^n}{a^m} = a^n \cdot a^{-m} = a^{n+(-m)} = a^{n-m}$$

The quotient requires $a \neq 0$ so that the denominator $a^m$ and its reciprocal are defined.

- - -

The quotient of powers with different bases $a$ and $b$ but the same exponent $n$ is a power whose base is the quotient of the original bases. The denominator requires $b \neq 0.$

$$\frac{a^n}{b^n} = \left(\frac{a}{b}\right)^n$$

> For example, $6^3/2^3 = \left(6/2\right)^3 = 3^3 = 27$ because the numerator and denominator have exponent $3.$

- - -

The power of a power is a power with the same base and exponent equal to the product of the two exponents.

$$(a^m)^n = a^{m \cdot n}$$

> For example, $(2^3)^4 = 2^{3 \cdot 4} = 2^{12}$ because the exponents multiply.

- - -

For $a > 0$ and every real number $n > 0,$ a negative power is the reciprocal of the corresponding positive power. When $n$ is an integer, the same rule holds for every $a \neq 0:$

$$a^{-n} = \frac{1}{a^n}$$

- - -

When the exponent is rational, the power can be expressed as a radical. If the base depends on a variable, this notation may define an [irrational function](../irrational-functions/).

$$a^{\frac{m}{n}} = \sqrt[n]{a^m} \quad \text{where} \quad a > 0, \quad m \in \mathbb{Z}, \quad n \in \mathbb{N}, \quad n > 0$$

## Why is $a^0 = 1$?

For $a \neq 0$ and every positive integer $n,$ division of $a^n$ by itself gives:

$$\frac{a^n}{a^n} = 1$$

The quotient rule gives another expression for the same quotient:

$$\frac{a^n}{a^n} = a^{n-n} = a^0$$

Therefore $a^0 = 1.$ The condition $a \neq 0$ is necessary because the quotient $a^n/a^n$ must be defined.

## Bernoulli's inequality

Bernoulli's inequality states that for every real number $x \ge -1$ and every positive integer $n,$ we have:

$$
(1+x)^n \ge 1+nx
$$

The condition $x \ge -1$ makes the base $1+x$ non-negative. Equality holds when $n = 1$ or when $x = 0;$ in every other case the inequality is strict.

A proof proceeds by induction on $n.$ For $n = 1$ both sides equal $1+x.$ Assume that the inequality holds for some $n \ge 1:$

$$
(1+x)^n \ge 1+nx
$$

Multiplication by the non-negative quantity $1+x$ preserves the direction of the inequality:

$$
(1+x)^{n+1} \ge (1+nx)(1+x) = 1+(n+1)x+nx^2
$$

Since $nx^2 \ge 0,$ the right-hand side is at least $1+(n+1)x:$

$$
(1+x)^{n+1} \ge 1+(n+1)x
$$

This establishes the statement for $n+1$ and completes the induction.

> The inequality extends to real exponents $r \ge 1$ when $x \ge -1$ and to $r \le 0$ when $x > -1;$ it reverses for $0 < r < 1$ when $x \ge -1.$ These statements follow from the convexity or concavity of the [power function](../power-function/) $t \mapsto t^r.$

- - -

Bernoulli's inequality proves that the sequence $a_n = \left(1+\frac{1}{n}\right)^n$ is strictly increasing. For $n \ge 1,$ the ratio of consecutive terms is:

$$
\frac{a_{n+1}}{a_n}
= \left(1+\frac{1}{n+1}\right)
\left(1-\frac{1}{(n+1)^2}\right)^n
$$

Applying Bernoulli's inequality with $x = -1/(n+1)^2$ gives:

$$
\begin{align}
\frac{a_{n+1}}{a_n}
&\ge \left(1+\frac{1}{n+1}\right)
\left(1-\frac{n}{(n+1)^2}\right) \\[6pt]
&= 1+\frac{1}{(n+1)^3} \\[6pt]
&> 1
\end{align}
$$

The sequence also has an upper bound, as shown in [Euler's number](../euler-number-limit-sequence/). Since it is increasing and bounded, it converges, and its limit defines the number $e:$

$$
e = \lim_{n \to +\infty}\left(1+\frac{1}{n}\right)^n
$$

## Power and exponential

A power $a^n$ has a specified base and exponent. A power function has the form $f(x) = x^r,$ with fixed exponent $r,$ while in an [exponential function](../exponential-function/) the variable is in the exponent. An exponential function has the form:

$$f(x) = e^x \quad \text{or} \quad f(x) = a^x$$

In the second expression, $a > 0$ and $a \neq 1.$

## Hierarchy of growth rates

The hierarchy of growth rates compares functions that tend to infinity. For every $\alpha > 0$ and every $a > 1,$ logarithms, positive powers, and exponentials satisfy:

$$
\lim_{x \to +\infty} \frac{\log_a x}{x^{\alpha}} = 0
\qquad \text{and} \qquad
\lim_{x \to +\infty} \frac{x^{\alpha}}{a^{x}} = 0
$$

The first limit states that every positive power of $x$ eventually exceeds the logarithm in relative growth. The second states that every exponential with base greater than $1$ eventually exceeds every positive power of $x$ in relative growth. Thus logarithms grow more slowly than positive powers, and positive powers grow more slowly than exponentials.

> For every $\varepsilon > 0,$ one can choose $x_0$ so that the corresponding quotient is less than $\varepsilon$ whenever $x > x_0.$ The required value of $x_0$ depends on $\alpha$ and $a.$

- - -

The second limit implies the first. If $y = \log_a x,$ then $x = a^y$ and:

$$
\frac{\log_a x}{x^\alpha}
= \frac{y}{(a^\alpha)^y}
\longrightarrow 0
$$

Here $a^\alpha > 1,$ so the expression on the right is a case of the second limit. To prove that limit, write $a^x = e^{x \ln a}.$ The Taylor series for the exponential gives the following estimate for every positive integer $k$ and every $u \ge 0:$

$$
e^{u} \ge \frac{u^{k}}{k!} \qquad k \ge 1, \quad u \ge 0
$$

Choose an integer $k > \alpha$ and set $u = x \ln a.$ For $x > 0,$ it follows that:

$$
0 \le \frac{x^\alpha}{a^x}
\le \frac{k!}{(\ln a)^k}x^{\alpha-k}
\longrightarrow 0
$$

- - -

If one term in a finite sum has a strictly greater growth rate than every other term, then it determines the leading-order behavior. For example:

$$
\lim_{x \to +\infty} \frac{2^{x}+x^{10}+\ln x}{2^{x}} = 1
$$

The contributions of $x^{10}$ and $\ln x$ become negligible compared with $2^{x}$ as $x$ tends to infinity, even though the [polynomial](../polynomials/) term may be larger for moderate values of $x.$ The same hierarchy distinguishes logarithmic, polynomial, and exponential running times in the classification of algorithmic complexity.

## Powers with complex exponents

For $a > 0$ and $z \in \mathbb{C},$ a power with a complex exponent is defined by $a^z = e^{z \ln a}.$ The complex exponential is defined by its convergent [Taylor series](../taylor-series/):

$$e^z = \sum_{n=0}^{\infty} \frac{z^n}{n!}$$

For $\theta \in \mathbb{R},$ substituting $z = i\theta$ and separating the even and odd powers of $i$ gives Euler's formula:

$$e^{i\theta} = \cos\theta + i\sin\theta$$

The formula gives the real and imaginary parts of $e^{i\theta}.$ Every nonzero [complex number](../complex-numbers-introduction/) can be written as $z = re^{i\theta},$ where $r > 0$ is its modulus and $\theta$ is an argument, defined modulo $2\pi.$ Setting $\theta = \pi$ gives Euler's identity:

$$e^{i\pi} + 1 = 0$$

A more detailed discussion of complex exponents, including methods for computing powers and roots of complex numbers, appears on the page [complex numbers in exponential form](../complex-numbers-exponential-form/).
