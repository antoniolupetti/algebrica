---
title: Integral of the Exponential Function
source: https://algebrica.org/integral-of-the-exponential-function/
license: CC BY-NC 4.0
tags:
  - antiderivative
  - chain-rule
  - error-function
  - exponential-function
  - indefinite-integral
  - integration
  - integration-by-parts
  - integration-by-substitution
  - linearity
  - logarithms
---

## Un richiamo alla funzione esponenziale

Una [funzione esponenziale](../exponential-function/) è una funzione della forma $e^x$ oppure $\alpha^x,$ con $\alpha > 0$ e $\alpha \neq 1.$ Il numero $e$ ha un ruolo centrale nell'analisi perché è l'unica base per cui la derivata della funzione esponenziale coincide con la funzione stessa. Per una generica funzione esponenziale $\alpha^x$ con $\alpha > 0,$ la derivazione infatti introduce un fattore aggiuntivo:

$$\frac{d}{dx}\alpha^x = \alpha^x \ln \alpha$$

Il termine [logaritmico](../logarithms/) esprime come la base scelta influisce sulla crescita della funzione. Questo fattore scompare in un solo caso ovvero quando $\ln \alpha = 1$ e la derivata coincide con la funzione stessa:

$$\frac{d}{dx}\alpha^x = \alpha^x$$

L'unico numero che soddisfa questa condizione è $e,$ perciò $e^x$ è l'unica funzione esponenziale che rimane invariata con la derivazione, e la stessa proprietà si estende all'integrazione. Ciò spiega il ruolo di $e$ nel calcolo differenziale e integrale. 

- - -

Per calcolare l'[integrale](../indefinite-integrals/) di una funzione esponenziale distinguiamo due casi, a seconda che la base sia $e$ oppure un generico numero positivo $\alpha \neq 1.$ L'integrale di $e^x$ è banale ed è dato da:

$$\int e^x \ dx = e^x + c \tag{1}$$

Se deriviamo il secondo membro otteniamo:

$$\frac{d}{dx}\left[e^x + c\right] = \frac{d}{dx}e^x + \frac{d}{dx}c = e^x + 0 = e^x$$

Abbiamo così verificato che $e^x + c$ è una primitiva di $e^x.$ L'integrale di $\alpha^x$ è invece dato da:

$$\int \alpha^x \ dx = \frac{1}{\ln \alpha} \cdot \alpha^x + c \tag{2}$$

Possiamo verificare direttamente anche questa formula nel seguente modo:

$$\frac{d}{dx}\left[ \frac{1}{\ln \alpha} \cdot \alpha^x + c \right] = \frac{1}{\ln \alpha} \cdot (\ln \alpha \cdot \alpha^x) = \alpha^x$$

Il fattore $1/\ln \alpha$ compensa il termine logaritmico prodotto dalla derivazione, e quindi ritroviamo la funzione integranda iniziale.

## Forme canoniche degli integrali esponenziali

Nella tabella seguente sono riportate le primitive delle forme esponenziali più comuni, con l'integrale a sinistra e la corrispondente primitiva a destra. Le costanti $a$ e $b$ sono reali, con $a \neq 0,$ mentre $\alpha > 0$ e $\alpha \neq 1.$ Nell'ultima riga, $f(x)$ è una qualsiasi funzione derivabile. Queste forme coprono i casi che incontriamo più spesso negli esercizi di integrazione.

[class="table-1"]

|    |                                            |                                                                |
| -- | ------------------------------------------ | -------------------------------------------------------------- |
| 1. | $$\int e^x \ dx$$                          | $$e^x + c$$                                                    |
| 2. | $$\int \alpha^x \ dx$$                     | $$\dfrac{1}{\ln \alpha} \alpha^x + c$$                         |
| 3. | $$\int e^{ax + b} \ dx$$                   | $$\dfrac{1}{a} e^{ax + b} + c$$                                |
| 4. | $$\int \alpha^{ax + b} \ dx$$              | $$\dfrac{1}{a \ln \alpha} \alpha^{ax + b} + c$$                |
| 5. | $$\int e^{f(x)} f'(x) \ dx$$               | $$e^{f(x)} + c$$                                               |

[/class]

> Osservate come le formule mostrino che l'integrazione conserva sempre la forma esponenziale. A meno della costante, il termine esponenziale nella primitiva differisce da quello iniziale solo per un fattore costante, che dipende dai coefficienti dell'esponente o dalla base della potenza.

## Esempio 1

Facciamo un primo esempio e calcoliamo il seguente integrale:

$$\int (e^x + 3^x) \ dx$$

Per la proprietà di linearità dell'[integrale indefinito](../indefinite-integrals/), l'integrale di una somma è uguale alla somma degli integrali, perciò possiamo riscriverlo come:

$$\int (e^x + 3^x) \ dx = \int e^x \ dx + \int 3^x \ dx$$

Il primo integrale si calcola banalmente con la formula $(1)$ ed è pari a $e^x + c.$ Per il secondo integrale usiamo la formula $(2)$ con $\alpha = 3$ ottenendo:

$$\int 3^x \ dx = \frac{1}{\ln 3} \cdot 3^x + c$$

Rimettendo insieme i due contributi e sommandoli otteniamo:

$$e^x + \frac{1}{\ln 3} \cdot 3^x + c$$

## Esponenziale con argomento lineare

Nelle applicazioni pratiche si incontrano spesso esponenziali con argomento una funzione lineare $ax + b,$ con $a \neq 0.$ In casi come questo la corrispondente formula di integrazione è:

$$\int e^{ax + b} \ dx = \frac{1}{a} e^{ax + b} + c \tag{3}$$

Il fattore $1/a$ compensa il coefficiente introdotto dalla [regola di derivazione delle funzioni composte](../chain-rule/). Per verificarlo, deriviamo il secondo membro e otteniamo:

$$\frac{d}{dx}\left[ \frac{1}{a} e^{ax + b} + c \right] = \frac{1}{a} \cdot a \cdot e^{ax + b} = e^{ax + b}$$

Come era intuibile, il risultato coincide con la funzione integranda iniziale. Quando l'esponente è una funzione derivabile $f(x),$ possiamo generalizzare la formula $(3)$ mediante il metodo di [integrazione per sostituzione](../integration-by-substitution/):

$$\int e^{f(x)} \cdot f'(x) \ dx = e^{f(x)} + c$$

Nell'integranda deve comparire l'esponenziale $e^{f(x)}$ moltiplicata per la derivata del suo esponente. In questa situazione l'integrazione è immediata e la primitiva è $e^{f(x)} + c.$ Se il fattore $f'(x)$ non compare nell'integranda, prima di applicare la regola dobbiamo ricondurci a questa forma con una manipolazione algebrica o una sostituzione adatta.

Lo stesso ragionamento si estende alle funzioni esponenziali con una base generica $\alpha.$ Quando l'esponente è $ax + b$ anziché $x,$ la derivazione produce due fattori, il coefficiente $a$ dovuto all'esponente e $\ln \alpha$ dovuto alla base. Otteniamo quindi la seguente formula:

$$\int \alpha^{ax + b} \ dx = \frac{1}{a \ln \alpha} \alpha^{ax + b} + c$$

Espressioni di questo tipo compaiono spesso nei passaggi intermedi, quando scomponiamo integrali più complicati cercando di ricondurli ad integrali elementari.

## Esempio 2

Calcoliamo il seguente integrale, in cui compare il prodotto di due termini esponenziali con basi diverse:

$$\int 8^x \cdot 2^{-3x + 4} \ dx$$

Possiamo semplificare l'integranda applicando le [proprietà delle potenze](../powers/). Nel secondo fattore separiamo i termini dell'esponente di $2$ e scriviamo:

$$2^{-3x + 4} = 2^{-3x} \cdot 2^4 = 16 \cdot 2^{-3x}$$

Sostituendo questa identità nell'integrale e portando fuori la costante otteniamo:

$$\int 8^x \cdot 2^{-3x + 4} \ dx = 16 \int 8^x \cdot 2^{-3x} \ dx$$

Possiamo riscrivere la base $8$ come potenza di $2$ cosicché l'integranda si riduce a un'unica potenza di $2:$

$$
\begin{align}
16 \int 8^x \cdot 2^{-3x} \ dx &= 16 \int (2^3)^x \cdot 2^{-3x} \ dx \\[6pt]
                               &= 16 \int 2^{3x} \cdot 2^{-3x} \ dx \\[6pt]
                               &= 16 \int 2^{3x - 3x} \ dx \\[6pt]
                               &= 16 \int 1 \ dx\\[6pt]
                               &= 16x + c
\end{align}
$$

> Come abbiamo visto, una volta ricondotti i due fattori esponenziali alla stessa base, l'integranda si semplifica e rimane soltanto da integrare una costante.

## Esempio 3

Consideriamo adesso il seguente integrale, in cui entrambi i fattori sono esponenziali con argomenti lineari e basi che possiamo ricondurre a una base comune:

$$\int 9^{x - 1} \cdot 3^{-x + 2} \ dx$$

Con le proprietà delle potenze possiamo separare i termini dei due esponenti e scrivere:

$$9^{x - 1} \cdot 3^{-x + 2} = 9^x \cdot 9^{-1} \cdot 3^{-x} \cdot 3^2$$

Facendo dei calcoli banali l'integranda diventa:

$$9^x \cdot 3^{-x}$$

Riscrivendo $9^x$ come $3^{2x},$ possiamo riunire il prodotto dei due fattori esponenziali di base $3$ in un'unica potenza:

$$9^x \cdot 3^{-x} = 3^{2x} \cdot 3^{-x} = 3^{2x - x} = 3^x$$

L'integrale si riconduce quindi alla forma canonica $\int \alpha^x \ dx$ con $\alpha = 3:$

$$\int 9^{x - 1} \cdot 3^{-x + 2} \ dx = \int 3^x \ dx$$

Applicando la formula $(2)$ otteniamo il risultato:

$$\frac{1}{\ln 3} \cdot 3^x + c$$

> Nella risoluzione di questo genere di integrali, il passaggio fondamentale è la riduzione a una base comune. Quando esprimiamo entrambi i fattori come potenze di una stessa base l'integranda diventa un'unica esponenziale e l'integrazione è immediata.

## Esempio 4

Facciamo un ulteriore esempio e proviamo a calcolare il seguente integrale in cui l'esponente è una funzione lineare di $x$:

$$\int e^{3x - 2} \ dx$$

Come sappiamo possiamo applicare direttamente la regola per le esponenziali della forma $e^{ax + b}.$ La derivata di $3x - 2$ è $3,$ perciò nella primitiva dobbiamo introdurre il fattore $1/3:$

$$\int e^{3x - 2} \ dx = \frac{1}{3} e^{3x - 2} + c$$

Verifichiamo il risultato derivando il secondo membro:

$$\frac{d}{dx}\left[ \frac{1}{3} e^{3x - 2} + c \right] = \frac{1}{3} \cdot 3 \cdot e^{3x - 2} = e^{3x - 2}$$

La derivazione restituisce l'integranda iniziale, quindi la primitiva ottenuta è coerente con la regola di integrazione.


## Esempio 5

Consideriamo ora il seguente integrale, in cui l'esponente non è più una funzione lineare di $x$ ma una funzione quadratica.

$$\int x e^{x^2} \ dx$$

In questo caso non possiamo applicare direttamente la regola per le esponenziali della forma $e^{ax + b}.$ La forma dell'integranda ci suggerisce però come procedere. La derivata di $x^2$ è $2x$ e nell'integranda compare già un fattore $x.$ Moltiplicando e dividendo per $2$ introduciamo la costante mancante senza modificare il valore dell'integrale:

$$\int x e^{x^2} \ dx = \frac{1}{2} \int 2x e^{x^2} \ dx$$

L'integranda ha adesso la forma canonica $e^{f(x)} f'(x)$ con $f(x) = x^2,$ quindi possiamo applicare la formula della riga $(5)$ della tabella e integrare direttamente:

$$\int x e^{x^2} \ dx = \frac{1}{2} e^{x^2} + c$$

Verifichiamo il risultato derivando il secondo membro:

$$\frac{d}{dx}\left[ \frac{1}{2} e^{x^2} + c \right] = \frac{1}{2} \cdot 2x \cdot e^{x^2} = x e^{x^2}$$

La derivazione restituisce l'integranda iniziale e conferma quindi la primitiva ottenuta.

## Quando manca il fattore corrispondente alla derivata

Facciamo adesso una breve incursione in un argomento più avanzato solo per completezza illustrativa. Per capire il ruolo del fattore $x$ nell'esempio precedente, vediamo cosa succede se lo togliamo. L'integrale diventerebbe:

$$\int e^{x^2} \ dx$$

Questo integrale non ammette una primitiva esprimibile mediante funzioni elementari. Le sue primitive si scrivono convenzionalmente in termini della cosiddetta funzione degli errori immaginaria $\mathrm{erfi}(x),$ definita da:

$$\mathrm{erfi}(x) = \frac{2}{\sqrt{\pi}} \int_0^x e^{t^2} \ dt$$

Questa non è una funzione elementare, cioè non si può ottenere da polinomi, esponenziali, logaritmi e funzioni trigonometriche mediante una combinazione finita di operazioni algebriche. Il [teorema fondamentale del calcolo integrale](../fundamental-theorem-of-calculus/) permette però di ricavarne la derivata direttamente dall'integrale che la definisce. Derivando ripetutamente possiamo inoltre verificare che è derivabile infinite volte.

Il confronto con l'esempio $5$ chiarisce il ruolo del fattore $x.$ Quindi, ricapitolando, nell'integrale $\int x e^{x^2} \ dx$ il fattore $x$ fornisce, a meno della costante $1/2,$ la derivata dell'esponente $x^2.$ L'integranda ha la forma canonica $e^{f(x)} f'(x)$ e la primitiva è elementare. Quando il fattore $x$ manca, questa corrispondenza viene meno e l'integrale non rientra più tra quelli risolvibili con tecniche elementari e al momento è fuori dal nostro ambito.

> Quando non abbiamo una forma chiusa elementare, possiamo comunque approssimare il corrispondente [integrale definito](../definite-integrals/) mediante l'[integrazione numerica](../numerical-integration/), come nel caso di $\int e^{x^2} \ dx$ su un intervallo finito.

## Integrazione per parti con fattori esponenziali

Diversi integrali che contengono la funzione esponenziale non si possono ricondurre a una forma canonica con le sole manipolazioni algebriche. Quando l'integranda è il prodotto di un'esponenziale e un polinomio, oppure di un'esponenziale e un'altra funzione trascendente, possiamo procedere in modo sistematico con l'[integrazione per parti](../integration-by-parts/). Il metodo si basa sulla formula:

$$\int u(x) v'(x) \ dx = u(x) v(x) - \int u'(x) v(x) \ dx$$

Quando compare un fattore esponenziale, in genere conviene porre $v'(x) = e^{ax + b},$ perché come sappiamo l'esponenziale rimane invariata con l'integrazione a meno di un fattore costante, mentre l'altro fattore viene derivato e progressivamente semplificato.

- - -

Il caso più semplice si presenta quando l'integranda è il prodotto di un polinomio di primo grado e un'esponenziale. Calcoliamo ad esempio il seguente integrale:

$$\int x e^x \ dx$$

Poniamo $u(x) = x$ e $v'(x) = e^x,$ da cui otteniamo $u'(x) = 1$ e $v(x) = e^x.$ Sostituendo i valori nella formula di integrazione per parti possiamo scrivere:

$$\int x e^x \ dx = x e^x - \int e^x \ dx = x e^x - e^x + c$$

Raccogliendo il fattore esponenziale otteniamo:

$$\int x e^x \ dx = (x - 1) e^x + c$$

Derivando direttamente il risultato ritroviamo l'integranda iniziale e verifichiamo la primitiva:

$$\frac{d}{dx}\left[ (x - 1) e^x + c \right] = e^x + (x - 1) e^x = x e^x$$

- - -

Quando il fattore [polinomiale](../polynomials/) ha grado maggiore di $1,$ una sola applicazione della formula non basta e dobbiamo ripetere il procedimento più volte. Consideriamo ad esempio il seguente integrale:

$$\int x^2 e^x \ dx$$

Poniamo $u(x) = x^2$ e $v'(x) = e^x.$ La prima applicazione della formula dà:

$$\int x^2 e^x \ dx = x^2 e^x - \int 2x e^x \ dx$$

L'integrale rimasto ha la stessa forma di quello dell'esempio precedente e lo abbiamo già calcolato. Sostituendo il risultato otteniamo:

$$\int x^2 e^x \ dx = x^2 e^x - 2(x - 1) e^x + c = (x^2 - 2x + 2) e^x + c$$

Lo stesso ragionamento si estende a un qualsiasi polinomio $P(x)$ di grado $n.$ Dopo $n$ applicazioni successive dell'integrazione per parti, il fattore polinomiale si riduce a una costante e il calcolo si conclude. La [relazione di ricorrenza generale](../reduction-formulas/) è esprimibile attraverso la seguente relazione:

$$\int x^n e^x \ dx = x^n e^x - n \int x^{n - 1} e^x \ dx$$

Questa uguaglianza esprime l'integrale di $x^n e^x$ mediante quello di $x^{n - 1} e^x$ e permette di ottenere una primitiva in forma chiusa con un numero finito di passaggi.

- - -

Un'ulteriore variante si presenta quando l'esponente è una funzione lineare di $x.$ Possiamo applicare lo stesso metodo applicato sopra, ricordando di introdurre il fattore $1/a$ nella primitiva di $e^{ax + b}.$ Calcoliamo quindi l'integrale:

$$\int x e^{2x} \ dx$$

Poniamo $u(x) = x$ e $v'(x) = e^{2x}.$ Una primitiva di $v'(x)$ è $v(x) = 1/2 \cdot e^{2x}$ e applicando la formula di integrazione per parti otteniamo:

$$\int x e^{2x} \ dx = \frac{x}{2} e^{2x} - \int \frac{1}{2} e^{2x} \ dx = \frac{x}{2} e^{2x} - \frac{1}{4} e^{2x} + c$$

Raccogliendo il termine esponenziale otteniamo il risultato:

$$\frac{1}{4} e^{2x} (2x - 1) + c$$

Il coefficiente $a = 2$ nell'esponente non cambia il procedimento ma introduce soltanto il fattore $1/2$ a ogni passaggio di integrazione, di cui ritroviamo l'effetto nell'espressione finale.