---
title: "Usar entornos para organizar cargas de trabajo"
slug: entornos-mco
---

### Resumen de entornos

La plataforma proporciona un mecanismo, el de **entornos**, para segregar cargas de trabajo y recursos, y para controlar quién tiene acceso a ellos. Los ejemplos de casos de uso de este concepto incluyen la creación de entornos distintos para aislar las cargas de trabajo de producción de los sistemas de desarrollo, o el establecimiento de aislamiento de procesos específicos del proyecto.

Un entorno pertenece a una organización y está asociado con un servicio específico (por ejemplo, a TIGO Cloud 360 como un centro de datos virtual o a AWS como una cuenta) y está compuesto por un conjunto de miembros que tienen visibilidad en un grupo de recursos compartidos, como instancias, almacenamiento, etc.

### Crear un ambiente

Usuario con un rol que tenga el permiso *Entornos: Crear*, puede agregar entornos adicionales y decidir quién puede tener acceso a él y bajo que modalidad. La siguiente es una lista de los pasos a seguir para crear un nuevo entorno (VDC) para TIGO Cloud 360.

1. Haz clic en *Agregar entorno* y aparecerá la página *Agregar entorno*.
1. Introduce un nombre y una descripción opcional para el entorno (VDC).
1. Si deseas permitir que los usuarios de otras organizaciones se agreguen como miembros, selecciona **Autorizar a miembros externos**.
1. Haz clic en *Siguiente* para iniciar el proceso de aprovisionamiento del entorno (VDC).
1. La página *Administrar miembros* aparecerá al finalizar el aprovisionamiento. Aquí puedes:
    - Seleccionar uno o más usuarios individuales de la lista
    - Buscar usuarios específicos
    - Agregar **todos los usuarios** en la organización (**membresía automática**)
    - Agregar ningunos usuarios al entorno (haz clic en *Omitir* para pasar a la página siguiente)
1. Para cualquier usuario que se haya agregado, es necesario seleccionar un rol de entorno. Si has activado la membresía automática, selecciona un rol de entorno predeterminado.
1. Haz clic en *Aplicar* para asginar los permisos a los miembros seleccionados.
