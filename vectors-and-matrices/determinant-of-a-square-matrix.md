---
title: Determinant of a Square Matrix
source: https://algebrica.org/determinant/
license: CC BY-NC 4.0
tags:
  - binet-theorem
  - determinant
  - gaussian-elimination
  - laplace-expansion
  - linear-algebra
  - matrices
  - sarrus-rule
  - vandermonde-determinant
---
## Definition

To every square [matrix](../matrices/) of order $n$ one can associate a [real number](../types-of-numbers/) called the determinant of the matrix, denoted $\det(A)$ or $|A|.$ The determinant is a scalar-valued function that encodes both algebraic and geometric properties of the associated linear transformation:

$$\det : M_n(\mathbb{R}) \to \mathbb{R}$$

It determines whether the matrix is invertible and measures the factor by which the transformation scales volumes. It appears in the explicit solution of [linear systems](../rouche-capelli-theorem/) via [Cramer's rule](../cramers-rule/), and in the study of [eigenvalues](../eigenvalues-and-eigenvectors/) and linear transformations. The determinant of a matrix of order 1 is the element itself:

$$A = \begin{pmatrix} a_{11} \end{pmatrix} \implies \det(A) = a_{11}$$

For a square matrix of order 2, the determinant is the difference between the product of the elements on the main diagonal and the product of the elements on the secondary diagonal:

$$
A = \begin{pmatrix} a_{11} & a_{12} \\[6pt] a_{21} & a_{22} \end{pmatrix}
\implies
\det(A) = a_{11} \cdot a_{22} - a_{21} \cdot a_{12}
$$

For example:

$$
A = \begin{pmatrix} 3 & 2 \\[6pt] 1 & 4 \end{pmatrix}
\implies
\det(A) = 3 \cdot 4 - 1 \cdot 2 = 10
$$

## Diagonal and triangular matrices

For a diagonal matrix, that is a square matrix in which all off-diagonal elements are zero, the determinant equals the product of the elements on the main diagonal:

$$
A = \begin{pmatrix}
a_{11} & 0 & \cdots & 0 \\[6pt]
0 & a_{22} & \cdots & 0 \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
0 & 0 & \cdots & a_{nn}
\end{pmatrix}
\implies
\det(A) = a_{11} \cdot a_{22} \cdot \ldots \cdot a_{nn}
$$

The same result holds for upper and lower triangular matrices. In both cases, the determinant is the product of the diagonal entries, since all the additional terms in the expansion vanish.

## Laplace expansion

The determinant of a square matrix of order $n \geq 3$ can be computed recursively using the cofactor expansion, also known as Laplace expansion. Given a square matrix $A = (a_{ij})$ of order $n,$ the minor $M_{ij}$ is the determinant of the $(n-1) \times (n-1)$ submatrix obtained by deleting the $i$-th row and $j$-th column of $A.$ The cofactor $C_{ij}$ is defined as:

$$C_{ij} = (-1)^{i+j} \cdot M_{ij}$$

The sign factor $(-1)^{i+j}$ is positive when $i+j$ is even and negative when $i+j$ is odd. The determinant of $A$ is then obtained by expanding along any row $i$:

$$\det(A) = \sum_{k=1}^{n} a_{ik} \cdot C_{ik} = \sum_{k=1}^{n} a_{ik} \cdot (-1)^{i+k} \cdot M_{ik}$$

The same result is obtained by expanding along any column $j$:

$$\det(A) = \sum_{k=1}^{n} a_{kj} \cdot C_{kj}$$

The following example illustrates the computation for a matrix of order 3. Consider:

$$
A = \begin{pmatrix}
2 & 0 & -1 \\[6pt]
3 & -2 & 0 \\[6pt]
1 & 4 & 1
\end{pmatrix}
$$

Expanding along the first row, we compute the cofactor contribution of each element.

- - -

For $a_{11} = 2,$ the minor is the determinant of the submatrix obtained by deleting row 1 and column 1:

$$C_{11} = (-1)^{1+1} \cdot \det\begin{pmatrix} -2 & 0 \\[6pt] 4 & 1 \end{pmatrix} = (+1) \cdot (-2-0) = -2$$

The contribution is $a_{11} \cdot C_{11} = 2 \cdot (-2) = -4.$

- - -

For $a_{12} = 0,$ the minor is:

$$C_{12} = (-1)^{1+2} \cdot \det\begin{pmatrix} 3 & 0 \\[6pt] 1 & 1 \end{pmatrix} = (-1) \cdot (3-0) = -3$$

The contribution is $a_{12} \cdot C_{12} = 0 \cdot (-3) = 0.$

- - -

For $a_{13} = -1,$ the minor is:

$$C_{13} = (-1)^{1+3} \cdot \det\begin{pmatrix} 3 & -2 \\[6pt] 1 & 4 \end{pmatrix} = (+1) \cdot (12+2) = 14$$

The contribution is $a_{13} \cdot C_{13} = (-1) \cdot 14 = -14.$

- - -

Summing the three contributions we obtain:

$$\det(A) = -4 + 0 + (-14) = -18$$

> The computational cost of Laplace expansion grows factorially with the order of the matrix, resulting in a time complexity of $O(n!).$ For this reason, the method is impractical for large matrices in numerical applications, where more efficient algorithms such as LU decomposition are preferred.

## Sarrus' rule

For matrices of order 3, the determinant can be computed using Sarrus' rule, a direct mnemonic method equivalent to the Laplace expansion. Given the matrix:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\[6pt]
a_{21} & a_{22} & a_{23} \\[6pt]
a_{31} & a_{32} & a_{33}
\end{pmatrix}
$$

the determinant is:

$$
\begin{align}
\det(A) &= a_{11} a_{22} a_{33} + a_{12} a_{23} a_{31} + a_{13} a_{21} a_{32} \\[6pt]
&\quad - a_{13} a_{22} a_{31} - a_{11} a_{23} a_{32} - a_{12} a_{21} a_{33}
\end{align}
$$

The three positive terms correspond to the products along the three main diagonals (top-left to bottom-right), and the three negative terms correspond to the products along the three secondary diagonals (top-right to bottom-left). A convenient way to visualize this is to append the first two columns of $A$ to its right:

$$
\begin{pmatrix}
a_{11} & a_{12} & a_{13} & \color{gray}{a_{11}} & \color{gray}{a_{12}} \\[6pt]
a_{21} & a_{22} & a_{23} & \color{gray}{a_{21}} & \color{gray}{a_{22}} \\[6pt]
a_{31} & a_{32} & a_{33} & \color{gray}{a_{31}} & \color{gray}{a_{32}}
\end{pmatrix}
$$

The following example applies Sarrus' rule to a concrete matrix. Consider:

$$
A = \begin{pmatrix}
1 & -2 & 3 \\[6pt]
0 & 4 & -1 \\[6pt]
2 & 1 & 0
\end{pmatrix}
$$

We obtain:

$$
\begin{align}
\det(A) &= (1)(4)(0) + (-2)(-1)(2) + (3)(0)(1) \\[6pt]
&\quad - (3)(4)(2) - (1)(-1)(1) - (-2)(0)(0) \\[6pt]
&= 0 + 4 + 0 - 24 + 1 + 0 \\[6pt]
&= -19
\end{align}
$$

> Sarrus' rule applies exclusively to matrices of order 3. It does not generalize to higher orders.

## Determinant and elementary operations

The determinant behaves in a controlled way under the three elementary operations on rows, and the same statements hold for the corresponding column operations, since $\det(A^{\mathrm{T}}) = \det(A).$ Let $A'$ be the matrix obtained from $A$ by a single elementary operation.

+ Adding to one row a multiple of another row leaves the determinant unchanged: $\det(A') = \det(A).$
+ Multiplying one row by a scalar $\alpha$ multiplies the determinant by the same scalar: $\det(A') = \alpha \det(A).$
+ Exchanging two distinct rows reverses the sign of the determinant: $\det(A') = -\det(A).$

The first rule explains why a matrix with two proportional rows has determinant zero, since adding a suitable multiple of one row to the other produces a row of zeros. The third rule shows that a single exchange of rows is enough to reverse the sign, while an even number of exchanges restores it.

## Computing the determinant by row reduction

The behavior under elementary operations gives a method for computing a determinant that avoids the factorial cost of Laplace expansion. One reduces the matrix to triangular form by elementary operations, records how each operation changes the determinant, and reads the determinant of the triangular matrix as the product of its diagonal entries.

Consider the matrix:

$$
A = \begin{pmatrix}
0 & 2 & 1 \\[6pt]
1 & 1 & 1 \\[6pt]
2 & 0 & 3
\end{pmatrix}
$$

The entry in position $(1,1)$ is zero, so we exchange the first two rows. A single exchange reverses the sign of the determinant:

$$
\begin{pmatrix}
1 & 1 & 1 \\[6pt]
0 & 2 & 1 \\[6pt]
2 & 0 & 3
\end{pmatrix}
$$

We clear the first column below the diagonal by subtracting twice the first row from the third. Adding a multiple of one row to another leaves the determinant unchanged:

$$
\begin{pmatrix}
1 & 1 & 1 \\[6pt]
0 & 2 & 1 \\[6pt]
0 & -2 & 1
\end{pmatrix}
$$

Adding the second row to the third clears the remaining entry below the diagonal, again without changing the determinant:

$$
\begin{pmatrix}
1 & 1 & 1 \\[6pt]
0 & 2 & 1 \\[6pt]
0 & 0 & 2
\end{pmatrix}
$$

The matrix is upper triangular, and its determinant is the product of the diagonal entries, $1 \cdot 2 \cdot 2 = 4.$ One row exchange was used along the way, so the determinant of the original matrix is the opposite of this value:

$$\det(A) = -4$$

> Reducing a matrix of order $n$ to triangular form uses about $2n^3/3$ arithmetic operations, against the roughly $n \cdot n!$ of a full Laplace expansion. Beyond order three or four, row reduction is the method of choice.

## Properties of the determinant

The following are the fundamental properties of the determinant.

+ If $A$ has an entire row or column of zeros, then $\det(A) = 0.$
+ If two rows or two columns of $A$ are proportional, then $\det(A) = 0.$ More generally, if one row or column is a [linear combination](../linear-combinations/) of others, then $\det(A) = 0.$
+ If all elements of a row or column are multiplied by a scalar $k,$ the determinant is multiplied by $k.$ Equivalently, a scalar factor can be extracted from any row or column: $\det(kA) = k^n \det(A)$ for a matrix of order $n.$
+ The determinant of a product equals the product of the determinants, a result known as Binet's theorem: $\det(AB) = \det(A) \cdot \det(B).$
+ The determinant of the transpose equals the determinant of the original matrix: $\det(A^{\mathrm{T}}) = \det(A).$
+ A square matrix $A$ is invertible if and only if $\det(A) \neq 0.$ When $\det(A) = 0,$ the matrix is called singular, as discussed in the entry on the [inverse matrix](../inverse-matrix/). The same condition characterises a [rank](../rank-of-a-matrix/) equal to $n$ for a square matrix of order $n.$

> Binet's theorem concerns products, not sums. In general $\det(A + B) \neq \det(A) + \det(B).$ For instance, with $A = I_2$ and $B = -I_2,$ both determinants equal $1,$ while $A + B = O$ has determinant $0.$

> The identity $\det(AB) = \det(A) \cdot \det(B),$ together with $\det(I) = 1,$ expresses the determinant as a [group](../groups/) homomorphism from the general linear group $GL_n(\mathbb{R})$ into the multiplicative group of the [field](../fields/) $\mathbb{R}.$ The kernel of this homomorphism is the special linear group $SL_n(\mathbb{R}),$ formed by the matrices of determinant one.

> The same scalar-valued criterion is used by the [Rouché-Capelli theorem](../rouche-capelli-theorem/) on linear systems: a square system $A\mathbf{x} = \mathbf{b}$ admits a unique solution exactly when $\det(A) \neq 0,$ which is also the condition for the explicit closed-form solution given by Cramer's rule.

## Cramer's rule

When the coefficient matrix of a square [linear system](../rouche-capelli-theorem/) $A\mathbf{x} = \mathbf{b}$ is invertible, the determinant gives each unknown in closed form as a ratio of determinants, $x_j = \det(A_j)/\det(A),$ where $A_j$ is obtained from $A$ by replacing its $j$-th column with $\mathbf{b}.$ This method is treated in the dedicated entry on [Cramer's rule](../cramers-rule/).

## The Vandermonde determinant

A recurring family of determinants appears in polynomial interpolation. Given $n$ scalars $x_1, x_2, \ldots, x_n,$ the Vandermonde matrix has $1, x_i, x_i^2, \ldots, x_i^{n-1}$ as its $i$-th row:

$$
V = \begin{pmatrix}
1 & x_1 & x_1^2 & \cdots & x_1^{n-1} \\[6pt]
1 & x_2 & x_2^2 & \cdots & x_2^{n-1} \\[6pt]
\vdots & \vdots & \vdots & \ddots & \vdots \\[6pt]
1 & x_n & x_n^2 & \cdots & x_n^{n-1}
\end{pmatrix}
$$

Its determinant factors as the product of all the differences $x_i - x_j$ with $i > j$:

$$\det(V) = \prod_{i > j} (x_i - x_j)$$

The product is zero exactly when two of the $x_i$ coincide, so the matrix is invertible if and only if the values $x_1, x_2, \ldots, x_n$ are distinct. This is the reason a polynomial of degree at most $n-1$ is determined by its values at $n$ distinct points, since its coefficients solve a linear system with a Vandermonde coefficient matrix.

For the three values $x_1 = 1,$ $x_2 = 2,$ $x_3 = 4,$ the matrix and its determinant are:

$$
V = \begin{pmatrix}
1 & 1 & 1 \\[6pt]
1 & 2 & 4 \\[6pt]
1 & 4 & 16
\end{pmatrix}
\qquad
\det(V) = (2-1)(4-1)(4-2) = 6
$$

A direct expansion of the determinant returns the same value.
