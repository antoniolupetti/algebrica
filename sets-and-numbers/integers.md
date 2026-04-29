# Integers

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/integers/

## Definition

Among the different [types of numbers](../types-of-numbers/), the integers emerge when we extend the [natural numbers](../natural-numbers) to include the additive opposites of every positive quantity. In this enlarged system we find all whole quantities, both positive and negative, together with zero. The [set](../sets/) is denoted by \\(\mathbb{Z}\\). Symbolically we write:
\\[
\mathbb{Z} = \{\ldots,-3,-2,-1,0,1,2,3,\ldots\}
\\]
an infinite collection of evenly spaced points along the number [line](../lines). 

A rigorous construction models each integer as a class of ordered pairs of natural numbers. Take pairs \\((a,b)\\) with \\(a,b \in \mathbb{N}\\) and say that two pairs belong to the same class whenever:
\\[
(a,b) \sim (c,d) \quad \longleftrightarrow \quad a + d = b + c
\\]

The pair \\((a,b)\\) represents the net difference between \\(a\\) and \\(b\\):  
- Pairs with equal components form the class corresponding to \\(0\\).
- Pairs where the first component dominates form the positive integers.  
- Pairs where the second dominates form the negative ones.

For example, consider the pair of natural numbers \\((2,5).\\) In the construction that builds the integers from ordered pairs, this element represents the net amount obtained by comparing its two components. Since the second entry is larger than the first, the pair corresponds to a negative integer:
\\[
2 - 5 = -3
\\]

This interpretation is justified by the fact that two pairs represent the same integer exactly when they fall into the same equivalence class, which occurs whenever:
\\[
(a,b) \sim (c,d) \quad \longleftrightarrow \quad a + d = b + c
\\]

For instance, the pair \\((4,7)\\) lies in the same class as \\((2,5)\\), because:
\\[
4 + 5 = 9 \qquad \text{and} \qquad 7 + 2 = 9
\\]

Although the components differ, both pairs encode the same overall difference, the integer \\(-3.\\)

- - -
## The Integers as an algebraic ring

When we say that the integers form a [ring](../rings/), we mean that the set \\(\mathbb{Z}\\) comes equipped with two operations, addition and multiplication, that interact in a structured and predictable way. This structure ensures that arithmetic with integers behaves consistently, no matter how large or small the numbers involved may be.

The ring axioms for \\((\mathbb{Z}, +, \cdot)\\) are the following. For all \\(a, b, c \in \mathbb{Z}\\):

+ Closure: the sum and product of any two integers are again integers: \\(a + b \in \mathbb{Z}\\) and \\(ab \in \mathbb{Z}.\\)
+ Associativity: both operations are associative: \\(a + (b+c) = (a+b) + c\\) and \\(a(bc) = (ab)c.\\)
+ Identity elements: there exist neutral elements for both operations: \\(a + 0 = a\\) and \\(a \cdot 1 = a.\\)
+ Additive inverses: every integer has an opposite: \\(a + (-a) = 0.\\)
+ Commutativity of addition: the order of summands does not affect the result: \\(a + b = b + a.\\)
+ Distributivity: multiplication distributes over addition: \\(a(b+c) = ab + ac.\\)

Multiplication in \\(\mathbb{Z}\\) is also commutative, that is, \\(ab = ba\\) for all \\(a, b \in \mathbb{Z}\\), which makes \\((\mathbb{Z}, +, \cdot)\\) a commutative ring. Note that integers do not possess multiplicative inverses in general: the only integers \\(a\\) for which \\(a^{-1} \in \mathbb{Z}\\) are \\(a = 1\\) and \\(a = -1\\), which is why \\(\mathbb{Z}\\) is a ring but not a field.

> A field extends the ring structure by requiring that every non-zero element also has a multiplicative inverse. The rational numbers \\(\mathbb{Q}\\) and the real numbers \\(\mathbb{R}\\) are standard examples; the integers are not, since \\(2^{-1} \notin \mathbb{Z}\\).

- - -
## Fundamental properties of the integers

Compatibility with equality: whenever two integers satisfy \\(a = b\\), any operation applied to both sides preserves that equality. In particular:
\\[a + c = b + c \\] 
\\[ac = bc\\]

- - -

Commutative laws: the order of the operands does not affect the result:
\\[a\ + b = b + a \\] 
\\[ab = ba\\]

- - -

Associative laws: grouping the terms does not change the outcome:
\\[a + (b + c) = (a + b) + c \\]
\\[a(bc) = (ab)c \\]

- - - 

Distributive law: multiplication distributes over addition:
   \\[
   a(b + c) = ab + ac
   \\]

- - -

The integers also include neutral elements for the two operations: adding zero leaves any integer unchanged, and multiplying by one preserves its value:
\\[
a + 0 = a \qquad a \cdot 1 = a
\\]

- - -
## Integers in base 10

Integers are typically written using the decimal system, that is, base 10. Each digit in a number carries a positional weight determined by a corresponding power of ten. By combining these weighted digits, we can reconstruct the entire value of the integer. Consider for example the number \\(235.\\) Using the positional principle, we can express the number as a sum of powers of ten:
\\[
235 = 2 \times 10^{2} + 3 \times 10^{1} + 5 \times 10^{0}
\\]

This decomposition shows exactly how each digit contributes to the final value. The following table summarises the structure of the number:

| Digit | Place value | Contribution |
|-------|-------------|--------------|
| 2     | \\(10^{2}\\) (hundreds) | \\(2 \times 10^{2} = 200\\) |
| 3     | \\(10^{1}\\) (tens)     | \\(3 \times 10^{1} = 30\\)  |
| 5     | \\(10^{0}\\) (units)    | \\(5 \times 10^{0} = 5\\)   |

Adding these contributions together recovers the integer:
\\[
235 = 200 + 30 + 5
\\]

> The same mechanism applies to any integer written in decimal notation. Each digit acts as a coefficient multiplying a specific power of ten, and the integer itself is obtained by summing all these positional contributions.

- - -
## The binary system

Although integers are commonly written in base 10, other numeral systems are equally valid and sometimes more convenient. An especially important alternative is base 2, or the binary system, which uses only the digits \\(0\\) and \\(1\\). This representation is fundamental in computer science and digital electronics, where information is stored and processed using two-state devices. In base 2, each position corresponds to a power of two rather than a power of ten. Any integer can be rewritten in binary by expanding it as a sum of weighted powers of two. For example, consider the integer:
\\[
53
\\]
To convert it to binary, we repeatedly divide by \\(2\\) and record the remainders. Reading the remainders from bottom to top yields the binary expansion.

| Division by 2 | Quotient | Remainder |
|--------------:|:--------:|:---------:|
| \\(53 \div 2\\) | \\(26\\)       | \\(1\\)         |
| \\(26 \div 2\\) | \\(13\\)       | \\(0\\)         |
| \\(13 \div 2\\) | \\(6\\)        | \\(1\\)         |
| \\(6 \div 2\\)  | \\(3\\)        | \\(0\\)         |
| \\(3 \div 2\\)  | \\(1\\)        | \\(1\\)         |
| \\(1 \div 2\\)  | \\(0\\)        | \\(1\\)         |

Reading the remainders upward gives the binary representation \\(53 = 110101.\\) We can check the conversion by expanding the binary digits in powers of two:

| Binary digit | Power of two      | Contribution              |
|--------------|-------------------|---------------------------|
| \\(1\\)            | \\(2^{5}\\)         | \\(1 \times 2^{5} = 32\\)   |
| \\(1\\)            | \\(2^{4}\\)         | \\(1 \times 2^{4} = 16\\)   |
| \\(0\\)            | \\(2^{3}\\)         | \\(0 \times 2^{3} = 0\\)    |
| \\(1\\)            | \\(2^{2}\\)         | \\(1 \times 2^{2} = 4\\)    |
| \\(0\\)            | \\(2^{1}\\)         | \\(0 \times 2^{1} = 0\\)    |
| \\(1\\)            | \\(2^{0}\\)         | \\(1 \times 2^{0} = 1\\)    |


The sum of the contributions confirms the conversion:
\\[
32 + 16 + 0 + 4 + 0 + 1 = 53
\\]

- - -
## The modulo operator

Modular arithmetic describes how integers behave when we are interested only in their remainders after division by a fixed integer \\(n\\). Within \\(\mathbb{Z}\\), two integers are said to be equivalent [modulo](../modulo-operator/) \\(n\\) when they differ by a multiple of \\(n\\). For example, in arithmetic modulo \\(12\\), the integers \\(14\\) and \\(2\\) represent the same residue class because \\(14 - 2 = 12\\). Addition and multiplication are carried out as usual, but the final result is replaced by its remainder upon division by \\(n\\). For example:

\\[7 + 9 \equiv 4 \pmod{12}\\] 
\\[ 5 \times 7 \equiv 11 \pmod{12}\\]

> In the case of \\(5 \times 7\\), the product is \\(35 = 24 + 11\\); since \\(24\\) is a multiple of \\(12\\), the value of the product modulo \\(12\\) is the remainder \\(11\\).

- - -

This kind of arithmetic is widely used beyond pure mathematics. In computer science, the modulo operator is essential for extracting remainders, generating cyclic patterns, and keeping values within a bounded range. A familiar example involves the months of the year: adding \\(n\\) months is naturally handled modulo \\(12\\), since month counts wrap around after December.

In many programming languages, including Java, the modulo operator is written as **%**. The following example computes the month occurring three months after October:

````
int month = 10; // October
int result = (month + 3) % 12;  
System.out.println(result);  // Output: 1  (January)
// Using modulo 12, the expression (month + 3) does not yield 13.
// Instead, 13 is reduced to its remainder when divided by 12, which is 1.
````

- - -
## Integers and the role of induction

In mathematics, several structural properties of the integers depend on the recursive nature of the natural numbers. The naturals form the foundation from which the integers are constructed, and many statements about \\( \mathbb{Z} \\) can be traced back to properties first established on \\( \mathbb{N} \\). The mechanism that allows these stepwise constructions and proofs is the [Principle of Mathematical Induction](../principle-of-mathematical-induction/).

Starting from the formal definition of an inductive set, let us consider a set \\( A \subseteq \mathbb{N} \\) defined by a property \\( p(n) \\), such that \\(A = \lbrace n \in \mathbb{N} \mid p(n) \rbrace\\). Suppose the following conditions hold:

+ \\( p(0) \\) is true, that is, \\( 0 \in A. \\)
+ \\( p(n) \rightarrow p(n+1) \\,\forall \\ n \in \mathbb{N}.\\) If \\( n \in A \\), then \\( n+1 \in A.\\)

Thus, \\( p(n) \\) is true for every \\( n \in \mathbb{N}.\\) A concrete illustration shows how this carries over to the integers. Consider the claim that the sum of the first \\( n \\) positive integers equals:

\\[ \frac{n(n+1)}{2} \\]

The base case \\( n = 1 \\) is immediate: both sides equal \\( 1 \\). For the inductive step, assuming the identity holds for some \\( n \\), one adds \\( n+1 \\) to both sides and verifies that the result matches the formula evaluated at \\( n+1 \\). Since the natural numbers embed into \\( \mathbb{Z} \\) as the non-negative integers, this identity holds in \\(\mathbb{Z}\\) as well, and the same method extends to any statement about \\(\mathbb{Z}\\) that can be reduced to a property of \\(\mathbb{N}\\) through the construction of the integers from ordered pairs of naturals.