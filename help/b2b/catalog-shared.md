---
title: Resumen del catálogo compartido
description: Conozca los catálogos compartidos que proporciona Adobe Commerce B2B y cómo puede utilizarlos para mantener catálogos cerrados con precios personalizados para diferentes cuentas de empresa.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Resumen del catálogo compartido

Adobe Commerce B2B le ofrece la capacidad de mantener _compartido_ catálogos con precios personalizados para diferentes empresas. Además de la norma, _principal_, catálogo de productos, proporciona al cliente acceso a dos tipos de catálogos compartidos con diferentes estructuras de precios.

Si la variable [Función de catálogo compartido](enable-basic-features.md) está habilitado en la configuración, el catálogo principal original permanece visible desde el administrador, pero solo el catálogo compartido público predeterminado (general) está visible desde la tienda. Además, se pueden crear catálogos personalizados que solo sean visibles para miembros de [compañía](account-companies.md) cuentas.

Para el `Default (General)` catálogo compartido público, debe asignar productos para mostrar el catálogo en la tienda. De forma predeterminada, está vacío y no contiene ningún producto.

>[!NOTE]
>
>**[Versión 1.3.0 de B2B](release-notes.md#b2b-v130) y más tarde** — Al crear un catálogo compartido, cada [permiso de categoría](../catalog/category-permissions.md) para el catálogo se establece en _[!UICONTROL Allow for the Display Product Prices]_y_[!UICONTROL Add to Cart]_ para grupos de clientes a los que se asigna este acceso en la configuración de permisos de catálogo. Anteriormente, esta configuración se establecía automáticamente en `Deny` incluso cuando los permisos de catálogo estaban configurados en `Allow`.

>[!IMPORTANT]
>
>Todos los existentes [configuración de permisos de grupo](../configuration-reference/catalog/catalog.md#category-permissions) son ignoradas por **_todo_** categorías en el catálogo cuando la variable **_[!UICONTROL Shared Catalog]_** La función está activada. [!UICONTROL Shared Catalog] controla completamente todos los permisos de categoría del catálogo cuando está activado.

El _[!UICONTROL Shared Catalogs]_proporciona acceso a las herramientas utilizadas para gestionar los catálogos compartidos. La página es similar al estándar [Admin Workspace](../getting-started/admin-workspace.md), con filtros y controles de acción. La cuadrícula enumera todos los catálogos compartidos, incluido el catálogo compartido público predeterminado y los catálogos personalizados que haya configurado.

![Catálogos compartidos](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Acceda a la [!UICONTROL Shared Catalogs] página

En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Controles de acciones

El [controles de acciones](../getting-started/admin-actions-control.md) en la esquina superior izquierda, se puede utilizar con el control de acciones masivas para eliminar los catálogos compartidos seleccionados que ya no sean necesarios. En la cuadrícula, la variable _[!UICONTROL Actions]_contiene la selección completa de herramientas para administrar los catálogos compartidos.

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
| [!UICONTROL Type] | Identifica el tipo de catálogo compartido como: <br/>**[!UICONTROL Public]**: El catálogo compartido público predeterminado se crea automáticamente cuando se instala Adobe Commerce B2B. Se asigna inicialmente al `General` y `Not Logged In` grupos de clientes y es visible para los invitados y los clientes individuales que iniciaron sesión y que no están asociados a una compañía. El sistema solo admite un catálogo compartido público a la vez.<br/>**[!UICONTROL Custom]** : un catálogo compartido personalizado contiene precios que solo son visibles para los socios que iniciaron sesión en las cuentas de empresa asignadas. Puede crear tantos catálogos compartidos personalizados como necesite. |
| [!UICONTROL Customer Tax Class] | La clase de impuesto asignada al grupo de clientes correspondiente. Esta columna no aparece en la cuadrícula predeterminada, pero se puede agregar cambiando el diseño de la columna. |
| [!UICONTROL Created At] | La fecha y la hora de creación del catálogo compartido. |
| [!UICONTROL Created By] | El nombre y los apellidos del administrador de la tienda que creó el catálogo compartido. |
| [!UICONTROL Action] | Enumera las acciones que se aplicarán a los catálogos seleccionados. Opciones: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
