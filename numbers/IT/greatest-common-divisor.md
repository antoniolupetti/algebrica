---
title: Greatest Common Divisor
source: https://algebrica.org/greatest-common-divisor/
license: CC BY-NC 4.0
tags:
  - bezout-identity
  - coprime-integers
  - divisibility
  - euclidean-algorithm
  - euclidean-division
  - greatest-common-divisor
  - integers
---

## Definizione

Il massimo comune divisore di due interi $m$ e $n,$ non entrambi nulli, che indichiamo come $\gcd(m,n),$ è il più grande dei loro divisori comuni positivi. L'insieme di questi divisori contiene $1$ ed è finito, perché ogni suo elemento è al più uguale al valore assoluto di uno degli interi non nulli della coppia dei numeri considerati. Per caratterizzarlo mediante la divisibilità, cerchiamo un intero positivo $d$ che soddisfi le condizioni:

$$
\tag{1}
\begin{align}
&d\mid m \\[6pt]
&d\mid n \\[6pt]
&(c\mid m \ \text{e}\ c\mid n)\ \Longrightarrow\ c\mid d
\end{align}
$$

Quando $d$ soddisfa la $(1),$ allora si ha che ogni divisore comune positivo è un divisore di $d$ ed è quindi minore o uguale a $d.$ Da questo segue che:

$$d=\gcd(m,n)$$

Se uno dei due interi è zero, i divisori comuni sono quelli dell'altro intero poiché ogni intero divide zero. In particolare vale:

$$\gcd(m,0)=|m| \quad \forall \ m\neq0 \tag{2}$$

L'algoritmo di Euclide è un algoritmo ricorsivo che permette di calcolare il massimo comune divisore di due interi mediante divisioni euclidee. Se entrambi gli interi sono non nulli, prendiamo i loro valori assoluti e li ordiniamo come $a\geq b>0.$ Il primo passo dell'algoritmo consiste nella divisione euclidea di $a$ per $b:$

$$
a=qb+r,\qquad 0\leq r<b
\tag{3}
$$

Per la $(3),$ ogni divisore comune di $a$ e $b$ divide anche $r=a-qb$ e, viceversa, ogni divisore comune di $b$ e $r$ divide anche $a=qb+r.$ Le coppie $(a,b)$ e $(b,r)$ hanno quindi gli stessi divisori comuni, da cui segue l'identità:

$$
\gcd(a,b)=\gcd(b,r)
\tag{4}
$$

Ripetiamo la divisione secondo la $(4)$ finché il resto è zero, il che avviene perché i resti positivi diminuiscono a ogni passo, e il divisore dell'ultima divisione è il massimo comune divisore dei due interi iniziali. Come esempio proviamo a calcolare il massimo comune divisore di $252$ e $198$ e otteniamo:

$$
\tag{5}
\begin{align}
252 &= 1\cdot198+54 \\[6pt]
198 &= 3\cdot54+36 \\[6pt]
54 &= 1\cdot36+18 \\[6pt]
36 &= 2\cdot18+0
\end{align}
$$

Nell'ultima riga della $(5)$ il resto è zero e quindi $\gcd(252,198)=18.$

- - -

I calcoli si complicano quando si prova ad estendere il calcolo del massimo comune divisore a più interi di una lista $a_1,\ldots,a_k.$ In questo caso si procede calcolando il massimo comune divisore tra il risultato del passo precedente e l'intero successivo della lista. Per chiarire il concetto, partiamo da $d_1=|a_1|$ e per ogni $j=2,\ldots,k$ calcoliamo:

$$
d_j=\gcd(d_{j-1},a_j)
\tag{10}
$$

I divisori di $d_1$ coincidono con quelli di $a_1.$ Se i divisori di $d_{j-1}$ sono i divisori comuni dei primi $j-1$ interi, per la $(1)$ e la $(10)$ i divisori di $d_j$ sono quelli che dividono anche $a_j.$ Per induzione, i divisori di $d_k$ sono quindi i divisori comuni a tutta la lista e $d_k=\gcd(a_1,\ldots,a_k).$

Il valore di $d_k$ permette di stabilire se gli interi della lista sono coprimi nel loro insieme e questo accade se $d_k=1.$ In particolare, come vedremo nel paragrafo successivo, due interi $a$ e $b,$ non entrambi nulli, sono coprimi se il loro unico divisore comune è $1.$ Per la coprimalità a due a due, invece, il massimo comune divisore deve essere $1$ per ogni coppia. Consideriamo ad esempio gli interi $6,10,15.$ Nessuna coppia è coprima, perché vale:

$$
\begin{align}
\gcd(6,10) &= 2 \\[6pt]
\gcd(6,15) &= 3 \\[6pt]
\gcd(10,15) &= 5
\end{align}
$$

Poiché $\gcd(6,10)=2,$ il massimo comune divisore dei tre numeri è $\gcd(2,15)=1,$ perciò i tre interi sono coprimi.

## Identità di Bézout e interi coprimi

L'identità di Bézout esprime il massimo comune divisore come combinazione lineare a coefficienti interi dei due numeri di partenza. In termini formali, per ogni coppia di interi $m$ e $n,$ non entrambi nulli, esistono due interi $s$ e $t$ tali che vale la seguente identità:

$$
sm+tn=\gcd(m,n)
\tag{6}
$$

Per trovare i coefficienti della $(6)$ facciamo un esempio considerando due interi, $252$ e $198,$ e ripercorrendo a ritroso le divisioni della $(5).$ Partiamo dall'ultimo resto positivo, $18.$ La terza riga dà $18=54-36.$ Sostituiamo quindi $36$ con l'espressione ricavata dalla seconda riga e $54$ con quella ricavata dalla prima ottenendo:

$$
\tag{7}
\begin{align}
18 &= 54-36 \\[6pt]
   &= 54-(198-3\cdot54) \\[6pt]
   &= 4\cdot54-198 \\[6pt]
   &= 4(252-198)-198 \\[6pt]
   &= 4\cdot252-5\cdot198
\end{align}
$$

La $(7)$ fornisce quindi i coefficienti $s=4$ e $t=-5$ per la coppia $(252,198).$ In generale, la $(3)$ permette di risalire allo stesso modo fino a esprimere il MCD in funzione di $|m|$ e $|n|.$ Se il MCD coincide già con uno dei due valori assoluti, bastano i coefficienti $1$ per quel termine e $0$ per l'altro. Per passare da $|m|$ e $|n|$ a $m$ e $n,$ si cambia il segno del coefficiente di ciascun intero negativo.

Una volta espresso il massimo comune divisore $d=\gcd(m,n)$ come combinazione lineare di $m$ e $n,$ possiamo ottenere anche tutti i suoi multipli, semplicemente moltiplicando entrambi i membri della $(6)$ per un intero $k$ per ottenere una forma del tipo:

$$kd=(ks)m+(kt)n$$

D'altra parte, ogni combinazione lineare intera di $m$ e $n$ è un multiplo di $d,$ perché $d$ divide entrambi. Le combinazioni lineari intere di $m$ e $n$ sono quindi esattamente i multipli di $d$ per cui possiamo scrivere:

$$
\{\ sm+tn\mid s,t\in\mathbb{Z}\ \}=d\mathbb{Z}
\tag{8}
$$

La $(8)$ fornisce una caratterizzazione degli interi coprimi. Due interi $a$ e $b,$ non entrambi nulli, sono coprimi se e solo se esistono interi $s$ e $t$ tali che:

$$sa+tb=1$$

Se $a$ e $b$ sono coprimi e dividono entrambi un intero $x,$ anche il loro prodotto divide $x.$ Infatti, possiamo scrivere $x=a\alpha=b\beta$ con $\alpha,\beta\in\mathbb{Z}.$ Moltiplicando $sa+tb=1$ per $x$ e sostituendo $x=b\beta$ nel primo termine e $x=a\alpha$ nel secondo si ottiene la seguente identità che esprime $x$ come multiplo intero di $ab:$

$$
x=sax+tbx=ab(s\beta+t\alpha)
\tag{9}
$$
