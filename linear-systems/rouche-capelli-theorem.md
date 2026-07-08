---
title: Rouché-Capelli Theorem
source: https://algebrica.org/rouche-capelli-theorem/
license: CC BY-NC 4.0
tags:
  - augmented-matrix
  - coefficient-matrix
  - consistent-system
  - homogeneous-system
  - linear-algebra
  - linear-systems
  - rank
  - rouche-capelli-theorem
  - solution-set
---

## Statement of the theorem

The Rouché-Capelli theorem characterizes the solvability of a [linear system](../systems-of-linear-equations/) in terms of two matrix invariants, the [rank](../rank-of-a-matrix/) of the coefficient matrix and the rank of the augmented matrix. Consider a linear system of $m$ equations in $n$ unknowns written in matrix form:

$$
A\mathbf{x} = \mathbf{b}
$$

Here $A \in M_{m,n}(\mathbb{R})$ is the coefficient [matrix](../matrices/), $\mathbf{x} \in \mathbb{R}^n$ is the column [vector](../vectors/) of unknowns, and $\mathbf{b} \in \mathbb{R}^m$ is the column vector of constant terms. The augmented matrix $A \mid \mathbf{b}$ is obtained by appending $\mathbf{b}$ as an additional column to $A$, producing a matrix of size $m \times (n+1)$.

Let $S$ be a linear system of $m$ equations in $n$ unknowns with coefficient matrix $A$ and augmented matrix $A \mid \mathbf{b}$. Then:

+ the system $S$ is consistent if and only if $r(A) = r(A \mid \mathbf{b})$;
+ when $S$ is consistent and $r(A) = r(A \mid \mathbf{b}) = r$, the system admits a unique solution if $r = n$, and infinitely many solutions depending on $n - r$ free parameters if $r < n$;
+ when $S$ is consistent, its solutions are the vectors $\mathbf{x} = \mathbf{x}_0 + \mathbf{y}$, where $\mathbf{x}_0$ is any fixed solution and $\mathbf{y}$ runs over the solutions of the associated homogeneous system $A\mathbf{y} = \mathbf{0}$.

The first part is a consistency criterion formulated in terms of the rank alone. The second part counts the solutions of a consistent system, and identifies the number of free parameters with the difference $n - r$ between the number of unknowns and the common rank. The third part describes the solution set. Once a single solution $\mathbf{x}_0$ is known, every other solution differs from it by a solution of the homogeneous system, so the solution set is the translate of the homogeneous solution space by $\mathbf{x}_0$.

> When $A$ is square and the [determinant](../determinant/) is nonzero, the system has rank $n$ and is solved in closed form through the [inverse matrix](../inverse-matrix/) as $\mathbf{x} = A^{-1}\mathbf{b},$ or unknown by unknown through [Cramer's rule](../cramers-rule/). The vanishing of the determinant is the algebraic counterpart of the rank deficiency that this theorem detects.

## Geometric interpretation

The condition $r(A) = r(A \mid \mathbf{b})$ can be read through the [linear combinations](../linear-combinations/) of the columns of $A$. Denote by $C_1, C_2, \ldots, C_n \in \mathbb{R}^m$ the columns of $A$. The matrix-vector product can be written as:

$$
A\mathbf{x} = x_1 C_1 + x_2 C_2 + \cdots + x_n C_n
$$

Solving the system therefore amounts to expressing $\mathbf{b}$ as a linear combination of the columns of $A$. Such an expression exists precisely when $\mathbf{b}$ belongs to the [column space](../vector-spaces/) of $A$, which happens exactly when adjoining $\mathbf{b}$ to the columns of $A$ does not enlarge the column space. Since the dimension of the column space equals the rank, this last condition is exactly $r(A) = r(A \mid \mathbf{b}).$

> The rank equality is therefore a test of whether $\mathbf{b}$ lies in the subspace spanned by the columns of $A$. When the equality fails, $\mathbf{b}$ lies outside that subspace, no linear combination of the columns can produce it, and the system has no solution.

## Proof of the theorem

The consistency part of the theorem can be proved by reducing the system to row echelon form via [Gaussian elimination](../solving-linear-systems-using-gaussian-elimination/) and analyzing the position of the pivots in the reduced matrix.

We apply elementary row operations to the augmented matrix $A \mid \mathbf{b}$ until a row echelon form $\tilde{A} \mid \tilde{\mathbf{b}}$ is obtained. The same operations transform $A$ into a row echelon matrix $\tilde{A}$, since the coefficient block is unaffected by the column appended on the right. Elementary row operations preserve the rank, so the following equalities hold:

$$
r(A) = r(\tilde{A}), \qquad r(A \mid \mathbf{b}) = r(\tilde{A} \mid \tilde{\mathbf{b}})
$$

Moreover, the original system $S$ and the reduced system $\tilde{S}$ defined by $\tilde{A} \mid \tilde{\mathbf{b}}$ have the same set of solutions, because each elementary row operation leaves the solution set unchanged. Swapping two equations or multiplying one by a nonzero scalar produces an equivalent system, and adding a multiple of one equation to another neither creates nor destroys solutions. The proof therefore reduces to verifying the consistency criterion for systems already in row echelon form.

A system in row echelon form is inconsistent if and only if the reduced augmented matrix contains a row of the form $(0, 0, \ldots, 0 \mid c)$ with $c \neq 0$, since such a row corresponds to the impossible equation $0 = c$. The presence of such a row is equivalent to the existence of a pivot in the last column of $\tilde{A} \mid \tilde{\mathbf{b}}$, namely a pivot that does not belong to $\tilde{A}$. When such a pivot exists, the augmented matrix has exactly one more pivot than the coefficient matrix, so:

$$
r(\tilde{A} \mid \tilde{\mathbf{b}}) = r(\tilde{A}) + 1
$$

When no such pivot exists, all pivots of $\tilde{A} \mid \tilde{\mathbf{b}}$ lie inside $\tilde{A}$, and the two matrices have the same rank. Consistency of $\tilde{S}$ is therefore equivalent to the equality:

$$
r(\tilde{A}) = r(\tilde{A} \mid \tilde{\mathbf{b}})
$$

Combining this with the rank equalities above, the original system $S$ is consistent if and only if $r(A) = r(A \mid \mathbf{b})$, which is the desired statement.

The second part of the theorem follows from the same row echelon analysis. When the reduced system is consistent and has $r$ pivots, the variables associated with the pivot columns can be expressed in terms of the remaining $n - r$ variables, which act as free parameters. This produces a unique solution exactly when $n - r = 0$, and an $(n-r)$-parameter family of solutions otherwise.

The third part describes the solution set once consistency is granted. Fix a particular solution $\mathbf{x}_0$, so that $A\mathbf{x}_0 = \mathbf{b}$, and let $\mathbf{x}$ be any other solution. Their difference $\mathbf{y} = \mathbf{x} - \mathbf{x}_0$ satisfies:

$$
A\mathbf{y} = A(\mathbf{x} - \mathbf{x}_0) = A\mathbf{x} - A\mathbf{x}_0 = \mathbf{b} - \mathbf{b} = \mathbf{0}
$$

so $\mathbf{y}$ solves the associated homogeneous system. Conversely, if $\mathbf{y}$ satisfies $A\mathbf{y} = \mathbf{0}$, then:

$$
A(\mathbf{x}_0 + \mathbf{y}) = A\mathbf{x}_0 + A\mathbf{y} = \mathbf{b} + \mathbf{0} = \mathbf{b}
$$

so $\mathbf{x}_0 + \mathbf{y}$ is again a solution. Every solution therefore has the form $\mathbf{x}_0 + \mathbf{y}$ with $\mathbf{y}$ in the solution set of the homogeneous system, which proves the third part.

## Example 1

The following system illustrates the case of a unique solution:

$$
\begin{cases}
3x - y = 7 \\[6pt]
x + 2y = 0
\end{cases}
$$

The coefficient matrix and the augmented matrix are:

$$
A \mid \mathbf{b} = \begin{pmatrix} 3 & -1 & 7 \\[6pt] 1 & \phantom{-}2 & 0 \end{pmatrix}
$$

Since $\det(A) = 3 \cdot 2 - (-1) \cdot 1 = 7 \neq 0$, the rank of $A$ is $2$, the maximum possible. The augmented matrix has at most rank $2$ and contains $A$ as a submatrix of rank $2$, so its rank is also $2$. The Rouché-Capelli theorem then guarantees consistency, and because $r = n = 2$ the solution is unique. To find it, we use the second equation to write $x = -2y$, and substitute into the first equation to obtain $3(-2y) - y = 7$, which gives $y = -1.$ Substituting back yields $x = 2.$ The system therefore admits the unique solution $(x, y) = (2, -1).$

## Example 2

The following system illustrates the case of infinitely many solutions:

$$
\begin{cases}
x_1 + x_2 - x_3 + 2x_4 = 1 \\[6pt]
2x_1 + 2x_2 + x_3 + x_4 = 5 \\[6pt]
x_1 + x_2 + x_4 = 2
\end{cases}
$$

The augmented matrix is:

$$
A \mid \mathbf{b} = \begin{pmatrix}
1 & 1 & -1 & 2 & 1 \\[6pt]
2 & 2 & \phantom{-}1 & 1 & 5 \\[6pt]
1 & 1 & \phantom{-}0 & 1 & 2
\end{pmatrix}
$$

Reducing to row echelon form by replacing the second row with $R_2 - 2R_1$ and the third row with $R_3 - R_1$ gives:

$$
\begin{pmatrix}
1 & 1 & -1 & \phantom{-}2 & 1 \\[6pt]
0 & 0 & \phantom{-}3 & -3 & 3 \\[6pt]
0 & 0 & \phantom{-}1 & -1 & 1
\end{pmatrix}
$$

A further step $R_2 \to \tfrac{1}{3} R_2$ followed by $R_3 \to R_3 - R_2$ produces:

$$
\begin{pmatrix}
1 & 1 & -1 & \phantom{-}2 & 1 \\[6pt]
0 & 0 & \phantom{-}1 & -1 & 1 \\[6pt]
0 & 0 & \phantom{-}0 & \phantom{-}0 & 0
\end{pmatrix}
$$

The reduced coefficient matrix and the reduced augmented matrix both have two pivots, located in the first and third columns. Therefore $r(A) = r(A \mid \mathbf{b}) = 2$, and the system is consistent. Since $n = 4$ and $r = 2$, the theorem predicts a family of solutions depending on two free parameters. Treating $x_2$ and $x_4$ as parameters, the second pivot equation gives $x_3 = 1 + x_4$, and the first pivot equation gives $x_1 = 1 - x_2 + x_3 - 2 x_4 = 2 - x_2 - x_4$. The complete solution set is therefore described by:

$$
\begin{cases}
x_1 = 2 - x_2 - x_4 \\[6pt]
x_3 = 1 + x_4
\end{cases}
$$

with $x_2, x_4 \in \mathbb{R}$ arbitrary. Collecting the parameters exhibits the structure predicted by the third part of the theorem:

$$
\begin{pmatrix} x_1 \\[6pt] x_2 \\[6pt] x_3 \\[6pt] x_4 \end{pmatrix}
= \begin{pmatrix} 2 \\[6pt] 0 \\[6pt] 1 \\[6pt] 0 \end{pmatrix}
+ x_2 \begin{pmatrix} -1 \\[6pt] \phantom{-}1 \\[6pt] \phantom{-}0 \\[6pt] \phantom{-}0 \end{pmatrix}
+ x_4 \begin{pmatrix} -1 \\[6pt] \phantom{-}0 \\[6pt] \phantom{-}1 \\[6pt] \phantom{-}1 \end{pmatrix}
$$

The first vector is the particular solution obtained for $x_2 = x_4 = 0$, and the other two solve the homogeneous system $A\mathbf{x} = \mathbf{0}$. The solution set is their span translated by the particular solution, a two-dimensional affine subspace of $\mathbb{R}^4$, in agreement with the value $n - r = 2$ given by the theorem.

## Example 3

The following system illustrates the case of an inconsistent system:

$$
\begin{cases}
x + 2y + z = 1 \\[6pt]
2x + y + 3z = 1 \\[6pt]
3x + 3y + 4z = 0
\end{cases}
$$

The coefficient matrix is:

$$
A = \begin{pmatrix}
1 & 2 & 1 \\[6pt]
2 & 1 & 3 \\[6pt]
3 & 3 & 4
\end{pmatrix}
$$

The third row is the sum of the first two, so the rows are linearly dependent and $\det(A) = 0$. Consequently $r(A) < 3$. The submatrix formed by the first two rows and the first two columns has determinant $1 \cdot 1 - 2 \cdot 2 = -3$, which is nonzero, confirming that $r(A) = 2$. The augmented matrix is:

$$
A \mid \mathbf{b} = \begin{pmatrix}
1 & 2 & 1 & 1 \\[6pt]
2 & 1 & 3 & 1 \\[6pt]
3 & 3 & 4 & 0
\end{pmatrix}
$$

The third row of $A \mid \mathbf{b}$ is no longer the sum of the first two, since the constant column gives $1 + 1 = 2 \neq 0$. To confirm that the rank has increased, we compute the $3 \times 3$ minor formed by the first, second, and fourth columns:

$$
\det \begin{pmatrix}
1 & 2 & 1 \\[6pt]
2 & 1 & 1 \\[6pt]
3 & 3 & 0
\end{pmatrix} = 3 \cdot (2 - 1) - 3 \cdot (1 - 2) + 0 = 3 + 3 = 6
$$

The minor is nonzero, so $r(A \mid \mathbf{b}) = 3$. Since $r(A) = 2 \neq 3 = r(A \mid \mathbf{b})$, the system is inconsistent by the Rouché-Capelli theorem.

## Discussion of a parametric system

When the coefficients of a system depend on a [parameter](../linear-equations-with-parameters/), the rank can change with the parameter, and with it the classification of the solutions. Consider the system:

$$
\begin{cases}
k x + 2 y = 2 \\[6pt]
3 x + (k+1) y = 3
\end{cases}
$$

with parameter $k \in \mathbb{R}$. The coefficient matrix is:

$$
A = \begin{pmatrix} k & 2 \\[6pt] 3 & k+1 \end{pmatrix}
$$

and its determinant is:

$$
\det(A) = k(k+1) - 6 = k^2 + k - 6 = (k - 2)(k + 3)
$$

which vanishes precisely for $k = 2$ and $k = -3$. For every other value of $k$ the determinant is nonzero, so $r(A) = 2$. The augmented matrix has at most rank $2$ and already contains $A$ as a submatrix of rank $2$, hence $r(A \mid \mathbf{b}) = 2$ as well. The Rouché-Capelli theorem then yields a unique solution.

For $k = 2$ the substitution gives:

$$
A = \begin{pmatrix} 2 & 2 \\[6pt] 3 & 3 \end{pmatrix}, \qquad A \mid \mathbf{b} = \begin{pmatrix} 2 & 2 & 2 \\[6pt] 3 & 3 & 3 \end{pmatrix}
$$

Both equations reduce to $x + y = 1$, so $r(A) = r(A \mid \mathbf{b}) = 1$. The system is consistent and admits a one-parameter family of solutions of the form $(x, y) = (1 - t, t)$ with $t \in \mathbb{R}.$

For $k = -3$ the substitution gives:

$$
A = \begin{pmatrix} -3 & \phantom{-}2 \\[6pt] \phantom{-}3 & -2 \end{pmatrix}, \qquad A \mid \mathbf{b} = \begin{pmatrix} -3 & \phantom{-}2 & 2 \\[6pt] \phantom{-}3 & -2 & 3 \end{pmatrix}
$$

The second row of $A$ is the opposite of the first, so $r(A) = 1$. For the augmented matrix, however, the minor formed by the first and third columns has determinant:

$$
\det \begin{pmatrix} -3 & 2 \\[6pt] \phantom{-}3 & 3 \end{pmatrix} = -9 - 6 = -15
$$

which is nonzero, so $r(A \mid \mathbf{b}) = 2$. The two ranks differ, so the system is inconsistent. In summary, the system admits a unique solution when $k \neq 2$ and $k \neq -3$, infinitely many solutions when $k = 2$, and no solution when $k = -3$.

## Homogeneous systems

A homogeneous linear system has the form:

$$
A\mathbf{x} = \mathbf{0}
$$

The augmented matrix differs from $A$ only by a column of zeros, which cannot increase the rank. Consequently $r(A) = r(A \mid \mathbf{0})$ always holds, and the Rouché-Capelli theorem implies that every homogeneous system is consistent. The zero vector $\mathbf{x} = \mathbf{0}$ is always a solution, called the trivial solution.

The theorem also describes when nontrivial solutions exist. If $r(A) = n$, the system admits only the trivial solution. If $r(A) < n$, the solution set forms an $(n - r)$-parameter family, and in particular contains nonzero vectors. This gives a criterion for the existence of nontrivial solutions:

> A homogeneous system $A\mathbf{x} = \mathbf{0}$ admits nontrivial solutions if and only if $r(A) < n.$

For square systems, where $m = n$, this condition becomes $\det(A) = 0.$ For systems with fewer equations than unknowns, that is $m < n$, the rank cannot exceed $m$ and is therefore strictly less than $n$; such systems always admit nontrivial solutions.
