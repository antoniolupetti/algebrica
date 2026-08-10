---
title: Linear Maps
source: https://algebrica.org/linear-maps/
license: CC BY-NC 4.0
tags:
  - basis
  - composition
  - endomorphism
  - image
  - isomorphism
  - kernel
  - linear-algebra
  - linear-map
  - matrices
  - matrix-representation
  - rank-nullity-theorem
  - vector-space
---
## Definition

Let $V$ and $W$ be [vector spaces](../vector-spaces/) over the same [field](../fields/) $F.$ A [function](../functions/) $T : V \to W$ is linear if, for all $\mathbf{u}, \mathbf{v} \in V$ and every $\alpha \in F$, it satisfies two conditions:

$$T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$$

$$T(\alpha\mathbf{v}) = \alpha T(\mathbf{v})$$

The first condition is additivity, the second is homogeneity. The sum $\mathbf{u} + \mathbf{v}$ and the product $\alpha\mathbf{v}$ are computed in $V,$ while the operations on the right-hand sides are computed in $W.$ When the field has to be emphasised, $T$ is called $F$-linear. The terms linear map, linear mapping and linear transformation are synonyms. The two conditions are equivalent to a single identity. Additivity and homogeneity imply:

$$T(\alpha\mathbf{u} + \beta\mathbf{v}) = \alpha T(\mathbf{u}) + \beta T(\mathbf{v})$$

Conversely, the choices $\alpha = \beta = 1$ and $\beta = 0$ give additivity and homogeneity, respectively. Induction on the number of terms gives the corresponding identity for every finite [linear combination](../linear-combinations/):

$$T\left(\sum_{i=1}^{n} \alpha_i\mathbf{v}_i\right) = \sum_{i=1}^{n} \alpha_i T(\mathbf{v}_i)$$

The image of a linear combination is the linear combination of the images with the same coefficients.

Homogeneity has two consequences. Taking $\alpha = 0$ gives $T(\mathbf{0}_V) = \mathbf{0}_W,$ and taking $\alpha = -1$ gives $T(-\mathbf{v}) = -T(\mathbf{v}).$ Thus a map that does not fix the origin is not linear.

An endomorphism of $V$ is a linear map $T : V \to V,$ also called a linear operator. A linear functional, or linear form, has codomain $F,$ regarded as a one-dimensional vector space over itself. A bijective linear map is an [isomorphism](../homomorphisms-and-isomorphisms/), and an isomorphism from $V$ to itself is an automorphism. [Injectivity, surjectivity and bijectivity](../injective-surjective-and-bijective-functions/) are the conditions defined for functions, applied here to the map between the underlying sets.

> Additivity alone makes $T$ a homomorphism of the underlying additive [groups](../groups/). Homogeneity requires compatibility with multiplication by scalars. Together, the same conditions define a homomorphism of [modules](../modules/) over a ring.

- - - 

For example, the zero map $\mathbf{v} \mapsto \mathbf{0}$ and the identity map $\mathrm{id}_V$ are linear. For a fixed $\lambda \in F,$ the map $T(\mathbf{v}) = \lambda\mathbf{v}$ is the homothety of ratio $\lambda$ and is linear. If $U$ is a [subspace](../subspaces/) of $V,$ both the inclusion $U \to V$ and the quotient map $V \to V/U$ are linear.

Every [matrix](../matrices/) defines a linear map. For $A \in M_{m \times n}(F),$ the map $L_A : F^n \to F^m$ is defined on column vectors by:

$$L_A(\mathbf{x}) = A\mathbf{x}$$

Distributivity of the matrix product gives $A(\mathbf{x} + \mathbf{y}) = A\mathbf{x} + A\mathbf{y},$ and compatibility with scalars gives $A(\alpha\mathbf{x}) = \alpha(A\mathbf{x}),$ so $L_A$ is linear. Every linear map between spaces of column vectors has this form, as proved below.

In the plane, the rotations about the origin, the orthogonal projections onto a line through the origin and the reflections in such a line are linear. The reflection across the line through the origin at angle $\theta$ to the $x$-axis has matrix:

$$A = \begin{pmatrix} \cos 2\theta & \sin 2\theta \\[6pt] \sin 2\theta & -\cos 2\theta \end{pmatrix}$$

Each of these maps fixes the origin and carries the parallelogram built on $\mathbf{u}$ and $\mathbf{v}$ to the parallelogram built on $T(\mathbf{u})$ and $T(\mathbf{v}),$ which is additivity stated geometrically.

- - -

Transposition is a linear map $M_{m \times n}(F) \to M_{n \times m}(F),$ since $(A + B)^{\mathrm{T}} = A^{\mathrm{T}} + B^{\mathrm{T}}$ and $(\alpha A)^{\mathrm{T}} = \alpha A^{\mathrm{T}}.$ On the space $P_n(\mathbb{R})$ of real [polynomials](../polynomials/) of degree at most $n,$ with $n \geq 1,$ differentiation $p \mapsto p'$ is linear with values in $P_{n-1}(\mathbb{R}).$

Evaluation at a fixed point $c \in F$ defines the linear functional $\mathrm{ev}_c(p) = p(c)$ on $F[x],$ because the value of a sum of polynomials is the sum of the values. On the space $C([a, b])$ of real [continuous functions](../continuous-functions/), the [definite integral](../definite-integrals/) defines the linear functional:

$$I(f) = \int_a^b f(x) \ dx$$

Linearity here is the additivity of the integral together with the rule for constant factors.

## Maps that are not linear

Translation by a fixed nonzero vector $\mathbf{b},$ defined by $\tau(\mathbf{v}) = \mathbf{v} + \mathbf{b},$ sends $\mathbf{0}$ to $\mathbf{b}$ and is therefore not linear. The sum of a linear map and a constant vector is the affine map $\mathbf{v} \mapsto T(\mathbf{v}) + \mathbf{b},$ which is linear exactly when $\mathbf{b} = \mathbf{0}.$ The real function $f(x) = mx + q$ is a linear map $\mathbb{R} \to \mathbb{R}$ only for $q = 0,$ although its graph is a [line](../lines/) for every value of $q.$

Neither additivity nor homogeneity implies the other. Define $H : \mathbb{R}^2 \to \mathbb{R}$ by:

$$
H(x, y) =
\begin{cases}
\dfrac{x^3}{x^2 + y^2} & \text{if } (x, y) \neq (0, 0) \\[6pt]
0 & \text{if } (x, y) = (0, 0)
\end{cases}
$$

For every real $\alpha,$ this function satisfies $H(\alpha x, \alpha y) = \alpha H(x, y),$ so it is homogeneous. It is not additive because $H(1, 0) = 1,$ $H(0, 1) = 0$ and $H(1, 1) = 1/2.$

Other functions fail both conditions. The absolute value satisfies $|\alpha x| = |\alpha||x|,$ so it is not homogeneous for negative $\alpha,$ and additivity fails since $|1 + (-1)| = 0$ while $|1| + |-1| = 2.$ The [determinant](../determinant/) $\det : M_2(\mathbb{R}) \to \mathbb{R}$ satisfies $\det(\alpha A) = \alpha^2\det(A),$ so it is not homogeneous. The values $\det(I_2 + I_2) = 4$ and $\det(I_2) + \det(I_2) = 2$ show that it is not additive.

Linearity depends on the field of scalars. Complex conjugation $z \mapsto \overline{z}$ is additive and satisfies $\overline{\alpha z} = \alpha\overline{z}$ for real $\alpha,$ so it is $\mathbb{R}$-linear on $\mathbb{C}$ viewed as a real vector space of dimension $2.$ It is not $\mathbb{C}$-linear, because $\overline{i \cdot 1} = -i$ while $i\overline{1} = i.$

> Conversely, additivity implies $T(q\mathbf{v}) = qT(\mathbf{v})$ for every rational $q,$ so over $\mathbb{Q}$ the second condition follows from the first. Over $\mathbb{R}$ the implication fails. Counterexamples can be defined by choosing a basis of $\mathbb{R}$ as a vector space over $\mathbb{Q}.$ This construction uses the axiom of choice, and the resulting functions are discontinuous at every point.

## Determination on a basis

The values of a linear map on a basis determine the map, and any values in the codomain may be assigned to the basis vectors. If $B$ is a basis of $V$ and $f : B \to W$ is any function, a unique linear map $T : V \to W$ satisfies $T(\mathbf{b}) = f(\mathbf{b})$ for every $\mathbf{b} \in B.$

For uniqueness, each $\mathbf{v} \in V$ has a unique expansion:

$$\mathbf{v} = \alpha_1\mathbf{v}_1 + \cdots + \alpha_r\mathbf{v}_r$$

with $\mathbf{v}_1, \ldots, \mathbf{v}_r$ distinct elements of $B.$ A linear extension of $f$ must satisfy:

$$T(\mathbf{v}) = \alpha_1f(\mathbf{v}_1) + \cdots + \alpha_rf(\mathbf{v}_r)$$

Thus the prescribed values determine $T(\mathbf{v}),$ and any two linear extensions of $f$ are equal.

For existence, define $T$ by the displayed formula. Uniqueness of the coordinates makes the assignment well defined. Given $\mathbf{u}$ and $\mathbf{v},$ expand both over a common finite subset of $B,$ allowing zero coefficients. The coordinates of $\mathbf{u} + \mathbf{v}$ are the sums of the corresponding coordinates and the coordinates of $\alpha\mathbf{v}$ are $\alpha$ times those of $\mathbf{v},$ so the formula gives $T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$ and $T(\alpha\mathbf{v}) = \alpha T(\mathbf{v}).$ The restriction of $T$ to $B$ is $f$ by construction.

Two linear maps that agree on a basis are equal, since their difference is zero on every linear combination of basis vectors. Thus a linear map from an $n$-dimensional space is determined by $n$ vectors of $W,$ and these vectors are arbitrary. For example, the prescription $T(\mathbf{e}_1) = (1, 0, -1)$ and $T(\mathbf{e}_2) = (2, 1, 0)$ determines the linear map $T : \mathbb{R}^2 \to \mathbb{R}^3$ given by:

$$T(x, y) = x(1, 0, -1) + y(2, 1, 0) = (x + 2y, y, -x)$$

Both properties of a basis are needed. The vectors $\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_1 + \mathbf{e}_2$ span $\mathbb{R}^2$ but are dependent, and the prescription $f(\mathbf{e}_1) = f(\mathbf{e}_2) = 0$ with $f(\mathbf{e}_1 + \mathbf{e}_2) = 1$ has no linear extension, since linearity requires the third value to be $0.$ Linear independence permits arbitrary values on $B,$ while the spanning property ensures that $T$ has a value on every vector of $V.$

## Kernel and image

The kernel and the image of a linear map $T : V \to W$ are:

$$\ker(T) = \{\ \mathbf{v} \in V \mid T(\mathbf{v}) = \mathbf{0}\ \}$$

$$\mathrm{im}(T) = \{\ T(\mathbf{v}) \mid \mathbf{v} \in V\ \}$$

The kernel is a subspace of $V.$ If $\mathbf{u}, \mathbf{v} \in \ker(T),$ then $T(\alpha\mathbf{u} + \beta\mathbf{v}) = \mathbf{0},$ so $\alpha\mathbf{u} + \beta\mathbf{v} \in \ker(T).$ The image is a subspace of $W.$ If $\mathbf{w}_1 = T(\mathbf{u})$ and $\mathbf{w}_2 = T(\mathbf{v})$ are in the image, then $\alpha\mathbf{w}_1 + \beta\mathbf{w}_2 = T(\alpha\mathbf{u} + \beta\mathbf{v}),$ which is also in the image.

The kernel also gives a criterion for injectivity. If $T$ is injective, then $T(\mathbf{v}) = \mathbf{0} = T(\mathbf{0})$ implies $\mathbf{v} = \mathbf{0},$ so the kernel is trivial. Conversely, if $\ker(T) = \{\ \mathbf{0}\ \}$ and $T(\mathbf{u}) = T(\mathbf{v}),$ then $T(\mathbf{u} - \mathbf{v}) = \mathbf{0}$ implies $\mathbf{u} = \mathbf{v}.$ Hence $T$ is injective precisely when $\ker(T) = \{\ \mathbf{0}\ \}.$

If $B$ spans $V,$ then $T(B)$ spans $\mathrm{im}(T),$ because every vector of $V$ is a linear combination of elements of $B$ and $T$ preserves such combinations. The dimension of the image is the rank of $T,$ and the dimension of the kernel is its nullity. The rank satisfies $\mathrm{rank}(T) \leq \min\{\dim V, \dim W\}.$ The rank-nullity theorem gives:

$$\dim V = \dim \ker(T) + \dim \mathrm{im}(T)$$

To prove the theorem, extend a basis of the kernel to a basis of $V.$ The images of the added vectors are then a basis of $\mathrm{im}(T).$ The page on the [kernel and image of a linear map](../kernel-and-image-of-a-linear-map/) gives the full proof, the description of the preimages of a vector and the translation of both subspaces into matrix terms.

## Composition and isomorphisms

Let $T : V \to W$ and $S : W \to U$ be linear maps. Their [composite](../composite-functions/) $S \circ T : V \to U$ is linear:

$$
\begin{align}
(S \circ T)(\alpha\mathbf{u} + \beta\mathbf{v}) &= S(\alpha T(\mathbf{u}) + \beta T(\mathbf{v})) \\[6pt]
  &= \alpha S(T(\mathbf{u})) + \beta S(T(\mathbf{v})) \\[6pt]
  &= \alpha(S \circ T)(\mathbf{u}) + \beta(S \circ T)(\mathbf{v})
\end{align}
$$

Composition of functions is associative, and the identity maps are neutral elements, since $T \circ \mathrm{id}_V = T$ and $\mathrm{id}_W \circ T = T.$ It is distributive over addition and compatible with scalar multiplication, as expressed by $S \circ (T_1 + T_2) = S \circ T_1 + S \circ T_2,$ $(S_1 + S_2) \circ T = S_1 \circ T + S_2 \circ T$ and $\alpha(S \circ T) = (\alpha S) \circ T = S \circ (\alpha T).$

Suppose that the linear map $T : V \to W$ is bijective. For $\mathbf{w}_1, \mathbf{w}_2 \in W,$ set $\mathbf{v}_i = T^{-1}(\mathbf{w}_i).$ Since $T(\alpha\mathbf{v}_1 + \beta\mathbf{v}_2) = \alpha\mathbf{w}_1 + \beta\mathbf{w}_2,$ its [inverse](../inverse-function/) satisfies:

$$T^{-1}(\alpha\mathbf{w}_1 + \beta\mathbf{w}_2) = \alpha T^{-1}(\mathbf{w}_1) + \beta T^{-1}(\mathbf{w}_2)$$

This identity proves that $T^{-1}$ is linear. Two vector spaces are isomorphic, written $V \cong W,$ if a linear bijection exists between them. Isomorphism is reflexive because each identity map is an isomorphism, transitive because a composite of isomorphisms is an isomorphism, and symmetric because the inverse of an isomorphism is an isomorphism.

For finite-dimensional spaces over $F,$ the condition $V \cong W$ is equivalent to $\dim V = \dim W.$ A linear bijection sends a basis of $V$ to a basis of $W,$ so isomorphic spaces have equal dimensions. Conversely, when the dimensions are equal, choose bases $(\mathbf{v}_1, \ldots, \mathbf{v}_n)$ of $V$ and $(\mathbf{w}_1, \ldots, \mathbf{w}_n)$ of $W.$ The linear map defined by $T(\mathbf{v}_j) = \mathbf{w}_j$ is bijective because it sends one basis to the other. In particular, an ordered basis of an $n$-dimensional space $V$ defines a coordinate isomorphism $V \cong F^n.$

For a linear map between finite-dimensional spaces of equal dimension, the rank-nullity theorem makes injectivity equivalent to surjectivity. Either condition is therefore sufficient for the map to be an isomorphism. This equivalence can fail for infinite-dimensional spaces. On the space of real [sequences](../sequences/), the left shift and the right shift are:

$$L(a_1, a_2, a_3, \ldots) = (a_2, a_3, \ldots)$$

$$R(a_1, a_2, a_3, \ldots) = (0, a_1, a_2, \ldots)$$

Both are linear endomorphisms of the same space. The left shift $L$ is surjective with kernel spanned by $(1, 0, 0, \ldots),$ while the right shift $R$ is injective and its image consists of the sequences whose first entry is zero. They satisfy $L \circ R = \mathrm{id}$ and $R \circ L \neq \mathrm{id},$ so a one-sided inverse need not be an inverse.

## The space of linear maps

Linear maps $V \to W$ are added and scaled pointwise:

$$(S + T)(\mathbf{v}) = S(\mathbf{v}) + T(\mathbf{v})$$

$$(\alpha T)(\mathbf{v}) = \alpha T(\mathbf{v})$$

Both operations preserve linearity. For the sum, $(S + T)(\alpha\mathbf{u} + \beta\mathbf{v})$ is equal to $\alpha S(\mathbf{u}) + \beta S(\mathbf{v}) + \alpha T(\mathbf{u}) + \beta T(\mathbf{v}),$ which is $\alpha(S + T)(\mathbf{u}) + \beta(S + T)(\mathbf{v}).$ For scalar multiplication, $(\alpha T)(\beta\mathbf{u} + \gamma\mathbf{v}) = \beta(\alpha T)(\mathbf{u}) + \gamma(\alpha T)(\mathbf{v}).$ With these pointwise operations, the linear maps from $V$ to $W$ form a vector space over $F,$ denoted by:

$$\mathrm{Hom}_F(V, W)$$

Its zero element is the zero map, and the additive inverse of $T$ is the map $\mathbf{v} \mapsto -T(\mathbf{v}).$

Composition is a multiplication on $\mathrm{End}_F(V) = \mathrm{Hom}_F(V, V).$ With addition and composition, this space is an associative [ring](../rings/) with identity $\mathrm{id}_V.$ It is also an algebra over $F$ because composition is compatible with scalar multiplication. This multiplication is noncommutative when $\dim V \geq 2.$ On $F^2,$ consider the endomorphisms $P(x, y) = (x, 0)$ and $Q(x, y) = (y, 0).$ Their composites are:

$$(P \circ Q)(x, y) = (y, 0)$$

$$(Q \circ P)(x, y) = (0, 0)$$

The second composite is the zero map while neither factor is zero, so $\mathrm{End}_F(V)$ has zero divisors and its nonzero elements need not be invertible.

- - -

Suppose that $\dim V = n$ and $\dim W = m,$ with bases $\mathbf{v}_1, \ldots, \mathbf{v}_n$ of $V$ and $\mathbf{w}_1, \ldots, \mathbf{w}_m$ of $W.$ For $i \leq m$ and $j \leq n,$ define $T_{ij} : V \to W$ by its values on the basis of $V$:

$$T_{ij}(\mathbf{v}_k) = \delta_{jk}\mathbf{w}_i$$

where $\delta_{jk}$ is the Kronecker delta. These $mn$ maps form a basis of $\mathrm{Hom}_F(V, W).$ Given $T,$ let $a_{ij}$ be the coordinates of $T(\mathbf{v}_j)$ in the basis of $W,$ so that $T(\mathbf{v}_j) = \sum_i a_{ij}\mathbf{w}_i.$ The maps $T$ and $\sum_{i, j} a_{ij}T_{ij}$ have the same values on every $\mathbf{v}_k,$ so they are equal and the family spans. If $\sum_{i, j} c_{ij}T_{ij}$ is the zero map, its value at $\mathbf{v}_k$ is $\sum_i c_{ik}\mathbf{w}_i = \mathbf{0}.$ Independence of the $\mathbf{w}_i$ then implies $c_{ik} = 0$ for every $i$ and $k.$ Hence:

$$\dim \mathrm{Hom}_F(V, W) = \dim V \cdot \dim W$$

The dual space $V^* = \mathrm{Hom}_F(V, F)$ is the case $W = F,$ so a finite-dimensional space and its dual have the same dimension.

## The matrix of a linear map

The scalars $a_{ij}$ of the previous section are the entries of a matrix. Fix ordered bases $\mathcal{B} = (\mathbf{v}_1, \ldots, \mathbf{v}_n)$ of $V$ and $\mathcal{C} = (\mathbf{w}_1, \ldots, \mathbf{w}_m)$ of $W.$ The matrix of $T$ relative to these bases is the $m \times n$ matrix $A$ whose $j$-th column is the coordinate column of $T(\mathbf{v}_j)$ in $\mathcal{C}.$ If $[\mathbf{v}]_{\mathcal{B}}$ denotes the coordinate column of $\mathbf{v},$ then:

$$[T(\mathbf{v})]_{\mathcal{C}} = A[\mathbf{v}]_{\mathcal{B}}$$

To verify this identity, it is enough to take $\mathbf{v} = \mathbf{v}_j.$ In that case $[\mathbf{v}_j]_{\mathcal{B}}$ is the $j$-th standard column, so the product with $A$ is the $j$-th column of $A.$ Conversely, each $m \times n$ matrix defines a unique linear map by this formula. The assignment $T \mapsto A$ is therefore a bijection, and it preserves sums and scalar multiples. Hence it is an isomorphism $\mathrm{Hom}_F(V, W) \cong M_{m \times n}(F).$

For $V = F^n$ and $W = F^m$ with the standard bases, the formula becomes $T(\mathbf{v}) = A\mathbf{v}.$ The $j$-th column of $A$ is $T(\mathbf{e}_j),$ so every linear map between these spaces is multiplication by a unique matrix.

Let $T : V \to W$ have matrix $A$ with respect to $\mathcal{B}$ and $\mathcal{C},$ and let $S : W \to U$ have matrix $B$ with respect to $\mathcal{C}$ and a basis $\mathcal{D}.$ Applying the coordinate formula first to $T$ and then to $S$ gives:

$$[(S \circ T)(\mathbf{v})]_{\mathcal{D}} = B(A[\mathbf{v}]_{\mathcal{B}}) = (BA)[\mathbf{v}]_{\mathcal{B}}$$

Thus the matrix of $S \circ T$ is $BA.$ The map $T$ is an isomorphism precisely when $A$ is [invertible](../inverse-matrix/), and in this case the matrix of $T^{-1}$ is $A^{-1}.$

The rank of $T$ is the [rank of the matrix](../rank-of-a-matrix/), and the kernel of $T$ corresponds to the solutions of the [homogeneous system](../systems-of-linear-equations/) $A\mathbf{x} = \mathbf{0}.$ The matrix depends on the two ordered bases. A [change of bases](../change-of-basis-matrix/) replaces $A$ by $Q^{-1}AP,$ where $P$ and $Q$ are invertible. If an endomorphism has the same basis in its domain and codomain, a change of basis has the form $C^{-1}AC.$ Matrices related by this formula are similar. If the endomorphism has a basis of [eigenvectors](../eigenvalues-and-eigenvectors/), then $C$ can be chosen so that $C^{-1}AC$ is diagonal and $A$ is [diagonalizable](../matrix-diagonalization/).

## A worked example

Let $P_2(\mathbb{R})$ be the space of real polynomials of degree at most $2.$ The two coordinates of $T : P_2(\mathbb{R}) \to \mathbb{R}^2$ are the value and derivative of a polynomial at $1$:

$$T(p) = (p(1), p'(1))$$

Both components are linear in $p,$ since $(p + q)(1) = p(1) + q(1)$ and $(p + q)' = p' + q',$ with the analogous identities for scalar multiples. Hence $T$ is linear.

The monomials $1, x, x^2$ form a basis of $P_2(\mathbb{R}).$ Their images are $T(1) = (1, 0),$ $T(x) = (1, 1)$ and $T(x^2) = (1, 2),$ so the matrix of $T$ with respect to this basis and the standard basis of $\mathbb{R}^2$ is:

$$A = \begin{pmatrix} 1 & 1 & 1 \\[6pt] 0 & 1 & 2 \end{pmatrix}$$

These three values determine $T.$ For $p = a + bx + cx^2,$ linearity gives:

$$T(p) = (a + b + c, b + 2c)$$

A polynomial lies in the kernel when $a + b + c = 0$ and $b + 2c = 0.$ The second equation gives $b = -2c,$ and substitution in the first gives $a = c.$ The kernel is therefore:

$$\ker(T) = \mathrm{span}\{\ (x - 1)^2\ \}$$

Its elements are the polynomials of $P_2(\mathbb{R})$ that have $1$ as a root of multiplicity at least $2.$ This is equivalent to the two conditions $p(1) = 0$ and $p'(1) = 0.$

The map is surjective. For $(s, t) \in \mathbb{R}^2,$ the polynomial $p(x) = s + t(x - 1)$ satisfies $p(1) = s$ and $p'(1) = t.$ Thus the rank is $2,$ the nullity is $1,$ and:

$$3 = \dim \ker(T) + \dim \mathrm{im}(T) = 1 + 2$$

Since $\dim P_2(\mathbb{R}) = 3$ exceeds $\dim \mathbb{R}^2 = 2,$ no linear map from $P_2(\mathbb{R})$ to $\mathbb{R}^2$ can be injective. On the subspace $P_1(\mathbb{R})$ of polynomials of degree at most $1,$ the restriction $T|_{P_1(\mathbb{R})} : P_1(\mathbb{R}) \to \mathbb{R}^2$ is an isomorphism. Its inverse sends $(s, t)$ to $s + t(x - 1),$ the [first-order Taylor polynomial](../taylor-formula-with-remainder/) at $1$ with value $s$ and derivative $t.$
