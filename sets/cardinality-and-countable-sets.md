---
title: Cardinality and Countable Sets
source: https://algebrica.org/cardinality-and-countable-sets/
license: CC BY-NC 4.0
tags:
  - cardinality
  - countable-sets
  - diagonal-argument
  - equipotence
  - transcendental-numbers
  - uncountable-sets
---

## Finite and countable sets

The cardinality of a finite set $A$ is the number of its elements and is denoted by $|A|.$ Counting the elements means matching them with the numbers $1,2,\ldots,n,$ assigning a different number to each element and using every number from $1$ to $n.$ When $A$ is empty, its cardinality is $0.$ For example, we denote the set of [natural numbers](../natural-numbers/) as follows:

$$\mathbb{N}=\{0,1,2,3,\ldots\} \tag{1}$$
For each $n\in\mathbb{N},$ with $\mathbb{N}$ defined in $(1),$ we set:

$$
I_n=\{\ k\in\mathbb{N}\mid 1\leq k\leq n \ \} \tag{2}
$$

Thus $I_n$ contains exactly $n$ elements, so for example $I_3=\{1,2,3\}.$ A set $A$ has finite cardinality $n$ if there is a [one-to-one correspondence](../injective-surjective-and-bijective-functions/) between $A$ and $I_n,$ that is, a bijective relation in which each element of $A$ corresponds to exactly one element of $I_n$ and vice versa. Using the same relation, we can also compare any two infinite sets $A$ and $B,$ which are called equipotent when there is a map $f\colon A\to B$ that establishes a one-to-one correspondence between their elements. Equipotence and equality of cardinalities are expressed by the following relation:

$$
A\sim B \iff |A|=|B| \tag{3}
$$

For finite sets, $(3)$ expresses the fact that the two sets have the same number of elements. We now consider countability, which, as mentioned at the beginning, expresses the possibility of listing all the elements of a set without repetitions, with each element occupying a position identified by a natural number. A set $A$ is countably infinite when it is equipotent with the set of natural numbers. A set is countable if it is finite or countably infinite, and uncountable if neither case applies. A finite set cannot be equipotent with $\mathbb{N}$ because, if it contains $n$ elements, matching each of them with a different natural number uses only $n$ natural numbers, whereas, as stated above, a one-to-one correspondence must include every element of both sets.

The equipotence relation $\sim,$ introduced in $(3),$ therefore relates sets of the same cardinality and satisfies the reflexive, symmetric, and transitive properties, as shown in the following statements:

$$
\begin{align}
&A\sim A \\[6pt]
&A\sim B \implies B\sim A \\[6pt]
&A\sim B \text{ and } B\sim C \implies A\sim C
\end{align} \tag{4}
$$

In $(4),$ the first relation expresses reflexivity and follows from the fact that the identity map is a bijection from any set $A$ onto itself. The second relation expresses symmetry and follows from the fact that every bijection $f\colon A\to B$ has an [inverse bijection](../inverse-function/) $f^{-1}\colon B\to A.$ The third relation expresses transitivity, which follows from the fact that, given two bijections $f\colon A\to B$ and $g\colon B\to C,$ their [composition](../composite-functions/) $g\circ f$ is again a bijection from $A$ to $C.$

When we choose a bijection $f\colon\mathbb{N}\to A$ and associate each natural number $n$ with the element $a_n=f(n),$ we obtain an enumeration of $A,$ that is, a list of its elements that can be written as follows:

$$
A=\{a_0,a_1,a_2,a_3,\ldots\} \tag{5}
$$

In $(5),$ the [injectivity](../injective-surjective-and-bijective-functions/) of $f$ ensures that different indices correspond to different elements, so no element ever appears twice, while [surjectivity](../injective-surjective-and-bijective-functions/) ensures that every element of $A$ appears in the list. For example, to prove that the set $\mathbb{Z}$ is countably infinite, we construct an enumeration of the form $(5)$ that includes zero, the [positive integers](../integers/), and the negative integers, defining a map $f\colon\mathbb{N}\to\mathbb{Z}$ by:

$$
f(n)=
\begin{cases}
\dfrac{n}{2} & \text{if } n \text{ is even} \\[6pt]
-\dfrac{n+1}{2} & \text{if } n \text{ is odd}
\end{cases} \tag{6}
$$

We now write an even index as $n=2k$ and an odd index as $n=2k+1,$ with $k\in\mathbb{N},$ and substitute these expressions into $(6)$ to obtain:

$$
\begin{align}
&f(2k)=k \\[6pt]
&f(2k+1)=-(k+1)
\end{align} \tag{7}
$$

The first line of $(7)$ shows that the even indices produce all the non-negative integers, while the second equality shows that the odd indices produce all the negative integers. Since the two groups are disjoint and together contain all of $\mathbb{Z},$ the map in $(6)$ is both injective and surjective, and hence is a bijection. To obtain the enumeration, we simply follow the indices in the order $n=0,1,2,3,\ldots,$ which gives:

$$
\mathbb{Z}=\{0,-1,1,-2,2,-3,3,\ldots\} \tag{8}
$$

Since every integer appears exactly once in $(8),$ we can conclude that $\mathbb{Z}$ is countably infinite. For another example, we consider the set $E$ of even natural numbers and show that it is countably infinite:

$$E=\{\ 2n\mid n\in\mathbb{N} \ \} \tag{9}$$

By $(9),$ the map $n\mapsto2n$ assigns a distinct even number to each natural number and reaches every element of $E,$ so it is a bijection from $\mathbb{N}$ to $E,$ and therefore $E$ is countably infinite. Furthermore, $E$ is called a [proper subset](../sets/) of $\mathbb{N}$ because it does not contain the odd numbers, yet it has the same cardinality as $\mathbb{N}.$ Notice that this property does not hold for a finite set, because every proper subset has fewer elements than the set containing it.

## Infinite subsets of the natural numbers

The example of the even numbers in $(9)$ shows how an infinite subset of the natural numbers can have the same cardinality as $\mathbb{N}.$ We now show that this holds for every infinite subset $A\subseteq\mathbb{N},$ and to prove it we list the elements of $A$ in increasing order, choosing at each step the smallest element not yet listed. This choice is possible because the natural numbers are [well-ordered](../natural-numbers/), meaning that every non-empty subset has a least element. We therefore define $f(0)=\min A.$ Once $f(0),\ldots,f(n)$ have been chosen, the next term is given by the following equality:

$$
f(n+1)=\min\ \bigl(A\setminus\{f(0),\ldots,f(n)\}\bigr) \tag{10}
$$

The construction in $(10)$ can continue for every $n\in\mathbb{N},$ and after each choice all the remaining elements are greater than the minimum just chosen, so the next value is necessarily greater than the previous one. Moreover, since the values are natural numbers, each increase is at least $1,$ so starting from $f(0)\geq0$ we obtain the following for every $n\in\mathbb{N}$:

$$
\begin{align}
&f(0)\lt f(1)\lt f(2)\lt\cdots \\[6pt]
&f(n)\geq n
\end{align} \tag{11}
$$

The first line of $(11)$ proves that $f$ is injective, because different indices correspond to different values. To prove surjectivity, suppose for a contradiction that there is an element $a\in A$ that is never reached by $f,$ meaning that $f(n)\neq a$ for every $n\in\mathbb{N}.$ Notice that when we choose $f(a),$ the element $a$ is still available, and since $(10)$ requires us to choose the least remaining element, we have:

$$f(a)\leq a \tag{12}$$

Combining $(12)$ with the second line of $(11)$ gives:

$$
a\leq f(a)\leq a \implies f(a)=a \tag{13}
$$

Equation $(13)$ gives $f(a)=a,$ contradicting the assumption that $f(n)\neq a,$ so every element of $A$ is reached, and hence $f$ is a bijection from $\mathbb{N}$ to $A,$ making $A$ countably infinite. It follows that every subset of a countable set is countable. Indeed, suppose $B$ is countable and $A\subseteq B.$ If $B$ is finite, then $A$ is necessarily finite as well. When $B$ is countably infinite, we choose a bijection $h\colon B\to\mathbb{N}$ and restrict its domain to $A$ to obtain a bijection between $A$ and its image:

$$
h|_A\colon A\to h(A) \tag{14}
$$

Thus, by $(14),$ we conclude that every subset $A$ of a countable set $B$ is countable.

## Criteria for countability

In the examples of the integers and the even natural numbers, we proved countability by constructing a bijection with $\mathbb{N}.$ We now show how to obtain the same result without constructing a bijection.

We can allow repetitions in the list of elements, or assign distinct natural numbers to the elements without using every natural number.

We have two criteria. The first allows repetitions in the list by requiring a surjective map from the natural numbers to $A,$ which we can write as:

$$
f\colon\mathbb{N}\to A \text{ surjective} \tag{15}
$$

Condition $(15)$ allows us to list all the elements of $A,$ with the same element allowed to appear more than once. The second criterion instead requires an injective map defined as follows:

$$
g\colon A\to\mathbb{N} \text{ injective} \tag{16}
$$

We prove that each of conditions $(15)$ and $(16)$ is equivalent to the countability of a non-empty set $A.$ We begin with the case in which $A$ is countable and construct a surjective map from $\mathbb{N}$ to $A,$ as required by $(15).$ If $A$ is infinite, the enumeration $(5)$ already provides a bijection and hence a surjection. If instead $A$ is finite with $m\geq1$ elements, we can list them as $a_0,\ldots,a_{m-1}$ and define:

$$
f(k)=
\begin{cases}
a_k & \text{if } 0\leq k<m \\[6pt]
a_0 & \text{if } k\geq m
\end{cases} \tag{17}
$$

In $(17),$ the values $f(0),\ldots,f(m-1)$ include all the elements of $A,$ while the subsequent values repeat $a_0,$ so $f$ is surjective in this case as well. We now show how a surjective map of the form $(15)$ gives an injection of the form $(16).$ Given $a\in A,$ we consider all the indices $n$ for which $f(n)=a$ and choose the smallest, so that:

$$
g(a)=\min\{\ n\in\mathbb{N}\mid f(n)=a \ \} \tag{18}
$$

The set defined in $(18)$ is non-empty because $f$ is surjective, so it has a least element by the well-ordering principle for the natural numbers mentioned earlier. Since $g(a)$ is the first index at which $f$ takes the value $a,$ applying $f$ to that index gives:

$$
f(g(a))=a \tag{19}
$$

If $g(a)=g(b),$ applying $f$ to both sides would give $f(g(a))=f(g(b)),$ and by $(19)$ the left-hand side is $a$ and the right-hand side is $b,$ so $a=b.$ The same index therefore cannot be assigned to two distinct elements, so $g$ is injective.

Finally, an injection of the form $(16)$ puts $A$ in one-to-one correspondence with the set of natural numbers actually used, namely the image $g(A).$ In the section 'Infinite subsets of the natural numbers', we proved that every subset of a countable set is countable, so $g(A)\subseteq\mathbb{N}$ is countable as well. Since $A$ is equipotent with $g(A),$ it too is countable. We have thus proved that countability implies $(15),$ that $(15)$ implies $(16),$ and that $(16)$ in turn implies countability. In general, $\mathbb{N}$ in criteria $(15)$ and $(16)$ can be replaced by any countably infinite set, since such a set is equipotent with $\mathbb{N}.$

## Products and unions of countable sets

We now show why the product of finitely many countable sets is still countable. We begin with $\mathbb{N}\times\mathbb{N},$ whose elements are pairs of natural numbers, and construct an enumeration that includes every pair without repetitions. To do so, we first group all pairs $(j,k)$ according to the sum $s=j+k.$ For each $s,$ the group contains the $s+1$ pairs of the form:

$$(s,0),(s-1,1),\ldots,(0,s)$$

Listing the resulting groups in increasing order of their sums gives:

$$
\mathbb{N}\times\mathbb{N}=\{(0,0),\ (1,0),\ (0,1),\ (2,0),\ (1,1),\ (0,2),\ (3,0),\ldots\} \tag{20}
$$

Every pair appears in the list $(20)$ because it is preceded by finitely many groups, each containing finitely many pairs. The groups with sum less than $s$ contain a total of $s(s+1)/2$ pairs. Within the group with sum $s,$ the pair $(j,k)$ occupies position $k,$ counting from zero. Substituting $s=j+k,$ its index in the list is therefore:

$$
\pi(j,k)=\frac{(j+k)(j+k+1)}{2}+k \tag{21}
$$

Formula $(21)$ assigns the consecutive indices $0,1,2,\ldots$ to the pairs in $(20),$ without repeating or omitting any index, so it is a bijection from $\mathbb{N}\times\mathbb{N}$ to $\mathbb{N},$ also called the Cantor pairing function. We can extend the result of $(21)$ to other sets by observing that replacing the factors with equipotent sets does not change the cardinality of the product. Suppose $f\colon A\to C$ and $g\colon B\to D$ are bijections, and define:

$$
\begin{align}
&h\colon A\times B\to C\times D \\[6pt]
&h(a,b)=(f(a),g(b))
\end{align} \tag{22}
$$

The map in $(22)$ is injective because equality of the images implies $f(a)=f(a')$ and $g(b)=g(b'),$ hence $a=a'$ and $b=b'.$ The map is also surjective because every pair $(c,d)$ is the image of $(f^{-1}(c),g^{-1}(d)),$ and therefore $A\times B\sim C\times D,$ meaning that the two [Cartesian products](../cartesian-product/) have the same cardinality. Since $\mathbb{Z}\sim\mathbb{N},$ applying $(22)$ and then $(21),$ and repeating the procedure for finitely many factors, gives:

$$
\begin{align}
&\mathbb{Z}\times\mathbb{Z}\sim\mathbb{N}\times\mathbb{N}\sim\mathbb{N} \\[6pt]
&\mathbb{N}^k\sim\mathbb{N} \qquad \text{for every } k\geq1
\end{align} \tag{23}
$$

To extend $(23)$ to the product of any $k$ countable sets, we assign distinct natural numbers to the elements of each factor, obtaining an injection from the product into the set $\mathbb{N}^k$ of $k$-tuples of natural numbers. Since $(23)$ provides a bijection between $\mathbb{N}^k$ and $\mathbb{N},$ composing the two maps gives an injection from the product into $\mathbb{N},$ which proves its countability by criterion $(16),$ while if a factor is empty, the product is empty and hence finite.

- - -

We now turn to unions of countable sets, showing that the union of a countable family of countable sets is still countable, even when the sets have elements in common. Consider, for example, the following union:

$$U=\bigcup_{i\in\mathbb{N}}A_i \tag{24}$$
If $U$ in $(24)$ is empty, the result is immediate. Otherwise, we choose $a\in U$ and replace the empty sets $A_i$ with $\{a\},$ without changing $U.$ By $(15),$ each $A_i$ admits a surjective map $f_i\colon\mathbb{N}\to A_i,$ so we define:

$$
\begin{align}
&F\colon\mathbb{N}\times\mathbb{N}\to U \\[6pt]
&F(i,j)=f_i(j)
\end{align} \tag{25}
$$

In $(25),$ the index $i$ identifies the set, while $j$ identifies an element in its list. Every $x\in U$ belongs to some $A_i$ and is therefore equal to $f_i(j)$ for some $j,$ so $F$ is surjective. Composing $F$ with the inverse of $(21)$ gives a surjection from $\mathbb{N}$ to $U,$ proving that the union is countable by criterion $(15).$

- - -

The results on products and the surjectivity criterion also allow us to prove that the [rational numbers](../rational-numbers/) are countable by representing each fraction through its numerator and denominator. Specifically, consider:

$$
\begin{align}
&q\colon\mathbb{Z}\times(\mathbb{N}\setminus\{0\})\to\mathbb{Q} \\[6pt]
&q(p,n)=\frac{p}{n}
\end{align} \tag{26}
$$

The domain in $(26)$ is countably infinite by the results on products, and $q$ is surjective because every rational number is the quotient of an integer by a positive integer. Criterion $(15)$ therefore ensures that $\mathbb{Q}$ is countable, and the inclusion $\mathbb{Z}\subseteq\mathbb{Q}$ rules out finiteness. Different pairs representing the same fraction, such as $(1,2)$ and $(2,4),$ cause no problem because the criterion allows repetitions.

## The uncountability of the real numbers

Using $(26),$ we proved that the rational numbers can be listed using the natural numbers. We now show why this is impossible for the [real numbers](../real-numbers/) by proving that the interval $(0,1]$ admits no enumeration. The procedure is to assume that a complete list exists and construct a number in the interval that does not appear in it. We therefore choose a unique decimal expansion for each number because, although it may seem counterintuitive, some numbers admit two, as the following [geometric series](../geometric-series/) shows:

$$
0.999\ldots=\sum_{n=1}^{\infty}\frac{9}{10^n}=\frac{9/10}{1-1/10}=1 \tag{27}
$$

When there are two representations, we choose the one that continues with $9$s, and under this convention every $x\in(0,1]$ has a unique expansion of the form:

$$
\begin{align}
&x=0.a_1a_2a_3\ldots \\[6pt]
&a_n\in\{0,1,\ldots,9\}
\end{align} \tag{28}
$$

In $(28),$ the digits are not all zero from some position onwards, and even the endpoint $1$ has the required representation by $(27).$ Suppose now, for a contradiction, that $(0,1]$ is countable, so that writing each term in the form $(28)$ would give:

$$
\begin{align}
&x_1=0.a_{11}a_{12}a_{13}a_{14}\ldots \\[6pt]
&x_2=0.a_{21}a_{22}a_{23}a_{24}\ldots \\[6pt]
&x_3=0.a_{31}a_{32}a_{33}a_{34}\ldots \\[6pt]
&x_4=0.a_{41}a_{42}a_{43}a_{44}\ldots \\[6pt]
&\cdots
\end{align} \tag{29}
$$

In $(29),$ the first index of $a_{nk}$ identifies the number $x_n,$ and the second identifies the position of the digit. We therefore consider the diagonal digits $a_{11},a_{22},a_{33},\ldots$ and modify each of them according to the following rule:

$$
d_n=
\begin{cases}
6 & \text{if } a_{nn}=5 \\[6pt]
5 & \text{if } a_{nn}\neq5
\end{cases} \tag{30}
$$

We now use the digits in $(30)$ to construct the number:

$$
y=0.d_1d_2d_3\ldots \tag{31}
$$

Every digit of $y$ is $5$ or $6,$ so $y\in(0,1]$ and the expansion $(31)$ follows the chosen convention, without ending in zeros. For every $n,$ rule $(30)$ gives $d_n\neq a_{nn},$ so $y$ differs from $x_n$ in its digit at position $n.$ Since we are comparing the unique expansions fixed by the convention, it follows that $y\neq x_n$ for every $n\geq1.$ The number $y$ therefore belongs to the interval but does not appear in the list $(29),$ contradicting the assumption that the list contains all its elements, so the interval $(0,1]$ is uncountable, and $\mathbb{R}$ must also be uncountable because every subset of a countable set is countable.

## Further applications

We apply the countability results for products and unions to [algebraic numbers](../types-of-numbers/) and [finite sequences](../sequences/). We know that a real number is algebraic if it is a [root](../roots-of-a-polynomial/) of a nonzero [polynomial](../polynomials/) with integer coefficients, and transcendental otherwise. If we fix $n,H\in\mathbb{N},$ there are only finitely many such polynomials of degree at most $n$ whose coefficients have absolute value at most $H,$ and together they have a finite set of real roots $E_{n,H}.$ Every algebraic number belongs to one of these sets, so:

$$
\mathcal{A}=\bigcup_{(n,H)\in\mathbb{N}\times\mathbb{N}}E_{n,H} \tag{32}
$$

Since $\mathbb{N}\times\mathbb{N}$ is countable by $(21),$ the union in $(32)$ is a countable union of finite sets, so $\mathcal{A}$ is countable. The [transcendental numbers](../types-of-numbers/) are uncountable, since otherwise $\mathbb{R},$ the union of the algebraic and transcendental numbers, would also be countable.

We now show that the set of finite sequences of natural numbers is countable as well. The sequences of length $k$ form $\mathbb{N}^k,$ while $\mathbb{N}^0$ contains only the empty sequence, so the set containing all of them is given by the union:

$$
\mathcal{S}=\bigcup_{k\in\mathbb{N}}\mathbb{N}^k \tag{33}
$$

By $(23),$ each set in $(33)$ is countable, so their union $\mathcal{S}$ is countable as well. Associating each finite subset of $\mathbb{N}$ with the increasing sequence of its elements gives an injection into $\mathcal{S},$ so the collection of finite subsets is countable too.
