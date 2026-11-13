---
title: Topology of the Real Line
source: https://algebrica.org/topology-of-the-real-line/
license: CC BY-NC 4.0
tags:
  - accumulation-point
  - boundary-point
  - closed-set
  - closure
  - compactness
  - connectedness
  - heine-borel-theorem
  - interior-point
  - isolated-point
  - neighborhood
  - open-cover
  - open-set
  - real-line
---

## Intorni e insiemi aperti

La distanza tra due numeri reali $x$ e $y$ è $|x-y|.$ L'intorno aperto di centro $x$ e raggio $\varepsilon\gt 0$ è l'intervallo aperto formato dai punti la cui distanza da $x$ è minore di $\varepsilon$ ed è rappresentabile come:

$$
I_\varepsilon(x)=(x-\varepsilon,x+\varepsilon)
=\{y\in\mathbb{R}\mid |y-x|\lt\varepsilon\} \tag{1}
$$

L'intorno bucato di centro $x$ e raggio $\varepsilon$ si ottiene invece togliendo $x$ dalla $(1),$ ottenendo:

$$
I_\varepsilon^*(x)=I_\varepsilon(x)\setminus\{x\}
=\{y\in\mathbb{R}\mid 0\lt |y-x|\lt\varepsilon\} \tag{2}
$$

Un insieme $U\subseteq\mathbb{R}$ è aperto se per ogni $x\in U$ esiste un raggio $\varepsilon\gt 0$ tale che l'intorno aperto $I_\varepsilon(x)$ della $(1)$ sia interamente contenuto in $U.$ Per esempio, se $x\in(a,b),$ scegliendo come raggio la minore delle distanze $x-a$ e $b-x$ si ottiene un intorno contenuto in $(a,b),$ perciò l'intervallo è aperto.

Vediamo ora due proprietà che definiscono la topologia di $\mathbb{R}.$ L'insieme vuoto e $\mathbb{R}$ sono aperti e anche l'unione di una famiglia qualsiasi di insiemi aperti è a sua volta aperta, perché ogni punto dell'unione appartiene ad almeno uno degli insiemi della famiglia e ha quindi un intorno contenuto in quell'insieme. Se un punto appartiene all'intersezione di un numero finito di aperti, si sceglie per ciascun insieme un intorno del punto contenuto al suo interno. Il più piccolo dei raggi scelti è ancora positivo e l'intorno con quel raggio è contenuto in tutti gli insiemi, e quindi l'intersezione è aperta. 

Con infiniti aperti, i raggi degli intorni possono diventare arbitrariamente piccoli. Per esempio, gli intorni $I_{1/n}(0)$ contengono tutti $0,$ ma ogni $x\neq 0$ resta fuori da almeno uno di essi, perché per la proprietà archimedea si può scegliere $n$ con $1/n\lt |x|,$ per cui si ottiene:

$$
\bigcap_{n=1}^{\infty} I_{1/n}(0)=\{0\} \tag{3}
$$

Nella $(3)$ il punto comune è $0,$ ma nessun suo intorno aperto è contenuto nell'intersezione, che perciò non è aperta. Il criterio di apertura si può applicare anche ai singoli punti di un insieme $E\subseteq\mathbb{R}.$ Un punto è interno a $E$ se ha un intorno contenuto in $E$ ed è esterno se ha un intorno contenuto nel complementare $\mathbb{R}\setminus E.$ I punti i cui intorni incontrano sempre entrambi gli insiemi formano la cosiddetta frontiera $\partial E.$ L'interno $E^\circ$ è l'unione di tutti gli aperti contenuti in $E,$ quindi è il più grande di essi. Per il criterio appena visto, $E$ è aperto se e solo se $E=E^\circ.$ Ad esempio, se consideriamo $E=(0,1]$ l'interno è $(0,1),$ l'esterno è $(-\infty,0)\cup(1,+\infty)$ e la frontiera è $\{0,1\}.$

## Punti di accumulazione e insiemi chiusi

Un punto $x$ è di accumulazione per $E$ se ogni suo intorno aperto contiene almeno un punto di $E$ diverso da $x,$ ossia se ogni intorno bucato $(2)$ contiene almeno un punto di $E.$ L'insieme dei punti di accumulazione si indica con $E'.$ Un punto $x\in E$ è invece isolato se possiede un intorno che incontra $E$ soltanto in $x.$

Un punto $x$ appartiene a $E'$ se e solo se esiste una successione $(x_n)$ di punti di $E\setminus\{x\}$ che converge a $x.$ Infatti, se $x\in E',$ per ogni intero positivo $n$ si può scegliere un punto $x_n$ di $E$ nell'intorno bucato di raggio $1/n,$ ottenendo una successione che converge a $x.$ In caso contrario, una successione di punti di $E$ distinti da $x$ che converge a $x$ ha termini in ogni intorno bucato di $x.$

Per il teorema di Bolzano-Weierstrass, ogni sottoinsieme infinito e limitato di $\mathbb{R}$ possiede almeno un punto di accumulazione. La nozione interviene anche nella definizione di limite di una funzione, dove il punto a cui tende la variabile deve essere di accumulazione per il dominio.

Un insieme $F$ è chiuso se il suo complementare è aperto, ossia se ogni punto che non appartiene a $F$ ammette un intorno disgiunto da $F.$ Questo equivale a chiedere che $F'\subseteq F,$ perché per $x\notin F$ ogni punto di $F$ che appartiene a un intorno di $x$ appartiene anche al corrispondente intorno bucato. Per il criterio delle successioni, la condizione equivale a richiedere che il limite di ogni successione convergente di punti di $F$ appartenga a $F.$ Infatti, un limite fuori da $F$ sarebbe un punto di accumulazione fuori da $F,$ e questo darebbe origine a una successione di questo tipo.

L'intervallo $[a,b]$ è chiuso perché il suo complementare è l'unione di due intervalli aperti. L'intervallo $(0,1]$ non è aperto, poiché $1$ non è interno, e non è chiuso, poiché $0$ è un punto di accumulazione che non gli appartiene. Per le leggi di De Morgan, le intersezioni arbitrarie e le unioni finite di insiemi chiusi sono chiuse.
## Chiusura e densità

Definiamo ora il concetto di chiusura $\overline{E}$ che è il più piccolo insieme chiuso che contiene $E,$ ottenuto intersecando tutti i chiusi che lo contengono. Un punto non appartiene a $\overline{E}$ se e solo se possiede un intorno disgiunto da $E.$ Infatti, il complementare di $\overline{E}$ è aperto e disgiunto da $E,$ mentre il complementare di un intorno disgiunto da $E$ è un chiuso che contiene $E$ e quindi anche $\overline{E}.$ Da questo si ricavano le seguenti identità:

$$
\begin{align}
x\in\overline{E}
&\iff I_\varepsilon(x)\cap E\neq\emptyset
\quad\text{per ogni }\varepsilon\gt 0 \tag{4} \\[6pt]
\overline{E} &= E\cup E' \tag{5} \\[6pt]
\partial E &= \overline{E}\cap\overline{\mathbb{R}\setminus E}
 = \overline{E}\setminus E^\circ \tag{6}
\end{align}
$$

Se $x\in E,$ ogni suo intorno incontra $E$ almeno in $x.$ Se $x\notin E,$ la condizione nella $(4)$ equivale a richiedere che ogni intorno bucato di $x$ incontri $E,$ da cui segue la $(5).$ Inoltre, un punto sta fuori dalla chiusura del complementare di $E$ esattamente quando possiede un intorno contenuto in $E,$ perciò l'insieme dei punti esclusi da quella chiusura è $E^\circ.$

Un insieme $E$ è denso in $\mathbb{R}$ se $\overline{E}=\mathbb{R},$ ossia se incontra ogni aperto non vuoto. Ogni intervallo aperto non vuoto contiene sia numeri razionali sia numeri irrazionali, quindi entrambi gli insiemi sono densi e la $(6)$ dà $\partial\mathbb{Q}=\mathbb{R}.$ Poiché $\mathbb{Q}$ è numerabile, la retta reale è separabile, ossia possiede un sottoinsieme denso e numerabile.

## Connessione e intervalli

Un insieme $S\subseteq\mathbb{R}$ è connesso se non si può scrivere come unione di due sottoinsiemi disgiunti, non vuoti e aperti in $S.$ Un sottoinsieme di $S$ è aperto in $S$ se è l'intersezione di $S$ con un insieme aperto della retta. Se un insieme contiene due punti ma omette un punto $c$ compreso tra essi, le intersezioni con $(-\infty,c)$ e $(c,+\infty)$ lo separano in due sottoinsiemi non vuoti e aperti in $S.$ Dunque ogni insieme connesso non vuoto è un intervallo.

Supponiamo ora che un intervallo $I$ sia l'unione di due sottoinsiemi $U$ e $V,$ disgiunti, non vuoti e aperti in $I.$ Scelti $u\in U$ e $v\in V,$ possiamo supporre che $u\lt v.$ Poiché $I$ è un intervallo, contiene $[u,v].$ Sia $c$ l'estremo superiore di $U\cap[u,v].$ Poiché $V$ contiene un intorno relativo di $v,$ si ha $c\lt v.$ Se $c\in U,$ l'apertura di $U$ in $I$ dà punti di $U\cap[u,v]$ maggiori di $c,$ mentre se $c\in V$ esiste un intorno di $c$ disgiunto da $U\cap[u,v].$ Entrambi i casi contraddicono la definizione di $c$ e quindi ogni intervallo è connesso e gli unici sottoinsiemi della retta che sono al tempo stesso aperti e chiusi sono $\emptyset$ e $\mathbb{R}.$

Ogni insieme aperto non vuoto di $\mathbb{R}$ si può scrivere come unione di intervalli aperti a due a due disgiunti. Per ogni punto dell'insieme aperto si prendono tutti gli intervalli aperti che contengono quel punto e sono contenuti nell'insieme. La loro unione è ancora un intervallo aperto, perché gli intervalli hanno un punto in comune. Due intervalli massimali ottenuti in questo modo, se si incontrano, coincidono, poiché la loro unione sarebbe altrimenti un intervallo aperto più grande. Ciascuno contiene un razionale e intervalli disgiunti contengono razionali distinti, quindi gli intervalli della decomposizione sono al più numerabili.

## Compattezza e teorema di Heine-Borel

Un ricoprimento aperto di $K\subseteq\mathbb{R}$ è una famiglia di aperti la cui unione contiene $K.$ L'insieme $K$ è compatto se da ogni suo ricoprimento aperto si può estrarre una sottofamiglia finita che ricopre ancora $K.$ Per esempio, gli intervalli $(1/n,1)$ con $n\geq 2$ ricoprono $(0,1),$ ma l'unione di un numero finito di essi è $(1/N,1),$ dove $N$ è l'indice più grande scelto, e lascia scoperti i punti vicini a $0.$

Il teorema di Heine-Borel afferma che un sottoinsieme di $\mathbb{R}$ è compatto se e solo se è chiuso e limitato. Per dimostrare la prima implicazione, sia $K$ compatto e non vuoto. Gli intervalli $(-n,n)$ per $n\geq 1$ ricoprono $K$ e l'unione di un sottoricoprimento finito coincide con l'intervallo di indice massimo, perciò $K$ è limitato. Per mostrare che $K$ è chiuso, fissiamo $y\notin K$ e consideriamo gli aperti:

$$
A_n=\left(-\infty,y-\frac{1}{n}\right)\cup
\left(y+\frac{1}{n},+\infty\right)
\qquad n=1,2,\ldots \tag{7}
$$

Gli insiemi $A_n$ sono crescenti e ricoprono $K,$ perché ogni punto di $K$ ha distanza positiva da $y.$ Un sottoricoprimento finito colloca $K$ interamente in un solo $A_N,$ perciò $I_{1/N}(y)$ è disgiunto da $K.$ Ogni punto del complementare ha dunque un intorno contenuto nel complementare. Anche l'insieme vuoto è compatto, chiuso e limitato.

Per il verso opposto, supponiamo che un ricoprimento aperto di $J_1=[a,b]$ non ammetta un sottoricoprimento finito. Dividendo $J_1$ a metà, almeno uno dei due intervalli chiusi così ottenuti ha la stessa proprietà, altrimenti l'unione dei due sottoricoprimenti finiti ricoprirebbe $J_1.$ Ripetendo la bisezione si ottengono intervalli chiusi annidati $J_n$ di lunghezza $(b-a)/2^{n-1},$ ciascuno privo di sottoricoprimento finito. Per la completezza, l'insieme degli estremi sinistri ha un estremo superiore $c.$ Poiché gli intervalli sono annidati, ogni estremo destro maggiora tutti gli estremi sinistri e dunque $c$ appartiene a ogni $J_n.$ Un aperto $A$ del ricoprimento contiene $c$ e quindi contiene un intorno $I_\varepsilon(c).$ Per $n$ sufficientemente grande, la lunghezza di $J_n$ è minore di $\varepsilon$ e, poiché $c\in J_n,$ si ha:

$$
J_n\subseteq I_\varepsilon(c)\subseteq A \tag{8}
$$

Il solo aperto $A$ ricopre $J_n,$ contro l'ipotesi con cui era stato scelto. Ogni intervallo chiuso e limitato è dunque compatto. Se $K$ è chiuso e limitato, lo si include in un intervallo $[a,b]$ e si aggiunge l'aperto $\mathbb{R}\setminus K$ a un qualunque ricoprimento aperto di $K.$ La famiglia così ottenuta ricopre $[a,b]$ e ammette un sottoricoprimento finito, dal quale basta togliere il complementare di $K$ se è stato scelto.

## Compattezza e successioni

Un insieme $K\subseteq\mathbb{R}$ è compatto se e solo se ogni successione di punti di $K$ ammette una sottosuccessione che converge a un punto di $K.$

Per dimostrare l'equivalenza, supponiamo che $K$ sia compatto. Per il teorema di Heine-Borel, $K$ è chiuso e limitato e ogni successione di punti di $K$ è dunque limitata. Inoltre, per il teorema di Bolzano-Weierstrass, ammette una sottosuccessione convergente. Quindi poiché $K$ è chiuso, il limite appartiene a $K.$

Al contrario, se supponiamo che ogni successione di punti di $K$ ammetta una sottosuccessione che converge a un punto di $K.$ Se $K$ fosse illimitato, potremmo scegliere una successione $(x_n)$ di punti di $K$ con $|x_n|\gt n,$ le cui sottosuccessioni sarebbero tutte illimitate e quindi divergenti. Se $K$ non fosse chiuso, il criterio di chiusura per successioni darebbe una successione di punti di $K$ convergente a un punto fuori da $K,$ e ogni sua sottosuccessione avrebbe lo stesso limite. L'ipotesi implica dunque che $K$ è chiuso e limitato, perciò è compatto per il teorema di Heine-Borel.

L'immagine di un compatto mediante una funzione continua è compatta. Da questa proprietà segue il teorema di Weierstrass, secondo cui una funzione continua a valori reali su un intervallo chiuso, limitato e non vuoto assume il massimo e il minimo.
