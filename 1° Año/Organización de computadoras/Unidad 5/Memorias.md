# Anki
TARGET DECK: Facultad:: Sistemas:: Primer año:: Organización de computadoras:: Unidad 5
# Archivos
![[Unidad 5.pdf]]
# Trabajo práctico
![[Trabajo Práctico 5 - Memorias.docx]]
#  Notas

## ¿Qué es una memoria?
Es una unidad que almacena información, como programas y datos

### ¿Cómo se clasifican las memorias? #flashcard
Según cuan cerca estén del procesador.
1. Registros
2. Memorias cache L1, L2, L3...
3. DRAM (Acceso aleatorio)
4. HDD, SSD, NVME.
5. Extraibles
6. Cintas magnéticas, almacenamiento en red.
<!--ID: 1700156773473-->



#### Características de la RAM y sus implementaciones #flashcard
1. Lectura-escritura
2. Volátiles
1. Dinámicas (DRAM)
	1. Bits en capacitores
	2. Simple
	3. Memoria principal lenta
2. Estáticas (SRAM)
	1. Interruptores
	2. Sin refrescos
	3. Compleja, rápida y cara
	4. Memoria caché
Capacidad DRAM > SRAM
Velocidad SRAM > DRAM
 
<!--ID: 1700156773478-->



## Discos magnéticos (Estructura) #flashcard
- Plato metálico con capa de material magnetizable
1. Plato (Superficie)
2. Pistas concéntricas (Surcos)
	1. Sectores
	2. Cabezal
	3. Cilindro (Pistas concéntricas de cada cara de un plato)
	4. Cluster (Agrupación de sectores mínima)
![[Estructura de un HDD.png]]
![[Estructura de un HDD(2).png]]
 
<!--ID: 1700156773483-->



### Cálculo de capacidad de almacenamiento de un HDD #flashcard
Capacidad = Sectores por pista x Tamaño sector (Bytes ) x Pistas (cilindros) por cara x Nro de caras
 
<!--ID: 1700156773492-->



## SSD #flashcard
- Memorias semiconductoras (flash)
 
<!--ID: 1700156773497-->



### SSD vs HDD #flashcard
Ventajas de los SSD:
1. Velocidad y rendimiento de E/S
2. Durabilidad
3. Menor consumo aunque su costo sea mayor
4. Menor ruido y calor
 
<!--ID: 1700156773504-->



## Discos ópticos #flashcard
- Bits leidos con láser incidente reflejado
- Tecnología de CD-ROM y DVD-ROM
 
<!--ID: 1700156773509-->



### Cálculo de capacidad de un disco óptico #flashcard
Ejemplo: CD-ROM. 270k sectores x 2kb datos = 527 MB
 
<!--ID: 1700156773513-->



## Cinta magnética #flashcard
1. Listón de plástico con óxido de hierro y otra capa magnética. 
2. Se graban bits con pulsos magnéticos.
3. Se suelen utilizar para guardar info. confidencial
 
<!--ID: 1700156773517-->



## Raids (Beneficios) #flashcard
Raid desde el 1 al 6
1. Integridad
2. Tolerancia a fallos
3. Rendimiento
4. Capacidad
5. Pueden soportar el uso de uno o más discos de reserva (hot spare).
 
<!--ID: 1700156773524-->



### Raid 0 #flashcard
Se distribuye partes de la información en ambos discos.
+ Velocidad y - Respaldo
 
<!--ID: 1700156773530-->



### Raid 1 #flashcard
Crea copias en ambos discos
+ Respaldo y - Velocidad
 
<!--ID: 1700156773536-->



### Raid 5 #flashcard
Mínimo 3 discos.
![[RAID 5.png]]
 
<!--ID: 1700156773546-->



### Raid 6 #flashcard
Como el raid 5 pero con 1 copia más en cada disco
![[RAID 6.png]]
 
<!--ID: 1700156773550-->



### Raid 10 #flashcard
Raid 1 + 0 para más seguridad, para bases de datos
 
<!--ID: 1700156773557-->



