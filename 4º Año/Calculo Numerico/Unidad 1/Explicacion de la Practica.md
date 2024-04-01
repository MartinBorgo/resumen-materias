
#### Ejercicio 1

Encuentre las cotas para $x$, siendo $x$ es una aproximación de $\pi$, y siendo $x$ una aproximación de $e$.
1. Truncando a 4 dígitos significativos.
2. Redondeo simétrico de 4 dígitos significativos.

Para cada uno de estos casos voy a aplicar las inecuaciones correspondientes y despejar en este caso la $x$ que sería nuestra aproximación, en ese caso cuando $x$ es una aproximación de $\pi$, la cuota de truncamiento sería:

$$
|\frac{\pi - x}{\pi}| \leq 10^{-4 + 1}
$$
$$
-10^{-3} \leq \frac{\pi - x}{\pi} \leq 10^{-3}
$$
$$
-10^{-3} \cdot \pi \leq \pi - x \leq 10^{-3} \cdot \pi
$$
multiplico por $-1$ para cambiar el signo de $x$:
$$
10^{-3} \cdot \pi \geq -\pi + x \geq -10^{-3} \cdot \pi
$$
Multiplico una vez más por $-1$ para que queden ordenados de menor a mayor:
$$
-10^{-3} \cdot \pi \leq -\pi + x \leq 10^{-3} \cdot \pi
$$
$$
\pi - 10^{-3} \cdot \pi \leq x \leq \pi + 10^{-3} \cdot \pi
$$
$$
3.141592 -0.001 \cdot 3.141592 \leq x \leq 3.141592 + 0.001 \cdot 3.141592
$$
$$
3.13845 \leq x \leq 3.14473
$$

>[!note] Nota
>El mismo procedimiento se debe aplicar para resolver la cuota de redondeo simétrico, con la diferencia que en este caso se debe aplicar si propia inecuación. En el caso del redondeo simétrico la "fórmula", aplicada al caso anterior es: 
>$$
|\frac{\pi - x}{\pi}| \leq 5 . 10^{-4}
$$

#### Ejercicio 2

¿Cuál es el error absoluto y el error relativo; al aproximar $P$ con $P^*$ considerando los siguientes valores de $P$ y $P^*$?.

1. $P = \pi$ $P^*=3.1$
2. $P=\frac{\pi}{1000}$ $P^*=0.0031$
3. $P=\frac{1}{3}$ $P^*=0.333$
4. $P=\frac{100}{3}$ $P^*=33.3$

Para encontrar el error absoluto y el error relativo, tenemos que ignorar las fórmulas que aparecen en la teoría y usar las siguientes:

$$
\text{Error Absoluto} = |x - \overline{x}|
$$
$$
\text{Error Relativo} = \frac{|x - \overline{x}|}{|x|}
$$

En donde:
- $x$ es el valor exacto.
- $\overline{x}$ es la aproximación a $x$.

>[!note] Error Relativo Porcentual
>En caso de que se quiera saber el error realtivo porcentual, solo se tiene que multiplicar el resultado por 100 y ya esta.

En este caso los dos primeros puntos nos quedarían:

1. $$ \frac{|\pi - 3.1|}{|\pi|} = \frac{0.04159}{\pi} = 0.01324 \rightarrow 0.01324 \times 100 = 1.324\% $$
2. $$\frac{|\frac{\pi}{1000}-0.0031|}{|\frac{\pi}{1000}|}= \frac{0.000041}{\frac{\pi}{1000}} = 0.01323 \rightarrow 0.01323 \times 100 = 1.323\%$$
Como el error absoluto es el numerador, al calcular el error relativo, ya estamos calculando el error absoluto al mismo tiempo.

#### Ejercicio 3

¿Con cuántas cifras significativas aproxima $P^*$ a $P$ en el ejercicio anterior?

Para este punto se tiene que construir las cotas de redondeo simétrico, con $t=i$, donde $i$ es un número que comienza desde $1$, una vez se hayan construido varias cotas se va a observar si el valor de $P^*$ de cada punto anterior está dentro de esa cotas.
Tomemos como ejemplo al punto 1 del ejercicio anterior, en ese caso construiremos 3 colas de redondeo simétrico, para cunado $t=1$, $t=2$ y $t=3$. Pero primero tratemos de resolver la inecuación:

$$
|\frac{\pi -p^*}{\pi}| \leq 5 \cdot 10^{-t}
$$
$$
-5 \cdot 10^{-t} \leq \frac{\pi -p^*}{\pi} \leq 5 \cdot 10^{-t}
$$
$$
-5 \cdot 10^{-t} \cdot \pi \leq \pi -p^* \leq 5 \cdot 10^{-t} \cdot \pi
$$
$$
5 \cdot 10^{-t} \cdot \pi \geq -\pi +p^* \geq -5 \cdot 10^{-t} \cdot \pi
$$
$$
-5 \cdot 10^{-t} \cdot \pi \leq -\pi +p^* \leq 5 \cdot 10^{-t} \cdot \pi
$$
$$
\pi -5 \cdot 10^{-t} \cdot \pi \leq p^* \leq \pi + 5 \cdot 10^{-t} \cdot \pi
$$
Una vez despejado $p^*$ lo único que deberemos hacer es reemplazar la $t$ por 1, 2 y 3, quedándonos las siguientes cotas:

$$ t = 1 \rightarrow 1.57079 \leq p^* \leq 4.71238 $$
$$ t = 2 \rightarrow 2.98451 \leq p^* \leq 3.29867 $$
$$ t = 3 \rightarrow 3.12588 \leq p^* \leq 3.15730 $$
Lo que se hace ahora es evaluar si el valor de $p^*$, en este caso $3.1$, está incluido en las cotas, y como podemos ver el valor de $p^*$ entra en la cota de $t = 1$ y $t = 2$, pero no en la de $t = 3$, ya que $3.1$ es menor que $3.12$. En ese caso $p^*$ aproxima a $p$, con 2 cifras significativas. Esto es así, ya que siempre se toma la cota con el $t$ más alto.

La forma general la podemos tomar de la siguiente manera:
$$
p -5 \cdot 10^{-t} \cdot p \leq p^* \leq p + 5 \cdot 10^{-t} \cdot p
$$
#### Ejercicio 4

Efectúe los siguientes cálculos de forma exacta, usando aritmética de redondeo truncado de tres dígitos y usando aritmética de redondeo simétrico de tres dígitos. Luego determine las pérdidas de dígitos significativos suponiendo que los números dados son exactos.

1. 14,1+0,0981
2. 0,0218\*179
3. (164+0,913)-(143+21)
4. (164-143)+(0,913-21)

En este caso resolvamos el punto 1 y 4 como para ver ejemplos de todo:

1. $14,1+0,0981 = 14,1981$
	1. Resultado exacto -> $14,1981$
	2. Redondeo Truncado -> $14,1$
	3. Redondeo Simétrico -> $14,2$

3. $(164-143)+(0,913-21) = 21 - 20.087 = 0.913$
	1. Resultado exacto -> $0.913$
	2. Redondeo Truncado -> $0.91$
	3. Redondeo Simétrico -> $0.91$

Luego para determinar cuantos dígitos significativos perdieron cada uno de esos resultados, se debe hacer lo mismo que el punto 3, es decir, sé calculan las cotas para $t=i$ y en este caso como se tenía que redondear a 3 dígitos si uno de los valores calculados en la primera parte de este ejercicio entra en la cota de $t=1$ entonces perdió dos dígitos significativos, en caso de que entre en la cota de $t=2$ solo perderá un dígito significativo.
