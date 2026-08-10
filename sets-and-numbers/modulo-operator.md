---
title: Modulo Operator
source: https://algebrica.org/modulo-operator/
license: CC BY-NC 4.0
tags:
  - bezout-identity
  - cancellation-law
  - cayley-table
  - chinese-remainder-theorem
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

For two integers $a$ and $n$ with $n > 0$, the modulo operator gives the remainder in the [Euclidean division](../floor-and-ceiling-functions/) of $a$ by $n$:

$$
a \bmod n = r
$$

Here $r$ is the unique integer satisfying $0 \le r < n$ and $a = qn + r$ for some integer $q$. The integer $q$ is the quotient, and $r$ is the remainder. The [division algorithm for integers](../integers/) states that each pair $(a, n)$ with $n > 0$ has a unique quotient $q$ and remainder $r$ satisfying these conditions. [Polynomial division](../polynomial-division/) over a field has the same existence and uniqueness property when the modulus is a fixed polynomial of positive degree.

The number $n$ is the modulus. When $a$ is positive, $a \bmod n$ is the usual remainder from elementary arithmetic. For example, $17 \bmod 5 = 2$, since $17 = 3 \cdot 5 + 2$. The quotient is $3$ and the remainder is $2$.

> The modulo operator is sometimes written as $a \ \mathrm{mod} \ n$ in textbooks and as `a % n` in many programming languages. For negative operands, a programming language may use a different convention from the mathematical definition.

- - -

When $a$ is negative, the remainder is still the unique integer in the range $0 \le r < n$. For $-7 \bmod 5$, the equation $-7 = q \cdot 5 + r$ has $q = -2$ and $r = 3$, since $-7 = (-2) \cdot 5 + 3$. Therefore $-7 \bmod 5 = 3$.

Programming languages do not all use this convention. In several languages, the result of % has the sign of the dividend, so $-7 \% 5$ is $-2$ rather than $3$. Under the definition above, the remainder is always non-negative.

## Congruence modulo n

Two integers $a$ and $b$ are congruent modulo $n$ if they have the same remainder upon division by $n$, or equivalently if their difference is a multiple of $n$. We write the relation as:

$$
a \equiv b \pmod{n}
$$

In terms of divisibility, $a \equiv b \pmod{n}$ if and only if $n \mid (a - b)$. For example, $17 \equiv 2 \pmod 5$ because $17 - 2 = 15$ is divisible by $5$. Equivalently, both $17$ and $2$ have remainder $2$ upon division by $5$.

The value $a \bmod n$ is a specific integer, whereas $a \equiv b \pmod n$ is a relation between two integers. The first is a [function](../functions/) of $a$ and $n$; the second is a statement that is either true or false. Congruence modulo $n$ is an [equivalence relation](../sets/) on the integers:

+ It is reflexive, since $a \equiv a \pmod n$ for every integer $a$.
+ It is symmetric, since $a \equiv b \pmod n$ implies $b \equiv a \pmod n$.
+ It is transitive, since $a \equiv b \pmod n$ and $b \equiv c \pmod n$ together imply $a \equiv c \pmod n$.

## Arithmetic properties

Congruence modulo $n$ is preserved by addition, subtraction, and multiplication. If $a \equiv b \pmod n$ and $c \equiv d \pmod n$, then the following congruences hold:

$$
\begin{align}
a + c &\equiv b + d \pmod n \\[6pt]
a - c &\equiv b - d \pmod n \\[6pt]
a \cdot c &\equiv b \cdot d \pmod n
\end{align}
$$

The three statements follow from the characterisation of congruence by divisibility. The hypotheses say that $n$ divides $a - b$ and $n$ divides $c - d$. For the sum, the difference of the two sides is:

$$
(a + c) - (b + d) = (a - b) + (c - d)
$$

Both summands on the right are divisible by $n$, hence so is the left side. Replacing $c - d$ by its negative proves the statement for subtraction. For multiplication, subtracting the right side from the left gives:

$$
ac - bd = (ac - bc) + (bc - bd) = (a - b)c + b(c - d)
$$

Each term on the right is divisible by $n$, so $n$ divides $ac - bd$.

An integer may be replaced by a congruent integer before addition, subtraction, or multiplication without changing the resulting residue class. Thus intermediate results may be reduced modulo $n$ throughout a computation.

Congruence is also preserved by non-negative integer [powers](../powers/). If $a \equiv b \pmod n$, then $a^k \equiv b^k \pmod n$ for every non-negative integer $k$. The statement follows from the multiplicative identity by [induction](../principle-of-mathematical-induction/) on $k$. Division does not have this unrestricted property because not every nonzero residue has a multiplicative inverse modulo $n$.

> A nonzero residue class $[a]_n$ has a multiplicative inverse if and only if $\gcd(a, n) = 1$. When an inverse exists, it is unique in $\mathbb{Z}/n\mathbb{Z}$.

Cancellation can fail in modular arithmetic. From $ac \equiv bc \pmod n$ one cannot conclude that $a \equiv b \pmod n$. With $n = 10$ and $c = 2$, the products $2 \cdot 3 = 6$ and $2 \cdot 8 = 16$ are congruent modulo $10,$ while $3$ and $8$ are not. In general, if $g = \gcd(c, n),$ then $ac \equiv bc \pmod n$ implies:

$$
a \equiv b \pmod{n/g}
$$

In the example $g = \gcd(2, 10) = 2,$ and the two residues are congruent modulo $5$. If $c$ is coprime with $n$, then $g = 1$ and ordinary cancellation is valid.

## Addition and multiplication tables

Addition and multiplication tables list every sum or product of two residues modulo $n$. Each row and column is labelled by a residue, and the entry at their intersection is the result reduced modulo $n$. For $n = 4$, the addition table is:

| + | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 1 | 2 | 3 |
| 1 | 1 | 2 | 3 | 0 |
| 2 | 2 | 3 | 0 | 1 |
| 3 | 3 | 0 | 1 | 2 |

Each row is a cyclic shift of the preceding row because addition by a fixed residue permutes the elements of $\mathbb{Z}/4\mathbb{Z}$. Every row and column contains each residue exactly once. The same property holds for addition modulo every positive integer.

The multiplication table modulo $4$ is:

| × | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 2 | 3 |
| 2 | 0 | 2 | 0 | 2 |
| 3 | 0 | 3 | 2 | 1 |

The row for $2$ does not contain $1$, so $2$ has no multiplicative inverse modulo $4$. This agrees with $\gcd(2, 4) = 2 \neq 1$. The rows for $1$ and $3$ contain $1$, so these two residues, both coprime with $4$, are invertible.

The entry in row $2$ and column $2$ is $0$, so a product of two nonzero residues can be zero. A nonzero residue $a$ is a zero divisor if $ab \equiv 0 \pmod n$ for some nonzero residue $b$. Modulo $4$ the residue $2$ is the only zero divisor. Modulo $12$ the residues $3$ and $4$ are zero divisors because their product is congruent to $0$. The integers have no zero divisors because a product of nonzero integers is nonzero.

> The Cayley table of a finite [group](../groups/) lists the result of its operation for every ordered pair of elements. The addition table modulo $n$ is the Cayley table of the cyclic group $(\mathbb{Z}/n\mathbb{Z}, +)$.

## Residue classes

For a fixed modulus $n$, the equivalence relation of congruence [partitions](../sets/) the set of integers into $n$ disjoint subsets, called residue classes or equivalence classes modulo $n$. The residue class of an integer $a$ is the set of all integers congruent to $a$ modulo $n$:

$$
[a]_n = \{ a + kn \mid k \in \mathbb{Z} \}
$$

Four conditions on a pair of integers $a$ and $b$ express the same relation:

+ $a \equiv b \pmod n$
+ $[a]_n = [b]_n$
+ $a \bmod n = b \bmod n$
+ $[a]_n \cap [b]_n \neq \emptyset$

Suppose $a \equiv b \pmod n$. If $c \equiv a \pmod n$, then transitivity gives $c \equiv b \pmod n$. The reverse inclusion follows from $b \equiv a \pmod n$, so $[a]_n = [b]_n$. Equal classes have the same unique element in the range $0 \le r < n$, so $a \bmod n = b \bmod n$. This common remainder belongs to both classes, which makes their intersection nonempty. Conversely, if $c$ belongs to the intersection, then $a \equiv c \pmod n$ and $c \equiv b \pmod n,$ so transitivity gives $a \equiv b \pmod n$.

The intersection condition shows that two residue classes are either equal or disjoint. Every integer belongs to the class of its remainder, so the classes are $[0]_n, [1]_n, \ldots, [n-1]_n$. They are pairwise distinct because the difference of two distinct remainders in the range $0 \le r < n$ is nonzero and has [absolute value](../absolute-value/) less than $n$, so it is not a multiple of $n$. The set of all residue classes modulo $n$ is denoted by $\mathbb{Z}/n\mathbb{Z}$ and has exactly these $n$ elements.

For $n = 4$, the integers split into four residue classes:

$$
\begin{align}
[0]_4 &= \{ \ldots, -8, -4, 0, 4, 8, \ldots \} \\[6pt]
[1]_4 &= \{ \ldots, -7, -3, 1, 5, 9, \ldots \} \\[6pt]
[2]_4 &= \{ \ldots, -6, -2, 2, 6, 10, \ldots \} \\[6pt]
[3]_4 &= \{ \ldots, -5, -1, 3, 7, 11, \ldots \}
\end{align}
$$

Every integer belongs to exactly one of these four classes, and the union of the four classes is all of $\mathbb{Z}$.

## Linear congruences and inverses

A linear congruence has the form $ax \equiv b \pmod n$, where $a$, $b$, and $n$ are fixed integers with $n > 0$ and $x$ is the unknown. Its solutions are the integers $x$ that satisfy the relation, grouped into residue classes modulo $n$.

The congruence has a solution if and only if $\gcd(a, n)$ divides $b$. When this condition holds, the solutions form one residue class modulo $n / \gcd(a, n)$, which corresponds to $\gcd(a, n)$ distinct classes modulo $n$. The criterion follows from Bézout's identity. For any integers $a$ and $n$, some integers $u$ and $v$ satisfy:

$$
au + nv = \gcd(a, n)
$$

For $b = 1$, the solutions of $ax \equiv 1 \pmod n$ are the multiplicative inverses of $a$ modulo $n$. Such an inverse exists if and only if $\gcd(a, n) = 1$, and it is then unique modulo $n$. The extended Euclidean algorithm computes integers $u$ and $v$ satisfying $au + nv = 1$. Reduction modulo $n$ gives $au \equiv 1 \pmod n$, so $u$ is an inverse of $a$.

For $a = 7$ and $n = 12$, the inverse exists because $\gcd(7, 12) = 1$. The identity $7 \cdot 7 + 12 \cdot (-4) = 1$ gives $7 \cdot 7 \equiv 1 \pmod{12}$. Thus $7$ is its own inverse modulo $12$.

If $\gcd(a, n) = 1$ and $u$ is the inverse of $a$, then $ax \equiv b \pmod n$ has the unique solution class $x \equiv ub \pmod n$. Indeed, multiplication by $u$ gives $uax \equiv ub \pmod n$, and $ua \equiv 1 \pmod n$. For $a = 7$ and $n = 12,$ the congruence $7x \equiv 5 \pmod{12}$ has the solution $x \equiv 7 \cdot 5 = 35 \equiv 11 \pmod{12}$. The identity $7 \cdot 11 = 6 \cdot 12 + 5$ verifies the solution.

Suppose $g = \gcd(a, n) > 1$ and $g$ divides $b$. Dividing $a$, $b$, and $n$ by $g$ gives:

$$
\frac{a}{g}x \equiv \frac{b}{g} \pmod{n/g}
$$

The coefficient $a/g$ is coprime with the modulus $n/g$, so the reduced congruence has one solution class modulo $n/g$. This class corresponds to $g$ classes modulo $n$. For example, consider $6x \equiv 9 \pmod{15}$. Here $g = 3$ divides $9,$ and the reduced congruence is $2x \equiv 3 \pmod 5$. The inverse of $2$ modulo $5$ is $3,$ so $x \equiv 9 \equiv 4 \pmod 5$. The original congruence has the three solutions $x = 4$, $x = 9$, and $x = 14$ modulo $15$.

## Fermat's little theorem and Euler's theorem

Fermat's little theorem concerns powers modulo a prime. If $p$ is prime and $a$ is not divisible by $p$, then the following congruence holds:

$$
a^{p-1} \equiv 1 \pmod p
$$

Equivalently, $a^p \equiv a \pmod p$ for every integer $a$. For $a$ not divisible by $p$, exponents may therefore be reduced modulo $p-1$.

Euler's theorem generalises the previous statement to an arbitrary modulus $n$. Let $\varphi(n)$ denote the Euler totient, defined as the number of integers in the range $1 \le k \le n$ that are coprime with $n$. If $\gcd(a, n) = 1$, then the following congruence holds:

$$
a^{\varphi(n)} \equiv 1 \pmod n
$$

When $n = p$ is prime, every integer in the range $1 \le k \le p - 1$ is coprime with $p$, so $\varphi(p) = p - 1$ and Euler's theorem reduces to Fermat's little theorem.

## The Chinese remainder theorem

The Chinese remainder theorem gives existence and uniqueness for systems of congruences with pairwise coprime moduli. Suppose the integers $n_1, n_2, \ldots, n_k$ are pairwise coprime and $a_1, a_2, \ldots, a_k$ are arbitrary integers. Consider the system:

$$
\begin{align}
x &\equiv a_1 \pmod{n_1} \\[6pt]
x &\equiv a_2 \pmod{n_2} \\[6pt]
  &\ \vdots \\[6pt]
x &\equiv a_k \pmod{n_k}
\end{align}
$$

The theorem states that such an integer exists and is unique modulo $N = n_1n_2 \cdots n_k$. For two coprime moduli, Bézout's identity gives integers $s$ and $t$ with $sn_1 + tn_2 = 1$. Let $e_1 = tn_2$ and $e_2 = sn_1$. The integer $e_1$ is a multiple of $n_2$ and differs from $1$ by the multiple $sn_1$ of $n_1$, so $e_1 \equiv 1 \pmod{n_1}$ and $e_1 \equiv 0 \pmod{n_2}$. Similarly, $e_2 \equiv 0 \pmod{n_1}$ and $e_2 \equiv 1 \pmod{n_2}$. For arbitrary $a_1$ and $a_2$, a solution is:

$$
x = a_1e_1 + a_2e_2
$$

Modulo $n_1$, the second term is congruent to zero and the first is congruent to $a_1$. Modulo $n_2$, the first term is congruent to zero and the second is congruent to $a_2$. Thus $x$ satisfies both congruences. If $x'$ is another solution, both $n_1$ and $n_2$ divide $x - x',$ and coprimality implies that $n_1n_2$ divides $x - x'$.

Iterating the construction proves the statement for any finite number of congruences. In terms of [rings](../rings/), the theorem gives the following [isomorphism](../homomorphisms-and-isomorphisms/):

$$
\mathbb{Z}/N\mathbb{Z} \cong \mathbb{Z}/n_1\mathbb{Z} \times \mathbb{Z}/n_2\mathbb{Z} \times \cdots \times \mathbb{Z}/n_k\mathbb{Z}
$$

This isomorphism sends addition and multiplication modulo $N$ to componentwise addition and multiplication modulo the factors $n_i$.

Consider the system $x \equiv 2 \pmod 3$ and $x \equiv 3 \pmod 5$. The Bézout identity $2 \cdot 3 - 1 \cdot 5 = 1$ gives $s = 2$ and $t = -1,$ so $e_1 = -5$ and $e_2 = 6$. The formula gives $x = 2 \cdot (-5) + 3 \cdot 6 = 8$. The equalities $8 = 2 \cdot 3 + 2$ and $8 = 1 \cdot 5 + 3$ verify both congruences. The set of solutions is the residue class $[8]_{15} = \{ \ldots, -7, 8, 23, 38, \ldots \}$.

## Examples

Suppose today is Wednesday and we want to determine the day of the week in $100$ days. Since $100 = 14 \cdot 7 + 2$, we have $100 \bmod 7 = 2$. The day is therefore two days after Wednesday, which is Friday, because the seven weekdays repeat after each complete week.

Parity is determined by the residue modulo $2$. An integer $a$ is even if $a \bmod 2 = 0$ and odd if $a \bmod 2 = 1$. The two residue classes modulo $2$ are the even and odd integers. The usual rules of parity, such as "even plus even is even" and "odd times odd is odd", are special cases of the arithmetic properties of congruences.

The residue $7^{100} \bmod 10$ is the last decimal digit of $7^{100}$. The successive powers of $7$ modulo $10$ are $7, 9, 3, 1, 7, 9, 3, 1, \ldots$, with period $4$.

Since $100 = 25 \cdot 4$, the exponent contains $25$ complete periods, so $7^{100} \equiv 1 \pmod{10}$. The last digit of $7^{100}$ is therefore $1$. The same conclusion follows from Euler's theorem, since $\varphi(10) = 4$ and $\gcd(7, 10) = 1$ imply $7^{4} \equiv 1 \pmod{10}$, from which $7^{100} = (7^{4})^{25} \equiv 1 \pmod{10}$.

## Relation with algebraic structures

Addition and multiplication of residue classes modulo $n$ are defined by:

$$
[a]_n + [b]_n = [a+b]_n \qquad [a]_n \cdot [b]_n = [a \cdot b]_n
$$

For these formulas to define operations on $\mathbb{Z}/n\mathbb{Z}$, their values must be independent of the chosen representatives. Suppose $a' \in [a]_n$ and $b' \in [b]_n$. Then $a \equiv a' \pmod n$ and $b \equiv b' \pmod n,$ so the arithmetic properties of congruence give $a + b \equiv a' + b' \pmod n$ and $ab \equiv a'b' \pmod n$. Therefore $[a+b]_n = [a'+b']_n$ and $[ab]_n = [a'b']_n$, and both operations are well defined.

An arbitrary partition of $\mathbb{Z}$ need not have this property. Group the integers according to the number of decimal digits of their absolute value. The integers $3$, $4$, $6$, and $7$ then belong to the one-digit class. The sum $3 + 4 = 7$ has one digit, whereas $6 + 7 = 13$ has two. The class of the sum depends on the representatives, so addition is not well defined on these classes. For residue classes, congruence is compatible with addition and multiplication, which gives the required independence.

The ring laws on $\mathbb{Z}/n\mathbb{Z}$ follow from the corresponding identities in $\mathbb{Z}$. For example, the following calculation proves associativity of multiplication:

$$
\begin{align}
([a]_n[b]_n)[c]_n &= [ab]_n[c]_n = [(ab)c]_n \\[6pt]
&= [a(bc)]_n = [a]_n[bc]_n = [a]_n([b]_n[c]_n)
\end{align}
$$

The middle equality is associativity in $\mathbb{Z}$. The other ring laws follow in the same way.

+ Addition is commutative and associative.
+ The class $[0]_n$ is the additive identity, and $[-a]_n$ is the additive inverse of $[a]_n$.
+ Multiplication is commutative and associative.
+ The class $[1]_n$ is the multiplicative identity.
+ Multiplication distributes over addition.

A set carrying two operations with these properties is a commutative [ring](../rings/), so $\mathbb{Z}/n\mathbb{Z}$ is a finite commutative ring.

Every nonzero class in $\mathbb{Z}/n\mathbb{Z}$ is either invertible or a zero divisor, but not both. Modulo $12$ the invertible classes are $[1]_{12}$, $[5]_{12}$, $[7]_{12}$, and $[11]_{12}$, whose representatives are coprime with $12$. Each remaining nonzero class is a zero divisor because the products $[2]_{12}[6]_{12}$, $[3]_{12}[4]_{12}$, $[8]_{12}[3]_{12}$, $[9]_{12}[4]_{12}$, and $[10]_{12}[6]_{12}$ are all equal to $[0]_{12}$.

The two cases are mutually exclusive. Suppose $[a]_n[b]_n = [1]_n$ and $[a]_n[c]_n = [0]_n$. Associativity gives:

$$
[c]_n = ([b]_n[a]_n)[c]_n = [b]_n([a]_n[c]_n) = [b]_n[0]_n = [0]_n
$$

Thus an invertible class annihilates no nonzero class. A counting argument proves that every nonzero, noninvertible class is a zero divisor. Multiplication by a fixed class defines the map:

$$
\mu_a : \mathbb{Z}/n\mathbb{Z} \to \mathbb{Z}/n\mathbb{Z} \qquad \mu_a([x]_n) = [ax]_n
$$

If $[a]_n$ has no inverse, no class maps to $[1]_n$, so $\mu_a$ is not surjective. A map from a finite set to itself that is not surjective is not injective. Hence two distinct classes $[x]_n$ and $[y]_n$ satisfy $[ax]_n = [ay]_n$. Their difference is a nonzero class annihilated by $[a]_n$, so $[a]_n$ is a zero divisor. Finiteness is necessary for this argument. In $\mathbb{Z}$, the integer $2$ has no inverse and is not a zero divisor.

When $n$ is prime, every nonzero residue is coprime with $n$ and is therefore invertible. Hence $\mathbb{Z}/n\mathbb{Z}$ has no zero divisors and is a [field](../fields/).

A [polynomial ring](../polynomials/) over a field can also be quotiented by the ideal generated by a nonconstant polynomial. Polynomial division gives each residue class a representative whose degree is smaller than the degree of the modulus. For example, the quotient $\mathbb{R}[x]/(x^2 + 1)$ is isomorphic to the field of [complex numbers](../complex-numbers/), denoted by $\mathbb{C}$.
