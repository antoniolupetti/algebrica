---
title: Supremum and Infimum
source: https://algebrica.org/supremum-and-infimum/
license: CC BY-NC 4.0
tags:
  - approximation-property
  - bounded-set
  - completeness-axiom
  - infimum
  - lower-bound
  - maximum
  - minimum
  - supremum
  - upper-bound
---

## Maggioranti e minoranti

Prima di introdurre i concetti di estremo superiore e inferiore, occorre definire i cosiddetti maggioranti e minoranti di un insieme, ovvero i valori che lo limitano dall'alto e dal basso. Come vedremo nel dettaglio più avanti, l'estremo superiore è il minimo dei maggioranti, mentre l'estremo inferiore è il massimo dei minoranti. Nella spiegazione considereremo solo sottoinsiemi dell'insieme dei numeri reali $\mathbb{R},$ che soddisfa l'assioma di completezza, secondo il quale ogni sottoinsieme non vuoto di $\mathbb{R}$ limitato superiormente e inferiormente ammette, rispettivamente, un estremo superiore e un estremo inferiore in $\mathbb{R}.$ Iniziamo col considerare dunque un insieme non vuoto $A \subseteq \mathbb{R}.$ Si dice che un numero reale $M$ è un maggiorante di $A$ se vale la seguente condizione:

$$
a \leq M \quad \forall \ a \in A \tag{1}
$$

Se esiste un tale numero, l'insieme $A$ è limitato superiormente. In modo simile, un numero reale $m$ è un minorante di $A$ se vale la seguente condizione:

$$
a \geq m \quad \forall \ a \in A \tag{2}
$$

In questo caso, $A$ è limitato inferiormente. Un insieme è limitato se è limitato sia superiormente sia inferiormente, ossia se esiste una costante reale $K > 0$ tale che:

$$
|a| \leq K \quad \forall \ a \in A \tag{3}
$$

I maggioranti, quando esistono, non sono in generale unici, infatti se $M$ è un maggiorante di $A,$ anche $M + 1$ e $M + 100$ sono suoi maggioranti. Un ragionamento analogo vale anche per i minoranti. Se $m$ è un minorante di $A,$ anche $m - 1$ è un minorante. Quindi, come abbiamo anticipato all'inizio, il minimo dei maggioranti si chiama estremo superiore, mentre il massimo dei minoranti si chiama estremo inferiore.


![Fig. 1](../svg/supremum-and-infimum-1.svg)


Queste definizioni si estendono agli insiemi non limitati e all'insieme vuoto ammettendo i valori $+\infty$ e $-\infty,$ secondo le seguenti convenzioni:

+ Se $A$ è non vuoto e non è limitato superiormente, si pone per convenzione $\sup A = +\infty.$
+ Se $A$ non è limitato inferiormente, si pone $\inf A = -\infty.$
+ Per l'insieme vuoto si adottano le convenzioni $\sup \emptyset = -\infty$ e $\inf \emptyset = +\infty.$

## Estremo superiore e inferiore

Consideriamo ora un sottoinsieme non vuoto $A \subseteq \mathbb{R}$ limitato superiormente. L'estremo superiore di $A,$ indicato con $\sup A,$ è il minimo dei suoi maggioranti. Un numero reale $s$ è uguale a $\sup A$ se e solo se soddisfa due condizioni. La prima è speculare alla $(1),$ ovvero:

$$
a \leq s \quad \forall \ a \in A
$$

La seconda condizione che assicura che ogni numero strettamente minore di $s$ sia superato da almeno un elemento di $A$:

$$
\forall \ \varepsilon > 0 \quad \exists \ a \in A : a > s - \varepsilon \tag{4}
$$

Queste condizioni determinano $s$ in modo univoco, ovvero se sia $s$ sia $s'$ soddisfano la definizione, si ha necessariamente che $s$ e $s'$ sono uguali, ovvero vale la seguente relazione:

$$
s \leq s' \ \wedge \ s' \leq s \ \to \ s = s' \tag{5}
$$

Una caratterizzazione equivalente afferma che $s = \sup A$ se e solo se $s$ è un maggiorante di $A$ ed esiste una successione $(a_n) \subseteq A$ tale che $a_n \to s.$

- - -

Facciamo ora una distinzione tra $\mathbb{R}$ e $\mathbb{Q}.$ Abbiamo anticipato che l'assioma di completezza garantisce che ogni insieme non vuoto di numeri reali limitato superiormente abbia un estremo superiore reale e per questo abbiamo considerato sottoinsiemi dei numeri reali. Mentre questa proprietà vale per i reali, non vale per i numeri razionali. Consideriamo infatti il seguente insieme:
$$A = \{q \in \mathbb{Q} : q^2 < 2\} \tag{6}$$Questo insieme contiene $0$ ed è limitato superiormente, per esempio da $2.$ Se cerchiamo il suo estremo superiore in $\mathbb{R},$ otteniamo $\sqrt{2},$ che è un numero irrazionale. Se invece ammettiamo solo maggioranti razionali, non esiste un maggiorante di $A$ che sia minore o uguale a tutti gli altri maggioranti razionali. Infatti, ogni maggiorante razionale $M$ è maggiore di $\sqrt{2}$ e, per la densità dei razionali, esiste un numero razionale $r$ tale che $\sqrt{2} < r < M$ e quindi anche $r$ è un maggiorante di $A.$ Quindi, l'insieme indicato nella $(6)$ ha dunque un estremo superiore in $\mathbb{R},$ ma non in $\mathbb{Q}.$

- - -

Passiamo adesso alla definizione di estremo inferiore, considerando, come nel caso dell'estremo superiore, un sottoinsieme non vuoto $A \subseteq \mathbb{R}$ ma stavolta limitato inferiormente. L'estremo inferiore di $A,$ indicato con $\inf A,$ è il massimo dei suoi minoranti. Un numero reale $i$ è uguale a $\inf A$ se e solo se soddisfa le seguenti condizioni. La prima corrisponde alla $(2)$ e afferma che $i$ è un minorante di $A$:

$$
	a \geq i \quad \forall \ a \in A \tag{7}
$$

La seconda, invece, assicura che ogni numero strettamente maggiore di $i$ sia maggiore di almeno un elemento di $A$:

$$
\forall \ \varepsilon > 0 \quad \exists \ a \in A : a < i + \varepsilon \tag{8}
$$

Analogamente all'estremo superiore, queste condizioni determinano $i$ in modo univoco, perciò se sia $i$ sia $i'$ soddisfano la definizione, si ha:

$$
i \geq i' \ \wedge \ i' \geq i \ \to \ i = i' \tag{9}
$$

Anche in questo caso, tirando in ballo le successioni si può determinare una definizione equivalente per cui $i = \inf A$ se e solo se $i$ è un minorante di $A$ ed esiste una successione $(a_n) \subseteq A$ tale che $a_n \to i.$

Può succedere che un insieme può avere un estremo inferiore che non appartiene all'insieme e quindi non è un minimo. Consideriamo, per esempio, il seguente insieme:

$$\{1/n : n \in \mathbb{N},\ n \geq 1\} \tag{10}$$

Ogni termine della $(10)$ è positivo, quindi si conclude facilmente che $0$ è un minorante dell'insieme. Tuttavia, nessun numero positivo può essere un minorante, poiché la proprietà archimedea garantisce che, per ogni valore positivo, esiste un intero $n \geq 1$ per cui $1/n$ è minore di tale soglia. Pertanto l'insieme ha il seguente estremo inferiore:

$$
\inf \{1/n : n \in \mathbb{N},\ n \geq 1\} = 0 \tag{11}
$$

Tuttavia, poiché il valore $0$ non appartiene all'insieme, l'insieme non ha un minimo.

## La proprietà di approssimazione

Le condizioni $(4)$ e $(8)$ mostrano che possiamo trovare elementi di un insieme arbitrariamente vicini al suo estremo superiore o inferiore, purché l'estremo considerato sia finito. Questa conseguenza delle definizioni si chiama proprietà di approssimazione e vale anche quando l'estremo non appartiene all'insieme. Consideriamo un insieme $A \subseteq \mathbb{R}$ non vuoto. Se $s = \sup A \in \mathbb{R},$ allora per ogni $\varepsilon > 0$ esiste un elemento $a \in A$ tale che:

$$
s - \varepsilon < a \leq s \tag{12}
$$

Infatti, $s - \varepsilon$ non può essere un maggiorante di $A,$ perché è minore dell'estremo superiore e quindi esiste un elemento $a \in A$ maggiore di $s - \varepsilon.$ Inoltre, si ha anche che $a \leq s$ perché $s$ è un maggiorante. Analogamente, se $i = \inf A \in \mathbb{R},$ allora per ogni $\varepsilon > 0$ esiste un elemento $a \in A$ tale che:

$$
i \leq a < i + \varepsilon
$$

In questo caso, $i + \varepsilon$ non può essere un minorante di $A,$ perché è maggiore dell'estremo inferiore e quindi esiste un numero $a \in A$ tale che $a < i + \varepsilon.$ Inoltre, $a \geq i$ perché $i$ è un minorante.

La possibilità di trovare elementi di $A$ arbitrariamente vicini a $s$ permette di costruire una successione che converge a $s.$ Per dimostrarlo, applichiamo la proprietà di approssimazione con valori di $\varepsilon$ che tendono a zero. Scegliendo $\varepsilon = 1/n$ per ogni intero $n \geq 1,$ otteniamo un elemento $a_n \in A$ tale che:

$$
s - \frac{1}{n} < a_n \leq s
$$

La distanza tra $a_n$ e $s$ soddisfa quindi $0 \leq s - a_n < 1/n,$ ovvero la $(12),$ e poiché $1/n$ tende a zero, anche questa distanza tende a zero, e quindi $a_n \to s.$ Lo stesso procedimento si applica all'estremo inferiore $i.$ Per ogni intero $n \geq 1,$ scegliamo $b_n \in A$ tale che $i \leq b_n < i + 1/n.$ Dalla disuguaglianza $0 \leq b_n - i < 1/n$ segue che $b_n \to i.$

## Massimo e minimo

Il massimo di un insieme $A$ è un elemento di $A$ maggiore o uguale a ogni altro elemento dell'insieme. Quando il massimo esiste, coincide con l'estremo superiore di $A$:

$$
\max A = \sup A \tag{13}
$$

Affinché valga la $(13),$ l'estremo superiore deve appartenere ad $A$ ma, come abbiamo visto sopra, la definizione di estremo superiore non impone questa condizione. Per cui in genere vale che un insieme può avere un estremo superiore senza avere un massimo. Per rendere più chiaro il concetto, consideriamo, per esempio, l'intervallo aperto $A = (0,1).$ Il numero $1$ è un maggiorante e ogni numero minore di $1$ è superato da qualche elemento di $A,$ quindi $\sup A = 1.$ Tuttavia, $1 \notin A,$ perciò $A$ non ha massimo. Analogamente, $\inf A = 0,$ ma $0 \notin A,$ quindi $A$ non ha minimo. Invece, nell'intervallo chiuso $B = [0,1],$ entrambi gli estremi appartengono all'insieme e coincidono rispettivamente con il massimo e il minimo:

$$
\begin{align}
\sup B &= \max B = 1 \\[6pt]
\inf B &= \min B = 0
\end{align}
$$

Il ragionamento è schematizzato nella seguente immagine:

![Fig. 2](../svg/supremum-and-infimum-2.svg)

In generale, valgono le seguenti implicazioni:

+ Se l'insieme $A$ ha un massimo, questo coincide con il suo estremo superiore, quindi $\max A = \sup A.$
+ Se l'insieme $A$ ha un minimo, questo coincide con il suo estremo inferiore, quindi $\min A = \inf A.$

## Estremi di funzioni

Le nozioni di estremo superiore ed estremo inferiore si estendono anche alle funzioni. In genere, per una funzione $f : D \to \mathbb{R},$ l'estremo superiore di $f$ su $D$ è l'estremo superiore della sua immagine, ovvero vale:

$$
\sup_{x \in D} f(x) = \sup \{ f(x) : x \in D \} \tag{14}
$$

Analogamente, l'estremo inferiore è definito dalla seguente uguaglianza:

$$
\inf_{x \in D} f(x) = \inf \{ f(x) : x \in D \} \tag{15}
$$

Le definizioni $(14)$ e $(15)$ individuano gli estremi dell'immagine di $f,$ che possono non appartenere all'immagine stessa. In questo caso, la funzione non assume il valore dell'estremo in alcun punto del dominio. Le condizioni seguenti permettono di stabilire se un numero reale è l'estremo superiore o l'estremo inferiore di $f$ su $D$:

+ Un numero reale $s$ è uguale a $\sup_{x \in D} f(x)$ se e solo se $f(x) \leq s$ per ogni $x \in D$ e, per ogni $\varepsilon > 0,$ esiste $x \in D$ tale che $f(x) > s - \varepsilon.$
+ Simmetricamente, un numero reale $i$ è uguale a $\inf_{x \in D} f(x)$ se e solo se $f(x) \geq i$ per ogni $x \in D$ e, per ogni $\varepsilon > 0,$ esiste $x \in D$ tale che $f(x) < i + \varepsilon.$

Per esempio, la funzione $f(x) = x$ definita sull'intervallo aperto $(0, 1)$ soddisfa $\sup_{x \in (0,1)} f(x) = 1,$ ma nessun $x \in (0, 1)$ soddisfa $f(x) = 1$ perciò la funzione non ammette un massimo. Quando invece l'estremo superiore è raggiunto in un punto $x_0 \in D,$ ossia se $f(x_0) = \sup_{x \in D} f(x),$ esso coincide con il massimo di $f$ su $D.$ La stessa situazione vale tra estremo inferiore e minimo. Quindi possiamo concludere che l'estremo superiore e l'estremo inferiore sono valori a cui la funzione può avvicinarsi senza necessariamente raggiungerli, mentre il massimo e il minimo sono valori che la funzione deve assumere necessariamente in almeno un punto del proprio dominio.

Il teorema di Weierstrass fornisce una condizione sufficiente affinché una funzione raggiunga il proprio estremo superiore e il proprio estremo inferiore. In particolare, se $f : [a,b] \to \mathbb{R}$ è continua su un intervallo chiuso, limitato e non vuoto, allora $f$ è limitata e assume sia un massimo sia un minimo su $[a,b].$ Il suo estremo superiore e il suo estremo inferiore sono quindi finiti e coincidono rispettivamente con questi valori.

## Algebra degli estremi superiori e inferiori

Gli estremi superiori e inferiori seguono alcune semplici relazioni algebriche che ne semplificano spesso il calcolo. Consideriamo per prima una traslazione dell'insieme e consideriamo un insieme non vuoto e limitato $A \subseteq \mathbb{R}$ e un numero reale $c,$ poniamo $c + A = \{ c + a : a \in A \}$ e $cA = \{ ca : a \in A \}.$ Questa traslazione, come è facile immaginare, sposta entrambi gli estremi della stessa quantità e perciò otteniamo:

$$
\begin{align}
\sup(c + A) &= c + \sup A \\[6pt]
\inf(c + A) &= c + \inf A
\end{align}
$$

Analogamente, la moltiplicazione per un fattore positivo $c$ moltiplica entrambi gli estremi per lo stesso fattore e si ottiene:

$$
\begin{align}
\sup(cA) &= c \sup A \tag{16} \\[6pt]
\inf(cA) &= c \inf A \notag
\end{align}
$$

Quando $c$ è negativo l'ordine della $(16)$ è invertito:

$$
\begin{align}
\sup(cA) &= c \inf A \\[6pt]
\inf(cA) &= c \sup A
\end{align}
$$

Supponiamo adesso che due insiemi $A$ e $B$ siano non vuoti e che $a \leq b$ per ogni $a \in A$ e ogni $b \in B.$ Ogni $a$ è allora un minorante di $B,$ quindi $a \leq \inf B.$ Di conseguenza, $\inf B$ è un maggiorante di $A.$ Per definizione di estremo superiore di $A,$ si ottiene:

$$
\sup A \leq \inf B \tag{17}
$$

La $(17)$ rimane una disuguaglianza non stretta anche se si dovesse rafforzare l'ipotesi e cioè richiedendo $a < b$ per ogni coppia di elementi dei due insiemi. Ad esempio se consideriamo due insiemi $A = \{ 0 \}$ e $B = \{1/n : n \in \mathbb{N},\ n \geq 1\}$ si ha sempre $a < b,$ eppure $\sup A = \inf B = 0.$

