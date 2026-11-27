---
title: Rings
source: https://algebrica.org/rings/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - commutative-ring
  - distributivity
  - homomorphism
  - ideal
  - integral-domain
  - polynomial-ring
  - ring-theory
  - subring
  - zero-divisor
---

## Definition

A ring is a [set](../sets/) $R$ equipped with two binary operations, addition and multiplication. Under addition, $(R,+)$ is an [abelian group](../groups/). We denote the ring by the triple:

$$(R, +, \cdot) \tag{1}$$

Writing $0$ for the additive identity and $-a$ for the additive inverse of $a,$ we have the following relations for every $a \in R$:

$$
\begin{align}
a + 0 &= a \notag\\[6pt]
a + (-a) &= 0 \tag{2}
\end{align}
$$

Multiplication is associative and distributes over addition. For all $a, b, c \in R$ the following identities hold:

$$
\begin{align}
(a \cdot b) \cdot c &= a \cdot (b \cdot c) \tag{3}\\[6pt]
a \cdot (b + c) &= a \cdot b + a \cdot c \tag{4}\\[6pt]
(a + b) \cdot c &= a \cdot c + b \cdot c \tag{5}
\end{align}
$$

A ring is commutative if the following holds for all $a, b \in R$:

$$a \cdot b = b \cdot a$$

It is called unital if it has a multiplicative identity $1 \in R$ such that the following identity holds for every $a \in R$:

$$1 \cdot a = a \cdot 1 = a$$

The set $2\mathbb{Z}$ of [even integers](../integers/) is an example of a ring, since the even integers form an abelian group under addition and the product of two even integers is even. Multiplication is associative and the distributive laws hold because the operations are those of $\mathbb{Z}.$ This ring has no multiplicative identity, since such an element $e$ would have to satisfy $2e = 2,$ giving $e = 1,$ which is odd. The [natural numbers](../natural-numbers/) $\mathbb{N},$ on the other hand, do not form a ring under the usual operations because the additive inverse of $1$ does not belong to $\mathbb{N}.$

The distributive laws $(4)$ and $(5)$ determine how zero behaves under multiplication. Since $0 + 0 = 0,$ for every $a \in R$ we have:

$$
\begin{align}
a \cdot 0 &= a \cdot (0 + 0) = a \cdot 0 + a \cdot 0 \\[6pt]
0 \cdot a &= (0 + 0) \cdot a = 0 \cdot a + 0 \cdot a
\end{align}
$$

Subtracting $a \cdot 0$ from both sides of the first equation and $0 \cdot a$ from both sides of the second gives:

$$a \cdot 0 = 0 \cdot a = 0 \tag{6}$$

It follows from $(6)$ and the distributive laws $(4)$ and $(5)$ that replacing a factor by its additive inverse gives the additive inverse of the product. Indeed, for any $a, b \in R,$ factoring out $b$ on the right in the first line and $a$ on the left in the second gives:

$$
\begin{align}
a \cdot b + (-a) \cdot b &= (a + (-a)) \cdot b = 0 \\[6pt]
a \cdot b + a \cdot (-b) &= a \cdot (b + (-b)) = 0
\end{align}
$$

Since the additive inverse of $a \cdot b$ is unique, it follows that:

$$(-a) \cdot b = a \cdot (-b) = -(a \cdot b) \tag{7}$$

If $a$ and $b$ are positive integers, $(7)$ explains why replacing either factor by its additive inverse makes the product negative. In any ring, applying $(7)$ twice gives:

$$(-a)(-b) = -(a(-b)) = -(-(ab)) = ab \tag{8}$$

If $R$ is a unital ring, setting $a = 1$ in $(7)$ shows that multiplying an element $b \in R$ by $-1$ gives its additive inverse:

$$(-1) \cdot b = -(1 \cdot b) = -b \tag{9}$$

In particular, when $b = -1,$ equation $(9)$ gives $(-1)(-1) = 1,$ so $-1$ is its own multiplicative inverse. In general, an element $u$ of a unital ring $R$ is called invertible if there is an element $v \in R$ such that:

$$uv = vu = 1 \tag{10}$$

The inverse of an invertible element is unique and is denoted by $u^{-1},$ and the invertible elements form the group $R^\times$ under multiplication. For example, the only invertible elements of $\mathbb{Z}$ are $1$ and $-1,$ since two integers whose product is $uv = 1$ must satisfy:

$$|u| = |v| = 1$$

A nonzero element $a \in R$ is called a zero divisor if there is some $b \neq 0$ in $R$ for which at least one of the following holds:

$$
\begin{align}
ab &= 0 \\[6pt]
ba &= 0
\end{align}
$$

Finally, an integral domain is a commutative ring in which the multiplicative identity $1$ is distinct from zero and there are no zero divisors, meaning that if $ab = 0,$ at least one of the two factors must be zero.

## Commutative and noncommutative rings

We compare several rings to see which elements have a multiplicative inverse, when the product of two nonzero elements can be zero, and when the order of the factors affects the result. Under the usual operations, $\mathbb{Z}$ is an integral domain because it is a commutative ring with identity and the product of two nonzero integers is always nonzero. However, $2$ has no multiplicative inverse in $\mathbb{Z}.$ In the rings $\mathbb{Q},$ $\mathbb{R}$ and $\mathbb{C},$ every nonzero element is invertible, so all three are [fields](../fields/).

The ring $\mathbb{R}[x]$ of [polynomials](../polynomials/) with real coefficients is also an integral domain. Multiplication is commutative, and its identity is the constant polynomial $1.$ Moreover, the coefficient of the highest-degree term in the product of two nonzero polynomials is the product of their leading coefficients. Since this coefficient is nonzero, the product is also nonzero.

Now consider the [real-valued functions](../functions/) on a set $X.$ They form a commutative ring under pointwise addition and multiplication. Indeed, for every $x \in X$ we have:

$$
\begin{align}
(f + g)(x) &= f(x) + g(x) \\[6pt]
(fg)(x) &= f(x)g(x)
\end{align}
$$

Since multiplication is defined pointwise, multiplying $f$ by the constant function with value $1$ leaves each value $f(x)$ unchanged. This constant function is therefore the multiplicative identity, so $(10)$ requires $f(x)g(x) = 1$ for every $x \in X.$ It follows that $f$ is invertible if and only if it is nowhere zero, in which case its multiplicative inverse is the function $x \mapsto 1/f(x).$

The [residue classes](../modulo-operator/) modulo an integer $n \geq 2$ also form a ring, namely the commutative ring $\mathbb{Z}/n\mathbb{Z}$ with identity $[1].$ If $n$ is prime, every nonzero class has an inverse, so the ring is a field. In $\mathbb{Z}/6\mathbb{Z},$ however, we have $[2][3] = [6] = [0],$ since $2 \cdot 3$ is a multiple of $6.$ Thus $[2]$ and $[3]$ are zero divisors because both classes are nonzero and their product is zero.

Finally, consider the ring $\mathrm{M}_n(F)$ of [square matrices](../matrices/) over a field $F,$ whose multiplicative identity is the identity matrix $I_n.$ For $n \geq 2,$ reversing the order of the factors can change the result of row-by-column multiplication, as the following matrices of order $2$ show:

$$A = \begin{pmatrix}0 & 1 \\ 0 & 0\end{pmatrix}, \qquad B = \begin{pmatrix}1 & 0 \\ 0 & 0\end{pmatrix} \tag{11}$$

Multiplying them in the two possible orders gives different results:

$$
\begin{align}
AB &= \begin{pmatrix}0 & 0 \\ 0 & 0\end{pmatrix} \\[6pt]
BA &= \begin{pmatrix}0 & 1 \\ 0 & 0\end{pmatrix} = A
\end{align}
$$

Since $A$ and $B$ are nonzero and $AB = 0,$ both are zero divisors, and since $BA \neq AB,$ the ring is noncommutative. For $n \gt 2,$ extending the two matrices with rows and columns of zeros gives the same result.

## Subrings and ideals

Having seen how the operations in a ring work, we can ask when restricting them to a subset again gives a ring. A subset $S$ of a ring $R$ with this property is called a subring of $R.$ For example, in the ring of real square matrices of order $n,$ the matrices with rational entries form a subring because sums, differences and products of such matrices still have rational entries. A nonempty subset $S \subseteq R$ is a subring if and only if both of the following conditions hold for all $a, b \in S$:

$$
\begin{align}
a - b &\in S \notag\\[6pt]
ab &\in S \tag{12}
\end{align}
$$

In $(12),$ closure under subtraction makes $S$ a [subgroup](../subgroups/) of $(R, +),$ while the second condition ensures that the product also belongs to $S.$ Every ring $R$ has as subrings both $\{0\},$ consisting of zero alone, and the whole ring $R,$ and these subrings coincide when zero is the only element of $R.$ A subring of $R$ is called proper if it omits at least one element of $R.$ For example, the even integers $2\mathbb{Z}$ form a proper subring of $\mathbb{Z}$ because the difference and the product of two even integers are even and $1$ is not even. We now apply criterion $(12)$ to upper triangular matrices, starting with an example of order $2$:

$$A = \begin{pmatrix}1 & 2 \\ 0 & 1\end{pmatrix}, \qquad B = \begin{pmatrix}2 & 1 \\ 0 & 3\end{pmatrix}$$

Computing the difference and the product in $(12)$ gives:

$$
\begin{align}
A-B &= \begin{pmatrix}-1 & 1 \\ 0 & -2\end{pmatrix} \\[6pt]
AB &= \begin{pmatrix}2 & 7 \\ 0 & 3\end{pmatrix}
\end{align}
$$

In general, if $A$ and $B$ are upper triangular and $i \gt j,$ the entry $a_{ij}-b_{ij}$ is zero. Each term $a_{ik}b_{kj}$ in the entry $(AB)_{ij}$ is also zero, since $a_{ik}=0$ when $k \lt i$ and $b_{kj}=0$ when $k \geq i \gt j.$ The difference and the product are therefore upper triangular, and since the zero matrix is also upper triangular, $(12)$ shows that these matrices form a subring.

In the ring of functions from $\mathbb{R}$ to $\mathbb{R},$ the [continuous functions](../continuous-functions/) form a subring because the difference and the product of two continuous functions are continuous.

An ideal is a subring $I$ of a ring $R$ such that the following conditions hold for every $a \in I$ and every $r \in R$:

$$
\begin{align}
ra &\in I\\[6pt]
ar &\in I
\end{align}
$$

The first condition defines a left ideal and the second a right ideal. If both hold, the ideal is called two-sided. In a commutative ring $ra = ar,$ so every left ideal is also a right ideal and vice versa, and hence every one-sided ideal is two-sided.

For example, the even integers form a two-sided ideal of $\mathbb{Z}$ because the product of an even integer and any integer is even.
