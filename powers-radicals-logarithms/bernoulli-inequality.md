---
title: Bernoulli's Inequality
source: https://algebrica.org/bernoulli-inequality/
license: CC BY-NC 4.0
tags:
  - bernoulli-inequality
  - inequalities
  - mathematical-induction
  - powers
---
## Statement

Bernoulli's inequality states that, for every [real number](../real-numbers/) $x \ge -1$ and every [positive integer](../integers/) $n,$ the [power](../powers/) $(1+x)^n$ is greater than or equal to the linear expression $1+nx:$

$$ \tag{1}
(1+x)^n \ge 1+nx
$$

Inequality $(1)$ holds when $n=1$ or $x=0.$ In every other case, the [strict inequality](../inequalities/) holds:

$$ \tag{2}
(1+x)^n \gt 1+nx
$$

Inequalities $(1)$ and $(2)$ provide a lower bound for a power in terms of a linear expression, without having to expand or evaluate the power itself, since this calculation can sometimes be computationally demanding. The condition $x \ge -1$ ensures that the term $1+x$ on the left-hand side is nonnegative, so that we do not have to reverse the direction of the inequality, as we will see in the proof.

The proof of $(1)$ proceeds by [induction](../principle-of-mathematical-induction/) on $n.$ When $n = 1,$ both sides are equal to $1+x.$ If we assume that the inequality holds for some $n \ge 1,$ multiplying by $1+x$ (which we have established is nonnegative) preserves the direction of the inequality and gives:

$$
(1+x)^{n+1} \ge (1+nx)(1+x) = 1+(n+1)x+nx^2
$$

Since $nx^2 \ge 0,$ the right-hand side is greater than or equal to $1+(n+1)x,$ so we have:

$$
(1+x)^{n+1} \ge 1+(n+1)x
$$

The inequality therefore holds for $n+1,$ and the proof by induction is complete.

## Some applications

For a practical application of $(1),$ suppose that a quantity $Q_0 > 0$ increases by $2\%$ $10$ times, each time relative to the value reached after the previous increase. Each increase multiplies the quantity by $1.02,$ so the final value is:

$$
Q = Q_0(1.02)^{10}
$$

Applying Bernoulli's inequality with $x = 0.02$ and $n = 10,$ we obtain the following estimate:

$$
(1.02)^{10} \ge 1+10\cdot 0.02 = 1.2
$$

Since $Q_0 > 0,$ we can multiply both sides of the inequality by $Q_0$ without changing its direction to obtain:

$$
Q_0(1.02)^{10} \ge 1.2Q_0
$$

The left-hand side is the final value $Q,$ while the right-hand side is $Q_0+0.2Q_0.$ Subtracting $Q_0$ from both sides gives:

$$
Q-Q_0 \ge 0.2Q_0
$$

The increase $Q-Q_0$ is therefore at least $20\%$ of the initial quantity.

- - -

Bernoulli's inequality can also be used to prove that certain [sequences](../sequences/) are [monotone](../monotone-sequences/) and, when they are also bounded, establish their [convergence](../convergent-and-divergent-sequences/). For example, we prove that the following sequence is strictly increasing:

$$a_n = \left(1+\frac{1}{n}\right)^n$$

For $n \ge 1,$ the ratio of consecutive terms is given by the following identity:

$$
\frac{a_{n+1}}{a_n}
= \left(1+\frac{1}{n+1}\right)
\left(1-\frac{1}{(n+1)^2}\right)^n
$$

Applying $(1)$ with $x = -1/(n+1)^2$ gives:

$$
\begin{align}
\frac{a_{n+1}}{a_n}
&\ge \left(1+\frac{1}{n+1}\right)
\left(1-\frac{n}{(n+1)^2}\right) \\[6pt]
&= 1+\frac{1}{(n+1)^3} \\[6pt]
&> 1
\end{align}
$$

The sequence is also bounded above, as shown on the page on [Euler's number](../euler-number-limit-sequence/). Since it is increasing and bounded, it converges, and its limit defines the number $e:$

$$
e = \lim_{n \to +\infty}\left(1+\frac{1}{n}\right)^n
$$
