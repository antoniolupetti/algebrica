---
title: Sign Function
source: https://algebrica.org/sign-function/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - functions
  - heaviside-function
  - odd-function
  - sign-function
---

## Introduzione alla funzione segno

La funzione segno è una funzione discontinua che associa a ogni numero reale il suo segno, indipendentemente dal suo valore assoluto ed è definita a tratti dalle seguenti relazioni:

$$ \tag{1}
y = \mathrm{sgn}(x) =
\begin{cases}
-1 & \text{se } x < 0 \\[6pt]
0 & \text{se } x = 0 \\[6pt]
1 & \text{se } x > 0
\end{cases}
\quad \forall \ x \in \mathbb{R}
$$

Per fare alcuni esempi, se applichiamo la $(1)$ a un numero reale otteniamo:

$$
\begin{align}
\mathrm{sgn}(-7) &= -1 \\[6pt]
\mathrm{sgn}(0) &= 0 \\[6pt]
\mathrm{sgn}(4) &= 1
\end{align}
$$

Il grafico della $(1)$ è formato da due semirette orizzontali e da un punto isolato. La prima semiretta giace sulla retta $y = -1$ e comprende tutti i punti con $x < 0,$ mentre la seconda giace sulla retta $y = 1$ e comprende tutti i punti con $x > 0.$ L'origine $(0, 0)$ rappresenta invece il punto isolato.

![IMG. 1](../svg/sign-function-1.svg)

Come si può vedere dal grafico, la funzione segno è una funzione dispari, poiché per qualunque valore di $x \in \mathbb{R}$ soddisfa l'identità:

$$
\mathrm{sgn}(-x) = -\mathrm{sgn}(x)
$$

## Proprietà e limiti

Dalla $(1)$ si ricavano le principali proprietà della funzione segno, che riportiamo di seguito.

+ Dominio: $\mathbb{R}$
+ Immagine: $\{-1,\ 0,\ 1\}$
+ La funzione è dispari, poiché $\mathrm{sgn}(-x) = -\mathrm{sgn}(x).$
+ La funzione ha un unico zero in $x = 0.$
+ La funzione è costante su $(-\infty, 0)$ e su $(0, +\infty)$ e poiché i suoi valori sono, nell'ordine, $-1,$ $0$ e $1,$ la funzione è non decrescente su $\mathbb{R}.$
+ La funzione ha una discontinuità in $x = 0$ mentre è continua in ogni altro punto.
+ La funzione non è derivabile in $x = 0$ mentre lo è, con derivata nulla, in ogni altro punto.

La funzione segno è moltiplicativa, cioè il segno di un prodotto è uguale al prodotto dei segni dei fattori. In termini formali, quindi, per ogni $x, y \in \mathbb{R}$ vale la seguente identità:

$$\mathrm{sgn}(xy) = \mathrm{sgn}(x)\mathrm{sgn}(y) \tag{2}$$

La $(2)$ rappresenta la regola dei segni che si incontra nella moltiplicazione. Se i due fattori sono non nulli e hanno lo stesso segno, il loro prodotto è positivo ed entrambi i membri valgono $1.$ Se hanno segni opposti, il prodotto è negativo ed entrambi i membri valgono $-1.$ Se almeno un fattore è nullo, anche il prodotto è nullo ed entrambi i membri valgono $0.$ Per quanto riguarda i limiti, poiché la funzione segno vale $-1$ per $x < 0$ e $1$ per $x > 0,$ i limiti laterali nell'origine sono:

$$
\begin{align}
\lim_{x \to 0^-} \mathrm{sgn}(x) &= -1 \\[6pt]
\lim_{x \to 0^+} \mathrm{sgn}(x) &= 1
\end{align}
$$

Se la funzione ammettesse limite $L$ per $x \to 0,$ anche i due limiti laterali dovrebbero essere uguali a $L.$ Per il teorema di unicità del limite, avremmo allora sia $L = -1$ sia $L = 1,$ il che è impossibile e pertanto il seguente limite non esiste:

$$\lim_{x \to 0} \mathrm{sgn}(x)$$

Quando $x$ tende a $\pm \infty$ la funzione segno mantiene un valore costante:

$$
\begin{align}
\lim_{x \to -\infty} \mathrm{sgn}(x) &= -1 \\[6pt]
\lim_{x \to +\infty} \mathrm{sgn}(x) &= 1
\end{align}
$$

Questi risultati seguono dal fatto che $\mathrm{sgn}(x) = -1$ per ogni $x < 0$ e $\mathrm{sgn}(x) = 1$ per ogni $x > 0.$ Il valore della funzione rimane quindi invariato quando $x$ si allontana da zero lungo ciascun semiasse.

## Derivata e integrale

Abbiamo visto nelle proprietà che la funzione segno ammette derivata nulla per $x \neq 0:$

$$
\frac{d}{dx} \mathrm{sgn}(x) = 0
$$

In $x = 0$ la derivata non esiste, perché la funzione è discontinua in quel punto. Attraversando l'origine da sinistra verso destra, la funzione passa da $-1$ a $1,$ con un salto di ampiezza $2$, cioè $1 - (-1).$ In uno studio più avanzato, che esula da questa trattazione, la teoria delle distribuzioni estende la nozione di derivata permettendo di rappresentare questo salto mediante un valore $\delta(x),$ chiamato delta di Dirac. Ai fini della nostra descrizione, segnaliamo solo che la derivata nel senso delle distribuzioni è data da:

$$
\frac{d}{dx} \mathrm{sgn}(x) = 2\delta(x)
$$

Su ciascuno dei due intervalli $(-\infty, 0)$ e $(0, +\infty),$ l'integrale indefinito della funzione segno è dato da:

$$
\int \mathrm{sgn}(x) \ dx = |x| + c
$$

La costante $c$ può essere scelta indipendentemente sui due intervalli. Questo risultato è in linea con il fatto che la derivata di $|x|$ è proprio uguale a $\mathrm{sgn}(x)$ in ogni punto in cui $|x|$ è derivabile.

## Relazione con la funzione valore assoluto e con la funzione gradino di Heaviside

Esiste una relazione algebrica diretta che collega la funzione segno al valore assoluto. Per ogni $x \neq 0,$ vale la seguente identità:

$$
\mathrm{sgn}(x) = \frac{x}{|x|} \tag{3}
$$

La $(3)$ concorda con la definizione della funzione segno data nella $(1)$. Infatti, quando $x > 0,$ il rapporto è pari a $1,$ quando $x < 0,$ il rapporto è $-1,$ e in $x = 0,$ il rapporto non è definito e il valore $\mathrm{sgn}(0) = 0$ viene assegnato per convenzione. Dalla $(3)$ si deriva anche che il valore assoluto può essere espresso mediante la funzione segno, attraverso la seguente relazione che vale per ogni $x \in \mathbb{R},$ compreso $x = 0,$ per il quale entrambi i membri sono nulli:

$$
|x| = x \cdot \mathrm{sgn}(x) \tag{4}
$$

Dalla $(4)$ si ricavano altre due identità. La prima esprime ogni numero reale come prodotto del suo valore assoluto e del suo segno come:

$$
x = |x| \cdot \mathrm{sgn}(x) \tag{5}
$$

La seconda usa l'uguaglianza $|x| = \sqrt{x^2},$ valida per ogni $x \in \mathbb{R},$ e fornisce un'espressione alternativa della funzione segno per $x \neq 0$ data dalla seguente uguaglianza:

$$
\mathrm{sgn}(x) = \frac{x}{\sqrt{x^2}} \tag{6}
$$
- - -

Un'altra relazione algebrica fondamentale, lega la funzione segno con la funzione gradino di Heaviside $H(x)$ che è definita come:

$$ \tag{7}
H(x) =
\begin{cases}
0 & \text{se } x < 0 \\[6pt]
\dfrac{1}{2} & \text{se } x = 0 \\[8pt]
1 & \text{se } x > 0
\end{cases}
$$

Il grafico della $(7)$ è rappresentato nella seguente figura e come si può vedere presenta una somiglianza con quello della funzione segno:

![IMG. 2](../svg/sign-function-2.svg)

Le due funzioni sono infatti legate dalla seguente trasformazione:

$$
\mathrm{sgn}(x) = 2H(x) - 1 \tag{8}
$$

Equivalentemente, dalla $(8)$ si deriva che la funzione di Heaviside è ottenuta dalla funzione segno attraverso la seguente trasformazione:

$$
H(x) = \frac{1 + \mathrm{sgn}(x)}{2}
$$
