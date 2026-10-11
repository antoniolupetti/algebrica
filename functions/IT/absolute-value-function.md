---
title: Absolute Value Function
source: https://algebrica.org/absolute-value-function/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - continuity
  - corner-point
  - even-function
  - graph-transformation
  - non-differentiability
  - sign-function
---

## Definizione

Prima di affrontare la funzione valore assoluto, richiamiamo brevemente il concetto di valore assoluto di un numero reale $x,$ che viene indicato con $|x|$ ed è definito in base al segno di $x$ nel seguente modo:

$$ \tag{1}
|x| =
\begin{cases}
+x & \text{se } x \geq 0 \\[6pt]
-x & \text{se } x < 0
\end{cases}
\quad \forall \ x \in \mathbb{R}
$$

In altri termini, il valore assoluto di un numero reale $x$ rappresenta la sua distanza dallo zero sulla retta reale ed è quindi un valore sempre non negativo. Nella figura seguente, ad esempio, i punti $-1$ e $2$ distano dallo zero rispettivamente $1$ e $2$ unità, perciò $|-1| = 1$ e $|2| = 2.$

![IMG. 1](../../numbers/svg/real-numbers-1.svg)

Più in generale, la distanza tra due punti $x$ e $a$ è data da $|x - a|$ e vale la seguente uguaglianza:

$$|x-a| = |a-x| \tag{2}$$

Dalla $(2),$ poiché $a - x = -(x - a)$ vale anche:

$$|a - x| = |-(x - a)| = |x - a|$$


Fatta questa premessa, possiamo introdurre la funzione valore assoluto, che associa a ogni numero reale $x$ il suo valore assoluto $|x|$ e, in coerenza con la $(1)$ è definita a tratti come:

$$ \tag{3}
y = |x| =
\begin{cases}
+x & \text{se } x \geq 0 \\[6pt]
-x & \text{se } x < 0
\end{cases}
$$

![IMG. 2](../../numbers/svg/absolute-value-1.svg)

Il suo grafico è formato da due semirette che si incontrano nell'origine del piano cartesiano ed è simmetrico rispetto all'asse delle ordinate, quindi la funzione è pari e soddisfa l'identità:

$$|{-x}| = |x| \quad \text{per ogni } x \in \mathbb{R}$$

## Proprietà

Dalla $\tag{3}$ si ricavano le principali proprietà della funzione valore assoluto, che riportiamo di seguito.

+ Dominio: $\mathbb{R}$
+ Immagine: $\mathbb{R}^+_0$
+ Per quanto riguarda la monotonia, la funzione è decrescente su $(-\infty, 0]$ e crescente su $[0, +\infty).$
+ La funzione è pari, poiché $|{-x}| = |x|.$
+ La funzione è continua su tutta la retta reale $\mathbb{R}.$
+ La funzione è derivabile in ogni punto tranne che in $x = 0,$ dove presenta un punto angoloso.
+ La funzione ha un minimo assoluto in $x = 0,$ dove $|x| = 0,$ e non ha massimo.
+ I limiti agli estremi del dominio sono:

$$
\begin{align}
\lim_{x \to -\infty} |x| &= +\infty \\[6pt]
\lim_{x \to +\infty} |x| &= +\infty
\end{align}
$$

Il grafico del valore assoluto di una funzione si ottiene attraverso una trasformazione, riflettendo rispetto all'asse delle $x$ le parti del grafico originario che si trovano al di sotto di tale asse. Consideriamo, ad esempio, il grafico della parabola definita dall'equazione:

$$y = x^2 - 1 \tag{4}$$

![IMG. 3](../svg/absolute-value-function-1.svg)

Studiando il segno della funzione verifichiamo che la $(4)$ è negativa nell'intervallo tra $-1$ e $1$, ovvero quando vale la seguente disequazione:

$$x^2 - 1 < 0$$
Applichiamo ora una trasformazione alla $(4)$ tale che valga:

$$f(x) = |x^2 - 1|$$

Per tracciare il grafico di questa funzione manteniamo invariate le parti del grafico che sono maggiori o uguali di zero, mentre riflettiamo quelle negative, ovvero quelle comprese proprio nell'intervallo tra $-1$ e $1$ ottenendo:

![IMG. 4](../svg/absolute-value-function-2.svg)


## Limiti, derivate e integrali della funzione valore assoluto

Analizziamo ora alcuni elementi utili della funzione valore assoluto che si incontrano nel calcolo dei limiti, quello differenziale ed integrale. Partiamo innanzitutto da un limite notevole della funzione valore assoluto:

$$\lim_{x \to 0} \frac{|x|}{x} \tag{5}$$

L'esistenza del limite richiede che i limiti sinistro e destro coincidano. In questo caso, invece, i due limiti laterali sono diversi, quindi il limite non esiste:

$$
\begin{align}
\lim_{x \to 0^-} \frac{|x|}{x} &= -1 \\[6pt]
\lim_{x \to 0^+} \frac{|x|}{x} &= 1
\end{align}
$$

Quindi, poiché i due limiti laterali del rapporto incrementale sono diversi, $|x|$ non è derivabile in $x = 0.$ Per quanto riguarda la derivata, derivando ciascun ramo della funzione valore assoluto, otteniamo la seguente espressione a tratti della sua derivata:

$$
\frac{d}{dx} |x| =
\begin{cases}
1 & \text{se } x > 0 \\[6pt]
-1 & \text{se } x < 0
\end{cases}
$$

Poiché come abbiamo visto non esiste il limite in $x=0$, la derivata non esiste in $x = 0,$ perché in quel punto la funzione presenta un punto angoloso. L'integrale indefinito della funzione valore assoluto è:

$$\int |x| \ dx = \frac{x^2 \cdot \mathrm{sgn}(x)}{2} + c \tag{6}$$

Nella $(6)$ compare la funzione segno, che consente di riunire in un'unica espressione i due rami della primitiva è definita da:

$$
\mathrm{sgn}(x) =
\begin{cases}
-1 & \text{se } x < 0 \\[6pt]
0 & \text{se } x = 0 \\[6pt]
1 & \text{se } x > 0
\end{cases}
$$
