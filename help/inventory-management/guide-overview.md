---
title: Guía de Inventory management [!DNL Inventory Management] Guide
description: Información completa sobre [!DNL Inventory Management] para administradores de Adobe Commerce y Magento Open Source, incluida la migración y configuración.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# Información general de la guía [!DNL Inventory Management]

Esta guía está dirigida a los administradores que trabajan en Adobe Commerce y en Magento Open Source Admin. Proporciona información detallada sobre cómo habilitar este módulo, incluida la configuración y administración de sus funciones. Supone una comprensión básica de la configuración y la funcionalidad principales de [!DNL Commerce].

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

- [Estado de stock incorrecto tras la instalación de Inventory](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Entradas de soporte técnico](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket): envía un ticket para recibir ayuda adicional.
