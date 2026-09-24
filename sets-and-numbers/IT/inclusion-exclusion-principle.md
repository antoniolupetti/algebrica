---
title: The Inclusion-Exclusion Principle
source: https://algebrica.org/inclusion-exclusion-principle/
license: CC BY-NC 4.0
tags:
  - cardinality
  - combinatorics
  - derangements
  - divisibility
  - inclusion-exclusion
  - set-operations
---

## Definizione

Il principio di inclusione-esclusione è un'importante regola di conteggio che consente di determinare quanti elementi di un insieme finito soddisfano almeno una condizione tra molte, in modo che ogni elemento venga contato una sola volta, anche se ne soddisfa più di una. Procediamo con una sua descrizione formale, fissando un insieme finito di elementi $U$ e associando a ciascuna condizione che vogliamo verificare un sottoinsieme degli elementi di $U$ che la soddisfano. Se, ad esempio, le condizioni sono due e i sottoinsiemi corrispondenti sono $A$ e $B,$ per le operazioni tra insiemi otteniamo quanto segue:

+ L'unione $A \cup B$ contiene gli elementi che soddisfano almeno una delle due condizioni.
+ L'intersezione $A \cap B$ contiene gli elementi che soddisfano entrambe le condizioni.
+ Il complemento $U \setminus (A \cup B)$ contiene gli elementi che non soddisfano nessuna delle due condizioni.

Indichiamo quindi con $|A|$ la cardinalità del sottoinsieme $A,$ che rappresenta il numero dei suoi elementi. La somma $|A|+|B|$ fa sì che un elemento appartenente soltanto ad $A$ o soltanto a $B$ venga contato una sola volta, mentre un elemento comune ai due sottoinsiemi viene contato due volte. Per fare in modo che anche in quest'ultimo caso l'elemento comune sia contato una sola volta, ricorriamo alla seguente relazione:

$$
|A \cup B| = |A| + |B| - |A \cap B| \tag{1}
$$

Quando $A$ e $B$ sono disgiunti, l'intersezione è vuota e la formula si riduce alla somma delle cardinalità dei sottoinsiemi, mentre se $A \subseteq B,$ allora $A \cap B=A$ e la formula restituisce $|A \cup B|=|B|.$

- - -

Consideriamo ora il caso di una famiglia finita di sottoinsiemi di un insieme finito $U$ dati da $A_1,\ldots,A_n$ e con $n \geq 1.$ Per ogni intero $k$ compreso tra $1$ e $n,$ indichiamo con $S_k$ la somma delle cardinalità di tutte le intersezioni ottenute scegliendo $k$ insiemi con indici distinti. Possiamo quindi scrivere:

$$ \tag{2}
S_k := \sum_{1 \leq i_1 < \cdots < i_k \leq n}
|A_{i_1} \cap \cdots \cap A_{i_k}|
$$

Nella $(2),$ la condizione $i_1<\cdots<i_k$ assicura che gli indici siano disposti in ordine crescente così da contare ogni combinazione una sola volta. Questo implica che $S_1$ sommi le cardinalità dei singoli insiemi, $S_2$ quelle delle intersezioni a due a due e $S_n$ sia la cardinalità dell'intersezione di tutti gli insiemi. Il principio di inclusione-esclusione afferma che:

$$ \tag{3}
\left|\bigcup_{i=1}^{n} A_i\right|
= \sum_{k=1}^{n} (-1)^{k+1}S_k
$$

In altre parole, la formula $(3)$ calcola il numero di elementi dell'unione nel modo seguente:

+ Per $k=1,$ si sommano le cardinalità dei singoli insiemi, ottenendo il contributo $+S_1.$
+ Per $k=2,$ si sottraggono le cardinalità delle intersezioni a due a due, ottenendo il contributo $-S_2.$
+ Per $k=3,$ si aggiungono le cardinalità delle intersezioni a tre a tre, ottenendo il contributo $+S_3.$

Si prosegue fino a $k=n,$ alternando somme e sottrazioni secondo il segno del fattore $(-1)^{k+1}$ finché non si ottiene l'ultimo termine, che riguarda l'intersezione di tutti gli insiemi. Facciamo un esempio per rendere più chiara la $(3)$ e consideriamo tre insiemi $A,$ $B$ e $C.$ Applicando la $(3)$ con $n=3$ e sostituendo le espressioni di $S_1,$ $S_2$ e $S_3$ date dalla $(2),$ otteniamo:

$$
\begin{align}
|A \cup B \cup C|
&= |A| + |B| + |C| \\[6pt]
&\quad - |A \cap B| - |A \cap C| - |B \cap C| \\[6pt]
&\quad + |A \cap B \cap C|
\end{align}
$$

In questo modo, ogni elemento dell'unione viene contato una sola volta, anche quando appartiene a più insiemi, che è proprio il risultato che volevamo ottenere applicando il principio di inclusione-esclusione.

- - -

In molti problemi, tuttavia, è più semplice contare gli elementi da escludere anziché quelli cercati. In pratica, se un dato sottoinsieme $A_i$ contiene gli elementi che soddisfano la $i$-esima condizione da escludere, gli elementi cercati apparterranno al complemento dell'unione. Quindi si ha:

$$ \tag{4}
\begin{align}
\left|U \setminus \bigcup_{i=1}^{n} A_i\right|
&= |U| - \left|\bigcup_{i=1}^{n} A_i\right| \\[6pt]
&= |U| + \sum_{k=1}^{n} (-1)^k S_k
\end{align}
$$

Come potete notare, nella formula $(4)$ i segni sono invertiti rispetto alla formula dell'unione data dalla $(3).$ Questo procedimento può essere più rapido del conteggio diretto quando conosciamo la cardinalità di $U$ e riusciamo a contare facilmente gli elementi da escludere. In questo caso basta sottrarli a $|U|$ per ottenere gli elementi cercati senza doverli individuare uno per uno.

## Dimostrazione

Per dimostrare la $(3),$ si parte col calcolare il contributo di un singolo elemento $x$ alla sommatoria. Se $x$ non appartiene a nessuno dei sottoinsiemi $A_i,$ allora non appartiene neppure alle loro intersezioni e quindi il suo contributo è chiaramente nullo. Supponiamo però che $x$ appartenga all'unione e definiamo l'insieme degli indici dei sottoinsiemi che lo contengono:

$$
I_x := \{\ i \in \{1,\ldots,n\} \mid x \in A_i \ \}
$$

Per rendere la spiegazione il più chiara possibile, consideriamo i seguenti punti:

+ L'insieme $I_x$ è necessariamente non vuoto.
+ Ogni intersezione nella $(3)$ si ottiene scegliendo uno o più insiemi tra $A_1,\ldots,A_n.$
+ Indichiamo con $J$ l'insieme degli indici scelti (ad esempio, $J=\{1,3\}$ corrisponde all'intersezione $A_1 \cap A_3).$
+ L'intersezione degli insiemi scelti al punto precedente contiene $x$ se e solo se ciascuno di essi contiene $x.$ Per $J=\{1,3\},$ significa che $x$ deve appartenere sia ad $A_1$ sia ad $A_3.$

Dunque, per ottenere un'intersezione che contenga $x,$ dobbiamo scegliere gli insiemi tra quelli che contengono $x.$ I loro indici devono perciò appartenere a $I_x,$ ossia deve valere $J \subseteq I_x.$

Facciamo ora un passo avanti e indichiamo con $k=|J|$ il numero degli insiemi scelti. Per capire come viene contato $x,$ consideriamo i seguenti punti riferiti alla $(3):$

+ Si aggiungono le cardinalità dei singoli insiemi, quindi ogni insieme che contiene $x$ dà un contributo $+1$ al conteggio di $x.$
+ Si sottraggono le cardinalità delle intersezioni di due insiemi, perciò in questo caso ogni intersezione che contiene $x$ dà un contributo $-1.$
+ Si aggiungono le cardinalità delle intersezioni di tre insiemi e quindi ogni intersezione che contiene $x$ dà un contributo $+1.$

Per ogni $k$ da $1$ a $|I_x|,$ consideriamo dunque tutte le intersezioni di $k$ insiemi che contengono $x,$ ciascuna delle quali contribuisce al conteggio di $x$ con $(-1)^{k+1}.$ Poiché gli indici in $J$ individuano gli insiemi scelti, il loro numero è $k=|J|$ e il contributo dell'intersezione corrispondente è pari a $(-1)^{|J|+1}.$

Indichiamo ora con $c(x)$ la somma di tutti questi contributi, ottenendo:

$$ \tag{5}
c(x) = \sum_{\varnothing \neq J \subseteq I_x} (-1)^{|J|+1}
$$

Scegliamo un indice $j \in I_x.$ A ogni sottoinsieme non vuoto $J$ di $I_x$ che non contiene $j$ associamo il sottoinsieme $J \cup \{j\}.$ I due sottoinsiemi hanno cardinalità che differiscono di uno, quindi i loro contributi si cancellano:

$$ \tag{6}
(-1)^{|J|+1} + (-1)^{|J|+2} = 0
$$

Ogni sottoinsieme non vuoto diverso da $\{j\}$ compare in una sola coppia, i cui contributi si cancellano. Rimane il contributo $+1$ di $\{j\},$ quindi $c(x)=1.$ La formula conta dunque ogni elemento dell'unione una sola volta e gli elementi esterni zero volte. Questo dimostra il principio.

È utile mostrare che la stessa conclusione si può esprimere anche attraverso i coefficienti binomiali. Infatti, se $x$ appartiene a esattamente $m$ insiemi, con $m \geq 1,$ allora compare in $\binom{m}{k}$ intersezioni definite da $k$ indici. Raggruppando i termini della $(5)$ secondo il numero $k$ di indici scelti e ricordando che $c(x)=1,$ otteniamo la seguente identità:

$$
\sum_{k=1}^{m} (-1)^{k+1}\binom{m}{k} = 1
$$

## Esempio

Per mostrare un esempio in cui il principio si applica, proviamo a determinare quanti interi da $1$ a $120,$ estremi inclusi, non sono divisibili né per $4,$ né per $6,$ né per $9.$ Scriviamo quindi l'insieme $U$ e i sottoinsiemi $A,$ $B$ e $C$ che rappresentano le nostre condizioni:

$$
\begin{align}
U &= \{1,2,\ldots,120\} \\[6pt]
A &= \{\ m \in U \mid 4 \text{ divide } m \ \} \\[6pt]
B &= \{\ m \in U \mid 6 \text{ divide } m \ \} \\[6pt]
C &= \{\ m \in U \mid 9 \text{ divide } m \ \}
\end{align}
$$

Per applicare la formula $(4),$ dobbiamo calcolare le cardinalità dei tre insiemi e delle loro intersezioni e per questo procediamo in questo modo.

Per ogni intero positivo $d,$ i suoi multipli positivi non superiori a $120$ sono chiaramente i numeri $qd$ con $q$ intero tale che $1 \leq q \leq 120/d.$ Il loro numero è quindi $\lfloor 120/d \rfloor,$ dove $\lfloor t \rfloor$ indica il più grande intero minore o uguale a $t.$ Un intero è multiplo contemporaneamente di due divisori se e solo se è multiplo del loro minimo comune multiplo. Per esempio, $A \cap B$ contiene i multipli di $12,$ perché il minimo comune multiplo di $4$ e $6$ è $12.$ Applicando lo stesso criterio alle altre intersezioni otteniamo:

| Insieme           | Condizione              | Cardinalità                 |
| ----------------- | ----------------------- | --------------------------- |
| $A$               | Essere multiplo di $4$  | $\lfloor 120/4 \rfloor=30$  |
| $B$               | Essere multiplo di $6$  | $\lfloor 120/6 \rfloor=20$  |
| $C$               | Essere multiplo di $9$  | $\lfloor 120/9 \rfloor=13$  |
| $A \cap B$        | Essere multiplo di $12$ | $\lfloor 120/12 \rfloor=10$ |
| $A \cap C$        | Essere multiplo di $36$ | $\lfloor 120/36 \rfloor=3$  |
| $B \cap C$        | Essere multiplo di $18$ | $\lfloor 120/18 \rfloor=6$  |
| $A \cap B \cap C$ | Essere multiplo di $36$ | $\lfloor 120/36 \rfloor=3$  |

Notate come le intersezioni $A \cap C$ e $A \cap B \cap C$ coincidano, perché ogni multiplo di $36$ è anche multiplo di $6.$ Sostituendo ora i valori nella formula per il complemento si ricava:

$$
\begin{align}
|U \setminus (A \cup B \cup C)|
&= 120 - (30+20+13) + (10+3+6) - 3 \\[6pt]
&= 120 - 63 + 19 - 3 \\[6pt]
&= 73
\end{align}
$$

Tra $1$ e $120$ sono dunque presenti $73$ interi che non sono divisibili per nessuno dei tre numeri indicati.

## Dismutazioni

Consideriamo ora $n$ oggetti distinti, ciascuno con una posizione assegnata, e chiediamoci in quanti modi possiamo ridisporli affinché nessun oggetto occupi la propria posizione. In termini più formali, il problema si riduce a contare le permutazioni $\sigma$ degli $n$ oggetti per le quali $\sigma(i) \neq i$ per ogni indice $i.$ Queste permutazioni sono dette permutazioni senza punti fissi, o dismutazioni, e indichiamo il loro numero con $D_n.$

Per $n \geq 1,$ prendiamo come insieme $U$ tutte le permutazioni degli $n$ oggetti. La sua cardinalità è data dal fattoriale $n!,$ che conta i modi in cui si possono ordinare $n$ oggetti distinti. Per ogni indice $i,$ definiamo $A_i$ come l'insieme delle permutazioni che lasciano l'oggetto $i$ nella propria posizione e scriviamo:

$$
A_i := \{\ \sigma \in U \mid \sigma(i)=i \ \}
$$

Le permutazioni che stiamo cercando non appartengono a nessun insieme $A_i$ e quindi il loro numero è dato dalla seguente formula:

$$\tag{7}
D_n = \left|U \setminus \bigcup_{i=1}^{n} A_i\right|
$$

Se imponiamo a $k$ oggetti specificati di rimanere nelle proprie posizioni, gli altri $n-k$ oggetti possono essere permutati liberamente nelle posizioni rimanenti. Perciò ogni intersezione relativa a $k$ indici distinti ha cardinalità $(n-k)!.$ Poiché sappiamo che i modi di scegliere i $k$ indici sono $\binom{n}{k},$ la somma delle cardinalità di queste intersezioni è data da:

$$ \tag{8}
S_k = \binom{n}{k}(n-k)!
$$

Sostituendo $|U|=n!$ e $S_k=\binom{n}{k}(n-k)!$ nella $(4),$ otteniamo quindi il numero delle permutazioni che è pari a:

$$
\begin{align}
D_n
&= n! + \sum_{k=1}^{n} (-1)^k\binom{n}{k}(n-k)! \\[6pt]
&= \sum_{k=0}^{n} (-1)^k\binom{n}{k}(n-k)! \\[6pt]
&= n!\sum_{k=0}^{n} \frac{(-1)^k}{k!}
\end{align}
$$

Per esempio, con cinque oggetti otteniamo:

$$
\begin{align}
D_5
&= 5!\left(1-1+\frac{1}{2!}-\frac{1}{3!}+\frac{1}{4!}-\frac{1}{5!}\right) \\[6pt]
&= 120-120+60-20+5-1 \\[6pt]
&= 44
\end{align}
$$

Esistono quindi esattamente $44$ permutazioni di cinque oggetti nelle quali nessun oggetto conserva la propria posizione.
