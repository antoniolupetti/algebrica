---
title: Absolute Value
source: https://algebrica.org/absolute-value/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - distance
  - even-function
  - inequalities
  - norm
  - real-line
  - reverse-triangle-inequality
  - sign-function
  - triangle-inequality
---
## Definizione

Per definire il valore assoluto consideriamo la retta reale e fissiamo un'unità di misura per misurare la distanza tra due punti qualsiasi $a$ e $b$. Per misurare questa distanza si ricorre alla formula della distanza euclidea che è data da:

$$  
d(a,b)=\sqrt{(a-b)^2} \tag{1}
$$

Come sappiamo una distanza è sempre non negativa mentre è nulla solo quando i due punti coincidono. Da questa premessa possiamo ricavare il valore assoluto di un numero reale che rappresenta la distanza di un punto $x$ dallo zero. Se nella $(1)$ poniamo $a=x$ e $b=0$ otteniamo:

$$  
|x|=d(x,0)=\sqrt{x^2} \tag{2}
$$

Come sappiamo, la radice quadrata restituisce sempre un valore non negativo, perciò possiamo riscrivere la $(2)$ nella seguente forma:

$$ \tag{3}
|x| =
\begin{cases}
+x & \text{se } x \geq 0 \\[6pt]
-x & \text{se } x < 0
\end{cases}
\quad
\forall \ x \in \mathbb{R}
$$

Per esempio, $|5|=5$ e $|-6|=-(-6)=6.$ Se al posto dell'origine prendiamo un punto qualsiasi di coordinata $a$, possiamo riscrivere la $(2)$ nel seguente modo:

$$  
d(x,a)=\sqrt{(x-a)^2}=|x-a|  \tag{4}
$$

In pratica, in questo caso il valore assoluto della differenza tra il punto $x$ e il punto $a$ generico esprime proprio la distanza tra i due punti


![IMG. 1](../svg/real-numbers-1.svg)


Più in generale la $(4)$ vale la seguente relazione di simmetria in quanto la distanza tra due punti, anche se si scambiassero, rimarrebbe sempre la stessa.

$$
|x-a| = |a-x|
$$

Per esempio, la distanza tra $3$ e $7$ è $|3-7|=4$ corrisponde alla distanza tra $7$ e $3$ che è pari a $|7-3|=4.$

- - -

Fino a questo punto, abbiamo parlato del valore assoluto inteso come numero, ma se facciamo variare la $x$ in $\mathbb{R}$ otteniamo una funzione che associa ad ogni numero reale il suo valore assoluto. Tale funzione è definita come:

$$
y = |x| =
\begin{cases}
+x & \text{if } x \geq 0 \\[6pt]
-x & \text{if } x < 0
\end{cases}
$$


![IMG. 1](../svg/absolute-value-1.svg)

Come si vede dall'immagine, il suo grafico è caratterizzato da due semirette che si incontrano all'origine ed è simmetrico rispetto all'asse $y$, perciò è una funzione pari che soddisfa la seguente relazione:

$$|{-x}| = |x| \quad \text{for all } x \in \mathbb{R}$$

Per una descrizione dettagliata della funzione valore assoluto si rimanda alla relativa voce.

- - -

Nella $(3)$ abbiamo visto che il segno di $x$ influisce nella determinazione del valore assoluto. Questa relazione si può esprimere mediante la funzione segno che consente di esprimere il valore assoluto nel seguente modo:

$$
|x| = x \cdot \mathrm{sgn}(x)\tag{5}
$$

La funzione segno è definita come segue, nei seguenti intervalli:

$$
\mathrm{sgn}(x) =
\begin{cases}
-1 & \text{se } x < 0 \\[6pt]
0 & \text{se } x = 0 \\[6pt]
1 & \text{se } x > 0
\end{cases}
$$

In ciascun intervallo il prodotto tra $x$ e $\mathrm{sgn}(x)$ è sempre non negativo perciò otteniamo i seguenti risultati che coincidono con quelli della definizione del valore assoluto data dalla $(3)$: 

+ Se $x > 0,$ allora $\mathrm{sgn}(x) = 1$ e $x \cdot \mathrm{sgn}(x) = x.$
+ Se $x < 0,$ allora $\mathrm{sgn}(x) = -1$ e $x \cdot \mathrm{sgn}(x) = -x.$
+ Se $x = 0,$ allora $\mathrm{sgn}(x) = 0$ e $x \cdot \mathrm{sgn}(x) = 0.$

## Proprietà

Dopo aver definito il valore assoluto di un numero reale, elenchiamo di seguito una serie di proprietà fondamentali. Iniziamo dalla più immediata che segue la definizione. Come abbiamo detto, un numero reale e il suo opposto hanno la stessa distanza dall'origine, e quindi stesso valore assoluto. Per esempio, $|3|=|-3|=3.$ In generale vale quindi la seguente identità:

$$
|x| = |-x| \quad \forall \ x \in \mathbb{R}
$$

- - -

Poiché $x$ e $-x$ hanno la stessa distanza dall'origine, il minore dei due è non positivo ed è pari a $-|x|,$ mentre il maggiore è pari a $|x|.$ Poiché $x$ coincide con uno di questi due valori, è compreso tra $-|x|$ e $|x|,$ per cui vale la seguente relazione.

$$
-|x| \leq x \leq |x| \quad \forall \ x \in \mathbb{R}
$$

Seguendo il ragionamento possiamo anche concludere che il valore assoluto è il massimo tra $x$ e $-x,$ per cui si ha:

$$
|x| = \max\{x,-x\} \quad \forall \ x \in \mathbb{R}
$$

- - -

Dal punto di vista algebrico, è importante conoscere che il valore assoluto di un prodotto è uguale al prodotto dei valori assoluti. Infatti, applicando ripetutamente questa proprietà, per ogni prodotto finito si ottiene:

$$|x_1 \cdot x_2 \cdots x_n|=|x_1| \cdot |x_2| \cdots |x_n|$$

La proprietà si esprime sinteticamente come:

$$
|x \cdot y| = |x| \cdot |y| \quad \forall \ x, y \in \mathbb{R} \tag{6}
$$

- - -

Consideriamo adesso due numeri reali $x$ e $y$. Tali numeri hanno lo stesso valore assoluto se e solo se sono uguali oppure opposti. Per come abbiamo definito il valore assoluto, ormai sappiamo che $|x|=|y|$ e cioè $x$ e $y$ hanno la stessa distanza dall'origine, il che accade esattamente quando $x=y$ oppure $x=-y.$ In termini formali questa proprietà si scrive come:

$$
|x| = |y| \iff x = \pm y \quad \forall \ x, y \in \mathbb{R}
$$

- - -

Tra due numeri non negativi, il primo è minore o uguale al secondo se e solo se il suo quadrato è minore o uguale al quadrato del secondo. Applichiamo questa proprietà a $|x|$ e $|y|,$ che sono non negativi per qualsiasi coppia di numeri reali $x$ e $y.$ Poiché $|x|^2=x^2$ e $|y|^2=y^2,$ possiamo scrivere:

$$
|x| \leq |y| \iff x^2 \leq y^2 \quad \forall \ x, y \in \mathbb{R}
$$

- - -

Un'altra proprietà utile nei calcoli, è data dal valore assoluto di un quoziente che è uguale al quoziente dei valori assoluti. Consideriamo due numeri $x$ e $y$ con $y \ne 0$ per non far annullare il denominatore e applichiamo la proprietà $(6)$ all'identità $yy^{-1}=1.$ In questo modo otteniamo $|y^{-1}|=|y|^{-1},$ da cui deriva:

$$
\left| \frac{x}{y} \right| = \frac{|x|}{|y|} \quad \forall \ x, y \in \mathbb{R},\ y \ne 0
$$

- - -

Infine consideriamo la radice quadrata di $x^2$ che come sappiamo è sempre non negativa e quindi è uguale a $x$ se $x\geq 0$ mentre a $-x$ se $x<0.$ Perciò possiamo scrivere l'ultima relazione che è molto importante perché si incontra spesso nelle equazioni e in particolare nelle equazioni irrazionali:

$$
\sqrt{x^2} = |x| \quad \forall \ x \in \mathbb{R}
$$

## Disuguaglianza triangolare

Per introdurre la disuguaglianza triangolare, partiamo da un ragionamento molto intuitivo. Se vogliamo andare da un punto $a$ a un punto $b$ sappiamo che il percorso più breve è dato dal segmento che collega i due punti. Passando per un terzo punto, il percorso può allungarsi, ma non può diventare più breve. Se applichiamo lo stesso ragionamento a un triangolo otteniamo che la lunghezza di un lato è sempre minore o al più uguale alla somma delle lunghezze degli altri due. Se consideriamo quindi il percorso da $0$ a $a+b,$ passando per $a$ il primo tratto ha lunghezza $|a|$ e il secondo ha lunghezza $|b|$. Tuttavia la distanza tra il punto iniziale e quello finale è invece $|a+b|$. Quella che abbiamo appena ottenuto è proprio la disuguaglianza triangolare data dalla seguente relazione:

$$
|a + b| \le |a| + |b| \tag{7}
$$

Per rendere il tutto più chiaro, partiamo ad esempio dal punto $0$ e ci spostiamo verso destra fino al punto $5.$ Poi torniamo indietro e arriviamo al punto $2,$ percorrendo 3 ulteriori unità. Il percorso che abbiamo seguito è di $8$ unità totali, ma la distanza tra il punto di partenza $0$ e quello di arrivo $2$ è solo $2,$ il che è coerente con la $(7)$.

- - -

Per dimostrare in modo formale la $(7)$ consideriamo tutti i casi relativi ai possibili segni di $a$ e $b:$

$$
\begin{align}
(1)\quad & a \ge 0, \quad b \ge 0 \\[6pt]
(2)\quad & a \le 0, \quad b \le 0 \\[6pt]
(3)\quad & a \ge 0, \quad b \le 0 \\[6pt]
(4)\quad & a \le 0, \quad b \ge 0
\end{align}
$$

Nel caso $(1),$ la somma soddisfa $a + b \geq 0,$ perciò vale:

$$
|a + b| = a + b = |a| + |b|
$$

Nel caso $(2),$ la somma soddisfa invece $a + b \leq 0,$ e quindi vale la seguente relazione:

$$
|a + b| = -(a + b) = (-a) + (-b) = |a| + |b|
$$

Nel caso $(3),$ poiché $a \ge 0$ e $b \le 0,$ abbiamo $|a| = a$ e $|b| = -b,$ quindi $|a| + |b| = a - b.$ Per dimostrare che $|a + b| \le a - b$ dobbiamo distinguere i seguenti casi:

+ Quando $a + b \ge 0,$ abbiamo $|a + b| = a + b \le a - b,$ poiché $b \le 0.$
+ Quando invece $a + b \le 0,$ otteniamo $|a + b| = -(a + b) = -a - b \le a - b.$ 

Quest'ultima disuguaglianza equivale a $-a \le a,$ e la condizione è soddisfatta perché $a \ge 0.$ Infine, il caso $(4)$ si riconduce al caso $(3)$ scambiando $a$ e $b.$

- - -

Dalla $7$ segue anche la relazione inversa, ovvero per ogni $a,b \in \mathbb{R},$ vale:

$$
\bigl||a| - |b|\bigr| \le |a - b| \tag{8}
$$

In questa relazione, il valore assoluto della differenza tra le distanze di $a$ e $b$ dallo zero è minore o uguale alla distanza tra $a$ e $b.$ Per dimostrarla, applichiamo la disuguaglianza triangolare all'identità $a=(a-b)+b,$ ottenendo:

$$
|a| = |(a - b) + b| \le |a - b| + |b|
$$

In questo modo si ha che $|a| - |b| \le |a - b|.$ Scambiando $a$ e $b$ otteniamo $|b| - |a| \le |a - b|$ e poiché sia $|a| - |b|$ che $|b|-|a|$ sono minori o uguali a $|a - b|,$ concludiamo che vale la $(8)$:

## Ulteriori considerazioni

Il valore assoluto si applica ai numeri reali e come abbiamo più volte ricordato in questa voce ne misura la distanza dallo zero. La norma $\|\cdot\|$ estende questa idea ai vettori, associando a ciascuno una lunghezza non negativa. In termini generali, una norma su uno spazio vettoriale reale $V$ è una funzione del tipo $\|\cdot\|:V \to [0,+\infty)$ che soddisfa le seguenti tre proprietà per ogni $x,y \in V$ e ogni $\lambda \in \mathbb{R}:$

$$
\begin{align}
\quad & \|x\| = 0 \iff x = 0 \\[6pt]
\quad & \|\lambda x\| = |\lambda| \cdot \|x\| \\[6pt]
\quad & \|x + y\| \le \|x\| + \|y\|
\end{align}
$$

Il valore assoluto soddisfa tutte e tre le proprietà: la prima segue dalla definizione della $(3)$, la seconda è la proprietà $(6)$ del prodotto applicata a $\lambda x,$ mentre la terza è la disuguaglianza triangolare illustrata nella $(7)$.

- - -

Infine, vale la pena citare le disequazioni con valore assoluto che esprimono una condizione sulla distanza lungo la retta reale. Il primo caso è dato dalla relazione $|A| < k$ che può essere scritta in modo equivalente come:

$$
-k < A < k
$$
Il secondo caso ha invece la forma $|A| > k$ che si può riscrivere come:

$$
A < -k \quad \text{or} \quad A > k
$$

Per una spiegazione dettagliata si rimanda alla relativa voce.
