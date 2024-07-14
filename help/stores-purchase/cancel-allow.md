---
title: Permitir orden de cancelación
description: Aprenda a proporcionar funciones de cancelación a sus clientes.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
source-git-commit: a9d1dc4fe50e98f0f1dfc8ec204930e2cc885d6e
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Permitir orden de cancelación

Cuando está activada, puede cancelar un pedido directamente desde la cuenta del cliente. Cancelar está deshabilitado de forma predeterminada.

## Criterios para activar la cancelación de un pedido

- La opción de configuración _Permitir cancelar pedido_ debe estar habilitada.

- Si el pedido está en estado `Hold`, `Canceled`, `Complete` o `Closed`, la opción de cancelación se deshabilita en la tienda.

- Si alguno de los artículos del pedido se ha enviado, la opción de cancelación se desactiva en la tienda.

- Si hay algún artículo pagado, la opción de cancelación se activa y se crea el reembolso para ese artículo.

- Si el pedido está en estado `Pending` o `Processing`, la opción de cancelación se habilita en la tienda.

## Configure para permitir la cancelación del cliente y personalizar los motivos de cancelación

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y seleccione **[!UICONTROL Sales]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Order cancellation]**.

   ![Opciones de cancelación de pedidos](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Order cancellation through GraphQL]** en `Yes`.

   Esta configuración habilita la funcionalidad de cancelación desde la cuenta de cliente en la tienda.

1. En **[!UICONTROL Order Order cancellation reasons]** puede agregar, eliminar o modificar cualquier motivo de cancelación.

   Con esta configuración, los motivos de cancelación se muestran en la tienda al cliente cuando cancela un pedido.
Asegúrese de haber especificado al menos un motivo.

1. Haga clic en **[!UICONTROL Save Config]**.

## Cancelar desde la tienda

Un cliente puede iniciar la funcionalidad de cancelación para un pedido específico desde tres páginas:

- _Mis pedidos_ página

- _Vista de pedidos_ página

- _Página de Mi cuenta_

### Mis pedidos

El botón _Cancelar pedido_ se muestra en la página Mis pedidos si es posible cancelar el pedido.

![Ejemplo de tienda - Página Mis pedidos](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Página de vista de pedidos

El botón _Cancelar pedido_ se muestra en la página Ver pedido si el pedido se puede cancelar.

![Página de detalles del pedido](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mi cuenta

El botón _Cancelar pedido_ se muestra en la sección Pedidos recientes de la página Mi cuenta, si el pedido se puede cancelar.

![Página de Mi cuenta](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
