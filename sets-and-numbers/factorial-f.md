# Factorial

Source: algebrica.org — CC BY-NC 4.0

## Definition

The factorial of a non-negative [integer](../types-of-numbers/) \\(n\\), written \\(n!\\), is the product of all positive integers from \\(1\\) to \\(n\\):

\\[
\begin{align}
n! &= n \cdot (n-1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1 \\\\[6pt]
&= n \cdot (n-1)!
\end{align}
\\]

For example, the factorial of \\(4\\) is computed as follows:

\\[
4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24
\\]

By convention, the factorial of \\(0\\) is equal to \\(1\\).

The factorial can also be expressed through a recursive [function](../functions/) defined by cases:

\\[
n! =
\begin{cases}
n \cdot (n-1)! & \text{if } n \in \mathbb{N},\ n > 0 \\\\[6pt]
1 & \text{if } n = 0
\end{cases}
\\]

The same definition can be written more compactly using the product symbol \\(\prod\\), where the index \\(k\\) ranges from \\(1\\) to \\(n\\):

\\[
n! =
\begin{cases}
\displaystyle\prod_{k=1}^{n} k & \text{if } n \in \mathbb{N},\ n > 0 \\\\[6pt]
1 & \text{if } n = 0
\end{cases}
\\]

The factorial is used to compute the [binomial coefficient](../binomial-coefficient/), which represents the number of ways to select a given number of elements from a larger set.

- - -
- 
## Simplifying factorial ratios

Suppose we are given two non-negative integers \\(n\\) and \\(k\\) with \\(n > k\\), and we want to compute the following ratio:

\\[
\frac{n!}{(n-k)!}
\\]

The denominator cancels the factors from \\((n-k)\\) to \\(1\\), leaving \\(k\\) terms in the numerator.

\\[
\frac{n!}{(n-k)!} = n \cdot (n-1) \cdot \ldots \cdot (n-k+1)
\\]

Consider the ratio between \\(7!\\) and \\(4!\\). The factors from \\(4\\) down to \\(1\\) appear in both numerator and denominator and therefore cancel. What remains in the numerator is the product of the integers from \\(7\\) down to \\(5\\), which is equal to \\(210\\):

\\[
\frac{7!}{4!} = \frac{7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}{4 \cdot 3 \cdot 2 \cdot 1} = 7 \cdot 6 \cdot 5 = 210
\\]

- - -

## Factorial in combinatorics

In combinatorics, \\(n!\\) counts the possible permutations of \\(n\\) objects. For example, with \\(n = 3\\) objects there are \\(3! = 6\\) possible permutations:

\\[
\begin{array}{rrrr}
& o_1 & o_2 & o_3 \\\\[6pt]
\hline
& 1 & 2 & 3 \\\\[6pt]
& 1 & 3 & 2 \\\\[6pt]
& 2 & 1 & 3 \\\\[6pt]
& 2 & 3 & 1 \\\\[6pt]
& 3 & 1 & 2 \\\\[6pt]
& 3 & 2 & 1
\end{array}
\\]

If the order of selection does not matter, many of these orderings become equivalent. Choosing the objects \\(1, 2, 3\\) is the same as choosing \\(3, 2, 1\\) or any other arrangement of the same three elements. Since each group of \\(k\\) elements can be arranged in \\(k!\\) different ways, dividing by \\(k!\\) eliminates these repetitions and yields the [binomial coefficient](../binomial-coefficient/):

\\[
\binom{n}{k} = \frac{n!}{k! \\, (n-k)!}
\\]

- - -

## A useful identity involving factorial

Starting from the recursive definition \\(n! = n \cdot (n-1)!\\) and substituting it into the denominator of the fraction \\(n/n!\\), the factor \\(n\\) cancels out and we obtain the following identity, which is often useful to simplify expressions involving factorials:

\\[
\frac{n}{n!} = \frac{n}{n \cdot (n-1)!} = \frac{1}{(n-1)!}
\\]

A typical application is the derivation of the mean of the [Poisson distribution](../poisson-distribution/) or the rewriting of binomial coefficients in a simpler form.

- - -

## Relationship between the factorial and the gamma function

The gamma function can be seen as the natural extension of the factorial. Where the factorial is defined only on the [natural numbers](../natural-numbers), the gamma function is defined for every positive real value. For any \\(c \in \mathbb{R}^+\\), the gamma function is defined by the following integral:

\\[
\Gamma\(c\) = \int_{0}^{+\infty} x^{c - 1} e^{-x} \\, dx
\\]

For integer arguments, the gamma function agrees with the factorial, as shown by the identity below:

\\[
\Gamma(n) = (n - 1)!
\\]

So the factorial can be seen as the discrete restriction of the gamma function to the natural numbers.

> The gamma function also appears in the [Beta distribution](../beta-distribution/), where it provides the normalizing constant that makes the total probability integrate to one.

- - -

## Stirling's approximation

Stirling's approximation is used to estimate \\(n!\\) for large values of \\(n\\) when direct multiplication of all terms is not practical. It gives the following asymptotic form:

\\[
n! \approx \sqrt{2\pi n} \left(\frac{n}{e}\right)^n
\\]

This approximation is needed because the factorial grows faster than both [polynomial](../polynomial-function/) and [exponential functions](../exponential-function/). Already for relatively small values, it can exceed \\(10^6\\), while \\(2^n\\) is still around \\(10^3\\).

| \\(n\\) | Polynomial \\(n^2\\) | Exponential \\(2^n\\) | Factorial \\(n!\\) |
|--------|---------------------|----------------------|-------------------|
| 2 | 4 | 4 | 2 |
| 5 | 25 | 32 | 120 |
| 10 | 100 | 1,024 | 3,628,800 |
| 15 | 225 | 32,768 | ~1.307 billion |

The ratio between \\(n!\\) and its Stirling approximation tends to \\(1\\) as \\(n\\) grows without bound:

\\[
\lim_{n \to \infty} \frac{n!}{\sqrt{2\pi n}\left(\dfrac{n}{e}\right)^n} = 1
\\]

This approximation becomes increasingly accurate as \\(n\\) grows. At \\(n = 10\\), the exact value \\(10! = 3{,}628{,}800\\) compares with Stirling's estimate of roughly \\(3{,}598{,}696\\), an error below \\(1\\%\\), while for \\(n > 100\\) the relative error drops under \\(0.1\\%\\). Another way to express the approximation is by introducing a correction term:

\\[
n! \approx \sqrt{2\pi n} \left(\frac{n}{e}\right)^n \left(1 + \frac{1}{12n}\right)
\\]

> Stirling's approximation is used in the asymptotic analysis of [binomial coefficients](../binomial-coefficient/). For any base \\(a > 1\\), the factorial \\(n!\\) always dominates the [exponential](../exponential-function/) \\(a^n\\), that is, \\(\lim_{n \to \infty} a^n/n! = 0\\).