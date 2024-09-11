## ¿Qué es una memoria?
Es una unidad que almacena información, como programas y datos.

### ¿Cómo se clasifican las memorias?
Según cuán cerca estén del procesador.  
1. **Registros**  
2. **Memorias caché L1, L2, L3**  
3. **DRAM (Acceso aleatorio)**  
4. **HDD, SSD, NVME**  
5. **Extraíbles**  
6. **Cintas magnéticas, almacenamiento en red**  

#### Características de la RAM y sus implementaciones
1. **Lectura-escritura**  
2. **Volátiles**  

**Tipos:**  
1. **Dinámicas (DRAM)**  
   1. Bits en capacitores  
   2. Simple  
   3. Memoria principal lenta  
2. **Estáticas (SRAM)**  
   1. Interruptores  
   2. Sin refrescos  
   3. Compleja, rápida y cara  
   4. Memoria caché  

**Capacidad DRAM > SRAM**  
**Velocidad SRAM > DRAM**

## Discos magnéticos (Estructura)
- Plato metálico con capa de material magnetizable  
1. **Plato (Superficie)**  
2. **Pistas concéntricas (Surcos)**  
   1. **Sectores**  
   2. **Cabezal**  
   3. **Cilindro** (Pistas concéntricas de cada cara de un plato)  
   4. **Cluster** (Agrupación mínima de sectores)  

### Cálculo de capacidad de almacenamiento de un HDD
**Capacidad** = Sectores por pista x Tamaño sector (Bytes) x Pistas por cara x Número de caras  

## SSD
- Memorias semiconductoras (flash)  

### SSD vs HDD
Ventajas de los SSD:  
1. **Velocidad y rendimiento**  
2. **Durabilidad**  
3. **Menor consumo** aunque su costo sea mayor  
4. **Menor ruido y calor**

## Discos ópticos
- Bits leídos con láser incidente reflejado  
- Tecnología de **CD-ROM y DVD-ROM**

### Cálculo de capacidad de un disco óptico
**Ejemplo**: CD-ROM. 270k sectores x 2KB datos = 527 MB  

## Cinta magnética
1. Listón de plástico con óxido de hierro y otra capa magnética  
2. Se graban bits con pulsos magnéticos  
3. Se suelen utilizar para guardar información confidencial  

## Raids (Beneficios)
RAID desde el 1 al 6  
1. **Integridad**  
2. **Tolerancia a fallos**  
3. **Rendimiento**  
4. **Capacidad**  
5. **Discos de reserva (hot spare)**  

### Raid 0
Distribuye partes de la información en ambos discos.  
- **Velocidad**  
- **Sin respaldo**  

### Raid 1
Crea copias en ambos discos.  
+ **Respaldo**  
- **Velocidad**  

### Raid 5
Mínimo 3 discos.  

### Raid 6
Como el RAID 5 pero con una copia extra de paridad.  

### Raid 10
RAID 1 + 0 para mayor seguridad, usado en bases de datos.
