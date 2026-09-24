---
title: The Inclusion-Exclusion Principle
source: https://algebrica.org/inclusion-exclusion-principle/
license: CC BY-NC 4.0
tags:
  - cardinality
  - combinatorics
  - derangements
  - divisibility
  - inclusion-exclusion
  - set-operations
---

## Definition

The inclusion-exclusion principle is an important counting rule that determines how many elements of a finite set satisfy at least one of several conditions, counting each element exactly once even if it satisfies more than one condition. To describe it formally, we fix a finite set $U$ and associate with each condition we wish to check the subset of elements of $U$ that satisfy it. If, for example, there are two conditions and the corresponding subsets are $A$ and $B,$ the relevant [set operations](../sets/) have the following meanings:

+ The union $A \cup B$ contains the elements that satisfy at least one of the two conditions.
+ The intersection $A \cap B$ contains the elements that satisfy both conditions.
+ The complement $U \setminus (A \cup B)$ contains the elements that satisfy neither condition.

We write $|A|$ for the [cardinality](../cardinality-and-countable-sets/) of the subset $A,$ which is the number of its elements. The sum $|A|+|B|$ counts an element belonging only to $A$ or only to $B$ once, whereas an element common to both subsets is counted twice. To ensure that an element common to both subsets is also counted only once, we use the following identity:

$$
|A \cup B| = |A| + |B| - |A \cap B| \tag{1}
$$

When $A$ and $B$ are disjoint, their intersection is empty and the formula reduces to the sum of the cardinalities of the subsets, whereas if $A \subseteq B,$ then $A \cap B=A$ and the formula gives $|A \cup B|=|B|.$

- - -

We now consider a finite family of subsets $A_1,\ldots,A_n$ of a finite set $U,$ with $n \geq 1.$ For each integer $k$ between $1$ and $n,$ let $S_k$ denote the sum of the cardinalities of all intersections obtained by choosing $k$ sets with distinct indices. We can therefore write:

$$ \tag{2}
S_k := \sum_{1 \leq i_1 < \cdots < i_k \leq n}
|A_{i_1} \cap \cdots \cap A_{i_k}|
$$

In $(2),$ the condition $i_1<\cdots<i_k$ ensures that the indices are in increasing order, so that each combination is counted only once. Thus $S_1$ is the sum of the cardinalities of the individual sets, $S_2$ is the sum of the cardinalities of their pairwise intersections, and $S_n$ is the cardinality of the intersection of all the sets. The inclusion-exclusion principle states that:

$$ \tag{3}
\left|\bigcup_{i=1}^{n} A_i\right|
= \sum_{k=1}^{n} (-1)^{k+1}S_k
$$

In other words, formula $(3)$ gives the number of elements in the union as follows:

+ For $k=1,$ we add the cardinalities of the individual sets, giving the contribution $+S_1.$
+ For $k=2,$ we subtract the cardinalities of the pairwise intersections, giving the contribution $-S_2.$
+ For $k=3,$ we add the cardinalities of the triple intersections, giving the contribution $+S_3.$

We continue up to $k=n,$ alternating addition and subtraction according to the sign of the factor $(-1)^{k+1}$ until the final term, which corresponds to the intersection of all the sets. To clarify $(3)$ with an example, we consider three sets $A,$ $B$ and $C.$ Applying $(3)$ with $n=3$ and substituting the expressions for $S_1,$ $S_2$ and $S_3$ given by $(2),$ we obtain:

$$
\begin{align}
|A \cup B \cup C|
&= |A| + |B| + |C| \\[6pt]
&\quad - |A \cap B| - |A \cap C| - |B \cap C| \\[6pt]
&\quad + |A \cap B \cap C|
\end{align}
$$

This counts each element of the union exactly once, even when it belongs to more than one set, which is precisely the result we wanted to obtain by applying the inclusion-exclusion principle.

- - -

In many problems, however, it is easier to count the elements to be excluded than the elements we seek. In practice, if a subset $A_i$ contains the elements that satisfy the $i$-th unwanted condition, the elements we seek belong to the complement of the union. We therefore have:

$$ \tag{4}
\begin{align}
\left|U \setminus \bigcup_{i=1}^{n} A_i\right|
&= |U| - \left|\bigcup_{i=1}^{n} A_i\right| \\[6pt]
&= |U| + \sum_{k=1}^{n} (-1)^k S_k
\end{align}
$$

Notice that the signs in formula $(4)$ are reversed relative to the union formula $(3).$ This method can be quicker than direct counting when we know the cardinality of $U$ and can easily count the elements to be excluded. In this case, subtracting their number from $|U|$ gives the number of elements we seek without having to identify them individually.

## Proof

To prove $(3),$ we begin by calculating the contribution of a single element $x$ to the sum. If $x$ belongs to none of the subsets $A_i,$ then it belongs to none of their intersections, so its contribution is clearly zero. Suppose instead that $x$ belongs to the union, and define the set of indices of the subsets containing it:

$$
I_x := \{\ i \in \{1,\ldots,n\} \mid x \in A_i \ \}
$$

To make the explanation as clear as possible, consider the following points:

+ The set $I_x$ is necessarily nonempty.
+ Each intersection in $(3)$ is obtained by choosing one or more sets from $A_1,\ldots,A_n.$
+ We write $J$ for the set of chosen indices (for example, $J=\{1,3\}$ corresponds to the intersection $A_1 \cap A_3).$
+ The intersection of the sets chosen in the preceding item contains $x$ if and only if each of those sets contains $x.$ For $J=\{1,3\},$ this means that $x$ must belong to both $A_1$ and $A_3.$

Thus, to obtain an intersection containing $x,$ we must choose sets from among those that contain $x.$ Their indices must therefore belong to $I_x,$ which means that $J \subseteq I_x.$

Next, we write $k=|J|$ for the number of chosen sets. To see how $x$ is counted, consider the following points about $(3):$

+ The cardinalities of the individual sets are added, so each set containing $x$ contributes $+1$ to the count of $x.$
+ The cardinalities of the intersections of two sets are subtracted, so each such intersection containing $x$ contributes $-1.$
+ The cardinalities of the intersections of three sets are added, so each such intersection containing $x$ contributes $+1.$

For each $k$ from $1$ to $|I_x|,$ we therefore consider all intersections of $k$ sets containing $x,$ each of which contributes $(-1)^{k+1}$ to the count of $x.$ Since the indices in $J$ identify the chosen sets, their number is $k=|J|$ and the contribution of the corresponding intersection is $(-1)^{|J|+1}.$

Writing $c(x)$ for the sum of all these contributions, we obtain:

$$ \tag{5}
c(x) = \sum_{\varnothing \neq J \subseteq I_x} (-1)^{|J|+1}
$$

We choose an index $j \in I_x.$ We pair each nonempty subset $J$ of $I_x$ that does not contain $j$ with the subset $J \cup \{j\}.$ The cardinalities of these two subsets differ by one, so their contributions cancel:

$$ \tag{6}
(-1)^{|J|+1} + (-1)^{|J|+2} = 0
$$

Every nonempty subset other than $\{j\}$ belongs to exactly one pair, whose contributions cancel. The contribution $+1$ from $\{j\}$ remains, so $c(x)=1.$ The formula therefore counts each element of the union once and each element outside the union zero times. This proves the principle.

It is useful to express the same conclusion in terms of [binomial coefficients](../binomial-coefficient/) as well. Indeed, if $x$ belongs to exactly $m$ sets, with $m \geq 1,$ then it appears in $\binom{m}{k}$ intersections specified by $k$ indices. Grouping the terms in $(5)$ according to the number $k$ of chosen indices and recalling that $c(x)=1,$ we obtain the following identity:

$$
\sum_{k=1}^{m} (-1)^{k+1}\binom{m}{k} = 1
$$

## Example

To illustrate an application of the principle, we determine how many [integers](../integers/) from $1$ to $120,$ inclusive, are not divisible by any of the numbers $4,$ $6,$ and $9.$ We therefore define the set $U$ and the subsets $A,$ $B$ and $C$ corresponding to our conditions as follows:

$$
\begin{align}
U &= \{1,2,\ldots,120\} \\[6pt]
A &= \{\ m \in U \mid 4 \text{ divides } m \ \} \\[6pt]
B &= \{\ m \in U \mid 6 \text{ divides } m \ \} \\[6pt]
C &= \{\ m \in U \mid 9 \text{ divides } m \ \}
\end{align}
$$

To apply formula $(4),$ we need to calculate the cardinalities of the three sets and their intersections, which we do as follows.

For any positive integer $d,$ its positive multiples no greater than $120$ are clearly the numbers $qd$ with $q$ an integer such that $1 \leq q \leq 120/d.$ Their number is therefore $\lfloor 120/d \rfloor,$ where $\lfloor t \rfloor$ denotes the [greatest integer less than or equal to](../floor-and-ceiling-functions/) $t.$ An integer is a multiple of two given numbers if and only if it is a multiple of their least common multiple. For example, $A \cap B$ contains the multiples of $12,$ because the least common multiple of $4$ and $6$ is $12.$ Applying the same criterion to the other intersections gives:

| Set               | Condition          | Cardinality                 |
| ----------------- | ------------------ | --------------------------- |
| $A$               | Divisible by $4$   | $\lfloor 120/4 \rfloor=30$  |
| $B$               | Divisible by $6$   | $\lfloor 120/6 \rfloor=20$  |
| $C$               | Divisible by $9$   | $\lfloor 120/9 \rfloor=13$  |
| $A \cap B$        | Divisible by $12$  | $\lfloor 120/12 \rfloor=10$ |
| $A \cap C$        | Divisible by $36$  | $\lfloor 120/36 \rfloor=3$  |
| $B \cap C$        | Divisible by $18$  | $\lfloor 120/18 \rfloor=6$  |
| $A \cap B \cap C$ | Divisible by $36$  | $\lfloor 120/36 \rfloor=3$  |

Notice that the intersections $A \cap C$ and $A \cap B \cap C$ coincide, since every multiple of $36$ is also a multiple of $6.$ Substituting the values into the formula for the complement gives:

$$
\begin{align}
|U \setminus (A \cup B \cup C)|
&= 120 - (30+20+13) + (10+3+6) - 3 \\[6pt]
&= 120 - 63 + 19 - 3 \\[6pt]
&= 73
\end{align}
$$

There are therefore $73$ integers from $1$ to $120$ that are not divisible by any of the three given numbers.

## Derangements

We now consider $n$ distinct objects, each with an assigned position, and ask how many ways we can rearrange them so that no object occupies its assigned position. In formal terms, the problem amounts to counting the [permutations](../symmetric-group/) $\sigma$ of the $n$ objects for which $\sigma(i) \neq i$ for every index $i.$ These are called permutations without fixed points, or derangements, and we denote their number by $D_n.$

For $n \geq 1,$ we take $U$ to be the set of all permutations of the $n$ objects. Its cardinality is the [factorial](../factorial/) $n!,$ which counts the ways to arrange $n$ distinct objects in order. For each index $i,$ we define $A_i$ as the set of permutations that leave object $i$ in its own position, and write:

$$
A_i := \{\ \sigma \in U \mid \sigma(i)=i \ \}
$$

The permutations we seek do not belong to any of the sets $A_i,$ so their number is given by the following formula:

$$\tag{7}
D_n = \left|U \setminus \bigcup_{i=1}^{n} A_i\right|
$$

If we require $k$ specified objects to remain in their own positions, the remaining $n-k$ objects can be permuted freely among the remaining positions. Thus every intersection associated with $k$ distinct indices has cardinality $(n-k)!.$ Since there are $\binom{n}{k}$ ways to choose the $k$ indices, the sum of the cardinalities of these intersections is given by:

$$ \tag{8}
S_k = \binom{n}{k}(n-k)!
$$

Substituting $|U|=n!$ and $S_k=\binom{n}{k}(n-k)!$ into $(4),$ we obtain the following number of permutations:

$$
\begin{align}
D_n
&= n! + \sum_{k=1}^{n} (-1)^k\binom{n}{k}(n-k)! \\[6pt]
&= \sum_{k=0}^{n} (-1)^k\binom{n}{k}(n-k)! \\[6pt]
&= n!\sum_{k=0}^{n} \frac{(-1)^k}{k!}
\end{align}
$$

For example, with five objects we obtain:

$$
\begin{align}
D_5
&= 5!\left(1-1+\frac{1}{2!}-\frac{1}{3!}+\frac{1}{4!}-\frac{1}{5!}\right) \\[6pt]
&= 120-120+60-20+5-1 \\[6pt]
&= 44
\end{align}
$$

There are therefore exactly $44$ permutations of five objects in which no object remains in its own position.
