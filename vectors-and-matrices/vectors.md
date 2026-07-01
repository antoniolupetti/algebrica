---
title: Vectors
source: https://algebrica.org/vectors/
license: CC BY-NC 4.0
tags:
  - cross-product
  - dot-product
  - euclidean-space
  - linear-algebra
  - vectors
---
## Geometric representation

A vector is a quantity characterised by both a magnitude and a direction, in contrast to a scalar, which is described by magnitude alone. This distinction arises in geometry and physics, where quantities such as displacement, velocity, and force require directional information that a single real number cannot encode.

The formal treatment developed here is algebraic and applies to vectors in the Euclidean spaces $\mathbb{R}^2$ and $\mathbb{R}^3,$ which are sufficient for most basic applications in calculus, geometry, and mechanics. A vector in the plane or in three-dimensional space is represented as a directed line segment, that is, a segment with a specified initial point and a terminal point. The direction of the segment indicates the orientation of the vector, and its length is the magnitude.

![IMG. 1](svg/vectors-1.svg)

Two directed segments that have the same length and the same direction are considered to represent the same vector, regardless of their position in space. This equivalence is the basis for the notion of a free vector, which is entirely characterised by its direction and magnitude, independently of where it is drawn.

![IMG. 2](svg/vectors-2.svg)

When a fixed origin $O$ is chosen, every point $P$ in the plane or in space determines a vector, the directed segment from $O$ to $P,$ called the position vector of $P.$ This correspondence identifies points with vectors applied at the origin, and it links the geometric description of space to the algebraic description by coordinates developed in the next section. A free vector describes a displacement independent of any particular point, whereas a position vector singles out a specific location relative to the origin.

Vectors are commonly denoted by boldface letters such as $\mathbf{v},$ or by the arrow notation $\vec{v}.$ The zero vector, denoted $\mathbf{0},$ has zero magnitude and no defined direction, and it is the additive identity in vector arithmetic.

## Components and coordinate representation

In a Cartesian coordinate system, every vector in $\mathbb{R}^n$ can be expressed in terms of its components along the coordinate axes. A vector $\mathbf{v}$ in $\mathbb{R}^2$ is written as an ordered pair:

$$\mathbf{v} = (v_1, v_2) \in \mathbb{R}^2$$

![IMG. 3](svg/vectors-3.svg)

A vector in $\mathbb{R}^3$ is written as an ordered triple.

$$\mathbf{v} = (v_1, v_2, v_3) \in \mathbb{R}^3$$

![IMG. 4](svg/vectors-4.svg)

The [real numbers](../properties-of-real-numbers/) $v_1, v_2, v_3$ are called the components of $\mathbf{v}$ in the chosen coordinate system. More generally, a vector in $\mathbb{R}^n$ is an ordered $n$-tuple of real numbers $(v_1, v_2, \ldots, v_n),$ and the operations defined in this entry extend to this general setting, with the exception of the cross product, which is specific to $\mathbb{R}^3.$ Two vectors are equal when they belong to the same space and their corresponding components coincide, so the equality $\mathbf{u} = \mathbf{v}$ in $\mathbb{R}^n$ amounts to the $n$ scalar equalities $u_1 = v_1, \ldots, u_n = v_n.$

The standard basis vectors in $\mathbb{R}^3$ are defined as follows.

$$\mathbf{i} = (1, 0, 0) \qquad \mathbf{j} = (0, 1, 0) \qquad \mathbf{k} = (0, 0, 1)$$

Every vector in $\mathbb{R}^3$ can be expressed as a [linear combination](../linear-combinations/) of these basis vectors.

$$\mathbf{v} = v_1\mathbf{i} + v_2\mathbf{j} + v_3\mathbf{k}$$

In this expression the coefficient $v_1$ scales $\mathbf{i}$ along the $x$-axis, $v_2$ scales $\mathbf{j}$ along the $y$-axis, and $v_3$ scales $\mathbf{k}$ along the $z$-axis. The sum of these three scaled basis vectors reconstructs $\mathbf{v}$ exactly.

For example, the vector $(3, -1, 2)$ is written as $3\mathbf{i} - \mathbf{j} + 2\mathbf{k},$ meaning a displacement of three units in the $x$-direction, one unit in the negative $y$-direction, and two units in the $z$-direction. This representation makes explicit the decomposition of $\mathbf{v}$ into contributions along each coordinate direction.

> The same construction in $\mathbb{R}^n$ uses the standard unit vectors $\mathbf{e}_1, \ldots, \mathbf{e}_n,$ where $\mathbf{e}_i$ has $i$-th component equal to $1$ and all other components equal to $0.$ Every vector $\mathbf{v} \in \mathbb{R}^n$ decomposes as $\mathbf{v} = v_1\mathbf{e}_1 + \cdots + v_n\mathbf{e}_n,$ and the vectors $\mathbf{i}, \mathbf{j}, \mathbf{k}$ correspond to $\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3.$

## Vector operations

The basic algebraic operations on vectors are addition, subtraction, and scalar multiplication. These operations are defined component-wise and admit clear geometric interpretations. Given two vectors $\mathbf{u} = (u_1, u_2, u_3)$ and $\mathbf{v} = (v_1, v_2, v_3)$ in $\mathbb{R}^3,$ their sum is defined as follows.

$$\mathbf{u} + \mathbf{v} = (u_1+v_1, u_2+v_2, u_3+v_3)$$

Geometrically, vector addition corresponds to placing the initial point of $\mathbf{v}$ at the terminal point of $\mathbf{u}.$ The resulting vector connects the initial point of $\mathbf{u}$ to the terminal point of $\mathbf{v}.$ This construction is known as the triangle rule.

![IMG. 5](svg/vectors-5.svg)

An equivalent formulation, the parallelogram rule, places both vectors at a common initial point and identifies their sum with the diagonal of the parallelogram they determine.

![IMG. 6](svg/vectors-6.svg)

Scalar multiplication by a real number $\lambda \in \mathbb{R}$ scales each component uniformly.

$$\lambda\mathbf{v} = (\lambda v_1, \lambda v_2, \lambda v_3)$$

When $\lambda > 0,$ the resulting vector has the same direction as $\mathbf{v}$ and magnitude scaled by $\lambda.$ When $\lambda < 0,$ the direction is reversed. When $\lambda = 0,$ the result is the zero vector. Subtraction is defined by combining the two preceding operations, $\mathbf{u} - \mathbf{v} = \mathbf{u} + (-1)\mathbf{v},$ which yields $(u_1-v_1, u_2-v_2, u_3-v_3).$

The difference $\mathbf{u} - \mathbf{v}$ also admits a direct geometric reading. When the two vectors are drawn from a common initial point, $\mathbf{u} - \mathbf{v}$ is the vector that joins the terminal point of $\mathbf{v}$ to the terminal point of $\mathbf{u},$ since adding $\mathbf{v}$ to it returns $\mathbf{u}.$ In the parallelogram determined by the two vectors, the sum corresponds to one diagonal and the difference to the other. In particular, if two points $P$ and $Q$ have position vectors $\mathbf{p}$ and $\mathbf{q},$ the difference $\mathbf{p} - \mathbf{q}$ is the displacement from $Q$ to $P.$

## Algebraic properties

The operations of vector addition and scalar multiplication satisfy a set of fundamental properties that hold for all vectors $\mathbf{u}, \mathbf{v}, \mathbf{w} \in \mathbb{R}^n$ and all scalars $\lambda, \mu \in \mathbb{R}.$

+ Addition is commutative, meaning that $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u},$ and associative, so that $(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w}).$
+ The zero vector $\mathbf{0}$ is the additive identity, satisfying $\mathbf{v} + \mathbf{0} = \mathbf{v}$ for every $\mathbf{v},$ and each vector $\mathbf{v}$ has an additive inverse $-\mathbf{v} = (-1)\mathbf{v}$ such that $\mathbf{v} + (-\mathbf{v}) = \mathbf{0}.$
+ Scalar multiplication distributes over vector addition according to $\lambda(\mathbf{u} + \mathbf{v}) = \lambda\mathbf{u} + \lambda\mathbf{v},$ and over scalar addition according to $(\lambda + \mu)\mathbf{v} = \lambda\mathbf{v} + \mu\mathbf{v}.$ It is compatible with multiplication of scalars, since $(\lambda\mu)\mathbf{v} = \lambda(\mu\mathbf{v}),$ and the scalar $1$ is the multiplicative identity, with $1 \cdot \mathbf{v} = \mathbf{v}.$

> Together these properties are the defining axioms of a vector space. The set $\mathbb{R}^n$ with these two operations is a vector space over the [field](../fields/) $\mathbb{R},$ examined in greater generality in the entry on [vector spaces](../vector-spaces/).

## Norm of a vector

The norm, or magnitude, of a vector $\mathbf{v} = (v_1, v_2, v_3)$ is a non-negative real number that measures its length. It is defined by the following expression:

$$\|\mathbf{v}\| = \sqrt{v_1^2 + v_2^2 + v_3^2}$$

This formula is a direct consequence of the [Pythagorean theorem](../pythagorean-theorem/) applied iteratively along the coordinate axes. In $\mathbb{R}^2,$ the analogous formula is the following:

$$\|\mathbf{v}\| = \sqrt{v_1^2 + v_2^2}$$

As an example, consider the vector $\mathbf{v} = (2, -3, 6)$ in $\mathbb{R}^3.$ Its norm is computed by summing the squares of its components and taking the square root:

$$
\begin{align}
\|\mathbf{v}\| &= \sqrt{2^2+(-3)^2+6^2} \\[6pt]
               &= \sqrt{4+9+36} \\[6pt]
               &= \sqrt{49} \\[6pt]
               &= 7
\end{align}
$$

Each term under the radical corresponds to the squared contribution of one coordinate direction, and the result confirms that $\mathbf{v}$ has length $7.$ A vector whose norm is equal to one is called a unit vector. Given any non-zero vector $\mathbf{v},$ dividing it by its norm produces a unit vector in the same direction. This operation is called normalisation.

$$\hat{\mathbf{v}} = \frac{\mathbf{v}}{\|\mathbf{v}\|}$$

The resulting vector $\hat{\mathbf{v}}$ satisfies $\|\hat{\mathbf{v}}\| = 1$ by construction.

## Dot product

The dot product, also called the scalar product or inner product, is a binary operation that takes two vectors and returns a real number. For $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n,$ it is defined algebraically as the sum of the products of corresponding components.

$$\mathbf{u} \cdot \mathbf{v} = \sum_{i=1}^{n} u_i v_i = u_1 v_1 + u_2 v_2 + \cdots + u_n v_n$$

The dot product admits an equivalent geometric formulation in terms of the [angle](../angles-and-angular-measure/) $\theta$ between the two vectors.

$$\mathbf{u} \cdot \mathbf{v} = \|\mathbf{u}\|\|\mathbf{v}\|\cos\theta$$

The factor $\cos\theta$ connects the dot product to the [cosine](../sine-and-cosine/) of the angle between the two vectors. When $\mathbf{u} \cdot \mathbf{v} = 0$ and neither vector is zero, it follows that $\cos\theta = 0,$ hence $\theta = \pi/2.$ Two vectors satisfying this condition are said to be orthogonal. Conversely, when the vectors are parallel, $\theta = 0$ or $\theta = \pi,$ and the dot product equals $\pm\|\mathbf{u}\|\|\mathbf{v}\|.$ The norm also follows from the dot product, since $\|\mathbf{v}\|^2 = \mathbf{v} \cdot \mathbf{v}.$ As an application, consider $\mathbf{u} = (1, 2, -1)$ and $\mathbf{v} = (3, 0, 3).$ The dot product is computed as follows.

$$
\begin{align}
\mathbf{u} \cdot \mathbf{v} &= (1)(3)+(2)(0)+(-1)(3) \\[6pt]
                             &= 3+0-3 \\[6pt]
                             &= 0
\end{align}
$$

Since the result is zero, the two vectors are orthogonal.

## Cross product

The cross product is an operation defined for vectors in $\mathbb{R}^3$ that takes two vectors and returns a third vector. Unlike the dot product, the result is not a scalar but a vector, and for this reason the operation is also called the vector product. Given $\mathbf{u} = (u_1, u_2, u_3)$ and $\mathbf{v} = (v_1, v_2, v_3),$ their cross product is defined by the following formula, expressed as the [determinant](../determinant/) of a [matrix](../matrices/).

$$
\mathbf{u} \times \mathbf{v} =
\begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\[6pt]
u_1 & u_2 & u_3 \\[6pt]
v_1 & v_2 & v_3
\end{vmatrix}
$$

Expanding along the first row yields the explicit component form.

$$\mathbf{u} \times \mathbf{v} = (u_2 v_3 - u_3 v_2, u_3 v_1 - u_1 v_3, u_1 v_2 - u_2 v_1)$$

The resulting vector is orthogonal to both $\mathbf{u}$ and $\mathbf{v},$ as can be verified by computing the dot products $(\mathbf{u} \times \mathbf{v}) \cdot \mathbf{u}$ and $(\mathbf{u} \times \mathbf{v}) \cdot \mathbf{v},$ both of which equal zero. The direction of $\mathbf{u} \times \mathbf{v}$ is determined by the right-hand rule. If the fingers of the right hand curl from $\mathbf{u}$ toward $\mathbf{v},$ the thumb points in the direction of $\mathbf{u} \times \mathbf{v}.$ The magnitude of the cross product has a geometric interpretation:

$$\|\mathbf{u} \times \mathbf{v}\| = \|\mathbf{u}\|\|\mathbf{v}\|\sin\theta$$

This quantity equals the area of the parallelogram spanned by $\mathbf{u}$ and $\mathbf{v}.$ In particular, $\mathbf{u} \times \mathbf{v} = \mathbf{0}$ if and only if $\sin\theta = 0,$ that is, if and only if the vectors are parallel. The cross product is anti-commutative, $\mathbf{v} \times \mathbf{u} = -(\mathbf{u} \times \mathbf{v}),$ which reflects the reversal of orientation when the order of the operands is exchanged.

- - -

As a concrete example, consider $\mathbf{u} = (1, 2, 3)$ and $\mathbf{v} = (4, 5, 6).$ Applying the component formula yields the following.

$$
\begin{align}
\mathbf{u} \times \mathbf{v} &= (u_2v_3-u_3v_2, u_3v_1-u_1v_3, u_1v_2-u_2v_1) \\[6pt]
&= (2\cdot6-3\cdot5, 3\cdot4-1\cdot6, 1\cdot5-2\cdot4) \\[6pt]
&= (12-15, 12-6, 5-8) \\[6pt]
&= (-3, 6, -3)
\end{align}
$$

One can verify that the result is orthogonal to both $\mathbf{u}$ and $\mathbf{v}$ by computing the two dot products. For the first:

$$(-3, 6, -3)\cdot(1, 2, 3) = -3 + 12 - 9 = 0$$

and for the second:

$$(-3, 6, -3)\cdot(4, 5, 6) = -12 + 30 - 18 = 0$$

Both results are zero, confirming that $\mathbf{u} \times \mathbf{v}$ is orthogonal to both factors.
