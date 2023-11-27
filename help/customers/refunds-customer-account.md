---
title: Devoluciones en el panel de cuentas del cliente
description: Los clientes de tienda pueden ver la información de reembolso asociada con el pedido en su panel de cuentas.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Devoluciones en el panel de cuentas del cliente

{{ee-feature}}

Si se ha emitido un reembolso para un pedido, los clientes pueden ver la información de reembolso asociada con el pedido en su panel de cuentas. Si ha habilitado la variable [!UICONTROL _Mostrar historial de crédito de la tienda a los clientes_] opción para [Configuración de crédito de tienda](../customers/credit-configure.md), los clientes también pueden acceder a sus [Crédito de tienda](../customers/store-credit.md) historia.

## Ver un reembolso en la tienda

1. Desde la tienda, el cliente inicia sesión en su cuenta de.

1. Localiza su pedido mediante uno de los siguientes métodos:

   * Encontrar el orden en la lista de **Pedidos recientes** y haciendo clic en **[!UICONTROL View]**.
   * En el panel izquierdo, elija **[!UICONTROL My Orders]**. A continuación, busque el orden en la lista y haga clic en **[!UICONTROL View]**.

1. El cliente hace clic en **[!UICONTROL Refunds]** para ver los detalles del reembolso.

   ![Detalles de reembolso en la tienda](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Ver el historial y el saldo de crédito de la tienda en la tienda

Método 1: **Desde el panel de cuentas del cliente**

1. Desde la tienda, el cliente inicia sesión en su cuenta de.

1. Si la devolución se aplicó para almacenar el crédito, elige **[!UICONTROL Store Credit]** en el panel izquierdo.

1. La cantidad reembolsada a su crédito de tienda aparece en la lista con la fecha y hora de la acción.

   ![Importe reembolsado para almacenar el crédito](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >La página Crédito de tienda también proporciona un vínculo para que el cliente canjee un [tarjeta regalo](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Método 2: **Desde el _Revisión y pagos_ página**

1. El cliente agrega un producto al carro de compras.

2. Pasa a la _Finalizar compra_ página.

3. Pasa el **[!UICONTROL Shipping]** paso.

4. Si hay crédito de tienda disponible, el cliente hace clic en **[!UICONTROL Use Store Credit]**.

   ![Crédito de tienda de la página de revisión y pagos](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Si el cliente cambia de opinión sobre el uso del crédito de la tienda, hace clic en **[!UICONTROL Remove]** en el _Resumen de pedidos_ sección.

## Acciones de pago en el administrador

Puede configurar las acciones de pago para sus [Método de pago](../configuration-reference/sales/payment-methods.md). Cada método de pago tiene un conjunto diferente de acciones de pago.

| Acción de pago | Descripción |
|--- |---|
| [!UICONTROL Capture Online] | Cuando se envía la factura, el sistema captura el pago desde la pasarela de pago de terceros. Un usuario administrador puede crear una nota de crédito y anular la factura. |
| [!UICONTROL Capture Offline] | Cuando se envía la factura, el sistema no registra el pago. Se supone que el pago se captura directamente a través de la puerta de enlace y que el pago no se puede capturar a través de Adobe Commerce. Un usuario administrador puede crear una nota de abono, pero no puede anular la factura. (Aunque el pedido utilizó un pago en línea, la factura es esencialmente una factura sin conexión). |
| [!UICONTROL Not Capture] | Cuando se envía la factura, el sistema no registra el pago. Se supone que el pago se captura a través de Adobe Commerce más adelante. Hay un [!UICONTROL _Capture_] botón de la factura completada. Antes de la captura, puede cancelar la factura. Después de la captura, puede crear una nota de abono y anular la factura. |

{style="table-layout:auto"}

>[!WARNING]
>
>Seleccione el [!UICONTROL _No Capturar_] a menos que esté seguro de que va a capturar el pago a través de Adobe Commerce más adelante. No puede crear una nota de abono hasta que el pago se haya capturado utilizando [!UICONTROL _Capture_] botón.
