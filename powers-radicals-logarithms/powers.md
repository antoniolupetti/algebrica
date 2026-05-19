# Powers

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/powers/

## Introduction to powers

Powers are mathematical operations that show how many times a [number](../types-of-numbers/) is to be multiplied by itself. The standard way of writing a power is \\(a^{\large{n}}\\) where \\(a\\) is the base and \\(n\\) is the exponent:
\\[a^n = \underbrace{a \cdot a \cdot a \cdots a}_{n \text{ times}} \quad \text{with} \quad a \in \mathbb{R}, \quad n \in \mathbb{Z}^+ \tag{1}\\]

> From a geometric perspective, when considering a positive number \\( a \\), it can be observed that the expressions \\( a^2 \\) and \\( a^3 \\) respectively denote the area of a square with its side length being \\( a \\) and the volume of a cube with its edge length being \\( a \\).

- - -

The value of the exponent \\( n \\) can be positive, negative, or zero. When the exponent is negative, it indicates a reciprocal relationship between powers, expressed as follows:
\\[a^{-n} = \frac{1}{a^{n}}\\]
This means that raising a number to a negative exponent is equivalent to taking the reciprocal of the same number raised to the corresponding positive exponent. If the exponent is fractional, for instance \\( n = \frac{1}{m} \\), the power can be rewritten in [radical](../radicals/) form as follows:
\\[a^{\frac{1}{m}} = \sqrt[m]{a}\\]
This expression represents the \\(m\\)-th root of \\( a \\). By combining both concepts, a negative fractional exponent can be interpreted as the reciprocal of a root:
\\[a^{-\frac{1}{m}} = \frac{1}{\sqrt[m]{a}}\\]
This unified notation allows exponents to represent both powers and roots, simplifying many algebraic expressions and making exponent rules consistent across different cases.

- - -

The table below illustrates selected values of \\(a^n\\). Each row corresponds to a fixed base \\(a\\) and each column to a fixed exponent \\(n\\).

|       | \\( a^{-2} \\) | \\( a^{-1} \\) | \\( a^{0} \\) | \\( a^{1} \\) | \\( a^{2} \\) | ... |
|:-----:|:--------------:|:--------------:|:--------------:|:--------------:|:--------------:|:---:|
| \\(-2\\) | \\( \dfrac{1}{4} \\) | \\( -\dfrac{1}{2} \\) | \\( 1 \\) | \\( -2 \\) | \\( 4 \\) | ... |
| \\(-1\\) | \\( 1 \\) | \\( -1 \\) | \\( 1 \\) | \\( -1 \\) | \\( 1 \\) | ... |
| \\(0\\)  | — | — | — | \\( 0 \\) | \\( 0 \\) | ... |
| \\(1\\)  | \\( 1 \\) | \\( 1 \\) | \\( 1 \\) | \\( 1 \\) | \\( 1 \\) | ... |
| \\(2\\)  | \\( \dfrac{1}{4} \\) | \\( \dfrac{1}{2} \\) | \\( 1 \\) | \\( 2 \\) | \\( 4 \\) | ... |
| ...     | ... | ... | ... | ... | ... | ... |

> The symbol — indicates that the expression is undefined: negative exponents of zero involve division by zero, and \\(0^0\\) is an [indeterminate form](../indeterminate-forms/).

If the base \\( a \\) is negative, the sign of \\( a^n \\) alternates according to the parity of \\( n \\). For instance, \\( (-1)^n = 1 \\) when \\( n \\) is even, and \\( (-1)^n = -1 \\) when \\( n \\) is odd. This alternating behaviour is particularly significant in the analysis of sequences and limits. Additionally, negative bases with fractional exponents must be treated carefully, since expressions such as \\( (-1)^{1/2} \\) are not defined in \\( \mathbb{R} \\).

- - -
## Powers with real exponents

The definition \\( a^n \\) in \\(1\\) is valid only for positive [integers](../integers/) \\( n \\), but the idea of repeated multiplication does not work when the exponent is not an integer. Extending this concept to [real](../properties-of-real-numbers/) exponents necessitates a different approach, one based on the [exponential function](../exponential-function/) and the [natural logarithm](../logarithms/). For any positive base \\( a > 0 \\) and real exponent \\( x \in \mathbb{R} \\), the power \\( a^x \\) is defined as follows.
\\[a^x = e^{x \ln a}\\]
When \\( x \\) is a positive integer, it yields repeated multiplication. For rational \\( x \\), it aligns with the radical interpretation. To verify this, let \\( x = \frac{p}{q} \\) with \\( p, q \in \mathbb{Z} \\) and \\( q \neq 0 \\). Applying the definition yields the following:

\\[e^{\frac{p}{q} \ln a} = \left(e^{\ln a}\right)^{\frac{p}{q}} = a^{\frac{p}{q}}\\]

This confirms that the exponential definition reduces to the usual radical interpretation when the exponent is rational, and the two notations are fully consistent.The necessity of this extension can be illustrated by considering \\( 2^{\sqrt{2}} \\). Because \\( \sqrt{2} \\) is irrational and cannot be written as a fraction \\( \frac{m}{n} \\), the radical definition is inapplicable. Applying the real exponent definition yields the following:
\\[2^{\sqrt{2}} = e^{\sqrt{2} \ln 2} \approx e^{0.9803} \approx 2.665\\]
This value is well-defined and can be approximated to any specified degree of precision. This definition also explains why the base must satisfy \\( a > 0 \\). If \\( a \leq 0 \\), the expression \\( \ln a \\) is undefined in \\( \mathbb{R} \\), and the extension fails. This is consistent with the earlier observation that negative bases with fractional exponents do not yield real numbers. As a result, the function \\( f(x) = a^x \\) is [continuous](../continuous-functions/) and [differentiable](../derivatives/) for all real numbers when \\( a > 0 \\).

- - -
## Fundamental rules of powers

The following rules govern the manipulation of expressions involving powers. They hold for real bases and exponents under the conditions specified in each case.

Raising any base not equal to zero to an exponent of zero always results in \\(1\\). The value of \\(a\\) is restricted because the operation \\(0^0\\) is meaningless and considered an indeterminate form.
\\[a^0 = 1 \quad \text{if} \quad a \neq 0\\]

- - -

Any power of zero always results in zero because it corresponds to the product of \\( n \\) zeros, where \\( n \\) is the exponent:
\\[0^n = 0 \quad \text{for } n > 0\\]
The condition \\( n > 0 \\) is necessary because \\( 0^0 \\) is an [indeterminate form](../indeterminate-forms/). Depending on the context, it can be approached as a [limit](../limits) in two ways:
\\[\lim_{x \to 0^+} 0^x = 0\\]
\\[\lim_{x \to 0} x^0 = 1\\]
The form \\( 0^0 \\) is therefore left undefined in the context of limits. More generally, the following expressions are indeterminate forms, meaning their value cannot be determined without further analysis of the specific limit: \\( 0^0 \\), \\( 1^{\infty} \\), and \\( \infty^0 \\).

> In combinatorics and algebra, however, it is conventionally assigned the value \\( 1 \\), since it arises naturally in expressions such as the [binomial theorem](../binomial-theorem/).

- - -

The product of two or more powers with the same base \\(a\\) is a power with the same base and exponent equal to the sum of the exponents:
\\[a^n \cdot a^m = a^{n+m}\\]
To see why this holds, observe that \\( a^n \\) represents the product of \\( n \\) factors equal to \\( a \\), and \\( a^m \\) represents the product of \\( m \\) such factors. Concatenating these two products gives a total of \\( n+m \\) factors, which is precisely \\( a^{n+m} \\). In formal terms, the argument reads as follows:
\\[a^n \cdot a^m = \underbrace{a \cdot a \cdots a}\_{n \text{ times}} \cdot \underbrace{a \cdot a \cdots a}\_{m \text{ times}} = \underbrace{a \cdot a \cdots a}\_{n+m \text{ times}} = a^{n+m}\\]
This reasoning applies directly to positive integer exponents, as it relies on counting factors. For integer, rational, or real exponents, the same result follows from the definition \\( a^x = e^{x \ln a} \\). Since the exponential function satisfies \\( e^u \cdot e^v = e^{u+v} \\), we have the following:
\\[a^n \cdot a^m = e^{n \ln a} \cdot e^{m \ln a} = e^{(n+m) \ln a} = a^{n+m}\\]

- - -

The product of powers with different bases \\(a\\) and \\(b\\) but the same exponent \\(n\\) is a power whose base is the product of the original bases.
\\[a^{n} \cdot b^n = (ab)^n\\]

> Consider the expression \\(2^3 \cdot 5^3\\). Since both factors share the same exponent, they can be combined into a single power of the product of the bases, giving \\(2^3 \cdot 5^3 = (2 \cdot 5)^3 = 10^3\\).

- - -

The quotient of two powers with the same base \\(a\\) is a power with the same base and exponent equal to the difference between the exponents.
\\[\frac{a^n}{a^m} = a^{n-m}\\]
This follows directly from the product rule already established. Dividing by \\(a^m\\) is equivalent to multiplying by \\(a^{-m}\\), so the quotient can be rewritten as follows.
\\[\frac{a^n}{a^m} = a^n \cdot a^{-m} = a^{n+(-m)} = a^{n-m}\\]
The condition \\(a \neq 0\\) is required for \\(a^{-m}\\) to be defined.

- - -

The quotient of powers with different bases \\(a\\) and \\(b\\) but the same exponent \\(n\\) is a power whose base is the quotient of the original bases.
\\[\frac{a^n}{b^n} = \left(\frac{a}{b}\right)^n\\]

> Consider the expression \\(\dfrac{6^3}{2^3}\\). Since both terms share the same exponent, the quotient can be rewritten as a single power of the ratio of the bases, giving \\(\dfrac{6^3}{2^3} = \left(\dfrac{6}{2}\right)^3 = 3^3 = 27\\).

- - -

The power of a power is a power with the same base and exponent equal to the product of the two exponents.
\\[(a^m)^n = a^{m \cdot n}\\]

> Consider the expression \\((2^3)^4\\). Applying the rule for the power of a power, the two exponents are multiplied, giving \\((2^3)^4 = 2^{3 \cdot 4} = 2^{12}\\).

- - -

When a base \\(a\\) is raised to a negative exponent, the result is the reciprocal of the same base raised to the corresponding positive exponent.
\\[a^{-n} = \frac{1}{a^n} \quad \text{with} \quad a \neq 0 \quad \text{and} \quad n > 0\\]

- - -

When the exponent is a rational number of the form \\( \frac{m}{n} \\), the power can be expressed as a radical.
\\[a^{\frac{m}{n}} = \sqrt[n]{a^m} \quad \text{where} \quad m, n \in \mathbb{N} \quad \text{and} \quad n \neq 0\\]

> The properties of powers transform multiplications and divisions of numbers raised to powers into simpler operations, making calculations faster and more manageable, especially in algebraic expressions.

- - -
## Summary

|                          |                                                        |                                  |
| :----------------------- | :----------------------------------------------------: | :------------------------------- |
| Zero exponent            |                    \\[ a^0 = 1 \\]                     | \\[ a \neq 0 \\]                 |
| Power of zero            |                    \\[ 0^n = 0 \\]                     | \\[ n > 0 \\]                    |
| Product (same base)      |            \\[ a^n \cdot a^m = a^{n+m} \\]             | \\[ a \in \mathbb{R} \\]         |
| Product (same exponent)  |             \\[ a^n \cdot b^n = (ab)^n \\]             | \\[ a, b \in \mathbb{R} \\]      |
| Quotient (same base)     |           \\[ \dfrac{a^n}{a^m} = a^{n-m} \\]           | \\[ a \neq 0 \\]                 |
| Quotient (same exponent) | \\[ \dfrac{a^n}{b^n} = \left(\dfrac{a}{b}\right)^n \\] | \\[ b \neq 0 \\]                 |
| Power of a power         |                \\[ (a^m)^n = a^{mn} \\]                | \\[ a \in \mathbb{R} \\]         |
| Negative exponent        |            \\[ a^{-n} = \dfrac{1}{a^n} \\]             | \\[ a \neq 0,\ n > 0 \\]         |
| Rational exponent        |        \\[ a^{\frac{m}{n}} = \sqrt[n]{a^m} \\]         | \\[ a > 0,\ n \neq 0 \\]         |
| Real exponent            |               \\[ a^x = e^{x \ln a} \\]                | \\[ a > 0,\ x \in \mathbb{R} \\] |
- - -
## Why is \\( a^0 = 1 \\)?

Among the properties of exponents, the result \\(a^0 = 1\\) may initially seem counterintuitive, but this outcome follows directly from the quotient rule, which states that dividing any power by itself yields \\(1\\).
\\[\frac{a^n}{a^n} = 1\\]
Applying the quotient rule to the left-hand side gives the following.
\\[\frac{a^n}{a^n} = a^{n-n} = a^0\\]
This reasoning establishes that \\( a^0 = 1 \\). The condition \\( a \neq 0 \\) is a direct consequence of the argument, since the expression \\( \frac{a^n}{a^n} \\) is defined only when \\( a \neq 0 \\).

- - -
## Bernoulli's inequality

Among the elementary results involving integer powers, one of the most useful is the inequality attributed to Jakob Bernoulli. For every real number \\( x \ge -1 \\) and every natural number \\( n \in \mathbb{N} \\) the following holds:

\\[
(1+x)^n \ge 1+nx
\\]

The condition \\( x \ge -1 \\) ensures that the base \\( 1+x \\) is non-negative and that the power \\( (1+x)^n \\) is well-defined in \\( \mathbb{R} \\) for every \\( n \\). Equality occurs when \\( n = 0 \\), when \\( n = 1 \\), or when \\( x = 0 \\); in every other case the inequality is strict.

A proof proceeds by induction on \\( n \\). For \\( n = 0 \\) both sides equal \\( 1 \\), and for \\( n = 1 \\) both sides equal \\( 1+x \\). Assume that the inequality holds for some \\( n \ge 1 \\):

\\[
(1+x)^n \ge 1+nx
\\]

Multiplying both sides by the non-negative quantity \\( 1+x \\) preserves the direction of the inequality, yielding the following:

\\[
(1+x)^{n+1} \ge (1+nx)(1+x) = 1+(n+1)x+nx^2
\\]

The term \\( nx^2 \\) is non-negative for every real \\( x \\), so it can be discarded without violating the inequality:

\\[
(1+x)^{n+1} \ge 1+(n+1)x
\\]

This establishes the statement for \\( n+1 \\) and completes the induction.

> The inequality extends to real exponents \\( r \\) with the conventions \\( r \ge 1 \\) or \\( r \le 0 \\), and reverses for \\( 0 < r < 1 \\). These generalisations rely on the convexity properties of the function \\( t \mapsto t^r \\) and are typically established through differential calculus.

- - -

The importance of Bernoulli's inequality stems from its role in obtaining sharp estimates with minimal effort. A classical application is the proof that the sequence \\( a_n = \left(1+\frac{1}{n}\right)^n \\) is monotonically increasing. The argument relies on the ratio of consecutive terms and on a single application of the inequality to control the resulting expression. Since the same sequence is bounded above, it admits a limit, and that limit is precisely [Euler's number](../euler-number-limit-sequence/) \\( e \\):

\\[
e = \lim_{n \to +\infty}\left(1+\frac{1}{n}\right)^n
\\]

In this sense Bernoulli's inequality is one of the elementary tools that make the introduction of \\( e \\) possible without recourse to the machinery of analysis.

- - -
## Power and exponential

Sometimes, people mistakenly mix up the concepts of power and exponential function. A power is an arithmetic operation in which a base \\(a\\) is multiplied by itself \\(n\\) times, with \\(n\\) referred to as the exponent. The [exponential function](../exponential-function/), by contrast, is a function in which the variable appears in the exponent rather than the base, taking the form:
\\[f(x) = e^x \quad \text{or} \quad f(x) = a^x\\]
where \\(a > 0\\) and \\(a \neq 1\\).

- - -
## Hierarchy of growth rates

A recurring problem in mathematical analysis is the comparison of functions that tend to infinity as the variable becomes arbitrarily large. The functions involving logarithms, powers, and exponentials form a strict ordering in this regard, often called the hierarchy of growth rates or the scale of infinities. The fundamental statement is that for every \\( \alpha > 0 \\) and every \\( a > 1 \\) the following holds:

\\[
\lim_{x \to +\infty} \frac{\log_a x}{x^{\alpha}} = 0
\qquad \text{and} \qquad
\lim_{x \to +\infty} \frac{x^{\alpha}}{a^{x}} = 0
\\]

The first limit asserts that any positive power of \\( x \\), however small the exponent, eventually dominates the logarithm. The second states that any exponential with base greater than \\( 1 \\) eventually dominates every power of \\( x \\), however large the exponent. Combining the two statements yields a strict three-tier ordering in which logarithms grow more slowly than powers, and powers grow more slowly than exponentials.

> The verb "eventually" carries a precise meaning. For any prescribed threshold \\( \varepsilon > 0 \\), one can find an \\( x_0 \\) such that the corresponding quotient remains below \\( \varepsilon \\) for every \\( x > x_0 \\). The point at which dominance becomes apparent depends on the parameters \\( \alpha \\) and \\( a \\), but the asymptotic behaviour does not.

- - -

Both limits can be reduced to a single fundamental result by elementary substitutions. Setting \\( y = \log_a x \\), so that \\( x = a^y \\), transforms the first limit into the second with adjusted constants. The second limit, in turn, follows from the series expansion of the exponential function. For every \\( a > 1 \\) one can write \\( a^x = e^{x \ln a} \\), and since the exponential function exceeds each of its truncated Taylor polynomials, the following estimate holds for every natural number \\( k \\):

\\[
e^{u} \ge \frac{u^{k}}{k!} \qquad \forall u \ge 0
\\]

Choosing \\( k \\) larger than \\( \alpha \\) and setting \\( u = x \ln a \\), one obtains a lower bound on \\( a^x \\) that grows faster than any prescribed power of \\( x \\). The quotient \\( x^{\alpha}/a^{x} \\) is therefore bounded above by an expression that tends to zero, which establishes the limit.

- - -

The practical value of this hierarchy lies in the simplification of asymptotic estimates. Whenever a sum or product involves terms of different growth orders, only the dominant one survives in the leading-order behaviour. For example:

\\[
\lim_{x \to +\infty} \frac{2^{x}+x^{10}+\ln x}{2^{x}} = 1
\\]

The contributions of \\( x^{10} \\) and \\( \ln x \\) become negligible compared with \\( 2^{x} \\) as \\( x \\) tends to infinity, even though for moderate values of \\( x \\) the polynomial term may still be numerically larger. The same hierarchy underlies the standard classification of algorithmic complexity, where logarithmic, polynomial, and exponential running times are treated as fundamentally distinct regimes.

- - -
## Powers with complex exponents

The definition \\( a^x = e^{x \ln a} \\) extends naturally to cases where the exponent is complex. When the exponent is purely imaginary, that is, when \\( x = i\theta \\) with \\( \theta \in \mathbb{R} \\), the expression \\( e^{i\theta} \\) is well-defined provided one interprets the exponential through its Taylor series expansion. Recalling that:

\\[e^z = \sum_{n=0}^{\infty} \frac{z^n}{n!}\\]

and substituting \\( z = i\theta \\), the series separates into real and imaginary parts by exploiting the periodicity of the powers of \\( i \\), yielding Euler's formula.

\\[e^{i\theta} = \cos\theta + i\sin\theta\\]

This result establishes a profound connection between the exponential function and trigonometry, showing that the two are in fact different expressions of the same underlying structure over the complex numbers. It enables any complex number to be represented in exponential form as \\( z = re^{i\theta} \\), where \\( r \\) denotes the modulus and \\( \theta \\) the argument. A notable consequence is one of the most celebrated identities in mathematics, obtained by setting \\( \theta = \pi \\):

\\[e^{i\pi} + 1 = 0\\]

This equation, known as Euler's identity, unites five fundamental mathematical constants in a single expression. A comprehensive discussion of complex exponents, including methods for computing powers and roots of complex numbers, is provided in the page [complex numbers in exponential form](../complex-numbers-exponential-form/).