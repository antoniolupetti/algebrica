---
title: Complex Powers
source: https://algebrica.org/complex-powers/
license: CC BY-NC 4.0
tags:
  - complex-exponential
  - complex-logarithm
  - complex-numbers
  - complex-powers
---
## Definizione

La potenza complessa di base $z\neq 0$ ed esponente $a\in\mathbb{C}$ è l'insieme dei valori che si ottengono moltiplicando ciascun logaritmo complesso di $z$ per $a$ e applicando l'esponenziale:

$$z^a:=\{\ e^{aw}\mid w\in\log z\ \} \tag{1}$$

Fissiamo il modulo $r=|z|$ e un argomento $\theta$ di $z.$ Ogni intero $k$ individua un logaritmo di $z,$ con parte reale $\ln r$ e parte immaginaria $\theta+2k\pi.$ Sostituendo questo logaritmo al posto di $w$ nella $(1),$ otteniamo il seguente valore:

$$v_k(a)=e^{a(\ln r+i(\theta+2k\pi))} \tag{2}$$

Al variare di $k$ tra gli interi, la $(2)$ usa tutti i logaritmi di $z,$ quindi dà lo stesso insieme di valori di $z^a$ qualunque sia l'argomento $\theta$ da cui partiamo. Il valore principale della potenza $z^a$ si ottiene usando il logaritmo principale $\mathrm{Log}(z),$ che sceglie l'argomento di $z$ in $(-\pi,\pi].$ Nella $(2)$ questa scelta corrisponde a $k=0$ quando $\theta=\mathrm{Arg}(z):$

$$z_{\mathrm{pr}}^a:=e^{a\mathrm{Log}(z)} \tag{3}$$

Quando $z=x>0,$ il logaritmo principale è $\ln x,$ quindi per $a$ reale la $(3)$ coincide con la potenza reale. Vediamo ora come si calcola il caso $i^i$ nella $(2)$ ponendo $\ln r=0,$ $\theta=\pi/2$ e $a=i.$ Il prodotto di $i$ per $i(\pi/2+2k\pi)$ è reale e uguale a $-\pi/2-2k\pi,$ perciò si ha:

$$i^i=\{\ e^{-\pi/2-2k\pi}\mid k\in\mathbb{Z}\ \} \tag{4}$$

Tutti i valori della $(4)$ sono numeri reali positivi e, quando $k=0,$ otteniamo il valore principale, pari a $e^{-\pi/2}.$

## Proprietà

Vediamo ora alcune proprietà delle potenze complesse partendo dal numero di valori distinti della potenza $z^a,$ che dipende soltanto dall'esponente $a.$ Per capire perché questo accade, cerchiamo quando due indici $k$ e $j$ danno lo stesso valore della potenza. Iniziamo col sottrarre gli esponenti nel rapporto $v_k(a)/v_j(a)$ tra i valori della $(2).$ I termini che contengono il modulo $r$ e l'argomento $\theta$ si cancellano e il rapporto diventa:

$$\frac{v_k(a)}{v_j(a)}=e^{2\pi i(k-j)a}$$

I valori $v_k(a)$ e $v_j(a)$ coincidono se e solo se il rapporto appena calcolato è uguale a $1.$ L'esponenziale complesso vale $1$ esattamente per i multipli interi di $2\pi i,$ da cui segue:

$$
\begin{aligned}
v_k(a)=v_j(a) &\quad\Longleftrightarrow\quad e^{2\pi i(k-j)a}=1 \\[6pt]
              &\quad\Longleftrightarrow\quad (k-j)a\in\mathbb{Z}
\end{aligned} \tag{5}
$$

Se l'esponente è razionale, scriviamo $a=p/q$ come frazione ridotta ai minimi termini, con $q>0,$ e applichiamo la $(5),$ secondo cui i valori $v_k(a)$ e $v_j(a)$ coincidono se e solo se $(k-j)p/q$ è un intero. Poiché $p$ e $q$ sono coprimi, ciò accade quando $k-j$ è un multiplo di $q,$ perciò i valori si ripetono ogni $q$ indici e quelli da $0$ a $q-1$ danno tutti i $q$ valori distinti della potenza, dato che nessuna coppia di indici distinti in questo intervallo differisce di un multiplo di $q.$

Nel caso di un esponente intero $a=n,$ il denominatore è $q=1,$ quindi il valore è unico e si ritrova la potenza intera, perché $e^{nw}=(e^w)^n=z^n$ per ogni logaritmo $w$ di $z.$ Per $a=1/q,$ invece, si ottengono tutte le radici $q$-esime di $z.$ Infatti, per ogni logaritmo $w$ di $z,$ elevando $e^{w/q}$ alla potenza $q$ si ottiene $e^w=z.$

Infine, quando $a$ è reale irrazionale oppure ha parte immaginaria diversa da zero, nessun multiplo intero non nullo di $a$ è un intero, quindi per la $(5),$ indici distinti danno valori distinti e la potenza ha infiniti valori.

- - -

Un'altra proprietà è data dalla legge di somma degli esponenti secondo cui per ogni coppia di esponenti $a,b\in\mathbb{C}$ vale la seguente relazione:

$$e^{aw}e^{bw}=e^{(a+b)w} \tag{6}$$

Facendo variare $w$ nella $(6)$ si ottengono tutti i valori di $z^{a+b},$ mentre scegliendo $w=\mathrm{Log}(z)$ per entrambi i fattori si ottiene la stessa identità per i valori principali. Se invece si sceglie il logaritmo separatamente per ciascun fattore, il prodotto può dare valori ulteriori, come quando si moltiplicano tra loro le due radici quadrate di $1,$ cioè $1$ e $-1,$ e si ottiene $-1,$ mentre $1^1$ ha come unico valore $1.$ Per la potenza di un prodotto, invece, se $w_1$ e $w_2$ sono logaritmi di $z_1$ e $z_2,$ allora $w_1+w_2$ è un logaritmo di $z_1z_2$ e da questa scelta segue la seguente identità:

$$e^{a(w_1+w_2)}=e^{aw_1}e^{aw_2} \tag{7}$$

Anche quando $w_1$ e $w_2$ sono i logaritmi principali, la loro somma può avere parte immaginaria fuori da $(-\pi,\pi],$ nel qual caso il primo membro della $(7)$ è calcolato con un logaritmo diverso da quello principale. Questo è ciò che accade quando $z_1=z_2=-1$ e $a=1/2,$ perché il valore principale della potenza del prodotto è $1,$ mentre il prodotto dei valori principali è $i\cdot i=-1.$

La scelta del logaritmo interviene anche nella potenza di una potenza, perché, se $u=e^{aw}$ è un valore di $z^a,$ usando $aw$ come logaritmo di $u$ si ottiene $e^{baw}$ come valore di $u^b.$ Il logaritmo principale di $u$ può dare un risultato diverso, come accade con $z=-1,$ $a=2$ e $b=1/2,$ quando elevare al quadrato e poi prendere il valore principale della radice quadrata dà $1,$ mentre la potenza con esponente $ab=1$ vale $-1.$