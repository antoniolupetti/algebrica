---
title: Intervals
source: https://algebrica.org/intervals/
license: CC BY-NC 4.0
tags:
  - bounded-interval
  - closed-interval
  - connectedness
  - convexity
  - half-open-interval
  - interval
  - length
  - neighborhood
  - open-interval
  - real-line
  - unbounded-interval
---

## Definizione

Un sottoinsieme $I \subseteq \mathbb{R}$ è un intervallo se e solo se per ogni coppia di numeri reali $a,b$ vale la seguente implicazione:

$$
\begin{align}
a,b \in I,\quad a \lt b &\implies \{x \in \mathbb{R} : a \leq x \leq b\} \subseteq I \tag{1}
\end{align}
$$

La $(1)$ dice che, se $a$ e $b$ appartengono a $I,$ anche ogni punto compreso tra $a$ e $b$ appartiene a $I.$ Questa proprietà si chiama convessità. Per esempio, l'insieme $\{0,2\}$ non è un intervallo perché contiene $0$ e $2,$ ma non il punto $1$ compreso tra loro. Un intervallo $I$ è limitato se esistono due numeri reali $m \leq M$ tali che ogni punto di $I$ sia maggiore o uguale a $m$ e minore o uguale a $M.$ Dati due numeri reali $a \lt b,$ l'intervallo aperto di estremi $a$ e $b$ si definisce come:

$$
\begin{align}
(a,b) &= \{x \in \mathbb{R} : a \lt x \lt b\} \tag{2}
\end{align}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-o | sign+r-in-o |     |
[/shortcode]

Dati due numeri reali $a \leq b,$ l'intervallo chiuso di estremi $a$ e $b$ è definito dalla seguente identità:

$$
\begin{align}
[a,b] &= \{x \in \mathbb{R} : a \leq x \leq b\} \tag{3}
\end{align}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-c | sign+r-in-c |     |
[/shortcode]

Dati due numeri reali $a \lt b,$ entrambi gli intervalli semiaperti di estremi $a$ e $b$ contengono tutti i punti strettamente compresi tra $a$ e $b$ e uno solo dei due estremi. Il primo si definisce così:

$$
\begin{align}
[a,b) &= \{x \in \mathbb{R} : a \leq x \lt b\} \tag{4}
\end{align}
$$


[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-c | sign+r-in-o |     |
[/shortcode]

Il secondo intervallo semiaperto si definisce nel seguente modo:

$$
\begin{align}
(a,b] &= \{x \in \mathbb{R} : a \lt x \leq b\} \tag{5}
\end{align}
$$

[shortcode="intervals"]
|     | $a$ | $b$ |     |
|:----|-----|-----|-----|
|     | sign+l-in-o | sign+r-in-c |     |
[/shortcode]

Esiste poi l'intervallo degenere $[a,a]=\{a\}$ che contiene un solo punto, e soddisfa la definizione di intervallo perché non contiene due punti distinti tra i quali occorra includerne altri. Passiamo ora agli intervalli illimitati che si estendono indefinitamente in almeno una direzione. Tali intervalli sono dati dalle seguenti identità:

$$
[a, +\infty) = \{x \in \mathbb{R} : x \geq a\} \tag{6}
$$

[shortcode="intervals"]
|     | $a$ |     |
|:----|-----|-----|
|     | sign+l-c |     |
[/shortcode]

$$
(a, +\infty) = \{x \in \mathbb{R} : x > a\} \tag{7}
$$

[shortcode="intervals"]
|     | $a$ |     |
|:----|-----|-----|
|     | sign+l-o |     |
[/shortcode]

$$
(-\infty, b] = \{x \in \mathbb{R} : x \leq b\} \tag{8}
$$

[shortcode="intervals"]
|     | $b$ |     |
|:----|-----|-----|
|     | sign+r-c |     |
[/shortcode]

$$
(-\infty, b) = \{x \in \mathbb{R} : x < b\} \tag{9}
$$

[shortcode="intervals"]
|     | $b$ |     |
|:----|-----|-----|
|     | sign+r-o |     |
[/shortcode]

Nello specifico, anche la retta reale è un intervallo che si può scrivere come $(-\infty,+\infty)=\mathbb{R}$ e comprende tutti i numeri reali.

## Operazioni sugli intervalli

Definiamo ora alcune operazioni sugli intervalli, partendo dall'[intersezione](../sets/) $I \cap J$ che rappresenta l'insieme dei punti che appartengono sia a $I$ sia a $J.$ Se due punti appartengono a entrambi gli intervalli, per la $(1)$ anche tutti i punti compresi tra loro appartengono a entrambi. L'intersezione quindi soddisfa la stessa condizione ed è un intervallo che può essere anche vuoto o degenere. Per esempio, un punto di $(1,5)$ appartiene anche a $(3,7)$ se è maggiore di $3$ e possiamo scrivere come risultato della loro intersezione la seguente uguaglianza:

$$
\begin{align}
(1,5) \cap (3,7) &= (3,5) \tag{10}
\end{align}
$$

[shortcode="intervals"]
|     | $1$ | $3$ | $5$ | $7$ |     |
|:----|-----|-----|-----|-----|-----|
|     | sign+l-in-o |             | sign+r-in-o |             |     |
|     |             | sign+l-in-o |             | sign+r-in-o |     |
|     |             | sign+l-in-o-h | sign+r-in-o-h |           |     |
[/shortcode]

La terza riga del diagramma mostra l'intervallo ottenuto nella $(10).$

- - -

L'unione $I \cup J$ è invece data dall'insieme dei punti che appartengono ad almeno uno dei due intervalli. Quindi, l'unione di due intervalli non vuoti è un intervallo se i due intervalli si intersecano oppure se si toccano in un estremo che appartiene ad almeno uno dei due. Nell'esempio precedente l'unione dà l'intervallo $(1,7).$

[shortcode="intervals"]
|     | $1$ | $3$ | $5$ | $7$ |     |
|:----|-----|-----|-----|-----|-----|
|     | sign+l-in-o |             | sign+r-in-o |             |     |
|     |             | sign+l-in-o |             | sign+r-in-o |     |
|     | sign+l-in-o-h | sign+s-h |             | sign+r-in-o-h |     |
[/shortcode]

La terza riga mostra l'unione $(1,7).$ L'unione $(1,3)\cup(5,7)$ non è invece un intervallo, perché i punti fra $3$ e $5$ non appartengono a nessuno dei due insiemi.

## Intorni

Dalla definizione di intervallo possiamo ricavare quella di intorno e, in particolare, di un $\varepsilon$-intorno di un punto $x_0 \in \mathbb{R}$ è l'intervallo aperto con centro $x_0$ e raggio $\varepsilon \gt 0.$ Questo intorno contiene tutti i punti la cui distanza da $x_0$ è strettamente minore di $\varepsilon$ e questa distanza, come sappiamo, corrisponde al [valore assoluto](../absolute-value/) di $x-x_0.$ Possiamo scrivere l'intorno in questo modo:

$$
\begin{align}
(x_0 - \varepsilon, \ x_0 + \varepsilon) &= \{x \in \mathbb{R} : |x-x_0| \lt \varepsilon\} \tag{11}
\end{align}
$$

[shortcode="intervals"]
|     | $x_0 - \varepsilon$ | $x_0$ | $x_0 + \varepsilon$ |     |
|:----|---------------------|-------|---------------------|-----|
|     | sign+l-in-o-h | sign+s-h | sign+r-in-o-h |     |
[/shortcode]

Gli intorni sono utili perché si usano nelle definizioni di [limite](../limits/) e della continuità. Ad esempio, una funzione $f\colon D\to\mathbb{R},$ con $D\subseteq\mathbb{R},$ si dice continua in $x_0\in D$ se, per ogni intorno $\varepsilon\gt 0,$ esiste un $\delta\gt 0$ tale che per ogni $x\in D$ valga la seguente implicazione:

$$
\begin{align}
|x-x_0| \lt \delta &\implies |f(x)-f(x_0)| \lt \varepsilon \tag{12}
\end{align}
$$

Nella $(12)$ scegliamo il raggio $\delta$ in modo che le immagini dei punti del dominio vicini a $x_0$ rimangano nell'intorno di $f(x_0).$ Per stabilire se $x_0$ è interno a un insieme $S\subseteq\mathbb{R},$ cerchiamo invece un raggio $\varepsilon\gt 0$ per cui tutti i punti dell'intorno di $x_0$ nella $(11)$ appartengano a $S.$

Ogni punto di $(a,b)$ è interno, perché si può scegliere un raggio minore della sua distanza da entrambi gli estremi. Ogni intorno di $a$ contiene punti minori di $a$ e ogni intorno di $b$ contiene punti maggiori di $b.$ Per questo gli estremi di $[a,b]$ non sono punti interni. La relazione tra intorni, punti interni e insiemi aperti e chiusi è sviluppata nella voce sulla [topologia della retta reale](../topology-of-the-real-line/).

## Lunghezza di un intervallo

La lunghezza di un intervallo limitato non vuoto $I$ è la distanza tra il suo estremo inferiore $a$ e il suo estremo superiore $b$ e possiamo indicarla come: 

$$
\begin{align}
\ell(I) &= b-a \tag{13}
\end{align}
$$

Poiché nella $(13)$ compaiono solo i valori degli estremi, per $a\lt b$ gli intervalli $(a,b),$ $[a,b),$ $(a,b]$ e $[a,b]$ hanno tutti la stessa lunghezza. Se i due estremi coincidono, la $(13)$ dà $\ell([a,a])=0,$ quindi l'intervallo degenere visto poco prima. Un intervallo illimitato ha lunghezza infinita, perché per ogni $M\gt 0$ contiene due punti a distanza maggiore di $M$ e dunque un intervallo chiuso di lunghezza maggiore di $M.$

Intervalli di lunghezze diverse possono avere la stessa cardinalità. Infatti ogni intervallo che contiene almeno due punti ha la stessa cardinalità di $\mathbb{R},$ sia che abbia lunghezza finita sia che abbia lunghezza infinita. La misura di Lebesgue estende la lunghezza degli intervalli a una classe più ampia di sottoinsiemi della retta reale e assegna a ogni intervallo limitato non vuoto la lunghezza data dalla $(13).$ In generale, ogni insieme finito ha [misura nulla](../riemann-integrability-criteria/), perciò aggiungere o togliere un numero finito di punti lascia invariata la misura anche quando l'insieme risultante non è più un intervallo (questa misura è alla base dell'integrale di Lebesgue).
