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
## Integrali su intervalli illimitati

Finora abbiamo analizzato gli [integrali indefiniti](../indefinite-integrals/) e quelli [definiti](../definite-integrals), descrivendo sia le primitive delle funzioni analitiche più comuni sia le principali regole di derivazione. Ricordiamo, in termini semplicistici, che gli integrali indefiniti non presentano estremi di integrazione, mentre quelli definiti sono sempre valutati all'interno di un [intervallo](../intervals/) limitato, ad esempio $[a,b]$. In quest'ultimo caso ci siamo imbattuti in integrali come questo:

$$\int_{a}^{b} f(x) \ dx = F(b) - F(a) \tag{1}$$

Al di là di quanto sia complesso il calcolo della primitiva della funzione integranda $f(x)$, ogni integrale definito si può ricondurre alla $(1)$. Come oramai sapete, essendo arrivati a questo punto della nostra trattazione, una volta giunti a tale formulazione, si valuta la primitiva $F$ ai due estremi del segno di integrale e si determina il valore dell'area con segno iscritta tra la curva e l'asse delle $x.$ Tenere conto del segno è fondamentale, in quanto le aree sopra l'asse delle $x$ (quelle quindi con segno positivo) si sommano, mentre quelle sotto l'asse delle $x$ (con segno negativo)  si sottraggono. Ciò deriva dalla definizione stessa di integrale come quantità accumulata sotto una data curva.

Questo modo di procedere però ha una limitazione non banale: funziona solo quando i due estremi circoscrivono un intervallo limitato. Più esattamente, richiamando i [criteri di integrazione di Riemann](../riemann-integrability-criteria), è necessario che l'intervallo in cui è definito l'integrale sia limitato, e $f$ sia limitata. 

Che cosa accade quando una di queste ipotesi non è verificata e uno degli estremi di integrazione è $+\infty$ o $-\infty?$ Ci troveremmo in un caso del genere:

$$\int_{a}^{+\infty} f(x) \ dx$$

![IMG. 1](svg/improper-integrals-3.svg) 

Come si può facilmente dedurre, in questa circostanza non è possibile valutare la primitiva direttamente nell'estremo $F(+\infty)$ non essendo $+\infty$ un numero reale.

Questa classe di integrali sono molto comuni e il loro comportamento si valuta ricorrendo all'algebra dei [limiti](../limits/). Prendono il nome di integrali impropri, a differenza di quelli propri di Riemann che abbiamo incontrato finora: o meglio il loro limite definisce quello che viene chiamato integrale improprio, come vedremo in termini più formali nei seguenti paragrafi.

## Integrali impropri su intervalli illimitati

Supponiamo che $f$ sia integrabile secondo Riemann su ogni intervallo $[a,t]$ con $t>a.$ L'integrale improprio su $[a,+\infty)$ è definito dal [limite](../limits/):

$$\int_a^{+\infty} f(x) \ dx := \lim_{t \to +\infty} \int_a^t f(x) \ dx$$

Quindi si impone l'estremo superiore pari a un numero finito $t,$ e si determina il limite per $t\to+\infty.$

![Img. 1](svg/improper-integrals-1.svg)

+ Quando il limite esiste ed è finito ed è pari ad un numero reale $\ell$, l'integrale converge.
+ Quando il limite è pari a $\pm\infty$, l'integrale diverge.
+ Quando il limite non esiste, l'integrale improprio si dice irregolare.

- - -

Lo stesso processo può essere replicato quando l'estremo inferiore è $-\infty.$ Supponiamo in questo caso che $f$ sia integrabile secondo Riemann su ogni intervallo $[t,b]$ con $t<b.$ La definizione corrispondente dell'integrale improprio è:

$$\int_{-\infty}^b f(x) \ dx := \lim_{t \to -\infty} \int_t^b f(x) \ dx$$

Un altro caso è quello in cui entrambe gli estremi sono $\pm\infty$ e quindi un solo limite non basta. In questa situazione si sceglie un punto qualsiasi $c$ e si pone:

$$\int_{-\infty}^{+\infty} f(x) \ dx := \int_{-\infty}^c f(x) \ dx + \int_c^{+\infty} f(x) \ dx$$

L'integrale improprio converge solo quando entrambi gli integrali a destra convergono separatamente e in tal caso il risultato non dipende dalla scelta di $c.$

## Esempio 1

Per illustrare un caso di studio molto frequente, calcoliamo il seguente integrale improprio:

$$\int_1^{+\infty} \frac{1}{x^2} \ dx$$

Per $b>1,$ l'integrale proprio di Riemann è:

$$\int_1^b \frac{1}{x^2} \ dx = \int_1^b x^{-2} \ dx = \left[ -x^{-1} \right]_1^b = -\frac{1}{b} + 1$$

Poiché $1/b\to0$ per $b\to+\infty,$ il limite che definisce l'integrale è:

$$\lim_{b \to +\infty} \left(1 - \frac{1}{b}\right) = 1$$

Tale limite è finito e quindi l'integrale improprio converge a $1.$

## Esempio 2

Consideriamo adesso il caso analogo con esponente pari a $1$ al denominatore:

$$\int_1^{+\infty} \frac{1}{x} \ dx$$

Per $b>1,$ l'integrale diventa:

$$\int_1^b \frac{1}{x} \ dx = \left[ \ln x \right]_1^b = \ln b$$

Il limite che lo definisce è:

$$\lim_{b \to +\infty} \ln b = +\infty$$

Tale limite è infinito, quindi l'integrale diverge.

## Integrali impropri con discontinuità infinite

Un secondo tipo di integrale improprio si presenta quando $f$ è illimitata in qualche punto dell'intervallo. Supponiamo che $f$ diventi illimitata per $x \to a^+$ ma sia integrabile secondo Riemann su ogni intervallo $[t,b]$ con $a<t<b.$ L'integrale improprio è definito da:

$$\int_a^b f(x) \ dx := \lim_{t \to a^+} \int_t^b f(x) \ dx$$

L'integrale improprio converge quando il limite esiste ed è finito. Allo stesso modo, supponiamo che $f$ diventi illimitata per $x \to b^-$ ma sia integrabile secondo Riemann su ogni intervallo $[a,t]$ con $a<t<b.$ La definizione corrispondente è:

$$\int_a^b f(x) \ dx := \lim_{t \to b^-} \int_a^t f(x) \ dx$$

Supponiamo che $c\in(a,b)$ sia l'unico punto singolare e che $f$ sia integrabile secondo Riemann su ogni intervallo $[a,t]$ con $a<t<c$ e su ogni intervallo $[s,b]$ con $c<s<b.$ La definizione impiega due limiti unilaterali indipendenti:

$$
\int_a^b f(x) \ dx
:=\lim_{t\to c^-}\int_a^t f(x) \ dx
+\lim_{s\to c^+}\int_s^b f(x) \ dx
$$

L'integrale improprio converge solo quando entrambi i limiti unilaterali esistono e sono finiti.

Se un integrale presenta più estremi impropri o più punti singolari, si scelgono punti di taglio regolari in modo che ogni pezzo unilaterale abbia una sola fonte di improprietà. In questi casi, l'integrale di partenza converge se e solo se converge ogni pezzo dell'integrale.

## Esempio 3

La funzione integranda del seguente integrale è illimitata nell'estremo inferiore:

$$\int_0^1 \frac{1}{\sqrt{x}} \ dx$$

Poiché $1/\sqrt{x}$ è illimitata per $x\to0^+,$ la definizione usa un estremo inferiore $t>0$ e il limite per $t\to0^+$:

$$\int_0^1 \frac{1}{\sqrt{x}} \ dx := \lim_{t \to 0^+} \int_t^1 x^{-1/2} \ dx$$

La primitiva è:

$$\int x^{-1/2} \ dx = 2x^{1/2} + C$$

Per $t>0,$ l'integrale proprio di Riemann è:

$$\int_t^1 x^{-1/2} \ dx = 2 - 2\sqrt{t}$$

Il limite che definisce l'integrale è:

$$\lim_{t \to 0^+} (2 - 2\sqrt{t}) = 2$$

Il limite esiste ed è finito, quindi l'integrale converge e vale $2.$

## Il criterio dell'integrale $p$

Il criterio dell'integrale $p$ classifica la famiglia di integrali del tipo:

$$\int_1^{+\infty} \frac{1}{x^p} \ dx \tag{2}$$

Il parametro $p$ è un numero reale e la convergenza dipende in questo caso dal suo valore. Quando $p\neq1,$ l'integrale proprio di Riemann è:

$$\int_1^b x^{-p} \ dx = \left[ \frac{x^{1-p}}{1-p} \right]_1^b = \frac{b^{1-p} - 1}{1 - p}$$

Il passaggio al limite per $b \to +\infty$ produce tre casi:

[class="table-1"]

|         |                       |                              |
| ------- | --------------------- | ---------------------------- |
| $p > 1$ | $b^{1-p} \to 0$       | converge a $\dfrac{1}{p - 1}$ |
| $p = 1$ | $\ln b \to +\infty$   | diverge                      |
| $p < 1$ | $b^{1-p} \to +\infty$ | diverge                      |

[/class]

L'integrale $(2)$ converge se e solo se $p>1.$ L'integrale corrispondente vicino all'origine è:

$$\int_0^1 \frac{1}{x^p} \ dx \tag{3}$$

Nell'origine il comportamento all'estremo si inverte. La funzione integranda è singolare in $x=0$ solo quando $p>0,$ mentre l'integrale $(3)$ converge se e solo se $p<1.$

> Queste [funzioni potenza](../powers/) sono i casi di riferimento per i criteri del confronto esposti di seguito.

## Convergenza e criteri del confronto

Non sempre è utile o conveniente ricorrere al calcolo degli integrali impropri attraverso il limite. In taluni casi si preferisce ricorrere ad altri meccanismi che consentono un risparmio computazionale significativo. Esistono infatti dei criteri di confronto, diretto e asintotico, che stabiliscono la convergenza senza calcolare la una primitiva e senza valutare il valore esatto dell'integrale.

Il criterio del confronto diretto usa una maggiorazione puntuale. Supponiamo che $f$ e $g$ siano integrabili secondo Riemann su ogni sottointervallo limitato di $[a,+\infty)$ e che $0\leq f(x)\leq g(x)$ per ogni $x\geq a$:

+ Se $\int_a^{+\infty} g(x) \ dx$ converge, converge anche $\int_a^{+\infty} f(x) \ dx.$
+ Se $\int_a^{+\infty} f(x) \ dx$ diverge, diverge anche $\int_a^{+\infty} g(x) \ dx.$


![Img. 2](svg/improper-integrals-2.svg)

Il criterio del confronto asintotico sostituisce la maggiorazione puntuale con un rapporto asintotico. Supponiamo che $f$ e $g$ siano positive e integrabili secondo Riemann su ogni sottointervallo limitato di $[a,+\infty),$ e che il loro rapporto abbia limite:

$$\lim_{x \to +\infty} \frac{f(x)}{g(x)} = L \qquad 0 < L < +\infty$$

Allora $\int_a^{+\infty} f(x) \ dx$ e $\int_a^{+\infty} g(x) \ dx$ convergono entrambi oppure divergono entrambi. 

In modo equivalente $f(x)\sim Lg(x)$ per $x\to+\infty;$ l'equivalenza asintotica di $f$ e $g$ è il caso particolare $L=1.$ Scegliendo $g(x)=1/x^p$ la questione si riconduce al criterio dell'integrale $p.$

I valori degeneri di $L$ danno implicazioni in un solo verso:

+ Se $L=0$ e $\int_a^{+\infty} g(x) \ dx$ converge, allora $\int_a^{+\infty} f(x) \ dx$ converge.
+ Se $L=+\infty$ e $\int_a^{+\infty} g(x) \ dx$ diverge, allora $\int_a^{+\infty} f(x) \ dx$ diverge.

Se $f$ e $g$ sono positive e integrabili secondo Riemann su ogni intervallo compatto contenuto in un lato di un punto finito $c,$ le stesse conclusioni valgono per i corrispondenti integrali impropri unilaterali quando $x\to c^+$ oppure $x\to c^-.$ Il modello potenza di riferimento è $1/|x-c|^p,$ il cui integrale su ciascun lato di $c$ converge se e solo se $p<1.$

## Procedura di decisione

Non è sempre immediato stabilire la convergenza di tali integrali. Tuttavia si può identificare una sorta di procedura decisionale che può aiutare nella sua determinazione.

+ Per prima cosa occorre individuare ogni sorgente di improprietà, cioè un intervallo illimitato, una funzione integranda illimitata in un estremo e ogni singolarità in un punto interno.
+ Se è disponibile una primitiva, bisogna applicare la definizione a ciascun pezzo dell'integrale improprio. La [regola di de l'Hôpital](../hopital-rule/) può aiutare con un quoziente indeterminato quando le sue ipotesi sono soddisfatte.
+ Per una funzione integranda non negativa, si può usare il criterio del confronto diretto quando si dispone di una maggiorazione puntuale mediante una funzione di riferimento.
+ Se la maggiorazione puntuale non è disponibile e la funzione integranda è definitivamente positiva, si può ricorrere al criterio del confronto asintotico quando il suo rapporto con una funzione di riferimento ha uno dei limiti descritti sopra. I modelli usuali sono $1/x^p$ all'infinito e $1/|x-c|^p$ vicino a un punto singolare finito.
+ Infine, spezzare un integrale con più sorgenti di improprietà in pezzi unilaterali e richiedere che ogni pezzo converga.

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
