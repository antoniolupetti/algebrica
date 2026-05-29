---
title: Groups
source: https://algebrica.org/groups/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - associativity
  - cyclic-group
  - group-theory
  - homomorphism
  - identity-element
  - inverse-element
  - isomorphism
  - subgroup
  - symmetric-group
---
## Definition

A group is one of the most fundamental structures in abstract algebra. The concept arises when one isolates the essential properties shared by many mathematical objects: the [integers](../integers/) under addition, the nonzero [real numbers](../real-numbers/) under multiplication, the symmetries of a geometric figure, and the invertible [matrices](../matrices/) of a given size all exhibit the same abstract pattern. In formal terms, a group is a set $G$ together with a binary operation $\cdot : G \times G \to G$ satisfying the following four axioms:

+ Closure: for all $a, b \in G$, the element $a \cdot b$ belongs to $G$.
+ Associativity: for all $a, b, c \in G$, the identity $(a \cdot b) \cdot c = a \cdot (b \cdot c)$ holds.
+ Identity element: there exists an element $e \in G$ such that $a \cdot e = e \cdot a = a$ for all $a \in G$.
+ Inverses: for every $a \in G$ there exists an element $a^{-1} \in G$ such that $a \cdot a^{-1} = a^{-1} \cdot a = e$.

A group $(G, \cdot)$ is called abelian, or commutative, if in addition $a \cdot b = b \cdot a$ for all $a, b \in G$.

> The identity element and the inverse of each element are unique. Both facts follow directly from the axioms and are standard early results in any treatment of group theory.

## Properties

Several consequences follow from the previous axioms. If $a \cdot b = a \cdot c$ for some $a, b, c \in G$, then multiplying both sides on the left by $a^{-1}$ gives $b = c$. This is the left cancellation law. The right cancellation law holds by an analogous argument. Together they imply that the equation $a \cdot x = b$ has a unique solution $x = a^{-1} \cdot b$ in $G$ for any given $a, b \in G$. The inverse of a product satisfies the following identity:

$$(a \cdot b)^{-1} = b^{-1} \cdot a^{-1}$$

This reversal of order is a consequence of the associativity axiom and is sometimes called the "sock-shoe" property. To undo the operation of first putting on a sock and then a shoe, one must first remove the shoe and then the sock. The order of a group $G$, denoted $|G|$, is the cardinality of the underlying set. A group with finitely many elements is called a finite group, otherwise it is infinite.

## Algebraic hierarchy

Groups are the most elementary objects in the hierarchy of algebraic structures. A group consists of a set equipped with a single binary operation satisfying closure, associativity, the existence of an identity element, and the existence of inverses. When a second operation is introduced and required to distribute over the first, the resulting structure is a [ring](../rings/).

Imposing the further condition that every nonzero element be invertible under multiplication then yields a [field](../fields/). The three structures form a chain of increasing rigidity:

+ A group carries one operation with inverses.
+ A ring carries two operations, with inverses guaranteed only for addition.
+ A field carries two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication.

> As an example, the integers $\mathbb{Z}$ form a ring but not a field. The [rational numbers](../rational-numbers/) $\mathbb{Q}$ form a field. Both extend the group structure by adding a second operation. The construction continues into the world of linear algebra: when scalars are drawn from a field, one obtains a [vector space](../vector-spaces/), and when they are drawn from a ring instead, the resulting structure is a [module](../modules/).

## Order of an element

The order of an element $a$ in a group $G$ is the smallest positive integer $n$ such that $a^n = e$, where $e$ is the identity element and the notation $a^n$ denotes the product of $a$ with itself $n$ times. When no such integer exists, the element is said to have infinite order. The order of $a$ is denoted $\operatorname{ord}(a)$.

As an example, consider the group $(\mathbb{Z}/6\mathbb{Z}, +)$. The element $2$ has order $3$, since $2 + 2 + 2 = 6 \equiv 0 \pmod{6}$ and neither $2$ nor $2 + 2 = 4$ is congruent to $0$. The element $1$ has order $6$, since $1$ must be added to itself six times to obtain $0$. In the group $(\mathbb{Z}, +)$ every nonzero element has infinite order, because no finite sum of a fixed nonzero integer can equal $0$.

> The modulo operator $a \bmod n$ returns the remainder of the division of $a$ by $n$. For example, $7 \bmod 5 = 2$ since $7 = 1 \cdot 5 + 2$. The systematic treatment is given on the page on the [modulo operator](../modulo-operator/).

## Examples

The set $\mathbb{Z}$ equipped with ordinary addition forms an abelian group. The identity element is $0$, and the inverse of an integer $n$ is $-n$. This is an infinite group and arguably the most natural example of a group in elementary mathematics.

Let $n$ be a positive integer. The set $\mathbb{Z}/n\mathbb{Z} = \\{\ 0, 1, \ldots, n - 1 \ \\}$ equipped with addition [modulo](../modulo-operator/) $n$ forms a finite abelian group of order $n$. For example, in $\mathbb{Z}/5\mathbb{Z}$ one has $3 + 4 = 2$, since $7 \equiv 2 \pmod{5}$. The identity element is $0$ and the inverse of $k$ is $n - k$.

- - -

Let $F$ be a [field](../fields/) and let $n$ be a positive integer. The set of all [invertible](../inverse-matrix/) $n \times n$ matrices with entries in $F$, denoted $\operatorname{GL}(n, F)$, forms a group under matrix multiplication. The identity element is the identity matrix $I_n$, and the inverse of a matrix $A$ is its matrix inverse $A^{-1}$. This group is not abelian for $n \geq 2$, since matrix multiplication does not commute in general.

Given a set $\\{\ 1, 2, \ldots, n \ \\}$, a permutation is a bijection from this set to itself. The collection of all such permutations forms a group under [composition of functions](../composite-functions/), denoted $S_n$ and called the symmetric group on $n$ elements. The identity element is the identity permutation, and the inverse of a permutation $\sigma$ is the inverse function $\sigma^{-1}$. The group $S_n$ has order equal to the [factorial](../factorial/) $n!$ and is non-abelian for $n \geq 3$.

As a concrete illustration, consider $S_3$, which has order $6$. Let $\sigma$ be the permutation sending $1 \mapsto 2$, $2 \mapsto 3$, $3 \mapsto 1$, and let $\tau$ be the permutation sending $1 \mapsto 2$, $2 \mapsto 1$, $3 \mapsto 3$:

$$\sigma = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 3 & 1 \end{pmatrix} \qquad \tau = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 1 & 3 \end{pmatrix}$$

To compute $\sigma \circ \tau$, one applies $\tau$ first and then $\sigma$. The element $1$ is sent by $\tau$ to $2$, and then $\sigma$ sends $2$ to $3$, so $1 \mapsto 3$. The element $2$ is sent by $\tau$ to $1$, and then $\sigma$ sends $1$ to $2$, so $2 \mapsto 2$. Finally, $3$ is fixed by $\tau$, and $\sigma$ sends $3$ to $1$, so $3 \mapsto 1$. Therefore:

$$\sigma \circ \tau = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 3 & 2 & 1 \end{pmatrix}$$

An analogous computation yields:

$$\tau \circ \sigma = \begin{pmatrix} 1 & 2 & 3 \\[6pt] 1 & 3 & 2 \end{pmatrix}$$

Since $\sigma \circ \tau \neq \tau \circ \sigma$, the group $S_3$ is indeed non-abelian.

## When the axioms fail

A good way to appreciate the group axioms is to look at pairs consisting of a set and an operation that almost form a group, but fail on one specific point. Each failure isolates a different axiom and shows why the definition is cut exactly as it is.

Consider the [natural numbers](../natural-numbers/) including zero, $\mathbb{N}_0 = \\{\ 0, 1, 2, \ldots \ \\}$, equipped with ordinary addition. The operation is closed and associative, and $0$ acts as an identity element. The axiom that fails is the existence of inverses. Given any positive integer $n$, there is no element in $\mathbb{N}_0$ that added to $n$ returns $0$, because the candidate $-n$ lies outside the set. The structure $(\mathbb{N}_0, +)$ is therefore not a group, but only a monoid.

- - -

The [integers](../integers/) with multiplication, $(\mathbb{Z}, \cdot)$, are another example. Closure, associativity, and the identity $1$ are all in place, yet the vast majority of integers lack a multiplicative inverse inside $\mathbb{Z}$. The only elements that admit an inverse are $1$ and $-1$, since for any other integer $n$ the reciprocal $1/n$ is not an integer. Dropping all non-invertible elements would leave only the two-element set $\\{\ 1, -1 \ \\}$, which is a group under multiplication but a much smaller object than the integers.

The [real numbers](../real-numbers/) with multiplication, $(\mathbb{R}, \cdot)$, come even closer to being a group. Every real number different from zero has a multiplicative inverse, namely its reciprocal. The obstacle is a single element: zero has no multiplicative inverse, and its presence in the set is enough to disqualify the whole structure. The fix is to remove it. The set of nonzero reals $\mathbb{R} \setminus \\{\ 0 \ \\}$ equipped with ordinary multiplication forms an abelian group, with identity $1$ and inverse $a^{-1} = 1/a$ for every $a \neq 0$.

> These three cases each fail a different axiom: inverses for $(\mathbb{N}_0, +)$, inverses for all but two elements in $(\mathbb{Z}, \cdot)$, and the existence of an inverse for the single element $0$ in $(\mathbb{R}, \cdot)$. The last case illustrates a recurring pattern in algebra, in which removing a problematic element produces a legitimate group.

## Cyclic groups

A group $G$ is called cyclic when there exists an element $g \in G$ such that every element of $G$ can be written as a power of $g$, that is:

$$G = \\{\ g^n : n \in \mathbb{Z} \ \\}$$

Such an element $g$ is called a generator of $G$. Every cyclic group is isomorphic either to $\mathbb{Z}$ when it is infinite, or to $\mathbb{Z}/n\mathbb{Z}$ for some positive integer $n$ when it is finite.

The group $(\mathbb{Z}/6\mathbb{Z}, +)$ is cyclic with generator $1$, since every element $0, 1, 2, 3, 4, 5$ can be obtained as a multiple of $1$. The element $5$ is also a generator, as repeated addition of $5$ modulo $6$ produces all six residues. The element $2$, however, is not a generator, since the multiples of $2$ modulo $6$ are only $\\{\ 0, 2, 4 \ \\}$, which form a proper subgroup of $\mathbb{Z}/6\mathbb{Z}$.

## Subgroups

A subset $H$ of a group $G$ is called a subgroup when $H$ is itself a group under the operation inherited from $G$. Rather than verifying all four group axioms separately, the following criterion is usually more convenient: a nonempty subset $H \subseteq G$ is a subgroup of $G$ if and only if for all $a, b \in H$ the element $a \cdot b^{-1}$ belongs to $H$. This condition encodes closure under the operation and under taking inverses, and the presence of the identity follows from setting $a = b$. The notation $H \leq G$ indicates that $H$ is a subgroup of $G$.

Every group $G$ has at least two subgroups: the trivial subgroup $\\{\ e \ \\}$ and $G$ itself. Any subgroup other than $G$ is called a proper subgroup.

As an example, consider the set of even integers $2\mathbb{Z} = \\{\ \ldots, -4, -2, 0, 2, 4, \ldots \ \\}$ as a subset of $(\mathbb{Z}, +)$. Taking any two even integers $a = 2m$ and $b = 2k$, the inverse of $b$ in $\mathbb{Z}$ is $-b = -2k$, so $a + (-b) = 2(m - k)$, which is again even. The subgroup criterion is therefore satisfied, and $2\mathbb{Z}$ is a subgroup of $\mathbb{Z}$.

## Group homomorphisms and isomorphisms

A group homomorphism is a [function](../functions/) between two groups that preserves the group structure. Given two groups $(G, \cdot)$ and $(H, \star)$, a function $\varphi : G \to H$ is a homomorphism when for all $a, b \in G$:

$$\varphi(a \cdot b) = \varphi(a) \star \varphi(b)$$

This condition requires that applying $\varphi$ after performing the operation in $G$ yields the same result as first applying $\varphi$ to each element and then performing the operation in $H$. Several basic properties follow from this definition. A homomorphism $\varphi : G \to H$ necessarily maps the identity of $G$ to the identity of $H$, and satisfies $\varphi(a^{-1}) = \varphi(a)^{-1}$ for all $a \in G$. Two particularly important subsets associated with a homomorphism $\varphi : G \to H$ are the [kernel](../homomorphisms-and-isomorphisms/) and the image. The kernel is defined as:

$$\ker(\varphi) = \\{\ a \in G : \varphi(a) = e_H \ \\}$$

where $e_H$ denotes the identity of $H$, and the image is defined as:

$$\operatorname{im}(\varphi) = \\{\ \varphi(a) : a \in G \ \\}$$

The kernel is always a subgroup of $G$, and the image is always a subgroup of $H$. Moreover, a homomorphism is injective if and only if its kernel contains only the identity element of $G$.

- - -

A homomorphism $\varphi : G \to H$ that is both injective and surjective is called an isomorphism. When an isomorphism exists between $G$ and $H$, the two groups are said to be isomorphic, written $G \cong H$. Isomorphic groups are structurally identical: they differ only in the names of their elements and their operation, and not in any property that is intrinsic to their group structure.

As an example, consider the group $(\mathbb{Z}/2\mathbb{Z}, +)$ and the group $(\\{\ 1, -1 \ \\}, \times)$ under ordinary multiplication. Define $\varphi : \mathbb{Z}/2\mathbb{Z} \to \\{\ 1, -1 \ \\}$ by setting $\varphi(0) = 1$ and $\varphi(1) = -1$. Since:

$$
\begin{align}
\varphi(1 + 1) &= \varphi(0) \\[6pt]
               &= 1 \\[6pt]
               &= (-1)(-1) \\[6pt]
               &= \varphi(1) \cdot \varphi(1)
\end{align}
$$

the function $\varphi$ preserves the group operation. Since it is also bijective, it is an isomorphism, and therefore $\mathbb{Z}/2\mathbb{Z} \cong \\{\ 1, -1 \ \\}$.

> The notions of kernel, image, and isomorphism extend naturally to the richer settings of [rings](../rings/), [fields](../fields/), [vector spaces](../vector-spaces/), and [modules](../modules/), where the structure-preserving maps acquire additional requirements but the underlying philosophy remains the same. A unified discussion that compares the different cases side by side is collected on the page about [homomorphisms and isomorphisms](../homomorphisms-and-isomorphisms/).
