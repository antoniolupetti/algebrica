# Integration by Parts

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/integration-by-parts/

## The method of integration by parts

The method of integration by parts allows us to rewrite the integral of the product of two [functions](../functions/) in a more convenient form. For [indefinite integrals](../indefinite-integrals), the formula is:

\\[
\int f(x)g'(x)\\, dx = f(x)g(x) - \int f'(x)g(x)\\, dx + c
\\]

For [definite integrals](../definite-integrals), the formula extends as:

\\[
\int_a^b f(x)g'(x)\\, dx = \Big[f(x)g(x)\Big]_a^b - \int_a^b f'(x)g(x)\\, dx
\\]

where \\( \Big[f(x)g(x)\Big]_a^b = f(b)g(b) - f(a)g(a) \\) is the boundary term, which must be evaluated. 

In both cases, \\( f \\) and \\( g \\) are assumed to be differentiable on the [interval](../intervals/) of integration. The method is conceptually simple, but it requires practice to identify which function should be differentiated and which should be integrated in order to simplify the expression.

> In some cases, integration by parts must be applied more than once to completely evaluate the integral. One should proceed carefully, since repeated applications may increase the length of the computation and make sign errors more likely.

- - -
## Derivation of the formula

The integration by parts formula follows directly from the product rule for [derivatives](../derivatives). Start from:

\\[
\frac{d}{dx}\big(f(x)g(x)\big) = f'(x)g(x) + f(x)g'(x)
\\]

Integrating both sides with respect to \\( x \\):

\\[
\int \frac{d}{dx}\big(f(x)g(x)\big)\\,dx = \int f'(x)g(x)\\,dx + \int f(x)g'(x)\\,dx
\\]

The left-hand side is the integral of a derivative, which returns the original function 
up to a constant:

\\[
f(x)g(x) = \int f'(x)g(x)\\,dx + \int f(x)g'(x)\\,dx
\\]

Rearranging to isolate the second integral on the left:

\\[
\int f(x)g'(x)\\,dx = f(x)g(x) \\,\\, - \int f'(x)g(x)\\,dx + c
\\]

This is the integration by parts formula. In the compact notation \\( u = f(x) \\), \\( dv = g'(x)\\,dx \\), it takes the familiar form:

\\[
\int u\\,dv = uv \\,\\, - \int v\\,du
\\]

> In practice, integration by parts is useful when differentiating one factor makes it simpler, while the other can still be integrated without difficulty. The method often turns a complicated expression into something more manageable, and in many problems it can be applied repeatedly until the integral is reduced to a standard form.

- - -
## How to choose \\(u\\) and \\(dv\\)

The method is effective only if the new integral \\( \int v\\,du \\) is simpler than 
the original one. This depends entirely on how \\( u \\) and \\( dv \\) are assigned, 
so the choice is not arbitrary. A practical strategy is:

- Choose \\( u \\) as the factor that becomes simpler when differentiated.
- Choose \\( dv \\) as the remaining factor, so that \\( v = \int dv \\) is easy to compute.

- - -

A useful order for selecting \\( u \\) is the hierarchy known by the acronym LIATE:

+ Logarithmic functions
+ Inverse trigonometric functions
+ Algebraic expressions
+ Trigonometric functions
+ Exponential functions

The ordering reflects how these functions behave under differentiation. [Logarithmic](../logarithmic-function/) and inverse trigonometric functions simplify considerably when differentiated, making them natural candidates for \\( u \\). [Exponential functions](../exponential-function/), by contrast, remain essentially unchanged after differentiation and are generally better assigned to \\( dv \\).

> Choosing \\( u \\) according to this hierarchy often reduces the complexity of the remaining integral after a single application of the formula

- - -
## Most common mistakes

A few recurring mistakes are worth keeping in mind when applying integration by parts.

Choosing \\( dv \\) carelessly, in particular assigning to \\( dv \\) a factor whose integral \\( v \\) is harder to compute than the original integral, often makes the problem worse rather than better. If the resulting \\( \int v\,du \\) is more complex than what you started with, it is worth reconsidering the assignment before proceeding.

In the [definite integral](../definite-integrals/) version of the formula, the boundary term \\( uv \big|\_a^b \\) must be evaluated explicitly. Omitting it is one of the most common sources of incorrect results, particularly when the computation spans several lines and attention drifts toward the integral that follows.

Sign errors during differentiation are especially insidious in cyclic cases, where \\( \sin(x) \\) and \\( \cos(x) \\) alternate and a misplaced minus sign propagates through the entire calculation. Keeping track of signs at each step, rather than reconstructing them at the end, saves considerable time.

Finally, in the indefinite case, the constant of integration \\( C \\) must appear in the final result. After repeated applications of the formula it is easy to lose track of it, particularly when intermediate integrals are written without it. A reliable habit is to carry \\( C \\) explicitly only in the last step and to confirm its presence before writing the answer.

- - -
## Example 1

Let's consider an example by solving the following integral:

\\[
\int x^2 \ln(x) \\, dx
\\]

The integrand is a product of a logarithmic function and a [power](../powers) of \\( x \\). Following the LIATE hierarchy, \\( \ln(x) \\) takes priority and is assigned to \\( f \\), while \\( x^2 \\) is assigned to \\( g' \\):

\\[
f(x) = \ln(x) \quad \rightarrow \quad f'(x) = \frac{1}{x}
\\]

\\[
g'(x) = x^2 \quad \rightarrow \quad g(x) = \frac{x^3}{3}
\\]

Applying the formula, we obtain:

\\[
\begin{align}
\int x^2 \ln(x)\, dx
&= \ln(x)\cdot\frac{x^3}{3} - \int \frac{1}{x}\cdot\frac{x^3}{3}\\, dx + c \\\\[6pt]
&= \ln(x)\cdot\frac{x^3}{3} - \int \frac{x^2}{3}\\, dx + c
\end{align}
\\]

The remaining integral is a straightforward power rule application, considerably simpler than the original. Completing the calculation we have:

\\[
\ln(x)\cdot\frac{x^3}{3} - \frac{x^3}{9} + c
\\]

Factoring out \\( \frac{x^3}{3} \\) gives the final result in compact form:

\\[
\frac{x^3}{3}\left(\ln(x) - \frac{1}{3}\right) + c
\\]

- - -
## Example 2

Some integrals do not resolve after a single application of integration by parts. Instead, repeated application leads back to the original integral, a situation that, rather than signaling failure, opens the door to an algebraic resolution. The following example illustrates this technique. Solve the following integral:

\\[
\int e^x\sin(x)\\,dx
\\]

Denote the integral by \\( I \\):

\\[
I = \int e^x\sin(x)\\,dx
\\]

Following the LIATE hierarchy, the trigonometric function \\( \sin(x) \\) takes priority over the exponential, so we assign \\(u = \sin(x)\\), \\(dv = e^x\\,dx\\) from which:

\\[du = \cos(x)\\,dx\\]
\\[ v = e^x\\]

Applying the formula, we obtain:

\\[
I = e^x\sin(x) - \int e^x\cos(x)\\,dx
\\]

The new integral is no simpler in structure than the original. It still involves the product of \\( e^x \\) and a trigonometric function. We apply integration by parts a second time, denoting:

\\[
J = \int e^x\cos(x)\\,dx
\\]

and assigning with the previous choice \\(u = \cos(x)\\) and \\(dv = e^x\\,dx\\). We obtain:

\\[du = -\sin(x)\\,dx\\]
\\[v = e^x\\]

This gives:

\\[
J = e^x\cos(x) + \int e^x\sin(x)\\,dx = e^x\cos(x) + I
\\]

The original integral \\( I \\) has reappeared. Substituting back into the expression 
for \\( I \\):

\\[
I = e^x\sin(x) - \bigl(e^x\cos(x) + I\bigr)
\\]

Both occurrences of \\( I \\) now appear on the same equation. Collecting them on 
the left-hand side:

\\[
2I = e^x\sin(x) - e^x\cos(x)
\\]

Dividing through by \\(2\\) and adding the constant of integration:

\\[
I = \frac{e^x}{2}\bigl(\sin(x) - \cos(x)\bigr) + c
\\]

> The key observation is that the cyclic structure transforms an apparently endless recursion into a [linear equation](../linear-equations/) in \\( I \\), which can be solved directly. This technique applies whenever repeated integration by parts returns the original integral with a nonzero coefficient.

- - -

## Example 3

The following example illustrates the definite integral version of the formula. Compute:

\\[
\int_0^1 x\ln(x)\\, dx
\\]

The integrand is a product of a logarithmic function and a power of \\( x \\). Following the LIATE hierarchy, \\( \ln(x) \\) takes priority and is assigned to \\( f \\), while \\( x \\) is assigned to \\( g' \\):

\\[
f(x) = \ln(x) \quad \rightarrow \quad f'(x) = \frac{1}{x}
\\]

\\[
g'(x) = x \quad \rightarrow \quad g(x) = \frac{x^2}{2}
\\]

Applying the definite integral form of the formula:

\\[
\begin{align}
\int_0^1 x\ln(x)\\, dx
&= \left[\frac{x^2}{2}\ln(x)\right]_0^1 - \int_0^1 \frac{x^2}{2} \cdot \frac{1}{x}\\, dx \\\\[0.4em]
&= \left[\frac{x^2}{2}\ln(x)\right]_0^1 - \frac{1}{2}\int_0^1 x\\, dx
\end{align}
\\]

The boundary term requires care at \\( x = 0 \\). Since \\( \ln(1) = 0 \\) and \\( x^2\ln(x) \to 0 \\) as \\( x \to 0^+ \\), both endpoints vanish:

\\[
\left[\frac{x^2}{2}\ln(x)\right]_0^1 = 0
\\]

The remaining integral is a standard power rule application:

\\[
\frac{1}{2}\int_0^1 x\\, dx = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}
\\]

Therefore:

\\[
\int_0^1 x\ln(x)\\, dx = -\frac{1}{4}
\\]

> The [limit](../limits) \\( \lim_{x \to 0^+} x^2 \ln(x) = 0 \\) follows from the fact that [polynomial](../polynomials/) growth dominates [logarithmic](../logarithms/) decay near zero. This kind of boundary analysis is essential whenever the integrand is not defined at one of the endpoints.

- - -
## Flowchart
- `Integral to solve`
  - **IF** the integrand is a product of two functions \\( f(x) \cdot g'(x) \\)
    - _choose u and dv via LIATE_
      assign \\( u \\) to the factor that appears first in the hierarchy  
      logarithmic, innverse trigonometric, algebraic, trigonometric, exponential  
      assign \\( dv \\) to the remaining factor  
    - _compute \\( f'(x) \\) and \\( g(x) \\)_
      differentiate \\( u \\) and integrate \\( dv \\)
    - _apply the formula_
      \\(\int f\\,g'\\,dx = f(x)g(x) - \int f'(x)g(x)\\,dx + c\\)
    - **IF** the new integral \\( \int f'g\\,dx \\) is more complex than the original
      - _swap u and dv and re-apply_
        the goal is always a simpler remaining integral
    - `ELSE IF` the original integral reappears (cyclic case)
      - _collect \\( I \\) on both sides_
        repeated application leads back to the original integral with a nonzero coefficient
      - _solve the linear equation in \\( I \\)_
        divide through by the coefficient and add the constant of integration
    - `ELSE`
      - _evaluate \\( \int f'g\\,dx \\)_
        apply the appropriate standard formula, or repeat integration by parts if needed
      - **IF** the integral is definite
        - _evaluate the boundary term \\( \bigl[f(x)g(x)\bigr]\_a^b \\)_
          compute \\( f(b)g(b) - f(a)g(a) \\) explicitly  
          omitting this term is a common error
        - _the result is a number_
          no further manipulation is needed
      - `ELSE`
        - _write the antiderivative_
          \\( f(x)g(x) - \int f'(x)g(x)\,dx + c \\)
        - _verify that \\( c \\) is present_
          after repeated applications it is easy to lose track of the constant; add it explicitly at the last step
  - `ELSE`
    - _simplify the integrand first_
      expand, factor, apply trigonometric identities, or split into partial fractions
    - _restart_