
# Notable Products

Source: algebrica.org — CC BY-NC 4.0

## Introduction

Notable products are identities describing the expansion or [factorisation](../factoring-ac-method/) of [polynomials](../polynomials) such as [binomials](../binomials) or [trinomials](../trinomials). They allow rewriting such expressions in a simpler form, and this is often what makes polynomial factorisation tractable in practice or what allows us to actually solve an [equation](../equations/).

Consider for example the identity $(a+b)^2 = a^2 + 2ab + b^2$. A useful property is that, read from left to right, it gives us the expansion of the square, while read from right to left it gives us its factorisation.

Most of the identities collected here are special cases of the [binomial theorem](../binomial-theorem/), which gives the expansion of $(a+b)^n$ for arbitrary non-negative integer $n$. The square and the cube of a binomial are just the cases $n=2$ and $n=3$ of this general expansion. Other identities on this page, like the difference of two squares or the factorisation of $a^3 \pm b^3$, cannot be obtained from the binomial theorem, although the underlying mechanism is essentially the same.

- - -

## Square of a binomial

The square of a binomial is what we obtain when a binomial is multiplied by itself. There are two cases, depending on whether the two terms are added or subtracted:

$$
\begin{align}
(a+b)^2 &= a^2 + 2ab + b^2 \\[6pt]
(a-b)^2 &= a^2 - 2ab + b^2
\end{align}
$$

Working out the expansion of $(a+b)^2$, we obtain three terms:

$$
\begin{align}
(a+b)^2 &= (a+b)(a+b) \\[6pt]
&= a^2 + ab + ab + b^2 \\[6pt]
&= a^2 + 2ab + b^2
\end{align}
$$

Two of them are the squares of $a$ and $b$, and the third one is twice their product. The case $(a-b)^2$ is analogous, with the only difference that the middle term comes out negative, since multiplying $a$ by $-b$ introduces a minus sign.

- - -

## Difference of two squares

When we multiply a sum and a difference of the same two terms, the result is the difference of their squares:

$$
a^2 - b^2 = (a+b)(a-b)
$$

The product on the right-hand side expands as follows:

$$
\begin{align}
(a+b)(a-b) &= a(a-b) + b(a-b) \\[6pt]
&= a^2 - ab + ab - b^2 \\[6pt]
&= a^2 - b^2
\end{align}
$$

The terms $-ab$ and $+ab$ cancel out, so what is left is just $a^2 - b^2$.

- - -

## Cube of a binomial

When we multiply a binomial by itself three times, the result is one of the following two identities, depending on the sign between the two terms:

$$
\begin{align}
(a+b)^3 &= a^3 + 3a^2b + 3ab^2 + b^3 \\[6pt]
(a-b)^3 &= a^3 - 3a^2b + 3ab^2 - b^3
\end{align}
$$

Both are special cases of the [binomial theorem](../binomial-theorem/) with $n=3$.

---

Closely related to the cube of a binomial are the sum and difference of two cubes, which work the other way around: they take an expression of the form $a^3 \pm b^3$ and rewrite it as a product.

$$
\begin{align}
a^3 + b^3 &= (a+b)(a^2 - ab + b^2) \\[6pt]
a^3 - b^3 &= (a-b)(a^2 + ab + b^2)
\end{align}
$$

The first identity can be verified by expanding the right-hand side:

$$
\begin{align}
(a+b)(a^2-ab+b^2) &= a^3 - a^2b + ab^2 + a^2b - ab^2 + b^3 \\[6pt]
&= a^3 + b^3
\end{align}
$$

The same procedure works for $a^3 - b^3$:

$$
\begin{align}
(a-b)(a^2+ab+b^2) &= a^3 + a^2b + ab^2 - a^2b - ab^2 - b^3 \\[6pt]
&= a^3 - b^3
\end{align}
$$

In both cases the mixed terms cancel in pairs, and only the cubes $a^3$ and $\pm b^3$ survive.

> In the expansion of $(a+b+c)^3$, the coefficient $6$ in the term $6abc$ arises from the number of permutations of the three distinct factors $a$, $b$, $c$, that is $3!=6$. This is an instance of the multinomial theorem, which generalises the [binomial theorem](../binomial-theorem/) to sums of more than two terms.

- - -

## Notable products and the binomial theorem

The square and the cube of a binomial both come from a more general formula, the [binomial theorem](../binomial-theorem/), which expands $(a+b)^n$ for any non-negative integer $n$:

$$
(a+b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^{k}
$$

The coefficients $\binom{n}{k}$ are the [binomial coefficients](../binomial-coefficient/):

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

If we now want to use this general formula to recover the cube of a binomial, we just need to set $n=3$ and work out the four coefficients, which turn out to be $\binom{3}{0}=\binom{3}{3}=1$ and $\binom{3}{1}=\binom{3}{2}=3$. Substituting these numbers back into the formula, the expansion comes out as:

$$
(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3
$$

- - -

## Example 1

Consider the following equation:

$$x^3 - 27 = 0$$

Since $27 = 3^3$, the left-hand side is a difference of two cubes. Applying the identity $a^3 - b^3 = (a-b)(a^2+ab+b^2)$ with $a = x$ and $b = 3$, we factorise:

$$(x - 3)(x^2 + 3x + 9) = 0$$

The equation holds when either factor equals zero:

$$
\begin{cases}
x - 3 = 0 \\[0.5em]
x^2 + 3x + 9 = 0
\end{cases}
$$

The first case yields $x = 3$ directly. For the second case, the [quadratic formula](../quadratic-formula/) is applied:

$$
\begin{align}
x &= \frac{-3 \pm \sqrt{3^2 - 4(1)(9)}}{2(1)} \\
  &= \frac{-3 \pm \sqrt{9 - 36}}{2} \\
  &= \frac{-3 \pm \sqrt{-27}}{2}
\end{align}
$$

Because the discriminant $\Delta = -27 < 0$, the two remaining solutions are [complex](../quadratic-equations-with-complex-solutions/). Substituting $\sqrt{-27} = 3i\sqrt{3}$ gives:

$$x = \frac{-3 + 3i\sqrt{3}}{2} \qquad x = \frac{-3 - 3i\sqrt{3}}{2}$$

Therefore, by applying the expansion of the difference of two cubes, we were able to easily determine the solutions of the third-degree equation, which are:

$$
x = 3, \quad x = \frac{-3 + 3i\sqrt{3}}{2}, \quad x = \frac{-3 - 3i\sqrt{3}}{2}
$$

- - -

## Sum and difference of nth powers

The identities seen so far cover only the cases $n=2$ and $n=3$. For a generic $n$, the parity of the exponent decides whether $a^n+b^n$ and $a^n-b^n$ admit a factorisation.

The difference $a^n-b^n$ factorises for any positive integer $n$, with no parity restrictions, as:

$$
a^n-b^n = (a-b)(a^{n-1}+a^{n-2}b+a^{n-3}b^2+\cdots+ab^{n-2}+b^{n-1})
$$

For the sum $a^n+b^n$ when $n$ is odd, an analogous factorisation does exist, with alternating signs in the second factor:

$$
a^n+b^n = (a+b)(a^{n-1}-a^{n-2}b+a^{n-3}b^2-\cdots-ab^{n-2}+b^{n-1})
$$

When $n$ is even, on the other hand, no such factorisation is available over $\mathbb{R}$ in general. The expressions $a^2+b^2$ and $a^4+b^4$, for instance, are irreducible over the reals unless further structure is brought in.

> The factorisation of $a^n-b^n$ is closely related to the structure of the $n$-th roots of unity in the [complex plane](../complex-numbers-introduction/). The [roots](../roots-of-a-polynomial/) of $a^n-b^n=0$ are precisely $a/b=e^{2\pi i k/n}$ for $k=0,1,\dots,n-1$.

---

The case of even $n$ admits one exception, known as Sophie Germain's identity, which has some consequences in showing that certain integers of the form $n^4+4m^4$ admit a non-trivial factorisation and are therefore not prime. The identity is:

$$
a^4+4b^4 = (a^2+2b^2+2ab)(a^2+2b^2-2ab)
$$

At first sight this might seem like a contradiction, since we have just said that sums of even powers do not generally factorise over $\mathbb{R}$. In this case the coefficient $4$ makes it possible to complete the square and obtain:

$$
a^4+4b^4 = (a^2+2b^2)^2-(2ab)^2
$$

In this way the expression is a difference of two squares, and the factorisation follows from the standard identity.

> The identities for $a^n \pm b^n$ are related to Newton's identities, which express power sums $p_k=a^k+b^k$ in terms of the elementary symmetric polynomials $e_1=a+b$ and $e_2=ab$.

- - -

## Example 2

Let's consider the following expression:

$$a^4 + b^4$$

Since $n = 4$ is even, $a^4 + b^4$ does not factorise over $\mathbb{R}$ using the sum of nth powers formula, which applies only for odd $n$.

However, it admits the following factorisation:

$$a^4 + b^4 = (a^2 + \sqrt{2}\,ab + b^2)(a^2 - \sqrt{2}\,ab + b^2)$$ 

The factorisation can be verified by expanding the right-hand side:

$$
\begin{align}
(a^2 + \sqrt{2}\,ab + b^2)(a^2 - \sqrt{2}\,ab + b^2) &= (a^2 + b^2)^2 - (\sqrt{2}\,ab)^2 \\
&= a^4 + 2a^2b^2 + b^4 - 2a^2b^2 \\
&= a^4 + b^4
\end{align}
$$

- - -

## List of the main notable products

| | |
|---|---|
| $(a + b)^2$ | $a^2 + 2ab + b^2$ |
| $(a - b)^2$ | $a^2 - 2ab + b^2$ |
| $a^2 - b^2$ | $(a + b)(a - b)$ |
| $(a + b)^3$ | $a^3 + 3a^2b + 3ab^2 + b^3$ |
| $(a - b)^3$ | $a^3 - 3a^2b + 3ab^2 - b^3$ |
| $a^3 + b^3$ | $(a + b)(a^2 - ab + b^2)$ |
| $a^3 - b^3$ | $(a - b)(a^2 + ab + b^2)$ |
| $a^n + b^n \quad (n \text{ odd})$ | $(a + b)(a^{n-1} - a^{n-2}b + \cdots + b^{n-1})$ |
| $a^n - b^n$ | $(a - b)(a^{n-1} + a^{n-2}b + \cdots + b^{n-1})$ |
| $a^{2n} - b^{2n}$ | $(a^n - b^n)(a^n + b^n)$ |
| $a^4 - b^4$ | $(a - b)(a + b)(a^2 + b^2)$ |
| $a^4 + b^4$ | $(a^2 + \sqrt{2}\,ab + b^2)(a^2 - \sqrt{2}\,ab + b^2)$ |
| $(a + b + c)^2$ | $a^2 + b^2 + c^2 + 2(ab + ac + bc)$ |
| $(a + b + c)^3$ | $a^3 + b^3 + c^3 + 3(a^2b + a^2c + b^2a + b^2c + c^2a + c^2b) + 6abc$ |