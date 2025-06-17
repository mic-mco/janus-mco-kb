---
title: "AWS: Agregar un volumen"
slug: aws-agregar-un-volumen
---

## Acerca de esta tarea

Este artículo lo guiará a través del proceso de agregar un nuevo volumen a un entorno (cuenta) de AWS.

## Antes de comenzar

- Tu entorno (cuenta) de AWS ya debe existir

## Procedimiento

1. Navega hasta el entorno (cuenta) deseado. Aparecerá la página **Instancias**.

2. Haz clic en el elemento **Volúmenes** y aparecerá una lista de volúmenes en este entorno (cuenta).

3. Haz clic en el botón **Agregar volumen** para iniciar el asistente **Agregar volumen**.

4. Configura el nuevo volumen:

     - Introduce un nombre en el campo **Nombre** o acepta el predeterminado.

     - Selecciona el tipo de volumen para crear.

     - Ingresa la cantidad de gigabytes para asignar para el nuevo volumen en el cuadro de texto **Tamaño**. El volumen debe ser un número entero.

     - Especifica la zona de disponibilidad en la cual se creará el nuevo volumen

          La zona de disponibilidad seleccionada definirá las instancias a las cuales el nuevo volumen será asociable.

5. \(Opcional\) Puedes adjuntar automáticamente el nuevo volumen a una instancia existente:

     - Haz clic en **Adjuntar volumen a instancia existente**.

     - Aparecerá una lista de instancias en la zona de disponibilidad seleccionada. Selecciona la instancia deseada.

     - Ingresa el nombre del dispositivo deseado en el cuadro de texto etiquetado como **Nombre del dispositivo**.

6. Haz clic en el botón **Aplicar**.

## Resultados

- El volumen del tamaño especificado se crea en el entorno activo
- Existe en la zona de disponibilidad seleccionada
- Si se seleccionó una instancia, el volumen se adjunta automáticamente a esa instancia
- El volumen aparece en la pantalla **Volúmenes** de la pestaña **Cómputo**
