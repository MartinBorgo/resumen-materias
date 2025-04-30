# Resumen Materias FCAD UNER
Este repositorio contiene resúmenes de las materias de la carrera Licenciatura en Sistemas de la Facultad de Ciencias de la Administración de la Universidad Nacional de Entre Ríos (FCAD UNER).
El resumen fue realizado teniendo en cuenta el plan de estudios del 2012. Los contenidos son probablemente aplicables a los nuevos planes de estudios, al menos las materias más relevantes.
## 📚 Contenido
El repositorio está organizado por años de la carrera:
- 1° Año
	- Organización de Computadoras
	- Teoría de Sistemas
- 2° Año
	- Arquitectura de Computadoras
	- Estructura de Datos
	- Organización de Empresas
	- Programación Orientada a Objetos
- 3° Año
	- Autómatas y Lenguajes Formales
	- Lenguajes de Programación
	- Metodología de la Investigación
	- Metodología de Sistemas I
	- Probabilidad y Estadística
	- Sistemas Operativos
- 4° Año
	- Bases de Datos
	- Comunicaciones y Redes
	- Lógica para las Ciencias Informáticas
	- Metodología de Sistemas II
	- Planeamiento y Control de Gestión
- 5° Año
	- Algoritmos y Complejidad
	- Desarrollo de Proyectos
	- Inteligencia Artificial
	- Investigación Operativa
	- Seguridad y Control de Sistemas
	- Ética y Deontología Profesional
	- Trabajo Final
## 📖 Cómo leer los archivos
Para una mejor experiencia en la lectura de los archivos Markdown (`.md`), se recomienda utilizar [Obsidian](https://obsidian.md/download). Obsidian es una aplicación de notas que permite:
- Visualizar los archivos Markdown con formato.
- Navegar entre archivos mediante enlaces.
- Ver imágenes y recursos multimedia embebidos.
- Utilizar gráficos y diagramas.
- Organizar la información de manera jerárquica.
### Pasos para clonar el repositorio:
1. Instala Git desde [git-scm.com](https://git-scm.com/downloads)
2. Abre una terminal o Git Bash
3. Navega hasta la carpeta donde quieras clonar el repositorio usando el comando `cd`
4. Ejecuta el siguiente comando y espere a que sé que complete la descarga:

```bash
git clone https://github.com/MartinBorgo/resumen-materias.git
```
### Pasos para usar este repositorio con Obsidian:
5. Descarga e instala [Obsidian](https://obsidian.md/download).
6. Abre Obsidian y selecciona “*Open folder as vault*”.
7. Navega hasta la carpeta donde clonaste el repositorio y selecciónala.
8. ¡Listo! Ya puedes navegar por los resúmenes con todas las funcionalidades de Obsidian.
## ⚙️ Configuración de Obsidian
Este apartado es opcional pero recomendada, ya que en caso de que se agreguen nuevos archivos al resumen de forma local, puede que algunos enlaces a recursos como otras notas o imágenes no se muestren o redirijan de forma correspondiente.
- **Files and links > Automatically update internal links** debe estar activado. Esta opción actualiza automáticamente las referencias internas que existen en un documento hacia otros, es útil para aquellos casos donde se cambia el nombre de los archivos.
- **Files and links > Default location for new attachments** se debe seleccionar “*in subfolder under current folder*”. Esto hará que los nuevos archivos adjuntados a un documento se organicen en una carpeta creada en el mismo nivel que el archivo donde se adjuntó ese documento. Al seleccionar esta opción se habilitará una nueva sección, **Files and links > Subfolder name**, en la cual se especifica el nombre de la carpeta donde se guardarán los archivos adjuntos, dicho valor debe ser fijado en “*Anexos*”, aunque una vez tengas el resumen en local se lo puede renombrar a preferencia.
- En la sección de **Community plugins** se puede instalar la extensión ***LanguageTool Integration*** que ayuda a corregir y chequear los errores ortográficos en las palabras. Una vez instalada la extensión se la debe activar y configurar. Las configuraciones son las siguientes:
	- **LanguageTool Integration > Autocheck Text** debe estar activado.
	- **LanguageTool Integration > Autocheck delay (ms)** es recomendable fijarlo a 4000, ya que se suele romper mucho el delineado sobre las palabras a corregir.
	- **LanguageTool Integration > Glass Background** debe estar activado, aunque es solo una opción estética.
	- **LanguageTool Integration > Static Language** se debe seleccionar “*Spanish*”. El reconocedor automático de idiomas no anda del todo bien.
	- **LanguageTool Integration > Picky Mode** esta opción se puede activar en caso de que se desee corregir terminologías o la sintaxis de ciertas oraciones. Es útil en caso de que se quiera evitar repetir palabras y estructurar correctamente los párrafos de una nota.
### Customización de los Estilos por Defecto de Obsidian
En caso de que se quiera tener una apariencia más ordenada de los párrafos, enumeraciones, ítems y tablas se puede ir a la siguiente sección **Appearence > CSS snippets** abrir la carpeta donde se sitúan los estilos customizados, crear un nuevo archivo ***CSS*** en dicha carpeta que contenga el siguiente código:
```css
/* ======== Justificado del Texto ======== */
.markdown-preview-view p,
.markdown-preview-view li,
.markdown-source-view.mod-cm6 .cm-line {
    text-align: justify;
    text-justify: inter-word;
}

.markdown-preview-view ul,
.markdown-preview-view ol {
    text-align: justify;
}

/* ======== Espaciado entre párrafos ======== */
.markdown-preview-view br {
  content: '';
  display: block;
  margin-top: 10px;
}

.markdown-source-view :is(.cm-line:not(.HyperMD-list-line):not(.HyperMD-codeblock):not(.HyperMD-callout)) {
  padding-bottom: 0.5em;
}
/* 
Espaciado entre listas (Descomentar si es que se quiere un espaciado entre los items de las listas)
body {
    --list-spacing: 0.150em;
}
*/

/* ======== Centrar imágenes ======== */
img {
  display: block !important;
  margin-left: auto !important;
  margin-right: auto !important;
  border-radius: 0.5rem;
  border: 0.125rem solid rgb(170, 183, 184);
}

.markdown-source-view.mod-cm6 .cm-content > * {
  margin: auto auto !important;
}

/* ======== Personalización de las Tablas ======== */

/* Centrar tablas en modo lectura y modo edición */
.markdown-preview-view table,
.cm-s-obsidian table {
  margin: 0 auto;
  min-width: 100%;
}
/* Centrar texto de los encabezados de cada columna */
.markdown-preview-view table thead tr th,
.cm-s-obsidian table thead tr th  {
	text-align: center;
}
/* Colores alternados para cada fila de la tabla */
.markdown-preview-view tr:nth-child(even),
.cm-s-obsidian tr:nth-child(even) {
  background-color: rgba(51, 51, 51, 0.2);
}
.markdown-preview-view tr:nth-child(even):hover,
.cm-s-obsidian tr:nth-child(even):hover {
  background-color: rgba(51, 51, 51, 0.2);
}
/* Color del encabezado de la tabla */
.markdown-preview-view table > thead,
.cm-s-obsidian table > thead {
  background-color: rgba(51, 51, 51, 0.2);
}
/* Redondear los bordes de la tabla */
.markdown-preview-view table,
.cm-s-obsidian table {
  border-collapse: separate;
  border: solid #333 1.5px;
  border-radius: 0.5rem;
  border-spacing: 0px;
}
/* Redondea los bordes de las últimas celdas */
.markdown-preview-view table > tbody > tr:last-child > td:first-child,
.markdown-preview-view table > tbody > tr:last-child > th:first-child,
.cm-s-obsidian table > tbody > tr:last-child > td:first-child,
.cm-s-obsidian table > tbody > tr:last-child > th:first-child {
  border-bottom-left-radius: 0.5rem;
}
.markdown-preview-view table > tbody > tr:last-child > td:last-child,
.markdown-preview-view table > tbody > tr:last-child > th:last-child,
.cm-s-obsidian table > tbody > tr:last-child > td:last-child,
.cm-s-obsidian table > tbody > tr:last-child > th:last-child {
  border-bottom-right-radius: 0.5rem;
}
/* Redondea los bordes de las primeras celdas */
.markdown-preview-view table > thead > tr:first-child > td:first-child,
.markdown-preview-view table > thead > tr:first-child > th:first-child,
.cm-s-obsidian table > thead > tr:first-child > td:first-child,
.cm-s-obsidian table > thead > tr:first-child > th:first-child {
  border-top-left-radius: 0.5rem;
}
.markdown-preview-view table > thead > tr:first-child > td:last-child,
.markdown-preview-view table > thead > tr:first-child > th:last-child,
.cm-s-obsidian table > thead > tr:first-child > td:last-child,
.cm-s-obsidian table > thead > tr:first-child > th:last-child {
  border-top-right-radius: 0.5rem;
}
```

Luego de guardar este archivo se lo debe activar para que se apliquen sus estilos al resto de la interfaz. Para aplicar los cambios se puede cerrar y volver a abrir Obsidian o simplemente refrescar los estilos customizados.
## ⚠️ Notas Importantes
- En el resumen no se contemplan las matemáticas duras como álgebra o análisis matemático, entre otras. Solo se enfoca en las materias con un contenido teórico más pesado.
- Los resúmenes de 1° y 2° año están menos desarrollados y pueden contener información incompleta o poco detallada.
- A partir de 3° año, los resúmenes son más completos y detallados, con excepción de algunas materias específicas como Estadística, que es un caso particular.
- La rama `dev` siempre está mucho más actualizada que la rama principal o `master`. En caso de que el resumen ya esté terminado, ambas ramas estarán iguales.