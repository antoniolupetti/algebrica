---
title: Operations with Complex Numbers
source: https://algebrica.org/complex-number-operations/
license: CC BY-NC 4.0
tags:
  - complex-conjugate
  - complex-division
  - complex-multiplication
  - complex-numbers
  - complex-reciprocal
  - complex-sum
  - field-operations
---
## Introduction

A [complex number](../complex-numbers-introduction/) $z$ is an expression of the form $z = a + bi$, where $a$ and $b$ are [real numbers](../properties-of-real-numbers/) and $i$ is the imaginary unit, characterized by the defining relation $i^2 = -1$.

The [real number](../real-numbers/) $a$ is called the real part of $z$ and is denoted by $\mathrm{Re}(z)$. The real number $b$ is called the imaginary part and is denoted $\mathrm{Im}(z)$. The set of all complex numbers is defined as follows:

$$\mathbb{C} := \\{\ z = a + bi \mid a, b \in \mathbb{R} \ \\}$$

Every real number $a \in \mathbb{R}$ can be identified with the complex number $a + 0i$, so $\mathbb{R}$ embeds naturally into $\mathbb{C}$ as a subfield.

- - -

The [set](/..sets/) $\mathbb{C}$, equipped with the addition and multiplication defined in the sections below, forms a [field](../fields/). Before examining these operations, it is useful to recall the field axioms that govern the arithmetic of complex numbers.

+ Closure: for any $z_1, z_2 \in \mathbb{C}$, the sum $z_1 + z_2$ and the product $z_1 \cdot z_2$ both belong to $\mathbb{C}$.
+ Commutativity and associativity: addition and multiplication are commutative and associative, in strict analogy with $\mathbb{R}$.
+ Neutral elements: the number $0 = 0 + 0i$ is the additive identity, and $1 = 1 + 0i$ is the multiplicative identity.
+ Additive inverse: for every $z = a + bi$, the additive inverse is $-z = -a - bi$, and one has $z + (-z) = 0$.
+ Multiplicative inverse: for every $z \neq 0$, there exists a unique $z^{-1} \in \mathbb{C}$ such that $z \cdot z^{-1} = 1$. Its explicit form is derived in the section on division below.
+ Distributivity: for all $z_1, z_2, z_3 \in \mathbb{C}$, the product distributes over the sum according to the following identity:

$$z_1 \cdot (z_2 + z_3) = z_1 \cdot z_2 + z_1 \cdot z_3$$

Two structural properties distinguish $\mathbb{C}$ from $\mathbb{R}$. First, unlike $\mathbb{R}$, the field $\mathbb{C}$ is not an ordered [field](../fields/). There is no total order on $\mathbb{C}$ compatible with its field operations, and expressions such as $z_1 < z_2$ are therefore undefined for general complex numbers.

Second, $\mathbb{C}$ is algebraically closed. Every nonconstant [polynomial](../polynomials/) with coefficients in $\mathbb{C}$ has at least one root in $\mathbb{C}$. This result, known as the [fundamental theorem of algebra](../roots-of-a-polynomial/), has no analogue in $\mathbb{R}$, where polynomials such as $x^2 + 1$ admit no [real roots](../roots-of-a-polynomial/).

## Sum and difference of complex numbers

The sum and difference of two complex numbers are defined componentwise, by operating separately on the real and imaginary parts. Given $z_1 = a + bi$ and $z_2 = c + di$, the definitions are the following.

$$z_1 + z_2 = (a + c) + (b + d)i$$

$$z_1 - z_2 = (a - c) + (b - d)i$$

- - -

Let $z_1 = 2 - 3i$ and $z_2 = 3 + 5i$. To compute $z_1 - z_2$, we subtract the real parts and the imaginary parts separately. Subtracting $z_2$ is equivalent to adding the additive inverse $-z_2 = -3 - 5i$, so the operation reduces to a componentwise subtraction.

$$
\begin{align}
z_1 - z_2 &= (2 - 3i) - (3 + 5i) \\[6pt]
          &= (2 - 3) + (-3 - 5)i \\[6pt]
          &= -1 - 8i
\end{align}
$$

Let $z_1 = -4 + 2i$ and $z_2 = 6 - 7i$. To compute $z_1 + z_2$, we add the real parts and the imaginary parts separately, since addition in $\mathbb{C}$ acts componentwise by definition.

$$
\begin{align}
z_1 + z_2 &= (-4 + 2i) + (6 - 7i) \\[6pt]
          &= (-4 + 6) + (2 - 7)i \\[6pt]
          &= 2 - 5i
\end{align}
$$

> The sum and difference of complex numbers inherit from the field structure of $\mathbb{C}$ all the algebraic properties that hold in $\mathbb{R}$: commutativity, associativity, and distributivity with respect to multiplication.

- - -

From a geometric point of view, complex numbers can be interpreted as [vectors](../vectors/) in the complex plane, where the horizontal axis represents the real part and the vertical axis represents the imaginary part. Given two complex numbers $z_1$ and $z_2$, represented as vectors from the origin, their sum $z_1 + z_2$ corresponds to vector addition by the parallelogram rule.

+ The vector corresponding to $z_2$ is translated so that its tail coincides with the tip of the vector corresponding to $z_1$.
+ The vector drawn from the origin to the new tip represents the resulting complex number $z_1 + z_2$.

![IMG. 1](svg/complex-number-operations-1.svg)

The two constructions together provide a complete geometric interpretation of addition and subtraction in the complex plane.

The difference $z_1 - z_2$ is obtained by adding $z_1$ to the additive inverse $-z_2$, whose vector is the reflection of $z_2$ through the origin. Geometrically, $z_1 - z_2$ corresponds to the vector from the tip of $z_2$ to the tip of $z_1$, when both vectors originate at the origin.

## Product of complex numbers

The product of two complex numbers is defined by applying the distributive property and the fundamental relation $i^2 = -1$. Given $z_1 = a + bi$ and $z_2 = c + di$, expanding the product yields the following.

$$(a + bi)(c + di) = (ac - bd) + (ad + bc)i$$

This formula need not be memorized as a rule: it is simply the result of distributing the multiplication and substituting $i^2 = -1$, as shown in the examples below.

An important property of multiplication in $\mathbb{C}$ is the multiplicativity of the modulus. Recalling that [the modulus](../complex-numbers-introduction/) of $z = a + bi$ is defined as $|z| = \sqrt{a^2 + b^2}$, one can verify that for any $z_1, z_2 \in \mathbb{C}$ the following identity holds.

$$|z_1 \cdot z_2| = |z_1| \cdot |z_2|$$

This means that multiplication scales the moduli of the two factors. The same identity extends to division: for any $z_1, z_2 \in \mathbb{C}$ with $z_2 \neq 0$, one has the following.

$$\left|\frac{z_1}{z_2}\right| = \frac{|z_1|}{|z_2|}$$

The geometric significance of both identities becomes fully transparent in the [trigonometric representation](../complex-numbers-trigonometric-form/), where multiplication adds the arguments and division subtracts them.

## Properties of the complex conjugate

The complex [conjugate](../complex-numbers-introduction/) satisfies several algebraic identities that follow directly from its definition. Let $z, z_1, z_2 \in \mathbb{C}$. The conjugation map is an involution, meaning that applying it twice returns the original number:

$$\overline{\overline{z}} = z$$

Conjugation is compatible with addition, subtraction, and multiplication in the following sense:

$$\overline{z_1 + z_2} = \overline{z_1} + \overline{z_2}$$

$$\overline{z_1 - z_2} = \overline{z_1} - \overline{z_2}$$

$$\overline{z_1 \cdot z_2} = \overline{z_1} \cdot \overline{z_2}$$

These identities show that conjugation is a field automorphism of $\mathbb{C}$. It preserves the algebraic structure of the field while fixing every element of $\mathbb{R}$. Finally, the product of a complex number with its own conjugate yields the square of the modulus, a nonnegative real number.

$$z \cdot \overline{z} = a^2 + b^2 = |z|^2$$

This last identity is the key step in the computation of both the reciprocal and the quotient of complex numbers: multiplying the denominator by its conjugate produces the real number $|z|^2$, which can then be divided out without leaving any imaginary part.

> A field automorphism is a bijective map from a field to itself that preserves addition and multiplication. Conjugation satisfies this condition, and since it fixes every real number, it is an automorphism of $\mathbb{C}$ over $\mathbb{R}$.

## Division of complex numbers

To divide two complex numbers, we multiply both the numerator and the denominator by the complex conjugate of the denominator. This eliminates the imaginary part from the denominator and reduces the quotient to standard form. Given $z_1 = a + bi$ and $z_2 = c + di$ with $z_2 \neq 0$, the conjugate of the denominator is $\overline{z_2} = c - di$, and the procedure begins as follows.

$$\frac{a + bi}{c + di} = \frac{(a + bi)(c - di)}{(c + di)(c - di)}$$

Since $(c + di)(c - di) = c^2 + d^2$, which is a strictly positive real number whenever $z_2 \neq 0$, the quotient reduces to the following explicit form.

$$\frac{a + bi}{c + di} = \frac{ac + bd}{c^2 + d^2} + \frac{bc - ad}{c^2 + d^2}i$$

As with multiplication, this closed form need not be memorized: it is more instructive to multiply by the conjugate directly in each case.

Let $z_1 = 5 + 3i$ and $z_2 = 2 - i$. To compute the quotient $z_1 / z_2$, we multiply both numerator and denominator by the conjugate of the denominator, which is $\overline{z_2} = 2 + i$. Since we are multiplying by $\overline{z_2} / \overline{z_2} = 1$, the value of the expression is unchanged, while the denominator becomes a positive real number.

$$
\begin{align}
\frac{5 + 3i}{2 - i} &= \frac{(5 + 3i)(2 + i)}{(2 - i)(2 + i)} \\[6pt]
                    &= \frac{10 + 5i + 6i + 3i^2}{4 + 1} \\[6pt]
                    &= \frac{10 + 11i + 3(-1)}{5} \\[6pt]
                    &= \frac{7 + 11i}{5} \\[6pt]
                    &= \frac{7}{5} + \frac{11}{5}i
\end{align}
$$

## Reciprocal of a complex number

The reciprocal of a nonzero complex number $z = a + bi$ is the multiplicative inverse $z^{-1}$, defined by the condition $z \cdot z^{-1} = 1$. It is a special case of division with numerator equal to $1$, and is computed by the same technique: multiplying numerator and denominator by the conjugate $\overline{z} = a - bi$. The general formula is the following.

$$z^{-1} = \frac{1}{a + bi} = \frac{a - bi}{a^2 + b^2} = \frac{a}{a^2 + b^2} - \frac{b}{a^2 + b^2}i$$

Let $z = 3 - 2i$. To compute $z^{-1}$, we multiply numerator and denominator by the conjugate $\overline{z} = 3 + 2i$. The denominator becomes $|z|^2 = 3^2 + 2^2 = 13$, a positive real number, so the expression reduces to a standard complex number.

$$
\begin{align}
\frac{1}{3 - 2i} &= \frac{3 + 2i}{(3 - 2i)(3 + 2i)} \\[6pt]
                 &= \frac{3 + 2i}{9 + 4} \\[6pt]
                 &= \frac{3 + 2i}{13} \\[6pt]
                 &= \frac{3}{13} + \frac{2}{13}i
\end{align}
$$

## Multiplication and division in trigonometric form

The operations of multiplication and division acquire a particularly transparent geometric interpretation when complex numbers are expressed in trigonometric or exponential form. Consider the following complex numbers:

$$z_1 = r_1(\cos\theta_1 + i\sin\theta_1)$$

$$z_2 = r_2(\cos\theta_2 + i\sin\theta_2)$$

Their product and quotient take the following form:

$$z_1 \cdot z_2 = r_1 r_2 \bigl(\cos(\theta_1 + \theta_2) + i\sin(\theta_1 + \theta_2)\bigr)$$

$$\frac{z_1}{z_2} = \frac{r_1}{r_2} \bigl(\cos(\theta_1 - \theta_2) + i\sin(\theta_1 - \theta_2)\bigr)$$

Multiplication therefore scales the moduli and adds the arguments, while division divides the moduli and subtracts the arguments. This geometric structure is entirely hidden in the algebraic form $a + bi$, and becomes visible only in the [trigonometric](../complex-numbers-trigonometric-form/) and [exponential](../complex-numbers-exponential-form/) representations of complex numbers.
