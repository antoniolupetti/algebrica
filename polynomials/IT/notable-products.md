---
title: Prodotti Notevoli
source: https://algebrica.org/notable-products/
license: CC BY-NC 4.0
tags:
  - binomial-theorem
  - difference-of-squares
  - factoring
  - notable-products
  - sum-and-difference-of-cubes
---

## Elenco dei prodotti notevoli

I prodotti notevoli sono identità che descrivono lo sviluppo o la scomposizione in fattori di polinomi e sono molto utili perché consentono di riscrivere espressioni come binomi o trinomi in una forma estesa o più semplice, a seconda delle esigenze di calcolo del singolo problema. In linea generale, molte delle identità illustrate di seguito sono casi particolari del teorema binomiale che per ogni intero $n$ non negativo e due numeri reali  $a$ e $b$ fornisce lo sviluppo del seguente binomio:

$$(a+b)^n$$

Iniziamo da una delle forme più riconoscibili dei prodotti notevoli, ovvero il quadrato di un binomio, che si ottiene moltiplicando il binomio per sé stesso. Possiamo distinguere due casi, uno per la somma e l'altro per la differenza dei termini:

$$ \tag{1}
\begin{align}
(a+b)^2 &= a^2 + 2ab + b^2 \\[6pt]
(a-b)^2 &= a^2 - 2ab + b^2
\end{align}
$$

Per dimostrarlo sviluppiamo il primo prodotto della $(1)$ ottenendo:

$$
\begin{align}
(a+b)^2 &= (a+b)(a+b) \\[6pt]
&= a^2 + ab + ab + b^2 \\[6pt]
&= a^2 + 2ab + b^2
\end{align}
$$

La seconda identità della $(1)$ si dimostra in modo analogo alla precedente:

$$
\begin{align}
(a-b)^2 &= (a-b)(a-b) \\[6pt]
&= a^2 - ab - ab + b^2 \\[6pt]
&= a^2 - 2ab + b^2
\end{align}
$$
- - -

Quando ci troviamo invece davanti alla differenza di due quadrati, possiamo riscriverla nel seguente modo:

$$
a^2 - b^2 = (a+b)(a-b) \tag{2}
$$

Per dimostrarlo, riscriviamo il prodotto al secondo membro attraverso semplici manipolazioni algebriche, ottenendo il risultato della $(2)$:

$$
\begin{align}
(a+b)(a-b) &= a(a-b) + b(a-b) \\[6pt]
&= a^2 - ab + ab - b^2 \\[6pt]
&= a^2 - b^2
\end{align}
$$

- - -

Vale la pena menzionare che per scomporre invece la somma di due quadrati in fattori lineari è necessario ricorrere ai numeri complessi, usando l'unità immaginaria $i.$ Supponiamo, per esempio di avere due numeri reali $a$ e $b$ reali e di riscrivere $b^2=-(ib)^2.$ Per la somma dei quadrati otteniamo:

$$ \tag{3}
\begin{align}
a^2+b^2 &= a^2-i^2b^2 \\[6pt]
&= a^2-(ib)^2 \\[6pt]
&= (a+ib)(a-ib)
\end{align}
$$

Per esempio, con $a=x$ e $b=1$ si ottiene la scomposizione:

$$x^2+1=(x+i)(x-i)$$

La formula $(3)$ è utile anche per eliminare la parte immaginaria dal denominatore di una frazione, ad esempio quando vogliamo scrivere il quoziente di due numeri complessi nella forma $x+iy$ per determinarne la parte reale e quella immaginaria. Se $a$ e $b$ non sono entrambi nulli, allora $a^2+b^2>0.$ Moltiplicando numeratore e denominatore per il coniugato $a-ib,$ ricaviamo:

$$
\begin{align}
\frac{1}{a+ib} &= \frac{a-ib}{(a+ib)(a-ib)} \\[6pt]
&= \frac{a-ib}{a^2+b^2} \\[6pt]
&= \frac{a}{a^2+b^2}-i\frac{b}{a^2+b^2}
\end{align}
$$

- - -

Per il cubo di un binomio valgono le seguenti identità, a seconda che i due termini siano sommati o sottratti:

$$ \tag{4}
\begin{align}
(a+b)^3 &= a^3 + 3a^2b + 3ab^2 + b^3 \\[6pt]
(a-b)^3 &= a^3 - 3a^2b + 3ab^2 - b^3
\end{align}
$$

Per dimostrare la prima identità della $(4)$ espandiamo il primo membro:

$$
\begin{align}
(a+b)^3 &= (a+b)^2(a+b) \\[6pt]
&= (a^2+2ab+b^2)(a+b) \\[6pt]
&= a(a^2+2ab+b^2)+b(a^2+2ab+b^2) \\[6pt]
&= a^3+2a^2b+ab^2+a^2b+2ab^2+b^3 \\[6pt]
&= a^3+3a^2b+3ab^2+b^3
\end{align}
$$

Analogamente, dimostriamo la seconda identità della $(4)$, ottenendo:

$$
\begin{align}
(a-b)^3 &= (a-b)^2(a-b) \\[6pt]
&= (a^2-2ab+b^2)(a-b) \\[6pt]
&= a(a^2-2ab+b^2)-b(a^2-2ab+b^2) \\[6pt]
&= a^3-2a^2b+ab^2-a^2b+2ab^2-b^3 \\[6pt]
&= a^3-3a^2b+3ab^2-b^3
\end{align}
$$

- - -

Consideriamo ora la somma e la differenza di due cubi ottenendo le seguenti identità:

$$ \tag{5}
\begin{align}
a^3 + b^3 &= (a+b)(a^2 - ab + b^2) \\[6pt]
a^3 - b^3 &= (a-b)(a^2 + ab + b^2)
\end{align}
$$

Dimostriamo la prima identità della $(5)$ sviluppando il secondo membro, ottenendo:

$$
\begin{align}
(a+b)(a^2-ab+b^2) &= a^3 - a^2b + ab^2 + a^2b - ab^2 + b^3 \\[6pt]
&= a^3 + b^3
\end{align}
$$

Lo stesso procedimento si applica alla differenza $a^3 - b^3$ e dà:

$$
\begin{align}
(a-b)(a^2+ab+b^2) &= a^3 + a^2b + ab^2 - a^2b - ab^2 - b^3 \\[6pt]
&= a^3 - b^3
\end{align}
$$

Non vi sarà di certo sfuggito che, mentre la somma di due cubi si scompone in fattori a coefficienti reali, per scomporre la somma di due quadrati in fattori lineari dobbiamo ricorrere all'unità immaginaria come visto nella $(3).$ Questo accade perché due numeri reali opposti hanno cubi opposti, quindi $a^3+b^3$ si annulla quando $a=-b$ e ammette il fattore $a+b.$ I quadrati reali sono invece sempre non negativi e la loro somma si può annullare solo quando entrambi i termini sono nulli.

- - - 

Riepiloghiamo quindi di seguito le formule illustrate sopra:

[class="table-1"]

|                                         |                                                                         |
| --------------------------------------- | ----------------------------------------------------------------------- |
| $$(a + b)^2$$                           | $$a^2 + 2ab + b^2$$                                                     |
| $$(a - b)^2$$                           | $$a^2 - 2ab + b^2$$                                                     |
| $$a^2 - b^2$$                           | $$(a + b)(a - b)$$                                                      |
| $$(a + b)^3$$                           | $$a^3 + 3a^2b + 3ab^2 + b^3$$                                           |
| $$(a - b)^3$$                           | $$a^3 - 3a^2b + 3ab^2 - b^3$$                                           |
| $$a^3 + b^3$$                           | $$(a + b)(a^2 - ab + b^2)$$                                             |
| $$a^3 - b^3$$                           | $$(a - b)(a^2 + ab + b^2)$$                                             |

[/class]


## Relazione col teorema binomiale

Abbiamo detto all'inizio che espressioni come il quadrato e il cubo di un binomio si ricavano da una formula generale data dal teorema binomiale, che fornisce lo sviluppo di di un generico binomi attraverso la seguente l'identità:

$$ \tag{6}
(a+b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^{k}
$$

Nella $(6)$ ricordiamo che i coefficienti binomiali sono definiti dalla formula $(7)$ che ricorre all'uso del fattoriale:

$$ \tag{7}
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

Per fare un esempio, proviamo a ricavare il cubo di un binomio, ovvero la prima identità della $(4)$, ponendo $n=3$ e calcolando i coefficienti della sommatoria. Otteniamo:

$$
\begin{align}
\binom{3}{0}=\binom{3}{3} &= \frac{3!}{0!3!}=1 \\[6pt]
\binom{3}{1}=\binom{3}{2} &= \frac{3!}{1!2!}=3
\end{align}
$$

Sostituendo questi valori nella $(6)$, otteniamo proprio la relazione che stavamo cercando:

$$
(a+b)^3 = a^3 + 3a^2b + 3ab^2 + b^3
$$

## Prodotti notevoli nella risoluzione di equazioni

I prodotti notevoli consentono di risolvere alcune equazioni polinomiali mediante la scomposizione in fattori, che permette di ricondurre il problema a equazioni di grado inferiore. Consideriamo la seguente equazione:

$$x^3-8=7(x-2) \tag{8}$$

Il membro a sinistra della $(8)$ si può riscrivere come Poiché $x^3-2^3,$ ottenendo una differenza di due cubi. Applicando la seconda identità della $(5)$ otteniamo:

$$
\begin{align}
(x-2)(x^2+2x+4)=7(x-2) \\[6pt]
(x-2)(x^2+2x+4)-7(x-2) &= 0 \\[6pt]
(x-2)(x^2+2x+4-7) &= 0 \\[6pt]
(x-2)(x^2+2x-3) &= 0
\end{align}
$$

Per la legge di annullamento del prodotto, sappiamo che l'equazione è soddisfatta quando almeno uno dei due fattori è nullo, il che significa risolvere le due equazioni:

$$
\begin{align}
&1) \ x-2 = 0 \\[6pt]
&2) \ x^2+2x-3 = 0
\end{align}
$$

La prima equazione lineare dà come soluzione $x=2.$ Per la seconda, utilizziamo la formula risolutiva delle equazioni di secondo grado e otteniamo:

$$
\begin{align}
x &= \frac{-2\pm\sqrt{2^2-4(1)(-3)}}{2} \\[6pt]
&= \frac{-2\pm\sqrt{16}}{2} \\[6pt]
&= \frac{-2\pm4}{2}
\end{align}
$$

Le soluzioni della seconda equazione sono $x=1$ e $x=-3.$ L'equazione iniziale ha quindi le tre soluzioni $-3,$ $1$ e $2.$ La scomposizione mediante i prodotti notevoli ha quindi ricondotto l'equazione di terzo grado alla risoluzione di un'equazione di primo grado e di una di secondo grado. Abbiamo così determinato le soluzioni di un'equazione di terzo grado senza ricorrere alla regola di Ruffini.

## Somma e differenza di potenze n-esime

Le scomposizioni viste per i quadrati e i cubi sono casi particolari di formule più generali. Per ogni intero positivo $n,$ la differenza $a^n-b^n$ ha sempre $a-b$ come fattore. La somma $a^n+b^n,$ invece, ha $a+b$ come fattore solo quando $n$ è dispari. Quando $n \geq 2,$ la differenza si scompone usando la formula:

$$ \tag{9}
a^n-b^n = (a-b)(a^{n-1}+a^{n-2}b+a^{n-3}b^2+\cdots+ab^{n-2}+b^{n-1})
$$

Quando $n \geq 3$ è dispari, la somma ammette una scomposizione analoga alla $(9)$,  con segni alternati nel secondo fattore:

$$ \tag{10}
a^n+b^n = (a+b)(a^{n-1}-a^{n-2}b+a^{n-3}b^2-\cdots-ab^{n-2}+b^{n-1})
$$

Sia nella $(9)$ che nella $(10),$ quando $n=1$ il secondo fattore è paria a $1.$ Quando $n$ è pari, la somma $a^n+b^n$ non è divisibile per $a+b,$ ma può ammettere altre scomposizioni a coefficienti reali. Il polinomio $a^2+b^2,$ ad esempio, è irriducibile su $\mathbb{R},$ mentre $a^4+b^4$ si scompone in due fattori quadratici a coefficienti reali. In questo secondo caso, infatti, poiché $n = 4$ è pari, non possiamo applicare la formula per la somma di potenze n-esime, valida per gli esponenti dispari. Il polinomio però ammette comunque la seguente scomposizione tramite coefficienti reali:

$$a^4 + b^4 = (a^2 + \sqrt{2}ab + b^2)(a^2 - \sqrt{2}ab + b^2)$$

Per verificare la scomposizione, raggruppiamo $a^2$ e $b^2$ in ciascun fattore e riscriviamo il primo fattore come $(a^2+b^2)+\sqrt{2}ab$ e il secondo come $(a^2+b^2)-\sqrt{2}ab.$ Il prodotto ha quindi la forma $(A+B)(A-B),$ con $A=a^2+b^2$ e $B=\sqrt{2}ab.$ Applicando l'identità $(2)$ otteniamo:

$$
\begin{align}
(a^2 + \sqrt{2}ab + b^2)(a^2 - \sqrt{2}ab + b^2) &= (a^2 + b^2)^2 - (\sqrt{2}ab)^2 \\[6pt]
&= a^4 + 2a^2b^2 + b^4 - 2a^2b^2 \\[6pt]
&= a^4 + b^4
\end{align}
$$

- - -

Un'altra scomposizione utile è l'identità di Germain permette di dimostrare che alcuni interi della forma $n^4+4m^4$ possono essere scritti come prodotto di due interi maggiori di $1:$

$$ \tag{11}
a^4+4b^4 = (a^2+2b^2+2ab)(a^2+2b^2-2ab)
$$

Il coefficiente $4$ che compare nella $(11)$ consente di completare il quadrato e di riscrivere il membro a destra come una differenza tra due quadrati:

$$
a^4+4b^4 = (a^2+2b^2)^2-(2ab)^2
$$

Di seguito sono riepilogati sinteticamente alcuni prodotti di potenze n-esime:

[class="table-1"]

|                                         |                                                                         |
| --------------------------------------- | ----------------------------------------------------------------------- |
| $$a^n + b^n \quad (n \text{ dispari})$$ | $$(a + b)(a^{n-1} - a^{n-2}b + \cdots + b^{n-1})$$                      |
| $$a^n - b^n$$                           | $$(a - b)(a^{n-1} + a^{n-2}b + \cdots + b^{n-1})$$                      |
| $$a^{2n} - b^{2n}$$                     | $$(a^n - b^n)(a^n + b^n)$$                                              |
| $$a^4 - b^4$$                           | $$(a - b)(a + b)(a^2 + b^2)$$                                           |
| $$a^4 + b^4$$                           | $$(a^2 + \sqrt{2}ab + b^2)(a^2 - \sqrt{2}ab + b^2)$$                    |
| $$(a + b + c)^2$$                       | $$a^2 + b^2 + c^2 + 2(ab + ac + bc)$$                                   |
| $$(a + b + c)^3$$                       | $$a^3 + b^3 + c^3 + 3(a^2b + a^2c + b^2a + b^2c + c^2a + c^2b) + 6abc$$ |
[/class]

