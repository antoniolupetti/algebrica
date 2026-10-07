---
title: Big-O Notation
source: https://algebrica.org/big-o-notation/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - big-o-notation
  - landau-symbols
  - limits
  - little-o-notation
  - taylor-series
---
## O grande di una variabile

Nella voce relativa al simbolo "o piccolo" abbiamo introdotto i cosiddetti simboli di Landau, che consentono di esprimere il comportamento asintotico di due funzioni attraverso lo studio del limite del loro rapporto. In questa pagina, introduciamo la notazione "O grande" nel seguente modo: supponiamo di avere due funzioni $f, g : A \to \mathbb{R},$ con $A \subseteq \mathbb{R},$ e che $x_0$ sia un punto di accumulazione di $A,$ ovvero un punto per cui ogni suo intorno contiene almeno un punto di $A$ diverso da $x_0.$ Supponiamo inoltre che $g(x)$ sia diversa da zero nei punti di $A$ vicini a $x_0$ e diversi da esso. Si dice che $f(x)$ è un "O grande" di $g(x)$ per $x$ che tende a $x_0$ se esiste una costante $M > 0$ tale che, per tutti questi punti, vale la disuguaglianza:

$$\left|\frac{f(x)}{g(x)}\right| \leq M \tag{1}$$

La $(1)$ si esprime con la notazione $f(x) = O(g(x))$ per $x \to x_0.$ La classe di tutte le funzioni $f$ che soddisfano questa condizione si può esprimere anche nel seguente modo:

$$O_{x_0}(g) = \{\ f : A \to \mathbb{R} \mid \limsup_{\substack{x \to x_0 \\ x \in A}} \left|\frac{f(x)}{g(x)}\right| < +\infty \ \}$$


Per precisare cosa significa "vicino a $x_0$", fissiamo una soglia $\delta > 0$ entro cui deve rimanere la distanza tra $x$ e $x_0,$ data da $|x - x_0|.$ La $(1)$ richiede quindi che si possano scegliere una costante $M > 0$ e un numero $\delta > 0$ in modo che la maggiorazione $(1)$ valga per tutti i punti di $A$ in questo intorno, escluso $x_0,$ in modo che valga la seguente relazione:

$$0 < |x - x_0| < \delta \tag{2}$$

Per tutti i punti che soddisfano la $(2),$ possiamo riscrivere la $(1)$ usando la proprietà del valore assoluto di un rapporto:

$$\frac{|f(x)|}{|g(x)|} \leq M \tag{3}$$

Poiché $|g(x)| > 0,$ moltiplicando entrambi i membri della $(3)$ per $|g(x)|$ otteniamo:

$$|f(x)| \leq M|g(x)| \tag{4}$$

Per chiarire il concetto, consideriamo le funzioni $f(x) = x^2$ e $g(x) = x$ per $x \to 0.$ Per $x \neq 0,$ il valore assoluto del loro rapporto è:

$$\left|\frac{x^2}{x}\right| = |x|$$

Se $0 < |x| < 1,$ questo rapporto è minore di $1.$ La $(1)$ è quindi soddisfatta con $M = 1$ e $\delta = 1,$ da cui segue che per $x$ che tende a zero si ha:

$$x^2 = O(x)$$

Per fare un confronto numerico, prendiamo alcuni valori positivi di $x$ sempre più vicini a zero e calcoliamo $x^2$ e il rapporto $x^2/x.$ Otteniamo:

$$
\begin{array}{c|c|c}
x & x^2 & x^2/x \\[6pt]
\hline
0.1 & 0.01 & 0.1 \\[6pt]
0.01 & 0.0001 & 0.01 \\[6pt]
0.001 & 0.000001 & 0.001
\end{array}
$$

Il rapporto rimane limitato e tende a zero, perciò, richiamando la definizione di o piccolo sono vere entrambe le relazioni $x^2 = O(x)$ e $x^2 = o(x)$ per $x \to 0.$

- - -

Consideriamo ora il limite per $x \to +\infty.$ In questo caso, la condizione $(2)$ viene sostituita da $x > N,$ dove $N > 0$ è un valore oltre il quale deve valere la maggiorazione della $(3)$. Per le funzioni $f(x) = x$ e $g(x) = x^2,$ quando $x > 1$ otteniamo:

$$\left|\frac{x}{x^2}\right| = \frac{1}{x} \leq 1$$

La $(1)$ vale con $M = 1$ e $N = 1,$ per cui $x = O(x^2)$ per $x \to \infty.$

- - -

Un ulteriore esempio è dato dal confronto tra $\log x$ e $x$ per cui si ha:

$$\lim_{x \to \infty} \frac{\log x}{x} = 0$$

Poiché una funzione che tende a zero rimane limitata per valori sufficientemente grandi di $x,$ dalla $(1)$ segue che $\log x = O(x)$ per $x \to \infty.$ Come nell'esempio di $x^2$ e $x$ per $x \to 0,$ il rapporto tende a zero e soddisfa quindi anche la definizione di o piccolo. Possiamo dunque scrivere $\log x = o(x)$ per $x \to \infty.$ Quest'ultima relazione fornisce un'informazione aggiuntiva rispetto all'O grande, perché afferma che $\log x$ è trascurabile rispetto a $x,$ mentre l'O grande richiede soltanto che il rapporto rimanga limitato.

- - -

Per vedere un caso in cui il rapporto non tende a zero, consideriamo il seguente polinomio che vogliamo confrontare con $x^2$ per $x \to \infty.$ 

$$f(x) = 3x^2 + 2x + 1$$

Dividendo ciascun termine per $x^2,$ otteniamo:

$$\frac{3x^2 + 2x + 1}{x^2} = 3 + \frac{2}{x} + \frac{1}{x^2} \tag{5}$$

Passando al limite, per $x$ che tende a $+\infty$ il rapporto nella $(5)$ tende a $3$ e quindi il rapporto rimane limitato. Ora, per verificare la definizione di O grande, applichiamo la $(3)$ e cerchiamo una costante $M > 0$ tale che il rapporto non superi $M$ per tutti i valori di $x$ sufficientemente grandi. Poiché stiamo considerando il limite per $x \to \infty,$ possiamo quindi limitarci ai valori $x \geq 1.$ Poiché $x \geq 1,$ anche $x^2 \geq 1.$ I denominatori sono quindi almeno $1,$ da cui deriva $2/x \leq 2$ e $1/x^2 \leq 1.$ Sommando queste maggiorazioni nell $(3),$ otteniamo:

$$\frac{3x^2 + 2x + 1}{x^2} \leq 3 + 2 + 1 = 6$$

La definizione è quindi soddisfatta con $M = 6$ e quindi possiamo concludere che per $x$ che tende a $+\infty$ vale:

$$3x^2 + 2x + 1 = O(x^2)$$

Moltiplicando la disuguaglianza precedente per $x^2 > 0,$ otteniamo $f(x) \leq 6x^2$ per $x \geq 1.$ Il Seguente grafico illustra questa maggiorazione, confrontando il polinomio con la funzione $6x^2,$ ottenuta moltiplicando $g(x) = x^2$ per la costante $M = 6.$

![IMG. 1](../svg/big-o-notation-1.svg)

Questa maggiorazione si può verificare anche su alcuni valori numerici, ad esempio:

$$
\begin{array}{c|c|c}
x & f(x) & 6x^2 \\[6pt]
\hline
10 & 321 & 600 \\[6pt]
100 & 30201 & 60000 \\[6pt]
1000 & 3002001 & 6000000
\end{array}
$$

- - -

È utile evidenziare che, rispetto alla notazione o piccolo, la notazione O grande richiede che il valore assoluto del rapporto tra due funzioni rimanga limitato, mentre la notazione o piccolo richiede che il rapporto tenda a zero. La condizione $(1)$ viene quindi sostituita dalla condizione più stringente:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = 0$$

Se questo limite è zero, il rapporto rimane limitato vicino a $x_0,$ quindi ogni relazione $f(x) = o(g(x))$ implica che $f(x) = O(g(x)).$ In termini insiemistici, si può affermare che la classe delle funzioni che soddisfano $f = o(g)$ è strettamente contenuta nella classe delle funzioni che soddisfano $f = O(g),$ mentre il viceversa non vale.


## Il significato di $O(1)$

Il simbolo $O(1),$ che si legge "O grande di 1", indica le funzioni che rimangono limitate quando $x \to x_0.$ Applicando la $(1)$ alla funzione costante $g(x) = 1,$ diciamo che $f(x) = O(1)$ se esistono $M > 0$ e $\delta > 0$ tali che, per ogni punto $x \in A$ che soddisfa la $(2),$ vale la seguente relazione:

$$\left|\frac{f(x)}{1}\right| = |f(x)| \leq M \tag{6}$$

In altri termini, sia $A \subseteq \mathbb{R}$ e sia $x_0$ un punto di accumulazione di $A.$ La classe delle funzioni definite su $A$ che sono O grande di $1$ per $x \to x_0$ si scrive come:

$$O_{x_0}(1) = \{\ f : A \to \mathbb{R} \mid \limsup_{\substack{x \to x_0 \\ x \in A}} |f(x)| < +\infty \ \}$$

Consideriamo, ad esempio, la seguente funzione, definita per $x \neq 0:$

$$f(x) = \sin\left(\frac{1}{x}\right)$$

Il seno assume valori compresi tra $-1$ e $1$ e anche quando l'argomento è $1/x,$ il suo valore assoluto non supera quindi $1,$ perciò per ogni $x \neq 0$ vale:

$$\left|\sin\left(\frac{1}{x}\right)\right| \leq 1 \tag{7}$$

La $(7)$ è proprio la condizione $(6)$ con $M = 1.$ Essa vale, in particolare, per tutti i punti con $0 < |x| < 1,$ quindi possiamo scegliere $\delta = 1.$ La definizione è soddisfatta e concludiamo che per $x$ che tende a zero vale::

$$\sin\left(\frac{1}{x}\right) = O(1)$$

## Proprietà

Illustriamo di seguito alcune priorità utili nelle manipolazioni algebriche che riguardano il calcolo del simbolo O grande. La prima segue dalla definizione $(1).$ Se $f(x) = O(g(x))$ per $x \to x_0$ e $g(x)$ è diversa da zero in un intorno bucato di $x_0$ relativo ad $A,$ il rapporto rimane limitato in valore assoluto. Questa condizione si scrive come:

$$\limsup_{x \to x_0} \left|\frac{f(x)}{g(x)}\right| < \infty$$

Il limite superiore che deve essere finito, esprime la limitatezza del rapporto, anche quando il limite non esiste, come nell'esempio precedente con $\sin(1/x).$ Un'altra proprietà riguarda la moltiplicazione di una funzione $g$ per una costante $c \in \mathbb{R}$ con $c \neq 0$ quando $x \to x_0$ per cui valgono le seguenti relazioni:

$$
\begin{align}
O(cg(x)) &= O(g(x)) \\[6pt]
cO(g(x)) &= O(g(x))
\end{align}
$$

Una proprietà analoga vale per l'addizione:

$$O(f(x)) + O(f(x)) = O(f(x))$$

Se due funzioni sono maggiorate in valore assoluto rispettivamente da $M_1|f(x)|$ e $M_2|f(x)|,$ per la disuguaglianza triangolare sappiamo che la loro somma è maggiorata in valore assoluto da $(M_1 + M_2)|f(x)|.$ Consideriamo ora il prodotto di un termine $O(g(x))$ per $f(x)$ e otteniamo la seguente relazione:

$$f(x)O(g(x)) = O(f(x)g(x))$$

Infatti, se $|r(x)| \leq M|g(x)|,$ allora $|f(x)r(x)| \leq M|f(x)g(x)|.$ Ad esempio, scegliendo $g(x) = x$ e moltiplicando un termine $O(x)$ per $f(x) = x^2,$ si ha che:

$$x^2O(x) = O(x^3)$$

Una proprietà analoga, che deriva dall'elevamento a potenza $a$ di entrambi i membri della $(4)$, vale anche per le potenze, ovvero se $f(x) = O(g(x))$ per $x \to x_0,$ con $f$ e $g$ non negative, allora per ogni esponente $a > 0$ vale:

$$[f(x)]^a = O([g(x)]^a) \tag{8}$$


A queste regole di calcolo si aggiunge la propreità transitività, per la quale se $f(x) = O(g(x))$ e $g(x) = O(h(x))$ per $x \to x_0,$ allora vale anche che:

$$f(x) = O(h(x))$$

Per ipotesi, infatti, esistono due costanti positive $M_1$ e $M_2$ tali che $|f(x)| \leq M_1|g(x)|$ e $|g(x)| \leq M_2|h(x)|$ in opportuni intorni bucati di $x_0.$ Considerando l'intersezione di questi intorni e combinando le due disuguaglianze, otteniamo $|f(x)| \leq M_1M_2|h(x)|.$

La transitività permette anche di ridurre due simboli O grande annidati a uno solo e in questo senso si può scrivere:

$$O(O(f(x))) = O(f(x))$$

## La notazione O grande negli sviluppi di Taylor

Negli sviluppi asintotici, la notazione O grande descrive l'errore dovuto al troncamento mediante una maggiorazione. In altre parole, se una funzione $f$ è derivabile $n+1$ volte in un intorno di $x_0,$ il suo sviluppo di Taylor di ordine $n$ ha la forma:

$$f(x) = f(x_0) + f'(x_0)(x - x_0) + \frac{f''(x_0)}{2!}(x - x_0)^2 + \cdots + \frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + O\big((x - x_0)^{n+1}\big)$$

Il simbolo $O((x - x_0)^{n+1})$ indica che il valore assoluto del resto è maggiorato da un multiplo costante di $|x - x_0|^{n+1}$ per $x \to x_0$ ed è quindi controllato dalla prima potenza omessa. La tabella seguente raccoglie alcuni sviluppi vicino a $x = 0$ con un resto espresso mediante la notazione O grande. Nell'ultima riga, $\alpha$ è un esponente reale fissato.

[class="table-1"]

|                  |                                                                       |
| ---------------- | --------------------------------------------------------------------- |
| $e^x$            | $1 + x + \dfrac{x^2}{2!} + \dfrac{x^3}{3!} + O(x^4)$                  |
| $\sin x$         | $x - \dfrac{x^3}{6} + O(x^5)$                                         |
| $\cos x$         | $1 - \dfrac{x^2}{2} + \dfrac{x^4}{24} + O(x^6)$                       |
| $\ln(1+x)$       | $x - \dfrac{x^2}{2} + \dfrac{x^3}{3} + O(x^4)$                        |
| $(1+x)^\alpha$   | $1 + \alpha x + \dfrac{\alpha(\alpha-1)}{2} x^2 + O(x^3)$              |

[/class]

Questi sviluppi sono utili perché permettono di calcolare limiti che presentano forme indeterminate. Consideriamo, ad esempio, il seguente limite che per sostituzione diretta non è risolvibile:

$$\lim_{x \to 0} \frac{e^x - 1 - x}{x^2}$$ 

Se sostituiamo $e^x$ con il suo sviluppo fino al termine di grado due, possiamo riscriverlo come:

$$\lim_{x \to 0} \frac{\dfrac{x^2}{2} + O(x^3)}{x^2} = \frac{1}{2}$$

Dopo la divisione per il denominatore, il resto $O(x^3)$ diventa un termine $O(x),$ il cui valore assoluto è maggiorato da $M|x|$ e tende quindi a zero e quindi il limite è determinato dal coefficiente del termine di grado due.
