---
title: Sets
source: https://algebrica.org/sets/
license: CC BY-NC 4.0
tags:
  - cardinality
  - cartesian-product
  - de-morgan-laws
  - inclusion-exclusion
  - indexed-family
  - ordered-pair
  - partition
  - power-set
  - set
  - set-operations
  - subset
  - universal-set
---

## Introduction

A set is a collection of objects called elements that are considered as a whole. Sets are represented by uppercase letters $A,$ $B,$ $C,$ and their elements by lowercase letters. The notation $x \in A$ indicates that an object $x$ belongs to the set $A,$ while $x \notin A$ indicates that $x$ is not an element of $A.$ For any given object, it is always possible to determine unambiguously whether the object belongs to the collection or not.

A set can be described by enumeration or by set-builder notation. Enumeration consists in explicitly listing each element of the set, and is practical when the cardinality of the set is finite and small:

$$
A = \{a_1, a_2, a_3, a_4\}
$$

When the elements are numerous or infinite, set-builder notation becomes preferable. In this case the set is described by the property that each element must satisfy in order to belong to it:

$$
A = \\{ x \in \mathbb{Z} \mid x > 4, \ x \leq 8 \\}
$$

The previous notation defines $A$ as the set of all [integers](../integers/) $x$ such that $x > 4$ and $x \leq 8,$ that is, the following set:

$$
A = \{5, 6, 7, 8\}
$$

The empty set contains no elements, is denoted by $\emptyset$ or $\\{\\},$ and plays a role in set theory analogous to that of zero in arithmetic.

## The universal set

A main collection containing all objects under consideration is called the universal set and is written as $U.$ All sets in a given context are subsets of $U.$ The choice of $U$ depends on the situation. In elementary number theory one often works with $U = \mathbb{Z},$ whereas in real analysis the usual choice is $U = \mathbb{R}.$

> The universal set is the tool that makes the notion of set complement unambiguous, as discussed in the section on set operations.

## Cardinality of finite sets

The cardinality of a set $A,$ denoted $|A|,$ is the number of elements the set contains. The cardinality can be measured in different situations, as follows.

The empty set has cardinality $|\emptyset| = 0.$ Two finite sets have the same cardinality if and only if they contain the same number of elements.

The cardinality of the power set of a finite set $A$ with $n$ elements is given by:

$$
|\mathcal{P}(A)| = 2^n
$$

The cardinality of the Cartesian product of two finite sets $A$ and $B$ is given by:

$$
|A \times B| = |A| \cdot |B|
$$

In this case each element of $A$ can be paired with every element of $B,$ producing $|A| \cdot |B|$ ordered pairs.

The cardinality of the union of two sets $A$ and $B$ is given by:

$$
|A \cup B| = |A| + |B| - |A \cap B|
$$

The previous expression is the inclusion-exclusion principle, which ensures that elements common to both sets are counted once. Every element of $A \cup B$ appears in the sum $|A| + |B|.$ Elements lying in $A \cap B$ are counted twice, so the term is subtracted to guarantee the correct count.

The principle extends to three sets, as expressed by:

$$
|A \cup B \cup C| = |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C|
$$

The structure of the formula can be read as follows:

+ Elements belonging to one set are counted only once.
+ Elements shared by two sets are counted twice and subtracted once, yielding a net contribution of $1.$
+ Elements lying in all three sets are added three times, subtracted three times, and added back once through the triple intersection, again producing a net contribution of one.

## Subsets and power sets

The notions of subset and power set are introduced together. Subsets are sets whose elements all belong to another set, while power sets are sets whose elements are themselves subsets of a given set. A set $A$ is a subset of $B$ if every element of $A$ is also an element of $B$:

$$
A \subseteq B \iff \forall \ x, \ x \in A \rightarrow x \in B
$$

Two sets are equal if and only if each is contained in the other, which is the standard way to establish set equality in mathematics:

$$
A = B \iff A \subseteq B \text{ and } B \subseteq A
$$

If $A \subseteq B$ and $A \neq B,$ then $A$ is a proper subset of $B,$ denoted $A \subsetneq B,$ and in this case there exists at least one element in $B$ that does not belong to $A.$ The empty set is a subset of every set. The inclusion $\emptyset \subseteq A$ holds for any set $A,$ because the implication $x \in \emptyset \Rightarrow x \in A$ is vacuously true.

The power set of a set $A$ is the set of all subsets of $A,$ denoted $\mathcal{P}(A).$ It includes the empty set $\emptyset$ and the set $A$ itself. If $A$ has $n$ elements, then $\mathcal{P}(A)$ has $2^n$ elements. For example, if $A = \\{a, b, c\\},$ then the power set contains $2^3 = 8$ elements:

$$
\mathcal{P}(A) = \{\emptyset, \ \{a\}, \ \{b\}, \ \{c\}, \ \{a,b\}, \ \{a,c\}, \ \{b,c\}, \ \{a,b,c\}\}
$$


## Indexed families of sets

When several sets are considered together, labeling them by an index keeps the notation compact. A family of sets indexed by a set $I$ assigns a set $A_i$ to each index $i \in I,$ and is written $\\{A_i\\}_{i \in I}.$ The index set $I$ can be finite, countable, or uncountable, so this notation is more general than a finite list of terms.

The union of the family is the set of elements that belong to at least one of its members, and the intersection is the set of elements that belong to every member:

$$
\bigcup_{i \in I} A_i = \\{x \mid x \in A_i \text{ for some } i \in I\\}
$$

$$
\bigcap_{i \in I} A_i = \\{x \mid x \in A_i \text{ for every } i \in I\\}
$$

An element belongs to the union as soon as one member of the family contains it, and belongs to the intersection only when every member contains it.

A family $\\{A_i\\}_{i \in I}$ is pairwise disjoint when any two distinct members share no elements:

$$
A_i \cap A_j = \emptyset \quad \forall \ i \neq j
$$

For each $n \in \mathbb{N}$ the singletons $\\{n\\}$ form a pairwise disjoint family, and their union is the set $\mathbb{N}.$


## Partitions

A partition of a set $A$ is a family of non-empty subsets $\\{A_i\\}_{i \in I}$ that are pairwise disjoint and cover the whole of $A.$ The following conditions must hold:

$$
\begin{align}
&A_i \neq \emptyset \quad \forall \ i \in I \\[6pt]
&A_i \cap A_j = \emptyset \quad \forall \ i \neq j \\[6pt]
& \bigcup_{i \in I} A_i = A
\end{align}
$$

The subsets $A_i$ are called the blocks of the partition, and each element of $A$ belongs to exactly one of them. A simple example is the set of [integers](../integers/) $\mathbb{Z},$ which can be partitioned into the set of even integers and the set of odd integers, since these two blocks are non-empty, disjoint, and together cover the whole of $\mathbb{Z}.$

Partitions are related to equivalence relations. Given an equivalence relation on $A$:

+ The equivalence classes it induces form a partition of $A.$
+ Any partition of $A$ defines an equivalence relation by declaring two elements equivalent whenever they belong to the same block.


## Set operations

Set operations generate new sets by combining the elements of different sets. The main operations are union, intersection, complement, and difference.

The union of $A$ and $B$ is the set of all elements that belong to at least one of the two sets. Elements common to $A$ and $B$ are listed only once, since sets do not allow repetitions.

![IMG. 1](svg/sets-1.svg)

$$
A \cup B = \\{x \mid x \in A \text{ or } x \in B\\}
$$
- - - 

The intersection of $A$ and $B$ is the set of elements that belong to both sets:

![IMG. 2](svg/sets-2.svg)

$$
A \cap B = \\{x \mid x \in A \text{ and } x \in B\\}
$$

If $A \cap B = \emptyset,$ the two sets are disjoint and share no elements.

- - -

The complement of $A$ with respect to a universal set $U$ is the set of all elements in $U$ that do not belong to $A.$ It is written as:

$$
A^c = \\{x \in U \mid x \notin A\\}
$$

![IMG. 3](svg/sets-3.svg)

Another way to represent the complement of $A$ is $\overline{A}$ or $U \setminus A.$ A single set may yield different complements when $U$ changes, since the elements of the complement vary with the universal set we pick.

- - -

The difference of $A$ and $B,$ written $A \setminus B,$ is the set of elements that belong to $A$ but not to $B$:

![IMG. 4](svg/sets-4.svg)

$$
A \setminus B = \\{x \mid x \in A \text{ and } x \notin B\\}
$$

The relation $A \setminus B \neq B \setminus A$ holds in general, since the difference of two sets is not a commutative operation. For any universal set that contains both $A$ and $B$ the identity $A \setminus B = A \cap B^c$ holds, which expresses the difference through the complement.

The symmetric difference of $A$ and $B,$ written $A \triangle B,$ is the set of elements that belong to one of the two sets but not to both:

![IMG. 5](svg/sets-5.svg)

$$
A \triangle B = (A \setminus B) \cup (B \setminus A)
$$

An equivalent representation is given by the following expression:

$$
A \triangle B = (A \cup B) \setminus (A \cap B)
$$

The symmetric difference is commutative and associative, and satisfies $A \triangle A = \emptyset$ and $A \triangle \emptyset = A.$ Together with intersection, it gives the collection of all subsets of a given set the structure of a Boolean [ring](../rings/).

## Properties of set operations

The set operations satisfy a series of identities that form the foundation of Boolean algebra and hold for any sets $A,$ $B,$ and $C$ within a universal set $U.$ Union and intersection are commutative operations. The order in which two sets are combined does not affect the result.

$$
\begin{align}
A \cup B &= B \cup A \\[6pt]
A \cap B &= B \cap A
\end{align}
$$

Both operations are also associative, meaning that when three sets are combined, the grouping of the operands is irrelevant.

$$
\begin{align}
(A \cup B) \cup C &= A \cup (B \cup C) \\[6pt]
(A \cap B) \cap C &= A \cap (B \cap C)
\end{align}
$$

Union and intersection distribute over each other, in a manner analogous to the distributive law of arithmetic.

$$
\begin{align}
A \cap (B \cup C) &= (A \cap B) \cup (A \cap C) \\[6pt]
A \cup (B \cap C) &= (A \cup B) \cap (A \cup C)
\end{align}
$$

The empty set and the universal set act as the identity element for union and intersection respectively. Combining any set with either of them returns the original set.

$$
\begin{align}
A \cup \emptyset &= A \\[6pt]
A \cap U &= A
\end{align}
$$

The empty set annihilates intersection and the universal set annihilates union. Combining any set with these elements returns the absorbing element rather than the original set:

$$
\begin{align}
A \cap \emptyset &= \emptyset \\[6pt]
A \cup U &= U
\end{align}
$$

Each element of $U$ lies either in $A$ or in its complement, never in both. Applying the complement operation a second time in succession returns the original set:

$$
\begin{align}
A \cup A^c &= U \\[6pt]
A \cap A^c &= \emptyset \\[6pt]
(A^c)^c &= A
\end{align}
$$

## De Morgan's laws

De Morgan's laws are algebraic identities that describe how union and intersection behave under the complement operation. These identities allow set expressions to be rewritten in equivalent forms and help to simplify the operations.

$$
\begin{align}
(A \cup B)^c &= A^c \cap B^c \\[6pt]
(A \cap B)^c &= A^c \cup B^c
\end{align}
$$

The first law states that the complement of a union equals the intersection of the complements. An element is missing from $A \cup B$ only when it is missing from both $A$ and $B,$ which is the same as belonging to both $A^c$ and $B^c.$

![IMG. 6](svg/sets-6.svg)

The second law states that an element is not in the intersection $A \cap B$ when it is missing from at least one of the two sets, and this places it in $A^c \cup B^c.$

These laws extend to an arbitrary family of sets $\\{A_i\\}_{i \in I},$ with no restriction on the size of the index set $I$:

$$
\begin{align}
\left(\bigcup_{i \in I} A_i\right)^c &= \bigcap_{i \in I} A_i^c \\[6pt]
\left(\bigcap_{i \in I} A_i\right)^c &= \bigcup_{i \in I} A_i^c
\end{align}
$$

A correspondence exists between the algebraic structure of sets and that of the logical connectives. De Morgan's laws translate into the following equivalences for the connectives $\land$ and $\lor$:

$$
\neg(P \lor Q) \equiv \neg P \land \neg Q
$$

$$
\neg(P \land Q) \equiv \neg P \lor \neg Q
$$

## Example

Let $U = \\{1, 2, 3, 4, 5, 6, 7, 8, 9, 10\\}$ be the universal set, and define the following two subsets:

$$
\begin{align}
A &= \{1, 2, 3, 4, 6\} \\[6pt]
B &= \{2, 4, 6, 8, 10\}
\end{align}
$$

The union and intersection of the two sets are computed directly from the definitions:

$$
\begin{align}
A \cup B &= \{1, 2, 3, 4, 6, 8, 10\} \\[6pt]
A \cap B &= \{2, 4, 6\}
\end{align}
$$

The complements with respect to $U$ collect the elements excluded from each set:

$$
\begin{align}
A^c &= \{5, 7, 8, 9, 10\} \\[6pt]
B^c &= \{1, 3, 5, 7, 9\}
\end{align}
$$

We now verify the first De Morgan law. The complement of the union is:

$$
(A \cup B)^c = U \setminus (A \cup B) = \\{5, 7, 9\\}
$$

The intersection of the complements gives:

$$
\begin{align}
A^c \cap B^c &= \{5, 7, 8, 9, 10\} \cap \{1, 3, 5, 7, 9\} \\[6pt]
&= \{5, 7, 9\}
\end{align}
$$

The two sets coincide, confirming the first De Morgan law. We now verify the inclusion-exclusion principle using cardinalities:

$$
|A| = 5 \quad |B| = 5 \quad |A \cap B| = 3
$$

$$
|A \cup B| = 5 + 5 - 3 = 7
$$

A direct count of the elements of $A \cup B = \\{1, 2, 3, 4, 6, 8, 10\\}$ confirms that $|A \cup B| = 7.$

We compute the symmetric difference and check how it relates to the other operations:

$$
A \triangle B = (A \setminus B) \cup (B \setminus A)
$$

The two differences are $A \setminus B = \\{1, 3\\}$ and $B \setminus A = \\{8, 10\\},$ giving:

$$
A \triangle B = \\{1, 3, 8, 10\\}
$$

The same result is obtained through the equivalent characterisation that uses union and intersection:

$$
\begin{align}
(A \cup B) \setminus (A \cap B) &= \{1, 2, 3, 4, 6, 8, 10\} \setminus \{2, 4, 6\} \\[6pt]
&= \{1, 3, 8, 10\}
\end{align}
$$


## Cartesian product

Given two sets $A$ and $B,$ the Cartesian product $A \times B$ is the set of all ordered pairs $(a, b)$ such that $a$ belongs to $A$ and $b$ belongs to $B$:

$$
A \times B = \\{(a, b) \mid a \in A, \ b \in B\\}
$$

An ordered pair is asymmetric: $(a, b)$ differs from $(b, a)$ if $a$ and $b$ are not the same. Two ordered pairs are equal if and only if their corresponding components are equal, as expressed by the following condition:

$$
(a, b) = (a', b') \iff a = a' \text{ and } b = b'
$$

In general $A \times B$ and $B \times A$ are not the same set. If $A$ contains $m$ elements and $B$ contains $n$ elements, then $A \times B$ contains $mn$ elements. For example $\mathbb{R} \times \mathbb{R},$ which is the set of all pairs of [real numbers](../real-numbers/), is the Cartesian plane $\mathbb{R}^2.$

Given the sets $A_1, A_2, \ldots, A_n,$ their Cartesian product is the set of all ordered $n$-tuples:

$$
A_1 \times A_2 \times \cdots \times A_n = \\{(a_1, a_2, \ldots, a_n) \mid a_i \in A_i \text{ for each } i = 1, \ldots, n\\}
$$

An $n$-tuple $(a_1, \ldots, a_n)$ is an ordered sequence of $n$ elements, and two $n$-tuples are equal if and only if all corresponding components are equal. If all sets are identical, that is, $A_i = A$ for every $i,$ the product is $A^n.$ The space $\mathbb{R}^n$ is the $n$-fold Cartesian product of $\mathbb{R}$ with itself, and its elements are $n$-tuples of real numbers.

## The ordered pair

The discussion so far has treated the ordered pair $(a, b)$ as an intuitive notion, namely a pair of objects in which the first component is $a$ and the second is $b.$ In formal terms, the ordered pair can be defined set-theoretically as a set containing two elements:

$$
(a, b) = \\{\\{a\\}, \ \\{a, b\\}\\}
$$

The term $\\{a\\}$ is the singleton, and $\\{a, b\\}$ is the unordered pair. The element $a$ appears in both, whereas $b$ appears only in one. This definition is justified by the following result:

$$
(a, b) = (c, d) \implies a = c \text{ and } b = d
$$

To verify this property, suppose $\\{\\{a\\}, \\{a, b\\}\\} = \\{\\{c\\}, \\{c, d\\}\\}.$ There are two cases, depending on whether $a = b$ or $a \neq b.$

In the first case, when $a = b,$ we have $\\{a, b\\} = \\{a\\},$ so the left-hand side becomes $\\{\\{a\\}\\},$ a singleton set. For equality, the right-hand side must also be a singleton, which requires $\\{c\\} = \\{c, d\\}$ and so $c = d.$ The single element on each side must coincide, so $\\{a\\} = \\{c\\},$ and therefore $a = c.$ Since $b = a = c = d,$ it follows that $a = c$ and $b = d.$

If $a \neq b,$ then the left-hand side contains two distinct elements: $\\{a\\}$ and $\\{a, b\\}.$ The singleton $\\{a\\}$ must correspond either to $\\{c\\}$ or to $\\{c, d\\}$ on the right-hand side. If $\\{a\\} = \\{c, d\\},$ then $c = d = a,$ which would make $\\{c\\} = \\{c, d\\},$ resulting in a singleton on the right, contradicting the presence of two distinct elements on the left. Therefore $\\{a\\} = \\{c\\},$ so $a = c.$ It follows that $\\{a, b\\} = \\{c, d\\} = \\{a, d\\},$ and since $a \neq b,$ it must be that $b = d.$

In both cases, $a = c$ and $b = d,$ as required. The converse is straightforward, since if $a = c$ and $b = d$ then the two sets are identical by substitution.
