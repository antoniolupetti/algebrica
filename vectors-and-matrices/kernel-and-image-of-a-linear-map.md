---
title: Kernel and Image of a Linear Map
source: https://algebrica.org/kernel-and-image-of-a-linear-map/
license: CC BY-NC 4.0
tags:
  - basis
  - image
  - isomorphism
  - kernel
  - linear-algebra
  - linear-map
  - linear-systems
  - matrices
  - rank-nullity-theorem
  - subspace
  - vector-space
---
## Definition

Suppose that $V$ and $W$ are vector spaces over a field $F,$ and fix a [linear map](../linear-maps/) $T : V \to W.$ The kernel of $T$ is the set of vectors mapped to the zero vector of $W:$

$$\ker(T) = \{\ \mathbf{v} \in V \mid T(\mathbf{v}) = \mathbf{0}_W\ \}$$

The image of $T$ is the set of its values:

$$\mathrm{im}(T) = \{\ T(\mathbf{v}) \mid \mathbf{v} \in V\ \}$$

Since $T(\mathbf{0}_V) = \mathbf{0}_W,$ the kernel contains $\mathbf{0}_V$ and the image contains $\mathbf{0}_W.$ The kernel is the preimage of $\{\ \mathbf{0}_W\ \},$ while the image is $T(V).$ The terms null space and range are also used for the kernel and the image, respectively.

- - -

The kernel is a [subspace](../subspaces/) of $V,$ and the image is a subspace of $W.$ To verify the first statement, take $\mathbf{u}, \mathbf{v} \in \ker(T)$ and $\alpha, \beta \in F.$ By linearity:

$$T(\alpha\mathbf{u} + \beta\mathbf{v}) = \alpha T(\mathbf{u}) + \beta T(\mathbf{v}) = \alpha\mathbf{0}_W + \beta\mathbf{0}_W = \mathbf{0}_W$$

Hence $\alpha\mathbf{u} + \beta\mathbf{v}$ is in $\ker(T).$ If $\mathbf{w}_1 = T(\mathbf{u})$ and $\mathbf{w}_2 = T(\mathbf{v})$ are in the image, then:

$$\alpha\mathbf{w}_1 + \beta\mathbf{w}_2 = T(\alpha\mathbf{u} + \beta\mathbf{v})$$

Thus $\alpha\mathbf{w}_1 + \beta\mathbf{w}_2$ is also in the image.

More generally, the image $T(U)$ of every subspace $U$ of $V$ is a subspace of $W,$ and the preimage $T^{-1}(Z)$ of every subspace $Z$ of $W$ is a subspace of $V.$ These statements follow from the same calculation. The choices $U = V$ and $Z = \{\ \mathbf{0}_W\ \}$ give the image and the kernel.

> The kernel is a subspace of the domain, whereas the image is a subspace of the codomain. When $V = W,$ they can coincide. For example, the endomorphism $N : F^2 \to F^2$ defined by $N(x, y) = (y, 0)$ has $\ker(N) = \mathrm{im}(N) = \mathrm{span}\{\ \mathbf{e}_1\ \}.$ Hence $\ker(N) + \mathrm{im}(N)$ is not a direct sum and is not equal to $F^2.$

## Injectivity and the fibres

A linear map is injective if and only if its kernel is $\{\ \mathbf{0}_V\ \}.$ If $T$ is injective and $\mathbf{v} \in \ker(T),$ then $T(\mathbf{v}) = T(\mathbf{0}_V),$ so $\mathbf{v} = \mathbf{0}_V.$ Conversely, suppose that the kernel is $\{\ \mathbf{0}_V\ \}$ and $T(\mathbf{u}) = T(\mathbf{v}).$ Linearity gives $T(\mathbf{u} - \mathbf{v}) = \mathbf{0}_W.$ Therefore $\mathbf{u} - \mathbf{v} = \mathbf{0}_V,$ and $T$ is injective.

The kernel also determines every nonempty fibre. Fix $\mathbf{w} \in \mathrm{im}(T)$ and choose $\mathbf{v}_0$ such that $T(\mathbf{v}_0) = \mathbf{w}.$ The equality $T(\mathbf{v}) = \mathbf{w}$ holds if and only if $T(\mathbf{v} - \mathbf{v}_0) = \mathbf{0}_W,$ which is equivalent to $\mathbf{v} - \mathbf{v}_0 \in \ker(T).$ Hence:

$$T^{-1}(\{\ \mathbf{w}\ \}) = \mathbf{v}_0 + \ker(T)$$

Every vector in the fibre can be used as $\mathbf{v}_0,$ and the resulting affine subspace is the same. If the kernel is trivial, each nonempty fibre has one element. For the map $\mathbf{x} \mapsto A\mathbf{x},$ this formula states that the solutions of a [linear system](../systems-of-linear-equations/) are one particular solution plus the solutions of the associated homogeneous system.

## Surjectivity and a spanning set for the image

If $S$ spans $V,$ then $T(S)$ spans $\mathrm{im}(T).$ Indeed, every $\mathbf{v} \in V$ is a finite [linear combination](../linear-combinations/) of elements of $S,$ and linearity expresses $T(\mathbf{v})$ as the corresponding combination of their images. If $V$ has a finite basis $\mathbf{v}_1, \ldots, \mathbf{v}_n,$ then:

$$\mathrm{im}(T) = \mathrm{span}\{\ T(\mathbf{v}_1), \ldots, T(\mathbf{v}_n)\ \}$$

These vectors need not be linearly independent. The map $T$ is surjective if and only if $\mathrm{im}(T) = W.$

The rank of $T$ is $\dim \mathrm{im}(T),$ and its nullity is $\dim \ker(T).$ When $V$ and $W$ are finite-dimensional, the inclusions and the spanning set above give $\mathrm{rank}(T) \leq \min(\dim V, \dim W).$

## The rank-nullity theorem

Let $V$ be finite-dimensional, and let $T : V \to W$ be linear. Then:

$$\dim V = \dim \ker(T) + \dim \mathrm{im}(T)$$

Set $K = \ker(T).$ In the [quotient space](../vector-spaces/) $V/K,$ the formula:

$$\overline{T}(\mathbf{v} + K) = T(\mathbf{v})$$

defines a map $\overline{T} : V/K \to \mathrm{im}(T).$ If $\mathbf{u} + K = \mathbf{v} + K,$ then $\mathbf{u} - \mathbf{v} \in K,$ so $T(\mathbf{u}) = T(\mathbf{v}).$ Thus the value of $\overline{T}$ does not depend on the representative of the coset. The map is linear and surjective. Its kernel consists only of $K,$ the zero vector of $V/K,$ so it is also injective. Therefore:

$$V/\ker(T) \cong \mathrm{im}(T)$$

It remains to calculate the dimension of the quotient. Let $\mathbf{k}_1, \ldots, \mathbf{k}_r$ be a basis of $K,$ and extend it to a basis of $V:$

$$\mathbf{k}_1, \ldots, \mathbf{k}_r, \mathbf{u}_1, \ldots, \mathbf{u}_s$$

The cosets $\mathbf{u}_1 + K, \ldots, \mathbf{u}_s + K$ form a basis of $V/K.$ They span because the terms involving the $\mathbf{k}_i$ vanish in the quotient. They are linearly independent because:

$$\sum_{j=1}^{s}\gamma_j(\mathbf{u}_j + K) = K$$

implies $\sum_{j=1}^{s}\gamma_j\mathbf{u}_j \in K,$ and the linear independence of the displayed basis of $V$ gives $\gamma_1 = \cdots = \gamma_s = 0.$ Consequently $\dim(V/K) = s,$ while $\dim V = r + s.$ Since $V/K$ and $\mathrm{im}(T)$ are isomorphic, $\dim \mathrm{im}(T) = s,$ and the theorem follows.

> The theorem requires only that $V$ be finite-dimensional. No finite-dimensional hypothesis on $W$ is needed. For infinite-dimensional spaces the corresponding equality of cardinal dimensions gives less information. Differentiation on $\mathbb{R}[x]$ is surjective and has the constant [polynomials](../polynomials/) as its kernel. In this case $\dim \mathbb{R}[x] = 1 + \dim \mathbb{R}[x].$

As an application, consider the trace map $\mathrm{tr} : M_n(F) \to F.$ It is linear and surjective because the matrix whose upper left entry is $1$ and whose other entries are $0$ has trace $1.$ Its image has dimension $1,$ and $M_n(F)$ has dimension $n^2.$ The kernel, which is the subspace of matrices with trace $0,$ therefore has dimension $n^2 - 1.$

## Consequences

Suppose that $V$ and $W$ are finite-dimensional. The rank-nullity theorem gives the following conclusions:

+ The rank satisfies $\dim \mathrm{im}(T) \leq \min(\dim V, \dim W).$
+ $\dim V > \dim W$ forces a nonzero kernel, so no linear map $F^5 \to F^3$ is injective.
+ $\dim V < \dim W$ forces a proper image, so no linear map $F^3 \to F^5$ is surjective.

If $\dim V = \dim W,$ then injectivity, surjectivity and bijectivity are equivalent. If $T$ is injective, its kernel has dimension $0,$ so its image has dimension $\dim V = \dim W$ and must equal $W.$ If $T$ is surjective, its image has dimension $\dim W = \dim V,$ so its kernel has dimension $0.$ Hence an injective endomorphism of a finite-dimensional space is [invertible](../inverse-function/). This equivalence fails in infinite dimension. Differentiation on $\mathbb{R}[x]$ is surjective but not injective, while multiplication by $x$ is injective but not surjective.

The domain also has a decomposition based on the kernel. Choose a complement $M$ such that $V = \ker(T) \oplus M.$ The restriction $T|_M : M \to \mathrm{im}(T)$ is an [isomorphism](../homomorphisms-and-isomorphisms/). Its kernel is $M \cap \ker(T) = \{\ \mathbf{0}\ \},$ so it is injective. Every $\mathbf{v} \in V$ has a decomposition $\mathbf{v} = \mathbf{k} + \mathbf{m}$ with $\mathbf{k} \in \ker(T)$ and $\mathbf{m} \in M,$ and $T(\mathbf{v}) = T(\mathbf{m}).$ Thus the restriction is surjective as well.

The complement $M$ is not unique. The quotient $V/\ker(T)$ is defined without choosing one, and the isomorphism used in the proof of the theorem identifies it with the image.

## Kernel and image of a matrix

Let $A \in M_{m \times n}(F),$ and let $L_A : F^n \to F^m$ be the map $L_A(\mathbf{x}) = A\mathbf{x}.$ Denote the columns of $A$ by $\mathbf{a}_1, \ldots, \mathbf{a}_n.$ For $\mathbf{x} = (x_1, \ldots, x_n),$ [matrix multiplication](../matrices/) gives:

$$A\mathbf{x} = x_1\mathbf{a}_1 + \cdots + x_n\mathbf{a}_n$$

It follows that $\mathrm{im}(L_A)$ is the column space of $A.$ Its dimension is the [rank](../rank-of-a-matrix/) $r(A),$ which is also the dimension of the row space. The kernel of $L_A$ is the null space of $A,$ namely the solution space of $A\mathbf{x} = \mathbf{0}.$ Thus:

$$n = \dim \ker(L_A) + r(A)$$

[Gaussian elimination](../gaussian-elimination/) gives both dimensions. The number of pivot columns is $r(A),$ and the number of free variables is $n - r(A).$ Solving the homogeneous system with one free variable equal to $1$ and the others equal to $0$ gives a basis of the kernel.

The system $A\mathbf{x} = \mathbf{b}$ has a solution if and only if $\mathbf{b}$ is in the column space. By the [Rouché-Capelli theorem](../rouche-capelli-theorem/), this condition is equivalent to $r(A) = r(A|\mathbf{b}).$ When a solution exists, the solution set is a translate of the null space and has $n - r(A)$ free parameters.

## A worked example

Consider the linear map $L_A : \mathbb{R}^4 \to \mathbb{R}^3$ associated with:

$$
A = \begin{pmatrix}
1 & 2 & 0 & 1 \\[6pt]
2 & 4 & 1 & 3 \\[6pt]
1 & 2 & 1 & 2
\end{pmatrix}
$$

Subtract twice the first row from the second and subtract the first row from the third. The last two rows are then equal, so subtracting one from the other gives the row echelon form:

$$
\begin{pmatrix}
1 & 2 & 0 & 1 \\[6pt]
0 & 0 & 1 & 1 \\[6pt]
0 & 0 & 0 & 0
\end{pmatrix}
$$

The first and third columns contain the pivots. Hence $r(A) = 2,$ and the rank-nullity theorem gives $\dim \ker(L_A) = 4 - 2 = 2.$

The free variables are $x_2$ and $x_4.$ The two nonzero equations are $x_1 + 2x_2 + x_4 = 0$ and $x_3 + x_4 = 0,$ so $x_1 = -2x_2 - x_4$ and $x_3 = -x_4.$ Setting each free variable in turn equal to $1,$ with the other equal to $0,$ gives:

$$\mathbf{k}_1 = (-2, 1, 0, 0)$$

$$\mathbf{k}_2 = (-1, 0, -1, 1)$$

If $a\mathbf{k}_1 + b\mathbf{k}_2 = \mathbf{0},$ the fourth entry gives $b = 0,$ and the second entry then gives $a = 0.$ Thus the two vectors are independent. Since the kernel has dimension $2,$ they form a basis of $\ker(L_A).$

The second column of $A$ is twice the first, and the fourth is the sum of the first and the third. Hence the first and third columns form a basis of the image:

$$\mathrm{im}(L_A) = \mathrm{span}\{\ (1, 2, 1), (0, 1, 1)\ \}$$

The image is therefore the plane in $\mathbb{R}^3$ with equation $y_1 - y_2 + y_3 = 0.$ Both basis vectors satisfy the equation, and the solution space of one nonzero homogeneous equation in $\mathbb{R}^3$ has dimension $2.$

It follows that $A\mathbf{x} = \mathbf{b}$ is solvable if and only if $b_1 - b_2 + b_3 = 0.$ For $\mathbf{b} = (1, 3, 2),$ the condition holds. Row reduction of the augmented matrix gives $x_1 = 1 - 2x_2 - x_4$ and $x_3 = 1 - x_4.$ Taking $x_2 = x_4 = 0$ gives the particular solution $\mathbf{v}_0 = (1, 0, 1, 0).$ Hence the complete solution set is:

$$L_A^{-1}(\{\ \mathbf{b}\ \}) = (1, 0, 1, 0) + \mathrm{span}\{\ \mathbf{k}_1, \mathbf{k}_2\ \}$$

The two free parameters agree with $\dim \ker(L_A) = 2.$ The equation $b_1 - b_2 + b_3 = 0$ describes the two-dimensional image inside $\mathbb{R}^3.$

> For null space, column space, rank-nullity and quotient factorization, see Anthony W. Knapp, Basic Algebra, Chapter II, Sections 2, 3, and 5, listed in the [bibliography](../bibliography/).
