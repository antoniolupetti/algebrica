---
title: Conjuntos
source: https://algebrica.org/sets/
license: CC BY-NC 4.0
tags:
  - bijection
  - cardinality
  - cartesian-product
  - de-morgan-laws
  - disjoint-union
  - inclusion-exclusion
  - indexed-family
  - indexed-product
  - ordered-pair
  - partition
  - power-set
  - set
  - set-operations
  - subset
  - universal-set
---

## Introducción

Un conjunto es una colección de objetos llamados elementos y queda determinado por completo por los objetos que pertenecen a él. Dos conjuntos son iguales precisamente cuando tienen los mismos elementos. Ni el orden en que se enumeran los elementos ni las repeticiones en la lista modifican el conjunto. Por ejemplo, las tres descripciones siguientes definen el mismo conjunto:

$$
\{1,2,3\}=\{3,1,2\}=\{1,1,2,3,3\}
$$

Un conjunto con exactamente un elemento es un conjunto unitario. Por tanto, $\{a\}$ es un conjunto unitario, mientras que $\{a,b\}$ tiene dos elementos cuando $a\neq b.$ Los conjuntos suelen representarse mediante letras mayúsculas $A,$ $B,$ $C,$ y sus elementos, mediante letras minúsculas. La notación $x\in A$ indica que $x$ pertenece a $A,$ mientras que $x\notin A$ indica que $x$ no pertenece a $A.$ La pertenencia debe tener un valor de verdad inequívoco para cada objeto considerado.

Un conjunto puede describirse por enumeración o mediante notación por comprensión. La enumeración consiste en indicar explícitamente cada elemento del conjunto y resulta práctica cuando la cardinalidad del conjunto es finita y pequeña:

$$
A = \{a_1, a_2, a_3, a_4\}
$$

Cuando los elementos son numerosos o infinitos, la notación por comprensión suele ser más breve. Esta selecciona, dentro de un conjunto especificado previamente, los elementos que satisfacen una condición dada. Por ejemplo, definimos un subconjunto de los [números enteros](../integers/) escribiendo:

$$
A = \{\ x \in \mathbb{Z} \mid x > 4, \ x \leq 8 \ \}
$$

El conjunto ambiente $\mathbb{Z}$ limita los candidatos a pertenecer al conjunto. A continuación, las dos inecuaciones seleccionan los cuatro enteros siguientes:

$$
A = \{5, 6, 7, 8\}
$$

> En la teoría ingenua de conjuntos, una condición arbitraria no define necesariamente un conjunto. Una expresión de la forma $\{\ x\in S\mid P(x)\ \}$ extrae elementos de un conjunto $S$ ya disponible. Sin un conjunto ambiente de este tipo, una condición puede describir una colección que no puede ser un conjunto. La paradoja de Russell surge de una definición no restringida de esta clase.

El conjunto vacío no contiene elementos, se denota por $\emptyset$ o $\{\ \},$ y desempeña en la teoría de conjuntos un papel análogo al del cero en la aritmética.

## El conjunto universal

Se denomina conjunto universal a una colección que contiene todos los objetos considerados, y se representa por $U.$ Todos los conjuntos de un contexto dado son subconjuntos de $U.$ La elección de $U$ depende de la situación. En teoría elemental de números se suele trabajar con $U = \mathbb{Z},$ mientras que en análisis real la elección habitual es $U = \mathbb{R}.$

> El conjunto universal es la herramienta que permite definir sin ambigüedad la noción de complementario de un conjunto, como se explica en la sección sobre operaciones con conjuntos.

## Cardinalidad de los conjuntos finitos

La cardinalidad de un conjunto finito $A,$ denotada por $|A|,$ es el número de elementos de $A.$ Las cardinalidades también pueden compararse mediante [funciones](../functions/). Dos conjuntos $A$ y $B$ tienen la misma cardinalidad cuando existe una [biyección](../injective-surjective-and-bijective-functions/) de $A$ en $B$. Esta condición se escribe del modo siguiente:

$$
|A|=|B| \iff \text{existe una biyección } f\colon A\to B
$$

Para conjuntos finitos, esta condición equivale a la igualdad entre sus números de elementos. El conjunto vacío tiene cardinalidad $|\emptyset|=0.$

Para conjuntos infinitos, las biyecciones definen la igualdad de cardinalidades incluso cuando ninguno de los conjuntos tiene un número finito de elementos. [Cardinalidad y conjuntos numerables](../cardinality-and-countable-sets/) amplía esta definición a los conjuntos infinitos e incluye la comparación con los conjuntos potencia.

La cardinalidad del producto cartesiano de dos conjuntos finitos $A$ y $B$ viene dada por:

$$
|A \times B| = |A| \cdot |B|
$$

En este caso, cada elemento de $A$ puede emparejarse con todos los elementos de $B,$ lo que produce $|A| \cdot |B|$ pares ordenados.

La cardinalidad de la unión de dos conjuntos $A$ y $B$ viene dada por:

$$
|A \cup B| = |A| + |B| - |A \cap B|
$$

La expresión anterior es el principio de inclusión-exclusión, que garantiza que los elementos comunes a ambos conjuntos se cuenten una sola vez. Cada elemento de $A \cup B$ aparece en la suma $|A| + |B|.$ Los elementos de $A \cap B$ se cuentan dos veces, por lo que se resta ese término para obtener el recuento correcto.

El principio se extiende a tres conjuntos, como expresa la fórmula:

$$
|A \cup B \cup C| = |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C|
$$

La estructura de la fórmula puede interpretarse del modo siguiente:

+ Los elementos que pertenecen a un solo conjunto se cuentan una única vez.
+ Los elementos compartidos por dos conjuntos se cuentan dos veces y se restan una vez, lo que da una contribución neta de $1.$
+ Los elementos que pertenecen a los tres conjuntos se suman tres veces, se restan tres veces y vuelven a sumarse una vez mediante la intersección triple, con lo que se obtiene de nuevo una contribución neta de uno.

## Subconjuntos y conjuntos potencia

Las nociones de subconjunto y conjunto potencia se introducen conjuntamente. Los subconjuntos son conjuntos cuyos elementos pertenecen todos a otro conjunto, mientras que los conjuntos potencia son conjuntos cuyos elementos son a su vez subconjuntos de un conjunto dado. Un conjunto $A$ es un subconjunto de $B$ si todo elemento de $A$ es también un elemento de $B$:

$$
A \subseteq B \iff \forall \ x, \ x \in A \rightarrow x \in B
$$

Dos conjuntos son iguales si y solo si cada uno está contenido en el otro, que es la forma habitual de demostrar la igualdad de conjuntos en matemáticas:

$$
A = B \iff A \subseteq B \text{ y } B \subseteq A
$$

Si $A \subseteq B$ y $A \neq B,$ entonces $A$ es un subconjunto propio de $B,$ denotado por $A \subsetneq B,$ y en este caso existe al menos un elemento de $B$ que no pertenece a $A.$ El conjunto vacío es un subconjunto de todo conjunto. La inclusión $\emptyset \subseteq A$ se cumple para cualquier conjunto $A,$ porque la implicación $x \in \emptyset \Rightarrow x \in A$ es verdadera por vacuidad.

El conjunto potencia de un conjunto $A$ es el conjunto de todos los subconjuntos de $A,$ denotado por $\mathcal{P}(A).$ Incluye el conjunto vacío $\emptyset$ y el propio conjunto $A$. Si $A$ tiene $n$ elementos, entonces $\mathcal{P}(A)$ tiene $2^n$ elementos. Por ejemplo, si $A=\{a,b,c\},$ el conjunto potencia contiene $2^3=8$ elementos:

$$
\mathcal{P}(A) = \{\emptyset, \ \{a\}, \ \{b\}, \ \{c\}, \ \{a,b\}, \ \{a,c\}, \ \{b,c\}, \ \{a,b,c\}\}
$$

El exponente $2^n$ procede de una correspondencia con funciones. Todo subconjunto $E\subseteq A$ tiene una función característica $\chi_E\colon A\to\{0,1\}$ definida por:

$$
\chi_E(a)=
\begin{cases}
1 & \text{si } a\in E \\[6pt]
0 & \text{si } a\notin E
\end{cases}
$$

Recíprocamente, una función $\chi\colon A\to\{0,1\}$ determina el subconjunto $\{\ a\in A\mid \chi(a)=1\ \}.$ Estas dos construcciones son inversas entre sí. Cuando $A$ tiene $n$ elementos, el valor de $\chi$ admite dos posibilidades independientes en cada elemento de $A,$ por lo que existen $2^n$ funciones características y, por tanto, $2^n$ subconjuntos.


## Familias indexadas de conjuntos

Cuando se consideran varios conjuntos a la vez, asignarles un índice permite mantener compacta la notación. Una familia de conjuntos indexada por un conjunto $I$ asigna un conjunto $A_i$ a cada índice $i\in I$ y se escribe $(A_i)_{i\in I}.$ Formalmente, la familia es una función cuyo dominio es $I$ y cuyo valor en $i$ es $A_i.$ Los índices siguen siendo distintos aunque coincidan dos valores, de modo que $A_i=A_j$ no implica $i=j.$ El conjunto de índices puede ser finito, numerable o no numerable.

La unión de la familia es el conjunto de los elementos que pertenecen al menos a uno de sus miembros, y la intersección es el conjunto de los elementos que pertenecen a todos ellos:

$$
\bigcup_{i\in I} A_i = \{\ x \mid x\in A_i \text{ para algún } i\in I \ \}
$$

$$
\bigcap_{i\in I} A_i = \{\ x \mid x\in A_i \text{ para todo } i\in I \ \}
$$

Un elemento pertenece a la unión en cuanto lo contiene un miembro de la familia, y pertenece a la intersección solo cuando lo contienen todos los miembros.

Una familia $(A_i)_{i\in I}$ es disjunta dos a dos cuando cualesquiera dos miembros con índices distintos no comparten ningún elemento:

$$
A_i \cap A_j = \emptyset \quad \forall \ i \neq j
$$

Para cada $n\in\mathbb{N}$, los conjuntos unitarios $\{n\}$ forman una familia disjunta dos a dos, y su unión es el conjunto $\mathbb{N}.$


## Particiones

Una partición de un conjunto $A$ es una familia de subconjuntos no vacíos $(A_i)_{i\in I}$ que son disjuntos dos a dos y cubren todo $A.$ Deben cumplirse las condiciones siguientes:

$$
\begin{align}
&A_i \neq \emptyset \quad \forall \ i \in I \\[6pt]
&A_i \cap A_j = \emptyset \quad \forall \ i \neq j \\[6pt]
& \bigcup_{i \in I} A_i = A
\end{align}
$$

Los subconjuntos $A_i$ se denominan bloques de la partición, y cada elemento de $A$ pertenece exactamente a uno de ellos. Un ejemplo sencillo es el conjunto de los [números enteros](../integers/) $\mathbb{Z},$ que puede dividirse en el conjunto de los enteros pares y el de los enteros impares, pues estos dos bloques son no vacíos, disjuntos y juntos cubren todo $\mathbb{Z}.$

Las particiones están relacionadas con las relaciones de equivalencia. Dada una relación de equivalencia sobre $A$:

+ Las clases de equivalencia que induce forman una partición de $A.$
+ Toda partición de $A$ define una relación de equivalencia al declarar equivalentes dos elementos cuando pertenecen al mismo bloque.


## Operaciones con conjuntos

Las operaciones con conjuntos generan nuevos conjuntos combinando los elementos de conjuntos distintos. Las operaciones principales son la unión, la intersección, el complementario y la diferencia.

La unión de $A$ y $B$ es el conjunto de todos los elementos que pertenecen al menos a uno de los dos conjuntos. Los elementos comunes a $A$ y $B$ se enumeran una sola vez, puesto que los conjuntos no admiten repeticiones.

![IMG. 1](svg/sets-1.svg)

$$
A \cup B = \\{x \mid x \in A \text{ o } x \in B\\}
$$
- - -

La intersección de $A$ y $B$ es el conjunto de los elementos que pertenecen a ambos conjuntos:

![IMG. 2](svg/sets-2.svg)

$$
A \cap B = \\{x \mid x \in A \text{ y } x \in B\\}
$$

Si $A \cap B = \emptyset,$ los dos conjuntos son disjuntos y no comparten elementos.

- - -

El complementario de $A$ respecto de un conjunto universal $U$ es el conjunto de todos los elementos de $U$ que no pertenecen a $A.$ Se escribe:

$$
A^c = \\{x \in U \mid x \notin A\\}
$$

![IMG. 3](svg/sets-3.svg)

Otra forma de representar el complementario de $A$ es $\overline{A}$ o $U \setminus A.$ Un mismo conjunto puede tener complementarios distintos al cambiar $U$, pues los elementos del complementario varían con el conjunto universal que se elija.

- - -

La diferencia de $A$ y $B,$ escrita $A \setminus B,$ es el conjunto de los elementos que pertenecen a $A$ pero no a $B$:

![IMG. 4](svg/sets-4.svg)

$$
A \setminus B = \\{x \mid x \in A \text{ y } x \notin B\\}
$$

En general se cumple la relación $A \setminus B \neq B \setminus A$, ya que la diferencia de dos conjuntos no es una operación conmutativa. Para todo conjunto universal que contenga tanto $A$ como $B$ se cumple la identidad $A \setminus B = A \cap B^c$, que expresa la diferencia mediante el complementario.

La diferencia simétrica de $A$ y $B,$ escrita $A \triangle B,$ es el conjunto de los elementos que pertenecen a uno de los dos conjuntos, pero no a ambos:

![IMG. 5](svg/sets-5.svg)

$$
A \triangle B = (A \setminus B) \cup (B \setminus A)
$$

La expresión siguiente proporciona una representación equivalente:

$$
A \triangle B = (A \cup B) \setminus (A \cap B)
$$

La diferencia simétrica es conmutativa y asociativa, y satisface $A \triangle A = \emptyset$ y $A \triangle \emptyset = A.$ Junto con la intersección, dota de estructura de [anillo](../rings/) booleano a la colección de todos los subconjuntos de un conjunto dado.

## Propiedades de las operaciones con conjuntos

Las operaciones con conjuntos satisfacen una serie de identidades que constituyen la base del álgebra de Boole y se cumplen para cualesquiera conjuntos $A,$ $B,$ y $C$ contenidos en un conjunto universal $U.$ La unión y la intersección son operaciones conmutativas. El orden en que se combinan dos conjuntos no afecta al resultado.

$$
\begin{align}
A \cup B &= B \cup A \\[6pt]
A \cap B &= B \cap A
\end{align}
$$

Ambas operaciones son también asociativas, lo que significa que, al combinar tres conjuntos, la agrupación de los operandos es irrelevante.

$$
\begin{align}
(A \cup B) \cup C &= A \cup (B \cup C) \\[6pt]
(A \cap B) \cap C &= A \cap (B \cap C)
\end{align}
$$

La unión y la intersección son distributivas entre sí, de manera análoga a la propiedad distributiva de la aritmética.

$$
\begin{align}
A \cap (B \cup C) &= (A \cap B) \cup (A \cap C) \\[6pt]
A \cup (B \cap C) &= (A \cup B) \cap (A \cup C)
\end{align}
$$

El conjunto vacío y el conjunto universal actúan como elementos neutros de la unión y la intersección, respectivamente. Al combinar cualquier conjunto con el elemento correspondiente se obtiene el conjunto original.

$$
\begin{align}
A \cup \emptyset &= A \\[6pt]
A \cap U &= A
\end{align}
$$

El conjunto vacío es absorbente para la intersección y el conjunto universal lo es para la unión. Al combinar cualquier conjunto con estos elementos se obtiene el elemento absorbente en lugar del conjunto original:

$$
\begin{align}
A \cap \emptyset &= \emptyset \\[6pt]
A \cup U &= U
\end{align}
$$

Cada elemento de $U$ pertenece a $A$ o a su complementario, pero nunca a ambos. Al aplicar dos veces seguidas la operación de complementación se recupera el conjunto original:

$$
\begin{align}
A \cup A^c &= U \\[6pt]
A \cap A^c &= \emptyset \\[6pt]
(A^c)^c &= A
\end{align}
$$

## Leyes de De Morgan

Las leyes de De Morgan son identidades algebraicas que describen cómo se comportan la unión y la intersección bajo la operación de complementación. Estas identidades permiten reescribir expresiones de conjuntos en formas equivalentes y ayudan a simplificar las operaciones.

$$
\begin{align}
(A \cup B)^c &= A^c \cap B^c \\[6pt]
(A \cap B)^c &= A^c \cup B^c
\end{align}
$$

La primera ley afirma que el complementario de una unión es igual a la intersección de los complementarios. Un elemento no pertenece a $A \cup B$ solo cuando no pertenece ni a $A$ ni a $B,$ lo que equivale a pertenecer tanto a $A^c$ como a $B^c.$

![IMG. 6](svg/sets-6.svg)

La segunda ley afirma que un elemento no pertenece a la intersección $A \cap B$ cuando falta en al menos uno de los dos conjuntos, por lo que pertenece a $A^c \cup B^c.$

Estas leyes se extienden a una familia arbitraria de conjuntos $(A_i)_{i\in I},$ sin restricciones sobre el tamaño del conjunto de índices $I$:

$$
\begin{align}
\left(\bigcup_{i \in I} A_i\right)^c &= \bigcap_{i \in I} A_i^c \\[6pt]
\left(\bigcap_{i \in I} A_i\right)^c &= \bigcup_{i \in I} A_i^c
\end{align}
$$

Existe una correspondencia entre la estructura algebraica de los conjuntos y la de las conectivas lógicas. Las leyes de De Morgan se traducen en las equivalencias siguientes para las conectivas $\land$ y $\lor$:

$$
\neg(P \lor Q) \equiv \neg P \land \neg Q
$$

$$
\neg(P \land Q) \equiv \neg P \lor \neg Q
$$

La interpretación mediante tablas de verdad de estas equivalencias se desarrolla en [lógica proposicional](../propositional-logic/).

## Ejemplo

Sea $U = \\{1, 2, 3, 4, 5, 6, 7, 8, 9, 10\\}$ el conjunto universal, y definamos los dos subconjuntos siguientes:

$$
\begin{align}
A &= \{1, 2, 3, 4, 6\} \\[6pt]
B &= \{2, 4, 6, 8, 10\}
\end{align}
$$

La unión y la intersección de los dos conjuntos se calculan directamente a partir de las definiciones:

$$
\begin{align}
A \cup B &= \{1, 2, 3, 4, 6, 8, 10\} \\[6pt]
A \cap B &= \{2, 4, 6\}
\end{align}
$$

Los complementarios respecto de $U$ reúnen los elementos excluidos de cada conjunto:

$$
\begin{align}
A^c &= \{5, 7, 8, 9, 10\} \\[6pt]
B^c &= \{1, 3, 5, 7, 9\}
\end{align}
$$

Comprobemos ahora la primera ley de De Morgan. El complementario de la unión es:

$$
(A \cup B)^c = U \setminus (A \cup B) = \\{5, 7, 9\\}
$$

La intersección de los complementarios da:

$$
\begin{align}
A^c \cap B^c &= \{5, 7, 8, 9, 10\} \cap \{1, 3, 5, 7, 9\} \\[6pt]
&= \{5, 7, 9\}
\end{align}
$$

Los dos conjuntos coinciden, lo que confirma la primera ley de De Morgan. Comprobemos ahora el principio de inclusión-exclusión mediante cardinalidades:

$$
|A| = 5 \quad |B| = 5 \quad |A \cap B| = 3
$$

$$
|A \cup B| = 5 + 5 - 3 = 7
$$

Un recuento directo de los elementos de $A \cup B = \\{1, 2, 3, 4, 6, 8, 10\\}$ confirma que $|A \cup B| = 7.$

Calculamos la diferencia simétrica y comprobamos su relación con las demás operaciones:

$$
A \triangle B = (A \setminus B) \cup (B \setminus A)
$$

Las dos diferencias son $A \setminus B = \\{1, 3\\}$ y $B \setminus A = \\{8, 10\\},$ de donde se obtiene:

$$
A \triangle B = \\{1, 3, 8, 10\\}
$$

El mismo resultado se obtiene mediante la caracterización equivalente que utiliza la unión y la intersección:

$$
\begin{align}
(A \cup B) \setminus (A \cap B) &= \{1, 2, 3, 4, 6, 8, 10\} \setminus \{2, 4, 6\} \\[6pt]
&= \{1, 3, 8, 10\}
\end{align}
$$


## Producto cartesiano

Dados dos conjuntos $A$ y $B,$ el producto cartesiano $A \times B$ es el conjunto de todos los pares ordenados $(a, b)$ tales que $a$ pertenece a $A$ y $b$ pertenece a $B$:

$$
A \times B = \\{(a, b) \mid a \in A, \ b \in B\\}
$$

Un par ordenado es asimétrico: $(a, b)$ es distinto de $(b, a)$ si $a$ y $b$ no son iguales. Dos pares ordenados son iguales si y solo si sus componentes correspondientes son iguales, como expresa la condición siguiente:

$$
(a, b) = (a', b') \iff a = a' \text{ y } b = b'
$$

En general, $A \times B$ y $B \times A$ no son el mismo conjunto. Si $A$ contiene $m$ elementos y $B$ contiene $n$ elementos, entonces $A \times B$ contiene $mn$ elementos. Por ejemplo, $\mathbb{R} \times \mathbb{R},$ que es el conjunto de todos los pares de [números reales](../real-numbers/), es el plano cartesiano $\mathbb{R}^2.$

Dados los conjuntos $A_1, A_2, \ldots, A_n,$ su producto cartesiano es el conjunto de todas las $n$-tuplas ordenadas:

$$
A_1 \times A_2 \times \cdots \times A_n = \\{(a_1, a_2, \ldots, a_n) \mid a_i \in A_i \text{ para todo } i = 1, \ldots, n\\}
$$

Una $n$-tupla $(a_1, \ldots, a_n)$ es una lista ordenada de $n$ elementos, y dos $n$-tuplas son iguales si y solo si todos sus componentes correspondientes son iguales. Si todos los conjuntos son idénticos, es decir, $A_i = A$ para todo $i,$ el producto es $A^n.$ El espacio $\mathbb{R}^n$ es el producto cartesiano de $n$ copias de $\mathbb{R}$, y sus elementos son $n$-tuplas de números reales.

El producto cartesiano se extiende a una familia indexada $(A_i)_{i\in I}.$ Un elemento del producto indexado tiene un componente $a_i\in A_i$ por cada índice $i.$ El producto se define por:

$$
\prod_{i\in I}A_i=\{\ (a_i)_{i\in I}\mid a_i\in A_i \text{ para todo } i\in I \ \}
$$

De forma equivalente, un elemento de $\prod_{i\in I}A_i$ es una función $a\colon I\to\bigcup_{i\in I}A_i$ tal que $a(i)\in A_i$ para todo $i\in I.$ Cuando $I=\{1,\ldots,n\},$ esta definición proporciona el producto cartesiano finito anterior. Si uno de los factores es vacío, todo el producto es vacío porque ninguna familia puede elegir un elemento de ese factor.

> Para una familia indexada arbitraria de conjuntos no vacíos, la afirmación de que el producto cartesiano no es vacío equivale al axioma de elección. Las familias finitas no necesitan este axioma.

## Unión disjunta

La unión ordinaria contiene una sola aparición de un elemento que pertenece tanto a $A$ como a $B.$ La unión disjunta contiene dos versiones etiquetadas de dicho elemento, una por cada conjunto de origen. Una construcción viene dada por:

$$
A\sqcup B=(\{0\}\times A)\cup(\{1\}\times B)
$$

Los conjuntos $\{0\}\times A$ y $\{1\}\times B$ son disjuntos porque sus pares ordenados tienen primeros componentes distintos. Las funciones $i_A\colon A\to A\sqcup B$ e $i_B\colon B\to A\sqcup B$ definidas por $i_A(a)=(0,a)$ e $i_B(b)=(1,b)$ son inyectivas. Sus imágenes son disjuntas y su unión es $A\sqcup B.$ Por tanto, cada elemento de la unión disjunta procede exactamente de uno de los dos conjuntos de origen.

Si $A$ y $B$ son finitos, las dos copias etiquetadas tienen $|A|$ y $|B|$ elementos, respectivamente. El hecho de que sean disjuntas da la fórmula:

$$
|A\sqcup B|=|A|+|B|
$$

Cuando $A\cap B=\emptyset,$ eliminar las etiquetas define una biyección de $A\sqcup B$ en $A\cup B.$ Si $A\cap B\neq\emptyset,$ la misma regla no es inyectiva. Para un elemento $x\in A\cap B,$ los elementos distintos $(0,x)$ y $(1,x)$ de $A\sqcup B$ tendrían ambos como imagen $x.$

## El par ordenado

Hasta aquí se ha tratado el par ordenado $(a, b)$ como una noción intuitiva, a saber, un par de objetos cuyo primer componente es $a$ y cuyo segundo componente es $b.$ En términos formales, el par ordenado puede definirse en teoría de conjuntos como un conjunto que contiene dos elementos:

$$
(a, b) = \\{\\{a\\}, \ \\{a, b\\}\\}
$$

El término $\\{a\\}$ es el conjunto unitario, y $\\{a, b\\}$ es el par no ordenado. El elemento $a$ aparece en ambos, mientras que $b$ aparece solo en uno. Esta definición queda justificada por el resultado siguiente:

$$
(a, b) = (c, d) \implies a = c \text{ y } b = d
$$

Para comprobar esta propiedad, supongamos que $\\{\\{a\\}, \\{a, b\\}\\} = \\{\\{c\\}, \\{c, d\\}\\}.$ Hay dos casos, según se cumpla $a = b$ o $a \neq b.$

En el primer caso, cuando $a = b,$ se tiene $\\{a, b\\} = \\{a\\},$ por lo que el miembro izquierdo se convierte en $\\{\\{a\\}\\},$ un conjunto unitario. Para que haya igualdad, el miembro derecho también debe ser un conjunto unitario, lo que exige que $\\{c\\} = \\{c, d\\}$ y, por tanto, que $c = d.$ El único elemento de cada miembro debe coincidir, de modo que $\\{a\\} = \\{c\\},$ y por consiguiente $a = c.$ Puesto que $b = a = c = d,$ se deduce que $a = c$ y $b = d.$

Si $a \neq b,$ el miembro izquierdo contiene dos elementos distintos: $\\{a\\}$ y $\\{a, b\\}.$ El conjunto unitario $\\{a\\}$ debe corresponderse con $\\{c\\}$ o con $\\{c, d\\}$ en el miembro derecho. Si $\\{a\\} = \\{c, d\\},$ entonces $c = d = a,$ lo que haría que $\\{c\\} = \\{c, d\\},$ dando como resultado un conjunto unitario en el miembro derecho, en contradicción con la presencia de dos elementos distintos en el izquierdo. Por tanto, $\\{a\\} = \\{c\\},$ de modo que $a = c.$ Se sigue que $\\{a, b\\} = \\{c, d\\} = \\{a, d\\},$ y, dado que $a \neq b,$ necesariamente $b = d.$

En ambos casos, $a = c$ y $b = d,$ como se quería demostrar. El recíproco es inmediato, pues si $a = c$ y $b = d$, los dos conjuntos son idénticos por sustitución.
