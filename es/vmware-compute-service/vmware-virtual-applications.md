---
title: "Cloud 360: Aplicaciones virtuales"
slug: cloud360-vapps
---

Una aplicación virtual es un contenedor de máquinas virtuales que proporciona la infraestructura para una aplicación nativa de la nube. Este artículo analiza el concepto de aplicaciones virtuales y cómo se administran en TIGO MCO.

Las aplicaciones virtuales se enumeran en la sección **Aplicaciones virtuales** del entorno (VDC) TIGO Cloud 360 seleccionado.

## Descripción detallada

Una aplicación virtual sirve como contenedor para gestionar y ejecutar una aplicación como una sola entidad. Está compuesta por máquinas virtuales que se han creado como parte de esa aplicación virtual, ya sea desde la página **Aplicaciones virtuales** o desde el asistente **Agregar máquina virtual**.

Se crea una aplicación virtual con su propia red, lo que permite que las máquinas virtuales de la aplicación se comuniquen entre sí. La red de una aplicación virtual puede estar aislada o con enrutamiento. Se destruye automáticamente cuando se elimina la aplicación virtual.

## Estados de aplicaciones virtuales

- **Encendida**

     Todas las máquinas virtuales asignadas a esta aplicación virtual están encendidas.

- **Parcialmente apagada**

     Durante el proceso de inicio normal, una aplicación virtual entrará brevemente en este estado.

- **Parcialmente funcionando**

     Una o más máquinas virtuales asignadas a esta aplicación virtual están suspendidas o apagadas.

## Lista de aplicaciones virtuales

Las aplicaciones virtuales se enumeran en la sección **Aplicaciones virtuales** del entorno (VDC) TIGO Cloud 360 seleccionado.

![Una captura de pantalla de la página de aplicaciones virtuales de TIGO Cloud 360, con puntos numerados que indican características de interés](/assets/vmware-vapps-list-es.png)

1. **Lista de aplicaciones virtuales**

     En esta área, aparece una lista de todas las aplicaciones virtuales en el entorno (VDC) seleccionado.

2. **Cuadro de búsqueda**

     Escriba en el cuadro de búsqueda para filtrar la lista de aplicaciones virtuales. El sistema buscará en el campo de nombre, así como en el UUID interno, y devolverá cualquier aplicación virtual que coincida con la cadena en el cuadro de búsqueda.

3. **Agregar aplicación virtual**

     Al hacer clic en este botón se abrirá el asistente **Agregar aplicación virtual**.

4. **Entrada de aplicación virtual**

     Cada entrada incluye el nombre de la aplicación virtual, su estado, la cantidad total de vCPU, memoria y almacenamiento aprovisionados entre todas las máquinas virtuales de la aplicación virtual y un recuento de todas las máquinas virtuales en la aplicación. Haga clic en una entrada para navegar a una página con detalles de configuración y una lista de todas las operaciones para esa aplicación virtual individual.

5. **Menú de acciones ocultas**

     Cada entrada en la lista de aplicaciones virtuales tiene un menú de acciones ocultas. Haga clic en el menú acciones ocultas para acceder a una lista de operaciones utilizadas con frecuencia para la aplicación virtual.
