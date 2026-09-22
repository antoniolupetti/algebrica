---
title: Integral of Trigonometric Functions
source: https://algebrica.org/integral-of-trigonometric-functions/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - hyperbolic-functions
  - indefinite-integral
  - integration
  - integration-by-substitution
  - power-reduction
  - pythagorean-identity
  - trigonometric-functions
  - trigonometric-identities
---
## Introduzione

Spesso, gli integrali che coinvolgono le funzioni trigonometriche, come [seno](../sine-function/), [coseno](../cosine-function/), [tangente](../tangent-function/) e [cotangente](../cotangent-function/), possono risultare decisamente ostici da risolvere. In linea generale (e questo vale per tutti gli integrali) richiedono la conoscenza di alcune tecniche di base che consentono di manipolare la funzione integranda, riducendola a quella di un integrale più facilmente risolvibile. In questa pagina sono illustrati i metodi più comuni per affrontare i casi più diffusi, sufficienti a risolvere gran parte degli integrali di questo tipo.

Prima di tutto, è necessario memorizzare le primitive delle funzioni trigonometriche elementari, poiché costituiscono la base dei passaggi fondamentali. Nella tabella di seguito trovate un riepilogo utile e sintetico.

[class="table-1"]

|     |                                                                              |
| --- | ---------------------------------------------------------------------------- |
| 1.  | $$\int \sin x \ dx = -\cos x + c$$                                           |
| 2.  | $$\int \cos x \ dx = \sin x + c$$                                            |
| 3.  | $$\int \tan x \ dx = -\ln \mid \cos x \mid + c$$                             |
| 4.  | $$\int \cot x \ dx = \ln \mid \sin x \mid + c$$                              |
| 5.  | $$\int \sec x \ dx = \ln \mid \sec x + \tan x \mid + c$$                     |
| 6.  | $$\int \csc x \ dx = \ln \mid \csc x - \cot x  \mid + c$$                    |
| 7.  | $$\int \sinh x \ dx = \cosh x + c$$                                          |
| 8.  | $$\int \cosh x \ dx = \sinh x + c$$                                          |
| 9.  | $$\int \tanh x \ dx = \ln \mid \cosh x \mid + c$$                            |
| 10. | $$\int \coth x \ dx = \ln \mid \sinh x \mid + c$$                            |
| 11. | $$\int \mathrm{sech} x \ dx = 2 \arctan\!\left(\tanh\frac{x}{2}\right) + c$$ |
| 12. | $$\int \operatorname{csch} x \ dx = \ln\left\lvert\tanh\frac{x}{2}\right\rvert + c$$ |

[/class]

Le casistiche non sono tantissime da memorizzare, ma richiedono un certo sforzo che con la pratica diventerà un'operazione automatica. Prima di procedere perciò vi invito a tenere molto bene a mente le espressioni sopra riportate in quanto alcune saranno utili nella teoria e negli esempi che seguono.

## Integrali di potenze trigonometriche con $n$ pari

Iniziamo con il caso semplice e anche piuttosto frequente in cui la funzione integranda presenta il seno o il coseno elevati a una potenza intera, ad esempio $\sin^4x,$ e che pertanto non può essere espressa con una primitiva immediata. Questo genere di integrali ha la seguente forma generalizzata:

$$\int \sin^{n} x \ dx \qquad \int \cos^{n} x \ dx \tag{1}$$

Consideriamo per primo il caso in cui l'esponente $n$ è pari. In questa circostanza l'integrale si semplifica riscrivendo i termini trigonometrici al quadrato mediante le formule di riduzione delle potenze che esprimono il seno e il coseno attraverso le seguenti relazioni:

$$\sin^{2} x = \frac{1 - \cos 2x}{2} \tag{2}$$

$$\cos^{2} x = \frac{1 + \cos 2x}{2} \tag{3}$$

Come si può notare, il membro a destra dell’uguaglianza esprime le potenze quadratiche del seno e del coseno in funzione di un termine di grado inferiore rispetto a quello presente a sinistra, consentendo a questo punto di calcolare l'integrale. La prima espressione deriva dall'[identità fondamentale della trigonometria](../pythagorean-identity/):

$$\sin^{2}x + \cos^{2}x = 1$$

La seconda, invece, è derivata dalla [formula di duplicazione](../trigonometric-identities/) del coseno:

$$\cos 2x = \cos^{2}x - \sin^{2}x$$

Se le combiniamo insieme, infatti, possiamo esprimere $\cos 2x$ in funzione di $\cos^{2}x$ oppure di $\sin^{2}x.$ Sostituendo $\sin^{2}x$ con $1 - \cos^{2}x$ si ottiene:

$$\cos 2x = \cos^{2}x - (1 - \cos^{2}x) = 2\cos^{2}x - 1$$

Ricavando $\cos^{2}x$ otteniamo appunto l'uguaglianza $(3)$:

$$\cos^{2}x = \frac{1 + \cos 2x}{2}$$

Lo stesso ragionamento vale per $\sin^{2}x.$ Sostituendo $\cos^{2}x = 1 - \sin^{2}x$ nella formula di duplicazione otteniamo:

$$\cos 2x = (1 - \sin^{2}x) - \sin^{2}x = 1 - 2\sin^{2}x$$

Ricavando $\sin^{2}x,$ si ottiene l'uguaglianza $(2)$:

$$\sin^{2}x = \frac{1 - \cos 2x}{2}$$
- - -

Per illustrare concretamente il metodo, consideriamo il seguente integrale:

$$\int 2\cos^{4}x \ dx$$

Ci troviamo di fronte a una potenza di quarto grado del coseno per la quale è conveniente utilizzare la $(3).$ Riscriviamo quindi la quarta potenza nella seguente forma:

$$
\begin{align}
\cos^{4}x &= \left(\frac{1 + \cos 2x}{2}\right)^{2} \\[6pt]
          &= \frac{1}{4}\left(1 + 2\cos 2x + \cos^{2} 2x\right) \tag{4}
\end{align}
$$

L'operazione ha abbassato il grado del coseno, ma rimane ancora una potenza di secondo grado che dobbiamo ridurre mediante la stessa identità, ottenendo:

$$\cos^{2} 2x = \frac{1 + \cos 4x}{2}$$

A questo punto sostituiamo questa espressione nella $(4)$ e svolgendo i calcoli otteniamo:

$$
\begin{align}
\cos^{4}x &= \frac{1}{4}\left(1 + 2\cos 2x + \frac{1 + \cos 4x}{2}\right) \\[6pt]
          &= \frac{1}{4}\left(\frac{3}{2} + 2\cos 2x + \frac{1}{2}\cos 4x\right) \\[6pt]
          &= \frac{3}{8} + \frac{1}{2}\cos 2x + \frac{1}{8}\cos 4x
\end{align}
$$

Moltiplicando per $2,$ come richiesto dall'integrale iniziale, otteniamo:

$$\int 2\cos^{4}x \ dx = \int \left(\frac{3}{4} + \cos 2x + \frac{1}{4}\cos 4x\right) \ dx$$

A questo punto abbiamo riscritto l'integrale iniziale come somma di termini integrabili separatamente, ottenendo:

$$\frac{3}{4}x + \frac{1}{2}\sin 2x + \frac{1}{16}\sin 4x + c$$

> Tenete quindi a mente che l'obiettivo in questo caso è quello di ridurre le potenze di grado superiore a $(1)$ a una somma di termini elementari, ciascuno integrabile separatamente e in modo immediato.

## Integrali di potenze trigonometriche con $n$ dispari

Quando l'esponente $n$ è dispari il metodo consiste nel separare un fattore della funzione la cui potenza è dispari e si riscrive la potenza pari rimanente mediante l'identità fondamentale della trigonometria. Consideriamo una potenza dispari generica nella forma $n = 2k + 1.$ Nel caso del seno avremmo:

$$
\begin{align}
\int \sin^{n} x \ dx &= \int \sin x (\sin^{2}x)^{k} \ dx \\[6pt]
                     &= \int \sin x (1 - \cos^{2}x)^{k} \ dx
\end{align}
$$

A questo punto utilizziamo il metodo di [integrazione per sostituzione](../integration-by-substitution/), ponendo $u = \cos x$ e $du = -\sin x \ dx.$ Otteniamo così l'integrale di un [polinomio](../polynomials/) in $u,$ che si calcola direttamente.

Il procedimento è del tutto analogo per una potenza dispari del coseno e consiste sempre nel separare un fattore $\cos x$ riscrivendo la potenza pari rimanente mediante l'identità:

$$\cos^{2}x = 1 - \sin^{2}x$$

A quel punto si applica quindi la sostituzione $u = \sin x,$ ottenendo anche in questo caso l'integrale di un polinomio.

- - -

Facciamo un esempio pratico, considerando il seguente integrale con potenza di esponente dispari:

$$\int \cos^{5}x \ dx$$

L'esponente è dispari, quindi separiamo un fattore coseno e riscriviamo la [potenza](../powers/) pari rimanente mediante l'identità fondamentale della trigonometria. Per prima cosa quindi riscriviamo l'integrale:

$$\int \cos^{5}x \ dx = \int \cos^{4}x \cdot \cos x \ dx$$

Il fattore $\cos^{4}x$ è una potenza pari, quindi può essere espresso con il procedimento visto in precedenza, in funzione di $\sin^{2}x$ mediante l'uguaglianza:

$$\cos^{4}x = (\cos^{2}x)^{2} = (1 - \sin^{2}x)^{2}$$

L'integrale quindi diventa:

$$\int (1 - \sin^{2}x)^{2} \cdot \cos x \ dx$$

Con un po' di mestiere riconosciamo subito che il fattore $\cos x \ dx$ è la derivata di $\sin x,$ e quindi operiamo la sostituzione $u = \sin x$ e $du = \cos x \ dx$ ottenendo così l'integrale di un polinomio in $u$:

$$\int (1 - u^{2})^{2} \ du$$

Sviluppando il quadrato, l'integrale diventa:

$$\int (1 - 2u^{2} + u^{4}) \ du$$

Integrando ciascun termine, otteniamo:

$$u - \frac{2}{3}u^{3} + \frac{1}{5}u^{5} + c$$

A questo punto sostituendo nuovamente $u = \sin x,$ si ha che la soluzione è la seguente:

$$\sin x - \frac{2}{3}\sin^{3}x + \frac{1}{5}\sin^{5}x + c$$

## Prodotti di potenze di seno e coseno

Una situazione più generale si presenta quando seno e coseno compaiono insieme in integrali della forma:

$$\int \sin^{m} x \cos^{n} x \ dx \tag{5}$$

In questo caso, la scelta del metodo dipende dagli esponenti e combina i due procedimenti illustrati in precedenza. Supponiamo che $n$ sia dispari. Quando almeno uno degli esponenti è dispari, si applica il metodo per le potenze dispari e si separa un fattore $\cos x,$ si esprime la potenza pari rimanente del coseno in funzione del seno mediante $\cos^{2}x = 1 - \sin^{2}x,$ e si sostituisce $u = \sin x.$ Se invece $m$ è dispari, il procedimento consiste nel separare un fattore $\sin x$ e porre $u = \cos x.$ Quando entrambi gli esponenti sono dispari, entrambe le scelte sono valide.

Quando sia $m$ sia $n$ sono pari si applicano come primo passaggio le formule di riduzione delle potenze, ovvero la $(2)$ e la $(3)$ a ciascun termine al quadrato. Un'altra identità spesso utile è la seguente:

$$\sin x \cos x = \frac{1}{2}\sin 2x$$

Questa ci consente di abbassare il grado complessivo in un solo passaggio. Applicando ripetutamente queste identità, si riduce l'integranda a una somma di termini della forma $\cos kx,$ ciascuno dei quali si integra immediatamente, come abbiamo visto negli esempi precedenti.

- - -

Per un esempio pratico, consideriamo il seguente integrale che è della forma $(5)$:

$$\int \sin^{2} x \cos^{3} x \ dx$$

Notiamo subito che l'esponente del coseno è dispari, quindi separiamo un fattore $\cos x$ e riscriviamo la potenza pari del coseno in funzione del seno:

$$\int \sin^{2} x \cos^{3} x \ dx = \int \sin^{2} x \cdot \cos^{2} x \cdot \cos x \ dx$$

Usando l'identità $\cos^{2}x = 1 - \sin^{2}x,$ l'integrale diventa:

$$\int \sin^{2} x (1 - \sin^{2}x) \cdot \cos x \ dx$$

Il fattore $\cos x \ dx$ è il differenziale di $\sin x,$ quindi poniamo $u = \sin x$ e $du = \cos x \ dx,$ ottenendo l'integrale di un polinomio in $u$:

$$\int u^{2}(1 - u^{2}) \ du = \int (u^{2} - u^{4}) \ du$$

Integrando ciascun termine, abbiamo:

$$\frac{1}{3}u^{3} - \frac{1}{5}u^{5} + c$$

Infine, sostituendo nuovamente $u = \sin x,$ si ha che il nostro integrale è pari a:

$$\frac{1}{3}\sin^{3}x - \frac{1}{5}\sin^{5}x + c$$

## Reciproci del seno e del coseno

Altri casi frequenti riguardano gli integrali dei reciproci del seno e del coseno. Sebbene queste espressioni possano sembrare meno immediate, in realtà i loro integrali si calcolano con lo stesso procedimento algebrico. Consideriamo ad esempio il reciproco del coseno:

$$\int \frac{1}{\cos x} \ dx$$

Sappiamo che l'integranda è pari alla secante. A questo punto moltiplichiamo la secante per una frazione uguale a $1$:

$$\begin{align}
\int \sec x \ dx &= \int \sec x \cdot \frac{\sec x + \tan x}{\sec x + \tan x} \ dx \\[12pt]
                 &= \int \frac{\sec^{2}x + \sec x\tan x}{\sec x + \tan x} \ dx
\end{align}
$$

Questo trucco consente di trasformare il numeratore nella derivata del denominatore, poiché vale l'uguaglianza:

$$\frac{d}{dx}(\sec x + \tan x) = \sec x\tan x + \sec^{2}x$$

L'integrale ha quindi la forma:

$$\int \frac{f'(x)}{f(x)} \ dx$$

La sua primitiva è $\ln|f(x)|.$ Si ottiene pertanto:

$$\int \frac{1}{\cos x} \ dx = \int \sec x \ dx = \ln|\sec x + \tan x| + c$$

La stessa struttura si applica all'integrale del reciproco del seno:

$$\int \frac{1}{\sin x} \ dx$$

In questo caso l'integranda corrisponde alla cosecante e moltiplicandola come sopra per una frazione pari a $1$ otteniamo lo speculare del reciproco del coseno:

$$
\begin{align}
\int \csc x \ dx &= \int \csc x \cdot \frac{\csc x - \cot x}{\csc x - \cot x} \ dx \\[12pt]
                 &= \int \frac{\csc^{2}x - \csc x\cot x}{\csc x - \cot x} \ dx
\end{align}
$$

Anche in questo caso il numeratore è la derivata del denominatore, poiché vale l'uguaglianza:

$$\frac{d}{dx}(\csc x - \cot x) = -\csc x\cot x + \csc^{2}x$$

L'integrale di $\csc x$ è quindi:

$$\int \frac{1}{\sin x} \ dx = \int \csc x \ dx = \ln|\csc x - \cot x| + c$$

## Una procedura per la scelta del metodo

È utile a questo punto descrivere una procedura che riassume l'applicazione dei casi visti qui sopra a un generico integrale trigonometrico.

+ Per prima cosa, quando l'integranda è una singola funzione trigonometrica o iperbolica, si integra direttamente usando i valori riportati nella tabella delle primitive fondamentali.
+ Quando l'integranda è una potenza $\sin^{n} x$ o $\cos^{n} x$ con $n$ pari, si applicano le formule di riduzione delle potenze a ciascun termine al quadrato e si ripete il procedimento finché non rimangono potenze pari. L'integranda si riduce così a una somma di espressioni della forma $\cos kx,$ che si integrano immediatamente.
+ Quando invece l'integranda è una potenza $\sin^{n} x$ o $\cos^{n} x$ con $n$ dispari, si separa un fattore della funzione, si riscrive la potenza pari rimanente mediante l'identità fondamentale della trigonometria e si applica la sostituzione $u = \cos x$ oppure $u = \sin x,$ in modo che il differenziale corrisponda al fattore separato. In questo modo otteniamo l'integrale di un polinomio in $u,$ che si calcola banalmente.
+ Nel caso in cui l'integranda ha la forma $\sin^{m} x \cos^{n} x$ con almeno un esponente dispari, occorre separare un fattore della funzione con esponente dispari e si riscrive la potenza pari rimanente mediante l'identità fondamentale della trigonometria. A questo punto si sceglie l'altra funzione come nuova variabile e si pone $u = \sin x$ quando il coseno ha esponente dispari o $u = \cos x$ quando l'esponente è pari.
+ Quando sia $m$ sia $n$ sono pari, si applicano le formule di riduzione delle potenze a ciascun termine al quadrato e si integra termine a termine.
+ Per $\sec x$ e $\csc x,$ si moltiplica l'integranda per una frazione uguale a $1,$ scelta in modo che il numeratore diventi la derivata del denominatore, e si ottiene la relativa forma logaritmica.
+ Infine quando l'integranda è una funzione razionale di $\sin x$ e $\cos x$ che non rientra nei casi precedenti, si applica la [sostituzione di Weierstrass](../the-weierstrass-substitution/), che trasforma l'integranda in una [funzione razionale](../rational-functions/) di una nuova variabile. Per i radicali di espressioni quadratiche si ricorre invece alla [sostituzione trigonometrica](../trigonometric-substitution-for-integrals/).

> Queste tecniche sono molto utili ma non sempre si possono ricondurre gli integrali trigonometrici alle sole casistiche mostrate in questa pagina. Quando ad esempio un prodotto di due funzioni non corrisponde a uno dei casi illustrati, l'alternativa tipica da usare è l'[integrazione per parti](../integration-by-parts/). Nei casi più complicati, quando non esiste una primitiva in forma chiusa, il valore di un integrale definito può comunque essere approssimato mediante l'[integrazione numerica](../numerical-integration/).
