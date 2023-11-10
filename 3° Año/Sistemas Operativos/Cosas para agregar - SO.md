
**Lo que tengo de memoria**
Sobre memoria, al realizar la asignación se hacen varias preguntas.
¿Hay espacio?, en caso de que no haya, mata algún proceso o manda a la memoria viartual. Si hay espacio se pregunta ¿Hay suficiente?, dependiendo si es segmentación o paginación se hace algo diferente. En segmentación, donde el tamaño es variable, tiene que hacer hueco para que entre. Con paginación usa marcos, espacios iguales, entonces se pregunta ¿Hay marcos suficientes?

Sobre el código compartido, se pregunta si nadie lo usa, si es así cierra y actualiza en disco.

El DMA accede directo a memoria, además cada disco tiene su propio DMA.

Las particiones dinámicas no tienen fragmentación interna, pero produce fragmentación externa. En paginación hay fragmentación interna. En los dos casos se genera desperdicio.

La fragmentación interna no se puede solucionar
La fragmentación externa se soluciona con la compactación (solamente se puede unir con el adyacente, tengo entendido)

Sobre el sistema de los asociados
Básicamente es un gran hueco que se va dividiendo hasta que tenga el menor desperdicio, las divisiones se las conoce como socios.
El SO se hace dos preguntas:
1. ¿Entro?
2. ¿Se puede seguir dividiendo?

Con la segmentación paginada, el ciclo de vida del proceso es más corto y se mantiene la multiprogramación.

Hiperpaginacion = Thrashing

**Siguiendo con memoria**
Sobre el código compartido se pregunta si nadie lo usa, cierra y actualiza en disco.

Dos discos no pueden usar el mismo espacio en memoria, pasa lo mismo en RAID.

Marco = tamaño de la página (porque son de tamaño fijo)

La memoria caché tiene más colisiones por ser más pequeña en tamaño

**Entrada/Salida**
Para que un proceso use un E/S este tiene que estar liberado, sino se produce un interbloqueo

En la tabla de archivos abiertos, si se usa y se termina, se tiene que actualizar al discos los datos.

Según lo que tengo anotado la imagen de principios de software de E/S es importante toca ver los videos de Berón

Abajo del driver está el controlador, ejemplo debajo del driver del disco sólido está el controlador del disco sólido, los controladores son hardware.

Los relojes tienen problemas con los SO distribuidos

Buffer sencillo -> entra y sale, una a la vez
Buffer doble (puede ser cuádruple) dos entradas y dos salidas
Buffer circular entra y sale desde el mismo buffer, cuando es lento el productor pregunta ¿hay espacio? Y el consumidor ¿hay algún carácter?

¿Qué diferencias hay entre la caché y buffer? <- tengo anotada esta pregunta xd

El SO solo reconoce bloques

Menos discos, hay más competencia para su uso.

**Archivos**
Se tienen que respetar las reglas del SO sobre los archivos

Con la extensión, se pregunta ¿hay algún programa compatible? Y muestra que programa puede abrirlo

Directorio = carpeta

Cabecera = i-nodo

El SO se abstrae de la estructura física, crea archivos

El almacenamiento es persistente y confiable, con confiable nos referimos a que se grabó y esto sea lo mismo que se lee

Sistema de nombres lógicos -> Para el usuario, no del SO

Si se abre y cierra, se modifica el archivo, se modifica quien accedió al archivo

El nombre lógico está guardado en el directorio, no en el encabezado. El directorio tiene un número de cabecera y nombre del directorio, este último sirve para ir al número de cabecera.

**Tengo anotado que las capas del sistemas de archivos es importante, es la diapositiva 9**

Un bloque tiene 1 o más sectores

¿Qué es un vínculo? Básicamente que podés acceder desde 2 puertas, un ejemplo de esto son los accesos directos de Windows

El borrado lógico, pero no físico, es como ocultar

**Esta parte es sobre las operaciones sobre archivos**

Si se abren dos archivos iguales, se incrementa el contador de la tabla general de archivos abiertos, recordemos el código compartido.

Si es lectura no va a haber interbloqueo, en lectura/escritura si

La búsqueda de archivos debe ser acotada (expresiones regulares, extensiones, etc. beneficia al acotamiento)

El borrado es lógico, la cabecera no se borra y se puede reasignar para otro archivo

El truncar varía cabecera (la ruta ejemplo), el nombre lógico no

El renombrar, modifica el directorio (registros -> links, carpetas, etc)

Cerrar cambia la tabla general de archivo, si hubo cambio en el archivo para grabar en disco.

**Superbloque importante**

Desfragmentación
No se mueve memoria virtual ni tabla de particiones, se necesita espacio porque hace copia y pega