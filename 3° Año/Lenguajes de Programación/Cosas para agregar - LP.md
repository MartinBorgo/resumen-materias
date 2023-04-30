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