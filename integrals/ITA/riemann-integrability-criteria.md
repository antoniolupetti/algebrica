---
title: Riemann Integrability Criteria
source: https://algebrica.org/riemann-integrability-criteria/
license: CC BY-NC 4.0
tags:
  - funzione-di-dirichlet
  - funzione-di-thomae
  - funzioni-continue
  - funzioni-limitate
  - funzioni-monotone
  - integrale-definito
  - integrale-di-riemann
  - integrazione
  - misura-di-lebesgue
  - partizione
  - somme-di-darboux
---
## Partizioni, somme superiori e somme inferiori

Sappiamo che l'integrale di Riemann di una [funzione](../functions/) limitata su un [intervallo chiuso](../intervals/) misura l'area (considerata con segno) al di sotto del suo grafico. Questo processo avviene tramite approssimazioni con rettangoli che via via convergono verso il medesimo valore. Di norma, il problema principale risiede nello stabilire se questo processo determinato dal [passaggio al limite](../limits/) sia ben definito. Di seguito illustreremo una serie di criteri che rispondono a questa domanda anche quando la funzione non è evidentemente [continua](../continuous-functions/).

I criteri che presenteremo permettono di stabilire l'integrabilità di una funzione limitata $f$ su $[a,b]$ nei casi seguenti. Le ultime due condizioni utilizzano la misura di Lebesgue, che introdurremo più avanti.

+ Se $f$ è continua su $[a, b],$ allora è integrabile.
+ Se $f$ è monotona su $[a, b],$ allora è integrabile.
+ Se $f$ ha solo un numero finito di discontinuità, allora è integrabile.
+ Se le discontinuità di $f$ formano un insieme di misura nulla, allora è integrabile.
+ Se l'insieme delle discontinuità di $f$ ha misura di Lebesgue positiva, allora $f$ non è integrabile secondo Riemann.

- - -

Iniziamo considerando due punti $a < b$ e una funzione limitata $f:[a,b]\to\mathbb{R}.$ Definiamo una partizione $P$ di $[a,b]$ come un insieme finito di punti $P = \{\ x_0, x_1, \dots, x_n \ \}$ per cui possiamo scrivere:

$$a = x_0 < x_1 < \cdots < x_n = b$$

Su ciascun sottointervallo $[x_{i-1}, x_i]$ definiamo l'estremo superiore e l'estremo inferiore di $f.$ Poiché $f$ è limitata, possiamo definire l'estremo superiore e quello inferiore come segue:

$$M_i = \sup_{x \in [x_{i-1}, x_i]} f(x)$$

$$m_i = \inf_{x \in [x_{i-1}, x_i]} f(x)$$

$M_i$ è il più piccolo numero maggiore o uguale a tutti i valori che $f$ assume sul sottointervallo $[x_{i-1},x_i],$ mentre $m_i$ è il più grande numero minore o uguale a tutti i valori che $f$ assume sullo stesso sottointervallo. In figura abbiamo una funzione non negativa con le somme inferiori. Su ciascun sottointervallo, il lato superiore del rettangolo si trova alla quota $m_i$ e giace sul grafico o al di sotto di esso.

![Fig. 1](../svg/riemann-integrability-criteria-1.svg)


L'immagine successiva mostra invece la somma superiore. Il lato superiore di ciascun rettangolo si trova alla quota $M_i$ e giace sul grafico o al di sopra di esso.

![Fig. 2](../svg/riemann-integrability-criteria-2.svg)

Sappiamo che quando $f$ è integrabile secondo Riemann, il suo integrale è compreso tra le somme inferiori e quelle superiori.

Quando $f$ è continua, $M_i$ e $m_i$ coincidono con il massimo e il minimo effettivamente assunti sul sottointervallo ma per una funzione limitata generica si usano l'estremo superiore e l'estremo inferiore perché il massimo o il minimo potrebbero non essere mai raggiunti in quell'intervallo. 

Mediante $M_i$ e $m_i$ si definiscono quelle che definiamo le somme superiori e inferiori di Darboux date rispettivamente da:

$$U(f, P) = \sum_{i=1}^n M_i(x_i - x_{i-1})$$

$$L(f, P) = \sum_{i=1}^n m_i(x_i - x_{i-1})$$

Per tali somme valgono le seguenti proprietà di ordine:

+ Raffinando la partizione in intervalli via via sempre più piccoli, la somma superiore può solo diminuire o restare invariata, mentre la somma inferiore può solo aumentare o restare invariata. 
+ Inoltre, ogni somma inferiore è minore o uguale a ogni somma superiore, anche quando sono associate a partizioni diverse, perché entrambe possono essere confrontate mediante un raffinamento comune. 

In particolare vale la seguente relazione:

$$L(f, P) \leq U(f, P)$$

Un raffinamento riduce quindi lo scarto tra le somme superiori e inferiori o al più lo lascia invariato, ma tale scarto non tende necessariamente a zero.

## Il criterio di Darboux

Il criterio di Darboux stabilisce che una funzione limitata su un intervallo chiuso e limitato è integrabile secondo Riemann se e solo se esistono partizioni che rendono arbitrariamente piccola la differenza tra la somma superiore e quella inferiore. Per mostrarlo, iniziamo col definire l'integrale superiore e l'integrale inferiore di $f$ come l'estremo inferiore di tutte le somme superiori e l'estremo superiore di tutte le somme inferiori:

$$U(f) = \inf_{P} U(f, P)$$

$$L(f) = \sup_{P} L(f, P)$$

In entrambe le definizioni, $P$ varia tra tutte le partizioni di $[a, b].$ La quantità $U(f)$ è il più grande minorante delle somme superiori, mentre $L(f)$ è il più piccolo maggiorante delle somme inferiori. Le proprietà di ordine precedenti danno $L(f) \leq U(f)$ per ogni funzione limitata $f.$ Una funzione limitata $f$ è integrabile secondo Riemann su $[a, b]$ se e solo se questi due numeri coincidono:

$$U(f) = L(f)$$

In tal caso, il loro valore è dato dal seguente integrale:

$$\int_a^b f(x) \ dx = U(f) = L(f)$$

Questa uguaglianza fornisce quindi la definizione di integrabilità secondo Riemann. Il criterio di Darboux, equivalente alla definizione, afferma che una funzione limitata $f$ è integrabile secondo Riemann su $[a, b]$ se e solo se per ogni $\varepsilon > 0$ esiste una partizione $P$ tale che:

$$U(f, P) - L(f, P) < \varepsilon$$

![Fig. 3](../svg/riemann-integrability-criteria-3.svg)

I diagrammi illustrano il criterio per una funzione continua arbitraria. Una partizione poco fine lascia uno scarto visibile tra i rettangoli superiori e inferiori mentre raffinandola, lo scarto si riduce perché l'oscillazione di questa funzione è piccola sui sottointervalli di lunghezza sufficientemente piccola.

![Fig. 4](../svg/riemann-integrability-criteria-4.svg)

Per una funzione integrabile si può trovare una partizione che renda le somme superiori e inferiori vicine quanto si vuole e per dimostrare l'integrabilità è sufficiente costruire una tale partizione per ogni $\varepsilon > 0.$ In particolare, su ciascun sottointervallo $[x_{i-1}, x_i],$ la differenza $M_i - m_i$ è l'oscillazione di $f$ su quel sottointervallo. Con un calcolo diretto otteniamo:

$$U(f, P) - L(f, P) = \sum_{i=1}^n (M_i - m_i)(x_i - x_{i-1})$$

Questa identità esprime quindi lo scarto tra le somme di Darboux. Una funzione limitata è integrabile esattamente quando, per ogni $\varepsilon > 0,$ esiste una partizione che renda questa somma minore di $\varepsilon.$

La funzione non è invece integrabile secondo Riemann se lo scarto ammette un minorante positivo valido per tutte le partizioni, cioè se esiste una costante $\eta > 0$ tale che per ogni partizione vale:

$$
U(f,P)-L(f,P)=\sum_{i=1}^{n}(M_i-m_i)(x_i-x_{i-1})\geq\eta
$$

Infatti, scegliendo $\varepsilon=\eta,$ nessuna partizione soddisfa la disuguaglianza richiesta dal criterio di Darboux.

## Condizioni sufficienti di uso comune

Le tre condizioni seguenti implicano l'integrabilità secondo Riemann e spesso permettono di evitare una stima diretta delle somme di Darboux in quanto determinare l'estremo superiore e quello inferiore su ogni intervallo e identificare una partizione che renda lo scarto minore di $\varepsilon$ può non essere una passeggiata. Una funzione limitata $f$ su $[a, b]$ è integrabile secondo Riemann se soddisfa almeno una di esse.

+ Se $f$ è [continua](../continuous-functions/) su $[a, b],$ allora è uniformemente continua. La sua oscillazione $M_i - m_i$ è quindi uniformemente piccola su tutti i sottointervalli di lunghezza sufficientemente piccola, e il criterio di Darboux dà l'integrabilità.
+ Se $f$ è monotona su $[a, b],$ indichiamo con $\lVert P\rVert$ la massima lunghezza dei sottointervalli. Maggiorando la lunghezza di ciascun sottointervallo con $\lVert P\rVert,$ si ottiene $U(f, P) - L(f, P) \leq \lVert P\rVert|f(b) - f(a)|,$ perché i valori assoluti delle differenze tra i valori agli estremi formano una somma telescopica. Lo scarto può quindi essere reso arbitrariamente piccolo.
+ Se $f$ è limitata e ha solo un numero finito di [discontinuità](../discontinuities-of-real-functions/), si possono ricoprire tali punti con intervalli di lunghezza totale arbitrariamente piccola. La limitatezza controlla il contributo di questi intervalli. Sulle porzioni compatte rimanenti, $f$ è uniformemente continua, e ciò permette di controllare il resto dello scarto tra le somme di Darboux. Questa condizione comprende le [funzioni continue a tratti](../piecewise-functions/) su intervalli chiusi e limitati.

Attenzione, perché una funzione può essere integrabile anche se non soddisfa nessuna delle tre condizioni precedenti. Inoltre, le discontinuità possono essere dense nell'intervallo persino per una funzione monotona. Per caratterizzare l'integrabilità secondo Riemann occorre quindi considerare la misura dell'insieme delle discontinuità, come vedremo nel prossimo criterio.

## Il criterio dell'insieme delle discontinuità

Analizziamo adesso un caso avanzato considerando una funzione limitata $f:[a,b]\to\mathbb{R}.$ Tale funzione è integrabile secondo Riemann se e solo se il suo insieme delle discontinuità ha misura di Lebesgue nulla ovvero, in termini semplici, se è possibile ricoprire tutti i punti di discontinuità con una famiglia finita o numerabile di intervalli la cui somma delle lunghezze sia arbitrariamente piccola.

In termini formali, un insieme $D \subset [a, b]$ ha misura nulla se, per ogni $\varepsilon > 0,$ può essere ricoperto da una famiglia numerabile di intervalli la cui lunghezza totale è minore di $\varepsilon.$ L'insieme delle discontinuità può quindi essere infinito o denso, purché abbia misura nulla. I due esempi seguenti mettono a confronto un insieme di discontinuità di misura positiva con uno di misura nulla.

- - -

Prendiamo come caso di esempio la [funzione di Dirichlet](../dirichlet-function/) definita da:

$$
f(x) =
\begin{cases}
1 & x \in \mathbb{Q} \\[6pt]
0 & x \notin \mathbb{Q}
\end{cases}
$$

Tale funzione è [discontinua](../discontinuities-of-real-functions/) in ogni punto di $[a, b],$ quindi il suo insieme delle discontinuità è l'intero intervallo e ha misura positiva. La funzione di Dirichlet non è dunque integrabile secondo Riemann. Ogni sottointervallo contiene sia numeri razionali sia numeri irrazionali, perciò $M_i = 1$ e $m_i = 0$ per ogni $i.$ Ne segue che $U(f, P) - L(f, P) = b - a$ per ogni partizione $P,$ indipendentemente da quanto sia fine.

- - -

Ogni insieme finito o numerabile ha misura di Lebesgue nulla. Consideriamo ora la funzione di Thomae, definita da:

$$
t(x) =
\begin{cases}
0 & x \notin \mathbb{Q} \\[6pt]
\dfrac{1}{q} & x = \dfrac{p}{q}
\end{cases}
$$

Nella seconda riga, $p\in\mathbb{Z},$ $q\in\mathbb{N},$ $q>0$ e la frazione $p/q$ è ridotta ai minimi termini.

Tale funzione è discontinua esattamente nei numeri razionali e continua in ogni numero irrazionale. I razionali in $[a, b]$ formano un insieme numerabile, quindi la funzione di Thomae è integrabile secondo Riemann. Poiché $t \geq 0$ e ogni sottointervallo contiene un numero irrazionale, ogni somma inferiore di Darboux è nulla. Il valore comune dell'integrale superiore e dell'integrale inferiore è dunque zero.
