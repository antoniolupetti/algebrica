---
title: Cauchy-Schwarz Inequality
source: https://algebrica.org/complex-number-fundamental-inequalities/
license: CC BY-NC 4.0
tags:
  - cauchy-schwarz-inequality
  - complex-modulus
  - complex-numbers
---
## Definizione

Se consideriamo due liste di numeri complessi, $a_1, \ldots, a_n$ e $b_1, \ldots, b_n,$ la disuguaglianza di Cauchy-Schwarz stima il modulo della somma dei prodotti $a_k\overline{b_k}$ a partire dai moduli di quei numeri. In termini formali la disuguaglianza è data dalla seguente relazione:

$$\left|\sum_{k=1}^{n} a_k \overline{b_k}\right|^2 \leq \left(\sum_{k=1}^{n} |a_k|^2\right) \left(\sum_{k=1}^{n} |b_k|^2\right) \tag{1}$$

Per dimostrare la disuguaglianza $(1),$ associamo a ogni $t \in \mathbb{C}$ la somma $P(t)$ definita nel seguente modo:

$$P(t) = \sum_{k=1}^{n} |a_k - t b_k|^2 \tag{2}$$

Indichiamo con $\sigma$ la somma che compare nel primo membro di $(1).$

$$\sigma = \sum_{k=1}^{n} a_k \overline{b_k} \tag{3}$$

Con la notazione di $(3),$ il primo membro di $(1)$ è $|\sigma|^2.$ Per sviluppare la somma della $(2),$ applichiamo l'identità $|z|^2 = z\overline{z}$ con $z = a_k - tb_k$ in modo da ottenere:

$$
\begin{aligned}
P(t) &= \sum_{k=1}^{n} |a_k - tb_k|^2 \\[6pt]
     &= \sum_{k=1}^{n} (a_k - tb_k)\bigl(\overline{a_k} - \overline{t}\overline{b_k}\bigr) \\[6pt]
     &= \sum_{k=1}^{n} \bigl(|a_k|^2 - tb_k\overline{a_k} - \overline{t}a_k\overline{b_k} + |t|^2|b_k|^2\bigr) \\[6pt]
     &= \sum_{k=1}^{n} |a_k|^2 - t\sum_{k=1}^{n} b_k\overline{a_k} - \overline{t}\sum_{k=1}^{n} a_k\overline{b_k} + |t|^2\sum_{k=1}^{n} |b_k|^2 \\[6pt]
     &= \sum_{k=1}^{n} |a_k|^2 - t\overline{\sigma} - \overline{t}\sigma + |t|^2 \sum_{k=1}^{n} |b_k|^2
\end{aligned}
\tag{4}
$$

Quando la somma $\sum_{k=1}^{n} |b_k|^2$ è nulla, ogni $b_k$ è nullo e in $(1)$ vale l'uguaglianza. Infatti, in questo caso entrambi i membri sono uguali a zero e si ottiene:

$$\left|\sum_{k=1}^{n} a_k\overline{b_k}\right|^2 = 0 = \left(\sum_{k=1}^{n} |a_k|^2\right)\left(\sum_{k=1}^{n} |b_k|^2\right) \tag{5}$$

Supponiamo ora che $\sum_{k=1}^{n} |b_k|^2 > 0$ e poniamo:

$$t_0 = \sigma / \sum_{k=1}^{n} |b_k|^2$$

Poiché $t_0\sum_{k=1}^{n} |b_k|^2 = \sigma,$ l'ultimo termine della $(4)$ diventa $\overline{t_0}\sigma$ e si cancella con il termine precedente. Per la definizione della $(2),$ $P(t_0)$ è non negativa, quindi si ottiene la seguente relazione:

$$0 \leq P(t_0) = \sum_{k=1}^{n} |a_k|^2 - t_0\overline{\sigma} = \sum_{k=1}^{n} |a_k|^2 - \frac{|\sigma|^2}{\sum_{k=1}^{n} |b_k|^2} \tag{6}$$

Da $(6)$ si ricava la seguente maggiorazione:

$$\frac{|\sigma|^2}{\sum_{k=1}^{n} |b_k|^2} \leq \sum_{k=1}^{n} |a_k|^2 \tag{7}$$

Ora basta moltiplicare entrambi i membri di $(7)$ per $\sum_{k=1}^{n} |b_k|^2$ e poiché questa somma è positiva, il verso della disuguaglianza si mantiene, ottenendo:

$$|\sigma|^2 \leq \left(\sum_{k=1}^{n} |a_k|^2\right) \left(\sum_{k=1}^{n} |b_k|^2\right) \tag{8}$$

Sostituendo nella $(8)$ l'espressione di $\sigma$ data dalla $(3),$ ritroviamo la disuguaglianza $(1).$ Dalla $(5)$ sappiamo che l'uguaglianza vale se tutti i $b_k$ sono nulli. Se almeno un $b_k$ è diverso da zero, dalla $(6)$ segue che nella $(8)$ vale l'uguaglianza esattamente quando $P(t_0) = 0.$ Dalla $(2)$ si vede che questa somma si annulla solo se tutti i suoi addendi sono nulli, cioè se $a_k = t_0b_k$ per ogni $k.$

Viceversa, se la seconda tupla è non nulla e $a_k = cb_k$ per ogni $k,$ dalla $(3)$ otteniamo $\sigma = c\sum_{k=1}^{n} |b_k|^2.$ Ne segue che $t_0 = c$ e $P(t_0) = 0.$

Abbiamo così dimostrato la disuguaglianza $(1)$ e stabilito che l'uguaglianza vale se e solo se le tuple $(a_1, \ldots, a_n)$ e $(b_1, \ldots, b_n)$ sono linearmente dipendenti in $\mathbb{C}^n.$

- - -

Vediamo come si può applicare la disuguaglianza andando a cercare il massimo di $|z + (1+i)w|$ tra le coppie di numeri complessi $(z,w)$ che soddisfano la seguente relazione:

$$|z|^2 + |w|^2 = 1 \tag{9}$$

Per applicare la $(1),$ scegliamo $(a_1,a_2) = (z,w)$ e $(b_1,b_2) = (1,1-i),$ così il coniugato di $b_2$ è il coefficiente di $w.$ Nel prodotto a destra della $(1),$ il primo fattore vale $1$ per la $(9)$ e il secondo vale $1 + |1-i|^2 = 1 + 1^2 + (-1)^2 = 3.$

$$|z + (1+i)w|^2 \leq (|z|^2 + |w|^2)(1 + |1-i|^2) = 3$$

Entrambi i membri sono non negativi, ed estraendo la radice quadrata otteniamo la stima per il modulo.

$$|z + (1+i)w| \leq \sqrt{3}$$

Nella $(1)$ vale l'uguaglianza se e solo se le due tuple sono linearmente dipendenti. In questo esempio la seconda tupla è $(1,1-i)$ ed è non nulla, quindi scegliamo $(z,w)$ come suo multiplo. Poiché $1 + |1-i|^2 = 3,$ dividiamo entrambe le componenti di $(1,1-i)$ per $\sqrt{3}$ per soddisfare il vincolo della $(9).$

$$z = \frac{1}{\sqrt{3}}, \qquad w = \frac{1-i}{\sqrt{3}} \tag{10}$$

Con i valori dati dalla $(10),$ il modulo $|z + (1+i)w|$ vale $|(1+2)/\sqrt{3}| = \sqrt{3}.$ Poiché la maggiorazione è raggiunta, $\sqrt{3}$ è il massimo cercato.
