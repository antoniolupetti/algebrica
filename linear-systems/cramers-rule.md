---
title: Cramer's Rule
source: https://algebrica.org/cramers-rule/
license: CC BY-NC 4.0
tags:
  - coefficient-matrix
  - cramers-rule
  - determinant
  - homogeneous-system
  - linear-algebra
  - linear-systems
---
## Definition

Cramer's rule solves a [system](../systems-of-linear-equations/) of $n$ [linear equations](../linear-equations/) in $n$ unknowns through the [determinant](../determinant/) of the coefficient [matrix](../matrices/). It applies when the coefficient matrix is square with nonzero determinant, the condition under which the system has a unique solution.

Consider a general system of $n$ equations in $n$ unknowns:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = b_1 \\[6pt]
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = b_2 \\[6pt]
\quad\vdots \\[6pt]
a_{n1}x_1 + a_{n2}x_2 + \dots + a_{nn}x_n = b_n
\end{cases}
$$

In matrix form the system is $A\mathbf{x} = \mathbf{b},$ with coefficient matrix:

$$
A =
\begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\[6pt]
a_{21} & a_{22} & \cdots & a_{2n} \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{pmatrix}
$$

The unknowns and the constants form two column [vectors](../vectors/):

$$
\mathbf{x} =
\begin{pmatrix}
x_1 \\[6pt]
x_2 \\[6pt]
\vdots \\[6pt]
x_n
\end{pmatrix}
\qquad
\mathbf{b} =
\begin{pmatrix}
b_1 \\[6pt]
b_2 \\[6pt]
\vdots \\[6pt]
b_n
\end{pmatrix}
$$

Suppose the coefficient matrix $A$ is invertible, so that $\det(A) \neq 0.$ The system then has a unique solution, which the inverse of $A$ expresses as:

$$
\begin{pmatrix}
x_1 \\[6pt]
x_2 \\[6pt]
\vdots \\[6pt]
x_n
\end{pmatrix}
=
\frac{1}{\det(A)}
\begin{pmatrix}
A_{11} & A_{21} & \cdots & A_{n1} \\[6pt]
A_{12} & A_{22} & \cdots & A_{n2} \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
A_{1n} & A_{2n} & \cdots & A_{nn}
\end{pmatrix}
\begin{pmatrix}
b_1 \\[6pt]
b_2 \\[6pt]
\vdots \\[6pt]
b_n
\end{pmatrix}
$$

This is the general form of Cramer's rule. Here $A_{ij}$ is the cofactor of the entry $a_{ij}$, so the matrix multiplying $\mathbf{b}$ is the transpose of the cofactor matrix, the adjugate of $A$, written $\mathrm{adj}(A)$.

The unknown in position $k$ is a fraction whose denominator is $\det(A)$ and whose numerator is the determinant of the matrix $A_k$ obtained by replacing the $k$-th column of $A$ with the column of constants:

$$
x_k = \frac{\det(A_k)}{\det(A)}
$$

> Example 2 carries out this step in full for a system of two equations.

## Proof of the rule

Cramer's rule states that if $A$ is an invertible $n \times n$ matrix and $A_k$ denotes $A$ with its $k$-th column replaced by the constants $\mathbf{b}$, then the unique solution of $A\mathbf{x} = \mathbf{b}$ has components $x_k = \det(A_k)/\det(A).$ The formula follows from two properties of the determinant, with no reference to the inverse. Adding to one column a scalar multiple of another column leaves the determinant unchanged, and multiplying a single column by a scalar multiplies the determinant by that scalar.

Write $C_1, C_2, \dots, C_n$ for the columns of $A$. The product $A\mathbf{x}$ combines these columns with the unknowns as coefficients, so the equation $A\mathbf{x} = \mathbf{b}$ is the single column identity:

$$
\mathbf{b} = x_1 C_1 + x_2 C_2 + \dots + x_n C_n
$$

Fix an index $k$. By construction the $k$-th column of $A_k$ is $\mathbf{b}$, while every other column agrees with $A$:

$$
A_k = \left( C_1 \ \cdots \ C_{k-1} \ \ \mathbf{b} \ \ C_{k+1} \ \cdots \ C_n \right)
$$

Replace $\mathbf{b}$ by the identity above and, for each $j \neq k$, subtract $x_j C_j$ from the $k$-th column. Every such step subtracts a multiple of another column of $A_k$, so none of them changes the determinant. Once all the terms with $j \neq k$ are removed, the $k$-th column has collapsed to $x_k C_k$:

$$
\det(A_k) = \det\left( C_1 \ \cdots \ x_k C_k \ \cdots \ C_n \right)
$$

Factoring the scalar $x_k$ out of that column gives:

$$
\det(A_k) = x_k \det\left( C_1 \ \cdots \ C_k \ \cdots \ C_n \right) = x_k \det(A)
$$

Since $A$ is invertible, $\det(A) \neq 0,$ and dividing isolates the unknown:

$$
x_k = \frac{\det(A_k)}{\det(A)}
$$

The same computation applies for each $k = 1, \dots, n,$ which proves the rule.

## Geometric interpretation

Every determinant in the formula is a signed area or, in higher dimension, a signed volume. Take $n = 2$ and regard the columns $C_1$ and $C_2$ as vectors in the plane. The equation becomes $x_1 C_1 + x_2 C_2 = \mathbf{b},$ and $\det(A)$ is the signed area of the parallelogram built on $C_1$ and $C_2$.

Start from the parallelogram built on $x_1 C_1$ and $C_2$. Stretching one side by the factor $x_1$ stretches the area by the same factor, so its signed area is $x_1 \det(A).$ Now add $x_2 C_2$ to that side, sliding it along the direction of $C_2$. Sliding a side parallel to the opposite one keeps both base and height, so the area does not change. The side has become $x_1 C_1 + x_2 C_2 = \mathbf{b},$ and the parallelogram is now built on $\mathbf{b}$ and $C_2$, whose signed area is $\det(A_1).$ Equating the two areas gives:

$$
\det(A_1) = x_1 \det(A)
$$

so that $x_1 = \det(A_1)/\det(A).$ Exchanging the roles of the two columns yields $x_2$ in the same way.

For $n$ unknowns the determinant of $n$ vectors is the signed volume of the parallelepiped they span, and the two moves used above, scaling one edge and shearing it parallel to the others, carry over without change. They reproduce $\det(A_k) = x_k \det(A)$ for every $k$, the relation already found by algebra.

> The invariance of the area under the sliding step is the planar case of Cavalieri's principle, which assigns equal volume to two solids whose parallel cross-sections match.

## Computational cost

Cramer's rule is a formula rather than a practical algorithm. Solving an $n \times n$ system through it means evaluating $n + 1$ determinants of order $n$, the denominator $\det(A)$ together with one numerator $\det(A_k)$ for each unknown. Expanding a determinant of order $n$ straight from its definition adds up $n!$ signed products, so the cost grows faster than any exponential in $n$.

Gaussian elimination brings the coefficient matrix to triangular form in about $n^3/3$ arithmetic operations, and the determinant is the product of the pivots once the reduction is finished, by which point the system is already solved. For $n = 20$ the expansion of a single determinant needs on the order of $20! \approx 2 \cdot 10^{18}$ multiplications, against roughly $20^3/3 \approx 2.7 \cdot 10^3$ operations for elimination. Cramer's rule remains useful for small systems and for theoretical arguments that need each unknown as an explicit ratio of determinants.

## Solutions of homogeneous systems

A [homogeneous system](../systems-of-linear-equations/) has all constant terms equal to zero. Such a system always has the trivial solution, in which every unknown is zero, and the determinant of the coefficient matrix decides whether any other solution exists:

+ If $\det(A) \neq 0,$ the system has only the trivial solution.
+ If $\det(A) = 0,$ the system has infinitely many solutions, including nontrivial ones in which at least one unknown is nonzero.

> A homogeneous system is always consistent, since the trivial solution satisfies every equation.

## Example 1

Consider the following homogeneous system of three equations in three unknowns:

$$
\begin{cases}
x + y + z = 0 \\[6pt]
2x - y + z = 0 \\[6pt]
3x + y + 2z = 0
\end{cases}
$$

In matrix form the system is $A\mathbf{x} = \mathbf{0},$ with coefficient matrix:

$$
A = \begin{pmatrix}
1 & 1 & 1 \\[6pt]
2 & -1 & 1 \\[6pt]
3 & 1 & 2
\end{pmatrix}
$$

The nature of the solutions follows from the determinant of $A$:

$$
\begin{align}
\det(A) &= 1 \cdot (-1 \cdot 2 - 1 \cdot 1) - 1 \cdot (2 \cdot 2 - 1 \cdot 3) + 1 \cdot (2 \cdot 1 - (-1) \cdot 3) \\[6pt]
&= 1(-2 - 1) - 1(4 - 3) + 1(2 + 3) \\[6pt]
&= -3 - 1 + 5 \\[6pt]
&= 1
\end{align}
$$

Since the determinant is nonzero, the system has only the trivial solution:

$$
x = 0 \quad y = 0 \quad z = 0
$$

> This agrees with Cramer's rule. When $\det(A) \neq 0,$ every numerator $\det(A_k)$ has a column of zeros, so each $x_k = 0$ and the trivial solution is the only one.

## Example 2

We solve the following system of two linear equations in two unknowns:

$$
\begin{cases}
2x + 3y = 8 \\[6pt]
4x - y = 2
\end{cases}
$$

We identify the coefficient matrix $A$, the vector of unknowns $\mathbf{x}$, and the vector of constants $\mathbf{b}$:

$$
A = \begin{pmatrix}
2 & 3 \\[6pt]
4 & -1
\end{pmatrix}
\qquad
\mathbf{x} = \begin{pmatrix}
x \\[6pt]
y
\end{pmatrix}
\qquad
\mathbf{b} = \begin{pmatrix}
8 \\[6pt]
2
\end{pmatrix}
$$

The determinant of the coefficient matrix is:

$$
\det(A) = 2 \cdot (-1) - 3 \cdot 4 = -2 - 12 = -14
$$

Since it is nonzero, the system has exactly one solution and Cramer's rule applies.

We build $A_1$ by replacing the first column of $A$ with the constants:

$$
A_1 = \begin{pmatrix}
8 & 3 \\[6pt]
2 & -1
\end{pmatrix}
\qquad\rightarrow\qquad
\det(A_1) = 8 \cdot (-1) - 3 \cdot 2 = -8 - 6 = -14
$$

We build $A_2$ by replacing the second column of $A$ with the constants:

$$
A_2 = \begin{pmatrix}
2 & 8 \\[6pt]
4 & 2
\end{pmatrix}
\qquad\rightarrow\qquad
\det(A_2) = 2 \cdot 2 - 8 \cdot 4 = 4 - 32 = -28
$$

The unknowns follow from the formula:

$$
\begin{align}
x &= \frac{\det(A_1)}{\det(A)} = \frac{-14}{-14} = 1 \\[6pt]
y &= \frac{\det(A_2)}{\det(A)} = \frac{-28}{-14} = 2
\end{align}
$$

The solution of the system is:

$$
x = 1 \qquad y = 2
$$

> A solution of a linear system is an $n$-tuple that satisfies every equation at once. Here the pair $(x, y) = (1, 2)$ is the only one that satisfies both equations.
