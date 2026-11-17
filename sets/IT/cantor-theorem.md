---
title: Cantor's Theorem
source: https://algebrica.org/cantor-theorem/
license: CC BY-NC 4.0
tags:
  - aleph-numbers
  - cantor-bernstein-theorem
  - cantors-theorem
  - cardinality
  - continuum-hypothesis
  - diagonal-argument
  - power-set
  - uncountable-sets
---
## Enunciato

Per enunciare il teorema di Cantor occorre introdurre l'insieme delle parti che per un generico insieme $A$ è dato dall'insieme di tutti i suoi sottoinsiemi ed è indicato come di seguito:

$$
\mathcal{P}(A)=\{\ B\mid B\subseteq A\ \}
\tag{1}
$$

Nella $(1)$ sono compresi sia l'insieme vuoto sia $A$ stesso. Per esempio, se $A=\{0,1\},$ abbiamo:

$$
\mathcal{P}(A)=\{\ \varnothing,\{0\},\{1\},\{0,1\}\ \}
\tag{2}
$$

Tutti gli elementi di $\mathcal{P}(A)$ sono quindi insiemi e il teorema di Cantor, in termini molto semplici, confronta la cardinalità di $A$ con quella di $\mathcal{P}(A).$ Prima di procedere ricordiamo anche che due insiemi sono equipotenti se esiste una biiezione fra loro che indichiamo come $A\sim B$ e che nessun insieme è equipotente al proprio insieme delle parti. Infatti per ogni insieme $A$ l'applicazione $x\mapsto\{x\}$ è un'iniezione da $A$ in $\mathcal{P}(A),$ quindi $|A|\leq|\mathcal{P}(A)|.$ 

Il teorema di Cantor afferma che l'insieme delle parti ha cardinalità strettamente maggiore di quella di $A,$ cioè vale la seguente relazione:

$$|A|\lt|\mathcal{P}(A)| \tag{3}$$ 

Infatti, nessuna applicazione $f\colon A\to\mathcal{P}(A)$ è suriettiva e, di conseguenza, non esiste una biiezione fra i due insiemi. Per dimostrarlo prendiamo un'applicazione generica e costruiamo un sottoinsieme di $A$ che non è immagine di alcun elemento. Poiché ogni $f(x)$ è un sottoinsieme di $A,$ possiamo considerare gli elementi $x$ che non appartengono al sottoinsieme $f(x)$ loro assegnato:

$$
D=\{\ x\in A\mid x\notin f(x)\ \}
\tag{4}
$$

L'insieme $D$ appartiene a $\mathcal{P}(A).$ Se fosse $D=f(z)$ per qualche $z\in A,$ avremmo due casi. Se $z\in D,$ per la $(4)$ avremmo $z\notin f(z),$ cioè $z\notin D$ mentre se $z\notin D,$ avremmo $z\notin f(z)$ e quindi, per la $(4),$ $z\in D$ e in entrambi i casi otteniamo una contraddizione. Dunque $D$ non è immagine di alcun elemento di $A,$ perciò $f$ non è suriettiva e, poiché è arbitraria, non esiste alcuna biiezione fra $A$ e $\mathcal{P}(A).$

Per $A=\mathbb{N},$ il teorema mostra che l'insieme delle parti dei naturali non è numerabile. Indicando con $2^{|A|}$ la cardinalità di $\mathcal{P}(A)$ e ricordando che $|\mathbb{N}|=\aleph_0,$ otteniamo:

$$
|\mathcal{P}(\mathbb{N})|=2^{\aleph_0}\gt\aleph_0
\tag{5}
$$

La $(5)$ mostra che esiste una cardinalità infinita maggiore di quella dei naturali. Applicando nuovamente il teorema a ogni insieme delle parti ottenuto, si trovano cardinalità sempre maggiori, quindi non esiste un cardinale infinito massimo.

## Teorema di Cantor-Bernstein

Un altro risultato sul confronto fra cardinalità è il teorema di Cantor-Bernstein, che, dati due insiemi $A$ e $B,$ afferma quanto segue:

$$
|A|\leq|B|\quad\text{e}\quad|B|\leq|A|\quad\Longrightarrow\quad A\sim B
\tag{6}
$$

Per dimostrare la $(6),$ consideriamo due iniezioni $f\colon A\to B$ e $g\colon B\to A.$ Partiamo dagli elementi di $A$ esterni all'immagine di $g$ e raccogliamo quelli ottenuti iterando $g\circ f$:

$$
\begin{align}
A_0 &= A\setminus g(B) \notag \\[6pt]
C &= \bigcup_{n\geq0}(g\circ f)^n(A_0) \tag{7}
\end{align}
$$

Poiché nella $(7)$ il termine con $n=0$ è $A_0,$ ogni elemento esterno a $C$ appartiene a $g(B)$ e possiamo definire:

$$
h(a)=
\begin{cases}
f(a) & \text{se } a\in C \\[6pt]
g^{-1}(a) & \text{se } a\notin C
\end{cases}
\tag{8}
$$

La funzione $h$ è iniettiva perché i due rami della $(8)$ sono iniettivi e hanno immagini disgiunte, dato che $g(f(C))\subseteq C.$ Ogni $b\in B$ è raggiunto, perché se $g(b)\notin C$ abbiamo $h(g(b))=b,$ mentre se $g(b)\in C,$ essendo $g(b)\notin A_0,$ esiste $a\in C$ con $g(b)=g(f(a)),$ da cui $b=f(a)=h(a).$ Dunque $h$ è una biiezione.

Per esempio, l'inclusione da $(0,1)$ in $(0,1]$ e l'applicazione $x\mapsto x/2$ nella direzione opposta sono iniettive, quindi $(0,1)\sim(0,1].$ Poiché $x\mapsto\tan(\pi x-\pi/2)$ è una biiezione da $(0,1)$ a $\mathbb{R},$ entrambi gli intervalli hanno la cardinalità dei reali.

Questa cardinalità è detta cardinalità del continuo e si indica con $\mathfrak{c}.$ Richiamiamo inoltre, senza dimostrarla, l'equipotenza fra $\mathcal{P}(\mathbb{N})$ e $\mathbb{R},$ da cui:

$$
\mathcal{P}(\mathbb{N})\sim\mathbb{R},\qquad \mathfrak{c}=2^{\aleph_0}
\tag{9}
$$

Per la $(9),$ la $(3)$ applicata ad $A=\mathbb{N}$ diventa $\aleph_0\lt\mathfrak{c},$ confermando che i numeri reali non sono numerabili.

- - -

Un'altra applicazione del teorema di Cantor-Bernstein mostra che il quadrato $(0,1)\times(0,1)$ ha la stessa cardinalità dell'intervallo $(0,1).$ Per mostrarlo, costruiamo un'iniezione dal quadrato nell'intervallo alternando le cifre decimali delle due coordinate, dopo aver scelto per ciascuna lo sviluppo che non termina con soli zeri:

$$
(0.a_1a_2a_3\ldots,\ 0.b_1b_2b_3\ldots)\longmapsto 0.a_1b_1a_2b_2a_3b_3\ldots
\tag{10}
$$

La $(10)$ è iniettiva perché le cifre nelle posizioni dispari danno la prima coordinata e quelle pari la seconda . Quando $x\mapsto(x,1/2)$ abbiamo invece una relazione iniettiva dall'intervallo nel quadrato e quindi per la $(6)$ abbiamo:

$$
(0,1)\times(0,1)\sim(0,1),\qquad \mathbb{R}^2\sim\mathbb{R}
\tag{11}
$$

La seconda equipotenza nella $(11)$ segue da $(0,1)\sim\mathbb{R},$ applicando una biiezione a ciascuna coordinata. A livello geometrico significa che la retta e il piano hanno dunque la stessa cardinalità pur avendo dimensioni diverse, perché una biiezione mette in corrispondenza i punti senza doverne conservare le relazioni topologiche.
