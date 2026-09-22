---
title: Finding Areas by Integration
source: https://algebrica.org/finding-areas-by-integration/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - area-between-curves
  - continuous-functions
  - definite-integral
  - even-and-odd-functions
  - integration
  - linearity
  - riemann-integral
---
## Il calcolo delle aree mediante integrali definiti

Sappiamo che il calcolo delle aree è una delle applicazioni degli [integrali definiti](../definite-integrals/) e che quando una funzione è non negativa su un intervallo, il suo integrale definito coincide con l'area compresa tra il grafico e l'asse delle ascisse. Questa stessa idea si può applicare abbastanza agevolmente anche nel caso in cui si voglia calcolare l'area tra due curve qualsiasi con qualche piccola accortezza di cui tener conto.

Consideriamo due [funzioni continue](../continuous-functions/) $f$ e $g$ su un [intervallo](../intervals/) $[a,b],$ con $a < b,$ e supponiamo che $f(x) \geq g(x)$ su tutto l'intervallo. L'area che vogliamo misurare è delimitata superiormente dal grafico di $f$ e inferiormente da quello di $g$ mentre le rette $x = a$ e $x = b$ rappresentano il bordo sinistro e destro della nostra regione quando le curve non si incontrano agli estremi. Utilizzando l'integrale definito, l'area di questa regione si calcola semplicemente con la formula:

$$A = \int_a^b [f(x) - g(x)] \ dx \tag{1}$$

È importante ricordare che la scelta dell'ordine nella differenza all'interno dell'integrale dipende naturalmente dalla posizione delle curve e poiché l'altezza della regione deve essere non negativa in ogni punto dell'intervallo, sottraiamo la funzione inferiore da quella superiore. Non occorre invece che le due funzioni siano entrambe positive, e la formula $(1)$ rimane valida anche quando una o entrambe si trovano sotto l'asse delle ascisse.

Un primo esempio banale è dato dalla regione compresa tra le rette $y = 2$ e $y = -1$ per $x \in [0,3].$ La distanza verticale tra le rette è costante e vale $2 - (-1) = 3.$ Applicando la $(1)$ otteniamo:

$$A = \int_0^3 [2 - (-1)] \ dx = [3x]_0^3 = 9$$

Il risultato coincide quindi con l'area di un rettangolo di base $3$ e altezza $3.$ Tuttavia i casi pratici sono tipicamente meno affabili, e in genere l'altezza tra due curve varia con $x,$ e pertanto l'integrale deve tenere conto di questa variazione su tutto l'intervallo in cui andiamo a calcolare l'area.

## Interpretazione geometrica

Per comprendere meglio da dove proviene la formula $(1),$ consideriamo la regione ombreggiata compresa tra le due curve date dalle funzioni $f$ e $g$:

![Img. 1](svg/finding-areas-by-integration-1.svg)

Un banale prodotto base per altezza, come nel caso del rettangolo, in questo caso non si può utilizzare, in quanto, come si vede dalla figura, l'altezza della regione varia al variare di $x$ tra $a$ e $b$. Suddividiamo allora $[a,b]$ in piccoli sottointervalli di ampiezza $\Delta x_i$ e scegliamo un punto $\xi_i$ tale che, su ogni sottointervallo, possiamo approssimare la porzione di regione con un rettangolo di base $\Delta x_i$ e altezza $f(\xi_i) - g(\xi_i).$ Sommando le aree di questi rettangoli otteniamo:

$$A \approx \sum_{i=1}^{n} [f(\xi_i) - g(\xi_i)]\Delta x_i$$

Poiché $f$ e $g$ sono continue, anche la differenza $f - g$ è continua e [integrabile secondo Riemann](../riemann-integrability-criteria/), e quando l'ampiezza dei sottointervalli tende a zero queste somme convergono all'integrale definito di $f - g.$ In questo modo si ottiene la formula $(1)$ che può anche essere riscritta sfruttando la linearità dell'integrale:

$$A = \int_a^b f(x) \ dx - \int_a^b g(x) \ dx \tag{2}$$

Questa uguaglianza esprime l'area cercata come differenza di due integrali calcolati sullo stesso intervallo. Attenzione però al fatto che se una funzione assume valori negativi, il suo integrale è un'area con segno, quindi non coincide necessariamente con l'area geometrica compresa tra il suo grafico e l'asse delle ascisse. La differenza resta corretta perché, in ogni punto, $f(x) - g(x)$ misura la distanza verticale tra i grafici. La forma che non richiede di stabilire quale curva si trovi sopra l'altra, è:

$$A = \int_{a}^{b} |f(x) - g(x)| \ dx \tag{3}$$

## Aree tra curve che si intersecano

Fin qui abbiamo supposto che le due curve si trovino una sopra all'altra 
su tutto l'intervallo. Quando questa condizione viene meno, per calcolare correttamente l'area dobbiamo capire dove cambia il segno di $f(x) - g(x)$ prima di lanciarci nei calcoli. Se l'intervallo non è assegnato, i punti nei quali le curve si incontrano, determinano gli estremi dell'intervallo e si calcolano ponendo semplicemente $f(x) = g(x).$

A questo punto bisogna però prestare molta attenzione perché due intersezioni consecutive possono delimitare una regione, mentre più intersezioni possono dare luogo a più regioni da considerare separatamente o insieme.

Supponiamo, ad esempio, che le curve si scambino la posizione (sopra / sotto) in un punto $c \in (a,b).$ Formalmente abbiamo questa situazione: $f(x) \geq g(x)$ su $[a,c]$ e $g(x) \geq f(x)$ su $[c,b].$ La situazione è rappresentata nell'immagine seguente:


![Img. 2](svg/finding-areas-by-integration-2.svg)

In questo caso, l'integrale di $f - g$ su tutto $[a,b]$ avrebbe con segno positivo la prima regione e con segno negativo la seconda. Per ottenere quindi l'area geometrica dobbiamo sommare i due contributi non negativi, invertendo l'ordine della differenza dopo il punto $c.$ Scriviamo quindi:

$$A = \int_a^c [f(x) - g(x)] \ dx + \int_c^b [g(x) - f(x)] \ dx \tag{4}$$

La stessa costruzione si applica quando i cambi di segno sono più di uno. Ecco spiegato il motivo perché nella $(3)$ si ricorre al [valore assoluto](../absolute-value/) che fornisce la distanza verticale tra le curve indipendentemente dal loro ordine. Per calcolare l'integrale mediante primitive, in genere occorre comunque studiare il segno di $f - g$ e riscrivere il valore assoluto nei diversi sottointervalli.

> C'è da notare che un punto di intersezione non comporta necessariamente uno scambio di posizione. I grafici di $f(x) = x^2$ e $g(x) = 0$ si incontrano nell'origine, ma $f(x) \geq g(x)$ su entrambi i lati. La suddivisione serve solo quando cambia il segno della differenza, o quando cambia l'espressione del bordo della regione.

## Esempio 1

Applichiamo il metodo finora descritto alle curve $y = e^x$ e $y = x^2 - 1$ sull'intervallo $[-1,1].$ In questo caso gli estremi dell'intervallo sono già assegnati, quindi dobbiamo stabilire quale curva si trovi sopra e quale sotto. Il grafico della regione è il seguente:

![Img. 3](svg/finding-areas-by-integration-3.svg)

La funzione $e^x$ è positiva per ogni $x,$ mentre $x^2 - 1 \leq 0$ su $[-1,1],$ pertanto il grafico dell'esponenziale è quindi superiore a quello della parabola su tutto l'intervallo. Per la formula $(1)$ otteniamo:

$$A = \int_{-1}^{1} [e^x - (x^2 - 1)] \ dx$$

Per nostra fortuna è un integrale più semplice di quanto non potesse sembrare all'inizio. Possiamo quindi risolverlo procedendo con pochi e semplici passaggi:

$$
\begin{align}
A &= \int_{-1}^{1} (e^x - x^2 + 1) \ dx \\[6pt]
  &= \left[e^x - \frac{x^3}{3} + x\right]_{-1}^{1} \\[6pt]
  &= \left(e - \frac{1}{3} + 1\right) - \left(e^{-1} + \frac{1}{3} - 1\right) \\[6pt]
  &= e - \frac{1}{e} + \frac{4}{3}
\end{align}
$$

Abbiamo quindi trovato l'area compresa tra le due curve nell'intervallo assegnato che è dunque pari a $e - 1/e + 4/3.$

## Esempio 2

Consideriamo adesso le curve $f(x) = x^3 - 3x$ e $g(x) = x$ e calcoliamo sempre l'area delle regioni racchiuse dai loro grafici. L'intervallo in questo caso non è assegnato, perciò dobbiamo trovare i punti di intersezione, ponendo $f(x) = g(x)$:

$$
\begin{align}
x^3 - 3x &= x \\[6pt]
x^3 - 4x &= 0 \\[6pt]
x(x - 2)(x + 2) &= 0
\end{align}
$$

La fattorizzazione ci consente di individuare immediatamente le soluzioni che sono $x = -2,$ $x = 0$ e $x = 2.$ Le curve delimitano quindi due regioni, una sull'intervallo $[-2,0]$ e l'altra su $[0,2].$ Per impostare i rispettivi integrali studiamo adesso il segno della differenza:

$$f(x) - g(x) = x(x - 2)(x + 2)$$

Per $-2 < x < 0$ i primi due fattori sono negativi e il terzo è positivo, quindi il prodotto è positivo. Su questo intervallo $f$ è la funzione superiore. Per $0 < x < 2$ soltanto il fattore $x - 2$ è negativo, quindi il prodotto è negativo e la funzione superiore è $g.$ Applicando la $(4)$ scriviamo:

$$A = \int_{-2}^{0} (x^3 - 4x) \ dx + \int_0^2 (4x - x^3) \ dx$$

Calcoliamo separatamente i due contributi. Per la regione a sinistra dell'origine otteniamo:

$$
\begin{align}
A_1 &= \left[\frac{x^4}{4} - 2x^2\right]_{-2}^{0} \\[6pt]
    &= 0 - (4 - 8) \\[6pt]
    &= 4
\end{align}
$$

Per la regione a destra dell'origine la differenza ha segno opposto, e il calcolo dà:

$$
\begin{align}
A_2 &= \left[2x^2 - \frac{x^4}{4}\right]_0^2 \\[6pt]
    &= (8 - 4) - 0 \\[6pt]
    &= 4
\end{align}
$$

L'area totale delle due regioni è quindi $A = A_1 + A_2 = 8.$

Notate che le due aree sono uguali perché $f$ e $g$ sono entrambe [funzioni dispari](../even-and-odd-functions/). In questo caso avremmo perciò potuto calcolare soltanto l'area su $[0,2]$ e raddoppiarla. Capite quindi che il cambio di segno è fondamentale perché se avessimo integrato $f - g$ su tutto $[-2,2]$ senza cambiare il segno, avremmo ottenuto zero, perché i due contributi si sarebbero cancellati.

## Integrazione rispetto a $y$

In molte situazioni la descrizione mediante sottointervalli verticali non è sempre la più comoda. Alcune regioni hanno un bordo sinistro e un bordo destro espressi direttamente come funzioni di $y$ e in questi casi è conveniente usare sezioni orizzontali piuttosto che verticali e integrare rispetto all'asse delle $y$.

Ad esempio, supponiamo di avere due funzioni $p$ e $q$ continue su $[c,d],$ con $c < d$ e $p(y) \geq q(y)$ su tutto l'intervallo. Consideriamo la regione delimitata a destra da $x = p(y),$ a sinistra da $x = q(y)$ e dalle rette $y = c$ e $y = d.$ La lunghezza di ogni sezione orizzontale è $p(y) - q(y),$ quindi l'area è:

$$A = \int_c^d [p(y) - q(y)] \ dy \tag{5}$$

Il ragionamento è lo stesso usato per la $(1),$ ma stavolta con le coordinate scambiate. Prima sottraevamo il bordo inferiore da quello superiore, adesso sottraiamo il bordo sinistro da quello destro. La scelta della variabile dipende dunque dalla forma della regione e dalle funzioni da integrare. Se una descrizione richiede di cambiare l'espressione di un bordo, mentre l'altra permette di mantenere gli stessi due bordi su tutto l'intervallo, la seconda può ridurre il numero di integrali necessari.

> Piccola nota, non del tutto marginale: per riscrivere una curva $y = f(x)$ nella forma $x = f^{-1}(y)$ occorre che $f$ sia [invertibile](../inverse-function/) sul tratto considerato. Se non lo è, può essere necessario distinguere più rami, come accade per la parabola $x = y^2,$ che fornisce $y = \sqrt{x}$ e $y = -\sqrt{x}.$

## Esempio 3

Calcoliamo l'area racchiusa dalla parabola $x = y^2$ e dalla retta $x = y + 2.$ Entrambe le curve sono espresse come funzioni di $y,$ quindi proviamo a usare la formula $(5).$ Anche in questo caso, come per l'esempio 2, gli estremi di integrazione non sono esplicitati e per trovarli dobbiamo uguagliare le due espressioni di $x:$

$$
\begin{align}
y^2 &= y + 2 \\[6pt]
y^2 - y - 2 &= 0 \\[6pt]
(y - 2)(y + 1) &= 0
\end{align}
$$

Le ordinate delle intersezioni sono $y = -1$ e $y = 2.$ Su questo intervallo la differenza tra l'ascissa della retta e quella della parabola è:

$$y + 2 - y^2 = (2 - y)(y + 1)$$

Entrambi i fattori sono non negativi per $-1 \leq y \leq 2.$ La retta è quindi il bordo destro e la parabola quello sinistro. Sottraendo in questo ordine e integrando otteniamo:

$$
\begin{align}
A &= \int_{-1}^{2} (y + 2 - y^2) \ dy \\[6pt]
  &= \left[\frac{y^2}{2} + 2y - \frac{y^3}{3}\right]_{-1}^{2} \\[6pt]
  &= \left(2 + 4 - \frac{8}{3}\right) - \left(\frac{1}{2} - 2 + \frac{1}{3}\right) \\[6pt]
  &= \frac{10}{3} + \frac{7}{6} = \frac{9}{2}
\end{align}
$$

L'area della regione racchiusa dalle due curve è quindi $9/2.$

- - -

Vediamo ora come cambia il calcolo usando sottointervalli verticali. La parabola fornisce i due rami $y = \pm\sqrt{x},$ mentre la retta diventa $y = x - 2.$ La regione si estende da $x = 0$ a $x = 4.$ Su $[0,1]$ il bordo inferiore è $y = -\sqrt{x};$ su $[1,4]$ è invece $y = x - 2.$ Il bordo superiore è $y = \sqrt{x}$ su entrambi gli intervalli. L'area è quindi data da

$$A = \int_0^1 2\sqrt{x} \ dx + \int_1^4 (\sqrt{x} - x + 2) \ dx$$

Anche questo integrale è relativamente semplice e la primitiva si calcola con la regola delle potenze:

$$
\begin{align}
A &= \left[\frac{4}{3}x^{3/2}\right]_0^1 + \left[\frac{2}{3}x^{3/2} - \frac{x^2}{2} + 2x\right]_1^4 \\[6pt]
  &= \frac{4}{3} + \frac{16}{3} - \left(\frac{2}{3} - \frac{1}{2} + 2\right) \\[6pt]
  &= \frac{4}{3} + \frac{19}{6} = \frac{9}{2}
\end{align}
$$

Come vedete il risultato è identico a quello ottenuto con i sottointervalli orizzontali.

## Alcune considerazioni pratiche finali

Come avete visto, il calcolo dell'area tra due curve tramite integrazione non è complicato. Al di là dei calcoli, la parte che richiede più attenzione è capire come è fatta la regione. Conviene quindi per prima cosa individuare i bordi e scegliere se integrarli rispetto a $x$ oppure a $y.$

A questo punto se l'intervallo non è assegnato, si trovano le intersezioni e si selezionano quelle che delimitano la regione richiesta. Quando le intersezioni sono più di due, occorre sempre distinguere l'area di una singola regione dalla somma delle aree di tutte le regioni racchiuse. Tra due intersezioni consecutive, la differenza di due funzioni continue non ha zeri e mantiene segno costante. In questo caso basta valutarla in un punto interno per determinarne il segno su tutto il sottointervallo.

Una volta individuato come è fatta la regione si imposta ciascun integrale sottraendo il bordo inferiore da quello superiore, oppure quello sinistro da quello destro. Se l'ordine o l'espressione dei bordi cambia, si suddivide il calcolo nei tratti corrispondenti. Attenzione però che la sola presenza di un'intersezione non impone necessariamente di invertire la differenza, perché si può presentare il caso di due grafici che si toccano in uno o più punti senza però attraversarsi.

Non resta altro che calcolare l'integrale e determinare quindi il valore dell'area.
