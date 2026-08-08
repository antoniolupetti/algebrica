---
title: Integrals
source: https://algebrica.org/category/integrals/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - definite-integral
  - fundamental-theorem-of-calculus
  - indefinite-integral
  - integration
  - riemann-integral
---
## Introduction to the chapter

An integral is a mathematical object that expresses the accumulation of a quantity over an interval. In single-variable calculus, the term has two related meanings. A [definite integral](../../definite-integrals/) assigns a real number to a Riemann-integrable function on a closed interval, while an [indefinite integral](../../indefinite-integrals/) denotes the family of all antiderivatives of a [function](../functions/). For a bounded function $f$ on $[a,b],$ consider an arbitrary partition $P$ given by $a=x_0 < x_1 < \cdots < x_n=b.$ Let $m_i$ and $M_i$ be the infimum and supremum of $f$ on $[x_{i-1},x_i].$ The lower and upper sums associated with $P$ are:

$$
\begin{align}
L(f,P) &= \sum_{i=1}^{n}m_i(x_i-x_{i-1}) \\[6pt]
U(f,P) &= \sum_{i=1}^{n}M_i(x_i-x_{i-1})
\end{align}
$$

The lower and upper integrals collect the best estimates obtained from all possible partitions:

$$
\begin{align}
L(f,[a,b]) &= \sup_P L(f,P) \\[6pt]
U(f,[a,b]) &= \inf_P U(f,P)
\end{align}
$$

The function $f$ is Riemann integrable precisely when these two values coincide. Their common value is the definite integral:

$$
L(f,[a,b])=U(f,[a,b])=\int_{a}^{b} f(x) \ dx
$$

The definite integral measures signed accumulation. When $f(x)\geq 0$ on $[a,b],$ it equals the area between the graph of $f$ and the $x$-axis. If $f$ changes sign, integrating $|f(x)|$ gives the geometric area. Equivalently, one splits the interval at each sign change and adds the absolute values of the resulting integrals.

The indefinite integral reverses [differentiation](../../derivatives/). If $F'(x)=f(x)$ on an interval, every antiderivative of $f$ on that interval has the form $F(x)+C,$ where $C\in\mathbb{R}.$ The notation for this family is:

$$
\int f(x) \ dx=F(x)+C
$$

The [Fundamental Theorem of Calculus](../../fundamental-theorem-of-calculus/) connects the two meanings. If $f$ is continuous on $[a,b]$ and $F'(x)=f(x),$ then the definite integral can be evaluated from any antiderivative by the formula:

$$
\int_a^b f(x) \ dx=F(b)-F(a)
$$

The computational treatment begins with [integration strategies](integration-strategies/), where the form of the integrand guides the choice of method, especially for more complex integrals.
