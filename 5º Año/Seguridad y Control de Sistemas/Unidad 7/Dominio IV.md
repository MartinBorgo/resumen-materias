El Dominio 4 de ISACA se enfoca en la **Integridad, Confidencialidad y Disponibilidad de los Sistemas de Información**. El objetivo principal es analizar y evaluar los controles lógicos, físicos, ambientales, de validación de datos, de procesamiento y balanceo, y el proceso de planificación y prueba de la continuidad del negocio.
### Controles Principales
Este dominio evalúa y protege los sistemas de información a través de los siguientes subdominios:
- **Controles de acceso lógico**: Se centra en la identificación, evaluación y prueba de los controles de acceso lógico para garantizar un suministro eficaz y eficiente de los sistemas, y para proteger la integridad, confidencialidad y disponibilidad de los datos.
- **Controles de acceso físico**: De manera similar a los controles lógicos, este subdominio se enfoca en la protección del acceso físico a las instalaciones y equipos para salvaguardar la integridad, confidencialidad y disponibilidad de la información.
- **Controles ambientales**: Identifica, evalúa y prueba los controles del entorno, como la climatización o la prevención de incendios, para asegurar la integridad, confidencialidad y disponibilidad de los datos.
- **Validación de datos, controles de procesamiento y balanceo**: Se encarga de evaluar los controles que aseguran que los datos sean precisos, completos y que el procesamiento sea correcto, previniendo errores y fraudes.
- **Planificación y prueba de la continuidad del negocio**: Se refiere a la identificación, evaluación y prueba de los controles de un plan de contingencia para garantizar la continuidad de las operaciones en caso de desastres o emergencias, asegurando la recuperación de los sistemas y datos.
### Controles de Acceso Lógico
El control de acceso lógico es una salvaguarda para proteger los sistemas y datos informáticos contra la divulgación, manipulación o destrucción no autorizada. El auditor de sistemas de información (SI) debe evaluar las políticas, estructuras y procedimientos de acceso.
#### Tareas del Auditor de SI
El auditor de SI debe realizar las siguientes tareas para evaluar los controles de acceso lógico:
- Obtener una comprensión del entorno de procesamiento de información revisando la documentación y observando los procedimientos.
- Documentar y evaluar las vías de acceso al sistema para verificar su eficacia.
- Probar los controles de las rutas de acceso para determinar su funcionamiento.
- Evaluar el ambiente de control de acceso y el ambiente de seguridad en general.
#### Requisitos de una Buena Política de Seguridad
Una política de seguridad escrita es fundamental para concientizar a toda la organización. Los componentes clave de esta política incluyen:
- **Apoyo de la gerencia**: La gerencia debe mostrar un compromiso claro con la seguridad a través de la aprobación de políticas y la capacitación.
- **Filosofía de acceso**: El acceso a la información debe basarse en el principio de "necesidad de saber, necesidad de hacer".
- **Autorización de acceso**: Un gerente debe otorgar una autorización escrita a los usuarios para acceder a la información.
- **Revisión de la autorización**: Los controles de acceso deben evaluarse regularmente, al menos una vez al año, para asegurar su eficacia.
- **Percepción de la seguridad**: Se debe recordar a todos los empleados la importancia de la seguridad a través de políticas, capacitación, declaraciones de no divulgación y auditorías periódicas.
- **Rol del Administrador de Seguridad**: Es responsable de implementar, monitorear y hacer cumplir las normas de seguridad.
- **Comité de Seguridad**: Debe ser conformado por representantes de la empresa para establecer directivas y procedimientos de seguridad .
- **Control de inventario**: Se debe mantener un catálogo de _hardware_ y _software_ para determinar los recursos disponibles y sus necesidades.
#### Rutas de Acceso Lógico
El acceso lógico puede realizarse por diversas vías, cada una con un nivel de seguridad adecuado. Algunas de estas rutas son:
- **Consola del operador**: Terminales privilegiadas que controlan las operaciones del computador y deben estar en un área controlada.
- **Terminales en línea**: El modo de acceso más común, que generalmente requiere un código de identificación y una contraseña.
- **Procesamiento diferido**: Acceso indirecto a través del procesamiento de transacciones acumuladas en lotes.
- **Puertas de telediscado**: Acceso remoto a través de una línea telefónica, utilizando mecanismos de devolución de llamada (_dial-back_) para validar la autoridad del usuario.
- **Redes de telecomunicaciones**: Enlazan terminales a un computador por medio de líneas de comunicación.
#### Exposiciones a Riesgos de Acceso Lógico
Los controles de acceso lógico inadecuados aumentan el riesgo de pérdidas para la organización. Los causantes de las violaciones de acceso pueden ser hackers, empleados (autorizados y no autorizados), personal de SI, ex-empleados, y terceros interesados. Las exposiciones a riesgos técnicos incluyen:
- **Manipulación de datos**: Alteración de datos antes de que se ingresen al sistema.
- **Caballos de Troya**: Código malicioso oculto dentro de un programa legítimo.
- **Técnica del salame o tajada**: Retiro de pequeñas sumas de dinero de transacciones para transferirlas a una cuenta no autorizada.
- **Virus informáticos**: Programas que se auto-duplican y dañan o alteran archivos.
- **Gusanos**: Programas destructivos que utilizan grandes cantidades de recursos del computador.
- **Bombas lógicas**: Similares a los virus, pero no se auto-duplican y se activan por un evento específico.
- **Puertas traseras**: Salidas ocultas en un programa que permiten la inserción de lógica no autorizada.
- **Fugas de datos**: Extracción no autorizada de información del computador.
- **Apagado del computador**: Iniciado por conexiones directas o indirectas, a menudo requiere un código de alta jerarquía.
#### Controles Específicos de Acceso Lógico
Para proteger los archivos computarizados del acceso no autorizado, se deben implementar controles que minimicen el riesgo de uso, robo o alteración. Estos controles son aplicables a todos los usuarios, incluyendo operadores, programadores, y gerentes.
- **Archivos y funciones a proteger**: Los controles de acceso lógico deben aplicarse a diversos elementos, tales como datos, _software_ de aplicaciones (de prueba y de producción), utilidades, bibliotecas, y archivos de registro (_logs_).
- **Códigos de ID y contraseñas**: Se utiliza una identificación de usuario en dos etapas para limitar el acceso. El sistema verifica primero un ID válido y luego obliga al usuario a substanciar su validez con una contraseña. Las contraseñas deben ser difíciles de adivinar, ser cambiadas periódicamente y no ser reusadas. Además, deben ser encriptadas internamente para reducir el riesgo de que alguien acceda a ellas.
- **Restricción de uso de terminales**: Los controles de acceso también pueden limitar el uso de terminales a transacciones específicas según su dirección física o lógica. También se puede evitar que una terminal se encienda hasta que se destrabe un cerrojo con una llave o tarjeta.
- **Procedimientos de devolución de llamada (_dial-back_)**: Cuando se utiliza el acceso remoto, el sistema interrumpe la conexión inicial y llama de vuelta al usuario para validar su autoridad. Esta devolución de llamada puede ser manual o automática.
- **Restricciones a funciones que "saltan" la seguridad**: El acceso a funciones que permiten "saltar" los controles de seguridad debe ser restringido, generalmente solo a programadores de _software_ de sistemas.
- **Clasificación de datos**: La gerencia puede asignar niveles de sensibilidad a los archivos (alta, media, baja) para determinar quién puede acceder a ellos. Esto reduce el riesgo y el costo de proteger los recursos de manera excesiva.
#### Técnicas de Evaluación y Auditoría
El auditor de SI debe emplear diversas técnicas para evaluar la eficacia de los controles de acceso lógico.
- **Revisión de políticas escritas**: El auditor debe revisar las políticas de acceso, los procedimientos de capacitación en seguridad y las autorizaciones documentadas. También debe asegurarse de que estas políticas sean comunicadas y aplicadas consistentemente.
- **Pruebas de seguridad**: El auditor debe probar directamente los controles. Esto incluye:
    - **Verificación de contraseñas**: Intentar crear contraseñas con formato inválido para ver si el sistema las rechaza.
    - **Prueba de desconexión automática**: Dejar una sesión activa y verificar que el sistema se desconecta después de un período de inactividad.
    - **Prueba de desactivación por intentos fallidos**: Intentar acceder a un sistema con contraseñas erróneas para confirmar que la cuenta se desactiva.
    - **Revisión de registros**: Examinar los _logs_ de seguridad para buscar evidencia de violaciones de acceso y verificar si se les da un seguimiento adecuado.
    - **Prueba de _dial-back_**: Llamar al sistema desde números autorizados y no autorizados para comprobar que solo se permite la conexión desde los números correctos.
### Controles de Acceso Físico
Los controles de acceso físico buscan proteger las instalaciones, los equipos y los medios de almacenamiento de la organización de los riesgos derivados de factores humanos o naturales. El objetivo es identificar, evaluar y probar estos controles para garantizar un suministro eficaz y eficiente de los sistemas, y para proteger la integridad, confidencialidad y disponibilidad de los datos.
#### Tareas del Auditor de SI
Para evaluar la efectividad de los controles de acceso físico y ambiental, el auditor de sistemas de información (SI) debe llevar a cabo las siguientes tareas:
- **Documentar y evaluar:** Debe documentar y evaluar la seguridad física y los controles ambientales en las áreas donde se encuentran los equipos y los medios de almacenamiento.
- **Probar los controles:** Debe aplicar técnicas de auditoría apropiadas para probar el funcionamiento y la eficacia de los controles de seguridad física.
- **Evaluar el ambiente de seguridad:** Debe evaluar el ambiente de seguridad física para asegurarse de que se cumplen los objetivos de control, analizando los resultados de las pruebas y la evidencia de auditoría.
#### Áreas y Activos a Proteger
Los controles físicos deben proteger tanto las áreas de trabajo como los activos de hardware y medios de almacenamiento. Las zonas a resguardar incluyen:
- Sala de computadoras y áreas de programación.
- Consolas y terminales del operador.
- Biblioteca de cintas, cintas, discos y otros medios magnéticos.
- Salas de almacenamiento y de suministros.
- Centro de almacenamiento de archivos de respaldo (_back-up_) fuera de la sede.
- Sala de control de entrada y salida.
- Cuartos de conexiones de comunicaciones.
- Equipos de telecomunicaciones y microcomputadoras.
- Fuente de energía eléctrica.
- Minicomputadoras, impresoras y redes de área local.
- Lugares de eliminación de residuos.
#### Medidas de Control Físico
Se detalla diversas medidas para garantizar el control físico:
- **Puertas con cerrojo:** Se deben utilizar cerraduras con llave, de combinación o electrónicas para restringir el acceso. Las combinaciones deben cambiarse periódicamente y cuando alguien con acceso abandona la organización.
- **Personal de seguridad y visitantes:** Se debe controlar el acceso de los visitantes mediante un registro de entrada y salida, verificación de identidad y el acompañamiento permanente por parte de un empleado responsable.
- **Identificación del personal:** Todo el personal y los visitantes deben portar insignias de identificación visibles.
- **Sistemas de alarma y vigilancia:** Se deben utilizar sistemas de alarma, detectores de movimiento y cámaras de video en puntos estratégicos, conectando las alertas a una estación de monitoreo.
- **Punto único de ingreso:** Para reducir el riesgo de acceso no autorizado, el ingreso debe limitarse a uno o dos puntos de entrada controlados.
- **Mecanismos de control electrónico:** El acceso puede estar controlado mediante tarjetas magnéticas o dispositivos biométricos que registren la entrada y salida del personal, permitiendo asignar permisos específicos y desactivar el acceso fácilmente.
- **Segregación de funciones:** El acceso físico del personal de sistemas de información debe limitarse estrictamente a una "necesidad de saber".
#### Control de Inventario
La organización debe mantener inventarios actualizados de todos los equipos y medios de almacenamiento, verificando periódicamente su ubicación y estado. El auditor debe confirmar que las bajas y movimientos estén documentados y aprobados por la gerencia.
#### Riesgos y Amenazas
Las exposiciones físicas a riesgos pueden surgir tanto por violaciones accidentales como intencionales de los puntos de acceso16. Entre los riesgos más frecuentes se incluyen el ingreso no autorizado, hurto de equipos o documentos, vandalismo, alteración de información sensible, abuso de confianza y extorsión.
Entre los posibles causantes de violaciones a la seguridad física se incluyen empleados descontentos o bajo sanción, ex-empleados, personal externo de mantenimiento, contratistas, proveedores, o incluso personas que violan la seguridad accidentalmente.
Los controles de acceso físico protegen a la organización de una variedad de amenazas, incluyendo:
- **Amenazas humanas:** Acceso no autorizado por parte de _hackers_, empleados, ex-empleados, competidores o personal temporal. También se incluyen actos de sabotaje, robo de equipos o información, y vandalismo.
- **Amenazas naturales y ambientales:** Incendios, inundaciones, terremotos y otros desastres naturales. Los controles ambientales (como la calidad del aire y la electricidad) también son parte de esta sección.
#### Consideraciones Adicionales
- **Planes de contingencia:** Es crucial que la organización cuente con un plan de recuperación ante desastres que incluya la reubicación en un centro de recuperación en caso de que las instalaciones principales resulten dañadas.
- **Prohibiciones:** Se debe prohibir el consumo de alimentos, bebidas y tabaco en las áreas de procesamiento de información para reducir el riesgo de daños a los equipos y de incendios.
- **Protección de datos:** Los diskettes y cintas de respaldo deben protegerse del daño por temperaturas extremas, campos magnéticos y humedad.

De acuerdo. Aquí tienes la versión actualizada del resumen para el apartado **4.3 Controles Ambientales**, con las mejoras y adiciones que se sugirieron integradas para que quede perfectamente alineado con el texto base.

### Controles Ambientales
Los controles ambientales tienen como objetivo reducir el riesgo de interrupción de las actividades del negocio debido a condiciones adversas en el entorno físico, incluyendo la calidad del aire, el suministro eléctrico y las condiciones atmosféricas. El auditor de SI debe documentar, evaluar y probar estos controles para determinar su eficacia y verificar que se cumplan los objetivos de protección.
#### Protección contra Incendios
Un conjunto de medidas coordinadas es fundamental para la detección, contención y extinción de incendios.
- **Detección:**
    - **Detectores de humo:** Deben instalarse en todo el centro, tanto por encima de los cielos rasos como por debajo de los pisos sobre-elevados. Deben activar una señal audible y estar conectados a una central de monitoreo, preferiblemente el departamento de bomberos.
    - **Alarmas manuales:** Deben existir alarmas de accionamiento manual en ubicaciones estratégicas para ser utilizadas por el personal.
- **Supresión:**
    - **Sistemas automáticos:** Se diseñan para activarse al detectar una fuente de calor intensa. El sistema debe ser revisado y probado anualmente. Las opciones más comunes son:
        - **Agua (rociadores):** Son eficaces pero pueden dañar los equipos electrónicos.
        - **Gas Halón 1301:** Libera un gas a alta presión que elimina el oxígeno del aire, extinguiendo el fuego sin dañar los equipos8. Requiere una alarma previa para permitir la evacuación del personal.
    - **Extinguidores portátiles:** Deben estar ubicados en puntos estratégicos, ser revisados anualmente y ser aptos para incendios de clase A, B o C.
- **Prevención y Contención:**
    - **Materiales ignífugos:** Las paredes, pisos y cielos rasos que rodean la sala de computadoras deben tener una resistencia al fuego de al menos dos horas. El mobiliario y equipamiento de oficina también deben ser resistentes al fuego.
    - **Prohibiciones:** Debe prohibirse estrictamente comer, beber y fumar en la instalación de procesamiento para evitar daños a equipos sensibles y reducir el riesgo de incendio.
    - **Inspección de bomberos:** El departamento de bomberos local debe inspeccionar las instalaciones anualmente para asegurar el cumplimiento de los códigos de edificación.
#### Protección del Suministro Eléctrico y Equipos
La continuidad y calidad de la energía eléctrica son vitales para la operación de un centro de datos.
- **Provisión Ininterrumpible de Energía (UPS):** Es un sistema con un generador a batería o combustible que garantiza una corriente uniforme y, en caso de un corte, sigue suministrando energía por un tiempo determinado, permitiendo una desconexión ordenada del equipo.
- **Protectores de picos de tensión:** Utilizan reguladores de voltaje para proteger los equipos de daños causados por sobretensiones. Generalmente están incorporados en los sistemas UPS.
- **Líneas de suministro redundantes:** La instalación debe estar alimentada por dos líneas eléctricas distintas para que la interrupción de una no afecte la provisión de energía.
- **Cableado protegido:** Todo el cableado eléctrico debe estar empotrado en paneles y cañerías a prueba de fuego para reducir el riesgo de que un incendio se inicie o se extienda.
- **Llave de desconexión de emergencia:** Deben existir interruptores claramente identificados para cortar la energía de inmediato en caso de una emergencia. Se recomienda tener uno dentro de la sala de computadoras y otro fuera, en un lugar cercano.
#### Salvaguardas de la Instalación Física y Condiciones Ambientales
- **Ubicación estratégica:** Para reducir el riesgo de inundaciones, la sala de computadoras no debe estar en sótanos o subsuelos. En edificios de varios pisos, se recomienda ubicarla entre los pisos 3 y 6 para minimizar los riesgos de fuego, humo y daños por agua.
- **Detectores de agua:** Deben colocarse debajo de los pisos sobre-elevados y cerca de los drenajes para proteger tanto al equipo como al personal de cortocircuitos. Su ubicación debe estar claramente marcada.
- **Control de temperatura y humedad:** Los sistemas de aire acondicionado y ventilación son cruciales para mantener la temperatura y humedad dentro de los rangos especificados por los fabricantes de equipos, evitando así la acumulación de estática o condensación.
- **Planes de evacuación:** La organización debe contar con planes de evacuación de emergencia documentados y probados que prioricen la seguridad del personal sin dejar las instalaciones desprotegidas.

### Planificación y Prueba de la Continuidad del Negocio
La planificación de la continuidad del negocio (BCP, por sus siglas en inglés) se refiere a la capacidad de una organización para sobrevivir a un desastre, asegurando que las operaciones críticas puedan reanudarse dentro de un marco de tiempo predefinido1. El auditor de SI debe evaluar la existencia, integridad y efectividad del plan, verificando que contemple la recuperación de sistemas críticos, la protección de datos y la continuidad de los servicios esenciales2222.

#### Requisitos Previos y Análisis de Impacto

Antes de elaborar el plan, la alta gerencia debe definir la política de continuidad y asignar responsabilidades formales a un comité o coordinador de contingencias3. Asimismo, se debe realizar un

**Análisis de Impacto al Negocio (BIA)** que identifique los procesos críticos, los recursos de los que dependen y el tiempo máximo de interrupción tolerable (MTD) para cada uno444444444.

#### Componentes Clave del Plan de Continuidad

Un plan de continuidad efectivo se compone de varios elementos esenciales que involucran a toda la organización.

- **Organización y Responsabilidades:**
    
    - El plan debe definir equipos de trabajo con responsabilidades claras para gestionar la crisis5555. Esto incluye un
        
        **Equipo de evaluación de daños** 6, un
        
        **Equipo de administración de la emergencia** que coordina la recuperación 7, y equipos específicos para software, aplicaciones, redes, seguridad y logística8888888888888888.
        
- **Análisis de Riesgos y Clasificación de Sistemas:**
    
    - Se deben identificar los sistemas y funciones del negocio y clasificarlos según su criticidad y tolerancia a la interrupción9. La clasificación típica es:
        
        - **Críticos:** No pueden realizarse manualmente y su interrupción tiene un costo muy alto10.
            
        - **Vitales:** Pueden realizarse manualmente por un corto período (generalmente hasta 5 días)11.
            
        - **Sensibles:** Pueden realizarse manualmente por un período más largo, aunque con dificultad y costos adicionales12.
            
        - **No críticos:** Pueden interrumpirse por un largo período con poco o ningún costo para la empresa13.
            
- **Procedimientos Documentados:**
    
    - El plan debe contener procedimientos detallados para cada fase del desastre, incluyendo la acción de emergencia 14, la notificación al personal clave 15, la declaración oficial del desastre 16, y la recuperación de sistemas, redes y funciones de usuario171717171717171717.
        
- **Cobertura de Seguros:**
    
    - La organización debe contar con una póliza de seguros adecuada que cubra los distintos aspectos de un desastre18. La cobertura debe incluir daños al equipamiento 19, reconstrucción de medios de almacenamiento 20, gastos extras por continuar operando 21, e interrupción del negocio22.
        
#### Estrategias de Recuperación y Sitios Alternativos

La capacidad de recuperación depende de la disponibilidad de instalaciones y recursos alternativos.

- **Tipos de Sitios de Recuperación:**
    
    - **"Hot-Site":** Un centro de procesamiento totalmente configurado y listo para operar en cuestión de horas23. Es la opción más costosa, pero justifica su precio para aplicaciones críticas24.
        
    - **"Warm-Site":** Un centro parcialmente configurado, generalmente con periféricos pero sin el computador principal25. La activación puede tomar días o semanas26.
        
    - **"Cold-Site":** Una instalación con la infraestructura básica (electricidad, aire acondicionado) pero sin ningún equipo de computación27. Su activación puede demorar semanas28.
        
    - **Acuerdos Recíprocos:** Contratos con otras organizaciones que tienen equipos similares29. Son de bajo costo pero a menudo no son exigibles legalmente y su fiabilidad es baja30303030.
        
- **Recuperación de Telecomunicaciones:**
    
    - El plan debe incluir la continuidad de las comunicaciones de voz y datos31. Las estrategias incluyen la
        
        **redundancia** (capacidad extra) 32,
        
        **rutas alternativas** (usar otros medios como microondas o redes de otros operadores) 33y
        
        **rutas diversificadas** (usar cableado físico separado)34.
        
- **Backups en Sede Alternativa:**
    
    - Es un prerrequisito crucial para cualquier recuperación35. Se deben realizar copias de seguridad periódicas de todos los archivos de datos, software de sistema, aplicaciones y documentación crítica y almacenarlas en una ubicación externa segura363636363636363636.
        
#### Prueba y Mantenimiento del Plan

Un plan de continuidad es inútil si no se prueba y actualiza regularmente.

- **Tipos de Pruebas:**
    
    - **Prueba sobre papel (Desktop Test):** Una recorrida teórica del plan donde los involucrados discuten los pasos a seguir en un escenario de desastre37.
        
    - **Prueba de nivel de preparación:** Una simulación localizada donde se ejecutan partes específicas del plan para probar su efectividad38.
        
    - **Prueba operativa completa:** Una simulación a gran escala donde se detienen las operaciones y se trasladan efectivamente a la sede de recuperación39393939.
        
- **Mantenimiento del Plan:**
    
    - El plan debe ser un documento vivo, revisado y actualizado periódicamente para reflejar los cambios en la organización404040404040404040. Un
        
        **Coordinador de Recuperación de Desastres** es generalmente el responsable de mantener el plan41.
        
### Entrenamiento y Concientización

El personal clave debe recibir entrenamiento regular y participar en las pruebas del plan para asegurar que conozcan sus responsabilidades y los procedimientos a seguir durante una emergencia42424242.