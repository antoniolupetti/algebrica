---
title: Binomial Coefficient
source: https://algebrica.org/binomial-coefficient/
license: CC BY-NC 4.0
tags:
  - binomial-coefficient
  - binomial-distribution
  - binomial-theorem
  - combinatorics
  - factorial
  - generalized-binomial-coefficient
  - pascals-triangle
  - recursion
  - vandermonde-identity
---

## Introduzione

Il coefficiente binomiale nasce per risolvere i problemi di calcolo combinatorio e rappresenta il numero di modi in cui si possono scegliere $k$ elementi da un insieme di $n$ elementi, senza tenere conto dell'ordine in cui vengono scelti. È descritto dalla seguente formula dove è presente il fattoriale che, come abbiamo visto nella voce dedicata, rappresenta le permutazioni di $n$ oggetti distinti:

$$\tag{1}
\binom{n}{k} = \begin{cases} \displaystyle\frac{n!}{k!(n-k)!} & \text{se } 0 \leq k \leq n \\[6pt] 0 & \text{se } k > n \end{cases}
$$

Per esempio, determinare il seguente coefficiente binomiale:

$$\binom{4}{2}$$
Vogliamo quindi determinare quanti insiemi di $2$ elementi si possono scegliere da un insieme di $4$ elementi rappresentato da $P = \{p, q, r, s\}.$ Le coppie che si possono formare sono sei, ovvero:

$$\tag{2}
\{p,q\} \quad \{p,r\} \quad \{p,s\} \quad \{q,r\} \quad \{q,s\} \quad \{r,s\}
$$

In questo caso si considera la coppia $\{p,q\}$ uguale alla coppia $\{q,p\}$ e pertanto, a differenza delle permutazioni, si conta una sola volta come per tutte le altre coppie individuate nella $(2).$ Applicando la formula $(1)$ con $n = 4$ e $k = 2,$ otteniamo lo stesso valore e il risultato coincide con le coppie riportate nella $(2)$:

$$
\binom{4}{2} = \frac{4!}{2!(4-2)!} = \frac{4!}{2!2!} = \frac{24}{2 \cdot 2} = 6
$$

Una menzione va fatta per la seconda condizione della $(1)$ che è abbastanza intuitiva e segue dal fatto che, se $k > n,$ non è mai possibile scegliere $k$ elementi distinti da un insieme che ne contiene soltanto $n$ e quindi il numero delle scelte possibili è pari a zero.Ad esempio se riconsideriamo l'insieme $P$ con quattro elementi, non possiamo mai scegliere $5$ elementi distinti perché ne abbiamo a disposizione solamente $4,$ e quindi si ha che:

$$\binom{4}{5} = 0$$
- - -

La formula $(1)$ può essere riscritta in forma generalizzata sostituendo $n$ con un qualunque numero reale $\alpha,$ mentre $k$ resta un intero non negativo. 

$$\tag{3}
\binom{\alpha}{k} = \frac{\alpha(\alpha - 1)(\alpha - 2) \cdots (\alpha - k + 1)}{k!}
$$

Vediamo alcuni casi tipici:

+ Per $k = 0,$ il prodotto al numeratore è vuoto e vale $1,$ quindi anche la $(3)$ vale $1.$
+ Se $\alpha$ è un intero non negativo e $k \leq \alpha,$ l'espressione si riduce alla $(1).$ 
+ Se $\alpha$ è un intero non negativo e $k > \alpha,$ il coefficiente binomiale vale $0.$ Infatti, in questo caso sottraiamo da $\alpha$ tutti gli interi da $0$ a $k-1$ che, per la condizione $k > \alpha,$ comprendono anche $\alpha$ stesso. Il prodotto al numeratore contiene quindi il fattore $\alpha-\alpha=0$ e la $(3)$ vale zero.

Per gli altri valori reali di $\alpha,$ il prodotto al numeratore rimane definito e il denominatore $k!$ è positivo e quindi la formula restituisce un valore che non è necessariamente intero.

- - -

La $(3)$ consente di estendere lo sviluppo delle potenze di un binomio a qualsiasi esponente reale $\alpha.$ Per $|x| < 1,$ vale la formula binomiale di Newton:

$$\tag{4}
(1 + x)^{\alpha} = \sum_{k=0}^{\infty} \binom{\alpha}{k} x^k
$$

Se $\alpha = n$ è un intero non negativo la serie si riduce alla somma finita del [teorema binomiale](../binomial-theorem/) mentre, per gli altri valori reali di $\alpha$ lo sviluppo contiene un numero infinito di termini. Consideriamo ora due casi particolari della $(4)$. Nel primo poniamo $\alpha = -1,$ ottenendo una serie geometrica:

$$
\frac{1}{1+x} = \sum_{k=0}^{\infty} (-1)^k x^k
$$

Nel secondo poniamo $\alpha = 1/2,$ ottenendo lo sviluppo di $\sqrt{1+x},$ che si usa in fisica (ad esempio per stimare la variazione del periodo di un pendolo semplice) quando $x$ è molto piccolo in valore assoluto:

$$
\sqrt{1+x} = 1 + \frac{1}{2}x - \frac{1}{8}x^2 + \frac{1}{16}x^3 - \cdots
$$

- - -

Il coefficiente binomiale compare anche nella distribuzione binomiale. Se si considerano $n$ prove indipendenti, ciascuna con due esiti possibili e probabilità costanti $p$ di successo e $q = 1-p$ di insuccesso, la probabilità di ottenere esattamente $x$ successi è data dalla distribuzione:

$$
b(x; n, p) = \binom{n}{x} p^{x} q^{n - x}
$$

L'espressione combina il coefficiente binomiale, che conta i modi in cui si possono distribuire $x$ successi tra $n$ prove, e il fattore $p^x q^{n-x},$ che esprime la probabilità di ciascuna di queste disposizioni.

## Triangolo di Pascal

Il triangolo di Pascal è una rappresentazione grafica che declina i coefficienti binomiali che compaiono nello sviluppo di un binomio $(a+b)$ elevato a una potenza intera non negativa. La prima riga contiene soltanto $1,$e per $n \geq 2$ e $1 \leq k \leq n-1$ vale la seguente relazione

$$\tag{5}
\binom{n}{k} = \binom{n - 1}{k - 1} + \binom{n - 1}{k}
$$

In pratica, la $5$ è una formula ricorsiva per cui ogni elemento interno del triangolo è la somma dei due elementi della riga precedente situati immediatamente sopra di esso. Ad esempio se costruiamo il triangolo per le prime sei righe otteniamo la seguente rappresentazione:

$$
\begin{array}{c}
1 \\[6pt]
1 \quad 1 \\[6pt]
1 \quad 2 \quad 1 \\[6pt]
1 \quad 3 \quad 3 \quad 1 \\[6pt]
1 \quad 4 \quad 6 \quad 4 \quad 1 \\[6pt]
1 \quad 5 \quad 10 \quad 10 \quad 5 \quad 1
\end{array}
$$

Numerando le righe e le colonne a partire da $0,$ l'elemento nella riga $n$ e nella colonna $k$ corrisponde al coefficiente binomiale dato dalla $(1).$ Per esempio, il numero nella posizione $n = 4,$ $k = 2$ è:

$$
\binom{4}{2} = \frac{4!}{2!(4 - 2)!} = \frac{4!}{2!2!} = \frac{24}{4} = 6
$$

Se infatti prendiamo la quinta riga, quella con indice indice $4,$ e la terza colonna, con indice $2$, trovando nel triangolo il numero $6.$ 

## Proprietà fondamentali

Elenchiamo di seguito una serie di proprietà fondamentali del coefficiente binomiale che risultano utili nella risoluzione dei problemi che lo vedono coinvolto. La prima proprietà è quella per cui i valori agli estremi della riga seono sempre pari a $1$. Infatti si ha:

$$
\binom{n}{0} = \binom{n}{n} = 1
$$

Abbiamo poi una proprietà di simmetria che riguarda la scelta di un sottoinsieme di $k$ elementi da un insieme di $n$ elementi per cui il numero di modi in cui si può effettuare questa scelta è uguale al numero di modi in cui si possono scegliere i rimanenti $n-k$ elementi:

$$
\binom{n}{k} = \binom{n}{n-k}
$$

Visivamente l'esito di questa proprietà si può osservare dal fatto che in ogni riga del triangolo di Pascal, i numeri posti alla stessa distanza a destra e a sinistra dell'asse centrale sono uguali.

La proprietà successiva è quella additiva che mette in relazione due coefficienti binomiali consecutivi per i quali vale la seguente identità:

$$
\binom{n}{k} + \binom{n}{k+1} = \binom{n+1}{k+1}
$$

In pratica proprietà permette di calcolare un coefficiente binomiale a partire dai due coefficienti della riga precedente.

- - -

Soffermiamoci adesso su un'ulteriore proprietà che merita un approfondimento e che riguarda la natura ricorsiva del coefficiente binomiale. In pratica, per contare i modi in cui si possono scegliere $k$ elementi da un insieme di $n$ basta conoscere le risposte a due versioni più piccole del problema, scegliendo rispettivamente $k-1$ e $k$ elementi da un insieme di $n-1$ elementi, come rappresentato nella seguente formula:

$$\tag{6}
\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}
$$

Calcoliamo per esempio il seguente valore del coefficiente binomiale riscrivendolo usando la $(6)$:

$$
\binom{3}{2} = \binom{2}{1} + \binom{2}{2} = 2 + 1 = 3
$$


## Identità notevoli

Elenchiamo ora una serie di identità fondamentali del coefficiente binomiale utili nella risoluzione dei problemi. La prima identità afferma che la somma di tutti i coefficienti binomiali della riga $n$ del triangolo di Pascal è uguale a $2^n:$

$$\tag{7}
\sum_{k=0}^{n} \binom{n}{k} = 2^n
$$

Per esempio, consideriamo la somma dei coefficienti binomiali della quinta riga, ovvero di indice $4$ del triangolo di Pascal. L'insieme composto da $4$ elementi ha un sottoinsieme vuoto, quattro sottoinsiemi di un elemento, sei di due elementi, quattro di tre elementi e uno di quattro elementi. Pertanto applicando la $(7)$ otteniamo il valore $16$:

$$
\binom{4}{0} + \binom{4}{1} + \binom{4}{2} + \binom{4}{3} + \binom{4}{4} = 1 + 4 + 6 + 4 + 1 = 16 = 2^4
$$
 
- - -

Abbiamo poi un'ulteriore identità che riguarda la somma alternata, analoga alla $(7)$, ma con segni alterni. Per $n \geq 1,$ vale la seguente relazione:

$$
\sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0
$$

Questa identità si ricava dal teorema binomiale ponendo $a = 1$ e $b = -1$ e il risultato esprime una simmetria tra i sottoinsiemi di cardinalità pari e quelli di cardinalità dispari.

- - -

Mostriamo adesso la seguente identità che mostra una proprietà della somma diagonale dei termini presenti nel triangolo di Pascal. Supponiamo di partire da un valore qualsiasi pari a $(1)$ posizionato tutto a sinistra di una generica riga $n$ e sommare tutti i valori lungo la diagonale fino alla riga $n+r$. Questa somma è pari al numero al numero in basso a sinistra dell'ultimo termine sommato. L'identità si può scrivere come:

$$
\sum_{i=0}^{r} \binom{n+i}{i} = \binom{n+r+1}{r}
$$

Per rendere chiara la formula, consideriamo ad esempio $n = 1$ e $r = 2$ e cioè partiamo dalla riga $1$ e sommiamo i termini che si incontrano scendendo della diagonale fino alla riga $3,$ ottenendo:

$$
\binom{1}{0} + \binom{2}{1} + \binom{3}{2} = 1 + 2 + 3 = 6
$$

Infatti il valore $6$ si trova proprio in basso a sinistra dell'ultimo termine $3.$

$$
\require{enclose}
\begin{array}{c}
1 \\[6pt]
1 \quad 1 \\[6pt]
1 \quad 2 \quad 1 \\[6pt]
1 \quad 3 \quad 3 \quad 1 \\[6pt]
1 \quad 4 \quad \enclose{circle}{6} \quad 4 \quad 1 \\[6pt]
1 \quad 5 \quad 10 \quad 10 \quad 5 \quad 1
\end{array}
$$

- - -

Infine, mostriamo l'identità di Vandermonde che conta quante sono le scelte possibili di $r$ elementi dall'unione di due insiemi disgiunti di $m$ e $n$ elementi:

$$\tag{8}
\binom{m+n}{r} = \sum_{k=0}^{r} \binom{m}{k} \binom{n}{r-k}
$$

Per fare un esempio concreto, riprendiamo l'esempio iniziale e ricontiamo i sottoinsiemi di due elementi ottenibili dall'insieme $P = \{p,q,r,s\},$ usando stavolta la $(8).$ Per prima cosa dividiamo $P$ in due sottoinsiemi disgiunti $A = \{p,q\}$ e $B = \{r,s\}$ e nella formula poniamo $m = n = 2$ e $r = 2.$ L'indice $k$ indica quanti dei due elementi scelti appartengono all'insieme $A,$ mentre i $2-k$ quanti appartengono a $B.$ Abbiamo tre casi:

+ Se $k = 0,$ significa che stiamo scegliendo entrambe gli elementi da $B$ e quindi l'unica coppia è $\{r,s\}.$
+ Se $k = 1,$ stiamo invece scegliendo un elemento da $A$ e uno da $B,$ perciò le coppie in tutto sono quattro, cioè $\{p,r\},$ $\{p,s\},$ $\{q,r\}$ e $\{q,s\}.$
+ Se $k = 2,$ stiamo considerando l'ultima opzione possibile, e quindi entrambi gli elementi appartengono ad $A$ e l'unica coppia è $\{p,q\}.$

Possiamo scrivere il tutto come:

$$
\begin{align}
\binom{4}{2} &= \binom{2}{0}\binom{2}{2} + \binom{2}{1}\binom{2}{1} + \binom{2}{2}\binom{2}{0} \\[6pt]
&= 1 \cdot 1 + 2 \cdot 2 + 1 \cdot 1 = 6
\end{align}
$$

Abbiamo quindi trovato le stesse coppie già elencate nella $(2)$ che in tutto sono $6.$

## Esempi

Vediamo adesso un paio di esempi che applica il coefficiente binomiale a casi reali. Nel primo esempio consideriamo un gruppo che comprende $7$ scienziati e $8$ ingegneri e vogliamo contare quanti gruppi si possono formare di $3$ scienziati e $4$ ingegneri. Per formarlo, dobbiamo scegliere $3$ scienziati tra i $7$ disponibili e $4$ ingegneri tra gli $8$ disponibili e quindi dobbiamo ricorrere al prodotto di due coefficienti binomiali:

$$
\binom{7}{3} \times \binom{8}{4}
$$

Calcolando i fattori otteniamo:

$$
\binom{7}{3} = \frac{7 \times 6 \times 5}{3 \times 2 \times 1} = 35
$$


$$
\binom{8}{4} = \frac{8 \times 7 \times 6 \times 5}{4 \times 3 \times 2 \times 1} = 70
$$

Pertanto il numero di gruppi possibili è pari a $35 \times 70 = 2.450.$

- - -

Consideriamo ora la stessa situazione dell'esempio precedente, con una condizione aggiuntiva: se due ingegneri per qualche ragione non possono essere assegnati allo stesso gruppo, quante combinazioni si possono formare? Intuitivamente è evidente che dobbiamo escludere i gruppi che comprendono entrambe gli ingegneri che non possono lavorare insieme. Procediamo in questo modo:

+ Consideriamo la presenza dei due ingegneri che non potrebbero lavorare insieme.
+ Per ciascun gruppo, questi occupano 2 dei 4 posti dedicati agli ingegneri.
+ Quindi dobbiamo sceglierne solo 2 tra gli $8-2=6$ rimasti, e quindi:

$$
\binom{6}{2}
$$

Non essendoci ulteriori vincoli, il numero di modi di scegliere gli scienziati è lo stesso dell'esempio precedente, e cioè:

$$
\binom{7}{3}
$$

Quindi il numero di gruppi non ammissibili, $N_{\text{NA}}$ che contengono entrambi gli ingegneri che non possono lavorare insieme, è quindi:

$$
N_{\text{NA}} = \binom{7}{3} \times \binom{6}{2}
$$

Calcolando i coefficienti e sostituendo i valori, otteniamo:

$$
\binom{7}{3} = 35 \qquad \binom{6}{2} = 15
$$

$$
N_{\text{NA}} = 35 \times 15 = 525
$$

A questo punto il calcolo è semplice e si riduce a sottrare dai casi ammissibili dell'esempio precedente, quelli non ammissibili appena trovati, ovvero:

$$
2.450 - 525 = 1.925
$$


