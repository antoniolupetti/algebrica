---
title: Anelli
source: https://algebrica.org/rings/
license: CC BY-NC 4.0
tags:
  - abelian-group
  - algebraic-structures
  - commutative-ring
  - distributivity
  - homomorphism
  - ideal
  - integral-domain
  - polynomial-ring
  - ring-theory
  - subring
  - zero-divisor
---

## Definizione

Un anello è una struttura algebrica che estende la nozione di [gruppo](../groups/) introducendo una seconda operazione binaria. Il concetto nasce dall'osservazione che oggetti quali gli [interi](../integers/), i [polinomi](../polynomials/) a coefficienti reali e le [matrici quadrate](../matrices/) di un dato ordine hanno proprietà comuni. Ammettono un'addizione e una moltiplicazione, legate dalle leggi distributive, ma la moltiplicazione non è necessariamente commutativa e non deve necessariamente ammettere inversi. Un anello è un insieme $R$ dotato di due operazioni binarie $+$ e $\cdot$ (addizione e moltiplicazione) che soddisfano i seguenti assiomi:

+ $(R, +)$ è un gruppo abeliano. Esiste un elemento $0 \in R$ tale che $a + 0 = a$ per ogni $a \in R,$ e per ogni $a \in R$ esiste $-a \in R$ tale che $a + (-a) = 0.$
+ La moltiplicazione è associativa, ossia per ogni $a, b, c \in R,$ vale l'identità $(a \cdot b) \cdot c = a \cdot (b \cdot c).$
+ Valgono le leggi distributive, ossia per ogni $a, b, c \in R,$ si hanno le identità $a \cdot (b + c) = a \cdot b + a \cdot c$ e $(a + b) \cdot c = a \cdot c + b \cdot c.$

Un anello $(R, +, \cdot)$ si dice commutativo quando $a \cdot b = b \cdot a$ per ogni $a, b \in R.$ Si dice anello con unità, o anello unitario, quando esiste un elemento neutro moltiplicativo $1 \in R$ tale che $1 \cdot a = a \cdot 1 = a$ per ogni $a \in R.$

L'elemento neutro moltiplicativo non fa parte degli assiomi di anello adottati qui. Questa convenzione comprende anelli come $2\mathbb{Z},$ che non ha un elemento neutro moltiplicativo. I numeri naturali $\mathbb{N},$ invece, non formano un anello rispetto alle operazioni usuali, perché un intero positivo non ha un opposto in $\mathbb{N}.$

## Proprietà

Dagli assiomi seguono direttamente alcune proprietà. Per ogni $a \in R,$ la moltiplicazione per l'elemento neutro additivo soddisfa $a \cdot 0 = 0 \cdot a = 0.$ Dalla distributività si ottiene:

$$a \cdot 0 = a \cdot (0 + 0) = a \cdot 0 + a \cdot 0$$

La cancellazione di $a \cdot 0$ da entrambi i membri, consentita dalla struttura di gruppo di $(R, +),$ dimostra l'uguaglianza. Analogamente, per ogni $a, b \in R$ vale la seguente identità:

$$(-a) \cdot b = a \cdot (-b) = -(a \cdot b)$$

In particolare, $(-1) \cdot a = -a$ quando $R$ ha un'unità. Queste regole dei segni valgono in ogni anello.

Supponiamo che $R$ abbia un'unità. Un elemento $u \in R$ si dice unità, o elemento invertibile, quando esiste $v \in R$ tale che $u \cdot v = v \cdot u = 1.$ L'associatività implica che tale elemento $v$ è unico, perciò lo si indica con $u^{-1}.$ Le unità formano un gruppo rispetto alla moltiplicazione, generalmente indicato con $R^\times.$ La descrizione di questo gruppo dipende dall'anello:

+ Le unità di $\mathbb{Z}$ sono $1$ e $-1,$ poiché un'uguaglianza $ab = 1$ tra interi impone $|a| = |b| = 1.$
+ Ogni numero reale, razionale o complesso non nullo è un'unità nel rispettivo anello.
+ Una matrice in $\mathrm{M}_n(F)$ è un'unità se e solo se il suo determinante è non nullo.
+ Le unità di $\mathbb{R}[x]$ sono i polinomi costanti non nulli, poiché $\deg(fg) = \deg(f) + \deg(g)$ per polinomi non nulli.
+ Una classe di resto $[a]$ in $\mathbb{Z}/n\mathbb{Z}$ è un'unità se e solo se $\gcd(a,n) = 1.$

Per l'ultima affermazione, l'identità di Bézout fornisce interi $r$ e $s$ tali che $ra + sn = 1$ quando $\gcd(a,n) = 1.$ Riducendo modulo $n$ si ottiene $[r][a] = [1].$ Viceversa, se $[r][a] = [1],$ ogni divisore comune di $a$ e $n$ divide $1,$ quindi $a$ e $n$ sono coprimi.

Un elemento non nullo $a \in R$ si dice divisore dello zero quando esiste un elemento non nullo $b \in R$ tale che $a \cdot b = 0$ oppure $b \cdot a = 0.$ I divisori dello zero distinguono gli anelli dai campi, poiché in un [campo](../fields/) nessun elemento non nullo può essere un divisore dello zero. Un anello commutativo non nullo con unità e privo di divisori dello zero si dice dominio d'integrità.

## Gerarchia delle strutture algebriche

Un gruppo è un insieme dotato di una sola operazione binaria che soddisfa la chiusura, l'associatività, l'esistenza di un elemento neutro e l'esistenza degli inversi.

Un anello estende questa struttura introducendo una seconda operazione, la moltiplicazione, che deve essere associativa e distributiva rispetto all'addizione, ma non necessariamente commutativa o dotata di inversi.

Un [campo](../fields/) è un anello commutativo con unità tale che $1 \neq 0$ e ogni elemento non nullo abbia un inverso moltiplicativo. La condizione $1 \neq 0$ esclude l'anello nullo, nel quale l'elemento neutro additivo e quello moltiplicativo coincidono. Le tre strutture impongono requisiti via via più restrittivi:

+ Un gruppo ha una sola operazione con inversi.
+ Un anello ha due operazioni, con inversi garantiti soltanto per l'addizione.
+ Un campo ha due operazioni, con inversi garantiti per l'addizione e per la moltiplicazione degli elementi non nulli.

> Gli interi $\mathbb{Z}$ sono un esempio di anello che non è un campo. Ogni intero ha un opposto, ma $2^{-1}$ non appartiene a $\mathbb{Z}.$ I [numeri razionali](../rational-numbers/) $\mathbb{Q},$ invece, formano un campo. La stessa distinzione ricompare in algebra lineare. Gli scalari appartenenti a un anello danno luogo a un [modulo](../modules/), mentre gli scalari appartenenti a un campo danno luogo a uno [spazio vettoriale](../vector-spaces/).

## Esempi

L'insieme $\mathbb{Z}$ degli interi, dotato dell'addizione e della moltiplicazione ordinarie, è un esempio di anello commutativo con unità. L'elemento neutro additivo è $0,$ quello moltiplicativo è $1,$ e ogni intero ha un opposto. Gli interi formano un dominio d'integrità, poiché il prodotto di due interi non nulli è sempre non nullo.

Gli insiemi numerici $\mathbb{Q},$ $\mathbb{R},$ e $\mathbb{C}$ sono anelli commutativi con unità. In ciascuno di essi ogni elemento non nullo ha un inverso moltiplicativo, quindi sono campi.

L'insieme dei polinomi a coefficienti reali, indicato con $\mathbb{R}[x],$ forma un anello commutativo con unità rispetto alle operazioni usuali di addizione e moltiplicazione di polinomi. L'elemento neutro additivo è il polinomio nullo, mentre quello moltiplicativo è il polinomio costante $1.$ Questo anello è anche un dominio d'integrità. La stessa costruzione vale per i polinomi in più variabili. Per esempio, $F[x,y]$ è un anello commutativo con unità per ogni campo $F.$

Sia $X$ un insieme. Le funzioni a valori reali definite su $X$ formano un anello commutativo quando l'addizione e la moltiplicazione sono definite punto per punto:

$$(f + g)(x) = f(x) + g(x)$$

$$(fg)(x) = f(x)g(x)$$

La funzione nulla è l'elemento neutro additivo e la funzione costante di valore $1$ è quello moltiplicativo. Una funzione $f$ è un'unità se e solo se $f(x) \neq 0$ per ogni $x \in X,$ perché la sua inversa deve essere la funzione $x \mapsto 1/f(x).$

- - -

Sia $n$ un intero positivo. Il quoziente $\mathbb{Z}/n\mathbb{Z}$ è formato dalle classi di resto $[0], [1], \ldots, [n - 1].$ Dotato dell'addizione e della moltiplicazione [modulo](../modulo-operator/) $n,$ esso forma un anello commutativo con unità. Per esempio, in $\mathbb{Z}/6\mathbb{Z}$ si ha $[2][3] = [0],$ quindi $[2]$ e $[3]$ sono divisori dello zero e $\mathbb{Z}/6\mathbb{Z}$ non è un dominio d'integrità. Quando $n$ è primo, invece, $\mathbb{Z}/n\mathbb{Z}$ non contiene divisori dello zero ed è un campo. L'aritmetica delle classi di resto, insieme alle tabelle di addizione e moltiplicazione che descrivono concretamente queste operazioni, è trattata nella pagina sull'[operatore modulo](../modulo-operator/).

Sia $F$ un campo e sia $n$ un intero positivo. L'insieme $\mathrm{M}_n(F)$ di tutte le [matrici](../matrices/) $n \times n$ a coefficienti in $F$ forma un anello rispetto all'addizione e alla moltiplicazione di matrici. L'elemento neutro additivo è la matrice nulla e quello moltiplicativo è la matrice identità $I_n.$ Per $n \geq 2,$ questo anello non è commutativo, poiché il prodotto di matrici non è in generale commutativo, e contiene divisori dello zero. Sostituendo $F$ con $\mathbb{Z}$ si ottiene l'anello $\mathrm{M}_n(\mathbb{Z})$ delle matrici a coefficienti interi, quindi l'insieme dei coefficienti non deve necessariamente essere un campo.

## Sottoanelli

Un sottoinsieme $S$ di un anello $R$ si dice sottoanello quando $S$ è a sua volta un anello rispetto alle operazioni ereditate da $R.$ Un sottoinsieme non vuoto $S \subseteq R$ è un sottoanello di $R$ se e solo se è chiuso rispetto alla sottrazione e alla moltiplicazione, ossia se per ogni $a, b \in S$ si ha $a - b \in S$ e $a \cdot b \in S.$ La chiusura rispetto alla sottrazione equivale a richiedere che $S$ sia un sottogruppo di $(R, +),$ mentre la chiusura rispetto alla moltiplicazione garantisce che anche la seconda operazione sia ben definita su $S.$ Ogni anello $R$ contiene i seguenti sottoanelli canonici:

+ Il sottoanello banale $\{\ 0 \ \}$
+ $R$ stesso

Ogni sottoanello diverso da $R$ si dice proprio.

Questi due sottoanelli coincidono quando $R$ è l'anello nullo. Un esempio di sottoanello proprio è l'insieme degli interi pari $2\mathbb{Z} = \{\ \ldots, -4, -2, 0, 2, 4, \ldots \ \}$ che è un sottoanello di $(\mathbb{Z}, +, \cdot).$ Per ogni coppia di interi pari $a = 2m$ e $b = 2k,$ si ha $a - b = 2(m - k) \in 2\mathbb{Z}$ e $a \cdot b = 4mk \in 2\mathbb{Z},$ quindi entrambe le condizioni sono soddisfatte. L'insieme $2\mathbb{Z}$ non contiene l'unità moltiplicativa $1$ di $\mathbb{Z},$ e mostra che un sottoanello di un anello unitario può non essere unitario.

Si ottengono sottoanelli anche restringendo i coefficienti o imponendo condizioni conservate dalle operazioni dell'anello. L'inclusione $\mathbb{Q} \subseteq \mathbb{R}$ rende $\mathrm{M}_n(\mathbb{Q})$ un sottoanello di $\mathrm{M}_n(\mathbb{R}).$ Le matrici triangolari superiori in $\mathrm{M}_n(\mathbb{R})$ formano un altro sottoanello, perché somme, opposti e prodotti di matrici triangolari superiori sono ancora triangolari superiori. Analogamente, le funzioni continue da $\mathbb{R}$ a $\mathbb{R}$ formano un sottoanello dell'anello di tutte le funzioni a valori reali su $\mathbb{R},$ poiché somme, opposti e prodotti di funzioni continue sono continui.

## Ideali

Gli ideali sono i sottoinsiemi che consentono di costruire gli anelli quoziente, in modo analogo ai sottogruppi normali nella teoria dei gruppi. Un sottoinsieme non vuoto $I \subseteq R$ si dice ideale sinistro di $R$ quando è chiuso rispetto all'addizione, al passaggio all'opposto e alla moltiplicazione a sinistra per elementi di $R,$ ossia quando, per ogni $a \in I$ e $r \in R$ l'elemento $r \cdot a$ appartiene a $I.$ Un ideale destro si definisce analogamente usando la moltiplicazione a destra. Un sottoinsieme che è sia un ideale sinistro sia un ideale destro si dice ideale bilatero, o semplicemente ideale.

L'insieme $n\mathbb{Z}$ di tutti i multipli di un intero fissato $n$ è un ideale di $\mathbb{Z}.$ Infatti, è chiuso rispetto all'addizione e al passaggio all'opposto e, per ogni $a = nk \in n\mathbb{Z}$ e ogni $r \in \mathbb{Z}$ si ha:

$$r \cdot a = n(rk) \in n\mathbb{Z}$$

> Gli ideali sono esattamente i nuclei degli omomorfismi di anelli. Questa proprietà permette di costruire gli anelli quoziente e di studiare gli anelli attraverso le loro immagini omomorfe.

## Omomorfismi e isomorfismi di anelli

Un omomorfismo di anelli è una [funzione](../functions/) tra due anelli che conserva entrambe le operazioni. Dati due anelli $(R, +, \cdot)$ e $(S, \oplus, \odot),$ una funzione $\varphi : R \to S$ è un omomorfismo di anelli quando, per ogni $a, b \in R$ valgono le identità:

$$\varphi(a + b) = \varphi(a) \oplus \varphi(b)$$

$$\varphi(a \cdot b) = \varphi(a) \odot \varphi(b)$$

La prima condizione richiede che $\varphi$ sia un [omomorfismo di gruppi](../groups/) tra i gruppi additivi, mentre la seconda richiede che conservi la moltiplicazione. Di conseguenza, $\varphi$ manda l'elemento neutro additivo di $R$ nell'elemento neutro additivo di $S.$ Quando entrambi gli anelli sono unitari, spesso si richiede inoltre che $\varphi(1_R) = 1_S.$ Il [nucleo](../homomorphisms-and-isomorphisms/) e l'immagine di un omomorfismo di anelli $\varphi : R \to S$ si definiscono come nel caso dei gruppi:

$$\ker(\varphi) = \{\ a \in R : \varphi(a) = 0_S \ \}$$

$$\mathrm{im}(\varphi) = \{\ \varphi(a) : a \in R \ \}$$

Il nucleo è sempre un ideale di $R,$ e l'immagine è sempre un sottoanello di $S.$ Un omomorfismo è iniettivo se e solo se il suo nucleo contiene soltanto l'elemento neutro additivo di $R.$

La valutazione di polinomi in una matrice fornisce un altro esempio. Fissiamo una matrice $T \in \mathrm{M}_n(\mathbb{R})$ e definiamo la seguente applicazione.

$$\mathrm{ev}_T : \mathbb{R}[x] \to \mathrm{M}_n(\mathbb{R})$$

$$a_0 + a_1x + \cdots + a_mx^m \mapsto a_0I_n + a_1T + \cdots + a_mT^m$$

Per due polinomi $p$ e $q,$ le identità $(p + q)(T) = p(T) + q(T)$ e $(pq)(T) = p(T)q(T)$ seguono dalle leggi del prodotto di matrici e dalla regola $T^iT^j = T^{i+j}.$ Pertanto $\mathrm{ev}_T$ è un omomorfismo di anelli. Quando $n = 1,$ questa costruzione si riduce alla valutazione ordinaria in un numero reale.

- - -

Un omomorfismo di anelli iniettivo e suriettivo si dice isomorfismo di anelli. Due anelli sono isomorfi, e si scrive $R \cong S,$ quando esiste un isomorfismo tra essi. Anelli isomorfi hanno la stessa struttura algebrica e condividono tutte le proprietà intrinseche alla loro struttura di anello.

Consideriamo, per esempio, l'applicazione $\varphi : \mathbb{Z} \to \mathbb{Z}/n\mathbb{Z}$ definita da $\varphi(a) = a \bmod n.$ Essa conserva entrambe le operazioni, poiché la classe di resto di una somma coincide con la somma delle classi di resto in $\mathbb{Z}/n\mathbb{Z},$ e lo stesso vale per il prodotto. È quindi un omomorfismo di anelli e il suo nucleo è esattamente $n\mathbb{Z},$ l'ideale dei multipli di $n.$

Due anelli $R$ e $S$ determinano una struttura di anello sul prodotto cartesiano $R \times S$ mediante operazioni definite componente per componente:

$$(r,s) + (r',s') = (r + r',s + s')$$

$$(r,s)(r',s') = (rr',ss')$$

Per due fattori questo anello si indica anche con $R \oplus S.$ Se $a$ e $b$ sono interi positivi coprimi, consideriamo la seguente applicazione.

$$
\Phi : \mathbb{Z}/ab\mathbb{Z} \to
\mathbb{Z}/a\mathbb{Z} \oplus \mathbb{Z}/b\mathbb{Z}$$

$$[x]_{ab} \mapsto ([x]_a,[x]_b)$$

Questa applicazione è un isomorfismo di anelli. È ben definita perché $x \equiv y \pmod{ab}$ implica sia $x \equiv y \pmod a$ sia $x \equiv y \pmod b,$ e le operazioni componente per componente mostrano che conserva somme e prodotti. Se $\Phi([x]_{ab}) = ([0]_a,[0]_b),$ allora sia $a$ sia $b$ dividono $x.$ Poiché $\gcd(a,b) = 1,$ il loro prodotto divide $x,$ quindi $[x]_{ab} = [0]_{ab}$ e $\Phi$ è iniettiva. Il teorema cinese del resto fornisce, per ogni coppia $([r]_a,[s]_b),$ un intero $x$ che soddisfa $x \equiv r \pmod a$ e $x \equiv s \pmod b.$ Pertanto $\Phi$ è suriettiva. Questa formulazione esprime un sistema di congruenze come un isomorfismo tra anelli.

> Richiedendo che $1 \neq 0$ e che ogni elemento non nullo sia invertibile, un anello commutativo con unità diventa un [campo](../fields/), la struttura sulla quale si sviluppa la teoria degli [spazi vettoriali](../vector-spaces/). La pagina sugli [omomorfismi e isomorfismi](../homomorphisms-and-isomorphisms/) tratta le applicazioni che conservano le operazioni nelle principali strutture algebriche.
