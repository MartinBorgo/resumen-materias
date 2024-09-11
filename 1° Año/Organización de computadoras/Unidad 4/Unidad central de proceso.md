# Anki
TARGET DECK: Facultad:: Sistemas:: Primer año:: Organización de computadoras:: Unidad 4
# Archivos
![[Unidad 4.pdf]]
# Trabajo práctico
![[Tp04.docx]]
#  Notas

## ¿Cómo se analiza una computadora? #flashcard
- Al ser un sistema complejo, por medio de una organización jerárquica
<!--ID: 1700156773564-->


## ¿Qué es la estructura? #flashcard
Es el modo en que los componentes están interrelacionados. 
<!--ID: 1700156773572-->


### Componentes estructurales de una computadora #flashcard
1. CPU
2. Memoria principal
3. E/S
4. Sistema de interconexión
<!--ID: 1700156773577-->


### Componentes estructurales de una UCP #flashcard
1. Unidad de control
2. Unidad aritmético-lógica
3. Registros
4. Interconexiones
<!--ID: 1700156773582-->


## ¿Qué es el funcionamiento? #flashcard
La operación de cada componente individual como parte de la estructura.
<!--ID: 1700156773591-->


### Funciones básicas de una computadora #flashcard
1. Procesamiento de datos
2. Almacenamiento de datos
3. Transferencia de datos
4. Control
<!--ID: 1700156773596-->


## ¿Qué es una CPU y para qué sirve? #flashcard
- Componente principal
- Ejecuta programas de la memoria. Busca instrucciones, las examina y las ejecuta
<!--ID: 1700156773600-->


### ¿Cuáles son los objetivos de la CPU? #flashcard
1. Captar instrucciones
2. Interpretar instrucciones
3. Captar datos
4. Procesar datos
5. Escribir datos
<!--ID: 1700156773606-->


## ¿Qué es una memoria principal y para qué sirve? #flashcard
Es un lugar donde se almacenan datos y programas de la CPU temporalmente. Es inseparable del CPU
<!--ID: 1700156773610-->


## ¿Primer CPU en un chip? #flashcard
1971 Intel 4004
<!--ID: 1700156773614-->


### ¿Qué es un microprocesador y para qué sirve? #flashcard
- Circuito integrado central
- Ejecuta los programas con instrucciones de bajo nivel
<!--ID: 1700156773620-->


### ¿Dónde va el microprocesador? #flashcard
- En un zócalo (socket) o soldado en la motherboard
<!--ID: 1700156773633-->


### ¿Qué tipos de velocidades tienen los micros? #flashcard
1. Interna (Procesamiento interno)
2. Externa (Velocidad de conexión)
<!--ID: 1700156773657-->


## ¿Cómo sería un esquema simplificado de CPU? #flashcard
![[Esquema simplificado de CPU.png]]
<!--ID: 1700156773661-->



## ¿Qué tipos de registros existen y para qué sirven? #flashcard
1. Dedicados
	1. Uso del sistema
2. Propósito general
	1.  Almacenar direcciones o datos (Programador)
<!--ID: 1700156773666-->



## ¿Para qué sirve la ALU? ¿Cuáles son sus partes? #flashcard
- Procesa las instrucciones del procesador de forma diádica (dos operandos)
1. Unidad aritmética
2. Unidad lógica
<!--ID: 1700156773671-->



### ¿Cómo se abaratan costos de fabricación en el sector aritmético? #flashcard
Usando solo un circuito sumado
<!--ID: 1700156773675-->


## ¿Cuáles son las funciones específicas de la unidad de control? #flashcard
1. Recibir el código máquina
2. Interpretar las instrucciones
3. Controlar la ejecución de instrucciones
4. Resolver situaciones anómalas
5. Atender interrupciones y comunicación con periféricos
<!--ID: 1700156773679-->



## ¿Cuáles son los pasos en la actuación de la unidad de control? #flashcard
1. Recibir código máquina por el **contador de programa
2. Cargar el código en el **Registro de instrucciones**. Ejecución en operaciones elementales. Se guardan las operaciones como información binaria en la **memoria de control**. El **decodificador de instrucciones** selecciona las operaciones elementales para la ejecución. 
3. El **secuenciador** se encarga de la E/S
<!--ID: 1700156773683-->


## Bus. Función, constitución, tipos y clases. #flashcard
- Camino de comunicación entre dos o más dispositivos, entre partes de la UCP o entre la UCP y periféricos
- Caminos de comunicación con señales binarias
- El bus que conecta los **elementos principales se denomina bus del sistema**
- Clases:
1. Datos
2. Dirección
3. Control
	1. Controla el acceso y uso de las líneas de datos
<!--ID: 1700156773690-->


## Repertorio de instrucciones
### ¿Qué es un programa? #flashcard
Conjunto de instrucciones con secuencia y lenguaje, interpretado por el computador para resolver un problema
 
<!--ID: 1700156773695-->



### ¿Qué es una instrucción? #flashcard
Orden para que se ejecute una operación
 
<!--ID: 1700156773699-->



#### Elementos y representación de las instrucciones
##### Código de operación #flashcard
Indica al micro con binario cuál es la operación
 
<!--ID: 1700156773705-->



##### Referencia a operandos fuente u origen, operando de destino o resultado #flashcard
Indica al micro con binario donde buscar los datos y donde guardar resultados
 
<!--ID: 1700156773709-->



##### Referencia a la próxima instrucción #flashcard
Indica al micro donde está la próxima instrucción
 
<!--ID: 1700156773713-->



## Repertorio de instrucciones
### Tipos de instrucciones #flashcard
1. Procesamiento de datos
	1. Aritméticas y lógicas
2. Almacenamiento de datos
3. Transferencia de datos
4. Control
	1. Comprobación y bifurcación
 
<!--ID: 1700156773717-->



### Aspectos del diseño del repertorio de instrucciones #flashcard
1. Repertorio de operaciones
2. Tipos de datos
3. Formato de instrucciones
4. Registros
5. Direccionamiento
 
<!--ID: 1700156773722-->



#### Consideraciones del formato de instrucciones #flashcard
1. Longitud
2. Bits asignados al código de operación y a cada operando
3. Forma de determinar el modo de direccionamiento
 
<!--ID: 1700156773727-->



#### Modos de direccionamiento #flashcard
1. Inmediato
	1. Operando presente en la instrucción (Magnitud limitada)
2. De memoria
	1. Directo
		1. Referencia a memoria del operando
	2. Indirecto
		1. Se referencia una palabra en la memoria donde está la dirección completa del operando
3. De registros
	1. Directo
		1. Referencia a registro del operando
	2. Indirecto
		1. Se referencia una palabra en el registro donde está la dirección completa del operando
4. Desplazamiento
	- Dos campos de direcciones con al menos uno explícito.
	1. Relativo
		1. Contador de programa
	2. Registro base
		1. Del registro a la memoria
	3. Indexado
		1. Referencia la memoria principal donde está referenciado por el registro
5. De pila
	1. Elementos en la cabecera de la pila. Puntero asociado mantenido en un registro
 
<!--ID: 1700156773732-->



#### Algoritmos, ventajas y desventajas de los modos de direccionamiento #flashcard
| Modo               | Alogritmo   | Ventaja                 | Desventaja                    |
| ------------------ | ----------- | ----------------------- | ----------------------------- |
| Inmediato          | Operando=A  | No referencia a memoria | Operando limitado             |
| Directo            | EA=A        | Sencillo                | Espacio de dirección limitado |
| Indirecto          | EA=(A)      | Espacio grande          | Referencia múltiple           |
| Registro directo   | EA=R        | No referencia a memoria | Número limitado de registros  |
| Registro indirecto | EA=(R)      | Espacio grande          | Referencia extra a memoria    |
| Con desplazamiento | EA=A+(R)    | Flexible                | Complejo                      |
| Pila               | EA=Cabecera | No usa memoria          | Aplicaciones limitadas        |
 
<!--ID: 1700156773737-->



## ¿Qué ciclos existen en el funcionamiento de la CPU? #flashcard
1. Ciclo de captación
2. Ciclo de ejecución
 
<!--ID: 1700156773742-->



### Ciclo de instrucción de la CPU #flashcard
1. Cálculo de la dirección de la instrucción
	1. Determina la dirección de la siguiente instrucción a ejecutar 
2. Captación de instrucción
	1. La CPU lee la instrucción desde su posición de memoria 
3. Decodificación de la operación indicada en la instrucción
	1. Analiza la instrucción para determinar la operación a realizar y los operandos a utilizar 
4. Cálculo de la dirección del operando
	1. Determina la dirección del operando (si está en memoria o disponible mediante E/S) 
5. Captación de operando
	1. Capta el operando desde memoria o se lee desde el dispositivo de E/S 
6. Operación con los datos: 
	1. Realiza la operación 
7. Almacenamiento de operando 
	1. Escribe el resultado en memoria o lo saca a través de un dispositivo de E/S
 
<!--ID: 1700156773746-->

