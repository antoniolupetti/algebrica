---
title: Rank of a Matrix
source: https://algebrica.org/rank-of-a-matrix/
license: CC BY-NC 4.0
tags:
  - gaussian-elimination
  - linear-algebra
  - matrices
  - rank
  - rank-nullity-theorem
---
## Definition

The rank of a matrix $A$, denoted $r(A)$ or $\mathrm{rank}(A)$, is the maximum number of linearly independent rows (or equivalently, columns) of $A$. For an $m \times n$ matrix $A$, the rank satisfies:

$$0 \leq r(A) \leq \min(m,n)$$

The rank of a matrix $A$ equals the dimension of the image of the associated linear transformation $T_A : \mathbb{R}^n \to \mathbb{R}^m$, defined by $T_A(\mathbf{x}) = A\mathbf{x}$, regarded as a map between the [vector spaces](../vector-spaces/) $\mathbb{R}^n$ and $\mathbb{R}^m$. The complementary quantity $n - r(A)$ is the dimension of the kernel of $T_A$, the subspace of [vectors](../vectors/) mapped to zero. These two quantities are related by the rank-nullity theorem. For any $A \in M_{m,n}(\mathbb{R})$ we have:

$$\mathrm{rank}(A) + \mathrm{nullity}(A) = n$$

> The rank determines the solvability of a linear system through the [Rouché-Capelli theorem](../rouche-capelli-theorem/), and the condition $r(A) = n$ characterizes when a square matrix is [invertible](../inverse-matrix/).

## Submatrices and minors

A submatrix of a matrix $A \in M_{m,n}(\mathbb{R})$ is any matrix obtained by selecting $k$ rows and $h$ columns from $A$, preserving the original order of elements, with $k \leq m$ and $h \leq n$. For example, selecting rows 1 and 3 and columns 1, 2, and 4 from a $3 \times 4$ matrix $A$ yields the $2 \times 3$ submatrix:

$$
B = \begin{pmatrix}
a_{11} & a_{12} & a_{14} \\[6pt]
a_{31} & a_{32} & a_{34}
\end{pmatrix}
$$

A minor of order $p$ of a matrix $A$ is the [determinant](../determinant/) of a square submatrix of size $p \times p$ extracted from $A$. Since the determinant is defined only for square matrices, only square submatrices have minors.

## Definition via minors

The rank of a matrix $A$ is the largest integer $r$ such that at least one minor of order $r$ is nonzero. Equivalently, all minors of order $r+1$ are zero.

The following example computes the rank of a $3 \times 4$ matrix. Consider:

$$
A = \begin{pmatrix}
1 & 2 & 3 & 4 \\[6pt]
2 & 4 & 6 & 8 \\[6pt]
1 & 0 & 1 & 2
\end{pmatrix}
$$

The second row is exactly twice the first. Every $3 \times 3$ minor uses all three rows, so it has two proportional rows and vanishes. However, the $2 \times 2$ submatrix extracted from rows 1 and 3 and columns 1 and 2 gives:

$$\det\begin{pmatrix} 1 & 2 \\[6pt] 1 & 0 \end{pmatrix} = 0-2 = -2 \neq 0$$

Since a minor of order 2 is nonzero and all minors of order 3 vanish, the rank of $A$ is:

$$r(A) = 2$$

## Computing the rank via Gaussian elimination

For matrices of large order, computing all minors is impractical. The standard computational method is [Gaussian elimination](../gaussian-elimination/), which reduces $A$ to row echelon form by applying elementary row operations that do not change the rank. The rank equals the number of nonzero rows in the reduced matrix. Consider the matrix from the previous example:

$$
A = \begin{pmatrix}
1 & 2 & 3 & 4 \\[6pt]
2 & 4 & 6 & 8 \\[6pt]
1 & 0 & 1 & 2
\end{pmatrix}
$$

Subtracting twice the first row from the second and the first row from the third gives:

$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\[6pt]
0 & 0 & 0 & 0 \\[6pt]
0 & -2 & -2 & -2
\end{pmatrix}
$$

Swapping the second and third rows gives:

$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\[6pt]
0 & -2 & -2 & -2 \\[6pt]
0 & 0 & 0 & 0
\end{pmatrix}
$$

The row echelon form has two nonzero rows, so $r(A) = 2$.

## Properties of the rank

The rank satisfies the following properties.

+ $r(A) = 0$ if and only if $A$ is the zero matrix.
+ For a square matrix $A$ of order $n$, $r(A) = n$ if and only if $A$ is nonsingular, that is $\det(A) \neq 0$.
+ $r(A) = r(A^{\mathrm{T}})$. The rank is unchanged by transposition.
+ $r(A+B) \leq r(A) + r(B)$.
+ $r(AB) \leq \min(r(A), r(B))$.

> The rank appears in the [Rouché-Capelli theorem](../rouche-capelli-theorem/), which characterizes the compatibility of a system of linear equations $A\mathbf{x} = \mathbf{b}$. The system is consistent if and only if $r(A) = r(A|\mathbf{b})$, where $A|\mathbf{b}$ denotes the augmented matrix. When consistent, the solution space has dimension $n - r(A)$.
