---
title: Modulo Operator
source: https://algebrica.org/modulo-operator/
license: CC BY-NC 4.0
tags:
  - bezout-identity
  - cancellation-law
  - cayley-table
  - congruence
  - division-algorithm
  - equivalence-relation
  - euclidean-algorithm
  - eulers-theorem
  - eulers-totient
  - fermat-little-theorem
  - linear-congruence
  - modular-arithmetic
  - modulo-operator
  - multiplicative-inverse
  - remainder
  - residue-class
  - ring-z-nz
  - zero-divisor
---
## Definizione

L'operatore modulo restituisce il resto della divisione euclidea ed è utile quando un certo conteggio si ripete a intervalli regolari e vogliamo sapere a che punto del ciclo ci troviamo. A livello intuitivo, se oggi è lunedì e vogliamo sapere che giorno sarà tra $17$ giorni, calcoliamo $14$ giorni (due settimane) più 3 giorni rimanenti, e sarà giovedì. A livello formale, dati due interi $a$ e $n$ con $n>0$  l'operatore modulo è definito come:

$$
a \bmod n = r \tag{1}
$$

Per esempio, $17\bmod5=2,$ poiché $17=3\cdot5+2.$ Nella formula $(1),$ $n$ è il modulo, $r$ è il resto della divisione euclidea di $a$ per $n$ ed è l'unico intero compreso tra $0$ e $n-1$ per cui vale la seguente uguaglianza:

$$
a = qn + r \tag{2}
$$

Il numero intero $q$ è il quoziente della divisione. Per il teorema della divisione euclidea l'uguaglianza $(2)$ determina un'unica coppia di interi $(q,r)$ con $0\leq r<n.$ Quando $a$ è negativo, il resto è ancora l'unico intero nell'intervallo $0\leq r<n$ che soddisfa la definizione $(1).$ Ad esempio, per  $-7\bmod5,$ l'equazione $-7=q\cdot5+r$ dà $q=-2$ e $r=3,$ poiché $-7=(-2)\cdot5+3.$ Pertanto $-7\bmod5=3.$



## Congruenza

Due interi $a$ e $b$ si dicono congruenti modulo $n$ se hanno lo stesso resto nella divisione per $n$ oppure, in modo equivalente, se la loro differenza è un multiplo di $n.$ Questa relazione si scrive nel seguente modo:

$$ \tag{3}
a \equiv b \pmod{n}
$$

Se $a$ e $b$ hanno lo stesso resto $r,$ possiamo scrivere $a=q_an+r$ e $b=q_bn+r$ e se li sottriamo otteniamo:

$$a-b=(q_a-q_b)n \tag{4}$$

Invece, se $a-b=kn$ per un intero $k$ e $b=q_bn+r,$ allora $a=(q_b+k)n+r.$ Il quoziente cambia di $k$ e il resto rimane $r.$ La formula $(5)$ esprime quindi l'equivalenza tra la congruenza di $a$ e $b$ modulo $n$ e la divisibilità di $a-b$ per $n:$

$$
a\equiv b\pmod n \quad\Longleftrightarrow\quad n\mid(a-b) \tag{5}
$$

I due interi hanno lo stesso resto, quindi sono congruenti modulo $5$ e possiamo scrivere la $(3)$ come $17\equiv2\pmod5.$ È utile evidenziare che la congruenza modulo $n$ è una relazione di equivalenza sugli interi con le seguenti caratteristiche:

+ È riflessiva, perché $a\equiv a\pmod n$ per ogni intero $a.$
+ È simmetrica, perché $a\equiv b\pmod n$ implica $b\equiv a\pmod n.$
+ È transitiva, perché $a\equiv b\pmod n$ e $b\equiv c\pmod n$ implicano $a\equiv c\pmod n.$

Inoltre, la congruenza gode di una serie di proprietà algebriche elencate di seguito. Per prima, la congruenza modulo $n$ si conserva rispetto all'addizione, alla sottrazione e alla moltiplicazione, quindi se abbiamo $a\equiv b\pmod n$ e $c\equiv d\pmod n,$ valgono le seguenti relazioni:

$$
\begin{aligned}
a + c &\equiv b + d \pmod n \\[6pt]
a - c &\equiv b - d \pmod n \\[6pt]
a \cdot c &\equiv b \cdot d \pmod n
\end{aligned} \tag{6}
$$

Dalle ipotesi $a\equiv b\pmod n$ e $c\equiv d\pmod n$ sappiamo che $a-b$ e $c-d$ sono multipli di $n.$ Per dimostrare che le somme $a+c$ e $b+d$ sono congruenti modulo $n,$ dobbiamo verificare che anche la loro differenza è un multiplo di $n.$

$$ \tag{7}
(a + c) - (b + d) = (a - b) + (c - d)
$$

Poiché la differenza del secondo membro della $(7)$ è la somma di due multipli di $n,$ è a sua volta un multiplo di $n.$ Ne segue che $a+c\equiv b+d\pmod n.$ Lo stesso criterio vale per la sottrazione dove abbiamo:
$$(a-c)-(b-d)=(a-b)-(c-d)\tag{8}$$

Per il prodotto, invece, vale la seguente identità:

$$ \tag{9}
ac-bd=(a-b)c+b(c-d)
$$

Anche qui entrambi gli addendi sono multipli di $n,$ quindi $ac\equiv bd\pmod n.$ Per induzione, la compatibilità con il prodotto vale anche per le potenze. Se $a\equiv b\pmod n,$ allora per ogni intero $k \gt 0$ vale:

$$a^k\equiv b^k\pmod n \tag{10}$$

Per le proprietà $(6)$ e $(10),$ possiamo ridurre modulo $n$ i risultati intermedi di somme, differenze, prodotti e potenze senza cambiare il resto finale. Per esempio, per calcolare il resto di $17\cdot8$ nella divisione per $5,$ possiamo sostituire ciascun fattore con il suo resto nella divisione per $5.$ Il resto di $17$ è $2$ e quello di $8$ è $3.$ Il prodotto dei resti è $2\cdot3=6.$ Dividendo $6$ per $5$ si ottiene resto $1,$ perché $6=1\cdot5+1$ e quindi per la proprietà $(6),$ anche il prodotto originale $17\cdot8$ ha resto $1$ nella divisione per $5.$

La proprietà $(6)$ permette di moltiplicare entrambi i membri di una congruenza per lo stesso intero $c.$ Per capire quando possiamo cancellare quel fattore, usiamo la $(5).$ Se $ac\equiv bc\pmod n,$ allora $n$ divide $c(a-b).$ Posto $g=\gcd(c,n),$ gli interi $c/g$ e $n/g$ sono coprimi. Poiché $n/g$ divide $(c/g)(a-b),$ deve dividere anche $a-b.$ Applicando di nuovo la $(5),$ otteniamo la seguente congruenza.

$$
a\equiv b\pmod{n/g} \tag{11}
$$

Quindi se $c$ è coprimo con $n,$ allora $g=1$ e la $(11)$ conserva il modulo $n.$
## Tabelle dell'addizione e della moltiplicazione

Le tabelle seguenti permettono di mostrare visivamente qual è il resto di una somma o di un prodotto modulo $n.$ La costruzione è molto semplice. Le righe e le colonne sono numerate da $0$ a $n-1$ mentre nelle caselle scriviamo il resto della divisione del risultato della somma o del prodotto per $n.$ Ad esempio, quella che segue è la tabella dell'addizione modulo $4.$ La somma $2+3$ è pari a $5$ e quindi nella cella corrispondente scriviamo il resto che è pari a $1$:

| +   | 0   | 1   | 2   | 3   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 1   | 2   | 3   |
| 1   | 1   | 2   | 3   | 0   |
| 2   | 2   | 3   | 0   | 1   |
| 3   | 3   | 0   | 1   | 2   |

Come potete notare, ogni riga è uno spostamento ciclico della precedente, perché aggiungere un resto fissato permuta gli elementi di $\mathbb{Z}/4\mathbb{Z}.$ Usando lo stesso esempio, costruiamo ora la tabella della moltiplicazione modulo $4.$ Anche in questo caso moltiplicando $3 \cdot 3$ otteniamo $9$ che in modulo $4$ è pari a $(1):$

| × | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 2 | 3 |
| 2 | 0 | 2 | 0 | 2 |
| 3 | 0 | 3 | 2 | 1 |

Notate che nella riga relativa al $2$ non è contenuto alcun $1,$ il che significa che $2$ non ha inverso moltiplicativo modulo $4,$ in accordo al fatto che $\gcd(2,4)=2\neq1.$ Le righe di $1$ e $3$ invece contengono $1,$ e quindi questi due resti, entrambi coprimi con $4,$ sono invertibili.

> La tabella dell'addizione modulo $n$ è la tavola di Cayley del gruppo ciclico $(\mathbb{Z}/n\mathbb{Z},+).$ > Una tavola di Cayley mostra il risultato dell'operazione per ogni coppia di elementi di un gruppo finito. Per ottenere la tavola di Cayley del gruppo moltiplicativo, si conservano solo le righe e le colonne dei resti invertibili. Per il modulo $4,$ per esempio, questi resti sono $1$ e $3.$

## Classi di resto

Se fissiamo un modulo $n$ e raggruppiamo gli interi che danno lo stesso resto nella divisione per $n$ otteniamo per ciascun gruppo una cosiddetta classe di resto, detta anche classe di equivalenza modulo $n.$ Una generica classe $[a]_n$ contiene tutti gli interi congruenti ad $a$ e per la $(5)$ questi interi si ottengono aggiungendo ad $a$ un multiplo di $n$ secondo la seguente relazione:

$$
[a]_n = \{ a + kn \mid k \in \mathbb{Z} \} \tag{12}
$$

Le classi di dicono disgiunte quando i resti sono diversi. Quando i resti sono diversi, le classi sono disgiunte, perché ogni intero ha un solo resto nella divisione per $n.$ Se un intero $c$ appartiene sia a $[a]_n$ sia a $[b]_n,$ il suo resto nella divisione per $n$ è lo stesso di $a$ e di $b.$ Le due classi contengono quindi tutti gli interi con lo stesso resto e coincidono.

Come sappiamo, nel calcolo del modulo $n$, i resti possibili sono $0,1,\ldots,n-1$ e ciascuno di tali interi rappresenta la propria classe. Quindi le classi di resto sono $[0]_n,[1]_n,\ldots,[n-1]_n$ e il loro insieme si indica con $\mathbb{Z}/n\mathbb{Z}.$ Consideriamo ad esempio il caso con $n=4$ dove gli interi si ripartiscono nelle seguenti classi di resto:

$$
\begin{align}
[0]_4 &= \{ \ldots, -8, -4, 0, 4, 8, \ldots \} \\[6pt]
[1]_4 &= \{ \ldots, -7, -3, 1, 5, 9, \ldots \} \\[6pt]
[2]_4 &= \{ \ldots, -6, -2, 2, 6, 10, \ldots \} \\[6pt]
[3]_4 &= \{ \ldots, -5, -1, 3, 7, 11, \ldots \}
\end{align}
$$

## Congruenze lineari e inversi

Consideriamo tre interi $a,$ $b$ e $n$  con $n>0$ e $x$ e definiamo una congruenza lineare nel seguente modo:

$$ax\equiv b\pmod n \tag{13}$$

Le soluzioni della $(13)$ sono gli interi $x$ che soddisfano la relazione, raggruppati in classi di resto modulo $n.$ La $(13)$ ha soluzione se e solo se $\gcd(a,n)$ divide $b$ e in tal caso le soluzioni formano una classe modulo $n/\gcd(a,n),$ che corrisponde a $\gcd(a,n)$ classi distinte modulo $n.$ 

Per giustificare il criterio di esistenza delle soluzioni della $(13),$ poniamo $g=\gcd(a,n).$ Per la $(5),$ se $x$ è una soluzione, allora $ax-b$ è un multiplo di $n.$ Poiché $g$ divide sia $a$ sia $n,$ deve dividere anche $b.$ Per il verso opposto usiamo l'identità di Bézout, secondo cui esistono interi $u$ e $v$ tali che valga l'uguaglianza seguente:

$$
au + nv = g \tag{14}
$$

Se $g$ divide $b,$ scriviamo $b=kg$ con $k$ intero. Moltiplicando la $(14)$ per $k$ si ottiene $b-a(ku)=n(kv).$ La differenza è un multiplo di $n,$ quindi, per la $(5),$ $x=ku$ risolve la $(13).$

- - -
- 
Per $b=1,$ una soluzione della $(13)$ è un inverso di $a$ modulo $n$ ed esiste se e solo se $g=1.$ In questo caso l'algoritmo euclideo esteso calcola i coefficienti della $(14).$ Poiché $nv$ è un multiplo di $n,$ dalla $(14)$ segue $au\equiv1\pmod n.$ Per un termine noto $b$ qualsiasi, moltiplicando la $(13)$ per $u$ si ottiene l'unica classe di soluzioni $x\equiv ub\pmod n.$ 

Per esempio, $7$ è il proprio inverso modulo $12,$ perché $7\cdot7=4\cdot12+1.$ Dunque $7x\equiv5\pmod{12}$ equivale a $x\equiv7\cdot5\equiv11\pmod{12}.$

Se $g>1$ e divide $b,$ la $(13)$ equivale alla congruenza ottenuta dividendo per $g$ il coefficiente di $x,$ il termine noto e il modulo.

$$
\frac{a}{g}x \equiv \frac{b}{g} \pmod{n/g} \tag{15}
$$

Poiché $a/g$ e $n/g$ sono coprimi, la $(15)$ ha una sola classe di soluzioni modulo $n/g,$ che corrisponde a $g$ classi modulo $n.$ Per esempio, $6x\equiv9\pmod{15}$ si riduce a $2x\equiv3\pmod5.$ Moltiplicando per $3,$ l'inverso di $2$ modulo $5,$ otteniamo $x\equiv4\pmod5.$ I resti modulo $15$ che danno resto $4$ nella divisione per $5$ sono $4,$ $9$ e $14.$

I sistemi con più moduli sono trattati nella voce sul teorema cinese del resto.

## Piccolo teorema di Fermat e teorema di Eulero

Il piccolo teorema di Fermat e il teorema di Eulero permettono di calcolare il resto di una potenza con un esponente grande usando una potenza con esponente più piccolo. L'idea consiste nel trovare un esponente $m$ per cui $a^m$ dà resto $1$ modulo $n.$ Se scriviamo l'esponente $k$ come $k=qm+r$ con $0\leq r<m,$ allora $a^k=(a^m)^qa^r$ ha lo stesso resto di $a^r.$ Se il modulo $p$ è primo e $a$ non è divisibile per $p,$ il piccolo teorema di Fermat permette di scegliere $m=p-1$ per cui vale:

$$
a^{p-1} \equiv 1 \pmod p \tag{16}
$$

Una forma equivalente del teorema, valida per ogni intero $a,$ è $a^p\equiv a\pmod p.$ Per esempio, per calcolare il resto di $3^{100}$ nella divisione per $7,$ usiamo la $(16)$ con $p=7.$ Poiché $3^6\equiv1\pmod7$ e $100=16\cdot6+4,$ basta calcolare il resto di $3^4=81$ nella divisione per $7$ che è pari a $4.$

Per un modulo qualsiasi $n>1,$ il teorema di Eulero permette di scegliere $m=\varphi(n)$ quando $a$ e $n$ sono coprimi e dove $\varphi(n)$ conta gli interi da $1$ a $n$ coprimi con $n.$ Sotto questa ipotesi vale la congruenza seguente:

$$
a^{\varphi(n)} \equiv 1 \pmod n \tag{17}
$$

Se $n=p$ è primo, tutti gli interi da $1$ a $p-1$ sono coprimi con $p.$ Quindi $\varphi(p)=p-1$ e la $(17)$ coincide con la $(16).$

## Legame con le strutture algebriche

Dalle proprietà della congruenza viste nella $(6)$ possiamo passare dalle operazioni sugli interi a quelle sulle classi di resto. Vediamo come l'addizione e la moltiplicazione così definite danno a $\mathbb{Z}/n\mathbb{Z}$ la struttura di un anello. Per sommare o moltiplicare due classi, scegliamo un rappresentante per ciascuna, eseguiamo l'operazione sugli interi e prendiamo la classe del risultato:

$$
\begin{aligned}
[a]_n + [b]_n &= [a+b]_n \\[6pt]
[a]_n[b]_n &= [ab]_n
\end{aligned} \tag{18}
$$

Il risultato della $(18)$ è indipendente dalla scelta dei suoi elementi, infatti, se scegliamo $a'$ nella classe di $a$ e $b'$ nella classe di $b,$ la $(6)$ garantisce che $a+b$ e $a'+b'$ appartengono alla stessa classe. Lo stesso vale per $ab$ e $a'b'.$ Questa indipendenza dipende dal modo in cui abbiamo raggruppato gli interi. Se li raggruppassimo per numero di cifre del valore assoluto, $3,$ $4,$ $6$ e $7$ starebbero tutti nella stessa classe. Eppure $3+4=7$ ha una cifra, mentre $6+7=13$ ne ha due. La classe della somma dipenderebbe quindi dagli elementi scelti.

Le operazioni della $(18)$ ereditano le proprietà dell'addizione e della moltiplicazione degli interi. Per esempio, l'associatività del prodotto si ottiene passando da $(ab)c$ ad $a(bc)$ dentro la classe di resto e vale:

$$
\begin{aligned}
([a]_n[b]_n)[c]_n &= [(ab)c]_n \\[6pt]
&= [a(bc)]_n = [a]_n([b]_n[c]_n)
\end{aligned} \tag{19}
$$

Entrambe le operazioni di somma e prodotto sono associative e commutative, e il prodotto è distributivo rispetto alla somma. L'elemento neutro della somma e dato dalla classe $[0]_n$ mentre $[-a]_n$ è l'opposto di $[a]_n$ e $[1]_n$ è l'elemento neutro del prodotto. Con queste operazioni possiamo definire $\mathbb{Z}/n\mathbb{Z}$ come un anello commutativo finito.

Una classe non nulla $[a]_n$ si chiama divisore dello zero se esiste una classe non nulla $[b]_n$ tale che $[a]_n[b]_n=[0]_n.$

Il criterio per risolvere la $(13)$ con $b=1$ dice che $[a]_n$ è invertibile se e solo se $\gcd(a,n)=1.$ Se $[a]_n$ è invertibile e $[a]_n[b]_n=[0]_n,$ moltiplicando per l'inverso di $[a]_n$ otteniamo $[b]_n=[0]_n.$ Se invece $[a]_n$ è non nulla e $g=\gcd(a,n)>1,$ la classe $[n/g]_n$ è non nulla e il prodotto è zero, perché $a(n/g)=(a/g)n$ e quindi possiamo scrivere:

$$
[a]_n[n/g]_n=[0]_n \tag{20}
$$

Ogni classe non nulla è quindi invertibile oppure è un divisore dello zero. Modulo $12,$ le classi invertibili sono quelle di $1,$ $5,$ $7$ e $11,$ i soli resti coprimi con $12.$ Per esempio, la classe di $8$ è un divisore dello zero. Poiché $\gcd(8,12)=4,$ la $(20)$ dà $[8]_{12}[3]_{12}=[0]_{12}.$

Quando $n$ è un numero primo, ogni resto non nullo è coprimo con $n.$ Tutte le classi non nulle sono quindi invertibili e $\mathbb{Z}/n\mathbb{Z}$ è perciò un campo.

Come per gli interi, anche per i polinomi a coefficienti in un campo possiamo formare un anello di classi di resto. Fissato ad esempio un polinomio non costante, raggruppiamo i polinomi che hanno lo stesso resto nella divisione per quel polinomio. Per esempio, nel quoziente $\mathbb{R}[x]/(x^2+1)$ ogni classe è rappresentata da un polinomio $a+bx,$ e la classe di $x$ ha quadrato uguale alla classe di $-1.$ Associando la classe di $a+bx$ al numero $a+bi$ si ottiene un isomorfismo con $\mathbb{C}.$
