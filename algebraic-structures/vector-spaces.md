---
title: Vector Spaces
source: https://algebrica.org/vector-spaces/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - basis
  - dimension
  - direct-sum
  - field
  - homomorphism-theorem
  - linear-combination
  - linear-independence
  - linear-map
  - quotient-space
  - rank-nullity-theorem
  - subspace
  - vector-space
---
## Definition

A vector space is an algebraic structure that formalises the idea of quantities that can be scaled and [combined linearly](../linear-combinations/). The concept arises wherever one encounters objects that can be added and multiplied by numbers in a coherent way: geometric arrows in the plane, [polynomials](../polynomials/) with real coefficients, sequences of [real numbers](../real-numbers/), and [continuous functions](../continuous-functions/) on an interval all share this common pattern.

Unlike a [group](../groups/) or a [ring](../rings/), which are defined on a single set, a vector space involves two distinct sets: a [field](../fields/) $F,$ whose elements are called scalars, and a set $V,$ whose elements are called [vectors](../vectors/). A vector space over $F$ is a set $V$ together with two operations, vector addition $+ : V \times V \to V$ and scalar multiplication $\cdot : F \times V \to V,$ satisfying the following axioms:

+ $(V, +)$ is an abelian group. There exists a zero vector $\mathbf{0} \in V$ such that $\mathbf{v} + \mathbf{0} = \mathbf{v}$ for all $\mathbf{v} \in V,$ and every vector $\mathbf{v}$ has an additive inverse $-\mathbf{v}.$
+ Compatibility with field multiplication: for all $\alpha, \beta \in F$ and $\mathbf{v} \in V,$ the identity $\alpha \cdot (\beta \cdot \mathbf{v}) = (\alpha\beta) \cdot \mathbf{v}$ holds.
+ Identity element of scalar multiplication: for all $\mathbf{v} \in V,$ the multiplicative identity $1 \in F$ satisfies $1 \cdot \mathbf{v} = \mathbf{v}.$
+ Distributivity of scalar multiplication over vector addition: for all $\alpha \in F$ and $\mathbf{u}, \mathbf{v} \in V,$ the identity $\alpha \cdot (\mathbf{u} + \mathbf{v}) = \alpha \cdot \mathbf{u} + \alpha \cdot \mathbf{v}$ holds.
+ Distributivity of scalar multiplication over field addition: for all $\alpha, \beta \in F$ and $\mathbf{v} \in V,$ the identity $(\alpha + \beta) \cdot \mathbf{v} = \alpha \cdot \mathbf{v} + \beta \cdot \mathbf{v}$ holds.

> The field $F$ over which $V$ is defined is called the scalar field of $V.$ In most applications encountered at the undergraduate level, $F$ is either $\mathbb{R}$ or $\mathbb{C},$ and one speaks of a real vector space or a complex vector space accordingly.

## Properties

Several elementary consequences follow directly from the axioms. For any scalar $\alpha \in F$ and any vector $\mathbf{v} \in V,$ multiplication by zero satisfies $0 \cdot \mathbf{v} = \mathbf{0}.$ To see this:

$$0 \cdot \mathbf{v} = (0 + 0) \cdot \mathbf{v} = 0 \cdot \mathbf{v} + 0 \cdot \mathbf{v}$$

and the cancellation of $0 \cdot \mathbf{v}$ from both sides through the group structure of $(V, +)$ yields the result. Similarly, for any $\mathbf{v} \in V$ one has $\alpha \cdot \mathbf{0} = \mathbf{0}$ and $(-1) \cdot \mathbf{v} = -\mathbf{v},$ and more generally $(-\alpha) \cdot \mathbf{v} = -(\alpha \cdot \mathbf{v})$ for every $\alpha \in F.$

When $\alpha \cdot \mathbf{v} = \mathbf{0},$ either $\alpha = 0$ or $\mathbf{v} = \mathbf{0}.$ This is a direct consequence of the invertibility of nonzero scalars: when $\alpha \neq 0$:

$$\mathbf{v} = 1 \cdot \mathbf{v} = (\alpha^{-1}\alpha) \cdot \mathbf{v} = \alpha^{-1} \cdot (\alpha \cdot \mathbf{v}) = \alpha^{-1} \cdot \mathbf{0} = \mathbf{0}$$

This property is the vector space analogue of the absence of zero divisors in a field, and the theory of linear independence relies on it.

Distinct scalars give distinct multiples of a fixed nonzero vector. When $\mathbf{v} \neq \mathbf{0}$ and $\alpha \neq \beta,$ the difference $(\alpha - \beta) \cdot \mathbf{v}$ is nonzero by the property just proved, so $\alpha \cdot \mathbf{v} \neq \beta \cdot \mathbf{v}.$ Over an infinite field such as $\mathbb{R}$ this forces every nontrivial space to be infinite, since a single nonzero vector $\mathbf{v}$ already produces one distinct multiple $\alpha \cdot \mathbf{v}$ for each scalar $\alpha.$ A real vector space therefore has either one element or infinitely many, and the trivial space $\{\ \mathbf{0} \ \}$ is the only finite one.

## Algebraic hierarchy

A vector space sits above groups, rings, and fields in the standard classification of algebraic structures, since it depends on the presence of a field of scalars.

A group consists of a set with a single operation admitting inverses. A ring introduces a second operation that need not be invertible. A field requires both operations to be fully invertible on nonzero elements. A vector space then takes a field as a given and builds a new structure on top of it, one in which the field acts on a separate set of vectors by scaling. The three underlying structures form a chain of increasing rigidity:

+ A group has one operation with inverses.
+ A ring has two operations, with inverses guaranteed only for addition.
+ A field has two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication.

> A vector space is not itself a further step in this chain but rather a structure that presupposes a field. Every vector space over $\mathbb{R}$ or $\mathbb{C}$ depends on the field axioms being in force for its scalar multiplication to be well defined. When the scalars are drawn from a [ring](../rings/) rather than a field, the resulting structure is a [module](../modules/), which generalises the notion of a vector space and is treated on the dedicated page.

## Examples

The smallest vector space is the trivial one, $\{\ \mathbf{0} \ \},$ consisting of the zero vector alone over any field $F.$ The operations are forced: $\mathbf{0} + \mathbf{0} = \mathbf{0}$ and $\alpha \cdot \mathbf{0} = \mathbf{0}$ for every $\alpha \in F.$ Its basis is the empty set, so it has dimension $0,$ and it is the only vector space of dimension $0.$

The set $\mathbb{R}^n$ of all ordered $n$-tuples of real numbers is a vector space over $\mathbb{R}$ under componentwise addition and scalar multiplication. For $n = 2,$ addition is defined by $(a_1, a_2) + (b_1, b_2) = (a_1 + b_1, a_2 + b_2)$ and scalar multiplication by $\alpha \cdot (a_1, a_2) = (\alpha a_1, \alpha a_2).$ The zero vector is $(0, 0).$ This is the prototype of a finite-dimensional real vector space, and it gives the geometric intuition for the general theory.

The same construction works over any field. For a field $F,$ the set $F^n$ is an $F$-vector space with the standard basis $\mathbf{e}_1, \ldots, \mathbf{e}_n.$ This includes $\mathbb{Q}^n$ over $\mathbb{Q}$ and $\mathbb{F}_p^n$ over the finite field $\mathbb{F}_p,$ where $p$ is prime.

The set $\mathbb{C}^n$ of all ordered $n$-tuples of complex numbers is a vector space over $\mathbb{C}$ under the analogous operations. It can also be regarded as a vector space over $\mathbb{R},$ though in that case its dimension doubles: $\mathbb{C}^n$ as a real vector space has dimension $2n.$

The set $M_{m \times n}(\mathbb{R})$ of all [matrices](../matrices/) with $m$ rows and $n$ columns and real entries is a vector space over $\mathbb{R}$ under entrywise addition and scalar multiplication. The sum of $A = (a_{ij})$ and $B = (b_{ij})$ is the matrix with entries $a_{ij} + b_{ij},$ and the scalar multiple $\alpha A$ has entries $\alpha a_{ij}.$ The zero vector is the matrix with every entry equal to $0.$ A basis consists of the $mn$ matrices having a single entry equal to $1$ and all others $0,$ so this space has dimension $mn.$ A single row reproduces $\mathbb{R}^n$ as $M_{1 \times n}(\mathbb{R}),$ and a single column gives the same space as $M_{n \times 1}(\mathbb{R}),$ so [row and column vectors](../vectors/) are particular matrices. When $m = n$ the matrices are square of order $n,$ and $M_{n \times n}(\mathbb{R})$ has dimension $n^2.$

- - -

The set $\mathbb{R}[x]_{\leq n}$ of all [polynomials](../polynomials/) with real coefficients of degree at most $n$ is a vector space over $\mathbb{R}$ under the usual addition of polynomials and multiplication of a polynomial by a real constant. The zero vector is the zero polynomial. A natural basis for this space is $\{\ 1, x, x^2, \ldots, x^n \ \},$ which contains $n + 1$ elements, so the dimension of this space is $n + 1.$ Removing the bound on the degree gives the space $\mathbb{R}[x]$ of all real polynomials, with basis $\{\ 1, x, x^2, \ldots \ \}$ and infinite dimension.

The set $\mathcal{C}([a, b])$ of all continuous real-valued functions on a closed interval $[a, b]$ is a vector space over $\mathbb{R}$ under pointwise addition and scalar multiplication: $(f + g)(x) = f(x) + g(x)$ and $(\alpha f)(x) = \alpha f(x).$ This space is infinite-dimensional, since the monomials $1, x, x^2, \ldots$ form a linearly independent subset with no finite spanning set.

More generally, if $X$ is any nonempty set, the set $F^X$ of all functions $f : X \to F$ is a vector space over $F.$ Both operations are defined pointwise, so $(f + g)(x) = f(x) + g(x)$ and $(\alpha f)(x) = \alpha f(x)$ for every $x \in X.$ When $I$ is an interval, the continuous real-valued functions on $I$ form a subspace of $\mathbb{R}^I,$ and the differentiable real-valued functions form a subspace of the continuous ones. For a fixed $x_0 \in X,$ the functions satisfying $f(x_0) = 0$ form a subspace of $F^X.$

## Subspaces

A nonempty subset $W \subseteq V$ is called a subspace of $V$ when $W$ is itself a vector space over $F$ under the operations inherited from $V.$ Rather than verifying all axioms separately, it is sufficient to check two conditions: for all $\mathbf{u}, \mathbf{v} \in W$ and all $\alpha \in F,$ the membership $\mathbf{u} + \mathbf{v} \in W$ and $\alpha \cdot \mathbf{v} \in W$ must hold. These two conditions together are called closure under linear combinations. The zero vector $\mathbf{0}$ must belong to every subspace, since setting $\alpha = 0$ gives $0 \cdot \mathbf{v} = \mathbf{0} \in W.$

Equivalently, a nonempty subset $W$ is a subspace when $\alpha\mathbf{u} + \beta\mathbf{v} \in W$ for every $\mathbf{u}, \mathbf{v} \in W$ and $\alpha, \beta \in F.$ This formulation makes two closure properties immediate. The intersection of any family of subspaces is a subspace, where the intersection of the empty family is understood as $V.$ The sum of two subspaces $A$ and $B,$ defined by $A + B = \{\ a + b \mid a \in A, b \in B\ \},$ is the smallest subspace containing both $A$ and $B.$

For any subset $S \subseteq V,$ the span of $S$ is the set of its finite linear combinations. It is given by:

$$\mathrm{span}(S) = \{\ \alpha_1\mathbf{v}_1 + \cdots + \alpha_n\mathbf{v}_n \mid n \geq 1,\ \alpha_i \in F,\ \mathbf{v}_i \in S\ \}$$

By convention, $\mathrm{span}(\varnothing) = \{\ \mathbf{0}\ \}.$ Closure under linear combinations shows that $\mathrm{span}(S)$ is a subspace. Every subspace containing $S$ contains each finite linear combination of elements of $S,$ so $\mathrm{span}(S)$ is also the unique smallest subspace containing $S.$ Equivalently, it is the intersection of all subspaces of $V$ that contain $S.$

As an example, the set $W = \{\ (x, y) \in \mathbb{R}^2 : y = 2x \ \}$ is a subspace of $\mathbb{R}^2.$ For any two vectors $(x_1, 2x_1)$ and $(x_2, 2x_2)$ in $W,$ their sum $(x_1 + x_2, 2x_1 + 2x_2) = (x_1 + x_2, 2(x_1 + x_2))$ belongs to $W,$ and for any scalar $\alpha \in \mathbb{R}$ the vector $\alpha(x_1, 2x_1) = (\alpha x_1, 2\alpha x_1)$ also belongs to $W.$ Both conditions are satisfied, so $W$ is a subspace of $\mathbb{R}^2.$ Geometrically, $W$ is the line through the origin with slope $2.$

![IMG. 1](svg/vector-spaces-1.svg)

> Any vector in $W$ lies on the line through the origin with slope $2.$ Adding two such vectors or multiplying one by a scalar always produces a vector that remains on the same line, so $W$ is closed under both operations.

If $W$ is a subspace of $V,$ its additive cosets form the quotient set:

$$V/W = \{\ \mathbf{v} + W \mid \mathbf{v} \in V\ \}$$

The quotient becomes a vector space over $F$ when addition and scalar multiplication are defined by:

$$(\mathbf{u} + W) + (\mathbf{v} + W) = (\mathbf{u} + \mathbf{v}) + W$$

$$\alpha(\mathbf{v} + W) = \alpha\mathbf{v} + W$$

Both operations are well defined. If $\mathbf{u} + W = \mathbf{u}' + W$ and $\mathbf{v} + W = \mathbf{v}' + W,$ then $(\mathbf{u} + \mathbf{v}) - (\mathbf{u}' + \mathbf{v}') \in W.$ Likewise, $\mathbf{v} - \mathbf{v}' \in W$ implies $\alpha\mathbf{v} - \alpha\mathbf{v}' \in W$ by closure under scalar multiplication. The quotient map $\pi : V \to V/W,$ defined by $\pi(\mathbf{v}) = \mathbf{v} + W,$ is linear and surjective, and its kernel is $W.$

The homomorphism theorem describes every quotient obtained from a linear map. If $T : V \to U$ is linear, the induced map $\overline{T} : V/\ker(T) \to \mathrm{im}(T)$ is defined by:

$$\overline{T}(\mathbf{v} + \ker(T)) = T(\mathbf{v})$$

It is a linear isomorphism. The map is well defined because two representatives differ by an element of $\ker(T),$ and its linearity follows from the linearity of $T.$ It is injective because $\overline{T}(\mathbf{v} + \ker(T)) = \mathbf{0}$ forces $\mathbf{v} \in \ker(T),$ and it is surjective by the definition of the image.

When $T : V \to U$ is surjective, inverse image gives a bijection between the subspaces of $U$ and the subspaces of $V$ that contain $\ker(T).$ The two inverse assignments are $L \mapsto T^{-1}(L)$ and $M \mapsto T(M).$ More generally, if $N \subseteq \ker(T),$ then $T$ factors uniquely through $V/N.$ If $\pi_N : V \to V/N$ is the quotient map, the formula $\widetilde{T}(\mathbf{v} + N) = T(\mathbf{v})$ defines a linear map satisfying $T = \widetilde{T} \circ \pi_N.$

Two further isomorphisms express how nested and intersecting subspaces behave. If $N \subseteq M \subseteq V,$ then:

$$(V/N)/(M/N) \cong V/M$$

If $A$ and $N$ are subspaces of $V,$ then $A + N$ is a subspace and:

$$(A + N)/N \cong A/(A \cap N)$$

The second isomorphism is induced by the map $A \to (A + N)/N$ that sends $\mathbf{a}$ to $\mathbf{a} + N.$ Its kernel is $A \cap N,$ and every coset in $(A + N)/N$ has a representative in $A.$

## Basis and dimension

Linear independence is a finitary condition even when the subset under consideration is infinite. A subset $S \subseteq V$ is linearly independent when every equation involving finitely many distinct vectors $\mathbf{v}_1, \ldots, \mathbf{v}_n \in S$ has only the trivial coefficients. The empty set is linearly independent, while any subset containing $\mathbf{0}$ is linearly dependent.

A set of vectors $\{\ \mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n \ \}$ in $V$ is called linearly independent when the only solution to the equation:

$$\alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2 + \cdots + \alpha_n \mathbf{v}_n = \mathbf{0}$$

is $\alpha_1 = \alpha_2 = \cdots = \alpha_n = 0.$ A set of vectors that is not linearly independent is called linearly dependent, which means that at least one vector in the set can be expressed as a [linear combination](../linear-combinations/) of the others. A basis of $V$ is a linearly independent set of vectors that spans $V,$ meaning that every vector in $V$ can be written as a linear combination of the basis vectors. The representation of any vector in terms of a given basis is unique. If:

$$\mathbf{v} = \alpha_1 \mathbf{v}_1 + \cdots + \alpha_n \mathbf{v}_n = \beta_1 \mathbf{v}_1 + \cdots + \beta_n \mathbf{v}_n$$

then subtracting yields:

$$(\alpha_1 - \beta_1)\mathbf{v}_1 + \cdots + (\alpha_n - \beta_n)\mathbf{v}_n = \mathbf{0}$$

and linear independence forces $\alpha_k = \beta_k$ for all $k.$

A basis $B$ admits two equivalent descriptions:

+ $B$ is a minimal spanning set, so $B$ spans $V$ and no proper subset of $B$ spans $V.$
+ $B$ is a maximal linearly independent set, so $B$ is linearly independent and no proper superset of $B$ in $V$ is linearly independent.

If a spanning set is linearly dependent, one of its vectors is a linear combination of the others and can be removed without changing the span. A minimal spanning set is therefore linearly independent. Removing a vector from a basis prevents the remaining set from spanning $V,$ since otherwise the removed vector would be a linear combination of the others. Thus every basis is minimal spanning. If $B$ is a basis and $\mathbf{v} \notin B,$ then $\mathbf{v} \in \mathrm{span}(B),$ so adjoining $\mathbf{v}$ makes the set linearly dependent. Hence every basis is maximal linearly independent. Conversely, if $B$ is maximal linearly independent, then $B \cup \{\ \mathbf{v}\ \}$ is dependent for each $\mathbf{v} \notin B.$ Independence of $B$ forces the coefficient of $\mathbf{v}$ in a nontrivial relation to be nonzero. Solving that relation for $\mathbf{v}$ shows that $\mathbf{v} \in \mathrm{span}(B),$ so $B$ spans $V.$

A vector space is finite-dimensional when it has a finite spanning set. Starting from such a set, one can remove a vector whenever it is a linear combination of the others. The process terminates with a finite basis, so every finite spanning set contains a basis. A vector space without a finite spanning set is infinite-dimensional, and one writes $\dim V = \infty.$

> Assuming the axiom of choice, every vector space has a basis. Zorn's lemma extends any linearly independent subset to a maximal linearly independent subset, which is a basis by the characterization above. No appeal to Zorn's lemma is needed in the finite-dimensional case.

- - -

Any two bases of the same finite-dimensional vector space contain the same number of elements. The argument rests on the observation that when a set of $m$ vectors spans $V$ and a set of $n$ vectors is linearly independent in $V,$ the inequality $n \leq m$ holds. Applying this inequality twice, once in each direction, to any two bases forces their cardinalities to be equal. This common cardinality is called the dimension of $V$ and is denoted $\dim V.$

The inequality follows from the exchange argument. Starting with a spanning list of $m$ vectors, adjoin the first vector from the independent list and remove one of the original spanning vectors that occurs with a nonzero coefficient in its expansion. The resulting list still spans $V.$ At each later step, independence ensures that the next vector is not in the span of the independent vectors already inserted, so its expansion has a nonzero coefficient on one of the remaining original vectors. Each insertion therefore removes a different original vector, and the process cannot continue more than $m$ times. Hence $n \leq m.$

If $W$ is a subspace of a finite-dimensional vector space $V,$ every linearly independent subset of $W$ can be extended to a basis of $W.$ A basis of $W$ can then be extended to a basis of $V.$ Consequently $W$ is finite-dimensional and $\dim W \leq \dim V,$ with equality if and only if $W = V.$

The standard basis of $\mathbb{R}^n$ consists of the $n$ vectors $\mathbf{e}_1, \mathbf{e}_2, \ldots, \mathbf{e}_n,$ where $\mathbf{e}_k$ has a $1$ in position $k$ and $0$ everywhere else. For example, in $\mathbb{R}^3$ the standard basis is:

$$\mathbf{e}_1 = (1, 0, 0), \quad \mathbf{e}_2 = (0, 1, 0), \quad \mathbf{e}_3 = (0, 0, 1)$$

Every [vector](../vectors/) $(a, b, c) \in \mathbb{R}^3$ can be written uniquely as $a \mathbf{e}_1 + b \mathbf{e}_2 + c \mathbf{e}_3,$ confirming that these three vectors form a basis and that $\dim \mathbb{R}^3 = 3.$

An ordered basis $B = (\mathbf{v}_1, \ldots, \mathbf{v}_n)$ records an order on the basis vectors. If $\mathbf{v} = \alpha_1\mathbf{v}_1 + \cdots + \alpha_n\mathbf{v}_n,$ its coordinate vector with respect to $B$ is:

$$[\mathbf{v}]_B = (\alpha_1, \ldots, \alpha_n)$$

The coordinate map $C_B : V \to F^n,$ defined by $C_B(\mathbf{v}) = [\mathbf{v}]_B,$ is a linear isomorphism. This isomorphism depends on the choice and ordering of a basis.

A basis also determines linear maps by their values on its elements. If $B$ is a basis of $V$ and $f : B \to W$ is any function into an $F$-vector space $W,$ exactly one linear map $T : V \to W$ satisfies $T(\mathbf{b}) = f(\mathbf{b})$ for every $\mathbf{b} \in B.$ For a finite expansion $\mathbf{v} = \sum_i \alpha_i\mathbf{b}_i,$ that map must satisfy:

$$T(\mathbf{v}) = \sum_i \alpha_i f(\mathbf{b}_i)$$

Existence follows from this formula, while uniqueness follows because every vector is a finite linear combination of basis vectors.

For vector spaces $V_1, \ldots, V_s$ over $F,$ the external direct sum $V_1 \oplus \cdots \oplus V_s$ is their Cartesian product with componentwise operations. Subspaces $A_1, \ldots, A_s$ of $V$ form an internal direct sum when every $\mathbf{v} \in V$ has a unique expression $\mathbf{v} = \mathbf{a}_1 + \cdots + \mathbf{a}_s$ with $\mathbf{a}_i \in A_i.$ Equivalently, $V = A_1 + \cdots + A_s$ and the relation $\mathbf{a}_1 + \cdots + \mathbf{a}_s = \mathbf{0}$ forces every $\mathbf{a}_i$ to be zero. In this case one writes $V = A_1 \oplus \cdots \oplus A_s.$

For two subspaces, the criterion reduces to $V = A + B$ and $A \cap B = \{\ \mathbf{0}\ \}.$ The subspace $B$ is then called a complement of $A.$ Every subspace of a finite-dimensional vector space has a complement, obtained by extending a basis of the subspace to a basis of the whole space. Complements need not be unique. When $A$ and $B$ are finite-dimensional, direct sums satisfy:

$$\dim(A \oplus B) = \dim A + \dim B$$

## Linear maps

A linear map, or linear transformation, is a [function](../functions/) $\varphi : V \to W$ between two vector spaces over the same field $F$ that preserves the vector space structure. Explicitly, $\varphi$ is linear when for all $\mathbf{u}, \mathbf{v} \in V$ and all $\alpha \in F$ the following two conditions hold:

$$\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})$$

$$\varphi(\alpha \cdot \mathbf{v}) = \alpha \cdot \varphi(\mathbf{v})$$

These two conditions can be combined into the single requirement that $\varphi(\alpha \mathbf{u} + \beta \mathbf{v}) = \alpha\varphi(\mathbf{u}) + \beta\varphi(\mathbf{v})$ for all $\alpha, \beta \in F$ and $\mathbf{u}, \mathbf{v} \in V.$ A linear map that is bijective is called a linear isomorphism, and two vector spaces are isomorphic when a linear isomorphism between them exists. Every $n$-dimensional vector space over $F$ is isomorphic to $F^n,$ so finite-dimensional vector spaces are completely classified by their dimension and their scalar field.

Every linear map satisfies $\varphi(\mathbf{0}) = \mathbf{0}$ and $\varphi(-\mathbf{v}) = -\varphi(\mathbf{v}).$ Compositions of linear maps are linear, and the inverse of a linear isomorphism is linear. A linear map from $V$ to itself is called an endomorphism of $V.$

Several operations on polynomials give linear maps. For a fixed polynomial $q(x) \in F[x],$ multiplication by $q$ defines $M_q : F[x] \to F[x]$ by $M_q(p) = qp.$ Formal differentiation defines $D : F[x] \to F[x]$ by:

$$D\left(\sum_{k=0}^n a_kx^k\right) = \sum_{k=1}^n ka_kx^{k-1}$$

For each $c \in F,$ evaluation at $c$ defines the linear map $E_c : F[x] \to F$ given by $E_c(p) = p(c).$ These examples show that linearity concerns preservation of addition and scalar multiplication, not the particular form of the elements in the vector spaces.

The [kernel](../homomorphisms-and-isomorphisms/) and image of a linear map $\varphi : V \to W$ are defined as follows:

$$\ker(\varphi) = \{\ \mathbf{v} \in V : \varphi(\mathbf{v}) = \mathbf{0} \ \}$$

$$\mathrm{im}(\varphi) = \{\ \varphi(\mathbf{v}) : \mathbf{v} \in V \ \}$$

Both $\ker(\varphi)$ and $\mathrm{im}(\varphi)$ are subspaces of $V$ and $W$ respectively. The dimension theorem, also known as the rank-nullity theorem, states that any linear map with finite-dimensional domain satisfies the following identity:

$$\dim V = \dim \ker(\varphi) + \dim \mathrm{im}(\varphi)$$

To prove the theorem, choose a basis $\mathbf{k}_1, \ldots, \mathbf{k}_r$ of $\ker(\varphi)$ and extend it to a basis $\mathbf{k}_1, \ldots, \mathbf{k}_r, \mathbf{v}_{r+1}, \ldots, \mathbf{v}_n$ of $V.$ The vectors $\varphi(\mathbf{v}_{r+1}), \ldots, \varphi(\mathbf{v}_n)$ span $\mathrm{im}(\varphi),$ since the kernel components of any vector disappear under $\varphi.$ They are also linearly independent. Indeed, if a linear combination of them is zero, the corresponding combination of $\mathbf{v}_{r+1}, \ldots, \mathbf{v}_n$ belongs to the kernel. Uniqueness of coordinates in the chosen basis forces every coefficient to be zero. Hence $\dim \mathrm{im}(\varphi) = n - r,$ which gives the stated identity.

The dimension of $\mathrm{im}(\varphi)$ is called the rank of $\varphi$ and the dimension of $\ker(\varphi)$ is called its nullity. The rank-nullity theorem underlies the theory of [systems of linear equations](../systems-of-linear-equations/), the analysis of [matrices](../matrices/), and the classification of linear maps between finite-dimensional spaces.

Surjective linear maps from finite-dimensional spaces split. If $T : V \to W$ is surjective, choose a basis $\mathbf{w}_1, \ldots, \mathbf{w}_s$ of $W$ and vectors $\mathbf{x}_i \in V$ with $T(\mathbf{x}_i) = \mathbf{w}_i.$ The assignment $\mathbf{w}_i \mapsto \mathbf{x}_i$ extends uniquely to a linear map $S : W \to V$ such that $T \circ S = \mathrm{id}_W.$ Its image is a complement of $\ker(T),$ and therefore:

$$V = \ker(T) \oplus \mathrm{im}(S) \cong \ker(T) \oplus W$$

Applying this construction to a linear map with finite-dimensional domain and codomain restricted to $\mathrm{im}(T)$ gives the noncanonical decomposition $V \cong \ker(T) \oplus \mathrm{im}(T).$ For a subspace $N$ of a finite-dimensional space $V,$ the quotient map yields $V \cong N \oplus V/N$ and $\dim V = \dim N + \dim(V/N).$

## Example

Consider the linear map $\varphi : \mathbb{R}^3 \to \mathbb{R}^2$ defined by:

$$\varphi(x, y, z) = (x + y, y + z)$$

To verify linearity, one checks that:

$$\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})$$

$$\varphi(\alpha \mathbf{v}) = \alpha \varphi(\mathbf{v})$$

hold for all vectors and scalars, which follows immediately from the linearity of addition and scalar multiplication in $\mathbb{R}^3.$ The kernel consists of all vectors $(x, y, z)$ satisfying $x + y = 0$ and $y + z = 0,$ that is, $x = -y$ and $z = -y.$ Every element of $\ker(\varphi)$ therefore has the form:

$$(-y, y, -y) = y(-1, 1, -1)$$

for some $y \in \mathbb{R},$ so the kernel is the one-dimensional subspace spanned by $(-1, 1, -1).$ The image is all of $\mathbb{R}^2,$ since for any $(a, b) \in \mathbb{R}^2$ the vector $(a, 0, b)$ satisfies $\varphi(a, 0, b) = (a, b),$ which shows that $\varphi$ is surjective and thus $\dim \mathrm{im}(\varphi) = 2.$ The rank-nullity theorem is verified:

$$\dim \mathbb{R}^3 = \dim \ker(\varphi) + \dim \mathrm{im}(\varphi) = 1 + 2 = 3$$

The kernel of $\varphi$ is therefore the line through the origin in direction $(-1, 1, -1),$ while $\mathrm{im}(\varphi) = \mathbb{R}^2.$

The surjectivity calculation also gives a right inverse $S : \mathbb{R}^2 \to \mathbb{R}^3$ defined by $S(a, b) = (a, 0, b).$ Indeed, $\varphi(S(a, b)) = (a, b).$ Its image is the plane $M = \{\ (a, 0, b) \mid a, b \in \mathbb{R}\ \},$ which intersects $\ker(\varphi)$ only at the zero vector. Every $(x, y, z) \in \mathbb{R}^3$ has the decomposition:

$$(x, y, z) = (-y, y, -y) + (x + y, 0, y + z)$$

The first summand belongs to $\ker(\varphi)$ and the second to $M,$ so $\mathbb{R}^3 = \ker(\varphi) \oplus M.$

> The notions of subspace, basis, dimension, and linear map all carry over, with minor adjustments, to the broader setting of [modules](../modules/) over a ring, where the absence of multiplicative inverses for scalars introduces phenomena that have no counterpart in linear algebra over a field. The unifying perspective on structure-preserving maps across algebraic structures is collected on the page about [homomorphisms and isomorphisms](../homomorphisms-and-isomorphisms/).
