### Ejercicio 3 - Estimación de la integral con la regla del Trapecio y Simpson

Vamos a resolver el ejercicio para estimar el valor de la integral en el intervalo $[1.0,1.4]$, aplicando los métodos del **Trapecio** y **Simpson** con paso de cálculo $h=0.1$

| **x**    | 1.0   | 1.1   | 1.2   | 1.3   | 1.4   |
| -------- | ----- | ----- | ----- | ----- | ----- |
| **f(x)** | 0.010 | 0.252 | 0.586 | 1.024 | 1.578 |

1. **Fórmula de la regla del trapecio**:
$$
\int_{x_0}^{x_n} f(x) dx \approx h \left[ \frac{1}{2}(y_0 + y_n) + \sum_{i=1}^{n-1} y_i \right]
$$

2. **Fórmula de la regla de Simpson**:
$$
\int_{a}^{b} f(x) dx \approx \frac{h}{3} \left[ y_0 + 2 \sum_{i=2, \text{pares}}^{n-2} y_i + 4 \sum_{i=1, \text{impares}}^{n-1} y_i + y_n \right]
$$
### **1. Regla del Trapecio**:

Aplicamos la fórmula del trapecio:

$$
\int_{1.0}^{1.4} f(x) dx \approx 0.1 \left[ \frac{1}{2}(0.010 + 1.578) + (0.252 + 0.586 + 1.024) \right]
$$

Primero calculamos los términos:

$\frac{1}{2}(0.010 + 1.578) = \frac{1.588}{2} = 0.794$

$0.252 + 0.586 + 1.024 = 1.862$

Sustituyendo:
$\int_{1.0}^{1.4} f(x) dx \approx 0.1 \left[ 0.794 + 1.862 \right] = 0.1 \times 2.656 = 0.2656$

El valor aproximado de la integral utilizando la regla del Trapecio es:

$$
\mathbf{0.2656}
$$
### **2. Regla de Simpson**:

Aplicamos la fórmula de Simpson:

$$
\int_{1.0}^{1.4} f(x) dx \approx \frac{0.1}{3} \left[ 0.010 + 2(0.586) + 4(0.252 + 1.024) + 1.578 \right]
$$

Calculamos los términos:

$2(0.586) = 1.172$
$4(0.252 + 1.024) = 4 \times 1.276 = 5.104$

Sustituyendo:
$\int_{1.0}^{1.4} f(x) dx \approx \frac{0.1}{3} \left[ 0.010 + 1.172 + 5.104 + 1.578 \right] = \frac{0.1}{3} \times 7.864$

Finalmente:
$\int_{1.0}^{1.4} f(x) dx \approx 0.26213$

El valor aproximado de la integral utilizando la regla de Simpson es:
$$
\mathbf{0.26213}
$$
