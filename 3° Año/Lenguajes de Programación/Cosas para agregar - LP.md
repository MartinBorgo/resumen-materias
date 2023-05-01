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

#### Unidad 3 entidades
##### La distinción entre estático y dinámico
Una de las cuestiones más importantes a las que nos enfrentamos al diseñar un compilador
para un lenguaje es la de qué decisiones puede realizar el compilador acerca de un programa. Si un lenguaje utiliza una directiva que permite al compilador decidir sobre una cuestión, entonces decimos que el lenguaje utiliza una directiva *estática*, o que la cuestión puede decidirse en *tiempo de compilación*. Por otro lado, se dice que una directiva que sólo permite realizar una decisión a la hora de ejecutar el programa es una directiva *dinámica*, o que requiere una decisión en tiempo de ejecución.

Un lenguaje utiliza el *alcance estático* o *alcance léxico* si es posible determinar el alcance de una declaración con sólo ver el programa. En cualquier otro caso, el lenguaje utiliza un *alcance dinámico*. Con el alcance dinámico, a medida que se ejecuta el programa, el mismo uso de x podría referirse a una de varias declaraciones distintas de x.

**Ejemplo:** Como otro ejemplo de la distinción entre estático y dinámico, considere el
uso del término “static” según se aplica a los datos en la declaración de una clase en Java. En Java, una variable es un nombre para una ubicación en memoria que se utiliza para almacenar un valor de datos. Aquí, “static” no se refiere al alcance de la variable, sino a la habilidad del compilador para determinar la ubicación en memoria en la que puede encontrarse la variable declarada. Una declaración como:
**public static int x;**

hace de x una variable de clase e indica que sólo hay una copia de x, sin importar cuántos
objetos se creen de esta clase. Lo que es más, el compilador puede determinar una ubicación en memoria en la que se almacene este entero x. En contraste, si se hubiera omitido la palabra “static” de esta declaración, entonces cada objeto de la clase tendría su propia ubicación en la que se guardara x, y el compilador no podría determinar todos estos lugares antes de ejecutar el programa. 
