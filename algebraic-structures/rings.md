---
title: Rings
source: https://algebrica.org/rings/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - commutative-ring
  - distributivity
  - homomorphism
  - ideal
  - integral-domain
  - polynomial-ring
  - ring-theory
  - subring
  - zero-divisor
---
## Definition

A ring is an algebraic structure that extends the notion of a [group](../groups/) by introducing a second binary operation. The concept arises from the observation that several fundamental objects, such as the [integers](../integers/), the [polynomials](../polynomials/) with real coefficients, and the [square matrices](../matrices/) of a given size, share a common pattern. They admit both an addition and a multiplication, the two operations interact in a predictable way, and yet multiplication need not be commutative and need not admit inverses. A ring is a set $R$ together with two binary operations $+$ and $\cdot$ (addition and multiplication), satisfying the following axioms:

+ $(R, +)$ is an abelian group. There exists an element $0 \in R$ such that $a + 0 = a$ for all $a \in R$, and for every $a \in R$ there exists $-a \in R$ with $a + (-a) = 0$.
+ Associativity of multiplication: for all $a, b, c \in R$, the identity $(a \cdot b) \cdot c = a \cdot (b \cdot c)$ holds.
+ Distributivity: for all $a, b, c \in R$, the identities $a \cdot (b + c) = a \cdot b + a \cdot c$ and $(a + b) \cdot c = a \cdot c + b \cdot c$ hold.

A ring $(R, +, \cdot)$ is called commutative when $a \cdot b = b \cdot a$ for all $a, b \in R$. It is called a ring with unity, or unital ring, when there exists a multiplicative identity element $1 \in R$ such that $1 \cdot a = a \cdot 1 = a$ for all $a \in R$.

## Properties

Several consequences follow directly from the axioms. For any $a \in R$, multiplication by the additive identity satisfies $a \cdot 0 = 0 \cdot a = 0$. This is a consequence of distributivity:

$$a \cdot 0 = a \cdot (0 + 0) = a \cdot 0 + a \cdot 0$$

and the cancellation of $a \cdot 0$ from both sides through the group structure of $(R, +)$. Similarly, for all $a, b \in R$ the following identity holds:

$$(-a) \cdot b = a \cdot (-b) = -(a \cdot b)$$

In particular, $(-1) \cdot a = -a$ whenever $R$ has a unity. These sign rules hold in any ring.

A nonzero element $a \in R$ is called a zero divisor when there exists a nonzero element $b \in R$ such that $a \cdot b = 0$ or $b \cdot a = 0$. Zero divisors are a feature that distinguishes rings from fields: in a [field](../fields/), no nonzero element can be a zero divisor. A commutative ring with unity that contains no zero divisors is called an integral domain.

## Algebraic hierarchy

A group is the most elementary of these structures. It consists of a set equipped with a single binary operation satisfying closure, associativity, the existence of an identity element, and the existence of inverses.

A ring extends this framework by introducing a second operation, multiplication, required to be associative and to distribute over addition, but not necessarily commutative and not required to admit inverses.

When the additional requirement that every nonzero element possess a multiplicative inverse is imposed on a commutative ring with unity, the structure becomes a [field](../fields/). The three structures form a chain of increasing rigidity:

+ A group carries one operation with inverses.
+ A ring carries two operations, with inverses guaranteed only for addition.
+ A field carries two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication.

> The integers $\mathbb{Z}$ are the most natural example of a ring that is not a field: every integer has an additive inverse, yet $2^{-1}$ does not belong to $\mathbb{Z}$. The rational numbers $\mathbb{Q}$, by contrast, form a field. The same hierarchy reappears in linear algebra: scalars drawn from a ring give rise to a [module](../modules/), and scalars drawn from a field give rise to a [vector space](../vector-spaces/).

## Examples

The set $\mathbb{Z}$ of integers, equipped with ordinary addition and multiplication, is the simplest example of a commutative ring with unity. The additive identity is $0$, the multiplicative identity is $1$, and every integer has an additive inverse. The integers form an integral domain, since the product of two nonzero integers is always nonzero.

The set of polynomials with real coefficients, denoted $\mathbb{R}[x]$, forms a commutative ring with unity under the usual addition and multiplication of polynomials. The additive identity is the zero polynomial, and the multiplicative identity is the constant polynomial $1$. This ring is also an integral domain.

- - -

Let $n$ be a positive integer. The set $\mathbb{Z}/n\mathbb{Z} = \\{\ 0, 1, \ldots, n - 1 \ \\}$, equipped with addition and multiplication [modulo](../modulo-operator/) $n$, forms a commutative ring with unity. For example, in $\mathbb{Z}/6\mathbb{Z}$ one has $2 \cdot 3 = 0$, so $2$ and $3$ are zero divisors and $\mathbb{Z}/6\mathbb{Z}$ is not an integral domain. When $n$ is prime, however, $\mathbb{Z}/n\mathbb{Z}$ contains no zero divisors and is in fact a field.

Let $F$ be a field and let $n$ be a positive integer. The set $\operatorname{M}_n(F)$ of all $n \times n$ [matrices](../matrices/) with entries in $F$ forms a ring under matrix addition and multiplication. The additive identity is the zero matrix, and the multiplicative identity is the identity matrix $I_n$. For $n \geq 2$, this ring is not commutative, since matrix multiplication does not commute in general, and it contains zero divisors.

## Subrings

A subset $S$ of a ring $R$ is called a subring when $S$ is itself a ring under the operations inherited from $R$. A nonempty subset $S \subseteq R$ is a subring of $R$ if and only if it is closed under subtraction and under multiplication, that is, for all $a, b \in S$ one has $a - b \in S$ and $a \cdot b \in S$. Closure under subtraction is equivalent to requiring that $S$ be a subgroup of $(R, +)$, and closure under multiplication then ensures that the second operation is also well-defined on $S$. Every ring $R$ contains at least two subrings:

+ the trivial subring $\\{\ 0 \ \\}$.
+ $R$ itself.

Any subring other than $R$ is called a proper subring.

As an example, the set of even integers $2\mathbb{Z} = \\{\ \ldots, -4, -2, 0, 2, 4, \ldots \ \\}$ is a subring of $(\mathbb{Z}, +, \cdot)$. For any two even integers $a = 2m$ and $b = 2k$, one has $a - b = 2(m - k) \in 2\mathbb{Z}$ and $a \cdot b = 4mk \in 2\mathbb{Z}$, so both conditions are satisfied. The set $2\mathbb{Z}$ does not contain the multiplicative identity $1$ of $\mathbb{Z}$, which illustrates that a subring of a unital ring need not itself be unital.

## Ideals

Ideals are the subsets that allow the construction of quotient rings, playing a role analogous to normal subgroups in group theory. A nonempty subset $I \subseteq R$ is called a left ideal of $R$ when it is closed under addition and under left multiplication by elements of $R$, that is, for all $a \in I$ and $r \in R$ the element $r \cdot a$ belongs to $I$. A right ideal is defined analogously with right multiplication. A subset that is simultaneously a left and a right ideal is called a two-sided ideal, or simply an ideal.

The set $n\mathbb{Z}$ of all multiples of a fixed integer $n$ is an ideal of $\mathbb{Z}$: for any $a = nk \in n\mathbb{Z}$ and any $r \in \mathbb{Z}$:

$$r \cdot a = n(rk) \in n\mathbb{Z}$$

> Ideals are precisely the kernels of ring homomorphisms, a fact that makes them the natural tool for constructing quotient rings and for studying the structure of rings through their homomorphic images.

## Ring homomorphisms and isomorphisms

A ring homomorphism is a [function](../functions/) between two rings that preserves both operations. Given two rings $(R, +, \cdot)$ and $(S, \oplus, \odot)$, a function $\varphi : R \to S$ is a ring homomorphism when for all $a, b \in R$:

$$\varphi(a + b) = \varphi(a) \oplus \varphi(b)$$

$$\varphi(a \cdot b) = \varphi(a) \odot \varphi(b)$$

The first condition requires that $\varphi$ be a [group homomorphism](../groups/) between the additive groups, and the second that it preserve multiplication. As a consequence, $\varphi$ maps the additive identity of $R$ to the additive identity of $S$. When both rings are unital, one often additionally requires that $\varphi(1_R) = 1_S$. The [kernel](../homomorphisms-and-isomorphisms/) and image of a ring homomorphism $\varphi : R \to S$ are defined as in the case of groups:

$$\ker(\varphi) = \\{\ a \in R : \varphi(a) = 0_S \ \\}$$

$$\operatorname{im}(\varphi) = \\{\ \varphi(a) : a \in R \ \\}$$

The kernel is always an ideal of $R$, and the image is always a subring of $S$. A homomorphism is injective if and only if its kernel contains only the additive identity of $R$.

- - -

A ring homomorphism that is both injective and surjective is called a ring isomorphism. Two rings are isomorphic, written $R \cong S$, when an isomorphism between them exists. Isomorphic rings are structurally identical and share all properties that are intrinsic to their ring structure.

As an example, consider the map $\varphi : \mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$ defined by $\varphi(a) = a \bmod n$. This map preserves both operations, since the residue class of a sum coincides with the sum of the residue classes in $\mathbb{Z}/n\mathbb{Z}$, and analogously for the product. It is therefore a ring homomorphism, and its kernel is precisely $n\mathbb{Z}$, the ideal of multiples of $n$.

> Adding the requirement that every nonzero element be invertible promotes a commutative ring with unity to a [field](../fields/), the structure in which linear algebra is developed and on which the theory of [vector spaces](../vector-spaces/) is built. The general framework of structure-preserving maps across the standard algebraic structures is treated on the page about [homomorphisms and isomorphisms](../homomorphisms-and-isomorphisms/).
