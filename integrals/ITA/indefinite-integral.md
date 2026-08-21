---
title: Indefinite Integrals
source: https://algebrica.org/indefinite-integrals/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - definite-integral
  - fundamental-theorem-of-calculus
  - indefinite-integral
  - integration
  - integration-rules
  - linearity
  - power-rule
  - primitive
---
## Un'introduzione amichevole agli integrali

Gli integrali godono notoriamente di una pessima reputazione tra gli studenti della scuola secondaria e dei primi anni dell'università. Sono considerati, almeno quando si approccia al loro studio, oggetti matematici caratterizzati da una complessità intrinseca che li rende, a dir poco, ostili. 
Ed è vero, quantomeno in parte.
Prendete ad esempio il seguente [integrale definito](../definite-integrals/) nell'intervallo $[+\infty, -\infty],$ noto come integrale di Gauss:

$$
\int_{-\infty}^{+\infty} e^{-x^2}\,dx = \sqrt{\pi}
$$

A prima vista può sembrare un oggetto innocuo, ma se si prova a risolverlo con i metodi elementari di integrazione non se ne viene a capo. La storia comunemente accettata vuole che Gauss l'abbia risolto a intorno ai trent'anni, quindi, almeno fino a quell'età, sentitevi pure dispensati dall'essere in grado di determinarne il valore.
Un altro integrale verso cui provare un reverenziale timore è quello di Dirichlet, semplice nella forma ma difficilissimo nella sostanza:

$$
\int_{0}^{\infty} \frac{\sin x}{x}\,dx = \frac{\pi}{2}
$$

Per nostra fortuna, la maggior parte di noi non corre per una _Field Medal_, nutre ambizioni più contenute e per questa ragione, gli integrali con cui avrà a che fare nel corso dei propri studi sono quindi, in prevalenza, alla portata di un qualunque studente volenteroso (fatto salvo il caso in cui abbia la sfortuna di imbattersi lungo il proprio percorso accademico in qualche professore particolarmente sadico).

La buona notizia è che una larga parte di questi oggetti matematici sono risolvibili con processi meccanici e un pizzico di intuizione che si può sviluppare solo ed esclusivamente facendo [tantissima pratica](../learning-mathematics/) sulle principali regole di integrazione e sulle tipiche scorciatoie che consentono di risparmiare un quantità significativa di passaggi.

- - -

Nei successivi paragrafi proporrò una definizione rigorosa degli integrali, in particolare di quelli indefiniti che sono l'oggetto di questa voce e sono fondamentali per introdurre gli omonimi [definiti](../definite-integrals). Tuttavia preferisco fare una premessa intuitiva, partendo dal concetto di derivazione, che come vedremo più avanti, parlando di _primitive_, è l'operazione inversa dell'integrazione. 

Consideriamo una semplice funzione $y=x^2$. Il suo grafico è una [parabola](../parabola/) passante per l'origine. Sappiamo, dallo studio delle regole di derivazione, che la sua derivata è unica ed è pari a $y'=2x$ e associa ad ogni valore di $x$ il coefficiente angolare della retta tangente al grafico in quel punto. Per esempio, per $x=2$ si ottiene $y'(2)=2 \cdot 2 = 4.$ Questo significa che la retta tangente alla parabola nel punto $(2,4)$ ha coefficiente angolare proprio pari a $4$.

![IMG. 1](indefinite-integrals-1.svg)

Analizziamo adesso il caso inverso, in cui abbiamo una data derivata, ad esempio proprio $y'=2x,$ e vogliamo calcolarne la primitiva $y.$ Avendo visto il percorso contrario, per analogia e all'asciutto di qualsiasi regola di integrazione, potremmo affermare che la sua primitiva sia $y=x^2.$

Peccato che non sia corretto, o perlomeno lo sia solo in parte, con un'omissione.

Mentre per una funzione $y$ esiste una sola derivata $y',$ data una derivata esistono infinite sue primitive che differiscono per una costante $c.$ Nel caso $y'=2x,$ la risposta corretta sarebbe quindi stata $y=x^2 + c.$ Il motivo di questa caratterizzazione è banale, ma è sorprendente come anche molti studenti già navigati non sanno fornire una risposta immediata a tale motivazione. Il grafico renderà il tutto più chiaro. Se immaginate di traslare sull'asse y la funzione $y=x^2$ avrete infinte funzioni omologhe lungo tutto l'asse che differiscono solo per il termine noto.

![IMG. 1](indefinite-integrals-2.svg)

La traslazione verticale, infatti, non modifica in alcun modo la pendenza della curva. Le funzioni $y=x^2$, $y=x^2+1$, $y=x^2-3$ e, più in generale, tutte le funzioni della forma $y=x^2+c$ hanno quindi esattamente la stessa derivata, $y'=2x$.

È proprio questa semplice osservazione geometrica a spiegare perché una funzione ha una sola derivata, mentre la stessa funzione può avere infinite primitive, tutte diverse tra loro per una costante.

Per concludere questa premessa, ricordate la seguente distinzione fondamentale: l'integrale indefinito determina la famiglia di primitive data una certa derivata, mentre l'integrale definito, oggetto di un'apposita voce, calcola l'area compresa tra una curva e l'asse delle ascisse all'interno di un dato intervallo. Nei paragrafi successivi sono elencate le principali primitive e le proprietà degli integrali. Per vostra sventura dovrete impararle tutte a memoria (intendo proprio tutte), condizione necessaria per avere qualche possibilità di sviluppare correttamente i calcoli degli integrali più complessi che incontreremo più avanti.

Vi lascio di seguito l'integrale sui cammini di Feynman, uno degli strumenti fondamentali della meccanica quantistica e della teoria quantistica dei campi. È naturalmente ben al di fuori della nostra portata.

$$
\langle x_f,t_f \mid x_i,t_i\rangle
=
\int_{x(t_i)=x_i}^{x(t_f)=x_f}
\mathcal{D}x(t)\,
\exp\left(\frac{i}{\hbar}S[x(t)]\right)
$$

Tenetelo però a mente, così, solo per essere avvertiti su cosa potrebbe aspettarvi.


## Primitive

Ogni funzione derivabile ha un'unica [derivata](../derivatives/). Il problema inverso consiste nello stabilire se una data funzione $f$ è la derivata di qualche funzione $F$. Ogni funzione $F$ di questo tipo è una primitiva (o antiderivata) di $f$. Sia $I$ un [intervallo](../intervals/) aperto. Una funzione derivabile $F\colon I \to \mathbb{R}$ è una primitiva di $f\colon I \to \mathbb{R}$ quando vale la seguente identità:

$$F'(x) = f(x) \qquad \forall x \in I$$

Non ogni funzione ammette una primitiva su un dato intervallo. La [continuità](../continuous-functions/) è sufficiente. Ogni funzione continua su un intervallo aperto $I$ ha una primitiva su $I$. Per esempio, $F(x) = x^3$ è una primitiva di $f(x) = 3x^2$. La sua derivata è:

$$\frac{d}{dx} x^3 = 3x^2$$

Una funzione non deve necessariamente essere continua per avere una primitiva. La funzione seguente è derivabile su $\mathbb{R}:$

$$
F(x) :=
\begin{cases}
x^2\sin(1/x) & \text{se } x \neq 0 \\[6pt]
0 & \text{se } x = 0
\end{cases}
$$

Per $x \neq 0,$ la sua derivata è $F'(x) = 2x\sin(1/x) - \cos(1/x).$ Nell'origine la derivata è:

$$F'(0) = \lim_{h \to 0}\frac{h^2\sin(1/h)}{h} = \lim_{h \to 0}h\sin(1/h) = 0$$

Quindi $f := F'$ ha $F$ come primitiva su $\mathbb{R},$ ma $f$ non è continua in $0$ perché $\cos(1/x)$ non ha limite per $x \to 0.$

Per il [teorema di Darboux](../darboux-theorem/), ogni derivata gode della proprietà dei valori intermedi. Di conseguenza una funzione con una discontinuità di salto, come la [funzione gradino di Heaviside](../heaviside-function/), non ha primitive su alcun intervallo aperto che contenga il punto di discontinuità.

- - -

A differenza delle derivate, le primitive non sono uniche. Poiché la derivata di una costante qualunque è nulla, le funzioni $x^3$, $x^3 + 5$ e $x^3 - \frac{1}{2}$ sono tutte primitive di $3x^2$. Più in generale, se $F(x)$ è una primitiva di $f(x)$ su un intervallo $I$, lo è anche $F(x) + c$ per ogni $c \in \mathbb{R}$. La derivata di $F(x) + c$ è:

$$\frac{d}{dx}[F(x) + c] = F'(x) = f(x)$$

Viceversa, due primitive qualunque della stessa funzione su un intervallo differiscono per una costante. Se $F_1(x)$ e $F_2(x)$ sono entrambe primitive di $f(x)$ su $I$, la loro differenza ha derivata nulla:

$$\frac{d}{dx}[F_1(x) - F_2(x)] = F_1'(x) - F_2'(x) = f(x) - f(x) = 0$$

Per il [teorema di Lagrange](../lagrange-theorem/), una funzione con derivata nulla su un intervallo è costante. Quindi $F_1(x) - F_2(x) = c$ per un certo $c \in \mathbb{R}$.

## L'integrale indefinito

Supponiamo che $f$ abbia una primitiva $F$ su un intervallo aperto $I$. L'integrale indefinito di $f$ su $I$ è la famiglia di tutte le sue primitive. Questa famiglia ha la forma $F(x) + c$, dove $c \in \mathbb{R}$. Scriviamo questa famiglia come:

$$\int f(x) \ dx = F(x) + c \qquad c \in \mathbb{R}$$

Ogni elemento di questa famiglia ha derivata $f$:

$$\frac{d}{dx}[F(x) + c] = f(x)$$

In modo equivalente, l'integrale di $F'$ è la famiglia di funzioni $F + c.$

$$\int F'(x) \ dx = F(x) + c \qquad c \in \mathbb{R}$$

Il [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/) mette in relazione le primitive con gli integrali definiti.

- - -

Determiniamo la primitiva di $f(x) = 3x$ il cui grafico passa per il punto $(2, 1)$. Ogni primitiva ha la forma:

$$F(x) = \int 3x \ dx = \frac{3}{2}x^2 + c$$

Poiché il grafico passa per $(2, 1)$, la costante deve soddisfare $F(2) = 1$:

$$
\begin{align}
\frac{3}{2}(2)^2 + c &= 1 \\[6pt]
6 + c &= 1 \\[6pt]
c &= -5
\end{align}
$$

L'unica primitiva che soddisfa la condizione data è:

$$F(x) = \frac{3}{2}x^2 - 5$$

Più in generale, sia $F_0$ una primitiva di $f$ su un intervallo aperto $I,$ e scegliamo $x_0 \in I$ e $y_0 \in \mathbb{R}.$ Ogni primitiva ha la forma $F_0 + c.$ La condizione $F(x_0) = y_0$ equivale a $c = y_0 - F_0(x_0),$ quindi esattamente una primitiva assume il valore prescritto:

$$F(x) = F_0(x) + y_0 - F_0(x_0)$$

I grafici delle funzioni $F_0 + c$ sono traslazioni verticali del grafico di $F_0.$ Esattamente uno di questi grafici passa per un punto prescritto $(x_0, y_0).$

## Proprietà di linearità

Supponiamo che $f$ e $g$ abbiano primitive $F$ e $G$ sullo stesso intervallo. Poiché $(F + G)' = f + g$, ogni primitiva di $f + g$ ha la forma $F + G + c$:

$$\int [f(x) + g(x)] \ dx = F(x) + G(x) + c \qquad c \in \mathbb{R} \tag{1}$$

Per ogni $k \in \mathbb{R}$, l'identità $(kF)' = kf$ mostra che ogni primitiva di $kf$ ha la forma $kF + c$:

$$\int kf(x) \ dx = kF(x) + c \qquad k, c \in \mathbb{R} \tag{2}$$

Queste formule sono le regole di linearità per gli integrali indefiniti. Riducono l'integrale di una combinazione lineare alle primitive dei suoi singoli termini.

- - -

Calcoliamo l'integrale di $f(x) = 3x^2 + 2x$. Per linearità, l'integrale è la somma di due termini, e a ciascuno si applica la regola della potenza:

$$\int (3x^2 + 2x) \ dx = \int 3x^2 \ dx + \int 2x \ dx$$

I due termini hanno costanti $c_1$ e $c_2$, la cui somma è un'altra costante arbitraria $c$. L'integrale è quindi:

$$\int (3x^2 + 2x) \ dx = x^3 + x^2 + c \qquad c \in \mathbb{R}$$

- - -

Calcoliamo l'integrale di $f(x) = 5\sin(x)$. Poiché $5$ è costante, la proprietà $(2)$ dà:

$$\int 5\sin(x) \ dx = 5 \int \sin(x) \ dx$$

Una primitiva di $\sin(x)$ è $-\cos(x)$. L'integrale è pertanto:

$$\int 5\sin(x) \ dx = -5\cos(x) + c \qquad c \in \mathbb{R}$$

## Integrale di una funzione potenza

Per ogni esponente reale $a \neq -1$, la [funzione potenza](../power-function/) $x^a$ ha il seguente integrale indefinito su $(0, +\infty)$:

$$\int x^a \ dx = \frac{x^{a+1}}{a+1} + c$$

Quando $a = -1$, il denominatore è nullo, quindi la formula non è definita. Per questo esponente la primitiva è logaritmica e segue una formula a parte. Calcoliamo il seguente integrale:

$$\int (3x^4 + 5x^2) \ dx$$

La linearità e la regola della potenza danno:

$$\int (3x^4 + 5x^2) \ dx = 3 \int x^4 \ dx + 5 \int x^2 \ dx = 3 \cdot \frac{x^5}{5} + 5 \cdot \frac{x^3}{3} + c$$

L'integrale è dunque:

$$\int (3x^4 + 5x^2) \ dx = \frac{3}{5}x^5 + \frac{5}{3}x^3 + c \qquad c \in \mathbb{R}$$

- - -

Per $x > 0$, calcoliamo il seguente integrale:

$$\int \left(4x^3 - \frac{3}{\sqrt{x}} + 2\cos x\right) \ dx$$

La linearità dà tre termini:

$$\int 4x^3 \ dx - \int 3x^{-1/2} \ dx + \int 2\cos x \ dx$$

Per la regola della potenza, $x^4$ è una primitiva di $4x^3$. Poiché $1/\sqrt{x} = x^{-1/2}$ per $x > 0$, $6\sqrt{x}$ è una primitiva di $3x^{-1/2}$. Infine, $2\sin x$ è una primitiva di $2\cos x$. La loro somma con i segni è:

$$\int \left(4x^3 - \frac{3}{\sqrt{x}} + 2\cos x\right) \ dx = x^4 - 6\sqrt{x} + 2\sin x + c$$

> Derivando termine a termine $x^4 - 6\sqrt{x} + 2\sin x + c$ si ottiene la funzione integranda di partenza.

## L'integrale logaritmico

Per $a = -1$, il denominatore nella formula della regola della potenza è nullo. Su ogni intervallo aperto contenuto in $\mathbb{R} \setminus \{0\}$, l'integrale corrispondente è il [logaritmo naturale](../logarithms/) del [valore assoluto](../absolute-value/):

$$\int \frac{1}{x} \ dx = \ln |x| + c$$

La funzione $\ln|x|$ ha derivata $1/x$ per ogni $x \neq 0$. Il valore assoluto serve perché $\ln x$ è definito solo per $x > 0$, mentre $1/x$ è definito anche per $x < 0$.

> L'identità $\int \frac{1}{x} \ dx = \ln|x| + c$ vale separatamente su $(-\infty, 0)$ e su $(0, +\infty)$. Su ciascun intervallo la costante arbitraria può assumere un valore diverso, quindi la primitiva più generale di $1/x$ su tutto il suo dominio non è un'unica espressione $\ln|x| + c$ con una sola costante, ma una famiglia definita a tratti con costanti indipendenti sulle due componenti.

## Regole fondamentali di integrazione

La tabella elenca le due identità di linearità, la regola della potenza per $a \neq -1$ e il caso logaritmico $a = -1$.

[class="table-1"]

|                       |                                                                                                   |
| --------------------- | ------------------------------------------------------------------------------------------------- |
| Linearità             | $$\int (f(x) + g(x)) \ dx = F(x) + G(x) + c \qquad F'=f,\quad G'=g,\quad c \in \mathbb{R}$$    |
| Linearità             | $$\int kf(x) \ dx = kF(x) + c \qquad F'=f,\quad k,c \in \mathbb{R}$$                         |
| Regola della potenza  | $$\int x^a \ dx = \dfrac{x^{a+1}}{a+1} + c \qquad a \in \mathbb{R}\setminus\{-1\},\quad x > 0$$ |
| Caso logaritmico      | $$\int \dfrac{1}{x} \ dx = \ln \lvert x \rvert + c$$                                          |
[/class]

## Integrali di uso comune

La tabella elenca gli integrali indefiniti elementari. La derivata di ciascun membro destro è la corrispondente funzione integranda. La voce sulla [funzione arcotangente](../arctangent-function/) ricava il caso trigonometrico inverso e le sue conseguenze per gli integrali definiti.

[class="table-1 -right"]

|                                                                       |                                                  |
| --------------------------------------------------------------------- | ------------------------------------------------ |
| $$\int \frac{1}{x} \ dx = \ln \lvert x \rvert + c$$                   | [altro](../integral-of-rational-functions/)      |
| $$\int a^x \ dx = \frac{a^x}{\ln a} + c \qquad a > 0,\quad a \neq 1$$ | [altro](../integral-of-the-exponential-function/) |
| $$\int \sin x \ dx = -\cos x + c$$                                    | [altro](../integral-of-trigonometric-functions/) |
| $$\int \cos x \ dx = \sin x + c$$                                     | [altro](../integral-of-trigonometric-functions/) |
| $$\int \frac{1}{\sin^2 x} \ dx = -\cot x + c$$                        | [altro](../integral-of-trigonometric-functions/) |
| $$\int \frac{1}{\cos^2 x} \ dx = \tan x + c$$                         | [altro](../integral-of-trigonometric-functions/) |
| $$\int \sec^2 x \ dx = \tan x + c$$                                   | [altro](../integral-of-trigonometric-functions/) |
| $$\int \sec x \tan x \ dx = \sec x + c$$                              | [altro](../integral-of-trigonometric-functions/) |
| $$\int \csc^2 x \ dx = -\cot x + c$$                                  | [altro](../integral-of-trigonometric-functions/) |
| $$\int \csc x \cot x \ dx = -\csc x + c$$                             | [altro](../integral-of-trigonometric-functions/) |
| $$\int \frac{1}{1 + x^2} \ dx = \arctan x + c$$                       |                                                  |
| $$\int \frac{1}{\sqrt{1 - x^2}} \ dx = \arcsin x + c$$                |                                                  |

[/class]

La voce sulle [strategie di integrazione](../integration-strategies/) esamina la struttura delle funzioni integrande più comuni e spiega come scegliere tra integrazione diretta, sostituzione, integrazione per parti e riduzione algebrica o trigonometrica.

> Le identità precedenti valgono su ogni intervallo in cui la funzione integranda è definita e continua. L'[integrazione per sostituzione](../integration-by-substitution/) e l'[integrazione per parti](../integration-by-parts/) si applicano ad alcuni integrali fuori da questa tabella, ma nessuno dei due metodi garantisce una primitiva elementare. Se $f$ è continua su $[a, b]$ e $F$ è continua su $[a, b]$ con $F'(x) = f(x)$ per ogni $x \in (a, b)$, il teorema fondamentale del calcolo integrale dà $\int_a^b f(x) \ dx = F(b) - F(a).$ Questo [integrale definito](../definite-integrals/) è l'area con segno compresa tra il grafico di $f$ e l'asse $x$ su $[a, b]$.
