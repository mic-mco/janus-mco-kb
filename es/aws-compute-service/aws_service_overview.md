---
title: "AWS: Resumen de servicios"
slug: aws-resumen-de-servicios
---

## Resumen

TIGO MCO permite acceder y administrar la infraestructura y los recursos que se han desplegado en la plataforma de Amazon Web Services \(AWS\). Este artículo presentará los conceptos básicos de esta nube y como trabajar con los recursos de AWS en TIGO MCO.

## Descripción detallada

La plataforma de AWS es una nube pública, donde los clientes pueden asignar recursos para construir una infraestructura para sus aplicaciones. TIGO MCO proporciona una interfaz unificada para acceder a AWS y otros servicios desde un único portal. A través de TIGO MCO, los usuarios pueden gestionar:

- [Recursos de cómputo y almacenamiento](aws-compute.md):
  - [Instancias](aws-instances.md)
  - [Imágenes de máquina de Amazon \(AMIs\)](aws-amis.md)
  - [Volúmenes](aws-volumes.md)
- [Recursos de red](aws-networking.md):
  - [VPCs](aws-vpcs.md)
  - [Subredes](aws-subnetworks.md)
- [Recursos de almacenamiento de objetos](aws-object_storage.md)

Debido a que TIGO MCO actúa como un portal único para los servicios de múltiples nubes, es posible que algunas operaciones parezcan comportarse de manera diferente que cuando interactúa directamente con AWS. Sin embargo, detrás de escena, todas las operaciones se ejecutan exactamente como lo harían normalmente. Los cambios realizados en las entidades de AWS en TIGO MCO se reflejarán inmediatamente en los recursos reales.
