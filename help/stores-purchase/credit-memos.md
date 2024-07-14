---
title: Notas de abono
description: Obtenga información sobre los abonos y cómo se utilizan para emitir un reembolso parcial o completo.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Notas de abono

Un _abono_ es un documento que muestra el importe que se debe al cliente por un reembolso total o parcial. El importe puede aplicarse a una compra o reembolsarse al cliente. Puede imprimir una nota de abono para un único pedido o para varios pedidos como un lote. Para poder imprimir una nota de abono, primero debe generarse para el pedido. La página _Notas de crédito_ muestra las notas de crédito que se han emitido a los clientes.

![Notas de abono](./assets/credit-memos.png){width="700" zoomable="yes"}

## Método de reembolso

El [método de pago](payments.md) del pedido determina, en cierta medida, el método por el cual se reembolsa un pedido.

Puede reembolsar pedidos de tres formas:

- Crédito de cuenta: los pedidos pagados mediante una cuenta de crédito se pueden reembolsar como un crédito de cuenta:
   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) [Crédito de tienda](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponible con Adobe Commerce B2B) [Pago con cuenta](../b2b/enable-basic-features.md#configure-payment-on-account) (método sin conexión)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponible con Adobe Commerce B2B) [Crédito de la compañía](../b2b/credit-company.md)
- [Reembolso en línea](payments.md#online-payment-methods): los pedidos pagados con tarjeta de crédito a través de una pasarela de pago, como PayPal o Braintree, se reembolsan en línea a través del procesador de pagos.
- [Reembolso sin conexión](payments.md#offline-payment-methods): los pedidos pagados mediante Pago contra reembolso ([COD](cash-on-delivery.md)) o mediante [cheque o giro postal](check-money-order.md) se reembolsan sin conexión.

Puedes emitir un reembolso sin conexión o un crédito de cuenta (si está activado) para cualquier forma de pago.

Un pedido pagado mediante Pago contra reembolso ([COD](cash-on-delivery.md)) o mediante [cheque o giro postal](check-money-order.md) se devuelve sin conexión.

## Flujo de trabajo de reembolso

1. **Acción de pago** - Si la configuración de [Acción de pago](credit-memo-create.md#payment-action-setting) está establecida en `Authorize`, debe generar una factura antes de crear una nota de abono. Continúe con el paso 2. Si se establece en `Authorize and Capture`, ya se ha generado una factura. Continúe con el paso 3.

1. **Generar factura** - [Cree una factura](invoices.md#create-an-invoice) para el pedido, de modo que pueda enviar un reembolso al cliente a través de un abono.

1. **Crear nota de crédito** - [Emitir una nota de crédito](credit-memo-create.md) en el administrador para una [compra de crédito](credit-memo-create.md#issue-a-refund-for-a-credit-purchase), o un [cheque o giro postal](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Descripciones de columna

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Select] | Seleccione las casillas de verificación de los elementos de nota de abono que deben estar sujetos a una acción o utilice el control de selección en el encabezado de la columna. Opciones: `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | Identificador numérico único que se asigna cuando se envía una solicitud de nota de abono. |
| [!UICONTROL Created] | La fecha y la hora en que el comprador envió por primera vez la solicitud de nota de abono. |
| [!UICONTROL Order#] | ID del pedido cuyos productos se están devolviendo. |
| [!UICONTROL Order Date] | La fecha y la hora en que el comprador hizo un pedido. |
| [!UICONTROL Bill-to Name] | El nombre de la persona responsable de pagar el pedido. |
| [!UICONTROL Status] | Indica el estado actual de una solicitud de abono. |
| [!UICONTROL Refunded] | El importe total reembolsado del pedido. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Abre la solicitud de una nota de abono y mantiene un registro de la negociación entre el comprador y el vendedor. |
| [!UICONTROL Order Status] | Indica el estado del pedido. |
| [!UICONTROL Purchased From] | Indica el sitio web, la tienda y la vista de la tienda donde se realizó el pedido. |
| [!UICONTROL Billing Address] | La dirección de facturación del cliente que realizó el pedido. |
| [!UICONTROL Shipping Address] | La dirección a la que se enviará el pedido. |
| [!UICONTROL Customer Name] | El nombre y los apellidos del cliente que realizó el pedido. |
| [!UICONTROL Email] | La dirección de correo electrónico de la persona que realizó el pedido. |
| [!UICONTROL Customer Group] | El grupo de clientes al que está asignado el cliente. |
| [!UICONTROL Payment Method] | El método de pago que se utilizará para el pago. |
| [!UICONTROL Shipping Information] | El método que se utilizará para enviar el pedido. |
| [!UICONTROL Subtotal] | El subtotal del pedido, sin envío ni manipulación, y los impuestos. |
| [!UICONTROL Shipping & Handling] | El importe cobrado por el envío y la manipulación. |
| [!UICONTROL Adjustment Refund] | El importe que se añade al importe total reembolsado como un reembolso adicional. |
| [!UICONTROL Adjustment Fee] | El importe que se resta del importe total reembolsado. |
| [!UICONTROL Grand Total] | El total del pedido. |

{style="table-layout:auto"}
