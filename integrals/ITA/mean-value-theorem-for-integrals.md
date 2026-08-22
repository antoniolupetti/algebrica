---
title: Mean Value Theorem for Integrals
source: https://algebrica.org/mean-value-theorem-for-integrals/
license: CC BY-NC 4.0
tags:
  - average-value
  - continuous-functions
  - darboux-theorem
  - definite-integral
  - fundamental-theorem-of-calculus
  - integration
  - intermediate-value-theorem
  - mean-value-theorem
  - weierstrass-theorem
---
## Enunciato

Il teorema del valore medio degli integrali è un teorema abbastanza semplice e intuitivo da comprendere senza neanche addentrarsi nell'enunciato e nella sua dimostrazione formali. Prendete una curva qualsiasi continua su un intervallo in cui ha un andamento definito. Il valor medio integrale è compreso tra il minimo e il massimo della funzione e, per continuità, è assunto dalla funzione in almeno un punto. Considerando questo valore come una soglia, le aree al di sopra si compensano con quelle al di sotto. Quando la funzione è non negativa, il suo integrale sull'intervallo è quindi l'area di un rettangolo con base pari all'intervallo scelto e altezza pari al valore medio. Sappiate fin da subito che l'impiego principale di questo teorema è nella dimostrazione del [primo teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/), dove converte il rapporto incrementale della funzione integrale in un valore della funzione integranda.

Vediamone adesso la descrizione formale. Consideriamo $f$ una [funzione continua](../continuous-functions/) su un [intervallo](../intervals/) chiuso e limitato $[a, b]$ con $a < b.$ Allora esiste un punto $c \in [a, b]$ tale che vale:

$$\int_a^b f(x) \ dx = f(c)(b - a) \tag{1}$$

In pratica l'[integrale definito](../definite-integrals/) di $f$ sull'intervallo coincide con l'integrale della funzione costante $f(c)$ sullo stesso intervallo limitato nella formula dalla differenza $(b-a)$. Quando $f$ è non negativa, l'identità $(1)$ mostra che la [regione compresa tra il grafico e l'asse orizzontale](../finding-areas-by-integration/) ha la stessa area di un rettangolo di base $b - a$ e altezza $f(c).$ L'identità si può scrivere anche come:

$$\int_a^b (f(x) - f(c)) \ dx = 0 \tag{2}$$

Questa seconda identità mostra come esiste una relazione tra le aree tratteggiate nella seguente figura, ovvero, sull'intervallo $[a, b],$ l'area di $f$ al di sopra di $f(c)$ è uguale all'area in difetto di $f(c).$ In figura, $M = f(x_M)$ è il valore massimo di $f$ sull'intervallo, e $m = f(x_m)$ è il suo valore minimo che, come vedremo nel paragrafo successivo, sono utili alla dimostrazione del teorema.

![Un grafico continuo con aree complessive uguali sopra e sotto la retta orizzontale posta al suo valor medio](svg/mean-value-theorem-for-integrals-1.svg)

> Da tenere a mente che l'unica ipotesi del teorema su $f$ è la continuità. La [derivabilità](../derivatives/) non è richiesta, e la conclusione resta valida quando $f$ non è derivabile in alcun punto di $(a, b).$

## Dimostrazione

La dimostrazione del teorema è anch'essa piuttosto semplice. Sappiamo che una funzione continua su un intervallo chiuso e limitato è integrabile secondo Riemann e che, per il [teorema di Weierstrass](../weierstrass-theorem/), $f$ assume su $[a, b]$ anche un [minimo e un massimo](../maximum-minimum-and-inflection-points/), rispettivamente nei punti $x_m$ e $x_M:$

$$m = f(x_m) \qquad M = f(x_M)$$

Ogni valore di $f$ è compreso tra questi due numeri, quindi $m \leq f(x) \leq M$ per ogni $x \in [a, b].$ La proprietà di confronto degli integrali definiti, applicata alle funzioni costanti $m$ e $M,$ dà:

$$m(b - a) \leq \int_a^b f(x) \ dx \leq M(b - a)$$

Dividendo per $b - a$ si ottiene:

$$m \leq \frac{1}{b - a} \int_a^b f(x) \ dx \leq M \tag{3} $$

Indichiamo con $\mu$ il termine centrale e otteniamo:

$$f(x_m) \le \mu \le f(x_M)$$

Per il [teorema dei valori intermedi](../intermediate-value-theorem/) del calcolo differenziale, esiste un punto $c$ nell'intervallo chiuso di estremi $x_m$ e $x_M$ tale che $f(c) = \mu.$ Poiché $x_m$ e $x_M$ appartengono entrambi a $[a, b],$ lo stesso vale per $c.$ Moltiplicando quindi $f(c) = \mu$ per $b - a$ si ottiene l'identità $(1)$.

> Oltre all'integrabilità secondo Riemann, la dimostrazione usa due conseguenze della continuità. Gli estremi $m$ e $M$ sono valori della funzione, e la funzione assume ogni valore compreso tra essi.

- - -

Il punto $c$ si può scegliere interno anche all'intervallo aperto $(a, b).$ Supponiamo che $m < \mu < M.$ Allora $f(x_m) \neq \mu$ e $f(x_M) \neq \mu,$ quindi il punto $c$ fornito dal teorema dei valori intermedi è strettamente compreso tra $x_m$ e $x_M.$ Entrambi questi punti appartengono a $[a, b],$ dunque $c \in (a, b).$

Supponiamo invece che $\mu = M.$ La funzione $M - f$ è continua e non negativa su $[a, b],$ e il suo integrale è nullo in quanto vale:

$$\int_a^b (M - f(x)) \ dx = M(b - a) - \mu(b - a) = 0 \tag{4}$$

Se $M - f$ fosse positiva in qualche valore di $x_0,$ la continuità fornirebbe un sottointervallo $J \subseteq [a, b]$ di lunghezza positiva $\ell$ sul quale varrebbe:

$$M - f(x) \geq \frac{1}{2}(M - f(x_0))$$

Ne seguirebbe che:

$$\int_a^b (M - f(x)) \ dx \geq \int_J (M - f(x)) \ dx \geq \frac{M - f(x_0)}{2} \ell > 0$$

Questo contraddice il fatto che l'integrale nella $(4)$ sia nullo. Dunque $f$ è costante e uguale a $M,$ e ogni punto interno soddisfa $f(c) = \mu$ (il caso $\mu = m$ è simmetrico).

## Il valor medio di una funzione

Per una funzione $f$ [integrabile secondo Riemann](../riemann-integrability-criteria/) su $[a, b],$ la quantità che compare nella dimostrazione, più precisamente nella $(3),$ è il valor medio di $f$ sull'intervallo, detto anche media integrale:

$$\mu = \frac{1}{b - a} \int_a^b f(x) \ dx$$

La definizione estende il concetto di [media aritmetica](../arithmetic-mean/) in termini statistici alle funzioni di variabile continua attraverso un limite di somme di Riemann. Supponiamo di dividere l'intervallo $[a, b]$ in $n$ parti di uguale lunghezza $\Delta x = (b - a)/n,$ e campioniamo $f$ nell'estremo destro $x_k = a + k \Delta x$ di ciascuna parte. Poiché $\Delta x/(b - a) = 1/n,$ la media aritmetica degli $n$ valori campionati si riscrive come:

$$\frac{1}{n} \sum_{k=1}^{n} f(x_k) = \frac{1}{b - a} \sum_{k=1}^{n} f(x_k) \Delta x$$

L'espressione a destra è una somma di Riemann di $f$ su $[a, b],$ divisa per la lunghezza dell'intervallo che, per $n \to \infty,$ converge a $\mu.$ Il valor medio è quindi il limite delle medie aritmetiche di campioni che diventano via via sempre più stretti.

Per citare un caso concreto, se $v(t)$ è la [velocità](../velocity/) di un punto che si muove lungo una retta e $t_1 < t_2$ son due istanti separati, l'integrale di $v$ su $[t_1, t_2]$ è lo spostamento in quell'intervallo di tempo. La velocità media sull'intervallo vale:

$$\mu = \frac{1}{t_2 - t_1} \int_{t_1}^{t_2} v(t) \ dt$$

Questo valore è la velocità costante che produrrebbe lo stesso spostamento nello stesso tempo. Quando la velocità è continua, esiste un istante $c \in [t_1, t_2]$ in cui $v(c) = \mu.$

## Una puntualizzazione terminologica

Per evitare ambiguità terminologiche che possono generare confusioni concettuali, ricordiamo che il teorema della media per gli integrali è ben diverso dall'altro teorema della media, conosciuto anche come [teorema di Lagrange](../lagrange-theorem/). Se $f$ è continua su $[a, b]$ e derivabile su $(a, b),$ quest'ultimo fornisce un punto $c \in (a, b)$ in cui la derivata è uguale al [rapporto incrementale](../difference-quotient/) tra gli estremi dell'intervallo:

$$f'(c) = \frac{f(b) - f(a)}{b - a} \tag{5}$$

Come abbiamo invece visto poco sopra, il teorema della media integrale afferma che una funzione integranda è uguale al proprio valor medio in qualche punto di un intervallo preso in considerazione:

$$f(c) = \frac{1}{b - a} \int_a^b f(x) \ dx$$

Sebbene i due teoremi abbiano ipotesi e conclusioni differenti, esiste un legame tra i due determinato dal [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/). In particolare, il secondo teorema del calcolo integrale afferma che, sia $f$ continua su $[a, b]$ e sia $F$ una qualunque [primitiva](../indefinite-integrals/) di $f.$ Il valore dell'integrale definito agli estremi sarà pari a:

$$\int_a^b f(x) \ dx = F(b) - F(a)$$

L'identità $(5)$ allora diventa:

$$F(b) - F(a) = F'(c)(b - a)$$

Questo è il teorema di Lagrange applicato a $F.$ Viceversa, il teorema di Lagrange applicato a una primitiva di una funzione continua $f$ dà il teorema integrale. È importante ricordare che per una funzione $F$ con derivata continua, i due teoremi sono equivalenti.

## Cosa accade senza la continuità

L'ipotesi di continuità è, nello studio delle funzioni, una delle ipotesi cardine per gran parte dei teoremi e delle conclusioni che da essi ne derivano. Per una funzione limitata e [integrabile secondo Riemann](../riemann-integrability-criteria/) valgono le stesse disuguaglianze, considerando però l'[estremo](../supremum-and-infimum/) inferiore e superiore al posto dei punti di [minimo e massimo](../maximum-minimum-and-inflection-point). La relazione $(3)$ pertanto si riscrive come:

$$\inf_{[a, b]} f \leq \frac{1}{b - a} \int_a^b f(x) \ dx \leq \sup_{[a, b]} f$$

Anche in questo caso, il valor medio resta ancora definito ed è compreso tra questi estremi ma, a differenza di quanto visto fino ad ora, la funzione non è detto che lo assuma. Consideriamo infatti la seguente funzione a gradino sull'intervallo $[0, 2]:$

$$
f(x) = \begin{cases} 0 & \text{se } 0 \leq x < 1 \\[6pt] 1 & \text{se } 1 \leq x \leq 2 \end{cases}
$$

La $f$ è limitata e ha una sola [discontinuità](../discontinuities-of-real-functions/), quindi è integrabile secondo Riemann, e il suo integrale su $[0, 2]$ vale $1$ (basta un semplicissimo calcolo per verificarlo). Il valor medio è pertanto $1/2,$ ma, come potete intuire, la funzione non assume mai questo valore perché la sua immagine è $\{\ 0, 1 \ \}.$ Quindi, la limitatezza e l'integrabilità secondo Riemann non bastano per la conclusione.


> Questa dimostrazione si applica a ogni funzione integrabile secondo Riemann che assume i propri estremi e gode della proprietà dei valori intermedi. Il [teorema di Darboux](../darboux-theorem/) mostra che quest'ultima proprietà può valere senza la continuità in quanto ogni derivata gode della proprietà dei valori intermedi, anche quando la derivata è discontinua.

## La forma pesata

Il teorema del valore medio per gli integrali ha anche una forma in cui i valori di $f$ sono mediati rispetto a un peso. Consideriamo una $f$ continua su $[a, b]$ e sia $g$ integrabile secondo Riemann e non negativa sullo stesso intervallo. Dietro queste condizioni esiste $c \in [a, b]$ tale che:

$$\int_a^b f(x) g(x) \ dx = f(c) \int_a^b g(x) \ dx \tag{6}$$

Se $g(x) = 1$ otteniamo l'identità $(1),$ e la dimostrazione segue gli stessi due passaggi. Moltiplicando le disuguaglianze $m \leq f(x) \leq M$ per $g(x)$ otteniamo:

$$m g(x) \leq f(x) g(x) \leq M g(x)$$

Il prodotto $fg$ è integrabile secondo Riemann, e integrando i tre termini si ottiene:

$$m \int_a^b g(x) \ dx \leq \int_a^b f(x) g(x) \ dx \leq M \int_a^b g(x) \ dx \tag{7}$$

Poniamo $G = \int_a^b g(x) \ dx$ e consideriamo i seguenti casi:

+ se $G = 0,$ dalla $(7)$ ricaviamo che l'integrale del prodotto $fg$ è nullo e quindi l'identità $(6)$ vale per ogni scelta di $c;$ 
+ se $G > 0,$ dividendo per $G$ il quoziente risulta compreso tra $m$ e $M,$ e il teorema dei valori intermedi fornisce un punto $c$ tale che:

$$f(c) = \frac{1}{G} \int_a^b f(x) g(x) \ dx$$

Il teorema è stato dimostrato per un peso non negativo, ma la stessa conclusione vale quando $g$ è non positiva su tutto l'intervallo. In questo caso la funzione $-g$ è non negativa, quindi soddisfa le ipotesi già dimostrate.

- - -

L'identità $(6)$ è l'enunciato del primo teorema della media integrale. In una sua seconda forma, la [monotonia](../increasing-and-decreasing-functions/) sostituisce l'ipotesi di segno costante su $g,$ e a $f$ si richiede soltanto l'integrabilità secondo Riemann. Sotto queste ipotesi esiste $\xi \in [a, b]$ tale che:

$$\int_a^b f(x) g(x) \ dx = g(a) \int_a^{\xi} f(x) \ dx + g(b) \int_{\xi}^b f(x) \ dx$$

Questa forma si usa nelle dimostrazioni dei [criteri di Dirichlet e di Abel](../convergence-tests-for-improper-integrals/) per la convergenza degli [integrali impropri](../improper-integrals/) utilizzati per la valutazione degli integrali di funzioni oscillanti.

## Alcuni esempi

Facciamo un esempio pratico, andando a calcolare il valor medio del seguente integrale e un punto in cui tale valore viene assunto. Abbiamo:

$$\int_0^9 \sqrt{x} \ dx = \left[ \frac{2}{3} x^{3/2} \right]_0^9 = \frac{2}{3} \cdot 27 = 18$$

L'intervallo ha lunghezza $9,$ quindi il valor medio è:

$$\mu = \frac{1}{9} \int_0^9 \sqrt{x} \ dx = \frac{18}{9} = 2$$

Per localizzare il punto risolviamo $f(c) = \mu,$ cioè $\sqrt{c} = 2$ ottenendo $c = 4$ che è un valore interno all'intervallo $(0, 9).$

Il punto $c = 4$ si trova a sinistra di $4.5,$ il punto medio dell'intervallo. Poiché $\sqrt{x} > 2$ per $x \in (4, 9],$ la funzione è sopra il proprio valor medio su un intervallo di lunghezza $5,$ che è più della metà della lunghezza di $[0, 9].$

- - -

Come abbiamo visto nella parte teorica, il teorema garantisce l'esistenza del punto $c$ ma non la sua unicità. Prendiamo ad esempio il seguente integrale:

$$\int_0^{\pi} \sin x \ dx = \left[ -\cos x \right]_0^{\pi} = -\cos \pi + \cos 0 = 1 + 1 = 2$$

L'intervallo ha lunghezza $\pi,$ quindi il valor medio è:

$$\mu = \frac{2}{\pi} \approx 0.6366$$

I punti ammissibili sono le soluzioni di $\sin c = 2/\pi$ su $[0, \pi].$ Su questo intervallo il seno, essendo periodico, assume ogni valore di $(0, 1)$ esattamente due volte, in due punti simmetrici rispetto a $\pi/2,$ quindi le sue due soluzioni si scrivono con il ricorso all'[arcoseno](../arcsine-function/):

$$c_1 = \arcsin \frac{2}{\pi} \approx 0.690$$

$$c_2 = \pi - \arcsin \frac{2}{\pi} \approx 2.451$$


Quindi, è importante ricordare che l'insieme dei punti ammissibili $c$ può essere un solo punto, un insieme finito, oppure un intero intervallo quando $f$ è costante.

- - -

Facciamo, infine, un ultimo esempio in cui la forma pesata cambia sia la media sia il punto in cui essa è assunta. Prendiamo la funzione $f(x) = x^2$ con il peso $g(x) = x$ su $[0, 2].$ La funzione $f$ è continua e $g$ è non negativa sull'intervallo, quindi le ipotesi del teorema sono soddisfatte. I due integrali sono:

$$\int_0^2 x^2 \cdot x \ dx = \left[ \frac{x^4}{4} \right]_0^2 = 4$$ 

$$\int_0^2 x \ dx = \left[ \frac{x^2}{2} \right]_0^2 = 2$$

La media pesata di $f$ è il quoziente del primo per il secondo, cioè $4/2 = 2.$ Imponendo $f(c) = 2$ si arriva a $c^2 = 2,$ le cui soluzioni sono $\pm \sqrt{2}.$ Solo quella positiva appartiene all'intervallo, quindi:

$$c = \sqrt{2} \approx 1.414$$

Per confronto, la media non pesata della stessa funzione sullo stesso intervallo è:

$$\frac{1}{2} \int_0^2 x^2 \ dx = \frac{1}{2} \cdot \frac{8}{3} = \frac{4}{3}$$

Questo valore è assunto dove $c^2 = 4/3,$ cioè in $c = 2/\sqrt{3} \approx 1.155.$ Il peso $x$ conta la parte destra dell'intervallo più di quella sinistra, e lì $f$ è più grande, quindi la media pesata supera quella non pesata e il punto in cui è raggiunta si sposta verso destra.
