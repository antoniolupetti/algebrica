---
title: Euclidean Division
source: https://algebrica.org/euclidean-division/
license: CC BY-NC 4.0
tags:
  - divisibility
  - division-algorithm
  - euclidean-algorithm
  - euclidean-division
  - greatest-common-divisor
  - integers
  - quotient
  - remainder
  - well-ordering
---

## Teorema della divisione euclidea

La divisione euclidea consente di esprimere un numero intero come somma di un multiplo del divisore e di un resto. Nello specifico, il relativo teorema afferma che fissati due interi $a$ e $d,$ con $d>0,$ esiste un'unica coppia di interi $(q,r)$ che soddisfa le condizioni:

$$ \tag{1}
\begin{align}
a&=dq+r \\[6pt]
0&\leq r<d
\end{align}
$$

Il numero $a$ è il dividendo, $d$ è il divisore, $q$ è il quoziente e $r$ è il resto. Poiché $r$ è intero, può assumere soltanto valori compresi tra $0$ e $d-1,$ mentre il dividendo e il quoziente possono anche essere negativi. Ad esempio, per dividere $23$ per $5,$ cerchiamo il più grande multiplo di $5$ che non superi il dividendo. Poiché $20=5\cdot4$ non supera $23,$ mentre il multiplo successivo $25=5\cdot5$ lo supera, possiamo scrivere:

$$
5\cdot4\leq23<5\cdot5
$$

Il quoziente è quindi $4$ e il resto è la differenza $23-20=3,$ per cui la divisione si scrive per la prima condizione della $(1)$ come:

$$
23=5\cdot4+3 \tag{2}
$$

Per la seconda relazione della $(1)$ si ha che $0\leq3<5,$ e quindi la coppia $(4,3)$ soddisfa entrambe le condizioni della divisione euclidea. Per chiarire meglio il concetto anche $23=5\cdot3+8$ sarebbe un'uguaglianza corretta, ma poiché il resto $8$ supera il divisore, non rispetta il vincolo $0\leq r<d$ e quindi la $(1)$ non è soddisfatta nel suo insieme.

Il quoziente $4$ e il resto $3$ della $(2)$ permettono di esprimere il rapporto $23/5$ come somma di un intero e di una frazione. In generale, dividendo per $d$ entrambi i membri della prima relazione della $(1),$ otteniamo:

$$
\frac{a}{d}=q+\frac{r}{d} \tag{3}
$$

Nell'esempio, al quoziente $4$ va quindi aggiunta la frazione $3/5$ corrispondente al resto, così da ottenere $23/5=4+3/5.$ Il quoziente intero $q$ e il rapporto $a/d$ coincidono se e solo se $r=0,$ perché la frazione $r/d$ è nulla esattamente in questo caso.

Una divisione si dice esatta quando il resto è zero, condizione che equivale a dire che il dividendo è un multiplo del divisore. In questo caso $d$ divide $a,$ relazione indicata con $d\mid a.$

- - -

La dimostrazione del teorema procede in due passaggi. Nel primo mostriamo che esiste almeno una coppia di interi $(q,r)$ che soddisfa entrambe le condizioni della $(1)$ e nel secondo proviamo che questa coppia è unica. Per prima cosa costruiamo il quoziente come il più grande intero il cui prodotto con $d$ non supera $a.$ Per farlo, consideriamo il seguente insieme:

$$
A=\{\ k\in\mathbb{Z}\mid kd\leq a\ \} \tag{4}
$$

L'insieme $A$ non è vuoto perché contiene l'intero $k=-|a|,$ per il quale la condizione $d\geq1$ dà:

$$
-|a|d\leq-|a|\leq a
$$

Inoltre, $A$ è limitato superiormente dall'intero $M=\max\{\ a,0\ \}.$ Infatti, se $k\leq0,$ allora $k\leq M,$ mentre se $k>0$ e $k\in A,$ dalla disuguaglianza $d\geq1$ segue $k\leq kd\leq a\leq M.$

Poiché $M$ è un maggiorante di $A,$ le differenze $M-k$ sono interi non negativi per ogni $k\in A$ che diminuiscono all'aumentare di $k,$ quindi possiamo individuare il massimo di $A$ cercando il minimo dell'insieme:

$$
B=\{\ M-k\mid k\in A\ \}
$$

Poiché $A$ è non vuoto, anche $B$ lo è e ammette un minimo $m$ a cui corrisponde l'intero $q=M-m,$ che appartiene ad $A$ ed è il suo massimo, perché $m\leq M-k$ implica $k\leq q$ per ogni $k\in A.$

Poiché $q\in A,$ dalla $(4)$ segue che $qd\leq a.$ Il numero $q+1$ non appartiene invece ad $A,$ altrimenti $q$ non sarebbe il massimo, quindi la disuguaglianza $(q+1)d\leq a$ non può valere e deve essere $(q+1)d>a.$ Riunendo queste due disuguaglianze otteniamo:

$$ \tag{5}
qd\leq a<(q+1)d
$$

Poniamo $r=a-qd,$ che è un intero perché $a,q,d$ sono interi. La definizione di $r$ dà $a=dq+r,$ e sottraendo $qd$ dai tre membri della $(5)$ otteniamo anche $0\leq r<d,$ come richiesto.

Dimostriamo adesso l'unicità del quoziente e del resto, supponendo che due coppie di interi $(q,r)$ e $(q',r')$ soddisfino entrambe le condizioni della $(1)$ e verificando che coincidono. Dalla prima condizione otteniamo:

$$
a=dq+r=dq'+r' \tag{6}
$$

Entrambi i resti della $(6)$ appartengono all'intervallo da $0$ a $d-1.$ Ordinando i termini otteniamo:

$$ \tag{7}
d(q-q')=r'-r
$$

Poiché $r'\geq0$ e $r<d,$ si ha $r'-r\geq-r>-d.$ Inoltre, da $r\geq0$ e $r'<d$ segue $r'-r\leq r'<d$ e riunendo le due disuguaglianze otteniamo:

$$
-d<r'-r<d \tag{8}
$$

Il membro di sinistra della $(7)$ è un multiplo intero di $d,$ e l'unico multiplo di $d$ strettamente compreso tra $-d$ e $d$ è zero. Infatti, se l'intero $q-q'$ fosse diverso da zero, il suo valore assoluto sarebbe almeno $1,$ e avremmo:

$$
|d(q-q')|=d|q-q'|\geq d \tag{9}
$$

Ma la $(9)$ non è compatibile con la $(8),$ quindi $q=q'.$ Sostituendo $q'=q$ nella $(6)$ otteniamo $dq+r=dq+r',$ da cui, sottraendo $dq$ da entrambi i membri, segue $r=r'.$ Le due coppie di numeri quindi coincidono e anche l'unicità è dimostrata. Abbiamo in questo modo dimostrato entrambe le affermazioni del teorema, ossia l'esistenza e l'unicità della coppia di interi $(q,r)$ che soddisfa le condizioni della $(1).$

## Applicazione con un dividendo negativo

Anche quando il dividendo è negativo, il resto deve soddisfare la condizione $0\leq r<d$ della $(1).$ Per esempio, per dividere $-23$ per $5$ dobbiamo cercare due multipli consecutivi di $5$ tra cui si trova il dividendo. In questo caso valgono le disuguaglianze:

$$
5\cdot(-5)=-25\leq-23<-20=5\cdot(-4)
$$

Il quoziente è dunque $-5$ e il resto è la distanza da $-25$ a $-23,$ cioè $-23-(-25)=2,$ per cui la divisione cercata che esprime la prima condizione della $(1)$ è:

$$
-23=5\cdot(-5)+2
$$

La divisione di $-23$ per $5$ appena ottenuta si può ricavare anche dalla divisione $23=5\cdot4+3.$ In generale, se $a>0$ e $a=dq+r,$ con $0<r<d,$ cambiando segno otteniamo $-a=d(-q)-r.$ Il termine $-r$ è negativo e non può essere il resto richiesto. Per renderlo positivo, aggiungiamo $d$ a $-r$ e sottraiamo $d$ dal multiplo $d(-q),$ ottenendo:

$$
-a=d(-q-1)+(d-r)
$$

Poiché $0<d-r<d,$ il nuovo quoziente è $-q-1$ e il nuovo resto è $d-r.$ Dalla divisione $23=5\cdot4+3$ ricaviamo così che $-23=5\cdot(-5)+2.$ Quando invece $r=0,$ il cambio di segno cambia soltanto il segno del quoziente. Per esempio, da $25=5\cdot5$ abbiamo che:

$$
-25=5\cdot(-5)+0
$$

La divisione di $-25$ per $5$ ha quindi quoziente $-5$ e resto $0$ e, in questo caso, la formula con resto $d-r$ non va applicata perché produrrebbe il valore escluso $d.$

## Algoritmo di Euclide

L'algoritmo di Euclide è un algoritmo ricorsivo che consente di calcolare il massimo comun divisore di due interi positivi applicando ripetutamente la divisione euclidea. Supponiamo che $a$ e $d$ siano due interi positivi e che $a\geq d,$ per cui vale la $(1).$ Le coppie $(a,d)$ e $(d,r)$ hanno gli stessi divisori comuni, perché ogni intero che divide $a$ e $d$ divide anche $r=a-dq$ e, viceversa, ogni intero che divide $d$ e $r$ divide anche $a=dq+r.$ Possiamo quindi sostituire il dividendo con il divisore e il divisore con il resto senza modificare il massimo comune divisore ottenendo:

$$
\gcd(a,d)=\gcd(d,r)
$$

Se $r=0,$ la divisione è esatta e il massimo comune divisore è $d.$ Quando invece $r\gt 0$ dividiamo $d$ per $r$ e ripetiamo lo stesso calcolo con il nuovo resto. Procediamo finché non otteniamo un resto pari a zero, e quando lo abbiamo trovato, il divisore dell'ultima divisione è il massimo comune divisore dei numeri iniziali.

Per esempio, calcoliamo il $\gcd(252,198)$ procedendo come segue:

$$
\begin{align}
252&=198\cdot1+54 \\[6pt]
198&=54\cdot3+36 \\[6pt]
54&=36\cdot1+18 \\[6pt]
36&=18\cdot2+0
\end{align}
$$

L'ultima divisione ha resto zero per cui il suo divisore il il massimo comun divisore tra $252$ e $198.$
