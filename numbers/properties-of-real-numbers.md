---
title: Properties of Real Numbers
source: https://algebrica.org/properties-of-real-numbers/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - additive-identity
  - additive-inverse
  - associativity
  - cauchy-sequence
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
  - rational-exponentiation
  - real-numbers
  - transitivity
  - triangle-inequality
  - trichotomy
---

## Order of operations

Expressions involving several operations require a fixed order of evaluation to have an unambiguous value. The mnemonic PEMDAS records this order:

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

+ In $3 + 4 \cdot 2,$ multiplication precedes addition. Since $4 \cdot 2 = 8,$ the value is $3 + 8 = 11.$
+ In $(3 + 4) \cdot 2,$ the parentheses require addition first. Since $3 + 4 = 7,$ the value is $7 \cdot 2 = 14.$
+ In $5 + 2^3 \cdot 4,$ exponentiation gives $2^3 = 8,$ multiplication gives $8 \cdot 4 = 32,$ and addition gives $5 + 32 = 37.$

## Density and completeness in $\mathbb{R}$

The real numbers are dense. For every $a,b\in\mathbb{R}$ with $a<b,$ the arithmetic mean $c=(a+b)/2$ satisfies $a<c<b.$ Repeatedly taking means gives infinitely many real numbers between $a$ and $b.$

The [integers](../integers/) are not dense because no integer lies between $2$ and $3.$ The [rational numbers](../rational-numbers/) $\mathbb{Q}$ are dense but incomplete. For example, $\sqrt{2}$ and $\pi$ are real but [irrational](../irrational-numbers/).

> The real numbers are dense and complete. Every non-empty subset of $\mathbb{R}$ bounded above has a least upper bound, or [supremum](../supremum-and-infimum/), in $\mathbb{R},$ and every [Cauchy sequence](../cauchy-sequence/) of real numbers converges to a real limit. The field $\mathbb{Q}$ is dense but has Cauchy sequences whose limits are irrational.

Order is preserved under [limits](../theorems-on-limits/) in its non-strict form. If convergent sequences satisfy $a_n\geq b_n$ for every $n,$ then $\lim a_n\geq\lim b_n.$ Strict inequalities need not remain strict. For example, $1+1/n>1-1/n$ for every positive integer $n,$ but both sequences converge to $1.$

For the non-strict statement, write $a=\lim a_n$ and $b=\lim b_n.$ If $a<b,$ set $\varepsilon=(b-a)/3.$ For all sufficiently large $n,$ one has $a_n<a+\varepsilon<b-\varepsilon<b_n,$ contradicting $a_n\geq b_n.$ Therefore $a\geq b.$

Two related $\varepsilon$ criteria are used throughout analysis. For real numbers $x$ and $y,$ if $x\leq y+\varepsilon$ for every $\varepsilon>0,$ then $x\leq y.$ Otherwise $x-y>0,$ and the choice $\varepsilon=(x-y)/2$ gives a contradiction. Similarly, if $|x-y|\leq\varepsilon$ for every $\varepsilon>0,$ then $x=y.$

## Closure property

The [set](../sets/) $\mathbb{R}$ is closed under addition and multiplication. For all $a,b\in\mathbb{R}:$

$$
a + b \in \mathbb{R}
$$

$$
a \cdot b \in \mathbb{R}
$$

Closure depends on both the set and the operation. The integers are closed under addition and multiplication but not division, since $1\div2$ is not an integer. The [natural numbers](../natural-numbers/) are not closed under subtraction, since $3-5$ is not natural.

> Closure makes addition and multiplication binary operations on $\mathbb{R}.$ Each operation maps a pair of real numbers to another real number.

## Commutative property

Addition and multiplication on $\mathbb{R}$ are commutative. For all $a,b\in\mathbb{R}:$

$$
a + b = b + a
$$

$$
a \cdot b = b \cdot a
$$

The real numbers form a commutative [field](../fields/). Subtraction and division are not commutative in general:

$$
5-2\neq2-5 \qquad \text{and} \qquad \frac{2}{5}\neq\frac{5}{2}
$$

For example, $3+7=7+3=10$ and $3\cdot7=7\cdot3=21.$ In both operations, exchanging the operands preserves the value.

> Commutativity permits terms in sums and factors in products to be reordered. For example, $2x+5=5+2x.$

## Associative property

Associativity permits a sum or product of several real numbers to be regrouped without changing its value. For all $a,b,c\in\mathbb{R}:$

$$
a + (b + c) = (a + b) + c
$$

$$
a \cdot (b \cdot c) = (a \cdot b) \cdot c
$$

The placement of parentheses does not change a sum or product. Subtraction and division are not associative in general:

$$
8-(4-2)=6\neq2=(8-4)-2
$$

$$
16\div(8\div2)=4\neq1=(16\div8)\div2
$$

Let $a = 2,$ $b = 3,$ and $c = 4.$ For addition:

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

In both cases, regrouping preserves the value. Hence expressions such as $a+b+c$ are unambiguous without parentheses.

## Distributive property

The distributive property relates multiplication to addition. For all $a,b,c\in\mathbb{R}:$

$$
a \cdot (b + c) = a \cdot b + a \cdot c
$$

$$
(b + c) \cdot a = b \cdot a + c \cdot a
$$

Multiplying a sum by a real number gives the sum of the two products. Since subtraction is addition of an additive inverse, the law also gives:

$$
a \cdot (b - c) = a \cdot b - a \cdot c
$$

- - -

Let $a = 3,$ $b = 4,$ and $c = 5.$ The left-hand side gives:

$$
3 \cdot (4 + 5) = 3 \cdot 9 = 27
$$

The right-hand side gives:

$$
3 \cdot 4 + 3 \cdot 5 = 12 + 15 = 27
$$

Both expressions have the same value. The distributive law expands $a(x+y)$ as $ax+ay$ and factors $ax+ay$ as $a(x+y).$ These two forms are used when simplifying expressions, solving [equations](../equations/), and manipulating [polynomials](../polynomials/).

> The distributive law is the field axiom that relates addition and multiplication.

## Identity properties

The real numbers have an additive identity and a multiplicative identity.

The additive identity $0$ satisfies, for every $a\in\mathbb{R}:$

$$
a + 0 = a \quad \text{and} \quad 0 + a = a
$$

The number $0$ is the additive identity because adding zero does not alter a real number. It is unique. If $a+n=a$ for all $a\in\mathbb{R},$ then $n=0.$

The multiplicative identity $1$ satisfies, for every $a\in\mathbb{R}:$

$$
a \cdot 1 = a \quad \text{and} \quad 1 \cdot a = a
$$

The number $1$ is the multiplicative identity because multiplying by one leaves every real number unchanged. It is unique. If $an=a$ for all $a\in\mathbb{R},$ then $n=1.$

> The additive identity $0$ is neutral for addition, and the multiplicative identity $1$ is neutral for multiplication.

## Inverse property

Every real number has an additive inverse, and every nonzero real number has a multiplicative inverse. Combining an element with its inverse gives the corresponding identity.

Every $a\in\mathbb{R}$ has an additive inverse $-a$ satisfying:

$$
a + (-a) = 0
$$

The number $-a$ is the additive inverse, or opposite, of $a.$ It is unique. If $a+b=0,$ then $b=-a.$

- - -

Every nonzero $a\in\mathbb{R}$ has a multiplicative inverse $1/a$ satisfying:

$$
a \cdot \frac{1}{a} = 1
$$

The number $\frac{1}{a}$ is the multiplicative inverse, or reciprocal, of $a.$ It is defined only for $a\neq0,$ since every product with $0$ equals $0.$ If $ab=1,$ then $b=1/a.$

> Closure, associativity, the additive identity, and additive inverses make $(\mathbb{R},+)$ an abelian [group](../groups/). The corresponding multiplicative axioms on the nonzero elements and the distributive law make $\mathbb{R}$ a [field](../fields/).

## The order relation

In addition to the field operations $+$ and $\cdot,$ the real numbers have an order relation $<.$ The relation $a>b$ means $b<a,$ the relation $a\leq b$ means $a<b$ or $a=b,$ and $a\geq b$ means $a>b$ or $a=b.$ A real number $a$ is positive when $a>0$ and negative when $a<0.$

The order relation is a binary relation, not an arithmetic operation. Its compatibility with the field operations makes $\mathbb{R}$ a totally ordered field.

The [absolute value](../absolute-value/) is defined from the order by $|x|=x$ when $x\geq0$ and $|x|=-x$ when $x<0.$ For all real numbers $x,y,$ it satisfies:

$$
|x|\geq0,\qquad |x|=0\Longleftrightarrow x=0
$$

$$
|xy|=|x||y|
$$

$$
|x+y|\leq|x|+|y|
$$

The bounds $-|x|\leq x\leq|x|$ and $-|y|\leq y\leq|y|$ give $-(|x|+|y|)\leq x+y\leq|x|+|y|,$ which proves the triangle inequality.

The function $d(x,y)=|x-y|$ is a distance on $\mathbb{R}.$ It is non-negative, satisfies $d(x,y)=0$ exactly when $x=y,$ is symmetric, and obeys:

$$
d(x,z)\leq d(x,y)+d(y,z)
$$

## Trichotomy and transitivity

The trichotomy law states that, for real numbers $a$ and $b,$ exactly one of the following conditions holds:

$$a < b \qquad a = b \qquad a > b$$

The three conditions are mutually exclusive and exhaustive. Hence every pair of real numbers is comparable.

The order is transitive. For any real numbers $a,b,c:$

$$a < b \text{ and } b < c \quad \Longrightarrow \quad a < c$$

Transitivity justifies the chained notation $a<b<c,$ which also implies $a<c.$

> Trichotomy and transitivity together make $\mathbb{R}$ a totally ordered set. They are independent of the field operations and concern only the comparability of pairs of real numbers.

## Compatibility with addition

Addition preserves order. For any real numbers $a,b,c:$

$$a < b \quad \Longrightarrow \quad a + c < b + c$$

The same statement holds for $\leq,$ $>,$ and $\geq.$ Subtracting the same quantity from both sides is the case obtained by adding $-c.$

Two inequalities with the same direction can be added. For any real numbers $a,b,c,d:$

$$a < b \text{ and } c < d \quad \Longrightarrow \quad a + c < b + d$$

Adding $c$ to the first inequality and $b$ to the second gives two inequalities that combine by transitivity. The analogous subtraction rule is false. From $a<b$ and $c<d,$ one cannot in general conclude $a-c<b-d.$

## Compatibility with multiplication

The effect of multiplication on an inequality depends on the sign of the multiplier. For any real numbers $a,b,c,$ two cases arise.

$$a < b \text{ and } c > 0 \quad \Longrightarrow \quad ac < bc$$

$$a < b \text{ and } c < 0 \quad \Longrightarrow \quad ac > bc$$

Multiplication by a positive number preserves the inequality, while multiplication by a negative number reverses it. Multiplication by any nonzero number preserves an equality.

The same statements hold for $\leq,$ $>,$ and $\geq.$ Division has the same rules because division by a nonzero number is multiplication by its reciprocal.

A related rule concerns the reciprocals of positive numbers. If $0 < a < b,$ then the reciprocals satisfy $0 < 1/b < 1/a,$ so inverting two positive numbers reverses their order. The reciprocal of a positive number is itself positive, because a positive number multiplied by a negative one would give a negative product, contradicting $a(1/a) = 1 > 0.$ Multiplying the inequality $a < b$ by the positive quantity $1/(ab)$ then yields $1/b < 1/a.$

> Multiplication by a negative number reverses an inequality but preserves an equality. This distinction is used when solving [inequalities](../inequalities/).

## The sign of a product

The multiplication rules determine the sign of a product. For any real numbers $a$ and $b:$

+ If $a$ and $b$ have the same sign (both positive or both negative), their product $ab$ is positive.
+ If $a$ and $b$ have opposite signs, their product $ab$ is negative.
+ If at least one of $a$ and $b$ is zero, their product $ab$ is zero.

The rule extends to a product of any finite number of nonzero real factors by induction. A product is positive when the number of negative factors is even, and negative when the number of negative factors is odd.

## The square rule

The square of every real number is non-negative. For any real number $a:$

$$a^2 \geq 0$$

The equality $a^2 = 0$ holds if and only if $a = 0,$ so the square of a nonzero real number is strictly positive. The proof of this fact is a direct application of the sign rule. When $a > 0,$ both factors of $a^2 = a \cdot a$ are positive and the product is positive. When $a < 0,$ both factors are negative and the product is positive. When $a = 0,$ the product is zero.

For example, $a^2+b^2$ is non-negative for all real numbers $a,b,$ and it is zero if and only if $a=b=0.$

Squaring is also monotone on the non-negative numbers. If $0 \leq a < b,$ then $a^2 < b^2,$ which follows from the factorisation $b^2 - a^2 = (b - a)(b + a)$ once one observes that both factors are positive. For non-negative numbers the converse holds as well, so $a^2 < b^2$ forces $a < b.$ Because of this monotonicity, the square root inverts squaring on $[0, +\infty),$ and two non-negative numbers can be compared through their squares.

The same reasoning applies to even powers $a^{2k}$ for any positive integer $k,$ since $a^{2k} = (a^k)^2$ is the square of a real number. Odd powers instead preserve the sign of the base, so $a^{2k+1}$ is positive when $a > 0$ and negative when $a < 0.$

More generally, for every positive integer $n,$ the map $x\mapsto x^n$ is [strictly increasing](../increasing-and-decreasing-functions/) on $[0,+\infty).$ If $0\leq a<b,$ then:

$$
b^n-a^n=(b-a)(b^{n-1}+b^{n-2}a+\cdots+a^{n-1})>0
$$

Consequently, every non-negative real number has at most one non-negative [$n$-th root](../radicals/). Its existence follows from completeness, as described in [real numbers](../real-numbers/). For $x>0$ and a [rational exponent](../powers/) $q=a/b$ with $a\in\mathbb{Z}$ and $b\in\mathbb{N}$ positive, define $x^q=(x^{1/b})^a.$ If $a/b=c/d$ is another representation with $c\in\mathbb{Z}$ and $d\in\mathbb{N}$ positive, then the positive numbers $(x^{1/b})^a$ and $(x^{1/d})^c$ have the same $bd$-th power, since $ad=bc.$ Uniqueness of positive roots makes the definition independent of the representation of $q.$ The exponent laws $x^{q+r}=x^qx^r,$ $(x^q)^r=x^{qr},$ and $x^{-q}=1/x^q$ follow from the corresponding integer laws.

## The ordered field structure

The preceding field and order axioms make $\mathbb{R}$ an ordered field. The field axioms are closure, associativity, commutativity, distributivity, identity elements, and inverse elements. The order axioms are trichotomy, transitivity, compatibility with addition, and compatibility with multiplication by positive numbers. The usual rules for $<,$ $\leq,$ $>,$ and $\geq$ follow from these axioms.

The ordered field axioms do not distinguish $\mathbb{R}$ from $\mathbb{Q},$ since both are ordered fields. The difference is completeness. Every non-empty subset of $\mathbb{R}$ bounded above has a least upper bound in $\mathbb{R},$ while the analogous statement fails in $\mathbb{Q}.$ The ordered field axioms together with completeness characterise $\mathbb{R}$ uniquely.

Not every field can be ordered compatibly with its operations. The [complex numbers](../complex-numbers/) $\mathbb{C}$ form a field, but any compatible order would make the square of every nonzero element positive. Since $i^2=-1,$ such an order would imply $-1>0,$ contradicting $1>0.$ Thus $\mathbb{R}$ is an ordered field and $\mathbb{C}$ is not.
