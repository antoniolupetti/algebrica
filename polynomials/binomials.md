# Binomials

Source: algebrica.org — CC BY-NC 4.0

## Definition

A binomial refers to a [polynomial](../polynomials) that contains exactly two non-zero terms. Its general form is expressed as \\( (a + b)\\) or \\( (a - b) \\).

In this context, \\(a\\) and \\(b\\) represent non-zero, unlike terms, meaning they cannot be combined into a single term. The degree of a binomial corresponds to the highest degree among its terms. For example, \\(x^3 + 2\\) is a binomial of degree 3, whereas \\(3x - 5\\) is a binomial of degree \\(1\\).

Binomials exhibit properties that facilitate algebraic manipulation. Among these properties are [notable products](../notable-products), which are specific products involving [powers](../powers), binomials, and [trinomials](../trinomials). These products are fundamental for solving equations and for identifying common mathematical patterns.

- - -
## Multiplying two binomials: The FOIL Method

When multiplying two binomials, such as \\((a + b)(c + d)\\) we use the FOIL method to expand the expression. FOIL is an acronym that helps remember the four steps:

- F (First): multiply the first terms: \\( a \cdot c \\)
- O (Outer): multiply the outer terms: \\( a \cdot d \\)
- I (Inner): multiply the inner terms: \\( b \cdot c \\)
- L (Last): multiply the last terms: \\( b \cdot d \\)

Putting it all together we have:

\\[
(a + b)(c + d) = ac + ad + bc + bd
\\]

The FOIL method applies exclusively to the multiplication of two binomials. For products involving polynomials with more than two terms, the general distributive property should be used.

> This method provides an efficient and systematic approach to expanding binomials, particularly when each binomial contains two terms. It ensures comprehensive multiplication and maintains organisational clarity throughout the process.

- - -
## Example 1

To see a practical example of multiplying two binomials, let’s consider the expression:
\\[(x + 3)(x + 5)\\]
  
We can apply the FOIL method, which helps recall the correct order of steps when multiplying the terms of each binomial.  

+ First, multiply the first terms: \\(x \cdot x = x^2\\).  
+ Then, multiply the outer terms: \\(x \cdot 5 = 5x\\).  
+ Next, multiply the inner terms: \\(3 \cdot x = 3x\\).  
+ Finally, multiply the last terms: \\(3 \cdot 5 = 15\\).  

Combining all the results, we get:  
\\[
x^2 + 5x + 3x + 15 = x^2 + 8x + 15
\\]

The final result shows that:  
\\[
(x + 3)(x + 5) = x^2 + 8x + 15
\\]

- - -
## Example 2

Let’s now look at another example that involves the product of two binomials containing [complex numbers](../complex-numbers-introduction/). Consider the following expression:  

\\[
(2x - i)(x + 4i)
\\]  

We can apply the FOIL method, following the same order of multiplication.  

+ First, multiply the first terms: \\(2x \cdot x = 2x^2\\).  
+ Then, multiply the outer terms: \\(2x \cdot 4i = 8xi\\).  
+ Next, multiply the inner terms: \\(-i \cdot x = -xi\\).  
+ Finally, multiply the last terms: \\(-i \cdot 4i = -4i^2\\).  

Combining all results, we get:  
\\[
2x^2 + 8xi - xi - 4i^2
\\]  

Now simplify by combining like terms and recalling that \\(i^2 = -1\\):  
\\[
2x^2 + 7xi - 4(-1) = 2x^2 + 7xi + 4
\\]

The final result shows that:  
\\[
(2x - i)(x + 4i) = 2x^2 + 7xi + 4
\\]


- - -
## Associative, distributive and commutative properties

The associative property states that when adding or multiplying three or more binomials, the grouping does not affect the final result. For addition, given three binomials \\((a + b)\\), \\((c + d)\\), and \\((e + f)\\), the following holds:

\\[((a + b) + (c + d)) + (e + f) = (a + b) + ((c + d) + (e + f))\\]

For multiplication:

\\[((a + b) \cdot (c + d)) \cdot (e + f) = (a + b) \cdot ((c + d) \cdot (e + f))\\]

In both cases, the grouping of the binomials can be changed freely without 
altering the overall result.

- - -

The distributive property is a principle that establishes the connection between multiplication and addition or subtraction. Specifically, it states that multiplying a term by the sum or difference of two other terms is equivalent to distributing the multiplication over each term. Formally:

\\[
\begin{align}
a(b + c) &= ab + ac \\\\[0.5em]
a(b - c) &= ab - ac
\end{align}
\\]

In these expressions, \\(a\\), \\(b\\), and \\(c\\) may represent real numbers, variables, or more complex algebraic expressions. For example, when applied to a binomial:

\\[x(x + 3) = x^2 + 3x\\]

The distributive property serves as a foundational tool for expanding and [factoring](../factoring-ac-method/) expressions, solving equations, and simplifying algebraic expressions.

 - - -

The commutative property states that the order of terms in the addition or multiplication of binomials does not influence the final outcome. For example, given two binomials \\((a + b)\\) and \\((c + d)\\), exchanging their order does not change the overall value.

In the case of addition:
\\[(a + b) + (c + d) = (c + d) + (a + b)\\]

In the case of multiplication:
\\[(a + b) \cdot (c + d) = (c + d) \cdot (a + b)\\]

In both operations, interchanging the order of the two binomials does not alter the result.

> These structural principles extend beyond binomials and originate from the foundational algebraic structure of the real number system. A detailed formal development is available in the section on [properties of real numbers](../properties-of-real-numbers/).

- - -
## Special cases: notable products

Two fundamental examples of [notable products](../notable-products) resulting from binomial multiplication include the following:

\\[(a+b)^2 = a^2 + 2ab + b^2\\]
\\[(a-b)(a+b) = a^2 - b^2\\]

These identities result from repeated application of the distributive property and illustrate recurring algebraic patterns. They are essential for algebraic expansion, simplification, and factorisation. A comprehensive and systematic discussion is provided on the related page.

- - -
## Expansion of a binomial expression

For any [natural number](../natural-numbers) \\( n \\), the expansion of a binomial \\( (a + b)^n \\) is given by the [binomial theorem](../binomial-theorem):

\\[
(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n - k}b^k
\\]

Where \\( \dbinom{n}{k} \\) represents the [binomial coefficient](../binomial-coefficient/) calculated as:  
  \\[
  \binom{n}{k} = \frac{n!}{k!(n - k)!}
  \\]

The sum indicates that all terms are summed for \\( k \\) ranging from \\( 0 \\) to \\( n \\) and \\( a^{n - k}b^k \\) represents the partial terms of the expansion.

- - -

To better understand how the expansion of a binomial works through the binomial theorem, let’s expand the following expression using the formula:  

\\[
(a + b)^5
\\]  

According to the binomial theorem, we can write:  

\\[
(a + b)^5 = \sum_{k=0}^{5} \binom{5}{k} a^{5-k} b^k
\\]  

Expanding each term step by step:  

\\[
\begin{aligned}
(a + b)^5 &= \binom{5}{0}a^5b^0 + \binom{5}{1}a^4b^1 + \binom{5}{2}a^3b^2 + \binom{5}{3}a^2b^3 + \binom{5}{4}a^1b^4 + \binom{5}{5}a^0b^5 \\\\[6pt]
&= 1 \cdot a^5 + 5a^4b + 10a^3b^2 + 10a^2b^3 + 5ab^4 + 1 \cdot b^5
\end{aligned}
\\]  

Combining all the terms, we get the expanded form:  

\\[
(a + b)^5 = a^5 + 5a^4b + 10a^3b^2 + 10a^2b^3 + 5ab^4 + b^5
\\]  

This example shows how the binomial theorem provides a systematic way to expand powers of a binomial expression, where each coefficient corresponds to a term in the fifth row of [Pascal’s triangle](binomial-coefficient/).
