Desarrollo
======

### Definition

Se denomina Desarrollo a la fase del ciclo de vida del [objetivo](objetivo.md) de un Grupo en la cual los miembros de éste reciben ofertas, las analizan y, finalmente, toman una decisión sobre ellas.

#### Description

Esta etapa es precedida por la fase de [incubacion](incubacion.md), en la que los miembros han definido todas las características del producto a adquirir las cuales son presentadas en esta etapa (desarrollo) a los proveedores para que elaboren las propuestas. Esta etapa está compuesta por los siguientes pasos:

1. Consolidación del objetivo
1. Visibilidad del objetivo
1. Recepción de ofertas
1. Ranking de ofertas
1. Adhesión a una oferta

A continuación se describen en detalle los pasos arriba mencionados.

##### Consolidación del objetivo

Bulkaria realiza la consolidación de todos los objetivos individuales de los miembros en un único objetivo grupal. Esto puede ser realizado gracias a que los objetivos individuales coinciden en la _Clase de producto_.
Pero como a partir de la clase de producto los miembros pueden divergir en varias características del mismo objetivo, BE mostrará todas las preferencias cuenten con un 15% (1/7) de adhesiones sobre el total del miembros que configuraron la misma clase de producto.

{{{{{{{{{{{{{{ REVISAR }}}}}}}}}}}}}}

##### Visibilidad del objetivo

Este paso consiste básicamente en dar visibilidad al objetivo perseguido por los miembros del grupo a todos los proveedores registrados que puedan hacer una oferta acorde con este objetivo. Los proveedores seleccionados por Bulkaria para cotizar son invitados por medio de correo electrónico. La selección de estos proveedores es realizada de acuerdo a su afinidad con el objetivo del grupo. Ejemplo: Si el objetivo del grupo es realizar un viaje de egresados donde un porcentaje desea hacerlo a Bariloche y otro porcentaje a Mendoza, Bulkaria invitará a todos los operadores turísticos habilitados a realizar uno o ambos de los destinos y que hayan indicado que desean recibir alertas de cotizaciones desde el lugar de origen del grupo.

##### Recepción de Ofertas

Los proveedores habilitados (de ahora en más _proveedores_) son informados por Bulkaria de que existe una oportunidad de negocios y son habilitados en el sistema para acceder a la información del [objetivo consolidado del grupo](incubacion.md).

Los proveedores pueden ver todas las alternativas  de configuración con su correspondiente _peso_ (cantidad de preferencias). Los proveedores pueden ahora interactuar con los miembros del _Grupo_ a través de un hilo propio en el _Muro del Objetivo_ [Hilo de Ofertas del Proveedor](hilo_ofertas.md) 

Un proveedor puede presentar ninguna, una o más ofertas. Todas las ofertas de un proveedor podrán ser discutidas en el [Hilo de Ofertas del Proveedor](hilo_ofertas.md).  

La recepción de ofertas es anunciada a los miembros mediante alertas (solo a quienes estén suscritos, ver [perfil de grupo](perfil-de-grupo.md)) y podrán ser examinadas en el [pizarrón de ofertas](offer-blackboard.md).

A medida que el grupo va recibiendo ofertas cada miembro podrá realizar un ranking personal de las mismas (ver mas abajo _Ranking de Ofertas_). 

Las ofertas tendrán tres atributos comunes y obligatorios:
* Validez de la oferta (FV): fecha límite para adherir a la misma
* Cupo mínimo de oferta (C-): cantidad mínima de adherentes para que la oferta se haga efectiva
* Cupo máximo de oferta (C+): máxima cantidad de adherentes que tolera la oferta

Cuando una oferta está próxima a llegar a su FV y no fue cubierto el C- se alertará al proveedor que la propuso para que evalúe modificar el FV. Si el proveedor opta por mantener el FV, llegada esta fecha la oferta  desaparece automáticamente del pizarrón, alertando a el oferente que la propuso y a los adherentes hasta el momento.

Si por el contrario la oferta llegara a su FV con una cantidad de adherentes igual o superior a C- (pero inferior o igual a C+, control que realizará BE en el momento de cada adhesion), se considerará adoptada la oferta y los miembros adherentes a la misma podrán pasar a la etapa de [cierre](cierre.md) en la fecha que el proveedor determine.

##### Ranking de Ofertas

Desde el momento de recepción de una oferta, ésta podrá ser evaluada por los miembros del Grupo. Para la evaluación, Bulkaria contará con las siguientes funcionalidades.

* Ranking de ofertas según proximidad con el Objetivo del miembro
* Ranking de ofertas según proximidad con el Objetivo del Grupo
* Filtros de selección por Clase, Características y configuración del Objetivo
* Filtros de selección de Proveedores
* Agrupación de Ofertas
* Comparación de Ofertas

Con el ranking individual de cada miembro BE conformará un ranking grupal en tiempo real que será visible a todos los miembros y proveedores. Este ranking grupal servirá para que cada miembro vea a lo que tiende el grupo y decida si cambia su ranking a favor del grupal o se mantiene en su posición. También servirá a los proveedores para confeccionar nuevas ofertas que le permitan posicionarse mejor en el ranking.

##### Adhesión a una oferta

Un miembro da por finalizada su selección de una propuesta cuando luego de experimentar con el ranking decide que tiene una decisión formada y procede al siguiente paso que consiste en adherir a una oferta.

En BE la adhesión a una oferta debe ser realizada por el miembro alumno y uno de los miembros padre relacionado al alumno, solo con la adhesión simultanea del alumno y de uno de sus padres Bulkaria descuenta un cupo de la propuesta seleccionada.

BE informa al proveedor de cada adhesión pero sin indicar de que miembro se trata. También muestra a los miembros del grupo la cantidad de adhesiones a una propuesta, pero en este caso los miembros si podrán ver que compañero adherió.

Un miembro podrá retractarse de su adhesión mientras la propuesta no se haya cerrado y cuando lo haga Bulkaria delvolverá el cupo resignado al total de disponibles para esa propuesta.

Cuando para una propuesta la cantidad de adhesiones halla llegado a C- se sucederán los siguientes eventos:

1. Se informará al proveedor que su oferta ha completado el cupo mínimo y se le pedirá la fecha de cierre, es decir hasta que fecha podrán adherirse más miembros y posterior a la cual se comenzará con la [etapa de cierre](cierre.md) propiamente dicha.
1. Cada miembro adherente será informado de que se completó el cupo mínimo de la propuesta a la que adirió y de la fecha de cierre que deterinó el proveedor.
1. Los demás miembros no adherentes también serán informados invitándoles a adherir a la propuesta antes de la fecha de cierre.
1. BE realizará el balance de adhesiones que consistirá en:
    * sumar las adhesiones por propuestas no cerradas
    * contabilizar los miembros indecisos, es decir los que no han adherido a ninguna propuesta
    * Estimar que otras propuestas pueden ser cerradas con este universo de miembros y cuales no, teniendo en cuenta el cupo de cada una.
1. BE informará a los miembros adherentes a propuestas no cerradas y a los indecisos de la posibilidad o no de cerrar alguna otra propuesta, especificando cual o cuales.
1. Los miembros indecisos y los adherentes a propuestas abiertas podrán sumarse (previo a retractarse de la propuesta actual en este ultimo caso) a la nueva propuesta cerrada antes de la fecha de cierre indicada por el proveedor.
1. Una vez alcanzada la fecha de cierre la propuesta pasará a la siguiente etapa y ya no se podrán adherir nuevos miembros a la misma.

#### Attributes

### Processes related to this concept

### Relationships with other concepts
* Link to other concept 
* ...
* Link to other concept

### Examples 

Provide some concrete examples whenever possible
* Example 
* ...
* Example
