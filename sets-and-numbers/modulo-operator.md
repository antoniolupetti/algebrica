
# Modulo Operator

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/modulo-operator/

## Definition

The modulo operator is one of the most frequently used operations in [integer](../integers/) arithmetic. Given two integers, it returns the remainder left over after dividing the first by the second. This operator plays a central role in number theory, computer science, and the construction of several algebraic structures. In formal terms, fiven two integers \\(a\\) and \\(n\\) with \\(n > 0\\), the modulo operator is defined as follows:

\\[
a \bmod n = r
\\]

\\(r\\) is the unique integer satisfying \\(0 \le r < n\\) and \\(a = qn + r\\) for some integer \\(q\\). The integer \\(q\\) is the quotient of the division of \\(a\\) by \\(n\\), and \\(r\\) is the remainder. The existence and uniqueness of this decomposition is guaranteed by the division algorithm for integers. The number \\(n\\) is called the modulus. When \\(a\\) is positive, the value of \\(a \bmod n\\) coincides with the intuitive notion of the remainder learned in elementary arithmetic. For example, \\(17 \bmod 5 = 2\\), since \\(17 = 3 \cdot 5 + 2\\). The quotient is \\(3\\) and the remainder is \\(2\\).

> The modulo operator is sometimes written as \\(a \\, \mathrm{mod} \\, n\\) in textbooks and as "a % n" in many programming languages, although the behaviour for negative operands may differ between the mathematical definition and specific programming implementations.

- - -
## Modulo of a negative integer

A subtle point arises when \\(a\\) is negative. The mathematical definition requires the remainder to satisfy \\(0 \le r < n\\), so the result is always a non-negative integer strictly smaller than the modulus. Consider \\(-7 \bmod 5\\). Writing \\(-7 = q \cdot 5 + r\\) with \\(0 \le r < 5\\), one finds \\(q = -2\\) and \\(r = 3\\), since \\(-7 = (-2) \cdot 5 + 3\\). Therefore \\(-7 \bmod 5 = 3\\), not \\(-2\\) as one might naively expect.

This convention is not universal. In several programming languages the `%` operator follows the sign of the dividend, so that `-7 % 5` returns \\(-2\\) rather than \\(3\\). In a purely mathematical context, however, the remainder is always taken to be non-negative.

- - -
## Congruence modulo n

Closely related to the modulo operator is the notion of congruence. Two integers \\(a\\) and \\(b\\) are said to be congruent modulo \\(n\\) if they leave the same remainder when divided by \\(n\\), or equivalently if their difference is a multiple of \\(n\\). This relation is written as follows:

\\[
a \equiv b \pmod{n}
\\]

The equivalent characterisation in terms of divisibility states that \\(a \equiv b \pmod{n}\\) if and only if \\(n \mid (a - b)\\). For example, \\(17 \equiv 2 \pmod 5\\) because \\(17 - 2 = 15\\) is divisible by \\(5\\), and equivalently because both \\(17\\) and \\(2\\) leave remainder \\(2\\) when divided by \\(5\\).

It is important to distinguish the operator \\(a \bmod n\\), which produces a specific integer, from the congruence \\(a \equiv b \pmod n\\), which is a relation between two integers. The first is a function of \\(a\\) and \\(n\\); the second is a statement that can be true or false depending on the integers involved. Congruence modulo \\(n\\) is an equivalence relation on the integers. 

+ It is reflexive, since \\(a \equiv a \pmod n\\) for every integer \\(a\\).
+ It is symmetric, since \\(a \equiv b \pmod n\\) implies \\(b \equiv a \pmod n\\).
+ It is transitive, since \\(a \equiv b \pmod n\\) and \\(b \equiv c \pmod n\\) together imply \\(a \equiv c \pmod n\\).
- - -
## Arithmetic properties

Congruence modulo \\(n\\) behaves well under the standard arithmetic operations, which is precisely what makes modular arithmetic a powerful tool. If \\(a \equiv b \pmod n\\) and \\(c \equiv d \pmod n\\), then the following identities hold:

\\[
\begin{align}
a + c &\equiv b + d \pmod n \\\\[6pt]
a - c &\equiv b - d \pmod n \\\\[6pt]
a \cdot c &\equiv b \cdot d \pmod n
\end{align}
\\]

In other words, one can replace any integer by a congruent one before performing addition, subtraction, or multiplication, and the result will still be congruent modulo \\(n\\). This property is what allows computations with very large numbers to be reduced modulo \\(n\\) at any intermediate step, a trick that is essential in cryptography and in many algorithmic contexts.

Raising to an integer power is compatible with congruence as well. If \\(a \equiv b \pmod n\\), then \\(a^k \equiv b^k \pmod n\\) for every non-negative integer \\(k\\). Division, on the other hand, is more delicate and does not always behave as expected, since not every nonzero integer has a multiplicative inverse modulo \\(n\\).

> A nonzero element \\(a\\) has a multiplicative inverse modulo \\(n\\) if and only if \\(\gcd(a, n) = 1\\), that is, if \\(a\\) and \\(n\\) are coprime. When such an inverse exists, it is unique modulo \\(n\\).

- - -
## Addition and multiplication tables

A useful way to visualise the arithmetic of residues modulo \\(n\\) is to arrange all possible sums or products in a square table. Each row and each column is labelled by a residue, and the entry at their intersection is the result of the operation reduced modulo \\(n\\). For \\(n = 4\\), the addition table is the following:

| + | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 1 | 2 | 3 |
| 1 | 1 | 2 | 3 | 0 |
| 2 | 2 | 3 | 0 | 1 |
| 3 | 3 | 0 | 1 | 2 |

Each row is a cyclic shift of the previous one, which reflects the fact that adding a fixed residue permutes the elements of \\(\mathbb{Z}/4\mathbb{Z}\\) without ever leaving the set. Every row and every column contains each residue exactly once, a feature that holds for the addition table modulo any positive integer.

The multiplication table modulo \\(4\\) is the following:

| × | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 2 | 3 |
| 2 | 0 | 2 | 0 | 2 |
| 3 | 0 | 3 | 2 | 1 |

The behaviour of multiplication is noticeably less regular than that of addition. The row corresponding to \\(2\\) never produces \\(1\\), which means that \\(2\\) does not admit a multiplicative inverse modulo \\(4\\). This is consistent with the fact that \\(\gcd(2, 4) = 2 \neq 1\\). On the other hand, the rows corresponding to \\(1\\) and \\(3\\) do produce \\(1\\) at some point, reflecting the existence of multiplicative inverses for the residues coprime with \\(4\\).

> In group theory, a table of this form is called a Cayley table. It describes a finite group by listing the result of its operation for every ordered pair of elements. The addition table modulo \\(n\\) is precisely the Cayley table of the group \\((\mathbb{Z}/n\mathbb{Z}, +)\\).

- - -
## Residue classes

For a fixed modulus \\(n\\), the equivalence relation of congruence partitions the set of integers into \\(n\\) disjoint subsets, called residue classes or equivalence classes modulo \\(n\\). The residue class of an integer \\(a\\) is the set of all integers congruent to \\(a\\) modulo \\(n\\):

\\[
[a]_n = \\{ a + kn : k \in \mathbb{Z} \\}
\\]

Two integers belong to the same residue class if and only if they are congruent modulo \\(n\\). The set of all residue classes modulo \\(n\\) is usually denoted \\(\mathbb{Z}/n\mathbb{Z}\\) and contains exactly \\(n\\) elements, represented by the possible remainders \\(0, 1, 2, \ldots, n-1\\).

As a concrete case, take \\(n = 4\\). The integers split into four residue classes:

\\[
\begin{align}
[0]_4 &= \\{ \ldots, -8, -4, 0, 4, 8, \ldots \\} \\\\[6pt]
[1]_4 &= \\{ \ldots, -7, -3, 1, 5, 9, \ldots \\} \\\\[6pt]
[2]_4 &= \\{ \ldots, -6, -2, 2, 6, 10, \ldots \\} \\\\[6pt]
[3]_4 &= \\{ \ldots, -5, -1, 3, 7, 11, \ldots \\}
\end{align}
\\]

Every integer belongs to exactly one of these four classes, and the union of the four classes is all of \\(\mathbb{Z}\\).

- - -
## Examples

Consider the problem of determining the day of the week a given number of days from today. If today is Wednesday and one wants to know what day it will be in \\(100\\) days, it is enough to compute \\(100 \bmod 7\\). Since \\(100 = 14 \cdot 7 + 2\\), the remainder is \\(2\\), so the answer is two days after Wednesday, that is, Friday. The modulo operator captures precisely the cyclical structure of the week.

A second classical example is the parity of an integer. An integer \\(a\\) is even if \\(a \bmod 2 = 0\\) and odd if \\(a \bmod 2 = 1\\). The two residue classes modulo \\(2\\) correspond exactly to the even and odd integers, and the familiar rules of parity, such as "even plus even is even" or "odd times odd is odd", are special cases of the arithmetic properties of congruences.

As a slightly less trivial example, one can use modular arithmetic to compute the last digit of a large power. The last digit of \\(7^{100}\\) in base \\(10\\) is simply \\(7^{100} \bmod 10\\). Computing successive powers of \\(7\\) modulo \\(10\\) yields \\(7, 9, 3, 1, 7, 9, 3, 1, \ldots\\), a cycle of length \\(4\\). Since \\(100 \bmod 4 = 0\\), the exponent falls at the end of a full cycle, so \\(7^{100} \equiv 1 \pmod{10}\\). The last digit of \\(7^{100}\\) is therefore \\(1\\).

- - -
## Relation with algebraic structures

The residue classes modulo \\(n\\) can be added and multiplied in a way that is compatible with the arithmetic of the integers. Defining:

\\[
[a]_n + [b]_n = [a+b]_n \qquad [a]_n \cdot [b]_n = [a \cdot b]_n
\\]

yields two well-defined operations on \\(\mathbb{Z}/n\mathbb{Z}\\), thanks to the compatibility of congruence with addition and multiplication. Under these operations \\(\mathbb{Z}/n\mathbb{Z}\\) becomes a finite commutative ring, and when \\(n\\) is prime it becomes a field. The modulo operator is therefore not only a computational device but also the arithmetic foundation on which an entire family of finite algebraic structures is built.
