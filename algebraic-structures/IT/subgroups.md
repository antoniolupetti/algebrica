---
title: Subgroups
source: https://algebrica.org/subgroups/
license: CC BY-NC 4.0
tags:
  - algebraic-structures
  - cyclic-subgroup
  - finite-group
  - generated-subgroup
  - group-theory
  - subgroup
---

## Definizione e proprietà

Dato un gruppo $G,$ un sottoinsieme $H \subseteq G$ è un sottogruppo di $G$ se è a sua volta un gruppo rispetto all'operazione di $G$ ristretta a $H.$ Si scrive allora $H \leq G.$ Vediamo quali proprietà occorre verificare perché un sottoinsieme $H$ sia un sottogruppo. L'associatività vale già in $G$ per ogni terna di elementi, quindi vale anche quando i tre elementi appartengono a $H.$ Quanto all'elemento neutro $e,$ si può dimostrare che quello di un sottogruppo coincide necessariamente con $e.$ Infatti, se $u$ è il neutro di $H,$ si ha $uu=u$ in $H$ e $ue=u$ in $G.$ Poiché il prodotto è lo stesso, da $uu=ue$ possiamo concludere che $u=e.$ Anche l'inverso di ciascun $a \in H$ coincide con il suo inverso in $G,$ perché in entrambi i gruppi è l'unica soluzione dell'equazione $ax=e.$

Per riconoscere un sottogruppo possiamo dunque usare l'elemento neutro e gli inversi di $G$ e verificare le seguenti condizioni, che sono necessarie e sufficienti:

$$
\begin{align}
&e \in H \tag{1a} \\[6pt]
&ab \in H \qquad \forall \ a,b \in H \tag{1b} \\[6pt]
&a^{-1} \in H \qquad \forall a \in H \tag{1c}
\end{align}
$$

Ogni gruppo $G$ è un sottogruppo di sé stesso e contiene il sottogruppo banale $\{e\},$ formato dal solo elemento neutro. Un sottogruppo si dice proprio se è diverso da $G.$ In particolare, quando $G$ ha più di un elemento, anche $\{e\}$ è un sottogruppo proprio.

Per un sottoinsieme non vuoto $H \subseteq G,$ le tre condizioni precedenti si possono riunire in un unico criterio:

$$
\begin{align}
H \leq G \quad &\Longleftrightarrow \quad \bigl(\forall a,b \in H,\ ab^{-1} \in H\bigr) \tag{2}
\end{align}
$$

Se $H$ è un sottogruppo e $a,b \in H,$ per la $(1\mathrm{c})$ anche $b^{-1}$ appartiene a $H,$ mentre se applichiamo la $(1\mathrm{b})$ ad $a$ e $b^{-1},$ otteniamo $ab^{-1} \in H.$ Per l'implicazione inversa, supponiamo che $xy^{-1} \in H$ per ogni $x,y \in H.$ Dati $a,b \in H,$ applichiamo l'ipotesi, nell'ordine, alle coppie $(a,a),$ $(e,b)$ e $(a,b^{-1}).$ Otteniamo rispettivamente $e \in H,$ $b^{-1} \in H$ e $ab \in H,$ quindi $H$ soddisfa le tre condizioni di sottogruppo.

- - -

Vediamo ora come usare il criterio $(2)$ per stabilire se i multipli di un intero $n \geq 1$ formano un sottogruppo di $(\mathbb{Z},+).$ In questo gruppo l'operazione è l'addizione e l'inverso di $b$ è il suo opposto $-b,$ perciò l'espressione $ab^{-1}$ della $(2)$ si scrive $a+(-b)=a-b.$ L'insieme $n\mathbb{Z}$ dei multipli di $n$ contiene lo zero, quindi resta da verificare che la differenza di due multipli di $n$ sia ancora un multiplo di $n.$ Scriviamo due multipli qualunque come $nr$ e $ns,$ con $r,s \in \mathbb{Z},$ e raccogliamo $n$ nella loro differenza:

$$
\begin{align}
nr-ns &= n(r-s) \in n\mathbb{Z} \tag{3}
\end{align}
$$

Poiché $r-s$ è un intero, la $(3)$ mostra che la differenza appartiene a $n\mathbb{Z}.$ Per il criterio $(2),$ dunque, $n\mathbb{Z}$ è un sottogruppo di $(\mathbb{Z},+).$ Per $n=2$ si ottiene il sottogruppo degli interi pari.

- - -

Vediamo infine perché, se $H$ è finito e non vuoto, basta verificare la chiusura rispetto al prodotto. Fissiamo $a \in H.$ I prodotti $ax$ con $x \in H$ appartengono a $H$ per la chiusura e sono tutti distinti per la legge di cancellazione. Poiché $H$ è finito, questi prodotti esauriscono $H,$ quindi tra essi compare $a,$ e da $ax=a$ segue che $x=e \in H.$ Lo stesso vale anche per $e,$ e da $ay=e$ segue $y=a^{-1} \in H.$ Questo ragionamento vale per ogni $a \in H,$ e quindi $H$ è un sottogruppo.

Applichiamo questo criterio al gruppo simmetrico $S_4,$ formato dalle permutazioni di $\{1,2,3,4\}$ con la composizione come operazione. Consideriamo l'insieme $H$ delle permutazioni che lasciano $4$ al suo posto, cosicché gli altri tre elementi si possono permutare liberamente. Quindi il numero degli elementi di $H$ è dato dal fattoriale $3!=6.$ Se applichiamo una dopo l'altra due permutazioni di $H,$ la prima manda $4$ in $4$ e la seconda fa lo stesso. La loro composizione appartiene dunque a $H$ e, poiché $H$ è finito e non vuoto, questa chiusura basta per concludere che $H$ è un sottogruppo di $S_4.$ Inoltre, il sottogruppo è proprio perché lo scambio di $3$ e $4$ appartiene a $S_4$ e sposta $4.$

## Intersezione e unione di sottogruppi

Consideriamo ora due sottogruppi $H$ e $K$ di uno stesso gruppo $G$ e dimostriamo che la loro intersezione è un sottogruppo. Poiché entrambi contengono $e,$ l'intersezione è non vuota. Se $a,b \in H \cap K,$ possiamo applicare la $(2)$ prima in $H$ e poi in $K.$ Il prodotto $ab^{-1}$ appartiene quindi a entrambi i sottogruppi, cioè appartiene a $H \cap K.$ Per il criterio $(2)$ questo dimostra che $H \cap K \leq G.$

Lo stesso argomento vale per l'intersezione di una famiglia non vuota di sottogruppi di $G,$ anche quando la famiglia è infinita. L'elemento neutro appartiene a ciascun sottogruppo della famiglia e, se $a$ e $b$ appartengono a tutti i sottogruppi, anche $ab^{-1}$ vi appartiene. Per esempio, gli elementi di $4\mathbb{Z} \cap 6\mathbb{Z}$ sono gli interi divisibili sia per $4$ sia per $6$ e, poiché il minimo comune multiplo di $4$ e $6$ è $12,$ otteniamo $4\mathbb{Z} \cap 6\mathbb{Z}=12\mathbb{Z}.$

Consideriamo ora l'unione degli stessi due sottogruppi, $4\mathbb{Z} \cup 6\mathbb{Z},$ che contiene $4$ e $6,$ ma non la loro somma $10.$ In generale, l'unione di due sottogruppi $H$ e $K$ di $G$ è un sottogruppo di $G$ se e solo se uno dei due è contenuto nell'altro e vale la seguente relazione:

$$
\begin{align}
H \cup K \leq G \quad &\Longleftrightarrow \quad (H \subseteq K) \lor (K \subseteq H) \tag{4}
\end{align}
$$

Se uno dei sottogruppi contiene l'altro, l'unione coincide con il maggiore. Altrimenti scegliamo $h \in H \setminus K$ e $k \in K \setminus H.$ Se $hk$ appartenesse a $H,$ anche $k=h^{-1}(hk)$ apparterrebbe a $H.$ Se appartenesse a $K,$ anche $h=(hk)k^{-1}$ apparterrebbe a $K.$ Entrambe le conclusioni contraddicono la scelta iniziale. L'unione non è dunque chiusa rispetto al prodotto e la $(4)$ è dimostrata.

## Sottogruppo generato da un insieme

Come possiamo individuare il più piccolo sottogruppo che contiene certi elementi assegnati? In linea generale, dato un sottoinsieme $S \subseteq G,$ prendiamo tutti i sottogruppi di $G$ che contengono $S$ e tra questi deve esserci almeno $G,$ per cui possiamo applicare il risultato sull'intersezione. Il sottogruppo che otteniamo si chiama sottogruppo generato da $S$ e si indica in questo modo:

$$
\begin{align}
\langle S \rangle &= \bigcap_{\substack{H \leq G \\ S \subseteq H}} H \tag{5}
\end{align}
$$

Ogni elemento di $S$ appartiene a tutti i sottogruppi che compaiono nella $(5),$ quindi appartiene anche a $\langle S \rangle.$ Infatti l'intersezione è contenuta in ciascuno di questi sottogruppi e in questo senso $\langle S \rangle$ è il più piccolo sottogruppo rispetto all'inclusione.

Per descrivere gli elementi del sottogruppo definito nella $(5),$ consideriamo l'insieme $P$ di tutti i prodotti finiti di elementi di $S$ e dei loro inversi, compreso il prodotto vuoto $e.$ Ogni sottogruppo che contiene $S$ contiene anche questi prodotti, e quindi si ha che $P \subseteq \langle S \rangle.$

Per ottenere l'inclusione opposta, basta osservare che moltiplicando due prodotti di $P$ si forma un unico prodotto dello stesso tipo. Anche l'inverso appartiene a $P,$ perché si ottiene invertendo l'ordine dei fattori e sostituendo ciascuno con il suo inverso. Poiché $e \in P,$ ne segue che $P$ è un sottogruppo. Inoltre ogni elemento di $S$ è un prodotto di un solo fattore, quindi $P$ contiene $S.$ Per la $(5)$ si ha dunque $\langle S \rangle \subseteq P,$ e questo dimostra che $\langle S \rangle = P.$ Nel caso particolare in cui $S=\{g\},$ questi prodotti sono le potenze intere di $g$ e formano il sottogruppo ciclico $\langle g \rangle = \{g^k \mid k \in \mathbb{Z}\}.$

Torniamo ora agli interi $4$ e $6$ visti sopra. Nella notazione additiva i prodotti diventano somme e gli inversi diventano opposti, quindi $\langle 4,6 \rangle$ è formato dagli interi della forma $4m+6n,$ con $m,n \in \mathbb{Z}.$ Per confrontare questo sottogruppo con $2\mathbb{Z},$ usiamo due identità valide per ogni $m,n,k \in \mathbb{Z}:$

$$
\begin{align}
4m+6n &= 2(2m+3n) \tag{6a} \\[6pt]
2k &= 4(-k)+6k \tag{6b}
\end{align}
$$

La $(6\mathrm{a})$ mostra che ogni somma $4m+6n$ è pari, mentre la $(6\mathrm{b})$ esprime ogni intero pari come una somma di questa forma. Dunque $\langle 4,6 \rangle = 2\mathbb{Z},$ cioè gli interi pari formano il più piccolo sottogruppo di $(\mathbb{Z},+)$ che contiene $4$ e $6.$ Per esempio, $2$ non appartiene all'unione $4\mathbb{Z} \cup 6\mathbb{Z},$ ma deve appartenere al sottogruppo generato perché $2=6-4.$
