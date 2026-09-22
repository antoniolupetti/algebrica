---
title: Definite Integrals
source: https://algebrica.org/definite-integrals/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - definite-integral
  - exponential-function
  - fundamental-theorem-of-calculus
  - geometric-sequence
  - improper-integrals
  - integration
  - linearity
  - mean-value-theorem
  - oriented-area
  - riemann-integral
  - riemann-sum
---
## Non abbiate fretta

Adrien-Marie Legendre è uno dei matematici più noti e influenti del Settecento. Nacque a Parigi, nel 1752 e intorno ai trent'anni iniziò ad interessarsi della teoria degli integrali ellittici, oggetti matematici utilizzati per il calcolo della lunghezza di un arco di [ellisse](../ellipse/).

Il problema non è banale, soprattutto non lo era all'epoca, quando non esisteva ancora una teoria consolidata per la sua risoluzione. Per un'ellisse con semiasse maggiore $a$ ed eccentricità $e\in[0,1),$ il perimetro è espresso dal seguente integrale ellittico completo di seconda specie:

$$
L=4aE(e)=4a\int_{0}^{\pi/2}\sqrt{1-e^2\sin^2\theta} \ d\theta
$$

Non affronteremo questi oggetti complessi nella nostra esposizione, ma ci focalizzeremo sulle tipologie di integrali definiti tipicamente trattate nelle scuole superiori e nei corsi di calcolo dei primi anni universitari. Sappiate però che certi mostri esistono e che richiedono metodi risolutivi tutt'altro che banali.

Nella formula $\pi/2$ e $0$ sono gli estremi di integrazione che differenziano, quantomeno in termini di rappresentazione, gli integrali definiti da quelli [indefiniti](../indefinite-integrals/).

Tornando alla nostra storia, le fonti indicano il 1786 come l'anno delle prime pubblicazioni di Legendre sulla teoria degli integrali ellittici. Le sue ricerche, tra il 1811 e il 1819, portarono alla pubblicazione di ulteriori volumi dedicati allo sviluppo della teoria e alle relative applicazioni. Non soddisfatto del proprio lavoro, qualche anno più tardi finì per riscrivere daccapo l'intero corpus, tenendolo aggiornato fino agli ultimi anni di vita. 

In una mattina d'inizio agosto, Legendre ricevette una lettera da Carl Gustav Jacobi, all'epoca ventiduenne, che offriva un cambio di prospettiva sull'argomento e proponeva una nuova teoria che rendeva obsoleta quella a cui Legendre aveva lavorato per quasi quarant'anni. Agli stessi risultati giunse il giovane norvegese Niels Henrik Abel.

Le fonti riferiscono che Legendre sostenne apertamente il lavoro dei due giovani, nonostante questo vanificasse quasi del tutto quattro decenni di ricerche. Abel morì a 26 anni. Jacobi a 46. Legendre arrivò, invece, ad ottant'anni.

Per tornare in argomento, a noi non serviranno quarant'anni per imparare a risolvere gli integrali definiti. Impiegheremo molto meno. Se avete già compreso cos'è un integrale indefinito e memorizzato le sue principali proprietà con le primitive fondamentali, siete già a buon punto. Altrimenti vi consiglio di fermarvi qui e di fare un necessario passo indietro.

In estrema sintesi un integrale definito rappresenta l'accumulazione di una quantità data da una funzione $y=f(x)$ all'interno di un intervallo $[a, b]$. In termini meno precisi, ma comunque validi, misura l'area con segno tra una certa curva e l'asse delle $x,$ dove le porzioni che si trovano sopra l'asse $x$ si sommano mentre quelle sotto si sottraggono.

In questa entry saranno trattate le principali definizioni e proprietà degli integrali definiti, mentre i metodi e le [strategie di integrazione](../integration-strategies/), che rappresentano il fulcro risolutivo del calcolo integrale, saranno trattati nelle apposite sezioni.

## Area sotto il grafico di una funzione: dalla curva all'integrale

Consideriamo una [funzione](../functions/) $f(x)$ definita su un [intervallo chiuso](../intervals/) $[a, b]$, con $a < b$. Se $f(x)$ è [continua](../continuous-functions/) e non negativa su $[a, b]$, il suo grafico, l'asse delle $x$ e le rette verticali $x = a$ e $x = b$ delimitano un trapezoide. L'area di questa regione è data dall'integrale definito:

$$\int_{a}^{b} f(x) \ dx$$

![Img. 1](svg/definite-integrals-1.svg)

Le formule usuali della geometria elementare non si applicano direttamente a un trapezoide generico, perché uno dei suoi contorni è una curva anziché un segmento rettilineo. L'area del trapezoide può essere approssimata suddividendo l'intervallo $[a, b]$ in $n$ sottointervalli di uguale ampiezza:

$$\Delta x = \frac{b - a}{n}$$

Su ciascun sottointervallo, la regione viene approssimata mediante un rettangolo e la somma delle aree di questi rettangoli fornisce una stima dell'area totale.

![Img. 2](svg/definite-integrals-2.svg)

Indichiamo i punti della partizione con $x_i = a + i\Delta x,$ per $i=0,\ldots,n.$ Si ha quindi $x_0=a$ e $x_n=b,$ e l'$i$-esimo sottointervallo è $[x_{i-1},x_i].$ Indicando con $m_i$ e $M_i$ l'estremo inferiore e l'estremo superiore di $f(x)$ su questo sottointervallo, definiamo le somme inferiori e superiori come:

$$s_n^{-} = \sum_{i=1}^{n} m_i \Delta x \qquad s_n^{+} = \sum_{i=1}^{n} M_i \Delta x$$

La somma inferiore $s_n^{-}$ approssima l'area per difetto, mentre la somma superiore $s_n^{+}$ la approssima per eccesso.

![Img. 3](svg/definite-integrals-3.svg)

I dati dei rettangoli inferiori e superiori seguono lo stesso schema su ogni sottointervallo:

| Rettangolo | Sottointervallo | Altezza inferiore | Altezza superiore | Area inferiore | Area superiore |
| :-------: | :-------------: | :----------: | :----------: | :-----------: | :-----------: |
|    $1$    |   $[x_0,x_1]$   |    $m_1$     |    $M_1$     | $m_1\Delta x$ | $M_1\Delta x$ |
|    $2$    |   $[x_1,x_2]$   |    $m_2$     |    $M_2$     | $m_2\Delta x$ | $M_2\Delta x$ |
|    $3$    |   $[x_2,x_3]$   |    $m_3$     |    $M_3$     | $m_3\Delta x$ | $M_3\Delta x$ |
| $\vdots$  |    $\vdots$     |   $\vdots$   |   $\vdots$   |   $\vdots$    |   $\vdots$    |
|    $n$    | $[x_{n-1},x_n]$ |    $m_n$     |    $M_n$     | $m_n\Delta x$ | $M_n\Delta x$ |


La costruzione con sottointervalli di uguale ampiezza è un caso particolare di una partizione i cui sottointervalli possono avere ampiezze diverse. Per una partizione arbitraria $P$ data da $a = x_0 < x_1 < \cdots < x_n = b,$ le somme inferiori e superiori sono:

$$
\begin{align}
L(f, P) &= \sum_{i=1}^{n} m_i(x_i - x_{i-1}) \\[6pt]
U(f, P) &= \sum_{i=1}^{n} M_i(x_i - x_{i-1})
\end{align}
$$

Se una partizione $P'$ raffina $P$ aggiungendo punti di suddivisione, la somma inferiore non può diminuire e la somma superiore non può aumentare. Di conseguenza:

$$L(f, P) \leq L(f, P') \leq U(f, P') \leq U(f, P)$$

Per una funzione $f(x)$ limitata su $[a, b],$ gli integrali inferiore e superiore forniscono le migliori stime ottenute considerando tutte le possibili partizioni:

$$
\begin{align}
L(f, [a, b]) &= \sup_P L(f, P) \\[6pt]
U(f, [a, b]) &= \inf_P U(f, P)
\end{align}
$$

Ogni somma inferiore è minore o uguale a ogni somma superiore, quindi $L(f, [a, b]) \leq U(f, [a, b]).$ La funzione $f(x)$ è [integrabile secondo Riemann](../riemann-integrability-criteria/) se e solo se questi due valori coincidono. Il loro valore comune è l'integrale definito:

$$L(f, [a, b]) = U(f, [a, b]) = \int_{a}^{b} f(x) \ dx$$

Una definizione equivalente dell'integrale definito utilizza le somme di Riemann con punti campione. Per una partizione $P$ data da $a = x_0 < x_1 < \cdots < x_n = b,$ scegliamo un punto $\xi_i \in [x_{i-1},x_i]$ in ciascun sottointervallo e poniamo $\Delta x_i = x_i - x_{i-1}.$ Il punto $\xi_i$ è detto punto campione dell'$i$-esimo sottointervallo e la norma di $P$ è definita da:

$$
\|P\| = \max_{1 \leq i \leq n} \Delta x_i
$$

Una funzione limitata $f$ è integrabile secondo Riemann con integrale $I$ se, per ogni $\varepsilon>0,$ esiste $\delta>0$ tale che ogni partizione $P$ e ogni scelta dei punti campione soddisfino:

$$
\|P\|<\delta
\implies
\left|\sum_{i=1}^{n}f(\xi_i)\Delta x_i-I\right|<\varepsilon
$$

Questa condizione richiede che tutte le somme di Riemann con punti campione, relative a partizioni di norma sufficientemente piccola, si avvicinino allo stesso valore. Si esprime comunemente con la notazione abbreviata:

$$
\int_a^b f(x) \ dx
=
\lim_{\|P\| \to 0}
\sum_{i=1}^{n} f(\xi_i)\Delta x_i
$$

Il limite indicato considera quindi tutte le partizioni con punti campione, anziché un'unica successione prefissata. In questa voce utilizzeremo la formulazione di Darboux mediante $L(f,P)$ e $U(f,P).$ Ogni somma di Riemann con punti campione è compresa tra le corrispondenti somme inferiore e superiore. Insieme alle stime per partizioni sufficientemente fini, questa disuguaglianza dimostra che una funzione limitata su $[a,b]$ è integrabile secondo una definizione se e solo se lo è secondo l'altra, e che entrambe le definizioni assegnano lo stesso valore.

> John K. Hunter presenta la formulazione mediante partizioni con punti campione e ne dimostra l'equivalenza con la definizione di Darboux in Introduction to Analysis, riportato nella [bibliografia](../bibliography/).

- - -

Ogni funzione continua a valori reali su $[a, b]$ è integrabile secondo Riemann. La continuità su questo intervallo implica la continuità uniforme, che rende l'oscillazione $M_i - m_i$ uniformemente piccola quando i sottointervalli sono sufficientemente corti. I valori $a$ e $b$ sono gli estremi inferiore e superiore di integrazione, e $f(x)$ è la funzione integranda. La notazione $f(x) \ dx$ è suggerita dall'area $f(x)\Delta x$ di ciascun rettangolo usato nell'approssimazione. Il simbolo $dx$ identifica $x$ come variabile di integrazione e richiama il ruolo delle ampiezze dei sottointervalli nel passaggio al limite.

## Calcolo degli integrali definiti

Se $f(x)$ è continua su $[a, b]$ e $F(x)$ è una qualsiasi [primitiva](../indefinite-integrals/) di $f(x)$, l'integrale definito è dato dalla differenza dei valori della primitiva agli estremi:

$$\int_{a}^{b} f(x) \ dx = F(b) - F(a)$$

Le quantità che compaiono in questa espressione hanno il seguente significato:

+ $F(x)$ è continua su $[a, b]$, derivabile su $(a, b)$ e soddisfa $F'(x) = f(x)$ per ogni $x \in (a, b)$.
+ $F(b)$ e $F(a)$ sono i valori della primitiva calcolati rispettivamente agli estremi superiore e inferiore di integrazione.

Questa formula è la conclusione del secondo [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/). La prima parte del teorema stabilisce che la funzione ottenuta integrando da un punto fisso a un estremo variabile è derivabile, con derivata uguale alla funzione integranda. Definiamo la funzione integrale mediante:

$$F(x) = \int_{a}^{x} f(t) \ dt$$

Per ogni $x \in (a, b)$, questa funzione soddisfa $F'(x) = f(x)$, per cui derivazione e integrazione sono operazioni inverse in un senso preciso. Entrambi i risultati sono trattati in dettaglio nella pagina dedicata al [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/).

## Proprietà

Quando i due estremi di integrazione coincidono, l'integrale si annulla:

$$\int_{a}^{a} f(x) \ dx = 0$$

L'identità segue direttamente dalla definizione, poiché un intervallo di ampiezza nulla non contribuisce all'area. Scambiando gli estremi di integrazione, l'integrale cambia segno:

$$\int_{a}^{b} f(x) \ dx = -\int_{b}^{a} f(x) \ dx$$

Questo riflette la natura orientata dell'integrale definito, poiché percorrere l'intervallo in senso opposto inverte il segno dell'area accumulata. Se $f(x) = k$ è costante su $[a, b]$, il suo integrale è il valore costante moltiplicato per la lunghezza dell'intervallo:

$$\int_{a}^{b} k \ dx = k(b - a)$$

Un fattore costante può essere portato fuori dal segno di integrale:

$$\int_{a}^{b} kf(x) \ dx = k \int_{a}^{b} f(x) \ dx$$

L'integrale è additivo rispetto alla somma di funzioni:

$$\int_{a}^{b} (f(x) + g(x)) \ dx = \int_{a}^{b} f(x) \ dx + \int_{a}^{b} g(x) \ dx$$

Le due proprietà precedenti rendono l'integrale definito un operatore lineare. L'integrale è additivo anche rispetto a intervalli adiacenti. Per tre punti qualsiasi $a$, $b$, $c$ nel dominio di $f$, vale la seguente identità:

$$\int_{a}^{c} f(x) \ dx = \int_{a}^{b} f(x) \ dx + \int_{b}^{c} f(x) \ dx$$

Questa additività consente di [integrare una funzione definita a tratti](../piecewise-functions/) suddividendo l'intervallo nei punti di raccordo.

Se $f(x) \leq g(x)$ per ogni $x \in [a, b]$, la stessa disuguaglianza vale per gli integrali:

$$\int_{a}^{b} f(x) \ dx \leq \int_{a}^{b} g(x) \ dx$$

> Questa è la proprietà di confronto degli integrali. La differenza verticale $g(x) - f(x)$ è non negativa su tutto l'intervallo, quindi anche il suo integrale è non negativo.

- - -

Per una funzione limitata $f(x)$ integrabile secondo Riemann su $[a, b],$ applicando la proprietà di confronto alle funzioni costanti uguali al suo estremo inferiore e al suo estremo superiore si ottengono le stime:

$$
(b - a)\inf_{x \in [a, b]} f(x)
\leq \int_{a}^{b} f(x) \ dx
\leq (b - a)\sup_{x \in [a, b]} f(x)
$$

Se $f(x)$ è integrabile secondo Riemann, anche $|f(x)|$ è integrabile secondo Riemann. Le disuguaglianze $-|f(x)| \leq f(x) \leq |f(x)|$ e la proprietà di confronto implicano:

$$\left|\int_{a}^{b} f(x) \ dx\right| \leq \int_{a}^{b} |f(x)| \ dx$$

## Teorema della media integrale

Il [teorema della media integrale](../mean-value-theorem-for-integrals/) afferma che, se $f(x)$ è continua su $[a, b]$, esiste almeno un punto $c \in (a, b)$ tale che:

$$\int_{a}^{b} f(x) \ dx = f(c)(b - a)$$

Il valore $f(c)$ è il valore medio della funzione sull'intervallo. Geometricamente, il teorema afferma l'esistenza di un rettangolo di base $b - a$ e altezza $f(c)$ la cui area orientata è uguale all'integrale definito. Il teorema garantisce l'esistenza di un tale punto senza fornire un metodo per individuarlo. Ricavando $f(c)$, il valore medio di $f$ su $[a, b]$ si può scrivere come:

$$f(c) = \frac{1}{b - a} \int_{a}^{b} f(x) \ dx$$

> Il teorema della media integrale è l'analogo, nel calcolo integrale, del [teorema di Lagrange](../lagrange-theorem/). L'enunciato differenziale garantisce un punto in cui il tasso di variazione istantaneo è uguale al tasso di variazione medio, mentre l'enunciato integrale garantisce un punto in cui il valore della funzione è uguale al valore medio sull'intervallo.

## Esempio 1

Calcoliamo il seguente integrale definito:

$$\int_{0}^{3} (3x - x^2) \ dx$$

Applicando la linearità e portando il fattore costante fuori dal primo integrale si ottiene:

$$3\int_{0}^{3} x \ dx - \int_{0}^{3} x^2 \ dx$$

La primitiva di ciascun termine si ricava dalla regola di integrazione delle potenze discussa nella pagina sugli [integrali indefiniti](../indefinite-integrals/):

$$F(x) = \frac{3x^2}{2} - \frac{x^3}{3}$$

Calcolando $F(3) - F(0)$ si ottiene:

$$
\begin{align}
F(3) - F(0) &= \left(\frac{3 \cdot 9}{2} - \frac{27}{3}\right) - \left(\frac{3 \cdot 0}{2} - \frac{0}{3}\right) \\[6pt]
            &= \frac{27}{2} - 9 \\[6pt]
            &= \frac{27 - 18}{2} \\[6pt]
            &= \frac{9}{2}
\end{align}
$$

L'area della regione delimitata dal grafico di $f(x) = 3x - x^2$ e dall'asse delle $x$ su $[0, 3]$ è quindi:

$$\int_{0}^{3} (3x - x^2) \ dx = \frac{9}{2}$$

> Quando una primitiva non è immediatamente riconoscibile, tecniche come l'[integrazione per sostituzione](../integration-by-substitution/) e l'[integrazione per parti](../integration-by-parts/) possono permettere di determinarla. Se non esiste una primitiva elementare, il calcolo dell'integrale definito può richiedere metodi numerici o funzioni speciali.

## Esempio 2

Calcoliamo il seguente integrale definito:

$$\int_{0}^{\pi} (x + \sin x) \ dx$$

> La funzione integranda combina un termine polinomiale con una funzione trigonometrica. Le primitive necessarie sono raccolte nella pagina sugli [integrali delle funzioni trigonometriche](../integral-of-trigonometric-functions/).

Applicando la linearità, l'integrale si scompone come segue:

$$\int_{0}^{\pi} x \ dx + \int_{0}^{\pi} \sin x \ dx$$

Determinando la primitiva di ciascun termine si ottiene:

$$F(x) = \frac{x^2}{2} - \cos x$$

Calcolando $F(\pi) - F(0)$ si ottiene:

$$
\begin{align}
F(\pi) - F(0) &= \left(\frac{\pi^2}{2} - \cos\pi\right) - \left(\frac{0}{2} - \cos 0\right) \\[6pt]
              &= \left(\frac{\pi^2}{2} + 1\right) - (0 - 1) \\[6pt]
              &= \frac{\pi^2}{2} + 2
\end{align}
$$

L'area della regione delimitata dal grafico di $f(x) = x + \sin x$ e dall'asse delle $x$ su $[0, \pi]$ è:

$$\int_{0}^{\pi} (x + \sin x) \ dx = \frac{\pi^2}{2} + 2$$

## Esempio 3

Calcoliamo l'area sotto la curva esponenziale $f(x)=e^{2x}$ su $[0,2]$ direttamente dalle somme di Riemann con punti campione negli estremi destri. Suddividiamo $[0,2]$ in $n$ sottointervalli di uguale ampiezza. L'ampiezza e l'estremo destro del $k$-esimo sottointervallo sono:

$$\Delta x = \frac{2}{n} \qquad x_k = \frac{2k}{n}$$

La funzione $f(x)=e^{2x}$ è crescente, quindi i rettangoli costruiti usando gli estremi destri forniscono somme superiori. L'altezza del $k$-esimo rettangolo è:

$$f(x_k) = e^{2x_k} = e^{4k/n}$$

La somma delle aree dei rettangoli è quindi:

$$R_n = \sum_{k=1}^{n} f(x_k)\Delta x = \frac{2}{n}\sum_{k=1}^{n} e^{4k/n}$$

Poniamo $q_n=e^{4/n}.$ I termini $e^{4k/n}=q_n^k$ formano una [progressione geometrica](../geometric-sequence/) finita, con $q_n^n=e^4.$ La formula per la somma finita fornisce:

$$
\begin{align}
R_n &= \frac{2}{n}\sum_{k=1}^{n}q_n^k \\[6pt]
    &= \frac{2}{n}\frac{q_n(q_n^n-1)}{q_n-1} \\[6pt]
    &= \frac{2q_n(e^4-1)}{n(q_n-1)}
\end{align}
$$

Quando $n$ tende all'infinito, $q_n$ tende a $1.$ Applicando il [limite notevole](../remarkable-limits/) per la funzione esponenziale si ottiene:

$$
\lim_{n \to \infty}n(q_n-1)
= \lim_{n \to \infty}4\left(\frac{e^{4/n}-1}{4/n}\right)
= 4
$$

Passando al limite nelle somme superiori si ottiene l'integrale definito:

$$
\int_{0}^{2}e^{2x} \ dx
= \lim_{n \to \infty}R_n
= \frac{e^4-1}{2}
$$

Poiché $e^{2x}$ è positiva su $[0,2],$ questo integrale è l'area geometrica sotto la curva, pari a circa $26.799.$

## Integrali definiti con aree positive e negative

L'interpretazione dell'integrale definito come area vale quando $f(x) \geq 0$ su tutto $[a, b]$. Quando $f(x)$ cambia segno all'interno dell'intervallo, l'integrale assegna un valore negativo alle porzioni della regione che si trovano sotto l'asse delle $x$, e il risultato è un'area orientata anziché un'area puramente geometrica.

![Img. 4](svg/definite-integrals-4.svg)

Per ricavare l'area geometrica, si suddivide l'intervallo $[a, b]$ in sottointervalli sui quali $f(x)$ mantiene segno costante. Se $f(x) \geq 0$ su $[a, c]$ e $f(x) \leq 0$ su $[c, b]$, l'additività fornisce l'integrale orientato:

$$\int_{a}^{b} f(x) \ dx = \int_{a}^{c} f(x) \ dx + \int_{c}^{b} f(x) \ dx$$

L'area geometrica si ottiene cambiando il segno del contributo negativo:

$$S = \int_{a}^{c} f(x) \ dx - \int_{c}^{b} f(x) \ dx = \int_{a}^{b} |f(x)| \ dx$$

Per una [funzione pari](../even-and-odd-functions/), la simmetria rispetto all'asse delle $y$ implica che i contributi di $[-a, 0]$ e $[0, a]$ siano uguali. Pertanto:

$$\int_{-a}^{a} f(x) \ dx = 2\int_{0}^{a} f(x) \ dx$$

![Img. 5](svg/definite-integrals-5.svg)

Per una [funzione dispari](../even-and-odd-functions/), la simmetria rispetto all'origine implica che i contributi di $[-a, 0]$ e $[0, a]$ siano uguali in valore assoluto ma di segno opposto. Pertanto:

$$\int_{-a}^{a} f(x) \ dx = 0$$

![Img. 6](svg/definite-integrals-6.svg)

In entrambi i casi, l'area geometrica compresa tra il grafico di $f(x)$ e l'asse delle $x$ su $[-a, a]$ si ottiene integrando il [valore assoluto](../absolute-value/) della funzione. Poiché $|f(x)|$ è pari quando $f(x)$ è pari o dispari, l'area è:

$$S = 2\int_{0}^{a} |f(x)| \ dx$$

Se $f(x)$ è pari e non negativa su $[0, a]$, questa formula si riduce a:

$$S = 2\int_{0}^{a} f(x) \ dx$$

Ulteriori esempi di calcolo di aree geometriche sono riportati nella pagina sul [calcolo delle aree mediante integrazione](../finding-areas-by-integration/).

## Integrali impropri

L'integrale di Riemann considerato sopra richiede un intervallo limitato e una funzione integranda limitata. Se l'intervallo è illimitato o la funzione integranda è illimitata in prossimità di un estremo o di un punto interno, si può definire un [integrale improprio](../improper-integrals/) sostituendo l'estremo problematico con un parametro e passando al limite. Per esempio, se $f(x)$ è integrabile secondo Riemann su ogni intervallo $[a,t]$ con $t>a,$ si ha:

$$\int_a^{+\infty}f(x) \ dx:=\lim_{t\to+\infty}\int_a^t f(x) \ dx$$

L'integrale converge soltanto quando il limite che lo definisce esiste ed è finito. La pagina dedicata presenta le definizioni degli altri tipi di integrale improprio, i criteri di convergenza e alcuni esempi svolti.
