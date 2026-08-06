---
title: Automated Deduction in First-Order Logic
source: https://algebrica.org/automated-deduction-in-first-order-logic/
license: CC BY-NC 4.0
tags:
  - automated-deduction
  - backward-chaining
  - clausal-form
  - decidable-fragments
  - definite-clause
  - first-order-logic
  - forward-chaining
  - generalized-modus-ponens
  - herbrand-universe
  - most-general-unifier
  - prenex-normal-form
  - refutation
  - resolution
  - semantic-tableaux
  - semidecidability
  - skolemization
  - unification
  - universal-instantiation
---

## Quantifiers

A deduction procedure for [first-order logic](../first-order-logic/) answers the same question as its [propositional counterpart](../automated-deduction-in-propositional-logic/). Given a finite set $S$ of sentences and a sentence $\varphi,$ does $S \models \varphi$ hold? The reduction to unsatisfiability also carries over unchanged:

$$
S \models \varphi \Longleftrightarrow S \cup \{\neg\varphi\} \ \text{has no model}
$$

The proof uses only the definition of logical consequence, so it does not depend on the internal structure of the interpretations. What fails is the method of testing the right-hand side. In [propositional logic](../propositional-logic/), $n$ atoms yield $2^n$ interpretations and saturation under resolution terminates because only finitely many clauses exist. A first-order signature instead admits structures with domains of [arbitrary cardinality](../cardinality-and-countable-sets/), so no finite truth table can enumerate them.

> The calculi below are presented for formulas without equality. When equality is interpreted as identity, completeness also requires equality axioms or dedicated inference rules. Resolution provers commonly use paramodulation or superposition.

- - -

First-order logic has a sound, complete, and effective proof system, so every valid sentence has a finite derivation. No algorithm decides validity. A fair proof-search procedure, which eventually examines every generated inference, can enumerate derivations and halt when it finds one. Validity is therefore semidecidable and undecidable.

The methods below use this fact in different ways. Instantiation, resolution, and tableaux search for a refutation of $S \cup \{\neg\varphi\},$ while forward and backward chaining derive queries directly from definite clauses. Under their stated completeness conditions, fair versions of these methods halt when the required entailment holds, but they need not halt when it fails.

## Instantiation and the Herbrand universe

The first approach replaces quantified clauses with ground instances and calls a propositional procedure. A ground term is a term with no variables. Universal instantiation replaces a universally quantified sentence by an instance:

$$
\frac{\forall x\ \varphi}{\varphi[t/x]}
$$

The rule is sound for every ground term $t$ of the language, since $\forall x \varphi$ asserts $\varphi$ of every element of the domain and $t$ denotes one of them. Existential quantifiers must be eliminated before grounding. In the simplest case, a top-level existential sentence is replaced by an instance built with a new constant:

$$
\exists x\ \varphi \quad \rightsquigarrow \quad \varphi[c/x] \qquad c \ \text{fresh}
$$

Here $c$ must not occur anywhere in the current set of sentences. The replacement preserves satisfiability but not logical equivalence. Freshness is essential because a constant already in use may be constrained to denote a different object. For example, $\{\exists x\ P(x), \neg P(c)\}$ is satisfiable, whereas replacing the existential sentence by $P(c)$ makes the set unsatisfiable. A model of $\exists x P(x)$ has a witness $d,$ and expanding it by interpreting the fresh $c$ as $d$ gives a model of $P(c).$ Conversely, any model of $P(c),$ restricted to the original language, satisfies $\exists x P(x).$

A refutation procedure needs only satisfiability preservation, since its goal is to establish unsatisfiability. When an existential quantifier lies within the scope of universal quantifiers, its witness may depend on their variables, so the replacement requires a fresh Skolem function rather than a constant. The general construction appears in the section on clausal form.

After Skolemization, the ground terms available for universal instantiation form the Herbrand universe of the clause set. It consists of all ground terms built from the finite signature occurring in the clauses, with one constant added if none occurs. For a signature with a constant $e$ and a unary function symbol $i,$ this set is

$$
\{\ e,\ i(e),\ i(i(e)),\ i(i(i(e))),\ \dots\ \}
$$

The set is infinite whenever a function symbol of positive arity is present, so instantiation cannot be run to completion. Herbrand's theorem makes the enumeration usable.

> A set of clauses is unsatisfiable if and only if some finite set of ground instances of its clauses is unsatisfiable as a propositional set.

- - -

For each $n,$ generate the ground instances whose terms have depth at most $n$ and treat every ground atom as a propositional atom. Test the resulting propositional set for satisfiability, and increase $n$ if the test succeeds. When $S \models \varphi,$ the theorem guarantees that some finite level yields an unsatisfiable propositional set and the procedure halts. When $S \not\models \varphi,$ every level is satisfiable and the procedure runs forever.

The enumeration grows rapidly. With $k$ constants and one binary function symbol, the number of ground terms of depth at most $n$ grows doubly exponentially in $n,$ and every clause with $m$ variables contributes one instance per assignment of ground terms to its variables. Most of those instances are irrelevant to the refutation. The methods that follow avoid generating them by instantiating only as far as a particular inference step requires.

## Unification

A substitution is a finite map from variables to terms, written $\theta = \{x_1/t_1, \dots, x_n/t_n\},$ and $E\theta$ denotes the result of applying it simultaneously to every free occurrence of the $x_i$ in the expression $E.$ Substitutions compose: $E(\theta\sigma) = (E\theta)\sigma.$

A substitution $\theta$ unifies two expressions $E_1$ and $E_2$ when $E_1\theta = E_2\theta$ as strings. A unifier $\theta$ is most general when every unifier $\sigma$ of the same pair factors as $\sigma = \theta\rho$ for some substitution $\rho.$ The standard unification algorithm computes a most general unifier or reports that none exists. It scans the two expressions from left to right and resolves their first disagreement:

+ If neither side of the disagreement is a variable, the pair has no unifier.
+ If one side is a variable $x$ and the other is a term $t$ not containing $x,$ extend the substitution with $x/t$ and continue.
+ If one side is a variable $x$ and the other is a term $t$ containing $x,$ the pair has no unifier.

After adding a binding, the algorithm applies it to both expressions and to the substitution accumulated so far before scanning again. The last clause is the occurs check. The atoms $P(x)$ and $P(f(x))$ illustrate it. Any unifier would have to make $x$ and $f(x)$ the same term, and no finite term equals its own image under $f.$ Omitting the occurs check may make the algorithm loop or produce an infinite term. Implementations that omit it for speed are therefore unsound on such inputs.

The most general unifier is unique up to renaming of variables, so an algorithm may return any of its variants. Its generality matters for completeness. Unifying $P(x, b)$ and $P(y, b)$ with $\{x/c, y/c\}$ is legitimate but commits both variables to one constant, whereas the most general unifier $\{y/x\}$ leaves the variables available for later instantiation.

The following two cases illustrate the algorithm. For $D(g(x,b), y)$ and $D(z, g(z,b)),$ unifying the first arguments gives $z/g(x,b).$ After this binding is applied, the second arguments are $y$ and $g(g(x,b), b),$ so the most general unifier is

$$
\theta = \{\ z/g(x,b),\ y/g(g(x,b), b)\ \}
$$

The atoms $P(x, f(x))$ and $P(g(y), y)$ cannot be unified. Unifying the first arguments gives $x/g(y).$ The second arguments then require $f(g(y))$ and $y$ to be unified, and $y$ occurs in $f(g(y)),$ so the occurs check rejects the pair.

Variables belong to the clause that contains them, and the same variable in two clauses stands for two independent universal quantifiers. Before any inference, the clauses are standardized apart by renaming their variables so that no variable occurs in more than one of them. Without this step, the query $D(x, b)$ against a clause containing $D(a, x)$ fails on a spurious conflict, since $x$ cannot take the two values at once. Renaming the second occurrence to $x'$ removes the conflict and gives the unifier $\{x/a, x'/b\}.$

## Generalized modus ponens

Unification makes it possible to reason in first-order form without instantiating anything in advance. The rule combines instantiation and modus ponens into one step. Given atoms $p_1', \dots, p_n'$ known to hold and an implication $(p_1 \wedge \cdots \wedge p_n) \rightarrow q$ whose variables are universally quantified, if a substitution $\theta$ satisfies $p_i'\theta = p_i\theta$ for every $i,$ then

$$
\frac{p_1' \quad \cdots \quad p_n' \qquad (p_1 \wedge \cdots \wedge p_n) \rightarrow q}{q\theta}
$$

The rule is sound. Applying $\theta$ to the universally quantified implication is a sequence of universal instantiations, and applying it to each $p_i'$ likewise. The premises of the instantiated implication are the instantiated facts, and propositional modus ponens gives $q\theta.$ The substitution is required to act on the facts as well as on the rule, because a known fact may itself contain variables. From the fact $D(a, y)$ and the rule with premise $D(x, z),$ the substitution $\{x/a, z/y\}$ makes the two atoms identical.

The rule applies to definite clauses, that is, clauses with exactly one positive literal, written as implications whose antecedent is a conjunction of positive literals. Consider the following knowledge base over a signature with constant symbols $2,$ $6,$ $42,$ a unary predicate $P$ for primality, a binary predicate $D$ for divisibility, and a unary predicate $F$ read as "has a prime divisor":

$$
\begin{array}{lll}
R_1 & P(u) \wedge D(u, v) \rightarrow F(v) & \\[6pt]
R_2 & D(x, y) \wedge D(y, z) \rightarrow D(x, z) & \\[6pt]
A_1 & P(2) & \text{fact} \\[6pt]
A_2 & D(2, 6) & \text{fact} \\[6pt]
A_3 & D(6, 42) & \text{fact}
\end{array}
$$

All variables are implicitly universally quantified, so the quantifiers are omitted. The rule $R_1$ says that a number divisible by a prime satisfies $F,$ and $R_2$ states the [transitivity of divisibility](../integers/). The query is $F(42).$

## Forward chaining

Forward chaining starts from the facts and applies generalized modus ponens to any rule whose premises unify with facts already derived, adding the instantiated conclusion. The process stops when the query is derived or when no application adds anything new.

For the knowledge base above, the derivation has two steps:

$$
\begin{array}{clll}
\text{step} & \text{rule} & \text{unifier} & \text{new fact} \\[6pt]
\hline
1 & R_2 & \{\ x/2,\ y/6,\ z/42\ \} & D(2, 42) \\[6pt]
2 & R_1 & \{\ u/2,\ v/42\ \} & F(42)
\end{array}
$$

Step $1$ matches the two premises of $R_2$ against $A_2$ and $A_3.$ The common value $6$ of $y$ forces the two facts to chain. Step $2$ matches the premises of $R_1$ against $A_1$ and the fact just derived. The query appears at step $2,$ so the knowledge base entails $F(42).$

Termination is no longer automatic. In the propositional case only finitely many distinct atoms can be added. Here a rule may build new terms. A knowledge base containing $N(x) \rightarrow N(s(x))$ and the fact $N(e)$ derives $N(s(e)),$ then $N(s(s(e))),$ and never stops. Forward chaining terminates for a finite Datalog program, where no function symbol has positive arity. The Herbrand universe then consists of the finitely many constants in the program, with one constant added if none occurs, so only finitely many ground atoms can be derived.

The naive procedure also repeats work. At each round it retries every rule against every combination of facts, including those tested in earlier rounds. An incremental implementation records, for each new fact, the rules whose premises it can match, and it tests only those combinations that involve at least one fact added in the previous round.

## Backward chaining

Backward chaining starts from the query and works towards the facts. A goal is unified with the head of a rule, the premises of that rule become new goals under the resulting substitution, and a goal that unifies with a fact is discharged. Substitutions found along the way are composed and applied to the goals that remain.

On the query $F(42)$ the search runs as follows. The goal unifies with the head of $R_1$ under $\{v/42\},$ which leaves the goals $P(u)$ and $D(u, 42).$ The first unifies with the fact $A_1$ under $\{u/2\},$ and applying this substitution to the second goal turns it into $D(2, 42).$ That goal unifies with the head of $R_2$ under $\{x/2, z/42\},$ leaving $D(2, y)$ and $D(y, 42).$ The fact $A_2$ discharges the first under $\{y/6\},$ and the second becomes $D(6, 42),$ which is the fact $A_3.$

The same derivation can be displayed as follows:

$$
\begin{array}{c}
F(42) \\[6pt]
\downarrow \ R_1, \ \{\ v/42\ \} \\[6pt]
P(u), \ D(u, 42) \\[6pt]
\downarrow \ A_1, \ \{\ u/2\ \} \\[6pt]
D(2, 42) \\[6pt]
\downarrow \ R_2, \ \{\ x/2,\ z/42\ \} \\[6pt]
D(2, y), \ D(y, 42) \\[6pt]
\downarrow \ A_2, \ \{\ y/6\ \} \\[6pt]
D(6, 42) \\[6pt]
\downarrow \ A_3 \\[6pt]
\text{success}
\end{array}
$$

Every goal is discharged, so the knowledge base entails $F(42),$ and the composed substitution $\{u/2, v/42, x/2, y/6, z/42\}$ records the values used in the derivation. For a query with variables, the answer is the restriction of the composed substitution to those variables. Replacing the initial query by $F(w)$ in the displayed derivation returns $\{w/42\},$ while another branch returns $\{w/6\}$ directly from $A_1$ and $A_2.$

The order in which alternatives are tried affects the search. Depth-first traversal with chronological backtracking, the strategy of Prolog, is a common choice, and it does not terminate on every definite knowledge base. The transitivity rule $R_2$ shows why. A goal $D(s, t)$ matches the head of $R_2$ and produces the subgoal $D(s, y),$ which matches the head of $R_2$ again and produces $D(s, y'),$ and the recursion descends without ever consulting a fact. Trying matching facts before the recursive rule lets the displayed derivation succeed, but it does not ensure termination for every query. Tabling prevents repeated expansion of variant goals, including this loop, but it cannot stop a search that generates infinitely many distinct goals.

Under fair search, forward chaining derives every ground atom entailed by the knowledge base, whether the query needs it or not, while backward chaining examines only the rules whose heads match a current goal. Backward chaining may prove the same subgoal several times along different branches. Both inference schemes are complete for definite clauses under this condition. Neither handles a clause with two positive literals, since such a clause has no single conclusion to chain on.

## Clausal form

Resolution applies beyond the definite-clause fragment, but it requires clauses. An arbitrary first-order sentence must therefore be converted. The conversion has six steps, applied in order.

+ Eliminate $\leftrightarrow$ and $\rightarrow$ by the equivalences $\varphi \leftrightarrow \psi \equiv (\varphi \rightarrow \psi) \wedge (\psi \rightarrow \varphi)$ and $\varphi \rightarrow \psi \equiv \neg\varphi \lor \psi.$
+ Move every negation inward by the double negation law, De Morgan's laws, and the quantifier dualities $\neg\forall x\varphi \equiv \exists x \neg\varphi$ and $\neg\exists x\varphi \equiv \forall x \neg\varphi.$
+ Standardize the variables apart, so that each quantifier binds a variable that occurs nowhere else, and move all quantifiers to the front to obtain prenex normal form.
+ Skolemize, replacing each existentially quantified variable by a term as described below.
+ Drop the universal quantifiers, which bind every remaining variable.
+ Distribute $\lor$ over $\wedge$ until the formula is a conjunction of clauses.

Skolemization is the step with no propositional analogue. An existential quantifier inside the scope of the universal quantifiers on $x_1, \dots, x_k$ is removed by replacing its variable with $f(x_1, \dots, x_k),$ where $f$ is a function symbol not occurring in the language. When $k = 0,$ the replacement is a new constant. The arguments of the Skolem term are the universally quantified variables whose scope contains the existential quantifier, so they record the possible dependence of its witness:

$$
\forall x \forall y \exists z\ S(x,y,z) \quad \text{gives} \quad S(x, y, h(x,y)) \qquad \exists z \forall x \forall y\ S(x,y,z) \quad \text{gives} \quad S(x,y,c)
$$

In the first sentence the witness may vary with $x$ and $y,$ so the Skolem symbol is a binary function. In the second a single $z$ serves for all $x$ and $y,$ so the Skolem symbol is a constant.

Skolemization preserves satisfiability but not logical equivalence. The sentence $\exists x\ P(x)$ and its Skolemization $P(c)$ are not equivalent. For example, a structure whose domain is $\{1,2\}$ with $P^{\mathcal{M}} = \{1\}$ and $c^{\mathcal{M}} = 2$ satisfies the first and falsifies the second. They are equisatisfiable. Every model of $P(c)$ satisfies $\exists x P(x),$ and every model of $\exists x P(x)$ becomes a model of $P(c)$ once the new symbol $c$ is interpreted as a witness. A refutation procedure needs only equisatisfiability, because the original set has no model exactly when the clause set has none. For a complete conversion, consider the sentence

$$
\forall x\ (P(x) \rightarrow \exists y\ (Q(y) \wedge R(x,y)))
$$

Eliminating the conditional gives $\forall x\ (\neg P(x) \lor \exists y\ (Q(y) \wedge R(x,y))).$ The negation is already innermost and the variables are already apart. Moving the quantifiers to the front gives

$$
\forall x \exists y\ (\neg P(x) \lor (Q(y) \wedge R(x,y)))
$$

The existential quantifier on $y$ lies inside the scope of $\forall x,$ so its variable is replaced by $f(x).$ Dropping $\forall x$ leaves

$$
\neg P(x) \lor (Q(f(x)) \wedge R(x, f(x)))
$$

Distributing produces two clauses:

$$
\{\ \neg P(x),\ Q(f(x))\ \} \qquad \{\ \neg P(x),\ R(x, f(x))\ \}
$$

For a concrete interpretation, let $P$ and $Q$ both say "is a positive real" and let $R(x,y)$ say $y < x.$ The sentence asserts that every [positive real](../real-numbers/) has a smaller positive real. The function $f(x) = x/2$ supplies such a witness, and the Skolem function makes the selected witness explicit.

## Resolution with unification

The propositional resolution rule cancels a complementary pair of literals. Its first-order form cancels a pair that unification can make complementary. Let $C \cup \{l_1\}$ and $D \cup \{l_2\}$ be clauses with no variable in common, and let $\theta$ be a most general unifier of $l_1$ and the complement of $l_2.$ The rule is

$$
\frac{C \cup \{l_1\} \qquad D \cup \{l_2\}}{(C \cup D)\theta}
$$

Soundness follows from the propositional case. The clauses are universally quantified, so their instances under $\theta$ are consequences of them, and those instances contain a complementary pair on which propositional resolution applies.

Binary resolution alone is not refutation complete. The two clauses $\{P(x), P(y)\}$ and $\{\neg P(u), \neg P(v)\}$ are jointly unsatisfiable, since the first says that $P$ holds of every object and the second that it holds of none. Resolving two clauses of two literals each cancels one literal from each and leaves two, and the two survivors here are atoms on distinct variables that no unifier of the cancelled pair identifies. Every clause derivable from the two therefore has exactly two literals, and $\square$ never appears. Factoring supplies the missing inference. If two literals of the same sign in one clause have a most general unifier $\theta,$ one may apply $\theta$ to the whole clause and merge the resulting duplicate literals. Factoring the first clause with $\{y/x\}$ gives $\{P(x)\},$ factoring the second with $\{v/u\}$ gives $\{\neg P(u)\},$ and one resolution step then yields $\square.$

Resolution with factoring is refutation complete for first-order clauses. A finite set of clauses is unsatisfiable if and only if $\square$ has a derivation from it. The proof combines Herbrand's theorem, which reduces unsatisfiability to a finite set of ground instances, with a lifting lemma stating that any resolution step available between ground instances is the instance of a step available between the clauses themselves. A fair proof search is guaranteed to find a refutation when the input clauses are unsatisfiable, but it may run forever on a satisfiable input.

## A resolution refutation

The knowledge base of the chaining sections, together with the negated query, gives the following clauses. Definite clauses become clauses with one positive literal, and the negated query is purely negative.

$$
\begin{array}{rll}
C_1 & \neg P(u) \lor \neg D(u, v) \lor F(v) & \text{from } R_1 \\[6pt]
C_2 & \neg D(x, y) \lor \neg D(y, z) \lor D(x, z) & \text{from } R_2 \\[6pt]
C_3 & P(2) & \text{fact} \\[6pt]
C_4 & D(2, 6) & \text{fact} \\[6pt]
C_5 & D(6, 42) & \text{fact} \\[6pt]
C_6 & \neg F(42) & \text{negated query}
\end{array}
$$

Resolving from the negated query towards the facts produces a refutation in five steps:

$$
\begin{array}{rlll}
C_7 & \neg P(u) \lor \neg D(u, 42) & C_1, C_6 & \{\ v/42\ \} \\[6pt]
C_8 & \neg D(2, 42) & C_7, C_3 & \{\ u/2\ \} \\[6pt]
C_9 & \neg D(2, y) \lor \neg D(y, 42) & C_8, C_2 & \{\ x/2,\ z/42\ \} \\[6pt]
C_{10} & \neg D(6, 42) & C_9, C_4 & \{\ y/6\ \} \\[6pt]
C_{11} & \square & C_{10}, C_5 & \{\ \}
\end{array}
$$

Each line records the two parent clauses and the most general unifier of the literals cancelled. Step $C_9$ resolves a unit clause against the positive literal of the transitivity clause. Its two negative literals remain and correspond to the subgoals of a backward chaining step. The empty clause appears, so the six clauses have no model, and the knowledge base entails $F(42).$

- - -

The refutation above resolves at each step against the clause descended from the negated query. This restriction is linear resolution, and further restricting one parent of every step to be an input clause gives input resolution, which is complete for Horn clauses and incomplete in general. Unrestricted saturation of a first-order clause set generates many clauses, so implementations combine such restrictions with orderings on literals and with subsumption. Subsumption deletes a clause $D$ when another clause $C$ already present has a substitution $\theta$ such that $C\theta \subseteq D.$

## Tableaux with quantifier rules

The tableau method extends to first-order logic by adding the gamma and delta rule families to the propositional alpha and beta rules. The alpha rules expand a formula whose truth requires both components and do not split the branch, while the beta rules expand a formula whose truth admits two cases and split it. The gamma rules govern formulas of universal force, and the delta rules govern formulas of existential force. Their quantifier forms are:

$$
\begin{array}{c|c|c}
 & \text{formula} & \text{expansion} \\[6pt]
\hline
\gamma_1 & \forall x\varphi & \varphi[t/x] \ \text{for any ground term } t \ \text{in the branch language} \\[6pt]
\gamma_2 & \neg\exists x\varphi & \neg\varphi[t/x] \ \text{for any ground term } t \ \text{in the branch language} \\[6pt]
\delta_1 & \exists x\varphi & \varphi[c/x] \ \text{for a constant } c \ \text{new to the branch} \\[6pt]
\delta_2 & \neg\forall x\varphi & \neg\varphi[c/x] \ \text{for a constant } c \ \text{new to the branch}
\end{array}
$$

The side conditions distinguish the two kinds of expansion.

+ A delta expansion introduces a constant that occurs nowhere on the branch, because the formula asserts that some object has a property and says nothing about which. Reusing a constant already present would assert that a named object has it, which does not follow.
+ A gamma expansion may use any ground term built from the constants and function symbols in the branch language. The gamma formula stays on the branch and may be expanded again with a different term, because a universal formula holds of every object and one instance rarely suffices. If a branch has no ground term when its first gamma formula is expanded, a fresh constant is added as a parameter that names an arbitrary element of the nonempty domain.

This asymmetry can prevent termination. A delta expansion is used once and adds a new constant; a gamma expansion can be repeated indefinitely, and each new constant supplies fresh terms for further gamma expansions. A closed tableau, when one exists, is found by fair application of the rules; an open branch may grow forever.

A tableau proof of a sentence $\varphi$ starts from $\neg\varphi$ and closes every branch. The first example is one direction of the quantifier duality, $\neg\forall x P(x) \rightarrow \exists x \neg P(x).$ Its closed tableau is:

$$
\begin{array}{c}
\neg(\neg\forall x P(x) \rightarrow \exists x \neg P(x)) \\[6pt]
\downarrow \ \alpha \\[6pt]
\neg\forall x P(x), \ \neg\exists x \neg P(x) \\[6pt]
\downarrow \ \delta_2 \\[6pt]
\neg P(c) \\[6pt]
\downarrow \ \gamma_2, \ t = c \\[6pt]
\neg\neg P(c) \\[6pt]
\downarrow \ \alpha \\[6pt]
P(c) \\[6pt]
\times
\end{array}
$$

The alpha step is the rule for a negated conditional, which asserts the antecedent and denies the consequent. The delta step introduces $c$ as a witness to the failure of $\forall x P(x).$ The gamma step then instantiates the second formula at that same $c,$ which is legitimate because $c$ is now a term of the branch. The branch contains $P(c)$ and $\neg P(c)$ and closes, so the sentence is valid. Expanding the delta formula first supplies $c$ for the gamma step and avoids an unnecessary initial parameter.

The second example is an invalid direction of quantifier exchange, $\forall x \exists y\ R(x,y) \rightarrow \exists y \forall x\ R(x,y).$ The alpha step gives $\forall x \exists y R(x,y)$ and $\neg\exists y \forall x R(x,y).$ Since no ground term is available, the first gamma expansion introduces $c_0$ and gives $\exists y\ R(c_0, y).$ A delta expansion then gives $R(c_0, c_1).$ A gamma expansion of the second formula at $c_1$ gives $\neg\forall x\ R(x, c_1),$ and a delta expansion gives $\neg R(c_2, c_1).$ The branch now contains the following formulas:

$$
R(c_0, c_1), \ \neg R(c_2, c_1)
$$

They are not complementary. The constant $c_2$ is available for a further gamma expansion of the first formula. Expanding it at $c_2$ and then applying the delta rule gives $R(c_2, c_3).$ Expanding the second gamma formula at $c_3$ and applying the delta rule gives $\neg R(c_4, c_3).$ The pattern repeats, so the branch never closes and never saturates.

The sentence is not valid, and the branch suggests a counter-model. Take the [natural numbers](../natural-numbers/) $\mathbb{N}$ as the domain and interpret $R(m,n)$ as $m < n.$ Then $\forall x \exists y\ R(x,y)$ is true, while $\exists y \forall x\ R(x,y)$ is false because no natural number exceeds every natural number. The limit of a fair, fully expanded open branch determines a model of the formulas at its root. Tableau search may therefore fail to terminate on an invalid sentence.

> Free-variable tableaux avoid choosing a term for each gamma expansion. They instantiate a gamma formula with a fresh variable, leave the choice open, and close a branch when two literals of opposite signs have unifiable atoms, applying the resulting substitution to the whole tableau. The delta rule then introduces a Skolem term whose arguments are the free variables in scope, exactly as in the clausal conversion.

## Decidability and restricted fragments

Instantiation, resolution with factoring, and fair tableaux are semidecision procedures for unrestricted first-order logic in the equality-free setting used here. They halt when the entailment holds but need not halt when it fails. Propositional validity and entailment are coNP-complete but decidable, whereas first-order validity is undecidable.

Fragments of the language recover decidability by restricting what can be written. The following fragments are decidable:

+ Monadic first-order logic has only predicate symbols of arity $1$ and no function symbols of positive arity.
+ The Bernays-Schönfinkel class consists of sentences whose prenex form has a block of existential quantifiers followed by a block of universal ones and whose signature has no function symbols of positive arity. Skolemization introduces only constants, so the Herbrand universe stays finite.
+ The two-variable fragment over relational signatures uses only two variable symbols, which may be reused by different quantifiers. Its satisfiability problem is NEXPTIME-complete.
+ The guarded fragment over relational signatures permits quantification in the forms $\exists\bar y\ (G(\bar x,\bar y) \wedge \varphi)$ and $\forall\bar y\ (G(\bar x,\bar y) \rightarrow \varphi),$ where the atomic guard $G$ contains every variable free in $\varphi.$

Two further restrictions appeared above. Datalog forbids function symbols of positive arity in definite clauses, which bounds the Herbrand universe by the constants of the program and makes forward chaining terminate. Description logics underlie OWL 2 DL, whose syntactic restrictions preserve decidability of its standard reasoning problems.

These restrictions exclude some first-order formulas but provide decision procedures that halt on every input. For unrestricted first-order logic, fair proof search terminates when a proof exists but may run forever when none exists.
