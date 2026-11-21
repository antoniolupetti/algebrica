---
title: Heine's Sequential Criterion for Limits
source: https://algebrica.org/heine-sequential-criterion-for-limits/
license: CC BY-NC 4.0
tags:
  - heine-theorem
  - limits
  - one-sided-limits
  - sequences
  - sequential-criterion
---

## Enunciato

Il criterio di Heine caratterizza il limite di una funzione attraverso i limiti delle successioni ottenute applicando la funzione ai termini di una successione di argomenti. In termini formali, consideriamo una funzione $f:A\to\mathbb{R},$ con $A\subseteq\mathbb{R},$ e sia $a\in\mathbb{R}$ un punto di accumulazione di $A.$ Fissato un valore $L\in\mathbb{R},$ vale la seguente equivalenza, nella quale la convergenza a destra è richiesta per ogni successione $(x_n)$ in $A\setminus\{a\}$ con $x_n\to a$:

$$
\lim_{x\to a}f(x)=L
\quad\Longleftrightarrow\quad
f(x_n)\to L \tag{1}
$$

Per dimostrare la prima implicazione della $(1)$ supponiamo che $f(x)\to L$ per $x\to a$ e prendiamo $(x_n)$ in $A\setminus\{a\}$ con $x_n\to a.$ Fissato $\varepsilon\gt0,$ per la definizione di limite esiste $\delta\gt0$ tale che, per ogni $x\in A,$ vale:

$$
0\lt|x-a|\lt\delta\implies |f(x)-L|\lt\varepsilon \tag{2}
$$

Poiché $x_n\to a$ e $x_n\neq a,$ esiste un indice $N$ tale che $0\lt|x_n-a|\lt\delta$ per ogni $n\geq N,$ quindi, per la scelta di $\delta,$ otteniamo:

$$
n\geq N\implies |f(x_n)-L|\lt\varepsilon \tag{3}
$$

Poiché $\varepsilon\gt0$ è arbitrario, la $(3)$ prova che $f(x_n)\to L$ e conclude la prima implicazione. Per l'implicazione inversa supponiamo che tutte le successioni ammissibili abbiano immagini convergenti a $L$ e dimostriamo per assurdo che $f(x)\to L.$ Se $f$ non tendesse a $L,$ esisterebbe un $\varepsilon_0\gt0$ tale che, per ogni $\delta\gt0,$ potremmo trovare un punto $x\in A$ dove valgono:

$$
\begin{align}
0\lt|x-a|\lt\delta \notag \\[6pt]
|f(x)-L|\geq\varepsilon_0 \tag{4}
\end{align}
$$

Applicando la $(4)$ con $\delta=1/n$ per ogni intero $n\geq1,$ potremmo scegliere una successione $(x_n)$ di punti di $A\setminus\{a\}$ tale che:

$$
\begin{align}
0\lt|x_n-a|\lt\frac{1}{n} \notag \\[6pt]
|f(x_n)-L|\geq\varepsilon_0 \tag{5}
\end{align}
$$

Nella $(5),$ la prima disuguaglianza dà $x_n\to a,$ poiché $1/n\to0,$ mentre la seconda esclude che $f(x_n)\to L$ e così abbiamo una successione ammissibile che contraddice l'ipotesi iniziale, per cui deve essere che $f(x)\to L.$

## Come escludere l'esistenza di un limite

La prima implicazione della $(1)$ permette di escludere l'esistenza di un limite confrontando due successioni ammissibili. Se le loro immagini tendono a valori diversi, la funzione non può avere limite, perché quel limite dovrebbe coincidere con entrambi i valori. Consideriamo il seguente esempio:

$$
f(x)=\sin\frac{1}{x} \tag{6}
$$

Per ottenere immagini con limiti diversi scegliamo gli argomenti in modo che il seno valga sempre $1$ lungo una successione e $-1$ lungo l'altra, quindi per ogni intero $n\geq1$ poniamo:

$$
\begin{align}
x_n&=\frac{1}{\pi/2+2\pi n} \notag \\[6pt]
y_n&=\frac{1}{3\pi/2+2\pi n} \tag{7}
\end{align}
$$

Le successioni nella $(7)$ hanno termini non nulli e tendono entrambe a zero, quindi sono ammissibili per il criterio di Heine in $a=0.$ Sostituendo i valori della $(7)$ nella $(6)$ e usando la periodicità del seno otteniamo:

$$
\begin{align}
f(x_n)&=\sin\left(\frac{\pi}{2}+2\pi n\right)=1 \notag \\[6pt]
f(y_n)&=\sin\left(\frac{3\pi}{2}+2\pi n\right)=-1 \tag{8}
\end{align}
$$

Nella $(8)$ abbiamo due limiti distinti che escludono l'esistenza di un unico limite di $f$ in $a.$ Il confronto tra i limiti della $(8)$ spiega anche perché nella $(1)$ occorre considerare tutte le successioni ammissibili. Infatti, scegliendo soltanto $z_n=1/(\pi n),$ avremmo $z_n\to0$ e $f(z_n)=0$ per ogni $n,$ ma questa convergenza non determina il limite della funzione, che abbiamo già escluso dalla $(8).$

## Come provare l'esistenza di un limite

Proviamo adesso il caso dell'esistenza di un limite usando l'implicazione inversa della $(1)$ e mostrando come le immagini di una successione arbitraria convergano. Consideriamo ad esempio la seguente funzione e studiamo il suo limite per $x\to0$:

$$
f(x)=
\begin{cases}
x & \text{se }x\in\mathbb{Q} \\[6pt]
-x & \text{se }x\in\mathbb{R}\setminus\mathbb{Q}
\end{cases}
\tag{9}
$$

Presa una successione arbitraria $(x_n)$ di numeri reali non nulli con $x_n\to0,$ otteniamo:

$$
|f(x_n)|=|x_n|\to0 \tag{10}
$$

La $(10)$ implica $f(x_n)\to0$ e questo risultato vale per ogni successione ammissibile, per cui, per la $(1),$ possiamo concludere che il limite esiste ed è pari a:

$$
\lim_{x\to0}f(x)=0 \tag{11}
$$

## Limiti laterali e infiniti

Il criterio di Heine permette di studiare anche i limiti da un solo lato, i limiti all'infinito e quelli in cui la funzione diverge, adattando le condizioni sulle successioni e sulle loro immagini. In particolare, per i limiti laterali si applica la $(1)$ alla parte di dominio situata dal lato considerato. Quindi, se $a$ è punto di accumulazione di $A\cap(a,+\infty),$ il limite destro si caratterizza mediante tutte le successioni $(x_n)$ di punti di questo insieme con $x_n\to a$:

$$
\lim_{x\to a^+}f(x)=L
\quad\Longleftrightarrow\quad
f(x_n)\to L \tag{12}
$$

Per il limite sinistro si considerano invece tutte le successioni in $A\cap(-\infty,a)$ con $x_n\to a,$ richiedendo che $a$ sia punto di accumulazione di questo insieme. Quando l'argomento tende a $+\infty,$ il dominio deve essere illimitato superiormente. La convergenza delle immagini è allora richiesta per ogni successione $(x_n)$ di punti di $A$ con $x_n\to+\infty$:

$$
\lim_{x\to+\infty}f(x)=L
\quad\Longleftrightarrow\quad
f(x_n)\to L \tag{13}
$$

Nel caso in cui $x\to-\infty$ si sostituisce nella $(13)$ la condizione $x_n\to+\infty$ con $x_n\to-\infty,$ richiedendo che $A$ sia illimitato inferiormente. Notate come nella $(13)$ sia l'argomento a tendere all'infinito, mentre $L$ è finito. Il criterio resta valido anche quando sono i valori della funzione a tendere a $\pm\infty$ e infatti, se $a$ è un punto di accumulazione finito di $A,$ per ogni successione $(x_n)$ in $A\setminus\{a\}$ con $x_n\to a$ si richiede la divergenza delle immagini:

$$
\lim_{x\to a}f(x)=+\infty
\quad\Longleftrightarrow\quad
f(x_n)\to+\infty \tag{14}
$$

Per dimostrare la $(14)$ si sostituisce nella $(2)$ la condizione $|f(x)-L|\lt\varepsilon$ con $f(x)\gt M,$ per ogni soglia $M\gt0.$ Il caso $L=-\infty$ segue applicando lo stesso risultato a $-f.$ Queste estensioni valgono anche in combinazione, per esempio per un limite destro uguale a $+\infty$ o per un limite infinito quando $x\to+\infty,$ con le rispettive condizioni sul dominio e sulle successioni.
