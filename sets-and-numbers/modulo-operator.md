---
title: Modulo Operator
source: https://algebrica.org/modulo-operator/
license: CC BY-NC 4.0
tags:
  - bezout-identity
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
---

## Definition

The modulo operator is one of the most frequently used operations in [integer](../integers/) arithmetic. Given two integers, it returns the remainder left over after dividing the first by the second. The operator plays a central role in number theory, computer science, and the construction of several algebraic structures. Given two integers $a$ and $n$ with $n > 0$, the modulo operator is defined as follows:

$$
a \bmod n = r
$$

Here $r$ is the unique integer satisfying $0 \le r < n$ and $a = qn + r$ for some integer $q$. The integer $q$ is the quotient of the division of $a$ by $n$, and $r$ is the remainder. The existence and uniqueness of this decomposition is guaranteed by the division algorithm for integers, which states that for every pair $(a, n)$ with $n > 0$ there is exactly one such pair $(q, r)$. An analogous statement holds for [polynomials](../polynomial-division/) over a field, where the role of the modulus is played by a fixed polynomial of positive degree.

The number $n$ is called the modulus. When $a$ is positive, the value of $a \bmod n$ coincides with the intuitive notion of the remainder learned in elementary arithmetic. For example, $17 \bmod 5 = 2$, since $17 = 3 \cdot 5 + 2$. The quotient is $3$ and the remainder is $2$.

> The modulo operator is sometimes written as $a \ \mathrm{mod} \ n$ in textbooks, and as `a % n` in many programming languages, although the behaviour for negative operands may differ between the mathematical definition and specific programming implementations.

## Modulo of a negative integer

A subtle point arises when $a$ is negative. The mathematical definition requires the remainder to satisfy $0 \le r < n$, so the result is always a non-negative integer strictly smaller than the modulus. Consider $-7 \bmod 5$. Writing $-7 = q \cdot 5 + r$ with $0 \le r < 5$, one finds $q = -2$ and $r = 3$, since $-7 = (-2) \cdot 5 + 3$. Therefore $-7 \bmod 5 = 3$, not $-2$ as one might naively expect.

The convention is not universal. In several programming languages the `%` operator follows the sign of the dividend, so that `-7 % 5` returns $-2$ rather than $3$. In a purely mathematical context, the remainder is always taken to be non-negative.

## Congruence modulo n

Closely related to the modulo operator is the notion of congruence. Two integers $a$ and $b$ are congruent modulo $n$ if they leave the same remainder when divided by $n$, or equivalently if their difference is a multiple of $n$. The relation is written as follows:

$$
a \equiv b \pmod{n}
$$

The equivalent characterisation in terms of divisibility states that $a \equiv b \pmod{n}$ if and only if $n \mid (a - b)$. For example, $17 \equiv 2 \pmod 5$ because $17 - 2 = 15$ is divisible by $5$, and equivalently because both $17$ and $2$ leave remainder $2$ when divided by $5$.

The operator $a \bmod n$, which produces a specific integer, is distinct from the congruence $a \equiv b \pmod n$, which is a relation between two integers. The first is a function of $a$ and $n$; the second is a statement that can be true or false depending on the integers involved. Congruence modulo $n$ is an [equivalence relation](../sets/) on the integers:

+ It is reflexive, since $a \equiv a \pmod n$ for every integer $a$.
+ It is symmetric, since $a \equiv b \pmod n$ implies $b \equiv a \pmod n$.
+ It is transitive, since $a \equiv b \pmod n$ and $b \equiv c \pmod n$ together imply $a \equiv c \pmod n$.

## Arithmetic properties

Congruence modulo $n$ behaves well under the standard arithmetic operations, which is what makes modular arithmetic a powerful tool. If $a \equiv b \pmod n$ and $c \equiv d \pmod n$, then the following identities hold:

$$
\begin{align}
a + c &\equiv b + d \pmod n \\[6pt]
a - c &\equiv b - d \pmod n \\[6pt]
a \cdot c &\equiv b \cdot d \pmod n
\end{align}
$$

One can replace any integer by a congruent one before performing addition, subtraction, or multiplication, and the result will still be congruent modulo $n$. The property allows computations with very large numbers to be reduced modulo $n$ at any intermediate step, a trick that is essential in cryptography and in many algorithmic contexts.

Raising to a non-negative integer power is compatible with congruence as well. If $a \equiv b \pmod n$, then $a^k \equiv b^k \pmod n$ for every non-negative integer $k$. The statement follows from the multiplicative identity by [induction](../principle-of-mathematical-induction/) on $k$. Division, on the other hand, is more delicate and does not always behave as expected, since not every nonzero integer has a multiplicative inverse modulo $n$.

> A nonzero element $a$ has a multiplicative inverse modulo $n$ if and only if $\gcd(a, n) = 1$, that is, if $a$ and $n$ are coprime. When such an inverse exists, it is unique modulo $n$.

## Addition and multiplication tables

A useful way to visualise the arithmetic of residues modulo $n$ is to arrange all possible sums or products in a square table. Each row and each column is labelled by a residue, and the entry at their intersection is the result of the operation reduced modulo $n$. For $n = 4$, the addition table is the following:

| + | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 1 | 2 | 3 |
| 1 | 1 | 2 | 3 | 0 |
| 2 | 2 | 3 | 0 | 1 |
| 3 | 3 | 0 | 1 | 2 |

Each row is a cyclic shift of the previous one, which reflects the fact that adding a fixed residue permutes the elements of $\mathbb{Z}/4\mathbb{Z}$ without ever leaving the set. Every row and every column contains each residue exactly once, a feature that holds for the addition table modulo any positive integer.

The multiplication table modulo $4$ is the following:

| × | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 2 | 3 |
| 2 | 0 | 2 | 0 | 2 |
| 3 | 0 | 3 | 2 | 1 |

The behaviour of multiplication is noticeably less regular than that of addition. The row corresponding to $2$ never produces $1$, which means that $2$ does not admit a multiplicative inverse modulo $4$. This is consistent with the fact that $\gcd(2, 4) = 2 \neq 1$. The rows corresponding to $1$ and $3$ do produce $1$ at some point, reflecting the existence of multiplicative inverses for the residues coprime with $4$.

> In group theory, a table of this form is called a Cayley table. It describes a finite [group](../groups/) by listing the result of its operation for every ordered pair of elements. The addition table modulo $n$ is precisely the Cayley table of the cyclic group $(\mathbb{Z}/n\mathbb{Z}, +)$.

## Residue classes

For a fixed modulus $n$, the equivalence relation of congruence [partitions](../sets/) the set of integers into $n$ disjoint subsets, called residue classes or equivalence classes modulo $n$. The residue class of an integer $a$ is the set of all integers congruent to $a$ modulo $n$:

$$
[a]_n = \\{ a + kn : k \in \mathbb{Z} \\}
$$

Two integers belong to the same residue class if and only if they are congruent modulo $n$. The set of all residue classes modulo $n$ is usually denoted $\mathbb{Z}/n\mathbb{Z}$ and contains exactly $n$ elements, represented by the possible remainders $0, 1, 2, \ldots, n-1$.

As a concrete case, take $n = 4$. The integers split into four residue classes:

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

A linear congruence has the form $ax \equiv b \pmod n$, where $a$, $b$, and $n$ are fixed integers with $n > 0$ and $x$ is the unknown. Solving the congruence amounts to determining all integers $x$ that satisfy the relation, considered up to congruence modulo $n$.

The congruence admits a solution if and only if $\gcd(a, n)$ divides $b$. When this condition is met, the set of solutions forms a single residue class modulo $n / \gcd(a, n)$, which corresponds to $\gcd(a, n)$ distinct classes modulo $n$. The criterion is a direct consequence of Bézout's identity, which states that for any pair of integers $a$ and $n$ there exist integers $u$ and $v$ such that:

$$
au + nv = \gcd(a, n)
$$

The special case $b = 1$ leads to the equation $ax \equiv 1 \pmod n$, whose solutions are precisely the multiplicative inverses of $a$ modulo $n$. By the previous criterion such an inverse exists if and only if $\gcd(a, n) = 1$, and in that case it is unique modulo $n$. The inverse can be computed explicitly using the extended Euclidean algorithm, which produces integers $u$ and $v$ satisfying $au + nv = 1$. Reducing this identity modulo $n$ yields $au \equiv 1 \pmod n$, so $u$ is the inverse of $a$ modulo $n$.

As a concrete example, take $a = 7$ and $n = 12$. Since $\gcd(7, 12) = 1$, the inverse exists. The extended Euclidean algorithm produces the identity $7 \cdot 7 + 12 \cdot (-4) = 1$, so $7 \cdot 7 \equiv 1 \pmod{12}$. The inverse of $7$ modulo $12$ is therefore $7$ itself, a coincidence specific to this small example.

## Fermat's little theorem and Euler's theorem

Two classical results describe the behaviour of powers in modular arithmetic and complement the rule $a \equiv b \pmod n \Rightarrow a^k \equiv b^k \pmod n$ with information about the exponent. The first is Fermat's little theorem, which addresses the case of a prime modulus. For a prime $p$ and an integer $a$ not divisible by $p$, the following identity holds:

$$
a^{p-1} \equiv 1 \pmod p
$$

An equivalent formulation, valid for every integer $a$ without restriction, states that $a^p \equiv a \pmod p$. The result provides an efficient way to reduce large exponents modulo $p$ and underlies several classical primality tests.

Euler's theorem generalises the previous statement to an arbitrary modulus $n$. Let $\varphi(n)$ denote the Euler totient, defined as the number of integers in the range $1 \le k \le n$ that are coprime with $n$. If $\gcd(a, n) = 1$, then:

$$
a^{\varphi(n)} \equiv 1 \pmod n
$$

When $n = p$ is prime, every integer in the range $1 \le k \le p - 1$ is coprime with $p$, so $\varphi(p) = p - 1$ and Euler's theorem reduces to Fermat's. The two results form the backbone of public key cryptography, where they justify the correctness of the RSA encryption scheme.

## The Chinese remainder theorem

The Chinese remainder theorem describes the structure of systems of congruences with pairwise coprime moduli. Given integers $n_1, n_2, \ldots, n_k$ that are pairwise coprime, and arbitrary integers $a_1, a_2, \ldots, a_k$, there exists an integer $x$ satisfying simultaneously:

$$
\begin{align}
x &\equiv a_1 \pmod{n_1} \\[6pt]
x &\equiv a_2 \pmod{n_2} \\[6pt]
  &\ \vdots \\[6pt]
x &\equiv a_k \pmod{n_k}
\end{align}
$$

The solution $x$ is unique modulo $N = n_1 n_2 \cdots n_k$. In the language of ring theory the theorem can be reformulated as an isomorphism of [rings](../rings/):

$$
\mathbb{Z}/N\mathbb{Z} \cong \mathbb{Z}/n_1\mathbb{Z} \times \mathbb{Z}/n_2\mathbb{Z} \times \cdots \times \mathbb{Z}/n_k\mathbb{Z}
$$

The result reduces computations modulo a large composite $N$ to parallel computations modulo each of the smaller factors $n_i$, a strategy widely used in computer algebra systems and in cryptographic algorithms.

As a small example, consider the system $x \equiv 2 \pmod 3$ and $x \equiv 3 \pmod 5$. The integers satisfying the first congruence are $2, 5, 8, 11, 14, \ldots$, and among these the value $x = 8$ also satisfies $8 \equiv 3 \pmod 5$. The complete set of solutions is the residue class $[8]_{15} = \\{ \ldots, -7, 8, 23, 38, \ldots \\}$.

## Examples

Consider the problem of determining the day of the week a given number of days from today. If today is Wednesday and we want to know what day it will be in $100$ days, it is enough to compute $100 \bmod 7$. Since $100 = 14 \cdot 7 + 2$, the remainder is $2$, so the answer is two days after Wednesday, that is, Friday. The modulo operator captures the cyclical structure of the week.

A second classical example is the parity of an integer. An integer $a$ is even if $a \bmod 2 = 0$ and odd if $a \bmod 2 = 1$. The two residue classes modulo $2$ correspond exactly to the even and odd integers, and the familiar rules of parity, such as "even plus even is even" or "odd times odd is odd", are special cases of the arithmetic properties of congruences.

A slightly less trivial example uses modular arithmetic to compute the last digit of a large power. The last digit of $7^{100}$ in base $10$ is simply $7^{100} \bmod 10$. Computing successive powers of $7$ modulo $10$ yields $7, 9, 3, 1, 7, 9, 3, 1, \ldots$, a cycle of length $4$. 

Since $100 \bmod 4 = 0$, the exponent falls at the end of a full cycle, so $7^{100} \equiv 1 \pmod{10}$. The last digit of $7^{100}$ is therefore $1$. The same conclusion follows from Euler's theorem, since $\varphi(10) = 4$ and $\gcd(7, 10) = 1$ imply $7^{4} \equiv 1 \pmod{10}$, from which $7^{100} = (7^{4})^{25} \equiv 1 \pmod{10}$.

## Relation with algebraic structures

The residue classes modulo $n$ can be added and multiplied in a way that is compatible with the arithmetic of the integers. Defining:

$$
[a]_n + [b]_n = [a+b]_n \qquad [a]_n \cdot [b]_n = [a \cdot b]_n
$$

yields two well-defined operations on $\mathbb{Z}/n\mathbb{Z}$, thanks to the compatibility of congruence with addition and multiplication. Under these operations $\mathbb{Z}/n\mathbb{Z}$ becomes a finite commutative [ring](../rings/), and when $n$ is prime it becomes a [field](../fields/), because every nonzero residue is then coprime with $n$ and therefore invertible.The modulo operator is not only a computational device but also the arithmetic foundation on which an entire family of finite algebraic structures is built. 

An analogous construction starts from a polynomial ring and a fixed polynomial, in which case the quotient is obtained through [polynomial division](../polynomial-division/) and produces important examples of fields, such as $\mathbb{R}[x]/(x^2 + 1) \cong \mathbb{C}$.
