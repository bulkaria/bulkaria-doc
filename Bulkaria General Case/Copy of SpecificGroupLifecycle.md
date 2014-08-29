	 	 	 	

**BulKariA**

Ciclo de Vida

Grupo Específico

# Table of contents

[Table of contents](#heading=h.4d34og8)

Nomenclatura del documento

Hashtags

Actores y conceptos

Etapa de Gestación

Determinación del tipo de producto

Determinación de la visibilidad

Invitación a miembros fundadores

Check-in del promotor

Lanzamiento del grupo

Finalización de la gestación

Check-in

Etapa de Incubación

Asignación del Asesor

Check-in disponible

Apertura del Muro del Grupo

Apertura del Blackboard del Grupo

Votar Preferencias

Consolidación de preferencias

Definición de la demanda

[Atributos a ser pasados a la siguiente etapa](#heading=h.3o7alnk)

Tipo de Producto

Cantidad

Preferencias

Condiciones de Compra

Rango de Precio

Medio de Entrega

[Otros (dependientes del Tipo de Producto)](#heading=h.vx1227)

Etapa de Desarrollo

Contacto con los proveedores

Recepción de ofertas

Funcionalidad del Blackboard Offer

[Estado de la oferta en tiempo real](#heading=h.28h4qwu)

Mejora de ofertas

Selección del Oferente

Funcionalidad del Blackboard Pick

Oferente Seleccionado

Etapa de Producción

Introducción

Consolidación

Incorporación de nuevos Miembros

Compras adicionales

Cierre de la Oferta

Entrega de Productos

Etapa de Cierre

Situaciones de cierre

Acciones de Cierre

# Nomenclatura del documento

Con el fin de formalizar conceptos, se utilizarán las siguientes convenciones:

@término se referirá a un actor.

{término} se referirá al estado que podrá tomar algún actor.

&término se referirá a un concepto (evento, acción o método) aplicable a un actor, proceso o estado.

[término] se referirá a algún proceso o caso de uso del sistema.

## Hashtags

Los hashtag tiene como propósito marcar dentro del documento párrafos a revisar. son los siguientes:

#define indica una concepto que se debe definir.

#check-xxx indica que se debe revisar el proceso xxxxx.

#new indica modificaciones realizadas por alguien sobre párrafos ya revisados por todos y que deben ser consensuadas. Una vez consensuadas se debe quitar este hashtag.

## Actores y conceptos

Los siguientes son los actores que intervendrán en todos los casos de uso del sitio:

* **@bulkaria-site: **sistema encargado de orquestar los actores y procesos de la compra en grupo.

* **@bulkaria: **empresa que gestiona @bulkaria-site.

* **@usuario:** persona física que se ha registrado al sitio utilizando su cuenta de alguna red social que @bulkaria-site habilita, o creando una nueva cuenta.

* **@empresa**: persona física o jurídica registrada en @bulkaria-site por un @usuario, representante legal o persona debidamente autorizada para gestionar las relaciones comerciales entre @empresa y @bulkaria.

* **@oferente:** @empresa que interviene en un @grupo con el fin de proveer el bien o servicio solicitado por el mismo.

* **@miembro: **@usuario que compone algún grupo de compra.

* **@visitante:** persona que no se ha registrado a @bulkaria-site y que accede anónimamente.

* **@comprador:** es un @miembro de un @grupo que está en estado {producción} y ya realizó su pago.

* **@promotor:** @usuario responsable de crear un grupo.

* **@asesor:** @usuario que ejerce la función de asesor.

* **@moderador**: @usuario perteneciente al staff de @bulkaria que interviene en la moderacion de los contenidos (Muro) #new #define

* **&categoría:** agrupación jerárquica de productos.

* **&tipo-producto:** último elemento de una árbol (hoja) de categorías a partir del cual se definen productos específicos, perfectamente identificables y existentes en el mercado.

* **&producto-especifico:** producto cuya definición se corresponde exactamente con uno existente en el mercado.

* **@grupo:** conjunto de @usuarios agrupados con el fin de comprar un bien o servicio. Un @grupo puede ser {público}, cualquier @usuario puede integrarlo, o {privado} al cual se accede sólo por invitación. Existen tres tipos de grupos:

    * {genérico} grupo creado a partir de un &tipo-producto seleccionado luego de recorrer el árbol de categorías.

    * {específico} grupo creado a partir de un producto específico y existente en el mercado.

    * {oferta-fija} grupo creado por un @oferente quien oferta un producto específico con la condición de completar la venta de una cantidad establecida.

* **&condiciones-compra:** son condiciones asociadas a la compra que no constituyen la definición del producto, por ejemplo cantidad, rango de precio, método de entrega, garantía, etc. Pueden existir limitaciones a estas condiciones según el &tipo-producto #define.

* **@UTO:** Unión temporal de oferentes organizados para cubrir una demanda de un @grupo {genérico} que supera el stock individual de cada uno. #define

* **&wall:** funcionalidad de @bulkaria-sitio que permite a los @miembros debatir sobre el objetivo de compra dentro de un @grupo y cuestiones relevantes del ciclo de vida del mismo. El &wall es solo lectura para @usuarios. Un @usuario podrá hacerse @miembro para solicitar aclaraciones mediante el &wall y luego abandonar el @grupo sin penalidad mientras el mismo no esté en {production}. #new

* **&group-blackboard: **funcionalidad de @bulkaria-sitio que permite a los @miembros consolidar las preferencias y condiciones de compra.

* **&offer-blackboard: **funcionalidad de @bulkaria-sitio que permite a los @oferentes publicar sus ofertas para que los @miembros seleccionen una.

* **&locación:** ubicación geográfica de un @grupo o @usuario. Esta deberá ser indicada a nivel ANYWHERE, país, zona, provincia, ciudad o barrio, pudiendo, de acuerdo al contexto, no indicar todos los niveles, por ejemplo: un grupo puede tener alcance de país, otro de país/zona/provincia, etc. El valor especial ANYWHERE indica que para el contexto no importa la locación. #new

# Etapa de Gestación

La etapa de gestación es el primer estadio de un @grupo {específico}.Comienza con la creación de un grupo por parte del @promotor y finaliza cuando la cantidad mínima de seis invitados ha realizado el &check-in.

Tiene como objetivo lograr la creación de grupos exitosos, por lo cual las características de este proceso son muy importantes.

A continuación se definen los distintos eventos que forman parte de este proceso.

## Determinación del tipo de producto

El @promotor debe seleccionar un &producto-especifico navegando por las distintas categorías de productos, que @bulkaria-site provee, hasta encontrar el que mejor define el objetivo de compra del grupo. Dicha definición incluye las características comerciales del producto que lo identifican unívocamente. #new

Una vez seleccionadas, las características de este producto permanecerán invariables durante esta etapa. #new

## Determinación de la visibilidad

En este punto el @promotor debe indicar si el grupo será {público} o {privado}.

## Invitación a miembros fundadores

El @promotor debe indicar un mínimo de 6 (seis) contactos, que junto con él, le darán creación al grupo para que este pueda pasar al siguiente estadio {hatching}. Lo hará enviándole invitaciones por correo electrónico y/o redes sociales habilitadas por @bulkaria-site.

También deberá indicar, si es un grupo {privado}, quien puede invitar a otros @miembros, existiendo las siguientes posibilidades:

* Solo el @promotor.

* Los @miembros que el @promotor específicamente indique (con un tilde que se habilita a tal fin en cada invitación).

* Todos los @miembros del grupo.

## Check-in del promotor

Durante la creación del grupo el @promotor deberá realizar su propio &check-in al grupo. Este proceso es común a todos los @usuarios que quieran enrolarse como @miembros del @grupo y sus características varían de acuerdo al estado en que el @grupo se encuentra.

Ver más adelante detalles del &check-in.

## Lanzamiento del grupo

Luego de realizar el &check-in el @promotor podrá lanzar la creación del @grupo, verificando que todos los datos ingresados sean correctos (resumen que le presentará @bulkaria-site).

Se denomina lanzamiento y no creación pues el @grupo no será una realidad hasta que el mínimo de seis @usuarios invitados hayan realizado el &check-in.

## Finalización de la gestación

Una vez que el @promotor ha lanzado la creación del @grupo, comienza a cronometrarse el periodo de confirmación de las invitaciones. Este periodo será solo de 24 horas #define.

La gestación finaliza con dos posibles resultados:

* Creación del grupo

Si durante el periodo de confirmación se cumplen los seis &check-in (siete contando al @promotor) el grupo pasará inmediatamente al estado de {creado} y @bulkaria informará de ello a todos los @miembros del @grupo hasta el momento (siete mínimo) y el @grupo pasará al siguiente estado {hatching}

* Eliminación de la petición de nuevo grupo

Durante el mismo, un mínimo de seis @usuarios invitados deberán realizar el &check-in al @grupo. Si pasado este periodo no se han realizado los seis &check-in, el grupo no se creará y @bulkaria-site enviará un correo a quienes hayan realizado el &check-in, @promotor incluido, informándoles de esta situación y procediendo a la eliminación del @grupo.

## Check-in

Se denomina &check-in a la transacción que deben realizar los @usuarios para convertirse en @miembros de un @grupo. Dicha transacción requiere que el @usuario indique una serie de datos que podrán variar de acuerdo al &producto-específico y al estado del @grupo.

El @usuario recibe la invitación a unirse al @grupo por correo y/o redes sociales, u otro medio que implemente @bulkaria-site o, si el @grupo es {público} se une seleccionando la opción "unirse" en la publicación del grupo en @bulkaria-site u otro sitio donde @bulkaria promocione el grupo.

Las principales características del &check-in son:

* La persona debe ser @usuario de @bulkaria-site, en caso contrario será redireccionado a la transacción de &registro  previo al &check-in.#define

---------------------------- 28-09-2013-------------------

* La &locación del @usuario es importante en el @grupo, pero no será necesario que la indique si ya la cargó en su perfil, salvo que desee indicar una distinta. Siempre será prioritaria la &locación indicada a nivel de @grupo, es decir en caso que el @oferente envíe a domicilio solo estará obligado a cubrir esta, aunque si la mayoría de los @miembros indican una distinta, el @oferente podrá tomar en cuenta esta tendencia. #new

* El @usuario deberá indicar todas las &condiciones-compra que sean definidas para el &tipo-producto heredadas en el caso de &producto-especifico. Asumimos que no existirán preferencias catalogadas obligatorias #check-hatching. #new

# Etapa de Incubación

El estado de Incubación cuenta con dos herramientas de colaboración el Group Blackboard y el Muro, ambos espacios se abren al comienzo del proceso, pero a diferencia del Wall, que permanece abierto durante toda la vida del grupo, el Group Blackboard se cierra una vez finalizado el proceso de hatching.

## Asignación del Asesor

* Un asesor será asignado al Grupo una vez que se ingresa en esta etapa. (Se deben definir aún las funciones específicas de este rol). #define

**Activación del Grupo**

Una vez realizado el proceso de check-in de los siete @miembros minimos para la creacion de un Grupo, el mismo pasa al estado "activo" y es visible en en las búsquedas y grupos destacados.

### Check-in disponible

* Mientras dure el proceso de hatching, development y production, el check-in permanece abierto y por más que la mayoría de @miembros no concuerde con la locación del grupo, ésta permanecerá inalterable.

## Apertura del Muro del Grupo

El muro es el lugar donde los @miembros del grupo pueden socializar y discutir sobre la conformación del producto de manera desestructurada, por ejemplo solicitando se les vote determinada preferencia.

Características: 

* El muro es visible para @miembros y @usuarios en un grupo público.

* El muro es visible sólo para los @miembros en un grupo privado. #check-close

* En el muro solo pueden realizar entradas los @miembros del grupo. 

* En el muro también participa el @asesor si es necesario.

* Esta conformado por mensajes que pueden ser respondidos de manera anidada.

* Los mensajes de mayor actividad se muestran primero, aunque debería contemplarse alguna función de ordenamiento y quizás de búsqueda también.

* No se permiten imágenes pero si links internos y externos.

* Los mensajes pueden ser advertidos para que un @moderador de Bulkaria tome una acción. #define

* Los mensajes no son anónimos.

* Los usuarios de BulKaria se pueden suscribir al wall para recibir avisos por email de eventos (nuevos mensajes, comentarios a mensajes propios, etc.)

* El muro permite el envío de mensajes privados (MP) entre los usuarios.

* El muro no se cierra luego del hatching.

* El muro no es visible a los @oferentes (aunque nada evita que tengan usuarios comunes para este menester).

## Apertura del Blackboard del Grupo

En el Group Blackboard se visualizarán las Preferencias y las Condiciones de Compra.

**Preferencias**

Para un producto específico solamente se exponen las preferencias Catalogadas. Estas tienen una estructura formal de [atributo, valor/es].

Existen dos tipos de Preferencias Catalogadas: obligatorias y opcionales, según el tipo de producto.

### Votar Preferencias

* Se votarán solamente las preferencias Catalogadas Opcionales y sólo pueden recibir votos positivos (me gusta).

**Condiciones de compra**:

* Price range. Cada @miembro puede indicar un rango de precios distinto al establecido en la creación del grupo, pero dentro de un más/menos X% que dependerá del product type. Bulkaria establecerá el rango de precios de acuerdo a un algoritmo basada en la curva de distribución de las entradas de los usuarios #define. Esta es la única preferencia (system o user) que se muestra en la ficha cuando el grupo está en estado de hatching.

* Delivery method. Cada @miembro podrá indicar un tipo de entrega entre:

    * A domicilio

    * Retira en local

    * Domicilio del grupo (nuevo parámetro de grupo - opcional)

* Others. Pueden existir otras condiciones de compra obligatorias que dependan del tipo de producto y son generadas por Bulkaria.

## Consolidación de preferencias

Se produce al cierre de la etapa de Incubación. Consiste en el cierre de las preferencias catalogadas opcionales y solo quedan aquellas con resultado positivo en las votaciones.. Esto quiere decir que ningún @miembro ingresado a partir de este punto puede votar por las existentes, se entiende que cuando un nuevo @miembro ingresa a partir de la Etapa de Desarrollo en adelante es porque acepta las preferencias del Grupo.

## Definición de la demanda

El proceso de hatching se cierra cuando se alcanzó la fecha de finalización establecida. #define

Principales eventos de la etapa:

* Se cierra el Group Blackboard.

* El Wall permanece abierto

* Se envía un correo de aviso de cierre a los @miembros: donde se informa del fin del proceso de incubación, se adjunta un enlace a los detalles del producto a adquirir, condiciones de compra y se invita a sugerir oferentes (con un límite establecido de fecha y hora)*.*

## Atributos a ser pasados a la siguiente etapa

### Tipo de Producto

Tipo de producto a ser adquirido de acuerdo a las categorías seleccionadas

### Cantidad

Cantidad total de productos a ser adquiridos

### Preferencias

Definición de las preferencias Catalogadas.

### Condiciones de Compra

Definición de las condiciones de compra del producto.

#### Rango de Precio

#### Medio de Entrega

#### Otros (dependientes del Tipo de Producto)

# Etapa de Desarrollo

## Contacto con los proveedores

En la etapa de desarrollo los oferentes @Oferente obtienen  visibilidad de los productos que son  requeridos por el grupo y definidos en la etapa anterior (Incubación)   El @oferente es notificado sobre la demanda específica. Las notificaciones se realizan a los oferentes que fueron sugeridos por los miembros integrantes del grupo y por @bulkaria-site que determina a qué @oferente invitar a participar según el rubro del  producto requerido en la compra.

El @oferente recibe un E-mail desde @bulkaria-site donde se lo invita a participar para  establecer su oferta según la demanda del producto definido, y se le informa básicamente lo siguiente:

* Tipo de producto

* Cantidad total  (requerida por cada miembro)

* Definición de las preferencias Catalogadas #new

* Condiciones específica de la compra

* Tiempo establecido de recepción de ofertas #Define

Si el @oferente aun no es @usuario de @bulkaria, @bulkaria-site  le envía un E-mail donde le  sugiere al @oferente (aun no usuario de @bulkaria-site) que se  inscriba de manera de  participar en la oferta.

El @oferente cuenta con un espacio específico donde puede visualizar todas las demandas de compra definidas por lo grupos y  acordes al rubro / categoría en la que el @oferente se ha registrado; de manera de autogestionar su participación y ofrecer sus productos activamente.

## Recepción de ofertas

Por cada demanda requerida de un grupo se genera un espacio denominado BlackBoard Offer, en el cual el  @oferente puede completar  y determinar su oferta específica. El @oferente responde a las preferencias que fueron establecidas por el grupo (cumple , no cumple). #new

La información correspondiente a la oferta  es confidencial y únicamente puede ser  visualizada por el @oferente participante, de manera que no es visible para otros oferentes participantes de este requerimiento de compra.

La oferta debe ser acorde a lo requerido en la definición del grupo, sin posibilidad de modificaciones. El mínimo de productos ofertados no puede ser superior a la cantidad de productos a adquirir y según lo requerido por los integrantes del grupo al momento de la apertura de esta etapa  (recepción de ofertas)

En la oferta se debe indicar, de manera obligatoria, la cantidad máxima de productos incluidos en la oferta.

## Funcionalidad del Blackboard Offer

El @oferente completa la información sobre cada una de las preferencias definidas por el grupo:

* Cumple con la preferencia  ( ) #new

* No cumple la preferencia: ( ) #new

El @oferente completa la información relativa a la cotización:

* Cantidad máxima de productos incluidos en esta oferta (límite superior de oferta -LSO)

* Cantidad mínima de productos (límite inferior de productos de la oferta - LIO)

* Cotización  por producto ($ )

El @oferente informa  sobre cada una de las características nomencladas, además cuenta con  la posibilidad de agregar "Características adicionales" en formato de de textos narrativos describiendo las características que considere adicionales e importantes sobre el producto. También puede agregar otras(*), de manera de lograr un mejor detalle de la oferta. #new

(*) Si un oferente desea indicar una nueva característica que aún no se encuentra nomenclada, puede solicitarle a @bulkaria-site para que sea agregada. @bulkaria-site analiza si la misma es pertinente al tipo de producto y realiza la inmediata incorporación o especifica la causa del rechazo.

El @oferente tiene visibilidad de los votos obtenidos, por parte de los miembros del grupo, de cada una de las preferencias del sistema. Con el propósito de orientarlo sobre el comportamiento del grupo.

### Estado de la oferta en tiempo real

Las ofertas que se van incorporando son visibles por los miembros del grupo en tiempo real, durante el tiempo establecido (recepción de ofertas) #define. Los miembros del grupo cuentan con un block de notas asociado a cada oferta, para realizar anotaciones sobre sus apreciaciones de la misma.

### Mejora de ofertas

Durante el tiempo establecido para la recepción de ofertas #define, el  @oferente puede realizar cambios de preferencias, precios y mejoras generales de las condiciones sobre la oferta originalmente realizada,

## Selección del Oferente

Una vez finalizada la recepción de las ofertas #define, los miembros del grupo tienen visibilidad de la matriz de las ofertas recepcionadas, de manera consolidada. @Bulkaria-site establece un ranking predefinido en forma ascendente sobre el posicionamiento de cada oferente.

El ranking se realiza por el cómputo de cumplimiento sobre las preferencias requeridas y por el mejor precio ofertado. La matriz de ofertas consolidada permite la apertura del Blackboard Pick.

### Funcionalidad del Blackboard Pick

Cada miembro del grupo puede evaluar cada una de las ofertas generando un voto de elección positivo o negativo sobre el @oferente.

El blackboard pick permite a los miembros del grupo evaluar mediante la validación (Cumple / No cumple) cada una de las preferencias y condiciones establecidas en la oferta. Así como aceptar (Valido / No valido) el precio ofertado del producto.

En el caso de que los miembros del grupo no evalúen las ofertas y por lo tanto no generan el voto de elección de un @oferente se finalizará la elección del @oferente una vez finalizado el tiempo de selección #define.

El blackboard Pick se muestra dinámico y en tiempo real modificando el estado y la posición del ranking de los oferentes.

Una vez que todos los miembros hayan votado o en su defecto se haya alcanzado el tiempo establecido para la elección del @oferente #define se realiza un proceso final de ranking posicionando al mejor @oferente.

### Oferente Seleccionado

Finalizada la elección del @oferente,@bulkaria-site informa a cada miembro integrante del grupo cuál fue el oferente seleccionado (mejor rankeado), e indicándole que se ha iniciado la etapa de confirmación de  la compra.

Cada miembro del grupo debe aceptar o rechazar la compra establecida sobre el @oferente seleccionado (confirmación de la compra).

@bulkaria-site informa en tiempo real a los miembros del grupo el estado de confirmación de compra en relación al límite inferior de productos de la oferta - LIO.

Una vez alcanzado o superado el límite inferior de productos de la oferta - LIO, producto de la confirmación de compra por parte de los miembros del grupo se pasa a la siguiente etapa denominada "Producción"

En  caso que el número de productos por compra confirmada sea menor al límite inferior de productos de la oferta - LIO @bulkaria-site informa y consulta  inmediatamente al @oferente si acepta la cantidad establecida (confirmación de compra) actual , si determina un tiempo de espera en las confirmaciones #define o rechaza su participación en la oferta.

Si el límite de espera #define es superado  o el @oferente rechaza su participación, el grupo de compra se cierra. @bulkaria-site informa a los miembros y al oferente que fue seleccionado el cierre de la compra.

**Consideraciones**:

Un miembro comprador no puede obtener más que el 15% del total de la compra el grupo (control que realiza @bulkaria-site)

# Etapa de Producción

## Introducción

La última etapa activa de un @grupo se denomina Producción. Comienza después de completarse la etapa de Desarrollo, en la cuál se define la mejor oferta, y precede a la etapa de Cierre, donde toda información relevante a la experiencia del @grupo en cuestión es clasificada y procesada como parte de un proceso de aprendizaje de @Bulkaria-site.

 

## Consolidación

Los @miembros que se comprometieron con la oferta ganadora deben efectuar sus pagos durante este proceso. Todos los métodos de pago operativos en @Bulkaria-site son electrónicos y sus transacciones asociadas producen sólo dos resultados posibles: pago aceptado o rechazado. Si el pago del @miembro es rechazado por cualquier motivo, el @miembro es debidamente informado, así  puede reintentarlo.

Una vez que el pago es procesado satisfactoriamente, el @miembro recibe una comunicación (email) incluyendo los detalles de la transacción usuales (fecha, hora, importe, etc) y la información de compra correspondiente (nombre del @grupo, número de oferta, etc). El emai enviado también incluye un link a un Recibo electrónico en @Bulkaria-site, el que puede ser impreso o descargado. El sistema también crea una Orden de Compra de Miembro (OCM) correspondiente a esta transacción.

Por cada pago recibido, el sistema incrementa el Contador de Productos del Grupo (CPG) de acuerdo al número de productos asociados al pago. El CPG representa el número total de productos pagos por los @miembros del @grupo. Una vez que el CPG es igual o superior al límite inferior de productos de la oferta (LIO), esto es, el menor número de productos para el cuál la oferta es válida, la OCM de cada @miembro que ha completado el pago es marcada como 'Lista para proceso'.  

Cuando el primer grupo de OCMs queda listo para ser procesado, una Orden de Compra de Grupo (OCG) es generada y puesta disponible online en @Bulkaria-site para el @oferente. El @oferente es informado de esta situación con un email incluyendo un link a la correspondiente OCG. Cada línea de la OCG se corresponde con una OCM. Después de alcanzarse o superarse el LIO, el sistema de @bulkaria-site continúa generando OCMs y actualizando la correspondiente OCG cada vez que se completa un pago, pero ahora las OCMs son generadas en estado 'Lista para proceso', esta condición permanecerá mientras no se supere el límite superior de oferta (LCO) 

Para permitir la entrega de los productos, @bulkaria-site genera un Voucher (&voucher) con un número único y un código de entrega único y lo envía al @miembro. El &voucher indica al @miembro que puede proceder a retirar / recibir los productos según lo establecido en la &oferta dentro del plazo establecido en el mismo (período de entrega).  

## Incorporación de nuevos Miembros

Una vez iniciado el proceso de Producción, los @usuarios de @bulkaria-site que no sean @miembros del @grupo quedan habilitados a unirse al proceso de compra, siempre y cuando la oferta esté todavía en estado 'Abierto' (&oferta-abierta). Las &ofertas-abiertas se comportan como &ofertas-fijas, esto es, están relacionadas con un producto específico con todas las condiciones de venta necesarias definidas, tales como el precio, la existencia disponible, alternativas de entrega, etc. Cuando un @usuario opta por una &oferta-abierta, se convierten en @miembros del @grupo por un proceso especial de &check-in, en el que proveen solamente la información necesaria para proceder con la compra.  En este caso, el pago es parte del proceso de &check-in.

## Compras adicionales

Un @miembro puede optar por el procedimiento descripto en el párrafo anterior  para volver a comprar, si ya hubiese completado la transacción comprometida en la etapa de Desarrollo. Esto puede hacerlo el número de veces que desee.

 

## Cierre de la Oferta

Una &oferta seleccionada por un @grupo como resultado de la etapa de Desarrollo es marcada como 'Abierta' (&oferta-abierta). Una &oferta-abierta puede aceptar pagos y, eventualmente, disparar la creación de una Orden de Compra de Grupo (OCG). Una &oferta adopta el estado 'Cerrado' (&oferta-cerrada) cuando exista al menos una de las siguientes condiciones.

* El Límite Superior de la Oferta (LSO) es alcanzado; esto es, el número total de productos en existencia dedicados a la &oferta ha sido ya asignado a los @miembros.

* La &oferta es cerrada por el @oferente. Esto puede ocurrir en cualquier momento para un número de productos que sea superior al número de productos asignado a los @miembros originales del grupo.

* La fecha tope de cierre de la &oferta (FTO) se cumple. Esta es la fecha que el @oferente ha indicado como tope para la validez de la &oferta. Notar que el @oferente puede extender esta fecha mientras la &oferta este abierta por única vez.

Si se alcanza la FTO y el número de productos asignados al @grupo no ha alcanzado el mínimo especificado por el @oferente para la &oferta (LIO), @bulkaria-site requiere al @oferente que opte entre aceptar el número de productos actualmente requeridos por el @grupo como un nuevo valor LIO o confirmar el LIO original. En el primer caso, el proceso continúa como se describió más arriba cuando el número de productos alcanza el valor LIO. En el segundo caso, todos los pagos realizados durante la sub-etapa de Consolidación asociados con la &oferta son reversados. Para este último caso el @grupo se cierra. 

 

## Entrega de Productos

Durante la entrega de los productos, el @miembro y el @oferente intercambian los productos y el &voucher correspondiente. Hecho esto, el @oferente ya puede ingresar el código de entrega del &voucher en la línea correspondiente de la OCG, la que automáticamente queda marcada como ‘entregada’. También se actualiza la OCM. Como verificación, @bulkaria-site informa al @miembro correspondiente de esta situación, a la vez que solicita la calificación del @oferente.. Las líneas de la OCG que estén marcadas como ‘entregadas’ pueden ser procesadas por el sistema de pago a @oferentes.

 

# Etapa de Cierre

### Situaciones de cierre

1. Se alcanza el LSO

2. El @oferente cierra la @oferta

3. Se alcanza la fecha tope de cierre de la @oferta

1. Se alcanzó el LIO

2. No se alcanzó el LIO

## Acciones de Cierre

1. El @grupo pasa a estado {cerrado}

2. El @grupo pierde visibilidad.

3. Se solicita calificación del proceso al @oferente

4. Se procesa el feedback de las calificaciones de @miembros y @oferentes

5. @bulkaria-site genera información estadística del ciclo de vida del @grupo

6. @bulkaria-site genera la información de calificación de @miembros y @oferentes

7. La información estadística queda disponible para

    1. @compradores

    2. @oferentes

    3. @usuarios

