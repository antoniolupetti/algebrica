---
title: Mathematical Foundations
source: https://algebrica.org/mathematical-foundations/
license: CC BY-NC 4.0
tags:
  - algebra
  - calculus
  - foundations
  - learning
  - trigonometry
---


## An uphill road

It takes many years to develop a broad understanding of the fundamental concepts of mathematics. It is a long journey, full of obstacles, that begins in the first years of school and ends with the completion of secondary education, by which time students should have acquired enough knowledge to approach their first university exams with confidence. The mathematics taught at school is far from trivial, yet, in hindsight, it is not as insurmountable as it seems when we first encounter certain topics. It requires commitment, discipline, concentration, memory and solitude: no different from any other subject we wish to master.

School curricula often set a demanding pace across many subjects, and the time devoted to each is mostly consumed by the rush from one assessment to the next, with our eyes on the end of the year and the hope of reaching it with respectable grades. We therefore acquire knowledge without having time to consolidate it.

This is not the wrong way to behave. It is sheer mental survival.

Time, meanwhile, is not on our side. The brain is built to forget, and it does a very good job with mathematical formulas. We have all probably studied to pass an exam, only to discover within a few weeks that we remember almost nothing. This is perfectly normal, because that is how most of us work. Memories fade quickly, and what we learn by rote soon slips away when we have no opportunity to recall and use it in everyday life.

This is known as the forgetting curve, and when something is lost, returning to it can be as demanding as tackling it for the first time, because we have to reconstruct its meaning and recover the lost connections. It is a demanding mental process that can be frustrating.

## Before giving up

In the late 1990s, computer engineering was among the most sought-after university degrees, driven by the promise of a future increasingly taking shape on computer screens. The idea excited me, and I decided to enroll. I had attended a secondary school specializing in classical studies, and my first year at university was brutal. Apart from a programming exam using Turbo Pascal, there was very little computer science. What I needed was an understanding of mathematical analysis and linear algebra, and I knew very little of either. A few months later, I realized I was sailing through rough waters, in command of a ship I did not know how to steer, afraid it might sink at any moment.

I gave it everything I had, but it did not work.

On a hot day in mid-June, thoroughly discouraged, I asked to meet with the professor teaching the analysis course. I called the department from a public telephone booth outside the red-brick buildings with blue roofs that housed the classrooms, and they put me through to him. He told me to come and see him immediately. At that moment, I wanted to disappear. He usually stayed behind after lectures to answer our questions, but I was afraid of his judgment and had always been too embarrassed to speak to him. Looking back years later, I think I was so desperate that I felt I had nothing left to lose, and that this helped me overcome every hesitation.

That day I found myself alone with him, sitting opposite him across a desk covered in papers. I gathered my courage and told him about my difficulties. He listened and told me that I was not the first and would not be the last, but that, as he told everyone, it was too early to give up. Perhaps I could allow myself another attempt. Then he gave me a list of prerequisite topics to study before the start of the new semester and urged me to keep studying them until I had mastered them.

I left feeling relieved, convinced that I lacked the foundations rather than the ability, and I was determined to acquire them.

Ever since I was little, I had spent my summers in my grandmother's village, a medieval hilltop settlement not far from Rome, dating back to around the year 1000, with stone buildings clustered along narrow alleys where no cars pass and windows stand open, their sills blooming with red geraniums. With my bag of books and lecture notes, I decided to retreat there, away from every distraction. In the mornings, I got up early, made coffee and began studying at a small table I had set up on the shaded terrace by the entrance. My grandmother went out to run her errands and returned at lunchtime. She almost always cooked me a plate of pasta with tomato sauce and a thin slice of meat with tomatoes.

What I remember of that summer is the scent of basil on the plates.

The first three days were a test of discipline. Then I began to develop a routine and a method and, with them, the sense that perhaps I could succeed. I have told this story in [a separate post](../learning-mathematics/), but what I have not explained is how I caught up on everything I was missing, had forgotten or simply did not know.

## A map of the territory

I want to begin by saying that no single study method works for everyone, so each person must follow a path suited to their abilities. The route may vary, but some signposts along the way can still hold true. So, if you need to rebuild your mathematical foundations to tackle your first year at university, you can follow this map, exploring the territory as you see fit.

The first topic to focus on is [number sets](../types-of-numbers/) and their fundamental properties, starting with the [natural numbers](../natural-numbers/) and moving through the [integers](../integers/), [rational numbers](../rational-numbers/), [real numbers](../real-numbers/) and [irrational numbers](../irrational-numbers/), in the following order:

$$
\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}, \qquad \mathbb{I} \subset \mathbb{R}
$$

The real numbers deserve particular attention because they form the set in which real analysis is developed, from the study of limits to the calculation of derivatives and integrals. At this initial stage, you can leave aside the [complex numbers](../complex-numbers/), which will be useful later.

Since number sets are particular instances of sets, it is worth studying [cardinality](../cardinality-and-countable-sets/), families of sets and [set operations](../sets/) alongside them, together with [De Morgan's laws](../de-morgan-laws/), which recur in the solution of many problems.

$$
\begin{align}
(A \cup B)^c &= A^c \cap B^c \\[6pt]
(A \cap B)^c &= A^c \cup B^c
\end{align}
$$

After sets, it is useful to tackle [first-order logic](../first-order-logic/), beginning with the [fundamental connectives](../propositional-logic/) and their truth tables (in the table below, T means true and F means false):

| $p$ | $q$ | $\neg p$ | $p\land q$ | $p\lor q$ | $p\Rightarrow q$ | $p\Leftrightarrow q$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| T | T | F | T | T | T | T |
| T | F | F | F | T | F | F |
| F | T | T | F | T | T | F |
| F | F | T | F | F | T | T |

Before going any further, it is essential to study the [principle of mathematical induction](../principle-of-mathematical-induction/), which allows us to prove a property for all natural numbers from an initial value $n_0.$ We verify that the property holds for $n_0$ and prove that, if it holds for an arbitrary natural number $n\ge n_0,$ then it also holds for the next:

$$
\bigl[P(n_0)\land\forall n\ge n_0,\ (P(n)\Rightarrow P(n+1))\bigr]\Rightarrow\forall n\ge n_0,\ P(n)
$$

Next, we can move on to [powers](../powers/), memorizing their fundamental properties, which allow us to rewrite them in terms of their exponents and simplify the algebraic expressions in which they appear. For example:

$$
\begin{align}
a^m a^n &= a^{m+n} \\[6pt]
\frac{a^m}{a^n} &= a^{m-n} \\[6pt]
(a^m)^n &= a^{mn} \\[6pt]
&\vdots
\end{align}
$$

[Logarithms](../logarithms/) allow us to recover the exponent of a power, so it is worth studying them alongside powers, understanding and memorizing their properties. Among these, the change-of-base formula is particularly useful for rewriting and simplifying logarithmic expressions:

$$
\log_a x = \frac{\log_b x}{\log_b a}
$$


Keep in mind that powers and logarithms together involve about a dozen very simple properties that, once learned, will help solve problems in many areas.

It is then worth reviewing [radicals](../radicals/), their connection with rational exponents and rationalization, together with algebraic fractions, the conditions under which they are defined and the rules for simplifying them and carrying out operations.

The [factorial](../factorial/) also deserves a mention (it is needed in combinatorics, [binomial coefficients](../binomial-coefficient/) and, later, [Taylor expansions](../limits-using-taylor-expansions/)); for a positive integer $n,$ it is the product of all integers from $1$ to $n:$

$$
n! =
\begin{cases}
n \cdot (n-1)! & \text{if } n \in \mathbb{N},\ n \gt 0 \\[6pt]
1 & \text{if } n = 0
\end{cases}
$$

The next step is to study [polynomials](../polynomials/) and their properties, paying particular attention to factorization and [division](../polynomial-division/), two useful tools for solving [polynomial equations](../polynomial-equations/). A polynomial of degree $n$ with $a_n\neq 0$ has the form:

$$
P(x) = a_n x^n + a_{n-1}x^{n-1} + \cdots + a_1 x + a_0
$$

At this point, we can tackle [linear equations in one variable](../linear-equations/), including [those involving parameters](../linear-equations-with-parameters/), because they introduce the principles of equivalence and the reasoning needed to solve more complex equations. We can then move on to [quadratic equations](../quadratic-equations/), which pose no particular difficulties because they can be solved mechanically by factorization or with the [quadratic formula](../quadratic-formula/):

$$
x_{1,2} = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
$$

Geometrically, the graph of a quadratic function $y=ax^2+bx+c$ is a [parabola](../parabola/), and the real solutions of the equation $ax^2+bx+c=0$ are the x-coordinates of its intersections with the $x$-axis. The parabola can therefore be studied alongside quadratic equations. Keep in mind, too, that the parabola belongs to the family of [conic sections](../introduction-to-conics/), which can be studied together in greater depth at a later stage.

Returning to quadratic equations with real coefficients, these have real solutions if and only if the discriminant $\Delta=b^2-4ac$ is nonnegative. The case $\Delta\lt 0$ therefore provides an opportunity to introduce complex numbers and the fundamental theorem of algebra, which states that every polynomial of degree $n\ge 1$ with complex coefficients has exactly $n$ complex roots, counted with multiplicity.

For complex numbers, it is also useful to understand their geometric representation in the Argand plane. After studying trigonometry, we can return to the [trigonometric](../complex-numbers-trigonometric-form/) and [exponential forms](../complex-numbers-exponential-form/), shown here in advance, which express a complex number in terms of its modulus $r$ and argument $\theta:$

$$
\begin{align}
z &= r(\cos\theta+i\sin\theta) \\[6pt]
z &= re^{i\theta}
\end{align}
$$

To complete the study of polynomial equations, it is useful to tackle cubic equations and methods for reducing equations of higher degree. In particular, [synthetic division](../synthetic-division/) allows us to divide a polynomial $P(x)$ of degree $n$ by a factor $x-r,$ obtaining a quotient $Q(x)$ of degree $n-1$ and a remainder equal to $P(r):$

$$
P(x)=(x-r)Q(x)+P(r)
$$

If $r$ is a root, the remainder is zero and we obtain the factorization $P(x)=(x-r)Q(x).$ For a cubic equation, knowing one root therefore allows us to reduce the search for the other solutions to a quadratic equation.

Once we have finished studying polynomial equations, we can move on to [rational equations](../rational-equations/) with the unknown in a denominator, [radical equations](../irrational-equations/), [equations involving absolute values](../absolute-value-equations/) and, finally, [exponential](../exponential-equations/) and [logarithmic equations](../logarithmic-equations/). For each type, we need to understand how to determine the conditions under which the expressions are defined and distinguish equivalent transformations from those that require us to check the resulting solutions.

The next topic is [inequalities](../inequalities/), which require us to identify the values of the unknown for which one expression is greater than, less than, greater than or equal to, or less than or equal to another. [Sign analysis](../sign-analysis-in-inequalities/) is useful when solving them: when an expression is factored into a product or a quotient, we determine the sign of each factor and combine the results using the rules of signs.

At this point, it is useful to tackle trigonometry, starting with the [unit circle](../unit-circle/) and the geometric interpretation of [sine](../sine-function/), [cosine](../cosine-function/), [tangent](../tangent-function/) and [cotangent](../cotangent-function/), with the [fundamental identities](../trigonometric-identities/):

$$
\begin{align}
\cos^2\theta+\sin^2\theta &= 1 \\[6pt]
\tan\theta &= \frac{\sin\theta}{\cos\theta} \\[6pt]
\cot\theta &= \frac{\cos\theta}{\sin\theta}
\end{align}
$$

We can then move on to the [inverse functions](../inverse-function/), defined by restricting the domains of the trigonometric functions:

$$
\begin{align}
y &= \arcsin x \\[6pt]
y &= \arccos x \\[6pt]
y &= \arctan x \\[6pt]
&\vdots
\end{align}
$$

Since trigonometry allows us to solve triangles, it is worth reviewing their properties, paying particular attention to [right triangles](../right-triangle-trigonometry/). If $a$ and $b$ are the legs, $c$ is the hypotenuse and $\alpha$ is the angle opposite $a,$ we have some fundamental identities that are worth memorizing.

$$
\begin{align}
a^2+b^2 &= c^2 \\[6pt]
\sin\alpha &= \frac{a}{c} \\[6pt]
\cos\alpha &= \frac{b}{c} \\[6pt]
&\vdots
\end{align}
$$

Finally, we can introduce the hyperbolic functions:

$$
\begin{align}
\sinh x &= \frac{e^x-e^{-x}}{2} \\[6pt]
\cosh x &= \frac{e^x+e^{-x}}{2} \\[6pt]
\tanh x &= \frac{\sinh x}{\cosh x} \\[6pt]
&\vdots
\end{align}
$$

Once we are familiar with the fundamental concepts of trigonometry, we can tackle [trigonometric equations](../trigonometric-equations/), in which the periodicity of the functions requires us to describe solutions as families that repeat at regular intervals. For example:

$$
\sin x=0\quad\Longleftrightarrow\quad x=k\pi,\qquad k\in\mathbb{Z}
$$

After studying equations and inequalities, we can move on to [systems of linear equations](../systems-of-linear-equations/) and inequalities. Solving a system means finding the values of the unknowns that simultaneously satisfy all its conditions. Two examples are:

$$
\begin{cases}
2x+y=5 \\
x-y=1
\end{cases}
\qquad
\begin{cases}
2x-1\gt 0 \\
x+2\le 5
\end{cases}
$$

In the first case, we seek the pairs $(x,y)$ common to both equations; in the second, the values of $x$ that belong to the intersection of the solution sets of the two inequalities. Solving systems can become demanding as the number of equations and unknowns increases, so, beyond elementary methods such as substitution, we need to study [matrices](../matrices/), which allow us to represent a system of linear equations in the form:

$$
A\mathbf{x}=\mathbf{b}
$$

We therefore need to study matrix algebra and [Gaussian elimination](../gaussian-elimination/), which allows us to solve systems through row operations. For square matrices, calculating the [determinant](../determinant/) is also useful because, if $\det A\neq 0,$ the matrix is [invertible](../inverse-matrix/) and the system has a unique solution. Otherwise, the system may have no solutions or infinitely many. Solving systems is perhaps the most demanding topic covered so far and requires plenty of practice to understand the methods and learn to apply them confidently.

After this overview, we can return to conic sections, already introduced through the parabola when studying quadratic equations. Conic sections are curves obtained by intersecting a plane with a circular cone, whose nondegenerate cases are the [circle](../circumference/), [ellipse](../ellipse/), parabola and [hyperbola](../hyperbola/). In the Cartesian plane, their general equation is:

$$
Ax^2+Bxy+Cy^2+Dx+Ey+F=0
$$

At this point, we can introduce the [concept of a function](../functions/), learn to determine its [domain](../determining-the-domain-of-a-function/) and study the properties and graphs of the most common elementary functions.

The next step is to [study limits](../limits/), which describe the behavior of a function as the variable approaches a point or tends to infinity. We need to understand their definition, know the [algebra of limits](../algebra-of-limits/) and study the [uniqueness, sign preservation and squeeze theorems](../theorems-on-limits/). Since not all limits can be evaluated by direct substitution, it is useful to learn to recognize [standard limits](../remarkable-limits/) and rewrite expressions in these familiar forms, for example:

$$
\begin{gathered}
\lim_{x\to 0}\frac{\sin x}{x} = 1 \\[6pt]
\vdots
\end{gathered}
$$
The seven [indeterminate forms](../indeterminate-forms/) deserve separate treatment, since the behavior of the individual terms is not enough to determine the limit of the expression:

$$
\begin{gathered}
\frac{0}{0} \\[6pt]
\frac{\infty}{\infty} \\[6pt]
0\cdot\infty \\[6pt]
\vdots
\end{gathered}
$$

To resolve them, we use factorization, rationalization, standard limits and [asymptotic comparison](../hierarchy-of-growth-rates/), or other specific techniques such as [l'Hôpital's rule](../hopital-rule/) or, in more advanced treatments beyond the scope of this discussion, Taylor expansions.

After tackling limits and [continuity](../continuous-functions/), we can move on to differential calculus. The [derivative of a function](../derivatives/) at an interior point $x_0$ of its domain is defined, when the limit exists and is finite, as the limit of the [difference quotient](../difference-quotient/):

$$
f'(x_0)=\lim_{h\to 0}\frac{f(x_0+h)-f(x_0)}{h}
$$

To calculate derivatives, we need to memorize those of the main elementary functions and know the [algebraic rules of differentiation](../differentiation-rules/). We can then move on to [higher-order derivatives](../higher-order-derivatives/), obtained by repeatedly differentiating the function, particularly the second derivative, which allows us to study [concavity](../convexity-and-concavity-of-functions/) and identify any inflection points on the graph of a function.

These tools come together in the [analysis of a function](../analyzing-the-graphs-of-functions/): limits allow us to identify [asymptotes](../asymptotes/), the sign of the first derivative describes [monotonicity](../increasing-and-decreasing-functions/) and changes in its sign allow us to recognize [local maxima and minima](../maximum-minimum-and-inflection-points/), while the second derivative helps us study concavity and inflection points.

After derivatives, it is time for [indefinite integrals](../indefinite-integrals/), which represent families of antiderivatives, that is, functions $F$ such that $F'(x)=f(x).$ Indefinite integration is the inverse operation of differentiation and requires us to know the main integration formulas to obtain results of the form:

$$
\int f(x) \ dx=F(x)+c
$$

Alongside the basic formulas, we need to learn the main techniques of integration, such as substitution and [integration by parts](../integration-by-parts/), which are needed to evaluate more complex integrals. We can then move on to [definite integrals](../definite-integrals/), which measure the accumulation of a quantity over a specified interval and geometrically represent the signed area between the graph of the function and the $x$-axis:

$$
\int_a^b f(x) \ dx=F(b)-F(a)
$$

The topics presented so far provide a foundation for approaching the first year of university studies in scientific subjects with greater confidence. Some secondary-school programs also cover [sequences](../sequences/) and [numerical series](../series/), which, however, require further study beyond this introductory overview and have therefore been deliberately omitted.

As I have already said, this is only a map of sometimes difficult terrain, which each person crosses at their own pace and with the experience they bring. I therefore suggest using it as a general reference, adapting the pace and depth of your study to your needs. The topics listed remain basic knowledge to acquire before tackling more advanced mathematics.
