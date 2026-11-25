---
title: Groups
source: https://algebrica.org/groups/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - associativity
  - cayley-table
  - cyclic-subgroup
  - element-order
  - group-theory
  - identity-element
  - inverse-element
  - subgroup
  - symmetric-group
---

## Definition

We begin with groups in our study of algebraic structures, which are [sets](../sets/) equipped with one or more operations satisfying specified properties. Groups, [rings](../rings/), and [fields](../fields/) are examples of algebraic structures. Briefly, a group has an associative operation with an identity and inverses, a ring is an abelian group under addition with an associative multiplication that distributes over addition, and a field is a ring whose nonzero elements form an abelian group under multiplication. For example, the [integers](../integers/) form a group under addition and a ring when we also consider multiplication.

A group is a set $G$ equipped with a binary operation that satisfies three axioms and is written as:

$$\cdot : G \times G \to G \tag{1}$$

In $(1)$ the dot $\cdot$ denotes the group operation, which assigns to each [ordered pair](../cartesian-product/) $(a,b) \in G \times G$ an element of $G,$ written $a \cdot b.$ For example, in the additive group of integers, $a \cdot b$ denotes the sum $a+b.$ We now consider the three axioms that the operation in $(1)$ must satisfy, starting with associativity. For all $a, b, c \in G,$ the following identity must hold:

$$(a \cdot b) \cdot c = a \cdot (b \cdot c) \tag{2}$$

The second axiom requires an identity element $e \in G$ such that multiplying any $a \in G$ by $e$ gives $a$:

$$a \cdot e = e \cdot a = a \tag{3}$$

The third axiom requires every element $a \in G$ to have an inverse $a^{-1} \in G$ satisfying the identity:

$$a \cdot a^{-1} = a^{-1} \cdot a = e \tag{4}$$

Some texts list closure as a separate axiom, but there is no need to state it separately because the choice of $G$ as the [codomain](../functions/) in $(1)$ already ensures that the product of two elements of $G$ belongs to $G.$

A group $(G, \cdot)$ is called abelian, or commutative, if reversing the order of the factors leaves the product unchanged. The following identity must therefore hold for all $a, b \in G$:

$$a \cdot b = b \cdot a \tag{5}$$

In the [symmetric group](../symmetric-group/) $S_3$ of permutations of $\{1,2,3\},$ first interchanging $1$ and $2$ and then interchanging $2$ and $3$ sends $1$ to $3.$ Performing the same interchanges in reverse order sends $1$ to $2.$ The two [compositions](../composite-functions/) are different, so $S_3$ is nonabelian.

- - -

Consider what happens when one of the axioms fails. Take, for example, the [real numbers](../real-numbers/) under multiplication, which is associative and has identity element $1.$ Zero is the only element without an inverse, since the following holds for every $x \in \mathbb{R}$:

$$0 \cdot x = 0 \neq 1 \tag{6}$$

Thus $(\mathbb{R}, \cdot)$ fails to satisfy axiom $(4).$ Once zero is excluded, each element $a$ has inverse $1/a,$ giving the abelian group $(\mathbb{R} \setminus \{0\}, \cdot).$

## Properties

Consider the identity element whose existence is guaranteed by $(3).$ To prove uniqueness, suppose that $e$ and $e'$ are both identity elements and consider their product:

$$e = e \cdot e' = e' \tag{7}$$

The first equality in $(7)$ holds because $e'$ is a right identity, and the second because $e$ is a left identity, so $e$ and $e'$ must coincide. The inverse is also unique, as we can see by fixing an element $a \in G$ and taking $h$ to be a left inverse of $a,$ so that $h \cdot a = e.$ Now let $k$ be a right inverse, so that $a \cdot k = e.$ Replacing $e$ by $a \cdot k$ in the product $h \cdot e$ and applying associativity $(2)$ gives the following equality:

$$
\begin{align}
h &= h \cdot e \notag \\[6pt]
  &= h \cdot (a \cdot k) \notag \\[6pt]
  &= (h \cdot a) \cdot k \notag \\[6pt]
  &= e \cdot k \notag \\[6pt]
  &= k \tag{8}
\end{align}
$$

Equation $(8)$ shows that every left inverse coincides with every right inverse, and since $a^{-1}$ satisfies both conditions by $(4),$ even a one-sided inverse of $a$ must coincide with $a^{-1}.$

Now fix an element $a \in G.$ If we know the product $a \cdot x,$ how can we recover $x$? What if the product is $x \cdot a$ instead? As $x$ ranges over $G,$ these two products define maps from $G$ to itself, left multiplication by $a$ and right multiplication by $a,$ which we write as:

$$
\begin{align}
L_a(x) &= a \cdot x \notag \\[6pt]
R_a(x) &= x \cdot a \tag{9}
\end{align}
$$

In the first case of $(9),$ we recover $x$ by multiplying $a \cdot x$ on the left by $a^{-1},$ which amounts to applying $L_a$ and then $L_{a^{-1}}.$ By associativity we can group the first two factors and write the calculation as follows:

$$
\begin{align}
L_{a^{-1}}(L_a(x)) &= a^{-1} \cdot (a \cdot x) \notag \\[6pt]
                   &= (a^{-1} \cdot a) \cdot x \notag \\[6pt]
                   &= e \cdot x \notag \\[6pt]
                   &= x \tag{10}
\end{align}
$$

Equation $(10)$ shows that multiplying on the left by $a^{-1}$ recovers $x$ from the product $a \cdot x.$ Applying the maps in the opposite order also gives $x,$ since $a \cdot a^{-1} = e.$ The same argument works for right multiplication. Both maps in $(9)$ are therefore [bijective](../injective-surjective-and-bijective-functions/), and their inverses are:

$$
\begin{align}
L_a^{-1} &= L_{a^{-1}} \notag \\[6pt]
R_a^{-1} &= R_{a^{-1}} \tag{11}
\end{align}
$$

Since $L_a$ and $R_a$ are injective, a common factor can be cancelled when it occurs on the same side of both products in an equation. Thus for all $a, b, c \in G$ the left and right cancellation laws hold:

$$
\begin{align}
a \cdot b = a \cdot c &\implies b = c \notag \\[6pt]
b \cdot a = c \cdot a &\implies b = c \tag{12}
\end{align}
$$

The [inverse maps](../inverse-function/) in $(11)$ also let us solve equations in the group, since for every $a, b \in G,$ multiplying both sides by $a^{-1}$ on the side where $a$ occurs gives a unique solution:

$$
\begin{align}
a \cdot x = b &\iff x = a^{-1} \cdot b \notag \\[6pt]
x \cdot a = b &\iff x = b \cdot a^{-1} \tag{13}
\end{align}
$$

The order of a group $G$ is its [cardinality](../cardinality-and-countable-sets/), denoted by $|G|.$ A group is finite if it has finitely many elements and infinite otherwise.

When $G$ is finite, the uniqueness of the solutions in $(13)$ can be read from the group's Cayley table. To construct the table, use the elements of $G$ as both row and column headings. The entry in row $a$ and column $x$ is the product $a \cdot x.$ Thus row $a$ lists the values of $L_a,$ while column $a$ lists those of $R_a.$ For example, the operation in $\mathbb{Z}/3\mathbb{Z}$ is addition modulo $3.$ Denoting the three [residue classes](../modulo-operator/) by $0, 1, 2$ and entering in each cell the remainder when the sum of its row and column headings is divided by $3,$ we obtain the following table:

$$
\begin{array}{c|ccc}
+ & 0 & 1 & 2 \\ \hline
0 & 0 & 1 & 2 \\
1 & 1 & 2 & 0 \\
2 & 2 & 0 & 1
\end{array}
\tag{14}
$$

In $(14),$ row $2$ contains $0$ in column $1,$ since $2+1 \equiv 0 \pmod{3}.$ From the same row we see that $x=1$ is the unique solution of $2+x=0$ in the group.

Finding an element $b$ in row $a$ amounts to solving the equation $a \cdot x = b,$ where $x$ is the column we seek. Finding the same element in column $a$ amounts to solving $x \cdot a = b,$ where $x$ now indicates the row. By $(13)$ each equation has a unique solution, so each element of $G$ occurs exactly once in each row and in each column.

- - -

We can also use the Cayley table to find the inverse of an element $g$ by looking for $e$ in row $g,$ since the heading of the column where it occurs is the unique element $x$ such that $g \cdot x = e,$ and hence is $g^{-1}.$ When $g = a \cdot b,$ we can solve the same equation in any group by using associativity to group $b$ and $x$ and then multiplying both sides on the left first by $a^{-1}$ and then by $b^{-1}$:

$$
\begin{align}
(a \cdot b) \cdot x &= e \notag \\[6pt]
a \cdot (b \cdot x) &= e \notag \\[6pt]
b \cdot x &= a^{-1} \notag \\[6pt]
x &= b^{-1} \cdot a^{-1} \tag{15}
\end{align}
$$

By $(15)$ and the uniqueness of the inverse proved in $(8),$ we obtain the formula for the inverse of a product:

$$(a \cdot b)^{-1} = b^{-1} \cdot a^{-1} \tag{16}$$

It also follows from $(4)$ that $a$ is the inverse of $a^{-1},$ since their product in either order is $e,$ and hence $(a^{-1})^{-1} = a.$

## Powers of an element

When all the factors in a product are equal to the same element $a \in G,$ the associative law $(2)$ lets us group them without changing the result. More formally, for each integer $n \geq 1$ we write $a^n$ for the product of $n$ copies of $a$:

$$a^n = \underbrace{a \cdot a \cdots a}_{n \text{ factors}} \tag{17}$$

The following properties also hold:

$$
\begin{align}
a^0 &= e \notag \\[6pt]
a^{-n} &= (a^{-1})^n \qquad (n \geq 1) \tag{18}
\end{align}
$$

For positive $m$ and $n,$ the product of $a^m$ and $a^n$ contains $m+n$ factors equal to $a,$ while $(a^m)^n$ contains $n$ groups of $m$ factors each. With the definitions in $(18),$ both laws hold for all integers $m$ and $n$:

$$
\begin{align}
a^m \cdot a^n &= a^{m+n} \notag \\[6pt]
(a^m)^n &= a^{mn} \tag{19}
\end{align}
$$

The two identities in $(19)$ give the rules for multiplying powers with the same base and raising a power to a power, both familiar from the discussion of real numbers in the entry on [powers](../powers/), and both valid for integer exponents even in nonabelian groups.

When the group operation is written as addition, we write $na$ in place of $a^n.$ For positive $n,$ $na$ is the sum of $n$ copies of $a.$ When raising a product to a power, the order of the factors also matters. If $a$ and $b$ commute, we can interchange the two middle factors in $(a \cdot b)^2 = a \cdot b \cdot a \cdot b$ to obtain $a^2 \cdot b^2.$ The same rearrangement works for every positive exponent and, on taking inverses, for negative exponents as well. Thus, if $a \cdot b = b \cdot a,$ the following identity holds for every integer $n$:

$$(a \cdot b)^n = a^n \cdot b^n \tag{20}$$

## Order of an element

We have seen from $(18)$ that $a^0=e$ for every element $a \in G.$ If we start at $e$ and repeatedly multiply by $a,$ how many steps does it take to return to $e$? When such a return occurs, the number of steps up to the first return to $e$ is called the order of $a,$ denoted by $\mathrm{ord}(a)$ and given by:

$$\mathrm{ord}(a) = \min\{n \in \mathbb{Z} : n \gt 0,\ a^n = e\} \tag{21}$$

If no positive power equals $e,$ we say that $a$ has infinite order and write $\mathrm{ord}(a)=\infty.$ In an additive group, finding the first return to the identity amounts to finding the smallest positive integer $n$ for which $na=0.$ Returning to the example of $(\mathbb{Z}/6\mathbb{Z},+),$ we start at $0$ and repeatedly add $2,$ reducing each sum modulo $6,$ to obtain:

$$0 \xrightarrow{+2} 2 \xrightarrow{+2} 4 \xrightarrow{+2} 0 \tag{22}$$

In $(22)$ we return to zero on the third addition, so $2$ has order $3.$ If we add $1$ each time, it takes six additions to return to zero, so $1$ has order $6.$ In $(\mathbb{Z},+)$ every nonzero integer has infinite order, since no positive integer multiple of a nonzero integer is zero. The order of $a$ also determines how many distinct powers of $a$ there are. To prove this, suppose that $\mathrm{ord}(a)=n.$ The first $n$ powers, from $a^0$ to $a^{n-1},$ are all distinct, since if $a^i=a^j$ for two exponents $0 \leq i \lt j \lt n,$ multiplying by $a^{-i}$ would give $a^{j-i}=e.$ Since $0 \lt j-i \lt n,$ this would contradict the choice of $n$ in $(21).$

To conclude that there are exactly $n$ distinct powers, it remains to show that every power $a^k$ equals one of those already listed. Since $a^n=e,$ increasing the exponent by $n$ leaves the power unchanged. Dividing $k$ by $n$ lets us reduce the exponent to an integer between $0$ and $n-1.$ Writing $k=qn+r$ with $0 \leq r \lt n$ and applying $(19)$ gives:

$$a^k = (a^n)^q \cdot a^r = e^q \cdot a^r = a^r \tag{23}$$

Equation $(23)$ shows that the [remainder](../euclidean-division/) $r$ determines the power. Since different remainders give different powers, $a^k=a^\ell$ if and only if $k \equiv \ell \pmod{n}.$ By $(18)$ and $(19),$ multiplying two integer powers of $a$ or taking the inverse of either one gives another power of $a.$ These powers therefore form a group under the same operation as $G.$ This is called the cyclic subgroup generated by $a$ and is denoted by $\langle a \rangle.$ In the finite case we therefore have:

$$
\begin{align}
\langle a \rangle &= \{a^r : 0 \leq r \lt n,\ r \in \mathbb{Z}\} \notag \\[6pt]
|\langle a \rangle| &= n = \mathrm{ord}(a) \tag{24}
\end{align}
$$

If $a$ has infinite order, two distinct exponents $i \lt j$ cannot give the same power, since that would again give $a^{j-i}=e$ with $j-i$ positive, so in this case $\langle a \rangle$ is infinite as well.
