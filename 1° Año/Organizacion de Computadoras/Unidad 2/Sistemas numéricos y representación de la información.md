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
4. La base se representa como 10  
5. Cada dígito a la izquierda vale diez veces más que el de la derecha  

### Sistema binario
1. Valor relativo  
2. Base dos  
3. 0, 1  
4. La base se representa como 10  
5. Cada dígito vale dos veces más que el de la derecha  

### Sistema octal y hexadecimal
**Octal**:  
1. Valor relativo  
2. Base 8  
3. 0,1,2,3,4,5,6,7  
4. La base se representa como 10  
5. Cada dígito vale 8 veces más que el de la derecha  

**Hexadecimal**:  
1. Valor relativo  
2. Base 16  
3. 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F  
4. La base se representa como 10  
5. Cada dígito vale 16 veces más que el de la derecha  

## Conversión entre sistemas
### Binario a decimal
Se descompone el número binario en las sucesivas potencias de la base y se calcula de forma directa. Ejemplo:  
1 1 0 1 = (1 × 2^3) + (1 × 2^2) + (0 × 2^1) + (1 × 2^0) = 13

### Decimal a binario
Se realizan divisiones sucesivas del número decimal por 2 hasta obtener el último cociente entero. El número binario se forma a partir del último cociente y los restos de las divisiones.

### Hexadecimal a decimal
Se descompone el número hexadecimal en potencias de la base 16 y se calcula de forma directa. Ejemplo:  
A4B = (10 × 16^2) + (4 × 16^1) + (11 × 16^0) = 2635

### Decimal a hexadecimal
El mismo proceso que el decimal a binario, pero utilizando la base 16. Los restos y cocientes se convierten a hexadecimal.

### Binario a hexadecimal
Se agrupan los dígitos binarios en bloques de 4, comenzando desde la derecha, y cada grupo se convierte a su equivalente hexadecimal.

### Hexadecimal a binario
Se convierte cada dígito hexadecimal en su equivalente binario de 4 dígitos.

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
Se utiliza una tabla de 16x16 para sumar o restar números hexadecimales. 

## Números signados
Representación de magnitud y signo, donde el bit más significativo indica el signo (0 para positivo, 1 para negativo).

## Números de punto fijo
1. Todos los números tienen la misma cantidad de dígitos.  
2. La coma decimal está en el mismo lugar para todos.  
- **Rango:** Diferencia entre el mayor y el menor número que puede representarse.  
- **Precisión:** Distancia entre dos números consecutivos.  
- **Error:** Mitad de la distancia entre dos números consecutivos.  

## Números de punto flotante
Permiten representar un amplio rango de números con menos dígitos binarios.  
- **Rango:** Determinado por el exponente.  
- **Precisión:** Determinada por la mantisa.  
- **Error:** Distancia entre dos números consecutivos.  

## Códigos
### Código BCD
Cada dígito decimal se representa con 4 dígitos binarios. Facilita la conversión entre decimal y binario sin errores de conversión.

### Códigos alfanuméricos
**EBCDIC**: Código binario extendido decimal intercambiable. Usa 8 bits para representar caracteres.  
**ASCII**: Utiliza 8 bits para representar caracteres.  
**Unicode**: Sistema de codificación universal para representar caracteres de múltiples alfabetos.

## Relación entre bases de sistemas numéricos
Los sistemas decimal, binario, octal y hexadecimal son sistemas posicionales de valor relativo. La diferencia radica en la base utilizada para agrupar los valores.

