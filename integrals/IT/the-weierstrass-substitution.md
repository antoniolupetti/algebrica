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

La sostituzione di Weierstrass è un metodo che consente di risolvere integrali non immediati in cui l'integranda è una funzione razionale contenente seno e coseno, mediante un opportuno cambio di variabile. In genere, questo tipo di integrali si presenta in forme simili a quelle elencate di seguito, dove il numeratore e il denominatore sono polinomi in $\sin x$ e $\cos x:$

$$\frac{1}{1 + \sin x} \qquad \frac{1}{5 - 3\cos x} \qquad \frac{1}{\sin x + \cos x} \tag{1}$$

Abbiamo già affrontato alcune tecniche per risolvere gli integrali delle funzioni trigonometriche, basate sulle formule di riduzione delle potenze o di separazione tra fattori, che tuttavia, in casi come quelli della $(1)$ non forniscono un procedimento utile per trovare un risultato in modo agevole. Nei casi che tratteremo tra poco, occorre effettuare un cambio di variabile che riduca il problema all'integrazione di una funzione razionale semplice che si affronta in genere con la divisione tra polinomi e la scomposizione in fratti semplici.

La sostituzione di Weierstrass si basa sull'introduzione della seguente variabile:
$$t = \tan\left(\frac{x}{2}\right) \tag{2}$$

Questa sostituzione consente di esprimere $\sin x,$ $\cos x$ e il differenziale $dx$ come espressioni razionali in $t.$ Per ricavare queste espressioni, come vedremo tra un attimo, si utilizzano le formule di duplicazione e l'[identità fondamentale della trigonometria](../pythagorean-identity/). Una volta calcolata la primitiva in $t,$ si torna alla variabile $x$ originaria sostituendo $t = \tan(x/2).$

Per prima cosa vediamo come si derivano le espressioni del seno, del coseno e del differenziale. Vi anticipo subito che sarà necessario un piccolo sforzo mnemonico per richiamare le varie identità trigonometriche che richiameremo nei calcoli, per cui prima di procedere vi invito a consultare la relativa pagina. Per il seno, partiamo dalla [formula di duplicazione](../trigonometric-identities/) per cui si ha:

$$\sin x = 2\sin\left(\frac{x}{2}\right)\cos\left(\frac{x}{2}\right) \tag{3}$$

Moltiplicando per $\cos(x/2) / \cos(x/2)$ possiamo riscrivere il secondo membro come:

$$2\tan\left(\frac{x}{2}\right)\cos^2\left(\frac{x}{2}\right) \tag{4}$$

Per il coseno vale la seguente identità trigonometrica:

$$\cos^2\left(\frac{x}{2}\right) = \frac{1}{1 + \tan^2(x/2)}$$

Sostituendola alla $(4)$ possiamo riscrivere il seno nella $(3)$ come:

$$\sin x = \frac{2t}{1 + t^2} \tag{5}$$

- - -

Un procedimento simile si applica alla derivazione dell'espressione del coseno, utilizzando la relativa formula di duplicazione:

$$\cos x = \cos^2\left(\frac{x}{2}\right) - \sin^2\left(\frac{x}{2}\right)$$

Dividiamo il secondo membro per $\cos^2(x/2) + \sin^2(x/2)$ e dividendo il numeratore e il denominatore per $\cos^2(x/2),$ otteniamo:

$$\cos x = \frac{1 - t^2}{1 + t^2} \tag{6}$$

- - -

Calcoliamo infine il differenziale, derivando la relazione $(2)$ rispetto a $x.$ In questo modo abbiamo:

$$\frac{dt}{dx} = \frac{1}{2}\sec^2\left(\frac{x}{2}\right) = \frac{1}{2}\left(1 + \tan^2\left(\frac{x}{2}\right)\right) = \frac{1 + t^2}{2}$$

Ricavando $dx$ otteniamo la terza identità su cui si basa la sostituzione che è pari a:

$$dx = \frac{2}{1 + t^2} \ dt \tag{7}$$

Le formule $(5),$ $(6)$ e $(7)$ appena ricavate permettono di applicare quindi il metodo di Weierstrass, sostituendole in un integrale di una qualsiasi espressione razionale in $\sin x$ e $\cos x$ nella più semplice variabile $t$. Quindi riepilogando le sostituzioni da applicare sono le seguenti:

[class="table-1"]

|          |                         |
| -------- | ----------------------- |
| $\sin x$ | $\dfrac{2t}{1+t^2}$     |
| $\cos x$ | $\dfrac{1-t^2}{1+t^2}$  |
| $dx$     | $\dfrac{2}{1+t^2} \ dt$ |

[/class]

## Applicazioni pratiche

Facciamo alcuni esempi per illustrare in pratica come il metodo di Weierstrass viene applicato. Consideriamo il seguente integrale, rappresentato da un'integranda razionale nella funzione seno:

$$\int \frac{dx}{1 + \sin x}$$

Utilizzando l'identità $(5),$ possiamo riscrivere il denominatore come segue:

$$
\begin{align}
1 + \sin x &= 1 + \frac{2t}{1+t^2} \\[6pt]
           &= \frac{1 + t^2 + 2t}{1+t^2} \\[6pt]
           &= \frac{(1+t)^2}{1+t^2}
\end{align}
$$

Riscriviamo adesso il differenziale utilizzando la $(7),$ e otteniamo:

$$
\begin{align}
\frac{1}{1+\sin x} \ dx &= \frac{1+t^2}{(1+t)^2} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                       &= \frac{2}{(1+t)^2} \ dt
\end{align}
$$

Otteniamo così un'integranda immediata la cui [primitiva](../indefinite-integrals/) si calcola direttamente:

$$\int \frac{2}{(1+t)^2} \ dt = -\frac{2}{1+t} + c$$

A questo punto, tornando alla variabile originaria mediante l'identità $t = \tan(x/2),$ otteniamo il risultato:

$$\int \frac{dx}{1 + \sin x} = -\frac{2}{1 + \tan(x/2)} + c$$

- - -

Consideriamo adesso il seguente integrale, la cui integranda è una funzione razionale in coseno:

$$\int \frac{dx}{5 - 3\cos x}$$

Utilizzando l'identità $(6),$ possiamo riscrivere il denominatore come:

$$
\begin{align}
5 - 3\cos x &= 5 - 3 \cdot \frac{1 - t^2}{1+t^2} \\[6pt]
            &= \frac{5(1+t^2) - 3(1-t^2)}{1+t^2} \\[6pt]
            &= \frac{2 + 8t^2}{1+t^2} \\[8pt]
            &= \frac{2(1 + 4t^2)}{1+t^2}
\end{align}
$$

Sostituendo adesso l'espressione del differenziale con il ricorso alla $(7),$ otteniamo:

$$
\begin{align}
\frac{1}{5-3\cos x} \ dx &= \frac{1+t^2}{2(1+4t^2)} \cdot \frac{2}{1+t^2} \ dt \\[6pt]
                        &= \frac{dt}{1 + 4t^2}
\end{align}
$$

Anche in questo caso l'integrale rimanente si riconduce a una forma elementare e poiché $1 + 4t^2 = 1 + (2t)^2,$ ponendo $u = 2t$ e $du = 2 \ dt,$ l'integrale diventa:

$$
\begin{align}
\int \frac{dt}{1 + 4t^2} &= \frac{1}{2}\int \frac{du}{1 + u^2} \\[6pt]
                        &= \frac{1}{2}\arctan u + c \\[6pt]
                        &= \frac{1}{2}\arctan(2t) + c
\end{align}
$$

Tornando alla variabile $x,$ otteniamo la primitiva:

$$\int \frac{dx}{5 - 3\cos x} = \frac{1}{2}\arctan(2\tan(x/2)) + c$$

- - -

Proponiamo un ultimo caso, calcolando il seguente integrale:

$$\int \frac{dx}{2 + \sin x}$$

Applicando le identità già ricavate possiamo riscrivere il denominatore come segue:

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

L'integrale quindi diventa:

$$\int \frac{dt}{\left(t+\frac{1}{2}\right)^2 + \frac{3}{4}}$$

Con un po' di pratica possiamo riconoscere che questa espressione corrisponde alla forma elementare:

$$\int \frac{du}{u^2 + a^2}$$

In questo caso abbiamo $u = t + 1/2$ e $a = \sqrt{3}/2.$ Utilizzando la relativa formula di integrazione, otteniamo:

$$\int \frac{dt}{t^2+t+1} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2t+1}{\sqrt{3}}\right) + c$$

Sostituendo nuovamente $t = \tan(x/2),$ otteniamo l'espressione finale:

$$\int \frac{dx}{2+\sin x} = \frac{2}{\sqrt{3}}\arctan\left(\frac{2\tan(x/2)+1}{\sqrt{3}}\right) + c$$

> Anche in questo caso abbiamo visto che dopo la sostituzione, l'integranda diventa una funzione razionale in $t,$ più semplice di quella di partenza e la sua primitiva può contenere arcotangenti e logaritmi, che compaiono tipicamente nell'integrazione delle funzioni razionali.

## Condizioni sul dominio

È importante fare alcune considerazioni sul dominio delle funzioni che consideriamo nelle sostituzioni: la sostituzione $t = \tan(x/2)$ è definita per ogni $x$ tale che $x/2 \neq \pi/2 + k\pi,$ cioè per ogni $x \notin \pi + 2\pi\mathbb{Z}.$ Quando si calcola un [integrale indefinito](../indefinite-integrals/), le formule ottenute valgono negli intervalli in cui sono definite sia l'integranda iniziale sia la sostituzione.

Richiede invece maggiore attenzione l'applicazione al caso di un [integrale definito](../definite-integrals/) i cui estremi possono appartenere a intervalli diversi. In questo caso si applica la sostituzione separatamente su ciascuna parte del [dominio](../determining-the-domain-of-a-function/) di integrazione in cui essa è definita, ha derivata continua e diversa da zero ed è invertibile nell'intervallo considerato, per poi sommare i contributi ottenuti. Applicare meccanicamente le sostituzioni viste sopra attraverso un punto della forma $x = (2k+1)\pi$ potrebbe portare a risultati errati, poiché la sostituzione potrebbe non essere definita in quel punto. Consideriamo, per esempio, l'integrale definito:

$$\int_0^{2\pi} \frac{dx}{5 - 3\cos x}$$

L'integranda è continua su tutto l'intervallo $[0,2\pi]$ ma la sostituzione $t = \tan(x/2),$ invece, non è definita in $x = \pi.$ Per questa ragione dobbiamo dividere l'integrale in questo punto e riscrivere i due contributi mediante i seguenti limiti:

$$
\lim_{a \to \pi^-}\int_0^a \frac{dx}{5 - 3\cos x}
+ \lim_{b \to \pi^+}\int_b^{2\pi} \frac{dx}{5 - 3\cos x}
$$

Come abbiamo già ricavato negli esempi precedenti, la sostituzione di Weierstrass trasforma l'espressione da integrare in:

$$\frac{dx}{5 - 3\cos x} = \frac{dt}{1 + 4t^2}$$

Nel primo intervallo, $x = 0$ corrisponde a $t = 0,$ mentre $t \to +\infty$ quando $x \to \pi^-.$ Nel secondo intervallo, $t \to -\infty$ quando $x \to \pi^+,$ mentre $x = 2\pi$ corrisponde a $t = 0.$ Otteniamo quindi due integrali impropri che scriviamo come segue:

$$\int_0^{+\infty} \frac{dt}{1 + 4t^2} + \int_{-\infty}^0 \frac{dt}{1 + 4t^2}$$

Calcoliamo separatamente i due contributi e otteniamo i seguenti valori per ciascun integrale:

$$
\begin{align}
\int_0^{+\infty} \frac{dt}{1 + 4t^2}
&= \lim_{A \to +\infty}\left[\frac{1}{2}\arctan(2t)\right]_0^A
= \frac{\pi}{4} \\[6pt]
\int_{-\infty}^0 \frac{dt}{1 + 4t^2}
&= \lim_{B \to -\infty}\left[\frac{1}{2}\arctan(2t)\right]_B^0
= \frac{\pi}{4}
\end{align}
$$

Sommando i due contributi, otteniamo infine il valore dell'integrale iniziale:

$$\frac{\pi}{4} + \frac{\pi}{4} = \frac{\pi}{2}$$

> L'integrale dato vale dunque $\pi/2.$ Se avessimo trasformato soltanto gli estremi iniziali $0$ e $2\pi$ questo avrebbe prodotto due estremi uguali a zero, perdendo il passaggio attraverso il punto in cui la sostituzione non è definita.

## Considerazioni finali

La sostituzione di Weierstrass non è sempre il metodo più efficiente. Quando l'integranda contiene soltanto potenze pari di $\sin x$ e $\cos x$ è preferibile utilizzare i metodi fondamentali dell'integrazione delle funzioni trigonometriche. Lo stesso vale anche quando l'integranda si può riscrivere sfruttando le seguenti identità:

$$\sin^2 x = (1 - \cos 2x)/2$$
$$\cos^2 x = (1 + \cos 2x)/2$$ 

Quando l'integranda ha la forma $R(\sin x)\cos x$ oppure $R(\cos x)\sin x,$ le [sostituzioni](../integration-by-substitution/) dirette $u = \sin x$ oppure $u = \cos x$ sono più rapide. Come criterio pratico, conviene ricorrere alla sostituzione di Weierstrass solo quando l'integranda è una funzione razionale di $\sin x$ e $\cos x$ che non ammette semplificazioni evidenti mediante [identità trigonometriche](../trigonometric-identities/) o sostituzioni dirette. Negli altri casi, le tecniche più semplici permettono calcoli più brevi.