## ¿Cómo se analiza una computadora?
- Al ser un sistema complejo, por medio de una organización jerárquica

## ¿Qué es la estructura?
Es el modo en que los componentes están interrelacionados.

### Componentes estructurales de una computadora
1. CPU  
2. Memoria principal  
3. E/S  
4. Sistema de interconexión  

### Componentes estructurales de una UCP
1. Unidad de control  
2. Unidad aritmético-lógica  
3. Registros  
4. Interconexiones  

## ¿Qué es el funcionamiento?
La operación de cada componente individual como parte de la estructura.

### Funciones básicas de una computadora
1. Procesamiento de datos  
2. Almacenamiento de datos  
3. Transferencia de datos  
4. Control  

## ¿Qué es una CPU y para qué sirve?
- Componente principal  
- Ejecuta programas de la memoria. Busca instrucciones, las examina y las ejecuta  

### ¿Cuáles son los objetivos de la CPU?
1. Captar instrucciones  
2. Interpretar instrucciones  
3. Captar datos  
4. Procesar datos  
5. Escribir datos  

## ¿Qué es una memoria principal y para qué sirve?
Es un lugar donde se almacenan datos y programas de la CPU temporalmente. Es inseparable del CPU  

## ¿Primer CPU en un chip?
1971 Intel 4004  

### ¿Qué es un microprocesador y para qué sirve?
- Circuito integrado central  
- Ejecuta los programas con instrucciones de bajo nivel  

### ¿Dónde va el microprocesador?
- En un zócalo (socket) o soldado en la motherboard  

### ¿Qué tipos de velocidades tienen los micros?
1. Interna (Procesamiento interno)  
2. Externa (Velocidad de conexión)  

## ¿Qué tipos de registros existen y para qué sirven?
1. Dedicados  
   1. Uso del sistema  
2. Propósito general  
   1. Almacenar direcciones o datos (Programador)  

## ¿Para qué sirve la ALU? ¿Cuáles son sus partes?
- Procesa las instrucciones del procesador de forma diádica (dos operandos)  
1. Unidad aritmética  
2. Unidad lógica  

### ¿Cómo se abaratan costos de fabricación en el sector aritmético?
Usando solo un circuito sumador  

## ¿Cuáles son las funciones específicas de la unidad de control?
1. Recibir el código máquina  
2. Interpretar las instrucciones  
3. Controlar la ejecución de instrucciones  
4. Resolver situaciones anómalas  
5. Atender interrupciones y comunicación con periféricos  

## Bus. Función, constitución, tipos y clases.
- Camino de comunicación entre dos o más dispositivos, entre partes de la UCP o entre la UCP y periféricos  
- Caminos de comunicación con señales binarias  
- El bus que conecta los **elementos principales se denomina bus del sistema**  
- Clases:  
   1. Datos  
   2. Dirección  
   3. Control  
      1. Controla el acceso y uso de las líneas de datos  

## Repertorio de instrucciones
### ¿Qué es un programa?
Conjunto de instrucciones con secuencia y lenguaje, interpretado por el computador para resolver un problema  

### ¿Qué es una instrucción?
Orden para que se ejecute una operación  

#### Elementos y representación de las instrucciones
##### Código de operación
Indica al micro con binario cuál es la operación  

##### Referencia a operandos fuente u origen, operando de destino o resultado
Indica al micro con binario dónde buscar los datos y dónde guardar resultados  

##### Referencia a la próxima instrucción
Indica al micro dónde está la próxima instrucción  

### Tipos de instrucciones
1. Procesamiento de datos  
   1. Aritméticas y lógicas  
2. Almacenamiento de datos  
3. Transferencia de datos  
4. Control  
   1. Comprobación y bifurcación  

### Aspectos del diseño del repertorio de instrucciones
1. Repertorio de operaciones  
2. Tipos de datos  
3. Formato de instrucciones  
4. Registros  
5. Direccionamiento  

#### Modos de direccionamiento
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
1. Ciclo de captación  
2. Ciclo de ejecución  

### Ciclo de instrucción de la CPU
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
6. Operación con los datos  
   1. Realiza la operación  
7. Almacenamiento de operando  
   1. Escribe el resultado en memoria o lo saca a través de un dispositivo de E/S  
