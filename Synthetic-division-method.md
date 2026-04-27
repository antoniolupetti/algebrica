
# The Synthetic Division Method

Source: algebrica.org — CC BY-NC 4.0

## Introduction

The synthetic division (or Ruffini's rule) is a method for dividing a polynomial by a binomial of the form \\((x - a)\\). It is widely used to factorize [polynomials](../polynomials) and to simplify the resolution of [equations](../equations) of degree higher than two, especially when these cannot be reduced to [quadratic equations](../quadratic-equations), [monomials](../monomials), or standard [trinomials](../trinomials). When \\(a\\) is a [root](../roots-of-a-polynomial/) of a polynomial \\(P(x)\\) of degree \\(n\\) and the [binomial](../binomials/) \\((x - r)\\) is a factor of \\(P(x)\\) we can write:

\\[
P(x) = (x - r)\\, Q(x)
\\]
where \\(Q(x)\\) is a polynomial of degree \\(n - 1\\).

- - -
Synthetic division is useful for two reasons:

+ The method provides a simple way to divide by \\((x - r)\\), making the factorization of a polynomial almost immediate once a root has been identified.

+ Since each step lowers the degree of the polynomial, higher-degree equations become easier to deal with, and other roots or factors often show up along the way.

Although this method is often used in conjunction with the rational root theorem, it is not the only available technique. Depending on how the expression is built, other tools, like [special products](../notable-products) or factoring methods such as [the AC method](../factoring-ac-method/), can sometimes get you to the factorization more easily or directly.

- - -

## Rational root theorem

The rational root theorem is used to find the rational roots of a polynomial with integer coefficients, when they exist. Consider a polynomial of the form:

\\[
P(x) = a_{n}x^{n} + a_{n-1}x^{n-1} + \dotsb + a_{1}x + a_{0}
\\]

where the coefficients \\(a_n, a_{n-1}, \dotsc, a_0 \in \mathbb{Z}\\) and \\(a_n \neq 0\\). The rational root theorem states that if \\(P(x)\\) admits a rational root, then that root can always be written as:

\\[
r = \frac{p}{q}
\\]

where \\(p\\) and \\(q\\) are coprime integers, \\(p\\) is a divisor of the constant term \\(a_0\\) and \\(q\\) is a divisor of the leading coefficient \\(a_n\\). Both positive and negative divisors are admitted, since the sign of \\(r\\) depends on the signs of \\(p\\) and \\(q\\). In this way it is possible to reduce the search for rational solutions to a finite list of possible candidates, obtained by combining the divisors of \\(a_0\\) with those of \\(a_n\\).

> Two integers are coprime when their greatest common divisor is \\(1\\). It means they share no factor other than \\(1\\).

- - -

## Statement of the method

To illustrate how the method works, consider a polynomial \\(P(x)\\) of degree \\(n\\) with real coefficients:

\\[
P(x) = a_{n}x^{n} + a_{n-1}x^{n-1} + \dotsb + a_{1}x + a_{0}
\\]

Dividing \\(P(x)\\) by a binomial of the form \\((x - r)\\), with \\(r\\) real, the result can be written as:

\\[
P(x) = (x - r)\\, Q(x) + R
\\]

\\(Q(x)\\), the quotient, is a polynomial of degree \\(n - 1\\). \\(R\\) is the remainder (a real constant) and, by the remainder theorem, coincides with the value of \\(P\(r\)\\). Moreover, if \\(r\\) is a root of \\(P(x)\\), the remainder is zero and \\((x - r)\\) becomes a factor of the polynomial.

The procedure as a whole is fairly mechanical and follows these steps:

+ Write down the coefficients of \\(P(x)\\) starting from the highest degree, and remember to put a zero whenever a power of \\(x\\) is missing.
+ Place the candidate root \\(r\\) to the left of the row of coefficients.
+ Bring down the leading coefficient \\(a_n\\) to the bottom row, where it becomes the leading coefficient of \\(Q(x)\\).
+ Multiply the value just written in the bottom row by \\(r\\), and add the result to the next coefficient in the top row. Write the sum in the bottom row.
+ Repeat the previous step for each coefficient, moving from left to right.
+ The last value in the bottom row is the remainder \\(R\\). The preceding values are the coefficients of \\(Q(x)\\), arranged in order of decreasing degree.

After \\(n\\) iterations the procedure stops, and you have both the quotient and the remainder. If \\(R = 0\\), then \\(P(x) = (x - r)\\, Q(x)\\), and you can apply the same procedure to \\(Q(x)\\) to find more roots.

> Synthetic division is equivalent to polynomial long division by \\((x - r)\\) but it works only on the coefficients and skips rewriting the variable at each step. However, the choice of \\(r\\) is not guaranteed to produce a factor: if \\(R \neq 0\\), then \\(r\\) is not a root of \\(P(x)\\), and \\((x - r)\\) is not a factor of the polynomial.

- - -

## Example

Let us examine a concrete example. Consider the polynomial:

\\[
P(x) = x^3 - 6x^2 + 11x - 6
\\]

We want to identify its rational roots using the rational root theorem. According to the theorem, any rational root must have the form:

\\[
r = \frac{p}{q}
\\]

where \\(p\\) divides the constant term \\(a_0 = -6\\) and \\(q\\) divides the leading coefficient \\(a_3 = 1\\). Since the only divisors of \\(1\\) are \\(\pm 1\\), the set of possible rational roots is:

\\[
r \in \\{\, \pm 1,\ \pm 2,\ \pm 3,\ \pm 6 \,\\}
\\]

To determine which of these candidates is an actual root, we evaluate \\(P(x)\\) at each value. Testing \\(x = 1\\):

\\[
\begin{align}
P(1) &= 1^3 - 6 \cdot 1^2 + 11 \cdot 1 - 6 \\\\[6pt]
     &= 1 - 6 + 11 - 6 \\\\[6pt]
     &= 0
\end{align}
\\]

Since \\(P(1) = 0\\), we conclude that \\(x = 1\\) is a root of the polynomial, and we can therefore apply synthetic division to divide \\(P(x)\\) by \\((x - 1)\\).

We begin by setting up the table. In the top row we insert the coefficients of \\(P(x)\\) in order of decreasing degree. If a coefficient of a certain degree were missing, we would write \\(0\\) in its place. To the left we place the value of the root, which is \\(1\\). The bottom row is initially empty and will be filled during the procedure.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &    &    &    \\\\[4pt]
\hline
  &   &    &    &
\end{array}
\\]

We bring down the leading coefficient unchanged, placing it as the first entry of the bottom row.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &    &    &    \\\\[4pt]
\hline
  & 1 &    &    &
\end{array}
\\]

Multiply the root by the value just written in the bottom row, and place the product in the middle row above the next coefficient.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &  1 &    &    \\\\[4pt]
\hline
  & 1 &    &    &
\end{array}
\\]

Sum the coefficient in the top row with the product in the middle row, and write the result in the bottom row.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &  1 &    &    \\\\[4pt]
\hline
  & 1 & -5 &    &
\end{array}
\\]

Multiply the root by the new value in the bottom row, and place the product above the next coefficient.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &  1 & -5 &    \\\\[4pt]
\hline
  & 1 & -5 &    &
\end{array}
\\]

Sum the coefficient with the product, and write the result in the bottom row.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &  1 & -5 &    \\\\[4pt]
\hline
  & 1 & -5 &  6 &
\end{array}
\\]

Repeat the multiplication for the last column.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &  1 & -5 &  6 \\\\[4pt]
\hline
  & 1 & -5 &  6 &
\end{array}
\\]

Finally, sum the last coefficient with the product to obtain the remainder.

\\[
\begin{array}{c|cccc}
  & 1 & -6 & 11 & -6 \\\\[4pt]
1 &   &  1 & -5 &  6 \\\\[4pt]
\hline
  & 1 & -5 &  6 &  0
\end{array}
\\]

The last entry of the bottom row is the remainder of the division, and in this case it is zero. This confirms that \\(x = 1\\) is a root of \\(P(x)\\) and that \\((x - 1)\\) is a factor of the polynomial. The preceding entries of the bottom row are the coefficients of the quotient \\(Q(x)\\), arranged in order of decreasing degree. Since the original polynomial has degree three, the quotient has degree two, and we obtain:

\\[
Q(x) = x^2 - 5x + 6
\\]

The polynomial can therefore be written as:

\\[
P(x) = (x - 1)(x^2 - 5x + 6)
\\]

The quadratic factor can be further decomposed by elementary techniques. The two numbers whose product is \\(6\\) and whose sum is \\(-5\\) are \\(-2\\) and \\(-3\\), so we can write:

\\[
x^2 - 5x + 6 = (x - 2)(x - 3)
\\]

Substituting this factorization into the previous expression, the polynomial \\(P(x)\\) admits the complete factorization \\(P(x) = (x - 1)(x - 2)(x - 3)\\), and its three roots are \\(1\\), \\(2\\) and \\(3\\).

> If the remainder is not zero, the value tested is not a root of the polynomial. In that case, the procedure must be repeated with a different candidate from the list provided by the rational root theorem.

- - -

## Limitations

In its usual form, the method applies to polynomials with real coefficients and linear divisors of the form \\((x - r)\\) where \\(r \in \mathbb{R}\\). It also has some limitations.

The first is that if the divisor has the form \\(x - (a + bi)\\), the method cannot be applied directly, because the procedure only handles real numbers and not complex ones.

The second limitation is that dividing by \\((x - r)\\) provides you with only one quotient and one remainder. Therefore, in order to completely factor a polynomial of degree \\(n\\), one must repeat the process multiple times. 

Advancing through the iterations requires knowing a valid root, which makes finding the roots impractical for high-degree polynomials.

> The rational root theorem makes the search easier for polynomials with integer coefficients, because it reduces it to a finite number of candidates. But it does not help when the remaining roots are irrational or complex.

- - -
## A practical case where the method cannot be applied

Suppose we want to divide the polynomial \\(P(x)\\) by the binomial \\(D(x)\\):

\\[
P(x) = x^3 - 3x^2 + 4x - 4
\\]
\\[
D(x) = x - (1 + i)
\\]

As mentioned earlier, synthetic division only works with polynomials that have real coefficients and divisors of the form \\(x - r\\) with \\(r \in \mathbb{R}\\). In this example the divisor has the form \\(x - r\\), but the value \\(r = 1 + i\\) is a [complex number](../complex-numbers-introduction/) rather than a real one, and for the reason explained above the synthetic division table cannot be used to carry out the division.

Consider now the case when \\(1 + i\\) is a root of the polynomial, evaluating \\(P(x)\\) at this value we obtain:

\\[
\begin{align}
P(1 + i) &= (1 + i)^3 - 3(1 + i)^2 + 4(1 + i) - 4 \\\\[6pt]
&= (-2 + 2i) - 6i + (4 + 4i) - 4 \\\\[6pt]
&= -2
\end{align}
\\]

The nonzero result demonstrates that \\(1 + i\\) is not a root of \\(P(x)\\). Although division by \\(x - (1 + i)\\) is a valid operation, standard synthetic division is not applicable. Instead, polynomial long division must be used, as it is a general method that imposes no restrictions on the type of coefficients.

> The roots of \\(P(x) = x^3 - 3x^2 + 4x - 4\\) are the real root \\(x = 2\\) and the complex conjugate pair \\(x = \frac{1 \pm i\sqrt{7}}{2}\\). The real root can be identified by inspection or by applying the rational root theorem. The remaining two roots are obtained from the quadratic factor that results after performing synthetic division with the real root.

- - -

## Computational insight

Why is synthetic division so useful in practice? It comes down to how it compares with the alternatives in terms of cost.

Synthetic division consists of a sequence of operations, each requiring a constant amount of work, and for this reason its complexity is linear, \\(O(n)\\), where \\(n\\) is the degree of the polynomial. The cost increases proportionally with the number of coefficients, making division by \\((x - r)\\) efficient even for polynomials of high degree.

Polynomial long division has a higher complexity of \\(O(n^2)\\). At each step you multiply and subtract polynomials of decreasing degree, and the total effort grows quadratically. Long division works with any kind of divisor, but when the divisor is linear, like \\((x - r)\\), synthetic division gives you the same result at a much lower cost.

Polynomial factorization is harder. For polynomials with [integer](../integers/) coefficients, no polynomial-time algorithm is currently known, and in practice the process combines several techniques, like testing candidate roots. In this case synthetic division plays a key role: once a root is found, it removes the corresponding factor and leaves a simpler polynomial.

The expressions \\(O(n)\\) and \\(O(n^2)\\) use [Big-O notation](../big-o-notation/), the standard way of describing how the number of operations of an algorithm scales with the size of the input.