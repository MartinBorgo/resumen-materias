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


##### Temporizador

##### Gestión de procesos

##### Gestión de memoria

##### Gestión de almacenamiento

##### Protección y seguridad

##### Sistemas distribuidos

##### Sistemas embebidos en tiempo real

##### Sistema cliente-servidor