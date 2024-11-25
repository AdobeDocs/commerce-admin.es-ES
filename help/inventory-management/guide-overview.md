---
title: 'Guía de Inventory management [!DNL Inventory Management] Guide'
description: Información completa sobre [!DNL Inventory Management] para administradores de Adobe Commerce y Magento Open Source, incluida la migración y configuración.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Información general de la guía [!DNL Inventory Management]

Esta guía está destinada a administradores de Adobe Commerce y Magento Open Source. Proporciona información detallada sobre cómo habilitar este módulo, incluida la configuración y administración de sus funciones. Supone una comprensión básica de la configuración y la funcionalidad principales de [!DNL Commerce].

[!DNL Inventory Management] tiene dos áreas para administradores:

- Administración: utilice esta área para acceder a la interfaz de usuario de configuración y a los informes.
- Interfaz de línea de comandos: Utilice esta herramienta para ejecutar tareas de instalación y configuración back-end.

Esta guía describe:

| Asunto | Descripción |
| ------- | ----------- |
| [Introducción](introduction.md) | Descripción general de las funciones de [!DNL Inventory Management] que puede usar para administrar existencias en varias ubicaciones de modo que el almacén de Commerce refleje con precisión el inventario físico. |
| [Notas de la versión](release-notes.md) | Revise las notas de la versión para obtener información acerca de todas las versiones de [!DNL Inventory Management]. |
| Conceptos básicos de inventario | Conozca los conceptos básicos sobre la administración del inventario: [Existencias y fuentes](sources-stocks.md), [selección y reservas de origen](selection-reservations.md), [estado de pedidos y reservas](order-status.md) y [tipos de productos](product-types.md) |
| Introducción | Obtenga información acerca del módulo [!DNL Inventory Management] y cómo encaja en las operaciones de la tienda e instancia de Commerce: [actualizaciones de Commerce](migrate.md), [instalación y actualización de módulos](install-update.md), [tipos de abastecimiento de comerciantes](merchant-sourcing.md) y [cambios en la estructura de abastecimiento](expand-restructure.md) |
| [Configuración](configuration.md) | Obtenga información acerca de la configuración de las opciones de [!DNL Inventory Management] que determinan la disponibilidad del origen, los productos de la tienda y el envío del pedido. |
| [Administrar orígenes](sources-manage.md) | Obtenga información sobre las fuentes y cómo definen las ubicaciones físicas en las que se administra y envía el inventario de productos para la realización de pedidos o en las que hay servicios disponibles. |
| [Administrar existencias](stocks-manage.md) | Descubra cómo se utilizan las existencias para representar un inventario virtual agregado de productos para las fuentes de sus canales de ventas. |
| [Administrar cantidades](quantities-manage.md) | Aprenda a asignar fuentes y cantidades para nuevos productos o a cambiar los productos existentes. |
| [Administrar pedidos y envíos](shipments.md) | Obtenga información acerca de las características y opciones adicionales de [!DNL Inventory Management] para administrar las cantidades de inventario a través del proceso de envío. |
| [Referencia de CLI](cli.md) | Obtenga información acerca de los comandos proporcionados por el módulo [!DNL Inventory Management] para administrar los datos de inventario y las opciones de configuración. |

{style="table-layout:auto"}

## Información para desarrolladores

Consulte [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) en la documentación para desarrolladores para obtener detalles sobre la arquitectura de módulos, las API y la personalización de algoritmos.

## Documentación de Commerce

{{docs-links}}

## Solución de problemas y asistencia

Si necesita información o tiene preguntas que no se tratan en esta guía, utilice los siguientes recursos:

- [Estado de stock incorrecto después de la instalación del inventario](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Entradas de soporte técnico](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket): envía un ticket para recibir ayuda adicional.
