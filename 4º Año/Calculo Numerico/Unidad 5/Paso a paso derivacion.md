### Fórmula Central y Lateral primera derivada

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
### Derivada Segunda $f''(x)$

#### Fórmula Central

$$
f''(x) \approx \frac{f(x+h) - 2f(x) + f(x-h)}{h^2}
$$

#### Fórmula Lateral hacia Adelante

$$
f''(x) \approx \frac{f(x + 2h) - 2f(x + h) + f(x)}{h^2}
$$

### Derivada Tercera $f'''(x)$

#### Fórmula Central

$$
f'''(x) \approx \frac{f(x+2h) - 2f(x+h) + 2f(x-h) - f(x-2h)}{2h^3}
$$

#### Fórmula Lateral hacia Adelante

$$
f'''(x) \approx \frac{f(x + 3h) - 3f(x + 2h) + 3f(x + h) - f(x)}{h^3}
$$

### Derivada Cuarta $f''''(x)$

#### Fórmula Central

$$
f''''(x) \approx \frac{f(x+2h) - 4f(x+h) + 6f(x) - 4f(x-h) + f(x-2h)}{h^4}
$$

#### Fórmula Lateral hacia Adelante

$$
f''''(x) \approx \frac{f(x + 4h) - 4f(x + 3h) + 6f(x + 2h) - 4f(x + h) + f(x)}{h^4}
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

Usando la fórmula lateral hacia adelante, sustituyendo los valores:

$$
f'(25^\circ) \approx \frac{0.8660 - 0.9063}{0.5236 - 0.4363} \approx \frac{-0.0403}{0.0873} \approx -0.4615
$$

### Paso 4: Derivada central

Usando la fórmula central, sustituyendo los valores:

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

# Derivación Numérica - Ejercicio 2

Problema a)
Dada la función:

$$
f(x) = x^3 \cdot e^{x^2} - \sin(x)
$$

Queremos aproximar la derivada $f'(2.19)$ usando la fórmula central con $h = 0.1$.

### Paso 1: Calcular $f(x+h)$ y $f(x-h)$

Primero, calculamos los valores de $x+h$ y $x-h$:

$$
x+h = 2.19 + 0.1 = 2.29
$$
$$
x-h = 2.19 - 0.1 = 2.09
$$

Ahora, calculamos $f(x+h)$ y $f(x-h)$.

1. **Calcular $f(2.29)$**:

   $$
   f(2.29) = (2.29)^3 \cdot e^{(2.29)^2} - \sin(2.29)
   $$
   $$
   f(2.29) \approx 12.0143 \cdot e^{5.2441} - \sin(2.29)
   $$
   $$
   f(2.29) \approx 12.0143 \cdot 188.5931 - 0.7501
   $$
   $$
   f(2.29) \approx 2265.21
   $$

2. **Calcular $f(2.09)$**:

   $$
   f(2.09) = (2.09)^3 \cdot e^{(2.09)^2} - \sin(2.09)
   $$
   $$
   f(2.09) \approx 9.1187 \cdot e^{4.3681} - \sin(2.09)
   $$
   $$
   f(2.09) \approx 9.1187 \cdot 78.7635 - 0.8632
   $$
   $$
   f(2.09) \approx 718.57
   $$

### Paso 2: Calcular $f'(2.19)$

Usamos la fórmula central para calcular la derivada:

$$
f'(2.19) \approx \frac{f(2.29) - f(2.09)}{2 \cdot 0.1}
$$

Sustituyendo los valores calculados:

$$
f'(2.19) \approx \frac{2265.21 - 718.57}{0.2}
$$

$$
f'(2.19) \approx \frac{1546.64}{0.2} \approx 7733.20
$$

### Resultado final

La aproximación de la derivada $f'(2.19)$ usando la fórmula central con $h = 0.1$ es:

$$
f'(2.19) \approx 7733.20
$$
