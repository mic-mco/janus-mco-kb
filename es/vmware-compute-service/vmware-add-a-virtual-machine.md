---
title: "Cloud 360: Agregar una máquina virtual"
slug: cloud360-agregar-maquina-virtual
---

## Acerca de esta tarea

Este artículo te guiará a través del proceso de agregar una nueva máquina virtual a un entorno (VDC) TIGO Cloud 360.

## Antes de comenzar

- Debe de existir una red previamente aprovisionada en su entorno (VDC) TIGO Cloud 360.

## Procedimiento

1. Navegue hasta el entorno (VDC) deseado. Al hacerlo, aparecerá la página **Máquinas virtuales**.

2. Haga clic en el botón **Agregar máquina virtual** para iniciar el asistente **Agregar máquina virtual**.

3. Ingrese un nombre para la nueva máquina virtual en el campo **Nombre** o acepte el valor predeterminado.

4. Para que la máquina virtual se encienda automáticamente en el momento de la creación, marque la casilla de verificación **Encender**.

5. Si desea que la máquina virtual forme parte de una aplicación virtual existente, seleccione la aplicación deseada en el menú emergente **Aplicación virtual**.

6. Seleccione del menú emergente **Red** a qué red desea conectar la nueva máquina virtual o acepte la opción predeterminada.

7. Seleccione de entre un conjunto de plantillas con varios sistemas operativos y versiones ya instaladas la opción requerida. Además, seleccione los tamaños de memoria y vCPU predeterminados disponibles dentro de la opción **Política de dimensionamiento de máquinas virtuales**.

8. Haga clic en el botón **Aplicar** para crear la nueva máquina virtual.

## Resultados

- La máquina virtual se crea utilizando la configuración especificada
- Si se seleccionó **Encender**, el sistema inicia la máquina virtual inmediatamente después de crearla
- La máquina virtual aparece en la pantalla **Máquinas virtuales**

**Importante:** Debes almacenar de forma segura la contraseña de acceso como administrador. No se almacenará en ningún lugar de la interfaz de usuario de TIGO MCO y no se podrá recuperar una vez que se borre la notificación del panel. No se puede iniciar sesión en el sistema operativo de la máquina virtual sin esta clave. Si se pierde, deberás seguir un procedimiento de recuperación, que requiere puede implicar el reinicio de la máquina virtual.
