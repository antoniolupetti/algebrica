---
title: Cartesian Product
source: https://algebrica.org/cartesian-product/
license: CC BY-NC 4.0
tags:
  - axiom-of-choice
  - bijection
  - cardinality
  - cartesian-product
  - indexed-product
  - n-tuple
  - ordered-pair
  - set-operations
---

## Definition

In simple terms, the Cartesian product is the set of all ordered pairs that can be formed from two sets. Each pair has two components, the first belonging to the first set and the second to the second set. Formally, the Cartesian product of two [sets](../sets/) $A$ and $B$ is given by the following identity:

$$
A \times B = \{\ (a,b) \mid a \in A,\ b \in B \ \} \tag{1}
$$

By convention, the symbol $\times$ in $(1)$ denotes this construction on sets rather than the algebraic multiplication of their elements. Two ordered pairs are equal when their components have the same values in the same positions, that is:

$$
(a,b)=(c,d) \iff a=c \text{ and } b=d \tag{2}
$$

To make an important distinction, suppose we have a set $A=\{2,5\}$ and a set $B=\{5,2\}.$ By the properties of sets, $A$ and $B$ are equal because they contain the same elements, regardless of order. For ordered pairs, however, order matters. If we form the pairs $(2,5)$ and $(5,2)$ from $A$ and $B,$ they are different because the order of their components is reversed.

To illustrate the construction in $(1),$ consider two sets, $A=\{2,5,8\}$ and $B=\{u,v\},$ and arrange their elements as column and row headings. At each intersection, we enter the ordered pair formed from the corresponding column and row entries, obtaining:

$$ \tag{3}
\begin{array}{c|ccc}
B\backslash A & 2 & 5 & 8 \\[6pt]
\hline
u & (2,u) & (5,u) & (8,u) \\[6pt]
v & (2,v) & (5,v) & (8,v)
\end{array}
$$

We have thus constructed the Cartesian product $A \times B,$ in which each element of $A$ is paired with both elements of $B.$ The interior cells therefore list all six possible pairs in the product. We can also use this table to calculate the [cardinality](../cardinality-and-countable-sets/) of a product of finite sets. In general, if $A$ has $m$ elements and $B$ has $n,$ the total number of possible pairs is $m \times n,$ that is:

$$
|A \times B|=|A|\cdot|B| \tag{4}
$$

Indeed, in the example shown in the table, the product contains exactly $3\cdot 2=6$ elements. Formula $(4)$ therefore gives the cardinality of the Cartesian product. If either set is empty, no pair can be formed; conversely, if both sets contain at least one element, choosing $a\in A$ and $b\in B$ gives $(a,b)\in A\times B.$ Thus:

$$
A\times B=\emptyset
\iff
\begin{cases}
A=\emptyset & \text{or} \\[6pt]
B=\emptyset
\end{cases}
$$

Formula $(4)$ remains valid in this case, since at least one of the two numerical factors is zero, so the product has cardinality zero.

- - -

We now make an important distinction for pairs whose components are sets rather than numerical values. We must keep in mind that a set containing the empty set is not empty. For example, the [power set](../sets/) of $\{q\},$ that is, the set of all its subsets, including the empty set, is $\mathcal{P}(\{q\})=\{\emptyset,\{q\}\}.$ Its Cartesian product with a singleton (a set with exactly one element), such as $\{3\},$ is given by:

$$
\mathcal{P}(\{q\})\times\{3\}
=\{(\emptyset,3),(\{q\},3)\}
$$

The product is therefore not empty but contains two elements.

- - -

When both factors in $(1)$ are subsets of $\mathbb{R},$ the pairs in the product $A \times B$ are points in the [Cartesian plane](../the-cartesian-coordinate-plane/). Taking the product of $\mathbb{R}$ with itself gives the entire plane:

$$
\mathbb{R}^2=\mathbb{R}\times\mathbb{R}
=\{\ (x,y)\mid x\in\mathbb{R},\ y\in\mathbb{R}\ \}
$$

For example, the product of the [intervals](../intervals/) $[-2,1]$ and $[0,3]$ is:

$$
[-2,1]\times[0,3]
=\{\ (x,y)\in\mathbb{R}^2\mid -2\leq x\leq 1,\ 0\leq y\leq 3\ \}
$$

The product is therefore the rectangle with vertices $(-2,0),$ $(1,0),$ $(1,3)$ and $(-2,3),$ including its boundary and interior.

## The order of the factors

We now examine how the order of the factors affects the Cartesian product, returning to the sets $A=\{2,5,8\}$ and $B=\{u,v\}$ used earlier. Reversing the factors and forming $B\times A$ gives a different arrangement from that in table $(3),$ with the rows and columns interchanged:

$$ \tag{5}
\begin{array}{c|cc}
A\backslash B & u & v \\[6pt]
\hline
2 & (u,2) & (v,2) \\[6pt]
5 & (u,5) & (v,5) \\[6pt]
8 & (u,8) & (v,8)
\end{array}
$$

As we can see, table $(5)$ contains the same number of pairs as table $(3),$ but the pairs are different. For example, the pair $(u,2)$ belongs only to $B \times A$ and not to $A\times B,$ because its first component $u$ does not belong to $A.$ The Cartesian product is therefore not a commutative operation, and we have:

$$A\times B\neq B\times A$$

We can associate each pair $(a,b)$ in $A\times B$ with the pair $(b,a)$ in $B\times A$ by interchanging the components. For example, $(2,u)$ is matched with $(u,2).$ The general rule is:

$$
(a,b)\longleftrightarrow(b,a)
$$

Each pair in the second product is thus matched with exactly one pair in the first. To recover that pair, we simply interchange the components again, returning from $(b,a)$ to $(a,b).$ No pair is left out or matched twice, which is why the two products have the same cardinality even when they contain different pairs. For non-empty sets, the equality $A\times B=B\times A$ holds if and only if $A=B.$ If at least one factor is empty, however, both products are empty even when the factors are different. These cases are expressed by the following equivalence:

$$
A\times B=B\times A
\iff
\begin{cases}
A=B & \text{or} \\[6pt]
A=\emptyset & \text{or} \\[6pt]
B=\emptyset
\end{cases}
$$

## Set operations

In $(1)$ we defined the Cartesian product as an operation on sets, and as such it has several properties, including distributivity over [union, intersection and difference](../sets/). Thus, for three sets $A,$ $B$ and $C,$ the following identities hold:

$$
\begin{align}
A\times(B\cup C)&=(A\times B)\cup(A\times C) \\[6pt]
A\times(B\cap C)&=(A\times B)\cap(A\times C) \\[6pt]
A\times(B\setminus C)&=(A\times B)\setminus(A\times C)
\end{align}
$$

+ In the first identity, a pair belongs to the right-hand side when it belongs to at least one of the products $A\times B$ and $A\times C.$ This requires its first component to belong to $A$ and its second component to belong to at least one of $B$ and $C,$ that is, to $B\cup C,$ which is precisely the condition for membership in the left-hand side.
+ In the second identity, membership in the right-hand side requires the first component to belong to $A$ and the second to belong to both $B$ and $C,$ which are exactly the conditions defining the left-hand side.
+ Finally, in the last identity, the pair must belong to $A\times B$ and be excluded from $A\times C.$ The first condition already ensures that its first component belongs to $A.$ Exclusion from the second product is therefore equivalent to requiring that its second component does not belong to $C.$ That component therefore belongs to $B\setminus C,$ as required by the left-hand side.

Another property of the Cartesian product concerns inclusion. If $A\subseteq A'$ and $B\subseteq B',$ every pair in $A\times B$ has its first component in $A'$ and its second in $B'.$ Hence:

$$
A\subseteq A' \text{ and } B\subseteq B'
\implies A\times B\subseteq A'\times B'
$$

## Products of several factors

We now consider the case in which the Cartesian product in $(1)$ is extended to a product of $n$ sets of numbers. We first define an ordered $n$-tuple as a sequence $(a_1,\ldots,a_n)$ with $n$ components, where $n\geq 1.$ Two $n$-tuples are equal if and only if the components in corresponding positions are equal. The Cartesian product of $n$ sets is therefore defined by the following expression:

$$ \tag{6}
A_1\times\cdots\times A_n
=\{\ (a_1,\ldots,a_n)\mid a_i\in A_i \text{ for every } i\in\{1,\ldots,n\}\ \}
$$

If the factors are finite, each component can be chosen in $|A_i|$ ways. Applying formula $(4)$ for the cardinality of the product of two sets repeatedly gives:

$$
|A_1\times\cdots\times A_n|=\prod_{i=1}^{n}|A_i|
$$

When all factors are the same set, say $A,$ we use the notation $A^n.$ If $A$ is finite, then $|A^n|=|A|^n.$ In particular, $\mathbb{R}^n$ is the set of $n$-tuples of [real numbers](../real-numbers/). A particular case is $\mathbb{R}^3,$ which describes space using three coordinates. With three factors, we must distinguish an ordered triple from a pair containing another pair, and the elements have the following forms:

$$
\begin{align}
((a,b),c)&\in(A\times B)\times C \\[6pt]
(a,(b,c))&\in A\times(B\times C) \\[6pt]
(a,b,c)&\in A\times B\times C
\end{align}
$$

If one factor is empty, all three constructions give the empty set.

## Subsets and binary sequences

Cartesian products are useful in combinatorics because they allow us to count all the subsets of a finite set. Consider $E=\{e_1,\ldots,e_n\},$ with $n$ distinct elements, and associate each subset $S\subseteq E$ with the $n$-tuple $(\varepsilon_1,\ldots,\varepsilon_n)\in\{0,1\}^n$ defined by:

$$ \tag{7}
\varepsilon_i=
\begin{cases}
1 & \text{if } e_i\in S \\[6pt]
0 & \text{if } e_i\notin S
\end{cases}
$$

Each component $\varepsilon_i$ in $(7)$ indicates whether the element $e_i$ belongs to $S.$ The resulting $n$-tuple contains only the values $0$ and $1,$ so it is called a binary sequence. The set $\{0,1\}^n$ contains all such sequences of length $n.$

For example, if we fix the order $e_1,e_2,e_3,e_4,$ the subset $S=\{e_2,e_4\}$ is described by the sequence $(0,1,0,1).$ The first and third entries are $0$ because $e_1$ and $e_3$ do not belong to $S,$ while the second and fourth are $1$ because $e_2$ and $e_4$ do belong to it. We can also start with the sequence and recover the corresponding subset by reading its components in the fixed order, including $e_i$ when the entry in position $i$ is $1$ and excluding it when the entry is $0.$ For example, from $(0,1,0,1)$ we obtain exactly $\{e_2,e_4\}.$

Notice that each subset determines exactly one sequence, and each sequence determines exactly one subset. Counting the subsets of $E$ is therefore equivalent to counting the elements of the Cartesian product $\{0,1\}^n,$ and since each factor has two elements, the cardinality is:

$$
|\mathcal{P}(E)|=|\{0,1\}^n|=2^n
$$

## Products of indexed families

The definition of the Cartesian product extends to a [family of sets](../sets/) $(A_i)_{i\in I},$ even when the index set $I$ is infinite, that is, when the product has infinitely many factors. An element of the product assigns to each index $i$ a component belonging to $A_i,$ and the product is written as:

$$
\prod_{i\in I}A_i
=\{\ (a_i)_{i\in I}\mid a_i\in A_i \quad \forall \ i\in I\ \}
$$

Formally, such a family of components is a [function](../functions/) $a$ with domain $I$ and values in the union of the factors, satisfying the condition:

$$
a\colon I\longrightarrow\bigcup_{i\in I}A_i
\qquad
a(i)\in A_i \quad \forall \ i\in I
$$

If a factor is empty, the product is empty because no function can assign an admissible value to that index. If the index set is empty, however, exactly one function has that domain, namely the empty function. The product with no factors is therefore a singleton and has cardinality $1$ (the only element of $A^0$ is the empty sequence).
