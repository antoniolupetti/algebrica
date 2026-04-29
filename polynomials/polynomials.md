# Polynomials

Source: algebrica.org — CC BY-NC 4.0

## Definition

Let \\(\mathbb{R}\\) represent the field of real numbers. A polynomial in one variable \\(x\\) with coefficients in \\(\mathbb{R}\\) is defined as an expression of the following form:

\\[a_{n}x^{n}+a_{n-1}x^{n-1}+\dotsb +a_{1}x+a_{0}\\]

\\(n\\) is a non-negative integer and \\(a_0, a_1, \ldots, a_n \in \mathbb{R}\\) are referred to as the coefficients, with \\(a_n \neq 0\\). Each term \\(a_k x^k\\) is known as a monomial of degree \\(k\\). Polynomials are typically denoted by \\(P(x)\\) or \\(p(x)\\). The [set](../sets/) of all polynomials in \\(x\\) with real coefficients is denoted by \\(\mathbb{R}[x]\\). This set forms a [ring](../rings/) under two standard operations. For two polynomials:

\\[P(x) = \sum_{k=0}^{n} a_k x^k\\] 
\\[Q(x) = \sum_{k=0}^{m} b_k x^k\\]

their sum is defined by adding the coefficients of corresponding degrees:

\\[(P + Q)(x) = \sum_{k=0}^{\max(n,m)} (a_k + b_k) \\, x^k\\]

The product of two polynomials is defined by the Cauchy convolution of their coefficient sequences:

\\[(P \cdot Q)(x) = \sum_{k=0}^{n+m} \left( \sum_{j=0}^{k} a_j b_{k-j} \right) x^k\\]

Coefficients with indices exceeding the degree of the respective polynomial are defined to be zero. Under these two operations, \\(\mathbb{R}[x]\\) forms a commutative ring with identity and is an integral domain, since the product of two nonzero polynomials is never the zero polynomial.

> The set \\(\mathbb{R}[x]\\) constitutes a ring under the standard operations of addition and multiplication, as the sum, difference, or product of any two polynomials in \\(\mathbb{R}[x]\\) yields another polynomial within the same set.

- - -
## Degree of a polynomial

The degree of a polynomial \\(P(x)\\) is defined as the largest integer \\(k\\) such that the coefficient \\(a_k\\) is nonzero. This degree is denoted as \\(\deg P\\) or \\(\deg P(x)\\). For example, consider the polynomial:

\\[P(x) = 2x^3 - 5x^2 + 3x - 7\\]

\\(P(x)\\) has degree 3, since the largest exponent appearing with a nonzero coefficient is 3. A polynomial may still be of degree 3 even if some intermediate terms are absent: the polynomial \\(P(x) = 4x^3 + x - 2\\) is also of degree 3, despite the absence of the quadratic term.

The degree is well defined due to the requirement that \\(a_n \neq 0\\) in the definition. The leading coefficient uniquely determines the highest-degree term, known as the leading term.

The zero polynomial, where all coefficients are zero, is the only polynomial that is not assigned a degree in the usual sense. By convention, \\(\deg 0 = -\infty\\), a choice motivated by the requirement that the following identity remain valid even when one of the two factors is the zero polynomial:

\\[\deg(P \cdot Q) = \deg P + \deg Q\\]

- - -
## Interpolation and degree of a polynomial

An important implication of the concept of polynomial degree is its role in interpolation. Given \\(n+1\\) distinct points \\(\alpha_0, \alpha_1, \dots, \alpha_n \in \mathbb{R}\\) and corresponding values \\(\beta_0, \beta_1, \dots, \beta_n \in \mathbb{R}\\), there exists a unique polynomial \\(p(x) \in \mathbb{R}[x]\\) of degree at most \\(n\\) that satisfies the following conditions:

\\[p(\alpha_i) = \beta_i \quad \forall \, i = 0, 1, \dots, n\\]

This result demonstrates a direct relationship between the degree of a polynomial and the number of data points necessary for its unique determination. Specifically, a polynomial of degree at most \\(n\\) is uniquely specified by \\(n+1\\) distinct interpolation nodes. The process of constructing such a polynomial is known as polynomial interpolation. Several explicit methods are available for this purpose, with the Lagrange interpolation formula being the most classical approach.

- - -
## Degree of a polynomial and its geometric interpretation

The degree of a polynomial directly influences the shape of its graph in the Cartesian plane, determining the overall behaviour and geometry of the curve. A first-degree polynomial, also referred to as a linear polynomial, produces a graph that is a straight line of the form:

\\[y = mx + q\\]

In this equation, \\(m\\) represents the slope (also known as the angular coefficient), and \\(q\\) denotes the y-intercept. For example, the equation \\(y = 2x + 1\\) defines a specific straight line. The graph shows the equation of the line \\( y = 2x + 1 \\).

> In the equation of a straight line, the slope \\( m \\) corresponds to the [derivative](../derivatives) when the line is tangent to the graph of a function at a given point. In general, the derivative of a function at a point gives the slope of the tangent line at that point.

- - -

Second-degree polynomials, also known as quadratic polynomials, have a graph that corresponds to a [parabola](../parabola) of the form:

\\[y = ax^2 + bx + c \\]

\\(a\\) determines the concavity of the parabola, \\(b\\) and \\(c\\) jointly determine 
the position of the vertex, and \\(c\\) represents the y-intercept. The graph shows the equation of the parabola \\( y = x^2 + 4x - 4.\\) In this case, the parabola opens upward since the coefficient of \\( x^2 \\) is positive.

- - -

Third-degree polynomials, also known as cubic polynomials, have a graph that corresponds to a cubic curve of the form:  
\\[y = ax^3 + bx^2 + cx + d \\]
where \\( a \\) determines the overall shape and orientation of the curve, \\( b \\) and \\( c \\) influence the curvature and inflection points, and \\( d \\) represents the y-intercept.

- - -

## End behavior of polynomial

The end behavior of a polynomial is determined exclusively by its leading term, that is, the term of highest degree \\(a_n x^n\\). As \\(|x|\\) approaches infinity, all lower-degree terms become [asymptotically](../asymptotes/) negligible compared to the growth imposed by the power \\(x^n\\). 

Consequently, the description of the polynomial’s behavior for \\(x \to -\infty\\) and \\(x \to +\infty\\) reduces to analyzing the interplay between the parity of the degree \\(n\\) and the sign of the leading coefficient \\(a_n\\). 

+ When the degree is even, the function \\(x^n\\) is non-negative for all real values of \\(x\\), and the end behavior is therefore symmetric: the polynomial diverges to \\(+\infty\\) if \\(a_n > 0\\) and to \\(-\infty\\) if \\(a_n < 0\\). 

+ When the degree is odd, the power \\(x^n\\) changes sign with \\(x\\), yielding a non-symmetric configuration in which the two ends of the graph point in opposite directions.

| Degree \\(n\\) | \\(a_n\\) | \\(x \to -\infty\\) | \\(x \to +\infty\\) | Direction              | End orientation    |
|----------------|-----------|----------------------|----------------------|------------------------|---------------|
| even           | \\(>0\\)  | \\(+\infty\\)        | \\(+\infty\\)        | same         | \\( \nwarrow \\) \\( \nearrow \\)       |
| even           | \\(<0\\)  | \\(-\infty\\)        | \\(-\infty\\)        | same         | \\( \swarrow \\) \\( \searrow \\)   |
| odd            | \\(>0\\)  | \\(-\infty\\)        | \\(+\infty\\)        | opposite    | \\( \swarrow \\) \\( \nearrow \\)     |
| odd            | \\(<0\\)  | \\(+\infty\\)        | \\(-\infty\\)        | opposite    | \\( \nwarrow \\)  \\( \searrow \\)  |

> In all cases, the leading term fully determines the polynomial’s asymptotic behavior, while the contribution of the remaining terms diminishes progressively as \\(|x|\\) increases.

- - -

To clarify the concept further, let us consider the case in the third row with the following polynomial:
\\[ x^3 + 5x^2 + 5x + 1 \\]

In this case the polynomial exhibits the characteristic end behavior of a cubic function with a positive leading coefficient. As \\(x\\) moves toward \\(-\infty\\), the term of highest degree dominates and forces the graph to decrease without bound, causing the curve to descend on the left side. Conversely, as \\(x\\) approaches \\(+\infty\\), the leading term becomes increasingly positive and drives the entire expression upward, making the graph rise indefinitely on the right side.

| Degree \\(n\\) | \\(a_n\\) | \\(x \to -\infty\\) | \\(x \to +\infty\\) | Direction              | End orientation    |
|----------------|-----------|----------------------|----------------------|------------------------|---------------|
| odd            | \\(>0\\)  | \\(-\infty\\)        | \\(+\infty\\)        | opposite    | \\( \swarrow \\) \\( \nearrow \\)     |


This behavior produces the familiar down–to–up orientation characteristic of all odd-degree polynomials with a positive leading coefficient. Understanding a polynomial’s end behavior directly from its algebraic structure is especially valuable when studying the overall [behavior of functions](../analyzing-the-graphs-of-functions/). By focusing on the leading term \\(a_n x^n\\), one can predict how the graph evolves as \\(x \to +\infty\\) or \\(x \to -\infty\\), since the rapid growth of \\(x^n\\) dominates and makes all lower-degree contributions negligible. In many cases, identifying the degree of the polynomial and the sign of its leading coefficient already provides a clear, immediate indication of the global shape of the function.

- - -
## Monomials, binomials, trinomials

A [monomial](../monomials) is a polynomial expression comprising only one term, a constant, a single variable, or a combination of constants and variables raised to non-negative integer powers. For instance, \\(3x^2\\) and \\(-5y\\) are both monomials.

A [binomial](../binomials) is a polynomial expression consisting of two terms: constants, variables, or the product of constants and variables raised to non-negative integer powers. For example, \\(3x + 7\\) and \\(-2y^2 + 5y\\) are both binomials.

A [trinomial](../trinomial) is a polynomial expression consisting of three terms, which can also be constants, variables, or the product of constants and variables raised to non-negative integer powers. For instance, \\(x^2-2x + 4\\) and \\(3y^3 + 2y^2- y\\) are both trinomials.

- - -
## Sum or difference of two polynomials

The [sum or difference](../adding-and-subtracting-polynomials/) of two polynomials of the same degree results in a polynomial of the same degree, or of lower degree if the terms of highest degree cancel out. For example, if we have two polynomials of degree \\(n\\), say \\(P(x)\\) and \\(Q(x)\\), then their sum or difference, denoted by \\(P(x) ± Q(x)\\), is also a polynomial of degree \\(\leq n\\). 

The sum or difference of the two polynomials is obtained by adding or subtracting the corresponding coefficients of the like terms.

\\[
\begin{align*}
P(x) + Q(x) &= (ax^n + bx^{n-1} + \ldots + z) + (px^n + qx^{n-1} + \ldots + w) \\\\[0.6em]
&= (a+p)x^n + (b+q)x^{n-1} + \ldots + (z+w) \\\\[0.6em]
P(x)-Q(x) &= (ax^n + bx^{n-1} + \ldots + z) - (px^n + qx^{n-1} + \ldots + w) \\\\[0.6em]
&= (a-p)x^n + (b-q)x^{n-1} + \ldots + (z-w)
\end{align*}
\\]

- - -
## Example 1

Given two polynomial \\(P(x)\\) and \\(Q(x)\\), calculate the sum \\(P(x)\\) + \\(Q(x)\\):

\\[ P(x) = x^2 + 3x-1  \\]
\\[ Q(x) = 2x^2-x + 5 \\]

Their sum is given by:

\\\[ P(x) + Q(x) = \left( x^2 + 3x-1 \right) + (2x^2-x + 5) \\]

- - -

Removing the parentheses and collecting terms of equal degree we obtain:

\\[
\\begin{align}
P(x) + Q(x) &= x^2 + 3x - 1 + 2x^2 - x + 5 \\\\[0.5em]
&= (x^2 + 2x^2) + (3x - x) + (-1 + 5) \\\\[0.5em]
&= 3x^2 + 2x + 4
\\end{align}
\\]

The result of the two polynomials \\(P(x) + Q(x)\\) is expressed as: 

\\[3x^2 + 2x + 4 \\]

- - -
## Example 2

Consider two polynomials \\(P(x)\\) and \\(Q(x)\\) of degree \\(n\\). As established above, their sum or difference is a polynomial of degree at most \\(n\\). The following example illustrates the case in which the degree strictly decreases.

\\[ P(x) = 2x^2+3x-1 \\]
\\[ Q(x) = 2x^2-x+5 \\]

The difference \\(P(x)-Q(x)\\) is:

\\[ P(x)-Q(x) = \left( 2x^2+3x-1 \right)-\left( 2x^2-x+5 \right) \\]

Expanding and collecting terms of equal degree:

\\[
\begin{align*}
P(x)-Q(x) &= 2x^2+3x-1-2x^2+x-5 \\\\[0.5em]
&= (2x^2-2x^2)+(3x+x)+(-1-5) \\\\[0.5em]
&= 4x-6
\end{align*}
\\]

> The leading terms of degree \\(n=2\\) cancel exactly, reducing the result to a polynomial of degree \\(n-1=1\\). This confirms that the degree of a sum or difference can be strictly less than the degree of the summands.

- - -
## How to divide two polynomials

[Dividing two polynomials](../polynomial-division/) is a more complex process compared to their addition or subtraction. Given two polynomials \\( P(x) \\) and \\( D(x) \\), it is always possible to determine two polynomials \\( Q(x) \\) and \\( R(x) \\) such that:

\\[P(x) = Q(x) D(x) + R(x) \\]

- \\( Q(x) \\) is the quotient of the division.  
- \\( R(x) \\) is the remainder.  
- The degree of \\( R(x) \\) is strictly less than the degree of \\( D(x) \\)

> This result is known as the polynomial division algorithm, or polynomial long division. It provides a systematic procedure for dividing any polynomial by a nonzero polynomial of lower or equal degree, guaranteeing that the remainder is either zero or of strictly lower degree than the divisor.

- - -

When the division between two polynomials is expressed as a reduced quotient (without explicitly showing the remainder), we obtain a rational function defined as:

\\[
R(x) = \frac{P(x)}{Q(x)}
\\]

where \\( P(x) \\) and \\( Q(x) \\) are polynomials and \\( Q(x) \ne 0 \\).

> In this context, it is worth exploring [rational equations](../rational-equations) and rational inequalities, which involve expressions where both the numerator and the denominator are polynomials.

- - -
## Factoring polynomials

A number \\( \alpha \\) is said to be a [root](../roots-of-a-polynomial/) of the polynomial \\( P(x) \\) if \\( P(\alpha) = 0 \\). The root \\( \alpha \\) is called integer, rational, real, or complex depending on whether \\( \alpha \\) is an integer, a [rational number](../types-of-numbers), a real number, or a [complex number](../complex-numbers-introduction/).

---

The existence of roots over \\( \mathbb{C} \\) is guaranteed by the [Fundamental Theorem of Algebra](../roots-of-a-polynomial/), which states that every non-constant polynomial with complex coefficients has at least one complex root. As a consequence, any polynomial of degree \\( n \\) over \\( \mathbb{C} \\) factors into exactly \\( n \\) linear factors, counted with multiplicity. Over \\( \mathbb{R} \\), the situation is more nuanced: real roots may not always exist, and irreducible quadratic factors with no real roots may appear in the factorization.

Under the assumption that all roots are known, any polynomial \\( P(x) \\) with \\( P(0) \ne 0 \\) admits a factored representation in terms of its roots:

\\[
P(x) = P(0) \prod_{\rho} \left(1 - \frac{x}{\rho} \right)
\\]

where the product runs over all roots \\( \rho \\) of the polynomial, real or complex, counted with multiplicity. This representation expresses the polynomial entirely in terms of the values at which it vanishes, and makes the role of each root explicit in the structure of the expression.

---

The manipulation of polynomials, together with a thorough understanding of their structural properties, underlies a wide range of techniques in algebra and analysis. The following topics extend the material covered in this page and are recommended as natural continuations.

+ [Notable products](../notable-products/)
+ [AC method](../factoring-ac-method/)
+ [Completing the square](../factoring-completing-the-square/)
+ [The Synthetic Division Method](../synthetic-division/)

- - -
## Polynomial Equations

A [polynomial equation](../polynomial-equations/) is an equation of the form:

\\[a_{n}x^{n}+a_{n-1}x^{n-1}+\dotsb +a_{2}x^{2}+a_{1}x+a_{0} = 0\\]

Polynomial equations are classified according to the degree of the leading term. Depending on their degree, they are referred to as [linear](../linear-equations) (degree 1), [quadratic](../quadratic-equations) (degree 2), [cubic](../cubic-equations) (degree 3), or of higher degree when \\(n > 3\\).

- - -
## Polynomial functions

A [polynomial function](../polynomial-function/) is a [function](../functions) of the form:

\\[y = a_{n}x^{n}+a_{n-1}x^{n-1}+\dotsb +a_{2}x^{2}+a_{1}x+a_{0} \\]


Let \\( p(x) \\) and \\( q(x) \\) be two polynomials. If the two polynomial functions are equal for every value of \\( x \\), that is:

\\[ p(x) = q(x) \quad \text{for all } x \\]
  
then the two polynomials are exactly the same, meaning they have the same coefficients. This is known as the identity principle of polynomials.

- - -

Polynomial functions possess several notable analytical properties. 

+ Their domain is the entire real line \\(\mathbb{R}\\), and they are [continuous](../continuous-functions/) and smooth at every point, with no [discontinuities](../discontinuities-of-real-functions/), singularities, cusps, or corners. 
+ As a consequence of their global regularity, polynomial functions do not admit [asymptotes](../asymptotes/) of any kind. 
+ Regarding [symmetry](../even-and-odd-functions/), an odd polynomial function has an [inflection point](../maximum-minimum-and-inflection-points/) at the origin \\((0,0)\\), while an even polynomial function attains a local maximum or minimum at \\(x = 0\\). 