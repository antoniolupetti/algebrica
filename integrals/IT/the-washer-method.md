---
title: The Washer Method for Volumes of Revolution
source: https://algebrica.org/the-washer-method/
license: CC BY-NC 4.0
tags:
  - annulus
  - calculus
  - definite-integral
  - disc-method
  - integral-applications
  - solids-of-revolution
  - volume
  - washer-method
---
## Regioni di piano separate dall'asse di rotazione

Il washer method serve a determinare l'area di un solido di rotazione che, al suo interno, presenti una cavità. Prima di introdurre il procedimento e le formule, è però necessaria una premessa.

Se avete avuto la pazienza di arrivare a questo punto, converrete sul fatto che gli integrali non sono meri strumenti analitici concepiti per complicare la vita degli studenti, ma hanno una chiara utilità geometrica non trascurabile. Bisogna anche ammettere che le categorie di integrali viste sin qui sono meno drammatiche di quanto dichiarato all'inizio della sezione. Questo non li rende, tuttavia, oggetti intrinsecamente amichevoli, ma significa solo che gli argomenti trattati finora, mantengono una sorta di amichevole cortesia, destinata, come vedremo, a sgretolarsi rapidamente più avanti.

Introducendo gli [integrali definiti](../definite-integrals), abbiamo appreso come questi rappresentino la misura con segno dell'area determinata da una certa curva $\gamma$ e l'asse delle $x,$ sommando le accumulazioni positive sopra l'asse $x$ e sottraendo quelle negative al di sotto dello stesso asse.

Proseguendo nelle spiegazioni è emerso poi che gli integrali possono essere utilizzati anche per calcolare i volumi di solidi, in particolare quelli generati da una rotazione di una superficie piana $R$ attorno all'asse $x$. Un metodo per determinare il volume di questi solidi è quello [dei dischi](../the-disc-method/) che, in termini molto sintetici, consente di calcolarne il valore ricorrendo al seguente integrale definito:

$$V = \int_a^b \pi \big(f(x)\big)^2 \ dx$$

Si noti che, facendo ruotare la superficie piana attorno all'asse delle ascisse, si ottiene un solido completamente pieno al suo interno, e il calcolo del suo volume diventa un'operazione relativamente semplice. 


![IMG. 1](svg/the-disk-method-1.svg)

In figura è riportato il caso di una sola curva generata dalla funzione $f(x)$, che determina una superficie $R,$ tutta al di sopra dell'asse $x.$

Come cambierebbe la situazione se avessimo un'ulteriore curva g(x) compresa tra l'asse delle ascisse e la $f(x)?$ Immaginiamo, cioè, di trovarci nel caso di due funzioni $f$ e $g$ continue su $[a, b],$ tali che valga $0 \lt g(x) \lt f(x)$ per ogni $x$ appartenente al suddetto intervallo.

![IMG. 2](svg/the-washer-method-1.svg)


Anche in questo caso, tra le due curve, possiamo identificare una regione di piano $R$ Simile a quella presente nella prima figura, ma con una differenza immediata: la superficie $R$ è separata dall'asse $x$ dalla condizione $g(x) > 0$ e pertanto se la si facesse ruotare attorno al medesimo asse, si genererebbe un solido cavo, il cui profilo esterno è determinato dalla funzione $f(x)$ mentre quello interno dalla $g(x).$


![IMG. 3](svg/the-washer-method-2.svg)


Ogni sezione di S ottenuta con il piano perpendicolare ad un punto qualsiasi $x_0$ identifica una cosiddetta corona circolare, caratterizzata da due circonferenze concentriche rispettivamente di raggio $f(x)$, per quello esterno, e $g(x)$ per quello interno.

L'area di una corona circolare è data dalla differenza fra l'area con cerchio di raggio $f(x)$ e quello di raggio $g(x)$ ed è pari quindi a:

$$A(x) = \pi(f(x))^2 - \pi(g(x))^2 = \pi\left[(f(x))^2 - (g(x))^2\right]$$

![IMG. 4](svg/the-washer-method-3.svg)

Tenete a mente che La differenza va calcolata fra i quadrati dei due raggi, e non fra i raggi perché stiamo sottraendo delle aree.

## Determinazione del volume

Entriamo adesso nel vivo del calcolo del volume. Per prima cosa, suddividiamo l'intervallo $[a,b]$ in $n$ sottointervalli uguali e di ampiezza $\Delta x = (b-a)/n,$ individuati ciascuno dai punti:

$$a = x_0 < x_1 < \cdots < x_n = b.$$

Possiamo indicare il generico sottointervallo come $[x_{k-1}, x_k]$ e scegliamo un punto $x_k^{*}$ al suo interno, nel quale misurare i due raggi.

Se l'ampiezza $\Delta x$ è piccola, la porzione di $S$ si discosta poco da un solido elementare, in particolare da un cilindro di raggio $f(x_k^{*})$ dal quale è stato asportato un cilindro interno di raggio $g(x_k^{*}),$ più piccolo di $f(x_k^{*})$, entrambi di altezza $\Delta x.$ È facilmente intuibile che il volume di questo solido si ottiene banalmente come differenza tra i volumi dei due cilindri ovvero attraverso la formula:

$$
\begin{align}
\Delta V_k &= \pi(f(x_k^{*}))^2\Delta x - \pi(g(x_k^{*}))^2\Delta x \\[6pt]
           &= \pi\left[(f(x_k^{*}))^2 - (g(x_k^{*}))^2\right]\Delta x
\end{align}
$$

Sommando i contributi di tutte le porzioni ottenute dai singoli sottointervalli, si ottiene una certa approssimazione del volume di $S$:

$$V \approx \sum_{k=1}^{n} \pi\left[(f(x_k^{*}))^2 - (g(x_k^{*}))^2\right]\Delta x$$

Il membro di destra è una [somma di Riemann](../riemann-integrability-criteria/) della funzione $\pi(f^2 - g^2)$ r e poiché $f$ e $g$ sono continue su $[a,b],$ anche la loro differenza $f^2 - g^2$ lo è, quindi la funzione integranda è integrabile secondo Riemann e la somma converge all'[integrale definito](../definite-integrals/) quando $\Delta x \to 0.$ 

Quando $n$ aumenta le singole porzioni diventano più sottili e approssimano meglioil profilo del solido. In tal caso il volume di $S$ è:

$$V = \pi\int_a^b \left[f^2(x) - g^2(x)\right] \ dx$$


Per la linearità dell'integrale possiamo anche scrivere:

$$V = \pi \left[\int_a^b f^2(x) \, dx - \int_a^b g^2(x) \, dx\right]$$

Analogamente a quanto mostrato prima, l'integrale di $f(x)^2$ determina il volume del solido generato dal grafico di $f,$ mentre l'integrale di $g(x)^2$ quello del volume "vuoto".

Quando $g$ è nulla la corona circolare degenera in un cerchio pieno e la formula si riduce a quella del metodo dei dischi che è un caso limite del metodo delle corone.

- - -

La costruzione del volume non richiede che l'asse di rotazione sia necessariamente un asse ordinato. Nella formula infatti sono presenti solo i due raggi della corona, quindi basta misurare la loro lunghezza a partire dall'asse effettivo anziché ad esempio dall'asse delle $x.$ Banalmente, se la rotazione avviene attorno ad una retta orizzontale $y = c$ con $c \leq g(x) \leq f(x)$ il raggio esterno della corona diventa $f(x) - c$ e quello interno $g(x) - c.$ Il volume pertanto può essere scritto come:

$$V = \pi\int_a^b \left[(f(x)-c)^2 - (g(x)-c)^2\right] \ dx$$

Quando invece l'asse sta al di sopra di $f$ e $g$, cioè vale $g(x) \leq f(x) \leq c,$ le distanze si misurano nel verso opposto e i due raggi diventano $c - g(x)$ e $c - f(x).$ In questa casistica è come se $f$ e $g$ si invertano cosicché $g$ diventa il raggio esterno e $f$ quello intero. Perciò anche il volume va riscritto come nella seguente formula:

$$V = \pi\int_a^b \left[(c-g(x))^2 - (c-f(x))^2\right] \ dx$$

Quando invece la rotazione avviene attorno all'asse delle $y,$ i ruoli delle due variabili si scambiano e la regione va descritta nella forma $0 \leq q(y) \leq x \leq p(y)$ per $y \in [a,b].$ In questo caso il volume è determinato da:

$$V = \pi\int_a^b \left[(p(y))^2 - (q(y))^2\right] \ dy$$

Per una retta verticale generica $x = c,$ i raggi devono invece essere misurati a partire da tale retta. Se $c \leq q(y) \leq p(y),$ il volume è:

$$V = \pi\int_a^b \left[(p(y)-c)^2 - (q(y)-c)^2\right] \ dy$$

Se invece $q(y) \leq p(y) \leq c,$ il raggio esterno è $c-q(y)$ e quello interno è $c-p(y),$ quindi il volume è:

$$V = \pi\int_a^b \left[(c-q(y))^2 - (c-p(y))^2\right] \ dy$$

Il principio di fondo rimane pressoché lo stesso al caso della rotazione attorno all'asse $x$, ma giusto per non dare l'impressione che questi processi siano diventati per voi troppo meccanici è pur sempre utile che manteniate viva una certa soglia di allerta per evitare errori banali nella risoluzione degli esercizi. Spesso si individua il procedimento corretto da seguire, ma si sbaglia nei dettagli e in sede s'esame anche una piccola distrazione può risultare fatale.å

## Esempio 1

Risolviamo adesso qualche esempio tipico, andando a calcolare il volume del solido generato dalla rotazione attorno all'asse delle $x$ della regione compresa fra la retta $y = x$ e la [parabola](../parabola/) $y = x^2.$

Le due curve si incontrano quando $x = x^2,$ cioè in $x = 0$ e $x = 1,$ e sull'intervallo $[0,1]$ vale $x^2 \leq x.$ La retta delimita quindi il raggio esterno con $f(x) = x$ e la parabola $g(x) = x^2$ quello interno.

![Img. 3](svg/the-washer-method-4.svg)

Adottando la formula della corona circolare otteniamo

$$V = \pi\int_0^1 \left[x^2 - (x^2)^2\right] \ dx = \pi\int_0^1 \left(x^2 - x^4\right) \ dx$$

Come abbiamo ricordato poco sopra, per la proprietà di linearità possiamo separare l'integrale nei suoi due addendi e risolverli separatamente. Otteniamo un integrale semplicissimo da risolvere i cui passaggi sono riepilogati di seguito.

$$
\begin{align}
V &= \pi\left[\frac{x^3}{3} - \frac{x^5}{5}\right]_0^1 \\[6pt]
  &= \pi\left(\frac{1}{3} - \frac{1}{5}\right) \\[6pt]
  &= \pi \cdot \frac{5-3}{15} \\[6pt]
  &= \frac{2\pi}{15}
\end{align}
$$

Il solido generato dalla rotazione della regione compresa fra $y = x$ e $y = x^2$ attorno all'asse delle $x$ ha pertanto proprio volume pari a $2\pi/15.$

## Esempio 2

Consideriamo adesso la stessa regione dell'esempio precedente, ma ruotiamola attorno alla retta $y = -1.$ Questa rotazione produce come ovvio un solido diverso da quello ottenuto nell'esempio 1, con una cavità che ora attraversa tutta la lunghezza. Osserviamo che le due curve si trovano al di sopra della retta $y = -1,$ quindi le distanze vanno misurate verso l'alto. Il raggio esterno è dato quindi dalla distanza fra l'asse e la curva più lontana, cioè la retta $y = x$:

$$f(x) - c = x - (-1) = x+1$$

Applicando lo stesso procedimento alla parabola, si ottiene il raggio interno:

$$g(x) - c = x^2 - (-1) = x^2+1$$

Il volume si è calcolato sostituendo i due raggi nella formula:

$$V = \pi\int_0^1 \left[(x+1)^2 - (x^2+1)^2\right] \ dx$$

Sviluppando i quadrati si ottiene senza difficoltà un [polinomio](../polynomials/) di quarto grado all'interno del segno di integrale:

$$
\begin{align}
(x+1)^2 - (x^2+1)^2 &= x^2 + 2x + 1 - x^4 - 2x^2 - 1 \\[6pt]
                    &= -x^4 - x^2 + 2x
\end{align}
$$

Questa è sempre una buona notizia perché l'integrale di un polinomio è la forma più semplice di integrale che vi possa capitare. Non abituatevi troppo però: nella realtà vi imbatterete quasi sempre in situazioni molto meno accomodanti che non vi faranno sorridere. Per i nostri scopi, tuttavia, approfittiamo della fortuna finché dura e otteniamo:

$$
\begin{align}
V &= \pi\int_0^1 \left(-x^4 - x^2 + 2x\right) \ dx \\[6pt]
  &= \pi\left[-\frac{x^5}{5} - \frac{x^3}{3} + x^2\right]_0^1 \\[6pt]
  &= \pi\left(-\frac{1}{5} - \frac{1}{3} + 1\right) \\[6pt]
  &= \pi \cdot \frac{-3-5+15}{15} \\[6pt]
  &= \frac{7\pi}{15}
\end{align}
$$

Notate una cosa interessante e non del tutto immediata. Il volume $7\pi/15$ è maggiore di quello dell'Esempio 1 pari invece a $2\pi/15$. Come è possibile se le curve considerate erano le stesse? Il motivo sta nella geometria elementare e, se non ci siete arrivati subito è del tutto naturale. La matematica fa sembrare complicate cose che a uno sguardo più attendo diventano ovvie. Allontanando la regione dall'asse di rotazione comporta che i suoi punti descrivano circonferenze di raggio maggiore e generano quinti un volume maggiore.


## Esempio 3

Facciamo un'ultimo esempio di rito, considerando una sfera di raggio $R$ da cui si ricava un anello praticando un foro cilindrico di raggio $a$ lungo un certo diametro, con $0 < a < R.$ Proviamo a calcolare il volume del solido che rimane.

La nostra sfera è il solido generato dalla rotazione di una semicirconferenza $y = \sqrt{R^2-x^2},$ mentre il foro è generato dalla rotazione della retta orizzontale $y = a.$ Analogamente ai casi precedenti, il solido residuo è quindi generato dalla regione compresa fra le due curve, con raggio esterno $f(x) = \sqrt{R^2-x^2}$ e raggio interno $g(x) = a.$

Gli estremi di integrazione sono le ascisse in cui le due curve si incontrano, quindi, nel nostro caso $x = \pm\sqrt{R^2-a^2}$. Poniamo $c = \sqrt{R^2-a^2},$ e otteniamo:

$$V = \pi\int_{-c}^{c} \left[(R^2-x^2) - a^2\right] \ dx$$

Poiché $R^2 - a^2 = c^2,$ possiamo riscrivere il tutto in funzione di $c$:

$$V = \pi\int_{-c}^{c} \left(c^2 - x^2\right) \ dx$$

Per una fortunosa casualità la funzione dentro il segno d'integrazione è pari (simmetrica rispetto all'asse $y$), quindi l'integrale sull'intervallo $[-c,c]$ è esattamente doppio dell'integrale su $[0,c]$ ed è facilmente calcolabile come:

$$
\begin{align}
V &= 2\pi\int_{0}^{c} \left(c^2 - x^2\right) \ dx \\[6pt]
  &= 2\pi\left[c^2x - \frac{x^3}{3}\right]_0^{c} \\[6pt]
  &= 2\pi\left(c^3 - \frac{c^3}{3}\right) \\[6pt]
  &= \frac{4\pi c^3}{3}
\end{align}
$$

Sostituendo a $c$ il valore originale, il volume che si ottiene è:

$$V = \frac{4\pi}{3}\left(R^2-a^2\right)^{3/2}$$

Il risultato si può anche riscrivere in funzione dell'altezza $h$ dell'anello residuo, ossia della distanza tra le due circonferenze che delimitano le aperture del foro. Poiché $h = 2c,$ sostituendo $c = h/2$ si ottiene:

$$V = \frac{4\pi}{3}\left(\frac{h}{2}\right)^3 = \frac{\pi h^3}{6}$$

Come si può constatare il volume dell'anello dipende esclusivamente dalla sua altezza, e non dal raggio della sfera di partenza e pertanto due anelli della stessa altezza hanno lo stesso volume anche se ricavati da sfere di dimensioni molto diverse.

## Alcune considerazioni finali

Nella nostra trattazione abbiamo considerato esclusivamente la condizione $g(x) \leq f(x)$ che deve essere soddisfatta su tutto l'intervallo $[a,b]$. Tuttavia nei casi pratici si possono riscontrare situazioni meno accomodanti. Se le due curve si intersecano in un punto, bisogna ricordarsi di suddividere l'intervallo in due sottointervalli $[a,c]$ e $[c,b]$ scrivendo un integrale per ciascun tratto, con lo stesso criterio usato per il [calcolo delle aree](../finding-areas-by-integration/).

La scelta poi del procedimento per determinare il volume del solido di rotazione dipende in maniera principale dalla posizione dell'asse rispetto alla regione e dalla variabile con cui la regione si descrive. Quando l'asse di rotazione appartiene al bordo della regione, la rotazione produce un solido pieno e in tal caso si usa il [metodo dei dischi](../the-disc-method/).

Quando la regione ruota attorno a un asse perpendicolare alla variabile in cui è naturalmente descritta, la formula delle corone richiede di invertire le funzioni che delimitano la regione.

Quando, infine, le sezioni perpendicolari all'asse non sono corone circolari, la formula non si applica. In tal caso bisogna ricorrere al calcolo per sezioni, che richiede solo la conoscenza dell'area $A(x)$ di ciascuna sezione.

