---
title: Integers
source: https://algebrica.org/integers/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - binary-system
  - commutative-ring
  - decimal-system
  - divisibility
  - equivalence-class
  - euclidean-division
  - induction
  - integers
  - integral-domain
  - modular-arithmetic
  - number-line
  - ordered-pair
  - total-order
---

## Definition

Among the different [types of numbers](../types-of-numbers/), the integers are the extension of the [natural numbers](../natural-numbers/) obtained by adjoining the additive opposite of every positive quantity. The enlarged system contains all whole quantities, positive and negative, together with zero. The set is denoted by $\mathbb{Z}.$ Symbolically we write:

$$
\mathbb{Z} = \{\ldots,-3,-2,-1,0,1,2,3,\ldots\}
$$

The integers are an infinite collection of evenly spaced points along the number line and embed into the [rational numbers](../rational-numbers/) through the identification $n \mapsto n/1;$ the rationals in turn are contained in the [real numbers](../real-numbers/) and the [complex numbers](../complex-numbers/).

![IMG. 1](svg/integers-1.svg)

The inclusions $\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$ record successive extensions, each of which permits an operation or equation unavailable in the preceding system.

A rigorous construction models each integer as a class of [ordered pairs](../sets/) $(a,b)$ of natural numbers. Two pairs belong to the same class whenever:

$$
(a,b) \sim (c,d) \quad \longleftrightarrow \quad a + d = b + c
$$

The pair $(a,b)$ is intended to represent the formal difference $a-b.$ This interpretation motivates the construction but does not define it, since the equivalence relation itself uses only addition on $\mathbb{N}:$

+ Pairs with equal components form the class corresponding to $0.$
+ Pairs where the first component is larger form the positive integers.
+ Pairs where the second component is larger form the negative ones.

For example, consider the pair of natural numbers $(2,5).$ Since the second component is larger than the first, the pair corresponds to a negative integer:

$$
2 - 5 = -3
$$

Two pairs represent the same integer exactly when they belong to the same equivalence class. For instance, the pair $(4,7)$ lies in the same class as $(2,5),$ because:

$$
4 + 5 = 9 \qquad \text{and} \qquad 7 + 2 = 9
$$

Although the components differ, both pairs represent the same difference, the integer $-3.$

Write $[(a,b)]$ for the equivalence class of $(a,b).$ The relation above is reflexive and symmetric. It is also transitive. If $(a,b) \sim (c,d)$ and $(c,d) \sim (e,f),$ then $a+d=b+c$ and $c+f=d+e.$ Adding these equalities and cancelling $c+d$ gives $a+f=b+e,$ so $(a,b) \sim (e,f).$

Addition and multiplication are defined directly on the classes by:

$$
[(a,b)]+[(c,d)] := [(a+c,b+d)]
$$

$$
[(a,b)][(c,d)] := [(ac+bd,ad+bc)]
$$

These definitions must be independent of the chosen representatives. Suppose $(a,b) \sim (a',b'),$ so $a+b'=b+a'.$ For addition, adding $c+d$ to this equality shows that $(a+c,b+d) \sim (a'+c,b'+d).$ For multiplication, the two equalities

$$
ac+b'c=bc+a'c
$$

$$
ad+b'd=bd+a'd
$$

follow by multiplying $a+b'=b+a'$ by $c$ and $d,$ respectively. Adding the first equality to the reverse of the second gives the equality required for $(ac+bd,ad+bc) \sim (a'c+b'd,a'd+b'c).$ The same argument applies to a change of representative in the second factor. Hence both operations are well-defined.

The map $n \mapsto [(n,0)]$ embeds $\mathbb{N}$ into $\mathbb{Z}$ and preserves addition and multiplication. Under this identification, $0=[(0,0)]$ and $1=[(1,0)].$ Negation is given by $-[(a,b)]=[(b,a)],$ since:

$$
[(a,b)]+[(b,a)]=[(a+b,a+b)]=0
$$

The trichotomy law on $\mathbb{N}$ now shows that every integer has exactly one of three forms. If $a>b,$ then $[(a,b)]=[(a-b,0)]$ is positive; if $a=b,$ then $[(a,b)]=0;$ if $a<b,$ then $[(a,b)]=-[(b-a,0)]$ is negative.

## The integers as an algebraic ring

The integers form a [ring](../rings/) because addition and multiplication satisfy the following axioms.

The ring axioms for $(\mathbb{Z}, +, \cdot)$ are the following. For all $a, b, c \in \mathbb{Z}:$

+ Closure: the sum and product of any two integers are again integers, $a + b \in \mathbb{Z}$ and $ab \in \mathbb{Z}.$
+ Associativity: both operations are associative, $a + (b+c) = (a+b) + c$ and $a(bc) = (ab)c.$
+ Identity elements: both operations have a neutral element, $a + 0 = a$ and $a \cdot 1 = a.$
+ Additive inverses: every integer has an opposite, so that $(\mathbb{Z}, +)$ is an abelian [group](../groups/), with $a + (-a) = 0.$
+ Commutativity of addition: the order of summands does not affect the result, $a + b = b + a.$
+ Distributivity: multiplication distributes over addition, $a(b+c) = ab + ac.$

Multiplication in $\mathbb{Z}$ is also commutative, that is, $ab = ba$ for all $a, b \in \mathbb{Z},$ which makes $(\mathbb{Z}, +, \cdot)$ a commutative ring. Integers do not have multiplicative inverses in general. The only integers $a$ for which $a^{-1} \in \mathbb{Z}$ are $a = 1$ and $a = -1,$ which is why $\mathbb{Z}$ is a ring but not a field.

> A [field](../fields/) is a ring in which every nonzero element has a multiplicative inverse. The [rational numbers](../rational-numbers/) $\mathbb{Q}$ and the [real numbers](../real-numbers/) $\mathbb{R}$ are fields; the integers are not, since $2^{-1} \notin \mathbb{Z}.$

A further property refines the ring structure of $\mathbb{Z}.$ A product of two integers is zero only when at least one factor is zero, so $\mathbb{Z}$ has no zero divisors. A commutative ring with this property is an integral domain. Consequently, $ab=ac$ with $a\neq0$ implies $b=c.$ The same property fails in rings such as $\mathbb{Z}/n\mathbb{Z}$ when $n$ is composite, where products of nonzero classes may vanish.

## Fundamental properties of the integers

Operations preserve equality. If two integers satisfy $a=b,$ then, in particular:

$$
a + c = b + c
$$

$$
ac = bc
$$

- - -

The commutative laws state that the order of the operands does not affect the result:

$$
a + b = b + a
$$

$$
ab = ba
$$

- - -

The associative laws state that grouping the terms does not change the outcome:

$$
a + (b + c) = (a + b) + c
$$

$$
a(bc) = (ab)c
$$

- - -

The distributive law states that multiplication distributes over addition:

$$
a(b + c) = ab + ac
$$

- - -

The integers also have neutral elements for the two operations. Adding zero leaves any integer unchanged, and multiplying by one preserves its value:

$$
a + 0 = a \qquad a \cdot 1 = a
$$

## Order on the integers

The set $\mathbb{Z}$ inherits a total order from the [natural numbers](../natural-numbers/) and extends it to the negative range. Given two integers $a,b\in\mathbb{Z},$ the relation $a\leq b$ holds when the difference $b-a$ is a non-negative integer. The relation is reflexive, antisymmetric, transitive, and total. Thus, for any $a,b\in\mathbb{Z},$ exactly one of $a<b,$ $a=b,$ or $b<a$ holds.

The order is compatible with the [ring](../rings/) operations. For all $a, b, c \in \mathbb{Z}:$

+ If $a \leq b,$ then $a + c \leq b + c.$
+ If $a \leq b$ and $c \geq 0,$ then $ac \leq bc.$

The order on $\mathbb{Z}$ differs from the order on $\mathbb{N}.$ Every non-empty subset of $\mathbb{N}$ has a least element, whereas $\mathbb{Z}$ itself has none because the negative integers have no lower bound. Every non-empty subset of $\mathbb{Z}$ that is bounded below does have a least element, and elementary number theory uses this restricted form of well-ordering.

The [absolute value](../absolute-value/) measures the distance of an integer from zero. For any integer $a,$ the value $|a|$ equals $a$ when $a \geq 0$ and $-a$ otherwise. This non-negative measure allows comparisons between positive and negative integers and appears in the bound on the remainder of the Euclidean division.

## Integers in base 10

Integers are typically written using the decimal system, that is, base 10. Each digit has a positional weight given by a power of ten. The number $235,$ for example, is a sum of powers of ten:

$$
235 = 2 \times 10^{2} + 3 \times 10^{1} + 5 \times 10^{0}
$$

The decomposition shows how each digit contributes to the value. The following table summarises the number:

| Digit | Place value         | Contribution               |
|-------|---------------------|----------------------------|
| 2     | $10^{2}$ (hundreds) | $2 \times 10^{2} = 200$    |
| 3     | $10^{1}$ (tens)     | $3 \times 10^{1} = 30$     |
| 5     | $10^{0}$ (units)    | $5 \times 10^{0} = 5$      |

Adding the contributions recovers the integer:

$$
235 = 200 + 30 + 5
$$

> The same mechanism applies to any integer written in decimal notation. Each digit is a coefficient of a specific power of ten, and the integer itself is obtained by summing all the positional contributions.

## The binary system

Although integers are commonly written in base 10, other numeral systems are equally valid. The binary system uses only the digits $0$ and $1$ and is used in computer science and digital electronics, where two-state devices store and process information. In base 2, each position corresponds to a power of two rather than a power of ten. Repeated division of $53$ and each successive quotient by $2$ produces the binary digits as remainders. Reading them from bottom to top yields the binary expansion.

| Division by 2  | Quotient | Remainder |
|---------------:|:--------:|:---------:|
| $53 \div 2$    | $26$     | $1$       |
| $26 \div 2$    | $13$     | $0$       |
| $13 \div 2$    | $6$      | $1$       |
| $6 \div 2$     | $3$      | $0$       |
| $3 \div 2$     | $1$      | $1$       |
| $1 \div 2$     | $0$      | $1$       |

Reading the remainders upward gives the binary representation $53=(110101)_2.$ Expanding the binary digits in powers of two checks the conversion:

| Binary digit | Power of two | Contribution            |
|--------------|--------------|-------------------------|
| $1$          | $2^{5}$      | $1 \times 2^{5} = 32$   |
| $1$          | $2^{4}$      | $1 \times 2^{4} = 16$   |
| $0$          | $2^{3}$      | $0 \times 2^{3} = 0$    |
| $1$          | $2^{2}$      | $1 \times 2^{2} = 4$    |
| $0$          | $2^{1}$      | $0 \times 2^{1} = 0$    |
| $1$          | $2^{0}$      | $1 \times 2^{0} = 1$    |

The sum of the contributions confirms the conversion:

$$
32 + 16 + 0 + 4 + 0 + 1 = 53
$$

## Divisibility and Euclidean division

Within $\mathbb{Z}$ the operation of division is not always possible without remainder. For two integers $a$ and $b,$ with $b \neq 0,$ we say that $b$ divides $a,$ written $b \mid a,$ when there exists an integer $q$ such that:

$$
a = bq
$$

Divisibility leads to the study of factorisation, prime numbers, and greatest common divisors. The integer $q$ is the quotient of the exact division.

When $b$ does not divide $a,$ the Euclidean division theorem guarantees that the quotient and the remainder still exist in a controlled form. For every pair of integers $a$ and $b$ with $b \neq 0,$ there exist unique integers $q$ and $r$ such that:

$$
a = bq + r \qquad \text{with} \qquad 0 \leq r < |b|
$$

The integer $q$ is the quotient and $r$ the remainder of the division of $a$ by $b.$ The [absolute value](../absolute-value/) in the bound on $r$ allows the statement to cover negative divisors uniformly. The [modulo operator](../modulo-operator/) and modular arithmetic are built on the uniqueness of the pair $(q, r).$ An analogous statement holds for [polynomials](../polynomial-division/) over a field, where the absolute value of the divisor is replaced by its degree.

For example, dividing $17$ by $5$ gives $q = 3$ and $r = 2,$ since $17 = 3 \cdot 5 + 2.$ Dividing $-17$ by $5$ gives $q = -4$ and $r = 3,$ since $-17 = (-4) \cdot 5 + 3.$ The remainder is again non-negative, in agreement with the convention $0 \leq r < |b|.$

## The modulo operator

Modular arithmetic records only the remainders after division by a fixed integer $n.$ Within $\mathbb{Z},$ two integers are equivalent [modulo](../modulo-operator/) $n$ when they differ by a multiple of $n.$ In arithmetic modulo $12,$ the integers $14$ and $2$ represent the same residue class because $14-2=12.$ Addition and multiplication are carried out as usual, and the result is replaced by its remainder upon division by $n.$ For example:

$$
7 + 9 \equiv 4 \pmod{12}
$$

$$
5 \times 7 \equiv 11 \pmod{12}
$$

In the case of $5 \times 7,$ the product is $35 = 24 + 11.$ Since $24$ is a multiple of $12,$ the value of the product modulo $12$ is the remainder $11.$

> Computer science uses the modulo operator to extract remainders, generate cyclic patterns, and keep values within a bounded range. Month calculations give a familiar example. Adding $n$ months is handled modulo $12,$ since month counts restart after December.

## Integers and the role of induction

Several properties of the integers follow from the recursive structure of the natural numbers. Since $\mathbb{Z}$ is constructed from $\mathbb{N},$ many statements about integers reduce to statements proved by the [principle of mathematical induction](../principle-of-mathematical-induction/).

Consider a set $A \subseteq \mathbb{N}$ defined by a property $p(n),$ such that $A = \{n \in \mathbb{N} \mid p(n)\}.$ Suppose the following conditions hold:

+ $p(0)$ is true, that is, $0 \in A.$
+ $p(n) \rightarrow p(n+1)$ for every $n \in \mathbb{N}.$ If $n \in A,$ then $n+1 \in A.$

It follows that $p(n)$ is true for every $n \in \mathbb{N}.$ For example, consider the claim that the sum of the first $n$ positive integers equals:

$$
\frac{n(n+1)}{2}
$$

The base case $n = 1$ is immediate, since both sides equal $1.$ For the inductive step, assuming the identity holds for some $n,$ one adds $n+1$ to both sides and verifies that the result matches the formula evaluated at $n+1.$ Since the natural numbers embed into $\mathbb{Z}$ as the non-negative integers, the identity holds in $\mathbb{Z}$ as well, and the same method applies to statements about $\mathbb{Z}$ that reduce to properties of $\mathbb{N}.$

Ordinary induction from $0$ does not prove a property for every integer. Consider $p(n)$ given by $n \geq 0.$ The statement $p(0)$ is true, and $p(n)$ implies $p(n+1)$ for every $n \in \mathbb{Z}.$ Nevertheless, $p(-1)$ is false. A proof covering all of $\mathbb{Z}$ therefore needs a separate argument for negative integers, such as induction applied to $p(-n)$ for $n \in \mathbb{N}.$
