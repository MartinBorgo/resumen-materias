La sintaxis de un lenguaje de programación proporciona las reglas de sintaxis para un lenguaje de programación significa decir como se escriben los enunciados, declaraciones y otras construcciones de lenguaje, describe la serie de símbolos que constituyen programas válidos. La semántica de un lenguaje de programación es el significado que se da a las diversas construcciones sintácticas.

La sintaxis está definida por reglas:
-   Léxicas.
-   Sintácticas.

Se usa la siguiente terminología:
-   **Lenguaje**: conjuntos de cadenas de caracteres válidos pertenecientes a algún alfabeto.
-   **Sentencia**: cada una de estas cadenas.
-   **Lexemas**: unidades sintácticas de más bajo nivel. (+, *, else, begin, end, contador, suma, etc.)
-   **Token**: categoría de lexemas. (P.e. identificadores, símbolos_de_operador, etc.)

#### Criterios Generales de sintaxis
El propósito primordial de la sintaxis es proveer una notación para la comunicación entre programador y el procesador de lenguajes de programación. Sin embargo, la elección de estructuras sintácticas particulares está restringida sólo ligeramente por la necesidad de comunicar elementos particulares de información. Los detalles de sintaxis se eligen en gran medida con base en criterios secundarios, como la legibilidad, los cuales no tienen relación con el objetivo primario de comunicar información al procesador de lenguajes. Existen muchos criterios secundarios, pero se pueden clasificar en forma aproximada bajo los objetivos generales de hacer que los programas sean fáciles de leer, fáciles de escribir, fáciles de traducir y no ambiguos. Consideraremos a continuación algunas de las formas de designar estructuras sintácticas de lenguajes para satisfacer estos objetivos a menudo conflictivos.

##### **Legibilidad**
Las diferencias sintácticas deben reflejar diferencias semánticas subyacentes.

Un programa es legible si la estructura subyacente del algoritmo y los datos que el programa representa quedan de manifiesto al inspeccionar el texto del programa. Se suele  decir que un programa legible es autodocumentable, es entendible sin documentación independiente alguna (aunque este objetivo se alcanza pocas veces en la práctica). La legibilidad se mejora a través de características de lenguaje tales como formatos naturales de enunciado, enunciados estructurados, uso abundante de palabras clave y palabras pregonadas, recursos para comentarios incrustados, identificadores de longitud sin restricción, símbolos memotécnicos de operadores, formatos de campo libre y declaraciones completas de datos. La legibilidad no se puede garantizar mediante el diseño de un lenguaje, porque incluso el mejor diseño se puede entrampar por una programación deficiente. La legibilidad mejora a través de una sintaxis de programa en la cual las diferencias sintácticas reflejan diferencias sintácticas subyacentes, y las construcciones de programa que hacen cosas radicalmente distintas  se ven diferentes. En general, cuanto mayor es la variedad de construcciones sintácticas empleadas, resulta más fácil hacer que la estructura del programa refleje estructuras semánticas subyacentes distintas.

##### **Facilidad de escritura** 
Utilización de estructuras concisas y regulares.

Las características sintácticas que hace que un programa sea fácil de escribir suelen encontrarse en conflicto con las características que facilitan su lectura. El atributo de fácil escritura mejora a través del uso de estructuras sintácticas concisas y regulares, en tanto que para la legibilidad son de ayuda diversas construcciones más elocuentes. Las convenciones sintácticas implícitas que permiten  dejar sin especificar declaraciones y operaciones hacen a los programas más cortos y fáciles de escribir pero dificultan su lectura. Otras características favorecen ambos objetivos; Por ejemplo, el uso de enunciados estructurados, formatos simples de enunciados naturales, símbolos nemotécnicos de operaciones e identificadores no restringidos facilita por lo común la escritura de programas al permitir que la estructura natural de los algoritmos y datos del problema se represente directamente en el programa. 
Una sintaxis es redundante si comunica el mismo elemento de información en más de una forma. Cierta redundancia es útil en la sintaxis de lenguajes de programación porque facilita la lectura del programa y también permite revisar en busca de errores durante la traducción. La desventaja es que la redundancia hace a los programas más elocuentes y por tanto dificulta su escritura. Casi todas las reglas por omisión para el significado de construcciones de lenguaje buscan reducir la redundancia eliminando la expresión de significados que se pueden inferir del contexto. 
Por ejemplo, en vez de requerir la declaración explícita del tipo de cada variable simple, FORTRAN suministra una convención de nomenclatura que declara implícitamente que las variables cuyos nombres comienzan con una de las letras I-N son de tipo entero y todas las demás variables son de tipo real. La mera incidencia de un nuevo nombre de variable en un programa basta para “declararla”. Desafortunadamente, la conveniencia adicional queda neutralizada por un efecto negativo más serio: el compilador de FORTRAN no puede detectar un nombre de variable mal escrito.

##### **Facilidad de verificación:** 
Entender un enunciado es fácil, crear programas correctos es difícil.

Tiene relación con la legibilidad y facilidad escritura el concepto de corrección del programa o verificación del programa. Si bien entender cada enunciado de lenguaje de programación  es relativamente fácil, el proceso global de crear programas correctos es un extremo difícil. Por consiguiente, se necesitan técnicas que permitan probar que el programa es matemáticamente correcto.

##### **Facilidad de traducción:** 
Regularidad de la estructura.

Un tercer objetivo en conflicto es el de hacer que los programas sean fáciles de traducir a una forma ejecutable. Legibilidad y facilidad de escritura son criterios dirigidos a las necesidades del programador humano. La facilidad de traducción se relaciona con las necesidades del traductor que procesa el programa escrito. La clave para una traducción fácil es la regularidad de la estructura.

Por ejemplo, la sintaxis de LISP proporciona un ejemplo de una estructura de programa que no es particularmente legible ni especialmente fácil de escribir pero que resulta en extremo fácil de traducir. La estructura sintáctica completa de cualquier programa en LISP se puede describir en unas cuantas reglas sencillas a causa de la regularidad de la sintaxis. La traducción de los programas se dificulta conforme aumenta el número de construcciones sintácticas especiales. Por ejemplo, la traducción de COBOL se hace muy difícil a causa del gran número de formas de enunciados y declaraciones que se permiten, no obstante que la semántica del lenguaje no es complicada de manera expresa.

##### **Carencia de ambigüedad:** 
Idealmente un sólo significado para cada construcción sintáctica que se puede escribir.

La ambigüedad es un problema medular en todo diseño de lenguaje. Una definición de lenguaje proporciona idealmente un significado único para cada construcción sintáctica que el programador puede escribir. Una construcción ambigua permite dos o más interpretaciones distintas. El problema de ambigüedad surge por lo común no en la estructura de elementos individuales de programa, sino en la interacción entre diferentes estructuras.

Por ejemplo, tanto PASCAL como ALGOL permiten dos formas distintas de enunciado condicional:

1. 
**if** expresión booleana 
**then** enunciado 
**else** enunciado.

2.
**if** expresión booleana 
**then** enunciado.

La interpretación que se debe dar a cada forma de enunciado está claramente definida. Sin embargo, cuando las dos formas se combinan al permitir que el enunciado sea otro enunciado condicional, entonces se forma la estructura que se conoce como else ambiguo:

**if** expresión booleana 
**then if** expresión booleana 
**then** enunciado 
**else** enunciado

Esta forma de enunciado es ambigua porque no queda claro cuál de las dos secuencias de ejecución es la deseada. La ambigüedad se ha resultado cambiando la sintaxis del lenguaje para introducir un par delimitador **begin…end** requerido en torno al enunciado condicional incrustado. Así, la combinación natural pero ambigua de dos enunciados condicionales ha sido reemplazada por las dos construcciones menos naturales pero no ambiguas, de acuerdo con la interpretación deseada.

**if** expresión booleana 
**then begin if** expresión booleana 
**then** enunciado
**end**
**else** enunciado

#### **Elementos sintácticos de un lenguaje.**

##### **Identificadores (Variable):**
La sintaxis básica para identificadores, una cadena de letras y dígitos comienza con una letra, tiene amplia aceptación. Las variaciones entre lenguajes se dan principalmente en la inclusión opcional de caracteres especiales como . o -para mejorar la legibilidad y en restricciones de longitud. Las restricciones de longitud, como la antigua restricción de FORTRAN a seis caracteres, obligan al uso de identificadores con poco valor nemotécnico en muchos casos y en esta forma restringen la legibilidad del programa en forma significativa.

##### **Símbolos de operadores:**
el campo de aplicacion del lenguaje define las operaciones que seran soportadas por el lenguajes, asi como la asociacion de un simbolo a la operacion que realiza un simbolo ej el sombolo + para la operacion de suma
Casi todos los lenguajes emplean los caracteres especiales + y - para representar las dos operaciones aritméticas básicas, pero más allá de esto casi no existe uniformidad. Las operaciones primitivas se pueden representar cabalmente por caracteres especiales. Alternativamente, se pueden usar identificadores para todas las primitivas. Casi todos los lenguajes adoptan alguna combinación y utilizan caracteres especiales para ciertos operadores, identificadores para otros, y con frecuencia también algunas cadenas de caracteres que no encajan en estados dos categorías (por ejemplo, .EQ. y ** de FORTRAN, para igualdad y exponenciación, respectivamente).

###### **Palabras clave y palabras reservadas:**
Una palabra clave es un identificador que se usa como una parte fija de la sintaxis de un enunciado, por ejemplo “IF” al principio de un enunciado condicional. Una palabra clave es una palabra reservada si no se puede usar también como un identificador elegido por el programador. Casi todos los lenguajes emplean actualmente palabras reservadas, con lo cual se mejora la capacidad de detección de errores de los traductores. La mayoría de los enunciados comienzan con una palabra clave que designa el tipo de enunciado: READ, IF, WHILE, etc. El análisis sintáctico durante la traducción se facilita usando palabras reservadas. La dificultad primordial con las palabras reservadas se presenta cuando se necesita ampliar el lenguaje para incluir enunciados nuevos empleando palabras reservadas.

###### **Palabras pregonadas:**
Las palabras pregonadas son palabras opcionales que se insertan en los enunciados para mejorar la legibilidad. Ejemplo COBOL ofrece muchas opciones de este tipo, en el enunciado goto, que se escribe GO TO rótulo, se requiere la palabra clave GO, pero TO es opcional; no transmite información y solo se usa para mejorar la legibilidad.

###### **Comentarios:**
La inclusión de comentarios en un programa es una parte importante de su documentación. Un lenguaje puede permitir comentarios de varias maneras: 1. Renglones de comentarios por separado en el programa, como FORTRAN; 2. Delimitados por marcadores especiales, los /* y */ de C sin que importen los límites de renglón; o 3 comenzando en cualquier punto de un renglón pero ya concluidos al final del mismo, como el - en Ada, / en C++. La tercera alternativa incluye a la primera y también permite introducir un comentario breve después del enunciado o declaración en un renglón. La segunda alternativa tiene la desventaja de que la falta de un delimitador de conclusión en un comentario transforma los enunciados siguientes (hasta el final del siguiente comentario) en “comentarios”, de modo que, aunque parezcan correctos al leer el programa, de hecho no se traducen ni se ejecutan.

###### **Espacios en blanco:**
Las reglas sobre el uso de espacios en blanco varían ampliamente entre los lenguajes. En FORTRAN, los espacios en blanco no son significativos en cualquier parte excepto en datos literales de cadena de caracteres. Otros lenguajes usan espacios en blanco como separadores, de modo que desempeñan un papel sintáctico importante. El SNOBOL4 se usa como operación de concatenación.

###### **Delimitadores y corchetes:**
Un delimitador es un elemento sintáctico que se usa simplemente para señalar el principio o el final de alguna unidad sintáctica, como un enunciado o expresión. Los corchetes son delimitadores apareados, por ejemplo, paréntesis o pareja de begin…end. Los delimitadores se pueden usar simplemente para mejorar la legibilidad o simplificar el análisis sintáctico, pero con más frecuencia tienen el importante propósito de eliminar ambigüedad definiendo explícitamente los límites de una construcción sintáctica particular.

##### **Formatos de campos libres y fijos:**
Una sintaxis es de campo libre si los enunciados de programa se pueden escribir en cualquier parte de un renglón de entrada sin que importe la posición sobre el renglón o las interrupciones entre renglones. Una sintaxis de campo fijo utiliza la posición sobre un renglón para transmitir información. La sintaxis campo fijo es estricta, donde cada elemento de un enunciado debe aparecer dentro de una parte dada de un renglón de entrada, se observa más a menudo en lenguajes ensambladores. Es más común el uso de un formato de campo fijo parcial; Por ejemplo, en FORTRAN los cinco primeros caracteres de cada renglón están reservados para un rótulo de enunciado. La sintaxis de campo fijo es cada vez más rara en la actualidad y la norma es el campo libre.

###### **Expresiones:**
Las expresiones son funciones que acceden a objetos de datos en un programa y devuelven algún valor. Las expresiones son los bloques sintácticos básicos de construcción a partir de los cuales se construyen enunciados. En lenguajes imperativos como C, las expresiones constituyen las operaciones básicas que permiten que cada enunciado modifique el estado de la máquina. En lenguajes aplicativos como ML o LISP, las expresiones forman el control básico de secuencia que dirige la ejecución de programas.

###### **Enunciados:**
Los enunciados constituyen el componente sintáctico más destacado en los lenguajes imperativos, la clase dominante de lenguajes que se usan en la actualidad. Su sintaxis tiene un efecto decisivo sobre la regularidad, legibilidad y facilidad de escritura generales de lenguaje. Ciertos lenguajes adoptan un formato único de enunciado básico, mientras que otros emplean diferente sintaxis para cada tipo distinto de enunciado. El primer enfoque hace énfasis en la regularidad, en tanto que el segundo resalta la legibilidad. Casi todos los lenguajes se inclinan a suministrar  diferentes estructuras sintácticas para cada tipo de enunciado. La ventaja de usar diversas estructuras sintácticas, por supuesto, es que se puede hacer que cada una exprese de manera natural las operaciones que intervienen. Una diferencia más importante en las estructuras de enunciado es que existe entre los enunciados estructurados o anidados y los enunciados simples. Un enunciado simple no contiene otros enunciados incrustados. Ejemplo APL y SNOBOL4 solo permiten enunciados simples. Un enunciado estructurado puede contener enunciados incrustados.

#### **Unidad 2 Semántica**

##### **Gramáticas de atributos**

Uno de los primeros intentos para desarrollar un modelo semántico de un LP fue en concepto de gramáticas de atributos, desarrollado por Donald Knuth. La idea era asociar una función con cada nodo del árbol de análisis sintáctico de un programa dando el contenido semántico de ese nodo. Las gramáticas de atributos se crearon agregando funciones (atributos) a cada regla de una gramática. 

Un atributo heredado es una función que relaciona valores no terminales de un árbol con valores no terminales más arriba en el árbol. O, en otras palabras, el valor funcional para los no terminales a la derecha de cualquier regla son una función del no terminal del lado izquierdo.

Un atributo sintetizado es una función que relaciona el no terminal del lado izquierdo con los valores de los no terminales del lado derecho. Estos atributos pasan información hacia arriba del árbol, es decir, fueron “sintetizados” a partir de la información de la parte baja del árbol.

Las gramáticas de atributos se pueden usar para transmitir información semántica por todo el árbol semántico. Por ejemplo, las producciones de un lenguaje pueden recoger información de declaraciones y esa información de tabla de símbolos se puede transmitir hacia abajo del árbol para usarse en la generación de código para expresiones

Atributos sintetizados: son aquellos atributos que se calculan en un símbolo no terminal a partir de los atributos de sus símbolos hijos. Estos atributos se utilizan para representar información que se "sintetiza" a medida que se construye la cadena del lenguaje. Un ejemplo de un atributo sintetizado podría ser el número de elementos en una lista, que se calcula a partir de los elementos individuales de la lista.

Atributos heredados: son aquellos atributos que se pasan desde un símbolo no terminal a uno o más de sus símbolos hijos. Estos atributos se utilizan para representar información que se "hereda" de un nivel de la gramática a otro. Un ejemplo de un atributo heredado podría ser el tipo de dato de una variable en un programa, que se hereda desde la declaración de la variable a su uso posterior en el código.

Atributos intrínsecos: son aquellos atributos que están asociados a un símbolo no terminal pero no se calculan a partir de los atributos de sus símbolos hijos ni se pasan a los símbolos hijos. Estos atributos se utilizan para representar información que es inherente a un símbolo no terminal, como el nombre de una variable en un programa o el valor de una constante en una expresión.

##### **Semántica axiomática**

Este método amplía el cálculo de predicados para incluir programas. Se puede definir la semántica de cada construcción sintáctica en el lenguaje como axiomas o reglas de inferencia que se pueden usar para deducir el efecto de la ejecución de esa construcción. Para entender el significado del programa completo, se usan los axiomas  y reglas de inferencia un poco como en las pruebas ordinarias en matemáticas. A partir del supuesto inicial de que los valores de las variables de entrada satisfacen ciertas restricciones, los axiomas y reglas de inferencia se pueden usar para deducir las restricciones que satisfacen los valores de otras variables después de la ejecución de cada enunciado de programa. En último término, se prueba que los resultados del programa satisfacen las restricciones deseadas de sus valores en relación con los valores de entrada. Es decir, se prueba que los valores de salida representan la función correcta computada a partir de los valores.

Se utiliza para lenguajes que la ejecución del programa se basa en cambios de variables de estado (imperativo), por ello este enfoque no es adecuado para los lenguajes funcionales.

##### **Semántica operacional**
Describe el **significado** del lenguaje **especificando como se ejecuta un programa en una máquina abstracta**, básicamente esta semántica se centra en **conocer el resultado** que genera el programa y **el modo en que este resultado es obtenido**. Puede estar basado en una máquina abstracta concreta (que existe) o en una genérica (que no existe físicamente, pero se especifica). Son **útiles, sobre todo, en la implementación de los lenguajes.** Porque dice como debe ejecutarse el programa en tiempo de ejecución.

##### **Semántica denotacional**
Define la función que computa el programa (se lo ve al programa como una función, entrada, proceso, salida), pero sin ocuparse de la forma en que lo hace (se abstrae). Tiene un nivel de abstracción mayor que el de la semántica operacional y esto permite estudiar propiedades formales de los programas, como, por ejemplo, las equivalencias que pueda haber entre dos programas, desde el POV del resultado que dan (sin importar la entrada, proceso). 