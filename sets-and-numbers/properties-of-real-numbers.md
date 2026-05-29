---
title: Properties of Real Numbers
source: https://algebrica.org/properties-of-real-numbers/
license: CC BY-NC 4.0
tags:
  - additive-identity
  - additive-inverse
  - associativity
  - closure
  - commutativity
  - completeness
  - density
  - distributivity
  - multiplicative-identity
  - multiplicative-inverse
  - pemdas
  - real-numbers
---

## Order of operations

Before discussing the algebraic properties of [real numbers](../real-numbers/), it is necessary to clarify how operations are performed in an expression. The fundamental properties of real numbers allow us to manipulate expressions, but the order of operations ensures that every expression has a well-defined and unambiguous value. When an expression involves several operations at once, we follow a precise and universally accepted sequence. A commonly used mnemonic is PEMDAS:

+ P, Parentheses
+ E, Exponents
+ M, Multiplication
+ D, Division
+ A, Addition
+ S, Subtraction

Expressions inside parentheses are evaluated first. Exponents are computed next. Multiplication and division are performed from left to right. Addition and subtraction are then carried out from left to right.

> Multiplication and division have equal precedence, as do addition and subtraction. When two operations have the same priority, they are evaluated from left to right.

- - -

A few examples illustrate the rule:

+ Consider $3 + 4 \cdot 2$. By precedence, multiplication comes before addition: $4 \cdot 2 = 8$, so $3 + 8 = 11$.
+ Consider now $(3 + 4) \cdot 2$. Parentheses alter the natural priority: $3 + 4 = 7$, then $7 \cdot 2 = 14$.
+ Consider the expression $5 + 2^3 \cdot 4$. First, compute the exponent, $2^3 = 8$. Then multiply, $8 \cdot 4 = 32$. Finally add, $5 + 32 = 37$.

## Density and completeness in $\mathbb{R}$

The real numbers are dense: between any two distinct real numbers there always exists another. For every $a, b \in \mathbb{R}$ with $a < b$, there exists $c \in \mathbb{R}$ such that $a < c < b$. One natural choice is the arithmetic mean $c = (a+b)/2$, but infinitely many such values exist.

The property sets $\mathbb{R}$ apart from the [integers](../integers/), where gaps are plainly visible: there is no integer between $2$ and $3$. The [rational numbers](../rational-numbers/) $\mathbb{Q}$ are also dense, yet incomplete: they contain gaps at points such as $\sqrt{2}$ and $\pi$, which are real but [irrational](../irrational-numbers/).

> The real numbers are distinguished by being both dense and complete: every gap is filled, and the number line has no missing points. Completeness is a deeper structural property: every non-empty subset of $\mathbb{R}$ bounded above has a least upper bound, or [supremum](../supremum-and-infimum/), in $\mathbb{R}$, and every [Cauchy sequence](../cauchy-sequence/) of real numbers converges to a real limit. In contrast, $\mathbb{Q}$ is dense but not complete: there exist Cauchy sequences of rationals that converge to an irrational limit.

## Closure property

Closure is the most fundamental property of the real numbers, since it guarantees that the [set](../sets/) $\mathbb{R}$ is self-contained with respect to its basic operations. For all $a, b \in \mathbb{R}$:

$$
a + b \in \mathbb{R}
$$

$$
a \cdot b \in \mathbb{R}
$$

When we add or multiply two real numbers, we always obtain a real number. The result never escapes the set. Closure is far from automatic when working with other collections of numbers. The integers, for instance, are closed under addition and multiplication, but division lets you out: $1 \div 2$ is not an integer. Going one step further and subtracting within the [natural numbers](../natural-numbers/), $3 - 5$ has no answer there. Closure is therefore not a birthright of every number set, but a property that has to be earned, checked operation by operation, set by set.

> In the axiomatic treatment of the real numbers, closure is typically listed as the first field axiom. Without it, writing $a + b$ would be meaningless, there would be no guarantee that the sum of two real numbers is itself a real number, and the entire arithmetic of $\mathbb{R}$ would rest on uncertain ground.

## Commutative property

The commutative property expresses a structural symmetry of the real number system. The result of an operation does not depend on the order of the operands. Within the real numbers, the property holds for both addition and multiplication. For all real numbers $a, b \in \mathbb{R}$:

$$
a + b = b + a
$$

$$
a \cdot b = b \cdot a
$$

The property is an intrinsic feature of the algebraic structure of $\mathbb{R}$. The real numbers form a commutative [field](../fields/), in which both addition and multiplication are commutative binary operations. Commutativity does not apply to every algebraic operation. Subtraction and division, for instance, are not commutative in general:

$$
a - b \neq b - a \quad \text{and} \quad \frac{a}{b} \neq \frac{b}{a}
$$

Commutativity characterizes specific operations and plays a fundamental role in simplifying expressions and rearranging terms. Let $a = 3$ and $b = 7$. Then $3 + 7 = 10$ and $7 + 3 = 10$. Similarly, $3 \cdot 7 = 21$ and $7 \cdot 3 = 21$. The equality of the results illustrates that the order of the operands does not affect the outcome.

> In algebraic manipulation, commutativity allows us to reorder terms within sums or products. For example $2x + 5 = 5 + 2x$, which may be useful when grouping like terms or arranging expressions into a standard form.

## Associative property

The associative property concerns the way operands are grouped when more than two numbers are combined under the same operation. While the commutative property allows us to change the order of terms, the associative property allows us to change their grouping without affecting the result. For the real numbers, associativity holds for both addition and multiplication. For all $a, b, c \in \mathbb{R}$:

$$
a + (b + c) = (a + b) + c
$$

$$
a \cdot (b \cdot c) = (a \cdot b) \cdot c
$$

When adding or multiplying three real numbers, the placement of parentheses does not change the final value. The operation may therefore be performed in successive steps without ambiguity. As in the commutative case, associativity does not hold for all operations. Subtraction and division are not associative in general:

$$
a - (b - c) \neq (a - b) - c
$$

$$
a \div (b \div c) \neq (a \div b) \div c
$$

Associativity is a specific structural property of addition and multiplication in the real numbers.


Let $a = 2$, $b = 3$, and $c = 4$. For addition:

$$
2 + (3 + 4) = 2 + 7 = 9
$$

$$
(2 + 3) + 4 = 5 + 4 = 9
$$

For multiplication:

$$
2 \cdot (3 \cdot 4) = 2 \cdot 12 = 24
$$

$$
(2 \cdot 3) \cdot 4 = 6 \cdot 4 = 24
$$

In both cases, the value is unchanged by regrouping. Associativity ensures that expressions involving repeated addition or multiplication can be written without parentheses. For example $a + b + c$ is unambiguous because any grouping yields the same result. The property is fundamental in algebra, as it allows long sums and products to be manipulated, simplified, and reorganized without altering their meaning.

## Distributive property

The distributive property describes the interaction between multiplication and addition. While commutativity and associativity concern a single operation, the distributive property connects two distinct operations and explains how one distributes over the other. In the real numbers, multiplication distributes over addition. For all $a, b, c \in \mathbb{R}$:

$$
a \cdot (b + c) = a \cdot b + a \cdot c
$$

$$
(b + c) \cdot a = b \cdot a + c \cdot a
$$

Multiplying a sum by a real number is equivalent to multiplying each term of the sum individually and then adding the results. The distributive law also extends naturally to subtraction, since subtraction can be interpreted as the addition of an additive inverse:

$$
a \cdot (b - c) = a \cdot b - a \cdot c
$$

- - -

Let $a = 3$, $b = 4$, and $c = 5$. The left-hand side gives:

$$
3 \cdot (4 + 5) = 3 \cdot 9 = 27
$$

The right-hand side gives:

$$
3 \cdot 4 + 3 \cdot 5 = 12 + 15 = 27
$$

Both expressions yield the same result, confirming the distributive property. The distributive law allows us to expand expressions such as $a(x + y)$ into $ax + ay$, and conversely to factor expressions like $ax + ay$ into $a(x + y)$. It provides the structural bridge between addition and multiplication in the real number system, and is essential for simplifying expressions, solving [equations](../equations/), and developing [polynomial](../polynomials/) algebra.

> Within the framework of real numbers, the distributive property is one of the defining axioms of a field, ensuring coherence between the additive and multiplicative structures.

## Identity properties

The identity properties describe the existence of special elements in the real numbers that leave other elements unchanged under a given operation. These elements are called identity elements because they preserve the value of a number when combined with it. In the real number system, there are two identity elements, one for addition and one for multiplication.

There exists a unique real number, denoted $0$, such that for every $a \in \mathbb{R}$:

$$
a + 0 = a \quad \text{and} \quad 0 + a = a
$$

The number $0$ is called the additive identity, because adding zero does not alter the value of a real number. The uniqueness of this element is significant. If a number $n$ satisfies $a + n = a$ for all $a \in \mathbb{R}$, then necessarily $n = 0$.

There also exists a unique real number, denoted $1$, such that for every $a \in \mathbb{R}$:

$$
a \cdot 1 = a \quad \text{and} \quad 1 \cdot a = a
$$

The number $1$ is called the multiplicative identity, because multiplying by one leaves every real number unchanged. As in the additive case, the identity element is unique. If a number $n$ satisfies $a \cdot n = a$ for all $a \in \mathbb{R}$, then necessarily $n = 1$.

> The existence of identity elements is one of the defining features of the real numbers as a field. The additive identity $0$ anchors the additive structure, while the multiplicative identity $1$ anchors the multiplicative structure.

## Inverse property

The inverse property complements the identity property. While identity elements leave numbers unchanged, inverse elements undo an operation and return the identity element. In the real number system, every element has an additive inverse, and every nonzero element has a multiplicative inverse.

For every $a \in \mathbb{R}$, there exists a real number, denoted $-a$, such that:

$$
a + (-a) = 0
$$

The number $-a$ is called the additive inverse, or opposite, of $a$. Its defining property is that when added to $a$, the result is the additive identity $0$. The additive inverse is unique. If a number $b$ satisfies $a + b = 0$, then necessarily $b = -a$.

- - -

For every nonzero real number $a \in \mathbb{R}$, there exists a unique real number $\dfrac{1}{a}$ such that:

$$
a \cdot \frac{1}{a} = 1
$$

The number $\dfrac{1}{a}$ is called the multiplicative inverse, or reciprocal, of $a$. It is defined only for $a \neq 0$, since no real number multiplied by $0$ can produce the multiplicative identity $1$. As in the additive case, the multiplicative inverse is unique. If a number $b$ satisfies $a \cdot b = 1$, then necessarily $b = \dfrac{1}{a}$.

> The closure, associativity, additive identity, and additive inverse axioms together state that $(\mathbb{R}, +)$ is an abelian [group](../groups/). Adjoining the corresponding multiplicative axioms for the nonzero elements, together with the distributive law, promotes the structure to a [field](../fields/), the abstract setting that captures the algebraic behaviour of $\mathbb{R}$, $\mathbb{Q}$, and $\mathbb{C}$ at once.
