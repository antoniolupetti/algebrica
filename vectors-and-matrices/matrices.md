---
title: Matrices
source: https://algebrica.org/matrices/
license: CC BY-NC 4.0
tags:
  - linear-algebra
  - matrices
  - matrix-multiplication
  - matrix-operations
  - transpose
---
## Introduction

A matrix is a rectangular array of [real numbers](../types-of-numbers/) arranged in rows and columns. A matrix with $m$ rows and $n$ columns is said to have dimensions $m \times n$, and is called an $m \times n$ matrix. For example, a $3 \times 2$ matrix has 3 rows and 2 columns. Each number appearing in a matrix is called an element. Elements are identified by two subscript indices: the first indicates the row and the second the column. Thus $a_{2,3}$ denotes the element in the second row and third column. A matrix $A$ of dimensions $m \times n$ is written as follows:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\[6pt]
a_{21} & a_{22} & \cdots & a_{2n} \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

This is also written in compact form as $A = (a_{ij})$, where $a_{ij}$ denotes the element in the $i$-th row and $j$-th column, with $1 \leq i \leq m$ and $1 \leq j \leq n$.

> The set of all $m \times n$ matrices with real entries forms an abelian group under addition. When restricted to square matrices of order $n$, the additional structure of matrix multiplication makes $M_{n \times n}(\mathbb{R})$ a [ring](../rings/). The subset of invertible matrices of order $n$ forms a [group](../groups/) under multiplication, known as the general linear group $GL(n, \mathbb{R})$.

## Vectors and the zero matrix

A matrix consisting of a single row is called a row [vector](../vectors/), and a matrix consisting of a single column is called a column vector. The following are a row vector $A$ with 3 columns and a column vector $B$ with 3 rows:

$$
A = \begin{pmatrix} a_1 & a_2 & a_3 \end{pmatrix}
\qquad
B = \begin{pmatrix} b_1 \\[6pt] b_2 \\[6pt] b_3 \end{pmatrix}
$$

A matrix in which every element is equal to zero is called the zero matrix, denoted $O$. The zero matrix plays the role of the additive identity in matrix addition, as discussed below.

> Row and column vectors are matrices in the usual sense and obey all the same algebraic rules. They are treated as special cases here for clarity, but are studied more extensively in the context of [linear combinations](../linear-combinations/) and [vector spaces](../vector-spaces/).

## Square matrices and special types

A matrix is called square when its number of rows equals its number of columns, that is, when it has dimensions $n \times n$. The integer $n$ is called the order of the matrix. In a square matrix, the elements $a_{ij}$ for which $i = j$ form the main diagonal. The elements for which $i + j = n+1$ form the secondary diagonal:

$$
A = \begin{pmatrix}
\boldsymbol{a_{11}} & a_{12} & a_{13} \\[6pt]
a_{21} & \boldsymbol{a_{22}} & a_{23} \\[6pt]
a_{31} & a_{32} & \boldsymbol{a_{33}}
\end{pmatrix}
$$

A square matrix in which all elements outside the main diagonal are zero is called a diagonal matrix. The following is an example of a $3 \times 3$ diagonal matrix:

$$
D = \begin{pmatrix}
4 & 0 & 0 \\[6pt]
0 & 5 & 0 \\[6pt]
0 & 0 & 6
\end{pmatrix}
$$

A square matrix is called upper triangular if all elements below the main diagonal are zero, and lower triangular if all elements above the main diagonal are zero:

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

A square matrix $A$ is called symmetric if it equals its own transpose, that is, if $A = A^{\mathrm{T}}$. This means that $a_{ij} = a_{ji}$ for all $i$ and $j$: the element in row $i$ and column $j$ equals the element in row $j$ and column $i$. The following is a $3 \times 3$ symmetric matrix:

$$
S = \begin{pmatrix}
1 & 3 & -2 \\[6pt]
3 & 0 & 5 \\[6pt]
-2 & 5 & 4
\end{pmatrix}
$$

> Symmetric matrices arise naturally in many areas of mathematics, including quadratic forms, inner product spaces, and spectral theory. Every real symmetric matrix has real [eigenvalues](../eigenvalues-and-eigenvectors/) and an orthogonal basis of eigenvectors, a result known as the spectral theorem.

## Transpose

The transpose of a matrix $A$ of dimensions $m \times n$, denoted $A^{\mathrm{T}}$, is the matrix of dimensions $n \times m$ obtained by interchanging the rows and columns of $A$. Formally, the element in position $(i,j)$ of $A^{\mathrm{T}}$ is the element in position $(j,i)$ of $A$. For example:

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

The additive inverse of a matrix $A$, denoted $-A$, is the matrix obtained by negating every element of $A$: each entry $a_{ij}$ becomes $-a_{ij}$. The matrices $A$ and $-A$ have the same dimensions, and their sum is the zero matrix:

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

Two matrices can be added or subtracted only if they have the same dimensions. Given two $m \times n$ matrices $A = (a_{ij})$ and $B = (b_{ij})$, their sum $C = A + B$ is the $m \times n$ matrix defined by:

$$c_{ij} = a_{ij}+b_{ij}$$

Each element of $C$ is the sum of the corresponding elements of $A$ and $B$. The following example illustrates the computation for two $2 \times 3$ matrices:

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

The difference $A-B$ is defined as $A+(-B)$, that is, the sum of $A$ and the additive inverse of $B$. Matrix addition satisfies the following properties, for any matrices $A$, $B$, $C$ of dimensions $m \times n$:

+ Commutativity: $A+B = B+A$. The order in which two matrices are added does not affect the result.
+ Associativity: $(A+B)+C = A+(B+C)$. Sums of three or more matrices can be computed in any grouping.
+ Additive identity: $A+O = A$, where $O$ is the zero matrix of the same dimensions. Adding the zero matrix leaves $A$ unchanged.
+ Additive inverse: $A+(-A) = O$. Every matrix has a unique additive inverse.

## Scalar multiplication

Given a matrix $A = (a_{ij})$ of dimensions $m \times n$ and a real number $k$, the scalar multiple $kA$ is the $m \times n$ matrix whose element in position $(i,j)$ is $k \cdot a_{ij}$. Every entry of the matrix is multiplied by $k$. For example, with $k = 2$:

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

+ Associativity: $k(hA) = (kh)A$. Successive scalar multiplications can be combined into one.
+ Distributivity over matrix addition: $k(A+B) = kA+kB$. A scalar distributes over a sum of matrices.
+ Distributivity over scalar addition: $(k+h)A = kA+hA$. A sum of scalars distributes over a single matrix.

## Matrix multiplication

Matrix multiplication is defined under a compatibility condition: the product $AB$ is defined only when the number of columns of $A$ equals the number of rows of $B$. If $A$ has dimensions $m \times n$ and $B$ has dimensions $n \times p$, the product $C = AB$ is a matrix of dimensions $m \times p$, whose element in position $(i,j)$ is defined by:

$$c_{ij} = \sum_{k=1}^{n} a_{ik}\,b_{kj}$$

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

The result is a $2 \times 2$ matrix, consistent with the dimensions $m \times p = 2 \times 2$.

$$
C = AB = \begin{pmatrix}
16 & -19 \\[6pt]
-8 & 23
\end{pmatrix}
$$

> Matrix multiplication is not commutative in general: even when both $AB$ and $BA$ are defined, it is typically the case that $AB \neq BA$. This distinguishes matrix multiplication from multiplication of real numbers and is one of its most consequential properties.

- - -

The identity matrix of order $n$, denoted $I_n$, is the $n \times n$ square matrix with ones on the main diagonal and zeros elsewhere. It acts as the multiplicative identity: for any matrix $A$ of compatible dimensions,

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

+ Associativity: $(AB)C = A(BC)$. The order in which successive products are computed does not affect the result.
+ Left distributivity: $A(B+C) = AB+AC$. Multiplication distributes over addition from the left.
+ Right distributivity: $(B+C)A = BA+CA$. Multiplication distributes over addition from the right.
+ Non-commutativity: in general, $AB \neq BA$, even when both products are defined.

To every square matrix of order $n$ one associates a real number called the [determinant](../determinant/) of the matrix, denoted $\det(A)$. The determinant encodes fundamental information about the matrix, including whether it is invertible, as discussed in the entry on the [inverse matrix](../inverse-matrix/). The maximum number of linearly independent rows or columns is the [rank](../rank-of-a-matrix/), another invariant of fundamental importance. When the matrix is square and admits a basis of [eigenvectors](../eigenvalues-and-eigenvectors/), it can be reduced to a particularly simple form by [diagonalization](../matrix-diagonalization/).
