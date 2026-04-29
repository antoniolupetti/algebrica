
## Binomial Theorem

Source: algebrica.org — CC BY-NC 4.0
## Statement

The binomial theorem asserts that for any positive integer \\(n\\), the expression \\((a+b)^n\\) can be expanded as a finite sum of \\(n+1\\) terms. Each term consists of a binomial coefficient multiplied by a [power](../powers/) of \\(a\\) and a power of \\(b\\):

\\[
(a + b)^n = \binom{n}{0} a^n b^0 + \binom{n}{1} a^{n-1} b^1 + \ldots + \binom{n}{n-1} a^1 b^{n-1} + \binom{n}{n} a^0 b^n
\\]

+ The exponent \\(n\\) is a positive integer, that is \\(n \in \mathbb{N}^+\\). 
+ The base \\(a\\) is raised to a decreasing power, from \\(n\\) down to \\(0\\)
+ The base \\(b\\) is raised to an increasing power, from \\(0\\) up to \\(n\\). 
+ The factor \\(\dbinom{n}{k}\\) is the [binomial coefficient](../binomial-coefficient/), where the index \\(k\\) takes integer values between \\(0\\) and \\(n\\).

> The coefficients \\(\binom{n}{k}\\) appearing in the expansion correspond exactly to the entries of the \\(n\\)-th row of [Pascal's triangle](../binomial-coefficient/). The symmetry \\(\binom{n}{k} = \binom{n}{n-k}\\) reflects the fact that choosing \\(k\\) elements from a set of \\(n\\) is equivalent to leaving out the remaining \\(n-k\\).

In its compact form, the binomial theorem can be expressed as a summation of \\(n+1\\) terms:

\\[
(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^k
\\]

- - -
## Binomial coefficient

The [binomial coefficient](../binomial-coefficient/) represents the number of ways to choose \\(k\\) items from a set of \\(n\\) elements, without regard to the order of selection. In combinatorics it is commonly read as "n choose k" and is denoted by:

\\[
\binom{n}{k} = \begin{cases}
\displaystyle \frac{n!}{k!\,(n-k)!} & 0 \leq k \leq n \\\\[6pt]
0 & n < k
\end{cases}
\\]

- \\(n, k \in \mathbb{N}\\).
- \\(n\\) is the total number of elements in the set.
- \\(k\\) is the number of items to be selected.
- \\(n!\\) and \\((n-k)!\\) are the [factorials](../factorial/) of the [natural numbers](../natural-numbers/) \\(n\\) and \\(n-k\\) respectively.

- - -
## Proof

There are two standard proofs of the theorem. The first is based on a combinatorial argument. The expansion of \\((a+b)^n\\) can be viewed as the product of \\(n\\) identical factors:

\\[
(a+b)^n = \underbrace{(a+b)(a+b)\cdots(a+b)}_{n \text{ factors}}
\\]

Each term in the expanded product results from selecting either \\(a\\) or \\(b\\) from each factor. A term of the form \\(a^{n-k} b^k\\) occurs when \\(b\\) is chosen from exactly \\(k\\) of the \\(n\\) factors, and \\(a\\) from the remaining \\(n-k\\). The number of such selections is \\(\binom{n}{k}\\), which enumerates the \\(k\\)-element subsets of the \\(n\\) factors. Summing over all possible values of \\(k\\) from \\(0\\) to \\(n\\) establishes the theorem.

The second proof uses [mathematical induction](../principle-of-mathematical-induction/) on \\(n\\). For \\(n = 1\\) the identity becomes \\((a+b)^1 = a + b\\), which is clearly valid. Assume the theorem holds for some integer \\(n \geq 1\\). Multiplying both sides of the inductive hypothesis by \\((a+b)\\) yields:

\\[
\begin{align}
(a+b)^{n+1} &= (a+b) \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^k \\\\[6pt]
&= \sum_{k=0}^{n} \binom{n}{k} a^{n-k+1} b^k + \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^{k+1}
\end{align}
\\]

Re-indexing the second sum by setting \\(j = k+1\\) and isolating the edge terms gives:

\\[
(a+b)^{n+1} = a^{n+1} + \sum_{k=1}^{n} \left[\binom{n}{k} + \binom{n}{k-1}\right] a^{n+1-k} b^{k} + b^{n+1}
\\]

Applying Pascal's identity \\(\binom{n}{k} + \binom{n}{k-1} = \binom{n+1}{k}\\) to the interior coefficients yields:

\\[
(a+b)^{n+1} = \sum_{k=0}^{n+1} \binom{n+1}{k} a^{n+1-k} b^k
\\]

This is the statement of the binomial theorem for \\(n+1\\), which completes the induction.

- - -
## Properties of the binomial expansion

The binomial theorem gives rise to several identities that follow directly from specific choices of \\(a\\) and \\(b\\), or from structural features of the coefficients themselves.

The sum of all binomial coefficients of order \\(n\\) is obtained by setting \\(a = b = 1\\) in the expansion. The left-hand side becomes \\(2^n\\), so:

\\[
\sum_{k=0}^{n} \binom{n}{k} = 2^n
\\]

This identity admits a combinatorial interpretation: the total number of subsets of a set with \\(n\\) elements equals \\(2^n\\), and each subset corresponds to choosing some \\(k\\) elements out of \\(n\\) for a value of \\(k\\) between \\(0\\) and \\(n\\). Setting \\(a = 1\\) and \\(b = -1\\) yields the alternating sum identity:

\\[
\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0 \qquad \text{for } n \geq 1
\\]

The relation states that, for any positive integer \\(n\\), the number of subsets of even cardinality equals the number of subsets of odd cardinality. The coefficients of the expansion satisfy the symmetry relation:

\\[
\binom{n}{k} = \binom{n}{n-k}
\\]

As a consequence, the expansion of \\((a+b)^n\\) is symmetric: the coefficient of \\(a^{n-k} b^k\\) coincides with the coefficient of \\(a^k b^{n-k}\\). When the two are listed in order, the sequence of coefficients reads identically from left to right and from right to left.

The general term of the expansion, often denoted \\(T_{k+1}\\), is:

\\[
T_{k+1} = \binom{n}{k} a^{n-k} b^k
\\]

The index \\(k+1\\) reflects the position of the term in the expansion, since \\(k\\) ranges from \\(0\\) to \\(n\\) and the first term corresponds to \\(k = 0\\). This formulation is useful when a specific term of the expansion is required without computing the full sum.

- - -
## Special cases

Several classical identities arise as particular instances of the binomial theorem and are worth stating explicitly for their frequent use in algebraic manipulation. 

The case \\(n = 2\\) reproduces the well-known identity for the square of a binomial:

\\[
(a + b)^2 = a^2 + 2ab + b^2
\\]

The three coefficients \\(1, 2, 1\\) correspond to the second row of Pascal's triangle, and the expansion contains the cross term \\(2ab\\) arising from the two ways of selecting one factor of \\(a\\) and one factor of \\(b\\).

The case \\(n = 3\\) gives the cube of a binomial:

\\[
(a + b)^3 = a^3 + 3a^2 b + 3a b^2 + b^3
\\]

The coefficients \\(1, 3, 3, 1\\) form the third row of Pascal's triangle. The two interior coefficients are equal, in agreement with the symmetry relation \\(\binom{3}{1} = \binom{3}{2}\\). When one of the two terms is equal to \\(1\\), the theorem reduces to the expansion of \\((1 + x)^n\\):

\\[
(1 + x)^n = \sum_{k=0}^{n} \binom{n}{k} x^k
\\]

This form is particularly important since it expresses \\((1+x)^n\\) as a [polynomial](../polynomials/) in \\(x\\) whose coefficients are precisely the binomial coefficients of order \\(n\\). It also serves as the starting point for the generalization to real and complex exponents, known as the binomial series.

Setting \\(x = 1\\) in the previous identity recovers the sum of binomial coefficients already discussed, while setting \\(x = -1\\) yields the alternating sum. These two evaluations show how the special case \\((1+x)^n\\) encodes, in a single expression, the structural identities satisfied by the binomial coefficients.

- - -
## Example 1

Consider the expansion of \\((x + 2)^4\\) using the binomial theorem, with \\(a = x\\), \\(b = 2\\), and \\(n = 4\\). Applying the formula:

\\[
(x + 2)^4 = \sum_{k=0}^{4} \binom{4}{k} x^{4-k} \cdot 2^k
\\]

Computing each term of the summation:

\\[
\begin{align}
k = 0 &\quad \binom{4}{0} x^4 \cdot 2^0 = x^4 \\\\[6pt]
k = 1 &\quad \binom{4}{1} x^3 \cdot 2^1 = 8x^3 \\\\[6pt]
k = 2 &\quad \binom{4}{2} x^2 \cdot 2^2 = 24x^2 \\\\[6pt]
k = 3 &\quad \binom{4}{3} x^1 \cdot 2^3 = 32x \\\\[6pt]
k = 4 &\quad \binom{4}{4} x^0 \cdot 2^4 = 16
\end{align}
\\]

Summing all the terms, the expansion is:

\\[(x+2)^4 = x^4 + 8x^3 + 24x^2 + 32x + 16\\]

- - -
## Example 2

For a binomial involving subtraction, the binomial theorem applies with \\(b\\) replaced by a negative value. The signs alternate in the expansion because \\((-1)^k\\) yields a positive value for even \\(k\\) and a negative value for odd \\(k\\). Consider the expansion of \\((x - 1)^5\\), where \\(a = x\\), \\(b = -1\\), and \\(n = 5\\):

\\[
(x - 1)^5 = \sum_{k=0}^{5} \binom{5}{k} x^{5-k} \cdot (-1)^k
\\]

Each term of the summation is computed as follows:

\\[
\begin{align}
k = 0 &\quad \binom{5}{0} x^5 \cdot (-1)^0 = x^5 \\\\[6pt]
k = 1 &\quad \binom{5}{1} x^4 \cdot (-1)^1 = -5x^4 \\\\[6pt]
k = 2 &\quad \binom{5}{2} x^3 \cdot (-1)^2 = 10x^3 \\\\[6pt]
k = 3 &\quad \binom{5}{3} x^2 \cdot (-1)^3 = -10x^2 \\\\[6pt]
k = 4 &\quad \binom{5}{4} x^1 \cdot (-1)^4 = 5x \\\\[6pt]
k = 5 &\quad \binom{5}{5} x^0 \cdot (-1)^5 = -1
\end{align}
\\]

Summing all the terms, the expansion is:

\\[
(x - 1)^5 = x^5 - 5x^4 + 10x^3 - 10x^2 + 5x - 1
\\]