---
title: Partial Fraction Decomposition
source: https://algebrica.org/partial-fraction-decomposition/
license: CC BY-NC 4.0
tags:
  - cover-up-rule
  - improper-rational-function
  - partial-fractions
  - polynomial-division
  - rational-function
---

## Il metodo di scomposizione

La scomposizione in fratti semplici è un metodo per riscrivere una funzione razionale propria come somma di frazioni e si basa sul principio secondo cui, quando il denominatore si può scomporre in fattori irriducibili, la funzione iniziale può essere espressa come combinazione di termini elementari. Questa separazione è utile per semplificare molti calcoli, ad esempio nel calcolo degli integrali dove il metodo riduce l'integrazione a quella di fratti semplici, che generalmente hanno una primitiva nota. Consideriamo, per esempio, una generica funzione razionale propria, dove $P(x)$ e $Q(x)$ sono polinomi e il grado di $P$ è minore di quello di $Q$:

$$\frac{P(x)}{Q(x)} \tag{1}$$

Per scomporre la frazione $(1)$ in fratti semplici, scriviamo $Q(x)$ come prodotto di fattori irriducibili sui reali, di primo o di secondo grado. Se $Q(x)=(x-a)(x-b)$ con $a\ne b,$ i due fratti semplici hanno numeratori costanti $A$ e $B$:

$$
\frac{P(x)}{(x-a)(x-b)} = \frac{A}{x-a} + \frac{B}{x-b} \tag{2}
$$

Per fare un esempio, applichiamo la $(2)$ alla seguente funzione razionale:

$$
\frac{5x + 4}{2x^2 - x - 6} \tag{3}
$$

La frazione $(3)$ è propria e il denominatore si scompone nel prodotto $(x-2)(2x+3).$ Poiché i due fattori hanno radici distinte, la regola $(2)$ dà la seguente scomposizione:

$$
\frac{5x + 4}{(x - 2)(2x + 3)} = \frac{A}{x - 2} + \frac{B}{2x + 3} \tag{4}
$$

Per determinare $A$ e $B,$ moltiplichiamo entrambi i membri della $(4)$ per il denominatore comune $(x-2)(2x+3)$ e otteniamo:

$$
5x + 4 = A(2x + 3) + B(x - 2) \tag{5}
$$

Per isolare un coefficiente alla volta, sostituiamo nella $(5)$ le due radici del denominatore utilizzando il metodo di Heaviside. Per esempio, sostituendo $x = 2$ nella $(5)$ si ottiene:

$$
5(2) + 4 = A(2 \cdot 2 + 3) + B(0)
$$

Semplificando otteniamo $A$:

$$
\begin{align}
14 &= 7A \\[6pt]
A &= 2
\end{align}
$$

Adesso dobbiamo ricavare $B.$ Ponendo $x=-3/2$ nella $(5)$ si ottiene:

$$
\begin{align}
5\left(-\frac{3}{2}\right)+4 &= B\left(-\frac{3}{2}-2\right) \\[6pt]
-\frac{7}{2} &= -\frac{7}{2}B \\[6pt]
B &= 1
\end{align}
$$

Sostituendo $A=2$ e $B=1$ nella $(4),$ otteniamo la scomposizione della $(3)$ in due fratti semplici:

$$
\frac{5x + 4}{(x - 2)(2x + 3)} = \frac{2}{x - 2} + \frac{1}{2x + 3}
$$

- - -

In generale, se un fattore irriducibile di $Q(x)$ ha molteplicità $k,$ si scrive un fratto semplice per ciascuna delle sue potenze dalla prima alla $k$-esima. Ad esempio, per un fattore lineare $x+a$ i numeratori sono costanti e il contributo di questo fattore alla scomposizione è quindi:

$$
\frac{A_1}{x+a}+\frac{A_2}{(x+a)^2}+\cdots+\frac{A_k}{(x+a)^k} \tag{6}
$$

Per un fattore quadratico irriducibile $q(x)=x^2+ax+b,$ i numeratori hanno grado al più uno. Scrivendo ciascun numeratore nella forma $B_jx+C_j,$ otteniamo:

$$
\frac{B_1x+C_1}{q(x)}+\frac{B_2x+C_2}{q(x)^2}+\cdots+\frac{B_kx+C_k}{q(x)^k} \tag{7}
$$

> Ogni frazione razionale propria a coefficienti reali ammette una scomposizione in fratti semplici e, una volta fissati i fattori del denominatore, i coefficienti nelle formule $(6)$ e $(7)$ sono univocamente determinati.

## Esempio 1

Facciamo un ulteriore esempio applicando la $(6)$ a una frazione con denominatore di terzo grado:

$$
\frac{1}{x^3-6x^2+11x-6} \tag{8}
$$

Il denominatore si annulla per $x=1,$ poiché $1-6+11-6=0.$ Dividendo per $x-1$ con la regola di Ruffini otteniamo:

$$
\begin{array}{r|rrrr}
1 & 1 & -6 & 11 & -6 \\[6pt]
  &   & 1 & -5 & 6 \\[6pt]
\hline
  & 1 & -5 & 6 & 0
\end{array} \tag{9}
$$

Il quoziente $x^2-5x+6$ ottenuto nella $(9)$ si fattorizza in $(x-2)(x-3).$ Il denominatore ha dunque tre fattori lineari distinti, a ciascuno dei quali corrisponde un numeratore costante, perciò possiamo scrivere:

$$
\frac{1}{(x-1)(x-2)(x-3)}
= \frac{A}{x-1}+\frac{B}{x-2}+\frac{C}{x-3} \tag{10}
$$

Moltiplicando la $(10)$ per il denominatore comune otteniamo la seguente identità:

$$
\begin{align}
1 &= A(x-2)(x-3)+B(x-1)(x-3) \\[6pt]
  &\quad + C(x-1)(x-2) \tag{11}
\end{align}
$$

Nella $(11)$ ogni radice del denominatore della $(8)$ annulla due termini e permette di determinare il coefficiente del terzo, quindi otteniamo:

$$
\begin{align}
x=1 &\implies 1=2A  &&\implies A=1/2 \\[6pt]
x=2 &\implies 1=-B  &&\implies B=-1 \\[6pt]
x=3 &\implies 1=2C  &&\implies C=1/2 \tag{12}
\end{align}
$$

Sostituendo nella $(10)$ i coefficienti trovati nella $(12)$ otteniamo la scomposizione della $(8)$:

$$
\frac{1}{x^3-6x^2+11x-6}
= \frac{1}{2(x-1)}-\frac{1}{x-2}+\frac{1}{2(x-3)}
$$

## Esempio 2

Applichiamo ora la $(6)$ al caso di un fattore lineare ripetuto:

$$
\frac{2x+3}{(x-1)^2(x+2)}
= \frac{A}{x-1}+\frac{B}{(x-1)^2}+\frac{C}{x+2}
$$

Moltiplicando per il denominatore comune, come abbiamo fatto nell'esempio precedente, otteniamo la seguente identità:

$$
2x+3=A(x-1)(x+2)+B(x+2)+C(x-1)^2 \tag{13}
$$

Nella $(13)$ le radici del denominatore permettono di isolare prima $B$ e poi $C$:

$$
\begin{align}
x=1 &\implies 5=3B &&\implies B=5/3 \\[6pt]
x=-2 &\implies -1=9C &&\implies C=-1/9
\end{align}
$$

Confrontando i coefficienti di $x^2$ nella $(13)$ otteniamo $A+C=0,$ da cui $A=-C=1/9.$ La scomposizione cercata è:

$$
\frac{2x+3}{(x-1)^2(x+2)}
= \frac{1}{9(x-1)}+\frac{5}{3(x-1)^2}-\frac{1}{9(x+2)}
$$

- - -

Vediamo ora il caso di un denominatore con un fattore lineare e uno di secondo grado, $x^2+1,$ che non ha radici reali. Per la $(7)$ il numeratore del fratto corrispondente ha la forma $Bx+C.$

$$
\frac{3x+1}{(x-1)(x^2+1)}
= \frac{A}{x-1}+\frac{Bx+C}{x^2+1}
$$

Moltiplicando per il denominatore comune, otteniamo l'identità:

$$
3x+1=A(x^2+1)+(Bx+C)(x-1) \tag{14}
$$

Ponendo $x=1$ nella $(14)$ otteniamo $4=2A,$ da cui $A=2.$ Confrontiamo ora i coefficienti di $x^2$ e i termini costanti nei due membri:

$$
\begin{align}
A+B &= 0 &&\implies B=-2 \\[6pt]
A-C &= 1 &&\implies C=1
\end{align}
$$

La scomposizione cercata è quindi:

$$
\frac{3x+1}{(x-1)(x^2+1)}
= \frac{2}{x-1}+\frac{-2x+1}{x^2+1}
$$

## Funzioni razionali improprie

Negli esempi precedenti abbiamo considerato solo frazioni proprie. Vediamo adesso cosa accade quando il grado di $P(x)$ è maggiore o uguale a quello di $Q(x).$ Se dividiamo $P$ per $Q$ otteniamo un quoziente $S$ e un resto $R,$ per cui possiamo riscrivere il rapporto tra i due polinomi come segue:

$$
\frac{P(x)}{Q(x)}=S(x)+\frac{R(x)}{Q(x)} \tag{15}
$$

Se il resto è nullo, la divisione è esatta. Altrimenti $\deg R\lt\deg Q,$ quindi $R(x)/Q(x)$ è una frazione propria.

Consideriamo ad esempio la seguente frazione impropria:

$$
\frac{x^3+2x}{x^2-1} \tag{16}
$$

Dividendo il numeratore $x^3+2x$ per il denominatore $x^2-1$ otteniamo il quoziente $S(x)=x$ e il resto $R(x)=3x$ e dalla $(15)$ possiamo riscrivere la $(16)$ come:

$$
\begin{align}
\frac{x^3+2x}{x^2-1}
&=x+\frac{3x}{x^2-1} \\[6pt]
&=x+\frac{3}{2(x-1)}+\frac{3}{2(x+1)}
\end{align}
$$

## Applicazione al calcolo degli integrali

Come abbiamo accennato all'inizio, la scomposizione in fratti semplici è utile in diversi calcoli che coinvolgono funzioni razionali, in particolare nel calcolo integrale. Consideriamo, per esempio, il seguente integrale:

$$
I=\int \frac{5x+4}{(x-2)(2x+3)} \ dx \tag{17}
$$

La funzione integranda è la $(3),$ per la quale abbiamo già determinato i coefficienti $A=2$ e $B=1.$ Utilizzando la scomposizione $(4)$ possiamo quindi scrivere:

$$
\frac{5x+4}{(x-2)(2x+3)}=\frac{2}{x-2}+\frac{1}{2x+3}
$$

Per la linearità dell'integrale, la $(17)$ si riduce alla somma di due integrali:

$$
I=2\int\frac{1}{x-2} \ dx+\int\frac{1}{2x+3} \ dx
$$

Entrambi hanno una primitiva logaritmica perché il denominatore è lineare e il numeratore è costante e quindi otteniamo:

$$
I=2\ln|x-2|+\frac{1}{2}\ln|2x+3|+c
$$