Incubación
======

### Definition
Se llama incubación a la fase en que los miembros definen las características del producto o servicio que desean contratar.

#### Description
Esta es una de las fases más importantes de BE, en ella los miembros definen las características del producto o servicio que desean contratar siguiendo el flujo que se explica más abajo. 

Se entiende que el actor [miembro](../actors/miembro.md) ha realizado el proceso de [check-in](../process/check-in.md), convirtiéndose en un [miembro](../actors/miembro.md) del [grupo](../actors/grupo.md), antes de iniciar el proceso.

En este proceso, el miembro interactúa con tres estructuras bien definidas: **clase de objetivo**, **objetivo individual** y **configuración del objetivo individual**.

##### Clase de objetivo
La clase de objetivo acota el tipo de objetivo que podrá configurar un miembro. Cada clase de objetivo agrupa objetivos de un mismo tipo, con características intrínsecamente similares y con un ciclo de vida común. Un miembro del grupo podrá definir varias clases de objetivos diferentes, es decir apuntar a varios objetivos distintos, por ejemplo *viaje de egresados* y *fiesta de egresados*, pero cada uno tendrá su propio ciclo de vida, por lo tanto sus propios tiempos, un único [wall](wall.md), etc.

Si bien el grupo puede tener cualquier cantidad de miembros, no necesariamente todos compartirán las mismas clases de objetivos, es decir los mismos objetivos. Cuando un miembro comience a configurar un objetivo partiendo de seleccionar una clase de objetivo, verá la actividad de los miembros que estén configurando la misma clase y podrá interactuar con ellos a través de comentarios tanto en el wall asociado al objetivo como en cada ítem de la configuración.

No obstante esta separación de objetivos, todos los miembros podrán interactuar independientemente de estos en el [wall general del grupo](wall.md)

##### Objetivo individual
Dada una clase de objetivo cada miembro podrá definir una instancia de dicha clase que consiste en seleccionar las características esenciales del objetivo que lo hacen diferente de otros objetivos de la misma clase. Para ello Bulkaria contará con una plantilla por clase de objetivo que consistirá en un conjunto de todas las características que poseen todos los objetivos de la misma clase. Mediante esta plantilla cada miembro irá definiendo su objetivo individual como se explica a continuación. 

Las características tienen una organización jerárquica de árbol con varias raíces y el objetivo queda completamente definido cuando se ha seleccionado un rama completa de **cada** raíz del árbol. Ejemplo: para la clase *viaje de egresados* el objetivo individual de un miembro (ramas completas) podría ser: 
```
Destino > Nacional > Bariloche
Mes > Septiembre
```
Cada nodo del árbol de características cuenta con la posibilidad de recibir comentarios en los que los miembros podrán fundamentar su elección y/o contestar otros comentarios de manera anidada (ver [estructura de comentarios](estructura-de-comentarios.md)).

Cada miembro verá la tendencia del grupo visualizando los distintos objetivos grupales definidos al momento.  Ejemplo:
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

A medida que el miembro vaya definiendo las características, y en base a un costo de referencia que tendrá cada rama, podrá ver un costo total aproximado de su [objetivo individual](objetivo.md) y los costos estimados de los diferentes [objetivos grupales](objetivos.md)  definidos hasta este momento.

##### Configuración del objetivo individual
Una vez seleccionado el objetivo, el miembro debe proceder a definir la configuración del mismo. La configuración del objetivo consiste en definir las preferencias sobre las características en mayor detalle; detalles que podrán diferir con las preferencias de otros miembros que compartan el mismo objetivo (objetivo grupal).

Para este fin el miembro cuenta con una estructura de árbol con varias raíces que va recorriendo por rama y definiendo, en cada nodo su preferencia. Esta estructura es propuesta por Bulkaria en base a una plantilla asociada al objetivo seleccionado en el paso anterior.

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

Cada miembro podrá visualizar la tendencia sobre cada item de configuración a través de un indicador de tendencia ('heat-map', estrellita, etcs. a definir). Estos indicadores son dinámicos, ya que dependen de los tiempos de interacción de los miembros con la plataforma.

##### Clonado de un objetivo individual NUEVO!
Un miembro puede optar por evitar todo el preceso de seleccionar y configurar su objetivo individual clonando (copiando) el de otro miembro que ya lo haya realizado. Si clona un objetivo individual ya finalizado, el mismo será copiado pero sin la marca de finalización, es decir el miembro específicamente deberá finalizarlo.
El clonado de un objetivo individual permite su posterior modificación por si el miembro quisiera variar alguna configuración.

##### Flujo del proceso de incubación
Para una mejor comprensión de los pasos de este proceso, a continuación se ejemplifica con el flujo de la [clase de objetivo](clase-de-objetivo) **viaje de egresados**.

1. El miembro selecciona la clase de objetivo de acuerdo al objetivo pretendido. Esto creará una instancia de dicha clase para el miembro. Ejemplo: Selecciona **viaje de egresados**
1. Se le presenta el árbol de caracteríticas y debe selecionar un nodo por cada raíz del arbol
1. Luego de seleccionar un nodo raíz (por ejemplo: **Destino**) debe seleccionar uno de los subnodos que se le presentan (de existir alguno). Ejemplo: **Nacional** o **internacional**
1. Seguirá profundizando en la selección hasta que no existan más ramas en el árbol. Ejemplo:
```
Destino > Nacional > Neuquén > Bariloche
Mes > Septiembre
```
**Nota.** En este momento se considera que el miembro ha definido su objetivo individual.


1. BE consulta al usuario si desea continuar con el siguiente paso: Configuración del objetivo individual
1. BE buscará la plantilla de configuración del objetivo según el objetivo seleccionado. Ejemplo: no es lo mismo una plantilla para un viaje de egresados a Bariloche que una para un viaje de egresados a Carlos Paz.
1. El miembro deberá configurar los nodos obligatorios del árbol de configuración y podrá optar por completar los opcionales
1. Una vez que el miembro considere finalizada su configuración y BE valide su completud, deberá indicarlo tildando la señal de proceso finalizado

###### Señal de proceso finalizado
El miembro contará con una marca de control que le permitirá indicar que ha finalizado con todos los pasos del proceso. Esta marca de control solo será accesible en el proceso de configuración del objetivo y se habilitará luego de que se hayan seleccionado todos los nodos obligatorios.
El miembro podrá desmarcar el control si desea rever su configuración, siempre y cuando la etapa de incubación no haya finalizado (ver a continuación).

##### Finalización de la etapa de incubación
La finalización de la etapa de incubación no esta definida aun, pero tiene cuatro escenarios posibles a saber.

###### Escenario 1: Con 3/4 de los miembros del grupo
El proceso de incubación finaliza cuando 3/4 de los miembros del grupo han finalizado la configuración de su  objetivo individual.

###### Escenario 2: Con 3/4 de los miembros de la clase
El proceso de incubación finaliza cuando 3/4 de los miembros que han instanciado la misma clase de objetivo, han marcado su configuración como finalizada.

###### Escenario 3: El primer miembro finaliza la configuración
El proceso de incubación finaliza cuando uno cualquiera de los miembros que han instanciado la misma clase de objetivo, han marcado su configuración como finalizada.

###### Escenario 4: 7 miembros han finalizado la configuración
El proceso de incubación finaliza cuando 7 (siete) cualquiera de los miembros que han instanciado la misma clase de objetivo, han marcado su configuración como finalizada.

##### Resolución de conflictos
Cuando (independientemente del escenario) no se pueda cumplir con la condición requerida para finalizar la etapa de incubación, se pordrá finalizar a través de una [asamblea](asamblea.md). 

#### Attributes
No aplica

### Processes related to this concept
* [Check-in](../process/check-in.md)

### Relationships with other concepts
* [Gestación](gestacion.md)
* [Desarrollo](desarrollo.md)

### Examples 
In line