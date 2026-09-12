---
title: Lógica proposicional
source: https://algebrica.org/propositional-logic/
license: CC BY-NC 4.0
tags:
  - atomic-proposition
  - conjunctive-normal-form
  - contradiction
  - deductive-closure
  - disjunctive-normal-form
  - inference-rules
  - interpretation
  - logical-connective
  - logical-consequence
  - logical-equivalence
  - modus-ponens
  - modus-tollens
  - propositional-constants
  - propositional-logic
  - satisfiability
  - semantics
  - tautology
  - truth-table
  - valuation
  - well-formed-formula
---

## Lenguaje proposicional

La lógica proposicional estudia los argumentos cuya validez depende del modo en que las conectivas proposicionales combinan proposiciones. Considera cada proposición atómica verdadera o falsa y determina el valor de verdad de una proposición compuesta a partir de los valores de verdad de sus componentes.

El contenido de una proposición atómica es irrelevante para este cálculo. Si un argumento tiene la forma $p,$ $p \rightarrow q,$ por tanto $q,$ su validez depende de esa forma, con independencia de las proposiciones representadas por $p$ y $q.$ Esta restricción confiere precisión a la lógica proposicional, pero también limita lo que el lenguaje puede expresar.

Un lenguaje proposicional $\mathrm{Prop}[P]$ tiene símbolos atómicos, conectivas lógicas y paréntesis. El conjunto $P$ contiene los símbolos de proposición atómica; por ejemplo, $P = \{p, q, r\}.$ Los paréntesis indican cómo agrupan las conectivas las fórmulas.

El lenguaje empleado aquí tiene las conectivas siguientes:

+ Negación $\neg$
+ Conjunción $\wedge$
+ Disyunción $\lor$
+ Condicional material $\rightarrow$
+ Bicondicional material $\leftrightarrow$
+ Disyunción exclusiva $\oplus$

La elección de las conectivas primitivas es convencional. El bicondicional y la disyunción exclusiva pueden definirse a partir de otras conectivas, pero el uso de símbolos propios abrevia las fórmulas habituales.

El lenguaje también tiene dos constantes proposicionales, $\top$ y $\bot.$ La primera es verdadera bajo toda interpretación y la segunda es falsa bajo toda interpretación. No toman argumentos, por lo que son conectivas de aridad cero, y cada una tiene el valor de verdad de una fórmula compuesta: $\top$ tiene el de $p \lor \neg p$ y $\bot$ el de $p \wedge \neg p.$

Una fórmula construida con los símbolos de $P$ de acuerdo con las reglas de formación es una fórmula bien formada (FBF). Las proposiciones atómicas son las FBF más sencillas, mientras que cualquier otra FBF tiene una o más FBF como componentes inmediatos.

## Conectivas lógicas

Una conectiva es veritativo-funcional cuando los valores de verdad de sus componentes inmediatos determinan de manera unívoca el valor de verdad de la fórmula compuesta. Todas las conectivas de $\mathrm{Prop}[P]$ son veritativo-funcionales.

+ La negación $\neg p$ es verdadera precisamente cuando $p$ es falsa.
+ La conjunción $p \wedge q$ es verdadera precisamente cuando $p$ y $q$ son ambas verdaderas.
+ La disyunción $p \lor q$ es verdadera precisamente cuando al menos una de $p$ y $q$ es verdadera. La conectiva $\lor$ tiene sentido inclusivo, por lo que $p \lor q$ también es verdadera cuando ambos disyuntos son verdaderos.
+ El condicional material $p \rightarrow q$ es falso precisamente cuando su antecedente $p$ es verdadero y su consecuente $q$ es falso.
+ El bicondicional material $p \leftrightarrow q$ es verdadero precisamente cuando $p$ y $q$ tienen el mismo valor de verdad.
+ La disyunción exclusiva $p \oplus q$ es verdadera precisamente cuando $p$ y $q$ tienen valores de verdad distintos.

El sentido de un condicional requiere atención. La proposición «$p$ solo si $q$» es $p \rightarrow q,$ mientras que «$p$ si $q$» es $q \rightarrow p.$ En la primera fórmula, $p$ es una condición suficiente para $q,$ y $q$ es una condición necesaria para $p.$

El lenguaje ordinario contiene conectivas que no son veritativo-funcionales. La verdad de «es necesario que $p$» no viene determinada únicamente por la verdad de $p$. Palabras como «pero» y «aunque» pueden expresar un contraste que la conjunción no conserva, mientras que un condicional contrafáctico no es, en general, veritativo-funcional. Una simbolización en lógica proposicional solo conserva la estructura veritativo-funcional de la proposición original.

## Ejemplo de simbolización

Consideremos un lenguaje proposicional $\mathrm{Prop}[P]$ sobre $P = \{p, q\},$ con la siguiente clave de simbolización:

+ $p =$ la puerta está abierta.
+ $q =$ la ventana está abierta.

Las dos proposiciones atómicas y las conectivas bastan para simbolizar varias proposiciones compuestas.

+ La puerta no está abierta se escribe $\neg p.$
+ La puerta y la ventana están abiertas se escribe $p \wedge q.$
+ La puerta o la ventana están abiertas, quizá ambas, se escribe $p \lor q.$
+ Si la puerta está abierta, entonces la ventana está abierta se escribe $p \rightarrow q.$
+ La puerta está abierta si y solo si la ventana está abierta se escribe $p \leftrightarrow q.$
+ O bien la puerta o bien la ventana está abierta, pero no ambas, se escribe $p \oplus q.$
+ Ni la puerta ni la ventana están abiertas se escribe $\neg(p \lor q).$
+ La negación del condicional «si la puerta está abierta, entonces la ventana está abierta» se escribe $\neg(p \rightarrow q).$

Los paréntesis son necesarios en las dos últimas fórmulas porque el alcance de la negación es la fórmula compuesta completa. Por tanto, $\neg(p \lor q)$ difiere de $\neg p \lor q.$

## Reglas de formación

Las reglas de formación constituyen una definición inductiva de las FBF de $\mathrm{Prop}[P].$

+ Toda proposición atómica $p \in P$ es una FBF, y las constantes $\top$ y $\bot$ son FBF.
+ Si $\varphi$ es una FBF, entonces $\neg\varphi$ es una FBF.
+ Si $\varphi$ y $\psi$ son FBF, entonces son FBF $(\varphi \wedge \psi),$ $(\varphi \lor \psi),$ $(\varphi \rightarrow \psi),$ $(\varphi \leftrightarrow \psi),$ así como $(\varphi \oplus \psi)$.
+ Ninguna otra expresión es una FBF.

La última cláusula excluye toda cadena que no pueda obtenerse mediante un número finito de aplicaciones de las cláusulas anteriores. Estas cláusulas también determinan la estructura de cada fórmula. Toda FBF compuesta tiene una única conectiva principal, que es la conectiva aplicada en el último paso de su construcción.

Omitimos el par de paréntesis exterior cuando no se produce ninguna ambigüedad. Conforme a esta convención, la conectiva principal de $\neg(p \wedge q)$ es $\neg,$ mientras que la conectiva principal de $\neg p \wedge q$ es $\wedge.$ El alcance de una aparición de una conectiva es la subfórmula a la que se aplica esa aparición. Por tanto, los paréntesis determinan tanto la conectiva principal como el alcance de las conectivas interiores.

Otras dos convenciones permiten eliminar los paréntesis restantes. Las conectivas tienen un orden de precedencia, desde la que liga con mayor fuerza hasta la que liga con menor fuerza:

$$
\neg \quad \wedge \quad \lor \quad \rightarrow \quad \leftrightarrow
$$

Por tanto, la fórmula $\neg p \wedge q \rightarrow r$ es una abreviación de $((\neg p) \wedge q) \rightarrow r.$ Las conectivas con la misma precedencia se asocian por la izquierda, de modo que $p \wedge q \wedge r$ abrevia $(p \wedge q) \wedge r.$ La agrupación es irrelevante para $\wedge$ y $\lor,$ que son asociativas, pero no lo es para $\rightarrow.$ Bajo $M(p) = M(q) = M(r) = F$ la fórmula $(p \rightarrow q) \rightarrow r$ es falsa, mientras que $p \rightarrow (q \rightarrow r)$ es verdadera.

> Algunos textos interpretan por la derecha una cadena de condicionales, de modo que $p \rightarrow q \rightarrow r$ abrevia $p \rightarrow (q \rightarrow r).$ Las dos convenciones discrepan; los paréntesis explícitos en los condicionales anidados evitan la ambigüedad.

## Semántica

La semántica de la lógica proposicional tiene dos valores de verdad:

$$
\mathrm{Bool} := \{\ T, F\ \}
$$

Las constantes reciben siempre el mismo valor: $T$ para $\top$ y $F$ para $\bot.$ Las tablas de verdad características definen las conectivas. La tabla conjunta de las seis conectivas es la siguiente:

$$
\begin{array}{cc|cccccc}
p & q & \neg p & p \wedge q & p \lor q & p \rightarrow q & p \leftrightarrow q & p \oplus q \\[6pt]
\hline
T & T & F & T & T & T & T & F \\[6pt]
T & F & F & F & T & F & F & T \\[6pt]
F & T & T & F & T & T & F & T \\[6pt]
F & F & T & F & F & T & T & F
\end{array}
$$

Una tabla de verdad completa tiene una fila por cada asignación de valores de verdad a las distintas proposiciones atómicas de una fórmula. Si una fórmula contiene $n$ proposiciones atómicas distintas, su tabla de verdad completa tiene $2^n$ filas. La columna situada bajo la conectiva principal contiene el valor de verdad de la fórmula completa para cada asignación.

La tabla también proporciona las equivalencias lógicas siguientes:

+ $p \rightarrow q \equiv \neg p \lor q$
+ $p \leftrightarrow q \equiv (p \rightarrow q) \wedge (q \rightarrow p)$
+ $p \oplus q \equiv (p \lor q) \wedge \neg(p \wedge q)$

El símbolo $\equiv$ es una relación del metalenguaje entre fórmulas. Significa que las fórmulas tienen el mismo valor de verdad bajo toda asignación. El símbolo no es otra conectiva de $\mathrm{Prop}[P].$

## Interpretaciones

Una interpretación, también denominada valoración en lógica proposicional, es una función que asigna un valor de verdad a cada proposición atómica de $P$:

$$
M : P \rightarrow \{T, F\}
$$

El valor de una fórmula compuesta bajo $M$ queda entonces determinado recursivamente por su formación y por las tablas de verdad de las conectivas.

+ Si $\varphi$ es verdadera bajo $M,$ escribimos $M \models \varphi$ y decimos que $M$ es un modelo de $\varphi.$
+ Si $\varphi$ es falsa bajo $M,$ escribimos $M \not\models \varphi$ y decimos que $M$ es un contramodelo de $\varphi.$

Consideremos la interpretación en la que $p$ es verdadera y $q$ es falsa. A la fórmula $p \rightarrow \neg q$ le corresponde la fila siguiente:

$$
\begin{array}{cc|cc}
p & q & \neg q & p \rightarrow \neg q \\[6pt]
\hline
T & F & T & T
\end{array}
$$

Bajo esta interpretación, el antecedente $p$ y el consecuente $\neg q$ son verdaderos. En consecuencia, $p \rightarrow \neg q$ es verdadera, y $M \models p \rightarrow \neg q.$

Las nociones siguientes se definen cuantificando sobre las interpretaciones.

+ Una fórmula $\varphi$ es satisfacible si alguna interpretación la satisface.
+ Una fórmula $\varphi$ es una tautología si toda interpretación la satisface.
+ Una fórmula $\varphi$ es una contradicción si ninguna interpretación la satisface.
+ Una fórmula $\varphi$ es contingente si alguna interpretación la satisface y alguna interpretación no la satisface.

Por tanto, toda tautología y toda fórmula contingente es satisfacible, mientras que toda contradicción es insatisfacible. Un conjunto de fórmulas $S$ es conjuntamente satisfacible si alguna interpretación satisface todas las fórmulas de $S.$ Si no existe tal interpretación, $S$ es conjuntamente insatisfacible, o inconsistente.

Dos fórmulas $\varphi$ y $\psi$ son lógicamente equivalentes cuando coinciden bajo toda interpretación:

$$
\varphi \equiv \psi \Longleftrightarrow \forall M \ (M \models \varphi \Longleftrightarrow M \models \psi)
$$

## Consecuencia lógica

Una fórmula $\varphi$ es consecuencia lógica de un conjunto de fórmulas $S$ si toda interpretación que satisface todas las fórmulas de $S$ también satisface $\varphi.$ Esta relación se escribe del modo siguiente:

$$
S \models \varphi
$$

De forma equivalente, ninguna interpretación hace verdaderas todas las fórmulas de $S$ y mantiene $\varphi$ falsa. El símbolo $\models$ es una relación del metalenguaje, mientras que $\rightarrow$ es una conectiva que forma una nueva fórmula. Para dos fórmulas $\varphi$ y $\psi,$ la relación entre ambas es la siguiente:

$$
\varphi \models \psi \Longleftrightarrow \models \varphi \rightarrow \psi
$$

Consideremos el conjunto $S = \{p, p \rightarrow q\}$ y la consecuencia propuesta $q.$ La tabla de verdad pertinente es la siguiente:

$$
\begin{array}{cc|c}
p & q & p \rightarrow q \\[6pt]
\hline
T & T & T \\[6pt]
T & F & F \\[6pt]
F & T & T \\[6pt]
F & F & T
\end{array}
$$

Solo la primera fila hace verdaderos ambos miembros de $S$ y esa fila también hace verdadera $q$. Por tanto, $S \models q.$ La regla de inferencia correspondiente es el modus ponens.

Una tercera formulación de la relación sustituye el examen de los modelos de $S$ por una cuestión acerca de un único conjunto de fórmulas:

$$
S \models \varphi \Longleftrightarrow S \cup \{\neg\varphi\} \ \text{es insatisfacible}
$$

Supongamos que $S \models \varphi$ y sea $M$ una interpretación que satisface todas las fórmulas de $S \cup \{\neg\varphi\}.$ De $M \models S$ obtenemos $M \models \varphi,$ mientras que $M \models \neg\varphi$ da $M \not\models \varphi,$ y las dos conclusiones son incompatibles. Recíprocamente, supongamos que $S \cup \{\neg\varphi\}$ es insatisfacible y sea $M \models S.$ Si $\varphi$ fuese falsa bajo $M,$ entonces $M$ satisfaría $\neg\varphi$ y, por tanto, el conjunto completo. En consecuencia, todo modelo de $S$ es un modelo de $\varphi.$ Los [procedimientos de deducción automatizada](../automated-deduction-in-propositional-logic/) comprueban el miembro derecho, pues es posible buscar mecánicamente una demostración de insatisfacibilidad.

## Reglas de inferencia

Una regla de inferencia es un esquema para obtener una conclusión a partir de una o más premisas. Si $S \vdash \varphi,$ entonces $\varphi$ tiene una derivación a partir de premisas de $S$ dentro del sistema de demostración elegido. El símbolo $\vdash$ se refiere a las derivaciones, mientras que $\models$ se refiere a las interpretaciones.

Un sistema de demostración es correcto cuando $S \vdash \varphi$ implica $S \models \varphi,$ y es completo cuando $S \models \varphi$ implica $S \vdash \varphi.$ Los sistemas de demostración habituales para la lógica proposicional tienen ambas propiedades. La clausura deductiva de $S$ es el conjunto de sus consecuencias lógicas:

$$
\mathrm{Cn}(S) := \{\ \varphi \mid S \models \varphi \ \}
$$

En un sistema correcto y completo, $\mathrm{Cn}(S)$ es también el conjunto de fórmulas derivables de $S.$ Es infinito para todo $S,$ pues contiene todas las tautologías del lenguaje.

El modus ponens permite obtener $q$ a partir de $p$ y $p \rightarrow q$:

$$
\frac{p \qquad p \rightarrow q}{q}
$$

El modus tollens permite obtener $\neg p$ a partir de $\neg q$ y $p \rightarrow q$:

$$
\frac{\neg q \qquad p \rightarrow q}{\neg p}
$$

El silogismo hipotético permite obtener $p \rightarrow r$ a partir de $p \rightarrow q$ y $q \rightarrow r$:

$$
\frac{p \rightarrow q \qquad q \rightarrow r}{p \rightarrow r}
$$

En cada esquema, las fórmulas situadas sobre la línea son las premisas y la fórmula situada bajo la línea es la conclusión.

Por ejemplo, sea $p$ la afirmación de que llueve, sea $q$ la afirmación de que el suelo está mojado y sea $r$ la afirmación de que el partido se ha cancelado. A partir de $p \rightarrow q$ y $q \rightarrow r,$ el silogismo hipotético da $p \rightarrow r.$ Si $p$ es también una premisa, el modus ponens da $r.$

Otras reglas rigen las conectivas restantes. La eliminación y la introducción de la conjunción relacionan una conjunción con sus miembros, la introducción de la disyunción debilita una fórmula convirtiéndola en una disyunción y el silogismo disyuntivo elimina un disyunto:

$$
\frac{\varphi \wedge \psi}{\varphi} \qquad \frac{\varphi \qquad \psi}{\varphi \wedge \psi} \qquad \frac{\varphi}{\varphi \lor \psi} \qquad \frac{\varphi \lor \psi \qquad \neg\varphi}{\psi}
$$

Una sola regla, la [resolución](../automated-deduction-in-propositional-logic/), engloba a la vez el modus ponens, el modus tollens y el silogismo disyuntivo, y es la regla sobre la que se construye la búsqueda mecánica de demostraciones.

## Formas normales

Un literal es una proposición atómica o la negación de una proposición atómica. Una cláusula es una disyunción de literales y un término es una conjunción de literales.

Una fórmula está en forma normal conjuntiva (FNC) si es una conjunción de cláusulas:

$$
(l_{1,1} \lor \cdots \lor l_{1,k}) \wedge (l_{2,1} \lor \cdots \lor l_{2,m}) \wedge \cdots
$$

Una fórmula está en forma normal disyuntiva (FND) si es una disyunción de términos:

$$
(l_{1,1} \wedge \cdots \wedge l_{1,k}) \lor (l_{2,1} \wedge \cdots \wedge l_{2,m}) \lor \cdots
$$

En cualquiera de las dos formas normales solo aparecen las conectivas $\neg,$ $\wedge,$ así como $\lor$ y toda negación tiene como alcance una proposición atómica. Un solo literal es a la vez una cláusula y un término, por lo que es tanto una fórmula en FNC como una fórmula en FND.

Toda fórmula proposicional es lógicamente equivalente a una fórmula en FNC y a una fórmula en FND. Un método de conversión elimina primero $\rightarrow,$ $\leftrightarrow,$ así como $\oplus,$ desplaza después cada negación hacia el interior mediante la doble negación y las leyes de De Morgan y, por último, aplica las leyes distributivas.

Por ejemplo, consideremos $\neg(p \lor q) \rightarrow r.$ La equivalencia $\varphi \rightarrow \psi \equiv \neg\varphi \lor \psi$ proporciona el cálculo siguiente:

$$
\neg(p \lor q) \rightarrow r \equiv \neg\neg(p \lor q) \lor r \equiv (p \lor q) \lor r
$$

La fórmula resultante es equivalente a $p \lor q \lor r.$ Es una única cláusula y, por tanto, está en FNC. Como cada disyunto es también un término de un solo literal, la misma fórmula está en FND.

Una tabla de verdad completa ofrece otra demostración de los teoremas sobre las formas normales. Para la FND, se toma cada fila en la que la fórmula original es verdadera, se forma un término que solo es verdadero en esa fila y se establece la disyunción de esos términos. Para la FNC, se toma cada fila en la que la fórmula es falsa, se forma una cláusula que solo es falsa en esa fila y se establece la conjunción de esas cláusulas. Cuando la fórmula es una contradicción, $p \wedge \neg p$ es una forma normal equivalente. Cuando es una tautología, $p \lor \neg p$ es una forma normal equivalente.

El procedimiento DPLL y varios métodos relacionados de satisfacibilidad toman como entrada fórmulas en FNC, al igual que el [procedimiento de resolución](../automated-deduction-in-propositional-logic/).
