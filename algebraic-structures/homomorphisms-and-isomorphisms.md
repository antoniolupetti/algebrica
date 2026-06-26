---
title: Homomorphisms and Isomorphisms
source: https://algebrica.org/homomorphisms-and-isomorphisms/
license: CC BY-NC 4.0
tags:
  - algebraic-structures
  - automorphism
  - endomorphism
  - epimorphism
  - homomorphism
  - image
  - isomorphism
  - kernel
  - monomorphism
---
## The general idea

A homomorphism is a [function](../functions/) between two algebraic structures of the same type that preserves the operations defining that type. The notion appears under different names and with slightly different requirements when one moves from groups to rings, from rings to modules, or from [modules](../modules/) to [vector spaces](../vector-spaces), yet the underlying principle is uniform: a structure-preserving map between objects of the same kind.

The algebraic structures introduced in this section all share a common shape. Each one consists of a set together with one or more binary operations, such as addition, multiplication, or scalar action, and possibly a few distinguished elements such as an identity or a zero. 

A homomorphism from one such structure to another is a function between the underlying [sets](../sets/) that commutes with every operation and respects every distinguished element. The specific axioms attached to a particular family enter the definition only by determining the list of operations that must be preserved.

> A more refined perspective treats homomorphisms as the morphisms of a category whose objects are the algebraic structures themselves. The categorical viewpoint clarifies which constructions, such as kernel, image, and quotient, belong to a single conceptual framework rather than being reformulated separately for each family of structures.

## Specialisations across the standard families

A [group](../groups/) is a set with one operation. A group homomorphism $\varphi : (G, \cdot) \to (H, \star)$ is a function such that:

$$\varphi(a \cdot b) = \varphi(a) \star \varphi(b)$$

for all $a, b \in G.$ Compatibility with identities and inverses is then automatic, in the sense that $\varphi(e_G) = e_H$ and $\varphi(a^{-1}) = \varphi(a)^{-1}$ follow from the single equation above.

A [ring](../rings/) is a set with two operations. A ring homomorphism $\varphi : R \to S$ is a function satisfying both:

$$\varphi(a + b) = \varphi(a) + \varphi(b)$$

$$\varphi(a \cdot b) = \varphi(a) \cdot \varphi(b)$$

for all $a, b \in R.$ For unital rings one usually adds the condition $\varphi(1_R) = 1_S,$ which is not a consequence of the previous two.

A [field](../fields/) is a commutative ring with unity in which every nonzero element is invertible. A field homomorphism is a ring homomorphism between fields. Every field homomorphism is automatically injective, because its kernel is an ideal of the source field, and the only ideals of a field are the trivial ideal and the field itself.

A [module](../modules/) over a ring $R$ is an abelian group equipped with a compatible scalar action of $R.$ A module homomorphism, also called an $R$-linear map, $\varphi : M \to N$ satisfies:

$$\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})$$

$$\varphi(r \cdot \mathbf{v}) = r \cdot \varphi(\mathbf{v})$$

for all $\mathbf{u}, \mathbf{v} \in M$ and all $r \in R.$ A linear map between [vector spaces](../vector-spaces/) is the same notion specialised to the case in which the scalars form a field.

> Each case adds the conditions corresponding to the operations that define the structure under consideration. As the structure becomes richer, the definition of a homomorphism grows accordingly, and no condition imposed at a previous stage is ever dropped.

## Kernel and image

When the codomain admits a distinguished neutral element, denoted by $e_B$ and equal to the identity for groups or to the zero element for additive structures, the kernel of a homomorphism $\varphi : A \to B$ is the preimage of this element:

$$\ker(\varphi) = \\{\ a \in A : \varphi(a) = e_B \ \\}$$

The image of $\varphi$ is defined uniformly for every family of structures:

$$\mathrm{im}(\varphi) = \\{\ \varphi(a) : a \in A \ \\}$$

Both subsets carry intrinsic algebraic meaning. The kernel is always a substructure of $A$ of a specific kind: a normal subgroup when $A$ is a [group](../groups/), an ideal when $A$ is a [ring](../rings/), a submodule when $A$ is a [module](../modules/). The image is always a substructure of $B$ of the same type as $B$ itself. In every case the homomorphism $\varphi$ is injective if and only if its kernel is the trivial substructure, namely the subgroup containing only the identity, the zero ideal, or the zero submodule, respectively.

> The kernel measures the failure of $\varphi$ to be injective. Two elements $a, a' \in A$ have the same image under $\varphi$ if and only if their difference (in the additive case) or their quotient (in the multiplicative case) belongs to $\ker(\varphi).$ The kernel is therefore exactly the information that $\varphi$ discards.

## Monomorphisms, epimorphisms, isomorphisms

Specialised classes of homomorphism receive their own names according to injectivity, surjectivity, or the relation between domain and codomain:

+ A monomorphism is an injective homomorphism.
+ An epimorphism is a surjective homomorphism.
+ An isomorphism is a bijective homomorphism.
+ An endomorphism is a homomorphism from a structure to itself.
+ An automorphism is a bijective endomorphism, that is, an isomorphism from a structure to itself.

When an isomorphism $\varphi : A \to B$ exists, the structures $A$ and $B$ are said to be isomorphic, written $A \cong B.$ Isomorphic structures are indistinguishable at the algebraic level. Every property formulated in the language of the relevant axioms transfers from one to the other through $\varphi.$

> The categorical notion of monomorphism agrees with injectivity for groups, rings, modules, and vector spaces, and so does the categorical notion of isomorphism with bijectivity. The categorical notion of epimorphism, by contrast, can be strictly weaker than surjectivity. The inclusion $\mathbb{Z} \hookrightarrow \mathbb{Q}$ is an epimorphism in the category of rings even though it is not surjective, since any two ring homomorphisms out of $\mathbb{Q}$ that agree on the image of $\mathbb{Z}$ must agree everywhere.

## Composition and the automorphism group

The composition of two homomorphisms is again a homomorphism. Given $\varphi : A \to B$ and $\psi : B \to C$ of the same type, the composite $\psi \circ \varphi : A \to C$ preserves all the operations involved, because each is preserved separately by $\varphi$ and by $\psi.$ The composition of two isomorphisms is an isomorphism, and the inverse of an isomorphism is itself an isomorphism. The relation of being isomorphic is therefore reflexive, symmetric, and transitive, and it partitions any class of structures into isomorphism classes.

For a fixed structure $A,$ the collection $\mathrm{End}(A)$ of all endomorphisms of $A$ is closed under composition and contains the identity map $\mathrm{id}_A.$ It forms a monoid, that is, an associative structure with an identity element but without inverses in general. 

Restricting attention to endomorphisms that are bijective yields the set $\mathrm{Aut}(A)$ of automorphisms of $A,$ which is closed under composition and under inversion. The structure $(\mathrm{Aut}(A), \circ)$ is a [group](../groups/), called the automorphism group of $A.$

As a concrete example, consider the additive group $(\mathbb{Z}, +).$ An endomorphism $\varphi : \mathbb{Z} \to \mathbb{Z}$ is determined by the value $\varphi(1).$ For every positive integer $n$ one has:

$$\varphi(n) = \varphi(\underbrace{1 + 1 + \cdots + 1}_{n \text{ summands}}) = n\varphi(1)$$

The same identity extends by additivity to negative integers and to zero, giving $\varphi(n) = n\varphi(1)$ for every $n \in \mathbb{Z}.$ The endomorphism $\varphi$ is bijective when $\varphi(1)$ is a generator of $\mathbb{Z},$ that is, when $\varphi(1) = 1$ or $\varphi(1) = -1.$ The automorphism group $\mathrm{Aut}(\mathbb{Z})$ therefore consists of exactly two elements, the identity and the map $n \mapsto -n,$ and is isomorphic to $\mathbb{Z}/2\mathbb{Z}.$

## The first isomorphism theorem

A theorem of central importance recurs in every family of structures considered here, with a statement that takes the same shape in each case. Given a homomorphism $\varphi : A \to B,$ the quotient of $A$ by the kernel of $\varphi$ is isomorphic to the image of $\varphi$:

$$A / \ker(\varphi) \cong \mathrm{im}(\varphi)$$

The meaning of the quotient depends on the family of structures involved. For [groups](../groups/), $A / \ker(\varphi)$ denotes the quotient group by a normal subgroup. For [rings](../rings/), it denotes the quotient ring by an ideal. For [modules](../modules/), it denotes the quotient module by a submodule. In each case the construction is available precisely because the kernel is the kind of substructure that admits a quotient, and the resulting bijection is induced by the assignment $a \cdot \ker(\varphi) \mapsto \varphi(a).$ This map is well-defined because two elements of the same coset have the same image under $\varphi.$

> The first isomorphism theorem reduces the classification of certain quotient structures to the construction of suitable homomorphisms. To show that a given quotient is isomorphic to a particular target, it is often enough to produce a surjective homomorphism whose kernel coincides with the required substructure.

## What isomorphism captures

Isomorphism is the formal notion of equivalence at the level of algebraic structure. Two groups that are isomorphic may have entirely different presentations, names for their elements, or notations for their operations, and they nevertheless share every property expressible in the language of group theory alone. The same applies to rings, fields, modules, and vector spaces.

A useful illustration is provided by the cyclic group of order two. The group $(\mathbb{Z}/2\mathbb{Z}, +),$ the multiplicative group $\\{\ 1, -1 \ \\}$ under ordinary multiplication, and the group of symmetries of an isosceles non-equilateral triangle all appear in unrelated contexts. The three structures are nevertheless isomorphic, and any theorem proved for one of them automatically holds for the other two after the appropriate relabelling of elements and operations.

> Isomorphism is not equality. Two isomorphic structures remain distinct sets of distinct objects, and the isomorphism is a specific function that translates between them. In most contexts this distinction is harmless and one speaks loosely of "the" cyclic group of order two. In settings where the underlying sets matter, for instance in homological algebra or in arguments based on universal properties, the isomorphism class and a chosen representative play different roles.
