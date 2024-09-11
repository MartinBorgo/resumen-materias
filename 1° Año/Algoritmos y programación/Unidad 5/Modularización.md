# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Algoritmos y programación:: Unidad 5
# Archivos
![[AyP-Subprogramas.pdf]]
![[Parámetros.pdf]]
![[Funciones.pdf]]
# Notas
## Abstracción #flashcard
Proceso para manejar la complejidad de las cosas reduciendo el contenido de una información
<!--ID: 1700071104179-->


### Clasificación de abstracción en informática #flashcard
Abstracción de datos
Abstracción de procesos
<!--ID: 1700071104184-->


## Modularización #flashcard
1. Forma de programación que consiste en divid un programa en módulos para hacerlo más legible y manejable
<!--ID: 1700071104191-->


### Ventajas de la modularización #flashcard
1. Productividad
2. Reusabilidad
3. Facilidad de mantenimiento
4. Facilidad de crecimiento del sistema
<!--ID: 1700071104196-->


### Características generales de la modularización #flashcard
1. Procedimiento invocado
2. Un solo punto de entrada
3. La ejecución de la unidad que llama a un procedimiento es suspendida
4. El control siempre retoma a la instrucción siguiente cuando finaliza el procedimiento
<!--ID: 1700071104200-->


## Subprogramas y tipos #flashcard
- Bloques de programas que constituyen uno de los conceptos más importantes en el diseño de los lenguajes
- Procedimientos (Algoritmos, call)
- Funciones (Evalúan una expresión, producen resultado)
<!--ID: 1700071104208-->


### Características deseables de los módulos de subprogramas #flashcard
1. Cohesión (Mayor es mejor) (Sencillez)
2. Acoplamiento (Menor es mejor) (Interacciones)
<!--ID: 1700071104213-->


## Variables locales y globales #flashcard
1. Globales en todo el programa y procedimiento
2. Locales solo en el procedimiento
<!--ID: 1700071104216-->


## Parámetros, tipos y pases #flashcard
Variable o estructura de datos.
- Tipo real
El del programa principal
- Tipo formal
El escrito en el subprograma
1. Pase por copia
Se copia del parámetro real al formal (Proteje el real y ocupa más memoria)
2. Por referencia
Se copia la dirección del parámetro (Afecta el real, ocupa menos memoria)
<!--ID: 1700071104223-->


### Orden de búsqueda del parámetro en un procedimiento #flashcard
1. Busca si es variable local
2. Se fija si es un parámetro
3. Busca si es variable global
4. Si no la encuentra, da error
<!--ID: 1700071104227-->


## Funciones
### Componentes de una función #flashcard
1. Parámetros
2. Código
3. Resultado
<!--ID: 1700071104231-->


### Formato de una función #flashcard
Function ```<Nombre>``` (parámetros): ```<tipodatoregreso>;```
Begin
	Instrucciones;
	[Nombre := (valor/resultado)]
end;
<!--ID: 1700071104236-->


## Diferencias entre  procedimientos y funciones #flashcard
| Procedimientos                        | Funciones                                    |
| ------------------------------------- | -------------------------------------------- |
| Llamada explícita                     | El Se codifica en una expresión              |
| El nombre no se asocia a una variable | Se asocia a una variable con el mismo nombre |
| Puede devolver 0, 1 o "n"             | Devuelve un solo valor                       |
<!--ID: 1700071104241-->
