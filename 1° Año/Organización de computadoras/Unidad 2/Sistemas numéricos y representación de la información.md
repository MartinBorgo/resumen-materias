# Anki
TARGET DECK: Facultad:: Sistemas:: Primer año:: Organización de computadoras:: Unidad 2
# Archivos
![[UNIDAD 2.pdf]]
![[Punto Flotante - Andrew S. Tanenbaum - Organizaciones de Computadoras Un enfoque estructurado 4ta.pdf]]

# Trabajo práctico
![[TP02.pdf]]
#  Notas

## Sistemas de numeración existentes #flashcard
1. Absoluto
	1. Romano
2. Posicional
	1.  Decimal
<!--ID: 1700156793737-->


## Características de los sistemas de numeración de valor relativo #flashcard
1. Base
2. Forma de escribir la base
3. Mayor dígito 
4. Forma de agrupar
5. Forma de descomponer
 
<!--ID: 1700156793744-->



### Sistema decimal #flashcard
1. Valor relativo
2. Base diez
3. 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
4. La base se representa 10
5. Cada dígito de la izquierda vale diez veces más que el de la derecha
 
<!--ID: 1700156793749-->



### Sistema binario #flashcard
1. Valor relativo
2. Base dos
3. 0, 1 
4. La base se representa 10 
5. Cada dígito vale dos veces más que el de la derecha
 
<!--ID: 1700156793754-->



### Sistema octal y hexadecimal #flashcard
Octal:
1. Valor relativo 
2. Base 8 
3. 0,1,2,3,4,5,6,7 
4. La base se representa 10 
5. Cada dígito vale 8 veces más que el de la derecha
Hexadecimal
1. Valor relativo
2. Base 16
3. 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F
4. La base se representa 10
5. Cada dígito vale 16 veces más que el de la derecha
 
<!--ID: 1700156793759-->



## Conversión entre sistemas
### Binario a decimal #flashcard
Se descompone el número binario en las sucesivas potencias de la base y se calcula de forma directa
 
<!--ID: 1700156793763-->



### Decimal a binario #flashcard
Se realizan sucesivas divisiones del número decimal por 2 hasta llegar al último cociente entero. Luego el número binario se escribe desde el último cociente y todos los restos de las divisiones, del último al primero
 
<!--ID: 1700156793767-->



### Hexadecimal a decimal #flashcard
Se descompone el número hexadecimal en las sucesivas potencias de la base y se calcula de forma directa
 
<!--ID: 1700156793771-->



### Decimal a hexadecimal #flashcard
El mismo sistema que el decimal a binario, salvo que la división es con 16 y los restos y cociente se transforman a sistema hexadecimal
 
<!--ID: 1700156793775-->



### Binario a hexadecimal #flashcard
Se separa el número binario en grupos de cuatro dígitos comenzando desde la derecha y se busca el número hexadecimal que le corresponde. Si al de la izquierda le faltan dígitos se le agregan ceros a la izquierda
 
<!--ID: 1700156793779-->



### Hexadecimal a binario #flashcard
Se busca el número binario de 4 dígitos correspondiente a cada dígito hexadecimal
 
<!--ID: 1700156793783-->



## Operaciones aritméticas
### Suma y resta binaria #flashcard
0 + 0 = 0 
0 + 1 = 1 
1 + 0 = 1 
1 + 1 = 0 llevando 1
1 - 1 = 0 
1 - 0 = 1 
0 - 0 = 0 
0 - 1 = 1 pidiendo 1 al anterior
 
<!--ID: 1700156793786-->



### Suma y resta hexadecimal #flashcard
1. Se resta igual que cualquier otro sistema
2. Se crea una tabla 16x16 con todos los números hexadecimales y sus respectivas sumas en intersecciones
 
<!--ID: 1700156793791-->



## Números signados #flashcard
- Magnitud y signo
 
<!--ID: 1700156793795-->



## Números de punto fijo #flashcard
1. Todos los números a representar tienen la misma cantidad de dígitos
2. La coma decimal está en el mismo lugar
- Rango:
	- Diferencia entre el mayor y el menor que expresa
- Precisión
	- Distancia entre dos números consecutivos
3. Error
	1. La mitad entre la distancia de dos números consecutivos
 
<!--ID: 1700156793799-->



## Números de punto flotante #flashcard
1. Amplio rango de números con pocos dígitos binarios
- Rango:
	- Exponente
- Precisión:
	- Mantisa
2. Error
	1. Distancia entre dos números consecutivos
 
<!--ID: 1700156793802-->



## ¿En base a qué estandar están definidos los números de punto flotante? #flashcard
- IEE 754 32 bits o 64
 
<!--ID: 1700156793807-->



## Diferencia entre notación en coma flotante y fija #flashcard
1. Velocidad (Mayor en fija)
2. Rango (Mayor en flotante)
 
<!--ID: 1700156793811-->



## Códigos
### Código BCD #flashcard
- Datos numéricos con 4 dígitos binarios
![[BCD.png]]
 
<!--ID: 1700156793815-->



### Alfanuméricos
#### Código EBCDIC #flashcard
- Extended Binary Coded Decimal Interchange
- 4 Numéricos y 4 de zona
- ![[EBCDIC.png]]
 
<!--ID: 1700156793818-->



#### Código ASCII 8 #flashcard
- Secuencia de 8 bits
- American standard code for information interchange
- ![[ASCII (1).png]]
- ![[ASCII (2).png]]
- ![[ASCII (3).png]]
 
<!--ID: 1700156793823-->



#### Código unicode #flashcard
- Universalidad, uniformidad y unicidad
- 4 grupos de 4 bits
 
<!--ID: 1700156793827-->



## ¿Qué relación existe  entre las bases del sistema decimal, binario, octal y hexadecimal? #flashcard
- Todos son sistemas de valor relativo y base 10
 
<!--ID: 1700156793831-->

