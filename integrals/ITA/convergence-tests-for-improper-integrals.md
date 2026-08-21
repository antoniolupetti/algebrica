---
title: Convergence Tests for Improper Integrals
source: https://algebrica.org/convergence-tests-for-improper-integrals/
license: CC BY-NC 4.0
tags:
  - abel-test
  - absolute-convergence
  - cauchy-criterion
  - cauchy-principal-value
  - conditional-convergence
  - dirichlet-test
  - fresnel-integrals
  - improper-integrals
  - oscillating-integrands
  - second-mean-value-theorem
---
In questa voce ci occuperemo dei criteri di convergenza degli integrali impropri che rappresentano una famiglia di integrali in cui uno o entrambi gli estremi di integrazione sono $\pm \infty$ oppure l'integranda è illimitata presso un estremo finito. Ricorderete che questi integrali non possono essere valutati con la mera differenza del valore delle rispettive primitive agli estremi, in quanto una quantità infinita renderebbe impossibile questo calcolo. Per tale ragione si ricorre a studiarne il limite nella tipica forma:

$$\int_a^{+\infty} f(x) \ dx := \lim_{t \to +\infty} \int_a^t f(x) \ dx \tag{1}$$

Nella voce dedicata agli integrali impropri sono stati esposti i criteri del confronto, diretto e asintotico, che stabiliscono la convergenza senza calcolare la primitiva. Quei criteri, nella forma esposta, richiedono però una funzione integranda di segno costante e non determinano la convergenza condizionata quando l'integranda oscilla, perché in tal caso la convergenza dipende dalla compensazione fra i contributi positivi e negativi. I criteri raccolti in questa voce trattano proprio questo caso.

## Il criterio di Cauchy

Il primo Criterio è quello di Cauchy, che come vedremo non richiede ipotesi di segno della funzione e, questo è fondamentale, non fornisce il valore dell'integrale, ma solo la sua convergenza. Consideriamo, quindi, una funzione $f$ integrabile secondo Riemann su ogni intervallo $[a,t]$ con $t\gt a,$ e sia $F$ la sua funzione integrale:

$$F(t):=\int_a^t f(x) \ dx$$

Richiamando il concetto di convergenza, l'integrale improprio converge solo quando $F$ ammette un limite finito per $t\to+\infty.$ Consideriamo quindi l'integrale visto nella $(1)$:

$$\int_a^{+\infty}f(x) \ dx$$ 

Questo integrale converge se e solo se per ogni $\varepsilon\gt0$ esiste $c\geq a$ tale che:

$$\left|\int_u^v f(x) \ dx\right|\lt\varepsilon \qquad v\gt u\gt c \tag{2}$$

Gli estremi $u$ e $v$ sono arbitrari, purché entrambi maggiori della soglia $c,$ che si sceglie in funzione di $\varepsilon.$


- - -

Un criterio analogo alla $(2)$ vale anche per un singolo estremo finito. Supponiamo infatti che $f$ sia integrabile secondo Riemann su ogni intervallo $[t,b]$ con $a\lt t\lt b$ e illimitata in ogni intorno destro di $a.$ Consideriamo l'integrale:

$$\int_a^b f(x) \ dx$$ 
Questo integrale converge se e solo se per ogni $\varepsilon\gt0$ esiste un $\delta\gt0$ tale che:

$$\left|\int_u^v f(x) \ dx\right|\lt\varepsilon \qquad a\lt u\lt v\lt a+\delta \tag{3}$$

Una conseguenza immediata della $(3)$ è che la convergenza assoluta, ovvero la convergenza dell'integrale del valore assoluto dell'integranda, implica la convergenza semplice. Dalla disuguaglianza si ha:

$$\left|\int_u^v f(x) \ dx\right|\leq\int_u^v|f(x)| \ dx$$

Da questa segue che la condizione di Cauchy soddisfatta da $|f|$ è soddisfatta anche da $f.$

## Il criterio di Dirichlet

Un secondo criterio per valutare la convergenza di un integrale improprio di una funzione oscillante è quello di Dirichlet che considera due funzioni $f$ e $g$ definite su un intervallo $[a,+\infty),$ con $f$ integrabile secondo Riemann su ogni intervallo $[a,t]$ e $g$ monotona. Consideriamo la funzione integrale:

$$F(t)=\int_a^t f(x) \ dx \tag{4}$$ 
Il criterio richiede due ipotesi preliminari:

+ La prima è che $F(t)$ sia limitata, cioè deve valere $|F(t)|\leq K$ per ogni $t\geq a.$
+ La seconda ipotesi è che $g(x)\to0$ per $x\to+\infty$

Consideriamo adesso l'integrale:

$$\int_a^{+\infty}f(x)g(x) \ dx \tag{5}$$

Se le suddette ipotesi sono soddisfatte l'integrale  converge.

- - - 

Per dimostrarlo supponiamo $K\gt0$ e fissiamo $v\gt u\geq a.$ Il secondo teorema della media fornisce un punto $\xi\in[u,v]$ per cui vale la seguente identità:

$$\int_u^v f(x)g(x) \ dx=g(u)\int_u^{\xi}f(x) \ dx+g(v)\int_{\xi}^v f(x) \ dx \tag{6}$$

Possiamo esprimere i due integrali parziali nel membro a destra dell'uguaglianza in funzione delle rispettive primitive, come:

$$\left|\int_u^{\xi}f(x) \ dx\right|=|F(\xi)-F(u)|\leq2K$$

$$\left|\int_{\xi}^v f(x) \ dx\right|=|F(v)-F(\xi)|\leq2K$$

Sostituendo le precedenti uguaglianze nella $(6)$ si ottiene:

$$\left|\int_u^v f(x)g(x) \ dx\right|\leq2K\big(|g(u)|+|g(v)|\big)$$

Fissiamo $\varepsilon\gt0.$ Ricordando la seconda ipotesi, $g$ è infinitesima e pertanto esiste $c\geq a$ tale che $|g(x)|\lt\varepsilon/(4K)$ per ogni $x\geq c.$ Se $v\gt u\geq c,$ entrambi i valori $|g(u)|$ e $|g(v)|$ rispettano questa disuguaglianza, e la precedente maggiorazione diventa:

$$\left|\int_u^v f(x)g(x) \ dx\right|\leq2K\left(|g(u)|+|g(v)|\right)\lt2K\left(\frac{\varepsilon}{4K}+\frac{\varepsilon}{4K}\right)=\varepsilon$$

Il criterio di Cauchy dà quindi la convergenza dell'integrale $(5)$.

## Il criterio di Abel

Il criterio di Abel introduce una variazione al criterio di Dirichlet rinunciando all'ipotesi che la funzione $g$ sia infinitesima. Consideriamo quindi $f$ e $g$ definite su $[a,+\infty),$ con $f$ integrabile secondo Riemann su ogni intervallo $[a,t]$ e $g$ monotona e limitata. Assumiamo poi la convergenza del seguente integrale:

$$\int_a^{+\infty}f(x) \ dx \tag{7}$$ 
Da queste premesse si può concludere che il seguente integrale converge:

$$\int_a^{+\infty}f(x)g(x) \ dx$$ 
La dimostrazione non è particolarmente complicata e riconduce l'enunciato al criterio di Dirichlet. Se un funzione monotona e limitata ammette limite finito $L$ per $x\to+\infty,$ la funzione $h=g-L$ è allora monotona e infinitesima. La funzione integrale $F$ è quindi continua e ha limite finito per $t\to+\infty,$ dunque è limitata su $[a,+\infty).$ Il criterio di Dirichlet applicato alla coppia $f$ e $h$ garantisce la convergenza di: 

$$\int_a^{+\infty}f(x)h(x) \ dx$$ 
Dalla decomposizione si ottiene che:

$$f(x)g(x)=f(x)h(x)+Lf(x)$$

Pertanto dalla convergenza di $(7)$ segue la tesi.

## Integrali nella funzione seno

Nella pratica esiste una famiglia di integrali che coinvolge la funzione seno piuttosto nota che è data dalla seguente espressione:

$$\int_1^{+\infty}\frac{\sin x}{x^p} \ dx \tag{8}$$

In questo caso, per ogni $p\gt0$ le ipotesi del criterio di Dirichlet sono soddisfatte dalla coppia $f(x)=\sin x$ e $g(x)=x^{-p}.$ Inoltre, la funzione integrale di $f$ è limitata secondo la seguente relazione:

$$\left|\int_1^t\sin x \ dx\right|=|\cos1-\cos t|\leq2$$

$x^{-p}$ è invece decrescente e infinitesima. Da questo si deduce che l'integrale $(8)$ converge quindi per ogni $p\gt0.$

- - -

Se vogliamo studiare la convergenza assoluta della $(8)$, questa richiede una condizione più restrittiva. Per $p\gt1$ dobbiamo considerare la seguente maggiorazione:

$$|\sin x|/x^p\leq1/x^p$$ 
Tale maggiorazione e il criterio del $p$-integral ne determinano la convergenza assoluta. Per $0\lt p\leq1$ l'integrale del valore assoluto diverge. Dalla disuguaglianza $\sin^2x\leq|\sin x|$ e dall'identità $\sin^2x=(1-\cos2x)/2$ segue:

$$\int_1^T\frac{|\sin x|}{x^p} \ dx\geq\frac{1}{2}\int_1^T\frac{dx}{x^p}-\frac{1}{2}\int_1^T\frac{\cos2x}{x^p} \ dx$$

Il primo integrale a destra tende a $+\infty$ perché $p\leq1,$ mentre il secondo converge per il criterio di Dirichlet, dato che $\int_1^t\cos2x \ dx$ è limitato e $x^{-p}$ è infinitesima. Il membro destro tende quindi a $+\infty$ e per $0\lt p\leq1$ l'integrale $(8)$ converge semplicemente.

Per $p\leq0$ il criterio di Cauchy fallisce. Consideriamo un valore $k$ intero positivo e poniamo il seguente intervallo:

$$I_k=[2k\pi+\pi/6,\ 2k\pi+5\pi/6]$$ 

Su tale intervallo vale $\sin x\geq1/2,$ e da $p\leq0$ segue $x^{-p}\geq1$ per $x\geq1,$ quindi:

$$\int_{I_k}\frac{\sin x}{x^p} \ dx\geq\frac{1}{2}\cdot\frac{2\pi}{3}=\frac{\pi}{3}$$

Gli estremi di $I_k$ tendono a $+\infty$ mentre l'integrale esteso a $I_k$ si allontana dallo zero e quindi l'integrale $(8)$ non converge. In sintesi possiamo quindi sintetizzare i casi come riportato nella tabella:

[class="table-1"]

|              |                          |
| ------------ | ------------------------ |
| $p\gt1$        | converge assolutamente   |
| $0\lt p\leq1$   | converge semplicemente   |
| $p\leq0$     | non converge             |

[/class]

## Gli integrali di Fresnel

Il criterio di Dirichlet vale anche per gli integrali di Fresnel, le cui integrande non sono infinitesime. Questi integrali sono del tipo
$$\int_0^{+\infty}\sin(x^2) \ dx=\int_0^{+\infty}\cos(x^2) \ dx=\frac{1}{2}\sqrt{\frac{\pi}{2}}$$

Facciamo il caso del seno:

$$\int_0^{+\infty}\sin(x^2) \ dx \tag{9}$$

Sull'intervallo $[0,1]$ la funzione integranda è continua e l'integrale è proprio. Sull'intervallo $[1,T]$ effettuiamo la [sostituzione](../integration-by-substitution/) $t=x^2,$ con $x=\sqrt t$ e $dx=dt/(2\sqrt t),$ ottenendo:

$$\int_1^T\sin(x^2) \ dx=\frac{1}{2}\int_1^{T^2}\frac{\sin t}{\sqrt t} \ dt$$

Il membro destro ammette limite finito per $T\to+\infty$ perché è il caso $p=1/2$ della famiglia $(8).$ Sommando l'integrale proprio su $[0,1]$ si conclude che $(9)$ converge. Poiché $p=1/2\lt1,$ l'integrale del valore assoluto diverge e la convergenza è semplice. La stessa sostituzione si può applicare a $\cos(x^2)$ portando alle medesime conclusioni.

I due integrali sono noti come integrali di Fresnel e hanno lo stesso valore:

$$\int_0^{+\infty}\sin(x^2) \ dx=\int_0^{+\infty}\cos(x^2) \ dx=\frac{1}{2}\sqrt{\frac{\pi}{2}}$$

Il calcolo di questo valore può essere effettuato con metodi di analisi complessa.

> Vale la pena richiamare che per le [serie](../cauchy-convergence-criterion-series/) la convergenza di $\sum a_n$ impone $a_n\to0$ mentre per gli integrali impropri non vale l'analogo, e $\sin(x^2)$ ne è il controesempio: oscilla fra $-1$ e $1$ senza ammettere limite, eppure il suo integrale converge. Il periodo delle oscillazioni si accorcia come $\pi/x,$ quindi le aree dei lobi consecutivi hanno segno alterno e modulo decrescente a zero, e i loro contributi si sommano come i termini di una [serie a segni alterni](../leibniz-criterion/).

## Il valore principale di Cauchy

Per concludere introduciamo il valore principale di Cauchy che esprime il limite degli integrali estesi a intervalli simmetrici rispetto all'origine, ed è dato dalla seguente espressione:

$$\mathrm{v.p.}\int_{-\infty}^{+\infty}f(x) \ dx:=\lim_{R\to+\infty}\int_{-R}^{R}f(x) \ dx$$

Prendiamo ad esempio la seguente funzione dispari:

$$f(x)=\frac{2x}{1+x^2}$$

Consideriamo adesso l'integrale improprio esteso a tutto $\mathbb{R}$: $$\int_{-\infty}^{+\infty}\frac{2x}{1+x^2} \ dx$$
Questo integrale non converge, perché per ogni $R$ abbiamo

$$\int_0^R f(x) \ dx=\ln(1+R^2) \to +\infty$$

$$\int_{-R}^R f(x) \ dx=0$$Quindi il valore principale è nullo.

Se invece un generico integrale improprio converge, il valore principale esiste e coincide con esso, poiché la coppia simmetrica di limiti è un caso particolare dei due limiti indipendenti. Il viceversa invece è falso, come mostra l'esempio precedente.
