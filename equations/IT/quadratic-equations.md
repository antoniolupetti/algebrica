---
title: Quadratic Equations
source: https://algebrica.org/quadratic-equations/
license: CC BY-NC 4.0
tags:
  - discriminant
  - parabola
  - quadratic-equation
  - quadratic-formula
  - vieta-formulas
---
## Introduzione

Un'equazione di secondo grado è un'equazione polinomiale di grado due in una sola incognita. La sua forma standard è la seguente:

$$ax^2 + bx + c = 0 \tag{1}$$

In questa espressione $a,$ $b$ e $c$ sono coefficienti reali, con $a \neq 0,$ mentre $x$ è l'incognita. Il coefficiente $a$ moltiplica il termine quadratico $x^2,$ il coefficiente $b$ moltiplica il termine lineare $x$ e $c$ è il termine noto. Quando $a = 0$ e $b \neq 0,$ la $(1)$ si riduce ad un'equazione di primo grado della forma $bx + c = 0.$ Se $a$ e $b$ sono entrambi pari a zero, l'equazione contiene soltanto il termine costante e per $c \neq 0$ non ha soluzioni, mentre per $c=0$ ne ha infinite.

In linea generale, un'equazione di secondo grado è il caso più semplice di equazione trinomia, la cui forma standard è data dalla seguente espressione:

$$ax^{2n} + bx^{n} + c = 0 \tag{2}$$

Ponendo $n = 1$ nella $(2)$ si ottiene la $(1),$ mentre per $n \geq 2,$ l'equazione si può ricondurre a un'equazione di secondo grado nella variabile ausiliaria $y = x^n$ e risolvere con le stesse tecniche che vedremo più avanti in questa sezione.

Se alla $(1)$ sostituiamo il segno di uguaglianza con una delle relazioni $<,$ $>,$ $\leq$ o $\geq,$ si ottiene una disequazione di secondo grado, che si risolve studiando il segno della stessa espressione quadratica.

- - -

Dal punto di vista geometrico il grafico di $y = ax^2 + bx + c$ è una parabola. Questa corrispondenza è trattata più ampiamente nella voce sul significato geometrico delle equazioni di secondo grado.

![Fig. 1](../svg/quadratic-equations.svg)

È però utile richiamare in modo sintetico alcune caratteristiche peculiari. Quando il coefficiente $a > 0,$ la parabola ha la concavità rivolta verso l'alto e il suo vertice è il punto di minimo della funzione mentre quando $a < 0,$ la concavità è rivolta verso il basso e il vertice diventa il punto di massimo.

Le soluzioni reali della $(1)$ corrispondono alle ascisse dei punti in cui la parabola interseca l'asse delle $x.$ Possiamo avere tre casi, a seconda del segno del discriminante $\Delta = b^2 - 4ac$:

+ Per $\Delta > 0,$ la parabola interseca l'asse in due punti distinti.
+ Per $\Delta = 0,$ la parabola è tangente all'asse.
+ Per $\Delta < 0,$ la parabola non interseca l'asse e l'equazione non ha soluzioni reali.

> Quando $a = 0,$ l'espressione $y = bx + c$ descrive una retta. L'equazione associata $bx + c = 0$ è di primo grado solo se $b \neq 0.$

## Metodi risolutivi

Vediamo adesso il metodo risolutivo delle equazioni di secondo grado, che è piuttosto meccanico e semplice da applicare. Partiamo innanzitutto dalle equazioni di secondo grado incomplete ovvero le equazioni nella forma $(1)$ in cui uno dei coefficienti $b$ e $c$ è uguale a zero. In questo caso l'equazione assume una forma più semplice e può essere risolta direttamente, senza applicare la formula generale che vedremo tra poco e come descritto nella voce ad esse dedicata.

Nel caso tipico, invece, in cui tutti i coefficienti sono diversi da zero, il primo passo per risolvere un'equazione di secondo grado consiste nel ricondurla alla sua forma normale, ovvero alla $(1).$ Consideriamo, ad esempio, l'equazione $2x(x + 1) = x + 3.$ Svolgendo i calcoli otteniamo:

$$  
\begin{align}  
2x(x + 1) &= x + 3 \\[6pt]  
2x^2 + 2x &= x + 3 \\[6pt]  
2x^2 + x - 3 &= 0  
\end{align}  
$$

L'equazione è ora in forma normale, con i coefficienti ben determinati e pari ad $a = 2,$ $b = 1$ e $c = -3.$ In questo modo possiamo subito determinare la natura delle soluzioni, attraverso il calcolo del suo discriminante: 

$$\Delta = b^2 - 4ac \tag{3}$$

A seconda del valore della $(3)$ abbiamo i seguenti casi che è necessario imparare a memoria per risolvere correttamente questo tipo di equazioni.

+ Quando $\Delta > 0$ si ottengono due radici reali e distinte.
+ Quando $\Delta = 0$ si ottiene una radice reale di molteplicità due, ovvero due radici reali e coincidenti.
+ Quando $\Delta < 0$ non esiste una soluzione nel campo dei numeri reali, ma l'equazione ammette come soluzione una coppia di radici complesse coniugate. Il teorema fondamentale dell'algebra garantisce che un'equazione di secondo grado abbia sempre esattamente due radici in $\mathbb{C},$ contate con la loro molteplicità.

- - -

Una volta calcolato il discriminante possiamo applicare la formula risolutiva delle equazioni di secondo grado che permette di calcolare le radici come segue:

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} \tag{4}$$

+ I coefficienti $a,$ $b$ e $c$ sono i coefficienti reali della $(1).$
+ Il simbolo $\pm$ fornisce le due soluzioni dell'equazione, una per ciascun segno.

Come si può notare nella $(4)$ il discriminante è contenuto sotto al segno di radice. Per il discriminante vale questa proprietà che mostra esplicitamente che $\Delta \geq 0$ quando le radici sono reali e che $\Delta = 0$ se e solo se le due radici coincidono:

$$\Delta = a^2(x_1 - x_2)^2$$

Le radici dell'equazione soddisfano le seguenti relazioni derivanti dalle formule di Viète:

$$x_1 + x_2 = -\frac{b}{a}$$
$$x_1x_2 = \frac{c}{a}$$

- - -

Applichiamo la formula $(4)$ a tre equazioni, una per ciascuno dei casi possibili determinati dal segno del discriminante. Consideriamo la prima equazione:

$$2x^2 - 5x + 2 = 0$$

L'equazione è già nella forma standard $(1)$ e i suoi coefficienti sono $a = 2,$ $b = -5$ e $c = 2.$ Sostituiamo i coefficienti nella $(3)$ e calcoliamo per prima cosa il discriminante:

$$\Delta = (-5)^2 - 4(2)(2) = 25 - 16 = 9$$

Il discriminante è positivo, quindi dobbiamo aspettarci due soluzioni reali e distinte. Applicando la $(4),$ otteniamo:

$$
\begin{align}
x_{1,2} &= \frac{-(-5) \pm \sqrt{9}}{2(2)} \\[6pt]
&= \frac{5 \pm 3}{4}
\end{align}
$$

Da questa ricaviamo le soluzioni dell'equazione:
$$x_1 = \frac{5 - 3}{4} = \frac{1}{2} $$ $$x_2 = \frac{5 + 3}{4} = 2$$

L'equazione ha quindi due radici reali e distinte, $x_1 = 1/2$ e $x_2 = 2.$

- - -

Consideriamo adesso la seconda equazione:

$$x^2 - 6x + 9 = 0$$

In questo caso $a = 1,$ $b = -6$ e $c = 9.$ Ripetendo i passaggi dell'esempio precedente calcoliamo il discriminante e otteniamo:

$$\Delta = (-6)^2 - 4(1)(9) = 36 - 36 = 0$$

In questo caso $\Delta$ è pari a zero, e quindi dobbiamo aspettarci due soluzioni reali e coincidenti. Applicando la formula $(4)$ si ha:

$$
\begin{align}
x_{1,2} &= \frac{-(-6) \pm \sqrt{0}}{2(1)} \\[6pt]
&= \frac{6 \pm 0}{2} \\[6pt]
&= 3
\end{align}
$$

L'equazione ha quindi una sola soluzione distinta, $x = 3,$ che è una radice di molteplicità due.

- - -

Consideriamo infine l'ultimo caso in cui non esistono radici reali:

$$x^2 + 2x + 5 = 0$$

Calcolando il discriminante notiamo che esso è negativo:

$$\Delta = 2^2 - 4(1)(5) = 4 - 20 = -16$$

L'equazione non ha quindi soluzioni reali ma ammette soluzioni nel campo dei numeri complessi. Ricorrendo all'identità $i^2 = -1,$ la formula $(4)$ dà:

$$
\begin{align}
x_{1,2} &= \frac{-2 \pm \sqrt{-16}}{2(1)} \\[6pt]
&= \frac{-2 \pm 4i}{2} \\[6pt]
&= -1 \pm 2i
\end{align}
$$

L'equazione ha quindi due radici complesse coniugate, $x_1 = -1 - 2i$ e $x_2 = -1 + 2i.$

## Scomposizione in fattori

Oltre alla formula risolutiva data dalla $(4)$ e ai metodi risolutivi più immediati delle equazioni di secondo grado incomplete, esiste un ulteriore modo per risolvere un'equazione di secondo grado dato dalla sua scomposizione in fattori. Un'equazione di secondo grado nella forma standard data dalla $(1)$ può essere scritta nella seguente forma scomposta dove $x_1$ e $x_2$ sono le radici dell'equazione:

$$a(x - x_1)(x - x_2) = 0 \tag{5}$$

Il processo di scomposizione è trattato esaustivamente nella voce dedicata e nell'esempio che segue. Per ora è sufficiente sapere che questo metodo è efficace quando i fattori lineari sono immediatamente riconoscibili, mentre in tutti gli altri casi si preferisce ricorrere alla formula risolutiva. È importante sottolineare che quando il discriminante è negativo, il polinomio non si può scomporre in fattori lineari reali e la $(4)$ permette di determinare le sue radici complesse. Consideriamo, ad esempio, la seguente equazione che potremmo tranquillamente risolvere con la $(4)$:

$$x^2 - 5x + 6 = 0 \tag{6}$$

Con un po' di esperienza però si nota subito che può essere fattorizzata in una forma più semplice, tenendo conto della seguente relazione:

$$(x + r)(x + s) = x^2 + (r + s)x + rs$$

Questa relazione ci dice che dobbiamo cercare due numeri la cui somma sia il coefficiente di $x,$ cioè $-5,$ e il cui prodotto sia il termine noto, cioè $6.$ Per ricavare questi valori è sufficiente utilizzare la seguente tabellina:

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

La costruzione della tabella è molto semplice: se il prodotto deve essere 6, lo posso ottenere come $1 \cdot 6$ oppure $2 \cdot 3$ e così via. Affinché valga anche la condizione della somma devo considerare solo la riga la cui somma $r + s$ sia pari a $-5,$ ovvero l'ultima, per cui i numeri che soddisfano entrambe le condizioni sono $-2$ e $-3.$ Quindi possiamo scomporre la $(6)$ come:

$$(x - 2)(x - 3) = 0$$

A questo punto, per la legge di annullamento del prodotto, il prodotto è nullo se e solo se almeno uno dei fattori è nullo. Otteniamo quindi:

$$x - 2 = 0 \quad \text{oppure} \quad x - 3 = 0$$

Da queste uguaglianze ricaviamo quindi che le soluzioni dell'equazione sono $x_1 = 2$ e $x_2 = 3.$ Attenzione: la scomposizione ottenuta corrisponde alla $(5),$ con $a = 1,$ ma se $a$ fosse diverso da 1 dovremmo cercare due numeri la cui somma sia $b/a$ e il cui prodotto sia $c/a.$

## Equazioni di secondo grado con parametri

Lo studio delle equazioni di secondo grado si estende anche al caso in cui i coefficienti dipendono da un parametro. Queste equazioni si chiamano equazioni di secondo grado parametriche e hanno la seguente forma:

$$a(k)x^2 + b(k)x + c(k) = 0 \tag{7}$$

Per i valori di $k$ tali che $a(k) \neq 0,$ la natura delle soluzioni si determina calcolando il discriminante:

$$\Delta(k) = b(k)^2 - 4a(k)c(k)$$

  + Se $\Delta(k) > 0,$ l'equazione ha due soluzioni reali distinte.
  + Se $\Delta(k) = 0,$ ha due soluzioni reali e coincidenti.
  + Se $\Delta(k) < 0,$ ha due soluzioni complesse coniugate.

La condizione $a(k) \neq 0$ deve essere sempre verificata prima di utilizzare il discriminante in quanto per un valore di $k$ tale che $a(k) = 0,$ l'equazione non è più di secondo grado, ma richiede comunque un'analisi separata. Diventa di primo grado quando $b(k) \neq 0.$ Se anche $b(k) = 0,$ l'equazione non ha soluzioni quando $c(k) \neq 0,$ mentre ogni valore di $x$ è soluzione quando $c(k) = 0.$
