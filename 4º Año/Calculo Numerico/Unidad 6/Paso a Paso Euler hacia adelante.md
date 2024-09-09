**Este es el ejercicio 1) a) del  TP ecuaciones diferenciales.**

El primer paso es resolver la ecuación diferencial de forma manual utilizando el método de **Euler hacia adelante**. Este método aproxima la solución de una ecuación diferencial $y' = f(t, y)$ a partir de un valor inicial $y(0)$ y un paso $h$.
### Datos proporcionados:
- Ecuación diferencial: $y' = -20y + 7e^{-0.5t}$
- Condición inicial: $y(0) = 5$
- Paso: $h = 0.01$
- Intervalo: $0 \leq t \leq 0.02$

El método de Euler hacia adelante tiene la siguiente fórmula:
$y_{n+1} = y_n + h f(t_n, y_n)$

Donde:
- $y_n$ es el valor aproximado de $y$ en el paso $n$.
- $f(t_n, y_n)$ es la función que define la derivada de $y$ en el paso $n$, es decir, $f(t_n, y_n) = -20y_n + 7e^{-0.5t_n}$.

### Paso 1: Calcular para $t = 0$ (punto inicial)
- $t_0 = 0$
- $y_0 = 5$ (condición inicial)

La derivada en este punto es:

$f(0, 5) = -20(5) + 7e^{0} = -100 + 7 = -93$

Ahora aplicamos la fórmula de Euler:
$y_1 = y_0 + h f(0, 5) = 5 + 0.01(-93) = 5 - 0.93 = 4.07$

### Paso 2: Calcular para $t = 0.01$
- $t_1 = 0.01$
- $y_1 = 4.07$

La derivada en este punto es:
$f(0.01, 4.07) = -20(4.07) + 7e^{-0.5(0.01)} = -81.4 + 7e^{-0.005} \approx -81.4 + 6.965 \approx -74.435$
Aplicamos nuevamente la fórmula de Euler:
$y_2 = y_1 + h f(0.01, 4.07) = 4.07 + 0.01(-74.435) = 4.07 - 0.74435 \approx 3.32565$

| Paso $n$ | $t_n$ | $y_n$   |
| -------- | ----- | ------- |
| 0        | 0.00  | 5.00000 |
| 1        | 0.01  | 4.07000 |
| 2        | 0.02  | 3.32565 |
