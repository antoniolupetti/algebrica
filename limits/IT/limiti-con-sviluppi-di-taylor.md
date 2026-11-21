---
title: Limits Using Taylor Expansions
source: https://algebrica.org/limits-using-taylor-expansions/
license: CC BY-NC 4.0
tags:
  - indeterminate-forms
  - limits
  - little-o-notation
  - peano-remainder
  - taylor-polynomial
---

## Sviluppi di Taylor

Come sappiamo, lo sviluppo in serie di Taylor permette di esprimere una funzione in un punto come la somma di un polinomio e di un resto. Questa scrittura è molto utile nei casi in cui il calcolo del limite tramite sostituzione diretta produce una forma indeterminata, perché consente di semplificare l'espressione iniziale e di individuare i termini rimanenti, così da verificare il contributo dell'errore. Supponiamo quindi di avere una funzione $f$ definita in un intorno di $x_0$ e derivabile $n$ volte in $x_0,$ con $n\geq1.$ Questo metodo è preferibile alla regola di de l'Hôpital o alle manipolazioni algebriche quando queste richiedono calcoli molto lunghi, perché consente di determinare il valore del limite in modo più immediato. Per $x\to x_0$ la formula di Taylor con il resto di Peano è data dalla seguente uguaglianza: 

$$
f(x)=\sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k+o\big((x-x_0)^n\big) \tag{1}
$$

Il polinomio ottenuto nella $(1)$ ha gli stessi valori delle derivate di $f$ fino all'ordine $n$ nel punto $x_0,$ mentre il resto è la differenza tra la funzione e il polinomio, e la notazione o piccolo significa che:

$$
\lim_{x\to x_0}\frac{f(x)-\displaystyle\sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k}{(x-x_0)^n}=0 \tag{2}
$$

La $(2)$ giustifica l'uso dello sviluppo nei limiti, perché il resto, una volta diviso per $(x-x_0)^n,$ tende a zero e quindi non contribuisce al valore del limite. Quando nella $(2)$ $x_0=0,$ lo sviluppo prende anche il nome di sviluppo di Maclaurin. Per gli sviluppi delle funzioni elementari, utili a risolvere i problemi, si rimanda alla relativa voce.

## Scegliere l'ordine dello sviluppo

Quando vogliamo applicare questo metodo al calcolo dei limiti, per prima cosa è necessario scegliere fino a quale ordine sviluppare le funzioni, perché alcuni termini possono cancellarsi e il resto deve essere abbastanza piccolo da tendere a zero dopo la divisione per il denominatore. Consideriamo, per esempio, il seguente limite:

$$
\lim_{x\to0}\frac{\cos x-1+\dfrac{x^2}{2}}{x^4} \tag{3}
$$

Se ci fermiamo allo sviluppo di ordine $2$ della $(3)$ otteniamo:

$$\cos x=1-x^2/2+o(x^2)$$

Questa espansione però non è sufficiente perché il rapporto $o(x^2)/x^4$ non tende necessariamente a zero e il resto potrebbe contenere un termine di grado quattro che contribuisce al limite. Proseguendo lo sviluppo fino al grado $4$ otteniamo:
$$
\begin{align}
\cos x-1+\frac{x^2}{2}&=1-\frac{x^2}{2}+\frac{x^4}{24}+o(x^4)-1+\frac{x^2}{2} \notag \\[6pt]
&=\frac{x^4}{24}+o(x^4) \tag{4}
\end{align}
$$

Dividendo la $(4)$ per $x^4,$ il resto diventa $o(1)$ e il limite nella $(3)$ vale $1/24.$ A livello generale, supponiamo che il denominatore abbia la seguente forma, con $b\neq0$ e $m$ intero positivo: 
$$bx^m+o(x^m)$$

La regola generale è sviluppare il numeratore complessivo fino all'ordine $m,$ in modo che il resto, dopo la divisione per il denominatore, tenda a zero. Se i termini di grado inferiore si cancellano e rimane $ax^m+o(x^m),$ abbiamo:

$$
\lim_{x\to0}\frac{ax^m+o(x^m)}{bx^m+o(x^m)}
=\lim_{x\to0}\frac{a+o(1)}{b+o(1)}=\frac ab \tag{5}
$$

Se anche il coefficiente $a$ è nullo, il numeratore è $o(x^m)$ e il limite è zero. Se invece al numeratore rimane un termine non nullo di grado inferiore a $m,$ il rapporto non può avere un limite finito e non occorre proseguire lo sviluppo, perché i termini di grado superiore non possono cancellare quello già individuato. In questo caso si studia allora il segno del rapporto per stabilire se il limite è infinito oppure se i due limiti laterali sono infiniti di segno opposto.

## Operazioni e controllo del resto

Per gli sviluppi in serie di Taylor valgono le comuni operazioni algebriche che conservano il controllo dei resti. Per $x\to0$ valgono le seguenti relazioni:

$$
\begin{align}
o(x^m)+o(x^m)&=o(x^m) \notag \\[6pt]
x^r o(x^m)&=o(x^{m+r}) \notag \\[6pt]
\frac{o(x^m)}{x^r}&=o(x^{m-r}) \tag{6}
\end{align}
$$

Vediamo un caso pratico di applicazione delle regole della $(6)$ calcolando il seguente limite per cui la sostituzione diretta dà la forma indeterminata $0/0:$ 

$$
\lim_{x\to0}\frac{e^x-1-x}{\sin^2 x} \tag{7}
$$

Al numeratore usiamo lo sviluppo $e^x=1+x+x^2/2+o(x^2),$ ottenendo $x^2/2+o(x^2).$ Al denominatore basta lo sviluppo $\sin x=x+o(x),$ perché dobbiamo poi elevarlo al quadrato ottenendo:

$$
\sin^2 x=(x+o(x))^2=x^2+o(x^2) \tag{8}
$$

Applicando le $(5)$ e $(8)$ otteniamo:

$$
\lim_{x\to0}\frac{e^x-1-x}{\sin^2 x}
=\lim_{x\to0}\frac{\dfrac{x^2}{2}+o(x^2)}{x^2+o(x^2)}=\frac12 \tag{9}
$$

## Sviluppi di funzioni composte

Nei limiti possono comparire funzioni composte, come $e^{x^2},$ in cui l'argomento dell'esponenziale è $x^2$ anziché $x.$ Per svilupparle possiamo partire dallo sviluppo della funzione esterna nell'origine e sostituire alla sua variabile l'espressione interna, purché quest'ultima tenda a zero. La sostituzione va effettuata anche nel resto, il cui ordine deve essere espresso rispetto alla variabile del limite. Consideriamo, per esempio, il seguente limite:

$$
\lim_{x\to0}\frac{e^{x^2}-\cos x-\dfrac32x^2}{x^4} \tag{10}
$$

Per l'esponenziale poniamo $t=x^2$ e, poiché $t\to0,$ possiamo usare lo sviluppo di $e^t$ fino all'ordine due in modo che $t^2$ diventi $x^4$ e il resto $o(t^2)$ diventi $o(x^4),$ perciò si ha:

$$
\begin{align}
e^{x^2}&=1+x^2+\frac{x^4}{2}+o(x^4) \notag \\[6pt]
\cos x&=1-\frac{x^2}{2}+\frac{x^4}{24}+o(x^4) \tag{11}
\end{align}
$$

Sostituendo le $(11)$ e apportando le cancellazioni rimane:

$$
e^{x^2}-\cos x-\frac32x^2=\frac{11}{24}x^4+o(x^4) \tag{12}
$$

Nella $(12),$ dopo la divisione per $x^4,$ il resto tende a zero e il limite nella $(10)$ vale $11/24.$

## Forme esponenziali

Gli sviluppi di Taylor permettono anche di trattare le forme come $1^\infty,$ passando al logaritmo e risolvendo. Ad esempio, consideriamo il seguente limite che non è risolvibile per sostituzione diretta:

$$
\lim_{x\to0}\left(\frac{\sin x}{x}\right)^{1/x^2} \tag{13}
$$

Poniamo $y(x)=(\sin x/x)^{1/x^2}.$ Poiché $\sin x/x$ tende a $1,$ la base è positiva per $x$ sufficientemente vicino a zero, con $x\neq0,$ e possiamo applicare il logaritmo, ottenendo:

$$
\ln y(x)=\frac{1}{x^2}\ln\left(\frac{\sin x}{x}\right) \tag{14}
$$

A questo punto usiamo lo sviluppo $\sin x=x-x^3/6+o(x^3)$ e dividendo per $x,$ possiamo scrivere la base nella forma $1+u(x)$ e individuare il termine $u(x):$

$$
\begin{align}
\frac{\sin x}{x}&=1+u(x) \notag \\[6pt]
u(x)&=-\frac{x^2}{6}+o(x^2) \tag{15}
\end{align}
$$

Adesso usiamo lo sviluppo $\ln(1+u)=u+o(u)$ e dalla $(15)$ segue che $u(x)/x^2\to-1/6,$ quindi il resto $o(u(x))$ è anche $o(x^2).$ Perciò la $(14)$ diventa:

$$
\ln y(x)=\frac{-\dfrac{x^2}{6}+o(x^2)}{x^2}\longrightarrow-\frac16 \tag{16}
$$

Per la continuità dell'esponenziale, da $y(x)=e^{\ln y(x)}$ segue che il limite della $(13)$ vale $e^{-1/6}.$

## Punti diversi da zero e limiti all'infinito

Gli sviluppi di Taylor nell'origine si possono usare anche quando la variabile tende a un altro punto. Infatti, per un limite con $x\to a$ si può porre $h=x-a,$ così che $h\to0.$ Per esempio, riscriviamo il seguente limite:

$$
\lim_{x\to1}\frac{\ln x-(x-1)}{(x-1)^2}
=\lim_{h\to0}\frac{\ln(1+h)-h}{h^2} \tag{17}
$$

Lo sviluppo $\ln(1+h)=h-h^2/2+o(h^2)$ mostra che il numeratore nella $(17)$ è $-h^2/2+o(h^2).$ Dividendo per $h^2,$ otteniamo quindi il limite $-1/2.$ Nel caso all'infinito possiamo invece introdurre la variabile $t=1/x$ per ottenere il nostro risultato. Consideriamo, ad esempio, il seguente limite che per sostituzione diretta determina la forma indeterminata $\infty-\infty:$

$$
\lim_{x\to+\infty}\left(\sqrt{x^2+x}-x\right) \tag{18}
$$

Poiché $x\gt0,$ raccogliamo $x$ dalla radice e poniamo $t=1/x.$ Quando $x\to+\infty,$ abbiamo $t\to0^+$ e l'espressione diventa:

$$
\sqrt{x^2+x}-x=x\left(\sqrt{1+\frac1x}-1\right)=\frac{\sqrt{1+t}-1}{t} \tag{19}
$$

A questo punto, nello sviluppo della potenza scegliamo $\alpha=1/2$ e conserviamo i termini fino al primo ordine:

$$
\sqrt{1+t}=1+\frac t2+o(t) \tag{20}
$$

Sostituendo la $(20)$ nella $(19),$ i termini costanti si cancellano e otteniamo:

$$
\lim_{t\to0^+}\frac{\dfrac t2+o(t)}{t}=\frac12 \tag{21}
$$

