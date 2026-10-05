---
title: Little-o Notation
source: https://algebrica.org/little-o-notation/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - big-o-notation
  - landau-symbols
  - limits
  - little-o-notation
  - taylor-series
---
## o piccolo di una variabile

Quando si studia un limite, può essere utile confrontare il comportamento di due funzioni per capire come esse si comportano, ad esempio, quanto rapidamente crescono o tendono a zero, così da stabilire quali termini prevalgono e quali sono trascurabili. Questo confronto viene espresso attraverso i simboli di Landau, ovvero il cosiddetto "o piccolo" e "o grande" di una variabile reale o complessa.

Supponiamo di avere due funzioni $f(x), \ g(x) : A \to \mathbb{R}$ (se avete seguito fin qui gli argomenti presenti su Algebrica, dovreste ormai aver acquisito che $A$ è il dominio e $\mathbb{R}$ il codominio), e supponiamo che $x_0$ sia un punto di accumulazione di $A,$ ovvero un punto per cui ogni suo intorno contiene almeno un punto di $A$ diverso da $x_0.$ Si dice che $f(x)$ è un "o piccolo" di $g(x)$ per $x$ che tende a $x_0$ se vale la seguente relazione:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = 0 \tag{1}$$

La $(1)$ richiede che $g(x)$ sia diversa da zero e, in altri termini, si esprime con la notazione $f(x) = o(g(x))$ per $x \to x_0,$ per indicare proprio il concetto che $f(x)$ è trascurabile rispetto a $g(x)$ quando $x$ tende a $x_0.$ In generale, possiamo descrivere la classe di tutte le funzioni $f$ che soddisfano la $(1)$ nel seguente modo:

$$o_{x_0}(g) = \{\ f : A \to \mathbb{R} \mid \lim_{x \to x_0} \frac{f(x)}{g(x)} = 0 \ \}$$

Ma in termini formali, cosa significa "trascurabile"? Proviamo a precisarlo meglio richiamando la definizione stessa di limite, trattata nella relativa voce, per cui la differenza tra il rapporto della $(1)$ e lo zero deve diventare minore di un qualunque numero positivo assegnato quando $x$ è molto vicino a $x_0$. Questa distanza la esprimiamo, scegliendo un $\varepsilon$ piccolo a piacere, attraverso la seguente disuguaglianza:

$$\left|\frac{f(x)}{g(x)} - 0\right| < \varepsilon \tag{2}$$

Quindi, per ogni $\varepsilon > 0,$ esiste $\delta > 0$ tale che la $(2)$ vale per tutti i punti $x \in A$ che soddisfano la condizione:

$$0 < |x - x_0| < \delta \tag{3}$$

Per tutti i punti che soddisfano la $(3)$ vale dunque la $(2)$ che possiamo riscrivere come:

$$\frac{|f(x)|}{|g(x)|} < \varepsilon \tag{4}$$


In questo modo otteniamo:

$$|f(x)| < \varepsilon \cdot |g(x)| \tag{5}$$

Il legame con l'o piccolo sta nel fatto che possiamo rendere $|f(x)|$ inferiore a una frazione arbitrariamente piccola di $|g(x)|$ e questo spiega il significato di "trascurabile" rispetto a $g(x)$.

- - -

Per rendere più chiaro il concetto, consideriamo due funzioni, $f(x) = x^2$ e $g(x) = x$ e calcoliamo il limite del loro rapporto:

$$\lim_{x \to 0} \frac{x^2}{x} = 0$$

Poiché tale limite è zero, in accordo con la definizione della $(1)$ ricaviamo che $f(x)$ è un "o piccolo" di $g(x)$ e che per $x$ che tende a zero, vale:

$$x^2 = o(x)$$

La spiegazione è resa ancora più immediata dal seguente grafico. Quando $x \to 0,$ entrambi le funzioni tendono a zero, ma con velocità diverse. Infatti, in prossimità dell'origine, $x^2$ è molto più piccolo di $x$ in valore assoluto, come si può vedere dal grafico della curva corrispondente:


![IMG. 1](../svg/little-o-1.svg)


Per leggere questo confronto numericamente, prendiamo alcuni valori di $x$ sempre più vicini a zero e per ciascuno di essi calcoliamo $x^2$ e il rapporto $x^2/x:$

$$
\begin{array}{c|c|c}
x & x^2 & x^2/x \\[6pt]
\hline
0.1 & 0.01 & 0.1 \\[6pt]
0.01 & 0.0001 & 0.01 \\[6pt]
0.001 & 0.000001 & 0.001
\end{array}
$$

Procedendo, il quadrato diventa una frazione sempre più piccola rispetto a $x$ e questo quindi dimostra proprio che $x^2$ è trascurabile rispetto a $x,$ ossia che $x^2 = o(x)$ per $x \to 0.$

- - -

Consideriamo adesso un caso simile ma con la variabile $x$ che tende all'infinito. Calcoliamo il seguente limite:

$$\lim_{x \to \infty} \frac{x}{x^2} = \lim_{x \to \infty} \frac{1}{x} = 0$$

Anche in questo caso il rapporto tra le due funzioni $x$ e $x^2$ tende a zero, per cui dalla $(1)$ otteniamo, che per $x \to \infty,$ si ha:

$$x = o(x^2)$$

- - -

Vediamo un ultimo esempio, andando a calcolare questo limite:

$$\lim_{x \to \infty} \frac{\log x}{x} = 0$$

Poiché il rapporto è pari a zero, dalla $(1)$ segue che per $x \to \infty,$ $\log x = o(x).$ Questo risultato è molto utile perché ha una sua applicabilità pratica soprattutto nella costruzione degli algoritmi, in quanto la crescita logaritmica è trascurabile rispetto a quella lineare.

## Il significato di $o(1)$

Procediamo adesso con l'introduzione del simbolo $o(1)$ "o piccolo di 1" che rappresenta le funzioni che tendono a zero quando $x \to x_0.$ Possiamo dire che una funzione $f(x)$ appartiene a $o(1)$ quando è infinitesima rispetto alla costante $1$ in tale limite, ovvero vale la seguente uguaglianza:

$$\lim_{x \to x_0} \frac{f(x)}{1} = \lim_{x \to x_0} f(x) = 0 \tag{6}$$

In altri termini, sia $A \subseteq \mathbb{R}$ e sia $x_0$ un punto di accumulazione di $A.$ La classe delle funzioni definite su $A$ che sono o piccolo di $1$ per $x \to x_0$ si scrive come:

$$o_{x_0}(1) = \{\ f : A \to \mathbb{R} \mid \lim_{x \to x_0} f(x) = 0 \ \}$$

Facciamo subito un esempio considerando il seguente limite notevole:

$$\lim_{x \to 0} \frac{\sin x}{x}$$

Per calcolare il limite, usiamo lo sviluppo di Taylor, che permette di scrivere $\sin x$ come $x$ più un errore trascurabile rispetto a $x$ e per $x \to 0$ otteniamo: 

$$\sin x = x - \frac{x^3}{6} + o(x^3) \quad \text{per} \quad x \to 0 \tag{7}$$

Dividendo entrambi i membri per $x,$ la $(7)$ diventa:

$$\frac{\sin x}{x} = 1 - \frac{x^2}{6} + o(x^2) \tag{8}$$

Sia $-x^2/6$ che $o(x^2),$ tendono a zero per $x$ che tende a zero e poiché $o(1)$ indica proprio una quantità che tende a zero, possiamo riscrivere la $(8)$ come segue:

$$\frac{\sin x}{x} = 1 + o(1)$$


## Proprietà

Elenchiamo ora una serie di proprietà notevoli dell'o piccolo, utili nella risoluzione dei problemi tipici che si incontrano in questo ambito. La prima segue direttamente dalla definizione $(1)$ e cioè se $g(x) = o(f(x))$ per $x \to x_0,$ il rapporto tra le due funzioni tende a zero:

$$\lim_{x \to x_0} \frac{o(f(x))}{f(x)} = 0$$

Un'altra proprietà riguarda la moltiplicazione. Moltiplicare una funzione per una costante diversa da zero non modifica il suo comportamento asintotico nella notazione o piccolo e quindi, per ogni costante $c \in \mathbb{R}$ con $c \neq 0$ e ogni funzione $g(x),$ quando $x \to x_0,$ valgono le seguenti relazioni:

$$
\begin{align}
o(c \cdot g(x)) &= o(g(x)) \\[6pt]
c \cdot o(g(x)) &= o(g(x))
\end{align}
$$

Una proprietà analoga vale per l'addizione e cioè, la somma di due termini o piccolo della stessa funzione è ancora un termine o piccolo di quella funzione e vale:

$$o(f(x)) + o(f(x)) = o(f(x))$$

Ricordiamo che per l'algebra dei limiti, il limite di una somma è la somma dei limiti, e quindi la somma di due rapporti che tendono a zero tende anch'essa a zero. Consideriamo, ora, un'ulteriore proprietà che riguarda il prodotto di un o piccolo per una funzione. Moltiplicando un termine o piccolo di $g(x)$ per $f(x),$ con $f(x) \neq 0$ nei punti di $A$ sufficientemente vicini a $x_0$ e diversi da esso, otteniamo un termine o piccolo del prodotto $f(x)g(x),$ ovvero: 

$$f(x) \cdot o(g(x)) = o(f(x) g(x))$$

Per esempio, se $g(x) = x$ e $o(g(x)) = o(x),$ moltiplicando per $f(x) = x^2$ otteniamo:

$$x^2 \cdot o(x) = o(x^3)$$

Una proprietà analoga vale per le potenze. Se $f(x) = o(g(x))$ per $x \to x_0,$ con $f$ e $g$ non negative, allora per ogni esponente $a > 0$ vale, nello stesso limite:

$$[f(x)]^a = o([g(x)]^a)$$

A queste regole di calcolo si aggiunge la transitività della relazione o piccolo per cui se $f(x) = o(g(x))$ e $g(x) = o(h(x))$ per $x \to x_0,$ allora vale:

$$f(x) = o(h(x))$$

Anche questa relazione segue direttamente dalla definizione $(1)$, perché entrambi i rapporti tendono a zero e anche il loro prodotto tende quindi a zero. Infine, la transitività permette di ridurre due simboli o piccolo annidati a un solo simbolo. Se $h(x) = o(g(x))$ e $g(x) = o(f(x))$ per $x \to x_0,$ allora ogni funzione o piccolo di $g$ è anche o piccolo di $f,$ per cui vale la seguente relazione:

$$o(o(f(x))) = o(f(x))$$

## Differenza con la notazione O grande

Vale la pena citare brevemente, in questa pagina, la differenza tra la notazione o piccolo con la notazione O grande che è trattata nello specifico in una voce dedicata. In breve, quando $x$ si avvicina a $x_0,$ l'O grande richiede che il valore assoluto del rapporto tra le due funzioni non superi una costante, mentre l'o piccolo richiede che il rapporto tenda a zero.

Rispetto alla $(1),$ sostituiamo quindi la condizione di limite nullo con una disuguaglianza. Supponendo $g(x) \neq 0$ nei punti considerati, scriviamo $f(x) = O(g(x))$ per $x \to x_0$ se esistono costanti $M > 0$ e $\delta > 0$ tali che, per ogni $x \in A$ con $0 < |x - x_0| < \delta,$ vale:

$$\left|\frac{f(x)}{g(x)}\right| \leq M$$

In termini di inclusione tra insiemi, la classe delle funzioni che soddisfano $f = o(g)$ è strettamente contenuta nella classe delle funzioni che soddisfano $f = O(g).$ Ogni relazione o piccolo è anche una relazione O grande, ma il viceversa non vale.

## La notazione o piccolo negli sviluppi di Taylor

Un'applicazione più avanzata riguarda gli sviluppi asintotici dell'o piccolo e che merita un breve cenno perché estende l'uso già visto nell'esempio con $\sin x.$ In genere, in uno sviluppo asintotico, la notazione o piccolo descrive l'errore dovuto al troncamento in un certo grado. Data una funzione $f(x)$ derivabile $n$ volte in $x_0,$ il suo sviluppo di Taylor di ordine $n$ ha la forma:

$$f(x) = f(x_0) + f'(x_0)(x - x_0) + \frac{f''(x_0)}{2!}(x - x_0)^2 + \cdots + \frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + o\big( (x - x_0)^n \big)$$

Il simbolo $o((x - x_0)^n)$ rappresenta il resto e fornisce un'informazione asintotica della funzione, ovvero che l'errore tende a zero più rapidamente di $(x - x_0)^n$ per $x \to x_0$ ed è quindi trascurabile rispetto a questa potenza. Quando $f^{(n)}(x_0) \neq 0,$ l'errore è trascurabile anche rispetto all'ultimo termine esplicito dello sviluppo. Diversi sviluppi di Taylor vicino a $x = 0$ contengono un resto espresso mediante la notazione o piccolo come ad esempio i seguenti:

[class="table-1"]

|                  |                                                                       |
| ---------------- | --------------------------------------------------------------------- |
| $e^x$            | $1 + x + \dfrac{x^2}{2!} + \dfrac{x^3}{3!} + o(x^3)$                  |
| $\sin x$         | $x - \dfrac{x^3}{6} + o(x^3)$                                         |
| $\cos x$         | $1 - \dfrac{x^2}{2} + \dfrac{x^4}{24} + o(x^4)$                       |
| $\ln(1+x)$       | $x - \dfrac{x^2}{2} + \dfrac{x^3}{3} + o(x^3)$                        |
| $(1+x)^\alpha$   | $1 + \alpha x + \dfrac{\alpha(\alpha-1)}{2} x^2 + o(x^2)$              |

[/class]

Questi sviluppi sono utili perché permettono di calcolare limiti che presentano forme indeterminate, in quanto sostituendo una funzione con il suo sviluppo di Taylor, si ottiene un'espressione in cui il contributo del resto tende a zero. Per esempio:

$$\lim_{x \to 0} \frac{e^x - 1 - x}{x^2} = \lim_{x \to 0} \frac{\dfrac{x^2}{2} + o(x^2)}{x^2} = \frac{1}{2}$$

Per $x \to 0,$ il rapporto $o(x^2)/x^2$ tende a zero e il limite è quindi determinato dal coefficiente del termine di grado due.