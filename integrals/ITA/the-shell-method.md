---
title: The Shell Method for Volumes of Revolution
source: https://algebrica.org/the-shell-method/
license: CC BY-NC 4.0
tags:
  - calculus
  - cylindrical-shells
  - definite-integral
  - disc-method
  - integral-applications
  - shell-method
  - solids-of-revolution
  - volume
  - washer-method
---
## C'è sempre un modo

Andrew Wiles è un matematico britannico noto per aver dimostrato l'ultimo teorema di Fermat. In termini molto semplici il teorema riguarda le soluzioni della seguente equazione:

$$x^n + y^n = z^n \tag{1}$$

A prima vista sembra innocua, ma ricordate che in matematica vale il principio secondo cui la complessità di un'espressione è inversamente proporzionale alla semplicità con cui essa viene rappresentata ($E=mc^2$ vi dice qualcosa?).

Fermat è vissuto nel diciassettesimo secolo e a quel tempo l'equazione $(1)$ era largamente nota. Già nel quinto secolo avanti Cristo, Pitagora la utilizzava con una cerca disinvoltura nel suo celebre teorema: la somma dei quadrati costruiti sui cateti di un triangolo rettangolo è pari all'area del quadrato costruito sull'ipotenusa. 

Fin qui, niente di nuovo. Il problema è un altro. 

Il teorema asserisce che quando $n>2$ non esistono soluzioni intere positive dell'equazione, ma esistono solo soluzioni reali che si possono determinare abbastanza agevolmente. Si dice che Fermat avesse appuntato sul margine di un libro di aver trovato la soluzione al suo teorema, ma che lo spazio fosse troppo stretto per contenerla. Non so se la storia abbia un qualche fondamento storico, ma l'ho trovata curiosa, perciò l'ho riportata lasciando l'onere della verifica agli storiografi. Ad ogni modo, quella dimostrazione nessuno l'ha mai trovata e il problema è rimasto aperto fino agli anni Novanta.

Pare che Wiles venne a conoscenza del teorema di Fermat negli anni Sessanta e ne rimase totalmente affascinato da dedicarvi una gran parte della propria vita professionale. All'epoca aveva solo dieci anni, un'età nella quale la maggior parte degli ragazzini ancora fatica con la tabellina del nove. Confesso che, mentre mi documentavo su questo episodio, ho accusato un lieve crollo dell'autostima. Posso però assicurarvi che le fonti che lo attestano sono abbastanza numerose da rendere superflua qualsiasi verifica da parte dei più increduli.

Per farla breve, Wiles provò a dimostrare il teorema da ragazzo, ma non vi riuscì. Più avanti spese anni ritentando, ma fallì. Nel 1993 annunciò  di averlo risolto, ma uno dei revisori, Nicholas Katz, spense il suo entusiasmo mostrando che il metodo utilizzato non funzionava. Due anni più tardi Wiles ne venne finalmente a capo, cambiando metodo e fornendo così il supporto necessario alla dimostrazione del teorema che tanto lo aveva occupato.

Tutto questo per dire che, in matematica, quasi sempre esiste un metodo che funziona, tra decine di altri che non funzionano. Il punto è scoprire quale sia. Per nostra fortuna, nella maggior parte dei problemi che si incontrano in ambito scolastico non dobbiamo inventarci nulla, poiché il grosso del lavoro è già stato fatto da altri. Dobbiamo tuttavia essere sufficientemente attrezzati per cogliere il metodo più efficace in termini computazionali e di risoluzione.

- - -

Per determinare il volume di un solido di rotazione abbiamo precedentemente introdotto [the disc method](../the-disc-method) e [the washer method](../the-washer-method) che offrono due semplici procedure di calcolo attraverso il ricorso ad integrali definiti in un certo intervallo.

La questione, però, si complica quando l'asse di rotazione non è quello delle ascisse ma quello delle ordinate. In questo caso, infatti, il raggio delle sezioni perpendicolari all'asse $y$ è misurato orizzontalmente e per questa ragione dobbiamo essere in grado di esprimere $x$ in funzione di $y.$ In termini analitici, dobbiamo invertire le funzioni $f$ e $g$ che delimitano la regione di piano $R$ e questa operazione, il più delle volte, è tutt'altro che indolore.

Se consideriamo, ad esempio, la regione compresa fra l'asse delle $x$ e la curva $y=2x^2-x^3$ sull'intervallo $[0,2],$ per applicare il metodo delle corone dovremmo ricavare $x$ da un'equazione di terzo grado, cosa non proprio comodissima. Inoltre, siccome la curva non è iniettiva su $[0,2],$ l'inversa andrebbe costruita a pezzi, complicando ancora di più tutto il  quadro. Purtroppo, questa è una situazione abbastanza diffusa nella pratica, in quanto le funzioni non invertibili in forma elementare sono la regola e non l'eccezione.

Per aggirare del tutto il problema, bisogna cambiare il metodo con cui scomponiamo il solido. Invece di tagliarlo in tante fette perpendicolari all'asse di rotazione lo immaginiamo formato da tanti sottili gusci concentrici, uno dentro l'altro. In questo modo poiché una striscia verticale è descritta direttamente dalla variabile $x$, possiamo calcolare direttamente il volume senza riscrivere la funzione in termini di $y$.


## Il volume di un guscio cilindrico

Per uniformità, impostiamo il problema con la stessa notazione usata per le corone circolari. Siano $f$ e $g$ due funzioni continue su $[a,b],$ con $0 \leq a$ e $g(x) \leq f(x)$ per ogni $x$ dell'intervallo, e sia $R$ la regione di piano compresa fra i due grafici.

![IMG. 1](svg/the-shell-method-1.svg)


Chiamiamo guscio cilindrico il solido compreso fra due cilindri coassiali di uguale altezza $h$ e raggio $r_1<r_2.$ Il suo volume è la differenza fra i volumi dei due cilindri:

$$V = \pi r_2^2h - \pi r_1^2h = \pi h\left(r_2^2-r_1^2\right)$$

$r_2^2-r_1^2$ è un [prodotto notevole](../notable-products/) che si scompone in $(r_2+r_1)(r_2-r_1).$ Facendo qualche semplice operazione algebrica otteniamo:

$$
\begin{align}
V &= \pi h(r_2+r_1)(r_2-r_1) \\[6pt]
  &= 2\pi \cdot \frac{r_1+r_2}{2} \cdot h \cdot (r_2-r_1)
\end{align}
$$

 $(r_1+r_2)/2$ è il raggio medio del guscio, $h$ è la sua altezza, $r_2-r_1$ è il suo spessore. Il volume di un guscio cilindrico è quindi dato dalla seguente espressione:

$$V = 2\pi \cdot (\text{raggio medio}) \cdot (\text{altezza}) \cdot (\text{spessore})$$
![IMG. 2](svg/the-shell-method-2.svg)


Suddividiamo adesso l'intervallo $[a,b]$ in $n$ sottointervalli uguali di ampiezza $\Delta x=(b-a)/n,$ individuati dai punti:

$$a = x_0 < x_1 < \cdots < x_n = b$$

Sul generico sottointervallo $[x_{k-1},x_k]$ scegliamo come punto di riferimento il suo punto medio $x_k^{*},$ e consideriamo la striscia verticale $R_k$ della regione che sta sopra a quel sottointervallo. Se $\Delta x$ è piccola, la striscia si discosta poco dal rettangolo di base $\Delta x$ e altezza $f(x_k^{*})-g(x_k^{*}).$

Facendo ruotare quel rettangolo attorno all'asse delle ordinate otteniamo esattamente un guscio cilindrico di raggio interno $x_{k-1},$ raggio esterno $x_k$ e altezza $f(x_k^{*})-g(x_k^{*}).$ Qui la scelta del punto medio si rivela particolarmente comoda, perché il raggio medio del guscio è proprio:

$$\frac{x_{k-1}+x_k}{2} = x_k^{*}$$

Il volume del guscio si ottiene quindi sostituendo nella formula ricavata poco sopra il raggio medio $x_k^{*},$ l'altezza $f(x_k^{*})-g(x_k^{*})$ e lo spessore $\Delta x,$ da cui:

$$\Delta V_k = 2\pi x_k^{*}\left[f(x_k^{*})-g(x_k^{*})\right]\Delta x$$

Sommando i contributi di tutti i sottointervalli otteniamo un'approssimazione del volume del solido pari a:

$$V \approx \sum_{k=1}^{n} 2\pi x_k^{*}\left[f(x_k^{*})-g(x_k^{*})\right]\Delta x$$

Il membro di destra è una [somma di Riemann](../riemann-integrability-criteria/) della funzione $2\pi x[f(x)-g(x)],$ che è continua su $[a,b]$ perché prodotto e differenza di funzioni continue. La somma converge quindi all'[integrale definito](../definite-integrals/) quando $\Delta x \to 0,$ e il volume del solido diventa:

$$V = 2\pi\int_a^b x\left[f(x)-g(x)\right] \ dx \tag{2}$$


Quando la regione è delimitata inferiormente dall'asse delle $x$, cioè quando $g$ è identicamente nulla, la formula si riduce a:

$$V = 2\pi\int_a^b xf(x) \ dx$$

## Rotazioni attorno ad altri assi

Come per le corone circolari, la costruzione non richiede che l'asse di rotazione sia un asse coordinato. Nella formula compaiono soltanto il raggio e l'altezza della striscia, quindi basta misurare il raggio a partire dall'asse effettivo.

Se la rotazione avviene attorno alla retta verticale $x=c$ con $c \leq a,$ la regione sta tutta a destra dell'asse e il raggio della striscia è la differenza $x-c.$ Da questo si ricava che il volume è pari a:

$$V = 2\pi\int_a^b (x-c)\left[f(x)-g(x)\right] \ dx$$

Se invece $c \geq b,$ la regione sta tutta a sinistra dell'asse, le distanze si misurano nel verso opposto e il raggio diventa $c-x,$ quindi:

$$V = 2\pi\int_a^b (c-x)\left[f(x)-g(x)\right] \ dx$$

Quando la rotazione avviene attorno all'asse delle ascisse i ruoli delle due variabili si scambiano. La regione va descritta nella forma $q(y) \leq x \leq p(y)$ per $y \in [a,b],$ con $0 \leq a.$ Le strisce sono adesso orizzontali e il raggio di ciascuna è l'ordinata $y,$ da cui:

$$V = 2\pi\int_a^b y\left[p(y)-q(y)\right] \ dy$$

Se l'asse di rotazione interseca la regione, il solido generato dalla parte sinistra si sovrappone a quello generato dalla parte destra. In tal caso la somma dei volumi dei due pezzi conterebbe due volte la zona comune, il cui volume deve quindi essere sottratto.

## Esempio 1

Per analogia, replichiamo l'esempio già visto nella voce su the [washer method](../the-washer-method) e calcoliamo il volume del solido generato dalla rotazione attorno all'asse delle ordinate della regione compresa fra la retta $y=x$ e la [parabola](../parabola/) $y=x^2.$

Le due curve si incontrano quando $x=x^2,$ cioè in $x=0$ e $x=1,$ e sull'intervallo $[0,1]$ vale $x^2 \leq x.$ La retta delimita quindi la regione superiormente con $f(x)=x$ e la parabola inferiormente con $g(x)=x^2.$

![IMG. 4](svg/the-washer-method-4.svg)

La striscia verticale posta all'ascissa $x$ ha altezza $x-x^2$ e dista $x$ dall'asse di rotazione. Utilizzando la formula si ottiene:

$$
\begin{align}
V &= 2\pi\int_0^1 x\left(x-x^2\right) \ dx \\[6pt]
  &= 2\pi\int_0^1 \left(x^2-x^3\right) \ dx \\[6pt]
  &= 2\pi\left[\frac{x^3}{3}-\frac{x^4}{4}\right]_0^1 \\[6pt]
  &= 2\pi\left(\frac{1}{3}-\frac{1}{4}\right) \\[6pt]
  &= \frac{\pi}{6}
\end{align}
$$

Il solido ha quindi volume $\pi/6$. Lo stesso valore è stato ottenuto utilizzando il metodo delle corone circolari, come è ovvio che sia.

## Esempio 2

Riprendiamo adesso una regione un po' più ostica, quella compresa fra l'asse delle ascisse e la curva $y=2x^2-x^3,$ e facciamola ruotare attorno all'asse delle ordinate.

La curva si annulla quando $x^2(2-x)=0,$ cioè in $x=0$ e $x=2,$ e su $[0,2]$. Entrambe i fattori sono positivi, quindi la curva sta sopra l'asse. Quindi la nostra $f$ e la nostra $g$ sono rispettivamente $f(x)=2x^2-x^3$ e $g(x)=0.$

Applicando la $(2)$, il raggio $x$ si moltiplica per l'altezza della striscia e aument di un grado il polinomio:

$$
\begin{align}
V &= 2\pi\int_0^2 x\left(2x^2-x^3\right) \ dx \\[6pt]
  &= 2\pi\int_0^2 \left(2x^3-x^4\right) \ dx \\[6pt]
  &= 2\pi\left[\frac{x^4}{2}-\frac{x^5}{5}\right]_0^2 \\[6pt]
  &= 2\pi\left(8-\frac{32}{5}\right) \\[6pt]
  &= \frac{16\pi}{5}
\end{align}
$$

Notate quello che è successo, perché è il punto centrale del metodo. L'equazione di terzo grado che ci avrebbe costretti a cercare un'inversa è rimasta tale e quale, moltiplicata per $x,$ e l'integrale che ne è uscito è quello di un polinomio di quarto grado, molto semplice da risolvere. Il metodo dei gusci, quindi, non ha risolto un problema difficile, ha semplicemente evitato di crearlo.

## Esempio 3

Consideriamo di nuovo la regione fra $y=x$ e $y=x^2$ su $[0,1]$ dell'esempio 1, ma ruotiamola attorno alla retta verticale $x=2.$ La regione sta tutta a sinistra dell'asse, dato che $1 \leq 2,$ quindi il raggio della striscia si misura da destra verso sinistra e vale $2-x.$ L'altezza invece non cambia, perché dipende solo dalle due curve e resta $x-x^2.$ Il volume è quindi:

$$V = 2\pi\int_0^1 (2-x)\left(x-x^2\right) \ dx$$

Svolgendo i calcoli si ottiene:

$$
\begin{align}
V &= 2\pi\int_0^1 \left(x^3-3x^2+2x\right) \ dx \\[6pt]
  &= 2\pi\left[\frac{x^4}{4}-x^3+x^2\right]_0^1 \\[6pt]
  &= 2\pi\left(\frac{1}{4}-1+1\right) \\[6pt]
  &= \frac{\pi}{2}
\end{align}
$$

Il volume ottenuto, pari a $\pi/2,$ è maggiore del $\pi/6$ dell'Esempio 1, e il motivo è lo stesso incontrato con l'omologo esempio delle corone circolari. Allontanando la regione dall'asse di rotazione, ogni suo punto descrive una circonferenza di raggio maggiore determina quindi un volume maggiore.

## Come scegliere il metodo

A questo punto siamo arrivati a contemplare ben tre metodi diversi per la stessa famiglia di problemi, ciascuno con delle proprie caratteristiche, è ragionevole chiedersi quale usare. Per nostra fortuna il criterio è piuttosto semplice.

I dischi e le corone tagliano la regione perpendicolarmente all'asse di rotazione, quindi la variabile di integrazione è quella misurata parallelamente all'asse. I gusci tagliano invece la regione parallelamente all'asse, quindi la variabile di integrazione è quella misurata perpendicolarmente all'asse. Schematizzando il tutto in termini pratici possiamo riassumere i seguenti punti:

+ Si usano i dischi o le corone in caso di una rotazione attorno all'asse delle ascisse e una regione descritta da $y=f(x)$ oppure con una rotazione attorno all'asse delle ordinate e regione descritta da $x=p(y)$ 
+ Con una rotazione attorno all'asse delle ordinate e una regione descritta da $y=f(x)$ si usano i gusci. Lo stesso vale per una rotazione attorno all'asse delle $x$ e una regione descritta da $x=p(y)$.

Tenete sempre a mente che, nella scelta di un metodo, si deve propendere verso quello che evita di invertire le funzioni.

- - -
-
Rimane infine un ultimo caso, quello in cui i gusci non sono comodissimi da ricavare ma indispensabili. Consideriamo la regione compresa fra l'asse delle $x$ e la curva $y=\sin(x^2)$ per $x \in [0,\sqrt{\pi}],$ fatta ruotare attorno all'asse delle ordinate. Applicando il metodo dei gusci il volume diventa:

$$V = 2\pi\int_0^{\sqrt{\pi}} x\sin(x^2) \ dx$$

Questo è un tipico integrale che si risolve per [sostituzione](../integration-by-substitution/), imponendo $u=x^2,$ da cui $du=2x \ dx$. L'integrale diventa;
$$\pi\int_0^{\pi}\sin(u) \ du$$

Il calcolo è immediato e vale $2\pi.$ In questo caso l'utilizzo del metodo dei gusci ha fatto comparire la variabile $x$ nella formula e tale fattore ha reso possibile la sostituzione. Se avessimo invece utilizzato il metodo delle corone circolari avremmo dovuto invertire $\sin(x^2)$ (che non ha inversa elementare), e saremmo rimasti impantanati nei calcoli senza venirne a capo.
