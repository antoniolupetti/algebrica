---
title: Algebra of Limits
source: https://algebrica.org/algebra-of-limits/
license: CC BY-NC 4.0
tags:
  - algebra-of-limits
  - continuous-functions
  - indeterminate-forms
  - limits
  - remarkable-limits
---
## Limite di una somma

Come abbiamo visto nella sua definizione, un limite descrive il comportamento di una funzione 𝑓(𝑥) quando 𝑥 si avvicina a un punto $x_0.$ Al dì là della determinazione del limite per sostituzione o con le tecniche per risolvere le forme indeterminate, nella maggior parte dei problemi è necessario ricorrere a delle operazioni che consentono di riscrivere le espressioni iniziali in forme più semplici, attraverso l'algebra dei limiti. Per approcciare il problema, definiamo due numeri reali $L$ e $M$ per cui valgano le seguenti identità:

$$
\begin{align}
\lim_{x \to x_0} f(x) &= L \notag \\[6pt]
\lim_{x \to x_0} g(x) &= M \tag{1}
\end{align}
$$

Sulla base della $(1)$ iniziamo a vedere come si comporta il limite di una somma di due funzioni tendono a valori finiti in prossimità di un certo punto. In parole semplici se $f$ tende a $L$ e $g$ a $M$ il limite della somma è pari alla somma dei limiti e si ha:

$$\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M \tag{2}$$

Per dimostrare la $(2),$ fissiamo un $\varepsilon \gt 0$ e per la $(1),$ con $x$ sufficientemente vicino a $x_0$ e $x \neq x_0,$ entrambi gli scarti $|f(x)-L|$ e $|g(x)-M|$ sono minori di $\varepsilon/2.$ Per la disuguaglianza triangolare si ha:

$$|f(x)+g(x)-(L+M)| \leq |f(x)-L|+|g(x)-M| \lt \varepsilon \tag{3}$$

La $(3)$ mostra quindi che la somma tende a $L+M.$ Come esempio della regola $(2)$ consideriamo le seguenti funzioni

$$
\begin{align}
f(x) &= \frac{\sin x}{x} \notag \\[6pt]
g(x) &= \frac{1 - \cos x}{x^2} \tag{4}
\end{align}
$$

Calcoliamo ora i seguenti limiti, ottenendo due valori finiti:

$$
\begin{align}
&\lim_{x \to 0} \frac{\sin x}{x} = 1 \notag \\[6pt]
&\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2} \tag{5}
\end{align}
$$

Quindi, usando i valori trovati nella $(5)$ e usando la regola $(2),$ otteniamo proprio che il limite della somma equivale alla somma dei limiti:

$$\lim_{x \to 0} \left(\frac{\sin x}{x}+\frac{1-\cos x}{x^2}\right) = 1 + \frac{1}{2} = \frac{3}{2} \tag{6}$$

La regola della somma $(2)$ vale anche per il limite della differenza. Sotto le ipotesi della $(1),$ vale:

$$\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M \tag{7}$$

Infatti, se $g(x)$ tende a $M,$ allora $-g(x)$ tende a $-M$ e applicando la $(2)$ si ottiene la $(7).$ Come esempio, consideriamo le seguenti funzioni:

$$
\begin{align}
f(x) &= \frac{x^2-1}{x-1} \notag \\[6pt]
g(x) &= \frac{x^3-1}{x-1} \tag{8}
\end{align}
$$

Le funzioni della $(8)$ non sono definite in $x=1,$ ma per calcolarne il limite basta considerare i valori con $x\neq1,$ per i quali è possibile semplificare il fattore $x-1.$ Osserviamo che le funzioni hanno al numeratore, rispettivamente, la differenza di due quadrati e la differenza di due cubi che possiamo quindi scomporre come segue:

$$
\begin{align}
\lim_{x \to 1} \frac{x^2-1}{x-1} &= \lim_{x \to 1}\frac{(x-1)(x+1)}{x-1} \notag \\[6pt]
\lim_{x \to 1} \frac{x^3-1}{x-1} &= \lim_{x \to 1}\frac{(x-1)(x^2+x+1)}{x-1} \tag{9}
\end{align}
$$

Dalla $(9)$ otteniamo i seguenti limiti:

$$
\begin{align}
&\lim_{x \to 1}(x+1) = 2 \notag \\[6pt]
&\lim_{x \to 1}(x^2+x+1) = 3 \tag{10}
\end{align}
$$

Applicando la $(7)$ con i limiti trovati nella $(10),$ otteniamo:

$$\lim_{x \to 1} \left(\frac{x^2-1}{x-1}-\frac{x^3-1}{x-1}\right) = 2-3 = -1 \tag{11}$$

Quindi abbiamo dimostrato che il limite della differenza è dato proprio dalla differenza dei due limiti.

## Limite del prodotto

Oltre alla somma e alla differenza, se $f(x)$ tende a un valore finito $L,$ come nella $(1),$ per ogni costante reale $c$ vale la seguente relazione:

$$\lim_{x \to x_0} c f(x) = c L \tag{12}$$

Per $c=0$ la dimostrazione è banale in quanto il prodotto è nulle. Quando invece $c \neq 0,$ abbiamo che vale la seguente relazione lineare:

$$|cf(x)-cL|=|c||f(x)-L|$$ 
Quindi anche il limite è un'operazione lineare. Per fare un esempio, calcoliamo il seguente limite:

$$\lim_{x \to 0} 3\frac{\ln(1+x)}{x} \tag{13}$$

Per sostituzione diretta il quoziente non è definito in $x=0,$ ma la $(13)$ ha il seguente limite notevole:

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1 \tag{13}$$

Applicando la $(12)$ con $c=3$ e usando il limite ottenuto nella $(13),$ otteniamo:

$$\lim_{x \to 0} 3\frac{\ln(1 + x)}{x} = 3\lim_{x \to 0}\frac{\ln(1 + x)}{x} = 3 \cdot 1 = 3 \tag{14}$$

Vediamo ora il caso in cui entrambi i fattori sono funzioni che hanno limiti finiti, come nelle ipotesi della $(1),$ e calcoliamo il limite del prodotto che è dato dal prodotto dei rispettivi limiti:

$$\lim_{x \to x_0} \big(f(x)g(x)\big) = LM \tag{15}$$

Per dimostrare la $(15),$ riscriviamo lo scarto dal valore $LM$ e applichiamo la disuguaglianza triangolare, ottenendo:

$$|f(x)g(x)-LM| \leq |f(x)||g(x)-M|+|M||f(x)-L| \tag{16}$$

Poiché $f(x)$ tende a un valore finito, è limitata vicino a $x_0$ e per la $(1),$ entrambi gli scarti nella $(16)$ tendono a zero, quindi anche il prodotto tende a $LM.$ Ad sesmpio, consideriamo le seguentifunzioni:

$$
\begin{align}
&f(x) = \frac{e^x-1}{x} \notag \\[6pt]
&g(x) = \frac{\ln(1+x)}{x} \tag{17}
\end{align}
$$

Le funzioni nella $(17)$ non sono definite in $x=0,$ ma i loro limiti sono notevoli notevoli (il secondo lo abbiamo visto nella $(13)$:

$$
\begin{align}
&\lim_{x \to 0} \frac{e^x-1}{x} = 1 \notag \\[6pt]
&\lim_{x \to 0} \frac{\ln(1+x)}{x} = 1 \tag{18}
\end{align}
$$

Applicando la $(15)$ con i valori della $(18),$ otteniamo la regola generale della $(15)$:

$$\lim_{x \to 0} \frac{(e^x-1)\ln(1+x)}{x^2} = 1 \cdot 1 = 1 \tag{19}$$

## Limite di un quoziente

Consideriamo adesso il limite del quoziente per il quale, sotto le ipotesi della $(1),$ vale la seguente relazione:

$$\lim_{x \to x_0} \frac{f(x)}{g(x)} = \frac{L}{M}\tag{20}$$

Nella $(20),$ M e $g(x)$ devono essere diversi da zero. In particolare la prima condizione garantisce che, per $x$ sufficientemente vicino a $x_0$ e diverso da $x_0,$ si abbia la seguente maggiorazione:

$$|g(x)| \gt |M|/2$$

In questo modo il denominatore è non nullo e lo scarto del suo reciproco soddisfa la seguente catena di relazioni:

$$\left|\frac{1}{g(x)}-\frac{1}{M}\right| = \frac{|g(x)-M|}{|g(x)||M|} \leq \frac{2}{|M|^2}|g(x)-M| \tag{21}$$

Per la $(1),$ l'ultimo membro della $(21)$ tende a zero, quindi $1/g(x)$ tende a $1/M.$ A questo punto, applicando la regola del prodotto $(15)$ si ottiene la $(20).$ Quando invece $M=0,$ la regola non si applica e il quoziente richiede un'analisi separata, come ne caso della forma intederminata $0/0.$ Consideriamo quindi le seguenti funzioni e calcoliamo il limite del loro quoziente.:

$$
\begin{align}
f(x) = \frac{e^x-1}{x} &\notag \\[6pt]
g(x) = \frac{x^2+1}{x+1} &\tag{22}
\end{align}
$$

Per $f$ usiamo il limite notevole già riportato nella $(18).$ La funzione $g$ è invece continua in $x=0,$ quindi il suo limite si calcola per sostituzione. In questo modo otteniamo:

$$
\begin{align}
&\lim_{x \to 0}\frac{e^x-1}{x} = 1 \notag \\[6pt]
&\lim_{x \to 0}\frac{x^2+1}{x+1} = \frac{0+1}{0+1} = 1 \tag{23}
\end{align}
$$

Applicando la $(20),$ quindi otteniamo:

$$\lim_{x \to 0}\frac{\dfrac{e^x-1}{x}}{\dfrac{x^2+1}{x+1}} = \frac{1}{1} = 1 \tag{24}$$


## Limiti di potenze e polinomi

La regola del prodotto mostrata nella $(15)$ permette di calcolare anche il limite di una potenza. Sempre sotto le ipotesi della $(1),$ per ogni intero positivo $n$ si ha:

$$\lim_{x \to x_0}\big(f(x)\big)^n = L^n \tag{25}$$

Per dimostrare la $(25),$ il caso $n=1$ coincide con l'ipotesi sul limite di $f;$ ogni passaggio da $n$ a $n+1$ segue applicando la regola del prodotto $(15)$ a $f(x)^n$ e $f(x).$ Combinando poi la $(25)$ con le regole della somma $(2)$ e del prodotto per una costante $(12),$ si ottiene il limite di un polinomio $P(x)$ e si ha:

$$\lim_{x \to x_0}P(x) = a_0+a_1x_0+\cdots+a_nx_0^n = P(x_0) \tag{26}$$

Come esempio della regola della potenza, calcoliamo il seguente limite:

$$\lim_{x \to 0}\left(\frac{\ln(1+2x)}{x}\right)^4 \tag{27}$$

Procediamo per passi, calcolando per prima cosa il limite della base, moltiplicando numeratore e denominatore per $2$ e ponendo $t=2x,$ in modo che $t \to 0$ per $x \to 0.$ Usando la $(12)$ e il limite notevole già visto nella $(18),$ otteniamo:

$$
\begin{align}
\lim_{x \to 0}\frac{\ln(1+2x)}{x}
&= \lim_{x \to 0}\frac{2\ln(1+2x)}{2x} \notag \\[6pt]
&= 2\lim_{x \to 0}\frac{\ln(1+2x)}{2x} \notag \\[6pt]
&= 2\lim_{t \to 0}\frac{\ln(1+t)}{t} \notag \\[6pt]
&= 2 \cdot 1 = 2 \tag{28}
\end{align}
$$

Quindi la base tende a $2$ e applicando la $(25)$ con $n=4,$ otteniamo:

$$\lim_{x \to 0}\left(\frac{\ln(1+2x)}{x}\right)^4 = \left(\lim_{x \to 0}\frac{\ln(1+2x)}{x}\right)^4 = 2^4 = 16 \tag{29}$$

## Limite di una composizione

Vediamo ora come si comporta il limite nel caso di una composizione tra funzioni della forma $\varphi(f(x)).$ In questo caso se $f(x)$ tende al valore finito $L,$ come nella $(1),$ e $\varphi$ è continua in $L,$ vale la seguente relazione:

$$\lim_{x \to x_0}\varphi(f(x)) = \varphi\left(\lim_{x \to x_0}f(x)\right) = \varphi(L) \tag{30}$$

Per dimostrare il risultato della $(30)$ supponiamo che la composizione sia definita per $x$ sufficientemente vicino a $x_0$ e con $x \neq x_0.$ La continuità in $L$ garantisce che, quando $f(x)$ tende a $L,$ il valore $\varphi(f(x))$ tenda a $\varphi(L).$ Per mostrare la $(30)$ in pratica calcoliamo il seguente limite:

$$\lim_{x \to 0}e^{\frac{\sqrt{1+x}-1}{x}} \tag{31}$$

Per prima cosa separiamo le due funzioni, ottenendo:

$$
\begin{align}
f(x) &= \frac{\sqrt{1+x}-1}{x} \notag \\[6pt]
\varphi(t) &= e^t \tag{32}
\end{align}
$$

Calcoliamo prima il limite di $f(x),$ ottenendo:

$$
\begin{align}
\lim_{x \to 0}\frac{\sqrt{1+x}-1}{x}
&= \lim_{x \to 0}\frac{(\sqrt{1+x}-1)(\sqrt{1+x}+1)}{x(\sqrt{1+x}+1)} \notag \\[6pt]
&= \lim_{x \to 0}\frac{x}{x(\sqrt{1+x}+1)} \notag \\[6pt]
&= \lim_{x \to 0}\frac{1}{\sqrt{1+x}+1} = \frac{1}{2} \tag{33}
\end{align}
$$

La funzione esponenziale è continua in $t=1/2,$ quindi:

$$\lim_{t \to 1/2}e^t = e^{1/2} \tag{34}$$

Poiché nella $(33)$ la funzione interna tende a $1/2,$ applicando la regola della composizione $(30)$ otteniamo:

$$\lim_{x \to 0}e^{\frac{\sqrt{1+x}-1}{x}} = e^{1/2} = \sqrt{e} \tag{35}$$

## Riepilogo

La tabella riassume le regole dimostrate sotto le ipotesi della $(1).$ Per il quoziente si richiede $M \neq 0,$ come nella $(20).$ Per la potenza, $n$ è un intero positivo, come nella $(25)$ mentre per la composizione, $\varphi$ deve essere continua in $L$ e definita sui valori assunti da $f$ vicino a $x_0,$ come nella $(30).$

[class="table-1"]

|                       |                                                            |
| --------------------- | ---------------------------------------------------------- |
| Somma                 | $\lim_{x \to x_0} \big( f(x) + g(x) \big) = L + M$         |
| Differenza            | $\lim_{x \to x_0} \big( f(x) - g(x) \big) = L - M$         |
| Prodotto per costante | $\lim_{x \to x_0} c f(x) = c L$                            |
| Prodotto di funzioni  | $\lim_{x \to x_0} \big( f(x) \cdot g(x) \big) = L \cdot M$ |
| Quoziente             | $\lim_{x \to x_0} \dfrac{f(x)}{g(x)} = \dfrac{L}{M}$       |
| Potenza               | $\lim_{x \to x_0} \big( f(x) \big)^n = L^n$                |
| Composizione          | $\lim_{x \to x_0} \varphi(f(x)) = \varphi(L)$              |
[/class]

Se uno dei limiti è infinito o il denominatore di un quoziente tende a zero, occorre un'analisi separata, perché vengono meno le ipotesi delle regole enunciate e in alcuni casi possiamo ottenere delle forme indeterminate che sono trattate nella voce dedicata.
