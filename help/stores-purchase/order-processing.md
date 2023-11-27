---
title: Flujo de trabajo y procesamiento de pedidos
description: Obtenga información sobre el flujo de trabajo de pedidos, el estado que se aplica en cada paso y cómo mover las solicitudes a través de este proceso.
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1733'
ht-degree: 0%

---

# Flujo de trabajo y procesamiento de pedidos

Cuando un cliente realiza un pedido, se crea un pedido de venta como un registro temporal de la transacción. En la cuadrícula Pedidos, los pedidos de venta tienen inicialmente el estado &quot;Pendiente&quot; y se pueden cancelar en cualquier momento hasta que se procese el pago. Una vez confirmado el pago, el pedido se puede facturar y enviar.

**Paso 1: Realizar el pedido** - El proceso de pago comienza cuando el comprador hace clic **[!UICONTROL Go to Checkout]** en la página del carro de compras o [reordenar](reorders-allow.md) directamente desde su cuenta de cliente.

**Paso 2: Pedido pendiente** - El estado inicial del pedido de ventas es `Pending`. En este estado, el pago no se ha procesado y el pedido se puede editar o cancelar. Este estado se produce cuando el método de pago está configurado para el modo de autorización.

**Paso 3: Recibir pago** - El estado del pedido cambia a `Processing` cuando el pago se recibe o se autoriza. Según la forma de pago, podría recibir una notificación cuando la transacción se autorice o procese. Este estado se produce automáticamente cuando el método de pago se configura para el modo de captura o venta por intención.

**Paso 4: Orden de factura** - Un pedido se factura normalmente después de recibir el pago. El método de pago determina qué opciones de facturación son necesarias para el pedido. Una vez generada y enviada la factura, se envía una copia al cliente. Si la forma de pago está configurada con `capture` o `intent sale` acción de pago, se genera automáticamente una factura cuando se autoriza y captura el pago.

>[!NOTE]
>
>Las facturas no se crean automáticamente para los pedidos realizados utilizando `Gift Card`, `Store Credit`, `Reward Points`u otros métodos de pago sin conexión.

**Paso 5: Reservar un solo envío** - El estado del pedido cambia a `Complete` cuando se completa el detalle del envío, se reserva el envío y se establece el envío. El requisito de envío se cumple con un albarán impreso y una etiqueta de envío para la _Notificar listo para recoger_ está seleccionado (método de envío en tienda). El cliente recibe una notificación y se envía el paquete. Si se utilizan números de seguimiento, se puede realizar el seguimiento del envío desde la cuenta del cliente.

>[!NOTE]
>
>Para obtener más información sobre el estado del pedido y las opciones de configuración del método de pago, consulte [Estado del pedido](order-status.md) y [Pagos](payments.md).

## Ver un pedido

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Busque el orden en la cuadrícula.

1. En el _[!UICONTROL Action]_, haga clic en **[!UICONTROL View]**.

1. Comprobar estado del pedido:

   - A `Pending` el pedido puede modificarse, retenerse, cancelarse o facturarse y enviarse.

   - A `Processing` El pedido ya no se puede editar ni cancelar de forma sustancial, pero sí editar la dirección de facturación y envío.

   - A `Completed` el orden se puede reordenar.

El correo electrónico del cliente se puede editar en cualquier momento del flujo de trabajo del pedido editando el cliente. El correo electrónico no se puede editar si un invitado ha realizado el pedido.

El panel izquierdo de una solicitud abierta proporciona acceso a diferentes tipos de información relacionados con la solicitud.

![Ver pedido](./assets/order-view.png){width="700" zoomable="yes"}

## Procesamiento de un pedido

Cuando un cliente realiza un pedido, se crea un pedido de venta como un registro temporal de la transacción. El pedido de ventas tiene un estado de `Pending` hasta recibir el pago. Mientras está en `Pending` estado, los pedidos se pueden editar o cancelar hasta el momento en que se reciba el pago y se genere una factura. Una manera fácil de pensarlo es que los pedidos se convierten en facturas y las facturas se convierten en envíos. La cuadrícula Pedidos enumera todas las solicitudes, independientemente de su ubicación en el flujo de trabajo. Para aprender a ayudar a los clientes con un pedido, consulte [Actualización de un pedido](order-update.md).

![Pedidos](./assets/orders-grid.png){width="700" zoomable="yes"}

Para abrir un `Pending` Haga clic en el botón **[!UICONTROL Edit]** en la esquina superior derecha.

>[!NOTE]
>
>Los pedidos solo se pueden editar mientras se encuentra en `Pending` estado. El botón Editar no está visible para pedidos en un estado diferente o para pedidos basados en un [presupuesto negociado](../b2b/quotes.md).

![Editar pedido de ventas](./assets/order-pending.png){width="600" zoomable="yes"}

Revise las siguientes secciones del pedido de venta, utilizando las descripciones de los campos como referencia.

### Descripciones de vistas de pedidos

| Ficha | Descripción |
|--- |--- |
| [!UICONTROL Information] | Muestra información detallada sobre el pedido y la cuenta, incluidas las direcciones de facturación y envío, los métodos de pago y envío, los artículos, los pedidos, los totales y las notas. |
| [!UICONTROL Invoices] | Muestra todas las facturas asociadas con el pedido. |
| [!UICONTROL Credit Memos] | Muestra todas las notas de abono asociadas al pedido. |
| [!UICONTROL Shipments] | Muestra todos los registros de envío asociados al pedido. |
| [!UICONTROL Comments History] | Enumera todas las notas relacionadas con el pedido. |

{style="table-layout:auto"}

>[!NOTE]
>
>Un usuario administrador debe tener **[!UICONTROL Sales / Archive]** [permissions](../systems/permissions-user-roles.md) para que su ámbito de función vea el _Facturas_, _Notas de abono_, y _Envíos_ Ordenar pestañas.

### Barra de botones

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página Pedidos sin guardar los cambios. |
| **[!UICONTROL Cancel]** | Cancela el pedido de venta. |
| **[!UICONTROL Send Email]** | Envía un correo electrónico sobre el pedido al cliente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Cambia el estado del pedido de venta a `On Hold`. Para liberar la retención en el pedido de venta, seleccione **[!UICONTROL Unhold]**. |
| **[!UICONTROL Invoice]** | Crea una factura a partir del pedido de venta convirtiendo el pedido en una factura. |
| **[!UICONTROL Ship]** | Crea un registro de envío para el pedido. |
| **[!UICONTROL Notify Order is Ready for Pickup]** | Solo aparece cuando un pedido se realiza como envío en tienda. Notifica al cliente que el pedido está listo para recoger. |
| **[!UICONTROL Reorder]** | Crea un pedido de ventas basado en el pedido actual. |
| **[!UICONTROL Edit]** | Abre un pedido pendiente en modo de edición. El botón Editar no está visible para pedidos con un estado de `Processing`o pedidos basados en ofertas negociadas. |

{style="table-layout:auto"}

### Cancelar un pedido

Puede [cancelar](order-update.md) pedidos que aún no se han facturado. A [nota de crédito](credit-memos.md) se debe emitir si un cliente desea cancelar un pedido después de facturarlo (se captura el pago).

Si un pedido es `Pending` o `Processing` y el pago no se captura o no se captura por completo, puede [Anular el pedido](#void-an-order) en lugar de cancelarlo.

Para restaurar un pedido cancelado, haga clic en **[!UICONTROL Reorder]** y se crea un nuevo pedido con el estado `Pending`.

>[!NOTE]
>
>La cancelación de un pedido también produce un vacío, pero la anulación de un pedido no déclencheur una cancelación.

### Anular un pedido

Solo los pedidos de venta que no se facturan tienen un estado de `Processing`, y a [configuración de integración de pagos de `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions), puede ser [anulado](order-update.md#void-a-processing-order). Una vez anulada una solicitud, puede cancelarla.

### [!UICONTROL Order and Account Information]

![Información de pedido y cuenta](./assets/order-account-information.png){width="600" zoomable="yes"}

#### Información del pedido

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Order Number] | El número de pedido aparece en la parte superior del pedido de ventas, seguido de una nota que indica si se envió el correo electrónico de confirmación. |
| [!UICONTROL Order Date] | La fecha y la hora en que se realizó el pedido. |
| [!UICONTROL Purchased From] | Indica el sitio web, la tienda y la vista de la tienda donde se realizó el pedido. |
| [!UICONTROL Placed from IP] | Indica la dirección IP del equipo desde el que se realizó el pedido. |
| [!UICONTROL Order Placed from Quote] | ![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B para Adobe Commerce) Indica el [citar](../b2b/quotes.md) a partir de la cual se generó el pedido, si corresponde. El nombre de la oferta está vinculado a la oferta. |

{style="table-layout:auto"}

#### Información de cuenta

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Customer Name] | El nombre del cliente o comprador que realizó el pedido. El nombre del cliente está vinculado al perfil del cliente. |
| [!UICONTROL Email] | La dirección de correo electrónico del cliente o comprador. La dirección de correo electrónico está vinculada para abrir un nuevo mensaje. |
| [!UICONTROL Customer Group] | El nombre del grupo de clientes o del catálogo compartido al que está asignado el cliente. |
| [!UICONTROL Company Name] | ![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B para Adobe Commerce) El nombre de la empresa con la que está asociado el comprador y en cuyo nombre se realiza el pedido. El nombre de la empresa está vinculado al [perfil de empresa](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![Información de dirección](./assets/order-address-information.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Billing Address] | El nombre del cliente o comprador que realizó el pedido, seguido de la dirección de facturación, el número de teléfono y el código de identificación del cliente. [IVA](vat.md), si procede. El número de teléfono está vinculado al marcado automático en un dispositivo móvil. |
| [!UICONTROL Shipping Address] | El nombre de la persona a cuya atención debe enviarse el pedido, seguido de la dirección de envío y el número de teléfono. El número de teléfono está vinculado al marcado automático en un dispositivo móvil. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![Pago y método de envío](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Payment Information] | El método de pago que se va a utilizar para el pedido y el número de pedido de compra, si corresponde, seguido de la divisa utilizada para realizar el pedido. Si el pedido se carga al crédito de la empresa mediante [Pago a cuenta](../b2b/enable-basic-features.md#configure-payment-on-account), se indica el importe cargado en la cuenta. |
| [!UICONTROL Shipping & Handling Information] | El método de envío que se va a utilizar y cualquier tarifa de manipulación que sea aplicable. |

{style="table-layout:auto"}

### Revisar artículos pedidos

![Elementos pedidos](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

En el **[!UICONTROL Order Total]** , haga lo siguiente:

1. Introduzca una **[!UICONTROL Comment]** para incluirla en el pedido.

1. Si desea enviar el comentario por correo electrónico al cliente, seleccione la **[!UICONTROL Notify Customer by Email]** casilla de verificación

1. Si desea que el comentario sea visible en la cuenta del cliente, seleccione la opción **[!UICONTROL Visible on Storefront]** casilla de verificación

   ![Total de pedido](./assets/order-total.png){width="600" zoomable="yes"}

1. Si está listo para facturar el pedido, haga clic en **[!UICONTROL Invoice]** y siga las instrucciones para [crear una factura](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Product] | El nombre del producto, SKU y opciones, si corresponde. |
| [!UICONTROL Item Status] | Indica el estado del elemento. Valor: `Ordered` |
| [!UICONTROL Original Price] | El precio de catálogo original del artículo antes de los descuentos. |
| [!UICONTROL Price] | El precio de compra del artículo. Este valor refleja cualquier descuento aplicado al artículo desde el catálogo compartido, si corresponde. |
| [!UICONTROL Qty] | La cantidad pedida. |
| [!UICONTROL Subtotal] | El subtotal es el precio de compra multiplicado por la cantidad. |
| [!UICONTROL Tax Amount] | El importe del impuesto que se aplica al artículo como valor decimal. |
| [!UICONTROL Tax Percent] | Porcentaje de impuestos aplicados a este artículo como porcentaje. |
| [!UICONTROL Discount Amount] | El descuento que se aplica a este artículo. El valor de descuento es cero si el pedido se basa en una oferta. |
| [!UICONTROL Row Total] | El total del artículo de línea, incluidos los impuestos aplicables que vencen en el nivel de producto, menos los descuentos. |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Status] | Muestra el estado del pedido de venta. |
| [!UICONTROL Comment] | Cuadro de texto que se utiliza para escribir un comentario para el cliente que acompaña al pedido. <br/>**[!UICONTROL Notify Customer by Email]**: seleccione la casilla de verificación si desea enviar el comentario al cliente como un correo electrónico independiente.<br/>**[!UICONTROL Visible on Storefront]** - Seleccione la casilla de verificación si desea que el comentario sea visible desde la cuenta del cliente. <br/>**[!UICONTROL Submit Comment]**: envía el comentario y lo envía por correo electrónico, si corresponde. |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Shipping & Handling] | El importe cobrado por los gastos de envío y manipulación. |
| [!UICONTROL Tax] | El importe del impuesto aplicado al pedido, si corresponde. |
| [!UICONTROL Grand Total] | El total del pedido. |
| [!UICONTROL Total Paid] | El importe total pagado para el pedido, si corresponde. |
| [!UICONTROL Total Refunded] | El importe total reembolsado del pedido, si corresponde. |
| [!UICONTROL Total Due] | El importe total que vence. |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) El importe del crédito de tienda disponible que se aplica al pedido, si corresponde. |
| [!UICONTROL Catalog Total Price] | ![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B para Adobe Commerce) El precio total de los artículos de la oferta sin impuestos, según el precio del catálogo compartido o el catálogo estándar que se utiliza como base de la oferta. Si la divisa de visualización de la tienda difiere de la moneda base, el valor aparecerá en ambas divisas y la tienda se mostrará entre corchetes. |
| [!UICONTROL Negotiated Discount] | ![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B para Adobe Commerce) El descuento resultante de un presupuesto negociado entre el comprador y el vendedor. Si la divisa de visualización de la tienda difiere de la moneda base, el valor aparecerá en ambas divisas y la tienda se mostrará entre corchetes. |
| [!UICONTROL Subtotal] | ![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B para Adobe Commerce) El precio total del catálogo menos el descuento negociado. |

{style="table-layout:auto"}

## Demostración del procesamiento de pedidos

Vea este vídeo y obtenga más información sobre el procesamiento y el estado de los pedidos:

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12)
