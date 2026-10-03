---
title: L'Hopital's Rule
source: https://algebrica.org/hopital-rule/
license: CC BY-NC 4.0
tags:
  - derivatives
  - differential-calculus-theorems
  - hopital-rule
  - indeterminate-forms
  - limits
---

## Risolvere i limiti di forme indeterminate

La regola di de l'Hôpital è un metodo molto utile che consente di calcolare agevolmente alcuni [limiti](../limits/) che presentano delle [forme indeterminate](../indeterminate-forms/) del tipo $0/0$ o $\infty/\infty$. In termini informali, sotto alcune condizioni, il teorema da cui deriva la formula stabilisce che il limite del rapporto tra due funzioni coincide con il limite del rapporto tra le rispettive [derivate](../derivatives/). In alcuni casi, questo passaggio è funzionale a eliminare la forma indeterminata e consente di calcolare il limite per sostituzione diretta o con poche manipolazioni algebriche. Tenete presente che questa trasformazione non sempre semplifica il calcolo, perché in alcune situazioni il rapporto delle derivate può anch'esso presentare una forma indeterminata. In questa situazione, se le ipotesi del teorema continuano a valere, si può applicare nuovamente la regola, oppure ricorrere a un altro metodo.

Per illustrare il teorema, consideriamo due [funzioni](../functions/) $f$ e $g$ definite in un intorno aperto $I$ contenente $x_0,$ escluso eventualmente il punto $x_0$ stesso, e consideriamo il limite del loro rapporto:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} \tag{1}$$

Sostituendo $x_0$ alla $(1)$ otteniamo una delle seguenti forme indeterminate che non ci dice nulla sulla natura del limite:

$$\frac{0}{0} \quad \frac{\infty}{\infty}$$

Supponiamo allora che per la $(1)$ valgano le seguenti condizioni:

+ $f$ e $g$ sono derivabili in ogni punto di $I$ diverso da $x_0.$
+ La derivata $g'(x)$ è diversa da zero per ogni $x \in I$ con $x \neq x_0.$
+ Nel caso $0/0,$ vale $\displaystyle \lim_{x \to x_0} f(x) = \lim_{x \to x_0} g(x) = 0;$ nel caso $\infty/\infty,$ ciascuna funzione tende a $+\infty$ o a $-\infty$ per $x \to x_0.$
+ Esiste, finito o infinito, il limite del rapporto delle derivate di $f$ e $g$:

$$\lim_{x \to x_0} \frac{f'(x)}{g'(x)} \tag{2}$$

Se valgono le suddette ipotesi allora possiamo affermare che esiste anche il limite del rapporto delle funzioni e vale la seguente uguaglianza:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)} \tag{3}$$

Notate che nella $(3)$ il numeratore e il denominatore si derivano separatamente e non va quindi applicata la formula della derivata del quoziente. 

- - -

Una considerazione importante riguarda l'esistenza del limite del rapporto delle derivate. Infatti se tale limite non esiste, il teorema non permette di concludere nulla sul limite originario della $(1)$. Consideriamo, per esempio, le funzioni $f(x) = x + \sin x$ e $g(x) = x.$ Quando $x$ tende a $\infty$ il loro rapporto tende a uno e infatti si ha:

$$\lim_{x \to +\infty} \frac{f(x)}{g(x)} = \lim_{x \to +\infty} \left(1 + \frac{\sin x}{x}\right) = 1$$

Se calcoliamo invece le derivate del numeratore e del denominatore ci accorgiamo che il loro rapporto è pari a $1 + \cos x$ ed è un'espressione oscillante che non ammette limite all'infinito. Quindi possiamo concludere che l'esistenza del limite del rapporto delle derivate è una condizione sufficiente, sotto le altre ipotesi del teorema, ma non necessaria per l'esistenza del limite del rapporto delle funzioni.

## Dimostrazione del caso $0/0$

Procediamo adesso con la dimostrazione della regola $(3)$ quando il limite della $(1)$ conduce alla forma indeterminata $0/0.$ Poiché sia $f(x)$ che $g(x)$ tendono a zero, possiamo estenderle per continuità al punto $x_0,$ assegnando a ciascuna il valore del proprio limite:

$$f(x_0) = g(x_0) = 0\tag{4}$$ 

Fissiamo ora $x \in I$ con $x > x_0.$ In questo caso, il denominatore è diverso da zero. Infatti, se fosse uguale a zero, $g(x)$ avrebbe lo stesso valore ai due estremi dell'intervallo $[x_0, x],$ ma essendo continua sull'intervallo chiuso e derivabile al suo interno, per il teorema di Rolle la sua derivata dovrebbe annullarsi in almeno un punto interno. Questo contraddice l'ipotesi che $g'$ sia diversa da zero in ogni punto di $I$ diverso da $x_0.$ Pertanto possiamo concludere che $g(x) \neq 0$ e applicare il [teorema di Cauchy](../cauchy-theorem/) sull'intervallo $[x_0, x]$ e ottenere un punto $c \in (x_0, x)$ tale che valga la seguente relazione:

$$\frac{f(x) - f(x_0)}{g(x) - g(x_0)} = \frac{f'(c)}{g'(c)} \tag{5}$$

Poiché vale la $(4)$ la $(5)$ diventa:

$$\frac{f(x)}{g(x)} = \frac{f'(c)}{g'(c)}$$

Per ogni $x > x_0,$ il teorema di Cauchy garantisce l'esistenza di un punto che indichiamo con $c(x)$ che soddisfa:

$$x_0 < c(x) < x \tag{6}$$

Sottraendo $x_0$ dai tre membri della $(6)$ otteniamo:

$$0 < c(x) - x_0 < x - x_0$$

Per il limite destro, la distanza $x - x_0$ tende a zero e quindi anche la distanza $c(x) - x_0$ deve tendere a zero. Per il [teorema del confronto](../squeeze-theorem/) segue che:

$$\lim_{x \to x_0^+} c(x) = x_0$$

Per il limite sinistro, invece, applichiamo il teorema di Cauchy sull'intervallo $[x, x_0]$ dove il punto $c(x)$ soddisfa:

$$x < c(x) < x_0$$

Sottraendo ciascun membro da $x_0$ e riordinando le disuguaglianze otteniamo:

$$0 < x_0 - c(x) < x_0 - x$$

Quando $x$ si avvicina a $x_0$ da sinistra, la distanza $x_0 - x$ tende a zero e anche la distanza $x_0 - c(x)$ tende quindi a zero. Per il teorema del confronto otteniamo:

$$\lim_{x \to x_0^-} c(x) = x_0$$

Abbiamo quindi dimostrato che $c(x)$ tende a $x_0$ sia da destra sia da sinistra; possiamo ora usare l'ipotesi secondo cui esiste il limite $(2),$ indicando con $L$ il suo valore, finito o infinito:

$$\lim_{x \to x_0} \frac{f'(x)}{g'(x)} = L$$

Poiché $c(x) \to x_0$ e $c(x) \neq x_0$ possiamo scrivere:

$$\lim_{x \to x_0} \frac{f'(c(x))}{g'(c(x))} = L$$

Riprendiamo l'uguaglianza $(5)$ ottenuta con il teorema di Cauchy. Per la $(4),$ i valori delle funzioni in $x_0$ sono nulli e indicando il punto intermedio con $c(x),$ abbiamo quindi:

$$\frac{f(x)}{g(x)} = \frac{f'(c(x))}{g'(c(x))}$$

Abbiamo appena dimostrato che il rapporto a destra tende a $L$ ma poiché i due rapporti sono uguali, anche quello a sinistra tende a $L,$ dunque vale:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = L$$

Sostituendo ad $L$ il limite dato dalla $(2),$ otteniamo proprio la formula $(3)$ che volevamo dimostrare per il caso $0/0$:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)}$$

## Dimostrazione del caso $\infty/\infty$

Dimostriamo ora il teorema quando dalla $(1)$ otteniamo la forma indeterminata $\infty/\infty.$ In questo caso si procede in questo modo. Supponiamo che la $(2)$ sia un numero reale $L.$ Fissato $\varepsilon > 0,$ per la definizione di limite, possiamo scegliere un $\delta > 0$ in modo che valga la seguente relazione:

$$
\left| \frac{f'(t)}{g'(t)} - L \right| < \frac{\varepsilon}{2} \quad \forall \ t \in (x_0, x_0 + \delta)
$$

Fissiamo adesso un punto $y \in (x_0, x_0 + \delta)$ e consideriamo $x$ tale che $x_0 < x < y.$ Per il [teorema di Cauchy](../cauchy-theorem/), esiste un punto $c \in (x, y)$ per il quale vale la seguente relazione:

$$
\frac{f(x) - f(y)}{g(x) - g(y)} = \frac{f'(c)}{g'(c)} \tag{7}
$$

Quando $x$ è sufficientemente vicino a $x_0,$ anche $f(x)$ e $g(x)$ sono diversi da zero, e possiamo riscrivere la $(7)$ in questo modo:

$$
\frac{f(x)}{g(x)} \cdot \frac{1 - f(y)/f(x)}{1 - g(y)/g(x)} = \frac{f'(c)}{g'(c)}
$$

Adesso poniamo:

$$
\begin{align}
A(x) &= \frac{1 - f(y)/f(x)}{1 - g(y)/g(x)} \\[6pt]
R(x) &= \frac{f'(c)}{g'(c)}
\end{align}
$$

La $(7)$ quindi diventa

$$\frac{f(x)}{g(x)} = \frac{R(x)}{A(x)} \tag{8}$$

Poiché $c$ appartiene all'intorno scelto, la stima iniziale sul rapporto delle derivate vale anche per $R(x).$ Inoltre, per la disuguaglianza triangolare abbiamo un limite superiore e quindi possiamo scrivere le seguenti disuguaglianze:

$$
\begin{align}
|R(x) - L| &< \frac{\varepsilon}{2} \\[6pt]
|R(x)| &\leq |L| + |R(x) - L| < |L| + \frac{\varepsilon}{2}
\end{align}
$$

Poiché $|R(x)|$ è limitato e $1/A(x) - 1$ tende a zero, per $x$ abbastanza vicino a $x_0,$ da destra, abbiamo:

$$|R(x)|\left|\frac{1}{A(x)} - 1\right| < \frac{\varepsilon}{2}$$

Usiamo ora la $(8)$ e otteniamo:

$$
\begin{align}
\left|\frac{f(x)}{g(x)} - L\right|
&= \left|R(x)\left(\frac{1}{A(x)} - 1\right) + R(x) - L\right| \\[6pt]
&\leq |R(x)|\left|\frac{1}{A(x)} - 1\right| + |R(x) - L| \\[6pt]
&< \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon
\end{align}
$$

La stima ottenuta mostra che il rapporto delle funzioni si avvicina a $L$ quanto vogliamo, purché $x$ sia sufficientemente vicino a $x_0$ da destra. Poiché $L$ è il limite del rapporto delle derivate, abbiamo dimostrato che:

$$\lim_{x \to x_0^+} \frac{f(x)}{g(x)} = \lim_{x \to x_0^+} \frac{f'(x)}{g'(x)} = L$$

Questo conclude la dimostrazione della regola per la forma $\infty/\infty,$ nel caso del limite destro con $L$ finito.

> Abbiamo dimostrato quindi il risultato quando $L$ è un numero reale finito. Lo stesso procedimento si adatta al caso $L = +\infty,$ mostrando che il rapporto delle funzioni supera qualsiasi soglia positiva per $x$ sufficientemente vicino a $x_0.$ Il caso $L = -\infty$ si ottiene cambiando il segno della $f$ e con analoghe modifiche si trattano il limite sinistro e i limiti all'infinito.

## Esempi

Di seguito sono proposti alcuni esempi che consentono di risolvere limiti di forme indeterminate usando la regola di de l'Hôpital. Consideriamo ad esempio il primo limite notevole:

$$\lim_{x \to 0} \frac{\sin x}{x}$$

Per sostituzione diretta, il numeratore e il denominatore tendono entrambi a zero, quindi in questo caso si ottiene la forma indeterminata $0/0.$ Verifichiamo come prima cosa se possiamo applicare la regola di de l'Hôpital. Le funzioni al numeratore e al denominatore sono derivabili in un intorno di zero e la derivata del denominatore è uguale a $1$ (quindi non si annulla). Il rapporto delle derivate è $\cos x,$ che tende a $1.$ Abbiamo così mostrato che sono soddisfatte tutte le ipotesi e possiamo quindi applicare la regola ottenendo:

$$
\begin{align}
\lim_{x \to 0} \frac{\sin x}{x}
&= \lim_{x \to 0} \frac{(\sin x)'}{(x)'} \\[6pt]
&= \lim_{x \to 0} \frac{\cos x}{1} \\[6pt]
&= 1
\end{align}
$$

- - - 

Consideriamo adesso il caso di una differenza di funzioni che presenta la forma indeterminata $\infty - \infty.$ Tale forma può essere riscritta come un unico quoziente, per ricondurla a una delle forme cui si applica la regola. Verifichiamolo, ad esempio, per il seguente limite:

$$\lim_{x \to 0} \left(\frac{1}{\sin x} - \frac{2}{x}\right)$$

Possiamo riscrivere il limite come:

$$\frac{1}{\sin x} - \frac{2}{x} = \frac{x - 2\sin x}{x \sin x}$$

Il nuovo quoziente presenta la forma $0/0.$ Il numeratore e il denominatore sono derivabili vicino a zero e il rapporto delle loro derivate è:

$$\frac{1 - 2\cos x}{\sin x + x\cos x}$$

Per $0 < |x| < \pi/2,$ i termini $\sin x$ e $x\cos x$ hanno lo stesso segno, quindi la loro somma non si annulla e l'ipotesi sulla derivata del denominatore è soddisfatta. Il numeratore tende a $-1,$ mentre il denominatore tende a zero e pertanto abbiamo:

$$
\lim_{x \to 0^+} \frac{1 - 2\cos x}{\sin x + x\cos x} = -\infty
$$

$$
\lim_{x \to 0^-} \frac{1 - 2\cos x}{\sin x + x\cos x} = +\infty
$$

Applichiamo quindi la regola di de l'Hôpital a ciascun limite laterale ottenendo:

$$
\lim_{x \to 0^+} \left(\frac{1}{\sin x} - \frac{2}{x}\right) = -\infty
$$

$$
\lim_{x \to 0^-} \left(\frac{1}{\sin x} - \frac{2}{x}\right) = +\infty
$$

I limiti laterali sono diversi, quindi il limite bilatero non esiste.

- - -

Mostriamo adesso un caso in cui confrontiamo la manipolazione algebrica con la sostituzione della regola di de l'Hôpital. Consideriamo il seguente limite:

$$\lim_{x \to 1} \frac{\sqrt{x} - 1}{x^2 - 1} \tag{9}$$

Per sostituzione diretta otteniamo la forma $0/0.$ Proviamo quindi ad eliminarla, come primo caso, con un procedimento algebrico scomponendo il denominatore. Possiamo riscrivere la $(9)$ come:

$$
\begin{align}
\lim_{x \to 1} \frac{\sqrt{x} - 1}{x^2 - 1}
&= \lim_{x \to 1} \frac{\sqrt{x} - 1}{(x + 1)(x - 1)} \\[6pt]
&= \lim_{x \to 1} \frac{\sqrt{x} - 1}{(x + 1)(\sqrt{x} - 1)(\sqrt{x} + 1)} \\[6pt]
&= \lim_{x \to 1} \frac{1}{(x + 1)(\sqrt{x} + 1)} \\[6pt]
&= \frac{1}{(1 + 1)(1 + 1)} = \frac{1}{4}
\end{align}
$$

In questo caso il calcolo con la regola di de l'Hôpital è più breve. Verifichiamo per prima cosa le condizioni del toerema:

+ le funzioni $f(x) = \sqrt{x} - 1$ e $g(x) = x^2 - 1$ sono derivabili per $x > 0.$
+ $g'(x) = 2x$ non si annulla in un intorno di $1.$ 
+ Il rapporto delle derivate è $1/(4x\sqrt{x}),$ che è continuo in $1$ e ha limite $1/4.$ 

Le ipotesi sono dunque valide, perciò applichiamo la $(3)$ ottenendo il limite in un solo passaggio:

$$
\begin{align}
\lim_{x \to 1} \frac{\sqrt{x} - 1}{x^2 - 1}
&= \lim_{x \to 1} \frac{\dfrac{1}{2\sqrt{x}}}{2x} \\[6pt]
&= \lim_{x \to 1} \frac{1}{4x\sqrt{x}} = \frac{1}{4}
\end{align}
$$

- - -

Consideriamo ora questo limite:

$$\lim_{x \to 0^+} x \ln x$$

Il prodotto presenta la forma indeterminata $0 \cdot (-\infty)$ che possiamo ricondurre alla forma $\infty/\infty$ a cui possiamo applicare la regola di de l'Hôpital:

$$\lim_{x \to 0^+} x \ln x = \lim_{x \to 0^+} \frac{\ln x}{\dfrac{1}{x}}$$

In questo modo, per sostituzione diretta il numeratore tende a $-\infty$ e il denominatore a $+\infty.$ Verificando le condizioni di applicabilità del teorema otteniamo che entrambe le funzioni sono derivabili per $x > 0,$ e la derivata del denominatore è $-1/x^2,$ quindi diversa da zero. Il rapporto delle derivate è $-x$ e tende a zero, quindi applichiamo la regola e otteniamo il limite:

$$
\begin{align}
\lim_{x \to 0^+} \frac{\ln x}{\dfrac{1}{x}}
&= \lim_{x \to 0^+} \frac{(\ln x)'}{\left(\dfrac{1}{x}\right)'} \\[6pt]
&= \lim_{x \to 0^+} \frac{\dfrac{1}{x}}{-\dfrac{1}{x^2}} \\[6pt]
&= \lim_{x \to 0^+} (-x) = 0
\end{align}
$$

## Forme indeterminate esponenziali

La regola di de l'Hôpital permette di trattare anche le seguenti forme indeterminate esponenziali:

$$0^0 \qquad \infty^0 \qquad 1^\infty$$

L'obiettivo è quello di procedere come nell'ultimo esempio, cercando cioè di ricondurle a una forma del tipo $0/0$ o $\infty/\infty$. Consideriamo ad esempio la tipica situazione data dalla seguente funzione esponenziale:

$$y = f(x)^{g(x)} \tag{10}$$

Supponendo $f(x) > 0$ nell'intorno considerato, possiamo applicare il logaritmo e riscrivere la $(10)$ in questo modo:

$$\ln y = g(x)\ln f(x) \tag{11}$$

Se inoltre $g(x) \neq 0$ nello stesso intorno, possiamo riscrivere la $(11)$ come quoziente a cui applicare la regola di de l'Hôpital in questo modo:

$$\ln y = g(x)\ln f(x) = \frac{\ln f(x)}{\dfrac{1}{g(x)}} \tag{12}$$

A questo punto, se le ipotesi sono soddisfatte, applichiamo la regola di de l'Hôpital alla $(12)$ per calcolare $L = \lim \ln y.$ Se $L$ è finito, per la continuità dell'esponenziale otteniamo:

$$\lim f(x)^{g(x)} = e^L \tag{13}$$

Consideriamo, per esempio:

$$\lim_{x \to 0^+} x^x$$

La base e l'esponente tendono entrambi a zero, quindi si presenta la forma indeterminata $0^0.$ Ponendo $y = x^x,$ abbiamo $\ln y = x\ln x.$ Nella sezione precedente abbiamo dimostrato che:

$$\lim_{x \to 0^+} x\ln x = 0$$

Applicando l'esponenziale otteniamo dalla $(13)$ il limite:

$$\lim_{x \to 0^+} x^x = e^0 = 1$$
