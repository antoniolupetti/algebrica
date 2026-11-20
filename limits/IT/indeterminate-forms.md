---
title: Indeterminate Forms
source: https://algebrica.org/indeterminate-forms/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - hopital-rule
  - indeterminate-forms
  - limits
  - taylor-series
---

## Che cosa sono le forme indeterminate

Nel calcolo dei limiti si incontrano spesso espressioni in cui il valore del limite non può essere determinato direttamente, dette forme indeterminate, le cui tipologie esaustive sono riportate di seguito:

$$
\begin{align}
&\frac{0}{0} \qquad \frac{\infty}{\infty} \qquad 0 \cdot \infty \qquad \infty - \infty \notag \\[6pt]
&1^{\infty} \qquad 0^{0} \qquad \infty^{0} \tag{1}
\end{align}
$$

In termini molto semplici, una forma di quelle della $(1)$ non indica un numero specifico ma segnala che la sostituzione diretta non è utile per calcolare il relativo limite. Supponiamo, per esempio, di avere due funzioni $f(x)$ e $g(x)$ che tendono entrambe a zero quando $x$ si avvicina ad $a$:

$$
\begin{align}
\lim_{x \to a} f(x) &= 0 \notag \\[6pt]
\lim_{x \to a} g(x) &= 0 \tag{2}
\end{align}
$$

Se volessimo calcolare il limite del loro rapporto per sostituzione diretta otterremmo un risultato indeterminato, che non ci dice nulla sul comportamento del limite:

$$\lim_{x \to a} \frac{f(x)}{g(x)} \to \frac{0}{0} \tag{3}$$

Nella $(3)$ il limite potrebbe essere un qualunque numero finito, zero, infinito, oppure potrebbe anche non esistere affatto e quindi, quando ci si trova davanti a queste forme, è necessario agire diversamente con una serie di tecniche che sono elencate di seguito. Prima di analizzare ciascuna forma, occorre tenere presente che una forma indeterminata come quelle della $(1)$ non rappresenta un numero, né esprime un'uguaglianza, ma è solamente una sorta di indicatore che ci segnala che il comportamento del limite deve essere approfondito in altro modo.

## La forma $\frac{0}{0}$

Questa è la forma indeterminata che si incontra più spesso negli esercizi e compare tipicamente quando numeratore e denominatore si annullano nello stesso punto. A volte, per risolverla, è possibile semplificare l'espressione del limite mediante alcuni passaggi algebrici prima di procedere al calcolo. Consideriamo, per esempio, il seguente limite:

$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} \tag{4}$$

Nella $(4)$ la sostituzione diretta di $x=2$ dà proprio $0/0$ e quindi non possiamo concludere nulla sul comportamento del limite. Possiamo però aggirare questo problema scomponendo il numeratore come differenza di due quadrati:

$$x^2 - 4 = (x - 2)(x + 2) \tag{5}$$

Sostituendo la $(5)$ nella $(4)$ e imponendo $x \neq 2,$ otteniamo:

$$
\begin{align}
&\lim_{x \to 2} \frac{(x - 2)(x + 2)}{x - 2} \notag \\[6pt]
& \lim_{x \to 2} (x + 2) = 2 + 2 = 4 \tag{6}
\end{align}
$$

Nei problemi più avanzati, la regola di de l'Hôpital fornisce un metodo sistematico per risolvere questo tipo di limite, mentre in altri casi occorre utilizzare gli sviluppi di Taylor o la notazione di o piccolo con l'obiettivo di isolare il termine dominante del numeratore e del denominatore. Queste tecniche sono sviluppate nel dettaglio nelle rispettive voci.

## La forma $\dfrac{\infty}{\infty}$

Vediamo ora come trattare questa forma che si presenta quando il numeratore e il denominatore di un rapporto divergono. Consideriamo, per esempio, il seguente limite:

$$\lim_{x \to \infty} \frac{3 x^2 + 1}{2 x^2 - 5} \tag{7}$$

Anche in questo caso, una sostituzione diretta porta alla forma indeterminata $\infty/\infty$ e come nell'esempio precedente non possiamo dire nulla sul valore del limite. Possiamo però provare a risolvere la $(7)$ applicando qualche trasformazione algebrica, ad esempio raccogliendo la potenza di grado massimo di $x$ al numeratore e al denominatore, ottenendo:

$$
\begin{align}
\frac{3 x^2 + 1}{2 x^2 - 5}
&= \frac{x^2 (3 + 1/x^2)}{x^2 (2 - 5/x^2)} \notag \\[6pt]
&= \frac{3 + 1/x^2}{2 - 5/x^2} \tag{8}
\end{align}
$$

Quando $x \to \infty,$ i termini $1/x^2$ e $5/x^2$ tendono a zero e quindi il limite diventa:

$$\lim_{x \to \infty} \frac{3 x^2 + 1}{2 x^2 - 5} = \frac{3}{2}$$

In alcune circostanze si può ottenere il medesimo risultato più rapidamente iterando la regola di de l'Hôpital, ma tenete comunque in mente che una volta acquisito il metodo, il procedimento di risoluzione del limite diventa piuttosto meccanico e si riduce a pochi e immediati passaggi.

## La forma $0 \cdot \infty$

Questa forma si presenta quando nel limite compare un prodotto tra due fattori di cui uno tende a zero mentre l'altro cresce illimitatamente. Per esempio, consideriamo il seguente limite:

$$\lim_{x \to +\infty} x\left(\sqrt{x^2 + 1} - x\right) \tag{9}$$

Nella $(9),$ il fattore $x$ tende a $+\infty,$ mentre $\sqrt{x^2 + 1} - x$ tende a zero, perché razionalizzando questa differenza si ottiene $1/(\sqrt{x^2 + 1} + x).$ Il prodotto presenta quindi la forma $0 \cdot \infty.$ Anche in questo caso possiamo utilizzare un semplice trucco algebrico, scrivendo $x = 1/(1/x),$ ed esprimendo la $(9)$ come quoziente:

$$x\left(\sqrt{x^2 + 1} - x\right) = \frac{\sqrt{x^2 + 1} - x}{1/x} \tag{10}$$

Nella $(10),$ numeratore e denominatore tendono entrambi a zero e quindi otteniamo la forma $0/0$ vista in precedenza. In questo caso possiamo razionalizzare il numeratore e raccogliere $x$ al denominatore, tenendo conto che $x \gt 0,$ in modo da ottenere:

$$
\begin{align}
\frac{\sqrt{x^2 + 1} - x}{1/x}
&= \frac{(x^2 + 1) - x^2}{(1/x)\left(\sqrt{x^2 + 1} + x\right)} \notag \\[6pt]
&= \frac{1}{(1/x)x\left(\sqrt{1 + 1/x^2} + 1\right)} \notag \\[6pt]
&= \frac{1}{\sqrt{1 + 1/x^2} + 1} \tag{11}
\end{align}
$$

Nella $(11),$ il termine $1/x^2$ tende a zero e il denominatore tende a $2$ e in questo modo possiamo finalmente calcolare il limite come segue:

$$\lim_{x \to +\infty} \frac{1}{\sqrt{1 + 1/x^2} + 1} = \frac{1}{2} \tag{12}$$

I casi come quello appena visto si risolvono semplicemente trasformando il prodotto in quoziente, se si è fortunati, procedendo a calcolare il limite già dopo un primo passaggio. Se, come nel caso mostrato nella $(10),$ la manipolazione dovesse produrre un'ulteriore forma indeterminata, possiamo proseguire la riscrittura dell'espressione del limite, con le modalità appropriate per il caso ottenuto, in modo da risolvere l'indeterminazione.

## La forma $\infty - \infty$

Questa forma si ottiene quando il limite è riconducibile alla differenza di due quantità che divergono. Proviamo ad esempio a risolvere il seguente limite:

$$\lim_{x \to \infty} \left( \sqrt{x^2 + x} - x \right) \tag{13}$$

Per sostituzione diretta otteniamo la forma $\infty - \infty$ che si può risolvere razionalizzando il numeratore, cioè moltiplicando e dividendo per il coniugato dell'espressione all'interno del limite (ottenuto cambiando il segno tra gli addendi). In questo modo la radice viene eliminata dal numeratore e otteniamo:

$$
\begin{align}
\sqrt{x^2 + x} - x
&= \frac{\left( \sqrt{x^2 + x} - x \right) \left( \sqrt{x^2 + x} + x \right)}{\sqrt{x^2 + x} + x} \notag \\[6pt]
&= \frac{x^2 + x - x^2}{\sqrt{x^2 + x} + x} \notag \\[6pt]
&= \frac{x}{\sqrt{x^2 + x} + x} \tag{14}
\end{align}
$$

A questo punto possiamo raccogliere la $x$ al denominatore e, con pochi passaggi algebrici, ottenere la seguente riscrittura:

$$
\begin{align}
\frac{x}{\sqrt{x^2 + x} + x}
&= \frac{x}{x \left( \sqrt{1 + 1/x} + 1 \right)} \\[6pt]
&= \frac{1}{\sqrt{1 + 1/x} + 1}
\end{align}
$$

A questo punto abbiamo ottenuto una forma risolvibile, e infatti passando al limite per $x \to \infty,$ otteniamo:

$$\lim_{x \to \infty} \frac{1}{\sqrt{1 + 1/x} + 1} = \frac{1}{\sqrt{1} + 1} = \frac{1}{2}$$

Abbiamo visto che nella tecnica applicata alla $(14)$ usiamo il coniugato dell'espressione iniziale e per capire il motivo consideriamo un ulteriore esempio:

$$\lim_{x \to \infty} \left( \sqrt{x^2 + 2 x + 3} - x \right) \tag{15}$$

Per sostituzione diretta nella $(15)$ otteniamo la forma indeterminata $\infty - \infty$ perché le due quantità hanno lo stesso termine dominante $x,$ quindi occorre determinare cosa rimane della loro differenza. Moltiplicando e dividendo per il coniugato, otteniamo al numeratore la differenza dei quadrati delle due quantità, nella quale i termini $x^2$ si cancellano:

$$
\begin{align}
\frac{\left( \sqrt{x^2 + 2 x + 3} - x \right) \left( \sqrt{x^2 + 2 x + 3} + x \right)}{\sqrt{x^2 + 2 x + 3} + x}
&= \frac{x^2 + 2 x + 3 - x^2}{\sqrt{x^2 + 2 x + 3} + x} \\[6pt]
&= \frac{2 x + 3}{\sqrt{x^2 + 2 x + 3} + x}
\end{align}
$$

In questo modo abbiamo riscritto la differenza iniziale come quoziente e il termine dominante $x^2$ è stato eliminato. A questo punto otteniamo:

$$
\begin{align}
\frac{2 x + 3}{\sqrt{x^2 + 2 x + 3} + x}
&= \frac{x \left( 2 + 3/x \right)}{x \left( \sqrt{1 + 2/x + 3/x^2} + 1 \right)} \\[6pt]
&= \frac{2 + 3/x}{\sqrt{1 + 2/x + 3/x^2} + 1}
\end{align}
$$

Quando $x \to \infty,$ i termini con $x$ al denominatore tendono a zero e quindi otteniamo:

$$\lim_{x \to \infty} \frac{2 + 3/x}{\sqrt{1 + 2/x + 3/x^2} + 1} = \frac{2}{1 + 1} = 1$$

Lo stesso limite si può calcolare anche mediante sviluppi asintotici, usando le notazioni di O grande e o piccolo per controllare i termini di resto dopo la cancellazione dei termini dominanti.

## Forme esponenziali

Vediamo ora il caso delle forme della $(1)$ che coinvolgono forme indeterminate esponenziali del tipo:

$$1^{\infty} \qquad 0^{0} \qquad \infty^{0} \tag{16}$$

Le espressioni si presentano tipicamente quando il limite è ricondotto a espressioni nella seguente forma:

$$\lim_{x \to a} F(x)^{G(x)} \tag{17}$$

Supponiamo che $F(x) \gt 0$ per $x$ sufficientemente vicino ad $a,$ nel dominio considerato ed escluso eventualmente $a.$ Il procedimento standard per risolvere le espressioni come nella $(17)$ consiste nell'applicare il logaritmo alla potenza, ottenendo $\ln(F(x)^{G(x)}) = G(x)\ln F(x).$ Il prodotto può poi essere riscritto come rapporto e studiato con la regola di de l'Hôpital o con uno sviluppo di Taylor. Indichiamo con $L$ il limite da calcolare, se esiste:

$$L = \lim_{x \to a} F(x)^{G(x)} \tag{18}$$

Calcoliamo prima il limite del logaritmo dell'espressione nella $(18)$:

$$\ell = \lim_{x \to a} G(x) \ln F(x) \tag{19}$$

Il problema si riduce così a un limite della forma $0 \cdot \infty,$ eventualmente riscrivibile come $0/0,$ che si può studiare con le tecniche già discusse. Se il limite $\ell$ esiste ed è finito, per la continuità dell'esponenziale esiste anche il limite iniziale e vale:

$$L = e^{\ell} \tag{20}$$

Se invece $\ell = -\infty,$ il limite iniziale è $0;$ se $\ell = +\infty,$ è $+\infty.$

Consideriamo ad esempio il seguente limite che per sostituzione diretta presenta la forma indeterminata $1^{\infty}:$

$$\lim_{x \to 0} (1 + x)^{1/x} \tag{21}$$

Applichiamo alla $(21)$ la trasformazione presentata nella $(19)$ in modo da ottenere:

$$\ell = \lim_{x \to 0} \frac{\ln(1 + x)}{x}$$

A questo punto abbiamo ottenuto la forma $0/0$ che possiamo risolvere in questo caso con la regola di de l'Hôpital, derivando separatamente il numeratore e il denominatore. La regola è discussa nella relativa voce, ma ai nostri fini vi basti sapere che il limite diventa:

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = \lim_{x \to 0} \frac{1/(1+x)}{1} = 1$$

Applicando quindi la riscrittura della $(20)$ otteniamo:

$$L = e^{1} = e$$

## Una strategia per il calcolo

In genere, al di là dei metodi illustrati, ogni forma indeterminata può ammettere più tecniche risolutive, e la scelta tra queste influisce sulla rapidità con cui il calcolo conduce a un'espressione determinata calcolabile. A livello pratico, la strategia migliore per affrontare questi problemi consiste nel riconoscere la forma indeterminata e applicare una tecnica che ci consenta di ottenere il risultato il più rapidamente possibile e con meno calcoli. Quando ad esempio un tentativo diventa algebricamente troppo laborioso o porta iterativamente a ulteriori forme indeterminate, probabilmente, il metodo che si è scelto non è il migliore per trattare quel limite.

Quello che posso suggerirvi è che per la forma $0/0,$ il primo tentativo consiste spesso nella semplificazione algebrica mediante scomposizione del numeratore e del denominatore e con la cancellazione del fattore che tende a zero. In alcuni casi si può ricorrere ai limiti notevoli, soprattutto in presenza di espressioni trigonometriche, esponenziali o logaritmiche. Se nessuna delle due strade è praticabile, si possono usare gli sviluppi asintotici con la notazione di o piccolo che isolano il comportamento dominante del numeratore e del denominatore. In altri casi si può ricorrere alla regola di de l'Hôpital soprattutto quando i metodi precedenti diventano laboriosi.

Per la forma $\infty/\infty,$ il procedimento standard consiste nel raccogliere il termine dominante al numeratore e al denominatore e ricavare il limite dal rapporto che rimane. Quando il termine dominante non è immediatamente identificabile, si può ricorrere al [confronto tra logaritmi, potenze ed esponenziali](../hierarchy-of-growth-rates/). In alcuni casi la regola di de l'Hôpital può essere applicabile, ma il metodo del termine dominante è tipicamente più rapido e semplice.

Per la forma $0 \cdot \infty$ si applicano le tecniche sopra elencate, mentre per la forma $\infty - \infty,$ il passaggio opportuno dipende dalla struttura algebrica delle due quantità che divergono. Infine, per le forme esponenziali e per il prodotto $0 \cdot \infty,$ si usano le tecniche sopra illustrate. Nella seguente tabella è riportato un quadro di sintesi delle principali tecniche da applicare alle singole forme:

[class="table-1"]

|                          |                                                                                                                  |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| $\dfrac{0}{0}$           | Scomporre e semplificare, applicare la regola di de l'Hôpital oppure usare uno sviluppo in serie di Taylor |
| $\dfrac{\infty}{\infty}$ | Raccogliere il termine dominante oppure applicare la regola di de l'Hôpital |
| $0 \cdot \infty$         | Riscrivere come $\dfrac{0}{1/\infty}$ o $\dfrac{\infty}{1/0}$ per ottenere $\dfrac{0}{0}$ o $\dfrac{\infty}{\infty}$ |
| $\infty - \infty$        | Moltiplicare e dividere per il coniugato oppure portare a denominatore comune |
| $1^{\infty}$             | Applicare il logaritmo e ricondursi a $0 \cdot \infty$ |
| $0^{0}$                  | Applicare il logaritmo e ricondursi a $0 \cdot \infty$ |
| $\infty^{0}$             | Applicare il logaritmo e ricondursi a $0 \cdot \infty$ |
[/class]
