---
title: Area of a Surface of Revolution
source: https://algebrica.org/surface-area-of-revolution/
license: CC BY-NC 4.0
tags:
  - arc-length
  - cone-frustum
  - definite-integral
  - integral-applications
  - parametric-curves
  - solids-of-revolution
  - surface-area
  - surfaces-of-revolution
---
## L'area laterale di un tronco di cono

In questa voce vedremo come si calcola l'area di una superficie generata da un arco di curva che ruota attorno a una retta, ricorrendo all'integrale definito. Com'è stato ripetuto più volte nelle varie voci sull'argomento, gli integrali hanno un legame molto stretto con la geometria e non sono soltanto meri strumenti analitici. Prima di lanciarci nella spiegazione, è però opportuno fare un piccolo passo indietro e richiamare qualche concetto di geometria elementare.

Per questo partiremo da un cono circolare retto (ovvero un cono con il proprio asse perpendicolare alla base) con apotema $\ell$. Ricordiamo che l'apotema è la lunghezza del segmento inclinato che unisce il vertice con un punto della circonferenza di base ed è ricavato dalla formula:

$$\ell = \sqrt{h^2 + r^2} \tag{1}$$ 
Questa espressione dovrebbe esservi molto familiare: $h$ è l'altezza, $r$ è il raggio di base del cono. È nient'altro che il teorema di Pitagora applicato al cono, dove l'apotema rappresenta l'ipotenusa del triangolo rettangolo mentre $h$ e $r$ i suoi cateti. Un cono come quello appena descritto si sviluppa nel piano in un settore circolare di raggio $\ell$ il cui arco ha la lunghezza $2\pi r,$ pari alla circonferenza di base. Poiché l'area di un settore circolare è metà del prodotto fra il raggio e la lunghezza dell'arco, l'area laterale del cono può essere scritta come:

$$S=\pi r\ell \tag{2}$$

Consideriamo adesso un tronco di cono di raggi $r_1$ e $r_2,$ con $r_1<r_2,$ e apotema $\ell.$ Indichiamo con $L_1$ l'apotema del cono di raggio $r_1$ e con $L_2$ quello del cono di raggio $r_2.$ I due coni sono simili perché hanno lo stesso vertice e basi parallele, mentre i loro apotemi soddisfano $L_2-L_1=\ell.$ Possiamo quindi scrivere la seguente relazione:

$$\frac{r_1}{L_1}=\frac{r_2}{L_2}$$

Da questa proporzione e dalla relazione fra i tre apotemi si ricavano le seguenti lunghezze:

$$L_1=\frac{r_1\ell}{r_2-r_1} \qquad L_2=\frac{r_2\ell}{r_2-r_1}$$

L'area laterale del tronco di cono è data dalla differenza fra le aree laterali dei due coni, e la formula $(2)$ può essere riscritta come:

$$
\begin{align}
S &= \pi r_2L_2-\pi r_1L_1 \\[6pt]
  &= \frac{\pi\ell r_2^2}{r_2-r_1}-\frac{\pi\ell r_1^2}{r_2-r_1} \\[6pt]
  &= \frac{\pi\ell(r_2^2-r_1^2)}{r_2-r_1} \\[12pt]
  &= \pi(r_1+r_2)\ell
\end{align}
$$

Introduciamo adesso il raggio medio $\bar r=(r_1+r_2)/2$ in modo da scrivere la formula in modo più compatto:

$$S=2\pi\bar r\ell \tag{3}$$

Notate che se i due raggi coincidono il tronco degenera nel cilindro e l'area diventa $2\pi r\ell,$ mentre se uno dei due si annulla si ritrova l'area laterale del cono.

## Dalla somma all'integrale

Dopo questa noiosa introduzione geometrica, passiamo finalmente al risvolto sugli integrali. Consideriamo $f$ una funzione non negativa e di classe $C^1$ (ovvero, derivabile e con derivata $f'$ continua) sull'intervallo chiuso $[a,b],$ e sia $\Sigma$ la superficie generata dalla rotazione completa del suo grafico attorno all'asse delle $x.$ Consideriamo una [partizione](../riemann-integrability-criteria/) dell'intervallo:

$$a=x_0 \lt x_1 \lt \dots \lt x_n=b$$

Adesso, nel sottointervallo $[x_{k-1},x_k]$ sostituiamo l'arco di curva con la corda che ne unisce gli estremi. Ruotando quest'ultima si genera un tronco di cono i cui raggi sono le ordinate degli estremi, mentre l'apotema è la lunghezza della corda stessa. Ricordando la formula $(1)$ otteniamo:

$$\ell_k=\sqrt{(\Delta x_k)^2+\big(f(x_k)-f(x_{k-1})\big)^2}$$

Per il [teorema di Lagrange](../lagrange-theorem/) esiste un punto $\xi_k$ interno al sottointervallo per il quale la differenza delle ordinate vale $f'(\xi_k)\Delta x_k.$ Raccogliendo $(\Delta x_k)^2$ sotto il radicale, la formula diventa:

$$\ell_k=\sqrt{1+\big[f'(\xi_k)\big]^2} \ \Delta x_k$$

A questo punto, sommando i contributi dei singoli tronchi secondo la formula $(3)$ si ottiene l'area della superficie che è data approssimativamente dalla seguente sommatoria:

$$\Sigma_n=\pi\sum_{k=1}^{n}\big(f(x_{k-1})+f(x_k)\big)\sqrt{1+\big[f'(\xi_k)\big]^2} \ \Delta x_k \tag{4}$$

Attenzione! L'espressione $(4)$ non è una somma di Riemann, perché in ciascun addendo compaiono tre punti distinti dello stesso sottointervallo: i due estremi nelle ordinate e il punto individuato dal teorema di Lagrange nella derivata. Il passaggio al limite richiede un po' di lavorio in più che vedremo tra un istante.

- - -

Lo dico subito: i seguenti passaggi possono risultare all'inizio poco immediati, ma vi assicuro che a una seconda lettura risulteranno decisamente più chiari. Quindi non abbandonate la lotta prima di vincerla e tenete duro ancora per un po'. Quando vi sentirete sfiniti sarà il momento in cui vi risulterà tutto ovvio. Con un po' di astrazione (o meglio perché qualcuno lo ha già fatto prima di noi) poniamo: 

$$M=\max_{[a,b]}\sqrt{1+[f'(x)]^2}$$

Questo punto di massimo sappiamo esistere perché $f'$ è continua su un intervallo chiuso e limitato. Per ogni indice $k$ adesso scriviamo la somma delle due ordinate isolando il valore nel punto di Lagrange:

$$f(x_{k-1})+f(x_k)=2f(\xi_k)+\eta_k$$ 
$$\eta_k=\big(f(x_{k-1})-f(\xi_k)\big)+\big(f(x_k)-f(\xi_k)\big)$$

Poiché $f$ è continua su un intervallo compatto è anche [uniformemente continua](../uniform-continuity/). Posto $\delta=\max_{1\leq k\leq n}\Delta x_k,$ indichiamo con $\omega(\delta)$ il suo modulo di continuità. I punti $x_{k-1},$ $x_k$ e $\xi_k$ distano tra loro al più $\delta,$ quindi vale $|\eta_k|\leq2\omega(\delta).$ La differenza fra $\Sigma_n$ e la somma costruita con il punto $\xi_k$ può essere rappresentata dalla seguente relazione:

$$\left|\Sigma_n-2\pi\sum_{k=1}^{n}f(\xi_k)\sqrt{1+\big[f'(\xi_k)\big]^2} \ \Delta x_k\right|\leq2\pi M\omega(\delta)(b-a)$$

Facendo tendere a zero la maglia $\delta$ della partizione, la continuità uniforme garantisce che $\omega(\delta)$ tenda a zero, quindi il secondo membro dell'espressione si annulla. La somma rimasta è adesso una somma di Riemann della funzione continua $2\pi f\sqrt{1+(f')^2}$ relativa ai punti $\xi_k,$ e come sappiamo dai criteri di integrabilità di Riemann converge all'integrale della stessa funzione. Possiamo scrivere quindi la superficie come:

$$S=2\pi\int_a^b f(x)\sqrt{1+\big[f'(x)\big]^2} \ dx \tag{5}$$

Per le superfici regolari esiste anche una definizione parametrica dell'area. Nel presente caso essa coincide con il limite appena ottenuto, che assumiamo come definizione dell'area di $\Sigma.$

> Si noti che se $f$ cambia segno, la formula $(5)$ resta valida sostituendo $f$ con $|f|,$ perché il raggio di ciascun tronco è la distanza fra la curva e l'asse. Solo una precisazione relativa al [metodo dei dischi](../the-disc-method/): in quel caso il raggio compare al quadrato e il valore assoluto è quindi superfluo.

## L'elemento di superficie

La formula $(5)$ è il prodotto di due fattori: la lunghezza $ds=\sqrt{1+[f'(x)]^2} \ dx$ introdotta per la [lunghezza d'arco](../arc-length-of-a-curve/) e la circonferenza descritta dal punto della curva mentre ruota. Indicando con $r$ la distanza del punto dall'asse di rotazione, definiamo l'elemento di superficie come:

$$dS=2\pi r \ ds \tag{6}$$

Ogni variante della formula si ottiene scegliendo $r$ e $ds$ secondo la configurazione del problema, senza rifare ogni volta la costruzione daccapo e questo è inevitabilmente molto utile. Per una sintesi delle casistiche tenete conto della seguente tabella:

[class="table-1"]

|                                                   |                                                                             |
| ------------------------------------------------- | --------------------------------------------------------------------------- |
| Grafico di $f$ attorno all'asse $x$               | $$2\pi\int_a^b f(x)\sqrt{1+\big[f'(x)\big]^2} \ dx$$                        |
| Grafico di $f$ attorno all'asse $y,$ con $a\geq0$ | $$2\pi\int_a^b x\sqrt{1+\big[f'(x)\big]^2} \ dx$$                           |
| Grafico di $f$ attorno alla retta $y=c$           | $$2\pi\int_a^b\lvert f(x)-c\rvert\sqrt{1+\big[f'(x)\big]^2} \ dx$$                        |
| Curva parametrica attorno all'asse $x$            | $$2\pi\int_{t_0}^{t_1}\lvert y(t)\rvert\sqrt{\big[x'(t)\big]^2+\big[y'(t)\big]^2} \ dt$$ |

[/class]

Nella seconda riga il raggio è l'ascissa del punto e la condizione $a\geq0$ impedisce alla curva di attraversare l'asse di rotazione. L'ultima riga invece usa l'elemento di lunghezza in forma parametrica e copre anche le curve che non sono grafici di funzioni. Se la rotazione ricopre più volte la stessa porzione di superficie, l'integrale ne conta l'area con la stessa molteplicità.

## Esempio 1

Calcoliamo l'area della sfera di raggio $r$ come superficie generata dalla rotazione della semicirconferenza $f(x)=\sqrt{r^2-x^2}$ attorno all'asse delle $x.$ La funzione non è di classe $C^1$ agli estremi, quindi applichiamo la formula $(5)$ su $[-r+\varepsilon,r-\varepsilon]$ e passiamo al limite per $\varepsilon\to0.$ Per $-r<x<r$ la derivata della funzione è pari a:

$$f'(x)=-\frac{x}{\sqrt{r^2-x^2}}$$

Facendo qualche sostituzione algebrica otteniamo:

$$1+\big[f'(x)\big]^2=1+\frac{x^2}{r^2-x^2}=\frac{r^2}{r^2-x^2}$$

Il fattore $\sqrt{r^2-x^2}$ dell'ordinata cancella quello a denominatore, e il prodotto che compare nella formula $(5)$ si riduce a una costante:

$$f(x)\sqrt{1+\big[f'(x)\big]^2}=\sqrt{r^2-x^2}\cdot\frac{r}{\sqrt{r^2-x^2}}=r$$

Il prodotto ammette l'estensione continua uguale a $r$ anche agli estremi, quindi l'integrale improprio è:

$$S=2\pi\int_{-r}^{r}r \ dx=4\pi r^2$$

La sfera di raggio $r$ ha quindi area $4\pi r^2$ come sappiamo dalle nozioni di geometria elementare che ci portiamo appresso dalle scuole superiori. Notate come l'area di una zona sferica dipende solo dalla distanza fra i due piani paralleli che la delimitano, e non dalla loro posizione rispetto al centro. Questo significa che una zona sferica e la porzione di cilindro circoscritto delimitata dagli stessi piani hanno la medesima area.

## Esempio 2

Consideriamo adesso la funzione $f(x)=\sqrt{x}$ sull'intervallo $[0,4]$ e ruotiamone il grafico attorno all'asse delle $x,$ ottenendo il paraboloide di cui il [metodo dei dischi](../the-disc-method/) fornisce il volume. La derivata e il radicando sono:

$$f'(x)=\frac{1}{2\sqrt{x}}$$
$$1+\big[f'(x)\big]^2=1+\frac{1}{4x}=\frac{4x+1}{4x}$$

Il fattore $\sqrt{x}$ dell'ordinata cancella il denominatore del radicale, e l'integranda si riduce alla radice quadrata di una funzione lineare:

$$f(x)\sqrt{1+\big[f'(x)\big]^2}=\sqrt{x}\cdot\frac{\sqrt{4x+1}}{2\sqrt{x}}=\sqrt{x+\frac{1}{4}}$$

Risolvendo l'integrale, anche questo immediato, otteniamo:

$$
\begin{align}
S &= 2\pi\int_0^4\sqrt{x+\frac{1}{4}} \ dx \\[6pt]
  &= 2\pi\cdot\frac{2}{3}\left[\left(x+\frac{1}{4}\right)^{3/2}\right]_0^4 \\[6pt]
  &= \frac{4\pi}{3}\left(\left(\frac{17}{4}\right)^{3/2}-\left(\frac{1}{4}\right)^{3/2}\right) \\[6pt]
  &= \frac{4\pi}{3}\cdot\frac{17\sqrt{17}-1}{8} \\[6pt]
  &= \frac{\pi}{6}\big(17\sqrt{17}-1\big)
\end{align}
$$

L'area della superficie vale $\pi(17\sqrt{17}-1)/6.$ La derivata di $f$ non è limitata in un intorno destro dell'origine, quindi $f$ non è di classe $C^1$ sull'intervallo chiuso, ma l'integranda definita su $(0,4]$ ammette un'estensione continua a $[0,4]$ perché il fattore $f(x)$ si annulla nell'origine con la stessa velocità con cui il radicale diverge. Il valore dell'estensione nell'origine è $1/2.$

## Esempio 3

Guardiamo adesso un arco di [cicloide](../arc-length-of-a-curve/) che è descritto dalle equazioni parametriche seguenti, con $t$ che varia in $[0,2\pi]$ e $r$ raggio della circonferenza:

$$x(t)=r(t-\sin t)$$
$$y(t)=r(1-\cos t)$$

Ruotando l'arco attorno all'asse delle $x$ si riutilizza l'elemento di lunghezza già ottenuto nel calcolo della lunghezza dell'arco:

$$\sqrt{\big[x'(t)\big]^2+\big[y'(t)\big]^2}=2r\sin\frac{t}{2}$$

L'ordinata si riscrive con la formula di bisezione come $y(t)=2r\sin^2(t/2),$ e l'integranda contiene allora solo potenze del seno di $t/2$:

$$
\begin{align}
S &= 2\pi\int_0^{2\pi}2r\sin^2\frac{t}{2}\cdot2r\sin\frac{t}{2} \ dt \\[6pt]
  &= 8\pi r^2\int_0^{2\pi}\sin^3\frac{t}{2} \ dt \\[6pt]
  &= 16\pi r^2\int_0^{\pi}\sin^3u \ du
\end{align}
$$

L'ultimo passaggio è la [sostituzione](../integration-by-substitution/) $u=t/2,$ che porta $dt$ in $2 \ du$ e dimezza gli estremi. Ricordiamo che l'integrale di una [potenza dispari del seno](../integral-of-trigonometric-functions/) si calcola isolando un fattore e usando l'identità fondamentale, e vale $4/3$:

$$S=16\pi r^2\cdot\frac{4}{3}=\frac{64}{3}\pi r^2$$

> L'area di una superficie curva non può essere definita in generale come il limite delle aree di poliedri inscritti. Anche quando il diametro delle facce tende a zero, il limite può dipendere dal modo in cui si costruiscono i poliedri, come mostra la lanterna di Schwarz per il cilindro. L'approssimazione mediante tronchi di cono evita questa ambiguità perché lega l'inclinazione di ciascun elemento alla corda corrispondente della curva generatrice.

## Alcune considerazioni finali

In chiusura riportiamo alcune considerazioni utili a fornire un orientamento utile sull'utilizzo di quanto appena illustrato.

+ La formula $(5)$ è stata ricavata con $f$ non negativa e di classe $C^1$ su $[a,b],$ ipotesi che rende continua l'integranda. Come mostrano i primi due esempi si tratta di una condizione sufficiente ma non necessaria. La formula resta valida, per esempio, se $f$ è continua su $[a,b],$ di classe $C^1$ fuori da un numero finito di punti e gli integrali impropri dell'integranda convergono.
+ Nella seconda riga della tabella la condizione $a\geq0$ consente di usare $x$ come raggio. Se il grafico attraversa l'asse delle $y,$ il raggio è $|x|$ e due punti distinti generano la stessa circonferenza solo quando hanno la stessa ordinata e ascisse opposte. Anche per una curva parametrica occorre verificare che la superficie non sia percorsa più volte.
+ Il metodo delle [sezioni parallele](../volumes-by-parallel-cross-sections/) restituisce il volume esatto, ma le pareti laterali dei cilindri approssimanti formano una superficie a gradini la cui area non converge in generale all'area di $\Sigma.$ Il volume di un solido di rotazione e l'area della sua superficie richiedono due costruzioni distinte.
+ Quando l'integrale in $(5)$ non ha primitiva elementare il valore si determina per [via numerica](../numerical-integration/).
