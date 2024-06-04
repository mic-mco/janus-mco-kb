---
title: "AWS: Agregar una VPC"
slug: aws-agregar-una-vpc
---

## Acerca de esta tarea

Este artículo te guiará a través del proceso de agregar una nueva VPC a un entorno (cuenta) de AWS.

## Antes de comenzar

- Tu entorno (cuenta) de AWS ya debe existir
- Si no deseas utilizar los valores predeterminados proporcionados por el sistema, debes tener el nombre y el CIDR que deseas asignar a la nueva VPC

## Procedimiento

1. Haz clic en el botón **Agregar una red VPC**. Aparecerá la página **Agregar una red VPC**.

2. Introduce un nombre para la nueva VPC en el campo **Nombre** o acepta el valor predeterminado.

3. Ingresa el CIDR deseado para la nueva VPC en el campo **CIDR** o acepta el valor predeterminado.

     El CIDR expresa el tamaño y el rango de direcciones IP que se usarán para definir la nueva VPC. Consulta [VPCs](aws-vpcs.md) para obtener más detalles.

     El sistema presentará un error si se proporciona un CIDR no válido.

4. Haz clic en **Aplicar**.

## Resultados

- Se crea la VPC y se puede usar para agregar subredes
- La VPC tiene el rango de IP especificado por el CIDR
- La VPC aparece en la pestaña **Redes**
