- **man [comand]** -> muestra la documentación (páginas del manual) sobre el comando, archivo o función solicitada.
- **--help** -> Es una opción que tienen todos los comandos, la cual muestra un mensaje por pantalla sobre el modo de empleo del comando.
- **whatis** -> muestra un breve mensaje por pantalla sobre el propósito del comando.
- **ls** -> muestra el listado de archivos y directorios.
- **pwd** -> muestra el directorio sobre el que se está actualmente.
- **cd [path]** -> cambia de directorio.
- **mkdir** -> crea un directorio.
- **rmdir** -> elimina un directorio, siempre y cuando este esté vacío.
- **cat, more, less** -> nos permiten visualizar por consola el contenido de un archivo.
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

- **ps** -> obtiene un listado y estadísticas de los procesos activos. Si a este comando le agregamos la opción ***-aux*** se mostrarán todos los procesos activos de todos los usuarios.
- **kill** -> solicita a un proceso que finalice su ejecución o lo mata.
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

## Scripts y Scripting

Un Script es un archivo de texto que contiene una secuencia de comandos, los cuales serán ejecutados ordenadamente. Son muy útiles para procesamiento por lotes, automatizar tareas, atajos a comandos complejos, generalización de operaciones. 