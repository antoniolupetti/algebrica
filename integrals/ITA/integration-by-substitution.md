---
title: Integration by Substitution
source: https://algebrica.org/integration-by-substitution/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - chain-rule
  - change-of-variable
  - composite-functions
  - definite-integral
  - indefinite-integral
  - integration
  - integration-by-substitution
  - trigonometric-substitution
---
## Semplificare l'integrazione

Nei problemi reali si incontrano regolarmente integrali la cui forma di partenza non consente né una risoluzione immediata né intuitiva. Per ricondurli a oggetti più facilmente maneggiabili, occorre ricorrere a una serie di manipolazioni. Le prime volte si procede un po' a tentativi, ma con l'esperienza si acquisisce una certa padronanza che ci consente di individuare a colpo d'occhio una strategia in grado di ottenere benefici computazionali anche per quegli integrali che, a prima vista, sembrano molto complicati. Ho ripetuto più volte, nelle voci riguardanti questo argomento, che gli integrali, quantomeno quelli che si incontrano nei primi anni dei corsi universitari, sono risolvibili con procedimenti piuttosto meccanici e non richiedono chissà quale capacità di astrazione. Più che altro richiedono tanta, tantissima pratica e la conoscenza a memoria di tutte le primitive fondamentali, delle loro proprietà algebriche e dei principali metodi di integrazione.

Il metodo di integrazione per sostituzione, che vedremo nel dettaglio tra un attimo, è abbastanza semplice, in quanto è il procedimento inverso della regola della catena. In breve, il metodo mira a semplificare l'integrale di partenza, adattando opportunamente la variabile di integrazione e si applica in genere a integrali della seguente forma:

$$\int f(g(x))g'(x) \ dx \tag{1}$$

Supponiamo che $F$ sia una primitiva di $f,$ cioè $F' = f.$ Adottando la sostituzione $u = g(x),$ l'integrale diventa:

$$\int f(g(x))g'(x) \ dx = \int f(u) \ du = F(u) + c = F(g(x)) + c$$

Il procedimento può essere ridotto a quattro passaggi fondamentali:

+ Prima di tutto si sostituisce $u = g(x),$ scegliendo $g(x)$ in base alla struttura dell'integrale di partenza.
+ Si deriva poi la funzione scelta per ottenere $du = g'(x) \ dx.$
+ A questo punto, si riscrivono tutti i fattori e il differenziale in funzione di $u.$
+ Infine si integra rispetto a $u$ e per un integrale indefinito, si sostituisce nuovamente $u$ con $g(x).$ 

> Nel caso in cui l'integrale sia definito, è necessario ricordare che si devono usare gli estremi di partenza espressi però in funzione di $u$ come si vedrà più avanti nel paragrafo dedicato.

- - -

Come anticipato poco sopra, il metodo della sostituzione deriva dalla regola della catena per le derivate. Applicando la regola della catena alla funzione composta $F(g(x))$ otteniamo:

$$\frac{d}{dx}F(g(x)) = F'(g(x))g'(x) = f(g(x))g'(x)$$

L'integranda $f(g(x))g'(x)$ è quindi la derivata di $F(g(x)).$ Ponendo $u = g(x)$ si ottiene:

$$\int f(u) \ du = F(u) + c$$

Sostituendo nuovamente $u$ con $g(x)$ si ottiene $F(g(x)) + c,$ come nella formula iniziale.

- --

Come capire quanto una sostituzione è davvero utile? Per optare per questo metodo bisogna riconoscere quando si presenta lo schema della $(1),$ ovvero quando l'integranda contiene una [funzione composta](../composite-functions/) insieme a un fattore proporzionale alla derivata della sua funzione interna.

Dopo aver individuato una possibile funzione interna $g(x),$ si calcola $g'(x)$ e si confronta questa derivata con i fattori rimanenti nell'integranda. Non è necessario che $g'(x)$ compaia esattamente, basta che uno di tali fattori sia un suo multiplo costante non nullo. La costante viene raccolta fuori dall'integrale, mentre la sostituzione $u = g(x)$ trasforma $g'(x) \ dx$ in $du.$

Ad esempio consideriamo questo tipo di espressioni:

$$(ax + b)^n \quad \quad \sqrt{ax + b}$$
$$\ln(ax + b) \quad \quad e^{ax + b}$$

In tutti questi casi, la funzione interna è:

$$g(x) = ax + b$$

La sua derivata è banalmente $g'(x) = a.$ Poiché questa derivata è costante, la sostituzione $u = ax + b$ può essere applicata anche quando il fattore $a$ non compare esplicitamente nell'integranda. Per $a \neq 0,$ infatti, dalla relazione $du = a \ dx$ si ricava $dx = \frac{1}{a} \ du.$ Lo 

stesso criterio si applica a un'espressione razionale della seguente forma, con al denominatore la funzione interna e al numeratore quella che ne rappresenta la derivata:

$$\frac{g'(x)}{g(x)}$$

Se il numeratore coincide con $g'(x)$ a meno di un fattore costante non nullo, si pone $u = g(x).$

- - -

Sintetizzando quanto abbiamo fin qui illustrato, si riportano nella seguente tabella gli schemi ricorrenti con le opportune sostituzioni:

[class="table-1"]

|                                  |              |
| -------------------------------- | ------------ |
| $$\int f(g(x))g'(x) \ dx$$       | $$u = g(x)$$ |
| $$\int (ax + b)^n \ dx$$         | $$u = ax + b$$ |
| $$\int e^{ax + b} \ dx$$         | $$u = ax + b$$ |
| $$\int \ln(ax + b) \ dx$$        | $$u = ax + b$$ |
| $$\int \dfrac{g'(x)}{g(x)} \ dx$$ | $$u = g(x)$$ |

[/class]

Come si può notare i casi non sono tantissimi, quindi si riconoscono immediatamente con un po' di pratica.

## Esempi

Di seguito proponiamo alcuni esempi concreti per illustrare come il metodo funziona in pratica. Consideriamo, per primo, il seguente integrale:

$$\int (2x + 1)^3 \ dx$$

Questo è il caso $(ax+b)^n$, quindi basta porre $u = 2x + 1$ per sostituire l'espressione cubica con $u^3.$ Derivando il differenziale si ottiene $du = 2 \ dx$ da cui:

$$dx = \frac{du}{2}$$
L'integrale trasformato diventa quindi:

$$\int \frac{u^3}{2} \ du = \frac{1}{2}\int u^3 \ du$$

Come si può notare, abbiamo ridotto l'integrale a una forma elementare, e dalla regola di integrazione della potenza si ottiene:

$$\frac{1}{2}\left(\frac{u^4}{4}\right) + c = \frac{u^4}{8} + c$$

Ricordatevi sempre di tornare però all'espressione di partenza sostituendo nuovamente $u.$ In questo caso si ottiene:

$$\int (2x + 1)^3 \ dx = \frac{1}{8}(2x + 1)^4 + c$$

- - -

Facciamo adesso l'esempio di una funzione integranda razionale:

$$\int \frac{1}{3x - 5} \ dx$$

Come abbiamo visto, in questo caso basta porre $u = 3x - 5$ e derivando si ottiene $du = 3 \ dx.$ Possiamo quindi scrivere che:

$$dx = \frac{du}{3}$$

L'integrale trasformato diventa:

$$\int \frac{1}{3u} \ du = \frac{1}{3}\int \frac{du}{u}$$

Anche questo è un integrale elementare che si riduce alla forma logaritmica ottenendo:

$$\frac{1}{3}\ln|u| + c$$

Sostituendo nuovamente $u$ con $3x - 5$ si ottiene:

$$\int \frac{1}{3x - 5} \ dx = \frac{1}{3}\ln|3x - 5| + c$$

- - -

Calcoliamo adesso il seguente integrale:

$$\int x \sin(x^2) \ dx$$

L'espressione interna $x^2$ ha derivata $2x.$ Poniamo $u = x^2$ e otteniamo $du = 2x \ dx$, da cui:

$$\qquad x \ dx = \frac{1}{2} \ du$$

La sostituzione dà:

$$\int x\sin(x^2) \ dx = \frac{1}{2}\int \sin u \ du$$

La primitiva nella nuova variabile è:

$$\frac{1}{2}\int \sin u \ du = -\frac{1}{2}\cos u + c$$

Sostituendo nuovamente $u$ con $x^2$ si ottiene:

$$\int x\sin(x^2) \ dx = -\frac{1}{2}\cos(x^2) + c$$

- - -

Consideriamo infine il seguente integrale:

$$\int \cos x \sqrt{\sin x} \ dx$$

In questo caso dobbiamo sostituire $u = \sin x$ in modo da trasformare il radicale in $\sqrt{u}.$ Il differenziale della nuova variabile è pertanto $du = \cos x \ dx$ e l'integrale diventa:

$$\int \sqrt{u} \ du = \int u^{1/2} \ du$$

Anch'esso è un integrale banale che, sempre per la regola delle potenze, dà:

$$\int u^{1/2} \ du = \frac{u^{3/2}}{3/2} = \frac{2}{3} u^{3/2} + c$$

Sostituendo nuovamente $u$ con $\sin x$ si ottiene:

$$\int \cos x\sqrt{\sin x} \ dx = \frac{2}{3}(\sin x)^{3/2} + c$$

## Sostituzioni trigonometriche

Oltre alle sostituzioni visto poc'anzi alle volte è necessario ricorrere alle cosiddette sostituzioni trigonometriche utili soprattutto quando si incontrano all'interno di un integrale delle espressioni con i radicali contenenti una qualche forma quadratica del tipo $a^2 - x^2,$ $a^2 + x^2$ e $x^2 - a^2$. 

La sostituzione trigonometrica permette di maneggiarle riconducendo queste espressioni all'utilizzo dell'[identità fondamentale](../pythagorean-identity/) della trigonometria:

$$\sin^2 x + \cos^2 x = 1$$

Questa identità può essere riscritta in forma equivalente come:

$$
\begin{align}
\cos^2 x &= 1 - \sin^2 x \\[6pt]
\sec^2 x &= 1 + \tan^2 x \\[6pt]
\tan^2 x &= \sec^2 x - 1
\end{align}
$$

Quando $a > 0,$ la sostituzione  dipende dall'espressione sotto il radicale. È importante che ogni sostituzione deve essere applicata su un intervallo nel quale la funzione trigonometrica scelta è invertibile e il segno dei fattori ottenuti è determinato. Ad esempio, nel caso di $\sqrt{x^2 - a^2},$ i rami $x \geq a$ e $x \leq -a$ devono essere trattati separatamente. La scelta degli intervalli e la gestione dei valori assoluti sono illustrate nella voce dedicata alle [sostituzioni trigonometriche per gli integrali](../trigonometric-substitution-for-integrals/). Le sostituzioni ricorrenti sono schematizzate di seguito:

[class="table-1"]

|                         |                  |
| ----------------------- | ---------------- |
| $$\sqrt{a^2 - x^2}$$   | $$x = a\sin u$$ |
| $$\sqrt{a^2 + x^2}$$   | $$x = a\tan u$$ |
| $$\sqrt{x^2 - a^2}$$   | $$x = a\sec u$$ |

[/class]

- - -

Calcoliamo ad esempio il seguente integrale indefinito:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx$$

Per $|x| < 3,$ scegliamo $u \in (-\pi/2, \pi/2)$ e poniamo $x = 3\sin u.$ Il differenziale diventa:

$$dx = 3\cos u \ du$$

Quindi, il denominatore dopo la sostituzione diventa:

$$\sqrt{9 - x^2} = \sqrt{9 - 9\sin^2 u} = \sqrt{9(1 - \sin^2 u)}$$

Nell'intervallo scelto abbiamo che $\cos u > 0.$ L'identità $\sin^2 u + \cos^2 u = 1$ dà:

$$\sqrt{9(1 - \sin^2 u)} = \sqrt{9\cos^2 u} = 3\lvert\cos u\rvert = 3\cos u$$

L'integrale quindi diventa:

$$\int \frac{3\cos u \ du}{3\cos u} = \int \ du = u + c$$

Poiché $u$ appartiene all'intervallo dei valori principali dell'[arcoseno](../arcsine-function/), l'equazione $x = 3\sin u$ implica:

$$u = \arcsin\left(\frac{x}{3}\right)$$

La primitiva espressa nella variabile originale è pertanto:

$$\int \frac{1}{\sqrt{9 - x^2}} \ dx = \arcsin\left(\frac{x}{3}\right) + c$$

## Regola di sostituzione per gli integrali definiti

Fino ad ora abbiamo considerato solo il caso di integrali indefiniti. Quando ci troviamo a calcolare integrali definiti, bisogna tener conto di trasormare anche gli estremi in funzione della sostituzione che mettiamo in atto. In alternativa, possiamo trovare una primitiva rispetto a $u,$ sostituire nuovamente $u$ con $g(x)$ e usare gli estremi originali in $x.$ Supponiamo che $g$ sia derivabile con continuità su $[a,b]$ e che $f$ sia continua su un intervallo contenente $g([a,b]).$ Sotto queste ipotesi, la regola di sostituzione è omologa alla $(1)$, solo con gli estremi di integrazione esplicitati:

$$\int_a^b f(g(x))g'(x) \ dx = \int_{g(a)}^{g(b)} f(u) \ du$$

Facciamo un esempio pratico, calcolando il seguente integrale definito:

$$\int_{2}^{3} x\cos(x^2) \ dx$$

Poniamo $u = x^2.$ La relazione tra i differenziali è:

$$du = 2x \ dx \qquad x \ dx = \frac{1}{2} \ du$$

Trasformiamo gli estremi mediante la stessa sostituzione:

$$x = 2 \Longrightarrow u = 4 \qquad x = 3 \Longrightarrow u = 9$$

L'integrale nella nuova variabile è quindi:

$$\int_2^3 x\cos(x^2) \ dx = \frac{1}{2}\int_4^9 \cos u \ du$$

Per il [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/) otteniamo:

$$\frac{1}{2}\Bigl[\sin u\Bigr]_{4}^{9} = \frac{1}{2}(\sin 9 - \sin 4)$$

Il valore dell'integrale è dunque $\frac{1}{2}(\sin 9 - \sin 4).$

- - -

Quando l'integranda è una funzione razionale di $\sin x$ e $\cos x$ che non si semplifica mediante identità trigonometriche o sostituzioni dirette, si può ricorrere alla [sostituzione di Weierstrass](../the-weierstrass-substitution/).

## Ulteriori esempi svolti

La tabella elenca gli integrali in ordine crescente di difficoltà. Una frase prima di ogni soluzione identifica la caratteristica dell'integranda che suggerisce la sostituzione. Negli esempi successivi, la soluzione trasforma anche gli estremi, riscrive un fattore algebrico oppure usa una sostituzione trigonometrica.

[class="table-1"]

|                                                        |
| :----------------------------------------------------- |
| $$1 \quad \int \dfrac{dt}{(1 - 6t)^4}$$                |
| $$2. \quad \int x^3(2 + x^4)^5 \ dx$$                  |
| $$3. \quad \int \cos^3\theta\sin\theta \ d\theta$$     |
| $$4. \int \dfrac{2^{\ln x}}{x} \ dx$$                  |
| $$5. \quad \int_0^{\ln 4} \dfrac{e^t}{1 + 2e^t} \ dt$$ |
| $$6. \quad \int_{\pi/4}^{\pi/3} \csc^2(5x) \ dx$$      |
| $$7. \quad \int \dfrac{9x^3}{\sqrt{1 + x^2}} \ dx$$    |
| $$8. \quad \int_0^1 \sqrt{4 - x^2} \ dx$$              |
[/class]

Partiamo dal primo integrale. Il denominatore è una potenza dell'espressione lineare $1 - 6t,$ la cui derivata è costante. Poniamo $u = 1 - 6t$ da cui $du = -6 \ dt.$ Possiamo quindi riscrivere l'integrale come:

$$
\begin{align}
\int \frac{dt}{(1 - 6t)^4} &= -\frac{1}{6} \int u^{-4} \ du \\[6pt]
&= \frac{1}{18}u^{-3} + c \\[6pt]
&= \frac{1}{18(1 - 6t)^3} + c
\end{align}
$$

- - -

Nel secondo integrale, il fattore $x^3$ è proporzionale alla derivata dell'espressione interna $2 + x^4.$ Sostituiamo $u = 2 + x^4$ e ricaviamo $du = 4x^3 \ dx.$ L'integrale si può quindi riscrivere come:

$$
\begin{align}
\int x^3(2 + x^4)^5 \ dx &= \frac{1}{4} \int u^5 \ du \\[6pt]
&= \frac{u^6}{24} + c \\[6pt]
&= \frac{(2 + x^4)^6}{24} + c
\end{align}
$$

- - -

Per il terzo integrale, si noti che il fattore $\sin\theta$ è l'opposto della derivata di $\cos\theta.$ Sostituiamo $u = \cos\theta$ da cui $du = -\sin\theta \ d\theta.$ L'integrale trasformato diventa:

$$
\begin{align}
\int \cos^3\theta\sin\theta \ d\theta &= -\int u^3 \ du \\[6pt]
&= -\frac{u^4}{4} + c \\[6pt]
&= -\frac{\cos^4\theta}{4} + c
\end{align}
$$

- - -

Nel quarto integrale notiamo che l'esponente $\ln x$ ha derivata $1/x,$ che è l'altro fattore dell'integranda. Quindi sostituiamo $u = \ln x,$ da cui $du = 1/x \ dx.$ L'integrale si riscrive come:

$$
\begin{align}
\int \frac{2^{\ln x}}{x} \ dx &= \int 2^u \ du \\[6pt]
&= \frac{2^u}{\ln 2} + c \\[6pt]
&= \frac{2^{\ln x}}{\ln 2} + c
\end{align}
$$

- - -

Studiamo ora il quinto integrale. Il denominatore $1 + 2e^t$ ha derivata $2e^t,$ che è il doppio del numeratore. Essendo un integrale definito bisogna ricordarsi di trasformare anche gli estremi di integrazione insieme alla variabile. Poniamo la seguente sostituzione:

$$u = 1 + 2e^t \qquad du = 2e^t \ dt$$

$$t = 0 \Longrightarrow u = 3 \qquad t = \ln 4 \Longrightarrow u = 9$$

L'integrale quindi può essere riscritto quindi come:

$$
\begin{align}
\int_0^{\ln 4} \frac{e^t}{1 + 2e^t} \ dt &= \frac{1}{2} \int_3^9 \frac{1}{u} \ du \\[6pt]
&= \frac{1}{2}\Bigl[\ln u\Bigr]_3^9 \\[6pt]
&= \frac{1}{2}\ln 3
\end{align}
$$

- - -

Per il sesto integrale, notiamo che l'argomento della cosecante $5x$ ha derivata costante. Poniamo quindi le seguenti sostituzioni:

$$u = 5x \qquad du = 5 \ dx$$

$$x = \frac{\pi}{4} \Longrightarrow u = \frac{5\pi}{4} \qquad x = \frac{\pi}{3} \Longrightarrow u = \frac{5\pi}{3}$$

A questo punto possiamo riscrivere l'integrale, e risolverlo tendo conto degli estremi cambiati:

$$
\begin{align}
\int_{\pi/4}^{\pi/3} \csc^2(5x) \ dx &= \frac{1}{5} \int_{5\pi/4}^{5\pi/3} \csc^2u \ du \\[6pt]
&= -\frac{1}{5}\Bigl[\cot u\Bigr]_{5\pi/4}^{5\pi/3} \\[6pt]
&= \frac{1}{5}\left[\cot\left(\frac{5\pi}{4}\right) - \cot\left(\frac{5\pi}{3}\right)\right] \\[6pt]
&= \frac{1}{5}\left(1 + \frac{\sqrt{3}}{3}\right)
\end{align}
$$

- - -

Nell'esempio numero $7$ l'espressione $1 + x^2$ contenuta sotto radice ha derivata $2x.$ Dopo la sostituzione $u = 1 + x^2,$ il fattore rimanente è $x^2 = u - 1.$

$$u = 1 + x^2 \qquad du = 2x \ dx \qquad x^2 = u - 1$$

Pertanto l'integrale si trasforma in:

$$
\begin{align}
\int \frac{9x^3}{\sqrt{1 + x^2}} \ dx &= \frac{9}{2} \int \frac{u - 1}{\sqrt{u}} \ du \\[6pt]
&= \frac{9}{2} \int \left(u^{1/2} - u^{-1/2}\right) \ du \\[6pt]
&= 3u^{3/2} - 9u^{1/2} + c \\[6pt]
&= 3(x^2 - 2)\sqrt{1 + x^2} + c
\end{align}
$$

- - -

Infine, per l'ultimo caso, rileviamo che il radicale ha la forma $\sqrt{a^2 - x^2},$ quindi poniamo $x = 2\sin\theta$ e trasformiamo anche l'intervallo. Dalla trasformazione si ottiene:

$$x = 2\sin\theta \qquad dx = 2\cos\theta \ d\theta$$

$$x = 0 \Longrightarrow \theta = 0 \qquad x = 1 \Longrightarrow \theta = \frac{\pi}{6}$$

$$\sqrt{4 - x^2} = \sqrt{4 - 4\sin^2\theta} = \sqrt{4\cos^2\theta} = 2\cos\theta$$

L'integrale diventa quindi:

$$
\begin{align}
\int_0^1 \sqrt{4 - x^2} \ dx &= 4 \int_0^{\pi/6} \cos^2\theta \ d\theta \\[6pt]
&= 2 \int_0^{\pi/6} \left(1 + \cos(2\theta)\right) \ d\theta \\[6pt]
&= \Bigl[2\theta + \sin(2\theta)\Bigr]_0^{\pi/6} \\[6pt]
&= \frac{\pi}{3} + \frac{\sqrt{3}}{2}
\end{align}
$$
