---
title: Creación de envíos de varios orígenes
description: Descubra cómo los comerciantes de varios orígenes pueden crear y enviar envíos.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Creación de envíos de varios orígenes

Con [!DNL Inventory Management], envíe uno o más envíos ya que tiene inventario. Para generar envíos adicionales según sea necesario, repita estas instrucciones utilizando las cantidades y fuentes recomendadas o introducidas manualmente. Estas instrucciones detallan cómo los comerciantes de varias fuentes envían envíos. Los comerciantes de un solo origen envían envíos sin estos pasos adicionales (consulte [Crear un envío](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} en la guía del usuario principal).

Al crear envíos, utilice el algoritmo de selección de Source para las recomendaciones calculadas. Siga y utilice estas recomendaciones o establezca las cantidades por fuente, generando envíos personalizados. Controle el inventario saliente para cada pedido, configurando las cantidades a deducir, enviando uno o más envíos y entregando el stock y los pedidos pendientes a medida que el inventario esté disponible. Para cada artículo de línea del pedido, introduzca una cantidad que deducir de la cantidad de origen.

Es posible que desee enviar envíos parciales a:

- Satisfacer pedidos pendientes a medida que llega el inventario

- Equilibrar deducciones de inventario entre orígenes

A medida que introduce envíos, las cantidades de inventario disponible deducirán los importes introducidos. De hecho, las reservas se convierten en deducciones de cantidad real.

## Creación de un envío

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el pedido y abra en el modo de vista.

1. Si el pedido se ha pagado y facturado y está listo para enviarse, haga clic en **[!UICONTROL Ship]**.

1. Complete la selección de Source para enviar productos por origen:

   - Para ver las recomendaciones de envío, haga clic en **[!UICONTROL Source Selection Algorithm]** y seleccione un algoritmo.

     | Algoritmo | Descripción |
     |--|--|
     | [Prioridad de Source](source-priority-algorithm.md) | Recomienda envíos de fuentes según los pedidos de fuentes asignadas a la reserva. |
     | [Prioridad de distancia](distance-priority-algorithm.md) | Recomienda envíos de fuentes más cercanas a la dirección de envío en función de la distancia física o el tiempo más corto para la entrega. |

     >[!IMPORTANT]
     >
     >Cuando se usa el algoritmo de prioridad de distancia para el envío y las rutas y los datos no se devuelven para el [modo de cálculo](distance-priority-algorithm.md) seleccionado (conducir, andar en bicicleta o caminar) para un envío, el SSA toma como valor predeterminado la prioridad de Source. También se recomienda establecer la [prioridad de orígenes por existencia](stocks-prioritize-sources.md).


   - Para **[!UICONTROL Select a Source to Ship from]**, seleccione un origen para enviar un envío.

   - Para cada elemento de línea, conserve la cantidad recomendada o escriba una cantidad específica en **[!UICONTROL Qty to Deduct]**. Este valor especifica la cantidad que se deduce del inventario del origen seleccionado.

   - Haga clic en **[!UICONTROL Proceed to Shipment]**.

     ![Seleccione un Source e introduzca una cantidad](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Revise la página _[!UICONTROL New Shipment]_&#x200B;e introduzca los cambios adicionales que sean necesarios.

   La sección _[!UICONTROL Inventory]_&#x200B;muestra el origen, el envío de productos, la cantidad total solicitada y la cantidad a enviar.

   ![Detalles de inventario para el envío, por ejemplo, envío parcial](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Haga clic **[!UICONTROL Submit Shipment]** para completar.
