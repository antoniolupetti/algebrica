---
title: Fundamental Theorem of Arithmetic
source: https://algebrica.org/fundamental-theorem-of-arithmetic/
license: CC BY-NC 4.0
tags:
  - divisibility
  - euclids-lemma
  - fundamental-theorem-of-arithmetic
  - integers
  - prime-factorization
  - prime-numbers
  - unique-factorization
---

## Statement

The fundamental theorem of arithmetic states that every [natural number](../natural-numbers/) $n\geq2$ can be written as a product of primes and that each prime occurs the same number of times in any factorization of $n.$ To prove that a prime factorization exists, we apply [strong induction](../principle-of-mathematical-induction/) to $n.$ As usual in an induction proof, we begin with a base case, which here is $n=2,$ a prime number. For $n\gt2,$ suppose that every natural number from $2$ through $n-1$ has a prime factorization. If $n$ is prime, the product consists of the single factor $n,$ whereas if $n$ is composite, we can write it as follows.

$$
\tag{1}
\begin{align}
n &= ab \\[6pt]
1 &\lt a\lt n \\[6pt]
1 &\lt b\lt n
\end{align}
$$

Since $a$ and $b$ in $(1)$ are less than $n,$ the inductive hypothesis allows us to write each of them as a product of primes. Substituting these two products for $a$ and $b$ gives a prime factorization of $n.$ It follows from this part of the theorem that there are infinitely many primes. If $p_1,\ldots,p_k$ were all the primes, we could consider the natural number defined by:

$$
N=p_1p_2\cdots p_k+1
\tag{2}
$$

Since each $p_i$ divides the product in $(2),$ dividing $N$ by $p_i$ leaves a [remainder](../euclidean-division/) of $1.$ Moreover, since $N\gt1,$ the existence of a prime factorization guarantees that $N$ has at least one prime divisor, which must differ from every prime on the list, so the list cannot be complete.

## Euclid's lemma and uniqueness

Euclid's lemma states that if a prime $p$ divides the product of two [integers](../integers/) $a$ and $b,$ then it divides at least one of the two factors.

$$
p\mid ab \quad\Longrightarrow\quad p\mid a \ \text{or}\ p\mid b
\tag{3}
$$

To prove $(3),$ suppose that $p\mid ab$ and $p\nmid a.$ Since the only positive divisors of $p$ are $1$ and $p,$ the assumption that $p\nmid a$ implies that $\gcd(p,a)=1.$ By [Bézout's identity](../greatest-common-divisor/), there are therefore integers $s,t$ such that $sp+ta=1.$ Multiplying by $b$ gives the following identity.

$$
b=spb+tab
\tag{4}
$$

In $(4),$ the first term is clearly a multiple of $p,$ and so is the second, because $p\mid ab,$ meaning that $ab=pk$ for some integer $k,$ so $tab=p(tk).$ Their sum is therefore divisible by $p.$ By applying $(3)$ to the first factor and the product of the remaining factors, then repeating the argument on the remaining product, we conclude that a prime that divides a finite product divides at least one of its factors. Now suppose that a natural number $n\geq2$ has two prime factorizations satisfying the following identity:

$$
n=p_1p_2\cdots p_r=q_1q_2\cdots q_s
\tag{5}
$$

Since $p_1$ divides the product on the right-hand side of $(5),$ Euclid's lemma implies that $p_1$ divides some $q_j.$ Since $q_j$ is prime, its only positive divisor greater than $1$ is $q_j$ itself, so $p_1=q_j.$ We can then cancel the common factor and repeat the procedure on the remaining products. Once there are no factors left in one product, there must be none left in the other either, because a product containing at least one prime factor is greater than $1.$ The two factorizations therefore have the same factors with the same multiplicities.

## Factorization of nonzero integers

Now consider an integer $n$ with $|n|\gt1,$ and apply the theorem to its [absolute value](../absolute-value/), grouping the occurrences of each prime to obtain the following form:

$$
n=\varepsilon p_1^{e_1}\cdots p_k^{e_k}
\tag{6}
$$

In $(6),$ the product $p_1^{e_1}\cdots p_k^{e_k}$ is the prime factorization of $|n|.$ The numbers $p_1,\ldots,p_k$ are the distinct primes in the factorization, and each exponent $e_i$ gives the number of times the prime $p_i$ occurs. To recover $n$ from $|n|,$ we multiply the product by $\varepsilon,$ which is $1$ if $n$ is positive and $-1$ if $n$ is negative.

For example, since $|-60|=60=2^2\cdot3\cdot5,$ the factor $\varepsilon$ in the factorization of $-60$ is $-1,$ the prime $2$ occurs twice, and the primes $3$ and $5$ occur once each. Thus we obtain $-60=(-1)\cdot2^2\cdot3\cdot5.$ Equation $(6)$ also holds for $n=1$ and $n=-1$ under the convention that a product with no factors equals $1.$ In these two cases, $n$ is therefore equal to $\varepsilon.$

If the integers $a_1,\ldots,a_k$ are [pairwise coprime](../greatest-common-divisor/) and each divides $x,$ then their product $a_1\cdots a_k$ also divides $x.$ For $x=0$ it suffices to observe that $0=(a_1\cdots a_k)\cdot0.$ If $x\neq0,$ all the $a_i$ are nonzero, and we can compare the prime factorizations of their absolute values with that of $|x|.$

Fix a prime $p$ that occurs in the product $|a_1\cdots a_k|.$ If $p$ divided two distinct factors, it would be a common divisor greater than $1,$ contrary to the assumption that the $a_i$ are pairwise coprime. Thus $p$ occurs in exactly one factor $|a_i|,$ and its exponent in the product is the same as in $|a_i|.$ Since $a_i$ divides $x,$ we can write $|x|=|a_i||q|$ for some nonzero integer $q.$ The prime factorization of $|x|$ therefore contains all the occurrences of $p$ in $|a_i|.$ This holds for every prime in the product, so $|a_1\cdots a_k|$ divides $|x|$ and hence $a_1\cdots a_k$ divides $x.$
