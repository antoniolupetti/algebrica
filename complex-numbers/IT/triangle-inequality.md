---
title: Triangle Inequality
source: https://algebrica.org/complex-number-fundamental-inequalities/
license: CC BY-NC 4.0
tags:
  - absolute-value
  - complex-modulus
  - complex-numbers
  - reverse-triangle-inequality
  - triangle-inequality
---
## Definizione

La disuguaglianza triangolare consente di maggiorare il modulo della somma di due numeri complessi $z_1$ e $z_2$ con la somma dei loro moduli ed è data dalla seguente relazione:

$$|z_1 + z_2| \leq |z_1| + |z_2| \tag{1}$$

Per dimostrare la $(1)$ usiamo l'identità $|z|^2 = z\overline{z}$ e la seguente proprietà del coniugato di una somma.

$$\overline{z_1 + z_2} = \overline{z_1} + \overline{z_2} \tag{2}$$

Calcoliamo quindi $|z_1 + z_2|^2$ e otteniamo:

$$
\begin{aligned}
|z_1 + z_2|^2 &= (z_1 + z_2)\overline{(z_1 + z_2)} \\[6pt]
              &= (z_1 + z_2)(\overline{z_1} + \overline{z_2}) \\[6pt]
              &= |z_1|^2 + z_1\overline{z_2} + \overline{z_1}z_2 + |z_2|^2
\end{aligned}
\tag{3}
$$

Nell'ultima uguaglianza della $(3)$ i termini $z_1\overline{z_2}$ e $\overline{z_1}z_2$ sono coniugati. La loro somma è quindi il doppio della parte reale di ciascuno.

$$z_1\overline{z_2} + \overline{z_1}z_2 = 2\mathrm{Re}(z_1\overline{z_2}) \tag{4}$$

La $(4)$ riduce la stima dei termini misti a quella di $\mathrm{Re}(z_1\overline{z_2}).$ Per ogni numero complesso $w = a + bi$ si ha $\mathrm{Re}(w) \leq |w|,$ poiché $\mathrm{Re}(w) = a \leq |a|$ e $|a| = \sqrt{a^2} \leq \sqrt{a^2 + b^2} = |w|.$ Se poniamo $w = z_1\overline{z_2}$ otteniamo $\mathrm{Re}(z_1\overline{z_2}) \leq |z_1\overline{z_2}| = |z_1||z_2|,$ poiché il modulo è moltiplicativo e $|\overline{z_2}| = |z_2|.$ Usiamo dunque questa maggiorazione nello sviluppo di $|z_1 + z_2|^2$ della $(3)$ e otteniamo:

$$
\begin{aligned}
|z_1 + z_2|^2 &= |z_1|^2 + 2\mathrm{Re}(z_1\overline{z_2}) + |z_2|^2 \\[6pt]
              &\leq |z_1|^2 + 2|z_1||z_2| + |z_2|^2 \\[6pt]
              &= (|z_1| + |z_2|)^2
\end{aligned}
\tag{5}
$$

Applichiamo ora la radice quadrata ai due membri della disuguaglianza $(5)$ e otteniamo:

$$|z_1 + z_2| = \sqrt{|z_1 + z_2|^2} \leq \sqrt{(|z_1| + |z_2|)^2} = |z_1| + |z_2|$$

Abbiamo così dimostrato la $(1).$

- - -

L'uguaglianza nella $(1)$ equivale all'uguaglianza nella $(5),$ perché la radice quadrata è strettamente crescente sui reali non negativi.

Quando i vettori $z_1$ e $z_2$ non sono allineati, i segmenti che li congiungono all'origine sono i lati adiacenti di un parallelogramma. Il vettore somma $z_1 + z_2$ è la diagonale che per la $(1)$ ha lunghezza che non supera quella del percorso tra gli stessi vertici lungo i lati consecutivi.

![IMG. 1](../svg/triangle-inequality-1.svg)

Applicando la $(1)$ a $z_1$ e $-z_2$ e usando $|-z_2| = |z_2|,$ otteniamo una maggiorazione per il modulo della differenza.

$$|z_1 - z_2| \leq |z_1| + |z_2| \tag{6}$$

![IMG. 2](../svg/triangle-inequality-2.svg)

Il membro sinistro è la lunghezza del segmento che unisce $z_1$ e $z_2.$ Il membro destro è la lunghezza del percorso da $z_1$ a $z_2$ che passa per l'origine.

## Disuguaglianza triangolare inversa

La disuguaglianza triangolare inversa permette di stimare dal basso la distanza tra due numeri complessi $z_1$ e $z_2$ conoscendo soltanto i loro moduli ed è data dalla seguente espressione:

$$\bigl||z_1| - |z_2|\bigr| \leq |z_1 - z_2| \tag{7}$$

Per dimostrare la $(7),$ scriviamo $z_1 = (z_1 - z_2) + z_2$ e applichiamo la $(1)$ ai due addendi, ottenendo:

$$|z_1| \leq |z_1 - z_2| + |z_2| \tag{8}$$

Sottraendo $|z_2|$ da entrambi i membri della $(8)$ otteniamo la prima stima:

$$|z_1| - |z_2| \leq |z_1 - z_2| \tag{9}$$

Se nella $(9)$ scambiamo $z_1$ e $z_2$ e usiamo $|z_2 - z_1| = |z_1 - z_2|,$ otteniamo la seconda stima:

$$|z_2| - |z_1| \leq |z_1 - z_2| \tag{10}$$

La $(9)$ e la $(10)$ mostrano che sia $|z_1| - |z_2|$ sia $|z_2| - |z_1|$ sono minori o uguali a $|z_1 - z_2|.$ La stessa stima vale per il loro massimo, che è $\bigl||z_1| - |z_2|\bigr|.$ In questo modo abbiamo dimostrato la $(7).$

- - -

Per stabilire quando si ha l'uguaglianza nella $(7),$ confrontiamo i quadrati dei suoi membri, che sono entrambi non negativi. Sostituendo $z_2$ con $-z_2$ nella prima riga della $(5)$ e sottraendo il quadrato della differenza dei moduli, otteniamo l'identità seguente.

$$|z_1 - z_2|^2 - (|z_1| - |z_2|)^2 = 2\bigl(|z_1||z_2| - \mathrm{Re}(z_1\overline{z_2})\bigr) \tag{11}$$

Per la $(11),$ i quadrati sono uguali se e solo se $\mathrm{Re}(z_1\overline{z_2}) = |z_1\overline{z_2}|.$ È la stessa condizione di uguaglianza della $(1).$ Nel piano complesso si verifica quando almeno uno dei due numeri è nullo oppure quando entrambi si trovano sulla stessa semiretta uscente dall'origine.

> Dalla $(7)$ segue che il modulo è uniformemente continuo su $\mathbb{C}.$ La $(7)$ dice che la variazione in valore assoluto del modulo non supera la distanza tra i due punti. In questo senso il modulo è lipschitziano con costante $1.$ Per mantenere la variazione del modulo al di sotto di una tolleranza $\varepsilon > 0,$ basta quindi scegliere $\delta = \varepsilon.$ Per ogni coppia $z_1, z_2 \in \mathbb{C}$ con $|z_1 - z_2| < \delta,$ si ha infatti $\bigl||z_1| - |z_2|\bigr| < \varepsilon.$ La stessa soglia $\delta$ vale per tutti i punti del piano complesso.
