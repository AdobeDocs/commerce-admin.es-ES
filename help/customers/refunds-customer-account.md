---
title: Devoluciones en el panel de cuentas del cliente
description: Los clientes de tienda pueden ver la información de reembolso asociada con el pedido en su panel de cuentas.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/ggaeec6NA2K12-eHl7ESC10nU2u11ihbaxaPlbNAE9I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# Devoluciones en el panel de cuentas del cliente

{{ee-feature}}

Si se ha emitido un reembolso para un pedido, los clientes pueden ver la información de reembolso asociada con el pedido en su panel de cuentas. Si has habilitado la opción [!UICONTROL _Mostrar historial de crédito de la tienda a los clientes_] para la [configuración de crédito de la tienda](../customers/credit-configure.md), los clientes también podrán acceder a su historial de [crédito de la tienda](../customers/store-credit.md).

## Ver un reembolso en la tienda

1. Desde la tienda, el cliente inicia sesión en su cuenta de.

1. Localiza su pedido mediante uno de los siguientes métodos:

   * Encontrando el pedido en la lista de **Pedidos recientes** y haciendo clic en **[!UICONTROL View]**.
   * En el panel izquierdo, elija **[!UICONTROL My Orders]**. A continuación, busque el orden en la lista y haga clic en **[!UICONTROL View]**.

1. El cliente hace clic en la ficha **[!UICONTROL Refunds]** para ver los detalles del reembolso.

   ![Detalle del reembolso en la tienda](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Ver el historial y el saldo de crédito de la tienda en la tienda

Método 1: **Del panel de cuentas del cliente**

1. Desde la tienda, el cliente inicia sesión en su cuenta de.

1. Si la devolución se aplicó al crédito del almacén, elige **[!UICONTROL Store Credit]** en el panel izquierdo.

1. La cantidad reembolsada a su crédito de tienda aparece en la lista con la fecha y hora de la acción.

   ![Importe reembolsado para almacenar crédito](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >La página Crédito de tienda también proporciona un vínculo para que el cliente canjee una [tarjeta regalo](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Método 2: **De la página _Revisión y pagos_**

1. El cliente agrega un producto al carro de compras.

2. Continúa con la página _Cierre de compra_.

3. Pasa el paso **[!UICONTROL Shipping]**.

4. Si hay crédito de tienda disponible, el cliente hace clic en **[!UICONTROL Use Store Credit]**.

   ![Crédito de tienda de la página Revisión y pagos](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Si el cliente cambia de opinión sobre el uso del crédito de la tienda, hace clic en **[!UICONTROL Remove]** en la sección _Resumen de pedidos_.

## Acciones de pago en el administrador

Puedes configurar las acciones de pago para tu [método de pago](../configuration-reference/sales/payment-methods.md) específico. Cada método de pago tiene un conjunto diferente de acciones de pago.

| Acción de pago | Descripción |
|--- |---|
| [!UICONTROL Capture Online] | Cuando se envía la factura, el sistema captura el pago desde la pasarela de pago de terceros. Un usuario administrador puede crear una nota de crédito y anular la factura. |
| [!UICONTROL Capture Offline] | Cuando se envía la factura, el sistema no registra el pago. Se supone que el pago se captura directamente a través de la puerta de enlace y que el pago no se puede capturar a través de Adobe Commerce. Un usuario administrador puede crear una nota de abono, pero no puede anular la factura. (Aunque el pedido utilizó un pago en línea, la factura es esencialmente una factura sin conexión). |
| [!UICONTROL Not Capture] | Cuando se envía la factura, el sistema no registra el pago. Se supone que el pago se captura a través de Adobe Commerce más adelante. Hay un botón [!UICONTROL _Capturar_] en la factura completada. Antes de la captura, puede cancelar la factura. Después de la captura, puede crear una nota de abono y anular la factura. |

{style="table-layout:auto"}

>[!WARNING]
>
>Seleccione la opción [!UICONTROL _No capturar_] a menos que esté seguro de que va a capturar el pago mediante Adobe Commerce más adelante. No puede crear un abono hasta que se haya capturado el pago mediante el botón [!UICONTROL _Capturar_].
