# Hyperbolic Sine and Cosine

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/hyperbolic-sine-and-cosine/

## Introduction to hyperbolic sine and cosine

We have seen that the [sine](../sine-and-cosine/) of an angle can be introduced geometrically by looking at how a point moves along the [unit circle](../unit-circle/). The hyperbolic sine, instead, is obtained by relating a point on the right branch of the equilateral [hyperbola](../hyperbola/):

\\[
X^{2} - Y^{2} = 1
\\]

to the area of a corresponding hyperbolic sector. For any real value \\(x\\), we select a point:

\\[
P(X_{P},\\, Y_{P})
\\]

on the branch with \\(X>0\\) such that the signed area enclosed by the \\(OX\\) axis, the segment from the origin to \\(P\\), and the portion of the hyperbola between \\((1,0)\\) and \\(P\\) is equal to \\(x/2\\). 

The notion of signed area makes it possible to accommodate both positive and negative values in a continuous way: when \\(x>0\\) the sector lies in the first quadrant, while for \\(x<0\\) it extends into the fourth quadrant, without breaking the correspondence between the parameter \\(x\\) and the position of \\(P\\). Once this point has been determined, the hyperbolic sine of \\(x\\) is simply its vertical coordinate:

\\[
\sinh(x) := Y_{P}
\\]

Specularly to what has just been shown for the hyperbolic sine, we can introduce the hyperbolic cosine by looking at the same equilateral hyperbola. Once the point: 
\\[
P(X_{P},\\, Y_{P})
\\]
has been identified as the one corresponding to a signed hyperbolic sector of area \\(x/2\\), the hyperbolic cosine of \\(x\\) is defined simply as its horizontal coordinate.

While \\(\sinh(x)\\) reflects how far the point rises or falls along the branch of the hyperbola, \\(\cosh(x)\\) captures its horizontal position:

\\[
\cosh(x) := X_{P}
\\]

In this geometric interpretation, the pair \\(\bigl(\cosh(x),\\, \sinh(x)\bigr)\\) represents the coordinates of the unique point \\(P\\) that produces the assigned sector \\(A\\).

- - -
## Fundamental hyperbolic identity

The hyperbolic sine and hyperbolic cosine satisfy a relationship that plays a role analogous to the [Pythagorean identity](../pythagorean-identity/). This relationship is known as the fundamental hyperbolic identity:

\\[
\cosh^{2} x - \sinh^{2} x = 1
\\]

From a geometric point of view, this equality expresses the fact that the point \\(\bigl(\cosh(x),\\, \sinh(x)\bigr)\\) lies exactly on the right branch of the equilateral hyperbola:

\\[
X^{2} - Y^{2} = 1
\\]

Here the horizontal coordinate \\(\cosh(x)\\) and the vertical coordinate \\(\sinh(x)\\) play roles similar to those of the adjacent and opposite sides in the unit-circle setting, but the geometry is governed by a hyperbola instead of a circle. The identity emerges from this construction: the coordinates of the point must satisfy the defining equation of the hyperbola, and this is precisely what leads to \\(\cosh^{2} x - \sinh^{2} x = 1\\).

- - -
## Hyperbolic identities

+ \\[
\text{1. } \quad \sinh(2x) = 2\\,\sinh(x)\\,\cosh(x)
\\]

+ \\[
\text{2. } \quad \cosh(2x)
= 1 + 2\\,\sinh^{2}(x)
\\]

+ \\[
\text{3. } \quad \sinh(x+y)
= \sinh(x)\cosh(y) + \cosh(x)\sinh(y)
\\]

+ \\[
\text{4. } \quad \cosh(x+y)
= \cosh(x)\cosh(y) + \sinh(x)\sinh(y)
\\]

+ \\[
\text{5. } \quad \sinh(x-y)
= \sinh(x)\cosh(y) - \cosh(x)\sinh(y)
\\]

+ \\[
\text{6. } \quad \cosh(x-y)
= \cosh(x)\cosh(y) - \sinh(x)\sinh(y)
\\]

> Each identity reflects the deep algebraic symmetry of the hyperbolic functions. Their addition and double-angle formulas closely parallel the circular case, but follow the geometry of the equilateral hyperbola, where \\(\cosh(x)\\) and \\(\sinh(x)\\) arise as the coordinates of the point associated with a hyperbolic sector.

- - -
## Analytical expression of the hyperbolic sine

A first derivation comes directly from the [exponential function](../exponential-function/). If we look at how \\(e^{x}\\) and \\(e^{-x}\\) behave, we notice that they naturally split into a symmetric and an antisymmetric part. Writing them as:

\\[e^{x} = \cosh(x) + \sinh(x)\\]
\\[e^{-x} = \cosh(x) - \sinh(x)\\]

we can treat these two expressions as a simple system in the unknowns \\(\cosh(x)\\) and \\(\sinh(x)\\). Subtracting one equation from the other isolates the antisymmetric component, giving:

\\[
e^{x} - e^{-x} = 2\\,\sinh(x)
\\]

and therefore:

\\[
\sinh(x) = \frac{e^{x} - e^{-x}}{2}
\\]

---

A complementary way to obtain the same formula is to go back to geometry. The point \\((\cosh(x), \sinh(x))\\) belongs to the equilateral hyperbola:

\\[
X^{2} - Y^{2} = 1
\\]

Since we already know that the horizontal coordinate satisfies:

\\[
X = \cosh(x) = \frac{e^{x} + e^{-x}}{2}
\\]

we can plug this expression directly into the hyperbola’s equation and solve for \\(Y\\). We have:

\\[
Y^{2}
= X^{2} - 1
= \left(\frac{e^{x} + e^{-x}}{2}\right)^{2} - 1
\\]

Expanding the square and simplifying leads to:

\\[
Y^{2}
= \left(\frac{e^{x} - e^{-x}}{2}\right)^{2}
\\]

Taking the square root requires paying attention to the sign of \\(Y\\).

+ If \\(x > 0\\), the point lies in the first quadrant and \\(Y\\) is positive.  
+ If \\(x < 0\\), it lies in the fourth quadrant and \\(Y\\) is negative.

In both cases, the correct choice is:
\\[
Y = \frac{e^{x} - e^{-x}}{2}
\\]

Thus the analytical expression emerges naturally from the geometry of the hyperbola:

\\[
\sinh(x) = \frac{e^{x} - e^{-x}}{2}
\\]

- - -
## Analytical expression of the hyperbolic cosine

Compared to the derivation of the hyperbolic sine, there is another way to obtain the analytical expression of the hyperbolic cosine, and it emerges directly from the classical geometric construction. In this approach, we start from the computation of the signed area \\(A\\) of the hyperbolic sector on the right branch of the equilateral hyperbola. The integral that describes this area leads to the relation:

\\[
A = \frac{1}{2}\\,\ln\\!\bigl(X + \sqrt{X^{2}-1}\bigr)
\\]

This motivates the introduction of the hyperbolic parameter \\(x\\), which is defined so that it depends only on the horizontal coordinate \\(X\\):

\\[
x = \ln\\!\bigl(X + \sqrt{X^{2}-1}\bigr) = 2A
\\]

Once this link between the sector area and the coordinate \\(X\\) has been established, we can reverse the relation to express \(X\) in terms of \(x\). Exponentiating gives:

\\[
X + \sqrt{X^{2}-1} = e^{x}
\\]

and from here we isolate the square root:

\\[
\sqrt{X^{2}-1} = e^{x} - X
\\]

Squaring both sides and simplifying the resulting expression shows that the admissible solution must satisfy:

\\[
X = \frac{e^{x} + e^{-x}}{2}
\\]

This value is therefore taken as the analytical definition of the hyperbolic cosine:

\\[
\cosh(x) = \frac{e^{x} + e^{-x}}{2}
\\]

- - -
## Analytical hyperbolic definitions

+ \\[
\text{1. } \quad \sinh(x)
= \frac{e^{x} - e^{-x}}{2}
\\]

+ \\[
\text{2. } \quad \cosh(x)
= \frac{e^{x} + e^{-x}}{2}
\\]

> These analytic definitions express the hyperbolic sine and cosine directly in terms of the [exponential function](../exponential-function/). Their symmetry follows from the structure of the equilateral hyperbola.

- - -
## Hyperbolic sine and cosine function

The hyperbolic sine function \\(f(x) = \sinh(x)\\) associates each [real number](../types-of-numbers/) \\(x\\) with a value derived from the exponential function. Unlike the circular sine, it does not oscillate: its graph grows exponentially for large positive or negative values of \\(x\\), crossing the origin with slope \\(1\\). The function \\(f(x) = \sinh(x)\\) is defined for all real numbers, and its range also spans the entire real line.

+ Domain: \\(x \in \mathbb{R}\\)  
+ Range: \\(y \in \mathbb{R}\\)  
+ Periodicity: not periodic; grows exponentially as \\(|x|\\) increases  
+ Parity: [odd](../even-and-odd-functions/), \\(\sinh(-x) = -\sinh(x)\\)

- - -

The hyperbolic cosine function \\(f(x) = \cosh(x)\\) assigns to each real number \\(x\\) a value obtained from the symmetric part of the exponential function. Unlike the circular cosine, it is not periodic: its graph has a minimum at \\(x = 0\\), where \\(\cosh(0) = 1\\), and increases exponentially as the [absolute value](../absolute-value/) of \\(x\\) becomes larger. The function \\(f(x) = \cosh(x)\\) is defined for all real numbers, and its range is given by \\(\cosh(x) \geq 1\\).

+ Domain: \\( x \in \mathbb{R} \\)  
+ Range: \\( y \in \mathbb{R} : y \geq 1 \\)  
+ Periodicity: not periodic; grows exponentially as \\(|x|\\) increases  
+ Parity: [even](../even-and-odd-functions/), \\(\cosh(-x) = \cosh(x)\\)

- - -
## Relation to the circular sine and cosine

Hyperbolic sine and cosine originate from the geometry of the equilateral hyperbola: 
\\[
x^{2} - y^{2} = 1
\\]
where a hyperbolic sector determines a parameter \\(x\\). The point on the hyperbola associated with this area has coordinates:

\\[
X_{P} = \cosh(x) = \frac{e^{x} + e^{-x}}{2}
\\]
\\[
Y_{P} = \sinh(x) = \frac{e^{x} - e^{-x}}{2}
\\]

In the circular setting, the corresponding quantities arise from the [unit circle](../unit-circle/) of radius \\(1\\), where a central angle \\( \theta \\) determines the circular [sine and cosine](../sine-and-cosine/), identified by the point:
\\[
P(X_{P}, Y_{P}) = P(\cos\theta,\\, \sin\theta)
\\]

> Both constructions follow the same basic idea: whether on a circle or on a hyperbola, a sector picks out a point on the curve. In the circular case this leads to the familiar sine and cosine, while in the hyperbolic case it gives the hyperbolic sine and cosine, which mirror the circular behaviour but within the geometry of the hyperbola.

