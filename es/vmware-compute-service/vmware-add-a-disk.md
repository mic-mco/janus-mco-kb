---
title: "Cloud 360: Agregar un disco"
slug: cloud360-agregar-un-disco
---

## Acerca de esta tarea

Este artículo lo guiará a través del proceso de agregar un nuevo disco a una máquina virtual ya aprovisionada en un entorno (VDC) VMware. La interfaz de TIGO MCO proporciona un asistente para configurar y desplegar discos virtuales.

## Antes de comenzar

- Su entorno (VDC) TIGO Cloud 360 ya debe existir
- La máquina virtual a la que se requiere añadir un nuevo disco debe existir dentro del entorno (VDC).

## Procedimiento

1. Navegue hasta el entorno (VDC) deseado. Aparece la página **Máquinas virtuales**.

2. En el listado que se muestra ubique la máquina virtual a la que se le añadirá el nuevo disco y de clic en ella.

3. Aparece la página con los **Detalles** de la máquina virtual. De click en la opción **Discos duros** que se ubica en el menú de opciones a la izquierda de la página.

4. Aparece un listado con los discos que actualmente están asociados a la máquina virtual. Debe de aparecer el disco base (en el que está instalado el sistema operativo) y discos adicionales (en caso de que la máquina virtual cuente con ellos.).

5. De clic en el botón **Agregar disco** para iniciar el asistente de despliegue.

    1. Capture el tamaño del disco a crear, puede seleccionar unidades en GB o MB.

    2. En el campo **Tipo de bus** seleccione el valor Paravirtual (SCSI).

    3. Los valores a ingresar en los campos **Número de bus** y **Número de unidad** son unidades enteras entre 0 y 3. El disco base (donde está instalado el sistema operativo) utiliza el bus 0 y la unidad 0. Puede elegir cualquier otra combinación según sus requerimientos técnicos. Se recomienda seguir un orden, por ejemplo, para el primer disco adicional utilizar el bus 0 y la unidad 1, para el segundo disco adicional utilizar el bus 0 y la unidad 2, para el tercer disco utilizar el bus 0 y la unidad 3. En esta secuencia el cuarto disco ya utilizaría el bus 1 y la unidad 1 y continuar con esta lógica para mas discos.

6. Haga clic en el botón **Aplicar**.

7. El disco duro se aprovisionará en el virtualizador. Acciones adicionales dentro del sistema operativo son requeridas para que este nuevo disco pueda ser utilizado. Consulte la documentación de cada sistema operativo para obtener la lista de acciones a realizar.

## Resultados

- El disco adicional se aprovisiona y queda disponible para ser configurado a nivel sistema operativo.
- En la sección **Discos duros** se mostrará el nuevo disco.
