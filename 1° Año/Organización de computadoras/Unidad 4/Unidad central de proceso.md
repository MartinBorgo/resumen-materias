## ¿Cómo se analiza una computadora?
Al ser un sistema complejo, se analiza por medio de una **organización jerárquica** que permite comprender cómo interactúan sus componentes.

## ¿Qué es la estructura?
Es el modo en que los componentes están interrelacionados, estableciendo la base de cómo una computadora gestiona las tareas asignadas.

### Componentes estructurales de una computadora
1. **CPU**: Unidad Central de Proceso, el cerebro del sistema.
2. **Memoria principal**: Donde se almacenan los datos y programas temporalmente.
3. **E/S**: Entrada/Salida, los medios por los cuales la computadora interactúa con el entorno externo.
4. **Sistema de interconexión**: Los buses que permiten la comunicación entre los componentes.

### Componentes estructurales de una UCP (Unidad Central de Proceso)
1. **Unidad de control**: Dirige y coordina el funcionamiento de la CPU.
2. **Unidad aritmético-lógica**: Procesa las operaciones aritméticas y lógicas.
3. **Registros**: Proporcionan almacenamiento interno para la CPU.
4. **Interconexiones**: Permiten la comunicación entre los componentes de la CPU.

## ¿Qué es el funcionamiento?
La operación de cada componente individual como parte de la estructura.

### Funciones básicas de una computadora
1. **Procesamiento de datos**  
2. **Almacenamiento de datos**  
3. **Transferencia de datos**  
4. **Control**  

## ¿Qué es una CPU y para qué sirve?
La **Unidad Central de Proceso** es el componente principal de una computadora.  
Su función es ejecutar programas almacenados en la memoria, captando y ejecutando instrucciones secuencialmente.

### ¿Cuáles son los objetivos de la CPU?
1. Captar instrucciones  
2. Interpretar instrucciones  
3. Captar datos  
4. Procesar datos  
5. Escribir datos  

## ¿Qué es una memoria principal y para qué sirve?
La memoria principal almacena temporalmente los datos y programas que la CPU procesa. Está directamente conectada con el procesador mediante el bus de datos y de direcciones.

### Primer CPU en un chip
1971: Intel 4004.

### ¿Qué es un microprocesador y para qué sirve?
El microprocesador es un **circuito integrado** que ejecuta programas con **instrucciones de bajo nivel**.

### ¿Dónde va el microprocesador?
Se coloca en un **zócalo** o está soldado a la **motherboard**.

### ¿Qué tipos de velocidades tienen los micros?
1. **Velocidad interna**: Velocidad de procesamiento dentro del microprocesador.  
2. **Velocidad externa**: Velocidad de conexión con la motherboard.

## ¿Qué tipos de registros existen y para qué sirven?
1. **Registros dedicados**: Usados por el sistema, como el contador de programa (PC).  
2. **Registros de propósito general**: Almacenan direcciones o datos temporales.

## ¿Para qué sirve la ALU? ¿Cuáles son sus partes?
La **Unidad Aritmético-Lógica (ALU)** procesa las instrucciones mediante operaciones aritméticas y lógicas.  
1. **Unidad aritmética**  
2. **Unidad lógica**  

### ¿Cómo se abaratan costos de fabricación en el sector aritmético?
Usando un solo circuito sumador para realizar todas las operaciones.

## ¿Cuáles son las funciones específicas de la unidad de control?
1. Captar el código máquina  
2. Interpretar instrucciones  
3. Controlar la ejecución de instrucciones  
4. Resolver situaciones anómalas  
5. Atender interrupciones y comunicarse con periféricos  

## ¿Qué es un bus? Función, constitución, tipos y clases
Un **bus** es un camino de comunicación entre dispositivos. Puede ser de **datos**, **dirección** o **control**, permitiendo el acceso y uso compartido de recursos.

## Repertorio de instrucciones
### ¿Qué es un programa?
Un **programa** es un conjunto de instrucciones que el computador ejecuta secuencialmente para resolver un problema.

### ¿Qué es una instrucción?
Una **instrucción** es una orden específica para que el computador ejecute una operación.

#### Elementos y representación de las instrucciones
1. **Código de operación**: Indica al procesador qué operación realizar.
2. **Referencia a operandos**: Indica de dónde obtener los datos y dónde almacenar resultados.
3. **Referencia a la próxima instrucción**: Indica la siguiente instrucción a ejecutar.

### Tipos de instrucciones
1. **Procesamiento de datos**  
2. **Almacenamiento de datos**  
3. **Transferencia de datos**  
4. **Control**  

### Aspectos del diseño del repertorio de instrucciones
1. **Repertorio de operaciones**  
2. **Tipos de datos**  
3. **Formato de instrucciones**  
4. **Registros**  
5. **Modos de direccionamiento**  

### Modos de direccionamiento
1. **Inmediato**: El operando está presente en la instrucción.  
2. **Directo**: Referencia directa a la dirección del operando en memoria.  
3. **Indirecto**: La dirección del operando se encuentra en otra posición de memoria.  
4. **De registro**: El operando está en un registro.  
5. **Desplazamiento**: Combina direcciones para obtener la dirección del operando.  

#### Algoritmos, ventajas y desventajas de los modos de direccionamiento
| Modo               | Algoritmo   | Ventaja                 | Desventaja                    |
| ------------------ | ----------- | ----------------------- | ----------------------------- |
| Inmediato          | Operando=A  | No referencia a memoria | Operando limitado             |
| Directo            | EA=A        | Sencillo                | Espacio de dirección limitado |
| Indirecto          | EA=(A)      | Espacio grande          | Referencia múltiple           |
| Registro directo   | EA=R        | No referencia a memoria | Número limitado de registros  |
| Registro indirecto | EA=(R)      | Espacio grande          | Referencia extra a memoria    |
| Con desplazamiento | EA=A+(R)    | Flexible                | Complejo                      |
| Pila               | EA=Cabecera | No usa memoria          | Aplicaciones limitadas        |

## ¿Qué ciclos existen en el funcionamiento de la CPU?
1. **Ciclo de captación**  
2. **Ciclo de ejecución**  

### Ciclo de instrucción de la CPU
1. **Cálculo de la dirección de la instrucción**  
2. **Captación de instrucción**  
3. **Decodificación de la operación**  
4. **Cálculo de la dirección del operando**  
5. **Captación de operando**  
6. **Operación con los datos**  
7. **Almacenamiento de operando**  
 