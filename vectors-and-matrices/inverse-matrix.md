---
title: Inverse Matrix
source: https://algebrica.org/inverse-matrix/
license: CC BY-NC 4.0
tags:
  - adjugate
  - cofactor-method
  - gauss-jordan
  - inverse-matrix
  - linear-algebra
  - matrices
---
## Definition

Given a square [matrix](../matrices/) $A$ of order $n,$ the inverse of $A,$ denoted $A^{-1},$ is the matrix such that:

$$A \cdot A^{-1} = A^{-1} \cdot A = I$$

where $I$ is the identity matrix of order $n.$ When such a matrix exists, it is unique. A square matrix that admits an inverse is called invertible or nonsingular. A matrix that does not admit an inverse is called singular.

The inverse matrix represents the linear transformation that reverses the effect of the original transformation. If $A$ maps a vector $\mathbf{x}$ to $\mathbf{b},$ that is $A\mathbf{x} = \mathbf{b},$ then $A^{-1}$ maps $\mathbf{b}$ back to $\mathbf{x}$:

$$A\mathbf{x} = \mathbf{b} \implies \mathbf{x} = A^{-1}\mathbf{b}$$

This is precisely the principle underlying the solution of [linear systems](../rouche-capelli-theorem/) via the inverse matrix.

A square matrix $A$ is invertible if and only if its [determinant](../determinant/) is nonzero:

$$A \text{ is invertible} \iff \det(A) \neq 0$$

> The condition $\det(A) \neq 0$ is both necessary and sufficient for invertibility. It is equivalent to requiring that the rows (or columns) of $A$ are linearly independent, and that the [rank](../rank-of-a-matrix/) of $A$ equals $n.$ The set of all invertible matrices of order $n$ forms a group under matrix multiplication, known as the general linear group $GL(n, \mathbb{R}),$ discussed in the entry on [groups](../groups/).

## Properties of the inverse

The inverse matrix satisfies the following properties, for square matrices $A$ and $B$ of order $n$:

+ $(A^{-1})^{-1} = A.$ The inverse of the inverse is the original matrix.
+ $(AB)^{-1} = B^{-1} A^{-1}.$ The inverse of a product reverses the order of the factors.
+ $(A^{\mathrm{T}})^{-1} = (A^{-1})^{\mathrm{T}}.$ The inverse of the transpose equals the transpose of the inverse.
+ $\det(A^{-1}) = \dfrac{1}{\det(A)}.$ The determinant of the inverse is the reciprocal of the determinant of $A.$

> The reversal of order in $(AB)^{-1} = B^{-1}A^{-1}$ is necessary for the same reason as in the transpose: matrix multiplication is not commutative, so inverting a product requires inverting each factor and reversing their order.

## Computing the inverse: the cofactor method

The inverse of a square matrix $A$ of order $n,$ when it exists, can be computed using the cofactor method. Given a square matrix $A = (a_{ij}),$ the minor $M_{ij}$ is the determinant of the $(n-1) \times (n-1)$ submatrix obtained by deleting the $i$-th row and $j$-th column of $A.$ The cofactor $C_{ij}$ is defined as:

$$C_{ij} = (-1)^{i+j} \cdot M_{ij}$$

The cofactor matrix $C$ is the matrix whose entry in position $(i,j)$ is the cofactor $C_{ij}.$ The transpose of the cofactor matrix, denoted $C^{\mathrm{T}},$ is called the adjugate of $A$ and written $\mathrm{adj}(A).$ The inverse is then given by:

$$A^{-1} = \frac{1}{\det(A)} C^{\mathrm{T}} = \frac{1}{\det(A)} \mathrm{adj}(A)$$

The computation proceeds as follows: calculate the cofactor $C_{ij}$ for every entry of $A,$ assemble the cofactor matrix $C,$ take its transpose to obtain $\mathrm{adj}(A),$ and divide every entry by $\det(A).$

## The inverse of a matrix of order 2

For a matrix of order 2 the cofactor method reduces to an explicit formula. Given:

$$A = \begin{pmatrix} a & b \\[6pt] c & d \end{pmatrix}$$

the adjugate is obtained by exchanging the two diagonal entries and reversing the sign of the two off-diagonal entries, and the determinant is $ad - bc.$ The inverse is therefore:

$$A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\[6pt] -c & a \end{pmatrix}$$

The formula holds whenever $ad - bc \neq 0.$ Consider the matrix:

$$A = \begin{pmatrix} 1 & 2 \\[6pt] 3 & 4 \end{pmatrix}$$

Its determinant is $ad - bc = (1)(4) - (2)(3) = -2,$ which is nonzero, so the matrix is invertible. Applying the formula gives:

$$
A^{-1} = \frac{1}{-2} \begin{pmatrix} 4 & -2 \\[6pt] -3 & 1 \end{pmatrix}
= \begin{pmatrix} -2 & 1 \\[6pt] \frac{3}{2} & -\frac{1}{2} \end{pmatrix}
$$

A direct multiplication confirms that $A \cdot A^{-1} = I.$

> The same formula follows from the Cayley-Hamilton theorem, which for a matrix of order 2 reads $A^2 - (a+d)A + (ad-bc)I = O.$ More generally, the theorem expresses the inverse of any invertible matrix as a polynomial in the matrix, a method developed in the entry on [matrix diagonalization](../matrix-diagonalization/).

## Example 1

Consider the following matrix:

$$
A = \begin{pmatrix}
3 & 0 & 0 \\[6pt]
2 & 1 & 0 \\[6pt]
-1 & 4 & 2
\end{pmatrix}
$$

This is a lower triangular matrix. Its determinant is the product of the diagonal entries, that is $\det(A) = 3 \cdot 1 \cdot 2 = 6.$ We now compute the nine cofactors of $A$ one by one.

$$
\begin{align}
C_{11} &= (+1) \cdot \det\begin{pmatrix} 1 & 0 \\[6pt] 4 & 2 \end{pmatrix} = 2 \\[6pt]
C_{12} &= (-1) \cdot \det\begin{pmatrix} 2 & 0 \\[6pt] -1 & 2 \end{pmatrix} = -4 \\[6pt]
C_{13} &= (+1) \cdot \det\begin{pmatrix} 2 & 1 \\[6pt] -1 & 4 \end{pmatrix} = 9 \\[6pt]
C_{21} &= (-1) \cdot \det\begin{pmatrix} 0 & 0 \\[6pt] 4 & 2 \end{pmatrix} = 0 \\[6pt]
C_{22} &= (+1) \cdot \det\begin{pmatrix} 3 & 0 \\[6pt] -1 & 2 \end{pmatrix} = 6 \\[6pt]
C_{23} &= (-1) \cdot \det\begin{pmatrix} 3 & 0 \\[6pt] -1 & 4 \end{pmatrix} = -12 \\[6pt]
C_{31} &= (+1) \cdot \det\begin{pmatrix} 0 & 0 \\[6pt] 1 & 0 \end{pmatrix} = 0 \\[6pt]
C_{32} &= (-1) \cdot \det\begin{pmatrix} 3 & 0 \\[6pt] 2 & 0 \end{pmatrix} = 0 \\[6pt]
C_{33} &= (+1) \cdot \det\begin{pmatrix} 3 & 0 \\[6pt] 2 & 1 \end{pmatrix} = 3
\end{align}
$$

The cofactor matrix $C$ is assembled from the nine cofactors computed above:

$$
C = \begin{pmatrix}
\phantom{-}2 & -4 & \phantom{-}9 \\[6pt]
\phantom{-}0 & \phantom{-}6 & -12 \\[6pt]
\phantom{-}0 & \phantom{-}0 & \phantom{-}3
\end{pmatrix}
$$

Taking the transpose of $C$ gives the adjugate of $A$:

$$
\mathrm{adj}(A) = C^{\mathrm{T}} = \begin{pmatrix}
\phantom{-}2 & \phantom{-}0 & \phantom{-}0 \\[6pt]
-4 & \phantom{-}6 & \phantom{-}0 \\[6pt]
\phantom{-}9 & -12 & \phantom{-}3
\end{pmatrix}
$$

Dividing by $\det(A) = 6$:

$$
A^{-1} = \frac{1}{6}
\begin{pmatrix}
\phantom{-}2 & \phantom{-}0 & \phantom{-}0 \\[6pt]
-4 & \phantom{-}6 & \phantom{-}0 \\[6pt]
\phantom{-}9 & -12 & \phantom{-}3
\end{pmatrix}
=
\begin{pmatrix}
\dfrac{1}{3} & 0 & 0 \\[10pt]
-\dfrac{2}{3} & 1 & 0 \\[10pt]
\dfrac{3}{2} & -2 & \dfrac{1}{2}
\end{pmatrix}
$$

> The cofactor method is exact but computationally expensive for large matrices, with complexity $O(n!)$ due to the determinant evaluations involved. In numerical practice, the inverse is typically computed via [Gaussian elimination](../solving-linear-systems-using-gaussian-elimination/) or LU decomposition, which achieve $O(n^3)$ complexity.

## Inversion by Gauss-Jordan elimination

The cofactor method is conceptually transparent, but its computational cost becomes prohibitive as the order of the matrix grows, since it inherits the factorial cost of evaluating determinants by Laplace expansion. In practice, the inverse of a matrix is more efficiently computed using Gauss-Jordan elimination, which reduces the cost to $O(n^3).$

The procedure begins by constructing the augmented matrix obtained by placing the identity matrix $I$ of the same order to the right of $A$:

$$[\ A \mid I\ ]$$

Elementary row operations are then applied to this augmented matrix, with the goal of transforming the left-hand block into the identity. The operations admitted are the same as those used in the solution of linear systems: swapping two rows, multiplying a row by a nonzero scalar, and adding to a row a scalar multiple of another row. Each operation is applied simultaneously to both blocks of the augmented matrix.

When the procedure terminates and the left-hand block has been reduced to $I,$ the right-hand block contains the inverse:

$$[\ A \mid I\ ] \ \longrightarrow\ [\ I \mid A^{-1}\ ]$$

The same procedure provides an immediate test for invertibility. If during the reduction a row of the left-hand block becomes entirely zero, the matrix $A$ is singular and the inverse does not exist.

> The Gauss-Jordan method is the method of choice whenever the order of the matrix exceeds three. The cofactor method retains its value as a definition and as a tool for theoretical reasoning, but for explicit computation Gauss-Jordan is consistently preferable.

## Example 2

Consider for example the following matrix:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\[6pt]
0 & 1 & 4 \\[6pt]
5 & 6 & 0
\end{pmatrix}
$$

We construct the augmented matrix by placing the identity to the right of $A$:

$$
[\ A \mid I\ ] =
\left(
\begin{array}{ccc|ccc}
1 & 2 & 3 & 1 & 0 & 0 \\[6pt]
0 & 1 & 4 & 0 & 1 & 0 \\[6pt]
5 & 6 & 0 & 0 & 0 & 1
\end{array}
\right)
$$

We begin by eliminating the entry in the third row of the first column. Replacing the third row with itself minus five times the first row gives:

$$
\left(
\begin{array}{ccc|ccc}
1 & 2 & 3 & 1 & 0 & 0 \\[6pt]
0 & 1 & 4 & 0 & 1 & 0 \\[6pt]
0 & -4 & -15 & -5 & 0 & 1
\end{array}
\right)
$$

We now eliminate the entry in the third row of the second column. Replacing the third row with itself plus four times the second row gives:

$$
\left(
\begin{array}{ccc|ccc}
1 & 2 & 3 & 1 & 0 & 0 \\[6pt]
0 & 1 & 4 & 0 & 1 & 0 \\[6pt]
0 & 0 & 1 & -5 & 4 & 1
\end{array}
\right)
$$

The left-hand block is now in upper triangular form with ones on the main diagonal. We continue the reduction upwards, eliminating the entries above the diagonal. Replacing the second row with itself minus four times the third row, and the first row with itself minus three times the third row, we obtain:

$$
\left(
\begin{array}{ccc|ccc}
1 & 2 & 0 & 16 & -12 & -3 \\[6pt]
0 & 1 & 0 & 20 & -15 & -4 \\[6pt]
0 & 0 & 1 & -5 & 4 & 1
\end{array}
\right)
$$

Finally, replacing the first row with itself minus two times the second row gives the identity on the left and the inverse on the right:

$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & -24 & 18 & 5 \\[6pt]
0 & 1 & 0 & 20 & -15 & -4 \\[6pt]
0 & 0 & 1 & -5 & 4 & 1
\end{array}
\right)
$$

The inverse of $A$ is therefore:

$$
A^{-1} = \begin{pmatrix}
-24 & 18 & 5 \\[6pt]
20 & -15 & -4 \\[6pt]
-5 & 4 & 1
\end{pmatrix}
$$

A direct check confirms the result, since $A \cdot A^{-1} = I.$ The inverse appears in the [diagonalization](../matrix-diagonalization/) of a matrix, where the change-of-basis matrix $P$ must itself be invertible.
