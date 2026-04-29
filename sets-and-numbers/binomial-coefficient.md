# Binomial Coefficient

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/binomial-coefficient/

## Introduction

Given two non-negative natural numbers \\(k\\) and \\(n\\), the binomial coefficient denotes the number of ways to combine a specific number of elements \\(k\\) from a larger set of \\(n\\) elements, disregarding the selection order. It is denoted by the notation \\(n\\) choose \\(k\\), and its formula is:

\\[ \binom{n}{k} = \begin{cases} \displaystyle\frac{n!}{k!\\,(n-k)!} & \text{if}\\,0 \leq k
 \leq n \\\\[6pt] 0 & \text{if}\,k > n \end{cases} \\]

* \\(n\\) represents the number of elements in the set.
* \\(k\\) indicates the number of elements to be selected.
* \\(n!\\) and \\((n-k)!\\) are two [factorials](../factorial/).

For example, to determine the value of the binomial coefficient \\( \large{4 \choose 2} \\), we count the number of pairs that can be formed from a set of four elements. Starting from a generic set \\(P=(p,q,r,s)\\), the number of subsets formed by two elements is six, and they are:

\\[ (p,q) \quad (p,r) \quad (p,s) \quad (q,r) \quad (q,s) \quad (r,s) \\]

Unlike permutations, where order matters, the pairs \\((p,q)\\) and \\((q,p)\\) describe the same selection and are counted once. The expression \\( \frac{n!}{(n-k)!} \\) counts the ordered selections of \\(k\\) elements from a set of \\(n\\): since order does not matter, each unordered subset is counted \\(k!\\) times, once per arrangement of its elements. Dividing by \\(k!\\) removes the double counting and yields:

\\[ \binom{n}{k} = \frac{n!}{(n-k)!} \cdot \frac{1}{k!} = \frac{n!}{k!\\,(n-k)!} \\]

> The binomial coefficient appears in the [binomial theorem](../binomial-theorem/), where it gives the coefficients of each term in the expansion of \\((a+b)^n\\).

- - -
## Pascal's triangle

Pascal's triangle is a triangular arrangement of binomial coefficients, the coefficients that appear in the expansion of the [binomial](../binomial/) \\((a+b)\\) raised to a non-negative integer power \\(n\\). The first row contains only \\(1\\), and each number in the subsequent rows is the sum of the two numbers directly above it. The outermost elements of every row are always 1. Here are the first six rows:

\\[
\begin{array}{c}
1  \\\\
1 \quad 1  \\\\
1 \quad 2 \quad 1  \\\\
1 \quad 3 \quad 3 \quad 1  \\\\
1 \quad 4 \quad 6 \quad 4 \quad 1  \\\\
1 \quad 5 \quad 10 \quad 10 \quad 5 \quad 1
\end{array}
\\]

- - -

Each element in row \\( n \\) and column \\( k \\) corresponds to the binomial coefficient. For example, the number at \\( n = 4, k = 2 \\) is:

\\[
\binom {4}{2} = \frac{4!}{2!(4 - 2)!} = \frac{4!}{2!2!} = \frac{24}{4} = 6 
\\]

And indeed, in the fourth row, the third number is 6.

- - -

Pascal's Triangle satisfies the recurrence relation which directly follows from the triangle's construction:

\\[
\binom{n}{k} = \binom{n - 1}{k - 1} + \binom{n - 1}{k} 
\\]

- - -
## Fundamental properties of the binomial coefficient

The edge property of the binomial coefficient expresses a basic rule that appears along the borders of [Pascal’s triangle](#pascal-triangle). It states that the coefficients located at the two ends of each row are always equal to one:

\\[
\binom{n}{0} = \binom{n}{n} = 1
\\]

For any natural number \\( n \\), there is exactly one possible way to choose none of the available elements, and likewise only one way to choose all of them.

- - -

The symmetry property is observed when selecting a subset of \\(k\\) elements from a set of \\(n\\) elements, with the number of ways to do this always equal to the number of ways to select the remaining \\(n-k\\) elements. This symmetry is reflected in the equivalence: 

\\[ \binom{n}{k} = \binom{n}{n-k} \\]

This principle of symmetric selection is not just a theoretical idea, but a practical tool used in various fields. It is particularly useful in probability theory, combinatorics, and statistics, where it helps in calculating probabilities, counting possibilities, and analyzing data.

- - -

The additive property of the binomial coefficient establishes a relationship between consecutive binomial coefficients. If we consider the binomial coefficients \\( \large{n \choose k} \\) and \\( \large{{n \choose k+1}}\\), then:

\\[{n \choose k} + {n \choose k+1} = {n+1 \choose k+1} \\]

This property is fundamental in practical applications, as it provides a way to quickly compute the value of the next binomial coefficient, knowing the previous ones. It relies on the definition of the binomial coefficient and its recursive relationship, which allows the expression of a binomial coefficient in terms of preceding binomial coefficients.

- - -

The [recursive property](#recursion) describes how each binomial coefficient can be derived from those in the previous row of Pascal’s triangle. According to this relationship, every coefficient is obtained as the sum of the two elements positioned directly above it:

\\[
\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}
\\]

This rule provides a recursive definition for the binomial coefficient and explains the additive structure underlying Pascal’s triangle.

- - -
## Notable identities of the binomial coefficient

Beyond the core properties, the binomial coefficient satisfies a number of deeper identities that appear repeatedly across combinatorics, probability, and analysis. Each of them reflects a structural truth about how counting works.

The row sum identity states that the sum of all binomial coefficients in 
row \\( n \\) of Pascal's triangle equals \\( 2^n \\):

\\[
\sum_{k=0}^{n} \binom{n}{k} = 2^n
\\]

One way to see why this is true: consider a set of \\( n \\) elements. Each element can either be included in a subset or not, giving two independent choices per element. The total number of subsets is therefore \\( 2^n \\), and since \\( \binom{n}{k} \\) counts the subsets of exactly \\( k \\) elements, summing over all possible values of \\( k \\) from \\( 0 \\) to \\( n \\) recovers the same count.

---

The alternating sum identity is a close relative of the row sum, but with alternating signs:

\\[
\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0
\\]

This follows directly from evaluating the binomial theorem at \\( a = 1 \\) and \\( b = -1 \\). The result reflects a symmetry between subsets of even and odd size: for any \\( n \geq 1 \\), there are exactly as many even-sized subsets of an \\( n \\)-element set as there are odd-sized ones.

---

The Vandermonde identity describes what happens when two independent selections are combined into a single one. Given two disjoint groups of \\( m \\) and \\( n \\) elements respectively, the number of ways to choose \\( r \\) elements from the combined group equals:

\\[
\binom{m+n}{r} = \sum_{k=0}^{r} \binom{m}{k} \binom{n}{r-k}
\\]

The reasoning is direct: any selection of \\( r \\) elements from the  combined group must draw exactly \\( k \\) elements from the first group and  \\( r - k \\) from the second, for some value of \\( k \\) between \\( 0 \\) and \\( r \\). Each such split contributes \\( \binom{m}{k} \cdot \binom{n}{r-k} \\) combinations, and summing over all valid values of \\( k \\) gives the total. A particularly useful special case arises when \\( m = n \\) and \\( r = n \\):

\\[
\binom{2n}{n} = \sum_{k=0}^{n} \binom{n}{k}^2
\\]

This tells us that the central binomial coefficient — the middle entry of row  \\( 2n \\) in Pascal's triangle — counts the number of ways to select \\( n \\) elements from a group of \\( 2n \\), which can always be decomposed as choosing \\( k \\) from one half and \\( n - k \\) from the other.

---

The upper summation identity relates a binomial coefficient to a sum of coefficients from earlier rows:

\\[
\sum_{i=0}^{r} \binom{n+i}{i} = \binom{n+r+1}{r}
\\]

The name comes from the shape this identity traces in Pascal's triangle:  a diagonal run of entries whose sum equals a single entry one step to the right and one step down — resembling the blade and handle of a hockey stick. This identity is especially useful when computing cumulative counts that build row by row.

- - -
## Generalized binomial coefficient

The definition introduced at the start of this page requires \\( n \\) and \\( k \\) to be natural numbers. This constraint, however, is not as rigid as it appears. The factorial in the numerator can be replaced by a product that makes sense for any real number \\( \alpha \\), leading to the generalized binomial coefficient:

\\[
\binom{\alpha}{k} = \frac{\alpha(\alpha - 1)(\alpha - 2) \cdots (\alpha - k + 1)}{k!}
\\]

where \\( \alpha \in \mathbb{R} \\) and \\( k \\) remains a non-negative integer. When \\( \alpha \\) is a natural number and \\( k \leq \alpha \\), this expression reduces to the standard binomial coefficient. When \\( \alpha \\) is not a natural number or when \\( k > \alpha \\) it produces values that are no longer integers, but remain well-defined. This generalization is what allows the [binomial theorem](../binomial-theorem/) 
to extend beyond integer exponents. For \\( |x| < 1 \\), Newton showed that:

\\[
(1 + x)^{\alpha} = \sum_{k=0}^{\infty} \binom{\alpha}{k} x^k
\\]

Unlike the standard binomial theorem, this sum does not terminate and it is an infinite series. Two cases are worth noting. Taking \\( \alpha = -1 \\) recovers the [geometric series](../geometric-series/):

\\[
\frac{1}{1+x} = \sum_{k=0}^{\infty} (-1)^k x^k
\\]

Taking \\( \alpha = \tfrac{1}{2} \\) produces the expansion of \\( \sqrt{1+x} \\):

\\[
\sqrt{1+x} = 1 + \frac{1}{2}x - \frac{1}{8}x^2 + \frac{1}{16}x^3 - \cdots
\\]

an approximation used routinely in physics and engineering when \\( x \\) is small. In both cases, the coefficients are computed directly from the generalized binomial coefficient (the same formula, with \\( \alpha \\) no longer restricted to a whole number).

- - -
## Example 1

A research team is made up of 7 scientists and 8 engineers. In how many ways can we form a working group consisting of 3 scientists and 4 engineers? To form the group, we must independently select 3 scientists from 7 and 4 engineers from 8. Since the two selections are independent, the total number of possible combinations is given by:

\\[
N = \binom{7}{3} \times \binom{8}{4}
\\]

Now, compute each term:

\\[
\binom{7}{3} = \frac{7 \times 6 \times 5}{3 \times 2 \times 1} = 35
\\]

\\[
\binom{8}{4} = \frac{8 \times 7 \times 6 \times 5}{4 \times 3 \times 2 \times 1} = 70
\\]

- - -
Therefore, by combining the possible selections of scientists and engineers, we obtain:

\\[
N = 35 \times 70 = 2450
\\]

>This means that, based on our group of scientists and engineers, we can form 2,450 distinct working teams composed of 3 scientists and 4 engineers. 

- - -
## Example 2

Let’s now consider the same situation described in Example 1, but with an additional condition: if 2 engineers have a disagreement and cannot be assigned to the same group, how many valid combinations can be formed? We already know that the total number of possible groups, without any restriction, is 2450.

Now, we must exclude the groups that include both of the two engineers who cannot work together. If both conflicting engineers are included in the same group, we have already chosen 2 specific engineers, so we only need to select the remaining 2 engineers from the other 6:

\\[
\binom{6}{2}
\\]

At the same time, we still need to select 3 scientists from the 7 available:

\\[
\binom{7}{3}
\\]

The number of invalid groups that contain both conflicting engineers is therefore:

\\[
N_{\text{invalid}} = \binom{7}{3} \times \binom{6}{2}
\\]

Substituting the values we have:

\\[
\binom{7}{3} = 35 \qquad \binom{6}{2} = 15
\\]

\\[
N_{\text{invalid}} = 35 \times 15 = 525
\\]

Finally, subtract these invalid cases from the total to find the number of valid combinations:

\\[
N_{\text{valid}} = N_{\text{total}} - N_{\text{invalid}} = 2450 - 525 = 1925
\\]

There are 1,925 valid combinations if the two conflicting engineers cannot be assigned to the same group.

- - -
## Recursion

The binomial coefficient has a natural recursive structure: to count the ways to choose \\( k \\) elements from \\( n \\), it is enough to know the answers to two smaller versions of the same problem.

\\[ \binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k} \\]

The reasoning is combinatorial. Fix one element from the set — call it \\( x \\). Every subset of size \\( k \\) either contains \\( x \\) or it does not. If it does, the remaining \\( k-1 \\) elements must be chosen from the other \\( n-1 \\), giving \\( \binom{n-1}{k-1} \\). If it does not, all \\( k \\) elements come from the remaining \\( n-1 \\), giving \\( \binom{n-1}{k} \\). The two cases are mutually exclusive and together cover all possibilities. For example:

\\[ \binom{3}{2} = \binom{2}{1} + \binom{2}{2} = 2 + 1 = 3 \\]

What makes this identity particularly useful in computing is that the recursion is not imposed on the problem from the outside: it is already there in the mathematics. A recursive function does nothing more than follow that structure directly, reducing each call to two smaller ones until it reaches the base cases:

\\[
\binom{n}{0} = \binom{n}{n} = 1
\\]

> Note that recursion recalculates the same values multiple times. The computational cost grows quickly with \\( n, \\) a problem that memoization solves by storing intermediate results as they are computed. This trade-off between simplicity and efficiency is explored in depth in the analysis of [Big O notation](../big-o-notation/).

- - -
## Foundation of the binomial distribution

The binomial coefficient provides the foundation for the [binomial distribution](../binomial-distribution/), which describes the probability of obtaining a specific number of successes in a fixed number of independent trials. If each trial has only two possible outcomes, success with probability \\( p \\) and failure with probability \\( q = 1 - p \\), the probability of observing exactly \\( x \\) successes in \\( n \\) trials is given by:

\\[
b(x; n, p) = \binom{n}{x} p^{x} q^{n - x}
\\]

This expression combines the binomial coefficient, which counts the number of ways \\( x \\) successes can be arranged across \\( n \\) trials, and the factor \\( p^x q^{n-x} \\), which measures the probability of any one such arrangement. Fixing \\( n \\) and \\( p \\), and letting \\( x \\) vary from \\( 0 \\) to \\( n \\), gives the full distribution, with each outcome weighted by the number of ways it can occur.