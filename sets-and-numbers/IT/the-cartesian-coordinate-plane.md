---
title: The Cartesian Coordinate Plane
source: https://algebrica.org/the-cartesian-coordinate-plane/
license: CC BY-NC 4.0
tags:
  - analytic-geometry
  - cartesian-coordinates
  - distance-formula
  - midpoint
  - plane-geometry
  - symmetry
---

## Costruzione

Se consideriamo una retta reale, sappiamo che ogni suo punto è individuato da un numero. Quando passiamo al piano, invece, per determinare la posizione di un punto abbiamo bisogno di due coordinate. È su questo principio che si basa il concetto di piano cartesiano, costruito a partire da due rette perpendicolari, dette assi cartesiani, che si intersecano nell'origine $O=(0,0),$ l'unico punto in comune tra gli assi. L'asse orizzontale, o asse delle $x$ è chiamato anche asse delle ascisse, mentre l'asse verticale, o asse delle $y,$ è chiamato asse delle ordinate. Scegliamo la stessa unità di lunghezza sui due assi.

Consideriamo ora un generico punto $P$ del piano e tracciamo in corrispondenza del punto le parallele agli assi. La parallela all'asse $y$ incontra l'asse $x$ in un punto $a,$ mentre la parallela all'asse $x$ incontra l'asse $y$ in un punto $b.$ Per identificare il punto $P$ possiamo quindi associargli la coppia ordinata $(a,b),$ e scrivere:

$$P(a,b) \tag{1}$$

Lo stesso ragionamento vale al contrario, ovvero, una volta assegnati due numeri reali $a$ e $b,$ la retta verticale che passa per $(a,0)$ e la retta orizzontale che passa per $(0,b)$ si incontrano in un unico punto che è proprio il nostro punto $P$. In questo modo si ottiene una corrispondenza biunivoca fra tutti i punti del piano e le coppie ordinate di numeri reali che li caratterizzano. L'insieme di queste coppie è dato dal prodotto cartesiano di $\mathbb{R}$ con se stesso, perciò possiamo scrivere:

$$\mathbb{R}^2 = \mathbb{R} \times \mathbb{R} = \{(x,y) \mid x \in \mathbb{R},\ y \in \mathbb{R}\}$$

Abbiamo definito la $(1)$ come coppia ordinata, per cui va ricordato che l'ordine delle coordinate è fondamentale per identificare univocamente il punto. Consideriamo ad esempio i punti $P=(3,2)$ e $Q=(2,3).$ I due punti sono distinti, sebbene nelle coppie compaiano gli stessi numeri. In generale, due coppie individuano lo stesso punto solo quando le coordinate corrispondenti coincidono, ovvero vale la seguente relazione:

$$ (a,b)=(c,d) \quad \Longleftrightarrow \quad a=c \text{ e } b=d $$

Gli assi cartesiani dividono il piano in quattro quadranti, numerati in senso antiorario a partire dalla regione in alto a destra. Nei quadranti valgono le seguenti relazioni:

| Quadrante | Relazione     |
| :-------: | :------------ |
|     I     | $x>0$ e $y>0$ |
|    II     | $x<0$ e $y>0$ |
|    III    | $x<0$ e $y<0$ |
|    IV     | $x>0$ e $y<0$ |

![IMG. 1](../svg/the-cartesian-coordinate-plane-1.svg)

Per esempio, il punto $R(-3,2)$ appartiene al secondo quadrante e vale la seconda relazione $x<0$ e $y>0,$ mentre il punto $S(-3/2,-\sqrt{2})$ si colloca nel terzo quadrante e per esso vale la terza relazione $x<0$ e $y<0$.

## La distanza euclidea 

Una volta individuati due punti sul piano, viene da chiedersi quanto siano distanti tra loro. Per rispondere a questa domanda si ricorre alla distanza euclidea $d(A,B)$ fra $A(x_1,y_1)$ e $B(x_2,y_2)$ che rappresenta la lunghezza del segmento che li congiunge. Quando i punti coincidono, la loro distanza è pari a zero. Supponiamo dapprima che $x_1\ne x_2$ e $y_1\ne y_2.$ Introduciamo ora il punto $H(x_2,y_1)$ e colleghiamo questo punto ai punti $A$ e $B$ ottenendo un triangolo rettangolo in $H.$ Il segmento $AH$ è il cateto orizzontale, mentre il segmento $HB$ è il cateto verticale le cui lunghezze sono:

$$AH=|x_2-x_1| \qquad HB=|y_2-y_1|$$

Applichiamo quindi il [teorema di Pitagora](../pythagorean-theorem/) per ricavare l'ipotenusa che è proprio la distanza che vogliamo determinare tra $A$ e $B$. Ricordiamo che nella determinazione della lunghezza si utilizza il [valore assoluto](../absolute-value/) perché una differenza di coordinate può essere negativa, mentre una lunghezza è sempre non negativa:

$$
\begin{align}
d(A,B)^2 &= |x_2-x_1|^2+|y_2-y_1|^2 \\[6pt]
&= (x_2-x_1)^2+(y_2-y_1)^2 \tag{2}
\end{align}
$$

Dalla $(2)$ ricaviamo $d(A,B)$ prendendo la radice quadrata non negativa, perché una distanza non può essere negativa:

$$d(A,B)=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2} \tag{3}$$

Se $y_1=y_2,$ il segmento è orizzontale e la $(3)$ dà $|x_2-x_1|.$ Se $x_1=x_2,$ il segmento è verticale e la formula dà $|y_2-y_1|.$ Se i punti coincidono, dà zero. La formula vale quindi anche nei casi in cui non si forma un triangolo.

La formula $(3)$ è quindi la formula per ricavare la distanza tra qualunque coppia di punti sul piano. Applichiamola ad un esempio reale, considerando i punti $A=(-3,1)$ e $B=(3,5).$ Per andare da $A$ a $B,$ la variazione orizzontale è $3-(-3)=6,$ mentre quella verticale è $5-1=4.$ La figura mostra il triangolo rettangolo costruito con queste due variazioni.


![IMG. 2](../svg/the-cartesian-coordinate-plane-2.svg)


Il cateto AH ha lunghezza $|3-(-3)|=6$ mentre il cateo $HB$ ha distanza $|5-1| = 4.$ Sostituendo questi valori nella $(3)$ otteniamo:

$$
\begin{align}
d(A,B)&=\sqrt{(3-(-3))^2+(5-1)^2} \\[6pt]
&=\sqrt{36+16}=\sqrt{52}\\[10pt]
&=2\sqrt{13}
\end{align}
$$

La distanza fra i due punti è quindi $2\sqrt{13}.$ Notate che scambiando i punti $A$ e $B,$ le differenze cambiano segno ma i loro quadrati restano uguali e per questo $d(A,B)=d(B,A).$

## Il punto medio

Il punto medio di un generico segmento $AB$ è definito come il punto $M$ del segmento che ha la stessa distanza dai due estremi. Le coordinate di $M$ sono dunque le medie aritmetiche delle coordinate corrispondenti degli estremi:

$$
\begin{align}
x_M&=x_1+\frac{x_2-x_1}{2}=\frac{x_1+x_2}{2} \\[6pt]
y_M&=y_1+\frac{y_2-y_1}{2}=\frac{y_1+y_2}{2}
\end{align}
$$

Possiamo quindi scrivere il punto $M$ come:

$$M=\left(\frac{x_1+x_2}{2},\frac{y_1+y_2}{2}\right) \tag{4}$$

Per ottenere $M,$ partiamo da $A$ e dimezziamo sia lo spostamento orizzontale sia quello verticale necessari per raggiungere $B.$ Questo ci porta a metà strada lungo il segmento $AB,$ quindi $M$ appartiene al segmento.

Per verificare la distanza di $M$ da A possiamo applicare la $(3)$ ottenendo:

$$d(A,M)=\sqrt{\left(\frac{x_2-x_1}{2}\right)^2+\left(\frac{y_2-y_1}{2}\right)^2}=\frac{d(A,B)}{2}$$

Poiché le differenze fra le coordinate di $B$ e quelle di $M$ sono le stesse, lo stesso risultato vale anche per $d(M,B).$ Riprendiamo l'esempio precedente con i punti $A=(-3,1)$ e $B=(3,5)$ e calcoliamo il punto medio applicando la $(4):$

$$M=\left(\frac{-3+3}{2},\frac{1+5}{2}\right)=(0,3)$$

Il punto medio è quindi $M=(0,3).$ Per determinare la distanza di $M$ da $A$ e $B$ sostituiamo le coordinate dei punti alla formula $(3)$ ottenendo:

$$
\begin{align}
d(A,M)&=\sqrt{(0-(-3))^2+(3-1)^2}=\sqrt{13} \\[6pt]
d(M,B)&=\sqrt{(3-0)^2+(5-3)^2}=\sqrt{13}
\end{align}
$$

Come potevamo aspettarci, proprio per la definizione del punto medio, le due distanze sono dunque entrambe $\sqrt{13}.$ La figura illustra il ragionamento fatto:

![IMG. 3](../svg/the-cartesian-coordinate-plane-3.svg)


Naturalmente, il procedimento vale anche al contrario, e cioè se conosciamo $A=(x_1,y_1)$ e il punto medio $M=(u,v),$ dalle uguaglianze $2u=x_1+x_2$ e $2v=y_1+y_2$ possiamo ricavare facilmente l'altro estremo utilizzando la formula:

$$B=(2u-x_1,\ 2v-y_1) \tag{5}$$

Per esempio, da $A=(-3,1)$ e $M=(0,3)$ si ottiene banalmente che l'estremo $B$ è pari a:

$$B=(2\cdot0-(-3),\ 2\cdot3-1)=(3,5)$$

## Simmetria tra punti

Dalla formula $(5)$ possiamo ricavare quella che è definita come simmetria centrale tra due punti. Due punti sono simmetrici rispetto a un centro $C$ quando $C$ è il punto medio del segmento che li congiunge. Ad esempio, se il nostro centro $C$ è l'origine, poniamo $u=v=0$ e otteniamo che il simmetrico del punto $P=(a,b)$ è:

$$P_O=(-a,-b)$$

Geometricamente, questa trasformazione è una rotazione di $180^\circ$ attorno ad $O$. La stessa costruzione vale per un centro qualunque $C=(u,v)$ e dà il punto $(2u-a,\ 2v-b).$

Un ragionamento simile si può fare per la simmetria rispetto agli assi. Se consideriamo l'asse $x,$ la posizione del punto lungo la $x$ rimane invariata mentre quella verticale cambia segno, per cui il simmetrico di un generico punto $P=(a,b)$ è dato da:

$$P_x=(a,-b)$$

Per l'asse $y$ vale invece:

$$P_y=(-a,b)$$

Per fare un esempio pratico, consideriamo il punto $P=(3,2).$ La riflessione rispetto all'asse $x$ dà $P_x=(3,-2),$ quella rispetto all'asse $y$ dà $P_y=(-3,2),$ mentre la simmetria rispetto all'origine dà $P_O=(-3,-2).$ Nella figura i quattro punti sono i vertici di un rettangolo con centro nell'origine.

![IMG. 4](../svg/the-cartesian-coordinate-plane-4.svg)

Come potete notare, se si riflette prima rispetto a un asse e poi rispetto all'altro asse, si ottiene un cambio di segno a entrambe le coordinate che produce la simmetria centrale. L'origine è l'unico punto che rimane fermo nella simmetria rispetto a $O$, perché le condizioni $a=-a$ e $b=-b$ impongono $a=b=0.$

## Considerazioni finali

Le coordinate cartesiane permettono anche di trovare tutta una serie di punti di cui conosciamo alcune proprietà geometriche. Per esempio, fissiamo un centro $C=(a,b)$ e una lunghezza $r>0.$ Per la $(3)$ un qualunque punto $P=(x,y)$ dista $r$ da $C$ se e solo se soddisfa la relazione:

$$\sqrt{(x-a)^2+(y-b)^2}=r$$

Elevando al quadrato otteniamo l'equazione della [circonferenza](../circumference/) di centro $C$ e raggio $r.$

$$ (x-a)^2+(y-b)^2=r^2 $$

Consideriamo un'altra situazione e cerchiamo un punto $E$ sull'asse $x$ che abbia la stessa distanza dai punti $A=(-3,1)$ e $B=(3,5).$ Poiché $E$ appartiene all'asse delle $x$, possiamo scrivere che $E=(t,0).$ Le due distanze sono necessariamente non negative e sono uguali se e solo se sono uguali i loro quadrati. Quindi possiamo scrivere:

$$ (t+3)^2+1=(t-3)^2+25 $$

Svolgendo i calcoli e ricavando $t$ otteniamo:

$$
\begin{align}
t^2+6t+10&=t^2-6t+34 \\[6pt]
12t&=24 \\[6pt]
t&=2
\end{align}
$$

Il punto cercato è quindi $E=(2,0).$ Verificando le distanze otteniamo:

$$
\begin{align}
d(E,A)&=\sqrt{5^2+(-1)^2}=\sqrt{26} \\[6pt]
d(E,B)&=\sqrt{(-1)^2+(-5)^2}=\sqrt{26}
\end{align}
$$

![IMG. 5](../svg/the-cartesian-coordinate-plane-5.svg)

Il punto $E$ è equidistante da $A$ e $B,$ ma non è il punto medio del segmento. Negli esempi svolti abbiamo infatti trovato $M=(0,3),$ che è diverso da $E.$ Questo esempio chiarisce perché nella definizione di punto medio dobbiamo richiedere anche l'appartenenza al segmento.
