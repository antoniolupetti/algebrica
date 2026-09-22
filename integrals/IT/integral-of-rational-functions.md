---
title: Integral of Rational Functions
source: https://algebrica.org/integral-of-rational-functions/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - arctangent
  - completing-the-square
  - indefinite-integral
  - integration
  - integration-by-substitution
  - linearity
  - logarithms
  - partial-fractions
  - polynomial-division
  - rational-functions
---
## Come approcciare all'integrazione delle funzioni razionali

Come sappiamo, una [funzione razionale](../rational-functions/) è una funzione caratterizzata dal rapporto tra due [polinomi](../polynomials/), $N(x)$ al numeratore e $D(x)$ al denominatore. Il suo [integrale indefinito](../indefinite-integrals/) ha la seguente forma generica:

$$\int \frac{N(x)}{D(x)} \ dx \tag{1}$$

Bisogna tenere a mente che, negli integrali delle funzioni razionali, prima di procedere con i calcoli bisogna sempre individuare i punti in cui $D(x)$ si annulla affinché la funzione integranda sia definita.

Gli integrali generalizzati dalla $(1)$ saranno declinati di seguito in varie casistiche che si presentano abbastanza frequentemente e per ciascuna di esse verrà mostrato il metodo risolutivo più adatto con cui procedere. In linea di massima non stiamo parlando di integrali molto complicati da risolvere, tuttavia è necessario molto esercizio per individuare immediatamente il metodo da applicare in modo da risparmiare molti passaggi e giungere a una soluzione in modo agevole. 

Per scegliere il metodo risolutivo iniziamo a confrontare i gradi dei due polinomi cercando di ricondurre il rapporto a una frazione propria, ovvero una frazione con il grado del numeratore strettamente minore di quello del denominatore.

Quando l'integrale iniziale si presenta già con una frazione propria, possiamo applicare direttamente i metodi descritti di seguito.

Quando, invece, il grado del numeratore è maggiore o uguale a quello del denominatore, abbiamo una frazione impropria e possiamo utilizzare la [divisione tra polinomi](../polynomial-division/) ottenendo un quoziente $Q(x)$ e un resto $R(x)$ che soddisfano l'identità:

$$N(x) = Q(x)D(x) + R(x)$$

Il resto può essere nullo oppure presentare un grado strettamente minore di quello di $D(x).$ Nei punti in cui il denominatore non si annulla possiamo dividere l'identità per $D(x)$ e scrivere:

$$\frac{N(x)}{D(x)} = Q(x) + \frac{R(x)}{D(x)}$$

Dalla $(1)$ e per la linearità dell'integrale possiamo scrivere:

$$\int \frac{N(x)}{D(x)} \ dx = \int Q(x) \ dx + \int \frac{R(x)}{D(x)} \ dx \tag{2}$$

Se il resto $R(x)$ è nullo, basta calcolare l'integrale di $Q(x)$ che si integra banalmente, termine a termine, con la regola delle potenze. Se invece il resto è diverso da zero, dobbiamo integrare anche la frazione $R(x)/D(x).$ La divisione tra polinomi ha reso il grado del numeratore minore di quello del denominatore ottenendo così una frazione propria, che era il nostro obiettivo.

Per integrare il secondo integrale della $(2)$ va ricordato che nei numeri reali ogni polinomio non costante si scompone in fattori lineari e fattori quadratici irriducibili, eventualmente ripetuti. Questa scomposizione permette di riscrivere la frazione come somma di fratti semplici, ai quali possiamo applicare le formule di integrazione che vedremo nei prossimi paragrafi.

> Prima di lanciarci nella divisione o nella scomposizione dei polinomi conviene sempre controllare se il numeratore e il denominatore hanno fattori comuni che possono essere semplificati, ricordando sempre di escludere gli zeri del denominatore originario che non appartengono al dominio della funzione integranda.

- - -

Facciamo subito un esempio che ricalca quanto illustrato finora. Calcoliamo il seguente integrale che presenta una frazione impropria:

$$\int \frac{x^3 + x + 1}{x^2 + 1} \ dx$$

Il numeratore ha grado $3$ e il denominatore ha grado $2,$ quindi procediamo con la divisione tra polinomi cercando di ricondurre l'integrale alla forma $(2)$. Il rapporto tra i termini di grado massimo è $x^3/x^2 = x.$ Moltiplicando il denominatore per $x$ otteniamo $x^3 + x$ e possiamo scrivere:

$$x^3 + x + 1 = x(x^2 + 1) + 1$$

Il quoziente è $Q(x) = x$ e il resto è $R(x) = 1.$ Dividendo per $x^2 + 1$ otteniamo:

$$\frac{x^3 + x + 1}{x^2 + 1} = x + \frac{1}{x^2 + 1}$$

Quindi possiamo riscrivere il nostro integrale iniziale come:

$$
\begin{align}
\int \frac{x^3 + x + 1}{x^2 + 1} \ dx &= \int x \ dx + \int \frac{1}{x^2 + 1} \ dx \\[6pt]
  &= \frac{x^2}{2} + \arctan x + k
\end{align}
$$

Il primo termine è banale e si integra con la regola delle potenze, mentre il secondo è la derivata dell'arcotangente. Abbiamo così trovato le primitive della funzione su tutto $\mathbb{R},$ perché il denominatore $x^2 + 1$ è sempre positivo.

## Quando il denominatore è lineare

Se una frazione propria ha il denominatore di primo grado, il suo numeratore è inevitabilmente una costante. Se indichiamo questa costante con $c,$ ci troveremo a calcolare un integrale della forma:

$$\int \frac{c}{ax + b} \ dx \tag{3}$$

 I coefficienti $a,$ $b$ e $c$ sono reali e $a \neq 0.$ In casi come questo possiamo applicare l'[integrazione per sostituzione](../integration-by-substitution/) e ponendo $t = ax + b$ e $dt = a \ dx$ otteniamo che l'integrale (3) si può riscrivere come:

$$
\begin{align}
\int \frac{c}{ax + b} \ dx &= \frac{c}{a} \int \frac{1}{t} \ dt \\[8pt]
  &= \frac{c}{a} \ln|t| + k \\[10pt]
  &= \frac{c}{a} \ln|ax + b| + k
\end{align}
$$

- - -
 
Applichiamo il metodo appena descritto al seguente integrale:

$$\int \frac{2}{6x + 1} \ dx$$

Poniamo $t = 6x + 1.$ La derivata di $t$ rispetto a $x$ è $6,$ quindi $dt = 6 \ dx$ e $dx = dt/6.$ Sostituendo, otteniamo:

$$
\begin{align}
\int \frac{2}{6x + 1} \ dx &= \frac{2}{6} \int \frac{1}{t} \ dt \\[8pt]
  &= \frac{1}{3} \ln|t| + k \\[10pt]
  &= \frac{1}{3} \ln|6x + 1| + k
\end{align}
$$

Il calcolo è piuttosto semplice perché conduce sempre a una primitiva contenente il logaritmo. L'importante è individuare la sostituzione corretta e la risoluzione diventa immediata.


## Scomposizione in fratti semplici

Analizziamo adesso il caso in cui il denominatore contiene più fattori e per separarne i contributi ricorriamo alla [scomposizione in fratti semplici](../partial-fraction-decomposition/). Consideriamo, ad esempio, l'integrale:



$$\int \frac{7x + 5}{(x - 1)(3x + 2)} \ dx$$

Quando i fattori sono lineari e distinti, a ciascuno di essi associamo una frazione con un numeratore costante. 

$$\frac{A}{x - 1} + \frac{B}{3x + 2}$$

I coefficienti $A$ e $B$ si determinano imponendo l'uguaglianza con la funzione iniziale:

$$\frac{7x + 5}{(x - 1)(3x + 2)} = \frac{A}{x - 1} + \frac{B}{3x + 2} \tag{4}$$

Svolgendo i calcoli otteniamo:

$$7x + 5 = A(3x + 2) + B(x - 1)$$

Scegliendo $x=1$ il termine con coefficiente $B$ si annulla e otteniamo $A = 12/5.$ Per $x = -2/3$ invece si annulla il termine con coefficiente $A$ e otteniamo $B = -1/5.$ Sostituendo i valori ottenuti alla $(4)$ otteniamo:

$$\frac{7x + 5}{(x - 1)(3x + 2)} = \frac{12}{5(x - 1)} - \frac{1}{5(3x + 2)}$$

Possiamo quindi riscrivere l'integrale come:

$$
\begin{align}
\int \frac{7x + 5}{(x - 1)(3x + 2)} \ dx &= \frac{12}{5} \int \frac{1}{x - 1} \ dx - \frac{1}{5} \int \frac{1}{3x + 2} \ dx \\[6pt]
  &= \frac{12}{5} \ln|x - 1| - \frac{1}{15} \ln|3x + 2| + k
\end{align}
$$

Le primitive sono quindi espresse da questa differenza tra logaritmi sugli intervalli $(-\infty,-2/3),$ $(-2/3,1)$ e $(1,+\infty).$

## Fattori lineari ripetuti

Vediamo adesso un'ulteriore casistica in cui il denominatore contiene un fattore $(x - r)^k$ con molteplicità $k \geq 2$. Nella scomposizione dobbiamo prevedere un termine per ciascuna potenza del fattore, dalla prima fino alla $k$-esima ottenendo la seguente forma:

$$\frac{A_1}{x - r} + \frac{A_2}{(x - r)^2} + \dots + \frac{A_k}{(x - r)^k}$$

I numeratori sono costanti da determinare con la scomposizione in fratti semplici vista sopra e se siamo fortunati alcune potrebbero risultare nulle, semplificando i calcoli. Il primo termine, quello con denominatore $x - r$ dà la primitiva $A_1\ln|x - r|$ mentre, per le potenze successive, usiamo invece la regola di integrazione delle potenze, perché l'esponente dell'integranda è $-j \neq -1.$ Per ogni $j \geq 2$ vale:

$$\int \frac{A_j}{(x - r)^j} \ dx = \frac{A_j}{1 - j}(x - r)^{1 - j} + k$$

Facciamo subito un esempio pratico calcolando il seguente integrale:

$$\int \frac{3x + 1}{(x - 1)^2(x + 2)} \ dx \tag{5}$$

Il fattore $x - 1$ ha molteplicità $2,$ mentre $x + 2$ compare una sola volta. Scriviamo quindi la scomposizione:

$$\frac{3x + 1}{(x - 1)^2(x + 2)} = \frac{A}{x - 1} + \frac{B}{(x - 1)^2} + \frac{C}{x + 2}$$

Moltiplicando per il denominatore comune otteniamo:

$$3x + 1 = A(x - 1)(x + 2) + B(x + 2) + C(x - 1)^2$$

Per $x = 1$ si annullano il primo e il terzo termine a destra, quindi $4 = 3B$ e $B = 4/3.$ Per $x = -2$ rimane soltanto il termine contenente $C,$ perciò $-5 = 9C$ e $C = -5/9.$ Per trovare $A$ possiamo confrontare i coefficienti di $x^2.$ A sinistra il coefficiente è zero, mentre a destra è $A + C.$ Di conseguenza $A + C = 0$ e $A = 5/9.$ La scomposizione risulta quindi:

$$\frac{3x + 1}{(x - 1)^2(x + 2)} = \frac{5}{9(x - 1)} + \frac{4}{3(x - 1)^2} - \frac{5}{9(x + 2)}$$

Otteniamo dunque:

$$
\begin{align}
\int \frac{3x + 1}{(x - 1)^2(x + 2)} \ dx &= \frac{5}{9} \int \frac{1}{x - 1} \ dx + \frac{4}{3} \int \frac{1}{(x - 1)^2} \ dx - \frac{5}{9} \int \frac{1}{x + 2} \ dx \\[6pt]
  &= \frac{5}{9} \ln|x - 1| - \frac{4}{3(x - 1)} - \frac{5}{9} \ln|x + 2| + k
\end{align}
$$

Abbiamo così ottenuto le primitive su ciascuno degli intervalli $(-\infty,-2),$ $(-2,1)$ e $(1,+\infty),$ che escludono i punti $x = -2$ e $x = 1,$ nei quali il denominatore della $(5)$ si annulla e l'integranda iniziale non è definita.

## Fattori quadratici irriducibili

Vediamo un ulteriore caso, un po' più complicato dei precedenti, ricordando che un polinomio di secondo grado con [discriminante](../quadratic-formula/) negativo non ha radici reali e non si può scomporre in fattori lineari reali. Per questo motivo il fattore quadratico rimane quindi al denominatore così com'è. Per semplificare i calcoli, dividiamo numeratore e denominatore per il coefficiente di $x^2,$ così da scrivere il fattore nella forma:

$$q(x) = x^2 + bx + c \qquad b^2 - 4c < 0$$

Se questo fattore compare una sola volta, gli associamo un termine della forma:

$$\frac{Ax + B}{q(x)}$$

Il numeratore ha grado al massimo $1,$ quindi al limite può anche essere costante o nullo. Per integrare questa frazione confrontiamo il numeratore con la derivata $q'(x) = 2x + b.$ Riscriviamo quindi il numeratore come somma di un multiplo di questa derivata e di una costante:

$$Ax + B = \frac{A}{2}(2x + b) + \left(B - \frac{Ab}{2}\right)$$

L'integrale si separa così in due parti:

$$\int \frac{Ax + B}{q(x)} \ dx = \frac{A}{2} \int \frac{q'(x)}{q(x)} \ dx + \left(B - \frac{Ab}{2}\right) \int \frac{1}{q(x)} \ dx$$

La prima parte dà un logaritmo mediante la sostituzione $v = q(x).$ Per la seconda usiamo il metodo del [completamento del quadrato](../completing-the-square/):

$$q(x) = \left(x + \frac{b}{2}\right)^2 + c - \frac{b^2}{4}$$

Il discriminante negativo implica $c - b^2/4 > 0.$ Poniamo quindi $\rho = \sqrt{c - b^2/4} > 0$ e $u = x + b/2.$ Poiché $du = dx,$ il secondo integrale diventa:

$$\int \frac{1}{q(x)} \ dx = \int \frac{1}{u^2 + \rho^2} \ du$$

Con l'ulteriore sostituzione $t = u/\rho$ abbiamo $du = \rho \ dt$ e riconosciamo la derivata dell'[arcotangente](../arctangent-and-arccotangent/):

$$
\begin{align}
\int \frac{1}{u^2 + \rho^2} \ du &= \frac{1}{\rho} \int \frac{1}{1 + t^2} \ dt \\[6pt]
  &= \frac{1}{\rho} \arctan t + k \\[6pt]
  &= \frac{1}{\rho} \arctan\left(\frac{u}{\rho}\right) + k
\end{align}
$$

Riunendo i due contributi otteniamo la formula:

$$\int \frac{Ax + B}{q(x)} \ dx = \frac{A}{2}\ln q(x) + \frac{B - Ab/2}{\rho}\arctan\left(\frac{x + b/2}{\rho}\right) + k$$

La formula permette quindi di calcolare l'integrale esprimendo la primitiva attraverso un logaritmo e un'arcotangente. Per applicarla, individuiamo i coefficienti $A,$ $B,$ $b$ e $c,$ calcoliamo $\rho = \sqrt{c - b^2/4}$ e sostituiamo questi valori nell'espressione ottenuta.

- - -

Vediamo un caso pratico per comprendere meglio i passaggi e la natura delle sostituzioni. Risolviamo il seguente integrale:

$$\int \frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} \ dx$$

Il denominatore contiene il fattore lineare $x + 1$ e il fattore quadratico $x^2 + 2x + 3.$ Il discriminante di quest'ultimo è $2^2 - 4 \cdot 3 = -8,$ quindi il fattore è irriducibile nei reali. Impostiamo la scomposizione:

$$\frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} = \frac{A}{x + 1} + \frac{Bx + C}{x^2 + 2x + 3}$$

Moltiplicando per il denominatore comune otteniamo l'identità:

$$5x^2 + 3x - 2 = A(x^2 + 2x + 3) + (Bx + C)(x + 1)$$

Per $x = -1$ il membro sinistro vale $5 - 3 - 2 = 0$ e quello destro si riduce a $2A.$ Ne segue $A = 0.$ Sviluppando il prodotto rimasto troviamo:

$$5x^2 + 3x - 2 = Bx^2 + (B + C)x + C$$

Dal confronto dei coefficienti di $x^2$ e del termine costante ricaviamo $B = 5$ e $C = -2.$ Anche il coefficiente di $x$ coincide, perché $B + C = 3.$ Per $x \neq -1$ la frazione si riduce dunque a:

$$\frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} = \frac{5x - 2}{x^2 + 2x + 3}$$

La derivata del nuovo denominatore è $2x + 2.$ Per ottenere questo termine al numeratore scriviamo:

$$5x - 2 = \frac{5}{2}(2x + 2) - 7$$

Separando i contributi, possiamo riscrivere l'integrale iniziale come:

$$\int \frac{5x - 2}{x^2 + 2x + 3} \ dx = \frac{5}{2} \int \frac{2x + 2}{x^2 + 2x + 3} \ dx - 7 \int \frac{1}{x^2 + 2x + 3} \ dx$$

Nel primo integrale il numeratore è la derivata del denominatore, quindi otteniamo $(5/2)\ln(x^2 + 2x + 3).$ Il denominatore è positivo perché $x^2 + 2x + 3 = (x + 1)^2 + 2.$ Questa stessa uguaglianza ci permette di calcolare il secondo integrale ponendo $u = x + 1$ e usando la formula dell'arcotangente con $\rho = \sqrt{2}:$

$$-7 \int \frac{1}{(x + 1)^2 + 2} \ dx = -\frac{7}{\sqrt{2}}\arctan\left(\frac{x + 1}{\sqrt{2}}\right) + k$$

Riunendo i risultati otteniamo:

$$\int \frac{5x^2 + 3x - 2}{(x + 1)(x^2 + 2x + 3)} \ dx = \frac{5}{2}\ln(x^2 + 2x + 3) - \frac{7}{\sqrt{2}}\arctan\left(\frac{x + 1}{\sqrt{2}}\right) + k$$

Il procedimento in questi casi è un po' più complicato dei precedenti, ma non avvilitevi perché avendo a mente la forma finale a cui vogliamo arrivare e operando con metodo le corrette sostituzioni, anche questo genere di integrali diventeranno con l'esperienza abbastanza immediati da calcolare. 

## Fattori quadratici irriducibili ripetuti

Vediamo un'ultima casistica, che alza l'asticella della complicazione, e che riguarda gli integrali il cui denominatore contiene una potenza $q(x)^k$ di un fattore quadratico irriducibile. In questo caso dobbiamo prevedere tutte le potenze da $1$ a $k,$ come abbiamo fatto per i fattori lineari ripetuti. Con $q(x) = x^2 + bx + c$ e $b^2 - 4c < 0,$ la parte corrispondente della scomposizione è:

$$\frac{A_1x + B_1}{q(x)} + \frac{A_2x + B_2}{q(x)^2} + \dots + \frac{A_kx + B_k}{q(x)^k}$$

Ogni numeratore ha grado al massimo $1.$ Per integrare il termine di indice $j$ usiamo la stessa separazione del caso precedente:

$$A_jx + B_j = \frac{A_j}{2}q'(x) + \left(B_j - \frac{A_jb}{2}\right)$$

La parte che contiene $q'(x)$ si calcola con la sostituzione $v = q(x).$ Per $j = 1$ ritroviamo il logaritmo. Per $j \geq 2$ otteniamo invece:

$$\int \frac{q'(x)}{q(x)^j} \ dx = \int v^{-j} \ dv = \frac{q(x)^{1-j}}{1-j} + K$$

Rimane da integrare il termine con numeratore costante. Ponendo ancora $u = x + b/2$ e $\rho = \sqrt{c - b^2/4} > 0,$ lo riconduciamo alla famiglia di integrali:

$$I_j = \int \frac{1}{(u^2 + \rho^2)^j} \ du$$

Il caso $j = 1$ lo abbiamo appena visto, mentre per $j \geq 2$ possiamo abbassare l'esponente con una [formula di riduzione](../reduction-formulas/). Per ricavarla partiamo dalla derivata:

$$
\begin{align}
\frac{d}{du}\left[\frac{u}{(u^2 + \rho^2)^{j-1}}\right] &= \frac{1}{(u^2 + \rho^2)^{j-1}} - \frac{2(j-1)u^2}{(u^2 + \rho^2)^j} \\[6pt]
  &= \frac{2(j-1)\rho^2}{(u^2 + \rho^2)^j} - \frac{2j-3}{(u^2 + \rho^2)^{j-1}}
\end{align}
$$

Nell'ultimo passaggio abbiamo sostituito $u^2 = (u^2 + \rho^2) - \rho^2$ e raccolto i termini con lo stesso denominatore. Integrando l'identità e isolando $I_j$ otteniamo:

$$I_j = \frac{u}{2(j-1)\rho^2(u^2 + \rho^2)^{j-1}} + \frac{2j-3}{2(j-1)\rho^2}I_{j-1} \qquad (j \geq 2)$$

Ogni applicazione riduce l'indice di uno, quindi dopo $j - 1$ passaggi arriviamo a questa forma:

$$I_1 = \frac{1}{\rho}\arctan\left(\frac{u}{\rho}\right) + K$$

Ad esempio, per $j = 2$ basta una sola applicazione della formula e troviamo:

$$I_2 = \frac{u}{2\rho^2(u^2 + \rho^2)} + \frac{1}{2\rho^3}\arctan\left(\frac{u}{\rho}\right) + k$$

Questa espressione descrive le primitive di $1/(u^2 + \rho^2)^2$ su tutto $\mathbb{R},$ perché $\rho > 0$ e il denominatore non si annulla.

Questi casi possono risultare piuttosto laboriosi, soprattutto quando la molteplicità del fattore quadratico è elevata, perché occorre determinare più coefficienti e applicare più volte la formula di riduzione. Ci limitiamo quindi all'applicazione con $j = 2,$ che mostra come usare la formula. Un ulteriore esempio riprenderebbe la scomposizione e le sostituzioni già illustrate in precedenza, aggiungendo soprattutto passaggi algebrici senza introdurre nuove tecniche di integrazione.
