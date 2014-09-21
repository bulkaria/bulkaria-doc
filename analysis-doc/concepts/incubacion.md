Incubación
======

### Definition
Se llama incubación a la fase en que los miembros definen las características del [producto](producto.md) que desean contratar.

#### Description
Esta es una de las fases más importantes de BE, en ella los miembros definen las características del producto que desean contratar siguiendo el flujo que se explica más abajo. 

Antes de iniciar con el proceso se entiende que el actor [miembro](../actors/miembro.md) ha realizado el proceso de [check-in](../process/check-in.md) convirtiéndose en un [miembro](../actors/miembro.md) del [grupo](../actors/grupo.md).

En este proceso, el miembro interactúa con tres estructuras bien definidas, **clase de producto**, **objetivo** y **configuración del objetivo**.

##### Clase de producto
La clase de producto acota el tipo de objetivo que podrá configurar un miembro. Cada clase de producto agrupa objetivos de un mismo tipo, con características intrínsecamente similares y con un ciclo de vida común. Un miembro del grupo podrá definir varias clases de producto diferentes, es decir apuntar a varios objetivos distintos, por ejemplo *viaje de egresados* y *fiesta de egresados*, pero cada uno tendrá su propio ciclo de vida, por lo tanto sus propios tiempos, un único [wall](wall.md), etc.

Si bien el grupo puede tener cualquier cantidad de miembros, no necesariamente todos compartirán las mismas clases de productos, es decir los mismos objetivos. Cuando un miembro comience a configurar un objetivo partiendo de seleccionar una clase de producto, verá la actividad de los miembros que estén configurando la misma clase y podrá interactuar con ellos a través de comentarios tanto en el wall asociado al objetivo como en cada ítem de la configuración.

No obstante esta separación de objetivos, todos los miembros podrán interactuar independientemente de estos en el [wall general del grupo](wall.md)

##### Objetivo
Dada una clase de producto cada miembro podrá definir el _producto objetivo_ que consiste en seleccionar las características esenciales del producto que lo hacen diferente de otros productos de la misma clase. Para ello Bulkaria contará con una plantilla por clase de producto que consistirá en un conjunto de todas las características que poseen todos los productos de la misma clase. Mediante esta plantilla cada miembro irá definiendo el objetivo como se explica a continuación. 

Las características tienen una organización jerárquica de árbol con varias raíces y el objetivo queda completamente definido cuando se ha seleccionado un rama completa de **cada** raíz del árbol. Ejemplo: para la clase *viaje de egresados* el objetivo del producto seleccionado por un miembro (ramas completas) podría ser: 
```
Destino > Nacional > Bariloche
Mes > Septiembre
```
Cada nodo del árbol de características cuenta con la posibilidad de recibir comentarios en los que los miembros podrán fundamentar su elección y/o contestar otros comentarios de manera anidada (ver [estructura de comentarios](estructura-de-comentarios.md)).

Cada miembro verá la tendencia en el objetivo del grupo gracias a un indicador que mostrará las características seleccionadas por sus compañeros. Ejemplo:
```
+ Destino
|-- Nacional [+18]
    |-- Bariloche [+15] <- Tu selección
    |-- Mendoza [+3]
    |-- San Martín de los Andes [--]
|-- Internacional [+12]
    |-- Brasil [+10]
        |-- Rio de Janeiro [+10]
        |-- Torres [--]
    |-- Europa [+2]
        |-- Barcelona+Madrid+Paris+Londres [+2]
        |-- Barcelona+Madrid+Berlin+Roma [--]
```

A medida que el miembro vaya definiendo las características, y en base a un costo de referencia que tendrá cada rama, podrá ver un costo total aproximado de su propio objetivo y el del objetivo grupal.

##### Configuración del objetivo
Una vez seleccionado el objetivo, el miembro debe proceder a definir la configuración del mismo. La configuración del objetivo consiste en definir las preferencias sobre las características que definen el objetivo a un nivel de mayor detalle, detalles que podrán diferir con las preferencias de otros miembros con el mismo objetivo.

Para este fin el miembro cuenta con una estructura de árbol con varias raíces que va recorriendo por rama y definiendo, en cada nodo que lo requiera, su preferencia. Esta estructura es propuesta por Bulkaria en base a una plantilla asociada al objetivo seleccionado en el paso anterior.

La preferencia del miembro será indicada mediante un valor numérico entre 0 y N dependiendo de:

* si el nodo es final (no tiene hijos o subnodos):
    * podrá recibir 0 ó 1 si es de opción binaria (si o no)
    * podrá recibir 0 ó N si es de opción unitaria (cuantas unidades se desean)
    * podrá recibir 1 ó N si es de opción unitaria obligatoria (al menos se debe optar por una unidad)
* si el nodo tiene hijos (subnodos):
    * podrá ser 0 ó 1 si es de opción única no obligatoria, es decir si se puede elegir un subnodo y solo uno o ninguno
    * podrá ser 0 ó N si es de opción múltiple no obligatoria, es decir se pueden elegir uno o mas subnodos o ninguno
    * podrá ser 1 si se debe elegir uno y solo uno de sus subnodos
    * podrá ser 1 ó N si de de opción múltiple obligatoria, es decir se deben elegir uno o mas subnodos.

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
Cada nodo del árbol de configuración cuenta con la posibilidad de recibir comentarios en los que los miembros podrán fundamentar su elección y/o contestar otros comentarios de manera anidada (ver [estructura de comentarios](estructura-de-comentarios.md)).

Cada miembro verá la suma de los valores que cada uno de sus compañeros, con el mismo objetivo, han asignado a un nodo y de esta manera tendrá un panorama de la configuración a la que tiende el grupo. Estos indicadores con dinámicos, ya que dependen de los tiempos de interacción de los miembros con la plataforma.

A medida que el miembro va realizando la configuración y en base a costos de referencia (promedio o maximo/mínimo) que tendrá cada nodo, dispondrá de un costo total aproximado del producto. Y en base a la configuración consolidada de todos los miembros también podrá ver una tendencia del costo total aproximado de la preferencia del grupo.

##### Flujo del proceso de incubación
Para una mejor comprensión de los pasos de este proceso, a continuación se ejemplifica con el flujo de la [clase de producto](clase-de-producto) **viaje de egresados**.

1. El miembro selecciona la clase de producto de acuerdo al objetivo pretendido. Esto creará una instancia de dicha clase para el miembro. Ejemplo: Selecciona **viaje de egresados**
1. Se le presenta el árbol de caracteríticas y debe selecionar un nodo por cada raíz del arbol
1. Luego de seleccionar un nodo raíz (por ejemplo: **Destino**) debe seleccionar uno de los subnodos que se le presentan (de existir alguno). Ejemplo: **Nacional** o **internacional**
1. Seguirá profundizando en la selección hasta que no existan más ramas en el árbol. Ejemplo:
```
Destino > Nacional > Neuquén > Bariloche
Mes > Septiembre
```
1. BE consulta al usuario si desea continuar con el siguiente paso: Configuración del objetivo
1. BE buscará la plantilla de configuración del objetivo adecuada al objetivo seleccionado. Ejemplo: no es lo mismo una plantilla para un viaje de egresados a Bariloche que una para un viaje de egresados a Carlos Paz
1. El miembro deberá configurar los nodos obligatorios del árbol de configuración y podrá optar por completar los opcionales
1. Una vez que el miembro considere finalizada su configuración y BE valide su completud, deberá indicarlo tildando la señal de proceso finalizado

##### Proceso finalizado
El miembro contará con una marca de control que le permitirá indicar que ha finalizado con todos los pasos del proceso. Esta marca de control solo será accesible en el proceso de configuración del objetivo y se habilitará luego de que se hayan seleccionado todos los nodos obligatorios.
El miembro podrá desmarcar el control si desea rever su configuración, siempre y cuando la etapa de incubación no haya finalizado.
El proceso de incubación finaliza cuando 3/4 de los miembros han marcado su configuración como terminada.

#### Attributes
No aplica

### Processes related to this concept
* [Check-in](../process/check-in.md)

### Relationships with other concepts
* [Gestación](gestacion.md)
* [Desarrollo](desarrollo.md)

### Examples 
In line