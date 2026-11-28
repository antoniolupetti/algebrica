---
title: Fields
source: https://algebrica.org/fields/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - characteristic
  - complex-numbers
  - distributivity
  - field-extension
  - field-theory
  - finite-field
  - homomorphism
  - rational-numbers
  - real-numbers
  - subfield
---

## Definizione

Un campo $F$ è un anello commutativo con elemento neutro moltiplicativo $1$ distinto dall’elemento neutro additivo $0$, in cui ogni elemento $a \neq 0$ ammette un elemento $a^{-1} \in F$ tale che vale la seguente relazione:

$$
\begin{align}
a \cdot a^{-1} &= 1 \tag{1}
\end{align}
$$

Per ogni $a,b \in F$ con $b \neq 0$, il quoziente $a/b$ è l’elemento $a \cdot b^{-1}$ di $F$. Rispetto all'addizione, $F$ è un gruppo abeliano con elemento neutro $0$, quindi per ogni $a \in F$ vale:

$$a+0=a \tag{2}$$

Inoltre, ogni elemento $a$ ha un opposto  $-a$ per cui vale:

$$a+(-a)=0\tag{3}$$

Rispetto alla moltiplicazione, gli elementi non nulli di $F$ formano un gruppo abeliano con elemento neutro $1$. Inoltre, la moltiplicazione è distributiva rispetto all’addizione, e quindi per ogni $a,b,c \in F$ vale la seguente relazione:

$$a(b+c)=ab+ac\tag{4}$$ 
Dalla $(4)$ seguono le identità:

$$
\begin{align}
a \cdot 0 &= 0 \notag\\[6pt]
(-a)b &= a(-b) = -(ab) \notag\\[6pt]
(-a)(-b) &= ab \notag
\end{align}
$$ 
L'esistenza dell'inverso permette di cancellare ogni fattore non nullo. Se $ab=ac$ e $a \neq 0,$ moltiplicando entrambi i membri per $a^{-1}$ e usando la $(1)$ si ottiene:

$$
\begin{align}
(a^{-1}a)b &= (a^{-1}a)c \notag\\[6pt]
b &= c \tag{5}
\end{align}
$$

In particolare, se $ab=0$ e $a \neq 0,$ possiamo scrivere $ab=a \cdot 0$ e applicando la $(5)$ con $c=0$ otteniamo che $b=0.$ Ogni campo è dunque privo di divisori dello zero e, per la definizione data nella voce sugli anelli, è un dominio d'integrità.

Per fare un esempio, consideriamo l'anello degli interi $\mathbb{Z}$ e mostriamo perché, per ottenere un campo che lo contenga, occorre introdurre i numeri razionali. In $\mathbb{Z}$ solo $1$ e $-1$ hanno un inverso moltiplicativo, perché se due interi $a,b$ soddisfano $ab=1$, allora $|a||b|=1$ e ciascuno ha valore assoluto $1$. Per esempio, l'equazione $2x=1$ ha soluzione $x=1/2$ in $\mathbb{Q}$. Più in generale, un campo che contiene gli interi deve contenere l'inverso $1/q$ di ogni intero $q \neq 0$ e quindi anche, per ogni intero $p$, il prodotto $p \cdot (1/q)=p/q$. Le frazioni che abbiamo ottenuto formano il campo $\mathbb{Q}$, in cui ogni elemento non nullo $p/q$ ha come inverso l'elemento $q/p$ e dunque possiamo concludere che $\mathbb{Q}$ è il più piccolo campo che contiene gli interi.

Consideriamo adesso le equazioni $x^2=2$ e $x^2=-1$ e chiediamoci in quali insiemi numerici possiamo risolverle: nei razionali, nei reali o nei complessi? L'equazione $x^2=2$ non ha soluzioni razionali e ha due soluzioni reali, $x=\pm\sqrt{2}$. L'equazione $x^2=-1$ non ha soluzioni reali, perché il quadrato di un numero reale è sempre maggiore o uguale a zero. In $\mathbb{C}$, dalla fattorizzazione $x^2+1=(x-i)(x+i)$ si ricavano le due soluzioni $x=\pm i$.

Facciamo infine un ulteriore esempio, analizzando dei polinomi con i coefficienti che appartengono a un campo generico $K$ e chiediamoci se l'anello $K[x]$ sia un campo. Se $x$ avesse un inverso in $K[x]$, esisterebbe un polinomio $g$ tale che $xg=1$. Questo è impossibile perché, per ogni $g$ non nullo, il prodotto $xg$ ha grado $\deg(g)+1$, mentre il polinomio costante $1$ ha grado zero. Lo stesso ragionamento vale per ogni polinomio di grado positivo e quindi gli unici polinomi invertibili sono le costanti non nulle $c$, il cui inverso è $1/c$. Quindi, poiché $x$ è non nullo e privo di inverso, possiamo concludere che $K[x]$ non è un campo.

Definiamo ora il concetto di caratteristica di un campo $F$ che è il più piccolo intero positivo $n$ per cui sommando $1$ per $n$ volte si ottiene $0$. Indicando tale somma con $n \cdot 1,$ possiamo scrivere la condizione in questo modo:

$$
\begin{align}
n \cdot 1 &= \underbrace{1+\cdots+1}_{n \text{ addendi}} = 0 \tag{6}
\end{align}
$$

Se nessun intero positivo soddisfa la $(6),$ si dice che $F$ ha caratteristica zero, come nel caso di $\mathbb{Q}$, $\mathbb{R}$ e $\mathbb{C}$. In $\mathbb{R}$, per esempio, sommando $1$ per $n$ volte si ottiene $n$, che è positivo per ogni intero $n \geq 1$. La caratteristica positiva è sempre un numero primo e per dimostrarlo osserviamo che il minimo $n$ che soddisfa la $(6)$ è maggiore di $1$, poiché $1 \neq 0$. Se fosse un numero composto, potremmo scrivere $n=uv$ con $1 \lt u,v \lt n.$ Poiché $n$ è il primo intero positivo per cui la somma è zero e sia $u$ sia $v$ sono interi positivi minori di $n$, $u \cdot 1$ e $v \cdot 1$ sarebbero entrambi non nulli, ma per la distributività e la $(6)$ il loro prodotto sarebbe zero:

$$
\begin{align}
(u \cdot 1)(v \cdot 1) &= (uv) \cdot 1 \notag\\[6pt]
&= n \cdot 1 = 0 \notag
\end{align}
$$

Poiché in un campo il prodotto di due elementi non nulli è diverso da zero, $n$ non può essere composto e deve quindi essere primo.

## Campi finiti e sottocampi

Introduciamo ora il concetto di campo finito che come suggerisce intuitivamente il termine è un campo che contiene un numero finito di elementi. Per esempio, consideriamo le classi di resto modulo $3$, indicate con la seguente espressione:

$$
\begin{align}
\mathbb{Z}/3\mathbb{Z} &= \{[0], [1], [2]\} \tag{7}
\end{align}
$$

Sappiamo che per sommare o moltiplicare due classi bisogna eseguire l'operazione sui loro elementi e poi prendere la classe del risultato. Ciascuna delle due classi non nulle della $(7)$ è l'inverso di sé stessa. Infatti per $[1]$ si ha $[1]\cdot[1]=[1]$ e per $[2]$ si ha $[2]\cdot[2]=[4]=[1]$, e quindi la $(7)$ è un campo finito di tre elementi. Più in generale, per ogni numero primo $p$ ciascuna classe non nulla modulo $p$ ammette un inverso. Infatti, se $[a]$ è una classe non nulla modulo $p$, allora $a$ e $p$ sono necessariamente coprimi e per l'identità di Bézout esistono due interi $r$ e $s$ tali che vale:

$$
\begin{align}
ar+ps &= 1 \tag{8}
\end{align}
$$

Riducendo la $(8)$ modulo $p$, il termine $ps$ ha resto zero e si ottiene $[a][r]=[1]$. Poiché $[a]$ era una qualunque classe non nulla, abbiamo così trovato un inverso per ciascuna classe diversa da $[0]$. L'anello $\mathbb{Z}/p\mathbb{Z}$ è dunque un campo finito con $p$ elementi, indicato con $\mathbb{F}_p$. La sua caratteristica è $p$, perché la somma di $n$ copie di $[1]$ è $[n]$ e il più piccolo intero positivo per cui $[n]=[0]$ è $p$. Se al posto di $p,$ che sappiamo essere un numero primo, scegliamo come modulo un numero composto $n=uv$, con $1 \lt u,v \lt n$, alcune classi non nulle sono prive di inverso. Ad esempio, $[u]$ e $[v]$ sono entrambe classi diverse da $[0]$, ma il loro prodotto è $[uv]=[n]=[0]$, quindi sono divisori dello zero e per questo motivo $\mathbb{Z}/n\mathbb{Z}$ non è un campo. Affinché le classi di resto modulo $n$ formino un campo, $n$ deve quindi essere un numero primo.

## Sottocampi ed estensioni di campi

Un sottoinsieme $K$ di un campo $F$ è un sottocampo se è a sua volta un campo rispetto alle operazioni di $F.$ Per verificarlo, basta controllare le seguenti condizioni:

$$
\begin{align}
0,1 &\in K \notag\\[6pt]
a-b &\in K &&\forall \ a,b \in K \notag\\[6pt]
\frac{a}{b} &\in K &&\forall \ a,b \in K \text{ con } b \neq 0 \tag{9}
\end{align}
$$

Per esempio, i razionali soddisfano le condizioni della $(9)$ rispetto alle operazioni dei reali, quindi $\mathbb{Q}$ è un sottocampo di $\mathbb{R}$ e allo stesso modo, $\mathbb{R}$ è un sottocampo di $\mathbb{C}$ per cui si hanno le seguenti inclusioni:

$$
\begin{align}
\mathbb{Q} \subsetneq \mathbb{R} \subsetneq \mathbb{C} \tag{10}
\end{align}
$$

Quando $K$ è un sottocampo di $F,$ si dice che $F$ è un'estensione di $K$ e si scrive $F/K.$ Prendendo come scalari gli elementi di $K,$ si può considerare $F$ come uno spazio vettoriale su $K$ e la sua dimensione si definisce grado dell'estensione e si indica con $[F:K].$

Per calcolare il grado dell'estensione $\mathbb{C}/\mathbb{R}$ della $(10)$, cerchiamo una base di $\mathbb{C}$ come spazio vettoriale su $\mathbb{R}$. Gli elementi $1$ e $i$ formano una base perché ogni numero complesso si esprime in modo unico come loro combinazione lineare $a\cdot 1+b\cdot i$, con $a,b\in\mathbb{R}$. Poiché la base ha due elementi, il grado dell'estensione è $[\mathbb{C}:\mathbb{R}]=2$.