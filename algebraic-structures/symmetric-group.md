---
title: Symmetric Group
source: https://algebrica.org/symmetric-group/
license: CC BY-NC 4.0
tags:
  - algebraic-structures
  - alternating-group
  - cycle-notation
  - group-theory
  - parity-of-permutations
  - permutation
  - sign-homomorphism
  - symmetric-group
  - transposition
---
## Definition

Let $X_n = \{\ 1, 2, \ldots, n \ \}.$ A permutation of $X_n$ is a [bijection](../inverse-function/) $\sigma : X_n \to X_n.$ The set of all permutations of $X_n,$ equipped with [composition of functions](../composite-functions/), is the symmetric group on $n$ elements and is denoted $S_n.$

The group axioms follow from the properties of functions. The composite of two bijections of $X_n$ is a bijection of $X_n,$ so composition is an operation on $S_n.$ Composition is associative, the identity map is the identity element, and every bijection has an inverse that is also a bijection of $X_n.$ Hence $S_n$ is a [group](../groups/). Cayley's theorem states that every finite group of order $n$ is [isomorphic](../homomorphisms-and-isomorphisms/) to a subgroup of $S_n.$

The two-row notation for a permutation has the arguments in the first row and their images in the second:

$$\sigma = \begin{pmatrix} 1 & 2 & \cdots & n \\[6pt] \sigma(1) & \sigma(2) & \cdots & \sigma(n) \end{pmatrix}$$

The second row is a rearrangement of the first, and every such rearrangement determines a permutation. The image of $1$ has $n$ possible choices. Once that image is fixed, the image of $2$ has $n - 1$ choices, and the number of choices decreases by one at each step. Thus the order of the group is the [factorial](../factorial/):

$$|S_n| = n!$$

## Composition and non-commutativity

Composition is read from right to left, so $\sigma \circ \tau$ means that $\tau$ acts first and $\sigma$ acts on the result. The order of the two factors matters. The smallest non-abelian symmetric group is $S_3,$ which has order $6.$ Let $\sigma$ send $1 \mapsto 2,$ $2 \mapsto 3,$ $3 \mapsto 1,$ and let $\tau$ exchange $1$ and $2$ while fixing $3:$

$$\sigma = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 3 & 1 \end{pmatrix} \qquad \tau = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 1 & 3 \end{pmatrix}$$

To compute $\sigma \circ \tau,$ we track each element first under $\tau$ and then under $\sigma.$ The element $1$ is sent by $\tau$ to $2,$ and $\sigma$ sends $2$ to $3,$ so $1 \mapsto 3.$ The element $2$ is sent by $\tau$ to $1,$ and $\sigma$ sends $1$ to $2,$ so $2 \mapsto 2.$ The element $3$ is fixed by $\tau,$ and $\sigma$ sends $3$ to $1,$ so $3 \mapsto 1.$ Therefore:

$$\sigma \circ \tau = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 3 & 2 & 1 \end{pmatrix}$$

Reversing the order changes the result. Now $1$ is sent by $\sigma$ to $2,$ and $\tau$ sends $2$ to $1,$ so $1 \mapsto 1.$ The element $2$ is sent by $\sigma$ to $3,$ which $\tau$ fixes, so $2 \mapsto 3.$ The element $3$ is sent by $\sigma$ to $1,$ and $\tau$ sends $1$ to $2,$ so $3 \mapsto 2:$

$$\tau \circ \sigma = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 1 & 3 & 2 \end{pmatrix}$$

The two results differ, so $S_3$ is not abelian. For $n \geq 3,$ define the two permutations above to fix all elements from $4$ to $n.$ Their composites still differ, so $S_n$ is non-abelian. The groups $S_1$ and $S_2$ are abelian, of orders $1$ and $2.$

## Cycle notation

The two-row display lists every image of a permutation. Cycle notation records the sequence obtained by applying the permutation repeatedly to a single element.

Let $a_1, a_2, \ldots, a_k$ be distinct elements of $X_n.$ The cycle $(a_1\ a_2\ \cdots\ a_k)$ is the permutation sending $a_1$ to $a_2,$ $a_2$ to $a_3,$ and so on until $a_k,$ which is sent back to $a_1,$ while every element outside the list is fixed. Such a permutation is a $k$-cycle, and $k$ is its length. A $2$-cycle is a transposition. In this notation the permutations of the previous section are $\sigma = (1\ 2\ 3)$ and $\tau = (1\ 2),$ and their composites are $\sigma \circ \tau = (1\ 3)$ and $\tau \circ \sigma = (2\ 3).$

The same cycle can be written in $k$ ways, since any of its elements can be the starting point: $(1\ 2\ 3),$ $(2\ 3\ 1),$ and $(3\ 1\ 2)$ denote the same permutation.

Two cycles are disjoint when no element appears in both. Disjoint cycles commute, because each moves only elements that the other fixes, so applying them in either order gives the same values.

Every permutation decomposes into disjoint cycles. Start from any element $a,$ and form the sequence $a, \sigma(a), \sigma^2(a), \ldots$ Since $X_n$ is finite the sequence must repeat, and the first repetition returns to $a,$ because $\sigma$ is injective. The terms before this repetition form a cycle. Removing its elements from $X_n$ leaves a smaller set that $\sigma$ maps to itself, and repeating the argument exhausts $X_n.$ The decomposition is unique up to the order of the factors and the choice of starting point inside each cycle. Fixed points correspond to cycles of length $1$ and are usually omitted.

As an example, consider the permutation of $X_6$ given by:

$$\rho = \begin{pmatrix} 1 & 2 & 3 & 4 & 5 & 6 \\[6pt] 3 & 5 & 1 & 4 & 2 & 6 \end{pmatrix}$$

Following $1$ gives $1 \mapsto 3 \mapsto 1,$ which closes the cycle $(1\ 3).$ Following $2$ gives $2 \mapsto 5 \mapsto 2,$ which closes the cycle $(2\ 5).$ The elements $4$ and $6$ are fixed. Therefore $\rho = (1\ 3)(2\ 5),$ a product of two disjoint transpositions.

## Order of a permutation

The cycle decomposition determines the [order](../groups/) of a permutation as an element of $S_n.$ Applying a $k$-cycle $j$ times moves each of its elements $j$ places forward along the cycle. The smallest positive value of $j$ that returns every element to its starting position is $k,$ so a $k$-cycle has order $k.$

For a general permutation $\sigma$ with disjoint cycles of lengths $k_1, k_2, \ldots, k_m,$ the power $\sigma^j$ acts on each cycle independently, because disjoint cycles commute. So $\sigma^j$ is the identity exactly when $j$ is a multiple of every $k_i,$ which gives the order as the least common multiple:

$$\mathrm{ord}(\sigma) = \mathrm{lcm}(k_1, k_2, \ldots, k_m)$$

The permutation $\rho = (1\ 3)(2\ 5)$ has order $2.$ A permutation of $X_5$ with a disjoint $2$-cycle and $3$-cycle has order $6,$ which exceeds the length of either cycle.

## Transpositions and the sign homomorphism

Every permutation is a product of transpositions. For a single cycle, the required identity is:

$$(a_1\ a_2\ \cdots\ a_k) = (a_1\ a_k)(a_1\ a_{k-1}) \cdots (a_1\ a_2)$$

The right side contains $k - 1$ transpositions. It sends $a_1$ to $a_2,$ since only the rightmost factor moves $a_1$ and the others leave $a_2$ fixed. For $2 \leq i \leq k - 1,$ the factors send $a_i$ to $a_1$ and then $a_1$ to $a_{i+1}.$ They send $a_k$ to $a_1.$ Since every permutation is a product of disjoint cycles, every permutation is a product of transpositions.

A factorisation into transpositions need not be unique, and different factorisations can have different numbers of factors. The parity of the number depends only on the permutation. To prove this without choosing a factorisation, consider the [polynomial](../polynomials/) in $n$ variables:

$$\Delta = \prod_{1 \leq i < j \leq n} (x_i - x_j)$$

For a permutation $\sigma,$ let $\sigma \cdot \Delta$ be the polynomial obtained by replacing each variable $x_i$ with $x_{\sigma(i)}.$ Every factor $x_{\sigma(i)} - x_{\sigma(j)}$ of the result equals $\pm(x_k - x_l)$ for exactly one pair $k < l,$ and distinct pairs $(i, j)$ give distinct pairs $(k, l)$ because $\sigma$ is injective. The factors of $\sigma \cdot \Delta$ are therefore the factors of $\Delta$ up to sign and up to order, which gives $\sigma \cdot \Delta = \pm\Delta.$ Define:

$$\mathrm{sgn}(\sigma) = \frac{\sigma \cdot \Delta}{\Delta} \in \{\ 1, -1 \ \}$$

The substitution rule satisfies $\sigma \cdot (\tau \cdot \Delta) = (\sigma \circ \tau) \cdot \Delta.$ Since $\tau \cdot \Delta$ is a scalar multiple of $\Delta,$ that scalar is unchanged by the substitution. Hence $\mathrm{sgn}(\sigma \circ \tau) = \mathrm{sgn}(\sigma)\mathrm{sgn}(\tau),$ so $\mathrm{sgn}$ is a [homomorphism](../homomorphisms-and-isomorphisms/) from $S_n$ to the multiplicative group $\{\ 1, -1 \ \}.$ This homomorphism is the sign homomorphism, and it is surjective for $n \geq 2.$

A transposition has sign $-1.$ Suppose that it exchanges $k$ and $l.$ Every factor involving neither $x_k$ nor $x_l$ is fixed. For each $r \notin \{\ k, l \ \},$ the two factors associated with the pairs $\{\ r, k \ \}$ and $\{\ r, l \ \}$ have a product that is unchanged by the exchange. The factor associated with $\{\ k, l \ \}$ changes sign. Hence the whole polynomial changes sign. Combining this result with a factorisation into transpositions gives $\mathrm{sgn}(\sigma) = (-1)^m$ whenever $\sigma$ is a product of $m$ transpositions.

A permutation is even when its sign is $1$ and odd when its sign is $-1.$ Since $\mathrm{sgn}(\sigma)$ depends on $\sigma$ alone, any two factorisations of the same permutation into transpositions have numbers of factors with the same parity.

> A $k$-cycle is a product of $k - 1$ transpositions, so it is even when $k$ is odd and odd when $k$ is even. The parity of a cycle is opposite to the parity of its length, and the $3$-cycle $(1\ 2\ 3)$ is an even permutation.

## The alternating group

The [kernel](../homomorphisms-and-isomorphisms/) of the sign homomorphism is the set of even permutations. This kernel is a normal subgroup of $S_n$ called the alternating group on $n$ elements and denoted $A_n.$

For $n \geq 2$ the sign homomorphism is surjective onto a group of order $2,$ so $A_n$ has index $2$ in $S_n.$ [Lagrange's theorem](../groups/) gives its order:

$$|A_n| = \frac{n!}{2}$$

The odd permutations form the other coset, which is $(1\ 2)A_n.$ If $\pi$ is odd, then $(1\ 2) \circ \pi$ is even, so $\pi$ belongs to $(1\ 2)A_n,$ and conversely every element of that coset is odd. The set of odd permutations is therefore not a subgroup, since it does not contain the identity.

As an example, $A_3$ has order $3$ and consists of the identity together with the two $3$-cycles $(1\ 2\ 3)$ and $(1\ 3\ 2),$ so it is cyclic. The group $A_4$ has order $12$ and is a counterexample to the converse of Lagrange's theorem, since it has no subgroup of order $6.$

## Conjugacy and cycle type

[Conjugation](../groups/) in $S_n$ relabels the entries of each cycle. For a permutation $\pi$ and a cycle $(a_1\ a_2\ \cdots\ a_k),$ the conjugate is obtained by applying $\pi$ to each entry:

$$\pi (a_1\ a_2\ \cdots\ a_k) \pi^{-1} = (\pi(a_1)\ \pi(a_2)\ \cdots\ \pi(a_k))$$

To verify this, apply the left side to $\pi(a_i).$ First $\pi^{-1}$ returns $a_i,$ then the cycle sends it to $a_{i+1},$ and finally $\pi$ sends $a_{i+1}$ to $\pi(a_{i+1}),$ which is the value of the right side. An element outside the cycle on the right is sent by $\pi^{-1}$ outside the original cycle, fixed by that cycle, and returned to its starting point by $\pi.$

The cycle type of a permutation is the list of the lengths of its disjoint cycles, written in decreasing order. Conjugation replaces each cycle by a cycle of the same length, so it preserves the cycle type. Conversely two permutations with the same cycle type are conjugate. Define $\pi$ by mapping each entry of the first cycle decomposition to the corresponding entry of the second. The formula above then shows that $\pi$ conjugates the first permutation into the second. The conjugacy classes of $S_n$ are therefore in bijection with the cycle types, that is, with the partitions of the integer $n.$

The five partitions of $4$ correspond to the five conjugacy classes of $S_4:$ the identity, the six transpositions, the three products of two disjoint transpositions, the eight $3$-cycles, and the six $4$-cycles. Their total is $24,$ the order of the group.

> Every normal subgroup of $S_n$ is a union of conjugacy classes, although not every union of conjugacy classes is a subgroup. In $S_4,$ the identity and the three products of two disjoint transpositions form a subgroup of order $4.$ This subgroup is normal and isomorphic to the Klein four-group.
