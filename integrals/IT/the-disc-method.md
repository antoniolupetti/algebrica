---
title: The Disc Method for Volumes of Revolution
source: https://algebrica.org/the-disc-method/
license: CC BY-NC 4.0
tags:
  - calculus
  - disc-method
  - integral-applications
  - solids-of-revolution
  - volume
---
## Solidi generati da una rotazione

Il metodo dei dischi serve a calcolare il volume dei cosiddetti solidi di rotazione, caratterizzati da una regione piana che ruota attorno a una retta fissa. Durante la rotazione ogni punto della regione descrive una [circonferenza](../circumference/) il cui piano è perpendicolare all'asse di rotazione e l'unione di tutte le circonferenze genera il solido.

Consideriamo $f$ una funzione [continua](../continuous-functions/) su $[a, b]$ con $f(x) \geq 0,$ e sia $R$ la regione delimitata superiormente dal grafico $y = f(x),$ inferiormente dall'asse delle $x$ e lateralmente dalle rette $x = a$ e $x = b.$ Nel caso in questione l'asse delle $x$ rappresenta l'asse di rotazione.

![IMG. 1](svg/the-disk-method-1.svg)

Se ruotiamo la regione $R$ attorno all'asse delle $x$ otteniamo un solido che chiamiamo $S$ le cui sezioni perpendicolari all'asse sono dischi circolari.

![IMG. 2](svg/the-disk-method-2.svg)


Abbiamo ottenuto un solido che ricorda un cilindro che si allarga man mano che il valore di $x$ decresce. Come possiamo calcolarne il volume? Per prima cosa richiamiamo la formula del volume di un cilindro circolare retto di raggio $r$ e altezza $h$ che è data da:

$$V = \pi r^2h \tag{1}$$

Suddividiamo adesso l'intervallo $[a, b]$ in $n$ sottointervalli, ciascuno di ampiezza $\Delta x = (b - a)/n,$ e tale che:

$$a = x_0 < x_1 < \dots < x_n = b.$$

Un generico sottointervallo $[x_{k-1}, x_k]$ individua in $S$ una fetta perpendicolare all'asse delle $x.$ Scegliamo in questo sottointervallo un punto $x_k^{*}$ in cui misurare l'altezza del grafico (escludendo gli estremi). A questo punto la fetta si approssima con un cilindro di spessore $\Delta x$ la cui base circolare ha raggio pari all'altezza del grafico nel punto $x_k^{*},$ ossia $f(x_k^{*}).$ Applichiamo adesso a questo disco la formula $(1)$ del volume del cilindro ottenendo:

$$\Delta V_k = \pi \big(f(x_k^{*})\big)^2 \Delta x$$

Se estendiamo questo procedimento alla sommatoria dei contributi di tutte le fette che possiamo idealmente individuare nell'intervallo, riusciamo ad approssimare il volume di $S$ dato da:

$$V \approx \sum_{k=1}^{n} \pi \big(f(x_k^{*})\big)^2 \Delta x \tag{2}$$

Il membro di destra è una [somma di Riemann](../riemann-integrability-criteria/) della funzione $\pi(f(x))^2$ su $[a, b].$ Quando nella suddivisione $\Delta x$ tende a $0,$ i dischi diventano sempre più sottili seguendo in maniera più accurata il profilo del solido, perciò la somma converge all'[integrale definito](../definite-integrals/). Possiamo quindi riscrivere il volume del solido di rotazione generato ruotando $R$ attorno all'asse delle $x$ con il seguente integrale calcolato agli estremi dell'intervallo:

$$V = \int_a^b \pi \big(f(x)\big)^2 \ dx \tag{3}$$

Il raggio del disco in corrispondenza di $x$ è il valore $f(x)$ e il suo quadrato, moltiplicato per $\pi$ esprime l'area $\pi r^2$ di ciascuna base circolare.

- - -

La stessa costruzione si può applicare anche quando l'asse di rotazione è l'asse delle $y.$ Se una regione è compresa tra il grafico $x = g(y)$ e l'asse delle $y,$ per $c \leq y \leq d$ con $g(y) \geq 0,$ la sua rotazione attorno all'asse delle $y$ produce dischi perpendicolari a tale asse, e la $(3)$ si può riscrivere come:

$$V = \int_c^d \pi \big(g(y)\big)^2 \ dy \tag{4}$$

Come potete osservare il ruolo delle variabili è invertito, mentre il principio di costruzione del volume rimane lo stesso.

## Esempio

Facciamo un esempio per calcolare il volume del solido generato dalla rotazione attorno all'asse delle $x$ della regione $R$ compresa tra la curva $y = \sqrt{x}$ e l'asse delle $x,$ nell'intervallo $0 \leq x \leq 4.$ Il solido ottenuto è un [paraboloide di rotazione](../surface-area-of-revolution/) e ha la forma di una sorta di ciotola dalla superficie liscia.

![IMG. 3](svg/the-disk-method-3.svg)

In corrispondenza di $x,$ la sezione perpendicolare all'asse è un disco di raggio $f(x) = \sqrt{x},$ quindi la sua area è $\pi(\sqrt{x})^2 = \pi x.$ Poiché l'asse di rotazione coincide con l'asse $x$, possiamo applicare direttamente il metodo dei dischi per calcolare il volume con la $(3)$ ottenendo:

$$V = \int_0^4 \pi \big(\sqrt{x}\big)^2 \ dx$$

Svolgendo i calcoli otteniamo:

$$V = \int_0^4 \pi x \ dx = \pi \int_0^4 x \ dx$$

Quindi con il [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/) calcoliamo il volume valutando l'integrale agli estremi del nostro intervallo:

$$V = \pi \left[ \frac{x^2}{2} \right]_0^4 = \pi \left( \frac{16}{2} - \frac{0}{2} \right) = 8\pi$$

Pertanto, il paraboloide ottenuto dalla rotazione di $R$ ha volume pari a $8\pi$.


## Quando si applica il metodo

Quali sono le condizioni di applicabilità per cui possiamo ricorrere alla $(3)$ e alla $(4)$ per calcolare il volume di un solido di rotazione? Nella costruzione precedente abbiamo usato due ipotesi principali.

La prima è la continuità di $f$ su $[a, b],$ che garantisce che $f$ sia [integrabile](../riemann-integrability-criteria/) e che lo sia anche il suo quadrato, perciò le somme di Riemann convergono all'integrale che esprime il volume. La continuità è una condizione sufficiente, ma non necessaria. Il metodo si applica anche, per esempio, a funzioni limitate con un numero finito di discontinuità.

La seconda ipotesi riguarda la posizione della regione rispetto all'asse. Il metodo dei dischi si applica quando ogni sezione del solido perpendicolare all'asse di rotazione è un disco pieno, ma se la regione è separata dall'asse, le sezioni sono corone circolari e in questi casi si può usare il metodo delle corone circolari. In alternativa si può ricorrere al metodo dei gusci cilindrici.

- - -

Da notare che la condizione $f(x) \geq 0$ può essere rimossa quando la regione da ruotare è compresa tra il grafico e l'asse delle $x.$ Se $f(x) < 0,$ il segmento che congiunge l'asse al grafico si trova sotto l'asse, ma ruotando genera comunque un disco. Il suo raggio, infatti, è la lunghezza del segmento, data dal valore assoluto di $f(x).$ 

Per esempio, consideriamo un punto del grafico con ordinata $2$ e uno con ordinata $-2.$ In ciascun caso, il segmento che congiunge il punto all'asse genera per rotazione un disco di raggio $2$ e area $4\pi.$ Pertanto il raggio del disco è sempre positivo.

Quindi, in generale, l'area della sezione è $\pi|f(x)|^2 = \pi(f(x))^2,$ perciò la formula del volume rimane valida anche quando $f$ assume valori negativi o cambia segno nell'intervallo.

Lo stesso ragionamento si applica alla rotazione attorno a una qualsiasi retta parallela a un asse coordinato. Se la regione compresa tra il grafico $y = f(x)$ e la retta orizzontale $y = c,$ per $a \leq x \leq b$ con $f(x) \geq c,$ ruota attorno a tale retta, il raggio in corrispondenza di $x$ è la distanza $f(x) - c,$ e il volume diventa:

$$\int_a^b \pi\big(f(x) - c\big)^2 \ dx$$

La struttura della formula rimane sostanzialmente identica alla $(3)$ e alla $(4)$ con il raggio però misurato a partire dall'effettivo asse di rotazione.