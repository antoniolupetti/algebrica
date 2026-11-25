---
title: Subgroups
source: https://algebrica.org/subgroups/
license: CC BY-NC 4.0
tags:
  - algebraic-structures
  - cyclic-subgroup
  - finite-group
  - generated-subgroup
  - group-theory
  - subgroup
---

## Definition and properties

Given a [group](../groups/) $G,$ a [subset](../sets/) $H \subseteq G$ is a subgroup of $G$ if it is itself a group under the operation of $G$ restricted to $H.$ We then write $H \leq G.$ Let us examine the properties that a subset $H$ must satisfy to be a subgroup. Associativity holds for every triple of elements of $G,$ so it still holds when all three elements belong to $H.$ As for the identity element $e,$ we can show that the identity of a subgroup must coincide with $e.$ Indeed, if $u$ is the identity of $H,$ then $uu=u$ in $H$ and $ue=u$ in $G.$ Since the operation is the same, $uu=ue$ implies $u=e.$ The inverse of each $a \in H$ also coincides with its inverse in $G,$ since in both groups it is the unique solution of the equation $ax=e.$

To determine whether a subset is a subgroup, we can therefore use the identity and inverses in $G$ to check the following necessary and sufficient conditions:

$$
\begin{align}
&e \in H \tag{1a} \\[6pt]
&ab \in H \qquad \forall \ a,b \in H \tag{1b} \\[6pt]
&a^{-1} \in H \qquad \forall a \in H \tag{1c}
\end{align}
$$

Every group $G$ is a subgroup of itself and contains the trivial subgroup $\{e\},$ which consists of the identity alone. A subgroup is called proper if it is different from $G.$ In particular, if $G$ has more than one element, $\{e\}$ is itself a proper subgroup.

For a nonempty subset $H \subseteq G,$ the three conditions above can be combined into a single test:

$$
\begin{align}
H \leq G \quad &\Longleftrightarrow \quad \bigl(\forall a,b \in H,\ ab^{-1} \in H\bigr) \tag{2}
\end{align}
$$

If $H$ is a subgroup and $a,b \in H,$ then $b^{-1}$ also belongs to $H$ by $(1\mathrm{c}),$ and applying $(1\mathrm{b})$ to $a$ and $b^{-1}$ gives $ab^{-1} \in H.$ For the converse, suppose that $xy^{-1} \in H$ for every $x,y \in H.$ Given $a,b \in H,$ we apply this assumption in turn to the pairs $(a,a),$ $(e,b)$ and $(a,b^{-1}).$ This gives $e \in H,$ $b^{-1} \in H$ and $ab \in H,$ respectively, so $H$ satisfies all three subgroup conditions.

- - -

We can now use $(2)$ to determine whether the multiples of an [integer](../integers/) $n \geq 1$ form a subgroup of $(\mathbb{Z},+).$ In this group the operation is addition and the inverse of $b$ is its negative $-b,$ so the expression $ab^{-1}$ in $(2)$ becomes $a+(-b)=a-b.$ The set $n\mathbb{Z}$ of multiples of $n$ contains zero, so it remains to check that the difference of two multiples of $n$ is again a multiple of $n.$ We write two arbitrary multiples as $nr$ and $ns,$ with $r,s \in \mathbb{Z},$ and factor $n$ out of their difference:

$$
\begin{align}
nr-ns &= n(r-s) \in n\mathbb{Z} \tag{3}
\end{align}
$$

Since $r-s$ is an integer, $(3)$ shows that the difference belongs to $n\mathbb{Z}.$ By $(2),$ it follows that $n\mathbb{Z}$ is a subgroup of $(\mathbb{Z},+).$ Taking $n=2$ gives the subgroup of even integers.

- - -

Finally, let us see why it is enough to check closure under multiplication when $H$ is finite and nonempty. Fix $a \in H.$ The products $ax$ with $x \in H$ belong to $H$ by closure and are all distinct by the [cancellation law](../groups/). Since $H$ is finite, these products exhaust $H,$ so one of them is $a,$ and $ax=a$ implies $x=e \in H.$ The identity $e$ is therefore also among the products, and $ay=e$ implies $y=a^{-1} \in H.$ This argument applies to every $a \in H,$ so $H$ is a subgroup.

We apply this test to the [symmetric group](../symmetric-group/) $S_4,$ which consists of the permutations of $\{1,2,3,4\}$ under composition. Consider the set $H$ of permutations that fix $4,$ so the other three elements can be permuted freely. The number of elements of $H$ is therefore the [factorial](../factorial/) $3!=6.$ If we apply two permutations in $H$ in succession, the first sends $4$ to $4$ and the second does the same. Their composition therefore belongs to $H,$ and since $H$ is finite and nonempty, closure suffices to show that $H$ is a subgroup of $S_4.$ Moreover, the subgroup is proper because the transposition that interchanges $3$ and $4$ belongs to $S_4$ and moves $4.$

## Intersection and union of subgroups

We now consider two subgroups $H$ and $K$ of the same group $G$ and prove that their [intersection](../sets/) is a subgroup. Since both contain $e,$ their intersection is nonempty. If $a,b \in H \cap K,$ we can apply $(2)$ first in $H$ and then in $K.$ The product $ab^{-1}$ therefore belongs to both subgroups, so it belongs to $H \cap K.$ By $(2),$ this proves that $H \cap K \leq G.$

The same argument applies to the intersection of any nonempty family of subgroups of $G,$ even if the family is infinite. The identity belongs to every subgroup in the family, and if $a$ and $b$ belong to all of them, so does $ab^{-1}.$ For example, the elements of $4\mathbb{Z} \cap 6\mathbb{Z}$ are the integers divisible by both $4$ and $6,$ and since the least common multiple of $4$ and $6$ is $12,$ we obtain $4\mathbb{Z} \cap 6\mathbb{Z}=12\mathbb{Z}.$

Consider now the [union](../sets/) of the same two subgroups, $4\mathbb{Z} \cup 6\mathbb{Z},$ which contains $4$ and $6$ but does not contain their sum $10.$ In general, the union of two subgroups $H$ and $K$ of $G$ is a subgroup of $G$ if and only if one is contained in the other, as expressed by the following equivalence:

$$
\begin{align}
H \cup K \leq G \quad &\Longleftrightarrow \quad (H \subseteq K) \lor (K \subseteq H) \tag{4}
\end{align}
$$

If one subgroup contains the other, their union is the larger subgroup. Otherwise, choose $h \in H \setminus K$ and $k \in K \setminus H.$ If $hk$ belonged to $H,$ then $k=h^{-1}(hk)$ would also belong to $H.$ If it belonged to $K,$ then $h=(hk)k^{-1}$ would also belong to $K.$ Both conclusions contradict the choice of $h$ and $k.$ The union is therefore not closed under multiplication, which proves $(4).$

## Subgroup generated by a set

How can we identify the smallest subgroup containing given elements? In general, given a subset $S \subseteq G,$ we take all the subgroups of $G$ that contain $S,$ and since at least $G$ itself is among them, we can apply the result on intersections. The resulting subgroup is called the subgroup generated by $S$ and is denoted as follows:

$$
\begin{align}
\langle S \rangle &= \bigcap_{\substack{H \leq G \\ S \subseteq H}} H \tag{5}
\end{align}
$$

Every element of $S$ belongs to all the subgroups in $(5)$ and therefore also belongs to $\langle S \rangle.$ Indeed, the intersection is contained in each of these subgroups, and in this sense $\langle S \rangle$ is the smallest subgroup with respect to inclusion.

To describe the elements of the subgroup defined in $(5),$ let $P$ be the set of all finite products of elements of $S$ and their inverses, including the empty product $e.$ Every subgroup containing $S$ contains all these products, so $P \subseteq \langle S \rangle.$

For the reverse inclusion, observe that multiplying two products in $P$ gives a single product of the same form. The inverse of such a product also belongs to $P,$ since we obtain it by reversing the order of the factors and replacing each factor with its inverse. Since $e \in P,$ it follows that $P$ is a subgroup. Moreover, every element of $S$ is a product with a single factor, so $P$ contains $S.$ By $(5),$ we therefore have $\langle S \rangle \subseteq P,$ which proves that $\langle S \rangle = P.$ In the special case $S=\{g\},$ these products are the integer powers of $g$ and form the [cyclic subgroup](../cyclic-groups/) $\langle g \rangle = \{g^k \mid k \in \mathbb{Z}\}.$

Let us return to the integers $4$ and $6$ considered above. In additive notation, products become sums and inverses become negatives, so $\langle 4,6 \rangle$ consists of the integers of the form $4m+6n,$ with $m,n \in \mathbb{Z}.$ To compare this subgroup with $2\mathbb{Z},$ we use two identities that hold for all $m,n,k \in \mathbb{Z}:$

$$
\begin{align}
4m+6n &= 2(2m+3n) \tag{6a} \\[6pt]
2k &= 4(-k)+6k \tag{6b}
\end{align}
$$

Equation $(6\mathrm{a})$ shows that every sum $4m+6n$ is even, while $(6\mathrm{b})$ expresses every even integer as a sum of this form. Thus $\langle 4,6 \rangle = 2\mathbb{Z},$ meaning that the even integers form the smallest subgroup of $(\mathbb{Z},+)$ containing both $4$ and $6.$ For example, $2$ does not belong to the union $4\mathbb{Z} \cup 6\mathbb{Z},$ but it must belong to the generated subgroup because $2=6-4.$
