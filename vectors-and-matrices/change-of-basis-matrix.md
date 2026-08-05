---
title: Coordinates and the Change-of-Basis Matrix
source: https://algebrica.org/change-of-basis-matrix/
license: CC BY-NC 4.0
tags:
  - basis
  - change-of-basis
  - coordinates
  - endomorphism
  - linear-algebra
  - linear-map
  - matrices
  - similar-matrices
  - vector-space
---
## Coordinates relative to an ordered basis

Let $V$ be a [vector space](../vector-spaces/) of dimension $n$ over a [field](../fields/) $F.$ An ordered basis of $V$ is a finite sequence $\mathcal{B} = (\mathbf{v}_1, \ldots, \mathbf{v}_n)$ whose terms form a basis. Every vector $\mathbf{v} \in V$ then has a unique expansion:

$$\mathbf{v} = \alpha_1\mathbf{v}_1 + \cdots + \alpha_n\mathbf{v}_n$$

The coefficients exist because $\mathcal{B}$ spans $V,$ and they are unique because $\mathcal{B}$ is [linearly independent](../linear-combinations/). If a second expansion has coefficients $\beta_1, \ldots, \beta_n,$ subtracting one expansion from the other gives:

$$(\alpha_1 - \beta_1)\mathbf{v}_1 + \cdots + (\alpha_n - \beta_n)\mathbf{v}_n = \mathbf{0}$$

Linear independence forces every coefficient of this combination to vanish, so $\alpha_i = \beta_i$ for each $i.$

The coordinate column of $\mathbf{v}$ with respect to $\mathcal{B}$ is the column formed by the coefficients of the expansion:

$$
[\mathbf{v}]_{\mathcal{B}} =
\begin{pmatrix}
\alpha_1 \\[6pt]
\vdots \\[6pt]
\alpha_n
\end{pmatrix} \in F^n
$$

Coordinates are written as columns so that a [matrix](../matrices/) acts on them by multiplication on the left.

- - -

The coordinate map $C_{\mathcal{B}} : V \to F^n$ sends $\mathbf{v}$ to $[\mathbf{v}]_{\mathcal{B}}.$ It is linear. If $\mathbf{u} = \sum_i \alpha_i\mathbf{v}_i$ and $\mathbf{w} = \sum_i \beta_i\mathbf{v}_i,$ then $\lambda\mathbf{u} + \mu\mathbf{w} = \sum_i (\lambda\alpha_i + \mu\beta_i)\mathbf{v}_i.$ By uniqueness of the expansion, the coordinates of $\lambda\mathbf{u} + \mu\mathbf{w}$ are the scalars $\lambda\alpha_i + \mu\beta_i.$ The map is injective because a vector with zero coordinates is the zero vector, and surjective because any $n$ scalars can be used as coefficients. Hence $C_{\mathcal{B}}$ is an [isomorphism](../homomorphisms-and-isomorphisms/) and $V \cong F^n.$

The isomorphism depends on the basis and on its ordering. In $\mathbb{R}^2$ the vector $\mathbf{v} = (3, 1)$ has coordinate column $(3, 1)^{\mathsf{T}}$ with respect to $(\mathbf{e}_1, \mathbf{e}_2)$ and coordinate column $(1, 3)^{\mathsf{T}}$ with respect to $(\mathbf{e}_2, \mathbf{e}_1).$ A basis has no prescribed order, whereas an ordered basis has an enumeration that fixes the positions of the coordinates.

The choice of basis changes which coefficients appear as coordinates. In the space $P_2(\mathbb{R})$ of real [polynomials](../polynomials/) of degree at most $2,$ the monomials $1, x, x^2$ give the coefficients of $p$ in the usual sense, while the basis $1, x - 1, (x - 1)^2$ gives the coefficients of the [Taylor expansion](../taylor-formula-with-remainder/) of $p$ at $1.$ For $p(x) = x^2$ the identity $x^2 = 1 + 2(x - 1) + (x - 1)^2$ shows that the two coordinate columns are $(0, 0, 1)^{\mathsf{T}}$ and $(1, 2, 1)^{\mathsf{T}}.$

## The change-of-basis matrix

Fix two ordered bases of the same space $V:$

$$\mathcal{B} = (\mathbf{v}_1, \ldots, \mathbf{v}_n) \qquad \mathcal{B}' = (\mathbf{v}'_1, \ldots, \mathbf{v}'_n)$$

For each $j,$ unique scalars $p_{1j}, \ldots, p_{nj}$ satisfy:

$$\mathbf{v}_j = \sum_{i=1}^{n} p_{ij}\mathbf{v}'_i$$

The change-of-basis matrix from $\mathcal{B}$ to $\mathcal{B}'$ is the square matrix $P_{\mathcal{B} \to \mathcal{B}'} = (p_{ij})$ of order $n.$ Its $j$-th column is the coordinate column $[\mathbf{v}_j]_{\mathcal{B}'}.$ The matrix is also called the transition matrix between the two bases.

Take $\mathbf{v} \in V$ with coordinates $\alpha_1, \ldots, \alpha_n$ in $\mathcal{B},$ substitute the expansion of each $\mathbf{v}_j,$ and exchange the two finite sums:

$$
\begin{align}
\mathbf{v} &= \sum_{j=1}^{n} \alpha_j\mathbf{v}_j \\[6pt]
  &= \sum_{j=1}^{n} \alpha_j \sum_{i=1}^{n} p_{ij}\mathbf{v}'_i \\[6pt]
  &= \sum_{i=1}^{n} \left(\sum_{j=1}^{n} p_{ij}\alpha_j\right)\mathbf{v}'_i
\end{align}
$$

The inner sum is the $i$-th entry of the product $P_{\mathcal{B} \to \mathcal{B}'}[\mathbf{v}]_{\mathcal{B}},$ and the outer sum is an expansion of $\mathbf{v}$ in $\mathcal{B}'.$ Uniqueness of coordinates therefore gives the change-of-basis formula:

$$[\mathbf{v}]_{\mathcal{B}'} = P_{\mathcal{B} \to \mathcal{B}'}[\mathbf{v}]_{\mathcal{B}}$$

> The direction of the arrow fixes both parts of the convention. The columns of $P_{\mathcal{B} \to \mathcal{B}'}$ are the vectors of $\mathcal{B}$ expressed in $\mathcal{B}',$ and multiplication by this matrix converts $\mathcal{B}$-coordinates into $\mathcal{B}'$-coordinates. The reverse conversion uses $P_{\mathcal{B}' \to \mathcal{B}}.$ The composition law below proves that the two matrices are inverses.

No other matrix satisfies the formula. If $M[\mathbf{v}]_{\mathcal{B}} = [\mathbf{v}]_{\mathcal{B}'}$ for every $\mathbf{v},$ take $\mathbf{v} = \mathbf{v}_j.$ Then $[\mathbf{v}_j]_{\mathcal{B}}$ is the $j$-th standard column of $F^n,$ so the product $M[\mathbf{v}_j]_{\mathcal{B}}$ is the $j$-th column of $M,$ which must equal $[\mathbf{v}_j]_{\mathcal{B}'}.$

- - -

More generally, relative to an ordered basis $\mathcal{B}$ of $V$ and an ordered basis $\mathcal{C}$ of $W,$ the [matrix of a linear map](../linear-maps/) $T : V \to W$ has $[T(\mathbf{v}_j)]_{\mathcal{C}}$ as its $j$-th column. It is the unique matrix $A$ such that $[T(\mathbf{v})]_{\mathcal{C}} = A[\mathbf{v}]_{\mathcal{B}}$ for every $\mathbf{v} \in V.$ Taking $W = V,$ $T = \mathrm{id}_V$ and $\mathcal{C} = \mathcal{B}'$ shows that $P_{\mathcal{B} \to \mathcal{B}'}$ is the matrix of the identity map relative to $\mathcal{B}$ in the domain and $\mathcal{B}'$ in the codomain. Each vector of $V$ is unchanged, while its coordinate column changes.

## Invertibility and composition of changes

Let $\mathcal{B},$ $\mathcal{B}'$ and $\mathcal{B}''$ be three ordered bases of $V.$ Applying the change-of-basis formula twice to an arbitrary $\mathbf{v}$ gives:

$$[\mathbf{v}]_{\mathcal{B}''} = P_{\mathcal{B}' \to \mathcal{B}''}[\mathbf{v}]_{\mathcal{B}'} = P_{\mathcal{B}' \to \mathcal{B}''}P_{\mathcal{B} \to \mathcal{B}'}[\mathbf{v}]_{\mathcal{B}}$$

The product on the right satisfies the defining property of the change of basis from $\mathcal{B}$ to $\mathcal{B}'',$ so uniqueness gives the composition law:

$$P_{\mathcal{B}' \to \mathcal{B}''}P_{\mathcal{B} \to \mathcal{B}'} = P_{\mathcal{B} \to \mathcal{B}''}$$

The $j$-th column of $P_{\mathcal{B} \to \mathcal{B}}$ is $[\mathbf{v}_j]_{\mathcal{B}},$ the $j$-th standard column, so $P_{\mathcal{B} \to \mathcal{B}} = I_n.$ Setting $\mathcal{B}'' = \mathcal{B}$ in the composition law gives:

$$P_{\mathcal{B}' \to \mathcal{B}}P_{\mathcal{B} \to \mathcal{B}'} = I_n$$

Exchanging the roles of the two bases gives the product in the other order. Every change-of-basis matrix is therefore [invertible](../inverse-matrix/), and:

$$P_{\mathcal{B} \to \mathcal{B}'}^{-1} = P_{\mathcal{B}' \to \mathcal{B}}$$

In particular $\det P_{\mathcal{B} \to \mathcal{B}'} \neq 0,$ since a matrix is invertible exactly when its [determinant](../determinant/) is nonzero.

- - -

Conversely, fix an ordered basis $\mathcal{B}' = (\mathbf{v}'_1, \ldots, \mathbf{v}'_n)$ of $V,$ take an invertible matrix $P = (p_{ij})$ of order $n,$ and define $n$ vectors by:

$$\mathbf{v}_j = \sum_{i=1}^{n} p_{ij}\mathbf{v}'_i$$

To show that these vectors form a basis, suppose that $\sum_j \gamma_j\mathbf{v}_j = \mathbf{0}.$ Applying $C_{\mathcal{B}'}$ gives $\sum_j \gamma_j[\mathbf{v}_j]_{\mathcal{B}'} = \mathbf{0}.$ These coordinate columns are the columns of $P.$ Since $P$ is invertible, its columns are linearly independent, so every $\gamma_j$ vanishes. Thus $\mathbf{v}_1, \ldots, \mathbf{v}_n$ are $n$ linearly independent vectors in a space of dimension $n.$ They form an ordered basis $\mathcal{B}$ with $P_{\mathcal{B} \to \mathcal{B}'} = P.$

The change-of-basis matrices on $V$ are exactly the invertible matrices of order $n.$ Once one ordered basis has been fixed, the ordered bases of $V$ correspond bijectively to the elements of the [general linear group](../groups/) $\mathrm{GL}_n(F).$

## Worked examples

In $\mathbb{R}^2,$ let $\mathcal{E} = (\mathbf{e}_1, \mathbf{e}_2)$ be the standard basis, and set $\mathbf{u}_1 = (1, 1)$ and $\mathbf{u}_2 = (1, -1).$ If $a\mathbf{u}_1 + b\mathbf{u}_2 = \mathbf{0},$ then $a + b = 0$ and $a - b = 0,$ so $a = b = 0.$ Thus $\mathcal{B} = (\mathbf{u}_1, \mathbf{u}_2)$ is an ordered basis. Coordinates with respect to $\mathcal{E}$ are the entries themselves, so the columns of $P_{\mathcal{B} \to \mathcal{E}}$ are $\mathbf{u}_1$ and $\mathbf{u}_2:$

$$
P_{\mathcal{B} \to \mathcal{E}} =
\begin{pmatrix}
1 & 1 \\[6pt]
1 & -1
\end{pmatrix}
$$

The change in the opposite direction is the inverse matrix:

$$
P_{\mathcal{E} \to \mathcal{B}} = -\frac{1}{2}
\begin{pmatrix}
-1 & -1 \\[6pt]
-1 & 1
\end{pmatrix}
=
\begin{pmatrix}
\dfrac{1}{2} & \dfrac{1}{2} \\[6pt]
\dfrac{1}{2} & -\dfrac{1}{2}
\end{pmatrix}
$$

For $\mathbf{v} = (3, 1)$ the change-of-basis formula gives:

$$
[\mathbf{v}]_{\mathcal{B}} =
\begin{pmatrix}
\dfrac{1}{2} & \dfrac{1}{2} \\[6pt]
\dfrac{1}{2} & -\dfrac{1}{2}
\end{pmatrix}
\begin{pmatrix}
3 \\[6pt]
1
\end{pmatrix}
=
\begin{pmatrix}
2 \\[6pt]
1
\end{pmatrix}
$$

The expansion $2\mathbf{u}_1 + \mathbf{u}_2 = (2, 2) + (1, -1) = (3, 1)$ verifies the coordinate column. The given vectors determine $P_{\mathcal{B} \to \mathcal{E}}$ directly, while its inverse changes $\mathcal{E}$-coordinates into $\mathcal{B}$-coordinates.

- - -

The polynomial bases from the first section are:

$$\mathcal{M} = (1, x, x^2) \qquad \mathcal{T} = (1, x - 1, (x - 1)^2)$$

The expansions $1 = 1,$ $x = 1 + (x - 1)$ and $x^2 = 1 + 2(x - 1) + (x - 1)^2$ give the three columns of the change of basis from $\mathcal{M}$ to $\mathcal{T}:$

$$
P_{\mathcal{M} \to \mathcal{T}} =
\begin{pmatrix}
1 & 1 & 1 \\[6pt]
0 & 1 & 2 \\[6pt]
0 & 0 & 1
\end{pmatrix}
$$

For the reverse direction, the identities $1 = 1,$ $x - 1 = -1 + x$ and $(x - 1)^2 = 1 - 2x + x^2$ give the three columns:

$$
P_{\mathcal{T} \to \mathcal{M}} =
\begin{pmatrix}
1 & -1 & 1 \\[6pt]
0 & 1 & -2 \\[6pt]
0 & 0 & 1
\end{pmatrix}
$$

Multiplying the two matrices in either order gives $I_3.$ For $p(x) = a + bx + cx^2$ the coordinate column in $\mathcal{T}$ is:

$$
P_{\mathcal{M} \to \mathcal{T}}
\begin{pmatrix}
a \\[6pt]
b \\[6pt]
c
\end{pmatrix}
=
\begin{pmatrix}
a + b + c \\[6pt]
b + 2c \\[6pt]
c
\end{pmatrix}
$$

The three entries are $p(1),$ $p'(1)$ and $p''(1)/2,$ the Taylor coefficients of $p$ at $1.$ Thus $P_{\mathcal{M} \to \mathcal{T}}$ changes the Taylor coefficients of $p$ at $0$ into those at $1.$

## Change of basis for a linear map

Let $W$ be a vector space of dimension $m$ over $F,$ let $T : V \to W$ be a [linear map](../linear-maps/), and choose two ordered bases $\mathcal{B},$ $\mathcal{B}'$ of $V$ and two ordered bases $\mathcal{C},$ $\mathcal{C}'$ of $W.$ Write $A$ for the matrix of $T$ relative to $\mathcal{B}$ and $\mathcal{C},$ and $A'$ for the matrix of $T$ relative to $\mathcal{B}'$ and $\mathcal{C}'.$ Set:

$$P = P_{\mathcal{B}' \to \mathcal{B}} \qquad Q = P_{\mathcal{C}' \to \mathcal{C}}$$

The matrix $P$ converts $\mathcal{B}'$-coordinates into $\mathcal{B}$-coordinates, while $Q$ converts $\mathcal{C}'$-coordinates into $\mathcal{C}$-coordinates. Hence $Q^{-1}$ converts $\mathcal{C}$-coordinates into $\mathcal{C}'$-coordinates. For $\mathbf{v} \in V,$ the three coordinate operations are:

$$
\begin{align}
[T(\mathbf{v})]_{\mathcal{C}'} &= Q^{-1}[T(\mathbf{v})]_{\mathcal{C}} \\[6pt]
  &= Q^{-1}A[\mathbf{v}]_{\mathcal{B}} \\[6pt]
  &= Q^{-1}AP[\mathbf{v}]_{\mathcal{B}'}
\end{align}
$$

The equality holds for every $\mathbf{v} \in V,$ so uniqueness of the matrix of $T$ gives:

$$A' = Q^{-1}AP$$

Two matrices $A$ and $A'$ of size $m \times n$ are equivalent when $A' = Q^{-1}AP$ for an invertible matrix $P$ of order $n$ and an invertible matrix $Q$ of order $m.$ Equivalent matrices are matrices of the same linear map relative to different bases of the domain and the codomain.

- - -

The rank determines a normal form under independent changes of basis in the domain and the codomain. Let $r$ be the [rank](../rank-of-a-matrix/) of $T.$ By the [rank-nullity theorem](../kernel-and-image-of-a-linear-map/), the kernel of $T$ has dimension $n - r.$ Choose vectors $\mathbf{u}_1, \ldots, \mathbf{u}_r$ of $V$ whose images form a basis of $\mathrm{im}(T),$ choose a basis $\mathbf{k}_1, \ldots, \mathbf{k}_{n-r}$ of $\ker(T),$ and take:

$$\mathcal{B}' = (\mathbf{u}_1, \ldots, \mathbf{u}_r, \mathbf{k}_1, \ldots, \mathbf{k}_{n-r})$$

These $n$ vectors are linearly independent. If $\sum_{i=1}^{r} a_i\mathbf{u}_i + \sum_{j=1}^{n-r} b_j\mathbf{k}_j = \mathbf{0},$ applying $T$ gives $\sum_{i=1}^{r} a_iT(\mathbf{u}_i) = \mathbf{0}.$ Since the vectors $T(\mathbf{u}_1), \ldots, T(\mathbf{u}_r)$ are linearly independent, every $a_i$ is zero. The remaining relation $\sum_{j=1}^{n-r} b_j\mathbf{k}_j = \mathbf{0}$ then implies that every $b_j$ is zero. Thus $\mathcal{B}'$ is an ordered basis of $V.$ The linearly independent vectors $T(\mathbf{u}_1), \ldots, T(\mathbf{u}_r)$ can be completed to an ordered basis $\mathcal{C}'$ of $W.$ By construction, the first $r$ columns of the matrix of $T$ are the first $r$ standard columns of $F^m,$ and the remaining columns are zero. Hence the matrix in these bases is:

$$
A' =
\begin{pmatrix}
I_r & 0 \\[6pt]
0 & 0
\end{pmatrix}
$$

Every $m \times n$ matrix of rank $r$ is therefore equivalent to this one. Since multiplication by an invertible matrix preserves the rank, two matrices of the same size are equivalent if and only if they have the same rank. Thus the rank completely determines the equivalence class when the bases of the domain and the codomain may be chosen independently.

## Endomorphisms and similar matrices

For an endomorphism $T : V \to V,$ its matrix in an ordered basis $\mathcal{B}$ is the matrix relative to $\mathcal{B}$ in both the domain and the codomain. The change-of-basis formula therefore contains one matrix and its inverse. Let $A$ be the matrix of $T$ in $\mathcal{B},$ let $A'$ be its matrix in $\mathcal{B}',$ and set $P = P_{\mathcal{B}' \to \mathcal{B}}.$ The formula of the previous section with $Q = P$ becomes:

$$A' = P^{-1}AP$$

Two square matrices $A$ and $A'$ of order $n$ are similar when $A' = P^{-1}AP$ for some invertible $P.$ Similarity is an equivalence relation. It is reflexive because $A = I^{-1}AI.$ It is symmetric because $A' = P^{-1}AP$ gives $A = (P^{-1})^{-1}A'P^{-1}.$ It is transitive because $A'' = R^{-1}A'R$ and $A' = P^{-1}AP$ give $A'' = (PR)^{-1}A(PR).$ The similarity class of $A$ is the set of matrices of the fixed endomorphism $T$ relative to the ordered bases of $V.$

- - -

The determinant is independent of the ordered basis, because the product rule gives:

$$\det(P^{-1}AP) = \det(P)^{-1}\det(A)\det(P) = \det(A)$$

The [characteristic polynomial](../eigenvalues-and-eigenvectors/) is independent of the ordered basis because $P^{-1}AP - \lambda I = P^{-1}(A - \lambda I)P$ and therefore $\det(P^{-1}AP - \lambda I) = \det(A - \lambda I).$ Similar matrices have the same eigenvalues with the same algebraic multiplicities. The [trace](../matrices/) is invariant because $\mathrm{tr}(XY) = \mathrm{tr}(YX)$ gives $\mathrm{tr}(P^{-1}AP) = \mathrm{tr}(APP^{-1}) = \mathrm{tr}(A).$ The rank is invariant because similar matrices are in particular equivalent.

Similarity is a finer relation than equivalence. The matrices $I_2$ and $\mathrm{diag}(1, 2)$ both have rank $2,$ so they are equivalent, but $P^{-1}I_2P = I_2$ for every invertible $P,$ so the only matrix similar to $I_2$ is $I_2$ itself. Equivalence permits independent basis changes in the domain and the codomain, whereas similarity uses the same basis change on both sides. Rank classifies equivalence classes but not similarity classes.

- - -

A basis of [eigenvectors](../eigenvalues-and-eigenvectors/) makes the matrix of $T$ diagonal. If $\mathcal{B}' = (\mathbf{w}_1, \ldots, \mathbf{w}_n)$ satisfies $T(\mathbf{w}_j) = \lambda_j\mathbf{w}_j,$ then the $j$-th column of the matrix of $T$ in $\mathcal{B}'$ is $\lambda_j$ in position $j$ and zero elsewhere. Thus this matrix is $D = \mathrm{diag}(\lambda_1, \ldots, \lambda_n).$ If $A$ is the matrix of $T$ in the standard basis $\mathcal{E}$ of $F^n$ and $P = P_{\mathcal{B}' \to \mathcal{E}},$ then the columns of $P$ are the eigenvectors and the [diagonalization](../matrix-diagonalization/) formula is:

$$P^{-1}AP = D$$

Consider the endomorphism $T$ of $\mathbb{R}^2$ defined by $T(x, y) = (x + 2y, 2x + y),$ whose matrix in the standard basis is:

$$
A =
\begin{pmatrix}
1 & 2 \\[6pt]
2 & 1
\end{pmatrix}
$$

The basis $\mathcal{B} = (\mathbf{u}_1, \mathbf{u}_2)$ of the first worked example consists of eigenvectors, since $T(\mathbf{u}_1) = (3, 3) = 3\mathbf{u}_1$ and $T(\mathbf{u}_2) = (-1, 1) = -\mathbf{u}_2.$ The matrices computed in that example satisfy:

$$
\begin{pmatrix}
\dfrac{1}{2} & \dfrac{1}{2} \\[6pt]
\dfrac{1}{2} & -\dfrac{1}{2}
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\[6pt]
2 & 1
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\[6pt]
1 & -1
\end{pmatrix}
=
\begin{pmatrix}
3 & 0 \\[6pt]
0 & -1
\end{pmatrix}
$$

The endomorphism $T$ multiplies vectors on the line spanned by $(1, 1)$ by $3$ and vectors on the line spanned by $(1, -1)$ by $-1.$ These invariant lines are the coordinate axes relative to $\mathcal{B},$ and the matrix of $T$ in this basis is diagonal.

> For coordinates, transition matrices, equivalence and similarity, see Sheldon Axler, Linear Algebra Done Right, Chapter 3, and Anthony W. Knapp, Basic Algebra, Chapter II, Section 3, listed in the [bibliography](../bibliography/).
