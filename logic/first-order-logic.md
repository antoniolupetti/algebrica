---
title: First-Order Logic
source: https://algebrica.org/first-order-logic/
license: CC BY-NC 4.0
tags:
  - atomic-formula
  - bound-variable
  - domain-of-discourse
  - existential-quantifier
  - first-order-logic
  - free-variable
  - interpretation
  - logical-consequence
  - model
  - predicate-symbol
  - satisfaction
  - second-order-logic
  - sentence
  - signature
  - structure
  - substitution
  - term
  - universal-quantifier
  - validity
  - variable-assignment
---

## Introduction

Consider the following argument. Every prime greater than $2$ is odd; the number $7$ is a prime greater than $2$; therefore $7$ is odd. A symbolization in [propositional logic](../propositional-logic/) assigns $p$ and $q$ to the premises and $r$ to the conclusion. The interpretation $M(p) = M(q) = T$ and $M(r) = F$ satisfies both premises and falsifies the conclusion, so $\{p, q\} \not\models r.$ The original argument is valid, whereas its propositional argument form is invalid.

The mismatch comes from the symbolization. Propositional logic treats an atom as a unit with a truth value, so the words "every", "prime", "greater than" and the name "$7$" leave no trace in the formulas. The symbolization therefore omits the link between the general premise and the particular premise.

First-order logic preserves this information. It analyses a proposition in terms of the objects it mentions, the properties and relations ascribed to them, and the quantifiers that say whether a claim concerns every object or at least one. We symbolize the three propositions as follows:

$$
\forall x\ ((P(x) \wedge G(x, c)) \rightarrow O(x)) \qquad P(d) \wedge G(d, c) \qquad O(d)
$$

Here $P$ reads "is prime", $O$ reads "is odd", $G$ reads "is greater than", and the constant symbols $c$ and $d$ name $2$ and $7.$ Instantiating the first premise at $d$ gives $(P(d) \wedge G(d, c)) \rightarrow O(d),$ and the second premise then yields $O(d).$

## Symbols and signatures

The symbols of a first-order language fall into two groups. We use the following logical symbols throughout:

+ An infinite supply of variables $x, y, z, x_1, x_2, \dots$
+ The connectives $\neg,$ $\wedge,$ $\lor,$ $\rightarrow,$ $\leftrightarrow$
+ The quantifiers $\forall$ and $\exists$
+ The equality symbol $=$
+ Parentheses and the comma

The non-logical symbols vary with the subject under discussion and form the signature $\Sigma$ of the language:

+ Constant symbols $a, b, c, \dots$
+ Function symbols $f, g, h, \dots,$ each with an arity $n \geq 1$
+ Predicate symbols $P, Q, R, \dots,$ each with an arity $n \geq 1$

A unary predicate symbol is used for a property, and a predicate symbol of arity $2$ or greater is used for a relation. Some presentations treat a constant symbol as a function symbol of arity $0,$ which shortens the definitions below by one clause. We use equality throughout, with its interpretation fixed as identity on the domain.

The signature determines which terms and formulas can be formed, but it does not assign meanings to the non-logical symbols. A signature with one binary predicate $D$ and no function symbols can express that $D$ is transitive, but it cannot contain a term for the greatest common divisor of two objects until a corresponding function symbol is added.

## Terms and formulas

A first-order language has two syntactic categories, terms and formulas. Terms name objects, formulas make assertions. The categories are disjoint, so a term is never a formula and a formula is never a term. This separation has no counterpart in propositional logic, where formulas are the only category.

The terms of $\Sigma$ are defined inductively:

+ Every variable is a term.
+ Every constant symbol of $\Sigma$ is a term.
+ If $f$ is an $n$-ary function symbol of $\Sigma$ and $t_1, \dots, t_n$ are terms, then $f(t_1, \dots, t_n)$ is a term.
+ Nothing else is a term.

A term containing no variable is a ground term. The formulas are then defined by a second induction:

+ If $P$ is an $n$-ary predicate symbol of $\Sigma$ and $t_1, \dots, t_n$ are terms, then $P(t_1, \dots, t_n)$ is a formula, called atomic.
+ If $t_1$ and $t_2$ are terms, then $t_1 = t_2$ is an atomic formula.
+ If $\varphi$ is a formula, then $\neg\varphi$ is a formula.
+ If $\varphi$ and $\psi$ are formulas, then $(\varphi \wedge \psi),$ $(\varphi \lor \psi),$ $(\varphi \rightarrow \psi)$ and $(\varphi \leftrightarrow \psi)$ are formulas.
+ If $\varphi$ is a formula and $x$ is a variable, then $\forall x\varphi$ and $\exists x\varphi$ are formulas.
+ Nothing else is a formula.

Atomic formulas correspond to the atomic propositions of propositional logic, and the connective clauses are unchanged. The quantifier clause has no propositional counterpart. In $\forall x\varphi$ and $\exists x\varphi,$ the formula $\varphi$ is the scope of the quantifier occurrence.

Precedence conventions carry over, with the quantifiers binding more tightly than the binary connectives. Under this convention $\forall x P(x) \rightarrow Q(x)$ abbreviates $(\forall x P(x)) \rightarrow Q(x),$ which is a different formula from $\forall x (P(x) \rightarrow Q(x)).$ Explicit parentheses make the scope visible, since the two formulas differ in which occurrences of $x$ the quantifier governs.

## Free and bound variables

An occurrence of a variable $x$ in a formula is bound when it lies within the scope of a quantifier on $x,$ and free otherwise. The set $\mathrm{FV}(\varphi)$ of variables with a free occurrence in $\varphi$ is defined by induction on the construction of $\varphi.$ For a term $t,$ let $\mathrm{Var}(t)$ be the set of variables occurring in $t.$

$$
\begin{array}{ll}
\mathrm{FV}(P(t_1, \dots, t_n)) = \mathrm{Var}(t_1) \cup \cdots \cup \mathrm{Var}(t_n) \\[6pt]
\mathrm{FV}(t_1 = t_2) = \mathrm{Var}(t_1) \cup \mathrm{Var}(t_2) \\[6pt]
\mathrm{FV}(\neg\varphi) = \mathrm{FV}(\varphi) \\[6pt]
\mathrm{FV}(\varphi \star \psi) = \mathrm{FV}(\varphi) \cup \mathrm{FV}(\psi) \qquad \text{for } \star \in \{\ \wedge, \lor, \rightarrow, \leftrightarrow\ \} \\[6pt]
\mathrm{FV}(\forall x\varphi) = \mathrm{FV}(\exists x\varphi) = \mathrm{FV}(\varphi) \setminus \{x\}
\end{array}
$$

Only the last clause removes a variable from the set of free variables. A quantifier on $x$ binds the free occurrences of $x$ in its scope and leaves every other variable untouched.

The same variable can occur both free and bound in one formula. In

$$
L(x, y) \wedge \exists y\ L(y, x)
$$

the two occurrences of $x$ are free. The occurrence of $y$ in the left conjunct is free, while the occurrence of $y$ in $L(y, x)$ is bound by $\exists y.$ The free variables of the displayed formula are therefore $\{x, y\}.$ Renaming the bound variable to $z$ gives $L(x, y) \wedge \exists z\ L(z, x),$ which says the same thing without using $y$ in both roles.

A formula with $\mathrm{FV}(\varphi) = \varnothing$ is closed, or a sentence. A sentence makes an assertion without requiring values for variables. A formula with free variables requires assigned values for those variables. For example, under the usual interpretation of $>$ and $3,$ the formula $x > 3$ is neither true nor false until $x$ is fixed.

## Substitution

Write $\varphi[t/x]$ for the result of replacing every free occurrence of $x$ in $\varphi$ by the term $t.$ Bound occurrences are left unchanged because the substitution applies only to free occurrences.

The replacement is admissible only when it does not cause a variable of $t$ to become bound. Take a signature with one binary predicate $L,$ read as strict order. Consider the formula:

$$
\varphi := \exists y\ L(x, y)
$$

Over the integers with $L$ read as $<,$ the formula $\varphi$ holds for every value of $x,$ since every integer has a larger one. Substituting the term $y$ for $x$ produces $\exists y\ L(y, y),$ which asserts that some integer is smaller than itself and is false. This substitution causes variable capture. The quantifier binds the occurrence of $y$ introduced by the substitution, so the resulting formula has a different meaning.

A term $t$ is substitutable for $x$ in $\varphi$ when no free occurrence of $x$ in $\varphi$ lies within the scope of a quantifier binding a variable of $t.$ Renaming the bound variables of $\varphi$ to fresh variables can restore substitutability without changing the meaning of the formula. In the example above, rewriting $\varphi$ as $\exists z\ L(x, z)$ makes $y$ substitutable and yields $\exists z\ L(y, z),$ which says of $y$ what $\varphi$ said of $x.$ This side condition applies whenever a quantifier rule substitutes a term for a variable.

## Structures

Propositional semantics requires an assignment of truth values to the atoms. First-order semantics also requires a domain and interpretations of the non-logical symbols. A structure for the signature $\Sigma,$ also called an interpretation, consists of the following data:

+ A non-empty set $M,$ the domain or universe of discourse
+ An element $c^{\mathcal{M}} \in M$ for each constant symbol $c$ of $\Sigma$
+ A function $f^{\mathcal{M}} : M^n \rightarrow M$ for each $n$-ary function symbol $f$ of $\Sigma$
+ A relation $P^{\mathcal{M}} \subseteq M^n$ for each $n$-ary predicate symbol $P$ of $\Sigma$

We write $\mathcal{M}$ for this structure. Its domain determines the range of the variables, and the interpretations $c \mapsto c^{\mathcal{M}},$ $f \mapsto f^{\mathcal{M}},$ $P \mapsto P^{\mathcal{M}}$ determine the meanings of the non-logical symbols. We require $M \neq \varnothing$ throughout.

As a running example, take $\Sigma$ with constant symbols $a$ and $b,$ binary function symbols $g$ and $l,$ and one binary predicate symbol $D.$ Define the domain and the interpretations of the constants by:

$$
M = \{\ 1, 2, 3, 6\ \} \qquad a^{\mathcal{M}} = 1 \qquad b^{\mathcal{M}} = 6
$$

Interpret $g^{\mathcal{M}}$ as the greatest common divisor and $l^{\mathcal{M}}$ as the least common multiple. The predicate $D$ is interpreted by:

$$
D^{\mathcal{M}} = \{\ (m, n) \in M^2 \mid m \ \text{divides} \ n\ \}
$$

The domain is the set of divisors of $6,$ which is closed under both $\gcd$ and $\mathrm{lcm},$ so $g^{\mathcal{M}}$ and $l^{\mathcal{M}}$ are total functions on $M$ as required.

## Assignments and satisfaction

To evaluate terms containing variables, we also need values for those variables. A variable assignment is a function $s$ from the variables to the domain, $s : \mathrm{Var} \rightarrow M.$ Write $s[x \mapsto d]$ for the assignment that agrees with $s$ everywhere except at $x,$ where it takes the value $d.$ Each term $t$ then denotes an element $t^{\mathcal{M}}[s]$ of $M,$ computed by recursion on $t$:

$$
x^{\mathcal{M}}[s] = s(x) \qquad c^{\mathcal{M}}[s] = c^{\mathcal{M}} \qquad (f(t_1, \dots, t_n))^{\mathcal{M}}[s] = f^{\mathcal{M}}(t_1^{\mathcal{M}}[s], \dots, t_n^{\mathcal{M}}[s])
$$

In the structure above, with $s(x) = 2$ and $s(y) = 3,$ the term $l(x, g(y, b))$ evaluates in two steps. The inner term gives $g^{\mathcal{M}}(3, 6) = 3,$ and the outer term gives $l^{\mathcal{M}}(2, 3) = 6.$

The notation $\mathcal{M} \models \varphi[s]$ means that $\varphi$ is true in $\mathcal{M}$ under $s.$ Satisfaction is defined by recursion on the construction of $\varphi.$

$$
\begin{array}{ll}
\mathcal{M} \models P(t_1, \dots, t_n)[s] & \text{iff} \quad (t_1^{\mathcal{M}}[s], \dots, t_n^{\mathcal{M}}[s]) \in P^{\mathcal{M}} \\[6pt]
\mathcal{M} \models (t_1 = t_2)[s] & \text{iff} \quad t_1^{\mathcal{M}}[s] = t_2^{\mathcal{M}}[s] \\[6pt]
\mathcal{M} \models \neg\varphi[s] & \text{iff} \quad \mathcal{M} \not\models \varphi[s] \\[6pt]
\mathcal{M} \models (\varphi \wedge \psi)[s] & \text{iff} \quad \mathcal{M} \models \varphi[s] \ \text{and} \ \mathcal{M} \models \psi[s] \\[6pt]
\mathcal{M} \models (\varphi \lor \psi)[s] & \text{iff} \quad \mathcal{M} \models \varphi[s] \ \text{or} \ \mathcal{M} \models \psi[s] \\[6pt]
\mathcal{M} \models (\varphi \rightarrow \psi)[s] & \text{iff} \quad \mathcal{M} \not\models \varphi[s] \ \text{or} \ \mathcal{M} \models \psi[s] \\[6pt]
\mathcal{M} \models (\varphi \leftrightarrow \psi)[s] & \text{iff} \quad (\mathcal{M} \models \varphi[s] \ \text{and} \ \mathcal{M} \models \psi[s]) \ \text{or} \ (\mathcal{M} \not\models \varphi[s] \ \text{and} \ \mathcal{M} \not\models \psi[s]) \\[6pt]
\mathcal{M} \models \forall x\varphi[s] & \text{iff} \quad \mathcal{M} \models \varphi[s[x \mapsto d]] \ \text{for every} \ d \in M \\[6pt]
\mathcal{M} \models \exists x\varphi[s] & \text{iff} \quad \mathcal{M} \models \varphi[s[x \mapsto d]] \ \text{for some} \ d \in M
\end{array}
$$

The clauses for the connectives reproduce the propositional truth tables. The quantifier clauses range over the domain. Because the domain may be infinite, first-order formulas cannot in general be evaluated by a finite truth table.

Satisfaction depends on the assignment only through the free variables. If $s$ and $s'$ agree on $\mathrm{FV}(\varphi),$ then $\mathcal{M} \models \varphi[s]$ if and only if $\mathcal{M} \models \varphi[s'].$ The proof is an induction on $\varphi.$ The atomic case holds because $t^{\mathcal{M}}[s]$ depends only on the values of $s$ at $\mathrm{Var}(t),$ and the connective cases are immediate from the induction hypothesis. For $\forall x\varphi,$ the assignments $s[x \mapsto d]$ and $s'[x \mapsto d]$ agree on $\mathrm{FV}(\varphi) \subseteq \mathrm{FV}(\forall x\varphi) \cup \{x\}$ for each $d,$ so the induction hypothesis applies to each of them.

A sentence has no free variables, so the assignment plays no part and we write $\mathcal{M} \models \varphi.$ The domain and the interpretations of the non-logical symbols determine the truth value of a sentence.

## Models, validity and logical consequence

The semantic notions from propositional logic extend to structures as follows.

+ A structure $\mathcal{M}$ is a model of a sentence $\varphi$ when $\mathcal{M} \models \varphi.$
+ A sentence is satisfiable when it has a model, and unsatisfiable otherwise.
+ A sentence is valid, written $\models \varphi,$ when every structure for its signature is a model of it.
+ Formulas $\varphi$ and $\psi$ are logically equivalent, written $\varphi \equiv \psi,$ when they have the same truth value in every structure under every variable assignment.
+ A sentence $\varphi$ is a logical consequence of a set $S$ of sentences, written $S \models \varphi,$ when every structure that satisfies every member of $S$ also satisfies $\varphi.$

For formulas with free variables, $\varphi \models \psi$ means that every structure and variable assignment satisfying $\varphi$ also satisfies $\psi.$

The same [refutation equivalence](../automated-deduction-in-propositional-logic/) holds in first-order logic. For a set $S$ of sentences and a sentence $\varphi,$ $S \models \varphi$ if and only if $S \cup \{\neg\varphi\}$ is unsatisfiable. The proof is the same as in the propositional case and does not depend on the internal structure of the interpretations.

For a propositional formula with $n$ atoms, validity ranges over $2^n$ interpretations and can be settled by a finite table. First-order validity ranges over all structures for the signature, whose domains may have [arbitrary cardinality](../cardinality-and-countable-sets/). No finite truth table can enumerate all these structures, so the [methods of automated deduction](../automated-deduction-in-first-order-logic/) search for a refutation instead.

A sentence has a truth value relative to a structure. The sentence $\exists x \forall y\ D(y, x)$ is true in the divisor structure above, where $6$ is divisible by every element of the domain. In the structure of the positive integers with the same divisibility relation, the sentence is false, since no positive integer is a multiple of all positive integers. The same sentence is true in one structure and false in the other, so it is contingent rather than valid.

The following sentences of the same signature are all true in the divisor structure:

+ $\forall x\ D(a, x),$ since $1$ divides every element.
+ $\forall x \forall y\ ((D(x, y) \wedge D(y, x)) \rightarrow x = y),$ the antisymmetry of divisibility.
+ $\forall x \forall y\ D(g(x, y), x),$ since a greatest common divisor divides its arguments.

The sentence $\forall x \exists y\ (D(x, y) \wedge \neg(x = y))$ is false in $\mathcal{M}.$ For $x = 6,$ no witness for $y$ exists because $6$ is the largest element of the domain under divisibility. Over the positive integers the same sentence is true, with $y = 2x$ as a witness.

## Quantifier laws

The satisfaction clauses give the equivalences that govern the quantifiers. The two duality laws are the following:

$$
\neg \forall x\varphi \equiv \exists x \neg\varphi \qquad \neg \exists x\varphi \equiv \forall x \neg\varphi
$$

For the first, fix $\mathcal{M}$ and $s.$ Then $\mathcal{M} \models \neg\forall x\varphi[s]$ holds if and only if $\mathcal{M} \models \varphi[s[x \mapsto d]]$ fails for at least one $d \in M,$ that is, if and only if $\mathcal{M} \models \neg\varphi[s[x \mapsto d]]$ holds for at least one $d \in M.$ The last statement is the satisfaction clause for $\exists x\neg\varphi.$ The second law follows by the same argument, or by applying the first to $\neg\varphi.$

Either quantifier is therefore definable from the other together with negation, and a language may take one of them as primitive. Keeping both makes formulas shorter and their reading more direct.

The following two distributive equivalences hold:

$$
\forall x (\varphi \wedge \psi) \equiv \forall x \varphi \wedge \forall x \psi \qquad \exists x (\varphi \lor \psi) \equiv \exists x \varphi \lor \exists x \psi
$$

The universal quantifier does not distribute over disjunction. Over the integers, with $\varphi$ reading "$x$ is even" and $\psi$ reading "$x$ is odd", the sentence $\forall x (\varphi \lor \psi)$ is true while $\forall x \varphi \lor \forall x \psi$ is false. Dually, the same pair of formulas makes $\exists x \varphi \wedge \exists x \psi$ true and $\exists x(\varphi \wedge \psi)$ false, since no integer is both even and odd. One direction remains valid in each case, from $\forall x \varphi \lor \forall x \psi$ to $\forall x (\varphi \lor \psi)$ and from $\exists x (\varphi \wedge \psi)$ to $\exists x \varphi \wedge \exists x \psi.$

A quantifier can be moved across a subformula that does not contain its variable. If $x \notin \mathrm{FV}(\psi),$ then

$$
\forall x (\varphi \lor \psi) \equiv \forall x \varphi \lor \psi \qquad \exists x (\varphi \wedge \psi) \equiv \exists x \varphi \wedge \psi
$$

After the bound variables have been renamed apart, repeated application of these laws and propositional equivalences yields a formula in prenex form, with every quantifier at the front.

- - -

Adjacent quantifiers of the same kind commute, so $\forall x \forall y \varphi \equiv \forall y \forall x \varphi$ and likewise for $\exists.$ Quantifiers of different kinds do not commute in general. For distinct variables $x$ and $y,$ the following implication is valid:

$$
\exists y \forall x\ \varphi \models \forall x \exists y\ \varphi
$$

Fix a structure $\mathcal{M}$ and an assignment $s,$ and suppose $\mathcal{M} \models \exists y \forall x\ \varphi[s].$ Some $e \in M$ satisfies $\forall x \varphi$ under $s[y \mapsto e],$ so for each $d \in M$ the assignment $s[y \mapsto e][x \mapsto d]$ satisfies $\varphi.$ Since $x$ and $y$ are distinct, this assignment is also $s[x \mapsto d][y \mapsto e].$ The element $e$ is therefore a witness for the inner existential quantifier for every $d,$ so $\mathcal{M} \models \forall x \exists y\ \varphi[s].$ The single $e$ works for every $d,$ which is a stronger condition than the conclusion requires.

The converse fails. Over the integers with $\varphi$ reading $x + y = 0,$ the sentence $\forall x \exists y\ (x + y = 0)$ is true, since $y = -x$ is a witness for each $x.$ The sentence $\exists y \forall x\ (x + y = 0)$ is false, since a single $y$ would have to be the additive inverse of every integer at once. The order of the quantifiers records whether the witness may depend on the universally quantified object, and swapping them changes the assertion.

## Symbolizing quantified statements

The basic universal pattern has a conditional as its matrix, while the basic existential pattern has a conjunction:

$$
\text{every } F \text{ is } G : \quad \forall x\ (F(x) \rightarrow G(x)) \qquad \text{some } F \text{ is } G : \quad \exists x\ (F(x) \wedge G(x))
$$

Exchanging the connectives gives the wrong content in both cases. The formula $\forall x (F(x) \wedge G(x))$ says that every object in the domain is both $F$ and $G,$ which is a claim about the whole domain rather than about the objects satisfying $F.$ The formula $\exists x (F(x) \rightarrow G(x))$ is satisfied by any object that is not $F,$ because a conditional with a false antecedent is true. It may therefore be true even when no object is both $F$ and $G.$

> A universally quantified conditional is true when no object satisfies its antecedent. The sentence $\forall x (F(x) \rightarrow G(x))$ holds in any structure with $F^{\mathcal{M}} = \varnothing,$ regardless of $G.$ Ordinary language may suggest that some objects satisfying $F$ exist, but the formula does not assert their existence. Adding $\exists x F(x)$ as a separate conjunct states it explicitly.

- - -

The divisor signature gives further examples. Read $D(x, y)$ as "$x$ divides $y$" over the positive integers, and add a unary predicate $P$ for primality:

+ "Every number is divisible by $1$" becomes $\forall x\ D(a, x).$
+ "A prime has no divisors except $1$ and itself" becomes $\forall x \forall y\ ((P(x) \wedge D(y, x)) \rightarrow (y = a \lor y = x)).$
+ "Some number has a prime divisor other than itself" becomes $\exists x \exists y\ (P(y) \wedge D(y, x) \wedge \neg(y = x)).$
+ "Every number is a multiple of some prime" becomes $\forall x \exists y\ (P(y) \wedge D(y, x)),$ which is false over the positive integers because $1$ has no prime divisor.

The statement that [the primes are unbounded](../integers/) cannot be expressed directly in terms of size with this signature because it has no order symbol. Over the positive integers, the sentence $\forall x \exists y\ (P(y) \wedge \neg D(y, x))$ is an equivalent divisibility formulation, since it states that every number has a prime that does not divide it. Adding a binary predicate $L$ for strict order expresses unboundedness directly as $\forall x \exists y\ (P(y) \wedge L(x, y)).$ The signature determines which formulations are available, while a structure determines their truth.

## First-order and second-order logic

Adding symbols to the signature does not change what the quantifiers range over. In a first-order language, quantifiers bind variables that range over the domain, not variables ranging over [subsets of the domain](../sets/), relations, or functions. A second-order language has such variables. Under standard semantics, the formula $\exists X\ (X(a) \wedge \neg X(b))$ quantifies over subsets $X$ of $M.$

The [induction principle for the natural numbers](../principle-of-mathematical-induction/) illustrates this distinction. Its second-order statement quantifies over all subsets of $\mathbb{N}$:

$$
\forall X\ ((X(0) \wedge \forall n\ (X(n) \rightarrow X(n+1))) \rightarrow \forall n\ X(n))
$$

First-order arithmetic cannot quantify over $X.$ Its induction principle is therefore an axiom schema with one instance for each formula $\varphi(n, \overline{y})$ of the language. Universal closure over the parameters $\overline{y}$ is understood in the following formula:

$$
(\varphi(0, \overline{y}) \wedge \forall n\ (\varphi(n, \overline{y}) \rightarrow \varphi(n+1, \overline{y}))) \rightarrow \forall n\ \varphi(n, \overline{y})
$$

The schema has countably many instances, one for each formula, whereas the second-order axiom covers all subsets of $\mathbb{N},$ of which there are uncountably many. Together with the remaining [axioms for the natural numbers](../natural-numbers/), the second-order formulation determines $\mathbb{N}$ [up to isomorphism](../homomorphisms-and-isomorphisms/), while the first-order theory has nonstandard models.

First-order logic has a sound and complete proof system and satisfies compactness. In a countable language, any set of sentences with an infinite model has a countably infinite model and models of every infinite cardinality. Second-order logic under standard semantics has no complete recursively axiomatizable proof system. The deduction procedures for first-order logic rely on completeness and apply to first-order formulas.
