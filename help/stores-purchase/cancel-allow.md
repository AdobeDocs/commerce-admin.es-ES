---
title: Permitir orden de cancelación
description: Aprenda a proporcionar funciones de cancelación a sus clientes.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
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
