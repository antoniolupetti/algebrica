---
title: Modules
source: https://algebrica.org/modules/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - annihilator
  - basis
  - cyclic-module
  - direct-sum
  - endomorphism-ring
  - free-module
  - homomorphism
  - ideal
  - linear-independence
  - module
  - module-theory
  - ring
  - submodule
  - torsion
---
## Definition

A module is defined like a [vector space](../vector-spaces/), except that its scalars form a [ring](../rings/) rather than a [field](../fields/). [Ideals](../rings/) inside a ring, [abelian groups](../groups/) with their canonical $\mathbb{Z}$-action, and a vector space with the action of one [linear operator](../eigenvalues-and-eigenvectors/) all have this form, although their scalars need not be invertible. Every vector space is a module, and module theory is the common language of commutative algebra and homological algebra.

Let $R$ be a ring. A left module over $R,$ or simply a left $R$-module, is an [abelian group](../groups/) $(M, +)$ equipped with a scalar multiplication $\cdot : R \times M \to M$ satisfying the following axioms for all $r, s \in R$ and all $\mathbf{u}, \mathbf{v} \in M$:

+ Distributivity over module addition: $r \cdot (\mathbf{u} + \mathbf{v}) = r \cdot \mathbf{u} + r \cdot \mathbf{v}.$
+ Distributivity over ring addition: $(r + s) \cdot \mathbf{v} = r \cdot \mathbf{v} + s \cdot \mathbf{v}.$
+ Compatibility with ring multiplication: $(rs) \cdot \mathbf{v} = r \cdot (s \cdot \mathbf{v}).$

These three axioms say nothing about the multiplicative identity of $R.$ When $R$ has an identity element $1,$ the module $M$ is called unital when in addition $1\mathbf{v} = \mathbf{v}$ for every $\mathbf{v} \in M.$ The three axioms alone do not imply this: the zero multiplication $r\mathbf{v} = \mathbf{0}$ satisfies all of them on any abelian group and fails the identity axiom whenever $M \neq \{\ \mathbf{0} \ \}.$

> Throughout this page $R$ has an identity element and every module is assumed unital, which is the standard convention. With this convention, the axioms reduce exactly to those of a vector space when $R$ is a field, so every vector space is a module and the theory of modules contains the theory of vector spaces as a special case. The ring $R$ over which $M$ is defined is called the ring of scalars of $M.$

A right module over $R$ is an abelian group $(M, +)$ with a product $M \times R \to M$ satisfying $\mathbf{v}(rs) = (\mathbf{v}r)s,$ $\mathbf{v}(r + s) = \mathbf{v}r + \mathbf{v}s,$ and $(\mathbf{u} + \mathbf{v})r = \mathbf{u}r + \mathbf{v}r.$ The side on which the scalar is written matters. Transcribing a left action on the right would produce $(rs)\mathbf{v} = s(r\mathbf{v}),$ which reverses the order of the factors, so left and right modules over a noncommutative ring are different structures. When $R$ is commutative the two notions coincide and one speaks simply of an $R$-module. Unless stated otherwise, module means left module.

## Modules as ring actions

An action of a [group](../groups/) $G$ on a set $X$ is a [homomorphism](../homomorphisms-and-isomorphisms/) $\rho : G \to \mathrm{Sym}(X)$ into the group of permutations of $X.$ Writing $gx = \rho(g)(x)$ converts the homomorphism property of $\rho$ into the mixed associative law $(g_1g_2)x = g_1(g_2x).$ A module is the analogous action of a ring on an abelian group.

Let $M$ be an abelian group and let $\mathrm{End}(M)$ be the set of its group endomorphisms, that is, the maps $f : M \to M$ with $f(\mathbf{u} + \mathbf{v}) = f(\mathbf{u}) + f(\mathbf{v}).$ With pointwise addition $(f + g)(\mathbf{v}) = f(\mathbf{v}) + g(\mathbf{v})$ and composition $(fg)(\mathbf{v}) = f(g(\mathbf{v})),$ the set $\mathrm{End}(M)$ is a ring with identity $\mathrm{id}_M,$ called the endomorphism ring of $M.$ An action of a ring $R$ on $M$ is a ring homomorphism:

$$\varphi : R \to \mathrm{End}(M)$$

Given such a $\varphi,$ define a product by $r\mathbf{v} = \varphi(r)(\mathbf{v}).$ The statement that each $\varphi(r)$ lies in $\mathrm{End}(M)$ is the first distributive axiom, additivity of $\varphi$ is the second, and multiplicativity of $\varphi$ is the compatibility axiom:

$$
\begin{align}
r(\mathbf{u} + \mathbf{v}) &= \varphi(r)(\mathbf{u} + \mathbf{v}) = \varphi(r)(\mathbf{u}) + \varphi(r)(\mathbf{v}) = r\mathbf{u} + r\mathbf{v} \\[6pt]
(r + s)\mathbf{v} &= \varphi(r + s)(\mathbf{v}) = \big(\varphi(r) + \varphi(s)\big)(\mathbf{v}) = r\mathbf{v} + s\mathbf{v} \\[6pt]
(rs)\mathbf{v} &= \varphi(rs)(\mathbf{v}) = \big(\varphi(r)\varphi(s)\big)(\mathbf{v}) = r(s\mathbf{v})
\end{align}
$$

Conversely, a product $R \times M \to M$ satisfying the three axioms determines maps $\varphi(r) : M \to M$ by $\varphi(r)(\mathbf{v}) = r\mathbf{v}.$ The first axiom says $\varphi(r) \in \mathrm{End}(M),$ and the remaining two say that $\varphi$ preserves addition and multiplication. Specifying an $R$-module structure on $M$ is therefore the same as specifying a ring homomorphism from $R$ into $\mathrm{End}(M),$ and the module is unital exactly when $\varphi(1) = \mathrm{id}_M.$

> For any module structure on $M,$ the ring of scalars acts through a ring homomorphism into $\mathrm{End}(M).$ In particular, with $R = \mathrm{End}(M)$ and $\varphi = \mathrm{id},$ every abelian group is a module over its own endomorphism ring. The kernel of $\varphi$ consists of the scalars that send all of $M$ to $\mathbf{0},$ so the action is faithful exactly when $\ker(\varphi) = \{\ 0 \ \}.$

## Properties

Several consequences follow directly from the axioms. For any $\mathbf{v} \in M,$ multiplication by the additive identity of the ring satisfies $0\mathbf{v} = \mathbf{0}.$ To see this, one writes:

$$0\mathbf{v} = (0 + 0)\mathbf{v} = 0\mathbf{v} + 0\mathbf{v}$$

and then cancels $0\mathbf{v}$ from both sides using the abelian group structure of $(M, +).$ The same cancellation applied to the first distributive axiom gives $r\mathbf{0} = \mathbf{0}$ for every $r \in R.$ Since $r\mathbf{v} + r(-\mathbf{v}) = r(\mathbf{v} - \mathbf{v}) = r\mathbf{0} = \mathbf{0},$ we have $r(-\mathbf{v}) = -(r\mathbf{v}).$ The symmetric computation with the second axiom gives $(-r)\mathbf{v} = -(r\mathbf{v}).$ For $r = 1,$ this identity is $(-1)\mathbf{v} = -\mathbf{v}.$ These arguments use only the three axioms and the group structure of $M,$ and they are the same ones that establish the corresponding rules for vector spaces.

Unlike [vector spaces](../vector-spaces/), modules can have nonzero elements annihilated by a nonzero scalar. An element $\mathbf{v} \in M$ is called a torsion element when there exists a nonzero $r \in R$ with $r\mathbf{v} = \mathbf{0}.$ The set of all torsion elements of $M$ is denoted $T(M),$ and when $R$ is an [integral domain](../rings/) it is a submodule of $M.$ A module is torsion-free when $T(M) = \{\ \mathbf{0} \ \},$ and a torsion module when $T(M) = M.$ Vector spaces are automatically torsion-free, since in a [field](../fields/) the equation $\alpha\mathbf{v} = \mathbf{0}$ with $\alpha \neq 0$ forces $\mathbf{v} = \mathbf{0}$ by invertibility of $\alpha.$

## Algebraic hierarchy

The structures introduced so far form a chain of increasing rigidity. A [group](../groups/) has one operation in which every element has an inverse. A [ring](../rings/) has two operations. Every element has an additive inverse, but a nonzero element need not have a multiplicative inverse. In a [field](../fields/), every nonzero element has a multiplicative inverse. A [vector space](../vector-spaces/) has an underlying field and a separate set of vectors on which the field acts by scalar multiplication.

A module has the same form as a vector space, except that its ring of scalars need not be a field. Without multiplicative inverses for general scalars, phenomena absent from linear algebra become possible:

+ Bases need not exist.
+ Rank, when defined, need not be invariant over a noncommutative ring.
+ Torsion elements may occur.
+ A submodule need not have a complement.
+ A module can be isomorphic to a proper submodule of itself.

> Every vector space is a module over its field of scalars, and every abelian group is a module over the ring of [integers](../integers/). The category of modules over a ring $R$ generalises both vector spaces and abelian groups, and reduces to either of them in the appropriate special case.

## Examples

Every abelian group $(A, +)$ has exactly one structure of unital $\mathbb{Z}$-module. The identity axiom fixes $1a = a,$ and distributivity over ring addition then forces the scalar multiplication of a positive integer $n$ by $a \in A$ to be repeated addition:

$$n \cdot a = \underbrace{a + a + \cdots + a}_{n \text{ summands}}$$

For $n < 0$ the rule $(-r)\mathbf{v} = -(r\mathbf{v})$ of the previous section gives $n \cdot a = -((-n) \cdot a),$ and $0 \cdot a = 0$ was proved there as well, so the whole scalar multiplication is determined. The module axioms reduce in this case to the standard rules for integer multiples in an abelian group, so the theory of $\mathbb{Z}$-modules and the theory of abelian groups coincide.

Let $R$ be a ring and let $n$ be a positive integer. The set $R^n$ of ordered $n$-tuples with entries in $R,$ with componentwise addition and componentwise scalar multiplication, is an $R$-module. This is the direct generalisation of the [vector space](../vector-spaces/) $F^n$ over a field $F.$ When $R = \mathbb{Z},$ the module $\mathbb{Z}^n$ is the prototypical free module of finite rank.

- - -

Every ring $R$ is a module over itself, with scalar multiplication given by the ring multiplication. More generally, every [left ideal](../rings/) of $R$ is a left $R$-module and every right ideal is a right $R$-module, since an ideal is by definition closed under multiplication by arbitrary ring elements on the appropriate side. Ideals are therefore modules of this form, which explains the use of module theory in commutative algebra.

The set $\mathbb{Z}/n\mathbb{Z}$ is an abelian group of order $n$ under addition [modulo](../modulo-operator/) $n,$ so by the construction above it is a $\mathbb{Z}$-module. Every element $\bar{a} \in \mathbb{Z}/n\mathbb{Z}$ satisfies $n\bar{a} = 0,$ so the entire module is torsion.

Let $V$ be a vector space over a field $K$ and let $\mathrm{End}_K(V)$ be the ring of $K$-linear maps from $V$ to itself. With the evaluation action $T\mathbf{v} = T(\mathbf{v}),$ the vector space $V$ is a unital module over $\mathrm{End}_K(V).$ The compatibility axiom is the definition of composition, and the two distributive laws are the linearity of each $T$ and the definition of pointwise addition. The matrix form of this action appears next.

Let $K$ be a field and let $R = \mathrm{M}_n(K)$ be the [ring of $n \times n$ matrices](../matrices/) over $K.$ For each $s \geq 1,$ the set of $n \times s$ matrices over $K$ is a left $R$-module under matrix multiplication on the left, and the set of $s \times n$ matrices is a right $R$-module under matrix multiplication on the right. Associativity of matrix multiplication is the compatibility axiom in both cases, and the distributive laws for matrices give the other two axioms. For $s = 1,$ the left module is the column space $K^n,$ which is the coordinate version of the action of $\mathrm{End}_K(V)$ on $V.$ When $s = n,$ the same set of matrices has both structures, which are distinct actions of the same noncommutative ring.

## Modules over a polynomial ring

Let $V$ be a vector space over a field $K$ and let $T : V \to V$ be a $K$-linear map. Evaluation of [polynomials](../polynomials/) at $T$ is a unital ring homomorphism:

$$\varphi_T : K[x] \to \mathrm{End}_K(V)$$

$$\sum_i \alpha_ix^i \mapsto \sum_i \alpha_iT^i$$

with the convention $T^0 = \mathrm{id}_V.$ Every $K$-linear map is in particular additive, so $\mathrm{End}_K(V)$ is a subring of $\mathrm{End}(V)$ and $\varphi_T$ is an action of $K[x]$ on the additive group of $V.$ Thus $V$ is a unital $K[x]$-module with scalar multiplication:

$$\Big(\sum_i \alpha_ix^i\Big) \cdot \mathbf{v} = \sum_i \alpha_iT^i(\mathbf{v})$$

The construction can be reversed. Suppose $V$ is a unital $K[x]$-module and let $\varphi : K[x] \to \mathrm{End}(V)$ be the corresponding homomorphism. With scalars restricted to the constant polynomials, $V$ is a unital $K$-module, hence a $K$-vector space, with $\alpha\mathbf{v} = \varphi(\alpha)(\mathbf{v}).$ Set $T = \varphi(x).$ Since $K[x]$ is commutative, the elements $\varphi(x)$ and $\varphi(\alpha)$ commute in $\mathrm{End}(V),$ so for all $\alpha \in K$ and $\mathbf{v} \in V$:

$$T(\alpha\mathbf{v}) = \varphi(x)\varphi(\alpha)(\mathbf{v}) = \varphi(\alpha)\varphi(x)(\mathbf{v}) = \alpha T(\mathbf{v})$$

which shows that $T$ is $K$-linear. Multiplicativity of $\varphi$ gives $\varphi(x^i) = T^i,$ and additivity then gives $\varphi(\sum_i \alpha_ix^i) = \sum_i \alpha_iT^i,$ which agrees with the module structure defined above. A unital $K[x]$-module is therefore the same thing as a $K$-vector space together with a choice of linear operator on it.

> Under this correspondence, the $K[x]$-submodules are exactly the invariant subspaces of $T,$ and the annihilator of $V$ is the ideal generated by the minimal polynomial of $T.$ The classification of finitely generated $K[x]$-modules gives the canonical forms of a linear map. When $T$ has a basis of eigenvectors, its matrix admits a [diagonalization](../matrix-diagonalization/). For $\mathbb{Z}$-modules, the classification of finitely generated modules is the structure theorem for finitely generated abelian groups.

## Submodules

A subset $N \subseteq M$ is called a submodule of $M$ when $N$ is a subgroup of $(M, +)$ and $r\mathbf{v} \in N$ for all $r \in R$ and $\mathbf{v} \in N.$ Under the unital convention, closure under negation is automatic because $-\mathbf{v} = (-1)\mathbf{v}.$ Thus a nonempty $N$ is a submodule as soon as $\mathbf{u} + \mathbf{v} \in N$ and $r\mathbf{v} \in N$ for all $\mathbf{u}, \mathbf{v} \in N$ and $r \in R.$ The two conditions together express closure under arbitrary $R$-linear combinations, and they imply that $\mathbf{0}$ belongs to every submodule. Every module $M$ has the trivial submodule $\{\ \mathbf{0} \ \}$ and $M$ itself, and any submodule different from $M$ is called proper.

Consider the $\mathbb{Z}$-module $\mathbb{Z}$ and the subset $2\mathbb{Z}$ of even integers. For $a, b \in 2\mathbb{Z}$ the sum $a + b$ is even, and for $n \in \mathbb{Z}$ and $a \in 2\mathbb{Z}$ the product $na$ is even, so $2\mathbb{Z}$ is a submodule of $\mathbb{Z}.$ More generally, every [subgroup](../groups/) of an abelian group $A$ is automatically a $\mathbb{Z}$-submodule of $A,$ since the additive structure already determines integer scalar multiplication.

When $R$ acts on itself by left multiplication, the submodules of $R$ are precisely the left ideals of $R,$ because the two closure conditions are word for word the definition of a left ideal. For the right module structure, the submodules are the right ideals. The submodules of the $K[x]$-module attached to an operator $T$ also have a direct description. A subset $W \subseteq V$ closed under the action of every polynomial is in particular closed under the constants, hence a $K$-subspace, and closed under $x,$ hence invariant under $T.$ Conversely, a subspace $W$ with $T(W) \subseteq W$ satisfies $T^i(W) \subseteq W$ for every $i$ and is therefore closed under all of $K[x].$ The $K[x]$-submodules of $V$ are exactly the $T$-invariant subspaces. Every $T$ has at least two of them, the kernel $\ker(T),$ which $T$ sends to $\mathbf{0},$ and the image $\mathrm{im}(T),$ which $T$ maps into itself.

- - -

Submodules are stable under some set-theoretic operations and not others. If $\{\ N_\alpha \ \}$ is any family of submodules of $M,$ the intersection $\bigcap_\alpha N_\alpha$ is a submodule, since each closure condition holds in every $N_\alpha$ and therefore in the intersection. A union need not be a submodule: both $2\mathbb{Z}$ and $3\mathbb{Z}$ are submodules of the $\mathbb{Z}$-module $\mathbb{Z},$ while $2 + 3 = 5$ lies outside $2\mathbb{Z} \cup 3\mathbb{Z}.$ For an increasing sequence $N_1 \subseteq N_2 \subseteq \cdots$ the obstruction disappears, and the union $\bigcup_n N_n$ is a submodule, because any two of its elements already lie in a common $N_n$ and so does their sum. For submodules $A$ and $B$ the set:

$$A + B = \{\ \mathbf{a} + \mathbf{b} : \mathbf{a} \in A,\ \mathbf{b} \in B \ \}$$

is a submodule, and it is the smallest submodule containing both $A$ and $B.$ Under intersection and sum, the submodules of $M$ are a lattice with $\{\ \mathbf{0} \ \}$ and $M$ as least and greatest elements.

## Generated submodules and annihilators

Let $S \subseteq M$ be any subset and define:

$$RS = \{\ r_1\mathbf{s}_1 + \cdots + r_n\mathbf{s}_n : n \in \mathbb{N},\ r_i \in R,\ \mathbf{s}_i \in S \ \}$$

The set $RS$ is closed under addition, and multiplying such a combination by $r \in R$ gives $\sum_i (rr_i)\mathbf{s}_i,$ again of the same form, so $RS$ is a submodule of $M.$ The identity $\mathbf{s} = 1\mathbf{s}$ gives $S \subseteq RS,$ and any submodule containing $S$ contains all $R$-linear combinations of its elements, so $RS$ is the smallest submodule of $M$ containing $S.$ It is called the submodule generated by $S,$ or the [span](../linear-combinations/) of $S.$

> Without the identity axiom the inclusion $S \subseteq RS$ can fail, and the smallest submodule containing $S$ is $\langle S \rangle + RS,$ where $\langle S \rangle$ is the subgroup of $(M, +)$ generated by $S.$ The two candidates coincide as soon as $R$ has an identity and $M$ is unital, which is the case treated here.

For a single element $\mathbf{x} \in M,$ the submodule $R\mathbf{x} = \{\ r\mathbf{x} : r \in R \ \}$ is called the cyclic submodule generated by $\mathbf{x}.$ A module is cyclic when $M = R\mathbf{x}$ for some $\mathbf{x} \in M,$ and finitely generated when $M = RS$ for some finite $S \subseteq M.$ The ring $R$ is cyclic as a module over itself, generated by $1,$ and $\mathbb{Z}/n\mathbb{Z}$ is cyclic as a $\mathbb{Z}$-module, generated by $\bar{1}.$ Cyclic $\mathbb{Z}$-modules are exactly the cyclic abelian groups.

Two further constructions relate the submodules of $M$ to the ideals of $R.$ Let $I$ be a left ideal of $R$ and set:

$$IM = \{\ r_1\mathbf{x}_1 + \cdots + r_k\mathbf{x}_k : k \geq 1,\ r_i \in I,\ \mathbf{x}_i \in M \ \}$$

Sums of such expressions have the same form, and for $r \in R$ one has $r\sum_i r_i\mathbf{x}_i = \sum_i (rr_i)\mathbf{x}_i$ with $rr_i \in I$ because $I$ is a left ideal, so $IM$ is a submodule of $M.$

In the other direction, let $N$ be a submodule of $M$ and define the annihilator of $N$ in $R$ by:

$$\mathrm{ann}(N) = \{\ r \in R : r\mathbf{x} = \mathbf{0} \text{ for all } \mathbf{x} \in N \ \}$$

If $r, r' \in \mathrm{ann}(N)$ then $(r - r')\mathbf{x} = r\mathbf{x} - r'\mathbf{x} = \mathbf{0},$ so $\mathrm{ann}(N)$ is a subgroup of $(R, +).$ For $s \in R$ and $\mathbf{x} \in N$ one has $(sr)\mathbf{x} = s(r\mathbf{x}) = s\mathbf{0} = \mathbf{0},$ so $\mathrm{ann}(N)$ is a left ideal, and $(rs)\mathbf{x} = r(s\mathbf{x}) = \mathbf{0}$ because $s\mathbf{x}$ again lies in $N.$ The annihilator is therefore a two-sided ideal of $R,$ and the second computation requires $N$ to be a submodule rather than an arbitrary subset.

For $N = M,$ the annihilator is the kernel of the ring homomorphism $\varphi : R \to \mathrm{End}(M)$ attached to the action, so the action is faithful exactly when $\mathrm{ann}(M) = \{\ 0 \ \}.$ In the $\mathbb{Z}$-module $\mathbb{Z}/n\mathbb{Z}$ the annihilator of the whole module is $n\mathbb{Z}.$ For the $K[x]$-module attached to an operator $T$ on a finite-dimensional space, the annihilator of $V$ consists of the polynomials $p$ with $p(T) = 0,$ which is the ideal generated by the minimal polynomial of $T.$

## Direct sums

Given $R$-modules $M_1, M_2, \ldots, M_n,$ their external direct sum is the Cartesian product $M_1 \times \cdots \times M_n$ with componentwise operations:

$$(\mathbf{x}_1, \ldots, \mathbf{x}_n) + (\mathbf{y}_1, \ldots, \mathbf{y}_n) = (\mathbf{x}_1 + \mathbf{y}_1, \ldots, \mathbf{x}_n + \mathbf{y}_n)$$

$$r(\mathbf{x}_1, \ldots, \mathbf{x}_n) = (r\mathbf{x}_1, \ldots, r\mathbf{x}_n)$$

This module is denoted $M_1 \oplus M_2 \oplus \cdots \oplus M_n.$ Each axiom holds because it holds in every component. Inside the direct sum, the set $\widetilde{M}_i$ of tuples whose entries vanish outside position $i$ is a submodule isomorphic to $M_i,$ and the sum of these $n$ submodules is the whole direct sum. The module $R^n$ is the direct sum of $n$ copies of $R.$

An internal direct sum describes a module as a sum of submodules it already contains. Let $A_1, \ldots, A_s$ be submodules of $M$ with $M = A_1 + \cdots + A_s$ and consider the map:

$$\sigma : A_1 \oplus \cdots \oplus A_s \to M$$

$$\sigma(\mathbf{a}_1, \ldots, \mathbf{a}_s) = \mathbf{a}_1 + \cdots + \mathbf{a}_s$$

The following four conditions are equivalent:

1. The map $\sigma$ is an isomorphism of abelian groups.
2. The map $\sigma$ is an isomorphism of $R$-modules.
3. Every $\mathbf{x} \in M$ can be written as $\mathbf{x} = \mathbf{a}_1 + \cdots + \mathbf{a}_s$ with $\mathbf{a}_i \in A_i$ in exactly one way.
4. The only decomposition $\mathbf{0} = \mathbf{a}_1 + \cdots + \mathbf{a}_s$ with $\mathbf{a}_i \in A_i$ has $\mathbf{a}_i = \mathbf{0}$ for every $i.$

Surjectivity of $\sigma$ is the hypothesis $M = A_1 + \cdots + A_s,$ and injectivity of $\sigma$ is the fourth condition, so the first, third and fourth are equivalent by the corresponding statement for abelian groups. The second condition implies the first. For the converse, $\sigma$ respects the action of every scalar:

$$\sigma\big(r(\mathbf{a}_1, \ldots, \mathbf{a}_s)\big) = r\mathbf{a}_1 + \cdots + r\mathbf{a}_s = r\sigma(\mathbf{a}_1, \ldots, \mathbf{a}_s)$$

so a bijective $\sigma$ is an isomorphism of modules. When these conditions hold one writes $M = A_1 \oplus \cdots \oplus A_s$ and calls $M$ the internal direct sum of the $A_i.$ For two submodules the criterion reduces to $M = A + B$ together with $A \cap B = \{\ \mathbf{0} \ \}.$

> Every subspace of a vector space has a complement, so a vector space always splits as a direct sum of a given subspace and a second one. This fails for modules. In the $\mathbb{Z}$-module $\mathbb{Z}$ the submodule $2\mathbb{Z}$ has no complement: a complement would be a submodule $n\mathbb{Z}$ with $2\mathbb{Z} \cap n\mathbb{Z} = \{\ 0 \ \},$ and the element $2n$ lies in both submodules whenever $n \neq 0,$ while $n = 0$ gives $2\mathbb{Z} + n\mathbb{Z} = 2\mathbb{Z} \neq \mathbb{Z}.$

## Free modules and bases

A subset $S \subseteq M$ is linearly independent over $R$ when, for any distinct $\mathbf{x}_1, \ldots, \mathbf{x}_n \in S$ and any $r_1, \ldots, r_n \in R,$ the relation:

$$r_1\mathbf{x}_1 + r_2\mathbf{x}_2 + \cdots + r_n\mathbf{x}_n = \mathbf{0}$$

forces $r_i = 0$ for every $i.$ A basis of $M$ is a linearly independent subset $B$ with $RB = M,$ and a module that admits a basis is called free. The module $R^n$ is free with the standard basis $\hat{\mathbf{e}}_1, \ldots, \hat{\mathbf{e}}_n,$ where $\hat{\mathbf{e}}_j$ has $1$ in position $j$ and $0$ in every other position. Every vector space is free as a module over its field of scalars, so freeness is automatic in the vector space case.

Let $\mathbf{x}_1, \ldots, \mathbf{x}_n$ be distinct nonzero elements of $M.$ The following three conditions are equivalent:

1. The set $B = \{\ \mathbf{x}_1, \ldots, \mathbf{x}_n \ \}$ is a basis of $M.$
2. The map $R^n \to M$ sending $(r_1, \ldots, r_n)$ to $r_1\mathbf{x}_1 + \cdots + r_n\mathbf{x}_n$ is an isomorphism of $R$-modules.
3. For each $i$ the map $r \mapsto r\mathbf{x}_i$ is injective, and $M = R\mathbf{x}_1 \oplus R\mathbf{x}_2 \oplus \cdots \oplus R\mathbf{x}_n.$

The map in the second condition is $R$-linear, it is injective exactly when $B$ is linearly independent, and it is surjective exactly when $B$ generates $M,$ which gives the equivalence of the first two conditions. For the third, injectivity of $r \mapsto r\mathbf{x}_i$ says that $R \cong R\mathbf{x}_i,$ and the direct sum decomposition says that a vanishing sum $\sum_i r_i\mathbf{x}_i$ has every term $r_i\mathbf{x}_i$ equal to $\mathbf{0},$ which combined with the injectivity gives $r_i = 0.$

Two statements about generating sets follow. A basis is a minimal generating set: if $B$ is a basis and $B'$ is a proper subset of $B,$ choose $\mathbf{b} \in B \setminus B'.$ Were $\mathbf{b}$ an element of $RB',$ it would be an $R$-linear combination of elements of $B'$ and the resulting relation would contradict the linear independence of $B.$ Hence $\mathbf{b} \notin RB'$ and $B'$ does not generate $M.$ Every basis of a finitely generated free module is then finite: if $B$ is a basis and $S$ is a finite generating set, each element of $S$ is a combination of finitely many elements of $B,$ so $S \subseteq RB_0$ for some finite $B_0 \subseteq B.$ This gives $M = RS \subseteq RB_0,$ so $B_0$ generates $M,$ and minimality forces $B_0 = B.$ A finitely generated free module is therefore isomorphic to $R^n$ for some $n.$

- - -

The cardinality of a basis of a free module is called its rank. Over a commutative ring $R$ with $1 \neq 0$ the rank is well-defined, so $R^m \cong R^n$ implies $m = n,$ and over a field it coincides with the dimension. Over a noncommutative ring this can fail. Let $V$ be an infinite-dimensional vector space over $K$ and put $R = \mathrm{End}_K(V),$ so that $R$ is free of rank $1$ over itself with basis $\{\ \mathrm{id}_V \ \}.$ Since $\dim_K V$ is infinite, $V$ splits as $V_1 \oplus V_2$ with $V_1 \cong V_2 \cong V.$ Restricting a linear map to each summand of the source gives an isomorphism of abelian groups $R \cong \mathrm{Hom}_K(V_1, V) \oplus \mathrm{Hom}_K(V_2, V),$ and this isomorphism commutes with composing on the left by an element of $R,$ which is the module action. Each summand is isomorphic to $R$ because $V_i \cong V,$ so $R \cong R \oplus R$ as left $R$-modules and the same module is free of rank $1$ and free of rank $2.$

Many modules are not free. Let $G$ be a finite abelian group with more than one element, regarded as a $\mathbb{Z}$-module, and let $n$ be its order. Every $\mathbf{x} \in G$ satisfies $n\mathbf{x} = 0$ with $n \neq 0,$ so no nonempty subset of $G$ is linearly independent, and a basis would have to be empty, which would give $G = \{\ 0 \ \}.$ Hence $G$ is not free. The modules $\mathbb{Z}/n\mathbb{Z}$ with $n > 1$ are the smallest instances: each is generated by the single element $\bar{1},$ yet $\bar{1}$ is not linearly independent because $n\bar{1} = 0$ while $n \neq 0$ in $\mathbb{Z}.$ More generally, every torsion element is linearly dependent by itself.

The preceding constructions give two further examples of nonfree modules. Let $V$ be a nonzero finite-dimensional vector space over $K$ with the $K[x]$-module structure attached to an operator $T.$ The powers $\mathrm{id}_V, T, T^2, \ldots$ lie in the finite-dimensional space $\mathrm{End}_K(V),$ so some nonzero polynomial $p$ satisfies $p(T) = 0.$ Then $p \cdot \mathbf{v} = \mathbf{0}$ for every $\mathbf{v} \in V,$ every element of $V$ is a torsion element, and $V$ is not free over $K[x].$

Let $\dim_K V = n$ and let $R = \mathrm{End}_K(V)$ act on $V$ by evaluation. For any nonzero $\mathbf{v} \in V$ and any $\mathbf{w} \in V$ there is a linear map that sends $\mathbf{v}$ to $\mathbf{w},$ so $R\mathbf{v} = V$ and $V$ is cyclic. When $n > 1,$ extend $\mathbf{v}$ to a basis of $V$ and let $T$ send $\mathbf{v}$ to $\mathbf{0}$ and fix the remaining basis vectors. Then $T \neq 0$ and $T\mathbf{v} = \mathbf{0},$ so $\{\ \mathbf{v} \ \}$ is linearly dependent. Every nonzero element of $V$ is dependent by itself for the same reason, so no nonempty subset of $V$ is independent and $V$ is not free over $R.$ In contrast, the direct sum $V^n$ of $n$ copies of $V$ is free. Fixing a basis $\mathbf{e}_1, \ldots, \mathbf{e}_n$ of $V,$ the map $T \mapsto (T\mathbf{e}_1, \ldots, T\mathbf{e}_n)$ is a bijection from $R$ to $V^n,$ because a linear map is determined by prescribed values on a basis and any tuple of values occurs. It is $R$-linear, since $ST$ has image $(ST\mathbf{e}_1, \ldots, ST\mathbf{e}_n) = S(T\mathbf{e}_1, \ldots, T\mathbf{e}_n).$ Hence $V^n \cong R$ as left $R$-modules and $V^n$ is free of rank $1.$

Free modules of infinite rank also occur. Let $R^{(\infty)}$ be the set of sequences $(x_1, x_2, \ldots)$ with entries in $R$ such that $x_i = 0$ for all but finitely many $i,$ with componentwise operations. The elements $\hat{\mathbf{e}}_i,$ with $1$ in position $i$ and $0$ elsewhere, generate $R^{(\infty)},$ because every element has finitely many nonzero entries and is the corresponding finite combination. They are linearly independent, because a relation $\sum_i r_i\hat{\mathbf{e}}_i = \mathbf{0}$ reads componentwise as $r_i = 0$ for each $i.$ Hence $R^{(\infty)}$ is free with a countably infinite basis. The set of all sequences with arbitrary entries is also an $R$-module, but the $\hat{\mathbf{e}}_i$ do not generate it, since every $R$-linear combination has finitely many nonzero terms.

> Over a field every module is free and every generating set contains a basis, so every vector space has a dimension. Over a general ring both statements fail, and the two characterisations of a basis that agree for vector spaces come apart. A basis is still a minimal generating set, but a maximal linearly independent set need not be a basis: the set $\{\ 2 \ \}$ is linearly independent in the $\mathbb{Z}$-module $\mathbb{Z}$ and cannot be enlarged, yet it generates only $2\mathbb{Z}.$

## Module homomorphisms and isomorphisms

A module homomorphism, also called an $R$-linear map, is a [function](../functions/) $\varphi : M \to N$ between two left $R$-modules that preserves both the additive structure and the action of the ring. Explicitly, $\varphi$ is a homomorphism when for all $\mathbf{u}, \mathbf{v} \in M$ and all $r \in R$ the following two identities hold:

$$\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})$$

$$\varphi(r \cdot \mathbf{v}) = r \cdot \varphi(\mathbf{v})$$

These two conditions combine into the single requirement that $\varphi(r\mathbf{u} + s\mathbf{v}) = r\varphi(\mathbf{u}) + s\varphi(\mathbf{v})$ for all $r, s \in R$ and $\mathbf{u}, \mathbf{v} \in M.$ The [kernel](../homomorphisms-and-isomorphisms/) and image of a module homomorphism are defined as follows:

$$\ker(\varphi) = \{\ \mathbf{v} \in M : \varphi(\mathbf{v}) = \mathbf{0} \ \}$$

$$\mathrm{im}(\varphi) = \{\ \varphi(\mathbf{v}) : \mathbf{v} \in M \ \}$$

The kernel is a submodule of $M,$ the image is a submodule of $N,$ and a composition of module homomorphisms is again a module homomorphism. A homomorphism is injective if and only if its kernel reduces to the zero submodule.

The set of all $R$-module homomorphisms from $M$ to $N$ is denoted $\mathrm{Hom}_R(M, N).$ With pointwise addition $(\varphi + \psi)(\mathbf{v}) = \varphi(\mathbf{v}) + \psi(\mathbf{v}),$ it is an abelian group with the zero map as identity element. A homomorphism from $M$ to itself is called an endomorphism, and the set of these is denoted $\mathrm{End}_R(M).$ With pointwise addition and composition, $\mathrm{End}_R(M)$ is a ring with identity $\mathrm{id}_M.$ It is the subring of $\mathrm{End}(M)$ consisting of the additive endomorphisms that commute with the action of every scalar. For $R = \mathbb{Z}$ the two rings coincide: a map $\varphi : A \to B$ between abelian groups that preserves addition satisfies $\varphi(n\mathbf{a}) = n\varphi(\mathbf{a})$ for every integer $n,$ by induction for $n > 0$ and by $\varphi(-\mathbf{a}) = -\varphi(\mathbf{a})$ for $n < 0.$ Homomorphisms of abelian groups and homomorphisms of $\mathbb{Z}$-modules are the same maps.

Let $R$ be commutative and regard $R^n$ as the set of $n \times 1$ columns over $R.$ For a fixed $n \times m$ matrix $A$ with entries in $R,$ left multiplication $\mathbf{x} \mapsto A\mathbf{x}$ is an $R$-module homomorphism from $R^m$ to $R^n.$ Additivity is the distributive law for matrices, while the identity $A(r\mathbf{x}) = r(A\mathbf{x})$ uses commutativity: the $i$th entry of $A(r\mathbf{x})$ is $\sum_j a_{ij}rx_j,$ and rewriting it as $r\sum_j a_{ij}x_j$ requires $a_{ij}r = ra_{ij}.$ The same statement holds over a noncommutative $R$ whenever the entries of $A$ are central, in particular when they are integer multiples of $1.$ For a noncommutative example, let $R = \mathrm{M}_n(K)$ and let $M$ be the left $R$-module of $n \times s$ matrices over $K.$ For a fixed $s \times s$ matrix $C$ over $K,$ right multiplication $X \mapsto XC$ is an endomorphism of $M,$ because $(AX)C = A(XC)$ for every $A \in R.$

- - -

A module homomorphism that is bijective is called a module isomorphism, and two modules are isomorphic, written $M \cong N,$ when an isomorphism between them exists. A module can be isomorphic to a proper submodule. Consider the $\mathbb{Z}$-module $\mathbb{Z}$ and the map $\varphi : \mathbb{Z} \to \mathbb{Z}$ defined by $\varphi(a) = 2a.$ For any $a, b \in \mathbb{Z}$ one has:

$$
\begin{align}
\varphi(a + b) &= 2(a + b) \\[6pt]
               &= 2a + 2b \\[6pt]
               &= \varphi(a) + \varphi(b)
\end{align}
$$

A direct verification also shows $\varphi(na) = 2na = n\varphi(a)$ for every $n \in \mathbb{Z},$ so $\varphi$ is $\mathbb{Z}$-linear. Its kernel is the trivial submodule $\{\ 0 \ \},$ so $\varphi$ is injective, and its image is the proper submodule $2\mathbb{Z}.$ The map $\varphi$ is therefore an isomorphism between $\mathbb{Z}$ and one of its proper submodules, a phenomenon that cannot occur for finite-dimensional [vector spaces](../vector-spaces/), where an injective linear map from a space to itself is necessarily surjective.

> This example distinguishes modules from finite-dimensional vector spaces. In a finite-dimensional vector space, the [rank-nullity theorem](../rank-of-a-matrix/) implies that an endomorphism is injective if and only if it is surjective. Over a general ring a nonzero scalar need not be invertible, so even an endomorphism of a free module of rank $1$ can be injective without being surjective. The page about [homomorphisms and isomorphisms](../homomorphisms-and-isomorphisms/) defines the related notions of monomorphism, epimorphism, isomorphism, endomorphism, and automorphism.
