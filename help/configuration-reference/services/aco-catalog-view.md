---
title: '[!UICONTROL Services] > Vista de catálogo de ACO'
description: Revise y actualice las opciones de configuración de Adobe Commerce Optimizer en la página [!UICONTROL Services] > [!UICONTROL ACO Catalog View] del administrador de Commerce.
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

Use esta configuración para controlar los tokens de acceso emitidos por [!DNL Adobe Commerce Optimizer Connector for B2B]. Las tiendas utilizan estos tokens para autenticarse en las vistas de catálogo privado de Commerce Optimizer rellenadas con datos sincronizados a partir de catálogos compartidos personalizados configurados en el administrador.

{{config}}

![Administrador de Adobe Commerce que muestra la configuración del token de acceso de la vista de catálogo de ACO, con un TTL de 3600 segundos y una emisión de token habilitada.](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | Global | Número de segundos que un token de acceso sigue siendo válido después de generarse. Esta configuración es de solo lectura en el ámbito predeterminado. Los valores configurados en el sitio web o en el ámbito de la vista de tienda se omiten. El valor predeterminado es: 3600 segundos. |
| [!UICONTROL Issue Access Tokens] | Vista de tienda | Controla si la tienda puede obtener un token de acceso para una vista de catálogo. Cuando se establece en `No`, `Company.catalogViewContext` devuelve el identificador de vista de catálogo, pero no el token de acceso, por lo que los escaparates no pueden autenticarse para leer desde [!DNL Adobe Commerce Optimizer] vistas de catálogo privado sincronizadas desde Adobe Commerce. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Sincronización de vista de catálogo ACO](./aco-catalog-view-sync.md): configure cómo se sincronizan las vistas de catálogo en [!DNL Adobe Commerce Optimizer]
> - [Supervisión del estado de sincronización de la vista de catálogo](../../systems/catalog-view-sync-status.md) — Supervisión del estado de sincronización y conciliación de la deriva
