---
title: Subspaces
source: https://algebrica.org/subspaces/
license: CC BY-NC 4.0
tags:
  - basis
  - complement
  - dimension
  - direct-sum
  - grassmann-formula
  - linear-algebra
  - span
  - subspaces
  - vector-spaces
---
## Definition of a subspace

A [vector space](../vector-spaces/) $V$ over a [field](../fields/) $F$ has an addition and a scalar multiplication. For a [subset](../sets/) $W \subseteq V,$ these operations restrict to $W$ only when their values belong to $W.$ The following three subsets fail this requirement in different ways.

The first quadrant $Q = \{\ (x, y) \in \mathbb{R}^2 \mid x \geq 0,\ y \geq 0 \ \}$ contains the sum of any two of its elements, since the sum of nonnegative numbers is nonnegative. It is not closed under scalar multiplication, because $(-1)(1, 1) = (-1, -1)$ lies outside $Q.$

The union $U$ of the two coordinate axes contains $\alpha\mathbf{v}$ for every $\mathbf{v} \in U$ and every $\alpha \in \mathbb{R},$ since every scalar multiple of a vector on either axis lies on that axis. It is not closed under addition, because $(1, 0) + (0, 1) = (1, 1)$ lies on neither axis.

The line $r$ of equation $y = x + 1$ does not contain the origin. It cannot be a vector space under the inherited operations, because every vector space contains the [zero vector](../vectors/).

The three failures are independent of one another. Neither closure condition implies the other, and neither implies that the zero vector belongs to the subset. A subset that contains the zero vector and satisfies both closure conditions is a subspace.

A subset $W$ of a vector space $V$ over $F$ is a subspace of $V$ when $W$ is itself a vector space over $F$ under the operations inherited from $V.$ The subsets $\{\ \mathbf{0} \ \}$ and $V$ are subspaces for every $V.$ These are the trivial subspaces.

## The subspace criterion

Checking the definition against every vector space axiom is unnecessary, since most axioms are identities that hold for all vectors of $V$ and therefore for the vectors of $W.$ Associativity and commutativity of addition, the two distributive laws and the compatibility of scalar multiplication require no further verification. Only closure under the two operations and membership of the zero vector and the additive inverses remain to be checked.

A subset $W \subseteq V$ is a subspace precisely when the following three conditions hold:

+ $\mathbf{0} \in W$
+ $\mathbf{u} + \mathbf{v} \in W$ for all $\mathbf{u}, \mathbf{v} \in W$
+ $\alpha\mathbf{v} \in W$ for all $\alpha \in F$ and $\mathbf{v} \in W$

The first condition ensures that the zero vector belongs to $W.$ The third ensures that each additive inverse belongs to $W,$ since $-\mathbf{v} = (-1)\mathbf{v}$ whenever $\mathbf{v} \in W.$ The second and third ensure that the two operations are well defined on $W.$

The first condition can be weakened to the requirement that $W$ be nonempty. Choosing any $\mathbf{v} \in W$ and applying the third condition with $\alpha = 0$ gives $0\mathbf{v} = \mathbf{0} \in W.$ Writing the condition explicitly lets us discard any candidate that omits the origin.

The two closure conditions combine into a single one, so that $W$ is a subspace when it is nonempty and:

$$\alpha\mathbf{u} + \beta\mathbf{v} \in W \qquad \text{for all } \mathbf{u}, \mathbf{v} \in W \text{ and all } \alpha, \beta \in F$$

With $\alpha = \beta = 1,$ the condition states closure under addition, and with $\beta = 0,$ it states closure under scalar multiplication. [Induction](../principle-of-mathematical-induction/) on the number of terms proves the same statement for every finite [linear combination](../linear-combinations/), so a subspace contains every linear combination of its own elements.

## Solutions of a homogeneous system

Let $A$ be an $m \times n$ matrix with real entries. The solution set of the associated homogeneous [system](../systems-of-linear-equations/) is:

$$\mathcal{S} = \{\ \mathbf{x} \in \mathbb{R}^n \mid A\mathbf{x} = \mathbf{0} \ \}$$

Since $A\mathbf{0} = \mathbf{0},$ the origin belongs to $\mathcal{S}.$ For $\mathbf{x}, \mathbf{y} \in \mathcal{S}$ and $\alpha, \beta \in \mathbb{R},$ the [linear map](../linear-maps/) $\mathbf{x} \mapsto A\mathbf{x}$ satisfies:

$$A(\alpha\mathbf{x} + \beta\mathbf{y}) = \alpha A\mathbf{x} + \beta A\mathbf{y} = \mathbf{0}$$

The set $\mathcal{S}$ is therefore a subspace of $\mathbb{R}^n$ and is the [kernel](../homomorphisms-and-isomorphisms/) of the map $\mathbf{x} \mapsto A\mathbf{x}.$ If $r$ is the [rank](../rank-of-a-matrix/) of $A,$ then after [Gaussian elimination](../gaussian-elimination/) the reduced system has $n - r$ free variables, and its standard parametrization has one basis vector for each free variable. Hence $\dim \mathcal{S} = n - r = n - \mathrm{rank}(A).$

The solution set of a system $A\mathbf{x} = \mathbf{b}$ with $\mathbf{b} \neq \mathbf{0}$ is not a subspace, since $\mathbf{x} = \mathbf{0}$ fails the equation. The [Rouché-Capelli theorem](../rouche-capelli-theorem/) determines whether the system is solvable. If it is and $\mathbf{x}_0$ is one of its solutions, the solution set is the translate $\mathbf{x}_0 + \mathcal{S},$ whose elements have the form $\mathbf{x}_0 + \mathbf{s}$ with $\mathbf{s} \in \mathcal{S}.$

> A translate of a subspace is called an affine subspace. Lines and planes that do not pass through the origin are affine subspaces, but they are not subspaces. A homogeneous system has a subspace as its solution set, whereas a solvable nonhomogeneous system has an affine subspace as its solution set.

## Subspaces of the plane and of space

The subspaces of $\mathbb{R}^2$ are the zero subspace, the [lines](../lines/) through the origin and $\mathbb{R}^2$ itself. If $W$ contains a nonzero vector $\mathbf{v},$ then every multiple $\alpha\mathbf{v}$ belongs to $W.$ These multiples form the line through the origin with direction $\mathbf{v}.$ If $W$ contains a second vector $\mathbf{w}$ outside that line, then $\mathbf{v}$ and $\mathbf{w}$ form a basis of $\mathbb{R}^2,$ so $W = \mathbb{R}^2.$

The subspaces of $\mathbb{R}^3$ are the zero subspace, the lines through the origin, the planes through the origin and $\mathbb{R}^3$ itself. Each is the solution set of a homogeneous system. A plane has an equation $ax + by + cz = 0$ with $(a, b, c) \neq (0, 0, 0),$ and a line is the solution set of two independent equations of that form.

Dimension distinguishes these cases. Every subspace of $\mathbb{R}^n$ has a dimension $k$ with $0 \leq k \leq n$ and is [linearly isomorphic](../homomorphisms-and-isomorphisms/) to $\mathbb{R}^k.$

## Subspaces of function and matrix spaces

The polynomials of degree at most $n$ form a subspace of the space of all [polynomials](../polynomials/) with coefficients in $F,$ because every sum and scalar multiple is either the zero polynomial or has degree at most $n.$ The polynomials of degree exactly $n$ do not form a subspace, since the sum of $x^n$ and $1 - x^n$ has degree $0.$

Inside the space $M_n(\mathbb{R})$ of square [matrices](../matrices/) of order $n,$ the symmetric matrices form a subspace, since transposition satisfies $(\alpha A + \beta B)^{\mathrm{T}} = \alpha A^{\mathrm{T}} + \beta B^{\mathrm{T}},$ and the right-hand side equals $\alpha A + \beta B$ when both matrices are symmetric. The matrices of trace zero form a subspace because the trace is linear. The [invertible matrices](../inverse-matrix/) do not, since the identity $I$ and its opposite $-I$ are both invertible while their sum is the zero matrix.

Among functions $f : \mathbb{R} \to \mathbb{R},$ the [continuous](../continuous-functions/) ones form a subspace of the space of all functions, because sums and scalar multiples of continuous functions are continuous. The same holds for the [differentiable functions](../derivatives/), for the functions vanishing at a fixed point $x_0,$ and for the solutions of a homogeneous linear [differential equation](../differential-equations/). The functions satisfying $f(x_0) = 1$ do not form a subspace, since the zero function is not among them.

## Intersection and union

Let $\{\ W_i \ \}_{i \in I}$ be any family of subspaces of $V.$ Their intersection contains $\mathbf{0},$ since every $W_i$ does. If $\mathbf{u}$ and $\mathbf{v}$ belong to the intersection and $\alpha, \beta \in F,$ then $\alpha\mathbf{u} + \beta\mathbf{v}$ belongs to each $W_i$ by closure, hence to the intersection. The intersection of any family of subspaces, finite or infinite, is therefore a subspace.

The union behaves differently. The two coordinate axes of $\mathbb{R}^2$ are subspaces whose union is not, as the sum of $(1, 0)$ and $(0, 1)$ shows. More generally, suppose that $W_1$ and $W_2$ are subspaces and neither contains the other. Choose $\mathbf{u} \in W_1$ outside $W_2$ and $\mathbf{v} \in W_2$ outside $W_1.$ Were $\mathbf{u} + \mathbf{v}$ in the union, say $\mathbf{u} + \mathbf{v} \in W_1,$ then $\mathbf{v} = (\mathbf{u} + \mathbf{v}) - \mathbf{u}$ would lie in $W_1,$ against the choice of $\mathbf{v},$ and the symmetric argument rules out $\mathbf{u} + \mathbf{v} \in W_2.$ Thus the union of two subspaces is a subspace if and only if one of them contains the other.

## The sum of two subspaces

Given two subspaces $A$ and $B$ of $V,$ their sum is:

$$A + B = \{\ \mathbf{a} + \mathbf{b} \mid \mathbf{a} \in A,\ \mathbf{b} \in B \ \}$$

This set is a subspace. It contains $\mathbf{0} = \mathbf{0} + \mathbf{0}.$ For two of its elements $\mathbf{a}_1 + \mathbf{b}_1$ and $\mathbf{a}_2 + \mathbf{b}_2,$ we have:

$$\alpha(\mathbf{a}_1 + \mathbf{b}_1) + \beta(\mathbf{a}_2 + \mathbf{b}_2) = (\alpha\mathbf{a}_1 + \beta\mathbf{a}_2) + (\alpha\mathbf{b}_1 + \beta\mathbf{b}_2)$$

The first bracket lies in $A$ and the second in $B,$ so the result belongs to $A + B.$ Choosing $\mathbf{b} = \mathbf{0}$ shows $A \subseteq A + B,$ and symmetrically $B \subseteq A + B,$ so the sum contains the union. Any subspace $W$ containing both $A$ and $B$ contains each $\mathbf{a} + \mathbf{b}$ by closure under addition, hence contains $A + B.$ The sum is thus the smallest subspace containing $A \cup B$ and is the span of that union.

The definition extends to finitely many subspaces $A_1, \ldots, A_s,$ whose sum consists of all vectors $\mathbf{a}_1 + \cdots + \mathbf{a}_s$ with $\mathbf{a}_i \in A_i.$ When each $A_i$ is the line $F\mathbf{v}_i$ generated by a single vector, the sum is the span of $\mathbf{v}_1, \ldots, \mathbf{v}_s,$ so the span of a finite set is a particular case of a sum of subspaces.

In $\mathbb{R}^3,$ two distinct planes through the origin meet in a line and their sum is the whole space, while a plane and a line contained in it have the plane itself as sum. The intersection of the two summands determines the dimension of the sum.

## Grassmann's formula

For finite-dimensional subspaces $A$ and $B$ of a vector space $V$:

$$\dim(A + B) = \dim A + \dim B - \dim(A \cap B)$$

The proof starts with a basis $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k \ \}$ of $A \cap B.$ Since this set is linearly independent in $A,$ it can be extended to a basis $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{a}_1, \ldots, \mathbf{a}_p \ \}$ of $A.$ It is also linearly independent in $B,$ so it can be extended to a basis $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{b}_1, \ldots, \mathbf{b}_q \ \}$ of $B.$ The union of the two bases is:

$$\mathcal{B} = \{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{a}_1, \ldots, \mathbf{a}_p, \mathbf{b}_1, \ldots, \mathbf{b}_q \ \}$$

This set is a basis of $A + B.$

Every element of $A + B$ is a sum of an element of $A$ and an element of $B.$ These two elements are linear combinations of the corresponding bases, so $\mathcal{B}$ spans $A + B.$ To prove independence, suppose that a linear combination of the vectors of $\mathcal{B}$ vanishes:

$$\sum_{i=1}^{k} \lambda_i\mathbf{u}_i + \sum_{j=1}^{p} \mu_j\mathbf{a}_j + \sum_{l=1}^{q} \nu_l\mathbf{b}_l = \mathbf{0}$$

Set $\mathbf{w} = \sum_l \nu_l\mathbf{b}_l.$ The relation implies $\mathbf{w} = -\sum_i \lambda_i\mathbf{u}_i - \sum_j \mu_j\mathbf{a}_j,$ so $\mathbf{w}$ belongs to $A.$ Its definition also shows that $\mathbf{w}$ belongs to $B.$ Hence $\mathbf{w} \in A \cap B$ and $\mathbf{w} = \sum_i \delta_i\mathbf{u}_i$ for suitable scalars $\delta_i.$ The two expressions for $\mathbf{w}$ imply:

$$\sum_{i=1}^{k} \delta_i\mathbf{u}_i - \sum_{l=1}^{q} \nu_l\mathbf{b}_l = \mathbf{0}$$

The vectors in this relation are a subset of the basis of $B,$ so their independence implies $\nu_l = 0$ for all $l$ and $\delta_i = 0$ for all $i.$ The original relation then reduces to a vanishing combination of the basis of $A,$ so $\lambda_i = 0$ and $\mu_j = 0.$ All coefficients vanish, and $\mathcal{B}$ is independent.

The basis $\mathcal{B}$ has $k + p + q$ elements, so $\dim(A + B) = k + p + q.$ Since $\dim A = k + p$ and $\dim B = k + q,$ the sum $\dim A + \dim B = 2k + p + q$ counts the $k$ vectors of the intersection twice. Subtracting $\dim(A \cap B) = k$ gives the formula.

- - -

In $\mathbb{R}^4,$ define the two planes:

$$A = \mathrm{span}\{\ (1, 0, 1, 0),\ (0, 1, 0, 1) \ \}, \qquad B = \mathrm{span}\{\ (1, 1, 0, 0),\ (0, 0, 1, 1) \ \}$$

A vector of $A$ has the form $(a, b, a, b)$ and a vector of $B$ has the form $(c, c, d, d).$ The two forms are equal only if $a = c,$ $b = c,$ $a = d$ and $b = d.$ Thus all four parameters coincide, and the intersection is the line generated by $(1, 1, 1, 1).$ By Grassmann's formula, $\dim(A + B) = 2 + 2 - 1 = 3,$ so the two planes span a hyperplane of $\mathbb{R}^4$ rather than the whole space. Two planes in a four-dimensional space may also meet only at the origin, in which case their sum has dimension $4.$

## Direct sums

The decomposition of a vector of $A + B$ as $\mathbf{a} + \mathbf{b}$ is not always unique. In $\mathbb{R}^2,$ if $A = B = \mathbb{R}^2,$ the vector $(1, 1)$ has the decompositions $(1, 1) + (0, 0)$ and $(1, 0) + (0, 1).$ Uniqueness of the decomposition is a condition on the intersection.

The sum $A + B$ is direct, written $A \oplus B,$ when every vector of $A + B$ has exactly one expression $\mathbf{a} + \mathbf{b}$ with $\mathbf{a} \in A$ and $\mathbf{b} \in B.$ This happens precisely when $A \cap B = \{\ \mathbf{0} \ \}.$ If the intersection contains a nonzero vector $\mathbf{w},$ then the expressions $\mathbf{w} + \mathbf{0}$ and $\mathbf{0} + \mathbf{w}$ are two distinct decompositions of $\mathbf{w}.$ Conversely, if $\mathbf{a}_1 + \mathbf{b}_1 = \mathbf{a}_2 + \mathbf{b}_2,$ then $\mathbf{a}_1 - \mathbf{a}_2 = \mathbf{b}_2 - \mathbf{b}_1$ is a vector lying in both subspaces, hence zero, and the two decompositions coincide.

Grassmann's formula reduces in this case to:

$$\dim(A \oplus B) = \dim A + \dim B$$

Thus a sum of two finite-dimensional subspaces is direct exactly when $\dim(A + B) = \dim A + \dim B.$

For more than two summands the condition on pairwise intersections is no longer sufficient. The sum $A_1 + \cdots + A_s$ is direct when the only decomposition of the zero vector into terms $\mathbf{a}_i \in A_i$ is the one with all terms equal to $\mathbf{0}$:

$$\mathbf{0} = \mathbf{a}_1 + \cdots + \mathbf{a}_s \quad \Longrightarrow \quad \mathbf{a}_1 = \cdots = \mathbf{a}_s = \mathbf{0}$$

This requirement is equivalent to the uniqueness of the decomposition of every vector of the sum. Three distinct lines of $\mathbb{R}^2$ show why the pairwise condition falls short. Let $A_1,$ $A_2$ and $A_3$ be generated by $(1, 0),$ $(0, 1)$ and $(1, 1)$ respectively. Any two of them meet only at the origin, yet the zero vector has the nontrivial decomposition:

$$(1, 0) + (0, 1) - (1, 1) = (0, 0)$$

The sum of the three lines therefore has dimension $2$ instead of $3.$ For a direct sum, each $A_i$ must meet the sum of the remaining subspaces only at the origin.

## Complements

A subspace $B$ of $V$ is a complement of the subspace $A$ when $V = A \oplus B,$ that is when $A + B = V$ and $A \cap B = \{\ \mathbf{0} \ \}.$ Every vector of $V$ then splits in exactly one way into a component in $A$ and a component in $B.$

In finite dimension a complement always exists. A basis $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k \ \}$ of $A$ can be extended to a basis $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{w}_1, \ldots, \mathbf{w}_{n-k} \ \}$ of $V.$ Let $B$ be the subspace generated by the added vectors. Every vector of $V$ is a linear combination of this basis. Its coefficients split into a part in $A$ and a part in $B,$ so $A + B = V.$ If $\mathbf{x} \in A \cap B,$ then $\mathbf{x}$ has one expression in terms of the $\mathbf{u}_i$ and another in terms of the $\mathbf{w}_j.$ Subtracting the two expressions gives a relation among the vectors of the basis, so independence implies $\mathbf{x} = \mathbf{0}.$ The dimensions satisfy:

$$\dim A + \dim B = \dim V$$

Complements are not unique. In $\mathbb{R}^2$ the subspace $A$ generated by $(1, 0)$ has every other line through the origin as a complement, including the lines generated by $(0, 1)$ and $(1, 1).$ A basis of $A$ has different extensions to a basis of $V,$ and each extension determines a complement of dimension $\dim V - \dim A.$

## Internal and external direct sums

The symbol $\oplus$ denotes two different constructions. Given vector spaces $V_1, \ldots, V_s$ over the same field, not assumed to be subspaces of a common vector space, their external direct sum is the Cartesian product $V_1 \times \cdots \times V_s$ with componentwise operations:

$$(\mathbf{v}_1, \ldots, \mathbf{v}_s) + (\mathbf{w}_1, \ldots, \mathbf{w}_s) = (\mathbf{v}_1 + \mathbf{w}_1, \ldots, \mathbf{v}_s + \mathbf{w}_s), \qquad \alpha(\mathbf{v}_1, \ldots, \mathbf{v}_s) = (\alpha\mathbf{v}_1, \ldots, \alpha\mathbf{v}_s)$$

Its dimension is the sum of the dimensions of the factors.

The internal direct sum, treated above, concerns subspaces $A_1, \ldots, A_s$ of one space $V.$ The formula $(\mathbf{a}_1, \ldots, \mathbf{a}_s) \mapsto \mathbf{a}_1 + \cdots + \mathbf{a}_s$ defines a linear map from the external direct sum of the $A_i$ to $V.$ Its image is $A_1 + \cdots + A_s,$ and it is injective exactly when the zero vector has only the trivial decomposition. Thus the sum of the $A_i$ is direct precisely when this map is an isomorphism from the external direct sum onto $A_1 + \cdots + A_s.$
