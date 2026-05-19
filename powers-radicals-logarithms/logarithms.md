# Logarithms

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/logarithms/

## Definition

If \\(a\\) and \\(b\\) are positive [real numbers](../../properties-of-real-numbers/), where \\(a \neq 1\\), the logarithm of \\(b\\) to the base \\(a\\), denoted as \\(\log_a(b)\\), is defined as the real number \\(c\\) such that \\(a^c = b\\).

\\[\log_a{b} = c \iff a^c = b \\]

The following conditions must be satisfied:

\\[a>0 \quad a \neq 1 \quad b > 0 \\]

In simpler terms, the logarithm of a number refers to the exponent to which a specified base must be raised to obtain that number. Therefore, the logarithm is the inverse operation of [exponentiation](../exponential-function).

+ \\(a\\) is the base of the logarithm.
+ \\(b\\) is the argument.

> To clarify the concept, let's consider a simple example: \\(\log{_2}8 = 3 \to 2^3 =8\\).

- - -

The condition \\( a \neq 1 \\) is essential. In fact, when \\( a = 1 \\), the exponential expression \\( a^x \\) becomes \\( 1^x = 1 \quad \forall \\, x \in \mathbb{R} \\) In this case, the exponential function is constant and therefore not [invertible](../inverse-function/). Since the logarithm is defined as the inverse operation of exponentiation, it cannot be defined when the base is equal to \\(1\\). For this reason, the base of a logarithm must satisfy \\( a > 0 \\) and \\( a \neq 1 \\).

- - -
## Basic identities

Understanding logarithms requires a review of the concept of [powers](../powers), as these two mathematical ideas are closely related. The following identities arise directly from the principle that logarithms are the inverse operation of exponentiation:

\\[a^0 = 1 \to \log{_a}1 = 0 \\]
\\[a^1 = a \to \log{_a}a = 1 \\]

Since the exponential is always positive, it is not possible to determine the logarithm of a negative number. In formal terms, \\(\nexists\\) a number \\(c \in \mathbb{R}\\) such that \\(a^c < 0\\).

+ Logarithms with base \\(e\\), known as natural or Napierian logarithms, are typically denoted as \\( \ln a \\) without specifying the base, where \\(e \approx 2.71828\\) is [Euler's number](../euler-number-limit-sequence//), the base of the natural exponential function \\(e^x\\).

+ Logarithms with the base of the number \\(10\\), known as common logarithms, are typically denoted as \\( \text{Log} a \\) without specifying the base.

> The base-10 logarithm is especially useful when dealing with very large or very small numbers. It helps reduce the scale, making the values easier to interpret and compare. That’s why it’s commonly used in scientific and technical fields, often represented on logarithmic scales.

- - -
## Logarithmic function

As previously introduced, the [logarithmic function](../logarithmic-function) is the [inverse](../inverse-function/) of the exponential function. Consequently, its [domain](../determining-the-domain-of-a-function/) and range are inverted compared to the exponential function. A logarithmic function is typically expressed in the following form:

\\[
\log_a : (0,+\infty) \to \mathbb{R}, \quad a > 0,\\; a \neq 1
\\]

The domain is \\(x \in \mathbb{R}^+ \\) and the range is \\(\mathbb{R}\\). The function is [continuous](../continuous-functions/) and [differentiable](../derivatives/) on \\( (0,+\infty) \\).

- - -

The graph above illustrates the monotonic behaviour and asymptotic properties of the logarithmic function. For values of \\( a > 1 \\), the function \\(f(x) = \log_a x\\) is strictly increasing on \\( (0,+\infty) \\). It has a vertical [asymptote](../asymptotes/) at \\( x = 0 \\), and its limits are:

\\[
\begin{aligned}
\lim_{x \to 0^+} \log_a x &= -\infty \\\\[8pt]
\lim_{x \to +\infty} \log_a x &= +\infty
\end{aligned}
\\]

- - -

For \\( 0 < a < 1 \\), the function is strictly decreasing on \\( (0,+\infty) \\). The line \\( x = 0 \\) is again a vertical asymptote, but the limiting behaviour is reversed:

\\[
\begin{aligned}
\lim_{x \to 0^+} \log_a x &= +\infty \\\\[8pt]
\lim_{x \to +\infty} \log_a x &= -\infty
\end{aligned}
\\]

> The logarithmic function is utilised across various disciplines, for example in computer science, where it is fundamental to the analysis of algorithmic complexity. For example, algorithms such as [binary search](../logarithmic-function) exhibit logarithmic time complexity, indicating that their performance remains efficient as input sizes increase. This characteristic demonstrates how logarithmic growth enables concise and effective representations of exponential processes.

- - -
## Properties of logarithms

Logarithms have properties that facilitate the manipulation of mathematical expressions and [equations](../equations). These properties are fundamentally linked to those of exponential functions as each logarithmic identity directly results from a corresponding law of exponents.

Because the logarithm is defined as the inverse of the exponential function, the following identities are valid:

\\[
a^{\log_a x} = x \qquad \forall x \in (0,+\infty)
\\]

\\[
\log_a(a^x) = x \qquad \forall x \in \mathbb{R}
\\]

- - -

The product rule states that the logarithm of a product of two numbers is equal to the sum of their logarithms in the same base: \\[\log_a(xy) = \log_ax + \log_ay \\]

- - -

The quotient rule states that the logarithm of a quotient of two numbers is equal to the difference of the numerator and the denominator: \\[ \log_a{\frac{x}{y}} = \log_ax-\log_ay  \\] From the previous expression, if the numerator \\(x\\) is equal to \\(1\\), we obtain: \\[ \log_a{\frac{1}{y}} = -\log_ay \\] This means that the logarithm of the reciprocal of a number \\(\frac{1}{y}\\) is the opposite of its logarithm, and this is called the co-logarithm, indicated as: \\[\text{colog}_a{y} = -log_a{y} = \log_a{\frac{1}{y}}\\]

- - -

The property of the logarithm of a power states that the logarithm of a [power](../powers) of a number is equal to the product of the exponent and the logarithm of the base number: \\[ \log{_a}x^n = n \cdot \log{_a}x \\] This property directly follows from the properties of exponentials, as an expression like \\( x^n \\) can be understood as the result of multiplying \\( x \\) by itself \\( n \\) times.

- - -

From the previous property and the property of [radicals](../radicals), it follows that the logarithm of a radical is equal to the quotient between the logarithm of the radicand and the index of the root: \\[\log_a\sqrt[n]{b} = \frac{1}{n}\log_ab \\]

- - -
## Fundamental inequality for the natural logarithm

A key inequality involving the natural logarithm \\(\ln\\)is given by:

\\[
\ln x \le x - 1 \qquad \forall x > 0
\\]

This equality holds if and only if \\( x = 1 \\). This result follows directly from the concavity of the function \\( \ln x \\) on the interval \\( (0,+\infty) \\). Since the second derivative satisfies:

\\[
(\ln x)^{\prime\prime} = -\frac{1}{x^2} < 0 \qquad \forall x > 0
\\]

The graph of the logarithm always lies below each of its tangent lines. In particular, consider the tangent at \\( x = 1 \\), where:

\\[
\ln 1 = 0 \quad \text{and} \quad (\ln x)’ \big|_{x=1} = 1
\\]

The equation of the tangent line is:

\\[
y = x - 1
\\]

Therefore, the inequality expresses the geometric fact that the curve \\( y = \ln x \\) does not rise above its tangent at \\( x = 1 \\).

- - -
## The role of logarithms in algebraic structure

The logarithm acts as a structural bridge between two distinct algebraic systems. Within the set of positive real numbers \\((0,+\infty)\\), multiplication is the primary operation, while addition serves this role in \\(\mathbb{R}\\). The logarithm connects these systems by transforming multiplicative relationships into additive relationships. For example, consider the following product:

\\[
x^3 y^2
\\]

Taking logarithms gives:

\\[
\log_a(x^3 y^2) = 3\log_a x + 2\log_a y
\\]

This process converts the multiplicative structure, characterised by products and powers, into an additive structure, characterised by sums and scalar multiples. In this context, the logarithm functions as a homomorphism from the multiplicative group \\((0,+\infty)\\) to the additive group \\(\mathbb{R}\\), preserving the underlying structure while altering the operation. The standard logarithmic rules provide exact algebraic formulations of this transformation.

> A homomorphism is a function between two algebraic structures that preserves the operation, meaning \\(\varphi(x \star y) = \varphi(x) \circ \varphi(y)\\). Here \\( \star \\) and \\( \circ \\) denote the operations of the two algebraic structures, such as addition or multiplication.

- - -
## Example 1

Let's simplify the following logarithmic expression using the properties of logarithms:  

\\[
\log_a \left( \frac{x^3 \cdot y}{z^2} \right)
\\]

First, we apply the quotient rule, which states that the logarithm of a quotient is the difference between the logarithms of the numerator and the denominator:  

\\[
\log_a \left( \frac{x^3 \cdot y}{z^2} \right) = \log_a(x^3 \cdot y) - \log_a(z^2)
\\]

Next, we apply the product rule, which tells us that the logarithm of a product is the sum of the logarithms of the factors:  

\\[
\log_a(x^3 \cdot y) = \log_a(x^3) + \log_a(y)
\\]

Thus, the expression becomes:  

\\[
\log_a \left( \frac{x^3 \cdot y}{z^2} \right) = \log_a(x^3) + \log_a(y) - \log_a(z^2)
\\]

Now, we apply the power rule, which states that the logarithm of a power is the exponent times the logarithm of the base:  

\\[
\log_a(x^3) = 3 \log_a(x) \quad \text{and} \quad \log_a(z^2) = 2 \log_a(z)
\\]

Finally, we substitute and simplify, obtaining the expression:

\\[
\log_a \left( \frac{x^3 \cdot y}{z^2} \right) = 3 \log_a(x) + \log_a(y) - 2 \log_a(z)
\\]

- - -
## Changing the base of a logarithm

Any logarithm with base \\(a\\) can be represented as the ratio of logarithms with a common base. Specifically, a logarithm with base \\(a\\) and argument \\(b\\) can be written as the ratio of two logarithms with base \\(p\\), where the numerator has argument \\(b\\) and the denominator has argument \\(a\\):

\\[\log{_a}b = \frac{\log{_p}b}{\log{_p}a} \\]

> This property is advantageous because it significantly simplifies calculations in various contexts.

- - -
## Example 2

Let's use a simple example to demonstrate the formula for changing the base of the logarithms. According to the definition of logarithm, the logarithm in base \\(a\\) of a number \\(x\\), denoted as \\(\log_a(x)\\), represents the exponent to which we must raise the base \\(a\\) to get the number \\(x\\). We can write the change of base property as:

\\[\log_a(x) = \frac{\log_b(x)}{\log_b(a)}\\]

Let's consider the substitution \\( y = \log_a(x) \\), which means, according to the definition of logarithm, \\( a^y = x \\). We have:

\\[\log_b(a^y) = \log_b(x)\\]


For the property of the power of a logarithm, we obtain:

\\[y \cdot \log_b(a) = \log_b(x)\\]


Now, dividing both sides by \\(\log_b(a) \\) we obtain:

\\[y = \frac{\log_b(x)}{\log_b(a)}\\]

While \\( y = \log_a(x) \\), we have proved that:

\\[\log_a(x) = \frac{\log_b(x)}{\log_b(a)}\\]

- - -
## Logarithmic equations

[Logarithmic equations](../logarithmic-equations) are mathematical expressions in which the variable appears within a logarithmic function. Solving such equations requires a thorough understanding of logarithmic properties, which are essential for isolating and determining the variable's value. A typical logarithmic equation is structured as follows:

\\[ \log_af(x) = g(x) \\]

+ \\( a \\) is the base of the logarithm and it must meet the condition \\( a \gt 0, a\\neq 1.\\)

+ The function \\(f(x)\\) serves as the argument of the logarithm and must be greater than zero. This requirement arises because the logarithm function is defined only for positive numbers.
- - -
## The natural logarithm

From an analytical standpoint, the natural logarithm is defined independently of exponentiation using a [definite integral](../definite-integrals/). For every real number \\( x > 0 \\), the natural logarithm is given by:

\\[
\ln x = \int_1^x \frac{1}{t} \\, dt
\\]

This definition ensures that \\( \ln x \\) is well-defined for all positive real numbers because the function \\( \frac{1}{t} \\) is continuous on \\( (0,+\infty) \\). By the [Fundamental Theorem of Calculus](../fundamental-theorem-of-calculus/), the natural logarithm is differentiable and satisfies:

\\[
(\ln x)’ = \frac{1}{x} \qquad x>0
\\]

Furthermore, the natural logarithm is [strictly increasing](../increasing-and-decreasing-functions/) because its [derivative](../derivatives/) is positive on \\( (0,+\infty) \\). It is also concave, as:

\\[
(\ln x)^{\prime\prime}= -\frac{1}{x^2} < 0
\\]

- - -

The exponential function \\( e^x \\) is defined as the inverse of \\( \ln x \\). Once the natural logarithm is established, logarithms with any base \\( a>0 \\), \\( a\neq 1 \\), are defined by:

\\[
\log_a x = \frac{\ln x}{\ln a}
\\]

This construction offers a rigorous analytical foundation for logarithms and accounts for their continuity, differentiability, and structural properties.

- - -
## Series expansion of the natural logarithm

The integral definition of the natural logarithm provides a direct route to its representation as a power series. Starting from the identity:

\\[
\ln(1+x) = \int_0^x \frac{1}{1+t} \\, dt
\\]

the integrand can be expanded as a geometric series. For \\( |t| < 1 \\) one has the following:

\\[
\frac{1}{1+t} = \sum_{n=0}^{\infty} (-1)^n t^n = 1-t+t^2-t^3+\cdots
\\]

The series converges uniformly on every closed subinterval of \\( (-1,1) \\), which allows termwise integration. Integrating from \\( 0 \\) to \\( x \\) gives:

\\[
\ln(1+x) = \sum_{n=0}^{\infty} \frac{(-1)^n}{n+1}\\, x^{n+1} = x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+\cdots
\\]

The series converges for \\( -1 < x \le 1 \\). The case \\( x = -1 \\) is excluded because the corresponding series is the negative of the harmonic series, which diverges. At \\( x = 1 \\) the series converges by the alternating series test and yields the elegant identity:

\\[
\ln 2 = 1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\cdots
\\]

- - -

The series provides a constructive method for computing the natural logarithm and clarifies its local behaviour. Truncating the expansion after the first term gives the linear approximation:

\\[
\ln(1+x) \approx x \qquad \text{for } x \to 0
\\]

with an error of order \\( x^2 \\). This approximation is the analytical content of the equivalent statement:

\\[
\lim_{x \to 0} \frac{\ln(1+x)}{x} = 1
\\]

which appears in countless calculations involving limits, derivatives, and the analysis of small perturbations. The same idea underlies the use of the natural logarithm in continuously compounded interest, in the approximation of small percentage changes, and in the local linearisation of multiplicative phenomena.

> The series for \\( \ln(1+x) \\) converges slowly when \\( x \\) is close to \\( 1 \\), which makes it impractical for direct numerical computation of values such as \\( \ln 2 \\). The transformation \\( \ln\frac{1+y}{1-y} = 2\left(y+\frac{y^3}{3}+\frac{y^5}{5}+\cdots\right) \\), obtained by combining the series for \\( \ln(1+y) \\) and \\( \ln(1-y) \\), converges much more rapidly and forms the basis of efficient algorithms for computing logarithms.

- - -
## Logarithmic differentiation

A function of the form \\( y = f(x)^{g(x)} \\), in which both the base and the exponent depend on the variable, cannot be differentiated by direct application of the power rule or the exponential rule. The standard technique to handle such expressions is logarithmic differentiation. The procedure consists of taking the natural logarithm of both sides and then differentiating implicitly.

Applying the logarithm to \\( y = f(x)^{g(x)} \\) and using the power rule for logarithms gives the following:

\\[
\ln y = g(x)\\,\ln f(x)
\\]

Differentiating both sides with respect to \\( x \\), and applying the chain rule on the left and the product rule on the right, one obtains:

\\[
\frac{y'}{y} = g'(x)\\,\ln f(x)+g(x)\\,\frac{f'(x)}{f(x)}
\\]

Solving for \\( y' \\) and substituting the original expression for \\( y \\) yields the explicit derivative:

\\[
y' = f(x)^{g(x)}\left[g'(x)\\,\ln f(x)+g(x)\\,\frac{f'(x)}{f(x)}\right]
\\]

The technique requires the condition \\( f(x) > 0 \\) on the interval of interest, so that the logarithm is well-defined.

- - -

As a concrete illustration, consider the derivative of \\( y = x^x \\) for \\( x > 0 \\). Taking the natural logarithm of both sides gives the following:

\\[
\ln y = x \ln x
\\]

Differentiating both sides, the left-hand side becomes \\( y'/y \\) by the chain rule, while the right-hand side is computed using the product rule:

\\[
\frac{y'}{y} = \ln x+x \cdot \frac{1}{x} = \ln x+1
\\]

Multiplying both sides by \\( y = x^x \\) yields the result:

\\[
\frac{d}{dx}\\,x^x = x^x\\,(\ln x+1)
\\]

The same method applies to any expression in which the variable appears in both the base and the exponent, and is also a convenient tool whenever the function admits a representation as a product of several factors, since the logarithm converts the product into a sum and simplifies the subsequent differentiation.

- - -
## The AM-GM inequality via logarithms

The [arithmetic mean](https://algebrica.org/arithmetic-mean/) and the [geometric mean](https://algebrica.org/geometric-mean/) of a finite set of positive real numbers satisfy a fundamental inequality: the arithmetic mean is always greater than or equal to the geometric mean. For positive real numbers \\(x_1, x_2, \ldots, x_n\\), this is stated as:

\\[
\frac{x_1 + x_2 + \cdots + x_n}{n} \geq \left( x_1 x_2 \cdots x_n \right)^{\frac{1}{n}}
\\]

with equality if and only if \\(x_1 = x_2 = \cdots = x_n\\). The logarithm provides one of the most elegant proofs of this result, relying on a single concavity argument.

---

The key observation is that \\(\ln\\) is a strictly concave function on \\((0,+\infty)\\), since its second derivative satisfies \\((\ln x)\'' = -1/x^2 < 0\\) for all \\(x > 0\\). Since \\(\ln\\) is concave, the following holds for any positive real numbers \\(x_1, \ldots, x_n\\):

\\[
\frac{1}{n} \sum_{i=1}^{n} \ln x_i \leq \ln\\!\left( \frac{1}{n} \sum_{i=1}^{n} x_i \right)
\\]

The left-hand side is the arithmetic mean of \\(\ln x_1, \ldots, \ln x_n\\), which by the logarithmic form of the [geometric mean](https://algebrica.org/geometric-mean/) equals \\(\ln M_g\\). The right-hand side is \\(\ln M_a\\), where \\(M_a\\) denotes the [arithmetic mean](https://algebrica.org/arithmetic-mean/). The inequality therefore becomes:

\\[
\ln M_g \leq \ln M_a
\\]

Since \\(\ln\\) is strictly increasing, this is equivalent to \\(M_g \leq M_a\\), which is the AM-GM inequality. Equality holds if and only if all arguments are equal, that is, \\(x_1 = x_2 = \cdots = x_n\\).

> This proof makes explicit the structural role of the logarithm: by mapping the multiplicative structure of \\(M_g\\) into the additive structure of \\(M_a\\), it reduces the inequality between two different types of mean to a single analytic property of \\(\ln\\).