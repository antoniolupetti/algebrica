---
title: Integrals of Irrational Functions
source: https://algebrica.org/integrals-of-irrational-functions/
license: CC BY-NC 4.0
tags:
  - binomial-differentials
  - completing-the-square
  - euler-substitution
  - indefinite-integral
  - integration-by-substitution
  - integration-techniques
  - irrational-functions
  - rationalizing-substitution
---
## Introduzione

Gli integrali delle funzioni irrazionali, che presentano la variabile sotto il segno di radice, possono risultare piuttosto laboriosi se non si conoscono gli approcci necessari per calcolarli in modo agevole. In genere, dobbiamo porci l'obiettivo di ridurre l'integrale iniziale a una forma priva di radici e di trasformare la funzione integranda in una funzione razionale il cui calcolo è molto più semplice.

Indichiamo con $R(u,v)$ una funzione razionale nelle due indeterminate $u$ e $v.$ Consideriamo una sostituzione $x=\chi(t)$ e definiamo $\psi(t)=\sqrt[n]{\varphi\big(\chi(t)\big)}.$ Se $\chi(t)$ e $\psi(t)$ sono funzioni razionali di $t,$ la sostituzione razionalizza l'integrale e vale:

$$\int R\big(x,\sqrt[n]{\varphi(x)}\big) \ dx=\int R\big(\chi(t),\psi(t)\big)\chi'(t) \ dt$$

Nel seguito ogni sostituzione è intesa su un intervallo del dominio reale nel quale si fissa il ramo dei radicali e i denominatori non si annullano. Questa convenzione permette di interpretare le identità fra radicali e potenze senza introdurre cambi di segno.

Questa rappresenta la formula del processo generale, ma bisogna tenere a mente che non tutte le funzioni irrazionali ammettono una primitiva elementare. Classi di integrali come quello che segue appartengono ai cosiddetti integrali ellittici, che non si riescono ad esprimere tramite funzioni elementari:

$$\int\frac{dx}{\sqrt{1-x^4}}$$

Pertanto, tutte le sostituzioni discusse in questa voce riguardano esclusivamente i casi in cui la razionalizzazione è possibile, rimandando invece il caso degli integrali ellittici ad altra trattazione. Prima di procedere assicuratevi di aver acquisito le principali tecniche di integrazione perché altrimenti quanto riportato potrebbe risultarvi poco comprensibile.

## Radicali di espressioni lineari fratte

Iniziamo con un caso relativamente semplice, considerando un'integranda razionale in $x$ e nella radice $n$-esima di un rapporto di due binomi di primo grado:

$$\int R\left(x,\sqrt[n]{\frac{ax+b}{cx+d}}\right) \tag{1}dx$$

Prima di procedere bisogna porre la condizione $ad-bc\neq0$ che serve a escludere il caso in cui numeratore e denominatore sono proporzionali. Se così fosse, il radicale si riduce a un numero e non serve alcuna sostituzione. Il concetto sarà più chiaro con il seguente esempio. Poniamo $a=2,$ $b=4,$ $c=1$ e $d=2$ ottenendo:

$$\sqrt{\frac{2x+4}{x+2}}=\sqrt2 \qquad x\neq-2$$

Il radicale è una costante e l'integranda è già razionale nella sola $x,$ pertanto non necessita alcuna sostituzione. Poiché la fortuna è per pochi, più spesso ci si imbatte in integrali che invece richiedono una sostituzione che per la $(1)$ consiste nel sostituire $t$ al radicale:

$$t=\sqrt[n]{\frac{ax+b}{cx+d}}$$

La precedente espressione implica che:

$$t^n=\frac{ax+b}{cx+d}$$

A questo punto si ricava $x$ dalla seconda uguaglianza e con banali passaggi algebrici si ottiene:

$$x=\frac{b-dt^n}{ct^n-a}$$

Questa è una funzione razionale di $t,$ e lo è anche la sua derivata. Sviluppando la derivata del quoziente, il numeratore si contrae nella costante $ad-bc$ moltiplicata per $nt^{n-1}$:

$$dx=\frac{n(ad-bc)t^{n-1}}{(ct^n-a)^2} \ dt$$

In questo modo abbiamo completato la razionalizzazione.

- - -

Un caso frequente si incontra per $c=0$ e $d=1,$ quando sotto radice compare un semplice binomio di primo grado:

$$\int R\big(x,\sqrt[n]{ax+b}\big) \ dx \qquad t=\sqrt[n]{ax+b}$$

Qui la sostituzione inversa è $x=(t^n-b)/a$ e il differenziale è $dx=(n/a)t^{n-1} \ dt.$

Nel caso in cui lo stesso binomio compare sotto radici di indici diversi, una sola sostituzione le razionalizza tutte, purché l'esponente scelto sia divisibile per ciascun indice. La forma generale con più radicali è la seguente:

$$\int R\big(x,\sqrt[n_1]{ax+b},\dots,\sqrt[n_j]{ax+b}\big) \ dx$$

Qui si pone $t^m=ax+b$ con $m$ pari al minimo comune multiplo di $n_1,\dots,n_j.$ Se $m$ è pari, si sceglie $t\geq0.$ Ogni radice diventa allora una potenza intera di $t,$ perché $\sqrt[n_i]{ax+b}=t^{m/n_i}$ e l'esponente $m/n_i$ è intero per come è stato scelto $m.$

Per rendere più immediato il criterio, applichiamolo al seguente integrale:

$$\int\frac{dx}{\sqrt x+\sqrt[3]x}$$

Nell'esempio gli indici dei radicali sono rispettivamente $2$ e $3$ e il minimo comune multiplo è $6.$ Ponendo $x=t^6$ con $t>0$, segue $dx=6t^5 \ dt,$ $\sqrt x=t^3$ e $\sqrt[3]x=t^2.$ Con banali calcoli otteniamo:

$$\int\frac{6t^5}{t^3+t^2} \ dt=6\int\frac{t^3}{t+1} \ dt$$

Abbiamo quindi ottenuto un numeratore il cui grado è maggiore di quello del denominatore e pertanto possiamo applicare la [divisione tra polinomi](../polynomial-division/) ottenendo:

$$\frac{t^3}{t+1}=t^2-t+1-\frac{1}{t+1}$$

L'integrale è banale e si può procedere integrando termine a termine:

$$6\left(\frac{t^3}{3}-\frac{t^2}{2}+t-\ln|t+1|\right)=2t^3-3t^2+6t-6\ln(t+1)$$

Poiché $t > 0$ possiamo togliere il valore assoluto dal logaritmo. Ora, tornando alla variabile iniziale abbiamo che $t=\sqrt[6]x,$ da cui $t^3=\sqrt x$ e $t^2=\sqrt[3]x$. Pertanto l'integrale di partenza vale:

$$\int\frac{dx}{\sqrt x+\sqrt[3]x}=2\sqrt x-3\sqrt[3]x+6\sqrt[6]x-6\ln\big(\sqrt[6]x+1\big)+k$$

- - -

Facciamo un secondo esempio, e proviamo a risolvere il seguente integrale:

$$\int\sqrt{\frac{x}{1-x}} \ dx \qquad 0\leq x<1$$

I coefficienti sono $a=1,$ $b=0,$ $c=-1,$ $d=1,$ quindi $ad-bc=1,$ e pertanto dobbiamo applicare la sostituzione. Poniamo $t=\sqrt{x/(1-x)},$ da cui $t^2(1-x)=x$ e otteniamo:

$$x=\frac{t^2}{1+t^2} \qquad dx=\frac{2t}{(1+t^2)^2} \ dt$$

A questo punto l'integranda diventa una funzione razionale:

$$\int t\cdot\frac{2t}{(1+t^2)^2} \ dt=2\int\frac{t^2}{(1+t^2)^2} \ dt$$

Piccola divagazione: tenete a mente che, in moltissimi contesti, aggiungere e sottrarre una certa quantità a un'espressione nella quale si è apparentemente impantanati, può svoltare la situazione. Un trucco classico, che gli studenti non conoscono o fanno fatica a maneggiare perché i corsi canonici di matematica lo trattano come un orpello quasi superfluo, è quello di aggiungere la quantità $\pm 1.$ Nel caso del nostro esempio, scrivendo $t^2=(1+t^2)-1$ il quoziente si spezza nella differenza fra $1/(1+t^2)$ e $1/(1+t^2)^2.$ Il secondo termine si riduce al caso $n=2$ della [formula di riduzione](../reduction-formulas/) per le potenze di un denominatore quadratico e si può ottenere:

$$\int\frac{dt}{(1+t^2)^2}=\frac{t}{2(1+t^2)}+\frac{1}{2}\arctan t$$

Per tornare adesso alla variabile iniziale osserviamo che $1+t^2=1/(1-x),$ quindi $t/(1+t^2)=t(1-x)=\sqrt{x(1-x)}.$ Il risultato è:

$$\int\sqrt{\frac{x}{1-x}} \ dx=\arctan\sqrt{\frac{x}{1-x}}-\sqrt{x(1-x)}+k$$

## La radice di un trinomio di secondo grado

Passiamo ora ad analizzare la famiglia di integrali più ricorrente, quella in cui sotto radice compare un polinomio di secondo grado:

$$\int R\big(x,\sqrt{ax^2+bx+c}\big) \ dx$$

Bisogna porre le condizioni $a\neq0$ e $b^2-4ac\neq0$ per escludere un caso degenere. Il primo strumento a cui ricorrere in questi casi è il [completamento del quadrato](../completing-the-square/), che riporta il trinomio a una delle tre forme canoniche trattate nella pagina sulla [sostituzione trigonometrica](../trigonometric-substitution-for-integrals/). Conviene però registrare prima le due primitive elementari che ricorrono in quasi ogni calcolo di questa famiglia. Scriviamo $Q(x)=ax^2+bx+c$ e $D=b^2-4ac,$ e osserviamo che moltiplicando $Q$ per $4a$ e completando il quadrato vale l'identità:

$$4aQ(x)=(2ax+b)^2-D$$

Questa relazione suggerisce una sostituzione lineare $w=2ax+b,$ con $dw=2a \ dx$. Per $a>0$ l'identità dà $\sqrt{Q(x)}=\sqrt{w^2-D}/(2\sqrt a),$ e l'integrale si riduce alla primitiva di $1/\sqrt{w^2-D}:$

$$\int\frac{dx}{\sqrt{ax^2+bx+c}}=\frac{1}{\sqrt a}\ln\left|2ax+b+2\sqrt a\sqrt{ax^2+bx+c}\right|+k$$

Per $a<0$ il radicando è positivo solo su un intervallo limitato, e questo obbliga il discriminante a essere positivo. L'identità dà ora $\sqrt{Q(x)}=\sqrt{D-w^2}/(2\sqrt{-a}),$ e l'integrale si riduce alla primitiva dell'[arcoseno](../arcsine-function/):

$$\int\frac{dx}{\sqrt{ax^2+bx+c}}=-\frac{1}{\sqrt{-a}}\arcsin\frac{2ax+b}{\sqrt{b^2-4ac}}+k$$

Poiché $Q'(x)=2ax+b,$ ogni binomio $mx+n$ si decompone come combinazione lineare della derivata del trinomio e della costante $1$:

$$mx+n=\frac{m}{2a}(2ax+b)+\left(n-\frac{mb}{2a}\right)$$

Il primo addendo produce un integrale immediato, perché il suo numeratore è esattamente la derivata del radicando e la primitiva di $Q'/\sqrt Q$ è $2\sqrt Q.$ Il secondo riporta alle due formule appena scritte, quindi:

$$\int\frac{mx+n}{\sqrt{ax^2+bx+c}} \ dx=\frac{m}{a}\sqrt{ax^2+bx+c}+\left(n-\frac{mb}{2a}\right)\int\frac{dx}{\sqrt{ax^2+bx+c}}$$

## Le sostituzioni di Eulero

Non tutto però fila sempre liscio. Il completamento del quadrato risolve infatti i soli casi in cui la radice compare isolata al numeratore o al denominatore. Quando invece $R$ combina $x$ e la radice in una frazione qualunque, la via trigonometrica conduce a un integrale di funzione razionale in seno e coseno, che a sua volta richiede la [sostituzione di Weierstrass](../the-weierstrass-substitution/).

In questi casi intervengono le sostituzioni di Eulero che consentono di razionalizzare l'integranda direttamente, senza passare per le funzioni trigonometriche.

La prima sostituzione richiede $a>0$ e pone:

$$\sqrt{ax^2+bx+c}=t-x\sqrt a$$

Elevando al quadrato entrambi i membri il termine $ax^2$ si cancella e resta $bx+c=t^2-2\sqrt atx.$ Da qui $x$ si ricava come funzione razionale di $t$:

$$x=\frac{t^2-c}{2\sqrt at+b}$$

Derivando il quoziente si ottiene il differenziale, e riportando l'espressione di $x$ dentro la sostituzione si ricava il radicale:

$$dx=\frac{2\big(\sqrt at^2+bt+\sqrt ac\big)}{(2\sqrt at+b)^2} \ dt$$
$$\sqrt{ax^2+bx+c}=\frac{\sqrt at^2+bt+\sqrt ac}{2\sqrt at+b}$$

- - -

La seconda sostituzione richiede $c>0$ e pone:

$$\sqrt{ax^2+bx+c}=xt+\sqrt c$$

Elevando al quadrato si cancella il termine noto e resta $ax^2+bx=x^2t^2+2\sqrt cxt.$ Scartando la radice $x=0,$ che non porta informazione sulla primitiva, e dividendo per $x$ si ottiene un'equazione di primo grado, da cui:

$$x=\frac{2\sqrt ct-b}{a-t^2}$$

- - -

La terza sostituzione richiede che il trinomio abbia due [radici](../roots-of-a-polynomial/) reali distinte $\alpha$ e $\beta,$ cioè $b^2-4ac>0.$ In tal caso vale la fattorizzazione:

$$ax^2+bx+c=a(x-\alpha)(x-\beta)$$

Poi si pone:

$$\sqrt{ax^2+bx+c}=t(x-\alpha)$$

Elevando tutto al quadrato e dividendo per il fattore comune $x-\alpha$ otteniamo:

$$x=\frac{a\beta-\alpha t^2}{a-t^2}$$

È utile sapere che le tre sostituzioni si sovrappongono nella copertura dei casi. Quando $a>0$ si applica la prima. Quando $a<0$ il radicando è positivo solo su un intervallo limitato e quindi il discriminante è positivo, il che rende applicabile la terza. La prima e la terza bastano a coprire ogni trinomio con radicando non ovunque negativo, mentre la seconda è una scorciatoia che conviene sfruttare quando $c>0$ perché accorcia sensibilmente i calcoli.

- - -

Per chiarire con un esempio pratico quanto abbiamo fin qui descritto, calcoliamo con questo metodo il seguente integrale:

$$\int\frac{dx}{x\sqrt{x^2+x+1}}$$

Il trinomio ha $a=1$ e $c=1,$ quindi possiamo ricorrere sia alla prima sia alla seconda sostituzione (poiché il discriminante vale $-3,$ possiamo escludere la terza). Scegliamo la seconda e poniamo:

$$\sqrt{x^2+x+1}=xt+1$$

Elevando al quadrato e semplificando il termine noto resta $x^2+x=x^2t^2+2xt.$ Dividendo per $x$ otteniamo $x+1=xt^2+2t$ e quindi:

$$x=\frac{2t-1}{1-t^2}$$

Da questa espressione ricaviamo il differenziale e il radicale come funzioni razionali di $t$:

$$dx=\frac{2\big(t^2-t+1\big)}{(1-t^2)^2} \ dt$$

$$\sqrt{x^2+x+1}=xt+1=\frac{t^2-t+1}{1-t^2}$$

Sostituendo i tre fattori nell'integranda e completando i calcoli otteniamo:

$$
\begin{align}
\int\frac{dx}{x\sqrt{x^2+x+1}} &= \int\frac{1-t^2}{2t-1}\cdot\frac{1-t^2}{t^2-t+1}\cdot\frac{2\big(t^2-t+1\big)}{(1-t^2)^2} \ dt \\[6pt]
&= \int\frac{2}{2t-1} \ dt
\end{align}
$$

L'integrale finale vale $\ln|2t-1|.$ Dalla sostituzione, poi, ricaviamo $t=\big(\sqrt{x^2+x+1}-1\big)/x,$ quindi $2t-1=\big(2\sqrt{x^2+x+1}-x-2\big)/x$ e la primitiva è:

$$\int\frac{dx}{x\sqrt{x^2+x+1}}=\ln\left|\frac{2\sqrt{x^2+x+1}-x-2}{x}\right|+k$$

> Fidatevi del fatto che questo procedimento è molto più efficiente della sostituzione trigonometrica che in taluni casi potrebbe complicare di molto l'integrale iniziale rendendo i calcoli molto più lunghi o addirittura poco praticabili. Quindi il suggerimento è di imparare a maneggiare con una certa confidenza questi metodi perché i casi pratici a cui si applicano sono piuttosto frequenti e possono quindi risultare molto utili se non decisivi per la risoluzione di integrali di primo acchito piuttosto laboriosi.

## Numeratore polinomiale e coefficienti indeterminati

Analizziamo a questo punto un ulteriore caso, quando la radice compare solo al denominatore e il numeratore è un polinomio. La buona notizia è che esiste un metodo che evita del tutto le sostituzioni. Indichiamo con $P_n$ un polinomio di grado $n$ e come sopra con $Q(x)=ax^2+bx+c$ il trinomio sotto radice. Bisogna ricercare una primitiva nella seguente forma:

$$\int\frac{P_n(x)}{\sqrt{Q(x)}} \ dx=S_{n-1}(x)\sqrt{Q(x)}+\lambda\int\frac{dx}{\sqrt{Q(x)}}$$

$S_{n-1}$ è un polinomio di grado $n-1$ a coefficienti incogniti e $\lambda$ è una costante. L'integrale a destra è una delle due primitive ricavate sopra con il completamento del quadrato, quindi è già noto. Per determinare i coefficienti si deriva l'uguaglianza rispetto a $x$ e si moltiplicano entrambi i membri per $\sqrt Q,$ operazione che elimina ogni radice e lascia un'identità fra polinomi:

$$P_n(x)=S_{n-1}'(x)Q(x)+\frac{1}{2}S_{n-1}(x)Q'(x)+\lambda$$

I due membri hanno lo stesso grado $n,$ perché $S_{n-1}'$ ha grado $n-2$ e $Q$ ha grado $2,$ mentre $S_{n-1}$ ha grado $n-1$ e $Q'$ ha grado $1.$ Il confronto dei coefficienti produce $n+1$ equazioni lineari nelle $n$ incognite di $S_{n-1}$ e in $\lambda,$ cioè in $n+1$ incognite, e il sistema si risolve in cascata partendo dal grado massimo. Vediamo un caso pratico che spero possa rendere il tutto meno fumoso. Risolviamo il seguente integrale:

$$\int\frac{x^2}{\sqrt{x^2+1}} \ dx$$

Qui $n=2,$ quindi $S_1(x)=Ax+B$ e l'identità fra polinomi diventa:

$$x^2=A\big(x^2+1\big)+\frac{1}{2}(Ax+B)(2x)+\lambda=2Ax^2+Bx+(A+\lambda)$$

Il confronto dei coefficienti dà $A=1/2$ dal termine quadratico, $B=0$ dal termine lineare e $\lambda=-1/2$ dal termine noto. L'integrale residuo è il caso $a=1,$ $b=0,$ $c=1$ della formula per $a>0,$ che si riduce a $\ln\big(x+\sqrt{x^2+1}\big)$. La primitiva è quindi:

$$\int\frac{x^2}{\sqrt{x^2+1}} \ dx=\frac{x}{2}\sqrt{x^2+1}-\frac{1}{2}\ln\big(x+\sqrt{x^2+1}\big)+k$$

## I differenziali binomi

L'ultima famiglia di integrali che vedremo ha una struttura diversa da quelle viste fino ad ora, perché la radice si riferisce a un binomio in cui la variabile compare con un esponente qualunque. Si definisce differenziale binomio un'espressione della forma:

$$x^m\big(a+bx^n\big)^p \ dx \qquad a,b\neq0, \quad m,n,p\in\mathbb{Q}, \quad n\neq0$$

L'ipotesi $n\neq0$ esclude il caso degenere $n=0,$ nel quale il fattore $(a+bx^n)^p$ è costante e l'integrale, quando definito, si riduce a un integrale monomiale.

Ponendo $z=x^n,$ da cui $dz=nx^{n-1} \ dx,$ l'integrale si riscrive in una forma che mette in evidenza gli esponenti $(m+1)/n-1$ e $p,$ dai quali dipende la classificazione che segue:

$$\int x^m\big(a+bx^n\big)^p \ dx=\frac{1}{n}\int z^{\frac{m+1}{n}-1}(a+bz)^p \ dz$$

Nel caso generale la primitiva non è per nulla elementare. Il risultato che stabilisce esattamente quando lo è si deve a Chebyshev (ma è fuori dalla nostra trattazione) e riguarda i tre numeri seguenti:

$$p \qquad \frac{m+1}{n} \qquad \frac{m+1}{n}+p$$

Sappiate solo che, in questi casi, l'integrale si esprime attraverso funzioni elementari se e solo se almeno uno di questi tre numeri è intero.

+ Se $p$ è intero, l'integranda è razionale nelle potenze di $x^{1/s},$ dove $s$ è il minimo comune multiplo dei denominatori di $m$ e $n,$ quindi si pone $x=t^s.$
+ Se $(m+1)/n$ è intero, si pone $a+bx^n=t^s,$ dove $s$ è il denominatore di $p.$
+ Se $(m+1)/n+p$ è intero, si pone $ax^{-n}+b=t^s,$ con lo stesso $s.$

- - -

Il secondo caso si riconosce con facilità. Consideriamo ad esempio:

$$\int\frac{\sqrt[3]{1+\sqrt[4]x}}{\sqrt x} \ dx \qquad x>0$$

Riscritto come differenziale binomio ha $m=-1/2,$ $n=1/4$ e $p=1/3.$ Il denominatore di $p$ vale $3,$ e la sostituzione è $1+x^{1/4}=t^3,$ da cui:

$$x=\big(t^3-1\big)^4$$
$$dx=12t^2\big(t^3-1\big)^3 \ dt$$
$$\sqrt x=\big(t^3-1\big)^2$$

Possiamo riscrivere il tutto come

$$
\begin{align}
\int\frac{t\cdot12t^2\big(t^3-1\big)^3}{\big(t^3-1\big)^2} \ dt &= 12\int\big(t^6-t^3\big) \ dt \\[6pt]
&= \frac{12t^7}{7}-3t^4
\end{align}
$$

Tornando alla variabile iniziale con $t=\sqrt[3]{1+\sqrt[4]x}$ si ottiene:

$$\int\frac{\sqrt[3]{1+\sqrt[4]x}}{\sqrt x} \ dx=\frac{12}{7}\big(1+\sqrt[4]x\big)^{7/3}-3\big(1+\sqrt[4]x\big)^{4/3}+k$$

Un po' laborioso come avete visto, ma fattibile.

- - -

Il terzo caso è il meno immediato da riconoscere, perché la condizione riguarda una somma e non un singolo esponente. Prendiamo ad esempio:

$$\int\frac{dx}{x^4\sqrt{1+x^2}} \qquad x>0$$

Gli esponenti sono $m=-4,$ $n=2$ e $p=-1/2.$ Né $p$ né $(m+1)/n=-3/2$ sono interi, mentre la somma $(m+1)/n+p=-2$ lo è, quindi poniamo $x^{-2}+1=t^2$ con $t>1.$ Da questa relazione segue $x^2=1/(t^2-1),$ e derivando si ottiene:

$$dx=-t\big(t^2-1\big)^{-3/2} \ dt$$
$$\sqrt{1+x^2}=\frac{t}{\sqrt{t^2-1}}$$

Semplificando le potenze di $t^2-1,$ l'integranda si riduce di nuovo a un polinomio e quindi:

$$
\begin{align}
\int\frac{dx}{x^4\sqrt{1+x^2}} &= \int\big(t^2-1\big)^2\cdot\frac{\sqrt{t^2-1}}{t}\cdot\Big({-t}\big(t^2-1\big)^{-3/2}\Big) \ dt \\[6pt]
&= -\int\big(t^2-1\big) \ dt \\[6pt]
&= t-\frac{t^3}{3}
\end{align}
$$

Tornando alla sostituzione iniziale, con $t=\sqrt{1+x^2}/x$ e raccogliendo la radice a fattore comune si ottiene:

$$\int\frac{dx}{x^4\sqrt{1+x^2}}=\frac{\big(2x^2-1\big)\sqrt{1+x^2}}{3x^3}+k$$

## Considerazioni sulla scelta della sostituzione

Possiamo riassumere la scelta del criterio da utilizzare secondo i seguenti punti di sintesi.

+ Per le radici di un binomio di primo grado, anche con indici diversi, si pone $t^m=ax+b$ con $m$ minimo comune multiplo degli indici.
+ Per la radice di un rapporto fra due binomi di primo grado si pone $t$ uguale al radicale, dopo aver verificato che sia $ad-bc\neq0.$
+ Per la radice di un trinomio di secondo grado che compare isolata si completa il quadrato e si applica la sostituzione trigonometrica, oppure si usano le due formule dirette ricavate sopra.
+ Per la radice di un trinomio dentro un'espressione razionale qualunque si sceglie fra le tre sostituzioni di Eulero secondo il segno di $a,$ quello di $c$ e il discriminante.
+ Per un polinomio diviso per la radice di un trinomio si applica il metodo dei coefficienti indeterminati.
+ Per una potenza di $x$ moltiplicata per una potenza di un binomio in $x^n$ si verifica il criterio di Chebyshev e si sceglie fra le tre sostituzioni corrispondenti.

Un integrale può ricadere in più voci dell'elenco, e in tal caso conviene decidere in base alla lunghezza dei calcoli che ciascuna via comporta. Naturalmente questo non è immediato a priori, ma con un po' di esperienza si riesce a capire abbastanza agevolmente quale sostituzione è preferibile.

> Fuori da queste famiglie la primitiva elementare in generale non esiste. Se $P$ è un polinomio di grado $3$ o $4$ privo di radici multiple, l'integrale $\int \frac{dx}{\sqrt{P(x)}}$ è un integrale ellittico. La sola presenza di $\sqrt{P(x)}$ nell'integranda non basta però a escludere una primitiva elementare, perché radici multiple o numeratori particolari possono ridurre l'integrale a forme elementari. Gli integrali ellittici compaiono ad esempio nel calcolo della [lunghezza](../arc-length-of-a-curve/) di un arco di ellisse e si studiano come funzioni speciali.
