# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Algoritmos y programación:: Unidad 6
# Archivos
![[Archivos Directos.pdf]]
![[Archivos Secuenciales 2022.pdf]]
# Notas
## Archivo #flashcard
Estructura de datos que consiste en un conjunto de registros del mismo tipo y en número indeterminado
<!--ID: 1700071125468-->


### Archivos de acceso directo #flashcard
Contiene un archivo datos y uno de índices. Ambos tienen un campo de clave principal que no se repite en otros registros
<!--ID: 1700071125475-->


### Sintaxis de la lectura secuencial de todos los registros de archivos directos #flashcard
Leer ```<Nombre de archivo>```(campo clave) { Próximo o Anterior}
Próximo o anterior se usa para leer del final al inicio o del inicio al final
<!--ID: 1700071125481-->


#### Ejemplo de código de lectura secuencial #flashcard
Inicio
Assign (PROD, "Produc.dat")
Abrir ````````````<Nombre>````````````
PROD.Num := 999999
Leer ````````````<Nombre>```````````` (PROD.Num) Anterior
Mientras NOEOF `````````<Nombre>`````````
	Imprimir: PORD.Num, PORD.Des, PORD.Pre, PORD.Can
	Leer `````````<Nombre>````````` (PROD.Num) Anterior
FinMientras
Cerrar `````````<Nombre>`````````
FIN
<!--ID: 1700071125486-->


#### Ejemplo de código de eliminar un registro #flashcard
Inicio
Assign (PROD, “Produc.dat”)
Abrir `````````<Nombre>`````````
Ingresar PROD.Num 
Mientras PROD.Num <> 0 
	Leer (PROD.Num) 
	Si (L.V.)  = `````````<Nombre>`````````
		Borrar  `````````<Nombre>`````````
	Sino 
	Mostrar: ‘NO EXISTE PRODUCTO‘ 
	Finsi 
	Ingresar PROD.Num 
Finmientras 
Cerrar `````````<Nombre>`````````
FIN
<!--ID: 1700071125490-->


### Características de los archivos #flashcard
1. Residen en soportes de información externos
2. Independientes de los programas
3. Información permanente almacenada
4. Gran capacidad
5. Posibilidad de variar la cantidad de elementos durante la ejecución
<!--ID: 1700071125498-->


### Clasificación de los archivos #flashcard
Contenido:
1. Datos
2. Programa
3. Texto
Tipo de acceso:
1. Secuencial (Se necesita leer los registros anteriores para llegar a uno)
2. Directo
<!--ID: 1700071125502-->


### Sintaxis de las operaciones fundamentales de los archivos #flashcard
1. Apertura y cierre
ABRIR ```<Nombre>```
CERRAR ```<Nombre>```
2. Lectura
LEER ```<Nombre>```
3. Grabación
GRABAR ```<Nombre>```
4. Re-Grabación
REGRABAR ```<Nombre>```
5. EOF(Nombre)
Retorna TRUE si llegó al final de un archivo
Se usa NO EOF ```<Archivo>```
<!--ID: 1700071125506-->


### Tipos de registro en archivos #flashcard
1. Registro lógico
- Conjunto de información unitario.
2. Registro físico
- Contiene uno o más registros lógicos
<!--ID: 1700071125513-->


### ¿Cómo trabajamos en nuestros programas de archivos? #flashcard
A nivel lógico. Con primitivas de transferencia
<!--ID: 1700071125518-->


### ¿Cómo se definen los archivos? #flashcard
Declarar la variable
Var
	NombreFile : file of R-nombre;
...
Asignar un nombre real para guardar en disco
Assign (NombreFile, "Nombre.dat")
<!--ID: 1700071125523-->
