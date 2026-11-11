---
title: Greatest Common Divisor
source: https://algebrica.org/greatest-common-divisor/
license: CC BY-NC 4.0
tags:
  - bezout-identity
  - coprime-integers
  - divisibility
  - euclidean-algorithm
  - euclidean-division
  - greatest-common-divisor
  - integers
---

## Definition

The greatest common divisor of two [integers](../integers/) $m$ and $n,$ at least one of which is nonzero, is their largest positive common divisor and is denoted by $\gcd(m,n).$ The set of these divisors contains $1$ and is finite because each of its elements is at most the [absolute value](../absolute-value/) of any nonzero integer in the pair. To characterize the greatest common divisor in terms of divisibility, we look for a positive integer $d$ that satisfies the following conditions:

$$
\tag{1}
\begin{align}
&d\mid m \\[6pt]
&d\mid n \\[6pt]
&(c\mid m \ \text{and}\ c\mid n)\ \Longrightarrow\ c\mid d
\end{align}
$$

If $d$ satisfies $(1),$ every positive common divisor divides $d$ and is therefore less than or equal to $d.$ It follows that:

$$d=\gcd(m,n)$$

If one of the two integers is zero, their common divisors are the divisors of the other integer, since every integer divides zero. In particular:

$$\gcd(m,0)=|m| \quad \forall \ m\neq0 \tag{2}$$

The Euclidean algorithm is a recursive algorithm for computing the greatest common divisor of two integers using [Euclidean division](../euclidean-division/). If both integers are nonzero, we take their absolute values and order them so that $a\geq b\gt0.$ The first step of the algorithm is to perform Euclidean division of $a$ by $b:$

$$
a=qb+r,\qquad 0\leq r\lt b
\tag{3}
$$

By $(3),$ every common divisor of $a$ and $b$ also divides $r=a-qb,$ and conversely, every common divisor of $b$ and $r$ also divides $a=qb+r.$ The pairs $(a,b)$ and $(b,r)$ therefore have the same common divisors, which gives the identity:

$$
\gcd(a,b)=\gcd(b,r)
\tag{4}
$$

We repeat the division using $(4)$ until the remainder is zero, which must happen because the positive remainders decrease at each step, and the divisor in the final division is the greatest common divisor of the two original integers. For example, to compute the greatest common divisor of $252$ and $198,$ we perform the following divisions:

$$
\tag{5}
\begin{align}
252 &= 1\cdot198+54 \\[6pt]
198 &= 3\cdot54+36 \\[6pt]
54 &= 1\cdot36+18 \\[6pt]
36 &= 2\cdot18+0
\end{align}
$$

The remainder in the last line of $(5)$ is zero, so $\gcd(252,198)=18.$

- - -

The calculation becomes more involved when we extend it to the greatest common divisor of a list of integers $a_1,\ldots,a_k.$ At each step, we compute the greatest common divisor of the previous result and the next integer in the list. To see how this works, we start with $d_1=|a_1|$ and, for each $j=2,\ldots,k,$ compute:

$$
d_j=\gcd(d_{j-1},a_j)
\tag{10}
$$

The divisors of $d_1$ are the same as those of $a_1.$ If the divisors of $d_{j-1}$ are the common divisors of the first $j-1$ integers, then by $(1)$ and $(10)$ the divisors of $d_j$ are those that also divide $a_j.$ By [induction](../principle-of-mathematical-induction/), the divisors of $d_k$ are therefore the common divisors of the entire list, and $d_k=\gcd(a_1,\ldots,a_k).$

The value of $d_k$ determines whether the integers in the list are collectively coprime, which is the case when $d_k=1.$ In particular, as we will see in the next section, two integers $a$ and $b,$ at least one of which is nonzero, are coprime if their only common divisor is $1.$ [Pairwise coprimality](../chinese-remainder-theorem/), by contrast, requires the greatest common divisor of every pair to be $1.$ Consider, for example, the integers $6,10,15.$ No pair is coprime, as the following calculations show:

$$
\begin{align}
\gcd(6,10) &= 2 \\[6pt]
\gcd(6,15) &= 3 \\[6pt]
\gcd(10,15) &= 5
\end{align}
$$

Since $\gcd(6,10)=2,$ the greatest common divisor of all three numbers is $\gcd(2,15)=1,$ so the three integers are coprime.

## Bézout's identity and coprime integers

Bézout's identity expresses the greatest common divisor as a [linear combination](../linear-combinations/) of the two original integers with integer coefficients. More precisely, for any pair of integers $m$ and $n,$ at least one of which is nonzero, there are integers $s$ and $t$ such that:

$$
sm+tn=\gcd(m,n)
\tag{6}
$$

To illustrate how to find the coefficients in $(6),$ we take the integers $252$ and $198$ and work backward through the divisions in $(5).$ We start with the last positive remainder, $18.$ The third line gives $18=54-36.$ We then substitute the expression from the second line for $36$ and the expression from the first line for $54$ to obtain:

$$
\tag{7}
\begin{align}
18 &= 54-36 \\[6pt]
   &= 54-(198-3\cdot54) \\[6pt]
   &= 4\cdot54-198 \\[6pt]
   &= 4(252-198)-198 \\[6pt]
   &= 4\cdot252-5\cdot198
\end{align}
$$

Thus $(7)$ gives the coefficients $s=4$ and $t=-5$ for the pair $(252,198).$ In general, we can work backward in the same way using $(3)$ until the greatest common divisor is expressed in terms of $|m|$ and $|n|.$ If the greatest common divisor is already equal to one of the two absolute values, the coefficients are $1$ for that term and $0$ for the other. To go from $|m|$ and $|n|$ to $m$ and $n,$ we reverse the sign of the coefficient of each negative integer.

Once we have expressed the greatest common divisor $d=\gcd(m,n)$ as a linear combination of $m$ and $n,$ we can obtain all its multiples by multiplying both sides of $(6)$ by an integer $k$ to get an expression of the form:

$$kd=(ks)m+(kt)n$$

Conversely, every integer linear combination of $m$ and $n$ is a multiple of $d,$ since $d$ divides both integers. The integer linear combinations of $m$ and $n$ are therefore exactly the multiples of $d,$ which we can write as:

$$
\{\ sm+tn\mid s,t\in\mathbb{Z}\ \}=d\mathbb{Z}
\tag{8}
$$

Equation $(8)$ gives a characterization of coprime integers. Two integers $a$ and $b,$ at least one of which is nonzero, are coprime if and only if there are integers $s$ and $t$ such that:

$$sa+tb=1$$

If $a$ and $b$ are coprime and both divide an integer $x,$ then their product also divides $x.$ We can write $x=a\alpha=b\beta$ with $\alpha,\beta\in\mathbb{Z}.$ Multiplying $sa+tb=1$ by $x$ and substituting $x=b\beta$ in the first term and $x=a\alpha$ in the second gives the following identity, which expresses $x$ as an integer multiple of $ab:$

$$
x=sax+tbx=ab(s\beta+t\alpha)
\tag{9}
$$
