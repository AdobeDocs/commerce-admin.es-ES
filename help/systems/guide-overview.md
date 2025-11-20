---
title: Guía de sistemas de administración
description: Conozca las prácticas de seguridad recomendadas para proteger su tienda de Commerce y administrar permisos, y cómo importar y exportar datos, administrar integraciones y extensiones y ocuparse del mantenimiento rutinario.
exl-id: 9d22571e-9e09-4d1a-ba55-a889f094158d
source-git-commit: 0cda54e8d52a866151658573c6d2ace1820dab75
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 7%

---

# Guía de Adobe Commerce Admin Systems

Esta guía está destinada a administradores de sistemas e integradores que trabajan en Adobe Commerce y en Magento Open Source Admin. Proporciona información detallada sobre la seguridad de administración, las operaciones de mantenimiento y los recursos de todo el sistema que admiten actividades en varias funciones organizativas para su negocio de comercio electrónico. Supone una comprensión básica de la configuración y la funcionalidad principales de Commerce.

Esta guía describe:

| Asunto | Descripción |
| ------- | ----------- |
| [Introducción](introduction.md) | Información general sobre los sistemas y las funciones de integración en una instancia de Commerce. |
| [Menú del sistema](system-menu.md) | Utilice el menú [!UICONTROL System] para acceder a las herramientas de importación y exportación de datos, administración de caché e índice del sistema, administración de cuentas de usuario y permisos, copias de seguridad, notificaciones del sistema y variables personalizadas. |
| [Cuentas y permisos de administrador](permissions.md) | Administre las cuentas de usuario de Admin y las funciones que se utilizan para otorgar acceso a las funciones de la tienda. |
| [Variables](variables-predefined.md) | Las variables facilitan la personalización de las plantillas de correo electrónico, boletines informativos y otros tipos de contenido que admitan el sitio y la experiencia del cliente. |
| [Plantillas de correo electrónico](email-templates.md) | Las plantillas de correo electrónico definen el diseño, el contenido y el formato de los mensajes automatizados enviados desde su tienda. Se denominan correos electrónicos transaccionales porque cada uno está asociado a un tipo específico de transacción o evento. |
| [Transferencia de datos](data-transfer.md) | <ul><li>Las herramientas de importación y exportación permiten administrar varios registros en una sola operación. No solo puede importar nuevos artículos, sino también actualizar, reemplazar y eliminar conjuntos de productos existentes.</li><li>Ver el estado de sincronización de datos de las entidades transferidas a los servicios conectados de Commerce desde [[!UICONTROL Data Management Dashboard]](data-dashboard.md).</li><li>Monitorice el estado de sincronización para la exportación de fuentes de datos a los servicios SaaS de Commerce desde la página [[!UICONTROL Data Export Feed Sync Status]](data-feed-sync-status.md).</li></ul> |
| [Registros de acciones](action-log.md) | En Adobe Commerce, los registros de acciones capturan todos los cambios realizados por un usuario administrador que trabaja en su tienda. Esto le permite realizar un seguimiento de todos los cambios realizados en la tienda. |
| Herramientas | [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} Los administradores del sistema tienen una colección de herramientas disponibles: Las [herramientas de soporte](support.md) están diseñadas para identificar problemas conocidos en su sistema. Las herramientas del sistema proporcionan soporte operativo para realizar la administración rutinaria de [index](index-management.md) y [cache](cache-management.md), hacer una copia de seguridad del sistema[, administrar ](backups.md)operaciones programadas[ y usar una variedad de ](data-scheduled-import-export.md)herramientas para desarrolladores[.](developer-tools.md) |
| [Integraciones](integrations.md) | Establezca la ubicación de las credenciales de OAuth y proporcione las direcciones URL de redireccionamiento para integraciones de terceros. |
| [Seguridad](security.md) | Obtenga información acerca de las herramientas disponibles para proteger su tienda y sus datos, y las directrices para un plan de acción de seguridad si detecta un compromiso. |

{style="table-layout:auto"}

## Documentación disponible

{{docs-links}}
