# Eigenvalues and Eigenvectors

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/eigenvalues-and-eigenvectors/

## Definition

A linear transformation, represented by a square [matrix](../matrices/) \\(A\\), acts on vectors by moving them in space. It can stretch, compress, rotate, or reflect them, and in general the image of a [vector](../vectors/) points in a different direction from the original. Among all vectors however there are those for which the action of \\(A\\) is particularly simple. The transformation scales them by a constant factor, leaving their direction unchanged. Such vectors are called eigenvectors of \\(A\\), and the corresponding scaling factors are called eigenvalues.

> Eigenvectors reveal the intrinsic geometry of a linear transformation, and the collection of eigenvalues encodes information about the matrix that is invariant under a wide class of coordinate changes.

- - -

Let \\(A\\) be a square [matrix](../matrices/) of order \\(n\\) with entries in \\(\mathbb{R}\\) or \\(\mathbb{C}\\). A non-zero [vector](../vectors/) \\(\mathbf{v}\\) is called an eigenvector of \\(A\\) if there exists a scalar \\(\lambda\\) such that the following equation holds:

\\[
A\mathbf{v} = \lambda\mathbf{v}
\\]

The scalar \\(\lambda\\) is called the eigenvalue of \\(A\\) associated with \\(\mathbf{v}\\). The condition requires that \\(A\\) maps \\(\mathbf{v}\\) to a scalar multiple of itself: the vector \\(\mathbf{v}\\) may be stretched or compressed, and its orientation may be reversed if \\(\lambda\\) is negative, but it remains on the same line through the origin. Eigenvectors are the invariant directions of the transformation and eigenvalues are the scaling factors along those directions.

> The zero vector is excluded by convention. The equation \\(A\mathbf{0} = \lambda\mathbf{0}\\) is satisfied for every \\(\lambda\\) and carries no information about the matrix.

- - -

The following diagram illustrates this idea for the square matrix:

\\[
A = \begin{pmatrix} 2 & 1 \\\\ 1 & 2 \end{pmatrix}
\\]

The [unit circle](../unit-circle/) is mapped to an [ellipse](../ellipse/): most vectors change direction under the transformation. The two eigenvectors \\(\mathbf{v}\_1\\) and \\(\mathbf{v}\_2\\) are the exception. They remain on the same line through the origin, scaled by \\(\lambda_1 = 3\\) and \\(\lambda_2 = 1\\) respectively.

- - -
## The characteristic equation

Rewriting the eigenvalue equation as \\((A - \lambda I)\mathbf{v} = \mathbf{0}\\), where \\(I\\) is the identity matrix of order \\(n\\), it is clear that a non-zero solution \\(\mathbf{v}\\) exists precisely when the matrix \\(A - \lambda I\\) is singular. The condition for singularity is that its determinant vanishes. The equation

\\[
\det(A - \lambda I) = 0
\\]

is called the characteristic equation of \\(A\\). Expanding the determinant yields a polynomial of degree \\(n\\) in \\(\lambda\\), known as the characteristic polynomial of \\(A\\). The eigenvalues of \\(A\\) are the roots of this polynomial, and by the fundamental theorem of algebra there are exactly \\(n\\) of them, counted with multiplicity, in \\(\mathbb{C}\\).

> A matrix with real entries has a characteristic polynomial with real coefficients, but this does not prevent complex roots. Complex eigenvalues of a real matrix always appear in conjugate pairs.

- - -
## Eigenspaces

For each eigenvalue \\(\lambda_0\\), the [set](../sets/) of all vectors satisfying \\(A\mathbf{v} = \lambda_0\mathbf{v}\\) is a subspace of \\(\mathbb{R}^n\\) or \\(\mathbb{C}^n\\). It coincides with the [kernel](../?s=kernel) of \\(A - \lambda_0 I\\) and is called the eigenspace of \\(A\\) associated with \\(\lambda_0\\):

\\[
E_{\lambda_0} = \ker(A - \lambda_0 I) = \\{\\, \mathbf{v} : (A - \lambda_0 I)\mathbf{v} = \mathbf{0} \\,\\}
\\]

The dimension of \\(E_{\lambda_0}\\) is called the geometric multiplicity of \\(\lambda_0\\). Separately, the multiplicity of \\(\lambda_0\\) as a root of the characteristic polynomial is called the algebraic multiplicity of \\(\lambda_0\\). It can be shown that the geometric multiplicity never exceeds the algebraic one, and the two coincide in the most well-behaved cases.

- - -
## Example 1

Consider the following [matrix](../matrices/):

\\[
A = \begin{pmatrix} 3 & 1 \\\\ 0 & 2 \end{pmatrix}
\\]

We compute the characteristic [polynomial](../polynomials/) by forming the matrix \\(A - \lambda I\\) and computing its [determinant](../determinant/). Since \\(A - \lambda I\\) is upper triangular, its determinant is the product of the diagonal entries:

\\[
\det(A - \lambda I) = (3 - \lambda)(2 - \lambda)
\\]

Setting this expression equal to zero gives \\(\lambda_1 = 2\\) and \\(\lambda_2 = 3\\). For \\(\lambda_1 = 2\\), we solve \\((A - 2I)\mathbf{v} = \mathbf{0}\\). The matrix \\(A - 2I\\) reduces to:

\\[
A - 2I = \begin{pmatrix} 1 & 1 \\\\ 0 & 0 \end{pmatrix}
\\]

The system yields the single condition \\(v_1 + v_2 = 0\\), so \\(v_1 = -v_2\\). Taking \\(v_2 = 1\\), the eigenspace \\(E_2\\) is spanned by:

\\[
\mathbf{v}_1 = \begin{pmatrix} -1 \\\\ 1 \end{pmatrix}
\\]

For \\(\lambda_2 = 3\\), the matrix \\(A - 3I\\) is:

\\[
A - 3I = \begin{pmatrix} 0 & 1 \\\\ 0 & -1 \end{pmatrix}
\\]

Both rows give the condition \\(v_2 = 0\\), leaving \\(v_1\\) free. Taking \\(v_1 = 1\\), the eigenspace \\(E_3\\) is spanned by:

\\[
\mathbf{v}\_2 = \begin{pmatrix} 1 \\\\ 0 \end{pmatrix}
\\]

The matrix \\(A\\) has therefore eigenvalue \\(\lambda_1 = 2\\) with eigenvector \\((-1, 1)^T\\), and eigenvalue \\(\lambda_2 = 3\\) with eigenvector \\((1, 0)^T\\).

- - -
## Example 2

Consider the matrix

\\[
A = \begin{pmatrix} 2 & 1 & 0 \\\\ 0 & 2 & 0 \\\\ 0 & 0 & 3 \end{pmatrix}
\\]

The matrix \\(A - \lambda I\\) is block upper triangular, so its determinant is again the product of the diagonal entries. The characteristic polynomial is the following:

\\[
p(\lambda) = (2 - \lambda)^2(3 - \lambda)
\\]

Setting \\(p(\lambda) = 0\\) gives two eigenvalues: \\(\lambda_1 = 2\\), with algebraic multiplicity two, and \\(\lambda_2 = 3\\), with algebraic multiplicity one.

For \\(\lambda_2 = 3\\), we solve \\((A - 3I)\mathbf{v} = \mathbf{0}\\). The matrix \\(A - 3I\\) is:

\\[
A - 3I = \begin{pmatrix} -1 & 1 & 0 \\\\ 0 & -1 & 0 \\\\ 0 & 0 & 0 \end{pmatrix}
\\]

The second row gives \\(v_2 = 0\\), and the first row then gives \\(v_1 = 0\\), leaving \\(v_3\\) free. Taking \\(v_3 = 1\\), the eigenspace \\(E_3\\) is spanned by:

\\[
\mathbf{v}_1 = \begin{pmatrix} 0 \\\\ 0 \\\\ 1 \end{pmatrix}
\\]

For \\(\lambda_1 = 2\\), we solve \\((A - 2I)\mathbf{v} = \mathbf{0}\\). The matrix \\(A - 2I\\) is:

\\[
A - 2I = \begin{pmatrix} 0 & 1 & 0 \\\\ 0 & 0 & 0 \\\\ 0 & 0 & 1 \end{pmatrix}
\\]

The first row gives \\(v_2 = 0\\) and the third row gives \\(v_3 = 0\\), while \\(v_1\\) remains free. Taking \\(v_1 = 1\\), the eigenspace \\(E_2\\) is one-dimensional, spanned by:

\\[
\mathbf{v}\_2 = \begin{pmatrix} 1 \\\\ 0 \\\\ 0 \end{pmatrix}
\\]

The geometric multiplicity of \\(\lambda_1 = 2\\) is therefore one, while its algebraic multiplicity is two. Since these two values differ, the matrix \\(A\\) is not diagonalizable. It possesses only two [linearly independent](../rank-of-a-matrix/) eigenvectors, which is insufficient to form a basis of \\(\mathbb{R}^3\\).

- - -
## Linear independence of eigenvectors

Eigenvectors corresponding to distinct eigenvalues are always linearly independent. More precisely, if \\(\lambda_1, \ldots, \lambda_k\\) are pairwise distinct eigenvalues of \\(A\\) with associated eigenvectors \\(\mathbf{v}\_1, \ldots, \mathbf{v}\_k\\), then \\(\mathbf{v}\_1, \ldots, \mathbf{v}\_k\\) are linearly independent. The proof proceeds by induction on \\(k\\) and uses the fact that each eigenvalue is distinct to derive a contradiction from any supposed linear dependence relation.

As a consequence, a square matrix of order \\(n\\) with \\(n\\) distinct eigenvalues always possesses \\(n\\) linearly independent eigenvectors, and therefore admits a basis of eigenvectors.

- - -
## Diagonalization

A matrix \\(A\\) of order \\(n\\) is called diagonalizable if it can be written in the form

\\[
A = PDP^{-1}
\\]

where \\(P\\) is an invertible matrix and \\(D\\) is diagonal. The columns of \\(P\\) are eigenvectors of \\(A\\), and the corresponding diagonal entries of \\(D\\) are the associated eigenvalues. This decomposition, when it exists, simplifies many computations substantially. In particular, the \\(k\\)-th power of \\(A\\) takes the form:

\\[
A^k = PD^kP^{-1}
\\]

Since raising a diagonal matrix to a power amounts to raising each diagonal entry to that power, this avoids the need to perform \\(k\\) successive matrix multiplications.

A matrix is diagonalizable if and only if, for every eigenvalue, its geometric multiplicity equals its algebraic multiplicity. When this condition fails, the matrix cannot be diagonalized but can be reduced to Jordan canonical form, which is the closest diagonal-like structure available in the general case.

- - -
## Trace, determinant and eigenvalues

Let \\(\lambda_1, \lambda_2, \ldots, \lambda_n\\) be the eigenvalues of \\(A\\) counted with algebraic multiplicity. Two classical identities relate them directly to entries of the matrix. The trace of \\(A\\), defined as the sum of its diagonal entries, satisfies:

\\[
\text{tr}(A) = \lambda_1 + \lambda_2 + \cdots + \lambda_n
\\]

The [determinant](../determinant/) of \\(A\\) satisfies:

\\[
\det(A) = \lambda_1 \cdot \lambda_2 \cdots \lambda_n
\\]

Both identities follow from the structure of the characteristic polynomial. The second has the following consequence: a matrix is singular if and only if zero is one of its eigenvalues. Together, these two relations offer a quick consistency check when eigenvalues are computed by hand, without requiring any additional verification.