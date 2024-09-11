# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Álgebra y geometría analítica:: Unidad 8
# Archivos y videos
## Archivos
![[Espacios_Vectoriales_2015.pdf]]
![[Estructuras algebraicas 2015.pdf]]


# Notas

## Ley de composición interna #flashcard 
Definida en un conjunto A no vacío, es aquella donde $A x A->A$. Es decir, que a cada elemento de A, multiplicado por cualquier otro de A, nos devuelve un elemento del mismo conjunto.
<!--ID: 1700708745256-->

### Propiedades de la ley de composición interna #flashcard 
1. Asociatividad
2. Conmutatividad
3. Elemento neutro
4. Inverso de ley con neutro
5. Unicidad del elemento neutro
6. Inverso de la ley asociativa
7. Regularidad de un elemento
8. Distributividad
<!--ID: 1700708745314-->

#### Asociatividad en la ley de composición interna #flashcard 
$*:A^2\to A$
Es asociativa porque:
$(axb)xc = ax(bxc)$
<!--ID: 1700708745328-->

#### Conmutatividad en la ley de composición interna #flashcard 
$*:A^2\to A$
Porque:
$axb=bxa$
<!--ID: 1700708745339-->

#### Elemento neutro en la ley de composición interna #flashcard 
$*:A^2\to A$
Posee si: Existe un elemento tal que multiplicado un elemento de A, nos devuelve el mismo elemento.
<!--ID: 1700708745353-->

#### Existencia de inverso en una ley con neutro en la ley de composición interna #flashcard 
$a*a'=a'*a=e*$
El inverso, si existe, es relativo a cada elemento. Los elementos que lo admiten se llaman invertibles
<!--ID: 1700708745365-->

#### Unicidad del elemento neutro en la ley de composición interna #flashcard 
Si existe el elemento neutro, entonces es único. Porque $e*e'=e'*e=e$
<!--ID: 1700708745376-->

#### Unicidad del inverso respecto de una ley asociativa en la ley de composición interna #flashcard 
Si admite inverso, entonces este es único.
$a" = a"*e = a"*(a*a´) = (a"*a)*a ´ = e*a ´ = a ´$
<!--ID: 1700708745383-->

#### Regularidad de un elemento respecto de una ley de composición interna #flashcard 
Sea * una ley de composición interna en A,
- Elemento de a es regular a la izquierda: $a*b=a*c\to b=c$
- Elemento de a es regular a la derecha: $b*a=c*a\to b=c$
- Es regular si es regular en ambos lados
- * es cancelativa respecto a A si y sólo si todos los elementos son regulares
<!--ID: 1700708745390-->

#### Distributividad de una ley de composición interna respecto de otra #flashcard 
Sean * y º, dos leyes de composición interna del mismo conjunto.
Si una es distributiva respecto de la otra por derecha y por izquierda, es distributiva una respecto de otra.
- Distributiva por derecha: $(a*b)°c=(a°c)*(b°c)$
- Distributiva por izquierda: $c°(a*b)=(c°a)*(c°b)$
<!--ID: 1700708745397-->

## ¿Qué operación es el "círculo" entre dos elementos? #flashcard 
Producto vectorial
<!--ID: 1700708745408-->

## Estructura de grupo #flashcard 
Sea G un conjunto no vacío y una ley * definida en él. El par (G, * ) es un grupo si y sólo si:
- * es de composición interna
- * es asociativa
- Existe neutro para *
- Todo elemento de G admite inverso respecto de *
Los grupos para los que la ley es conmutativa se denominan abelianos o conmutativos.
Si * es LCI asociativa, el par (G, * ) es semigrupo
<!--ID: 1700708745418-->

### Ejemplos de estructuras de grupo #flashcard 
- (Z, +) es abeliano
- (N, +) no es grupo. No tiene neutro ni inverso
- ($N_{0}$, +) no es grupo. Tiene neutro pero no posee inverso aditivo
- (Q, .) no es grupo, el 0 no tiene inverso multiplicativo
<!--ID: 1700708745426-->

## Subgrupo #flashcard 
- Subconjunto no vacío B, del conjunto A. si y sólo sí (B, * ) es un grupo
- (Z, +) subgrupo de (Q, +)
<!--ID: 1700708745432-->

## Anillo #flashcard 
Conjunto no vacío A y leyes * y . definidas en él.
La terna (A, * , .) es un anillo:
1. (K, * ) grupo abeliano
2. (K, .) semigrupo
3. . distribuye doblemente * :
$$∀a, b, c ∈A$$
$$a ⋅ (b*c)=(a ⋅ b)*(a ⋅ c)∧ (𝑏 ∗ 𝑐) ⋅ 𝑎 = (𝑏 ⋅ 𝑎) ∗ (𝑐 ⋅ 𝑎)$$
<!--ID: 1700708745440-->

### Características de los anillos #flashcard 
1. ⋅ conmutativa, anillo conmutativo
2. ⋅ con elemento neutro, anillo con identidad o anillo con Unidad
3. Todo elemento distinto de cero es invertible respecto de ⋅, entonces se tiene un anillo de división
<!--ID: 1700708745447-->

### Ejemplos de anillos #flashcard 
1. (N, +, ⋅) no es anillo, no tiene neutro de adición
2. ($N_{0}$, +, ⋅) no es anillo, $N_{0}$ no tiene inverso aditivo
3. (Z, +, c) es anillo conmutativo con unidad
<!--ID: 1700708745454-->

### Anillos particulares #flashcard 
Anillo sin divisores de cero (A, * , ⋅): Elementos no nulos dan producto no nulo
Anillo de integridad: (A, * , ⋅) es anillo y 0 es el único divisor de cero
Dominio de integridad (A, * , ⋅) es anillo conmutativo con unidad o identidad sin divisores de cero (de integridad)
<!--ID: 1700708745461-->

## Enteros módulo n ($Zn$) #flashcard 
n es entero tal que $n\geq 2$, $Zn$ al conjunto:
$Zn = {0, 1, 2, 3, \dots, n-1}$
<!--ID: 1700708745467-->

### Operaciones y estructuras en $Zn$ #flashcard 
- Operaciones
1. Suma: h +k es igual al resto de la división de h + k por n.
2. Producto: h* k es igual al resto de la división de h* k por n.
- Estructuras
1. La terna ($Zn$, +, ⋅) es el anillo de los enteros módulo n
2. ($Zn$, +, ⋅) es un dominio de integridad si y sólo si n es primo
<!--ID: 1700708745475-->

## Ley de composición externa #flashcard 
Sean dos conjuntos A y Ω, este último llamado de operadores.
Función del tipo: $AxΩ\to A$
<!--ID: 1700708745494-->

### Ejemplo de ley de composición externa #flashcard 
A conjunto de segmentos de un plano, $AxΩ\to A$ es el producto de números naturales por segmentos del plano.
<!--ID: 1700708745502-->

## Espacio vectorial real #flashcard 
Conjunto de objetos, llamados *vectores* con operaciones de *adición y multiplicación por un escalar* que satisface los axiomas:
1. Ley de cierre. ($x∈V, y∈V, x+y∈V$)
2. Ley asociativa ($(x + y) + z = x + (y + z)$)
3. Vector nulo ($0∈V, x+0=0+x=x$)
4. Elemento opuesto ($x+(-x)=0$)
5. Ley conmutativa ($x+y=y+x$)
6. Ley de cierre ($α∈V, x∈V, α*x∈V$)
7. Distributiva del escalar ($α*(x+y)=α*x+α*y$)
8. Distributiva del vector ($(α+β)*x=α*x+β*x$)
9. Asociativa del escalar  ($(α*β)*x=α*(β*x)$)
10. Elemento neutro de la multiplicación ($1*x=x$)
<!--ID: 1700743915019-->

### Propiedades del espacio vectorial #flashcard 
Siendo θ y v vectores:
1. $α*θ=θ$ para todo escalar α
2. $0*v=θ$
3. $α*v=θ\toα=0 ∨ v=θ$
4. $(-1)*v=-v$
<!--ID: 1700746900480-->


## Subespacio #flashcard 
H subconjunto no vacío de un espacio vectorial V, si este H es un espacio vectorial, entonces es subespacio de V
Cumple las siguientes reglas de cerradura:
$$x∈H, y∈H\to x+y∈H$$
$$x∈H\to αx∈H, ∀α∈R$$
<!--ID: 1700746900485-->


## Combinación lineal #flashcard 
Sean $v_{1}, v_{2}, v_{3}, \dots, v_{n}$ vectores en un espacio vectorial V.
Cualquier vector de la forma: 
$$a_{1}* v_{1}+a_{2}* v_{2}+a_{3}* v_{3}\dots a_{n}*v_{n}$$
Donde $a_{n}$ son escalares
Se llama combinación lineal de $v_{1}, v_{2}, v_{3}, \dots, v_{n}$ 
<!--ID: 1700746900490-->


### Conjunto generador #flashcard 
Los vectores $v_{1}, v_{2}, v_{3}, \dots, v_{n}$ , generan a V si se pueden escribir como combinación lineal de ellos. Tales que:
$$a_{1}* v_{1}+a_{2}* v_{2}+a_{3}* v_{3}\dots a_{n}*v_{n}=v$$
<!--ID: 1700746900494-->


### Espacio generado por un conjunto de vectores #flashcard 
- Sean $v_{1}, v_{2}, \dots, v_{k}$, k vectores de un espacio vectorial V. El espacio generado por {${v_{1}, v_{2}, \dots, v_{k}}$} es el conjunto de combinaciones lineales de $v_{1}, v_{2}, \dots, v_{k}$
- gen{$v_{1}, v_{2}, \dots, v_{k}$}={$v/ v=α_{1}* v_{1}+α_{2}* v_{2}+α_{3}* v_{3}\dots, +α_{n}*v_{n}$}
- Donde $α_{1}, α_{2}, \dots, α_{k}$ son escalares arbitrarios
<!--ID: 1700746900498-->


### Dependencia e independencia lineal #flashcard 
- Son independientes si la única combinación lineal: $a_{1}* v_{1}+a_{2}* v_{2}+a_{3}* v_{3}\dots a_{n}*v_{n}=θ$ cuando los $a_{i}$ con i= 1, 2, 3... n son simultáneamente nulos. sino son dependientes
<!--ID: 1700746900502-->


### Dependencia lineal #flashcard 
- Teorema 1: Dos vectores sin linealmente dependiente si y sólo si uno es múltiplo escalar de otro
- Teorema 2: Conjunto de n vectores en $R^m$ es siempre linealmente dependiente si n>m
- Teorema 3 $$A=\begin{pmatrix}
a_{1 1} & a_{1 2} & \dots & a_{1 n} \\ 
a_{21} & a_{22} & \dots & a_{2 n}  \\ 
\dots&\dots&\dots&\dots \\
a_{m1}&a_{m2}&\dots&a_{mn} \\
\end{pmatrix}$$
- Las columnas de A consideradas como vectores son linealmente dependientes si y sólo si el sistema $A*c=0$, tiene soluciones no triviales. Donde:
$$c=\begin{pmatrix}
c_{1} \\
c_{2} \\
\dots \\
c_{n}
\end{pmatrix}$$
- Teorema 4: sean $v_{1}, v_{2}, v_{3}, \dots, v_{n}$ vectores en $R^n$ y sea A una matriz nxn con columnas $v_{1}, v_{2}, v_{3}, \dots, v_{n}$.
Entonces los vectores son linealmente independientes si y sólo si la única solución al sistema homogéneo $A*c=0$ es la solución trivial c=0
- Teorema 5: Sea A matriz nxn. Entonces det(A) es distinto de cero si y sólo si las columnas de A son linealmente independientes
- Teorema 7: Cualquier conjunto de n vectores linealmente independientes en $R^n$  genera a $R^n$
<!--ID: 1700746900506-->

### Resumen de teoremas de dependencia lineal #flashcard 
- Sea A una matriz nxn:
1. A es invertible
2. La unica solución al sistema homogéneo es la trivial
3. El sistema A x = b tiene única solución para cada n-vector b
4. A es equivalente por renglones a la matriz identidad de nxn
5. La forma escalonada por renglones de A tiene n pivotes
6. El determinante de A es dintinto de cero
7. Columnas y renglones de A son linealmente independientes
<!--ID: 1700766804324-->


## Base #flashcard 
- Un conjunto finito de vectores {$v_{1}, v_{2}, v_{3}, \dots, v_{n}$} es una base para un espacio vectorial V si:
1. El conjunto {$v_{1}, v_{2}, v_{3}, \dots, v_{n}$} es linealmente independiente
2. El conjunto {$v_{1}, v_{2}, v_{3}, \dots, v_{n}$} genera a V
<!--ID: 1700766804329-->


### Teorema de base #flashcard 
1. Teorema 1: Si {$v_{1}, v_{2}, v_{3}, \dots, v_{n}$} es base de V y si $v∈V$ entonces existe un conjunto único de escalares $c_{1}, c_{2}, c_{3}, \dots, c_{n}$ tales que $v/ v=c_{1}* v_{1}+c_{2}* v_{2}+c_{3}* v_{3}\dots, +c_{n}*v_{n}$
2. Teorema 2: Si {$v_{1}, v_{2}, v_{3}, \dots, v_{n}$} y {$u_{1}, u_{2}, u_{3}, \dots, u_{m}$}  son bases de un espacio vectorial , entonces n=m. Cualesquiera dos bases en un espacio vectorial tienen mismo número de vectores
<!--ID: 1700766804333-->


## Rango de una matriz A $\rho(A)$ #flashcard 
- Es el número de pivotes en su forma escalonada por renglones
- Es el número de columnas linealmente independientes que tiene una matriz (o renglones)
- Tiene un número infinito de soluciones si y sólo si $\rho(A)=\rho(A, b)$
<!--ID: 1700766804337-->


## Teorema de Rouché-Frobenius #flashcard 
Un sistema de ecuaciones tiene solución si y sólo si su matriz de coeficientes y la matriz ampliada tienen igual rango. Si $\rho(A)=\rho(A, b)$ es compatible, sino incompatible
1. Si estos rangos son iguales al número de n incógnitas es compatible determinado $\rho(A)=\rho(A, b)=n$
2. Si el rango de estos es menor que el número de n incógnitas es compatible indeterminado $\rho(A)=\rho(A, b)<n$
<!--ID: 1700766804341-->


### Cambio de base #flashcard 
La matriz A nxn, con columnas de vectores de la base $B_{1}$ expresados en la base $B_{2}$, es la matriz de transición de $B_{1}$ a $B_{2}$
$$A=\begin{pmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n} \\
a_{21} & a_{22} & a_{23} & \dots & a_{2n} \\
\dots & \dots & \dots & \dots & \dots \\
a_{n_{1}} & a_{n_{2}} & a_{n_{3}} & \dots & a_{nn} \\
\end{pmatrix}$$
Donde $a_{nn}$ son reemplazados por $(u_{n})B_{2}$
<!--ID: 1700766804345-->


#### Teoremas de cambio de base #flashcard 
1. Sean $B_{1}$ y $B_{2}$ bases de un espacio vectorial V. Sea A la matriz de transición de $B_{1}$ a $B_{2}$. Entonces:
$$(x)_{B_{2}}=A*(x)_{B_{1}}$$
2. Si A es la matriz de transición, entonces su inversa es la matriz de transición de $B_{2}$ a $B_{1}$
<!--ID: 1700766804349-->


