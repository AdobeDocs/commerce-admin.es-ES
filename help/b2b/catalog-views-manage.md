---
title: Administrar configuración de vista de catálogo
description: Obtenga información sobre cómo revisar las vistas de catálogo de Adobe Commerce Optimizer creadas para los catálogos compartidos B2B y asignar las claves de acceso restringido que los protegen.
feature: B2B, Companies, Catalog Management
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
last-update: 2026-10-01
source-git-commit: 82862dcdd7667b46cfe7bd08863926ae5bafd24b
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# Administrar configuración de vista de catálogo

Con la extensión [!DNL Adobe Commerce Optimizer Connector for B2B] instalada, la página Vistas del catálogo enumera las [!DNL Adobe Commerce Optimizer] [proyecciones de vista del catálogo](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"} creadas para el catálogo compartido personalizado.  Una _proyección_ es la vista de catálogo creada cuando el conector sincroniza los datos del catálogo compartido con [!DNL Adobe Commerce Optimizer]. El conector crea una proyección independiente para cada vista de tienda en el catálogo compartido, de modo que un catálogo compartido puede tener varias vistas de catálogo. En las experiencias de tienda, estas vistas de catálogo solo son accesibles para las empresas asignadas al catálogo compartido asociado.

Por ejemplo, supongamos que Acme Industrial está asignada a un catálogo compartido, EU Business, que pertenece al sitio web de la UE. Ese sitio web tiene dos vistas de la tienda:

- `English (UK)`

- `German (Germany)`

El conector proyecta el catálogo compartido en dos vistas de catálogo [!DNL Adobe Commerce Optimizer]:

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

La empresa tiene vistas de catálogo en inglés y alemán, pero solo una asignación de catálogo compartido. Cada vista de tienda muestra los datos de su vista de catálogo correspondiente.

Ambas vistas de catálogo pueden compartir el mismo libro de precios cuando utilizan el mismo sitio web y el mismo ámbito de precios del grupo de clientes.

## Autenticación de vista de catálogo

El conector protege las vistas del catálogo con claves de acceso restringidas. Adobe Commerce utiliza la clave privada para firmar un token de acceso para un comprador autorizado. Antes de devolver los datos del catálogo protegido, [!DNL Adobe Commerce Optimizer] valida el token con la clave pública correspondiente asociada a la vista de catálogo solicitada.

Para configurar la duración del token o deshabilitar la emisión del token, consulte [Servicios > Vista de catálogo de ACO](/help/configuration-reference/services/aco-catalog-view.md).

Puede revisar estas vistas de catálogo y administrar sus claves asignadas desde la pestaña _[!UICONTROL Catalog Views]_del catálogo compartido o desde la sección_[!UICONTROL Catalog Views]_ de la empresa asociada; ambas muestran las mismas vistas de catálogo y las asignaciones de claves actuales. Consulte [Editar claves de acceso restringido](#edit-restricted-access-keys) para ver la ruta de navegación exacta desde cada ubicación.

Para supervisar la sincronización de datos del catálogo compartido con [!DNL Adobe Commerce Optimizer], consulte [Supervisión del estado de sincronización de la vista de catálogo](/help/systems/catalog-view-sync-status.md).

## Referencia de vistas de catálogo

{{$include /help/_includes/catalog-views-reference-table.md}}

## Editar claves de acceso restringido

{{$include /help/_includes/edit-restricted-access-keys.md}}

Para obtener más información, consulte [Administrar claves de acceso restringido](/help/systems/restricted-access-keys.md).

>[!MORELIKETHIS]
>
> - [Proyección de catálogo compartido B2B](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [Servicios > Vista de catálogo de ACO](/help/configuration-reference/services/aco-catalog-view.md)
> - [Supervisión del estado de sincronización de vista de catálogo](/help/systems/catalog-view-sync-status.md)
> - [Administrar sus catálogos compartidos](catalog-shared-manage.md)
> - [Administrar cuentas de compañía](account-company-manage.md)
