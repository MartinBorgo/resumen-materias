# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Algoritmos y programación:: Unidad 7
# Archivos
![[Clase 28 - Recursividad-2021-Parte 1.pdf]]
![[Clase 28 - Recursividad-2021-Parte 2.pdf]]

# Notas

## Recursividad #flashcard
Método alternativo a esquema repetitivo en el cual un subprograma puede invocarse a sí mismo. Se utiliza una condición de final (Stop)
<!--ID: 1700070990425-->


### Algoritmo divergente #flashcard
- Subprograma que no contempla condición final
- Genera error en ejecución. "overflow"
<!--ID: 1700070990431-->


### Ventajas y desventajas de la recursividad #flashcard
| Ventajas                                  | Desventajas              |
| ----------------------------------------- | ------------------------ |
| Soluciona problemas recurrentes           | Ineficiencia de recursos |
| Programas menos extensos                  | Problemas de "overflow"  |
| Facilita la comprención de modularización |                          |
<!--ID: 1700070990436-->


### Ejemplo algorítmico recursivo sumando los primeros 5 naturales #flashcard
Procedure UNO
	Si x < 5
		Con := Con + 1
		Res := Res + Con
		UNO
	FinSi
Fin-Procedimiento UNO
BEGIN
	Res, Con := 0
	UNO
	Imprimir RES
FIN
<!--ID: 1700070990441-->


### Concepto de concurrencia #flashcard
Dos procesos son concurrentes cuando la primera instrucción de uno se ejecuta después de la primera del otro y antes de la última
<!--ID: 1700070990446-->


## Concepto de programación paralela #flashcard
Cuando ejecutan al mismo tiempo dos proceso
<!--ID: 1700071007023-->
