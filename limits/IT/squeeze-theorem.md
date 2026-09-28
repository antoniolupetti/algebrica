---
title: Squeeze Theorem
source: https://algebrica.org/squeeze-theorem/
license: CC BY-NC 4.0
tags:
  - bounded-functions
  - geometric-proof
  - limits
  - oscillating-functions
  - remarkable-limits
  - squeeze-theorem
---
## Enunciato

Nel calcolo dei limiti si possono incontrare problemi in cui la risoluzione diretta per sostituzione non è un metodo efficace con il quale procedere. Esistono delle tecniche che, come vedremo nelle voci dedicate della sezione dedicata ai limiti, consentono di risolvere forme particolari, come le forme indeterminate. Alcune funzioni, come seno e coseno, hanno invece un andamento oscillante e meritano una trattazione a parte. In tali casi si ricorre al teorema del confronto che consente di risolvere agevolmente i limiti di espressioni del tipo:

$$x\sin\left( \frac{1}{x} \right) \qquad \frac{\sin x}{x} \qquad x^2\cos\left( \frac{1}{x} \right)$$

In termini pratici, il teorema consente di racchiudere la funzione originaria tra due funzioni che hanno uno stesso limite, così da determinarne il limite. Consideriamo un punto di accumulazione $x_0 \in \mathbb{R} \cup \{ \pm\infty \}.$ Per definizione, qualunque suo intorno contiene almeno un punto del dominio diverso da $x_0.$ Consideriamo quindi tre funzioni reali $f,$ $g$ e $h$ definite sui punti del dominio appartenenti a un intorno $I$ di $x_0.$ Immaginiamo anche che valga la seguente disuguaglianza, che consente di esprimere il grafico della funzione $f$ sempre compreso tra i grafici della funzione $g$ e $h$:

$$g(x) \leq f(x) \leq h(x) \tag{1}$$

A questo punto supponiamo di conoscere il seguente limite $\ell$:

$$\lim_{x \to x_0} g(x) = \lim_{x \to x_0} h(x) = \ell\tag{2}$$

Allora, sotto queste ipotesi anche la funzione $f(x)$ ammette un limite e il suo valore è proprio pari al limite della $(2)$:

$$\lim_{x \to x_0} f(x) = \ell\tag{3}$$

Da un punto di vista grafico, abbiamo che la curva che rappresenta $f(x)$ è sempre compresa tra la funzione minorante $g(x)$ e la funzione maggiorante $h(x),$ e poiché entrambe tendono a $\ell,$ allora anche $f(x)$ deve convergere allo stesso limite.


![IMG. 1](../svg/squeeze-theorem-1.svg)



Per dimostrare questo risultato, fissiamo un numero arbitrario $\varepsilon > 0$ e dimostriamo che la funzione $f(x),$ compresa tra $g(x)$ e $h(x),$ tende allo stesso limite $\ell$ per $x \to x_0.$ Per l'ipotesi formulata con la $(1)$ sappiamo che vale $\lim_{x \to x_0} g(x) = \ell.$ Per la definizione di limite, esiste quindi un numero positivo $\delta_1$ tale che, per ogni $x$ del dominio che soddisfa $0 < |x - x_0| < \delta_1,$ si ha:

$$\ell - \varepsilon < g(x) < \ell + \varepsilon \tag{4}$$

Sempre dalla $(1)$, poiché sappiamo che vale $\lim_{x \to x_0} h(x) = \ell,$ esiste, analogamente al ragionamento appena fatto, un numero positivo $\delta_2$ tale che, per ogni $x$ del dominio che soddisfa $0 < |x - x_0| < \delta_2,$ si ha:

$$\ell - \varepsilon < h(x) < \ell + \varepsilon \tag{5}$$

Ponendo $\delta = \min(\delta_1, \delta_2)$ per ogni $x$ del dominio tale che $0 < |x - x_0| < \delta,$ valgono sia la $(4)$ che la $(5)$. Poiché vale anche la $(1)$ allora si ottiene che:

$$\ell - \varepsilon < f(x) < \ell + \varepsilon \tag{6}$$

Poiché questa condizione è verificata per ogni $\varepsilon > 0,$ concludiamo che:

$$\lim_{x \to x_0} f(x) = \ell$$

Quando $x_0 = +\infty,$ le condizioni $0 < |x - x_0| < \delta_1,$ e $0 < |x - x_0| < \delta_2,$ sono sostituite da $x > M_1$ e $x > M_2.$ Scegliendo $M = \max(M_1, M_2)$ abbastanza grande entrambe le stime valgono per $x > M,$ e il teorema del confronto giunge alla medesima conclusione del caso appena dimostrato. Per $x_0 = -\infty,$ si usano invece le condizioni $x < M_1$ e $x < M_2,$ scegliendo $M = \min(M_1, M_2).$

## Esempi

Facciamo di seguito alcuni esempi per mostrare come si applica il teorema nella pratica. Proviamo a calcolare il limite della seguente funzione:

$$\lim_{x \to 0} x \cdot \sin\left( \frac{1}{x} \right) \tag{7}$$

La sostituzione diretta $x = 0$ non è possibile, perché $1/x$ non è definito in zero. Il fattore $x$ tende a zero, mentre $\sin(1/x)$ non ammette limite per $x \to 0,$ perché oscilla indefinitamente tra $-1$ e $1.$ Sappiamo però che per $x \neq 0$ vale la seguente disuguaglianza, in quanto la funzione seno è compresa tra questi valori:

$$-1 \leq \sin\left( \frac{1}{x} \right) \leq 1 \tag{8}$$

Per calcolare il limite nella $(7),$ osserviamo che la $(8)$ garantisce che il seno abbia valore assoluto al più uguale a $1$ e da questo, moltiplicando per $x,$ otteniamo:

$$-|x| \leq x \cdot \sin\left( \frac{1}{x} \right) \leq |x| \tag{9}$$

Dalla $(9)$ possiamo ricavare che le funzioni $-|x|$ e $|x|$ tendono a zero per $x \to 0$ e quindi, poiché $x \sin(1/x)$ è compresa tra esse, per il teorema del confronto otteniamo che il limite della $(7)$ è pari a zero:

$$\lim_{x \to 0} x \cdot \sin\left( \frac{1}{x} \right) = 0$$

In generale, ricordate questa regola che è molto utile nella risoluzione di problemi simili a quello appena proposto: quando una funzione oscillante e limitata viene moltiplicata per una potenza $x^n$ con $n$ intero positivo, il prodotto tende a zero per $x$ che tende a zero.

- - -

Consideriamo adesso il seguente limite:

$$\lim_{x \to +\infty} \frac{\ln(3 + \sin x)}{x^3} \tag{10}$$

Il numeratore oscilla ma resta limitato, mentre il denominatore tende a $+\infty.$ Per applicare il teorema del confronto, analizziamo l'argomento del logaritmo. Per prima cosa sappiamo che vale:

$$-1 \leq \sin x \leq 1 \tag{11}$$

Se aggiungiamo un $3$ a ciascun membro della $(11)$, per replicare la struttura dell'argomento del logaritmo, otteniamo:

$$2 \leq 3 + \sin x \leq 4$$

Applichiamo adesso la funzione logaritmo alla disuguaglianza e otteniamo:

$$\ln 2 \leq \ln(3 + \sin x) \leq \ln 4$$

Dividiamo adesso per il denominatore della $(10),$ ottenendo:

$$\frac{\ln 2}{x^3} \leq \frac{\ln(3 + \sin x)}{x^3} \leq \frac{\ln 4}{x^3}$$

Con questa riscrittura, per $x \to +\infty,$ la funzione minorante e la maggiorante tendono entrambe a zero e quindi anche il limite della $(10)$ tende a zero. Perciò possiamo scrivere:

$$\lim_{x \to +\infty} \frac{\ln(3 + \sin x)}{x^3} = 0$$

- - -

Calcoliamo ora il limite:

$$\lim_{x \to 0} \left( x^4 \cdot \cos\left( \frac{2}{x} \right) + 2 \right) \tag{12}$$

Come per il seno, anche la funzione coseno è compresa tra $-1$ e $1,$ quindi per ogni $x \neq 0$ vale la seguente disuguaglianza:

$$-1 \leq \cos\left( \frac{2}{x} \right) \leq 1$$

Moltiplicando i tre membri per $x^4,$ come nella $(12),$ otteniamo:

$$-x^4 \leq x^4 \cdot \cos\left( \frac{2}{x} \right) \leq x^4$$

Per $x$ che tende a $0$ i limiti della funzione minorante e maggiorante sono pari a zero e quindi, per il teorema del confronto si ha che:
$$\lim_{x \to 0} x^4 \cdot \cos\left( \frac{2}{x} \right) = 0$$

Come potete osservare è rimasto da calcolare il contributo della costante 2 della $(12)$, per cui, ricorrendo alle regole dell'algebra dei limiti, in particolare al limite della somma, otteniamo:

$$\lim_{x \to 0} \left( x^4 \cdot \cos\left( \frac{2}{x} \right) + 2 \right) = 0 + 2 = 2$$

Il limite della $(12)$ è quindi $2.$

## Un limite fondamentale

Vale la pena fare un ulteriore approfondimento del teorema del confronto applicato al caso di un limite fondamentale della trigonometria:

$$\lim_{x \to 0} \frac{\sin x}{x} = 1 \tag{13}$$

Consideriamo un angolo $x \in (0, \pi/2)$ sulla [circonferenza unitaria](../unit-circle/) e indichiamo con $O$ il centro, con $A$ il punto $(1, 0)$ sul semiasse positivo delle ascisse e con $P$ il punto della circonferenza individuato dall'angolo $x,$ misurato in senso antiorario a partire da $OA.$ Individuiamo adesso il punto $T$ dato dall'intersezione della semiretta $OP$ con la retta tangente verticale passante per $A.$ Abbiamo così ottenuto tre regioni:

+ il triangolo $OAP$
+ il settore circolare delimitato da $OA,$ $OP$ e dall'arco $AP$
+ il triangolo $OAT.$

Possiamo quindi procedere a confrontarle partendo dal primo punto, ovvero, dal triangolo $OAP$ la cui area è pari a

$$\mathrm{Area}(OAP) = \frac{1}{2} \sin x$$

![IMG. 2](squeeze-theorem-2.svg)


L'area del settore circolare del secondo punto è invece pari a

$$\mathrm{Area}(\text{settore}) = \frac{1}{2} x$$

![IMG. 3](squeeze-theorem-3.svg)

Infine, il triangolo $OAT$ ha area:

$$\mathrm{Area}(OAT) = \frac{1}{2} \tan x$$

![IMG. 3](squeeze-theorem-3.svg)

Da questa costruzione possiamo ricavare che il triangolo $OAP$ è contenuto nel settore circolare, che a sua volta è contenuto nel triangolo $OAT$ e pertanto le aree soddisfano la seguente disuguaglianza:

$$\frac{1}{2} \sin x < \frac{1}{2} x < \frac{1}{2} \tan x \tag{14}$$

Togliamo il denominatore dalla $(14)$ moltiplicando per $2$ e otteniamo:

$$\sin x < x < \tan x \tag{15}$$

Poiché $\sin x$ è strettamente positivo per $x \in (0, \pi/2),$ dividendo la $(15)$ per $\sin x,$ otteniamo:

$$1 < \frac{x}{\sin x} < \frac{1}{\cos x}$$

Il membro centrale è il reciproco della funzione presente nel limite della $(13)$, quindi possiamo riscrivere la $(15)$ passando al suo reciproco e ottenendo:

$$\cos x < \frac{\sin x}{x} < 1$$

La disuguaglianza appena ottenuta vale per $0 < x < \pi/2,$ quindi permette di studiare il rapporto $\sin x/x$ quando $x$ si avvicina a zero da destra. La funzione minorante $\cos x$ e la funzione maggiorante costante $1$ hanno entrambe limite uguale a $1$:

$$
\begin{align}
& \lim_{x \to 0^+} \cos x = 1 \\[6pt]
&\lim_{x \to 0^+} 1 = 1
\end{align}
$$

Quando $x$ si avvicina a zero da destra, $\cos x$ si avvicina a $1,$ mentre l'estremo superiore è già $1.$ Il rapporto $\sin x/x,$ compreso tra questi due valori, deve quindi avvicinarsi anch'esso a $1$ e dunque per il teorema del confronto otteniamo:

$$\lim_{x \to 0^+} \frac{\sin x}{x} = 1$$

Lo stesso risultato vale quando $x$ si avvicina a zero da sinistra. Infatti, cambiando il segno di $x,$ cambiano segno sia il seno sia il denominatore, e il rapporto rimane invariato:

$$\frac{\sin(-x)}{-x} = \frac{-\sin x}{-x} = \frac{\sin x}{x}$$

Il rapporto quindi tende a $1$ da entrambi i lati e pertanto possiamo concludere che il limite della $(13)$ è verificato.
