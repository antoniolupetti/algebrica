---
title: Anelli
source: https://algebrica.org/rings/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - commutative-ring
  - distributivity
  - homomorphism
  - ideal
  - integral-domain
  - polynomial-ring
  - ring-theory
  - subring
  - zero-divisor
---

## Definizione

Un anello è un insieme $R$ dotato di due operazioni binarie, l'addizione e la moltiplicazione. Rispetto all'addizione, $(R,+)$ è un gruppo abeliano. L'anello si indica con la terna:

$$(R, +, \cdot) \tag{1}$$

Indicando con $0$ l'elemento neutro e con $-a$ l'opposto di $a,$ per ogni $a \in R$ si hanno le seguenti relazioni:

$$
\begin{align}
a + 0 &= a \notag\\[6pt]
a + (-a) &= 0 \tag{2}
\end{align}
$$

La moltiplicazione è associativa e distributiva rispetto all'addizione. Per ogni $a, b, c \in R$ valgono le seguenti identità:

$$
\begin{align}
(a \cdot b) \cdot c &= a \cdot (b \cdot c) \tag{3}\\[6pt]
a \cdot (b + c) &= a \cdot b + a \cdot c \tag{4}\\[6pt]
(a + b) \cdot c &= a \cdot c + b \cdot c \tag{5}
\end{align}
$$

Un anello è commutativo quando per ogni $a, b \in R$ vale:

$$a \cdot b = b \cdot a$$

Si definisce invece unitario quando esiste un elemento neutro moltiplicativo $1 \in R$ tale che, per ogni $a \in R$ vale la seguente identità:

$$1 \cdot a = a \cdot 1 = a$$

Un esempio di anello è l'insieme $2\mathbb{Z}$ degli interi pari, in quanto questi formano un gruppo abeliano rispetto all'addizione e il loro prodotto è ancora pari. L'associatività della moltiplicazione e le leggi distributive valgono perché le operazioni sono quelle di $\mathbb{Z}.$ Questo anello è privo di unità, poiché un elemento neutro moltiplicativo $e$ dovrebbe soddisfare $2e = 2,$ da cui $e = 1,$ che però non è pari. I numeri naturali $\mathbb{N},$ invece, non formano un anello rispetto alle operazioni usuali, perché l'opposto di $1$ non appartiene a $\mathbb{N}.$

Le leggi distributive $(4)$ e $(5)$ determinano come si comporta lo zero rispetto alla moltiplicazione. Poiché $0 + 0 = 0,$ per ogni $a \in R$ si ha:

$$
\begin{align}
a \cdot 0 &= a \cdot (0 + 0) = a \cdot 0 + a \cdot 0 \\[6pt]
0 \cdot a &= (0 + 0) \cdot a = 0 \cdot a + 0 \cdot a
\end{align}
$$

Sottraendo da entrambi i membri della prima uguaglianza $a \cdot 0$ e da quelli della seconda $0 \cdot a,$ si ottiene:

$$a \cdot 0 = 0 \cdot a = 0 \tag{6}$$

Dalla $(6)$ e dalle leggi distributive $(4)$ e $(5)$ segue che, sostituendo un fattore con il suo opposto, si ottiene l'opposto del prodotto. Infatti, per ogni $a, b \in R,$ raccogliendo $b$ a destra nella prima riga e $a$ a sinistra nella seconda si ottiene:

$$
\begin{align}
a \cdot b + (-a) \cdot b &= (a + (-a)) \cdot b = 0 \\[6pt]
a \cdot b + a \cdot (-b) &= a \cdot (b + (-b)) = 0
\end{align}
$$

Poiché l'opposto di $a \cdot b$ è unico, segue che:

$$(-a) \cdot b = a \cdot (-b) = -(a \cdot b) \tag{7}$$

Se $a$ e $b$ sono interi positivi, la $(7)$ spiega perché il prodotto diventa negativo quando si sostituisce uno dei fattori con il suo opposto. In qualunque anello, applicando due volte la $(7)$ si ottiene:

$$(-a)(-b) = -(a(-b)) = -(-(ab)) = ab \tag{8}$$

Se $R$ è un anello unitario, ponendo $a = 1$ nella $(7)$ si vede che moltiplicare un elemento $b \in R$ per $-1$ dà il suo opposto:

$$(-1) \cdot b = -(1 \cdot b) = -b \tag{9}$$

In particolare, per $b = -1$ la $(9)$ dà $(-1)(-1) = 1,$ quindi $-1$ è il proprio inverso moltiplicativo. In generale, un elemento $u$ di un anello unitario $R$ si dice invertibile se esiste $v \in R$ tale che:

$$uv = vu = 1 \tag{10}$$

L'elemento inverso di un anello è unico e si indica con $u^{-1}$ e il loro insieme forma il gruppo $R^\times$ rispetto alla moltiplicazione. Per esempio, in $\mathbb{Z}$ gli unici elementi invertibili sono $1$ e $-1,$ perché un prodotto di interi $uv = 1$ richiede che valga:

$$|u| = |v| = 1$$

Un elemento non nullo $a \in R$ si dice divisore dello zero se esiste un valore $b \neq 0$ in $R$ tale che valga una delle seguenti condizioni:

$$
\begin{align}
ab &= 0 \\[6pt]
ba &= 0
\end{align}
$$

Infine, introduciamo il concetto di dominio d'integrità che si riferisce a un anello commutativo in cui l'unità $1$ è distinta dallo zero e non esistono divisori dello zero e cioè, se $ab = 0,$ almeno uno dei due fattori deve essere zero.

## Anelli commutativi e non commutativi

Confrontiamo alcuni anelli per vedere quali elementi ammettono un inverso moltiplicativo, quando il prodotto di due elementi non nulli può essere zero e quando l'ordine dei fattori cambia il risultato. Consideriamo l'insieme $\mathbb{Z}$ che con le operazioni usuali è un dominio d'integrità perché è un anello commutativo con unità e il prodotto di due interi non nulli è sempre non nullo. Tuttavia, il numero $2$ non ha inverso in $\mathbb{Z}.$ Negli anelli $\mathbb{Q},$ $\mathbb{R}$ e $\mathbb{C},$ invece, ogni elemento non nullo è invertibile, perciò questi tre anelli sono campi.

Anche l'anello dei polinomi reali $\mathbb{R}[x]$ è un dominio d'integrità. La moltiplicazione è commutativa e ha per elemento neutro il polinomio costante $1.$ Inoltre, quando due polinomi sono non nulli, il coefficiente del termine di grado massimo del loro prodotto è il prodotto dei rispettivi coefficienti direttivi. Poiché tale coefficiente è non nullo, anche il prodotto è non nullo.

Consideriamo ora il caso di funzioni reali definite su un insieme $X.$ Queste formano un anello commutativo rispetto alla somma e al prodotto definiti punto per punto. Infatti, per ogni $x \in X$ si ha:

$$
\begin{align}
(f + g)(x) &= f(x) + g(x) \\[6pt]
(fg)(x) &= f(x)g(x)
\end{align}
$$

Poiché il prodotto si calcola punto per punto, moltiplicare $f$ per la funzione costante di valore $1$ lascia invariato ogni valore $f(x).$ Questa funzione costante è quindi l'elemento neutro del prodotto, per cui la $(10)$ richiede che $f(x)g(x) = 1$ per ogni $x \in X.$ Da questo segue che $f$ è invertibile se e solo se non si annulla mai, e in tal caso la sua inversa moltiplicativa è la funzione $x \mapsto 1/f(x).$

Anche le classi di resto modulo un intero $n \geq 2$ formano un anello, in particolare l'anello commutativo $\mathbb{Z}/n\mathbb{Z},$ con unità $[1].$ Se $n$ è primo, ogni classe non nulla ha un inverso e l'anello diventa un campo. In $\mathbb{Z}/6\mathbb{Z},$ invece, si ha $[2][3] = [6] = [0],$ poiché $2 \cdot 3$ è un multiplo di $6.$ Le classi $[2]$ e $[3]$ sono dunque divisori dello zero perché ciascuna è non nulla e dà prodotto zero quando viene moltiplicata per l'altra.

Vediamo infine il caso dell'anello $\mathrm{M}_n(F)$ delle matrici quadrate su un campo $F,$ in cui l'unità è la matrice identità $I_n.$ Per $n \geq 2$ l'ordine dei fattori può cambiare il prodotto riga per colonna, come mostrano le seguenti matrici di ordine $2$:

$$A = \begin{pmatrix}0 & 1 \\ 0 & 0\end{pmatrix}, \qquad B = \begin{pmatrix}1 & 0 \\ 0 & 0\end{pmatrix} \tag{11}$$

Il loro prodotto dà un risultato diverso a seconda dell'ordine con cui viene eseguito, e infatti si ha:

$$
\begin{align}
AB &= \begin{pmatrix}0 & 0 \\ 0 & 0\end{pmatrix} \\[6pt]
BA &= \begin{pmatrix}0 & 1 \\ 0 & 0\end{pmatrix} = A
\end{align}
$$

Poiché $A$ e $B$ sono non nulle e $AB = 0,$ entrambe sono divisori dello zero, e inoltre $BA \neq AB,$ quindi l'anello non è commutativo. Per $n \gt 2$ si ottiene lo stesso risultato completando le due matrici con righe e colonne di zeri.

## Sottoanelli e ideali

Dopo aver visto come si opera in un anello, chiediamoci quando sia possibile restringere le operazioni a un suo sottoinsieme e ottenere ancora un anello. Un sottoinsieme $S$ di un anello $R$ con questa proprietà si chiama sottoanello di $R.$ Per esempio, nell'anello delle matrici quadrate reali di ordine $n,$ le matrici a coefficienti razionali formano un sottoanello, perché somme, differenze e prodotti di queste matrici hanno ancora coefficienti razionali. Per verificare che un sottoinsieme non vuoto $S \subseteq R$ sia un sottoanello, è necessario e sufficiente che, per ogni $a, b \in S,$ valgano entrambe le condizioni:

$$
\begin{align}
a - b &\in S \notag\\[6pt]
ab &\in S \tag{12}
\end{align}
$$

Nella $(12),$ la chiusura rispetto alla sottrazione rende $S$ un sottogruppo di $(R, +),$ mentre la seconda condizione garantisce che anche il prodotto appartenga a $S.$ Ogni anello $R$ ha come sottoanelli sia $\{0\},$ formato dal solo zero, sia l'intero anello $R$ e questi anelli coincidono quando $R$ contiene soltanto lo zero. Un sottoanello di $R$ si dice proprio se esclude almeno un elemento di $R.$ Per esempio, gli interi pari $2\mathbb{Z}$ formano un sottoanello proprio di $\mathbb{Z}$ perché la differenza e il prodotto di due interi pari sono ancora pari e perché tra essi non compare $1.$ Applichiamo ora il criterio $(12)$ alle matrici triangolari superiori, partendo da un esempio di ordine $2$:

$$A = \begin{pmatrix}1 & 2 \\ 0 & 1\end{pmatrix}, \qquad B = \begin{pmatrix}2 & 1 \\ 0 & 3\end{pmatrix}$$

Calcoliamo la differenza e il prodotto indicati nella $(12)$ e otteniamo:

$$
\begin{align}
A-B &= \begin{pmatrix}-1 & 1 \\ 0 & -2\end{pmatrix} \\[6pt]
AB &= \begin{pmatrix}2 & 7 \\ 0 & 3\end{pmatrix}
\end{align}
$$

In generale, se $A$ e $B$ sono triangolari superiori e $i \gt j,$ la voce $a_{ij}-b_{ij}$ è zero. Anche nella voce $(AB)_{ij}$ ogni termine $a_{ik}b_{kj}$ è nullo, perché per $k \lt i$ si ha $a_{ik}=0,$ mentre per $k \geq i \gt j$ si ha $b_{kj}=0.$ La differenza e il prodotto sono quindi triangolari superiori e, poiché anche la matrice nulla è triangolare superiore, la $(12)$ garantisce che queste matrici formano un sottoanello.

Nell'anello delle funzioni da $\mathbb{R}$ a $\mathbb{R},$ le funzioni continue formano un sottoanello perché la differenza e il prodotto di due funzioni continue sono continui.

Un ideale è un sottoanello $I$ di un anello $R$ tale che, per ogni $a \in I$ e ogni $r \in R,$ valgono le seguenti condizioni:

$$
\begin{align}
ra &\in I\\[6pt]
ar &\in I
\end{align}
$$

La prima condizione definisce un ideale sinistro, la seconda un ideale destro. Se valgono entrambe, l'ideale si dice bilatero. In un anello commutativo si ha $ra = ar,$ quindi ogni ideale sinistro è anche destro e viceversa, per cui ogni ideale unilatero è anche bilatero.

Per esempio, gli interi pari formano un ideale bilatero di $\mathbb{Z}$ perché il prodotto di un intero pari per un intero qualsiasi è ancora pari.
