---
title: Propositional Logic
source: https://algebrica.org/propositional-logic/
license: CC BY-NC 4.0
tags:
  - atomic-proposition
  - conjunctive-normal-form
  - contradiction
  - disjunctive-normal-form
  - inference-rules
  - interpretation
  - logical-connective
  - logical-consequence
  - logical-equivalence
  - modus-ponens
  - modus-tollens
  - propositional-logic
  - satisfiability
  - semantics
  - tautology
  - truth-table
  - valuation
  - well-formed-formula
---

## Introduction

Propositional logic studies arguments whose validity depends on how propositional connectives combine propositions. It treats each atomic proposition as either true or false and determines the truth value of a compound proposition from the truth values of its components.

The subject matter of an atomic proposition is irrelevant to this calculation. If an argument has the form $p,$ $p \rightarrow q,$ therefore $q,$ its validity depends on that form, regardless of the propositions represented by $p$ and $q.$ This restriction makes propositional logic precise, but it also limits what the language can express.

## Propositional language

A propositional language $\mathrm{Prop}[P]$ has atomic symbols, logical connectives, and parentheses. The set $P$ contains the atomic proposition symbols, for example $P = \{p, q, r\}.$ Parentheses record how the connectives group the formulas.

The language used here has the following connectives:

+ Negation $\neg$
+ Conjunction $\wedge$
+ Disjunction $\lor$
+ Material conditional $\rightarrow$
+ Material biconditional $\leftrightarrow$
+ Exclusive disjunction $\oplus$

The choice of primitive connectives is conventional. The biconditional and exclusive disjunction can be defined from other connectives, but separate symbols make common formulas shorter.

A formula built from the symbols in $P$ according to the formation rules is a well-formed formula (WFF). Atomic propositions are the simplest WFFs, while every other WFF has one or more WFFs as immediate components.

## Logical connectives

A connective is truth-functional when the truth values of its immediate components uniquely determine the truth value of the compound formula. Every connective in $\mathrm{Prop}[P]$ is truth-functional.

+ The negation $\neg p$ is true exactly when $p$ is false.
+ The conjunction $p \wedge q$ is true exactly when $p$ and $q$ are both true.
+ The disjunction $p \lor q$ is true exactly when at least one of $p$ and $q$ is true. The connective $\lor$ has the inclusive meaning, so $p \lor q$ is also true when both disjuncts are true.
+ The material conditional $p \rightarrow q$ is false exactly when its antecedent $p$ is true and its consequent $q$ is false.
+ The material biconditional $p \leftrightarrow q$ is true exactly when $p$ and $q$ have the same truth value.
+ The exclusive disjunction $p \oplus q$ is true exactly when $p$ and $q$ have different truth values.

The direction of a conditional requires care. The proposition "$p$ only if $q$" is $p \rightarrow q,$ while "$p$ if $q$" is $q \rightarrow p.$ In the first formula, $p$ is a sufficient condition for $q,$ and $q$ is a necessary condition for $p.$

Ordinary language has connectives that are not truth-functional. The truth of "it is necessary that $p$" is not determined by the truth of $p$ alone. Words such as "but" and "although" can express a contrast that conjunction does not retain, while a counterfactual conditional is not, in general, truth-functional. A symbolization in propositional logic has only the truth-functional structure of the original proposition.

## Symbolization example

Consider a propositional language $\mathrm{Prop}[P]$ over $P = \{p, q\},$ with the following symbolization key:

+ $p =$ the door is open.
+ $q =$ the window is open.

The two atomic propositions and the connectives are enough to symbolize several compound propositions.

+ The door is not open is written $\neg p.$
+ The door and the window are both open is written $p \wedge q.$
+ The door or the window is open, possibly both, is written $p \lor q.$
+ If the door is open, then the window is open is written $p \rightarrow q.$
+ The door is open if and only if the window is open is written $p \leftrightarrow q.$
+ Either the door or the window is open, but not both, is written $p \oplus q.$
+ Neither the door nor the window is open is written $\neg(p \lor q).$
+ The negation of the conditional "if the door is open, then the window is open" is written $\neg(p \rightarrow q).$

Parentheses are necessary in the last two formulas because the negation has the entire compound formula as its scope. Thus $\neg(p \lor q)$ differs from $\neg p \lor q.$

## Formation rules

The formation rules are an inductive definition of the WFFs of $\mathrm{Prop}[P].$

+ Every atomic proposition $p \in P$ is a WFF.
+ If $\varphi$ is a WFF, then $\neg\varphi$ is a WFF.
+ If $\varphi$ and $\psi$ are WFFs, then each of $(\varphi \wedge \psi),$ $(\varphi \lor \psi),$ $(\varphi \rightarrow \psi),$ $(\varphi \leftrightarrow \psi),$ and $(\varphi \oplus \psi)$ is a WFF.
+ No other expression is a WFF.

The last clause excludes every string that cannot be obtained by finitely many applications of the preceding clauses. These clauses also determine the structure of each formula. Every compound WFF has a unique main connective, the connective applied at the last step of its construction.

We omit the outermost pair of parentheses when no ambiguity results. Under this convention, the main connective of $\neg(p \wedge q)$ is $\neg,$ while the main connective of $\neg p \wedge q$ is $\wedge.$ The scope of an occurrence of a connective is the subformula to which that occurrence applies. Parentheses therefore determine both the main connective and the scope of the inner connectives.

## Semantics

The semantics of propositional logic has two truth values:

$$
\mathrm{Bool} := \{\ T, F\ \}
$$

The characteristic truth tables define the connectives. A single table for the six connectives is the following:

$$
\begin{array}{cc|cccccc}
p & q & \neg p & p \wedge q & p \lor q & p \rightarrow q & p \leftrightarrow q & p \oplus q \\[6pt]
\hline
T & T & F & T & T & T & T & F \\[6pt]
T & F & F & F & T & F & F & T \\[6pt]
F & T & T & F & T & T & F & T \\[6pt]
F & F & T & F & F & T & T & F
\end{array}
$$

A complete truth table has one row for each assignment of truth values to the distinct atomic propositions in a formula. If a formula contains $n$ distinct atomic propositions, its complete truth table has $2^n$ rows. The column under the main connective contains the truth value of the whole formula on each assignment.

The table also gives the following logical equivalences:

+ $p \rightarrow q \equiv \neg p \lor q$
+ $p \leftrightarrow q \equiv (p \rightarrow q) \wedge (q \rightarrow p)$
+ $p \oplus q \equiv (p \lor q) \wedge \neg(p \wedge q)$

The symbol $\equiv$ is a metalanguage relation between formulas. It means that the formulas have the same truth value under every assignment. The symbol is not another connective of $\mathrm{Prop}[P].$

## Interpretations

An interpretation, also called a valuation in propositional logic, is a function that assigns a truth value to each atomic proposition in $P$:

$$
M : P \rightarrow \{T, F\}
$$

The value of a compound formula under $M$ is then determined recursively by its formation and the truth tables of the connectives.

+ If $\varphi$ is true under $M,$ we write $M \models \varphi$ and call $M$ a model of $\varphi.$
+ If $\varphi$ is false under $M,$ we write $M \not\models \varphi$ and call $M$ a counter-model of $\varphi.$

Consider the interpretation in which $p$ is true and $q$ is false. The formula $p \rightarrow \neg q$ has the following row:

$$
\begin{array}{cc|cc}
p & q & \neg q & p \rightarrow \neg q \\[6pt]
\hline
T & F & T & T
\end{array}
$$

Under this interpretation, the antecedent $p$ and the consequent $\neg q$ are true. Hence $p \rightarrow \neg q$ is true, and $M \models p \rightarrow \neg q.$

The following notions are defined by quantifying over interpretations.

+ A formula $\varphi$ is satisfiable if some interpretation satisfies it.
+ A formula $\varphi$ is a tautology if every interpretation satisfies it.
+ A formula $\varphi$ is a contradiction if no interpretation satisfies it.
+ A formula $\varphi$ is contingent if some interpretation satisfies it and some interpretation does not satisfy it.

Thus every tautology and every contingent formula is satisfiable, while every contradiction is unsatisfiable. A set of formulas $S$ is jointly satisfiable if some interpretation satisfies every formula in $S.$ If no such interpretation exists, $S$ is jointly unsatisfiable, or inconsistent.

Two formulas $\varphi$ and $\psi$ are logically equivalent when they agree under every interpretation:

$$
\varphi \equiv \psi \Longleftrightarrow \forall M \ (M \models \varphi \Longleftrightarrow M \models \psi)
$$

## Logical consequence

A formula $\varphi$ is a logical consequence of a set of formulas $S$ if every interpretation that satisfies all formulas in $S$ also satisfies $\varphi.$ This relation is written as follows:

$$
S \models \varphi
$$

Equivalently, no interpretation makes every formula in $S$ true and $\varphi$ false. The symbol $\models$ is a relation in the metalanguage, whereas $\rightarrow$ is a connective that forms a new formula. For two formulas $\varphi$ and $\psi,$ the connection between them is the following:

$$
\varphi \models \psi \Longleftrightarrow \models \varphi \rightarrow \psi
$$

Consider the set $S = \{p, p \rightarrow q\}$ and the proposed consequence $q.$ The relevant truth table is the following:

$$
\begin{array}{cc|c}
p & q & p \rightarrow q \\[6pt]
\hline
T & T & T \\[6pt]
T & F & F \\[6pt]
F & T & T \\[6pt]
F & F & T
\end{array}
$$

Only the first row makes both members of $S$ true, and that row also makes $q$ true. Therefore $S \models q.$ The corresponding inference rule is modus ponens.

## Inference rules

An inference rule is a schematic pattern for deriving a conclusion from one or more premises. If $S \vdash \varphi,$ then $\varphi$ has a derivation from premises in $S$ within the chosen proof system. The symbol $\vdash$ concerns derivations, while $\models$ concerns interpretations.

A proof system is sound when $S \vdash \varphi$ implies $S \models \varphi,$ and it is complete when $S \models \varphi$ implies $S \vdash \varphi.$ Standard proof systems for propositional logic have both properties.

Modus ponens derives $q$ from $p$ and $p \rightarrow q$:

$$
\frac{p \qquad p \rightarrow q}{q}
$$

Modus tollens derives $\neg p$ from $\neg q$ and $p \rightarrow q$:

$$
\frac{\neg q \qquad p \rightarrow q}{\neg p}
$$

The hypothetical syllogism derives $p \rightarrow r$ from $p \rightarrow q$ and $q \rightarrow r$:

$$
\frac{p \rightarrow q \qquad q \rightarrow r}{p \rightarrow r}
$$

In each schema, the formulas above the line are the premises and the formula below the line is the conclusion.

For example, let $p$ mean that it is raining, let $q$ mean that the ground is wet, and let $r$ mean that the match is cancelled. From $p \rightarrow q$ and $q \rightarrow r,$ the hypothetical syllogism gives $p \rightarrow r.$ If $p$ is also a premise, modus ponens gives $r.$

## Normal forms

A literal is an atomic proposition or the negation of an atomic proposition. A clause is a disjunction of literals, and a term is a conjunction of literals.

A formula is in conjunctive normal form (CNF) if it is a conjunction of clauses:

$$
(l_{1,1} \lor \cdots \lor l_{1,k}) \wedge (l_{2,1} \lor \cdots \lor l_{2,m}) \wedge \cdots
$$

A formula is in disjunctive normal form (DNF) if it is a disjunction of terms:

$$
(l_{1,1} \wedge \cdots \wedge l_{1,k}) \lor (l_{2,1} \wedge \cdots \wedge l_{2,m}) \lor \cdots
$$

In either normal form, only $\neg,$ $\wedge,$ and $\lor$ occur, and every negation has an atomic proposition as its scope. A single literal is both a clause and a term, so it is both a CNF formula and a DNF formula.

Every propositional formula is logically equivalent to a formula in CNF and to a formula in DNF. One conversion method first removes $\rightarrow,$ $\leftrightarrow,$ and $\oplus,$ then moves each negation inward by double negation and De Morgan's laws, and finally applies the distributive laws.

For example, consider $\neg(p \lor q) \rightarrow r.$ The equivalence $\varphi \rightarrow \psi \equiv \neg\varphi \lor \psi$ gives the following calculation:

$$
\neg(p \lor q) \rightarrow r \equiv \neg\neg(p \lor q) \lor r \equiv (p \lor q) \lor r
$$

The resulting formula is equivalent to $p \lor q \lor r.$ It is a single clause and is therefore in CNF. Since each disjunct is also a one-literal term, the same formula is in DNF.

A complete truth table gives another proof of the normal-form theorems. For DNF, take each row on which the original formula is true, form a term that is true only on that row, and disjoin those terms. For CNF, take each row on which the formula is false, form a clause that is false only on that row, and conjoin those clauses. When the formula is a contradiction, $p \wedge \neg p$ is an equivalent normal form. When it is a tautology, $p \lor \neg p$ is an equivalent normal form.

The DPLL procedure and several related satisfiability methods take CNF formulas as input.
