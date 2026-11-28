---
title: Fields
source: https://algebrica.org/fields/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - characteristic
  - complex-numbers
  - distributivity
  - field-extension
  - field-theory
  - finite-field
  - homomorphism
  - rational-numbers
  - real-numbers
  - subfield
---

## Definition

A field $F$ is a [commutative ring](../rings/) whose multiplicative identity $1$ is distinct from its additive identity $0$ and in which every element $a \neq 0$ has an inverse $a^{-1} \in F$ satisfying:

$$
\begin{align}
a \cdot a^{-1} &= 1 \tag{1}
\end{align}
$$

For any $a,b \in F$ with $b \neq 0$, the quotient $a/b$ is the element $a \cdot b^{-1}$ of $F$. Under addition, $F$ is an [abelian group](../groups/) with identity $0$, so for every $a \in F$:

$$a+0=a \tag{2}$$

Each element $a$ also has an additive inverse $-a$ satisfying:

$$a+(-a)=0\tag{3}$$

Under multiplication, the nonzero elements of $F$ form an abelian group with identity $1$. Multiplication also distributes over addition, so for all $a,b,c \in F$:

$$a(b+c)=ab+ac\tag{4}$$ 
Equation $(4)$ gives the following identities:

$$
\begin{align}
a \cdot 0 &= 0 \notag\\[6pt]
(-a)b &= a(-b) = -(ab) \notag\\[6pt]
(-a)(-b) &= ab \notag
\end{align}
$$

The existence of inverses allows us to cancel any nonzero factor. If $ab=ac$ and $a \neq 0$, multiplying both sides by $a^{-1}$ and applying $(1)$ gives:

$$
\begin{align}
(a^{-1}a)b &= (a^{-1}a)c \notag\\[6pt]
b &= c \tag{5}
\end{align}
$$

In particular, if $ab=0$ and $a \neq 0$, we can write $ab=a \cdot 0$ and apply $(5)$ with $c=0$ to obtain $b=0$. Thus a field has no zero divisors and, by the definition given in the entry on rings, is an integral domain.

As an example, consider the ring of [integers](../integers/) $\mathbb{Z}$ and why any field containing it must also contain the [rational numbers](../rational-numbers/). Only $1$ and $-1$ have multiplicative inverses in $\mathbb{Z}$, since if two integers $a,b$ satisfy $ab=1$, then $|a||b|=1$ and each has [absolute value](../absolute-value/) $1$. For example, the equation $2x=1$ has the solution $x=1/2$ in $\mathbb{Q}$. More generally, a field containing the integers must contain the inverse $1/q$ of every integer $q \neq 0$ and hence the product $p \cdot (1/q)=p/q$ for every integer $p$. These fractions form the field $\mathbb{Q}$, in which each nonzero element $p/q$ has inverse $q/p$, so $\mathbb{Q}$ is the smallest field containing the integers.

Now consider the equations $x^2=2$ and $x^2=-1$: which of them can we solve over the rationals, [the reals](../real-numbers/), or the [complex numbers](../complex-numbers/)? The equation $x^2=2$ has no rational solutions and has two real solutions, $x=\pm\sqrt{2}$. The equation $x^2=-1$ has no real solutions because the square of a real number is always greater than or equal to zero. Over $\mathbb{C}$, the factorization $x^2+1=(x-i)(x+i)$ gives the two solutions $x=\pm i$.

As a final example, consider [polynomials](../polynomials/) with coefficients in an arbitrary field $K$ and ask whether the ring $K[x]$ is itself a field. If $x$ had an inverse in $K[x]$, there would be a polynomial $g$ such that $xg=1$. This is impossible because for every nonzero $g$ the product $xg$ has degree $\deg(g)+1$, whereas the constant polynomial $1$ has degree zero. The same reasoning applies to every polynomial of positive degree, so the only invertible polynomials are the nonzero constants $c$, each with inverse $1/c$. Since $x$ is nonzero and has no inverse, we conclude that $K[x]$ is not a field.

We now define the characteristic of a field $F$ as the smallest positive integer $n$ for which the sum of $n$ copies of $1$ is $0$. Writing $n \cdot 1$ for this sum, we can express the condition as follows:

$$
\begin{align}
n \cdot 1 &= \underbrace{1+\cdots+1}_{n \text{ terms}} = 0 \tag{6}
\end{align}
$$

If no positive integer satisfies $(6)$, then $F$ is said to have characteristic zero, as is the case for $\mathbb{Q}$, $\mathbb{R}$, and $\mathbb{C}$. In $\mathbb{R}$, for example, the sum of $n$ copies of $1$ is $n$, which is positive for every integer $n \geq 1$. To see why a positive characteristic is always prime, observe that the smallest $n$ satisfying $(6)$ is greater than $1$, since $1 \neq 0$. If $n$ were composite, we could write $n=uv$ with $1 \lt u,v \lt n$. Since $n$ is the first positive integer for which the sum is zero and both $u$ and $v$ are positive integers smaller than $n$, the elements $u \cdot 1$ and $v \cdot 1$ would both be nonzero, yet distributivity and $(6)$ would give a product of zero:

$$
\begin{align}
(u \cdot 1)(v \cdot 1) &= (uv) \cdot 1 \notag\\[6pt]
&= n \cdot 1 = 0 \notag
\end{align}
$$

Since the product of two nonzero elements of a field is nonzero, $n$ cannot be composite and must therefore be prime.

## Finite fields and subfields

We now turn to finite fields, which, as the name suggests, are fields with finitely many elements. For example, consider the residue classes [modulo](../modulo-operator/) $3$, written as follows:

$$
\begin{align}
\mathbb{Z}/3\mathbb{Z} &= \{[0], [1], [2]\} \tag{7}
\end{align}
$$

Recall that to add or multiply two residue classes, we perform the operation on their representatives and take the class of the result. Each of the two nonzero classes in $(7)$ is its own inverse. Indeed, for $[1]$ we have $[1]\cdot[1]=[1]$, and for $[2]$ we have $[2]\cdot[2]=[4]=[1]$, so the ring in $(7)$ is a finite field with three elements. More generally, for every prime $p$, each nonzero class modulo $p$ has an inverse. Indeed, if $[a]$ is a nonzero class modulo $p$, then $a$ and $p$ are relatively prime, so by Bézout's identity there are integers $r$ and $s$ such that:

$$
\begin{align}
ar+ps &= 1 \tag{8}
\end{align}
$$

Reducing $(8)$ modulo $p$ gives $[a][r]=[1]$, since $ps$ has remainder zero. Since $[a]$ was an arbitrary nonzero class, we have found an inverse for every class other than $[0]$. The ring $\mathbb{Z}/p\mathbb{Z}$ is therefore a finite field with $p$ elements, denoted by $\mathbb{F}_p$. Its characteristic is $p$, since the sum of $n$ copies of $[1]$ is $[n]$, and the smallest positive integer for which $[n]=[0]$ is $p$. If we replace the prime modulus $p$ with a composite modulus $n=uv$, where $1 \lt u,v \lt n$, some nonzero classes have no inverse. For example, $[u]$ and $[v]$ are both distinct from $[0]$, but their product is $[uv]=[n]=[0]$, so they are zero divisors and $\mathbb{Z}/n\mathbb{Z}$ is therefore not a field. Thus, for the residue classes modulo $n$ to form a field, $n$ must be prime.

## Subfields and field extensions

A [subset](../sets/) $K$ of a field $F$ is a subfield if it is itself a field under the operations of $F$. To verify this, it suffices to check the following conditions:

$$
\begin{align}
0,1 &\in K \notag\\[6pt]
a-b &\in K &&\forall \ a,b \in K \notag\\[6pt]
\frac{a}{b} &\in K &&\forall \ a,b \in K \text{ with } b \neq 0 \tag{9}
\end{align}
$$

For example, the rational numbers satisfy the conditions in $(9)$ under the usual operations on the real numbers, so $\mathbb{Q}$ is a subfield of $\mathbb{R}$, and similarly $\mathbb{R}$ is a subfield of $\mathbb{C}$, giving the following inclusions:

$$
\begin{align}
\mathbb{Q} \subsetneq \mathbb{R} \subsetneq \mathbb{C} \tag{10}
\end{align}
$$

When $K$ is a subfield of $F$, we say that $F$ is an extension of $K$ and write $F/K$. Taking the elements of $K$ as scalars, we can view $F$ as a [vector space](../vector-spaces/) over $K$ whose dimension is called the degree of the extension and is denoted by $[F:K]$.

To find the degree of the extension $\mathbb{C}/\mathbb{R}$ in $(10)$, we look for a basis of $\mathbb{C}$ as a vector space over $\mathbb{R}$. The elements $1$ and $i$ form a basis because every complex number can be written uniquely as a [linear combination](../linear-combinations/) $a\cdot 1+b\cdot i$ with real coefficients $a,b\in\mathbb{R}$. Since this basis has two elements, the degree of the extension is $[\mathbb{C}:\mathbb{R}]=2$.
