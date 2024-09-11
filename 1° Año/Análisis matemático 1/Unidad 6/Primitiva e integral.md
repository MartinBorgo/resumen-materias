# Anki
TARGET DECK: Facultad:: Sistemas:: Primer año:: Análisis matemático 1:: Unidad 6
# Archivos y videos
![[Primitiva de una función 2023.pptx]]


# Notas

## Primitiva de una función y ejemplo #flashcard
Antiderivada de una función definida o integral. Ejemplo, x^4 -> 4x^3
<!--ID: 1690150646330-->


## Propiedades de la integral definida #flashcard
1. Cambia de signo si se permutan los límites de integración
2. Si los límites coinciden, la integral es cero.
3. Si c es el punto medio del intervalo [a,b], la integral definida se puede descomponer como la suma de integrar [a,c] + [c,b]
4. La integral de la suma de funciones es igual a la suma de integrales.
5. La integral del producto de una constante es igual a la constante por la integral
<!--ID: 1690150646335-->


## Integración por descomposición #flashcard
∫(f(x)+g(x)) = ∫f(x) + ∫g(x)
<!--ID: 1690150646339-->


## Integración por sustitución #flashcard
∫(f^n.f´) = ((f^n+1)/n+1) + k
∫((3x^2+5x)^6. (6x+5)) = ((3x^2+5x)^7/7) + k
<!--ID: 1690150646345-->


## Integración por partes #flashcard
∫u.dv = u.v-∫v.du
Como no existe una fórmula para encontrar la primitiva de un producto y si una de las funciones es inmediatamente integrable, se cumple lo siguiente:
(f g)´ = f´g + fg´
∫(fg)´ = ∫(f´g) + ∫(fg´)
fg + k = ∫(f´g) + ∫(fg)´
∫(f´g) = fg - ∫(fg´) + k
Ejemplo.
∫(xlnx) = ∫((x^2/2)(1/x))
(x^2/2)lnx-∫x/2 = (x^2/2)lnx-1/2∫x
(x^2/2)lnx-(x^2/4)+k
<!--ID: 1690150646352-->


## Integración de funciones racionales #flashcard
Para integrar el cociente de funciones polinómicas y el grado del numerador es mayor que el del denominador se debe realizar la división
1. Las raíces del denominador son reales y simples. El denominador se expresa como producto de diferentes polinomios lineales reales.
∫1/(x^2-x-6) -> (A1/x-3) + (A2/x+2)
Para calcular los valores de A1 y A2, tome un denominador común en el segundo miembro
Los numeradores son iguales.
Entonces, ∫1/(x^2-x-6) = 1/5 ∫1/(x-3) - 1/5 ∫1/(x+2) = 1/5 ln |x-3| - 1/5 ln |x+2| + k = ln 5√|(x-3)/(x+2)| +k
2. Las raíces del denominador son reales y múltiples. El denominador se expresa como producto de polinomios lineales, algunos repetidos.
3. El denominador tiene raíces complejas, no reales, simples. Al factorizar el denominador aparecen polinomios cuadráticos irreducibles, todos diferentes entre sí.
4. El denominador tiene raíces múltiples, complejas y no reales. Aparecen factores cuadráticos irreducibles repetidos en la factorización
<!--ID: 1690150646358-->

