
**Lo que tengo de memoria**
Sobre memoria la asignación se hacen varias preguntas.
¿Hay espacio?, en caso de que no haya, mata algún proceso o manda a la VM. Si hay espacio se pregunta ¿Hay suficiente?, dependiendo si es segmentación o paginación se hace algo diferente. En segmentación donde hay variables, tiene que hacer hueco para que entre. Con paginación usa marcos, espacios iguales, entonces se pregunta ¿Hay marcos suficientes?

Sobre el código compartido, se pregunta si nadie lo usa, si es así cierra y actualiza en disco.

El DMA accede directo a memoria, además cada disco tiene su propio DMA.

Las particiones dinámicas no tienen fragmentación interna, pero produce fragmentación externa. En paginación hay fragmentación interna. En los dos casos se genera desperdicio.

La fragmentación interna no se puede solucionar
La fragmentación externa se soluciona con la compactación (solamente se puede unir con el adyacente, tengo entendido)

Sobre el sistema de los asociados
Básicamente es un gran hueco que se va diviendo hasta que tenga el menor desperdicio, las divisiones se las conoce como socios.
El SO se hace dos preguntas:
1. ¿Entro?
2. ¿Se puede seguir dividiendo?