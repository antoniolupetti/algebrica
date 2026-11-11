---
title: Complex Logarithm
source: https://algebrica.org/complex-logarithm/
license: CC BY-NC 4.0
tags:
  - branch-cut
  - complex-argument
  - complex-exponential
  - complex-logarithm
  - complex-numbers
  - principal-logarithm
---
## Definizione e proprietà

Il logaritmo complesso di un numero complesso $z \neq 0$ è un numero $w\in\mathbb{C}$ che soddisfa l'equazione:

$$e^w=z \tag{1}$$

Come sappiamo, nei numeri reali il logaritmo naturale è la funzione inversa dell'esponenziale, che è una biezione da $\mathbb{R}$ a $(0,\infty).$ Per questo ogni numero reale positivo ha un unico logaritmo reale. Nel campo complesso, le cose si complicano poiché l'esponenziale complesso è invece periodico e per ogni $w\in\mathbb{C}$ e ogni $k\in\mathbb{Z}$ vale la seguente identità:

$$e^{w+2k\pi i}=e^w \tag{2}$$

Dalla $(2)$ segue che, se $w$ è una soluzione della $(1),$ anche $w+2k\pi i$ lo è per ogni $k\in\mathbb{Z}.$ Quindi per determinare tutte le soluzioni della $(1)$, scriviamo $w=u+iv$ con $u,v\in\mathbb{R}$ e $z=re^{i\theta},$ dove $r=|z|$ e $\theta$ è un argomento di $z.$ Per la formula di Eulero vale:

$$e^w=e^{u+iv}=e^u(\cos v+i\sin v) \tag{3}$$

Dal confronto tra la $(3)$ e la forma esponenziale di $z$ segue che la $(1)$ vale se e solo se i moduli coincidono, cioè $e^u=r,$ e gli argomenti differiscono di un multiplo intero di $2\pi,$ cioè $v=\theta+2k\pi$ per qualche $k\in\mathbb{Z}.$ Poiché $r>0,$ l'equazione reale $e^u=r$ dà $u=\ln r.$ L'insieme dei logaritmi complessi di $z$ è quindi dato da:

$$\log z:=\{\ \ln|z|+i(\theta+2k\pi)\mid k\in\mathbb{Z}\ \} \tag{4}$$

A livello geometrico, nel piano complesso, i logaritmi rappresentati dalla $(4)$ giacciono tutti sulla retta verticale di ascissa $\ln|z|,$ con una distanza di $2\pi$ tra due valori consecutivi.

- - -

Per $z\neq0,$ il logaritmo principale $\mathrm{Log}(z)$ è il valore della $(4)$ ottenuto scegliendo $\mathrm{Arg}(z),$ l'unico argomento di $z$ in $(-\pi,\pi]:$

$$\mathrm{Log}(z):=\ln|z|+i\mathrm{Arg}(z) \tag{5}$$

La $(5)$ dà un solo valore, mentre $\log z$ indica l'insieme di tutti i logaritmi di $z.$ Per $x>0$ si ha $\mathrm{Arg}(x)=0$ e $\mathrm{Arg}(-x)=\pi,$ quindi:

$$
\begin{align}
\mathrm{Log}(x)&=\ln x \notag\\[6pt]
\mathrm{Log}(-x)&=\ln x+i\pi \tag{6}
\end{align}
$$

Per la $(6),$ sul semiasse reale positivo il logaritmo principale coincide con il logaritmo naturale. Per esempio il numero complesso $z=-\sqrt{3}-i$ si trova nel terzo quadrante e ha modulo e argomento principale pari a:

$$
\begin{aligned}
|z|&=\sqrt{(-\sqrt{3})^2+(-1)^2}=2\\[6pt]
\mathrm{Arg}(z)&=-\frac{5\pi}{6}
\end{aligned} \tag{7}
$$

Sostituendo i valori della $(7)$ nella $(5)$ otteniamo:

$$\mathrm{Log}(-\sqrt{3}-i)=\ln 2-\frac{5\pi i}{6} \tag{8}$$

Usando la $(4)$ otteniamo l'insieme completo di tutti i logaritmi complessi:

$$\log(-\sqrt{3}-i)=\left\{\ \ln 2+i\left(-\frac{5\pi}{6}+2k\pi\right)\mid k\in\mathbb{Z}\ \right\} \tag{9}$$

Nella $(9)$ quando $k=0$ si ottiene il logaritmo principale della $(8).$ Per ogni $z\neq0,$ il logaritmo principale è una soluzione della $(1),$ quindi:

$$e^{\mathrm{Log}(z)}=z \tag{10}$$

Se invertiamo l'ordine delle operazioni nella $(10),$ la $(5)$ seleziona il logaritmo con parte immaginaria in $(-\pi,\pi].$ Si ritrova quindi $w$ esattamente quando la sua parte immaginaria è già in quell'intervallo:

$$\mathrm{Log}(e^w)=w \quad\Longleftrightarrow\quad -\pi<\mathrm{Im}(w)\leq\pi \tag{11}$$

La restrizione nella $(11)$ si vede già con $w=2\pi i,$ per cui $e^w=1$ e $\mathrm{Log}(1)=0.$

- - -

Vediamo adesso le principali proprietà del logaritmo complesso partendo dal logaritmo del prodotto. Per due numeri complessi non nulli $z_1$ e $z_2$ vale la seguente relazione:

$$\log(z_1z_2)=\log z_1+\log z_2 \tag{12}$$

La $(12)$ è un'uguaglianza tra insiemi, quindi nel membro di destra si sommano un logaritmo di $z_1$ e uno di $z_2$ in tutti i modi possibili. Se $\theta_1$ e $\theta_2$ sono gli argomenti dei due fattori, dalla $(4)$ e per qualunque $k\in\mathbb{Z}$ si ottengono tutte le somme della forma:

$$\ln|z_1|+\ln|z_2|+i(\theta_1+\theta_2+2k\pi) \tag{13}$$

Per il logaritmo principale abbiamo invece:

$$\mathrm{Log}(z_1z_2)=\mathrm{Log}(z_1)+\mathrm{Log}(z_2)-2m\pi i \tag{14}$$

Nella $(14),$ l'intero $m$ si determina imponendo che $\mathrm{Arg}(z_1)+\mathrm{Arg}(z_2)-2m\pi$ appartenga a $(-\pi,\pi].$