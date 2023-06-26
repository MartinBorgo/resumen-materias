## Comandos Fundamentales
- **man [comand]** -> muestra la documentación (páginas del manual) sobre el comando, archivo o función solicitada.
- **--help** -> Es una opción que tienen todos los comandos, la cual muestra un mensaje por pantalla sobre el modo de empleo del comando.
- **whatis** -> muestra un breve mensaje por pantalla sobre el propósito del comando.
- **ls** -> muestra el listado de archivos y directorios.
- **pwd** -> muestra el directorio sobre el que se está actualmente.
- **cd [path]** -> cambia de directorio.
- **mkdir** -> crea un directorio.
- **rmdir** -> elimina un directorio, siempre y cuando este esté vacío.
- **cat, more, less** -> nos permiten visualizar por consola el contenido de un archivo.
	- cat se usa para concatenar el contenido de dos o mas archivos y que te lo mostrara por consola.
	- more te muestra el archivo completo en consola.
	- less te lista los archivos en formato página, es decir, te muestra solo una parte del archivo, y vos podes ir navegando a la siguiente página usando las teclas correspondientes.
- **cp** -> copia uno o varios archivos o directorios a otro archivo o directorio.
- **mv** -> mueve un archivo o directorio a otro directorio, o también se puede usar para cambiar el nombre a los archivos.
- **rm** -> elimina un archivo o directorio si se le agrega unas opciones.
- **ln** -> crea un enlace entre archivos.
- **find** -> busca archivos siguiendo ciertos criterios.
- **nano** -> permite crear y editar archivos de texto.
- **clear** -> limpia la consola
- **echo** -> imprime un mensaje por consola
- **alias** -> define un pseudónimo para un comando que resulta difícil de recordar o largo de escribir.
- **shutdown** -> permite reiniciar, apagar o programar el apagado de la computadora. Es un comando que engloba un conjunto de comandos como por ejemplo el ***reboot***.

>[!note] Algunas Utilidades extras del Comando
>**sudo shutdown -r** -> reinicia la computadora.
>**sudo shutdown +10** -> va a apagar la computadora dentro de 10 minutos.
>**sudo shutdown 18:00** -> va a apagar la computadora a las 18 horas.
>
>En caso de que se necesite cancelar algún reinicio o apagado programado, se puede hacer usando el siguiente comando.
>
>sudo shutdown -c

- **ps** -> obtiene un listado y estadísticas de los procesos activos. Al igual que muchos otros comandos, el ps cuenta con una serie de argumentos que se le pueden pasar.
	- **a** muestra los procesos de todos los usuarios.
	- **x** muestra los procesos de todas las terminales.
	- **u** muestra la información en forma más amigable.

Claro esta que se pueden poner todos estos argumentos juntos, por ejemplo, **-aux**, o solo poniendo ***-ax***

>[!info] Información Mostrada en el Listado
>Cuando usamos el comando ***ps*** con el argumento **u**, se nos listara los procesos fila por fila, y poniendo en una serie de columnas una serie de información extra sobre el proceso correspondiente.
>- **USER**: Nombre de usuario que ejecuta el programa.
>- **PID**: Número encargado de identificar el proceso.
>- **%CPU**: Porcentaje total de tiempo de CPU que utiliza el proceso.
>- **%MEM**: Porcentaje de memoria utilizada por el proceso.
>- **VSZ**: Tamaño total del proceso en la memoria virtual, en KB.
>- **RSS** Cantidad de memoria utilizada por el proceso.
>- **TTY**: Terminal en la que se ejecuta el proceso.
>- **STAT**: Estado del proceso.
>- **START**: Indica la hora de ejecución. TIME Cantidad total de tiempo de CPU consumido.
>- **COMAND**: Comando utilizado para iniciar el proceso.
>
> En la columna ***STAT***, van a aparecer los estados en lo que se encuentra cada proceso representado a través de una letra, estas letras representarían lo siguiente:
> - **R (runnable)**: En ejecución, corriendo o ejecutándose.
> - **S (sleeping)**: Proceso en ejecución pero sin actividad por el momento, o esperando por algún evento para continuar.
> - **Z (zombie)**: Proceso que por alguna razón no terminó de manera correcta.
> - **T (stopped)**: Proceso detenido totalmente, pero puede ser reiniciado.
> - **D (uninterruptible sleep)**: Procesos generalmente asociados a acciones de E/S del Sistema.
> 
> #### Listar Procesos Específicos
> 
> El comando ***ps***, también te permite listar procesos de un determinado tipo usando el argumento **grep** seguido de una expresión regular, por ejemplo ps -ax | grep name*, lo cual me listara a todos los procesos que contengan en su descripción la palabra *name*.
> Existe un comando específico que sirve para mostrarte el PID dado un nombre de proceso determinado, este comando es el ***pgrep***, el cual se usa de la siguiente manera, ***pgrep firefox***, el cual listara el PID del proceso que esta corriendo firefox. 

- **kill** -> solicita a un proceso que finalice su ejecución o lo mata, en el caso de que el proceso no responda se puede llamar al SO para que finalice ese proceso, esa llamada se hace de la siguiente manera, ***kill -SIGKILL PID*** o simplemente ***kill -9 PID***. También se puede finalizar a los procesos por su nombre usando ***killall*** y el nombre del proceso, con la desventaja que finalizara todos los procesos que tengan ese nombre.
- **chmod** -> cambia el modo de los archivos que es el que controla los permisos de acceso asociados con ese archivo.

>[!note] Asignación de Permisos a Archivos y directorios
>Para un archivo
>- (r) Read: El archivo puede ser mostrado o copiado.
>- (w) Write: Se puede modificar el contenido del archivo.
>- (x) Execute: El archivo puede ser ejecutado.
>Para un directorio
>- (r) Read: Se puede listar el contenido del directorio.
>- (w) Write: Se puede agregar o borrar archivos de él.
>- (x) Execute: Control de acceso para el directorio.
>
>El comando ***chmod*** tiene diferentes opciones, las cuales le permiten cambiar los permisos a distintos grupos de usuarios.
> - **u** -> Corresponde al propietario, ‘user’.
> - **g** -> Corresponde al grupo, ‘group’.
> - **o** -> Corresponde al resto de los usuarios, ‘other’.
> - **a** -> Corresponde a todos los usuarios, ‘all’.
> - **+** -> Autoriza el permiso.
> - **-** -> Deniega el Permiso.

- **nice**: nos sirve para crear un proceso con una prioridad predefinida por el usuario, se usa de la siguiente manera, **nice -n -10 gedit**, en este estamos creando un proceso que ejecuta gedit con una prioridad (en este caso alta, ya que en Linux las prioridades más altas son las que tienen los números más bajos) de -10.
- **renice**: nos ayuda a cambiar la prioridad de un proceso ya existente, se utiliza de la siguiente manera, ***renice 0 3043***, en este caso le estamos cambiando la prioridad el proceso *3043* a 0, por defecto Linux solo te deja bajar la prioridad de los procesos, en caso de que se quiera subir la prioridad de un proceso se deberá usar ***sudo***.

>[!tldr] Gestión y Creación de Procesos en Segundo Plano
>Para iniciar un proceso en segundo plano debemos escribir ***&*** al final del nombre del programa que queramos lanzar. En caso de que queramos listar a todos los procesos que tenemos ejecutando en segundo plano, basta con ejecutar el comando ***jobs*** para que se listen todos. Y si se desea poner a algún proceso en primer plano, tendremos que introducir el comando ***fg %nmr_job***. 

---

## Scripts y Scripting

Un Script es un archivo de texto que contiene una secuencia de comandos, los cuales serán ejecutados ordenadamente. Son muy útiles para procesamiento por lotes, automatizar tareas, atajos a comandos complejos, generalización de operaciones. 