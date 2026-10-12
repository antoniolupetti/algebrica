---
title: Chinese Remainder Theorem
source: https://algebrica.org/chinese-remainder-theorem/
license: CC BY-NC 4.0
tags:
  - bezout-identity
  - chinese-remainder-theorem
  - congruence
  - coprime-integers
  - greatest-common-divisor
  - least-common-multiple
  - modular-arithmetic
  - multiplicative-inverse
  - residue-class
  - ring-isomorphism
  - systems-of-congruences
---

## Enunciato e dimostrazione

Il teorema cinese del resto garantisce la possibilità di ricostruire un numero intero a partire dai resti delle sue divisioni per più interi positivi, detti moduli. Quando questi moduli sono coprimi a due a due, cioè ogni coppia di moduli distinti ha massimo comune divisore uguale a $1$, il teorema assicura che qualsiasi scelta dei resti è realizzata da un intero e che tutti gli interi con quei resti differiscono per un multiplo del prodotto dei moduli. Prima di enunciare il teorema, è utile introdurre il concetto di congruenza: due interi $a$ e $b$ si dicono congruenti modulo $n$ se hanno lo stesso resto nella divisione per $n$ e si scrive 

$$a\equiv b\pmod n \tag{1}$$

Ad esempio, $8\equiv5\pmod3,$ perché $8=2\cdot3+2$ e $5=1\cdot3+2,$ quindi entrambi hanno resto $2$ nella divisione per $3.$ Quindi, per assegnare i resti di uno stesso intero rispetto a più moduli, scriviamo per ciascun modulo una congruenza della forma $(1).$ Possiamo allora riunire queste condizioni in un sistema di congruenze, perché cerchiamo un intero che le soddisfi tutte. Per esempio, assegnando resto $2$ nella divisione per $3$ e resto $3$ nella divisione per $5,$ otteniamo il sistema:

$$ \tag{2}
\begin{cases}
x \equiv 2 \pmod 3 \\[6pt]
x \equiv 3 \pmod 5
\end{cases}
$$

Il numero $8$ soddisfa entrambe le congruenze, perché $8=2\cdot3+2$ e $8=1\cdot5+3,$ e più in generale, lo stesso vale per ogni intero della forma $8+15q,$ con $q\in\mathbb{Z}.$ Poiché $3$ e $5$ sono coprimi, come abbiamo detto poc'anzi, il teorema cinese del resto assicura che gli interi $8+15q$ sono tutte e sole le soluzioni del sistema. Vedremo più avanti i vari passaggi della soluzione. Per ora vi basti intuitivamente capire il processo. Passiamo quindi ad enunciare formalmente il problema, considerando $m$ e $n$ due interi maggiori di $1,$ con $\gcd(m,n)=1.$ Fissati due interi arbitrari $a$ e $b,$ consideriamo dunque il sistema che generalizza la $(2)$:

$$ \tag{3}
\begin{cases}
x \equiv a \pmod m \\[6pt]
x \equiv b \pmod n
\end{cases}
$$

Sotto queste condizioni, il teorema cinese del resto afferma che il sistema $(3)$ ammette esattamente una soluzione $x_0$ tra gli interi da $0$ a $mn-1.$ Tutte e sole le soluzioni del sistema si ottengono aggiungendo a $x_0$ un multiplo intero di $mn,$ secondo la formula:

$$
x=x_0+qmn \qquad q\in\mathbb{Z} \tag{4}
$$

Le soluzioni intere sono infinite, ma hanno tutte lo stesso resto $x_0$ nella divisione per $mn.$ Si dice perciò che la soluzione è unica modulo $mn.$

- - -

La dimostrazione del teorema si divide in due parti. Per prima cosa si dimostra che il sistema $(3)$ ammette almeno una soluzione e poi si dimostra che tutte le soluzioni hanno lo stesso resto nella divisione per $mn.$ Nel primo caso si prova a costruirne una usando l'identità di Bézout, secondo la quale dati due interi positivi $m$ e $n,$ esistono due interi $s$ e $t$ tali che vale la seguente relazione:

$$
sm+tn=\gcd(m,n) \tag{5}
$$

Per le ipotesi fatte, $m$ e $n$ sono coprimi, quindi $\gcd(m,n)=1,$ perciò possiamo riscrivere la $(5)$ come:

$$ \tag{4}
sm+tn=1
$$

Da questa identità proviamo dunque a ricavare due numeri che permettono di soddisfare separatamente le condizioni della $(3).$ Per prima cosa poniamo $e_1=tn$ ed $e_2=sm.$ Poiché $tn=1-sm,$ è congruente a $1$ modulo $m$ e $sm=1-tn,$ è congruente a $1$ modulo $n,$ valgono le relazioni:

$$ \tag{5}
\begin{align}
e_1 &\equiv 1 \pmod m & e_1 &\equiv 0 \pmod n \\[6pt]
e_2 &\equiv 0 \pmod m & e_2 &\equiv 1 \pmod n
\end{align}
$$

Consideriamo la somma $ae_1+be_2.$ Per le relazioni della $(5)$, questa somma è congruente ad $a\cdot1+b\cdot0=a$ modulo $m$ e ad $a\cdot0+b\cdot1=b$ modulo $n,$ e soddisfa entrambe le condizioni della $(3),$ per cui una soluzione del sistema è data da:

$$ \tag{6}
x_0=ae_1+be_2=atn+bsm
$$

In questo modo abbiamo dimostrato l'esistenza di una soluzione per qualsiasi coppia di interi $a$ e $b.$ Passiamo ora a dimostrare la seconda parte, ovvero l'unicità modulo $mn,$ supponendo che $x_0$ e $x_1$ siano due soluzioni che soddisfano entrambe il sistema. La loro differenza sarà quindi divisibile sia per $m$ sia per $n,$ perché le due soluzioni devono avere gli stessi resti rispetto a entrambi i moduli. Scriviamo allora $x_1-x_0=mq.$ Poiché $n$ divide $mq$ ed è coprimo con $m,$ deve dividere anche $q,$ per cui $q=nh$ per un qualche intero $h.$ Da questo ne consegue che:

$$
x_1-x_0=mnh \tag{7}
$$

Le due soluzioni $x_0$ e $x_1$ sono dunque congruenti modulo $mn.$ Abbiamo così dimostrato il teorema per due moduli coprimi e descritto tutte e sole le soluzioni del sistema $(3).$

- - -

Riprendiamo l'esempio visto all'inizio e proviamo a risolvere il sistema $(2),$ usando la formula $(6).$ Per trovare i coefficienti $s$ e $t,$ scriviamo l'identità di Bézout nella sua forma $(4)$:

$$
2\cdot3-1\cdot5=1
$$

Confrontando la precedente uguaglianza con quella generale ricaviamo che $m=3,$ $s=2,$ $n=5$ e $t=-1.$ Dalle definizioni $e_1=tn$ ed $e_2=sm$ otteniamo quindi $e_1=(-1)\cdot5=-5$ ed $e_2=2\cdot3=6.$ Sostituendo questi valori nella $(6)$ otteniamo:

$$
x_0=2\cdot(-5)+3\cdot6=-10+18=8
$$

Poiché, come sappiamo i moduli sono coprimi, tutte le soluzioni si ottengono aggiungendo a $8$ un multiplo di $15.$ Il sistema ha quindi come insieme delle soluzioni la classe di resto definita da:

$$ \tag{8}
[8]_{15}=\{\ 8+15q\mid q\in\mathbb{Z}\ \}
$$

Il caso mostrato è un caso abbastanza semplice, dove per moduli piccoli, i coefficienti di Bézout si possono individuare direttamente. In generale però il calcolo non è immediato e si ricorre all'algoritmo di Euclide. Il sistema $(2)$ si può anche risolvere sostituendo la prima congruenza nella seconda, ottenendo:

$$
\begin{align}
2+3q &\equiv 3 \pmod 5 \\[6pt]
3q &\equiv 1 \pmod 5
\end{align}
$$

L'inverso di $3$ modulo $5$ è $2,$ perché $3\cdot2=6\equiv1\pmod5.$ Moltiplicando per questo inverso ricaviamo $q\equiv2\pmod5,$ quindi $q=2+5h$ con $h\in\mathbb{Z}.$ Tornando all'incognita iniziale troviamo quindi la stessa soluzione della $(8)$:

$$
x=2+3(2+5h)=8+15h
$$

## Estensione del teorema

Il teorema può essere esteso anche a un numero finito di congruenze. Consideriamo, ad esempio, $n_1,n_2,\ldots,n_k$ interi maggiori di $1,$ con $k\geq2,$ coprimi a due a due, e fissati degli interi arbitrari $a_1,a_2,\ldots,a_k,$ costruiamo il seguente sistema:

$$ \tag{9}
\begin{cases}
x \equiv a_1 \pmod{n_1} \\[6pt]
x \equiv a_2 \pmod{n_2} \\[6pt]
\vdots \\[6pt]
x \equiv a_k \pmod{n_k}
\end{cases}
$$

Trovata una soluzione $x_0$ del $(9),$ tutte e sole le soluzioni si ottengono aggiungendo a $x_0$ un multiplo intero di $N.$ Per costruire una soluzione della $(9),$ poniamo:

$$
N_i=\frac{N}{n_i}
$$

$N_i$ è il prodotto di tutti i moduli tranne $n_i.$ Poiché ciascuno di questi fattori è coprimo con $n_i,$ anche il loro prodotto lo è, e dunque $\gcd(N_i,n_i)=1.$ Esiste allora un intero $u_i$ che è l'inverso moltiplicativo di $N_i$ modulo $n_i,$ che soddisfa:

$$
N_i u_i\equiv1\pmod{n_i}
$$

Il prodotto $N_i u_i$ è invece congruente a zero rispetto a ogni altro modulo $n_j,$ perché $n_j$ è un fattore di $N_i$ quando $j\neq i.$ Questi prodotti hanno quindi la stessa funzione svolta da $e_1$ ed $e_2$ nel caso di due congruenze, perciò una soluzione del sistema $(9)$ è data dalla seguente sommatoria:

$$ \tag{10}
x_0=\sum_{i=1}^{k}a_iN_i u_i
$$

Per verificarla, fissiamo un indice $j$ e consideriamo la somma modulo $n_j.$ Tutti i termini con $i\neq j$ sono multipli di $n_j,$ quindi sono congruenti a zero modulo $n_j$ e non modificano il resto della somma nella divisione per $n_j.$ La somma è perciò congruente al solo termine $a_jN_j u_j,$ che è congruente ad $a_j$ perché $N_j u_j\equiv1\pmod{n_j}.$ Il numero $x_0$ dato dalla $(10)$ soddisfa quindi ciascuna congruenza del sistema.

Per dimostrare anche l'unicità modulo $N,$ confrontiamo la soluzione $x_0$ appena costruita con un'altra soluzione $x_1.$ Le due soluzioni hanno lo stesso resto modulo ogni $n_i,$ quindi ciascun $n_i$ divide $x_1-x_0$ e poiché i moduli sono coprimi a due a due, anche il loro prodotto $N$ divide questa differenza. Ne segue che $x_1\equiv x_0\pmod N,$ quindi ogni soluzione appartiene alla stessa classe di resto di $x_0$ modulo $N$ e questo dimostra quindi l'unicità modulo $N.$

- - -

Facciamo ora un esempio concreto aggiungendo al sistema $(2)$ una terza condizione:

$$ \tag{11}
\begin{cases}
x \equiv 2 \pmod 3 \\[6pt]
x \equiv 3 \pmod 5 \\[6pt]
x \equiv 2 \pmod 7
\end{cases}
$$

Poiché i moduli $3,$ $5$ e $7$ sono coprimi a due a due, il sistema ha un'unica classe di soluzioni modulo $N=3\cdot5\cdot7=105.$ I prodotti dei moduli presi due alla volta sono:

$$
\begin{align}
N_1 &= 105/3=35 \\[6pt]
N_2 &= 105/5=21 \\[6pt]
N_3 &= 105/7=15
\end{align}
$$

Per applicare la formula $(10)$ dobbiamo trovare l'inverso di $35$ modulo $3,$ di $21$ modulo $5$ e di $15$ modulo $7.$ Poiché $35\equiv2\pmod3$ e $2\cdot2\equiv1\pmod3,$ possiamo scegliere $u_1=2.$ Gli altri due inversi sono entrambi uguali a $1,$ dato che $21\equiv1\pmod5$ e $15\equiv1\pmod7.$ Quindi, applicando la $(10)$ otteniamo:

$$
\begin{align}
x_0 &= 2\cdot35\cdot2+3\cdot21\cdot1+2\cdot15\cdot1 \\[6pt]
&=140+63+30=233
\end{align}
$$

Dalla soluzione $x_0=233$ ricaviamo la più piccola soluzione non negativa prendendo il resto nella divisione per $105.$ Poiché $233=2\cdot105+23,$ otteniamo $23,$ che appartiene alla stessa classe di resto modulo $105.$ Il numero $23$ soddisfa infatti le tre congruenze della $(11)$, e infatti si ha:

$$
\begin{align}
23 &= 7\cdot3+2 \\[6pt]
23 &= 4\cdot5+3 \\[6pt]
23 &= 3\cdot7+2
\end{align}
$$

Tutte le soluzioni del sistema sono dunque gli interi della forma:

$$23+105q \quad q\in\mathbb{Z} \tag{12}$$

$23$ è la più piccola soluzione non negativa. Come nel caso del sistema con le due congruenze, possiamo ottenere lo stesso risultato per sostituzione, partendo dalle prime due congruenze, le cui soluzioni sono tutti gli interi $x=8+15h,$ con $h\in\mathbb{Z}.$ Dobbiamo quindi individuare i valori di $h$ per cui questi interi soddisfano anche la terza congruenza, $x\equiv2\pmod7.$ Sostituendo $x=8+15h$ otteniamo:

$$
8+15h\equiv2\pmod7
$$

Poiché $8=7+1$ e $15=2\cdot7+1,$ entrambi sono congruenti a $1$ modulo $7.$ Di conseguenza $15h\equiv h\pmod7,$ e la congruenza diventa $1+h\equiv2\pmod7.$ Sottraendo $1$ da entrambi i membri ricaviamo $h\equiv1\pmod7.$ Quest'ultima condizione significa che $h-1$ è un multiplo di $7,$ quindi $h=1+7q$ per un intero $q.$ Sostituendo questa espressione nella formula $x=8+15h$ troviamo:

$$
\begin{align}
x &= 8+15(1+7q) \\[6pt]
&=8+15+105q \\[6pt]
&=23+105q
\end{align}
$$

Abbiamo in questo modo riottenuto la soluzione ricavata nella $(12).$

## Moduli non coprimi

Riprendiamo il sistema $(3)$ e consideriamo il caso in cui i moduli $m$ e $n$ abbiano un divisore comune maggiore di $1.$ In questa circostanza le due congruenze possono essere incompatibili. Per esempio, se consideriamo $x\equiv1\pmod4$ richiede che $x$ sia dispari, mentre $x\equiv2\pmod6$ richiede che sia pari e quindi è evidente che nessun intero può soddisfare contemporaneamente le due richieste. In genere però, la mancanza di coprimalità, non esclude sempre l'esistenza di soluzioni del nostro sistema. Consideriamo infatti due moduli $m,n>1,$ e poniamo $d=\gcd(m,n).$ Il sistema $(3)$ ammette soluzioni se e solo se:

$$ \tag{13}
d\mid(b-a)
$$

La $(13)$ equivale a richiedere $a\equiv b\pmod d$ e quando è soddisfatta, la soluzione è unica modulo il minimo comune multiplo dei moduli, dato da:

$$ \tag{14}
L=\mathrm{lcm}(m,n)=\frac{mn}{d}
$$

Dimostriamo quindi che la condizione $(13)$ è necessaria e sufficiente affinché il sistema $(3)$ ammetta soluzioni. Iniziamo a provare che la condizione è necessaria e supponiamo che $x$ soddisfi entrambe le congruenze del sistema. Sotto questa ipotesi $m$ divide $x-a$ e $n$ divide $x-b$ e poiché $d$ divide entrambi i moduli, divide anche la loro differenza che è pari a $b-a.$ Per dimostrare invece che la condizione è sufficiente, riscriviamo la prima congruenza del sistema $(3),$ cioè $x\equiv a\pmod m,$ nella forma $x=a+mq,$ con $q\in\mathbb{Z}.$ Sostituendo questa espressione nella seconda congruenza, $x\equiv b\pmod n,$ otteniamo la seguente congruenza:

$$
mq\equiv b-a\pmod n
$$

Se $d$ divide $b-a,$ possiamo dividere per $d,$ ottenendo la congruenza equivalente:

$$ \tag{15}
\frac{m}{d}q\equiv\frac{b-a}{d}\pmod{n/d}
$$

Nella congruenza $(15),$ il coefficiente $m/d$ e il modulo $n/d$ sono coprimi, perché abbiamo diviso $m$ e $n$ per il loro massimo comune divisore $d.$ Se $n/d>1,$ possiamo quindi moltiplicare entrambi i membri per l'inverso di $m/d$ modulo $n/d,$ ottenendo un'unica classe di soluzioni $q\equiv q_0\pmod{n/d}.$ Scrivendo $q=q_0+(n/d)h,$ con $h\in\mathbb{Z},$ e sostituendo questa espressione in $x=a+mq,$ otteniamo la soluzione generale del sistema $(3)$:

$$
x=a+mq_0+\frac{mn}{d}h \qquad h\in\mathbb{Z} \tag{16}
$$

Al variare di $h$ in $\mathbb{Z},$ la $(16)$ descrive tutte e sole le soluzioni del sistema, che formano un'unica classe di resto modulo $L=mn/d.$ Se invece $n/d=1,$ allora $n$ divide $m$ e, grazie alla condizione $(9),$ la prima congruenza implica già la seconda. In questo caso tutti gli interi $x=a+mq$ sono soluzioni e il periodo è ancora $L=m.$ Per esempio, consideriamo il sistema:

$$
\begin{cases}
x \equiv 2 \pmod 6 \\[6pt]
x \equiv 5 \pmod 9
\end{cases}
$$

I moduli hanno massimo comune divisore $3,$ che divide la differenza $5-2=3,$ quindi il sistema ammette soluzioni. Dalla prima congruenza ricaviamo $x=2+6q,$ mentre la seconda diventa $6q\equiv3\pmod9,$ e dividendo per $3$ otteniamo $2q\equiv1\pmod3.$ L'inverso di $2$ modulo $3$ è $2,$ quindi $q\equiv2\pmod3.$ Ne segue quindi che $q=2+3h$ e dunque la soluzione è:

$$
x=2+6(2+3h)=14+18h \qquad h\in\mathbb{Z}
$$

Il sistema ha quindi un'unica classe di soluzioni modulo $18.$

## Interpretazione mediante anelli

La formulazione del teorema può essere effettuata anche in termini di anelli e richiede alcune nozioni di algebra astratta più avanzate. Consideriamo $n_1,\ldots,n_k$ coprimi a due a due e $N=n_1\cdots n_k.$ Definiamo una mappa $\Phi,$ cioè una funzione che a ogni classe $[x]_N$ associa una tupla delle classi dello stesso intero modulo $n_1,\ldots,n_k$ data da:

$$ \tag{17}
\begin{align}
&\Phi :\mathbb{Z}/N\mathbb{Z}\longrightarrow\mathbb{Z}/n_1\mathbb{Z}\times\cdots\times\mathbb{Z}/n_k\mathbb{Z} \\[6pt]
&\Phi([x]_N) =([x]_{n_1},\ldots,[x]_{n_k})
\end{align}
$$

Questa mappa è ben definita poiché, se scegliamo un generico elemento $y$ della stessa classe modulo $N,$ la differenza $x-y$ è divisibile per $N$ e quindi per ciascun $n_i.$ Le classi $[x]_{n_i}$ e $[y]_{n_i}$ coincidono per ogni indice, per cui la tupla associata non dipende dal rappresentante scelto. Verificato che $\Phi$ è ben definita, mostriamo adesso che ogni tupla del codominio è l'immagine di un'unica classe modulo $N.$ Per ogni tupla $([a_1]_{n_1},\ldots,[a_k]_{n_k}),$ il teorema garantisce l'esistenza di un intero $x$ tale che $x\equiv a_i\pmod{n_i}.$ La funzione definita nella $(17)$ associa quindi $[x]_N$ a quella tupla, perciò $\Phi$ è suriettiva. Se poi due classi hanno la stessa immagine, i loro elementi hanno gli stessi resti rispetto a tutti i moduli, quindi per l'unicità modulo $N,$ questi elementi sono congruenti modulo $N,$ e percil le due classi coincidono e ciò dimostra che $\Phi$ è anche iniettiva e dunque biiettiva.

Per mostrare invece che la biiezione $\Phi$ è anche un isomorfismo di anelli, verifichiamo che la somma e il prodotto sono conservati. La riduzione modulo ciascun $n_i$ conserva entrambe le operazioni, quindi per ogni $x,y\in\mathbb{Z}$ valgono le identità:

$$
\begin{align}
\Phi([x]_N+[y]_N)&=\Phi([x]_N)+\Phi([y]_N) \\[6pt]
\Phi([x]_N[y]_N)&=\Phi([x]_N)\Phi([y]_N)
\end{align}
$$

Ponendo $x=1$ nella $(17),$ otteniamo $\Phi([1]_N)=([1]_{n_1},\ldots,[1]_{n_k}).$ Abbiamo quindi una funzione biiettiva che conserva somma, prodotto e identità moltiplicativa, ossia un isomorfismo di anelli. Il teorema cinese del resto assume così la forma:

$$
\mathbb{Z}/N\mathbb{Z}\cong\mathbb{Z}/n_1\mathbb{Z}\times\cdots\times\mathbb{Z}/n_k\mathbb{Z}
$$
