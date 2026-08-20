---
title: Fundamental Theorem of Calculus
source: https://algebrica.org/fundamental-theorem-of-calculus/
license: CC BY-NC 4.0
tags:
  - accumulation-function
  - antiderivative
  - average-value
  - change-of-variable
  - continuous-functions
  - definite-integral
  - derivatives
  - differentiation
  - extreme-value-theorem
  - fundamental-theorem-of-calculus
  - indefinite-integral
  - integration
  - leibniz-rule
  - mean-value-theorem
---
## Ricordi indelebili

Non ho tra le mani alcuna statistica ufficiale a supporto di quanto sto per dire, ma posso azzardare che ci sono due teoremi che rimangono impressi per sempre nella mente di chi intraprende un percorso di studi nelle materie scientifiche. Il primo è quello di Pitagora: si recita a memoria fin da piccoli, come una litania, e finisce per imprimersi indelebilmente nella neocorteccia, dove si ritiene che la memoria a lungo termine sia conservata. La somma delle aree dei quadrati costruiti sui cateti è pari all'area del quadrato costruito sull'ipotenusa. Breve, semplice, non serve nemmeno la formula per capirlo. Nell'ordinamento scolastico italiano si incontra intorno ai dodici anni e viene presentato come un mero strumento per risolvere i triangoli rettangoli. Bisogna attendere il ciclo delle scuole superiori (se si è fortunati) o, più frequentemente, l'università per capirne l'effettiva potenza e le molteplici applicazioni.

Il secondo teorema, invece, tocca corde più alte, quantomeno in senso anagrafico, perché lo si scopre con la maggiore età. Mi riferisco al teorema fondamentale del calcolo integrale, uno dei teoremi fondanti dell'analisi matematica. In termini semplicistici, collega le operazioni di derivazione e di integrazione, definendole l'una l'inversa dell'altra sotto opportune ipotesi. 

A essere puntigliosi, il teorema ha due enunciati, noti come primo e secondo teorema fondamentale del calcolo integrale. Il primo afferma che ogni funzione continua su un intervallo chiuso ammette una primitiva. Il secondo postula che l'integrale definito di una funzione integranda sia pari al valore della primitiva calcolato come differenza tra i suoi estremi.

## Introduzione alle stime

Prima di presentare il teorema, è però necessario fare una digressione su un prerequisito utile alla sua dimostrazione, che si basa su una stima valida quando la funzione integranda è continua su un intervallo chiuso e limitato. Consideriamo una funzione $f$ continua su $[a, b]$ con $a < b.$ Per il [teorema di Weierstrass](../weierstrass-theorem/), $f$ ammette un minimo e un massimo nei punti $t_m, t_M \in [a, b].$ Indichiamo questi valori con:

$$m = f(t_m) \qquad M = f(t_M)$$

Ogni valore di $f$ sull'intervallo è quindi compreso tra questi due numeri, e pertanto vale $m \leq f(t) \leq M$ per ogni $t \in [a, b].$ Applicando la proprietà di confronto degli [integrali definiti](../definite-integrals/) otteniamo la seguente relazione:

$$m(b - a) \leq \int_a^b f(t) \ dt \leq M(b - a) \tag{1}$$

Quando $f$ è non negativa, poiché $f(t)$ non scende mai sotto $m$ e non supera $M$ il suo integrale deve essere necessariamente compreso tra le aree dei rettangoli di base $b-a$ e altezze $m$ e $M$. In figura, il rettangolo di altezza $m$ è contenuto nella regione compresa tra il grafico e l'asse orizzontale, e tale regione è a sua volta contenuta nel rettangolo di altezza $M.$

![Img. 1](svg/fundamental-theorem-of-calculus-1.svg)


> Le altezze dei due rettangoli sono il minimo e il massimo di $f,$ assunti nei punti $t_m,t_M \in [a,b].$ Nella figura entrambi i punti sono interni all'intervallo, ma ciascuno può coincidere con un estremo.

- - -

Facciamo ora un passo avanti e consideriamo una funzione limitata e [integrabile secondo Riemann](../riemann-integrability-criteria/). Tale funzione soddisfa la disuguaglianza $(1)$, con $m$ e $M$ sostituiti dall'[estremo inferiore e dall'estremo superiore](../supremum-and-infimum/) di $f$ sull'intervallo. Dalla continuità derivano due conseguenze.

La prima riguarda il segno dell'integrale, ovvero se $f(t) > 0$ per ogni $t \in [a, b],$ allora $m$ è un valore di $f$ ed è quindi necessariamente positivo. Pertanto si ha:

$$0 < m(b - a) \leq \int_a^b f(t) \ dt \tag{2}$$

La seconda conseguenza riguarda il valor medio di $f.$ Dividendo la $(1)$ per $b - a > 0$ otteniamo:

$$m \leq \frac{1}{b - a} \int_a^b f(t) \ dt \leq M$$

La quantità centrale corrisponde al valor medio di $f$ su $[a, b].$ Poiché tale media è compresa tra $m$ e $M,$ il [teorema dei valori intermedi](../intermediate-value-theorem/) applicato a $f$ sull'intervallo di estremi $t_m$ e $t_M$ fornisce un punto $c$ in cui $f(c)$ è proprio uguale alla media:

$$\int_a^b f(t) \ dt = f(c)(b - a)$$

Questa identità è anche nota come il teorema della media integrale. Questa identità sarà usata nella dimostrazione del primo teorema per riscrivere il rapporto incrementale della funzione integrale come un valore di $f$ e mostrare che la sua derivata coincide effettivamente con la funzione integranda.

## Il primo teorema fondamentale del calcolo integrale

Entriamo adesso nel vivo del primo teorema. Consideriamo una funzione $f$ [continua](../continuous-functions/) su un [intervallo chiuso](../intervals/) $[a, b].$ Per $x \in [a, b],$ definiamo la primitiva $F(x)$ come:

$$F(x) = \int_a^x f(t) \ dt$$

La funzione $F$ è continua su $[a, b],$ derivabile su $(a, b)$ e soddisfa:

$$F'(x) = f(x)$$

In $a$ e in $b$ la stessa identità vale rispettivamente per la derivata destra e per la derivata sinistra. Da questo punto in avanti enunciamo la dimostrazione che non è banale ma neanche impossibile. Intanto, per dimostrare la continuità poniamo $K = \max\{|m|, |M|\},$ dove $m$ e $M$ sono i valori estremi introdotti nel paragrafo precedente. In questo modo abbiamo che $|f(t)| \leq K$ su $[a, b].$ Poiché $-K \leq f(t) \leq K$ su $a,b,$ la disuguaglianza $(1)$ applicata all'intervallo di estremi $x$ e $y$ fornisce, per ogni $x,y\in[a,b]:$

$$|F(y) - F(x)| = \left|\int_x^y f(t) \ dt\right| \leq K|y - x| \tag{3}$$

Quindi $F$ è [lipschitziana](../uniform-continuity/) su $a,b$ con costante $K,$ ovvero la differenza tra i valori assunti da $F$ in due punti non supera $K$ volte la distanza tra i punti stessi. Per dimostrare l'identità sulla derivata, fissiamo ora $x \in (a, b)$ e consideriamo il [rapporto incrementale](../difference-quotient/) per $h \neq 0$ tale che $x + h \in [a, b]:$

$$\frac{F(x + h) - F(x)}{h} = \frac{1}{h} \left( \int_a^{x + h} f(t) \ dt - \int_a^x f(t) \ dt \right)$$

Gli [integrali definiti](../definite-integrals/) soddisfano la proprietà di additività su intervalli adiacenti perciò possiamo scrivere:

$$\int_a^b f(t) \ dt + \int_b^c f(t) \ dt = \int_a^c f(t) \ dt$$

Il rapporto incrementale diventa quindi:

$$\frac{F(x + h) - F(x)}{h} = \frac{1}{h} \int_x^{x + h} f(t) \ dt$$

Il teorema della media integrale mostrato sopra (ecco a cosa serviva) fornisce un punto $c_h$ compreso tra $x$ e $x + h$ tale che:

$$\int_x^{x + h} f(t) \ dt = f(c_h) h$$

Il rapporto incrementale è dunque:

$$\frac{F(x + h) - F(x)}{h} = f(c_h)$$

Poiché $c_h$ è compreso tra $x$ e $x + h,$ tende a $x$ per $h \to 0.$ Per la continuità di $f$ otteniamo:

$$\lim_{h \to 0} \frac{F(x + h) - F(x)}{h} = f(x)$$

Quindi $F'(x) = f(x).$ Come punto base si può usare un qualunque punto fissato $d \in [a, b].$ Definiamo:

$$F_d(x) = \int_d^x f(t) \ dt$$

Per la proprietà di additività, $F_d(x)=F(x)-F(d).$ Poiché $F(d)$ è costante rispetto a $x,$ le funzioni $F_d$ e $F$ hanno la stessa derivata. Per $d=a$ si ritrova la funzione integrale $F$ definita in precedenza.

Ricordiamo dalla definizione di integrale che il valore $F(x)$ è l'[area con segno](../finding-areas-by-integration/) accumulata da $a$ a $x.$ La sua derivata invece è la velocità con cui tale area varia. Quando $f(x) > 0$ l'area cresce, quando $f(x) < 0$ decresce.

![Img. 2](svg/fundamental-theorem-of-calculus-2.svg)


> Nell'immagine sopra, l'area con segno evidenziata è la nostra $F(x)$ che cresce dove $f$ è positiva e decresce dove $f$ è negativa.


## Estensione a estremi di integrazione variabili

Come abbiamo appena visto, nel teorema precedente l'estremo inferiore è costante e l'estremo superiore è dato dalla variabile $x.$ Supponiamo invece che $a$ e $b$ siano funzioni derivabili e che $f$ sia continua su un [intervallo](../intervals/) contenente le loro immagini. Tipicamente, questo argomento è trattato nei corsi di analisi matematica più avanzati, ma merita comunque una presentazione. Definiamo:

$$\Phi(x) = \int_{a(x)}^{b(x)} f(t) \ dt$$

La derivata di $\Phi$ è:

$$\Phi'(x) = f(b(x)) b'(x) - f(a(x)) a'(x) \tag{4}$$

Questa identità è la forma più semplice della regola di Leibniz per la derivazione sotto il segno di integrale. Se $a(x) = a$ è costante e $b(x) = x,$ la formula diventa $\Phi'(x) = f(x)$ perché $a'(x) = 0$ e $b'(x) = 1,$ e si ritrova il primo teorema fondamentale. Per dimostrare la formula fissiamo una costante $c$ nel dominio di $f$ e usiamo l'additività su intervalli adiacenti:

$$\int_{a(x)}^{b(x)} f(t) \ dt = \int_c^{b(x)} f(t) \ dt - \int_c^{a(x)} f(t) \ dt$$

Definiamo adesso una funzione ausiliaria $F(u)$ tale che valga la seguente espressione:

$$F(u) = \int_c^u f(t) \ dt$$

Per il primo teorema fondamentale deve valere $F'(u) = f(u).$ Dalla definizione di $F$ segue:

$$\Phi(x) = F(b(x)) - F(a(x))$$

La [regola della catena](../chain-rule/) dà:

$$
\begin{align}
\Phi'(x) &= F'(b(x))b'(x) - F'(a(x))a'(x) \\[6pt]
         &= f(b(x))b'(x) - f(a(x))a'(x)
\end{align}
$$

Questo dimostra la formula $(4)$. Per rendere più chiaro il meccanismo, consideriamo per esempio:

$$\Phi(x) = \int_{x}^{x^2} \sin(t^2) \ dt$$

La funzione integranda è la [funzione seno](../sine-function/) che è continua su $\mathbb{R}.$ Entrambi gli estremi sono derivabili. L'estremo inferiore $a(x) = x$ ha derivata $a'(x) = 1,$ e l'estremo superiore $b(x) = x^2$ ha derivata $b'(x) = 2x.$ La regola di Leibniz dà:

$$
\begin{align}
\Phi'(x) &= \sin\!\left((x^2)^2\right) \cdot 2x - \sin(x^2) \cdot 1 \\[6pt]
         &= 2x \sin(x^4) - \sin(x^2)
\end{align}
$$

La funzione integranda $\sin(t^2)$ non ammette [primitive elementari](../integration-strategies/), ma la regola di Leibniz fornisce in forma chiusa la derivata dell'integrale.

## Il secondo teorema fondamentale del calcolo integrale

Passiamo adesso al secondo teorema e consideriamo una funzione $f$ continua su $[a, b],$ e supponiamo che $F,$ la sua primitiva, sia continua su $[a, b],$ derivabile su $(a, b)$ e soddisfi $F'(x) = f(x)$ per ogni $x \in (a, b).$ In questo caso vale:

$$\int_a^b f(x) \ dx = F(b) - F(a)$$

Come anticipato in premessa, il secondo enunciato afferma che l'integrale definito è la variazione di una qualunque primitiva sull'intervallo di integrazione. Definiamo adesso una nuova funzione $G(x)$:

$$G(x) = \int_a^x f(t) \ dt$$

Per il primo teorema fondamentale $G'(x) = f(x).$ Poiché $F$ e $G$ hanno la stessa derivata, il [teorema di Lagrange](../lagrange-theorem/) implica che la loro differenza è costante:

$$F(x) = G(x) + c$$

Valutando in $x = a$ otteniamo:

$$F(a) = G(a) + c$$

Poiché $G(a) = 0,$ la costante è $c = F(a),$ e quindi:

$$G(x) = F(x) - F(a)$$

Per $x = b$ questa identità diventa:

$$\int_a^b f(x) \ dx = G(b) = F(b) - F(a)$$

Quindi, per una funzione continua $f,$ l'integrale definito è l'[area netta con segno](../finding-areas-by-integration/) compresa tra il suo grafico e l'asse orizzontale. Per il teorema, tale area è la variazione $F(b) - F(a)$ di una qualunque primitiva $F.$

## Una precisazione sulla continuità

La continuità di $f$ è una condizione sufficiente per entrambi gli enunciati precedenti. Quando $f$ è soltanto integrabile secondo Riemann, la funzione integrale conserva alcune di queste proprietà, ma non tutte.

Ad esempio, sia $f$ [integrabile secondo Riemann](../riemann-integrability-criteria/) su $[a, b],$ e definiamo la funzione integrale:

$$F(x) = \int_a^x f(t) \ dt$$

La funzione $F$ è definita per ogni $x \in [a, b].$ Una funzione integrabile secondo Riemann è limitata, quindi $|f|$ ammette una maggiorazione $K$ su $[a, b].$ Qui $f$ non ha necessariamente minimo o massimo. Per $u, v \in [a, b]$ con $u < v,$ applicando la stima $(3)$ all'intervallo $[u, v]$ otteniamo:

$$|F(v) - F(u)| = \left| \int_{u}^{v} f(t) \ dt \right| \leq K (v - u)$$

Per simmetria la stessa stima vale con $|v - u|.$ Quindi $F$ è lipschitziana su $[a, b]$ con costante di Lipschitz $K,$ e in particolare è continua. La derivabilità dipende dal comportamento locale di $f.$ Fissiamo un punto $x_0 \in (a, b)$ in cui $f$ è continua, e sia $\varepsilon > 0.$ Poiché $f$ è continua in $x_0,$ scegliamo $\delta > 0$ in modo che valga la disuguaglianza seguente ogni volta che $|t - x_0| < \delta:$

$$|f(t) - f(x_0)| < \varepsilon$$

Se $0 < |h| < \delta$ e $x_0 + h \in [a, b],$ allora:

$$
\begin{align}
\left|\frac{F(x_0 + h) - F(x_0)}{h} - f(x_0)\right|
&= \left|\frac{1}{h}\int_{x_0}^{x_0 + h} (f(t) - f(x_0)) \ dt\right| \\[6pt]
&\leq \frac{1}{|h|}\int_{\min\{x_0,x_0+h\}}^{\max\{x_0,x_0+h\}} |f(t) - f(x_0)| \ dt \\[6pt]
&< \varepsilon
\end{align}
$$

Quindi $F'(x_0) = f(x_0).$ Questa dimostrazione richiede la continuità soltanto in $x_0,$ mentre il teorema della media integrale usato sopra richiede la continuità su tutto l'intervallo di integrazione. Lo stesso ragionamento fornisce la derivata quando $x_0$ è un estremo. In un punto di [discontinuità](../discontinuities-of-real-functions/) di $f$ il rapporto incrementale di $F$ può non convergere, e la derivabilità può venire meno.

Consideriamo ad esempio la [funzione segno](../sign-function/) su $[-1, 1]:$

$$
f(t) = \begin{cases} -1 & \text{se } t < 0 \\[6pt] 0 & \text{se } t = 0 \\[6pt] 1 & \text{se } t > 0 \end{cases}
$$

La funzione $f$ è integrabile secondo Riemann su $[-1, 1]$ perché è limitata e ha una sola discontinuità. Prendendo $-1$ come punto base, quando $x \in [-1, 0)$ la funzione integranda vale $-1$ su tutto l'intervallo di integrazione, quindi:

$$F(x) = \int_{-1}^{x} (-1) \ dt = -x - 1$$

Per $x \in [0, 1]$ l'intervallo di integrazione attraversa $0,$ quindi l'additività dà:

$$F(x) = \int_{-1}^{0} (-1) \ dt + \int_{0}^{x} 1 \ dt = -1 + x$$

Entrambe le espressioni danno $F(0) = -1,$ quindi $F(x) = |x| - 1$ su $[-1, 1].$ Si tratta della [funzione valore assoluto](../absolute-value-function/) traslata verso il basso di $1.$ La funzione $F$ è continua su questo intervallo. Per $x \neq 0$ la sua derivata esiste ed è uguale a $f(x).$ Nell'origine la derivata sinistra è $-1$ e la derivata destra è $1,$ quindi $F$ ha un [punto di non derivabilità](../points-of-non-differentiability/) in corrispondenza dell'unica discontinuità di $f.$

Il teorema ammette ulteriori estensioni e applicazioni, che esulano però dallo scopo della presente trattazione.

## Esempio 1

Applichiamo ora il teorema fondamentale del calcolo in due casi concreti, prima per valutare un integrale definito mediante una primitiva nota e poi per costruire una primitiva mediante una funzione integrale. Calcoliamo per esempio il seguente semplice integrale:

$$\int_0^1 3x^2 \ dx$$

Una primitiva di $3x^2$ è $F(x) = x^3.$ Per il secondo teorema fondamentale si ha:

$$\int_0^1 3x^2 \ dx = F(1) - F(0) = 1^3 - 0^3 = 1$$

Quindi l'area sottesa dalla curva $3x^2$ su $[0, 1]$ è $1.$

- - -

Consideriamo adesso la [funzione logaritmica](../logarithmic-function/) e valutiamo:

$$H(x) = \int_1^x \ln t \ dt$$

Il valore $H(1)$ è $0$ perché un integrale su un intervallo degenere è nullo. Poiché $\ln t$ è continua per $t > 0,$ la funzione $H$ è definita per $x > 0.$ Il primo teorema fondamentale dà:

$$H'(x) = \ln x$$

Quindi $H$ è una primitiva di $\ln x$ su $(0, +\infty)$ con $H(1) = 0.$

## Esempio 2

Consideriamo ora una funzione integranda che non ammette primitive elementari. Il primo teorema fondamentale permette comunque di calcolare la derivata della corrispondente funzione integrale:

$$\frac{d}{dx} \int_1^x e^{-t^2} \ dt$$

La funzione integranda $f(t) = e^{-t^2}$ è la [funzione esponenziale](../exponential-function/) composta con $-t^2,$ quindi è continua su $\mathbb{R}.$ L'estremo inferiore è costante e l'estremo superiore è $x.$ Il primo teorema fondamentale dà:

$$\frac{d}{dx} \int_1^x e^{-t^2} \ dt = e^{-x^2}$$

Qui non serve una primitiva elementare perché la funzione $e^{-t^2}$ non ne ammette, ma la derivata scritta sopra è esplicita. Un integrale definito di questa funzione può essere approssimato per [via numerica](../numerical-integration/) oppure espresso mediante la funzione errore $\mathrm{erf},$ definita da:

$$\mathrm{erf}(x) = \frac{2}{\sqrt{\pi}}\int_0^x e^{-t^2} \ dt$$

## La formulazione infinitesimale

Per chi desidera approfondire, il teorema fondamentale del calcolo integrale ammette anche una formulazione infinitesimale nel quadro dell'analisi non standard. Sia $x$ un punto reale interno al dominio, e indichiamo con gli stessi simboli le estensioni naturali di $F$ e $f$ agli iperreali. Se, per ogni infinitesimo non nullo $\Delta x$ con $x+\Delta x$ nel dominio, il rapporto incrementale è finito e la sua parte standard non dipende da $\Delta x,$ allora $F$ è derivabile in $x$ e:

$$F'(x) = \mathrm{st}\!\left(\frac{F(x + \Delta x) - F(x)}{\Delta x}\right)$$

Per il principio di transfer, quando $\Delta x > 0$ e $m$ e $M$ sono il minimo e il massimo di $f$ sull'intervallo di estremi $x$ e $x+\Delta x,$ la stima $(1)$ diventa:

$$m\Delta x \leq F(x + \Delta x) - F(x) \leq M\Delta x$$

Dividendo per $\Delta x,$ il rapporto incrementale è compreso tra $m$ e $M,$ che per la continuità di $f$ sono infinitamente vicini a $f(x).$ Per $\Delta x < 0$ si ottiene la stessa conclusione invertendo gli estremi dell'integrale. La parte standard del rapporto incrementale è quindi $f(x)$ per ogni infinitesimo non nullo $\Delta x,$ da cui $F'(x) = f(x).$

>  Se siete curiosi, un testo basato su questa formulazione è [Elementary Calculus: An Infinitesimal Approach](https://people.math.wisc.edu/~hkeisler/calc.html) di H. Jerome Keisler, la cui seconda edizione del 1986 tratta il teorema fondamentale nella sezione 4.2.
