---
title: Lagrange's Theorem for Finite Groups
source: https://algebrica.org/lagrange-theorem-for-finite-groups/
license: CC BY-NC 4.0
tags:
  - coset
  - finite-group
  - group-theory
  - lagrange-theorem
  - subgroup
  - subgroup-index
---

## Enunciato

Il teorema di Lagrange per i gruppi finiti afferma che, dato un generico gruppo finito $G,$ l'ordine di ogni suo sottogruppo $H$ divide l'ordine di $G$ e il quoziente è l'indice $[G : H],$ ossia il numero dei laterali sinistri distinti di $H$ in $G.$ Per laterale sinistro di $H$ si intende l'insieme dei prodotti che si ottengono fissando un elemento $a \in G$ e moltiplicando a sinistra per $a$ ogni elemento di $H$ che è dato da:

$$aH = \{ah \mid h \in H\} \tag{1}$$

Per esempio, nel gruppo additivo $\mathbb{Z}/6\mathbb{Z}$ il sottogruppo $H = \{0, 2, 4\}$ ha due laterali. Il primo è $H$ stesso, mentre il secondo è $1 + H = \{1, 3, 5\}.$ Per Lagrange, vale quindi la seguente identità:

$$|G| = [G : H]|H| \tag{2}$$

Per dimostrare la $(2)$ bisogna provare che ogni laterale sinistro di $H$ contiene $|H|$ elementi e che i laterali distinti formano una partizione di $G.$ Per il primo punto, fissiamo $a \in G.$ L'applicazione $h \mapsto ah$ è una biiezione da $H$ ad $aH,$ perché la sua inversa associa a ogni $x \in aH$ l'elemento $a^{-1}x \in H.$ Da questo segue che:

$$|aH| = |H| \tag{3}$$

Per il secondo punto, ogni $a \in G$ appartiene ad $aH$ perché $a = ae$ ed $e \in H.$ Per stabilire che i laterali distinti sono disgiunti, supponiamo che $aH$ e $bH$ abbiano un elemento in comune. Possiamo scriverlo sia come $ah_1$ sia come $bh_2,$ con $h_1, h_2 \in H.$ Moltiplicando l'uguaglianza $ah_1 = bh_2$ a sinistra per $b^{-1}$ e a destra per $h_1^{-1}$ otteniamo la seguente identità:

$$b^{-1}a = h_2h_1^{-1} \in H \tag{4}$$

La $(4)$ vale in particolare se $aH = bH,$ perché in tal caso entrambi i laterali contengono $a.$ Viceversa, se $k = b^{-1}a$ appartiene a $H,$ la moltiplicazione a sinistra per $k$ è una biiezione di $H$ su sé stesso, perciò $kH = H.$ Da $a = bk$ segue allora $aH = b(kH) = bH.$ L'appartenenza di $b^{-1}a$ a $H$ è dunque necessaria e sufficiente per l'uguaglianza dei laterali per cui si ha:

$$aH = bH \iff b^{-1}a \in H \tag{5}$$

Se due laterali hanno un elemento in comune, soddisfano la $(4)$ e quindi per la $(5)$ coincidono. I laterali distinti sono quindi disgiunti e poiché il loro numero è $[G : H]$ per definizione di indice e ciascuno contiene $|H|$ elementi per la $(3)$, contando gli elementi di $G$ si ottiene proprio la $(2)$ e il teorema è dimostrato.

Per la $(2),$ se $G$ contiene un sottogruppo di ordine $d,$ allora $d$ divide $|G|.$ Ci si può chiedere se, viceversa, ogni divisore di $|G|$ sia l'ordine di un sottogruppo di $G.$ Il gruppo alterno $A_4,$ formato dalle permutazioni pari di quattro elementi, fornisce un controesempio. Ha ordine $12$ e, sebbene $6$ divida $12,$ nessuno dei suoi sottogruppi ha ordine $6.$

- - -

Il teorema di Lagrange lega l'ordine di ogni sottogruppo all'ordine di $G.$ Questo legame riguarda anche i singoli elementi, perché l'ordine di un elemento $a \in G$ coincide con l'ordine del sottogruppo ciclico che esso genera. Se indichiamo con $d$ questo ordine e poniamo $H = \langle a \rangle$ nella $(2),$ otteniamo

$$|G| = [G : \langle a \rangle]d \tag{6}$$

La $(6)$ mostra che l'ordine di $a$ divide l'ordine di $G.$ Se indichiamo con $k$ l'indice $[G : \langle a \rangle],$ possiamo quindi scrivere che $|G| = kd$ e poiché $a^d = e$ per definizione di ordine, segue che:

$$a^{|G|} = (a^d)^k = e \tag{7}$$

La $(7)$ vale per ogni elemento di $G.$ Un gruppo si dice di ordine primo quando il numero $p$ dei suoi elementi è un numero primo. In questo caso la $(6)$ mostra che l'ordine di ciascun elemento divide $p,$ quindi può essere soltanto $1$ oppure $p.$ Poiché solo l'elemento neutro ha ordine $1,$ ogni $a \neq e$ ha ordine $p$ e genera un sottogruppo che contiene tutti i $p$ elementi di $G.$ Ne segue che $G$ è ciclico e isomorfo al gruppo additivo $\mathbb{Z}/p\mathbb{Z}.$
