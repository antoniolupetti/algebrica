---
title: Gaussian Elimination
source: https://algebrica.org/gaussian-elimination/
license: CC BY-NC 4.0
tags:
  - augmented-matrix
  - back-substitution
  - gauss-jordan-elimination
  - gaussian-elimination
  - linear-algebra
  - linear-systems
  - matrices
  - pivot
  - row-echelon-form
---

## What is Gaussian elimination

The Gauss method, or Gaussian elimination, is an algorithm for solving [systems](../systems-of-linear-equations/) of linear equations. The process eliminates one variable at a time and transforms the system into a form that is easy to solve. The algorithm applies to any system of $m$ equations in $n$ unknowns; we describe it on a $3\times3$ system, which has a unique solution when its coefficient matrix is invertible:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a_{21}x_1 + a_{22}x_2 + a_{23}x_3 = b_2 \\[6pt]
a_{31}x_1 + a_{32}x_2 + a_{33}x_3 = b_3
\end{cases}
$$

Every step of the algorithm is one of three elementary operations:

+ swapping two equations
+ multiplying an equation by a nonzero constant
+ adding to one equation a multiple of another equation

Each operation is reversible by an operation of the same type, so the solution set of the system never changes.

> The algorithm uses only the four arithmetic operations on the coefficients, so it works unchanged over any [field](../fields/), for example $\mathbb{Q},$ $\mathbb{R},$ or $\mathbb{C}.$

- - -

The process has four steps:

+ Eliminate the variable $x_1$ from all equations except the first.
+ Eliminate the variable $x_2$ from the third equation.
+ Solve the third equation for $x_3$.
+ Work backwards to find the remaining variables.

The last two steps are called back substitution. The elimination does not always end with a unique solution. If it produces an equation of the form $0 = c$ with $c \neq 0,$ the system is inconsistent and has no solutions. If no inconsistency appears and the pivots are fewer than the unknowns, the system has infinitely many solutions, parametrized by the unknowns that do not correspond to a pivot; in a square system this is the case when an equation reduces to the identity $0 = 0.$ The [Rouché-Capelli theorem](../rouche-capelli-theorem/) distinguishes these cases by comparing the ranks of the coefficient matrix and of the augmented matrix.

## Connection with matrices

In practice the computation acts on the augmented matrix of the system, the [matrix](../matrices/) of coefficients with the column of constant terms appended:

$$
\left(
\begin{array}{ccc|c}
a_{11} & a_{12} & a_{13} & b_1 \\[6pt]
a_{21} & a_{22} & a_{23} & b_2 \\[6pt]
a_{31} & a_{32} & a_{33} & b_3
\end{array}
\right)
$$

Operations on equations become elementary row operations on this matrix. Gaussian elimination brings a matrix into row echelon form, in which every zero row is below the nonzero rows and the leading nonzero entry of each row, called the pivot, is strictly to the right of the pivot of the row above. For an invertible $3\times3$ matrix the row echelon form is upper triangular:

$$
A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\[6pt]
a_{21} & a_{22} & a_{23} \\[6pt]
a_{31} & a_{32} & a_{33}
\end{pmatrix}
\quad \xrightarrow{\text{to}} \quad
\begin{pmatrix}
a_{11} & a_{12} & a_{13} \\[6pt]
0 & a^\prime_{22} & a^\prime_{23} \\[6pt]
0 & 0 & a^{\prime\prime}_{33}
\end{pmatrix}
$$

> If the reduction continues until every pivot is $1$ and is the only nonzero entry in its column, the result is the reduced row echelon form, which is unique. This longer procedure is called Gauss-Jordan elimination.

## Reduction to triangular form

We begin by eliminating the variable $x_1$ from all equations except the first. If $a_{11} = 0,$ we first swap the first equation with one whose coefficient of $x_1$ is nonzero; the same swap works at every later stage in which the pivot is zero. To remove $x_1$ from the second equation, we multiply the first equation by $a_{21}$ and the second by $a_{11}$ (legitimate because $a_{11} \neq 0$), subtract the two resulting equations, and replace the second equation with the result:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
\left(a_{11}a_{22} - a_{21}a_{12}\right)x_2 + \left(a_{11}a_{23} - a_{21}a_{13}\right)x_3 = a_{11}b_2 - a_{21}b_1 \\[6pt]
a_{31}x_1 + a_{32}x_2 + a_{33}x_3 = b_3
\end{cases}
$$

To simplify the calculations, we rewrite the second equation as:

$$a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2$$

The system becomes:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
a_{31}x_1 + a_{32}x_2 + a_{33}x_3 = b_3
\end{cases}
$$

Next we multiply the first equation by $a_{31}$ and the third equation by $a_{11}$, subtract the two resulting equations, and replace the third equation with the result:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
\left(a_{11}a_{32} - a_{31}a_{12}\right)x_2 + \left(a_{11}a_{33} - a_{31}a_{13}\right)x_3 = a_{11}b_3 - a_{31}b_1
\end{cases}
$$

We rewrite the third equation as:

$$a^\prime_{32}x_2 + a^\prime_{33}x_3 = b^\prime_3$$

The system is now:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
a^\prime_{32}x_2 + a^\prime_{33}x_3 = b^\prime_3
\end{cases}
$$

We proceed with the second step and eliminate the variable $x_2$ from the third equation. We multiply the second equation by $a^\prime_{32}$ and the third equation by $a^\prime_{22}$, subtract the two resulting equations, and replace the third equation with the result. Completing the calculations as in the first step, the system reduces to:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
a^{\prime\prime}_{33}x_3 = b^{\prime\prime}_3
\end{cases}
$$

This is a triangular system. Since the coefficient matrix is invertible, $a^{\prime\prime}_{33} \neq 0$ and we solve for $x_3$ from the third equation:

$$x_3 = \frac{b^{\prime\prime}_3}{a^{\prime\prime}_{33}}$$

From the known value of $x_3$ we determine each remaining variable in turn.

## Example

Consider the following $3\times3$ system of linear equations:

$$
\begin{cases}
x + y + z = 6 \\[6pt]
2x + 3y + z = 14 \\[6pt]
x + 2y + 3z = 14
\end{cases}
$$

To eliminate $x$ from the second equation, we subtract twice the first equation from the second:

$$(2x + 3y + z) - 2(x + y + z) = y - z = 2$$

To eliminate $x$ from the third equation, we subtract the first equation from the third:

$$(x + 2y + 3z) - (x + y + z) = y + 2z = 8$$

The system becomes:

$$
\begin{cases}
x + y + z = 6 \\[6pt]
y - z = 2 \\[6pt]
y + 2z = 8
\end{cases}
$$

Using the second equation as the new pivot, we eliminate $y$ from the third equation by subtracting the second equation from the third:

$$(y + 2z) - (y - z) = 3z = 6 \Rightarrow z = 2$$

Substituting back gives the remaining variables. From the second equation:

$$y - z = 2 \Rightarrow y = 2 + z = 4$$

From the first equation:

$$x = 6 - y - z = 6 - 4 - 2 = 0$$

The solution is:

$$x = 0, \quad y = 4, \quad z = 2$$

In matrix form the same computation acts on the augmented matrix; the labels above the arrows record the row operations:

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\[6pt]
2 & 3 & 1 & 14 \\[6pt]
1 & 2 & 3 & 14
\end{array}
\right)
\xrightarrow{\substack{R_2 - 2R_1 \\ R_3 - R_1}}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\[6pt]
0 & 1 & -1 & 2 \\[6pt]
0 & 1 & 2 & 8
\end{array}
\right)
\xrightarrow{R_3 - R_2}
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\[6pt]
0 & 1 & -1 & 2 \\[6pt]
0 & 0 & 3 & 6
\end{array}
\right)
$$

The final matrix is in row echelon form and corresponds to the triangular system solved above by back substitution.

- - -

Elimination also detects the systems without a unique solution. Consider:

$$
\begin{cases}
x + y + z = 1 \\[6pt]
x + y + 2z = 3 \\[6pt]
2x + 2y + 3z = 4
\end{cases}
$$

Subtracting the first equation from the second, and twice the first equation from the third, leaves $z = 2$ in both; subtracting the second of these from the third then produces the identity $0 = 0.$ The echelon form has two pivots and three unknowns, so the system has infinitely many solutions. The unknown $y$ is free, and back substitution gives $z = 2$ and $x = -1 - y.$ If the constant term of the third equation were $5$ instead of $4,$ the last row would read $0 = 1,$ and the system would have no solutions.

## Applications of row reduction

The [rank](../rank-of-a-matrix/) of a matrix is the number of nonzero rows of its row echelon form, because elementary row operations do not change the row space. The nonzero rows of the echelon form are a basis of the row space, and the columns of the original matrix at the pivot positions are a basis of the [column space](../vector-spaces/).

The [determinant](../determinant-of-a-square-matrix/) of a square matrix can be read from the elimination. Swapping two rows changes the sign of the determinant, multiplying a row by a constant $c \neq 0$ multiplies the determinant by $c,$ and adding a multiple of one row to another leaves it unchanged. If the reduction of $A$ to the triangular form above uses $s$ row swaps and multiplies rows by the constants $c_1, \dots, c_k,$ then:

$$\det A = \frac{(-1)^s}{c_1 \cdots c_k} a^{\vphantom{\prime}}_{11}a^\prime_{22}a^{\prime\prime}_{33}$$

The same formula holds for any $n \times n$ matrix, with the product of the $n$ diagonal entries of the triangular form in place of $a_{11}a^\prime_{22}a^{\prime\prime}_{33}.$ For an $n \times n$ matrix the elimination requires about $2n^3/3$ arithmetic operations, while the cost of the Laplace expansion grows like $n!,$ so row reduction is the practical method for large matrices.

The [inverse](../inverse-matrix/) of a square matrix is computed by the same procedure. We augment $A$ with the identity matrix and apply Gauss-Jordan elimination to the block matrix $[A \mid I_n].$ The matrix $A$ is invertible exactly when the reduction turns the left block into $I_n,$ and in that case the right block of the result is $A^{-1},$ because the row operations that transform $A$ into $I_n$ correspond to left multiplication by $A^{-1}.$
