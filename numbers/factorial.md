---
title: Factorial
source: https://algebrica.org/factorial/
license: CC BY-NC 4.0
tags:
  - asymptotic-analysis
  - binomial-coefficient
  - combinatorics
  - factorial
  - gamma-function
  - permutations
  - recursive-definition
  - stirling-approximation
---

## Definition

The factorial of a non-negative integer $n$ is the product of all positive integers from $1$ to $n$ and is denoted by $n!.$ As we shall see in more detail below, the factorial arises in combinatorial problems, particularly in counting the different ways to arrange $n$ distinct objects. For now, we focus on its recursive definition, which, for $n \geq 1,$ is given by the following relation:

$$
\begin{align} \tag{1}
n! &= n \cdot (n-1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1 \\[6pt]
&= n \cdot (n-1)!
\end{align}
$$

For example, the factorial of $4,$ which equals $24,$ is calculated by multiplying all the integers from $4$ down to $1:$

$$
4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24
$$

By convention, the factorial of $0$ equals $1.$ The reason is straightforward. This convention makes the recursive formula in $(1)$ consistent. Setting $n = 1$ in the expression $n \cdot (n-1)!$ gives $1! = 1 \cdot 0!.$ Since $1!$ equals $1,$ the equality requires $0!$ to equal $1$ as well.

Starting from $(1),$ the factorial can also be expressed as a recursive function defined by cases:

$$ \tag{2}
n! =
\begin{cases}
n \cdot (n-1)! & \text{if } n \in \mathbb{N},\ n > 0 \\[6pt]
1 & \text{if } n = 0
\end{cases}
$$

The same definition can be written more compactly using the product symbol $\prod,$ with the index $k$ ranging from $1$ to $n:$

$$\tag{3}
n! =
\begin{cases}
\displaystyle\prod_{k=1}^{n} k & \text{if } n \in \mathbb{N},\ n > 0 \\[6pt]
1 & \text{if } n = 0
\end{cases}
$$

One common application of the factorial is the calculation of the binomial coefficient, which, briefly stated, counts the ways to choose a given number of elements from a set.

Calculating the factorial for $n = 0, 1, 2, 3, \ldots$ gives a sequence of natural numbers whose term of index $n$ is $a_n = n!:$

$$
a_0 = 1,\quad a_1 = 1,\quad a_2 = 2,\quad a_3 = 6,\quad a_4 = 24,\quad \ldots
$$

Another interesting property of the factorial, often omitted from introductory accounts, concerns the prime factorization of $n!.$ For a fixed prime $p,$ its exponent counts the total number of times the factor $p$ occurs in the integers from $1$ to $n.$ In its prime factorization, every multiple of $p$ contains at least one factor $p,$ every multiple of $p^2$ contains at least two, every multiple of $p^3$ at least three, and so on.

The multiples of $p$ between $1$ and $n$ are the numbers $kp,$ where $k$ is a positive integer and $kp \leq n,$ or equivalently, $k \leq n/p.$ Their number is therefore $\lfloor n/p \rfloor,$ the floor of $n/p,$ that is, the greatest integer less than or equal to $n/p.$ Counting the multiples of successive powers of $p$ in the same way gives the exponent:

$$
\left\lfloor \frac{n}{p} \right\rfloor + \left\lfloor \frac{n}{p^2} \right\rfloor + \left\lfloor \frac{n}{p^3} \right\rfloor + \cdots
$$

This sum has finitely many nonzero terms because, whenever $p^j > n,$ we have $\lfloor n/p^j \rfloor = 0.$

To make the reasoning more concrete, we calculate the exponent of the prime factor $2$ in the factorization of $5!,$ taking $n = 5$ and $p = 2.$ In the product $5! = 1 \cdot 2 \cdot 3 \cdot 4 \cdot 5,$ only the multiples of $2,$ namely $2$ and $4,$ contain the prime factor $2.$ We therefore begin by counting one factor $2$ for each of them. However, the number $4 = 2^2$ contains a second factor $2,$ which we count by considering the multiples of $2^2 = 4.$ Between $1$ and $5,$ the only multiple of $4$ is $4,$ and there are no multiples of $2^3 = 8$ or of higher powers. The exponent of $2$ in $5!$ is therefore $3:$

$$
\left\lfloor \frac{5}{2} \right\rfloor + \left\lfloor \frac{5}{4} \right\rfloor = 2 + 1 = 3
$$

Indeed, the prime factorization of $5!$ is $120 = 2^3 \cdot 3 \cdot 5.$

## Simplifying factorial ratios

The definition of the factorial yields algebraic properties that allow us to simplify ratios involving two or more factorials. Suppose, for example, that we have two non-negative integers $n$ and $k$ with $n > k$ and want to calculate the following ratio:

$$
\frac{n!}{(n-k)!}
$$

The factors from $(n-k)$ down to $1$ cancel with the denominator, leaving a product of $k$ factors in the numerator:

$$
\frac{n!}{(n-k)!} = n \cdot (n-1) \cdot \ldots \cdot (n-k+1)
$$

For $k = 0,$ the ratio is $n!/n! = 1,$ and the product on the right is understood to be empty, with value $1.$

Consider, for example, the ratio of $7!$ to $4!.$ The factors from $4$ down to $1$ appear in both the numerator and the denominator and therefore cancel. The numerator is left with the product of the integers from $7$ down to $5:$

$$
\frac{7!}{4!} = \frac{7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}{4 \cdot 3 \cdot 2 \cdot 1} = 7 \cdot 6 \cdot 5 = 210 \tag{4}
$$

The ratio of $7!$ to $4!$ is therefore $210.$ The same reasoning applies when calculating the ratio of $4!$ to $7!.$ Canceling the common factors from $4$ down to $1$ leaves $1$ in the numerator and the product $7 \cdot 6 \cdot 5$ in the denominator.

$$
\frac{4!}{7!} = \frac{4 \cdot 3 \cdot 2 \cdot 1}{7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1} = \frac{1}{210}
$$

The ratio is therefore $1/210,$ the reciprocal of the value in $(4),$ as expected.

## Factorial in combinatorics

As noted at the beginning, the factorial arises in the solution of combinatorial problems. In particular, $n!$ counts the permutations of $n$ distinct objects, that is, the different ways in which these objects can be arranged in order. For example, with $n = 3$ objects, there are $3! = 6$ possible permutations:

$$
\begin{array}{rrrr}
& o_1 & o_2 & o_3 \\[6pt]
\hline
& 1 & 2 & 3 \\[6pt]
& 1 & 3 & 2 \\[6pt]
& 2 & 1 & 3 \\[6pt]
& 2 & 3 & 1 \\[6pt]
& 3 & 1 & 2 \\[6pt]
& 3 & 2 & 1
\end{array}
$$

Suppose we now want to choose just two of our three objects, taking their order into account (choosing $1$ first and then $2$ is different from choosing $2$ first and then $1$). The possible ordered pairs are:

$$
(1,2),\quad (2,1),\quad (1,3),\quad (3,1),\quad (2,3),\quad (3,2)
$$

Each group of two objects appears exactly twice, for example as $(1,2)$ and $(2,1).$ To count the groups without distinguishing their order, we divide the total number of ordered pairs by $2!,$ giving $6/2.$ This yields three groups, consisting of the following objects:

$$
\{1,2\},\quad \{1,3\},\quad \{2,3\}
$$

The same reasoning applies when choosing $k$ objects from $n$ distinct objects, with $1 \leq k \leq n.$ If order matters, we have $n$ choices for the first object, $n-1$ for the second, and so on, down to $n-k+1$ for the $k$th object, because each object can be chosen only once. Multiplying these numbers of choices gives:

$$
n \cdot (n-1) \cdot \ldots \cdot (n-k+1) = \frac{n!}{(n-k)!}
$$

In this count, each group of $k$ objects appears $k!$ times, once for every possible ordering of its elements. If we care only about which objects are chosen, we divide by $k!$ so that each group is counted only once. The resulting number of groups is the binomial coefficient, which deserves a separate treatment and is given by:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!} \tag{5}
$$

## A useful identity involving the factorial

We next consider an identity that helps simplify calculations involving factorials. Consider the following fraction:

$$
\frac{n}{n!}
$$

For $n \geq 1,$ substituting the recursive definition from $(1)$ into the denominator allows the factor $n$ to cancel, giving the identity:

$$
\frac{n}{n!} = \frac{n}{n \cdot (n-1)!} = \frac{1}{(n-1)!}
$$

This identity can be used, for example, to simplify expressions that arise when calculating the mean of the Poisson distribution or when rewriting the binomial coefficient in $(5)$ in a simpler form.

## Relationship between the factorial and the gamma function

At the beginning of this discussion, we defined the factorial only for non-negative integers. This definition can be extended to non-negative real numbers through the gamma function, which is defined for every $c \in \mathbb{R}^+$ by the following improper integral:

$$
\Gamma(c) = \int_{0}^{+\infty} x^{c - 1} e^{-x} \ dx
$$

To obtain the factorial of a number, we evaluate the gamma function at that number plus one. For example, the factorial of $4$ equals $\Gamma(5).$ The following relation provides a way to define the factorial even when the number is not an integer:

$$
\Gamma(n+1) = n! \tag{6}
$$

Relation $(6)$ suggests defining the factorial for every real number $x \geq 0$ as follows:

$$
x! := \Gamma(x+1)
$$

For natural numbers, the gamma function gives the same result as the original definition of the factorial. For example, multiplying the integers from $1$ to $4$ gives $4! = 24,$ and $\Gamma(5) = 24$ as well. If we consider the fraction $1/2,$ however, the definition in $(1)$ does not apply, because $1/2$ is not an integer. We can instead use the extended definition through the gamma function. Since $1/2 + 1 = 3/2,$ we substitute $c = 3/2$ into the integral definition. The exponent of $x$ becomes $3/2 - 1 = 1/2,$ so $x^{1/2} = \sqrt{x}.$ We obtain:

$$
\begin{align}
\left(\frac{1}{2}\right)! &:= \Gamma\left(\frac{3}{2}\right) \\[6pt]
&= \int_{0}^{+\infty} x^{\frac{3}{2}-1}e^{-x} \ dx \\[6pt]
&= \int_{0}^{+\infty} \sqrt{x}e^{-x} \ dx \\[6pt]
&= \frac{\sqrt{\pi}}{2}
\end{align}
$$

> The factor $\sqrt{\pi}$ comes from evaluating the Gaussian integral. We refer to that calculation for a justification of this result.

## Stirling's approximation

Calculating a factorial is not always straightforward or efficient because, as $n$ increases, the factorial grows faster than polynomial functions and exponential functions with a fixed base. In such cases, we use Stirling's approximation to estimate $n!$ for very large values of $n.$ The estimate has the following asymptotic form:

$$
n! \approx \sqrt{2\pi n} \left(\frac{n}{e}\right)^n
$$

Even for relatively small values of $n,$ the factorial can exceed $10^6$ while $2^n$ is still of the order of $10^3.$ The table compares these rates of growth as $n$ increases.

| $n$ | Polynomial $n^2$ | Exponential $2^n$ | Factorial $n!$ |
|-----|------------------|-------------------|----------------|
| 2   | 4                | 4                 | 2              |
| 5   | 25               | 32                | 120            |
| 10  | 100              | 1,024             | 3,628,800      |
| 15  | 225              | 32,768            | Approximately 1.308 trillion |

The approximation becomes increasingly accurate as $n$ grows, so the ratio of $n!$ to its Stirling approximation tends to $1$ as $n$ tends to infinity:

$$
\lim_{n \to \infty} \frac{n!}{\sqrt{2\pi n}\left(\dfrac{n}{e}\right)^n} = 1
$$

For $n = 10,$ the exact value is $10! = 3{,}628{,}800,$ whereas Stirling's estimate is approximately $3{,}598{,}696,$ with a relative error below $1\%.$ For $n > 100,$ the relative error falls below $0.1\%.$ More accurate estimates can be obtained by introducing a correction term, derived by applying the Euler-Maclaurin formula to the sum $\log(n!) = \sum_{k=1}^{n} \log k:$

$$
n! \approx \sqrt{2\pi n} \left(\frac{n}{e}\right)^n \left(1 + \frac{1}{12n}\right) \tag{7}
$$

Formula $(7)$ leads into a more advanced treatment beyond the scope of this discussion, so we limit ourselves to stating the result without developing its proof.
