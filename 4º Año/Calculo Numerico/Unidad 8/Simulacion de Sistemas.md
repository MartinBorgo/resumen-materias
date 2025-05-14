## 1. Tipos de Modelos Dinámicos

### Sistemas Continuos
- Caracterizados por cambios pequeños y continuos en los atributos de las entidades
- Generalmente definidos por ecuaciones diferenciales
- Pueden resolverse por:
  - Métodos analíticos (ej: sistema masa-resorte)
  - Procedimientos numéricos cuando el análisis directo no es posible
### Sistemas Discretos
- Los cambios ocurren en instantes discretos del tiempo
- Basados en la ocurrencia de sucesos específicos
- Ejemplo típico: sistemas de colas
## 2. Métodos de Simulación
### Simulación Continua
- Basada en sistemas de ecuaciones diferenciales
- Herramientas:
  - Simuladores analógicos (uso histórico)
  - Software moderno (ej: SIMULINK en MATLAB)
  - Métodos numéricos computarizados
### Simulación Discreta
- Seguimiento de cambios de estado basados en sucesos
- Elementos clave:
  - Identificación de causas de cambio
  - Temporización de sucesos
  - Relaciones lógicas entre eventos
## 3. Ejemplo Práctico: Sistema de Colas
### Características del Sistema
- Población fuente infinita
- Distribución de llegadas: Poisson (tasa λ)
- Servicio: Distribución exponencial (tasa μ)
- Cola infinita
- Estación de servicio única
### Elementos de la Simulación
1. **Estado del Sistema**
   - Definido por el número de unidades en el sistema
   - Incluye unidades en cola y en servicio
2. **Tipos de Sucesos**
   - Llegada: Nueva unidad al sistema
   - Salida: Unidad completando servicio
3. **Proceso de Simulación**
   - Generación de números aleatorios según distribuciones
   - Seguimiento temporal de eventos
   - Actualización de estado del sistema
   - Recolección de estadísticas
### Parámetros de Rendimiento Medibles
- Longitudes medias de colas
- Tiempos medios de espera
- Utilización de recursos
- Throughput del sistema
## 4. Ventajas de la Simulación Discreta
- Manejo de complejidad en sistemas aleatorios
- Superación de limitaciones analíticas
- Flexibilidad para diferentes distribuciones de probabilidad
- Capacidad de análisis de escenarios complejos
## 5. Consideraciones Metodológicas
- La simulación requiere un modelo conceptual claro
- Importancia de la correcta definición de estados
- Necesidad de identificar y caracterizar sucesos
- Relevancia de la generación de números aleatorios apropiados
