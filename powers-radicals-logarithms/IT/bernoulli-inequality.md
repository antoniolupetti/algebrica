---
title: Bernoulli's Inequality
source: https://algebrica.org/bernoulli-inequality/
license: CC BY-NC 4.0
tags:
  - bernoulli-inequality
  - inequalities
  - mathematical-induction
  - powers
---
## Enunciato

La disuguaglianza di Bernoulli afferma che, per ogni numero reale $x \ge -1$ e per ogni intero positivo $n,$ la potenza $(1+x)^n$ è maggiore o uguale all'espressione lineare $1+nx:$

$$ \tag{1}
(1+x)^n \ge 1+nx
$$

La $(1)$ vale quando $n=1$ o $x=0$. In ogni altro caso vale invece la disuguaglianza stretta:

$$ \tag{2}
(1+x)^n \gt 1+nx
$$

La $(1)$ e la $(2)$ consentono in pratica di stimare dal basso una potenza mediante un'espressione lineare, senza dover sviluppare o calcolare la potenza stessa perché in alcuni casi questo calcolo può risultare praticamente oneroso. La condizione $x \ge -1$ serve a garantire che il termine $1+x$ del membro a sinistra sia non negativo, così da non dover invertire il verso della disuguaglianza come vedremo nella dimostrazione.

La dimostrazione della $(1)$ procede per induzione, considerando $n.$ Quando $n = 1$ entrambi i membri sono uguali a $1+x.$ Se supponiamo che la disuguaglianza valga per un certo $n \ge 1,$ moltiplicando per $1+x$ (che abbiamo detto essere non negativo) si conserva il verso della disuguaglianza e si ottiene:

$$
(1+x)^{n+1} \ge (1+nx)(1+x) = 1+(n+1)x+nx^2
$$

Poiché $nx^2 \ge 0,$ il membro di destra è maggiore o uguale a $1+(n+1)x$ e quindi si ha:

$$
(1+x)^{n+1} \ge 1+(n+1)x
$$

La disuguaglianza vale quindi per $n+1,$ e la dimostrazione per induzione è completa.

## Alcune applicazioni

Vediamo un'applicazione pratica dell'applicazione della $(1)$ e supponiamo che una certa quantità $Q_0 > 0$ aumenti del $2\%$ rispetto al valore raggiunto dopo l'aumento precedente per $10$ volte. Ogni aumento moltiplica la quantità per $1{,}02$ e quindi il valore finale è:

$$
Q = Q_0(1{,}02)^{10}
$$

Se applichiamo la disuguaglianza di Bernoulli con $x = 0{,}02$ e $n = 10,$ otteniamo la seguente stima:

$$
(1{,}02)^{10} \ge 1+10\cdot 0{,}02 = 1{,}2
$$

Poiché $Q_0 > 0,$ possiamo moltiplicare entrambi i membri della disuguaglianza per $Q_0$ senza cambiarne il verso e ottenere:

$$
Q_0(1{,}02)^{10} \ge 1{,}2Q_0
$$

Il membro a sinistra è il valore finale $Q,$ mentre quello a destra è $Q_0+0{,}2Q_0.$ Sottraendo $Q_0$ da entrambi i membri, otteniamo:

$$
Q-Q_0 \ge 0{,}2Q_0
$$

L'aumento $Q-Q_0$ è quindi almeno pari al $20\%$ della quantità iniziale.

- - -

La disuguaglianza di Bernoulli può essere usata anche per dimostrare la monotonia di alcune successioni e, quando sono anche limitate, stabilirne la convergenza. Ad esempio, dimostriamo che la seguente successione è strettamente crescente:

$$a_n = \left(1+\frac{1}{n}\right)^n$$ 
Consideriamo il caso con $n \ge 1,$ per cui il rapporto fra termini consecutivi è dato dalla seguente identità:

$$
\frac{a_{n+1}}{a_n}
= \left(1+\frac{1}{n+1}\right)
\left(1-\frac{1}{(n+1)^2}\right)^n
$$

Applicando la $(1)$ con $x = -1/(n+1)^2$ si ottiene:

$$
\begin{align}
\frac{a_{n+1}}{a_n}
&\ge \left(1+\frac{1}{n+1}\right)
\left(1-\frac{n}{(n+1)^2}\right) \\[6pt]
&= 1+\frac{1}{(n+1)^3} \\[6pt]
&> 1
\end{align}
$$

La successione è anche limitata superiormente, come dimostrato nella pagina sul numero di Eulero. Poiché è crescente e limitata, converge e il suo limite definisce il numero $e:$

$$
e = \lim_{n \to +\infty}\left(1+\frac{1}{n}\right)^n
$$
