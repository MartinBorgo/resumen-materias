# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Algoritmos y programación:: Unidad 4
# Archivos
![[Estructura de datos.pdf]]
![[Unidad IV - 2022 - Estructuras de Datos - Caso de Estudio - Parte 1.pdf]]
![[Unidad IV - 2022- Estructura de Datos - Práctico Dos-Campus.pdf]]
![[Estructura de datos - Matrices -Parte 1 v2.pdf]]
![[Estructura de datos.pdf]]
![[Estructura de datos - Matrices -Parte 1 v2.pdf]]
![[Ordenamiento BurbujaShell.pdf]]
![[Busqueda de datos.pdf]]
# Notas
## Arreglos #flashcard
- Objeto de datos conformado por un conjunto de datos homogéneos
<!--ID: 1700071232116-->


### Arreglos unidimensionales #flashcard
Vectores o listas: Conjunto finito n de elementos.
<!--ID: 1700071232148-->


### Sintáxis de una arreglo unidimensional #flashcard
- Vector(Posición)
<!--ID: 1700071232182-->


## Formas de acceder a un array #flashcard
- Directa: A través del subíndice (Selector dinámico), se puede acceder a cualquier elemento del array. 
- Secuencial: Recorriendo la estructura de datos. Se utiliza un esquema repetitivo. El recorrido puede efectuarse en dos direcciones: 
	- Desde el primer elemento hasta el último
	- Desde el último elemento hasta el primero.
<!--ID: 1700071232216-->


### Tipos de selector dinámico (subíndice) #flashcard
1. Constante
2. Variable
3. Expresión aritmética
<!--ID: 1700071232248-->


## Tipos de datos #flashcard
1. Primitivos (integer, Real, string)
2. Generados por el usuario
	1. Arrays
<!--ID: 1700071232280-->


## Objetos de datos #flashcard
Lugar donde se almacenan datos en tiempos de ejecución.
<!--ID: 1700071232316-->


## ¿Cómo definimos estructuras que agrupen datos de distintos tipos en pascal? #flashcard
Usamos el dato Record
```Record
Nombre = Record
Variable/s
end;```
```
<!--ID: 1700071232347-->


## ¿Cómo se referencia al campo donde guardaremos el dato en una estructura de registro? #flashcard
Nombre Arreglo [subíndice]. Nombre de campo
<!--ID: 1700071232427-->


## Arreglos unidimensionales simples encadenados #flashcard
Arreglos de misma dimensión con datos relacionados entre si
<!--ID: 1700071232506-->


## Registros #flashcard
- Varios tipos de datos en un campo
- Type, record en pascal con los distintos tipos de datos, **end** y Var con la definición del vector
<!--ID: 1700071232582-->


## Estrategia para arreglos con dimensión desconocida #flashcard
1. Definir un arreglo con dimensión suficientemente grande
2. Ingresar datos y almacenar la posición del último dato en una variable
3. Para todo proceso posterior sobre datos del arreglo, considerar la dimensión hasta el valor final de la variable
<!--ID: 1700071232730-->


## ¿Qué es una matriz? #flashcard
Un arreglo bidimensional
<!--ID: 1700071232799-->


## ¿Cómo se declara un arreglo bidimensional? #flashcard
Nombre(fila, columna)
<!--ID: 1700071232841-->


## Método de ordenamiento burbuja #flashcard
Se compara la primera posición con la siguiente, si no se encuentran en el orden requerido, se intercambian. El valor de la primera pasa a la burbuja, el valor de la segunda a la primera y el valor de la burbuja a la segunda. Así con todas las posiciones hasta la penúltima.
<!--ID: 1700071232846-->


#### ¿Cuántas recorridas máximas necesita un array para ordenarse? #flashcard
Es la cantidad de elementos total, menos uno
<!--ID: 1700071232850-->


#### ¿De qué tipo debe ser la variable auxiliar en el ordenamiento de arreglos de tipo registro? #flashcard
Del mismo tipo de registro del que se quiere ordenar
<!--ID: 1700071232854-->


### Burbuja simplificado #flashcard
Se utiliza una variable bandera (booleana por ejemplo) para saber si el array está ordenado
<!--ID: 1700071232858-->


### Burbuja con acotamiento #flashcard
Cuando en una recorrida el último elemento queda ordenado, se acorta la distancia de ordenamiento para obtener eficiencia.
<!--ID: 1700071232863-->


### Burbuja con retroceso #flashcard
Se hace una sola recorrida al array, si se efectúa un cambio, se retrocede a comparar los elementos anteriores para asegurar el orden
<!--ID: 1700071232868-->


## Método de ordenamiento Shell #flashcard
1. Se calcula la distancia de elementos a comparar (Total/2)
2. Se comparan valores por una distancia igual al valor calculado desde el punto uno. Si se intercambian, se debe retroceder.
3. Se recalcula el valor dividiendo al valor utilizado en la recorrida anterior por dos.
<!--ID: 1700071232872-->


### El método Shell continúa hasta... #flashcard
1. Retroceso
Diferencia del valor primera posición con el segundo. Si es positiva, se vuelve a esa posición, si es negativa o cero, se sigue comparando.
a) La comparación efectuada indica que están en orden
b) Se llega al inicio del vector
2. Que finaliza
Termina cuando finaliza una recorrida en la cual se compararon e intercambiaron elementos en posiciones contiguas
<!--ID: 1700071232878-->


### Construcción del método Shell #flashcard
distancia := n/2
Mientras distancia > 0
	Para i = 1, (n-distancia), 1
		z := i
		Mientras z > 0 and then V(z) > V(z+distancia)
			Aux := V(z)
			V(z) := V(z+distancia)
			V(z+distancia) := Aux
			z := z - distancia
		FinMientras
	FinPara
	distancia := distancia / 2
FinMientras
<!--ID: 1700071232882-->


## Búsqueda de datos

### Búsqueda de datos secuencial desordenada #flashcard
Se recorre todo el arreglo 
<!--ID: 1700071232887-->


### Búsqueda de datos dicotómica. Requisitos y metodología #flashcard
1. La estructura tiene que estar ordenada
2. Se debe conocer la cantidad de elementos
a. Se ingresa el dato
b. Se controla si está en el centro
c. Si es el dato, se finaliza la búsqueda. Sino, se determina si es mayor que el encontrado
d. De ahí se descarta uno de los intervalos de búsqueda y se repite desde el paso b
<!--ID: 1700071232891-->


### Ejemplo de código de búsqueda de datos dicotómica #flashcard
Ingresar ND
Mientras ND <>0
	LI := 0
	LS := 520
	X := (LI+LS)/2
	Mientras LS > LI and ALU[x].DOC <> ND
		Si ND > ALU[x].DOC
			LI := x + 1
		Sino
			LS := x - 1
		FinSi
		x := (LI+LS)/2
	FinMientras
	Si ALU[x].DOC = ND
		Mostrar "Nombre: ", ALU[x].NOM
	Sino
		Mostrar "Dato no encontrado"
	FinSi
	Ingresar ND
FinMientras
<!--ID: 1700071232896-->
