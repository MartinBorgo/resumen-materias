# Anki
TARGET DECK: Facultad:: Sistemas:: Primer año:: Organización de computadoras:: Unidad 7
# Archivos
![[Unidad 7.pdf]]
# Notas


## La toma de decisiones se puede tomar de dos formas #flashcard
1. Intuitiva
2. Racional
<!--ID: 1700156627124-->




### Toma de decisiones intuitiva #flashcard
En base a la experiencia anterior del que decide y sus expectativas. Mayor riesgo
<!--ID: 1700156627129-->




### Toma de decisiones racional #flashcard
Se basa en información disponible debidamente evaluada por la persona que decide. Menos riesgo
<!--ID: 1700156627133-->


#### ¿Qué se necesita para tomar decisiones en forma racional? #flashcard
Las características de la información útil
<!--ID: 1700156627136-->


## Sistema de soporte a las decisiones #flashcard
- Sistema para servir de apoyo a la toma de decisiones
- Decisión basada en estimaciones de valores de esas alternativas
<!--ID: 1700156627140-->


## Archivo #flashcard
Conjunto finito organizado de registros similares que se tratan como una unidad
<!--ID: 1700156627146-->


## Campo de un archivo #flashcard
- Conjunto de caracteres tratado como una unidad de datos
- Elemento de dato básico
- Se caracteriza por su longitud y su tipo
<!--ID: 1700156627150-->


## Registro relacionado a un archivo #flashcard
- Conjunto de campos relacionados por un atributo
- Puede ser tratado como unidad
<!--ID: 1700156627154-->


## Campo clave #flashcard
- Campo de identificación que contiene cada registro lógico
- Se utiliza para acceder al registro o para clasificar en un orden determinado
<!--ID: 1700156627158-->


## Claves múltiples #flashcard
- Campos múltiples para acceder al mismo registro
<!--ID: 1700156627164-->


## Lenguaje #flashcard
Conjunto de caracteres, convenciones y reglas para comunicar información. 
1. Pragmática (Práctica)
2. Semántica (Significado)
3. Sintaxis (Estructura)
<!--ID: 1700156627170-->


## Lenguaje de programación #flashcard
Lenguaje interpretables y ejecutables por el computador
<!--ID: 1700156627174-->


## Lenguaje absoluto #flashcard
Depende del computador. También llamados lenguaje máquina u objeto
<!--ID: 1700156627179-->


## Lenguaje simbólico #flashcard
Lenguaje cuyas instrucciones tienen correspondencia con las instrucciones del lenguaje máquina. Deben ser traducidos al lenguaje máquina antes de ser ejecutables.
<!--ID: 1700156627183-->


### Lenguajes de bajo nivel #flashcard
Lenguajes cuyas instrucciones tienen correspondencia univoca con las instrucciones del lenguaje absoluto. 
Usan programas ensambladores para traducir.
Únicos para cada procesador. 
<!--ID: 1700156627187-->


### Lenguajes de alto nivel #flashcard
Lenguaje para los programadores. Sentencias equivalentes a varias instrucciones de bajo nivel.
Independientes de la máquina.
<!--ID: 1700156627191-->


## Instrucción #flashcard
Espicificación de una operación identificando operandos y direcciones.
<!--ID: 1700156627196-->


## Programa #flashcard
1. Secuencia lógica y completa de instrucciones para dirigir a un computador en la ejecución de un problema
2. Secuencia lógica de instrucciones que un computador almacena, interpreta y ejecuta.
<!--ID: 1700156627201-->


## Sistema. Definición general y definición en programación #flashcard
Conjunto de elementos interrelacionados destinados a cumplir un objetivo total.
En programación, un conjunto de programas que se interrelacionan a fin de conseguir un objetivo.
Un sistema resuelve un conjunto de problemas, o apunta a resolver una serie de problemas particulares.
<!--ID: 1700156627205-->


## Programas a medidas y enlatados #flashcard
Construidos por o para un individuo u organización específicos. 
Puede ser un problema inédito o no tratado
Los enlatados se los concibe en forma stándard, se orientan a aplicaciones específicas de los usuarios.
<!--ID: 1700156627208-->


## Etapas del desarrollo de un sistema #flashcard
- Definir el problema
- Análisis del sistema
- Diseño de la solución
- Programación
- Prueba
- Implementación
- Documentación
<!--ID: 1700156627214-->


## Definir el problema #flashcard
Definir claramente las necesidades observando la utilización del sistema actual de procesamiento de información
<!--ID: 1700156627218-->


## Análisis del sistema #flashcard
Estudiar en profundidad el funcionamiento actual del sistema, sus límites, componentes y relaciones. Se identifican datos utilizados, su manejo y la información a obtener
<!--ID: 1700156627223-->


## Diseño de la solución #flashcard
De acuerdo a la información obtenida y a los objetivos, se usan modelos lógicos para la solución. Si existen soluciones equifinales se evaluan y elige una de ellas
<!--ID: 1700156627227-->


## Programación #flashcard
Se vuelca el modelo construido a uno o varios programas de computación. Se desarrollan en algún lenguaje de programación, analizando varios factores como el tipo de equipamiento, complejidad de la solución y usuarios que la operarán
<!--ID: 1700156627233-->


## Prueba #flashcard
Funcionamiento del sistema, usando datos ficticios para detectar errores. Si existe error, implica revisar la solución diseñada o corregir la información obtenida durante el análiisis.
<!--ID: 1700156627240-->


## Implementación #flashcard
Puesta en marcha de manera gradual con un posterior seguimiento para determinar su correcto funcionamiento. Se adquiere el equipo y elementos necesarios para su funcionamiento
<!--ID: 1700156627246-->


## Documentación #flashcard
Para facilitar la modificación del sistema posteriormente. Fundamentalmente por si las modificaciones deben realizarlas otras personas.
<!--ID: 1700156627250-->


## Utiliarios de base #flashcard
- Editor
- Intérprete
- Compilador
- Sistemas operativos
<!--ID: 1700156627254-->


## Sistema lógico de base #flashcard
Relativo al conjunto de programasy rutinas diseñadas para permitir la utilización racional y eficiente de los recursos del soporte físico de un sistema de procesamiento de datos.
<!--ID: 1700156627259-->


## Intérpretes y compiladores #flashcard
Denominados traductores, se utilizan para pasar de lenguaje de alto nivel a bajo nivel y viceversa
<!--ID: 1700156627264-->


## Compilador #flashcard
Programa que traduce el programa fuente a programa objeto.
Solo efectúa la traducción, no lo ejecuta.
<!--ID: 1700156627270-->


## Intérprete #flashcard
Traduce cada instrucción o sentencia en lenguaje fuente a código máquina e inmediatamente se ejecuta.
Traduce una y la ejecuta, así secuencialmente con todas.
<!--ID: 1700156627278-->


## Compilador vs Intérprete #flashcard

|                      | Compilador                                        | Intérprete                                                                          |
| -------------------- | ------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Edición              | No tiene editor, no corrige. Salvo algunos nuevos | Corrige errores de sintáxis                                                         |
| Ejecución            | Si se modifica el código, se recompila            | Se puede modificar y probar. Una nueva corrida del programa debe ser reinterpretada |
| Ocupación de memoria | Solo se carga el código objeto                    | Carga el programa más el código fuente                                              |
| Rapidez              | Solo ejecutar el código máquina                   | Se traduce cada vez que se ejecuta                                                  |
<!--ID: 1700156627283-->


## Lenguajes de programación importantes del siglo 20 #flashcard
FORTRAN (1954). Traductor de fórmulas, compilado. Uso científico.
COBOL (1959). Compilado, manejo de estructuras de datos. Lenguaje orientado hacia negocios comunes
Pascal (1971). Similar a C
C (1972). Alto nivel para programación de bajo nivel. Usado para programar linux, unix
BASIC (1985). Intérprete y compilador, propósito general
<!--ID: 1700156627287-->


## Editor #flashcard
Se utiliza para crear, ver y modificar programa fuente.
Los lenguajes que trabajan con intérpretes tienen su propio editor.
<!--ID: 1700156627292-->


## Sistemas operativos #flashcard
Programa o conjunto de programas que permiten el mejor aprovechamiento de los recursos del sistema, base de escritura de programas de aplicación.
Componente del soporte lógico con un conjunto integrado de instrucciones y rutinas que regulan y controlan la ejecución de programas en un computador y supervisan la operación y explotación del mismo.
<!--ID: 1700156627300-->


## Programa supervisor #flashcard
Clave del sistema operativo.
Este se carga en la RAM mientras la computadora esté en uso, controla el funcionamiento de la misma.
<!--ID: 1700156627306-->


## Funciones específicas del programa supervisor #flashcard
1. Control de tareas
2. Calendarización del sistema. Balancear los requisitos de entrada y salida y de proceso
3. Manejar las interrupciones del sistema cuando se usa multiprogramación
4. Controlar el estado del sistema
5. Inventario de tareas realizadas
6. Seguridad del sistema
<!--ID: 1700156627312-->
