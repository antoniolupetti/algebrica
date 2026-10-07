---
title: Cartesian Product
source: https://algebrica.org/cartesian-product/
license: CC BY-NC 4.0
tags:
  - axiom-of-choice
  - bijection
  - cardinality
  - cartesian-product
  - indexed-product
  - n-tuple
  - ordered-pair
  - set-operations
---

## Definizione

Il prodotto cartesiano è, in termini molto semplici, l'insieme di tutte le coppie ordinate che si possono ottenere tra due insiemi. Ciascuna coppia ha due componenti: la prima appartiene al primo insieme e la seconda al secondo. In termini formali, il prodotto cartesiano tra due insiemi $A$ e $B$ è dato dalla seguente identità:

$$
A \times B = \{\ (a,b) \mid a \in A,\ b \in B \ \} \tag{1}
$$

Per convenzione, nella $(1)$ si utilizza il simbolo $\times$ che indica proprio questa costruzione tra insiemi e non la moltiplicazione algebrica dei loro elementi. Due coppie sono uguali quando coincide l'ordine e il valore delle componenti ovvero:

$$
(a,b)=(c,d) \iff a=c \text{ e } b=d \tag{2}
$$

È importante fare una distinzione: supponiamo di avere un insieme $A=\{2,5\}$ e un insieme $B=\{5,2\}$. Per le proprietà degli insiemi, $A$ e $B$ coincidono, perché sono composti dagli stessi elementi, indipendentemente dall'ordine. Nel caso delle coppie invece l'ordine è fondamentale. Se a partire da $A$ e $B$ determiniamo le coppie $(2,5)$ e $(5,2),$ queste sono diverse perché l'ordine dei loro elementi è scambiato.

Per mostrare come funziona la costruzione della $(1)$, consideriamo due insiemi, $A=\{2,5,8\}$ e $B=\{u,v\}$ e disponiamo i loro elementi in riga e in colonna. Nell'intersezione dei valori, inseriamo la coppia formata dal valore sulla relativa riga e colonna e otteniamo:

$$ \tag{3}
\begin{array}{c|ccc}
B\backslash A & 2 & 5 & 8 \\[6pt]
\hline
u & (2,u) & (5,u) & (8,u) \\[6pt]
v & (2,v) & (5,v) & (8,v)
\end{array}
$$

Abbiamo così costruito il prodotto cartesiano $A \times B$ dove ogni elemento di $A$ compare con entrambi gli elementi di $B.$ Le caselle interne elencano quindi tutte le coppie possibili ottenibili dal prodotto, che sono sei. Attraverso questa tabella possiamo anche calcolare la cardinalità di un prodotto di insiemi finiti. In generale, se $A$ ha $m$ elementi e $B$ ne ha $n$ il numero totale di coppie ottenibile è $m \times n,$ ossia:

$$
|A \times B|=|A|\cdot|B| \tag{4}
$$

Infatti, nell'esempio della tabella il prodotto contiene proprio $3\cdot 2=6$ elementi. La $(4)$ esprime quindi la formula per il calcolo della cardinalità del prodotto cartesiano. Se uno dei due insiemi è vuoto, non si può formare alcuna coppia mentre per il viceversa, se entrambi contengono almeno un elemento, scegliendo $a\in A$ e $b\in B$ si ottiene $(a,b)\in A\times B.$ Quindi:

$$
A\times B=\emptyset
\iff
\begin{cases}
A=\emptyset & \text{oppure} \\[6pt]
B=\emptyset
\end{cases}
$$

La $(3)$ resta valida anche in questo caso, poiché essendo almeno uno dei due fattori pari a zero, il prodotto ha cardinalità pari a zero.

- - -

Facciamo adesso una distinzione importante quando le componenti delle coppie non sono valori numerici ma insiemi. Bisogna tenere a mente che un insieme che contiene l'insieme vuoto non è vuoto. Per esempio, l'insieme delle parti di $\{q\},$ ovvero l'insieme che raccoglie tutti i sottoinsiemi di un insieme, incluso l'insieme vuoto è dato da $\mathcal{P}(\{q\})=\{\emptyset,\{q\}\}.$ Il suo prodotto cartesiano con un generico insieme singoletto (ovvero un insieme con un solo elemento) è dato da:

$$
\mathcal{P}(\{q\})\times\{3\}
=\{(\emptyset,3),(\{q\},3)\}
$$

Il prodotto quindi non è vuoto ma contiene quindi due elementi.

- - -

Quando entrambi i fattori della $(1)$ sono sottoinsiemi di $\mathbb{R},$ le coppie del prodotto $A \times B$ sono i punti del [piano cartesiano](../the-cartesian-coordinate-plane/). Quando il prodotto si estende a $\mathbb{R}$ con se stesso, otteniamo l'intero piano:

$$
\mathbb{R}^2=\mathbb{R}\times\mathbb{R}
=\{\ (x,y)\mid x\in\mathbb{R},\ y\in\mathbb{R}\ \}
$$

Per esempio, il prodotto degli [intervalli](../intervals/) $[-2,1]$ e $[0,3]$ è:

$$
[-2,1]\times[0,3]
=\{\ (x,y)\in\mathbb{R}^2\mid -2\leq x\leq 1,\ 0\leq y\leq 3\ \}
$$

Il prodotto è quindi il rettangolo con vertici $(-2,0),$ $(1,0),$ $(1,3)$ e $(-2,3),$ che comprendono il bordo e l'interno.

## L'ordine dei fattori

Vediamo ora come l'ordine dei fattori incide nel calcolo del prodotto cartesiano, riprendendo gli insiemi $A=\{2,5,8\}$ e $B=\{u,v\}$ visti in precedenza. Scambiando i fattori e moltiplicando $B\times A$ otteniamo una configurazione diversa da quella della tabella $(3),$ dove abbiamo un'inversione tra righe e colonne:

$$ \tag{5}
\begin{array}{c|cc}
A\backslash B & u & v \\[6pt]
\hline
2 & (u,2) & (v,2) \\[6pt]
5 & (u,5) & (v,5) \\[6pt]
8 & (u,8) & (v,8)
\end{array}
$$

Come si può vedere, la tabella $(5)$ contiene lo stesso numero di coppie della tabella $(3),$ ma le coppie sono diverse. Per esempio, la coppia $(u,2)$ appartiene solo a $B \times A$ e non appartiene invece a $A\times B,$ perché la sua prima componente $u$ non appartiene ad $A.$ Pertanto il prodotto cartesiano non è un'operazione commutativa e vale quindi che:

$$A\times B\neq B\times A$$

A ogni coppia $(a,b)$ di $A\times B$ possiamo associare la coppia $(b,a)$ di $B\times A,$ scambiando la posizione delle componenti. Per esempio, $(2,u)$ viene abbinata a $(u,2).$ La regola generale è:

$$
(a,b)\longleftrightarrow(b,a)
$$

Ogni coppia del secondo prodotto viene così abbinata a una sola coppia del primo. Per ritrovarla basta scambiare nuovamente le componenti, tornando da $(b,a)$ ad $(a,b).$ Nessuna coppia rimane esclusa e nessuna viene abbinata due volte ed è per questo motivo che i due prodotti hanno la stessa cardinalità, anche se contengono coppie diverse. Quando si tratta di insiemi non vuoti, l'uguaglianza $A\times B=B\times A$ vale se e solo se $A=B.$ Se invece almeno un fattore è vuoto, entrambi i prodotti sono vuoti anche quando i fattori sono diversi. In pratica vale la seguente relazione:

$$
A\times B=B\times A
\iff
\begin{cases}
A=B & \text{oppure} \\[6pt]
A=\emptyset & \text{oppure} \\[6pt]
B=\emptyset
\end{cases}
$$

## Operazioni tra insiemi

Con la $(1)$ abbiamo definito il prodotto cartesiano come un'operazione tra insiemi e come tale ha una serie di proprietà che riguardano, in particolare, la distribuzione rispetto all'unione, all'intersezione e alla differenza. Quindi, se si considerano tre insiemi $A,$ $B$ e $C$ valgono le seguenti identità:

$$
\begin{align}
A\times(B\cup C)&=(A\times B)\cup(A\times C) \\[6pt]
A\times(B\cap C)&=(A\times B)\cap(A\times C) \\[6pt]
A\times(B\setminus C)&=(A\times B)\setminus(A\times C)
\end{align}
$$

+ Nella prima abbiamo che una coppia appartiene al membro di destra quando appartiene ad almeno uno dei prodotti $A\times B$ e $A\times C.$ Questo richiede che la prima componente sia in $A$ e che la seconda sia in almeno uno fra $B$ e $C,$ ossia in $B\cup C$ che equivale alla condizione di appartenenza al membro di sinistra.
+ Nella seconda relazione, nel membro di destra, la prima componente deve essere in $A$ e la seconda deve appartenere sia a $B$ sia a $C,$ che sono proprio le condizioni che definiscono il membro di sinistra.
+ Infine, nell'ultima, la coppia deve appartenere ad $A\times B$ ed essere esclusa da $A\times C.$ La prima condizione assicura già che la prima componente sia in $A.$ L'esclusione dal secondo prodotto equivale dunque a richiedere che la seconda componente non sia in $C.$ Essa appartiene dunque a $B\setminus C,$ come richiesto dal membro di sinistra.

Un'altra proprietà del prodotto cartesiano riguarda l'inclusione. Se $A\subseteq A'$ e $B\subseteq B',$ ogni coppia di $A\times B$ ha la prima componente in $A'$ e la seconda in $B'.$ Pertanto vale la seguente relazione:

$$
A\subseteq A' \text{ e } B\subseteq B'
\implies A\times B\subseteq A'\times B'
$$

## Prodotti di più fattori

Consideriamo adesso il caso in cui il prodotto cartesiano della $(1)$ è espresso come prodotto di $n$ insiemi numerici. Definiamo per prima cosa una $n$-upla ordinata che è una sequenza $(a_1,\ldots,a_n)$ con $n$ componenti, con $n\geq 1$. Due $n$-uple sono uguali se e solo se coincidono le componenti che occupano la stessa posizione. Il prodotto cartesiano di $n$ insiemi è quindi definito dalla seguente espressione:

$$ \tag{6}
A_1\times\cdots\times A_n
=\{\ (a_1,\ldots,a_n)\mid a_i\in A_i \text{ per ogni } i\in\{1,\ldots,n\}\ \}
$$

Se i fattori sono finiti, si può scegliere ciascuna componente in $|A_i|$ modi. Applicando ripetutamente la formula $(4)$ per la cardinalità del prodotto di due insiemi, si ottiene:

$$
|A_1\times\cdots\times A_n|=\prod_{i=1}^{n}|A_i|
$$

Quando tutti i fattori coincidono con uno stesso insieme, ad esempio l'insieme $A,$ si usa la notazione $A^n.$ Se $A$ è finito, allora $|A^n|=|A|^n.$ In particolare, $\mathbb{R}^n$ è l'insieme delle $n$-uple di numeri reali. Un caso particolare è $\mathbb{R}^3$ che descrive lo spazio mediante tre coordinate. In questo caso, con tre fattori occorre distinguere una tripla da una coppia che contiene un'altra coppia e le forme degli elementi sono:

$$
\begin{align}
((a,b),c)&\in(A\times B)\times C \\[6pt]
(a,(b,c))&\in A\times(B\times C) \\[6pt]
(a,b,c)&\in A\times B\times C
\end{align}
$$

Se un fattore è vuoto, tutte e tre le costruzioni danno l'insieme vuoto.

## Sottoinsiemi e sequenze binarie

I prodotti cartesiani sono utili nel calcolo combinatorio perché permettono di contare tutti i sottoinsiemi di un insieme finito. Consideriamo $E=\{e_1,\ldots,e_n\},$ con $n$ elementi distinti e a ogni sottoinsieme $S\subseteq E$ associamo la $n$-upla $(\varepsilon_1,\ldots,\varepsilon_n)\in\{0,1\}^n$ definita da:

$$ \tag{7}
\varepsilon_i=
\begin{cases}
1 & \text{se } e_i\in S \\[6pt]
0 & \text{se } e_i\notin S
\end{cases}
$$

Ogni componente $\varepsilon_i$ della $(7)$ indica se l'elemento $e_i$ appartiene o meno a $S.$ La $n$-upla così costruita contiene soltanto i valori $0$ e $1,$ perciò si chiama sequenza binaria. L'insieme $\{0,1\}^n$ raccoglie tutte queste sequenze di lunghezza $n.$

Ad esempio, se fissiamo l'ordine $e_1,e_2,e_3,e_4,$ il sottoinsieme $S=\{e_2,e_4\}$ viene descritto dalla sequenza $(0,1,0,1).$ Il primo e il terzo valore sono $0$ perché $e_1$ ed $e_3$ non appartengono a $S$ mentre il secondo e il quarto sono $1$ perché $e_2$ ed $e_4$ vi appartengono. Possiamo anche partire dalla sequenza per ritrovare il relativo sottoinsieme, leggendo le componenti nell'ordine fissato e includendo $e_i$ quando nella posizione $i$ compare $1,$ e escludendolo quando compare $0.$ Per esempio, da $(0,1,0,1)$ otteniamo proprio $\{e_2,e_4\}.$

Notate come ogni sottoinsieme determina una sola sequenza, e ogni sequenza determina un solo sottoinsieme. Contare i sottoinsiemi di $E$ equivale quindi a contare gli elementi del prodotto cartesiano $\{0,1\}^n$ e poiché ciascuno dei suoi fattori ha due elementi, la cardinalità è pari a:

$$
|\mathcal{P}(E)|=|\{0,1\}^n|=2^n
$$

## Prodotti di famiglie indicizzate

La definizione di prodotto cartesiano si estende a una famiglia di insiemi $(A_i)_{i\in I},$ anche quando l'insieme degli indici $I$ è infinito, ovvero quando il prodotto comprende infiniti fattori. Un elemento del prodotto assegna a ogni indice $i$ una componente appartenente ad $A_i$ e si scrive:

$$
\prod_{i\in I}A_i
=\{\ (a_i)_{i\in I}\mid a_i\in A_i \quad \forall \ i\in I\ \}
$$

Formalmente, una tale famiglia è una funzione $a$ con dominio $I$ e valori nell'unione dei suoi fattori, per cui vale la condizione:

$$
a\colon I\longrightarrow\bigcup_{i\in I}A_i
\qquad
a(i)\in A_i \quad \forall \ i\in I
$$

Se un fattore è vuoto, il prodotto è vuoto, perché nessuna funzione può assegnare a quell'indice un valore ammesso. Per un insieme di indici vuoto esiste invece esattamente una funzione con dominio vuoto, dato dalla funzione vuota. Il prodotto senza fattori è quindi un singoletto e ha cardinalità $1$ ($A^0,$ ha come unico elemento è la sequenza vuota).
