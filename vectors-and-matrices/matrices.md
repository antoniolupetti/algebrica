---
title: Matrices
source: https://algebrica.org/matrices/
license: CC BY-NC 4.0
tags:
  - antisymmetric-matrices
  - linear-algebra
  - matrices
  - matrix-multiplication
  - matrix-operations
  - matrix-powers
  - nilpotent-matrices
  - trace
  - transpose
  - vector-space
---
## Introduction

A matrix is a rectangular array of [real numbers](../types-of-numbers/) arranged in rows and columns. A matrix with $m$ rows and $n$ columns is said to have dimensions $m \times n.$ For example, a $3 \times 2$ matrix has 3 rows and 2 columns. Each number appearing in a matrix is called an element. Elements are identified by two subscript indices: the first indicates the row and the second the column. Thus $a_{2,3}$ denotes the element in the second row and third column. A matrix $A$ of dimensions $m \times n$ is written as follows:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\[6pt]
a_{21} & a_{22} & \cdots & a_{2n} \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

This is also written in compact form as $A = (a_{ij}),$ where $a_{ij}$ denotes the element in the $i$-th row and $j$-th column, with $1 \leq i \leq m$ and $1 \leq j \leq n.$

> The set of all $m \times n$ matrices with real entries forms an abelian group under addition. When restricted to square matrices of order $n,$ the additional structure of matrix multiplication makes $M_{n \times n}(\mathbb{R})$ a [ring](../rings/). The subset of invertible matrices of order $n$ forms a [group](../groups/) under multiplication, known as the general linear group $GL(n, \mathbb{R}).$

## Vectors and the zero matrix

A matrix consisting of a single row is a row [vector](../vectors/), and a matrix consisting of a single column is  a column vector. The following are a row vector $A$ with 3 columns and a column vector $B$ with 3 rows:

$$
A = \begin{pmatrix} a_1 & a_2 & a_3 \end{pmatrix}
\qquad
B = \begin{pmatrix} b_1 \\[6pt] b_2 \\[6pt] b_3 \end{pmatrix}
$$

A matrix in which every element is equal to zero is the zero matrix, denoted $O.$ The zero matrix is the additive identity for matrix addition, as discussed below.

> Row and column vectors are matrices in the usual sense and obey all the same algebraic rules. They are treated as special cases here for clarity, but are studied more extensively in the context of [linear combinations](../linear-combinations/) and [vector spaces](../vector-spaces/).

## Square matrices and special types

A matrix is called square when its number of rows equals its number of columns, that is, when it has dimensions $n \times n.$ The integer $n$ the order of the matrix. In a square matrix, the elements $a_{ij}$ for which $i = j$ form the main diagonal ($a_{11}, a_{22}, a_{33}$.) The elements for which $i + j = n+1$ form the secondary diagonal:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\[6pt]
a_{21} & a_{22} & a_{23} \\[6pt]
a_{31} & a_{32} & a_{33}
\end{pmatrix}
$$

A square matrix in which all elements outside the main diagonal are zero is a diagonal matrix. The following is an example of a $3 \times 3$ diagonal matrix:

$$
D = \begin{pmatrix}
4 & 0 & 0 \\[6pt]
0 & 5 & 0 \\[6pt]
0 & 0 & 6
\end{pmatrix}
$$

A square matrix is upper triangular if all elements below the main diagonal are zero, and lower triangular if all elements above the main diagonal are zero:

$$
U = \begin{pmatrix}
2 & -1 & 3 \\[6pt]
0 & 5 & 4 \\[6pt]
0 & 0 & 7
\end{pmatrix}
\qquad
L = \begin{pmatrix}
3 & 0 & 0 \\[6pt]
-2 & 6 & 0 \\[6pt]
5 & 1 & 4
\end{pmatrix}
$$

A square matrix $A$ is symmetric if it equals its own transpose, that is, if $A = A^{\mathrm{T}}.$ This means that $a_{ij} = a_{ji}$ for all $i$ and $j$: the element in row $i$ and column $j$ equals the element in row $j$ and column $i.$ The following is a $3 \times 3$ symmetric matrix:

$$
S = \begin{pmatrix}
1 & 3 & -2 \\[6pt]
3 & 0 & 5 \\[6pt]
-2 & 5 & 4
\end{pmatrix}
$$

> Symmetric matrices appear in quadratic forms, inner product spaces, and spectral theory. Every real symmetric matrix has real [eigenvalues](../eigenvalues-and-eigenvectors/) and an orthogonal basis of eigenvectors, a result known as the spectral theorem.

A square matrix $A$ is antisymmetric, also called skew-symmetric, if it equals the opposite of its transpose, that is if $A^{\mathrm{T}} = -A.$ In terms of entries this reads $a_{ij} = -a_{ji}$ for all $i$ and $j.$ Setting $i = j$ gives $a_{ii} = -a_{ii},$ so every entry on the main diagonal of an antisymmetric matrix is zero. The following is a $3 \times 3$ antisymmetric matrix:

$$
T = \begin{pmatrix}
0 & 2 & -3 \\[6pt]
-2 & 0 & 5 \\[6pt]
3 & -5 & 0
\end{pmatrix}
$$

> The only matrix that is at once symmetric and antisymmetric is the zero matrix, since $a_{ij} = a_{ji}$ and $a_{ij} = -a_{ji}$ together force $a_{ij} = 0.$ Every square matrix splits uniquely as $A = \frac{1}{2}(A + A^{\mathrm{T}}) + \frac{1}{2}(A - A^{\mathrm{T}}),$ in which the first term is symmetric and the second antisymmetric.

## Transpose

The transpose of a matrix $A$ of dimensions $m \times n,$ denoted $A^{\mathrm{T}},$ is the matrix of dimensions $n \times m$ obtained by interchanging the rows and columns of $A.$ Formally, the element in position $(i,j)$ of $A^{\mathrm{T}}$ is the element in position $(j,i)$ of $A.$ For example:

$$
A = \begin{pmatrix}
2 & -1 & 3 \\[6pt]
7 & 5 & 4 \\[6pt]
9 & 6 & 8
\end{pmatrix}
\qquad
A^{\mathrm{T}} = \begin{pmatrix}
2 & 7 & 9 \\[6pt]
-1 & 5 & 6 \\[6pt]
3 & 4 & 8
\end{pmatrix}
$$

The transpose satisfies the following properties, for matrices $A$ and $B$ of compatible dimensions and any scalar $k$:

+ $(A^{\mathrm{T}})^{\mathrm{T}} = A$
+ $(A + B)^{\mathrm{T}} = A^{\mathrm{T}} + B^{\mathrm{T}}$
+ $(kA)^{\mathrm{T}} = k A^{\mathrm{T}}$
+ $(AB)^{\mathrm{T}} = B^{\mathrm{T}} A^{\mathrm{T}}$

> The identity $(AB)^{\mathrm{T}} = B^{\mathrm{T}} A^{\mathrm{T}}$ reverses the order of the factors. This reversal is necessary because matrix multiplication is not commutative, and it recurs in several other contexts, including the [inverse of a product](../inverse-matrix/).

## Additive inverse matrix

The additive inverse of a matrix $A,$ denoted $-A,$ is the matrix obtained by negating every element of $A$: each entry $a_{ij}$ becomes $-a_{ij}.$ The matrices $A$ and $-A$ have the same dimensions, and their sum is the zero matrix:

$$A + (-A) = O$$

For example:

$$
A = \begin{pmatrix}
2 & -1 & 3 \\[6pt]
7 & 5 & 4 \\[6pt]
9 & 6 & 8
\end{pmatrix}
\qquad
-A = \begin{pmatrix}
-2 & 1 & -3 \\[6pt]
-7 & -5 & -4 \\[6pt]
-9 & -6 & -8
\end{pmatrix}
$$

## Matrix addition and subtraction

Two matrices can be added or subtracted only if they have the same dimensions. Given two $m \times n$ matrices $A = (a_{ij})$ and $B = (b_{ij}),$ their sum $C = A + B$ is the $m \times n$ matrix defined by:

$$c_{ij} = a_{ij}+b_{ij}$$

Each element of $C$ is the sum of the corresponding elements of $A$ and $B.$ The following example illustrates the computation for two $2 \times 3$ matrices:

$$
A = \begin{pmatrix}
2 & -1 & 3 \\[6pt]
7 & 5 & 4
\end{pmatrix}
\qquad
B = \begin{pmatrix}
4 & 0 & -2 \\[6pt]
1 & 3 & 6
\end{pmatrix}
$$

The sum is the following:

$$
\begin{align}
A+B &= \begin{pmatrix}
2+4 & -1+0 & 3+(-2) \\[6pt]
7+1 & 5+3 & 4+6
\end{pmatrix} \\[12pt]
&= \begin{pmatrix}
6 & -1 & 1 \\[6pt]
8 & 8 & 10
\end{pmatrix}
\end{align}
$$

The difference $A-B$ is defined as $A+(-B),$ that is, the sum of $A$ and the additive inverse of $B.$ Matrix addition satisfies the following properties, for any matrices $A,$ $B,$ $C$ of dimensions $m \times n$:

+ Commutativity: $A+B = B+A.$ The order in which two matrices are added does not affect the result.
+ Associativity: $(A+B)+C = A+(B+C).$ Sums of three or more matrices can be computed in any grouping.
+ Additive identity: $A+O = A,$ where $O$ is the zero matrix of the same dimensions. Adding the zero matrix leaves $A$ unchanged.
+ Additive inverse: $A+(-A) = O.$ Every matrix has a unique additive inverse.

## Scalar multiplication

Given a matrix $A = (a_{ij})$ of dimensions $m \times n$ and a real number $k,$ the scalar multiple $kA$ is the $m \times n$ matrix whose element in position $(i,j)$ is $k \cdot a_{ij}.$ Every entry of the matrix is multiplied by $k.$ For example, with $k = 2$:

$$
A = \begin{pmatrix}
1 & -2 & 4 \\[6pt]
0 & 3 & -1
\end{pmatrix}
\qquad
2A = \begin{pmatrix}
2 & -4 & 8 \\[6pt]
0 & 6 & -2
\end{pmatrix}
$$

Scalar multiplication satisfies the following properties, for matrices $A$ and $B$ of the same dimensions and real numbers $k$ and $h$:

+ Associativity: $k(hA) = (kh)A.$ Successive scalar multiplications can be combined into one.
+ Distributivity over matrix addition: $k(A+B) = kA+kB.$ A scalar distributes over a sum of matrices.
+ Distributivity over scalar addition: $(k+h)A = kA+hA.$ A sum of scalars distributes over a single matrix.

> Matrix addition and scalar multiplication together satisfy the vector space axioms, so $M_{m \times n}(\mathbb{R})$ is a real [vector space](../vector-spaces/). The $mn$ matrices with a single entry equal to $1$ and zeros elsewhere form a basis, so its dimension is $mn.$

## Matrix multiplication

Matrix multiplication is defined under a compatibility condition: the product $AB$ is defined only when the number of columns of $A$ equals the number of rows of $B.$ If $A$ has dimensions $m \times n$ and $B$ has dimensions $n \times p,$ the product $C = AB$ is a matrix of dimensions $m \times p,$ whose element in position $(i,j)$ is defined by:

$$c_{ij} = \sum_{k=1}^{n} a_{ik} b_{kj}$$

Each entry $c_{ij}$ is computed by taking the dot product of the $i$-th row of $A$ with the $j$-th column of $B$: multiply corresponding entries pairwise and sum the results. The following example computes the product of a $2 \times 3$ matrix $A$ and a $3 \times 2$ matrix $B$:

$$
A = \begin{pmatrix}
1 & -2 & 3 \\[6pt]
0 & 4 & -1
\end{pmatrix}
\qquad
B = \begin{pmatrix}
2 & 0 \\[6pt]
-1 & 5 \\[6pt]
4 & -3
\end{pmatrix}
$$

The entries $c_{ij}$ of the product matrix $AB$ are obtained by multiplying each row of $A$ by each column of $B$:

$$
\begin{align}
c_{11} &= (1)(2)+(-2)(-1)+(3)(4) = 16 \\[6pt]
c_{12} &= (1)(0)+(-2)(5)+(3)(-3) = -19 \\[6pt]
c_{21} &= (0)(2)+(4)(-1)+(-1)(4) = -8 \\[6pt]
c_{22} &= (0)(0)+(4)(5)+(-1)(-3) = 23
\end{align}
$$

The result is a $2 \times 2$ matrix, consistent with the dimensions $m \times p = 2 \times 2.$

$$
C = AB = \begin{pmatrix}
16 & -19 \\[6pt]
-8 & 23
\end{pmatrix}
$$

> Matrix multiplication is not commutative in general. Even when both $AB$ and $BA$ are defined, the two products typically differ. This distinguishes matrix multiplication from multiplication of real numbers.

A further difference from the arithmetic of real numbers concerns products that vanish, since the product of two nonzero matrices can be the zero matrix. The matrices

$$
A = \begin{pmatrix} 2 & 4 \\[6pt] 1 & 2 \end{pmatrix}
\qquad
B = \begin{pmatrix} 2 & 4 \\[6pt] -1 & -2 \end{pmatrix}
$$

are both nonzero, yet their product vanishes:

$$
AB = \begin{pmatrix}
(2)(2)+(4)(-1) & (2)(4)+(4)(-2) \\[6pt]
(1)(2)+(2)(-1) & (1)(4)+(2)(-2)
\end{pmatrix}
=
\begin{pmatrix} 0 & 0 \\[6pt] 0 & 0 \end{pmatrix}
$$

The implication from $AB = O$ to $A = O$ or $B = O,$ valid for real numbers, has no analogue for matrices.

> A nonzero matrix that occurs as a factor of a product equal to the zero matrix is a zero divisor of the [ring](../rings/) $M_{n \times n}(\mathbb{R}).$ The presence of zero divisors is what prevents the cancellation law $AB = AC \implies B = C$ from holding for an arbitrary nonzero factor $A.$

- - -

The identity matrix of order $n,$ denoted $I_n,$ is the $n \times n$ square matrix with ones on the main diagonal and zeros elsewhere. It is the multiplicative identity, so for any matrix $A$ of compatible dimensions,

$$A \cdot I = I \cdot A = A$$

For example:

$$
\begin{pmatrix}
3 & 5 \\[6pt]
1 & -2
\end{pmatrix}
\cdot
\begin{pmatrix}
1 & 0 \\[6pt]
0 & 1
\end{pmatrix}
=
\begin{pmatrix}
3 & 5 \\[6pt]
1 & -2
\end{pmatrix}
$$

Matrix multiplication satisfies the following properties, for matrices of compatible dimensions:

+ Associativity: $(AB)C = A(BC).$ The order in which successive products are computed does not affect the result.
+ Left distributivity: $A(B+C) = AB+AC.$ Multiplication distributes over addition from the left.
+ Right distributivity: $(B+C)A = BA+CA.$ Multiplication distributes over addition from the right.
+ Non-commutativity: in general, $AB \neq BA,$ even when both products are defined.

## Powers of a square matrix

For a square matrix $A$ of order $n,$ the associativity of the product makes integer powers well defined. One sets $A^1 = A$ and, for every integer $p \geq 2,$ defines $A^p = A^{p-1} A,$ so that $A^2 = AA$ and $A^3 = AAA.$ Since the identity matrix is the multiplicative identity, it is consistent to set $A^0 = I_n.$

Non-commutativity changes the algebraic identities that hold without comment over the real numbers. Expanding $(A+B)^2$ by distributivity gives

$$(A+B)^2 = A^2 + AB + BA + B^2$$

which reduces to the familiar $A^2 + 2AB + B^2$ only when $A$ and $B$ commute, that is when $AB = BA.$ Take for instance

$$
A = \begin{pmatrix} 1 & 1 \\[6pt] 0 & 1 \end{pmatrix}
\qquad
B = \begin{pmatrix} 1 & 0 \\[6pt] 1 & 1 \end{pmatrix}
$$

These two matrices do not commute, since

$$
AB = \begin{pmatrix} 2 & 1 \\[6pt] 1 & 1 \end{pmatrix}
\qquad
BA = \begin{pmatrix} 1 & 1 \\[6pt] 1 & 2 \end{pmatrix}
$$

and a direct computation gives

$$
(A+B)^2 = \begin{pmatrix} 5 & 4 \\[6pt] 4 & 5 \end{pmatrix}
\qquad
A^2 + 2AB + B^2 = \begin{pmatrix} 6 & 4 \\[6pt] 4 & 4 \end{pmatrix}
$$

The two results disagree, so the binomial identity fails. The same obstruction affects the other standard factorizations, and an identity such as $A^2 - B^2 = (A+B)(A-B)$ holds only for commuting matrices.

## Nilpotent matrices

A square matrix $A$ is nilpotent if some positive integer power of it equals the zero matrix, that is if $A^p = O$ for some integer $p \geq 1.$ The smallest such $p$ is the index of nilpotency. An upper triangular matrix whose diagonal entries are all zero gives a typical example:

$$
N = \begin{pmatrix}
0 & 1 & 2 \\[6pt]
0 & 0 & 3 \\[6pt]
0 & 0 & 0
\end{pmatrix}
$$

Each power moves the nonzero entries further above the diagonal, so

$$
N^2 = \begin{pmatrix}
0 & 0 & 3 \\[6pt]
0 & 0 & 0 \\[6pt]
0 & 0 & 0
\end{pmatrix}
\qquad
N^3 = O
$$

and $N$ is nilpotent of index $3.$

A nilpotent matrix is never invertible. Suppose $A^p = O$ and that some matrix $B$ satisfies $AB = I_n.$ Then

$$A^{p-1} = A^{p-1} I_n = A^{p-1}(AB) = A^p B = OB = O$$

so the exponent drops by one. Repeating the step lowers it to $A = O,$ but the zero matrix gives $OB = O \neq I_n$ and cannot satisfy $AB = I_n.$ No such $B$ exists, which ties nilpotency to the criterion for invertibility discussed in the entry on the [inverse matrix](../inverse-matrix/).

## Trace

The trace of a square matrix $A$ of order $n,$ denoted $\mathrm{tr}(A),$ is the sum of the entries on its main diagonal:

$$\mathrm{tr}(A) = a_{11} + a_{22} + \cdots + a_{nn} = \sum_{i=1}^{n} a_{ii}$$

The trace is linear in its argument, so $\mathrm{tr}(A+B) = \mathrm{tr}(A) + \mathrm{tr}(B)$ and $\mathrm{tr}(kA) = k\mathrm{tr}(A)$ for every scalar $k.$ Transposition fixes the diagonal, hence $\mathrm{tr}(A^{\mathrm{T}}) = \mathrm{tr}(A).$ The trace of a product does not depend on the order of the factors, even though the product itself does. For square matrices $A$ and $B$ of order $n,$

$$\mathrm{tr}(AB) = \sum_{i=1}^{n} \sum_{k=1}^{n} a_{ik} b_{ki} = \sum_{k=1}^{n} \sum_{i=1}^{n} b_{ki} a_{ik} = \mathrm{tr}(BA)$$

> The trace equals the sum of the eigenvalues of $A,$ counted with algebraic multiplicity, as shown in the entry on [eigenvalues and eigenvectors](../eigenvalues-and-eigenvectors/).

> The definitions and properties in this entry were stated for real entries, but the operations of sum, scalar multiple, product, and transpose carry over unchanged to complex entries, and more generally to matrices over any [field](../fields/) $K.$ Only the field axioms are used in the proofs, so the same algebra holds whether $K$ is $\mathbb{R},$ $\mathbb{C},$ or another field.

To every square matrix of order $n$ one associates a real number called the [determinant](../determinant/), denoted $\det(A),$ which determines whether the matrix is invertible, as discussed in the entry on the [inverse matrix](../inverse-matrix/). The maximum number of linearly independent rows or columns is the [rank](../rank-of-a-matrix/). When a square matrix admits a basis of [eigenvectors](../eigenvalues-and-eigenvectors/), it can be reduced to diagonal form by [diagonalization](../matrix-diagonalization/).
