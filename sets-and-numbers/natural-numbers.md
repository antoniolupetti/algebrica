# Natural Numbers

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/natural-numbers/

## Introduction

The natural numbers arise from the act of counting, but a modern treatment demands an axiomatic foundation that makes their properties explicit and independent from any informal notion. This page develops the natural numbers from two complementary perspectives: an axiomatic one, based on the Peano axioms, and an algebraic one, focused on the operations defined on them and on the structure they give rise to.

We denote the set of natural numbers by \\(\\mathbb{N}\\), and throughout this page we adopt the convention that \\(0 \\in \\mathbb{N}\\), consistent with the modern formulation of the Peano axioms and with the treatment of the [principle of mathematical induction](../principle-of-mathematical-induction/) already developed on this site.

- - -

A useful way to visualise the natural numbers is to place them on the real line, alongside the other [numerical systems](../types-of-numbers/) that extend them. The real [line](../lines/) provides a geometric representation of every number, and the natural numbers appear within it as a distinguished discrete subset.

Starting from \\(0\\), the natural numbers occupy equally spaced positions to the right, corresponding to \\(0, 1, 2, 3, \\dots\\), and extending indefinitely in that direction. They form an unbounded, discrete sequence of points, with no natural number lying strictly between two consecutive ones. This discreteness sets them apart from the rational and irrational numbers, which are densely distributed along the line and fill the gaps between the integer positions.

To the left of \\(0\\), the line continues with the negative integers \\(-1, -2, -3, \\dots\\), which do not belong to \\(\\mathbb{N}\\) and are introduced only when the set is extended to the integers \\(\\mathbb{Z}\\). Between any two consecutive integers one finds infinitely many rational numbers, such as \\(1/3\\), and infinitely many irrational numbers, such as \\(-\\sqrt{3}\\) or \\(\\pi\\), which require the further extensions to \\(\\mathbb{Q}\\) and \\(\\mathbb{R}\\). In this picture the natural numbers are the most elementary layer, from which all the other numerical systems are progressively built.

- - -
## The Peano axioms

The axiomatic approach characterises \\(\\mathbb{N}\\)as a set that satisfies a minimal list of properties, from which every other fact about natural numbers can be derived. The Peano axioms describe a set \\(\\mathbb{N}\\) together with a distinguished element \\(0\\) and a function \\(S : \\mathbb{N} \\to \\mathbb{N}\\), called the successor [function](../functions/), subject to the following conditions:

\\[
\\begin{align}
&\\text{(P1)} \\quad 0 \\in \\mathbb{N} \\\\[6pt]
&\\text{(P2)} \\quad \\forall \\, n \\in \\mathbb{N}, \\ S(n) \\in \\mathbb{N} \\\\[6pt]
&\\text{(P3)} \\quad \\forall \\, n \\in \\mathbb{N}, \\ S(n) \\neq 0\\\\[6pt]
&\\text{(P4)} \\quad \\forall \\, m, n \\in \\mathbb{N}, \\ S(m) = S(n) \\implies m = n\\\\[6pt]
&\\text{(P5)} \\quad \\text{induction axiom}
\\end{align}
\\]

+ The first axiom ensures the existence of an initial element, which acts as the starting point of the construction. 
+ The second states that the successor operation never leaves the set, so that every natural number has a natural number as its successor. 
+ The third excludes the possibility that \\(0\\) is itself the successor of some element, which guarantees that the sequence does not close into a cycle. 
+ The fourth axiom, often called the injectivity of the successor, ensures that distinct natural numbers have distinct successors, so that applying \\(S\\) repeatedly generates genuinely new elements at each step.

The fifth axiom, the [principle of induction](../principle-of-mathematical-induction/), asserts that any subset of \\(\\mathbb{N}\\) containing \\(0\\) and closed under the successor function must coincide with \\(\\mathbb{N}\\) itself. This is the axiom that fixes \\(\\mathbb{N}\\) as the smallest structure satisfying the previous four, and it is the conceptual engine behind every proof by induction. A detailed treatment is given in the page on the [principle of mathematical induction](../principle-of-mathematical-induction/).

- - -
## Set-theoretic construction

The Peano axioms characterise \\(\\mathbb{N}\\) up to isomorphism, but they do not exhibit an explicit model. A concrete realisation was proposed by John von Neumann within the framework of set theory, and it is by now the standard reference construction. In this construction the natural number \\(0\\) is identified with the empty set, and the successor of a natural number is defined as the union of that number with the singleton containing it. The definitions are the following:

\\[
\\begin{align}
&0 = \\varnothing \\\\[6pt]
&S(n) = n \\cup \\{n\\}
\\end{align}
\\]

Applying the successor function repeatedly produces an explicit sequence of sets that realises the natural numbers. The first few elements are as follows:

\\[
\\begin{align}
&1 = \\{0\\} = \\{\\varnothing\\} \\\\[6pt]
&2 = \\{0, 1\\} = \\{\\varnothing, \\{\\varnothing\\}\\} \\\\[6pt]
&3 = \\{0, 1, 2\\}
\\end{align}
\\]

A notable feature of this construction is that each natural number coincides with the set of all its predecessors, so that the number \\(n\\) has exactly \\(n\\) elements. This provides a direct and elegant link between the ordinal and the cardinal aspects of \\(\\mathbb{N}\\).

- - -
## Addition and multiplication

Once the successor function is available, the two fundamental arithmetic operations can be introduced by recursion. The idea is to define each operation by specifying its value in a base case and then extending it to all natural numbers by appealing to the successor.

Addition is defined, for every \\(m \\in \\mathbb{N}\\), by the recursive clauses:

\\[
\\begin{align}
&m + 0 = m \\\\[6pt]
&m + S(n) = S(m + n)
\\end{align}
\\]

The first clause specifies that adding zero leaves the number unchanged, while the second reduces the addition of a successor to the successor of an addition, thereby propagating the definition to all natural numbers.

- - -

Multiplication is defined in a similar way, for every \\(m \\in \\mathbb{N}\\), by the clauses:

\\[
\\begin{align}
&m \\cdot 0 = 0 \\\\[6pt]
&m \\cdot S(n) = m \\cdot n + m
\\end{align}
\\]

Multiplication is therefore constructed on top of addition, according to the idea that multiplying by a successor corresponds to adding one further copy of the multiplicand.

- - -
## Properties of the operations

From the recursive definitions, together with the induction axiom, one can prove that addition and multiplication satisfy the expected algebraic properties. The proofs proceed by induction on one of the arguments, and they are a standard exercise in arithmetic.

+ Addition is associative and commutative, and admits \\(0\\) as neutral element. 
+ Multiplication is associative and commutative, admits \\(1\\) as neutral element, and distributes over addition. 

These properties are summarised as follows:

\\[
\\begin{align}
&(a + b) + c = a + (b + c) \\\\[6pt]
&a + b = b + a \\\\[6pt]
&a + 0 = a, \\\\[6pt]
&(a \\cdot b) \\cdot c = a \\cdot (b \\cdot c) \\\\[6pt]
&a \\cdot b = b \\cdot a \\\\[6pt]
&a \\cdot 1 = a \\\\[6pt]
&a \\cdot (b + c) = a \\cdot b + a \\cdot c
\\end{align}
\\]

A further property, which distinguishes \\(\\mathbb{N}\\) from more general algebraic structures, is the absence of zero divisors. If the product of two natural numbers equals zero, then at least one of the two factors must be zero.

- - -
## Order and well-ordering

The set \\(\\mathbb{N}\\) is equipped with a total order, which can be defined directly in terms of addition. Given two natural numbers \\(m\\) and \\(n\\), the relation \\(m \\leq n\\) holds if and only if there exists a natural number \\(k\\) such that the following equality is satisfied:

\\[
n = m + k.
\\]

In this definition the element \\(k\\) measures the gap between \\(m\\) and \\(n\\), and its existence corresponds to the intuitive idea that \\(n\\) can be reached from \\(m\\) by a finite number of successor steps. The relation so defined is reflexive, antisymmetric, transitive, and total, so that any two natural numbers are comparable.

A distinctive feature of this order is the well-ordering property. Every non-empty subset of \\(\\mathbb{N}\\) admits a least element with respect to \\(\\leq\\). It is logically equivalent to the principle of induction, in the sense that each can be derived from the other within a suitable axiomatic framework, and it provides an alternative foundation for the same body of results.

- - -
## Example

As an illustration of how the recursive definitions interact with the algebraic properties, we compute the sum \\(2 + 3\\) directly from the definition of addition. The computation relies exclusively on the recursive clauses and on the fact that \\(3 = S(S(S(0)))\\). We start from the outer successor and apply the recursive clause for addition at each step:

\\[
\\begin{align}
2 + 3 &= 2 + S(S(S(0))) \\\\[6pt]
&= S(2 + S(S(0))) \\\\[6pt]
&= S(S(2 + S(0))) \\\\[6pt]
&= S(S(S(2 + 0))) \\\\[6pt]
&= S(S(S(2)))
\\end{align}
\\]

Since \\(S(S(S(2)))\\) is, by definition, the natural number obtained from \\(2\\) by applying the successor function three times, the final value coincides with the natural number \\(5\\).

The result of the computation is \\(2 + 3 = 5\\).