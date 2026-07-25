---
title: Fields
source: https://algebrica.org/fields/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - characteristic
  - complex-numbers
  - distributivity
  - field-extension
  - field-theory
  - finite-field
  - homomorphism
  - rational-numbers
  - real-numbers
  - subfield
---
## Definition

A field is a set equipped with addition and multiplication in which every element has an additive inverse and every nonzero element has a multiplicative inverse. The [rational numbers](../rational-numbers/), the [real numbers](../real-numbers/), and the [complex numbers](../complex-numbers/) are fields. In each case, addition and multiplication satisfy the field axioms, while subtraction and division by a nonzero element remain in the same set.

Formally, a field is a set $F$ together with two binary operations $+$ and $\cdot$ satisfying the following axioms:

+ $(F, +)$ is an abelian group. The additive identity is denoted $0,$ and the additive inverse of an element $a \in F$ is denoted $-a.$
+ $(F \setminus \{\ 0 \ \}, \cdot)$ is an abelian group. The multiplicative identity is denoted $1,$ and the multiplicative inverse of a nonzero element $a$ is denoted $a^{-1}.$
+ Multiplication distributes over addition: for all $a, b, c \in F,$ the identities $a \cdot (b + c) = a \cdot b + a \cdot c$ and $(a + b) \cdot c = a \cdot c + b \cdot c$ hold.

In a ring $R$ with a multiplicative identity, a unit, or invertible element, is an element $u \in R$ for which some $v \in R$ satisfies $u \cdot v = v \cdot u = 1.$ This inverse is unique by associativity and is denoted by $u^{-1}.$ The units of a field $F$ are its nonzero elements. The additive identity cannot be a unit when $0 \neq 1,$ since $0 \cdot a = 0$ for every $a \in F.$

> The multiplicative group $F \setminus \{\ 0 \ \}$ has identity $1,$ so the axioms require $0 \neq 1.$ Thus the zero ring is not a field. Equivalently, a field is a commutative [ring](../rings/) with unity in which every nonzero element is invertible. Every field is a ring, but not every ring is a field.

## Properties

For any $a \in F,$ multiplication by zero satisfies $a \cdot 0 = 0.$ Distributivity gives:

$$a \cdot 0 = a \cdot (0 + 0) = a \cdot 0 + a \cdot 0$$

The cancellation law in the additive group then gives $a \cdot 0 = 0.$

A field contains no zero divisors. If $a \cdot b = 0$ and $a \neq 0,$ then $a$ is invertible and:

$$b = a^{-1} \cdot (a \cdot b) = a^{-1} \cdot 0 = 0$$

In a field the product of two nonzero elements is nonzero, so nonzero factors may be cancelled. The additive and multiplicative structures satisfy:

$$(-a) \cdot b = a \cdot (-b) = -(a \cdot b)$$

The expression holds for all $a, b \in F.$ Multiplying two additive inverses gives:

$$(-a) \cdot (-b) = a \cdot b$$

This follows from the previous identity after replacing $b$ by $-b.$

## Algebraic hierarchy

A [group](../groups/) is a set equipped with a single binary operation satisfying closure, associativity, the existence of an identity element, and the existence of inverses.

A [ring](../rings/) has addition and multiplication. Addition makes the set an abelian group, while multiplication is associative and distributes over addition on both sides. Multiplication need not be commutative, as the multiplication of [matrices](../matrices/) in $\mathrm{M}_n(\mathbb{R})$ shows when $n \geq 2,$ and a ring need not have a multiplicative identity under the convention used here. The integers $\mathbb{Z}$ are a commutative ring with identity. Every [integer](../integers/) has an additive inverse, yet most integers lack a multiplicative inverse in $\mathbb{Z},$ since $2^{-1}$ does not belong to $\mathbb{Z}.$

A field is a commutative ring with unity in which every nonzero element has a multiplicative inverse. This gives the following hierarchy:

+ A group has one operation, and every element has an inverse.
+ A ring has two operations, and every element has an additive inverse.
+ A field has two operations, and every nonzero element also has a multiplicative inverse.

> The rational numbers $\mathbb{Q},$ the real numbers $\mathbb{R},$ and the complex numbers $\mathbb{C}$ are fields. The integers $\mathbb{Z}$ are a ring but not a field, since division does not close within them. A [vector space](../vector-spaces/) has scalars in a field, whereas a [module](../modules/) has scalars in a ring.

## Examples

The set $\mathbb{Q}$ of rational numbers, equipped with ordinary addition and multiplication, is the smallest field containing the integers. Every nonzero rational number $p/q$ has a multiplicative inverse $q/p,$ and all field axioms are satisfied.

The set $\mathbb{R}$ of real numbers is a field extending $\mathbb{Q}.$ It has an order compatible with the field operations and is complete, so every nonempty subset bounded above has a [least upper bound](../supremum-and-infimum/). The page on the [properties of real numbers](../properties-of-real-numbers/) lists the field axioms for $\mathbb{R}$ and gives concrete examples.

The set $\mathbb{C}$ of complex numbers is a field extending $\mathbb{R}.$ It is algebraically closed, whereas $\mathbb{R}$ is not. The [fundamental theorem of algebra](../roots-of-a-polynomial/) states that every nonconstant polynomial with coefficients in $\mathbb{C}$ has a root in $\mathbb{C}.$

The ring $\mathbb{Z}$ has identity $1,$ but not every nonzero integer has an inverse. If integers $a$ and $b$ satisfy $ab = 1,$ then $|a||b| = 1,$ so $|a| = |b| = 1.$ Thus $1$ and $-1$ are the only units in $\mathbb{Z},$ and $\mathbb{Z}$ is not a field.

For any field $K,$ the [polynomial ring](../polynomials/) $K[x]$ is another commutative ring with identity that is not a field. Its units are exactly the nonzero constant polynomials. If nonzero polynomials $f$ and $g$ satisfied $fg = 1,$ then:

$$\deg(fg) = \deg(f) + \deg(g) = 0$$

Both degrees must be zero. A polynomial of positive degree cannot have a multiplicative inverse in $K[x].$

- - -

For any prime $p,$ the set $\mathbb{Z}/p\mathbb{Z} = \{\ [0], [1], \ldots, [p - 1] \ \}$ equipped with addition and multiplication [modulo](../modulo-operator/) $p$ is the field $\mathbb{F}_p.$ It has $p$ elements. If $[a]$ is nonzero, then $p$ does not divide $a,$ so $\gcd(a,p) = 1.$ Bezout's identity gives integers $r$ and $s$ such that $ar + ps = 1.$ Reducing this equation modulo $p$ gives $[a][r] = [1],$ so $[r]$ is the inverse of $[a].$ A composite modulus need not give a field. In $\mathbb{Z}/6\mathbb{Z},$ the elements $[2]$ and $[3]$ satisfy $[2][3] = [0],$ so neither is invertible and $\mathbb{Z}/6\mathbb{Z}$ is not a field.

> Finite fields exist only when the number of elements is a prime power $p^n,$ for some prime $p$ and positive integer $n.$ For every such prime power there exists, up to isomorphism, exactly one finite field, denoted $\mathbb{F}_{p^n}$ or $\mathrm{GF}(p^n).$

## Subfields and field extensions

A subset $K \subseteq F$ is a subfield of $F$ when $K$ is itself a field under the operations inherited from $F.$ Equivalently, $K$ is a subfield of $F$ when it contains $0$ and $1$ and is closed under addition, negation, multiplication, and taking multiplicative inverses of nonzero elements. The rational numbers $\mathbb{Q}$ form a subfield of $\mathbb{R},$ which is itself a subfield of $\mathbb{C}.$ These inclusions define a chain of fields:

$$\mathbb{Q} \subseteq \mathbb{R} \subseteq \mathbb{C}$$

When $K$ is a subfield of $F,$ the field $F$ is a field extension of $K,$ written $F/K.$ The extension $\mathbb{C}/\mathbb{R}$ is a two-dimensional [vector space](../vector-spaces/) over $\mathbb{R}$ with basis $\{\ 1, i \ \}.$ The degree $[F : K]$ of an extension is the dimension of $F$ as a vector space over $K.$ Thus $[\mathbb{C} : \mathbb{R}] = 2.$

## Characteristic of a field

Every field $F$ has a characteristic, a non-negative integer determined by repeated addition of the multiplicative identity. If a positive number of copies of $1$ sums to zero, the characteristic is the smallest such number $n$:

$$\underbrace{1 + 1 + \cdots + 1}_{n} = 0$$

When no such $n$ exists, the characteristic is defined to be $0.$ The characteristic of a field is always either zero or a prime number. If the characteristic were a composite number $n = ab$ with $1 < a, b < n,$ one could write:

$$0 = \underbrace{1 + \cdots + 1}_{n} = \left(\underbrace{1 + \cdots + 1}_{a}\right) \cdot \left(\underbrace{1 + \cdots + 1}_{b}\right)$$

Since a field has no zero divisors, one of the two factors would have to be zero, contradicting the minimality of $n.$ The fields $\mathbb{Q},$ $\mathbb{R},$ and $\mathbb{C}$ all have characteristic zero. The finite field $\mathbb{F}_p$ has characteristic $p.$

## Field homomorphisms

A field homomorphism is a [function](../functions/) $\varphi : F \to K$ between two fields that preserves both operations: for all $a, b \in F$:

$$\varphi(a + b) = \varphi(a) + \varphi(b)$$

$$\varphi(a \cdot b) = \varphi(a) \cdot \varphi(b)$$

The definition also requires $\varphi(1_F) = 1_K.$ Every field homomorphism is injective. To see this, the [kernel](../homomorphisms-and-isomorphisms/):

$$\ker(\varphi) = \{\ a \in F : \varphi(a) = 0 \ \}$$

is an [ideal](../rings/) of $F.$ Since $F$ is a field, its only ideals are $\{\ 0 \ \}$ and $F$ itself, and the condition $\varphi(1) = 1 \neq 0$ rules out the second possibility. A bijective field homomorphism is a field isomorphism. Two fields are isomorphic, written $F \cong K,$ when an isomorphism between them exists. Isomorphic fields have the same algebraic properties.

> A function is injective, or one-to-one, when $\varphi(a) = \varphi(b)$ implies $a = b.$ A function is bijective when it is injective and surjective. Thus every element of the codomain has exactly one preimage. The page on [homomorphisms and isomorphisms](../homomorphisms-and-isomorphisms/) gives the corresponding definitions for [groups](../groups/), [rings](../rings/), and [modules](../modules/).
