---
title: Cyclic Groups
source: https://algebrica.org/cyclic-groups/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - cyclic-group
  - element-order
  - generator
  - group-theory
  - subgroup
---

## Definition

A [group](../groups/) $G$ is cyclic if it contains an element $g$ such that every element of $G$ can be written as an integer power of $g.$ For example, in the group $\{1,-1\}$ under multiplication, the powers of $g=-1$ give both elements, since $(-1)^1=-1$ and $(-1)^2=1.$ An element with this property is called a generator of $G.$ If $\langle g\rangle$ denotes the set of all integer powers of $g,$ then saying that $g$ generates $G$ is equivalent to requiring the following equality:

$$
\begin{align}
G = \langle g\rangle &= \{g^k \mid k \in \mathbb{Z}\} \tag{1}
\end{align}
$$

In $(1),$ the exponent zero gives the identity element $e,$ while negative exponents give powers of the inverse of $g.$ When the group operation is written as addition, we speak of integer multiples of $g,$ and $(1)$ becomes:

$$
\begin{align}
G = \langle g\rangle &= \{kg \mid k \in \mathbb{Z}\} \tag{1a}
\end{align}
$$

To apply $(1a),$ let us return to the element $-1$ from the first example and see what it generates in the additive group of [integers](../integers/). Adding one or more copies of $-1$ gives every negative integer. Their additive inverses give every positive integer, and the multiple with coefficient zero is $0.$ The integer multiples of $-1$ therefore make up all of $\mathbb{Z}.$ The element $1$ also generates this group, since every integer $k$ equals $k\cdot 1.$

To see how the same definition applies to a finite group, consider the [rotations about the center of a square](../dihedral-groups/) that carry the square onto itself. For example, after a quarter turn counterclockwise, each vertex occupies the former position of the next vertex. If we denote this rotation by $r,$ the four rotations are:

$$e,r,r^2,r^3$$

Composing $r^3$ with $r$ completes a full turn, so $r^4=e$ and the subsequent powers cycle through the same four rotations. The group is therefore cyclic. The element $r^{-1}$ also generates it, cycling through the rotations in the opposite direction, whereas $r^2$ generates only the subgroup $\{e,r^2\}.$

The fact that every element is a power of the same base allows us to prove that every cyclic group is abelian. Indeed, for any two elements $x,y\in G,$ equation $(1)$ lets us write $x=g^a$ and $y=g^b$ with $a,b\in\mathbb{Z}.$ The product rule for powers with the same base reduces the comparison of $xy$ and $yx$ to addition of integers, so we can write:

$$
\begin{align}
xy &= g^a g^b = g^{a+b} \notag \\[6pt]
   &= g^{b+a} = g^b g^a = yx \tag{2}
\end{align}
$$

Since $x$ and $y$ were arbitrary, $(2)$ proves that the operation in $G$ is commutative. To test the converse, consider the following pairs under addition modulo $2$ in each coordinate:

$$(0,0),(1,0),(0,1),(1,1)$$

Addition is commutative, and adding any pair to itself gives $(0,0).$ The multiples of a pair therefore take at most two values. This group is abelian, but no element generates all four pairs.

## Order of a generator and classification

In the square example, the fourth power of $r$ is the first positive power that gives the identity. Let us see how the first return to the identity determines the structure of a cyclic group. We first prove that every infinite cyclic group is [isomorphic](../homomorphisms-and-isomorphisms/) to the additive group of integers and that every finite cyclic group of order $n$ is isomorphic to the additive group of residue classes modulo $n.$ Fix a generator $g$ and define the map $\psi\colon\mathbb{Z}\to G$ by $\psi(k)=g^k.$ For any two integers $a,b,$ the product rule for powers with the same base gives:

$$
\begin{align}
\psi(a+b) &= g^{a+b} = \psi(a)\psi(b) \tag{3}
\end{align}
$$

By $(3)$ the map is a homomorphism, and by $(1)$ it is [surjective](../injective-surjective-and-bijective-functions/). To determine when it is also injective, observe that two powers $g^a$ and $g^b$ coincide when $g^{a-b}=e.$ If no positive power of $g$ equals $e,$ this can happen only when $a=b.$ Indeed, if the two exponents were distinct, subtracting the smaller from the larger would give a positive exponent for which the power equals $e.$ In this case, $g$ is said to have infinite order. The map $\psi$ is therefore bijective and gives an isomorphism between $(\mathbb{Z},+)$ and $G.$

Suppose instead that some positive power equals $e,$ and let $n$ be the least positive exponent for which this holds. This integer is the order of $g,$ written $n=\mathrm{ord}(g).$ To see which exponents give the same power, we divide an arbitrary integer $k$ by $n$ and write $k=qn+r,$ where $0\leq r\lt n.$ Since $g^n=e,$ only the [remainder](../euclidean-division/) matters when computing $g^k.$

$$
\begin{align}
g^k &= (g^n)^q g^r = g^r \tag{4}
\end{align}
$$

By $(4),$ every power equals one of $e,g,\ldots,g^{n-1}.$ These $n$ powers are distinct, since if two were equal, the positive difference between their exponents would be smaller than $n$ and would give another power equal to $e.$ Thus $G$ has exactly $n$ elements. Two exponents give the same power if and only if they have the same remainder modulo $n,$ as expressed by the following equivalence:

$$
\begin{align}
g^a=g^b &\iff a\equiv b \pmod n \tag{5}
\end{align}
$$

By $(5),$ we can assign the power $g^k$ to the residue class $[k]$ regardless of the representative chosen. Distinct classes give distinct powers, and since $g$ generates $G,$ we obtain them all this way. The correspondence is therefore bijective and preserves the operation by $(3).$ We have now constructed the required isomorphism in the finite case as well, from $(\mathbb{Z}/n\mathbb{Z},+)$ to $G,$ which completes the proof of the classification.

## Order of a power and choice of generators

Let us return to the distinction we saw in the square example. If $g$ generates a finite group of order $n,$ how can we tell which powers $g^k$ also generate the whole group? Since the order of an element equals the number of elements in the subgroup it generates, it suffices to find the order of $g^k$ and check whether it equals $n.$ We will prove that this order is obtained by dividing $n$ by the [greatest common divisor](../greatest-common-divisor/) of $n$ and $k:$

$$
\begin{align}
\mathrm{ord}(g^k) &= \frac{n}{\gcd(n,k)} \tag{6}
\end{align}
$$

We begin by looking for the least positive integer $t$ such that $(g^k)^t=e.$ Since $(g^k)^t=g^{kt},$ equation $(5)$ tells us that $t$ must satisfy $n\mid kt.$ To find the least such $t,$ put $d=\gcd(n,k)$ and write $n=dn'$ and $k=dk'.$ Dividing by $d$ reduces the condition to $n'\mid k't,$ and since $n'$ and $k'$ are coprime, [Euclid's lemma](../fundamental-theorem-of-arithmetic/) gives $n'\mid t.$ Conversely, every multiple of $n'$ satisfies the condition, so the least positive $t$ is $n'=n/d.$ This proves $(6).$

It follows that $g^k$ generates $G$ if and only if $\gcd(n,k)=1.$ There are therefore as many generators as there are residue classes modulo $n$ coprime to $n,$ and their number is denoted by $\varphi(n),$ where $\varphi$ is Euler's totient function. For example, in the additive group $\mathbb{Z}/12\mathbb{Z},$ the classes that generate the whole group are $[1],[5],[7]$ and $[11].$ The class $[8],$ on the other hand, has order $12/\gcd(12,8)=3.$ Indeed, starting at $[0]$ and repeatedly adding $[8]$ takes us from $[0]$ to $[8],$ then to $[4]$ and finally back to $[0].$

In the infinite case, the exponents tell us directly which elements are generators. Indeed, the powers of $g^k,$ when written as powers of $g,$ have as their exponents precisely the multiples of $k.$ To obtain $g$ itself, we therefore need $kt=1$ for some integer $t,$ since distinct exponents give distinct powers. This happens only for $k=1$ or $k=-1,$ and in both cases we obtain every integer exponent. The generators of an infinite cyclic group are therefore precisely $g$ and $g^{-1}.$

## Subgroups of a cyclic group

In the example modulo $12,$ we found a subgroup of order $3$ by taking the multiples of $[8].$ Let us see why every subgroup $H$ of a cyclic group $G=\langle g\rangle$ is itself cyclic. To prove this, we look for the least positive integer $m$ such that $g^m\in H.$ If no positive exponent has this property, then no power with a negative exponent can belong to $H$ either, since its inverse would have a positive exponent and would also belong to $H.$ In this case $H=\{e\}=\langle e\rangle,$ so $H$ is cyclic.

Now suppose that such a least exponent $m$ exists, and take any element $g^k\in H.$ We want to show that it is a power of $g^m.$ Divide $k$ by $m$ and write $k=qm+r,$ where $0\leq r\lt m.$ Since $g^m$ belongs to $H,$ so does its power with exponent $-q.$ We can therefore express $g^r$ as a product of two elements of $H,$ obtaining

$$
\begin{align}
g^k(g^m)^{-q} &= g^{k-qm} = g^r \in H \tag{7}
\end{align}
$$

If $r$ were positive, $(7)$ would contradict the choice of $m,$ so $r=0$ and $k$ is a multiple of $m.$ This proves that every element of $H$ is a power of $g^m.$ Conversely, since $g^m$ belongs to $H,$ all its powers belong to $H,$ so $H=\langle g^m\rangle,$ which completes the proof.

If $H$ is a subgroup of $\mathbb{Z}$ other than $\{0\},$ its least positive element $m$ generates $H.$ Its elements are therefore precisely the multiples of $m.$ This gives the subgroups $m\mathbb{Z}$ for $m\geq 1,$ together with the trivial subgroup $0\mathbb{Z}=\{0\}.$

When $G$ has finite order $n,$ we can make the result more precise by proving that for every positive divisor $d$ of $n$ there is a unique subgroup of order $d.$ Indeed, $g^n=e$ belongs to every subgroup $H,$ so the least exponent $m$ considered above exists even for $H=\{e\}.$ We have just seen that every exponent $k$ for which $g^k\in H$ is a multiple of $m.$ Applying this conclusion to $k=n$ gives $m\mid n.$ By $(6),$ the order of $H=\langle g^m\rangle$ is then $n/m.$

For $H$ to have order $d,$ we must therefore have $m=n/d.$ To check that this choice does give a subgroup of the required order, we apply $(6)$ to $g^{n/d}$ and use the fact that $n/d$ divides $n,$ obtaining:

$$
\begin{align}
\bigl|\langle g^{n/d}\rangle\bigr| &= \frac{n}{\gcd(n,n/d)} = d \tag{8}
\end{align}
$$

Equation $(8)$ proves that the subgroup exists, and the fact that $m$ is uniquely determined proves its uniqueness. For example, in $\mathbb{Z}/12\mathbb{Z},$ the unique subgroup of order $3$ is generated by $[12/3]=[4]$ and consists of the classes $[0],[4],[8],$ so we recover the subgroup generated by $[8]$ in the preceding section.
