# Anki
TARGET DECK: Facultad::  Sistemas:: Primer año:: Algoritmos y programación:: Unidad 1
# Archivos
![[Clase 01 - 2022-v2 (1).pdf]]
![[Clase 00 - Parte 2 - 2022 - Lenguajes de Programación1.pdf]]
![[Clase 00 - 2022 - Atributos-Ligaduras.pdf]]
# Notas

## ¿Qué es un algoritmo y de qué tipo existen? #flashcard
- Una serie de pasos (acciones) organizados que describe el proceso que se debe seguir, para dar solución a un problema específico.
- Naturales y computacionales
<!--ID: 1700071329631-->

## Esquema secuencial #flashcard
![[Esquema de control secuencial.png]]
<!--ID: 1700071329635-->

## Esquemas de control #flashcard
![[Esquemas de control selectivo.png]]
- En el esquema selectivo se diferencia entre simple y doble (si, sino)
<!--ID: 1700071329640-->

## ¿Cómo construimos algoritmos? #flashcard
- Utilizando:
- Elementos: Objetos válidos (Alfabeto).
- Esquemas: Estructuras válidas para combinar elementos (Sintaxis)
<!--ID: 1700071329645-->

## ¿Cuáles son los elementos de un algoritmo? #flashcard
- Acciones y condiciones
<!--ID: 1700071329650-->

## ¿Qué es un lenguaje de programación? #flashcard
- Un Lenguaje de Programación es un conjunto de reglas, notaciones, símbolos y/o caracteres que, mediante la aplicación de una gramática permite al usuario (programador) expresar su pensamiento y resolver un problema en una computadora.
<!--ID: 1700071329654-->

### ¿Qué es la gramática de un lenguaje de programación y cuáles sus partes? ¿Cómo se describe un lenguaje? #flashcard
Son las reglas del lenguaje.
1. Sintaxis ¿Cómo está compuesto?
	1. Forma del lenguaje
2. Semántica ¿Qué significan?
	1. Significado del lenguaje
3. Pragmática ¿Qué hace?
	1. Uso práctico
<!--ID: 1700071329663-->

## ¿Cómo se clasifican los lenguajes y cuáles son sus propiedades? #flashcard
| Naturales                                     | Formales                           |
| --------------------------------------------- | ---------------------------------- |
| Propiedad polisémica (Distintos significados) | Se desarrolla partir de una teoría |
| Enriquecimiento progresivo                    | Semántica mínima                   |
| Dificultad de formalización completa          | Sin ambigüedad                     |
| Lenguaje humano                               | Lenguaje de programación           |
<!--ID: 1700071329669-->

## ¿Cómo se clasifican los lenguajes de programación? #flashcard
![[Clasificación de lenguajes de programación.png]]
<!--ID: 1700071329674-->

### Bajo nivel

#### Primera generación de lenguajes #flashcard
- Dependen de la máquina
- Instrucción a instrucción
- Poco legibles
<!--ID: 1700071329678-->

#### Segunda generación de lenguajes #flashcard
- Concepto de abstracción
- Nombres simbólicos
- Poco legibles
<!--ID: 1700071329683-->

### Lenguajes de alto nivel
#### ¿Cuáles son las características y ventajas de los lenguajes de alto nivel? #flashcard
Características:
- Macro instrucciones
- Nombres simbólicos
- Lenguajes multipropósito y específicos
- Lenguajes multiplataforma
Ventajas:
- Fácil aprender y escribir
- Mejor documentación
- Mejor mantenimiento
<!--ID: 1700071329687-->

#### ¿En base a qué arquitectura se basan los lenguajes más populares y cuáles son sus características? #flashcard
Arquitectura de von Neumann. 
1. Datos y programas almacenados en memoria. 
2. Memoria y CPU separados
3.  Entubamiento “piping”
4.   Concepto de variable. 
5.   Asignación de datos. 
6.   Esquema de control de iteración.
<!--ID: 1700071329691-->

## ¿Cuál es el esquema de comunicación entre programa fuente y programa ejecutable? #flashcard
![[Esquema de comunicación entre programa fuente y programa ejecutable.png]]
<!--ID: 1700071329695-->

## Ciclo de vida del software #flashcard
1. Especificación y análisis de requerimientos
	1. Análisis de factibilidad
	2. Identificar y documentar los requerimientos exactos del Sistema 
	3.  ¿Cuál? Es el problema. ¿Qué? Debe realizar el sistema. 
	4.  Alcance del Sistema 
	5.  Resultado de la fase: documento de especificación de requerimientos
2. Diseño de software
	1. ¿Cómo? Resolver el problema. 
	2. Definición de la arquitectura del sistema
	3. El método elegido puede afectar la elección del lenguaje utilizado.
	4. Resultado de la fase: documento de especificación de diseño.
3. Codificación e implementación
	1. Elección de una forma de codificación ajustada al diseño. 
	2. Resultado de la fase: sistema implementado y documentado.
4. Verificación y evaluación
	1. • Evaluación de la calidad de la implementación del sistema. 
		1. ¿Estamos creando correctamente el producto? 
		2.  ¿Estamos creando el producto correcto? • 
	2.  Testeo de módulos y testeo de integración entre módulos
5. Mantenimiento
	1. • Previsión de cambios. 
		1. Funcionamiento incorrecto. •
		2. Adición de nuevas capacidades o mejora de las existentes. 
		3. Adaptación a nuevos ambientes operacionales.
<!--ID: 1700071329699-->

## Paradigma #flashcard
- Modelo computacional para desarrollar programas que solucionen problemas reales
<!--ID: 1700071337263-->

### Paradigmas procedurales y no procedurales #flashcard
- Procedurales
	- Sentencias que modifican el estado de un programa (PHP, Java, etc.)
	- Se especifican las acciones de un programa
- No procedurales
	- Se describe la lógica para resolver un problema (Lisp, Miranda)
	- No se necesita definir algoritmos
<!--ID: 1700071329703-->


### ¿Qué otros paradigmas existen? #flashcard
- Concurrente
	- Técnicas de paralelismo entre tareas para problemas de comunicación y sincronización (Java)
- Orientado a eventos
	- Dependen de los sucesos del sistema, se puede interactuar con el usuario en cualquier momento (Javascript)
- Orientado a aspectos
	- Separar funcionalidades del sistema para generar independencia entre módulos (AspectJ)
<!--ID: 1700071329707-->


## Paradigma imperativo o algorítmico #flashcard
- Un programa con una secuencia de instrucciones para indicar el flujo de la ejecución
<!--ID: 1700071329711-->


### Características del paradigma imperativo #flashcard
- Concepto de celda de memoria
- Operaciones de asignación
- Tipos de datos
- Estructuras de control
<!--ID: 1700071329715-->


## Tipos de paradigma imperativo #flashcard
- No estructurado
	- Libertad para definir datos como y donde pareciera mejor
	- Libertad para escribir instrucciones de salto (**goto**)
		- Código Spaghetti
		- Crisis de los ´70
- Estructurado
	- Sistema de Tipos
	- Conjunto de instrucciones básicas para **bloques de instrucción**
<!--ID: 1700071329719-->


## ¿Cuáles son las componentes fundamentales del paradigma imperativo? #flashcard
1. Secuencia y estructuras de control
2. Concepto de variable
3. Tipos de datos 
4. Operación de asignación
<!--ID: 1700071329723-->


## Algoritmo+Estructura de datos=? #flashcard
Programa
<!--ID: 1700071329727-->


## ¿Qué es una entidad? #flashcard
Es una variable, constante, subprograma, sentencia, expresiones, etc.
<!--ID: 1700071329731-->


## ¿Qué es un atributo? #flashcard
Propiedades de una entidad
<!--ID: 1700071329735-->


## ¿Qué es una ligadura? #flashcard
Asociar un atributo a una entidad
<!--ID: 1700071329740-->


### ¿Qué es el tiempo de ligadura , qué tipos hay y para qué se usan? #flashcard
Es el momento en el que ocurre la ligadura
1. Ligadura dinámica (durante) (flexibilidad) (desarrollo rápido)
2. Ligadura estática (antes) (segura) (desarrollo complejo)
<!--ID: 1700071329748-->


