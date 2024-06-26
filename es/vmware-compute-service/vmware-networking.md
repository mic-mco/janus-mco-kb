---
title: "Cloud 360: Redes"
slug: cloud360-redes
---

La creación de redes es una parte fundamental de cualquier infraestructura en la nube. Este artículo presenta los conceptos básicos de redes en TIGO Cloud 360 y las funciones correspondientes en la interfaz de usuario.

Se puede acceder a todas las funciones de red a través de la sección **Redes** del entorno (VDC) Cloud 360 seleccionado.

## Descripción detallada

TIGO Cloud 360 proporciona un conjunto completo de funciones de redes virtuales. Se puede crear una red básica y aislada sin ningún otro requisito previo. La red proporciona un servidor DHCP para configurar automáticamente los dispositivos que se conectan a la red, utilizando un espacio de direcciones IP que usted define en el momento de la creación. También se puede configurar manualmente las interfaces que se conectan a la red, si lo desea. Una red aislada permitirá la creación de máquinas virtuales que podrán comunicarse entre sí, pero no tendrán conectividad con ninguna otra red. Para poder conectarse a otras redes o al Internet público, se debe configurar una puerta de enlace Edge en su entorno (VDC).

Se admiten los siguientes tipos diferentes de redes:

- **Aislada**

    El modo de red más básico, una red aislada, proporciona conectividad entre las interfaces conectadas a ella. Este tipo de redes no proporcionan conectividad con el mundo exterior. Al utilizar una red aislada, sólo las máquinas virtuales dentro del mismo entorno (VDC) se pueden comunicar entre ellas.

- **Con enrutamiento**

    Esto también se conoce como red enrutada NAT. Una red enrutada proporciona conectividad externa junto con servicios NAT, firewall y VPN.

## Estados de redes

Las redes tienen los siguientes estados:

- **Realizado**

     La red ha sido creada y está lista para su uso.

- **Pendiente**

     La configuración de red ha sido enviada y está esperando para comenzar a realizarse.

- **Configurando**

     Actualmente se está realizando la configuración de la red.

- **Realización fallida**

     El sistema no pudo realizar la configuración de la red.

- **Desconocido**

     No es posible conocer el estado actual de la red, puede ser un estado temporal.
