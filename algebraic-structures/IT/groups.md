---
title: Groups
source: https://algebrica.org/groups/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - associativity
  - cayley-table
  - cyclic-subgroup
  - element-order
  - group-theory
  - identity-element
  - inverse-element
  - subgroup
  - symmetric-group
---

## Definizione

Con i gruppi iniziamo lo studio delle strutture algebriche, cioè degli insiemi dotati di una o più operazioni che soddisfano determinate proprietà. Gruppi, anelli e campi sono esempi di strutture algebriche. In breve, i gruppi hanno un'operazione associativa con elemento neutro e inversi, gli anelli sono gruppi additivi commutativi dotati anche di una moltiplicazione associativa e distributiva rispetto all'addizione, e i campi sono anelli in cui gli elementi non nulli formano un gruppo commutativo rispetto alla moltiplicazione. Solo per fare un esempio, l'insieme dei numeri interi, dotato dell'addizione, è un gruppo, mentre, se si considera anche la moltiplicazione, è un anello.

Un gruppo è un insieme $G$ dotato di un'operazione binaria che soddisfa tre assiomi ed è indicata come:

$$\cdot : G \times G \to G \tag{1}$$

Nello specifico, nella $(1)$ il punto $\cdot$ indica l'operazione del gruppo e a ogni coppia ordinata $(a,b) \in G \times G$ l'operazione associa un elemento di $G,$ che possiamo scrivere come $a \cdot b.$ Per esempio, nel gruppo additivo degli interi $a \cdot b$ indica la somma $a+b.$ Vediamo ora i tre assiomi che la $(1)$ deve rispettare, partendo dall'associatività. Per ogni $a, b, c \in G$ deve valere l'identità:

$$(a \cdot b) \cdot c = a \cdot (b \cdot c) \tag{2}$$

Il secondo assioma richiede l'esistenza di un elemento neutro $e \in G$ per il quale, moltiplicando qualunque $a \in G$ per $e$ otteniamo $a$:

$$a \cdot e = e \cdot a = a \tag{3}$$

Il terzo assioma richiede che ogni elemento $a \in G$ ammetta un inverso $a^{-1} \in G$ per cui si ha:

$$a \cdot a^{-1} = a^{-1} \cdot a = e \tag{4}$$

In alcuni testi viene elencato un ulteriore assioma, quello della chiusura, ma di fatto, non è necessario esplicitarla in quanto nella $(1)$ la scelta di $G$ come codominio garantisce già che il prodotto di due elementi di $G$ appartenga ancora a $G.$

Un gruppo $(G, \cdot)$ si dice abeliano, o commutativo, se scambiando l'ordine dei fattori il prodotto rimane lo stesso. Per ogni $a, b \in G$ deve quindi valere la seguente identità:

$$a \cdot b = b \cdot a \tag{5}$$

Nel gruppo simmetrico $S_3$ delle permutazioni di $\{1,2,3\},$ scambiare prima $1$ e $2$ e poi $2$ e $3$ manda $1$ in $3.$ Eseguendo gli stessi scambi in ordine inverso, $1$ viene mandato in $2.$ Le due composizioni sono diverse, quindi $S_3$ non è abeliano.

- - -

Vediamo ora cosa succede nel caso in cui un assioma non è verificato. Prendiamo ad esempio il caso dei numeri reali in cui la moltiplicazione è associativa e ha elemento neutro $1.$ Lo zero è l'unico elemento privo di inverso, perché per ogni $x \in \mathbb{R}$ si ha:

$$0 \cdot x = 0 \neq 1 \tag{6}$$

Dunque $(\mathbb{R}, \cdot)$ non soddisfa l'assioma $(4).$ Escludendo lo zero, ogni elemento $a$ ha inverso $1/a$ e si ottiene il gruppo abeliano $(\mathbb{R} \setminus \{0\}, \cdot).$

## Proprietà

Vediamo ora come si comporta l'elemento neutro la cui esistenza è garantita dalla $(3)$. Per dimostrarne l'unicità, supponiamo che $e$ ed $e'$ siano entrambi elementi neutri e consideriamo il loro prodotto:

$$e = e \cdot e' = e' \tag{7}$$

Nella $(7),$ la prima uguaglianza vale perché $e'$ è neutro a destra, mentre la seconda perché $e$ è neutro a sinistra e dunque $e$ ed $e'$ devono coincidere. Anche l'inverso è unico e per dimostrarlo fissiamo un elemento $a \in G$ e consideriamo $h$ un inverso a sinistra di $a,$ tale che $h \cdot a = e.$ Consideriamo poi $k$ un inverso a destra, per cui si ha che $a \cdot k = e.$ Sostituendo $e$ con $a \cdot k$ nel prodotto $h \cdot e$ e applicando l'associatività $(2)$ otteniamo la seguente uguaglianza:

$$
\begin{align}
h &= h \cdot e \notag \\[6pt]
  &= h \cdot (a \cdot k) \notag \\[6pt]
  &= (h \cdot a) \cdot k \notag \\[6pt]
  &= e \cdot k \notag \\[6pt]
  &= k \tag{8}
\end{align}
$$

La $(8)$ mostra che ogni inverso a sinistra coincide con ogni inverso a destra e poiché $a^{-1}$ soddisfa entrambe le condizioni per la $(4),$ ogni inverso di $a,$ anche solo da un lato, coincide con $a^{-1}.$

Fissiamo ora un elemento $a \in G.$ Se conosciamo il prodotto $a \cdot x,$ come possiamo ritrovare $x$? E se il prodotto è invece $x \cdot a$? Al variare di $x$ in $G,$ questi due prodotti definiscono due applicazioni da $G$ su di sé, la moltiplicazione a sinistra per $a$ e la moltiplicazione a destra per $a,$ per cui possiamo scrivere:

$$
\begin{align}
L_a(x) &= a \cdot x \notag \\[6pt]
R_a(x) &= x \cdot a \tag{9}
\end{align}
$$

Nel primo caso della $(9)$, per ritrovare $x$ moltiplichiamo $a \cdot x$ a sinistra per $a^{-1}$ che equivale ad applicare prima $L_a$ e poi $L_{a^{-1}}.$ Per la proprietà associativa possiamo raggruppare i primi due fattori e riscrivere il tutto come:

$$
\begin{align}
L_{a^{-1}}(L_a(x)) &= a^{-1} \cdot (a \cdot x) \notag \\[6pt]
                   &= (a^{-1} \cdot a) \cdot x \notag \\[6pt]
                   &= e \cdot x \notag \\[6pt]
                   &= x \tag{10}
\end{align}
$$

La $(10)$ mostra che moltiplicando a sinistra per $a^{-1}$ si recupera $x$ dal prodotto $a \cdot x.$ Anche nell'ordine opposto si ritrova $x,$ perché $a \cdot a^{-1} = e.$ Lo stesso ragionamento vale per la moltiplicazione a destra. Le due applicazioni della $(9)$ sono dunque biiettive e le loro inverse sono:

$$
\begin{align}
L_a^{-1} &= L_{a^{-1}} \notag \\[6pt]
R_a^{-1} &= R_{a^{-1}} \tag{11}
\end{align}
$$

Per l'iniettività di $L_a$ e $R_a$ si può cancellare un fattore comune quando compare dallo stesso lato in entrambi i membri. Per ogni $a, b, c \in G$ valgono quindi le leggi di cancellazione a sinistra e a destra:

$$
\begin{align}
a \cdot b = a \cdot c &\implies b = c \notag \\[6pt]
b \cdot a = c \cdot a &\implies b = c \tag{12}
\end{align}
$$

Le inverse nella $(11)$ permettono anche di risolvere le equazioni di gruppo, per cui per ogni $a, b \in G$ si ottiene un'unica soluzione moltiplicando entrambi i membri per $a^{-1}$ dal lato in cui compare $a$:

$$
\begin{align}
a \cdot x = b &\iff x = a^{-1} \cdot b \notag \\[6pt]
x \cdot a = b &\iff x = b \cdot a^{-1} \tag{13}
\end{align}
$$

L'ordine di un gruppo $G$ è la sua cardinalità e si indica con $|G|.$ Il gruppo si dice finito se ha un numero finito di elementi, infinito altrimenti.

Quando $G$ è finito, l'unicità delle soluzioni nella $(13)$ si può leggere nella tavola di Cayley del gruppo. Per costruirla, si usano gli elementi di $G$ come intestazioni sia delle righe sia delle colonne. All'incrocio tra la riga $a$ e la colonna $x$ si scrive il prodotto $a \cdot x.$ La riga $a$ elenca quindi i valori di $L_a,$ mentre la colonna $a$ elenca quelli di $R_a.$ Per fare un esempio, nel gruppo $\mathbb{Z}/3\mathbb{Z}$ l'operazione è l'addizione modulo $3.$ Per mostrarlo, indichiamo le tre classi di resto con $0, 1, 2$ e in ogni cella scriviamo il resto della divisione per $3$ della somma delle due intestazioni, ottenendo

$$
\begin{array}{c|ccc}
+ & 0 & 1 & 2 \\ \hline
0 & 0 & 1 & 2 \\
1 & 1 & 2 & 0 \\
2 & 2 & 0 & 1
\end{array}
\tag{14}
$$

Nella $(14)$ la riga $2$ contiene $0$ nella colonna $1,$ perché $2+1 \equiv 0 \pmod{3}.$ Leggendo la stessa riga si vede che $x=1$ è l'unica soluzione di $2+x=0$ nel gruppo.

Cercare un elemento $b$ nella riga $a$ equivale a risolvere l'equazione $a \cdot x = b,$ dove $x$ indica la colonna cercata. Cercare lo stesso elemento nella colonna $a$ equivale a risolvere $x \cdot a = b,$ dove in questo caso $x$ indica la riga. Per la $(13)$ ciascuna equazione ha un'unica soluzione, quindi ogni elemento di $G$ compare esattamente una volta in ogni riga e in ogni colonna.

- - -

Nella tavola di Cayley possiamo anche trovare l'inverso di un elemento $g$ e infatti se cerchiamo $e$ nella riga $g$ l'intestazione della colonna in cui compare è l'unico elemento $x$ per cui $g \cdot x = e,$ e dunque è $g^{-1}.$ Quando $g = a \cdot b,$ possiamo risolvere la stessa equazione in qualunque gruppo, usando  l'associatività per raggruppare $b$ e $x,$ poi moltiplicando entrambi i membri a sinistra prima per $a^{-1}$ e infine per $b^{-1}$:

$$
\begin{align}
(a \cdot b) \cdot x &= e \notag \\[6pt]
a \cdot (b \cdot x) &= e \notag \\[6pt]
b \cdot x &= a^{-1} \notag \\[6pt]
x &= b^{-1} \cdot a^{-1} \tag{15}
\end{align}
$$

Dalla $(15)$ per l'unicità dell'inverso dimostrata nella $(8)$ otteniamo la formula per l'inverso del prodotto:

$$(a \cdot b)^{-1} = b^{-1} \cdot a^{-1} \tag{16}$$

Dalla $(4)$ segue anche che $a$ è l'inverso di $a^{-1},$ poiché il loro prodotto in entrambi gli ordini dà $e$ e quindi si ha che $(a^{-1})^{-1} = a.$

## Potenze di un elemento

Quando tutti i fattori di un prodotto sono uguali a uno stesso elemento $a \in G,$ la proprietà associativa della $(2)$ permette di raggrupparli senza cambiare il risultato. In termini formali, per ogni intero $n \geq 1$ indichiamo con $a^n$ il prodotto di $n$ fattori dati da $a$:

$$a^n = \underbrace{a \cdot a \cdots a}_{n \text{ fattori}} \tag{17}$$

Valgono inoltre le seguenti proprietà:

$$
\begin{align}
a^0 &= e \notag \\[6pt]
a^{-n} &= (a^{-1})^n \qquad (n \geq 1) \tag{18}
\end{align}
$$

Per $m$ e $n$ positivi, il prodotto di $a^m$ e $a^n$ contiene $m+n$ fattori uguali ad $a,$ mentre $(a^m)^n$ contiene $n$ gruppi di $m$ fattori ciascuno. Con le definizioni della $(18)$ le due leggi valgono per tutti gli interi $m$ e $n$:

$$
\begin{align}
a^m \cdot a^n &= a^{m+n} \notag \\[6pt]
(a^m)^n &= a^{mn} \tag{19}
\end{align}
$$

Le due identità della $(19)$ sono le regole del prodotto di potenze con la stessa base e della potenza di una potenza, già viste per i numeri reali nella voce sulle potenze e per gli esponenti interi valgono anche nei gruppi non abeliani.

Quando l'operazione del gruppo si scrive come addizione, al posto di $a^n$ si scrive $na.$ Per $n$ positivo, $na$ è la somma di $n$ copie di $a.$ Per la potenza di un prodotto conta anche l'ordine dei fattori. Se $a$ e $b$ commutano, nel prodotto $(a \cdot b)^2 = a \cdot b \cdot a \cdot b$ possiamo scambiare i due fattori centrali e ottenere $a^2 \cdot b^2.$ Lo stesso riordinamento vale per ogni esponente positivo e, passando agli inversi, anche per gli esponenti negativi. Perciò, se $a \cdot b = b \cdot a,$ per ogni intero $n$ vale l'identità:

$$(a \cdot b)^n = a^n \cdot b^n \tag{20}$$

## Ordine di un elemento

Abbiamo visto che per la $(18)$ vale $a^0=e$ per ogni elemento $a \in G.$ Se partiamo da $e$ e moltiplichiamo ogni volta per $a,$ dopo quanti passi ritroviamo $e$? Quando questo accade, il numero di passi necessari per ritrovare $e$ si chiama ordine di $a$ e si indica con $\mathrm{ord}(a)$ e si scrive come:

$$\mathrm{ord}(a) = \min\{n \in \mathbb{Z} : n \gt 0,\ a^n = e\} \tag{21}$$

Se nessuna potenza con esponente positivo è uguale a $e,$ si dice che $a$ ha ordine infinito e si scrive $\mathrm{ord}(a)=\infty.$ In un gruppo additivo, cercare il primo ritorno all'elemento neutro equivale a cercare il più piccolo intero positivo $n$ per cui $na=0.$ Per esempio, riprendendo l'esempio $(\mathbb{Z}/6\mathbb{Z},+)$ partiamo da $0$ e aggiungiamo ogni volta $2,$ calcolando la somma modulo $6$ ottenendo:

$$0 \xrightarrow{+2} 2 \xrightarrow{+2} 4 \xrightarrow{+2} 0 \tag{22}$$

Nella $(22)$ ritroviamo lo zero alla terza addizione, quindi $2$ ha ordine $3.$ Se aggiungiamo ogni volta $1,$ occorrono invece sei addizioni e l'ordine di $1$ è $6.$ In $(\mathbb{Z},+)$ ogni intero non nullo ha ordine infinito, poiché nessuno dei suoi multipli con coefficiente positivo è zero. L'ordine di $a$ determina anche quante potenze distinte di $a$ esistono. Per dimostrarlo, supponiamo che $\mathrm{ord}(a)=n.$ Le prime $n$ potenze, da $a^0$ ad $a^{n-1},$ sono tutte distinte e infatti, se $a^i=a^j$ per due esponenti $0 \leq i \lt j \lt n,$ moltiplicando per $a^{-i}$ si otterrebbe $a^{j-i}=e.$ Poiché $0 \lt j-i \lt n,$ questo contraddirebbe la scelta di $n$ nella $(21).$

Per concludere che le potenze distinte sono esattamente $n,$ resta da mostrare che ogni potenza $a^k$ coincide con una di quelle già elencate. Poiché $a^n=e,$ aumentare l'esponente di $n$ lascia invariata la potenza. Dividendo $k$ per $n,$ possiamo ricondurci a un esponente compreso tra $0$ e $n-1.$ Scrivendo $k=qn+r,$ con $0 \leq r \lt n,$ dalla $(19)$ otteniamo:

$$a^k = (a^n)^q \cdot a^r = e^q \cdot a^r = a^r \tag{23}$$

La $(23)$ mostra che il resto $r$ determina la potenza. Poiché a resti diversi corrispondono potenze diverse, $a^k=a^\ell$ se e solo se $k \equiv \ell \pmod{n}.$ Per le formule $(18)$ e $(19),$ moltiplicando due potenze intere di $a$ o prendendo l'inverso di una di esse si ottiene ancora una potenza di $a.$ Queste potenze formano dunque un gruppo con la stessa operazione di $G.$ Si chiama sottogruppo ciclico generato da $a$ e si indica con $\langle a \rangle.$ Nel caso finito abbiamo dunque:

$$
\begin{align}
\langle a \rangle &= \{a^r : 0 \leq r \lt n,\ r \in \mathbb{Z}\} \notag \\[6pt]
|\langle a \rangle| &= n = \mathrm{ord}(a) \tag{24}
\end{align}
$$

Se $a$ ha ordine infinito, due esponenti distinti $i \lt j$ non possono dare la stessa potenza, perché si avrebbe di nuovo $a^{j-i}=e$ con $j-i$ positivo e in questo caso anche $\langle a \rangle$ è infinito.