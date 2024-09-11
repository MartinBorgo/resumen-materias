## Álgebra de Boole
Las puertas lógicas que implementan las operaciones lógicas del álgebra de Boole son esenciales para el diseño de circuitos digitales. Estas operaciones permiten que las computadoras realicen tareas mediante combinaciones de estados binarios (0 y 1).

## Operaciones lógicas
### ¿Qué operación lógica implementa el producto, cuál es su circuito y cuál su puerta lógica?
La operación lógica AND.  
- Su circuito es el serie.
- Su puerta lógica es la AND.

### ¿Qué operación lógica implementa la suma, cuál es su circuito y cuál su puerta lógica?
La operación lógica OR.  
- Su circuito es el paralelo.
- Su puerta lógica es la OR.

### ¿Qué operación lógica invierte el resultado de AND y OR, cuál es su expresión simbólica y cuál su símbolo?
La operación lógica NOT invierte los resultados de AND y OR.  
- Su expresión simbólica es: X = A'.
- Su símbolo es un triángulo con un círculo en la salida.

#### ¿Cuáles son los símbolos de las puertas lógicas NAND y NOR?
- **NAND**: Puerta AND seguida de NOT (una barra sobre la expresión AND).
- **NOR**: Puerta OR seguida de NOT (una barra sobre la expresión OR).

### ¿Cuál es la operación de la suma exclusiva, cuál es su símbolo?
La operación lógica XOR es la suma exclusiva.  
- Su símbolo es un OR con un círculo alrededor (⊕).

## ¿Se puede representar XOR con otras puertas? Si se puede, ¿Cómo?
Sí, se puede representar utilizando puertas AND, OR y NOT.  
- Ejemplo:  
  Z = (A AND NOT B) OR (NOT A AND B)

## ¿Qué es una puerta lógica y cuál es su voltaje típico?
- Una puerta lógica es un elemento eléctrico simple que toma una o más señales de entrada y genera un valor de salida que depende de los valores de entrada.
- Voltaje típico: 5V para representar 1 y 0V para representar 0.

## ¿Cuáles son las formas de definir una puerta?
1. **Símbolo gráfico**: Representación visual de la puerta lógica.
2. **Notación algebraica o ecuación booleana**: Representación matemática de las operaciones.
3. **Tabla de verdad**: Muestra todas las combinaciones posibles de entradas y la salida correspondiente.

## ¿Qué es una expresión canónica, mintérmino y maxtérmino?
- **Expresión canónica**: Producto o suma donde aparecen todas las variables de forma directa o inversa.
1. **Mintérmino**: Suma de productos que incluye todas las variables en una forma específica. La suma de todos los resultados 1 en la tabla de verdad.
2. **Maxtérmino**: Producto de sumas que incluye todas las variables. La multiplicación de todos los resultados 0 en la tabla de verdad.

## Ejemplo de suma de productos lógicos:
Expresión:  
F = A'·B'·C + A'·B·C + A·B'·C + A·B·C' + A·B·C

### Tabla de verdad:

| A | B | C | F |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

## Propiedades del álgebra de Boole:
1. **Conmutativa**:  
   - X·Y = Y·X  
   - X+Y = Y+X
2. **Asociativa**:  
   - (X·Y)·Z = X·(Y·Z)  
   - (X+Y)+Z = X+(Y+Z)
3. **Distributiva**:  
   - X·(Y+Z) = X·Y + X·Z  
   - X+(Y·Z) = (X+Y)·(X+Z)
4. **Ley de la doble negación**:  
   - (X')' = X
5. **Leyes de De Morgan**:  
   - (X·Y·Z)' = X' + Y' + Z'  
   - (X+Y+Z)' = X'·Y'·Z'

## Ejemplo de producto de sumas lógicas:
Expresión:  
F = (A + B + C) · (A + B' + C) · (A' + B + C)

### Tabla de verdad:

| A | B | C | F |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

## Implementación de funciones booleanas
Las puertas lógicas se utilizan para implementar funciones booleanas mediante la combinación de puertas AND, OR, NOT, NAND, NOR, XOR y XNOR. Estas funciones pueden representarse con expresiones algebraicas y tablas de verdad, y permiten diseñar circuitos digitales complejos a partir de bloques simples.
