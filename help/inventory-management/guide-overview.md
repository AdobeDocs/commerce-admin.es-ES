---
title: Guía de Inventory management [!DNL Inventory Management] Guía'
description: Información completa sobre [!DNL Inventory Management] para administradores de Adobe Commerce y de Magento Open Source, incluida la migración y la configuración.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# [!DNL Inventory Management] Información general de guía

Esta guía está destinada a administradores de Adobe Commerce y Magento Open Source. Proporciona información detallada sobre cómo habilitar este módulo, incluida la configuración y administración de sus funciones. Supone una comprensión básica del núcleo [!DNL Commerce] configuración y funcionalidad.

[!DNL Inventory Management] tiene dos áreas para los administradores:

- Administración: utilice esta área para acceder a la interfaz de usuario de configuración y a los informes.
- Interfaz de línea de comandos: Utilice esta herramienta para ejecutar tareas de instalación y configuración back-end.

Esta guía describe:

| Asunto | Descripción |
| ------- | ----------- |
| [Introducción](introduction.md) | Descripción general de [!DNL Inventory Management] funciones que puede utilizar para administrar existencias en varias ubicaciones, de modo que el almacén de Commerce refleje con precisión el inventario físico. |
| [Notas de la versión](release-notes.md) | Revise las notas de la versión para obtener información acerca de todos los [!DNL Inventory Management] versiones. |
| Conceptos básicos de inventario | Obtenga información básica sobre la administración del inventario: [Existencias y fuentes](sources-stocks.md), [selección de fuentes y reservas](selection-reservations.md), [estado del pedido y la reserva](order-status.md), y [tipos de producto](product-types.md) |
| Introducción | Obtenga información acerca de [!DNL Inventory Management] y cómo se adapta a su instancia de Commerce y a las operaciones de la tienda: [Actualizaciones de Commerce](migrate.md), [instalación y actualización del módulo](install-update.md), [tipos de abastecimiento de comerciante](merchant-sourcing.md), y [cambios en la estructura de abastecimiento](expand-restructure.md) |
| [Configuración](configuration.md) | Obtenga información acerca de la configuración de [!DNL Inventory Management] opciones que determinan la disponibilidad del origen, los productos de la tienda y el envío del pedido. |
| [Administrar fuentes](sources-manage.md) | Obtenga información sobre las fuentes y cómo definen las ubicaciones físicas en las que se administra y envía el inventario de productos para la realización de pedidos o en las que hay servicios disponibles. |
| [Administrar existencias](stocks-manage.md) | Descubra cómo se utilizan las existencias para representar un inventario virtual agregado de productos para las fuentes de sus canales de ventas. |
| [Administrar cantidades](quantities-manage.md) | Aprenda a asignar fuentes y cantidades para nuevos productos o a cambiar los productos existentes. |
| [Administrar pedidos y envíos](shipments.md) | Obtenga información acerca de los [!DNL Inventory Management] funciones y opciones para gestionar cantidades de inventario a través del proceso de envío. |
| [Referencia de CLI](cli.md) | Obtenga información acerca de los comandos proporcionados por [!DNL Inventory Management] para administrar los datos de inventario y las opciones de configuración. |

{style="table-layout:auto"}

## Información para desarrolladores

Consulte [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) en la documentación para desarrolladores para obtener más información sobre la arquitectura de módulos, las API y la personalización de algoritmos.

## Documentación de Commerce

{{docs-links}}

## Solución de problemas y asistencia

Si necesita información o tiene preguntas que no se tratan en esta guía, utilice los siguientes recursos:

- [Incoherencias de reserva de gran número](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Problemas de incoherencia del inventario](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [El inventario de muestras no tachadas alcanza &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Estado de stock incorrecto tras la instalación de Inventory](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Tickets de asistencia](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)—Envíe un ticket para recibir ayuda adicional.
