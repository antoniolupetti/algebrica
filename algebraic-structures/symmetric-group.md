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

Consider the set $X_n = \{1, 2, \ldots, n\},$ where $n \geq 1,$ and define the symmetric group $S_n$ to be the group of all permutations of $X_n$ under composition. Since a permutation is a bijection from $X_n$ to itself, the product of two permutations and the inverse of any permutation are again permutations of $X_n.$ Composition is associative, and its identity element is the identity map on $X_n.$

To count the elements of $S_n,$ we can write each permutation of $X_n$ as follows:

$$
\begin{align}
\sigma &= \begin{pmatrix}
1 & 2 & \cdots & n \\[6pt]
\sigma(1) & \sigma(2) & \cdots & \sigma(n)
\end{pmatrix} \tag{1}
\end{align}
$$

In $(1),$ the second row determines the permutation and can list the $n$ elements in any order. There are $n$ choices for $\sigma(1),$ then $n-1$ choices left for $\sigma(2),$ and so on until only one choice remains for the last image. The order of $S_n$ is therefore the factorial of $n:$

$$
\begin{align}
|S_n| &= n(n-1)\cdots 1 = n! \tag{2}
\end{align}
$$

By $(2),$ the groups $S_1$ and $S_2$ have one and two elements, respectively, and composition is commutative in both because each has at most one element other than the identity. To see whether the same property holds in $S_3,$ we compare the two orders of composition for the following permutations, written in the notation of $(1):$

$$
\begin{align}
\sigma &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 3 & 1 \end{pmatrix} \tag{3a} \\[6pt]
\tau &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 1 & 3 \end{pmatrix} \tag{3b}
\end{align}
$$

Composing the permutations in $(3a)$ and $(3b)$ in the two possible orders gives $(\sigma \circ \tau)(1) = \sigma(2) = 3$ and $(\tau \circ \sigma)(1) = \tau(2) = 1.$ Computing the images of $2$ and $3$ in the same way gives the two products in full:

$$
\begin{align}
\sigma \circ \tau &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 3 & 2 & 1 \end{pmatrix} \tag{4a} \\[6pt]
\tau \circ \sigma &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 1 & 3 & 2 \end{pmatrix} \tag{4b}
\end{align}
$$

Since the two products send $1$ to different elements, the permutations $\sigma$ and $\tau$ do not commute. Thus $S_3$ is nonabelian. For $n \gt 3,$ the same counterexample extends to $S_n$ by fixing the elements from $4$ to $n,$ so $S_n$ is nonabelian for every $n \geq 3.$

## Cycle notation and the order of a permutation

Cycle notation expresses a permutation in terms of cycles. To write a cycle, choose an element and list the elements encountered before returning to the starting point. For example, in $(3a)$ we can write $\sigma = (1\ 2\ 3)$ because the successive images of $1$ follow this sequence:

$$1 \mapsto 2 \mapsto 3 \mapsto 1$$

In general, given $k$ distinct elements of $X_n,$ the cycle $(a_1\ a_2\ \cdots\ a_k)$ sends each element in the list to the next and the last to the first, fixing all other elements. The length of the cycle is $k.$ Any of its elements can be chosen as the starting point, so the following expressions denote the same cycle:

$$
\begin{align}
\sigma &= (1\ 2\ 3) \notag \\[6pt]
       &= (2\ 3\ 1) \notag \\[6pt]
       &= (3\ 1\ 2) \notag
\end{align}
$$

A transposition is a cycle of length $2$ that interchanges two elements. In $(3b),$ the permutation $\tau$ interchanges $1$ and $2$ and fixes $3,$ so we write it as $(1\ 2).$ Both products are also transpositions, since $\sigma \circ \tau$ interchanges $1$ and $3$ in $(4a),$ while $\tau \circ \sigma$ interchanges $2$ and $3$ in $(4b).$

$$
\begin{align}
\sigma &= (1\ 2\ 3) & \tau &= (1\ 2) \tag{6a} \\[6pt]
\sigma \circ \tau &= (1\ 3) & \tau \circ \sigma &= (2\ 3) \tag{6b}
\end{align}
$$

For any permutation $\pi \in S_n,$ repeatedly applying it to an element eventually brings that element back to its starting point because $X_n$ is finite and $\pi$ is injective. Once a cycle is complete, we start again with an element not yet listed and continue until every element of $X_n$ has been listed. The resulting cycles are disjoint, and their product equals $\pi$ because the two agree on every element. The decomposition into disjoint cycles is therefore unique up to the order of the factors, which commute because each fixes the elements moved by the others. In the following permutation of $X_6,$ we can therefore write the two transpositions in either order:

$$
\begin{align}
\rho &= \begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6 \\[6pt]
3 & 5 & 1 & 4 & 2 & 6
\end{pmatrix} \notag \\[6pt]
&= (1\ 3)(2\ 5) = (2\ 5)(1\ 3) \tag{7}
\end{align}
$$

By convention, the cycle notation in $(7)$ omits cycles of length $1,$ in this case $(4)$ and $(6).$

- - -

In $(2)$ we found the order of $S_n$ by counting its permutations. In general, the order of an individual permutation $\sigma \in S_n$ is the least integer $j \geq 1$ for which $\sigma^j$ is the identity. To find this minimum, we must determine how many applications of $\sigma$ it takes for all elements to return to their starting points. In a cycle of length $k,$ each element advances one position with each application, so after $j$ steps it is back at its starting point if and only if $k$ divides $j.$ If the disjoint cycles of $\sigma$ have lengths $k_1, \ldots, k_m,$ the smallest positive exponent for which all elements return to their starting points simultaneously is the least common multiple of the cycle lengths:

$$
\begin{align}
\mathrm{ord}(\sigma) &= \mathrm{lcm}(k_1, \ldots, k_m) \tag{8}
\end{align}
$$

Applying $(8)$ to the permutation $(1\ 2)(3\ 4\ 5) \in S_5$ gives:

$$
\begin{align}
\mathrm{ord}\bigl((1\ 2)(3\ 4\ 5)\bigr) &= \mathrm{lcm}(2,3) = 6 \tag{8a}
\end{align}
$$

In six steps, the first cycle completes three full turns and the second completes two.

## The sign of a permutation and the alternating group

The permutation $(1\ 2)(3\ 4\ 5)$ in $(8a)$ can be written as $(1\ 2)(3\ 5)(3\ 4).$ Can it also be written as a product of an even number of transpositions? To answer this question, we start by expressing a cycle of length $k \geq 2$ as a product of $k-1$ transpositions:

$$
\begin{align}
(a_1\ a_2\ \cdots\ a_k) &= (a_1\ a_k) \cdots (a_1\ a_2) \tag{9}
\end{align}
$$

To determine the parity, let $c(\pi)$ denote the number of disjoint cycles of $\pi,$ including those of length $1.$ In the product $\pi \circ (a\ b),$ the images of $a$ and $b$ are interchanged. If the two elements belong to different cycles, those cycles merge, whereas a cycle containing both elements splits in two. The number of cycles therefore changes parity at each step. Since the identity has $n$ cycles, the following holds for any product $\sigma$ of $m$ transpositions:

$$
\begin{align}
m &\equiv n-c(\sigma) \pmod{2} \tag{10}
\end{align}
$$

By $(10),$ the parity of $m$ depends only on $\sigma,$ so we can define the sign of $\sigma$ by setting $\mathrm{sgn}(\sigma)=(-1)^m,$ so that a permutation is even if its sign is $1$ and odd if its sign is $-1.$ Every decomposition of the permutation in $(8a)$ into transpositions therefore has an odd number of factors, while by $(9)$ a cycle of length $k$ has sign $(-1)^{k-1}.$

If $\sigma$ and $\tau$ are products of $p$ and $q$ transpositions, respectively, their decompositions give $p+q$ factors for $\sigma \circ \tau,$ so the sign function $\mathrm{sgn}$ is a homomorphism:

$$
\begin{align}
\mathrm{sgn}(\sigma \circ \tau) &= (-1)^{p+q} \notag \\[6pt]
&= \mathrm{sgn}(\sigma)\mathrm{sgn}(\tau) \tag{11}
\end{align}
$$

For $n \geq 2,$ this homomorphism from $S_n$ to the multiplicative group $\{1,-1\}$ is surjective because the identity has sign $1$ and a transposition has sign $-1.$

- - -

We now turn to the alternating group $A_n,$ which consists of the even permutations in $S_n.$ Since these are precisely the permutations that the sign homomorphism in $(11)$ sends to $1,$ the alternating group is its kernel and hence a normal subgroup of $S_n.$ For $n \geq 2,$ fix the transposition $\tau = (1\ 2).$ For every $\sigma \in S_n,$ the sign of the product $\tau \circ \sigma$ is the opposite of the sign of $\sigma$ because the factor $\mathrm{sgn}(\tau)$ in $(11)$ equals $-1.$ Composing on the left with $\tau$ a second time gives back $\sigma.$ The odd permutations therefore form the coset $\tau A_n,$ and there are as many odd permutations as even ones. This coset is not a subgroup because the identity is even. Since $A_n$ and $\tau A_n$ together make up $S_n,$ we obtain the following from $(2):$

$$
\begin{align}
[S_n : A_n] &= 2 \tag{12a} \\[6pt]
|A_n| &= \frac{|S_n|}{2} = \frac{n!}{2} \tag{12b}
\end{align}
$$

By $(12b),$ the group $A_3$ has order $3.$ The cycle $(1\ 2\ 3)$ in $(6a)$ is even and has order $3,$ so it generates all of $A_3:$

$$
\begin{align}
A_3 &= \langle (1\ 2\ 3) \rangle = \{\mathrm{id}, (1\ 2\ 3), (1\ 3\ 2)\} \tag{13}
\end{align}
$$

## Conjugation and cycle type

Fix a permutation $\pi \in S_n$ and define conjugation by $\pi$ to be the map that sends each $\sigma \in S_n$ to the following permutation:

$$\pi\sigma\pi^{-1} \tag{14}$$

Two permutations $\sigma$ and $\tau$ are conjugate in $S_n$ if there is a permutation $\pi \in S_n$ for which the following relation holds:

$$\tau = \pi\sigma\pi^{-1} \tag{15}$$

If $\sigma(a)=b,$ it follows that $\tau(\pi(a))=\pi(\sigma(a))=\pi(b).$ Thus, in a cycle $c=(a_1\ a_2\ \cdots\ a_k),$ conjugation replaces each label $a_i$ with $\pi(a_i),$ as shown in $(14a).$

$$
\begin{align}
\pi c\pi^{-1} &= (\pi(a_1)\ \pi(a_2)\ \cdots\ \pi(a_k)) \tag{14a} \\[6pt]
(2\ 3)(1\ 2\ 3)(2\ 3) &= (1\ 3\ 2) \tag{14b}
\end{align}
$$

We now introduce the cycle type of a permutation, the list of the lengths of its disjoint cycles in decreasing order, counting fixed points as cycles of length $1.$ By $(14a),$ conjugation preserves cycle type. Conversely, if two permutations have the same cycle type, we pair up cycles of equal length, including the fixed points. After choosing a starting point in each cycle, we map its elements in order to the corresponding elements of the paired cycle. Together these assignments define a permutation $\pi$ on all of $X_n$ that conjugates the first permutation to the second by $(14a).$

The conjugacy classes of $S_n$ therefore correspond to the partitions of $n,$ since the cycle lengths sum to $n$ and every partition can be realized by disjoint cycles of those lengths. In $S_4,$ the five classes contain a total of $24$ permutations.

| Cycle type | Permutations | Number |
| --- | --- | ---: |
| $(4)$ | Cycles of length $4$ | $6$ |
| $(3,1)$ | Cycles of length $3$ | $8$ |
| $(2,2)$ | Products of two disjoint transpositions | $3$ |
| $(2,1,1)$ | Transpositions | $6$ |
| $(1,1,1,1)$ | Identity | $1$ |

By $(8),$ the permutations $(1\ 2)$ and $(1\ 2)(3\ 4)$ in $S_4$ both have order $2.$ Their cycle types are $(2,1,1)$ and $(2,2),$ respectively, so the two permutations are not conjugate.