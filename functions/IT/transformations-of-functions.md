---
title: Trasformazioni Delle Funzioni
source: https://algebrica.org/transformations-of-functions/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - function-transformations
  - functions
  - graphs
  - reflections
  - scaling
  - translations
---

## Traslazioni verticali

In questo capitolo saranno trattate le trasformazioni delle funzioni di variabile reale, ovvero una serie di operazioni che intervengono sul valore della funzione o sul suo argomento, in grado di trasformare il grafico della funzione di partenza attraverso, ad esempio, una traslazione o una rotazione dello stesso. Se consideriamo, ad esempio, una generica funzione $f(x),$ una sua possibile trasformazione è data dall'espressione $f(x)+2$ il cui effetto è quello di traslare verticalmente il grafico di $f(x).$ Un'altra trasformazione è data dall'espressione $f(x+2)$ che consente invece di ottenere una traslazione orizzontale della funzione di partenza. Per mostrare come queste trasformazioni funzionano in pratica, supponiamo di avere la seguente funzione polinomiale di secondo grado, il cui grafico è una parabola con vertice nel punto $(1,1),$ un generico punto $P(u,v)$ appartenente al grafico di $f.$

$$
f(x)=(x-1)^2+1 \tag{1}
$$

Come prima trasformazione, consideriamo quella di una funzione $g$ ottenuta aggiungendo una costante reale $k$ ai valori di $f$:

$$
g(x)=f(x)+k \tag{2}
$$

Nel punto di ascissa $u$ abbiamo che $g(u)=f(u)+k=v+k,$ ovvero: 

$$
P(u,v)\longmapsto P^\prime(u,v+k)
$$

Se $k>0,$ il grafico si sposta verso l'alto mentre se $k<0,$ si sposta verso il basso di $|k|$. In questo modo otteniamo una traslazione verticale del grafico della funzione originaria $f,$ applicata a tutti i suoi punti. Per fare un esempio concreto, consideriamo la $(1)$ e aggiungiamo una costante $k=2,$ così da ottenere:

$$
g(x)=f(x)+2=(x-1)^2+3
$$

Il grafico di $g$ rappresenta la stessa parabola di $f$ ma traslata di $2$ verso l'alto:

![IMG. 1](../svg/transformations-of-functions-1.svg)

Se invece dalla $(1)$ sottraiamo $2,$ otteniamo:

$$
g(x)=f(x)-2=(x-1)^2-1
$$

In questo caso il vertice della parabola della funzione $g$ è $(1,-1)$ e il punto $(2,2)$ diventa $(2,0).$ Il grafico quindi si è spostato di $2$ verso il basso:

![IMG. 2](../svg/transformations-of-functions-2.svg)

Una traslazione verticale lascia quindi invariato il dominio della funzione ottenuta dalla generica trasformazione data dalla $(2)$, in quanto non modifica gli argomenti ai quali viene applicata $f.$

## Dilatazioni e compressioni verticali

Vediamo ora cosa accade quando si moltiplica una funzione $f$ per un numero positivo $a \gt 0$ per ottenere una nuova funzione $g,$ in modo che valga la seguente identità:

$$
g(x)=af(x) \tag{3}
$$

Poiché $g(u)=af(u)=av,$ ogni punto della $f$ si trasforma secondo la regola:

$$
P(u,v)\longmapsto P^\prime(u,av)
$$

In questo caso abbiamo due configurazioni possibili. Quando $a>1$ la funzione $g$ presenta una dilatazione verticale mentre se $0<a<1$ abbiamo una compressione verticale. Ad esempio, con $a=2$ la $(1)$ diventa:

$$
g(x)=2f(x)=2(x-1)^2+2
$$

Il vertice $(1,1)$ passa a $(1,2)$ e il punto $(2,2)$ passa a $(2,4).$ Le ordinate raddoppiano. Il vertice si sposta di una unità verso l'alto, mentre il secondo punto si sposta di due unità, quindi il cambiamento è diverso da una traslazione.

![IMG. 3](../svg/transformations-of-functions-3.svg)

Se poniamo invece $a=1/2,$ ci troviamo nel secondo caso e dalla $(1)$ otteniamo invece:

$$
g(x)=\frac{1}{2}f(x)=\frac{1}{2}(x-1)^2+\frac{1}{2}
$$

Il vertice diventa $(1,1/2)$ e il punto $(2,2)$ diventa $(2,1).$ Le distanze dall'asse delle ascisse si dimezzano, e il grafico risulta compresso in verticale.

![IMG. 4](../svg/transformations-of-functions-4.svg)

Come nel caso della traslazione verticale, anche la dilatazione e la compressione verticale lascia invariato il dominio della funzione ottenuta dalla generica trasformazione data dalla $(3).$


## Riflessione rispetto all'asse x

Vediamo adesso cosa accade al grafico quando si cambia il segno della funzione originaria per ottenere una nuova funzione $g$ data dalla seguente identità:

$$
g(x)=-f(x) \tag{4}
$$

La $(4)$ fa sì che ogni punto del grafico mantiene la propria ascissa mentre cambia segno all'ordinata. Questa trasformazione genera quindi una riflessione rispetto all'asse $x$ in cui per tutti i punti vale la seguente relazione:

$$
P(u,v)\longmapsto P^\prime(u,-v)
$$

Tornando al nostro esempio della $(1)$ la funzione $f$ trasformata attraverso la $(4)$ diventa:

$$
g(x)=-(x-1)^2-1
$$

Il vertice si sposta nel punto $(1,-1)$ e il punto $(2,2)$ diventa $(2,-2)$ e la concavità della parabola è rivolta verso il basso.

![IMG. 5](../svg/transformations-of-functions-5.svg)


## Traslazioni orizzontali

Consideriamo ora una modifica all'argomento della funzione $f$ introducendo un addendo $h \in \mathbb{R}$ per ottenere una funzione trasformata $g$ data da:

$$
g(x)=f(x-h) \tag{5}
$$

Ciascun punto del grafico della funzione trasformata diventa:

$$
P (u,v)\longmapsto P^{\prime}(u+h,v)
$$

Se $h>0,$ il grafico trasla verso destra di $h$ altrimenti se è minore di zero verso sinistra. Ad esempio, se volessimo traslare la parabola di tre unità verso destra scriviamo la $(5)$ nel seguente modo:

$$
g(x)=f(x-3)=((x-3)-1)^2+1=(x-4)^2+1
$$

Il vertice passa da $(1,1)$ a $(4,1)$ e il punto $(2,2)$ diventa $(5,2).$ In pratica, tutti i valori delle ascisse del grafico aumentano di tre unità, mentre le ordinate rimangono invariate.

![IMG. 6](../svg/transformations-of-functions-6.svg)

Se vogliamo spostare invece la parabola verso sinistra dobbiamo invece usare la seguente relazione:

$$
g(x)=f(x+3)=((x+3)-1)^2+1=(x+2)^2+1
$$

In questo caso il vertice diventa $(-2,1)$ e il punto $(2,2)$ diventa $(-1,2).$ È utile evidenziare che la traslazione orizzontale trasla il dominio della funzione trasformata, ovvero, se abbiamo una $f$ definita su $[1,5],$ la funzione $f(x-3)$ è definita quando $x-3\in[1,5],$ cioè su $[4,8].$ 

## Dilatazioni e compressioni orizzontali

Vediamo ora cosa accade quando moltiplichiamo l'argomento della $(1)$ per un numero positivo $b \gt 0.$ La funzione trasformata $g$ è data dalla seguente identità:

$$
g(x)=f(bx) \tag{6}
$$

La relazione tra i punti della $(1)$ e della trasformata $(6)$ diventa:

$$
P(u,v)\longmapsto P^{\prime}\left(\frac{u}{b},v\right) \tag{7}
$$

Il fattore che moltiplica le distanze dall'asse delle ordinate è $1/b.$ Se $b>1,$ queste distanze diminuiscono e abbiamo una compressione orizzontale mentre se $0<b<1,$ le distanze aumentano e abbiamo una dilatazione orizzontale. Ad esempio se sostituiamo $2x$ all'argomento della $(1)$ otteniamo:

$$
g(x)=f(2x)=(2x-1)^2+1
$$

Il vertice $(1,1)$ si sposta nel punto $(1/2,1)$ e il punto $(2,2)$ diventa $(1,2).$ Le ascisse quindi si dimezzano ritrovando il rapporto $u/b$ della $(7)$ e il grafico viene compresso verso l'asse delle ordinate:


![IMG. 7](../svg/transformations-of-functions-7.svg)

Se all'argomento della $(1)$ sostituiamo invece il valore $x/2,$ abbiamo:

$$
g(x)=f\left(\frac{x}{2}\right)=\left(\frac{x}{2}-1\right)^2+1
$$

In questo caso il vertice della parabola diventa $(2,1)$ e il punto $(2,2)$ diventa $(4,2).$ Le ascisse quindi raddoppiano e il grafico subisce una dilatazione orizzontale come rappresentato nella seguente immagine.

![IMG. 8](../svg/transformations-of-functions-8.svg)

Queste trasformazioni conservano l'immagine della funzione mentre il dominio diventa l'insieme degli $x$ per i quali $bx$ appartiene al dominio iniziale. Ad esempio se il dominio di $f$ è $[2,6],$ quello di $f(2x)$ sarà $[1,3],$ mentre quello di $f(x/2)$ sarà pari a $[4,12].$

## Riflessione rispetto all'asse y

Consideriamo il caso in cui si voglia sostituire $-x$ all'argomento della $(1)$. La funzione trasformata $g$ sarà data dalla seguente relazione:

$$
g(x)=f(-x) \tag{8}
$$

Ciascun punto del grafico della $f$ verrà quindi trasformato nel seguente modo:

$$
P(u,v)\longmapsto P^{\prime}(-u,v)
$$

Come si vede, i punti si riflettono rispetto all'asse delle ordinate, quindi se consideriamo la $(1)$ e ricaviamo la $g$ dalla $(8)$ otteniamo:

$$
g(x)=f(-x)=(-x-1)^2+1=(x+1)^2+1
$$

Il vertice di $g$ passa da $(1,1)$ a $(-1,1)$ e il punto $(2,2)$ diventa $(-2,2).$ In generale il dominio della $g$ si riflette rispetto allo zero, perciò un generico dominio $[r,s]$ diventa $[-s,-r].$

![IMG. 9](../svg/transformations-of-functions-9.svg)

Se $f$ è una funzione pari, la riflessione lascia il grafico di $g$ invariato, perché $f(-x)=f(x).$ Per questo, se abbiamo una parabola data da $y=x^2$ non avremmo alcun cambiamento nel suo grafico trasformato.

## Simmetria rispetto all'origine

Se applichiamo le riflessioni precedenti, otteniamo che ogni punto del grafico della funzione trasformata $g$ cambia segno a tutte e due le coordinate, ottenendo:

$$
P(u,v)\longmapsto P^{\prime}(-u,-v)
$$

In questo modo si ottiene una simmetria centrale rispetto all'origine, equivalente a una rotazione di mezzo giro della funzione $g$ sul piano rispetto alla $f$. La funzione corrispondente è pertanto:

$$
g(x)=-f(-x) \tag{9}
$$

Per la parabola della $(1)$ la formula $(9)$ diventa quindi $g(x)=-(x+1)^2-1.$ In questo caso, il vertice passa a $(-1,-1)$ e il punto $(2,2)$ passa a $(-2,-2).$ Inoltre, il segmento che unisce ogni punto della $f$ e della $g$ ha il proprio punto medio esattamente nell'origine.

![IMG. 10](../svg/transformations-of-functions-10.svg)

È interessante notare come l'ordine con cui vengono applicate le due riflessioni non conta, perché ciascuna modifica una coordinata diversa e quindi cambiando l'ordine il risultato finale sul grafico della $g$ trasformata è sempre lo stesso. Se la funzione $f$ è una funzione dispari, applicando questo genere di trasformazione, il grafico rimane invariato, dato che $-f(-x)=f(x).$

## Trasformazioni composte

Tutte le trasformazioni che abbiamo visto fino ad ora si possono raccogliere in un'unica formula, con parametri $a\neq0,$ $b\neq0$ e $k$:

$$
g(x)=af\bigl(b(x-h)\bigr)+k \tag{10}
$$

Per trovare il punto corrispondente a $(u,v),$ con $v=f(u),$ imponiamo che l'argomento di $f$ sia $u$ e otteniamo:

$$
b(x-h)=u\qquad\Longrightarrow\qquad x=h+\frac{u}{b}
$$

Otteniamo quindi la regola completa di relazione tra i punti di $f$ e $g$:

$$
P(u,v)\longmapsto P^{\prime}\left(h+\frac{u}{b},av+k\right) \tag{11}
$$

Possiamo interpretare la $(11)$ come una sequenza di operazioni sui punti in questo ordine:

+ Dividiamo le ascisse per $b.$ Il fattore di scala orizzontale è $1/|b|$ e se $b<0,$ si aggiunge la riflessione rispetto all'asse delle ordinate.
+ Aggiungiamo $h$ alle ascisse ottenute, traslando il grafico orizzontalmente.
+ Moltiplichiamo le ordinate per $a.$ Il fattore di scala verticale è $|a|$ e se $a<0,$ si aggiunge la riflessione rispetto all'asse delle ascisse.
+ Infine aggiungiamo $k$ alle ordinate ottenute, traslando il grafico verticalmente.

Possiamo riscrivere l'argomento della $(10)$ nella forma $bx+c.$ Infatti, sviluppando $b(x-h)=bx-bh,$ otteniamo $c=-bh,$ cioè $h=-c/b.$ Sostituendo questo valore nella nuova ascissa della $(11),$ abbiamo:

$$
h+\frac{u}{b}=-\frac{c}{b}+\frac{u}{b}=\frac{u-c}{b}
$$

Quindi, la $(11)$, per la funzione $(10)$ si scrive come:

$$
P(u,v)\longmapsto P^{\prime}\left(\frac{u-c}{b},av+k\right) \tag{12}
$$

Le formule $(11)$ e $(12)$ sono dunque equivalenti. Per descrivere come cambiano il dominio e l'immagine della funzione trasformata, torniamo alla forma $(10)$ e indichiamo con $D$ il dominio di $f,$ cioè l'insieme degli argomenti per cui è definita, e con $I=f(D)$ la sua immagine, cioè l'insieme dei valori che assume. La funzione $g$ è definita quando l'argomento $b(x-h)$ appartiene a $D.$ Se chiamiamo $u$ un elemento di $D,$ risolvendo $b(x-h)=u$ otteniamo $x=h+u/b.$ Il nuovo dominio raccoglie quindi tutte le ascisse ottenute in questo modo:

$$
D_g=\left\{\ h+\frac{u}{b}\ \middle|\ u\in D\ \right\}
$$

Per ottenere come cambia l'immagine della funzione trasformata $g$, consideriamo invece i valori della funzione. Moltiplichiamo ogni valore $v$ assunto da $f$ per $a$ e aggiungiamo $k,$ ottenendo $av+k.$ L'insieme di tutti questi risultati è l'immagine di $g,$ indicata con $g(D_g).$

$$
g(D_g)=\{\ av+k\mid v\in I\ \}
$$

Consideriamo, ad esempio, la funzione $f(x)=\sqrt{x},$ che sappiamo essere definita per $x\geq0,$ e costruiamo la sua trasformata in questo modo:

$$
g(x)=3-2\sqrt{4-2x} \tag{13}
$$

Per prima cosa ricaviamo i parametri, riscrivendo la $(13)$ come:

$$
g(x)=-2f\bigl(-2(x-2)\bigr)+3
$$

I parametri sono quindi $a=-2,$ $b=-2,$ $h=2$ e $k=3$ e la corrispondenza tra i punti, come mostrato dalla $(11)$ diventa:

$$
P(u,v)\longmapsto P^{\prime}\left(2-\frac{u}{2},3-2v\right)
$$

Scegliamo adesso alcuni punti sul grafico di $f$ e otteniamo le seguenti trasformazioni:

| Punto sul grafico di $f$ | Nuova ascissa | Nuova ordinata | Punto sul grafico di $g$ |
| ------------------------ | ------------- | -------------- | ------------------------ |
| $(0,0)$                  | $2$           | $3$            | $(2,3)$                  |
| $(1,1)$                  | $3/2$         | $1$            | $(3/2,1)$                |
| $(4,2)$                  | $0$           | $-1$           | $(0,-1)$                 |

Il punto iniziale della radice si sposta da $(0,0)$ a $(2,3),$ e il ramo trasformato si estende verso sinistra e verso il basso. La figura confronta direttamente la radice iniziale e la funzione $g$ ottenuta:

![IMG. 11](../svg/transformations-of-functions-11.svg)

Verifichiamo adesso il dominio e l'immagine di $g$. Per il dominio abbiamo che l'argomento della $g$ deve essere maggiore o uguale di zero:

$$
4-2x\geq0\qquad\Longleftrightarrow\qquad x\leq2
$$

Il dominio è dunque $(-\infty,2]$. Per l'immagine di $g$ osserviamo che $\sqrt{4-2x}$ assume tutti i valori non negativi: se li moltiplichiamo per $-2$ e aggiungiamo $3,$ che ricordiamo sono i parametri di trasformazione della $(13),$ possiamo scrivere:

$$
\begin{align}
D_g &= (-\infty,2] \\[6pt]
g(D_g) &= (-\infty,3]
\end{align}
$$

## Valore assoluto della funzione

Oltre alle trasformazioni già citate, un'altra trasformazione frequente si ottiene applicando il valore assoluto alla funzione $f$:

$$
g(x)=|f(x)| \tag{14}
$$

Come sappiamo, la funzione valore assoluto, si esprime nel seguente modo:

$$
|f(x)|=
\begin{cases}
f(x) & \text{se }f(x)\geq0 \\[6pt]
-f(x) & \text{se }f(x)<0
\end{cases}
$$

Quando applichiamo il valore assoluto, quello che succede al grafico è che i punti che si trovano sopra l'asse delle $x$ rimangono tali, mentre quelli che si trovano sotto vengono riflessi verso l'alto in modo che l'immagine contenga esclusivamente valori non negativi. Consideriamo, ad esempio la funzione $f(x)=x^2-2$ che è negativa per $-\sqrt{2}<x<\sqrt{2}$ e non negativa all'esterno di questo intervallo. Il punto $(0,-2)$ della $f$ trasformata diventa $(0,2),$ mentre i punti con ordinata positiva rimangono intatti. Come si può vedere dal grafico sotto, il tratto centrale della parabola si riflette verso l'alto:


![IMG. 12](../svg/transformations-of-functions-12.svg)

Prestate attenzione al fatto che questa trasformazione non è quindi una riflessione completa dell'intero grafico ma solo dei punti con valore negativo delle ordinate.

- - - 

Quando il valore assoluto si applica all'argomento, le cose cambiano e la funzione $g$ è espressa dalla seguente identità:

$$
g(x)=f(|x|)
$$

Per $x\geq0$ abbiamo $|x|=x,$ quindi usiamo il valore $f(x).$ Per $x<0$ abbiamo $|x|=-x,$ quindi usiamo $f(-x).$ In pratica abbiamo:

$$
f(|x|)=
\begin{cases}
f(x) & \text{se }x\geq0 \\[6pt]
f(-x) & \text{se }x<0
\end{cases}
$$

Vediamo come si trasforma il grafico di $g$ con un esempio. Trasformiamo sempre la $(1),$ applicando il valore assoluto all'argomento, ottenendo:

$$
g(x)=(|x|-1)^2+1
$$

La metà sinistra della parabola iniziale viene sostituita dalla copia speculare della metà destra e quindi otteniamo un grafico come quello sotto riportato:

![IMG. 13](../svg/transformations-of-functions-13.svg)


Per trovare il dominio di $g(x)=f(|x|),$ dobbiamo controllare che $f$ sia definita in $|x|.$ Supponiamo, per esempio, che $f$ abbia dominio $[1,4].$ Possiamo calcolare $g(x)$ soltanto quando $1\leq|x|\leq4,$ perciò il dominio di $g$ è:

$$
D_g=[-4,-1]\cup[1,4]
$$

Per l'immagine di $g$ osserviamo che $|x|$ è sempre non negativo, quindi $g$ ha soltanto i valori che $f$ assume per argomenti maggiori o uguali a zero. Per esempio, la funzione $f(x)=x,$ definita su $\mathbb{R},$ assume tutti i valori reali. Dopo la trasformazione otteniamo $g(x)=|x|,$ che assume soltanto valori non negativi. In questo caso il dominio resta $\mathbb{R},$ mentre l'immagine passa da $\mathbb{R}$ a $[0,+\infty).$
