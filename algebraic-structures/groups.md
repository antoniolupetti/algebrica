---
title: Groups
source: https://algebrica.org/groups/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - associativity
  - cayley-table
  - coset
  - cyclic-group
  - dihedral-group
  - group-theory
  - homomorphism
  - identity-element
  - inverse-element
  - isomorphism
  - klein-four-group
  - lagrange-theorem
  - normal-subgroup
  - subgroup
  - symmetric-group
---
## Definition

A group is a set $G$ together with a binary operation $\cdot : G \times G \to G$ satisfying three axioms:

+ Associativity: for all $a, b, c \in G,$ the identity $(a \cdot b) \cdot c = a \cdot (b \cdot c)$ holds.
+ Identity element: there exists an element $e \in G$ such that $a \cdot e = e \cdot a = a$ for all $a \in G.$
+ Inverses: for every $a \in G$ there exists an element $a^{-1} \in G$ such that $a \cdot a^{-1} = a^{-1} \cdot a = e.$

The [integers](../integers/) under addition, the nonzero [real numbers](../real-numbers/) under multiplication, the symmetries of a fixed geometric object under composition, such as the [dihedral group](../dihedral-groups/) of a regular polygon, and invertible [matrices](../matrices/) of a fixed size under multiplication are examples of groups.

> Many treatments list closure as a further axiom, requiring that $a \cdot b$ belong to $G$ for all $a, b \in G.$ Here the operation has codomain $G,$ so its definition already includes closure. Closure must be checked when determining whether a subset is a subgroup, since the subset need not contain the products of its elements.

- - -

A group $(G, \cdot)$ is abelian, or commutative, if $a \cdot b = b \cdot a$ for all $a, b \in G.$

The identity element is unique, as is the inverse of each element. Suppose $e$ and $e'$ both satisfy the identity axiom. Then $e = e \cdot e'$ because $e'$ is an identity, and $e \cdot e' = e'$ because $e$ is an identity, so $e = e'.$ For inverses, suppose $h \cdot a = e$ for some $h \in G$:

$$h = h \cdot e = h \cdot (a \cdot a^{-1}) = (h \cdot a) \cdot a^{-1} = e \cdot a^{-1} = a^{-1}$$

If $a \cdot h = e,$ the symmetric computation gives the same conclusion. Thus every one-sided inverse of $a$ is $a^{-1}.$

## Properties

For $a \in G,$ the maps $L_a(x) = a \cdot x$ and $R_a(x) = x \cdot a$ are left and right multiplication by $a.$ The composition of $L_a$ with $L_{a^{-1}}$ satisfies:

$$L_{a^{-1}}(L_a(x)) = a^{-1} \cdot (a \cdot x) = (a^{-1} \cdot a) \cdot x = e \cdot x = x$$

The same computation in the opposite order shows that $L_a$ and $L_{a^{-1}}$ are inverse maps, so both are bijections from $G$ to itself. The same argument applies to $R_a.$

Since $L_a$ is injective, $a \cdot b = a \cdot c$ implies $b = c.$ This is the left cancellation law, while the injectivity of $R_a$ gives the right cancellation law. Since $L_a$ is bijective, the equation $a \cdot x = b$ has the unique solution $x = a^{-1} \cdot b$ for every $b \in G.$ Similarly, $x \cdot a = b$ has the unique solution $x = b \cdot a^{-1}.$

For a finite group these bijections constrain its multiplication table, or Cayley table. Its rows and columns are indexed by the elements of $G,$ and its entry in position $(a, b)$ is the product $a \cdot b.$ The row indexed by $a$ lists the values of $L_a,$ and the column indexed by $a$ lists the values of $R_a.$ Both maps are bijections, so each element of $G$ occurs exactly once in every row and column. Thus a Cayley table is a Latin square.

> The converse fails because a Latin square need not satisfy associativity. Latin squares are the multiplication tables of finite quasigroups. In a quasigroup, the equations $a \cdot x = b$ and $y \cdot a = b$ have unique solutions, but the operation need not be associative.

- - -

The inverse of a product has its factors in reverse order:

$$(a \cdot b)^{-1} = b^{-1} \cdot a^{-1}$$

This identity follows from associativity and is sometimes called the "sock-shoe" property. To undo the operation of first putting on a sock and then a shoe, one must first remove the shoe and then the sock. Since $a$ is the inverse of $a^{-1},$ applying inversion twice gives $(a^{-1})^{-1} = a.$

The order of a group $G,$ denoted $|G|,$ is the cardinality of its underlying set. A group with finitely many elements is finite; otherwise it is infinite.

## Algebraic hierarchy

Groups, [rings](../rings/), and [fields](../fields/) can be compared by their operations and inverses:

+ A group has one associative operation, an identity element, and an inverse for every element.
+ A ring has addition and multiplication. Addition makes the ring an abelian group, while multiplication is associative and distributes over addition.
+ A field is a commutative ring in which every nonzero element has a multiplicative inverse.

> The integers $\mathbb{Z}$ are a ring but not a field, while the [rational numbers](../rational-numbers/) $\mathbb{Q}$ are a field. A [vector space](../vector-spaces/) has scalars in a field, while a [module](../modules/) has scalars in a ring.

## Powers of an element

A power is a product of equal factors, so a product of more than two factors must first be defined. For three factors, associativity states that the two possible groupings are equal. Four factors have five groupings, and repeated use of associativity shows that all five are equal:

$$a(b(cd)) = a((bc)d) = (ab)(cd) = (a(bc))d = ((ab)c)d$$

For every $n \geq 1,$ associativity makes every parenthesization of $a_1a_2 \cdots a_n$ equal. A proof by [induction](../principle-of-mathematical-induction/) on $n$ splits any parenthesized product into a product of $k$ factors and a product of $n - k$ factors. The induction hypothesis fixes the value of both shorter products, and associativity shows that this value is independent of $k.$ This result is the general associative law and allows products of several factors to be written without parentheses.

For an element $a \in G$ and a positive integer $n,$ define its powers recursively by $a^1 = a$ and $a^n = a^{n-1} \cdot a.$ For positive $n,$ the remaining powers are:

$$a^0 = e \qquad a^{-n} = (a^{-1})^n$$

For all integers $m$ and $n,$ these powers satisfy:

$$a^m \cdot a^n = a^{m+n} \qquad (a^m)^n = a^{mn}$$

Induction on the exponents proves both identities from the recursive definition. In additive notation, the power $a^n$ becomes the multiple $na,$ and the identities become $ma + na = (m + n)a$ and $n(ma) = (mn)a.$

> If $a$ and $b$ commute, then $(a \cdot b)^n = a^n \cdot b^n$ for every integer $n.$ Without the commutativity hypothesis, this identity can fail.

## Examples

Under ordinary addition, $\mathbb{Z}$ is an infinite abelian group. Its identity element is $0,$ and the inverse of an integer $n$ is $-n.$

Let $n$ be a positive integer. With addition [modulo](../modulo-operator/) $n,$ the set $\mathbb{Z}/n\mathbb{Z} = \{\ 0, 1, \ldots, n - 1 \ \}$ is a finite abelian group of order $n.$ For example, in $\mathbb{Z}/5\mathbb{Z}$ one has $3 + 4 = 2,$ since $7 \equiv 2 \pmod{5}.$ The identity element is $0,$ and the inverse of the residue $k$ is the residue $-k.$

Not every finite group has this form. Up to isomorphism, there are exactly two groups of order $4.$ One is $\mathbb{Z}/4\mathbb{Z}.$ The other is the Klein four-group $V,$ whose elements are the identity $e$ and three elements $a, b, c$ satisfying $a^2 = b^2 = c^2 = e.$ The product of any two distinct nonidentity elements is the third. The groups are not isomorphic, since every element of $V$ satisfies $x^2 = e,$ while a generator of $\mathbb{Z}/4\mathbb{Z}$ does not. A rectangle with unequal side lengths gives a geometric realization of $V,$ which is the [dihedral group](../dihedral-groups/) $D_2.$ Its elements are the identity symmetry and the half-turns about the two symmetry axes in its plane and the axis perpendicular to its plane. Each half-turn has order $2,$ and the product of any two distinct half-turns is the third. The residues $\{\ 1, 3, 5, 7 \ \}$ under multiplication modulo $8$ give another realization, since each residue squares to $1.$ The group $V$ is the smallest noncyclic group.

- - -

Let $F$ be a [field](../fields/) and let $n$ be a positive integer. The general linear group $\mathrm{GL}(n, F)$ has the [invertible](../inverse-matrix/) $n \times n$ matrices over $F$ as its elements and matrix multiplication as its operation. Its identity element is the identity matrix $I_n,$ and the inverse of $A$ is $A^{-1}.$ For $n \geq 2,$ this group is not abelian because matrix multiplication need not commute.

A permutation of $\{\ 1, 2, \ldots, n \ \}$ is a bijection from this set to itself. The [symmetric group](../symmetric-group/) $S_n$ has these permutations as its elements and [composition of functions](../composite-functions/) as its operation. Its identity element is the identity permutation, and the inverse of a permutation $\sigma$ is the inverse function $\sigma^{-1}.$ The group has order $n!,$ the [factorial](../factorial/) of $n,$ and is non-abelian for $n \geq 3.$

The group $S_3$ is the smallest non-abelian symmetric group and has order $6.$ Let $\sigma$ be the permutation sending $1 \mapsto 2,$ $2 \mapsto 3,$ $3 \mapsto 1,$ and let $\tau$ be the permutation exchanging $1$ and $2$ while fixing $3$:

$$\sigma = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 3 & 1 \end{pmatrix} \qquad \tau = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 1 & 3 \end{pmatrix}$$

The two compositions satisfy $\sigma \circ \tau \neq \tau \circ \sigma.$ The page on the [symmetric group](../symmetric-group/) gives the computation and develops the theory of permutations.

The symmetries of a regular $n$-gon are a further family of finite groups. For $n \geq 3$ they consist of $n$ rotations about the centre and $n$ reflections in axes through the centre, so the group has order $2n.$ It is the [dihedral group](../dihedral-groups/) $D_n,$ and it is non-abelian for every $n \geq 3,$ since a rotation and a reflection commute only when the rotation is the identity or the half-turn. The smallest case $D_3$ has order $6$ and is isomorphic to $S_3,$ because every permutation of the three vertices of an equilateral triangle comes from a symmetry.

## When the axioms fail

The following set-operation pairs are associative and have an identity element, but some of their elements have no inverse.

Consider the [natural numbers](../natural-numbers/) including zero, $\mathbb{N}_0 = \{\ 0, 1, 2, \ldots \ \},$ under ordinary addition. The operation is closed and associative, and $0$ is an identity element. No positive integer $n$ has an additive inverse in $\mathbb{N}_0,$ because $-n$ is outside the set. Thus $(\mathbb{N}_0, +)$ is a monoid but not a group.

Multiplication on the [integers](../integers/) is closed and associative and has identity $1,$ but only $1$ and $-1$ have multiplicative inverses in $\mathbb{Z}.$ For any other integer $n,$ the reciprocal $1/n$ is not an integer. Removing the noninvertible elements leaves the group $\{\ 1, -1 \ \}$ under multiplication.

Every nonzero [real number](../real-numbers/) has a multiplicative inverse, but zero does not. Thus $(\mathbb{R}, \cdot)$ is not a group. Removing zero gives the abelian group $\mathbb{R} \setminus \{\ 0 \ \}$ under multiplication, with identity $1$ and inverse $a^{-1} = 1/a$ for every $a \neq 0.$

## Subgroups

A subset $H$ of a group $G$ is a subgroup if $H$ is a group under the operation inherited from $G.$ The following criterion avoids checking each group axiom separately.

A nonempty subset $H \subseteq G$ is a subgroup of $G$ if and only if $a \cdot b^{-1}$ belongs to $H$ for all $a, b \in H.$ Setting $a = b$ shows that $e \in H.$ Setting $a = e$ then shows that $b^{-1} \in H,$ and replacing $b$ by $b^{-1}$ shows that $a \cdot b \in H.$ The notation $H \leq G$ means that $H$ is a subgroup of $G.$

Every group $G$ has the trivial subgroup $\{\ e \ \}$ and the subgroup $G$ itself. These subgroups coincide when $G = \{\ e \ \}.$ A subgroup different from $G$ is a proper subgroup.

The even integers $2\mathbb{Z} = \{\ \ldots, -4, -2, 0, 2, 4, \ldots \ \}$ are a subgroup of $(\mathbb{Z}, +).$ For $a = 2m$ and $b = 2k,$ the inverse of $b$ is $-b = -2k,$ and $a + (-b) = 2(m - k)$ is even. Thus $2\mathbb{Z}$ satisfies the subgroup criterion.

Intersections of subgroups are subgroups. If $H$ and $K$ are subgroups of $G,$ then the identity belongs to $H \cap K,$ and $a, b \in H \cap K$ implies $a \cdot b^{-1} \in H \cap K.$ The same argument applies to any nonempty family of subgroups.

Given a subset $S \subseteq G,$ consider the family of all subgroups of $G$ that contain $S.$ This family contains $G,$ so it is nonempty. Its intersection is a subgroup that contains $S$ and is contained in every other subgroup containing $S.$ It is the subgroup generated by $S,$ written $\langle S \rangle.$

Equivalently, $\langle S \rangle$ consists of the identity and all finite products $g_1g_2 \cdots g_n$ in which each $g_i$ belongs to $S$ or is the inverse of an element of $S.$ Concatenating two lists of factors gives the product of their elements, while reversing a list and inverting each factor gives the inverse. Hence this set is a subgroup containing $S.$ Every subgroup containing $S$ contains all these products, so the set is $\langle S \rangle.$ When $\langle S \rangle = G,$ the set $S$ is a set of generators of $G,$ and $G$ is generated by $S.$

An element $a \in G$ is central if it commutes with every $g \in G.$ The centre of $G$ is the set of its central elements:

$$Z(G) = \{\ a \in G : a \cdot g = g \cdot a \ \text{ for all } g \in G \ \}$$

The identity is in $Z(G),$ and if $a$ and $b$ commute with every element of $G,$ then so do $a \cdot b$ and $a^{-1}.$ Thus the centre is a subgroup. A group is abelian exactly when $Z(G) = G.$ For $n \geq 3,$ the centre of $S_n$ is $\{\ e \ \}.$

## Cyclic groups

A group $G$ is cyclic if it has an element $g$ such that every element of $G$ is a power of $g,$ or equivalently, if $G = \langle g \rangle$:

$$G = \{\ g^n : n \in \mathbb{Z} \ \}$$

Such an element $g$ is a generator of $G,$ and a cyclic group has a one-element generating set. Every cyclic group is isomorphic to $\mathbb{Z}$ if it is infinite and to $\mathbb{Z}/n\mathbb{Z}$ for some positive integer $n$ if it is finite.

The group $(\mathbb{Z}/6\mathbb{Z}, +)$ is cyclic with generator $1,$ since every residue is a multiple of $1.$ The element $5$ is also a generator because its multiples modulo $6$ include all six residues. The element $2$ is not a generator because its multiples are $\{\ 0, 2, 4 \ \},$ a proper subgroup of $\mathbb{Z}/6\mathbb{Z}.$

## Order of an element

The order of an element $a$ in a group $G$ is the smallest positive integer $n$ such that $a^n = e,$ where $e$ is the identity element. If no such integer exists, $a$ has infinite order. We write this order as $\mathrm{ord}(a).$

In $(\mathbb{Z}/6\mathbb{Z}, +),$ the element $2$ has order $3,$ since $2 + 2 + 2 = 6 \equiv 0 \pmod{6}$ and neither $2$ nor $2 + 2 = 4$ is congruent to $0.$ The element $1$ has order $6,$ since $6$ is the smallest positive multiple of $1$ congruent to $0$ modulo $6.$ In $(\mathbb{Z}, +),$ every nonzero element has infinite order because no positive multiple of a nonzero integer is $0.$

> The modulo operator $a \bmod n$ is the remainder when $a$ is divided by $n.$ For example, $7 \bmod 5 = 2$ since $7 = 1 \cdot 5 + 2.$ The page on the [modulo operator](../modulo-operator/) gives the general definition.

The order of an element equals the order of the cyclic subgroup it generates. Suppose $a$ has finite order $n.$ The powers $e, a, a^2, \ldots, a^{n-1}$ are pairwise distinct, because $a^i = a^j$ with $0 \leq i < j \leq n - 1$ would give $a^{j-i} = e$ with $0 < j-i < n,$ contrary to the minimality of $n.$ Write an integer $k$ as $k = qn + r,$ where $0 \leq r < n.$ Then $a^k = (a^n)^q \cdot a^r = a^r,$ so these $n$ powers are all the elements of $\langle a \rangle.$ Therefore:

$$\langle a \rangle = \{\ e, a, a^2, \ldots, a^{n-1} \ \} \qquad \mathrm{ord}(a) = |\langle a \rangle|$$

The same division argument shows that $a^k = a^l$ if and only if $k \equiv l \pmod{n}.$ If $a$ has infinite order, all its powers are distinct and $\langle a \rangle$ is infinite. Thus $a$ has infinite order exactly when $\langle a \rangle$ is infinite.

## Cosets and Lagrange's theorem

Let $H$ be a subgroup of $G.$ For $a \in G,$ the set $aH = \{\ a \cdot h : h \in H \ \}$ is a left coset of $H,$ and $Ha$ is a right coset. A coset need not be a subgroup, since $aH$ contains the identity only when $a \in H.$

Two left cosets are equal or disjoint. Suppose $c \in aH \cap bH,$ so $c = a \cdot h_1 = b \cdot h_2$ for some $h_1, h_2 \in H.$ Then $k = b^{-1} \cdot a = h_2 \cdot h_1^{-1}$ belongs to $H,$ and therefore $aH = bkH = bH.$ Hence:

$$aH = bH \iff b^{-1} \cdot a \in H$$

Every element $a$ belongs to $aH,$ so the left cosets cover $G.$ Since distinct left cosets are disjoint, they partition $G.$ All cosets have the same cardinality because $x \mapsto b \cdot a^{-1} \cdot x$ is a bijection from $aH$ to $bH,$ with inverse $y \mapsto a \cdot b^{-1} \cdot y.$

The index of $H$ in $G,$ denoted $[G : H],$ is the number of distinct left cosets of $H.$ If $G$ is finite, the cosets partition $G$ and each has $|H|$ elements. Lagrange's theorem therefore gives:

$$|G| = [G : H] \cdot |H|$$

Thus the order of a subgroup divides the order of the group. For a chain of subgroups $K \leq H \leq G,$ the indices satisfy $[G : K] = [G : H][H : K].$ This identity also holds for infinite groups.

> The index is also defined for infinite groups because it counts cosets rather than elements. The subgroup $n\mathbb{Z}$ has index $n$ in $\mathbb{Z},$ while the cosets of $\mathbb{Z}$ in $\mathbb{R}$ are in bijection with $[0, 1).$ Hence $\mathbb{Z}$ has uncountable index in $\mathbb{R}.$

For every $a \in G,$ Lagrange's theorem shows that $\mathrm{ord}(a)$ divides $|G|,$ since $\mathrm{ord}(a) = |\langle a \rangle|.$ It follows that $a^{|G|} = e.$ If $|G| = p$ is prime, the only possible subgroup orders are $1$ and $p.$ For any $a \neq e,$ the subgroup $\langle a \rangle$ is therefore $G.$ Thus every group of prime order is cyclic and isomorphic to $\mathbb{Z}/p\mathbb{Z}.$

> The converse of Lagrange's theorem fails. A divisor of $|G|$ need not be the order of any subgroup: the alternating group $A_4$ has order $12$ and contains no subgroup of order $6.$

## Normal subgroups

The left and right cosets of a subgroup need not agree. In $S_3,$ the subgroup generated by the transposition exchanging $1$ and $2$ has different left and right cosets, whereas the subgroup $K$ of order $3$ satisfies $aK = Ka$ for every $a \in S_3.$

A subgroup $N \leq G$ is normal if $gNg^{-1} = N$ for every $g \in G,$ where $gNg^{-1}$ is the set of elements $g \cdot n \cdot g^{-1}$ with $n \in N.$ We write $N \trianglelefteq G.$ The element $g \cdot n \cdot g^{-1}$ is the conjugate of $n$ by $g,$ so a normal subgroup is closed under conjugation by every element of $G.$

Equivalently, $N$ is normal if and only if $gN = Ng$ for every $g,$ so its left and right cosets coincide. It is enough to prove $gNg^{-1} \subseteq N$ for every $g \in G.$ Replacing $g$ by $g^{-1}$ gives $g^{-1}Ng \subseteq N,$ which is equivalent to $N \subseteq gNg^{-1}$ and proves the reverse inclusion.

Every subgroup of an abelian group is normal because conjugation fixes each element. The centre $Z(G)$ is normal in any group. A subgroup $H$ of index $2$ is also normal: its left and right cosets are $H$ and its complement, so the two coset decompositions coincide.

If $N$ is normal, the set of cosets $G/N$ is a group under the operation $(aN)(bN) = abN.$ The product does not depend on the representatives of the two cosets. If $N$ is not normal, different representatives can give different products, so this operation is not well defined.

> The [first isomorphism theorem](../homomorphisms-and-isomorphisms/) states that $G/\ker(\varphi) \cong \mathrm{im}(\varphi)$ for every group homomorphism $\varphi.$ Rings, modules, and vector spaces have corresponding theorems.

## Group homomorphisms and isomorphisms

For groups $(G, \cdot)$ and $(H, \star),$ a [function](../functions/) $\varphi : G \to H$ is a homomorphism if for all $a, b \in G$:

$$\varphi(a \cdot b) = \varphi(a) \star \varphi(b)$$

Thus performing the group operation before applying $\varphi$ gives the same result as applying $\varphi$ before the operation. A homomorphism maps the identity of $G$ to the identity of $H$ and satisfies $\varphi(a^{-1}) = \varphi(a)^{-1}$ for all $a \in G.$ If $e_H$ is the identity of $H,$ the [kernel](../homomorphisms-and-isomorphisms/) is:

$$\ker(\varphi) = \{\ a \in G : \varphi(a) = e_H \ \}$$

The image is:

$$\mathrm{im}(\varphi) = \{\ \varphi(a) : a \in G \ \}$$

The kernel is a subgroup of $G,$ and the image is a subgroup of $H.$ A homomorphism is injective if and only if its kernel contains only the identity element of $G.$

More generally, for every subgroup $A \leq G,$ the image $\varphi(A)$ is a subgroup of $H,$ since the product of $\varphi(a_1)$ and $\varphi(a_2)$ is $\varphi(a_1 \cdot a_2)$ and the inverse of $\varphi(a)$ is $\varphi(a^{-1}).$ For every subgroup $B \leq H,$ the preimage $\varphi^{-1}(B) = \{\ a \in G : \varphi(a) \in B \ \}$ is a subgroup of $G,$ even if $\varphi$ is not invertible. Taking $A = G$ gives the image of $\varphi,$ and taking $B = \{\ e_H \ \}$ gives the kernel.

The kernel is normal. For $x \in \ker(\varphi)$ and $g \in G,$ one has:

$$\varphi(g \cdot x \cdot g^{-1}) = \varphi(g) \star \varphi(x) \star \varphi(g)^{-1} = \varphi(g) \star e_H \star \varphi(g)^{-1} = e_H$$

Thus $g \ker(\varphi) g^{-1} \subseteq \ker(\varphi)$ for every $g \in G,$ which proves normality. Conversely, every normal subgroup $N$ is the kernel of a homomorphism, namely the map from $G$ to $G/N$ that sends each element to its coset.

For a [field](../fields/) $F$ and a positive integer $n,$ the [determinant](../determinant-of-a-square-matrix/) satisfies $\det(AB) = \det(A)\det(B),$ so it is a homomorphism from $\mathrm{GL}(n, F)$ onto the multiplicative group of nonzero elements of $F.$ Its kernel is the special linear group $\mathrm{SL}(n, F),$ which consists of the matrices with determinant $1$ and is a normal subgroup of $\mathrm{GL}(n, F).$

- - -

A bijective homomorphism $\varphi : G \to H$ is an isomorphism. If such a map exists, the groups are isomorphic, written $G \cong H.$ Isomorphic groups have the same group-theoretic properties.

Consider $(\mathbb{Z}/2\mathbb{Z}, +)$ and the group $(\{\ 1, -1 \ \}, \cdot)$ under multiplication. Define $\varphi : \mathbb{Z}/2\mathbb{Z} \to \{\ 1, -1 \ \}$ by $\varphi(0) = 1$ and $\varphi(1) = -1.$ Any sum involving $0$ satisfies the homomorphism condition because $\varphi(0) = 1$ is the multiplicative identity. For the remaining case:

$$
\begin{align}
\varphi(1 + 1) &= \varphi(0) \\[6pt]
               &= 1 \\[6pt]
               &= (-1)(-1) \\[6pt]
               &= \varphi(1) \cdot \varphi(1)
\end{align}
$$

Thus $\varphi$ is a homomorphism. It is bijective, so it is an isomorphism and $\mathbb{Z}/2\mathbb{Z} \cong \{\ 1, -1 \ \}.$

Let $\mathbb{R}^{+}$ be the positive real numbers under multiplication and let $\mathbb{R}$ be the real numbers under addition. The [logarithm](../logarithms/) $\log : \mathbb{R}^{+} \to \mathbb{R}$ satisfies $\log(xy) = \log(x) + \log(y),$ which is the homomorphism condition for these operations. The map is bijective and has the exponential function as its inverse. Hence it is an isomorphism, so the multiplicative group $\mathbb{R}^{+}$ and the additive group $\mathbb{R}$ have the same group structure.

A homomorphism from a group to itself is an endomorphism, and a bijective endomorphism is an automorphism. The identity map is an automorphism of every group. The composition of two homomorphisms is also a homomorphism.

The inverse $\varphi^{-1} : H \to G$ of an isomorphism is also an isomorphism. It is bijective. If $y_i = \varphi(x_i)$ for $i = 1, 2,$ then $\varphi^{-1}(y_1 \star y_2) = \varphi^{-1}(\varphi(x_1 \cdot x_2)) = x_1 \cdot x_2,$ so $\varphi^{-1}$ is a homomorphism. Hence isomorphism is a symmetric relation between groups.

> [Rings](../rings/), [fields](../fields/), [vector spaces](../vector-spaces/), and [modules](../modules/) also have kernels, images, and isomorphisms, defined with respect to their operations. The page on [homomorphisms and isomorphisms](../homomorphisms-and-isomorphisms/) compares these definitions.
