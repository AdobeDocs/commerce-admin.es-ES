---
title: Agregar stock de inventario
description: Aprenda a añadir existencias y asignar fuentes a canales de ventas (sitios web), proporcionando un vínculo directo a cantidades vendibles e inventarios de productos.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Añadir un stock

Las existencias asignan sus fuentes a canales de venta (o sitios web), lo que proporciona un vínculo directo a cantidades vendibles e inventarios de productos.

Al crear un inventario personalizado, puede asignar sitios web y fuentes. Las fuentes pueden incluir fuentes habilitadas y deshabilitadas. Por ejemplo, puede añadir un almacén a sus existencias, preparándose para abrir la ubicación para administrar el inventario y completar los envíos.

Después de agregar orígenes, debe priorizar el orden de los orígenes de arriba (primero) a abajo (último). Este pedido afecta a las recomendaciones durante el envío del pedido.

![Nuevo Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Agregar las existencias de inventario

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Haga clic en **[!UICONTROL Add New Stock]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General]** e introduzca un **[!UICONTROL Name]** único para identificar el nuevo inventario.

   ![Opciones de stock generales](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Sales Channels]** y seleccione **[!UICONTROL Websites]** donde este archivo esté disponible.

   Para una instalación multisitio, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada sitio web.

   >[!NOTE]
   >
   >Si selecciona un sitio web o canal de ventas asignado a otro inventario, se anula su asignación de ese inventario. Todas las Sales Channel que no estén asignadas a un inventario personalizado se asignan al inventario de stock predeterminado.

   ![opciones de Sales Channel para existencias](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Sources]** y haga lo siguiente para cualquier inventario que no sea el predeterminado:

   - Haga clic en **[!UICONTROL Assign Sources]**.

   ![Orígenes asignados](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Seleccione las casillas de verificación de todos los orígenes que desee asignar al inventario.

   >[!IMPORTANT]
   >
   >Si asigna el mismo origen a varias existencias, podría provocar una venta excesiva de los productos asignados a ese origen.

   - Haga clic en **[!UICONTROL Done]**.

     Los orígenes agregados se muestran en Orígenes asignados.

     ![Asignar orígenes a Stock](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Use ![Icono de orden](assets/icon-sort.png) para arrastrar y soltar los orígenes en una prioridad de arriba (primero) a abajo (último).

   El pedido de origen es importante cuando se envían pedidos.

   ![Ejemplo de orígenes asignados](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. En el menú _[!UICONTROL Save]_(![Flecha del menú](../assets/icon-menu-down-arrow-red.png)), elija **[!UICONTROL Save & Close]**.

## Descripciones de campos

| Campo | Descripción |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Nombre de la acción. Por ejemplo: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Define el [ámbito](../getting-started/websites-stores-views.md#scope-settings) de las existencias al asignar las existencias a sitios web específicos como _canales de ventas_. Seleccione uno o varios sitios web por acción. Cada sitio web solo puede asignarse a un inventario. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Asigna orígenes de inventario a este stock. Los orígenes personalizados no se pueden asignar a Stock predeterminado. |
| [!UICONTROL Assigned Sources] | Lista de orígenes asignados. Arrastre y suelte los orígenes utilizando ![Icono de ordenación](assets/icon-sort.png) en un pedido priorizado para el envío y el cumplimiento de pedidos.<br/><br/>**[!UICONTROL Code]**: ID de código único para el origen.<br/>**[!UICONTROL Name]**: nombre y descripción para el origen.<br/>**[!UICONTROL Unassign]**- Quitar el origen asignado de las existencias usando ![icono de papelera](../assets/icon-delete-trashcan-solid.png). |
