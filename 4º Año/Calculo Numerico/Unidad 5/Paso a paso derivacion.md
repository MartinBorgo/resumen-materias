### a) Fórmula Central y Lateral

Las fórmulas para la derivación numérica son:

1. **Fórmula Central**:
   $$
   f'(x) \approx \frac{f(x+h) - f(x-h)}{2h}
   $$
   donde $h$ es un pequeño incremento.

2. **Fórmula Lateral hacia Adelante**:
   $$
   f'(x) \approx \frac{f(x+h) - f(x)}{h}
   $$
## Cálculo de $f'(25^\circ)$ para $f(x) = \cos(x)$
### Paso 1: Convertir los ángulos a radianes

$$
\text{radianes} = \frac{\text{grados} \times \pi}{180}
$$

- $x_1 = 20^\circ = \frac{20 \times \pi}{180} \approx 0.3491 \, \text{rad}$
- $x_2 = 25^\circ = \frac{25 \times \pi}{180} \approx 0.4363 \, \text{rad}$
- $x_3 = 30^\circ = \frac{30 \times \pi}{180} \approx 0.5236 \, \text{rad}$

### Paso 2: Calcular $f(x) = \cos(x)$ para cada $x$

$$
f(x_1) = \cos(0.3491) \approx 0.9397
$$

$$
f(x_2) = \cos(0.4363) \approx 0.9063
$$

$$
f(x_3) = \cos(0.5236) \approx 0.8660
$$

### Paso 3: Derivada lateral hacia adelante

Usando la fórmula lateral hacia adelante:

$$
f'(x_2) \approx \frac{f(x_3) - f(x_2)}{x_3 - x_2}
$$

Sustituyendo los valores:

$$
f'(25^\circ) \approx \frac{0.8660 - 0.9063}{0.5236 - 0.4363} \approx \frac{-0.0403}{0.0873} \approx -0.4615
$$

### Paso 4: Derivada central

Usando la fórmula central:

$$
f'(x_2) \approx \frac{f(x_3) - f(x_1)}{x_3 - x_1}
$$

Sustituyendo los valores:

$$
f'(25^\circ) \approx \frac{0.8660 - 0.9397}{0.5236 - 0.3491} \approx \frac{-0.0737}{0.1745} \approx -0.4223
$$

### Paso 5: Tabla de Resultados

| $x$ | $x$ (radianes) | $f(x) = \cos(x)$ | Derivada lateral $f'(25^\circ)$ | Derivada central $f'(25^\circ)$ |
| --- | -------------- | ---------------- | ------------------------------- | ------------------------------- |
| 20º | 0.3491 rad     | 0.9397           | -                               | -                               |
| 25º | 0.4363 rad     | 0.9063           | -0.4615                         | -0.4223                         |
| 30º | 0.5236 rad     | 0.8660           | -                               | -                               |
## Resultado

- **Derivada lateral hacia adelante en $25^\circ$**: $f'(25^\circ) \approx -0.4615$
- **Derivada central en $25^\circ$**: $f'(25^\circ) \approx -0.4223$
