---
title: Leggi di De Morgan
source: https://algebrica.org/de-morgan-laws/
license: CC BY-NC 4.0
tags:
  - de-morgan-laws
  - set
  - set-operations
  - universal-set
---

## Definizione

Le leggi di De Morgan descrivono le relazioni tra unione, intersezione e complementare di insiemi. Consideriamo due sottoinsiemi $A$ e $B$ di uno stesso insieme universo $U$ e indichiamo con $A^c = U \setminus A$ il complementare di $A$ rispetto a $U.$ Le due leggi affermano che:

$$ \tag{1}
\begin{align}
(A \cup B)^c &= A^c \cap B^c \\[6pt]
(A \cap B)^c &= A^c \cup B^c
\end{align}
$$

La prima legge afferma che il complementare dell'unione di due insiemi è uguale all'intersezione dei loro complementari. Infatti, un elemento di $U$ non appartiene ad $A \cup B$ se e solo se non appartiene né ad $A$ né a $B,$ il che equivale ad appartenere sia ad $A^c$ sia a $B^c,$ e dunque alla loro intersezione.

![Complementare dell'unione di due insiemi](../svg/sets-6.svg)

La seconda legge afferma che il complementare dell'intersezione di due insiemi è uguale all'unione dei loro complementari. Infatti, un elemento di $U$ non appartiene ad $A \cap B$ se e solo se almeno uno dei due insiemi non lo contiene. L'elemento appartiene quindi ad almeno uno tra $A^c$ e $B^c,$ ossia alla loro unione.

![IMG. 2](../svg/sets-7.svg)

Queste leggi si estendono a una famiglia arbitraria di sottoinsiemi $(A_i)_{i\in I}$ di uno stesso insieme universo $U,$ senza alcuna restrizione sulla cardinalità dell'insieme degli indici $I.$ Tutti i complementari sono calcolati rispetto a $U$ e, analogamente alla $(1),$ valgono le seguenti identità:

$$ \tag{2}
\begin{align}
\left(\bigcup_{i \in I} A_i\right)^c &= \bigcap_{i \in I} A_i^c \\[6pt]
\left(\bigcap_{i \in I} A_i\right)^c &= \bigcup_{i \in I} A_i^c
\end{align}
$$

La prima uguaglianza afferma che un elemento di $U$ è esterno all'unione se e solo se non appartiene ad alcun $A_i,$ cioè se appartiene a tutti i complementari $A_i^c.$ La seconda uguaglianza afferma che un elemento di $U$ è esterno all'intersezione se e solo se almeno un $A_i$ non lo contiene, cioè se appartiene all'unione dei complementari.

> Quando $I = \emptyset,$ si adottano le convenzioni $\bigcup_{i\in\emptyset} A_i = \emptyset$ e $\bigcap_{i\in\emptyset} A_i = U.$ Con queste convenzioni, le identità della $(2)$ valgono anche per la famiglia vuota.

- - -

Il ragionamento appena fatto si basa sulla negazione delle condizioni di appartenenza e può essere anche espresso mediante i connettivi logici. Nel caso di due insiemi, ad esempio, fissiamo un elemento $x\in U$ e indichiamo con $P$ la proposizione $x\in A$ e con $Q$ la proposizione $x\in B.$ L'elemento $x$ appartiene all'unione $A\cup B$ se e solo se almeno una delle due proposizioni è vera, mentre appartiene all'intersezione $A\cap B$ se e solo se entrambe sono vere.

L'unione corrisponde quindi alla disgiunzione $\lor,$ l'intersezione alla congiunzione $\land$ e il complementare alla negazione $\neg.$ Le leggi di De Morgan esprimono questa relazione attraverso le seguenti equivalenze, valide per due proposizioni qualsiasi:

$$ \tag{3}
\begin{align}
\neg(P \lor Q) &\equiv \neg P \land \neg Q \\[6pt]
\neg(P \land Q) &\equiv \neg P \lor \neg Q
\end{align}
$$

La prima equivalenza della $(3)$ afferma che negare che almeno una delle due proposizioni sia vera equivale ad affermare che entrambe sono false. La seconda afferma che negare che entrambe siano vere equivale ad affermare che almeno una è falsa. Possiamo verificare queste equivalenze mediante le tavole di verità, considerando tutte le combinazioni dei valori di $P$ e $Q$ e indicando con $\mathrm{V}$ il valore vero e con $\mathrm{F}$ il valore falso. Per la prima equivalenza della $(3)$ otteniamo:

$$
\begin{array}{cc|cc}
P & Q & \neg(P\lor Q) & \neg P\land\neg Q \\[6pt]
\hline
\mathrm{V} & \mathrm{V} & \mathrm{F} & \mathrm{F} \\[6pt]
\mathrm{V} & \mathrm{F} & \mathrm{F} & \mathrm{F} \\[6pt]
\mathrm{F} & \mathrm{V} & \mathrm{F} & \mathrm{F} \\[6pt]
\mathrm{F} & \mathrm{F} & \mathrm{V} & \mathrm{V}
\end{array}
$$

Per la seconda equivalenza della $(3)$ la tavola è la seguente:

$$
\begin{array}{cc|cc}
P & Q & \neg(P\land Q) & \neg P\lor\neg Q \\[6pt]
\hline
\mathrm{V} & \mathrm{V} & \mathrm{F} & \mathrm{F} \\[6pt]
\mathrm{V} & \mathrm{F} & \mathrm{V} & \mathrm{V} \\[6pt]
\mathrm{F} & \mathrm{V} & \mathrm{V} & \mathrm{V} \\[6pt]
\mathrm{F} & \mathrm{F} & \mathrm{V} & \mathrm{V}
\end{array}
$$

In ciascuna tavola le ultime due colonne coincidono in ogni riga, verificando l'equivalenza dei due membri. Applicando queste equivalenze alle condizioni di appartenenza per ogni $x\in U,$ si ottengono le due identità tra insiemi. Ad esempio, ricaviamo la prima uguaglianza della $(1)$ fissando un elemento arbitrario $x\in U.$ Le definizioni di unione e complementare permettono di tradurre l'appartenenza a $(A\cup B)^c$ nella negazione di una disgiunzione. Applichiamo quindi la prima equivalenza logica della $(3)$ e otteniamo:

$$
\begin{align}
x\in(A\cup B)^c &\iff \neg\bigl((x\in A)\lor(x\in B)\bigr) \\[6pt]
&\iff (x\notin A)\land(x\notin B) \\[6pt]
&\iff (x\in A^c)\land(x\in B^c) \\[6pt]
&\iff x\in A^c\cap B^c
\end{align}
$$

Poiché queste equivalenze valgono per ogni $x\in U,$ i due insiemi hanno gli stessi elementi. Si conclude quindi che $(A\cup B)^c = A^c\cap B^c.$

## Esempio

Sia $U = \{1, 2, 3, 4, 5, 6, 7, 8, 9, 10\}$ l'insieme universo. Consideriamo i due sottoinsiemi:

$$ \tag{4}
\begin{align}
A &= \{1, 2, 3, 4, 6\} \\[6pt]
B &= \{2, 4, 6, 8, 10\}
\end{align}
$$

Dalle definizioni di unione e intersezione tra insiemi segue che:

$$
\begin{align}
A \cup B &= \{1, 2, 3, 4, 6, 8, 10\} \\[6pt]
A \cap B &= \{2, 4, 6\}
\end{align}
$$

Per calcolare i complementari rispetto a $U,$ selezioniamo gli elementi dell'insieme universo che non appartengono rispettivamente ad $A$ e a $B.$ Otteniamo:

$$
\begin{align}
A^c &= \{5, 7, 8, 9, 10\} \\[6pt]
B^c &= \{1, 3, 5, 7, 9\}
\end{align}
$$

Verifichiamo quindi la prima legge di De Morgan calcolando separatamente i due membri. Gli elementi di $U$ esclusi dall'unione sono $5,$ $7$ e $9,$ quindi:

$$
(A \cup B)^c = U \setminus (A \cup B) = \{5, 7, 9\}
$$

Gli stessi elementi sono comuni ai due complementari, perciò possiamo scrivere:

$$
\begin{align}
A^c \cap B^c &= \{5, 7, 8, 9, 10\} \cap \{1, 3, 5, 7, 9\} \\[6pt]
&= \{5, 7, 9\}
\end{align}
$$

I due insiemi coincidono, verificando la prima legge per gli insiemi scelti.

- - -

Utilizzando gli stessi insiemi verifichiamo il principio di inclusione-esclusione, ovvero la formula che calcola la cardinalità dell'unione di due insiemi finiti sommando le loro cardinalità e sottraendo quella dell'intersezione. Ciascuno dei due insiemi della $(4)$ ha cinque elementi e la loro intersezione ne ha tre:

$$
|A| = 5 \quad |B| = 5 \quad |A \cap B| = 3
$$

Nella somma $|A| + |B|$ gli elementi comuni vengono contati due volte e sottraendo la cardinalità dell'intersezione, ogni elemento dell'unione viene contato una sola volta:

$$
|A \cup B| = 5 + 5 - 3 = 7
$$

Il conteggio diretto degli elementi di $A \cup B = \{1, 2, 3, 4, 6, 8, 10\}$ conferma che $|A \cup B| = 7,$ come previsto dal principio.

- - -

Calcoliamo infine la differenza simmetrica, che contiene gli elementi appartenenti a uno solo dei due insiemi. Per definizione vale l'uguaglianza:

$$
A \triangle B = (A \setminus B) \cup (B \setminus A)
$$

Gli elementi di $A$ che non appartengono a $B$ formano l'insieme $A \setminus B = \{1, 3\},$ mentre quelli di $B$ che non appartengono ad $A$ formano l'insieme $B \setminus A = \{8, 10\}.$ La loro unione è dunque:

$$
A \triangle B = \{1, 3, 8, 10\}
$$

Lo stesso risultato si può ottenere rimuovendo dall'unione gli elementi dell'intersezione, poiché sono quelli che appartengono a entrambi gli insiemi:

$$
\begin{align}
(A \cup B) \setminus (A \cap B) &= \{1, 2, 3, 4, 6, 8, 10\} \setminus \{2, 4, 6\} \\[6pt]
&= \{1, 3, 8, 10\}
\end{align}
$$

Entrambe le espressioni danno quindi $A\triangle B = \{1, 3, 8, 10\}.$
