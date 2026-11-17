---
title: Cantor's Theorem
source: https://algebrica.org/cantor-theorem/
license: CC BY-NC 4.0
tags:
  - aleph-numbers
  - cantor-bernstein-theorem
  - cantors-theorem
  - cardinality
  - continuum-hypothesis
  - diagonal-argument
  - power-set
  - uncountable-sets
---
## Statement

To state Cantor's theorem, we first introduce the [power set](../sets/), which, for an arbitrary set $A,$ is the set of all its subsets and is denoted as follows:

$$
\mathcal{P}(A)=\{\ B\mid B\subseteq A\ \}
\tag{1}
$$

Both the empty set and $A$ itself are included in $(1).$ For example, if $A=\{0,1\},$ we have:

$$
\mathcal{P}(A)=\{\ \varnothing,\{0\},\{1\},\{0,1\}\ \}
\tag{2}
$$

Every element of $\mathcal{P}(A)$ is therefore a set, and Cantor's theorem, in simple terms, compares the cardinality of $A$ with that of $\mathcal{P}(A).$ Before proceeding, recall also that two sets are [equipotent](../cardinality-and-countable-sets/) if there is a [bijection](../injective-surjective-and-bijective-functions/) between them, a relation denoted by $A\sim B,$ and that no set is equipotent to its own power set. Indeed, for every set $A,$ the map $x\mapsto\{x\}$ is an [injection](../injective-surjective-and-bijective-functions/) from $A$ into $\mathcal{P}(A),$ so $|A|\leq|\mathcal{P}(A)|.$ 

Cantor's theorem states that the power set has strictly greater cardinality than $A,$ that is, the following relation holds:

$$|A|\lt|\mathcal{P}(A)| \tag{3}$$ 

Indeed, no map $f\colon A\to\mathcal{P}(A)$ is [surjective](../injective-surjective-and-bijective-functions/), and consequently there is no bijection between the two sets. To prove this, we take an arbitrary map and construct a subset of $A$ that is not the image of any element. Since each $f(x)$ is a subset of $A,$ we can consider the elements $x$ that do not belong to the subset $f(x)$ assigned to them:

$$
D=\{\ x\in A\mid x\notin f(x)\ \}
\tag{4}
$$

The set $D$ belongs to $\mathcal{P}(A).$ If $D=f(z)$ for some $z\in A,$ there would be two cases. If $z\in D,$ then by $(4)$ we would have $z\notin f(z),$ that is, $z\notin D,$ whereas if $z\notin D,$ we would have $z\notin f(z)$ and hence, by $(4),$ $z\in D,$ giving a contradiction in either case. Thus $D$ is not the image of any element of $A,$ so $f$ is not surjective and, since it is arbitrary, there is no bijection between $A$ and $\mathcal{P}(A).$

For $A=\mathbb{N},$ the theorem shows that the power set of the [natural numbers](../natural-numbers/) is [uncountable](../cardinality-and-countable-sets/). Denoting the cardinality of $\mathcal{P}(A)$ by $2^{|A|}$ and recalling that $|\mathbb{N}|=\aleph_0,$ we obtain:

$$
|\mathcal{P}(\mathbb{N})|=2^{\aleph_0}\gt\aleph_0
\tag{5}
$$

Equation $(5)$ shows that there is an infinite cardinality greater than that of the natural numbers. Applying the theorem again to each successive power set yields ever greater cardinalities, so there is no greatest infinite cardinal.

## Cantor-Bernstein theorem

Another result on the comparison of cardinalities is the Cantor-Bernstein theorem, which states the following for any two sets $A$ and $B$:

$$
|A|\leq|B|\quad\text{and}\quad|B|\leq|A|\quad\Longrightarrow\quad A\sim B
\tag{6}
$$

To prove $(6),$ consider two injections $f\colon A\to B$ and $g\colon B\to A.$ We start with the elements of $A$ outside the image of $g$ and collect those obtained by iterating $g\circ f$:

$$
\begin{align}
A_0 &= A\setminus g(B) \notag \\[6pt]
C &= \bigcup_{n\geq0}(g\circ f)^n(A_0) \tag{7}
\end{align}
$$

Since the term with $n=0$ in $(7)$ is $A_0,$ every element outside $C$ belongs to $g(B),$ and we can define:

$$
h(a)=
\begin{cases}
f(a) & \text{if } a\in C \\[6pt]
g^{-1}(a) & \text{if } a\notin C
\end{cases}
\tag{8}
$$

The function $h$ is injective because the two branches of $(8)$ are injective and have disjoint images, since $g(f(C))\subseteq C.$ Every $b\in B$ is in the image, because if $g(b)\notin C,$ we have $h(g(b))=b,$ whereas if $g(b)\in C,$ then, since $g(b)\notin A_0,$ there is an $a\in C$ with $g(b)=g(f(a)),$ giving $b=f(a)=h(a).$ Thus $h$ is a bijection.

For example, the inclusion from $(0,1)$ into $(0,1]$ and the map $x\mapsto x/2$ in the opposite direction are injective, so $(0,1)\sim(0,1].$ Since $x\mapsto\tan(\pi x-\pi/2)$ is a bijection from $(0,1)$ to $\mathbb{R},$ both [intervals](../intervals/) have the cardinality of the [real numbers](../real-numbers/).

This cardinality is called the cardinality of the continuum and is denoted by $\mathfrak{c}.$ We also recall, without proof, the equipotence of $\mathcal{P}(\mathbb{N})$ and $\mathbb{R},$ from which we obtain:

$$
\mathcal{P}(\mathbb{N})\sim\mathbb{R},\qquad \mathfrak{c}=2^{\aleph_0}
\tag{9}
$$

By $(9),$ equation $(3)$ applied to $A=\mathbb{N}$ becomes $\aleph_0\lt\mathfrak{c},$ confirming that the real numbers are uncountable.

- - -

Another application of the Cantor-Bernstein theorem shows that the square $(0,1)\times(0,1)$ has the same cardinality as the interval $(0,1).$ To show this, we construct an injection from the square into the interval by interleaving the decimal digits of the two coordinates, after choosing for each the expansion that does not end in zeros:

$$
(0.a_1a_2a_3\ldots,\ 0.b_1b_2b_3\ldots)\longmapsto 0.a_1b_1a_2b_2a_3b_3\ldots
\tag{10}
$$

The map in $(10)$ is injective because the digits in odd positions give the first coordinate and those in even positions give the second. The map $x\mapsto(x,1/2)$ gives an injection from the interval into the square, so by $(6)$ we have:

$$
(0,1)\times(0,1)\sim(0,1),\qquad \mathbb{R}^2\sim\mathbb{R}
\tag{11}
$$

The second equipotence in $(11)$ follows from $(0,1)\sim\mathbb{R}$ by applying a bijection to each coordinate. Geometrically, this means that the line and the plane have the same cardinality despite having different dimensions, because a bijection pairs their points without having to preserve their [topological relationships](../topology-of-the-real-line/).
