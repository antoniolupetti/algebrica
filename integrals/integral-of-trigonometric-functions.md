# Integral of Trigonometric Functions

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/integral-of-trigonometric-functions/

## Introduction

On the individual [function](../functions/) pages, such as those for [sine](../sine-function/), [cosine](../cosine-function/), [tangent](../tangent-function/), and [cotangent](../cotangent-function/), the corresponding antiderivatives are stated alongside the other defining properties. These integrals are straightforward to compute and worth keeping in mind, since they appear constantly in problem solving. The list below collects the antiderivatives of all the main trigonometric functions, giving an immediate overall view of the essential results. The final six entries record the corresponding [hyperbolic](../?s=hyperbolic+functions) integrals, included here for completeness because they arise from the same techniques and are often needed alongside their circular counterparts.

+ \\[\text{1. } \quad \int \sin x\\,dx = -\cos x + c\\]

+ \\[\text{2. } \quad \int \cos x\\,dx = \sin x + c\\]

+ \\[\text{3. } \quad \int \tan x\\,dx = -\ln|\cos x| + c\\]
+ \\[\text{4. } \quad \int \cot x\\,dx = \ln|\sin x| + c\\]
+ \\[\text{5. } \quad \int \sec x\\,dx = \ln|\sec x + \tan x| + c\\]
+ \\[\text{6. } \quad \int \csc x\\,dx = \ln|\csc x - \cot x| + c\\]
+ \\[\text{7. } \quad \int \sinh x\\,dx = \cosh x + c\\]
+ \\[\text{8. } \quad \int \cosh x\\,dx = \sinh x + c\\]
+ \\[\text{9. } \quad \int \tanh x\\,dx = \ln|\cosh x| + c\\]
+ \\[\text{10. } \quad \int \coth x\\,dx = \ln|\sinh x| + c\\]
+ \\[\text{11. } \quad \int \operatorname{sech} x\\,dx = 2\\,\arctan\\!\left(\tanh\frac{x}{2}\right) + c\\]
+ \\[\text{12. } \quad \int \operatorname{csch} x\\,dx = \ln\left|\tanh\frac{x}{2}\right| + c\\]

> Here \\(c\\) denotes the constant of integration, included to represent the entire family of antiderivatives associated with an [indefinite integral](../indefinite-integrals/). Each value of \\(c\\) corresponds to a different primitive, and all of them share the same derivative.

- - -
## Integrals of trigonometric powers with \\(n\\) even

A frequent case in which the antiderivative is not immediately accessible occurs when sine or cosine appears raised to an integer power, namely:

\\[\int \sin^{n} x\\,dx\\]
\\[\int \cos^{n} x\\,dx\\]

When the exponent \\(n\\) is even, the integral is simplified by rewriting the squared trigonometric terms through the power-reduction identities:

\\[\sin^{2} x = \frac{1 - \cos 2x}{2}\\]
\\[\cos^{2} x = \frac{1 + \cos 2x}{2}\\]

These identities lower the power of the function and make the integral accessible. They follow directly from two standard relationships. Starting from the [Pythagorean identity](../pythagorean-identity/):

\\[
\sin^{2}x + \cos^{2}x = 1
\\]

and combining it with the [double-angle formula](../trigonometric-identities/):

\\[
\cos 2x = \cos^{2}x - \sin^{2}x
\\]

we can express \\(\cos 2x\\) entirely in terms of either \\(\cos^{2}x\\) or \\(\sin^{2}x\\).

Replacing \\(\sin^{2}x\\) with \\(1 - \cos^{2}x\\) we obtain:

\\[
\cos 2x = \cos^{2}x - (1 - \cos^{2}x) = 2\cos^{2}x - 1
\\]

Solving this expression for \\(\cos^{2}x\\) yields:

\\[
\cos^{2}x = \frac{1 + \cos 2x}{2}
\\]

A similar argument holds for \\(\sin^{2}x\\). Substituting \\(\cos^{2}x = 1 - \sin^{2}x\\) into the double-angle formula gives:

\\[
\cos 2x = (1 - \sin^{2}x) - \sin^{2}x = 1 - 2\sin^{2}x
\\]

Solving for \\(\sin^{2}x\\) gives:

\\[
\sin^{2}x = \frac{1 - \cos 2x}{2}
\\]

- - -
## Example 1

As an illustration of the method, let us consider the following integral:

\\[
\int 2\cos^{4}x\\,dx
\\]

To handle the fourth power of the cosine, we start by recalling the power-reduction identity:

\\[
\cos^{2}x = \frac{1+\cos 2x}{2}
\\]

Applying this identity allows us to rewrite the expression in a more manageable form:

\\[
\begin{aligned}
\cos^{4}x & = \left(\frac{1+\cos 2x}{2}\right)^{2} \\\\[6pt]
&= \frac{1}{4}\left(1 + 2\cos 2x + \cos^{2} 2x\right)
\end{aligned}
\\]

At this point, one power of cosine still remains. We reduce it using the identity:

\\[
\cos^{2} 2x = \frac{1+\cos 4x}{2}
\\]

Substituting this expression into the previous result gives:

\\[
\begin{aligned}
\cos^{4}x & = \frac{1}{4}\left(1 + 2\cos 2x + \frac{1+\cos 4x}{2}\right) \\\\[6pt]
&= \frac{1}{4}\left(\frac{3}{2} + 2\cos 2x + \frac{1}{2}\cos 4x\right) \\\\[6pt]
&= \frac{3}{8} + \frac{1}{2}\cos 2x + \frac{1}{8}\cos 4x
\end{aligned}
\\]

Multiplying by \\(2\\), as required by the original integral, we obtain the simplified form:

\\[
2\cos^{4}x = \frac{3}{4} + \cos 2x + \frac{1}{4}\cos 4x
\\]

Integrating each term separately, we obtain:

\\[
\int 2\cos^{4}x\\,dx = \frac{3}{4}x + \frac{1}{2}\sin 2x + \frac{1}{16}\sin 4x + c
\\]

> The fourth power has therefore been reduced to a sum of elementary terms, each integrable on sight, which is the central advantage of the power-reduction approach when the exponent is even.

- - -
## Integrals of trigonometric powers with \\(n\\) odd

When the exponent \\(n\\) is odd, the method becomes more direct. We separate one factor of the function whose power is odd and rewrite the remaining even power using the Pythagorean identity. Writing \\(n = 2k + 1\\), for sine this gives:

\\[
\begin{aligned}
\int \sin^{n} x\\,dx
&= \int \sin x\\,(\sin^{2}x)^{k}\\,dx \\\\[6pt]
&= \int \sin x\\,(1 - \cos^{2}x)^{k}\\,dx
\end{aligned}
\\]

The [substitution](../integration-by-substitution/):

\\[ u = \cos x \\]
\\[ du = -\sin x\\,dx \\]

transforms the integral into a [polynomial](../polynomials/) in \\(u\\), which can then be integrated without difficulty. The procedure for an odd power of cosine is entirely analogous: one extracts a single factor \\(\cos x\\) and rewrites the remaining even power using

\\[
\cos^{2}x = 1 - \sin^{2}x
\\]

leading to the substitution \\(u = \sin x\\). In both cases, isolating one factor reduces the integral to a polynomial form.

- - -
## Example 2

Consider the following integral:

\\[\int \cos^{5}x \\, dx\\]

The exponent is odd, so the strategy is to isolate one factor of cosine and rewrite the remaining even [power](../powers/) using the Pythagorean identity. We write:

\\[\int \cos^{5}x \\, dx = \int \cos^{4}x \cdot \cos x \\, dx\\]

The factor \\(\cos^{4}x\\) is an even power, so we can express it in terms of \\(\sin^{2}x\\):

\\[\cos^{4}x = (\cos^{2}x)^{2} = (1 - \sin^{2}x)^{2}\\]

The integral becomes:

\\[\int (1 - \sin^{2}x)^{2} \cdot \cos x \\, dx\\]

At this point the factor \\(\cos x \\, dx\\) is exactly the differential of \\(\sin x\\), so we set:

\\[u = \sin x \qquad du = \cos x \\, dx\\]

and the integral transforms into a [polynomial](../polynomials/) in \\(u\\):

\\[\int (1 - u^{2})^{2} \\, du\\]

Expanding the square we obtain:

\\[\int (1 - 2u^{2} + u^{4}) \\, du\\]

Each term integrates immediately:

\\[u - \frac{2}{3}u^{3} + \frac{1}{5}u^{5} + c\\]

Substituting back \\(u = \sin x\\) we have:

\\[\sin x - \frac{2}{3}\sin^{3}x + \frac{1}{5}\sin^{5}x + c\\]

> The substitution resolved the integral cleanly because the isolated factor \\(\cos x\\) was precisely the derivative of \\(u = \sin x\\). Recognising this pattern is what reduces the odd-exponent case to a routine polynomial integration.

- - -
## Mixed powers of sine and cosine

A more general situation arises when sine and cosine appear together, in integrals of the form:

\\[\int \sin^{m} x \cos^{n} x\\,dx\\]

The strategy depends on the parity of the exponents, and it combines the two methods already developed. If at least one of the exponents is odd, the odd-power technique applies directly. Suppose \\(n\\) is odd. We isolate one factor of \\(\cos x\\), convert the remaining even power of cosine into sine through \\(\cos^{2}x = 1 - \sin^{2}x\\), and use the substitution \\(u = \sin x\\). If instead \\(m\\) is odd, the symmetric procedure isolates one factor of \\(\sin x\\) and substitutes \\(u = \cos x\\). When both exponents are odd, either choice works.

If both \\(m\\) and \\(n\\) are even, no factor can be split off to serve as a differential. In this case the power-reduction identities are applied to every squared term:

\\[\sin^{2} x = \frac{1 - \cos 2x}{2}\\]
\\[\cos^{2} x = \frac{1 + \cos 2x}{2}\\]

The identity \\(\sin x \cos x = \tfrac{1}{2}\sin 2x\\) is frequently useful as well, since it lowers the combined degree in a single step. Repeated application reduces the integrand to a sum of terms of the form \\(\cos kx\\), each of which integrates immediately, exactly as in Example 1.

- - -
## Example 3

Consider the following integral:

\\[\int \sin^{2} x \cos^{3} x \\, dx\\]

The exponent of cosine is odd, so we isolate one factor of \\(\cos x\\) and rewrite the remaining even power in terms of sine:

\\[\int \sin^{2} x \cos^{3} x \\, dx = \int \sin^{2} x \cdot \cos^{2} x \cdot \cos x \\, dx\\]

Using \\(\cos^{2}x = 1 - \sin^{2}x\\), the integral becomes:

\\[\int \sin^{2} x \\,(1 - \sin^{2}x) \cdot \cos x \\, dx\\]

The factor \\(\cos x \\, dx\\) is the differential of \\(\sin x\\), so we set:

\\[u = \sin x \qquad du = \cos x \\, dx\\]

and the integral transforms into a [polynomial](../polynomials/) in \\(u\\):

\\[\int u^{2}\\,(1 - u^{2}) \\, du = \int (u^{2} - u^{4}) \\, du\\]

Each term integrates immediately:

\\[\frac{1}{3}u^{3} - \frac{1}{5}u^{5} + c\\]

Substituting back \\(u = \sin x\\) we have:

\\[\frac{1}{3}\sin^{3}x - \frac{1}{5}\sin^{5}x + c\\]

The presence of a second function raised to a power did not change the method: as long as one factor with an odd exponent can be detached, the integral reduces to a polynomial in the complementary function.

- - -
## Reciprocals of sine and cosine

Other frequently encountered cases involve the integrals of the reciprocals of sine and cosine. Although these expressions appear less straightforward at first, both follow from the same algebraic device. For the secant, the integrand is multiplied by a fraction equal to \\(1\\):

\\[
\begin{aligned}
\int \sec x\\,dx
&= \int \sec x \cdot \frac{\sec x + \tan x}{\sec x + \tan x}\\,dx \\\\[6pt]
&= \int \frac{\sec^{2}x + \sec x\tan x}{\sec x + \tan x}\\,dx
\end{aligned}
\\]

The numerator is now exactly the derivative of the denominator, since:

\\[
\frac{d}{dx}(\sec x + \tan x) = \sec x\tan x + \sec^{2}x
\\]

The integral therefore has the form \\(\int \frac{f'(x)}{f(x)}\\,dx\\), which integrates directly to \\(\ln|f(x)|\\). We obtain:

\\[
\int \frac{1}{\cos x}\\,dx = \int \sec x\\,dx = \ln|\sec x + \tan x| + c
\\]

The same structure applies to the cosecant. Multiplying the integrand by \\(\frac{\csc x - \cot x}{\csc x - \cot x}\\) gives:

\\[
\begin{aligned}
\int \csc x\\,dx
&= \int \csc x \cdot \frac{\csc x - \cot x}{\csc x - \cot x}\\,dx \\\\[6pt]
&= \int \frac{\csc^{2}x - \csc x\cot x}{\csc x - \cot x}\\,dx
\end{aligned}
\\]

Once again the numerator is the derivative of the denominator, since:

\\[
\frac{d}{dx}(\csc x - \cot x) = -\csc x\cot x + \csc^{2}x
\\]

so the integral of \\(\csc x\\) produces:

\\[
\int \frac{1}{\sin x}\\,dx = \int \csc x\\,dx = \ln|\csc x - \cot x| + c
\\]

In both cases the result is [logarithmic](../logarithms/), and the sign inside the [absolute value](../absolute-value/) is easily confused. The two forms are best memorised together: \\(\sec x + \tan x\\) for the cosine reciprocal, \\(\csc x - \cot x\\) for the sine reciprocal.

- - -
## Flowchart

- `Integral to solve`
  - **IF** the integrand is a single trigonometric or hyperbolic function
    - _integrate directly_
      apply the corresponding standard formula from the summary list
  - `ELSE IF` the integrand is a single power \\( \sin^{n} x \\) or \\( \cos^{n} x \\)
    - **IF** the exponent \\( n \\) is even
      - _apply the power-reduction identities_
        rewrite each squared term using
        \\[\begin{align*}
        \sin^{2} x &= \frac{1 - \cos 2x}{2} \\\\[3pt]
        \cos^{2} x &= \frac{1 + \cos 2x}{2}
        \end{align*}\\]
      - _repeat until no even power remains_
        a residual squared term is reduced again, doubling the angle each time
      - _integrate term by term_
        the integrand is now a sum of expressions of the form \\( \cos kx \\)
    - `ELSE` the exponent \\( n \\) is odd
      - _detach one factor of the function_
        write \\( \sin^{n} x = \sin x \,(\sin^{2} x)^{k} \\) or the analogous form for cosine
      - _convert the remaining even power_
        use \\( \sin^{2} x + \cos^{2} x = 1 \\) to express it through the complementary function
      - _substitute_
        set \\( u = \cos x \\) or \\( u = \sin x \\), so the differential matches the detached factor
      - _integrate the polynomial in \\( u \\) and substitute back_
  - `ELSE IF` the integrand has the form \\( \sin^{m} x \cos^{n} x \\)
    - **IF** at least one exponent is odd
      - _detach one factor of the odd-power function_
        convert the remaining even power through the Pythagorean identity
      - _substitute with the complementary function_
        \\( u = \sin x \\) when cosine has the odd power, \\( u = \cos x \\) otherwise
      - _integrate the polynomial in \\( u \\) and substitute back_
    - `ELSE` both exponents are even
      - _apply the power-reduction identities to every squared term_
        the identity \\( \sin x \cos x = \frac{1}{2}\sin 2x \\) often shortens the work
      - _integrate term by term_
        the integrand reduces to a sum of expressions of the form \\( \cos kx \\)
  - `ELSE IF` the integrand is \\( \sec x \\) or \\( \csc x \\)
    - _multiply by a fraction equal to_ \\( 1 \\)
      use \\( \frac{\sec x + \tan x}{\sec x + \tan x} \\) for the secant, \\( \frac{\csc x - \cot x}{\csc x - \cot x} \\) for the cosecant
    - _recognise the logarithmic form_
      the numerator is the derivative of the denominator, so the integral is \\( \int \frac{f'(x)}{f(x)}\,dx = \ln|f(x)| + c \\)
  - `ELSE`
    - _simplify the integrand first_
      expand, factor, or apply trigonometric identities to reach one of the cases above
    - _restart_