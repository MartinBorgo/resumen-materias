## Sistemas de numeración existentes
1. Absoluto  
   1. Romano  
2. Posicional  
   1. Decimal  

## Características de los sistemas de numeración de valor relativo
1. Base  
2. Forma de escribir la base  
3. Mayor dígito  
4. Forma de agrupar  
5. Forma de descomponer  

### Sistema decimal
1. Valor relativo  
2. Base diez  
3. 0, 1, 2, 3, 4, 5, 6, 7, 8, 9  
4. La base se representa 10  
5. Cada dígito de la izquierda vale diez veces más que el de la derecha  

### Sistema binario
1. Valor relativo  
2. Base dos  
3. 0, 1  
4. La base se representa 10  
5. Cada dígito vale dos veces más que el de la derecha  

### Sistema octal y hexadecimal
**Octal**:  
1. Valor relativo  
2. Base 8  
3. 0,1,2,3,4,5,6,7  
4. La base se representa 10  
5. Cada dígito vale 8 veces más que el de la derecha  

**Hexadecimal**:  
1. Valor relativo  
2. Base 16  
3. 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F  
4. La base se representa 10  
5. Cada dígito vale 16 veces más que el de la derecha  

## Conversión entre sistemas
### Binario a decimal
Se descompone el número binario en las sucesivas potencias de la base y se calcula de forma directa  

### Decimal a binario
Se realizan sucesivas divisiones del número decimal por 2 hasta llegar al último cociente entero. Luego el número binario se escribe desde el último cociente y todos los restos de las divisiones, del último al primero  

### Hexadecimal a decimal
Se descompone el número hexadecimal en las sucesivas potencias de la base y se calcula de forma directa  

### Decimal a hexadecimal
El mismo sistema que el decimal a binario, salvo que la división es con 16 y los restos y cociente se transforman a sistema hexadecimal  

### Binario a hexadecimal
Se separa el número binario en grupos de cuatro dígitos comenzando desde la derecha y se busca el número hexadecimal que le corresponde. Si al de la izquierda le faltan dígitos se le agregan ceros a la izquierda  

### Hexadecimal a binario
Se busca el número binario de 4 dígitos correspondiente a cada dígito hexadecimal  

## Operaciones aritméticas
### Suma y resta binaria
0 + 0 = 0  
0 + 1 = 1  
1 + 0 = 1  
1 + 1 = 0 llevando 1  
1 - 1 = 0  
1 - 0 = 1  
0 - 0 = 0  
0 - 1 = 1 pidiendo 1 al anterior  

### Suma y resta hexadecimal
1. Se resta igual que cualquier otro sistema  
2. Se crea una tabla 16x16 con todos los números hexadecimales y sus respectivas sumas en intersecciones  

## Números signados
- Magnitud y signo  

## Números de punto fijo
1. Todos los números a representar tienen la misma cantidad de dígitos  
2. La coma decimal está en el mismo lugar  

- Rango:  
  - Diferencia entre el mayor y el menor que expresa  
- Precisión:  
  - Distancia entre dos números consecutivos  
- Error:  
  - La mitad entre la distancia de dos números consecutivos  

## Números de punto flotante
1. Amplio rango de números con pocos dígitos binarios  

- Rango:  
  - Exponente  
- Precisión:  
  - Mantisa  
- Error:  
  - Distancia entre dos números consecutivos  

## ¿En base a qué estándar están definidos los números de punto flotante?
- IEE 754 32 bits o 64  

## Diferencia entre notación en coma flotante y fija
1. Velocidad (Mayor en fija)  
2. Rango (Mayor en flotante)  

## Códigos
### Código BCD
- Datos numéricos con 4 dígitos binarios  

### Alfanuméricos
#### Código EBCDIC
- Extended Binary Coded Decimal Interchange  
- 4 Numéricos y 4 de zona  

#### Código ASCII 8
- Secuencia de 8 bits  
- American standard code for information interchange  

#### Código unicode
- Universalidad, uniformidad y unicidad  
- 4 grupos de 4 bits  

## ¿Qué relación existe entre las bases del sistema decimal, binario, octal y hexadecimal?
- Todos son sistemas de valor relativo y base 10  
