Check-in
======

### Definition
Se denomina check-in a la acción que deben realizar los [usuarios](../actors/usuario.md) para convertirse en [miembros](../actors/miembro.md) de un [grupo](../actors/grupo.md).

#### Description
El futuro [miembro](../actors/miembro.md) recibe un correo con un link para realizar el check-in, este correo es enviado por el fundador en la etapa de gestación del grupo o por cualquier [miembro](../actors/miembro.md) del grupo en cualquier etapa.

El miembro que crea el [grupo](../actors/grupo.md) se denomina **fundador**

En flujo del proceso el siguiente:

1. Si la persona no es usuario de Bulkaria, es derivado al la función de registración ([sign-in](../process/sign-in.md)]
1. El usuario registrado debe completar los siguientes datos
    * Curso al que pertenece
    * Confirmar o corregir datos personales (Nombre, documento, etc.)
1. El nuevo miembro opcionalmente configura su [perfil de grupo](../concepts/perfil-de-grupo.md).
1. Se envía notificación a los miembros del grupo subscriptos a este tipo de alerta.
1. Si el grupo se encuentra en estado de [incubación](../concepts/incubacion.md), controla si debe pasar al siguiente estado ([gestación](../concepts/gestacion.md))

#### Attributes
* [curso](../entities/curso.md): Curso al que pertenece el alumno, por defecto es el curso del miembro fundador.
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
