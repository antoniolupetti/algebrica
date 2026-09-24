---
title: Quadratic Formula
source: https://algebrica.org/quadratic-formula/
license: CC BY-NC 4.0
tags:
  - completing-the-square
  - discriminant
  - quadratic-equation
  - quadratic-formula
  - vieta-formulas
---
## Definizione

Nella voce sulle equazioni di secondo grado abbiamo mostrato come un'equazione di questo tipo, ricondotta alla forma standard $ax^2 + bx + c = 0,$ è caratterizzata da un polinomio di secondo grado e ammette sempre esattamente due radici in $\mathbb{C},$ come conseguenza del teorema fondamentale dell'algebra. La natura delle radici, come richiameremo più avanti in questa pagina, è determinata dal segno del discriminante $\Delta = b^2 - 4ac$ e, per ottenere tali radici, si ricorre il più delle volte all'uso della formula risolutiva:

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} \tag{1}$$

La $(1)$ fornisce un metodo semplice e meccanico per risolvere qualunque equazione di secondo grado e si applica a qualsiasi equazione di questo tipo con coefficienti reali o complessi, purché valga la condizione $a \neq 0,$ essendo il coefficiente $a$ presente al denominatore. Osservando la $(1)$ possiamo evidenziare quanto segue:

+ $a,$ $b$ e $c$ sono i coefficienti dell'equazione di secondo grado ricondotta alla forma standard e, come abbiamo detto, deve valere $a \neq 0.$
+ Il simbolo più o meno indica i valori corrispondenti alle due radici del polinomio.

La $(1)$ permette anche di studiare come variano le radici quando i coefficienti dipendono da un parametro come mostrato sulla pagina relativa alle equazioni di secondo grado parametriche.

- - -

Per la classificazione seguente e la sua interpretazione geometrica assumiamo che i coefficienti $a,$ $b$ e $c$ siano reali.

Come abbiamo ricordato all'inizio, la quantità sotto il segno di radice, $b^2 - 4ac,$ è detta discriminante e il suo segno determina univocamente il numero e la natura delle soluzioni dell'equazione.

Quando $\Delta > 0,$ l'equazione ha due soluzioni reali distinte che scriviamo come $S = \{\ x_1, x_2 \ \}$ con $x_1, x_2 \in \mathbb{R}$ e $x_1 \neq x_2.$ Le soluzioni sono ottenute applicando direttamente la $(1)$.

Quando $\Delta = 0,$ l'equazione ha due soluzioni reali e coincidenti, cioè un'unica radice di molteplicità due che scriviamo come $S = \{\ x \ \}$ con $x \in \mathbb{R}$ e $x = x_1 = x_2.$ Essendo il discriminante nullo, la $(1)$ si riduce alla seguente formula che determina il valore della soluzione dell'equazione.

$$x = -\frac{b}{2a} \tag{2}$$

Quando, infine, $\Delta < 0,$ l'equazione non ha soluzioni reali ma ha invece sempre due soluzioni complesse coniugate con parte immaginaria diversa da zero, quindi si scrive $\nexists\ x \in \mathbb{R}.$ Le soluzioni complesse sono ottenute dalla $(1)$ moltiplicando la radice per l'unità immaginaria $i$:

$$x_{1,2} = \frac{-b \pm i\sqrt{4ac - b^2}}{2a}\tag{3}$$

Il discriminante determina anche la posizione del grafico della funzione quadratica $f(x) = ax^2 + bx + c$ rispetto all'asse $x.$ Dal punto di vista geometrico, sappiamo che a un'equazione di secondo grado è associata una parabola, le cui intersezioni con l'asse dipendono proprio dal segno del discriminante:

![IMG. 1](../polynomials/svg/polynomials-2.svg)

Nello specifico:

+ Se $\Delta > 0,$ la parabola interseca l'asse $x$ in due punti distinti, quindi l'equazione ha due soluzioni.
+ Se $\Delta = 0,$ la parabola è tangente all'asse $x$ in un unico punto, il vertice, e quindi l'equazione ha una soluzione con molteplicità due.
+ Se $\Delta < 0,$ la parabola non interseca l'asse $x,$ quindi non ammette soluzioni reali.

## Dimostrazione

La $(1)$ si ricava dalla forma standard delle equazioni di secondo grado mediante il metodo del completamento del quadrato. Riscriviamo $ax^2 + bx + c = 0$ isolando il termine noto:

$$ax^2 + bx = -c$$

Per applicare il completamento del quadrato dividiamo entrambi i membri per $a,$ che sappiamo essere per ipotesi diverso da zero, ottenendo:

$$x^2 + \frac{b}{a}x = -\frac{c}{a} \tag{4}$$

Trasformiamo ora il primo membro in un quadrato perfetto. Sappiamo che il quadrato di un binomio $(a+b)^2$ è pari a $a^2 + 2ab + b^2.$ Quindi, per ottenere un quadrato perfetto, al primo membro della $(4)$ manca l'equivalente di $b^2.$ Perciò riscriviamo la $(4)$ come segue:

$$x^2 + \frac{b}{a}x + \left(\frac{b}{2a}\right)^2 = -\frac{c}{a} + \left(\frac{b}{2a}\right)^2$$

Al primo membro abbiamo così ottenuto il quadrato di un binomio. Raggruppiamo i termini del binomio e svolgiamo i calcoli al secondo membro ottenendo:

$$\left(x + \frac{b}{2a}\right)^2 = \frac{b^2 - 4ac}{4a^2} \tag{5}$$

Estraiamo la radice quadrata ricordandoci di introdurre il doppio segno, poiché una radice quadrata e il suo opposto hanno lo stesso quadrato. Quindi possiamo riscrivere la $(5)$ nel seguente modo:

$$x + \frac{b}{2a} = \pm\frac{\sqrt{b^2 - 4ac}}{2a}$$

Isolando la $x$ otteniamo quindi la $(1):$

$$x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

- - -

Dopo aver applicato la formula risolutiva, vale la pena citare che possiamo verificare le soluzioni trovate confrontando la loro somma e il loro prodotto con i coefficienti dell'equazione. Per questo ci vengono in aiuto le formule di Viète che stabiliscono che, per un'equazione di secondo grado $ax^2 + bx + c = 0$ con radici $x_1$ e $x_2,$ valgono le seguenti relazioni:

$$
\begin{align}
x_1 + x_2 &= -\frac{b}{a} \\[6pt]
x_1x_2 &= \frac{c}{a}
\end{align}
$$

Queste relazioni valgono in $\mathbb{C}$ per qualsiasi valore del discriminante e si ottengono sviluppando la forma fattorizzata $a(x - x_1)(x - x_2)$ e confrontando i coefficienti.

## Esempi

Iniziamo ad applicare alla prima equazione, $x^2 - 4x + 2 = 0,$ la $(1).$ L'equazione è già nella forma standard, con $a = 1,$ $b = -4$ e $c = 2,$ quindi sostituendo questi coefficienti nella formula otteniamo:

$$
\begin{align*}
x_{1,2} &= \frac{-(-4) \pm \sqrt{(-4)^2 - 4(1)(2)}}{2(1)} \\[6pt]
&= \frac{4 \pm \sqrt{16 - 8}}{2} \\[6pt]
&= \frac{4 \pm \sqrt{8}}{2} \\[6pt]
&=\frac{4 \pm 2\sqrt{2}}{2}
\end{align*}
$$

Poiché $\Delta = 8 > 0,$ l'equazione ha due soluzioni reali distinte per cui otteniamo $x_1 = 2 - \sqrt{2}$ e $x_2 = 2 + \sqrt{2}.$

- - -

La seconda equazione richiede alcuni passaggi per essere ricondotta alla forma standard:

$$\frac{(x-1)^2}{2} - \frac{(x+1)(x-2)}{3} = \frac{x-1}{3}$$

Per prima cosa eliminiamo i denominatori e sviluppiamo il quadrato e i prodotti, ottenendo:
$$
\begin{align}
3(x^2 - 2x + 1) - 2(x^2 - x - 2) &= 2x - 2 \\[6pt]
3x^2 - 6x + 3 - 2x^2 + 2x + 4 &= 2x - 2 \\[6pt]
x^2 - 4x + 7 &= 2x - 2\\[6pt]
x^2 - 4x + 7 - 2x + 2 &= 0 \\[6pt]
x^2 - 6x + 9 &= 0
\end{align}
$$

Abbiamo quindi riportato l'equazione originaria nella sua forma standard. I suoi coefficienti sono $a = 1,$ $b = -6$ e $c = 9,$ e il discriminante è:

$$\Delta = (-6)^2 - 4(1)(9) = 36 - 36 = 0$$

Poiché $\Delta = 0,$ le due radici coincidono. Sostituendo i coefficienti nella $(2),$ che ricordiamo è ottenuta dalla $(1)$ quando il discriminante è nullo, otteniamo:

$$x = -\frac{b}{2a} = -\frac{-6}{2(1)} = 3$$

L'equazione ha quindi una sola radice reale $x = 3,$ di molteplicità due.

- - -

Risolviamo infine l'equazione $x^2 + 2x + 5 = 0.$ I coefficienti sono $a = 1,$ $b = 2$ e $c = 5,$ e il discriminante stavolta è minore di zero:

$$\Delta = 2^2 - 4(1)(5) = 4 - 20 = -16$$

L'equazione quindi non ha soluzioni reali. Esprimendo la radice quadrata mediante l'unità immaginaria $i,$ $\sqrt{-16} = 4i,$ dalla $(3)$ otteniamo:

$$x_{1,2} = \frac{-2 \pm 4i}{2} = -1 \pm 2i$$

Abbiamo quindi ottenuto due soluzioni complesse e coniugate $x_1 = -1 - 2i$ e $x_2 = -1 + 2i.$
