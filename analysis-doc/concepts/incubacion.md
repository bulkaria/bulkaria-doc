Incubación
======

### Definition
Se lama incubación a la fase en que los alumnos definen las características del [producto](producto.md) que desean contratar.

#### Description
Esta es una de las fases más importantes de BE, en ella los alumnos definen las características del producto que desean contratar siguiendo el flujo que se explica más abajo. 

Antes de iniciar con el proceso se entiende que el actor [alumno](../actors/alumno.md) ha realizado el proceso de [check-in](../process/check-in.md) convirtiendose en un [miembro](../actors/miembro.md) del [grupo](../actors/grupo.md).

En este proceso, el alumno interactura con tres estructuras bien definidas, **clase de producto**, **característica del producto** y **configuración del producto**.

##### Clase de producto
La clase de producto define un objetivo del grupo que tiene un ciclo de vida propio. Un grupo puede definir varias clases de producto distintas, es decir varios objetivos distintos, por ejemplo *viaje de egresados* y *fiesta de egresados*, pero cada objetivo tendrá su propio [wall](wall.md), su propio [group blackboard](group-blackboard.md) y un ciclo de vida independiente del otro. Solo compartiran los miembros del grupo quienes podrán interactuar con una clase u otra.

##### Característica del producto
Define las características escenciales del producto, que no conforman parte de la configuración. Son caracteríticas que deben ser definidas previamente a la configuración, pues sin ellas es imposible configurarlo. 
Las características tienen una organización gerárquica de árbol y queda completamente definida cuando se ha seleccionado un rama completa del árbol. Ejemplo: para la clase *viaje de egresados* la caracterítica del producto (rama completa) pordría ser: 
```
Destino > Nacional > Bariloche
```
Cada nodo del árbol de carcterísticas cuenta con la posibilidad de recibir comentarios en los que los alumnos podrán fundamentar su elección y/o contestar otros comentarios de manera anidada (ver [estructura de comentarios](estructura-de-comentarios.md)).

##### Configuración del producto
Una vez seleccionadas las características del producto, el alumno debe proceder a definir la configuración del mismo. Para este fin cuenta con una estructura de árbol que va recorriendo por rama y definiendo, en cada nodo que lo requiera, su preferencia.
La preferencia será indicada mediante un valor numérico entre 0 y N dependiendo de:

* si el nodo es final (no tiene hijos o subnodos):
    * podrá recibir 0 ó 1 si es de opción binaria (si o no)
    * podrá recibir 0 ó N si es de opción unitaria (cuantas unidades se desean)
    * podrá recibir 1 ó N si es de opción unitaria obligatoria (al menos se debe optar por una unidad)
* si el nodo tiene hijos (subnodos):
    * podrá ser 0 ó 1 si es de opción única no obligatoria, es decir si se puede elegir un subnodo y solo uno o ninguno
    * podrá ser 0 ó N si es de opción múltiple no oblicatoria, es decir se pueden elegir uno o mas subnodos o ninguno
    * podrá ser 1 si se debe elegir uno y solo uno de sus subnodos
    * podrá ser 1 ó N si de de opción múltiple oblicatoria, es decir se deben elegir uno o mas subnodos.

Ejemplo:
```
+ Transporte [1]
|-- Bus (0,1)
|-- Tren (0,1)
|-- Aereo (0,1)
+ Excursiones [0..N]
|-- Lago Lacar (0,1)
|-- Cerro Catedral (0,1)
+ Disco [0..N]
|-- Cerebro (0..N)
|-- Pachanga (0..N)
```
Cada nodo del árbol de configuración cuenta con la posibilidad de recibir comentarios en los que los alumnos podrán fundamentar su elección y/o contestar otros comentarios de manera anidada (ver [estructura de comentarios](estructura-de-comentarios.md)).

##### Flujo del proceso de incubación
Para una mejor comprensión de los pasos de este proceso se definen basados en la [clase de producto](#clase de producto) *viaje de egresados*.

1. El alumno selecciona la clase de producto en la que desea definir sus preferencias. Si la clase no se encuentra en la lista podrá iniciarla y quedará disponible para otros alumnos. Ejemplo: Selecciona *viaje de egresados*
2. Se le presenta la raíz del árbol de caracteríticas y debe selecionar un nodo. Ejemplo: *Destino Nacional, Destino Internacional*
3. Luego de seleccionar un nodo raíz (ejemplo: Destino Nacional) debe seleccionar uno de los subnodos que se le presentan (de existir alguno). Ejemplo: *Bariloche, Córdoba, Mendoza, San Martín de los Andes*
4. Seguirá profundizando en la selección hasta que no existan más ramas en el árbol
5. BE buscará la plantilla de configuración del producto adecuada a las caracteríticas del producto seleccionado. Ejemplo: no es lo mismo una plantilla para un viaje de egresados a Bariloche que una para un viaje de egresados a Córdoba->Carlos Paz
6. El alumno deberá configurar los nodos obligatorios del árbol de configuración y podra optar po completar los opcionales
7. Una vez que el alumno considere finalizada su configuración y BE valide su completitud, deberá indicarlo tildando la señal de proceso finalizado

##### Proceso finalizado
El alumno contará con un control que le permitirá indicar que ha finalizado con todos los pasos del proceso. Este control solo será accesible en el proceso de configuración del producto y se habilitará luego de que se hayan seleccionado todos los nodos obligatorios.
El alumno podrá deseleccionar el control si desea reveer su configuración, siempre y cuando el proceso de incubación no haya finalizado.
El proceso de incubación finaliza cuando 3/4 de los alumnos han marcado su configuración como terminada.

#### Attributes
No aplica

### Processes related to this concept
* [Check-in](../process/check-in.md)

### Relationships with other concepts
* [Gestación](gestacion.md)
* [Desarrollo](development-phase.md)

### Examples 
In line