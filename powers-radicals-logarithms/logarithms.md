---
title: Logarithms
source: https://algebrica.org/logarithms/
license: CC BY-NC 4.0
tags:
  - change-of-base
  - exponential-inverse
  - logarithmic-function
  - logarithmic-properties
  - logarithms
---
## Definition

The logarithm of a number is the exponent to which a given base must be raised to obtain that number. For example, $\log_2 8 = 3$ because $2^3 = 8.$ Formally, if $a$ and $b$ are positive [real numbers](../properties-of-real-numbers/), the logarithm of $b$ to base $a$ is the real number $c$ such that $a^c = b.$ We can express this relationship as follows:

$$\log_a b = c \iff a^c = b \tag{1}$$

$a$ is the base of the logarithm, while $b$ is its argument. For $(1)$ to be well-defined, the following conditions must hold:

+ $a > 0$ because a zero or negative base does not allow real powers to be defined for every real exponent.
+ $a \neq 1$ because $1^c = 1$ for every $c,$ so the equation has no solutions if $b \neq 1$ and infinitely many if $b = 1.$
+ $b > 0$ because every power of a positive base is positive, so $a^c$ cannot be zero or negative.

From $(1),$ we can therefore deduce that taking a logarithm is the inverse operation of exponentiation. Using the [properties of powers](../powers/) and $(1),$ we can derive the following identities:

$$a^0 = 1 \Rightarrow \log_a 1 = 0$$

$$a^1 = a \Rightarrow \log_a a = 1$$

Two particular types of logarithm are quite common, namely natural logarithms and common logarithms. Natural logarithms, or logarithms to base $e,$ are denoted by $\ln x,$ where the constant $e$ is [Euler's number](../euler-number-limit-sequence/), and are used in differential and integral calculus. Logarithms to base $10,$ on the other hand, are denoted by $\log_{10}x$ or $\log x.$ These are very useful because they allow us to compare the orders of magnitude of numbers. For example, whenever a positive number is multiplied by $10,$ its common logarithm increases by $1$ (the numbers $10,$ $100$ and $1000$ have logarithms $1,$ $2$ and $3$, respectively).

> Fixing a base $a > 0,$ with $a \neq 1,$ and allowing the argument $x > 0$ to vary gives the [logarithmic function](../logarithmic-function/), whose graph and analytic properties we study in the dedicated article.

## Properties

Logarithms satisfy several algebraic properties that allow us to rewrite expressions in simpler forms and make calculations easier. In all the properties below, the base satisfies $a > 0$ and $a \neq 1.$ For $x,y > 0,$ we begin with the product rule, which expresses the logarithm of a product as the sum of the logarithms of its factors:

$$
\log_a(xy) = \log_a x + \log_a y \tag{2}
$$

Identity $(2)$ follows from the properties of powers, and to prove it we set $u = \log_a x$ and $v = \log_a y,$ so that, by definition, $x = a^u$ and $y = a^v.$ As we know, the product of two powers with the same base is obtained by adding their exponents, so we can write the product as follows:

$$xy = a^u a^v = a^{u+v}$$

The exponent to which $a$ must be raised to obtain $xy$ is therefore $u+v,$ so the definition of a logarithm gives precisely $(2).$

- - -

For $x,y > 0,$ the second property expresses the logarithm of a quotient as the difference between the logarithm of the numerator and the logarithm of the denominator, giving the following identity:

$$ \tag{3}
\log_a{\frac{x}{y}} = \log_a x - \log_a y
$$

Again, to prove $(3),$ we use a property of powers. We set $u = \log_a x$ and $v = \log_a y,$ so that $x = a^u$ and $y = a^v.$ The quotient of two powers with the same base is obtained by subtracting their exponents, so we can write:

$$\frac{x}{y} = \frac{a^u}{a^v} = a^{u-v}$$

By $(1),$ the exponent $u-v$ is the logarithm of $x/y$ to base $a,$ which gives $(3).$ As a special case, setting $x = 1$ gives:

$$
\log_a{\frac{1}{y}} = -\log_a y
$$

Thus, the logarithm of the reciprocal of $y$ is the negative of the logarithm of $y.$

- - -

For $x > 0$ and $n \in \mathbb{R},$ another useful property is the power rule, which states that the logarithm of a power equals the exponent multiplied by the logarithm:

$$ \tag{4}
\log_a x^n = n\log_a x
$$

To prove it, we set $u = \log_a x,$ and the definition of a logarithm gives $x = a^u.$ Raising both sides to the power $n$ and using the rule for a power of a power, we obtain:

$$x^n = (a^u)^n = a^{nu}$$

By $(1),$ the exponent to which $a$ must be raised to obtain $x^n$ is therefore $nu.$ Since $u = \log_a x,$ identity $(4)$ follows.

Identity $(4)$ requires the argument of the logarithm to be positive. For example, $\log_a(x^2)$ is defined for every $x \neq 0,$ even when $x$ is negative. In this case, since $x^2 = |x|^2,$ the formula valid for all admissible values is $\log_a(x^2) = 2\log_a|x|.$ The expression $2\log_a x,$ however, is defined only for $x > 0.$

- - -

Identity $(4)$ gives the rule for the logarithm of a [radical](../radicals/), valid for $b > 0$ and $n \in \mathbb{N}$ with $n \ge 2.$ Since a radical can be written as a power with a [rational exponent](../rational-numbers/) ($\sqrt[n]{b} = b^{1/n}$), we obtain:
$$ \tag{5}
\log_a\sqrt[n]{b} = \frac{1}{n}\log_a b
$$

- - -

Suppose that $x,y,z > 0,$ and let us apply the properties just discussed to the following expression:

$$ \tag{6}
\log_a \left( \frac{x^3 \cdot y}{z^2} \right)
$$

We begin by observing that $(6)$ contains a quotient within the argument of the logarithm, so we can apply $(3)$ and rewrite the expression as:

$$ \tag{7}
\log_a(x^3 \cdot y) - \log_a(z^2)
$$

The first logarithm contains a product, and by $(2)$ we can rewrite it as:

$$
\log_a(x^3 \cdot y) = \log_a(x^3) + \log_a(y)
$$

Expression $(7)$ then becomes:

$$
\log_a(x^3) + \log_a(y) - \log_a(z^2)
$$

Finally, the power rule allows us to rewrite the first and third logarithms using $(4)$ to obtain:

$$ \tag{8}
3 \log_a(x) + \log_a(y) - 2 \log_a(z)
$$


## Changing the base of a logarithm

The change-of-base formula allows us to express any logarithm in terms of logarithms to a base for which values are known or calculation tools are available, such as base $e$ or base $10.$ It is also very useful when working with expressions because it allows logarithms with different bases to be expressed in terms of logarithms with the same base, making calculations easier. Suppose that $a,b>0,$ $a,b\neq1$ and $x>0.$ The change-of-base formula is:

$$\log_a x = \frac{\log_b x}{\log_b a} \tag{9}$$

To prove it, we set $y=\log_a x,$ and the definition of a logarithm gives the equality $a^y=x.$ Taking the logarithm to base $b$ of both sides gives:

$$\log_b(a^y) = \log_b(x)$$

On the left-hand side, we can use the power rule given in $(4)$ to obtain:

$$y\log_b(a) = \log_b(x)$$

Solving for $y$ gives precisely $(9).$ As a concrete example, let us show how changing the base allows us to evaluate the following expression.

$$\log_2 3 \cdot \log_3 8 \tag{10}$$

If we rewrite the second logarithm from base $3$ to base $2,$ we obtain a common factor in the numerator and denominator that we can cancel. Using $(9),$ we can rewrite $(10)$ and obtain the following result:

$$
\begin{align}
\log_2 3 \cdot \log_3 8 &= \log_2 3 \cdot \frac{\log_2 8}{\log_2 3} \\[6pt]
&= \log_2 8 \\[6pt]
&= 3
\end{align}
$$

## Logarithms and algebraic structures

The properties of logarithms can be interpreted in the language of abstract algebra, which studies [sets](../sets/) and the operations defined on them. In this setting, the product rule $(2)$ allows us to interpret the logarithm as a correspondence between two algebraic structures.

As we know, the set of positive real numbers is a [group](../groups/) under multiplication, with identity element $1$ and the inverse of any element $x$ equal to $1/x.$ The real numbers, on the other hand, form a group under addition, with identity element $0$ and the inverse of each element $u$ equal to $-u.$ The logarithm associates a real number with each positive number and transforms multiplication in the first group into addition in the second, according to identity $(2).$

A correspondence of this kind, which preserves the operations of the two groups, is a [homomorphism](../homomorphisms-and-isomorphisms/). This correspondence also preserves the identity elements and inverses of the two groups. Indeed, $\log_a 1 = 0$ maps the multiplicative identity to the additive identity, while $\log_a(1/x) = -\log_a x$ maps the reciprocal of $x$ to the negative of its logarithm.

Moreover, every real number $u$ is the logarithm of a unique positive number $a^u.$ The correspondence is therefore [bijective](../injective-surjective-and-bijective-functions/) and hence a [group isomorphism](../homomorphisms-and-isomorphisms/).
