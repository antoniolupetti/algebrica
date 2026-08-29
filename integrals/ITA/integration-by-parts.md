---
title: Integration by Parts
source: https://algebrica.org/integration-by-parts/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - definite-integral
  - indefinite-integral
  - integration
  - integration-by-parts
  - liate-rule
  - product-rule
  - trigonometric-integrals
---
## Il metodo di integrazione per parti

Il metodo di integrazione per parti è, insieme al [metodo di integrazione per sostituzione](../integration-by-substitution/), una delle tecniche più utili per ricondurre un integrale non del tutto immediato a una forma più semplice, mediante una serie di riscritture che hanno lo scopo di trasferire l'operazione di derivazione da un fattore all'altro, in modo che il nuovo integrale abbia una primitiva più semplice da determinare rispetto a quello di partenza. Il metodo si applica generalmente a integrali che si presentano in questa forma:

$$\int f(x)g'(x) \ dx $$

Questi integrali possono essere riscritti, con un'opportuna riscrittura nel seguente modo:

$$\int u \ dv = uv - \int v \ du \tag{1}$$

In genere questo metodo è meno immediato di quello per sostituzione in quanto la difficoltà consiste proprio nello scegliere in modo appropriato $u$ e $dv$ affinché l'integrale ottenuto risulti più semplice. Un tipico esempio di applicazione del metodo è dato dal seguente integrale:

$$\int x e^x\,dx$$

Questo integrale si può riscrivere sostituendo $u=x$ e $dv=e^x\,dx$ ottenendo $du=dx$ e $v=e^x.$ Applicando la $(1)$ si ottiene:

$$\begin{aligned}  \int xe^x\,dx &= xe^x-\int e^x\,dx \\[6pt] &= xe^x-e^x+C \\[12pt]  &= e^x(x-1)+C \end{aligned}$$

Per gli [integrali indefiniti](../indefinite-integrals/), la formula è:

$$\int f(x)g'(x) \ dx = f(x)g(x) - \int f'(x)g(x) \ dx + c \tag{2}$$

Per gli [integrali definiti](../definite-integrals/) dobbiamo, come naturale, considerare gli estremi di integrazione.

$$\int_a^b f(x)g'(x) \ dx = [f(x)g(x)]_a^b - \int_a^b f'(x)g(x) \ dx \tag{3}$$

Il metodo può essere applicato più volte con l'obiettivo di ottenere ad ogni iterazione un'integrale più semplice e può anche essere alternato, laddove utile e possibile, con il metodo per sostituzione.

- - -

La formula $(1)$ si ottiene partendo dalla [regola del prodotto](../differentiation-rules/) della derivazione. Si parte da:

$$\frac{d}{dx}(f(x)g(x)) = f'(x)g(x) + f(x)g'(x)$$

Integrando entrambi i membri rispetto a $x$ si ottiene:

$$\int \frac{d}{dx}(f(x)g(x)) \ dx = \int f'(x)g(x) \ dx + \int f(x)g'(x) \ dx \tag{4}$$

Una primitiva della funzione integranda al primo membro è banalmente $f(x)g(x)$ perciò possiamo riscrivere la precedente espressione come:

$$f(x)g(x) = \int f'(x)g(x) \ dx + \int f(x)g'(x) \ dx$$

Spostando i membri a destra e sinistra del segno di uguale si ottiene la formula di integrazione per parti:

$$\int f(x)g'(x) \ dx = f(x)g(x) - \int f'(x)g(x) \ dx + c$$

Ponendo infine $u = f(x)$ e $dv = g'(x) \ dx,$ la formula diventa proprio la $(1)$:

$$\int u \ dv = uv - \int v \ du$$

Nell’applicazione del metodo bisogna sempre verificare che l’integrale risultante sia effettivamente più semplice di quello di partenza. Questo avviene, in genere, quando la derivazione semplifica uno dei fattori e l’altro ammette una primitiva elementare. In caso contrario, si rischia di ottenere un integrale ancora più complesso, anziché semplificare il calcolo, e probabilmente la strada imboccata non è la più funzionale. Comunque, come per il metodo di integrazione per sostituzione, l'esperienza renderà pressoché immediato trovare una sostituzione efficace che renda l'integrale facilmente risolvibile.

## Interpretazione geometrica

In genere tendiamo ad accettare a priori i risultati presentati nella teoria matematica, e questo, per certi versi, è un bene. Vuol dire che nutriamo una sincera fiducia in coloro che ci hanno preceduto, ma è anche la prova che lo spirito di autoconservazione insito in ciascuno di noi fa il proprio lavoro. In caso contrario, la maggior parte di noi probabilmente impazzirebbe.

Ci sono però delle cose che vale la pena approfondire, perché talvolta non sono menzionate nei classici corsi di studio, ma che rendono certe formule intuitive e concrete. Questo è il caso dell'interpretazione geometrica della formula dell'integrazione per parti che interpreta i termini della formula come [aree nel piano](../finding-areas-by-integration/). 

Consideriamo due punti per cui valga $a < b,$ e siano $u,v\colon [a,b] \to \mathbb{R}$ [funzioni a valori reali](../functions/), continuamente derivabili, [strettamente crescenti](../increasing-and-decreasing-functions/) e tali che $u(a) = v(a) = 0$ in modo che $u$ e $v$ siano non negative su tutto $[a,b].$ Possiamo scrivere:

$$
\begin{align}
\int_a^b u \ dv &= \int_a^b u(x)v'(x) \ dx \\[6pt]
\int_a^b v \ du &= \int_a^b v(x)u'(x) \ dx
\end{align}
$$

La curva parametrica $x \mapsto (v(x),u(x))$ congiunge l'origine nel punto $(v(b),u(b))$ e divide il rettangolo $[0,v(b)] \times [0,u(b)]$ in due regioni.

![IMG. 1](svg/integration-by-parts-1.svg)

L'area della regione inferiore è data dal seguente integrale:

$$A_1 = \int_0^{v(b)} u(v^{-1}(t)) \ dt = \int_a^b u(x)v'(x) \ dx = \int_a^b u \ dv$$

L'area della regione superiore è invece data da:

$$A_2 = \int_0^{u(b)} v(u^{-1}(s)) \ ds = \int_a^b v(x)u'(x) \ dx = \int_a^b v \ du$$

Poiché le due regioni riempiono il rettangolo vale:

$$\int_a^b u \ dv + \int_a^b v \ du = u(b)v(b)$$

Riordinando questa uguaglianza si ottiene:

	$$\int_a^b u \ dv = u(b)v(b) - \int_a^b v \ du \tag{5}$$

Poiché $u(a)=v(a)=0,$ si ha:
$$[uv]_a^b=u(b)v(b)$$ 
L'uguaglianza $(5)$ diventa quindi proprio la formula d'integrazione per parti che abbiamo visto sopra:

$$\int_a^b u \ dv = [uv]_a^b - \int_a^b v \ du$$

> Le ipotesi di stretta monotonia crescente e di non negatività consentono di interpretare i due integrali come aree geometriche non orientate, ma non sono necessarie per la validità della formula generale. Se infatti $u$ o $v$ cambia segno o non è crescente, questa costruzione non fornisce più, in maniera generalizzata, due regioni separate le cui aree coincidono con i due integrali.

## Come scegliere $u$ e $dv$

Abbiao più volte ripetuto fin qui che l'applicazione del metodo, per essere davvero utile, deve rendere l'integrale risultante più semplice di quello iniziale. Ma come si possono scegliere le sostituzioni di $u$ e $dv$ affinchè siano effettivamente utili al nostro scopo? Possiamo idealmente identificare due metodi di scelta:

+ Si sceglie come $u$ il fattore che si semplifica quando viene derivato.
+ Si sceglie come $dv$ il fattore rimanente, in modo che $v = \int dv$ possa essere calcolato direttamente.

La regola euristica LIATE indica una sequenza di possibili tentativi per selezionare $u$ in modo appropriato. La sequenza prevede una sostituzione con: 

+ Logaritmiche
+ Inverse delle funzioni trigonometriche
+ Algebriche
+ Trigonometriche
+ [Esponenziali](../exponential-function/)

Attenzione però, questa regola non sempre è utile. In generale possiamo dire che un fattore [logaritmico](../logarithmic-function/) o una funzione trigonometrica inversa vengono spesso scelti come sostituzione di $u,$ perché la derivazione tende a semplificarne la forma. Tuttavia se la scelta produce un integrale più difficile occorre affrontare il problema diversamente, scegliendo un'altra sostituzione o ricorrendo a un altro metodo. Gli integrali purtroppo sono così, ma la buona notizia è che richiedono più pratica che intuizione e con un costante esercizio le sostituzioni verranno immediate e naturali.

- - -

Nelle applicazioni dell'integrazione per parti ricorrono alcuni errori abbastanza tipici, il più comune dei quali consiste nella scelta dei fattori che complica l'integrale di partenza invece di semplificarlo.

Nel caso indefinito, la costante di integrazione deve sempre comparire nel risultato. Le costanti provenienti dalle primitive intermedie possono essere assorbite in questa costante, perciò si può aggiungere solo una $c$ dopo l'ultima semplificazione algebrica.

Spesso si dimentica che per gli integrali definiti, il termine al bordo $[uv]_a^b$ deve essere calcolato esplicitamente. Se viene omesso, l'uguaglianza $(3)$ vale solo nel caso in cui il termine al bordo sia nullo (cosa tutt'altro che scontata).

Quando si sceglie una funzione trigonometrica come $u,$ occorre calcolare $du$ con attenzione. La derivata di $\sin(x)$ è $\cos(x),$ mentre quella di $\cos(x)$ è $-\sin(x),$ da cui deriva un'inevitabile alternanza dei segni nelle derivazioni successive. Scrivere esplicitamente $du$ prima di applicare la formula, evita di sbagliare il segno.


## Esempio 1

Mettiamo adesso in atto il metodo con alcuni esempio. Partiamo dal considerare il seguente integrale:

$$\int x^2\ln(x) \ dx$$

L'integranda contiene il prodotto tra una [potenza](../powers/) e un logaritmo. Entrambi i fattori ammettono primitive elementari e la sostituzione risulta piuttosto immediata. Poniamo:

$$f(x) = \ln(x) \quad \rightarrow \quad f'(x) = \frac{1}{x}$$

$$g'(x) = x^2 \quad \rightarrow \quad g(x) = \frac{x^3}{3}$$

Applicando la formula $(2)$ si ottiene:

$$
\begin{align}
\int x^2\ln(x) \ dx &= \frac{x^3}{3}\ln(x) - \int \frac{x^3}{3x} \ dx + c \\[6pt]
                     &= \frac{x^3}{3}\ln(x) - \int \frac{x^2}{3} \ dx + c\\[6pt]
                     & = \frac{x^3}{3}\ln(x) - \frac{x^3}{9} + c
\end{align}
$$

Ora basta raccogliere il termine comune per ottenere come risultato:

$$\frac{x^3}{3}\left(\ln(x) - \frac{1}{3}\right) + c$$

## Esempio 2

Facciamo ora un ulteriore esempio indicativo di come una seconda applicazione dell'integrazione per parti può ricondurre all'integrale iniziale. Consideriamo ad esempio il seguente integrale:

$$\int e^x\sin(x) \ dx$$

Indichiamo questo integrale con $I.$ Poiché il fattore $e^x$ ha come primitiva $e^x$ e $\sin(x)$ ha come derivata $\cos(x),$ scegliamo $u = \sin(x)$ e $dv = e^x \ dx.$ Calcolando la derivata e la primitiva otteniamo:

$$du = \cos(x) \ dx \qquad v = e^x$$

Per la formula $(2)$ scriviamo:

$$I = e^x\sin(x) - \int e^x\cos(x) \ dx$$

Se fate attenzione, il nuovo integrale contiene ancora il prodotto di $e^x$ e di una [funzione trigonometrica](../sine-and-cosine/) perciò occorre applicare una seconda volta l'integrazione per parti definendo:

$$J = \int e^x\cos(x) \ dx$$

Scegliamo $u = \cos(x)$ e $dv = e^x \ dx$ e calcoliamo la derivata e la primitiva:

$$du = -\sin(x) \ dx \qquad v = e^x$$

Sempre per la formula $(2)$ scriviamo:

$$J = e^x\cos(x) + \int e^x\sin(x) \ dx = e^x\cos(x) + I$$

L'integrale iniziale $I$ è ricomparso. Sostituendo l'espressione di $J$ nell'equazione per $I$ si ottiene:

$$I = e^x\sin(x) - (e^x\cos(x) + I)$$

Sommando $I$ a entrambi i membri si ottiene:

$$2I = e^x\sin(x) - e^x\cos(x)$$

E quindi:

$$I = \frac{e^x}{2}(\sin(x) - \cos(x)) + c$$

## Esempio 3

Consideriamo adesso il seguente [integrale improprio](../improper-integrals/):

$$\int_0^1 \ln(x) \ dx$$

Possiamo immaginare l'integrale come il prodotto tra un logaritmo e una funzione costante pari a 1. Derivando $\ln(x)$ otteniamo banalmente $1/x,$ mentre per la funzione costante $1$ la primitiva $x.$ Poniamo quindi la seguente sostituzione:

$$f(x) = \ln(x) \quad \rightarrow \quad f'(x) = \frac{1}{x}$$

$$g'(x) = 1 \quad \rightarrow \quad g(x) = x$$

Per escludere l'estremo singolare $0,$ scegliamo $\varepsilon \in (0,1)$ e applichiamo la formula $(3)$ all'[intervallo](../intervals/) $[\varepsilon,1]:$

$$
\begin{align}
\int_\varepsilon^1 \ln(x) \ dx &= [x\ln(x)]_\varepsilon^1 - \int_\varepsilon^1 \frac{x}{x} \ dx \\[6pt]
                                  &= [x\ln(x)]_\varepsilon^1 - \int_\varepsilon^1 1 \ dx
\end{align}
$$

Come sappiamo, l'integrale improprio è il [limite](../limits/) per $\varepsilon \to 0^+.$ Poiché $\ln(1) = 0$ e $\varepsilon\ln(\varepsilon) \to 0,$ il limite del primo termine è:

$$\lim_{\varepsilon \to 0^+}[x\ln(x)]_\varepsilon^1 = 0$$

Il limite dell'integrale invece è:

$$\lim_{\varepsilon \to 0^+}\int_\varepsilon^1 1 \ dx = 1$$

Pertanto si ottiene:

$$\int_0^1 \ln(x) \ dx = -1$$


## Procedura di scelta

Abbiamo visto fin qui che quando l'integranda è il prodotto di due fattori, si può usare la procedura seguente di integrazione per parti nel seguente modo.

Si identifica per prima cosa l'integranda come prodotto $u(x)v'(x).$ Se a prima vista non si osserva alcun prodotto, si può provare a manipolare l'integrale iniziale scomponendolo in fattori, usando le [identità trigonometriche](../trigonometric-identities/) oppure ricorrereno alla [scomposizione in fratti semplici](../partial-fraction-decomposition/), quindi si valuta nuovamente se l'integrazione per parti sia applicabile.

Una volta che l'integrale è ridotto a un prodotto tra fattori compatibile con il metodo, si usa la procedura LIATE come guida iniziale per scegliere $u$ e $dv.$ Come primo criterio si verifica che la derivazione semplifichi il fattore $u$ e che sia possibile calcolare direttamente $v = \int dv.$ La prima condizione non è necessaria quando ulteriori applicazioni fanno ricomparire l'integrale iniziale o producono una formula di riduzione.

Si calcolano poi $du = u'(x) \ dx$ e $v = \int dv$ e si applica la formula $(1).$ A questo punto si esamina il nuovo integrale $\int v \ du$ e si possono presentare i seguenti casi casi.

+ Il nuovo integrale è più difficile di quello iniziale. Si torna allora alla scelta di $u$ e $dv$ e si prova una scelta diversa. Se nessuna scelta semplifica il calcolo o produce una relazione utile con l'integrale iniziale, occorre usare un altro metodo.

+ L'integrale iniziale ricompare come nell'esempio 2, eventualmente dopo un'altra applicazione della formula. Raccogliendo in un solo membro tutte le occorrenze dell'integrale si ottiene un'[equazione lineare](../linear-equations/) risolvibile quando il coefficiente dell'integrale è diverso da zero.

 + Per ultimo, l'integranda del nuovo integrale ha una primitiva nota oppure il nuovo integrale richiede un'altra applicazione dell'integrazione per parti. Nel caso definito, si calcolano il termine al bordo $[uv]_a^b = u(b)v(b) - u(a)v(a)$ e l'integrale definito rimanente. Nel caso indefinito, si calcola l'integrale rimanente e si aggiunge una sola costante di integrazione $c$ dopo l'ultima semplificazione algebrica.

Nota: quando l'integranda è un'espressione razionale in $\sin(x)$ e $\cos(x)$ la [sostituzione di Weierstrass](../the-weierstrass-substitution/) o una [sostituzione diretta](../integration-by-substitution/) come $u = \sin(x)$ oppure $u = \cos(x)$ può produrre un [integrale di una funzione razionale](../integral-of-rational-functions/).

Infine, per alcune famiglie di integrali parametrizzate da un esponente intero, l'integrazione per parti restituisce un integrale della stessa famiglia con indice inferiore e la relazione così ottenuta è una [formula di riduzione](../reduction-formulas/) da applicare fino a raggiungere un caso base.
