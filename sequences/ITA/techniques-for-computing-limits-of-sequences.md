---
title: Techniques for Computing Limits of Sequences
source: https://algebrica.org/techniques-for-computing-limits-of-sequences/
license: CC BY-NC 4.0
tags:
  - asymptotic-equivalence
  - growth-rates
  - indeterminate-forms
  - limit-of-a-sequence
  - logarithms
  - rationalization
  - remarkable-limits
  - sequence
---

## Limiti di successioni non immediati

Una delle maggiori difficoltà nel calcolo dei limiti risiede nella grande varietà di casi che si possono incontrare nella loro trattazione. Nel caso delle successioni, determinarne il limite non è sempre agevole né immediato. Quando, ad esempio, ci troviamo di fronte a successioni che si riducono a una [forma indeterminata](../indeterminate-forms/) del tipo $0/0,$ $+\infty/+\infty,$ $0\cdot\infty$ e $+\infty-\infty.$ L'algebra dei limiti da sola non basta più a determinare la convergenza della successione e, in casi come questi, è necessario ricorrere a strumenti differenti, analizzando, per esempio, la struttura e il comportamento delle relative componenti.

In generale, è importante ricordare che il limite di una successione dipende esclusivamente dalla sua coda. Questo è di per sé abbastanza intuitivo: più una successione tende a comportarsi in un certo modo da un punto in poi, tanto più tende a un dato valore e, in quel caso, convergerà. In caso contrario, divergerà. In termini pratici, supponiamo di avere due successioni, $a_n$ e $b_n,$ tali per cui $a_n=b_n$ per ogni $n\geq n_0.$ È abbastanza intuitivo dedurre che dopo il valore $n_0$ le due successioni hanno un medesimo comportamento e pertanto anche lo stesso limite. Questo modo di ragionare consente di ignorare eventuali condizioni iniziali e di imporne altre a partire da un certo indice $n_i$ in poi, semplificando sensibilmente il procedimento di calcolo.

Esistono diversi approcci per valutare i limiti meno immediati, derivanti dalle caratteristiche dei termini che caratterizzano una data successione, che illustreremo nel dettaglio nei paragrafi successivi.

## Termini dominanti

Uno dei metodi più semplici è quello dei cosiddetti termini dominanti. Quando si ha un limite di una successione caratterizzata dal rapporto di polinomi, si divide l'espressione per la massima potenza che compare nei polinomi al numeratore e al denominatore. Consideriamo il semplice caso del limite della seguente successione:

$$\lim_{n\to+\infty}\frac{4n^3-5n+1}{2n^3+n^2-7}$$

Valutando direttamente il valore della successione per $n$ che tende all'infinito otteniamo la forma indeterminata $\infty / \infty$ che non dice nulla sul suo comportamento. Dividendo invece per il termine di grado massimo otteniamo:

$$\lim_{n\to+\infty}\frac{4-5/n^2+1/n^3}{2+1/n-7/n^3}=2$$

Più in generale, se $P$ e $Q$ hanno gradi $p$ e $q$ e coefficienti di grado massimo $a$ e $b,$ vale l'identità seguente:

$$
\frac{P(n)}{Q(n)}
=n^{p-q}\frac{a+o(1)}{b+o(1)}
$$

Con la [notazione o piccolo](../little-o-notation/) $o(1)$ raggruppiamo sinteticamente tutti i termini che tendono a zero. In questo modo, nella valutazione del rapporto abbiamo tre casistiche:

+ la prima è che esso tende a $0$ per $p<q;$
+ la seconda invece tende a $a/b$ per $p=q;$ 
+ nell'ultimo caso, per $p>q,$ il rapporto diverge in modulo e assume definitivamente il segno di $a/b.$ 

- - -

Lo stesso procedimento, che consiste nel mettere in evidenza la potenza di $n$ con esponente maggiore, si utilizza nelle somme di potenze. Consideriamo, per esempio, la differenza $n^\alpha-3n^\beta$ con $\alpha<\beta.$ Mettendo in evidenza la potenza con esponente maggiore si ottiene:

$$
n^\alpha-3n^\beta
=n^\beta\left(n^{\alpha-\beta}-3\right)
$$

Poiché $n^{\alpha-\beta}$ tende a zero, il fattore tra parentesi tende a $-3$ e il termine dominante è $-3n^\beta.$

- - -

Un altro caso è quello in cui si deve estrarre un quadrato da una radice. Poiché il radicando deve sempre essere maggiore o uguale a zero, per ogni valore di $n$ vale:
$$\sqrt{n^2}=|n|$$ 
Il ricorso al valore assoluto è quindi d'obbligo. Se consideriamo il limite $n\to+\infty,$ gli indici sono tutti positivi, quindi $|n|=n$ e si può scrivere, per esempio, $\sqrt{n^2+3}=n\sqrt{1+3/n^2}.$

## Gerarchie di crescita

Quando $n\to+\infty,$ per ogni scelta di costanti $p,q>0$ e $a>1$ vale la seguente gerarchia di crescita:

$$
(\ln n)^p\ll n^q\ll a^n\ll n!\ll n^n
$$

La generica notazione $u_n\ll v_n$ significa che il rapporto $u_n/v_n\to0,$ che equivale a dire che la successione a sinistra del simbolo $\ll$ cresce più lentamente di quella successiva (ad esempio il rapporto $(\ln n)^p/n^q$ tende a 0 e lo stesso vale per le altre coppie che considerano al numeratore la successione di indice $i$ e al denominatore quella di indice $i+1$).

Per esplicitare i confronti, consideriamo la prima relazione: $(\ln n)^p\ll n^q.$ Ponendo $t=\ln n,$ il rapporto diventa:

$$
\frac{(\ln n)^p}{n^q}
=\frac{t^p}{e^{qt}}
\longrightarrow0
$$

Per i due confronti $n^q\ll a^n\ll n!$ definiamo invece $d_n=n^q/a^n$ e $c_n=a^n/n!.$ I rispettivi rapporti soddisfano le seguenti identità:

$$
\begin{align}
\frac{d_{n+1}}{d_n}&=\frac{(1+1/n)^q}{a}\longrightarrow\frac{1}{a}<1 \\[6pt]
\frac{c_{n+1}}{c_n}&=\frac{a}{n+1}\longrightarrow0
\end{align}
$$

Entrambe le successioni tendono quindi a zero. 

Infine, consideriamo l'ultimo caso con il fattoriale. Possiamo scrivere intanto la seguente identità:
$$n!/n^n=\prod_{k=1}^n(k/n)$$

Almeno $\lfloor n/2\rfloor$ fattori sono minori o uguali a $1/2,$ mentre gli altri sono minori o uguali a $1.$ La relazione si può quindi riscrivere come:

$$
0\leq\frac{n!}{n^n}
\leq\left(\frac{1}{2}\right)^{\lfloor n/2\rfloor}
\longrightarrow0
$$

Quando si confrontano successioni della stessa forma, l'ordine dipende invece dai parametri. Per $0<r<s$ si ha $n^r\ll n^s,$ mentre per $1<a<b$ si ha $a^n\ll b^n.$

Il ricorso alla gerarchia non è quindi solo uno strumento teorico, ma ha anche un'importante applicazione pratica che consente di risolvere successioni non immediatamente risolvibili con l'algebra dei limiti e a prima vista complicate. Ad esempio, consideriamo la seguente successione:

$$
a_n=\frac{2^n+n^5}{3^n+\ln n}
$$

Questa successione tende a zero. Infatti, nel denominatore $3^n$ domina $\ln n,$ quindi dividiamo numeratore e denominatore per $3^n:$

$$
a_n=\frac{(2/3)^n+n^5/3^n}{1+(\ln n)/3^n}
$$

La gerarchia fornisce $n^5/3^n\to0$ e $(\ln n)/3^n\to0.$ Inoltre $(2/3)^n\to0$ perché $0<2/3<1.$ Il numeratore tende quindi a $0,$ mentre il denominatore tende a $1,$ da cui $a_n\to0.$

## Comportamento asintotico e limiti notevoli

Un modo per valutare due successioni è quello del ricorso al loro comportamento asintotico. Una successione $a_n$ si dice asintoticamente equivalente a $b_n$ se vale l'uguaglianza seguente:

$$
\lim_{n\to+\infty}\frac{a_n}{b_n}=1 \tag{1}
$$

L'equivalenza asintotica si scrive anche come $a_n\sim b_n$ e richiede $b_n\neq0.$ Dalla $(1)$ possiamo tradurre i [limiti notevoli](../remarkable-limits/) in equivalenze tra successioni. Ad esempio, sia $(x_n)$ una successione tale che $x_n\to0$ e $x_n\neq0$. Consideriamo il limite notevole:

$$\lim_{x\to0}\frac{\sin x}{x}=1$$

Sempre per la $(1)$ deve valere $\sin x_n\sim x_n.$ Se applichiamo lo stesso ragionamento ai limiti notevoli fondamentali, otteniamo le seguenti equivalenze:

[class="table-1"]

| Espressione | Equivalente asintotico |
| ----------- | ----------------------- |
| $\sin x_n$ | $x_n$                   |
| $\ln(1+x_n)$ | $x_n$                 |
| $e^{x_n}-1$ | $x_n$                   |
| $1-\cos x_n$ | $x_n^2/2$             |

[/class]

Queste equivalenze sono molto utili perché si possono sostituire nei prodotti e nei quozienti per semplificare la valutazione del comportamento di una successione, purché i denominatori siano definitivamente non nulli. Consideriamo ad esempio la seguente successione. Facendo le opportune sostituzioni si ottiene il seguente limite:

$$
\frac{(e^{2/n}-1)\ln(1+3/n)}{1-\cos(1/n)}
\sim
\frac{(2/n)(3/n)}{1/(2n^2)}=12
$$

Come dicevo, la sostituzione si può fare nei prodotti e nei quozienti, ma non fra i termini di una differenza, perché potrebbe cancellare la parte principale che determina il comportamento della successione, alterando il risultato del limite.

Il ricorso a queste forme equivalenti permette anche di risolvere prodotti indeterminati. Ad esempio consideriamo la seguente successione:

$$
a_n=n^\alpha\ln\left(1+\frac{1}{n}\right),\qquad \alpha>0
$$

Il fattore $n^\alpha$ tende a $+\infty,$ mentre $\ln(1+1/n)$ tende a $0,$ quindi una sostituzione diretta produrrebbe la forma indeterminata $\infty\cdot0.$ Per applicare l'equivalenza $\ln(1+x)\sim x$ bisogna confrontare il logaritmo con $1/n:$

$$
a_n
=n^{\alpha-1}\frac{\ln(1+1/n)}{1/n}
\sim n^{\alpha-1}
$$

Il quoziente con il logaritmo tende a $1,$ perciò il comportamento di $a_n$ coincide con quello di $n^{\alpha-1}.$ Ne seguono tre casi: $a_n\to0$ per $0<\alpha<1,$ $a_n\to1$ per $\alpha=1$ e $a_n\to+\infty$ per $\alpha>1.$

## Razionalizzazione

Consideriamo adesso il caso di due termini di una differenza che tendono a $+\infty$ e che per sostituzione diretta producono la forma indeterminata $+\infty-\infty.$ C'è un caso, non del tutto raro, in cui la differenza può coinvolgere delle radici quadrate e per il quale è utile procedere moltiplicando e dividendo per la loro somma (anche detta espressione coniugata). Consideriamo ad esempio $A_n,B_n\geq0$ con $A_n+B_n>0.$ In questo caso vale:

$$
\sqrt{A_n}-\sqrt{B_n}
=\frac{A_n-B_n}{\sqrt{A_n}+\sqrt{B_n}} \tag{2}
$$

La $(2)$ elimina la differenza tra le radici e la sostituisce con la differenza tra i radicandi. Consideriamo l'esempio seguente:

$$
\begin{align}
n\left(\sqrt{n^2+3}-n\right)
&=n\frac{(n^2+3)-n^2}{\sqrt{n^2+3}+n} \\[6pt]
&=\frac{3}{\sqrt{1+3/n^2}+1}
\longrightarrow\frac{3}{2}
\end{align}
$$

La sostituzione vale solo per radici quadrate. Quando si incontrano radici di ordine superiore si procede prima per [razionalizzare](../radicals/) e si usa la fattorizzazione della differenza di potenze.

## Potenze variabili

Consideriamo adesso una successione a potenza variabile, ovvero una successione con i termini della forma $a_n=b_n^{c_n},$ nei quali la base $b_n$ e l'esponente $c_n$ possono dipendere entrambi da $n.$ Anche in questo caso, una sostituzione diretta nel calcolo del limite può produrre forme indeterminate del tipo $1^\infty,$ $0^0$ e $(+\infty)^0$ che non dicono nulla sul comportamento della successione. Quando $b_n>0$ definitivamente, possiamo ricorrere al $\ln b_n$ che trasforma la potenza in un prodotto mediante l'identità:

$$
a_n=e^{c_n\ln b_n} \tag{3}
$$

Il limite dipende quindi solo da $c_n\ln b_n.$ Se questo prodotto tende a un valore $\ell\in\mathbb{R},$ allora $a_n\to e^\ell.$ Se invece tende a $-\infty$ oppure a $+\infty,$ la potenza tende a $0$ oppure a $+\infty.$ Richiamando i limiti notevoli e il loro comportamento asintotico, se ci troviamo nel caso in cui $u_n\to0,$ $u_n\neq0$ definitivamente e $c_nu_n\to \ell,$ il limite notevole $\ln(1+u_n)\sim u_n$ produce:

$$
(1+u_n)^{c_n}\to e^\ell
$$

Per chiarire con un esempio, consideriamo la successione seguente:

$$
a_n=\left(\frac{n+2}{n-1}\right)^n
=\left(1+\frac{3}{n-1}\right)^n
$$

Il suo logaritmo soddisfa la seguente relazione:

$$
\ln a_n
=\frac{3n}{n-1}
\frac{\ln(1+3/(n-1))}{3/(n-1)}
\longrightarrow3
$$

Da questo ne segue che $a_n\to e^3.$

## Sulle successioni che oscillano

Consideriamo adesso il caso di successioni che oscillano senza superare un certo valore assoluto (cosiddette perturbazioni), come $\sin n$ o $\cos n$ che possono oscillare senza superare $\vert 1 \vert$. Se si moltiplica per una successione infinitesima, il loro contributo tende a zero. In termini formali, se $(u_n)$ è limitata e $v_n\to0,$ allora $u_nv_n\to0.$ Ad esempio:

$$
\left|\frac{\sin(n^2)}{\sqrt n}\right|
\leq\frac{1}{\sqrt n}\to0
$$

Più in generale, se $b_n\to \ell,$ $r_n\to0$ e $|a_n-b_n|\leq r_n$ definitivamente, il [teorema del confronto](../squeeze-theorem/) dà $a_n\to \ell.$ Consideriamo ad esempio la successione:

$$
a_n=\frac{2n+\sin n}{n+\cos n}
$$

Per $n\geq2$ vale la stima:

$$
|a_n-2|
=\left|\frac{\sin n-2\cos n}{n+\cos n}\right|
\leq\frac{3}{n-1}\to0
$$

Pertanto $a_n\to2,$ nonostante le perturbazioni trigonometriche non convergano.
