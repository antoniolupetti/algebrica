# Linear Equations with Parameters

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/linear-equations-with-parameters/

## Definition

A first-degree [linear equation](../linear-equations/) involving parameters is an equation in which the unknown variable appears only to the first power, while some of the coefficients are represented by symbolic quantities rather than fixed numbers. A general form of such an equation is:

\\[
a x + b = c
\\]

+ \\(x\\) is the variable to be determined
+ \\(a\\), \\(b\\), and \\(c\\) are parameters. These parameters may take different real values, and their specific choice influences how the equation behaves and whether a solution exists.

One way to interpret this structure is to view each triple \\((a, b, c)\\) as selecting a particular instance of the equation. Changing the parameters modifies the balance between the terms and can turn the equation into a typical linear relation, an identity, or even an inconsistency. The leading coefficient \\(a\\) is especially important: when it is nonzero, the equation defines a unique value for \\(x\\); when it is zero, the expression reduces to a constant statement whose truth depends only on \\(b\\) and \\(c\\).

This parametric perspective makes it possible to study not just a single equation, but an entire family of linear equations at once, highlighting how algebraic structure shifts as the parameters vary.

> This page focuses on the linear case. For a broader discussion of parametric equations across different degrees, see [equations with parameters](../equations-with-parameters/).

- - -
## Classification of cases

For the parametric linear equation \\(a x + b = c\\) all possible behaviours can be reduced to three fundamental situations:

+ \\(a \neq 0\\): the equation admits a unique solution.
+ \\(a = 0\\) and \\(b = c\\): the equation is an identity, satisfied for every real \\(x\\).
+ \\(a = 0\\) and \\(b \neq c\\): the equation is a contradiction, with no solution.

> These three cases cover the entire family of first-degree equations with parameters and allow the structure of the equation to be analysed systematically.

- - -

When the leading coefficient satisfies \\(a \neq 0\\), the equation behaves as a standard linear relation. In this case the variable \\(x\\) can be isolated directly, giving:

\\[
x = \frac{c - b}{a}
\\]

This expression provides a single real solution for every choice of parameters with \\(a \neq 0\\).

- - -

When \\(a = 0\\), the term containing \\(x\\) disappears and the equation becomes the constant statement:

\\[
b = c
\\]

At this point the presence or absence of solutions depends entirely on the relationship between \\(b\\) and \\(c\\). When \\(b = c\\), the statement holds for every real \\(x\\), and the equation is an identity. When \\(b \neq c\\), the statement is false and no solution exists.

- - -

A compact summary of the three fundamental situations can be written as follows. Each condition on the parameters determines a different algebraic behaviour, ranging from a fully determined equation to an identity or a contradiction:

\\[
a x + b = c
\quad\rightarrow\quad
\begin{cases}
a = 0,\\; b = c 
& \\; x \in \mathbb{R} \\\\[10pt]
a = 0,\\; b \neq c 
& \\; \varnothing \\\\[5pt]
a \neq 0, \\; \forall \\; b, c
& \\; x = \dfrac{c - b}{a}
\end{cases}
\\]

This classification captures all possible outcomes for a linear equation with parameters and shows how different choices of \\(a\\), \\(b\\), and \\(c\\) affect the existence and uniqueness of the solution.

- - -
## Example 1

In practice, the parameters need not be independent: a single real quantity, commonly denoted \(k\), may appear simultaneously in several coefficients, and the classification above applies by treating that quantity as the free parameter. As a concrete illustration of the general classification, consider the parametric equation

\\[
(a - 1)x = \frac{1}{c}
\\]

Before analysing its solutions, we observe that the right-hand side is defined only when \\(c \neq 0.\\) This condition is required for the equation to be meaningful in the real numbers. Once this requirement is satisfied, the behaviour of the equation depends on the value of the coefficient \\(a - 1\\):

\\[
(a - 1)x = \frac{1}{c}
\quad\rightarrow\quad
\begin{cases}
c = 0 
& \\text{undefined} \\\\[10pt]
c \neq 0,\\; a = 1 
& \varnothing \\\\[10pt]
c \neq 0,\\; a \neq 1 
& x = \dfrac{1}{c(a - 1)}
\end{cases}
\\]

From the analysis of the possible cases, we obtain:

+ If \\(c = 0\\), the quantity \\(1/c\\) is not defined and the equation loses meaning.  
+ If \\(c \neq 0\\) and \\(a = 1\\), the coefficient of \\(x\\) vanishes and the equation becomes the false statement \\(0 = 1/c\\).  
+ If \\(c \neq 0\\) and \\(a \neq 1\\), the equation remains linear and admits a single solution.

This example highlights how changing the parameters can alter the nature of the equation itself, showing how a linear relation may shift from being undefined to impossible or uniquely solvable depending on their values.

- - -
## Example 2

Let us now examine a simple linear equation that depends on a real parameter. Consider the problem of solving:

\\[
(2k - 3)x + (k + 1) = 4
\\]

where \\(k \in \mathbb{R}\\). The equation behaves as an ordinary [linear equation](../linear-equations/) as long as the coefficient of \\(x\\) does not vanish. This coefficient is \\(2k - 3\\), so the equation is solvable in the usual way whenever:

\\[
2k - 3 \neq 0
\quad\longrightarrow\quad
k \neq \frac{3}{2}
\\]

- - -

Under this condition, isolating the variable gives:

\\[
x = \frac{4 - (k + 1)}{2k - 3}
   = \frac{3 - k}{2k - 3}
\\]

If instead the parameter takes the value \\(k = \frac{3}{2}\\), the coefficient of \\(x\\) becomes zero and the equation reduces to a constant statement:

\\[
k + 1 = 4
\\]

Since \\(k = \frac{3}{2}\\), the left-hand side evaluates to \\(\frac{3}{2} + 1 = \frac{5}{2}\\), which is not equal to \\(4\\). The statement is therefore false.

Therefore, in this case no real value of \\(x\\) can satisfy the equation. Summarising the two possible situations we obtain:

\\[
\begin{cases}
k = \tfrac{3}{2} 
& \varnothing \\\\[8pt]
k \neq \tfrac{3}{2} 
& x = \dfrac{3 - k}{2k - 3}
\end{cases}
\\]

- - -
## Example 3

Consider the linear equation:

\\[
(k + 4)x = 2k - 1 \quad k \in \mathbb{R}
\\]

The equation is well defined for every \\(k\\) except when the coefficient of \\(x\\) becomes zero. Thus the only value that requires special attention is:

\\[
k + 4 = 0
\quad\longrightarrow\quad
k = -4
\\]

For all other values of \\(k\\), the equation can be solved directly:

\\[
x = \frac{2k - 1}{k + 4}
\\]

Since the right-hand side is a real expression whenever \\(k \neq -4\\), the equation admits a real solution for every parameter in:

\\[
k \in \mathbb{R} \setminus \\{-4\\}
\\]

If the parameter takes the value \\(k = -4\\), the equation becomes:

\\[
0 \cdot x = -9
\\]

which is a contradiction and therefore has no solution.

In summary we have:

\\[
\begin{cases}
k = -4 
& \varnothing \\\\[8pt]
k \neq -4 
& x = \dfrac{2k - 1}{k + 4}\\;\in\\;\mathbb{R}
\end{cases}
\\]
