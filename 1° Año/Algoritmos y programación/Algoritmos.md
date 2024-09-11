# Primer cuatrimestre
## 25/03
Algoritmos y programación. FCAD. UNER.
Problemas:
1. Ingresar tres números enteros por teclado, luego sumar los dos primeros y al resultado restarle el tercero. Imprimir el resultado
2. Ingresar cuatro números enteros por teclado, multiplicar la suma de los dos primeros por la suma de los dos últimos e imprimir el resultado.
3. Ingresar el sueldo mensual de un empleado de cada uno  los primeros 6 meses de un aNo e imprimirlos. Luego imprimir el promedio mensual
4. Se ingresa la base y la altura de un rectángulo. Se debe calcular e imprimir su perímetro y superficie (área)
5. A un inquilino le informan que el alquiler que paga se incrementará un 10% Codificar un algoritmo para que, ingresando el alquiler que pagó el mes pasado, calcule e imprima el nuevo importe del alquiler
6. Ingresar el importe de la compra de un cliente en un supermercado. Calcular un descuento del 10% sobre el importe de la compra e imprimir el importe neto resultante

### 1
```
Program SUM
	Var
		N1, N2, N3, SUM, RES: integer;
	Inicio
		Ingresar N1, N2, N3
		SUM = N1+N2
		RES = SUM-N3
		Imprimir RES
	Fin
```
### 2
```
Program MUL
	Var
		N1, N2, N3, N4, SUM1, SUM2, MUL: integer
	Inicio
		Ingresar N1, N2, N3, N4
		SUM1 = N1 + N2
		SUM2 = N3 + N4
		MUL = SUM1 *SUM2
		Imprimir MUL
	Fin
```
### 3
```
Program PROM
	Var
		DEV1, DEV2, DEV3, DEV4, DEV5, DEV6, PROM: Real
	Inicio
		Ingresar DEV1, DEV2, DEV3, DEV4, DEV5, DEV6
		PROM = (DEV1 + DEV2 + DEV3 + DEV4 + DEV5 + DEV6) / 6
		Imprimir "Sus sueldos son: ", DEV1, DEV2, DEV3, DEV4, DEV5, DEV6
		Imprimir "Su promedio es: ", PROM
	Fin
```
### 4
```
Program PER AR
	Var
		A, B, AR, PER: Real
	Inicio
		Ingresar A, B
		AR = A*B
		PER = 2*(A+B)
		Imprimir "La superficie es: ", AR
		Imprimir "El perímetro es: ", PER
	Fin
```
### 5
```
Program INMO
	Var
		ALQUI, RES: Real
	Inicio
		Ingresar ALQUI
		RES = ALQUI*1,1
		Imprimir "El nuevo valor del alquiler es: ", RES
```
### 6
```
Program SUPER
	Var
		IMP, RES: Real
	Inicio
		Ingresar IMP
		RES = IMP*0,9
		Imprimir "El importe neto resultante es: ", RES
	Fin
```
## 28/03
Se requiere ingresar el número de documento y el nombre de los 235 alumnos de Algoritmos y programación e imprimir un listado de todos ellos
```
Program Alumnos
	Var
		cont, DNI: integer
		Nom: string
	Inicio
		cont = 0
		Repetir
			Ing Nom, DNI
			Imp Nom, DNI
			cont = cont + 1
		Hasta que cont = 235
	Fin
```
## 29/03
Se ingresa por teclado la edad de un alumno, se requiere imprimir un texto que diga "Es mayor de edad" cuando lo sea

```
Program Mayor
	Var
		Edad:integer
	Inicio
		Ing Edad
		Si Edad >= 18
			Imp "Es mayor de edad"
		FinSi
	Fin
```
## 05/04
Se ingresa por teclado los siguientes datos de los 1255 libros que tiene una persona en su biblioteca

Título del libro

Autor

Código de origen: (1-Comprado, 2-Regalado, 3-Prestado)

Se requiere ingresar los datos e imprimir un listado. Cuando finaliza el ingreso de datos se debe imprimir la cantidad de libros prestados que tiene la persona en su biblioteca.
```
Program biblio
	Var
		Tit, Aut: string
		P, i, c: integer
	Inicio
		p=0
		Para i = 1, 1255, 1
			Ing Tit, Aut, c
			Si c=3
				p=p+1
			FinSi
			Imp Tit, Aut, c
		FinPara
		Imp p
	Fin
```
Se ingresa el Nombre, número de documento y edad de las personas internadas en un Hospital. Imprimir un listado que incluya los datos ingresados.

Cuando finaliza el ingreso de datos imprimir la cantidad total de personas internadas y la cantidad de personas internadas mayores de 60 aNos.

El proceso finaliza cuando ingresa un número de documento igual a cero.
```
Program Hospital
	Var
		Nom: string
		DNI, Edad, Tot, Tot60: integer
	Inicio
		Tot, Tot60 := 60
		Ing DNI
		Mientras DNI <> 0
			Ing Nom, Edad
			Imp Nom, Edad, DNI
			Tot= Tot + 1
			Si Edad > 60
				Tot60= Tot60 + 1
			FinSi
			Ing DNI
		Fin Mientras
		Imp Tot, Tot60
	Fin
```
### **Ejercicio TP 1.1**

Se ingresan los siguientes datos de los inscriptos para asistir a un curso de capacitación:

-   **NDoc - Número de Documento**
    
-   **ApeN - Apellido y Nombre**
    
-   **CCod – Código de Categoría (1-Alumno, 2-Docente, 3-Otros)**
    

  

Se Requiere:

a) Ingresar por teclado los datos de los inscriptos.

b) Imprimir listado de los datos ingresados.

c) Al finalizar el proceso imprimir el total de inscriptos en el curso y el total de alumnos inscriptos en el curso.

El ingreso de datos finaliza cuando ingresa un número de documento igual a Cero.
```
Program Curso
	Var
		NDOC, CCOD, Tot, TotA: integer
		ApeN: string
	Inicio
		Tot, TotA = 0
		Ing DNI
		Mientras DNI <> 0
			Ing ApeN, CCOD
			Imp ApeN, CCOD, DNI
			Tot = Tot + 1
			Si CCOD = 1
				TotA = TotA + 1
			FinSi
			Ing DNI
		FinMientras
		Imp Tot, TotA
	Fin
```
### **Ejercicio TP 1.2**

Para procesar los datos del personal de una empresa que debe pagar un incremento de sueldo, se requiere:

a) Ingresar los siguientes datos de cada empleado

-   **- Ndoc – Número de Documento**
    
-   **- Nom – Nombre el empleado**
    
-   **- Sueldo – Sueldo Básico del empleado**
    

  

b) Imprimir un listado con los datos que ingresan que contenga:

**N°Documento – Nombre – Sueldo – Incremento**

* El incremento a pagar es el 12% del Sueldo Básico de cada empleado.

Al finalizar el proceso, imprimir:

a) Cantidad de empleados que tiene la empresa

b) Cantidad de empleados que cobran mas de $ 25,000 de incremento.

Nota: El ingreso de datos finaliza cuando ingresa un número de documento igual a cero.
```
Program Inc Sueldo
	Var
		Ndoc, Tot, Tot25: integer
		Nom: string
		Sueldo, Inc: Real
	Inicio
		Tot, Tot25 = 0
		Ing Ndoc
		Mientras Ndoc <> 0
			Ing Nom, Sueldo
			Inc = Sueldo*0,12
			Imp = Ndoc, Nom, Sueldo, Inc
			Tot = Tot + 1
			Si Inc > 25000
				Tot25 = Tot25 + 1
			FinSi
			Ing Ndoc
		FinMientras
		Imp Tot, Tot25
	Fin
```
### **Ejercicio TP 1.3**

  Se ingresan los siguientes datos de los docentes de la carrera de Licenciatura en Sistemas:

-   **DocNom – Nombre del Docente**
    
-   **DocCat – Código de Categoría (1-Titular, 2-Asociado, 3-Adjunto)**
    

Se debe:

- Imprimir un listado con los datos ingresados

- Imprimir la cantidad de docentes discriminados por código de categoría.

El ingreso de datos finaliza cuando en lugar de un nombre de docente el operador digita la letra “F”.
```
Program Docentes
	Var
		DocNom: string
		DocCat, C1, C2, C3: integer
	Inicio
		C1, C2, C3 = 0
		Ing DocNom
		Mientras DocNom <> "F"
			Ing DocCat
			Imp DocNom, DocCat
			Si DocCat = 1
				C1=C1+1
			Sino
				Si DocCat=2
					C2=C2+1
				Sino
					C3=C3+1
			FinSi
			Ing DocNom
		FinMientras
		Imp C1, C2, C3
	Fin
```
### **Ejercicio TP 1.4**

  

Una distribuidora que vende productos informáticos al por mayor debe procesar las entregas de pendrives que vende a distintos comercios. De cada entrega se ingresa por teclado:

-   **- Marca - Marca del pendrive**
    
-   **- Capa – Capacidad en Gb (-Puede ingresar: 16, 32 o 64-)**
    
-   **- Canti - Cantidad de unidades vendidas**
    
-   **- Precio - Precio Unitario**
    

Se requiere:

a) Imprimir de cada venta que ingresa los siguientes datos:

**Marca – Cantidad de Unidades – Importe de la venta**

* El importe de la venta se obtiene multiplicando el precio unitario por la cantidad de unidades vendidas.

Al finalizar el proceso, imprimir:

a) Importe total vendido.

b) Cantidad de unidades vendidas discriminadas por capacidad en Gb.

Nota: El ingreso de datos finaliza cuando al solicitar el ingreso de la marca de una venta, el operador digita la letra «F»
```
Program Distribuidora
	Var
		Marca: string
		Capa, Canti, C1, C2, C3: integer
		Precio, Imp, ImpT: Real
	Inicio
		C1, C2, C3, ImpT = 0
		Ing Marca
		Mientras Marca <> "F"
			Ing Capa, Canti, Precio
			Imp = Canti*Precio
			Imp Marca, Canti, Imp
			ImpT = ImpT + Imp
			Si Capa = 16
				C1=C1+1
			Sino
				Si Capa=32
					C2=C2+1
				Sino
					C3=C3+1
			FinSi
			Ing Marca
		FinMientras
		Imp ImpT, C1, C2, C3
	Fin
```
## 07/04
La administración de un restaurante necesita implementar un sistema que le permita obtener información relacionada con el funcionamiento del mismo. Para ello al final del día ingresan por teclado los siguientes datos de cada mesa ocupada durante el día:

-   NME - Número Mesa
-   CAN - Cantidad de personas
-   MOZ - Número Mozo (1 a 3 )
-   IMC - Importe total consumido por la mesa

Se requiere: Imprimir un listado de los datos ingresados que contenga:

Nº Mesa – Nº Mozo– Imp total consumición – Imp comisión mozo

El porcentaje para calcular el importe de comisión para el mozo es de 5% sobre el importe de la consumición.

Al finalizar el ingreso de los datos:

a)Cantidad de mesas atendidas con más de 6 personas

b)Importe total recaudado en el día.

c) Importe total de comisión a cobrar discriminado por mozo

```
Program adminresto
	Var
		NME, CAN, MOZ, M6: integer
		IMC, IMCM, IT, IT1, IT2, IT3: Real
	Inicio
		IT, IT1, IT2, IT3, M6 := 0
		Ingresar NME
		Mientras NME <> 0
			Ing CAN, MOZ, IMC
			Si CAN > 6
				M6 = M6 + 1
			FinSi
			IT = IT+IMC
			Si MOZ = 1
				IT1 = IT1 + IMC
			Sino
				Si MOZ = 2
					IT2 = IT2 + IMC
				Sino
					IT3 = IT3 + IMC
			FinSi
			IMCM = IMC*0,05
			Imp NME, MOZ, IMC, IMCM
			Ing NME
		FinMientras
		Imp M6, IT, IT1, IT2, IT3
	Fin
```

## 12/04
### **Ejercicio TP 2.1**
En un stand de una feria de libros se está vendiendo un «best seller» de un conocido autor. De cada venta que se realiza se ingresa:

-   **LibNom – Nombre de la persona que compra**
-   **LibCan – Cantidad de libros comprados**

Se debe imprimir un tiket de venta que contenga:

**Nombre del comprador – Cantidad Libros – Importe de la Compra**

El importe de la compra se calcula multiplicando la cantidad de libros comprados por el precio unitario del libro que debe ingresarse UNA SOLA VEZ, al inicio del algoritmo.

El ingreso de datos finaliza cuando en lugar de un nombre de comprador el operador digita la letra “F”.
```
Program BestSeller
	Var
		LibNom: string
		LibCan, Imp, Pu: Real
	Inicio
		Ing LibNom, Pu
		Mientras LibNom <> "F"
			Ing LibCan
			Imp = LibCan*Pu
			Imp Lib LibNom, LibCan, Imp
			Ing LibNom
		FinMientras
	Fin
```


**Ejercicio TP 2.2**

  

Una Estación de servicio que vende gasoil para productores de soja, requiere implementar un software que contemple:

a) Ingresar los siguientes datos de cada venta de gasoil de un surtidor

-   **- GasFec – Fecha de la venta**
-   **- GasSur – Número de Surtidor (rango de 1 a 3)**
-   **- GasCal – Cantidad de litros vendidos**

b) Imprimir un listado con los datos que ingresan que contenga:

**N°Surtidor – Cantidad Litros Vendidos – Importe de la Venta**

Para calcular el importe de la venta se debe multiplicar la cantidad de litros vendidos por el precio del litro de gasoil, cuyo valor ingresa UNA SOLA VEZ, al inicio del algoritmo.

c) Al finalizar el proceso, imprimir la cantidad total de litros vendidos discriminados por número de surtidor.

Nota: El ingreso de datos finaliza cuando ingresa una fecha igual a cero

```
Program Ps
	Var
		GasFec: string
		GasSur, GasCal, PG, Imp, S1, S2, S3: Real
	Inicio
		S1, S2, S3 = 0
		Ing PG, GasFec
		Mientras GasFec <> 0
			Ing GasSur, GasCal
			Imp = GasCal*PG
			Imp GasSur, GasCal, Imp
			Si GasSur = 1
				S1 = S1 + GasCal
			Sino
				Si GasSur = 2
					S1 = S2 + GasCal
				Sino
					S3 = S3 + GasCal
			FinSi
			Ing GasFec
		FinMientras
		Imp S1, S2, S3
```

**Ejercicio TP 2.3**
Para participar en un campeonato universitario de futbol femenino, la FCAd debe enviar la lista de deportistas al Comité de la Organización. Se requiere:

a) Ingresar los siguientes datos de cada jugadora:

-   **- JugDoc – Número de Documento**
-   **- JugNom – Nombre de la jugadora**
-   **- JugEda – Edad de la jugadora (en aNos)**
-   **- JugCop – Código de puesto (1-Arquera, 2-Defensora, 3-Mediocampo, 4-Delantera)**

b) Imprimir un listado con los datos que ingresan que contenga:

**N°Documento – Nombre – Edad**

Al finalizar el proceso, imprimir:

a) Cantidad total de jugadoras que integran la delegación discriminada por código de puesto.

b) Cantidad de jugadoras menores de 20 aNos.

Nota: El ingreso de datos finaliza cuando ingresa un número de documento igual a cero.
```
Program Campeonato
	Var
		A, B, C, D, JugDoc, JugEda, JugCop, J20: integer
		JugNom: string
	Inicio
		A, B, C, D, J20 = 0
		Ing JugDoc
		Mientras JugDoc <> 0
			Ing JugNom, JugEda, JugCop
			Imp JugDoc, JugNom, JugEda
			Si JugEda < 20
				J20 = J20 + 1
			FinSi
			Si JugCop = 1
				A = A + 1
			Sino
				Si JugCop = 2
					B = B + 1
				Sino
					Si JugCop = 3
						C = C + 1
					Sino
						D = D + 1
			FinSi
		Ing JugDoc
		FinMientras
		Imp A, B, C, D, J20
	Fin

```
## 19/04
**Ejercicio TP 3.1**
«MetaData» es una empresa que brinda cursos de capacitación de lenguajes de programación. Tiene abierta la inscripción de dos cursos: PHP y Phyton. Por cada alumno que se inscribe se ingresa:

-   **CurDoc – Número de documento del alumno**
-   **CurNom – Nombre del alumno**
-   **CurCoc – Código de curso al que se inscribe (1-PHP, 2-Phyton)**

Se debe imprimir un recibo para el alumno que contenga:

**Nombre del Alumno– Curso al que se inscribe – Importe de la matrícula**

El importe de la matrícula de cada uno de los cursos (que son distintos) se deben ingresarse UNA SOLA VEZ, al inicio del algoritmo.

Al finalizar el ingreso de datos se debe imprimir la cantidad de alumnos inscriptos discriminado por código de curso.

El ingreso de datos finaliza cuando en lugar de un número de documento el operador digita un número cero

```
Program Metadata
	Var
		CurDoc, CurCoc, Pphp, Pphy, Imp, C1, C2: Real
		CurNom: string
	Inicio
		C1, C2 = 0
		Ing CurDoc, Pphp, Pphy
		Mientras CurDoc <> 0
			CurNom, CurCoc
			Si CurCoc = 1
				C1 = C1 + 1
				Imp Pphp, "Se inscribe al de PHP ", CurNom
			Sino
				Imp Pphy, "Se inscribe al de phyton", CurNom
				C2 = C2 + 1
			FinSi
			Ing CurDoc
		FinMientras
		Imp C1, C2
	Fin
```

**Ejercicio TP 3.2**

  

«PocosKilos» es una clínica para personas que desean adelgazar. Debe procesar los resultados de los tratamientos a sus pacientes realizados en un mes. De cada paciente tratado se ingresa por teclado:

-   **PacNom - Nombre del Paciente**
    
-   **PacPei - Peso al iniciar el tratamiento (en Kg.)**
    
-   **PacPse – Peso al finalizar la segunda semana (en Kg)**
    
-   **PacPef - Peso al finalizar todo el tratamiento (en Kg)**
    

Se requiere:

Imprimir un listado que contenga:

**Nombre del Paciente – Kgs. que adelgazó durante el tratamiento**

Al finalizar el proceso se debe imprimir:

- Cuantos pacientes adelgazaron mas de 20 Kgs. en total

- Cuantos pacientes iniciaron el tratamiento con mas de 120 kgs.

- Cantidad de pacientes tratados.

- Cantidad de pacientes que adelgazaron mas de 10 kgs. al finalizar la segunda semana del tratamiento.

**Nota**: El ingreso de datos finaliza cuando ingresa un nombre igual a «F».

```
Program PocosKilos
	Var
		PacNom: string
		PacPei, PacPse, PacPef, PacPA, P20, P120, PT, P10: Real
	Inicio
		PacPA, P20, P120, PT, P1 := 0
		Ing PacNom
		Mientras PacNom <> "F"
			Ing PacPei, PacPse, PacPef
			PacPA = PacPei - PacPef
			Imp PacNom, PacPA
			Si PacPA > 20
				P20 = P20 + 1
			FinSi
			Si PacPei > 120
				P120 = P120 + 1
			FinSi
			PT = PT + 1
			PA = PacPei - PacPse
			Si PA > 10
				P10 = P10 +1
			FinSi
			Ing PacNom
		FinMientras
		Imp P20, P120, PT, P10
	Fin
```

**Ejercicio TP 3.3**

  

Para la emisión de la boleta de pago del impuesto inmobiliario provincial, se ingresan los siguientes datos de cada contribuyente:

-   **ImpCod - Código de inmueble**
    
-   **ImpTit - Titular del inmueble**
    
-   **ImpSup - Superficie del inmueble (en metros cuadrados).**
    
-   **ImpCod - Código de ubicación (1-Residencial, 2-Complementaria)**
    

Se requiere imprimir los datos de cada contribuyente que contenga:

**Código de Inmueble – Titular – Superficie – Importe del Impuesto**

El cálculo del importe del impuesto se determina de la siguiente manera:

Para ubicación residencial: $ 50,- por cada metro cuadrado

Para ubicación complementaria: $ 35 por cada metro cuadrado.

Al final del proceso imprimir el Importe total que deben pagar los contribuyentes discriminados por código de ubicación.

El proceso finaliza cuando el operador ingresa un código de inmueble igual a cero.
```
Program Impuesto
	Var
		ImpCod, ImpSup, ImpUb, Imp, I1, I2: Real
		Imp Tit: string
	Inicio
		I1, I2 := 0
		Ing ImpCod
		Mientras ImpCod <> 0
			Ing ImpTit, ImpSup, ImpUb
			Si ImpUb = 1
				Imp = ImpSup*50
			Sino
				Imp = ImpSup*35
			FinSi
			Imp ImpCod, ImpTit, ImpSup, Imp
			Si ImpUb = 1
				I1 = I1 + Imp
			Sino
				I2 = I2 + Imp
			FinSi
			Ing ImpCod
		FinMientras
		Imp I1, I2
	Fin
```
## 26/04
**Ejercicio clase 6.1**

  

En una librería se debe procesar las ventas que se realizan. Se requiere codificar los siguientes procesos:

a) Ingresar por teclado los siguientes datos de cada venta:

-   **NTike – Nro. de tiket**
-   **TArt Tipo de artículo vendido (1-Libro, 2-revista)**
-   **Impo - Importe de la venta**

b) Imprimir un listado de todos los ingresos que contenga:

**Nro. de Tiket – Tipo Artículo – Importe venta**

c) Cuando finaliza el ingreso de datos se debe imprimir:

- Importe total vendido.

- Importe total vendido discriminado por tipo de artículo.

- Nro. de Tiket al que corresponde el mayor importe vendido.

El ingreso de datos finaliza cuando se ingresa un Nro. de Tiket igual a cero.

```
Program Lib
	Var
		ID2, NTike, TArt, Impo, IT, ID, TikM, TikMN: Real
	Inicio
		ID, IT := 0
		TikM = low_value
		Ing NTike
		Mientras NTike <> 0
			Ing TArt, Impo
			Imp NTike, TArt, Impo
			IT = Impo + IT
			Si TArt = 1
				ID = ID + Impo
			FinSi
			Si Impo > TikM
				TikMN = NTike
			FinSi
			Ing NTike
		FinMientras
		ID2 = IT - ID
		Imp IT, ID, ID2, TikMN
	Fin
```  

**Ejercicio clase 6.2**

  

En un negocio de venta de artículos electrónicos, cada vez que se concreta una venta por parte de uno de sus vendedores, se ingresan los siguientes datos:

-   **Nope - Número de operación**
    
-   **Desc - Descripción del producto vendido**
    
-   **Cpago - Código de pago (1-Contado, 2-T. Crédito, 3-T. Débito)**
    
-   **Impo - Importe cobrado**
    

Con los datos que ingresan se requiere:

a) Imprimir un comprobante que debe contener:

**Descripción del producto vendido – Código de Pago – Importe cobrado.**

b) Al final del proceso imprimir:

- Importe total vendido discriminado por código de pago

- Número de operación que corresponde a la venta de mayor importe

El ingreso de datos finaliza cuando se ingresa un Número de operación igual a cero.

```
Program OP
	Var
		Nope, Cpago, Impo, I1, I2, I3, NopeM, ImpoM: Real
		Desc: string
	Inicio
		I1, I2, I3 := 0
		ImpoM = low_value
		Ing Nope
		Mientras Nope <> 0
			Ing Desc, Cpago, Impo
			Imp Desc, Cpago, Impo
			Si Cpago = 1
				I1 = I1 + Impo
			Sino
				Si Cpago = 2
					I2 = I2 + Impo
				Sino
					I3 = I3 + Impo
			FinSi
			Si Impo > ImpoM
				NopeM = Nope
			FinSi
			Ing Nope
		FinMientras
		Imp I1, I2, I3
	Fin

```
## 03/05
La Facultad debe procesar los datos de los alumnos ingresantes a las distintas carreras que se dictan en su sede Se requiere codificar los siguientes procesos:

a) Ingreso de datos de cada alumno inscripto: Se ingresa:

-   **NumDoc – Número de documento del alumno**
    
-   **NomAlu – Nombre del Alumno**
    
-   **CodCar – Código de Carrera (1=Sistemas, 2=portugués, 3=Contador, 4=Turismo, 5=Administración, 6=Tecnicatura Web)**
    
-   **FecNac – Fecha de nacimiento (formato aaaammdd)**
    

b) Imprimir un listado que contenga los siguientes datos.

**Nombre Alumno – Nro. de Documento – Código de Carrera**

c) Al finalizar el ingreso de todos los datos se debe imprimir:

- Cantidad total de alumnos inscriptos en Facultad discriminado por Código de área del conocimiento.

- Cantidad de alumnos inscriptos en Sistemas que nacieron antes del aNo 2000.

```
Program Facu
	Var
		NumDoc, CodCar, C1, C2, C3, C4, C5, C6, FecNac, F2: Real
		NomAlu: string
	Inicio
		C1, C2, C3, C4, C5, C6, F2 := 0
		Ing NumDoc
		Mientras NumDoc <> 0
			Ing NomAlu, CodCar, FecNac
			Imp NomAlu, NumDoc, CodCar
			Si FecNac < 20000101
				F2 = F2 + 1
			FinSi
			Según CodCar
				1 : C1 = C1 + 1
				2 : C2 = C2 + 1
				3 : C3 = C3 + 1
				4 : C4 = C4 + 1
				5 : C5 = C5 + 1
				6 : C6 = C6 + 1
			FinSegún
			Ing NumDoc
		FinMientras
		Imp C1, C2, C3, C4, C5, C6, F2
	Fin
```

**Ejercicio clase 7.2**

  

El área de mantenimiento de una represa hidroeléctrica necesita desarrollar un algoritmo que le permita procesar las tareas de reparación realizadas en cada una de sus 3 turbinas durante el mes de abril.

Para ello se ingresan por teclado los siguientes datos de cada reparación realizada:

-   **NUM -N° de turbina (1… 3)**
-   **DIA -Día del mes**
-   **TIE -Tiempo de reparación en Hs.**
-   **DES -Descripción de la falla**
-   **COS -Costo total de reparación**

Se requiere imprimir un listado que contenga:

**N.º de turbina – Descripción de la falla – Costo total reparación**

Al finalizar el ingreso de datos imprimir:

-   N.º de turbina y descripción de la falla de mayor costo
    
-   Tiempo total de reparación discriminado por N.º de turbinas
    
-   N.º de turbina que estuvo más tiempo sin funcionar por reparaciones

```
Program hidro
	Var
		NUM, NUMM, DIA: integer
		DES, DESM: string
		COS, COSM, TIE, TIE1, TIE2, TIE3: Real
	Inicio
		COSM = low_value
		TIE1, TIE2, TIE3 := 0
		Ing DIA
		Mientras DIA <> 0
			Ing NUM, TIE, DES, COS
			Imp, NUM, DES, COS
			Si COSM < COS
				COSM := COS
				NUMM := NUM
				DESM := DES
			FinSi
			Según NUM
				1 : TIE1 = TIE1 + TIE
				2 : TIE2 = TIE2 + TIE
				3 : TIE3 = TIE3 + TIE
			FinSegún
			Ing DIA
		FinMientras
		Imp NUMM, DESM, TIE1, TIE2, TIE3
		Si TIE1 > TIE2 and TIE1 > TIE3
			Imp "1"
		Sino
			Si TIE2 > TIE1 and TIE2 > TIE3
				Imp "2"
			Sino
				Imp "3"
		FinSi
	
```

## 11/05
Se ingresan los siguientes datos de un censo habitacional realizado en tres ciudades de la provincia:

-   **CodCiu – Código de ciudad (1-Concordia, 2-Paraná, 3-C.del Uruguay)**
-   **CenDom – Domicilio censado**
-   **CenTip – Tipo de ocupación (1-Propia, 2-Alquiler)**

Los datos ingresan ordenados por código de ciudad
Se requiere:
a) Ingresar los datos del censo e imprimir un listado que contenga los datos ingresados.

b) Cuando finaliza **el ingreso de los datos de una ciudad**, se debe imprimir la cantidad de domicilios censados discriminados por tipo de ocupación.

```
Program Censo 1
	Var
		CodCiu, CenTip, Aux, C1, C2: Real
		CenDom: string
	Inicio
		Ing CodCiu
		Mientras CodCiu <> 0
			C1, C2 = 0
			CodCiu = Aux
			Mientras CodCiu = Aux
				Ing CenDom, CenTip
				Imp CenDom, CodCiu
				Si CenTip = 1
					C1 = C1 + 1
				Sino
					C2 = C2 + 1
				FinSi
				Ing CodCiu
			FinMientras
			Imp C1, C2
		FinMientras
	Fin
```
**Ejercicio clase 8.2**

  

Se ingresan los siguientes datos de un censo habitacional realizado en tres ciudades de la provincia:

-   **CodCiu – Código de ciudad (1-Concordia, 2-Paraná, 3-C.del Uruguay)**
    
-   **CenDom – Domicilio censado**
    
-   **CenTip – Tipo de ocupación (1-Propia, 2-Alquiler)**
    

Los datos ingresan ordenados por código de ciudad

Se requiere:

a) Ingresar los datos del censo e imprimir un listado que contenga los datos ingresados.

b) Cuando finaliza **el proceso de todas las ciudades** se debe imprimir la cantidad de domicilios censados discriminados por tipo de ocupación

```
Program Censo2
	Var
		CodCiu, CenTip, Aux, C1, C2: Real
		CenDom: string
	Inicio
		Ing CodCiu
		C1, C2 = 0
		Mientras CodCiu <> 0
			CodCiu = Aux
			Mientras CodCiu = Aux
				Ing CenDom, CenTip
				Imp CenDom, CenTip, CodCiu
				Si CenTip = 1
					C1 = C1 + 1
				Sino
					C2 = C2 + 1
				FinSi
				Ing CodCiu
			FinMientras
		FinMientras
		Imp C1, C2
	Fin
```

**Ejercicio clase 8.3**

  

“El buen Diente”, es un negocio que vende empanadas y pizzas con entrega a domicilio. Los días lunes debe procesar las ventas que ha realizado a sus clientes durante la semana anterior. Se requiere codificar para procesar los datos de las compras realizadas durante el día:

a) Ingreso de datos de cada venta realizada:

-   **Fecha – Fecha de la venta**
    
-   **Domi - Domicilio donde se debe entregar la compra**
    
-   **Tipo – Tipo de producto (1-Empanada, 2-Pizza)**
    
-   **Impo – Importe cobrado al cliente.**
    

* Los datos ingresan agrupados por fecha de la venta

b) Imprimir un listado de todas las ventas que contenga:

**Domicilio donde se entrega la venta – Importe cobrado**

c) Cuando finalice el ingreso de los datos de una fecha, y antes de comenzar con los de la siguiente, se debe imprimir Importe total cobrado en dicho día discriminado por tipo de producto.
```
Program Pizza
	Var
		Fecha, Domi, Aux: string
		Tipo, Impo, IE, IP : Real
	Inicio
		Ing Fecha
		Mientras Fecha <> "F"
			Fecha := Aux
			IE, IP := 0
			Mientras Fecha = Aux
				Ing Domi, Tipo, Impo
				Imp Fecha, Domi, Tipo, Impo
				Si Tipo = 1
					IE = IE + Impo
				Sino
					IP = IP + Impo
				FinSi
				Ing Fecha
			FinMientras
			Imp IE, IP
		FinMientras
	Fin
```

## 12/05
**Ejercicio clase 8.4**

Una concesionaria de automóviles usados necesita desarrollar un algoritmo que le permita obtener información de los vehículos disponibles para la venta. Para ello ingresa por teclado los siguientes datos de cada vehículo:

**MAR – Marca del vehículo**

**PAT - Numero de patente**

**ANO – ANo de fabricación**

**TIP - Tipo de vehículo (1-Automóvil 2-Utilitario 3-Moto)**

**PRE – Precio de venta**

**KMS - Kilómetros**

El ingreso se realiza ordenado por MARCA del vehículo.

Con los datos ingresados se requiere:

a) Imprimir un listado de todos los vehículos ingresados que contenga:

**Numero de patente – Marca – Kilómetros - Precio Venta**

Se requiere:

1) Cuando finaliza **la impresión de los vehículos de una marca** y antes de comenzar con la siguiente se debe imprimir:

- Cantidad de vehículos discriminados por tipo.

2) Finalizado el proceso imprimir:

- Cantidad vehículos que NO superan los $ 1.000.000 de precio de venta.

- Cantidad total de vehículos disponibles para la venta

- Marca y aNo de fabricación del automóvil más caro.

```
Program Conces
	Var
		Mar, PAT, Maux, Mac: string
		ANO, TIP, PRE, KMS, T1, T2 , T3, V1, AD, AC, C: Real
	Inicio
		V1, AD := 0
		C := low_value
		Ing Mar
		Mientras Mar <> "F"
			Mar := Maux
			T1, T2, T3 = 0
			Mientras Mar = Maux
				Ing PAT, KMS, PRE TIP
				Imp PAT, Mar, KMS, PRE
				Si PRE < 1000000
					V1 = V1 + 1
				FinSi
				AD = AD + 1
				Si C < PRE
					C = PRE
					AC = ANO
					MaC := Mar
				FinSi
				Según TIP
					1 : T1 = T1 + 1
					2 : T2 = T2 + 1
					3 : T3 = T3 + 1
				FinSegún
				Ing Mar
			FinMientras
			Imp T1, T2, T3
		FinMientras
		Imp V1, VD, AD, MaC
	Fin
```

## 13/05
**Ejercicio clase 8.5**

La dirección de un colegio secundario desea procesar los resultados de los exámenes realizados por los alumnos. Para ello ingresa por teclado los siguientes datos:

-   **- (NM) N° de matrícula del alumno**
    
-   **- (CM) Código de materia**
    
-   **- (NO) Nota (rango de 1 a 10)**
    

El ingreso se realiza ordenado por N° de matrícula

Se requiere:

- Imprimir un listado con los datos ingresados

**Al finalizar un alumno y antes de comenzar con el siguiente**:

- Cantidad de materias rendidas por el alumno

- Promedio de notas

Por fin de proceso

- Imprimir cantidad de alumnos que rindieron

```
Program Secu
	Var
		AuxMt, NM, CM, NO, AM, CA, CaM, PROM, CN AuxMa: Real
	Inicio
		CA = 0
		Ing NM
		Mientras NM <> 0
			CA = CA + 1
			CN, CaM, PROM = 0
			Ing CM
			NM = AuxMa
			Mientras NM = AuxMa
				Mientras CM <> 0
					CM = AuxMt
					CaM = CaM + 1
					Mientras CM = AuxMt
						Ing NO
						Mientras NO <> 0
							Imp NM, CM, NO
							PROM = PROM + NO
							CN = CN + 1
							Ing NO
						FinMientras
						Ing CM
					FinMientras
				FinMientras
				Imp PROM, CaM
				Ing NM
			FinMientras
		FinMientras
		Imp CA
	Fin
```
**Ejercicio clase 8.6**

  

Una importadora cinematográfica provee películas a 15 distribuidoras. A fin de mes ingresa en una computadora los datos que corresponden a cada entrega efectuada. El ingreso se realiza ordenado por N° de distribuidora

-   **(ND) N° de distribuidora**
    
-   **(NR) N° de remito**
    
-   **(FE) Fecha de entrega**
    
-   **(CT) Código del título**
    
-   **(IMP) Importe**
    

Se necesita emitir un listado con los datos ingresados ordenados por N° de distribuidora.

**Al finalizar el ingreso de una distribuidora** y antes de procesar la siguiente imprimir:

- Cantidad de películas enviadas

- Importe a abonar por la distribuidora

Al finalizar el ingreso de datos mostrar:

- Cantidad total de películas comercializadas

- Importe total a cobrar
```
Program Cine
	Var
		ND, NR, CT, IMP, AuxND, CPE, ID, AuxCT, CTP, IT: Real
		FE: string
	Inicio
		CTP, IT = 0
		Ing ND
		Mientras ND <> 0
			ND = AuxND
			CPE, ID = 0
			Mientras ND = AuxND
				Ing CT
				Mientras CT <> 0
					CT = AuxCT
					Mientras CT = AuxCT
						Ing NR, FE, IMP
						ID = ID + IMP
						CPE = CPE + 1
						Imp ND, NR, FE, CT, IMP
						Ing CT
					FinMientras
				FinMientras
			FinMientras
			Imp CPE, ID
			CTP = CTP + CPE
			IT = IT + ID
		FinMientras
		Imp IT, CTP
	Fin
```
## 24/05

**Ejercicios clase 9**

  Generar un vector de nombre “Vector” de 100 elementos que contenga valor 0 en todos sus elementos, a excepción en los elementos de la posición 60 y 77 que deben contener valor 9.

```CSS
	Program V100
		Var
			Vector = array [1..100] of integer;
			i : integer;
			Inicio
				Para i = 1, 100, 1
					Vector(i) := 0
					Si i = 60 or i = 77
						Vector(i) := 9
					FinSi
				FinPara
		Fin
```

Se tiene grabado en memoria un vector “Dato” de 120 elementos que contiene valores numéricos. Codificar un algoritmo por el cual:
a) se impriman todos los valores
b) al final se imprima la sumatoria de todos los los elementos.

```CSS
	Program D120
		Var
			D120 = array [1..120] of Real;
			i, sumatoria: Real;
		Inicio
			sumatoria = 0
			Para i = 1, 120, 1
				Imprimir D120(i)
				sumatoria = sumatoria + D120(i)
			FinPara
			Imprimir sumatoria
		Fin
```

Se tiene grabado en memoria un vector “Dato” de 180 elementos que contiene contiene valores numéricos reales. Codificar un algoritmo por el cual se imprima el elemento de mayor valor y su posición. 

```CSS
	Program D180Mayor
		Var
			Dato = array [1..180] of Real;
			i, pos: integer;
			MAY: Real;
		Inicio
			MAY := low_value
			Para i = 1, 180, 1
				Si MAY < Dato(i)
					MAY := Dato(i)
					pos := i
				FinSi
			FinPara
			Imprimir MAY, pos
		Fin
```

Se tiene grabado en memoria un array “Bebe” que contiene el peso de los 18 bebés nacidos en una clínica durante un día. Se debe:
a) se impriman todos los valores
b) al final se imprima el peso del bebé de menor peso


```CSS
	Program Bebe
		Var
			Bebe = array [1..18] of Real;
			i: integer;
			MEN: Real;
		Inicio
			MEN := high_value
			Para i = 1, 18, 1
				Imprimir Bebe(i)
				Si MEN > Bebe(i)  /*Acá compara*/
					MEN := Bebe(i)
				FinSi
			FinPara
			Imprimir "El bebé de menor peso es de", MEN, "kg"
		FIN
```

## 26/05

**Ejercicio clase 9.1**
1. Generar un vector de 350 posiciones que contenga los números naturales impares comenzando por el número 1. Luego, imprimirlos.

```CSS
	Program V350
		Var
			Impares = array [1..350] of integer;
			i: integer;
		Inicio
			Impares(1) = 1
			Para i = 2, 350, 1
				Impares(i) = Impares(i-1) + 2
			FinPara
			Para i = 1, 350, 1
				Imprimir Impares(i)
			FinPara
		Fin
```
2. Se tiene grabado en memoria un vector de 150 elementos de tipo string. Se requiere imprimir el contenido de los elementos ubicados en el rango 10 a 20 y entre 80 y 140.
```CSS
	Program V150
		Var
			V150 = array [1..150] of string;
			i: integer;
		Inicio
			Para i = 1, 150, 1
				Si i >= 10 and i <= 20 or i >= 80 and i <= 140
					Imprimir V150(i)
				FinSi
			FinPara
		Fin
```
3. Se tiene grabado en memoria un vector de 31 posiciones que contiene el importe de ventas diarias de cada día del mes de mayo. Se requiere mostrar el mayor importe y el día al que corresponde
```CSS
	Program V31
		Var
			V31 = array [1..31] of Real
			i, dia: integer;
			MayImpo: Real;
		Inicio
			MayImpo = low_value
			Para i = 1, 31, 1
				Si MayImpo < V31(i)
				MayImpo := V31(i)
				día := i
			FinPara
			Mostrar MayImpo, día
		Fin
```
## 31/05
### Enunciado
En una estación de servicio trabajan 18 empleados de playa (en la venta de Combustible) en distintos turnos. Se necesita procesar los datos de las ventas de un día. Se debe codificar el siguiente algoritmo:
a) Ingresar el nombre de los 18 empleados de playa
b) Ingresar los siguientes datos de cada venta realizada en el día
NroEmp : Número de empleado rango de 1 a 18
TipCom : tipo de combustible vendido 1-Nafta, 2-GasOil, 3-Kerosene
Impo : Importe de la venta.
Con los datos de cada venta imprimir:
Nombre del empleado – Importe de la venta
c) Al finalizar el ingreso de datos imprimir el importe total de ventas 
discriminados por tipo de combustible.
### Solución
```Pascal
Program 18Emp2.0
	Var
		NomEMP : array[1..18] of string
		TotCombs : array[1..3] of Real
		NroEmp : integer
		TipCom : integer
		Impo : Real
		i : integer
	Inicio
		Para i = 1, 3, 1
			TotCombs[i] := 0
		FinPara
		Ing NroEmp
		Mientras NroEmp <> 0
			Ingresar NomEMP[NroEmp], TipCom, Impo
			Imp NomEmp[NroEMP], Impo
			TotCombs[TipCom] += Impo
			Ing NroEmp
		FinMientras
		Para i = 1, 3, 1
			Imp TotCombs[i]
		FinPara
	Fin
```
### Enunciado
En una estación de servicio trabajan 18 empleados de playa (en la venta de Combustible) en distintos turnos. Se necesita procesar los datos de las ventas de un fin de semana largo. Se debe codificar el siguiente algoritmo:
b) Ingresar los siguientes datos de cada venta realizada por cada empleado: 
- Fecha : Fecha de la venta
- NroEmp : Número de empleado rango de 1 a 18
- TipCom : tipo de combustible vendido 1-Nafta, 2-GasOil, 3-Kerosene
- Impo : Importe de la venta.
Con los datos de cada venta imprimir:
Fecha – Tipo Combustible – Importe de la venta
c) Al finalizar el ingreso de datos imprimir el importe total de ventas que vendió cada empleado, con el formato:
Nro.de Empleado – Importe total vendido
### Solución
```Pascal
Program 18Emp2.0
 Var
 VecEmp: array(1..18) of real;
 NroEmp, TipCom, Fecha, Nro, i: integer;
 Impo: real;
Inicio
 Para Nro = 1, 18, 1
  VecEmp(Nro) := 0
  FinPara
 Ingresar Nro
 Mientras Nro <> 0
  Si Nro < 0 or Nro > 18
   Mostrar "El número ingresado está fuera de alcance"
   Sino
    Ingresar Fecha, TipCom, Impo
    Imprimir Fecha, TipCom, Impo
    VecEmp(Nro) = VecEmp(Nro) + Impo
  FinSi
  Ingresar Nro
 FinMientras
 Para i = 1, 18, 1
  Imprimir "Nro", i, "Importe", VecEmp(i)
 FinPara
Fin
```
## 02/06
### **Ejercicio clase 10.3**
Una empresa de transporte de pasajeros necesita procesar los datos obtenidos en cada uno de los servicios prestados durante el mes de Mayo. Para ello se ingresan por teclado los siguientes datos de cada viaje realizado :
**UNI _ Nº de unidad (1..32)**
**KMS_ Kilómetros recorridos**
**PAS _ Cantidad de pasajeros que viajaron**
**CHO_ Nº de chofer (1..3)**
**PRE _ Precio del pasaje**
**DES _ Destino**
Se requiere:
1) Imprimir un listado de los datos ingresados con el siguiente diseNo :
**Nº de Unidad - Destino - Cantidad de pasajeros – Importe total recaudado**
2) Finalizado el ingreso de datos imprimir:
a) Importe total recaudado discriminado por unidad
b) Cuantas veces viajaron más de 25 pasajeros
c) Nº de chofer y destino del viaje más largo
d) Promedio de pasajeros por viaje
e) Importe total recaudado en el mes por la empresa.
f) Nº de unidad que más recaudó en el mes.
g) Teniendo en cuenta que el consumo de combustible es de 12 litros cada 100 Km.
¿Cuántos litros de combustible consumieron el total de unidades?.
### Solución
```Pascal
Program Transporte
	Var
		UNIT : array[1..32] of Real
		M25 : integer
		NChofMax : integer
		DesMax : string
		KMSMax : integer
		ViajesTot : integer
		PasTot : integer
		PromPasV : Real
		ImpoTD : Real
		UniImpoMax : Real
		UniMax : integer
		ConsuCombT : Real
		UNI : integer
		KMS : Real
		PAS : integer
		CHO : integer
		PRE : Real
		DES : string
		i : integer
	Inicio
		M25 := 0
		KMSMax := low_value
		ViajesTot := 0
		PasTot := 0
		ConsuCombT := 0
		Para i = 1, 32, 1
			UNIT[i] := 0
		FinPara
		UniImpoMax := low_value
		Ingresar UNI
		Mientras UNI <> 0
			Ingresar KMS, PAS, CHO, PRE, DES
			ImpoT = PAS * PRE
			Imprimir UNI, DES, PAS, ImpoT
			UNIT[UNI] += ImpoT
			Si PAS > 25
				M25 += 1
			FinSi
			Si KMSMax < KMS
				KMSMax := KMS
				NChofMax := CHO
				DesMax := Des
			FinSi
			ViajesTot += 1
			PasTot += PAS
			ConsuCombT += KMS*12/100
			Ingresar UNI
		FinMientras
		Para i = 1, 32, 1
			Imprimir UNIT[i]
			Si UniImpoMax < UniT
				UniImpoMax := UniT
				UniMax := i
			FinSi
		FinPara
		Imprimir M25
		Imprimir NchofMax, DesMax
		PromPasV = PasTot/ViajesTot
		Imprimir PromPasV
		Imprimir UniMax
		Imprimir ConsuCombT
	Fin
```

## 07/06
### **Ejercicio clase 10.4**
Se deben procesar los datos de las ventas de libros en una Feria de Libros. En la feria existen 15 stands de distintas editoriales, y se deben codificar los siguientes procesos:
a) Ingresar el nombre de cada una de las 15 editoriales que tienen stand en la feria
b) Ingresar los siguientes datos de cada libro que se vende:
**Nro : Número de stand de la editorial donde se vendió (rango de 1 a 15)**
**TitLib : Titulo del libro**
**Impo : Importe de la venta**
De cada venta imprimir:
**Nombre de la Editorial - Titulo del libro – Importe**
c) Al final del proceso imprimir los importes totales de la venta discriminado por editorial
**Nombre de la Editorial - Importe de la venta** 

### Solución
```Pascal
Program Feria
	Var
		Edit : array[1..15] of string
		EditTot : array[1..15] of Real
		NRO : integer
		TitLib : string
		Impo : Real
		i : integer
	Inicio
		Para i = 1, 15, 1
			Ingresar Edit[i]
			EditTot[i] := 0
		FinPara
		Ingresar Nro
		Mientras Nro <> 0
			Si Nro < 1 or Nro > 15
				Mostrar "Fuera de rango"
			Sino
				Ingresar Nro, TitLib, Impo
				EditTot[i] += Impo
				Imprimir Edit[Nro], TitLib, Impo
			FinSi
			Ingresar TitLib
		FinMientras
		Para i = 1, 15, 1
			Imprimir Edit[i], EditTot[i]
		FinMientras
	Fin
```


### **Ejercicio clase 10.5**
Se deben procesar las ventas de una estación de servicio de un día, realizadas por cada uno de los 18 empleados de playa. Se requiere procesar:
a) Ingresar los nombres de los 18 empleados de playa
b) Ingresar los siguientes datos de cada venta:
-   **Nro : Número de empleado (rango de 1 a 18)**
-   **CodCom : Código de combustible (1-Nafta, 2-GasOil, 3-querosene)**
-   **CanLit : Cantidad de litros vendidos**
-   **Impo : Importe de la venta**
Al finalizar el proceso imprimir:
a) Importes totales de ventas discriminadas por empleado:
**Nombre del Empleado - Importe total vendido en el día**
b) Cantidad total de litros vendidos discriminados por código de combustible.
### Solución
```Pascal
Program Estación
	Var
		Nombres : array[1..18] of string
		ImpoTDía : array[1..18] of Real
		LitTot : array[1..3] of Real
		Nro : integer
		CodCom : integer
		CanLit : Real
		Impo : Real
		i : integer
	Inicio
		Para i = 1, 18, 1
			Ingresar Nombres[i]
			ImpoTDía[i] := 0
		FinPara
		Para i = 1, 3, 1
			LitTot[i] := 0
		FinPara
		Ingresar Nro
		Mientras Nro <> 0
			Si Nro < 1 or Nro > 18
				Mostrar "Fuera de rango"
			Sino
				Ingresar Nro, CodCom, CanLit, Impo
				ImpoTDía[Nro] += Impo
				LitTot[CodCom] += CanLit
			FinSi
			Ingresar Nro
		FinMientras
		Para i = 1, 18, 1
			Imprimir Nombres[i], ImpoTDía[i]
		FinPara
		Para i = 1, 3, 1
			Imprimir LitTot[i]
		FinPara
	Fin
```
## 09/06
### **Ejercicio clase 10.6**
La oficina central de aduanas necesita implementar un sistema que le permita procesar las operaciones de importación, realizadas durante el mes de Mayo en los 34 puestos aduaneros situados en distintos puntos del país. Se requiere:
1) Ingresar los nombres de cada puesto y guardarlos en una estructura de datos.
2) Ingresar por teclado los siguientes datos de cada operación de importación/exportación realizados durante el mes de Mayo:
-   **DIA _ Día del mes**
-   **NRO – Número de operación**
-   **TIP – Tipo de operación ( 1- Importación – 2 Exportación )**
-   **PUE _ Puesto de aduana (1..34)**
-   **IMP _ Importe de la operación**
De cada ingreso se debe imprimir :
**Día del mes – Nombre del puesto – Nº de operación – Impuesto abonado**
El impuesto se calcula en base al tipo de operación:
- Importación : 18 % sobre el importe de la operación - Exportación : 15 % sobre el importe de la operación
3) Al finalizar el ingreso de datos imprimir:
- Listado de todos los puesto con el siguiente diseNo:
**Nº de puesto – Nombre del puesto – Importe total de impuestos - Cantidad de operaciones realizadas en el mes**
- Nº y nombre del puesto que más impuestos recaudó en el mes
### Solución
```Pascal
Program aduana
	Var
		Puesto : array[1..34] of string
		ImpuT : array[1..34] of Real
		OpeT : array[1..34] of integer
		DIA : string
		NMAX : integer
		ImpuMAX : Real
		NRO : integer
		TIP : integer
		PUE : integer
		IMP : Real
		Impu : Real
		i : integer
	Inicio
		ImpuMAX := low_value
		Para i = 1, 34, 1
			Ingresar Puesto[i]
			ImpuT[i] := 0
			OpeT[i] := 0
		FinPara
		Ingresar DIA
		Mientras DIA <> "F"
			Ingresar NRO, TIP, PUE, IMP
			Si TIP = 1
				Impu = IMP*1,18
				ImpuT[i] += Impu
			Sino
				Impu = IMP*1,15
				ImpuT[i] += Impu
			FinSi
			OpeT[NRO] += 1
			Si ImpuMAX < Impu
				ImpuMAX := Impu
				NMAX := NRO
			FinSi
			Imprimir DIA, Puesto[NRO], NRO, Impu
			Ingresar DIA
		FinMientras
		Para i = 1, 34, 1
			Imprimir i, Puesto[i], ImpuT[i], OpeT[i]
		FinPara
		Imprimir NMAX, Puesto[NMAX]
	Fin
```
  
## 13/06

**Ejercicios TP (Clase 10)**

Catorce (14) inmobiliarias de una ciudad decidieron integrar una asociación con el fin de potenciar 
sus ventas y compartir recursos y gastos (publicidad en web, en medios, cartelería, etc.). 
La asociación necesita un sistema para gestionar las operaciones que realiza cada una, por lo cual 
se requiere la codificación de:
a) Ingresar el nombre de cada una de las 14 inmobiliarias.
b) Ingresar los datos de cada venta que realiza alguna inmobiliaria:
Nro = Número de inmobiliaria (rango de 1 a 14)
Tipo = Tipo de inmueble vendido (1-Terreno, 2-Casa, 3-Local Comercial, 4-Departamento, 5-Galpón Depósito)
Impo = Importe de la venta
De cada venta realizada se debe imprimir un comprobante que contenga:
- Nombre de la inmobiliaria
- Importe de la Venta
- Comisión que cobra la asociación (se aplica un 5% sobre el importe de la venta) 
c) Al finalizar el ingreso de datos se debe imprimir: 
1. Cantidad total de ventas realizadas discriminadas por tipo de inmueble vendido.
2. Un listado con los totales de ventas acumulados discriminados por inmobiliaria:
Nombre de la inmobiliaria – Importe total acumulado por ventas

Al finalizar el listado imprimir el nombre de la inmobiliaria que mayor importe acumulado 
por ventas registró.

```CSS
Program sociedad inmobiliaria
 Var
  Inmobiliaria = array [1..14] of: string;
  Tipos = array [1..5] of: integer;
  TotalImpo = array [1..14] of: Real;
  Nro, NroAux, Tipo, i: integer;
  Impo, comi, Mayor: Real;
  NomMayor: string;
 Inicio
  Mayor = low_value
  Para i = 1, 14, 1
      Ingresar Inmobiliaria(i)
  FinPara
  Para i = 1, 14, 1
   TotalImpo(i) = 0 
  FinPara
  Para i = 1, 5, 1
   Tipos(i) = 0
  FinPara
  Ingresar Nro
  Mientras Nro <> 0
   Nro = NroAux
   Mientras Nro = NroAux
    Ingresar Tipo, Impo
	TotalImpo(Nro) = TotalImpo(Nro) + Impo
	comi = Impo x 0,05
	Imprimir Inmobiliaria(Nro), Impo, comi
    Tipos(Tipo) = Tipos(Tipo) + 1
	Ingresar Nro
   FinMientras
  FinMientras
  Para i = 1, 5, 1
   Imprimir Tipo(i) 
  FinPara
  Para i = 1, 14, 1
   Imprimir Inmobiliaria(i), TotalImpo(i)
  FinPara
	Para i = 1, 14, 1
		Si TotalImpo(i) > Mayor
			Mayor = TotalImpo(i)
			NomMayor = Inmobiliaria(i)
		FinSi
	FinPara
	Imprimir NomMayor
 Fin
```

## 20/06
### Ejercicio
Para una solicitud de empleo que ha publicado una empresa, se han Presentado 56 postulantes. 
Se requiere: 
a) Ingresar los siguientes datos de cada postulante: 

- Apellido y Nombre - Número de Documento - Dirección de Contacto - Edad 

b) Finalizado el ingreso de datos, imprimir un listado: 

Apellido y Nombre – Nro.de Documento – Dirección - Edad

Al finalizar el listado imprimir el apellido y nombre del postulante de mayor edad.
### Solución
```
Program Postulantes 20-6
Type
	R-Postulantes = record
		R-ApeYNom : string;
		R-DNI : integer;
		R-Direc : string;
		R-Edad : integer;
Var
	i : integer;
	ApeYNomMAYOR : string;
	EdadMAYOR : integer;
	VecPostu: array[1..56] of R-Postulantes;
Inicio
	EdadMAYOR := low_value
	Para i = 1, 56, 1
		Ingresar VecPostu[i].R-ApeYNom
		Ingresar VecPostu[i].R-DNI
		Ingresar VecPostu[i].R-Direc
		Ingresar VecPostu[i].R-Edad
		Si EdadMAYOR < VecPostu[i].R-Edad
			EdadMAYOR = VecPostu[i].R-Edad
			ApeYNomMAYOR := VecPostu[i].R-ApeYNom 
		FinSi
	FinPara
	Para i = 1, 56, 1
		Imprimir VecPostu[i].R-ApeYNom, VecPostu[i].R-DNI, VecPostu[i].R-Direc, VecPostu[i].R-Edad
	FinPara
	Imprimir ApeYNomMAYOR
FIN
```

### Ejercicio
Dado el ejercicio anterior codificar los siguientes procesos: 
a) Imprimir la cantidad de postulantes de acuerdo con el siguiente rango de edades: 

- Menores de 30 aNos - Entre 31 y 40 aNos - Entre 41 y 50 aNos - Mas de 50 aNos 

b) Mostrar todos los datos de un aspirante cuyo número de documento ingresa el operador.

### Solución
```CSS
Var
	RanEdades : array[1..4] of integer;
	DocIng : integer;
	j : integer;
CALL Postulantes 20-6
Inicio
	Para i = 1, 56, 1
		Si VecPostu[i].R-Edad <= 30
			RanEdades[1] = RanEdades[1] + 1
		Sino
			Si VecPostu[i].R-Edad >= 31 and VecPostu[i].R-Edad <= 40
				RanEdades[2] = RanEdades[2] + 1
			Sino
				Si VecPostu[i].R-Edad >= 41 and VecPostu[i].R-Edad <= 50
					RanEdades[3] = RanEdades[3] + 1
				Sino
					RanEdades[4] = RanEdades[4] +1
				FinSi
	FinPara
	Para i = 1, 4, 1
		Imprimir RanEdades[i]
	FinPara
	Ingresar DocIng
	Para i = 1, 56, 1
		Si DocIng = VecPostu[i].R-DNI
			j := i
		Sino
			Mostrar "No encontrado"
		FinSi
	FinPara
	Imprimir VecPostu[j].R-ApeYNom, VecPostu[j].R-DNI, VecPostu[j].R-Direc, VecPostu[j].R-Edad
FIN
```
# Segundo cuatrimestre
## 08/08
### Ejercicio
Para una solicitud de empleo que ha publicado una empresa, se han presentado 56 postulantes. Se requiere:
a) Ingresar los siguientes datos de cada postulante:
- Nombre
- Número de documento
### Solución
```CSS
Program Aspirantes
    Type
        R-Aspira = record
            R-Nom : string
            R-Doc : integer
        end
    Var
        VecAsp = array [1..56] of R-Aspira
        i : integer
    Inicio
        Ingresar i
        Mientras i <> 0
            Ingresar VecAsp[i].R-Nom
            Ingresar VecAsp[i].R-Doc
            Ingresar i
        FinMientras
Fin
```
### Ejercicio
Para una solicitud de empleo que ha publicado una empresa, se han presentado 56 postulantes. Se requiere:
a) Ingresar los siguientes datos de cada postulante:
- Nombre
- Número de documento
- Dirección de contacto
- Edad
b) Finalizando el ingreso de datos, imprimir un listado:
Apellido y nombre - Nro. de documento - Dirección - Edad
Al finalizar el listado imprimir el apellido y nombre del postulante de mayor edad

### Solución
```CSS
Program Aspirantes 2.0
    Type
        R-Aspira = record
            R-Nom : string
            R-Doc : integer
            R-Direc : string
            R-Edad : integer
        end
    Var
        VecAsp = array [1..56] of R-Aspira
        PostuMAXEdad : integer
        PostuMAXNom : string
        i : integer
    Inicio
        Ingresar i
        PostuMAXEdad := low_value
        Mientras i <> 0
            Si i > 56 or i < 1
                Mostrar "Fuera de rango"
            Sino
                Ingresar VecAsp[i].R-Nom
                Ingresar VecAsp[i].R-Doc
                Ingresar VecAsp[i].R-Direc
                Ingresar VecAsp[i].R-Edad
                Si VecAsp[i].R-Edad > PostuMAXEdad
                    PostuMAXEdad := VecAsp[i].R-Edad
                    PostuMAXNom := VecAsp[i].R-Nom
                FinSi
            FinSi
            Ingresar i
        FinMientras
        Para i = 1, 56, 1
            Imprimir VecAsp[i].R-Nom, VecAsp[i].R-Doc, VecAsp[i].R-Direc, VecAsp[i].R-Edad
        FinPara
        Imprimir PostuMAXNom
Fin
```
### Ejercicio
Dado el ejercicio anterior, codificar los siguientes procesos:
a) Imprimir la cantidad de postulantes de acuerdo con el siguiente rango de edades:
- Menores de 30 aNos
- Entre 31 y 40 aNos
- Entre 41 y 50 aNos
- Más de 50 aNos
b) Mostrar todos los datos de un aspirante cuyo número de documento ingresa el operador

### Solución
```CSS
Program ConsultAspirantes 2.0
	Var
		RangoEdad = array [1..4] of integer
		DocIng : integer
		Z : boolean
	Inicio
		Para i = 1, 4, 1
			RangoEdad[i] = 0
		FinPara
		Para i = 1, 56, 1
			Si VecAsp[i].R-Edad < 30
				RangoEdad[1] = RangoEdad[1] + 1
				Sino
					Si VecAsp[i].R-Edad > 30 and VecAsp[i].R-Edad < 41
						RangoEdad[2] = RangoEdad[2] + 1
						Sino
							Si VecAsp[i].R-Edad > 40 and VecAsp[i].R-Edad < 51
								RangoEdad[3] = RangoEdad[3] + 1
								Sino
									RangoEdad[4] = RangoEdad[4] + 1
			FinSi
		FinPara
			Imprimir "Cantidad de postulantes menores de 30 aNos: ", RangoEdad[1]
			Imprimir "Cantidad de postulantes entre 31 y 40 aNos: ", RangoEdad[2]
			Imprimir "Cantidad de postulantes entre 41 y 50 aNos: ", RangoEdad[3]
			Imprimir "Cantidad de postulantes mayores de 50 aNos: ", RangoEdad[4]
		Mostrar "Ingrese un número de documento para mostrar los datos (0 Si desea cancelar): "
		Ingresar DocIng
		Mientras DocIng <> 0
			Para i = 1, 56, 1
				Si DocIng = VecAsp[i].R-Doc
					Mostrar "Nombre: ", VecAsp[i].R-Nom
					Mostrar "Número de documento: ", VecAsp[i].R-Doc
					Mostrar "Dirección: ", VecAsp[i].R-Direc
					Mostrar "Edad: ", VecAsp[i].R-Edad
					Z = True
				FinSi
			FinPara
			Si Z = False
			    Mostrar "Postulante no encontrado"
		    FinSi
		    Z = False
			Mostrar "Ingrese otro número de documento para mostrar los datos (0 Si desea cancelar): "
			Ingresar DocIng
		FinMientras
	Fin
```
## 09/08
### Ejercicio
Un aserradero necesita implementar un sistema que permita procesar los datos de las partidas de maderas recibidas durante el aNo 2021 hasta la fecha.
El algoritmo debe contemplar el ingreso por teclado de los datos correspondientes a cada una de las partidas, siendo estas 100.
Los datos que se ingresan son los siguientes:
NPAR - Número de partida [1..100]
FECHA - Fecha de ingreso
NOMVAR - Nombre de variedad
CANT - Peso de la partida en toneladas
El ingreso de datos se realiza sin seguir orden alguno y se debe utilizar la estructura (vector) para ser guardadas
Se requiere:
1) Imprimir un listado de todas las partidas ingresadas que contenga:
Nro de partida - Nombre variedad - Cantidad de toneladas
2) Al finalizar el listado debe imprimirse:
- Número de partida y nombre de la variedad de mayor peso
- Cantidad total de toneladas recibidas

### Solución
```CSS
Program AserraderoR
    Type
        R-Partida = record
            R-NOMVAR : string
            R-CANT : Real
        end
    Var
        NPAR = array [1..100] of R-Partida
        FECHA : string
        i : integer
        PesoMAX : Real
        NOMVARMAX : string
        NPARMAX : integer
        CANTTOTAL : Real
    Inicio
        CANTTOTAL := 0
        PesoMAX := low_value
        Ingresar FECHA
        Mientras FECHA <> "F"
            Para i = 1, 100, 1
                Ingresar NPAR[i].R-NOMVAR, NPAR[i].R-CANT
                Imprimir i,  NPAR[i].R-NOMVAR, NPAR[i].R-CAN
                Si NPAR[i].R-CANT > PesoMAX
                    PesoMAX := NPAR[i].R-CANT
                    NOMVARMAX := NPAR[i].R-NOMVAR
                    NPARMAX := i
                FinSi
                CANTTOTAL += NPAR[i].R-CANT
            FinPara
            Ingresar FECHA
        FinMientras
        Imprimir NPARMAX, NOMVARMAX
        Imprimir CANTTOTAL
    Fin
```
## 12/08
### Ejercicio
Prefectura Naval Argentina ha decidido realizar un reempadronamiento de los distintos tipos de embarcaciones que circulan en las distintas áreas navegables del país.
Para ello ingresa por teclado los siguientes datos de cada una de las 350 embarcaciones :
MAT _ Nº de matrícula
NOM _ Nombre del propietario 
MAR _ Marca 
ANO _ ANo de fabricación 
TIP _ Tipo de embarcación (rango de 1 a 16) 
Se requiere: 
1.- Ingresar los datos y guardarlos en una estructura de datos cuyo diseNo queda a criterio del programador. 
2- Finalizado el ingreso de datos imprimir un listado que contenga: 
Nº de matrícula – Nombre del propietario - Impuesto a pagar 
El impuesto a pagar se calcula de acuerdo a la antigüedad : 
Hasta 6 aNos – $ 2.800,00.- “ 
12 aNos – $ 2.200,00.- “ 
20 aNos - $ 1.100,00.- 
más de 20 aNos – No paga impuesto 
Al finalizar el listado imprimir : 
- Cantidad de embarcaciones procesadas discriminadas por tipo de embarcación. 
- Importe total de impuestos a pagar. 
3- Desarrollar un módulo de consulta donde ingresando el numero de matrícula, muestre por pantalla: 
Nombre propietario – Tipo de embarcación – ANo de fabricación
### Solución
```Pascal
Program Prefectura
    Type
        R-PRE = record
            MAT : integer
            NOM : string
            MAR : string
            ANO : integer
            TIP : integer
        end
    Var
        VPRE: array [1..350] of R-PRE
        VTIP: array [1..16] of integer
        Impu, TOTI : Real
        MAT, X, ANTI : integer
        Esta : boolean
    Inicio
        Para x = 1, 16, 1
            VTIP[x] = 0
        FinPara
        Ingresar x
        ​•Mientras x <> 0
            Si x < 0 or x > 350
                Mostrar "Fuera de rango"
                Sino
                    Ingresar VPRE[x].MAT, VPRE[x].NOM, VPRE[x].MAR, VPRE[x].ANO, VPRE[x].TIP
            FinSi
            Ingresar x
        FinMientras
        TOTI := 0
        Para x = 1, 16, 1
            ANTI := 2023 - VPRE[x].ANO
            Si ANTI < 7
                IMPU := 2800
            Sino
                Si ANTI < 13
                    IMPU := 2200
                Sino
                    Si ANTI < 21
                        IMPU := 1100
                    Sino
                        IMPU := 0
                    FinSi
                FinSi
            Finsi
            Imprimir VPRE(X).MAT, VPRE(X).NOM, IMPU
            TOTI := TOTI + IMPU
            VTIP[R-PRO[x].TIP] += 1
        FinPara
        Esta = False
        Para x = 1, 16, 1
            Imprimir x, VTIP(x)
        FinPara
        Imprimir "Impuestos total a pagar: ", TOTI
        Ingresar MAT
        Para x = 1, 350, 1
            Si MAT = R-PRO[x].TIP
                Imprimir R-PRO[x].NOM, R-PRO[x].TIP, R-PRO[x].ANO
            Finsi
            Si Esta = False
                Mostrar "No encontrado"
            Finsi
            Ingresar MAT
        FinPara
    FIN
```
## 16/08
### Ejercicio
El área de mantenimiento de una represa hidroeléctrica necesita desarrollar un algoritmo que le permita procesar las tareas de reparación realizadas en cada una de sus 14 turbinas durante el mes de julio. Para ello se ingresan por teclado los siguientes datos de cada reparación realizada:
TUR _ Nº de turbina 
DIA _ Día 
TIE _ Tiempo de reparación en Hs. 
FAL _ Código de falla 
COS _ Costo total de la reparación 
Se requiere : 
1) Ingreso de datos.
Ingresar los datos arriba detallados, y guardarlos en una estructura de datos:. 
2) Listado. 
Imprimir un listado de todas las reparaciones realizadas en el mes que contenga : 
Nº de turbina – Día – Costo total de la reparación.
Al finalizar el listado imprimir : 
- Nº de turbina y código de la falla de la reparación de mayor costo.
- Importe total de reparaciones del mes 
- Informe del mes discriminado por turbina que contenga :
Nº de turbina – Tiempo total fuera de servicio 
3) Consulta.
Desarrollar un módulo de consulta dónde ingresando el día del mes muestre por pantalla los datos de las reparaciones realizadas ese día
### Solución
```CSS
Program mantenimiento 2.0
	Type
		R-Turbina = record
			DIA = string
			TIE = Real
			FAL = integer
			COS = Real
		end
	Var
		TUR = array [1..31] of R-Turbina
		TIENOSERV = array [1..14] of Real
		x, TURMAX, FALMAX, DiaMes = integer
		IMPOMAX = Real
	Inicio
		Ingresar x
		Mientras x <> 0
			Si x < 1 or x > 31
				Mostrar "Fuera de rango"
			Sino
				Ingresar TUR[x].DIA, TUR[x].TIE, TUR[x].FAL, TUR[x].COS
			FinSi
			Ingresar x
		FinMientras
		Para x = 1, 31, 1
			Imprimir x, TUR[x].DIA, TUR[x].COS
		FinPara
	FIN
```
### Ejercicio
Prefectura Naval Argentina ha decidido realizar un reempadronamiento de los distintos tipos de embarcaciones que circulan en las distintas áreas navegables del país. Para ello ingresa por teclado los siguientes datos de cada una de las 350 embarcaciones:
- MAT _ Nº de matrícula 
- NOM _ Nombre del propietario 
- MAR _ Marca 
- ANO _ ANo de fabricación 

Se requiere:

1.- Ingresar los datos y guardarlos en una estructura de datos cuyo diseNo queda a criterio del programador. 

2- Finalizado el ingreso de datos imprimir un listado que contenga: 
Nº de matrícula – Nombre del propietario – Marca 

3- Desarrollar un módulo de consulta donde ingresando el numero de matrícula, muestre por pantalla: 
Nombre propietario – Marca de embarcación – ANo de fabricación

### Solución
```Pascal
Program Prefectura
	Type
		R-Embarcacion = record
			MAT = integer
			NOM = string
			MAR = string
			ANO = integer
		end
	Var
		EMB = array [1..350] of R-Embarcacion
		i, MatIng = integer
		x = false
	Inicio
		Ingresar i
		Mientras i <> 0
			Ingresar EMB[i].MAT, EMB[i].NOM, EMB[i].MAR, EMB[i].ANO
			Ingresar i
		FinMientras
		Para i = 1, 350, 1
			Imprimir EMB[i].MAT, EMB[i].NOM, EMB[i].MAR, EMB[i].ANO
		FinPara
		Ingresar MatIng
		Para i = 1, 350, 1
			Mientras MatIng <> 0
				Mientras x = false
					Si EMB[i].MAT = MatIng
						x = true
						Mostrar EMB[i].NOM, EMB[i].MAR, EMB[i].ANO
						x = false
					FinSi
				FinMientras
				Ingresar MatIng
			FinMientras
		FinPara
	FIN
```

### Ejercicio
Prefectura Naval Argentina ha decidido realizar un reempadronamiento de los distintos tipos de embarcaciones que circulan en las distintas áreas navegables del país. 
Para ello ingresa por teclado los siguientes datos de cada una de las embarcaciones:
MAT _ Nº de matrícula 
NOM _ Nombre del propietario 
MAR _ Marca 
ANO _ ANo de fabricación 
Se requiere: 

1.- Ingresar los datos y guardarlos en una estructura de datos cuyo diseNo queda a criterio del programador. 

2- Finalizado el ingreso de datos imprimir un listado que contenga: 
Nº de matrícula – Nombre del propietario – Marca 

3- Desarrollar un módulo de consulta donde ingresando el numero de matrícula, muestre por pantalla: 
Nombre propietario – Marca de embarcación – ANo de fabricación

### Solución
```Pascal
Program Prefectura
	Type
		R-Embarcacion = record
			MAT = integer
			NOM = string
			MAR = string
			ANO = integer
		end
	Var
		EMB = array [1..500] of R-Embarcacion
		i, MatIng, LIM = integer
		x = false
	Inicio
		Ingresar i
		LIM := 0
		Mientras i <> 0
			LIM += 1
			Si LIM <= 500
				Ingresar EMB[i].MAT, EMB[i].NOM, EMB[i].MAR, EMB[i].ANO
			Sino
				Mostrar "Registro lleno"
			FinSi
			Ingresar i
		FinMientras
		Para i = 1, LIM, 1
			Imprimir EMB[i].MAT, EMB[i].NOM, EMB[i].MAR, EMB[i].ANO
		FinPara
		Ingresar MatIng
		Para i = 1, LIM, 1
			Mientras MatIng <> 0
				Mientras x = false
					Si EMB[i].MAT = MatIng
						x = true
						Mostrar EMB[i].NOM, EMB[i].MAR, EMB[i].ANO
						x = false
					FinSi
				FinMientras
				Ingresar MatIng
			FinMientras
		FinPara
	FIN
```
## 23/08
### Enunciado
Un equipo de investigadores de fenómenos meteorológicos ha decidido implementar 
un sistema que le permita establecer las influencias del agujero de ozono sobre el 
clima de 12 localidades de la provincia. 
 
 Para ello se han tomado diariamente durante el mes de Julio los siguientes datos 
del estado del tiempo :
 
- Código de Localidad (1..12)
- Día del mes (1..31)
- Temperatura máxima
- Temperatura mínima
- % de humedad
- Lluvias registradas ( en mm.)
Se requiere :
1) Imprimir un listado de los datos ingresados que contenga :
 Código de localidad - Día del mes - Te.Máxima - Te.Mínima - % Humedad - Lluvia 
Registrada
2) Codificar un modulo de consulta donde ingresando el número de localidad nos 
muestre por pantalla el total de lluvias registradas en el mes y la cantidad de días que 
llovieron en la localidad indicada.. 
3) Por fin de proceso imprimir :
 - Promedio de Temperaturas Máximas
 - Promedio de Temperaturas Mínimas
 - Promedio de Humedad

### Solución
```Pascal
Program meteoróloga
	Type
		R-TiempoLocal = record
			TeMin : Real
			TeMax : Real
			Hume : Real
			Preci : Real
		end
	Var
	    Dia = integer
	    LocCod = integer
	    Tiempo = array [1..12, 1..31] of R-TiempoLocal
	    i, j = integer
	    CantLluvia = array [1..12] of Real
	    DiasLlovidos = array [1..12] of integer
	    CodIng = integer
	    TPMAX, TPMIN, PHum = Real
	Inicio
	    Para i = 1, 12, 1
	        CantLluvia[i] := 0
	    FinPara
		Ingresar LocCod
		Mientras LocCod <> 0
		    Ingresar Dia
		    Ingresar Tiempo[LocCod, Dia].TeMin, Tiempo[LocCod, Dia].TeMax, Tiempo[LocCod, Dia].Hume, Tiempo[LocCod, Dia].Preci
		        Ingresar Dia
		    Ingresar LocCod
		FinMientras
		Para i = 1, 12, 1
		    Imprimir i
	        Para j = 1, 31, 1
	            Imprimir j, Tiempo[i, j].TeMax, Tiempo[i, j].TeMin, Tiempo[i, j].Hume, Tiempo[i, j].Preci
	            Si Tiempo[i, j].Preci > 0
		        CantLluvia[LocCod] += Tiempo[LocCod, Dia].Preci
		        DiasLlovidos[LocCod] += 1
		    FinSi
	        FinPara
	    FinPara
	    Ingresar CodIng
	    Mientras CodIng <> 0
	        Mostrar CantLluvia[CodIng], DiasLlovidos[CodIng]
	    FinMientras
	    Para i = 1, 12, 1
		    Para j = 1, 31, 1
			    TPMAX += Tiempo[i, j].TeMax
			    TPMIN += Tiempo[i, j].TeMin
			    PHum += Tiempo[i, j].Hume
			FinPara
		FinPara
		Imprimir TPMAX, TPMIN, PHum
	FIN
```

### Ejercicio
1. Escribir un algoritmo por el cual se obtenga la sumatoria de los elementos de tipo enteros de una matriz “M” de 10x30 elementos e imprimir su resultado. 

### Solución
```Pascal
Program Sumatoria
	Type
		R-M = record
			Dato : integer
		end
	Var
		M = array [1..10, 1..30] of R-M
		i, j = integer
		SUM = integer
	Inicio
		Para i = 1, 10, 1
			Para j = 1, 30, 1
				SUM += M[i, j]
			FinPara
		FinPara
		Imprimir SUM
	FIN
```

### Ejercicio
2. Dada una matriz “M” de 10x80 elementos que tiene valores reales en todas las columnas a excepción de la columna 80, se debe sumar los valores de cada fila y el resultado almacenarlo en la columna 80 de cada una de ellas; y al final imprimir el resultado de la suma de los valores de la columna 80. 

### Solución
```Pascal
Program Sumatoria 2
	Type
		R-M = record
			Dato : Real
		end
	Var
		M = array [1..10, 1..80] of R-M
		i, j = integer
	Inicio
		Para i = 1, 10, 1
			Para i = 1, 79, 1
				M[i, 80] += M[i, j]
			FinPara
		FinPara
		Para i = 1, 10, 1
			Imprimir M[i, 80]
		FinPara
	FIN
```
### Ejercicio
3. Dada una matriz “M” de 10x80 elementos de tipo real se debe buscar el menor valor y ubicarlo en el lugar de la primera fila y primera columna; y el elemento de la primera fila primer columna en el lugar del menor encontrado. 

### Solución
```Pascal
Program Sumatoria 3
	Type
		R-M = record
			Dato : Real
		end
	Var
		M = array [1..10, 1..80] of R-M
		i, j, iaux, jaux = integer
		EMIN, EAux = Real
	Inicio
		EMIN := low_value
		Para i = 1, 10, 1
			Para j = 1, 80, 1
				Si EMIN < M[i, j]
					EMIN := M[i, j]
					iaux := i
					jaux := j
				FinSi
				Si i = 10 and j = 80
					EAux := M[1, 1]
					M[1, 1] := EMIN
					M[iaux, jaux] := EAux
				FinSi
			FinPara
		FinPara
	FIN
```
### Ejercicio
4. Una Institución Educativa Superior debe procesar los gastos de los profesores que no son de la localidad y deben viajar para desarrollar sus clases. La Institución tiene calculado el monto total que puede gastar en cada uno de los rubros de cada carrera donde desarrolla sus clases cada profesor. 
Se requiere: 
a) Ingresar los montos totales que la Institución tiene calculado gastar. 
Se ingresa: 

CodCarr – Código de carrera en la cual el profesor desarrolla sus clases. 
Puede contener: 1-Abogacía, 2-Informatica, 3-Contador, 4-Turismo, 5-Astronomía, 6- Medicin, 7-Arqueología, 8-Educación, 9-Kinesiología, 10-Economía 
Cod-Rub – Código de rubro en el que el profesor puede gastar 
Puede contener: 1-Pasajes, 2-Hospedaje, 3-Comida, 4-Remis, 5-Viáticos, 6-Varios 
ImpPre – Importe total calculado que se puede gastar en cada rubro para cada carrera. 

b) Ingresar los gastos que cada profesor informa cada vez que viaja para desarrollar sus clases. Se ingresa: 
NomPro – Nombre del Profesor 
C-Carrera – Código de carrera donde desarrolla su clase (rango 1 a 10) 
C-Rubro – Código de rubro cuyo gasto informa (rango 1 a 6) 
ImpInf – Importe que informa que gasto en dicho rubro. 

Debe preverse que el importe informado se acumule para obtener luego un total general por cada rubro de cada carrera, y poder emitir posteriores informes. 

c) Impresión de listado. Se debe imprimir un listado que contenga la siguiente información: 
- Código de Carrera 
- Código de Rubro 
- Importe total calculado que se puede gastar 
- Importe informado acumulado por profesores 
Al finalizar el listado imprimir: 
- Total de importe informado acumulado de la carrera de Astronomía 
- Código de carrera y código de rubro que mayor importe informado acumulado tiene.

### Solución
```Pascal
Program Profes_gastos
	Type
		R-CálculoGastos = record
			CodCarr : integer
			Cod-Rub : integer
			ImpPre : Real
			ImpGas : Real
		end
	Var
		Insti : array [1..10, 1..6] of R-CálculoGastos
		ImpInfo, ImpoTAst : Real
		NomPro : string
		x, y : integer
		xmax, ymax : integer
	Inicio
		// Módulo a
		Mostrar "Ingreso de datos de la institución"
		Mostrar "Ingrese Código de carrera (0 para cancelar)"
		Ingresar x
		Mientras x <> 0
			Si x < 1 or i > 10
				Mostrar "Fuera de rango"
			Sino
				Mostrar "Ingrese código de rubro"
				Ingresar y
				Si y < 1 or y > 6
					Mostrar "Fuera de rango"
				Sino
					Mostrar "Ingrese importe total calculado"
					Ingresar Insti[x, y].ImpPre
					Insti[x, y].ImpGas := 0
				FinSi
			FinSi
			Mostrar "Ingrese código de carrera y luego código de rubro (0 para cancelar)"
			Ingresar x, y
		FinMientras
		// Módulo b
		Mostrar "Ingreso de datos de los profesores"
		Mostrar "Ingrese el nombre del profesor (Espacio para cancelar)"
		Ingresar NomPro
		Mientras NomPro <> " "
			Mostrar "Ingrese código de carrera y número de rubro"
			Ingresar x, y
			Mostrar "Ingrese el importe informado de dicho rubro"
			Ingresar ImpInf
			Insti[x, y].ImpGas += ImpInf
			Mostrar "Ingrese el nombre del profesor (Espacio para cancelar)"
			Ingresar NomPro
		FinMientras
		// Módulo c
		ImpoTAst := 0
		Para y = 1, 6, 1
			ImpoTAst += Insti[5, y]
		FinPara
		Imprimir "Total acumulado en astronomía: ", ImpoTAst
		
		Imprimir TImpAst
		ImpoInfMAX := low_value
		Para x = 1, 10, 1
			Para y = 1, 6, 1
				Imprimir x, y, Insti[x, y].ImpPre, Insti[x, y].ImpGas
				Si ImpoInfMAX < Insti[x, y].ImpGas
					ImpoInfMAX := Insti[x, y].ImpGas
					xmax := x
					ymax := y
				FinSi
			FinPara
		FinPara
		Imprimir "Código de carrera y código de rubro con mayor importe acumulado: ", xmax, ymax
	Fin
```

## 29/08
### Ejercicio
La asociación de pilotos de turismo carretera necesita desarrollar un algoritmo que le permita procesar los tiempos establecidos por cada uno de sus 60 autos y obtener al final del proceso la clasificación de la carrera.
Para ello, cada vez que un auto atraviesa la línea de largada se ingresan por teclado los siguientes datos: 
NUM -Nº del auto 
TIE -Tiempo de vuelta 
Se debe tener en cuenta que algún auto puede abandonar la carrera y se supone que al menos 3 autos terminan la carrera. 
Se requiere : 
1_ Imprimir los Nº de los autos y el nombre de los pilotos que suben al podio. 
Los nombres de los pilotos se ingresan al comienzo del algoritmo

Problemas de la solución planteada:
- No contabiliza que el segundo o tercer puesto pueden hacer 1 o más vueltas menos
- No contabiliza que algún auto abandone la carrera
### Solución
```Pascal
Program Pilotos
	Type
		R-autos = record
			Nom : string
			TIE : Real
			CANVUE : integer
			x : boolean
		end
	Var
		autos = array [1..60] of R-autos
		podio = array [1..3] of string
		i, NUM : integer
		CANVUE, TIE : Real
	Inicio
		// Ingreso de nombres e inicialización
		Para i = 1, 60, 1
			Mostrar "Ingrese los nombres"
			Ingresar autos[i].Nom
			autos[i].CANVUE := 0
			autos[i].TIE := 0
			autos[i].x := false // al principio ninguno abandona
		FinPara
		// Ingreso de datos
		Ingresar NUM
		Mientras NUM <> 0
			Ingresar TIE
			Ingresar autos[i].x // Acá se ingresa si abandonó la carrera (TRUE = Abandonó)
			autos[i].TIE += TIE
			autos[i].CANVUE += 1
			Ingresar NUM
		FinMientras
		// Comparación
		CANVUE := 0
		Para i = 1, 60, 1
			Si CANVUE < autos[i].CANVUE
				CANVUE := autos[i].CANVUE
			FinSi
		FinPara
		podio[1] := max_value
		Para i = 1, 60, 1
			Si autos[i].x = false
				Si autos[i].CANVUE = CANVUE
					Si podio[1] > autos[i].TIE
						podio[3] = podio[2]
						podio[2] = podio[1]
						podio[1] = autos[i].Nom
					FinSi	
				FinSi
			FinSi
		FinPara
		Para i = 1, 3, 1
			Imprimir "1: ", podio[1]
			Imprimir "2: ", podio[2]
			Imprimir "3: ", podio[3]
		FinPara
	Fin
```

### Ejercicio
Una Obra Social tiene grabado en memoria dos vectores : 
- VFEM de ( 1.. 3210 ) 
- VMAS de ( 1.. 2560 ) 
En ellos contienen el padrón de asociados femeninos y masculinos respectivamente. El diseNo de registro de ambos vectores es el mismo. 
DOC - Nº de documento 
NOM - Nombre 
DIR - Dirección 
EDAD - Edad 
Se requiere desarrollar los siguientes módulos: 
1. PROCESO. Unificar el padrón en un solo vector, agregando en el registro el sexo del asociado. 
2. CONSULTA Desarrollar un módulo de consulta dónde ingresando el número de documento del asociado muestre por pantalla los datos correspondiente

### Solución
```Pascal
Program ObraSocial
    Type
        R-asociados = record
            DOC : integer
            NOM : string
            DIR : string
            EDAD : integer
            SEX : string
        end
    Var
        ASOC : array[1..5770] of R-asociados
        i, x, DOC : integer
    Inicio
        Para i = 1, 3210, 1
            ASOC[i].DOC := VFEM[i].DOC
            ASOC[i].NOM := VFEM[i].NOM
            ASOC[i].EDAD := VFEM[i].EDAD
            ASOC[i].DIR := VFEM[i].DIR
            ASOC[i].SEX := "Femenino"
        FinPara
        Para i = 3210, 5770, 1
            ASOC[i].DOC := VMAS[i].DOC
            ASOC[i].NOM := VMAS[i].NOM
            ASOC[i].EDAD := VMAS[i].EDAD
            ASOC[i].DIR := VMAS[i].DIR
            ASOC[i].SEX := "Masculino"
        FinPara
        x := 0
        Ingresar DOC
        Para i = 1, 5770, 1
            Si DOC = ASOC[i].DOC
                x = 1
                Mostrar ASOC[i].DOC, ASOC[i].NOM, ASOC[i].DIR, ASOC[i].EDAD, ASOC[i].SEX
            FinSi
        FinPara
        Si x = 0 
            Mostrar "No encontrado"
        FinSi
    Fin
```
### Ejercicio
La financiera “Credifácil” necesita procesar los datos de sus clientes. Para ello tiene grabado en memoria un vector VCLI de 4230 elementos cuyo diseNo de registro es el siguiente:
DOC - Nº de documento 
NOM - Nombre 
DEU – Importe de deuda 
FEC – Fecha de último pago 
Se requiere desarrollar los siguientes módulos: 
1. PROCESO. 
- Generar 2 vectores con el mismo diseNo, uno que contenga los datos de aquellos clientes que no tengan deuda y otro con los que deben algún importe. 
2. LISTADO. 
- Imprimir un listado de los datos de aquellos clientes que tienen deuda. 
Al finalizar el listado imprimir el nombre del cliente que tiene la mayor deuda.

### Solución
```Pascal
Program Credifácil
    Type
        R-Deudores = record
            DOC : integer
            NOM : string
            DEU : Real
            FEC : string
        end
    Var
        Deuda : array [1..4230] of R-Deudores
        NoDeuda : array [1..4230] of R-Deudores
        i, LIM : integer
        DeuMAX : Real
        NomMAX : string
    Inicio
        LIM := 0
        Para i = 1, 4230, 1
            Si VCLI[i].DEU = 0
                NoDeuda[i].DEU := VCLI[i].DEU
                NoDeuda[i].DOC := VCLI[i].DOC
                NoDeuda[i].NOM := VCLI[i].NOM
                NoDeuda[i].FEC := VCLI[i].FEC
            Sino
                LIM += 1
                Deuda[i].DEU := VCLI[i].DEU
                Deuda[i].DOC := VCLI[i].DOC
                Deuda[i].NOM := VCLI[i].NOM
                Deuda[i].FEC := VCLI[i].FEC
            FinSi
        FinPara
        Para i = 1, LIM, 1
            Imprimir Deuda[i].DOC, Deuda[i].NOM, Deuda[i].FEC, Deuda[i].DEU
            Si Deuda[i].Deu > DeuMAX
                DeuMAX := Deuda[i].Deu
                NomMAX := Deuda[i].NOM
            FinSi
        FinPara
        Imprimir NomMAX
    Fin
```
### Ejercicio
Una institución bancaria necesita procesar los datos de los usuarios de tarjetas de crédito. Para ello ingresa por teclado los siguientes datos de cada usuario: 
NUM- Nº de tarjeta 
NOM- Nombre del titular 
LIM – Importe límite de compra 
SAL – Importe del saldo a pagar 
Se requiere desarrollar los siguientes módulos: 
1. INGRESO. 
Ingresar los datos de los usuarios y guardarlos en un arreglo cuyo diseNo queda a criterio del programador.
2. ACTUALIZACIÓN. 
Se ingresan los siguientes datos de cada compra realizada por el usuario y se debe actualizar en el vector el importe del saldo a pagar. 
NUT – Nº de tarjeta 
IMPO- Importe de la compra 
3. LISTADO
Imprimir un listado de todos los usuarios que contenga:
Nro de Tarjeta – Nombre titular – Importe de saldo a pagar 

Al finalizar el listado imprimir: 
Nº de tarjeta y nombre del titular de la tarjeta de mayor saldo a pagar.

### Solución
```Pascal
program Banco
	Type
		R-Tarjetas = record
			NOM : string
			LIM : Real
			SAL : Real
		end
	Var
		Tar = array [1..5000] of R-Tarjetas
		NUT, NUM, NUTMAX, i, LIM : integer
		IMPO, SALMAX : Real
	Inicio
		// Módulo 1
		LIM := 0
		Ingresar NUM
		Mientras NUM <> 0
			Si NUM < 1 or NUM > 5000
				Mostrar "Número excedido"
			Sino
				LIM += 1
				Ingresar Tar[NUM].NOM, Tar[NUM].LIM, Tar[NUM].SAL
			FinSi
			Ingresar NUM
		FinMientras
		// Módulo 2
		Ingresar NUT, IMPO
		Si (Tar[NUT].SAL + IMPO) > Tar[NUT].LIM
			Mostrar "Límite excedido"
		Sino
			Tar[NUT].SAL + IMPO
		FinSi
		// Módulo 3
		SALMAX := low_value
		Para i = 1, LIM, 1
			Imprimir i, Tar[i].NOM, Tar[i].SAL
			Si SALMAX < Tar[i].SAL
				SALMAX = Tar[i].SAL
				NUTMAX = i
			FinSi
		FinPara
		Imprimir NUTMAX, Tar[NUTMAX].NOM
	Fin

```


### Ejercicio
Ejercicio: Calcular el valor del impuesto a los Bienes Personales. 
Se ingresa: 
- Apellido y Nombre del contribuyente
- Valor total de los bienes 

Con estos datos se debe imprimir:
Apellido y Nombre – Valor Total de los Bienes – Impuesto a Pagar

Para el cálculo del Impuesto se debe tener en cuenta: 
a) Se aplica sobre el valor total de los bienes las siguientes alícuotas: 
hasta 2.000.000 = 0% 
de 2.000.001 a 5.000.000 = 1% sobre el excedente 
más de 5.000.000 = 2% sobre el excedente de 2.000.000 

b) Los cálculos deben efectuarse en un subprograma de tipo función (Cálculo).

A la función Cálculo se le pasa como parámetro el valor total de bienes ingresado.
### Solución
```Pascal
Program Bienes personales
	Type
		BIPE = record
			Nom : string;
			VT : Real;
			IP : Real;
		end
	Var
		BP : array[1..9999] of BIPE;
		i, LIM : integer;
	Inicio
		// Programa inicial
		Ingresar i
		LIM := 0
		Mientras i <> 0
			Ingresar BP[i].Nom, BP[i].VT
			Ingresar i
			LIM := LIM + 1
		FinMientras
		// Subprograma
		Si BP[i].VT < 2000000
			BP[i].IP := 0
		FinSi
		Si BP[i].VT > 2000000 y BP[i].VT < 5000000
			BP[i].IP := (BP[i].VT - 2000000)/100
		FinSi
		Si BP[i].VT > 5000000
			BP[i].IP := (BP[i].VT - 5000000)/50
		FinSi
		// Imprimir
		Para i := 1, LIM, 1
			Imprimir BP[i].Nom, BP[i].VT, BP[i].IP
		FinPara
	Fin
```
## 30/08
### Ejercicio
Se deben procesar los datos de la recaudación de un día de las 27 unidades de una línea de transporte urbano. Para ello se han definido los siguientes procedimientos: 
a) Ingreso de datos: 
Al finalizar el día, de cada unidad se ingresa: 
NUni – Número de unidad 
BJub – Cantidad boletos vendidos jubilados 
BGen – Cantidad boletos vendidos generales 
BEst – Cantidad de boletos vendidos estudiantes 

Para el proceso se debe definir un array de 27 elementos. Cada elemento debe contemplar el almacenamiento de la cantidad de boletos y un campo (Impo) para almacenar el importe recaudado por la unidad por la venta de boletos (las cantidades ingresadas y el importe deben sumarse a los datos que existen en el array).
El costo de cada boleto de cada una de las categorías (general, jubilado y estudiantes), se ingresa una sola vez al inicio del algoritmo, debiendo almacenarse en 3 variables (CosGen, CosJub y CosEst).
Para calcular el importe recaudado por cada unidad se debe multiplicar el costo de cada categoría por la cantidad de boletos vendidos de dicha categoría, y luego sumar los tres importes, para luego sumar este último al campo del array. 

b) Consulta de datos: Se ingresa por teclado el número de unidad y se deben mostrar todos los datos de los campos.

c) Procedimiento LISTADO:
Imprimir un listado de todas las unidades que contenga:
Nro. deUnidad – Cant. Bol Jubilados – Cant. Bol. Estudiantes – Cant. Boletos Generales- Imp. total recaudado
Al finalizar la impresión del listado imprimir:
1) Cantidad total de boletos vendidos discriminados por categoría.
2) Importe total recaudado.
3) Número de unidad que más cantidad de boletos vendió en total
4) Número de unidad que mayor importe recaudó.
### Solución
```Pascal
program transporte
	Type
		R-Cole = record
			RJub : integer
			RGen : integer
			BEst : integer
			Impo : Real
		end
	Var
		Cole = array [1..27] of R-Cole
		NUni, i, TGen, TJub, TEst, TImpo, BOLMAX, NUniMAXB, NUniMAXI : integer
		CosGen, CosJub, CosEst, IMPMAX : Real
	Inicio
		// Módulo 1
		Ingresar CosGen, CosJub, CosEst
		Para i = 1, 27, 1
			Cole[i].Impo := 0
		FinPara
		Para i = 1, 27, 1
			Ingresar Cole[i].RJub, Cole[i].RGen, Cole[i].BEst
			Cole[i].Impo += Cole[i].RJub
			Cole[i].Impo += Cole[i].RGen
			Cole[i].Impo += Cole[i].BEst
		FinPara
		// Módulo 2
		Ingresar NUni
		Mostrar Cole[NUni].RJub, Cole[NUni].RGen, Cole[NUni].BEst, Cole[NUni].Impo
		// Módulo 3
		TGen, TJub, TEst, TImpo := 0
		NUniMAX, IMPMAX := low_value
		Para i = 1, 27, 1
			Imprimir i, Cole[i].RJub, Cole[i].RGen, Cole[i].BEst, Cole[i].Impo
			TGen += Cole[i].RGen
			TJub += Cole[i].RJub
			TEst += Cole[i].BEst
			TImpo += Cole[i].Impo
			Si BOLMAX < (Cole[i].RGen + Cole[i].RJub + Cole[i].BEst)
				BOLMAX = (Cole[i].RGen + Cole[i].RJub + Cole[i].BEst)
				NUniMAXB = i
			FinSi
			Si IMPMAX < Cole[i].Impo
				IMPMAX := Cole[i].Impo
				NUniMAXI := i
			FinSi
		FinPara
		Imprimir TGen, TJub, TEst, TImpo, NUniMAXB, NUniMAXI
	Fin
```
## 06/09
### Ejercicio
Una Entidad Financiera debe procesar los datos de las retenciones por los aportes voluntarios que realizan sus empleados a una ONG que asiste económicamente a comedores escolares. Se han definido los siguientes procedimientos para ser codificados por módulos.
1 – Ingreso:
Ingresar los siguientes datos de todos los empleados (tanto de los que aportan como los que no 
aportan).
NumDoc – Número de Documento del empleado
NomEmp - Nombre del empleado
SueBru – Sueldo Bruto
CodApo – Código de aporte [1-Aporta a la ONG, 2-NO aporta a la ONG]
 Los datos ingresan sin seguir orden alguno
2- Ordenamiento e impresión:
Imprimir un listado con los datos ingresados ordenado por Nombre del empleado, que contenga:
Nombre del Empleado - Número de Documento – Importe del Aporte 
 El aporte a la ONG es un porcentaje del sueldo bruto según siguiente escala:
 
Hasta $ 20,000 - 1%
De $ 20,001 a 50,000 - 1,5%
Mas de $ 50,000 - 2%

 Al Finalizar el listado se debe imprimir:
a) Importe total de las retenciones
b) Cantidad de empleados que NO aportan a la ONG
c) Nombre del Empleado de mayor sueldo que aporta a la ONG.

### Solución
```Pascal
Program Financ
    Type
        R-Financ = record
            NumDoc : integer
            NomEmp : string
            SueBru : Real
            CodApo : integer
        end
    Var
        // Módulo 1
        Fina = array [1..2000] of R-Financ
        i, LIM, TNoApo : integer
        Aux : R-Financ
        ImpoT, AuxSuel: Real
        AuxNom : string
        x : boolean
    Inicio
        Ingresar i
        LIM := 0
        Mientras i <> 0
            LIM += 1
            Ingresar Fina[i].NumDoc, Fina[i].NomEmp, Fina[i].SueBru, Fina[i].CodApo
        FinMientras
        // Módulo 2
        x = false
        Mientras x = false
            x = true
            Para i = 1, LIM-1, 1
                Si Fina[i].NomEmp > Fina[i+1].NomEmp
                    Aux = Fina[i].NomEmp
                    Fina[i].NomEmp := Fina[i+1].NomEmp
                    Fina[i+1].NomEmp := Aux
                    x = false
                FinSi
            FinPara
        FinMientras
        AuxSuel := low_value
        ImpoT := 0
        TNoApo := 0
        Para i = 1, LIM, 1
            Imprimir Fina[i].NomEmp, Fina[i].NumDoc
            Si Fina[i].CodApo = 1
                Si Fina[i].SueBru > 50000
                    Si Fina[i].SueBru > AuxSuel
                        AuxSuel := Fina[i].SueBru
                        AuxNom := Fina[i].NomEmp
                    FinSi
                    ImpoT += Fina[i].SueBru
                    Imprimir Fina[i].SueBru*0.02
                Sino 
                    Si Fina[i].SueBru < 20001
                    ImpoT += Fina[i].SueBru
                    Imprimir Fina[i].SueBru*0.01
                    Sino
                        Impot += Fina[i].SueBru
                        Imprimir Fina[i].SueBru*0.015
                    Finsi
                FinSi
                Sino
                    TNoApo += 1
            FinSi
        FinPara
        Imprimir ImpoT, TNoApo, NomAux
    Fin
```

## 12/09
### Enunciado
Se desea procesar los datos de los prestamos de libros que realiza la biblioteca. Para ello se deben ingresar los siguientes datos de los socios :
NUS Número de socio
NOM Nombre del socio
CAP Cantidad de libros prestados en el aNo
CAD Cantidad de libros devueltos en el aNo
* Estos datos ingresan sin seguir orden alguno.
Se requiere desarrollar los siguientes módulos :
- LISTADO 
Imprimir un listado ORDENADO por número de socios que contenga :
Nº de socio – Nombre – Cantidad de libros pendientes de devolución
Finalizado el listado imprimir :
- Cantidad de libros prestados en el aNo a todos los socios 
- Nombre del socio que mayor cantidad de libros tiene pendiente de devolución 
-CONSULTA
Codificar un módulo de consulta tal que ingresando el número de socio se muestre
por pantalla todos los datos del socio (utilizar método dicotómico).

### Solución
```Pascal
Program Biblio 4.0
    Type
        R-Datos = record
            NUS : integer
            NOM : string
            CAP : integer
            CAD : integer
        end
    Var
        Dato = array [1..10000] of R-Datos
        i, LIM, AUXSOC, PREST, CAPMAX, LI, LS, NS : integer
        NOMMAX : string
        x : boolean
    Inicio
        // Módulo 1
        LIM := 0
        Ingresar i
        Mientras i <> 0
            Ingresar Dato[i].NUS, Dato[i].NOM, Dato[i].CAP, Dato[i].CAD
            Ingresar i
            LIM += 1
        FinMientras
        // Módulo 2
        x := false
        Mientras x = false
            x := true
            Para i = 1, LIM-1, 1
                Si Dato[i].NUS > Dato[i+1].NUS
                    AUXSOC := Dato[i].NUS
                    Dato[i].NUS := Dato[i+1].NUS
                    Dato[i+1].NUS := AUXSOC
                    x := false
                FinSi
            FinPara
        FinMientras
        PREST := 0
        CAPMAX := low_value
        Para i = 1, LIM, 1
            Imprimir Dato[i].NUS, Dato[i].NOM
            Imprimir Dato[i].CAP - Dato[i].CAD
            PREST += Dato[i].CAP
            Si CAPMAX < (Dato[i].CAP - Dato[i].CAD)
                CAPMAX := (Dato[i].CAP - Dato[i].CAD)
                NOMMAX := Dato[i].NOM
            FinSi
        FinPara
        Imprimir PREST, NOMMAX
        // Módulo 3
        Ingresar NS
        Mientras NS <> 0
            LI := 0
            LS := LIM
            i := (LS-LI)/2
            Mientras LS > LI and NS <> Dato[i].NUS
                Si NS > Dato[i].NUS
                    LI = i + 1
                Sino
                    LS = i - 1
                Finsi
                i = (LS+LI)/2
            FinMientras
            Si Dato[i].NUS = NS
                Mostrar "Nombre: ", Dato[i].NOM
                Mostrar "Número de socio", Dato[i].NUS
                Mostrar "Cantidad de libros restados: ", Dato[i].CAP
                Mostrar "Cantidad de libros devueltos: ", Dato[i].CAD
            Sino
                Mostrar "Dato no encontrado"
            Finsi
        FinMientras
    Fin
```
## 13/09
### Enunciado
Los alumnos de la Facultad han organizado un bono contribución para recaudar fondos para realizar un viaje de estudios y necesitan procesar los siguientes datos de cada bono:
NUD - Nro.Documento del Comprador 
APN - Apellido y Nombre del Comprador 
SPC - Situación primera cuota [1=Impaga, 2=Paga] 
SCC - Situación segunda cuota [1=Impaga, 2=Paga] 
Se requiere desarrollar los siguientes módulos:
INGRESO
- Ingresar los datos y guardarlos en una estructura de datos cuyo diseNo queda a criterio del programador. 
- Los campos SPC y SCC se generan con valor 1 (Impaga)
ACTUALIZACION 
- Registrar el pago de cuotas, para ello se ingresa por teclado el número de documento y la cuota que se abona, debiéndose actualizar el campo correspondiente. Para la búsqueda del bono debe utilizarse estrategia dicotómica.
LISTADO
Imprimir un listado ordenado por Nro.de Documento con el siguiente diseNo: 
| Documento | Apellido y nombre del comprador | Cuota 1 | Cuota 2 |
| --------- | ------------------------------- | ------- | ------- |
| 11111111  | Keith, Ricardo                  | Paga    | Impaga  |
| 11111112  | Jagger, Miguel                  | Impaga  | Impaga  |
| 11111113  | Watts, Carlos                   | Paga    | Paga    |
| 11111114  | Wood, Ronaldo                   | Impaga  | Impaga  |

### Solución
```Pascal
Program Facu
	Type
		R-Bono = record
			NUD : integer
			APN : string
			SPC : integer
			SCC : integer
		end
	Var
		Bono = array [1..9999] of R-Bono
		i, LIM, DNI: integer
	Inicio
		LIM := 0
		Ingresar i
		Mientras i <> 0
			Si i > 1 or < 9999
				Ingresar Bono[i].NUD, Bono[i].APN
				Bono[i].SPC := 1
				Bono[i].SCC := 1
				LIM += 1
			Sino
				Mostrar "Registro lleno"
			FinSi
			Ingresar i
		FinMientras
		Ingresar DNI, Cuota
	Fin
```

### Enunciado
Una embotelladora de gaseosas necesita implementar un sistema que le permita procesar los datos de las partidas producidas durante el mes de Agosto. Para ello se ingresan por teclado los siguientes datos de cada partida:
	DIA -  Día del mes 
	HS - Hora 
	NP - Nº Partida
	CS - Código de sabor (Rango de 1 a 7) 
	CL - Cantidad de litros 
Los datos se ingresan sin seguir orden alguno. 
Se requiere: 
1. Imprimir un listado de los datos ingresados con el siguiente diseNo:
Día – Nº de partida – Nombre de Sabor – Cantidad de Litros 
El nombre de los sabores se ingresa al comienzo del algoritmo. 
2. Por fin de proceso imprimir. 
a. Listado ordenado por Nº de partida que contenga.
Numero de partida - Día – Cantidad de litros – Nombre de sabor 
b. Cantidad total de litros producidos en el mes. 
c. Listado ordenado por nombre de sabor que contenga 
Nombre de sabor – Cantidad de litros
d. Sabor de gaseosa que más litros se produjo en el mes.
e. Teniendo en cuenta que el 30 % del total de litros se envasa en botellas de 2 litros y el resto en botellas de 1 litro y medio, obtener la cantidad de envases de 2 litros y de 1,5 litros que se necesitan para envasar la producción del mes.
f. Cantidad de etiquetas necesarias discriminadas por sabor

### Solución
```Pascal
Program embotelladora
	Type
		R-embo = record
			NP : integer
			DIA : string
			HS : integer
			CS : integer
			CL : Real
		end
		R-Sabs = record
			Nom : string
			CLTot : Real
		end
	Var
		SAB : array[1..7] of R-Sabs
		Embo : array[1..99999] of R-embo
		CESAB : array[1..7] of integer
		Aux : R-embo
		AuxSAB : R-Sabs
		CLTOT : Real
		SABMAXN : string
		SABMAXCL : Real
		BOT2L : integer
		BOT15L : integer
		LIM : integer
		NP : integer
		i : integer
		x : boolean
	Inicio
		Para i = 1, 7, 1
			Ingresar SAB[i].Nom
			SAB[i].CLTot := 0
			CESAB[i] := 0
		FinPara
		LIM := 0
		Ingresar i
		Mientras i <> 0
			Ingresar Embo[i].NP, Embo[i].DIA, Embo[i].HS, Embo[i].CS, Embo[i].CL
			Ingresar i
			SAB[Embo[i].CS].CLTot += Embo[i].CL
			CESAB[Embo[i].CS] += 1 
			LIM += 1
		FinMientras
		x := False
		Mientras x = False
			x := True
			Para i = 1, LIM-1, 1
				Si Embo[i].NP > Embo[i+1].NP
					Aux := Embo[i].NP
					Embo[i].NP := Embo[i+1].NP
					Embo[i+1].NP := Aux
					x := False
				FinSi
			FinPara
			Para i = 1, 6, 1
				Si SAB[i].Nom > SAB[i+1].Nom
					AuxSAB := SAB[i]
					SAB[i] := SAB[i+1]
					SAB[i+1] := AuxSAB
					x:= False
				FinSi
			FinPara
		FinMientras
		CLTOT := 0
		Para i = 1, LIM, 1
			Imprimir Embo[i].NP, Embo[i].DIA, Embo[i].CL, SAB[Embo[i].CS]
			CLTOT += Embo[i].CL
		FinPara
		Imprimir CLTOT
		SABMAXCL := low_value
		Para i = 1, 7, 1
			Imprimir SAB[i].Nom, SAB[i].CLTot
			Si SABMAXCL < SAB[i].CLTot
				SABMAXCL := SAB[i].CLTot
				SABMAXN := Sab[i].Nom
			FinSi
			Imprimir CESAB[i]
		FinPara
		Imprimir SABMAXN
		BOT2L := CLTOT*0.3
		BOT15L := CLTOT*0.7
		Imprimir BOT2L, BOT15L
	Fin
```
## 20/09
### Enunciado
Una compaNía de seguros necesita procesar los datos de las pólizas de automotores que fueron emitidas durante el mes de Agosto. Para ello de cada póliza tiene los siguientes datos: 
	PAT Nº de patente del automotor 
	DIA Día del mes ( 1..31) 
	PRO Nombre del propietario 
	MAR Marca del automotor 
	ANO ANo de fabricación 
	TIPO Tipo de seguro 1-Terceros 2- DaNo Parcial 3- DaNo Total 
Se requiere desarrollar los siguientes módulos 
1. Ingreso de Pólizas Ingresar los datos de las pólizas y guardarlas en una estructura cuyo diseNo queda a criterio del programador 
2. Consulta Pólizas Ingresando el Nº de Patente, muestre por pantalla, los datos correspondientes a la póliza 
3. Informes de Pólizas 
a) Imprimir un listado de todas las pólizas ordenadas por nombre del propietario que contenga:
Nombre propietario – Nº de patente – Marca automotor 
b) Cantidad total de pólizas discriminadas por tipo de seguro 
c) Cantidad de pólizas realizadas por cada día del mes.
### Solución
```Pascal
Program Automotores
	Type
		R-Auto = record
			PAT : string
			DIA : integer
			PRO : string
			MAR : string
			ANO : integer
			TIPO : integer
		end
	Var
		i : integer
		POL : array[1..99999] of R-Auto
		LIM : integer
		NPAT : string
	Inicio
		LIM := 0
		Ingresar i
		Mientras i <> 0
			Ingresar POL[i].PAT, POL[i].DIA, POL[i].PRO, POL[i].MAR, POL[i].ANO, POL[i].TIPO
			Ingresar i
			LIM += 1
		FinMientras
		Ingresar NPAT
		Mientras NPAT <> "F"
			Para i = 1, LIM, 1
				Mientras
			FinPara
			Ingresar NPAT
		FinMientras
	Fin
```
### Enunciado
Una mutual de empleados debe procesar los datos de sus asociados para lo cual, el analista ha definido la codificación de los siguientes procesos: 
ALTA 
Se deben ingresar los siguientes datos de todos los asociados: 
- Número de Asociado (ordenados en forma correlativa a partir del número 1 al 255) 
- Nombre del Titular 
- Saldo que debe por compras realizadas en distintos comercios. 
PROCESO 
Ingresar las operaciones que se realizaron con fecha posterior al saldo registrado en el punto anterior y actualizar el saldo que debe. 
- Número de Asociado 
- Código de operación [1=Pago, 2=Compra] 
- Importe 
CONSULTA 
Modulo de consulta. Se ingresa el número de asociado y se deben mostrar el número de asociado, el apellido y nombre y el saldo que debe. 
ESTADISTICO 
Mostrar por pantalla un cuadro estadístico con los siguientes datos: 
- Importe total adeudado por los Asociados 
- Nombre del Asociado que mas importe adeuda 
Se debe codificar un módulo por cada proceso, los que deben ser invocados por un menú de opciones.

### Solución
```Pascal
Program mutual
	Type
		R-Empleados = record
			Nom : string
			Sal : Real
		end
	Var
		Asoc : array[1..255] of R-Empleados
		i : integer
		COD : integer
		Impo : Real
		NomMAX : string
		SalMAX : Real
		ImpoT : Real
	Inicio
		MENU
		Mientras opcion <> 0
			Segun opcion
				1 : ALTA
				2 : PROCESO
				3 : CONSULTA
				4 : ESTADÍSTICO
			FinSegun
			MENU
		FinMientras
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento ALTA
			Para i = 1, 255, 1
				Ingresar Asoc[i].Nom, Asoc[i].Sal
			FinPara
		FinProcedimiento ALTA
		Procedimiento PROCESO
			Ingresar i, COD, Impo
			Si COD = 1
				Asoc[i].Sal -= Impo
			Sino
				Asoc[i].Sal += Impo
			FinSi
		FinProcedimiento PROCESO
		Procedimiento CONSULTA
		Ingresar i
			Mientras i <> 0
				Mostrar i, Asoc[i].Nom, Asoc[i].Sal
				Ingresar i
			FinMientras
		FinProcedimiento CONSULTA
		Procedimiento ESTADÍSTICO
			ImpoT := 0
			SalMAX := low_value
			Para i = 1, 255, 1
				ImpoT += Asoc[i].Sal
				Si SalMAX < Asoc[i].Sal
					SalMax := Asoc[i].Sal
					NomMax := Asoc[i].Nom
				FinSi
			FinPara
			Mostrar ImpoT, NomMax
		FinProcedimiento ESTADÍSTICO
	Fin
```
## 26/09
### Enunciado
Una empresa constructora necesita procesar los datos de cada uno de los proyectos de construcción de barrios que tiene en distintos estado de desarrollo. Luego de un relevamiento se establece la necesidad de desarrollar los siguientes módulos:
INGRESO DE DATOS 
De cada proyecto se ingresan los siguientes datos que deben ser grabados en una estructura de datos, cuyo diseNo queda a criterio del programador: 
- COD - Código de Proyecto 
- NOM - Nombre del Cliente 
- CAN - Cantidad de viviendas a construir 
- PRE - Presupuesto 
- COS - Código de situación [ 1-No Iniciado, 2-En desarrollo, 3-Terminado, 4-Entregado ] 
ACTUALIZACIÓN DE PRESUPUESTOS 
Producto del proceso inflacionario, la empresa decide ajustar los presupuestos de los proyectos. Se han definido las siguientes pautas de aumento de presupuesto: 
- 20% de aumento para proyectos no iniciados 
- 10% de aumento para proyectos en desarrollo 
Se deben actualizar los presupuestos (campo PRE) de todos los proyectos que cumplan los requisitos según pautas anteriores. 
CONSULTA
Se ingresa por teclado el código de situación y se debe imprimir un listado, ordenado por nombre del cliente, que contenga los datos de los proyectos que estén en la situación ingresada.. 
INFORMES 
Imprimir: 
- Cantidad de proyectos terminados discriminados por código de situación. 
- Nombre del cliente y código del proyecto de mayor presupuesto 
- Cantidad total de viviendas a construir en todos los proyectos 
**Debe utilizarse estrategia modular**

### Solución
```Pascal
Program Constructora
	Type
		R-Proyect = record
			COD : integer
			NOM : string
			CAN : integer
			PRE : Real
			COS : integer
		end
	Var
		Pro : array[1..9999] of R-Proyect
		ProOrd : array[1..9999] of R-Proyect
		ProAux : R-Proyect
		LIM : integer
		LIM2 : integer
		i : integer
		opcion : integer
		COS : integer
		x : boolean
		ProTer : integer
		NomMax : string
		CODMax : integer
		PREMax : Real
		CANT : integer
	Inicio
		MENU
		Mientras opcion <> 0
			Segun MENU
				1 : INGRESO
				2 : ACTUALIZACIÓN
				3 : CONSULTA
				4 : INFORMES
				MENU
			FinSegun
		FinMientras
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento INGRESO
			LIM := 0
			Ingresar i
			Mientras i <> 0
				Ingresar Pro[i].COD, Pro[i].NOM, Pro[i].CAN, Pro[i].PRE, Pro[i].COS
				Ingresar i
				LIM += 1
			FinMientras
		FinProcedimiento INGRESO
		Procedimiento ACTUALIZACIÓN
			Para i = 1, LIM, 1
				Si Pro[i].COS = 1
					Pro[i].PRE = Pro[i].PRE*1.2
				Sino
					Si Pro[i].COS = 2
						Pro[i].PRE = Pro[i].PRE*1.1
					FinSi
				FinSi
			FinPara
		FinProcedimiento ACTUALIZACIÓN
		Procedimiento CONSULTA
			Ingresar COS
			LIM2 := 0
			Para i = 1, LIM, 1
				Si COS = Pro[i].COS
					ProOrd[LIM2].COS := Pro[i].COS
					ProOrd[LIM2].NOM := Pro[i].NOM
					ProOrd[LIM2].CAN := Pro[i].CAN
					ProOrd[LIM2].PRE := Pro[i].PRE
					ProOrd[LIM2].COD := Pro[i].COD
					LIM2 += 1
				FinSi
			FinPara
			x := false
			Mientras x = false
				Para i = 1, LIM2-1, 1
					x := true
					Si ProOrd[i].NOM < ProOrd[i+1].NOM
						ProAux := ProOrd[i]
						ProOrd[i] := ProOrd[i+1]
						ProOrd[i+1] := ProAux
						x := false
					FinSi
				FinPara
			FinMientras
			Para i = 1, LIM2, 1
				Imprimir ProOrd[i].NOM, ProOrd[i].COD, ProOrd[i].CAN, ProOrd[i].PRE, ProOrd[i].COS
			FinPara
		FinProcedimiento CONSULTA
		Procedimiento INFORMES
			ProTer := 0
			PREMax := low_value
			CANT := 0
			Para i = 1, LIM, 1
				Si PREMax < Pro[i].PRE
					PREMax := Pro[i].PRE
					CODMax := Pro[i].COD
					NomMax := Pro[i].NOM
				FinSi
				Si Pro[i].COS = 3
					ProTer += 1
				FinSi
				CANT += Pro[i].CAN
			FinPara
			Imprimir ProTer, NomMax, CODMax, CANT
		FinProcedimiento INFORMES
	Fin
```
### Enunciado
La Sociedad Protectora de Animales necesita implementar un sistema que le permita procesar los datos de las atenciones realizadas a los distintos animales que son rescatados de la vía pública. Para ello se requiere desarrollar los siguientes módulos:
INGRESO.
Ingresar los datos de cada animal y guardarlos en una estructura de datos, cuyo diseNo queda a criterio del programador. Los datos que se ingresan son los siguientes:
NRO – Nº de Ficha 
FEC – Fecha de Ingreso 
TIP – Tipo 1- Perro 2- Gato 3- Caballo 4- Otros 
VAC – Cantidad de vacunas aplicadas 
ULT – Fecha última visita veterinaria 
(La fecha de última visita veterinaria y cantidad de vacunas aplicadas debe ingresarse con valor 0 (cero)) 

VISITA
Cada vez que el veterinario revisa un animal se ingresan por teclado los siguientes datos: 
NRO – Nº de ficha 
FEC – Fecha de visita 
VAC – Cantidad de Vacunas aplicadas 
Con los datos ingresados se debe actualizar la fecha última visita (ULT) y la cantidad de vacunas aplicadas (VAC) 

LISTADO. 
Imprimir un listado ordenado por Fecha de Ingreso de todos aquellos animales que recibieron menos de 5 vacunas con el siguiente diseNo: 
Fecha Ingreso – Nº de Ficha - Tipo – Cantidad de Vacunas aplicadas 

INFORMES. 
Imprimir: 
- Cantidad de animales alojados discriminados por tipo. 
- Nro. de Ficha y Tipo del animal que más vacunas recibió. 
- Cantidad de perros que todavía no han sido visitados por el veterinario.
### Solución
```Pascal
Program Protect
	Type
		R-Animal = record
			FEC : string
			TIP : integer
			VAC : integer
			ULT : string
		end
	Var
		Ani : array[1..9999] of R-Animal
		AniOrd : array[1..9999] of R-Animal
		AniAux : R-Animal
		CanAni : array[1..4] of integer
		opcion : integer
		i : integer
		LIM : integer
		LIM2 : integer
		FEC : string
		VAC : integer
		x : Boolean
		NroMax : integer
		TipMax : integer
		VacMax : integer
		CANP : integer
	Inicio
		MENU
		Mientras opcion <> 0
			Segun opcion
				1 : INGRESO
				2 : VISITA
				3 : LISTADO
				4 : INFORMES
			FinSegun
			MENU
		FinMientras
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento INGRESO
			LIM := 0
			Para i = 1, 4, 1
				CanAni[i] := 0
			FinPara
			Ingresar i
			Mientras i <> 0
				Ingresar Ani[i].FEC, Ani[i].TIP
				Ani[i].VAC := 0
				Ani[i].ULT := 0 
				LIM += 1
				Segun Ani[i].TIP
					1 : CanAni[1] += 1
					2 : CanAni[2] += 2
					3 : CanAni[3] += 3
					4 : CanAni[4] += 4
				FinSegun
			FinMientras
		FinProcedimiento INGRESO
		Procedimiento VISITA
			Ingresar i
			Mientras i <> 0
				Ingresar FEC, VAC
				Ani[i].ULT := FEC
				Ani[i].VAC += VAC
			FinMientras
		FinProcedimiento VISITA
		Procedimiento LISTADO
			LIM2 := 0
			Para i = 1, LIM, 1
				Si Ani[i].VAC < 5
					AniAux[LIM2].FEC := Ani[i].FEC
					AniAux[LIM2].TIP := Ani[i].TIP
					AniAux[LIM2].VAC := Ani[i].VAC
					LIM2 += 1
				FinSi
			FinPara
			x := false
			Mientras x = false
				x := true
				Para i = 1, LIM2-1, 1
					Si AniOrd[i].FEC < AniOrd[i+1].FEC
						AniAux := AniOrd[i]
						AniOrd[i] := AniOrd[i+1]
						AniOrd[i+1] := AniAux
						x := false
					FinSi
				FinPara
			FinMientras
			Para i = 1, LIM2, 1
				Imprimir AniOrd[i].FEC, i, AniOrd[i].TIP, AniOrd[i].VAC
			FinPara
		FinProcedimiento LISTADO
		Procedimiento INFORMES
			Para i = 1, 4, 1
				Imprimir CanAni[i]
			FinPara
			VacMax := low_value
			CANP := 0
			Para i = 1, LIM, 1
				Si VacMax < Ani[i].VAC
					VacMax := Ani[i].VAC
					NroMax := i
					TipMax := Ani[i].TIP
				FinSi
				Si Ani[i].ULT := 0
					CANP += 1
				FinSi
			FinPara
			Imprimir NroMax, TipMax, CANP
		FinProcedimiento INFORMES
	Fin
```
## 03/10
### Enunciado
Una empresa tiene grabado un vector, de 2300 elementos que contienen los datos de sus clientes. El diseNo del vector es el siguiente: 
C-CUIT – Nro. de Cuit del cliente 
C-NOM – Nombre 
C-DIR – Dirección 
Además existe en memoria un vector de 9880 elementos que contiene los siguientes datos de cada una de las ventas realizadas durante el mes de Septiembre. 
V-CUIT – Nro. de Cuit del cliente 
V-DIA – Día del mes 
V-IMPO – Importe de la venta
Los vectores NO se encuentran ordenados. 
Se requiere desarrollar los siguientes módulos:

LISTADO 
Imprimir un listado, ORDENADO por Nro de Cuit, de los clientes que compraron en el mes que contenga: 
Nombre de cliente - Importe total comprado en el mes 
Finalizado el listado imprimir: 
Cantidad de clientes que compraron. Importe total de ventas del mes

CONSULTA 
Ingresar por teclado un día del mes de septiembre y mostrar por pantalla:
Cantidad e importe total de ventas realizadas en el día.
### Solución
```Pascal
Program Empresa
	Type
		R-ImpoT = record
			Nom : string
			ImpoT : Real
		end
		R-Sept = record
			Tot : integer
			ImpoD : Real
		end
	Var
		i, j, k: integer
		ImpoT : array[1..2300] of R-ImpoT
		V2300 : array[1..2300] of R-cl
		V9880 : array[1..9880] of R-sp
		SPT : array[1..30] of R-Sept
		Aux2300 : R-cl
		ClienCom : integer
		ImpoT : Real
		x : boolean
		Dia : integer
	Inicio
		Para i = 1, 2300, 1
			ImpoT[i].ImpoT := 0
			ImpoT[i].Nom := V2300[i].C-Nom
		FinPara
		x := false
		Mientras x = false
			Para i = 1, 2299, 1
				x := true
				Si V2300[i].C-CUIT < V2300[i+1].C-CUIT
					Aux2300 := V2300[i]
					V2300[i] := V2300[i+1]
					V2300[i+1] := Aux2300
					x := false
				FinSi
			FinPara
		FinMientras
		Para k = 1, 30, 1
			SPT[k].Tot := 0
			SPT[k].ImpoD := 0
		FinPara
		Para i = 1, 2300, 1
			Para j = 1, 9880, 1
				Si V9880[j].V-CUIT = V2300[i].C-CUIT
					ImpoT[i].ImpoT += V9880[j].V-IMPO
				FinSi
				Para k = 1, 30, 1
					Si V9880[j].V-DIA = k
						SPT[k].Tot += 1
						SPT[k].ImpoD += V9880[i].V-IMPO 
					FinSi
				FinPara
			FinPara
		FinPara
		ClienCom, ImpoT := 0
		Para i = 1, 2300, 1
			Imprimir ImpoT[i].Nom, ImpoT[i].ImpoT
			Si ImpoT[i].ImpoT = 0
				ClienCom += 1
			FinSi
			ImpoT += ImpoT[i].ImpoT
		FinPara
		Imprimir ClienCom, ImpoT
		Ingresar Dia
		Mientras Dia <> 0
			Mostrar SPT[Dia].Tot, SPT[Dia].ImpoD
			Ingresar Dia
		FinMientras
	Fin
```
### Enunciado
Ejercicio: 
Calcular el valor del impuesto a los Bienes Personales. 
Se ingresa: 
- Apellido y Nombre del contribuyente 
- Valor total de los bienes
Con estos datos se debe imprimir: 
Apellido y Nombre – Valor Total de los Bienes – Impuesto a Pagar: 
Para el cálculo del Impuesto se debe tener en cuenta: 
a) Se aplica sobre el valor total de los bienes las siguientes alícuotas: 
hasta 2.000.000 = 0% 
de 2.000.001 a 5.000.000 = 1% sobre el excedente de 2.000.000 
mas de 5.000.000 = 2% sobre el excedente de 2.000.000 
b) Los cálculos deben efectuarse en un subprograma de tipo función (Cálculo). A la función Cálculo se le pasa como parámetro el valor total de bienes ingresado.
### Solución
```Pascal
Program Impuestos
	Var
		AyN : string
		Val : Real
	Inicio
		Ingresar AyN
		Mientras AyN <> " "
			Ingresar Val
			Imprimir AyN, Val, Calculo(Val)
			Ingresar AyN
		FinMientras
		Function Calculo(Impu: Real): Real;
		Var
			Monto : Real
		Begin
			Si BIEN[i].Val < 2000001
				Monto := BIEN[i].Val
			Sino
				Si BIEN[i].Val > 2000000 and BIEN[i].Val < 5000001
					Monto := (BIEN[i].Val-2000000)*0.01
				Sino
					Si BIEN[i].Val > 5000000
						Monto := (BIEN[i].Val-2000000)*0.02
					FinSi
				FinSi
			FinSi
			Impu := Monto
		end
	Fin
```
## 04/10
### Enunciado
El Juzgado de Faltas de un municipio debe procesar las infracciones que cometen los conductores de vehículos en la vía pública. El analista ha definido una serie de módulos que se deben codificar. Encarga a un programador codificar los siguientes:

Módulo Ingreso de Códigos de infracciones: Se encuentran catalogadas 455 infracciones y de cada una de ella se deben ingresar ls siguientes datos y almacenar los que correspondan en un array:
Codint- Código de infracción (rango de 1 2455)
Desinf- Descripción de la infracción (Ej. Conducir en estado de ebriedad, pasar semáforo en rojo, etc)
Mulinf= Multa que corresponde a la infracción (está expresado en litros de combustible)
El ingreso se realiza sin seguir orden alguno.

Módulo ingreso datos de infracciones: Luego de los operativos de control, se ingresan los datos de las actas labradas por los agentes de tránsito a los infractores:
Numact: Número de acta
NumDom: Dominio del vehículo infractor
NomCon : Nombre del conductor del vehículo
InfCom: Código de infracción cometida
InfSit: código de situación (1Impaga, 2-Cancelada) (grabar valor 2)
MulPag : Importe de la multa a pagar por el infractor (grabar valor cero)

Estos datos deben grabarse en un array. Se debe dimensionar con al menos 5000 elementos.

Módulo actualización: Cuando un infractor se presenta a abonar la multa por una infracción, se deben codificar las siguientes acciones
a) Ingresar al nico del módulo el mportedel litro de combustible.
b) Ingresar el número de acta y el dominio del ehículo infractor que se presenta,
c) Determinar sí el vehículo ha tenido otras infracciones (recorrer el arreglo contando la cantidad de infracciones del vehículo, sison mas de 1 es reincidente,
d) A continuación buscar en el arreglo el número de acta que el infractor quiere abonar.
e) Sino es reincidente actualizar el campo InfSit grabando valor 2 (sele perdona la multa), dejando en cero el campo MulPag,
f) Si es reincidente se calcula la multa multiplicando la multa que corresponde a la infracción (Mullnf por el valor del litro de combustible ingresado al nico del módulo y luego actualizar los campos InfSt y MulPag.

Aclaraciones: Codifiar con metodología modular.
### Solución
```Pascal
Program Faltas
	Type
		R-INF = record
			Codint : integer
			Desinf : string
			Mulinf : Real
		end
		R-DATINF = record
			Numact : integer
			NumDom : Real
			NomCon : string
			InfCom : integer
			InfSit : integer
			MulPag : integer
		end
	Var
		INF : array[1.455] of R-INF
		i : integer
		opcion : integer
	Inicio
		MENU
		Mientras opcion <> 0
			Segun opcion
				1 : CODINF
				2 : DATINF
				3 : ACT
			FinSegun
			MENU
		FinMientras
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento CODINF
			Ingresar i
			Mientras i <> 0
				Ingresar INF[i].CodInt, INF[i].Desinf, INF[i].Mulinf
				Ingresar i
			FinMientras
		FinProcedimiento CODINF
		Procedimiento DATINF
			Var
				DATINF : array[1..5000] of R-DATINF
				LIM : integer
			Inicio
				LIM := 0
				Ingresar i
				Mientras i <> 0
					Ingresar DATINF[i].Numact, DATINF[i].NumDom, DATINF[i].NomCon, DATINF[i].InfCom
					DATINF[i].InfSit := 2
					DATINF[i].MulPag := 0
					LIM += 1
					Ingresar i
				FinMientras
		FinProcedimiento DATINF
		Procedimiento ACT
			
		FinProcedimiento
	Fin
```
## 10/10
### Enunciado
Calcular el valor del impuesto a los Bienes Personales.
Se ingresa: 
- Apellido y Nombre del contribuyente 
- Valor total de los bienes 
Con estos datos se debe imprimir:
Apellido y Nombre – Valor Total de los Bienes – Impuesto a Pagar
Para el cálculo del Impuesto se debe tener en cuenta: 
a) Se aplica sobre el valor total de los bienes las siguientes alícuotas: 
hasta 2.000.000 = 0% 
de 2.000.001 a 5.000.000 = 1% sobre el excedente de 2.000.000 
mas de 5.000.000 = 2% sobre el excedente de 2.000.000 
b) Los cálculos deben efectuarse en un subprograma de tipo función (Cálculo). 
A la función Cálculo se le pasa como parámetro el valor total de bienes ingresado.
### Solución
 - terminar el anterior
## 11/10
### Enunciado
![[Estudios/FCAD/Licenciatura en Sistemas/1° Primer aNo/Algoritmos y programación/Anexos/Practico 1 -Parametros 2022.pdf]]
### Solución
 -
## 13/10
### Enunciado
Una institución bancaria necesita procesar los datos de los usuarios de tarjetas de crédito. Para ello ingresa por teclado los siguientes datos de cada usuario: 
NUM- Nº de tarjeta 
NOM- Nombre del titular 
LIM – Importe límite de compra 
SAL – Importe del saldo a pagar 
Se requiere desarrollar los siguientes módulos: 
1. Ingreso de Datos
Ingresar los datos de los usuarios y guardarlos en un vector cuyo diseNo queda a criterio del programador
Los datos se ingresan SIN SEGUIR ORDEN ALGUNO. 
2. Compras. 
Procesar las compras realizadas. Para ello se ingresan por teclado los siguientes datos:
TAR – Nº de tarjeta 
FEC – Fecha de la compra 
IMPO – Importe de la compra 
Se debe controlar que la suma del saldo a pagar más el importe de la compra no supere el límite de compra. 
- En caso de superar se debe rechazar la operación. 
- Si está dentro del límite de compra se debe actualizar el campo SAL. 
3. Listado Imprimir un listado ordenado por Nº de tarjeta que contenga:
Nº de tarjeta – Nombre titular – Importe de saldo a pagar
Finalizado el listado imprimir:
- Nombre y Nº de tarjeta del usuario de mayor saldo a pagar. 
- Importe total a pagar por todos los usuarios discriminados. 
- Cantidad de usuarios con saldo a pagar 0 (cero) 
4. Consulta Desarrollar un módulo de consulta dónde ingresando el Nº de tarjeta muestre por pantalla:
- Nombre del titular 
- Saldo disponible de compra
### Solución
 -
## 17/10
### Enunciado
Una empresa constructora necesita procesar los datos de cada uno de los proyectos de construcción de barrios que tiene en distintos estado de desarrollo.
Luego de un relevamiento se establece la necesidad de desarrollar los siguientes módulos: 
INGRESO DE DATOS
De cada proyecto se ingresan los siguientes datos que deben ser grabados en un archivo secuencial, cuyo diseNo queda a criterio del programador:
- COD - Código de Proyecto 
- NOM - Nombre del Cliente 
- CAN - Cantidad de viviendas a construir 
- PRE - Presupuesto 
- COS - Código de situación [ 1-No Iniciado, 2-En desarrollo, 3-Terminado, 4-Entregado ] 
ACTUALIZACIÓN DE PRESUPUESTOS 
Producto del proceso inflacionario, la empresa decide ajustar los presupuestos de los proyectos. Se han definido las siguientes pautas de aumento de presupuesto: 
- 20% de aumento para proyectos no iniciados 
- 10% de aumento para proyectos en desarrollo 
Se deben actualizar los presupuestos (campo PRE) de todos los proyectos que cumplan los requisitos según pautas anteriores. 
CONSULTA 
Se ingresa por teclado el código de situación y se debe imprimir un listado que contenga los datos de los proyectos que estén en la situación ingresada.. INFORMES
Imprimir:
- Cantidad de proyectos discriminados por código de situación. 
- Nombre del cliente y código del proyecto de mayor presupuesto
- Cantidad total de viviendas a construir en todos los proyectos
Debe utilizarse estrategia modular
### Solución

### Enunciado
La Sociedad Protectora de Animales necesita implementar un sistema que le permita procesar los datos de las atenciones realizadas a los distintos animales que son rescatados de la vía pública. Para ello se requiere desarrollar los siguientes módulos:
INGRESO. 
Ingresar los datos de cada animal y guardarlos en un archivo secuencial, cuyo diseNo queda a criterio del programador. 
Los datos que se ingresan son los siguientes: 
NRO – Nº de Ficha 
FEC – Fecha de Ingreso 
TIP – Tipo 1- Perro 2- Gato 3- Caballo 4- Otros 
VAC – Cantidad de vacunas aplicadas 
ULT – Fecha última visita veterinaria 
La fecha de última visita veterinaria y cantidad de vacunas aplicadas debe ingresarse con valor 0 (cero). 
VISITA.
Cada vez que el veterinario revisa un animal se ingresan por teclado los siguientes datos: 
NRO – Nº de ficha 
FEC – Fecha de visita 
VAC – Cantidad de Vacunas aplicadas 
Con los datos ingresados se debe actualizar la fecha última visita (ULT) y la cantidad de vacunas aplicadas (VAC) 
LISTADO. Imprimir un listado de todos aquellos animales que recibieron menos de 5 vacunas con el siguiente diseNo: 
Fecha Ingreso – Nº de Ficha - Tipo – Cantidad de Vacunas aplicadas 
INFORMES. 
Imprimir:
- Cantidad de animales alojados discriminados por tipo. 
- Nro. de Ficha y Tipo del animal que más vacunas recibió. 
- Cantidad de perros que todavía no han sido visitados por el veterinario.
### Solución
 -
## 24/10
### Enunciado
Un empaque de fruta necesita procesar los datos de las distintas partidas recibidas durante el mes de Septiembre. Para ello cada vez que llega una partida al empaque se obtienen los siguientes datos:
NUM- Nº de partida 
DIA – Día del mes 
PRO- Nombre del productor 
DES- Destino( 1-Industria ; 2-Mercado Interno; 3-Exportación ) 
KIL- Cantidad de kilos 
Se requiere desarrollar los siguientes módulos:
1. INGRESO 
Ingresar los datos de las partidas y guardarlas en un archivo secuencial cuyo diseNo queda a criterio del programador. 
2. CONSULTA Ingresar el número de partida y mostrar por pantalla los datos de la partida ingresada. 
3. LISTADO Imprimir un listado de todas las partidas ORDENADO por día del mes que contenga: 
Día del mes – Nº de Partida – Cantidad de kilos 
Al finalizar el listado imprimir:
- Cantidad de partidas y total de kilos enviados a exportación.
- Nombre del productor y Nro. de partida de la partida de mayor peso
### Solución
 -
## 25/10
### Enunciado
Un empaque de fruta necesita procesar los datos de las distintas partidas recibidas durante el mes de Septiembre. Para ello cada vez que llega una partida al empaque se obtienen los siguientes datos:
NUM- Nº de partida 
DIA – Día del mes 
PRO- Nombre del productor 
DES- Destino ( 1-Industria ; 2-Mercado Interno; 3-Exportación ) 
KIL- Cantidad de kilos
Se requiere desarrollar los siguientes módulos:
1. INGRESO
Ingresar los datos de las partidas y guardarlas en un archivo de ACCESO DIRECTO PARTIDAS cuyo diseNo queda a criterio del programador.
2. CONSULTA 
Ingresar el número de partida y mostrar por pantalla los datos de la partida ingresada. 
3. LISTADO 
Imprimir un listado de todas las partidas ORDENADO por día del mes que contenga : 
Día del mes – Nº de Partida – Cantidad de kilos 
Al finalizar el listado imprimir: 
- Cantidad de partidas y total de kilos enviados a exportación. 
- Nombre del productor y Nro. de partida de la partida de mayor peso.
### Solución
 -
## 29/10
### Enunciado
Una empresa constructora necesita procesar los datos de cada uno de los proyectos de construcción de barrios que tiene en distintos estado de desarrollo. 
Luego de un relevamiento se establece la necesidad de desarrollar los siguientes módulos:
INGRESO DE DATOS 
De cada proyecto se ingresan los siguientes datos que deben ser grabados en un archivo de ACCESO DIRECTO, cuyo diseNo queda a criterio del programador:
- COD - Código de Proyecto
- NOM - Nombre del Cliente 
- CAN - Cantidad de viviendas a construir 
- PRE - Presupuesto 
- COS - Código de situación [ 1-No Iniciado, 2-En desarrollo, 3-Terminado, 4-Entregado ] 
ACTUALIZACIÓN DE PRESUPUESTOS 
Producto del proceso inflacionario, la empresa decide ajustar los presupuestos de los proyectos. Se han definido las siguientes pautas de aumento de presupuesto:
- 20% de aumento para proyectos no iniciados
- 10% de aumento para proyectos en desarrollo 
Se deben actualizar los presupuestos (campo PRE) de todos los proyectos que cumplan los requisitos según pautas anteriores. 
CONSULTA 
Se ingresa por teclado el código de proyecto y se debe mostrar por pantalla todos los datos del proyecto ingresado. 
LISTADO 
Imprimir un listado de todos los proyectos ordenado por nombre del cliente que conentga: 
Nombre del cliente – Cantidad de viviendas a construir – Código de situación 
Al finalizar el listado imprimir: 
- Cantidad de proyectos discriminados por código de situación. 
- Nombre del cliente y código del proyecto de mayor presupuesto 
- Cantidad total de viviendas a construir en todos los proyectos
### Solución

### Enunciado
La Sociedad Protectora de Animales necesita implementar un sistema que le permita procesar los datos de las atenciones realizadas a los distintos animales que son rescatados de la vía pública. Para ello se requiere desarrollar los siguientes módulos:
INGRESO. 
Ingresar los datos de cada animal y guardarlos en un archivo de ACCESO DIRECTO , cuyo diseNo queda a criterio del programador. Los datos que se ingresan son los siguientes:
NRO – Nº de Ficha 
FEC – Fecha de Ingreso 
TIP – Tipo 1- Perro 2- Gato 3- Caballo 4- Otros 
VAC – Cantidad de vacunas aplicadas 
ULT – Fecha última visita veterinaria 
La fecha de última visita veterinaria y cantidad de vacunas aplicadas debe ingresarse con valor 0 (cero). 
VISITA. Cada vez que el veterinario revisa un animal se ingresan por teclado los siguientes datos:
NRO – Nº de ficha 
FEC – Fecha de visita 
VAC – Cantidad de Vacunas aplicadas 
Con los datos ingresados se debe actualizar la fecha última visita (ULT) y la cantidad de vacunas aplicadas (VAC) 
LISTADO. 
Imprimir un listado de todos aquellos animales que recibieron menos de 5 vacunas ORDENADO por fecha de ingreso con el siguiente diseNo:
Fecha Ingreso – Nº de Ficha - Tipo – Cantidad de Vacunas aplicadas
INFORMES.
Imprimir:
- Cantidad de animales alojados discriminados por tipo.
- Nro. de Ficha y Tipo del animal que más vacunas recibió. 
- Cantidad de perros que todavía no han sido visitados por el veterinario.

### Solución -
## 31/10
### Enunciado PT1
El área de mantenimiento de una represa hidroeléctrica necesita desarrollar un algoritmo que le permita procesar las tareas de reparación realizadas en cada una de sus 14 turbinas durante el mes de setiembre. Para ello dispone en memoria de un archivo secuencial repara, cuyo registro contiene los siguientes datos de cada reparación realizada:
repara acceso secuencial
NUM _ Nº de turbina  (Clave principal)
DIA _ Día del mes 
TIE _ Tiempo de reparación en Hs. 
DES _ Descripción de la falla 
COS _ Costo de total reparación 
Además tiene grabado en disco el siguiente archivo: 
TURBINAS Acceso DIRECTO 
NUM _ Nº de turbina ( Clave principal ) 
MAR_ Marca de la turbina 
CAN _ Cantidad de veces que falló
TIE _ Total de horas de reparación 
COS _ Costo total de reparaciones Se requiere desarrollar el siguiente módulo:
ACTUALIZACION. 
Actualizar los datos CAN, TIE y COS del archivo tomando como base el archivo.
### Solución

### Enunciado PT2

### Solución
Tomando como base los archivos procesados en el punto anterior, desarrollar los siguientes módulos:
CONSULTA. 
Desarrollar un módulo de consulta, dónde ingresando el Nº de turbina, muestre por pantalla el siguiente informe de todas las reparaciones realizadas durante el mes de septiembre:
Nº de Turbina – Marca 
Día – Tiempo de Reparación –Descripción de la falla

LISTADO. 
Imprimir un listado ordenado por Nº de turbina con el siguiente diseNo:
Nº turbina – Tiempo total de reparaciones en el mes – Costo total de reparaciones en el mes 

Al finalizar el listado imprimir el Nº de turbina que estuvo más tiempo parada en el mes. -

## 01/10
### Enunciado
Una compaNía de seguros necesita procesar los datos de las pólizas de automotores que fueron emitidas durante el mes de Septiembre. Para ello de cada póliza dispone de los siguientes datos: 
PAT - Nº de patente del automotor 
DIA - Día de emisión de la póliza ( 1..30 ) 
PRO - Nombre del propietario 
MAR - Marca del automotor 
ANO – ANo de fabricación 
TIP - Tipo de seguro 
1- Terceros 2- DaNo Parcial 3- DaNo Total 

Se requiere desarrollar los siguientes módulos: 
1. Ingreso de Pólizas Ingresar los datos de las pólizas y guardarlas en un archivo de acceso directo cuyo diseNo queda a criterio del programador.
2. Consulta Pólizas Ingresar el Nº de Patente y mostrar por pantalla todos los datos correspondientes a la póliza. 
3. Listado de Pólizas Imprimir un listado de todas las pólizas ordenadas por nombre del propietario que contenga: 
Nombre propietario – Nº de patente – Marca automotor – Importe del seguro 
El importe a pagar se encuentra en un archivo directo cuyo diseNo es el siguiente: 
TIP – Tipo de seguro ( Clave principal ) 
IMS – Importe del seguro 

Al finalizar el listado imprimir: 
- Cantidad total de pólizas e importe total a cobrar discriminado por tipo de seguro. 
- Día del mes en que se emitieron la mayor cantidad de pólizas

### Solución

## 01/11
### Enunciado
Una bodega necesita implementar un sistema que le permita procesar los datos de las partidas de vino tinto producidas durante el mes de noviembre. Para ello se ingresan por teclado los siguientes datos de cada partida:
Día del mes - Hora - Nº Partida - Código de variedad (Rango de 1 a 9) - Cantidad de litros 

Se requiere desarrollar los siguientes módulos: 
1. INGRESO 
Ingresar los datos de las partidas y guardarlos en una estructura de datos cuyo tipo y diseNo queda a criterio del programador. Además actualizar el archivo de acceso directo ya existente (ya está grabado en memoria auxiliar), cuyo registro tiene el siguiente diseNo:
V-REG V-SAP – Código de variedad (Clave principal) 
V-NOM – Nombre de variedad (Clave alternativa) 
V-LIT – Cantidad de litros producidos 
Se debe actualizar el campo V-LIT. 
2. LISTADO 
Imprimir un listado de los datos ingresados ordenado por día con el siguiente diseNo: 
Día – Nº de partida – Nombre de Variedad – Cantidad de Litros 
El nombre de las variedades se ingresan al comienzo del algoritmo. 
3. CONSULTA
Desarrollar un módulo de consulta dónde ingresando el día del mes nos muestre el total de litros producidos en el día. 
4. INFORMES
Imprimir: 
- Cantidad total de partidas y cantidad de litros producidos en el mes. 
- Variedad que más litros se produjo en el mes.

### Solución

## 23/11
### Enunciado
Una concesionaria de automóviles necesita implementar un sistema que le permita consultar y procesar los datos de los distintos vehículos que tiene para la venta. Para ello tiene grabado un archivo directo que contiene los datos de los vehículos disponibles en la concesionaria:
Archivo. Acceso directo 
03 A-NRO - Nro. de patente ( clave principal ) 
03 A-NOM - Nombre del propietario
03 A-MAR - Marca del vehículo 
03 A-TIP - Tipo de vehículo (1..12) 
03 A-PRE - Precio de Venta 
03 A-EST - Estado 1 – Disponible para la venta 2- Vendido 3- En taller 

Se requiere desarrollar los siguientes módulos: 
1. CONSULTA. 
Donde ingresando el tipo de vehículo muestre por pantalla todos los vehículos de ese tipo disponible para la venta. Se debe mostrar: 
Marca del vehículo – Nombre propietario – Precio de Venta 
2. VENTAS.
Ingresando el Nro. de patente se debe verificar que el vehículo esté disponible para la venta y en caso de estarlo actualizar el campo A-EST del archivo y grabar un archivo secuencial con los datos de los vehículos vendidos. 
3. INFORMES. 
Teniendo en cuenta que la comisión para la concesionaria es un 5 % del precio de venta imprimir el importe total cobrado de comisión por la concesionaria por todas las ventas realizadas. 
- Cantidad de vehículos disponibles para la venta discriminados por tipo. 
- Nro. de patente y nombre del propietario del vehículo más caro que se haya vendido

### Solución
# Exámenes
![[FCAD/Licenciatura en Sistemas/1° Primer aNo/Algoritmos y programación/Anexos/Imagen de WhatsApp 2023-02-27 a las 14.04.51.jpg]]
![[FCAD/Licenciatura en Sistemas/1° Primer aNo/Algoritmos y programación/Anexos/Imagen de WhatsApp 2023-03-02 a las 21.02.40.jpg]]
# Tarea David Mena 09-10 del 03/22
## Examen final regular 20-02-22
### Enunciado
**1.RESUELVA EL SIGUIENTE ALGORITMO**
Una unidad carcelaria necesita desarrollar un algoritmo que le permita controlar y obtener información de las visitas que familiares y amigos realizan a los detenidos alojados en distintos pabellones. Para ello se ingresan por teclado los siguientes datos de cada detenido:
DOC - Número de documento
NOM – Nombre del detenido
SALI - Nº de pabellón donde está alojado (1..17)
ING - Fecha de ingreso
SAL – Fecha de salida
EDAD – Edad del detenido
CAN - Cantidad de visitas
Se requiere desarrollar los siguientes módulos :
**INGRESO**
Ingresar los datos de los detenidos y grabarlos en un archivo directo </CARCEL> cuyo diseNo y claves de acceso queda a criterio del programador.
**VISITAS**
Cada vez que un detenido recibe una visita se ingresan por teclado los siguientes datos del visitante :
DIA - Día de la visita
HOR – Hora de entrada
NOV – Nombre visitante
DOD - Nro de documento del detenido que visita
Grabar los datos de cada visita en un archivo secuencial y actualizar el campo CAN del archivo </CARCEL>.
**LISTADO**
Desarrollar un módulo de consulta dónde ingresando el Nro. de pabellón imprima un listado ordenado por nombre de todos los detenidos alojados en el pabellón ingresado.
**INFORMES**
Imprimir: 
- Nº de pabellón que aloja la mayor cantidad de detenidos.
- Cantidad total de detenidos.
- Nombre y Nro documento del detenido que más tiempo lleva en la cárcel.

### Solución
```Pascal
Program carcel
	Type
		R-C = record
			DOC : integer; Clave principal
			NOM : string
			SAL : integer
			ING : string
			SALI : string
			EDAD : integer
			CAN : integer
		end
		R-V = record
			DIA : string
			HOR : string
			NOV : string
			DOD : integer
		end
	Var
		CAR : file of R-C
		VIS : file of R-V
		opcion : integer
		i : integer
	Inicio
		MENU
		Mientras opcion <> 0
			Segun opcion
				1 : INGRESO
				2 : VISITAS
				3 : LISTADO
				4 : INFORMES
			FinSegun
			MENU
		FinMientras
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento INGRESO
			ASSIGN (CAR, "CARCEL.dat")
			ABRIR (CAR)
			Ingresar CAR.DOC
			Mientras CAR.DOC <> 0
				Ingresar CAR.NOM, CAR.SAL, CAR.ING, CAR.SALI, CAR.EDAD, CAR.EDAD, CAR.CAN
				GRABAR (CAR)
				Ingresar CAR.DOC
			FinMientras
			CERRAR (CAR)
		FinProcedimiento INGRESO
		Procedimiento VISITAS
			Var
				DOC : integer
			Inicio
				ASSIGN (VIS, "VISITAS.dat")
				ABRIR (VIS)
				ABRIR (CAR)
				Ingresar VIS.DOD
				Mientras VIS.DOD <> 0
					Ingresar VIS.DIA, VIS.HOR, VIS.NOV
					GRABAR (VIS)
					DOC := VIS.DOD
					LEER (CAR) (DOC)
					Si L.V. (CAR)
						CAR.CAN += 1
						REGRABAR (CAR)
					FinSi
					Ingresar VIS.DOD
				FinMientras
				CERRAR (CAR)
				CERRAR (VIS)
			Fin
		FinProcedimiento VISITAS
		Procedimiento LISTADO
			Var
				PAB : array[1..17] of string
				Nro : integer
				LIM : integer
				BAN : Boolean
				AUX : string
			Inicio
				Ingresar Nro
				Mientras Nro <> 0
					ABRIR (CAR)
					CAR.DOC := 0
					LIM := 0
					LEER (CAR) (CAR.DOC) Próximo
					Mientras NOEOF (CAR)
						Si Nro = CAR.SALI
							LIM += 1
							PAB(LIM) := CAR.NOM
						FinSi
						LEER (CAR) (CAR.DOC) Próximo
					FinMientras
					CERRAR (CAR)
					BAN := FALSE
					Mientras BAN = FALSE
						BAN := TRUE
						Para i = 1, LIM-1, 1
							Si APAB(LIM) < APAB(LIM+1)
								AUX := APAB(LIM)
								APAB(LIM) := APAB(LIM+1)
								APAB(LIM+1) := AUX
								BAN := FALSE
							FinSi
						FinPara
					FinMientras
					Para i = 1, LIM, 1
						Imprimir PAB(i)
					FinPara
					Ingresar Nro
				FinMientras
			Fin
		FinProcedimiento LISTADO
		Procedimiento INFORMES
			Var
				CANPAB : array[1..17] of integer
				NPABMAX : integer
				NMAX : integer
				CANT : integer
				NOMMAX : string
				NROMAX : integer
				TIEMAX : string
			Inicio
				ABRIR (CAR)
				Para i = 1, 17, 1
					CANPAB(i) := 0
				FinPara
				CAR.DOC := 0
				TIEMAX := low_value
				LEER (CAR) (CAR.DOC) Próximo
				Mientras NOEOF (CAR)
					CANPAB(CAR.SALI) += 1
					LEER (CAR) (CAR.DOC) Próximo
					Si TIEMAX < CAR.ING
						TIEMAX := CAR.ING
						NROMAX := CAR.DOC
						NOMMAX := CAR.NOM
					FinSi
				FinMientras
				NMAX, CANT := 0
				Para i = 1, 17, 1
					Si NMAX < CANPAB(i)
						NMAX := CANPAB(i)
						NPABMAX := i
					FinSi
					CANT += CANPAB(i)
				FinPara
				Imprimir NPABMAX, CANT, NROMAX, NOMMAX
				CERRAR (CAR)
			Fin
		FinProcedimiento INFORMES
	Fin
```

## Examen final libre 20-02-22
### Enunciado
**1.RESUELVA EL SIGUIENTE ALGORITMO**
Una compaNía de telefonía celular necesita implementar un sistema que le permita procesar los datos de los consumos realizados por sus clientes durante el mes de noviembre.
Para ello dispone, ya grabado en memoria, de un archivo secuencial </LLAMADAS> que contiene la siguiente información de cada llamada realizadas por sus clientes :
Archivo </LLAMADAS> Acceso secuencial

NRO - Número de Celular
DIA - Día del mes
MIN – Minutos que duró la llamada

Los registros se encuentran grabados sin seguir orden alguno.
Se requiere desarrollar los siguientes módulos :
**LISTADO**
- Imprimir un listado de las llamadas realizadas en el mes ordenado por número de celular que contenga :
Número de celular – Cantidad de minutos – Importe de la llamada 
El importe a pagar por la llamada se calcula teniendo en cuenta que el costo por minuto es de $ 55,00 .
Al finalizar el listado imprimir :
- Cantidad de llamadas realizadas
- Importe total a pagar en el mes
- Día y número de celular que realizó la llamada de mayor importe.

**ACTUALIZACION**
Tomando como base los datos grabados en el archivo </LLAMADAS> actualizar el archivo directo </CELULAR> ya existente cuyo diseNo de registro es el siguiente :
Archivo </CELULAR> Acceso directo
NRO – Número de celular (Clave principal)
NOM – Nombre del titular (Clave alternativa)
MIN – Tiempo total de uso del celular
CAN – Cantidad total de llamadas realizadas

Se deben actualizar los campo MIN y CAN.
**INFORMES**
Imprimir :
- Cantidad total de celulares procesados.
- Día del mes que se realizaron la menor cantidad de llamadas.

### Solución
```Pascal
Program 
	Var
		opcion : integer
		i : integer
	Inicio
		MENU
		Mientras opcion <> 0
			Segun opcion
				1 : LISTADO
				2 : ACTUALIZACIOM
				3 : INFORMES
			FinSegun
			MENU
		FinMientras 
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento LISTADO
			Type
				R-NC = record
					NRO : integer
					MIN : Real
					COS : Real
				end
			Var
				NCO : array[1..99999] of R-NC
				LIM : integer
				AUX : R-NC
				CANT : integer
				IMPT : Real
				x : Boolean
				DIAMAX : string
				NROMAX : integer
				COSMAX : Real
			Inicio
				ASSIGN (LLAMADAS, "Llamadas.dat")
				ABRIR (LLAMADAS)
				LLAMADAS.NRO := 0
				LIM := 0
				CANT := 0
				IMPT := 0
				COSMAX := low_value
				LEER (LLAMADAS) (LLAMADAS.NRO) Próximo
				Mientras NOEOF (LLAMADAS)
					LIM += 1
					NCO(LIM).NRO := LLAMADAS.NRO
					NCO(LIM).MIN := LLAMADAS.MIN
					NCO(LIM).COS := LLAMADAS.MIN*55
					Si COSMAX < NCO(LIM).COS
						COSMAX := NCO(LIM).COS
						NROMAX := NCO(LIM).NRO
						DIAMAX := LLAMADAS.DIA
					FinSi
					CANT += 1
					LEER (LLAMADAS) (LLAMADAS.NRO) Próximo
				FinMientras
				x = FALSE
				Mientras x = FALSE
					x = TRUE
					Para i = 1, LIM-1, 1
						Si NCO(i).NRO < NCO(i+1).NRO
							AUX := NCO(i)
							NCO(i) := NCO(i+1)
							NCO(i+1) := AUX
							x = FALSE
						FinSi
					FinPara
				FinMientras
				Para i = 1, LIM, 1
					Imprimir NCO(i).NRO, NCO(i).MIN, NCO(i).COS
					IMPT += NCO(i).COS
				FinPara
				Imprimir CANT, IMPT, DIAMAX, NROMAX
				CERRAR (LLAMADAS)
			Fin
		FinProcedimiento LISTADO
		Procedimiento ACTUALIZACION
			ASSIGN (CELULAR, "Celular.dat")
			ABRIR (LLAMADAS)
			ABRIR (CELULAR)
			LLAMADAS.NRO := 0
			LEER (LLAMADAS)(LLAMADAS.NRO)Próximo
			Mientras NOEOF (LLAMADAS)
				NRO := LLAMADAS.NRO
				LEER (CELULAR) (NRO)
				Si (L.V.) (CELULAR)
					CELULAR.MIN += LLAMADAS.MIN
					CELULAR.CAN += 1
				FinSi
				REGRABAR (CELULAR)
				LEER (LLAMADAS)(LLAMADAS.NRO)Próximo
			FinMientras
			CERRAR (CELULAR)
			CERRAR (LLAMADAS)
		FinProcedimiento ACTUALIZACION
		Procedimiento INFORMES
			Var
				DLLM : array[1..31] of integer
				CANT : integer
				DMINAUX : string
				DMIN : integer
			Inicio
				ABRIR (CELULAR)
				ABRIR (LLAMADAS)
				Para i = 1, 31, 1
					DLLM(i) := 0
				FinPara
				CANT := 0
				TMIN := high_value
				CELULAR.NRO := 0
				LEER (CELULAR) (CELULAR.NRO) Próximo
				Mientras NOEOF (CELULAR)
					CANT += 1
					LEER (CELULAR) (CELULAR.NRO) Próximo
				FinMientras
				Imprimir CANT
				LLAMADAS.NRO := 0
				LEER (LLAMADAS) (LLAMDAS.NRO) Próximo
				Mientras NOEOF (LLAMADAS)
					DLLIM(LLAMADAS.DIA) += 1 
					LEER (LLAMADAS) (LLAMDAS.NRO) Próximo
				FinMientras
				DMIN := " "
				Para i = 1, 31, 1
					Si DMINAUX < DLLIM(i)
						DMINAUX := DLLIM(I)
						DMIN := i
					FinSi
				FinPara
				Imprimir DMIN
				CERRAR (LLAMADAS)
				CERRAR (CELULAR)
			Fin
		FinProcedimiento INFORMES
	Fin
	Fin
```
## Examen final regular 28-03-23
### Enunciado
Una productora agropecuaria necesita implementar un sistema que le permita procesar los datos de las atenciones veterinarias realizadas a los distintos animales que están alojados en 12 corrales distintos.
Para ello se requiere desarrollar los siguientes módulos:
**INGRESO.**
Ingresar los datos de cada animal y guardarlos en un archivo directo </ANIMALES>, cuyo diseNo queda a criterio del programador.
Los datos que se ingresan son los siguientes :
A-NRO – Nº de Ficha
A-NAC – Fecha de nacimiento
A-TIPO – Tipo 1- Toro 2- Vaca 3- Ternera/o 4- Novillo
A-COR – Nº corral dónde está alojado (1..12)
A-ULT – Fecha última visita veterinaria
A-PES – Peso en Kg
-   La fecha de última visita veterinaria y el peso debe ingresarse con valor 0 (cero)
**VISITA**
Cada vez que el veterinario revisa un animal se ingresan por teclado los siguientes datos:
NRO – Nº de ficha
FEC – Fecha de visita
PES – Peso en Kg.
Con los datos ingresados se debe grabar un archivo secuencial </VISITAS> y además actualizar la fecha de última visita (A-ULT) y el peso (A-PES) del archivo </ANIMALES>
**LISTADO.**
Imprimir un listado ordenado por fecha de nacimiento de todos los novillos que pesan menos de 500 Kg. , con el siguiente diseNo :
Fecha nacimiento – Nº de Ficha - Peso del animal
**INFORMES.**
Imprimir : - Listado discriminado por Nº de corral que contenga :
Nº de corral - Cantidad total de animales alojados
- Nº de Ficha y Tipo del animal de mayor peso.
- Cantidad de vacas que todavía no han sido visitadas por el veterinario.
## Solución
```Pascal
Program productora
	Type
		R-A = record
			A-NRO : integer
			A-NAC : string
			A-TIP : integer
			A-COR : integer
			A-ULT : string
			A-PES : Real
		end
		R-V = record
			NRO : integer
			FEC : string
			PES : Real
		end
	Var
		ANIMALES : file of R-A
		VISITAS : file of R-V
		opcion : integer
	Inicio
		MENU
		Mientras opcion <> 0
			Segun opcion
				1 : INGRESO
				2 : VISITA
				3 : LISTADO
				4 : INFORMES
			FinSegun
			MENU
		FinMientras
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento INGRESO
			ASSIGN (ANIMALES, "Animales.dat")
			ABRIR (ANIMALES)
			Ingresar ANIMALES.A-NRO
			Mientras ANIMALES.A-NRO <> 0
				Ingresar ANIMALES.A-NAC, ANIMALES.A-TIPO, ANIMALES.A-COR
				ANIMALES.A-ULT := 0
				ANIMALES.A-PES := 0
				GRABAR (ANIMALES)
				Ingresar A-NRO
			FinMientras
			CERRAR (ANIMALES)
		FinProcedimiento INGRESO
		Procedimiento VISITA
			Var
				NRO : integer
				FEC : string
				PES : Real
			Inicio
				ASSIGN (VISITAS, "Visitdas.dat")
				ABRIR (VISITAS)
				ABRIR (ANIMALES)
				Ingresar VISITAS.NRO
				Mientras VISITAS.NRO <> 0
					Ingresar VISITAS.FEC, VISITAS.PES
					GRABAR (VISITAS)
					NRO := VISITAS.NRO
					FEC := VISITAS.FEC
					PES := VISITAS.PES
					LEER (ANIMALES)(NRO)
						Si LV (Animales)
							ANIMALES.A-PES := PES
							ANIMALES.A-ULT := FEC
						Sino
							"El número de ficha no fue encontrado"
						FinSi
					Ingresar VISITAS.NRO
				FinMientras
				CERRAR (ANIMALES)
				CERRAR (VISITAS)
			Fin
		FinProcedimiento VISITA
		Procedimiento LISTADO
				
			Inicio
				
			Fin
		FinProcedimiento LISTADO
	Fin
```
### Solución
```Pascal
Program agropecuaria
	Type
		R-A = record
			A-NRO : integer; Clave principal
			A-NAC : string; Clave secundaria
			A-TIPO : integer
			A-COR : integer
			A-ULT : string
			A-PES : Real
		end
		R-V = record
			NRO : integer
			FEC : string
			PES : Real
		end
	Var
		VISITAS : file of R-V;
		ANIMALES : file of R-A;
		opcion : integer
	Inicio
		MENU
		Mientras opcion <> 0
			Segun opcion
				1 : INGRESO
				2 : VISITA
				3 : LISTADO
				4 : INFORMES
			FinSegun
			MENU
		FinMientras
		Procedimiento MENU
			Mostrar "Ingrese opción"
			Ingresar opcion
		FinProcedimiento MENU
		Procedimiento INGRESO
			ASSIGN (ANIMALES, "Animales.dat")
			ABRIR (ANIMALES)
			Ingresar ANIMALES.A-NRO
			Mientras ANIMALES.A-NRO <> 0
				Ingresar ANIMALES.A-NRO, ANIMALES.A-NAC, ANIMALES.A-TIPO, ANIMALES.A-COR
				ANIMALES.A-PES := 0
				ANIMALES.A-ULT := 0
				GRABAR (ANIMALES)
				Ingresar ANIMALES.A-NRO
			FinMientras
			CERRAR (ANIMALES)
		FinProcedimiento INGRESO
		Procedimiento VISITA
			Var
				NRO : integer
				PES : Real
				FEC : string
			Inicio
				ASSIGN (VISITAS, "Visitas.dat")
				ABRIR (VISITAS)
				ABRIR (ANIMALES)
				Ingresar VISITAS.NRO
				Mientras VISITAS.NRO
					Ingresar VISITAS.FEC, VISITAS.PES
					NRO := VISITAS.NRO
					PES := VISITAS.PES
					FEC := VISITAS.FEC
					LEER (ANIMALES) (NRO)
					Si (L.V.) (ANIMALES)
						ANIMALES.A-ULT := FEC
						ANIMALES.A-PES := PES
					Sino
						Mostrar "El animal no existe en la base de datos"
					FinSi
					Ingresar VISITAS.NRO
				FinMientras
				CERRAR (ANIMALES)
				CERRAR (VISITAS)
			    Fin
			FinProcedimiento VISITA
			Procedimiento LISTADO
				Type
					R-O = record
						NAC : string
						NRO : integer
						PES : Real
					end
				Var
					ORD : array[1..9999] of R-O
					LIM : integer
					AUX : R-O
					x : Boolean
				Inicio
					ABRIR (ANIMALES)
					LIM := 0
					ANIMALES.NRO := 0
					LEER (ANIMALES) (ANIMALES.NRO) Próximo
					Mientras NOEOF (ANIMALES)
						Si ANIMALES.A-PES < 501
							LIM += 1
							ORD(LIM).NAC := ANIMALES.A-NAC
							ORD(LIM).NRO := ANIMALES.A-NRO
							ORD(LIM).PES := ANIMALES.A-PES
						FinSi
						LEER (ANIMALES) (ANIMALES.NRO) Próximo
					FinMientras
					x := FALSE
					Mientras x = FALSE
						x := TRUE
						Para i = 1, LIM-1, 1
							Si ORD(LIM).NAC < ORD(LIM+1).NAC
								AUX := ORD(LIM)
								ORD(LIM) := ORD(LIM+1)
								ORD(LIM+1) := AUX
								x := FALSE
							FinSi
						FinPara
					FinMientras
					Para i = 1, LIM, 1
						Imprimir ORD(i).NAC, ORD(i).NRO, ORD(i).PES
					FinPara
					CERRAR (ANIMALES)
				Fin
			FinProcedimiento LISTADO
			Procedimiento INFORMES
			Var
				COR : array[1..12] of integer
				CORAx : integer
				NROMAX : integer
				TIPMAX : integer
				PESMAX : Real
				CANV : integer
			Inicio
				ABRIR (ANIMALES)
				Para i = 1, 12, 1
					COR(i) := 0
				FinPara
				ANIMALES.NRO := 0
				PESMAX := low_value
				CANV := 0
				LEER (ANIMALES) (ANIMALES.NRO) Próximo
				Mientras NOEOF (ANIMALES)
					CORAx := ANIMALES.A-COR
					COR(CORAx) += 1
					Si PESMAX < ANIMALES.PES
						PESMAX ANIMALES.PES
						TIPMAX := ANIMALES.TIPO
						NROMAX := ANIMALES.NRO
					FinSi
					Si ANIMALES.A-ULT = 0
						Si ANIMALES.A-TIPO = 2
							CANV += 1
						FinSi
					FinSi
					LEER (ANIMALES) (ANIMALES.NRO) Próximo
				FinMientras
				CERRAR (ANIMALES)
				Para i = 1, 12, 1
					Imprimir COR(i), i
				FinPara
				Imprimir TIPMAX, NROMAX, CANV
			Fin
		FinProcedimiento INFORMES
	Fin
	Fin
```