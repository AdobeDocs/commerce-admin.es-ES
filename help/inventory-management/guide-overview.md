---
title: Guía de [!DNL Inventory Management]
description: Guía de administración y CLI para  [!DNL Inventory Management] existencias, fuentes, cantidades, configuración, pedidos y envíos en Adobe Commerce y Magento Open Source.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a3817847081e56272e3677dede02d992e760a2d4
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 1%

---

# Información general de [!DNL Inventory Management]

Esta guía es para administradores que administran las existencias en varias ubicaciones de Adobe Commerce y Magento Open Source. Proporciona procedimientos de configuración y administración para el módulo [!DNL Inventory Management] y supone una comprensión básica de la funcionalidad principal [!DNL Commerce].

Use **Admin** para tareas de configuración, creación de informes e inventario diario. Use la **interfaz de línea de comandos** para la instalación, las actualizaciones y la configuración del servidor.

Esta guía describe:

| Asunto | Descripción |
| ------- | ----------- |
| [Introducción](introduction.md) | Características, terminología y la forma en que [!DNL Inventory Management] se adapta a tu tienda. |
| [Notas de la versión](release-notes.md) | Historial de versiones del módulo y problemas conocidos. |
| [Conceptos básicos de inventario](sources-stocks.md) | Conceptos de [existencias y orígenes](sources-stocks.md), [selección y reservas de origen](selection-reservations.md), [estado de pedidos y reservas](order-status.md) y [tipos de productos](product-types.md). |
| Introducción | [actualizaciones de Commerce](migrate.md), [instalación y actualizaciones](install-update.md), [tipos de abastecimiento de comerciantes](merchant-sourcing.md) y [reestructuración de inventarios](expand-restructure.md). |
| [Configuración](configuration.md) | Configuración global, de producto y de algoritmo para la visualización y el envío de tiendas. |
| [Administrar orígenes](sources-manage.md) | Crear y mantener ubicaciones de cumplimiento. |
| [Administrar existencias](stocks-manage.md) | Asignar orígenes a canales de ventas. |
| [Administrar cantidades](quantities-manage.md) | Asignar y actualizar cantidades de productos por origen. |
| [Administrar pedidos y envíos](shipments.md) | Satisfacer pedidos y administrar envíos desde el inventario. |
| [Referencia de CLI](cli.md) | Tareas de configuración e inventario de la línea de comandos. |

{style="table-layout:auto"}

## Información para desarrolladores

Acceda a recursos avanzados para API, personalización y arquitectura de módulos. Consulte [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) en la documentación para desarrolladores de API de REST para obtener detalles técnicos sobre las API y la personalización del algoritmo.

## Documentación de Commerce

Encuentre guías para comerciantes, nubes y desarrolladores que le ayuden con cada parte de Adobe Commerce. Utilice estos recursos para cualquier necesidad de configuración o administración.

{{docs-links}}

## Solución de problemas y asistencia

Utilice artículos de soporte y sistemas de tickets para resolver problemas de inventario rápidamente. Obtenga ayuda adicional sobre el estado de las existencias o la administración de productos.

Si necesita información o tiene preguntas que no se tratan en esta guía, utilice los siguientes recursos:

- [Estado de stock incorrecto tras la instalación de Inventory](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-29910)
- [Entradas de soporte técnico](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case): envía un ticket para recibir ayuda adicional.
