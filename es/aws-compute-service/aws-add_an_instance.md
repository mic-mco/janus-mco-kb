---
title: "AWS: Agregar una instancia"
slug: aws-agregar-una-instancia
---

## Acerca de esta tarea

Este artículo te guiará a través del proceso de agregar una nueva instancia a un entorno de AWS. La interfaz de TIGO MCO proporciona un asistente de varios pasos para seleccionar una configuración para la instancia (o instancias) y esta se creará después del paso final del asistente.

## Antes de comenzar

- Debes tener una VPC configurada
- La VPC debe tener una subred configurada
- La subred debe tener al menos una dirección IP disponible
- El número de instancias que se deben implementar inicialmente
- El número máximo de instancias para permitir cuando se escala automáticamente

## Procedimiento

1. Navega hasta el entorno deseado (cuenta AWS) para mostrar la página **Instancias**.

2. Haz clic en el botón **Agregar instancia** para iniciar el asistente **Agregar instancia**.

3. Configura los ajustes básicos para la instancia.

     - Introduce un nombre en el campo **Nombre** o acepta el predeterminado.

     - Selecciona la región donde se implementará la instancia.

     - Selecciona la imagen que se usará para implementar la instancia.

     - Selecciona el tipo de instancia deseado en el menú emergente **Tipo de instancia**.

     - Selecciona el número mínimo y máximo deseado de instancias para implementar.

     Haz clic en **Siguiente** para continuar.

4. Configura los ajustes de seguridad para la instancia.

     - Introduce un nombre para el nuevo par de claves SSH en el campo **Nombre de la clave** o acepta el valor predeterminado.

     - Define un nuevo grupo de seguridad para la instancia o selecciona un conjunto predefinido.

     Haz clic en **Siguiente** para continuar.

5. Configura los ajustes de red para la instancia.

     - En el menú emergente **VPC**, selecciona la VPC donde se creará la instancia.

     - En el menú emergente **Subred**, selecciona la subred donde se creará la instancia.

     Haz clic en **Siguiente** para continuar.

6. Configura los ajustes de almacenamiento para la instancia.

     En la página **Configuración del almacenamiento**, puedes elegir la configuración para el volumen raíz de la nueva instancia.

     - Ingresa el nombre del dispositivo deseado para el volumen en el campo **Nombre del dispositivo**, o acepta el valor predeterminado.

     - Selecciona el tipo de rendimiento de volumen en el menú emergente **Tipo de volumen**.

     - Introduce el tamaño del volumen en gigabytes \(GB\) en el campo **Tamaño**.

     - Si es necesario, selecciona la casilla de verificación **Eliminar en el momento de terminar**.

     En este paso, puedes agregar varios volúmenes con el botón **Añadir**. Al presionar este botón, aparecerá una sección de configuración de volumenes adicionales. Introduce los parámetros deseados en consecuencia. Al agregar varios volúmenes, el nombre del dispositivo debe ser único para cada volumen. Haz clic en el botón **Eliminar** para eliminar ese volumen de la lista.

     Haz clic en **Siguiente** para continuar.

7. Selecciona los volúmenes existentes para adjuntar.

     En la página **Adjuntar volúmenes existentes**, puedes adjuntar volúmenes que ya existen dentro de la zona de disponibilidad de la instancia que se creará.

     Se pueden adjuntar varios volúmenes a la nueva instancia haciendo clic en el botón **Añadir**. Asegúrate de que cada volumen tenga un nombre de dispositivo único.

     - Selecciona el volumen que deseas adjuntar en el menú emergente **Volúmenes**.

     - Ingresa el nombre del dispositivo deseado en el campo **Nombre del dispositivo**.

     Al hacer clic en el botón **Eliminar**, se elimina ese volumen de la lista.

8. Haz clic en el botón **Aplicar**.

     La pantalla del asistente se cerrará y volverá a la pantalla **Instancias** de la pestaña **Cómputo**. La instancia puede tardar varios minutos en agregarse. Durante este tiempo, el panel de notificaciones indicará que se está creando la instancia.

9. Guarda la clave SSH privada proporcionada en la notificación.

     - Haz clic en el icono **campana** para extender el panel de notificaciones.

     - Identifica la notificación para tu instancia buscando el nombre de la instancia.

     - Haz clic en el icono **Portapapeles** para copiar la clave SSH privada completa en tu portapapeles.

     - Guarda la clave SSH privada de forma segura.

## Resultados

- La instancia se crea con las opciones de configuración seleccionadas
- El número de instancias creadas es el valor proporcionado en el campo **Número mínimo de instancias**
- La instancia se creará en la zona de disponibilidad de la subred seleccionada
- Todos los volúmenes nuevos que se definieron se adjuntarán a la nueva instancia
- Todos los volúmenes existentes que se especificaron al asistente se adjuntarán a la nueva instancia
- La instancia ahora aparece en la página **Instancias** de la pestaña **Cómputo**
- La clave SSH privada necesaria para iniciar sesión en la instancia se ha almacenado de forma segura
