---
title: Configuración del producto - [!UICONTROL Sources]
description: Para un producto, la configuración de [!UICONTROL Sources] proporciona acceso a las  [!DNL Inventory Management] fuentes desde las que se puede distribuir el producto.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 259
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Sources]

La sección _[!UICONTROL Sources]_&#x200B;de la configuración del producto enumera los orígenes desde los que se puede distribuir el producto. Se utiliza para asignar y cancelar la asignación de orígenes, así como para administrar la cantidad y la disponibilidad del producto. Esta sección solo se muestra si hay más de un origen definido para la tienda. Para obtener más información sobre las fuentes, consulte [Administrar fuentes](../inventory-management/sources-manage.md).

## Asignar un origen para un producto

1. Haga clic en **[!UICONTROL Assign Source]**.

1. Seleccione la casilla de verificación de los orígenes necesarios.

1. Haga clic en **[!UICONTROL Done]**.

1. Seleccione **[!UICONTROL Source Item Status]** e introduzca los valores **[!UICONTROL Qty]** y **[!UICONTROL Notify Qty]** según sea necesario.

1. Haga clic en **[!UICONTROL Save]** para guardar los cambios.

![Vista de orígenes](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Referencia de campo

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Name] | El nombre único de un origen. |
| [!UICONTROL Source Status] | Determina si el producto está habilitado o deshabilitado en el catálogo. |
| [!UICONTROL Source Item Status] | Determina la disponibilidad actual del producto. Opciones:<br />**[!UICONTROL In Stock]**- Hace que el producto esté disponible para la compra.<br />**[!UICONTROL Out of Stock]** - A menos que se activen los pedidos pendientes, impide que el producto esté disponible para la compra y elimina el listado del catálogo. |
| [!UICONTROL Qty] | Cantidades de stock disponibles para cada origen. |
| [!UICONTROL Notify Qty] | Un importe para _Notificar por cantidad_ para este origen específico si `Notify Quantity Use Default` no está seleccionado. |
| [!UICONTROL Notify Qty Use Default] | Indica que se debe usar la configuración predeterminada para _Notificar por cantidad_ en el inventario avanzado del producto o la configuración global de la tienda. Para obtener más información acerca de la configuración de inventario avanzada de su producto, consulte [Configurar opciones de producto avanzadas](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Para un origen asignado, haga clic en **[!UICONTROL Unassign]** para que el origen no esté disponible para el producto. Para un origen no asignado, haga clic en **[!UICONTROL Assign Sources]** para que un origen esté disponible para el producto. Para obtener más información acerca de las opciones de [!UICONTROL Assign Sources], consulte [Asignación de orígenes por producto](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}

