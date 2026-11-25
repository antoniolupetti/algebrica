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
Prendete ad esempio il seguente integrale improprio su tutta la retta reale, noto come integrale di Gauss:

$$
\int_{-\infty}^{+\infty} e^{-x^2}\,dx = \sqrt{\pi}
$$

A prima vista può sembrare un oggetto innocuo, ma se si prova a risolverlo con i metodi elementari di integrazione non se ne viene a capo. La storia comunemente accettata vuole che Gauss l'abbia risolto a intorno ai trent'anni, quindi, almeno fino a quell'età, sentitevi pure dispensati dall'essere in grado di determinarne il valore.
Un altro integrale verso cui provare un reverenziale timore è quello di Dirichlet, semplice nella forma ma difficilissimo nella sostanza:

$$
\int_{0}^{\infty} \frac{\sin x}{x}\,dx = \frac{\pi}{2}
$$

Per nostra fortuna, la maggior parte di noi non corre per una _Field Medal_, nutre ambizioni più contenute e per questa ragione, gli integrali con cui avrà a che fare nel corso dei propri studi sono quindi, in prevalenza, alla portata di un qualunque studente volenteroso (fatto salvo il caso in cui abbia la sfortuna di imbattersi lungo il proprio percorso accademico in qualche professore particolarmente sadico).

La buona notizia è che una larga parte di questi oggetti matematici sono risolvibili con processi meccanici e un pizzico di intuizione che si può sviluppare solo ed esclusivamente facendo tantissima pratica sulle principali regole di integrazione e sulle tipiche scorciatoie che consentono di risparmiare un quantità significativa di passaggi.

- - -

Nei successivi paragrafi proporrò una definizione rigorosa degli integrali, in particolare di quelli indefiniti che sono l'oggetto di questa voce e sono fondamentali per introdurre gli omonimi definiti. Tuttavia preferisco fare una premessa intuitiva, partendo dal concetto di derivazione, che come vedremo più avanti, parlando di _primitive_, è l'operazione inversa dell'integrazione. 

Consideriamo una semplice funzione $y=x^2$. Il suo grafico è una parabola passante per l'origine. Sappiamo, dallo studio delle regole di derivazione, che la sua derivata è unica ed è pari a $y'=2x$ e associa ad ogni valore di $x$ il coefficiente angolare della retta tangente al grafico in quel punto. Per esempio, per $x=2$ si ottiene $y'(2)=2 \cdot 2 = 4.$ Questo significa che la retta tangente alla parabola nel punto $(2,4)$ ha coefficiente angolare proprio pari a $4$.

![IMG. 1](indefinite-integrals-1.svg)

Analizziamo adesso il caso inverso, in cui abbiamo una data derivata, ad esempio proprio $y'=2x,$ e cerchiamo una sua primitiva. Dal calcolo precedente sappiamo che $y=x^2$ è una primitiva di $2x.$

Se vogliamo invece descrivere tutte le primitive di $2x$ su $\mathbb{R},$ dobbiamo includere una costante arbitraria: ogni primitiva ha la forma $y=x^2+c,$ con $c\in\mathbb{R}.$ Il motivo di questa caratterizzazione è banale, ma è sorprendente come anche molti studenti già navigati non sanno fornire una risposta immediata a tale motivazione. Il grafico renderà il tutto più chiaro. Se immaginate di traslare sull'asse y la funzione $y=x^2$ avrete infinte funzioni omologhe lungo tutto l'asse che differiscono solo per il termine noto.

![IMG. 1](indefinite-integrals-2.svg)

La traslazione verticale, infatti, non modifica in alcun modo la pendenza della curva. Le funzioni $y=x^2$, $y=x^2+1$, $y=x^2-3$ e, più in generale, tutte le funzioni della forma $y=x^2+c$ hanno quindi esattamente la stessa derivata, $y'=2x$.

È proprio questa semplice osservazione geometrica a spiegare perché una funzione ha una sola derivata, mentre la stessa funzione può avere infinite primitive, tutte diverse tra loro per una costante.

Per concludere questa premessa, ricordate la seguente distinzione fondamentale: l'integrale indefinito determina la famiglia di primitive data una certa derivata, mentre l'integrale definito, oggetto di un'apposita voce, calcola l'area con segno compresa tra una curva e l'asse delle ascisse all'interno di un dato intervallo. Nei paragrafi successivi sono elencate le principali primitive e le proprietà degli integrali. Per vostra sventura dovrete impararle tutte a memoria (intendo proprio tutte), condizione necessaria per avere qualche possibilità di sviluppare correttamente i calcoli degli integrali più complessi che incontreremo più avanti.

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

Come sappiamo dallo studio delle derivate, ogni funzione derivabile ha un'unica derivata. Il problema inverso consiste nello stabilire se una generica funzione $f$ è la derivata di qualche funzione $F$. Consideriamo una funzione $f\colon I \to \mathbb{R}$ definita su un intervallo aperto $I.$ Una funzione derivabile $F\colon I \to \mathbb{R}$ si chiama primitiva o antiderivata di $f$ se soddisfa la seguente condizione:

$$F'(x) = f(x) \qquad \forall \ x \in I \tag{1}$$

Quando $f$ è continua su $I,$ ammette almeno una primitiva in $I$. Per esempio, il calcolo nella $(2)$ mostra che $F(x) = x^3$ è una primitiva di $f(x) = 3x^2$ su $\mathbb{R}:$

$$\frac{d}{dx} x^3 = 3x^2 \tag{2}$$

La continuità di $f$ è una condizione sufficiente e non necessaria per l'esistenza di una primitiva. Per dimostrarlo, consideriamo la seguente funzione $F$ e studiamone la derivata:

$$
F(x) :=
\begin{cases}
x^2\sin(1/x) & \text{se } x \neq 0 \\[6pt]
0 & \text{se } x = 0
\end{cases} \tag{3}
$$

Svolgendo i calcoli con le operazioni di derivazione, quando $x \neq 0$ si ottiene:

$$
\begin{align}
F'(x) &= 2x\sin(1/x) + x^2\cos(1/x)\left(-\frac{1}{x^2}\right) \notag \\[6pt]
      &= 2x\sin(1/x) - \cos(1/x) \tag{4}
\end{align}
$$

Vediamo ora il caso in cui $x=0$ usando la definizione di derivata come limite del rapporto incrementale. Per il teorema del confronto otteniamo la seguente identità:

$$
\begin{align}
F'(0) &= \lim_{h \to 0}\frac{F(h) - F(0)}{h} \notag \\[6pt]
      &= \lim_{h \to 0}h\sin(1/h) = 0 \tag{5}
\end{align}
$$

Le formule $(4)$ e $(5)$ definiscono quindi $f = F'$ su tutto $\mathbb{R}.$ Per $x \to 0,$ il termine $2x\sin(1/x)$ tende a zero, mentre $\cos(1/x)$ oscilla tra $-1$ e $1$ e di conseguenza $f$ è discontinua nell'origine, pur avendo $F$ come primitiva, valida su tutto $\mathbb{R}.$

- - -

Come abbiamo visto nell'introduzione, aggiungere una costante a una funzione derivabile ne lascia invariata la derivata, spostandone semplicemente la posizione rispetto all'asse $y$. Per fare un esempio, $x^3,$ $x^3 + 5$ e $x^3 - 1/2$ sono tutte primitive di $3x^2.$ In generale, se $F$ è una primitiva di $f$ su un intervallo $I,$ si ha che anche $F+c$ è una primitiva di $f$ per ogni $c \in \mathbb{R}:$

$$\frac{d}{dx}[F(x) + c] = F'(x) = f(x) \tag{6}$$

Viceversa, se consideriamo $F_1$ e $F_2$ due primitive di $f$ su $I,$ poiché entrambe hanno derivata $f,$ la loro differenza ha derivata nulla in ogni punto di $I:$

$$
\begin{align}
\frac{d}{dx}[F_1(x) - F_2(x)] &= F_1'(x) - F_2'(x) \notag \\[6pt]
                               &= f(x) - f(x) = 0 \tag{7}
\end{align}
$$

Per la $(7)$ e il teorema di Lagrange, $F_1-F_2$ è dunque costante su $I$ ed esiste dunque un unico $c \in \mathbb{R}$ tale che $F_1(x) = F_2(x) + c$ per ogni $x \in I.$

## L'integrale indefinito

Vediamo ora come il concetto di primitiva si applichi a quello di integrale indefinito, supponendo che una generica funzione $f$ abbia primitiva $F$ su un intervallo aperto $I$. L'integrale indefinito di $f$ su $I$ è definito come la famiglia di tutte le sue primitive e per una qualunque costante $c \in \mathbb{R}$ ha la seguente forma:

$$\int f(x) \ dx = F(x) + c \tag{8}$$

Per la $(6),$ derivando una qualunque delle primitive nella $(8)$ si ritrova $f$ mentre, nel verso opposto, integrando $F'$ si riottiene a $F$ a meno di una costante:

$$\int F'(x) \ dx = F(x) + c\tag{9}$$

Per fare un esempio esempio, calcoliamo la primitiva di $f(x) = 3x$ il cui grafico passa per il punto $(2,1).$ Per la $(8)$ otteniamo:

$$F(x) = \frac{3}{2}x^2 + c \tag{10}$$

Ora determiniamo la $c$ tenendo presente che il passaggio per $(2,1)$ impone $F(2) = 1.$ Quindi, sostituendo $x = 2$ nella $(10)$ si ottiene $6 + c = 1,$ da cui $c = -5$ e dunque la primitiva cercata è:

$$F(x) = \frac{3}{2}x^2 - 5 \tag{11}$$

Lo stesso ragionamento vale se $F_0$ è una primitiva di $f$ su un intervallo aperto $I$ e $(x_0,y_0)$ è il punto assegnato con $x_0 \in I$ e $y_0 \in \mathbb{R}.$ Affinché il grafico di $F_0+c$ passi per quel punto, deve valere:

$$F_0(x_0)+c=y_0 \tag{12}$$ 
Per la $(12)$ la costante $c$ è quindi determinata e la primitiva richiesta è data da:

$$F(x) = F_0(x) + y_0 - F_0(x_0) \tag{13}$$

In termini formali quindi, la differenza $y_0-F_0(x_0)$ nella $(12)$ corrisponde proprio allo spostamento verticale di cui abbiamo parlato e che porta il punto $(x_0,F_0(x_0))$ in $(x_0,y_0).$ 

Una considerazione importante che va fatta per saper calcolare gli integrali è la seguente: per risolverli è necessario imparare a memoria tutte le primitive delle funzioni elementari, non c'è altro modo. È quindi un esercizio prettamente mnemonico che con l'esperienza diventerà anche piuttosto immediato e meccanico.

## Proprietà di linearità

Vediamo adesso un'importante proprietà degli integrali che è quella della linearità, utile nella risoluzione pratica di molti problemi e che vale sia per gli integrali indefiniti che per quelli definiti che vedremo nella voce dedicata. Supponendo che $f$ e $g$ abbiano primitive $F$ e $G$ sullo stesso intervallo, la condizione di linearità si esprime nel seguente modo:

$$\int [f(x) + g(x)] \ dx = F(x) + G(x) + c\tag{14}$$

Inoltre, per ogni $k \in \mathbb{R}$, l'identità $(kF)' = kf$ mostra che ogni primitiva di $kf$ ha la seguente forma:

$$\int kf(x) \ dx = kF(x) + c\tag{15}$$

Applichiamo la $(14)$ alla funzione $f(x) = 3x^2 + 2x$ e otteniamo:

$$
\begin{align}
\int (3x^2 + 2x) \ dx &= \int 3x^2 \ dx + \int 2x \ dx \notag \\[6pt]
                      &= x^3 + x^2 + c \tag{16}
\end{align}
$$

La $(16)$ spezza quindi l'integrale originario nella somma di due integrali più semplici che sono immediatamente risolvibili. Un altro esempio è dato dal seguente integrale:

$$
\begin{align}
\int 5\sin(x) \ dx &= 5 \int \sin(x) \ dx \\[6pt]
                   &= -5\cos(x) + c
                   \end{align}
$$

## Integrale di potenza e logaritmico

Come sappiamo dallo studio delle derivate, la derivata di una funzione potenza $x^{a+1},$ con $x \gt 0$ e $a \in \mathbb{R},$ è pari a $(a+1)x^a.$ Applicando la $(8)$ otteniamo quindi l'integrale che è dato da:

$$\int x^a \ dx = \frac{x^{a+1}}{a+1} + c\tag{17}$$

Per ora escludiamo il caso $a=-1$ che sarà sarà trattato poco più avanti nella sezione sull'integrale logaritmico. Facciamo un esempio pratico di applicazione della $(17)$ all'integrale del seguente polinomio:

$$
\begin{align}
\int (3x^4 + 5x^2) \ dx &= 3\int x^4 \ dx + 5\int x^2 \ dx \notag \\[6pt]
                        &= 3\frac{x^5}{5} + 5\frac{x^3}{3} + c \notag \\[6pt]
                        &= \frac{3}{5}x^5 + \frac{5}{3}x^3 + c \tag{18}
\end{align}
$$

Nella $(18)$ abbiamo applicato la $(14),$ la $(15)$ e la $(17).$ Applichiamo le stesse regole a un integrale in cui compare una radice:

$$ \tag{19}
\begin{align}
f(x)           &= 4x^3 - \frac{3}{\sqrt{x}} + 2\cos x \notag \\[6pt]
               &= 4x^3 - 3x^{-1/2} + 2\cos x \notag
\end{align}
$$
Per le proprietà dei radicali, nella $(19)$ abbiamo riscritto la radice $\sqrt{x}$ come $x^{1/2}$ e poiché si trova al denominatore come $x^{-1/2},$ perciò l'integrale diventa:

$$
\begin{align}
\int f(x) \ dx &= 4\int x^3 \ dx - 3\int x^{-1/2} \ dx + 2\int \cos x \ dx \notag \\[6pt]
               &= x^4 - 3\frac{x^{1/2}}{1/2} + 2\sin x + c \notag \\[6pt]
               &= x^4 - 6\sqrt{x} + 2\sin x + c
\end{align}
$$
- - -

Vediamo ora il caso della funzione potenza con $a=-1$ dove abbiamo che il denominatore $a+1$ nella $(17)$ si annulla. In questo caso, per trovare una primitiva di $1/x,$ osserviamo che per $x \gt 0$ la funzione $\ln x$ ha derivata $1/x.$ Per $x \lt 0,$ l'argomento $-x$ è positivo e possiamo derivare $\ln(-x)$ con la regola della catena:

$$\frac{d}{dx}\ln(-x) = \frac{1}{-x}\cdot(-1) = \frac{1}{x}$$

Il valore assoluto unisce i due casi in una formula valida su ogni intervallo aperto che non contiene l'origine per cui si ha

$$\int \frac{1}{x} \ dx = \ln|x| + c \qquad c \in \mathbb{R} \tag{20}$$

## Riepilogo e Integrali di uso comune

Ricapitolando, le principali regole di integrazione sono riportate di seguito:

[class="table-1"]

|                                    |                                                      |
| ---------------------------------- | ---------------------------------------------------- |
| Linearità della somma              | $$\int (f(x) + g(x)) \ dx = F(x) + G(x) + c$$        |
| Linearità del prodotto di costante | $$\int kf(x) \ dx = kF(x) + c$$                      |
| Regola della potenza               | $$\int x^a \ dx = \dfrac{x^{a+1}}{a+1} + c$$         |
| [Caso logaritmico](../integral-of-rational-functions/)                   | $$\int \dfrac{1}{x} \ dx = \ln \lvert x \rvert + c$$ |

Nella tabella successiva sono riportate invece le altre regole di integrazione delle funzioni elementari. Come ho detto poco sopra, queste regole vanno imparate a memoria per consentirvi di risolvere gli esercizi d integrazione. A prima vista possono sembrare ostiche e tante da ricordare, ma vi assicuro che con un po' di esercizio ci si abitua rapidamente e la loro applicazione diventa davvero naturale e meccanica. Tenete anche conto che queste regole da sole non bastano per risolvere gli integrali. Esistono infatti alcuni metodi specifici come l'integrazione per sostituzione o per parti che sono necessarie per poter risolvere alcuni esercizi non immediati. Il mio suggerimento è quindi quello di proseguire per gradi, imparando prima le regole di base e poi i metodi più avanzati.

[class="table-1 -right"]

|                                                        |       |
| ------------------------------------------------------ | ----- |
| $$\int a^x \ dx = \frac{a^x}{\ln a} + c$$              | [altro](../integral-of-the-exponential-function/) |
| $$\int \sin x \ dx = -\cos x + c$$                     | [altro](../integral-of-trigonometric-functions/) |
| $$\int \cos x \ dx = \sin x + c$$                      | [altro](../integral-of-trigonometric-functions/) |
| $$\int \frac{1}{\sin^2 x} \ dx = -\cot x + c$$         | [altro](../integral-of-trigonometric-functions/) |
| $$\int \frac{1}{\cos^2 x} \ dx = \tan x + c$$          | [altro](../integral-of-trigonometric-functions/) |
| $$\int \sec^2 x \ dx = \tan x + c$$                    | [altro](../integral-of-trigonometric-functions/) |
| $$\int \sec x \tan x \ dx = \sec x + c$$               | [altro](../integral-of-trigonometric-functions/) |
| $$\int \csc^2 x \ dx = -\cot x + c$$                   | [altro](../integral-of-trigonometric-functions/) |
| $$\int \csc x \cot x \ dx = -\csc x + c$$              | [altro](../integral-of-trigonometric-functions/) |
| $$\int \frac{1}{1 + x^2} \ dx = \arctan x + c$$        |       |
| $$\int \frac{1}{\sqrt{1 - x^2}} \ dx = \arcsin x + c$$ |       |

[/class]

Per fornire una migliore comprensione delle regole, nella voce sulle strategie di integrazione trovate alcuni metodi utili ad esaminare la struttura delle funzioni integrande più comuni in modo da scegliere il meccanismo più adeguato di integrazione.