---
title: Cauchy's Theorem
source: https://algebrica.org/cauchy-theorem/
license: CC BY-NC 4.0
tags:
  - cauchy-theorem
  - derivatives
  - differential-calculus-theorems
  - mean-value-theorem
---

## Enunciato

Il teorema di Cauchy è uno dei teoremi fondamentali del calcolo differenziale e può essere considerato un'estensione del teorema di Lagrange al confronto tra due funzioni. Come ricorderete, il teorema di Lagrange è rappresentato dalla seguente formula:

$$
f'(c) = \frac{f(b)-f(a)}{b-a} \tag{1}
$$

La $(1)$ mette in relazione la variazione di una funzione $f$ su un intervallo $[a, b]$ con la sua derivata in un punto interno $c.$ Cauchy considera invece il rapporto tra le variazioni di due funzioni e afferma che questo rapporto coincide con quello delle rispettive derivate calcolate sempre in un punto interno dell'intervallo. In termini formali, il teorema considera due funzioni a valori reali $f$ e $g$ definite su un intervallo $[a, b],$ con $a < b.$ Si considerino le seguenti ipotesi:

+ Le funzioni $f$ e $g$ sono continue sull'intervallo chiuso $[a, b].$
+ Le funzioni $f$ e $g$ sono derivabili sull'intervallo aperto $(a, b).$
+ La derivata $g'(x)$ è diversa da zero per ogni $x \in (a, b).$

Se le ipotesi sono soddisfatte, allora esiste almeno un punto $c \in (a, b)$ tale che vale la seguente relazione:

$$\frac{f'(c)}{g'(c)} = \frac{f(b) - f(a)}{g(b) - g(a)} \tag{2}$$

In pratica, il teorema asserisce che il valore del rapporto della variazione delle due funzioni da $a$ a $b$ si ritrova tra le derivate di $f$ e $g$ in almeno un punto interno all'intervallo. Come potete notare, la terza condizione $g'(x) \neq 0$ assicura che i denominatori nella $(2)$ siano diversi da zero.

Su questo risultato si basa la dimostrazione della regola di de l'Hôpital, in quanto permette di esprimere il rapporto tra gli incrementi delle due funzioni attraverso il rapporto delle loro derivate in un punto intermedio.

> Il teorema garantisce l'esistenza di almeno un punto $c,$ ma non la sua unicità. Possono infatti esserci casi in cui più punti, o al limite anche tutti i punti interni all'intervallo, soddisfano l'uguaglianza $(2).$ Consideriamo per esempio $f(x) = 2x$ e $g(x) = x.$ Entrambi i membri dell'uguaglianza valgono $2$ e quindi ogni $c \in (a, b)$ soddisfa la conclusione del teorema.

## Dimostrazione

La dimostrazione del teorema di Cauchy usa il teorema di Rolle per garantire l'esistenza del punto $c$ in cui la $(2)$ è soddisfatta. Per prima cosa dobbiamo verificare che il denominatore $g(b) - g(a)$ sia diverso da zero. Supponiamo per assurdo che $g(a)$ sia uguale a $g(b).$ Poiché, per la prima e seconda ipotesi del teorema, $g$ è continua su $[a, b]$ e derivabile su $(a, b),$ per il teorema di Rolle avremmo un punto $\xi \in (a, b)$ in cui $g'(\xi) = 0.$ Questo però è in contraddizione con la terza ipotesi e quindi deve necessariamente valere che $g(b) \neq g(a).$

Procediamo adesso definendo una funzione ausiliaria che dipende da una costante reale $\lambda:$

$$\varphi(x) = f(x) - \lambda g(x) \tag{3}$$

Vogliamo scegliere $\lambda$ in modo che $\varphi$ assuma lo stesso valore agli estremi e questa condizione $\varphi(a) = \varphi(b)$ si può scrivere come:

$$f(a) - \lambda g(a) = f(b) - \lambda g(b)$$

Raccogliendo i termini che contengono $\lambda$ otteniamo:

$$\lambda[g(b) - g(a)] = f(b) - f(a) \tag{4}$$

Il coefficiente di $\lambda,$ ovvero $g(b) - g(a),$ è diverso da zero in quanto lo abbiamo dimostrato poco sopra e possiamo quindi riscrivere la $(4)$ come:

$$\lambda = \frac{f(b) - f(a)}{g(b) - g(a)}$$

A questo punto verifichiamo che le ipotesi del teorema di Rolle siano verificate. Poiché abbiamo moltiplicato $g$ per la costante $\lambda$ e sottratto il risultato a $f,$ la funzione $\varphi$ è una combinazione lineare di $f$ e $g$ e quindi è continua su $[a, b]$ e derivabile su $(a, b),$ soddisfacendo così le prime due ipotesi del teorema di Rolle. Inoltre, per come abbiamo scelto $\lambda,$ vale anche che $\varphi(a) = \varphi(b),$ che è la terza ipotesi del teorema di Rolle, anch'essa soddisfatta. Per questo motivo esiste allora un punto $c \in (a, b)$ tale che $\varphi'(c) = 0.$ Calcolando la derivata della $(3)$ otteniamo:

$$\varphi'(x) = f'(x) - \lambda g'(x)$$

Nel punto $c$ sappiamo che questa derivata si annulla, perciò si ha:

$$f'(c) = \lambda g'(c)$$

Poiché $g'(c) \neq 0,$ possiamo dividere entrambi i membri per $g'(c)$ e sostituire il valore di $\lambda$ ottenendo la seguente relazione che è proprio l'uguaglianza $(2)$ del teorema di Cauchy:

$$\frac{f'(c)}{g'(c)} = \lambda = \frac{f(b) - f(a)}{g(b) - g(a)}$$

## Interpretazione geometrica e legame con i teoremi di Lagrange e di Rolle

Per dare un significato geometrico alla formula $(2),$ immaginiamo un punto che si muove nel piano e le cui coordinate dipendono da un parametro $t.$ Usiamo $g(t)$ come coordinata orizzontale e $f(t)$ come coordinata verticale. Al variare di $t$ in $[a, b],$ la coppia $(g(t), f(t))$ descrive una curva che congiunge i punti $(g(a), f(a))$ e $(g(b), f(b))$ e la retta che passa per questi punti ha coefficiente angolare proprio uguale al rapporto tra la variazione delle due coordinate:

$$\frac{f(b) - f(a)}{g(b) - g(a)}$$

Nel punto corrispondente a $t = c,$ il vettore $(g'(c), f'(c))$ dà la direzione della tangente alla curva. Poiché $g'(c) \neq 0,$ il coefficiente angolare della tangente è dato da:

$$\frac{f'(c)}{g'(c)}$$

Come potete vedere anche nell'immagine seguente, la $(2)$ afferma che esiste almeno un punto interno all'intervallo in cui la tangente è parallela alla secante che congiunge gli estremi della curva.


![IMG. 1](../svg/cauchy-theorem-1.svg)



Come abbiamo appena visto, scegliendo $g(x) = x$ si ottiene il teorema di Lagrange. Infatti, in questo caso $g'(x) = 1$ e $g(b) - g(a) = b - a,$ quindi la $(2)$ diventa:

$$f'(c) = \frac{f(b) - f(a)}{b - a} \tag{5}$$

Se aggiungiamo un'ulteriore ipotesi per cui $f(a) = f(b),$ il numeratore a destra si annulla e otteniamo $f'(c) = 0,$ cioè la conclusione del teorema di Rolle. Questo ci fa concludere che il teorema di Lagrange è dunque un caso particolare del teorema di Cauchy, mentre il teorema di Rolle è un caso particolare di Lagrange.

## Esempio

Applichiamo il teorema a un esempio concreto, verificando le ipotesi e calcolando il punto $c.$ Consideriamo le funzioni $f$ e $g$ sull'intervallo $[1, 3]:$

$$f(x) = 2x^2 - 4x + 2$$

$$g(x) = x^2$$

Entrambe le funzioni sono polinomi, e quindi sono continue e derivabili su tutto $\mathbb{R},$ il che soddisfa le prime due ipotesi del teorema. Ricordiamo che dobbiamo applicare la $(2)$ perciò verifichiamo che la derivata di $g$ al denominatore non sia nulla. La terza ipotesi del teorema è quindi verificata in quanto $g'(x) = 2x,$ ed è positiva sull'intervallo scelto. A questo punto, siamo certi che tutte le ipotesi sono soddisfatte e possiamo allora cercare un punto $c \in (1, 3)$ tale che:

$$\frac{f'(c)}{g'(c)} = \frac{f(3) - f(1)}{g(3) - g(1)}$$

Calcoliamo adesso i valori delle funzioni agli estremi del nostro intervallo e otteniamo:

$$
\begin{align}
f(1) &= 2 - 4 + 2 = 0 \\[6pt]
f(3) &= 18 - 12 + 2 = 8 \\[6pt]
g(1) &= 1 \\[6pt]
g(3) &= 9
\end{align}
$$

Il rapporto tra gli incrementi diventa:

$$\frac{f(3) - f(1)}{g(3) - g(1)} = \frac{8 - 0}{9 - 1} = 1$$

Calcoliamo adesso le derivate di $f$ e $g$ che sono rispettivamente $f'(x) = 4x - 4$ e $g'(x) = 2x.$ Il punto cercato deve quindi soddisfare la seguente uguaglianza:

$$\frac{4c - 4}{2c} = 1$$

Ricavando $c$ otteniamo:

$$
\begin{align}
4c - 4 &= 2c \\[6pt]
2c &= 4 \\[6pt]
c &= 2
\end{align}
$$

Il valore $c = 2$ appartiene a $(1, 3)$ e soddisfa l'uguaglianza richiesta. In questo esempio abbiamo un'equazione di primo grado che ha un'unica soluzione e pertanto abbiamo un solo punto $c$ che realizza la conclusione del teorema. Potrebbero però esserci casi, come abbiamo detto prima, in cui all'interno dell'intervallo può esistere più di un punto $c,$ ad esempio nel caso l'equazione ottenuta fosse un'equazione di secondo grado con due soluzioni reali e distinte, entrambe appartenenti all'intervallo aperto considerato.

## Una formulazione più generale

Il teorema di Cauchy presenta una formulazione più generale nota come formulazione senza quozienti, nella quale non è richiesta la terza ipotesi per cui $g'$ sia diversa da zero. Questa formulazione si costruisce nel seguente modo. Consideriamo sempre due funzioni $f$ e $g$ continue su $[a, b]$ e derivabili su $(a, b),$ con $a < b.$ Allora esiste almeno un punto $c \in (a, b)$ tale che:

$$[g(b) - g(a)]f'(c) = [f(b) - f(a)]g'(c) \tag{6}$$

A differenza della $(2),$ nella formula $(6)$ non dividiamo né per $g(b) - g(a)$ né per $g'(c)$ e l'uguaglianza ha quindi significato anche quando uno di questi fattori si annulla. Quando entrambi i fattori sono diversi da zero, le due formulazioni sono equivalenti.

Per dimostrare la $(6)$ utilizziamo una nuova funzione ausiliaria continua su $[a, b]$ e derivabile su $(a, b),$ definita in questo modo:

$$H(x) = [g(b) - g(a)][f(x) - f(a)] - [f(b) - f(a)][g(x) - g(a)] \tag{7}$$

In $x = a$ entrambe le differenze che dipendono da $x$ si annullano, quindi $H(a) = 0.$ In $x = b$ si ottiene:

$$H(b) = [g(b) - g(a)][f(b) - f(a)] - [f(b) - f(a)][g(b) - g(a)] = 0$$

Poiché $H(a) = H(b),$ per il teorema di Rolle sappiamo esistere un punto $c \in (a, b)$ tale che $H'(c) = 0.$ Calcoliamo quindi la derivata della $(7)$ e otteniamo:

$$H'(x) = [g(b) - g(a)]f'(x) - [f(b) - f(a)]g'(x)$$

Valutando questa espressione in $c$ e ponendola uguale a zero otteniamo proprio la $(6)$ e quindi il teorema è dimostrato. Ricordate che per passare dalla $(6)$ alla $(2)$ occorre che $g(b) - g(a) \neq 0$ e che $g'(c)$ sia diversa da zero proprio nel punto fornito dal teorema. L'ipotesi $g'(x) \neq 0$ su tutto $(a, b)$ garantisce questa condizione prima ancora di conoscere $c,$ oltre ad assicurare che $g(b) - g(a) \neq 0.$

- - - 

Questa formulazione senza quozienti permette di capire meglio perché l'ipotesi $g'(x) \neq 0$ compare nell'enunciato del teorema iniziale. Se $g(a)$ fosse uguale a $g(b),$ il rapporto tra gli incrementi non sarebbe definito e non potremmo scegliere $\lambda$ con la formula usata nella prima dimostrazione. Se invece $g(a) \neq g(b),$ quel rapporto è definito, ma resta da verificare che si possa dividere anche per $g'(c).$

Per capire perché la sola condizione $g(a) \neq g(b)$ non basta, facciamo un esempio e consideriamo le seguenti funzioni sull'intervallo $[-1, 1]$:

$$f(x) = x^2$$
$$g(x) = x^3$$

Queste funzioni sono entrambe continue e derivabili su tutto $\mathbb{R},$ e agli estremi si ha:

$$
\begin{align}
f(1) - f(-1) &= 0 \\[6pt]
g(1) - g(-1) &= 2
\end{align}
$$

Pertanto, il rapporto tra gli incrementi è uguale a zero:

$$\frac{f(1) - f(-1)}{g(1) - g(-1)} = 0$$

Le derivate di $f$ e $g$ sono $f'(x) = 2x$ e $g'(x) = 3x^2$ e per ogni $c \in (-1, 1)$ diverso da zero, il loro rapporto vale:

$$\frac{f'(c)}{g'(c)} = \frac{2c}{3c^2} = \frac{2}{3c}$$

Questo rapporto non è mai zero. Nel punto $c = 0,$ invece, entrambe le derivate si annullano e il loro rapporto non è definito. Non esiste quindi alcun punto interno in cui valga la $(2),$ nonostante in questo caso il rapporto tra gli incrementi risulti definito. La formulazione senza quozienti invece continua a valere. Sostituendo gli incrementi e le derivate nella $(6)$ otteniamo:

$$2 \cdot 2c = 0 \cdot 3c^2$$

Quest'uguaglianza si riduce a $4c = 0$ e quindi il punto fornito dalla forma generale è proprio $c = 0.$ In quel punto l'identità è valida, ma non possiamo trasformarla in un'uguaglianza tra quozienti perché $g'(0) = 0.$
