---
title: The Weierstrass Substitution
source: https://algebrica.org/the-weierstrass-substitution/
license: CC BY-NC 4.0
tags:
  - arctangent
  - half-angle-substitution
  - indefinite-integral
  - integration-by-substitution
  - partial-fractions
  - rational-functions
  - trigonometric-identities
  - trigonometric-integrals
  - weierstrass-substitution
---
## La classe di integrali da trattare

Molti integrali che si incontrano nei corsi introduttivi di analisi contengono una [funzione razionale](../rational-functions/) la cui variabile è a sua volta una combinazione di seno e coseno. Le seguenti espressioni hanno una struttura comune:

$$\frac{1}{1 + \sin x} \qquad \frac{1}{5 - 3\cos x} \qquad \frac{1}{\sin x + \cos x}$$

Il numeratore e il denominatore sono [polinomi](../polynomials/) in $\sin x$ e $\cos x.$ Le tecniche sviluppate per gli [integrali di funzioni trigonometriche](../integral-of-trigonometric-functions/), basate sulle formule di riduzione delle potenze o sulla separazione di un fattore dagli altri, non forniscono un procedimento uniforme per integrande di questo tipo. Occorre un unico cambio di variabile che trasformi ogni espressione razionale in $\sin x$ e $\cos x$ in una funzione razionale della nuova variabile. Il problema si riduce così all'[integrazione di una funzione razionale](../integral-of-rational-functions/), che si affronta mediante la divisione tra polinomi e la [scomposizione in fratti semplici](../partial-fraction-decomposition/).

La sostituzione che permette questa trasformazione si basa sull'angolo metà $x/2$ e utilizza in un solo passaggio le identità algebriche che legano [tangente](../tangent-and-cotangent/), [seno e coseno](../sine-and-cosine/).

## La sostituzione $t = \tan(x/2)$

Introduciamo la nuova variabile mediante l'equazione:

$$t = \tan\left(\frac{x}{2}\right) \tag{1}$$

Limitiamo per il momento l'[angolo](../angles-and-angular-measure/) $x$ all'[intervallo](../intervals/) aperto $(-\pi, \pi),$ in modo che $\tan(x/2)$ sia ben definita e l'applicazione $x \mapsto t$ sia una biiezione sulla retta reale. Si recupera la variabile originaria mediante la relazione inversa $x = 2\arctan t,$ che utilizza la funzione [arcotangente](../arctangent-and-arccotangent/) e permette di esprimere nuovamente il risultato in funzione di $x.$

La sostituzione consente di esprimere $\sin x,$ $\cos x$ e il differenziale $dx$ come espressioni razionali in $t.$ Per ricavare queste espressioni si utilizzano le formule di duplicazione e l'[identità fondamentale della trigonometria](../pythagorean-identity/) $\sin^2\theta + \cos^2\theta = 1.$

## Espressioni del seno, del coseno e del differenziale

Partiamo dalla [formula di duplicazione](../trigonometric-identities/) del seno:

$$\sin x = 2\sin\left(\frac{x}{2}\right)\cos\left(\frac{x}{2}\right)$$

Scrivendo il secondo membro come $2\tan(x/2)\cos^2(x/2)$ e utilizzando l'identità $\cos^2(x/2) = 1/(1 + \tan^2(x/2)),$ otteniamo la seguente espressione del seno:

$$\sin x = \frac{2t}{1 + t^2} \tag{2}$$

La formula di duplicazione del coseno è $\cos x = \cos^2(x/2) - \sin^2(x/2).$ Scriviamo il secondo membro come una frazione con denominatore $1 = \cos^2(x/2) + \sin^2(x/2).$ Dividendo il numeratore e il denominatore per $\cos^2(x/2),$ otteniamo:

$$\cos x = \frac{1 - t^2}{1 + t^2} \tag{3}$$

Per calcolare il differenziale, deriviamo la relazione $t = \tan(x/2)$ rispetto a $x$:

$$\frac{dt}{dx} = \frac{1}{2}\sec^2\left(\frac{x}{2}\right) = \frac{1}{2}\left(1 + \tan^2\left(\frac{x}{2}\right)\right) = \frac{1 + t^2}{2}$$

Ricavando $dx$ otteniamo la terza identità su cui si basa la sostituzione:

$$dx = \frac{2}{1 + t^2} \ dt \tag{4}$$

Le formule $(2),$ $(3)$ e $(4)$ permettono di applicare il metodo. Sostituendole in un integrale di una qualsiasi espressione razionale in $\sin x$ e $\cos x,$ si ottiene un integrale di una funzione razionale in $t.$ Quest'ultimo si calcola con le tecniche già sviluppate per le funzioni razionali, mediante la divisione tra polinomi, la scomposizione in fratti semplici e l'integrazione dei termini elementari.

> Il fattore $2/(1+t^2)$ introdotto dal differenziale è il doppio della derivata di $\arctan t,$ in accordo con la relazione inversa $x = 2\arctan t$ tra le due variabili. La presenza di $1 + t^2$ nelle formule è legata a questa relazione.

## Esempio 1

Consideriamo l'integrale:

$$\int \frac{dx}{1 + \sin x}$$

Applicando la sostituzione e utilizzando l'identità $(2),$ il denominatore diventa:

$$
\begin{align}
1 + \sin x &= 1 + \frac{2t}{1+t^2} \\[6pt]
           &= \frac{1 + t^2 + 2t}{1+t^2} \\[6pt]
           &= \frac{(1+t)^2}{1+t^2}
\end{align}
$$

Combinando questa espressione con il differenziale $(4),$ otteniamo:

$$
\begin{align}
\frac{1}{1+\sin x} \ dx &= \frac{1+t^2}{(1+t)^2} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                       &= \frac{2}{(1+t)^2} \ dt
\end{align}
$$

Il fattore $1 + t^2$ si semplifica e rimane un integrale nella sola variabile $t.$ La [primitiva](../indefinite-integrals/) si calcola direttamente:

$$\int \frac{2}{(1+t)^2} \ dt = -\frac{2}{1+t} + c$$

Tornando alla variabile originaria mediante l'identità $t = \tan(x/2),$ otteniamo il risultato:

$$\int \frac{dx}{1 + \sin x} = -\frac{2}{1 + \tan(x/2)} + c$$

> Il risultato si verifica derivando l'espressione ottenuta, che restituisce l'integranda originaria dopo un breve calcolo.

## Esempio 2

Consideriamo l'integrale:

$$\int \frac{dx}{5 - 3\cos x}$$

Utilizzando l'identità $(3),$ il denominatore assume la forma:

$$
\begin{align}
5 - 3\cos x &= 5 - 3 \cdot \frac{1 - t^2}{1+t^2} \\[6pt]
            &= \frac{5(1+t^2) - 3(1-t^2)}{1+t^2} \\[6pt]
            &= \frac{2 + 8t^2}{1+t^2} \\[6pt]
            &= \frac{2(1 + 4t^2)}{1+t^2}
\end{align}
$$

Combinando questa espressione con il differenziale $(4),$ otteniamo:

$$
\begin{align}
\frac{1}{5-3\cos x} \ dx &= \frac{1+t^2}{2(1+4t^2)} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                        &= \frac{dt}{1 + 4t^2}
\end{align}
$$

Anche in questo caso il fattore $1 + t^2$ si semplifica. L'integrale rimanente si riconduce alla forma elementare che ha per primitiva un'arcotangente, poiché $1 + 4t^2 = 1 + (2t)^2.$ Ponendo $u = 2t,$ da cui $du = 2 \ dt,$ l'integrale diventa:

$$
\begin{align}
\int \frac{dt}{1 + 4t^2} &= \frac{1}{2}\int \frac{du}{1 + u^2} \\[6pt]
                        &= \frac{1}{2}\arctan u + c \\[6pt]
                        &= \frac{1}{2}\arctan(2t) + c
\end{align}
$$

Tornando alla variabile $x,$ otteniamo la primitiva:

$$\int \frac{dx}{5 - 3\cos x} = \frac{1}{2}\arctan(2\tan(x/2)) + c$$

> Il procedimento seguito è tipico del metodo. Dopo la sostituzione, l'integranda diventa una funzione razionale in $t.$ La sua primitiva può contenere arcotangenti e logaritmi, che compaiono nell'integrazione delle funzioni razionali.

## Esempio 3

Consideriamo l'integrale:

$$\int \frac{dx}{2 + \sin x}$$

Applicando la sostituzione al denominatore, otteniamo:

$$
\begin{align}
2 + \sin x &= 2 + \frac{2t}{1+t^2} \\[6pt]
           &= \frac{2(1+t^2) + 2t}{1+t^2} \\[6pt]
           &= \frac{2(t^2 + t + 1)}{1+t^2}
\end{align}
$$

L'espressione da integrare diventa quindi:

$$
\begin{align}
\frac{1}{2+\sin x} \ dx &= \frac{1+t^2}{2(t^2+t+1)} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                       &= \frac{dt}{t^2+t+1}
\end{align}
$$

Completando il quadrato al denominatore, otteniamo:

$$t^2 + t + 1 = \left(t + \frac{1}{2}\right)^2 + \frac{3}{4}$$

L'integrale assume ora la forma:

$$\int \frac{dt}{\left(t+\frac{1}{2}\right)^2 + \frac{3}{4}}$$

Questa espressione corrisponde alla forma elementare $\int du/(u^2 + a^2)$ con $u = t + 1/2$ e $a = \sqrt{3}/2.$ Utilizzando la relativa formula di integrazione, otteniamo:

$$\int \frac{dt}{t^2+t+1} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2t+1}{\sqrt{3}}\right) + c$$

Sostituendo nuovamente $t = \tan(x/2),$ otteniamo l'espressione finale:

$$\int \frac{dx}{2+\sin x} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2\tan(x/2)+1}{\sqrt{3}}\right) + c$$

> I tre esempi illustrano il comportamento tipico del metodo. Dopo la sostituzione, l'integranda è una funzione razionale in $t$ e la primitiva è una combinazione di funzioni razionali, arcotangenti e logaritmi nella nuova variabile. Alla fine si torna alla variabile originaria mediante l'identità $t = \tan(x/2).$

## Condizioni sul dominio

La sostituzione $t = \tan(x/2)$ è definita per ogni $x$ tale che $x/2 \neq \pi/2 + k\pi,$ cioè per ogni $x \notin \pi + 2\pi\mathbb{Z}.$ L'applicazione $x \mapsto t$ è una biiezione liscia da ciascun intervallo aperto $((2k-1)\pi, (2k+1)\pi)$ sull'intera retta reale. Quando si calcola un [integrale indefinito](../indefinite-integrals/), le formule ottenute valgono negli intervalli in cui sono definite sia la sostituzione sia l'integranda, e la costante di integrazione può assumere valori diversi su intervalli diversi.

La situazione richiede maggiore attenzione per un [integrale definito](../definite-integrals/) i cui estremi appartengono a intervalli fondamentali diversi. In questo caso si applica la sostituzione separatamente su ciascuna parte del [dominio](../determining-the-domain-of-a-function/) di integrazione in cui essa è regolare, per poi sommare i contributi ottenuti. Applicare meccanicamente la sostituzione attraverso un punto della forma $x = (2k+1)\pi$ porta a risultati errati, poiché la sostituzione non è definita in quel punto.

> Occorre inoltre scegliere correttamente il ramo della funzione inversa. La relazione $x = 2\arctan t$ manda la retta reale nell'intervallo aperto $(-\pi, \pi).$ Sugli altri intervalli fondamentali la relazione inversa è $x = 2\arctan t + 2k\pi.$ Un'espressione della primitiva che contiene $\arctan(\cdots\tan(x/2)\cdots)$ può presentare salti nei punti $x = (2k+1)\pi,$ la cui ampiezza dipende dall'espressione ottenuta. Quando l'integranda è continua attraverso questi punti e si richiede una primitiva continua su tutto il dominio, occorre scegliere opportunamente le costanti di integrazione sui diversi intervalli ed estendere la primitiva per continuità.

## Quando preferire altre tecniche

La sostituzione di Weierstrass si applica sempre alle integrande razionali in seno e coseno, ma non è sempre il metodo più efficiente. Quando l'integranda contiene soltanto potenze pari di $\sin x$ e $\cos x,$ oppure si può riscrivere mediante le identità $\sin^2 x = (1 - \cos 2x)/2$ e $\cos^2 x = (1 + \cos 2x)/2,$ la sostituzione dell'angolo metà introduce complicazioni algebriche superflue. Analogamente, quando l'integranda ha la forma $R(\sin x)\cos x$ oppure $R(\cos x)\sin x,$ le [sostituzioni](../integration-by-substitution/) dirette $u = \sin x$ oppure $u = \cos x$ sono più rapide, poiché evitano del tutto la razionalizzazione.

Come criterio pratico, quando l'integranda è una funzione razionale di $\sin x$ e $\cos x$ che non ammette semplificazioni evidenti mediante [identità trigonometriche](../trigonometric-identities/) o sostituzioni dirette, conviene ricorrere alla sostituzione di Weierstrass. Negli altri casi, le tecniche più semplici permettono calcoli più brevi.
