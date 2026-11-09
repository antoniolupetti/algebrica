---
title: Fundamental Inequalities for Complex Numbers
source: https://algebrica.org/complex-number-fundamental-inequalities/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - cauchy-schwarz-inequality
  - complex-modulus
  - complex-numbers
  - reverse-triangle-inequality
  - triangle-inequality
---
## Disuguaglianze fondamentali

Come abbiamo visto nell'introduzione, l'insieme dei numeri complessi $\mathbb{C}$ è un campo che non ammette un ordine totale compatibile con le sue operazioni aritmetiche. Una scrittura del tipo seguente richiede la scelta di un ordine sui numeri complessi.

$$z_1 < z_2 \tag{1}$$

Tuttavia, il modulo $|z|$ permette comunque una teoria quantitativa in quanto associa a ogni numero complesso un valore reale non negativo, mediante il quale si possono confrontare grandezze, stimare distanze e maggiorare somme e prodotti. Ricordiamo che il modulo di un numero complesso $z = a + bi$ è definito dalla seguente formula e rappresenta la lunghezza del vettore dall'origine al punto $(a,b).$

$$|z| = \sqrt{a^2 + b^2} \tag{2}$$

Abbiamo quindi una serie di disuguaglianze che ci forniscono gli strumenti per effettuare questo genere di confronti e sono usate anche nello studio delle successioni e delle serie a termini complessi. Iniziamo a vedere le disuguaglianze per la parte reale e immaginaria. Dato un numero complesso in forma algebrica del tipo $z = a + bi,$ poniamo $a = \mathrm{Re}(z)$ e $b = \mathrm{Im}(z).$ Dalla $(2)$ segue che il valore assoluto di ciascuna componente è al più uguale al modulo di $z.$

$$
\begin{align}
|\mathrm{Re}(z)| &\leq |z| \tag{3} \\[6pt]
|\mathrm{Im}(z)| &\leq |z| \tag{4}
\end{align}
$$

Per dimostrare la $(3)$ basta osservare che $a^2 \leq a^2 + b^2.$ Poiché la radice quadrata è crescente sui numeri reali non negativi, si ottiene:

$$|a| \leq \sqrt{a^2 + b^2} = |z|$$

Anche la $(4)$ segue dalla relazione $b^2 \leq a^2 + b^2.$ Nella $(3)$ si ha uguaglianza se e solo se $b = 0,$ mentre nella $(4)$ si ha uguaglianza se e solo se $a = 0.$ La somma dei valori assoluti delle componenti fornisce invece un limite superiore per il modulo dato da:

$$|z| \leq |\mathrm{Re}(z)| + |\mathrm{Im}(z)| \tag{5}$$

Per dimostrare la $(5)$ sviluppiamo il quadrato della somma, ottenendo:

$$(|a| + |b|)^2 = a^2 + b^2 + 2|a||b|$$

Poiché il termine $2|a||b|$ è non negativo, si ha la seguente disuguaglianza:

$$a^2 + b^2 \leq (|a| + |b|)^2 \tag{6}$$

Estraendo le radici dalla $(6)$ si ottiene la $(5).$ L'uguaglianza vale se e solo se $|a||b| = 0,$ ossia se almeno una delle due componenti è nulla. Altre disuguaglianze utili sono la disuguaglianza triangolare e la disuguaglianza di Cauchy-Schwarz, che sono indicate di seguito e trattate nelle relative voci:

[class="table-1 -right"]

|                                                                                                                                                                 |                                          |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| $$\lvert z_1 + z_2\rvert \leq \lvert z_1\rvert + \lvert z_2\rvert$$                                                                                             | [Explore](../triangle-inequality/)       |
| $$\left\lvert\sum_{k=1}^{n} a_k\overline{b_k}\right\rvert^2 \leq \left(\sum_{k=1}^{n} \lvert a_k\rvert^2\right)\left(\sum_{k=1}^{n} \lvert b_k\rvert^2\right)$$ | [Explore](../cauchy-schwarz-inequality/) |

[/class]