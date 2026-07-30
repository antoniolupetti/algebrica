---
title: Cardinality and Countable Sets
source: https://algebrica.org/cardinality-and-countable-sets/
license: CC BY-NC 4.0
tags:
  - aleph-numbers
  - cantor-bernstein-theorem
  - cantors-theorem
  - cardinality
  - continuum-hypothesis
  - countable-sets
  - diagonal-argument
  - equipotence
  - power-set
  - transcendental-numbers
  - uncountable-sets
---

## Introduction

The cardinality of a set is its size when order, operations, and other structure are disregarded. For a finite set the cardinality is the number of elements. Two sets have the same cardinality when their elements can be put in one-to-one correspondence. For finite sets this definition agrees with the ordinary count. For infinite sets it compares size without assigning a finite count.

A countable set has either a finite enumeration or an enumeration indexed by the natural numbers. The [integers](../integers/) and the [rational numbers](../rational-numbers/) are countable, although the first contains the natural numbers as a proper subset and the second is dense in the real line. A set is uncountable when no enumeration can contain all its elements. The [real numbers](../real-numbers/) are uncountable, so infinite sets can have unequal cardinalities.

## Equipotent sets

Counting a finite collection means pairing its elements with the numbers $1,2,\ldots,n$ until the collection is exhausted. Two finite collections have the same number of elements exactly when their elements can be matched with none left over on either side. Such a matching is a [bijection](../functions/), and the definition makes sense for finite and infinite sets.

Two sets $A$ and $B$ are equipotent when a bijection $f\colon A\to B$ exists. In that case we write $A\sim B$ and say that $A$ and $B$ have the same cardinality. The relation $\sim$ has the three formal properties of an equivalence relation. The identity map on $A$ gives $A\sim A.$ If $f\colon A\to B$ is a bijection, its [inverse](../inverse-function/) is a bijection from $B$ to $A,$ so $A\sim B$ implies $B\sim A.$ If $f\colon A\to B$ and $g\colon B\to C$ are bijections, the [composition](../composite-functions/) $g\circ f$ is a bijection from $A$ to $C,$ so $A\sim B$ and $B\sim C$ imply $A\sim C.$

> The collection of all sets is not itself a set, so $\sim$ is not an equivalence relation on a set in the usual sense. Axiomatic set theory treats it as a relation between members of a class. Each set has a cardinal number, its cardinality, and two sets have the same cardinal exactly when they are equipotent.

- - -

For finite sets this is the elementary count described in [sets](../sets/), where $|A|=|B|$ precisely when the two sets have equally many elements. For infinite sets, cardinality is defined by the existence of a bijection rather than by a finite count.

Throughout this entry $\mathbb{N}=\{0,1,2,3,\ldots\}$ denotes the [natural numbers](../natural-numbers/) with the convention adopted on this site, and for $n\geq1$ the symbol $I_n$ denotes the initial segment:

$$
I_n=\{\ k\in\mathbb{N}\mid 1\leq k\leq n \ \}
$$

The empty segment is $I_0=\emptyset.$

## Finite and countable sets

A set $A$ is finite with cardinality $n$ when $A\sim I_n,$ and it is countably infinite when $A\sim\mathbb{N}.$ A set is countable when one of the two alternatives holds, and uncountable when neither does. The alternatives are mutually exclusive, since a bijection between $\mathbb{N}$ and $I_n$ would restrict to an injection of $I_{n+1}$ into $I_n,$ which the pigeonhole principle forbids.

> Some texts reserve the word countable for the countably infinite case and use at most countable for the disjunction of the two cases. The convention used here calls a finite set countable, so a countable set is one whose elements can be listed with a first, a second, a third, and so on, the list being finite or endless.

- - -

A bijection $f\colon\mathbb{N}\to A$ is an enumeration of $A.$ With $a_n=f(n),$ the list has the form:

$$
A=\{a_0,a_1,a_2,a_3,\ldots\}
$$

Injectivity means that the terms of the list are pairwise distinct, and surjectivity means that every element of $A$ occupies some position. A countably infinite set is therefore one whose elements can be arranged in an infinite [sequence](../sequences/) without repetitions. The map $n\mapsto n+1$ is a bijection from $\mathbb{N}$ to $\mathbb{N}\setminus\{0\},$ so an enumeration can be indexed by the positive integers as $a_1,a_2,a_3,\ldots$ whenever that indexing is more convenient.

The [integers](../integers/) form a countably infinite set. Define $f\colon\mathbb{N}\to\mathbb{Z}$ by:

$$
f(n)=
\begin{cases}
\dfrac{n}{2} & \text{if } n \text{ is even} \\[6pt]
-\dfrac{n+1}{2} & \text{if } n \text{ is odd}
\end{cases}
$$

The values at even arguments are $0,1,2,3,\ldots,$ and the values at odd arguments are $-1,-2,-3,\ldots.$ These families are disjoint and their union is $\mathbb{Z}.$ Within each family the map is strictly monotonic, hence injective. The enumeration is:

$$
\mathbb{Z}=\{0,-1,1,-2,2,-3,3,\ldots\}
$$

- - -

The set $E=\{\ 2n\mid n\in\mathbb{N} \ \}$ of even natural numbers is countably infinite, since $n\mapsto2n$ is a bijection from $\mathbb{N}$ to $E.$ The set $E$ is a proper subset of $\mathbb{N}$ with the same cardinality. This cannot occur for a finite set, whose proper subsets have fewer elements. Galileo examined the analogous pairing of the natural numbers with their squares in the Discorsi of 1638. Dedekind later called a set infinite when it is equipotent with one of its proper subsets. Such a set is now called Dedekind-infinite, and in ZFC this condition is equivalent to infinitude.

## Infinite subsets of the natural numbers

Every infinite subset $A\subseteq\mathbb{N}$ is countably infinite. The proof constructs an enumeration of $A$ by repeatedly extracting the least remaining element, using the [well-ordering](../natural-numbers/) property of $\mathbb{N}.$ Let $f(0)$ be the least element of $A,$ which exists because $A$ is non-empty, and having defined $f(0),\ldots,f(n)$ let:

$$
f(n+1)=\min\ \bigl(A\setminus\{f(0),\ldots,f(n)\}\bigr)
$$

The set on the right is non-empty, since finitely many chosen elements cannot exhaust $A.$ The minimum therefore exists at every stage, and the recursion defines $f$ on all of $\mathbb{N}.$ Each new value exceeds all previously chosen values. Hence:

$$
f(0)<f(1)<f(2)<\cdots
$$

A strictly increasing map is injective, and induction on this chain gives $f(n)\geq n$ for every $n.$ For surjectivity, fix $a\in A.$ The inequality $f(a)\geq a$ shows that the set of indices $n$ with $f(n)\geq a$ is non-empty, so it has a least element $m.$ If $f(m)>a,$ then minimality of $m$ gives $f(k)<a$ for every $k<m,$ hence $a\neq f(k)$ for those indices and $a$ belongs to $A\setminus\{f(0),\ldots,f(m-1)\}.$ Since $f(m)$ is the least element of that set, the inequality $f(m)\leq a$ follows, contradicting $f(m)>a.$ Therefore $f(m)=a,$ and $f$ is a bijection from $\mathbb{N}$ to $A.$

A subset of a countable set is countable. Let $B$ be countable and $A\subseteq B.$ The claim is immediate when $A$ is empty or $B$ is finite. If $B$ is countably infinite and $A$ is non-empty, take a bijection $h\colon B\to\mathbb{N}.$ The image $h(A)$ is a non-empty subset of $\mathbb{N},$ so it is finite or countably infinite. The restriction $h|_A\colon A\to h(A)$ is a bijection, and $A$ is countable.

## Criteria for countability

For a non-empty set $A,$ countability is equivalent to either of two one-sided conditions. The following statements are equivalent:

+ $A$ is countable.
+ A surjective map $f\colon\mathbb{N}\to A$ exists.
+ An injective map $g\colon A\to\mathbb{N}$ exists.

Assume the first condition. If $A$ is countably infinite, an enumeration of $A$ is already a surjection of the kind required by the second condition. If $A$ is finite with cardinality $n\geq1,$ take a bijection $h\colon A\to I_n$ and define $s\colon\mathbb{N}\to I_n$ by $s(k)=k$ for $1\leq k\leq n$ and $s(k)=n$ for all other $k.$ The map $s$ is surjective, so $f=h^{-1}\circ s$ is a surjection from $\mathbb{N}$ to $A.$

Assume the second condition. Surjectivity makes the fibre $f^{-1}(\{a\})$ non-empty for each $a\in A.$ As a subset of $\mathbb{N},$ this fibre has a least element. Set $g(a)=\min f^{-1}(\{a\}).$ The fibres over distinct elements are disjoint, so their least elements differ and $g$ is injective.

Assume the third condition. The image $g(A)$ is a non-empty subset of $\mathbb{N},$ hence countable by the previous section. The map $g\colon A\to g(A)$ is a bijection, so $A$ is countable.

> The statement remains valid with $\mathbb{N}$ replaced by any countably infinite set $C.$ If $b\colon C\to\mathbb{N}$ is a bijection, then $f\circ b\colon C\to A$ is surjective whenever $f\colon\mathbb{N}\to A$ is surjective. If $g\colon A\to\mathbb{N}$ is injective, then $b^{-1}\circ g\colon A\to C$ is injective.

- - -

The second condition permits repetitions, so a list in which some elements occur more than once still proves countability. The third condition requires an injective encoding by natural numbers but does not require every natural number to be used.

## Products and unions of countable sets

The product $\mathbb{N}\times\mathbb{N}$ is countably infinite. Group the pairs according to the sum of their coordinates. For each $s\in\mathbb{N}$ exactly $s+1$ pairs $(j,k)$ satisfy $j+k=s.$ Each group is finite, every pair belongs to one group, and the groups can be listed in increasing order of $s:$

$$
\mathbb{N}\times\mathbb{N}=\{(0,0),\ (1,0),\ (0,1),\ (2,0),\ (1,1),\ (0,2),\ (3,0),\ldots\}
$$

The groups with sum smaller than $s$ contain $1+2+\cdots+s$ pairs. Within the group of sum $s,$ the pair $(j,k)$ has zero-based position $k.$ Substituting $s=j+k$ gives the map:

$$
\pi(j,k)=\frac{(j+k)(j+k+1)}{2}+k
$$

The first values are $\pi(0,0)=0,$ $\pi(1,0)=1,$ $\pi(0,1)=2,$ $\pi(2,0)=3,$ $\pi(1,1)=4$ and $\pi(0,2)=5.$ The map $\pi$ is a bijection from $\mathbb{N}\times\mathbb{N}$ to $\mathbb{N}$ and is called the Cantor pairing function.

Equipotence is compatible with products. Suppose $A\sim C$ and $B\sim D,$ with bijections $f\colon A\to C$ and $g\colon B\to D.$ Define the product map by:

$$
h\colon A\times B\to C\times D,\qquad h(a,b)=(f(a),g(b))
$$

The map $h$ is a bijection. Injectivity follows because $h(a,b)=h(a',b')$ forces $f(a)=f(a')$ and $g(b)=g(b'),$ hence $a=a'$ and $b=b'.$ Surjectivity follows because any $(c,d)\in C\times D$ is the image of the pair $(f^{-1}(c),g^{-1}(d)).$ Combining this with the previous result gives $\mathbb{Z}\times\mathbb{Z}\sim\mathbb{N}\times\mathbb{N}\sim\mathbb{N},$ and [induction](../principle-of-mathematical-induction/) on the number of factors gives $\mathbb{N}^k\sim\mathbb{N}$ for every $k\geq1.$ More generally, the product of finitely many countable sets is countable, since each factor injects into $\mathbb{N}$ and the induced map into $\mathbb{N}^k$ is injective.

- - -

The union of a countable family of countable sets is countable. Let $(A_i)_{i\in\mathbb{N}}$ be countable sets, not necessarily disjoint. If their union is empty, the claim is immediate. Otherwise, fix $a$ in the union and replace each empty $A_i$ by $\{a\}.$ This does not change the union, and all sets in the family are now non-empty. For each $i$ take a surjection $f_i\colon\mathbb{N}\to A_i$ and define:

$$
F\colon\mathbb{N}\times\mathbb{N}\to\bigcup_{i\in\mathbb{N}}A_i,\qquad F(i,j)=f_i(j)
$$

Given $x$ in the union, some index $i$ satisfies $x\in A_i.$ Since $f_i$ is surjective, some $j$ satisfies $x=f_i(j)=F(i,j).$ Thus $F$ is surjective. Its composition with the inverse of the pairing function is a surjection from $\mathbb{N}$ onto the union, which is therefore countable.

> The simultaneous selection of the maps $f_i$ uses the axiom of countable choice. When a rule specifies all the maps, no choice principle is needed.

The [rational numbers](../rational-numbers/) are countably infinite. Every rational number is a quotient of an integer by a positive integer. Consider the map:

$$
q\colon\mathbb{Z}\times(\mathbb{N}\setminus\{0\})\to\mathbb{Q},\qquad q(p,n)=\frac{p}{n}
$$

The map $q$ is surjective but not injective, since $2/4$ and $1/2$ have the same image. Its domain is countably infinite, so the surjective criterion proves that $\mathbb{Q}$ is countable. Since $\mathbb{Q}$ contains $\mathbb{Z},$ it is countably infinite. The entry on [rational numbers](../rational-numbers/) proves the same result by traversing a table of fractions and discarding those not in lowest terms.

## The uncountability of the real numbers

The proof that $\mathbb{R}$ has no enumeration uses decimal expansions. Some [real numbers](../real-numbers/) have two such expansions. For example, the equality below is exact:

$$
0.999\ldots=1
$$

The [geometric series](../geometric-series/) calculation is:

$$
0.999\ldots=\sum_{n=1}^{\infty}\frac{9}{10^n}=\frac{9/10}{1-1/10}=1
$$

Every number with a terminating expansion has this duplication, for instance $0.42=0.41999\ldots,$ and all other real numbers have one decimal expansion. To obtain a unique digit string, retain the expansion that is not eventually $0.$ Thus $0.41999\ldots$ is retained and $0.42$ is discarded. With this convention each $x\in(0,1]$ has exactly one expansion:

$$
x=0.a_1a_2a_3\ldots,\qquad a_n\in\{0,1,\ldots,9\}
$$

The digits in this expansion are not eventually all $0.$ Conversely, every such digit string is the retained expansion of exactly one $x\in(0,1].$

The interval $(0,1]$ is uncountable. Suppose it were countable. Being infinite, it would then be countably infinite, and its elements could be enumerated as $x_1,x_2,x_3,\ldots$ with the digits of each term arranged in an infinite array:

$$
\begin{align}
x_1&=0.a_{11}a_{12}a_{13}a_{14}\ldots \\[6pt]
x_2&=0.a_{21}a_{22}a_{23}a_{24}\ldots \\[6pt]
x_3&=0.a_{31}a_{32}a_{33}a_{34}\ldots \\[6pt]
x_4&=0.a_{41}a_{42}a_{43}a_{44}\ldots
\end{align}
$$

The diagonal entries $a_{11},a_{22},a_{33},\ldots$ determine a number absent from the array. The digits $d_n$ are defined by:

$$
d_n=
\begin{cases}
6 & \text{if } a_{nn}=5 \\[6pt]
5 & \text{if } a_{nn}\neq5
\end{cases}
$$

Let $y$ have the expansion $0.d_1d_2d_3\ldots$ Every digit of $y$ lies in $\{5,6\},$ so the string is not eventually $0$ and is the retained expansion of an element $y\in(0,1].$ For each $n$ the inequality $d_n\neq a_{nn}$ shows that $y$ and $x_n$ differ in their $n$-th digits. The retained expansions are unique, hence $y\neq x_n$ for every $n.$ Thus $y$ is absent from the enumeration, contrary to surjectivity.

The digits $5$ and $6$ ensure that the constructed expansion is the retained one. If modified digits were allowed to end in zeros, the displayed expansion might be discarded in favour of a second expansion, and a digitwise comparison with the retained expansions of the $x_n$ would be invalid.

> Suppose the first four terms of the enumeration begin with $0.1203\ldots,$ $0.1557\ldots,$ $0.2460\ldots$ and $0.3141\ldots.$ The diagonal digits are $1,$ $5,$ $6$ and $1,$ so the constructed number begins with $0.5655\ldots.$ It differs from each of those four terms in the corresponding diagonal position.

- - -

The real numbers are uncountable, because every subset of a countable set is countable. Cantor's first proof, published in 1874, used nested intervals rather than digits. The entry on [real numbers](../real-numbers/) gives that proof from completeness. His diagonal construction appeared in 1891.

The convention on expansions can be carried out in any base $r\geq2,$ with digits ranging over $\{0,1,\ldots,r-1\}.$ Base $2$ is the case used below, where $(0,1]$ corresponds to the binary strings that are not eventually $0.$

## The power set of the natural numbers

A sequence of binary digits can be read as a description of a subset. Let $\{0,1\}^{\mathbb{N}}$ denote the set of all maps $\varphi\colon\mathbb{N}\to\{0,1\}.$ A subset $A\subseteq\mathbb{N}$ determines its characteristic function:

$$
\chi_A(n)=
\begin{cases}
1 & \text{if } n\in A \\[6pt]
0 & \text{if } n\notin A
\end{cases}
$$

A map $\varphi\colon\mathbb{N}\to\{0,1\}$ determines the subset $\varphi^{-1}(\{1\}).$ The two constructions are inverse to each other, so the [power set](../sets/) of $\mathbb{N}$ is equipotent with the set of binary sequences:

$$
\mathcal{P}(\mathbb{N})\sim\{0,1\}^{\mathbb{N}}
$$

The set $\{0,1\}^{\mathbb{N}}$ is uncountable, by a diagonal argument that no longer needs any convention about representations. Suppose the binary sequences could be enumerated as $\varphi_1,\varphi_2,\varphi_3,\ldots$ and define $\psi(n)=1-\varphi_n(n).$ The values of $\psi$ lie in $\{0,1\},$ so $\psi$ is a binary sequence, and $\psi(n)\neq\varphi_n(n)$ shows that $\psi$ differs from $\varphi_n$ at the argument $n.$ Hence $\psi$ appears nowhere in the enumeration. The set of binary sequences admits no enumeration, and $\mathcal{P}(\mathbb{N})$ is uncountable as well.

If $\varphi_n$ is the characteristic function of $A_n\subseteq\mathbb{N},$ then $\psi$ is the characteristic function of $\{\ n\in\mathbb{N}\mid n\notin A_n\ \}.$

## Cantor's theorem

No set is equipotent with its power set. For any set $A$ the map $x\mapsto\{x\}$ is an injection from $A$ into $\mathcal{P}(A),$ so $|A|\leq|\mathcal{P}(A)|.$ Cantor's theorem states that no map $f\colon A\to\mathcal{P}(A)$ is surjective, and therefore the inequality is strict.

Let $f\colon A\to\mathcal{P}(A)$ be any map, so that $f(x)$ is a subset of $A$ for each $x\in A.$ Consider the set of elements that do not belong to the subset assigned to them:

$$
D=\{\ x\in A\mid x\notin f(x) \ \}
$$

Then $D$ is a subset of $A,$ hence an element of $\mathcal{P}(A),$ and $D$ lies outside the image of $f.$ Suppose $D=f(z)$ for some $z\in A.$ If $z\in D,$ the defining condition of $D$ gives $z\notin f(z)=D,$ a contradiction. If $z\notin D,$ then $z\notin f(z),$ which is the defining condition of $D$ and gives $z\in D,$ again a contradiction. Both alternatives fail, so no such $z$ exists and $f$ is not surjective. In particular $f$ is not a bijection, and $A\sim\mathcal{P}(A)$ is impossible.

For $A=\mathbb{N}$ the theorem gives another proof that $\mathcal{P}(\mathbb{N})$ is uncountable. Iterating the power-set construction gives the chain:

$$
A,\quad \mathcal{P}(A),\quad \mathcal{P}(\mathcal{P}(A)),\quad \ldots
$$

Each term has larger cardinality than its predecessor, so no infinite cardinal is the largest. In general, $2^{|A|}$ denotes $|\mathcal{P}(A)|,$ extending the identity $|\mathcal{P}(A)|=2^n$ for a finite set with $n$ elements. Since $|\mathbb{N}|=\aleph_0,$ we have:

$$
|\mathcal{P}(\mathbb{N})|=2^{\aleph_0}
$$

Cantor's theorem gives $\aleph_0<2^{\aleph_0}.$

> The diagonal set $D$ is built by the same device as Russell's paradox, where the collection of all sets that are not members of themselves leads to a contradiction. In Cantor's theorem the construction is harmless, since $D$ is extracted from a set $A$ that is given in advance, and the conclusion is a statement about $f$ rather than an inconsistency.

## Comparing cardinalities and the Cantor-Bernstein theorem

Cardinalities are compared through injections. We write $|A|\leq|B|$ when an injection from $A$ into $B$ exists. The relation is reflexive because the identity map is injective, and it is transitive because compositions of injections are injective. Its antisymmetry is the Cantor-Bernstein theorem.

The Cantor-Bernstein theorem states that injections $f\colon A\to B$ and $g\colon B\to A$ together imply $A\sim B.$ Cantor stated it in 1887 without a proof, Dedekind proved it the same year in a note he left unpublished, and Bernstein found the argument that became standard in 1897, while attending Cantor's seminar.

The proof combines the two injections into a single bijection by deciding, for each element of $A,$ whether to apply $f$ or the inverse of $g.$ Let $A_0=A\setminus g(B)$ be the set of elements outside the image of $g,$ and define:

$$
C=\bigcup_{n\geq0}(g\circ f)^n(A_0)
$$

The set $C$ consists of the elements obtained from $A_0$ by iterating $g\circ f,$ with $n=0$ giving $A_0$ itself. Define:

$$
h(a)=
\begin{cases}
f(a) & \text{if } a\in C \\[6pt]
g^{-1}(a) & \text{if } a\notin C
\end{cases}
$$

The second line makes sense because $a\notin C$ implies $a\notin A_0,$ so $a=g(b)$ for a unique $b\in B.$ To see that $h$ is injective, note that both branches are injective and their images are disjoint. An element $f(a)$ with $a\in C$ cannot equal $g^{-1}(a')$ for some $a'\notin C,$ since $a'=g(f(a))$ would place $a'$ inside $C.$ To see that $h$ is surjective, take $b\in B.$ If $g(b)\notin C,$ then $h(g(b))=b.$ If $g(b)\in C,$ then $g(b)\in(g\circ f)^n(A_0)$ for some $n\geq1,$ because $g(b)\notin A_0,$ so $g(b)=g(f(a))$ for some $a\in(g\circ f)^{n-1}(A_0)\subseteq C,$ and injectivity of $g$ gives $b=f(a)=h(a).$ Hence $h$ is a bijection.

The theorem reduces many comparisons to the construction of two injections. The inclusion $(0,1)\subseteq(0,1]$ is injective, and $x\mapsto x/2$ is an injection in the opposite direction. Hence $(0,1)\sim(0,1].$ The [tangent function](../tangent-function/) $x\mapsto\tan(\pi x-\pi/2)$ is a bijection from $(0,1)$ to $\mathbb{R},$ so $(0,1),$ $(0,1]$ and $\mathbb{R}$ are equipotent. In particular, every non-degenerate [interval](../intervals/) is uncountable.

- - -

Write $\mathfrak{c}=|\mathbb{R}|.$ To compare $\mathfrak{c}$ with $2^{\aleph_0},$ send each $A\subseteq\mathbb{N}$ to the real number whose $(n+1)$-st decimal digit is $1$ when $n\in A$ and $0$ otherwise. Distinct subsets have distinct images, since decimal strings containing only zeros and ones cannot be alternative expansions of each other. This is an injection from $\mathcal{P}(\mathbb{N})$ into $\mathbb{R}.$ Conversely, retained binary expansions define an injection from $(0,1]$ into $\{0,1\}^{\mathbb{N}}\sim\mathcal{P}(\mathbb{N}),$ and $(0,1]\sim\mathbb{R}.$ The Cantor-Bernstein theorem gives:

$$
\mathcal{P}(\mathbb{N})\sim\mathbb{R}
$$

Thus $\mathfrak{c}=2^{\aleph_0}.$ The [irrational numbers](../irrational-numbers/) also have cardinality $\mathfrak{c}.$ To prove the reverse of the inclusion $\mathbb{R}\setminus\mathbb{Q}\subseteq\mathbb{R},$ enumerate the rationals as $\mathbb{Q}=\{q_0,q_1,q_2,\ldots\}$ and set $r_n=\sqrt{2}+n.$ The values $r_n$ are distinct irrational numbers. Define $J\colon\mathbb{R}\to\mathbb{R}\setminus\mathbb{Q}$ by:

$$
J(x)=
\begin{cases}
r_{2n} & \text{if } x=q_n \\[6pt]
r_{2n+1} & \text{if } x=r_n \\[6pt]
x & \text{otherwise}
\end{cases}
$$

The three branches have disjoint images, and each branch is injective. Thus $J$ is injective, and the Cantor-Bernstein theorem gives $\mathbb{R}\setminus\mathbb{Q}\sim\mathbb{R}.$

> The relation $\leq$ between cardinalities is a partial order after the Cantor-Bernstein theorem, and no choice principle is needed for that theorem. The stronger statement that any two cardinalities are comparable, so that $|A|\leq|B|$ or $|B|\leq|A|$ always holds, is equivalent to the axiom of choice.

## Cardinality and dimension

The unit square and the unit interval are equipotent, so cardinality does not detect dimension. Define a map from $(0,1)\times(0,1)$ into $(0,1)$ by interleaving retained decimal expansions. For inputs $0.a_1a_2a_3\ldots$ and $0.b_1b_2b_3\ldots,$ the map is:

$$
(0.a_1a_2a_3\ldots,\ 0.b_1b_2b_3\ldots)\longmapsto 0.a_1b_1a_2b_2a_3b_3\ldots
$$

The odd-position digits recover the first argument and the even-position digits recover the second, so the map is injective. It is not surjective. The number with expansion $0.505050\ldots$ would require a second coordinate with all digits equal to $0,$ which is not an element of $(0,1).$ In the opposite direction, $x\mapsto(x,1/2)$ is injective. The Cantor-Bernstein theorem gives:

$$
(0,1)\times(0,1)\sim(0,1)
$$

Since $(0,1)\sim\mathbb{R},$ we have $\mathbb{R}^2\sim\mathbb{R}.$ By induction, $\mathbb{R}^n\sim\mathbb{R}$ for every $n\geq1,$ or $\mathfrak{c}^n=\mathfrak{c}$ in cardinal notation. Countably many factors have the same cardinality because:

$$
\mathfrak{c}^{\aleph_0}=(2^{\aleph_0})^{\aleph_0}=2^{\aleph_0\cdot\aleph_0}=2^{\aleph_0}=\mathfrak{c}
$$

Hence the set $\mathbb{R}^{\mathbb{N}}$ of real sequences is equipotent with $\mathbb{R}.$

Cantor obtained the equipotence of the square with the segment in 1877 and reported it to Dedekind with the remark that he saw it without believing it. The result does not contradict the geometric distinction between a line and a plane, because the bijection is discontinuous. A bijection $\mathbb{R}^2\to\mathbb{R}$ continuous in both directions does not exist, a fact established by Brouwer in 1911 in his work on the invariance of dimension. Cardinality counts points and ignores the way they are arranged, while dimension depends on the [topology](../topology-of-the-real-line/).

## The continuum hypothesis

Cantor asked whether a cardinal can lie strictly between $\aleph_0$ and $\mathfrak{c}.$ The continuum hypothesis says that no such cardinal exists. If $\aleph_1$ denotes the least uncountable cardinal, the hypothesis is the equality:

$$
2^{\aleph_0}=\aleph_1
$$

The axioms of Zermelo-Fraenkel set theory with the axiom of choice, abbreviated ZFC, do not decide the continuum hypothesis. Assuming ZFC is consistent, Gödel's constructible universe proves that ZFC together with the continuum hypothesis is consistent. Cohen's forcing method proves that ZFC together with the negation of the continuum hypothesis is also consistent. Gödel obtained the first result in 1938, and Cohen obtained the second in 1963. The same relative independence holds for the generalised continuum hypothesis, which states that $2^{\aleph_\alpha}=\aleph_{\alpha+1}$ for every ordinal $\alpha.$

## Applications to sets of numbers and functions

The algebraic numbers are countable, as Cantor proved in 1874. A real number is algebraic when it is a root of a nonzero [polynomial](../polynomials/) with integer coefficients. Fix $n,H\in\mathbb{N}.$ Only finitely many polynomials have degree at most $n$ and coefficients satisfying $|c_i|\leq H,$ and each nonzero polynomial has at most $n$ real roots. Every algebraic number belongs to one of these finite root sets for some pair $(n,H).$ Since $\mathbb{N}\times\mathbb{N}$ is countable, the algebraic numbers are a countable union of finite sets and are countable. Their complement in $\mathbb{R},$ the set of [transcendental numbers](../irrational-numbers/), is uncountable.

- - -

The set of finite sequences of natural numbers is $\bigcup_{k\geq0}\mathbb{N}^k,$ where $\mathbb{N}^0$ contains the empty sequence. Each $\mathbb{N}^k$ is countable, so their union is countable. The finite subsets of $\mathbb{N}$ are countable as well, since each is determined by the increasing sequence of its elements. Consequently, the collection of infinite subsets of $\mathbb{N}$ is uncountable. Otherwise it and the collection of finite subsets would form a countable partition of $\mathcal{P}(\mathbb{N}),$ contrary to Cantor's theorem.

- - -

The [continuous functions](../continuous-functions/) from $\mathbb{R}$ to $\mathbb{R}$ have cardinality $\mathfrak{c}.$ A continuous function is determined by its restriction to $\mathbb{Q},$ because two continuous functions that agree on a dense set agree everywhere. Restriction is an injection into the set of all maps $\mathbb{Q}\to\mathbb{R},$ whose cardinality is $\mathfrak{c}^{\aleph_0}=\mathfrak{c}.$ The constant functions give an injection from $\mathbb{R}$ into the continuous functions. The Cantor-Bernstein theorem proves that the continuous functions have cardinality $\mathfrak{c}.$

The set of all functions from $\mathbb{R}$ to $\mathbb{R}$ has cardinality:

$$
\mathfrak{c}^{\mathfrak{c}}=(2^{\aleph_0})^{\mathfrak{c}}=2^{\aleph_0\cdot\mathfrak{c}}=2^{\mathfrak{c}}
$$

Cantor's theorem gives $\mathfrak{c}<2^{\mathfrak{c}},$ so the set of all functions has larger cardinality than the set of continuous functions.
