---
title: Factoring Quadratic Equations
source: https://algebrica.org/factoring-quadratic-equations/
license: CC BY-NC 4.0
tags:
  - ac-method
  - discriminant
  - factoring
  - quadratic-equation
  - vieta-formulas
---
## Scomposizione in fattori

Quando abbiamo introdotto le equazioni di secondo grado abbiamo visto come queste sono rappresentabili secondo la seguente forma standard:

$$ax^{2} + bx + c = 0 \tag{1}$$

Abbiamo anche visto che la $(1)$ richiede che il coefficiente $a$ sia diverso da zero, le sue soluzioni sono ottenibili attraverso il ricorso alla formula quadratica e che la loro natura è determinata dal discriminante $\Delta = b^2 - 4ac.$ In alcuni casi però è possibile trovare le soluzioni senza il ricorso alla formula quadratica, in maniera più immediata utilizzando il metodo della fattorizzazione. L'obiettivo è quello di scomporre la $(1)$ in fattori lineari e trovare così le sue soluzioni. In pratica quando il discriminante è positivo, sappiamo che la $(1)$ ammette due radici reali e distinte, $x_1$ e $x_2,$ per le quali vale la seguente identità:

$$ax^{2} + bx + c = a(x - x_1)(x - x_2) \tag{2}$$

Quando $\Delta = 0$ le radici coincidono e in questo caso la scomposizione si riduce alla forma $a(x - x_0)^2.$ Quando $\Delta < 0,$ il polinomio è irriducibile in $\mathbb{R},$ ammette due radici complesse e coniugate ed è scomponibile solo in $\mathbb{C}.$ Per mostrare come funziona il metodo della fattorizzazione consideriamo il polinomio di secondo grado associato alla $(1)$:

$$P(x) = ax^2 + bx + c \tag{3}$$

Poiché, come condizione abbiamo imposto che $a$ deve essere diverso da zero, possiamo raccogliere a fattor comune il coefficiente del termine di grado massimo e riscrivere la $(3)$ nel seguente modo:

$$P(x) = a\left(x^2 + \frac{b}{a}x + \frac{c}{a}\right) \tag{4}$$

I coefficienti del polinomio tra parentesi sono legati alle radici dalle formule di Viète, trattate in dettaglio nella pagina dedicata, e che sono:

$$
\begin{align}
x_1 + x_2 &= -\frac{b}{a} \\[6pt]
x_1x_2 &= \frac{c}{a}
\end{align}
$$

Sostituendo queste espressioni nella $(4)$ otteniamo:

$$
\begin{align}
P(x) &= a\left[x^2 - (x_1 + x_2)x + x_1x_2\right] \\[6pt]
&= a\left(x^2 - x_1x - x_2x + x_1x_2\right) \\[6pt]
&= a\left[x(x - x_1) - x_2(x - x_1)\right] \\[6pt]
&= a(x - x_1)(x - x_2)
\end{align}
$$

In questo modo abbiamo così dimostrato l'identità $(2).$ A questo punto, le radici dell'equazione $(1)$ si ricavano semplicemente ponendo ciascun fattore lineare uguale a zero, ovvero:

$$ \tag{5}
\begin{align}
x - x_1 = 0 &\implies x = x_1 \\[6pt]
x - x_2 = 0 &\implies x = x_2
\end{align}
$$

> Un procedimento alternativo è il metodo AC, che permette di scomporre il polinomio senza calcolare esplicitamente il suo discriminante.

## Ricerca dei fattori

Addentriamoci ora nel metodo pratico per l'identificazione dei fattori che scompongono la $(1).$ Il processo è piuttosto semplice, ma richiede un po' di pratica. Per prima cosa possiamo cercare direttamente i termini costanti dei fattori lineari usando la seguente identità:

$$a(x + r)(x + s) = a\left[x^2 + (r + s)x + rs\right] \tag{6}$$

Confrontando i coefficienti con quelli della $(1)$ otteniamo due condizioni che $r$ e $s$ devono soddisfare, ovvero:

$$ \tag{7}
\begin{align}
rs &= \frac{c}{a} \\[6pt]
r + s &= \frac{b}{a}
\end{align}
$$

Il nostro obiettivo in questa fase è trovare $r$ e $s$. Disegniamo quindi una tabella come quella dell'esempio seguente che permette di verificare quale riga della tabella soddisfa entrambe le condizioni della $(7)$. Proviamo a scomporre il polinomio $x^2 - 5x + 6$ cercando due numeri il cui prodotto sia $6$ (ovvero $c/a$) e la cui somma sia $-5$ (ovvero $b/a$). Rappresentiamo prima tutte le coppie di interi che danno come prodotto $6$ e scriviamole nelle colonne $r$ e $s$. Nella colonna $r+s$ scriviamo invece la somma per riga dei due valori: 

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

Tenete a mente che l'ordine con cui scriviamo le righe è ininfluente, ma è conveniente operare con criterio per individuare tutti i potenziali numeri candidati. In questo modo possiamo facilmente osservare che la riga che soddisfa entrambe le nostre condizioni della $(7)$ è l'ultima. In questo modo, ponendo $r = -2$ e $s = -3,$ otteniamo la seguente scomposizione:

$$x^2 - 5x + 6 = (x - 2)(x - 3)$$

Quindi, per la $(5)$ l'equazione associata ha come soluzioni $x_1 = 2$ e $x_2 = 3,$ che sono le stesse che si otterrebbero risolvendo l'equazione $x^2 - 5x + 6=0$ con la formula quadratica.

## Esempi

Di seguito è proposta una serie di esempi per prendere confidenza con la scomposizione in fattori delle equazioni di secondo grado. In alcuni di questi casi, la formula risolutiva delle equazioni di secondo grado permetterebbe di ottenere le soluzioni con meno passaggi, tuttavia, in questo caso, la scelta del ricorso alla fattorizzazione risponde esclusivamente ad un obiettivo didattico.

[class="table-1 -right"]

|                      |                           |
| -------------------- | ------------------------- |
| $x^2 - 4x + 3 = 0$   | $x_1 = 1,$ $x_2 = 3$      |
| $2x^2 - 7x + 3 = 0$  | $x_1 = 3,$ $x_2 = 1/2$    |
| $x^2 - 6x + 9 = 0$   | $x_1 = x_2 = 3$           |
| $6x^2 + 13x - 8 = 0$ | $x_1 = 1/2,$ $x_2 = -8/3$ |


[/class]

Consideriamo la prima equazione della tabella e riscriviamo il polinomio ad essa associato:

$$x^{2} - 4x + 3$$

Per trovare la sua fattorizzazione sappiamo che dobbiamo trovare due numeri $r$ e $s$ che soddisfino le relazioni della $(7).$ In questo caso il prodotto deve essere $3$ e la somma $-4.$ Partiamo dall'identificare le coppie di interi il cui prodotto sia $3:$

$$
\begin{array}{c|c|c|c}
r & s & rs & r+s \\[6pt]
\hline
1 & 3 & 3 & 4 \\[6pt]
-1 & -3 & 3 & -4
\end{array}
$$

Ora bisogna verificare quale riga soddisfa la somma $-4$. La somma nella prima riga è $4$ e quindi va scartata. La seconda riga invece è quella che ci interessa. Pertanto i numeri che soddisfano la $(7)$ sono $r = -1$ e $s = -3$ e la scomposizione del polinomio determina quanto segue:

$$x^{2} - 4x + 3 = (x - 1)(x - 3)$$

L'equazione associata al polinomio, per la $(5)$ ha dunque soluzioni $x_1 = 1$ e $x_2 = 3.$

---

Consideriamo il polinomio della seconda equazione:

$$2x^{2} - 7x + 3$$

In questo caso $a = 2,$ perciò raccogliamo questo coefficiente a fattor comune come nella $(4)$ e otteniamo:

$$2\left(x^2 - \frac{7}{2}x + \frac{3}{2}\right)$$

A questo punto cerchiamo due numeri $r$ e $s$ il cui prodotto sia $3/2$ e la cui somma sia $-7/2$ e li rappresentiamo nella solita tabella:

$$
\begin{array}{c|c|c|c}
r & s & rs & r+s \\[6pt]
\hline
1 & 3/2 & 3/2 & 5/2 \\[6pt]
3 & 1/2 & 3/2 & 7/2 \\[6pt]
-1 & -3/2 & 3/2 & -5/2 \\[6pt]
-3 & -1/2 & 3/2 & -7/2
\end{array}
$$

L'ultima riga soddisfa entrambe le condizioni della $(7),$ perciò con $r = -3$ e $s = -1/2,$ otteniamo:

$$2x^{2} - 7x + 3 = 2(x - 3)\left(x - \frac{1}{2}\right) = (x - 3)(2x - 1)$$

Le soluzioni dell'equazione associata sono quindi $x_1 = 3$ e $x_2 = 1/2.$

---

Consideriamo ora il polinomio della terza equazione:

$$x^{2} - 6x + 9$$

Come negli esempi precedenti cerchiamo $r$ e $s$ in modo che il prodotto sia $9$ e la somma sia $-6.$ Scriviamo dunque la solita tabella:

$$
\begin{array}{c|c|c|c}
r & s & rs & r+s \\[6pt]
\hline
1 & 9 & 9 & 10 \\[6pt]
3 & 3 & 9 & 6 \\[6pt]
-1 & -9 & 9 & -10 \\[6pt]
-3 & -3 & 9 & -6
\end{array}
$$

L'ultima riga soddisfa entrambe le condizioni con $r = s = -3$ per cui la scomposizione è:

$$x^{2} - 6x + 9 = (x - 3)^{2}$$

L'equazione pertanto ammette una sola radice $x = 3$ con molteplicità due.

- - -

Consideriamo ora il polinomio:

$$6x^2 + 13x - 8 = 0$$

Raccogliamo il coefficiente $6$ e otteniamo:

$$6x^2 + 13x - 8 = 6\left(x^2 + \frac{13}{6}x - \frac{4}{3}\right)$$

I termini costanti dei fattori devono soddisfare le condizioni:

$$rs = -\frac{4}{3}\qquad r+s = \frac{13}{6}$$

Il prodotto è negativo, quindi i due numeri devono necessariamente avere i segni opposti. Costruiamo la tabella dei valori con alcune coppie di valori candidati:

$$
\begin{array}{c|c|c|c}
r & s & rs & r+s \\[6pt]
\hline
1/6 & -8 & -4/3 & -47/6 \\[6pt]
-1/6 & 8 & -4/3 & 47/6 \\[6pt]
1/3 & -4 & -4/3 & -11/3 \\[6pt]
-1/2 & 8/3 & -4/3 & 13/6
\end{array}
$$

La riga che soddisfa entrambe le condizioni della $(7)$ è quella con $r = -1/2$ e $s = 8/3.$ Svolgendo i calcoli si ottiene:

$$
\begin{align}
6x^2 + 13x - 8 &= 6\left(x - \frac{1}{2}\right)\left(x + \frac{8}{3}\right) \\[6pt]
&= (2x - 1)(3x + 8)
\end{align}
$$

L'equazione associata al polinomio può essere quindi scomposta nei seguenti fattori:

$$(2x - 1)(3x + 8) = 0$$

Per la legge di annullamento del prodotto, almeno uno dei fattori deve essere nullo per cui deve valere:

$$
\begin{align}
2x - 1 &= 0 \\[6pt]
3x + 8 &= 0
\end{align}
$$

Risolvendo le due equazioni di primo grado otteniamo le soluzioni $x_1 = 1/2$ e $x_2 = -8/3.$