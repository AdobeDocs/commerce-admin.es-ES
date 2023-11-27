---
title: Asignar cantidades de inventario por producto
description: Obtenga información sobre cómo actualizar las cantidades de inventario de su producto y rastrear las cantidades de stock disponibles y disponibles.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Asignar cantidades por producto

Después de agregar [orígenes](sources-assign-per-product.md), actualice las cantidades de inventario del producto. Estos valores hacen un seguimiento de las existencias disponibles.

Para ocultar el inventario de origen de los envíos sin eliminar el origen, establezca _[!UICONTROL Source Item Status]_hasta `Out of Stock`. Las opciones de SSA y envío solo acceden a los orígenes enumerados como `In Stock` con la cantidad de inventario disponible.

Todas las cantidades y orígenes actualizados se muestran en la cuadrícula del producto.

## Actualización de cantidades

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque y abra un producto en modo de edición.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Sources]** sección.

1. Establecer **[!UICONTROL Source Item Status]** hasta `In Stock`.

1. para actualizar la cantidad de stock disponible, introduzca una cantidad para **[!UICONTROL Qty]**.

1. Para establecer una notificación para cantidades de inventario, siga uno de estos procedimientos:

   - Cantidad de notificación personalizada: anule la selección del **[!UICONTROL Use Default]** e introduzca una cantidad en **[!UICONTROL Notify Qty]**.
   - Cantidad de notificación predeterminada: seleccione **[!UICONTROL Use Default]** casilla de verificación [!DNL Commerce] comprueba y utiliza la configuración de _[!UICONTROL Advanced Inventory]_o la configuración del almacén global.

   ![Actualizar cantidades de productos por origen](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Realice una de las siguientes acciones para guardar:

   - Haga clic **[!UICONTROL Save]**.

   - En el **[!UICONTROL Save]** (![Flecha de menú](../assets/icon-menu-down-arrow-red.png)), seleccione **[!UICONTROL Save & Close]**.


La cuadrícula de producto se actualiza con una lista de todos los orígenes y las cantidades relacionadas. Para productos con más de cinco orígenes asignados, pase el ratón sobre el _[!UICONTROL Quantity per Source]_para ver la lista completa.

![Cantidades de productos por origen](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
