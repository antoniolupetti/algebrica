---
title: Fundamental Theorem of Arithmetic
source: https://algebrica.org/fundamental-theorem-of-arithmetic/
license: CC BY-NC 4.0
tags:
  - divisibility
  - euclids-lemma
  - fundamental-theorem-of-arithmetic
  - integers
  - prime-factorization
  - prime-numbers
  - unique-factorization
---

## Enunciato

Il teorema fondamentale dell'aritmetica afferma che ogni numero naturale $n\geq2$ si può scrivere come prodotto di numeri primi e che, in qualunque fattorizzazione di $n,$ ciascun primo compare lo stesso numero di volte. Per dimostrare l'esistenza della fattorizzazione in primi, applichiamo il principio di induzione forte a $n.$ Come sappiamo, per il principio di induzione, dobbiamo per prima cosa considerare un caso iniziale, che nel nostro caso è $n=2,$ che è primo. Per $n\gt2,$ supponiamo che ogni numero naturale compreso fra $2$ e $n-1$ ammetta una fattorizzazione in primi. Se $n$ è primo, il prodotto consiste del solo fattore $n$ mentre se $n$ è composto, possiamo scriverlo nella forma seguente.

$$
\tag{1}
\begin{align}
n &= ab \\[6pt]
1 &\lt a\lt n \\[6pt]
1 &\lt b\lt n
\end{align}
$$

Poiché nella $(1)$ $a$ e $b$ sono minori di $n,$ l'ipotesi induttiva permette di scrivere ciascuno di essi come prodotto di numeri primi. Sostituendo questi due prodotti ad $a$ e $b$ si ottiene una fattorizzazione in primi di $n.$ Da questa parte del teorema segue che i numeri primi sono infiniti. Se $p_1,\ldots,p_k$ fossero tutti i primi, potremmo considerare il numero naturale seguente dato da:

$$
N=p_1p_2\cdots p_k+1
\tag{2}
$$

Poiché ciascun $p_i$ divide il prodotto nella $(2),$ la divisione di $N$ per $p_i$ dà come resto $1.$ Inoltre, poiché $N\gt1,$ l'esistenza della fattorizzazione garantisce che $N$ ha almeno un divisore primo che deve essere diverso da tutti i primi dell'elenco, che dunque non può essere completo.

## Lemma di Euclide e unicità

Il lemma di Euclide afferma che, se un numero primo $p$ divide il prodotto di due interi $a$ e $b,$ allora divide almeno uno dei due fattori.

$$
p\mid ab \quad\Longrightarrow\quad p\mid a \ \text{oppure}\ p\mid b
\tag{3}
$$

Per dimostrare la $(3),$ supponiamo che $p\mid ab$ e che $p\nmid a.$ Poiché i soli divisori positivi di $p$ sono $1$ e $p,$ l'ipotesi $p\nmid a$ implica che $\gcd(p,a)=1.$ Per l'identità di Bézout esistono quindi interi $s,t$ tali che $sp+ta=1.$ Moltiplicando per $b$ si ottiene l'identità seguente.

$$
b=spb+tab
\tag{4}
$$

Nella $(4)$ il primo addendo è banalmente un multiplo di $p$ mentre il secondo lo è perché $p\mid ab,$ ovvero $ab=pk$ per qualche intero $k,$ da cui $tab=p(tk).$ La loro somma è dunque divisibile per $p.$ Applicando la $(3)$ al primo fattore e al prodotto dei rimanenti, e ripetendo il ragionamento su quest'ultimo, si deduce che un primo che divide un prodotto finito divide almeno uno dei fattori. Supponiamo ora che un naturale $n\geq2$ ammetta due fattorizzazioni in numeri primi tale che valga la seguente identità:

$$
n=p_1p_2\cdots p_r=q_1q_2\cdots q_s
\tag{5}
$$

Poiché $p_1$ divide il prodotto di destra nella $(5),$ il lemma di Euclide implica che $p_1$ divide qualche $q_j.$ Essendo $q_j$ primo, il suo unico divisore positivo maggiore di $1$ è $q_j$ stesso, dunque $p_1=q_j.$ Possiamo allora cancellare il fattore comune e ripetere il procedimento sui prodotti rimasti. Quando uno dei due prodotti si esaurisce, l'altro deve esaurirsi nello stesso momento, perché un prodotto con almeno un fattore primo è maggiore di $1.$ Le due fattorizzazioni hanno quindi gli stessi fattori con le stesse molteplicità.

## Fattorizzazione degli interi non nulli

Consideriamo ora un intero $n$ con $|n|\gt1,$ e applicando il teorema al suo valore assoluto e raggruppando le occorrenze di ciascun numero primo, si ottiene la seguente forma:

$$
n=\varepsilon p_1^{e_1}\cdots p_k^{e_k}
\tag{6}
$$

Nella $(6)$ il prodotto $p_1^{e_1}\cdots p_k^{e_k}$ è la fattorizzazione di $|n|.$ I numeri $p_1,\ldots,p_k$ sono i primi distinti che compaiono nella fattorizzazione e ciascun esponente $e_i$ indica quante volte compare il primo $p_i.$ Per ricavare $n$ da $|n|$ basta moltiplicare il prodotto per $\varepsilon,$ che vale $1$ se $n$ è positivo e $-1$ se $n$ è negativo.

Per esempio, poiché $|-60|=60=2^2\cdot3\cdot5,$ nella fattorizzazione di $-60$ il fattore $\varepsilon$ vale $-1,$ il primo $2$ compare due volte e i primi $3$ e $5$ compaiono una volta ciascuno. Si ottiene così $-60=(-1)\cdot2^2\cdot3\cdot5.$ La $(6)$ vale anche per $n=1$ e $n=-1,$ se si usa la convenzione secondo cui il prodotto senza fattori vale $1.$ In questi due casi $n$ coincide quindi con $\varepsilon.$

Se gli interi $a_1,\ldots,a_k$ sono coprimi a due a due e ciascuno divide $x,$ allora anche il prodotto $a_1\cdots a_k$ divide $x.$ Per $x=0$ basta osservare che $0=(a_1\cdots a_k)\cdot0.$ Se $x\neq0,$ tutti gli $a_i$ sono non nulli e possiamo confrontare le fattorizzazioni dei loro valori assoluti con quella di $|x|.$

Fissiamo un primo $p$ che compare nel prodotto $|a_1\cdots a_k|.$ Se $p$ dividesse due fattori distinti, sarebbe un divisore comune maggiore di $1,$ contro l'ipotesi che gli $a_i$ siano coprimi a due a due. Dunque $p$ compare in un solo fattore $|a_i|$ e il suo esponente nel prodotto è lo stesso che ha in $|a_i|.$ Poiché $a_i$ divide $x,$ possiamo scrivere $|x|=|a_i||q|$ per un intero non nullo $q.$ Nella fattorizzazione di $|x|$ compaiono quindi tutte le occorrenze di $p$ presenti in $|a_i|.$ Questo vale per ogni primo del prodotto, perciò $|a_1\cdots a_k|$ divide $|x|$ e quindi $a_1\cdots a_k$ divide $x.$