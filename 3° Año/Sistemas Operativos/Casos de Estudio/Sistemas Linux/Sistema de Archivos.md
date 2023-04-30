El sistema de archivos de los sistemas operativos Linux, es un sistema jerárquico, es decir, la información no se va a encontrar distribuida al azar, sino que cada directorio del sistema contara y almacenara información específica.
Se lo puede considerar como un árbol o grafo, si es que este cuenta con enlaces ente los diferentes directorios.
En los sistemas Linux todos está representado por archivos, por eso van a existir archivos que estén representando a procesos, a dispositivos, y incluso a información del kernel.

>[!important] Los I-nodos
>Su nombre completo **nodos de identificación en el superbloque**, es una estructura especial que es la base del sistema de archivos, contiene toda la información relativa a los archivos (metadata) a excepción de su nombre. 
>
><span class="centerImg"> ![[SO-inodo.png]] </span>

>[!info] Distribución de los Programas en Linux
>A diferencia de otros SO como Windows, en el cual cuando instalamos una aplicación todo se ubica en una única carpeta, en Linux esto no es tan así. Ya que cada archivo va a tener su ubicación en un directorio específico en el sistema de archivos.
>Por ejemplo, si nosotros instalamos una aplicación, los archivos ejecutables estarán en un directorio, la documentación estarán en otra distinta, y los archivos de configuración a su vez en su directorio correspondiente. A continuación enumeraremos algunos directorios y que es lo que guardan en cada uno de ellos:
>
>- **/bin**: Esta carpeta contiene todos los binarios que van a utilizar el sistema.
>- **/sbin**: En esta carpeta contiene todos los binarios que utiliza el sistema para la administración (los que utiliza el usuario root).
>- **/boot**: Se encuentran los archivos que participan en el arranque del sistema, con el kernel y los archivos de configuración del gestor de arranque.
>- **/dev**: Se encuentran los archivos que representan a los dispositivos físicos y lógicos que estén instalados a la máquina.
>- **/etc**: Contienen los archivos de configuración del sistema.
>- **/home**: Se localiza toda la información de los usuarios comunes. Dentro de este directorio, existirá un directorio con más información para cada usuario creado en el sistema
>- **/root**: es como el directorio *home*, pero es único del usuario ***root***.
>- **/lib**: Se encuentran las librerías compartidas entre las aplicaciones y los módulos del kernel.
>- **/mnt & /media**: Se localizan los puntos de montaje de los otros sistemas de archivos.
>- **/opt**: Todos los otros programas de terceros que no siguen las convenciones de GNU/Linux.
>- **/proc**: Aquí se encuentran los archivos que guardan información de los procesos en ejecución. Estos archivos es virtual, ya que se guarda en memoria principal, no en el disco externo.
>- **/srv**: Todos los archivos de servidores que se tengan instalados en el sistema. Por Ej.: Los servidores de bases de datos o servidores web que se tenga en la máquina.
>- **/sys**: Es un archivo virtual que guarda información del kernel.
>- **/usr (user system resources)**: Almacena las utilidades del usuario. Replica una estructura siminalar "/".
>- **/var**: Los archivos que suelen crecer en tamaño. Por Ej.: archivos del sistema, base de datos, cache,etc.
