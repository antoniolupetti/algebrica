---
title: Hierarchy of Growth Rates
source: https://algebrica.org/hierarchy-of-growth-rates/
license: CC BY-NC 4.0
tags:
  - asymptotic-comparison
  - exponential-functions
  - growth-rates
  - limits
  - logarithms
  - powers
---
## Gerarchia degli ordini di crescita

La gerarchia degli ordini di crescita è un metodo che consente di calcolare limiti in cui compaiono logaritmi, potenze ed esponenziali, identificando quali termini di un'espressione diventano trascurabili rispetto agli altri, ed è molto utile, ad esempio, nella risoluzione di alcune forme indeterminate. Quando consideriamo un limite che tende a $\infty,$ alcune funzioni crescono più lentamente di altre, il che ci consente di trarre osservazioni utili per determinarne il comportamento. Consideriamo i seguenti parametri: 

$$ \tag{1}
\begin{align}
p &> 0 \\[6pt]
0 &< \alpha < \beta \\[6pt]
1 &< a < b
\end{align}
$$

Scriviamo quindi la seguente catena di disuguaglianze che indica l'ordine di crescita delle singole funzioni, che aumenta spostandosi verso destra:

$$
(\ln x)^p \ll x^\alpha \ll x^\beta \ll a^x \ll b^x \ll e^{x^2}
\qquad

\tag{2}
$$

Nella $(2),$ il simbolo $\ll$ indica che il rapporto tra la funzione a sinistra e quella a destra del simbolo tende a zero. Nel caso specifico della $(2),$ quando $x$ che tende a $+\infty$ tutte le funzioni tendono a $+\infty,$ ma lo fanno con velocità diverse. In linea generale dire che $f$ cresce più lentamente di $g$ significa che, per ogni costante positiva $M,$ la disuguaglianza $g>Mf$ vale per ogni $x$ sufficientemente grande. Questo confronto richiede più di una semplice disuguaglianza $f(x)<g(x):$ per esempio, $x$ è sempre minore di $2x$ per $x>0,$ ma il rapporto non tende a zero:

$$
\lim_{x\to+\infty}\frac{x}{2x}=\frac12\ne0
\tag{3}
$$

La $(3)$ mostra quindi che $x$ non è trascurabile rispetto a $2x$ mentre nella gerarchia della $(2),$ ogni funzione diventa trascurabile rispetto a quella successiva. Per calcolare questi limiti limite occorre quindi confrontare i rapporti, dopo aver semplificato le eventuali cancellazioni tra i termini.

## Confronto tramite il rapporto

Vediamo un primo confronto tra due funzioni positive che si basa sul limite del loro rapporto. Per $x$ sufficientemente grande, se questo limite è zero, significa che il numeratore è trascurabile rispetto al denominatore, mentre se si ottiene una costante positiva, le due funzioni hanno lo stesso ordine di grandezza. Nel primo caso si introduce la notazione di o piccolo, riferita al limite che stiamo considerando, per cui si ha:

$$
\lim_{x\to+\infty}\frac{f(x)}{g(x)}=0
\quad\Longleftrightarrow\quad f(x)=o(g(x))
\tag{4}
$$

Nel secondo caso, invece, si ha:

$$
\lim_{x\to+\infty}\frac{f(x)}{g(x)}=L,
\qquad 0<L<+\infty
\tag{5}
$$

Nella $(5),$ si dice che $f(x)$ è asintoticamente equivalente a $Lg(x)$ e, nel caso $L=1,$ si ha che le funzioni sono asintoticamente equivalenti e si scrive:

$$f(x)\sim g(x)\tag{6}$$ 
Per esempio, confrontiamo $3x^2$ e $x^2,$ poi $x^2+x$ e $x^2,$ calcolando il rapporto tra la prima e la seconda funzione di ciascuna coppia:

$$
\begin{align}
\lim_{x\to+\infty}\frac{3x^2}{x^2}&=3 \\[6pt]
\lim_{x\to+\infty}\frac{x^2+x}{x^2}
&=\lim_{x\to+\infty}\left(1+\frac1x\right)=1
\end{align}
\tag{7}
$$

Il primo limite della $(7)$ mostra che $3x^2$ e $x^2$ hanno lo stesso ordine, perché il rapporto tende a una costante positiva finita, mentre nel secondo limite il rapporto tende a $1,$ numeratore e denominatore sono asintoticamente equivalenti secondo la $(6).$ Consideriamo ora il caso in cui dal limite del rapporto otteniamo:
$$\frac{f(x)}{g(x)}\to+\infty \tag{8}$$

Il risultato della $(8)$ significa che $g$ è trascurabile rispetto a $f.$ Tenete conto che bon tutte le coppie di funzioni ammettono questo genere di confronti, perché in alcune situazioni il rapporto può non avere limite come nel seguente caso:

$$
\frac{(2+\sin x)x}{x}=2+\sin x \tag{9}
$$

Per $x\to+\infty,$ il rapporto nella $(9)$ non ha limite perché oscilla tra $3$ quando $x=\pi/2+2k\pi$ e $1$ nquando $x=3\pi/2+2k\pi$. Quindi, il metodo della gerarchia di crescita si può applicare solo quando il rapporto ha un comportamento determinato.

## Confronti nella stessa famiglia

Prima di confrontare famiglie diverse di funzioni, conviene sempre verificare come cambiano gli ordini di crescita al variare degli esponenti e delle basi. Per chiarire la questione consideriamo il rapporto tra due potenze di $x$ che, per le proprietà degli esponenti, quando $x\to+\infty$ e $\alpha<\beta$ possiamo scrivere come: 

$$
\frac{x^\alpha}{x^\beta}=x^{\alpha-\beta}
\longrightarrow0
\tag{10}
$$

Poiché nella $(10),$ l'esponente $\alpha-\beta$ è negativo, il rapporto tende a zero e questo significa che la potenza con esponente minore è trascurabile rispetto all'altra. Un altro caso frequente è dato dal rapporto tra esponenziali con esponente $x$ che, per $x \to \infty$ e $1<a<b$ si può riscrivere come:

$$
\frac{a^x}{b^x}=\left(\frac{a}{b}\right)^x \longrightarrow0
\tag{11}
$$

Nella $(11),$ la base $a/b$ appartiene all'intervallo $(0,1),$ quindi il rapporto tende a zero, pertanto l'esponenziale con base minore è sempre trascurabile rispetto a quello con base maggiore. Vediamo ora cosa accade per le potenze positive del logaritmo per le quali vale lo stesso criterio della $(10),$ relativo al confronto tra gli esponenti, perché $\ln x\to+\infty.$ Quando $x\to+\infty$ e $0<p<q,$ il rapporto si può infatti riscrivere come:

$$
\frac{(\ln x)^p}{(\ln x)^q}=(\ln x)^{p-q}\longrightarrow0
\tag{12}
$$

Nella $(12),$ l'esponente $p-q$ è negativo, quindi la potenza del logaritmo con esponente minore è trascurabile rispetto a quella con esponente maggiore.

Sempre nella $(12)$ abbiamo confrontato potenze dello stesso logaritmo, variando solo l'esponente ma se invece manteniamo l'esponente uguale a $1$ e cambiamo la base del logaritmo, la situazione cambia. Consideriamo $a,b>1$ e applichiamo la formula del cambiamento di base al seguente rapporto:

$$
\frac{\log_a x}{\log_b x}=\frac{\ln b}{\ln a}
\tag{13}
$$

I logaritmi della $(13)$ differiscono dunque soltanto per un fattore costante e hanno quindi lo stesso ordine.

## Logaritmi, potenze ed esponenziali

Dopo i confronti tra funzioni della stessa famiglia, consideriamo adesso quelli tra famiglie diverse. Il primo riguarda le potenze del logaritmo e le potenze di $x.$ Sappiamo che per quanto grande sia $p>0$ e per quanto piccolo sia $\alpha>0,$ la funzione $(\ln x)^p$ cresce più lentamente di $x^\alpha,$ per cui il limite del loro rapporto tende a zero:

$$
\lim_{x\to+\infty}\frac{(\ln x)^p}{x^\alpha}=0
\tag{14}
$$

Il secondo confronto riguarda le potenze di $x$ e gli esponenziali $a^x$ con base $a>1$ che crescono più rapidamente di qualunque potenza $x^\alpha$ con esponente costante $\alpha>0.$ Per fare un esempio esempio, $x^{100}$ è trascurabile rispetto a $2^x,$ e generalizzando si ha:

$$
\lim_{x\to+\infty}\frac{x^\alpha}{a^x}=0
\tag{15}
$$

I due confronti si possono dimostrare partendo dalla $(15).$ Utilizziamo lo sviluppo di Taylor dell'esponenziale che è dato da:

$$
e^u=\sum_{n=0}^{\infty}\frac{u^n}{n!}
=1+u+\frac{u^2}{2!}+\frac{u^3}{3!}+\cdots
$$

Scegliamo quindi un intero $k>\alpha$ e poniamo $u=x\ln a,$ ottenendo:

$$a^x=e^{x\ln a}\ge \frac{(x\ln a)^k}{k!} \tag{16}$$ 
Con la $(16)$ ricaviamo una maggiorazione del rapporto per cui si può scrivere la seguente relazione:

$$
0\le\frac{x^\alpha}{a^x}
\le\frac{k!x^\alpha}{(x\ln a)^k}
=\frac{k!}{(\ln a)^k}\frac{1}{x^{k-\alpha}}
\longrightarrow0
\tag{17}
$$

Poiché $k-\alpha>0,$ l'ultima espressione tende a zero e per il teorema del confronto otteniamo proprio la $(15).$ Per ricavare invece la $(14),$ poniamo $t=\ln x,$ così $x=e^t$ e $t\to+\infty,$ per cui possiamo scrivere: 

$$
\frac{(\ln x)^p}{x^\alpha}
=\frac{t^p}{e^{\alpha t}}
=\frac{t^p}{(e^\alpha)^t}
\longrightarrow0
\tag{18}
$$

Nella $(18)$ il denominatore è un esponenziale con base $e^\alpha>1,$ quindi la $(15)$ si applica alla variabile $t$ e dà il limite cercato. A questo punto rimane da dimostrare l'ultimo passaggio della gerarchia $(2),$ nel quale $e^{x^2}$ cresce più rapidamente di $b^x.$ Scrivendo $b^x=e^{x\ln b},$ otteniamo:

$$\tag{19}
\frac{b^x}{e^{x^2}}=e^{x\ln b-x^2}
$$

Il termine $x^2$ all'esponente della $(19)$ cresce più rapidamente di $x\ln b,$ che cresce linearmente perché $\ln b$ è una costante, quindi $x\ln b-x^2$ tende a $-\infty$ e l'esponenziale tende a zero. Perciò, in questo modo può concludere che $b^x$ è trascurabile rispetto a $e^{x^2}.$

## Prodotti di potenze e logaritmi

Nel calcolo dei limiti compaiono spesso prodotti di fattori appartenenti a famiglie diverse e in questi casi il primo passo da fare è quello di semplificare il rapporto ricorrendo ad esempio alle proprietà delle potenze e dei logaritmi. Consideriamo ad esempio il seguente rapporto con la sua relativa riscrittura:

$$
\frac{x^\alpha(\ln x)^p}{x^\beta(\ln x)^q}=x^{\alpha-\beta}(\ln x)^{p-q}
\tag{20}
$$

Quando $\alpha<\beta,$ la $(20)$ tende a zero qualunque sia il valore di $p-q,$ mentre quando questa differenza è positiva, si utilizza la $(14).$ Nel caso in cui la differenza è nulla o negativa il fattore logaritmico è limitato per $x$ sufficientemente grande e il fattore $x^{\alpha-\beta}$ tende a zero. Quando $\alpha>\beta,$ il rapporto tende a $+\infty.$ Quando $\alpha=\beta,$ le potenze di $x$ si semplificano e il confronto dipende solo dagli esponenti del logaritmo. Lo stesso ragionamento si estende ai prodotti della seguente forma, con parametri fissi e $a>1$: 

$$a^xx^\alpha(\ln x)^p\tag{21}$$ 
Se le basi degli esponenziali della $(21)$ sono diverse, cresce più rapidamente il prodotto con la base maggiore, mentre se le basi sono uguali, i fattori esponenziali si semplificano e si confrontano gli esponenti di $x.$ Infine, se anche questi esponenti sono uguali, si confrontano gli esponenti del logaritmo, come nella $(12).$ Per capire perché nella $(21)$ prevale la base maggiore, confrontiamo due prodotti con $1<a<b$ scrivendo il loro rapporto come segue: 

$$
\frac{a^xx^\alpha(\ln x)^p}{b^xx^\beta(\ln x)^q}
=\frac{x^{\alpha-\beta}(\ln x)^{p-q}}{(b/a)^x}
\tag{22}
$$

Nella $(22),$ la base $b/a$ è maggiore di $1,$ il logaritmo al numeratore cresce più lentamente di una potenza di $x,$ come mostra la $(14),$ e per la $(15)$ ogni potenza di $x$ cresce più lentamente dell'esponenziale al denominatore. Perciò il rapporto tende a zero.

## Limiti di somme e rapporti tra somme

I confronti illustrati permettono anche di calcolare limiti di somme e di rapporti tra somme seguendo un semplice principio che tiene conto della crescita di uno degli addendi. Quando un addendo cresce più rapidamente degli altri, si dice che diventa dominante rispetto agli altri che rimangono trascurabili rispetto ad esso, determinando il comportamento della somma. Supponiamo di avere la seguente somma, dove $c\ne0$ è una costante e $r(x)$ raccoglie tutti i termini trascurabili rispetto a $g(x):$

$$F(x)=cg(x)+r(x) \tag{23}$$  
Per verificare che la somma della $(23)$ si comporta come il solo termine $cg(x),$ riscriviamo la $(23)$ come segue:

$$
\frac{F(x)}{cg(x)}
=1+\frac{r(x)}{cg(x)}
\longrightarrow1
\tag{24}
$$

Il rapporto nella $(24)$ tende a $1,$ quindi $F(x)\sim cg(x).$ Per esempio, per $x\to+\infty,$ i termini dominanti del seguente rapporto seguente sono $2^x$ e $3x^3,$ per cui il limite diverge:

$$
\frac{2^x+x^{10}+\ln x}{3x^3+(\ln x)^2}
\sim\frac{2^x}{3x^3}
\longrightarrow+\infty
\tag{25}
$$

Quando invece i termini dominanti hanno lo stesso ordine, il limite può  essere finito e non nullo, come nel seguente esempio.

$$
\frac{5x^2\ln x+x^2}{2x^2\ln x+e^{-x}}
\sim\frac{5x^2\ln x}{2x^2\ln x}
=\frac52
\tag{26}
$$

Nei rapporti delle $(25)$ e $(26)$ abbiamo sostituito numeratore e denominatore con i rispettivi termini dominanti, ma quando si ha a che fare con delle differenze bisogna prestare maggiore attenzione, perché lo stesso procedimento può dare un risultato errato in quanto i termini principali possono cancellarsi. Consideriamo il seguente esempio:

$$
\lim_{x\to+\infty}\left(\sqrt{x^2+x}-x\right) \tag{27}
$$

Nella $(27),$ quando $x\to+\infty$ si ottiene che $\sqrt{x^2+x}\sim x,$ ma se si sostituisce la radice con $x$ si otterrebbe zero. Per calcolare il limite bisogna quindi utilizzare l'espressione completa e riscrivere l'espressione moltiplicando il numeratore e il denominatore per il suo coniugato:

$$
\begin{align}
\sqrt{x^2+x}-x
&=\frac{(\sqrt{x^2+x}-x)(\sqrt{x^2+x}+x)}{\sqrt{x^2+x}+x} \\[6pt]
&=\frac{x}{\sqrt{x^2+x}+x} \\[6pt]
&=\frac{1}{\sqrt{1+1/x}+1}\longrightarrow\frac12
\end{align}
\tag{28}
$$

## Infinitesimi e limiti in zero

Consideriamo ora delle funzioni che tendono a zero e sono quindi infinitesimi. Partiamo da un esempio semplice, considerando $a^x$ che cresce più rapidamente di $x^\alpha,$ e il suo reciproco $a^{-x}$ che tende a zero più rapidamente di $x^{-\alpha}.$ Infatti, il rapporto $a^{-x}/x^{-\alpha}=x^\alpha/a^x$ tende a zero per la $(15).$ Applicando lo stesso ragionamento al confronto tra potenze e logaritmi della $(14),$ per $p,\alpha>0$ e $a>1$ otteniamo:

$$
a^{-x}\ll x^{-\alpha}\ll\frac{1}{(\ln x)^p}
\qquad (x\to+\infty)
\tag{29}
$$

Per esempio, $x^\alpha e^{-x}\to0,$ poiché il prodotto si riscrive come $x^\alpha/e^x.$ Questo metodo è utile per risolvere le forme indeterminate del tipo $0\cdot\infty$ riconducendole a un confronto già noto. La stessa gerarchia permette di calcolare limiti in cui $x\to0^+$ co come nel seguente esempio:

$$
\lim_{x\to0^+}x\ln\frac1x \tag{30}
$$

Nella $(30)$ se tentiamo di risolvere il limite per sostituzione diretta otteniamo una forma indeterminata del tipo $0\cdot\infty.$ Per risolverla, applichiamo la sostituzione $t=1/x,$ da cui $x=1/t$ e otteniamo:

$$
\lim_{x\to0^+}x\ln\frac1x
=\lim_{t\to+\infty}\frac{\ln t}{t}
=0
\tag{31}
$$

Consideriamo ora un secondo esempio, con $\alpha>0:$

$$ \tag{32}
\lim_{x\to0^+}\frac{e^{-1/x}}{x^\alpha}
$$

Il numeratore e il denominatore della $(32)$ tendono entrambi a zero e applicando la stessa sostituzione di prima con $t=1/x,$ il numeratore diventa $e^{-t}$ e il denominatore $t^{-\alpha},$ e quindi otteniamo:

$$
\lim_{x\to0^+}\frac{e^{-1/x}}{x^\alpha}
=\lim_{t\to+\infty}\frac{t^\alpha}{e^t}
=0
\tag{33}
$$

La $(15)$ dà il limite nella $(33),$ che mostra come $e^{-1/x}$ tenda a zero più rapidamente di ogni potenza positiva di $x.$