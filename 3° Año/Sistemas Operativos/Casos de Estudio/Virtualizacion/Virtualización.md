>[!important] ¿Qué es la virtualización?
>La virtualización es una tecnología que permite crear múltiples entornos simulados o recursos dedicados desde un solo sistema de hardware físico.

Virtualización es un framework que divide los recursos de una computadora en múltiples entornos de ejecución, aplicando uno o más conceptos o tecnologías como el particionamiento de hardware y software, tiempo compartido, simulación parcial o total, emulación, calidad de servicio y otras.

La máquina física original equipada con el hipervisor se denomina **"host"** o **"anfitrión"**, y las VM que utilizan estos recursos se llaman **"guests"** o **"huéspedes"**.

>[!important] Hipervisor
>Un software llamado **hipervisor** se conecta directamente con el hardware y permite dividir un sistema en entornos separados, diferentes y seguros, los cuales se denominan **"máquinas virtuales"** (VM).

#### Propiedades de la virtualización
- **Particionamiento**: correr múltiples VMs en un mismo servidor físico.
- **Aislamiento**: las VMs están aisladas unas de otras.
- **Encapsulamiento**: el estado de cada VM puede ser copiado y trasladado.
- **Abstracción de Hardware**: las VMs pueden ser migradas a otros servidores

#### Ventajas de la virtualización
- Disminuye el número de servidores físicos.
	- Reduce tamaño del Datacenter.
	- Reduce consumo eléctrico.
	- Reduce gastos de mantenimiento.
- Reduce el impacto de cambios en aplicaciones.
- Posibilita desplegar múltiples SO en la misma plataforma HW.
- Minimiza o elimina el tiempo fuera de servicio.
- Reduce costos de capital y operacionales.
- Brinda rapidez en el aprovisionamiento de aplicaciones y recursos.
- Brinda continuidad del negocio y recuperación ante desastres.
- Aumenta la escalabilidad de TI.
- Aumenta la flexibilidad de TI.
- Aumenta la agilidad de TI

#### Hypervisor
Es la **capa de software** que separa al SO del hardware, es llamada como **Virtual Machine Monitor** (VMM). Se crea una **plataforma virtual** en la cual las instancias de los SO pueden ser ejecutados, esto permite que la plataforma de hardware sea **compartida** por muchos SO y aplicaciones.

Hay dos tipos de Hypervisor:
- Hypervisor tipo 1 (bare metal).
![[hypervisorTipo1.PNG]]
- Hypervisor tipo 2 (hosted).
![[hypervisorTipo2.PNG]]

#### Almacenamiento
Las imagenes de disco son archivos que se ubican en el host o en un NAS y las VMs las ven como discos rigidos. Cuando una VM lee o escribe datos, el hipervisor redirige la peticion a la imagen de disco.

Hay diferentes formatos: VDI (Virtualbox) – VMDK (VMWare) (abierto) – VHD (Microsoft) - QCOW2 (Qemu)

Al momento de su creación se debe especificar la capacidad del disco. Hay dos tipos de tamaño de imagen.
- Imágenes de tamaño fijo: Se crea una imagen de igual tamaño a la capacidad del disco.
- Imágenes de tamaño dinámico: Inicialmente, no ocupará espacio por los bloques libres, pero, irá creciendo a medida que se ocupen, hasta llegar a la capacidad máxima. Puede ser menos eficiente.

#### Instantáneas (Snapshots)
Permiten **resguardar** el **estado** de la VM en un momento particular. Al crear una instantánea se **"congelan"** las imágenes de disco de la máquina virtual y se crean **imágenes diferenciales**.

La imagen de disco original continua operando, pero las operaciones de escritura van a la imagen diferencial. Cada vez que se crea una nueva instantánea se crea una nueva imagen diferencial y se adjunta a la máquina virtual creando una **cadena** o **árbol de instantáneas**.

Si **restauramos** una instantánea (es decir, volver al estado de la VM en ese paso), ocurre lo siguiente:
- Se restaura la configuración de la VM al estado en el que se encontraba esa instantánea.
- Si la instantánea se tomó con la máquina corriendo, se restaura el **estado** de la máquina.
- Por cada disco adjuntado a la VM, las imágenes diferenciales son **eliminadas**, y la imagen "padre" se marca como **activa**.

#### Clonación
Permite crear una nueva VM a partir de otra original.
Hay dos tipos de clonación: Completa o Enlazada.

**Clonación completa**: Se crea una copia (configuración y discos) de la máquina original.

**Clonación enlazada**: Se crea una nueva máquina, pero el disco se **vincula** a una instantánea del disco de la máquina original. Los archivos de la máquina original deberán mantenerse.