# Factoring Polynomials: AC Method

Source: algebrica.org — CC BY-NC 4.0

## Introduction

A [trinomial](../trinomials/) of the form \\( ax^2 + bx + c \\), where \\( a, b, c \in \mathbb{Z} \\) and \\( a \neq 0 \\), is considered factorable over \\( \mathbb{Z} \\) if it can be written as the product of two linear [polynomials](../polynomials) with [integer](../integers/) coefficients. Specifically, this occurs if there exist integers \\( p, q, r, s \\) such that:

\\[ ax^2 + bx + c = (px + q)(rx + s) \\]

Expanding the right-hand side results in \\( pr \cdot x^2 + (ps + qr)x + qs \\), which leads to the identities:

\\[\begin{align}
a &= pr \\\\[6pt]
b &= ps + qr \\\\[6pt]
c &= qs
\end{align}\\]

The AC method exploits the multiplicative relationships among these constraints. Notably:

\\[ ac = pr \cdot qs = (ps)(qr) \\]

while simultaneously \\( b = ps + qr \\). Defining \\( m = ps \\) and \\( n = qr \\), the problem reduces to finding two integers satisfying:

\\[\begin{align}
mn &= ac \\\\[6pt]
m + n &= b
\end{align}\\]

The existence of such a pair \\( (m, n) \\) is both necessary and sufficient for the trinomial to be factorable over \\( \mathbb{Z} \\). If no such integer pair exists, the trinomial is irreducible over \\( \mathbb{Z} \\), though it may still admit a factorization over \\( \mathbb{Q} \\) or \\( \mathbb{R} \\), depending on the sign of the [discriminant](../quadratic-formula/) \\( b^2 - 4ac \\).

- - -
## The method

Consider a trinomial with integer coefficients in the standard form: 
\\[ ax^2 + bx + c \\]

The procedure is as follows. Compute the product \\( ac \\). Then identify integers \\( m \\) and \\( n \\), if they exist, such that \\( mn = ac \\) and \\( m + n = b \\). This amounts to enumerating the integer divisor pairs of \\( ac \\) and verifying which pair satisfies the sum condition. Once suitable values have been found, rewrite the middle term by splitting \\( bx \\) into \\( mx + nx \\):

\\[ ax^2 + bx + c = ax^2 + mx + nx + c \\]

Group the terms into pairs and factor out the greatest common divisor from each group:

\\[ ax^2 + mx + nx + c = (ax^2 + mx) + (nx + c) \\]

Each group yields a [monomial](../monomials/) factor, and the two resulting expressions share a common linear binomial. Extracting that common factor gives the complete factorisation of the trinomial as a product of two linear polynomials.

The two possible orderings of the pair, \\( (m, n) \\) and \\( (n, m) \\), result in different intermediate groupings but necessarily produce the same factorisation, since the product \\( (px + q)(rx + s) \\) is invariant under exchange of its factors.

- - -

In summary, the procedure reduces to the following steps:

- Compute \\( ac \\).
- List the integer divisor pairs of \\( ac \\).
- Identify the pair \\( (m, n) \\) whose sum equals \\( b \\).
- Rewrite the middle term as \\( mx + nx \\).
- Factor by grouping to extract the common linear binomial.
- - -
## Example 1

Consider the trinomial \\( 2x^2 + 7x + 3 \\). In this case, \\( a = 2 \\), \\( b = 7 \\), and \\( c = 3 \\), so \\( ac = 6 \\). The task is to find integers \\( m \\) and \\( n \\) such that \\( mn = 6 \\) and \\( m + n = 7 \\). The integer pairs \\( (m, n) \\) with \\( mn = 6 \\), listed by absolute value, are:

\\[ \begin{array}{rrrr} m & n & mn & m+n \\\\ \hline 1 & 6 & 6 & 7 \\\\ 2 & 3 & 6 & 5 \\\\ -1 & -6 & 6 & -7 \\\\ -2 & -3 & 6 & -5 \end{array} \\]

The pair \\( (m, n) = (1, 6) \\) satisfies both conditions. The trinomial can therefore be rewritten as

\\[ 2x^2 + 7x + 3 = 2x^2 + x + 6x + 3 \\]

Group the first two terms and the last two terms as follows:

\\[ 2x^2 + x + 6x + 3 = x(2x + 1) + 3(2x + 1) \\]

The [binomial](../binomials/) \\( (2x + 1) \\) is a common factor in both groups, thus we obtain:

\\[ x(2x + 1) + 3(2x + 1) = (x + 3)(2x + 1) \\]

Therefore, the trinomial factors as:

\\[ 2x^2 + 7x + 3 = (x + 3)(2x + 1) \\]

Consequently, the [roots](../roots-of-a-polynomial/) of the associated equation \\( 2x^2 + 7x + 3 = 0 \\) follow from the zero-product property, which states that a product of real numbers is zero if and only if at least one factor is zero.

This yields:

\\[x_1 = -3 \quad x_2 = -\frac{1}{2}\\]

> These results can be verified using the [quadratic formula](../quadratic-formula/) which returns the same values, confirming that the factorisation \\( (x + 3)(2x + 1) \\) is correct.

- - -
## Relation to Vieta's formulas

The conditions \\( mn = ac \\) and \\( m + n = b \\), which are central to the AC method, are closely related to a classical result in polynomial theory. [Vieta's formulas](../trinomials/) state that, for a monic quadratic \\( x^2 + px + q \\) with roots \\( x_1 \\) and \\( x_2 \\), the following relationships hold:

\\[\begin{align}
x_1 + x_2 &= -p \\\\
x_1 \cdot x_2 &= q
\end{align}\\]

In the special case where \\( a = 1 \\), the trinomial simplifies to \\( x^2 + bx + c \\), and the AC conditions become \\( mn = c \\) and \\( m + n = b \\). Vieta's formulas for this polynomial give \\( x_1 + x_2 = -b \\) and \\( x_1 x_2 = c \\), so one has \\( m = -x_1 \\) and \\( n = -x_2 \\): the integers sought by the AC method are the negatives of the roots, and the search for the pair is equivalent to a direct application of Vieta's formulas.

- - -

When \\( a \neq 1 \\), the correspondence is less direct but remains present. Multiplying the trinomial by \\( a \\) yields

\\[ a(ax^2 + bx + c) = (ax)^2 + b(ax) + ac \\]

which is a monic quadratic in the auxiliary variable \\( u = ax \\). Applying Vieta's formulas to this scaled polynomial requires identifying two numbers whose sum is \\( b \\) and whose product is \\( ac \\), which aligns precisely with the conditions imposed on \\( m \\) and \\( n \\) by the AC method. 

> The AC method can therefore be interpreted as an application of Vieta's formulas to a rescaled polynomial, with the splitting of the middle term serving as the mechanism that transfers the factorisation of the auxiliary polynomial back to the original trinomial.

- - -
## On the irreducibility of quadratic trinomials

When no integer pair \\( (m, n) \\) satisfies \\( mn = ac \\) and \\( m + n = b \\), the trinomial is irreducible over \\( \mathbb{Z} \\). This occurs precisely when the discriminant \\( \Delta = b^2 - 4ac \\) is not a perfect square integer. 

When \\( \Delta > 0 \\) but not a perfect square integer, the trinomial has two distinct irrational real roots and is irreducible over both \\( \mathbb{Z} \\) and \\( \mathbb{Q} \\); when \\( \Delta < 0 \\), it has two complex conjugate roots and is likewise irreducible over \\( \mathbb{R} \\).

When \\( \Delta = 0 \\), the trinomial has a repeated root \\( x = -b/(2a) \\), which is rational but not necessarily an integer, so irreducibility over \\( \mathbb{Z} \\) depends on whether \\( 2a \mid b \\). The AC method, being combinatorial in nature, terminates without output once all integer divisor pairs of \\( ac \\) have been checked without success, and this exhaustion of cases constitutes a constructive proof of irreducibility over \\( \mathbb{Z} \\).

- - - 

For illustration, consider the trinomial \\( 3x^2 + 5x + 4 \\). In this case, \\( a = 3 \\), \\( b = 5 \\), and \\( c = 4 \\), yielding \\( ac = 12 \\). The integer divisor pairs of \\( 12 \\) are as follows:

\\[ \begin{array}{rrrr} m & n & mn & m+n \\\\ \hline 1 & 12 & 12 & 13 \\\\ 2 & 6 & 12 & 8 \\\\ 3 & 4 & 12 & 7 \\\\ -1 & -12 & 12 & -13 \\\\ -2 & -6 & 12 & -8 \\\\ -3 & -4 & 12 & -7 \end{array} \\]

None of these pairs satisfies the condition \\( m + n = 5 \\). The discriminant confirms this: \\( \Delta = b^2 - 4ac = 25 - 48 = -23 < 0 \\). Because \\( \Delta < 0 \\), the trinomial has two [complex conjugate roots](../quadratic-equations-with-complex-solutions/):

\\[\begin{align}
x_{1,2} &= \frac{-5 \pm i\sqrt{23}}{6}
\end{align}\\]

So, the trinomial admits no factorisation over \\( \mathbb{R} \\), nor over \\( \mathbb{Z} \\).

- - -
## Limitations of the AC method

The AC method is effective when the coefficients are small integers and the divisor search concludes rapidly. Its computational cost grows with the number of integer divisor pairs of \\( ac \\). 

When \\( |ac| \\) is large, the enumeration becomes laborious and the method loses its practical advantage over direct application of the quadratic formula. More fundamentally, the method is inherently tied to factorisation over \\( \mathbb{Z} \\). 

When the trinomial is irreducible over \\( \mathbb{Z} \\) but possesses real roots, one must resort to the [quadratic formula](../quadratic-formula/), which returns the exact roots regardless of whether the discriminant is a perfect square.

- - -
## An additional connection

Multiplying the trinomial \\( ax^2 + bx + c \\) by \\( a \\) produces a monic quadratic in the auxiliary variable \\( u = ax \\):

\\[\begin{align}
a(ax^2 + bx + c) &= (ax)^2 + b(ax) + ac \\\\[6pt]
&= u^2 + bu + ac
\end{align}\\]

This polynomial factors over \\( \mathbb{Z} \\) as \\( (u + m)(u + n) \\), where \\( mn = ac \\) and \\( m + n = b \\). 

Substituting back \\( u = ax \\) gives \\( (ax + m)(ax + n) = a^2x^2 + b(ax) + ac \\), which equals \\( a(ax^2 + bx + c) \\), confirming the identity without leaving \\( \mathbb{Z}[x] \\). 

This scaling argument demonstrates that the AC method is equivalent to factoring a monic quadratic in a rescaled variable, and connects to the notion of reducibility in the polynomial [ring](../rings/) \\( \mathbb{Z}[x] \\). The trinomial \\( ax^2 + bx + c \\) is reducible in \\( \mathbb{Z}[x] \\) if and only if the integer pair \\( (m, n) \\) exists.