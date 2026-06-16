---
title: Almacenar crédito
description: El crédito de tienda es un importe que se restaura en una cuenta de cliente y que se puede utilizar para pagar compras o reembolsos en efectivo.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# Almacenar crédito

{{ee-feature}}

El crédito de tienda es una cantidad que se restaura en una cuenta de cliente. Los clientes pueden utilizar el crédito de su tienda para pagar las compras, y los administradores pueden utilizar el crédito de la tienda para los reembolsos en efectivo. Los saldos de las tarjetas regalo se pueden acreditar en la cuenta del cliente, en lugar de utilizar el código de la tarjeta regalo para compras futuras.

Después de pagar y facturar un pedido, el pedido, o una parte de él, se puede reembolsar mediante [la emisión de una nota de crédito](../stores-purchase/credit-memo-create.md). Una nota de abono difiere de una devolución porque el importe del abono se restaura en la cuenta del cliente, donde se puede utilizar para compras futuras. A veces, se puede realizar un reembolso al mismo tiempo que se emite una nota de abono y aplicarlo al crédito del saldo del almacén del cliente. La cantidad de crédito de tienda disponible en la cuenta del cliente se especifica en la configuración.

>[!NOTE]
>
>El método de pago [_Cierre de compra con subtotal cero_](../stores-purchase/zero-subtotal-checkout.md) debe estar habilitado en caso de que el crédito de la tienda cubra el total del pedido.

## Flujo de trabajo de crédito de tienda

1. **Inicio de sesión del cliente**: el cliente inicia sesión en su cuenta antes de comenzar el proceso de cierre de compra.

1. **Usar tienda** - Crédito Durante el paso de [!UICONTROL _Revisión y pagos_] del proceso de pago, el cliente selecciona [!UICONTROL _Usar crédito de tienda_] como opción de pago. El saldo disponible se muestra entre paréntesis. Si el saldo disponible es mayor que el total general, las demás formas de pago ya no se mostrarán.

1. **Crédito aplicado al pedido** - La cantidad de crédito de tienda que se aplica al pedido aparece con los totales del pedido y se resta del total general.

1. **Saldo del cliente ajustado** - El saldo disponible del cliente se ajusta cuando se realiza el pedido.
