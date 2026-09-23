---
title: Natural Numbers
source: https://algebrica.org/natural-numbers/
license: CC BY-NC 4.0
tags:
  - addition
  - induction
  - multiplication
  - natural-numbers
  - peano-axioms
  - real-line
  - successor-function
  - von-neumann-construction
  - well-ordering
---

## Costruzione assiomatica

Come abbiamo visto nella loro introduzione generale, i numeri sono organizzati in famiglie secondo una precisa gerarchia, dove ciascun insieme numerico è contenuto nel successivo secondo la seguente relazione:

$$
\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C} \tag{1}
$$

I numeri naturali, il cui insieme è indicato con $\mathbb{N},$ rappresentano il primo tassello della gerarchia rappresentata dalla $(1)$ e nascono informalmente dalla necessità dell'uomo di dover contare gli oggetti. Si possono rappresentare come punti discreti sulla retta reale e a partire dallo $0$, che per convenzione addotteremo appartenente a $\mathbb{N},$ occupano posizioni equidistanti verso destra, corrispondenti a $0, 1, 2, 3, \dots,$ e si estendono indefinitamente in quella direzione.

![IMG. 1](svg/integers-2.svg)

La caratteristica discreta dell'insieme è una delle proprietà che distingue gli interi dai numeri razionali e irrazionali che invece sono distribuiti in modo denso lungo la retta e possono occupare posizioni intermedie comprese tra due interi. Come si vede dalla figura, la retta non menziona gli interi negativi che non appartengono a $\mathbb{N}$ e che vengono introdotti quando si estende l'insieme dei naturali a $\mathbb{Z}.$

In termini formali, i numeri naturali sono introdotti dagli assiomi di Peano che descrivono $\mathbb{N}$ a partire da alcune sue proprietà peculiari, in particolare la presenza di un elemento distinto, rappresentato dallo zero, e di una funzione successore $S : \mathbb{N} \to \mathbb{N},$ che soddisfano le seguenti condizioni

$$
\begin{align}
&\text{(P1)} \quad 0 \in \mathbb{N} \\[6pt]
&\text{(P2)} \quad \forall \ n \in \mathbb{N}, \ S(n) \in \mathbb{N} \\[6pt]
&\text{(P3)} \quad \forall \ n \in \mathbb{N}, \ S(n) \neq 0 \\[6pt]
&\text{(P4)} \quad \forall \ m, n \in \mathbb{N}, \ S(m) = S(n) \implies m = n \\[6pt]
&\text{(P5)} \quad \text{principio di induzione}
\end{align}
$$

Nello specifico i suddetti assiomi sono così interpretabili:

+ $(P1)$ garantisce che $\mathbb{N}$ abbia un elemento iniziale da cui partire per la costruzione dell'insieme.
+ $(P2)$ considera l'operazione di successione $S$ e afferma che ogni successore di un numero interno è anche'esso un numero intero.
+ $(P3)$ afferma che $0$ non è il successore di alcun numero naturale.
+ $(P4)$ garantisce che due numeri naturali distinti abbiano successori distinti. Insieme a $(P3),$ assicura che l'applicazione ripetuta di $S$ a partire da $0$ produca un nuovo elemento a ogni passo.
+ $(P5)$ è il [principio di induzione](../principle-of-mathematical-induction/), secondo cui un sottoinsieme $A\subseteq\mathbb{N}$ coincide con $\mathbb{N}$ se contiene $0$ e, insieme a ogni suo elemento, anche il successore.

> Per dimostrare che una proprietà vale per tutti i numeri naturali, il principio di induzione richiede di verificarla per $0$ e di dimostrare che, per ogni $n\in\mathbb{N},$ se vale per $n,$ allora vale anche per $S(n).$

## Costruzione insiemistica

Gli assiomi di Peano non forniscono un modello esplicito di $\mathbb{N}$ e cioè definiscono quali sono le proprietà che i numeri naturali devono avere senza però specificare come in realtà siano fatti. La moderna matematica propone una costruzione di $\mathbb{N}$ nell'ambito della teoria degli insiemi dove lo zero viene identificato come l'insieme vuoto mentre il successore di un numero naturale è definito come unione di quel numero con l'insieme che lo contiene come unico elemento:
$$ \tag{1}
\begin{align}
&0 = \varnothing \\[6pt]
&S(n) = n \cup \{n\}
\end{align}
$$

Quando si applica ricorsivamente la funzione $S$ otteniamo una successione  di insiemi che realizza i numeri naturali.Per esempio, se vogliamo ottenere il numero naturale $1,$ applichiamo $S$ a $0=\varnothing,$ poiché $1$ è il successore di $0.$ Otteniamo quindi $1=S(0)=0\cup\{0\}=\{\varnothing\}.$ Lo stesso procedimento può essere applicato agli altri numeri ottenendo:

$$\begin{align}
&\vdots\\[6pt]
&2 = \{0, 1\} = \{\varnothing, \{\varnothing\}\} \\[6pt]
&3 = \{0, 1, 2\} \\[6pt]
&4 = \{0, 1, 2, 3\} \\[6pt]
&\vdots
\end{align}$$

Nella costruzione rappresentata dalla $(1)$, ogni numero naturale coincide con l'insieme di tutti i numeri naturali che lo precedono e quindi il numero $n$ ha esattamente $n$ elementi.

## Addizione dei numeri naturali

Analizziamo ora l'operazione di addizione, fissando un numero naturale $m,$ e costruendo una successione che parte da $m$ e passa al successore a ogni passo. Dopo $n$ passi quello che si ottiene è la somma $m + n$ in cui il primo addendo indica il punto di partenza mentre il secondo il numero di applicazioni della funzione $S$. Indichiamo quindi con $S^n$ la funzione che applica il successore $n$ volte. Quando $n = 0$ non si compie alcun passo, quindi possiamo scrivere che $S^0(m) = m.$ Ogni ulteriore passo è invece descritto dalla relazione $S^{S(n)}(m) = S(S^n(m))$ con cui possiamo definire l'addizione come l'operazione binaria $+ : \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ data da:

$$
m + n := S^n(m) \tag{2}
$$

La $(2)$ equivale alle seguenti condizioni ricorsive che valgono per ogni $m, n \in \mathbb{N}:$

$$ \tag{3}
\begin{align}
&m + 0 = m \\[6pt]
&m + S(n) = S(m + n)
\end{align}
$$

La prima stabilisce qual è il valore iniziale mentre la seconda consente di calcolare la somma quando è già nota quella con il secondo addendo precedente. Poiché abbiamo definito la somma come una relazione $\mathbb{N} \to \mathbb{N}$ e $S$ come una funzione che dato un numero produce un altro numero naturale, anche il risultato dell'addizione sarà necessariamente un numero naturale. Ad esempio, proviamo ad utilizzare la definizione ricorsiva data dalla $(3)$ alla somma di $4 + 2.$ Poiché $2=S(1),$ la somma $4+2$ è il successore di $4+1.$ A sua volta, poiché $1=S(0),$ la somma $4+1$ è il successore di $4+0.$ Otteniamo quindi:

$$  
\begin{align}  
4+2 &= S(4+1) \\[6pt]  
&= S(S(4+0)) \\[6pt]  
&= S(S(4)) \\[6pt]  
&= S(5) \\[6pt]  
&= 6  
\end{align}  
$$

Quindi, sommare due numeri $m$ e $n$ significa partire da $m$ e applicare $n$ volte la funzione successore.

- - -

Dopo aver illustrato come è costruita l'operazione di addizione tra numeri naturali, illustriamo ora la proprietà associativa per cui se si raggruppano diversamente gli addendi il risultato della somma non cambia. Consideriamo quindi tre numeri $a, b, c \in \mathbb{N}$ per cui vale la seguente uguaglianza:

$$
(a + b) + c = a + (b + c) \tag{4}
$$

Fissiamo quindi $a$ e $b$ e procediamo per induzione su $c.$ Quando $c = 0,$ per entrambi i membri dell'uguaglianza si ottiene $a + b$. Supponiamo ora che la $(4)$ valga per un numero naturale $c.$ Dobbiamo dimostrare che vale anche per il suo successore, cioè:

$$(a+b)+S(c)=a+(b+S(c))$$

Partiamo dal primo membro e usando definizione ricorsiva dell'addizionee e l'ipotesi induttiva otteniamo:

$$  
\begin{align}  
(a+b)+S(c) &= S((a+b)+c) \\[6pt]  
&= S(a+(b+c)) \\[6pt]  
&= a+S(b+c) \\[6pt]  
&= a+(b+S(c))  
\end{align}  
$$

Abbiamo quindi dimostrato che, se la (4) vale per $c,$ vale anche per $S(c)$ e poiché vale anche per $c=0,$ il principio di induzione assicura che vale per ogni $c\in\mathbb{N}.$

- - -

Dimostriamo ora la proprietà commutativa, secondo cui scambiare l'ordine degli addendi non cambia il risultato della somma. Vogliamo provare che, per ogni $a,n\in\mathbb{N},$ vale:

	$$a+n=n+a \tag{5}$$

Per prima cosa dobbiamo dimostrare che $0+n=n$ per ogni $n\in\mathbb{N}.$ Confrontiamo quindi le funzioni $u(n)=0+n$ e $v(n)=n.$ Per $n=0,$ la prima relazione della $(3)$ dà $u(0)=0+0=0,$ mentre dalla definizione di $v$ abbiamo $v(0)=0,$ il che porta a concludere che le due funzioni hanno lo stesso valore iniziale. Esaminiamo il caso del passaggio da $n$ a $S(n)$ e sempre per la $(3)$ possiamo scrivere:

$$ \tag{6}
\begin{align}
u(S(n)) &= 0+S(n)=S(0+n)=S(u(n)) \\[6pt]
v(S(n)) &= S(n)=S(v(n))
\end{align}
$$

Le uguaglianze della $(6)$ mostrano che le funzioni $u$ e $v$ raggiungono il valore in $S(n)$ applicando il successore al proprio valore in $n.$ Poiché partono dallo stesso valore e seguono la stessa regola, l'unicità del teorema di ricorsione assicura che per ogni $n\in\mathbb{N}$ vale

$$u(n)=v(n) \tag{7}$$

Per ora prendete come assodato questo risultato che sarà spiegato più avanti. Procediamo adesso sostituendo le definizioni di $u$ e $v$ nella $(7)$ così da ottenere $0+n=n.$ Insieme all'identità $n+0=n,$ già contenuta nella $(3),$ questo passaggio dimostra che $0$ è elemento neutro dell'addizione. 

Come secondo punto dobbiamo dimostrare che applicare il successore al primo addendo equivale ad applicarlo al risultato della somma e cioè:

$$S(a)+n=S(a+n)$$

Per questo scegliamo $a$ e confrontiamo le seguenti funzioni:

$$
\begin{align}
p(n) &= S(a)+n \\[6pt]
q(n) &= S(a+n)
\end{align}
$$

In $0$ entrambe valgono $S(a)$ e la $(3)$ si ha:

$$ \tag{8}
\begin{align}
p(S(n)) &= S(a)+S(n)=S(S(a)+n)=S(p(n)) \\[6pt]
q(S(n)) &= S(a+S(n))=S(S(a+n))=S(q(n))
\end{align}
$$

Anche in questo caso, per l'unicità nel teorema di ricorsione le due funzioni coincidono e si ha che $S(a)+n=S(a+n).$ A questo punto, possiamo completare la nostra dimostrazione fissando $a$ e confrontando due nuove funzioni:

$$
\begin{align}
f(n) &= a+n \\[6pt]
g(n) &= n+a
\end{align}
$$

Per le uguaglianze sull'elemento neutro abbiamo che:

$$f(0)=a+0=a=0+a=g(0)$$

Nel passaggio al successore si ha:

$$
\begin{align}
f(S(n)) &= a+S(n)=S(a+n)=S(f(n)) \\[6pt]
g(S(n)) &= S(n)+a=S(n+a)=S(g(n))
\end{align}
$$

Quindi, per l'unicità del teorema di ricorsione, $f=g$ e dunque $a+n=n+a$ per ogni $n\in\mathbb{N},$ il che dimostra la commutatività dell'addizione.

- - -

Facciamo ora un breve accenno al teorema di ricorsione, del quale a noi interessa solo il risultato. Tale teorema afferma che, dati un insieme $X,$ un elemento $x_0\in X$ e una funzione $T:X\to X,$ esiste un'unica funzione $h:\mathbb{N}\to X$ tale che $h(0)=x_0$ e $h(S(n))=T(h(n))$ per ogni $n\in\mathbb{N}.$ 

Quindi se due funzioni $h$ e $k$ soddisfano tali condizioni, allora hanno lo stesso valore iniziale pari a $h(0)=k(0)=x_0.$ Inoltre, entrambe calcolano il valore in $S(n)$ applicando la stessa funzione $T$ al proprio valore in $n$:

$$ \tag{9}
\begin{align}
h(S(n)) &= T(h(n)) \\[6pt]
k(S(n)) &= T(k(n))
\end{align}
$$

Supponendo che $h(n)=k(n)$ per la $(9)$ si ha:

$$h(S(n))=T(h(n))=T(k(n))=k(S(n))$$

Per induzione si dimostra che le funzioni coincidono per ogni numero naturale. Nel caso mostrato nella $(7)$ con $u$ e $v,$ l'insieme $X$ è $\mathbb{N},$ il valore iniziale è $0$ e la funzione $T$ è il successore $S.$

- - -

Mostriamo ora un risultato utile che consente di combinare l'associatività e la commutatività per cambiare come gli addendi sono raggruppati e il loro ordine. Consideriamo ad esempio le seguenti uguaglianza che ci consentono di scambiare gli addendi usando, nell'ordine, l'associatività, la commutatività e di nuovo l'associatività:

$$
\begin{align}
(a+b)+c &= a+(b+c) \\[6pt]
&= a+(c+b) \\[6pt]
&= (a+c)+b
\end{align}
$$

Nel caso di più addendi si ottiene la legge di interscambio che talvolta consente di raggruppare gli addendi e semplificare i calcoli:

$$
\begin{align}
(a+b)+(c+d) &= ((a+b)+c)+d \\[6pt]
&= ((a+c)+b)+d \\[6pt]
&= (a+c)+(b+d)
\end{align}
$$

- - -

Un'ultima proprietà dell'addizione è che l'operazione soddisfa la proprietà di cancellazione, che viene espressa come segue:

$$a+c=b+c\ \Longrightarrow\ a=b \tag{10}$$

Se consideriamo $c=0$ l'uguaglianza si riduce banalmente a $a=b.$ Supponiamo che la proprietà valga per un numero naturale $c$ qualsiasi e consideriamo un'uguaglianza $a+S(c)=b+S(c).$ Per la definizione ricorsiva dell'addizione della $(3)$ possiamo riscriverla come:

$$S(a+c)=S(b+c)$$

Nell'uguaglianza precedente, i numeri $a+c$ e $b+c$ hanno lo stesso successore. Per l'iniettività di $S,$ prevista da $(P4),$ otteniamo quindi $a+c=b+c.$ L'ipotesi induttiva afferma che la proprietà di cancellazione vale quando l'addendo comune è $c.$ Applicandola all'uguaglianza appena ottenuta, concludiamo che $a=b.$ Abbiamo così dimostrato che, se la proprietà vale per $c,$ vale anche per il suo successore $S(c).$ Poiché vale per $c=0,$ il principio di induzione assicura che vale per ogni $c\in\mathbb{N}.$

## Addizione e iterazione di funzioni

Abbiamo visto come la costruzione dell'addizione permette di considerare l'operazione di somma come una sequenza di passi di un procedimento iterativo. Possiamo generalizzare questa relazione anche attraverso il ricorso alle funzioni, considerando un insieme $X,$ una funzione $f : X \to X$ e definendo una funzione iterata $f^n$ ottenuta applicando $f$ per $n$ volte. Le iterate di $f$ sono definite ricorsivamente dalle seguenti relazioni, valide per ogni $x\in X$ e $n\in\mathbb{N}$:

$$ \tag{11}
\begin{align}
f^0(x) &= x \\[6pt]
f^{S(n)}(x) &= f(f^n(x))
\end{align}
$$

Per $f = S$ si ritrova l'iterazione del successore usata nella definizione dell'addizione vista nella $(3)$ mentre per una funzione qualsiasi eseguire prima $m$ applicazioni e poi altre $n$ significa eseguirne $m + n$ e vale:

$$\tag{12}
f^{m+n}(x) = f^n(f^m(x))
$$

Questa identità può essere dimostrata per induzione su $n,$ mantenendo fissi $m$ e $x.$ Nel caso $n = 0,$ il primo membro è $f^m(x)$ perché $m + 0 = m$ e il secondo ha lo stesso valore perché $f^0$ è la funzione identità. Supponiamo ora che il risultato valga per $n.$ Dalla definizione dell'addizione e dalla $(11)$ vale:

$$
\begin{align}
f^{m+S(n)}(x) &= f^{S(m+n)}(x) \\[6pt]
&= f(f^{m+n}(x)) \\[6pt]
&= f(f^n(f^m(x))) \\[6pt]
&= f^{S(n)}(f^m(x))
\end{align}
$$

Poiché abbiamo dimostrato che l'addizione è commutativa, scambiando i due indici si ottiene:

$$
f^n(f^m(x)) = f^{m+n}(x) = f^m(f^n(x))
$$

Pertanto, le iterate di una stessa funzione possono quindi essere composte in entrambi gli ordini con lo stesso risultato.

## Moltiplicazione e potenze

Fino ad ora ci siamo occupati dell'addizione, della sua definizione e delle sue proprietà. Procediamo adesso in maniera simile definendo la moltiplicazione mediante una nuova ricorsione e ponendo per ogni $m \in \mathbb{N}$ le seguenti relazioni:

$$ \tag{12}
\begin{align}
&m \cdot 0 = 0 \\[6pt]
&m \cdot S(n) = m \cdot n + m
\end{align}
$$

Come potete osservare la moltiplicazione è definita a partire dall'addizione. Calcoliamo ad esempio il prodotto $3 \cdot 2$ ricorrendo alla $(12)$ e otteniamo:

$$
\begin{align}
3 \cdot 2 &= 3 \cdot S(S(0)) \\[6pt]
&= 3 \cdot S(0) + 3 \\[6pt]
&= (3 \cdot 0 + 3) + 3 \\[6pt]
&= (0 + 3) + 3 \\[6pt]
&= 6
\end{align}
$$

Il calcolo procede applicando ripetutamente la clausola della moltiplicazione finché il moltiplicatore diventa zero e a quel punto bastano le regole dell'addizione per ottenere il risultato finale.

- - -

Vediamo adesso l'operazione di elevamento a potenza che viene costruito a partire dalla ricorsione della moltiplicazione. In modo speculare alla $(13)$ abbiamo:

$$ \tag{13}
\begin{align}
&m^0 = 1 \\[6pt]
&m^{S(n)} = m^n \cdot m
\end{align}
$$

La seconda uguaglianza riconduce la potenza di base $m$ il cui esponente è un successore a un'ulteriore moltiplicazione per $m$. Come abbiamo quindi visto fino ad ora possiamo concludere che ogni operazione aritmetica è dunque costruita mediante una ricorsione fondata sull'operazione precedente che la caratterizza.

- - - 

La moltiplicazione gode della proprietà associativa e commutativa, ha $1$ come elemento neutro ed è distributiva rispetto all'addizione. Per ogni $a, b, c \in \mathbb{N}$ valgono quindi le uguaglianze:

$$
\begin{align}
&(a \cdot b) \cdot c = a \cdot (b \cdot c) \\[6pt]
&a \cdot b = b \cdot a \\[6pt]
&a \cdot 1 = a \\[6pt]
&a \cdot (b + c) = a \cdot b + a \cdot c
\end{align}
$$

Il prodotto soddisfa inoltre la cancellazione dei fattori non nulli, ovvero Per ogni $a, b, c \in \mathbb{N},$ l'uguaglianza $a \cdot c = b \cdot c$ implica $a = b$ quando $c \neq 0.$ Vale infine l'assenza di divisori dello zero, che equivale a dire che il prodotto di due numeri naturali è uguale a zero solo se almeno uno dei due fattori è zero.

- - -

Dimostriamo ora la proprietà distributiva della moltiplicazione rispetto all'addizione, ossia che, per ogni $a,b,c\in\mathbb{N},$ vale la seguente relazione:

$$ \tag{14}
a\cdot(b+c)=a\cdot b+a\cdot c
$$

Fissiamo due interi $a$ e $b$ e procediamo per induzione su $c.$ Quando $c=0,$ la somma $b+0$ è uguale a $b$ e il prodotto $a\cdot 0$ è uguale a $0,$ quindi i membri dell'uguaglianza coincidono:

$$
\begin{align}
a\cdot(b+0) &= a\cdot b \\[6pt]
&= a\cdot b+0 \\[6pt]
&= a\cdot b+a\cdot 0
\end{align}
$$

Supponiamo ora che la $(14)$ valga per un numero naturale $c$ qualunque. Dobbiamo dimostrare che $a\cdot(b+S(c))=a\cdot b+a\cdot S(c).$ Per la $(3)$ abbiamo che $b+S(c)=S(b+c).$ Applicando la definizione ricorsiva della moltiplicazione otteniamo:

$$
\begin{align}
a\cdot(b+S(c)) &= a\cdot S(b+c) \\[6pt]
&= a\cdot(b+c)+a
\end{align}
$$

Nell'ultima espressione, l'ipotesi induttiva permette di sostituire $a\cdot(b+c)$ con $a\cdot b+a\cdot c.$ Usiamo poi l'associatività dell'addizione per raggruppare gli ultimi due addendi e otteniamo:

$$
\begin{align}
a\cdot(b+c)+a &= (a\cdot b+a\cdot c)+a \\[6pt]
&= a\cdot b+(a\cdot c+a) \\[6pt]
&= a\cdot b+a\cdot S(c)
\end{align}
$$

La proprietà vale dunque per ogni $c\in\mathbb{N}$ e poiché $a$ e $b$ sono stati scelti arbitrariamente, la distributività è dimostrata per tutti i numeri naturali. Da notare che la commutatività della moltiplicazione permette di ricavare anche la distributività quando al primo fattore ho una somma:

$$
\begin{align}
(a+b)\cdot c &= c\cdot(a+b) \\[6pt]
&= c\cdot a+c\cdot b \\[6pt]
&= a\cdot c+b\cdot c
\end{align}
$$
## Ordine

L'insieme $\mathbb{N}$ possiede un cosiddetto ordine totale, che può essere definito direttamente in termini di addizione. In pratica dati due numeri naturali $m$ e $n,$ la relazione $m \leq n$ vale se e solo se esiste un numero naturale $k$ tale che sia soddisfatta la seguente uguaglianza:

$$
n = m + k \tag{14}
$$

Il numero $k$ esiste esattamente quando $m\leq n$ e indica quante applicazioni del successore occorrono per raggiungere $n$ a partire da $m.$ La totalità dell'ordine significa che, per due numeri naturali qualsiasi $m$ e $n,$ vale almeno una delle relazioni $m\leq n$ oppure $n\leq m.$ L'ordine così definito possiede due ulteriori proprietà: 

+ La tricotomia, che afferma che, per ogni $m, n \in \mathbb{N},$ vale esattamente una delle relazioni $m < n,$ $m = n,$ $n < m$.
+ La discretezza, che afferma che nessun numero naturale è strettamente compreso tra due numeri naturali consecutivi e quindi per ogni $n \in \mathbb{N},$ non esiste dunque alcun $k \in \mathbb{N}$ che soddisfi $n < k < S(n).$

L'ordine che abbiamo fin qui descritto è definito come un buon ordinamento, ossia ogni sottoinsieme non vuoto di $\mathbb{N}$ ha un elemento minimo rispetto alla relazione $\leq.$
