---
title: Systems of Linear Equations
source: https://algebrica.org/systems-of-linear-equations/
license: CC BY-NC 4.0
tags:
  - augmented-matrix
  - coefficient-matrix
  - consistent-system
  - homogeneous-system
  - linear-algebra
  - linear-equations
  - linear-systems
  - matrix-representation
  - solution-set
---

## Definition and standard form

A linear system expresses several conditions on the same unknowns that must hold at the same time. Given $n$ variables $x_1, x_2, \dots, x_n,$ the system is linear when every equation is a [linear equation](../linear-equations/), so each variable appears to the first power and no products between variables occur. A linear system of $m$ equations in $n$ unknowns has the standard form:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = b_1 \\[6pt]
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = b_2 \\[6pt]
\quad\vdots \\[6pt]
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n = b_m
\end{cases}
$$

Each coefficient $a_{ij}$ is the value multiplying the variable $x_j$ in the $i$-th equation, and each $b_i$ is the constant term, also called the known term, on the right-hand side of the $i$-th equation.

## Solutions

Solving a linear system means finding an ordered $n$-tuple $(s_1, s_2, \dots, s_n)$ whose values satisfy every equation of the system at the same time. Consider the system:

$$
\begin{cases}
2x_1 - x_2 = 2 \\[6pt]
x_1 + x_2 = 1
\end{cases}
$$

The pair $(1, 0)$ is a solution: substituting $x_1 = 1$ and $x_2 = 0$ gives $2 \cdot 1 - 0 = 2$ in the first equation and $1 + 0 = 1$ in the second, so both hold. The pair $(0, 1)$ is not a solution, since it satisfies the second equation, $0 + 1 = 1,$ but not the first, where $2 \cdot 0 - 1 = -1 \neq 2.$ A tuple is a solution only when it satisfies every equation together.

Systems are classified by how many solutions they have:

+ A system is consistent, or possible, when at least one solution exists, and its equations are then compatible.
+ A system is inconsistent, or impossible, when no solution exists, and its equations are incompatible.
+ A consistent system is determined when it has exactly one solution.
+ A consistent system is undetermined when it has infinitely many solutions.

- - -

Each equation of a linear system describes a flat set in the space of the $n$ unknowns: a [line](../lines/) in two variables, a plane in three, and a hyperplane of dimension $n - 1$ in general. A [linear equation](../linear-equations/) imposes one such constraint, and a solution of the system lies on all of them at once, so the solution set is their intersection.

This picture matches the classification of the solutions. In the plane two lines meet at a single point, giving a determined system, or coincide along the same line, giving infinitely many solutions, or stay parallel without meeting, giving an inconsistent system. The same three outcomes recur for planes and hyperplanes in higher dimensions.

## Matrix representation

The coefficients and constants of a linear system can be arranged into [matrices](../matrices/), a compact notation on which the standard solution methods operate. Any system in standard form with $m$ equations and $n$ unknowns has an $m \times n$ coefficient matrix, built from the coefficients of the variables:

$$
A =
\begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\[6pt]
a_{21} & a_{22} & \cdots & a_{2n} \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}
$$

The variables and the constant terms form two column [vectors](../vectors/):

$$
X =
\begin{pmatrix}
x_1 \\[6pt]
x_2 \\[6pt]
\vdots \\[6pt]
x_n
\end{pmatrix}
\qquad
B =
\begin{pmatrix}
b_1 \\[6pt]
b_2 \\[6pt]
\vdots \\[6pt]
b_m
\end{pmatrix}
$$

With this notation the system becomes a single matrix equation:

$$
A \cdot X = B
$$

> In this compact form $A$ is the coefficient matrix, $X$ is the column vector of variables, and $B$ is the column vector of constants.

Placing the column of constants beside the coefficient matrix produces the augmented matrix, also called the complete matrix, written $(A \mid B)$:

$$
(A \mid B) =
\left(
\begin{array}{cccc|c}
a_{11} & a_{12} & \cdots & a_{1n} & b_1 \\[6pt]
a_{21} & a_{22} & \cdots & a_{2n} & b_2 \\[6pt]
\vdots & \vdots & \ddots & \vdots & \vdots \\[6pt]
a_{m1} & a_{m2} & \cdots & a_{mn} & b_m
\end{array}
\right)
$$

The vertical bar has no algebraic meaning. It marks where the coefficients end and the constants begin. The augmented matrix holds all the data of the system, and the standard solution methods act directly on it:

+ [Gaussian elimination](../gaussian-elimination/) reduces the augmented matrix by elementary row operations and applies to any number of equations and unknowns.
+ [Cramer's rule](../cramers-rule/) expresses each unknown as a ratio of determinants when the coefficient matrix is square and invertible.
+ The [Rouché-Capelli theorem](../rouche-capelli-theorem/) compares the [rank](../rank-of-a-matrix/) of the coefficient matrix with the rank of the augmented matrix to decide whether a system is consistent and how many free parameters its solutions depend on.

## Homogeneous systems

A system is homogeneous when all its constant terms are zero, that is $b_i = 0$ for every $i,$ so in matrix form it reads $A \cdot X = 0$:

$$
\begin{cases}
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = 0 \\[6pt]
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = 0 \\[6pt]
\quad\vdots \\[6pt]
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n = 0
\end{cases}
$$

Every linear system $A \cdot X = B$ has an associated homogeneous system $A \cdot X = 0,$ obtained by replacing the constant terms with zero while keeping the same coefficient matrix.

A homogeneous system is always consistent, because the zero tuple $(0, 0, \dots, 0),$ called the trivial solution, satisfies every equation. A homogeneous system therefore has either the trivial solution alone or infinitely many solutions. For a square system the trivial solution is the only one exactly when the coefficient matrix is invertible, that is when its [determinant](../determinant/) is nonzero, while a zero determinant produces nontrivial solutions. The general criterion, stated through matrix rank, belongs to the [Rouché-Capelli theorem](../rouche-capelli-theorem/).

## Existence and uniqueness of solutions

Whether a system has no solution, exactly one, or infinitely many depends on how the number of equations $m$ compares with the number of unknowns $n,$ together with the coefficient matrix:

+ A square system has $m = n.$ When its coefficient matrix is invertible, the system has exactly one solution, computed below with the inverse matrix.
+ An overdetermined system has $m > n,$ more equations than unknowns. The surplus equations may contradict one another, so an overdetermined system is often inconsistent.
+ An underdetermined system has $m < n,$ fewer equations than unknowns. When consistent, it has infinitely many solutions, since some unknowns stay free.

These are tendencies, not guarantees. The exact count follows from the [Rouché-Capelli theorem](../rouche-capelli-theorem/), which compares the [rank](../rank-of-a-matrix/) $r$ of the coefficient matrix with the rank of the augmented matrix $(A \mid B).$ A consistent system is determined when $r = n,$ and undetermined, with solutions depending on $n - r$ free parameters, when $r < n.$

If $X_0$ is one particular solution of $A \cdot X = B,$ every solution has the form:

$$
X = X_0 + Y
$$

where $Y$ ranges over the solutions of the associated homogeneous system $A \cdot X = 0,$ which form a [vector space](../vector-spaces/). The [Rouché-Capelli theorem](../rouche-capelli-theorem/) establishes this decomposition.

## Solving a square system with the inverse matrix

A square system with $n$ equations and $n$ unknowns can be solved with the [inverse matrix](../inverse-matrix/) when its coefficient matrix $A$ is nonsingular. If $\det(A) \neq 0,$ the matrix $A$ is invertible and the equation $A \cdot X = B$ has the unique solution:

$$
X = A^{-1}B
$$

The smallest case shows the method in full. Consider a system of two equations in two unknowns:

$$
\begin{cases}
3x_1 + x_2 = 5 \\[6pt]
x_1 + x_2 = 3
\end{cases}
$$

The coefficient matrix and the vector of constants are:

$$
A = \begin{pmatrix} 3 & 1 \\[6pt] 1 & 1 \end{pmatrix}
\qquad
B = \begin{pmatrix} 5 \\[6pt] 3 \end{pmatrix}
$$

The determinant is $\det(A) = 3 \cdot 1 - 1 \cdot 1 = 2,$ nonzero, so $A$ is invertible. For a $2 \times 2$ matrix the inverse swaps the two diagonal entries, negates the other two, and divides by the determinant:

$$
A^{-1} = \frac{1}{2}\begin{pmatrix} 1 & -1 \\[6pt] -1 & 3 \end{pmatrix}
$$

Multiplying this inverse by the vector of constants gives $X = A^{-1}B$:

$$
\begin{pmatrix} x_1 \\[6pt] x_2 \end{pmatrix}
=
\frac{1}{2}\begin{pmatrix} 1 & -1 \\[6pt] -1 & 3 \end{pmatrix}
\begin{pmatrix} 5 \\[6pt] 3 \end{pmatrix}
=
\frac{1}{2}\begin{pmatrix} 2 \\[6pt] 4 \end{pmatrix}
=
\begin{pmatrix} 1 \\[6pt] 2 \end{pmatrix}
$$

The system therefore has the unique solution $x_1 = 1$ and $x_2 = 2.$

- - -

We solve a linear system of three equations in three unknowns, so $n = m$:

$$
\begin{cases}
x_1 + x_2 + x_3 = 3 \\[6pt]
2x_1 + x_2 + x_3 = 4 \\[6pt]
2x_1 + x_2 + 3x_3 = 8
\end{cases}
$$

First we form the coefficient matrix $A$ and compute its determinant:

$$
A = \begin{pmatrix}
1 & 1 & 1 \\[6pt]
2 & 1 & 1 \\[6pt]
2 & 1 & 3
\end{pmatrix}
\qquad
\det(A) = -2
$$

> The section on [computing the determinant](../determinant/) of a square matrix sets out this method in full.

- - -

Since the determinant is nonzero, $A$ is nonsingular and its inverse exists:

$$
A^{-1} =
\begin{pmatrix}
-1 & 1 & 0 \\[6pt]
2 & -\dfrac{1}{2} & -\dfrac{1}{2} \\[6pt]
0 & -\dfrac{1}{2} & \dfrac{1}{2}
\end{pmatrix}
$$

> The section on the [inverse matrix](../inverse-matrix/) works through every step of this computation.

- - -

We now write the solution as $X = A^{-1}B$ and carry out the product:

$$
\begin{pmatrix}
x_1 \\[6pt]
x_2 \\[6pt]
x_3
\end{pmatrix}
=
\begin{pmatrix}
-1 & 1 & 0 \\[6pt]
2 & -\dfrac{1}{2} & -\dfrac{1}{2} \\[6pt]
0 & -\dfrac{1}{2} & \dfrac{1}{2}
\end{pmatrix}
\cdot
\begin{pmatrix}
3 \\[6pt]
4 \\[6pt]
8
\end{pmatrix}
$$

Multiplying the inverse by the vector of constants row by row gives the three unknowns:

$$
\begin{align}
x_1 &= -1 \cdot 3 + 1 \cdot 4 + 0 \cdot 8 = 1 \\[6pt]
x_2 &= 2 \cdot 3 - \dfrac{1}{2} \cdot 4 - \dfrac{1}{2} \cdot 8 = 0 \\[6pt]
x_3 &= 0 \cdot 3 - \dfrac{1}{2} \cdot 4 + \dfrac{1}{2} \cdot 8 = 2
\end{align}
$$

The system therefore has the unique solution:

$$
x_1 = 1 \qquad x_2 = 0 \qquad x_3 = 2
$$

## Example with infinitely many solutions

We solve a system of two equations in three unknowns, so $m < n$:

$$
\begin{cases}
x_1 + x_2 + x_3 = 2 \\[6pt]
2x_1 + x_2 - x_3 = 3
\end{cases}
$$

The coefficient matrix has rank $2,$ so by the [Rouché-Capelli theorem](../rouche-capelli-theorem/) the solutions depend on $n - r = 3 - 2 = 1$ free parameter. We take $x_3 = t$ as the free unknown and move it to the right-hand side:

$$
\begin{cases}
x_1 + x_2 = 2 - t \\[6pt]
2x_1 + x_2 = 3 + t
\end{cases}
$$

Subtracting the first equation from the second gives $x_1 = 1 + 2t,$ and substituting this back into the first gives $x_2 = 1 - 3t.$ The [Gaussian elimination](../gaussian-elimination/) page carries out this kind of reduction systematically.

The solutions form a one-parameter family, which separates into a constant part and a multiple of a fixed vector:

$$
X =
\begin{pmatrix}
1 + 2t \\[6pt]
1 - 3t \\[6pt]
t
\end{pmatrix}
=
\begin{pmatrix}
1 \\[6pt]
1 \\[6pt]
0
\end{pmatrix}
+
t
\begin{pmatrix}
2 \\[6pt]
-3 \\[6pt]
1
\end{pmatrix}
\qquad t \in \mathbb{R}
$$

Setting $t = 0$ gives the particular solution $X_0 = (1, 1, 0),$ while the vector $(2, -3, 1)$ solves the associated homogeneous system $A \cdot X = 0.$ As $t$ ranges over $\mathbb{R}$ it produces every solution of that homogeneous system. This family is the decomposition $X = X_0 + Y$ introduced above. Geometrically the solution set is a [line in vector form](../vector-and-parametric-equations-of-a-line/) through $X_0$ with direction $(2, -3, 1).$
