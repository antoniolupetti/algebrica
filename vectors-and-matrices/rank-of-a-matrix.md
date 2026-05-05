# Rank of a Matrix

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/rank-of-a-matrix/

## Definition

The rank of a matrix \\( A \\), denoted \\( r(A) \\) or \\( \\mathrm{rank}(A) \\), is the maximum number of linearly independent rows (or equivalently, columns) of \\( A \\). For an \\( m \\times n \\) matrix \\( A \\), the rank satisfies:

\\[
0 \\leq r(A) \\leq \\min(m,n)
\\]

The rank of a matrix \\( A \\) equals the dimension of the image of the associated linear transformation \\( T_A : \\mathbb{R}^n \\to \\mathbb{R}^m \\), defined by \\( T_A(\\mathbf{x}) = A\\mathbf{x} \\). The complementary quantity \\( n - r(A) \\) is the dimension of the kernel of \\( T_A \\), the subspace of [vectors](../vectors/) mapped to zero. These two quantities are related by the rank-nullity theorem: for any \\( A \\in M_{m,n}(\\mathbb{R}) \\) we have:

\\[
\\mathrm{rank}(A) + \\mathrm{nullity}(A) = n
\\]

> The rank is one of the most fundamental invariants of a matrix. It determines the solvability of [systems of linear equations](../systems-of-linear-equations/) via the Rouché-Capelli theorem, and it coincides with the condition \\( r(A) = n \\) for a square matrix to be [invertible](../inverse-matrix/)

- - -
## Submatrices and minors

A submatrix of a matrix \\( A \\in M_{m,n}(\\mathbb{R}) \\) is any matrix obtained by selecting \\( k \\) rows and \\( h \\) columns from \\( A \\), preserving the original order of elements, with \\( k \\leq m \\) and \\( h \\leq n \\). For example, selecting rows 1 and 3 and columns 1, 2, and 4 from a \\( 3 \\times 4 \\) matrix \\( A \\) yields the \\( 2 \\times 3 \\) submatrix:

\\[
B = \\begin{pmatrix}
a_{11} & a_{12} & a_{14} \\\\[6pt]
a_{31} & a_{32} & a_{34}
\\end{pmatrix}
\\]

A minor of order \\( p \\) of a matrix \\( A \\) is the [determinant](../determinant/) of a square submatrix of size \\( p \\times p \\) extracted from \\( A \\). Since the determinant is defined only for square matrices, only square submatrices give rise to minors.

- - -
## Definition via minors

The rank of a matrix \\( A \\) is the largest integer \\( r \\) such that at least one minor of order \\( r \\) is nonzero. Equivalently, all minors of order \\( r+1 \\) are zero.

The following example computes the rank of a \\( 3 \\times 4 \\) matrix. Consider:

\\[
A = \\begin{pmatrix}
1 & 2 & 3 & 4 \\\\[6pt]
2 & 4 & 6 & 8 \\\\[6pt]
1 & 0 & 1 & 2
\\end{pmatrix}
\\]

The second row is exactly twice the first, so any \\( 3 \\times 3 \\) minor involving both rows will have two proportional rows and therefore vanish. One can verify that all minors of order 3 are zero. However, the \\( 2 \\times 2 \\) submatrix extracted from rows 1 and 3 and columns 1 and 2 gives:

\\[
\\det\\begin{pmatrix} 1 & 2 \\\\[6pt] 1 & 0 \\end{pmatrix} = 0-2 = -2 \\neq 0
\\]

Since there exists a nonzero minor of order 2 and all minors of order 3 are zero, the rank of \\( A \\) is:

\\[
r(A) = 2
\\]

- - -
## Computing the rank via Gaussian elimination

For matrices of large order, computing all minors is impractical. The standard computational method is [Gaussian elimination](../solving-linear-systems-using-gaussian-elimination/): reduce \\( A \\) to row echelon form by applying elementary row operations, which do not change the rank. The rank equals the number of nonzero rows in the reduced matrix. Consider the matrix from the previous example:

\\[
A = \\begin{pmatrix}
1 & 2 & 3 & 4 \\\\[6pt]
2 & 4 & 6 & 8 \\\\[6pt]
1 & 0 & 1 & 2
\\end{pmatrix}
\\]

Subtracting twice the first row from the second, and the first row from the third:

\\[
\\begin{pmatrix}
1 & 2 & 3 & 4 \\\\[6pt]
0 & 0 & 0 & 0 \\\\[6pt]
0 & -2 & -2 & -2
\\end{pmatrix}
\\]

Swapping the second and third rows:

\\[
\\begin{pmatrix}
1 & 2 & 3 & 4 \\\\[6pt]
0 & -2 & -2 & -2 \\\\[6pt]
0 & 0 & 0 & 0
\\end{pmatrix}
\\]

The row echelon form has 2 nonzero rows, confirming \\( r(A) = 2 \\).

- - -
## Properties of the rank

- \\( r(A) = 0 \\) if and only if \\( A \\) is the zero matrix.
- For a square matrix \\( A \\) of order \\( n \\), \\( r(A) = n \\) if and only if \\( A \\) is nonsingular, that is \\( \\det(A) \\neq 0 \\).
- \\( r(A) = r(A^{\\mathrm{T}}) \\). The rank is unchanged by transposition.
- \\( r(A+B) \\leq r(A) + r(B) \\).
- \\( r(AB) \\leq \\min(r(A),\\, r(B)) \\).

> The rank appears in the Rouché-Capelli theorem, which characterizes the compatibility of a system of linear equations \\( A\\mathbf{x} = \\mathbf{b} \\): the system is consistent if and only if \\( r(A) = r(A|\\mathbf{b}) \\), where \\( A|\\mathbf{b} \\) denotes the augmented matrix. When consistent, the solution space has dimension \\( n - r(A) \\).