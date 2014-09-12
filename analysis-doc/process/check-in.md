Check-in
======

### Definition
Se denomina check-in a la acción que deben realizar los [usuarios](../actors/usuario.md) para convertirse en [miembros](../actors/miembro.md) de un [grupo](../actors/grupo.md).

El miembro que crea el [grupo](../actors/grupo.md) se denomina **fundador**

#### Description
El futuro [miembro](../actors/miembro.md) recibe un correo con un link para realizar el check-in, este correo podrá ser enviado por:

* el fundador en la etapa de [gestación](../concepts/gestacion.md) del grupo 
* cualquier [miembro](../actors/miembro.md) del grupo en cualquier etapa
* un miembro alumno a sus padres

El proceso de check-in diferencia entre un usuario invitado como miembro alumno y un usuario invitado como miembro padre, esto lo realiza a través del tipo de invitación, es decir, las invitaciones deberán indicar si se trata de una invitación a un compañero o a un padre.

Bulkaria guarda un registro de las invitaciones con la siguiente estructura:

* miembro remitente
* correo de destino
* tipo de invitacion que podrá ser: invitación a alumno, invitación a padre, en este ultimo caso, un miembro solo podrá cursar dos invitaciones de este tipo

Una invitación a padre no podrá ser realizada en la etapa de gestación.

El flujo del proceso es el siguiente:

1. Si la persona no es usuario de Bulkaria, es derivado a la función de registración ([sign-in](../process/sign-in.md)]
1. El usuario registrado debe completar los siguientes datos
    * Curso al que pertenece
    * Confirmar o corregir datos personales (Nombre, documento, etc.)
1. El nuevo miembro opcionalmente podrá configurar su [perfil de grupo](../concepts/perfil-de-grupo.md).
1. Se envía notificación a los miembros del grupo subscriptos a este tipo de alerta.
1. Si el grupo se encuentra en estado de [gestación](../concepts/gestacion.md), controla si debe pasar al siguiente estado ([incubación](../concepts/incubacion.md))

#### Attributes
* [curso](../entities/curso.md): Curso al que pertenece el alumno o padre, por defecto es el curso del miembro fundador.
* Número y tipo de documento
* Fecha de nacimiento
* Domicilio completo
* Teléfono

### Processes related to this concept
* [Sign-in](../process/sign-in.md)
* [Creación o actualización de perfil de grupo](../process/crud-perfil-de-grupo.md)
* [Creación de grupo](../process/creacion-de-grupo.md)

### Relationships with other concepts
* {TODO}

### Preconditions
* El miembro debe ser un usuario registrado de Bulkaria

### Examples 

Provide some concrete examples whenever possible
* {TODO}
