# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Álgebra y geometría analítica:: Unidad 1
# Archivos
![[ÁLGEBRA DE PROPOSICIONES 2016.pdf]]
# Notas
## Lógica #flashcard 
La lógica es el estudio del razonamiento; Se refiere específicamente a si el razonamiento es correcto. La lógica se centra en la relación entre declaraciones y no en el contenido de una declaración en particular. Los métodos lógicos se utilizan en matemáticas para demostrar teoremas y, en informática, para demostrar que los programas hacen lo que se supone que deben hacer.
## ¿Cómo llamamos proposición? #flashcard 
Una oración que es verdadera o falsa, pero no ambas, se llama proposición. Ejemplos de oraciones que son proposiciones:
Teoría de Sistemas es una asignatura de la Licenciatura en Sistemas de la FCAD
15 es múltiplo de 3
Ejemplos de oraciones que no son proposiciones:
Compra un pendrive y una resma de papel.
¡Qué día tan espectacular!
5 – x = 6
Es común que una proposición se exprese como una oración declarativa (y no como una pregunta, orden, exclamación, etc.)
Se utilizarán variables, como p, q y r, para representar las proposiciones.
<!--ID: 1700071629220-->




## Proposiciones simples y proposiciones compuestas #flashcard
- Las proposiciones simples (o atómicas) son aquellas que no contienen otras.
- Proposiciones compuestas (o moleculares): aquellas que no son simples.
<!--ID: 1700071629245-->




## Operaciones y conectivos lógicos #flashcard
![[Operaciones y conectivos lógicos.png]]
<!--ID: 1700071629266-->




## Tablas de verdad #flashcard
- Los valores de verdad de las proposiciones compuestas se describen mediante tablas de verdad.
- Cada proposición simple puede ser Verdadera o Falsa.
- El número de filas de la tabla de verdad de una proposición compuesta viene dado por 2^n, donde n es el número de proposiciones simples que la componen.
<!--ID: 1700071629272-->




### Conjunción (Tabla de verdad y explicación) #flashcard
![[Conjunción.png]]
<!--ID: 1700071629278-->





### Disyunción exclusiva (Tabla de verdad y explicación) #flashcard
![[Disyunción exclusiva.png]]
<!--ID: 1700071629282-->




### Disyunción inclusiva (Tabla de verdad y explicación) #flashcard
![[Disyunción inclusiva.png]]
<!--ID: 1700071629286-->




### Negación (Tabla de verdad y explicación) #flashcard
![[Negación.png]]
<!--ID: 1700071629290-->




### Proposición bicondicional (Tabla de verdad y explicación) #flashcard
![[Proposición bicondicional.png]]
<!--ID: 1700071629294-->




### Proposición condicional (Tabla de verdad y explicación) #flashcard
![[Proposición condicional (Implicación).png]]
<!--ID: 1700071629298-->




## Tautología #flashcard
Una proposición compuesta se llama tautología si es verdadera para alguno de los valores de verdad de las proposiciones que la componen.
<!--ID: 1700071629302-->




## Contingencia #flashcard
Una proposición compuesta se llama contingencia si su valor de verdad depende de los valores de verdad de las proposiciones que la componen.
<!--ID: 1700071629307-->




## Contradicción #flashcard
Una proposición compuesta se llama contradicción si es falsa para alguno de los valores de verdad de las proposiciones que la componen.
<!--ID: 1700071629311-->




## Equivalencias lógicas #flashcard
- Dos proposiciones compuestas son equivalentes si presentan la misma tabla de verdad.
- Dos proposiciones compuestas son equivalentes si y sólo si el operador bicondicional entre ellas es una tautología.
<!--ID: 1700071629315-->




## Propiedades del álgebra de proposiciones #flashcard
- Idempotencia
- Conmutativo
- asociativo
- Absorción
- Distributivo
- Negación
- Elemento neutro
- Elemento absorbente
- Involución
- Leyes de De Morgan
<!--ID: 1700071629319-->




### Idempotencia #flashcard
- Disyunción. p o p **equivalente a** p
- Conjunción. p y p **equivalente a** p
<!--ID: 1700071629323-->




### Conmutativa #flashcard
- Disyunción. p o q **equivalente a** q o p
- Conjunción. p y q **equivalente a** q y p
<!--ID: 1700071629328-->




### Asociativa #flashcard
- Disyunción. (p o q) o r **equivalente a** p o (q o r)
- Conjunción. (p y q) y r **equivalente a** p y (q y r)
<!--ID: 1700071629331-->




### Absorción #flashcard 
- Disyunción. p o (p y q) **equivalente a** p
- Conjunción. p y (p o q) **equivalente a** p
<!--ID: 1700071629335-->




### Distributiva #flashcard
- Disyunción. p o (q y r) **equivalente a** (p o q) y (p o r)
- Conjunción. p y (q o r) **equivalente a** (p y q) o (p y r)
<!--ID: 1700071629339-->




### Negación #flashcard
- Disyunción. p o -p **equivalente a** T
- Conjunción. p y -p **equivalente a** C
<!--ID: 1700071629343-->




### Elemento neutro #flashcard
- Disyunción. p o C **equivalente a** p
- Conjunción. p y T **equivalente a** p
<!--ID: 1700071629352-->




### Elemento absorbente #flashcard
- Disyunción. p o T **equivalente a** T
- Conjunción. p y C **equivalente a** C
<!--ID: 1700071629357-->




### Involución #flashcard
-(-p) **equivalente a** p
<!--ID: 1700071629361-->




### Leyes de De Morgan #flashcard
- Disyunción. -(p o q) **equivalente a** (-p) y (-q)
- Conjunción. -(p y q) **equivalente a** (-p) o (-q)
<!--ID: 1700071629365-->




## Circuitos lógicos gráficamente #flashcard
![[Circuitos lógicos.png]]
<!--ID: 1700071629369-->




## Circuitos lógicos, descripción #flashcard
Para encontrar el circuito lógico de cualquier proposición compuesta es necesario utilizar las propiedades y equivalencias lógicas que permitan transformarla en una proposición donde sólo intervienen disyunciones inclusivas y conjunciones entre proposiciones simples o sus negaciones.
<!--ID: 1700071629373-->




## Función proposicional #flashcard
Función proposicional en una variable x es cualquier oración que tiene x como sujeto y se transforma en una proposición para cada especificación de x.
Una función proposicional P, por sí sola, no es ni falsa ni verdadera. Sin embargo, para cada x en su dominio de discurso, P(x) es una proposición y, por tanto, es verdadera o falsa.
<!--ID: 1700071629377-->




## Cuantificador universal #flashcard
Sea P una función proposicional con universo U. Se dice que el enunciado para todo x, P(x) es un enunciado universalmente cuantificado. Simbólicamente:
![[Cuantificador universal.png]]
El símbolo ∀ se llama cuantificador universal. la afirmacion
∀x : P(x) es verdadero si P(x) es verdadero para todo x en U.
La afirmación ∀x: P(x) es falsa si P(x) es falsa para al menos una x en U.
<!--ID: 1700071629382-->




## Cuantificador existencial #flashcard
Sea P una función proposicional con dominio del discurso (universo) U. Se dice que el enunciado x existe tal que P(x) es un enunciado existencialmente cuantificado. El símbolo ∃ significa "existe". Simbólicamente:
![[Cuantificador existencial.png]]
El símbolo ∃ se llama cuantificador existencial.
La afirmación ∃x / P(x) es verdadera si P(x) es verdadera para al menos una x en U.
La afirmación ∃x / P(x) es falsa si P(x) es falsa para todo x en U.
<!--ID: 1700071629387-->




## Negación de cuantificadores #flashcard
![[Negación de funciones proposicionales cuantificadas.png]]
<!--ID: 1700071629390-->




## Relaciones lógicas #flashcard
1. Implicación formal: es esa implicación la que es una tautología. No puede suceder que si el antecedente es verdadero, el consecuente sea falso.
2. Doble implicación formal o equivalencia lógica: es esa doble implicación la que es una tautología (p implica formalmente q, y q implica formalmente p).
<!--ID: 1700071629394-->




## Condiciones necesarias y suficientes #flashcard
- Si P(x) implica formalmente Q(x), diremos que P(x) es una condición **suficiente** para Q(x), Q(x) si P(x); Q(x), es una condición **necesaria** para P(x), P(x) solo si Q(x).
- Si entre P(x) y Q(x) existe una doble implicación formal, diremos que P(x) es condición necesaria y suficiente para Q(x), P(x) si y sólo si Q(x) ).
- Ejemplo donde P(x) es una condición necesaria para Q(x), pero P(x) no es una condición suficiente para Q(x)
- ![[Condición necesaria y suficiente.png]]
<!--ID: 1700071629399-->




## Implicaciones asociadas #flashcard
Dada una implicación (teorema) 𝑝 ⟹ 𝑞 , que llamaremos implicación directa (teorema directo), hay tres implicaciones asociadas con ella. A saber:
1. Implicación directa (teorema directo) 𝑝 ⟹ 𝑞
2. Implicación recíproca (teorema recíproco): 𝑞 ⟹ 𝑝
3. Implicación contraria (teorema contrario): −𝑝 ⟹ −𝑞
3. Implicación cotrarecíproca (teorema contrarecíproco): −𝑞 ⟹ −p
- Las implicaciones directas y contrarecíprocas (teoremas) son equivalentes.
<!--ID: 1700071629403-->




## Razonamientos lógicos #flashcard 
- Razonamiento: Es cualquier par ordenado ({pi};q) en el que {pi} es un conjunto finito de proposiciones, llamadas premisas, y q es una proposición, llamada conclusión, respecto de la cual se afirma que se deriva de las premisas.
- Razonamiento deductivo: Las premisas son evidencia de la verdad de la conclusión (si las premisas son verdaderas, la conclusión es verdadera)
- Razonamiento deductivo válido: si no es posible que las premisas sean verdaderas y la conclusión falsa.
<!--ID: 1700071629407-->




## Reglas de inferencia #flashcard
![[Reglas de inferencia.png]]
<!--ID: 1700071629411-->



## Validez del razonamiento deductivo #flashcard
1. Primera opción: Construir la tabla de verdad para la implicación entre la conjunción de las premisas y la conclusión. Si resulta una tautología, el razonamiento deductivo es válido. En general, intentaremos no utilizar este camino.
2. Segunda opción: Aplicar la definición de razonamiento deductivo válido. Es decir, realizar la verificación directa de que si las hipótesis o premisas son verdaderas, la conclusión también lo es. Hacer que la conclusión sea falsa invalida el razonamiento.
3. Tercera opción: Aplicar las reglas de inferencia
<!--ID: 1700071629415-->


