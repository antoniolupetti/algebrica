---
title: Heine's Sequential Criterion for Limits
source: https://algebrica.org/heine-sequential-criterion-for-limits/
license: CC BY-NC 4.0
tags:
  - heine-theorem
  - limits
  - one-sided-limits
  - sequences
  - sequential-criterion
---

## Statement

Heine's criterion characterizes the limit of a [function](../functions/) in terms of the limits of [sequences](../sequences/) obtained by applying the function to the terms of a sequence of arguments. Formally, consider a function $f:A\to\mathbb{R},$ with $A\subseteq\mathbb{R},$ and let $a\in\mathbb{R}$ be an [accumulation point](../topology-of-the-real-line/) of $A.$ For a fixed value $L\in\mathbb{R},$ the following equivalence holds, with convergence on the right required for every sequence $(x_n)$ in $A\setminus\{a\}$ such that $x_n\to a$:

$$
\lim_{x\to a}f(x)=L
\quad\Longleftrightarrow\quad
f(x_n)\to L \tag{1}
$$

To prove the forward implication in $(1),$ suppose that $f(x)\to L$ as $x\to a$ and take $(x_n)$ in $A\setminus\{a\}$ with $x_n\to a.$ Given $\varepsilon\gt0,$ the [definition of a limit](../limits/) provides $\delta\gt0$ such that, for every $x\in A,$ we have:

$$
0\lt|x-a|\lt\delta\implies |f(x)-L|\lt\varepsilon \tag{2}
$$

Since $x_n\to a$ and $x_n\neq a,$ there is an index $N$ such that $0\lt|x_n-a|\lt\delta$ for every $n\geq N,$ so, by the choice of $\delta,$ we obtain:

$$
n\geq N\implies |f(x_n)-L|\lt\varepsilon \tag{3}
$$

Since $\varepsilon\gt0$ is arbitrary, $(3)$ proves that $f(x_n)\to L$ and establishes the forward implication. For the reverse implication, suppose that all admissible sequences have image sequences converging to $L$ and prove by contradiction that $f(x)\to L.$ If $f$ did not tend to $L,$ there would be some $\varepsilon_0\gt0$ such that, for every $\delta\gt0,$ we could find a point $x\in A$ satisfying:

$$
\begin{align}
0\lt|x-a|\lt\delta \notag \\[6pt]
|f(x)-L|\geq\varepsilon_0 \tag{4}
\end{align}
$$

Applying $(4)$ with $\delta=1/n$ for each integer $n\geq1,$ we could choose a sequence $(x_n)$ of points in $A\setminus\{a\}$ such that:

$$
\begin{align}
0\lt|x_n-a|\lt\frac{1}{n} \notag \\[6pt]
|f(x_n)-L|\geq\varepsilon_0 \tag{5}
\end{align}
$$

In $(5),$ the first inequality gives $x_n\to a,$ since $1/n\to0,$ while the second rules out $f(x_n)\to L,$ so we have an admissible sequence that contradicts the initial hypothesis, and therefore $f(x)\to L$ must hold.

## Ruling out the existence of a limit

The forward implication in $(1)$ allows us to rule out the existence of a limit by comparing two admissible sequences. If their image sequences tend to different values, the function cannot have a limit, because that limit would have to equal both values. Consider the following example:

$$
f(x)=\sin\frac{1}{x} \tag{6}
$$

To obtain image sequences with different limits, we choose the arguments so that the sine is always $1$ along one sequence and $-1$ along the other, so for each integer $n\geq1$ we set:

$$
\begin{align}
x_n&=\frac{1}{\pi/2+2\pi n} \notag \\[6pt]
y_n&=\frac{1}{3\pi/2+2\pi n} \tag{7}
\end{align}
$$

The sequences in $(7)$ have nonzero terms and both tend to zero, so they are admissible for Heine's criterion at $a=0.$ Substituting the values from $(7)$ into $(6)$ and using the [periodicity of the sine](../sine-function/), we obtain:

$$
\begin{align}
f(x_n)&=\sin\left(\frac{\pi}{2}+2\pi n\right)=1 \notag \\[6pt]
f(y_n)&=\sin\left(\frac{3\pi}{2}+2\pi n\right)=-1 \tag{8}
\end{align}
$$

In $(8),$ we have two distinct limits that rule out the existence of a unique limit of $f$ at $a.$ Comparing the limits in $(8)$ also explains why $(1)$ requires us to consider all admissible sequences. Indeed, if we chose only $z_n=1/(\pi n),$ we would have $z_n\to0$ and $f(z_n)=0$ for every $n,$ but this convergence does not determine the limit of the function, whose existence we have already ruled out using $(8).$

## Proving the existence of a limit

We now turn to proving that a limit exists, using the reverse implication in $(1)$ and showing that the image sequence of an arbitrary sequence [converges](../convergent-and-divergent-sequences/). For example, consider the following function and study its limit as $x\to0$:

$$
f(x)=
\begin{cases}
x & \text{if }x\in\mathbb{Q} \\[6pt]
-x & \text{if }x\in\mathbb{R}\setminus\mathbb{Q}
\end{cases}
\tag{9}
$$

Taking an arbitrary sequence $(x_n)$ of nonzero real numbers with $x_n\to0,$ we obtain:

$$
|f(x_n)|=|x_n|\to0 \tag{10}
$$

Equation $(10)$ implies $f(x_n)\to0,$ and this result holds for every admissible sequence, so, by $(1),$ we can conclude that the limit exists and is equal to:

$$
\lim_{x\to0}f(x)=0 \tag{11}
$$

## One-sided and infinite limits

Heine's criterion also allows us to study [one-sided limits](../limits/), limits at infinity, and limits in which the function diverges, by adapting the conditions on the sequences and their image sequences. In particular, for one-sided limits, we apply $(1)$ to the part of the domain on the side under consideration. Thus, if $a$ is an accumulation point of $A\cap(a,+\infty),$ the right-hand limit is characterized using all sequences $(x_n)$ of points in this set with $x_n\to a$:

$$
\lim_{x\to a^+}f(x)=L
\quad\Longleftrightarrow\quad
f(x_n)\to L \tag{12}
$$

For the left-hand limit, we instead consider all sequences in $A\cap(-\infty,a)$ with $x_n\to a,$ requiring $a$ to be an accumulation point of this set. When the argument tends to $+\infty,$ the domain must be unbounded above. Convergence of the image sequences is then required for every sequence $(x_n)$ of points in $A$ with $x_n\to+\infty$:

$$
\lim_{x\to+\infty}f(x)=L
\quad\Longleftrightarrow\quad
f(x_n)\to L \tag{13}
$$

When $x\to-\infty,$ we replace the condition $x_n\to+\infty$ in $(13)$ with $x_n\to-\infty,$ requiring $A$ to be unbounded below. Observe that in $(13)$ the argument tends to infinity, while $L$ is finite. The criterion remains valid when the values of the function tend to $\pm\infty;$ indeed, if $a$ is a finite accumulation point of $A,$ divergence of the image sequences is required for every sequence $(x_n)$ in $A\setminus\{a\}$ with $x_n\to a$:

$$
\lim_{x\to a}f(x)=+\infty
\quad\Longleftrightarrow\quad
f(x_n)\to+\infty \tag{14}
$$

To prove $(14),$ we replace the condition $|f(x)-L|\lt\varepsilon$ in $(2)$ with $f(x)\gt M,$ for every threshold $M\gt0.$ The case $L=-\infty$ follows by applying the same result to $-f.$ These extensions also hold in combination, for example for a right-hand limit equal to $+\infty$ or for an infinite limit as $x\to+\infty,$ with the corresponding conditions on the domain and the sequences.
