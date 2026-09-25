---
title: Vieta's Formulas
source: https://algebrica.org/vieta-formulas/
license: CC BY-NC 4.0
tags:
  - elementary-symmetric-polynomials
  - polynomial
  - polynomial-roots
  - symmetric-polynomials
  - vieta-formulas
---

## Introduzione e formule

Sappiamo che le equazioni polinomiali in una sola variabile sono equazioni della forma $P(x) = 0,$ in cui $P(x)$ è un polinomio. La loro forma standard è data da:

$$\tag{1}
a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0 = 0
$$

I coefficienti $a_0, a_1, \ldots, a_n$ possono essere numeri reali o complessi, mentre $n$ è il grado dell'equazione. Per garantire il grado $n$ della $(1)$ è fondamentale che valga l'ipotesi $a_n \neq 0.$ Ad esempio, un'equazione di secondo grado è un'equazione polinomiale con grado $n=2,$ $a \neq 0$ e forma standard:

$$ax^2 + bx + c = 0 \tag{2}$$

Nelle equazioni della forma $(1)$ o $(2)$ esistono delle relazioni che legano esplicitamente le radici dell'equazione ai coefficienti del polinomio, note come formule di Viète. Tali formule possono essere enunciate da due punti di vista equivalenti: permettono di esprimere somma e prodotto delle radici in funzione dei coefficienti in modo da poter risolvere un'equazione, e allo stesso tempo descrivono come determinare i coefficienti di un polinomio una volta note le radici.

- - -

Consideriamo una generica equazione di secondo grado nella forma standard espressa dalla $(2)$. Indichiamo le due radici come $x_1$ e $x_2$ in modo da poter scomporre il polinomio nel seguente modo:

$$a(x - x_1)(x - x_2) \tag{3}$$

Sviluppando i calcoli otteniamo:

$$
ax^2 - a(x_1 + x_2)x + ax_1 x_2
$$

Confrontando i coefficienti con quelli della $(2),$ otteniamo $-a(x_1 + x_2) = b$ e $ax_1x_2 = c.$ Poiché $a \neq 0,$ possiamo dividere per $a$ e ricavare le formule di Viète per il caso delle equazioni di secondo grado:

$$\tag{4}
\begin{align}
x_1 + x_2 &= -\frac{b}{a} \\[6pt]
x_1 x_2 &= \frac{c}{a}
\end{align}
$$

Queste identità esprimono quindi le relazioni tra radici e coefficienti e valgono per ogni valore del discriminante, anche quando le radici sono complesse e coniugate.

- - -

Un altro modo per ricavare le formule della $(4)$ utilizza la formula risolutiva delle equazioni di secondo grado con la quale possiamo scrivere le due radici nel seguente modo:

$$
x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

Ricordando che $\Delta = b^2 - 4ac,$ se sommiamo $x_1$ con $x_2$ otteniamo la prima relazione della $(4)$:

$$
\begin{align}
x_1 + x_2 &= \frac{-b + \sqrt{\Delta} - b - \sqrt{\Delta}}{2a} \\[6pt]
&= \frac{-2b}{2a} \\[6pt]
&= -\frac{b}{a}
\end{align}
$$

Per il prodotto, invece utilizziamo il seguente prodotto notevole $(u + v)(u - v) = u^2 - v^2$ al numeratore e sostituiamo l'espressione del discriminante, ottenendo la seconda relazione della $(4)$:

$$
\begin{align}
x_1 x_2 &= \frac{(-b + \sqrt{\Delta})(-b - \sqrt{\Delta})}{4a^2} \\[6pt]
&= \frac{b^2 - \Delta}{4a^2} \\[6pt]
&= \frac{b^2 - (b^2 - 4ac)}{4a^2} \\[6pt]
&= \frac{c}{a}
\end{align}
$$

## Forma generale

Le formule della $(4)$ si estendono a qualunque polinomio $P(x)$ di grado $n$ nella forma:

$$ \tag{5}
P(x) = a_n x^n + a_{n-1} x^{n-1} + \cdots + a_1 x + a_0
$$

Per il teorema fondamentale dell'algebra, il polinomio della $(5)$ ammette $n$ radici in $\mathbb{C},$ contate con la loro molteplicità. Indicandole con $x_1, x_2, \ldots, x_n,$ possiamo scomporlo come nel caso di secondo grado della $(3)$:

$$
P(x) = a_n (x - x_1)(x - x_2) \cdots (x - x_n)
$$

Eseguiamo i calcoli, tenendo a mente che, nello sviluppo, per ottenere un generico termine $x^{n-k}$ dobbiamo scegliere il termine $-x_i$ da $k$ fattori e il termine $x$ dai rimanenti $n-k.$ Il coefficiente di $x^{n-k}$ è quindi la somma di tutti i prodotti di $k$ radici con indici distinti, moltiplicata per $a_n(-1)^k.$ Questa somma si può scrivere nel seguente modo:

$$ \tag{6}
e_k(x_1, \ldots, x_n) = \sum_{1 \le i_1 < i_2 < \cdots < i_k \le n} x_{i_1} x_{i_2} \cdots x_{i_k}
$$

$e_k$ è definito polinomio simmetrico elementare. Confrontando il coefficiente di $x^{n-k}$ nello sviluppo con quello della $(5),$ otteniamo $a_{n-k} = a_n(-1)^k e_k$ e poiché $a_n \neq 0,$ possiamo dividere per $a_n$ e ricavare le formule di Viète nella loro forma generale:

$$
\frac{a_{n-k}}{a_n} = (-1)^k e_k(x_1, \ldots, x_n), \qquad k = 1, 2, \ldots, n
$$

Per $k = 1,$ ciascun prodotto nella $(6)$ contiene una sola radice, quindi $e_1 = x_1 + \cdots + x_n.$ Otteniamo così la formula di Viète per la somma delle radici di un polinomio di grado $n,$ che generalizza la prima relazione della $(4)$:

$$ \tag{7}
x_1 + x_2 + \cdots + x_n = -\frac{a_{n-1}}{a_n}
$$

La seconda relazione della $(4)$ si generalizza invece ponendo $k = n$:

$$ \tag{8}
x_1 x_2 \cdots x_n = (-1)^n\frac{a_0}{a_n}
$$

Nel caso di secondo grado, $n = 2$ e i coefficienti sono $a_2 = a,$ $a_1 = b$ e $a_0 = c.$ Poiché $e_1 = x_1 + x_2$ ed $e_2 = x_1 x_2,$ applicando la formula generale per $k = 1$ e $k = 2$ ritroviamo esattamente la $(4)$:

$$
\begin{align}
x_1 + x_2 &= -\frac{a_1}{a_2} = -\frac{b}{a} \\[6pt]
x_1 x_2 &= (-1)^2 \frac{a_0}{a_2} = \frac{c}{a}
\end{align}
$$
- - -

Vediamo adesso un caso particolare applicando la formula generale al grado tre considerando un'equazione di terzo grado in forma standard:

$$
ax^3 + bx^2 + cx + d = 0
$$

Come nel caso dell'equazione di secondo grado, indichiamo le radici con $x_1,$ $x_2$ e $x_3,$ e deriviamo le formule di Viète con le seguenti relazioni:

$$
\begin{align}
x_1 + x_2 + x_3 &= -\frac{b}{a} \\[6pt]
x_1 x_2 + x_1 x_3 + x_2 x_3 &= \frac{c}{a} \\[6pt]
x_1 x_2 x_3 &= -\frac{d}{a}
\end{align}
$$

## Esempi

Mettiamo in pratica le formule viste finora considerando l'equazione di secondo grado:

$$
x^2 - 5x + 6 = 0
$$

I coefficienti sono $a = 1,$ $b = -5$ e $c = 6,$ quindi le radici devono avere somma $5$ e prodotto $6.$ Per individuarle, seguiamo il procedimento descritto nella scomposizione delle equazioni di secondo grado e cerchiamo due fattori della forma $(x + r)(x + s).$ In questa notazione $r = -x_1$ e $s = -x_2,$ perché le radici annullano i rispettivi fattori. Sviluppando il prodotto otteniamo $x^2 + (r + s)x + rs.$ Il confronto dei coefficienti impone quindi le condizioni:

$$
\begin{align}
rs &= \frac{c}{a} = 6 \\[6pt]
r + s &= \frac{b}{a} = -5
\end{align}
$$

Per prima cosa, elenchiamo nella tabella tutte le coppie di interi il cui prodotto è $6$ e nell'ultima colonna calcoliamo la somma per verificare quale coppia soddisfa anche la condizione della somma:

$$
\begin{array}{c|c|c|c}
r & s & rs & r+s \\[6pt]
\hline
1 & 6 & 6 & 7 \\[6pt]
2 & 3 & 6 & 5 \\[6pt]
-1 & -6 & 6 & -7 \\[6pt]
-2 & -3 & 6 & -5
\end{array}
$$

Come si può vedere, l'unica riga che soddisfa entrabe le condizioni del prodotto e della somma è l'ultima, con $r = -2$ e $s = -3.$ Quindi il polinomio si può scomporre come:
$$
(x - 2)(x - 3)
$$

Per la legge di annullamento del prodotto, l'equazione è soddisfatta quando $x - 2 = 0$ oppure $x - 3 = 0$ e ee radici sono dunque $x_1 = 2$ e $x_2 = 3.$

- - -

Consideriamo adesso la seguente equazione di terzo grado:

$$
x^3 - 6x^2 + 11x - 6 = 0 \tag{9}
$$

Supponiamo di aver individuato le possibili radici $1,$ $2$ e $3$ e calcoliamo i polinomi $e_i$:

$$
\begin{align}
e_1 &= 1 + 2 + 3 = 6 \\[6pt]
e_2 &= 1 \cdot 2 + 1 \cdot 3 + 2 \cdot 3 = 11 \\[6pt]
e_3 &= 1 \cdot 2 \cdot 3 = 6
\end{align}
$$

Le formule di Viète diventano $-b = e_1,$ $c = e_2$ e $-d = e_3.$ Sostituendo i coefficienti dell'equazione otteniamo $-(-6) = 6,$ $11 = 11$ e $-(-6) = 6,$ verificando tutte le uguaglianze. La scomposizione della $(9)$ pertanto diventa:

$$
x^3 - 6x^2 + 11x - 6 = (x - 1)(x - 2)(x - 3)
$$

Quindi, sempre per la legge di annullamento del prodotto, le radici dell'equazione sono $1,$ $2$ e $3.$

- - -

Vediamo ora un ultimo caso che è caratterizzato da un coefficiente direttivo diverso da $1.$ Consideriamo la seguente equazione di secondo grado:

$$
2x^2 - 8x + 6 = 0
$$

Applicando le formule della $(4),$ otteniamo:

$$
\begin{align}
x_1 + x_2 &= -\frac{-8}{2} = 4 \\[6pt]
x_1 x_2 &= \frac{6}{2} = 3
\end{align}
$$

Cerchiamo quindi due numeri con prodotto $3$ e somma $4.$ Possiamo utilizzare una tabella come quella del primo esempio, riportando questa volta direttamente le possibili radici nelle colonne $x_1$ e $x_2$:

$$
\begin{array}{c|c|c|c}
x_1 & x_2 & x_1x_2 & x_1+x_2 \\[6pt]
\hline
1 & 3 & 3 & 4 \\[6pt]
-1 & -3 & 3 & -4
\end{array}
$$

Soltanto la prima riga ha anche somma $4,$ quindi i numeri cercati sono $1$ e $3.$ Poiché nella scomposizione dobbiamo tenere conto del coefficiente direttivo $a = 2,$ scriviamo:

$$
2x^2 - 8x + 6 = 2(x - 1)(x - 3)
$$

Anche in questo caso, sempre per la legge di annullamento del prodotto, le radici dell'equazione sono $x_1 = 1$ e $x_2 = 3.$

## Costruzione di un polinomio

Come abbiamo anticipato nell'introduzione, le formule di Viète si possono anche leggere nella direzione opposta per costruire il polinomio $P(x)$ a partire dalle radici. Se le radici sono $\alpha_1, \alpha_2, \ldots, \alpha_n,$ il polinomio monico, cioè quello con coefficiente direttivo pari a $1,$ è dato dalla seguente espressione:

$$\tag{10}
P(x) = x^n - e_1 x^{n-1} + e_2 x^{n-2} - \cdots + (-1)^n e_n
$$

Per esempio, cerchiamo il polinomio monico di terzo grado le cui radici sono $2,$ $-1$ e $3.$ Ponendo $n = 3,$ la formula diventa:

$$
P(x) = x^3 - e_1 x^2 + e_2 x - e_3
$$

Per determinarne i coefficienti dobbiamo calcolare $e_1,$ la somma delle radici, $e_2,$ la somma dei loro prodotti a due a due, ed $e_3,$ il prodotto delle tre radici. Con queste informazioni possiamo scrivere le seguenti uguaglianze:

$$
\begin{align}
e_1 &= 2 + (-1) + 3 = 4 \\[6pt]
e_2 &= 2 \cdot (-1) + 2 \cdot 3 + (-1) \cdot 3 = 1 \\[6pt]
e_3 &= 2 \cdot (-1) \cdot 3 = -6
\end{align}
$$

Applicando la $(10),$ il polinomio cercato è pertanto:

$$
P(x) = x^3 - 4x^2 + x + 6
$$
