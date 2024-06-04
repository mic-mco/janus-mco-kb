---
title: "Generar una clave API de TIGO MCO"
slug: clave-api-cloudmc
---

Cuando trabajas con la API de TIGO MCO, deberás generar una clave de API para usar con tu código. Las claves API brindan un método conveniente para que tu aplicación se identifique ante un servicio cuando realiza llamadas a la API del servicio.

Cualquier usuario de TIGO MCO puede generar una clave API. Las claves API de un usuario tendrán el mismo nivel de privilegio que tiene el usuario. No hay límite para la cantidad de claves API que un usuario puede generar. Se recomienda aprovechar esto generando una clave API para cada aplicación que accederá al sistema.

Para administrar tus claves de API, navega hasta el menú de usuario en la parte superior derecha de la página, haz clic en el elemento etiquetado como *Credenciales de API*.

### Enumerar endpoints y claves de API existentes

![Pantalla de credenciales de API](/assets/cloudmc-api-key-es-01.png)

La pantalla *Credenciales de API* enumera todas las claves existentes mostrando el nombre de cada clave, la última IP y última fecha en que se usó. Si esta clave nunca ha sido utilizada, los campos de IP y actividad no tendrán ningún valor.

Para cambiar el nombre de una clave, haz clic en el icono etiquetado *Editar clave API* en el extremo derecho de la entrada deseada.

El endpoint para realizar llamadas API al sistema se muestra en la parte superior de la lista de claves. Haz clic en el icono del portapapeles para copiar la URL.

### Generar una nueva clave API

![Clave API generada](/assets/cloudmc-api-key-es-02.png)

1. En la pantalla *Credenciales de API*, haz clic en el botón etiquetado como *Generar clave de API*.
1. Introduce un nombre para la nueva clave en el campo de texto **Nombre**. Es posible que deseas dar a la clave un nombre que refleje la aplicación para la que se utilizará. Haz clic en *Generar*.
1. Volverás a la pantalla *Credenciales de API*. Aparecerá una notificación con la nueva clave API oculta.
    - **Debes recuperar** la nueva clave de esta notificación. Una vez que se descarta la notificación, no hay forma de volver a mostrar la clave API.
    - Haz clic en el icono de develar (forma de ojo) para que la clave API sea visible.
    - Haz clic en el icono del portapapeles para copiar la clave API.
1. La clave API ahora está lista para usar. Guarda la información en un lugar seguro.

### Revocar una clave API

1. En la pantalla *Credenciales de API*, haz clic en el icono etiquetado como *Eliminar clave de API* en el extremo derecho de la entrada deseada.
1. Aparecerá un cuadro de diálogo de confirmación. Haz clic en *Eliminar* para confirmar la acción.
1. La clave API se revocará inmediatamente y ya no será válida para su uso.
