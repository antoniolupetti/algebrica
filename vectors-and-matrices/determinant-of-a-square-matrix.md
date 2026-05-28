---
title: Determinant of a Square Matrix
source: https://algebrica.org/determinant/
license: CC BY-NC 4.0
tags:
  - determinant
  - laplace-expansion
  - linear-algebra
  - matrices
  - sarrus-rule
---
## Definition

To every square [matrix](../matrices/) of order $n$ one can associate a [real number](../types-of-numbers/) called the determinant of the matrix, denoted $\det(A)$ or $|A|$. The determinant is a scalar-valued function that encodes both algebraic and geometric properties of the associated linear transformation:

$$\det : M_n(\mathbb{R}) \to \mathbb{R}$$

It determines whether the matrix is invertible and measures the factor by which the transformation scales volumes. It appears in the explicit solution of [linear systems](../rouche-capelli-theorem/) via Cramer's rule, and plays a central role in the study of [eigenvalues](../eigenvalues-and-eigenvectors/) and linear transformations.

The determinant of a matrix of order 1 is the element itself:

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

The determinant of a square matrix of order $n \geq 3$ can be computed recursively using the cofactor expansion, also known as Laplace expansion. Given a square matrix $A = (a_{ij})$ of order $n$, the minor $M_{ij}$ is the determinant of the $(n-1) \times (n-1)$ submatrix obtained by deleting the $i$-th row and $j$-th column of $A$. The cofactor $C_{ij}$ is defined as:

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

For $a_{11} = 2$, the minor is the determinant of the submatrix obtained by deleting row 1 and column 1:

$$C_{11} = (-1)^{1+1} \cdot \det\begin{pmatrix} -2 & 0 \\[6pt] 4 & 1 \end{pmatrix} = (+1) \cdot (-2-0) = -2$$

The contribution is $a_{11} \cdot C_{11} = 2 \cdot (-2) = -4$.

- - -

For $a_{12} = 0$, the minor is:

$$C_{12} = (-1)^{1+2} \cdot \det\begin{pmatrix} 3 & 0 \\[6pt] 1 & 1 \end{pmatrix} = (-1) \cdot (3-0) = -3$$

The contribution is $a_{12} \cdot C_{12} = 0 \cdot (-3) = 0$.

- - -

For $a_{13} = -1$, the minor is:

$$C_{13} = (-1)^{1+3} \cdot \det\begin{pmatrix} 3 & -2 \\[6pt] 1 & 4 \end{pmatrix} = (+1) \cdot (12+2) = 14$$

The contribution is $a_{13} \cdot C_{13} = (-1) \cdot 14 = -14$.

- - -

Summing the three contributions we obtain:

$$\det(A) = -4 + 0 + (-14) = -18$$

> The computational cost of Laplace expansion grows factorially with the order of the matrix, resulting in a time complexity of $O(n!)$. For this reason, the method is impractical for large matrices in numerical applications, where more efficient algorithms such as LU decomposition are preferred.

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

## Properties of the determinant

The following are the fundamental properties of the determinant.

+ If $A$ has an entire row or column of zeros, then $\det(A) = 0$.
+ If two rows or two columns of $A$ are proportional, then $\det(A) = 0$. More generally, if one row or column is a [linear combination](../linear-combinations/) of others, then $\det(A) = 0$.
+ If all elements of a row or column are multiplied by a scalar $k$, the determinant is multiplied by $k$. Equivalently, a scalar factor can be extracted from any row or column: $\det(kA) = k^n \det(A)$ for a matrix of order $n$.
+ The determinant of a product equals the product of the determinants: $\det(AB) = \det(A) \cdot \det(B)$.
+ The determinant of the transpose equals the determinant of the original matrix: $\det(A^{\mathrm{T}}) = \det(A)$.
+ A square matrix $A$ is invertible if and only if $\det(A) \neq 0$. When $\det(A) = 0$, the matrix is called singular, as discussed in the entry on the [inverse matrix](../inverse-matrix/). The same condition characterises a [rank](../rank-of-a-matrix/) equal to $n$ for a square matrix of order $n$.

> The identity $\det(AB) = \det(A) \cdot \det(B)$, together with $\det(I) = 1$, expresses the determinant as a [group](../groups/) homomorphism from the general linear group $GL_n(\mathbb{R})$ into the multiplicative group of the [field](../fields/) $\mathbb{R}$. The kernel of this homomorphism is the special linear group $SL_n(\mathbb{R})$, formed by the matrices of determinant one.

> The same scalar-valued criterion is used by the [Rouché-Capelli theorem](../rouche-capelli-theorem/) on linear systems: a square system $A\mathbf{x} = \mathbf{b}$ admits a unique solution exactly when $\det(A) \neq 0$, which is also the condition for the explicit closed-form solution given by Cramer's rule.
