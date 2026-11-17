---
title: Cardinality and Countable Sets
source: https://algebrica.org/cardinality-and-countable-sets/
license: CC BY-NC 4.0
tags:
  - cardinality
  - countable-sets
  - diagonal-argument
  - equipotence
  - transcendental-numbers
  - uncountable-sets
---

## Insiemi finiti e numerabili

La cardinalità di un insieme finito $A$ è il numero dei suoi elementi e si indica con $|A|.$ Contare gli elementi significa abbinarli ai numeri $1,2,\ldots,n,$ assegnando un numero diverso a ciascun elemento e usando tutti i numeri da $1$ a $n.$ Quando $A$ è vuoto, la sua cardinalità è $0.$ Indichiamo ad esempio l'insieme dei numeri naturali nel seguente modo:

$$\mathbb{N}=\{0,1,2,3,\ldots\} \tag{1}$$
Per ogni $n\in\mathbb{N},$ con $\mathbb{N}$ definito nella $(1),$ poniamo:

$$
I_n=\{\ k\in\mathbb{N}\mid 1\leq k\leq n \ \} \tag{2}
$$

In questo modo $I_n$ contiene esattamente $n$ elementi, quindi per esempio $I_3=\{1,2,3\}.$ Un insieme $A$ ha cardinalità finita $n$ se esiste una corrispondenza biunivoca fra $A$ e $I_n,$ cioè una relazione biettiva in cui a ogni elemento di $A$ corrisponde uno e un solo elemento di $I_n$ e viceversa. Usando la medesima relazione, possiamo confrontare anche due generici insiemi infiniti $A$ e $B$ che si dicono equipotenti quando esiste una relazione $f\colon A\to B,$ caratterizzata da una corrispondenza biunivoca fra i loro elementi. L'equipotenza e l'uguaglianza delle cardinalità si indicano con la seguente relazione:

$$
A\sim B \iff |A|=|B| \tag{3}
$$

Nel caso di insiemi finiti, la $(3)$ esprime il fatto che i due insiemi hanno lo stesso numero di elementi. Vediamo ora il concetto di numerabilità che, come abbiamo anticipato all'inizio, esprime la possibilità di elencare tutti gli elementi di un insieme, senza che vi siano ripetizioni, in modo che ciascuno di essi occupi una posizione identificata da un numero naturale. Un insieme $A$ è infinito numerabile quando è equipotente all'insieme dei numeri naturali. Un insieme è numerabile se è finito oppure infinito numerabile, ed è non numerabile se non rientra in nessuno di questi casi. Un insieme finito non può essere equipotente a $\mathbb{N}$ poiché se contiene $n$ elementi, abbinando ciascuno di essi a un numero naturale diverso si usano soltanto $n$ numeri naturali mentre, come abbiamo detto, una corrispondenza biunivoca deve comprendere tutti gli elementi di entrambi gli insiemi.

La relazione di equipotenza $\sim,$ introdotta nella $(3),$ mette dunque in relazione gli insiemi che hanno la stessa cardinalità e soddisfa le proprietà riflessiva, simmetrica e transitiva come riportato nelle seguenti implicazioni:

$$
\begin{align}
&A\sim A \\[6pt]
&A\sim B \implies B\sim A \\[6pt]
&A\sim B \text{ e } B\sim C \implies A\sim C
\end{align} \tag{4}
$$

Nella $(4)$, la prima relazione rappresenta la riflessività e segue dal fatto che l'applicazione identità è una biiezione di un generico insieme $A$ su se stesso. La seconda relazione è quella di simmetria ed è determinata dal fatto che per ogni biiezione $f\colon A\to B$ esiste una biiezione inversa $f^{-1}\colon B\to A.$  Infine, la terza relazione determina la transitività che è giustificata dal fatto che, date due biiezioni $f\colon A\to B$ e $g\colon B\to C,$ la composizione $g\circ f$ è ancora una biiezione da $A$ a $C.$

Quando scegliamo una biiezione $f\colon\mathbb{N}\to A$ e associamo a ogni numero naturale $n$ l'elemento $a_n=f(n),$ otteniamo un'enumerazione di $A,$ ossia un elenco dei suoi elementi che possiamo rappresentare come segue:

$$
A=\{a_0,a_1,a_2,a_3,\ldots\} \tag{5}
$$

Nella $(5),$ l'iniettività di $f$ garantisce che a indici diversi corrispondano elementi diversi, quindi nessun elemento compare mai due volte, mentre per la suriettività ogni elemento di $A$ compare sicuramente nell'elenco. Ad esempio, per dimostrare che l'insieme $\mathbb{Z}$ è infinito numerabile, costruiamo un'enumerazione del tipo $(5)$ che comprenda lo zero, gli interi positivi e quelli negativi, quindi definiamo una relazione $f\colon\mathbb{N}\to\mathbb{Z}$ ponendo:

$$
f(n)=
\begin{cases}
\dfrac{n}{2} & \text{se } n \text{ è pari} \\[6pt]
-\dfrac{n+1}{2} & \text{se } n \text{ è dispari}
\end{cases} \tag{6}
$$

Scriviamo ora l'indice pari come $n=2k$ e l'indice dispari come $n=2k+1,$ con $k\in\mathbb{N},$ e, sostituendoli nella $(6),$ otteniamo:

$$
\begin{align}
&f(2k)=k \\[6pt]
&f(2k+1)=-(k+1)
\end{align} \tag{7}
$$

La prima riga della $(7)$ mostra che gli indici pari producono tutti gli interi non negativi, mentre la seconda uguaglianza mostra che gli indici dispari producono tutti gli interi negativi. Poiché i due gruppi sono disgiunti e insieme comprendono tutto $\mathbb{Z},$ l'applicazione nella $(6)$ è sia iniettiva sia suriettiva, e dunque è una biiezione. Per ottenere l'enumerazione degli elementi basta seguire l'ordine degli indici $n=0,1,2,3,\ldots$ da cui deriva:

$$
\mathbb{Z}=\{0,-1,1,-2,2,-3,3,\ldots\} \tag{8}
$$

Poiché nella $(8)$ ogni intero compare esattamente una volta, allora possiamo concludere che $\mathbb{Z}$ è infinito numerabile. Facciamo un altro esempio, considerando l'insieme $E$ dei numeri naturali pari e dimostrando che è infinito numerabile:

$$E=\{\ 2n\mid n\in\mathbb{N} \ \} \tag{9}$$

Dalla $(9)$ si ha che l'applicazione $n\mapsto2n$ associa a ogni naturale un numero pari distinto e raggiunge tutti gli elementi di $E$ per cui è una biiezione da $\mathbb{N}$ a $E,$ perciò $E$ è infinito numerabile. Inoltre, si dice che $E$ è un sottoinsieme proprio di $\mathbb{N},$ perché non contiene i numeri dispari, ma ha la stessa cardinalità di $\mathbb{N}.$ Notate come questa caratteristica non valga invece per un insieme finito perché ogni suo eventuale sottoinsieme proprio contiene meno elementi dell'insieme che lo contiene.

## Sottoinsiemi infiniti dei numeri naturali

L'esempio dei numeri pari nella $(9)$ mostra come un sottoinsieme infinito dei naturali possa avere la stessa cardinalità di $\mathbb{N}.$ Vediamo adesso che questo vale in generale per ogni sottoinsieme infinito $A\subseteq\mathbb{N}$ e per dimostrarlo, elenchiamo gli elementi di $A$ in ordine crescente, scegliendo a ogni passo il più piccolo tra quelli non ancora elencati. Questa scelta è possibile grazie al buon ordinamento dei numeri naturali, cioè alla proprietà per cui ogni loro sottoinsieme non vuoto ammette sempre un minimo. Definiamo quindi $f(0)=\min A.$ Una volta scelti $f(0),\ldots,f(n),$ il termine successivo è dato dalla seguente uguaglianza:

$$
f(n+1)=\min\ \bigl(A\setminus\{f(0),\ldots,f(n)\}\bigr) \tag{10}
$$

La costruzione nella $(10)$ può proseguire per ogni $n\in\mathbb{N}$ e dopo ogni scelta, tutti gli elementi ancora disponibili sono maggiori del minimo scelto, quindi il valore successivo è necessariamente maggiore del precedente. Inoltre, poiché stiamo considerando i numeri naturali, ogni incremento è almeno $1$ e quindi partendo da $f(0)\geq0$ e per ogni $n\in\mathbb{N}$ otteniamo:

$$
\begin{align}
&f(0)\lt f(1)\lt f(2)\lt\cdots \\[6pt]
&f(n)\geq n
\end{align} \tag{11}
$$

La prima riga della $(11)$ dimostra l'iniettività di $f,$ perché a indici diversi corrispondono valori diversi. Per dimostrare la suriettività, supponiamo per assurdo che esista un elemento $a\in A$ che non viene mai raggiunto da $f,$ cioè che $f(n)\neq a$ per ogni $n\in\mathbb{N}.$ Ora notate che quando scegliamo $f(a),$ l'elemento $a$ è ancora disponibile e poiché la $(10)$ impone di scegliere il minimo tra gli elementi rimasti, abbiamo:

$$f(a)\leq a \tag{12}$$

Se combiniamo la $(12)$ con la seconda riga della $(11)$ otteniamo:

$$
a\leq f(a)\leq a \implies f(a)=a \tag{13}
$$

La $(13)$ dà $f(a)=a,$ in contraddizione con l'ipotesi $f(n)\neq a,$ quindi ogni elemento di $A$ viene dunque raggiunto, perciò $f$ è una biiezione da $\mathbb{N}$ ad $A$ e $A$ è infinito numerabile. Da questo risultato segue che ogni sottoinsieme di un insieme numerabile è numerabile. Supponiamo infatti che $B$ sia numerabile e $A\subseteq B.$ Se $B$ è finito, anche $A$ è necessariamente finito. Quando $B$ è infinito numerabile, scegliamo una biiezione $h\colon B\to\mathbb{N}$ e limitando il dominio ad $A,$ otteniamo una biiezione fra $A$ e la sua immagine:

$$
h|_A\colon A\to h(A) \tag{14}
$$

Quindi per la $(14)$ concludiamo che ogni sottoinsieme $A$ di un insieme numerabile $B$ è numerabile.

## Criteri di numerabilità

Negli esempi degli interi e dei naturali pari abbiamo dimostrato la numerabilità costruendo una biiezione con $\mathbb{N}.$ Vediamo adesso come ottenere lo stesso risultato senza dover costruire una biiezione.

Possiamo infatti ammettere ripetizioni nell'elenco degli elementi, oppure assegnare loro numeri naturali distinti senza usarli tutti.

Abbiamo due criteri. Nel primo possiamo ammettere ripetizioni nell'elenco degli elementi richiedendo un'applicazione suriettiva dai naturali ad $A$ che possiamo rappresentare come:

$$
f\colon\mathbb{N}\to A \text{ suriettiva} \tag{15}
$$

La $(15)$ permette di elencare tutti gli elementi di $A,$ ammettendo che uno stesso elemento compaia più volte. Nel secondo criterio dobbiamo richiedere invece un'applicazione iniettiva definita in questo modo:

$$
g\colon A\to\mathbb{N} \text{ iniettiva} \tag{16}
$$

Dimostriamo che ciascuna delle condizioni $(15)$ e $(16)$ equivale alla numerabilità di un insieme non vuoto $A.$ Partiamo dal caso in cui $A$ è numerabile e costruiamo una relazione suriettiva da $\mathbb{N}$ ad $A,$ come richiesto dalla $(15).$ Se $A$ è infinito, l'enumerazione $(5)$ fornisce già una biiezione e dunque una suriezione. Se invece $A$ è finito con $m\geq1$ elementi, possiamo elencarli come $a_0,\ldots,a_{m-1}$ e definiamo:

$$
f(k)=
\begin{cases}
a_k & \text{se } 0\leq k<m \\[6pt]
a_0 & \text{se } k\geq m
\end{cases} \tag{17}
$$

Nella $(17),$ i valori $f(0),\ldots,f(m-1)$ comprendono tutti gli elementi di $A,$ mentre i valori successivi ripetono $a_0$ e quindi $f$ è suriettiva anche in questo caso. Mostriamo ora come da una relazione suriettiva del tipo $(15)$ si ottenga un'iniezione del tipo $(16).$ Dato $a\in A,$ consideriamo tutti gli indici $n$ per cui $f(n)=a$ e scegliamo il più piccolo tale che:

$$
g(a)=\min\{\ n\in\mathbb{N}\mid f(n)=a \ \} \tag{18}
$$

L'insieme definito nella $(18)$ non è vuoto perché sappiamo che $f$ è suriettiva, e quindi esiste un minimo per il principio del buon ordinamento dei naturali già citato. Poiché $g(a)$ è il primo indice per cui $f$ assume il valore $a,$ applicando $f$ a tale indice otteniamo:

$$
f(g(a))=a \tag{19}
$$

Se avessimo $g(a)=g(b),$ applicando $f$ a entrambi i membri otterremmo $f(g(a))=f(g(b))$ e per la $(19),$ il primo membro è uguale ad $a$ e il secondo a $b,$ quindi $a=b.$ Lo stesso indice non può dunque essere assegnato a due elementi distinti, perciò $g$ è iniettiva.

Infine, un'iniezione del tipo $(16)$ mette $A$ in corrispondenza biunivoca con l'insieme dei naturali effettivamente utilizzati, cioè con l'immagine $g(A).$ Nella sezione 'Sottoinsiemi infiniti dei numeri naturali' abbiamo dimostrato che ogni sottoinsieme di un insieme numerabile è numerabile, quindi anche $g(A)\subseteq\mathbb{N}$ è numerabile. Anche $A,$ essendo equipotente a $g(A),$ è numerabile. Abbiamo così dimostrato che la numerabilità implica la $(15),$ che la $(15)$ implica la $(16)$ e che la $(16)$ implica a sua volta la numerabilità. In generale, nei criteri $(15)$ e $(16),$ al posto di $\mathbb{N}$ si può usare qualunque insieme infinito numerabile, poiché è equipotente a $\mathbb{N}.$

## Prodotti e unioni di insiemi numerabili

Vediamo ora perché il prodotto di un numero finito di insiemi numerabili è ancora numerabile. Partiamo da $\mathbb{N}\times\mathbb{N},$ i cui elementi sono coppie di naturali, e costruiamo un'enumerazione che le comprenda tutte senza ripetizioni. Per farlo iniziamo a raggruppare tutte le coppie $(j,k)$ secondo la somma $s=j+k.$ Per ogni $s$ il gruppo contiene le $s+1$ coppie del tipo:

$$(s,0),(s-1,1),\ldots,(0,s)$$

Se elenchiamo i gruppi ottenuti per somma crescente abbiamo:

$$
\mathbb{N}\times\mathbb{N}=\{(0,0),\ (1,0),\ (0,1),\ (2,0),\ (1,1),\ (0,2),\ (3,0),\ldots\} \tag{20}
$$

Nella $(20)$ ogni coppia compare nell'elenco, perché è preceduta da un numero finito di gruppi, ciascuno contenente un numero finito di coppie. I gruppi con somma minore di $s$ contengono complessivamente $s(s+1)/2$ coppie. Nel gruppo di somma $s,$ la coppia $(j,k)$ occupa la posizione $k,$ contando da zero. Sostituendo $s=j+k,$ il suo indice nell'elenco è quindi:

$$
\pi(j,k)=\frac{(j+k)(j+k+1)}{2}+k \tag{21}
$$

La $(21)$ assegna alle coppie della $(20)$ gli indici consecutivi $0,1,2,\ldots,$ senza ripetizioni e senza omettere alcun indice, pertanto è una biiezione da $\mathbb{N}\times\mathbb{N}$ a $\mathbb{N},$ che viene anche detta funzione di accoppiamento di Cantor. Possiamo estendere il risultato della $(21)$ ad altri insiemi, considerando che sostituire i fattori con insiemi equipotenti non cambia la cardinalità del prodotto. Supponiamo che $f\colon A\to C$ e $g\colon B\to D$ siano biiezioni e definiamo:

$$
\begin{align}
&h\colon A\times B\to C\times D \\[6pt]
&h(a,b)=(f(a),g(b))
\end{align} \tag{22}
$$

Nella $(22)$ abbiamo una relazione iniettiva perché l'uguaglianza delle immagini implica $f(a)=f(a')$ e $g(b)=g(b'),$ dunque $a=a'$ e $b=b'.$ Inoltre la relazione è anche suriettiva perché ogni coppia $(c,d)$ è l'immagine di $(f^{-1}(c),g^{-1}(d))$ e pertanto $A\times B\sim C\times D,$ ovvero i due prodotti cartesiani hanno la stessa cardinalità. Poiché $\mathbb{Z}\sim\mathbb{N},$ applicando la $(22)$ e poi la $(21)$ ripetendo il procedimento per un numero finito di fattori otteniamo:

$$
\begin{align}
&\mathbb{Z}\times\mathbb{Z}\sim\mathbb{N}\times\mathbb{N}\sim\mathbb{N} \\[6pt]
&\mathbb{N}^k\sim\mathbb{N} \qquad \text{per ogni } k\geq1
\end{align} \tag{23}
$$

Per estendere la $(23)$ al prodotto di $k$ insiemi numerabili qualsiasi, associamo agli elementi di ciascun fattore dei numeri naturali distinti, ottenendo un'iniezione del prodotto nell'insieme $\mathbb{N}^k$ delle $k$-uple di naturali. Poiché la $(23)$ fornisce una biiezione fra $\mathbb{N}^k$ e $\mathbb{N},$ componendo le due applicazioni otteniamo un'iniezione del prodotto in $\mathbb{N},$ che per il criterio $(16)$ ne dimostra la numerabilità, mentre se un fattore è vuoto il prodotto è vuoto e dunque finito.

- - -

Passiamo ora alle unioni degli insiemi numerabili, mostrando che riunire una famiglia numerabile di insiemi numerabili produce ancora un insieme numerabile, anche se gli insiemi hanno elementi in comune. Consideriamo ad esempio la seguente unione:

$$U=\bigcup_{i\in\mathbb{N}}A_i \tag{24}$$
Se nella $(24)$ $U$ è vuoto, il risultato è immediato. In caso contrario scegliamo $a\in U$ e sostituiamo gli $A_i$ vuoti con $\{a\},$ senza modificare $U.$ Per la $(15),$ ogni $A_i$ ammette una relazione suriettiva del tipo $f_i\colon\mathbb{N}\to A_i,$ perciò definiamo:

$$
\begin{align}
&F\colon\mathbb{N}\times\mathbb{N}\to U \\[6pt]
&F(i,j)=f_i(j)
\end{align} \tag{25}
$$

Nella $(25),$ l'indice $i$ è relativo all'insieme mentre $j$ a un elemento del suo elenco. Abbiamo che ogni $x\in U$ appartiene a qualche $A_i$ ed è quindi uguale a $f_i(j)$ per qualche $j,$ perciò $F$ è suriettiva. Componendo $F$ con l'inversa della $(21),$ possiamo ottenere una suriezione da $\mathbb{N}$ a $U,$ che dimostra la numerabilità dell'unione per il criterio $(15).$

- - -

I risultati sui prodotti e il criterio di suriettività permettono anche di dimostrare la numerabilità dei razionali, rappresentando ogni frazione mediante il numeratore e il denominatore. Consideriamo cioè:

$$
\begin{align}
&q\colon\mathbb{Z}\times(\mathbb{N}\setminus\{0\})\to\mathbb{Q} \\[6pt]
&q(p,n)=\frac{p}{n}
\end{align} \tag{26}
$$

Il dominio della $(26)$ è infinito numerabile per quanto dimostrato sui prodotti e $q$ è suriettiva perché ogni razionale è il quoziente di un intero per un intero positivo. Il criterio $(15)$ garantisce quindi che $\mathbb{Q}$ è numerabile, e la presenza di $\mathbb{Z}\subseteq\mathbb{Q}$ esclude che sia finito. Le diverse coppie che rappresentano la stessa frazione, come $(1,2)$ e $(2,4),$ non creano problemi, perché il criterio ammette ripetizioni.

## Non numerabilità dei numeri reali

Con la $(26)$ abbiamo dimostrato che i razionali possono essere elencati usando i numeri naturali. Vediamo ora perché questo non è possibile per i numeri reali, mostrando che l'intervallo $(0,1]$ non ammette un'enumerazione. Il procedimento consiste nel supporre che esista un possibile elenco completo e costruire un numero dell'intervallo che non vi compare. Scegliamo quindi uno sviluppo decimale unico per ogni numero perché, sebbene possa sembrare controintuitivo, alcuni numeri ne ammettono due, come mostra la seguente serie geometrica:

$$
0.999\ldots=\sum_{n=1}^{\infty}\frac{9}{10^n}=\frac{9/10}{1-1/10}=1 \tag{27}
$$

Nei casi con due rappresentazioni scegliamo quella che prosegue con i $9$ e con questa convenzione ogni $x\in(0,1]$ ha un unico sviluppo della forma:

$$
\begin{align}
&x=0.a_1a_2a_3\ldots \\[6pt]
&a_n\in\{0,1,\ldots,9\}
\end{align} \tag{28}
$$

Da una certa posizione in poi, nella $(28)$ le cifre non sono tutte nulle, e anche l'estremo $1$ è rappresentato nella forma richiesta grazie alla $(27).$ Supponiamo ora per assurdo che $(0,1]$ sia numerabile e quindi scrivendo ogni termine nella forma della $(28),$ otterremmo:

$$
\begin{align}
&x_1=0.a_{11}a_{12}a_{13}a_{14}\ldots \\[6pt]
&x_2=0.a_{21}a_{22}a_{23}a_{24}\ldots \\[6pt]
&x_3=0.a_{31}a_{32}a_{33}a_{34}\ldots \\[6pt]
&x_4=0.a_{41}a_{42}a_{43}a_{44}\ldots \\[6pt]
&\cdots
\end{align} \tag{29}
$$

Nella $(29),$ il primo indice di $a_{nk}$ indica il numero $x_n$ e il secondo la posizione della cifra. Consideriamo dunque le cifre diagonali $a_{11},a_{22},a_{33},\ldots$ e modifichiamo ciascuna di esse secondo la seguente regola:

$$
d_n=
\begin{cases}
6 & \text{se } a_{nn}=5 \\[6pt]
5 & \text{se } a_{nn}\neq5
\end{cases} \tag{30}
$$

A questo punto usiamo le cifre della $(30)$ per costruire il numero:

$$
y=0.d_1d_2d_3\ldots \tag{31}
$$

Tutte le cifre di $y$ sono $5$ o $6,$ quindi $y\in(0,1]$ e lo sviluppo $(31)$ rispetta la convenzione scelta, senza terminare con soli zeri. Per ogni $n,$ la regola $(30)$ dà $d_n\neq a_{nn},$ perciò $y$ differisce da $x_n$ nella cifra di posizione $n.$ Poiché stiamo confrontando gli sviluppi unici fissati dalla convenzione, segue che $y\neq x_n$ per ogni $n\geq1.$ Il numero $y$ appartiene dunque all'intervallo ma non compare nell'elenco $(29),$ in contraddizione con l'ipotesi che questo comprenda tutti i suoi elementi e quindi l'intervallo $(0,1]$ non è numerabile, e neppure $\mathbb{R}$ può esserlo, perché ogni sottoinsieme di un insieme numerabile è numerabile.

## Altre applicazioni

Applichiamo i risultati della numerabilità sui prodotti e sulle unioni ai numeri algebrici e alle successioni finite. Sappiamo che un numero reale è algebrico se è radice di un polinomio non nullo a coefficienti interi, altrimenti è trascendente. Se fissiamo $n,H\in\mathbb{N},$ i polinomi di questo tipo con grado al più $n$ e coefficienti di valore assoluto al più $H$ sono in numero finito e hanno complessivamente un insieme finito di radici reali $E_{n,H}.$ Ogni algebrico appartiene a uno di questi insiemi, quindi vale:

$$
\mathcal{A}=\bigcup_{(n,H)\in\mathbb{N}\times\mathbb{N}}E_{n,H} \tag{32}
$$

Poiché $\mathbb{N}\times\mathbb{N}$ è numerabile per la $(21),$ la $(32)$ è un'unione numerabile di insiemi finiti e $\mathcal{A}$ è numerabile. I numeri trascendenti sono invece non numerabili, altrimenti anche $\mathbb{R},$ che è dato dall'unione dei numeri algebrici e trascendenti, sarebbe numerabile.

Vediamo ora che anche l'insieme delle successioni finite di numeri naturali è numerabile. Le successioni di lunghezza $k$ formano infatti $\mathbb{N}^k,$ mentre $\mathbb{N}^0$ contiene la sola successione vuota, quindi l'insieme che le comprende tutte è dato dall'unione:

$$
\mathcal{S}=\bigcup_{k\in\mathbb{N}}\mathbb{N}^k \tag{33}
$$

Per la $(23)$ ciascun insieme della $(33)$ è numerabile e quindi anche la loro unione $\mathcal{S}$ è numerabile. Associando ogni sottoinsieme finito di $\mathbb{N}$ alla successione crescente dei suoi elementi, otteniamo un'iniezione in $\mathcal{S},$ perciò anche la collezione dei sottoinsiemi finiti è numerabile.
