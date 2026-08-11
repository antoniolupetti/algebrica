---
title: Taylor's Formula with Remainder
source: https://algebrica.org/taylor-formula-with-remainder/
license: CC BY-NC 4.0
tags:
  - higher-order-derivatives
  - lagrange-remainder
  - local-approximation
  - peano-remainder
  - taylor-polynomial
---
## From the tangent line to polynomials of higher degree

A function differentiable at a point has a polynomial approximation of degree at most one whose error is negligible compared with the increment of the variable. Rearranging the definition of [derivative](../derivatives/) at $x_0$ gives:

$$f(x) = f(x_0) + f'(x_0)(x - x_0) + o(x - x_0)$$ 
$$ x \to x_0$$

The approximating expression $f(x_0) + f'(x_0)(x-x_0)$ is a polynomial of degree at most one whose graph is the tangent line at $x_0,$ discussed in the entry on the [differential of a function](../differential-of-a-function/). Its evaluation requires only sums and products. Its error is local because the [little-o](../little-o-notation/) symbol describes a limit at $x_0,$ not a bound on an interval.

To obtain a higher-order approximation, we must choose its coefficients. A polynomial of degree at most $n$ written in powers of $x - x_0$ has $n+1$ coefficients, so $n+1$ conditions determine it. For degree one, the value and the first derivative agree with those of the function at $x_0.$ For degree at most $n,$ we require the [derivatives of every order](../higher-order-derivatives/) up to $n$ to agree there.

Let $p$ be such a polynomial, written as:

$$p(x) = \sum_{k=0}^{n} c_k (x - x_0)^k$$

Differentiating $j$ times, with $0 \leq j \leq n,$ annihilates the terms with $k < j$ and lowers the exponent of the others:

$$p^{(j)}(x) = \sum_{k=j}^{n} \frac{k!}{(k-j)!} c_k (x - x_0)^{k-j}$$

At $x = x_0$ every term with $k > j$ vanishes, since it retains a positive power of $x - x_0,$ and only the term with $k = j$ survives:

$$p^{(j)}(x_0) = j! c_j$$

Imposing $p^{(j)}(x_0) = f^{(j)}(x_0)$ for $j = 0, 1, \dots, n$ therefore determines each coefficient, and the choice is unique:

$$c_j = \frac{f^{(j)}(x_0)}{j!}$$

## The Taylor polynomial

Let $f$ be $n$ times differentiable at $x_0.$ The Taylor polynomial of $f$ of order $n$ centred at $x_0$ is:

$$T_n(x) = \sum_{k=0}^{n} \frac{f^{(k)}(x_0)}{k!} (x - x_0)^k = f(x_0) + f'(x_0)(x-x_0) + \frac{f''(x_0)}{2!}(x-x_0)^2 + \cdots + \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$$

When the centre is the origin the polynomial is called the Maclaurin polynomial of $f.$ By construction $T_n$ has the same value and the same derivatives as $f$ up to order $n$ at the centre, and it is the only polynomial of degree at most $n$ with this property.

The order $n$ and the degree of $T_n$ need not coincide, because the leading coefficient may vanish. For $f(x) = \cos x$ centred at the origin we have $f'''(0) = 0,$ so $T_3$ and $T_2$ are the same polynomial $1 - x^2/2$ of degree two. Thus this degree-two polynomial has the error estimate for order three.

If $f$ is itself a [polynomial](../polynomials/) of degree $m,$ then $T_n = f$ for every $n \geq m,$ because all derivatives of order greater than $m$ vanish identically and the coefficients reproduce those of $f.$

The difference between the function and its Taylor polynomial is the remainder of order $n:$

$$R_n(x) = f(x) - T_n(x)$$

Written as $f(x) = T_n(x) + R_n(x),$ the equality is an identity that defines $R_n.$ Taylor's formula consists of this identity together with a description of the remainder. The Peano form describes its limiting behaviour at the centre and requires fewer hypotheses. In the Lagrange form, the remainder has an expression that can be bounded on an interval, and the formula requires one more derivative.

## Peano form of the remainder

Let $f$ be defined on a neighborhood of $x_0$ and $n$ times differentiable at $x_0.$ Then:

$$\lim_{x \to x_0} \frac{f(x) - T_n(x)}{(x - x_0)^n} = 0$$

Equivalently, in the language of Landau symbols:

$$f(x) = T_n(x) + o\left((x-x_0)^n\right) \qquad x \to x_0$$

The statement says that the error divided by the $n$-th power of the increment tends to zero. Thus $T_n$ is a local approximation of order $n.$

For the proof, observe first that $R_n^{(j)}(x_0) = 0$ for every $j = 0, 1, \dots, n,$ since $T_n$ matches $f$ up to order $n$ at the centre. The existence of $f^{(n)}(x_0)$ means that $f^{(n-1)}$ is defined on a neighborhood of $x_0.$ Hence $R_n$ is $n-1$ times differentiable there, and both $R_n$ and $(x-x_0)^n$ vanish at $x_0$ together with their derivatives up to order $n-1.$ Applying [de l'Hôpital's rule](../hopital-rule/) $n-1$ times gives:

$$
\begin{align}
\lim_{x \to x_0} \frac{R_n(x)}{(x-x_0)^n} &= \lim_{x \to x_0} \frac{R_n'(x)}{n(x-x_0)^{n-1}} \\[6pt]
&= \cdots \\[6pt]
&= \lim_{x \to x_0} \frac{R_n^{(n-1)}(x)}{n!(x - x_0)}
\end{align}
$$

A further application of the rule to the last limit would be invalid because $R_n^{(n)}$ is known to exist only at $x_0.$ Instead, the definition of derivative at the centre and the equality $R_n^{(n-1)}(x_0) = 0$ give:

$$\lim_{x \to x_0} \frac{R_n^{(n-1)}(x)}{n!(x-x_0)} = \frac{1}{n!} \lim_{x \to x_0} \frac{R_n^{(n-1)}(x) - R_n^{(n-1)}(x_0)}{x - x_0} = \frac{R_n^{(n)}(x_0)}{n!} = 0$$

Since $R_n^{(n)}(x_0) = f^{(n)}(x_0) - T_n^{(n)}(x_0) = 0,$ the chain of equalities proves the claim.

> The Peano form does not bound the error at a specified point. It compares the error with $(x-x_0)^n$ in the limit, so it provides no bound on an interval.

## Uniqueness of the expansion

The Taylor polynomial is the only polynomial of degree at most $n$ that approximates $f$ to order $n$ at $x_0.$ Suppose $p$ has degree at most $n$ and satisfies:

$$f(x) = p(x) + o\left((x-x_0)^n\right) \qquad x \to x_0$$

Subtracting this from the Peano formula shows that the polynomial $q = p - T_n$ satisfies $q(x) = o((x-x_0)^n).$ Assume $q$ is not identically zero and write $q(x) = \sum_{k=0}^{n} b_k (x-x_0)^k,$ letting $m$ be the smallest index with $b_m \neq 0.$ Dividing by $(x-x_0)^m$ and passing to the limit gives $b_m$ on one side, while on the other side:

$$\frac{q(x)}{(x-x_0)^m} = (x - x_0)^{n-m} \frac{q(x)}{(x-x_0)^n} \longrightarrow 0$$

because $n - m \geq 0$ and the second factor tends to zero. This forces $b_m = 0,$ against the choice of $m,$ so $q$ vanishes identically and $p = T_n.$

Consequently, an expansion obtained by substitution, multiplication, or addition of known expansions is the Taylor expansion whenever those operations preserve the stated remainder order. Direct computation of the derivatives is then unnecessary.

## Lagrange form of the remainder

Let $f$ have derivatives through order $n+1$ on the open [interval](../intervals/) with endpoints $x_0$ and $x,$ and suppose that $f^{(n)}$ is [continuous](../continuous-functions/) on the corresponding closed interval. Then there exists a point $\xi$ strictly between $x_0$ and $x$ such that:

$$R_n(x) = \frac{f^{(n+1)}(\xi)}{(n+1)!} (x - x_0)^{n+1}$$

The formula generalises [Lagrange's mean value theorem](../lagrange-theorem/), which is the case $n = 0$ and reads $f(x) - f(x_0) = f'(\xi)(x-x_0).$ The remainder has the form of the next term of the Taylor polynomial, but the derivative is evaluated at an unspecified intermediate point rather than at the centre.

Suppose $x > x_0.$ If $x < x_0,$ the proof is the same after exchanging the endpoints. On $[x_0, x]$ define the auxiliary functions:

$$F(t) = f(x) - \sum_{k=0}^{n} \frac{f^{(k)}(t)}{k!} (x - t)^k$$
$$G(t) = (x-t)^{n+1}$$

The variable of differentiation is the centre $t$ of the expansion, while $x$ is held fixed. At the endpoints we have $F(x) = 0$ and $F(x_0) = f(x) - T_n(x) = R_n(x),$ together with $G(x) = 0$ and $G(x_0) = (x-x_0)^{n+1}.$

Differentiating a single summand of $F$ with respect to $t$ for $k \geq 1$ gives two contributions:

$$\frac{d}{dt}\left[\frac{f^{(k)}(t)}{k!}(x-t)^k\right] = \frac{f^{(k+1)}(t)}{k!}(x-t)^k - \frac{f^{(k)}(t)}{(k-1)!}(x-t)^{k-1}$$

The second contribution cancels the first contribution of the preceding summand. The derivative of the term with $k = 0$ is $f'(t),$ which is cancelled in the same way. The sum telescopes and only the last positive contribution remains:

$$F'(t) = -\frac{f^{(n+1)}(t)}{n!}(x-t)^n$$

The derivative of $G$ is $G'(t) = -(n+1)(x-t)^n,$ which does not vanish on the open interval $(x_0, x).$ The hypotheses of [Cauchy's mean value theorem](../cauchy-theorem/) are met, so there exists $\xi \in (x_0, x)$ with:

$$\frac{F(x) - F(x_0)}{G(x) - G(x_0)} = \frac{F'(\xi)}{G'(\xi)}$$

The two differences on the left are the opposites of $R_n(x)$ and of $(x-x_0)^{n+1},$ so the left-hand side equals $R_n(x)/(x-x_0)^{n+1}.$ On the right-hand side the factor $(x-\xi)^n$ is common to $F'(\xi)$ and $G'(\xi)$ and is different from zero, so it simplifies:

$$\frac{R_n(x)}{(x-x_0)^{n+1}} = \frac{f^{(n+1)}(\xi)}{(n+1)!}$$

Multiplying by $(x-x_0)^{n+1}$ gives the stated expression.

> The point $\xi$ depends on $x,$ on $n$ and on the function, and no general procedure determines it. Bounds on $f^{(n+1)}$ are sufficient, so the value of $\xi$ need not be found.

## Estimating the error

Suppose $f$ has $n+1$ derivatives on an interval $I$ containing $x_0$ and that a constant $M$ bounds the derivative of order $n+1$ on $I:$

$$\left|f^{(n+1)}(t)\right| \leq M \qquad t \in I$$

If $x \in I,$ then $\xi \in I.$ Taking absolute values in the Lagrange form therefore gives a bound without the intermediate point:

$$|R_n(x)| \leq \frac{M}{(n+1)!} |x - x_0|^{n+1} \qquad x \in I$$

The inequality relates the order $n,$ the distance from the centre and the error tolerance. A prescribed order and interval give a bound for the error. A prescribed interval and tolerance determine a sufficient order. A prescribed order and tolerance determine an interval on which the error has the required bound.

## Example 1

We approximate $\ln(1.2)$ by the Maclaurin polynomial of order three of $f(x) = \ln(1+x),$ evaluated at $x = 0.2,$ and we bound the error. Successive differentiation gives:

$$
\begin{align}
f'(x) &= \frac{1}{1+x} \\[6pt]
f''(x) &= -\frac{1}{(1+x)^2} \\[6pt]
f'''(x) &= \frac{2}{(1+x)^3} \\[6pt]
f^{(4)}(x) &= -\frac{6}{(1+x)^4}
\end{align}
$$

Evaluating the first three at the origin yields the polynomial:

$$T_3(x) = x - \frac{x^2}{2} + \frac{x^3}{3}$$

At $x = 0.2$ this gives $T_3(0.2) = 0.2 - 0.02 + 0.002666\dots = 0.182666\dots$ The fourth derivative is decreasing in absolute value on $[0, 0.2],$ so its largest absolute value is attained at the left endpoint and equals $6.$ The estimate with $n = 3$ and $M = 6$ reads:

$$|R_3(0.2)| \leq \frac{6}{4!} (0.2)^4 = \frac{1}{4} \cdot 0.0016 = 0.0004$$

The bound shows that the error is at most four ten-thousandths without using the true value. Since $\ln(1.2) = 0.182321\dots,$ the actual error is $0.000345,$ below the bound and of the same order of magnitude.

## Example 2

We ask how many terms of the Maclaurin expansion of $e^x$ guarantee an error below $10^{-6}$ for every $x$ in $[-1, 1].$ Every derivative of the [exponential function](../exponential-function/) is the function itself, whose largest value on the interval is $e.$ Since $e < 3,$ we may take $M = 3,$ and the estimate becomes:

$$|R_n(x)| \leq \frac{3}{(n+1)!} |x|^{n+1} \leq \frac{3}{(n+1)!} \qquad |x| \leq 1$$

The requirement is thus $(n+1)! > 3 \cdot 10^6.$ The relevant [factorials](../factorial/) are $9! = 362880$ and $10! = 3628800,$ so the smallest admissible value is $n + 1 = 10.$ The polynomial of order nine gives:

$$\left|e^x - \sum_{k=0}^{9} \frac{x^k}{k!}\right| \leq \frac{3}{10!} < 8.3 \cdot 10^{-7}$$

Order eight would leave a possible error of about $8.3 \cdot 10^{-6},$ ten times the tolerance, so nine terms beyond the constant are the minimum the estimate allows.

## Example 3

Fix the order and the tolerance. We seek the neighborhood of the origin on which the polynomial $1 - x^2/2$ approximates $\cos x$ with an error not exceeding $10^{-3}.$

The polynomial is $T_2$ of the cosine, but it is also $T_3,$ because the third derivative of the cosine vanishes at the origin. The estimate may therefore be applied with $n = 3,$ and since every derivative of the cosine is bounded by $1$ in absolute value we may take $M = 1:$

$$|R_3(x)| \leq \frac{|x|^4}{4!} = \frac{|x|^4}{24}$$

Imposing the tolerance gives $|x|^4 \leq 0.024,$ hence $|x| \leq 0.393.$ The same polynomial treated as $T_2$ would give the weaker bound $|x|^3/6 \leq 10^{-3},$ satisfied only for $|x| \leq 0.181.$ Using order three rather than order two increases the certified radius from $0.181$ to $0.393$ without changing the polynomial.

## Expansions of the elementary functions

The expansions below are centred at the origin and written with the Peano remainder as $x \to 0.$ Each follows from the general formula after the derivatives at the origin have been computed.

Every derivative of the [exponential function](../exponential-function/) is the exponential function, so all its Maclaurin coefficients are $1/k!:$

$$e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots + \frac{x^n}{n!} + o(x^n)$$

The derivatives of the [sine](../sine-function/) and of the [cosine](../cosine-function/) repeat with period four, and the [parity](../even-and-odd-functions/) of the two functions leaves only odd or only even powers:

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots + (-1)^n \frac{x^{2n+1}}{(2n+1)!} + o(x^{2n+2})$$

$$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots + (-1)^n \frac{x^{2n}}{(2n)!} + o(x^{2n+1})$$

In both cases the remainder has an exponent one unit higher than the last written power, because the first omitted term is two units higher. The [hyperbolic sine](../hyperbolic-sine-function/) and [hyperbolic cosine](../hyperbolic-sine-and-cosine/) obey the same pattern without the alternation of signs:

$$\sinh x = x + \frac{x^3}{3!} + \frac{x^5}{5!} + \cdots + \frac{x^{2n+1}}{(2n+1)!} + o(x^{2n+2})$$

$$\cosh x = 1 + \frac{x^2}{2!} + \frac{x^4}{4!} + \cdots + \frac{x^{2n}}{(2n)!} + o(x^{2n+1})$$

The [logarithm](../logarithmic-function/) is not defined at the origin and is expanded after the shift $x \mapsto 1 + x,$ which places the singular point at $x = -1:$

$$\ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots + (-1)^{n-1} \frac{x^n}{n} + o(x^n)$$

The generalised [binomial coefficients](../binomial-coefficient/) are the coefficients in the expansion of the [power function](../power-function/) $t^\alpha$ about $t = 1.$ With $t = 1+x,$ this expansion is

$$(1+x)^{\alpha} = 1 + \alpha x + \binom{\alpha}{2} x^2 + \cdots + \binom{\alpha}{n} x^n + o(x^n)$$

The choice $\alpha = -1$ with $-x$ in place of $x,$ or the sum of a finite [geometric progression](../geometric-series/), gives the expansion whose coefficients are all equal to one:

$$\frac{1}{1-x} = 1 + x + x^2 + \cdots + x^n + o(x^n)$$

The corresponding expansions for the [arctangent](../arctangent-and-arccotangent/) and the [tangent](../tangent-function/) are:

$$\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \cdots + (-1)^n \frac{x^{2n+1}}{2n+1} + o(x^{2n+2})$$

$$\tan x = x + \frac{x^3}{3} + \frac{2x^5}{15} + o(x^6)$$

- - -

Uniqueness allows these formulas to be combined. To expand the [composite function](../composite-functions/) $e^{-x^2}$ to order six it is enough to substitute $t = -x^2$ into the expansion of $e^t$ stopped at order three, since $t \to 0$ as $x \to 0$ and $o(t^3)$ becomes $o(x^6):$

$$e^{-x^2} = 1 - x^2 + \frac{x^4}{2} - \frac{x^6}{6} + o(x^6)$$

Computing the sixth derivative of $e^{-x^2}$ directly requires repeated applications of the [product rule](../differentiation-rules/) and gives the same coefficients.

## Computing limits

Replacing the terms of an [indeterminate form](../indeterminate-forms/) by their expansions identifies the lowest power that does not cancel. The choice of the required order and the algebra of the remainders are developed in [asymptotic expansion](../asymptotic-expansion/). Consider the limit:

$$\lim_{x \to 0} \frac{e^{x^2} - \cos x - \dfrac{3}{2}x^2}{x^4}$$

The denominator has degree four, so both functions in the numerator must be expanded to order four. Substituting $t = x^2$ in the expansion of $e^t$ stopped at order two gives the exponential term. The expansion of the cosine gives the other term:

$$
\begin{align}
e^{x^2} &= 1 + x^2 + \frac{x^4}{2} + o(x^4) \\[6pt]
\cos x &= 1 - \frac{x^2}{2} + \frac{x^4}{24} + o(x^4)
\end{align}
$$

After subtraction, the constant terms cancel. The quadratic terms combine into $\frac{3}{2}x^2$ and cancel with the last term in the numerator:

$$e^{x^2} - \cos x - \frac{3}{2}x^2 = \left(\frac{1}{2} - \frac{1}{24}\right) x^4 + o(x^4) = \frac{11}{24} x^4 + o(x^4)$$

After division by $x^4,$ the little-o term tends to zero, so the [algebra of limits](../algebra-of-limits/) gives the value $11/24.$ Four successive applications of l'Hôpital's rule give the same value after four differentiations of the numerator.

> If the expansion stops before the first term that does not cancel, the little-o remainder contains insufficient information to compute the limit. Expanding one order further resolves the indeterminacy.

## Stationary points and derivatives of higher order

The [second derivative test](../higher-order-derivatives/) classifies a [stationary point](../maximum-minimum-and-inflection-points/) $x_0$ when $f''(x_0) \neq 0.$ When $f''(x_0) = 0,$ the first derivative of higher order that does not vanish can determine the classification through the Peano form.

Let $f$ be $n$ times differentiable at $x_0$ with $n \geq 2,$ and suppose that all derivatives from the first to the one of order $n-1$ vanish at $x_0,$ while the one of order $n$ does not:

$$f'(x_0) = f''(x_0) = \cdots = f^{(n-1)}(x_0) = 0 \qquad f^{(n)}(x_0) \neq 0$$

All terms of the Taylor polynomial with order between one and $n-1$ vanish, so the expansion is:

$$f(x) - f(x_0) = \frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + o\left((x-x_0)^n\right)$$

Dividing by $(x-x_0)^n$ gives a quotient whose limit is the nonzero number $f^{(n)}(x_0)/n!.$ By [sign permanence](../theorems-on-limits/), the quotient has the sign of $f^{(n)}(x_0)$ on a punctured neighborhood of $x_0.$ The parity of $n$ then determines whether $x_0$ is an extremum:

+ If $n$ is even, $(x-x_0)^n > 0$ for $x \neq x_0,$ so $f(x) - f(x_0)$ has the sign of $f^{(n)}(x_0)$ throughout the neighborhood. The point is a strict local minimum when $f^{(n)}(x_0) > 0$ and a strict local maximum when $f^{(n)}(x_0) < 0.$
+ If $n$ is odd, $(x-x_0)^n$ changes sign at $x_0,$ so $f(x) - f(x_0)$ takes values of both signs in every neighborhood and $x_0$ is not an extremum.

The case $n = 2$ is the second derivative test. If $n$ is odd, the point is a horizontal inflection point. Indeed, the derivatives of $f'$ vanish at $x_0$ up to order $n-2,$ while the derivative of order $n-1$ is the nonzero number $f^{(n)}(x_0).$ Since $n-1$ is even, $x_0$ is a strict extremum of $f'.$ The derivative has the same sign on both sides of $x_0$ and vanishes at $x_0,$ so $x_0$ is a stationary point of inflection.

## Example 4

The function below has a single stationary point at the origin, where the second derivative test fails:

$$f(x) = \cos x - 1 + \frac{x^2}{2}$$

The first four derivatives are:

$$
\begin{align}
f'(x) &= x - \sin x \\[6pt]
f''(x) &= 1 - \cos x \\[6pt]
f'''(x) &= \sin x \\[6pt]
f^{(4)}(x) &= \cos x
\end{align}
$$

The first three vanish at the origin, while $f^{(4)}(0) = 1.$ The first surviving derivative has even order $n = 4$ and positive value, so the origin is a strict local minimum. The expansion of the cosine gives the same conclusion because the quadratic terms cancel:

$$f(x) = \frac{x^4}{24} + o(x^5)$$

For a stationary point of odd order consider instead:

$$g(x) = x^3 - 3x^2 + 3x$$

Its derivative is $g'(x) = 3(x-1)^2,$ which vanishes only at $x = 1.$ The second derivative $g''(x) = 6x - 6$ also vanishes there, and the third derivative is the constant $6.$ The first surviving derivative has odd order $n = 3,$ so $x = 1$ is not an extremum but a horizontal inflection point, in agreement with the sign of $g',$ which is positive on both sides.

> The criterion gives no conclusion when every derivative vanishes at the point. The function equal to $e^{-1/x^2}$ for $x \neq 0$ and to $0$ at the origin has all derivatives equal to zero there, yet the origin is a strict local minimum. In such cases one must instead examine the sign of $f'$ around the point.

## Choosing between the two forms

The two versions of Taylor's formula answer different questions and have different hypotheses. The Peano form requires $n$ derivatives at the single point $x_0$ and describes the error through a limit, so it applies to limits, comparisons of infinitesimals and classifications of stationary points. The Lagrange form requires $n+1$ derivatives on an interval and has an expression that can be bounded there, so it provides numerical error estimates.

The convergence of the [sequence of functions](../sequence-of-functions/) $(T_n)$ to $f$ as $n \to \infty$ is a separate question in the theory of [Taylor series](../taylor-series/). For some functions of class $C^{\infty},$ the sequence does not converge to the function. The estimates in this entry concern a fixed order and a shrinking neighborhood, and their hypotheses do not imply convergence as $n \to \infty.$
