---
title: Chinese Remainder Theorem
source: https://algebrica.org/chinese-remainder-theorem/
license: CC BY-NC 4.0
tags:
  - bezout-identity
  - chinese-remainder-theorem
  - congruence
  - coprime-integers
  - greatest-common-divisor
  - least-common-multiple
  - modular-arithmetic
  - multiplicative-inverse
  - residue-class
  - ring-isomorphism
  - systems-of-congruences
---

## From remainders to systems of congruences

The Chinese remainder theorem guarantees that an [integer](../integers/) can be recovered from the remainders of its divisions by several positive integers, called moduli. When these moduli are pairwise coprime, meaning that every pair of distinct moduli has greatest common divisor $1,$ the theorem guarantees that any choice of remainders is attained by an integer and that all integers with those remainders differ by a multiple of the product of the moduli. Before stating the theorem, it is useful to introduce the concept of [congruence](../modulo-operator/). Two integers $a$ and $b$ are congruent modulo $n$ if they have the same remainder upon division by $n.$ We write:

$$a\equiv b\pmod n \tag{1}$$

For example, $8\equiv5\pmod3,$ because $8=2\cdot3+2$ and $5=1\cdot3+2,$ so both have remainder $2$ upon division by $3.$ To prescribe the remainders of the same integer for several moduli, we therefore write a congruence of the form $(1)$ for each modulus. We can then combine these conditions into a system of congruences, because we seek an integer that satisfies all of them. For example, prescribing remainder $2$ upon division by $3$ and remainder $3$ upon division by $5$ gives the system:

$$ \tag{2}
\begin{cases}
x \equiv 2 \pmod 3 \\[6pt]
x \equiv 3 \pmod 5
\end{cases}
$$

The number $8$ satisfies both congruences, because $8=2\cdot3+2$ and $8=1\cdot5+3,$ and the same holds more generally for every integer of the form $8+15q,$ with $q\in\mathbb{Z}.$ Since $3$ and $5$ are coprime, as noted above, the Chinese remainder theorem guarantees that the integers $8+15q$ are all and only the solutions of the system. We will work through the solution in detail below. For now, an intuitive understanding of the procedure is sufficient. We now state the problem formally by taking two integers $m$ and $n$ greater than $1,$ with $\gcd(m,n)=1.$ Given arbitrary integers $a$ and $b,$ we consider the following system, which generalizes $(2)$:

$$ \tag{3}
\begin{cases}
x \equiv a \pmod m \\[6pt]
x \equiv b \pmod n
\end{cases}
$$

Under these assumptions, the Chinese remainder theorem states that system $(3)$ has exactly one solution $x_0$ among the integers from $0$ to $mn-1.$ All and only the solutions of the system are obtained by adding an integer multiple of $mn$ to $x_0,$ according to the formula:

$$
x=x_0+qmn \qquad q\in\mathbb{Z} \tag{4}
$$

There are infinitely many integer solutions, but they all have the same remainder $x_0$ upon division by $mn.$ The solution is therefore said to be unique modulo $mn.$

- - -

The proof of the theorem has two parts. We first show that system $(3)$ has at least one solution, and then that all solutions have the same remainder upon division by $mn.$ For the first part, we construct a solution using [Bézout's identity](../integers/), which states that for any two positive integers $m$ and $n,$ there are integers $s$ and $t$ satisfying the following relation:

$$
sm+tn=\gcd(m,n) \tag{5}
$$

By assumption, $m$ and $n$ are coprime, so $\gcd(m,n)=1,$ and we can rewrite $(5)$ as:

$$ \tag{6}
sm+tn=1
$$

From this identity, we seek two numbers that allow us to satisfy the conditions in $(3)$ separately. We first set $e_1=tn$ and $e_2=sm.$ Since $tn=1-sm$ is congruent to $1$ modulo $m$ and $sm=1-tn$ is congruent to $1$ modulo $n,$ the following relations hold:

$$ \tag{7}
\begin{align}
e_1 &\equiv 1 \pmod m & e_1 &\equiv 0 \pmod n \\[6pt]
e_2 &\equiv 0 \pmod m & e_2 &\equiv 1 \pmod n
\end{align}
$$

Consider the sum $ae_1+be_2.$ By the relations in $(7),$ this sum is congruent to $a\cdot1+b\cdot0=a$ modulo $m$ and to $a\cdot0+b\cdot1=b$ modulo $n.$ It therefore satisfies both conditions in $(3),$ so a solution of the system is given by:

$$ \tag{8}
x_0=ae_1+be_2=atn+bsm
$$

This proves the existence of a solution for any pair of integers $a$ and $b.$ We now prove the second part, uniqueness modulo $mn,$ by supposing that $x_0$ and $x_1$ are two solutions of the system. Their difference is divisible by both $m$ and $n,$ because the two solutions must have the same remainders for both moduli. We therefore write $x_1-x_0=mq.$ Since $n$ divides $mq$ and is coprime to $m,$ it must also divide $q,$ so $q=nh$ for some integer $h.$ It follows that:

$$
x_1-x_0=mnh \tag{9}
$$

The two solutions $x_0$ and $x_1$ are therefore congruent modulo $mn.$ We have thus proved the theorem for two coprime moduli and described all and only the solutions of system $(3).$

- - -

For a concrete example, we return to the system introduced at the beginning and solve $(2)$ using formula $(8),$ with $m=3,$ $n=5,$ $a=2$ and $b=3.$ To find the coefficients $s$ and $t,$ we write Bézout's identity in the form $(6)$:

$$
2\cdot3-1\cdot5=1
$$

Comparing this equality with the general identity $sm+tn=1,$ we obtain $m=3,$ $s=2,$ $n=5$ and $t=-1.$ From the definitions $e_1=tn$ and $e_2=sm,$ we then obtain $e_1=(-1)\cdot5=-5$ and $e_2=2\cdot3=6.$ Substituting these values into $(8)$ gives:

$$
x_0=2\cdot(-5)+3\cdot6=-10+18=8
$$

Since the moduli are coprime, all solutions are obtained by adding a multiple of $3\cdot5=15$ to $8.$ The solution set of the system is therefore the [residue class](../modulo-operator/) defined by:

$$ \tag{10}
[8]_{15}=\{\ 8+15q\mid q\in\mathbb{Z}\ \}
$$

This is a fairly simple example in which the small moduli allow us to find the Bézout coefficients directly. In general, however, the calculation is less immediate, and we use the [Euclidean algorithm](../euclidean-division/). The system $(2)$ can also be solved by substituting the expression for $x$ from the first congruence into the second, giving:

$$
\begin{align}
2+3q &\equiv 3 \pmod 5 \\[6pt]
3q &\equiv 1 \pmod 5
\end{align}
$$

The inverse of $3$ modulo $5$ is $2,$ because $3\cdot2=6\equiv1\pmod5.$ Multiplying by this inverse gives $q\equiv2\pmod5,$ so $q=2+5h$ with $h\in\mathbb{Z}.$ Returning to the original unknown, we obtain the same solution set as in $(10)$:

$$
x=2+3(2+5h)=8+15h
$$

## Extension of the theorem

The theorem also extends to a finite number of congruences. Let $n_1,n_2,\ldots,n_k$ be pairwise coprime integers greater than $1,$ with $k\geq2.$ Given arbitrary integers $a_1,a_2,\ldots,a_k,$ we form the following system:

$$ \tag{11}
\begin{cases}
x \equiv a_1 \pmod{n_1} \\[6pt]
x \equiv a_2 \pmod{n_2} \\[6pt]
\vdots \\[6pt]
x \equiv a_k \pmod{n_k}
\end{cases}
$$

Once a solution $x_0$ of $(11)$ has been found, all and only the solutions are obtained by adding to $x_0$ an integer multiple of the product $N=n_1n_2\cdots n_k.$ To construct a solution of $(11),$ we set:

$$
N_i=\frac{N}{n_i}
$$

The number $N_i$ is the product of all the moduli except $n_i.$ Since each of these factors is coprime to $n_i,$ their product is also coprime to $n_i,$ and hence $\gcd(N_i,n_i)=1.$ There is therefore an integer $u_i$ that is the [multiplicative inverse](../modulo-operator/) of $N_i$ modulo $n_i,$ satisfying:

$$
N_i u_i\equiv1\pmod{n_i}
$$

The product $N_i u_i$ is congruent to zero modulo every other modulus $n_j,$ because $n_j$ is a factor of $N_i$ when $j\neq i.$ These products therefore have the same role as $e_1$ and $e_2$ in the case of two congruences, so a solution of system $(11)$ is given by the following sum:

$$ \tag{12}
x_0=\sum_{i=1}^{k}a_iN_i u_i
$$

To verify this, fix an index $j$ and consider the sum modulo $n_j.$ All terms with $i\neq j$ are multiples of $n_j,$ so they are congruent to zero modulo $n_j$ and do not change the remainder of the sum upon division by $n_j.$ The sum is therefore congruent to the single term $a_jN_j u_j,$ which is congruent to $a_j$ because $N_j u_j\equiv1\pmod{n_j}.$ The number $x_0$ given by $(12)$ thus satisfies every congruence in the system.

To prove uniqueness modulo $N,$ we compare the solution $x_0$ just constructed with another solution $x_1.$ The two solutions have the same remainder modulo every $n_i,$ so each $n_i$ divides $x_1-x_0.$ Since the moduli are pairwise coprime, their product $N$ also divides this difference. It follows that $x_1\equiv x_0\pmod N,$ so every solution belongs to the same residue class as $x_0$ modulo $N,$ which proves uniqueness modulo $N.$

- - -

For a concrete example, we add a third condition to system $(2)$:

$$ \tag{13}
\begin{cases}
x \equiv 2 \pmod 3 \\[6pt]
x \equiv 3 \pmod 5 \\[6pt]
x \equiv 2 \pmod 7
\end{cases}
$$

Since the moduli $3,$ $5$ and $7$ are pairwise coprime, the system has a unique solution class modulo $N=3\cdot5\cdot7=105.$ The products of the moduli taken two at a time are:

$$
\begin{align}
N_1 &= 105/3=35 \\[6pt]
N_2 &= 105/5=21 \\[6pt]
N_3 &= 105/7=15
\end{align}
$$

To apply formula $(12),$ we need to find the inverse of $35$ modulo $3,$ of $21$ modulo $5$ and of $15$ modulo $7.$ Since $35\equiv2\pmod3$ and $2\cdot2\equiv1\pmod3,$ we can choose $u_1=2.$ The other two inverses are both $1,$ since $21\equiv1\pmod5$ and $15\equiv1\pmod7.$ Applying $(12)$ therefore gives:

$$
\begin{align}
x_0 &= 2\cdot35\cdot2+3\cdot21\cdot1+2\cdot15\cdot1 \\[6pt]
&=140+63+30=233
\end{align}
$$

From the solution $x_0=233,$ we obtain the smallest nonnegative solution by taking its remainder upon division by $105.$ Since $233=2\cdot105+23,$ we obtain $23,$ which belongs to the same residue class modulo $105.$ The number $23$ satisfies all three congruences in $(13),$ as the following equalities show:

$$
\begin{align}
23 &= 7\cdot3+2 \\[6pt]
23 &= 4\cdot5+3 \\[6pt]
23 &= 3\cdot7+2
\end{align}
$$

All solutions of the system are therefore the integers of the form:

$$23+105q \quad q\in\mathbb{Z} \tag{14}$$

The number $23$ is the smallest nonnegative solution. As in the case of two congruences, we can obtain the same result by substitution, starting with the first two congruences, whose solutions are all integers $x=8+15h,$ with $h\in\mathbb{Z}.$ We must therefore find the values of $h$ for which these integers also satisfy the third congruence, $x\equiv2\pmod7.$ Substituting $x=8+15h$ gives:

$$
8+15h\equiv2\pmod7
$$

Since $8=7+1$ and $15=2\cdot7+1,$ both are congruent to $1$ modulo $7.$ Consequently, $15h\equiv h\pmod7,$ and the congruence becomes $1+h\equiv2\pmod7.$ Subtracting $1$ from both sides gives $h\equiv1\pmod7.$ This last condition means that $h-1$ is a multiple of $7,$ so $h=1+7q$ for some integer $q.$ Substituting this expression into the formula $x=8+15h$ gives:

$$
\begin{align}
x &= 8+15(1+7q) \\[6pt]
&=8+15+105q \\[6pt]
&=23+105q
\end{align}
$$

We have thus recovered the solution given in $(14).$

## Non-coprime moduli

We return to system $(3)$ and consider the case in which the moduli $m$ and $n$ have a common divisor greater than $1.$ In this case, the two congruences may be incompatible. For example, $x\equiv1\pmod4$ requires $x$ to be odd, whereas $x\equiv2\pmod6$ requires it to be even, so no integer can satisfy both conditions. However, the lack of coprimality does not always rule out solutions of the system. Consider two moduli $m,n>1,$ and set $d=\gcd(m,n).$ System $(3)$ has solutions if and only if:

$$ \tag{15}
d\mid(b-a)
$$

Condition $(15)$ is equivalent to requiring $a\equiv b\pmod d.$ When it holds, the solution is unique modulo the least common multiple of the moduli, given by:

$$ \tag{16}
L=\mathrm{lcm}(m,n)=\frac{mn}{d}
$$

We now prove that condition $(15)$ is necessary and sufficient for system $(3)$ to have solutions. To prove necessity, suppose that $x$ satisfies both congruences in the system. Under this assumption, $m$ divides $x-a$ and $n$ divides $x-b.$ Since $d$ divides both moduli, it also divides the difference $(x-a)-(x-b)=b-a.$ To prove sufficiency, we rewrite the first congruence of system $(3),$ namely $x\equiv a\pmod m,$ as $x=a+mq,$ with $q\in\mathbb{Z}.$ Substituting this expression into the second congruence, $x\equiv b\pmod n,$ gives:

$$
mq\equiv b-a\pmod n
$$

If $d$ divides $b-a,$ we can divide by $d$ to obtain the equivalent congruence:

$$ \tag{17}
\frac{m}{d}q\equiv\frac{b-a}{d}\pmod{n/d}
$$

In congruence $(17),$ the coefficient $m/d$ and the modulus $n/d$ are coprime, because we have divided $m$ and $n$ by their greatest common divisor $d.$ If $n/d>1,$ we can therefore multiply both sides by the inverse of $m/d$ modulo $n/d,$ obtaining a unique solution class $q\equiv q_0\pmod{n/d}.$ Writing $q=q_0+(n/d)h,$ with $h\in\mathbb{Z},$ and substituting this expression into $x=a+mq,$ we obtain the general solution of system $(3)$:

$$
x=a+mq_0+\frac{mn}{d}h \qquad h\in\mathbb{Z} \tag{18}
$$

As $h$ ranges over $\mathbb{Z},$ formula $(18)$ describes all and only the solutions of the system, which form a single residue class modulo $L=mn/d.$ If instead $n/d=1,$ then $n$ divides $m,$ and condition $(15)$ ensures that the first congruence already implies the second. In this case, all integers $x=a+mq$ are solutions, and the period is again $L=m.$ For example, consider the system:

$$
\begin{cases}
x \equiv 2 \pmod 6 \\[6pt]
x \equiv 5 \pmod 9
\end{cases}
$$

The moduli have greatest common divisor $3,$ which divides the difference $5-2=3,$ so the system has solutions. From the first congruence, we obtain $x=2+6q.$ The second becomes $6q\equiv3\pmod9,$ and division by $3$ gives $2q\equiv1\pmod3.$ The inverse of $2$ modulo $3$ is $2,$ so $q\equiv2\pmod3.$ It follows that $q=2+3h,$ and hence the solution is:

$$
x=2+6(2+3h)=14+18h \qquad h\in\mathbb{Z}
$$

The system therefore has a unique solution class modulo $18.$

## Interpretation in terms of rings

The theorem can also be formulated in terms of [rings](../rings/), which requires some more advanced concepts from abstract algebra. Let $n_1,\ldots,n_k$ be pairwise coprime and set $N=n_1\cdots n_k.$ We define a map $\Phi,$ that is, a [function](../functions/) assigning to each class $[x]_N$ the tuple of classes of the same integer modulo $n_1,\ldots,n_k,$ as follows:

$$ \tag{19}
\begin{align}
&\Phi :\mathbb{Z}/N\mathbb{Z}\longrightarrow\mathbb{Z}/n_1\mathbb{Z}\times\cdots\times\mathbb{Z}/n_k\mathbb{Z} \\[6pt]
&\Phi([x]_N) =([x]_{n_1},\ldots,[x]_{n_k})
\end{align}
$$

This map is well-defined because, if we choose an arbitrary element $y$ of the same class modulo $N,$ the difference $x-y$ is divisible by $N$ and hence by each $n_i.$ The classes $[x]_{n_i}$ and $[y]_{n_i}$ coincide for every index, so the associated tuple does not depend on the chosen representative. Having established that $\Phi$ is well-defined, we now show that every tuple in the codomain is the image of a unique class modulo $N.$ For every tuple $([a_1]_{n_1},\ldots,[a_k]_{n_k}),$ the theorem guarantees the existence of an integer $x$ such that $x\equiv a_i\pmod{n_i}.$ The function defined in $(19)$ therefore maps $[x]_N$ to that tuple, so $\Phi$ is [surjective](../injective-surjective-and-bijective-functions/). If two classes have the same image, their elements have the same remainders for all moduli. By uniqueness modulo $N,$ these elements are congruent modulo $N,$ so the two classes coincide. This proves that $\Phi$ is also injective and hence bijective.

To show that the bijection $\Phi$ is also a ring isomorphism, we verify that addition and multiplication are preserved. Reduction modulo each $n_i$ preserves both operations, so the following identities hold for all $x,y\in\mathbb{Z}$:

$$
\begin{align}
\Phi([x]_N+[y]_N)&=\Phi([x]_N)+\Phi([y]_N) \\[6pt]
\Phi([x]_N[y]_N)&=\Phi([x]_N)\Phi([y]_N)
\end{align}
$$

Setting $x=1$ in $(19)$ gives $\Phi([1]_N)=([1]_{n_1},\ldots,[1]_{n_k}).$ We therefore have a bijective function that preserves addition, multiplication and the multiplicative identity, namely a [ring isomorphism](../homomorphisms-and-isomorphisms/). The Chinese remainder theorem thus takes the form:

$$
\mathbb{Z}/N\mathbb{Z}\cong\mathbb{Z}/n_1\mathbb{Z}\times\cdots\times\mathbb{Z}/n_k\mathbb{Z}
$$
