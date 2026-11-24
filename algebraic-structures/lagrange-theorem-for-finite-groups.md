---
title: Lagrange's Theorem for Finite Groups
source: https://algebrica.org/lagrange-theorem-for-finite-groups/
license: CC BY-NC 4.0
tags:
  - coset
  - finite-group
  - group-theory
  - lagrange-theorem
  - subgroup
  - subgroup-index
---

## Statement

Lagrange's theorem for finite groups states that for any [finite group](../groups/) $G,$ the order of each subgroup $H$ divides the order of $G$ and the quotient is the index $[G : H],$ the number of distinct left cosets of $H$ in $G.$ A left coset of $H$ is obtained by fixing an element $a \in G$ and multiplying each element of $H$ on the left by $a$ to form the following set of products:

$$aH = \{ah \mid h \in H\} \tag{1}$$

For example, in the additive group $\mathbb{Z}/6\mathbb{Z},$ the subgroup $H = \{0, 2, 4\}$ has two cosets. The first is $H$ itself, and the second is $1 + H = \{1, 3, 5\}.$ Lagrange's theorem thus gives the following identity:

$$|G| = [G : H]|H| \tag{2}$$

To prove $(2),$ we need to show that each left coset of $H$ contains $|H|$ elements and that the distinct cosets form a [partition](../sets/) of $G.$ For the first claim, fix $a \in G.$ The map $h \mapsto ah$ is a [bijection](../injective-surjective-and-bijective-functions/) from $H$ to $aH,$ since its [inverse](../inverse-function/) sends each $x \in aH$ to $a^{-1}x \in H.$ It follows that:

$$|aH| = |H| \tag{3}$$

For the second claim, each $a \in G$ belongs to $aH$ because $a = ae$ and $e \in H.$ To show that distinct cosets are disjoint, suppose that $aH$ and $bH$ have an element in common. We can write this element both as $ah_1$ and as $bh_2,$ with $h_1, h_2 \in H.$ Multiplying both sides of $ah_1 = bh_2$ on the left by $b^{-1}$ and on the right by $h_1^{-1}$ gives the following identity:

$$b^{-1}a = h_2h_1^{-1} \in H \tag{4}$$

In particular, $(4)$ holds if $aH = bH,$ since both cosets then contain $a.$ Conversely, if $k = b^{-1}a$ belongs to $H,$ left multiplication by $k$ is a bijection from $H$ to itself, so $kH = H.$ Since $a = bk,$ it follows that $aH = b(kH) = bH.$ Thus membership of $b^{-1}a$ in $H$ is necessary and sufficient for the two cosets to be equal, giving the following criterion:

$$aH = bH \iff b^{-1}a \in H \tag{5}$$

If two cosets have an element in common, they satisfy $(4)$ and hence are equal by $(5).$ Distinct cosets are therefore disjoint, and since there are $[G : H]$ of them by definition of the index and each contains $|H|$ elements by $(3),$ counting the elements of $G$ gives $(2)$ and completes the proof.

By $(2),$ if $G$ contains a subgroup of order $d,$ then $d$ divides $|G|.$ Conversely, one may ask whether every [divisor](../integers/) of $|G|$ is the order of a subgroup of $G.$ The [alternating group](../symmetric-group/) $A_4,$ consisting of the even permutations of four elements, provides a counterexample. It has order $12,$ and although $6$ divides $12,$ none of its subgroups has order $6.$

- - -

Lagrange's theorem relates the order of each subgroup to the order of $G.$ This relation extends to individual elements, since the order of an element $a \in G$ equals the order of the cyclic subgroup it generates. If we denote this order by $d$ and set $H = \langle a \rangle$ in $(2),$ we obtain

$$|G| = [G : \langle a \rangle]d \tag{6}$$

Equation $(6)$ shows that the order of $a$ divides the order of $G.$ If $k$ denotes the index $[G : \langle a \rangle],$ we can therefore write $|G| = kd,$ and since $a^d = e$ by the definition of order, it follows that:

$$a^{|G|} = (a^d)^k = e \tag{7}$$

Equation $(7)$ holds for every element of $G.$ A group has prime order if it has a prime number $p$ of elements. In this case, $(6)$ shows that the order of each element divides $p,$ so it can only be $1$ or $p.$ Since only the identity has order $1,$ every $a \neq e$ has order $p$ and generates a subgroup containing all $p$ elements of $G.$ It follows that $G$ is cyclic and [isomorphic](../homomorphisms-and-isomorphisms/) to the additive group $\mathbb{Z}/p\mathbb{Z}.$
