---
title: Automated Deduction in Propositional Logic
source: https://algebrica.org/automated-deduction-in-propositional-logic/
license: CC BY-NC 4.0
tags:
  - automated-deduction
  - backward-chaining
  - clause
  - conjunctive-normal-form
  - empty-clause
  - forward-chaining
  - horn-clause
  - propositional-logic
  - refutation
  - resolution
  - satisfiability
  - semantic-tableaux
  - unit-resolution
---

## Refutation

A deduction procedure for [propositional logic](../propositional-logic/) answers questions of the following form. Given a finite set $S$ of formulas and a formula $\varphi,$ does $S \models \varphi$ hold? The definition of logical consequence quantifies over all interpretations, so the direct test inspects the $2^n$ rows of a truth table on the $n$ atomic propositions occurring in $S \cup \{\varphi\}.$ The procedures described here replace that inspection by a test of unsatisfiability applied to the premises together with the negated conclusion.

The equivalence that licenses the replacement is the following.

$$
S \models \varphi \Longleftrightarrow S \cup \{\neg\varphi\} \ \text{is unsatisfiable}
$$

Assume $S \models \varphi$ and let $M$ satisfy every formula of $S \cup \{\neg\varphi\}.$ From $M \models S$ we get $M \models \varphi,$ while $M \models \neg\varphi$ gives $M \not\models \varphi,$ and no interpretation makes $\varphi$ both true and false. Hence no such $M$ exists. Conversely, assume that $S \cup \{\neg\varphi\}$ is unsatisfiable and let $M \models S.$ If $\varphi$ were false under $M,$ then $M$ would satisfy $\neg\varphi$ and therefore the whole set. So every model of $S$ is a model of $\varphi.$

A refutation is a derivation showing that a set of formulas is unsatisfiable. The resolution and tableau procedures below add $\neg\varphi$ to the premises and search for such a refutation of the enlarged set. On finite propositional inputs, both procedures terminate and decide the entailment. The later sections on forward and backward chaining answer the same question for premises of a restricted form by traversing the rules directly.

## Clauses and the resolution rule

Resolution takes formulas in conjunctive normal form. A literal is an atomic proposition or its negation, and a clause is a disjunction of literals. Since $\lor$ is associative, commutative and idempotent, neither the order nor repetition of literals matters, so a clause is identified with the set of its literals. The clause $p \lor \neg q \lor r$ is then the set $\{p, \neg q, r\},$ and a CNF formula is a set of clauses read conjunctively. The empty clause is written $\square.$ By convention, the disjunction of no literals is false under every interpretation, so $\square$ is unsatisfiable.

Two literals are complementary when one is the negation of the other. If $C$ and $D$ are clauses and $l$ is a literal, the resolution rule is:

$$
\frac{C \cup \{l\} \qquad D \cup \{\neg l\}}{C \cup D}
$$

The conclusion $C \cup D$ is the resolvent of the two premises on the literal $l.$ The rule is sound. Let $M$ satisfy both premises. If $M \models l,$ then $M \not\models \neg l,$ so $M$ makes some literal of $D$ true; if $M \not\models l,$ then $M$ makes some literal of $C$ true. In either case $M$ satisfies $C \cup D.$

Unit resolution is the special case in which one premise is a single literal. Taking $C = \varnothing$ and $D = \varnothing$ resolves $p$ against $\neg p$ and produces $\square.$ Resolution also yields two familiar rules. From $p$ and $\neg p \lor q,$ the clause form of $p \rightarrow q,$ resolution gives $q,$ which is modus ponens. From $\neg q$ and the same clause, it gives $\neg p,$ which is modus tollens.

> Each application cancels one complementary pair. Cancelling two pairs at once is unsound, since the clauses $p \lor q$ and $\neg p \lor \neg q$ would give $\square,$ although the interpretation $M(p) = T,$ $M(q) = F$ satisfies both. The two legitimate resolvents of that pair are $q \lor \neg q$ and $p \lor \neg p,$ which are tautologies.

## The resolution procedure

To decide whether $S \models \varphi,$ the procedure performs three steps.

+ Convert $S \cup \{\neg\varphi\}$ into a set of clauses.
+ Systematically choose two clauses containing a complementary pair, compute their resolvent, and add it to the set if it is not already present.
+ Repeat until $\square$ appears, in which case $S \models \varphi,$ or until no application produces a new clause, in which case $S \not\models \varphi.$

The procedure terminates. On $n$ atomic propositions each atom occurs in a clause positively, negatively, in both forms, or not at all. At most $4^n$ distinct clauses can therefore be formed, so the clause set can grow only finitely many times. By soundness, deriving $\square$ proves that the initial clauses are jointly unsatisfiable. If saturation ends without $\square,$ refutation completeness guarantees that the clause set is satisfiable, and a model can be constructed from it.

Refutation completeness does not say that saturating $S$ alone derives every clausal consequence of $S.$ From the clause $p$ no resolution step is possible, yet $p \models p \lor q.$ The procedure decides entailment through the negated conclusion rather than by generating all consequences of a clause set.

> Converting a formula to CNF by the distributive laws can double the number of clauses at each step and produce a formula of exponential size. A definitional transformation assigns a fresh atom to each subformula and produces a CNF formula whose size is linear in the size of the original. The result is equisatisfiable with the original formula rather than logically equivalent to it. Equisatisfiability suffices for a refutation procedure.

- - -

Propositional satisfiability is NP-complete, even for formulas in CNF. Some unsatisfiable families, including standard CNF encodings of the negation of the pigeonhole principle, require resolution refutations of exponential size. Full saturation can therefore be impractical on large inputs. The DPLL procedure instead searches for a model by assigning atoms one at a time, propagating unit clauses, and backtracking when a clause becomes false. Modern SAT solvers usually extend this scheme with conflict-driven clause learning.

## A resolution refutation

Consider the propositional skeleton of a strong-induction argument that every integer greater than $1$ has a prime divisor, with the case distinction made explicit. The symbolization key over $P = \{p, q, r, s\}$ is the following:

+ $p =$ the integer $n$ is greater than $1$.
+ $q =$ the integer $n$ is prime.
+ $r =$ the integer $n$ has a divisor $d$ with $1 < d < n$.
+ $s =$ the integer $n$ has a prime divisor.

The premises are $p \rightarrow (q \lor r),$ $q \rightarrow s,$ $r \rightarrow s$ and $p,$ and the proposed conclusion is $s.$ In a strong-induction proof on $n,$ the implication $r \rightarrow s$ follows by applying the induction hypothesis to $d < n.$ Eliminating the conditionals gives four clauses, and the negated conclusion gives a fifth. Numbering them and resolving produces the following derivation:

$$
\begin{array}{rll}
C_1 & \neg p \lor q \lor r & \text{premise} \\[6pt]
C_2 & \neg q \lor s & \text{premise} \\[6pt]
C_3 & \neg r \lor s & \text{premise} \\[6pt]
C_4 & p & \text{premise} \\[6pt]
C_5 & \neg s & \text{negated conclusion} \\[6pt]
C_6 & q \lor r & \text{from } C_4 \ \text{and} \ C_1 \ \text{on} \ p \\[6pt]
C_7 & \neg q & \text{from } C_2 \ \text{and} \ C_5 \ \text{on} \ s \\[6pt]
C_8 & r & \text{from } C_6 \ \text{and} \ C_7 \ \text{on} \ q \\[6pt]
C_9 & \neg r & \text{from } C_3 \ \text{and} \ C_5 \ \text{on} \ s \\[6pt]
C_{10} & \square & \text{from } C_8 \ \text{and} \ C_9 \ \text{on} \ r
\end{array}
$$

The same derivation has a tree form, in which each horizontal line is one application of the rule and the leaves are the initial clauses:

$$
\dfrac{\dfrac{\dfrac{p \qquad \neg p \lor q \lor r}{q \lor r} \qquad \dfrac{\neg q \lor s \qquad \neg s}{\neg q}}{r} \qquad \dfrac{\neg r \lor s \qquad \neg s}{\neg r}}{\square}
$$

The empty clause appears, so the premises together with $\neg s$ have no model, and the premises entail $s.$

- - -

Saturation without $\square$ can instead yield a counter-model. Take the premises $p \rightarrow q$ and $q \rightarrow r,$ with $p$ as the proposed conclusion. The clauses are $\neg p \lor q,$ $\neg q \lor r$ and $\neg p,$ the last one coming from the negated conclusion. The only applicable step resolves the first two clauses on $q$ and yields $\neg p \lor r.$ After this addition, the only complementary literals in the set are $q$ and $\neg q,$ and resolving the clauses that contain them reproduces $\neg p \lor r:$

$$
\{\ \neg p \lor q, \ \neg q \lor r, \ \neg p, \ \neg p \lor r \ \}
$$

The set is closed under resolution and does not contain $\square.$ Hence the premises do not entail $p.$ The interpretation $M(p) = M(q) = M(r) = F$ makes every clause true and is a counter-model to the proposed entailment.

## Semantic tableaux

The tableau method decides satisfiability without any preliminary conversion. A tableau for a finite set of formulas is a tree whose nodes carry sets of formulas. The set at a node is read conjunctively, the branches issuing from a node are read disjunctively, and each expansion step replaces a compound formula by its components according to the truth conditions of its main connective.

The expansion rules fall into two groups. The alpha rules apply when satisfying a formula requires satisfying every component listed in the corresponding row, and they extend the current branch without splitting it.

$$
\begin{array}{c|c|cc}
 & \text{formula} & \text{first component} & \text{second component} \\[6pt]
\hline
\alpha_1 & \neg\neg\varphi & \varphi & \\[6pt]
\alpha_2 & \varphi \wedge \psi & \varphi & \psi \\[6pt]
\alpha_3 & \neg(\varphi \lor \psi) & \neg\varphi & \neg\psi \\[6pt]
\alpha_4 & \neg(\varphi \rightarrow \psi) & \varphi & \neg\psi
\end{array}
$$

The beta rules apply to formulas whose truth admits two cases. Each beta expansion splits the current branch into those cases.

$$
\begin{array}{c|c|cc}
 & \text{formula} & \text{left branch} & \text{right branch} \\[6pt]
\hline
\beta_1 & \varphi \lor \psi & \varphi & \psi \\[6pt]
\beta_2 & \neg(\varphi \wedge \psi) & \neg\varphi & \neg\psi \\[6pt]
\beta_3 & \varphi \rightarrow \psi & \neg\varphi & \psi \\[6pt]
\beta_4 & \varphi \leftrightarrow \psi & \varphi, \ \psi & \neg\varphi, \ \neg\psi \\[6pt]
\beta_5 & \neg(\varphi \leftrightarrow \psi) & \varphi, \ \neg\psi & \neg\varphi, \ \psi
\end{array}
$$

A branch is closed when it contains a formula and its negation, and the closure is marked with $\times.$ A branch is saturated when every formula on it is a literal or has already been expanded. The tableau for $S \cup \{\neg\varphi\}$ therefore has two possible outcomes:

+ If every branch closes, the set is unsatisfiable and $S \models \varphi.$
+ If some saturated branch stays open, its literals define an interpretation that satisfies the set and $S \not\models \varphi.$

For a finite root, every branch has bounded length because each compound formula is expanded at most once and each expansion adds formulas of lower connective complexity. Since each beta expansion creates two branches, the whole tableau is finite.

An open saturated branch contains no complementary pair of literals, so the assignment that makes each of its literals true is well defined. Extending this partial assignment arbitrarily to the atoms it does not fix gives a model of every formula on the branch, including the formulas at the root. Expanding alpha formulas before a beta split avoids repeating the same alpha step in both new branches, so this order often keeps the tree smaller.

## Tableau expansions

The first expansion tests the law of contraposition, that is, the validity of $(p \rightarrow q) \rightarrow (\neg q \rightarrow \neg p).$ The root is the negation of the formula. The rule $\alpha_4$ applies twice, followed by $\alpha_1$ and $\beta_3:$

$$
\begin{array}{c}
\neg((p \rightarrow q) \rightarrow (\neg q \rightarrow \neg p)) \\[6pt]
\downarrow \ \alpha_4 \\[6pt]
p \rightarrow q, \ \neg(\neg q \rightarrow \neg p) \\[6pt]
\downarrow \ \alpha_4 \\[6pt]
p \rightarrow q, \ \neg q, \ \neg\neg p \\[6pt]
\downarrow \ \alpha_1 \\[6pt]
p \rightarrow q, \ \neg q, \ p \\[6pt]
\swarrow \ \beta_3 \ \searrow \\[6pt]
\begin{array}{ccc}
\neg p, \ \neg q, \ p & \quad & q, \ \neg q, \ p \\[6pt]
\times & & \times
\end{array}
\end{array}
$$

The left branch contains $p$ and $\neg p,$ and the right branch contains $q$ and $\neg q,$ so both close. The negation of the formula is unsatisfiable and the formula is a tautology.

The second expansion tests whether $p \lor q \models q.$ The root is $\{p \lor q, \neg q\},$ and the only applicable rule is $\beta_1:$

$$
\begin{array}{c}
p \lor q, \ \neg q \\[6pt]
\swarrow \ \beta_1 \ \searrow \\[6pt]
\begin{array}{ccc}
p, \ \neg q & \quad & q, \ \neg q \\[6pt]
\text{open} & & \times
\end{array}
\end{array}
$$

The right branch closes, while the left branch is saturated and open. Its literals give the interpretation $M(p) = T$ and $M(q) = F,$ which satisfies $p \lor q$ and falsifies $q,$ so $p \lor q \not\models q.$ The interpretation read from the open branch is a counter-model, obtained without building the four rows of a truth table.

## Horn clauses

A Horn clause is a clause with at most one positive literal. Horn clauses have three forms, each equivalent to an implication:

+ A fact is a single positive literal $q,$ equivalent to $\top \rightarrow q.$
+ A rule is a clause $q \lor \neg p_1 \lor \cdots \lor \neg p_n$ with exactly one positive literal, equivalent to $(p_1 \wedge \cdots \wedge p_n) \rightarrow q.$
+ A goal is a clause with negative literals only, $\neg p_1 \lor \cdots \lor \neg p_n,$ equivalent to $(p_1 \wedge \cdots \wedge p_n) \rightarrow \bot.$

Facts and rules are called definite clauses because they contain exactly one positive literal. A knowledge base $KB$ of definite clauses is always satisfiable, since the interpretation that makes every atom true satisfies each of them. A query $q$ is answered by adding the goal $\neg q$ and refuting the result.

Unit resolution alone is refutation complete on Horn clauses. Repeatedly resolving a rule against available positive unit clauses removes its negative literals one at a time and eventually leaves its positive conclusion as a unit clause. Resolving a negative goal against available positive units likewise removes its literals one at a time; for an unsatisfiable Horn set, this process eventually yields $\square.$ Satisfiability of Horn clause sets can be decided in linear time, whereas the same question for arbitrary clauses is NP-complete. The linear bound depends on the restriction to at most one positive literal. A definite clause has a single conclusion and does not require a case distinction.

Forward and backward chaining traverse the rules of a definite knowledge base in opposite directions. Both use the following knowledge base, with $u$ as the query:

$$
\begin{array}{lll}
R_1 & p \wedge q \rightarrow r & \\[6pt]
R_2 & r \rightarrow s & \\[6pt]
R_3 & q \wedge s \rightarrow t & \\[6pt]
R_4 & r \wedge t \rightarrow u & \\[6pt]
F_1 & p & \text{fact} \\[6pt]
F_2 & q & \text{fact}
\end{array}
$$

## Forward chaining

Forward chaining starts from the known facts and repeatedly applies a rule whose premises are already known and whose conclusion is not yet known. The process stops when the query appears or when no rule adds anything new. Each step applies a rule whose premises are all in the current set:

$$
\begin{array}{cll}
\text{step} & \text{rule} & \text{known atoms} \\[6pt]
\hline
0 & & p, \ q \\[6pt]
1 & R_1 & p, \ q, \ r \\[6pt]
2 & R_2 & p, \ q, \ r, \ s \\[6pt]
3 & R_3 & p, \ q, \ r, \ s, \ t \\[6pt]
4 & R_4 & p, \ q, \ r, \ s, \ t, \ u
\end{array}
$$

The query $u$ enters the set at step $4.$ Hence $KB \models u.$ The procedure terminates because each applied rule adds a new atom and only finitely many atoms occur in the knowledge base. Every derived atom is entailed by $KB.$ If the procedure reaches a fixed point, the interpretation that makes exactly the known atoms true satisfies every rule, because any rule whose premises are true has already added its conclusion. Thus a query absent at the fixed point is not a consequence of $KB.$

The strategy is data-driven. When run to saturation, it derives all atoms entailed by $KB,$ including those the query does not need. In the knowledge base above, $s$ and $t$ are needed for $u,$ while a further rule such as $s \rightarrow v$ would also derive $v,$ which does not contribute to the answer.

## Backward chaining

Backward chaining starts from the query and works towards the facts. To establish an atom that is not already a fact, the procedure tries the rules whose conclusion is that atom and recursively establishes their premises. It succeeds if all the premises of at least one such rule can be established, and it fails only when every alternative fails. On the knowledge base above the query $u$ decomposes as follows:

$$
\begin{array}{c}
u \\[6pt]
\swarrow \ R_4 \ \searrow \\[6pt]
\begin{array}{ccc}
r & \quad & t \\[6pt]
\downarrow \ R_1 & & \downarrow \ R_3 \\[6pt]
p, \ q & & q, \ s \\[6pt]
 & & \downarrow \ R_2 \\[6pt]
 & & r \\[6pt]
 & & \downarrow \ R_1 \\[6pt]
 & & p, \ q
\end{array}
\end{array}
$$

The descendants under $R_4$ are conjunctive obligations, and both must be discharged. A beta tableau split instead records alternative ways to satisfy the expanded formula. Every leaf of the decomposition is a fact, so $KB \models u.$ Read from the leaves upwards, the same tree is a derivation by modus ponens:

$$
\dfrac{\dfrac{p \qquad q}{r} \qquad \dfrac{q \qquad \dfrac{\dfrac{p \qquad q}{r}}{s}}{t}}{u}
$$

The atom $r$ is derived twice in this tree, once as a premise of $R_4$ and once inside the derivation of $s,$ and the facts $p$ and $q$ are used more than once. An implementation stores proved atoms in a table and consults it before repeating the work. It also records active goals to detect cycles. A knowledge base containing $a \rightarrow b$ and $b \rightarrow a$ sends a naive recursion on the query $a$ into a cycle, while a procedure that records active goals ends that branch as soon as $a$ reappears. Other rules with conclusion $a$ remain available as alternatives.

The strategy is goal-driven. With rules indexed by their conclusions, it may inspect only the part of the knowledge base relevant to the query, whereas forward chaining may process rules that do not contribute to it.

## Scope of the three methods

Resolution, tableaux, and chaining decide entailment under different syntactic restrictions. They differ in the form they require, in what they return, and in their cost.

Resolution requires clauses. It returns a refutation or a saturated set from which a model of the premises together with the negated conclusion can be constructed. In the latter case, the model is a counter-model to the entailment. Conversion to CNF is a separate step, and introducing fresh atoms for the subformulas keeps the size of the resulting CNF linear in the size of the original formula.

Tableaux accept formulas of any shape and return either a closed tree or an open saturated branch. An open saturated branch gives a counter-model explicitly. With $k$ beta expansions along a branch, a tableau can nevertheless generate up to $2^k$ branches.

Horn satisfiability, and hence entailment of an atomic query from a definite knowledge base, can be decided in linear time. Forward and backward chaining apply to this restricted setting. Neither direction accepts a rule with a disjunctive head, such as $p \rightarrow (q \lor r),$ because its clausal form $\neg p \lor q \lor r$ has two positive literals. Resolution handles this formula as a non-Horn clause, while tableaux split on the disjunction.
