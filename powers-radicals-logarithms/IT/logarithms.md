---
title: Logarithms
source: https://algebrica.org/logarithms/
license: CC BY-NC 4.0
tags:
  - change-of-base
  - exponential-inverse
  - logarithmic-function
  - logarithmic-properties
  - logarithms
---
## Definizione

Il logaritmo di un numero è l'esponente a cui occorre elevare una base assegnata per ottenere quel numero. Per esempio, $\log_2 8 = 3$ perché $2^3 = 8.$ In termini formali, se $a$ e $b$ sono numeri reali positivi, il logaritmo di $b$ in base $a$ è il numero reale $c$ tale che $a^c = b.$ Possiamo scrivere la seguente relazione come:

$$\log_a b = c \iff a^c = b \tag{1}$$

$a$ è la base del logaritmo, mentre $b$ è il suo argomento. Per definire correttamente la $(1)$ devono essere soddisfatte le seguenti condizioni:

+ $a > 0$ perché una base nulla o negativa non consente di definire potenze reali per ogni esponente reale.
+ $a \neq 1$ perché $1^c = 1$ per ogni $c,$ quindi l'equazione non ha soluzioni se $b \neq 1$ e ne ha infinite se $b = 1.$
+ $b > 0$ perché ogni potenza di una base positiva è positiva, quindi $a^c$ non può essere nullo o negativo.

Dalla $(1)$ possiamo dedurre che il logaritmo è quindi l'operazione inversa dell'elevamento a potenza. Per le proprietà delle potenze e dalla $(1)$ possiamo ricavare le seguenti identità:

$$a^0 = 1 \Rightarrow \log_a 1 = 0$$

$$a^1 = a \Rightarrow \log_a a = 1$$

Esistono due particolari tipi di logaritmo piuttosto comuni, ovvero i logaritmi naturali e i logaritmi decimali. I logaritmi naturali, o logaritmi in base $e,$ si indicano con $\ln x,$ dove la costante $e$ è il numero di Eulero e sono usati nel calcolo differenziale e integrale. I logaritmi in base $10,$ invece, si indicano con $\log_{10}x$ o $\log x.$ Questi ultimi sono molto utili perché permettono di confrontare gli ordini di grandezza dei numeri. Ad esempio, ogni volta che un numero positivo viene moltiplicato per $10,$ il suo logaritmo decimale aumenta di $1$ (i numeri $10,$ $100$ e $1000$ hanno rispettivamente logaritmo $1,$ $2$ e $3$).

> Fissando una base $a > 0,$ con $a \neq 1,$ e facendo variare l'argomento $x > 0,$ si ottiene la funzione logaritmica, di cui studiamo il grafico e le proprietà analitiche nella voce dedicata.

## Proprietà

I logaritmi soddisfano alcune proprietà algebriche che permettono di riscrivere le espressioni in forme più semplici e facilitare i calcoli. In tutte le proprietà che seguono, la base soddisfa $a > 0$ e $a \neq 1.$ Per $x,y > 0,$ partiamo dalla proprietà del prodotto che riscrive il logaritmo di un prodotto come la somma dei logaritmi dei fattori:

$$
\log_a(xy) = \log_a x + \log_a y \tag{2}
$$

La $(2)$ segue dalle proprietà delle potenze e per dimostrarla poniamo $u = \log_a x$ e $v = \log_a y$ da cui segue per definizione che $x = a^u$ e $y = a^v.$ Come sappiamo, il prodotto di due potenze con la stessa base si ottiene sommando gli esponenti, e quindi possiamo scrivere il prodotto nel seguente modo:

$$xy = a^u a^v = a^{u+v}$$

L'esponente a cui elevare $a$ per ottenere $xy$ è dunque $u+v$ e quindi per la definizione di logaritmo, otteniamo proprio la $(2).$

- - -

Per $x,y > 0,$ la seconda proprietà riscrive il logaritmo di un quoziente come la differenza tra il logaritmo del numeratore e il logaritmo del denominatore, ottenendo la seguente identità:

$$ \tag{3}
\log_a{\frac{x}{y}} = \log_a x - \log_a y
$$

Anche in questo caso, per dimostrare la $(3),$ ricorriamo alla proprietà delle potenze. Poniamo $u = \log_a x$ e $v = \log_a y,$ così che $x = a^u$ e $y = a^v.$ Il quoziente di due potenze con la stessa base si ottiene sottraendo gli esponenti e quindi possiamo scrivere:

$$\frac{x}{y} = \frac{a^u}{a^v} = a^{u-v}$$

Per la $(1),$ l'esponente $u-v$ è il logaritmo di $x/y$ in base $a,$ da cui segue appunto la $(3).$ Come caso particolare, se poniamo $x = 1$ otteniamo:

$$
\log_a{\frac{1}{y}} = -\log_a y
$$

Quindi il logaritmo del reciproco di $y$ è l'opposto del logaritmo di $y.$

- - -

Per $x > 0$ e $n \in \mathbb{R},$ un'altra proprietà utile è la proprietà della potenza per la quale il logaritmo di una potenza è uguale al prodotto dell'esponente per il logaritmo:

$$ \tag{4}
\log_a x^n = n\log_a x
$$

Per dimostrarla, poniamo $u = \log_a x$ e per la definizione di logaritmo otteniamo $x = a^u.$ Elevando entrambi i membri alla potenza $n$ e usando la proprietà della potenza di una potenza, otteniamo:

$$x^n = (a^u)^n = a^{nu}$$

Per la $(1)$ l'esponente a cui elevare $a$ per ottenere $x^n$ è quindi $nu.$ Poiché $u = \log_a x,$ segue quindi la $(4).$

La $(4)$ richiede che l'argomento del logaritmo sia positivo. Per esempio, $\log_a(x^2)$ è definito per ogni $x \neq 0$ anche quando $x$ è negativo. In questo caso, poiché $x^2 = |x|^2,$ la formula valida per tutti i valori ammessi è $\log_a(x^2) = 2\log_a|x|.$ La scrittura $2\log_a x$ è invece definita soltanto per $x > 0.$

- - -

Dalla $(4)$ discende la proprietà del logaritmo di un radicale, valida per $b > 0$ e $n \in \mathbb{N}$ con $n \ge 2.$ Poiché un radicale può essere scritto come una potenza con esponente razionale ($\sqrt[n]{b} = b^{1/n}$), otteniamo:
$$ \tag{5}
\log_a\sqrt[n]{b} = \frac{1}{n}\log_a b
$$

- - -

Supponiamo che $x,y,z > 0$ e proviamo ad applicare le proprietà appena viste alla seguente espressione:

$$ \tag{6}
\log_a \left( \frac{x^3 \cdot y}{z^2} \right)
$$

Partiamo dal notare che la $(6)$ contiene un quoziente all'interno dell'argomento del logaritmo, per cui possiamo applicare la $(3)$ e riscrivere l'espressione come:

$$ \tag{7}
\log_a(x^3 \cdot y) - \log_a(z^2)
$$

Il primo logaritmo contiene un prodotto e per la $(2)$ possiamo riscriverlo come:

$$
\log_a(x^3 \cdot y) = \log_a(x^3) + \log_a(y)
$$

La $(7)$ quindi diventa:

$$
\log_a(x^3) + \log_a(y) - \log_a(z^2)
$$

Infine, per la proprietà delle potenze possiamo riscrivere il primo e il terzo logaritmo usando la $(4)$ così da ottenere:

$$ \tag{8}
3 \log_a(x) + \log_a(y) - 2 \log_a(z)
$$


## Cambiamento di base di un logaritmo

La formula del cambiamento di base permette di riscrivere un logaritmo qualunque in un logaritmo in una base per la quale si conoscono i valori o si dispone di strumenti di calcolo, come la base $e$ o la base $10.$ Inoltre, è molto utile nelle espressioni perché consente di esprimere i logaritmi con basi diverse in logaritmi della stessa base, facilitando i calcoli. Supponiamo di avere $a,b>0,$ $a,b\neq1$ e $x>0.$ La formula del cambiamento è la seguente:

$$\log_a x = \frac{\log_b x}{\log_b a} \tag{9}$$

Per dimostrarla, poniamo $y=\log_a x$ e per la definizione di logaritmo otteniamo l'uguaglianza $a^y=x.$ Applicando il logaritmo in base $b$ a entrambi i membri si ottiene:

$$\log_b(a^y) = \log_b(x)$$

Nel membro di sinistra possiamo sfruttare la proprietà delle potenze vista nella $(4)$ e ottenere:

$$y\log_b(a) = \log_b(x)$$

Ricavando $y$ si ottiene dunque proprio la $(9).$ Facciamo un esempio concreto mostrando come il cambiamento di base permette di calcolare la seguente espressione.

$$\log_2 3 \cdot \log_3 8 \tag{10}$$

Se riscriviamo il secondo logaritmo dalla base $3$ alla base $2,$ otteniamo un fattore comune al numeratore e al denominatore che possiamo semplificare. Usando la $(9),$ possiamo riscrivere la $(10)$ e ottenere il seguente risultato:

$$
\begin{align}
\log_2 3 \cdot \log_3 8 &= \log_2 3 \cdot \frac{\log_2 8}{\log_2 3} \\[6pt]
&= \log_2 8 \\[6pt]
&= 3
\end{align}
$$

## Logaritmi e strutture algebriche

Le proprietà dei logaritmi possono essere interpretate nel linguaggio dell'algebra astratta, che studia gli insiemi e le operazioni definite su di essi. In questo ambito, la proprietà del prodotto $(2)$ permette di interpretare il logaritmo come una corrispondenza tra due strutture algebriche.

Come sappiamo, l'insieme dei numeri reali positivi è un gruppo rispetto alla moltiplicazione, con elemento neutro $1$ e inverso di ogni generico elemento $x$ pari a $1/x.$ I numeri reali formano invece un gruppo rispetto all'addizione, con elemento neutro $0$ e inverso di ogni elemento $u$ uguale a $-u.$ Nel caso del logaritmo, questo associa a ogni numero positivo un numero reale e trasforma il prodotto nel primo gruppo nella somma nel secondo, secondo l'identità $(2).$

Questo genere di corrispondenza che conserva le operazioni dei due gruppi è un omomorfismo. Questa corrispondenza rispetta anche gli elementi neutri e gli inversi dei due gruppi. Infatti, $\log_a 1 = 0$ associa l'elemento neutro della moltiplicazione a quello dell'addizione, mentre $\log_a(1/x) = -\log_a x$ associa il reciproco di $x$ all'opposto del suo logaritmo.

Inoltre, ogni numero reale $u$ è il logaritmo di un unico numero positivo $a^u.$ La corrispondenza è quindi biiettiva e per questo è un isomorfismo di gruppi.
