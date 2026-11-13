---
title: Intervals
source: https://algebrica.org/intervals/
license: CC BY-NC 4.0
tags:
  - bounded-interval
  - closed-interval
  - connectedness
  - convexity
  - half-open-interval
  - interval
  - length
  - neighborhood
  - open-interval
  - real-line
  - unbounded-interval
---

## Definizione

Un intervallo è un sottoinsieme della retta reale che, con due qualunque dei suoi punti, contiene anche tutti i punti compresi fra essi. Più precisamente, un sottoinsieme $I \subseteq \mathbb{R}$ è un intervallo se e solo se, per ogni coppia di punti $a, b \in I$ con $a < b,$ tutto l'insieme $\{x \in \mathbb{R} : a \leq x \leq b\}$ è contenuto in $I.$ Questa proprietà, detta convessità sulla retta reale, distingue gli intervalli da sottoinsiemi arbitrari di $\mathbb{R},$ quali gli insiemi finiti e le unioni di parti disgiunte separate da un vuoto.

Gli intervalli ricorrono in analisi matematica come domini di funzioni, come regioni di integrazione nella teoria degli [integrali definiti](../definite-integrals/) e come insiemi su cui studiare la continuità e la derivabilità. Servono inoltre a descrivere sottoinsiemi più complessi della [retta reale](../real-numbers/).

Gli intervalli si classificano in base all'inclusione o all'esclusione degli estremi e al fatto che siano limitati oppure si estendano indefinitamente in una o in entrambe le direzioni.

## Intervalli limitati

Un intervallo è limitato se è contenuto in una porzione finita della retta reale, ossia se esistono due numeri reali $a$ e $b$ con $a \leq b$ tali che l'intervallo sia contenuto in $[a,b].$ L'intervallo aperto di estremi $a$ e $b$ è l'insieme dei numeri reali strettamente compresi tra $a$ e $b.$ La definizione è la seguente.

$$
(a, b) = \{x \in \mathbb{R} : a < x < b\}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-o | sign+r-in-o |     |
[/shortcode]

L'intervallo chiuso di estremi $a$ e $b$ è l'insieme dei numeri reali compresi tra $a$ e $b,$ estremi inclusi. La definizione è la seguente.

$$
[a, b] = \{x \in \mathbb{R} : a \leq x \leq b\}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-c | sign+r-in-c |     |
[/shortcode]

Ciascuno dei due intervalli semiaperti di estremi $a$ e $b$ include un estremo ed esclude l'altro. Le definizioni sono le seguenti.

$$
[a, b) = \{x \in \mathbb{R} : a \leq x < b\}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-c | sign+r-in-o |     |
[/shortcode]

$$
(a, b] = \{x \in \mathbb{R} : a < x \leq b\}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-o | sign+r-in-c |     |
[/shortcode]

L'intervallo degenere $[a,a]=\{a\}$ contiene un solo punto. Soddisfa la definizione di intervallo perché non contiene due punti distinti tra i quali occorra includerne altri.

## Intervalli illimitati

Un intervallo illimitato si estende indefinitamente in almeno una direzione. I simboli $+\infty$ e $-\infty$ indicano per convenzione che l'intervallo non ha un estremo finito nella direzione corrispondente. Poiché tali simboli non rappresentano numeri reali, sono sempre accompagnati da una parentesi tonda. Si ottengono così i quattro tipi di intervalli illimitati in una sola direzione.

$$
[a, +\infty) = \{x \in \mathbb{R} : x \geq a\}
$$

[shortcode="intervals"]
|     | $a$ |     |
|:----|-----|-----|
|     | sign+l-c |     |
[/shortcode]

$$
(a, +\infty) = \{x \in \mathbb{R} : x > a\}
$$

[shortcode="intervals"]
|     | $a$ |     |
|:----|-----|-----|
|     | sign+l-o |     |
[/shortcode]

$$
(-\infty, b] = \{x \in \mathbb{R} : x \leq b\}
$$

[shortcode="intervals"]
|     | $b$ |     |
|:----|-----|-----|
|     | sign+r-c |     |
[/shortcode]

$$
(-\infty, b) = \{x \in \mathbb{R} : x < b\}
$$

[shortcode="intervals"]
|     | $b$ |     |
|:----|-----|-----|
|     | sign+r-o |     |
[/shortcode]

Anche l'intera retta reale è un intervallo. Si scrive $(-\infty,+\infty)=\mathbb{R}$ e comprende tutti i numeri reali.

## Operazioni sugli intervalli

Da due intervalli si possono ottenere nuovi insiemi mediante le operazioni di intersezione e unione definite nella voce sugli [insiemi](../sets/). L'intersezione $I \cap J$ è l'insieme dei punti che appartengono a entrambi gli intervalli. L'intersezione di due intervalli è sempre un intervallo, eventualmente vuoto o degenere. Se $I=(1,5)$ e $J=(3,7),$ i punti comuni sono esattamente quelli di $(3,5).$

[shortcode="intervals"]
|     | $1$ | $3$ | $5$ | $7$ |     |
|:----|-----|-----|-----|-----|-----|
|     | sign+l-in-o |             | sign+r-in-o |             |     |
|     |             | sign+l-in-o |             | sign+r-in-o |     |
|     |             | sign+l-in-o-h | sign+r-in-o-h |           |     |
[/shortcode]

La terza riga mostra l'intersezione $(3,5),$ la parte comune ai due intervalli.

- - -

L'unione $I \cup J$ è l'insieme dei punti che appartengono ad almeno uno dei due intervalli. L'unione di due intervalli non vuoti è un intervallo se i due intervalli si intersecano oppure se si toccano in un estremo che appartiene ad almeno uno dei due. Nell'esempio precedente, $I=(1,5)$ e $J=(3,7)$ si intersecano, perciò la loro unione è $(1,7).$

[shortcode="intervals"]
|     | $1$ | $3$ | $5$ | $7$ |     |
|:----|-----|-----|-----|-----|-----|
|     | sign+l-in-o |             | sign+r-in-o |             |     |
|     |             | sign+l-in-o |             | sign+r-in-o |     |
|     | sign+l-in-o-h | sign+s-h |             | sign+r-in-o-h |     |
[/shortcode]

La terza riga mostra l'unione $(1,7).$ L'unione $(1,3)\cup(5,7)$ non è invece un intervallo, perché i punti fra $3$ e $5$ non appartengono a nessuno dei due insiemi.

## Intervalli e intorni

A ogni punto $x_0 \in \mathbb{R}$ e a ogni numero reale $\varepsilon>0$ si associa il seguente intervallo aperto.

$$
(x_0 - \varepsilon, \ x_0 + \varepsilon)
$$

Questo intervallo è detto $\varepsilon$-intorno di $x_0,$ o semplicemente intorno di $x_0.$ Comprende tutti i punti la cui distanza da $x_0$ è strettamente minore di $\varepsilon,$ ossia tutti gli $x$ tali che $|x-x_0|<\varepsilon,$ dove $|\cdot|$ indica il [valore assoluto](../absolute-value/).

[shortcode="intervals"]
|     | $x_0 - \varepsilon$ | $x_0$ | $x_0 + \varepsilon$ |     |
|:----|---------------------|-------|---------------------|-----|
|     | sign+l-in-o-h | sign+s-h | sign+r-in-o-h |     |
[/shortcode]

Gli intorni permettono di formulare le definizioni di [limite](../limits/), continuità e derivabilità. Il loro legame con i punti interni, gli insiemi aperti e chiusi e la compattezza è sviluppato nella voce sulla [topologia della retta reale](../topology-of-the-real-line/). Una funzione $f$ è continua in $x_0$ se, per ogni intorno di $f(x_0),$ esiste un intorno di $x_0$ la cui immagine mediante $f$ è contenuta nel primo. Questa formulazione equivale alla definizione classica con $\varepsilon$ e $\delta$ ed esplicita il ruolo degli intervalli.

Un punto $x_0$ è interno a un insieme $S\subseteq\mathbb{R}$ se un suo intorno è interamente contenuto in $S.$ Ogni punto di un intervallo aperto è interno all'intervallo. Gli estremi di un intervallo chiuso non sono punti interni, perché ogni loro intorno contiene punti esterni all'intervallo.

## Lunghezza di un intervallo

La lunghezza di un intervallo limitato di estremi $a$ e $b$ è $b-a,$ indipendentemente dall'inclusione degli estremi. I quattro intervalli $(a,b),$ $[a,b),$ $(a,b]$ e $[a,b]$ hanno quindi la stessa lunghezza.

$$
\ell(I) = b - a
$$

Un singolo punto ha lunghezza nulla, perciò aggiungere o togliere un numero finito di punti da un intervallo non ne altera la misura. L'intervallo degenere $[a,a]$ ha lunghezza $\ell([a,a])=0.$ Gli intervalli illimitati hanno lunghezza infinita. Per ogni $M>0$ contengono infatti due punti a distanza maggiore di $M,$ quindi nessun valore finito può rappresentarne la lunghezza.

Lunghezza e cardinalità esprimono due nozioni diverse di grandezza. Ogni intervallo non degenere ha la stessa cardinalità di $\mathbb{R},$ indipendentemente dalla sua lunghezza e dall'inclusione degli estremi. Il risultato è dimostrato nella voce su [cardinalità e insiemi numerabili](../cardinality-and-countable-sets/).

La nozione di lunghezza è alla base della teoria della misura sulla retta reale, che estende questa nozione di grandezza a sottoinsiemi di $\mathbb{R}.$ La misura di $[a,b]$ coincide con la sua lunghezza $b-a.$ L'estensione della misura a insiemi più complessi, mediante le nozioni di misura esterna e misurabilità, è alla base dell'[integrale di Lebesgue](../riemann-integrability-criteria/).

## Caratterizzazione degli intervalli

Un sottoinsieme della retta reale è connesso se non si può esprimere come unione di due insiemi disgiunti, non vuoti e aperti nella sua topologia relativa. Un sottoinsieme $S\subseteq\mathbb{R}$ è un intervallo se e solo se è connesso.

Il risultato precisa l'idea che un intervallo sia una porzione di retta priva di lacune. Un insieme come $(1,2)\cup(3,4)$ non è connesso perché si può separare in due parti aperte e disgiunte.

[shortcode="intervals"]
|     | $1$ | $2$ | $3$ | $4$ |     |
|:----|-----|-----|-----|-----|-----|
|     | sign+l-in-o-h | sign+r-in-o-h |  |  |     |
|     |  |  | sign+l-in-o-h | sign+r-in-o-h |     |
[/shortcode]

> I due intervalli occupano porzioni separate della retta reale. La loro unione non è connessa e quindi non è un intervallo.
