---
title: Modules
source: https://algebrica.org/modules/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - basis
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

A module is the algebraic structure obtained by replacing the [field](../fields/) of scalars in the definition of a [vector space](../vector-spaces/) with a [ring](../rings/). The motivation is that several familiar constructions, such as [ideals](../rings/) inside a ring, [abelian groups](../groups/) regarded with their canonical $\mathbb{Z}$-action, and [polynomial rings](../polynomials/) viewed over their coefficient ring, all fit a single pattern in which the scalars need not be invertible. The resulting theory is broader than that of vector spaces and provides the common language used throughout commutative algebra and homological algebra.

Let $R$ be a ring with unity. A left module over $R$, or simply a left $R$-module, is an [abelian group](../groups/) $(M, +)$ equipped with a scalar multiplication $\cdot : R \times M \to M$ satisfying the following axioms:

+ Distributivity over module addition: for all $r \in R$ and $\mathbf{u}, \mathbf{v} \in M$, one has $r \cdot (\mathbf{u} + \mathbf{v}) = r \cdot \mathbf{u} + r \cdot \mathbf{v}$.
+ Distributivity over ring addition: for all $r, s \in R$ and $\mathbf{v} \in M$, one has $(r + s) \cdot \mathbf{v} = r \cdot \mathbf{v} + s \cdot \mathbf{v}$.
+ Compatibility with ring multiplication: for all $r, s \in R$ and $\mathbf{v} \in M$, one has $(rs) \cdot \mathbf{v} = r \cdot (s \cdot \mathbf{v})$.
+ Identity action: for all $\mathbf{v} \in M$, the multiplicative identity $1 \in R$ satisfies $1 \cdot \mathbf{v} = \mathbf{v}$.

A right module over $R$ is defined analogously, by placing the scalar on the right of the vector and reversing the compatibility condition to $\mathbf{v} \cdot (rs) = (\mathbf{v} \cdot r) \cdot s$. When $R$ is commutative the two notions coincide, and one speaks simply of an $R$-module.

> The ring $R$ over which $M$ is defined is called the ring of scalars of $M$. When $R$ is a [field](../fields/), the axioms reduce exactly to those of a vector space, so every vector space is a module and the theory of modules contains the theory of vector spaces as a special case.

## Properties

Several elementary consequences follow directly from the axioms. For any $\mathbf{v} \in M$, multiplication by the additive identity of the ring satisfies $0 \cdot \mathbf{v} = \mathbf{0}$. To see this, one writes:

$$0 \cdot \mathbf{v} = (0 + 0) \cdot \mathbf{v} = 0 \cdot \mathbf{v} + 0 \cdot \mathbf{v}$$

and then cancels $0 \cdot \mathbf{v}$ from both sides using the abelian group structure of $(M, +)$. An analogous argument shows that $r \cdot \mathbf{0} = \mathbf{0}$ for every $r \in R$, and that $(-r) \cdot \mathbf{v} = -(r \cdot \mathbf{v}) = r \cdot (-\mathbf{v})$ for all $r \in R$ and $\mathbf{v} \in M$. In particular, taking $r = 1$ one obtains $(-1) \cdot \mathbf{v} = -\mathbf{v}$.

A difference with respect to [vector spaces](../vector-spaces/) concerns the possible presence of nonzero elements that are annihilated by some nonzero scalar. An element $\mathbf{v} \in M$ is called a torsion element when there exists a nonzero $r \in R$ such that $r \cdot \mathbf{v} = \mathbf{0}$. The set of all torsion elements of $M$ is denoted $T(M)$, and when $R$ is an [integral domain](../rings/) it is a submodule of $M$. A module is called torsion-free when $T(M) = \\{\ \mathbf{0} \ \\}$, and a torsion module when $T(M) = M$. The absence of torsion is precisely the property that vector spaces enjoy automatically, since in a [field](../fields/) the equation $\alpha \cdot \mathbf{v} = \mathbf{0}$ with $\alpha \neq 0$ forces $\mathbf{v} = \mathbf{0}$ by invertibility of $\alpha$.

## Algebraic hierarchy

The structures introduced so far form a chain of increasing rigidity. A [group](../groups/) carries one operation with inverses. A [ring](../rings/) carries two operations, with inverses guaranteed only for addition. A [field](../fields/) carries two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication. A [vector space](../vector-spaces/) is then built on top of a field, with the field acting on a separate set of vectors by scaling.

A module sits between rings and vector spaces in this picture. It is constructed in the same way as a vector space, but the field of scalars is replaced by a ring. The loss of multiplicative inverses for general scalars produces a theory that is significantly richer in pathologies:

+ Bases need not exist.
+ Rank, when defined, need not be invariant for arbitrary rings.
+ Torsion phenomena appear and play a structural role.

> Every vector space is a module over its field of scalars, and every abelian group is a module over the ring of [integers](../integers/). The category of modules over a ring $R$ generalises both vector spaces and abelian groups, and reduces to either of them in the appropriate special case.

## Examples

The most fundamental example is the following. Every abelian group $(A, +)$ carries a unique structure of $\mathbb{Z}$-module, in which the scalar multiplication of an [integer](../integers/) $n$ by an element $a \in A$ is defined by repeated addition. For $n > 0$ one sets:

$$n \cdot a = \underbrace{a + a + \cdots + a}_{n \text{ summands}}$$

For $n < 0$ one sets $n \cdot a = -((-n) \cdot a)$, and for $n = 0$ one sets $0 \cdot a = 0$. The four module axioms reduce in this case to standard properties of integer multiples in an abelian group, so the theory of $\mathbb{Z}$-modules and the theory of abelian groups coincide.

Let $R$ be a ring and let $n$ be a positive integer. The set $R^n$ of ordered $n$-tuples with entries in $R$, equipped with componentwise addition and componentwise scalar multiplication, is an $R$-module. This is the direct generalisation of the [vector space](../vector-spaces/) $F^n$ considered over a field $F$. When $R = \mathbb{Z}$, the module $\mathbb{Z}^n$ is the prototypical example of a free module of finite rank.

- - -

Every ring $R$ is a module over itself, with scalar multiplication given by the ring multiplication. The submodules of $R$ regarded as a left $R$-module are precisely the [left ideals](../rings/) of $R$. This perspective unifies the language of ideals and modules and provides one of the chief motivations for studying modules in commutative algebra.

The set $\mathbb{Z}/n\mathbb{Z}$ is an abelian group of order $n$ under addition [modulo](../modulo-operator/) $n$, so by the construction above it is a $\mathbb{Z}$-module. Every element $\bar{a} \in \mathbb{Z}/n\mathbb{Z}$ satisfies $n \cdot \bar{a} = 0$, so the entire module is torsion. This shows that even a finitely generated $\mathbb{Z}$-module need not admit a basis, since the existence of a torsion element prevents any subset containing it from being linearly independent.

## Submodules

A nonempty subset $N \subseteq M$ is called a submodule of $M$ when $N$ is itself an $R$-module under the operations inherited from $M$. Equivalently, $N$ is a submodule when for all $\mathbf{u}, \mathbf{v} \in N$ and all $r \in R$ one has $\mathbf{u} + \mathbf{v} \in N$ and $r \cdot \mathbf{v} \in N$. The two conditions together express closure under arbitrary $R$-linear combinations, and they imply that the zero element $\mathbf{0}$ belongs to every submodule.

Every module $M$ has at least two submodules: the trivial submodule $\\{\ \mathbf{0} \ \\}$ and $M$ itself. Any submodule different from $M$ is called a proper submodule.

As an example, consider the $\mathbb{Z}$-module $\mathbb{Z}$ and the subset $2\mathbb{Z}$ of even integers. For any $a, b \in 2\mathbb{Z}$ the sum $a + b$ is again even, and for any $n \in \mathbb{Z}$ and $a \in 2\mathbb{Z}$ the product $n \cdot a$ is also even. Both closure conditions are satisfied, so $2\mathbb{Z}$ is a submodule of $\mathbb{Z}$. More generally, every [subgroup](../groups/) of an abelian group $A$ is automatically a $\mathbb{Z}$-submodule of $A$, since the additive structure already controls integer scalar multiplication.

## Free modules and bases

A subset $S \subseteq M$ is called linearly independent over $R$ when the only finite combination:

$$r_1 \mathbf{v}_1 + r_2 \mathbf{v}_2 + \cdots + r_k \mathbf{v}_k = \mathbf{0}$$

with $\mathbf{v}_i \in S$ and $r_i \in R$ is the trivial one in which every coefficient $r_i$ is equal to zero. The set $S$ is said to span $M$ when every element of $M$ can be written as a finite $R$-[linear combination](../linear-combinations/) of elements of $S$. A basis of $M$ is a linearly independent spanning set.

A module that admits a basis is called a free module, and the cardinality of any basis is called its rank. For modules over a commutative ring the rank is well-defined, in the sense that any two bases have the same cardinality. The module $R^n$ is free of rank $n$ over $R$, with basis given by the canonical $n$-tuples having a $1$ in one position and $0$ in all others.

Not every module is free. The $\mathbb{Z}$-module $\mathbb{Z}/n\mathbb{Z}$ admits no basis whenever $n > 1$, since every element is annihilated by $n$ and cannot belong to a linearly independent set. This is the precise point at which the analogy with vector spaces breaks down. Over a [field](../fields/) every module is free, and the rank coincides with the dimension. Over a general ring, freeness is the exception rather than the rule.

> The integers $\mathbb{Z}$, regarded as a $\mathbb{Z}$-module, are free of rank $1$ with basis $\\{\ 1 \ \\}$. The module $\mathbb{Z}/2\mathbb{Z}$, by contrast, is generated by the single element $\bar{1}$, but $\bar{1}$ is not linearly independent because $2 \cdot \bar{1} = 0$ holds in $\mathbb{Z}/2\mathbb{Z}$ while $2 \neq 0$ in $\mathbb{Z}$.

## Module homomorphisms and isomorphisms

A module homomorphism, also called an $R$-linear map, is a [function](../functions/) $\varphi : M \to N$ between two left $R$-modules that preserves both the additive structure and the action of the ring. Explicitly, $\varphi$ is a homomorphism when for all $\mathbf{u}, \mathbf{v} \in M$ and all $r \in R$ the following two identities hold:

$$\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})$$

$$\varphi(r \cdot \mathbf{v}) = r \cdot \varphi(\mathbf{v})$$

These two conditions can be combined into the single requirement that $\varphi(r\mathbf{u} + s\mathbf{v}) = r \varphi(\mathbf{u}) + s \varphi(\mathbf{v})$ for all $r, s \in R$ and $\mathbf{u}, \mathbf{v} \in M$. The kernel and image of a module homomorphism are defined as follows:

$$\ker(\varphi) = \\{\ \mathbf{v} \in M : \varphi(\mathbf{v}) = \mathbf{0} \ \\}$$

$$\operatorname{im}(\varphi) = \\{\ \varphi(\mathbf{v}) : \mathbf{v} \in M \ \\}$$

The kernel is a submodule of $M$, and the image is a submodule of $N$. A homomorphism is injective if and only if its kernel reduces to the zero submodule.

- - -

A module homomorphism that is bijective is called a module isomorphism, and two modules are isomorphic, written $M \cong N$, when an isomorphism between them exists. As an illustration of how flexible the notion can be, consider the $\mathbb{Z}$-module $\mathbb{Z}$ and the map $\varphi : \mathbb{Z} \to \mathbb{Z}$ defined by $\varphi(a) = 2a$. For any $a, b \in \mathbb{Z}$ one has:

$$
\begin{align}
\varphi(a + b) &= 2(a + b) \\[6pt]
               &= 2a + 2b \\[6pt]
               &= \varphi(a) + \varphi(b)
\end{align}
$$

A direct verification also shows $\varphi(n \cdot a) = 2na = n \cdot \varphi(a)$ for every $n \in \mathbb{Z}$, so $\varphi$ is $\mathbb{Z}$-linear. Its kernel is the trivial submodule $\\{\ 0 \ \\}$, so $\varphi$ is injective, and its image is the proper submodule $2\mathbb{Z}$. The map $\varphi$ is therefore an isomorphism between $\mathbb{Z}$ and its proper submodule $2\mathbb{Z}$, a phenomenon that cannot occur for finite-dimensional [vector spaces](../vector-spaces/), where an injective linear map from a space to itself is necessarily surjective.

> The example above highlights one of the most important differences between modules and vector spaces. The rank-nullity theorem and the equivalence between injectivity and surjectivity for endomorphisms of finite-dimensional spaces both rely on the absence of torsion and on the freeness of every vector space, properties that fail in the general module-theoretic setting.
