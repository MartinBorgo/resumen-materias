#### **Introducción**
Un sistema operativo es un programa que administra el hardware de una computadora. También proporciona las bases para los programas de aplicación y actúa como intermediario entre el usuario y el hardware de la computadora.
El SO controla y coordina el uso del hardware entre los diversos programas de aplicación por parte de los distintos usuarios, el objeto de un SO es proporcionar un entorno en el que el usuario pueda ejecutar programas de manera práctica y eficiente. El SO gestiona el hardware, el hardware debe proporcionar los mecanismos apropiados para asegurar el correcto funcionamiento del sistema informático e impedir que los programas de usuario interfieran con el apropiado funcionamiento del sistema.

Un SO es similar a un gobierno. Como un gobierno, no realiza ninguna función útil por sí mismo: simplemente proporciona un entorno en el que otros programas pueden llevar a cabo un trabajo útil.

El SO es el programa más íntimamente relacionado con el HW (Hardware). Podemos ver un SO como un **asignador de recursos**. Un sistema informático tiene muchos recursos que puedan ser necesarios para solucionar un problema: tiempo de CPU, espacio de memoria, espacio de almacenamiento de archivos, dispositivos de E/S, etc. El SO actúa como el administrador de estos recursos. Al enfrentarse a numerosas y posiblemente conflictivas solicitudes de recursos, el SO debe decidir como asignarlo a programas y usuarios específicos, de modo que la computadora pueda operar de forma eficiente y equitativa.
Un punto de vista ligeramente diferente de un SO es de un programa de control. Como programa de control, gestiona la ejecución de los programas de usuario para evitar errores y mejorar el uso de la computadora. Tiene que ver especialmente con el funcionamiento y control de los dispositivos de E/S.

##### Arranque del sistema
Para que una computadora comience a funcionar, por ejemplo cuando se enciende o se reinicia, es necesario que tenga un programa de inicio que ejecutar. Este programa de inicio, o programa de arranque, suele ser simple. Normalmente, se almacena en una memoria ROM o EEPROM y se conoce con el término general de **firmware**, dentro del hardware de la computadora. Se inicializan todos los aspectos del sistema, desde los registros de la CPU hasta las controladoras de dispositivos y el contenido de la memoria. El programa de arranque debe saber como cargar el SO e iniciar la ejecución de dicho sistema. Para conseguir este objetivo, el programa de arranque debe localizar y cargar en memoria el kernel (el núcleo) del SO. Después, el SO comienza ejecutando el primer proceso, como por ejemplo "init", y espera que produzca algún suceso. La ocurrencia de un suceso normalmente se indica mediante una interrupción bien del HW o de SW (software). El HW puede activar una interrupción en cualquier instante enviando una señal a la CPU, normalmente a través del bus del sistema. El SW puede activar una interrupción ejecutando una operación especial denominada **llamada del sistema** (o llamada de monitor). Se puede seguir especificando el arranque, pero hasta acá está bien.

##### Modo usuario y modo kernel (supervisor)
Para asegurar la correcta ejecución del SO, tenemos que poder distinguir entre la ejecución del código del sistema operativo y del código definido por el usuario. El método que usan la mayoría de los sistemas informáticos consiste en proporcionar soporte HW que nos permita diferencia entre varios modos de ejecución. Como mínimo, necesitamos dos modos diferentes de operación: **modo usuario** y **modo kernel** (también conocido como modo supervisor, modo del sistema o modo privilegiado). Un bit denominado **bit de modo** se añade al HW de la computadora para indicar el modo actual kernel (0) y usuario (1).
Cuando el sistema está ejecutando una aplicación de usuario, se encuentra en modo usuario. Sin embargo, cuando una aplicación solicita un servicio del sistema operativo (a través de una llamada al sistema), debe pasar del modo de usuario al modo *kernel* para satisfacer la solicitud. Cuando se arranca el SO, el HW se inicia en modo kernel. El SO se carga y se inician las aplicaciones de usuario en el modo usuario. Cuando se produce una excepción (son de SW) o interrupción (HW), el HW conmuta del modo usuario a modo kernel.

El modo dual (usuario - kernel) nos proporciona medios para proteger el SO de los usuarios que puedan causar errores, y también proteger a los usuarios de los errores de otros usuarios. Esta protección se consigue designando algunas de las instrucciones de máquina que pueden causar daño como **instrucciones privilegiadas**. Estas solo se ejecutan en modo *kernel*, si se trata de ejecutar en modo usuario la trata de ilegal y envía una excepción al SO.


##### Temporizador (Quantum)
Debemos asegurar que el SO mantenga el control sobre la CPU. Por ejemplo, debemos impedir que un programa de usuario entre en un bucle infinito o que no llame a los servicios del sistema y nunca devuelva el control al SO. Para alcanzar este objetivo, podemos usar un **temporizador**. Puede configurarse un temporizador para interrumpir a la computadora después de un periodo especificado. El periodo puede ser fijo o variable. Generalmente, se implementa un **temporizador variable** mediante un reloj de frecuencia fija y un contador. Antes de devolver el control al usuario, el SO se asegura de que el temporizador esté configurado para realizar interrupciones. Cuando el temporizador interrumpe, el control se transfiere automáticamente al SO, que puede tratar la interrupción como un error fatal o puede conceder más tiempo al programa. Evidentemente, las instrucciones que modifican el contenido del temporizador son instrucciones privilegiadas. Por tanto, podemos usar el temporizador para impedir que un programa de usuario se esté ejecutando durante un tiempo excesivo.

##### Gestión de procesos
Un programa no hace nada a menos que una CPU ejecute sus instrucciones. Un programa en ejecución, es un proceso. Un programa de usuario de tiempo compartido, como por ejemplo un compilador, es un proceso. Por el momento vamos a considerar que un proceso es un trabajo o un programa en tiempo compartido, aunque, es posible proporcionar llamadas al sistema que permitan a los procesos crear subprocesos que se ejecuten de forma concurrente.
Un proceso necesita para llevar a cabo su tarea ciertos recursos, entre los que incluyen tiempo de CPU, memoria, archivos y dispositivos de E/S. Estos recursos se proporcionan al proceso en el momento de crearlo o se le asignan mientras se está ejecutando. Además de los diversos recursos físicos y lógicos que un proceso obtiene en el momento de su creación, pueden pasársele diversos datos de inicialización (entradas).
Algo importante es que un programa por si solo no es un proceso; un programa es una entidad *pasiva*, tal como los contenidos de un archivo almacenado en disco, mientras que un proceso es una entidad activa. Un proceso de una sola hebra tiene un **contador de programa** que especifica la siguiente instruccion que hay que ejecutar. La ejecución de un proceso así debe ser secuencial: la CPU ejecuta una instrucción del proceso después de otra, hasta completarlo. Además, en cualquier instante, se estará ejecutando como mucho una instancia en nombre del proceso. Por tanto, puede haber dos procesos asociados con el mismo programa, se considerarían no obstante como dos secuencias de ejecución separadas. Un proceso multihebra que haya que ejecutar para una hebra determinada. Un proceso es una unidad de trabajo en un sistema. Cada sistema consta de una colección de procesos, siendo algunos de ellos procesos del SO (ejecutan código del sistema) y el resto procesos de usuario (ejecutan código del usuario). Todos estos (potencialmente) pueden ejecutarse de forma concurrente.

El SO es el encargado de las siguientes actividades en la gestión de procesos:
-Crear y borrar los procesos de usuario y del sistema.
-Suspender y reanudar los procesos.
-Proporcionar mecanismos para la sincronización de procesos.
-Proporcionar mecanismos para la comunicación entre procesos.
-Proporcionar mecanismos para el tratamiento de los interbloqueos.

##### Gestión de memoria
Para que un programa pueda ejecutarse, debe estar asignado a direcciones absolutas y cargado en memoria. Mientras el programa se está ejecutando, accede a las instrucciones y a los datos de la memoria generando dichos direcciones absolutas. Finalmente, el programa termina, su espacio de memoria se declara disponible y el siguiente programa puede ser cargado y ejecutado. Para mejorar tanto la utilización de la CPU como la velocidad de respuesta de la computadora frente a los usuarios, las computadoras de propósito general pueden mantener varios programas en memoria, lo que crea la necesidad de mecanismos (esquemas) de gestión de la memoria. Estos esquemas utilizan enfoques distintos y la efectividad de cualquier algoritmo dado depende de la situación. En la selección de un esquema de gestión de memoria para un sistema específico, debemos tener en cuenta muchos factores, especialmente relativos al diseño *hardware* del sistema. Cada algoritmo requiere su propio soporte HW.

El SO es el encargado de las siguientes actividades en la gestión de memoria:
-Controlar que partes de la memoria están actualmente en uso y por parte de quien.
-Decidir que datos y procesos (o partes de procesos) añadir o extraer de la memoria.
-Asignar y liberar la asignación de espacio de memoria según sea necesario.


##### Gestión de almacenamiento
Para que el sistema informático sea cómodo para los usuarios, el SO proporciona una vista lógica y uniforme del sistema de almacenamiento de la información. El SO abstrae las propiedades físicas de los dispositivos de almacenamiento y define una unidad de almacenamiento lógico, el **archivo**. El SO asigna los archivos a los soportes físicos y accede a dichos archivos a través de los dispositivos de almacenamiento. Los archivos normalmente se organizan en directorios para hacer más fácil su uso. 

El SO es el encargado de las siguientes actividades en la gestión de archivos:
-Creación y borrado de archivos.
-Creación y borrado de directorios para organizar los archivos.
-Soporte de primitivas para manipular archivos y directorios.
-Asignación de archivos a los dispositivos de almacenamiento secundario.
Copia de seguridad de los archivos en medios de almacenamiento estables (no volátiles).

---

#### Procesos
Un proceso es la unidad de trabajo (un programa en ejecución) en los sistemas modernos de tiempo compartido, mientras más complejo el SO, más se espera que haga en nombre de sus usuarios. Aunque su objetivo principal es la ejecución de programas de usuario, también tiene que ocuparse de diversas tareas del sistema, que no están incluidas dentro del kernel. Por tanto, un sistema está formado por una colección de procesos: procesos del SO que ejecutan código del sistema y procesos de usuario que ejecutan código de usuario.

Hay que resaltar que un proceso es algo más que el código de un programa (al que en ocasiones se denomina **sección de texto**) Además del código, un proceso incluye también la actividad actual, que queda representada por el valor del **contador de programa** y por los contenidos de los registros del procesador. Generalmente, un proceso incluye también la **pila** del proceso, que contiene datos temporales (parámetros de las funciones, las direcciones de retorno y las variables locales), y una **sección de datos**, que contiene las variables globales. El proceso puede incluir, asimismo, un **cúmulo de memoria,** que es la memoria que se asigna dinámicamente al proceso en tiempo de ejecución. Insistimos que un programa, por sí mismo, no es proceso; un programa es una unidad pasiva, un archivo que contiene una lista de instrucciones almacenadas en disco (a menudo denominado **archivo ejecutable**), mientras que un proceso es una entidad activa, con un contador de programa que especifica la siguiente instruccion que hay que ejecutar y un conjunto de recursos asociados. Un programa se convierte en un proceso cuando se carga en memoria un archivo ejecutable. Aunque puede haber dos procesos asociados con el mismo programa, esos procesos se consideran dos secuencias de ejecución separadas. 

Por ejemplo, varios usuarios pueden estar ejecutando copias diferentes del programa de correo, o el mismo usuario puede invocar muchas copias del explorador web. Cada copia es un proceso distinto y, aunque las secciones de texto (código del programa) sean equivalentes, las secciones de datos, del cúmulo (*heap*) de memoria y de la pila variaran de unos procesos a otros. También es habitual que un proceso cree muchos otros procesos a medida que se ejecuta.

##### Estado del proceso
A medida que se ejecuta un proceso, el proceso va cambiando de **estado**. El estado de un proceso se define, en parte, según la actividad actual de dicho proceso. Cada proceso puede estar en uno de los siguientes estados:
- **Nuevo.** El proceso está siendo creado.
- **En ejecución.** Se están ejecutando las instrucciones
- **En espera.** El proceso está esperando a que se produzca un suceso (como la terminación de una operación de E/S o la recepción de una señal)
- **Preparado.** El proceso está a la espera de que le asignen a un procesador.
- **Terminado.** Ha terminado la ejecución del proceso.

Es importante darse cuenta de que solo puede haber un proceso *ejecutándose* en cualquier procesador en cada instante concreto. Sin embargo, puede haber muchos procesos *preparados* y en *espera*.

##### Bloque de control de proceso
Cada proceso se representa en el SO mediante un **bloque de control de proceso** (PCB, process control block), también denominado *bloque de control de tarea*. Un bloque de control de proceso contiene muchos elementos de información asociados con un proceso específico, entre los que se incluyen.
- **Estado del proceso.**
- **Contador de programa.**
- **Registros de la CPU.**
- **Información de planificación de la CPU**
- **Información de gestión de memoria**
- **Información contable.**
- **Información del estado de E/S.**

##### Cambio de contexto

#### Operaciones sobre los procesos
##### Creación de procesos
##### Terminación de procesos
