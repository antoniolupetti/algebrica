
# Real Numbers

Source: algebrica.org — CC BY-NC 4.0
https://algebrica.org/real-numbers/

## Field and order structure

The real numbers are introduced as a structure characterised by a combination of algebraic and order properties. These properties determine their behaviour and distinguish it from all other numerical fields. The real numbers form a [field](../fields/) under addition and multiplication. This means that both operations are associative and commutative, multiplication distributes over addition, and every nonzero real number admits a multiplicative inverse. The additive identity is \\(0\\) and the multiplicative identity is \\(1\\). The algebraic axioms underlying this structure are discussed in detail in [Properties of Real Numbers](../properties-of-real-numbers/). Beyond its algebraic structure, \\(\mathbb{R}\\) carries a total order relation, denoted \\(<\\): for any two elements \\(x, y \in \mathbb{R}\\), exactly one of the following three relations holds:

\\[
x < y \qquad x = y \qquad y < x
\\]

The order is compatible with the field operations. 

+ If \\(x < y\\), then \\(x + z < y + z\\) for every \\(z \in \mathbb{R}\\)
+ If \\(x < y\\) and \\(z > 0\\) then \\(xz < yz\\)

A field equipped with a total order satisfying these compatibility conditions is an ordered field. Both \\(\mathbb{Q}\\) and \\(\mathbb{R}\\) are ordered fields (what separates the two is the completeness property introduced below).

- - -
## The real line

The real numbers admit a geometric interpretation that makes their order and completeness clear. Fix an arbitrary point on a straight line and label it \\(0\\). Fix a second point to its right and label it \\(1\\). Every real number \\(x\\) then corresponds to a unique point on the line: positive numbers lie to the right of \\(0\\), negative numbers to the left, at a distance from the origin equal to the [absolute value](../absolute-value/) \\(|x|\\). This correspondence is a bijection between \\(\mathbb{R}\\) and the points of the line and it preserves the order. \\(x < y\\) holds if and only if the point corresponding to \\(x\\) lies to the left of the point corresponding to \\(y\\).

- - -
## The completeness axiom

The property that distinguishes \\(\mathbb{R}\\) from \\(\mathbb{Q}\\) is completeness. It expresses the absence of gaps. Every position on the number line that could be approached by a [sequence](../sequences/) of rational numbers is actually occupied by a real number. The rational numbers, by contrast, leave the line with infinitely many holes, one for each irrational value.

The formulation relies on the notion of an upper bound. A subset \\(S \subseteq \mathbb{R}\\) is said to be bounded above if there exists a real number \\(M\\) such that \\(x \leq M\\) for every \\(x \in S\\). Such a number \\(M\\) is called an upper bound of \\(S\\). When a smallest upper bound exists, it is called the supremum of \\(S\\), or least upper bound, and is denoted \\(\sup S\\). 

The completeness axiom of the real numbers can be stated as follows: every non-empty subset of \\(\mathbb{R}\\) that is bounded above has a [supremum](../supremum-and-infimum/) in \\(\mathbb{R}\\). This statement is known as the least upper bound property. The rational numbers fail to satisfy it. To see why, consider the following set:

\\[
S = \\{ q \in \mathbb{Q} : q^2 < 2 \\}
\\]

This set is non-empty and bounded above within \\(\mathbb{Q}\\), yet it has no least upper bound in \\(\mathbb{Q}\\). The value \\(\sqrt{2}\\), which plays the role of \\(\sup S\\), is irrational and therefore absent from \\(\mathbb{Q}\\). In \\(\mathbb{R}\\), the number \\(\sqrt{2}\\) exists and one has \\(\sup S = \sqrt{2}\\).

A symmetric notion applies to sets bounded below. A subset \\(S \subseteq \mathbb{R}\\) is bounded below if there exists \\(m \in \mathbb{R}\\) such that \\(x \geq m\\) for all \\(x \in S\\). The greatest lower bound, or [infimum](../supremum-and-infimum/), is denoted \\(\inf S\\). The completeness axiom implies that every non-empty subset of \\(\mathbb{R}\\) bounded below has an infimum in \\(\mathbb{R}\\).

- - -
## The Archimedean property

A consequence of completeness is the Archimedean property of \\(\mathbb{R}\\). It states that for every real number \\(x\\), there exists a [natural number](../natural-numbers/) \\(n\\) such that \\(n > x\\). Equivalently, the set of natural numbers \\(\mathbb{N}\\) is not bounded above in \\(\mathbb{R}\\). The argument runs as follows. 

+ Suppose, for contradiction, that \\(\mathbb{N}\\) were bounded above in \\(\mathbb{R}\\). 
+ By the completeness axiom, \\(\mathbb{N}\\) would then have a supremum that we call \\(s = \sup \mathbb{N}\\). 
+ Since \\(s - 1 < s\\), the number \\(s - 1\\) is not an upper bound of \\(\mathbb{N}\\), so there exists \\(n \in \mathbb{N}\\) with \\(n > s - 1\\). 
+ It follows that \\(n + 1 > s\\). Since \\(n + 1 \in \mathbb{N}\\), this contradicts \\(s\\) being an upper bound of \\(\mathbb{N}\\).

To illustrate the property concretely, consider the real number \\(x = 7.4\\). The Archimedean property guarantees the existence of a natural number greater than \\(x\\): since \\(8 > 7.4\\), the smallest such natural number is \\(n = 8\\). The result, elementary as it appears, depends on the completeness of \\(\mathbb{R}\\) and fails in ordered fields that do not satisfy it.

- - - 
## Dedekind cuts

A Dedekind cut is a subset \\(A \subseteq \mathbb{Q}\\) satisfying three conditions: \\(A\\) is non-empty and \\(A \neq \mathbb{Q}\\). If \\(q \in A\\) and \\(p < q\\) then \\(p \in A\\), and \\(A\\) has no greatest element. The set \\(\mathbb{R}\\) is then defined as the collection of all Dedekind cuts of \\(\mathbb{Q}\\).

To illustrate, the rational number \\(r \in \mathbb{Q}\\) corresponds to the cut \\(A_r = \\{ q \in \mathbb{Q} : q < r \\}\\). An irrational number such as \\(\sqrt{2}\\) corresponds instead to the cut:

\\[
A = \\{ q \in \mathbb{Q} : q < 0 \\} \cup \\{ q \in \mathbb{Q} : q > 0 \text{ and } q^2 < 2 \\}.
\\]

This set satisfies all three conditions, yet has no rational supremum in \\(\mathbb{Q}\\): the cut carves out a position on the rational line where no rational number sits, and it is precisely this gap that the construction fills by declaring \\(A\\) itself to be a real number.

- - -

The algebraic structure of \\(\mathbb{R}\\) is then built directly from set-theoretic operations on cuts. Addition is defined by setting:

\\[
A + B = \\{ p + q : p \in A,\\, q \in B \\}
\\]

The order is given by inclusion: \\(A \leq B\\) if and only if \\(A \subseteq B\\). One verifies that these definitions make \\(\mathbb{R}\\) into a totally ordered field. The completeness of \\(\mathbb{R}\\) in this construction has the following proof: given a non-empty collection \\(S\\) of cuts that is bounded above, the supremum is the union \\(\bigcup_{A \in S} A\\), which is itself a cut and is the least upper bound of \\(S\\) by construction.

> The Dedekind construction builds the real numbers from the order structure of \\(\mathbb{Q}\\) alone. Its main contribution is to show that the completeness of \\(\mathbb{R}\\) is a consequence of filling in all the gaps that the rational order leaves open.

- - -
## Cauchy sequence construction

A second construction of \\(\mathbb{R}\\) starts from a limitation of \\(\mathbb{Q}\\). Not every [Cauchy sequence](../cauchy-sequence/) of rational numbers converges to a rational number. A sequence \\((x_n)_{n \in \mathbb{N}}\\) in \\(\mathbb{Q}\\) is a Cauchy sequence if for every \\(\varepsilon \in \mathbb{Q}^+\\) there exists \\(N \in \mathbb{N}\\) such that:

\\[
m, n \geq N \implies |x_m - x_n| < \varepsilon
\\]

The terms of the sequence cluster together without the sequence needing to refer to a [limit](../limits/), which may not yet exist in \\(\mathbb{Q}\\). The sequence of rational approximations to \\(\sqrt{2}\\) is a standard example:

\\[
\left(1,\, \frac{3}{2},\, \frac{7}{5},\, \frac{17}{12},\, \ldots\right)
\\]

It is Cauchy in \\(\mathbb{Q}\\), yet its limit lies outside \\(\mathbb{Q}\\). Two Cauchy sequences \\((x_n)\\) and \\((y_n)\\) in \\(\mathbb{Q}\\) are declared equivalent if their difference tends to zero:

\\[
(x_n) \sim (y_n) \iff \lim_{n \to \infty} |x_n - y_n| = 0
\\]

One verifies that \\(\sim\\) is an equivalence relation. The real numbers are then defined as the set of equivalence classes:

\\[
\mathbb{R} := C/{\sim}
\\]

\\(C\\) denotes the collection of all Cauchy sequences in \\(\mathbb{Q}\\). Addition and multiplication are defined termwise:

\\[[(x_n)] + [(y_n)] = [(x_n + y_n)]\\]
\\[ [(x_n)] \cdot [(y_n)] = [(x_n y_n)]\\]

These operations are well-defined, meaning independent of the choice of representative. The order is given by \\([(x_n)] \leq [(y_n)]\\) when either \\((x_n) \sim (y_n)\\) or there exists \\(N \in \mathbb{N}\\) such that \\(x_n < y_n\\) for all \\(n \geq N\\). The rational numbers embed into \\(\mathbb{R}\\) via \\(q \mapsto [(q, q, q, \ldots)]\\) preserving both operations and order.

The real number \\(\sqrt{2}\\), for instance, is the equivalence class of any Cauchy sequence of rationals converging to it, such as \\((1, 1.4, 1.41, 1.414, \ldots)\\). Two such sequences satisfy \\((x_n) \sim (y_n)\\) and therefore define the same real number. Completeness in this construction means that every Cauchy sequence of real numbers converges to a real number. The Dedekind and Cauchy constructions are isomorphic as complete ordered fields (they describe exactly the same mathematical object).

- - - 
## Consequences of completeness

The rational numbers are dense in \\(\mathbb{R}\\): between any two distinct real numbers there exists a rational number. In more formal terms for every \\(x, y \in \mathbb{R}\\) with \\(x < y\\), there exists \\(q \in \mathbb{Q}\\) such that \\(x < q < y\\). This follows from the Archimedean property. Given \\(x < y\\), one finds a natural number \\(n\\) satisfying \\(n(y - x) > 1\\) and among the integers \\(m\\) with \\(m > nx\\) one can identify one for which \\(x < m/n < y\\) holds.

Despite the density of \\(\mathbb{Q}\\) in \\(\mathbb{R}\\), the two sets differ in cardinality. The rational numbers are countable, meaning their elements can be placed in a one-to-one correspondence with the natural numbers. The real numbers are uncountable since no such correspondence exists. This result implies that the irrational numbers, which form the set \\(\mathbb{R} \setminus \mathbb{Q}\\), constitute the overwhelming majority of the real line.

The Bolzano-Weierstrass theorem is a further consequence of completeness. It states that every bounded sequence of real numbers has a convergent subsequence. This result guarantees that bounded infinite sets cannot spread indefinitely without accumulating somewhere, and it underpins the theory of [limits](../limits), [continuous functions](../continuous-functions/), and compactness in \\(\mathbb{R}\\).

- - -
## Uniqueness of \\(\mathbb{R}\\)

The real number system is the unique complete ordered field. Any two complete ordered fields are isomorphic as ordered fields, and the isomorphism between them is unique. This means that \\(\mathbb{R}\\) is not merely one among many possible completions of \\(\mathbb{Q}\\) but the only one up to a structure-preserving bijection.

- - -
## Intervals

Among the subsets of \\(\mathbb{R}\\), [intervals](../intervals/) occupy a central role. An interval is a subset \\(I \subseteq \mathbb{R}\\) with the property that, whenever two points belong to it, every point lying between them also belongs to it. Intervals may be bounded, such as the open interval \\((a, b)\\) or the closed interval \\([a, b]\\), or unbounded, such as \\([a, +\infty)\\) or \\((-\infty, b)\\). The entire real line is itself an interval, denoted \\((-\infty, +\infty)\\).