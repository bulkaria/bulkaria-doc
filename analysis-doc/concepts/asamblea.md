Asamblea (versión 1.0)
======

### Definition
La asamblea es una herramienta para la toma de decisiones grupales. 

#### Description
La asamblea funciona como un espacio virtual acotado en el tiempo donde los miembros de un grupo pueden reunirse para tomar decisiones sobre una agenda previamente definida utilizando la facultad de voto.

Una asamblea debe incluir la invitación a todos los miembros del grupo sin discriminar la clase de objetivo en cual estén trabajando. 

##### Llamado a asamblea
El llamado a una asamblea puede ser iniciado por cualquier miembro del grupo (de ahora en más originador), pero deberá tener la adhesión de 6 (seis) miembros más (de ahora en más precursores) para que bulkaria la publique.

Los atributos de un llamado a asamblea son:
* Tipo de asamblea: las asambleas podrán ser de dos tipos, *tradicional* o *extendida*. La asamblea tradicional será desarrollada en línea y solo podrán intervenir los miembros que hayan ingresado luego de la tolerancia para quorum automático (ver más bajao). La asamblea extendida funcionará como un foro de Q&A, podrá durar días y no precisará de simultaneidad en la concurrencia.
* Agenda: compuesta por temas a tratar con un orden y duración sugerida. El originador debe indicar al menos un tema inicial.
* Fecha y hora de inicio
* Tolerancia para quorum automático (solo tradicional): tiempo que se esperará por el ingreso de al menos 7 (siete) miembros del grupo a la asamblea. De no llegarse a este número en el tiempo estipulado la asamblea se cancelará.
* Duración de la asamblea: en la asamblea tradicional se establecerá en horas (tiempo que no podrá ser menor a la suma de los tiempos asignados a cada tema más la tolerancia para quorum automático), en la extendida en días corridos.
* Tiempo máximo de ponencias (solo tradicional): será el tiempo máximo que cada miembro podrá tomar para establecer su opinión sobre un tema.
* Reglas de la asamblea: lista de reglas que deberá cumplirse durante la asamblea. Podrán adoptarse de una plantilla propuesta por Bulkaria con modificaciones o agregados del originador y/o de los miembros precursores.

Los seis miembros precursores deben ser invitados específicamente por el miembro originador, pudiendo cursar seis o más invitaciones para asegurarse la publicación.

A medida que cada miembro precursor acepta la invitación podrá agregar más temas a la agenda y/o marcar su disconformidad con los temas preexistentes. También deberá sugerir una fecha y hora de inicio o adherir a una preexistentes. A su vez podrá agregar nuevas reglas y/o marcar su disconformidad con las existentes.

Cuando se hayan registrado todo los precursores, la agenda queda firme, eliminándose aquellos temas que tengan más de 3 disconformidades. La fecha y hora de inicio será aquella que más adhesiones haya logrado y en caso de empates bukaria seleccionará la primera registrada de las más votadas. Las reglas quedarán firmes eliminándose aquellas que tengan más de tres disconformidades. Si una asamblea no ha logrado las 6 adhesiones antes de la fecha de inicio seleccionada hasta ese momento se cancelará. 

##### Agenda
Como se dijo anteriormente una agenda esta compuesta por temas. Estos temas serán libres pero deberán tener un resolución tipificada según los tipos siguientes:

1. De resolución binaria: deberán votarse por si o por no
2. De resolución cuantitativa: deberán votarse con un valor numérico adecuado a una unidad predefinida
4. De resolución temporal: deberán votarse con una fecha (y hora de indicarse)
5. De resolución cualitativa: deberán votarse alguna de las opciones predefinidas
5. De resolución operativa: son tipos especiales que provee bulkaria para modificar estados del grupo

##### Publicación del llamado a asamblea
Bulkaria publicará en el muro del grupo y enviará un correo a cada miembro del mismo el llamado a toda asamblea que haya quedado firme con la adhesión de seis precursores más el originador.

Bulkaria podrá apuntar una cita en la agenda personal de cada miembros que haya configurado esta opción en su perfil (solo para tradicional).

##### Inicio de asamblea
En la fecha y hora definida Bulkaria habilitará un room virtual donde los miembros deberán ingresar para participar de la asamblea.

En el caso de una asamblea tradinional, esta se iniciará si:
1. Antes de la tolerancia de quorum automática todos los miembros del grupo han ingresado
1. Si superada la tolerancia de quorum automática, la cantidad de miembros ingresados es igual o mayor a 7 (siete)

##### Dashboard de asamblea
El dashboard de asamblea es un conjunto de utilidades que permiten el desenvolvimiento armónico de la misma. Estas utilidades son:

1. Moderación: En el caso de una asamblea tradicional, a medida que los miembros van ingresando al room deben votar por un miembro moderador entre los ingresados al momento, contemplándose el voto a si mismo. Una vez iniciada la asamblea el moderador será aquel con mayor cantidad de votos y en caso de empate el que haya ingresado primero. En el caso de una asamblea extendida el moderador será el originador.
La función del moderador será la de controlar que ningún miembro trasgreda las reglas de la asamblea. Su herramienta de acción son la posibilidad de silenciar la ponencia o banear un miembro de la asamblea. El moderador podrá ceder su posición en beneficio de otro miembro que él decida.
1. Ponencias: en una asamblea tradicional los miembros podrán solicitar la palabra para establecer la posición sobre un tema. Esto lo harán por medio de un botón dispuesto a tal fin. La ponencia podrá durar lo que se haya establecido en _Tiempo máximo de ponencias_. Los turnos los asignará bulkaria según el orden en que se haya solicitado la palabra. Cada ponencia podrá ser calificada por los miembros con +1 o -1. Podrá haber ponencias mientras reste algo del tiempo asignado al tema.
1. Discusión: en una asamblea extendida cada tema se discute con un hilo de funcionamiento similar a *stackexchange*
1. Votación: los miembros deberán votar el tema de acuerdo al tipo de resolución con que se lo haya configurado.

##### Fin de asamblea
Los miembros podrán abandonar la asamblea antes que finalice.

La asamblea se finaliza cuando queden menos de 7 (siete) miembros o se hayan completado todos los temas de la misma o, solo en el caso de la asamblea extendida, cuando llegue a la duración estipulada.

Los temas resueltos, es decir los que hayan sido votados según el tipo de resolución, serán publicados en el wall del grupo como resoluciones de asamblea.

##### Poder de voto
Todos los miembros de una asamblea tiene igual poder de voto, pero alguno puede ejercer el voto por tercero si posee un mandato del tercero que lo habilite. Este mandato se obtiene por medio de un token que el tercero solicita a bulkaria y transfiere al miembro que lo representará haciendo que su voto valga tanto como mandatos tenga. 
