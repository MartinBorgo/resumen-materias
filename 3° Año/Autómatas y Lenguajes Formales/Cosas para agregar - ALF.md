#### Máquinas secuenciales
Las máquinas secuenciales precedieron históricamente a los autómatas finitos. Mientras estos se dirigen principalmente al reconocimiento de lenguajes, las máquinas secuencias encuentran su aplicación principal en el diseño de circuitos electrónicos. Esencialmente, una máquina secuencia es un autómata finito determinista, sin estados finales, que le sirven al autómata para aceptar las palabras del lenguaje que reconoce. En su lugar, como los circuitos electrónicos que representa, tiene la capacidad de generar símbolos de salida, que, como los símbolos de entrada, pertenecerán a un alfabeto determinado, el alfabeto de salida, que no tiene por qué ser el mismo que el de entrada.
Existen dos tipos diferentes de máquina secuencial.
- Máquina secuencial de Mealy. Intuitivamente, se trata de un dispositivo capaz de adoptar distintos estados a lo largo de su historia y de pasar de uno a otro en función del estado en que se encuentra y de la información o estimulo (entrada) que recibe del entorno. Además, la máquina es capaz de reaccionar sobre el entorno mediante respuestas (salidas). En cada instante, la máquina secuencial se encuentra en un estado concreto, recibe un símbolo del alfabeto de entrada, pasa a un nuevo estado (posiblemente el mismo) y genera un símbolo del alfabeto de salida. Tanto el nuevo estado como el símbolo de salida generado dependen exclusivamente del estado anterior de la máquina y del símbolo de entrada que acaba de recibir.

- Máquina secuencial de Moore. Se trata de un caso particular de la máquina secuencial de Mealy, en la que la salida producida por la máquina no depende del símbolo de entrada recibida en el mismo momento, sino tan solo del estado en que se encuentra.

Se pueden representar en forma de tablas o en forma de diagramas de estados. Poseen además equivalencia y minimización de máquinas secuenciales.

#### Sobre el determinismo del AF
Un autómata finito puede ser determinista si, para cada estado y cada símbolo de entrada, existe una transición única a otro estado. Es decir, dado un estado y un símbolo de entrada, el autómata determinista siempre sabe exactamente a qué estado debe moverse a continuación, sin necesidad de tomar decisiones o elegir entre varias opciones.

Esta característica de un autómata finito determinista lo hace más fácil de implementar y analizar, ya que su comportamiento está completamente determinado por su estructura y función de transición.

##### Sobre la extensión de la función de transición
La función de transición es una función matemática que se define en un autómata finito determinista (AFD) y que toma como entrada un estado del autómata y un símbolo del alfabeto de entrada, y devuelve como salida el siguiente estado en el que debe encontrarse el autómata después de haber leído ese símbolo desde el estado actual.

La extensión de la función de transición se refiere a la posibilidad de extender esta función de transición a cadenas de símbolos del alfabeto de entrada, de tal forma que se pueda obtener el estado final en el que debería estar el autómata después de haber procesado completamente dicha cadena. Esta función extendida se llama ***función de transición extendida o función de transición de cadena*** (o sobre palabras).

##### Minimización de AFD
Los algoritmos que simulan o implementan automatas finitos deterministas suelen requerir un espacio más o menos proporcional al número de estados del autómata, por lo que interesa que el número de dichos estados sea el menor posible. En un autómata puede haber dos tipos de estados *innecesarios*, que es posible eliminar o combinar para minimizar el número de estados. Por esta razón, existen dos operaciones de minimización diferentes:

- Eliminación de estados inaccesibles: Un estado es inaccesible si no se puede alcanzar desde el estado inicial del AFD siguiendo cualquier combinación de transiciones de entrada. Estos estados no son necesarios para el funcionamiento del AFD y pueden ser eliminados sin afectar su comportamiento.

- Agrupación de estados equivalentes o indistinguibles: Dos estados son equivalentes si tienen el mismo comportamiento desde la perspectiva de cualquier cadena de entrada. Es decir, si tienen las mismas transiciones de entrada y salida y llegan a estados finales o no finales de manera similar. La agrupación de estados equivalentes en un único estado reduce el número total de estados del AFD.

### Procesadores de lenguaje
Un compilador es un programa que puede leer un programa en un lenguaje (el lenguaje fuente) y traducirlo en un programa equivalente en otro lenguaje (el lenguaje destino). Una función importante del compilador es reportar cualquier error en el programa fuente que detecte durante el proceso de traducción.

Un intérprete es otro tipo común de procesador de lenguaje. En vez de producir un programa destino como una traducción, el intérprete nos da la apariencia de ejecutar directamente las operaciones especificadas en el programa de origen (fuente) con las entradas proporcionadas por el usuario.

Ejemplo:
Los procesadores del lenguaje Java combinan la compilación y la interpretación. Un programa fuente en Java puede compilarse primero en un formato intermedio, llamado bytecodes. Después, una máquina virtual los interpreta. Un beneficio de este arreglo es que los bytecodes que se compilan en una máquina pueden interpretarse en otra, tal vez a través de una red. Para poder lograr un procesamiento más rápido de las entradas a las salidas, algunos compiladores de Java, conocidos como compiladores just-in-time (justo a tiempo), traducen los bytecodes en lenguaje máquina justo antes de ejecutar el programa intermedio para procesar la entrada.

El compilador puede producir un programa destino en ensamblador como su salida, ya que es más fácil producir el lenguaje ensamblador como salida y es más fácil su depuración. A continuación, el lenguaje ensamblador se procesa mediante un programa llamado ensamblador, el cual produce código máquina relocalizable como su salida.

A menudo, los programas extensos se compilan en partes, por lo que tal vez haya que enlazar (vincular) el código máquina relocalizable con otros archivos objeto relocalizables y archivos de biblioteca para producir el código que se ejecute en realidad en la máquina.

El enlazador resuelve las direcciones de memoria externas, en donde el código en un archivo puede hacer referencia a una ubicación en otro archivo. Entonces, el cargador reúne todos los archivos objeto ejecutables en la memoria para su ejecución


#### La estructura de un compilador

Un compilador tiene dos procesos: análisis y síntesis. 

La parte del análisis divide el programa fuente en componentes e impone una estructura gramatical sobre ellas. Después utiliza esta estructura para crear una representación intermedia del programa fuente. Si la parte del análisis detecta que el programa fuente está mal formado en cuanto a la sintaxis, o que no tiene una semántica consistente, entonces debe proporcionar mensajes informativos para que el usuario pueda corregirlo. La parte del análisis también recolecta información sobre el programa fuente y la almacena en una estructura de datos llamada tabla de símbolos, la cual se pasa junto con la representación intermedia a la parte de la síntesis.

La parte de la síntesis construye el programa destino deseado a partir de la representación intermedia y de la información en la tabla de símbolos. A la parte del análisis se le llama comúnmente el front-end del compilador; la parte de la síntesis (propiamente la traducción) es el back-end. Si examinamos el proceso de compilación con más detalle, podremos ver que opera como una secuencia de fases, cada una de las cuales transforma una representación del programa fuente en otro. En la práctica varias fases pueden agruparse, y las representaciones intermedias entre las fases agrupadas no necesitan construirse de manera explícita. La tabla de símbolos, que almacena información sobre todo el programa fuente, se utiliza en todas las fases del compilador.

##### Análisis de léxico
A la primera fase de un compilador se le llama análisis de léxico o escaneo. El analizador de léxico lee el flujo de caracteres que componen el programa fuente y los agrupa en secuencias significativas, conocidas como *lexemas*. Para cada lexema, el analizador léxico produce salida un *token* de la forma:
*<nombre-token, valor-atributo>*
que pasa a la fase siguiente, el análisis de la sintaxis. En el token, el primer componente nombre-token es un símbolo abstracto que se utiliza durante el análisis sintáctico, y el segundo componente valor-atributo apunta a una entrada en la tabla de símbolos para este token. La información de la entrada en la tabla de símbolos se necesita para el análisis semántico y la generación de código.

Ejemplo:
*posicion = inicial + velocidad * 60*
Los caracteres en esta asignación podrían agruparse en los siguientes lexemas y mapearse a los siguientes tokens que se pasan al analizador sintáctico:

1. posicion es un lexema que se asigna a un token *<id, 1>*, en donde id es un símbolo abstracto que representa la palabra identificador y 1 apunta a la entrada en la tabla de símbolos para posicion. La entrada en la tabla de símbolos para un identificador contiene información acerca de este, como su nombre y tipo.
2. El símbolo de asignación = es un lexema que se asigna al token *<=>*. Como este token no necesita un valor-atributo, hemos omitido el segundo componente. Podríamos haber utilizado cualquier símbolo abstracto como asignar para el nombre-token, pero por conveniencia de notación hemos optado por usar el mismo lexema como el nombre para el símbolo abstracto.
3. inicial es un lexema que se asigna al token *<id, 2>*, en donde 2 apunta a la entrada en la tabla de símbolos para inicial.
4. \+ es un lexema que se asigna al token *<+>*.
5. velocidad es un lexema que se asigna al token *<id, 3>*, en donde 3 apunta a la entrada en la tabla de símbolos para velocidad.
6. \* es un lexema que se asigna al token *<\*>*.
7. 60 es un lexema que se asigna al token *<60>*[^1].
![[ejemploTraduccion.PNG]]

##### Análisis sintáctico
La segunda fase del compilador es el análisis sintáctico o parsing. El parser (analizador sintáctico) utiliza los primeros componentes de los tokens producidos por el analizador de léxico para crear una representación intermedia en forma de árbol que describa la estructura gramatical del flujo de tokens. Una representación típica es el árbol sintáctico, en el cual cada nodo interior representa una operación y los hijos del nodo representan los argumentos de la operación. Las fases siguientes del compilador utilizan la estructura gramatical para ayudar a analizar el programa fuente y generar el programa destino.

Sigamos con el ejemplo del análisis léxico:
**posicion = inicial + velocidad \* 60**
El árbol tiene un nodo interior etiquetado como \*, con <id, 3> como su hijo izquierdo, y el entero 60 como su hijo derecho. El nodo <id, 3> representa el identificador velocidad. El nodo etiquetado como \* hace explícito que primero debemos multiplicar el valor de velocidad por 60. El nodo etiquetado como + indica que debemos sumar el resultado de esta multiplicación al valor de inicial. La raíz del árbol, que se etiqueta como =, indica que debemos almacenar
el resultado de esta suma en la ubicación para el identificador posicion. Este ordenamiento de operaciones es consistente con las convenciones usuales de la aritmética, las cuales nos indican que la multiplicación tiene mayor precedencia que la suma y, por ende, debe realizarse antes que la suma.

##### Análisis semántico
El analizador semántico utiliza el árbol sintáctico y la información en la tabla de símbolos para comprobar la consistencia semántica del programa fuente con la definición del lenguaje. También recopila información sobre el tipo y la guarda, ya sea en el árbol sintáctico o en la tabla de símbolos, para usarla más tarde durante la generación de código intermedio. Una parte importante del análisis semántico es la comprobación (verificación) de tipos, en donde el compilador verifica que cada operador tenga operandos que coincidan. Por ejemplo, muchas definiciones de lenguajes de programación requieren que el índice de un arreglo sea entero; el compilador debe reportar un error si se utiliza un número de punto flotante para indexar el arreglo. La especificación del lenguaje puede permitir ciertas conversiones de tipo conocidas como coerciones.

##### Generación de código intermedio
En el proceso de traducir un programa fuente a código destino, un compilador puede construir una o más representaciones intermedias, las cuales pueden tener una variedad de formas. Los árboles sintácticos son una forma de representación intermedia; por lo general, se utilizan durante el análisis sintáctico y semántico. Después del análisis sintáctico y semántico del programa fuente, muchos compiladores generan un nivel bajo explícito, o una representación intermedia similar al código máquina, que podemos considerar como un programa para una máquina abstracta. Esta representación intermedia debe tener dos propiedades importantes: debe ser fácil de producir y fácil de traducir en la máquina destino.

##### Optimización de código
La fase de optimización de código independiente de la máquina trata de mejorar el código intermedio, de manera que se produzca un mejor código destino. Por lo general, mejor significa más rápido, pero pueden lograrse otros objetivos, como un código más corto, o un código de destino que consuma menos poder. Hay una gran variación en la cantidad de optimización de código que realizan los distintos compiladores. En aquellos que realizan la mayor optimización, a los que se les denomina como “compiladores optimizadores”, se invierte mucho tiempo en esta fase. Hay optimizaciones simples que mejoran en forma considerable el tiempo de ejecución del programa destino, sin reducir demasiado la velocidad de la compilación.

##### Generación de código
El generador de código recibe como entrada una representación intermedia del programa fuente y la asigna al lenguaje destino. Si el lenguaje destino es código máquina, se seleccionan registros o ubicaciones (localidades) de memoria para cada una de las variables que utiliza el programa. Después, las instrucciones intermedias se traducen en secuencias de instrucciones de máquina que realizan la misma tarea. Un aspecto crucial de la generación de código es la asignación juiciosa de los registros para guardar las variables, es decir, al proceso de decidir qué variables deben almacenarse en los registros de la CPU.

##### Administración de la tabla de símbolos
Una función esencial de un compilador es registrar los nombres de las variables que se utilizan en el programa fuente, y recolectar información sobre varios atributos de cada nombre. Estos atributos pueden proporcionar información acerca del espacio de almacenamiento que se asigna para un nombre, su tipo, su alcance (en qué parte del programa puede usarse su valor), y en el caso de los nombres de procedimientos, cosas como el número y los tipos de sus argumentos, el método para pasar cada argumento (por ejemplo, por valor o por referencia) y el tipo devuelto. La tabla de símbolos es una estructura de datos que contiene un registro para cada nombre de variable, con campos para los atributos del nombre. La estructura de datos debe diseñarse de tal forma que permita al compilador buscar el registro para cada nombre, y almacenar u obtener datos de ese registro con rapidez. 

[^1]: Hablando en sentido técnico, para el lexema 60 formaríamos un token como *<número, 4>*, en donde 4 apunta a la tabla de símbolos para la representación interna del entero 60