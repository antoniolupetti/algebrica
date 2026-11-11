---
title: Modulo Operator
source: https://algebrica.org/modulo-operator/
license: CC BY-NC 4.0
tags:
  - bezout-identity
  - cancellation-law
  - cayley-table
  - congruence
  - division-algorithm
  - equivalence-relation
  - euclidean-algorithm
  - eulers-theorem
  - eulers-totient
  - fermat-little-theorem
  - linear-congruence
  - modular-arithmetic
  - modulo-operator
  - multiplicative-inverse
  - remainder
  - residue-class
  - ring-z-nz
  - zero-divisor
---
## Definition

The modulo operator returns the remainder of [Euclidean division](../euclidean-division/) and is useful when a count repeats at regular intervals and we want to know where we are in the cycle. For an intuitive example, if today is Monday and we want to know what day it will be in $17$ days, we count $14$ days (two weeks) plus the remaining 3 days to arrive at Thursday. Formally, given integers $a$ and $n$ with $n\gt 0,$ the modulo operator is defined by the following equation.

$$
a \bmod n = r \tag{1}
$$

For example, $17\bmod5=2,$ since $17=3\cdot5+2.$ In equation $(1),$ $n$ is the modulus and $r$ is the remainder of Euclidean division of $a$ by $n,$ the unique integer from $0$ to $n-1$ that satisfies the following equation for some integer quotient.

$$
a = qn + r \tag{2}
$$

The integer $q$ is the quotient. By the Euclidean division theorem, equation $(2)$ determines a unique pair of integers $(q,r)$ with $0\leq r\lt n.$ When $a$ is negative, the remainder in $(1)$ is still the unique integer in the range $0\leq r\lt n$ that satisfies the definition. For example, to find $-7\bmod5,$ the equation $-7=q\cdot5+r$ gives $q=-2$ and $r=3,$ since $-7=(-2)\cdot5+3.$ Hence $-7\bmod5=3.$

## Congruence

Two integers $a$ and $b$ are congruent modulo $n$ if they have the same remainder upon division by $n$ or, equivalently, if their difference is a multiple of $n.$ The relation is written as follows.

$$
a \equiv b \pmod{n} \tag{3}
$$

If $a$ and $b$ have the same remainder $r,$ we can write $a=q_an+r$ and $b=q_bn+r,$ and subtracting gives the following identity.

$$
a-b=(q_a-q_b)n \tag{4}
$$

Conversely, if $a-b=kn$ for some integer $k$ and $b=q_bn+r,$ then $a=(q_b+k)n+r.$ The quotient changes by $k$ and the remainder stays the same. Formula $(5)$ thus expresses the equivalence between congruence of $a$ and $b$ modulo $n$ and divisibility of $a-b$ by $n.$

$$
a\equiv b\pmod n \quad\Longleftrightarrow\quad n\mid(a-b) \tag{5}
$$

The two integers have the same remainder, so they are congruent modulo $5,$ and we can write $(3)$ in this case as $17\equiv2\pmod5.$ Congruence modulo $n$ is an [equivalence relation](../sets/) on the integers, with the following properties.

+ It is reflexive because $a\equiv a\pmod n$ for every integer $a.$
+ It is symmetric because $a\equiv b\pmod n$ implies $b\equiv a\pmod n.$
+ It is transitive because $a\equiv b\pmod n$ and $b\equiv c\pmod n$ imply $a\equiv c\pmod n.$

Congruence also has the algebraic properties given below. First, congruence modulo $n$ is preserved under addition, subtraction, and multiplication, so if $a\equiv b\pmod n$ and $c\equiv d\pmod n,$ the following relations hold.

$$
\begin{aligned}
a + c &\equiv b + d \pmod n \\[6pt]
a - c &\equiv b - d \pmod n \\[6pt]
a \cdot c &\equiv b \cdot d \pmod n
\end{aligned} \tag{6}
$$

The assumptions $a\equiv b\pmod n$ and $c\equiv d\pmod n$ tell us that $a-b$ and $c-d$ are multiples of $n.$ To prove that the sums $a+c$ and $b+d$ are congruent modulo $n,$ we must show that their difference is also a multiple of $n.$

$$
(a + c) - (b + d) = (a - b) + (c - d) \tag{7}
$$

Since the right-hand side of $(7)$ is the sum of two multiples of $n,$ the difference is also a multiple of $n.$ It follows that $a+c\equiv b+d\pmod n.$ The same criterion applies to subtraction, using the following identity.

$$
(a-c)-(b-d)=(a-b)-(c-d)\tag{8}
$$

For multiplication, we use the following identity.

$$
ac-bd=(a-b)c+b(c-d) \tag{9}
$$

Here too, both terms on the right are multiples of $n,$ so $ac\equiv bd\pmod n.$ By [induction](../principle-of-mathematical-induction/), compatibility with multiplication extends to [powers](../powers/). If $a\equiv b\pmod n,$ then the following holds for every integer $k \gt 0.$

$$
a^k\equiv b^k\pmod n \tag{10}
$$

By $(6)$ and $(10),$ we can reduce intermediate sums, differences, products, and powers modulo $n$ without changing the final remainder. For example, to find the remainder when $17\cdot8$ is divided by $5,$ we can replace each factor with its remainder upon division by $5.$ The remainder for $17$ is $2$ and the remainder for $8$ is $3.$ The product of the remainders is $2\cdot3=6.$ Dividing $6$ by $5$ gives a remainder of $1$ because $6=1\cdot5+1,$ so by $(6)$ the original product $17\cdot8$ also gives a remainder of $1$ upon division by $5.$

Property $(6)$ allows us to multiply both sides of a congruence by the same integer $c.$ To see when we can cancel that factor, we use $(5).$ If $ac\equiv bc\pmod n,$ then $n$ divides $c(a-b).$ With $g=\gcd(c,n),$ the integers $c/g$ and $n/g$ are coprime. Since $n/g$ divides $(c/g)(a-b),$ it must also divide $a-b.$ Applying $(5)$ again gives the following congruence.

$$
a\equiv b\pmod{n/g} \tag{11}
$$

Thus, if $c$ is coprime to $n,$ then $g=1$ and $(11)$ retains the modulus $n.$

## Addition and multiplication tables

The following tables show the remainder of a sum or product modulo $n$ at a glance. They are straightforward to construct. The rows and columns are numbered from $0$ to $n-1,$ and each cell contains the remainder obtained by dividing the corresponding sum or product by $n.$ For example, the table below gives addition modulo $4.$ The sum $2+3$ equals $5,$ so we enter its remainder, $1,$ in the corresponding cell.

| +   | 0   | 1   | 2   | 3   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 1   | 2   | 3   |
| 1   | 1   | 2   | 3   | 0   |
| 2   | 2   | 3   | 0   | 1   |
| 3   | 3   | 0   | 1   | 2   |

Each row is a cyclic shift of the preceding row because adding a fixed residue permutes the elements of $\mathbb{Z}/4\mathbb{Z}.$ We construct the multiplication table modulo $4$ in the same way. Here, multiplying $3 \cdot 3$ gives $9,$ which has remainder $1$ modulo $4.$

| × | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 2 | 3 |
| 2 | 0 | 2 | 0 | 2 |
| 3 | 0 | 3 | 2 | 1 |

The row for $2$ contains no $1,$ so $2$ has no multiplicative inverse modulo $4,$ consistent with $\gcd(2,4)=2\neq1.$ The rows for $1$ and $3$ contain $1,$ so these two residues, both coprime to $4,$ are invertible.

> The addition table modulo $n$ is the [Cayley table](../groups/) of the cyclic group $(\mathbb{Z}/n\mathbb{Z},+).$ A Cayley table gives the result of the group operation for each pair of elements of a finite group. To obtain the Cayley table of the multiplicative group, keep only the rows and columns for the invertible residues. Modulo $4,$ for example, these residues are $1$ and $3.$

## Residue classes

If we fix a modulus $n$ and group the integers by their remainders upon division by $n,$ each group is a residue class, also called an equivalence class modulo $n.$ The class $[a]_n$ contains all integers congruent to $a,$ which by $(5)$ are obtained by adding a multiple of $n$ to $a$ as shown below.

$$
[a]_n = \{ a + kn \mid k \in \mathbb{Z} \} \tag{12}
$$

Classes with different remainders are disjoint. When the remainders differ, the classes are disjoint because each integer has only one remainder upon division by $n.$ If an integer $c$ belongs to both $[a]_n$ and $[b]_n,$ its remainder upon division by $n$ is the same as that of $a$ and $b.$ The two classes therefore contain all the integers with the same remainder and coincide.

The possible remainders modulo $n$ are $0,1,\ldots,n-1,$ and each of these integers represents its own class. Thus the residue classes are $[0]_n,[1]_n,\ldots,[n-1]_n,$ and their set is denoted by $\mathbb{Z}/n\mathbb{Z}.$ For example, when $n=4,$ the integers fall into the following residue classes.

$$
\begin{align}
[0]_4 &= \{ \ldots, -8, -4, 0, 4, 8, \ldots \} \\[6pt]
[1]_4 &= \{ \ldots, -7, -3, 1, 5, 9, \ldots \} \\[6pt]
[2]_4 &= \{ \ldots, -6, -2, 2, 6, 10, \ldots \} \\[6pt]
[3]_4 &= \{ \ldots, -5, -1, 3, 7, 11, \ldots \}
\end{align}
$$

## Linear congruences and inverses

Given integers $a,$ $b,$ and $n$ with $n\gt 0,$ we define a linear congruence in the unknown $x$ as follows.

$$
ax\equiv b\pmod n \tag{13}
$$

The solutions of $(13)$ are the integers $x$ that satisfy the relation, grouped into residue classes modulo $n.$ Congruence $(13)$ has a solution if and only if $\gcd(a,n)$ divides $b,$ in which case the solutions form one class modulo $n/\gcd(a,n)$ corresponding to $\gcd(a,n)$ distinct classes modulo $n.$

To justify the criterion for the existence of solutions to $(13),$ let $g=\gcd(a,n).$ By $(5),$ if $x$ is a solution, then $ax-b$ is a multiple of $n.$ Since $g$ divides both $a$ and $n,$ it must also divide $b.$ For the converse, we use [Bézout's identity](../greatest-common-divisor/), which states that there are integers $u$ and $v$ satisfying the following equation.

$$
au + nv = g \tag{14}
$$

If $g$ divides $b,$ we write $b=kg$ for some integer $k.$ Multiplying $(14)$ by $k$ gives $b-a(ku)=n(kv).$ The difference is a multiple of $n,$ so by $(5),$ $x=ku$ solves $(13).$

- - -

For $b=1,$ a solution of $(13)$ is an inverse of $a$ modulo $n,$ and it exists if and only if $g=1.$ In this case, the extended Euclidean algorithm computes the coefficients in $(14).$ Since $nv$ is a multiple of $n,$ equation $(14)$ gives $au\equiv1\pmod n.$ For any right-hand side $b,$ multiplying both sides of $(13)$ by $u$ gives the unique solution class $x\equiv ub\pmod n.$

For example, $7$ is its own inverse modulo $12$ because $7\cdot7=4\cdot12+1.$ Thus $7x\equiv5\pmod{12}$ is equivalent to $x\equiv7\cdot5\equiv11\pmod{12}.$

If $g\gt 1$ and $g$ divides $b,$ congruence $(13)$ is equivalent to the congruence obtained by dividing the coefficient of $x,$ the right-hand side, and the modulus by $g.$

$$
\frac{a}{g}x \equiv \frac{b}{g} \pmod{n/g} \tag{15}
$$

Since $a/g$ and $n/g$ are coprime, $(15)$ has a single solution class modulo $n/g,$ which corresponds to $g$ classes modulo $n.$ For example, $6x\equiv9\pmod{15}$ reduces to $2x\equiv3\pmod5.$ Multiplying by $3,$ the inverse of $2$ modulo $5,$ gives $x\equiv4\pmod5.$ The residues modulo $15$ that leave a remainder of $4$ upon division by $5$ are $4,$ $9,$ and $14.$

Systems involving more than one modulus are covered in the entry on the [Chinese remainder theorem](../chinese-remainder-theorem/).

## Fermat's little theorem and Euler's theorem

Fermat's little theorem and Euler's theorem let us find the remainder of a power with a large exponent by using a power with a smaller exponent. The idea is to find an exponent $m$ for which $a^m$ leaves a remainder of $1$ modulo $n.$ If we write the exponent $k$ as $k=qm+r$ with $0\leq r\lt m,$ then $a^k=(a^m)^qa^r$ has the same remainder as $a^r.$ If the modulus $p$ is prime and $a$ is not divisible by $p,$ Fermat's little theorem lets us take $m=p-1$ and gives the following congruence.

$$
a^{p-1} \equiv 1 \pmod p \tag{16}
$$

An equivalent form of the theorem, valid for every integer $a,$ is $a^p\equiv a\pmod p.$ For example, to find the remainder of $3^{100}$ upon division by $7,$ we use $(16)$ with $p=7.$ Since $3^6\equiv1\pmod7$ and $100=16\cdot6+4,$ we need only find the remainder of $3^4=81$ upon division by $7,$ which is $4.$

For any modulus $n\gt 1,$ Euler's theorem lets us take $m=\varphi(n)$ when $a$ and $n$ are coprime, where $\varphi(n)$ counts the integers from $1$ to $n$ that are coprime to $n.$ Under this assumption, the following congruence holds.

$$
a^{\varphi(n)} \equiv 1 \pmod n \tag{17}
$$

If $n=p$ is prime, every integer from $1$ to $p-1$ is coprime to $p.$ Therefore $\varphi(p)=p-1,$ and $(17)$ coincides with $(16).$

## Connection with algebraic structures

The congruence properties in $(6)$ let us extend the operations on integers to residue classes. Addition and multiplication defined in this way give $\mathbb{Z}/n\mathbb{Z}$ the structure of a [ring](../rings/). To add or multiply two classes, we choose a representative from each class, perform the operation on the integers, and take the class of the result.

$$
\begin{aligned}
[a]_n + [b]_n &= [a+b]_n \\[6pt]
[a]_n[b]_n &= [ab]_n
\end{aligned} \tag{18}
$$

The result in $(18)$ is independent of the choice of representatives because, if we choose $a'$ in the class of $a$ and $b'$ in the class of $b,$ property $(6)$ guarantees that $a+b$ and $a'+b'$ belong to the same class. The same holds for $ab$ and $a'b'.$ This independence depends on how we have grouped the integers. If we grouped them by the number of digits in their [absolute values](../absolute-value/), $3,$ $4,$ $6,$ and $7$ would all belong to the same class. Yet $3+4=7$ has one digit, whereas $6+7=13$ has two. The class of the sum would therefore depend on the representatives chosen.

The operations in $(18)$ inherit the properties of addition and multiplication on the integers. For example, associativity of multiplication follows by replacing $(ab)c$ with $a(bc)$ within the residue class.

$$
\begin{aligned}
([a]_n[b]_n)[c]_n &= [(ab)c]_n \\[6pt]
&= [a(bc)]_n = [a]_n([b]_n[c]_n)
\end{aligned} \tag{19}
$$

Addition and multiplication are both associative and commutative, and multiplication distributes over addition. The class $[0]_n$ is the additive identity, $[-a]_n$ is the additive inverse of $[a]_n,$ and $[1]_n$ is the multiplicative identity. With these operations, $\mathbb{Z}/n\mathbb{Z}$ is a finite commutative ring.

A nonzero class $[a]_n$ is called a zero divisor if there is a nonzero class $[b]_n$ such that $[a]_n[b]_n=[0]_n.$

The criterion for solving $(13)$ with $b=1$ shows that $[a]_n$ is invertible if and only if $\gcd(a,n)=1.$ If $[a]_n$ is invertible and $[a]_n[b]_n=[0]_n,$ multiplying by the inverse of $[a]_n$ gives $[b]_n=[0]_n.$ If instead $[a]_n$ is nonzero and $g=\gcd(a,n)\gt 1,$ the class $[n/g]_n$ is nonzero and the product is zero because $a(n/g)=(a/g)n,$ which gives the following equation.

$$
[a]_n[n/g]_n=[0]_n \tag{20}
$$

Every nonzero class is therefore either invertible or a zero divisor. Modulo $12,$ the invertible classes are those of $1,$ $5,$ $7,$ and $11,$ the only residues coprime to $12.$ For example, the class of $8$ is a zero divisor. Since $\gcd(8,12)=4,$ equation $(20)$ gives $[8]_{12}[3]_{12}=[0]_{12}.$

When $n$ is prime, every nonzero residue is coprime to $n.$ Thus every nonzero class is invertible and $\mathbb{Z}/n\mathbb{Z}$ is a [field](../fields/).

As with integers, we can form a ring of residue classes for [polynomials](../polynomials/) with coefficients in a field. For instance, fix a nonconstant polynomial and group together the polynomials that have the same remainder upon [division](../polynomial-division/) by it. In the quotient $\mathbb{R}[x]/(x^2+1),$ for example, each class is represented by a polynomial $a+bx,$ and the square of the class of $x$ is the class of $-1.$ Mapping the class of $a+bx$ to the number $a+bi$ gives an [isomorphism](../homomorphisms-and-isomorphisms/) with $\mathbb{C}.$
