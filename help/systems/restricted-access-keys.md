---
title: Administración de claves de acceso restringido en Commerce
description: Cree, asigne y elimine las claves de acceso restringido que protegen las vistas de catálogo compartido B2B sincronizadas con Adobe Commerce Optimizer.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
last-update: 2026-10-01
source-git-commit: 82862dcdd7667b46cfe7bd08863926ae5bafd24b
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# Administrar claves de acceso restringido

Utilice la página Claves de acceso restringido para administrar las claves de acceso para las vistas de catálogo privado creadas por [!DNL Adobe Commerce Optimizer Connector for B2B]. El conector sincroniza las configuraciones del catálogo compartido B2B de Adobe Commerce a Adobe Commerce Optimizer.

>[!NOTE]
>
>Para las claves creadas manualmente que se usan para administrar catálogos privados en escenarios distintos de B2B, como portales de socios, administre claves de [[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}.

## Audiencia y disponibilidad {#audience}

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Solo se aplica a Adobe Commerce en infraestructura en la nube y a proyectos locales."}

La página [!UICONTROL Restricted Access Keys] está disponible para Adobe Commerce en la infraestructura en la nube y para los comerciantes locales que utilizan catálogos compartidos B2B con [!DNL Adobe Commerce Optimizer Connector for B2B]. El conector se instala y habilita la página automáticamente.

Cuando se crea una vista de catálogo por primera vez para un catálogo compartido, el conector genera y asigna automáticamente una clave. Utilice esta página para ver esa clave y para crear, asignar o eliminar claves adicionales.

## Acceso a la página Claves de Acceso Restringido {#access-restricted-access-keys-page}

En el área de Administración, vaya a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**.

![Claves de acceso restringido que enumeran las claves en la página y sus vistas de catálogo asignadas](assets/restricted-access-keys.png){width="600" zoomable="yes"}

En esta página se muestran todas las claves, independientemente de si están asignadas a una vista de catálogo. Para asignar una clave a una vista de catálogo específica, use la acción [!UICONTROL Edit Restricted Access Keys] en esa vista de catálogo. Ver [Asignar claves a una vista de catálogo](#assign-keys-to-a-catalog-view).

## Resumen de claves de acceso restringido {#restricted-access-keys-summary}

La cuadrícula contiene una clave por fila.

| Campo | Descripción |
| --- | --- |
| **ID de clave** | El identificador de clave única. |
| **Título** | Una etiqueta que proporcione para identificar la clave. |
| **Vistas de catálogo asignadas** | El catálogo ve esta clave a la que está asignada actualmente. |
| **Caduca A Las** | La fecha de caducidad de la clave. |
| **Acciones** | Acciones de nivel de fila. Consulte [Administrar claves](#manage-keys). |

## Administrar claves {#manage-keys}

- **[!UICONTROL Create Key]**: genera un nuevo par de claves sin asignar. Commerce genera el par de claves y almacena la clave privada. La clave pública no está registrada con [!DNL Adobe Commerce Optimizer] hasta que asigne la clave a una vista de catálogo.
- **[!UICONTROL View Public Key]**: abre una vista de sólo lectura de la clave pública de la clave, de modo que puede copiarla para volver a registrar o sincronizar la clave si es necesario. La clave privada nunca se muestra.
- **[!UICONTROL Delete]**: quita la clave y revoca su registro remoto en [!DNL Adobe Commerce Optimizer]. Los tokens de tienda ya emitidos con esta clave siguen siendo válidos hasta que caducan. Esta acción no se puede deshacer.

>[!NOTE]
>
>Una clave caducada solo se puede eliminar. No puede asignar ni cancelar la asignación de una clave caducada.

## Creación de una clave

En la página [!UICONTROL Restricted Access Keys], cree una clave seleccionando **[!UICONTROL Create Key]**.

Commerce genera un nuevo par de claves y almacena la clave privada. La tabla Claves de acceso restringido se actualiza con una nueva entrada de clave que muestra el ID de clave único. Utilice este(a) [!UICONTROL Key ID] cuando asigne la clave a una vista de catálogo.

La clave pública no se registra con [!DNL Adobe Commerce Optimizer] hasta que asigne la clave a una vista de catálogo. Después del registro, la entrada de la tabla Claves de acceso restringido se actualiza para mostrar la asignación del catálogo y la fecha de caducidad.

## Asignar o quitar claves de acceso restringido {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## Selección y rotación de claves {#key-selection-and-rotation}

Cuando se asigna más de una clave a una vista de catálogo, [!DNL Adobe Commerce] utiliza automáticamente la clave asignada que no ha caducado con la última fecha de caducidad para firmar tokens.

>[!IMPORTANT]
>
>La rotación automática de claves aún no está disponible. Las claves tienen de forma predeterminada un periodo de caducidad largo. Para girar una clave manualmente, cree una nueva clave y asígnela a la vista de catálogo junto con la existente. Después de confirmar que se está utilizando la clave nueva, elimine la clave antigua.

Para cambiar el período de caducidad predeterminado aplicado a las claves recién creadas, vaya a **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**. Consulte [Servicios > Claves de acceso restringido ACO](../configuration-reference/services/aco-restricted-access-keys.md).

## Limitaciones conocidas {#known-limitations}

- No hay ningún indicador activo o de estado en la cuadrícula principal [!UICONTROL Restricted Access Keys].

  Puede ver el estado del vínculo en la página [!UICONTROL Edit Restricted Access Keys]. Utilice la lista desplegable para ver las claves disponibles y su estado. Si se asigna una clave a una vista de catálogo, se vincula. Si no está asignado, no tiene estado. Puede asignar esas claves a la vista de catálogo que está editando.

  En la página [!UICONTROL Catalog View Sync Status], puede ver las claves vinculadas a una vista de catálogo desde la página de detalles de la vista de catálogo (acción **[!UICONTROL View details]**). La página de detalles también muestra el historial de claves, incluso cuándo se asignaron o quitaron asignaciones de una vista de catálogo.

- La rotación automática de claves aún no está disponible.

>[!MORELIKETHIS]
>
> - [Administrar configuración de vista de catálogo](/help/b2b/catalog-views-manage.md) — Asignar estas claves desde el catálogo compartido o la cuenta de la compañía
> - [Supervisión del estado de sincronización de la vista de catálogo](catalog-view-sync-status.md): supervise y concilie las vistas de catálogo que estas claves protegen
> - [Servicios > Claves de acceso restringido ACO](../configuration-reference/services/aco-restricted-access-keys.md) — Configurar el período de caducidad predeterminado de la clave
> - [Servicios > Vista de catálogo de ACO](../configuration-reference/services/aco-catalog-view.md): configure la duración del token de acceso de tienda y habilite o deshabilite la emisión
> - [Administrar claves de acceso restringido](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} en la *Guía del conector de Adobe Commerce Optimizer*: descubra cómo encajan estas claves en la sincronización del catálogo compartido B2B
> - [Claves de acceso restringido](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} en la *Guía de Adobe Commerce Optimizer*: el flujo de claves manual basado en ACO Studio para casos de uso que no son B2B
