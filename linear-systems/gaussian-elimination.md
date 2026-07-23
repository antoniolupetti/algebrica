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
  - reduced-row-echelon-form
  - row-echelon-form
---

## What is Gaussian elimination

The Gauss method, or Gaussian elimination, is an algorithm for solving [systems](../systems-of-linear-equations/) of linear equations. At each stage one variable is eliminated, and the result is an [equivalent system](../equations/) with fewer terms. The algorithm is valid for any system of $m$ equations in $n$ unknowns. The initial model below is a $3\times3$ system, which has a unique solution when its coefficient matrix is invertible. The equation-by-equation treatment of this case is in [systems of linear equations in three variables](../systems-of-linear-equations-in-three-variables/):

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

Each operation has an inverse of the same type, so the solution set is unchanged.

> The calculations on the coefficients require only the four arithmetic operations, so the algorithm is valid over any [field](../fields/), for example $\mathbb{Q},$ $\mathbb{R},$ or $\mathbb{C}.$

- - -

The process has four steps:

+ Eliminate the variable $x_1$ from all equations except the first.
+ Eliminate the variable $x_2$ from the third equation.
+ Solve the third equation for $x_3$.
+ Work backwards to find the remaining variables.

The last two steps are called back substitution. Elimination does not always end with a unique solution. A row of the form $0=c,$ with $c\neq0,$ means that the system is inconsistent. If no inconsistency appears and the pivots are fewer than the unknowns, the system has infinitely many solutions, parametrized by the unknowns without a pivot. In a square system this is the case when an equation reduces to the identity $0=0.$ The [Rouché-Capelli theorem](../rouche-capelli-theorem/) classifies these cases through the ranks of the coefficient and augmented matrices.

## Connection with matrices

The computation is carried out on the augmented [matrix](../matrices/) of the system, which has the coefficient matrix on the left and the column of constants on the right:

$$
\left(
\begin{array}{ccc|c}
a_{11} & a_{12} & a_{13} & b_1 \\[6pt]
a_{21} & a_{22} & a_{23} & b_2 \\[6pt]
a_{31} & a_{32} & a_{33} & b_3
\end{array}
\right)
$$

Operations on equations are elementary row operations on the augmented matrix. After Gaussian elimination, the matrix is in row echelon form. Every zero row is below the nonzero rows, and the leading nonzero entry of each row, called the pivot, is to the right of the pivot in the row above. For an invertible $3\times3$ matrix the row echelon form is upper triangular:

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

> Row echelon form has zeros below each pivot, but entries above a pivot may be nonzero. Gauss-Jordan elimination clears the entries above the pivots, and the result is the reduced row echelon form described below.

## Reduction to triangular form

We first eliminate the variable $x_1$ from every equation below the first. If $a_{11}=0,$ the first row is exchanged with a row whose coefficient of $x_1$ is nonzero. The same operation is available at any later stage when a pivot is zero. To remove $x_1$ from the second equation, we multiply the first equation by $a_{21}$ and the second by $a_{11}$ (legitimate because $a_{11}\neq0$), subtract the two equations, and use the result as the new second equation:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
\left(a_{11}a_{22} - a_{21}a_{12}\right)x_2 + \left(a_{11}a_{23} - a_{21}a_{13}\right)x_3 = a_{11}b_2 - a_{21}b_1 \\[6pt]
a_{31}x_1 + a_{32}x_2 + a_{33}x_3 = b_3
\end{cases}
$$

To simplify the calculations, we rewrite the second equation as:

$$a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2$$

The equivalent system is:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
a_{31}x_1 + a_{32}x_2 + a_{33}x_3 = b_3
\end{cases}
$$

Next we multiply the first equation by $a_{31}$ and the third equation by $a_{11}$, subtract the two equations, and use the result as the new third equation:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
\left(a_{11}a_{32} - a_{31}a_{12}\right)x_2 + \left(a_{11}a_{33} - a_{31}a_{13}\right)x_3 = a_{11}b_3 - a_{31}b_1
\end{cases}
$$

We rewrite the third equation as:

$$a^\prime_{32}x_2 + a^\prime_{33}x_3 = b^\prime_3$$

The equivalent system is:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
a^\prime_{32}x_2 + a^\prime_{33}x_3 = b^\prime_3
\end{cases}
$$

We now eliminate $x_2$ from the third equation. We multiply the second equation by $a^\prime_{32}$ and the third equation by $a^\prime_{22}$, subtract the two equations, and use the result as the new third equation. The equivalent system is:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = b_1 \\[6pt]
a^\prime_{22}x_2 + a^\prime_{23}x_3 = b^\prime_2 \\[6pt]
a^{\prime\prime}_{33}x_3 = b^{\prime\prime}_3
\end{cases}
$$

This is a triangular system. Since the coefficient matrix is invertible, $a^{\prime\prime}_{33} \neq 0$ and we solve for $x_3$ from the third equation:

$$x_3 = \frac{b^{\prime\prime}_3}{a^{\prime\prime}_{33}}$$

Back substitution uses the value of $x_3$ to determine the remaining variables in reverse order.

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

The equivalent system is:

$$
\begin{cases}
x + y + z = 6 \\[6pt]
y - z = 2 \\[6pt]
y + 2z = 8
\end{cases}
$$

Using the second equation as the new pivot, we eliminate $y$ from the third equation by subtracting the second equation from the third:

$$(y + 2z) - (y - z) = 3z = 6 \Rightarrow z = 2$$

Back substitution starts with the second equation:

$$y - z = 2 \Rightarrow y = 2 + z = 4$$

From the first equation:

$$x = 6 - y - z = 6 - 4 - 2 = 0$$

The solution is:

$$x = 0, \quad y = 4, \quad z = 2$$

The augmented matrix has the same sequence of operations. The labels above the arrows record each row replacement:

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

The final matrix is in row echelon form, and its rows are the triangular system solved above by back substitution.

- - -

Elimination shows when a system does not have a unique solution. Consider:

$$
\begin{cases}
x + y + z = 1 \\[6pt]
x + y + 2z = 3 \\[6pt]
2x + 2y + 3z = 4
\end{cases}
$$

Subtracting the first equation from the second, and twice the first equation from the third, leaves $z=2$ in both. Their difference is the identity $0=0.$ The echelon form has two pivots and three unknowns, so the system has infinitely many solutions. The unknown $y$ is free. The remaining relations from back substitution are $z=2$ and $x=-1-y.$ If the constant term of the third equation were $5$ instead of $4,$ the last row would be $0=1,$ and the system would have no solutions.

## Gauss-Jordan elimination and reduced row echelon form

Gaussian elimination stops when the matrix is in row echelon form. The pivot columns then have zeros below their pivots, and the unknowns are determined by back substitution. Gauss-Jordan elimination continues until every pivot column has zeros below and above its pivot. In reduced row echelon form (RREF), the solution is read without back substitution.

A matrix is in reduced row echelon form when it satisfies four conditions:

+ Every zero row is below every nonzero row.
+ The first nonzero entry of each nonzero row is $1.$ This entry is the pivot of the row.
+ The pivot of each row is to the right of the pivot in the row above it.
+ Every pivot is the only nonzero entry in its column.

The first and third conditions are part of row echelon form. In reduced form, every pivot is $1,$ and every entry above it is zero. Every row-equivalence class has one reduced row echelon form. The sequence of row operations is not unique, but the final reduced matrix is.

The Gauss-Jordan procedure has a forward phase and a backward phase:

+ Use Gaussian elimination to obtain row echelon form.
+ Divide each nonzero row by its pivot so that every pivot is $1.$
+ Starting with the last pivot, add suitable multiples of its row to the rows above it until every other entry in the pivot column is zero.
+ Continue upwards through the pivot rows.

Consider the following system:

$$
\begin{cases}
2x + y = 4 \\[6pt]
x - y = 5
\end{cases}
$$

Its augmented matrix is:

$$
\left(
\begin{array}{cc|c}
2 & 1 & 4 \\[6pt]
1 & -1 & 5
\end{array}
\right)
$$

The second row has coefficient $1$ in the first column, so we exchange the rows:

$$
\left(
\begin{array}{cc|c}
2 & 1 & 4 \\[6pt]
1 & -1 & 5
\end{array}
\right)
\xrightarrow{R_1 \leftrightarrow R_2}
\left(
\begin{array}{cc|c}
1 & -1 & 5 \\[6pt]
2 & 1 & 4
\end{array}
\right)
$$

The forward phase eliminates $x$ from the second row:

$$
\left(
\begin{array}{cc|c}
1 & -1 & 5 \\[6pt]
2 & 1 & 4
\end{array}
\right)
\xrightarrow{R_2 \to R_2 - 2R_1}
\left(
\begin{array}{cc|c}
1 & -1 & 5 \\[6pt]
0 & 3 & -6
\end{array}
\right)
$$

We normalize the second pivot and use it to clear the entry above:

$$
\left(
\begin{array}{cc|c}
1 & -1 & 5 \\[6pt]
0 & 3 & -6
\end{array}
\right)
\xrightarrow{R_2 \to \frac{1}{3}R_2}
\left(
\begin{array}{cc|c}
1 & -1 & 5 \\[6pt]
0 & 1 & -2
\end{array}
\right)
\xrightarrow{R_1 \to R_1 + R_2}
\left(
\begin{array}{cc|c}
1 & 0 & 3 \\[6pt]
0 & 1 & -2
\end{array}
\right)
$$

The coefficient block of the final matrix is the identity matrix. Its rows are the equations $x=3$ and $y=-2,$ so the system has the unique solution:

$$
(x,y) = (3,-2)
$$

- - -

In reduced row echelon form, the free variables of an undetermined system are visible from the columns without pivots. Consider the augmented matrix:

$$
\left(
\begin{array}{cccc|c}
1 & 2 & 0 & 1 & 3 \\[6pt]
1 & 2 & 1 & 2 & 5 \\[6pt]
2 & 4 & 1 & 3 & 8
\end{array}
\right)
$$

We subtract the first row from the second and twice the first row from the third:

$$
\left(
\begin{array}{cccc|c}
1 & 2 & 0 & 1 & 3 \\[6pt]
1 & 2 & 1 & 2 & 5 \\[6pt]
2 & 4 & 1 & 3 & 8
\end{array}
\right)
\xrightarrow{\substack{R_2 \to R_2 - R_1 \\ R_3 \to R_3 - 2R_1}}
\left(
\begin{array}{cccc|c}
1 & 2 & 0 & 1 & 3 \\[6pt]
0 & 0 & 1 & 1 & 2 \\[6pt]
0 & 0 & 1 & 1 & 2
\end{array}
\right)
$$

The last two rows are equal, so their difference is a zero row:

$$
\left(
\begin{array}{cccc|c}
1 & 2 & 0 & 1 & 3 \\[6pt]
0 & 0 & 1 & 1 & 2 \\[6pt]
0 & 0 & 1 & 1 & 2
\end{array}
\right)
\xrightarrow{R_3 \to R_3 - R_2}
\left(
\begin{array}{cccc|c}
1 & 2 & 0 & 1 & 3 \\[6pt]
0 & 0 & 1 & 1 & 2 \\[6pt]
0 & 0 & 0 & 0 & 0
\end{array}
\right)
$$

The final matrix is in reduced row echelon form. The pivots are in the columns of $x$ and $z,$ while the columns of $y$ and $w$ have no pivots. We set the free variables equal to $y=s$ and $w=t.$ The equations in the two nonzero rows are:

$$
\begin{align}
x + 2y + w &= 3 \\[6pt]
z + w &= 2
\end{align}
$$

With $y=s$ and $w=t,$ the pivot variables are:

$$
\begin{align}
x &= 3 - 2s - t \\[6pt]
y &= s \\[6pt]
z &= 2 - t \\[6pt]
w &= t
\end{align}
$$

The complete solution set is:

$$
\begin{pmatrix}
x \\[6pt]
y \\[6pt]
z \\[6pt]
w
\end{pmatrix}
=
\begin{pmatrix}
3 \\[6pt]
0 \\[6pt]
2 \\[6pt]
0
\end{pmatrix}
+
s
\begin{pmatrix}
-2 \\[6pt]
1 \\[6pt]
0 \\[6pt]
0
\end{pmatrix}
+
t
\begin{pmatrix}
-1 \\[6pt]
0 \\[6pt]
-1 \\[6pt]
1
\end{pmatrix}
\qquad s,t \in \mathbb{R}
$$

Each nonpivot column in the coefficient block has one free variable. If the last column of the reduced augmented matrix has a pivot, one row is an impossible equation of the form $0=c$ with $c\neq0,$ and the system is inconsistent.

## Applications of row reduction

The [rank](../rank-of-a-matrix/) of a matrix is the number of nonzero rows of its row echelon form, because elementary row operations do not change the [row space](../vector-spaces/). The nonzero rows of the echelon form are a basis of the row space, and the columns of the original matrix at the pivot positions are a basis of its [column space](../linear-combinations/).

The [determinant](../determinant-of-a-square-matrix/) of a square matrix can be read from the elimination. Swapping two rows changes its sign, multiplying one row by $c\neq0$ multiplies it by $c,$ and adding a multiple of one row to another leaves it unchanged. If the reduction of $A$ to triangular form has $s$ row swaps and row multipliers $c_1,\dots,c_k,$ then:

$$\det A = \frac{(-1)^s}{c_1 \cdots c_k} a^{\vphantom{\prime}}_{11}a^\prime_{22}a^{\prime\prime}_{33}$$

The same formula holds for any $n\times n$ matrix, with the product of the $n$ diagonal entries of the triangular form in place of $a_{11}a^\prime_{22}a^{\prime\prime}_{33}.$ For an $n\times n$ matrix, elimination requires about $2n^3/3$ arithmetic operations, while the cost of the Laplace expansion grows like $n!.$ Row reduction is the practical method for large matrices.

The [inverse](../inverse-matrix/) of a square matrix is computed by the same procedure. We place the identity matrix beside $A$ in the block matrix $[A\mid I_n]$ and apply Gauss-Jordan elimination. The matrix $A$ is invertible if and only if the reduced left block is $I_n.$ In that case the right block is $A^{-1},$ because the combined effect of the row operations on $A$ is left multiplication by $A^{-1}.$
