# Vector Spaces

Source: algebrica.org — CC BY-NC 4.0

## Definition

A vector space is an algebraic structure that formalises the idea of quantities that can be scaled and [combined linearly](../linear-combinations/). The concept arises wherever one encounters objects that can be added together and multiplied by numbers in a coherent way: geometric arrows in the plane, [polynomials](../polynomials/) with real coefficients, sequences of [real numbers](../properties-of-real-numbers/), and [continuous functions](../continuous-functions/) on an interval all share this common pattern.

Unlike a [group](../groups/) or a [ring](../rings/), which are defined on a single set, a vector space involves two distinct sets: a [field](../fields/) \\(F\\), whose elements are called scalars, and a set \\(V\\), whose elements are called [vectors](../vectors/). A vector space over \\(F\\) is a set \\(V\\) together with two operations, vector addition \\(+ : V \times V \to V\\) and scalar multiplication \\(\cdot : F \times V \to V\\), satisfying the following axioms:

- \\((V, +)\\) is an abelian group. In particular, there exists a zero vector \\(\mathbf{0} \in V\\) such that \\(\mathbf{v} + \mathbf{0} = \mathbf{v}\\) for all \\(\mathbf{v} \in V\\), and every vector \\(\mathbf{v}\\) has an additive inverse \\(-\mathbf{v}\\).
- Compatibility with field multiplication: for all \\(\alpha, \beta \in F\\) and \\(\mathbf{v} \in V\\), one has \\(\alpha \cdot (\beta \cdot \mathbf{v}) = (\alpha\beta) \cdot \mathbf{v}\\).
- Identity element of scalar multiplication: for all \\(\mathbf{v} \in V\\), the multiplicative identity \\(1 \in F\\) satisfies \\(1 \cdot \mathbf{v} = \mathbf{v}\\).
- Distributivity of scalar multiplication over vector addition: for all \\(\alpha \in F\\) and \\(\mathbf{u}, \mathbf{v} \in V\\), one has \\(\alpha \cdot (\mathbf{u} + \mathbf{v}) = \alpha \cdot \mathbf{u} + \alpha \cdot \mathbf{v}\\).
- Distributivity of scalar multiplication over field addition: for all \\(\alpha, \beta \in F\\) and \\(\mathbf{v} \in V\\), one has \\((\alpha + \beta) \cdot \mathbf{v} = \alpha \cdot \mathbf{v} + \beta \cdot \mathbf{v}\\).

> The field \\(F\\) over which \\(V\\) is defined is called the scalar field of \\(V\\). In most applications encountered at the undergraduate level, \\(F\\) is either \\(\mathbb{R}\\) or \\(\mathbb{C}\\), and one speaks of a real vector space or a complex vector space accordingly.

- - -
## Properties

Several elementary consequences follow directly from the axioms. For any scalar \\(\alpha \in F\\) and any vector \\(\mathbf{v} \in V\\), multiplication by zero satisfies \\(0 \cdot \mathbf{v} = \mathbf{0}\\). To see this, one writes \\(0 \cdot \mathbf{v} = (0 + 0) \cdot \mathbf{v} = 0 \cdot \mathbf{v} + 0 \cdot \mathbf{v}\\) and cancels \\(0 \cdot \mathbf{v}\\) from both sides using the group structure of \\((V, +)\\). Similarly, for any \\(\mathbf{v} \in V\\) one has \\(\alpha \cdot \mathbf{0} = \mathbf{0}\\) and \\((-1) \cdot \mathbf{v} = -\mathbf{v}\\).

If \\(\alpha \cdot \mathbf{v} = \mathbf{0}\\), then either \\(\alpha = 0\\) or \\(\mathbf{v} = \mathbf{0}\\). This is a direct consequence of the invertibility of nonzero scalars: if \\(\alpha \neq 0\\), then \\(\mathbf{v} = 1 \cdot \mathbf{v} = (\alpha^{-1}\alpha) \cdot \mathbf{v} = \alpha^{-1} \cdot (\alpha \cdot \mathbf{v}) = \alpha^{-1} \cdot \mathbf{0} = \mathbf{0}\\). This property is the vector space analogue of the absence of zero divisors in a field, and it plays a central role in the theory of linear independence.

- - -
## Algebraic hierarchy

Vector spaces occupy a position at the top of the standard hierarchy of algebraic structures, depending essentially on the presence of a field of scalars.

A [group](../groups/) consists of a set with a single operation admitting inverses. A [ring](../rings/) introduces a second operation that need not be invertible. A [field](../fields/) requires both operations to be fully invertible on nonzero elements. A vector space then takes a field as a given and builds a new structure on top of it, one in which the field acts on a separate set of vectors by scaling. The three structures form a chain of increasing rigidity:

- A group carries one operation with inverses.
- A ring carries two operations, with inverses guaranteed only for addition.
- A field carries two operations, with inverses guaranteed for both addition and all nonzero elements under multiplication.

> A vector space is not itself a further step in this chain but rather a structure that presupposes a field. Every vector space over \\(\mathbb{R}\\) or \\(\mathbb{C}\\) depends on the field axioms being in force for its scalar multiplication to be well-defined.

- - -
## Examples

The set \\(\mathbb{R}^n\\) of all ordered \\(n\\)-tuples of real numbers is a vector space over \\(\mathbb{R}\\) under componentwise addition and scalar multiplication. For \\(n = 2\\), addition is defined by \\((a_1, a_2) + (b_1, b_2) = (a_1 + b_1,\\, a_2 + b_2)\\) and scalar multiplication by \\(\alpha \cdot (a_1, a_2) = (\alpha a_1,\\, \alpha a_2)\\). The zero vector is \\((0, 0)\\). This is the prototype of a finite-dimensional real vector space, and it provides the geometric intuition underlying the general theory.

The set \\(\mathbb{C}^n\\) of all ordered \\(n\\)-tuples of complex numbers is a vector space over \\(\mathbb{C}\\) under the analogous operations. It can also be regarded as a vector space over \\(\mathbb{R}\\), though in that case its dimension doubles: \\(\mathbb{C}^n\\) as a real vector space has dimension \\(2n\\).

---

The set \\(\mathbb{R}[x]_{\leq n}\\) of all [polynomials](../polynomials/) with real coefficients of degree at most \\(n\\) is a vector space over \\(\mathbb{R}\\) under the usual addition of polynomials and multiplication of a polynomial by a real constant. The zero vector is the zero polynomial. A natural basis for this space is \\(\{1, x, x^2, \ldots, x^n\}\\), which contains \\(n+1\\) elements, so the dimension of this space is \\(n+1\\).

The set \\(\mathcal{C}([a,b])\\) of all continuous real-valued functions on a closed interval \\([a,b]\\) is a vector space over \\(\mathbb{R}\\) under pointwise addition and scalar multiplication: \\((f + g)(x) = f(x) + g(x)\\) and \\((\alpha f)(x) = \alpha f(x)\\). This space is infinite-dimensional, since the polynomials of all degrees form a linearly independent subset with no finite spanning set.

- - -
## Subspaces

A nonempty subset \\(W \subseteq V\\) is called a subspace of \\(V\\) if \\(W\\) is itself a vector space over \\(F\\) under the operations inherited from \\(V\\). Rather than verifying all axioms separately, it suffices to check two conditions: for all \\(\mathbf{u}, \mathbf{v} \in W\\) and all \\(\alpha \in F\\), one requires \\(\mathbf{u} + \mathbf{v} \in W\\) and \\(\alpha \cdot \mathbf{v} \in W\\). These two conditions together are called closure under linear combinations. The zero vector \\(\mathbf{0}\\) must belong to every subspace, since setting \\(\alpha = 0\\) gives \\(0 \cdot \mathbf{v} = \mathbf{0} \in W\\).

As an example, the set \\(W = \{(x, y) \in \mathbb{R}^2 : y = 2x\}\\) is a subspace of \\(\mathbb{R}^2\\). For any two vectors \\((x_1, 2x_1)\\) and \\((x_2, 2x_2)\\) in \\(W\\), their sum \\((x_1 + x_2,\\, 2x_1 + 2x_2) = (x_1 + x_2,\\, 2(x_1+x_2))\\) belongs to \\(W\\), and for any scalar \\(\alpha \in \mathbb{R}\\) the vector \\(\alpha(x_1, 2x_1) = (\alpha x_1,\\, 2\alpha x_1)\\) also belongs to \\(W\\). Both conditions are satisfied, so \\(W\\) is a subspace of \\(\mathbb{R}^2\\). Geometrically, \\(W\\) is the line through the origin with slope \\(2\\).

> The diagram illustrates the two closure conditions on the subspace \\(W = \\{(x, y) \\in \\mathbb{R}^2 : y = 2x\\}\\). Any vector in \\(W\\) lies on the line through the origin with slope \\(2\\). Adding two such vectors or multiplying one by a scalar always produces a vector that remains on the same line, confirming that \\(W\\) is closed under both operations.

- - -
## Basis and dimension

A set of vectors \\(\\{\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n\\}\\) in \\(V\\) is called linearly independent if the only solution to the equation

\\[
\alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2 + \cdots + \alpha_n \mathbf{v}_n = \mathbf{0}
\\]

is \\(\alpha_1 = \alpha_2 = \cdots = \alpha_n = 0\\). A set of vectors that is not linearly independent is called linearly dependent, meaning that at least one vector in the set can be expressed as a [linear combination](../linear-combinations/) of the others. A basis of \\(V\\) is a linearly independent set of vectors that spans \\(V\\), meaning every vector in \\(V\\) can be written as a linear combination of the basis vectors. The representation of any vector in terms of a given basis is unique. If 
\\[\mathbf{v} = \alpha_1 \mathbf{v}_1 + \cdots + \alpha_n \mathbf{v}_n = \beta_1 \mathbf{v}_1 + \cdots + \beta_n \mathbf{v}_n\\]

then subtracting yields: 
\\[(\alpha_1 - \beta_1)\mathbf{v}_1 + \cdots + (\alpha_n - \beta_n)\mathbf{v}_n = \mathbf{0}\\]

and linear independence forces \\(\alpha_k = \beta_k\\) for all \\(k\\).

- - -

One of the fundamental theorems of linear algebra states that any two bases of the same vector space contain the same number of elements. The argument rests on the observation that if a set of \\(m\\) vectors spans \\(V\\) and a set of \\(n\\) vectors is linearly independent in \\(V\\), then necessarily \\(n \leq m\\). Applying this inequality twice, once in each direction, to any two bases forces their cardinalities to be equal. This common cardinality is called the dimension of \\(V\\) and is denoted \\(\dim V\\).

The standard basis of \\(\mathbb{R}^n\\) consists of the \\(n\\) vectors \\(\mathbf{e}_1, \mathbf{e}_2, \ldots, \mathbf{e}_n\\), where \\(\mathbf{e}_k\\) has a \\(1\\) in position \\(k\\) and \\(0\\) everywhere else. For example, in \\(\mathbb{R}^3\\) the standard basis is the following:

\\[
\mathbf{e}_1 = (1, 0, 0), \quad \mathbf{e}_2 = (0, 1, 0), \quad \mathbf{e}_3 = (0, 0, 1)
\\]

Every [vector](../vectors/) \\((a, b, c) \in \mathbb{R}^3\\) can be written uniquely as \\(a\\,\mathbf{e}_1 + b\\,\mathbf{e}_2 + c\\,\mathbf{e}_3\\), confirming that these three vectors form a basis and that \\(\dim \mathbb{R}^3 = 3\\).

- - -
## Linear maps

A linear map, or linear transformation, is a function \\(\varphi : V \to W\\) between two vector spaces over the same field \\(F\\) that preserves the vector space structure. Explicitly, \\(\varphi\\) is linear if for all \\(\mathbf{u}, \mathbf{v} \in V\\) and all \\(\alpha \in F\\) the following two conditions hold:

\\[\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})\\]
\\[ \varphi(\alpha \cdot \mathbf{v}) = \alpha \cdot \varphi(\mathbf{v})\\]

These two conditions can be combined into the single requirement that \\(\varphi(\alpha \mathbf{u} + \beta \mathbf{v}) = \alpha\varphi(\mathbf{u}) + \beta\varphi(\mathbf{v})\\) for all \\(\alpha, \beta \in F\\) and \\(\mathbf{u}, \mathbf{v} \in V\\). A linear map that is bijective is called a linear isomorphism, and two vector spaces are isomorphic if a linear isomorphism between them exists. A fundamental result states that every \\(n\\)-dimensional vector space over \\(F\\) is isomorphic to \\(F^n,\\) so finite-dimensional vector spaces are completely classified by their dimension and their scalar field.

The kernel and image of a linear map \\(\varphi : V \to W\\) are defined as follows:

\\[\ker(\varphi) = \\{\mathbf{v} \in V : \varphi(\mathbf{v}) = \mathbf{0}\\}\\]
\\[\mathrm{im}(\varphi) = \\{\varphi(\mathbf{v}) : \mathbf{v} \in V\\}\\]

Both \\(\ker(\varphi)\\) and \\(\mathrm{im}(\varphi)\\) are subspaces of \\(V\\) and \\(W\\) respectively. The dimension theorem, also known as the rank-nullity theorem, states that for any linear map between finite-dimensional spaces the following identity holds:

\\[
\dim V = \dim \ker(\varphi) + \dim \mathrm{im}(\varphi)
\\]

The dimension of \\(\mathrm{im}(\varphi)\\) is called the rank of \\(\varphi\\) and the dimension of \\(\ker(\varphi)\\) is called its nullity. The rank-nullity theorem is one of the central results of linear algebra and underlies the theory of [systems of linear equations](../systems-of-linear-equations/), the analysis of [matrices](../matrices/), and the classification of linear maps between finite-dimensional spaces.

- - -
## Example 

Consider the linear map \\(\varphi : \mathbb{R}^3 \to \mathbb{R}^2\\) defined by the following assignment:

\\[
\varphi(x, y, z) = (x + y,\\; y + z)
\\]

To verify linearity, one checks that:
 
\\[\varphi(\mathbf{u} + \mathbf{v}) = \varphi(\mathbf{u}) + \varphi(\mathbf{v})\\] 
\\[\varphi(\alpha \mathbf{v}) = \alpha \varphi(\mathbf{v})\\] 

hold for all vectors and scalars, which follows immediately from the linearity of addition and scalar multiplication in \\(\mathbb{R}^3\\). The kernel consists of all vectors \\((x, y, z)\\) satisfying \\(x + y = 0\\) and \\(y + z = 0\\), that is, \\(x = -y\\) and \\(z = -y\\). Every element of \\(\ker(\varphi)\\) therefore has the form:

 \\[(-y, y, -y) = y(-1, 1, -1)\\] 

for some \\(y \in \mathbb{R}\\), so the kernel is the one-dimensional subspace spanned by \\((-1, 1, -1)\\). The image is all of \\(\mathbb{R}^2\\), since for any \\((a, b) \in \mathbb{R}^2\\) the vector \\((a, 0, b)\\) satisfies \\(\varphi(a, 0, b) = (a, b)\\), which shows that \\(\varphi\\) is surjective and thus \\(\dim \mathrm{im}(\varphi) = 2\\). The rank-nullity theorem is verified:

\\[
\dim \mathbb{R}^3 = \dim \ker(\varphi) + \dim \mathrm{im}(\varphi) = 1 + 2 = 3
\\]

The solution is therefore that \\(\ker(\varphi)\\) is the line through the origin in direction \\((-1, 1, -1)\\) and \\(\mathrm{im}(\varphi) = \mathbb{R}^2\\).
