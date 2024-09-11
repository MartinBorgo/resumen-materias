# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Álgebra y geometría analítica:: Unidad 2
# Archivos
![[Teoría de Conjuntos_4_2022.pdf]]
![[Teoría de Conjuntos_3_2022.pdf]]
![[Teoría de Conjuntos_3_2022.pdf]]
![[Teoría de conjuntos_1_2022.pdf]]
![[_lgebra_de_conjuntos_y_lgebra_de_proposiciones.pdf]]
![[complemento_Conjuntos_2015.pdf]]
![[Teor_a_de_Conjuntos.pdf]]
## Videos



# Autoevaluación

### La negación de ∀x∈R:x2=y2⇒x=y∀x∈ℜ:x2=y2⇒x=y es ... y su el valor de verdad de dicha negación es ...    #flashcard 
- ∃x∈R/x2=y2∧x≠y∃x∈ℜ/x2=y2∧x≠y
- Verdadera.
 
<!--ID: 1700071611709-->



### ![[Inecuación con módulo (1).png]] #flashcard 
![[Inecuación con módulo (2).png]]
 
<!--ID: 1700071611716-->




## Resolver: [[Resolver aplicando propiedades1.png]] #flashcard 
![[Resultado aplicando propiedades2.png]]
 
<!--ID: 1700071611722-->



# Notas

## Conjunto #flashcard 
Agrupación de objetos llamados elementos.
<!--ID: 1700071611730-->
## Relación de membresía #flashcard
Si A es un conjunto y x es un elemento de A, la expresión simbólica x ∈ A se lee “x pertenece a A” y significa que “x es un elemento del conjunto A
<!--ID: 1700071611738-->


## diagrama de Venn #flashcard 
- Conjuntos en círculos
- Conjunto universal, un rectángulo.
<!--ID: 1700071738715-->



## Relación de inclusión #flashcard
Sean A y B dos conjuntos, A está incluido en B, lo que se denota A ⊂ B si, y sólo si, todo elemento de A es un elemento de B.
A ⊂ B ↔∀x: (x ∈ A ∧ x ∈ B)
<!--ID: 1700071611744-->



## Propiedades de la relación de inclusión #flashcard
- A⊂A; ∀A (Reflexivo)
- A, B: si A⊂B∧B⊂A -> A=B (Antisimétrico)
- ∀A, B, C: si A⊂B∧B⊂C -> A⊂C (Transitivo)
<!--ID: 1700071611750-->



## Axiomas #flashcard
- Axioma de sustitución
- Axioma de extensión
- Axioma de especificación
- Axioma del conjunto de potencias
- Axioma de la unión de conjuntos.
<!--ID: 1700071611756-->



### Axioma 1. (Axioma de sustitución) #flashcard
“Sea P(x) una función proposicional con respecto a la variable x. Si P(x) es verdadera y si 𝑢 = 𝑥, entonces P(u) también es verdadera”.
 
<!--ID: 1700071611762-->



### Axioma 2. (Axioma de extensión) #flashcard
"Dos conjuntos A y B son iguales si y sólo si tienen los mismos elementos".
A = B ↔ (A ⊂ B∧ B ⊂ A)
 
 
<!--ID: 1700071611766-->




### Axioma 3. (Axioma de especificación) #flashcard
“Dado un conjunto 𝑼 y una función proposicional 𝑷(𝒙) con 𝒙 ∈ 𝑼, existe un subconjunto único 𝑨 𝒅𝒆 𝑼, cuyos elementos son todos elementos 𝒙 ∈ 𝑼 tal que 𝑷(𝒙) es verdadero”.
 
<!--ID: 1700071611772-->




### Axioma 4. (Axioma del conjunto de potencias) #flashcard
“Dado un conjunto 𝑨, existe uno y sólo un conjunto cuyos elementos son todos subconjuntos de 𝑨.”
 
<!--ID: 1700071611777-->



#### Cardenal del conjunto de potencias de A #flashcard
El cardinal del conjunto potencia de A es el número de elementos que tiene el conjunto potencia y viene dado por 2 elevado al cardinal del conjunto A
 
<!--ID: 1700071611780-->



#### Cardenal del conjunto de potencia de vacío #flashcard
Es igual a 1, ya que 2^0 = 1. Esto se debe a que el cardinal del conjunto vacío es 0 y por tanto P(∅) = {∅}
 
<!--ID: 1700071611784-->



### Axioma 5. (Axioma de la unión de conjuntos) #flashcard
"Dados dos conjuntos A y B, existe un conjunto U tal que A ⊂ U y B ⊂ U."
Sean A ⊂ U y B ⊂ U dos conjuntos, la unión de A y B, denotada por 𝐴 ∪ 𝐵, es el conjunto formado por todos los elementos 𝑥 ∈ 𝑈 tales que 𝑥 ∈ 𝐴 o 𝑥 ∈ 𝐵. Simbólicamente
𝐴 ∪ 𝐵 = {𝑥 ∈ 𝑈 / 𝑥 ∈ 𝐴 ∨ 𝑥 ∈ 𝐵}
Es decir, 𝑥 ∈ (𝐴 ∪ 𝐵) ⇔ (𝑥 ∈ 𝐴 ∨ 𝑥 ∈ 𝐵)
 
 DELETE# Si A intersección B = {} se dirá que los conjuntos A y B son... #flashcard
Desarticular
 
<!--ID: 1700071611790-->



#### Conjunto de unión #flashcard
𝐴∪𝐵 = {𝑥 ∈ 𝑈 / 𝐴(𝑥) ∈ 𝐵(𝑥)}, la unión de dos conjuntos A y B es el conjunto de verdad de la disyunción de las funciones proposicionales correspondientes
 
<!--ID: 1700071611795-->



## Propiedades de la relación de igualdad #flashcard
1.A=A; ∀A (Reflexivo)
2. ∀A, B: si A=B -> B=A (Simétrico)
3. ∀A, B, C: Si A=B ∧ B=C -> A=C (Transitiva)
- Si cumples los tres, es una equivalencia
 
<!--ID: 1700071611798-->



## Propiedades del conjunto vacío #flashcard
1. ∀a:a∉∅
1. Verdadero por definición de conjunto vacío
2. ∀A:∅⊂A
1. ∅⊂A:∀x: x∈∅ -> x∈A
2. Antecedente falso, luego es verdadero
3. Es único
- Demostración: Supongamos que son dos. ∅ y ∅´.
- Por propiedad de conjunto vacío, ∅⊂∅´ y ∅´⊂∅
- Según la propiedad antisimétrica ∅=∅´
 ![[Unión.png]]
 
<!--ID: 1700071611803-->


## Operaciones con conjuntos

### Intersección de conjuntos #flashcard
Sean A ⊂ U y B ⊂ U dos conjuntos, la intersección de A y B, denotada por 𝐴 ∩ 𝐵, es el conjunto formado por todos los elementos x de U, tales que:
x ∈ A y x ∈ B.
- Simbólicamente: 𝐴 ∩ 𝐵 = 𝑥 ∈ 𝑈/𝑥 ∈ 𝐴 ∧ 𝑥 ∈ 𝐵
- Es decir: 𝑥 ∈ 𝐴 ∩ 𝐵 ⇔ 𝑥 ∈ 𝐴 ∧ 𝑥 ∈ B)
![[Intersección.png]]
 
<!--ID: 1700071611806-->


### Observación sobre 𝐴 ∩ 𝐵 = ∅ #flashcard
Si 𝐴 ∩ 𝐵 = ∅ , diremos que los conjuntos A y B son disjuntos.
 
<!--ID: 1700071611810-->



### Diferencia de conjuntos #flashcard
Dados los conjuntos A ⊂ U y B ⊂ U, la diferencia de A y B, denotada por 𝐴 − 𝐵, es el conjunto formado por todos los elementos x de U tales que x ∈ A y x  B.
- Simbólicamente: 𝐴 − 𝐵 = {𝑥∈𝑈 / 𝑥∈𝐴 ∧ 𝑥∉𝐵}
- Es decir, 𝑥∈(𝐴 – 𝐵) ⇔( 𝑥∈𝐴 ∧ 𝑥∉𝐵)
![[Diferencia de conjuntos.png]]
 
<!--ID: 1700071611814-->



#### Conjunto de diferencias #flashcard
A – 𝐵 = {𝑥 ∈ 𝑈 / 𝐴(𝑥) ∧ −𝐵(𝑥)}, la diferencia de dos conjuntos A y B en ese orden es el conjunto de verdad de la conjunción entre A(x) y la negación de B ( X).
 
<!--ID: 1700071611818-->



### Complemento de un conjunto respecto al conjunto universal #flashcard
![[Complemento de un conjunto.png]]
![[Gráfico complemento de un conjunto.png]]
 
<!--ID: 1700071611822-->




### Diferencia simétrica #flashcard 
![[Diferencia simétrica.png]]
- Relativo al Álgebra de Proposiciones. Sean 𝐴 = {𝑥∈ 𝑈 / 𝐴(𝑥)} y 𝐵 = {𝑥∈ 𝑈 / 𝐵(𝑥)}, los conjuntos de verdad de 𝐴(𝑥) y 𝐵(𝑥), respectivamente, definimos:
- Diferencia simétrica: 𝐴 △ 𝐵 = {𝑥 ∈ 𝑈 / 𝐴(𝑥) ∨ 𝐵(𝑥)}, la diferencia simétrica de dos conjuntos A y B, es el conjunto de verdad de la disyunción exclusiva de las funciones proposicionales correspondientes
 
<!--ID: 1700071611827-->



## Álgebra de conjuntos, propiedades más utilizadas #flashcard
![[Álgebra de conjuntos, propiedades más utilizadas.png]]
 
<!--ID: 1700071611831-->



### Propiedades de la unión #flashcard
- Teorema 1
- Dados los conjuntos 𝐴, 𝐵, 𝐶,𝐷 y ∅, en un conjunto universal 𝑈, se satisfacen las siguientes propiedades:
![[Propiedades de la unión.png]]
 
<!--ID: 1700071611834-->



### Propiedades de intersección #flashcard
- Teorema 2
- Dados los conjuntos 𝐴,𝐵, 𝐶 y ∅, en el conjunto universal 𝑈, se cumplen las siguientes propiedades:
![[Propiedades de la intersección.png]]
 
<!--ID: 1700071611838-->



### Propiedades distributivas #flashcard
- Teorema 3
- Dados los conjuntos 𝐴, 𝐵 y 𝐶, se cumplen las siguientes propiedades distributivas:
a) 𝐴 ∪ (𝐵 ∩ 𝐶) = (𝐴 ∪ 𝐵) ∩ (𝐴 ∪ 𝐶)
b) 𝐴 ∩ (𝐵 ∪ 𝐶) = (𝐴 ∩ 𝐵) ∪ (𝐴 ∩ 𝐶)
 
<!--ID: 1700071611842-->



### Propiedades de la diferencia establecida #flashcard
- Teorema 4
- Dados los conjuntos 𝐴, 𝐵, 𝐶 y ∅, se cumplen las siguientes propiedades:
![[Propiedades de la diferencia de conjuntos.png]]
 
<!--ID: 1700071611846-->



### Propiedad complementaria #flashcard
- Teorema 5
- Dados los conjuntos ∅, 𝐴 ⊂ 𝑈 𝑦 𝐵 ⊂ 𝑈, se cumplen las siguientes propiedades:
![[Propiedad del complemento .png]]
 
<!--ID: 1700071611849-->



### De Morgan #flashcard 
![[Ley de De Morgan.png]]
 
<!--ID: 1700071611853-->



## Par ordenado #flashcard
- Es cualquier conjunto de dos elementos en el que se distinguen un primer elemento y un segundo elemento.
- (𝑎, 𝑏) par ordenado del primer componente 𝑎 y el segundo componente b
 
<!--ID: 1700071611858-->



## Producto cartesiano de dos conjuntos #flashcard
Es el conjunto que tiene como elementos todos los pares ordenados cuyo primer componente pertenece al conjunto 𝐴 y cuyo segundo componente pertenece al conjunto 𝐵. Simbólicamente AxB ={(x, y)/ x∈ A∧y∈B}
 
<!--ID: 1700071611863-->



### Propiedades del producto cartesiano #flashcard
![[Propiedades del producto cartesiano.png]]
 
<!--ID: 1700071611867-->



## Relación binaria #flashcard
- Una relación binaria entre los elementos de los conjuntos 𝐴 y 𝐵 es cualquier subconjunto del producto cartesiano 𝐴 × 𝐵
ℛ = {(𝑥, 𝑦) ∈ 𝐴 × 𝐵/𝑥ℛ}
 
<!--ID: 1700071611871-->



## Conjuntos importantes en producto cartesiano #flashcard
- A es el conjunto inicial de la relación.
- B es el conjunto de llegada de la relación.
- Dominio de la relación: es el conjunto que tiene como elementos los primeros componentes de los pares ordenados de la relación.
- Imagen de la relación: es el conjunto que tiene como elementos los segundos componentes de los pares ordenados de la relación.
![[Conjuntos importantes en producto cartesiano(Ejemplo).png]]
 
<!--ID: 1700071611875-->


## Relación definida en un conjunto #flashcard
Es cualquier relación definida a partir del producto cartesiano 𝐴 × 𝐴. El conjunto de salida es igual al conjunto de llegada.
 
## ¿Cómo se llaman los conjuntos de un solo elemento? #flashcard 
Conjuntos unitarios
<!--ID: 1700071611879-->
