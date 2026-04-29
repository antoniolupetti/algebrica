# Complex Numbers

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/complex-numbers-introduction/

## Introduction 

Complex numbers arise to overcome the limitations of the set of [real numbers](../types-of-numbers) \\(\mathbb{R}\\), particularly the impossibility of taking even-indexed roots of negative numbers. One major consequence of this restriction is the inability to determine the solutions of a [quadratic equation](../quadratic-equations) with a negative [discriminant](../quadratic-formula).

In the set of [real numbers](../properties-of-real-numbers/) \\( \mathbb{R} \\), it is impossible to find a number whose square is \\(-1\\), since the square of any real number is always non-negative. Consequently, solving the equation \\( p(x) = x^2 + 1 = 0 \\) has no solutions in \\( \mathbb{R} \\). Indeed, this would lead to \\( x^2 = -1 \\), which is never satisfied in the set of real numbers \\( \mathbb{R} \\).

Starting from this very equation, we introduce the symbol \\( i \\), known as the imaginary unit, which is defined by the property: 
\\[ i^2 = -1 \\]

In this way, the equation \\( x^2 + 1 = 0 \\) has two distinct complex roots, given by \\( \pm i \\).

- - -
## Construction of the complex numbers

The introduction of complex numbers is sometimes treated as a matter of convenient notation, as though the symbol \\( i \\) were simply declared to satisfy \\( i^2 = -1 \\) and the matter were settled.This approach leaves an important question unanswered: does such an object actually exist, and if so, in what mathematical sense? The answer requires a short excursion into the construction of \\( \mathbb{C} \\) from the [real numbers](../real-numbers).

The starting point is the Cartesian product \\( \mathbb{R}^2 \\), the set of all ordered pairs of real numbers. Each element of this set is a pair of the form \\( (a, b) \\) with \\( a, b \in \mathbb{R} \\). This [set](../sets/) is the familiar Euclidean plane but here we want to equip it with an algebraic structure that makes it a [field](../fields/). To do so, addition and multiplication must be defined on \\( \mathbb{R}^2 \\).

Addition is defined componentwise. Given two pairs \\( (a, b) \\) and \\( (c, d) \\), their sum is the following:
\\[
(a,\\, b) + (c,\\, d) \\;=\\; (a + c,\\; b + d)
\\]
This is the natural extension of [vector](../vectors/) addition in the plane and presents no difficulty.

- - -

Multiplication is more subtle, and it is precisely here that the algebraic structure of the complex numbers diverges from that of \\( \mathbb{R}^2 \\) viewed merely as a [vector space](../vector-spaces/). The product of two pairs is defined as follows.
\\[
(a,\\, b) \cdot (c,\\, d) \\;=\\; (ac - bd,\\; ad + bc)
\\]
This rule is not arbitrary. It is the unique multiplication that turns \\( \mathbb{R}^2 \\) into a field extending \\( \mathbb{R} \\), as will become apparent once the connection with the standard algebraic notation is made explicit. The set \\( \mathbb{R}^2 \\) equipped with these two operations is denoted \\( \mathbb{C} \\) and its elements are called complex numbers.

The real numbers embed into \\( \mathbb{C} \\) through the identification \\( a \mapsto (a, 0) \\). One can verify directly that this map preserves both addition and multiplication, so \\( \mathbb{R} \\) sits inside \\( \mathbb{C} \\) as a subfield in a precise algebraic sense. The element \\( (0, 1) \\), which has no counterpart in this embedded copy of \\( \mathbb{R} \\), plays a distinguished role. Computing its square according to the multiplication rule gives the following result.
\\[
(0,\\, 1) \cdot (0,\\, 1) \\;=\\; (0 \cdot 0 - 1 \cdot 1,\\; 0 \cdot 1 + 1 \cdot 0) \\;=\\; (-1,\\; 0)
\\]
Under the identification above, the pair \\( (-1, 0) \\) corresponds to the real number \\( -1 \\). In other words, the element \\( (0, 1) \\) of \\( \mathbb{C} \\) satisfies exactly the relation that the symbol \\( i \\) is traditionally required to satisfy. This element is called the imaginary unit and is denoted \\( i \\), so that by definition \\( i = (0, 1) \\) and consequently \\( i^2 = -1 \\). The property \\( i^2 = -1 \\) is therefore not a postulate imposed on an undefined symbol: it is a theorem that follows from the multiplication rule on \\( \mathbb{R}^2 \\).

With this notation established, every complex number \\( (a, b) \\) can be decomposed as a combination of the two basis elements \\( (1, 0) \\) and \\( (0, 1) \\), which correspond to \\( 1 \\) and \\( i \\) respectively. The decomposition takes the familiar form \\( a + bi \\), since the following chain of equalities holds.
\\[
\begin{align}
(a,\\, b) &= (a,\\, 0) + (0,\\, b) \\\\[6pt]
&= a\cdot(1,\\, 0) + b\cdot(0,\\, 1) \\\\[6pt]
&= a + bi
\end{align}
\\]
The notation \\( z = a + bi \\) is thus a compact encoding of the ordered pair \\( (a, b) \\), with \\( a \\) called the real part and \\( b \\) the imaginary part of \\( z \\). These are written as \\( \mathrm{Re}(z) = a \\) and \\( \mathrm{Im}(z) = b \\). Note that the imaginary part is the real number \\( b \\), not the quantity \\( bi \\).

- - -

It remains to verify that the algebraic properties expected of a field actually hold. The verification is mechanical but worth summarising. Under addition, \\( \mathbb{C} \\) forms an abelian [group](../groups/): commutativity and associativity are inherited directly from \\( \mathbb{R} \\), the additive identity is \\( (0, 0) \\), and the additive inverse of \\( (a, b) \\) is \\( (-a, -b) \\). 

Multiplication is also commutative and associative, as can be confirmed by direct computation, and the multiplicative identity is \\( (1, 0) \\). The distributive law holds. The only property requiring genuine attention is the existence of multiplicative inverses for nonzero elements. Given \\( (a, b) \neq (0, 0) \\), one checks that its multiplicative inverse is the following pair.
\\[
(a,\\, b)^{-1} \\;=\\; \left(\frac{a}{a^2 + b^2},\\; \frac{-b}{a^2 + b^2}\right)
\\]
The denominator \\( a^2 + b^2 \\) is strictly positive when \\( (a, b) \neq (0, 0) \\), which ensures the formula is well defined for every nonzero complex number. The conclusion is that \\( \mathbb{C} \\), as constructed, is a field. Moreover, since \\( \mathbb{R} \\) embeds into it as a subfield, \\( \mathbb{C} \\) is an extension field of \\( \mathbb{R} \\). This is the precise mathematical sense in which the complex numbers extend the real number system.

One may also observe that, as a vector space over \\( \mathbb{R} \\), the field \\( \mathbb{C} \\) has dimension two, with basis \\( \{1, i\} \\). This two-dimensionality is what makes the geometric interpretation in the complex plane so natural: the real and imaginary parts of a complex number serve as coordinates with respect to this basis. 

The construction just described also generalises: replacing \\( \mathbb{R} \\) with an arbitrary field \\( F \\) and seeking an extension in which a chosen irreducible [polynomial](../polynomials/) has a root leads to the broader theory of field extensions, of which \\( \mathbb{C} \cong \mathbb{R}[x]/(x^2 + 1) \\) is the simplest and most important example.

- - -
## Definition

A complex number \\( z \\) is a number of the form \\( z = a + bi \\), where \\( a \\) and \\( b \\) are real numbers. The set of complex numbers is denoted by \\( \mathbb{C} \\) and is formally defined as follows.
\\[
\mathbb{C} := \{ z = a + ib \mid a, b \in \mathbb{R}\}
\\]
Let \\( z \\) be any complex number. The quantity \\( a \\) is referred to as the real part of \\( z \\) and is denoted by \\( \mathrm{Re}(z) \\), while \\( b \\) is called the imaginary part of \\( z \\) and is denoted by \\( \mathrm{Im}(z) \\):
\\[
z = a + ib \quad \rightarrow \quad
\begin{cases} 
\mathrm{Re}(z) = a \\\\[0.6em] 
\mathrm{Im}(z) = b \\\\
\end{cases}
\\]
+ The representation \\( z = a + ib \\) is called the algebraic form of a complex number. As established in the construction above, the complex number \\( a + bi \\) is the ordered pair \\( (a, b) \in \mathbb{R} \times \mathbb{R} \\), and the set \\( \mathbb{C} \\) coincides with the Cartesian product \\( \mathbb{R} \times \mathbb{R} \\) equipped with the operations defined there.
+ The complex number \\( z = 2 + 3i \\) has a real part of \\( 2 \\) and an imaginary part of \\( 3 \\).
+ Numbers of the form \\( z = ib \\) are called purely imaginary numbers.

- - -

While the algebraic form is the most familiar representation of complex numbers, an alternative and often more powerful way to express them is through their polar [trigonometric form](../complex-numbers-trigonometric-form):
\\[z = r (\cos\theta + i\sin\theta) \\]
Another representation is the [exponential form](https://algebrica.org/complex-numbers-exponential-form/):
\\[z = r e^{i\theta} \\]

- - -
## Complex plane

Due to the structure of the set \\( \mathbb{C} \\) as a Cartesian product, complex numbers can be represented geometrically in the complex plane (also known as the Gaussian or Argand plane), where the real part corresponds to the \\( x \\)-coordinate and the imaginary part corresponds to the \\( y \\)-coordinate. Thus, the complex number:

\\[ z = x + iy \\] 

can be represented as the point \\( (x, y) \\) in the plane, which is known as the Gaussian plane (or complex plane).

A purely imaginary number is represented by the ordered pair \\( i = (0,1) \\).

- - -
## Conjugate and modulus

Given the complex number \\( z = a + bi \\), the conjugate of \\( z \\) is defined as the complex number:

\\[ \overline{z} = a - bi \\] 

\\( \overline{z} \\) is represented in the complex plane by the point symmetric to \\( z \\) with respect to the \\( x \\)-axis.

Given the complex number \\( z = a + bi \\), the modulus of \\( z \\) is defined as:  

\\[
|z| = \sqrt{a^2 + b^2} 
\\]

It represents the distance from the origin to the point \\( (a, b) \\) in the complex plane. This definition is directly derived from the [Pythagorean theorem](../pythagorean-theorem/), since the modulus corresponds to the hypotenuse of a right triangle with legs of lengths \\( |a| \\) and \\( |b| \\):

\\[
|z|^2 = a^2 + b^2
\\] 

- - -
## Example 

Let’s consider the complex number \\(z = 3 + 2i\\). Using the modulus formula, we substitute \\( a = 3 \\) and \\( b = 2 \\):

\\[|z| = \sqrt{3^2 + 2^2} = \sqrt{9 + 4} = \sqrt{13}\\]

Thus, the modulus of \\( z = 3 + 2i \\) is:

\\[|z| = \sqrt{13} \approx 3.61 \\]

> This value represents the distance of \\( z \\) from the origin in the complex plane for the complex number \\(3 + 2i\\).

- - -
## Argument

The argument of a complex number \\( z = a + bi \\) is the angle \\( \theta \\) formed between the positive real axis and the segment connecting the origin to the point \\( (a, b) \\) in the complex plane. It is measured in radians, counterclockwise from the positive real axis, and is denoted by \\( \arg(z) \\).

The argument is not uniquely determined: any two angles differing by an integer multiple of \\( 2\pi \\) describe the same geometric direction. To resolve this ambiguity, one typically works with the principal argument, denoted \\( \mathrm{Arg}(z) \\), which is the unique value of \\( \theta \\) satisfying the following condition.
\\[
-\pi < \mathrm{Arg}(z) \leq \pi
\\]

Computing the argument requires care, because the naive formula \\( \theta = \arctan(b/a) \\) is insufficient: the arctangent function returns values only in the interval \\( (-\pi/2,\, \pi/2) \\), which covers only the right half of the complex plane and fails entirely when \\( a = 0 \\). The correct determination of \\( \theta \\) depends on the quadrant in which \\( (a, b) \\) lies, and must be handled case by case.

When \\( a > 0 \\), the point lies in the right half-plane and the principal argument is given by the [arctangent](../arctangent-and-arccotangent/).
\\[
\mathrm{Arg}(z) = \arctan\\!\left(\frac{b}{a}\right)
\\]
When \\( a < 0 \\) and \\( b \geq 0 \\), the point lies in the second quadrant, and a correction of \\( \pi \\) must be added to bring the angle into the correct range.
\\[
\mathrm{Arg}(z) = \arctan\\!\left(\frac{b}{a}\right) + \pi
\\]
When \\( a < 0 \\) and \\( b < 0 \\), the point lies in the third quadrant, and the correction is \\( -\pi \\).
\\[
\mathrm{Arg}(z) = \arctan\\!\left(\frac{b}{a}\right) - \pi
\\]
When \\( a = 0 \\), the point lies on the imaginary axis and the arctangent is undefined. In this case the argument is determined directly from the sign of \\( b \\): if \\( b > 0 \\) then \\( \mathrm{Arg}(z) = \pi/2 \\), and if \\( b < 0 \\) then \\( \mathrm{Arg}(z) = -\pi/2 \\). The case \\( z = 0 \\) is excluded, since the argument of the origin is undefined.

- - -

As an illustration, consider the complex number \\( z = -1 + i \\). Its real part is negative and its imaginary part is positive, so the point lies in the second quadrant. Applying the arctangent to the ratio \\( b/a = 1/(-1) = -1 \\) gives \\( \arctan(-1) = -\pi/4 \\), which falls in the fourth quadrant and is therefore incorrect. Since \\( a < 0 \\) and \\( b \geq 0 \\), the correction of \\( +\pi \\) must be applied, yielding the following.
\\[
\mathrm{Arg}(z) = -\frac{\pi}{4} + \pi = \frac{3\pi}{4}
\\]
This value is consistent with the geometric position of \\( z = -1 + i \\): the point lies at equal distances from both axes in the second quadrant, forming an angle of \\( 135° \\) with the positive real axis.

- - -
## Properties of \\(\mathbb{C}\\)

The [sum and product](../complex-number-operations) of complex numbers satisfy the associative, commutative, and distributive properties, just like the set of real numbers. 
Associative property for sum and product. When adding or multiplying complex numbers, the way in which the numbers are grouped does not affect the result.
\\[(z_1 + z_2) + z_3 = z_1 + (z_2 + z_3) \\] 
\\[(z_1 \cdot z_2) \cdot z_3 = z_1 \cdot (z_2 \cdot z_3) \\]
Commutative property. The order in which two complex numbers are added or multiplied does not change the result.
\\[z_1 + z_2 = z_2 + z_1 \\] 
\\[z_1 \cdot z_2 = z_2 \cdot z_1 \\]
Distributive property. Multiplying a number by a sum gives the same result as multiplying each addend individually and then adding the products.
\\[z_1 \cdot (z_2 + z_3) = z_1 \cdot z_2 + z_1 \cdot z_3 \\]
- - -
The complex number \\( 0 + 0i \\) is the additive identity in \\( \mathbb{C} \\), since for every complex number \\( z = a + bi \\), we have:
\\[
\begin{align}
z + (0 + 0i) &= (a + bi) + (0 + 0i) \\\\[6pt]
&= (a + 0) + (b + 0)i \\\\[6pt]
&= a + bi \\\\[6pt]
&= z 
\end{align}
\\]
The complex number \\( 1 + 0i \\) is the multiplicative identity in \\( \mathbb{C} \\), since for every complex number \\( z = a + bi \\), we have:
\\[
\begin{align}
z \cdot (1 + 0i) &= (a + bi) \cdot (1 + 0i) \\\\[6pt]
&= a \cdot 1 + a \cdot 0i + bi \cdot 1 + bi \cdot 0i \\\\[6pt]
&= a + bi \\\\[6pt]
&= z 
\end{align}
\\]
- - -
The opposite of \\( a + bi \\) is the complex number:
\\[-(a + bi) = -a - bi \\]
The reciprocal of a nonzero complex number \\( z = a + bi \\) is the complex number:
\\[\frac{1}{z} = \frac{a}{a^2 + b^2} - \frac{b}{a^2 + b^2} i \\]
Complex numbers of the form \\( z = a + 0i \\), where the imaginary part is zero, are precisely the real numbers.
- - -
The set of complex numbers \\( \mathbb{C} \\) cannot be ordered in a way that is compatible with addition and multiplication. If there existed a total order \\( \leq \\) on \\( \mathbb{C} \\), we should be able to compare \\( i \\) with \\( 0 \\). There are two possible cases:  
+ If \\( i > 0 \\), then multiplying both sides by \\( i \\) gives \\( i^2 = -1 > 0 \\), which is a contradiction.  
+ If \\( i < 0 \\), multiplying both sides by \\( i \\) again leads to the same contradiction: \\( -1 > 0 \\).  
Since neither case is valid, no total order on \\( \mathbb{C} \\) can be defined.