El primero parte de 6 unidades, no se menciona sobre los elementos del cuerpo de la unidad.
El cuerpo de una unidad está conformado por:
- Declaraciones
- Bloques ejecutables
Otro que tengo anotado es que: Los parámetros son variables locales, aunque estén en el header

Una cosa a tener en cuenta es que en la imagen 1. Unidades (unidad 6)
la imagen de las semánticas: in, out e in-out mode. Pone "función llamadora" y "función llamada". En realidad tendría que ser "unidad llamadora" y "unidad llamada", haciendo todo más genérico, sin mencionar especificaciones de alguna unidad.

Estructura de control a nivel unidad
En simétricas se puede mencionar los mecanismos que tiene:
- Invocación -> master unit
- Suspensión -> para co-rutina hasta *x* punto
- Reanudación -> activa devuelta la unidad suspendida hasta el punto que se quedó
- Finalización

Sobre consideraciones de LP en Paralelas (lo que tengo anotado)
- Definición de variables en el resumen está completo.
- Composición paralela -> lo que nos brinda el LP.
- Estructura de programa -> Transformación Reactiva: No da resultado, pero da una respuesta de la unidad que se ejecuta.
- Comunicación -> Memoria compartida (necesita sincronización) o mensaje (necesita emisor y receptor).
- Sincronización.

Excepciones
Pregunta fundamental ¿cómo la trato, como afecta? Esta pregunta nos da la información sobre como definimos el alcance de la excepción (la unidad que la produjo, la que invoco, al bloque, etc.).
- La unidad que la produjo.
- La unidad que invocó a la que la produjo.
- Un bloque etiquetado fuera de la unidad que la produjo. 
- La unidad recibida como parámetro.
El alcance lo define el diseñador.