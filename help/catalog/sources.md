---
title: Configuración del producto - [!UICONTROL Sources]
description: Para un producto, la variable [!UICONTROL Sources] La configuración de proporciona acceso a [!DNL Inventory Management] orígenes desde los que se puede distribuir el producto.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# Configuración del producto - [!UICONTROL Sources]

El _[!UICONTROL Sources]_de la configuración del producto enumera los orígenes desde los que se puede distribuir el producto. Se utiliza para asignar y cancelar la asignación de orígenes, así como para administrar la cantidad y la disponibilidad del producto. Esta sección solo se muestra si hay más de un origen definido para la tienda. Para obtener más información sobre las fuentes, consulte [Administrar fuentes](../inventory-management/sources-manage.md).

## Asignar un origen para un producto

1. Haga clic **[!UICONTROL Assign Source]**.

1. Seleccione la casilla de verificación de los orígenes necesarios.

1. Haga clic **[!UICONTROL Done]**.

1. Seleccionar **[!UICONTROL Source Item Status]** e introduzca la variable **[!UICONTROL Qty]** y **[!UICONTROL Notify Qty]** valores según sea necesario.

1. Clic **[!UICONTROL Save]** para guardar los cambios.

![Vista de orígenes](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Referencia de campo

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Name] | El nombre único de un origen. |
| [!UICONTROL Source Status] | Determina si el producto está habilitado o deshabilitado en el catálogo. |
| [!UICONTROL Source Item Status] | Determina la disponibilidad actual del producto. Opciones:<br />**[!UICONTROL In Stock]**- Hace que el producto esté disponible para la compra.<br />**[!UICONTROL Out of Stock]** - A menos que se activen los pedidos pendientes, impide que el producto esté disponible para la compra y elimina el listado del catálogo. |
| [!UICONTROL Qty] | Cantidades de stock disponibles para cada origen. |
| [!UICONTROL Notify Qty] | Una cantidad para _Notificar por cantidad_ para esta fuente específica si `Notify Quantity Use Default` no está seleccionado. |
| [!UICONTROL Notify Qty Use Default] | Indica que se debe utilizar la configuración predeterminada para _Notificar por cantidad_ en el inventario avanzado de productos o en la configuración global de la tienda. Para obtener más información sobre la configuración avanzada de inventario del producto, consulte [Configuración de opciones de producto avanzadas](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Para un origen asignado, haga clic en **[!UICONTROL Unassign]** para que el origen no esté disponible para el producto. Para un origen no asignado, haga clic en **[!UICONTROL Assign Sources]** para que una fuente esté disponible para el producto. Para obtener más información acerca de [!UICONTROL Assign Sources] opciones, consulte [Asignación de fuentes por producto](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
