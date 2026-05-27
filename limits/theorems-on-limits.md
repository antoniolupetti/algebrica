---
title: Theorems on Limits
source: https://algebrica.org/theorems-on-limits/
license: CC BY-NC 4.0
tags:
  - comparison-theorem
  - limits
  - sign-permanence
  - squeeze-theorem
  - uniqueness-theorem
---
## Uniqueness of the limit

**Theorem 1.** If the [limit](../limits/) of $f(x)$ as $x \to x_0$ exists, then it is unique. The statement, in its general form, asserts that no [function](../functions/) can approach two different values, finite or infinite, as $x$ approaches the same point:

$$\lim_{x \to x_0} f(x) = \ell_1 \quad \text{and} \quad \lim_{x \to x_0} f(x) = \ell_2 \implies \ell_1 = \ell_2$$

The result holds for $\ell_1, \ell_2 \in \overline{\mathbb{R}}$, that is, including the cases in which one or both of the prospective limits are infinite.

- - -

The proof of the finite case proceeds by contradiction. Suppose that the same function $f(x)$ admits two distinct finite limits $\ell_1 \neq \ell_2$ as $x \to x_0$. The half-distance between the two values:

$$\varepsilon = \frac{|\ell_1 - \ell_2|}{2}$$

is strictly positive. Applying the definition of limit to $\ell_1$ with this choice of tolerance, there exists $\delta_1 > 0$ such that for every $x$ satisfying $0 < |x - x_0| < \delta_1$:

$$|f(x) - \ell_1| < \varepsilon$$

Applying the same definition to $\ell_2$ yields $\delta_2 > 0$ such that for every $x$ satisfying $0 < |x - x_0| < \delta_2$:

$$|f(x) - \ell_2| < \varepsilon$$

Set $\delta = \min(\delta_1, \delta_2)$. For every $x$ with $0 < |x - x_0| < \delta$ both inequalities hold simultaneously, and the triangle inequality gives:

$$|\ell_1 - \ell_2| = |(\ell_1 - f(x)) + (f(x) - \ell_2)| \leq |f(x) - \ell_1| + |f(x) - \ell_2| < 2\varepsilon = |\ell_1 - \ell_2|$$

The chain of estimates produces the strict inequality $|\ell_1 - \ell_2| < |\ell_1 - \ell_2|$, which is impossible. The assumption $\ell_1 \neq \ell_2$ must therefore be rejected, and the two limits coincide.

> The argument extends to the infinite cases by replacing $\varepsilon$-neighbourhoods with appropriate neighbourhoods of $\pm\infty$. If one of the prospective limits is finite and the other is $+\infty$, the two neighbourhoods can be chosen disjoint in $\overline{\mathbb{R}}$, and the function cannot belong to both at once for $x$ close to $x_0$. The values $+\infty$ and $-\infty$ admit disjoint neighbourhoods as well, and the same contradiction arises.

## Local boundedness

**Theorem 2.** A function which admits a finite limit at $x_0$ is bounded in a neighbourhood of $x_0$. The theorem provides a quantitative version of the intuition that values accumulating near a real number $\ell$ cannot escape arbitrarily far from it:

$$\lim_{x \to x_0} f(x) = \ell \in \mathbb{R} \implies \exists\ M > 0,\ \exists\ \delta > 0 \ \text{ such that } \ |f(x)| \leq M \ \text{ for all } x \text{ with } 0 < |x - x_0| < \delta$$

The hypothesis that the limit is finite is essential. The function $f(x) = 1/x$ has limit $+\infty$ as $x \to 0^+$ and is unbounded in every right neighbourhood of zero.

- - -

The proof follows by applying the definition of limit with the specific choice $\varepsilon = 1$. There exists $\delta > 0$ such that for every $x$ satisfying $0 < |x - x_0| < \delta$:

$$|f(x) - \ell| < 1$$

The reverse triangle inequality yields:

$$|f(x)| = |(f(x) - \ell) + \ell| \leq |f(x) - \ell| + |\ell| < 1 + |\ell|$$

Setting $M = |\ell| + 1$ provides the required bound on the punctured neighbourhood $0 < |x - x_0| < \delta$. The value of $\varepsilon$ has no role beyond producing a finite, explicit constant; any other positive value of $\varepsilon$ would give a bound of the form $|\ell| + \varepsilon$.

## Sign permanence

**Theorem 3.** f the limit of $f(x)$ at $x_0$ is strictly positive, the function is itself [strictly positive](../increasing-and-decreasing-functions/) in some punctured neighbourhood of $x_0$. The symmetric statement holds with positive replaced by negative throughout. In symbols, if $\ell > 0$:

$$\lim_{x \to x_0} f(x) = \ell \implies \exists\ \delta > 0 \ \text{ such that } \ f(x) > 0 \ \text{ for all } x \text{ with } 0 < |x - x_0| < \delta$$

The hypothesis $\ell > 0$ cannot be weakened to $\ell \geq 0$. If $\ell = 0$, the function may change sign arbitrarily close to $x_0$, as the example $f(x) = x \sin(1/x)$ at $x_0 = 0$ shows. The vanishing limit alone provides no information about the local sign.

- - -

The proof exploits the strict positivity of $\ell$ to choose a tolerance that leaves $f(x)$ trapped above zero. Set:

$$\varepsilon = \frac{\ell}{2} > 0$$

By the definition of limit, there exists $\delta > 0$ such that for every $x$ satisfying $0 < |x - x_0| < \delta$:

$$|f(x) - \ell| < \frac{\ell}{2} \quad \implies \quad \frac{\ell}{2} < f(x) < \frac{3\ell}{2}$$

The lower bound $f(x) > \ell/2 > 0$ proves the claim. The case $\ell < 0$ is treated by applying the same argument to the function $-f$, whose limit is $-\ell > 0$.

> A common refinement applies when $f$ is continuous at $x_0$ and $f(x_0) \neq 0$. In that setting $f$ has constant sign on a full neighbourhood of $x_0$, including the point $x_0$ itself. This form of the result is the one most often invoked in calculus, since continuous functions provide the natural domain of application.

## Comparison theorem

**Theorem 4.** Let $f$ and $g$ be defined in a neighbourhood of $x_0$ and assume that:

$$f(x) \leq g(x)$$

for every $x$ in the neighbourhood, with the possible exception of $x_0$ itself. If both limits exist as $x \to x_0$, the comparison theorem asserts that the inequality is preserved by the limit operator:

$$\lim_{x \to x_0} f(x) \leq \lim_{x \to x_0} g(x)$$

The statement provides the basic device for transferring pointwise information on two functions to a relation between their limit values.

- - -

The proof proceeds by contradiction. Denote the two limits by $\ell_f$ and $\ell_g$ and suppose that $\ell_f > \ell_g$. The positive quantity:

$$\varepsilon = \frac{\ell_f - \ell_g}{2}$$

isolates the two prospective limits in disjoint $\varepsilon$-neighbourhoods. By the definition of limit, there exists $\delta > 0$ such that for every $x$ with $0 < |x - x_0| < \delta$ both inequalities:

$$|f(x) - \ell_f| < \varepsilon \quad \text{and} \quad |g(x) - \ell_g| < \varepsilon$$

are satisfied. From the first inequality:

$$f(x) > \ell_f - \varepsilon = \frac{\ell_f + \ell_g}{2}$$

From the second:

$$g(x) < \ell_g + \varepsilon = \frac{\ell_f + \ell_g}{2}$$

Combining the two estimates gives $g(x) < f(x)$ on the punctured neighbourhood of radius $\delta$, in direct contradiction with the hypothesis $f \leq g$. The assumption $\ell_f > \ell_g$ is therefore untenable.

## Passing to the limit in inequalities

The comparison theorem admits a sharper formulation when the pointwise relation between $f$ and $g$ is a strict inequality rather than a large one. Suppose that:

$$f(x) < g(x)$$

for every $x$ in a punctured neighbourhood of $x_0$. The strongest conclusion that can be drawn about the limits is the large [inequality](../inequalities/):

$$\lim_{x \to x_0} f(x) \leq \lim_{x \to x_0} g(x)$$

Strict inequalities are not preserved under the limit operation. A standard counterexample is provided by:

$$f(x) = -|x| \qquad g(x) = |x|$$

The strict inequality $f(x) < g(x)$ holds for every $x \neq 0$, yet both functions tend to zero as $x \to 0$, so the two limits coincide and the strict inequality collapses into an equality.

The same caution applies to inequalities between a function and a constant. If $f(x) \geq c$ in a punctured neighbourhood of $x_0$ and the limit exists, the comparison theorem yields $\lim f \geq c$, while the strict inequality $f(x) > c$ cannot in general be promoted to $\lim f > c$. The constant case is recovered from the general statement by taking $g$ to be the constant function $c$.

## Connection with the squeeze theorem

The comparison theorem produces an inequality between two limits whenever both limits are known to exist. The [squeeze theorem](../squeeze-theorem/) addresses the converse situation, in which the existence of the central limit is itself the conclusion. If two functions $g$ and $h$ trap a third function $f$ between them:

$$g(x) \leq f(x) \leq h(x)$$

in a neighbourhood of $x_0$, and both bounding functions admit the same limit $\ell$ at $x_0$, then $f$ admits a limit at $x_0$ and that limit equals $\ell$. The squeeze theorem can be read as a strengthening of the comparison theorem, in which an a priori sandwich between three functions delivers both the existence and the value of the central limit.

> The discrete version applies to [sequences](../sequences/) and is known in the Italian tradition as the theorem of the two policemen. If $a_n \leq b_n \leq c_n$ from some index onwards and $a_n \to \ell$, $c_n \to \ell$, then $b_n \to \ell$. The discrete formulation is the form most frequently used in proofs concerning [convergent and divergent sequences](../convergent-and-divergent-sequences/).

## Conclusions

The operational rules for combining limits algebraically are developed in the page on the [algebra of limits](../algebra-of-limits/), where the uniqueness theorem and the local boundedness theorem are used implicitly in the justification of the quotient and composition rules. 

The interaction between limits and inequalities is exploited extensively in the [squeeze theorem](../squeeze-theorem/) and in the analysis of [indeterminate forms](../indeterminate-forms/). 

The role of the uniqueness theorem in characterising one-sided limits and discontinuities is discussed in the page on [limits](../limits/). 

The discrete counterpart of the comparison and sandwich principles is developed in the pages on [sequences](../sequences/) and on [convergent and divergent sequences](../convergent-and-divergent-sequences/).
