---
title: Linear Combinations
source: https://algebrica.org/linear-combinations/
license: CC BY-NC 4.0
tags:
  - linear-algebra
  - linear-combinations
  - linear-independence
  - span
  - vector-spaces
  - vectors
---
## Definition

A linear combination relates [vectors](../vectors/) to one another within a given collection. Each vector is scaled by a real coefficient, and the scaled vectors are then summed to produce a new vector. From this operation the notions of span, linear independence, [rank](../rank-of-a-matrix/), and dimension are built, along with the geometric objects of $\mathbb{R}^n$ such as [lines](../lines/), planes, and higher-dimensional subspaces. Let $V = \mathbb{R}^n$ and consider a finite collection of vectors:

$$v_1, v_2, \dots, v_k \in \mathbb{R}^n$$

A linear combination of these vectors is any vector of the form:

$$c_1 v_1 + c_2 v_2 + \dots + c_k v_k$$

where $c_1, c_2, \dots, c_k \in \mathbb{R}$ are real scalars. Each vector $v_i$ is multiplied by a scalar coefficient $c_i,$ and the resulting scaled vectors are then added. The scalars determine how strongly each vector contributes to the final result.

- - -

A linear combination carries a concrete geometric meaning. Consider two vectors $v, w \in \mathbb{R}^n.$ By forming expressions of the type:

$$a v + b w$$

with $a, b \in \mathbb{R},$ we allow each vector to be independently scaled and then combined through vector addition. Varying the coefficients $a$ and $b$ produces an entire collection of vectors, all obtained from the same two building blocks.

+ If the vectors $v$ and $w$ are not scalar multiples of one another, these combinations sweep out a plane passing through the origin. Every point of that plane can be reached by a suitable choice of the coefficients.
+ If, on the other hand, the two vectors are collinear, all linear combinations collapse onto a single line through the origin, since one vector can already be expressed in terms of the other.

> In this way, linear combinations generate geometric objects such as lines and planes, and more generally subsets of $\mathbb{R}^n$ with a linear structure. The dimension of the object depends on how the vectors relate to one another and on whether they contribute independent directions.

## Coordinate representation

To understand more concretely how linear combinations operate, it is helpful to express everything in coordinates. Since vectors in $\mathbb{R}^n$ are represented as ordered $n$-tuples of real numbers, every operation on vectors can be described component by component. Suppose each vector $v_i \in \mathbb{R}^n$ has components:

$$
v_i =
\begin{pmatrix}
v_{i1} \\[6pt]
v_{i2} \\[6pt]
\vdots \\[6pt]
v_{in}
\end{pmatrix}
$$

When we form a linear combination of these vectors, the operation unfolds coordinatewise. Indeed, we obtain:

$$
c_1 v_1 + \dots + c_k v_k
=
\begin{pmatrix}
c_1 v_{11} + \dots + c_k v_{k1} \\[6pt]
c_1 v_{12} + \dots + c_k v_{k2} \\[6pt]
\vdots \\[6pt]
c_1 v_{1n} + \dots + c_k v_{kn}
\end{pmatrix}
$$

Each entry of the resulting vector is therefore a linear combination of [real numbers](../types-of-numbers/) drawn from the corresponding entries of the original vectors. Scalar multiplication and vector addition are performed independently in each coordinate. A linear combination is therefore carried out coordinate by coordinate, and the operation reduces to ordinary arithmetic entry by entry.

## Matrix-vector interpretation

The relationship between linear combinations and [matrices](../matrices/) becomes especially clear when we look at matrix-vector multiplication more closely. Consider a matrix whose columns are the vectors $v_1, \dots, v_k$:

$$
A =
\begin{pmatrix}
| & | & & | \\[6pt]
v_1 & v_2 & \dots & v_k \\[6pt]
| & | & & |
\end{pmatrix}
$$

Now take a vector of scalars:

$$
c =
\begin{pmatrix}
c_1 \\[6pt]
c_2 \\[6pt]
\vdots \\[6pt]
c_k
\end{pmatrix}
$$

When we compute the product $A c,$ each column of $A$ is multiplied by the corresponding entry of $c,$ and the resulting vectors are added together. Writing this explicitly, we obtain:

$$A c = c_1 v_1 + c_2 v_2 + \dots + c_k v_k$$

Multiplying a matrix by a vector is nothing more than forming a linear combination of its columns. The entries of the vector $c$ are the coefficients that determine how strongly each column contributes to the result.

> From this perspective, a matrix-vector product combines the columns of the matrix, and the vectors reachable as $A c$ are exactly the span of those columns.

## Linear systems and solvability

A [linear system](../rouche-capelli-theorem/) can be written in matrix form:

$$A x = b$$

This equation is a compact way of writing several linear [equations](../equations/) at once. Once we interpret matrix-vector multiplication as a linear combination of columns, the meaning of the system becomes much clearer. Suppose the columns of $A$ are the vectors $v_1, \dots, v_k.$ Expanding the product $A x$ according to the definition of matrix multiplication, we obtain:

$$x_1 v_1 + x_2 v_2 + \dots + x_k v_k = b$$

Seen in this way, solving the system means searching for scalars $x_1, \dots, x_k$ that combine the columns of $A$ to produce the vector $b.$ The problem of solvability acquires a geometric interpretation. The question becomes: can the vector $b$ be assembled from the columns of $A$? In other words, does $b$ belong to the set of all linear combinations generated by those vectors?

+ If such scalars exist, the system has at least one solution.
+ If no such combination is possible, the system is inconsistent.

The structure of the solution set is thus determined entirely by how the vector $b$ relates to the space generated by the columns of $A.$

## Span

Once the notion of linear combination is in place, a natural question arises: given a finite collection of vectors, what is the totality of vectors that can be produced by scaling and summing them in all possible ways? The set of all linear combinations of $v_1, \dots, v_k$ is called their span:

$$\mathrm{span}(v_1, \dots, v_k) = \\{\ \sum_{i=1}^k c_i v_i \mid c_i \in \mathbb{R}\ \\}$$

The span consists of every vector that can be built from $v_1, \dots, v_k$ using the operations of scalar multiplication and vector addition. It is the entire region of $\mathbb{R}^n$ that becomes accessible once those vectors are taken as building blocks.

The vectors $v_1, \dots, v_k$ are called a spanning set, or a set of generators, of this subspace, and the subspace is the one they generate. A vector space is finitely generated when some finite spanning set produces every one of its vectors, as $\mathbb{R}^n$ is generated by its $n$ standard unit vectors. The notions of basis and dimension, which refine the idea of a spanning set, are developed in the entry on [vector spaces](../vector-spaces/).

- - -

By construction, the span is closed under addition and scalar multiplication. If two vectors belong to the span, any linear combination of them also belongs to the span. For this reason, the span is a subspace of $\mathbb{R}^n.$ From a geometric point of view we have:

+ A single nonzero vector spans a line through the origin.
+ Two vectors that are not collinear span a plane through the origin.
+ Three vectors, provided they introduce independent directions, may span a three-dimensional subspace.

- - -

The geometric description above suggests that the span behaves like a flat region passing through the origin. This intuition can be made precise by verifying that the span satisfies the defining properties of a subspace of $\mathbb{R}^n.$ First, the zero vector belongs to the span. By choosing all coefficients equal to zero, we obtain:

$$0 = 0 v_1 + 0 v_2 + \dots + 0 v_k$$

Hence:

$$0 \in \mathrm{span}(v_1, \dots, v_k)$$

Second, the span is closed under linear combinations. Let:

$$u = \sum_{i=1}^{k} a_i v_i \quad w = \sum_{i=1}^{k} b_i v_i$$

be two arbitrary vectors in $\mathrm{span}(v_1, \dots, v_k),$ and let $\alpha, \beta \in \mathbb{R}.$ Then:

$$
\begin{align}
\alpha u + \beta w &= \alpha \sum_{i=1}^{k} a_i v_i + \beta \sum_{i=1}^{k} b_i v_i \\[6pt]
&= \sum_{i=1}^{k} (\alpha a_i+\beta b_i) v_i
\end{align}
$$

Since the coefficients $\alpha a_i + \beta b_i$ are real numbers, the resulting vector is again a linear combination of $v_1, \dots, v_k.$ Therefore:

$$\alpha u + \beta w \in \mathrm{span}(v_1, \dots, v_k)$$

These properties show that the span is a subspace of $\mathbb{R}^n,$ since it contains the zero vector and is closed under addition and scalar multiplication.

The span is moreover the smallest subspace of $\mathbb{R}^n$ that contains $v_1, \dots, v_k.$ Any subspace that contains these vectors must also contain all their scalar multiples and all sums of such multiples, hence every linear combination of them, so it contains the entire span. The span is therefore contained in every subspace that contains the generators, which is what it means to be the smallest among them.

## Example

A vector belongs to the span of others exactly when it can be written as a linear combination of them, that is, when suitable coefficients reproduce it. Testing membership in a span therefore amounts to solving a [linear system](../rouche-capelli-theorem/), as the following computation shows.

Consider the vectors in $\mathbb{R}^3$:

$$
v_1 =
\begin{pmatrix}
1 \\[6pt]
2 \\[6pt]
1
\end{pmatrix}
\quad
v_2 =
\begin{pmatrix}
0 \\[6pt]
1 \\[6pt]
1
\end{pmatrix}
$$

We ask whether the vector:

$$
b =
\begin{pmatrix}
3 \\[6pt]
7 \\[6pt]
5
\end{pmatrix}
$$

belongs to $\mathrm{span}(v_1, v_2).$ To answer this question, we must determine whether there exist scalars $c_1, c_2 \in \mathbb{R}$ such that:

$$c_1 v_1 + c_2 v_2 = b$$

Writing the linear combination explicitly, we obtain:

$$
c_1
\begin{pmatrix}
1 \\[6pt]
2 \\[6pt]
1
\end{pmatrix}
+
c_2
\begin{pmatrix}
0 \\[6pt]
1 \\[6pt]
1
\end{pmatrix}
=
\begin{pmatrix}
3 \\[6pt]
7 \\[6pt]
5
\end{pmatrix}
$$

Equating the components yields the system:

$$
\begin{cases}
c_1 = 3 \\[6pt]
2c_1 + c_2 = 7 \\[6pt]
c_1 + c_2 = 5
\end{cases}
$$

From the first equation we obtain $c_1 = 3.$ Substituting into the second equation gives:

$$2(3) + c_2 = 7 \quad \rightarrow \quad c_2 = 1$$

Checking the third equation, we obtain:

$$3 + 1 = 4 \neq 5$$

The system is inconsistent. Therefore, no scalars $c_1, c_2$ produce the vector $b,$ and we conclude that $b \notin \mathrm{span}(v_1, v_2).$

- - -

Now consider instead:

$$
b =
\begin{pmatrix}
3 \\[6pt]
7 \\[6pt]
4
\end{pmatrix}
$$

Repeating the same computation, we obtain:

$$
\begin{cases}
c_1 = 3 \\[6pt]
2c_1 + c_2 = 7 \\[6pt]
c_1 + c_2 = 4
\end{cases}
$$

Substituting $c_1 = 3$ into the second equation gives $c_2 = 1,$ and the third equation becomes:

$$3 + 1 = 4$$

which is satisfied. Hence:

$$b = 3 v_1 + 1 v_2$$

and therefore $b \in \mathrm{span}(v_1, v_2).$

This example shows that membership in a span is a solvability condition. A vector lies in the span of given vectors exactly when the corresponding linear system has a solution.

## Uniqueness of representation

Suppose that a vector $b$ can be written as a linear combination of the vectors $v_1, \dots, v_k,$ namely:

$$b = c_1 v_1 + \dots + c_k v_k$$

A natural question arises. Once such a representation has been found, are the coefficients $c_1, \dots, c_k$ uniquely determined? Or could there exist different choices of scalars producing the same vector $b$? To investigate this, imagine that two distinct families of scalars lead to the same vector. Subtracting the two representations would produce an expression of the form

$$c_1 v_1 + \dots + c_k v_k = 0$$

where not all the coefficients are zero. The existence of such a relation means that the zero vector itself can be obtained as a nontrivial linear combination of the vectors $v_1, \dots, v_k.$ This situation has an important structural consequence. If a nontrivial combination of the vectors yields the zero vector, then at least one of the vectors can be expressed as a linear combination of the others. In that case, the original representation of $b$ need not be unique: different choices of coefficients may lead to the same vector.

For instance, take $v_1 = (1, 1, -1),$ $v_2 = (2, -3, 0),$ and $v_3 = (-3, 2, 1)$ in $\mathbb{R}^3.$ Setting all coefficients to zero produces the zero vector, and so does the choice of all coefficients equal to one, since $v_1 + v_2 + v_3 = (0, 0, 0).$ The zero vector therefore has more than one representation as a linear combination of $v_1, v_2, v_3,$ and the same non-uniqueness is inherited by every vector in their span.

> The question of uniqueness is therefore connected with the existence of nontrivial linear relations among the vectors. When no such relation exists, that is, when the only way to obtain the zero vector is by setting all coefficients to zero, the representation of any vector in the span is necessarily unique. This property defines what it means for a collection of vectors to be linearly independent, a concept that will be examined in detail in the dedicated entry.

## Redundant vectors and minimal spanning sets

A spanning set may contain more vectors than it needs. Suppose one of the vectors, say $v_k,$ is a linear combination of the others:

$$v_k = a_1 v_1 + \dots + a_{k-1} v_{k-1}$$

Removing $v_k$ then leaves the span unchanged:

$$\mathrm{span}(v_1, \dots, v_{k-1}, v_k) = \mathrm{span}(v_1, \dots, v_{k-1})$$

Any linear combination that uses $v_k$ can be rewritten with $v_1, \dots, v_{k-1}$ alone, by replacing $v_k$ with the combination above and collecting the coefficients. A vector of this kind contributes no new direction and is called redundant.

Discarding redundant vectors one at a time reduces a spanning set without changing the subspace it generates, until no remaining vector is a linear combination of the others. The set reached in this way is a minimal spanning set, one that still generates the subspace while no proper subset of it does. Minimal spanning sets are the bases of the subspace, and they all have the same number of elements, the dimension, as shown in the entry on [vector spaces](../vector-spaces/).

## General vector spaces

The definition of linear combination given above is stated for [vectors](../vectors/) in $\mathbb{R}^n,$ but the concept extends without modification to any vector space over a field. Let $V$ be a vector space over a [field](../fields/) $\mathbb{F},$ and let $v_1, v_2, \dots, v_k \in V.$ A linear combination of these vectors is any element of $V$ of the form:

$$c_1 v_1 + c_2 v_2 + \dots + c_k v_k$$

where $c_1, c_2, \dots, c_k \in \mathbb{F}.$ The field $\mathbb{F}$ may be taken to be $\mathbb{R}$ or $\mathbb{C},$ and the vector space $V$ may be a space of [polynomials](../polynomials/), of [matrices](../matrices/), or of [continuous functions](../continuous-functions/), among many others. In each of these settings, the notions of span and linear independence carry over directly, and the structural results of linear algebra remain valid in full generality.

Not every vector space is finitely generated. The space of all [polynomials](../polynomials/) is an example, since any finite set of polynomials has a largest degree $d,$ and no polynomial of degree greater than $d$ is a linear combination of them, so no finite set can span the whole space. The same holds for spaces of functions, such as the continuous functions on an interval.

## Affine, conical, and convex combinations

The notion of linear combination is the most general within a family of related operations, all obtained by imposing restrictions on the coefficients. Each restriction selects a different geometric object and a different kind of subset closed under the corresponding operation. If the coefficients are required to sum to one:

$$c_1 + c_2 + \dots + c_k = 1$$

the resulting expression is called an affine combination. The set of all affine combinations of a given collection of vectors is an affine subspace, that is, a translate of a linear subspace that need not pass through the origin. Lines and planes not containing the origin are typical examples. If the coefficients are required to be nonnegative:

$$c_1, c_2, \dots, c_k \geq 0$$

the expression is called a conical combination, and the set of all such combinations forms a convex cone. Quadrants and orthants in $\mathbb{R}^n$ are simple instances.

If both conditions are imposed simultaneously, that is, nonnegative coefficients summing to one, the expression is called a convex combination. The set of all convex combinations of a finite collection of vectors is a convex polytope, the simplest example being the segment joining two points or the triangle determined by three.

> Vector subspaces are the smallest of these structures: every linear combination is in particular affine, conical, and convex, so a subspace is automatically all three. The converse does not hold, and this is what makes these notions more general.
