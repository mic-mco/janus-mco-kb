---
title: "Cloud 360: Máquinas virtuales"
slug: cloud360-mvs
---

Las máquinas virtuales son un el componente fundamental de infraestructura proporcionada por TIGO Cloud 360. Este artículo analiza el concepto de máquinas virtuales y cómo se administran en TIGO MCO.

Las máquinas virtuales se enumeran en la sección **Máquinas virtuales** del entorno (VDC) TIGO Cloud 360 seleccionado.

## Descripción detallada

Al igual que en otras plataformas en la nube, una máquina virtual es una abstracción de una computadora física, que ejecuta un sistema operativo completo y proporciona dispositivos virtualizados tales como almacenamiento (discos), interfaces de red y firewalls. Una vez que se aprovisiona una máquina virtual, se puede utilizar para ejecutar los distintos componentes de sus aplicaciones.

Una máquina virtual se basa en una imagen predefinida, llamada plantilla. TIGO Cloud 360 ofrece múltiples ofertas predefinidas de vCPU y memoria.

Cada máquina virtual se crea con un disco duro ya conectado. El tamaño de este disco está determinado por la plantilla seleccionada en el momento de la configuración. Se puede crear almacenamiento adicional y adjuntarlo a una máquina virtual, según sea necesario.

Al implementar una nueva máquina virtual, debe hacerse dentro de una red existente. Si no hay ninguna red en el entorno (VDC) activo, no se le permitirá agregar una nueva máquina virtual.

## Estados de máquinas virtuales

Las máquinas virtuales tienen tres estados de poder principales:

- **Encendida**

     La máquina virtual está en funcionamiento y puede ejecutar su sistema operativo y otros procesos. En este estado, la consola web o la consola remota están disponibles.

- **Apagada**

     La máquina virtual está parada y no se está ejecutando ningún proceso.

- **Suspendida**

     Es factible detener la ejecución de una máquina virtual en el estado encendido y guardar toda la memoria actual en el disco. Una máquina virtual que ha sido suspendida puede regresar al estado encendido y reanudar la ejecución desde el punto en el que se suspendió.

Una máquina virtual también puede pasar por los siguientes subestados:

- **Estado inconsistente**

     Una máquina virtual en este estado se modificó directamente en el virtualizador y no mediante TIGO MCO por lo que es requerida una sinronización. Apague la máquina virtual y luego vuelva a encenderla para devolverla a su estado normal.

- **Iniciando**

     Las máquina virtuales pasan por este subestado durante su creación.

- **Apagando**

     Subestado temporal que sucede solo durante el apagado de la máquina virtual.

- **Eliminación**

     Subestado temporal que sucede solo durante el proceso de borrado de la máquina virtual.

- **Desconocido**

     Subestado temporal que sucede solo durante el proceso de borrado de la máquina virtual.

## Lista de máquinas virtuales

Las máquinas virtuales se enumeran en la sección **Máquinas virtuales** del entorno (VDC) TIGO Cloud 360 seleccionado.

![Una captura de pantalla de la página de máquinas virtuales en TIGO Cloud 360, con puntos numerados que indican características de interés](/assets/vmware-vms-list-es.png)

1. **Lista de máquinas virtuales**

     Aquí, en esta área, aparece una lista de todas las máquinas virtuales en el entorno (VDC) seleccionado.

2. **Cuadro de búsqueda**

     Escriba en el cuadro de búsqueda texto para filtrar la lista de máquinas virtuales. El sistema buscará en el campo Nombre, así como en el UUID interno, y devolverá cualquier máquina virtual que coincida con la cadena en el cuadro de búsqueda.

3. **Agregar máquina virtual**

     Al hacer clic en este botón se abrirá el asistente **Agregar máquina virtual**.

4. **Entrada de máquinas virtuales**

     Cada entrada incluye el nombre de la máquina virtual, su estado actual, la cantidad de vCPU y memoria aprovisionada para esta máquina virtual, el nombre de la plantilla que se utilizó para crearla y, si la máquina virtual se asignó a una aplicación virtual, su nombre también aparecerá aquí. Haga clic en una entrada para navegar a una página con detalles de configuración y una lista de todas las operaciones para esa máquina virtual individual.

5. **Menú de acciones**

     Cada entrada en la lista de máquinas virtuales tiene un menú de acciones. Haga clic en el ícono (3 puntos) para acceder a una lista de operaciones frecuentes utilizadas para gestionar la máquina virtual.
