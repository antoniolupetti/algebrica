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
  - order-relation
  - ordered-field
  - pemdas
  - real-numbers
  - transitivity
  - trichotomy
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

Commutativity is part of the algebraic structure of $\mathbb{R}$. The real numbers form a commutative [field](../fields/), in which both addition and multiplication are commutative binary operations. Commutativity does not apply to every algebraic operation. Subtraction and division, for instance, are not commutative in general:

$$
a - b \neq b - a \quad \text{and} \quad \frac{a}{b} \neq \frac{b}{a}
$$

Commutativity holds for specific operations and is used in simplifying expressions and rearranging terms. Let $a = 3$ and $b = 7$. Then $3 + 7 = 10$ and $7 + 3 = 10$. Similarly, $3 \cdot 7 = 21$ and $7 \cdot 3 = 21$. The equality of the results illustrates that the order of the operands does not affect the outcome.

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

> The existence of identity elements is one of the defining properties of the real numbers as a field. The additive identity $0$ is neutral for addition, and the multiplicative identity $1$ is neutral for multiplication.

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

## The order relation

In addition to the field operations $+$ and $\cdot$, the real numbers carry an order relation, written $<$, which expresses the fact that one number is smaller than another. The dual symbols are defined in terms of $<$ as follows: $a > b$ means $b < a$, $a \leq b$ means $a < b$ or $a = b$, and $a \geq b$ means $a > b$ or $a = b$. A real number $a$ is called positive when $a > 0$ and negative when $a < 0$.

The order relation is not an additional operation but a binary relation, and its interaction with the field operations is governed by a small number of properties that complement the field axioms listed above. Together, the field properties and the order properties characterise $\mathbb{R}$ as a totally ordered field.

## Trichotomy and transitivity

The first foundational property of the order relation is the trichotomy law. For any real numbers $a$ and $b$, exactly one of the following three conditions holds:

$$a < b \qquad a = b \qquad a > b$$

The trichotomy law guarantees that no real number can satisfy two of these conditions simultaneously, and that no pair of real numbers fails to satisfy at least one of them. The order relation is therefore total, that is, every pair of real numbers is comparable through the relation $<$.

The second foundational property is transitivity. For any real numbers $a$, $b$, and $c$:

$$a < b \text{ and } b < c \quad \Longrightarrow \quad a < c$$

Transitivity is the algebraic counterpart of the geometric intuition that on the real line, if $a$ precedes $b$ and $b$ precedes $c$, then $a$ precedes $c$. It is the property that justifies the chained notation $a < b < c$, in which the third inequality $a < c$ is implicit and need not be stated separately.

> Trichotomy and transitivity together make $\mathbb{R}$ a totally ordered set. They are independent of the field operations and concern only the comparability of pairs of real numbers.

## Compatibility with addition

The order relation interacts with addition in a way that preserves the direction of the relation. For any real numbers $a$, $b$, and $c$:

$$a < b \quad \Longrightarrow \quad a + c < b + c$$

The same statement applies to the symbols $\leq$, $>$, and $\geq$, with the direction of the order relation preserved in every case. Subtracting the same quantity from both sides is a particular case, obtained by adding the opposite $-c$, and the conclusion is again that the direction of the relation is preserved.

A useful corollary is the ability to combine two relations pointing in the same direction. For any real numbers $a$, $b$, $c$, and $d$:

$$a < b \text{ and } c < d \quad \Longrightarrow \quad a + c < b + d$$

The rule is obtained by adding $c$ to both sides of the first relation and adding $b$ to both sides of the second, then combining the two resulting relations through transitivity. The analogous statement for subtraction member by member is not admissible: from $a < b$ and $c < d$ one cannot in general conclude $a - c < b - d$, since the order of the resulting expression depends on the relative magnitudes of the four quantities.

## Compatibility with multiplication

The interaction of the order relation with multiplication is more subtle than the interaction with addition, since the direction of the relation depends on the sign of the multiplier. For any real numbers $a$, $b$, and $c$, two distinct cases arise.

$$a < b \text{ and } c > 0 \quad \Longrightarrow \quad ac < bc$$

$$a < b \text{ and } c < 0 \quad \Longrightarrow \quad ac > bc$$

The first rule states that multiplication by a positive number preserves the direction of the order relation. The second rule states that multiplication by a negative number reverses the direction of the order relation. The two rules together cover the case of any nonzero multiplier and have no analogue in the theory of equalities, where multiplication by any nonzero constant always preserves the equality.

The same statements hold for the symbols $\leq$, $>$, and $\geq$, with the same dependence of the direction on the sign of the multiplier. Division by a positive or negative quantity is treated as multiplication by its reciprocal, and the same rules apply.

A related rule concerns the reciprocals of positive numbers. If $0 < a < b,$ then the reciprocals satisfy $0 < 1/b < 1/a,$ so inverting two positive numbers reverses their order. The reciprocal of a positive number is itself positive, because a positive number multiplied by a negative one would give a negative product, contradicting $a(1/a) = 1 > 0.$ Multiplying the inequality $a < b$ by the positive quantity $1/(ab)$ then yields $1/b < 1/a.$

> The reversal of the direction upon multiplication by a negative number is the algebraic property of the order relation that has no counterpart in the equality relation. The operational consequences of this rule and its role in solving [inequalities](../inequalities/) are treated in the corresponding chapter.

## The sign of a product

The combination of the multiplication rules produces a useful classification of the sign of a product of two real numbers. For any real numbers $a$ and $b$:

+ If $a$ and $b$ have the same sign (both positive or both negative), their product $ab$ is positive.
+ If $a$ and $b$ have opposite signs, their product $ab$ is negative.
+ If at least one of $a$ and $b$ is zero, their product $ab$ is zero.

The rule extends to a product of any finite number of nonzero real factors by induction. A product is positive when the number of negative factors is even, and negative when the number of negative factors is odd.

## The square rule

A fundamental consequence of the sign rule for a product is the fact that the square of every real number is non-negative. For any real number $a$:

$$a^2 \geq 0$$

The equality $a^2 = 0$ holds if and only if $a = 0$, so the square of a nonzero real number is strictly positive. The proof of this fact is a direct application of the sign rule. When $a > 0$, both factors of $a^2 = a \cdot a$ are positive and the product is positive. When $a < 0$, both factors are negative and the product is positive. When $a = 0$, the product is zero.

The square rule is the algebraic foundation of many order relations involving polynomial expressions. As an illustration, the expression $a^2 + b^2$ is non-negative for every pair of real numbers $a$ and $b$, and it vanishes if and only if both $a$ and $b$ are zero.

Squaring is also monotone on the non-negative numbers. If $0 \leq a < b,$ then $a^2 < b^2,$ which follows from the factorisation $b^2 - a^2 = (b - a)(b + a)$ once one observes that both factors are positive. For non-negative numbers the converse holds as well, so $a^2 < b^2$ forces $a < b.$ Because of this monotonicity, the square root inverts squaring on $[0, +\infty),$ and two non-negative numbers can be compared through their squares.

The same reasoning applies to even powers $a^{2k}$ for any positive integer $k$, since $a^{2k} = (a^k)^2$ is the square of a real number. The corresponding statement for odd powers does not hold: an odd power preserves the sign of its base, so $a^{2k+1}$ is positive when $a > 0$ and negative when $a < 0$.

## The ordered field structure

The properties presented in the previous sections combine with the field properties to make $\mathbb{R}$ an ordered field, that is, a field in which the order relation is compatible with the field operations. The complete characterisation requires a small number of foundational axioms: the field axioms (closure, associativity, commutativity, distributivity, identity elements, inverse elements) and the order axioms (trichotomy, transitivity, compatibility of $<$ with $+$ and with multiplication by positive numbers). From these axioms, every operational rule for the manipulation of expressions involving the relations $<$, $\leq$, $>$, and $\geq$ can be obtained by a sequence of elementary deductions.

The ordered field structure alone does not single out $\mathbb{R}$ among other number systems. The [rational numbers](../rational-numbers/) $\mathbb{Q}$ also form an ordered field with the same axioms, yet they fail to capture the full structure of the real line because of the presence of gaps. The property that distinguishes $\mathbb{R}$ from $\mathbb{Q}$ is the completeness of the order relation, discussed at the beginning of this entry: every non-empty subset of $\mathbb{R}$ bounded above has a least upper bound in $\mathbb{R}$, while the analogous statement fails in $\mathbb{Q}$. The combination of the ordered field axioms with the completeness axiom characterises $\mathbb{R}$ uniquely.

Being a field and being an ordered field are separate conditions, and not every field meets the second. The [complex numbers](../complex-numbers/) $\mathbb{C}$ form a field, yet no order relation on $\mathbb{C}$ is compatible with its operations. In any ordered field the square of a nonzero element is positive, while in $\mathbb{C}$ one has $i^2 = -1.$ An order compatible with the operations would force $i^2 > 0,$ that is $-1 > 0,$ in conflict with $1 > 0.$ The order is extra structure that $\mathbb{R}$ admits and $\mathbb{C}$ does not.
