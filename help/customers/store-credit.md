---
title: Almacenar crédito
description: El crédito de tienda es un importe que se restaura en una cuenta de cliente y que se puede utilizar para pagar compras o reembolsos en efectivo.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Almacenar crédito

{{ee-feature}}

El crédito de tienda es una cantidad que se restaura en una cuenta de cliente. Los clientes pueden utilizar el crédito de su tienda para pagar las compras, y los administradores pueden utilizar el crédito de la tienda para los reembolsos en efectivo. Los saldos de las tarjetas regalo se pueden acreditar en la cuenta del cliente, en lugar de utilizar el código de la tarjeta regalo para compras futuras.

Después de pagar y facturar un pedido, el pedido, o una parte de él, puede ser reembolsado por [emisión de una nota de abono](../stores-purchase/credit-memo-create.md). Una nota de abono difiere de una devolución porque el importe del abono se restaura en la cuenta del cliente, donde se puede utilizar para compras futuras. A veces, se puede realizar un reembolso al mismo tiempo que se emite una nota de abono y aplicarlo al crédito del saldo del almacén del cliente. La cantidad de crédito de tienda disponible en la cuenta del cliente se especifica en la configuración.

>[!NOTE]
>
>El [_Cierre de compra con subtotal cero_](../stores-purchase/zero-subtotal-checkout.md) el método de pago debe estar habilitado en caso de que el crédito de la tienda cubra el total del pedido.

## Flujo de trabajo de crédito de tienda

1. **Inicio de sesión del cliente** - El cliente inicia sesión en la cuenta antes de iniciar el proceso de cierre de compra.

1. **Usar tienda** - Crédito durante el [!UICONTROL _Revisión y pagos_] paso del proceso de cierre de compra, el cliente selecciona [!UICONTROL _Usar crédito de tienda_] como opción de pago. El saldo disponible se muestra entre paréntesis. Si el saldo disponible es mayor que el total general, las demás formas de pago ya no se mostrarán.

1. **Crédito aplicado al pedido** - La cantidad de crédito de tienda que se aplica al pedido aparece con los totales del pedido y se resta del total general.

1. **Saldo del cliente ajustado** - El saldo disponible del cliente se ajusta cuando se realiza el pedido.
