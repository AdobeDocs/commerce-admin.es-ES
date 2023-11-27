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

Al ayudar a un cliente que ha realizado un pedido, debe determinar el estado del pedido. Las opciones disponibles para un `Pending` orden son diferentes de las opciones de un `Processing` pedido. Para obtener más información, consulte [Procesamiento de un pedido](order-processing.md).

## Pedidos pendientes

Después de que un cliente realice un pedido, pero antes de que se reciba el pago, el pedido se envía `Pending` estado. Puede editar el pedido, ponerlo en espera o cancelarlo por completo. La barra de botones de un pedido pendiente enumera las acciones disponibles para un pedido.

![Opciones de pedidos pendientes](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Si modifica partes sustanciales de un pedido, el pedido original se cancela y se genera un nuevo pedido. Sin embargo, puede cambiar la dirección de facturación o envío sin generar un nuevo pedido.

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página Pedidos sin guardar los cambios. |
| **[!UICONTROL Login as Customer]** | Permite que un usuario administrador ayude a los clientes con sus pedidos. |
| **[!UICONTROL Cancel]** | Cancela el pedido pendiente. |
| **[!UICONTROL Send Email]** | Envía un mensaje de correo electrónico sobre la orden pendiente al cliente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Cambia el estado de la orden pendiente a `On Hold`. Para liberar la retención, elija _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Crea un [factura](invoices.md#create-an-invoice) del pedido pendiente convirtiendo el pedido en una factura y cambia el estado del pedido a `processing`. |
| **[!UICONTROL Ship]** | Crea un [envío](shipments.md#create-a-shipment) registro para el pedido. |
| **[!UICONTROL Reorder]** | Crea una nueva orden pendiente que es un duplicado de la orden pendiente actual. |
| **[!UICONTROL Edit]** | Abre un pedido pendiente en modo de edición. El botón Editar solo está disponible para pedidos pendientes o para pedidos basados en pedidos negociados [comillas](../b2b/quotes.md). |

{style="table-layout:auto"}

## Procesamiento de pedidos

Un pedido introduce un `Processing` indicar cuándo:

* El pago de un pedido se recibe/captura y la factura se genera, cuando la acción de pago se establece en `Authorize and Capture`.
* Se autoriza una transacción de pedido, pero el pago aún no se captura, cuando la acción de pago se establece en `Authorize`.

El [configuración de acción de pago](../configuration-reference/sales/payment-methods.md#payment-actions) determina qué acciones de pedido están disponibles después de crear una solicitud.

No puede cambiar sustancialmente una `Processing` pedido, pero puede editar la dirección de facturación y envío.

![Opciones de orden de procesamiento](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Cuando la acción de pago del método de pago se establece en `Authorize and Capture`, se crea automáticamente una factura cuando el cliente realiza un pedido. En este caso, puede reembolsar fondos mediante una [nota de crédito](credit-memo-create.md), pero no puede [cancelar](#cancel-a-pending-order) o [anular](#void-a-processing-order) el pedido.

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página Pedidos sin guardar los cambios. |
| **[!UICONTROL Send Email]** | Envía un correo electrónico sobre el pedido al cliente. |
| **[!UICONTROL Void]** | [Vacíos](#void-a-processing-order) una transacción de pedido o una transacción de pedido parcial. |
| **[!UICONTROL Credit Memo]** | Inicia el proceso para crear un [nota de crédito](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Cambia el estado del pedido de venta a `On Hold`. Para liberar la retención en el pedido de venta, seleccione _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Crea un nuevo pedido pendiente basado en el pedido actual. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Inicia el proceso para [devolver](returns.md) uno o más elementos del pedido. |

{style="table-layout:auto"}

## Anular un pedido de procesamiento

Cuando un pedido sigue en un `Processing` y la integración de pagos se establece en `Authorize` (no `Authorize and Capture`), solo puede anular una transacción o cancelar una solicitud. [Cancelación de una solicitud](#cancel-a-pending-order) también anula la autorización.

Cuando se realiza un pedido utilizando un método de pago con la acción de pago configurada como `Authorize and Capture` puede reembolsar los fondos a través de una nota de abono, pero no puede cancelarla porque se ha facturado y se ha capturado el pago.

Tu forma de pago determina tus acciones de pago disponibles. Consulte [Acciones de pago](../configuration-reference/sales/payment-methods.md#payment-actions) para obtener más información.

**_Para anular una solicitud:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. En el **[!UICONTROL Action]** para editar el orden, haga clic en **[!UICONTROL View]**.

1. Clic **[!UICONTROL Void]** para anular el pedido.

1. En el mensaje, haga clic en **[!UICONTROL OK]** para anular el pedido.

Puede emitir cualquier reembolso necesario utilizando un [nota de crédito](credit-memo-create.md) después de haber capturado los fondos. También puede crear un [Autorización de devolución de mercancía (RMA)](returns.md) emitido para devoluciones de productos. Para obtener más información, consulte [Procesamiento de un pedido](order-processing.md).

## Editar una solicitud pendiente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. En el **[!UICONTROL Action]** para editar el orden, haga clic en **[!UICONTROL View]**.

1. Haga clic **[!UICONTROL Edit]**.

   ![Editar pedido](./assets/order-edit.png){width="600" zoomable="yes"}

1. En el mensaje, haga clic en **[!UICONTROL OK]** para continuar editando.

1. Actualice el pedido según sea necesario.

1. Aplique los cambios:
   * Para guardar los cambios realizados en la dirección de facturación o envío, haga clic en **[!UICONTROL Save]**.
   * Para guardar los cambios realizados en los elementos de línea y volver a procesar el pedido, haga clic en **[!UICONTROL Submit Order]**.

## Realizar un pedido en espera

Si el método de pago preferido del cliente no está disponible o si el artículo está temporalmente agotado, puede retener el pedido.

1. En el _Pedidos_ grid, busque la `Pending` el pedido que desea poner en espera.

1. En el _Acción_ , haga clic en **[!UICONTROL View]**.

1. Clic **[!UICONTROL Hold]** para poner el pedido en espera.

Para eliminar la retención de un pedido, vuelva a editarlo y haga clic en **[!UICONTROL Unhold]**.

## Cancelar una solicitud pendiente

La cancelación de un pedido cambia su estado de `Pending` hasta `Canceled`.

1. En el _[!UICONTROL Orders]_grid, busca la orden pendiente para cancelar.

1. En el _[!UICONTROL Action]_, haga clic en **[!UICONTROL View]**.

1. Clic **[!UICONTROL Cancel]** para cancelar la solicitud.

El estado del pedido es ahora `Canceled`.
