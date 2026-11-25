---
title: Symmetric Group
source: https://algebrica.org/symmetric-group/
license: CC BY-NC 4.0
tags:
  - algebraic-structures
  - alternating-group
  - cycle-notation
  - group-theory
  - parity-of-permutations
  - permutation
  - sign-homomorphism
  - symmetric-group
  - transposition
---

## Definizione

Consideriamo l'insieme $X_n = \{1, 2, \ldots, n\},$ con $n \geq 1,$ e definiamo gruppo simmetrico $S_n$ un gruppo che ha per elementi tutte le permutazioni di $X_n$ e per operazione la loro composizione. Poiché una permutazione è una biiezione di $X_n$ in sé, sia il prodotto di due permutazioni sia l'inversa di ciascuna sono ancora permutazioni di $X_n.$ La composizione è un'operazione associativa e ha per elemento neutro l'identità di $X_n.$

Per contare gli elementi di $S_n,$ possiamo scrivere ogni permutazione di $X_n$ in questo modo:

$$
\begin{align}
\sigma &= \begin{pmatrix}
1 & 2 & \cdots & n \\[6pt]
\sigma(1) & \sigma(2) & \cdots & \sigma(n)
\end{pmatrix} \tag{1}
\end{align}
$$

Nella $(1)$ la seconda riga determina la permutazione e può contenere gli $n$ elementi in qualsiasi ordine. Per $\sigma(1)$ abbiamo $n$ scelte, per $\sigma(2)$ ne restano $n-1$ e così via fino all'ultima immagine, che è obbligata. L'ordine di $S_n$ è quindi il fattoriale di $n:$

$$
\begin{align}
|S_n| &= n(n-1)\cdots 1 = n! \tag{2}
\end{align}
$$

Per la $(2)$ i gruppi $S_1$ e $S_2$ hanno rispettivamente uno e due elementi e in entrambi la composizione è commutativa, perché c'è al più un elemento diverso dall'identità. Facciamo un esempio per verificare se la stessa proprietà vale in $S_3,$ confrontando i due ordini di composizione delle seguenti permutazioni, scritte come nella $(1):$

$$
\begin{align}
\sigma &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 3 & 1 \end{pmatrix} \tag{3a} \\[6pt]
\tau &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 2 & 1 & 3 \end{pmatrix} \tag{3b}
\end{align}
$$

Componendo le permutazioni $(3a)$ e $(3b)$ nei due ordini, otteniamo $(\sigma \circ \tau)(1) = \sigma(2) = 3$ e $(\tau \circ \sigma)(1) = \tau(2) = 1.$ Calcolando allo stesso modo le immagini di $2$ e di $3$ si ottengono i due prodotti per esteso:

$$
\begin{align}
\sigma \circ \tau &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 3 & 2 & 1 \end{pmatrix} \tag{4a} \\[6pt]
\tau \circ \sigma &= \begin{pmatrix} 1 & 2 & 3 \\[6pt] 1 & 3 & 2 \end{pmatrix} \tag{4b}
\end{align}
$$

Poiché i due prodotti hanno immagini diverse in $1,$ le permutazioni $\sigma$ e $\tau$ non commutano. Dunque $S_3$ non è abeliano. Per $n \gt 3$ lo stesso controesempio si estende a $S_n$ lasciando fissi gli elementi da $4$ a $n,$ quindi $S_n$ non è abeliano per ogni $n \geq 3.$

## Notazione ciclica e ordine di una permutazione

La notazione ciclica è un modo di rappresentare una permutazione mediante dei cicli. Per scrivere un ciclo si sceglie un elemento e si elencano gli elementi che si incontrano prima di tornare al punto di partenza. Per esempio, nella $(3a)$ possiamo scrivere $\sigma = (1\ 2\ 3)$ in quanto le immagini successive di $1$ danno il seguente percorso:

$$1 \mapsto 2 \mapsto 3 \mapsto 1$$

In generale, dati $k$ elementi distinti di $X_n,$ un ciclo $(a_1\ a_2\ \cdots\ a_k)$ manda ciascun elemento dell'elenco nel successivo e l'ultimo nel primo, lasciando fissi tutti gli altri. La lunghezza del ciclo è $k.$ Ciascuno dei suoi elementi può essere scelto come punto di partenza, perciò le seguenti scritture indicano lo stesso ciclo:

$$
\begin{align}
\sigma &= (1\ 2\ 3) \notag \\[6pt]
       &= (2\ 3\ 1) \notag \\[6pt]
       &= (3\ 1\ 2) \notag
\end{align}
$$

Una trasposizione è un ciclo di lunghezza $2$ che scambia due elementi. Nella $(3b)$ la permutazione $\tau$ scambia $1$ e $2$ e lascia fisso $3,$ quindi si scrive $(1\ 2).$ Anche i due prodotti sono trasposizioni, perché $\sigma \circ \tau$ scambia $1$ e $3$ nella $(4a),$ mentre $\tau \circ \sigma$ scambia $2$ e $3$ nella $(4b).$

$$
\begin{align}
\sigma &= (1\ 2\ 3) & \tau &= (1\ 2) \tag{6a} \\[6pt]
\sigma \circ \tau &= (1\ 3) & \tau \circ \sigma &= (2\ 3) \tag{6b}
\end{align}
$$

Per una permutazione qualsiasi $\pi \in S_n,$ le immagini successive di un elemento tornano al punto di partenza perché $X_n$ è finito e $\pi$ è iniettiva. Una volta chiuso un ciclo, si riparte da un elemento che non vi compare e si prosegue fino a esaurire $X_n.$ Si ottengono così cicli disgiunti, il cui prodotto coincide con $\pi$ perché ne riproduce l'azione su ogni elemento. La scomposizione in cicli disgiunti è dunque unica a meno dell'ordine dei fattori, che commutano perché ciascuno lascia fissi gli elementi mossi dagli altri. Nella seguente permutazione di $X_6$ possiamo quindi scrivere le due trasposizioni in entrambi gli ordini:

$$
\begin{align}
\rho &= \begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6 \\[6pt]
3 & 5 & 1 & 4 & 2 & 6
\end{pmatrix} \notag \\[6pt]
&= (1\ 3)(2\ 5) = (2\ 5)(1\ 3) \tag{7}
\end{align}
$$

Nella forma ciclica della $(7)$ si omettono per convenzione i cicli di lunghezza $1,$ in questo caso $(4)$ e $(6).$

- - -

Nella $(2)$ abbiamo calcolato l'ordine di $S_n$ contando le sue permutazioni. In generale, l'ordine di una singola permutazione $\sigma \in S_n$ è il minimo intero $j \geq 1$ per cui $\sigma^j$ è l'identità. Per trovare questo minimo, dobbiamo stabilire dopo quante applicazioni di $\sigma$ tutti gli elementi tornano al punto di partenza. In un ciclo di lunghezza $k$ ciascun elemento avanza di una posizione a ogni applicazione, quindi dopo $j$ passi si ritrova nella posizione iniziale se e solo se $k$ divide $j.$ Se i cicli disgiunti di $\sigma$ hanno lunghezze $k_1, \ldots, k_m,$ il primo esponente per cui tutti gli elementi tornano simultaneamente al punto di partenza è il minimo comune multiplo delle lunghezze:

$$
\begin{align}
\mathrm{ord}(\sigma) &= \mathrm{mcm}(k_1, \ldots, k_m) \tag{8}
\end{align}
$$

Applicando la $(8)$ alla permutazione $(1\ 2)(3\ 4\ 5) \in S_5$ otteniamo:

$$
\begin{align}
\mathrm{ord}\bigl((1\ 2)(3\ 4\ 5)\bigr) &= \mathrm{mcm}(2,3) = 6 \tag{8a}
\end{align}
$$

In sei passi il primo ciclo compie tre giri e il secondo due.

## Segno di una permutazione e gruppo alterno

La permutazione $(1\ 2)(3\ 4\ 5)$ della $(8a)$ si può scrivere come $(1\ 2)(3\ 5)(3\ 4).$ È possibile scriverla anche come prodotto di un numero pari di trasposizioni? Per rispondere, partiamo dalla scomposizione di un ciclo di lunghezza $k \geq 2$ in $k-1$ trasposizioni, ottenendo:

$$
\begin{align}
(a_1\ a_2\ \cdots\ a_k) &= (a_1\ a_k) \cdots (a_1\ a_2) \tag{9}
\end{align}
$$

Per calcolare la parità, indichiamo con $c(\pi)$ il numero dei cicli disgiunti di $\pi,$ compresi quelli di lunghezza $1.$ Nel prodotto $\pi \circ (a\ b)$ le immagini di $a$ e $b$ si scambiano. Se i due elementi appartengono a cicli distinti, questi si uniscono, mentre se appartengono allo stesso ciclo, questo si divide in due. Il numero dei cicli cambia dunque parità a ogni passo. Poiché l'identità ha $n$ cicli, per ogni prodotto $\sigma$ di $m$ trasposizioni vale:

$$
\begin{align}
m &\equiv n-c(\sigma) \pmod{2} \tag{10}
\end{align}
$$

Per la $(10)$ la parità di $m$ dipende solo da $\sigma,$ quindi possiamo definire il segno di $\sigma$ ponendo $\mathrm{sgn}(\sigma)=(-1)^m$ in modo che una permutazione è pari se ha segno $1$ e dispari se il segno è $-1.$ Per la permutazione della $(8a)$ ogni scomposizione in trasposizioni ha dunque un numero dispari di fattori, mentre per la $(9)$ un ciclo di lunghezza $k$ ha segno $(-1)^{k-1}.$

Se $\sigma$ e $\tau$ sono prodotti rispettivamente di $p$ e $q$ trasposizioni, le loro scomposizioni danno $p+q$ fattori per $\sigma \circ \tau$ e ne segue che la funzione segno $\mathrm{sgn}$ è un omomorfismo:

$$
\begin{align}
\mathrm{sgn}(\sigma \circ \tau) &= (-1)^{p+q} \notag \\[6pt]
&= \mathrm{sgn}(\sigma)\mathrm{sgn}(\tau) \tag{11}
\end{align}
$$

Per $n \geq 2$ questo omomorfismo che va da $S_n$ al gruppo moltiplicativo $\{1,-1\}$ è suriettivo, perché l'identità ha segno $1$ e una trasposizione ha segno $-1.$

- - -

Vediamo ora cos'è il gruppo alterno $A_n,$ che è sostanzialmente un gruppo formato dalle permutazioni pari di $S_n.$ Poiché sono proprio quelle che l'omomorfismo segno della $(11)$ manda in $1,$ il gruppo alterno è il suo nucleo e quindi è un sottogruppo normale di $S_n.$ Quando $n \geq 2,$ fissiamo la trasposizione $\tau = (1\ 2).$ Per ogni $\sigma \in S_n,$ il prodotto $\tau \circ \sigma$ ha segno opposto a quello di $\sigma,$ perché nella $(11)$ il fattore $\mathrm{sgn}(\tau)$ vale $-1.$ Componendo di nuovo a sinistra con $\tau$ si riottiene $\sigma.$ Le permutazioni dispari formano dunque il laterale $\tau A_n$ e sono tante quante le pari. Questo laterale non è un sottogruppo, perché l'identità è pari. Poiché $A_n$ e $\tau A_n$ esauriscono $S_n,$ dalla $(2)$ otteniamo:

$$
\begin{align}
[S_n : A_n] &= 2 \tag{12a} \\[6pt]
|A_n| &= \frac{|S_n|}{2} = \frac{n!}{2} \tag{12b}
\end{align}
$$

Per la $(12b)$ il gruppo $A_3$ ha ordine $3.$ Il ciclo $(1\ 2\ 3)$ della $(6a)$ è pari e ha ordine $3,$ quindi genera tutto $A_3:$

$$
\begin{align}
A_3 &= \langle (1\ 2\ 3) \rangle = \{\mathrm{id}, (1\ 2\ 3), (1\ 3\ 2)\} \tag{13}
\end{align}
$$

## Coniugio e tipo ciclico

Fissata una permutazione $\pi \in S_n,$ si definisce coniugio mediante $\pi$ l'applicazione che a ogni $\sigma \in S_n$ associa la seguente permutazione:

$$\pi\sigma\pi^{-1} \tag{14}$$

Due permutazioni $\sigma$ e $\tau$ si dicono coniugate in $S_n$ se esiste $\pi \in S_n$ tale che valga la seguente relazione:

$$\tau = \pi\sigma\pi^{-1} \tag{15}$$

Se $\sigma(a)=b,$ otteniamo quindi $\tau(\pi(a))=\pi(\sigma(a))=\pi(b).$ In un ciclo $c=(a_1\ a_2\ \cdots\ a_k)$ il coniugio sostituisce dunque ogni etichetta $a_i$ con $\pi(a_i),$ come mostra la $(14a).$

$$
\begin{align}
\pi c\pi^{-1} &= (\pi(a_1)\ \pi(a_2)\ \cdots\ \pi(a_k)) \tag{14a} \\[6pt]
(2\ 3)(1\ 2\ 3)(2\ 3) &= (1\ 3\ 2) \tag{14b}
\end{align}
$$

Introduciamo ora il tipo ciclico, che rappresenta l'elenco delle lunghezze dei cicli disgiunti in ordine decrescente, contando i punti fissi come cicli di lunghezza $1.$ Per la $(14a)$ il coniugio conserva il tipo ciclico. Viceversa, se due permutazioni hanno lo stesso tipo, abbiniamo i cicli di uguale lunghezza, compresi i punti fissi. Scelto un punto di partenza in ciascun ciclo, mandiamo i suoi elementi, nell'ordine, in quelli del ciclo abbinato. Queste corrispondenze definiscono su tutto $X_n$ una permutazione $\pi$ che, per la $(14a),$ coniuga la prima permutazione nella seconda.

Le classi di coniugio di $S_n$ corrispondono quindi alle partizioni di $n,$ poiché le lunghezze dei cicli sommano a $n$ e ogni partizione si realizza con cicli disgiunti di quelle lunghezze. In $S_4$ le cinque classi contengono in tutto $24$ permutazioni.

| Tipo ciclico | Permutazioni | Numero |
| --- | --- | ---: |
| $(4)$ | Cicli di lunghezza $4$ | $6$ |
| $(3,1)$ | Cicli di lunghezza $3$ | $8$ |
| $(2,2)$ | Prodotti di due trasposizioni disgiunte | $3$ |
| $(2,1,1)$ | Trasposizioni | $6$ |
| $(1,1,1,1)$ | Identità | $1$ |

Per la $(8)$ le permutazioni $(1\ 2)$ e $(1\ 2)(3\ 4)$ di $S_4$ hanno entrambe ordine $2.$ I loro tipi ciclici sono rispettivamente $(2,1,1)$ e $(2,2),$ quindi le due permutazioni non sono coniugate.