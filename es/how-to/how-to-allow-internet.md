---
title: "Permitir salida a Internet en Tigo Cloud 360"
slug: salida-internet-cloud360
---

Los entornos (VDC) de TIGO Cloud 360 cuentan con capacidad de establcer conexion desde y hacía Internet. El presente artículo te guiará en la forma mas simple de otorgar salida a Internet a todas las máquinas virtuales que compartan una misma red o solo a una máquina virtual.

### Pasos inciales

Navegue hasta el entorno (VDC) deseado donde aparecerá la sección **Máquinas virtuales**. Seleccione la opción **Redes** y, posteriormente, la opción **Puerta de enlace EDGE**. Se mostrarán todos los dispositivos EDGE disponibles para el entorno (VDC) actual. En la mayoría de los casos, solo existirá un dispositivo EDGE.

Será dentro del dispositivo EDGE donde se realizarán todas las configuraciones necesarias para permitir la salida a Internet.

### Crear regla NAT

![Pantalla de credenciales de API](/assets/cloudmc-api-key-es-01.png)

De clic en el ícono de engrane para la sección **Reglas NAT** en el dispositivo EDGE. Al hacerlo, se mostrará el listado de las reglas de NAT actualmente configuradas. Es posible que el listado aparezca vacío si es la primera regla NAT que se genera o bien, si se realizó una eliminación completa de reglas.

De clic en el botón **Agregar una regla NAT** ubicado en la parte derecha de la página, esta acción iniciará el asistente de configuración de nuevas reglas.

Ingrese un nombre descriptivo para este regla. En el campo **Tipo** seleccione la opción SNAT.
De forma automática, el sistema asignará la IP Pública del EDGE en el campo **IP externas**. No haga cambios en este valor.
En el campo **IP internas** podrá especificar una IP puntual o un rango de IPs. Esta IP o rangos de IPs son las que tendrán salida a Internet mediante esta regla.

Asumamos que en su entorno se encuentra configurada la red 192.168.12.1/25 y que una de las máquinas virtuales aprovisionada tiene asignada la IP 192.168.12.10. Si desea otorgar salida a Internet a cualquier máquina virtual (actualmente aprovisionada o que se aprovisione a futuro) que tenga una interfaz en esta red, deberá entonces capturar 192.168.12.1/25 como valor en el campo **IP internas**. Si solo desea permitir la salida a Internet a una máquina virtual en particular, deberá capturar como valor la IP espécifica. En nuestro caso de ejemplo, el valor a capturar sería 192.168.12.10/32.

De clic en **Aplicar** para crear la regla NAT.

### Crear conjunto de IP

Un conjunto IP es un grupo de direcciones IP que pueden utilizarse como orígenes y destinos en las reglas de firewall. Un conjunto IP puede contener una combinación de direcciones IP individuales, rangos IP y subredes.

Navegue de regreso a la pantalla de configuración del dispositivo EDGE. De clic en el ícono de engrane para la sección **Conjutos de IP**. Al hacerlo, se mostrará el listado de los conjutos de IPs actualmente configurados. Es posible que el listado aparezca vacío si es el primer conjunto que se genera o bien, si se realizó una eliminación completa de conjuntos.

De clic en botón **Agregar un conjunto de IP** ubicado en la parte derecha de la página, esta acción iniciará el asistente de configuración de nuevos conjuntos.

Ingrese un nombre descriptivo para este conjunto y, opcionalmente, una descripción detallada. Si pretende otorgar la salida a Internet a todo un segmento de red, puede optar por seleccionar el valor Red CIDR del campo **Tipo** y seleccionar la red en cuestión del campo desplegable **Red CIDR**. Si pretende otorgar la salida a Internet solo a una máquina virtual, puede optar por seleccionar el valor Manual del campo **Tipo** y en el campo **Direcciones IP** ingresar la IP de la máquina virtual, en nuestro ejemplo el valor a asignar sería 192.168.12.10/32.

De clic en **Aplicar** para crear el conjuto de IP.

### Crear regla de Firewall

Navegue de regreso a la pantalla de configuración del dispositivo EDGE. De clic en el ícono de engrane para la sección **Reglas de firewall**. Al hacerlo, se mostrará el listado de las reglas de firewall actualmente configuradas. Este listado contendrá, por lo menos, la regla por defecto la cual es un drop desde *ANY* y hacia *ANY*. Esta regla no se puede eliminar, ya que es una medida de protección para descartar todo el tráfico que no tenga una regla que lo permita.

De clic en botón **Agregar regla de cortafuegos** ubicado en la parte derecha de la página, esta acción iniciará el asistente de configuración de nuevas reglas de firewall.

Ingrese un nombre descriptivo para este regla. Asegurese de que la casilla **Activada** esté seleccionada. En el campo **Prioridad** seleccione el valor Encima. Tenga en cuenta que la prioridad que se le asigne a una regla influye directamente en el resultado. Si la regla de firewall que permite comunicación está debajo de una regla que no permite esa misma comunicación, entonces la comunicació no se establecerá.

En el campo **Fuente** seleccione el nombre del conjunto de IP recién creado y, en el campo destino, seleccione el valor Cualquier. El campo acción debe de tener como valor Permitir. En nuestro ejemplo estamos trabajando con IPv4, por lo tanto, dicho valor debe estar seleccionado el campo **Protocolo IP**.

De clic en **Aplicar** para crear la regla de firewall.

Desde el sistema operativo de una máquina virtual dentro del segmento de red asociado a la regal NAT y al conjunto de IP, confirme la conectividad a Internet utilizando el navegador Web o un comando ping a una IP de un servidor en Internet o con cualquier otro método disponible y de su preferencia.
