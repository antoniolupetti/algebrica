---
title: Probability
source: https://algebrica.org/probability/
license: CC BY-NC 4.0
tags:
  - axioms-of-probability
  - conditional-probability
  - counting-principle
  - events
  - probability
  - sample-space
  - statistics
---

## Random experiments and events

A random experiment is a procedure whose individual outcome cannot be predicted, although its possible outcomes are known in advance. Rolling a die, drawing a ball from an urn, and recording the number of calls arriving at a switchboard in one hour are experiments of this kind.

The [set](../sets/) of all possible outcomes is the sample space, denoted by $\Omega$ or by $S,$ and its elements are the elementary outcomes. When the sample space is finite, we write:

$$
\Omega=\{\ \omega_1,\omega_2,\dots,\omega_n\ \}
$$

An event is a subset $E\subseteq\Omega,$ and it occurs when the outcome of the experiment belongs to $E.$ The sample space itself is the certain event, because every outcome belongs to it, while the empty set $\emptyset$ is the impossible event, because no outcome belongs to it. An event with exactly one outcome is elementary.

For a die with faces numbered from $1$ to $6,$ the sample space is $\Omega=\{\ 1,2,3,4,5,6\ \}.$ The event that the face shows an even number is the subset $E=\{\ 2,4,6\ \},$ the event that the face shows a number smaller than $7$ is $\Omega$ itself, and the event that the face shows $7$ is empty.

Since events are sets, union, intersection, and complement describe how they combine. The union $E\cup F$ occurs when at least one of the two events occurs, the intersection $E\cap F$ occurs when both occur, and the complement $E^c=\Omega\setminus E$ occurs when $E$ does not. These three operations correspond to the disjunction, the conjunction, and the negation of [propositional logic](../propositional-logic/) applied to the statements that describe the events. A numerical function on the sample space is a random variable. [Discrete random variables](../discrete-random-variables/) and [continuous random variables](../continuous-random-variables/) are treated separately.

In an Euler-Venn diagram, the sample space is a rectangle, and events are regions bounded by closed curves inside it. The shaded region for a union, an intersection, or a complement shows the corresponding logical relation between the events.

## Interpretations of probability

The probability of an event is a number between $0$ and $1$ that measures how likely the event is to occur. The impossible event has probability $0,$ and the certain event has probability $1.$ The classical, frequentist, and subjective interpretations explain how this number is obtained. The axiomatic approach specifies the properties that every probability assignment must satisfy.

For an experiment with finitely many equally likely cases, Laplace's classical definition is:

$$
p=\frac{x}{n}
$$

In this ratio $x$ is the number of cases favorable to the event and $n$ is the number of possible cases. On a fair die, the event that the face shows an even number has three favorable cases out of six, hence $p=3/6=1/2.$ The definition is circular because calling the cases equally likely already makes a statement about their probabilities. It also says nothing about experiments with infinitely many outcomes.

In the frequentist interpretation, the experiment is repeated under identical conditions, and the probability of $E$ is its limiting relative frequency. Bernoulli's law of large numbers makes this statement precise. In $n$ independent [Bernoulli trials](../bernoulli-distribution/) with $E$ as the success event, the relative frequency of $E$ converges in probability to $P(E)$ as $n$ increases. For fixed $n,$ the number of occurrences of $E$ has a [binomial distribution](../binomial-distribution/) with parameters $n$ and $P(E).$ On this interpretation, probability is a property of the experiment that can, in principle, be measured by repetition.

In the subjective interpretation, developed by Bruno de Finetti, the probability of an event is an individual's degree of belief that it will occur. The odds at which the individual would accept a bet measure that degree. Two people may assign different probabilities to the same event. For each person, coherence requires the assignments to satisfy the rules stated below, since otherwise a combination of accepted bets guarantees a loss.

In the axiomatic formulation published by Andrey Kolmogorov in 1933, probability is a function from events to numbers that satisfies a short list of requirements. The axioms give rules for calculations but do not prescribe the values assigned to events. The three interpretations above explain what those values mean.

## Incompatible, exhaustive, and independent events

Two events $E$ and $F$ are incompatible, or mutually exclusive, when they cannot occur together in the same trial. Their intersection is then empty:

$$
E\cap F=\emptyset
$$

The events $E_1,E_2,\dots,E_s$ are pairwise incompatible when $E_i\cap E_j=\emptyset$ for every pair of distinct indices $i$ and $j.$ They are exhaustive when at least one of them occurs in every trial, that is, when their union is the whole sample space:

$$
E_1\cup E_2\cup\dots\cup E_s=\Omega
$$

A family that is pairwise incompatible and exhaustive is a partition of $\Omega,$ and exactly one of its events occurs in each trial. The six elementary events of a die roll form a partition because exactly one face appears in each roll.

- - -

Events may also be independent or dependent. Two events are independent when the occurrence of one leaves the probability of the other unchanged, and dependent otherwise. In two independent coin tosses, the first outcome has no effect on the second. When balls are drawn from an urn [without replacement](../hypergeometric-distribution/), the ball removed at the first draw is absent at the second.

## Probability axioms

A probability is a [function](../functions/) $P$ that assigns a [real number](../real-numbers/) to each event of the sample space and satisfies three requirements. The first is non-negativity:

$$
P(E)\ge 0
$$

The second is normalization, under which the certain event has probability one:

$$
P(\Omega)=1
$$

The third is countable additivity. Whenever the events $E_1,E_2,\dots$ are pairwise incompatible, the probability of their union is:

$$
P\left(\bigcup_{i=1}^{\infty}E_i\right)=\sum_{i=1}^{\infty}P(E_i)
$$

If $E_i=\emptyset$ from some index onward, countable additivity gives the finite form:

$$
P(E_1\cup E_2\cup\dots\cup E_s)=P(E_1)+P(E_2)+\dots+P(E_s)
$$

If the family is also exhaustive, the left side equals $P(\Omega)$ and the sum equals $1.$

> A plus sign is sometimes written between events, as in $P(E_1+E_2),$ where $+$ denotes union rather than algebraic addition. We use the union symbol to avoid this ambiguity.

> The axioms do not include an upper bound for $P$ because $P(E)\le 1$ follows from them. When $\Omega$ is [uncountable](../cardinality-and-countable-sets/), $P$ cannot in general be defined on every subset of $\Omega,$ and the events are restricted to a $\sigma$-algebra, a family of subsets closed under complement and countable union. For a finite or countably infinite sample space, the power set of $\Omega$ may be used as the $\sigma$-algebra.

## Complements, bounds, and unions

The impossible event has probability zero. The events $\Omega$ and $\emptyset$ are incompatible and their union is $\Omega,$ so additivity gives $P(\Omega)=P(\Omega)+P(\emptyset).$ Subtracting $P(\Omega)$ from both sides gives $P(\emptyset)=0.$

For an arbitrary event $E,$ the events $E$ and $E^c$ are incompatible and their union is $\Omega,$ so additivity gives:

$$
1=P(\Omega)=P(E\cup E^c)=P(E)+P(E^c)
$$

Solving for the second term gives the complement rule:

$$
P(E^c)=1-P(E)
$$

If $E\subseteq F,$ the event $F$ is the union of the incompatible events $E$ and $F\setminus E,$ so $P(F)=P(E)+P(F\setminus E).$ Since the second term is non-negative, $P(E)\le P(F).$ With $F=\Omega,$ every probability is at most $1.$ Combining this upper bound with non-negativity gives:

$$
0\le P(E)\le 1
$$

- - -

For arbitrary events, the sets $E\setminus F,$ $E\cap F,$ and $F\setminus E$ are pairwise disjoint and have union $E\cup F.$ Applying additivity to $E\cup F,$ to $E,$ and to $F$ gives:

$$
\begin{align}
P(E\cup F)&=P(E\setminus F)+P(E\cap F)+P(F\setminus E) \\[6pt]
P(E)&=P(E\setminus F)+P(E\cap F) \\[6pt]
P(F)&=P(E\cap F)+P(F\setminus E)
\end{align}
$$

Adding the last two equations gives $P(E)+P(F)=P(E\cup F)+P(E\cap F).$ Solving this equality for $P(E\cup F)$ gives:

$$
P(E\cup F)=P(E)+P(F)-P(E\cap F)
$$

When we add $P(E)$ and $P(F),$ the intersection is counted twice, so we subtract $P(E\cap F)$ once. When the two events are incompatible, the last term is zero and the formula reduces to additivity. For three events, the same argument gives:

$$
\begin{align}
P(E\cup F\cup G)=\ &P(E)+P(F)+P(G) \\[6pt]
&-P(E\cap F)-P(E\cap G)-P(F\cap G) \\[6pt]
&+P(E\cap F\cap G)
\end{align}
$$

## Equally likely outcomes

Let $\Omega=\{\ \omega_1,\dots,\omega_N\ \}$ be finite and suppose that all elementary events have the same probability $p.$ They are pairwise incompatible and their union is $\Omega,$ so normalization and additivity give $1=P(\Omega)=Np.$ Solving for $p$ gives:

$$
P(\{\ \omega_i\ \})=\frac{1}{N}\qquad i=1,2,\dots,N
$$

An event $E$ formed by $k$ of these outcomes is the union of $k$ incompatible elementary events, and additivity gives $P(E)=k/N.$ The probability of $E$ is therefore the ratio between the number of outcomes favorable to $E$ and the number of possible outcomes, which is the classical definition. Under the axiomatic treatment, this formula is a theorem for equally likely outcomes rather than the definition of probability.

Suppose two independent fair dice are rolled. We compute the probability that the sum of their faces is $8.$ If the outcome of each die is recorded in order, the sample space is the set of $36$ ordered pairs $(i,j)$ with $i$ and $j$ between $1$ and $6.$ These pairs are equally likely. The favorable pairs are $(2,6),$ $(3,5),$ $(4,4),$ $(5,3),$ and $(6,2),$ so the probability is:

$$
P(\mathrm{sum}=8)=\frac{5}{36}
$$

The outcomes are ordered pairs because $(2,6)$ and $(6,2)$ are distinct outcomes of the experiment. If pairs that differ only in order were identified, the sample space would have $21$ unordered pairs that are not equally likely, so the counting formula would not apply.

## Conditional probability and independence

When an event $F$ with $P(F)>0$ is known to have occurred, the outcomes outside $F$ are excluded and the probability measure is rescaled on $F$ so that $F$ has probability $1.$ The conditional probability of $E$ given $F$ is:

$$
P(E\mid F)=\frac{P(E\cap F)}{P(F)}
$$

The numerator is the probability that both $E$ and $F$ occur, and the denominator is the normalization factor. For fixed $F,$ the map $E\mapsto P(E\mid F)$ satisfies the three axioms, so every property established above holds for conditional probabilities as well.

Solving the definition for the intersection gives $P(E\cap F)=P(F)P(E\mid F).$ If $P(E)>0,$ interchanging $E$ and $F$ gives the second form. The multiplication rule is therefore:

$$
P(E\cap F)=P(F)P(E\mid F)=P(E)P(F\mid E)
$$

The two forms give the same number, and the choice between them depends on which conditional probability is easier to evaluate. Assume $P(E_1\cap\dots\cap E_k)>0$ for $k=1,2,\dots,s-1,$ so that each conditional probability below is defined. Applying the rule repeatedly gives:

$$
P(E_1\cap E_2\cap\dots\cap E_s)=P(E_1)P(E_2\mid E_1)P(E_3\mid E_1\cap E_2)\cdots P(E_s\mid E_1\cap\dots\cap E_{s-1})
$$

- - -

The events $E$ and $F$ are independent when their joint probability is the product of their probabilities:

$$
P(E\cap F)=P(E)P(F)
$$

If $P(F)>0,$ this equality is equivalent to $P(E\mid F)=P(E),$ which means that conditioning on $F$ does not change the probability of $E.$ The events $E_1,E_2,\dots,E_s$ are independent when the product formula holds for every subfamily, and in that case the probability of their joint occurrence is:

$$
P(E_1\cap E_2\cap\dots\cap E_s)=P(E_1)P(E_2)\cdots P(E_s)
$$

> Independence of the whole family is stronger than pairwise independence. Consider two independent tosses of a fair coin, and let $A$ be the event that the first toss gives heads, $B$ the event that the second gives heads, and $C$ the event that the two tosses agree. Each pair among $A,$ $B,$ $C$ has intersection probability $1/4,$ equal to the product of the separate probabilities, but $A\cap B\cap C$ is the outcome with two heads and has probability $1/4,$ while the product of the three probabilities is $1/8.$

An urn contains five balls of different colors, one of which is red, and two balls are drawn without replacement. Let $R_1$ and $R_2$ be the events that the red ball appears at the first and at the second draw. All five balls are available at the first draw, so $P(R_1)=1/5.$ At the second draw, the available balls depend on the first outcome. If the red ball has already been drawn it cannot appear again, so $P(R_2\mid R_1)=0,$ and if it has not been drawn it is one of the four balls that remain, so $P(R_2\mid R_1^c)=1/4.$ The two conditional probabilities differ, hence the events are dependent.

## Law of total probability

Let $F_1,F_2,\dots,F_n$ be a partition of the sample space with $P(F_i)>0$ for every index, and let $E$ be an event. Its intersections with the events of the partition are pairwise incompatible. Their union is the original event:

$$
E=(E\cap F_1)\cup(E\cap F_2)\cup\dots\cup(E\cap F_n)
$$

Applying additivity to this decomposition and the multiplication rule to each term gives the law of total probability:

$$
P(E)=\sum_{i=1}^{n}P(E\cap F_i)=\sum_{i=1}^{n}P(F_i)P(E\mid F_i)
$$

The probability of $E$ is the [weighted average](../arithmetic-mean/) of the conditional probabilities $P(E\mid F_i),$ with weights $P(F_i).$ The formula is used when the conditional probabilities are easier to obtain than the probability of $E$ itself.

For the urn in the previous section, the events $R_1$ and $R_1^c$ form a partition of the sample space. Substituting the conditional probabilities computed above into the law of total probability gives:

$$
P(R_2)=P(R_1)P(R_2\mid R_1)+P(R_1^c)P(R_2\mid R_1^c)=\frac{1}{5}\cdot 0+\frac{4}{5}\cdot\frac{1}{4}=\frac{1}{5}
$$

The red ball is as likely to appear at the second draw as at the first, although the two draws are dependent. The drawing procedure treats all five balls symmetrically, so each ball has probability $1/5$ of occupying each position.

## Counting outcomes

For equally likely outcomes, a probability is the ratio of the number of favorable outcomes to the number of possible outcomes. The counting principle applies to successive experiments. If the first experiment has $m$ possible outcomes and the second has $n$ possible outcomes for each outcome of the first, the combined experiment has $mn$ possible outcomes. The corresponding ordered pairs form a table with $m$ rows and $n$ columns:

$$
\begin{array}{cccc}
(1,1) & (1,2) & \cdots & (1,n) \\[6pt]
(2,1) & (2,2) & \cdots & (2,n) \\[6pt]
\vdots & \vdots & \ddots & \vdots \\[6pt]
(m,1) & (m,2) & \cdots & (m,n)
\end{array}
$$

The entry $(i,j)$ records the $i$-th outcome of the first experiment together with the $j$-th outcome of the second. Every combination appears in exactly one cell, so the table has $mn$ cells.

The principle extends to a sequence of $r$ experiments. Suppose the first experiment has $n_1$ possible outcomes, the second experiment has $n_2$ possible outcomes for each outcome of the first, and in general the $k$-th experiment has $n_k$ possible outcomes for each combination of outcomes of the preceding experiments. The number of possible outcomes for the whole sequence is:

$$
n_1\times n_2\times\dots\times n_r
$$

When order is irrelevant, the number of selections of $k$ objects without repetition from a set of $n$ objects is the [binomial coefficient](../binomial-coefficient/) $\binom{n}{k}.$ A set of $n$ distinct objects has $n!$ orderings, where $n!$ is the [factorial](../factorial/) of $n.$

Suppose a fair die is rolled three times. We compute the probability that the three outcomes are different. Each roll has six possible outcomes, and the rolls are independent, so the sample space has $6^3=216$ equally likely outcomes. To count the favorable outcomes, the first roll has six possibilities, the second has five because it must differ from the first, and the third has four because it must differ from both. Thus the event has $6\cdot 5\cdot 4=120$ outcomes, and its probability is:

$$
P(\mathrm{three\ distinct\ outcomes})=\frac{120}{216}=\frac{5}{9}
$$
