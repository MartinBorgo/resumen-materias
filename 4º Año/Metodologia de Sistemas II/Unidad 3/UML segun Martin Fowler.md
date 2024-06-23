## ¿Que es UML?
El Lenguaje de Modelado Unificado (UML) es una familia de notaciones gráficas respaldadas por un metamodelo único, que facilita la descripción y el diseño de sistemas de software, especialmente aquellos construidos utilizando el estilo orientado a objetos (OO). Los lenguajes de modelado gráfico han sido parte de la industria del software durante mucho tiempo. La idea principal detrás de todos ellos es que los lenguajes de programación no proporcionan un nivel de abstracción suficientemente alto como para facilitar las discusiones sobre el diseño.

El UML es un estándar relativamente abierto, controlado por el Grupo de Gestión de Objetos (OMG), un consorcio formado por diversas empresas. El OMG fue creado para desarrollar estándares que promuevan la interoperabilidad, específicamente la interoperabilidad de sistemas orientados a objetos.
### ¿Dónde se usa UML?
Existen tres modos principales en que las personas utilizan UML: como boceto, plano y lenguaje de programación. De estos, el más común, al menos desde mi perspectiva, es el uso de UML como boceto. En esta modalidad, los desarrolladores utilizan UML para facilitar la comunicación de algunos aspectos de un sistema. Al igual que los planos, UML puede emplearse tanto en ingeniería directa como en ingeniería inversa. La ingeniería directa implica dibujar un diagrama UML antes de escribir el código, mientras que la ingeniería inversa consiste en construir un diagrama UML a partir de código existente para facilitar su comprensión.

Su objetivo es utilizar los bocetos para ayudar a comunicar ideas y
alternativas acerca de lo que está a punto de hacer. No se habla sobre todo el código que se va a trabajar, solo las cuestiones importantes que
desea ejecutar más allá de sus colegas primero o secciones del diseño que quiere visualizar antes de comenzar la programación. 

La idea es que los modelos sean desarrollados por un diseñador, cuyo trabajo consiste en construir un diseño detallado para un programador de alto nivel. Este diseño debe ser tan completo que todas las decisiones de diseño estén ya establecidas, permitiendo que la programación sea una actividad relativamente sencilla que requiera poca atención adicional. El diseñador puede ser la misma persona que el programador, pero generalmente es un desarrollador de mayor rango que diseña para un equipo de programadores. La inspiración para este enfoque proviene de otras ramas de la ingeniería, donde ingenieros profesionales crean planos que luego son utilizados por las empresas constructoras para llevar a cabo la construcción.

### Diagramas en UML
| Diagrama                      | Propósito                                                                           |
| ----------------------------- | ----------------------------------------------------------------------------------- |
| Actividad                     | Describir procesos paralelos y secuenciales en la ejecución de tareas.              |
| Clase                         | Representar clases, sus funciones y las relaciones entre ellas.                     |
| Comunicación                  | Facilitar la interacción entre objetos con un enfoque en las conexiones.            |
| Componente                    | Mostrar la estructura y las conexiones entre los componentes de un sistema.         |
| Estructura compuesta          | Descomponer una clase en tiempo de ejecución para detallar su estructura interna.   |
| Despliegue                    | Visualizar el despliegue de artefactos en distintos nodos de un sistema.            |
| Visión general de interacción | Combinar diagramas de secuencia y actividad para una visión integral de procesos.   |
| Objeto                        | Ejemplificar configuraciones de objetos en casos de uso específicos.                |
| Paquete#                      | Organizar elementos del modelo en estructuras jerárquicas durante la compilación.   |
| Secuencia                     | Detallar la interacción secuencial entre objetos para clarificar flujos de trabajo. |
| Máquina estatal               | Ilustrar cambios en los estados de un objeto a lo largo de su ciclo de vida.        |
| Sincronización                | Resaltar cómo se sincronizan las interacciones entre objetos en el tiempo.          |
| Caso de uso                   | Explicar cómo los usuarios interactúan con el sistema y sus funcionalidades.        |
Aunque UML proporciona un amplio conjunto de diagramas para definir una aplicación, no abarca todos los diagramas posibles que podrían resultar útiles. En diversas situaciones, puede ser beneficioso emplear otros tipos de diagramas no contemplados en UML, y no debería dudarse en utilizar un diagrama alternativo cuando ningún diagrama de UML se ajuste completamente a las necesidades específicas

### Contenido de los casos de uso

Los casos de uso son una técnica esencial para capturar los requisitos funcionales de un sistema, describiendo las interacciones típicas entre los usuarios y el sistema, y proporcionando una visión de cómo se utiliza el sistema.

Aunque los casos de uso son un componente clave de la UML, la definición de cómo capturar su contenido es sorprendentemente limitada en UML. UML se centra en el diagrama de casos de uso, que ilustra las relaciones entre diversos casos de uso; sin embargo, el verdadero valor de los casos de uso radica en su contenido textual, mientras que el diagrama en sí es de valor relativamente limitado.

Cada caso de uso identifica un actor principal, quien interactúa con el sistema para obtener un servicio. Este actor principal es el objetivo del caso de uso y, generalmente, pero no siempre, es quien inicia el caso de uso. Pueden existir otros actores, conocidos como actores secundarios, con los que el sistema se comunica para ejecutar el caso de uso.

Cada paso en un caso de uso refleja un elemento de la interacción entre un actor y el sistema. Estos pasos deben ser declaraciones sencillas que clarifiquen quién realiza la acción, mostrando la intención del actor más que la mecánica de sus acciones. Por esta razón, la interfaz de usuario no se describe dentro del caso de uso; de hecho, la redacción de los casos de uso generalmente precede al diseño de la interfaz de usuario.

Cuando un paso en un caso de uso es complejo, puede constituir un caso de uso por sí mismo. En términos de UML, se dice que el primer caso de uso "incluye" (include) al segundo. 

#### Diagrama de casos de uso

El UML no establece especificaciones sobre el contenido de un caso de uso, pero proporciona un formato de diagrama para representarlos. Aunque estos diagramas pueden ser útiles, no son obligatorios. En la elaboración de casos de uso, es aconsejable no invertir demasiado esfuerzo en el diagrama en sí; en cambio, el foco debe estar en el contenido textual de los casos de uso.

UML también incluye otras relaciones entre casos de uso, además de la simple inclusión, como "extend" (extender). Sin embargo, recomiendo no prestarles demasiada atención. He observado numerosas situaciones en las que los equipos se enredan ineficazmente al intentar utilizar estas relaciones adicionales, desperdiciando energía valiosa. Por ello, es más beneficioso concentrarse en la descripción textual de un caso de uso, ya que ahí reside el verdadero valor de esta técnica.

Un problema común con los casos de uso es que, al centrarse en la interacción entre el usuario y el sistema, se pueden descuidar situaciones donde un cambio en un proceso de negocio podría ser la mejor solución. A menudo se habla de "casos de uso del sistema" y "casos de uso del negocio". Aunque estos términos no son precisos, generalmente se entiende que un caso de uso del sistema implica una interacción con el software, mientras que un caso de uso de negocio analiza cómo una empresa responde a un cliente o a un evento específico.

Es importante recordar que los casos de uso ofrecen una visión externa del sistema. Por tanto, no se deben esperar correlaciones directas entre los casos de uso y las clases dentro del sistema. Cuanto más analizo los casos de uso, menos valor encuentro en el diagrama de casos de uso. Con los casos de uso, es mejor concentrar la energía en el texto en lugar del diagrama. Aunque UML no especifica detalles sobre el texto de los casos de uso, es precisamente este texto el que aporta todo el valor a la técnica.

Un riesgo significativo con los casos de uso es complicarlos excesivamente, lo que puede llevar a atascos. Generalmente, es menos perjudicial hacer menos que excederse. Un par de páginas por caso de uso suelen ser suficientes para la mayoría de las situaciones. Si el documento es breve, al menos será fácil de leer y servirá como punto de partida para preguntas. Si es demasiado extenso, probablemente nadie lo leerá ni lo comprenderá completamente.

### Diagrama de actividad

Los diagramas de actividad son una técnica utilizada para describir la lógica de procedimientos, procesos de negocio y flujos de trabajo. En muchos aspectos, cumplen una función similar a los diagramas de flujo. Sin embargo, la principal diferencia entre ellos y la notación de diagrama de flujo radica en que los diagramas de actividad admiten comportamientos paralelos.

El diagrama de actividad permite a quienes ejecutan el proceso elegir el orden de las acciones. En otras palabras, el diagrama solo indica las reglas de secuencia esenciales que se deben seguir. Esto es crucial para el modelado de procesos de negocio, dado que estos procesos a menudo ocurren en paralelo. También son útiles para algoritmos concurrentes, donde hilos independientes pueden ejecutar tareas simultáneamente.

Es importante destacar que los nodos en un diagrama de actividad se denominan "acciones", y no "actividades". Estrictamente, una "actividad" se refiere a una secuencia de acciones, por lo que el diagrama muestra una actividad compuesta por varias acciones.

Una consideración importante es la familiaridad con su uso. Actualmente, los diagramas de actividad no son la técnica más utilizada en UML, y sus antecesores en el modelado de flujo tampoco gozaban de mucha popularidad. Sin embargo, hay indicios en varias comunidades de una demanda latente que una técnica estándar podría ayudar a satisfacer.
#### ¿Cuándo usar diagramas de actividad?

La principal fortaleza de los diagramas de actividad es su capacidad para apoyar y fomentar comportamientos paralelos, lo que los convierte en una herramienta invaluable para el modelado de flujos de trabajo y procesos. De hecho, gran parte del impulso detrás de las actualizaciones en UML 2 proviene de profesionales involucrados en estos campos.

Los diagramas de actividad también pueden servir como diagramas de flujo compatibles con UML, aunque esto puede no ser particularmente emocionante. Teóricamente, puedes aprovechar características como horquillas y uniones para describir algoritmos paralelos en programas concurrentes. Sin embargo, aunque no interactúo frecuentemente en entornos de programación concurrente, no he observado que sean ampliamente utilizados. Creo que esto se debe a que la mayor complejidad de la programación concurrente radica en evitar la contención de datos, y los diagramas de actividad no ofrecen mucha ayuda en este aspecto.

Frecuentemente, he visto cómo se utilizan los diagramas de actividad para describir un caso de uso. El riesgo de este enfoque es que los expertos del dominio no siempre lo comprenden fácilmente. Si ese es el caso, podría ser más efectivo utilizar la forma textual tradicional.

Los diagramas de actividad te indican lo que sucede, pero no especifican quién realiza cada acción. En el ámbito de la programación, esto significa que el diagrama no clarifica qué clase es responsable de cada acción. En el modelado de procesos de negocio, no se especifica qué parte de una organización lleva a cabo cada acción. Esto no es necesariamente un problema, ya que a menudo es más útil centrarse en qué se hace, en lugar de quién realiza cada parte de la tarea. Si necesitas mostrar quién hace qué, puedes dividir un diagrama de actividad en "particiones" (swimlanes en inglés), que demuestran las acciones que realiza una unidad de clase u organización.

Los diagramas de actividad tienen un punto de partida claramente definido, que corresponde a una invocación de un programa o rutina. Las acciones también pueden responder a señales (signals en inglés). Esto es útil cuando necesitamos enviar un mensaje y luego esperar una respuesta antes de poder continuar. Aunque generalmente se acepta esperar un evento externo, también podemos mostrar un flujo que entra en ellos, indicando que no comenzamos a actuar hasta que el flujo desencadena la aceptación.

Con los diagramas de actividad, a menudo nos encontramos con situaciones donde la salida de una acción desencadena múltiples invocaciones de otra acción. Hay varias maneras de mostrar esto, pero la mejor forma es utilizar una "región de expansión" (expansion region en inglés). Una región de expansión marca un área del diagrama de actividad donde las acciones se ejecutan una vez por cada elemento de una colección.

### Diagrama de secuencias

Los diagramas de interacción describen cómo grupos de objetos colaboran en comportamientos específicos. Dentro de UML, existen varias formas de diagramas de interacción, siendo el diagrama de secuencia el más común.

Un diagrama de secuencia captura el comportamiento de un escenario único, mostrando una serie de objetos y los mensajes que se intercambian entre ellos dentro de un caso de uso. Estos diagramas no son adecuados para mostrar detalles de algoritmos, como bucles y comportamientos condicionales, pero son excelentes para visualizar las interacciones y procesamientos que realizan los participantes.

Los diagramas de secuencia son ideales cuando se desea examinar el comportamiento de varios objetos dentro de un único caso de uso. Son efectivos para mostrar la colaboración entre objetos, aunque no son tan precisos en definir comportamientos detallados. Si buscas analizar el comportamiento de un solo objeto a través de varios casos de uso, es recomendable utilizar un diagrama de estado. Para explorar comportamientos a través de múltiples casos de uso o varios hilos, considera usar un diagrama de actividad.

Para explorar rápidamente múltiples interacciones alternativas, las tarjetas CRC pueden ser una mejor opción, ya que evitan la necesidad de mucho dibujo y borrado. A menudo es útil realizar una sesión con tarjetas CRC para explorar alternativas de diseño y luego utilizar los diagramas de secuencia para documentar cualquier interacción que se desee revisar más adelante.

Otras formas útiles de los diagramas de interacción incluyen los diagramas de comunicación, que muestran las conexiones, y los diagramas de tiempo, que representan restricciones temporales.