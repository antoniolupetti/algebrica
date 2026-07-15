---
title: Natural Numbers
source: https://algebrica.org/natural-numbers/
license: CC BY-NC 4.0
tags:
  - addition
  - induction
  - multiplication
  - natural-numbers
  - peano-axioms
  - real-line
  - successor-function
  - von-neumann-construction
  - well-ordering
---

## Introduction

The natural numbers arise from the act of counting, but a modern treatment requires an axiomatic foundation that makes their properties explicit and independent from any informal notion. This page develops the natural numbers from two perspectives: an axiomatic one, based on the Peano axioms, and an algebraic one, focused on the operations defined on them and on the structure they give rise to.

We denote the [set](../sets/) of natural numbers by $\mathbb{N}$, and throughout this page we adopt the convention that $0 \in \mathbb{N}$, consistent with the modern formulation of the Peano axioms and with the treatment of the [principle of mathematical induction](../principle-of-mathematical-induction/) already developed on this site.

- - -

The natural numbers can be visualised on the real line, alongside the other numerical systems described in [types of numbers](../types-of-numbers/). The real line represents every number as a point, and the natural numbers appear within it as a discrete subset.

Starting from $0$, the natural numbers occupy equally spaced positions to the right, corresponding to $0, 1, 2, 3, \dots$, and extending indefinitely in that direction. They are an unbounded, discrete sequence of points, with no natural number lying strictly between two consecutive ones. This discreteness distinguishes them from the [rational](../rational-numbers/) and [irrational](../irrational-numbers/) numbers, which are densely distributed along the line and fill the gaps between the integer positions.

To the left of $0$, the line continues with the negative [integers](../integers/) $-1, -2, -3, \dots$, which do not belong to $\mathbb{N}$ and are introduced only when the set is extended to $\mathbb{Z}$. Between any two consecutive integers one finds infinitely many [rational numbers](../rational-numbers/), such as $1/3$, and infinitely many [irrational numbers](../irrational-numbers/), such as $-\sqrt{3}$ or $\pi$, which require the further extensions to $\mathbb{Q}$ and to the [real numbers](../real-numbers/) $\mathbb{R}$. In this picture the natural numbers are the most elementary layer, from which all the other numerical systems are built.

## The Peano axioms

The axiomatic approach characterises $\mathbb{N}$ as a set that satisfies a minimal list of properties, from which every other fact about natural numbers can be derived. The Peano axioms describe a set $\mathbb{N}$ together with a distinguished element $0$ and a function $S : \mathbb{N} \to \mathbb{N}$, called the successor function, subject to the following conditions:

$$
\begin{align}
&\text{(P1)} \quad 0 \in \mathbb{N} \\[6pt]
&\text{(P2)} \quad \forall \ n \in \mathbb{N}, \ S(n) \in \mathbb{N} \\[6pt]
&\text{(P3)} \quad \forall \ n \in \mathbb{N}, \ S(n) \neq 0 \\[6pt]
&\text{(P4)} \quad \forall \ m, n \in \mathbb{N}, \ S(m) = S(n) \implies m = n \\[6pt]
&\text{(P5)} \quad \text{induction axiom}
\end{align}
$$

+ The first axiom ensures that the set has an initial element, the starting point of the construction.
+ The second states that the successor operation never leaves the set, so that every natural number has a natural number as its successor.
+ The third states that $0$ is not the successor of any element, which guarantees that the sequence does not close into a cycle.
+ The fourth axiom, often called the injectivity of the successor, ensures that distinct natural numbers have distinct successors, so that repeated application of $S$ produces a new element at each step.

The fifth axiom, the [principle of induction](../principle-of-mathematical-induction/), asserts that any subset of $\mathbb{N}$ containing $0$ and closed under the successor function must coincide with $\mathbb{N}$ itself. The axiom fixes $\mathbb{N}$ as the smallest structure satisfying the previous four, and it is the basis of every proof by induction.

## Set-theoretic construction

The Peano axioms characterise $\mathbb{N}$ up to isomorphism, but they do not exhibit an explicit model. A concrete realisation was proposed by John von Neumann within set theory, and it is by now the standard construction. In this construction the natural number $0$ is identified with the empty set, and the successor of a natural number is defined as the union of that number with the singleton containing it:

$$
\begin{align}
&0 = \varnothing \\[6pt]
&S(n) = n \cup \{n\}
\end{align}
$$

Applying the successor function repeatedly produces an explicit sequence of sets that realises the natural numbers. The first few elements are as follows:

$$
\begin{align}
&1 = \{0\} = \{\varnothing\} \\[6pt]
&2 = \{0, 1\} = \{\varnothing, \{\varnothing\}\} \\[6pt]
&3 = \{0, 1, 2\}
\end{align}
$$

In this construction each natural number coincides with the set of all its predecessors, so the number $n$ has exactly $n$ elements. This connects the ordinal and the cardinal aspects of $\mathbb{N}$ directly.

## Arithmetic operations

Once the successor function is available, the arithmetic operations can be introduced by recursion. The idea is to define each operation by specifying its value in a base case and then extending it to all natural numbers by appealing to the successor.

Addition is defined, for every $m \in \mathbb{N}$, by the recursive clauses:

$$
\begin{align}
&m + 0 = m \\[6pt]
&m + S(n) = S(m + n)
\end{align}
$$

The first clause specifies that adding zero leaves the number unchanged, while the second reduces the addition of a successor to the successor of an addition and propagates the definition to all natural numbers.

- - -

Multiplication is defined in a similar way, for every $m \in \mathbb{N}$, by the clauses:

$$
\begin{align}
&m \cdot 0 = 0 \\[6pt]
&m \cdot S(n) = m \cdot n + m
\end{align}
$$

Multiplication is built from addition, since multiplying by a successor amounts to adding one further copy of the multiplicand.

> The legitimacy of recursive definitions of this kind rests on the recursion theorem, due to Dedekind, which guarantees that a function on $\mathbb{N}$ is uniquely determined once its value at $0$ and its behaviour under the successor are specified. Without this result the clauses would express an intention rather than a definition, since their consistency cannot be established by direct inspection of every natural number.

- - -

Exponentiation is built from multiplication by a recursion of the same form, for every $m \in \mathbb{N}$:

$$
\begin{align}
&m^0 = 1 \\[6pt]
&m^{S(n)} = m^n \cdot m
\end{align}
$$

The first clause assigns to the empty product its conventional value, and the second reduces a power with successor exponent to a further multiplication by the base. Each arithmetic operation is thus built from a recursion grounded in the previous one.

## Properties of the operations

From the recursive definitions, together with the induction axiom, one can prove that addition and multiplication satisfy the expected algebraic properties. The proofs proceed by induction on one of the arguments, and they are a standard exercise in arithmetic.

+ Addition is associative and commutative, and has $0$ as neutral element.
+ Multiplication is associative and commutative, has $1$ as neutral element, and distributes over addition.

These properties are summarised as follows:

$$
\begin{align}
&(a + b) + c = a + (b + c) \\[6pt]
&a + b = b + a \\[6pt]
&a + 0 = a \\[6pt]
&(a \cdot b) \cdot c = a \cdot (b \cdot c) \\[6pt]
&a \cdot b = b \cdot a \\[6pt]
&a \cdot 1 = a \\[6pt]
&a \cdot (b + c) = a \cdot b + a \cdot c
\end{align}
$$

Two further properties distinguish $\mathbb{N}$ from more general algebraic structures. The first is cancellation: for every $a, b, c \in \mathbb{N}$, the equality $a + c = b + c$ implies $a = b$, and the equality $a \cdot c = b \cdot c$ implies $a = b$ whenever $c \neq 0$. The second is the absence of zero divisors, that is, a product of two natural numbers equals zero only when at least one of the factors is zero. Multiplicative cancellation and the absence of zero divisors are logically equivalent in $\mathbb{N}$, and both state that no information is lost when a common nonzero factor is removed from an equality.

> Closure, associativity, commutativity, and the existence of the additive identity make $(\mathbb{N}, +)$ a commutative monoid, but not a [group](../groups/), since no positive natural number has a counterpart whose sum with it is $0$. The extension from $\mathbb{N}$ to $\mathbb{Z}$ supplies the missing additive inverses, and produces the first example of a [ring](../rings/).

## Order and well-ordering

The set $\mathbb{N}$ has a total order, which can be defined directly in terms of addition. Given two natural numbers $m$ and $n$, the relation $m \leq n$ holds if and only if there exists a natural number $k$ such that the following equality is satisfied:

$$
n = m + k
$$

In this definition the element $k$ measures the gap between $m$ and $n$, and its existence means that $n$ can be reached from $m$ by a finite number of successor steps. The relation so defined is reflexive, antisymmetric, transitive, and total, so that any two natural numbers are comparable.

The order so defined has two further properties. Trichotomy strengthens the totality of $\leq$ by asserting that for any $m, n \in \mathbb{N}$ exactly one of the relations $m < n$, $m = n$, $n < m$ holds, where $m < n$ denotes the conjunction of $m \leq n$ with $m \neq n$. Discreteness states that no natural number lies strictly between two consecutive ones: for every $n \in \mathbb{N}$ there is no $k \in \mathbb{N}$ satisfying $n < k < S(n)$. Together they express in algebraic form the picture of $\mathbb{N}$ as a sequence of evenly spaced points along the real line.

This order is a well-ordering, that is, every non-empty subset of $\mathbb{N}$ has a least element with respect to $\leq$. The well-ordering principle is logically equivalent to the principle of induction, in the sense that each can be derived from the other within a suitable axiomatic framework, and it gives an alternative foundation for the same results.

## Examples

As a first example, we compute the sum $2 + 3$ directly from the definition of addition. The computation relies exclusively on the recursive clauses and on the fact that $3 = S(S(S(0)))$. We start from the outer successor and apply the recursive clause for addition at each step:

$$
\begin{align}
2 + 3 &= 2 + S(S(S(0))) \\[6pt]
&= S(2 + S(S(0))) \\[6pt]
&= S(S(2 + S(0))) \\[6pt]
&= S(S(S(2 + 0))) \\[6pt]
&= S(S(S(2)))
\end{align}
$$

Since $S(S(S(2)))$ is, by definition, the natural number obtained from $2$ by applying the successor function three times, we conclude that $2 + 3 = 5$.

- - -

The same mechanism extends to multiplication, whose recursive clauses combine with those of addition. We compute the product $3 \cdot 2$ from $2 = S(S(0))$, applying the recursive clause for multiplication twice and reducing the result with the recursive clause for addition:

$$
\begin{align}
3 \cdot 2 &= 3 \cdot S(S(0)) \\[6pt]
&= 3 \cdot S(0) + 3 \\[6pt]
&= (3 \cdot 0 + 3) + 3 \\[6pt]
&= (0 + 3) + 3 \\[6pt]
&= 6
\end{align}
$$

The reduction proceeds by repeated application of the multiplicative clause until the multiplicand becomes zero, after which only the arithmetic of addition is required to reach the final value.

- - -

A proof by induction shows how the recursive definitions interact with the induction axiom to establish the algebraic properties listed above. As a representative case, we prove that $0$ is a left neutral element for addition, that is, $0 + n = n$ for every $n \in \mathbb{N}$.

The base case $n = 0$ follows directly from the first clause of the recursive definition of addition, which yields $0 + 0 = 0$. For the inductive step, we assume the equality $0 + n = n$ for some $n \in \mathbb{N}$ and derive the corresponding statement for $S(n)$:

$$
\begin{align}
0 + S(n) &= S(0 + n) \\[6pt]
&= S(n)
\end{align}
$$

The first equality follows from the second clause of the definition of addition, and the second from the inductive hypothesis. The induction axiom then guarantees that the equality holds for every natural number, which establishes the claim.

> The proof is asymmetric with respect to the two arguments, since the symmetric identity $n + 0 = n$ is given directly by the base clause of the recursive definition, while $0 + n = n$ requires induction. The commutativity of addition reconciles the two and, once established, makes this asymmetry invisible in subsequent computations.
