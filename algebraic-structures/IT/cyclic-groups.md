---
title: Cyclic Groups
source: https://algebrica.org/cyclic-groups/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - cyclic-group
  - element-order
  - generator
  - group-theory
  - subgroup
---

## Definizione

Un gruppo $G$ si dice ciclico se contiene un elemento $g$ tale che ogni elemento di $G$ si possa scrivere come una potenza intera di $g.$ Ad esempio, nel gruppo $\{1,-1\}$ con la moltiplicazione, le potenze di $g=-1$ danno entrambi gli elementi, perché $(-1)^1=-1$ e $(-1)^2=1.$ Un elemento con questa proprietà si chiama generatore di $G.$ Se indichiamo con $\langle g\rangle$ l'insieme delle potenze intere di $g,$ dire che $g$ genera $G$ equivale a richiedere la seguente uguaglianza:

$$
\begin{align}
G = \langle g\rangle &= \{g^k \mid k \in \mathbb{Z}\} \tag{1}
\end{align}
$$

Nella $(1)$ l'esponente zero dà l'elemento neutro $e,$ mentre gli esponenti negativi danno le potenze dell'inverso di $g.$ Quando l'operazione del gruppo è scritta come addizione, si parla dei multipli interi di $g$ e la $(1)$ si riscrive come:

$$
\begin{align}
G = \langle g\rangle &= \{kg \mid k \in \mathbb{Z}\} \tag{1a}
\end{align}
$$

Per applicare la $(1a),$ riprendiamo l'elemento $-1$ dell'esempio iniziale e vediamo che cosa genera nel gruppo additivo degli interi. Sommando una o più copie di $-1$ si ottengono tutti gli interi negativi. I loro opposti danno tutti gli interi positivi e il multiplo con coefficiente zero dà $0.$ I multipli interi di $-1$ formano dunque tutto $\mathbb{Z}.$ Anche $1$ genera lo stesso gruppo, perché ogni intero $k$ è uguale a $k\cdot 1.$

Per vedere come si presenta la stessa definizione in un gruppo finito, consideriamo le rotazioni attorno al centro di un quadrato dopo le quali la figura si sovrappone esattamente al quadrato iniziale. Per esempio, dopo un quarto di giro in senso antiorario ogni vertice occupa il posto del vertice successivo. Se indichiamo questa rotazione con $r,$ le quattro rotazioni sono:

$$e,r,r^2,r^3$$

Componendo ancora una volta $r^3$ con $r$ si compie un giro intero, quindi $r^4=e$ e le potenze successive ripercorrono le stesse quattro rotazioni. Il gruppo è dunque ciclico. Anche $r^{-1}$ lo genera, percorrendo le rotazioni in senso opposto, mentre $r^2$ genera soltanto il sottogruppo $\{e,r^2\}.$

La possibilità di scrivere tutti gli elementi come potenze di una stessa base permette di dimostrare che ogni gruppo ciclico è abeliano. Infatti, se prendiamo due elementi qualunque $x,y\in G,$ per la $(1)$ possiamo scrivere che $x=g^a$ e $y=g^b$ con $a,b\in\mathbb{Z}.$ La regola del prodotto di potenze con la stessa base riconduce il confronto tra $xy$ e $yx$ a una somma di interi, per cui possiamo scrivere:

$$
\begin{align}
xy &= g^a g^b = g^{a+b} \notag \\[6pt]
   &= g^{b+a} = g^b g^a = yx \tag{2}
\end{align}
$$

Poiché $x$ e $y$ erano arbitrari, la $(2)$ dimostra la proprietà commutativa di $G.$ Per verificare se vale anche il viceversa, consideriamo l'addizione modulo $2$ in ciascuna coordinata per le seguenti coppie:

$$(0,0),(1,0),(0,1),(1,1)$$

L'addizione è commutativa e la somma di ogni coppia con sé stessa è $(0,0).$ I multipli di una coppia assumono quindi al più due valori. Questo gruppo è abeliano, ma nessun elemento genera tutte e quattro le coppie.

## Ordine del generatore e classificazione

Nell'esempio del quadrato, la quarta potenza di $r$ è la prima potenza con esponente positivo che dà l'identità. Vediamo ora come il primo ritorno all'elemento neutro determini la struttura di un gruppo ciclico. Dimostriamo prima che ogni gruppo ciclico infinito è isomorfo al gruppo additivo degli interi e che ogni gruppo ciclico finito di ordine $n$ è isomorfo al gruppo additivo delle classi di resto modulo $n.$ Fissiamo dunque un generatore $g$ e definiamo l'applicazione $\psi\colon\mathbb{Z}\to G$ ponendo $\psi(k)=g^k.$ Per ogni coppia di interi $a,b,$ la regola del prodotto di potenze con la stessa base dà:

$$
\begin{align}
\psi(a+b) &= g^{a+b} = \psi(a)\psi(b) \tag{3}
\end{align}
$$

Per la $(3)$ l'applicazione è un omomorfismo, e per la $(1)$ è una relazione suriettiva. Per stabilire quando sia anche iniettiva, osserviamo che due potenze $g^a$ e $g^b$ coincidono quando $g^{a-b}=e.$ Se nessuna potenza di $g$ con esponente positivo è uguale a $e,$ questo può accadere soltanto per $a=b.$ Infatti, se due esponenti fossero distinti, sottraendo il minore dal maggiore otterremmo un esponente positivo la cui potenza è $e.$ In questo caso si dice che $g$ ha ordine infinito. L'applicazione $\psi$ è quindi biiettiva e dà l'isomorfismo tra $(\mathbb{Z},+)$ e $G.$

Supponiamo invece che esista un esponente positivo per cui la potenza è $e$ e indichiamo con $n$ il minimo di tali esponenti. Questo intero è l'ordine di $g$ e si scrive $n=\mathrm{ord}(g).$ Per capire quali esponenti danno la stessa potenza, dividiamo un intero qualunque $k$ per $n$ e con la seguente relazione $0\leq r\lt n$ scriviamo $k=qn+r.$  Poiché $g^n=e,$ nel calcolo di $g^k$ conta soltanto il resto.

$$
\begin{align}
g^k &= (g^n)^q g^r = g^r \tag{4}
\end{align}
$$

Per la $(4)$ ogni potenza coincide con una tra $e,g,\ldots,g^{n-1}.$ Queste $n$ potenze sono distinte, perché se due coincidessero, la differenza positiva dei loro esponenti sarebbe minore di $n$ e darebbe ancora una potenza uguale a $e.$ Dunque $G$ ha esattamente $n$ elementi. Due esponenti danno la stessa potenza se e solo se hanno lo stesso resto modulo $n,$ come nella seguente relazione:

$$
\begin{align}
g^a=g^b &\iff a\equiv b \pmod n \tag{5}
\end{align}
$$

Per la $(5)$ possiamo associare alla classe di resto $[k]$ la potenza $g^k$ indipendentemente dal rappresentante scelto. A classi distinte corrispondono potenze distinte e, poiché $g$ genera $G,$ in questo modo le otteniamo tutte. La corrispondenza è quindi biiettiva e conserva l'operazione per la $(3).$ Abbiamo così costruito anche nel caso finito l'isomorfismo cercato, da $(\mathbb{Z}/n\mathbb{Z},+)$ a $G$ e questo conclude la dimostrazione della classificazione.

## Ordine di una potenza e scelta dei generatori

Torniamo ora di nuovo alla distinzione emersa nell'esempio del quadrato. Se $g$ genera un gruppo finito di ordine $n,$ come possiamo stabilire quali potenze $g^k$ generano ancora tutto il gruppo? Poiché l'ordine di un elemento coincide con il numero di elementi del sottogruppo che genera, basta determinare l'ordine di $g^k$ e verificare se è uguale a $n.$ Dimostriamo che quest'ordine si ricava dividendo $n$ per il massimo comune divisore di $n$ e $k:$

$$
\begin{align}
\mathrm{ord}(g^k) &= \frac{n}{\gcd(n,k)} \tag{6}
\end{align}
$$

Iniziamo con il cercare il minimo intero positivo $t$ per cui $(g^k)^t=e.$ Poiché $(g^k)^t=g^{kt},$ per la $(5)$ si ha che $t$ deve soddisfare la condizione $n\mid kt.$ Per trovare il primo $t$ che la soddisfa, poniamo $d=\gcd(n,k)$ e scriviamo $n=dn'$ e $k=dk'.$ Dividendo per $d,$ la condizione diventa $n'\mid k't$ e poiché $n'$ e $k'$ sono coprimi, per il lemma di Euclide deve essere $n'\mid t.$ Viceversa, ogni multiplo di $n'$ soddisfa la condizione, quindi il minimo $t$ positivo è $n'=n/d.$ Questo dimostra la $(6).$

Ne segue che $g^k$ genera $G$ se e solo se $\gcd(n,k)=1.$ I generatori sono quindi tanti quante le classi di resto modulo $n$ coprime con $n,$ e il loro numero si indica con $\varphi(n),$ dove $\varphi$ è la funzione di Eulero. Per esempio, nel gruppo additivo $\mathbb{Z}/12\mathbb{Z}$ le classi che generano l'intero gruppo sono $[1],[5],[7]$ e $[11].$ La classe $[8]$ ha invece ordine $12/\gcd(12,8)=3.$ Infatti, aggiungendo ripetutamente $[8]$ a partire da $[0],$ si passa da $[0]$ a $[8],$ poi a $[4]$ e infine di nuovo a $[0].$

Nel caso infinito la scelta dei generatori si legge direttamente sugli esponenti. Infatti, le potenze di $g^k$ hanno per esponenti tutti e soli i multipli di $k.$ Per ottenere anche $g$ occorre quindi che $kt=1$ per qualche intero $t,$ perché a esponenti distinti corrispondono potenze distinte. Ciò accade soltanto per $k=1$ o $k=-1,$ e in entrambi i casi si ottengono tutti gli esponenti interi. I generatori di un gruppo ciclico infinito sono dunque esattamente $g$ e $g^{-1}.$

## Sottogruppi di un gruppo ciclico

Nell'esempio modulo $12$ abbiamo trovato un sottogruppo di ordine $3$ prendendo i multipli di $[8].$ Vediamo ora perché ogni sottogruppo $H$ di un gruppo ciclico $G=\langle g\rangle$ è a sua volta ciclico. Per dimostrarlo, cerchiamo il minimo intero positivo $m$ per cui $g^m\in H.$ Se nessun esponente positivo ha questa proprietà, neppure una potenza con esponente negativo può appartenere a $H,$ perché il suo inverso avrebbe esponente positivo e apparterrebbe ancora a $H.$ In questo caso $H=\{e\}=\langle e\rangle,$ quindi $H$ è ciclico.

Supponiamo ora che tale minimo $m$ esista e prendiamo un elemento qualunque $g^k\in H.$ Vogliamo mostrare che è una potenza di $g^m.$ Dividiamo $k$ per $m$ e scriviamo $k=qm+r,$ con $0\leq r\lt m.$ Dal momento che $g^m$ appartiene a $H,$ anche la sua potenza con esponente $-q$ appartiene a $H.$ Possiamo quindi isolare $g^r$ come prodotto di due elementi di $H,$ ottenendo

$$
\begin{align}
g^k(g^m)^{-q} &= g^{k-qm} = g^r \in H \tag{7}
\end{align}
$$

Se $r$ fosse positivo, la $(7)$ contraddirebbe la scelta di $m$ e dunque $r=0$ e $k$ è un multiplo di $m.$ Questo prova che ogni elemento di $H$ è una potenza di $g^m.$ Viceversa, poiché $g^m$ appartiene a $H,$ tutte le sue potenze appartengono a $H$ perciò si conclude che $H=\langle g^m\rangle,$ completando la dimostrazione.

Se $H$ è un sottogruppo di $\mathbb{Z}$ diverso da $\{0\},$ il suo più piccolo elemento positivo $m$ genera $H.$ I suoi elementi sono quindi tutti e soli i multipli di $m.$ Si ottengono così i sottogruppi $m\mathbb{Z}$ con $m\geq 1,$ ai quali si aggiunge il sottogruppo banale $0\mathbb{Z}=\{0\}.$

Quando $G$ ha ordine finito $n,$ possiamo precisare il risultato dimostrando che per ogni divisore positivo $d$ di $n$ esiste un unico sottogruppo di ordine $d.$ Infatti $g^n=e$ appartiene a ogni sottogruppo $H,$ quindi il minimo $m$ considerato sopra esiste anche per $H=\{e\}.$ Abbiamo appena visto che ogni esponente $k$ per cui $g^k\in H$ è un multiplo di $m.$ Applicando questa conclusione a $k=n,$ otteniamo $m\mid n.$ Per la $(6)$ l'ordine di $H=\langle g^m\rangle$ è allora $n/m.$

Se vogliamo che $H$ abbia ordine $d,$ deve dunque essere $m=n/d.$ Per verificare che questa scelta dia effettivamente un sottogruppo dell'ordine richiesto, applichiamo la $(6)$ a $g^{n/d}$ e teniamo conto che $n/d$ divide $n,$ ottenendo:

$$
\begin{align}
\bigl|\langle g^{n/d}\rangle\bigr| &= \frac{n}{\gcd(n,n/d)} = d \tag{8}
\end{align}
$$

La $(8)$ prova l'esistenza del sottogruppo e la scelta obbligata di $m$ ne prova l'unicità. Per esempio, se consideriamo $\mathbb{Z}/12\mathbb{Z}$ l'unico sottogruppo di ordine $3$ è generato da $[12/3]=[4]$ ed è formato dalle classi $[0],[4],[8]$ e in questo modo ritroviamo il sottogruppo generato da $[8]$ nella sezione precedente.
