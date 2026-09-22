---
title: Reduction Formulas for Integrals
source: https://algebrica.org/reduction-formulas/
license: CC BY-NC 4.0
tags:
  - definite-integral
  - indefinite-integral
  - integration-by-parts
  - integration-techniques
  - recurrence-relations
  - reduction-formulas
---
## Introduzione

Le formule di riduzione per gli integrali che introdurremo tra un istante possono fare la differenza nella risoluzione agevole di integrali che, a prima vista, non appaiono particolarmente amichevoli. La loro applicazione è utile per la risoluzione di alcuni integrali che presentano l'esponenziale o alcune funzioni trigonometriche. 

In generale, prima di introdurre le formule, è necessario specificare che si possono identificare delle famiglie di integrali attraverso un indice $I_n.$ Tale indice è funzionale ad agevolare i calcoli, ricorrendo all'esponente generico. Nel seguito $n$ indica sempre un intero non negativo, salvo le restrizioni più forti specificate per una singola famiglia. Prendete ad esempio i due seguenti integrali:

$$\int \sin^3 x dx \quad \text{o} \quad \int \sin^5 x dx$$

Possiamo raggrupparli nell'unica seguente famiglia:

$$I_n=\int\sin^nx \ dx$$

Questa generalizzazione consente di svolgere i calcoli una sola volta, considerando l'integrale con l'esponente $n$ e senza dover rifare i calcoli per il caso con l'esponente $n=3$ o $n=5.$ Come intuite, questo modo di procedere è piuttosto utile perché riduce significativamente il carico di calcoli nei problemi che coinvolgono questo tipo di integrali. 

Le formule di riduzione considerate in questo post hanno la forma:

$$I_n=g_n(x)+\lambda_nI_{n-k} \tag{1}$$

+ Il termine $g_n(x)$ è la parte già integrata
+ Il coefficiente $\lambda_n$ dipende dall'indice ma non dalla variabile
+ L'intero $k\geq1$ è il passo della riduzione dell'indice. 

Nel seguito ogni uguaglianza tra integrali indefiniti è intesa modulo una costante additiva. In modo equivalente, per ciascuna famiglia scegliamo primitive compatibili con la ricorrenza e aggiungiamo la costante arbitraria soltanto al risultato finale.

Il metodo per procedere sarà immediatamente chiaro nei seguenti paragrafi. Tuttavia, come nella maggior parte della matematica, non è però sempre tutto così bello come può apparire nelle premesse. In genere conviene ricorrere a una formula di riduzione quando l'esponente è abbastanza alto da rendere lunga l'integrazione per parti o una qualunque manipolazione diretta, mentre per esponenti bassi non è sempre indicata.

## Potenze di $x$ per un esponenziale, $\sin x$ e $\cos x$  

Partiamo dalla famiglia di integrali che si presentano come prodotti di potenze di $x$ per un [esponenziale](../integral-of-the-exponential-function/) e la identifichiamo con $J_n$:

$$J_n=\int x^ne^{ax} \ dx \qquad a\neq0, \quad n\geq0$$

Il fattore $e^{ax}$ ha una primitiva immediata, mentre la potenza di $x$ si abbassa derivando, quindi ricorriamo ad una sostituzione ponendo $u=x^n$ e $dv=e^{ax} \ dx.$ Da qui otteniamo $du=nx^{n-1} \ dx$ e $v=e^{ax}/a,$ e la formula per parti dà:

$$J_n=\frac{x^ne^{ax}}{a}-\frac{n}{a}J_{n-1} \qquad n\geq1 \tag{2}$$

Il caso base per $n=0$ è $J_0=e^{ax}/a.$ Calcoliamo per esempio il seguente integrale:

$$\int x^3e^x \ dx$$ 
Se applichiamo la relazione $(2)$ iterativamente otteniamo:

$$
\begin{align}
J_3 &= x^3e^x-3J_2 \\[6pt]
J_2 &= x^2e^x-2J_1 \\[6pt]
J_1 &= xe^x-J_0 \\[6pt]
J_0 &= e^x
\end{align}
$$

Risalendo dal fondo troviamo $J_1=xe^x-e^x$ e poi $J_2=x^2e^x-2xe^x+2e^x.$ Sostituendo nella prima riga e raccogliendo l'esponenziale otteniamo che l'integrale di partenza è pari a:

$$\int x^3e^x \ dx=e^x(x^3-3x^2+6x-6)+c$$

Per $n$ generico si ottiene la forma chiusa, con i coefficienti che sono dati dai rapporti fra fattoriali prodotti dalle derivate successive della potenza:

$$\int x^ne^{ax} \ dx=e^{ax}\sum_{k=0}^{n}(-1)^k\frac{n!}{(n-k)!}\frac{x^{n-k}}{a^{k+1}}+c \tag{3}$$

- - -

Con seno o coseno al posto dell'esponenziale la situazione cambia leggermente. Ponendo $u=x^n$ e $dv=\sin x \ dx$ nell'integrale compare il coseno, e serve una seconda integrazione per parti per tornare al seno:

$$\int x^n\sin x \ dx=-x^n\cos x+nx^{n-1}\sin x-n(n-1)\int x^{n-2}\sin x \ dx \qquad n\geq2$$

I casi base sono ora due: per $n$ pari la catena termina su $\int\sin x \ dx,$ per $n$ dispari su $\int x\sin x \ dx.$

## Potenze del seno e del coseno

Vediamo adesso un altro caso che riguarda le potenze intere del seno. Definiamo la nostra famiglia come $S_n$ e la identifichiamo come segue:

$$S_n=\int\sin^nx \ dx \qquad n\geq0$$

Scriviamo l'integranda come $\sin^{n-1}x\cdot\sin x$ e poniamo $u=\sin^{n-1}x$ e $dv=\sin x \ dx,$ da cui $du=(n-1)\sin^{n-2}x\cos x \ dx$ e $v=-\cos x.$ La formula per parti ci consente di riscrivere l'integrale come:

$$S_n=-\sin^{n-1}x\cos x+(n-1)\int\sin^{n-2}x\cos^2x \ dx$$

L'integrale a destra non appartiene alla famiglia, perché contiene un quadrato del coseno. Facendo ricorso all'identità fondamentale trigonometrica $\cos^2x=1-\sin^2x$ lo dividiamo in due integrali che invece vi appartengono, rispettivamente di indice $n-2$ e di indice $n$:

$$S_n=-\sin^{n-1}x\cos x+(n-1)S_{n-2}-(n-1)S_n$$

Risolvendo rispetto a $S_n$ portiamo a sinistra il termine $(n-1)S_n$ e dividendo per $n$ otteniamo:

$$S_n=-\frac{\sin^{n-1}x\cos x}{n}+\frac{n-1}{n}S_{n-2} \qquad n\geq2 \tag{4}$$

Il calcolo è analogo per il coseno, cambiando però $u=\cos^{n-1}x$ e $dv=\cos x \ dx.$ Da questo otteniamo una relazione omologa alla $(4)$:

$$C_n=\int\cos^nx \ dx=\frac{\cos^{n-1}x\sin x}{n}+\frac{n-1}{n}C_{n-2} \qquad n\geq2 \tag{5}$$

Determiniamo adesso i due casi base per ciascuna famiglia. Per il seno abbiamo $S_0=x$ e $S_1=-\cos x,$ mentre per il coseno $C_0=x$ e $C_1=\sin x.$ Applichiamo la $(4)$ a $\int\sin^4x \ dx,$ dove il primo passo porta all'indice due e il secondo all'indice zero:

$$
\begin{align}
S_4 &= -\frac{\sin^3x\cos x}{4}+\frac{3}{4}S_2 \\[6pt]
S_2 &= -\frac{\sin x\cos x}{2}+\frac{1}{2}S_0 \\[6pt]
S_0 &= x
\end{align}
$$

Sostituendo $S_2$ nella prima riga e riordinando i termini si ottiene la primitiva:

$$\int\sin^4x \ dx=-\frac{\sin^3x\cos x}{4}-\frac{3\sin x\cos x}{8}+\frac{3x}{8}+c$$

Per gli esponenti dispari la $(4)$ resta valida, ma conviene isolare un fattore e usare l'identità fondamentale trigonometrica per esprimere il resto in funzione del coseno, riducendo l'integrale a una [sostituzione](../integration-by-substitution/) che si chiude in un passo, come mostrato fra gli [integrali delle funzioni trigonometriche](../integral-of-trigonometric-functions/). Nota: la formula di riduzione serve soprattutto per gli esponenti pari, dove il ricorso all'identità fondamentale non abbassa l'esponente.

## Potenze della tangente e del logaritmo

Vediamo adesso il caso delle potenze della tangente per cui basta l'uso di un'identità algebrica. In questo caso non si utilizza l'integrazione per parti. Consideriamo ad esempio la seguente famiglia:

$$T_n=\int\tan^nx \ dx \qquad n\geq0$$

Sostituiamo $\tan^2x=\sec^2x-1,$ che è l'identità fondamentale trigonometrica divisa per $\cos^2x$ e otteniamo:

$$
\begin{align}
T_n &= \int\tan^{n-2}x(\sec^2x-1) \ dx \\[6pt]
    &= \int\tan^{n-2}x\sec^2x \ dx-T_{n-2}
\end{align}
$$

Il primo integrale è immediato con la sostituzione $u=\tan x,$ perché $\sec^2x$ è la derivata della tangente. Otteniamo quindi:

$$T_n=\frac{\tan^{n-1}x}{n-1}-T_{n-2} \qquad n\geq2 \tag{6}$$

I casi base sono $T_0=x$ e $T_1=-\ln|\cos x|.$ Il coefficiente della $(6)$ vale $-1$ e non dipende dall'indice, quindi i termini della catena si alternano di segno e la primitiva è una somma a segni alterni di potenze della tangente, chiusa da $x$ oppure dal logaritmo secondo la parità di $n.$ Per $n=4$ la discesa dà $T_4=\tan^3x/3-T_2$ e poi $T_2=\tan x-T_0,$ da cui:

$$\int\tan^4x \ dx=\frac{\tan^3x}{3}-\tan x+x+c$$

- - -

Le potenze del [logaritmo](../logarithms/) tornano invece all'integrazione per parti. Definiamo intanto la nostra famiglia nel seguente modo:

$$L_n=\int\ln^nx \ dx \qquad n\geq0$$

Qui il fattore da integrare è il fattore assente, cioè $dv=dx,$ mentre $u=\ln^nx$ è la parte che si deriva. Da $v=x$ e $du=n\ln^{n-1}x/x \ dx$ segue che la $x$ prodotta da $v$ semplifica il denominatore della derivata, e resta:

$$L_n=x\ln^nx-nL_{n-1} \qquad n\geq1 \tag{7}$$

Il caso base è $L_0=x.$ La discesa ha la stessa struttura della $(2).$ Per $n=3$ si ottiene la catena $L_3=x\ln^3x-3L_2,$ $L_2=x\ln^2x-2L_1,$ $L_1=x\ln x-x,$ da cui:

$$\int\ln^3x \ dx=x\ln^3x-3x\ln^2x+6x\ln x-6x+c$$

Notate come i coefficienti $1,3,6,6$ sono gli stessi che compaiono nell'esempio dell'esponenziale, e la coincidenza non è casuale. La sostituzione $x=e^t$ infatti trasforma $dx$ in $e^t \ dt$ e $\ln^nx$ in $t^n,$ quindi trasforma $L_n$ esattamente in $J_n$ con $a=1.$ Le due famiglie sono la stessa famiglia scritta in due variabili diverse, e le relazioni $(2)$ e $(7)$ si corrispondono sotto quella sostituzione.

## Le potenze del denominatore quadratico

L'ultima famiglia che vedremo è quella che serve all'integrazione delle [funzioni razionali](../integral-of-rational-functions/) e ha una struttura diversa dalle precedenti. Il procedimento è più complicato ma vale la pena illustrarlo perché integrali di questo tipo sono abbastanza comuni:

$$I_n=\int\frac{dx}{(x^2+a^2)^n} \qquad a\neq0, \quad n\geq1$$

Il caso base richiama l'[arcotangente](../arctangent-function/) ed è:


$$I_1=\frac{1}{a}\arctan\frac{x}{a}$$

Si pone $u=(x^2+a^2)^{-n}$ e $dv=dx,$ quindi $v=x$ e $du=-2nx(x^2+a^2)^{-n-1} \ dx.$ La formula per parti produce:

$$I_n=\frac{x}{(x^2+a^2)^n}+2n\int\frac{x^2}{(x^2+a^2)^{n+1}} \ dx$$

L'integrale a destra si riporta alla famiglia scrivendo $x^2=(x^2+a^2)-a^2$ e separando la frazione in due termini. Il primo semplifica una potenza del denominatore e riproduce $I_n,$ il secondo dà $I_{n+1}$ ottenendo:

$$\int\frac{x^2}{(x^2+a^2)^{n+1}} \ dx=I_n-a^2I_{n+1}$$

Sostituendo e raccogliendo i termini in $I_n$ otteniamo:

$$I_n=x(x^2+a^2)^{-n}+2nI_n-2na^2I_{n+1}$$ 

Risolvendo l'espressione rispetto all'indice più alto otteniamo la formula di riduzione:

$$I_{n+1}=\frac{1}{2na^2}\left[\frac{x}{(x^2+a^2)^n}+(2n-1)I_n\right] \tag{8}$$

Tenete a mente che questa è l'unica relazione fra quelle viste che si legge verso l'alto, perché l'integrazione per parti applicata a una potenza negativa ne alza il modulo invece di abbassarlo. Riscrivendola quindi con l'indice traslato si ottiene la forma discendente, valida per $n\geq2$:

$$I_n=\frac{1}{2(n-1)a^2}\left[\frac{x}{(x^2+a^2)^{n-1}}+(2n-3)I_{n-1}\right]$$

In entrambe le letture la catena si chiude su $I_1,$ cioè sull'arcotangente. Il primo passo dà il valore più ricorrente:

$$I_2=\frac{x}{2a^2(x^2+a^2)}+\frac{1}{2a^3}\arctan\frac{x}{a}+c$$

La $(8)$ completa la decomposizione in fratti semplici nel caso di un fattore quadratico irriducibile ripetuto. Quando il denominatore contiene $(x^2+bx+c)^k$ con discriminante negativo, la decomposizione porta un termine per ogni potenza del fattore, da uno a $k,$ ciascuno con numeratore di primo grado:

$$\frac{A_1x+B_1}{x^2+bx+c}+\frac{A_2x+B_2}{(x^2+bx+c)^2}+\dots+\frac{A_kx+B_k}{(x^2+bx+c)^k}$$

Ogni numeratore si scrive come multiplo della derivata del denominatore più una costante. La parte proporzionale alla derivata si integra per sostituzione e dà una potenza del denominatore, oppure un logaritmo quando l'esponente è uno. La parte costante è invece un integrale della famiglia $I_j,$ che si raggiunge completando il quadrato, poiché la sostituzione $u=x+b/2$ porta il denominatore nella forma $u^2+a^2$ con $a^2=c-b^2/4,$ positivo perché il discriminante è negativo.

Facciamo un esempio per rendere chiaro il concetto. Prendete il seguente caso: con $j=2,$ il numeratore contiene già la derivata del denominatore più una costante, quindi la separazione dell'integrale in due integrali è immediata:

$$\int\frac{2x+3}{(x^2+4)^2} \ dx=\int\frac{2x}{(x^2+4)^2} \ dx+3\int\frac{dx}{(x^2+4)^2}$$

Il primo integrale si calcola con $u=x^2+4,$ che manda $2x \ dx$ in $du$ e lascia $\int u^{-2} \ du=-1/u.$ Il secondo è $3I_2$ con $a=2,$ e dalla formula appena ricavata otteniamo: 

$$I_2=x/\big(8(x^2+4)\big)+\frac{1}{16}\arctan(x/2).$$

Sommando i due contributi e riducendo allo stesso denominatore i termini razionali si ottiene:

$$\int\frac{2x+3}{(x^2+4)^2} \ dx=\frac{3x-8}{8(x^2+4)}+\frac{3}{16}\arctan\frac{x}{2}+c$$

## Ricorrenze sull'integrale definito

Consideriamo il seguente caso di integrale definito:

$$\int_a^b u \ dv=\Big[uv\Big]_a^b-\int_a^b v \ du$$

Ogni formula di riduzione diventa una sorta di relazione fra numeri, in cui il termine $g_n$ della $(1)$ compare come differenza tra il termine valutato in $b$ e lo stesso termine valutato in $a.$ Quando questo termine si annulla la ricorrenza ha coefficienti puramente numerici e l'intera famiglia è determinata dai soli casi base.

L'esempio classico è la potenza del seno nell'intervallo $[0,\pi/2].$ Il termine elementare della $(4)$ è $-\sin^{n-1}x\cos x/n,$ che si annulla in $0$ per il fattore seno e in $\pi/2$ per il fattore coseno, quindi la relazione si riduce a:

$$\int_0^{\pi/2}\sin^nx \ dx=\frac{n-1}{n}\int_0^{\pi/2}\sin^{n-2}x \ dx \qquad n\geq2 \tag{9}$$

I due casi base sono $\int_0^{\pi/2}dx=\pi/2$ e $\int_0^{\pi/2}\sin x \ dx=1.$ La discesa conserva la parità dell'indice, quindi il valore per $n$ pari eredita il fattore $\pi/2,$ mentre per $n$ dispari è un numero razionale. Per $n=4$ e $n=5$ ad esempio otteniamo:

$$\int_0^{\pi/2}\sin^4x \ dx=\frac{3}{4}\cdot\frac{1}{2}\cdot\frac{\pi}{2}=\frac{3\pi}{16} \qquad \int_0^{\pi/2}\sin^5x \ dx=\frac{4}{5}\cdot\frac{2}{3}=\frac{8}{15}$$

La sostituzione $x = \pi/2-x$ scambia seno e coseno e lascia fisso l'intervallo, quindi i due integrali definiti coincidono per ogni $n$ e la relazione $(5)$ produce sugli stessi estremi la medesima successione di valori.

> I numeri definiti dalla $(9)$ sono detti integrali di Wallis. La loro monotonia, il comportamento asintotico e il prodotto infinito che se ne ricava riguardano la successione in quanto tale e non la tecnica di integrazione, quindi appartengono a una trattazione separata.
