---
title: Discrete Random Variables
source: https://algebrica.org/discrete-random-variables/
license: CC BY-NC 4.0
tags:
  - cumulative-distribution-function
  - discrete-random-variables
  - joint-probability-distributions
  - probability
  - probability-mass-function
  - random-variables
  - statistics
---

## Definition

A discrete random variable is a [function](../functions/) $X$ that assigns a [real number](../real-numbers/) to each element of a discrete sample space $\Omega$:

$$
X : \Omega \rightarrow \mathbb{R}
$$

In this definition $\Omega$ is a discrete sample space, a [set](../sets/) of outcomes that is finite or countably infinite. Through the function $X$ the outcomes of a random experiment become numerical values, which can then be analyzed statistically.

> When the sample space is continuous, composed of infinitely many infinitesimally close outcomes, we speak of [continuous random variables](../continuous-random-variables/).

- - -

Consider an experiment in which a single die is rolled twice, and let $X$ be the number of sixes obtained. The possible values of $X$ are $0,$ $1,$ and $2,$ where $0$ means that no six appears in the two rolls, $1$ that exactly one six appears, and $2$ that both rolls show a six. The following table lists each value $x$ of the random variable and its probability $f(x)$:

| $x$ | $0$ | $1$ | $2$ |
|:------|:--:|:--:|:--:|
| $f(x)$ | $\dfrac{25}{36}$ | $\dfrac{10}{36}$ | $\dfrac{1}{36}$ |

The probabilities satisfy:

$$
\sum_x f(x) = 1
$$

This is consistent with the law of total probability, which states that the probabilities of all mutually exclusive outcomes of an experiment sum to $1.$

The values of $f(x)$ are obtained as follows:

$$
\begin{align}
P(X = 0) &= \left(\frac{5}{6}\right)^2 = \frac{25}{36} \\[6pt]
P(X = 1) &= 2 \cdot \frac{1}{6} \cdot \frac{5}{6} = \frac{10}{36} \\[6pt]
P(X = 2) &= \left(\frac{1}{6}\right)^2 = \frac{1}{36}
\end{align}
$$

+ In the case of $x = 0,$ both rolls show a number other than six. Since the probability of not getting a six on a single roll is $\frac{5}{6},$ the probability that this happens twice in a row is $\left(\frac{5}{6}\right)^2.$
+ In the case of $x = 1,$ exactly one six appears in the two rolls. This can happen in two ways, either the first roll shows a six and the second does not, or the first does not and the second does. Each of these events has probability $\frac{1}{6} \cdot \frac{5}{6},$ so the total probability is $2 \cdot \frac{1}{6} \cdot \frac{5}{6}.$
+ Finally, in the case of $x = 2,$ both rolls show a six. Since the probability of rolling a six on a single roll is $\frac{1}{6},$ the probability that this occurs twice in a row is $\left(\frac{1}{6}\right)^2.$

## Discrete probability distribution

A discrete random variable has a certain probability of taking each of its possible values. The function $f(x)$ that describes these probabilities is called the probability mass function, or discrete probability distribution. For such a distribution, the following conditions must hold:

$$
\begin{align}
& f(x) \ge 0 \\[6pt]
& \sum_x f(x) = 1 \\[6pt]
& P(X = x) = f(x)
\end{align}
$$

These conditions state that every probability is non-negative, that the probabilities sum to $1,$ and that the probability of the value $x$ is $f(x).$ The probability mass function determines every probabilistic property of $X,$ in particular its [mean or expected value](../mean-or-expected-value-of-a-random-variable/) and its [variance](../variance-and-covariance-of-a-random-variable/).

- - -

The cumulative distribution function $F(x)$ is the probability that $X$ takes a value not greater than $x$:

$$
F(x) = P(X \le x) = \sum_{t \le x} f(t)
$$

The function $F(x)$ is the total probability accumulated up to $x.$ It is defined for all real values of $x$ and increases in steps as new probability mass is added; it is non-decreasing and never exceeds $1.$

We return to the example of the die rolled twice, where $X$ is the number of sixes obtained, and construct its cumulative distribution function. The probability mass function of $X$ is:

| $x$    |       $0$        |       $1$       |      $2$       |
| :----- | :--------------: | :-------------: | :------------: |
| $f(x)$ | $\dfrac{25}{36}$ | $\dfrac{10}{36}$ | $\dfrac{1}{36}$ |

The cumulative distribution function is obtained by adding the probabilities up to each value of $x$:

| $x$ | $0$ | $1$ | $2$ |
|:------|:--:|:--:|:--:|
| $F(x)$ | $\dfrac{25}{36}$ | $\dfrac{35}{36}$ | $1$ |

In fact, we have:

$$
\begin{align}
F(0) &= P(X \le 0) = f(0) = \frac{25}{36} \\[6pt]
F(1) &= P(X \le 1) = f(0) + f(1) = \frac{25}{36} + \frac{10}{36} = \frac{35}{36} \\[6pt]
F(2) &= P(X \le 2) = f(0) + f(1) + f(2) = 1
\end{align}
$$

The table gives $F$ only at the possible values of $X,$ but the function is defined for every real $x.$ For $x < 0$ we have $F(x) = 0,$ since no probability has yet been accumulated. Between consecutive values the function is constant; it jumps by $f(x)$ at each possible value and equals $1$ for $x \ge 2,$ once every outcome has been included.

## Joint probability distributions

When the sample space is multidimensional, each outcome of the experiment involves two or more random variables. For two discrete random variables $X$ and $Y,$ the probability that they take a given pair of values together is described by a function $f(x, y),$ called the joint probability distribution:

$$
f(x, y) = P(X = x, Y = y)
$$

In this expression $f(x, y)$ is the probability that $X$ takes the value $x$ and, at the same time, $Y$ takes the value $y.$ For a joint probability distribution, the following conditions must hold:

$$
\begin{align}
& f(x, y) \ge 0 \\[6pt]
& \sum_x \sum_y f(x, y) = 1 \\[6pt]
& P(X = x, Y = y) = f(x, y)
\end{align}
$$

These conditions state that $f(x, y)$ is non-negative for every pair $(x, y),$ that the sum over all pairs equals $1,$ and that each joint probability $P(X = x, Y = y)$ is $f(x, y).$ Summing $f(x, y)$ over one variable gives the distribution of the other variable alone, called its marginal probability distribution:

$$
g(x) = \sum_y f(x, y) \qquad h(y) = \sum_x f(x, y)
$$

The function $g(x)$ is the probability that $X$ takes the value $x$ regardless of the value of $Y,$ and $h(y)$ is the analogous probability for $Y.$

## Example 1

A small box contains $4$ balls, $2$ white and $2$ black. Two balls are drawn at random without replacement. Let $X$ be the number of black balls drawn and $Y$ the number of white balls drawn.

Since only two balls are drawn, every outcome satisfies $x + y = 2,$ and the possible pairs are:

$$
(0, 2),\ (1, 1),\ (2, 0)
$$

Each pair has probability equal to the number of favorable draws divided by the total number of draws. The [binomial coefficient](../binomial-coefficient/) $\binom{2}{x}$ counts the ways of choosing $x$ black balls out of $2,$ $\binom{2}{y}$ counts the ways of choosing $y$ white balls, and $\binom{4}{2} = 6$ is the total number of ways of drawing two balls from the box:

$$
f(x, y) = \frac{\dbinom{2}{x}\dbinom{2}{y}}{\dbinom{4}{2}}
$$

This formula holds when $x + y = 2.$ Every other pair has probability $0,$ since a draw of two balls cannot produce it. Evaluating $f(x, y)$ at each pair gives the following table, with the values of $x$ along the rows and the values of $y$ along the columns:

$$
\begin{array}{c|ccc|c}
f(x, y) & 0 & 1 & 2 & \mathrm{Totals} \\[6pt]
\hline
0 & \dfrac{0}{6} & \dfrac{0}{6} & \dfrac{1}{6} & \dfrac{1}{6} \\[6pt]
1 & \dfrac{0}{6} & \dfrac{4}{6} & \dfrac{0}{6} & \dfrac{4}{6} \\[6pt]
2 & \dfrac{1}{6} & \dfrac{0}{6} & \dfrac{0}{6} & \dfrac{1}{6} \\[6pt]
\hline
\mathrm{Totals} & \dfrac{1}{6} & \dfrac{4}{6} & \dfrac{1}{6} & 1
\end{array}
$$

Each cell is the probability of drawing a specific combination of black and white balls. The row and column totals are the marginal probability distributions $g(x)$ and $h(y),$ and the sum of all the entries equals $1.$
