---
title: Improper Integrals
source: https://algebrica.org/improper-integrals/
license: CC BY-NC 4.0
tags:
  - absolute-convergence
  - comparison-test
  - continuous-functions
  - convergence
  - definite-integral
  - divergence
  - improper-integrals
  - integration
  - limits
  - p-integral-test
  - riemann-integral
  - unbounded-intervals
---
## Introduzione

Un integrale improprio è un [integrale definito](../definite-integrals/) in cui l'intervallo di integrazione è illimitato, la funzione integranda è illimitata in uno o più punti, oppure entrambe le cose. Nel calcolo elementare l'integrale definito si scrive:

$$\int_a^b f(x) \ dx$$

La sua definizione usuale richiede che l'intervallo $[a,b]$ sia limitato e che la funzione $f$ sia [continua](../continuous-functions/), o almeno [integrabile secondo Riemann](../riemann-integrability-criteria/), su quell'intervallo. Un [intervallo illimitato](../intervals/), come $(a,+\infty),$ oppure una funzione integranda illimitata cadono fuori da queste ipotesi. L'integrale viene allora definito attraverso uno o più limiti.

> Un integrale improprio è un limite di integrali di Riemann ordinari. La convergenza va verificata separatamente in ogni estremo improprio e in ogni punto singolare.

- - -

Un'applicazione formale del [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/) alla seguente espressione produce un risultato non valido:

$$\int_{-1}^{1} \frac{1}{x^2} \ dx$$

Il calcolo $\left[-x^{-1}\right]_{-1}^{1}=-2$ non è valido perché $1/x^2$ è illimitata in $x=0,$ e il teorema fondamentale non si applica attraverso quel punto. Poiché la funzione integranda è positiva, un valore negativo rivela già l'errore. Dopo aver spezzato l'intervallo in $0,$ entrambi gli integrali impropri unilaterali divergono a $+\infty.$

## Integrali impropri su intervalli illimitati

Supponiamo che $f$ sia integrabile secondo Riemann su ogni intervallo $[a,t]$ con $t>a.$ L'integrale improprio su $[a,+\infty)$ è definito dal [limite](../limits/):

$$\int_a^{+\infty} f(x) \ dx := \lim_{t \to +\infty} \int_a^t f(x) \ dx$$

Ogni integrale ordinario ha estremo superiore finito $t,$ e la definizione passa al limite per $t\to+\infty.$

![Img. 1](svg/improper-integrals-1.svg)

+ Quando il limite esiste ed è finito, l'integrale converge.
+ Quando il limite non esiste come numero reale finito, l'integrale diverge.

- - -

La stessa idea vale quando l'estremo inferiore è $-\infty.$ Supponiamo che $f$ sia integrabile secondo Riemann su ogni intervallo $[t,b]$ con $t<b.$ La definizione corrispondente è:

$$\int_{-\infty}^b f(x) \ dx := \lim_{t \to -\infty} \int_t^b f(x) \ dx$$

Supponiamo che $f$ sia integrabile secondo Riemann su ogni intervallo limitato. Per un integrale esteso a tutta la retta reale nessuno dei due estremi è finito, quindi un solo limite non basta. Si sceglie un punto qualsiasi $c$ e si pone:

$$\int_{-\infty}^{+\infty} f(x) \ dx := \int_{-\infty}^c f(x) \ dx + \int_c^{+\infty} f(x) \ dx$$

L'integrale improprio sulla retta reale converge solo quando entrambi gli integrali a destra convergono separatamente. In tal caso il risultato non dipende dalla scelta di $c.$

## Esempio 1

Calcoliamo il seguente integrale:

$$\int_1^{+\infty} \frac{1}{x^2} \ dx$$

Per $b>1,$ l'integrale ordinario è:

$$\int_1^b \frac{1}{x^2} \ dx = \int_1^b x^{-2} \ dx = \left[ -x^{-1} \right]_1^b = -\frac{1}{b} + 1$$

Poiché $1/b\to0$ per $b\to+\infty,$ il limite che definisce l'integrale è:

$$\lim_{b \to +\infty} \left(1 - \frac{1}{b}\right) = 1$$

Il limite è finito, quindi l'integrale improprio converge a $1.$

## Esempio 2

L'integrale analogo con esponente $1$ è:

$$\int_1^{+\infty} \frac{1}{x} \ dx$$

Per $b>1,$ l'integrale ordinario è:

$$\int_1^b \frac{1}{x} \ dx = \left[ \ln x \right]_1^b = \ln b$$

Il limite che lo definisce è:

$$\lim_{b \to +\infty} \ln b = +\infty$$

Il limite è infinito, quindi l'integrale diverge.

## Integrali impropri con discontinuità infinite

Un secondo tipo di integrale improprio si presenta quando $f$ è illimitata in qualche punto dell'intervallo. Supponiamo che $f$ diventi illimitata per $x \to a^+$ ma sia integrabile secondo Riemann su ogni intervallo $[t,b]$ con $a<t<b.$ L'integrale improprio è definito da:

$$\int_a^b f(x) \ dx := \lim_{t \to a^+} \int_t^b f(x) \ dx$$

L'integrale improprio converge quando il limite esiste ed è finito. Simmetricamente, supponiamo che $f$ diventi illimitata per $x \to b^-$ ma sia integrabile secondo Riemann su ogni intervallo $[a,t]$ con $a<t<b.$ La definizione corrispondente è:

$$\int_a^b f(x) \ dx := \lim_{t \to b^-} \int_a^t f(x) \ dx$$

Supponiamo che $c\in(a,b)$ sia l'unico punto singolare e che $f$ sia integrabile secondo Riemann su ogni intervallo $[a,t]$ con $a<t<c$ e su ogni intervallo $[s,b]$ con $c<s<b.$ La definizione impiega due limiti unilaterali indipendenti:

$$
\int_a^b f(x) \ dx
:=\lim_{t\to c^-}\int_a^t f(x) \ dx
+\lim_{s\to c^+}\int_s^b f(x) \ dx
$$

L'integrale improprio converge solo quando entrambi i limiti unilaterali esistono e sono finiti.

Se un integrale presenta più estremi impropri o più punti singolari, si scelgono punti di taglio regolari in modo che ogni pezzo unilaterale abbia una sola sorgente di improprietà. L'integrale di partenza converge se e solo se converge ogni pezzo.

## Esempio 3

La funzione integranda del seguente integrale è illimitata nell'estremo inferiore:

$$\int_0^1 \frac{1}{\sqrt{x}} \ dx$$

Poiché $1/\sqrt{x}$ è illimitata per $x\to0^+,$ la definizione usa un estremo inferiore $t>0$ e il limite per $t\to0^+$:

$$\int_0^1 \frac{1}{\sqrt{x}} \ dx := \lim_{t \to 0^+} \int_t^1 x^{-1/2} \ dx$$

La primitiva è:

$$\int x^{-1/2} \ dx = 2x^{1/2} + C$$

Per $t>0,$ l'integrale ordinario è:

$$\int_t^1 x^{-1/2} \ dx = 2 - 2\sqrt{t}$$

Il limite che definisce l'integrale è:

$$\lim_{t \to 0^+} (2 - 2\sqrt{t}) = 2$$

Il limite esiste ed è finito, quindi l'integrale converge e vale $2.$

## Il criterio dell'integrale $p$

Il criterio dell'integrale $p$ classifica la famiglia:

$$\int_1^{+\infty} \frac{1}{x^p} \ dx \tag{1}$$

Il parametro $p$ è reale e la convergenza dipende dal suo valore. Quando $p\neq1,$ l'integrale ordinario è:

$$\int_1^b x^{-p} \ dx = \left[ \frac{x^{1-p}}{1-p} \right]_1^b = \frac{b^{1-p} - 1}{1 - p}$$

Il passaggio al limite per $b \to +\infty$ produce tre casi:

[class="table-1"]

|         |                       |                              |
| ------- | --------------------- | ---------------------------- |
| $p > 1$ | $b^{1-p} \to 0$       | converge a $\dfrac{1}{p - 1}$ |
| $p = 1$ | $\ln b \to +\infty$   | diverge                      |
| $p < 1$ | $b^{1-p} \to +\infty$ | diverge                      |

[/class]

L'integrale $(1)$ converge se e solo se $p>1.$ L'integrale corrispondente vicino all'origine è:

$$\int_0^1 \frac{1}{x^p} \ dx \tag{2}$$

Nell'origine il comportamento all'estremo si inverte. La funzione integranda è singolare in $x=0$ solo quando $p>0,$ mentre l'integrale $(2)$ converge se e solo se $p<1.$

> Queste [funzioni potenza](../powers/) sono i casi di riferimento per i criteri del confronto esposti di seguito.

## Convergenza e criteri del confronto

I criteri del confronto stabiliscono la convergenza senza una primitiva e senza il valore esatto dell'integrale.

Il criterio del confronto diretto usa una maggiorazione puntuale. Supponiamo che $f$ e $g$ siano integrabili secondo Riemann su ogni sottointervallo limitato di $[a,+\infty)$ e che $0\leq f(x)\leq g(x)$ per ogni $x\geq a$:

+ Se $\int_a^{+\infty} g(x) \ dx$ converge, converge anche $\int_a^{+\infty} f(x) \ dx.$
+ Se $\int_a^{+\infty} f(x) \ dx$ diverge, diverge anche $\int_a^{+\infty} g(x) \ dx.$

![Img. 2](svg/improper-integrals-2.svg)

> Per ogni $b>a$ la disuguaglianza $0\leq f\leq g$ dà $0\leq\int_a^b f(x) \ dx\leq\int_a^b g(x) \ dx.$ Il passaggio al limite dimostra la prima implicazione, e la seconda segue per contrapposizione.

Il criterio del confronto asintotico sostituisce la maggiorazione puntuale con un rapporto asintotico. Supponiamo che $f$ e $g$ siano positive e integrabili secondo Riemann su ogni sottointervallo limitato di $[a,+\infty),$ e che il loro rapporto abbia limite:

$$\lim_{x \to +\infty} \frac{f(x)}{g(x)} = L \qquad 0 < L < +\infty$$

Allora $\int_a^{+\infty} f(x) \ dx$ e $\int_a^{+\infty} g(x) \ dx$ convergono entrambi oppure divergono entrambi. In modo equivalente $f(x)\sim Lg(x)$ per $x\to+\infty;$ l'equivalenza asintotica di $f$ e $g$ è il caso particolare $L=1.$ Scegliendo $g(x)=1/x^p$ la questione si riconduce al criterio dell'integrale $p.$

I valori degeneri di $L$ danno implicazioni in un solo verso:

+ Se $L=0$ e $\int_a^{+\infty} g(x) \ dx$ converge, allora $\int_a^{+\infty} f(x) \ dx$ converge.
+ Se $L=+\infty$ e $\int_a^{+\infty} g(x) \ dx$ diverge, allora $\int_a^{+\infty} f(x) \ dx$ diverge.

Se $f$ e $g$ sono positive e integrabili secondo Riemann su ogni intervallo compatto contenuto in un lato di un punto finito $c,$ le stesse conclusioni valgono per i corrispondenti integrali impropri unilaterali quando $x\to c^+$ oppure $x\to c^-.$ Il modello potenza di riferimento è $1/|x-c|^p,$ il cui integrale su ciascun lato di $c$ converge se e solo se $p<1.$

## Procedura di decisione

Per stabilire la convergenza si eseguono i seguenti controlli.

+ Individuare ogni sorgente di improprietà, cioè un intervallo illimitato, una funzione integranda illimitata in un estremo e ogni singolarità in un punto interno.
+ Se è disponibile una primitiva, applicare la definizione a ciascun pezzo improprio. La [regola di de l'Hôpital](../hopital-rule/) può aiutare con un quoziente indeterminato quando le sue ipotesi sono soddisfatte.
+ Per una funzione integranda non negativa, usare il criterio del confronto diretto quando si dispone di una maggiorazione puntuale mediante una funzione di riferimento.
+ Se la maggiorazione puntuale non è disponibile e la funzione integranda è definitivamente positiva, usare il criterio del confronto asintotico quando il suo rapporto con una funzione di riferimento ha uno dei limiti descritti sopra. I modelli usuali sono $1/x^p$ all'infinito e $1/|x-c|^p$ vicino a un punto singolare finito.
+ Spezzare un integrale con più sorgenti di improprietà in pezzi unilaterali e richiedere che ogni pezzo converga.

## Esempio 4

Consideriamo il seguente integrale:

$$\int_1^{+\infty} \frac{1}{x^2 + 1} \ dx$$

La funzione integranda ha primitiva $\arctan x,$ ma il confronto dimostra la convergenza senza calcolare l'integrale improprio. Il rapporto di confronto è:

$$\lim_{x \to +\infty} \frac{\dfrac{1}{x^2 + 1}}{\dfrac{1}{x^2}} = \lim_{x \to +\infty} \frac{x^2}{x^2 + 1} = 1$$

Il rapporto tende a $1,$ quindi i due integrali convergono o divergono insieme:

$$\int_1^{+\infty} \frac{1}{x^2 + 1} \ dx \qquad \int_1^{+\infty} \frac{1}{x^2} \ dx$$

Il secondo integrale converge per il criterio dell'integrale $p$ perché $p=2>1.$ Di conseguenza converge anche il primo.

## Esempio 5

Consideriamo il seguente integrale:

$$\int_2^{+\infty} \frac{\cos^2 x}{x^2} \ dx$$

Poiché $0 \leq \cos^2 x \leq 1$ per ogni $x,$ la funzione integranda soddisfa:

$$0 \leq \frac{\cos^2 x}{x^2} \leq \frac{1}{x^2}$$

Poiché $p=2>1,$ il criterio dell'integrale $p$ dà:

$$\int_2^{+\infty} \frac{1}{x^2} \ dx<+\infty$$

Il criterio del confronto diretto dà allora:

$$\int_2^{+\infty} \frac{\cos^2 x}{x^2} \ dx<+\infty$$

L'integrale di partenza converge.

## Esempio 6

Fissato $\beta>0,$ determiniamo i valori di $\alpha\in\mathbb{R}$ per cui il seguente integrale converge:

$$I_{\alpha,\beta}:=\int_0^{+\infty}\frac{x^\alpha}{1+x^\beta} \ dx$$

L'estremo $+\infty$ è improprio per ogni $\alpha,$ mentre $0$ è un estremo singolare quando $\alpha<0.$ Spezzando in $1$ si ottengono due integrali indipendenti:

$$I_{\alpha,\beta}=\int_0^1\frac{x^\alpha}{1+x^\beta} \ dx+\int_1^{+\infty}\frac{x^\alpha}{1+x^\beta} \ dx$$

Vicino all'origine il confronto con $x^\alpha$ segue da:

$$\lim_{x\to0^+}\frac{\dfrac{x^\alpha}{1+x^\beta}}{x^\alpha}=\lim_{x\to0^+}\frac{1}{1+x^\beta}=1$$

Il primo integrale converge se e solo se $\alpha>-1.$ All'infinito la funzione di confronto è $x^{\alpha-\beta}$ perché:

$$\lim_{x\to+\infty}\frac{\dfrac{x^\alpha}{1+x^\beta}}{x^{\alpha-\beta}}=\lim_{x\to+\infty}\frac{x^\beta}{1+x^\beta}=1$$

Il secondo integrale converge se e solo se $\alpha-\beta<-1,$ ossia $\alpha<\beta-1.$ Entrambi i pezzi convergono dunque se e solo se:

$$-1<\alpha<\beta-1$$

Per ogni altro valore di $\alpha$ l'integrale diverge.

## Convergenza assoluta

Consideriamo un integrale improprio della forma:

$$\int_a^{+\infty} f(x) \ dx$$

L'integrale converge assolutamente quando converge l'integrale del valore assoluto:

$$\int_a^{+\infty} |f(x)| \ dx < +\infty$$

La convergenza assoluta implica la convergenza, ma il viceversa non vale. Per esempio:

$$\int_1^{+\infty} \frac{\sin x}{x} \ dx$$

L'[integrazione per parti](../integration-by-parts/) mostra che questo integrale converge. L'integrale del suo valore assoluto è:

$$\int_1^{+\infty} \frac{|\sin x|}{x} \ dx$$

Il secondo integrale diverge. Un integrale che converge senza convergere assolutamente si dice semplicemente convergente.

> Supponiamo che $f$ sia integrabile secondo Riemann su ogni sottointervallo limitato di $[a,+\infty).$ La funzione $f$ è integrabile secondo Lebesgue su $[a,+\infty)$ se e solo se il suo integrale improprio converge assolutamente, e in tal caso i due valori coincidono. Quindi $\int_1^{+\infty}\sin x/x \ dx$ converge come integrale improprio, ma $x\mapsto\sin x/x$ non è integrabile secondo Lebesgue su $[1,+\infty)$ perché l'integrale di $|\sin x|/x$ diverge.

> Se non è disponibile un valore analitico, l'[integrazione numerica](../numerical-integration/) su un intervallo troncato richiede una stima separata della coda omessa.
