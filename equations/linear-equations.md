# Linear Equations

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/linear-equations/

## Definition

A linear equation in the unknowns \\(x_1, x_2, \ldots, x_n\\) is an algebraic [equation](../equations/) of degree one, in which each variable appears with exponent equal to \\(1\\) and never multiplied by another variable. Its standard form is:

\\[
a_1x_1 + a_2x_2 + \ldots + a_nx_n = b
\\]

+ \\(x_1, x_2, \ldots, x_n \in \mathbb{R}\\) are the unknowns.
+ \\(a_1, a_2, \ldots, a_n \in \mathbb{R}\\) are the coefficients, with at least one \\(a_i \neq 0\\).
+ \\(b \in \mathbb{R}\\) is the constant term.
+ When \\(b = 0\\), the equation is called homogeneous.

The adjective linear refers to a precise algebraic property of the left-hand side. If we denote it by:

\\[L(x_1, \ldots, x_n) = a_1x_1 + \ldots + a_nx_n\\] 

then \\(L\\) satisfies the two defining properties of linearity:

\\[L(x + y) = L(x) + L(y)\\]
\\[L(\lambda x) = \lambda \\, L(x)\\]

These two identities are the algebraic counterpart of what, geometrically, makes the solution set a line, a plane, or more generally a hyperplane. The same notion of linearity underlies vector spaces and linear maps, and explains why linear equations occupy such a central role in mathematics. 

A linear equation may involve any finite number of unknowns. The expression \\(ax + by + c = 0\\), for example, is a linear equation in the two variables \\(x\\) and \\(y\\), with constant term \\(-c\\) once written in standard form.

> Linear equations are the foundation on which [systems of linear equations](../systems-of-linear-equations/) and [matrix](../matrices/) calculus are built, and they provide the language in which problems involving several unknowns can be formulated and solved simultaneously.

- - -
## Type of solution

The geometric nature of the solution set of a linear equation depends on the number of unknowns and on whether the equation is homogeneous. In every case the solution set is an affine subspace of \\(\mathbb{R}^n\\), that is, a translate of a linear subspace, and its dimension equals \\(n - 1\\) when the equation is non-degenerate.

+ With one unknown, the solution reduces to a single point on the real line.
+ With two unknowns, the solutions form a [line](../lines/) in the plane, passing through the origin if the equation is homogeneous.
+ With three unknowns, they form a plane in space, again through the origin in the homogeneous case.
+ With \\(n > 3\\) unknowns, the solution set is a hyperplane of \\(\mathbb{R}^n\\), namely an affine subspace of dimension \\(n - 1\\).

> The drop in dimension by exactly one reflects the fact that a single linear equation imposes one scalar constraint on the \\(n\\) unknowns. Imposing further independent linear conditions corresponds to intersecting hyperplanes, and leads naturally to the theory of [systems of linear equations](../systems-of-linear-equations/).

- - -
## Linear equations in one variable

A linear equation in one unknown can always be reduced, through elementary algebraic manipulations, to the standard form:

\\[
ax = b
\\]

The behaviour of this equation depends entirely on the coefficients \\(a\\) and \\(b\\). Three cases need to be distinguished.

When \\(a \neq 0\\), the equation admits one and only one solution, obtained by dividing both sides by \\(a\\):

\\[
x = \frac{b}{a}
\\]

This is the situation contemplated by the standard definition, which requires at least one coefficient to be non-zero. The remaining two cases arise only when the original equation, after simplification, collapses into the degenerate form \\(0 \cdot x = b\\), and they reveal the boundary between a genuine linear equation and a relation that no longer depends on the unknown.

When \\(a = 0\\) and \\(b = 0\\), the equation becomes \\(0 = 0\\), an identity satisfied by every real number. The solution set is the whole of \\(\mathbb{R}\\) and the equation is called indeterminate.

When \\(a = 0\\) and \\(b \neq 0\\), the equation reduces to \\(0 = b\\), a contradiction with no solution. The solution set is empty and the equation is called impossible.

The three cases above are not abstract curiosities. They appear systematically when the coefficients depend on one or more real parameters, giving rise to [linear equations with parameters](../linear-equations-with-parameters/) of the form \\(a(k)\, x = b(k)\\). The values of \\(k\\) for which \\(a(k) = 0\\) are precisely those that switch the equation between the determinate, indeterminate, and impossible regimes, and identifying them is the central problem in the parametric setting.

- - -
## Example 1

Consider the equation:

\\[
2x + 3 = 11x
\\]

The unknown \\(x\\) ranges over the whole set of [real numbers](../types-of-number/), without restrictions on its [domain](../determining-the-domain-of-a-function/). To solve the equation we move all terms containing \\(x\\) to one side and the constants to the other, reducing it to the standard form \\(ax = b\\):

\\[
\begin{align}
2x + 3 &= 11x \\\\[6pt]
2x - 11x &= -3 \\\\[6pt]
-9x &= -3
\end{align}
\\]

The coefficient of the unknown is \\(-9 \neq 0\\), so the equation falls under the determinate case and admits one and only one solution. Dividing both sides by \\(-9\\) we obtain:

\\[
x = \frac{-3}{-9} = \frac{1}{3}
\\]

To verify the result we substitute \\(x = 1/3\\) into the original equation and check that both sides yield the same value:

\\[
\begin{align}
2 \left( \frac{1}{3} \right) + 3 &= 11 \left( \frac{1}{3} \right) \\\\[6pt]
\frac{2}{3} + \frac{9}{3} &= \frac{11}{3} \\\\[6pt]
\frac{11}{3} &= \frac{11}{3}
\end{align}
\\]

The identity is confirmed, and the unique solution of the equation is:

\\[ x = \frac{1}{3} \\]

- - --
## Linear equations in two variables

A linear equation in two unknowns has the standard form:

\\[
ax + by = c
\\]

with \\(a, b, c \in \mathbb{R}\\) and at least one between \\(a\\) and \\(b\\) different from zero. Geometrically, its solution set is a straight [line](../lines/) in the Cartesian plane, and the equation is the implicit representation of that line. The constant term \\(c\\) determines the position of the line: when \\(c \neq 0\\) the line does not pass through the origin, while when \\(c = 0\\) the equation reduces to the homogeneous form and the corresponding line passes through the origin.

The general solution can be obtained by treating one of the unknowns as a free parameter. Assuming \\(b \neq 0\\) and setting \\(x = \lambda\\), the equation gives:

\\[
y = \frac{c - a \lambda}{b}, \qquad \lambda \in \mathbb{R}
\\]

Each value of the parameter \\(\lambda\\) produces a point of the plane lying on the line, and as \\(\lambda\\) varies over \\(\mathbb{R}\\) the entire line is described. The role of \\(\lambda\\) and that of the unknown chosen as free can be exchanged, with no effect on the geometric content of the solution.

> The same equation \\(ax + by = c\\) may be rewritten in the explicit form \\(y = mx + q\\) whenever \\(b \neq 0\\), with slope \\(m = -a/b\\) and intercept \\(q = c/b\\). The implicit form is more general because it also accommodates vertical lines, those with \\(b = 0\\), which cannot be expressed in explicit form. 

When \\(c = 0\\) the equation becomes:

\\[
ax + by = 0
\\]

and represents a line through the origin. The set of its solutions is a one-dimensional vector subspace of \\(\mathbb{R}^2\\), spanned by any non-zero vector orthogonal to the coefficient vector \\((a, b)\\). A particularly symmetric parametrisation, which makes the structure transparent, is:

\\[
x = \lambda b, \qquad y = -\lambda a, \qquad \lambda \in \mathbb{R}
\\]

The pair \\((b, -a)\\) is indeed a solution of the equation, since \\(a b + b(-a) = 0\\), and every other solution is a scalar multiple of it. This is a first concrete instance of a phenomenon that runs through the whole theory: the solutions of a homogeneous linear equation form a vector subspace, while those of the corresponding non-homogeneous equation form an affine subspace obtained by translation.

- - -
## Example 2

Consider the homogeneous linear equation:

\\[
2x - 3y = 0
\\]

The coefficients are \\(a = 2\\) and \\(b = -3\\), so the equation represents a line through the origin in the Cartesian plane. Solving for \\(y\\) we obtain the explicit form:

\\[
y = \frac{2}{3} x
\\]

which shows that the line has slope \\(2/3\\). Every solution \\((x, y)\\) of the equation satisfies this relation, and the entire solution set can be described by introducing a real parameter \\(\lambda\\) and writing:

\\[
x = \lambda, \qquad y = \frac{2}{3} \lambda, \qquad \lambda \in \mathbb{R}
\\]

The same line admits the symmetric parametrisation \\(x = \lambda b = -3 \lambda\\), \\(y = -\lambda a = -2 \lambda\\) introduced in the general discussion. The two descriptions differ only by a rescaling of the parameter and produce the same set of points: the substitution \\(\lambda \mapsto -3 \lambda\\) maps the second parametrisation onto the first.

Choosing arbitrary values of \\(\lambda\\), for instance \\(\lambda = 3\\) and \\(\lambda = -6\\) (any real number would do), we obtain specific points on the line:

+ for \\(\lambda = 3\\), the pair \\((x, y) = (3, 2)\\);
+ for \\(\lambda = -6\\), the pair \\((x, y) = (-6, -4)\\).

A direct substitution into the original equation confirms that both pairs satisfy it.

The diagram shows the line of equation \\(2x - 3y = 0\\) together with the two points just computed.

The solution set of the equation \\(2x - 3y = 0\\) is the line through the origin of equation: 

\\[y = \tfrac{2}{3} x\\]

- - -
## Linear equations in three variables

A linear equation in three unknowns has the standard form:

\\[
ax + by + cz = d
\\]

with \\(a, b, c, d \in \mathbb{R}\\) and at least one between \\(a\\), \\(b\\), and \\(c\\) different from zero. Geometrically, its solution set is a plane in three-dimensional space, and the equation is the implicit representation of that plane. The vector of coefficients \\((a, b, c)\\) is normal to the plane and determines its orientation, while the constant term \\(d\\) controls its distance from the origin: when \\(d = 0\\) the plane passes through the origin and the equation is homogeneous, otherwise the plane is a parallel translate of the homogeneous one.

The general solution is obtained by choosing two unknowns as free parameters. Assuming \\(c \neq 0\\) and setting \\(x = \lambda\\), \\(y = \mu\\), the equation gives:

\\[
z = \frac{d - a \lambda - b \mu}{c}, \qquad \lambda, \mu \in \mathbb{R}
\\]

Each pair \\((\lambda, \mu)\\) determines a point of the plane, and as the two parameters vary independently over \\(\mathbb{R}\\) the entire plane is described. The number of free parameters required, two in this case, equals the dimension of the plane, in agreement with the general principle that a single linear equation in \\(n\\) unknowns lowers the dimension by one. 

When \\(d = 0\\) the equation reduces to:

\\[
ax + by + cz = 0
\\]

and represents a plane through the origin. The set of its solutions is a two-dimensional vector subspace of \\(\mathbb{R}^3\\), formed by all vectors orthogonal to the coefficient vector \\((a, b, c)\\). The same parametric description used above applies, with \\(d = 0\\):

\\[
x = \lambda, \qquad y = \mu, \qquad z = -\frac{a \lambda + b \mu}{c}, \qquad \lambda, \mu \in \mathbb{R}
\\]

> The role of the unknown chosen as dependent is conventional. If \\(c = 0\\) but \\(a \neq 0\\) or \\(b \neq 0\\), the same construction can be carried out by isolating \\(x\\) or \\(y\\) instead. What does not depend on the choice is the geometric object obtained: the plane itself, with its orientation fixed by the normal vector \\((a, b, c)\\).

- - -
## Example 3

Consider the homogeneous linear equation:

\\[
x + 2y - z = 0
\\]

The coefficients are \\(a = 1\\), \\(b = 2\\), \\(c = -1\\), so the equation represents a plane through the origin in three-dimensional space, with normal vector \\((1, 2, -1)\\). To find the general solution we isolate \\(z\\) and obtain:

\\[
z = x + 2y
\\]

The two unknowns \\(x\\) and \\(y\\) can be chosen as free parameters, setting \\(x = \lambda\\) and \\(y = \mu\\) with \\(\lambda, \mu \in \mathbb{R}\\). Substituting back, the third coordinate is determined:

\\[
z = \lambda + 2 \mu
\\]

The solution set of the equation consists of all triples of the form:

\\[
(x, y, z) = (\lambda, \\, \mu, \\, \lambda + 2 \mu), \qquad \lambda, \mu \in \mathbb{R}
\\]

Specific points of the plane are obtained by assigning numerical values to the two parameters. 

+ For \\(\lambda = 1\\), \\(\mu = 0\\) we obtain \\((1, 0, 1)\\)
+ For \\(\lambda = 0\\), \\(\mu = 1\\) we obtain \\((0, 1, 2)\\)
+ For \\(\lambda = 2\\), \\(\mu = -1\\) we obtain \\((2, -1, 0)\\). 

A direct substitution confirms that all three triples satisfy the original equation.

The two triples \\((1, 0, 1)\\) and \\((0, 1, 2)\\) are [linearly independent](../rank-of-a-matrix/) and span the whole plane, in the sense that every solution can be written as the linear combination \\(\lambda (1, 0, 1) + \mu (0, 1, 2)\\). This pair of vectors constitutes a basis of the two-dimensional subspace of \\(\mathbb{R}^3\\) defined by the equation, and the parametrisation written above is precisely the expression of a generic vector of the subspace in terms of this basis.

The solution set of the equation \\(x + 2y - z = 0\\) is the plane through the origin described by:

\\[
(x, y, z) = (\lambda, \\, \mu, \\, \lambda + 2\mu), \qquad \lambda, \mu \in \mathbb{R}
\\]

- - -
## Linear equations with a parameter

A natural extension of the theory developed so far consists in allowing the coefficients to depend on one or more real parameters, rather than being fixed numbers. This gives rise to [linear equations with a parameter](../linear-equations-with-parameters/), a family of relations of the form:

\\[
a(k)\\, x + b(k) = c(k)
\\]

whose behaviour varies with the value assigned to \\(k\\). Reducing the equation to standard form yields \\(a(k)\\, x = c(k) - b(k)\\), and the three regimes already encountered in the discussion of the one-variable case appear here in their natural setting. For values of \\(k\\) such that \\(a(k) \neq 0\\) the equation is determinate and admits the unique solution \\(x = (c(k) - b(k)) / a(k)\\). For values such that \\(a(k) = 0\\) and \\(c(k) - b(k) = 0\\) the equation becomes the identity \\(0 = 0\\), satisfied by every real \\(x\\). For values such that \\(a(k) = 0\\) and \\(c(k) - b(k) \neq 0\\) the equation is impossible and admits no solution.

> Studying a parametric equation amounts to identifying the values of \\(k\\) that mark the transitions between these three regimes. The points at which \\(a(k)\\) vanishes are the critical ones, since they are precisely those at which the equation may lose its determinate character and degenerate into an identity or a contradiction.