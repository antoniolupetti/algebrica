# Matrix Diagonalization

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/matrix-diagonalization/

## The diagonalization condition

A square [matrix](../matrices/) is said to be diagonalizable when it is possible to find a basis of the underlying [vector space](../vector-spaces/) consisting entirely of [eigenvectors](../eigenvalues-and-eigenvectors/) of that matrix. When such a basis exists, the matrix can be expressed in a particularly simple form: a diagonal matrix whose entries are precisely the eigenvalues. This representation is not merely a notational convenience; it reveals the intrinsic geometric structure of the linear transformation associated with the matrix and simplifies substantially the computation of powers, exponentials, and solutions to linear differential equations.

Let \\(A\\) be a square matrix of order \\(n\\) with entries in \\(\mathbb{R}\\) or \\(\mathbb{C}\\). The matrix \\(A\\) is diagonalizable if and only if there exists an invertible matrix \\(P\\) and a diagonal matrix \\(D\\) such that the following relation holds:

\\[
A = P D P^{-1}
\\]

The columns of \\(P\\) are eigenvectors of \\(A\\), and the diagonal entries of \\(D\\) are the corresponding eigenvalues. Equivalently, the relation above can be rewritten as follows:

\\[
P^{-1} A P = D
\\]

This formulation makes clear that \\(P\\) is a change-of-basis matrix: it transforms the standard representation of \\(A\\) into the diagonal representation \\(D\\) expressed in the eigenvector basis.

> The matrix \\(D\\) is unique up to the ordering of the eigenvalues along the diagonal, while \\(P\\) is not unique, since each eigenvector may be replaced by any nonzero scalar multiple.

- - -
## Eigenvalues and eigenvectors

The construction of the diagonalization relies entirely on the [eigenstructure](../eigenvalues-and-eigenvectors/) of \\(A\\). Recall that a scalar \\(\lambda\\) is an eigenvalue of \\(A\\) if there exists a nonzero vector \\(\mathbf{v}\\) satisfying the following equation:

\\[
A \mathbf{v} = \lambda \mathbf{v}
\\]

Such a vector \\(\mathbf{v}\\) is called an eigenvector of \\(A\\) associated with \\(\lambda\\). The eigenvalues are determined by solving the characteristic equation, which is obtained by requiring that the matrix \\(A - \lambda I\\) be singular:

\\[
\det(A - \lambda I) = 0
\\]

The left-hand side of this equation is a [polynomial](../polynomials/) of degree \\(n\\) in \\(\lambda\\), called the characteristic polynomial of \\(A\\). Its roots, counted with multiplicity, are the eigenvalues of \\(A\\). Once an eigenvalue \\(\lambda_k\\) has been determined, the associated eigenvectors are the nonzero solutions of the homogeneous [linear system](../systems-of-linear-equations/):

\\[
(A - \lambda_k I)\\,\mathbf{v} = \mathbf{0}
\\]

The set of all solutions, including the zero vector, constitutes a [subspace](../spaces/) of \\(\mathbb{R}^n\\) (or \\(\mathbb{C}^n\\)), called the eigenspace associated with \\(\lambda_k\\).

- - -
## Algebraic and geometric multiplicity

Each eigenvalue \\(\lambda_k\\) carries two distinct notions of multiplicity that play a central role in determining whether \\(A\\) is diagonalizable. The algebraic multiplicity of \\(\lambda_k\\), denoted \\(m_a(\lambda_k)\\), is the multiplicity of \\(\lambda_k\\) as a root of the characteristic polynomial. The geometric multiplicity of \\(\lambda_k\\), denoted \\(m_g(\lambda_k)\\), is the dimension of the corresponding eigenspace, that is:

\\[
m_g(\lambda_k) = \dim \ker(A - \lambda_k I)
\\]

It can be shown that for every eigenvalue the geometric multiplicity does not exceed the algebraic multiplicity:

\\[
1 \leq m_g(\lambda_k) \leq m_a(\lambda_k)
\\]

The matrix \\(A\\) is diagonalizable if and only if, for every eigenvalue \\(\lambda_k\\), the geometric multiplicity equals the algebraic multiplicity. In particular, a matrix with \\(n\\) distinct eigenvalues is always diagonalizable, since in that case both multiplicities are equal to one for every eigenvalue.

- - -
## The diagonalization procedure

The practical construction of the matrices \\(P\\) and \\(D\\) follows a well-defined sequence of steps.

+ The first step consists of computing the characteristic polynomial \\(\det(A - \lambda I)\\) and finding all its [roots](../roots-of-a-polynomial/). These roots are the eigenvalues \\(\lambda_1, \lambda_2, \ldots, \lambda_k\\) of \\(A\\).

+ The second step consists of determining, for each eigenvalue, a basis of the corresponding eigenspace by solving the homogeneous system \\((A - \lambda_j I)\\,\mathbf{v} = \mathbf{0}\\). The union of all these bases must contain exactly \\(n\\) linearly independent vectors for the matrix to be diagonalizable.

+ The third step consists of forming the matrix \\(P\\) by placing the eigenvectors as columns, in an order that corresponds to the arrangement of eigenvalues in \\(D\\). The diagonal matrix \\(D\\) is then constructed by placing the eigenvalue \\(\lambda_j\\) in position \\((j,j)\\).

Once \\(P\\) has been assembled, one verifies that it is invertible and computes \\(P^{-1}\\), thereby completing the factorization \\(A = P D P^{-1}\\).

- - -
## Example 1

Consider the following matrix:

\\[
A = \begin{pmatrix} 3 & 1 \\\\ 0 & 2 \end{pmatrix}
\\]

To find the eigenvalues, one computes the [determinant](../determinant/) of \\(A - \lambda I\\):

\\[
\det(A - \lambda I) = \det \begin{pmatrix} 3 - \lambda & 1 \\\\ 0 & 2 - \lambda \end{pmatrix} = (3 - \lambda)(2 - \lambda)
\\]

The characteristic equation is therefore the following:

\\[
(3 - \lambda)(2 - \lambda) = 0
\\]

The two roots are \\(\lambda_1 = 2\\) and \\(\lambda_2 = 3\\), both simple, so the matrix is diagonalizable. For \\(\lambda_1 = 2\\), one solves the system \\((A - 2I)\\,\mathbf{v} = \mathbf{0}\\):

\\[
\begin{pmatrix} 1 & 1 \\\\ 0 & 0 \end{pmatrix} \begin{pmatrix} v_1 \\\\ v_2 \end{pmatrix} = \begin{pmatrix} 0 \\\\ 0 \end{pmatrix}
\\]

The first row gives \\(v_1 + v_2 = 0\\), so that \\(v_1 = -v_2\\). Choosing \\(v_2 = 1\\), one obtains the eigenvector \\(\mathbf{v}_1 = (-1,\\, 1)^T\\). For \\(\lambda_2 = 3\\), one solves \\((A - 3I)\\,\mathbf{v} = \mathbf{0}\\):

\\[
\begin{pmatrix} 0 & 1 \\\\ 0 & -1 \end{pmatrix} \begin{pmatrix} v_1 \\\\ v_2 \end{pmatrix} = \begin{pmatrix} 0 \\\\ 0 \end{pmatrix}
\\]

Both rows give \\(v_2 = 0\\), leaving \\(v_1\\) free. Choosing \\(v_1 = 1\\), one obtains the eigenvector \\(\mathbf{v}_2 = (1,\\, 0)^T\\). The matrix \\(P\\) is formed by placing these eigenvectors as columns:

\\[
P = \begin{pmatrix} -1 & 1 \\\\ 1 & 0 \end{pmatrix}
\\]

Its [inverse](../inverse-matrix/) is computed directly:

\\[
P^{-1} = \begin{pmatrix} 0 & 1 \\\\ 1 & 1 \end{pmatrix}
\\]

The diagonal matrix collects the eigenvalues in the corresponding order:

\\[
D = \begin{pmatrix} 2 & 0 \\\\ 0 & 3 \end{pmatrix}
\\]

One may verify that \\(A = P D P^{-1}\\) holds by direct multiplication. The matrix \\(A\\) is therefore diagonalizable, and its diagonalization is given by the factorization above, with \\(P\\) and \\(D\\) as constructed.

- - -

## Example 2

Consider a matrix with a repeated eigenvalue. Let \\(A\\) be the following \\(3 \times 3\\) matrix:

\\[
A = \begin{pmatrix} 4 & 1 & 0 \\\\ 0 & 4 & 0 \\\\ 0 & 0 & 2 \end{pmatrix}
\\]

The characteristic polynomial is obtained by expanding the determinant of \\(A - \lambda I\\):

\\[
\det(A - \lambda I) = \det \begin{pmatrix} 4 - \lambda & 1 & 0 \\\\ 0 & 4 - \lambda & 0 \\\\ 0 & 0 & 2 - \lambda \end{pmatrix} = (4 - \lambda)^2 (2 - \lambda)
\\]

The eigenvalues are therefore \\(\lambda_1 = 4\\), with algebraic multiplicity two, and \\(\lambda_2 = 2\\), with algebraic multiplicity one. The simple eigenvalue \\(\lambda_2 = 2\\) presents no difficulty. Solving \\((A - 2I)\\,\mathbf{v} = \mathbf{0}\\) gives the system:

\\[
\begin{pmatrix} 2 & 1 & 0 \\\\ 0 & 2 & 0 \\\\ 0 & 0 & 0 \end{pmatrix} \begin{pmatrix} v_1 \\\\ v_2 \\\\ v_3 \end{pmatrix} = \begin{pmatrix} 0 \\\\ 0 \\\\ 0 \end{pmatrix}
\\]

The second row gives \\(v_2 = 0\\), and substituting into the first row gives \\(v_1 = 0\\), while \\(v_3\\) remains free. The eigenspace is therefore one-dimensional, spanned by the vector \\(\mathbf{v}_3 = (0,\\, 0,\\, 1)^T\\). \The repeated eigenvalue \\(\lambda_1 = 4\\) is the critical case. Solving \\((A - 4I)\\,\mathbf{v} = \mathbf{0}\\) gives the system:

\\[
\begin{pmatrix} 0 & 1 & 0 \\\\ 0 & 0 & 0 \\\\ 0 & 0 & -2 \end{pmatrix} \begin{pmatrix} v_1 \\\\ v_2 \\\\ v_3 \end{pmatrix} = \begin{pmatrix} 0 \\\\ 0 \\\\ 0 \end{pmatrix}
\\]

The first row gives \\(v_2 = 0\\), and the third row gives \\(v_3 = 0\\), while \\(v_1\\) remains free. The eigenspace associated with \\(\lambda_1 = 4\\) is therefore one-dimensional, spanned by \\(\mathbf{v}_1 = (1,\\, 0,\\, 0)^T\\). Since the geometric multiplicity of \\(\lambda_1 = 4\\) is one, strictly less than its algebraic multiplicity of two, the three eigenvectors found are not sufficient to form a basis of \\(\mathbb{R}^3\\), and the matrix \\(A\\) is not diagonalizable.

> This example illustrates that the presence of a repeated eigenvalue does not by itself prevent diagonalization: what matters is whether the corresponding eigenspace has dimension equal to the algebraic multiplicity. A matrix with a repeated eigenvalue may or may not be diagonalizable depending on the rank of \\(A - \lambda I\\).

- - -
## When diagonalization fails

Not every square matrix is diagonalizable. A matrix fails to be diagonalizable precisely when, for at least one eigenvalue, the geometric multiplicity is strictly less than the algebraic multiplicity. In such cases, the eigenspace associated with that eigenvalue is too small to provide a sufficient number of linearly independent eigenvectors. A standard example is the matrix:

\\[
B = \begin{pmatrix} 2 & 1 \\\\ 0 & 2 \end{pmatrix}
\\]

Its characteristic polynomial is \\((2 - \lambda)^2\\), so \\(\lambda = 2\\) is the only eigenvalue with algebraic multiplicity two. Solving \\((B - 2I)\\,\mathbf{v} = \mathbf{0}\\) yields:

\\[
\begin{pmatrix} 0 & 1 \\\\ 0 & 0 \end{pmatrix} \begin{pmatrix} v_1 \\\\ v_2 \end{pmatrix} = \begin{pmatrix} 0 \\\\ 0 \end{pmatrix}
\\]

The only condition is \\(v_2 = 0\\), so the eigenspace is one-dimensional, spanned by \\((1,\, 0)^T\\). Since the geometric multiplicity is one while the algebraic multiplicity is two, it is not possible to assemble a basis of eigenvectors for \\(\mathbb{R}^2\\), and the matrix \\(B\\) is not diagonalizable.

> Matrices of this type are studied within the framework of Jordan normal form, which provides the canonical representation for non-diagonalizable matrices through the introduction of Jordan blocks.

- - -
## Powers of a diagonalizable matrix

One of the most immediate applications of diagonalization concerns the computation of integer powers of a matrix. For a diagonalizable matrix \\(A = P D P^{-1}\\), the \\(k\\)-th power admits the following compact expression:

\\[
A^k = P D^k P^{-1}
\\]

This identity follows from the observation that \\(A^2 = (PDP^{-1})(PDP^{-1}) = PD^2P^{-1}\\), and by induction the pattern extends to any positive integer \\(k\\). Since \\(D\\) is diagonal, its \\(k\\)-th power is simply obtained by raising each diagonal entry to the \\(k\\)-th power:

\\[
D^k = \begin{pmatrix} \lambda_1^k & & \\ & \ddots & \\ & & \lambda_n^k \end{pmatrix}
\\]

This observation transforms an otherwise laborious matrix multiplication into a straightforward scalar computation.