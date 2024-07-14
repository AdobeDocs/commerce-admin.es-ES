---
title: Actualización de un pedido
description: Obtenga información sobre cómo actualizar el pedido de un cliente en Admin.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Actualización de un pedido

Al ayudar a un cliente que ha realizado un pedido, debe determinar el estado del pedido. Las opciones disponibles para un pedido de `Pending` son diferentes de las opciones para un pedido de `Processing`. Para obtener más información, vea [Procesar un pedido](order-processing.md).

## Pedidos pendientes

Una vez que un cliente realiza un pedido, pero antes de que se reciba el pago, el pedido se encuentra en el estado `Pending`. Puede editar el pedido, ponerlo en espera o cancelarlo por completo. La barra de botones de un pedido pendiente enumera las acciones disponibles para un pedido.

![Opciones de pedidos pendientes](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Si modifica partes sustanciales de un pedido, el pedido original se cancela y se genera un nuevo pedido. Sin embargo, puede cambiar la dirección de facturación o envío sin generar un nuevo pedido.

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página Pedidos sin guardar los cambios. |
| **[!UICONTROL Login as Customer]** | Permite que un usuario administrador ayude a los clientes con sus pedidos. |
| **[!UICONTROL Cancel]** | Cancela el pedido pendiente. |
| **[!UICONTROL Send Email]** | Envía un mensaje de correo electrónico sobre la orden pendiente al cliente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Cambia el estado de la solicitud pendiente a `On Hold`. Para liberar la suspensión, elija _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Crea una [factura](invoices.md#create-an-invoice) del pedido pendiente convirtiendo el pedido en una factura y cambia el estado del pedido a `processing`. |
| **[!UICONTROL Ship]** | Crea un registro de [envío](shipments.md#create-a-shipment) para el pedido. |
| **[!UICONTROL Reorder]** | Crea una nueva orden pendiente que es un duplicado de la orden pendiente actual. |
| **[!UICONTROL Edit]** | Abre un pedido pendiente en modo de edición. El botón Editar solo está disponible para pedidos pendientes o para pedidos basados en [ofertas](../b2b/quotes.md) negociadas. |

{style="table-layout:auto"}

## Procesamiento de pedidos

Un pedido entra en un estado `Processing` cuando:

* El pago de un pedido se recibe/captura y la factura se genera, cuando la acción de pago se establece en `Authorize and Capture`.
* Una transacción de pedido está autorizada, pero el pago aún no se ha capturado, cuando la acción de pago se ha establecido en `Authorize`.

La [configuración de acción de pago](../configuration-reference/sales/payment-methods.md#payment-actions) determina qué acciones de pedido están disponibles después de que se cree un pedido.

No puede cambiar sustancialmente un pedido de `Processing`, pero puede editar la dirección de facturación y envío.

![Opciones de orden de procesamiento](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Cuando la acción de pago del método de pago está establecida en `Authorize and Capture`, se crea automáticamente una factura cuando el cliente realiza un pedido. En esta circunstancia, puedes reembolsar fondos usando un [abono](credit-memo-create.md), pero no puedes [cancelar](#cancel-a-pending-order) ni [anular](#void-a-processing-order) el pedido.

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página Pedidos sin guardar los cambios. |
| **[!UICONTROL Send Email]** | Envía un correo electrónico sobre el pedido al cliente. |
| **[!UICONTROL Void]** | [Anula](#void-a-processing-order) una transacción de pedido o una transacción de pedido parcial. |
| **[!UICONTROL Credit Memo]** | Inicia el proceso para crear un [abono](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Cambia el estado del pedido de ventas a `On Hold`. Para liberar la retención en el pedido de ventas, elija _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Crea un nuevo pedido pendiente basado en el pedido actual. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) inicia el proceso para [devolver](returns.md) uno o más elementos del pedido. |

{style="table-layout:auto"}

## Anular un pedido de procesamiento

Cuando un pedido sigue en estado `Processing` y la integración de pago está establecida en `Authorize` (no en `Authorize and Capture`), solo puede anular una transacción o cancelar un pedido. [Al cancelar un pedido](#cancel-a-pending-order) también se anula la autorización.

Cuando se realiza un pedido utilizando un método de pago con la acción de pago establecida en `Authorize and Capture`, puede devolver los fondos a través de una nota de crédito, pero no puede cancelarla porque se factura y se captura el pago.

Tu forma de pago determina tus acciones de pago disponibles. Consulte [Acciones de pago](../configuration-reference/sales/payment-methods.md#payment-actions) para obtener más información.

**_Para anular un pedido:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. En la columna **[!UICONTROL Action]** para editar el orden, haga clic en **[!UICONTROL View]**.

1. Haga clic en **[!UICONTROL Void]** para anular el pedido.

1. Cuando se le solicite, haga clic en **[!UICONTROL OK]** para anular el pedido.

Puede emitir cualquier reembolso necesario utilizando [nota de crédito](credit-memo-create.md) después de capturar los fondos. También puede crear una [autorización de devolución de mercancía (RMA)](returns.md) para devoluciones de productos. Para obtener más información, consulte [Procesar un pedido](order-processing.md).

## Editar una solicitud pendiente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. En la columna **[!UICONTROL Action]** para editar el orden, haga clic en **[!UICONTROL View]**.

1. Haga clic en **[!UICONTROL Edit]**.

   ![Editar pedido](./assets/order-edit.png){width="600" zoomable="yes"}

1. Cuando se le solicite, haga clic en **[!UICONTROL OK]** para continuar editando.

1. Actualice el pedido según sea necesario.

1. Aplique los cambios:
   * Para guardar los cambios realizados en la dirección de facturación o envío, haga clic en **[!UICONTROL Save]**.
   * Para guardar los cambios realizados en los elementos de línea y volver a procesar el pedido, haga clic en **[!UICONTROL Submit Order]**.

## Realizar un pedido en espera

Si el método de pago preferido del cliente no está disponible o si el artículo está temporalmente agotado, puede retener el pedido.

1. En la cuadrícula _Pedidos_, busque el pedido `Pending` que desea poner en espera.

1. En la columna _Acción_, haga clic en **[!UICONTROL View]**.

1. Haga clic en **[!UICONTROL Hold]** para poner el pedido en espera.

Para quitar la retención de un pedido, vuelva a editarlo y haga clic en **[!UICONTROL Unhold]**.

## Cancelar una solicitud pendiente

Al cancelar un pedido, su estado cambia de `Pending` a `Canceled`.

1. En la cuadrícula _[!UICONTROL Orders]_, busque la orden pendiente que se va a cancelar.

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL View]**.

1. Haga clic en **[!UICONTROL Cancel]** para cancelar el pedido.

El estado del pedido ahora es `Canceled`.
