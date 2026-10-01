---
title: '[!UICONTROL Services] > sincronización de vista de catálogo de ACO'
description: Revise las opciones de configuración en la página [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync] del administrador de Commerce.
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

Utilice esta configuración para controlar cómo [!DNL Adobe Commerce Optimizer Connector for B2B] sincroniza las configuraciones de catálogo compartido B2B (vista de catálogo, directiva, libro de precios y clave) en [!DNL Adobe Commerce Optimizer] y cómo resuelve las diferencias de configuración entre los dos sistemas. Consulte [Supervisión del estado de sincronización de la vista de catálogo](../../systems/catalog-view-sync-status.md) para supervisar los resultados de esta configuración.

{{config}}

## [!UICONTROL Deletion]

![Eliminación](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | Global | Período de retención de datos del catálogo compartido. Especifica el número de días que se conservan las vistas de catálogo, las directivas y los metadatos de un catálogo compartido eliminado antes de eliminarse de forma rígida. El valor predeterminado es de 7 días. Se debe establecer en `0` para su eliminación inmediata. |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | Global | Número de días que una vista de catálogo recién registrada puede esperar a que [!DNL Adobe Commerce Optimizer Connector for B2B] complete su primera sincronización de las configuraciones de vista de catálogo, directiva, libro de precios y clave, mientras que su estado se comunica como [!UICONTROL Pending]. Si el período de gracia transcurre sin que la sincronización se haya realizado correctamente, el estado cambia a [!UICONTROL Failed]. Valor predeterminado: `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| --- | --- | --- |
| [!UICONTROL Enabled] | Global | Ejecuta el reconciliador de deriva programado para detectar e informar de las diferencias entre la vista de catálogo proyectada desde [!DNL Adobe Commerce] y la configuración de la vista de catálogo en [!DNL Adobe Commerce Optimizer]. Si `automatically repair drift` está habilitado, también intentará corregir cualquier discrepancia reparable. |
| [!UICONTROL Automatically Repair Drift] | Global | Cuando se establece en `Yes`, el reconciliador de deriva programado actualiza la configuración de [!DNL Adobe Commerce Optimizer] para que coincida con [!DNL Adobe Commerce] y vuelve a sincronizar la configuración. Cuando se establece en `No`, la ejecución solo detecta e informa de la deriva. Siempre se informa de las entidades huérfanas [!DNL Adobe Commerce Optimizer], nunca se eliminan automáticamente. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Vista de catálogo ACO](./aco-catalog-view.md): configure tokens de acceso para lecturas de tienda de una vista de catálogo
> - [Supervisión del estado de sincronización de la vista de catálogo](../../systems/catalog-view-sync-status.md): supervise el estado de sincronización y concilie la desviación con esta configuración
> - [Administración de claves de acceso restringido](../../systems/restricted-access-keys.md): administre las claves de acceso asignadas a las vistas de catálogo sincronizadas
