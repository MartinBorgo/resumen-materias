# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Álgebra y geometría analítica:: Unidad 6
# Archivos y videos
## Archivos
![[determinantes_y_sistemas.pdf]]
![[Aplicaciones Geométricas-determinantes.pdf]]


## Videos
https://www.youtube.com/watch?v=J-evjfvDmUk&ab_channel=Videosparamisalumnos


# Notas

## Calcular determinante de una matriz #flashcard 
Es un número obtenido de restar la diagonal principal multiplicada menos la diagonal secundaria
Tiene que ser cuadrada
det(A) = det(A1, A2, A3... An)
 
## Regla de Sarrus para matrices de orden 3 #flashcard 
![[Regla de Sarrus.png]]
Sumar los productos de las diagonales principales y restarles la suma de los productos de las secundarias
 
<!--ID: 1700071738624-->




## Propiedades de los determinantes de matrices cuadradas #flashcard 
1. Si la matriz se descompone en dos sumandos se puede realizar las determinantes de la suma de las matrices
2. Si hay un número escalar lambda multiplicando a una fila o columna, se puede sacar fuera del determinante como coeficiente
3. Si una matriz tiene dos filas iguales, el determinante es cero
4. El determinante de toda matriz identidad, sin importar el orden, es uno
5. ![[Propiedades de determinantes.png]]
6. Si se permutan las filas de una matriz cuadrada los determinantes son opuestas
 
<!--ID: 1700071738630-->


## Menor complementario #flashcard 
Determinante de orden inferior n-1, obtenido eliminando la fila i y la columna j de la matriz.
Indicado con barras laterales |A|
![[Menor complementario.png]]
 
<!--ID: 1700071738637-->



## Complemento algebraico #flashcard
Menor complementario con signo si i + j es par (Positivo) o no par (Negativo)
$$Cy=(-1)^{i+j}*Ay)$$ 
<!--ID: 1700071738644-->



## Ley de Laplace   #flashcard 
El determinante de una matriz es igual a la suma de los productos de los elementos de una fila
o columna por sus respectivos cofactores.
![[Ejemplo de Laplace.png]]
- Intentar usar las columnas con cero
 
<!--ID: 1700071738651-->


### la suma de los productos de los elementos de una recta (fila o columna) por los cofactores de una recta paralela son... #flashcard 
Nulos
 
<!--ID: 1700071738659-->



## Método de Chío #flashcard 
- El método consiste en transformar un determinante de orden n en otro del mismo valor de orden n-1.
- Se elige un elemento no nulo como pivote, aij y se extrae como factor común de la fila i. Luego, los otros elementos de la columna pivote se reducen a cero restando h de cada fila, con h diferente de i, fila i multiplicada por ahj, entonces:
 ![[Método de chío.png]]
 
<!--ID: 1700071738666-->



## Matriz adjunta #flashcard 
Indicado como Adj(A). Se obtiene transponiendo la matriz donde cada elemento se reemplaza por su cofactor.
<!--ID: 1700071738679-->



### Propiedades de las matrices adjuntas #flashcard
1. El determinante de una matriz y el de su transpuesta son el mismo
2. El determinante del producto de dos matrices es distributivo.
 
<!--ID: 1700071738687-->



## Producto de una matriz por su #flashcard adjunta
1. Conmutativo
2. Igual al determinante de A multiplicado por la matriz identidad
 


## Inversión de matrices no singulares #flashcard
1. Una matriz es invertible si y sólo si su determinante no es nulo.
2. $$A^{-1}=\frac{Adj(A)}{\det A}$$
 
<!--ID: 1700071738694-->




## Matriz ortogonal #flashcard
Su matriz inversa es igual a su transpuesta.
 
<!--ID: 1700071738701-->



## Teorema de Cramer #flashcard
1. Se utiliza para resolver sistemas de ecuaciones lineales donde el determinante de la matriz de coeficientes no es cero.
![[Teorema de Cramer.png]]
2. Resueltos los términos de x uno a uno
$$xj=\frac{\det(Aj)}{\det(A)}$$

det(Aj) significa intercambiar los términos de la columna j por su columna de términos de coeficiente
 
<!--ID: 1700071738708-->

