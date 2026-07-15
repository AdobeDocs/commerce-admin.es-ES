---
title: Resumen del catálogo compartido
description: Conozca los catálogos compartidos que proporciona Adobe Commerce B2B y cómo puede utilizarlos para mantener catálogos cerrados con precios personalizados para diferentes cuentas de empresa.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
TQID: https://experienceleague.adobe.com/9w%2D%2D%2DIjoMFMTgsCSfjp8E0W7Xlp0dxvExVyLMCAJw-c
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 97a3e3469e45ec9c7e3316f1ce5ca7894ea2ddb7
workflow-type: tm+mt
source-wordcount: 597
ht-degree: 0%

---

# Resumen del catálogo compartido

Adobe Commerce B2B le permite mantener _catálogos compartidos_ con puertas y precios personalizados para diferentes empresas. Además del catálogo de productos estándar _primary_, proporciona al cliente acceso a dos tipos de catálogos compartidos con diferentes estructuras de precios.

Si la característica [Catálogo compartido](enable-basic-features.md) está habilitada en la configuración, el catálogo principal original permanece visible desde el administrador, pero solo el catálogo compartido público predeterminado (general) está visible desde la tienda. Además, se pueden crear catálogos personalizados que solo sean visibles para los miembros de cuentas específicas de [empresa](account-companies.md).

Para el catálogo compartido público `Default (General)`, debe asignar productos para que se muestre el catálogo en la tienda. De forma predeterminada, está vacío y no contiene ningún producto.

>[!NOTE]
>
>**[Versión B2B 1.3.0](release-notes.md#b2b-v130) y posterior**: al crear un catálogo compartido, cada [permiso de categoría](../catalog/category-permissions.md) para el catálogo se establece en _[!UICONTROL Allow for the Display Product Prices]_&#x200B;y_[!UICONTROL Add to Cart]_ para los grupos de clientes a los que se asigna este acceso en la configuración de permisos del catálogo. Anteriormente, esta configuración se establecía automáticamente en `Deny` incluso cuando los permisos de catálogo se establecían en `Allow`.

>[!IMPORTANT]
>
>**_todas_** las categorías del catálogo omiten la configuración de permisos de grupo[&#128279;](../configuration-reference/catalog/catalog.md#category-permissions) de existente cuando la característica **_[!UICONTROL Shared Catalog]_** está habilitada. [!UICONTROL Shared Catalog] controla completamente todos los permisos de categoría en el catálogo cuando está habilitado.

La página _[!UICONTROL Shared Catalogs]_&#x200B;proporciona acceso a las herramientas utilizadas para administrar los catálogos compartidos. La página es similar al [espacio de trabajo de administración](../getting-started/admin-workspace.md) estándar, con filtros y controles de acción. La cuadrícula enumera todos los catálogos compartidos, incluido el catálogo compartido público predeterminado y los catálogos personalizados que haya configurado.

![Catálogos compartidos](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Acceder a la página [!UICONTROL Shared Catalogs]

En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Controles de acciones

Los [controles de acciones](../getting-started/admin-actions-control.md) de la esquina superior izquierda se pueden usar con el control de acciones masivas para eliminar los catálogos compartidos seleccionados que ya no son necesarios. En la cuadrícula, la columna _[!UICONTROL Actions]_&#x200B;contiene la selección completa de herramientas para administrar los catálogos compartidos.

![Acciones de catálogo compartido](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| Control | Descripción |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | Determina la selección de productos y los precios personalizados disponibles en el catálogo compartido. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | Determina qué empresas pueden acceder a un catálogo compartido. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | Determina la información detallada del catálogo, incluido el nombre, el tipo de catálogo, la clase de impuestos del cliente y la descripción. |
| [!UICONTROL Delete] | Elimina los catálogos compartidos seleccionados. |

{style="table-layout:auto"}

## Descripciones de columna

| Encabezado | Descripción |
|--- |--- |
| [!UICONTROL Select] | Selecciona registros de catálogo compartido para aplicar una acción. El control del encabezado se puede utilizar para seleccionar todos los registros del catálogo compartido o anular su selección en la cuadrícula. Para seleccionar un catálogo compartido individual, marque la casilla de verificación. |
| [!UICONTROL ID] | Identificador numérico único que se asigna en secuencia cuando se crea el catálogo. |
| [!UICONTROL Name] | Nombre del catálogo compartido. De forma predeterminada, el catálogo compartido predeterminado (General) está disponible. |
| [!UICONTROL Type] | Identifica el tipo de catálogo compartido como: <br/>**[!UICONTROL Public]**- El catálogo compartido público predeterminado se crea automáticamente cuando se instala Adobe Commerce B2B. Inicialmente se asigna a los grupos de clientes `General` y `Not Logged In`, y es visible para los invitados y los clientes individuales que iniciaron sesión y que no están asociados a una compañía. El sistema solo admite un catálogo compartido público a la vez.<br/>**[!UICONTROL Custom]**: un catálogo compartido personalizado contiene precios que solo son visibles para los asociados que iniciaron sesión en las cuentas de compañía asignadas. Puede crear tantos catálogos compartidos personalizados como necesite. |
| [!UICONTROL Customer Tax Class] | La clase de impuesto asignada al grupo de clientes correspondiente. Esta columna no aparece en la cuadrícula predeterminada, pero se puede agregar cambiando el diseño de la columna. |
| [!UICONTROL Created At] | La fecha y la hora de creación del catálogo compartido. |
| [!UICONTROL Created By] | El nombre y los apellidos del administrador de la tienda que creó el catálogo compartido. |
| [!UICONTROL Action] | Enumera las acciones que se aplicarán a los catálogos seleccionados. Opciones: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
