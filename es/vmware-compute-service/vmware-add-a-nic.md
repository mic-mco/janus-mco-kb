---
title: "Cloud 360: Agregar una interfaz de red"
slug: cloud360-agregar-una-nic
---

## Acerca de esta tarea

Este artículo lo guiará a través del proceso de agregar una nueva interfaz de red a una máquina virtual ya aprovisionada en un entorno (VDC) VMware. La interfaz de TIGO MCO proporciona un asistente para configurar y desplegar nuevas interfaces de red.

## Antes de comenzar

- Su entorno (VDC) TIGO Cloud 360 ya debe existir
- La máquina virtual a la que se requiere añadir la nueva interfaz de red debe existir dentro del entorno (VDC).

## Procedimiento

1. Navegue hasta el entorno (VDC) deseado. Aparece la página **Máquinas virtuales**.

2. En el listado que se muestra ubique la máquina virtual a la que se le añadirá la interfaz de red y de clic en ella.

3. Aparece la página con los **Detalles** de la máquina virtual. De click en la opción **Controladores de interfaz de red** que se ubica en el menú de opciones a la izquierda de la página.

4. Aparece un listado con las interfaces de red que actualmente están asociadas a la máquina virtual. Pudiera no existir ninguna interfaz de red asociada a la máquina virtual lo cual implicaría que la máquina estaría aislada del resto de máquinas dentro del entorno (VDC) e inclusive de conectividad externa (Internet, MPLS)

5. De clic en el botón **Agregar NIC** para iniciar el asistente de despliegue.

    1. En el campo **Red** se listarán todas las redes disponibles dentro del entorno (VDC). Seleccione aquella red que se quiere asociar con la nueva interfaz de red.

    2. Seleccione la casilla **Principal** solo en el caso de que desee establecer la nueva interfaz de red como la principal para la máquina virtual.

    3. En caso de que quiera asociar la nueva interfaz de red con una red distinta a las que están disponibles, debe primero crear la nueva red. Consulte el artículo [Cloud 360: Agregar una red](vmware-add-a-network.md) para obtener más detalles de como crar una nueva red.

6. Haga clic en el botón **Aplicar**.

7. La nueva interfaz de red se aprovisionará en el virtualizador. Acciones adicionales dentro del sistema operativo son requeridas para que esta nueva interfaz pueda ser utilizada. Consulte la documentación de cada sistema operativo para obtener la lista de acciones a realizar.

## Resultados

- La interfaz de red se aprovisiona y queda disponible para ser configurada a nivel sistema operativo.
- En la sección **Controladores de interfaz de red** se mostrará la nueva interfaz de red.
