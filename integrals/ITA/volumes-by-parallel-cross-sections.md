---
title: Volumes by Parallel Cross Sections
source: https://algebrica.org/volumes-by-parallel-cross-sections/
license: CC BY-NC 4.0
tags:
  - cavalieri-principle
  - cross-sections
  - definite-integral
  - integral-applications
  - riemann-sum
  - solid-geometry
  - volume
---
## Il volume come somma di sezioni

Supponiamo di avere un solido molto semplice, come un cubo, un parallelepipedo o un cilindro. Calcolarne il volume è un prodotto elementare tra la sua area di base e l'altezza. Niente di più. Questa formula vale per qualunque solido ottenuto dalla traslazione di un poligono (o di un cerchio, nel caso di un cilindro) lungo una direzione perpendicolare al suo piano. È un po' come accumulare, una sopra l'altra, tante fette infinitesime della stessa figura, affinché lo spessore di ciascuna contribuisca a determinare l'altezza del solido e, di conseguenza, il suo volume. 

Come dicevo poc'anzi, determinare il volume di queste figure è un'operazione banale che si acquisisce fin dalla scuola primaria, poiché non richiede chissà quale livello di astrazione. Ma in genere, più le cose sono semplici e all'apparenza banali, più tendono a complicarsi in modo imprevisto a causa di variazioni che a prima vista paiono innocenti.

Prendete il caso di un solido di rivoluzione a raggio variabile. A dispetto del nome intimidatorio, è nient'altro che un cilindro il cui raggio varia lungo la perpendicolare alla sezione circolare che ne costituisce la base. Possiamo immaginarlo come una specie di clessidra o, nel caso più semplice, come un cono, quando il raggio di base diminuisce linearmente lungo la sua perpendicolare. Se avete mai armeggiato con un tornio, saprete cosa intendo. Chi studia ingegneria meccanica dovrebbe provarlo almeno una volta nella vita: è un'esperienza utile per toccare con mano la potenza dei processi rotazionali. Divagando più del necessario, è affascinante scoprire che, utilizzando lame utensili con un profilo specifico, è possibile ottenere cavità a sezione triangolare mediante rotazione. Pensateci un secondo: un triangolo a partire da una rotazione. Non vi pare un controsenso? Vi invito comunque a fidarvi, per non perderci in discussioni che esulano troppo dall'obiettivo di questa voce, e a rientrare in tema.

Per determinare il volume di un solido, come quelli di cui abbiamo appena parlato, non basta più il semplice prodotto, ma occorre ricorrere agli integrali. Quando abbiamo introdotto gli [integrali indefiniti](../indefinite-integrals/) e quelli [definiti](../definite-integrals/) li abbiamo descritti in sostanza come strumenti analitici, ma in realtà la loro connessione con la geometria è molto più stretta di quanto non si noti all'inizio del loro studio.
 
Consideriamo, ad esempio, un solido $S$ compreso fra due piani perpendicolari a una retta fissata, che assumiamo come asse delle $x,$ e supponiamo che i due piani incontrino tale asse nei punti di ascissa $a$ e $b,$ con $a<b.$ Per ogni $x$ appartenente all'intervallo $[a,b]$ il piano perpendicolare all'asse interseca il solido descrivendo una sezione piana $S$ la cui area viene indicata con $A(x).$

![IMG. 1](svg/volumes-by-parallel-cross-sections-1.svg)

Ora suddividiamo $[a,b]$ in $n$ sottointervalli di uguale ampiezza $\Delta x=(b-a)/n,$ Individuati dai seguenti punti.

$$a=x_0<x_1<\dots<x_n=b$$

Il piano di ascissa $x_{k-1}$ e quello di ascissa $x_k$ ritagliano da $S$ una fetta di spessore $\Delta x.$ Scegliamo adesso nel sottointervallo $[x_{k-1},x_k]$ un punto $x_k^{*}$ diverso dagli estremi. Come abbiamo detto nell'introduzione, se la sezione restasse immutata mentre $x$ percorre il sottointervallo, la fetta che abbiamo appena delimitato, descriverebbe un cilindro con la base data dalla sezione in $x_k^{*}$ e altezza $\Delta x,$ e il suo volume sarebbe il prodotto fra l'area di base e lo spessore:

$$\Delta V_k=A(x_k^{*})\Delta x$$

![IMG. 2](svg/volumes-by-parallel-cross-sections-2.svg)

Sommando i contributi di tutte le fette si ottiene un valore approssimato del volume di $S$ che possiamo scrivere con la seguente formula:

$$V\approx\sum_{k=1}^{n}A(x_k^{*})\Delta x$$

Il secondo membro è proprio una [somma di Riemann](../riemann-integrability-criteria/) della funzione $A$ sull'intervallo $[a,b]$ e che ormai dovrebbe esserci familiare in quanto ne abbiamo parlato più volte dall'inizio della sezione dedicata agli integrali. Sappiamo che se $A$ è [continua](../continuous-functions/) su $[a,b]$ la funzione è integrabile, e al tendere di $\Delta x$ a zero le fette si assottigliano sempre di più seguendo il profilo del solido migliorandone l'approssimazione al suo profilo. Il limite di queste somme è allora l'integrale definito di $A$ tra i due estremi dell'intervallo:

$$V=\int_a^b A(x) \ dx \tag{1}$$

Affinché questo procedimento sia percorribile devono però valere due condizioni:

+ La prima è che ogni sezione sia una figura dotata di area.
+ La seconda è che la funzione $A$ sia integrabile su $[a,b].$ Ricordiamo che la continuità di $A$ garantisce l'integrabilità, ma non è necessaria: infatti possiamo tranquillamente incontrare un numero finito di discontinuità che lascia la funzione integrabile (ad esempio nel caso di solidi ottenuti accostando elementi di forma diversa tra loro).

- - -

È utile notare come il volume dipenda dalle sole aree delle sezioni e non dalla loro forma. Una conseguenza di questo enunciato riguarda i solidi obliqui. Se un cilindro viene inclinato mantenendo la base e l'altezza il suo volume non cambia. La stessa osservazione vale per prismi e le piramidi oblique, motivo per cui le formule della geometria solida non contengano mai alcun riferimento all'inclinazione degli spigoli (il che semplifica di molto le cose).

Di seguito vedremo come calcolare il volume di alcune figure solide tipiche il cui risultato è riepilogato qui in breve:

[class="table-1"]

| | | |
| --- | --- | --- |
| Piramide | $$\int_0^h \frac{B}{h^2}x^2 \ dx$$ | $$\frac{1}{3}Bh$$ |
| Cono circolare retto | $$\int_0^h \frac{\pi r^2}{h^2}x^2 \ dx$$ | $$\frac{1}{3}\pi r^2h$$ |
| Sfera | $$\int_{-r}^{r}\pi(r^2-x^2) \ dx$$ | $$\frac{4}{3}\pi r^3$$ |
| Solido a sezioni quadrate | $$\int_{-1}^{1}(1-x^2)^2 \ dx$$ | $$\frac{16}{15}$$ |
| Cuneo cilindrico | $$\int_0^r 2y\sqrt{r^2-y^2}\tan\alpha \ dy$$ | $$\frac{2}{3}r^3\tan\alpha$$ |

[/class]

## Il volume della piramide e del cono

Consideriamo proprio il caso di una piramide di altezza $h$ e base $B.$ Disponiamo l'asse delle $x$ lungo la retta dell'altezza, con origine nel vertice. Il piano perpendicolare a quest'asse a una distanza $x$ dal vertice è parallelo alla base e taglia la piramide in un poligono che, in termini semplici, è una copia della base ottenuta attraverso quella che viene definita omotetia di centro il vertice e rapporto $x/h$.

![IMG. 3](svg/volumes-by-parallel-cross-sections-3.svg)

Con il termine omotetia di rapporto $k$ s'intende una trasformazione che ingrandisce o riduce una figura mantenendone invariata la forma di un fattore $k$. Questa trasformazione moltiplica le lunghezze per $k$ e le aree per $k^2,$ da cui possiamo derivare la seguente relazione:

$$A(x)=B\left(\frac{x}{h}\right)^2=\frac{B}{h^2}x^2$$

A questo punto, il volume si ottiene integrando dal vertice alla base rispetto a $x$. Portando il fattore $B/h^2$ fuori dal segno di integrale, i calcoli risolutivi sono immediati:

$$
\begin{align}
V &= \int_0^h \frac{B}{h^2}x^2 \ dx \\[6pt]
  &= \frac{B}{h^2}\int_0^h x^2 \ dx \\[6pt]
  &= \frac{B}{h^2}\left[\frac{x^3}{3}\right]_0^h \\[6pt]
  &= \frac{B}{h^2}\cdot\frac{h^3}{3} \\[6pt]
  &= \frac{1}{3}Bh
\end{align}
$$

Pertanto, una piramide di base $B$ e altezza $h$ ha volume pari a un terzo del prodotto fra l'area di base e l'altezza! Piccola nota storica a margine: l'idea dell'omotetia è antichissima. Se prendiamo per buono il terzo millennio avanti Cristo il periodo a cui far risalire la costruzione delle piramidi, già allora gli antichi Egizi utilizzavano tale concetto nella costruzione delle piramidi (e no, non credo siano stati gli alieni a costruirle...).

- - -

Tornando, invece, a questioni più vicine ai nostri giorni, per un cono circolare retto il processo di calcolo del suo volume è lo stesso di quello della piramide. La sezione a distanza $x$ dal vertice è un cerchio di raggio $rx/h,$ dove $r$ è il raggio di base, e la sua area vale $\pi r^2x^2/h^2.$ L'integrale è quello appena svolto ma il fattore $B/h^2$  viene riscritto con $B=\pi r^2$. Svolgendo i calcoli otteniamo: 

$$V=\frac{1}{3}\pi r^2h$$

Lo stesso risultato vale per ogni solido a punta le cui sezioni parallele alla base siano ottenute mediante omotetie di centro il vertice. Alla distanza $x$ dal vertice il rapporto di omotetia è $x/h,$ per cui il volume è $Bh/3,$ qualunque sia la base.

## I solidi di rotazione

Un metodo di calcolo simile a quello appena illustrato si applica ai solidi ottenuti ruotando una certa regione di piano $R$ attorno a un'asse (in particolare all'asse delle $x$). In termini più formali, supponiamo che una funzione $f$ sia continua e non negativa su $[a,b],$ e sia $R$ la regione delimitata dal grafico di $f,$ dall'asse delle $x$ e dalle rette $x=a$ e $x=b.$ Ruotando $R$ attorno all'asse delle $x$ si ottiene un solido le cui sezioni perpendicolari a quell'asse sono cerchi di raggio $f(x)$ di area pari a $A(x)$:

$$A(x)=\pi\big(f(x)\big)^2$$

La formula generale restituisce l'espressione del [metodo dei dischi](../the-disc-method/):

$$V=\int_a^b\pi\big(f(x)\big)^2 \ dx$$

Mentre, se una seconda curva $g,$ con $0\le g(x)\le f(x)$ su $[a,b],$ separa la regione dall'asse, la rotazione apre una cavità e la sezione diventa una corona circolare di raggio esterno $f(x)$ e raggio interno $g(x).$ In questo caso si ottiene la formula del [metodo delle corone circolari](../the-washer-method/):

$$V=\int_a^b\pi\left[\big(f(x)\big)^2-\big(g(x)\big)^2\right] \ dx$$

Il [metodo dei gusci](../the-shell-method/) invece non rientra in questo schema, perché non decompone il solido in fette perpendicolari all'asse di rotazione ma in superfici cilindriche coassiali. Notate che la scelta dei metodi è fatta esclusivamente in funzione di quanto risultino semplici gli integrali da risolvere, ma al di là degli aspetti computazionali essi conducono allo stesso valore del volume. Per un approfondimento dei singoli metodi vi suggerisco il rimando diretto alle singole voci che sono più dettagliate e contengono esempi esplicativi.

- - -

La sfera è un caso a parte e si tratta con la formula generale senza passare per l'idea di rotazione. Se fissiamo l'origine della sfera nel centro e tagliamo con piani perpendicolari a un diametr (che assumiamo come asse delle $x$), il piano di ascissa $x,$ con $-r\le x\le r,$ interseca la sfera in un cerchio. Il raggio di questo cerchio e la distanza $|x|$ dal centro sono i cateti di un triangolo rettangolo di ipotenusa $r,$ e per il [teorema di Pitagora](../pythagorean-theorem/) il raggio della sezione vale $\sqrt{r^2-x^2}.$ L'area della sezione è dunque:

$$A(x)=\pi(r^2-x^2)$$

Integrando $A(x)$ fra i due poli della sferma si ottiene il volume:

$$
\begin{align}
V &= \int_{-r}^{r}\pi(r^2-x^2) \ dx \\[6pt]
  &= \pi\left[r^2x-\frac{x^3}{3}\right]_{-r}^{r} \\[6pt]
  &= \pi\left[\left(r^3-\frac{r^3}{3}\right)-\left(-r^3+\frac{r^3}{3}\right)\right] \\[6pt]
  &= \pi\left(\frac{2}{3}r^3+\frac{2}{3}r^3\right) \\[6pt]
  &= \frac{4}{3}\pi r^3
\end{align}
$$

## Solidi non di rotazione

Consideriamo adesso un caso diverso, prendendo in esame la regione $R$ compresa fra la parabola di equazione $y=1-x^2$ e l'asse delle ascisse, e costruiamo il solido $S$ che ha $R$ come base e le cui sezioni perpendicolari all'asse delle $x$ sono quadrati.

![IMG. 4](svg/volumes-by-parallel-cross-sections-4.svg)

La parabola $y=1-x^2$ incontra l'asse $x$ nei punti di ascissa $-1$ e $1,$ che delimitano l'intervallo di integrazione. Fissato un $x$ generico in $[-1,1],$ il piano perpendicolare all'asse taglia la base lungo il segmento che congiunge l'asse al grafico della parabola, di lunghezza $1-x^2$ che rappresenta il lato del quadrato della nostra sezione. Possiamo scrivere quindi l'area $A(x)$ del quadrato come:

$$A(x)=(1-x^2)^2$$

I calcoli sono piuttosto banali e conducono al seguente risultato:

$$
\begin{align}
V &= \int_{-1}^{1}(1-x^2)^2 \ dx \\[6pt]
  &= \int_{-1}^{1}(1-2x^2+x^4) \ dx \\[6pt]
  &= \left[x-\frac{2}{3}x^3+\frac{x^5}{5}\right]_{-1}^{1} \\[6pt]
  &= 2\left(1-\frac{2}{3}+\frac{1}{5}\right) \\[6pt]
  &= \frac{16}{15}
\end{align}
$$

Ricordate che $A(x)=(1-x^2)^2$ è una [funzione pari](../even-and-odd-functions/), per cui il suo integrale su $[-1,1]$ vale il doppio dell'integrale su $[0,1].$ Quindi il solido a sezioni quadrate costruito sulla regione parabolica ha volume $16/15.$

- - -

Facciamo ora un ulteriore esempio che mostra come la direzione lungo cui si taglia il solido è libera, e che direzioni del taglio differenti producono sezioni di forma diversa ma determinano lo stesso volume.

Prendiamo un cilindro circolare retto di raggio $r$ e scegliamo un diametro della sua base. Immaginiamo ora di far ruotare attorno a questo diametro un piano, inclinandolo di un angolo $\alpha$ rispetto al piano di base, con $0<\alpha<\pi/2$. Supponiamo che il cilindro abbia altezza $H\ge r\tan\alpha,$ in modo che la base superiore non tronchi il cuneo. Il piano così ottenuto taglia il cilindro: la parte del cilindro compresa tra la base e il piano inclinato prende il nome di cuneo cilindrico.


![IMG. 5](svg/volumes-by-parallel-cross-sections-5.svg)

Riferiamo la base a un sistema cartesiano con origine nel centro e poniamo l'asse $x$ lungo il diametro attorno al quale ruota il piano di taglio, mentre l'asse $y$ perpendicolare a esso. Nel semipiano $y\ge0$ l'altezza cresce linearmente con $y$ ed è data da $z=y\tan\alpha$ (prendetelo per brevità come un dato di fatto).

Tagliamo adesso il cuneo che abbiamo ottenuto con piani perpendicolari all'asse delle $y.$ Fissato $y$ in $[0,r],$ la corda del cerchio di base, a distanza $y$ dal centro, ha lunghezza $2\sqrt{r^2-y^2},$ mentre l'altezza del piano di taglio abbiamo già visto che vale $y\tan\alpha$ ed è la stessa in tutti i punti della corda. La sezione è dunque un rettangolo di area pari a:

$$A(y)=2y\sqrt{r^2-y^2}\tan\alpha$$

Questo è un tipico integrale che si risolve [per sostituzione](../integration-by-substitution/) ponendo $u=r^2-y^2,$ da cui $du=-2y \ dy.$ Svolgendo i calcoli otteniamo il seguente valore del volume:

$$
\begin{align}
V &= \int_0^r 2y\sqrt{r^2-y^2}\tan\alpha \ dy \\[6pt]
  &= \tan\alpha\int_0^r 2y\sqrt{r^2-y^2} \ dy \\[6pt]
  &= \tan\alpha\left[-\frac{2}{3}(r^2-y^2)^{3/2}\right]_0^r \\[6pt]
  &= \tan\alpha\left(0+\frac{2}{3}r^3\right) \\[6pt]
  &= \frac{2}{3}r^3\tan\alpha
\end{align}
$$

Quindi il cuneo ricavato da un cilindro di raggio $r$ con un piano inclinato di $\alpha,$ e passante per un diametro qualunque della base, ha volume $2/3 \cdot r^3\tan\alpha.$ Come nei casi visti sopra questa è una formula generale.

Facciamo ad esempio il caso in cui tagliamo lo stesso cuneo con piani perpendicolari all'asse $x.$ Le sezioni cambiano forma e fissato $x$ in $[-r,r],$ la sezione è il triangolo rettangolo che ha un cateto lungo $\sqrt{r^2-x^2}$ sul piano di base e l'altro cateto verticale, lungo $\sqrt{r^2-x^2}\tan\alpha.$ La sua area vale base per altezza diviso 2:

$$\frac{1}{2}(r^2-x^2)\tan\alpha$$

Svolgendo l'integrale otteniamo banalmente $2/3 \cdot r^3\tan\alpha$ che è lo stesso risultato ottenuto poco sopra.

## Condizioni di applicabilità

Questo metodo è piuttosto semplice da mettere in pratica una volta che si è compreso il meccanismo di base. Tuttavia esistono delle condizioni di applicabilità sintetizzate di seguito.

La direzione lungo cui si affetta il solido va scelta considerando le sezioni prodotte dal taglio. Il cuneo cilindrico da esempio ammette due decomposizioni ugualmente valide, in rettangoli e in triangoli, e i due integrali che ne derivano hanno difficoltà confrontabile. In altri casi la differenza è più marcata e meritano maggiore attenzione. Un cono tagliato perpendicolarmente al proprio asse genera dei cerchi, mentre piani con inclinazioni diverse possono produrre sezioni ellittiche, paraboliche o [iperboliche](../hyperbola/), i cui integrali sono generalmente più laboriosi.

Da notare che quando sostituiamo ciascuna fetta del solido con un piccolo cilindro o prisma di area di base $A(x_i)$ e spessore $\Delta x$, stiamo approssimando soltanto il suo volume. Se $A$ varia in modo sufficientemente regolare, l'errore prodotto da ogni fetta diventa sempre più piccolo al diminuire di $\Delta x$ e, nel limite, la somma di questi errori tende a zero e la somma converge al volume del solido.

Questa costruzione non fornisce invece un'approssimazione della superficie laterale: i bordi delle singole fette non ricostruiscono, nel limite, l'area della superficie del solido. Per calcolarla è necessario un procedimento distinto.

Da tenere sempre a mente infine che tutto questo richiede che la funzione $A(x)$, che descrive l'area delle sezioni, sia integrabile nell'intervallo considerato. Se la forma delle sezioni cambia lungo l'asse, basta spesso suddividere il solido in più parti. Per esempio, se un solido è formato da un cono e un cilindro, $A(x)$ avrà espressioni diverse nei due tratti che delimitano le due figure e il volume si calcolerà separando i corrispondenti integrali.
