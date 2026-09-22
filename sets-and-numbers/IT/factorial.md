---
title: Factorial
source: https://algebrica.org/factorial/
license: CC BY-NC 4.0
tags:
  - asymptotic-analysis
  - binomial-coefficient
  - combinatorics
  - factorial
  - gamma-function
  - permutations
  - recursive-definition
  - stirling-approximation
---

## Definizione

Il fattoriale di un numero intero non negativo $n$ rappresenta il prodotto di tutti gli interi positivi da 1 a $n$ e si indica con il simbolo $n!.$ Come vedremo nel dettaglio più avanti, la sua origine deriva dai problemi del calcolo combinatorio e in particolare dalla necessità di calcolare in quanti modi diversi si possono ordinare $n$ oggetti distinti. Per ora, soffermiamoci ad analizzare la sua definizione ricorsiva che, per $n \geq 1,$ è data dalla seguente relazione:

$$
\begin{align} \tag{1}
n! &= n \cdot (n-1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1 \\[6pt]
&= n \cdot (n-1)!
\end{align}
$$

Per fare un esempio, il fattoriale di $4,$ che è pari a $24,$ si calcola moltiplicando tutti gli interi da $4$ a $1:$

$$
4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24
$$

Per convenzione, il fattoriale di $0$ è uguale a $1.$ Il motivo è molto semplice: questa convenzione rende coerente la sua formulazione ricorsiva ottenuta dalla $(1).$ Consideriamo infatti la relazione $n \cdot (n-1)!$ e poniamo $n=1$. Da questa si ottiene che $1! = 1\cdot0!$ e siccome 1! è pari a 1, allora per soddisfare l'uguaglianza deve per forza essere che $0!$ sia anch'esso pari a 1.

Partendo dalla $(1)$ il fattoriale può anche essere espresso mediante una funzione ricorsiva definita per casi:

$$ \tag{2}
n! =
\begin{cases}
n \cdot (n-1)! & \text{se } n \in \mathbb{N},\ n > 0 \\[6pt]
1 & \text{se } n = 0
\end{cases}
$$

La stessa definizione si può scrivere in forma più compatta usando il simbolo della produttoria $\prod,$ con l'indice $k$ che varia da $1$ a $n:$

$$\tag{3}
n! =
\begin{cases}
\displaystyle\prod_{k=1}^{n} k & \text{se } n \in \mathbb{N},\ n > 0 \\[6pt]
1 & \text{se } n = 0
\end{cases}
$$

Una delle applicazioni che più frequentemente si presentano con l'uso del fattoriale è quella per il calcolo del coefficiente binomiale che, in estrema sintesi, conta i modi in cui si può scegliere un dato numero di elementi da un insieme.

Calcolando invece il fattoriale per $n = 0, 1, 2, 3, \ldots,$ otteniamo la successione di numeri naturali il cui termine di indice $n$ è $a_n = n!:$

$$
a_0 = 1,\quad a_1 = 1,\quad a_2 = 2,\quad a_3 = 6,\quad a_4 = 24,\quad \ldots
$$

Un'altra proprietà interessante del fattoriale, che viene spesso omessa nella sua descrizione, riguarda la scomposizione di $n!$ in fattori primi. In pratica, fissato un numero primo $p,$ il suo esponente conta quante volte il fattore $p$ compare complessivamente nei numeri da $1$ a $n.$ Nella scomposizione in fattori primi, ogni multiplo di $p$ contiene almeno un fattore $p,$ ogni multiplo di $p^2$ ne contiene almeno due, ogni multiplo di $p^3$ almeno tre, e così via.

I multipli di $p$ compresi tra $1$ e $n$ sono i numeri $kp,$ con $k$ intero positivo e $kp \leq n,$ ossia $k \leq n/p.$ Il loro numero è quindi $\lfloor n/p \rfloor,$ la parte intera inferiore di $n/p,$ cioè il più grande intero minore o uguale a $n/p.$ Contando allo stesso modo i multipli delle potenze successive di $p,$ l'esponente è dato da:

$$
\left\lfloor \frac{n}{p} \right\rfloor + \left\lfloor \frac{n}{p^2} \right\rfloor + \left\lfloor \frac{n}{p^3} \right\rfloor + \cdots
$$

Questa somma ha un numero finito di termini non nulli, perché quando $p^j > n$ si ha $\lfloor n/p^j \rfloor = 0.$

Per esempio, per rendere la spiegazione più chiara, calcoliamo l'esponente del fattore primo $2$ nella scomposizione di $5!,$ scegliendo quindi $n = 5$ e $p = 2.$ Nel prodotto $5! = 1 \cdot 2 \cdot 3 \cdot 4 \cdot 5,$ i numeri che ontengono il fattore primo $2$ solo solo i multipli di $2,$ ovvero $2$ e $4,$ perciò contiamo inizialmente un fattore $2$ per ciascuno di essi. Il numero $4 = 2^2$ contiene però un secondo fattore $2,$ che contiamo considerando i multipli di $2^2 = 4.$ Tra $1$ e $5$ il solo multiplo di $4$ è $4,$ mentre non ci sono multipli di $2^3 = 8$ o di potenze successive. L'esponente di $2$ in $5!$ è pertanto $3$:

$$
\left\lfloor \frac{5}{2} \right\rfloor + \left\lfloor \frac{5}{4} \right\rfloor = 2 + 1 = 3
$$

E difatti, la scomposizione in fattori primi di $5!$ è proprio pari a $120 = 2^3 \cdot 3 \cdot 5.$

## Semplificazione di rapporti tra fattoriali

Dalla definizione del fattoriale si ricavano delle proprietà algebriche che consentono di semplificare i rapporti tra fattoriali due o più fattoriali. Supponiamo ad esempio di avere due interi non negativi $n$ e $k$ con $n > k$ e di voler calcolare il seguente rapporto:

$$
\frac{n!}{(n-k)!}
$$

I fattori da $(n-k)$ a $1$ si semplificano con il denominatore, lasciando al numeratore un prodotto di $k$ fattori:

$$
\frac{n!}{(n-k)!} = n \cdot (n-1) \cdot \ldots \cdot (n-k+1)
$$

Per $k = 0,$ il rapporto è $n!/n! = 1$ e il prodotto a destra si intende vuoto, con valore $1.$

Consideriamo, per esempio, il rapporto tra $7!$ e $4!.$ I fattori da $4$ a $1$ compaiono sia al numeratore sia al denominatore e quindi si semplificano. Al numeratore rimane il prodotto degli interi da $7$ a $5:$

$$
\frac{7!}{4!} = \frac{7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}{4 \cdot 3 \cdot 2 \cdot 1} = 7 \cdot 6 \cdot 5 = 210 \tag{4}
$$

Il rapporto tra $7!$ e $4!$ è quindi $210.$ Lo stesso ragionamento vale se si vuole calcolare il rapporto tra $4!$ e $7!.$ Semplificando i fattori comuni da $4$ a $1,$ al numeratore rimane $1$ e al denominatore il prodotto $7 \cdot 6 \cdot 5.$ 

$$
\frac{4!}{7!} = \frac{4 \cdot 3 \cdot 2 \cdot 1}{7 \cdot 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1} = \frac{1}{210}
$$

Pertanto rapporto è $1/210,$ ovvero il reciproco della $(4)$ come era ovvio aspettarsi..

## Il fattoriale nel calcolo combinatorio

Come abbiamo detto all'inizio, il fattoriale trova la sua origine nella risoluzione di problemi derivanti dal calcolo combinatorio. Infatti $n!$ conta le permutazioni di $n$ oggetti distinti, ovvero in quanti modi diversi questi oggetti possono essere disposti in un certo ordine. Per esempio, con $n = 3$ oggetti si hanno $3! = 6$ permutazioni possibili:

$$
\begin{array}{rrrr}
& o_1 & o_2 & o_3 \\[6pt]
\hline
& 1 & 2 & 3 \\[6pt]
& 1 & 3 & 2 \\[6pt]
& 2 & 1 & 3 \\[6pt]
& 2 & 3 & 1 \\[6pt]
& 3 & 1 & 2 \\[6pt]
& 3 & 2 & 1
\end{array}
$$

Supponiamo ora di voler scegliere dai nostri tre oggetti un gruppo con soltanto due oggetti, tenendo conto dell'ordine (scegliere prima $1$ e poi $2$ è diverso da scegliere prima $2$ e poi $1).$ Le coppie ordinate possibili sono:

$$
(1,2),\quad (2,1),\quad (1,3),\quad (3,1),\quad (2,3),\quad (3,2)
$$

Ogni gruppo di due oggetti compare esattamente due volte, ad esempio $(1,2)$ e $(2,1)$. Per contare quanti sono i gruppi senza distinguere l'ordine, basta dividere il numero dei gruppi totali per $2!,$ ovvero 6/2. In questo modo is ottengono tre gruppi, formati rispettivamente dagli oggetti:

$$
\{1,2\},\quad \{1,3\},\quad \{2,3\}
$$

Lo stesso ragionamento vale quando scegliamo $k$ oggetti tra $n$ oggetti distinti, con $1 \leq k \leq n.$ Se teniamo conto dell'ordine, abbiamo $n$ possibilità per il primo oggetto, $n-1$ per il secondo, fino a $n-k+1$ per il $k$-esimo, perché ogni oggetto può essere scelto una sola volta. Moltiplicando queste possibilità, otteniamo:

$$
n \cdot (n-1) \cdot \ldots \cdot (n-k+1) = \frac{n!}{(n-k)!}
$$

In questo conteggio, ciascun gruppo di $k$ oggetti compare $k!$ volte, una per ogni possibile ordine dei suoi elementi. Se ci interessa soltanto quali oggetti vengono scelti, dividiamo per $k!$ in modo da contare ciascun gruppo una sola volta. Il numero di gruppi così ottenuto è rappresentato dal coefficiente binomiale che merita una trattazione a parte e la cui formula è:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!} \tag{5}
$$

## Un'identità utile con il fattoriale

Proponiamo adesso un'identità che aiuta a semplificare le operazioni con i fattoriali. Consideriamo la seguente frazione:

$$
\frac{n}{n!}
$$

Per $n \geq 1,$ se sostituiamo la definizione ricorsiva della $(1)$ al denominatore d il fattore $n$ si semplifica e si ottiene così la seguente identità:

$$
\frac{n}{n!} = \frac{n}{n \cdot (n-1)!} = \frac{1}{(n-1)!}
$$

Questa identità si applica, per esempio, per semplificare le espressioni che compaiono nel calcolo della media della distribuzione di Poisson o nella riscrittura del coefficiente binomiale della $(5)$ in una forma più semplice.

## Relazione tra il fattoriale e la funzione gamma

All'inzio di questa trattazione abbiamo definito il fattoriale solo per i numeri interi non negativi. In realtà questa definizione può essere estesa anche ai numeri reali non negativi attraverso la funzione gamma che è definita per ogni $c \in \mathbb{R}^+,$ dal seguente integrale improprio:

$$
\Gamma(c) = \int_{0}^{+\infty} x^{c - 1} e^{-x} \ dx
$$

Per ottenere il fattoriale di un numero, occorre calcolare la funzione gamma del numero aumentato di uno. Per esempio, il fattoriale di $4$ è uguale a $\Gamma(5).$ Vale pertanto la seguente relazione che permette di definire il fattoriale anche quando il numero non è intero.

$$
\Gamma(n+1) = n! \tag{6}
$$

La relazione $(6)$ suggerisce di definire, per ogni numero reale $x \geq 0,$ il fattoriale nel modo seguente:

$$
x! := \Gamma(x+1)
$$

Per i numeri naturali, la funzione gamma restituisce lo stesso risultato che otteniamo con la definizione iniziale del fattoriale. Per esempio, moltiplicando gli interi da $1$ a $4$ otteniamo $4! = 24,$ e anche $\Gamma(5) = 24.$ Se invece consideriamo la frazione $1/2,$ la definizione della $(1)$ non si applica, perché $1/2$ non è un intero. Possiamo però usare la definizione estesa mediante la funzione gamma. Poiché $1/2 + 1 = 3/2,$ sostituiamo $c = 3/2$ nella definizione integrale. L'esponente di $x$ diventa $3/2 - 1 = 1/2,$ perciò $x^{1/2} = \sqrt{x}.$ Otteniamo:

$$
\begin{align}
\left(\frac{1}{2}\right)! &:= \Gamma\left(\frac{3}{2}\right) \\[6pt]
&= \int_{0}^{+\infty} x^{\frac{3}{2}-1}e^{-x} \ dx \\[6pt]
&= \int_{0}^{+\infty} \sqrt{x}e^{-x} \ dx \\[6pt]
&= \frac{\sqrt{\pi}}{2}
\end{align}
$$

> Il fattore $\sqrt{\pi}$ deriva dal calcolo dell'integrale di Gauss, al quale rimandiamo per la giustificazione del risultato.

## Approssimazione di Stirling

Non sempre è possibile calcolare in maniera agevole ed efficente il fattoriale perché per $n$ che cresce rapidamente la sua crescita è più rapida delle funzioni polinomiali e delle funzioni esponenziali a base fissa. In questi casi si ricorre all'approssimazione di Stirling che è una stima di $n!$ per valori di $n$ molto grandi. La stima si basa sulla seguente forma asintotica:

$$
n! \approx \sqrt{2\pi n} \left(\frac{n}{e}\right)^n
$$

Già per valori relativamente piccoli di $n,$ il valore del fattoriale può superare $10^6,$ mentre $2^n$ è ancora dell'ordine di $10^3.$ Nella tabella è rappresentato un confronto tra le varie crescite all'aumentare di $n$.

| $n$ | Polinomio $n^2$ | Esponenziale $2^n$ | Fattoriale $n!$ |
|-----|----------------|-------------------|----------------|
| 2   | 4              | 4                 | 2              |
| 5   | 25             | 32                | 120            |
| 10  | 100            | 1.024             | 3.628.800      |
| 15  | 225            | 32.768            | Circa 1.308 miliardi |

L'approssimazione diventa sempre più accurata al crescere di $n,$ perciò il rapporto tra $n!$ e la sua approssimazione di Stirling tende a $1$ quando $n$ tende ad infinito:

$$
\lim_{n \to \infty} \frac{n!}{\sqrt{2\pi n}\left(\dfrac{n}{e}\right)^n} = 1
$$

 Per $n = 10,$ il valore esatto è $10! = 3.628.800,$ mentre la stima di Stirling è circa $3.598.696,$ con un errore relativo inferiore all'$1\%.$ Per $n > 100,$ l'errore relativo scende sotto lo $0{,}1\%.$ Per ottenere stime più accurate si può introdurre un termine correttivo, ricavato applicando la formula di Eulero-Maclaurin alla somma $\log(n!) = \sum_{k=1}^{n} \log k:$

$$
n! \approx \sqrt{2\pi n} \left(\frac{n}{e}\right)^n \left(1 + \frac{1}{12n}\right) \tag{7}
$$

Con la $(7)$ entriamo in una trattazione più avanzata che va al di là del nostro scopo, pertanto ci limitiamo a una presentazione del risultato senza svilupparne la dimostrazione.