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

[^1]: Hablando en sentido técnico, para el lexema 60 formaríamos un token como *<número, 4>*, en donde 4 apunta a la tabla de símbolos para la representación interna del entero 60