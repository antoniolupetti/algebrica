---
title: Powers
source: https://algebrica.org/powers/
license: CC BY-NC 4.0
tags:
  - exponential
  - exponents
  - logarithms
  - power-rules
  - powers
---
## Introduzione

La potenza $a^n$ di un numero reale $a$ (detto base) e un intero positivo $n$ (detto esponente) è il prodotto di $n$ fattori uguali ad $a:$

$$a^n = \underbrace{a \cdot a \cdots a}_{n \text{ volte}}\tag{1}$$

Le potenze con esponente intero estendono la definizione $(1)$ anche agli esponenti nulli e negativi. Quando $a \neq 0$ e per ogni intero positivo $n,$ una potenza con esponente negativo è definita dal reciproco:

$$a^{-n} = \frac{1}{a^{n}} \tag{2}$$

Quando $a > 0$ e per ogni intero positivo $m,$ una potenza con esponente della forma $1/m$ è definita mediante un radicale:

$$a^{\frac{1}{m}} = \sqrt[m]{a} \tag{3}$$

Combinando la $(2)$ e la $(3)$ possiamo ottenere la seguente identità:

$$a^{-\frac{1}{m}} = \frac{1}{\sqrt[m]{a}} \tag{4}$$

La tabella seguente riporta alcuni valori di $a^n.$ Ogni riga corrisponde a una base $a$ fissata e ogni colonna a un esponente $n$ fissato.

|      | $a^{-2}$ | $a^{-1}$ | $a^{0}$ | $a^{1}$ | $a^{2}$ | ... |
| :--: | :------: | :------: | :-----: | :-----: | :-----: | :-: |
| $-2$ |  $1/4$   |  $-1/2$  |   $1$   |  $-2$   |   $4$   | ... |
| $-1$ |   $1$    |   $-1$   |   $1$   |  $-1$   |   $1$   | ... |
| $0$  | non definita | non definita | non definita |   $0$   |   $0$   | ... |
| $1$  |   $1$    |   $1$    |   $1$   |   $1$   |   $1$   | ... |
| $2$  |  $1/4$   |  $1/2$   |   $1$   |   $2$   |   $4$   | ... |
| ...  |   ...    |   ...    |   ...   |   ...   |   ...   | ... |

Consideriamo nello specifico il caso di una base negativa. In questo caso l'esponente determina sia l'esistenza di un valore reale della potenza sia il suo segno. Infatti quando $a \lt 0$ e $n$ è intero, il segno di $a^n$ dipende dalla parità di $n.$ Per esempio, $(-1)^n$ è pari a $1$ quando $n$ è pari a $-1$ quando $n$ è dispari. Quando $a < 0$ e all'esponente abbiamo una frazione $p/q$ è ridotta ai minimi termini e con $q > 0,$ allora $a^{p/q}$ ha un valore reale se e solo se $q$ è dispari. Quindi $(-8)^{1/3} = -2,$ mentre $(-1)^{1/2}$ non ha valore in $\mathbb{R}.$

- - -

È importante sottolineare che la $(1)$ definisce $a^n$ solo quando $n$ è un intero positivo, ma quando dobbiamo definire le potenze con un esponente reale dobbiamo ricorrere alla funzione esponenziale e al logaritmo naturale, nel seguente modo. Considerando una base $a > 0$ e $x \in \mathbb{R},$ vale:

$$a^x = e^{x \ln a} \tag{5}$$

Questa definizione coincide con la $(1)$ nel caso di esponenti interi positivi e con i radicali per gli esponenti razionali. Se $p \in \mathbb{Z}$ e $q$ è un intero positivo, si ha infatti:

$$a^{p/q} = e^{\frac{p}{q}\ln a} = \sqrt[q]{a^p} \tag{6}$$

La stessa definizione permette di calcolare potenze con esponente irrazionale, come:

$$2^{\sqrt{2}} = e^{\sqrt{2}\ln 2} \approx 2.665$$

In questo caso, la base deve essere positiva perché il logaritmo è definito nei reali solo quando il suo argomento è maggiore di zero.

## Proprietà delle potenze

Le proprietà fondamentali delle potenze consentono di riscrivere le espressioni in forme equivalenti e semplificare i calcoli. Iniziamo dal considerare una base non nulla elevata a un esponente pari a zero. Per qualsiasi base $a \gt 0$ si ha la seguente relazione:

$$a^0 = 1 \tag{7}$$
Come si può vedere anche dalla tabella sopra, le potenze di zero con esponente negativo non sono definite, perché richiederebbero una divisione per zero. Anche $0^0$ è non definito perché non è possibile assegnargli un valore che renda continua la funzione potenza nell'origine $(0,0).$ È utile ricordare che, nel calcolo dei limiti, $0^0$ è una forma indeterminata che non si risolve per sostituzione diretta ma attraverso opportune tecniche illustrate nella pagina dedicata all'argomento. Nel calcolo combinatorio e nell'algebra si adotta la seguente convenzione che mantiene valide le formule come quella del teorema binomiale, consentendo di valutare termini con esponente paria a zero anche quando una delle basi è nulla:

$$0^0=1 \tag{8}$$

Per un intero positivo $n,$ la potenza $0^n$ è un prodotto di $n$ zeri e più in generale nel caso di esponenti reali positivi l'espressione $0^x$ è definite come:

$$0^x = 0 \tag{9}$$
- - -

Vediamo ora un'ulteriore proprietà che riguarda il prodotto di due potenze con la stessa base $a.$ In questo caso vale la seguente identità:

$$a^n \cdot a^m = a^{n+m} \tag{10}$$

La $(10)$ si può dimostrare facilmente richiamando la definizione $(1).$ Quando l'esponente è un intero positivo, $a^n$ è il prodotto di $n$ fattori uguali ad $a$ e $a^m$ è il prodotto di $m$ fattori sempre uguali a $a$. Per questo otteniamo $n+m$ fattori pari alla base $a$ che possiamo scrivere come:

$$ \tag{11}
a^n \cdot a^m = \underbrace{a \cdot a \cdots a}_{n \text{ volte}} \cdot \underbrace{a \cdot a \cdots a}_{m \text{ volte}} = \underbrace{a \cdot a \cdots a}_{n+m \text{ volte}} = a^{n+m}
$$

Per esponenti reali arbitrari e con $a > 0,$  dalle identità $(5)$ si ottiene:

$$a^n \cdot a^m = e^{n \ln a} \cdot e^{m \ln a} = e^{(n+m) \ln a} = a^{n+m}\tag{12}$$

Quando il prodotto delle potenze coinvolge basi diverse con uno stesso esponente, per $a,b > 0$ e $n \in \mathbb{R}$ vale la seguente identità:

$$a^{n} \cdot b^n = (ab)^n\tag{13}$$

- - -

Nel caso del quoziente di due potenze con la stessa base $a$ vale la seguente relazione.

$$\frac{a^n}{a^m} = a^{n-m} \tag{14}$$

Questa proprietà segue direttamente dalla $(10).$ Infatti, dividere per $a^m$ equivale a moltiplicare per $a^{-m},$ e quindi possiamo riscrivere la $(14)$ come:

$$\frac{a^n}{a^m} = a^n \cdot a^{-m} = a^{n+(-m)} = a^{n-m}$$

Naturalmente la $(14)$ richiede $a \neq 0$ affinché il denominatore $a^m$ e il suo reciproco siano definiti. Quando il quoziente coinvolge basi diverse con lo stesso esponente $n,$ per $a,b > 0$ e $n \in \mathbb{R}$ otteniamo una situazione speculare alla $(13):$

$$\frac{a^n}{b^n} = \left(\frac{a}{b}\right)^n \tag{15}$$

- - -

Nel caso invece di una potenza di potenza, per $a > 0$ e $m,n \in \mathbb{R}$ vale la seguente relazione che moltiplica gli esponenti:

$$(a^m)^n = a^{m \cdot n}\tag{16}$$

Quando l'esponente è un razionale, la potenza può essere espressa mediante un radicale come abbiamo visto nella $(3)$. Quando abbiamo $a \gt 0,$  $m \in \mathbb{Z}$ e $n \in \mathbb{N}$ e $n\gt 0,$ otteniamo:

$$a^{\frac{m}{n}} = \sqrt[n]{a^m} \tag{17}$$

- - -

Richiamando la proprietà $(14),$ possiamo dimostrare perché $a^0=1.$ Partiamo dalla seguente identità:

$$\frac{a^n}{a^n} = 1$$

Riscrivendola come differenza degli esponenti otteniamo:

$$\frac{a^n}{a^n} = a^{n-n} = a^0 = 1$$

Infine facciamo un riferimento alla disuguaglianza di Bernoulli che fornisce una stima dal basso per la potenza $(1+x)^n,$ affermando che $(1+x)^n \ge 1+nx$ per $x \ge -1$ e per ogni intero positivo $n$ e la cui trattazione è rimandata ad una voce dedicata.

## Potenze con esponente complesso

Fino ad ora abbiamo considerato potenze con esponente reale, ma possiamo definire anche potenze con esponente nel campo dei numeri complessi. Consideriamo una base $a > 0$ e $z \in \mathbb{C},$ e definiamo una potenza con esponente complesso come:

$$a^z = e^{z \ln a} \tag{18}$$

Per ricavare la 18 usiamo la serie di Taylor dell'esponenziale reale, che converge per ogni $w \in \mathbb{C}:$

$$e^w = \sum_{n=0}^{\infty} \frac{w^n}{n!}$$

Quando $w = i\theta,$ con $\theta \in \mathbb{R},$ i termini con potenze pari di $i$ formano la serie del coseno, mentre quelli con potenze dispari formano $i$ volte la serie del seno, ottenendo la formula di Eulero:

$$e^{i\theta} = \cos\theta + i\sin\theta \tag{19}$$

Grazie alla $(19)$ possiamo calcolare la potenza definita nella $(18).$ Infatti, riscrivendo $z = u+iv,$ con $u,v \in \mathbb{R},$ otteniamo:

$$a^{u+iv} = e^{u\ln a}e^{iv\ln a} = a^u\bigl(\cos(v\ln a) + i\sin(v\ln a)\bigr)$$

La parte reale della potenza è $a^u\cos(v\ln a),$ mentre $a^u\sin(v\ln a)$ è la parte immaginaria. Nel caso particolare di $\theta = \pi,$ la formula di Eulero dà $e^{i\pi} = -1,$ da cui segue l'identità di Eulero:

$$e^{i\pi} + 1 = 0 \tag{20}$$

La formula di Eulero permette anche di scrivere ogni numero complesso non nullo nella forma $re^{i\theta},$ dove $r > 0$ è il suo modulo e $\theta$ è un argomento, definito modulo $2\pi.$ Questa rappresentazione e i metodi per calcolare potenze e radici di numeri complessi sono trattati nella pagina sui numeri complessi in forma esponenziale.
