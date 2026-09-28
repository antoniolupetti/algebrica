---
title: Fermat's Theorem
source: https://algebrica.org/fermat-theorem/
license: CC BY-NC 4.0
tags:
  - derivatives
  - differential-calculus-theorems
  - extrema
  - fermat-theorem
  - stationary-points
---

## Enunciato

Il teorema di Fermat è un importante teorema del calcolo differenziale e afferma che ogni punto di massimo e minimo locale interno al dominio di una funzione derivabile è un punto stazionario, ovvero un punto in cui la derivata prima della funzione è uguale a zero e la retta tangente è pertanto parallela all'asse delle $x$. Enunciamo il teorema in termini formali, considerando una funzione $y = f(x)$ definita su un intervallo chiuso e limitato $[a, b]$ e derivabile all'interno dell'intervallo aperto $(a, b).$ Se la $f(x)$ assume un massimo o un minimo locale in un punto $x_0 \in (a, b),$ allora la derivata della funzione in quel punto è nulla e vale:

$$
f'(x_0) = 0 \tag{1}
$$

Questa situazione è rappresentata dal seguente grafico che mostra una generica funzione $f(x)$ con un punto di massimo locale $\mu$ all'interno di un dato intervallo. In quel punto la retta tangente al grafico è orizzontale, parallela all'asse delle ascisse e quindi vale la $(1):$

![IMG. 1](../svg/fermat-theorem-1.svg)


Questa condizione è necessaria ma non sufficiente, poiché una derivata nulla in un punto non implica necessariamente che quel punto sia un massimo o un minimo. Questi punti infatti sono detti punti stazionari non estremanti e comprendono, ad esempio, i punti di flesso a tangente orizzontale, nei quali la derivata è nulla ma la funzione non cambia verso di monotonia.

> Una curiosità: il teorema di Fermat è importante anche perché si usa nella dimostrazione del teorema di Rolle, su cui si basa la dimostrazione del teorema di Lagrange e, attraverso questo, del teorema di Cauchy e della regola di de l'Hôpital per il calcolo dei limiti di alcune forme indeterminate come $0/0$ e $\infty/\infty.$

- - -

Procediamo con la dimostrazione della $(1)$, supponendo che in $x_0$ si abbia un punto di massimo locale $\mu$. Esiste quindi un intorno $I$ di $x_0$ in cui vale la seguente disuguaglianza:

$$
f(x) \leq f(x_0) \quad \forall \ x \in I \tag{2}
$$

Poniamo nella $(2)$ che $x = x_0 + h,$ con $h \neq 0$ e sufficientemente piccolo in valore assoluto affinché $x_0 + h$ appartenga all'intervallo $I$. Possiamo quindi riscrivere la $(2)$ come $f(x_0 + h) \leq f(x_0)$ e ottenere:

$$
f(x_0 + h) - f(x_0) \leq 0 \tag{3}
$$

Se osserviamo bene la $(3),$ possiamo riconoscere facilmente il numeratore del rapporto incrementale, utilizzato per definire le derivate. Se dividiamo per $h$ abbiamo due casi. Quando $h > 0$ otteniamo:

$$
\frac{f(x_0 + h) - f(x_0)}{h} \leq 0 \tag{4}
$$

Per $h < 0,$ invece, il segno della disuguaglianza cambia verso e otteniamo:

$$
\frac{f(x_0 + h) - f(x_0)}{h} \geq 0 \tag{5}
$$

Dalla definizione di derivata come limite del rapporto incrementale segue che i limiti della $(4)$ e della $(5)$ soddisfano le relazioni:

$$
\lim_{h \to 0^+} \frac{f(x_0 + h) - f(x_0)}{h} \leq 0 \tag{6}
$$

$$
\lim_{h \to 0^-} \frac{f(x_0 + h) - f(x_0)}{h} \geq 0 \tag{7}
$$

Poiché $f(x)$ è derivabile in $x_0,$ i limiti destro e sinistro esistono e coincidono proprio con la derivata, per cui dalla $(6)$ e dalla $(7)$ possiamo ottenere la conclusione del teorema per cui:

$$
f'(x_0) = 0
$$

La dimostrazione presentata considera che $x_0$ sia un punto di massimo locale. Se, invece, $x_0$ è un punto di minimo locale, la dimostrazione segue lo stesso procedimento, ma i versi delle disuguaglianze $(6)$ e $(7)$ si invertono, ottenendo la stessa conclusione.

## Esempio

Per mostrare un'applicazione pratica del teorema, consideriamo la seguente funzione polinomiale, continua e derivabile in tutto $\mathbb{R}:$

$$
f(x) = x^{3} - 3x^{2} + 2
$$

Assumendo che esista un massimo o un minimo locale in un punto interno del suo dominio, per il teorema di Fermat si ha che la derivata della funzione in quel punto è nulla. Per trovare il massimo o il minimo calcoliamo la derivata della funzione e verifichiamo quando si annulla:

$$ \tag{8}
\begin{align}
f'(x) &= 3x^{2} - 6x \\[6pt]
      &= 3x(x - 2)
\end{align}
$$

La $(8)$ si annulla per $x = 0$ e $x = 2.$ Ora dobbiamo determinare la natura di questi punti andando ad esaminare il comportamento della derivata nei tre possibili intervalli che questi punti determinano. Per $x < 0,$ la derivata è positiva e la funzione è crescente. Tra $0$ e $2,$ la derivata è negativa e la funzione è decrescente. Per $x > 2,$ la derivata è positiva e la funzione è di nuovo crescente.

![IMG. 2](../svg/fermat-theorem-4.svg)

[class="table-sign"]

La seguente tabella dei segni riassume il comportamento della derivata e la corrispondente monotonia della funzione.

|         |            |    $0$     |    $2$     |
| :-----: | :--------: | :--------: | :--------: |
| $f'(x)$ |    $+$     |    $-$     |    $+$     |
| $f(x)$  | $\nearrow$ | $\searrow$ | $\nearrow$ |

[/class]

Possiamo quindi concludere che la funzione ha un massimo locale in $x = 0$ e un minimo locale in $x = 2.$ Calcolando i corrispondenti valori della funzione, otteniamo $f(0) = 2$ e $f(2) = -2.$ Sul grafico, il punto di massimo locale ha dunque coordinate $(0, 2),$ mentre il punto di minimo locale ha coordinate $(2, -2).$

> Tenete presente che nell'esempio, il teorema di Fermat individua $x = 0$ e $x = 2$ come candidati a punti di estremo locale, mentre ciò che permette di classificarli come tali è il cambiamento di segno della derivata.

- - -

Come abbiamo già detto, non tutti i punti stazionari sono necessariamente punti di massimo o di minimo. Prendiamo, ad esempio, la funzione $f(x) = x^3$ e dimostriamo che una derivata nulla non implica necessariamente la presenza di un estremo locale.

![IMG. 3](../svg/fermat-theorem-2.svg)

Calcolando la derivata, otteniamo:

$$
f'(x) = 3x^2
$$

In $x = 0,$ si ha $f'(0) = 0$ e quindi $x = 0$ è un punto stazionario ma, sebbene la derivata sia nulla, il punto non è né di massimo né di minimo locale, come è anche evidente dal grafico. Ci troviamo infatti davanti a un punto di flesso a tangente orizzontale, in cui la derivata è nulla mentre la funzione rimane crescente in entrambi i lati.

## Il criterio della derivata seconda

Nell'esempio precedente abbiamo classificato i punti stazionari esaminando il segno della derivata prima. Un criterio alternativo per ottenere la stessa classificazione è dato dal calcolo della derivata seconda che fornisce una condizione sufficiente e non più solo necessaria. Consideriamo una funzione $f$ con derivata seconda in un intorno di un punto $x_0$ in cui $f'(x_0) = 0.$ In base al valore di $f''(x_0),$ possiamo distinguere tre casi.

+ Se $f''(x_0) > 0,$ allora $x_0$ è un punto di minimo locale di $f.$
+ Se $f''(x_0) < 0,$ allora $x_0$ è un punto di massimo locale di $f.$
+ Se $f''(x_0) = 0,$ il criterio non permette di concludere se $x_0$ sia un massimo o un minimo e, in questo caso, sono necessarie ulteriori informazioni.

Per dimostrare i primi due casi, confrontiamo il valore $f(x_0)$ con i valori della funzione nei punti vicini $x_0 + h.$ Per questo procediamo con uno sviluppo di Taylor del secondo ordine e otteniamo:

$$
f(x_0 + h) = f(x_0) + \tfrac{1}{2} f''(x_0) h^2 + o(h^2) \tag{9}
$$

Sottraiamo $f(x_0)$ e dividiamo per $h^2$ alla $(9),$ ottenendo:

$$
\frac{f(x_0 + h) - f(x_0)}{h^2} = \frac{1}{2}f''(x_0) + \frac{o(h^2)}{h^2} \tag{10}
$$

Quando $h \to 0,$ il termine $o(h^2)/h^2$ tende a zero e quindi la $(10)$ tende a $\frac{1}{2}f''(x_0).$ Se $f''(x_0) \neq 0,$ per $h \neq 0$ sufficientemente piccolo in valore assoluto il rapporto ha lo stesso segno di $f''(x_0)$ e di conseguenza valgono le seguenti conclusioni:

+ Se $f''(x_0) > 0,$ allora $f(x_0 + h) > f(x_0),$ quindi tutti i punti sufficientemente vicini a $x_0$ e diversi da esso hanno un valore della funzione maggiore di $f(x_0),$ e quindi $x_0$ è un punto di minimo locale.
+ Se $f''(x_0) < 0,$ vale il contrario e quindi $x_0$ è un punto di massimo locale.

- - -

Nel terzo caso, supponiamo che $f$ sia derivabile fino all'ordine $k$ in un intorno di $x_0$ e che $f^{(k)}(x_0)$ sia la prima derivata non nulla, con $k \geq 2.$ Distinguiamo due casi:

+ Se $k$ è pari, $x_0$ è un punto di minimo locale se $f^{(k)}(x_0) > 0$ o di massimo locale se $f^{(k)}(x_0) < 0.$
+ Se $k$ invece è dispari, $x_0$ è un punto di flesso a tangente orizzontale e non è un punto di estremo.

Riprendiamo, ad esempio, la funzione $f(x) = x^3,$ già considerata in precedenza. Nel punto $x = 0$ la derivata prima e la derivata seconda si annullano, quindi il punto è stazionario ma il criterio della derivata seconda non permette di classificarlo. Calcoliamo allora la derivata terza, che vale $f'''(0) = 6.$ Quindi, la prima derivata non nulla nel punto è di ordine $k = 3,$ ed essendo l'ordine dispari, allora $x = 0$ è un punto di flesso a tangente orizzontale.

Facciamo un altro esempio considerando la funzione $f(x) = x^4.$ Anche in questo caso la derivata prima e la derivata seconda si annullano in $x = 0,$ ma proseguendo il calcolo anche $f'''(0) = 0.$ Calcolando la derivata quarta invece otteniamo il valore $f^{(4)}(0) = 24.$ Quindi la prima derivata non nulla nel punto è questa volta di ordine pari, $k = 4$ e il suo valore è positivo, quindi si può concludere che $x = 0$ è un punto di minimo locale.

## Perché le ipotesi sono necessarie

Negli esempi precedenti abbiamo cercato gli estremi tra i punti stazionari e poi ne abbiamo studiato la natura. Per applicare il teorema di Fermat a un punto di estremo locale, occorre che il punto sia interno al dominio e che la funzione sia derivabile in quel punto. I seguenti esempi mostrano cosa accade quando una di queste condizioni manca. Consideriamo la funzione valore assoluto, definita su tutta la retta reale dalla formula:

$$
y = f(x) = |x| =
\begin{cases}
+x & \text{se } x \ge 0\\[4pt]
-x & \text{se } x < 0
\end{cases}
$$

Poiché $|x| \geq 0$ per ogni $x \in \mathbb{R}$ e $f(0) = 0,$ la funzione ha un minimo assoluto in $x = 0.$ Questo punto è interno al dominio, ma in quel punto la funzione non è derivabile in quanto la derivata sinistra vale $-1,$ mentre la derivata destra vale $1.$ Come si può vedere anche dal grafico, abbiamo che esiste un punto di minimo ma manca l'ipotesi di derivabilità richiesta dal teorema.

![IMG. 4](../svg/fermat-theorem-3.svg)

Facciamo un ulteriore esempio, considerando ora la funzione $f(x) = x,$ e limitandone il dominio all'intervallo $[0,1].$ La funzione assume quindi un minimo assoluto in $(0,0),$ e il massimo assoluto in $(1,1),$ eppure la derivata vale $f'(x) = 1$ in tutto l'intervallo aperto $(0,1),$ e quindi non ci sono punti stazionari. Quindi il teorema di Fermat non si applica ai punti $x = 0$ e $x = 1,$ perché non sono interni all'intervallo.