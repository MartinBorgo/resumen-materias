## La toma de decisiones se puede tomar de dos formas
1. Intuitiva  
2. Racional  

### Toma de decisiones intuitiva
En base a la experiencia anterior del que decide y sus expectativas. Mayor riesgo  

### Toma de decisiones racional
Se basa en información disponible debidamente evaluada por la persona que decide. Menos riesgo  

#### ¿Qué se necesita para tomar decisiones en forma racional?
Las características de la información útil  

## Sistema de soporte a las decisiones
- Sistema para servir de apoyo a la toma de decisiones  
- Decisión basada en estimaciones de valores de esas alternativas  

## Archivo
Conjunto finito organizado de registros similares que se tratan como una unidad  

## Campo de un archivo
- Conjunto de caracteres tratado como una unidad de datos  
- Elemento de dato básico  
- Se caracteriza por su longitud y su tipo  

## Registro relacionado a un archivo
- Conjunto de campos relacionados por un atributo  
- Puede ser tratado como unidad  

## Campo clave
- Campo de identificación que contiene cada registro lógico  
- Se utiliza para acceder al registro o para clasificar en un orden determinado  

## Claves múltiples
- Campos múltiples para acceder al mismo registro  

## Lenguaje
Conjunto de caracteres, convenciones y reglas para comunicar información.  
1. Pragmática (Práctica)  
2. Semántica (Significado)  
3. Sintaxis (Estructura)  

## Lenguaje de programación
Lenguaje interpretables y ejecutables por el computador  

## Lenguaje absoluto
Depende del computador. También llamados lenguaje máquina u objeto  

## Lenguaje simbólico
Lenguaje cuyas instrucciones tienen correspondencia con las instrucciones del lenguaje máquina. Deben ser traducidos al lenguaje máquina antes de ser ejecutables.

### Lenguajes de bajo nivel
Lenguajes cuyas instrucciones tienen correspondencia unívoca con las instrucciones del lenguaje absoluto.  
Usan programas ensambladores para traducir.  
Únicos para cada procesador.  

### Lenguajes de alto nivel
Lenguaje para los programadores. Sentencias equivalentes a varias instrucciones de bajo nivel.  
Independientes de la máquina.  

## Instrucción
Especificación de una operación identificando operandos y direcciones.  

## Programa
1. Secuencia lógica y completa de instrucciones para dirigir a un computador en la ejecución de un problema  
2. Secuencia lógica de instrucciones que un computador almacena, interpreta y ejecuta.  

## Sistema. Definición general y definición en programación
Conjunto de elementos interrelacionados destinados a cumplir un objetivo total.  
En programación, un conjunto de programas que se interrelacionan a fin de conseguir un objetivo.  
Un sistema resuelve un conjunto de problemas, o apunta a resolver una serie de problemas particulares.  

## Programas a medida y enlatados
Construidos por o para un individuo u organización específicos.  
Puede ser un problema inédito o no tratado.  
Los enlatados se los concibe en forma estándar, se orientan a aplicaciones específicas de los usuarios.  

## Etapas del desarrollo de un sistema
- Definir el problema  
- Análisis del sistema  
- Diseño de la solución  
- Programación  
- Prueba  
- Implementación  
- Documentación  

## Definir el problema
Definir claramente las necesidades observando la utilización del sistema actual de procesamiento de información  

## Análisis del sistema
Estudiar en profundidad el funcionamiento actual del sistema, sus límites, componentes y relaciones. Se identifican datos utilizados, su manejo y la información a obtener  

## Diseño de la solución
De acuerdo a la información obtenida y a los objetivos, se usan modelos lógicos para la solución. Si existen soluciones equifinales se evalúan y elige una de ellas  

## Programación
Se vuelca el modelo construido a uno o varios programas de computación. Se desarrollan en algún lenguaje de programación, analizando varios factores como el tipo de equipamiento, complejidad de la solución y usuarios que la operarán  

## Prueba
Funcionamiento del sistema, usando datos ficticios para detectar errores. Si existe error, implica revisar la solución diseñada o corregir la información obtenida durante el análisis.  

## Implementación
Puesta en marcha de manera gradual con un posterior seguimiento para determinar su correcto funcionamiento. Se adquiere el equipo y elementos necesarios para su funcionamiento.  

## Documentación
Para facilitar la modificación del sistema posteriormente. Fundamentalmente por si las modificaciones deben realizarlas otras personas.  

## Utilitarios de base
- Editor  
- Intérprete  
- Compilador  
- Sistemas operativos  

## Sistema lógico de base
Relativo al conjunto de programas y rutinas diseñadas para permitir la utilización racional y eficiente de los recursos del soporte físico de un sistema de procesamiento de datos.  

## Intérpretes y compiladores
Denominados traductores, se utilizan para pasar de lenguaje de alto nivel a bajo nivel y viceversa.  

## Compilador
Programa que traduce el programa fuente a programa objeto.  
Solo efectúa la traducción, no lo ejecuta.  

## Intérprete
Traduce cada instrucción o sentencia en lenguaje fuente a código máquina e inmediatamente se ejecuta.  
Traduce una y la ejecuta, así secuencialmente con todas.  

## Compilador vs Intérprete

|                      | Compilador                                        | Intérprete                                                                          |
| -------------------- | ------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Edición              | No tiene editor, no corrige. Salvo algunos nuevos | Corrige errores de sintaxis                                                         |
| Ejecución            | Si se modifica el código, se recompila            | Se puede modificar y probar. Una nueva corrida del programa debe ser reinterpretada |
| Ocupación de memoria | Solo se carga el código objeto                    | Carga el programa más el código fuente                                              |
| Rapidez              | Solo ejecutar el código máquina                   | Se traduce cada vez que se ejecuta                                                  |

## Lenguajes de programación importantes del siglo 20
FORTRAN (1954). Traductor de fórmulas, compilado. Uso científico.  
COBOL (1959). Compilado, manejo de estructuras de datos. Lenguaje orientado hacia negocios comunes.  
Pascal (1971). Similar a C.  
C (1972). Alto nivel para programación de bajo nivel. Usado para programar Linux, Unix.  
BASIC (1985). Intérprete y compilador, propósito general.  

## Editor
Se utiliza para crear, ver y modificar programa fuente.  
Los lenguajes que trabajan con intérpretes tienen su propio editor.  

## Sistemas operativos
Programa o conjunto de programas que permiten el mejor aprovechamiento de los recursos del sistema, base de escritura de programas de aplicación.  
Componente del soporte lógico con un conjunto integrado de instrucciones y rutinas que regulan y controlan la ejecución de programas en un computador y supervisan la operación y explotación del mismo.  

## Programa supervisor
Clave del sistema operativo.  
Este se carga en la RAM mientras la computadora esté en uso, controla el funcionamiento de la misma.  

## Funciones específicas del programa supervisor
1. Control de tareas  
2. Calendarización del sistema. Balancear los requisitos de entrada y salida y de proceso  
3. Manejar las interrupciones del sistema cuando se usa multiprogramación  
4. Controlar el estado del sistema  
5. Inventario de tareas realizadas  
6. Seguridad del sistema  
