---
title: Asignar cantidades de inventario por producto
description: Defina las cantidades físicas actuales y los umbrales por origen en una página de productos para mantener la precisión de [!DNL Inventory Management] existencias vendibles.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%
---
# Asignar cantidades por producto

Después de agregar [orígenes](sources-assign-per-product.md), actualice las cantidades de inventario del producto. Estos valores hacen un seguimiento de las existencias disponibles.

Para ocultar el inventario de un origen de los envíos sin quitar el origen, establezca _[!UICONTROL Source Item Status]_en `Out of Stock`. Las opciones de SSA y envío solo acceden a los orígenes enumerados como `In Stock` con la cantidad de inventario disponible.

Todas las cantidades y orígenes actualizados se muestran en la cuadrícula del producto.

## Actualización de cantidades

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque y abra un producto en modo de edición.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Sources]**.

1. Establezca **[!UICONTROL Source Item Status]** en `In Stock`.

1. para actualizar la cantidad de existencias disponibles, escriba una cantidad para **[!UICONTROL Qty]**.

1. Para establecer una notificación para cantidades de inventario, siga uno de estos procedimientos:

   - Cantidad de notificación personalizada - Anule la selección de la casilla de verificación **[!UICONTROL Use Default]** e introduzca una cantidad en **[!UICONTROL Notify Qty]**.
   - Cantidad de notificación predeterminada: seleccione la casilla **[!UICONTROL Use Default]**. [!DNL Commerce] comprueba y usa la configuración de _[!UICONTROL Advanced Inventory]_o de la configuración del almacén global.

   ![Actualizar cantidades de productos por Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Realice una de las siguientes acciones para guardar:

   - Haga clic en **[!UICONTROL Save]**.

   - En el menú **[!UICONTROL Save]** (![Flecha del menú](../assets/icon-menu-down-arrow-red.png)), elija **[!UICONTROL Save & Close]**.


La cuadrícula de producto se actualiza con una lista de todos los orígenes y las cantidades relacionadas. Para los productos con más de cinco orígenes asignados, pase el ratón sobre la columna _[!UICONTROL Quantity per Source]_para ver la lista completa.

![Cantidades de productos por origen](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
