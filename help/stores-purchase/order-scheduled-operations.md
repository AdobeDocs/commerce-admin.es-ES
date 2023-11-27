---
title: Operaciones de pedido programado
description: Obtenga información acerca de las operaciones de pedidos programados y la configuración de cron de pedidos que admiten esta funcionalidad.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Operaciones de pedido programado

Uso [Cron](../systems/cron.md) trabajos para programar las siguientes tareas de procesamiento de pedidos:

![cuadrícula de pedidos](./assets/orders-grid.png){width="700" zoomable="yes"}

## Establecer duración de orden de pago pendiente

La duración de los pedidos con pagos pendientes está determinada por la variable _Configuración de pedidos de Cron_ configuración. El valor predeterminado es 480 minutos, es decir, ocho horas.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Orders Cron Settings]** sección.

   ![Configuración de pedidos de Cron](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, introduzca el número de minutos antes de que caduque un pago pendiente.

1. Haga clic **[!UICONTROL Save Config]**.

## Habilitar las actualizaciones y reindexaciones programadas de la cuadrícula

La configuración de Configuración de rejilla programa actualizaciones para las siguientes rejillas de gestión de pedidos y reindexa los datos según lo programado por [Cron](../systems/cron.md):

- [Pedidos](orders.md#orders-workspace)
- [Facturas](invoices.md)
- [Envíos](shipments.md)
- [Notas de abono](credit-memos.md)

Al programar estas tareas, puede evitar los bloqueos que se producen cuando se guardan los datos y reducir el tiempo de procesamiento. Cuando está habilitado, las actualizaciones solo se realizan durante el trabajo cron programado. Para obtener los mejores resultados, Cron debe configurarse para ejecutarse una vez cada minuto.

**_Para habilitar las actualizaciones y la reindexación:_**

Cuándo [Modo de producción](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (el modo predeterminado utilizado en Adobe Commerce en la infraestructura en la nube) está habilitado, ejecute el siguiente comando:

``bin/magento config:set dev/grid/async_indexing 1``

Cuándo [Modo predeterminado](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) está activada, complete los siguientes pasos:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Developer]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Grid Settings]** sección.

1. Establecer **[!UICONTROL Asynchronous Indexing]** hasta `Enable`.

   ![Configuración de cuadrícula](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save Config]**.
