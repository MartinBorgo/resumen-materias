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

La extensión de la función de transición se refiere a la posibilidad de extender esta función de transición a cadenas de símbolos del alfabeto de entrada, de tal forma que se pueda obtener el estado final en el que debería estar el autómata después de haber procesado completamente dicha cadena. Esta función extendida se llama función de transición extendida o función de transición de cadena (o sobre palabras).

##### Minimización de AFD
Los algoritmos que simulan o implementan automatas finitos deterministas suelen requerir un espacio más o menos proporcional al número de estados del autómata, por lo que interesa que el número de dichos estados sea el menor posible. En un autómata puede haber dos tipos de estados *innecesarios*, que es posible eliminar o combinar para minimizar el número de estados. Por esta razón, existen dos operaciones de minimización diferentes:

- Eliminación de estados inaccesibles: Un estado es inaccesible si no se puede alcanzar desde el estado inicial del AFD siguiendo cualquier combinación de transiciones de entrada. Estos estados no son necesarios para el funcionamiento del AFD y pueden ser eliminados sin afectar su comportamiento.

- Agrupación de estados equivalentes o indistinguibles: Dos estados son equivalentes si tienen el mismo comportamiento desde la perspectiva de cualquier cadena de entrada. Es decir, si tienen las mismas transiciones de entrada y salida y llegan a estados finales o no finales de manera similar. La agrupación de estados equivalentes en un único estado reduce el número total de estados del AFD.