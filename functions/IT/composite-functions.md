---
title: Funzioni Composte
source: https://algebrica.org/composite-functions/
license: CC BY-NC 4.0
tags:
  - domain
  - function-composition
  - functions
  - identity-function
  - inverse-function
---

## Definizione di composizione

Quando si parla di composizione di funzioni, si intende un'operazione che applica in successione due o più funzioni utilizzando il risultato di ciascuna come argomento della successiva. In termini formali, quindi, date due generiche funzioni $f$ e $g,$ la loro composizione è la funzione ottenuta applicando prima $f$ e poi $g$ al risultato di $f,$ e si indica con la seguente relazione:

$$
(g \circ f)(x) = g(f(x)) \tag{1}
$$

A livello analitico, l'ordine di applicazione della $(1)$ procede da destra verso sinistra. Per rendere più chiara l'operazione, possiamo descrivere la composizione con il seguente diagramma, considerando le funzioni $f : A \rightarrow B$ e $g : B \rightarrow C.$

![IMG.1](../svg/composite-functions-1.svg)

Come primo passo, un generico argomento $x$ in $A$ viene associato da $f$ al valore $f(x)$ in $B,$ quindi da $g$ al valore $g(f(x))$ in $C.$ La freccia esterna corrisponde proprio alla composizione identificata dalla $(1).$ Poiché $f(x) \in B$ per ogni $x \in A$ e $B$ è il dominio di $g,$ il valore $g(f(x))$ sarà definito per ogni $x \in A.$ Pertanto $g \circ f$ è una funzione da $A$ a $C$ definita dalla seguente legge di corrispondenza:

$$
\begin{align}
&g \circ f \colon A \rightarrow C \\[6pt]
&x \mapsto g(f(x))
\end{align}
$$

Una considerazione va fatta sul dominio della funzione composta. Affinché il dominio della $(1)$ sia definito devono valere due condizioni:

+ Il punto $x$ deve appartenere al dominio di $f.$
+ Il valore $f(x)$ deve appartenere al dominio di $g.$

Il dominio della funzione composta è quindi l'insieme dei punti che soddisfano entrambe le condizioni:

$$
\mathrm{dom}(g \circ f) = \{\ x \in \mathrm{dom}(f) \mid f(x) \in \mathrm{dom}(g)\ \}
$$

La seconda condizione distingue la composizione dalle altre operazioni tipiche che intervengono tra funzioni. Ad esempio la somma e il prodotto di due funzioni sono definiti sull'intersezione dei rispettivi domini e lo stesso vale per il quoziente dopo aver escluso gli zeri del denominatore. In una composizione, quindi, ogni condizione sull'argomento di $g$ diventa una condizione su $f(x).$ Perciò, per determinare il dominio della funzione composta si procede in tre passaggi:

+ Come prima cosa si determina $\mathrm{dom}(f),$ considerando la funzione interna della $(1).$
+ Si scrivono poi le condizioni che definiscono $\mathrm{dom}(g)$ e, in ciascuna di esse, si sostituisce la variabile di $g$ con l'espressione $f(x).$
+ Infine, si risolvono queste condizioni e si interseca l'insieme delle loro soluzioni con $\mathrm{dom}(f).$

Attenzione però al fatto che semplificare subito l'espressione $g(f(x))$ prima di determinare il dominio della funzione composta può condurre a un risultato errato. Consideriamo ad esempio la seguente composizione tra $f$ e $g$:

$$
\begin{align}
f(x) &= x - 3 \\[6pt]
g(x) &= \sqrt{x}
\end{align}
$$

La prima è una funzione polinomiale, che sappiamo essere definita su tutto $\mathbb{R},$ mentre la seconda è una radice di indice pari, definita quando l'argomento non è negativo. Possiamo quindi scrivere:

$$ \tag{2}
\begin{align}
\mathrm{dom}(f) &= \mathbb{R} \\[6pt]
\mathrm{dom}(g) &= [0, +\infty)
\end{align}
$$

Sostituendo $x - 3$ nell'espressione di $g,$ otteniamo:

$$
(g \circ f)(x) = g(x - 3) = \sqrt{x - 3} \tag{3}
$$

Nella $(2)$ quindi abbiamo una restrizione del dominio data dalla seconda relazione per cui il dominio di $g \circ f$ è l'intervallo $[3, +\infty),$ un sottoinsieme proprio del dominio della funzione $f.$

[shortcode="intervals"]

|     | $-\infty$ | $0$      | $3$        |     |
| :-- | --------- | -------- | ---------- | --- |
|     | sign+l    |          |            |     |
|     |           | sign+l-c |            |     |
|     |           |          | sign+l-c   |     |
|     |           |          | sign+l-c-h |     |
[/shortcode]

L'ordine inverso di composizione non è detto che mantenga lo stesso dominio della $(3).$ Immaginiamo infatti di avere:

$$
(f \circ g)(x) = f(\sqrt{x}) = \sqrt{x} - 3
$$

In questo ordine di composizione, la funzione interna è $g,$ quindi l'argomento $x$ deve appartenere al suo dominio $[0, +\infty).$ La funzione esterna $f$ è invece definita su tutto $\mathbb{R},$ perciò può essere applicata a ogni valore $\sqrt{x}$ ottenuto senza imporre ulteriori restrizioni. Riportando prima il dominio della funzione interna e poi quello della funzione esterna, abbiamo:

$$
\begin{align}
\mathrm{dom}(g) &= [0, +\infty) \\[6pt]
\mathrm{dom}(f) &= \mathbb{R}
\end{align}
$$

Il dominio di $f \circ g$ è quindi l'intervallo $[0, +\infty),$ che coincide con il dominio della funzione interna $g.$

Questo mostra come la composizione non sia un'operazione commutativa.

- - -

Facciamo un ulteriore esempio considerando le funzioni:

$$ \tag{4}
\begin{align}
f(x) &= \frac{x + 1}{x - 2} \\[6pt]
g(x) &= \ln x
\end{align}
$$

La $f$ è una funzione razionale definita per $x \neq 2,$ mentre nella $g$ il logaritmo è definito per argomenti strettamente positivi. Applicando la $(1)$ otteniamo il risultato della composizione dato da:

$$
(g \circ f)(x) = \ln \frac{x + 1}{x - 2}
$$

Come abbiamo visto sopra, la condizione sul dominio della funzione esterna deve essere applicata anche al quoziente, che deve essere strettamente positivo:

$$
\frac{x + 1}{x - 2} > 0
$$

Il numeratore si annulla in $x = -1$ mentre il denominatore in $x = 2.$ Dallo studio del segno otteniamo:

[class="table-sign"]

|                             |                  |       $-1$       |       $2$        |
| :-------------------------: | :--------------: | :--------------: | :--------------: |
|        $$x + 1 > 0$$        | $-$ | $+$ | $+$ |
|        $$x - 2 > 0$$        | $-$ | $-$ | $+$ |
| $$\frac{x + 1}{x - 2} > 0$$ | $+$ | $-$ | $+$ |
[/class]

Lo studio del segno mostra che il quoziente è positivo dove numeratore e denominatore hanno lo stesso segno, cioè per $x < -1$ e per $x > 2.$ Il punto $x = 2$ non appartiene a questo insieme, quindi il dominio è:

$$
\mathrm{dom}(g \circ f) = (-\infty, -1) \cup (2, +\infty)
$$

Anche in questo caso, se componiamo nell'ordine inverso otteniamo:

$$ \tag{5}
(f \circ g)(x) = \frac{\ln x + 1}{\ln x - 2}
$$

Per determinare il dominio della funzione composta nella $(5),$ osserviamo che il quoziente contiene il logaritmo $\ln x,$ definito soltanto per $x > 0.$ Inoltre, il denominatore $\ln x - 2$ deve essere diverso da zero, quindi dobbiamo escludere i valori per cui $\ln x = 2,$ cioè $x = e^2.$ Il dominio comprende dunque tutti i numeri reali positivi tranne $e^2,$ perciò possiamo scrivere:

$$
\mathrm{dom}(f \circ g) = (0, e^2) \cup (e^2, +\infty)
$$

## Associatività e ordine di composizione

Analizziamo adesso il caso di composizione di tre funzioni. Questa situazione si può risolvere in due modi, ed entrambi danno lo stesso risultato. Consideriamo ad esempio:

$$ \tag{6}
((h \circ g) \circ f)(x)
$$

Applicando due volte la $(1)$ al raggruppamento di sinistra della $(6),$ otteniamo:

$$
(h \circ g)(f(x)) = h(g(f(x))) \tag{7}
$$

Se applichiamo sempre la $(1),$ ma stavolta al raggruppamento di destra della $(6),$ otteniamo lo stesso risultato:

$$
h((g \circ f)(x)) = h(g(f(x))) \tag{8}
$$

Poiché dalla $(7)$ e dalla $(8)$ abbiamo ottenuto lo stesso valore $h(g(f(x))),$ possiamo scrivere che

$$
(h \circ g) \circ f = h \circ (g \circ f) = h \circ g \circ f \tag{9}
$$

La $(9)$ mostra quindi che la composizione di funzioni è associativa, ovvero possiamo cambiare il raggruppamento delle funzioni senza modificare il risultato, purché il loro ordine rimanga invariato. L'associatività quindi riguarda solo il raggruppamento, non l'ordine con cui si eseguono le operazioni. La composizione infatti, non è commutativa, come abbiamo mostrato nelle espressioni delle funzioni composte viste negli esempi.

## Scomposizione di una funzione

Negli esempi precedenti siamo partiti da due funzioni e abbiamo calcolato la loro composizione. Possiamo anche partire da una funzione già assegnata e cercare le funzioni che, applicate in successione, restituiscono la sua espressione. Consideriamo, per esempio, la seguente funzione:

$$
F(x) = \sqrt{\ln(x^2 + 1)}
$$

Per scrivere $F$ come composizione, individuiamo le operazioni da eseguire a partire dall'argomento $x:$

$$ \tag{10}
\begin{align}
&h(x) = x^2 + 1 \\[6pt]
&g(h(x)) = \ln(x^2 + 1) \\[10pt]
&f(g(h(x))) = \sqrt{\ln(x^2 + 1)} = F(x)
\end{align}
$$

Riconoscere le funzioni componenti è utile, per esempio, per applicare la regola di derivazione delle funzioni composte che stabilisce come combinare le derivate delle singole funzioni della $(10)$ per ottenere proprio la derivata di $F.$

Anche nell'integrazione per sostituzione, riconoscere una funzione interna di un'integranda non immediata aiuta a scegliere l'espressione da assumere come nuova variabile. Consideriamo, per esempio, l'integrale:

$$
\int 2x\cos(x^2) \ dx
$$

Nel fattore $\cos(x^2)$ riconosciamo la composizione della funzione interna $x^2$ con il coseno. Il fattore $2x$ che la moltiplica è proprio la derivata di $x^2,$ quindi scegliamo $u = x^2.$ Poiché $du = 2x \ dx,$ la sostituzione trasforma l'integrale in:

$$
\int \cos u \ du = \sin u + C \tag{11}
$$

Dalla $(11),$ tornando alla variabile $x,$ otteniamo le primitive dell'integrale che sono date da:

$$\sin(x^2) + C$$

## Monotonia e parità

La monotonia di una funzione composta di riduce allo studio del comportamento delle funzioni che la compongono. Per illustrare praticamente il problema, proviamo a determinare la monotonia della seguente funzione composta  sull'intervallo $x \gt 0$:

$$
\begin{align}
&f(x) = x^3 \\[6pt]
&g(t) = \frac{1}{t}\\[6pt]
&g(f(x)) = 1/x^3
\end{align}
$$

La funzione $f$ è strettamente crescente mentre $g$ diminuisce all'aumentare di $x.$ La funzione composta è dunque strettamente decrescente nell'intervallo considerato. Supponiamo ora che $f$ sia strettamente monotona su un generico intervallo $I$ e che $g$ sia strettamente monotona sull'immagine $f(I).$ Dobbiamo distinguere due casi

+ Quando $f$ e $g$ sono entrambe crescenti o entrambe decrescenti, la funzione composta è strettamente crescente.
+ Invece, se una funzione è crescente e l'altra decrescente, la funzione composta sarà strettamente decrescente.

- - -

Quando vogliamo invece studiare la parità di una funzione composta dobbiamo confrontare, per definizione, i valori della funzione composta in $x$ e in $-x,$ supponendo che il suo dominio sia simmetrico rispetto all'origine. Se la funzione interna $f$ è pari, si ha $f(-x) = f(x).$ La funzione esterna $g$ riceve quindi lo stesso argomento nei due casi e restituisce lo stesso valore:

$$
g(f(-x)) = g(f(x))
$$

La funzione composta è dunque pari, qualunque sia la parità di $g.$ Per esempio, $e^{-x^2}$ è pari perché $-x^2$ è pari. Se invece $f$ è dispari, vale $f(-x) = -f(x).$ In questo caso, la parità della funzione dipende dalla funzione $g$. Se $g$ è pari, il cambio di segno all'argomento non influisce sul risultato e la funzione composta è pari. Ad esempio, $\sin^2 x,$ si comporta in questo modo, essendo la funzione seno dispari, mentre il quadrato è pari. Quando sostituiamo $x$ con $-x,$ il seno cambia segno, ma il quadrato riconduce tutto a valori positivi, per cui si ottiene:

$$
\sin^2(-x) = (-\sin x)^2 = \sin^2 x
$$

La funzione composta è quindi pari.

## Iniettività, suriettività

Consideriamo adesso due funzioni $f \colon A \rightarrow B$ e $g \colon B \rightarrow C.$ Se entrambe sono iniettive, anche la loro composizione è iniettiva. Per verificarlo, prendiamo due argomenti $x_1$ e $x_2$ in $A$ e supponiamo che la funzione composta restituisca lo stesso valore:

$$
g(f(x_1)) = g(f(x_2)) \tag{12}
$$

Poiché $g$ è iniettiva, l'uguaglianza della $(12)$ implica che i suoi argomenti siano uguali, e quindi vale $f(x_1) = f(x_2).$ Ma anche $f$ è iniettiva, quindi dobbiamo avere $x_1 = x_2.$ Abbiamo quindi dimostrato che da $g(f(x_1)) = g(f(x_2))$ segue $x_1 = x_2,$ perciò la funzione composta $g \circ f$ è iniettiva.

Quando invece sappiamo che a essere iniettiva è la funzione composta, possiamo concludere immediatamente che $f$ è iniettiva. Infatti, se $f$ associasse lo stesso valore a due argomenti distinti, applicando $g$ otterremmo ancora lo stesso valore, e la composizione non sarebbe iniettiva. Tuttavia, non possiamo concludere che anche $g$ sia iniettiva su tutto $B.$ Consideriamo, per esempio, il seguente caso:

$$
\begin{gathered}
f(x) = x \\[6pt]
g(t) = t^2 \\[6pt]
(g \circ f)(x) = x^2
\end{gathered}
$$

La funzione composta è iniettiva sul suo dominio $[0, +\infty).$ La funzione $g,$ invece, non è iniettiva su $\mathbb{R},$ perché, per esempio, $g(-1) = g(1) = 1.$ Nella composizione questo problema non si presenta, perché $f$ assume soltanto valori non negativi, sui quali $g$ è iniettiva.

- - -

Vediamo adesso cosa accade per la suriettività. Supponiamo che $f$ sia suriettiva su $B$ e $g$ su $C.$ Vogliamo dimostrare che la funzione composta possa assumere ogni valore di $C.$ Se scegliamo un qualunque $c \in C,$ la suriettività di $g$ ci assicura che esiste un elemento $b \in B$ tale che $g(b) = c.$ Inoltre, poiché $f$ è suriettiva, questo garantisce l'esistenza di un numero $a \in A$ tale che $f(a) = b.$ Perciò possiamo scrivere la seguente relazione che dimostra che la funzione composta è suriettiva:

$$
(g \circ f)(a) = g(f(a)) = g(b) = c
$$

Se invece $g \circ f$ è suriettiva su $C,$ possiamo concludere che $g$ è suriettiva su $C,$ perché ogni valore assunto dalla composizione è anche un valore assunto da $g.$ Non è però necessario che $f$ sia suriettiva su $B.$ Per esempio, consideriamo la seguente situazione:

$$
\begin{align}
f(x) = x^2 \\[6pt]
g(t) = t^2
\end{align}
$$

La funzione $f$ non è suriettiva sul proprio codominio $\mathbb{R},$ perché non assume valori negativi. La funzione composta $(g \circ f)(x) = x^4$ è invece suriettiva su $[0, +\infty),$ perché ogni numero $c \ge 0$ si ottiene scegliendo $x = \sqrt[4]{c}.$ In questo caso, i soli valori non negativi prodotti da $f$ bastano a $g$ per raggiungere tutto il codominio della composizione.

Infine, se $f$ e $g$ sono entrambe biiettive, la loro composizione è sia iniettiva sia suriettiva, quindi è biiettiva.

## Limitatezza

Per studiare la limitatezza di una funzione composta, partiamo dall'osservare la funzione esterna $g.$ Se questa è limitata sul proprio dominio, tutti i valori che restituisce saranno compresi tra due valori costanti. Necessariamente, quindi, anche i valori $g(f(x))$ avranno questi limiti, e quindi la funzione composta è limitata. Per esempio, il seno assume sempre valori tra $-1$ e $1,$ qualunque sia il suo argomento, e per qualunque funzione $f$ a valori reali vale:

$$
-1 \le \sin(f(x)) \le 1
$$

Se invece ad essere limitata è la funzione interna, questo non basta a garantire che la funzione composta sia anch'essa limitata. Consideriamo, ad esempio, le funzioni:

$$
\begin{align}
f(x) &= \frac{1}{1 + x^2} \\[6pt]
g(t) &= \frac{1}{t}
\end{align}
$$

La funzione $f$ è limitata, perché per ogni $x$ reale si ha $0 < f(x) \le 1.$ La composizione dà:

$$
(g \circ f)(x) = 1 + x^2
$$

Il risultato della composizione è dunque una funzione illimitata.

## Continuità, limiti e derivabilità

Quando si vuole determinare la continuità di una funzione composta si considera il comportamento delle funzioni che la compongono. Supponiamo di avere una funzione $f$ continua in $x_0$ e che $g$ sia continua in $f(x_0).$ Quando $x$ tende a $x_0,$ i valori $f(x)$ tendono a $f(x_0).$ La continuità di $g$ in questo punto garantisce allora che è soddisfatta la seguente uguaglianza:

$$\tag{13}
\lim_{x \to x_0} g(f(x)) = g(f(x_0))
$$

Il limite nella $(13)$ coincide con il valore della funzione composta in $x_0,$ e quindi $g \circ f$ è continua in quel punto. Per esempio, la funzione $\ln(x^2 + 1)$ è continua su tutto $\mathbb{R},$ perché il polinomio $x^2 + 1$ è a sua volta continuo e assume soltanto valori positivi nei quali il logaritmo è continuo.

Lo stesso ragionamento si usa per calcolare il limite di una funzione composta quando la funzione $f$ tende a un valore finito $L.$ Quando $L$ appartiene al dominio di $g$ e $g$ è continua nel punto $L,$ allora possiamo scrivere:

$$
\lim_{x \to x_0} f(x) = L
\quad \Longrightarrow \quad
\lim_{x \to x_0} g(f(x)) = g(L)
$$

Consideriamo, per esempio, $f(x) = x$ e la funzione $g$ definita a tratti:

$$
g(t) =
\begin{cases}
1 & \text{se } t \neq 0 \\[6pt]
0 & \text{se } t = 0
\end{cases}
$$

Per $x \to 0$ la $f$ tende a zero, ma in quel punto $g$ è discontinua e quindi per ogni $x \neq 0$ si ha $g(f(x)) = 1,$ perciò possiamo scrivere:

$$
\lim_{x \to 0} g(f(x)) = 1 \neq 0 = g(0)
$$

- - -

Supponiamo ora che $f$ sia uniformemente continua su un insieme $A$ e che $g$ sia uniformemente continua sull'immagine $f(A).$ Quello che vogliamo dimostrare è che anche $g \circ f$ è uniformemente continua su $A.$ Per la continuità uniforme di $g,$ esiste $\eta > 0$ tale che, fissato un numero $\epsilon \gt 0,$ per ogni $u,v \in f(A),$ vale:

$$
|u - v| < \eta \quad \Longrightarrow \quad |g(u) - g(v)| < \varepsilon \tag{14}
$$

La continuità uniforme di $f$ permette poi di scegliere $\delta > 0$ tale che, per ogni $x,y \in A,$ si abbia:

$$
|x - y| < \delta \quad \Longrightarrow \quad |f(x) - f(y)| < \eta
$$

Applicare la $(14)$ con $u = f(x)$ e $v = f(y),$ ottenendo:

$$
|x - y| < \delta \quad \Longrightarrow \quad |g(f(x)) - g(f(y))| < \varepsilon
$$

Poiché lo stesso $\delta$ vale per tutte le coppie di punti di $A,$ la funzione composta è uniformemente continua su $A.$

- - -

Infine vale la pena citare che per calcolare la derivata di una funzione composta si ricorre alla regola della catena data dalla seguente relazione:

$$
(g \circ f)'(x_0) = g'(f(x_0))f'(x_0)
$$

Per una trattazione approfondita, si rimanda alla relativa voce.

## Composizione con la funzione inversa

Quando $f$ ammette una funzione inversa, le funzioni composte con quest'ultima sono funzioni identità su insiemi diversi:

$$ \tag{15}
\begin{align}
(f^{-1} \circ f)(x) &= x \\[6pt]
(f \circ f^{-1})(y) &= y
\end{align}
$$

La prima identità vale per ogni $x$ nel dominio di $f,$ la seconda per ogni $y$ nella sua immagine. L'invertibilità richiede che $f$ sia iniettiva e suriettiva sul codominio scelto. Una funzione non iniettiva può avere una restrizione invertibile, e le due identità valgono allora sugli insiemi ristretti. Se $f$ e $g$ sono entrambe biiettive, l'inversa della loro composizione si ottiene componendo le rispettive inverse in ordine inverso:

$$
(g \circ f)^{-1} = f^{-1} \circ g^{-1}
$$

Per esempio, consideriamo la funzione $f(x)=x^2$ limitando il dominio ai numeri non negativi. Su questo dominio $f$ è biiettiva, perché ogni numero non negativo è il quadrato di un unico numero non negativo. L'inversa di $f$ è la funzione radice quadrata. Applicando prima $f$ e poi la sua inversa, ritroviamo l'argomento iniziale, come previsto dalla prima uguaglianza della $(15):$

$$
(f^{-1} \circ f)(x) = \sqrt{x^2} = x
$$

Se invece estendiamo la definizione della $f(x) = x^2$ su tutto $\mathbb{R},$ otteniamo una funzione non iniettiva, perché dati due numeri opposti, come $-3$ e $3,$ questi hanno sempre lo stesso quadrato. A differenza del caso visto prima, la radice quadrata non può quindi essere la sua inversa su tutto $\mathbb{R}.$ Possiamo comunque comporre le due funzioni, sempre nell'ordine della prima uguaglianza della $(15),$ ma in questo caso il risultato è:

$$
\sqrt{x^2} = |x|
$$

Per gli argomenti negativi non ritroviamo quindi il valore iniziale. Per esempio, partendo da $-3,$ il quadrato dà $9$ e la radice quadrata di $9$ dà $3,$ anziché $-3.$ Procedendo nell'ordine opposto, la radice richiede $x \ge 0,$ e per ogni argomento che soddisfa questa condizione otteniamo:

$$
(\sqrt{x})^2 = x
$$

## Composizione con una funzione definita a tratti

Analizziamo adesso un caso particolare di composizione che coinvolge, nella funzione esterna, una funzione definita a tratti. In questi casi, bisogna tenere a mente che ogni condizione che individua un ramo di $g$ deve essere imposta anche su $f(x).$ Consideriamo ad esempio la funzione:

$$
g(t) =
\begin{cases}
1 - t & t < 0 \\[6pt]
1 + t^2 & t \ge 0
\end{cases}
$$

Immaginiamo che $f(x) = x^2 - 1$ sia la funzione interna. Per calcolare $g(f(x)),$ sostituiamo $t$ con $x^2 - 1$ sia nelle espressioni di $g$ sia nelle condizioni che stabiliscono quale espressione usare. La prima espressione, $1 - t,$ si usa quando l'argomento di $g$ è negativo. Poiché nella composizione questo argomento è $x^2 - 1,$ dobbiamo quindi richiedere:

$$
x^2 - 1 < 0 \quad \Longleftrightarrow \quad -1 < x < 1
$$

Per questi valori di $x$ usiamo quindi la prima espressione di $g,$ sostituendo $t$ con $x^2 - 1,$ ottenendo:

$$
(g \circ f)(x) = 1 - (x^2 - 1) = 2 - x^2
$$

La seconda espressione, $1 + t^2,$ si usa invece quando l'argomento di $g$ è non negativo e in questo caso la condizione è:

$$
x^2 - 1 \ge 0 \quad \Longleftrightarrow \quad x \in (-\infty, -1] \cup [1, +\infty)
$$

Per questi valori di $x$ sostituiamo $t$ con $x^2 - 1$ nella seconda espressione di $g,$ ottenendo:

$$
(g \circ f)(x) = 1 + (x^2 - 1)^2
$$

Riunendo tutti e tre i tratti, la funzione composta è quindi:

$$
(g \circ f)(x) =
\begin{cases}
1 + (x^2 - 1)^2 & x \le -1 \\[6pt]
2 - x^2 & -1 < x < 1 \\[6pt]
1 + (x^2 - 1)^2 & x \ge 1
\end{cases}
$$
