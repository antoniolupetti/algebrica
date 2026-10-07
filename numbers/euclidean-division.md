---
title: Euclidean Division
source: https://algebrica.org/euclidean-division/
license: CC BY-NC 4.0
tags:
  - divisibility
  - division-algorithm
  - euclidean-algorithm
  - euclidean-division
  - greatest-common-divisor
  - integers
  - quotient
  - remainder
  - well-ordering
---

## Euclidean division theorem

Euclidean division allows us to express an [integer](../integers/) as the sum of a multiple of the divisor and a [remainder](../modulo-operator/). More precisely, the theorem states that given two integers $a$ and $d,$ with $d\gt 0,$ there is a unique pair of integers $(q,r)$ satisfying the conditions:

$$ \tag{1}
\begin{align}
a&=dq+r \\[6pt]
0&\leq r\lt d
\end{align}
$$

The number $a$ is the dividend, $d$ is the divisor, $q$ is the quotient, and $r$ is the remainder. Since $r$ is an integer, it can only take values from $0$ to $d-1,$ whereas the dividend and the quotient may also be negative. For example, to divide $23$ by $5,$ we look for the greatest multiple of $5$ that does not exceed the dividend. Since $20=5\cdot4$ does not exceed $23,$ while the next multiple $25=5\cdot5$ does, we can write:

$$
5\cdot4\leq23\lt 5\cdot5
$$

The quotient is therefore $4$ and the remainder is the difference $23-20=3,$ so the first condition in $(1)$ gives:

$$
23=5\cdot4+3 \tag{2}
$$

The second condition in $(1)$ holds because $0\leq3\lt 5,$ so the pair $(4,3)$ satisfies both conditions of Euclidean division. To clarify this point, $23=5\cdot3+8$ would also be a correct equality, but since the remainder $8$ exceeds the divisor, it does not satisfy the constraint $0\leq r\lt d,$ so $(1)$ does not hold in full.

The quotient $4$ and the remainder $3$ in $(2)$ allow us to express the ratio $23/5$ as the sum of an integer and a [fraction](../rational-numbers/). In general, dividing both sides of the first relation in $(1)$ by $d,$ we obtain:

$$
\frac{a}{d}=q+\frac{r}{d} \tag{3}
$$

In this example, we must therefore add the fraction $3/5$ corresponding to the remainder to the quotient $4,$ giving $23/5=4+3/5.$ The integer quotient $q$ and the ratio $a/d$ are equal if and only if $r=0,$ because the fraction $r/d$ is zero precisely in this case.

A division is said to be exact when the remainder is zero, which is equivalent to saying that the dividend is a multiple of the divisor. In this case, $d$ divides $a,$ a relation denoted by $d\mid a.$

- - -

The proof of the theorem has two parts. In the first, we show that at least one pair of integers $(q,r)$ satisfies both conditions in $(1),$ and in the second, we prove that this pair is unique. We first construct the quotient as the greatest integer whose product with $d$ does not exceed $a.$ To do so, we consider the following [set](../sets/):

$$
A=\{\ k\in\mathbb{Z}\mid kd\leq a\ \} \tag{4}
$$

The set $A$ is nonempty because it contains the integer $k=-|a|,$ for which the condition $d\geq1$ gives:

$$
-|a|d\leq-|a|\leq a
$$

Moreover, $A$ is bounded above by the integer $M=\max\{\ a,0\ \}.$ Indeed, if $k\leq0,$ then $k\leq M,$ while if $k\gt 0$ and $k\in A,$ the inequality $d\geq1$ implies $k\leq kd\leq a\leq M.$

Since $M$ is an [upper bound](../supremum-and-infimum/) for $A,$ the differences $M-k$ are [nonnegative integers](../natural-numbers/) for every $k\in A$ and decrease as $k$ increases, so we can find the maximum of $A$ by finding the minimum of the set:

$$
B=\{\ M-k\mid k\in A\ \}
$$

Since $A$ is nonempty, so is $B,$ and it has a minimum $m$ corresponding to the integer $q=M-m,$ which belongs to $A$ and is its maximum, because $m\leq M-k$ implies $k\leq q$ for every $k\in A.$

Since $q\in A,$ it follows from $(4)$ that $qd\leq a.$ However, the number $q+1$ does not belong to $A,$ since otherwise $q$ would not be the maximum, so the inequality $(q+1)d\leq a$ cannot hold and we must have $(q+1)d\gt a.$ Combining these two inequalities, we obtain:

$$ \tag{5}
qd\leq a\lt (q+1)d
$$

Set $r=a-qd,$ which is an integer because $a,q,d$ are integers. The definition of $r$ gives $a=dq+r,$ and subtracting $qd$ from all three terms in $(5)$ also gives $0\leq r\lt d,$ as required.

We now prove the uniqueness of the quotient and the remainder by assuming that two pairs of integers $(q,r)$ and $(q',r')$ satisfy both conditions in $(1)$ and showing that they are equal. The first condition gives:

$$
a=dq+r=dq'+r' \tag{6}
$$

Both remainders in $(6)$ lie in the [interval](../intervals/) from $0$ to $d-1.$ Rearranging the terms, we obtain:

$$ \tag{7}
d(q-q')=r'-r
$$

Since $r'\geq0$ and $r\lt d,$ we have $r'-r\geq-r\gt -d.$ Moreover, $r\geq0$ and $r'\lt d$ imply $r'-r\leq r'\lt d,$ and combining the two inequalities gives:

$$
-d\lt r'-r\lt d \tag{8}
$$

The left-hand side of $(7)$ is an integer multiple of $d,$ and the only multiple of $d$ strictly between $-d$ and $d$ is zero. Indeed, if the integer $q-q'$ were nonzero, its [absolute value](../absolute-value/) would be at least $1,$ and we would have:

$$
|d(q-q')|=d|q-q'|\geq d \tag{9}
$$

But $(9)$ contradicts $(8),$ so $q=q'.$ Substituting $q'=q$ into $(6)$ gives $dq+r=dq+r',$ from which, by subtracting $dq$ from both sides, we obtain $r=r'.$ The two pairs of numbers are therefore equal, which also proves uniqueness. We have thus proved both assertions of the theorem, namely the existence and uniqueness of the pair of integers $(q,r)$ satisfying the conditions in $(1).$

## Application with a negative dividend

Even when the dividend is negative, the remainder must satisfy the condition $0\leq r\lt d$ in $(1).$ For example, to divide $-23$ by $5,$ we must find two consecutive multiples of $5$ between which the dividend lies. In this case, the following inequalities hold:

$$
5\cdot(-5)=-25\leq-23\lt -20=5\cdot(-4)
$$

The quotient is therefore $-5$ and the remainder is the distance from $-25$ to $-23,$ that is, $-23-(-25)=2,$ so the required division, which expresses the first condition in $(1),$ is:

$$
-23=5\cdot(-5)+2
$$

The division of $-23$ by $5$ just obtained can also be derived from the division $23=5\cdot4+3.$ In general, if $a\gt 0$ and $a=dq+r,$ with $0\lt r\lt d,$ changing signs gives $-a=d(-q)-r.$ The term $-r$ is negative and cannot be the required remainder. To make it positive, we add $d$ to $-r$ and subtract $d$ from the multiple $d(-q),$ obtaining:

$$
-a=d(-q-1)+(d-r)
$$

Since $0\lt d-r\lt d,$ the new quotient is $-q-1$ and the new remainder is $d-r.$ From the division $23=5\cdot4+3,$ we thus obtain $-23=5\cdot(-5)+2.$ When $r=0,$ however, changing signs only changes the sign of the quotient. For example, from $25=5\cdot5,$ we have:

$$
-25=5\cdot(-5)+0
$$

The division of $-25$ by $5$ therefore has quotient $-5$ and remainder $0,$ and in this case the formula with remainder $d-r$ must not be applied because it would give the excluded value $d.$

## Euclidean algorithm

The Euclidean algorithm is a recursive algorithm for computing the [greatest common divisor](../integers/) of two positive integers by repeatedly applying Euclidean division. Suppose that $a$ and $d$ are two positive integers with $a\geq d,$ so that $(1)$ holds. The pairs $(a,d)$ and $(d,r)$ have the same common divisors, because every integer that divides $a$ and $d$ also divides $r=a-dq,$ and conversely, every integer that divides $d$ and $r$ also divides $a=dq+r.$ We can therefore replace the dividend with the divisor and the divisor with the remainder without changing the greatest common divisor, obtaining:

$$
\gcd(a,d)=\gcd(d,r)
$$

If $r=0,$ the division is exact and the greatest common divisor is $d.$ If $r\gt 0,$ however, we divide $d$ by $r$ and repeat the same calculation with the new remainder. We continue until we obtain a remainder of zero, at which point the divisor in the last division is the greatest common divisor of the original numbers.

For example, we calculate $\gcd(252,198)$ as follows:

$$
\begin{align}
252&=198\cdot1+54 \\[6pt]
198&=54\cdot3+36 \\[6pt]
54&=36\cdot1+18 \\[6pt]
36&=18\cdot2+0
\end{align}
$$

The last division has remainder zero, so its divisor is the greatest common divisor of $252$ and $198.$
