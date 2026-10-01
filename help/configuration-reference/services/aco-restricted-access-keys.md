---
title: '[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]'
description: Revise las opciones de configuración en la página [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys] del administrador de Commerce.
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
source-wordcount: '182'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

Utilice esta configuración para controlar el período de caducidad predeterminado que [!DNL Adobe Commerce Optimizer Connector for B2B] aplica a las claves de acceso restringido que aprovisiona para las vistas de catálogo compartido B2B. Para crear, asignar y eliminar estas claves, consulte [Administración de claves de acceso restringido](../../systems/restricted-access-keys.md).

{{config}}

## [!UICONTROL Provisioning]

![Aprovisionamiento](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | Global | Período de validez de las claves de acceso restringido recién aprovisionadas. [!DNL Adobe Commerce Optimizer] requiere una fecha de caducidad al menos un minuto en el futuro en cada clave y excluye las claves caducadas de las lecturas de puerta de enlace, por lo que siempre se aplica un valor de al menos un día. Valor predeterminado: `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>La caducidad predeterminada se establece en un período de caducidad largo porque la rotación automática de claves aún no está disponible. Ver [Selección y rotación de clave](../../systems/restricted-access-keys.md#key-selection-and-rotation).

>[!MORELIKETHIS]
>
> - [Vista de catálogo ACO](./aco-catalog-view.md) — Configurar tokens de acceso a tienda para vistas de catálogo
> - [Administración de claves de acceso restringido](../../systems/restricted-access-keys.md): cree, asigne y elimine claves de acceso restringido
> - [Supervisión del estado de sincronización de la vista de catálogo](../../systems/catalog-view-sync-status.md): las claves de monitor están a punto de expirar
