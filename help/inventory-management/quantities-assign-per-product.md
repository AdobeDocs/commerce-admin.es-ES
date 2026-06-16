---
title: Asignar cantidades de inventario por producto
description: Obtenga información sobre cómo actualizar las cantidades de inventario de su producto y rastrear las cantidades de stock disponibles y disponibles.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Asignar cantidades por producto

Después de agregar [orígenes](sources-assign-per-product.md), actualice las cantidades de inventario del producto. Estos valores hacen un seguimiento de las existencias disponibles.

Para ocultar el inventario de un origen de los envíos sin quitar el origen, establezca _[!UICONTROL Source Item Status]_&#x200B;en `Out of Stock`. Las opciones de SSA y envío solo acceden a los orígenes enumerados como `In Stock` con la cantidad de inventario disponible.

Todas las cantidades y orígenes actualizados se muestran en la cuadrícula del producto.

## Actualización de cantidades

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque y abra un producto en modo de edición.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Sources]**.

1. Establezca **[!UICONTROL Source Item Status]** en `In Stock`.

1. para actualizar la cantidad de existencias disponibles, escriba una cantidad para **[!UICONTROL Qty]**.

1. Para establecer una notificación para cantidades de inventario, siga uno de estos procedimientos:

   - Cantidad de notificación personalizada - Anule la selección de la casilla de verificación **[!UICONTROL Use Default]** e introduzca una cantidad en **[!UICONTROL Notify Qty]**.
   - Cantidad de notificación predeterminada: seleccione la casilla **[!UICONTROL Use Default]**. [!DNL Commerce] comprueba y usa la configuración de _[!UICONTROL Advanced Inventory]_&#x200B;o de la configuración del almacén global.

   ![Actualizar cantidades de productos por Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Realice una de las siguientes acciones para guardar:

   - Haga clic en **[!UICONTROL Save]**.

   - En el menú **[!UICONTROL Save]** (![Flecha del menú](../assets/icon-menu-down-arrow-red.png)), elija **[!UICONTROL Save & Close]**.


La cuadrícula de producto se actualiza con una lista de todos los orígenes y las cantidades relacionadas. Para los productos con más de cinco orígenes asignados, pase el ratón sobre la columna _[!UICONTROL Quantity per Source]_&#x200B;para ver la lista completa.

![Cantidades de productos por origen](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
