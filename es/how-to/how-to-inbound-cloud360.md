---
title: "Permitir comunicación entrante en TIGO Cloud 360"
slug: entrada-internet-cloud360
---

Los entornos (VDC) de TIGO Cloud 360 cuentan con capacidad de establcer conexion desde y hacía Internet. El presente artículo describe las configuraciones a realizar para publicar un puerto en Internet y permitir la comunicación entrante. Particularmente se aborda como publicar el puerto 443 (https) para una página Web.

### Pasos inciales

Navegue hasta el entorno (VDC) deseado donde aparecerá la sección **Máquinas virtuales**. Seleccione la opción **Redes** y, posteriormente, la opción **Puerta de enlace EDGE**. Se mostrarán todos los dispositivos EDGE disponibles para el entorno (VDC) actual. En la mayoría de los casos, solo existirá un dispositivo EDGE.

Será dentro del dispositivo EDGE donde se realizarán todas las configuraciones necesarias para permitir la comunicación entrante desde Internet.

![Pantalla principal del EDGE](/assets/vmware-edge-es.png)

### Crear regla NAT

De clic en el ícono de engrane para la sección **Reglas NAT** en el dispositivo EDGE. Al hacerlo, se mostrará el listado de las reglas de NAT actualmente configuradas. Es posible que el listado aparezca vacío si es la primera regla NAT que se genera o bien, si se realizó una eliminación completa de reglas.

De clic en el botón **Agregar una regla NAT** ubicado en la parte derecha de la página, esta acción iniciará el asistente de configuración de nuevas reglas.

Ingrese un nombre descriptivo para este regla. En el campo **Tipo** seleccione la opción DNAT.
De forma automática, el sistema asignará la IP Pública del EDGE en el campo **IP externas**. No haga cambios en este valor.
En el campo **IP internas** podrá especificar una IP puntual que, en este caso, corresponde a la dirección asociada a la máquina virtual donde reside el servicio Web a publicar. Asusmamos que la IP de esta máquina es la 192.168.12.10/32.

En el campo **Puerto exterior** podemos especificar un puerto personalizado para el servicio en caso de que no se quiera utilizar el puerto real del servicio. Para nuestro ejemplo, este campo se dejará en blanco.

Seleccionar el valor HTTPS - TCP: 443 de la lista asociada al campo **Aplicación**.

De clic en **Aplicar** para crear la regla NAT.

![Pantalla con ejemplo de configuración de una regla NAT](/assets/vmware-nat-rule-out-es.png)

### Crear conjunto de IP

Un conjunto IP es un grupo de direcciones IP que pueden utilizarse como orígenes y destinos en las reglas de firewall. Un conjunto IP puede contener una combinación de direcciones IP individuales, rangos IP y subredes.

Navegue de regreso a la pantalla de configuración del dispositivo EDGE. De clic en el ícono de engrane para la sección **Conjutos de IP**. Al hacerlo, se mostrará el listado de los conjutos de IPs actualmente configurados. Es posible que el listado aparezca vacío si es el primer conjunto que se genera o bien, si se realizó una eliminación completa de conjuntos.

De clic en botón **Agregar un conjunto de IP** ubicado en la parte derecha de la página, esta acción iniciará el asistente de configuración de nuevos conjuntos.

Ingrese un nombre descriptivo para este conjunto y, opcionalmente, una descripción detallada. Si pretende otorgar la salida a Internet a todo un segmento de red, puede optar por seleccionar el valor Red CIDR del campo **Tipo** y seleccionar la red en cuestión del campo desplegable **Red CIDR**. Si pretende otorgar la salida a Internet solo a una máquina virtual, puede optar por seleccionar el valor Manual del campo **Tipo** y en el campo **Direcciones IP** ingresar la IP de la máquina virtual, en nuestro ejemplo el valor a asignar sería la IP del servidor Web, es decir, 192.168.12.10/32.

De clic en **Aplicar** para crear el conjuto de IP.

![Pantalla con ejemplo de configuración de un conjunto de IP](/assets/vmware-ip-set-out-es.png)

### Crear regla de Firewall

Navegue de regreso a la pantalla de configuración del dispositivo EDGE. De clic en el ícono de engrane para la sección **Reglas de firewall**. Al hacerlo, se mostrará el listado de las reglas de firewall actualmente configuradas. Este listado contendrá, por lo menos, la regla por defecto la cual es un drop desde *ANY* y hacia *ANY*. Esta regla no se puede eliminar, ya que es una medida de protección para descartar todo el tráfico que no tenga una regla que lo permita.

De clic en botón **Agregar regla de cortafuegos** ubicado en la parte derecha de la página, esta acción iniciará el asistente de configuración de nuevas reglas de firewall.

Ingrese un nombre descriptivo para este regla. Asegurese de que la casilla **Activada** esté seleccionada. En el campo **Prioridad** seleccione el valor Encima. Tenga en cuenta que la prioridad que se le asigne a una regla influye directamente en el resultado. Si la regla de firewall que permite comunicación está debajo de una regla que no permite esa misma comunicación, entonces la comunicació no se establecerá.

En el campo **Fuente** seleccione el valor Cualquier para permitir el acceso desde cualquier ubicación en Internet. Si quiere limitar el acceso solo a ciertas IPs, es necesario primero crear el conjunto de IP. En el campo destino, seleccione el nombre del conjunto de IP recién creado. El campo acción debe de tener como valor Permitir. En nuestro ejemplo estamos trabajando con IPv4, por lo tanto, dicho valor debe estar seleccionado el campo **Protocolo IP**.

De clic en **Aplicar** para crear la regla de firewall.

![Pantalla con ejemplo de configuración de una regla FW](/assets/vmware-fw-rule-out-es.png)

Confirme el resultado accediendo al portal Web desde Internet.
