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
##### Ligadura y tiempo de ligadura (enlace, enlace = ligadura)
Ligadura de un elemento de programa a una caracteristica o propiedad particular como simplemente la eleccion de la propiedad de entre un conjunto de propiedades posibles. El momento durante la formulacion o procesamiento del programa en el que se hace esta eleccion se conoce como el tiempo de ligadura de esa propiedad para ese elemento.

##### Clases de ligaduras
Es posible distinguir unos cuantos tiempos de enlace principales si se recuerda el supuesto basico de que en el procesamiento de un programa, independientemende del lenguaje, siempre interviene un paso de traduccion seguido de la ejecucion del programa traducido.

1. Tiempo de ejecucion: Muchos enlaces se llevan a cabo durante la ejecucion del programa. Esto incluye enlaces de variables a sus valores, asi como el enlace de variables a localidades particulares de almacenamiento. Es posible distinguir dos subcategorias importantes *Al entrar a un subprograma o bloque* y *En puntos arbitrarios durante la ejecucion*.
	1. Al entrar a un subprograma o bloque: En casi todos los lenguajes las clases importantes de enlaces solo pueden ocurrir ren el momento de entrar a un subprograma o bloque durante la ejecucion. Por ejemplo. en C y Pascal, el enlace de parametros formales a reales y el enlace de parametros formales a localidades particulares de almacenamiento solo pueden ocurrir a entrar a un subprograma.
	2. En puntos arbitrarios durante la ejecucion: Ciertos enlaces pueden ocurrir en cualquier punto durante la ejecucion de un programa. El ejemplo mas importante en este caso es el enlace basico de variables a valores a traves de asignacion, en tanto que ciertos lenguajes como LISP tambien permiten que ocurra el enlace de nombres a localidades de almacenamiento en puntos arbitrarios del programa.

2. Tiempo de traduccion (tiempo de compilacion): Se pueden distinguir tres clases distintas de enlaces: 
	1. Enlaces elegidos por el programador: Al escribir un programa, el programador toma conscientemente muchas decisiones respecto a opciones de nombres de variables, tipos para las variables, etc. Que representan enlaces durante la traduccion. El traductor del lenguaje utiliza estos enlaces para determinar la forma final del programa objeto.

	1.  Enlaces elegidos por el traductor: Ciertos enlances son elegidos por el traductor del lenguaje sin que el programador los especifique directamente. Por ejemplo, la localidad relativa de un objeto de datos en el almacenamiento asignado para un procedimiento se maneja en general sin el conocimiento o intervencion del programador. Como se guardan los arreglos, en su caso, es otra decision que toma el traductor del lenguaje.
##### La distinción entre estático y dinámico
Una de las cuestiones más importantes a las que nos enfrentamos al diseñar un compilador
para un lenguaje es la de qué decisiones puede realizar el compilador acerca de un programa. Si un lenguaje utiliza una directiva que permite al compilador decidir sobre una cuestión, entonces decimos que el lenguaje utiliza una directiva *estática*, o que la cuestión puede decidirse en *tiempo de compilación*. Por otro lado, se dice que una directiva que sólo permite realizar una decisión a la hora de ejecutar el programa es una directiva *dinámica*, o que requiere una decisión en tiempo de ejecución.

Un lenguaje utiliza el *alcance estático* o *alcance léxico* si es posible determinar el alcance de una declaración con sólo ver el programa. En cualquier otro caso, el lenguaje utiliza un *alcance dinámico*. Con el alcance dinámico, a medida que se ejecuta el programa, el mismo uso de x podría referirse a una de varias declaraciones distintas de x.

**Ejemplo:** Como otro ejemplo de la distinción entre estático y dinámico, considere el
uso del término “static” según se aplica a los datos en la declaración de una clase en Java. En Java, una variable es un nombre para una ubicación en memoria que se utiliza para almacenar un valor de datos. Aquí, “static” no se refiere al alcance de la variable, sino a la habilidad del compilador para determinar la ubicación en memoria en la que puede encontrarse la variable declarada. Una declaración como:
**public static int x;**

hace de x una variable de clase e indica que sólo hay una copia de x, sin importar cuántos
objetos se creen de esta clase. Lo que es más, el compilador puede determinar una ubicación en memoria en la que se almacene este entero x. En contraste, si se hubiera omitido la palabra “static” de esta declaración, entonces cada objeto de la clase tendría su propia ubicación en la que se guardara x, y el compilador no podría determinar todos estos lugares antes de ejecutar el programa. 
