---
title: Homomorphisms and Isomorphisms
source: https://algebrica.org/homomorphisms-and-isomorphisms/
license: CC BY-NC 4.0
tags:
  - algebraic-structures
  - alternating-group
  - automorphism
  - endomorphism
  - epimorphism
  - group-action
  - homomorphism
  - image
  - isomorphism
  - kernel
  - monomorphism
  - permutation
---
## The general idea

Every algebraic structure considered here has an underlying [set](../sets/), one or more operations such as addition, multiplication, or scalar multiplication, and sometimes distinguished elements such as an identity or a zero.

A homomorphism is a [function](../functions/) between two algebraic structures of the same type. It commutes with each operation and preserves each distinguished element required by the definition. The precise conditions depend on whether the structures are groups, rings, [modules](../modules/), or [vector spaces](../vector-spaces/). [Injectivity and surjectivity](../injective-surjective-and-bijective-functions/) are separate properties and are not part of the definition.

> In category theory, algebraic structures are objects and their homomorphisms are morphisms. In this language, kernels, images, and quotients have common definitions whenever the category has the required constructions.

## Homomorphisms for standard algebraic structures

A [group](../groups/) is a set with one operation. A group homomorphism $\varphi : (G, \cdot) \to (H, \star)$ is a function such that:

$$\varphi(a \cdot b) = \varphi(a) \star \varphi(b)$$

for all $a, b \in G.$ This equation implies $\varphi(e_G) = e_H$ and $\varphi(a^{-1}) = \varphi(a)^{-1},$ so no separate conditions for identities and inverses are needed. Indeed, $\varphi(e_G) = \varphi(e_G) \star \varphi(e_G),$ and cancellation in $H$ gives $\varphi(e_G) = e_H.$ It follows that $e_H = \varphi(a \cdot a^{-1}) = \varphi(a) \star \varphi(a^{-1}),$ which gives $\varphi(a^{-1}) = \varphi(a)^{-1}.$

A [ring](../rings/) is a set with two operations. A ring homomorphism $\varphi : R \to S$ is a function satisfying both:

$$\varphi(a + b) = \varphi(a) + \varphi(b)$$

$$\varphi(a \cdot b) = \varphi(a) \cdot \varphi(b)$$

for all $a, b \in R.$ For unital rings one usually adds the condition $\varphi(1_R) = 1_S,$ which is not a consequence of the previous two.

A [field](../fields/) is a commutative ring with unity in which every nonzero element is invertible. A field homomorphism is a ring homomorphism between fields that preserves unity. Every field homomorphism is injective. Its kernel is an ideal of the source field, so it is either the zero ideal or the whole field. Since the homomorphism preserves unity, its kernel cannot be the whole field.

A [module](../modules/) over a ring $R$ is an abelian group with a compatible scalar multiplication by elements of $R.$ A module homomorphism $\varphi : M \to N,$ also called an $R$-linear map, satisfies:

$$\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})$$

$$\varphi(r \cdot \mathbf{v}) = r \cdot \varphi(\mathbf{v})$$

for all $\mathbf{u}, \mathbf{v} \in M$ and all $r \in R.$ A [linear map](../linear-maps/) between [vector spaces](../vector-spaces/) is a module homomorphism whose ring of scalars is a field.

> The definition for each structure has one condition for each operation that must be preserved. A group homomorphism preserves the group operation, a ring homomorphism preserves addition and multiplication, and a module homomorphism preserves addition and scalar multiplication.

## Group actions and cyclic homomorphisms

Suppose that a group $G$ acts on a set $X.$ Each element $g \in G$ defines a permutation $\rho(g)$ of $X$ by $\rho(g)(x) = g \cdot x.$ The assignment $\rho : G \to \mathrm{Sym}(X)$ is a homomorphism because:

$$\rho(gh)(x) = (gh) \cdot x = g \cdot (h \cdot x) = \rho(g)(\rho(h)(x))$$

Thus $\rho(gh) = \rho(g) \circ \rho(h).$ Its kernel consists of the elements of $G$ that fix every point of $X.$ The action is faithful if and only if this kernel is $\{\ e_G \ \}.$

Let $D_4$ be the [symmetry group of a square](../dihedral-groups/). Its action on the four vertices defines a homomorphism $\rho_V : D_4 \to S_4.$ This homomorphism is injective because a symmetry that fixes all four vertices is the identity. It is not surjective because $D_4$ has $8$ elements, while $S_4$ has $24.$ The action on the two diagonals defines a surjective homomorphism $\rho_D : D_4 \to S_2.$ Its kernel has four elements, the identity, the half-turn, and the two reflections across the diagonals.

Every element $a$ of a group $G$ defines a homomorphism $\eta_a : \mathbb{Z} \to G$ by $\eta_a(k) = a^k.$ The identity $a^{k+l} = a^ka^l$ proves the homomorphism property, and the image is the cyclic subgroup $\langle a \rangle.$ If $a$ has finite order $m,$ then $\ker(\eta_a) = m\mathbb{Z}.$ If $a$ has infinite order, then $\ker(\eta_a) = \{\ 0 \ \}.$

For a positive integer $n,$ the reduction map $q_n : \mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$ is defined by $q_n(k) = [k].$ It is a surjective homomorphism with kernel $n\mathbb{Z}.$ For $G = \mathbb{Z}/n\mathbb{Z}$ and $a = [1],$ this map is $\eta_a.$

If $G$ is abelian and $n \in \mathbb{Z},$ the power map $P_n : G \to G$ defined by $P_n(g) = g^n$ is an endomorphism because $(gh)^n = g^nh^n.$ Its kernel is $\{\ g \in G : g^n = e_G \ \}.$ When $n \neq 0,$ every element in this kernel has finite order dividing $|n|,$ and every element with such an order belongs to the kernel. When $n = 0,$ the kernel is all of $G.$ If $G$ is finite, $n > 0,$ and $\gcd(n, |G|) = 1,$ then $P_n$ is an isomorphism. An element in its kernel has order dividing both $n$ and $|G|,$ so it is the identity. The map is therefore injective, and an injective map from a finite set to itself is surjective. Consequently, each $g \in G$ has a unique $n$th root in $G.$

## Kernel and image

For a group homomorphism, the kernel is the preimage of the identity in the codomain. For a homomorphism of rings, modules, or vector spaces, it is the preimage of zero. If $e_B$ denotes the relevant neutral element of $B,$ then:

$$\ker(\varphi) = \{\ a \in A : \varphi(a) = e_B \ \}$$

The image of $\varphi$ is:

$$\mathrm{im}(\varphi) = \{\ \varphi(a) : a \in A \ \}$$

The kernel is a normal subgroup when $A$ is a [group](../groups/), an ideal when $A$ is a [ring](../rings/), and a submodule when $A$ is a [module](../modules/). The image is a substructure of $B$ of the same type as $B.$ For these structures, $\varphi$ is injective if and only if its kernel is trivial, namely the subgroup containing only the identity, the zero ideal, or the zero submodule.

For a group homomorphism $\varphi : (G, \cdot) \to (H, \star),$ images and preimages of subgroups are subgroups. If $A \leq G,$ then $\varphi(A)$ is a subgroup of $H,$ since products and inverses of elements in $\varphi(A)$ remain in $\varphi(A).$ If $B \leq H,$ then $\varphi^{-1}(B) = \{\ g \in G : \varphi(g) \in B \ \}$ is a subgroup of $G,$ whether or not $\varphi$ is invertible. Indeed, if $x, y \in \varphi^{-1}(B),$ then $\varphi(x \cdot y^{-1}) = \varphi(x) \star \varphi(y)^{-1} \in B,$ so the subgroup test applies. Taking $A = G$ gives $\mathrm{im}(\varphi),$ while taking $B = \{\ e_H \ \}$ gives $\ker(\varphi).$

If $A$ is normal in $G$ and $\varphi$ is surjective, then $\varphi(A)$ is normal in $H.$ Given $h \in H,$ choose $g \in G$ with $\varphi(g) = h.$ For every $a \in A,$ we have $h\varphi(a)h^{-1} = \varphi(gag^{-1}) \in \varphi(A),$ since $gag^{-1} \in A.$

The kernel of a group homomorphism is normal. If $x \in \ker(\varphi)$ and $g \in G,$ then:

$$\varphi(g \cdot x \cdot g^{-1}) = \varphi(g) \star \varphi(x) \star \varphi(g)^{-1} = e_H$$

Thus $g \ker(\varphi) g^{-1} \subseteq \ker(\varphi)$ for every $g \in G.$ Replacing $g$ by $g^{-1}$ gives $g^{-1}\ker(\varphi)g \subseteq \ker(\varphi).$ Conjugating this inclusion by $g$ gives the reverse inclusion, so $g\ker(\varphi)g^{-1} = \ker(\varphi).$ Conversely, every normal subgroup $N \trianglelefteq G$ is a kernel. The quotient map $\pi : G \to G/N,$ defined by $\pi(g) = gN,$ has kernel $N.$

For a [field](../fields/) $F$ and a positive integer $n,$ the [determinant](../determinant-of-a-square-matrix/) $\det : \mathrm{GL}(n, F) \to F^{\times}$ is a group homomorphism because $\det(AB) = \det(A)\det(B).$ It is surjective, since $\mathrm{diag}(a, 1, \ldots, 1)$ has determinant $a$ for every $a \in F^{\times}.$ Its kernel is the special linear group $\mathrm{SL}(n, F),$ whose elements are the invertible matrices with determinant $1.$ Hence $\mathrm{SL}(n, F)$ is a normal subgroup of $\mathrm{GL}(n, F).$

> In an additive structure, $\varphi(a) = \varphi(a')$ if and only if $a - a' \in \ker(\varphi).$ In a group written multiplicatively, the same equality holds if and only if $a^{-1}a' \in \ker(\varphi).$ If $N = \ker(\varphi),$ these conditions are also equivalent to $aN = a'N.$ Thus the kernel records exactly which elements have the same image.

## The sign homomorphism

For $\sigma$ in the [symmetric group](../symmetric-group/) $S_n,$ let $P_\sigma$ be the permutation matrix defined by $P_\sigma\mathbf{e}_i = \mathbf{e}_{\sigma(i)}.$ Since $P_{\sigma\tau} = P_\sigma P_\tau,$ the determinant defines a group homomorphism:

$$\mathrm{sgn} : S_n \to \{\ 1, -1 \ \}$$

Its value at $\sigma$ is $\mathrm{sgn}(\sigma) = \det(P_\sigma).$

The permutation matrix of a transposition is obtained from the identity matrix by exchanging two columns, so its determinant is $-1.$ If $\sigma$ is a product of $r$ transpositions, then $\mathrm{sgn}(\sigma) = (-1)^r.$ Since the sign is defined without choosing such a product, the parity of $r$ is independent of the chosen decomposition.

A permutation is even when its sign is $1$ and odd when its sign is $-1.$ The even permutations form the alternating group:

$$A_n = \ker(\mathrm{sgn})$$

The group $A_n$ is normal in $S_n.$ For $n \geq 2,$ the sign homomorphism is surjective, so $A_n$ has index $2.$ If $\tau$ is any transposition, the set of odd permutations is the coset $\tau A_n.$

Every $k$-cycle has the decomposition:

$$(a_1, a_2, \ldots, a_k) = (a_1, a_k)(a_1, a_{k-1})\cdots(a_1, a_2)$$

It follows that the sign of a $k$-cycle is $(-1)^{k-1}.$ Hence a $k$-cycle is even when $k$ is odd and odd when $k$ is even.

## Monomorphisms, epimorphisms, isomorphisms

We use the following terminology:

+ A monomorphism is an injective homomorphism.
+ An epimorphism is a surjective homomorphism.
+ An isomorphism is a bijective homomorphism.
+ An endomorphism is a homomorphism from a structure to itself.
+ An automorphism is a bijective endomorphism, that is, an isomorphism from a structure to itself.

When an isomorphism $\varphi : A \to B$ exists, the structures $A$ and $B$ are isomorphic, written $A \cong B.$ They have the same properties expressible in the language of the relevant algebraic structure.

> In category theory, monomorphisms and epimorphisms are defined by cancellation properties. For groups, rings, modules, and vector spaces, monomorphisms are precisely the injective homomorphisms, and isomorphisms are precisely the bijective homomorphisms. An epimorphism need not be surjective. For example, the inclusion $\mathbb{Z} \hookrightarrow \mathbb{Q}$ is an epimorphism in the category of rings with unity, although it is not surjective. Any two ring homomorphisms from $\mathbb{Q}$ that agree on $\mathbb{Z}$ agree on every rational number.

## Composition and the automorphism group

If $\varphi : A \to B$ and $\psi : B \to C$ are homomorphisms between structures of the same type, their composite $\psi \circ \varphi : A \to C$ is a homomorphism. Each map preserves the given operations, so their composite preserves them. The identity map is an automorphism. The composite of two isomorphisms is an isomorphism, and the inverse of an isomorphism is an isomorphism. Isomorphism is therefore an equivalence relation, and its equivalence classes are the isomorphism classes.

For a fixed structure $A,$ the set $\mathrm{End}(A)$ of all endomorphisms of $A$ is closed under composition and contains the identity map $\mathrm{id}_A.$ It is a monoid, since composition is associative and an endomorphism need not have an inverse.

The bijective endomorphisms of $A$ are its automorphisms. Their set $\mathrm{Aut}(A)$ is closed under composition and inversion, so $(\mathrm{Aut}(A), \circ)$ is a [group](../groups/) called the automorphism group of $A.$

Each element $g$ of a group $G$ defines a map $c_g : G \to G$ by $c_g(x) = gxg^{-1}.$ For all $x, y \in G,$ we have $c_g(xy) = c_g(x)c_g(y),$ and $c_{g^{-1}}$ is the inverse of $c_g.$ Hence $c_g$ is an automorphism, called an inner automorphism. Two elements $x$ and $y$ are conjugate when $y = c_g(x)$ for some $g \in G.$ In $S_n,$ two permutations are conjugate if and only if, for each $\ell \in \{\ 1, 2, \ldots, n \ \},$ their disjoint cycle decompositions contain equally many $\ell$-cycles.

Consider the additive group $(\mathbb{Z}, +).$ An endomorphism $\varphi : \mathbb{Z} \to \mathbb{Z}$ is determined by $\varphi(1).$ For every positive integer $n,$ additivity gives:

$$\varphi(n) = \varphi(\underbrace{1 + 1 + \cdots + 1}_{n \text{ summands}}) = n\varphi(1)$$

The identity also holds for negative integers and zero, so $\varphi(n) = n\varphi(1)$ for every $n \in \mathbb{Z}.$ The endomorphism $\varphi$ is bijective if and only if $\varphi(1)$ is a generator of $\mathbb{Z},$ which means that $\varphi(1) = 1$ or $\varphi(1) = -1.$ Hence $\mathrm{Aut}(\mathbb{Z})$ has two elements, the identity and the map $n \mapsto -n.$ It is isomorphic to $\mathbb{Z}/2\mathbb{Z}.$

## Isomorphism theorems

The isomorphism theorems state relations between homomorphisms, substructures, and quotients. The first identifies a homomorphic image with a quotient by a kernel. The second compares a substructure with its image under a quotient map, and the third replaces two successive quotients with one quotient.

The first isomorphism theorem has the same form for groups, rings, modules, and vector spaces. If $\varphi : A \to B$ is a homomorphism, then the quotient of $A$ by the kernel of $\varphi$ is isomorphic to the image of $\varphi$:

$$A / \ker(\varphi) \cong \mathrm{im}(\varphi)$$

For a linear map with finite-dimensional domain, taking dimensions in this isomorphism gives the [rank-nullity theorem](../kernel-and-image-of-a-linear-map/).

The quotient depends on the type of structure. For [groups](../groups/), $A / \ker(\varphi)$ is the quotient group by a normal subgroup. For [rings](../rings/), it is the quotient ring by an ideal. For [modules](../modules/), it is the quotient module by a submodule. In each case the kernel has the type required to form the quotient. The induced map is defined by $\overline{\varphi}([a]) = \varphi(a).$ It is well-defined because two elements in the same class have the same image under $\varphi.$

> To identify a quotient with another structure, one can construct a surjective homomorphism onto that structure and calculate its kernel. If the kernel is the substructure that defines the quotient, the first isomorphism theorem gives the required isomorphism.

- - -

The second isomorphism theorem compares a subgroup with its image under a quotient map. If $H \leq G$ and $N \trianglelefteq G,$ then $H \cap N \trianglelefteq H,$ the product $HN$ is a subgroup of $G,$ and the quotient map $G \to G/N$ induces the isomorphism:

$$H/(H \cap N) \cong HN/N$$

For a ring, module, or vector space $A,$ let $M$ and $N$ be ideals, submodules, or subspaces, respectively. The isomorphism is:

$$M/(M \cap N) \cong (M + N)/N$$

In each case the quotient map has the intersection as its kernel, so the first isomorphism theorem gives the isomorphism.

- - -

The third isomorphism theorem describes quotients in stages. Let $X$ be a group, ring, module, or vector space, and let $N \subseteq M$ be normal subgroups, ideals, submodules, or subspaces of $X,$ respectively. Then $M/N$ is a normal subgroup, ideal, submodule, or subspace of $X/N,$ respectively, and the theorem gives the isomorphism:

$$(X/N)/(M/N) \cong X/M$$

The quotient map $X/N \to X/M$ has kernel $M/N,$ so the first isomorphism theorem gives this isomorphism.

## What isomorphism captures

An isomorphism preserves every property expressible in the language of the given algebraic structure. Two isomorphic groups may have different presentations, names for their elements, or notation for their operations, but they satisfy the same group-theoretic properties. The same statement holds for rings, fields, modules, and vector spaces.

Let $\mathrm{Aff}(n, \mathbb{R})$ be the group of affine maps $T_{A,\mathbf{b}}(\mathbf{x}) = A\mathbf{x} + \mathbf{b},$ where $A \in \mathrm{GL}(n, \mathbb{R})$ and $\mathbf{b} \in \mathbb{R}^n.$ Define a map from $\mathrm{Aff}(n, \mathbb{R})$ to $\mathrm{GL}(n+1, \mathbb{R})$ by:

$$
T_{A,\mathbf{b}} \longmapsto
\begin{pmatrix}
A & \mathbf{b} \\
0 & 1
\end{pmatrix}
$$

This map is an isomorphism onto the subgroup formed by these block matrices. The equation $T_{A,\mathbf{b}} \circ T_{C,\mathbf{d}} = T_{AC, A\mathbf{d} + \mathbf{b}}$ agrees with block matrix multiplication. The projection $p(T_{A,\mathbf{b}}) = A$ is a surjective homomorphism onto $\mathrm{GL}(n, \mathbb{R}),$ and its kernel is the group of translations $T_{I,\mathbf{b}}.$ The map $\mathbf{b} \mapsto T_{I,\mathbf{b}}$ is an isomorphism from the additive group $\mathbb{R}^n$ to this kernel.

The additive group $(\mathbb{Z}/2\mathbb{Z}, +),$ the multiplicative group $(\{\ 1, -1 \ \}, \cdot),$ and the symmetry group of an isosceles non-equilateral triangle are isomorphic. The map from $\mathbb{Z}/2\mathbb{Z}$ to $\{\ 1, -1 \ \}$ defined by $0 \mapsto 1$ and $1 \mapsto -1$ is one of these isomorphisms. Any theorem proved for one of the three groups holds for the other two after the elements and operations are relabelled.

The [logarithm](../logarithms/) is an isomorphism from the positive real numbers under multiplication to the real numbers under addition:

$$\log : (\mathbb{R}^{+}, \cdot) \to (\mathbb{R}, +)$$

The identity $\log(xy) = \log(x) + \log(y)$ proves that the map is a homomorphism, and the exponential function is its inverse.

> Isomorphism is not equality. Two isomorphic structures may have different underlying sets, and an isomorphism is a function between them. When only algebraic properties are under discussion, one often speaks of "the" cyclic group of order two. When the underlying sets or the chosen maps matter, as in homological algebra and arguments based on universal properties, an isomorphism class and a chosen representative are different data.
