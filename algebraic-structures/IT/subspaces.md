---
title: Sottospazi
source: https://algebrica.org/subspaces/
license: CC BY-NC 4.0
tags:
  - basis
  - complement
  - dimension
  - direct-sum
  - grassmann-formula
  - linear-algebra
  - span
  - subspaces
  - vector-spaces
---

## Definizione di sottospazio

Uno [spazio vettoriale](../vector-spaces/) $V$ su un [campo](../fields/) $F$ ha un'addizione e una moltiplicazione per scalari. Per un [sottoinsieme](../sets/) $W \subseteq V,$ queste operazioni si possono restringere a $W$ soltanto quando i loro valori appartengono a $W.$ I tre sottoinsiemi seguenti non soddisfano questo requisito per ragioni diverse.

Il primo quadrante $Q = \{\ (x, y) \in \mathbb{R}^2 \mid x \geq 0,\ y \geq 0 \ \}$ contiene la somma di ogni coppia di suoi elementi, poiché la somma di numeri non negativi è non negativa. Non è chiuso rispetto alla moltiplicazione per scalari, perché $(-1)(1, 1) = (-1, -1)$ non appartiene a $Q.$

L'unione $U$ dei due assi coordinati contiene $\alpha\mathbf{v}$ per ogni $\mathbf{v} \in U$ e ogni $\alpha \in \mathbb{R},$ poiché ogni multiplo scalare di un vettore su uno dei due assi appartiene allo stesso asse. Non è chiusa rispetto all'addizione, perché $(1, 0) + (0, 1) = (1, 1)$ non appartiene a nessuno dei due assi.

La retta $r$ di equazione $y = x + 1$ non contiene l'origine. Non può essere uno spazio vettoriale rispetto alle operazioni ereditate, poiché ogni spazio vettoriale contiene il [vettore nullo](../vectors/).

Le due condizioni di chiusura non si implicano a vicenda e, senza richiedere che il sottoinsieme sia non vuoto, nessuna delle due garantisce che esso contenga il vettore nullo. Un sottoinsieme che contiene il vettore nullo e soddisfa entrambe le condizioni di chiusura è un sottospazio.

Un sottoinsieme $W$ di uno spazio vettoriale $V$ su $F$ è un sottospazio di $V$ quando $W$ è a sua volta uno spazio vettoriale su $F$ rispetto alle operazioni ereditate da $V.$ I sottoinsiemi $\{\ \mathbf{0} \ \}$ e $V$ sono sottospazi per ogni $V.$ Questi sono i sottospazi banali.

## Il criterio di sottospazio

Non occorre verificare tutti gli assiomi di spazio vettoriale, poiché la maggior parte di essi è costituita da identità valide per tutti i vettori di $V$ e quindi per quelli di $W.$ L'associatività e la commutatività dell'addizione, le due leggi distributive e la compatibilità della moltiplicazione per scalari non richiedono ulteriori verifiche. Restano da controllare la chiusura rispetto alle due operazioni e l'appartenenza del vettore nullo e degli opposti.

Un sottoinsieme $W \subseteq V$ è un sottospazio se e solo se valgono le tre condizioni seguenti:

+ $\mathbf{0} \in W$
+ $\mathbf{u} + \mathbf{v} \in W$ per ogni $\mathbf{u}, \mathbf{v} \in W$
+ $\alpha\mathbf{v} \in W$ per ogni $\alpha \in F$ e $\mathbf{v} \in W$

La prima condizione garantisce che il vettore nullo appartenga a $W.$ La terza garantisce che ogni opposto appartenga a $W,$ poiché $-\mathbf{v} = (-1)\mathbf{v}$ quando $\mathbf{v} \in W.$ La seconda e la terza garantiscono che le due operazioni siano ben definite su $W.$

La prima condizione può essere sostituita dal requisito che $W$ sia non vuoto. Scegliendo un qualsiasi $\mathbf{v} \in W$ e applicando la terza condizione con $\alpha = 0$ si ottiene $0\mathbf{v} = \mathbf{0} \in W.$ Scrivere esplicitamente la condizione permette però di escludere subito ogni candidato che non contenga l'origine.

Le due condizioni di chiusura si possono riunire in una sola. Il sottoinsieme $W$ è un sottospazio quando è non vuoto e vale:

$$\alpha\mathbf{u} + \beta\mathbf{v} \in W \qquad \text{per ogni } \mathbf{u}, \mathbf{v} \in W \text{ e per ogni } \alpha, \beta \in F$$

Con $\alpha = \beta = 1,$ la condizione esprime la chiusura rispetto all'addizione, mentre con $\beta = 0,$ esprime la chiusura rispetto alla moltiplicazione per scalari. L'[induzione](../principle-of-mathematical-induction/) sul numero dei termini dimostra la stessa affermazione per ogni [combinazione lineare](../linear-combinations/) finita, quindi un sottospazio contiene ogni combinazione lineare dei propri elementi.

## Soluzioni di un sistema omogeneo

Sia $A$ una matrice $m \times n$ a coefficienti reali. L'insieme delle soluzioni del [sistema](../systems-of-linear-equations/) omogeneo associato è:

$$\mathcal{S} = \{\ \mathbf{x} \in \mathbb{R}^n \mid A\mathbf{x} = \mathbf{0} \ \}$$

Poiché $A\mathbf{0} = \mathbf{0},$ l'origine appartiene a $\mathcal{S}.$ Per $\mathbf{x}, \mathbf{y} \in \mathcal{S}$ e $\alpha, \beta \in \mathbb{R},$ l'[applicazione lineare](../linear-maps/) $\mathbf{x} \mapsto A\mathbf{x}$ soddisfa:

$$A(\alpha\mathbf{x} + \beta\mathbf{y}) = \alpha A\mathbf{x} + \beta A\mathbf{y} = \mathbf{0}$$

L'insieme $\mathcal{S}$ è dunque un sottospazio di $\mathbb{R}^n$ ed è il [nucleo](../kernel-and-image-of-a-linear-map/) dell'applicazione $\mathbf{x} \mapsto A\mathbf{x}.$ Se $r$ è il [rango](../rank-of-a-matrix/) di $A,$ dopo l'[eliminazione di Gauss](../gaussian-elimination/) il sistema ridotto ha $n - r$ variabili libere e la sua parametrizzazione usuale ha un vettore di base per ciascuna variabile libera. Pertanto $\dim \mathcal{S} = n - r = n - \mathrm{rank}(A).$

L'insieme delle soluzioni di un sistema $A\mathbf{x} = \mathbf{b}$ con $\mathbf{b} \neq \mathbf{0}$ non è un sottospazio, poiché $\mathbf{x} = \mathbf{0}$ non soddisfa l'equazione. Il [teorema di Rouché-Capelli](../rouche-capelli-theorem/) stabilisce se il sistema ammette soluzioni. Se ne ammette e $\mathbf{x}_0$ è una di esse, l'insieme delle soluzioni è il traslato $\mathbf{x}_0 + \mathcal{S},$ i cui elementi hanno la forma $\mathbf{x}_0 + \mathbf{s}$ con $\mathbf{s} \in \mathcal{S}.$

> Il traslato di un sottospazio si chiama sottospazio affine. Le rette e i piani che non passano per l'origine sono sottospazi affini, ma non sottospazi vettoriali. L'insieme delle soluzioni di un sistema omogeneo è un sottospazio, mentre quello di un sistema non omogeneo compatibile è un sottospazio affine.

## Sottospazi del piano e dello spazio

I sottospazi di $\mathbb{R}^2$ sono il sottospazio nullo, le [rette](../lines/) passanti per l'origine e $\mathbb{R}^2$ stesso. Se $W$ contiene un vettore non nullo $\mathbf{v},$ ogni multiplo $\alpha\mathbf{v}$ appartiene a $W.$ Questi multipli formano la retta passante per l'origine con direzione $\mathbf{v}.$ Se $W$ contiene un secondo vettore $\mathbf{w}$ esterno a tale retta, allora $\mathbf{v}$ e $\mathbf{w}$ formano una base di $\mathbb{R}^2,$ quindi $W = \mathbb{R}^2.$

I sottospazi di $\mathbb{R}^3$ sono il sottospazio nullo, le rette passanti per l'origine, i [piani passanti per l'origine](../planes/) e $\mathbb{R}^3$ stesso. Ciascuno è l'insieme delle soluzioni di un sistema omogeneo. Un piano ha un'equazione $ax + by + cz = 0$ con $(a, b, c) \neq (0, 0, 0),$ e una retta è l'insieme delle soluzioni di due equazioni indipendenti di questa forma.

La dimensione distingue questi casi. Ogni sottospazio di $\mathbb{R}^n$ ha una dimensione $k$ con $0 \leq k \leq n$ ed è [linearmente isomorfo](../homomorphisms-and-isomorphisms/) a $\mathbb{R}^k.$

## Sottospazi di spazi di funzioni e di matrici

I polinomi di grado al più $n$ formano un sottospazio dello spazio di tutti i [polinomi](../polynomials/) a coefficienti in $F,$ perché ogni somma e ogni multiplo scalare è il polinomio nullo oppure ha grado al più $n.$ I polinomi di grado esattamente $n$ non formano un sottospazio, poiché la somma di $x^n$ e $1 - x^n$ ha grado $0.$

Nello spazio $M_n(\mathbb{R})$ delle [matrici](../matrices/) quadrate di ordine $n,$ le matrici simmetriche formano un sottospazio, poiché la trasposizione soddisfa $(\alpha A + \beta B)^{\mathrm{T}} = \alpha A^{\mathrm{T}} + \beta B^{\mathrm{T}},$ e il membro destro è uguale a $\alpha A + \beta B$ quando entrambe le matrici sono simmetriche. Le matrici di traccia nulla formano un sottospazio perché la traccia è lineare. Le [matrici invertibili](../inverse-matrix/) non formano invece un sottospazio, poiché l'identità $I$ e la sua opposta $-I$ sono entrambe invertibili, mentre la loro somma è la matrice nulla.

Tra le funzioni $f : \mathbb{R} \to \mathbb{R},$ quelle [continue](../continuous-functions/) formano un sottospazio dello spazio di tutte le funzioni, perché somme e multipli scalari di funzioni continue sono continui. Lo stesso vale per le [funzioni derivabili](../derivatives/), per le funzioni che si annullano in un punto fissato $x_0,$ e per le soluzioni di un'[equazione differenziale](../differential-equations/) lineare omogenea. Le funzioni che soddisfano $f(x_0) = 1$ non formano un sottospazio, poiché tra esse non compare la funzione nulla.

## Intersezione e unione

Sia $\{\ W_i \ \}_{i \in I}$ una famiglia qualsiasi di sottospazi di $V.$ La loro intersezione contiene $\mathbf{0},$ poiché ogni $W_i$ lo contiene. Se $\mathbf{u}$ e $\mathbf{v}$ appartengono all'intersezione e $\alpha, \beta \in F,$ allora $\alpha\mathbf{u} + \beta\mathbf{v}$ appartiene a ogni $W_i$ per la chiusura, e quindi all'intersezione. L'intersezione di una famiglia qualsiasi di sottospazi, finita o infinita, è dunque un sottospazio.

L'unione si comporta diversamente. I due assi coordinati di $\mathbb{R}^2$ sono sottospazi la cui unione non è un sottospazio, come mostra la somma di $(1, 0)$ e $(0, 1).$ Più in generale, supponiamo che $W_1$ e $W_2$ siano sottospazi e che nessuno contenga l'altro. Scegliamo $\mathbf{u} \in W_1$ esterno a $W_2$ e $\mathbf{v} \in W_2$ esterno a $W_1.$ Se $\mathbf{u} + \mathbf{v}$ appartenesse all'unione, per esempio se $\mathbf{u} + \mathbf{v} \in W_1,$ allora $\mathbf{v} = (\mathbf{u} + \mathbf{v}) - \mathbf{u}$ apparterrebbe a $W_1,$ contro la scelta di $\mathbf{v},$ e l'argomento simmetrico esclude $\mathbf{u} + \mathbf{v} \in W_2.$ L'unione di due sottospazi è quindi un sottospazio se e solo se uno dei due contiene l'altro.

## La somma di due sottospazi

Dati due sottospazi $A$ e $B$ di $V,$ la loro somma è definita da:

$$A + B = \{\ \mathbf{a} + \mathbf{b} \mid \mathbf{a} \in A,\ \mathbf{b} \in B \ \}$$

Questo insieme è un sottospazio. Esso contiene $\mathbf{0} = \mathbf{0} + \mathbf{0}.$ Per due suoi elementi $\mathbf{a}_1 + \mathbf{b}_1$ e $\mathbf{a}_2 + \mathbf{b}_2,$ si ha:

$$\alpha(\mathbf{a}_1 + \mathbf{b}_1) + \beta(\mathbf{a}_2 + \mathbf{b}_2) = (\alpha\mathbf{a}_1 + \beta\mathbf{a}_2) + (\alpha\mathbf{b}_1 + \beta\mathbf{b}_2)$$

La prima parentesi appartiene a $A$ e la seconda a $B,$ quindi il risultato appartiene a $A + B.$ Scegliendo $\mathbf{b} = \mathbf{0}$ si ottiene $A \subseteq A + B,$ e simmetricamente $B \subseteq A + B,$ quindi la somma contiene l'unione. Ogni sottospazio $W$ che contiene sia $A$ sia $B$ contiene ogni $\mathbf{a} + \mathbf{b}$ per la chiusura rispetto all'addizione, e quindi contiene $A + B.$ La somma è dunque il più piccolo sottospazio contenente $A \cup B$ ed è il sottospazio generato da tale unione.

La definizione si estende a un numero finito di sottospazi $A_1, \ldots, A_s,$ la cui somma è formata da tutti i vettori $\mathbf{a}_1 + \cdots + \mathbf{a}_s$ con $\mathbf{a}_i \in A_i.$ Quando ogni $A_i$ è la retta $F\mathbf{v}_i$ generata da un singolo vettore, la somma è il sottospazio generato da $\mathbf{v}_1, \ldots, \mathbf{v}_s,$ quindi il sottospazio generato da un insieme finito è un caso particolare di somma di sottospazi.

In $\mathbb{R}^3,$ due piani distinti passanti per l'origine si intersecano in una retta e la loro somma è l'intero spazio, mentre un piano e una retta in esso contenuta hanno come somma il piano stesso. L'intersezione dei due addendi determina la dimensione della somma.

## Formula di Grassmann

Per due sottospazi di dimensione finita $A$ e $B$ di uno spazio vettoriale $V$ vale la formula:

$$\dim(A + B) = \dim A + \dim B - \dim(A \cap B)$$

La dimostrazione parte da una base $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k \ \}$ di $A \cap B.$ Poiché questo insieme è linearmente indipendente in $A,$ si può estendere a una base $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{a}_1, \ldots, \mathbf{a}_p \ \}$ di $A.$ È anche linearmente indipendente in $B,$ quindi si può estendere a una base $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{b}_1, \ldots, \mathbf{b}_q \ \}$ di $B.$ L'unione delle due basi è:

$$\mathcal{B} = \{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{a}_1, \ldots, \mathbf{a}_p, \mathbf{b}_1, \ldots, \mathbf{b}_q \ \}$$

Questo insieme è una base di $A + B.$

Ogni elemento di $A + B$ è la somma di un elemento di $A$ e di un elemento di $B.$ Questi due elementi sono combinazioni lineari delle rispettive basi, quindi $\mathcal{B}$ genera $A + B.$ Per dimostrare l'indipendenza, supponiamo che una combinazione lineare dei vettori di $\mathcal{B}$ sia nulla:

$$\sum_{i=1}^{k} \lambda_i\mathbf{u}_i + \sum_{j=1}^{p} \mu_j\mathbf{a}_j + \sum_{l=1}^{q} \nu_l\mathbf{b}_l = \mathbf{0}$$

Poniamo $\mathbf{w} = \sum_l \nu_l\mathbf{b}_l.$ La relazione implica $\mathbf{w} = -\sum_i \lambda_i\mathbf{u}_i - \sum_j \mu_j\mathbf{a}_j,$ quindi $\mathbf{w}$ appartiene a $A.$ La sua definizione mostra anche che $\mathbf{w}$ appartiene a $B.$ Pertanto $\mathbf{w} \in A \cap B$ e $\mathbf{w} = \sum_i \delta_i\mathbf{u}_i$ per opportuni scalari $\delta_i.$ Le due espressioni di $\mathbf{w}$ implicano:

$$\sum_{i=1}^{k} \delta_i\mathbf{u}_i - \sum_{l=1}^{q} \nu_l\mathbf{b}_l = \mathbf{0}$$

I vettori in questa relazione sono un sottoinsieme della base di $B,$ quindi la loro indipendenza implica $\nu_l = 0$ per ogni $l$ e $\delta_i = 0$ per ogni $i.$ La relazione iniziale si riduce allora a una combinazione nulla della base di $A,$ da cui $\lambda_i = 0$ e $\mu_j = 0.$ Tutti i coefficienti sono nulli, e $\mathcal{B}$ è indipendente.

La base $\mathcal{B}$ ha $k + p + q$ elementi, quindi $\dim(A + B) = k + p + q.$ Poiché $\dim A = k + p$ e $\dim B = k + q,$ la somma $\dim A + \dim B = 2k + p + q$ conta due volte gli $k$ vettori della base dell'intersezione. Sottraendo $\dim(A \cap B) = k$ si ottiene la formula.

- - -

In $\mathbb{R}^4,$ definiamo i due piani:

$$A = \mathrm{span}\{\ (1, 0, 1, 0),\ (0, 1, 0, 1) \ \}, \qquad B = \mathrm{span}\{\ (1, 1, 0, 0),\ (0, 0, 1, 1) \ \}$$

Un vettore di $A$ ha la forma $(a, b, a, b)$ e un vettore di $B$ ha la forma $(c, c, d, d).$ Le due espressioni sono uguali soltanto se $a = c,$ $b = c,$ $a = d$ e $b = d.$ Tutti e quattro i parametri coincidono, e l'intersezione è la retta generata da $(1, 1, 1, 1).$ Per la formula di Grassmann, $\dim(A + B) = 2 + 2 - 1 = 3,$ quindi i due piani generano un iperpiano di $\mathbb{R}^4$ anziché l'intero spazio. Due piani in uno spazio di dimensione quattro possono anche intersecarsi soltanto nell'origine, e in questo caso la loro somma ha dimensione $4.$

## Somme dirette

La scomposizione di un vettore di $A + B$ nella forma $\mathbf{a} + \mathbf{b}$ non è sempre unica. In $\mathbb{R}^2,$ se $A = B = \mathbb{R}^2,$ il vettore $(1, 1)$ ammette le scomposizioni $(1, 1) + (0, 0)$ e $(1, 0) + (0, 1).$ L'unicità della scomposizione dipende dall'intersezione.

La somma $A + B$ si dice diretta, e si scrive $A \oplus B,$ quando ogni vettore di $A + B$ ha esattamente un'espressione $\mathbf{a} + \mathbf{b}$ con $\mathbf{a} \in A$ e $\mathbf{b} \in B.$ Questo accade precisamente quando $A \cap B = \{\ \mathbf{0} \ \}.$ Se l'intersezione contiene un vettore non nullo $\mathbf{w},$ le espressioni $\mathbf{w} + \mathbf{0}$ e $\mathbf{0} + \mathbf{w}$ sono due scomposizioni distinte di $\mathbf{w}.$ Viceversa, se $\mathbf{a}_1 + \mathbf{b}_1 = \mathbf{a}_2 + \mathbf{b}_2,$ allora $\mathbf{a}_1 - \mathbf{a}_2 = \mathbf{b}_2 - \mathbf{b}_1$ è un vettore appartenente a entrambi i sottospazi, quindi è nullo, e le due scomposizioni coincidono.

In questo caso la formula di Grassmann si riduce a:

$$\dim(A \oplus B) = \dim A + \dim B$$

La somma di due sottospazi di dimensione finita è dunque diretta se e solo se $\dim(A + B) = \dim A + \dim B.$

Per più di due addendi, la condizione sulle intersezioni a due a due non è più sufficiente. La somma $A_1 + \cdots + A_s$ è diretta quando l'unica scomposizione del vettore nullo in termini $\mathbf{a}_i \in A_i$ è quella con tutti i termini uguali a $\mathbf{0}.$ La condizione è:

$$\mathbf{0} = \mathbf{a}_1 + \cdots + \mathbf{a}_s \quad \Longrightarrow \quad \mathbf{a}_1 = \cdots = \mathbf{a}_s = \mathbf{0}$$

Questo requisito equivale all'unicità della scomposizione di ogni vettore della somma. Tre rette distinte di $\mathbb{R}^2$ mostrano perché la condizione sulle intersezioni a due a due non basta. Siano $A_1,$ $A_2$ e $A_3$ generate rispettivamente da $(1, 0),$ $(0, 1)$ e $(1, 1).$ Ogni coppia si interseca soltanto nell'origine, ma il vettore nullo ha la scomposizione non banale:

$$(1, 0) + (0, 1) - (1, 1) = (0, 0)$$

La somma delle tre rette ha quindi dimensione $2$ anziché $3.$ Per una somma diretta, ciascun $A_i$ deve intersecare la somma dei sottospazi rimanenti soltanto nell'origine.

## Complementi

Un sottospazio $B$ di $V$ è un complemento del sottospazio $A$ quando $V = A \oplus B,$ ossia quando $A + B = V$ e $A \cap B = \{\ \mathbf{0} \ \}.$ Ogni vettore di $V$ si scompone allora in un unico modo in una componente in $A$ e una componente in $B.$

In dimensione finita un complemento esiste sempre. Una base $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k \ \}$ di $A$ si può estendere a una base $\{\ \mathbf{u}_1, \ldots, \mathbf{u}_k, \mathbf{w}_1, \ldots, \mathbf{w}_{n-k} \ \}$ di $V.$ Sia $B$ il sottospazio generato dai vettori aggiunti. Ogni vettore di $V$ è una combinazione lineare di questa base. I suoi coefficienti determinano una parte in $A$ e una parte in $B,$ quindi $A + B = V.$ Se $\mathbf{x} \in A \cap B,$ allora $\mathbf{x}$ ha un'espressione in termini dei vettori $\mathbf{u}_i$ e un'altra in termini dei vettori $\mathbf{w}_j.$ Sottraendo le due espressioni si ottiene una relazione tra i vettori della base, perciò l'indipendenza implica $\mathbf{x} = \mathbf{0}.$ Le dimensioni soddisfano:

$$\dim A + \dim B = \dim V$$

I complementi non sono unici. In $\mathbb{R}^2$ il sottospazio $A$ generato da $(1, 0)$ ha come complemento ogni altra retta passante per l'origine, comprese le rette generate da $(0, 1)$ e $(1, 1).$ Una base di $A$ ammette diverse estensioni a una base di $V,$ e ogni estensione determina un complemento di dimensione $\dim V - \dim A.$

## Somme dirette interne ed esterne

Il simbolo $\oplus$ indica due costruzioni diverse. Dati spazi vettoriali $V_1, \ldots, V_s$ sullo stesso campo, non necessariamente sottospazi di un medesimo spazio vettoriale, la loro somma diretta esterna è il prodotto cartesiano $V_1 \times \cdots \times V_s$ con operazioni definite componente per componente:

$$(\mathbf{v}_1, \ldots, \mathbf{v}_s) + (\mathbf{w}_1, \ldots, \mathbf{w}_s) = (\mathbf{v}_1 + \mathbf{w}_1, \ldots, \mathbf{v}_s + \mathbf{w}_s), \qquad \alpha(\mathbf{v}_1, \ldots, \mathbf{v}_s) = (\alpha\mathbf{v}_1, \ldots, \alpha\mathbf{v}_s)$$

La sua dimensione è la somma delle dimensioni dei fattori.

La somma diretta interna, trattata sopra, riguarda sottospazi $A_1, \ldots, A_s$ di uno stesso spazio $V.$ La formula $(\mathbf{a}_1, \ldots, \mathbf{a}_s) \mapsto \mathbf{a}_1 + \cdots + \mathbf{a}_s$ definisce un'applicazione lineare dalla somma diretta esterna degli $A_i$ a $V.$ La sua immagine è $A_1 + \cdots + A_s,$ ed essa è iniettiva esattamente quando il vettore nullo ammette soltanto la scomposizione banale. La somma degli $A_i$ è dunque diretta se e solo se questa applicazione è un isomorfismo dalla somma diretta esterna su $A_1 + \cdots + A_s.$
