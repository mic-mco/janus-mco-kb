---
title: "AWS: Instancias"
slug: aws-instancias
---

Al igual que otras plataformas en la nube, AWS proporciona la infraestructura para ejecutar máquinas virtuales. Estas máquinas virtuales se denominan instancias. Una instancia se basa en una imagen predefinida llamada **[AMI](aws-amis.md)**, que no se puede cambiar una vez que se implementa una instancia. Diferentes conjuntos de especificaciones se agrupan como tipos de instancia. Cada tipo de instancia es un paquete de varios tamaños de vCPU, memoria y un volumen de almacenamiento raíz. Para obtener más detalles, consulte [Tipos de instancias de Amazon EC2](https://aws.amazon.com/es/ec2/instance-types/) en la documentación de AWS.

Al implementar una instancia, se debe seleccionar una región de AWS. La región determina qué subredes, volúmenes, AMI y otros recursos estarán disponibles para las nuevas instancias.

Para iniciar sesión en una instancia, es requerido utilizar el par de claves SSH que se generan automáticamente al crear la instancia. La clave SSH privada es la única forma de iniciar sesión en la instancia y debe almacenarse e instalarse de manera segura en la aplicación SSH que usará para conectarse a la instancia.

**Importante:** Debes almacenar de forma segura la clave SSH privada inmediatamente. No se almacenará en ningún lugar de la interfaz de usuario de TIGO MCO y no se podrá recuperar una vez que se borre la notificación del panel. No se puede iniciar sesión en una instancia sin esta clave. Si se pierde, deberás seguir un procedimiento de recuperación, que requiere el reinicio de la instancia.

Las instancias se enumeran en la pestaña **Cómputo** de tu entorno de AWS, en la sección **Instancias**.

**Tema principal:** [AWS: Cómputo](aws-compute.md)
